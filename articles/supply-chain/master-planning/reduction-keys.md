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
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc2b63bfdec1c663027cb4e551589a705c2164e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431835"
---
# <a name="forecast-reduction-keys"></a><span data-ttu-id="ca5f0-105">予測下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-105">Forecast reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca5f0-106">このトピックでは、予測要求を減らすために使用されるさまざまな方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="ca5f0-107">これには、各メソッドの結果の例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="ca5f0-108">予測下方修正キーの作成、設定、および使用方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="ca5f0-109">予測要求を減らすため予測下方修正キーを使用するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="ca5f0-110">予測要求の削減に使用する方法</span><span class="sxs-lookup"><span data-stu-id="ca5f0-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="ca5f0-111">マスター プランに予測を含める場合、実際の需要が含まれるときに予測要求を削減する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span> <span data-ttu-id="ca5f0-112">マスター プランでは、過去から予測要求が除外されます。つまり、今日の日付より前のすべての予測要求が除外されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-112">Note that master planning excludes forecast requirements from the past, which means all forecast requirements before today's date.</span></span>

<span data-ttu-id="ca5f0-113">マスター プランに予測を含め、予測要求を減らすために使用される方法を選択するには、**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-113">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="ca5f0-114">**予測モデル** フィールドで、予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-114">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="ca5f0-115">**予測要求の削減に使用する方法** フィールドで、方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-115">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="ca5f0-116">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-116">The following options are available:</span></span>

- <span data-ttu-id="ca5f0-117">なし</span><span class="sxs-lookup"><span data-stu-id="ca5f0-117">None</span></span>
- <span data-ttu-id="ca5f0-118">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-118">Percent – reduction key</span></span>
- <span data-ttu-id="ca5f0-119">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-119">Transactions – reduction key</span></span>
- <span data-ttu-id="ca5f0-120">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="ca5f0-120">Transactions – dynamic period</span></span>

<span data-ttu-id="ca5f0-121">次のセクションでは、各オプションの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-121">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="ca5f0-122">なし</span><span class="sxs-lookup"><span data-stu-id="ca5f0-122">None</span></span>

<span data-ttu-id="ca5f0-123">**なし** を選択すると、予測要求はマスター スケジューリング時に削減されません。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-123">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="ca5f0-124">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-124">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="ca5f0-125">これらの計画オーダーは、他のタイプの需要に関係なく、推奨数量を管理します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-125">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="ca5f0-126">たとえば、販売注文が出された場合、マスター プランは販売注文を供給する追加の計画オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-126">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="ca5f0-127">予測要求の数量は削減されません。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-127">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="ca5f0-128">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-128">Percent – reduction key</span></span>

<span data-ttu-id="ca5f0-129">**率 - 下方修正キー** を選択すると、予測要求は下方修正キーで定義された割合および期間に従って削減されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-129">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="ca5f0-130">この場合、マスター プランでは各期間の予測数量 × 下方修正キーとして数量が計算される計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-130">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="ca5f0-131">他のタイプの需要がある場合、マスター プランではその要求を供給する計画オーダーも作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-131">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="ca5f0-132">例: 率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-132">Example: Percent – reduction key</span></span>

<span data-ttu-id="ca5f0-133">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-133">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="ca5f0-134">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-134">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="ca5f0-135">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-135">Month</span></span>    | <span data-ttu-id="ca5f0-136">需要予測</span><span class="sxs-lookup"><span data-stu-id="ca5f0-136">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="ca5f0-137">1 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-137">January</span></span>  | <span data-ttu-id="ca5f0-138">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-138">1,000</span></span>           |
| <span data-ttu-id="ca5f0-139">2 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-139">February</span></span> | <span data-ttu-id="ca5f0-140">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-140">1,000</span></span>           |
| <span data-ttu-id="ca5f0-141">3 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-141">March</span></span>    | <span data-ttu-id="ca5f0-142">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-142">1,000</span></span>           |
| <span data-ttu-id="ca5f0-143">4 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-143">April</span></span>    | <span data-ttu-id="ca5f0-144">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-144">1,000</span></span>           |

