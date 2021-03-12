---
title: プロセス製造向けの生産ジョブの順序付け
description: この手順では、色と梱包サイズの優先順位に従って計画オーダーを配列する方法を示す 1 例として、塗料製品が使用されます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981063"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="13865-103">プロセス製造向けの生産ジョブの順序付け</span><span class="sxs-lookup"><span data-stu-id="13865-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13865-104">この手順では、色と梱包サイズの優先順位に従って計画オーダーを配列する方法を示す 1 例として、塗料製品が使用されます。</span><span class="sxs-lookup"><span data-stu-id="13865-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="13865-105">この手順の作成に使用するデモ データの会社は USPI です。</span><span class="sxs-lookup"><span data-stu-id="13865-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="13865-106">この手順は、生産の計画者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="13865-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="13865-107">USPI のマスター プランを実行します。</span><span class="sxs-lookup"><span data-stu-id="13865-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="13865-108">[マスター プラン] > [マスター プラン] > [実行] > [マスター プラン] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13865-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="13865-109">[マスター プラン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="13865-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="13865-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13865-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="13865-111">マスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="13865-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="13865-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13865-112">Click OK.</span></span>
    * <span data-ttu-id="13865-113">これは、順序のプロセスを含むマスター プランを開始します。</span><span class="sxs-lookup"><span data-stu-id="13865-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="13865-114">このプロセスには数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="13865-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="13865-115">塗料製品の計画オーダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="13865-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="13865-116">[マスター プラン] > [マスタープラン] > [計画オーダー]　の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13865-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="13865-117">情報ボックスで品目の詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="13865-118">情報ボックスでスケジュールの詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="13865-119">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="13865-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="13865-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="13865-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="13865-121">マスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="13865-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="13865-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13865-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="13865-123">クイック フィルターを使用して、'P300' の値で品目番号フィールドにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="13865-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="13865-124">右へスクロールしてロック解除すると、注文日と配送日を確認できます。</span><span class="sxs-lookup"><span data-stu-id="13865-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="13865-125">これらの品目が今日の注文日であることと、計画オーダーの出荷日が製品名に示す色や梱包サイズの優先順位後に配列されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="13865-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="13865-126">品目番号をポイントすると、製品名と優先順位を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="13865-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="13865-127">塗料の順序付き計画オーダー</span><span class="sxs-lookup"><span data-stu-id="13865-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="13865-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="13865-128">Close the page.</span></span>
2. <span data-ttu-id="13865-129">[マスター プラン] > [マスター プラン] > [順序付き計画オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13865-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="13865-130">情報ボックスで品目の詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="13865-131">情報ボックスでスケジュールの詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="13865-132">注記: ここでは、計画オーダーの開始日/開始時刻が 28 日間のバケット期間内に色と梱包サイズに従って配列されていることが分かります。</span><span class="sxs-lookup"><span data-stu-id="13865-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="13865-133">これらの期間はフィールド キャンペーンの数によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="13865-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="13865-134">順序付き計画オーダーのフォームは一般的な計画オーダー フォームと同様に動作し、生産計画担当者は、ここで計画オーダーを確定できます。</span><span class="sxs-lookup"><span data-stu-id="13865-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="13865-135">すべての行をマークします。</span><span class="sxs-lookup"><span data-stu-id="13865-135">Mark all rows.</span></span>
6. <span data-ttu-id="13865-136">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13865-136">Click Accept.</span></span>
    * <span data-ttu-id="13865-137">これは、選択した順序のアクションを含む計画オーダーを延期するか、または繰り上げるかについて更新します。</span><span class="sxs-lookup"><span data-stu-id="13865-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="13865-138">計画オーダーの順序を確認します。</span><span class="sxs-lookup"><span data-stu-id="13865-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="13865-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="13865-139">Close the page.</span></span>
2. <span data-ttu-id="13865-140">[マスター プラン] > [マスタープラン] > [計画オーダー]　の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13865-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="13865-141">情報ボックスで品目の詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="13865-142">情報ボックスでスケジュールの詳細を展開します。</span><span class="sxs-lookup"><span data-stu-id="13865-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="13865-143">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="13865-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="13865-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="13865-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="13865-145">マスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="13865-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="13865-146">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="13865-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="13865-147">クイック フィルターを使用して、'P300' の値で品目番号フィールドにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="13865-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="13865-148">今の注文が、色やサイズの優先順位に従って配列されていないと、計画オーダーが最も早い注文日付および配送日で開始することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="13865-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="13865-149">スケジュールの詳細情報ボックスの注文日付列、または開始日を検証します。</span><span class="sxs-lookup"><span data-stu-id="13865-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

