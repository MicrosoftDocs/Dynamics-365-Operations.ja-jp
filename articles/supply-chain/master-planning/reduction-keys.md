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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4b7f4ebd635e02f3cfc6d0f620dad30e6b1a98a2
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="reduction-keys"></a><span data-ttu-id="4f2d0-105">下方修正キー</span><span class="sxs-lookup"><span data-stu-id="4f2d0-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f2d0-106">この記事は、下方修正キーを設定する方法を示す例を提供します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="4f2d0-107">これには、さまざまな下方修正キーの設定とそれぞれの結果に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="4f2d0-108">予測要求を減らす方法を定義するには下方修正キーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="4f2d0-109">例 1: 割合 -下方修正キーの予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="4f2d0-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="4f2d0-110">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="4f2d0-111">**下方修正キー** ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="4f2d0-112">計上額</span><span class="sxs-lookup"><span data-stu-id="4f2d0-112">Change</span></span> | <span data-ttu-id="4f2d0-113">単位</span><span class="sxs-lookup"><span data-stu-id="4f2d0-113">Unit</span></span>  | <span data-ttu-id="4f2d0-114">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="4f2d0-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="4f2d0-115">1</span><span class="sxs-lookup"><span data-stu-id="4f2d0-115">1</span></span>    | <span data-ttu-id="4f2d0-116">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-116">Month</span></span> |   <span data-ttu-id="4f2d0-117">100</span><span class="sxs-lookup"><span data-stu-id="4f2d0-117">100</span></span>   |
   |   <span data-ttu-id="4f2d0-118">2</span><span class="sxs-lookup"><span data-stu-id="4f2d0-118">2</span></span>    | <span data-ttu-id="4f2d0-119">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-119">Month</span></span> |   <span data-ttu-id="4f2d0-120">75</span><span class="sxs-lookup"><span data-stu-id="4f2d0-120">75</span></span>    |
   |   <span data-ttu-id="4f2d0-121">3</span><span class="sxs-lookup"><span data-stu-id="4f2d0-121">3</span></span>    | <span data-ttu-id="4f2d0-122">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-122">Month</span></span> |   <span data-ttu-id="4f2d0-123">50</span><span class="sxs-lookup"><span data-stu-id="4f2d0-123">50</span></span>    |
   |   <span data-ttu-id="4f2d0-124">4</span><span class="sxs-lookup"><span data-stu-id="4f2d0-124">4</span></span>    | <span data-ttu-id="4f2d0-125">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-125">Month</span></span> |   <span data-ttu-id="4f2d0-126">25</span><span class="sxs-lookup"><span data-stu-id="4f2d0-126">25</span></span>    |


2. <span data-ttu-id="4f2d0-127">品目の補充グループに下方修正キーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="4f2d0-128">**マスター プラン** ページで、**下方修正原則**フィールドで**割合 - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="4f2d0-129">毎月 1,000 個の需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="4f2d0-130">1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー**ページで設定したパーセンテージに従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="4f2d0-131">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="4f2d0-132">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-132">Month</span></span>                | <span data-ttu-id="4f2d0-133">必要な個数</span><span class="sxs-lookup"><span data-stu-id="4f2d0-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="4f2d0-134">1 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-134">January</span></span>              | <span data-ttu-id="4f2d0-135">0</span><span class="sxs-lookup"><span data-stu-id="4f2d0-135">0</span></span>                         |
| <span data-ttu-id="4f2d0-136">2 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-136">February</span></span>             | <span data-ttu-id="4f2d0-137">250</span><span class="sxs-lookup"><span data-stu-id="4f2d0-137">250</span></span>                       |
| <span data-ttu-id="4f2d0-138">3 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-138">March</span></span>                | <span data-ttu-id="4f2d0-139">500</span><span class="sxs-lookup"><span data-stu-id="4f2d0-139">500</span></span>                       |
| <span data-ttu-id="4f2d0-140">4 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-140">April</span></span>                | <span data-ttu-id="4f2d0-141">750</span><span class="sxs-lookup"><span data-stu-id="4f2d0-141">750</span></span>                       |
| <span data-ttu-id="4f2d0-142">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-142">May through December</span></span> | <span data-ttu-id="4f2d0-143">1.000</span><span class="sxs-lookup"><span data-stu-id="4f2d0-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="4f2d0-144">例 2: トランザクション - 下方修正キーの予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="4f2d0-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="4f2d0-145">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="4f2d0-146">**マスター プラン** ページで、**下方修正原則**フィールドで**トランザクション - 下方修正キー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="4f2d0-147">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="4f2d0-148">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-148">Month</span></span>    | <span data-ttu-id="4f2d0-149">注文数</span><span class="sxs-lookup"><span data-stu-id="4f2d0-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="4f2d0-150">1 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-150">January</span></span>  | <span data-ttu-id="4f2d0-151">956</span><span class="sxs-lookup"><span data-stu-id="4f2d0-151">956</span></span>                      |
| <span data-ttu-id="4f2d0-152">2 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-152">February</span></span> | <span data-ttu-id="4f2d0-153">1,176</span><span class="sxs-lookup"><span data-stu-id="4f2d0-153">1,176</span></span>                    |
| <span data-ttu-id="4f2d0-154">3 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-154">March</span></span>    | <span data-ttu-id="4f2d0-155">451</span><span class="sxs-lookup"><span data-stu-id="4f2d0-155">451</span></span>                      |
| <span data-ttu-id="4f2d0-156">4 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-156">April</span></span>    | <span data-ttu-id="4f2d0-157">119</span><span class="sxs-lookup"><span data-stu-id="4f2d0-157">119</span></span>                      |