<span data-ttu-id="ca5f0-145">**下方修正キー** ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-145">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="ca5f0-146">計上額</span><span class="sxs-lookup"><span data-stu-id="ca5f0-146">Change</span></span> | <span data-ttu-id="ca5f0-147">単位</span><span class="sxs-lookup"><span data-stu-id="ca5f0-147">Unit</span></span>  | <span data-ttu-id="ca5f0-148">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="ca5f0-148">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="ca5f0-149">1</span><span class="sxs-lookup"><span data-stu-id="ca5f0-149">1</span></span>      | <span data-ttu-id="ca5f0-150">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-150">Month</span></span> | <span data-ttu-id="ca5f0-151">100</span><span class="sxs-lookup"><span data-stu-id="ca5f0-151">100</span></span>     |
| <span data-ttu-id="ca5f0-152">2</span><span class="sxs-lookup"><span data-stu-id="ca5f0-152">2</span></span>      | <span data-ttu-id="ca5f0-153">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-153">Month</span></span> | <span data-ttu-id="ca5f0-154">75</span><span class="sxs-lookup"><span data-stu-id="ca5f0-154">75</span></span>      |
| <span data-ttu-id="ca5f0-155">3</span><span class="sxs-lookup"><span data-stu-id="ca5f0-155">3</span></span>      | <span data-ttu-id="ca5f0-156">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-156">Month</span></span> | <span data-ttu-id="ca5f0-157">50</span><span class="sxs-lookup"><span data-stu-id="ca5f0-157">50</span></span>      |
| <span data-ttu-id="ca5f0-158">4</span><span class="sxs-lookup"><span data-stu-id="ca5f0-158">4</span></span>      | <span data-ttu-id="ca5f0-159">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-159">Month</span></span> | <span data-ttu-id="ca5f0-160">25</span><span class="sxs-lookup"><span data-stu-id="ca5f0-160">25</span></span>      |

<span data-ttu-id="ca5f0-161">品目の補充グループに下方修正キーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-161">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="ca5f0-162">その後、**マスター プラン** ページの **予測要求の削減に使用する方法** フィールドで、**率 - 下方修正キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-162">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="ca5f0-163">この場合、1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー** ページで設定した率に従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-163">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="ca5f0-164">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-164">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ca5f0-165">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-165">Month</span></span>                | <span data-ttu-id="ca5f0-166">計画オーダーの数量</span><span class="sxs-lookup"><span data-stu-id="ca5f0-166">Planned order quantity</span></span> | <span data-ttu-id="ca5f0-167">計算</span><span class="sxs-lookup"><span data-stu-id="ca5f0-167">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="ca5f0-168">1 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-168">January</span></span>              | <span data-ttu-id="ca5f0-169">0</span><span class="sxs-lookup"><span data-stu-id="ca5f0-169">0</span></span>                      | <span data-ttu-id="ca5f0-170">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-170">= 0% × 1,000</span></span>   |
| <span data-ttu-id="ca5f0-171">2 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-171">February</span></span>             | <span data-ttu-id="ca5f0-172">250</span><span class="sxs-lookup"><span data-stu-id="ca5f0-172">250</span></span>                    | <span data-ttu-id="ca5f0-173">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-173">= 25% × 1,000</span></span>  |
| <span data-ttu-id="ca5f0-174">3 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-174">March</span></span>                | <span data-ttu-id="ca5f0-175">500</span><span class="sxs-lookup"><span data-stu-id="ca5f0-175">500</span></span>                    | <span data-ttu-id="ca5f0-176">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-176">= 50% × 1,000</span></span>  |
| <span data-ttu-id="ca5f0-177">4 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-177">April</span></span>                | <span data-ttu-id="ca5f0-178">750</span><span class="sxs-lookup"><span data-stu-id="ca5f0-178">750</span></span>                    | <span data-ttu-id="ca5f0-179">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-179">= 75% × 1,000</span></span>  |
| <span data-ttu-id="ca5f0-180">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-180">May through December</span></span> | <span data-ttu-id="ca5f0-181">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-181">1,000</span></span>                  | <span data-ttu-id="ca5f0-182">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-182">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="ca5f0-183">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-183">Transactions – reduction key</span></span>

