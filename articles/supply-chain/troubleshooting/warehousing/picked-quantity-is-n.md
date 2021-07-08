---
title: 梱包明細の生成中に、ピッキング済数量が十分ではない
description: 梱包明細を生成すると、出庫積荷に、積荷明細行で作成された作業数量と一致しないピッキング済数量が含まれます。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249132"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="43fb1-103">梱包明細の生成中に、ピッキング済数量が十分ではない</span><span class="sxs-lookup"><span data-stu-id="43fb1-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="43fb1-104">エラーコード: SYS54073</span><span class="sxs-lookup"><span data-stu-id="43fb1-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="43fb1-105">現象</span><span class="sxs-lookup"><span data-stu-id="43fb1-105">Symptoms</span></span>

<span data-ttu-id="43fb1-106">梱包明細を生成すると、出庫積荷に、積荷明細行で作成された作業数量と一致しないピッキング済数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="43fb1-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="43fb1-107">梱包明細を生成しようとすると、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="43fb1-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="43fb1-108">%1 がピッキングされているため、残余が %3 である場合は、%2 を更新できません。</span><span class="sxs-lookup"><span data-stu-id="43fb1-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="43fb1-109">したがって、積荷の梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="43fb1-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="43fb1-110">原因</span><span class="sxs-lookup"><span data-stu-id="43fb1-110">Cause</span></span>

<span data-ttu-id="43fb1-111">次のいずれかの条件が存在する可能性があるため、現在の状態では梱包明細を生成することができません:</span><span class="sxs-lookup"><span data-stu-id="43fb1-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="43fb1-112">関連する作業がまだ選択されていないので、最終的な出荷場所に移動されていません。</span><span class="sxs-lookup"><span data-stu-id="43fb1-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="43fb1-113">作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。</span><span class="sxs-lookup"><span data-stu-id="43fb1-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="43fb1-114">積荷明細行の数量、作業作成数量、およびピッキング済数量が一致しません。</span><span class="sxs-lookup"><span data-stu-id="43fb1-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="43fb1-115">解決策</span><span class="sxs-lookup"><span data-stu-id="43fb1-115">Resolution</span></span>

<span data-ttu-id="43fb1-116">積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="43fb1-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="43fb1-117">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="43fb1-118">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="43fb1-119">積荷明細行の数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="43fb1-120">すべてのピッキング登録を取り消し、ピッキングを再実行します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="43fb1-121">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する</span><span class="sxs-lookup"><span data-stu-id="43fb1-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="43fb1-122">次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="43fb1-123">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="43fb1-124">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="43fb1-125">**積荷明細行** クイックタブで、積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="43fb1-126">**作業作成数量** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="43fb1-127">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="43fb1-128">作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="43fb1-129">すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="43fb1-130">積荷明細行の数量を調整する</span><span class="sxs-lookup"><span data-stu-id="43fb1-130">Adjust the load line quantity</span></span>

<span data-ttu-id="43fb1-131">次の手順を使用して、積荷明細行の数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="43fb1-132">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="43fb1-133">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="43fb1-134">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="43fb1-135"> *\*積荷明細行** タブで、問題の原因となる品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="43fb1-136">**ピッキング済数量の削減** を選択して、選択した数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="43fb1-137">**ピッキング済数量の削減** フィールドが積荷明細行の調整を反映するように設定します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="43fb1-138">すべてのピッキング登録を取り消し、ピッキングを再実行する</span><span class="sxs-lookup"><span data-stu-id="43fb1-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="43fb1-139">ユーザーがピッキング登録を使用し、作業なしで積荷明細行をクローズすることにより、問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="43fb1-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="43fb1-140">この場合は、手動ピッキング登録を取り消す必要があります。また Warehouse Management モバイル アプリを使用してピッキングを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43fb1-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="43fb1-141">ピッキング登録を取り消すには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="43fb1-142">**売掛金勘定 \> 注文 \> すべての注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="43fb1-143">積荷の梱包明細を転記できない販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="43fb1-144"> *\*販売注文明細行** タブで、ピッキング登録が実行された販売注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="43fb1-145">**明細行の更新 \> ピッキング** を選択して、品目のピッキングを解除します。</span><span class="sxs-lookup"><span data-stu-id="43fb1-145">Select **Update line \> Pick** to unpick the items.</span></span>
