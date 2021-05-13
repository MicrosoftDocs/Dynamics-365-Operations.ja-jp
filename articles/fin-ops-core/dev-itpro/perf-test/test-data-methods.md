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
ms.openlocfilehash: 16000b172bfbb7c354716dcd32059683f5b78341
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866138"
---
# <a name="test-data-methods"></a><span data-ttu-id="754a3-103">テスト データ メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-103">Test data methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="754a3-104">エンティティやヘルパー ナビゲーション オブジェクトは、テスト データを設定するテスト メソッドを公開します。</span><span class="sxs-lookup"><span data-stu-id="754a3-104">Entity and helper navigation objects expose test methods that let you set up test data.</span></span> <span data-ttu-id="754a3-105">このトピックでは、最も一般的な種類のテスト データ メソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="754a3-105">This topic provides information about the most common types of test data methods.</span></span>

## <a name="factory-methods"></a><span data-ttu-id="754a3-106">ファクトリ メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-106">Factory methods</span></span>

<span data-ttu-id="754a3-107">ファクトリ メソッドはデータベースにまだ存在しないデータの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="754a3-107">Factory methods focus on creating data that doesn't yet exist in the database.</span></span> <span data-ttu-id="754a3-108">エンティティ ファクトリ メソッドには 2 つのタイプがあります、`init` メソッドと `create` メソッド。</span><span class="sxs-lookup"><span data-stu-id="754a3-108">There are two types of entity factory methods, `init` methods and `create` methods.</span></span> <span data-ttu-id="754a3-109">`init` メソッドはエンティティを初期化しますがデータベースに保存しません。</span><span class="sxs-lookup"><span data-stu-id="754a3-109">An `init` method initializes the entity but doesn't save it to the database.</span></span> <span data-ttu-id="754a3-110">`create` メソッドはエンティティを初期化して、そしてデータベースに保存します。</span><span class="sxs-lookup"><span data-stu-id="754a3-110">A `create` method initializes the entity and saves it to the database.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-111">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-111">Naming convention</span></span>

`init<EntitySpecification>`

`create<EntitySpecification>`

<span data-ttu-id="754a3-112">この命名規則で、`<EntitySpecification>` は作成する必要があるオブジェクトの重要な特性の説明です。</span><span class="sxs-lookup"><span data-stu-id="754a3-112">In this naming convention, `<EntitySpecification>` is the description of the key characteristics of the object that must be created.</span></span>

### <a name="examples"></a><span data-ttu-id="754a3-113">例</span><span class="sxs-lookup"><span data-stu-id="754a3-113">Examples</span></span>

```xpp
salesOrder = data.sales().salesOrders().initDefault();

purchaseOrder = data.purch().purchaseOrders().createDefault();
```

### <a name="best-practices"></a><span data-ttu-id="754a3-114">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="754a3-114">Best practices</span></span>

<span data-ttu-id="754a3-115">`create` メソッドは、同じエンティティ仕様を持つ `init` メソッドを常に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-115">The `create` method should always call the `init` method that has the same entity specification.</span></span>

#### <a name="example"></a><span data-ttu-id="754a3-116">例</span><span class="sxs-lookup"><span data-stu-id="754a3-116">Example</span></span>

```xpp
public AtlEntitySalesOrder createDefault()
{
    AtlEntitySalesOrder salesOrder = this.initDefault();
    salesOrder.save();
    return salesOrder;
}
```

### <a name="prerequisite-data"></a><span data-ttu-id="754a3-117">前提条件データ</span><span class="sxs-lookup"><span data-stu-id="754a3-117">Prerequisite data</span></span>

<span data-ttu-id="754a3-118">`init` メソッドは前提条件の設定を処理します。</span><span class="sxs-lookup"><span data-stu-id="754a3-118">The `init` method should take care of setting up prerequisites.</span></span>

<span data-ttu-id="754a3-119">なにかエンティティを作成する前に、特定の前提条件を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-119">Before some entities can be created, specific prerequisites must be set up.</span></span> <span data-ttu-id="754a3-120">そのような場合、エンティティが初期化される前に `ensure` メソッドが呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-120">In these cases, the `ensure` method must be called before the entity is initialized.</span></span> <span data-ttu-id="754a3-121">また、前提条件の自動設定を必要とする、すべてのエンティティ イベントを購読する必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-121">You must also subscribe to all the entity events that require automatic setup of prerequisites.</span></span>

