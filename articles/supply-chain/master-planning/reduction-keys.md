---
title: 予測下方修正キー
description: このトピックでは、下方修正キーを設定する方法を示す例を提供します。 これには、さまざまな下方修正キーの設定とそれぞれの結果に関する情報が含まれます。 予測要求を減らす方法を定義するには下方修正キーを使用できます。
author: roxanadiaconu
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11d5613f23805993b2a83d007c818c80de6a4b9b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814286"
---
# <a name="forecast-reduction-keys"></a><span data-ttu-id="2ad96-105">予測下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-105">Forecast reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad96-106">このトピックでは、予測要求を減らすために使用されるさまざまな方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="2ad96-107">これには、各メソッドの結果の例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="2ad96-108">予測下方修正キーの作成、設定、および使用方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="2ad96-109">予測要求を減らすため予測下方修正キーを使用するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="2ad96-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="2ad96-110">予測要求の削減に使用する方法</span><span class="sxs-lookup"><span data-stu-id="2ad96-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="2ad96-111">マスター プランに予測を含める場合、実際の需要が含まれるときに予測要求を削減する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span>

<span data-ttu-id="2ad96-112">マスター プランに予測を含め、予測要求を減らすために使用される方法を選択するには、**マスター プラン \> 設定 \> プラン \> マスター プラン**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-112">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="2ad96-113">**予測モデル**フィールドで、予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-113">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="2ad96-114">**予測要求の削減に使用する方法**フィールドで、方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-114">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="2ad96-115">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-115">The following options are available:</span></span>

- <span data-ttu-id="2ad96-116">なし</span><span class="sxs-lookup"><span data-stu-id="2ad96-116">None</span></span>
- <span data-ttu-id="2ad96-117">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-117">Percent – reduction key</span></span>
- <span data-ttu-id="2ad96-118">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-118">Transactions – reduction key</span></span>
- <span data-ttu-id="2ad96-119">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="2ad96-119">Transactions – dynamic period</span></span>

<span data-ttu-id="2ad96-120">次のセクションでは、各オプションの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-120">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="2ad96-121">なし</span><span class="sxs-lookup"><span data-stu-id="2ad96-121">None</span></span>

<span data-ttu-id="2ad96-122">**なし**を選択すると、予測要求はマスター スケジューリング時に削減されません。</span><span class="sxs-lookup"><span data-stu-id="2ad96-122">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="2ad96-123">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-123">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="2ad96-124">これらの計画オーダーは、他のタイプの需要に関係なく、推奨数量を管理します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-124">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="2ad96-125">たとえば、販売注文が出された場合、マスター プランは販売注文を供給する追加の計画オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-125">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="2ad96-126">予測要求の数量は削減されません。</span><span class="sxs-lookup"><span data-stu-id="2ad96-126">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="2ad96-127">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-127">Percent – reduction key</span></span>

<span data-ttu-id="2ad96-128">**率 - 下方修正キー**を選択すると、予測要求は下方修正キーで定義された割合および期間に従って削減されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-128">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="2ad96-129">この場合、マスター プランでは各期間の予測数量 × 下方修正キーとして数量が計算される計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-129">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="2ad96-130">他のタイプの需要がある場合、マスター プランではその要求を供給する計画オーダーも作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-130">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="2ad96-131">例: 率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-131">Example: Percent – reduction key</span></span>

<span data-ttu-id="2ad96-132">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-132">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="2ad96-133">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-133">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="2ad96-134">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-134">Month</span></span>    | <span data-ttu-id="2ad96-135">需要予測</span><span class="sxs-lookup"><span data-stu-id="2ad96-135">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="2ad96-136">1 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-136">January</span></span>  | <span data-ttu-id="2ad96-137">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-137">1,000</span></span>           |
| <span data-ttu-id="2ad96-138">2 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-138">February</span></span> | <span data-ttu-id="2ad96-139">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-139">1,000</span></span>           |
| <span data-ttu-id="2ad96-140">3 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-140">March</span></span>    | <span data-ttu-id="2ad96-141">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-141">1,000</span></span>           |
| <span data-ttu-id="2ad96-142">4 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-142">April</span></span>    | <span data-ttu-id="2ad96-143">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-143">1,000</span></span>           |

