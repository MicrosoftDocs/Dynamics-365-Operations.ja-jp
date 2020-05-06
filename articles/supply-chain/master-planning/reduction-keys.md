---
title: 予測下方修正キー
description: このトピックでは、下方修正キーを設定する方法を示す例を提供します。 これには、さまざまな下方修正キーの設定とそれぞれの結果に関する情報が含まれます。 予測要求を減らす方法を定義するには下方修正キーを使用できます。
author: roxanadiaconu
manager: tfehr
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6191b4809c3785d92395bec1b7d51bfc978f9245
ms.sourcegitcommit: 5419f2b8f51cd5de55be66d1389b5b9d7771fd52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262699"
---
# <a name="forecast-reduction-keys"></a><span data-ttu-id="74584-105">予測下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-105">Forecast reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74584-106">このトピックでは、予測要求を減らすために使用されるさまざまな方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="74584-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="74584-107">これには、各メソッドの結果の例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="74584-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="74584-108">予測下方修正キーの作成、設定、および使用方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="74584-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="74584-109">予測要求を減らすため予測下方修正キーを使用するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="74584-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="74584-110">予測要求の削減に使用する方法</span><span class="sxs-lookup"><span data-stu-id="74584-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="74584-111">マスター プランに予測を含める場合、実際の需要が含まれるときに予測要求を削減する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="74584-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span> <span data-ttu-id="74584-112">マスター プランでは、過去から予測要求が除外されます。つまり、今日の日付より前のすべての予測要求が除外されます。</span><span class="sxs-lookup"><span data-stu-id="74584-112">Note that master planning excludes forecast requirements from the past, which means all forecast requirements before today's date.</span></span>

<span data-ttu-id="74584-113">マスター プランに予測を含め、予測要求を減らすために使用される方法を選択するには、**マスター プラン \> 設定 \> プラン \> マスター プラン**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74584-113">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="74584-114">**予測モデル**フィールドで、予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-114">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="74584-115">**予測要求の削減に使用する方法**フィールドで、方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-115">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="74584-116">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="74584-116">The following options are available:</span></span>

- <span data-ttu-id="74584-117">なし</span><span class="sxs-lookup"><span data-stu-id="74584-117">None</span></span>
- <span data-ttu-id="74584-118">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-118">Percent – reduction key</span></span>
- <span data-ttu-id="74584-119">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-119">Transactions – reduction key</span></span>
- <span data-ttu-id="74584-120">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="74584-120">Transactions – dynamic period</span></span>

<span data-ttu-id="74584-121">次のセクションでは、各オプションの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="74584-121">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="74584-122">なし</span><span class="sxs-lookup"><span data-stu-id="74584-122">None</span></span>

<span data-ttu-id="74584-123">**なし**を選択すると、予測要求はマスター スケジューリング時に削減されません。</span><span class="sxs-lookup"><span data-stu-id="74584-123">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="74584-124">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-124">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="74584-125">これらの計画オーダーは、他のタイプの需要に関係なく、推奨数量を管理します。</span><span class="sxs-lookup"><span data-stu-id="74584-125">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="74584-126">たとえば、販売注文が出された場合、マスター プランは販売注文を供給する追加の計画オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="74584-126">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="74584-127">予測要求の数量は削減されません。</span><span class="sxs-lookup"><span data-stu-id="74584-127">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="74584-128">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-128">Percent – reduction key</span></span>

<span data-ttu-id="74584-129">**率 - 下方修正キー**を選択すると、予測要求は下方修正キーで定義された割合および期間に従って削減されます。</span><span class="sxs-lookup"><span data-stu-id="74584-129">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="74584-130">この場合、マスター プランでは各期間の予測数量 × 下方修正キーとして数量が計算される計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-130">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="74584-131">他のタイプの需要がある場合、マスター プランではその要求を供給する計画オーダーも作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-131">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="74584-132">例: 率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-132">Example: Percent – reduction key</span></span>

