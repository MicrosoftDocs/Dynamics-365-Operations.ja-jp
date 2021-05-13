---
title: EventHandlerResult を使用して応答
description: このトピックでは、IEventHandlerResult インターフェイスを実装する任意の型パラメーターを持つイベントをサブスクライブする方法について説明します。
author: LarsBlaaberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 6bc3c530c0d895b267f3abeed6a51a164d14b653
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866250"
---
# <a name="respond-by-using-eventhandlerresult"></a>EventHandlerResult を使用して応答

[!include [banner](../includes/banner.md)]

いくつかのデリゲート メソッドは、デリゲート ハンドラー メソッドのサブスクライブから応答を要求できるように実装されます。 デリゲート呼び出しロジックは、応答の受信後に実行を継続するときに潜在的なサブスクライバからの応答を使用します。 これらのデリゲート メソッドは通常、**EventHandlerResult** パラメーターを最後のパラメーターとして持つシグネチャを持っています。 ただし、**EventHandlerAcceptResult** および **EventHandlerRejectResult** タイプのサポートが原因で、パラメーターは **IEventHandlerResult** インターフェイスを実装する任意のタイプになります。

+ 一般に、デリゲート ハンドラー メソッドに実装されているロジックには、サブスクライブしているロジックが応答の提供を担当していることを検証する条件を含める必要があります。 結果のフォームに応答を提供するロジックも含める必要があります。
+ デリゲート ハンドラー メソッドが **EventHandlerResult** オブジェクト パラメーターへの応答を提供する必要があるとき、サブスクライブするロジックには結果の計算または取得のためのロジックも含まれている場合があります。
+ 条件と応答ロジックが実装されると、条件が **true** と評価されたときのみ、結果の計算を実行する必要があります。
+ すべてのサブスクライブしているデリゲート ハンドラー メソッドはデリゲートが呼び出されたときに実行されます。 したがって、メソッドがレスポンスの提供を担当していない場合は、メソッドを実行する間接費ができるだけ低いことを確認する必要があります。 したがって、デリゲート ハンドラー メソッドが結果を提供する責任を負わない場合、できるだけ早く条件が **false** に評価されていることを確認してください。

## <a name="examples"></a>例
次の例は、**switch** ステートメントの形式の条件を持つデリゲート ハンドラーを示しています。 デリゲート ハンドラーには結果のフォームに応答を提供するロジックがあります。 応答するロジックは、条件が **true** に評価された場合にのみ実行されます。

```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
{
    switch (_inventLocationType)
    {
        case InventLocationType::Standard:
        case InventLocationType::Quarantine:
        case InventLocationType::Transit:
            _result.result(true);
            break;
    }
}
```

デリゲート メソッドが、**EventHandlerAcceptResult** または **EventHandlerRejectResult** オブジェクト パラメーターを使用して、応答を要求するとき、サブスクライバーは、承認または否認でのみ応答することを想定します。 サブスクライブ ロジックは、メッセージを Infolog に追加することもできます。

次の例は、前の例に似ています。 ただし、デリゲート メソッドは、**EventHandlerAcceptResult** オブジェクトの使用によりおよび **受け入れ** メソッドを呼び出すことにより、応答を要求するようになります。
    
```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerAcceptResult _result)
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

次の例では、**EventHandlerRejectResult** オブジェクトを使用して応答するデリゲート ハンドラー メソッドを示しています。 **EventHandlerRejectResult** オブジェクトを使用して応答するには、**reject** メソッドまたは **checkFailed** 拡張メソッドを呼び出します。 **checkFailed** メソッドを使用する場合は、情報ログに警告メッセージを追加できます。 内部的には、**checkFailed** メソッドは **reject** メソッドを呼び出します。

```xpp
[SubscribesTo(classStr(ProdTableType), delegateStr(ProdTableType, validateWriteProdTableInventRefTypeDelegate))]
public static void validateWriteProdTableInventRefTypeDelegateHandler(ProdTable _prodTable, EventHandlerRejectResult _result)
{
    if (_prodTable.InventRefType == InventRefType::ProdLine)
    {
        if (! _prodTable.InventRefId || !_prodTable.InventRefTransId)
        {
            _result.checkFailed("@SYS19558");
        }
        ProdBOM prodBOM;
        select prodBOM
            where prodBOM.InventTransId  == _prodTable.InventRefTransId;
        if (! _prodTable.checkRefProdBOM(prodBOM))
        {
            _result.reject();
        }
    }
}
```

## <a name="guidelines"></a>ガイドライン
前述の実例に加えて、次の一般的なガイドラインが適用されます。

- サブスクライブしているロジックが応答を担当する場合にのみ対応します。 デリゲート ハンドラー メソッドは、特定の条件が満たされたときに応答を提供するために実装されました。 したがって、サブスクライブしているロジックは、特定の条件が満たされた場合に結果を提供する必要があります。 サブスクライブしているロジックが応答する前に、結果オブジェクト パラメーターは既に結果が含まれているかどうかを評価することができません。 たとえば、デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。 このロジックは、メソッド実行時に **EventHandlerResult** オブジェクト パラメーターに結果がすでに含まれているかどうかを評価します。

    > [!WARNING]
    > この例は、書くべきでは **ない** コードの例です。

    ```xpp
    [SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
    public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
    {
        // this if statement is an example of the bad practice.
        if (_result.hasResult())
        {
             return;
        }
        switch (_inventLocationType)
        {
            case InventLocationType::Standard:
            case InventLocationType::Quarantine:
            case InventLocationType::Transit:
                 _result.result(true);
                break;
        }
    }
    ```
    
- 他のサブスクライバーの代理として応答を提供しないでください。 デリゲート ハンドラー メソッドが応答を提供する責任を負わない場合、メソッドは応答を提供できません。 条件が満たされていないときに、メソッドが応答を提供する場合は、他のサブスクライバーに代わって応答を提供しています。 要求元のロジックは、サブスクライバーが応答していない状況を処理する責任を負わなければなりません。 デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。 このロジックは、条件が **false** と評価されたときに結果を提供します。
    
    > [!WARNING]
    > この例は、書くべきでは **ない** コードの例です。
    
    ```xpp
    [SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
    public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
    {
        switch (_inventLocationType)
        {
            case InventLocationType::Standard:
            case InventLocationType::Quarantine:
            case InventLocationType::Transit:
                _result.result(true);
                break;
            // this default block is an example of the bad practice
            default:
                _result.result(false);
                break;
        }
    }
    ```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]