<span data-ttu-id="2ad96-144">**下方修正キー**ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-144">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="2ad96-145">計上額</span><span class="sxs-lookup"><span data-stu-id="2ad96-145">Change</span></span> | <span data-ttu-id="2ad96-146">単位</span><span class="sxs-lookup"><span data-stu-id="2ad96-146">Unit</span></span>  | <span data-ttu-id="2ad96-147">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="2ad96-147">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="2ad96-148">1</span><span class="sxs-lookup"><span data-stu-id="2ad96-148">1</span></span>      | <span data-ttu-id="2ad96-149">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-149">Month</span></span> | <span data-ttu-id="2ad96-150">100</span><span class="sxs-lookup"><span data-stu-id="2ad96-150">100</span></span>     |
| <span data-ttu-id="2ad96-151">2</span><span class="sxs-lookup"><span data-stu-id="2ad96-151">2</span></span>      | <span data-ttu-id="2ad96-152">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-152">Month</span></span> | <span data-ttu-id="2ad96-153">75</span><span class="sxs-lookup"><span data-stu-id="2ad96-153">75</span></span>      |
| <span data-ttu-id="2ad96-154">3</span><span class="sxs-lookup"><span data-stu-id="2ad96-154">3</span></span>      | <span data-ttu-id="2ad96-155">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-155">Month</span></span> | <span data-ttu-id="2ad96-156">50</span><span class="sxs-lookup"><span data-stu-id="2ad96-156">50</span></span>      |
| <span data-ttu-id="2ad96-157">4</span><span class="sxs-lookup"><span data-stu-id="2ad96-157">4</span></span>      | <span data-ttu-id="2ad96-158">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-158">Month</span></span> | <span data-ttu-id="2ad96-159">25</span><span class="sxs-lookup"><span data-stu-id="2ad96-159">25</span></span>      |

<span data-ttu-id="2ad96-160">品目の補充グループに下方修正キーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-160">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="2ad96-161">その後、**マスター プラン**ページの**予測要求の削減に使用する方法**フィールドで、**率 - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-161">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="2ad96-162">この場合、1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー**ページで設定した率に従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-162">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="2ad96-163">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-163">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="2ad96-164">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-164">Month</span></span>                | <span data-ttu-id="2ad96-165">計画オーダーの数量</span><span class="sxs-lookup"><span data-stu-id="2ad96-165">Planned order quantity</span></span> | <span data-ttu-id="2ad96-166">計算</span><span class="sxs-lookup"><span data-stu-id="2ad96-166">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="2ad96-167">1 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-167">January</span></span>              | <span data-ttu-id="2ad96-168">0</span><span class="sxs-lookup"><span data-stu-id="2ad96-168">0</span></span>                      | <span data-ttu-id="2ad96-169">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="2ad96-169">= 0% × 1,000</span></span>   |
| <span data-ttu-id="2ad96-170">2 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-170">February</span></span>             | <span data-ttu-id="2ad96-171">250</span><span class="sxs-lookup"><span data-stu-id="2ad96-171">250</span></span>                    | <span data-ttu-id="2ad96-172">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="2ad96-172">= 25% × 1,000</span></span>  |
| <span data-ttu-id="2ad96-173">3 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-173">March</span></span>                | <span data-ttu-id="2ad96-174">500</span><span class="sxs-lookup"><span data-stu-id="2ad96-174">500</span></span>                    | <span data-ttu-id="2ad96-175">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="2ad96-175">= 50% × 1,000</span></span>  |
| <span data-ttu-id="2ad96-176">4 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-176">April</span></span>                | <span data-ttu-id="2ad96-177">750</span><span class="sxs-lookup"><span data-stu-id="2ad96-177">750</span></span>                    | <span data-ttu-id="2ad96-178">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="2ad96-178">= 75% × 1,000</span></span>  |
| <span data-ttu-id="2ad96-179">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-179">May through December</span></span> | <span data-ttu-id="2ad96-180">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-180">1,000</span></span>                  | <span data-ttu-id="2ad96-181">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="2ad96-181">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="2ad96-182">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-182">Transactions – reduction key</span></span>

