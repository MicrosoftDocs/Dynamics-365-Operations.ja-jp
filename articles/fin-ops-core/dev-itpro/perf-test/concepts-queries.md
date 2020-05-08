---
title: 承認テスト ライブラリのクエリ
description: このトピックでは承認テスト ライブラリでのクエリの使用法に関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: b53e35f374dc446788ab6563e71ee3eda88fd0bc
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270271"
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
