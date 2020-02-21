---
title: 承認テスト ライブラリのベスト プラクティス
description: このトピックは承認テスト ライブラリのベスト プラクティスについて説明します。
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
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 5dcfd0a667bfc0ded7855a6b1deb42d84d18a15e
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033041"
---
# <a name="best-practices-for-the-acceptance-test-library"></a><span data-ttu-id="6ac23-103">承認テスト ライブラリのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="6ac23-103">Best practices for the Acceptance test library</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]


## <a name="use-var-and-declare-variables-inline"></a><span data-ttu-id="6ac23-104">var を使用して変数をインラインで宣言する</span><span class="sxs-lookup"><span data-stu-id="6ac23-104">Use var and declare variables inline</span></span>

+ <span data-ttu-id="6ac23-105">`var` キーワード (型推論) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ac23-105">Use the `var` keyword (type inference).</span></span>
+ <span data-ttu-id="6ac23-106">離れたステートメントではなくインラインで変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="6ac23-106">Declare variables inline instead of in a separate statement.</span></span>

### <a name="do-this"></a><span data-ttu-id="6ac23-107">操作</span><span class="sxs-lookup"><span data-stu-id="6ac23-107">Do this</span></span>

```xpp
var item = items.default(); 
var salesOrder = data.sales().salesOrders().createDefault();
var salesLine = salesOrder.addLine().setItem(item).setInventDims([warehouse]).setQuantity(10).save();
```

### <a name="dont-do-this"></a><span data-ttu-id="6ac23-108">このようにしない</span><span class="sxs-lookup"><span data-stu-id="6ac23-108">Don't do this</span></span>

```xpp
InventTable item; 
AtlEntitySalesOrder salesOrder;
AtlEntitySaleOrderLine salesLine;
…
item = items.default(); 
salesOrder = data.sales().salesOrders().createDefault();
salesLine = salesOrder.addLine().setItem(item).setInventDims([warehouse]).setQuantity(10).save();
```

### <a name="justification"></a><span data-ttu-id="6ac23-109">両端揃え</span><span class="sxs-lookup"><span data-stu-id="6ac23-109">Justification</span></span>

<span data-ttu-id="6ac23-110">`var` を使用する利点は記述するコードを減らし、正確な型名を覚える必要がなく、テストロジックが重要でない情報で散らかっていないことです。</span><span class="sxs-lookup"><span data-stu-id="6ac23-110">The advantages of using `var` are that you write less code, you don't have to remember exact type names, and the test logic isn't cluttered with unimportant information.</span></span> <span data-ttu-id="6ac23-111">全体的にテストコードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="6ac23-111">Overall, the test code easier to read.</span></span>

<span data-ttu-id="6ac23-112">前の例で、`item` が `ItemId`、`InventlTable`、`AtlEntityInventItem` 型かどうかは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="6ac23-112">In the previous example, it doesn't matter whether `item` is of the `ItemId`, `InventlTable`, or `AtlEntityInventItem` type.</span></span> <span data-ttu-id="6ac23-113">重要な詳細は、一般的な既定のアイテムを含む販売明細行を作成しているということです。</span><span class="sxs-lookup"><span data-stu-id="6ac23-113">The important detail is that you're creating a sales line that has a well-known default item.</span></span> <span data-ttu-id="6ac23-114">`salesOrder` や `salesLine` 変数の正確な型は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="6ac23-114">The exact types of the `salesOrder` and `salesLine` variables aren't important.</span></span> <span data-ttu-id="6ac23-115">これらの型の契約は、命名と使用法から明らかです。</span><span class="sxs-lookup"><span data-stu-id="6ac23-115">The contracts of these types are clear from the naming and usage.</span></span>

### <a name="considerations"></a><span data-ttu-id="6ac23-116">注意事項</span><span class="sxs-lookup"><span data-stu-id="6ac23-116">Considerations</span></span>

- <span data-ttu-id="6ac23-117">メソッドの戻り値の型が変わったらコンパイルを失敗させる場合は、型推論を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6ac23-117">Don't use type inference if you want compilation to fail if the return type of a method changes.</span></span>
- <span data-ttu-id="6ac23-118">意味のある変数名やメソッド名を作成できない場合は、型推論を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6ac23-118">Don't use type inference if you can't invent meaningful variable or method names.</span></span>

## <a name="use-entities-instead-of-ids-as-method-parameters"></a><span data-ttu-id="6ac23-119">メソッド パラメータとして ID ではなくエンティティを使用する</span><span class="sxs-lookup"><span data-stu-id="6ac23-119">Use entities instead of IDs as method parameters</span></span>

<span data-ttu-id="6ac23-120">一般的なデータ メソッド、作成者メソッド、および `init` メソッドは、通常 ID の代わりにレコードやエンティティを返します。</span><span class="sxs-lookup"><span data-stu-id="6ac23-120">Well-known data methods, creator methods, and `init` methods usually return records or entities instead of IDs.</span></span> <span data-ttu-id="6ac23-121">メソッドのパラメーターにレコードやエンティティを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6ac23-121">We recommend that you use records or entities as method parameters.</span></span>

