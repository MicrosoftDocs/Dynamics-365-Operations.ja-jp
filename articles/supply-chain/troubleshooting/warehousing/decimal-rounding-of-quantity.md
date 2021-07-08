---
title: 物理的な更新数量の 10 進数の丸めが正しくありません
description: 梱包明細を生成すると、出庫積荷に単位で定義された小数点以下の精度と一致しない数量が含まれます。
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248791"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="cd7a2-103">物理的な更新数量の 10 進数の丸めが正しくありません</span><span class="sxs-lookup"><span data-stu-id="cd7a2-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="cd7a2-104">エラーコード: SYS19589</span><span class="sxs-lookup"><span data-stu-id="cd7a2-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="cd7a2-105">現象</span><span class="sxs-lookup"><span data-stu-id="cd7a2-105">Symptoms</span></span>

<span data-ttu-id="cd7a2-106">梱包明細を生成すると、出庫積荷に単位で定義された小数点以下の精度と一致しない数量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="cd7a2-107">梱包明細を生成しようとすると、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="cd7a2-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="cd7a2-108">単位 %1 の更新現物数量の小数の丸めが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="cd7a2-109">したがって、積荷の梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cd7a2-110">原因</span><span class="sxs-lookup"><span data-stu-id="cd7a2-110">Cause</span></span>

<span data-ttu-id="cd7a2-111">システムでは、出荷数量の 10 進数の丸めが出荷単位に定義されている小数点以下の精度に対応するかどうかが評価されます。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="cd7a2-112">システムにより出荷数量を指定した 10 進数の桁数に丸めたときに、丸め出荷数量が実際の出荷数量と一致しない場合は、梱包明細を生成できません。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="cd7a2-113">たとえば、販売数量が 1.75 キログラム (kg) で、小数点以下の精度が *1* に設定されている場合にこの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="cd7a2-114">解決策</span><span class="sxs-lookup"><span data-stu-id="cd7a2-114">Resolution</span></span>

<span data-ttu-id="cd7a2-115">積荷または出荷は現在、梱包明細の生成に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="cd7a2-116">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="cd7a2-117">負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="cd7a2-118">積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="cd7a2-119">負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整する</span><span class="sxs-lookup"><span data-stu-id="cd7a2-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="cd7a2-120">次の手順を使用して負荷行を確認し、10 進数および他の丸め問題なしに数量を正しく変換できるように調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="cd7a2-121">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd7a2-122">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd7a2-123">アクション ウィンドウの、 **出荷と入荷** タブの、 **取消** グループで、 **出荷確定の取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="cd7a2-124"> *\*積荷明細行** タブで、問題の原因となる品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="cd7a2-125">**ピッキング済数量の削減** を選択して、選択した数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="cd7a2-126"> *\*明細行の詳細** タブで、*\*注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="cd7a2-127">**数量** フィールドをピッキング済数量 (つまり、**作業作成数量** フィールドの値) に設定して、梱包明細の生成が続行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="cd7a2-128">積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整する</span><span class="sxs-lookup"><span data-stu-id="cd7a2-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="cd7a2-129">次の手順を使用して積荷明細行を確認し、単位の小数点以下の精度に合わせて単位と数量を調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="cd7a2-130">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd7a2-131">梱包明細が生成できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd7a2-132">**積荷明細行** クイックタブで、問題の原因となる品目の積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="cd7a2-133">**数量** および **単位** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="cd7a2-134">**組織管理 \> 単位 \> 単位** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="cd7a2-135">梱包明細が生成できない単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd7a2-136">必要に応じて **小数点以下の精度** フィールドの値を調整します。</span><span class="sxs-lookup"><span data-stu-id="cd7a2-136">Adjust the value of the **Decimal precision** field as required.</span></span>