<span data-ttu-id="ca5f0-184">**トランザクション - 下方修正キー** を選択すると、予測要求は下方修正キーで定義された期間に発生するトランザクションによって削減されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-184">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="ca5f0-185">例: トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="ca5f0-185">Example: Transactions – reduction key</span></span>

<span data-ttu-id="ca5f0-186">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-186">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="ca5f0-187">この例では、**マスター プラン** ページの **予測要求の削減に使用する方法** フィールドで、**トランザクション – 下方修正キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-187">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="ca5f0-188">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-188">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="ca5f0-189">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-189">Month</span></span>    | <span data-ttu-id="ca5f0-190">注文数</span><span class="sxs-lookup"><span data-stu-id="ca5f0-190">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="ca5f0-191">1 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-191">January</span></span>  | <span data-ttu-id="ca5f0-192">956</span><span class="sxs-lookup"><span data-stu-id="ca5f0-192">956</span></span>                      |
| <span data-ttu-id="ca5f0-193">2 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-193">February</span></span> | <span data-ttu-id="ca5f0-194">1,176</span><span class="sxs-lookup"><span data-stu-id="ca5f0-194">1,176</span></span>                    |
| <span data-ttu-id="ca5f0-195">3 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-195">March</span></span>    | <span data-ttu-id="ca5f0-196">451</span><span class="sxs-lookup"><span data-stu-id="ca5f0-196">451</span></span>                      |
| <span data-ttu-id="ca5f0-197">4 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-197">April</span></span>    | <span data-ttu-id="ca5f0-198">119</span><span class="sxs-lookup"><span data-stu-id="ca5f0-198">119</span></span>                      |

<span data-ttu-id="ca5f0-199">前の例で使用した毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-199">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ca5f0-200">月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-200">Month</span></span>                | <span data-ttu-id="ca5f0-201">必要な個数</span><span class="sxs-lookup"><span data-stu-id="ca5f0-201">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="ca5f0-202">1 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-202">January</span></span>              | <span data-ttu-id="ca5f0-203">44</span><span class="sxs-lookup"><span data-stu-id="ca5f0-203">44</span></span>                        |
| <span data-ttu-id="ca5f0-204">2 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-204">February</span></span>             | <span data-ttu-id="ca5f0-205">0</span><span class="sxs-lookup"><span data-stu-id="ca5f0-205">0</span></span>                         |
| <span data-ttu-id="ca5f0-206">3 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-206">March</span></span>                | <span data-ttu-id="ca5f0-207">549</span><span class="sxs-lookup"><span data-stu-id="ca5f0-207">549</span></span>                       |
| <span data-ttu-id="ca5f0-208">4 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-208">April</span></span>                | <span data-ttu-id="ca5f0-209">881</span><span class="sxs-lookup"><span data-stu-id="ca5f0-209">881</span></span>                       |
| <span data-ttu-id="ca5f0-210">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-210">May through December</span></span> | <span data-ttu-id="ca5f0-211">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-211">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="ca5f0-212">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="ca5f0-212">Transactions – dynamic period</span></span>

