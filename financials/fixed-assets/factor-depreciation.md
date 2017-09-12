---
title: "係数減価償却"
description: "この記事は、係数償却方法の減価償却の概要を示します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: ja-jp
ms.lasthandoff: 06/29/2017


---

# <a name="factor-depreciation"></a><span data-ttu-id="49305-103">係数減価償却</span><span class="sxs-lookup"><span data-stu-id="49305-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="49305-104">この記事は、係数償却方法の減価償却の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="49305-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="49305-105">係数は、資産の減価償却に使用される比率です。</span><span class="sxs-lookup"><span data-stu-id="49305-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="49305-106">固定資産減価償却プロファイルを設定し、**減価償却プロファイル** ページの**方法**フィールドで**係数**を選択すると、累進的減価償却、累減的減価償却、または定額減価償却を設定できます。</span><span class="sxs-lookup"><span data-stu-id="49305-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="49305-107">累進的減価償却では、減価償却期間ごとに減価償却金額は増加します。</span><span class="sxs-lookup"><span data-stu-id="49305-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="49305-108">累減的減価償却では、期間ごとの減価償却金額はしだいに減少します。</span><span class="sxs-lookup"><span data-stu-id="49305-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="49305-109">定額法では、各期間の減価償却金額は同じになります。</span><span class="sxs-lookup"><span data-stu-id="49305-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="49305-110">次のルールと例は、減価償却の各タイプに対して、係数をどのように設定できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="49305-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="49305-111">**方法**フィールドで**係数**を選択すると、**係数**フィールドおよび**間隔**フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="49305-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="49305-112">累進的減価償却</span><span class="sxs-lookup"><span data-stu-id="49305-112">Progressive depreciation</span></span>
<span data-ttu-id="49305-113">**係数**フィールドの値は **50** より大きくなります。</span><span class="sxs-lookup"><span data-stu-id="49305-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="49305-114">例</span><span class="sxs-lookup"><span data-stu-id="49305-114">Example</span></span>

<span data-ttu-id="49305-115">取得価格は 100,000、係数は 70、耐用年数は 10 年、および減価償却は 1 月 1 日から開始します。</span><span class="sxs-lookup"><span data-stu-id="49305-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="49305-116">減価償却金額と正味簿価額の金額は、耐用年数の最初 6 年間のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="49305-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="49305-117">年</span><span class="sxs-lookup"><span data-stu-id="49305-117">Year</span></span> | <span data-ttu-id="49305-118">期間</span><span class="sxs-lookup"><span data-stu-id="49305-118">Period</span></span>      | <span data-ttu-id="49305-119">減価償却金額</span><span class="sxs-lookup"><span data-stu-id="49305-119">Depreciation amount</span></span> | <span data-ttu-id="49305-120">正味簿価金額</span><span class="sxs-lookup"><span data-stu-id="49305-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="49305-121">1</span><span class="sxs-lookup"><span data-stu-id="49305-121">1</span></span>    | <span data-ttu-id="49305-122">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-122">December 31</span></span> | <span data-ttu-id="49305-123">307.69</span><span class="sxs-lookup"><span data-stu-id="49305-123">307.69</span></span>              | <span data-ttu-id="49305-124">99,692.31</span><span class="sxs-lookup"><span data-stu-id="49305-124">99,692.31</span></span>             |
| <span data-ttu-id="49305-125">2</span><span class="sxs-lookup"><span data-stu-id="49305-125">2</span></span>    | <span data-ttu-id="49305-126">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-126">December 31</span></span> | <span data-ttu-id="49305-127">1,447.21</span><span class="sxs-lookup"><span data-stu-id="49305-127">1,447.21</span></span>            | <span data-ttu-id="49305-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="49305-128">98,245.10</span></span>             |
| <span data-ttu-id="49305-129">3</span><span class="sxs-lookup"><span data-stu-id="49305-129">3</span></span>    | <span data-ttu-id="49305-130">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-130">December 31</span></span> | <span data-ttu-id="49305-131">3,104.50</span><span class="sxs-lookup"><span data-stu-id="49305-131">3,104.50</span></span>            | <span data-ttu-id="49305-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="49305-132">95,140.60</span></span>             |
| <span data-ttu-id="49305-133">4</span><span class="sxs-lookup"><span data-stu-id="49305-133">4</span></span>    | <span data-ttu-id="49305-134">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-134">December 31</span></span> | <span data-ttu-id="49305-135">5,150.21</span><span class="sxs-lookup"><span data-stu-id="49305-135">5,150.21</span></span>            | <span data-ttu-id="49305-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="49305-136">89,990.39</span></span>             |
| <span data-ttu-id="49305-137">5</span><span class="sxs-lookup"><span data-stu-id="49305-137">5</span></span>    | <span data-ttu-id="49305-138">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-138">December 31</span></span> | <span data-ttu-id="49305-139">7,522.95</span><span class="sxs-lookup"><span data-stu-id="49305-139">7,522.95</span></span>            | <span data-ttu-id="49305-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="49305-140">82,467.44</span></span>             |
| <span data-ttu-id="49305-141">6</span><span class="sxs-lookup"><span data-stu-id="49305-141">6</span></span>    | <span data-ttu-id="49305-142">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-142">December 31</span></span> | <span data-ttu-id="49305-143">10,184.06</span><span class="sxs-lookup"><span data-stu-id="49305-143">10,184.06</span></span>           | <span data-ttu-id="49305-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="49305-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="49305-145">累減的減価償却</span><span class="sxs-lookup"><span data-stu-id="49305-145">Digressive depreciation</span></span>
<span data-ttu-id="49305-146">**係数**フィールドの値は **50** より小さくなります。</span><span class="sxs-lookup"><span data-stu-id="49305-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="49305-147">例</span><span class="sxs-lookup"><span data-stu-id="49305-147">Example</span></span>

