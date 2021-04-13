---
title: テスト データ メソッド
description: このトピックでは、最も一般的な種類のテスト データ メソッドについて説明します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 1ed969ac0edc297b3ae2be243106a02f4c89621c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745147"
---
# <a name="test-data-methods"></a>テスト データ メソッド

[!include [banner](../includes/banner.md)]

エンティティやヘルパー ナビゲーション オブジェクトは、テスト データを設定するテスト メソッドを公開します。 このトピックでは、最も一般的な種類のテスト データ メソッドについて説明します。

## <a name="factory-methods"></a>ファクトリ メソッド

ファクトリ メソッドはデータベースにまだ存在しないデータの作成に重点を置きます。 エンティティ ファクトリ メソッドには 2 つのタイプがあります、`init` メソッドと `create` メソッド。 `init` メソッドはエンティティを初期化しますがデータベースに保存しません。 `create` メソッドはエンティティを初期化して、そしてデータベースに保存します。

### <a name="naming-convention"></a>名前付け規則

`init<EntitySpecification>`

`create<EntitySpecification>`

この命名規則で、`<EntitySpecification>` は作成する必要があるオブジェクトの重要な特性の説明です。

### <a name="examples"></a>例

```xpp
salesOrder = data.sales().salesOrders().initDefault();

purchaseOrder = data.purch().purchaseOrders().createDefault();
```

### <a name="best-practices"></a>ベスト プラクティス

`create` メソッドは、同じエンティティ仕様を持つ `init` メソッドを常に呼び出す必要があります。

#### <a name="example"></a>例

```xpp
public AtlEntitySalesOrder createDefault()
{
    AtlEntitySalesOrder salesOrder = this.initDefault();
    salesOrder.save();
    return salesOrder;
}
```

### <a name="prerequisite-data"></a>前提条件データ

`init` メソッドは前提条件の設定を処理します。

なにかエンティティを作成する前に、特定の前提条件を設定する必要があります。 そのような場合、エンティティが初期化される前に `ensure` メソッドが呼び出される必要があります。 また、前提条件の自動設定を必要とする、すべてのエンティティ イベントを購読する必要があります。

#### <a name="example"></a>例

```xpp
public AtlEntitySalesOrder initDefault()
{
    AtlEntitySalesOrder salesOrder;

    this.ensureCanCreate();

    salesOrder = new AtlEntitySalesOrder();
    salesOrder.parmCustomer(data.cust().customers().default());

    _salesOrder.postingInvoice += eventhandler(this.ensureCanPostInvoice);
    _salesOrder.postingPackingSlip += eventhandler(this.ensureCanPostPackingSlip);
    _salesOrder.releasingToWarehouse += eventhandler(this.ensureCanReleaseToWarehouse);
}
```

## <a name="builder-methods"></a>ビルダー メソッド

ビルダー メソッドは、データベースにまだ存在しないデータを作成するために使用される、作成者オブジェクトの初期化を行います。

### <a name="naming-convention"></a>名前付け規則

`<EntitySpecification>Builder`

この命名規則で、`<EntitySpecification>` は作成する必要があるオブジェクトの重要な特性の説明です。

### <a name="example"></a>例

```xpp
catchWeightItem = data.invent().items().cwBuilder();
```

## <a name="well-known-data-methods"></a>一般的なデータ メソッド

よく使われるデータ メソッドは、特定の方法で設定されたエンティティを参照する方法を提供します。 エンティティがデータベースに存在しない場合は作成します。

### <a name="naming-convention"></a>名前付け規則

`<EntitySpecification>`

この命名規則で、`<EntitySpecification>` は取得する必要があるオブジェクトの重要な特性の説明です。

### <a name="example"></a>例

```xpp
fifo = data.invent().modelGroup().fifo();
```

この例でメソッドの契約は、在庫モデルとしてモデル グループが先入れ先出し (FIFO) を使用するよう指定します。 その他の設定は既定値のままにできます。

場合によっては、実際の名前が契約をより理解しやすくします。

```xpp
pieces = data.common().units().pieces();
```

この例では **個数** が "数量" クラスの測定単位であり、小数点以下の桁数が 0 (ゼロ) であることが明らかです。

### <a name="contract-of-well-known-data-methods"></a>一般的なデータ メソッドの契約