<span data-ttu-id="ca5f0-213">**トランザクション - 動的期間** を選択する場合、予測要求が動的期間中に発生する実際の注文トランザクションから削減されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-213">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="ca5f0-214">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-214">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="ca5f0-215">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-215">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="ca5f0-216">ただし、実際の注文トランザクションが出されると、予測要求が削減されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-216">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="ca5f0-217">実際のトランザクションは、予測要求の一部を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-217">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="ca5f0-218">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-218">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="ca5f0-219">下方修正キーは必要でないまたは使用されません。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-219">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="ca5f0-220">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-220">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="ca5f0-221">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-221">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="ca5f0-222">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-222">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="ca5f0-223">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-223">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="ca5f0-224">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-224">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="ca5f0-225">例 1: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="ca5f0-225">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="ca5f0-226">ここでは、**トランザクション - 動的期間** メソッドの使用方法を示す簡単な例を上げます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-226">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="ca5f0-227">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-227">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="ca5f0-228">日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-228">Date</span></span>       | <span data-ttu-id="ca5f0-229">需要予測</span><span class="sxs-lookup"><span data-stu-id="ca5f0-229">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="ca5f0-230">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-230">January 1</span></span>  | <span data-ttu-id="ca5f0-231">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-231">1,000</span></span>           |
| <span data-ttu-id="ca5f0-232">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-232">February 1</span></span> | <span data-ttu-id="ca5f0-233">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-233">1,000</span></span>             |

<span data-ttu-id="ca5f0-234">次の販売注文も作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-234">You also create the following sales orders.</span></span>

| <span data-ttu-id="ca5f0-235">日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-235">Date</span></span>        | <span data-ttu-id="ca5f0-236">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="ca5f0-236">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="ca5f0-237">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-237">January 15</span></span>  | <span data-ttu-id="ca5f0-238">200</span><span class="sxs-lookup"><span data-stu-id="ca5f0-238">200</span></span>                  |
| <span data-ttu-id="ca5f0-239">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-239">February 15</span></span> | <span data-ttu-id="ca5f0-240">400</span><span class="sxs-lookup"><span data-stu-id="ca5f0-240">400</span></span>                  |

<span data-ttu-id="ca5f0-241">この場合、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-241">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="ca5f0-242">需要予測日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-242">Demand forecast date</span></span> | <span data-ttu-id="ca5f0-243">件数</span><span class="sxs-lookup"><span data-stu-id="ca5f0-243">Quantity</span></span> | <span data-ttu-id="ca5f0-244">説明</span><span class="sxs-lookup"><span data-stu-id="ca5f0-244">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="ca5f0-245">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-245">January 1</span></span>            | <span data-ttu-id="ca5f0-246">800</span><span class="sxs-lookup"><span data-stu-id="ca5f0-246">800</span></span>      | <span data-ttu-id="ca5f0-247">予測要求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="ca5f0-247">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="ca5f0-248">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-248">January 15</span></span>           | <span data-ttu-id="ca5f0-249">200</span><span class="sxs-lookup"><span data-stu-id="ca5f0-249">200</span></span>      | <span data-ttu-id="ca5f0-250">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="ca5f0-250">Sales orders requirements</span></span>             |
| <span data-ttu-id="ca5f0-251">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-251">February 1</span></span>           | <span data-ttu-id="ca5f0-252">600</span><span class="sxs-lookup"><span data-stu-id="ca5f0-252">600</span></span>      | <span data-ttu-id="ca5f0-253">予測要求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="ca5f0-253">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="ca5f0-254">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="ca5f0-254">February 15</span></span>          | <span data-ttu-id="ca5f0-255">400</span><span class="sxs-lookup"><span data-stu-id="ca5f0-255">400</span></span>      | <span data-ttu-id="ca5f0-256">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="ca5f0-256">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="ca5f0-257">例 2: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="ca5f0-257">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="ca5f0-258">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-258">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="ca5f0-259">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-259">These periods are defined in the reduction key.</span></span> <span data-ttu-id="ca5f0-260">ただし、2 つの需要予測行の間の時間も、*暗黙に* 期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-260">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="ca5f0-261">この例では、次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-261">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="ca5f0-262">日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-262">Date</span></span>       | <span data-ttu-id="ca5f0-263">需要予測</span><span class="sxs-lookup"><span data-stu-id="ca5f0-263">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="ca5f0-264">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-264">January 1</span></span>  | <span data-ttu-id="ca5f0-265">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-265">1,000</span></span>           |
| <span data-ttu-id="ca5f0-266">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-266">January 5</span></span>  | <span data-ttu-id="ca5f0-267">500</span><span class="sxs-lookup"><span data-stu-id="ca5f0-267">500</span></span>             |
| <span data-ttu-id="ca5f0-268">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-268">January 12</span></span> | <span data-ttu-id="ca5f0-269">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-269">1,000</span></span>           |