<span data-ttu-id="2ad96-183">**トランザクション - 下方修正キー**を選択すると、予測要求は下方修正キーで定義された期間に発生するトランザクションによって削減されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-183">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="2ad96-184">例: トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="2ad96-184">Example: Transactions – reduction key</span></span>

<span data-ttu-id="2ad96-185">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-185">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="2ad96-186">この例では、**マスター プラン**ページの**予測要求の削減に使用する方法**フィールドで、**トランザクション – 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-186">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="2ad96-187">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-187">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="2ad96-188">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-188">Month</span></span>    | <span data-ttu-id="2ad96-189">注文数</span><span class="sxs-lookup"><span data-stu-id="2ad96-189">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="2ad96-190">1 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-190">January</span></span>  | <span data-ttu-id="2ad96-191">956</span><span class="sxs-lookup"><span data-stu-id="2ad96-191">956</span></span>                      |
| <span data-ttu-id="2ad96-192">2 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-192">February</span></span> | <span data-ttu-id="2ad96-193">1,176</span><span class="sxs-lookup"><span data-stu-id="2ad96-193">1,176</span></span>                    |
| <span data-ttu-id="2ad96-194">3 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-194">March</span></span>    | <span data-ttu-id="2ad96-195">451</span><span class="sxs-lookup"><span data-stu-id="2ad96-195">451</span></span>                      |
| <span data-ttu-id="2ad96-196">4 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-196">April</span></span>    | <span data-ttu-id="2ad96-197">119</span><span class="sxs-lookup"><span data-stu-id="2ad96-197">119</span></span>                      |

<span data-ttu-id="2ad96-198">前の例で使用した毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-198">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="2ad96-199">月</span><span class="sxs-lookup"><span data-stu-id="2ad96-199">Month</span></span>                | <span data-ttu-id="2ad96-200">必要な個数</span><span class="sxs-lookup"><span data-stu-id="2ad96-200">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="2ad96-201">1 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-201">January</span></span>              | <span data-ttu-id="2ad96-202">44</span><span class="sxs-lookup"><span data-stu-id="2ad96-202">44</span></span>                        |
| <span data-ttu-id="2ad96-203">2 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-203">February</span></span>             | <span data-ttu-id="2ad96-204">0</span><span class="sxs-lookup"><span data-stu-id="2ad96-204">0</span></span>                         |
| <span data-ttu-id="2ad96-205">3 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-205">March</span></span>                | <span data-ttu-id="2ad96-206">549</span><span class="sxs-lookup"><span data-stu-id="2ad96-206">549</span></span>                       |
| <span data-ttu-id="2ad96-207">4 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-207">April</span></span>                | <span data-ttu-id="2ad96-208">881</span><span class="sxs-lookup"><span data-stu-id="2ad96-208">881</span></span>                       |
| <span data-ttu-id="2ad96-209">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="2ad96-209">May through December</span></span> | <span data-ttu-id="2ad96-210">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-210">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="2ad96-211">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="2ad96-211">Transactions – dynamic period</span></span>

