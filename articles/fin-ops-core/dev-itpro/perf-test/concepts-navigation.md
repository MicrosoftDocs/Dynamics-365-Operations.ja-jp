---
title: テスト データのナビゲーション概念
description: このトピックでは、ナビゲーションを使用してテスト データ生成メソッドの発見可能性を単純化する方法に関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 99467eb7aa302024c93a1e5fa271e87b205cf997
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680920"
---
# <a name="navigation-concepts-for-test-data"></a>テスト データのナビゲーション概念

[!include [banner](../includes/banner.md)]

テスト データの生成メソッドの発見可能性を単純化するために、一連のナビゲーション オブジェクトが導入されました。 生成メソッドの詳細は [テスト データのメソッド](test-data-methods.md) を参照してください。

ナビゲーションはルート オブジェクトから開始し、モジュールを指定して、そしてエンティティはテスト データ メソッドと一緒に指定する必要があります。

```xpp
data.module().entity().testDataMethod();
```

### <a name="examples"></a>例

```xpp
modelGroup = data.invent().modelGroups().fifo();

itemBuilder = data.products().items().whsBuilder();

data.sales().salesOrders().ensureCanCreate();

data.invent().parameters().enableQualityManagement();
```

### <a name="advantages"></a>メリット

- データ生成アプリケーション プログラミング インターフェイス (API) の発見可能性。 IntelliSense はエンティティに関連するヘルパー メソッドを取得するのに役立ちます。
- 頻繁に使用されるノード (たとえば、`items.whsBuilder()`) へのローカル参照 したがって、長い名前は必要ありません。

## <a name="root-navigation-object"></a>ルート ナビゲーション オブジェクト

ルート ナビゲーション オブジェクトは、必要なテスト データ メソッドを検索するための開始点です。 ルート ナビゲーション オブジェクトは、テスト データ メソッドが定義されているモジュールを公開します。

### <a name="variable-naming"></a>変数の命名

ナビゲーション ルートを参照する変数の推奨される名前は `data` です。

### <a name="class-naming"></a>クラスの命名

`AtlDataRootNode` という名前のルート クラス。

## <a name="module-navigation-object"></a>モジュール ナビゲーション オブジェクト

モジュール ナビゲーション オブジェクトを使用すると、テスト データ メソッドを関連するモジュールごとにグループ化できます。 モジュール ナビゲーション オブジェクトは、エンティティ ナビゲーション オブジェクトを公開できます。

### <a name="navigation-node-naming"></a>ナビゲーション ノードの命名

モジュール名はメイン メニューのモジュール名に基づく必要があります。 ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。

#### <a name="examples"></a>例

- **販売とマーケティング** モジュール: `data.sales()`
- **在庫管理** モジュール: `data.invent()`

### <a name="class-naming"></a>クラスの命名

`AtlData<ModuleName>`

#### <a name="examples"></a>例

- **販売とマーケティング** モジュール: `AtlDataSales`
- **調達** モジュール: `AtlDataPurch`
- **在庫管理** モジュール: `AtlDataInvent`
- **売掛金勘定** モジュール: `AtlDataCust`
- **買掛金勘定** モジュール: `AtlDataVend`

## <a name="entity-navigation-objects"></a>エンティティ ナビゲーション オブジェクト

エンティティ ナビゲーション オブジェクトを使用すると、[テスト データ メソッド](test-data-methods.md) を関連するエンティティごとにグループ化できます。

### <a name="navigation-node-naming"></a>ナビゲーション ノードの命名

エンティティ名の複数形はエンティティ ナビゲーション ノードの名前として使用する必要があります。

#### <a name="examples"></a>例

```xpp
data.products().items();

data.whs().warehouses();
```

### <a name="class-naming"></a>クラスの命名 

`AtlData<ModuleName><EntityNamePlural>`

#### <a name="examples"></a>例

```xpp
AtlDataProductsItems

AtlDataInventChargeGroups
```

### <a name="notes"></a>摘要

このアプローチが役立つ場合、同じエンティティ ナビゲーション オブジェクトを複数のモジュールから公開できます。 たとえば、`AtlDataProductsItems` は `data.product()` と `data.invent()` の両方から公開されます。

## <a name="helper-navigation-objects"></a>ヘルパー ナビゲーション オブジェクト

場合によって、[テスト データ メソッド](test-data-methods.md) はどのエンティティにも固有ではありません。 この場合は、モジュール レベルでヘルパー ノードを公開できます。 

### <a name="navigation-node-naming"></a>ナビゲーション ノードの命名

ヘルパー ナビゲーション ノードは `helpers` という名前にする必要があります。

#### <a name="examples"></a>例

```xpp
data.helpers();

data.whs().helpers();
```

### <a name="class-naming"></a>クラスの命名

`AtlData<ModuleName>Helpers`

#### <a name="examples"></a>例

```xpp
AtlDataHelpers

AtlDataWHSHelpers
```
