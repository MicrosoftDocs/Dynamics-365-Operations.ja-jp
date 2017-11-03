---
title: "下方修正キー"
description: "この記事は、下方修正キーを設定する方法を示す例を提供します。 これには、さまざまな下方修正キーの設定とそれぞれの結果に関する情報が含まれます。 予測要求を減らす方法を定義するには下方修正キーを使用できます。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506ca3aac7ad271ca7472f3b74627e94d97a74ee
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="92b13-105">下方修正キー</span><span class="sxs-lookup"><span data-stu-id="92b13-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="92b13-106">この記事は、下方修正キーを設定する方法を示す例を提供します。</span><span class="sxs-lookup"><span data-stu-id="92b13-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="92b13-107">これには、さまざまな下方修正キーの設定とそれぞれの結果に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="92b13-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="92b13-108">予測要求を減らす方法を定義するには下方修正キーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="92b13-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="92b13-109">例 1: 割合 -下方修正キーの予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="92b13-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="92b13-110">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="92b13-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="92b13-111">**下方修正キー** ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="92b13-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="92b13-112">計上額</span><span class="sxs-lookup"><span data-stu-id="92b13-112">Change</span></span> | <span data-ttu-id="92b13-113">単位</span><span class="sxs-lookup"><span data-stu-id="92b13-113">Unit</span></span>  | <span data-ttu-id="92b13-114">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="92b13-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="92b13-115">1</span><span class="sxs-lookup"><span data-stu-id="92b13-115">1</span></span>      | <span data-ttu-id="92b13-116">月</span><span class="sxs-lookup"><span data-stu-id="92b13-116">Month</span></span> | <span data-ttu-id="92b13-117">100</span><span class="sxs-lookup"><span data-stu-id="92b13-117">100</span></span>     |
    | <span data-ttu-id="92b13-118">2</span><span class="sxs-lookup"><span data-stu-id="92b13-118">2</span></span>      | <span data-ttu-id="92b13-119">月</span><span class="sxs-lookup"><span data-stu-id="92b13-119">Month</span></span> | <span data-ttu-id="92b13-120">75</span><span class="sxs-lookup"><span data-stu-id="92b13-120">75</span></span>      |
    | <span data-ttu-id="92b13-121">3</span><span class="sxs-lookup"><span data-stu-id="92b13-121">3</span></span>      | <span data-ttu-id="92b13-122">月</span><span class="sxs-lookup"><span data-stu-id="92b13-122">Month</span></span> | <span data-ttu-id="92b13-123">50</span><span class="sxs-lookup"><span data-stu-id="92b13-123">50</span></span>      |
    | <span data-ttu-id="92b13-124">4</span><span class="sxs-lookup"><span data-stu-id="92b13-124">4</span></span>      | <span data-ttu-id="92b13-125">月</span><span class="sxs-lookup"><span data-stu-id="92b13-125">Month</span></span> | <span data-ttu-id="92b13-126">25</span><span class="sxs-lookup"><span data-stu-id="92b13-126">25</span></span>      |