<span data-ttu-id="2ad96-212">**トランザクション - 動的期間**を選択する場合、予測要求が動的期間中に発生する実際の注文トランザクションから削減されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-212">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="2ad96-213">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-213">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="2ad96-214">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-214">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="2ad96-215">ただし、実際の注文トランザクションが出されると、予測要求が削減されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-215">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="2ad96-216">実際のトランザクションは、予測要求の一部を使用します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-216">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="2ad96-217">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-217">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="2ad96-218">下方修正キーは必要でないまたは使用されません。</span><span class="sxs-lookup"><span data-stu-id="2ad96-218">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="2ad96-219">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="2ad96-219">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="2ad96-220">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-220">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="2ad96-221">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-221">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="2ad96-222">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-222">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="2ad96-223">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="2ad96-223">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="2ad96-224">例 1: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="2ad96-224">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="2ad96-225">ここでは、**トランザクション - 動的期間**メソッドの使用方法を示す簡単な例を上げます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-225">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="2ad96-226">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-226">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="2ad96-227">日</span><span class="sxs-lookup"><span data-stu-id="2ad96-227">Date</span></span>       | <span data-ttu-id="2ad96-228">需要予測</span><span class="sxs-lookup"><span data-stu-id="2ad96-228">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="2ad96-229">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-229">January 1</span></span>  | <span data-ttu-id="2ad96-230">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-230">1,000</span></span>           |
| <span data-ttu-id="2ad96-231">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-231">February 1</span></span> | <span data-ttu-id="2ad96-232">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-232">1,000</span></span>             |

<span data-ttu-id="2ad96-233">次の販売注文も作成します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-233">You also create the following sales orders.</span></span>

| <span data-ttu-id="2ad96-234">日</span><span class="sxs-lookup"><span data-stu-id="2ad96-234">Date</span></span>        | <span data-ttu-id="2ad96-235">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="2ad96-235">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="2ad96-236">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-236">January 15</span></span>  | <span data-ttu-id="2ad96-237">200</span><span class="sxs-lookup"><span data-stu-id="2ad96-237">200</span></span>                  |
| <span data-ttu-id="2ad96-238">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="2ad96-238">February 15</span></span> | <span data-ttu-id="2ad96-239">400</span><span class="sxs-lookup"><span data-stu-id="2ad96-239">400</span></span>                  |

<span data-ttu-id="2ad96-240">この場合、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-240">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="2ad96-241">需要予測日</span><span class="sxs-lookup"><span data-stu-id="2ad96-241">Demand forecast date</span></span> | <span data-ttu-id="2ad96-242">件数</span><span class="sxs-lookup"><span data-stu-id="2ad96-242">Quantity</span></span> | <span data-ttu-id="2ad96-243">説明</span><span class="sxs-lookup"><span data-stu-id="2ad96-243">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="2ad96-244">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-244">January 1</span></span>            | <span data-ttu-id="2ad96-245">800</span><span class="sxs-lookup"><span data-stu-id="2ad96-245">800</span></span>      | <span data-ttu-id="2ad96-246">予測要求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="2ad96-246">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="2ad96-247">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-247">January 15</span></span>           | <span data-ttu-id="2ad96-248">200</span><span class="sxs-lookup"><span data-stu-id="2ad96-248">200</span></span>      | <span data-ttu-id="2ad96-249">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="2ad96-249">Sales orders requirements</span></span>             |
| <span data-ttu-id="2ad96-250">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-250">February 1</span></span>           | <span data-ttu-id="2ad96-251">600</span><span class="sxs-lookup"><span data-stu-id="2ad96-251">600</span></span>      | <span data-ttu-id="2ad96-252">予測要求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="2ad96-252">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="2ad96-253">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="2ad96-253">February 15</span></span>          | <span data-ttu-id="2ad96-254">400</span><span class="sxs-lookup"><span data-stu-id="2ad96-254">400</span></span>      | <span data-ttu-id="2ad96-255">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="2ad96-255">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="2ad96-256">例 2: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="2ad96-256">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="2ad96-257">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など。</span><span class="sxs-lookup"><span data-stu-id="2ad96-257">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="2ad96-258">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-258">These periods are defined in the reduction key.</span></span> <span data-ttu-id="2ad96-259">ただし、2 つの需要予測行の間の時間も、*暗黙に*期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-259">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="2ad96-260">この例では、次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-260">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="2ad96-261">日</span><span class="sxs-lookup"><span data-stu-id="2ad96-261">Date</span></span>       | <span data-ttu-id="2ad96-262">需要予測</span><span class="sxs-lookup"><span data-stu-id="2ad96-262">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="2ad96-263">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-263">January 1</span></span>  | <span data-ttu-id="2ad96-264">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-264">1,000</span></span>           |
| <span data-ttu-id="2ad96-265">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-265">January 5</span></span>  | <span data-ttu-id="2ad96-266">500</span><span class="sxs-lookup"><span data-stu-id="2ad96-266">500</span></span>             |
| <span data-ttu-id="2ad96-267">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-267">January 12</span></span> | <span data-ttu-id="2ad96-268">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-268">1,000</span></span>           |