<span data-ttu-id="74584-133">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="74584-133">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="74584-134">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="74584-134">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="74584-135">月</span><span class="sxs-lookup"><span data-stu-id="74584-135">Month</span></span>    | <span data-ttu-id="74584-136">需要予測</span><span class="sxs-lookup"><span data-stu-id="74584-136">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="74584-137">1 月</span><span class="sxs-lookup"><span data-stu-id="74584-137">January</span></span>  | <span data-ttu-id="74584-138">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-138">1,000</span></span>           |
| <span data-ttu-id="74584-139">2 月</span><span class="sxs-lookup"><span data-stu-id="74584-139">February</span></span> | <span data-ttu-id="74584-140">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-140">1,000</span></span>           |
| <span data-ttu-id="74584-141">3 月</span><span class="sxs-lookup"><span data-stu-id="74584-141">March</span></span>    | <span data-ttu-id="74584-142">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-142">1,000</span></span>           |
| <span data-ttu-id="74584-143">4 月</span><span class="sxs-lookup"><span data-stu-id="74584-143">April</span></span>    | <span data-ttu-id="74584-144">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-144">1,000</span></span>           |

<span data-ttu-id="74584-145">**下方修正キー**ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="74584-145">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="74584-146">計上額</span><span class="sxs-lookup"><span data-stu-id="74584-146">Change</span></span> | <span data-ttu-id="74584-147">単位</span><span class="sxs-lookup"><span data-stu-id="74584-147">Unit</span></span>  | <span data-ttu-id="74584-148">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="74584-148">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="74584-149">1</span><span class="sxs-lookup"><span data-stu-id="74584-149">1</span></span>      | <span data-ttu-id="74584-150">月</span><span class="sxs-lookup"><span data-stu-id="74584-150">Month</span></span> | <span data-ttu-id="74584-151">100</span><span class="sxs-lookup"><span data-stu-id="74584-151">100</span></span>     |
| <span data-ttu-id="74584-152">2</span><span class="sxs-lookup"><span data-stu-id="74584-152">2</span></span>      | <span data-ttu-id="74584-153">月</span><span class="sxs-lookup"><span data-stu-id="74584-153">Month</span></span> | <span data-ttu-id="74584-154">75</span><span class="sxs-lookup"><span data-stu-id="74584-154">75</span></span>      |
| <span data-ttu-id="74584-155">3</span><span class="sxs-lookup"><span data-stu-id="74584-155">3</span></span>      | <span data-ttu-id="74584-156">月</span><span class="sxs-lookup"><span data-stu-id="74584-156">Month</span></span> | <span data-ttu-id="74584-157">50</span><span class="sxs-lookup"><span data-stu-id="74584-157">50</span></span>      |
| <span data-ttu-id="74584-158">4</span><span class="sxs-lookup"><span data-stu-id="74584-158">4</span></span>      | <span data-ttu-id="74584-159">月</span><span class="sxs-lookup"><span data-stu-id="74584-159">Month</span></span> | <span data-ttu-id="74584-160">25</span><span class="sxs-lookup"><span data-stu-id="74584-160">25</span></span>      |

<span data-ttu-id="74584-161">品目の補充グループに下方修正キーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="74584-161">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="74584-162">その後、**マスター プラン**ページの**予測要求の削減に使用する方法**フィールドで、**率 - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-162">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="74584-163">この場合、1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー**ページで設定した率に従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="74584-163">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="74584-164">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="74584-164">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="74584-165">月</span><span class="sxs-lookup"><span data-stu-id="74584-165">Month</span></span>                | <span data-ttu-id="74584-166">計画オーダーの数量</span><span class="sxs-lookup"><span data-stu-id="74584-166">Planned order quantity</span></span> | <span data-ttu-id="74584-167">計算</span><span class="sxs-lookup"><span data-stu-id="74584-167">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="74584-168">1 月</span><span class="sxs-lookup"><span data-stu-id="74584-168">January</span></span>              | <span data-ttu-id="74584-169">0</span><span class="sxs-lookup"><span data-stu-id="74584-169">0</span></span>                      | <span data-ttu-id="74584-170">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="74584-170">= 0% × 1,000</span></span>   |
| <span data-ttu-id="74584-171">2 月</span><span class="sxs-lookup"><span data-stu-id="74584-171">February</span></span>             | <span data-ttu-id="74584-172">250</span><span class="sxs-lookup"><span data-stu-id="74584-172">250</span></span>                    | <span data-ttu-id="74584-173">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="74584-173">= 25% × 1,000</span></span>  |
| <span data-ttu-id="74584-174">3 月</span><span class="sxs-lookup"><span data-stu-id="74584-174">March</span></span>                | <span data-ttu-id="74584-175">500</span><span class="sxs-lookup"><span data-stu-id="74584-175">500</span></span>                    | <span data-ttu-id="74584-176">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="74584-176">= 50% × 1,000</span></span>  |
| <span data-ttu-id="74584-177">4 月</span><span class="sxs-lookup"><span data-stu-id="74584-177">April</span></span>                | <span data-ttu-id="74584-178">750</span><span class="sxs-lookup"><span data-stu-id="74584-178">750</span></span>                    | <span data-ttu-id="74584-179">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="74584-179">= 75% × 1,000</span></span>  |
| <span data-ttu-id="74584-180">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="74584-180">May through December</span></span> | <span data-ttu-id="74584-181">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-181">1,000</span></span>                  | <span data-ttu-id="74584-182">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="74584-182">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="74584-183">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-183">Transactions – reduction key</span></span>