<span data-ttu-id="4f2d0-158">毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="4f2d0-159">月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-159">Month</span></span>                | <span data-ttu-id="4f2d0-160">必要な個数</span><span class="sxs-lookup"><span data-stu-id="4f2d0-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="4f2d0-161">1 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-161">January</span></span>              | <span data-ttu-id="4f2d0-162">44</span><span class="sxs-lookup"><span data-stu-id="4f2d0-162">44</span></span>                        |
| <span data-ttu-id="4f2d0-163">2 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-163">February</span></span>             | <span data-ttu-id="4f2d0-164">0</span><span class="sxs-lookup"><span data-stu-id="4f2d0-164">0</span></span>                         |
| <span data-ttu-id="4f2d0-165">3 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-165">March</span></span>                | <span data-ttu-id="4f2d0-166">549</span><span class="sxs-lookup"><span data-stu-id="4f2d0-166">549</span></span>                       |
| <span data-ttu-id="4f2d0-167">4 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-167">April</span></span>                | <span data-ttu-id="4f2d0-168">881</span><span class="sxs-lookup"><span data-stu-id="4f2d0-168">881</span></span>                       |
| <span data-ttu-id="4f2d0-169">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="4f2d0-169">May through December</span></span> | <span data-ttu-id="4f2d0-170">1.000</span><span class="sxs-lookup"><span data-stu-id="4f2d0-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="4f2d0-171">例 3: トランザクション - 動的期間の予測下方修正原則</span><span class="sxs-lookup"><span data-stu-id="4f2d0-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="4f2d0-172">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など)。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="4f2d0-173">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="4f2d0-174">ただし、2 つの需要予測行の間の時間も、*暗黙に*期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="4f2d0-175">次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="4f2d0-176">日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-176">Date</span></span>       | <span data-ttu-id="4f2d0-177">需要予測</span><span class="sxs-lookup"><span data-stu-id="4f2d0-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="4f2d0-178">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-178">January 1</span></span>  | <span data-ttu-id="4f2d0-179">1.000</span><span class="sxs-lookup"><span data-stu-id="4f2d0-179">1,000</span></span>           |
   | <span data-ttu-id="4f2d0-180">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-180">January 5</span></span>  | <span data-ttu-id="4f2d0-181">500</span><span class="sxs-lookup"><span data-stu-id="4f2d0-181">500</span></span>             |
   | <span data-ttu-id="4f2d0-182">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-182">January 12</span></span> | <span data-ttu-id="4f2d0-183">1.000</span><span class="sxs-lookup"><span data-stu-id="4f2d0-183">1,000</span></span>           |

   <span data-ttu-id="4f2d0-184">この予測では、予測日の間に明瞭な周期がありません。日付 1 と日付 2 の間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="4f2d0-185">このように周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="4f2d0-186">販売注文明細行を次のように作成します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="4f2d0-187">日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-187">Date</span></span>                             | <span data-ttu-id="4f2d0-188">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="4f2d0-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="4f2d0-189">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-189">December 15 in the previous year</span></span> | <span data-ttu-id="4f2d0-190">500</span><span class="sxs-lookup"><span data-stu-id="4f2d0-190">500</span></span>                  |
   | <span data-ttu-id="4f2d0-191">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-191">January 3</span></span>                        | <span data-ttu-id="4f2d0-192">100</span><span class="sxs-lookup"><span data-stu-id="4f2d0-192">100</span></span>                  |
   | <span data-ttu-id="4f2d0-193">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-193">January 10</span></span>                       | <span data-ttu-id="4f2d0-194">200</span><span class="sxs-lookup"><span data-stu-id="4f2d0-194">200</span></span>                  |

<span data-ttu-id="4f2d0-195">予測は次のように減少します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="4f2d0-196">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="4f2d0-197">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="4f2d0-198">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="4f2d0-199">予測を達成するために次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="4f2d0-200">需要予測日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-200">Demand forecast date</span></span> | <span data-ttu-id="4f2d0-201">数量の削減</span><span class="sxs-lookup"><span data-stu-id="4f2d0-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="4f2d0-202">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-202">January 1</span></span>            | <span data-ttu-id="4f2d0-203">900</span><span class="sxs-lookup"><span data-stu-id="4f2d0-203">900</span></span>              |
| <span data-ttu-id="4f2d0-204">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-204">January 5</span></span>            | <span data-ttu-id="4f2d0-205">300</span><span class="sxs-lookup"><span data-stu-id="4f2d0-205">300</span></span>              |
| <span data-ttu-id="4f2d0-206">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="4f2d0-206">January 12</span></span>           | <span data-ttu-id="4f2d0-207">1.000</span><span class="sxs-lookup"><span data-stu-id="4f2d0-207">1,000</span></span>            |

<span data-ttu-id="4f2d0-208">**トランザクション - 動的期間**の下方修正の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="4f2d0-209">予測要求は、動的期間中に発生する実際の注文トランザクションによって減算されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="4f2d0-210">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="4f2d0-211">この方法では、下方修正キーを使用せず、要求もしません。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="4f2d0-212">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="4f2d0-213">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="4f2d0-214">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="4f2d0-215">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="4f2d0-216">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="4f2d0-217">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="4f2d0-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="4f2d0-218">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4f2d0-218">Additional resources</span></span>
--------

[<span data-ttu-id="4f2d0-219">マスター プラン</span><span class="sxs-lookup"><span data-stu-id="4f2d0-219">Master plans</span></span>](master-plans.md)