<span data-ttu-id="2ad96-269">この予測では、予測日の間にクリア期間がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2ad96-269">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="2ad96-270">日付 1 と日付 2 と間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="2ad96-270">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="2ad96-271">このような周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-271">These spans are the dynamic periods.</span></span>

<span data-ttu-id="2ad96-272">次の販売注文明細行も作成します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-272">You also create the following sales order lines.</span></span>

| <span data-ttu-id="2ad96-273">日</span><span class="sxs-lookup"><span data-stu-id="2ad96-273">Date</span></span>                             | <span data-ttu-id="2ad96-274">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="2ad96-274">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="2ad96-275">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-275">December 15 in the previous year</span></span> | <span data-ttu-id="2ad96-276">500</span><span class="sxs-lookup"><span data-stu-id="2ad96-276">500</span></span>                  |
| <span data-ttu-id="2ad96-277">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-277">January 3</span></span>                        | <span data-ttu-id="2ad96-278">100</span><span class="sxs-lookup"><span data-stu-id="2ad96-278">100</span></span>                  |
| <span data-ttu-id="2ad96-279">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-279">January 10</span></span>                       | <span data-ttu-id="2ad96-280">200</span><span class="sxs-lookup"><span data-stu-id="2ad96-280">200</span></span>                  |

<span data-ttu-id="2ad96-281">この場合、次のように予測が削減されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-281">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="2ad96-282">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="2ad96-282">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="2ad96-283">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-283">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="2ad96-284">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-284">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="2ad96-285">したがって、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-285">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="2ad96-286">需要予測日</span><span class="sxs-lookup"><span data-stu-id="2ad96-286">Demand forecast date</span></span>             | <span data-ttu-id="2ad96-287">件数</span><span class="sxs-lookup"><span data-stu-id="2ad96-287">Quantity</span></span> | <span data-ttu-id="2ad96-288">説明</span><span class="sxs-lookup"><span data-stu-id="2ad96-288">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="2ad96-289">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-289">December 15 in the previous year</span></span> | <span data-ttu-id="2ad96-290">500</span><span class="sxs-lookup"><span data-stu-id="2ad96-290">500</span></span>      | <span data-ttu-id="2ad96-291">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="2ad96-291">Sales order requirements</span></span>                                            |
| <span data-ttu-id="2ad96-292">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-292">January 1</span></span>                        | <span data-ttu-id="2ad96-293">900</span><span class="sxs-lookup"><span data-stu-id="2ad96-293">900</span></span>      | <span data-ttu-id="2ad96-294">1 月 1 日から 1 月 5 日の期間の予測要求 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="2ad96-294">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="2ad96-295">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-295">January 3</span></span>                        | <span data-ttu-id="2ad96-296">100</span><span class="sxs-lookup"><span data-stu-id="2ad96-296">100</span></span>      | <span data-ttu-id="2ad96-297">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="2ad96-297">Sales order requirements</span></span>                                            |
| <span data-ttu-id="2ad96-298">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-298">January 5</span></span>                        | <span data-ttu-id="2ad96-299">300</span><span class="sxs-lookup"><span data-stu-id="2ad96-299">300</span></span>      | <span data-ttu-id="2ad96-300">1 月 5 日から 1 月 10 日の期間の予測要求 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="2ad96-300">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="2ad96-301">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="2ad96-301">January 12</span></span>                       | <span data-ttu-id="2ad96-302">1.000</span><span class="sxs-lookup"><span data-stu-id="2ad96-302">1,000</span></span>    | <span data-ttu-id="2ad96-303">1 月 12 日から終了日の期間の予測要求</span><span class="sxs-lookup"><span data-stu-id="2ad96-303">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="2ad96-304">予測下方修正キーの作成および設定</span><span class="sxs-lookup"><span data-stu-id="2ad96-304">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="2ad96-305">予測下方修正キーは、予測要求を削減するため**トランザクション - 下方修正キー**および**率 - 下方修正キー**の方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-305">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="2ad96-306">下方修正キーを作成および設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2ad96-306">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="2ad96-307">**マスター プラン \> 設定 \> 補充 \> 下方修正キー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-307">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="2ad96-308">**新規**を選択または **Ctrl+N** を押して下方修正キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-308">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="2ad96-309">**下方修正キー**フィールドで、予測下方修正キーの固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-309">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="2ad96-310">その後、**名前**フィールドで、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-310">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="2ad96-311">各期間の期間および下方修正キーの割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-311">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="2ad96-312">**有効日**フィールドは、期間の作成が開始する日付を示します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-312">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="2ad96-313">**有効日を使用**オプションを**はい**に設定すると、有効日の期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-313">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="2ad96-314">**いいえ**に設定すると、マスター プランが実行される日付で期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-314">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="2ad96-315">予測下方修正が発生する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-315">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="2ad96-316">特定の期間の、予測要求を削減する必要がある割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-316">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="2ad96-317">要件を削減するには正の値、または要件を増加するには負の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-317">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="2ad96-318">下方修正キーの使用</span><span class="sxs-lookup"><span data-stu-id="2ad96-318">Use a reduction key</span></span>