<span data-ttu-id="49305-148">取得価格は 100,000、係数は 20、耐用年数は 10 年、および減価償却は 1 月 1 日から開始します。</span><span class="sxs-lookup"><span data-stu-id="49305-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="49305-149">減価償却金額と正味簿価額の金額は、耐用年数の最初 6 年間のみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="49305-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="49305-150">年</span><span class="sxs-lookup"><span data-stu-id="49305-150">Year</span></span> | <span data-ttu-id="49305-151">期間</span><span class="sxs-lookup"><span data-stu-id="49305-151">Period</span></span>      | <span data-ttu-id="49305-152">減価償却金額</span><span class="sxs-lookup"><span data-stu-id="49305-152">Depreciation amount</span></span> | <span data-ttu-id="49305-153">正味簿価金額</span><span class="sxs-lookup"><span data-stu-id="49305-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="49305-154">1</span><span class="sxs-lookup"><span data-stu-id="49305-154">1</span></span>    | <span data-ttu-id="49305-155">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-155">December 31</span></span> | <span data-ttu-id="49305-156">56,080.43</span><span class="sxs-lookup"><span data-stu-id="49305-156">56,080.43</span></span>           | <span data-ttu-id="49305-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="49305-157">43,919.57</span></span>             |
| <span data-ttu-id="49305-158">2</span><span class="sxs-lookup"><span data-stu-id="49305-158">2</span></span>    | <span data-ttu-id="49305-159">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-159">December 31</span></span> | <span data-ttu-id="49305-160">10,665.70</span><span class="sxs-lookup"><span data-stu-id="49305-160">10,665.70</span></span>           | <span data-ttu-id="49305-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="49305-161">33,253.87</span></span>             |
| <span data-ttu-id="49305-162">3</span><span class="sxs-lookup"><span data-stu-id="49305-162">3</span></span>    | <span data-ttu-id="49305-163">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-163">December 31</span></span> | <span data-ttu-id="49305-164">7,156.22</span><span class="sxs-lookup"><span data-stu-id="49305-164">7,156.22</span></span>            | <span data-ttu-id="49305-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="49305-165">26,097.65</span></span>             |
| <span data-ttu-id="49305-166">4</span><span class="sxs-lookup"><span data-stu-id="49305-166">4</span></span>    | <span data-ttu-id="49305-167">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-167">December 31</span></span> | <span data-ttu-id="49305-168">5,538.06</span><span class="sxs-lookup"><span data-stu-id="49305-168">5,538.06</span></span>            | <span data-ttu-id="49305-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="49305-169">20,559.59</span></span>             |
| <span data-ttu-id="49305-170">5</span><span class="sxs-lookup"><span data-stu-id="49305-170">5</span></span>    | <span data-ttu-id="49305-171">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-171">December 31</span></span> | <span data-ttu-id="49305-172">4,579.89</span><span class="sxs-lookup"><span data-stu-id="49305-172">4,579.89</span></span>            | <span data-ttu-id="49305-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="49305-173">15,979.70</span></span>             |
| <span data-ttu-id="49305-174">6</span><span class="sxs-lookup"><span data-stu-id="49305-174">6</span></span>    | <span data-ttu-id="49305-175">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="49305-175">December 31</span></span> | <span data-ttu-id="49305-176">3,937.36</span><span class="sxs-lookup"><span data-stu-id="49305-176">3,937.36</span></span>            | <span data-ttu-id="49305-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="49305-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="49305-178">定額減価償却</span><span class="sxs-lookup"><span data-stu-id="49305-178">Straight line depreciation</span></span>
<span data-ttu-id="49305-179">**係数**フィールドの値は、**50** に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="49305-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="49305-180">この場合、各期間の減価償却額は同じになり、「[耐用年数定額減価償却](straight-line-service-life-depreciation.md)」での説明に従って、他のフィールドでの選択の関連について考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49305-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




