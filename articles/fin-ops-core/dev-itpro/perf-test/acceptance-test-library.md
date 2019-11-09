---
title: 承認テスト ライブラリ のリソース
description: このトピックでは承認テスト ライブラリに関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 07/23/2019
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
ms.openlocfilehash: 9f71b1d13d4e2d7ad2507ff9a97e6545ca35d44b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191816"
---
# <a name="acceptance-test-library-resources"></a><span data-ttu-id="8db9b-103">承認テスト ライブラリ のリソース</span><span class="sxs-lookup"><span data-stu-id="8db9b-103">Acceptance test library resources</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8db9b-104">承認テスト ライブラリ (ATL) は、X++ テスト ライブラリであり、以下の利点を提供します:</span><span class="sxs-lookup"><span data-stu-id="8db9b-104">The Acceptance test library (ATL) is an X++ test library that offers the following benefits:</span></span>

- <span data-ttu-id="8db9b-105">一貫したテスト データを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8db9b-105">It lets you create consistent test data.</span></span>
- <span data-ttu-id="8db9b-106">テスト コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="8db9b-106">It increases the readability of test code.</span></span>
- <span data-ttu-id="8db9b-107">テスト データの作成に使用されているメソッドの発見可能性が向上します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-107">It provides improved discoverability of the methods that are used to create test data.</span></span>
- <span data-ttu-id="8db9b-108">前提条件の設定の複雑さを隠します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-108">It hides the complexity of setting up prerequisites.</span></span>
- <span data-ttu-id="8db9b-109">パフォーマンスの高いテスト ケースをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8db9b-109">It supports high performance of test cases.</span></span>

## <a name="example-of-a-test-that-is-written-in-atl"></a><span data-ttu-id="8db9b-110">ATL で記述されたテストの例</span><span class="sxs-lookup"><span data-stu-id="8db9b-110">Example of a test that is written in ATL</span></span>

```
// Create the data root node
var data = AtlDataRootNode::construct();

// Get a reference to a well-known warehouse 
var warehouse = data.invent().warehouses().default();
 
// Create a new item with the "default" setup using the item creator class. Adjust the default warehouse before saving the item.
var item = items.defaultBuilder().setDefaultWarehouse(warehouse).create();

// Add on-hand (information about availability of the item in the warehouse) by using the on-hand adjustment command.
onHand.adjust().forItem(item).forInventDims([warehouse]).setQty(100).execute();

// Create a sales order with one line using the sales order entity
var salesOrder = data.sales().salesOrders().createDefault();
var salesLine = salesOrder.addLine().setItem(item).setQuantity(10).save();

// Reserve 3 units of the item using the reserve() command that is exposed directly on the sales line entity
salesLine.reserve().setQty(3).execute();

// Verify inventory transactions that are associated with the sales line using the inventoryTransactions query and specifications
salesLine.inventoryTransactions().assertExpectedLines(
    invent.trans().spec().withStatusIssue(StatusIssue::OnOrder).withInventDims([warehouse]).withQty(-7),
    invent.trans().spec().withStatusIssue(StatusIssue::ReservPhysical).withInventDims([warehouse]).withQty(-3)); 
```

## <a name="concepts"></a><span data-ttu-id="8db9b-111">概念</span><span class="sxs-lookup"><span data-stu-id="8db9b-111">Concepts</span></span>

<span data-ttu-id="8db9b-112">ATL のクラスとメソッドの構造と命名は非常に厳格です。</span><span class="sxs-lookup"><span data-stu-id="8db9b-112">The structure and naming of the classes and methods in ATL are quite rigid.</span></span> <span data-ttu-id="8db9b-113">この厳格さにより、発見性が向上し、慣れないドメインでさえもテストを簡単に作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8db9b-113">This rigidity helps improve discoverability and also makes it easier to write tests, even in domains that you're unfamiliar with.</span></span>

<span data-ttu-id="8db9b-114">クラスは次の概念に分類されます:</span><span class="sxs-lookup"><span data-stu-id="8db9b-114">The classes are grouped into the following concepts:</span></span>

- <span data-ttu-id="8db9b-115">[ナビゲーション](concepts-navigation.md) – 慣れている階層でエンティティを検出し、データ メソッドをテストします。</span><span class="sxs-lookup"><span data-stu-id="8db9b-115">[Navigation](concepts-navigation.md) – Discover entities and test data methods in a familiar hierarchy.</span></span>
- <span data-ttu-id="8db9b-116">[テスト データ メソッド](test-data-methods.md) – これらのメソッドはテスト データの設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8db9b-116">[Test data methods](test-data-methods.md) – These methods are used to set up test data.</span></span>
- <span data-ttu-id="8db9b-117">[エンティティ](concepts-entities.md) – エンティティは、ひとつの単位として認識されるデータと、それに関連する動作を表します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-117">[Entities](concepts-entities.md) – Entities represent data and associated behavior that is perceived as a single unit.</span></span>
- <span data-ttu-id="8db9b-118">[作成者](concepts-creators.md) – 作成者により特定のテスト データを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8db9b-118">[Creators](concepts-creators.md) – Creators let you create specific test data.</span></span>
- <span data-ttu-id="8db9b-119">[コマンド](concepts-commands.md) – コマンドは事業運営を実行します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-119">[Commands](concepts-commands.md) – Commands run business operations.</span></span>
- <span data-ttu-id="8db9b-120">[クエリ](concepts-queries.md) – クエリはエンティティを検索します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-120">[Queries](concepts-queries.md) – Queries find entities.</span></span>
- <span data-ttu-id="8db9b-121">[仕様](concepts-specifications.md) – 仕様はテストの終わりで期待されるエンティティを説明します。</span><span class="sxs-lookup"><span data-stu-id="8db9b-121">[Specifications](concepts-specifications.md) – Specifications describe expected entities at the end of the test.</span></span>

## <a name="code-generation"></a><span data-ttu-id="8db9b-122">コード生成</span><span class="sxs-lookup"><span data-stu-id="8db9b-122">Code generation</span></span>

<span data-ttu-id="8db9b-123">クエリと仕様は、エンティティの作成プロセスを簡素化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8db9b-123">Queries and specifications help simplify the process of creating entities.</span></span> <span data-ttu-id="8db9b-124">詳細は [承認テスト ライブラリ コード生成ウィザード](code-generation-wizard.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8db9b-124">For more information, see [Acceptance test library Code generation wizard](code-generation-wizard.md).</span></span> <span data-ttu-id="8db9b-125">**コード生成** ウィザードを使用してシナリオを作成し、またそれらを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="8db9b-125">The **Code generation** wizard can be used to create scenarios and update them.</span></span>

## <a name="further-reading"></a><span data-ttu-id="8db9b-126">参考文献</span><span class="sxs-lookup"><span data-stu-id="8db9b-126">Further reading</span></span>

<span data-ttu-id="8db9b-127">何千ものテスト基盤として、Microsoft は ATL を社内で何年も使用してきました。</span><span class="sxs-lookup"><span data-stu-id="8db9b-127">Microsoft has used ATL internally for several years, as the foundation for thousands of tests.</span></span> <span data-ttu-id="8db9b-128">詳細については [承認テスト ライブラリのベスト プラクティス](atl-best-practices.md) および [承認テスト ライブラリについてよく寄せられる質問](atl-faq.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8db9b-128">For more information see, [Best practices for the Acceptance test library](atl-best-practices.md) and [Acceptance test library FAQ](atl-faq.md).</span></span>