<span data-ttu-id="ca5f0-270">この予測では、予測日の間にクリア期間がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-270">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="ca5f0-271">日付 1 と日付 2 と間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-271">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="ca5f0-272">このような周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-272">These spans are the dynamic periods.</span></span>

<span data-ttu-id="ca5f0-273">次の販売注文明細行も作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-273">You also create the following sales order lines.</span></span>

| <span data-ttu-id="ca5f0-274">日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-274">Date</span></span>                             | <span data-ttu-id="ca5f0-275">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="ca5f0-275">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="ca5f0-276">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-276">December 15 in the previous year</span></span> | <span data-ttu-id="ca5f0-277">500</span><span class="sxs-lookup"><span data-stu-id="ca5f0-277">500</span></span>                  |
| <span data-ttu-id="ca5f0-278">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-278">January 3</span></span>                        | <span data-ttu-id="ca5f0-279">100</span><span class="sxs-lookup"><span data-stu-id="ca5f0-279">100</span></span>                  |
| <span data-ttu-id="ca5f0-280">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-280">January 10</span></span>                       | <span data-ttu-id="ca5f0-281">200</span><span class="sxs-lookup"><span data-stu-id="ca5f0-281">200</span></span>                  |

<span data-ttu-id="ca5f0-282">この場合、次のように予測が削減されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-282">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="ca5f0-283">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-283">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="ca5f0-284">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-284">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="ca5f0-285">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-285">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="ca5f0-286">したがって、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-286">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="ca5f0-287">需要予測日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-287">Demand forecast date</span></span>             | <span data-ttu-id="ca5f0-288">件数</span><span class="sxs-lookup"><span data-stu-id="ca5f0-288">Quantity</span></span> | <span data-ttu-id="ca5f0-289">説明</span><span class="sxs-lookup"><span data-stu-id="ca5f0-289">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="ca5f0-290">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-290">December 15 in the previous year</span></span> | <span data-ttu-id="ca5f0-291">500</span><span class="sxs-lookup"><span data-stu-id="ca5f0-291">500</span></span>      | <span data-ttu-id="ca5f0-292">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="ca5f0-292">Sales order requirements</span></span>                                            |
| <span data-ttu-id="ca5f0-293">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-293">January 1</span></span>                        | <span data-ttu-id="ca5f0-294">900</span><span class="sxs-lookup"><span data-stu-id="ca5f0-294">900</span></span>      | <span data-ttu-id="ca5f0-295">1 月 1 日から 1 月 5 日の期間の予測要求 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="ca5f0-295">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="ca5f0-296">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-296">January 3</span></span>                        | <span data-ttu-id="ca5f0-297">100</span><span class="sxs-lookup"><span data-stu-id="ca5f0-297">100</span></span>      | <span data-ttu-id="ca5f0-298">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="ca5f0-298">Sales order requirements</span></span>                                            |
| <span data-ttu-id="ca5f0-299">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-299">January 5</span></span>                        | <span data-ttu-id="ca5f0-300">300</span><span class="sxs-lookup"><span data-stu-id="ca5f0-300">300</span></span>      | <span data-ttu-id="ca5f0-301">1 月 5 日から 1 月 10 日の期間の予測要求 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="ca5f0-301">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="ca5f0-302">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="ca5f0-302">January 12</span></span>                       | <span data-ttu-id="ca5f0-303">1.000</span><span class="sxs-lookup"><span data-stu-id="ca5f0-303">1,000</span></span>    | <span data-ttu-id="ca5f0-304">1 月 12 日から終了日の期間の予測要求</span><span class="sxs-lookup"><span data-stu-id="ca5f0-304">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="ca5f0-305">予測下方修正キーの作成および設定</span><span class="sxs-lookup"><span data-stu-id="ca5f0-305">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="ca5f0-306">予測下方修正キーは、予測要求を削減するため **トランザクション - 下方修正キー** および **率 - 下方修正キー** の方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-306">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="ca5f0-307">下方修正キーを作成および設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-307">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="ca5f0-308">**マスター プラン \> 設定 \> 補充 \> 下方修正キー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-308">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="ca5f0-309">**新規** を選択または **Ctrl+N** を押して下方修正キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-309">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="ca5f0-310">**下方修正キー** フィールドで、予測下方修正キーの固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-310">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="ca5f0-311">その後、**名前** フィールドで、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-311">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="ca5f0-312">各期間の期間および下方修正キーの割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-312">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="ca5f0-313">**有効日** フィールドは、期間の作成が開始する日付を示します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-313">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="ca5f0-314">**有効日を使用** オプションを **はい** に設定すると、有効日の期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-314">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="ca5f0-315">**いいえ** に設定すると、マスター プランが実行される日付で期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-315">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="ca5f0-316">予測下方修正が発生する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-316">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="ca5f0-317">特定の期間の、予測要求を削減する必要がある割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-317">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="ca5f0-318">要件を削減するには正の値、または要件を増加するには負の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-318">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="ca5f0-319">下方修正キーの使用</span><span class="sxs-lookup"><span data-stu-id="ca5f0-319">Use a reduction key</span></span>