一般的なデータ メソッドの共通契約について、いくつか覚える必要があります。

- 同じ一般的なデータ メソッドを 2 回呼び出すと、同じエンティティへの参照を呼び出し元に提供する必要があります。

    ```xpp
    fifo1 = data.invent().modelGroups().fifo();
    fifo2 = data.invent().modelGroups().fifo();
    fifo1.InventModelGroupId == fifo2.InventModelGroupId;
    ```

- テスト エンティティの作成はいつも努力に値するとは限りません。 テスト エンティティが作成されない場合は、対応するレコード バッファが一般的なデータ メソッドから返される必要があります。 たとえば、サイト エンティティの作成に時間と労力を費やさなければ、`site` の一般的なデータ メソッドは InventSite レコードを返します。

    ```xpp
    InventSite site = data.invent().sites().default();
    ```

- このアプローチが理にかなっている場合、一般的なデータ メソッドは ID をオプション パラメータとして取ることができます。

    ```xpp
    item1 = data.products().items().default('Item1');
    item2 = data.products().items().default('item2');
    ```

### <a name="implementation"></a>実装

`<EntitySpecification>` という名前のビルダーまたはファクトリ メソッドがすでに存在する場合、一般的なエンティティを作成するには内部実装としてそれを使用する必要があります。

#### <a name="example"></a>例

```xpp
public InventTable whsBatchAbove(ItemId _itemId = this.whsBatchAboveItemId())
{
    InventTable whsItem = InventTable::find(_itemId, true);
    if (!whsItem)
    {
        whsItem = this.whsBatchAboveBuilder().setItemId(_itemId).create();
    }
    return whsItem;
}
```

## <a name="ensure-methods"></a>確認メソッド

確認メソッドは、エンティティを作成したり事業運営を実行するために必要な前提条件の設定を処理します。

### <a name="naming-convention"></a>名前付け規則

`ensureCan<ExecuteBusinessOperation>`

この命名規則で `<ExecuteBusinessOperation>` は事業運営を表す動詞です。

### <a name="examples"></a>例

```xpp
data.sales().salesOrders().ensureCanCreate();

data.purch().purchaseOrders().ensureCanPostProductReceipt();
```

### <a name="implementation"></a>実装

請求書の転記など、複雑な事業運営のための前提条件の把握は複雑になる可能性があり、機能分野に関する多くの知識が必要です。

#### <a name="example"></a>例

```xpp
public void ensureCanCreate()
{
    data.helpers().setNumberSequenceReference(extendedTypeNum(InventDimId));
}
```

#### <a name="automatic-prerequisite-setup"></a>自動前提条件設定

自動前提条件設定を有効にするには、適切な `init` メソッドで `ensure` メソッドを呼び出す必要があります。 詳細については、このトピックで前述した [ファクトリ メソッド](#factory-methods) セクションを参照してください。

## <a name="query-methods"></a>クエリ メソッド

クエリ メソッドは、定義されているナビゲーション ノードのエンティティ タイプの、新しいクエリの初期化を処理します。

### <a name="naming-convention"></a>名前付け規則

`query`

### <a name="examples"></a>例

```xpp
loadLinesQuery = data.whs().loadLines().query();

purchaseLinesQuery = data.invent().transferOrderLines().query();
```

## <a name="specification-methods"></a>詳細メソッド

詳細メソッドは、定義されているナビゲーション ノードのエンティティ タイプの、新しい詳細オブジェクトの初期化を処理します。

### <a name="naming-convention"></a>名前付け規則

`spec`

### <a name="example"></a>例

```xpp
loadLinesSpec = data.whs().loadLines().spec();
```

## <a name="find-methods"></a>検索メソッド

検索メソッドによって主キーに基づくエンティティを検索できます。

### <a name="naming-convention"></a>名前付け規則

`find`

### <a name="example"></a>例

```xpp
salesOrder = data.sales().salesOrders().find(salesOrderId);
```

### <a name="automatic-prerequisite-setup"></a>自動前提条件設定

エンティティがクエリ サポートを持っている場合、実装は既に前提条件サポートを設定しているクエリを使う必要があります。 それ以外の場合は、レコード バッファを検索してエンティティの新しいインスタンスを初期化した後で、エンティティの事業運営イベントに `ensure` メソッドを購読する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]