---
title: ナビゲーション概念
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
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: c47272f47a38a0e78bd14897e9bfe9873a1e6af6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183095"
---
# <a name="navigation-concepts"></a><span data-ttu-id="34024-103">ナビゲーション概念</span><span class="sxs-lookup"><span data-stu-id="34024-103">Navigation concepts</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="34024-104">テスト データの生成メソッドの発見可能性を単純化するために、一連のナビゲーション オブジェクトが導入されました。</span><span class="sxs-lookup"><span data-stu-id="34024-104">To simplify the discoverability of generation methods for test data, a set of navigation objects is introduced.</span></span> <span data-ttu-id="34024-105">生成メソッドの詳細は [テスト データ生成メソッド](test-data-methods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34024-105">For more information about the generation methods, see [Test data generation methods](test-data-methods.md).</span></span>

<span data-ttu-id="34024-106">ナビゲーションはルート オブジェクトから開始し、モジュールを指定して、そしてエンティティはテスト データ メソッドと一緒に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34024-106">Navigation should start from the root object, the module must be specified, and then the entity must be specified together with the test data methods.</span></span>

```
data.module().entity().testDataMethod();
```

### <a name="examples"></a><span data-ttu-id="34024-107">例</span><span class="sxs-lookup"><span data-stu-id="34024-107">Examples</span></span>

```
modelGroup = data.invent().modelGroups().fifo();

itemBuilder = data.products().items().whsBuilder();

data.sales().salesOrders().ensureCanCreate();

data.invent().parameters().enableQualityManagement();
```

### <a name="advantages"></a><span data-ttu-id="34024-108">メリット</span><span class="sxs-lookup"><span data-stu-id="34024-108">Advantages</span></span>

- <span data-ttu-id="34024-109">データ生成アプリケーション プログラミング インターフェイス (API) の発見可能性。</span><span class="sxs-lookup"><span data-stu-id="34024-109">Discoverability of data creation application programming interfaces (APIs).</span></span> <span data-ttu-id="34024-110">IntelliSense はエンティティに関連するヘルパー メソッドを取得するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="34024-110">IntelliSense helps you get to the helper methods that are relevant for the entity.</span></span>
- <span data-ttu-id="34024-111">頻繁に使用されるノード (たとえば、`items.whsBuilder()`) へのローカル参照</span><span class="sxs-lookup"><span data-stu-id="34024-111">Local references to frequently used nodes (for example, `items.whsBuilder()`).</span></span> <span data-ttu-id="34024-112">したがって、長い名前は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="34024-112">Therefore, long names aren't required.</span></span>

## <a name="root-navigation-object"></a><span data-ttu-id="34024-113">ルート ナビゲーション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="34024-113">Root navigation object</span></span>

<span data-ttu-id="34024-114">ルート ナビゲーション オブジェクトは、必要なテスト データ メソッドを検索するための開始点です。</span><span class="sxs-lookup"><span data-stu-id="34024-114">The root navigation object is the starting point for finding the test data methods that are required.</span></span> <span data-ttu-id="34024-115">ルート ナビゲーション オブジェクトは、テスト データ メソッドが定義されているモジュールを公開します。</span><span class="sxs-lookup"><span data-stu-id="34024-115">The root navigation object exposes modules where test data methods are defined.</span></span>

### <a name="variable-naming"></a><span data-ttu-id="34024-116">変数の命名</span><span class="sxs-lookup"><span data-stu-id="34024-116">Variable naming</span></span>

<span data-ttu-id="34024-117">ナビゲーション ルートを参照する変数の推奨される名前は `data` です。</span><span class="sxs-lookup"><span data-stu-id="34024-117">The suggested name for variables that reference the navigation root is `data`.</span></span>

### <a name="class-naming"></a><span data-ttu-id="34024-118">クラスの命名</span><span class="sxs-lookup"><span data-stu-id="34024-118">Class naming</span></span>

