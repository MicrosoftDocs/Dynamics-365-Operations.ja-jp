---
title: リーン生産のプロセス活動の作成
description: リーン生産のプロセス活動を作成します。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc93f3f696f470d7e2f174bd3342f0877e0b4e74
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212161"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="87ced-103">リーン生産のプロセス活動の作成</span><span class="sxs-lookup"><span data-stu-id="87ced-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87ced-104">リーン生産のプロセス活動を作成します。</span><span class="sxs-lookup"><span data-stu-id="87ced-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="87ced-105">前提条件:</span><span class="sxs-lookup"><span data-stu-id="87ced-105">Prerequisites:</span></span> 

1. <span data-ttu-id="87ced-106">有効ではない生産フローおよびバージョンを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87ced-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="87ced-107">作業セルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87ced-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="87ced-108">生産フロー バージョンの検索</span><span class="sxs-lookup"><span data-stu-id="87ced-108">Find the production flow version</span></span>
1. <span data-ttu-id="87ced-109">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="87ced-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="87ced-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="87ced-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="87ced-112">新しい活動の作成</span><span class="sxs-lookup"><span data-stu-id="87ced-112">Create a new activity</span></span>
1. <span data-ttu-id="87ced-113">[活動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-113">Click Activities.</span></span>
    * <span data-ttu-id="87ced-114">選択した生産フローに、ドラフト バージョンがあることを確認し、そのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="87ced-115">[新しい計画活動の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="87ced-116">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-116">Click Next.</span></span>
4. <span data-ttu-id="87ced-117">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="87ced-118">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="87ced-119">すべてのバージョンにおいて、指定された生産フローに対する名前は一意にする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="87ced-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="87ced-120">[処理数量] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="87ced-121">処理される作業数量にかかわらず、これが人件費を計算する作業ごとの最小数量であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="87ced-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="87ced-122">作業の数量がこの数量から逸脱すると、人件費の差異が作成されます。</span><span class="sxs-lookup"><span data-stu-id="87ced-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="87ced-123">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="87ced-124">作業セルの選択</span><span class="sxs-lookup"><span data-stu-id="87ced-124">Select the work cell</span></span>
1. <span data-ttu-id="87ced-125">[作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="87ced-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="87ced-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="87ced-127">在庫更新の定義</span><span class="sxs-lookup"><span data-stu-id="87ced-127">Define the inventory updates</span></span>
1. <span data-ttu-id="87ced-128">[入庫時に手持在庫を更新] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="87ced-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="87ced-129">[手持在庫の更新] = [いいえ] である場合、半完成品の製品を入庫する活動を定義できます (その活動は次の BOM レベルには達しません)。</span><span class="sxs-lookup"><span data-stu-id="87ced-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="87ced-130">半完成の製品の消費も選択できます。</span><span class="sxs-lookup"><span data-stu-id="87ced-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="87ced-131">ピッキング活動の定義</span><span class="sxs-lookup"><span data-stu-id="87ced-131">Define the picking activities</span></span>
1. <span data-ttu-id="87ced-132">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-132">Click Next.</span></span>
2. <span data-ttu-id="87ced-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="87ced-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="87ced-134">既定のピッキング活動は、選択された作業セルの入庫場所に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="87ced-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="87ced-135">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-135">Click Add.</span></span>
    * <span data-ttu-id="87ced-136">作業セルの入力活動がステージ完了になっていない、特定の製品の追加のピッキング活動を作成できます。</span><span class="sxs-lookup"><span data-stu-id="87ced-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="87ced-137">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="87ced-138">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="87ced-139">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="87ced-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="87ced-140">この定義により、活動で消費されたすべての材料は、既定の入庫場所、および 2 番目のピッキング活動で定義された品目を除外する場所からピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="87ced-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="87ced-141">この品目は、別の倉庫および場所からピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="87ced-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="87ced-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="87ced-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="87ced-144">[仕損の登録] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="87ced-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="87ced-145">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="87ced-146">活動時間の定義</span><span class="sxs-lookup"><span data-stu-id="87ced-146">Define the activity times</span></span>
1. <span data-ttu-id="87ced-147">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="87ced-148">ランタイムの定義が必要です。</span><span class="sxs-lookup"><span data-stu-id="87ced-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="87ced-149">ランタイムは、かんばん作業の原価およびスループットの時間の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="87ced-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="87ced-150">ランタイムは最大能力負荷および消費の計算には使用されていません。これは生産フロー バージョンのタスクから導かれるサイクル時間で計算されます。</span><span class="sxs-lookup"><span data-stu-id="87ced-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="87ced-151">[時刻] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="87ced-152">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="87ced-153">[時間単位] を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-153">Select the Time unit.</span></span>
5. <span data-ttu-id="87ced-154">[数量ごと] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="87ced-155">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="87ced-156">待ち時間はオプションです。</span><span class="sxs-lookup"><span data-stu-id="87ced-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="87ced-157">[時刻] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="87ced-158">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="87ced-159">[時間単位] を選択します。</span><span class="sxs-lookup"><span data-stu-id="87ced-159">Select the Time unit.</span></span>
10. <span data-ttu-id="87ced-160">[数量ごと] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87ced-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="87ced-161">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-161">Click Next.</span></span>
12. <span data-ttu-id="87ced-162">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87ced-162">Click Finish.</span></span>
13. <span data-ttu-id="87ced-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87ced-163">Close the page.</span></span>

