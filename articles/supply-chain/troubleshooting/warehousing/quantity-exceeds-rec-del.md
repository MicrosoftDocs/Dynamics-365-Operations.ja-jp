---
title: 更新しようとしている数量が、入庫済/配送済の数量を超えています。
description: 梱包明細を生成すると、出庫積荷には販売注文に対して選択および保存された作業数量を超えた数量が含まれます。
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249133"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="c1699-103">更新しようとしている数量が、入庫済/配送済の数量を超えている場合</span><span class="sxs-lookup"><span data-stu-id="c1699-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="c1699-104">エラーコード: SYS7676</span><span class="sxs-lookup"><span data-stu-id="c1699-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="c1699-105">現象</span><span class="sxs-lookup"><span data-stu-id="c1699-105">Symptoms</span></span>

<span data-ttu-id="c1699-106">梱包明細を生成すると、出庫積荷には販売注文に対して選択および保存された作業数量を超えた数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1699-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="c1699-107">梱包明細を生成しようとすると、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="c1699-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="c1699-108">更新しようとした数量は受入/配送できる数量を超えています。</span><span class="sxs-lookup"><span data-stu-id="c1699-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="c1699-109">したがって、積荷の梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="c1699-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c1699-110">原因</span><span class="sxs-lookup"><span data-stu-id="c1699-110">Cause</span></span>

<span data-ttu-id="c1699-111">作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。</span><span class="sxs-lookup"><span data-stu-id="c1699-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="c1699-112">たとえば、積荷明細行の数量、作成済作業の数量、またはピッキング済数量が正確ではない場合、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c1699-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="c1699-113">解決策</span><span class="sxs-lookup"><span data-stu-id="c1699-113">Resolution</span></span>

<span data-ttu-id="c1699-114">積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="c1699-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="c1699-115">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c1699-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c1699-116">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c1699-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="c1699-117">積荷明細行の数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c1699-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="c1699-118">すべてのピッキング登録を取り消し、ピッキングを再実行します。</span><span class="sxs-lookup"><span data-stu-id="c1699-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="c1699-119">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する</span><span class="sxs-lookup"><span data-stu-id="c1699-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="c1699-120">次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c1699-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="c1699-121">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c1699-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1699-122">発送が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="c1699-123">**積荷明細行** クイックタブで、積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="c1699-124">**作業作成数量** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="c1699-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="c1699-125">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="c1699-126">作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c1699-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="c1699-127">すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c1699-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="c1699-128">積荷明細行の数量を調整する</span><span class="sxs-lookup"><span data-stu-id="c1699-128">Adjust the load line quantity</span></span>

<span data-ttu-id="c1699-129">次の手順を使用して、積荷明細行の数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c1699-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="c1699-130">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c1699-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1699-131">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c1699-132">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="c1699-133"> *\*積荷明細行** タブで、問題の原因となる品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="c1699-134">**ピッキング済数量の削減** を選択して、選択した数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c1699-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="c1699-135">**ピッキング済数量の削減** フィールドが積荷明細行の調整を反映するように設定します。</span><span class="sxs-lookup"><span data-stu-id="c1699-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="c1699-136">すべてのピッキング登録を取り消し、ピッキングを再実行する</span><span class="sxs-lookup"><span data-stu-id="c1699-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="c1699-137">ピッキングの登録を使用して作業なしで積荷明細行をクローズした場合、積荷明細行の数量とピッキング済数量の間に不一致が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1699-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="c1699-138">この場合は、手動ピッキング登録を取り消す必要があります。また Warehouse Management モバイル アプリを使用してピッキングを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1699-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="c1699-139">ピッキング登録を取り消すには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1699-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="c1699-140">**売掛金勘定 \> 注文 \> すべての注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c1699-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="c1699-141">積荷の梱包明細を転記できない販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="c1699-142"> *\*販売注文明細行** タブで、ピッキング登録が実行された販売注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1699-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="c1699-143">**明細行の更新 \> ピッキング** を選択して、品目のピッキングを解除します。</span><span class="sxs-lookup"><span data-stu-id="c1699-143">Select **Update line \> Pick** to unpick the items.</span></span>