<span data-ttu-id="74584-184">**トランザクション - 下方修正キー**を選択すると、予測要求は下方修正キーで定義された期間に発生するトランザクションによって削減されます。</span><span class="sxs-lookup"><span data-stu-id="74584-184">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="74584-185">例: トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="74584-185">Example: Transactions – reduction key</span></span>

<span data-ttu-id="74584-186">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="74584-186">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="74584-187">この例では、**マスター プラン**ページの**予測要求の削減に使用する方法**フィールドで、**トランザクション – 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-187">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="74584-188">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="74584-188">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="74584-189">月</span><span class="sxs-lookup"><span data-stu-id="74584-189">Month</span></span>    | <span data-ttu-id="74584-190">注文数</span><span class="sxs-lookup"><span data-stu-id="74584-190">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="74584-191">1 月</span><span class="sxs-lookup"><span data-stu-id="74584-191">January</span></span>  | <span data-ttu-id="74584-192">956</span><span class="sxs-lookup"><span data-stu-id="74584-192">956</span></span>                      |
| <span data-ttu-id="74584-193">2 月</span><span class="sxs-lookup"><span data-stu-id="74584-193">February</span></span> | <span data-ttu-id="74584-194">1,176</span><span class="sxs-lookup"><span data-stu-id="74584-194">1,176</span></span>                    |
| <span data-ttu-id="74584-195">3 月</span><span class="sxs-lookup"><span data-stu-id="74584-195">March</span></span>    | <span data-ttu-id="74584-196">451</span><span class="sxs-lookup"><span data-stu-id="74584-196">451</span></span>                      |
| <span data-ttu-id="74584-197">4 月</span><span class="sxs-lookup"><span data-stu-id="74584-197">April</span></span>    | <span data-ttu-id="74584-198">119</span><span class="sxs-lookup"><span data-stu-id="74584-198">119</span></span>                      |

<span data-ttu-id="74584-199">前の例で使用した毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="74584-199">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="74584-200">月</span><span class="sxs-lookup"><span data-stu-id="74584-200">Month</span></span>                | <span data-ttu-id="74584-201">必要な個数</span><span class="sxs-lookup"><span data-stu-id="74584-201">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="74584-202">1 月</span><span class="sxs-lookup"><span data-stu-id="74584-202">January</span></span>              | <span data-ttu-id="74584-203">44</span><span class="sxs-lookup"><span data-stu-id="74584-203">44</span></span>                        |
| <span data-ttu-id="74584-204">2 月</span><span class="sxs-lookup"><span data-stu-id="74584-204">February</span></span>             | <span data-ttu-id="74584-205">0</span><span class="sxs-lookup"><span data-stu-id="74584-205">0</span></span>                         |
| <span data-ttu-id="74584-206">3 月</span><span class="sxs-lookup"><span data-stu-id="74584-206">March</span></span>                | <span data-ttu-id="74584-207">549</span><span class="sxs-lookup"><span data-stu-id="74584-207">549</span></span>                       |
| <span data-ttu-id="74584-208">4 月</span><span class="sxs-lookup"><span data-stu-id="74584-208">April</span></span>                | <span data-ttu-id="74584-209">881</span><span class="sxs-lookup"><span data-stu-id="74584-209">881</span></span>                       |
| <span data-ttu-id="74584-210">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="74584-210">May through December</span></span> | <span data-ttu-id="74584-211">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-211">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="74584-212">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="74584-212">Transactions – dynamic period</span></span>