#### <a name="example"></a><span data-ttu-id="754a3-122">例</span><span class="sxs-lookup"><span data-stu-id="754a3-122">Example</span></span>

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

## <a name="builder-methods"></a><span data-ttu-id="754a3-123">ビルダー メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-123">Builder methods</span></span>

<span data-ttu-id="754a3-124">ビルダー メソッドは、データベースにまだ存在しないデータを作成するために使用される、作成者オブジェクトの初期化を行います。</span><span class="sxs-lookup"><span data-stu-id="754a3-124">Builder methods are responsible for initializing creator objects that will be used to create data that doesn't yet exist in the database.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-125">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-125">Naming convention</span></span>

`<EntitySpecification>Builder`

<span data-ttu-id="754a3-126">この命名規則で、`<EntitySpecification>` は作成する必要があるオブジェクトの重要な特性の説明です。</span><span class="sxs-lookup"><span data-stu-id="754a3-126">In this naming convention, `<EntitySpecification>` is the description of the key characteristics of the object that must be created.</span></span>

### <a name="example"></a><span data-ttu-id="754a3-127">例</span><span class="sxs-lookup"><span data-stu-id="754a3-127">Example</span></span>

```xpp
catchWeightItem = data.invent().items().cwBuilder();
```

## <a name="well-known-data-methods"></a><span data-ttu-id="754a3-128">一般的なデータ メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-128">Well-known data methods</span></span>

<span data-ttu-id="754a3-129">よく使われるデータ メソッドは、特定の方法で設定されたエンティティを参照する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="754a3-129">Well-known data methods provide a way to reference an entity that is set up in a specific way.</span></span> <span data-ttu-id="754a3-130">エンティティがデータベースに存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="754a3-130">If the entity doesn't exist in the database, it's created.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-131">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-131">Naming convention</span></span>

`<EntitySpecification>`

<span data-ttu-id="754a3-132">この命名規則で、`<EntitySpecification>` は取得する必要があるオブジェクトの重要な特性の説明です。</span><span class="sxs-lookup"><span data-stu-id="754a3-132">In this naming convention, `<EntitySpecification>` is the description of the key characteristics of the object that must be retrieved.</span></span>

### <a name="example"></a><span data-ttu-id="754a3-133">例</span><span class="sxs-lookup"><span data-stu-id="754a3-133">Example</span></span>

```xpp
fifo = data.invent().modelGroup().fifo();
```

<span data-ttu-id="754a3-134">この例でメソッドの契約は、在庫モデルとしてモデル グループが先入れ先出し (FIFO) を使用するよう指定します。</span><span class="sxs-lookup"><span data-stu-id="754a3-134">In this example, the contract of the method specifies that the model group should use first in, first out (FIFO) as the inventory model.</span></span> <span data-ttu-id="754a3-135">その他の設定は既定値のままにできます。</span><span class="sxs-lookup"><span data-stu-id="754a3-135">The rest of the settings can be left at their default values.</span></span>

<span data-ttu-id="754a3-136">場合によっては、実際の名前が契約をより理解しやすくします。</span><span class="sxs-lookup"><span data-stu-id="754a3-136">Sometimes, a real-world name communicates the contract better.</span></span>

```xpp
pieces = data.common().units().pieces();
```

<span data-ttu-id="754a3-137">この例では **個数** が "数量" クラスの測定単位であり、小数点以下の桁数が 0 (ゼロ) であることが明らかです。</span><span class="sxs-lookup"><span data-stu-id="754a3-137">In this example, it's clear that **pieces** is a unit of measure of the "quantity" class, and that is has a decimal precision of 0 (zero).</span></span>

### <a name="contract-of-well-known-data-methods"></a><span data-ttu-id="754a3-138">一般的なデータ メソッドの契約</span><span class="sxs-lookup"><span data-stu-id="754a3-138">Contract of well-known data methods</span></span>

