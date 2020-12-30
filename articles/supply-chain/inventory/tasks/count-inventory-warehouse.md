---
title: 倉庫の在庫棚卸
description: このトピックでは、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを示します。
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432230"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="4773d-103">倉庫の在庫棚卸</span><span class="sxs-lookup"><span data-stu-id="4773d-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4773d-104">このトピックでは、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="4773d-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="4773d-105">この手順は、倉庫管理モジュールで使用できる倉庫機能ではなく、在庫管理モジュールで使用できる "基本倉庫" 機能に該当します。</span><span class="sxs-lookup"><span data-stu-id="4773d-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="4773d-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="4773d-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="4773d-107">独自のデータを使用する場合は、製品および場所を設定してあること、および棚卸仕訳帳用の在庫仕訳帳名を作成したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4773d-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="4773d-108">通常、在庫棚卸は倉庫の従業員が実行します。</span><span class="sxs-lookup"><span data-stu-id="4773d-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="4773d-109">在庫棚卸仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="4773d-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="4773d-110">**ナビゲーション ウィンドウ > モジュール > 在庫管理 > 仕訳入力 > 品目棚卸 > 棚卸** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4773d-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="4773d-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-111">Select **New**.</span></span>
3. <span data-ttu-id="4773d-112">**名前** フィールドで、ドロップダウン リストから使用する在庫棚卸仕訳帳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="4773d-113">他の一部のフィールドは、選択した在庫棚卸仕訳帳名の設定に基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="4773d-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="4773d-114">**作業者** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4773d-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4773d-115">一覧で、使用する作業者を **選択** します。</span><span class="sxs-lookup"><span data-stu-id="4773d-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="4773d-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="4773d-117">仕訳帳明細行を作成します</span><span class="sxs-lookup"><span data-stu-id="4773d-117">Create journal lines</span></span>
1. <span data-ttu-id="4773d-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-118">Select **New**.</span></span>
2. <span data-ttu-id="4773d-119">**品目番号** フィールドで、ドロップダウン リストから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="4773d-120">デモ データの会社 USMF を使用している場合は、**A0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="4773d-121">**サイト** フィールドで、ドロップダウン リストから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="4773d-122">デモ データの会社 USMF を使用している場合は、サイト **2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="4773d-123">**倉庫** フィールドで、ドロップダウン リストから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="4773d-124">デモ データの会社 USMF を使用している場合は、倉庫 **24** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="4773d-125">**場所** フィールドで、ドロップダウン リストから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="4773d-126">デモ データの会社 USMF を使用している場合は、場所 **BULK-001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="4773d-127">[カウント済] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4773d-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="4773d-128">**手持在庫** フィールドに表示されている数値と異なるカウント済数を入力すると、**数量** フィールドが更新されて差異が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4773d-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="4773d-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="4773d-130">在庫棚卸仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="4773d-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="4773d-131">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-131">Select **Post**.</span></span> <span data-ttu-id="4773d-132">在庫棚卸仕訳帳を転記する際に、カウントした量が **手持在庫** フィールドで報告されている量と異なる場合は、在庫入庫または在庫払出が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4773d-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="4773d-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="4773d-134">在庫トランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="4773d-134">View inventory transactions</span></span>
1. <span data-ttu-id="4773d-135">**在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="4773d-136">**トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4773d-136">Select **Transactions**.</span></span> <span data-ttu-id="4773d-137">ここで、在庫棚卸仕訳帳を転記するときに作成されるすべての関連トランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="4773d-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