<span data-ttu-id="34024-119">`AtlDataRootNode` という名前のルート クラス。</span><span class="sxs-lookup"><span data-stu-id="34024-119">The root class is named `AtlDataRootNode`.</span></span>

## <a name="module-navigation-object"></a><span data-ttu-id="34024-120">モジュール ナビゲーション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="34024-120">Module navigation object</span></span>

<span data-ttu-id="34024-121">モジュール ナビゲーション オブジェクトを使用すると、テスト データ メソッドを関連するモジュールごとにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="34024-121">The module navigation objects let you group test data methods by relevant modules.</span></span> <span data-ttu-id="34024-122">モジュール ナビゲーション オブジェクトは、エンティティ ナビゲーション オブジェクトを公開できます。</span><span class="sxs-lookup"><span data-stu-id="34024-122">Module navigation objects can expose entity navigation objects.</span></span>

### <a name="navigation-node-naming"></a><span data-ttu-id="34024-123">ナビゲーション ノードの命名</span><span class="sxs-lookup"><span data-stu-id="34024-123">Navigation node naming</span></span>

<span data-ttu-id="34024-124">モジュール名はメイン メニューのモジュール名に基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="34024-124">Module names should be based on the names of the modules on the main menu.</span></span> <span data-ttu-id="34024-125">ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34024-125">However, a short version or an abbreviation should be used to support brevity of test code.</span></span>

#### <a name="examples"></a><span data-ttu-id="34024-126">例</span><span class="sxs-lookup"><span data-stu-id="34024-126">Examples</span></span>

- <span data-ttu-id="34024-127">**販売とマーケティング** モジュール: `data.sales()`</span><span class="sxs-lookup"><span data-stu-id="34024-127">**Sales and marketing** module: `data.sales()`</span></span>
- <span data-ttu-id="34024-128">**在庫管理** モジュール: `data.invent()`</span><span class="sxs-lookup"><span data-stu-id="34024-128">**Inventory management** module: `data.invent()`</span></span>

### <a name="class-naming"></a><span data-ttu-id="34024-129">クラスの命名</span><span class="sxs-lookup"><span data-stu-id="34024-129">Class naming</span></span>

`AtlData<ModuleName>`

#### <a name="examples"></a><span data-ttu-id="34024-130">例</span><span class="sxs-lookup"><span data-stu-id="34024-130">Examples</span></span>

- <span data-ttu-id="34024-131">**販売とマーケティング** モジュール: `AtlDataSales`</span><span class="sxs-lookup"><span data-stu-id="34024-131">**Sales and marketing** module: `AtlDataSales`</span></span>
- <span data-ttu-id="34024-132">**調達** モジュール: `AtlDataPurch`</span><span class="sxs-lookup"><span data-stu-id="34024-132">**Procurement and sourcing** module: `AtlDataPurch`</span></span>
- <span data-ttu-id="34024-133">**在庫管理** モジュール: `AtlDataInvent`</span><span class="sxs-lookup"><span data-stu-id="34024-133">**Inventory management** module: `AtlDataInvent`</span></span>
- <span data-ttu-id="34024-134">**売掛金勘定** モジュール: `AtlDataCust`</span><span class="sxs-lookup"><span data-stu-id="34024-134">**Accounts receivable** module: `AtlDataCust`</span></span>
- <span data-ttu-id="34024-135">**買掛金勘定** モジュール: `AtlDataVend`</span><span class="sxs-lookup"><span data-stu-id="34024-135">**Accounts payable** module: `AtlDataVend`</span></span>

## <a name="entity-navigation-objects"></a><span data-ttu-id="34024-136">エンティティ ナビゲーション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="34024-136">Entity navigation objects</span></span>

<span data-ttu-id="34024-137">エンティティ ナビゲーション オブジェクトを使用すると、[テスト データ メソッド](test-data-methods.md) を関連するエンティティごとにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="34024-137">Entity navigation objects let you group [test data methods](test-data-methods.md) by relevant entities.</span></span>

