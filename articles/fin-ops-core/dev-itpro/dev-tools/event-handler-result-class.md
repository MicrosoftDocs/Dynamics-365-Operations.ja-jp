---
title: 要求または応答シナリオの EventHandlerResult クラス
description: このトピックでは、デリゲート メソッドで EventHandlerResult クラスを使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.assetid: 3b2a9b85-f779-4358-b347-7b11a8e7960c
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10ced7ee0961b2af1a60ade7da641fb1430afa62
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408968"
---
# <a name="eventhandlerresult-classes-in-request-or-response-scenarios"></a>要求または応答シナリオの EventHandlerResult クラス

[!include [banner](../includes/banner.md)]

デリゲート メソッドとデリゲート ハンドラー メソッドは、デリゲート呼び出しロジックがサブスクライバに応答を要求する要求/応答シナリオをサポートするために宣言することができます。 このシナリオをサポートするために、**EventHandlerResult** クラスがパラメーターとして渡されることが最も多く、デリゲート ハンドラー メソッドがクラスの result メソッドの 1 つを使用して結果を提供します。 ただし、**EventHandlerResult** クラスは単一の結果のみを含むため、複数のサブスクライバが個々の結果を提供する場合は、最後の回答者が獲得し、前のサブスクライバからの結果が上書きされます。

このトピックで説明されている機能が導入される前 (プラットフォーム更新プログラム 5) は、最大でも単一のサブスクライバーが結果を提供し、複数のサブスクライバーが存在すると結果が失われないことを保証するメカニズムはありませんでした。

## <a name="ensuring-at-most-one-response"></a>最大で 1 つの応答を確認

プラットフォーム更新プログラム 5 では、1 つ以上のサブスクライバーが結果を提示している場合にロジックが失敗することを確認する追加の静的コンストラクターが、**EventHandlerResult** クラスにあります。 新しいコンストラクターの名前は、**newSingleResponse**。 このメソッドを使用して **EventHandlerResult** オブジェクトをインスタンス化したとき、2 番目のデリゲート ハンドラー メソッドが結果を提供しようとすると、このフレームワークはただちに例外をスローします。

```xpp
EventHandlerResult result = EventHandlerResult::newSingleResponse();
this.validateWarehouseTypeDelegate(this.WarehouseType, result);
```

## <a name="ieventhandlerresultvalidator-interface"></a>IEventHandlerResultValidator インターフェイス

**EventHandlerResult** クラスの検証は、**IEventHandlerResultValidator** インターフェイスを実装するタイプのオブジェクトを挿入することで処理されます。 **newSingleResponse** 静的コンストラクターを使用して **EventHandlerResult** オブジェクトをインスタンス化するとき、**EventHandlerSingleResponseValidator** オブジェクトがインスタンス化されて **EventHandlerResult** オブジェクトに挿入され、その挿入されたオブジェクトが **EventhandlerResult** オブジェクトに提供される結果の検証を担当します。 他の検証クラスは、クラスで **IEventHandlerResultValidator** インターフェイスを実装することにより実装され、**newWithResultValidator** という別の新しい静的コンストラクターを使って **EventHandlerResult** オブジェクトをインスタンス化することにより **EventHandlerResult** クラスに挿入できます。 コンストラクターは、**IEventHandlerResultValidator** 型の引数をとります。これにより **IEventHandlerResultValidator** インターフェイスを実装している限り、任意の検証オブジェクトを挿入できます。

たとえば、**newSingleResponse** 静的コンストラクターは単にインスタンス化を **newWithResultValidator** 静的コンストラクターに委任し、次のようになります。

```xpp
return EventHandlerResult::newWithResultValidator(EventHandlerSingleResponseValidator::construct());
```

## <a name="accept-and-reject-requestresponse-scenarios"></a>要求/応答シナリオを承認して拒否する

特定の要求/応答シナリオでは、サブスクライバーは承認または拒否を提示することのみ期待されます。 サブスクライバーがブール値での応答のみを期待している場合、受入/拒否の要求に **EventHandlerResult** クラスを使用することは分かりにくい可能性があります。 たとえば、検証シナリオで、検証が失敗した場合にサブスクライバーはブール値 false でのみ応答すべきか、また検証が成功した場合にサブスクライバーがブール値 true で応答すべきかがあります。 **EventHandlerResult** オブジェクトを使用して応答が収集される場合、第二のサブスクライバーが true のブール値で検証し、応答すると、第一サブスクライバーの false のブール値が上書きされる可能性があります。

この混乱を軽減するために、**EventHandlerAcceptResult** と **EventHandlerRejectResult** の 2 つの新しい結果型クラスがプラットフォーム更新プログラム 5 に導入されました。

**EventHandlerAcceptResult** クラスを使用するとき、デリゲート ハンドラー メソッドは **承認** メソッドの呼び出しによってのみ応答できます。 **EventHandlerRejectResult** クラスを使用するとき、**否認** メソッドのみを呼び出すことができます。

```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(
    InventLocationType _inventLocationType, 
    EventHandlerAcceptResult _result)
{
    switch (_inventLocationType)
    {
        case InventLocationType::Standard: 
        case InventLocationType::Quarantine: 
        case InventLocationType::Transit: 
            _result.accept(); 
            break; 
    }     
}
```

2 つの新しいクラスには、最大で 1 つのサブスクライバーが拒否または承認で応答するシナリオで使用するための **newSingleResponse** 静的コンストラクターも含まれています。 いずれかのサブスクライバーが応答したかどうかは **hasResult** メソッドをクエリすることによってまだ回答できます。承認/否認は、**EventHandlerAcceptResult** および **EventHandlerRejectResult** クラスの **isAccepted** または **isRejected** のいずれかのメソッドをそれぞれ呼び出すことによってクエリされます。

```xpp
boolean ret = false;
EventHandlerAcceptResult result = EventHandlerAcceptResult::newSingleResponse(); 
this.validateWarehouseTypeDelegate(this.WarehouseType, result);
if (result.hasResult())
{
    ret = result.isAccepted();
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]