2.  <span data-ttu-id="92b13-127">品目の補充グループに下方修正キーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="92b13-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="92b13-128">**マスター プラン** ページで、**下方修正原則**フィールドで**割合 - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="92b13-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="92b13-129">毎月 1,000 個の需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="92b13-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="92b13-130">1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー**ページで設定したパーセンテージに従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="92b13-131">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="92b13-132">月</span><span class="sxs-lookup"><span data-stu-id="92b13-132">Month</span></span>                | <span data-ttu-id="92b13-133">必要な個数</span><span class="sxs-lookup"><span data-stu-id="92b13-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="92b13-134">1 月</span><span class="sxs-lookup"><span data-stu-id="92b13-134">January</span></span>              | <span data-ttu-id="92b13-135">0</span><span class="sxs-lookup"><span data-stu-id="92b13-135">0</span></span>                         |
| <span data-ttu-id="92b13-136">2 月</span><span class="sxs-lookup"><span data-stu-id="92b13-136">February</span></span>             | <span data-ttu-id="92b13-137">250</span><span class="sxs-lookup"><span data-stu-id="92b13-137">250</span></span>                       |
| <span data-ttu-id="92b13-138">3 月</span><span class="sxs-lookup"><span data-stu-id="92b13-138">March</span></span>                | <span data-ttu-id="92b13-139">500</span><span class="sxs-lookup"><span data-stu-id="92b13-139">500</span></span>                       |
| <span data-ttu-id="92b13-140">4 月</span><span class="sxs-lookup"><span data-stu-id="92b13-140">April</span></span>                | <span data-ttu-id="92b13-141">750</span><span class="sxs-lookup"><span data-stu-id="92b13-141">750</span></span>                       |
| <span data-ttu-id="92b13-142">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="92b13-142">May through December</span></span> | <span data-ttu-id="92b13-143">1.000</span><span class="sxs-lookup"><span data-stu-id="92b13-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="92b13-144">例 2: トランザクション - 下方修正キーの予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="92b13-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="92b13-145">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="92b13-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="92b13-146">**マスター プラン** ページで、**下方修正原則**フィールドで**トランザクション - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="92b13-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="92b13-147">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="92b13-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="92b13-148">月</span><span class="sxs-lookup"><span data-stu-id="92b13-148">Month</span></span>    | <span data-ttu-id="92b13-149">注文数</span><span class="sxs-lookup"><span data-stu-id="92b13-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="92b13-150">1 月</span><span class="sxs-lookup"><span data-stu-id="92b13-150">January</span></span>  | <span data-ttu-id="92b13-151">956</span><span class="sxs-lookup"><span data-stu-id="92b13-151">956</span></span>                      |
| <span data-ttu-id="92b13-152">2 月</span><span class="sxs-lookup"><span data-stu-id="92b13-152">February</span></span> | <span data-ttu-id="92b13-153">1,176</span><span class="sxs-lookup"><span data-stu-id="92b13-153">1,176</span></span>                    |
| <span data-ttu-id="92b13-154">3 月</span><span class="sxs-lookup"><span data-stu-id="92b13-154">March</span></span>    | <span data-ttu-id="92b13-155">451</span><span class="sxs-lookup"><span data-stu-id="92b13-155">451</span></span>                      |
| <span data-ttu-id="92b13-156">4 月</span><span class="sxs-lookup"><span data-stu-id="92b13-156">April</span></span>    | <span data-ttu-id="92b13-157">119</span><span class="sxs-lookup"><span data-stu-id="92b13-157">119</span></span>                      |