### <a name="navigation-node-naming"></a><span data-ttu-id="34024-138">ナビゲーション ノードの命名</span><span class="sxs-lookup"><span data-stu-id="34024-138">Navigation node naming</span></span>

<span data-ttu-id="34024-139">エンティティ名の複数形はエンティティ ナビゲーション ノードの名前として使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34024-139">The plural of the entity name should be used as the name of the entity navigation node.</span></span>

#### <a name="examples"></a><span data-ttu-id="34024-140">例</span><span class="sxs-lookup"><span data-stu-id="34024-140">Examples</span></span>

```
data.products().items();

data.whs().warehouses();
```

### <a name="class-naming"></a><span data-ttu-id="34024-141">クラスの命名</span><span class="sxs-lookup"><span data-stu-id="34024-141">Class naming</span></span> 

`AtlData<ModuleName><EntityNamePlural>`

#### <a name="examples"></a><span data-ttu-id="34024-142">例</span><span class="sxs-lookup"><span data-stu-id="34024-142">Examples</span></span>

```
AtlDataProductsItems

AtlDataInventChargeGroups
```

### <a name="notes"></a><span data-ttu-id="34024-143">摘要</span><span class="sxs-lookup"><span data-stu-id="34024-143">Notes</span></span>

<span data-ttu-id="34024-144">このアプローチが役立つ場合、同じエンティティ ナビゲーション オブジェクトを複数のモジュールから公開できます。</span><span class="sxs-lookup"><span data-stu-id="34024-144">The same entity navigation object can be exposed from multiple modules when this approach makes sense.</span></span> <span data-ttu-id="34024-145">たとえば、`AtlDataProductsItems` は `data.product()` と `data.invent()` の両方から公開されます。</span><span class="sxs-lookup"><span data-stu-id="34024-145">For example, `AtlDataProductsItems` is exposed from both `data.product()` and `data.invent()`.</span></span>

## <a name="helper-navigation-objects"></a><span data-ttu-id="34024-146">ヘルパー ナビゲーション オブジェクト</span><span class="sxs-lookup"><span data-stu-id="34024-146">Helper navigation objects</span></span>

<span data-ttu-id="34024-147">場合によって、[テスト データ メソッド](test-data-methods.md) はどのエンティティにも固有ではありません。</span><span class="sxs-lookup"><span data-stu-id="34024-147">Sometimes, a [test data method](test-data-methods.md) isn't specific to any entity.</span></span> <span data-ttu-id="34024-148">この場合は、モジュール レベルでヘルパー ノードを公開できます。</span><span class="sxs-lookup"><span data-stu-id="34024-148">In this case, a helpers node can be exposed at the module level.</span></span> 

### <a name="navigation-node-naming"></a><span data-ttu-id="34024-149">ナビゲーション ノードの命名</span><span class="sxs-lookup"><span data-stu-id="34024-149">Navigation node naming</span></span>

<span data-ttu-id="34024-150">ヘルパー ナビゲーション ノードは `helpers` という名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="34024-150">The helpers navigation node should be named `helpers`.</span></span>

#### <a name="examples"></a><span data-ttu-id="34024-151">例</span><span class="sxs-lookup"><span data-stu-id="34024-151">Examples</span></span>

```
data.helpers();

data.whs().helpers();
```

### <a name="class-naming"></a><span data-ttu-id="34024-152">クラスの命名</span><span class="sxs-lookup"><span data-stu-id="34024-152">Class naming</span></span>

`AtlData<ModuleName>Helpers`

#### <a name="examples"></a><span data-ttu-id="34024-153">例</span><span class="sxs-lookup"><span data-stu-id="34024-153">Examples</span></span>

```
AtlDataHelpers

AtlDataWHSHelpers
```