<span data-ttu-id="74584-213">**トランザクション - 動的期間**を選択する場合、予測要求が動的期間中に発生する実際の注文トランザクションから削減されます。</span><span class="sxs-lookup"><span data-stu-id="74584-213">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="74584-214">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="74584-214">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="74584-215">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-215">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="74584-216">ただし、実際の注文トランザクションが出されると、予測要求が削減されます。</span><span class="sxs-lookup"><span data-stu-id="74584-216">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="74584-217">実際のトランザクションは、予測要求の一部を使用します。</span><span class="sxs-lookup"><span data-stu-id="74584-217">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="74584-218">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="74584-218">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="74584-219">下方修正キーは必要でないまたは使用されません。</span><span class="sxs-lookup"><span data-stu-id="74584-219">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="74584-220">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="74584-220">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="74584-221">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="74584-221">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="74584-222">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="74584-222">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="74584-223">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="74584-223">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="74584-224">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="74584-224">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="74584-225">例 1: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="74584-225">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="74584-226">ここでは、**トランザクション - 動的期間**メソッドの使用方法を示す簡単な例を上げます。</span><span class="sxs-lookup"><span data-stu-id="74584-226">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="74584-227">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="74584-227">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="74584-228">日</span><span class="sxs-lookup"><span data-stu-id="74584-228">Date</span></span>       | <span data-ttu-id="74584-229">需要予測</span><span class="sxs-lookup"><span data-stu-id="74584-229">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="74584-230">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-230">January 1</span></span>  | <span data-ttu-id="74584-231">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-231">1,000</span></span>           |
| <span data-ttu-id="74584-232">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-232">February 1</span></span> | <span data-ttu-id="74584-233">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-233">1,000</span></span>             |

<span data-ttu-id="74584-234">次の販売注文も作成します。</span><span class="sxs-lookup"><span data-stu-id="74584-234">You also create the following sales orders.</span></span>

| <span data-ttu-id="74584-235">日</span><span class="sxs-lookup"><span data-stu-id="74584-235">Date</span></span>        | <span data-ttu-id="74584-236">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="74584-236">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="74584-237">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="74584-237">January 15</span></span>  | <span data-ttu-id="74584-238">200</span><span class="sxs-lookup"><span data-stu-id="74584-238">200</span></span>                  |
| <span data-ttu-id="74584-239">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="74584-239">February 15</span></span> | <span data-ttu-id="74584-240">400</span><span class="sxs-lookup"><span data-stu-id="74584-240">400</span></span>                  |

<span data-ttu-id="74584-241">この場合、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-241">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="74584-242">需要予測日</span><span class="sxs-lookup"><span data-stu-id="74584-242">Demand forecast date</span></span> | <span data-ttu-id="74584-243">件数</span><span class="sxs-lookup"><span data-stu-id="74584-243">Quantity</span></span> | <span data-ttu-id="74584-244">説明</span><span class="sxs-lookup"><span data-stu-id="74584-244">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="74584-245">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-245">January 1</span></span>            | <span data-ttu-id="74584-246">800</span><span class="sxs-lookup"><span data-stu-id="74584-246">800</span></span>      | <span data-ttu-id="74584-247">予測要求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="74584-247">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="74584-248">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="74584-248">January 15</span></span>           | <span data-ttu-id="74584-249">200</span><span class="sxs-lookup"><span data-stu-id="74584-249">200</span></span>      | <span data-ttu-id="74584-250">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="74584-250">Sales orders requirements</span></span>             |
| <span data-ttu-id="74584-251">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-251">February 1</span></span>           | <span data-ttu-id="74584-252">600</span><span class="sxs-lookup"><span data-stu-id="74584-252">600</span></span>      | <span data-ttu-id="74584-253">予測要求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="74584-253">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="74584-254">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="74584-254">February 15</span></span>          | <span data-ttu-id="74584-255">400</span><span class="sxs-lookup"><span data-stu-id="74584-255">400</span></span>      | <span data-ttu-id="74584-256">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="74584-256">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="74584-257">例 2: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="74584-257">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="74584-258">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など。</span><span class="sxs-lookup"><span data-stu-id="74584-258">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="74584-259">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="74584-259">These periods are defined in the reduction key.</span></span> <span data-ttu-id="74584-260">ただし、2 つの需要予測行の間の時間も、*暗黙に*期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="74584-260">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="74584-261">この例では、次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="74584-261">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="74584-262">日</span><span class="sxs-lookup"><span data-stu-id="74584-262">Date</span></span>       | <span data-ttu-id="74584-263">需要予測</span><span class="sxs-lookup"><span data-stu-id="74584-263">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="74584-264">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-264">January 1</span></span>  | <span data-ttu-id="74584-265">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-265">1,000</span></span>           |
| <span data-ttu-id="74584-266">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="74584-266">January 5</span></span>  | <span data-ttu-id="74584-267">500</span><span class="sxs-lookup"><span data-stu-id="74584-267">500</span></span>             |
| <span data-ttu-id="74584-268">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="74584-268">January 12</span></span> | <span data-ttu-id="74584-269">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-269">1,000</span></span>           |