<span data-ttu-id="92b13-158">毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="92b13-159">月</span><span class="sxs-lookup"><span data-stu-id="92b13-159">Month</span></span>                | <span data-ttu-id="92b13-160">必要な個数</span><span class="sxs-lookup"><span data-stu-id="92b13-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="92b13-161">1 月</span><span class="sxs-lookup"><span data-stu-id="92b13-161">January</span></span>              | <span data-ttu-id="92b13-162">44</span><span class="sxs-lookup"><span data-stu-id="92b13-162">44</span></span>                        |
| <span data-ttu-id="92b13-163">2 月</span><span class="sxs-lookup"><span data-stu-id="92b13-163">February</span></span>             | <span data-ttu-id="92b13-164">0</span><span class="sxs-lookup"><span data-stu-id="92b13-164">0</span></span>                         |
| <span data-ttu-id="92b13-165">3 月</span><span class="sxs-lookup"><span data-stu-id="92b13-165">March</span></span>                | <span data-ttu-id="92b13-166">549</span><span class="sxs-lookup"><span data-stu-id="92b13-166">549</span></span>                       |
| <span data-ttu-id="92b13-167">4 月</span><span class="sxs-lookup"><span data-stu-id="92b13-167">April</span></span>                | <span data-ttu-id="92b13-168">881</span><span class="sxs-lookup"><span data-stu-id="92b13-168">881</span></span>                       |
| <span data-ttu-id="92b13-169">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="92b13-169">May through December</span></span> | <span data-ttu-id="92b13-170">1.000</span><span class="sxs-lookup"><span data-stu-id="92b13-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="92b13-171">例 3: トランザクション - 動的期間の予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="92b13-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="92b13-172">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など)。</span><span class="sxs-lookup"><span data-stu-id="92b13-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="92b13-173">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="92b13-174">ただし、2 つの需要予測行の間の時間も、*暗黙に*期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="92b13-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="92b13-175">次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="92b13-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="92b13-176">日</span><span class="sxs-lookup"><span data-stu-id="92b13-176">Date</span></span>       | <span data-ttu-id="92b13-177">需要予測</span><span class="sxs-lookup"><span data-stu-id="92b13-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="92b13-178">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="92b13-178">January 1</span></span>  | <span data-ttu-id="92b13-179">1.000</span><span class="sxs-lookup"><span data-stu-id="92b13-179">1,000</span></span>           |
    | <span data-ttu-id="92b13-180">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="92b13-180">January 5</span></span>  | <span data-ttu-id="92b13-181">500</span><span class="sxs-lookup"><span data-stu-id="92b13-181">500</span></span>             |
    | <span data-ttu-id="92b13-182">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="92b13-182">January 12</span></span> | <span data-ttu-id="92b13-183">1.000</span><span class="sxs-lookup"><span data-stu-id="92b13-183">1,000</span></span>           |

    <span data-ttu-id="92b13-184">この予測では、予測日の間に明瞭な周期がありません。日付 1 と日付 2 の間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="92b13-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="92b13-185">このように周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="92b13-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="92b13-186">販売注文明細行を次のように作成します。</span><span class="sxs-lookup"><span data-stu-id="92b13-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="92b13-187">日</span><span class="sxs-lookup"><span data-stu-id="92b13-187">Date</span></span>                             | <span data-ttu-id="92b13-188">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="92b13-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="92b13-189">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="92b13-189">December 15 in the previous year</span></span> | <span data-ttu-id="92b13-190">500</span><span class="sxs-lookup"><span data-stu-id="92b13-190">500</span></span>                  |
    | <span data-ttu-id="92b13-191">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="92b13-191">January 3</span></span>                        | <span data-ttu-id="92b13-192">100</span><span class="sxs-lookup"><span data-stu-id="92b13-192">100</span></span>                  |
    | <span data-ttu-id="92b13-193">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="92b13-193">January 10</span></span>                       | <span data-ttu-id="92b13-194">200</span><span class="sxs-lookup"><span data-stu-id="92b13-194">200</span></span>                  |

<span data-ttu-id="92b13-195">予測は次のように減少します。</span><span class="sxs-lookup"><span data-stu-id="92b13-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="92b13-196">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="92b13-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="92b13-197">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="92b13-198">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="92b13-199">予測を達成するために次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="92b13-200">需要予測日</span><span class="sxs-lookup"><span data-stu-id="92b13-200">Demand forecast date</span></span> | <span data-ttu-id="92b13-201">数量の削減</span><span class="sxs-lookup"><span data-stu-id="92b13-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="92b13-202">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="92b13-202">January 1</span></span>            | <span data-ttu-id="92b13-203">900</span><span class="sxs-lookup"><span data-stu-id="92b13-203">900</span></span>              |
| <span data-ttu-id="92b13-204">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="92b13-204">January 5</span></span>            | <span data-ttu-id="92b13-205">300</span><span class="sxs-lookup"><span data-stu-id="92b13-205">300</span></span>              |
| <span data-ttu-id="92b13-206">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="92b13-206">January 12</span></span>           | <span data-ttu-id="92b13-207">1.000</span><span class="sxs-lookup"><span data-stu-id="92b13-207">1,000</span></span>            |

<span data-ttu-id="92b13-208">**トランザクション - 動的期間**の下方修正の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="92b13-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="92b13-209">予測要求は、動的期間中に発生する実際の注文トランザクションによって減算されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="92b13-210">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="92b13-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="92b13-211">この方法では、下方修正キーを使用せず、要求もしません。</span><span class="sxs-lookup"><span data-stu-id="92b13-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="92b13-212">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="92b13-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="92b13-213">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="92b13-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="92b13-214">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="92b13-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="92b13-215">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="92b13-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="92b13-216">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="92b13-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="92b13-217">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="92b13-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="92b13-218">参照</span><span class="sxs-lookup"><span data-stu-id="92b13-218">See also</span></span>
--------

[<span data-ttu-id="92b13-219">マスタ プラン</span><span class="sxs-lookup"><span data-stu-id="92b13-219">Master plans</span></span>](master-plans.md)