<span data-ttu-id="754a3-139">一般的なデータ メソッドの共通契約について、いくつか覚える必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-139">Here are a few things to remember about the common contract of the well-known data methods.</span></span>

- <span data-ttu-id="754a3-140">同じ一般的なデータ メソッドを 2 回呼び出すと、同じエンティティへの参照を呼び出し元に提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-140">Two calls to the same well-known data method should provide the caller with the reference to the same entity.</span></span>

    ```xpp
    fifo1 = data.invent().modelGroups().fifo();
    fifo2 = data.invent().modelGroups().fifo();
    fifo1.InventModelGroupId == fifo2.InventModelGroupId;
    ```

- <span data-ttu-id="754a3-141">テスト エンティティの作成はいつも努力に値するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="754a3-141">Creation of a test entity isn't always worth the effort.</span></span> <span data-ttu-id="754a3-142">テスト エンティティが作成されない場合は、対応するレコード バッファが一般的なデータ メソッドから返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-142">If a test entity isn't created, the corresponding record buffer should be returned from the well-known data method.</span></span> <span data-ttu-id="754a3-143">たとえば、サイト エンティティの作成に時間と労力を費やさなければ、`site` の一般的なデータ メソッドは InventSite レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="754a3-143">For example, if you don't invest the time and effort to create the Site entity, the `site` well-known data method will return InventSite records.</span></span>

    ```xpp
    InventSite site = data.invent().sites().default();
    ```

- <span data-ttu-id="754a3-144">このアプローチが理にかなっている場合、一般的なデータ メソッドは ID をオプション パラメータとして取ることができます。</span><span class="sxs-lookup"><span data-stu-id="754a3-144">Well-known data methods can take IDs as optional parameters when this approach makes sense.</span></span>

    ```xpp
    item1 = data.products().items().default('Item1');
    item2 = data.products().items().default('item2');
    ```

### <a name="implementation"></a><span data-ttu-id="754a3-145">実装</span><span class="sxs-lookup"><span data-stu-id="754a3-145">Implementation</span></span>

<span data-ttu-id="754a3-146">`<EntitySpecification>` という名前のビルダーまたはファクトリ メソッドがすでに存在する場合、一般的なエンティティを作成するには内部実装としてそれを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-146">If there is already a builder or a factory method that is named `<EntitySpecification>`, it should be used as the internal implementation to create the well-known entity.</span></span>

#### <a name="example"></a><span data-ttu-id="754a3-147">例</span><span class="sxs-lookup"><span data-stu-id="754a3-147">Example</span></span>

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

## <a name="ensure-methods"></a><span data-ttu-id="754a3-148">確認メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-148">Ensure methods</span></span>

<span data-ttu-id="754a3-149">確認メソッドは、エンティティを作成したり事業運営を実行するために必要な前提条件の設定を処理します。</span><span class="sxs-lookup"><span data-stu-id="754a3-149">Ensure methods are responsible for setting up prerequisites that are required in order to create an entity or run a business operation.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-150">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-150">Naming convention</span></span>

`ensureCan<ExecuteBusinessOperation>`

<span data-ttu-id="754a3-151">この命名規則で `<ExecuteBusinessOperation>` は事業運営を表す動詞です。</span><span class="sxs-lookup"><span data-stu-id="754a3-151">In this naming convention, `<ExecuteBusinessOperation>` is a verb that describes the business operation.</span></span>

### <a name="examples"></a><span data-ttu-id="754a3-152">例</span><span class="sxs-lookup"><span data-stu-id="754a3-152">Examples</span></span>

```xpp
data.sales().salesOrders().ensureCanCreate();

data.purch().purchaseOrders().ensureCanPostProductReceipt();
```

### <a name="implementation"></a><span data-ttu-id="754a3-153">実装</span><span class="sxs-lookup"><span data-stu-id="754a3-153">Implementation</span></span>

<span data-ttu-id="754a3-154">請求書の転記など、複雑な事業運営のための前提条件の把握は複雑になる可能性があり、機能分野に関する多くの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="754a3-154">Figuring out prerequisites for a complex business operation, such as invoice posting, can be complicated and requires lots of knowledge about the feature area.</span></span>

