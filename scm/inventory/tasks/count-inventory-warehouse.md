---
title: "倉庫の在庫棚卸"
description: "この手順では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="bb369-103">倉庫の在庫棚卸</span><span class="sxs-lookup"><span data-stu-id="bb369-103">Count inventory in a warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb369-104">この手順では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="bb369-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="bb369-105">この手順は、倉庫管理モジュールで使用できる倉庫機能ではなく、在庫管理モジュールで使用できる "基本倉庫" 機能に該当します。</span><span class="sxs-lookup"><span data-stu-id="bb369-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="bb369-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="bb369-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="bb369-107">独自のデータを使用する場合は、製品および場所を設定してあること、および棚卸仕訳帳用の在庫仕訳帳名を作成したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bb369-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="bb369-108">通常、在庫棚卸は倉庫の従業員が実行します。</span><span class="sxs-lookup"><span data-stu-id="bb369-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="bb369-109">在庫棚卸仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="bb369-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="bb369-110">[在庫管理] > [仕訳入力] > [品目棚卸] > [棚卸] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="bb369-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-111">Click New.</span></span>
3. <span data-ttu-id="bb369-112">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bb369-113">一覧で、使用する在庫棚卸仕訳帳の名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="bb369-114">他の一部のフィールドは、選択した在庫棚卸仕訳帳名の設定に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="bb369-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="bb369-115">[作業者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bb369-116">一覧で、使用する作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="bb369-117">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-117">Click Select.</span></span>
8. <span data-ttu-id="bb369-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="bb369-119">仕訳帳明細行の作成</span><span class="sxs-lookup"><span data-stu-id="bb369-119">Create journal lines</span></span>
1. <span data-ttu-id="bb369-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-120">Click New.</span></span>
2. <span data-ttu-id="bb369-121">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bb369-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb369-123">デモ データの会社 USMF を使用する場合は、'A0001' を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="bb369-124">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bb369-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb369-126">デモ データの会社 USMF を使用する場合は、サイト '2' を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="bb369-127">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bb369-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb369-129">デモ データの会社 USMF を使用する場合は、倉庫 '24' を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="bb369-130">[場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb369-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bb369-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb369-132">デモ データの会社 USMF を使用する場合は、場所 'BULK-001' を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb369-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="bb369-133">[カウント済] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb369-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="bb369-134">[手持在庫] フィールドに表示されている数値と異なるカウント済数を入力すると [数量] フィールドが更新されて差異が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb369-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="bb369-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="bb369-136">在庫棚卸仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="bb369-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="bb369-137">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-137">Click Post.</span></span>
    * <span data-ttu-id="bb369-138">在庫棚卸仕訳帳を転記する際に、カウントした量が [手持在庫] フィールドで報告されている量と異なる場合は、在庫入庫または在庫払出が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="bb369-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="bb369-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="bb369-140">在庫トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="bb369-140">View inventory transactions</span></span>
1. <span data-ttu-id="bb369-141">[在庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-141">Click Inventory.</span></span>
2. <span data-ttu-id="bb369-142">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb369-142">Click Transactions.</span></span>
    * <span data-ttu-id="bb369-143">ここで、在庫棚卸仕訳帳を転記するときに作成されるすべての関連トランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="bb369-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   