<span data-ttu-id="74584-270">この予測では、予測日の間にクリア期間がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="74584-270">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="74584-271">日付 1 と日付 2 と間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="74584-271">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="74584-272">このような周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="74584-272">These spans are the dynamic periods.</span></span>

<span data-ttu-id="74584-273">次の販売注文明細行も作成します。</span><span class="sxs-lookup"><span data-stu-id="74584-273">You also create the following sales order lines.</span></span>

| <span data-ttu-id="74584-274">日</span><span class="sxs-lookup"><span data-stu-id="74584-274">Date</span></span>                             | <span data-ttu-id="74584-275">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="74584-275">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="74584-276">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="74584-276">December 15 in the previous year</span></span> | <span data-ttu-id="74584-277">500</span><span class="sxs-lookup"><span data-stu-id="74584-277">500</span></span>                  |
| <span data-ttu-id="74584-278">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="74584-278">January 3</span></span>                        | <span data-ttu-id="74584-279">100</span><span class="sxs-lookup"><span data-stu-id="74584-279">100</span></span>                  |
| <span data-ttu-id="74584-280">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="74584-280">January 10</span></span>                       | <span data-ttu-id="74584-281">200</span><span class="sxs-lookup"><span data-stu-id="74584-281">200</span></span>                  |

<span data-ttu-id="74584-282">この場合、次のように予測が削減されます。</span><span class="sxs-lookup"><span data-stu-id="74584-282">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="74584-283">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="74584-283">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="74584-284">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="74584-284">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="74584-285">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="74584-285">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="74584-286">したがって、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="74584-286">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="74584-287">需要予測日</span><span class="sxs-lookup"><span data-stu-id="74584-287">Demand forecast date</span></span>             | <span data-ttu-id="74584-288">件数</span><span class="sxs-lookup"><span data-stu-id="74584-288">Quantity</span></span> | <span data-ttu-id="74584-289">説明</span><span class="sxs-lookup"><span data-stu-id="74584-289">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="74584-290">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="74584-290">December 15 in the previous year</span></span> | <span data-ttu-id="74584-291">500</span><span class="sxs-lookup"><span data-stu-id="74584-291">500</span></span>      | <span data-ttu-id="74584-292">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="74584-292">Sales order requirements</span></span>                                            |
| <span data-ttu-id="74584-293">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="74584-293">January 1</span></span>                        | <span data-ttu-id="74584-294">900</span><span class="sxs-lookup"><span data-stu-id="74584-294">900</span></span>      | <span data-ttu-id="74584-295">1 月 1 日から 1 月 5 日の期間の予測要求 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="74584-295">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="74584-296">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="74584-296">January 3</span></span>                        | <span data-ttu-id="74584-297">100</span><span class="sxs-lookup"><span data-stu-id="74584-297">100</span></span>      | <span data-ttu-id="74584-298">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="74584-298">Sales order requirements</span></span>                                            |
| <span data-ttu-id="74584-299">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="74584-299">January 5</span></span>                        | <span data-ttu-id="74584-300">300</span><span class="sxs-lookup"><span data-stu-id="74584-300">300</span></span>      | <span data-ttu-id="74584-301">1 月 5 日から 1 月 10 日の期間の予測要求 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="74584-301">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="74584-302">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="74584-302">January 12</span></span>                       | <span data-ttu-id="74584-303">1.000</span><span class="sxs-lookup"><span data-stu-id="74584-303">1,000</span></span>    | <span data-ttu-id="74584-304">1 月 12 日から終了日の期間の予測要求</span><span class="sxs-lookup"><span data-stu-id="74584-304">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="74584-305">予測下方修正キーの作成および設定</span><span class="sxs-lookup"><span data-stu-id="74584-305">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="74584-306">予測下方修正キーは、予測要求を削減するため**トランザクション - 下方修正キー**および**率 - 下方修正キー**の方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="74584-306">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="74584-307">下方修正キーを作成および設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74584-307">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="74584-308">**マスター プラン \> 設定 \> 補充 \> 下方修正キー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74584-308">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="74584-309">**新規**を選択または **Ctrl+N** を押して下方修正キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="74584-309">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="74584-310">**下方修正キー**フィールドで、予測下方修正キーの固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="74584-310">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="74584-311">その後、**名前**フィールドで、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="74584-311">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="74584-312">各期間の期間および下方修正キーの割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="74584-312">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="74584-313">**有効日**フィールドは、期間の作成が開始する日付を示します。</span><span class="sxs-lookup"><span data-stu-id="74584-313">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="74584-314">**有効日を使用**オプションを**はい**に設定すると、有効日の期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="74584-314">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="74584-315">**いいえ**に設定すると、マスター プランが実行される日付で期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="74584-315">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="74584-316">予測下方修正が発生する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="74584-316">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="74584-317">特定の期間の、予測要求を削減する必要がある割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="74584-317">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="74584-318">要件を削減するには正の値、または要件を増加するには負の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="74584-318">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="74584-319">下方修正キーの使用</span><span class="sxs-lookup"><span data-stu-id="74584-319">Use a reduction key</span></span>