#### <a name="example"></a><span data-ttu-id="754a3-155">例</span><span class="sxs-lookup"><span data-stu-id="754a3-155">Example</span></span>

```xpp
public void ensureCanCreate()
{
    data.helpers().setNumberSequenceReference(extendedTypeNum(InventDimId));
}
```

#### <a name="automatic-prerequisite-setup"></a><span data-ttu-id="754a3-156">自動前提条件設定</span><span class="sxs-lookup"><span data-stu-id="754a3-156">Automatic prerequisite setup</span></span>

<span data-ttu-id="754a3-157">自動前提条件設定を有効にするには、適切な `init` メソッドで `ensure` メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-157">To enable automatic prerequisite setup, you must call the `ensure` methods in the appropriate `init` method.</span></span> <span data-ttu-id="754a3-158">詳細については、このトピックで前述した [ファクトリ メソッド](#factory-methods) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="754a3-158">For more information, see the [Factory methods](#factory-methods) section earlier in this topic.</span></span>

## <a name="query-methods"></a><span data-ttu-id="754a3-159">クエリ メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-159">Query methods</span></span>

<span data-ttu-id="754a3-160">クエリ メソッドは、定義されているナビゲーション ノードのエンティティ タイプの、新しいクエリの初期化を処理します。</span><span class="sxs-lookup"><span data-stu-id="754a3-160">Query methods are responsible for initializing new queries for the entity type of the navigation node that they are defined on.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-161">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-161">Naming convention</span></span>

`query`

### <a name="examples"></a><span data-ttu-id="754a3-162">例</span><span class="sxs-lookup"><span data-stu-id="754a3-162">Examples</span></span>

```xpp
loadLinesQuery = data.whs().loadLines().query();

purchaseLinesQuery = data.invent().transferOrderLines().query();
```

## <a name="specification-methods"></a><span data-ttu-id="754a3-163">詳細メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-163">Specification methods</span></span>

<span data-ttu-id="754a3-164">詳細メソッドは、定義されているナビゲーション ノードのエンティティ タイプの、新しい詳細オブジェクトの初期化を処理します。</span><span class="sxs-lookup"><span data-stu-id="754a3-164">Specification methods are responsible for initializing new specification objects for the entity type of the navigation node that they are defined on.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-165">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-165">Naming convention</span></span>

`spec`

### <a name="example"></a><span data-ttu-id="754a3-166">例</span><span class="sxs-lookup"><span data-stu-id="754a3-166">Example</span></span>

```xpp
loadLinesSpec = data.whs().loadLines().spec();
```

## <a name="find-methods"></a><span data-ttu-id="754a3-167">検索メソッド</span><span class="sxs-lookup"><span data-stu-id="754a3-167">Find methods</span></span>

<span data-ttu-id="754a3-168">検索メソッドによって主キーに基づくエンティティを検索できます。</span><span class="sxs-lookup"><span data-stu-id="754a3-168">Find methods let you find an entity based on the primary key.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="754a3-169">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="754a3-169">Naming convention</span></span>

`find`

### <a name="example"></a><span data-ttu-id="754a3-170">例</span><span class="sxs-lookup"><span data-stu-id="754a3-170">Example</span></span>

```xpp
salesOrder = data.sales().salesOrders().find(salesOrderId);
```

### <a name="automatic-prerequisite-setup"></a><span data-ttu-id="754a3-171">自動前提条件設定</span><span class="sxs-lookup"><span data-stu-id="754a3-171">Automatic prerequisite setup</span></span>

<span data-ttu-id="754a3-172">エンティティがクエリ サポートを持っている場合、実装は既に前提条件サポートを設定しているクエリを使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-172">If the entity has query support, the implementation should use the query that has already set up prerequisite support.</span></span> <span data-ttu-id="754a3-173">それ以外の場合は、レコード バッファを検索してエンティティの新しいインスタンスを初期化した後で、エンティティの事業運営イベントに `ensure` メソッドを購読する必要があります。</span><span class="sxs-lookup"><span data-stu-id="754a3-173">Otherwise, after you find the record buffer and initialize the new instance of the entity, you should subscribe `ensure` methods to the business operation events of the entity.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]