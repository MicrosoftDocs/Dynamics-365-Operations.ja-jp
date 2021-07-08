---
title: 単位の残余現物数量がゼロではない
description: 梱包明細を生成するとき、提供されたデータの在庫数量はゼロではありませんが、販売数量はゼロになります。
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248790"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="c5533-103">単位の残余現物数量がゼロではない</span><span class="sxs-lookup"><span data-stu-id="c5533-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="c5533-104">エラーコード: SYS19591</span><span class="sxs-lookup"><span data-stu-id="c5533-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="c5533-105">現象</span><span class="sxs-lookup"><span data-stu-id="c5533-105">Symptoms</span></span>

<span data-ttu-id="c5533-106">梱包明細を生成するとき、提供されたデータの在庫数量はゼロではありませんが、販売数量はゼロになります。</span><span class="sxs-lookup"><span data-stu-id="c5533-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="c5533-107">梱包明細を生成しようとすると、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="c5533-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="c5533-108">単位 %1 の残余現物数量はゼロ以外でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c5533-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="c5533-109">したがって、積荷の梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="c5533-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c5533-110">原因</span><span class="sxs-lookup"><span data-stu-id="c5533-110">Cause</span></span>

<span data-ttu-id="c5533-111">システムは、在庫単位の残余現物数量と出荷単位の残余現物数量を評価します。</span><span class="sxs-lookup"><span data-stu-id="c5533-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="c5533-112">システムにおいて出荷単位の残余現物数量が 0 (ゼロ) であるが、在庫単位の残余現物数量が 0 でない場合、梱包明細を生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="c5533-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="c5533-113">たとえば、品目の販売単位と在庫単位が異なり、単位間の変換が正確でない場合、この問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="c5533-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5533-114">解決策</span><span class="sxs-lookup"><span data-stu-id="c5533-114">Resolution</span></span>

<span data-ttu-id="c5533-115">積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="c5533-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="c5533-116">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c5533-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c5533-117">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5533-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="c5533-118">積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="c5533-119">積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="c5533-120">在庫単位が販売単位よりも少ないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c5533-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="c5533-121">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認する</span><span class="sxs-lookup"><span data-stu-id="c5533-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="c5533-122">次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5533-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="c5533-123">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5533-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5533-124">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c5533-125">**積荷明細行** クイックタブで、積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="c5533-126">**作業作成数量** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="c5533-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="c5533-127">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="c5533-128">作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5533-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="c5533-129">すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5533-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="c5533-130">積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整する</span><span class="sxs-lookup"><span data-stu-id="c5533-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="c5533-131">次の手順を使用して積荷明細行を確認し、丸め問題なしに数量を正しく変換できるように調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="c5533-132">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5533-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5533-133">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5533-134">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="c5533-135"> *\*積荷明細行** タブで、超過配送を超える品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="c5533-136">**ピッキング済数量の削減** を選択して、選択した数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="c5533-137"> *\*明細行の詳細** タブで、*\*注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="c5533-138">**数量** フィールドをピッキング済数量 (つまり、**作業作成数量** フィールドの値) に設定して、梱包明細の生成が続行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="c5533-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="c5533-139">積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整する</span><span class="sxs-lookup"><span data-stu-id="c5533-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="c5533-140">次の手順を使用して積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="c5533-141">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5533-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5533-142">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5533-143">**積荷明細行** クイックタブで、問題の原因となる品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="c5533-144">**数量** および **単位** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="c5533-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="c5533-145">**組織管理 \> 単位 \> 単位** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5533-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="c5533-146">梱包明細が生成できない単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5533-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5533-147">必要に応じて **小数点以下の精度** フィールドの値を調整します。</span><span class="sxs-lookup"><span data-stu-id="c5533-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="c5533-148">在庫単位が販売単位よりも少ないことを確認する</span><span class="sxs-lookup"><span data-stu-id="c5533-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="c5533-149">在庫単位が販売単位よりも少ないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c5533-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="c5533-150">必要に応じて、品目の単位を再構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5533-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