<span data-ttu-id="74584-320">予測下方修正キーは、品目の補充グループに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="74584-320">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="74584-321">これらの手順に従い、下方修正キーを品目の補充グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="74584-321">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="74584-322">**マスター プラン \> 設定 \> 補充 \> 補充グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74584-322">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="74584-323">**その他**クイック タブの、**下方修正キー**フィールドで、補充グループに割り当てる下方修正キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-323">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="74584-324">その後、下方修正キーは、補充グループに属する品目すべてに適用されます。</span><span class="sxs-lookup"><span data-stu-id="74584-324">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="74584-325">マスター スケジューリング時に予測下方修正の計算に下方修正キーを使用するには、予測計画またはマスター プランの設定でこの設定を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74584-325">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="74584-326">次の場所のいずれかに移動します:</span><span class="sxs-lookup"><span data-stu-id="74584-326">Go to one of the following locations:</span></span>

    - <span data-ttu-id="74584-327">マスター プラン \> 設定 \> 計画 \> 予測計画</span><span class="sxs-lookup"><span data-stu-id="74584-327">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="74584-328">マスター プラン \> 設定 \> 計画 \> マスター プラン</span><span class="sxs-lookup"><span data-stu-id="74584-328">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="74584-329">**予測計画**または**マスター プラン**ページの、**一般**クイック タブの、**予測要求の削減に使用する方法**フィールドで、**率 - 下方修正キー**または**トランザクション - 下方修正キー**のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-329">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="74584-330">トランザクションによる予測の削減</span><span class="sxs-lookup"><span data-stu-id="74584-330">Reduce a forecast by transactions</span></span>

<span data-ttu-id="74584-331">予測要求の削減のメソッドとして**トランザクション - 下方修正キー**または**トランザクション - 動的期間**を選択すると、予測を削減するトランザクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="74584-331">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="74584-332">**補充グループ** ページの、**その他** クイック タブにある、**予測の削減方法** フィールドで、すべてのトランザクションで予測を削減する必要がある場合は **すべてのトランザクション** を、または販売注文のみで予測を削減する必要がある場合は **販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74584-332">On the **Coverage groups** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74584-333">追加リソース</span><span class="sxs-lookup"><span data-stu-id="74584-333">Additional resources</span></span>

[<span data-ttu-id="74584-334">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="74584-334">Master plans overview</span></span>](master-plans.md)