<span data-ttu-id="ca5f0-320">予測下方修正キーは、品目の補充グループに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-320">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="ca5f0-321">これらの手順に従い、下方修正キーを品目の補充グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-321">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="ca5f0-322">**マスター プラン \> 設定 \> 補充 \> 補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-322">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="ca5f0-323">**その他** クイック タブの、**下方修正キー** フィールドで、補充グループに割り当てる下方修正キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-323">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="ca5f0-324">その後、下方修正キーは、補充グループに属する品目すべてに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-324">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="ca5f0-325">マスター スケジューリング時に予測下方修正の計算に下方修正キーを使用するには、予測計画またはマスター プランの設定でこの設定を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-325">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="ca5f0-326">次の場所のいずれかに移動します:</span><span class="sxs-lookup"><span data-stu-id="ca5f0-326">Go to one of the following locations:</span></span>

    - <span data-ttu-id="ca5f0-327">マスター プラン \> 設定 \> 計画 \> 予測計画</span><span class="sxs-lookup"><span data-stu-id="ca5f0-327">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="ca5f0-328">マスター プラン \> 設定 \> 計画 \> マスター プラン</span><span class="sxs-lookup"><span data-stu-id="ca5f0-328">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="ca5f0-329">**予測計画** または **マスター プラン** ページの、**一般** クイック タブの、**予測要求の削減に使用する方法** フィールドで、**率 - 下方修正キー** または **トランザクション - 下方修正キー** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-329">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="ca5f0-330">トランザクションによる予測の削減</span><span class="sxs-lookup"><span data-stu-id="ca5f0-330">Reduce a forecast by transactions</span></span>

<span data-ttu-id="ca5f0-331">予測要求の削減のメソッドとして **トランザクション - 下方修正キー** または **トランザクション - 動的期間** を選択すると、予測を削減するトランザクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-331">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="ca5f0-332">**補充グループ** ページの、**その他** クイック タブにある、**予測の削減方法** フィールドで、すべてのトランザクションで予測を削減する必要がある場合は **すべてのトランザクション** を、または販売注文のみで予測を削減する必要がある場合は **販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca5f0-332">On the **Coverage groups** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca5f0-333">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ca5f0-333">Additional resources</span></span>

[<span data-ttu-id="ca5f0-334">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="ca5f0-334">Master plans overview</span></span>](master-plans.md)
