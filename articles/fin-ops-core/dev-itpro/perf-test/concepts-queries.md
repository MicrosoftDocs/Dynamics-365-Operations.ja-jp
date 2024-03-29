---
title: 承認テスト ライブラリのクエリ
description: この記事では承認テスト ライブラリでのクエリの使用法に関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4053dd6d90336d35ed942f694ce9fde37627bc86
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281698"
---
# <a name="queries-in-the-acceptance-test-library"></a>承認テスト ライブラリのクエリ

[!include [banner](../includes/banner.md)]

クエリ クラスはさまざまな条件に基づいて対応するエンティティのインスタンスを見つけるために使用する Fluent アプリケーション プログラミング インターフェイス (API) を提供します。 クエリ クラスは検証シナリオでよく使用されます。 通常それらは詳細と一緒に使用されます。

## <a name="naming-convention"></a>名前付け規則

`AtlQuery<ModuleName><EntityNamePlural>`

この命名規則で:

- `<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。 ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。
- `<EntityNamePlural>` はエンティティ名の複数形です。

## <a name="examples"></a>例

```xpp
AtlQueryWHSLoadLines

AtlQueryInventTransferOrderLines
```

## <a name="implementation"></a>実装

クエリ クラスは、すべてのクエリに共通の `AtlQuery` クラスから継承します。

## <a name="fluent-setters"></a>Fluent セッター

クエリ クラスは、クエリの範囲を指定するために Fluent セッター メソッドを提供する必要があります。

### <a name="example"></a>例

```xpp
loadLine = data.whs().loadLines().query().forSalesOrder(salesOrder).single();
```

クエリは 2 種類の Fluent セッター メソッドを許可します、`for` メソッドと `with` メソッド:

- **for** – これらのメソッドは構成または集計関係の親として機能するクエリのフィルターに使用されます。 たとえば、販売明細行クエリは、特定の販売注文に対して販売明細行をフィルターする `for` メソッドを公開しています。
- **with** – これらのメソッドはクエリの他のすべての範囲で使用されます。

### <a name="naming-convention"></a>名前付け規則

`for<QueryRangeName>`

`with<QueryRangeName>`

この命名規則では、`<QueryRangeName>` はその範囲が適用されるフィールド名です。

### <a name="examples"></a>例

```xpp
loadLine = data.whs().loadLines().query().forLoad(load).withInventQty(10).single();

transferLine = data.invent().transferOrderLines().query().forTransferOrder(transferOrder).withInventDims([batch1]).single();
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