<span data-ttu-id="2ad96-319">予測下方修正キーは、品目の補充グループに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ad96-319">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="2ad96-320">これらの手順に従い、下方修正キーを品目の補充グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-320">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="2ad96-321">**マスター プラン \> 設定 \> 補充 \> 補充グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-321">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="2ad96-322">**その他**クイック タブの、**下方修正キー**フィールドで、補充グループに割り当てる下方修正キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-322">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="2ad96-323">その後、下方修正キーは、補充グループに属する品目すべてに適用されます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-323">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="2ad96-324">マスター スケジューリング時に予測下方修正の計算に下方修正キーを使用するには、予測計画またはマスター プランの設定でこの設定を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ad96-324">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="2ad96-325">次の場所のいずれかに移動します:</span><span class="sxs-lookup"><span data-stu-id="2ad96-325">Go to one of the following locations:</span></span>

    - <span data-ttu-id="2ad96-326">マスター プラン \> 設定 \> 計画 \> 予測計画</span><span class="sxs-lookup"><span data-stu-id="2ad96-326">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="2ad96-327">マスター プラン \> 設定 \> 計画 \> マスター プラン</span><span class="sxs-lookup"><span data-stu-id="2ad96-327">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="2ad96-328">**予測計画**または**マスター プラン**ページの、**一般**クイック タブの、**予測要求の削減に使用する方法**フィールドで、**率 - 下方修正キー**または**トランザクション - 下方修正キー**のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-328">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="2ad96-329">トランザクションによる予測の削減</span><span class="sxs-lookup"><span data-stu-id="2ad96-329">Reduce a forecast by transactions</span></span>

<span data-ttu-id="2ad96-330">予測要求の削減のメソッドとして**トランザクション - 下方修正キー**または**トランザクション - 動的期間**を選択すると、予測を削減するトランザクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2ad96-330">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="2ad96-331">**リリース済製品**ページの、**その他**クイック タブ、**予測の削減方法**フィールドで、すべてのトランザクションで予測を削減する必要がある場合は**すべてのトランザクション**を、または販売注文のみで予測を削減する必要がある場合は**注文**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ad96-331">On the **Released products** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ad96-332">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2ad96-332">Additional resources</span></span>

[<span data-ttu-id="2ad96-333">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="2ad96-333">Master plans overview</span></span>](master-plans.md)
