---
title: リーン生産の転送活動の作成
description: リーン生産の移動活動を作成します。
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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e3c92c5fc9cdba7c77942fae5c32d625cc939f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237921"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="28d2c-103">リーン生産の転送活動の作成</span><span class="sxs-lookup"><span data-stu-id="28d2c-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28d2c-104">リーン生産の移動活動を作成します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="28d2c-105">前提条件:</span><span class="sxs-lookup"><span data-stu-id="28d2c-105">Prerequisites:</span></span> 

1. <span data-ttu-id="28d2c-106">有効ではない生産フローおよびバージョンを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28d2c-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="28d2c-107">配送元と配送先の倉庫と場所を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28d2c-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="28d2c-108">必要に応じて、補充する作業セルまたは補充された作業セルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28d2c-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="28d2c-109">生産フロー バージョンの検索</span><span class="sxs-lookup"><span data-stu-id="28d2c-109">Find the production flow version</span></span>
1. <span data-ttu-id="28d2c-110">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="28d2c-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28d2c-112">生産フローはドラフト ステータスのバージョンが必要なことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="28d2c-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="28d2c-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="28d2c-114">新しい活動の作成</span><span class="sxs-lookup"><span data-stu-id="28d2c-114">Create a new activity</span></span>
1. <span data-ttu-id="28d2c-115">[活動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-115">Click Activities.</span></span>
    * <span data-ttu-id="28d2c-116">選択した生産フローに、ドラフト バージョンがあることを確認し、そのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="28d2c-117">[新しい計画活動の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="28d2c-118">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-118">Click Next.</span></span>
4. <span data-ttu-id="28d2c-119">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="28d2c-120">[活動タイプ] フィールドで、「移動」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="28d2c-121">[処理数量] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="28d2c-122">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="28d2c-123">作業セルの選択</span><span class="sxs-lookup"><span data-stu-id="28d2c-123">Select the Work cells</span></span>
1. <span data-ttu-id="28d2c-124">[補充中] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28d2c-125">転送活動で移動元場所として作業セルの出荷場所を使用するには、作業セルを選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="28d2c-126">転送活動の移動先の場所を設定する、補充する作業セルに対しても同じことが当てはまります。</span><span class="sxs-lookup"><span data-stu-id="28d2c-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="28d2c-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="28d2c-128">在庫更新の定義</span><span class="sxs-lookup"><span data-stu-id="28d2c-128">Define the inventory updates</span></span>
1. <span data-ttu-id="28d2c-129">[製品タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="28d2c-130">転送は製品のタイプを変更しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="28d2c-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="28d2c-131">完成品または半完成製品 (生産フローおよびかんばんフローなど 2 つの活動間の転送) を転送できます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="28d2c-132">完成品を転送すると、在庫トランザクションのピッキングまたは受取結果を選択できます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="28d2c-133">配送場所の定義</span><span class="sxs-lookup"><span data-stu-id="28d2c-133">Define the transfer locations</span></span>
1. <span data-ttu-id="28d2c-134">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-134">Click Next.</span></span>
2. <span data-ttu-id="28d2c-135">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="28d2c-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="28d2c-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="28d2c-138">[場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="28d2c-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="28d2c-140">[配送業者] フィールドで、「荷主」を選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="28d2c-141">次のオプションがあります。荷主 - 出荷倉庫を運営している組織。受取人 - 入荷倉庫を運営している組織。配送業者 - サード パーティの仕入先。</span><span class="sxs-lookup"><span data-stu-id="28d2c-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="28d2c-142">運営組織が仕入先である場合、転送活動には外注契約が必要です。</span><span class="sxs-lookup"><span data-stu-id="28d2c-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="28d2c-143">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="28d2c-144">活動時間の定義</span><span class="sxs-lookup"><span data-stu-id="28d2c-144">Define the activity times</span></span>
1. <span data-ttu-id="28d2c-145">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28d2c-146">ランタイムの定義が必要です。</span><span class="sxs-lookup"><span data-stu-id="28d2c-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="28d2c-147">ランタイムは、かんばん作業の原価およびスループットの時間の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="28d2c-148">ランタイムは最大能力負荷および消費の計算には使用されていません。これは生産フロー バージョンのタスクから導かれるサイクル時間で計算されます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="28d2c-149">[時刻] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="28d2c-150">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="28d2c-151">[時間単位] を選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-151">Select the Time unit.</span></span>
5. <span data-ttu-id="28d2c-152">[数量ごと] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="28d2c-153">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28d2c-154">待ち時間はオプションです。</span><span class="sxs-lookup"><span data-stu-id="28d2c-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="28d2c-155">[時刻] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="28d2c-156">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="28d2c-157">[時間単位] を選択します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-157">Select the Time unit.</span></span>
10. <span data-ttu-id="28d2c-158">[数量ごと] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d2c-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="28d2c-159">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-159">Click Next.</span></span>
12. <span data-ttu-id="28d2c-160">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d2c-160">Click Finish.</span></span>
13. <span data-ttu-id="28d2c-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28d2c-161">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]