### <a name="do-this"></a><span data-ttu-id="6ac23-122">操作</span><span class="sxs-lookup"><span data-stu-id="6ac23-122">Do this</span></span>

```xpp
var salesLine = salesOrder.addLine().setItem(item).save();
```

### <a name="dont-do-this"></a><span data-ttu-id="6ac23-123">このようにしない</span><span class="sxs-lookup"><span data-stu-id="6ac23-123">Don't do this</span></span>

```xpp
var salesLine = salesOrder.addLine().setItemId(item.ItemId).save();
```

### <a name="justification"></a><span data-ttu-id="6ac23-124">両端揃え</span><span class="sxs-lookup"><span data-stu-id="6ac23-124">Justification</span></span>

<span data-ttu-id="6ac23-125">重要ではない専門語が散らばっていないので、コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="6ac23-125">The code is easier to read, because it isn't cluttered with unimportant technicalities.</span></span>

### <a name="considerations"></a><span data-ttu-id="6ac23-126">注意事項</span><span class="sxs-lookup"><span data-stu-id="6ac23-126">Considerations</span></span>

<span data-ttu-id="6ac23-127">ID しかわからない場合は、ID を引数に取るメソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="6ac23-127">If you know only the ID, use the method that takes the ID as an argument.</span></span>

## <a name="use-navigation-node-shortcuts"></a><span data-ttu-id="6ac23-128">ナビゲーション ノードのショートカットを使用する</span><span class="sxs-lookup"><span data-stu-id="6ac23-128">Use navigation node shortcuts</span></span>

<span data-ttu-id="6ac23-129">新しいドメイン領域を自動化するときは、その領域で最も頻繁に使用されるナビゲーション オブジェクトのショートカットを保持する基本クラスを導入します。</span><span class="sxs-lookup"><span data-stu-id="6ac23-129">When you automate a new domain area, introduce a base class that holds shortcuts to the most frequently used navigation objects in that area.</span></span>

<span data-ttu-id="6ac23-130">たとえば、倉庫管理エリアには `AtlWHSTestCase` という名前の基本クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="6ac23-130">For example, for the warehouse management area, there is a base class that is named `AtlWHSTestCase`.</span></span> <span data-ttu-id="6ac23-131">`data.whs()`、`data.invent()`、`data.invent().items()`、`data.invent().units()` そして他のナビゲーション オブジェクトのショートカットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ac23-131">It contains shortcuts to `data.whs()`, `data.invent()`, `data.invent().items()`, `data.invent().units()`, and other navigation objects.</span></span> <span data-ttu-id="6ac23-132">ショートカットはテスト コードを単純にします。</span><span class="sxs-lookup"><span data-stu-id="6ac23-132">The shortcuts simplify your test code.</span></span>

```xpp
class AtlWHSTestCase extends SysTestCase
{
    AtlDataRootNote          data;
    AtlDataInvent            invent;
    AtlDataInventOnHand      onHand;
    AtlDataProductItems      items;
    AtlDataWHS               whs;

    protected void initDataSetupReferences()
    {
        data = new AtlDataRootNode();
        invent = data.invent();
        onHand = data.invent().onHand();
        items = data.invent().items();
        whs = data.whs();
```

<span data-ttu-id="6ac23-133">同じクラスの多くのテスト メソッド間で共有されるショートカットを導入するのも便利です。</span><span class="sxs-lookup"><span data-stu-id="6ac23-133">It also makes sense to introduce shortcuts that are shared among many test methods in the same class.</span></span>

### <a name="do-this"></a><span data-ttu-id="6ac23-134">操作</span><span class="sxs-lookup"><span data-stu-id="6ac23-134">Do this</span></span>

```xpp
class WHSMinMaxReplenishmentScenarioTest extends AtlWHSTestCase
…
    var item = items.default(); 
    var warehouse = invent.warehouses().default(); 
```

### <a name="dont-do-this"></a><span data-ttu-id="6ac23-135">このようにしない</span><span class="sxs-lookup"><span data-stu-id="6ac23-135">Don't do this</span></span>

```xpp
class WHSMinMaxReplenishmentScenarioTest extends SysTestCase
…
    var item = data.invent().items().default(); 
    var warehouse = data.invent().warehouses().default(); 
```

### <a name="considerations"></a><span data-ttu-id="6ac23-136">注意事項</span><span class="sxs-lookup"><span data-stu-id="6ac23-136">Considerations</span></span>

<span data-ttu-id="6ac23-137">必要なナビゲーション ノードすべてにショートカットを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6ac23-137">You don't have to create a shortcut for every navigation node that you need.</span></span> <span data-ttu-id="6ac23-138">ただし、頻繁に使用されるナビゲーション ノードに対してそれらを作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="6ac23-138">However, consider creating them for the navigation nodes that are frequently used.</span></span>
