---
title: "X++ ビジネス ランタイム関数"
description: "このトピックでは、ビジネス ランタイム関数について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31281
ms.assetid: 7107cd00-ecb0-46d2-91d6-c342e4314345
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 13f945a77920783c3e9d49874c367e6edb0692db
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="x-business-run-time-functions"></a><span data-ttu-id="23e50-103">X++ ビジネス ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="23e50-103">X++ business run-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23e50-104">このトピックでは、ビジネス ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="23e50-104">This topic describes the business run-time functions.</span></span>

<span data-ttu-id="23e50-105">これらの関数は財務データを入力し、式を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-105">These functions enter financial data and calculate formulas.</span></span>

## <a name="cterm"></a><span data-ttu-id="23e50-106">cTerm</span><span class="sxs-lookup"><span data-stu-id="23e50-106">cTerm</span></span>
<span data-ttu-id="23e50-107">現在の投資価値がターゲット値に達するために必要な期間の数を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-107">Calculates the number of periods that are required for the current investment value to yield a target value.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-108">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-108">Syntax</span></span>

    real cTerm(real interest, real future_value, real current_value)

### <a name="parameters"></a><span data-ttu-id="23e50-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-109">Parameters</span></span>

| <span data-ttu-id="23e50-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-110">Parameter</span></span>      | <span data-ttu-id="23e50-111">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-111">Description</span></span>                   |
|----------------|-------------------------------|
| <span data-ttu-id="23e50-112">利息</span><span class="sxs-lookup"><span data-stu-id="23e50-112">interest</span></span>       | <span data-ttu-id="23e50-113">利率。</span><span class="sxs-lookup"><span data-stu-id="23e50-113">The interest rate.</span></span>            |
| <span data-ttu-id="23e50-114">future\_value</span><span class="sxs-lookup"><span data-stu-id="23e50-114">future\_value</span></span>  | <span data-ttu-id="23e50-115">ターゲット値。</span><span class="sxs-lookup"><span data-stu-id="23e50-115">The target value.</span></span>             |
| <span data-ttu-id="23e50-116">current\_value</span><span class="sxs-lookup"><span data-stu-id="23e50-116">current\_value</span></span> | <span data-ttu-id="23e50-117">現在の投資価値。</span><span class="sxs-lookup"><span data-stu-id="23e50-117">The current investment value.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-118">Return value</span></span>

<span data-ttu-id="23e50-119">*future\_value* に達するために必要な期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-119">The number of periods that are required in order to reach *future\_value*.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-120">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-120">Remarks</span></span>

<span data-ttu-id="23e50-121">*current\_value* および *future\_value* パラメーターには、同じ接頭辞記号 (プラスまたはマイナス) が付いています。</span><span class="sxs-lookup"><span data-stu-id="23e50-121">The *current\_value* and *future\_value* parameters must have the same prefixed sign (plus or minus).</span></span>

### <a name="example"></a><span data-ttu-id="23e50-122">例</span><span class="sxs-lookup"><span data-stu-id="23e50-122">Example</span></span>

    static void cTermExample(Args _arg)
    {
        real r;
        ;
        r = cTerm(10.0, 500.00, 100.00);
        print "The cTerm is " + num2Str(r, 2, 2, 1, 1);
        pause;
    }

<a name="ddb"></a><span data-ttu-id="23e50-123">ddb</span><span class="sxs-lookup"><span data-stu-id="23e50-123">ddb</span></span>
---

<span data-ttu-id="23e50-124">資産の増加償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-124">Calculates the accelerated depreciation of an asset.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-125">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-125">Syntax</span></span>

    real ddb(real price, real scrap, real life, int period)

### <a name="parameters"></a><span data-ttu-id="23e50-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-126">Parameters</span></span>

| <span data-ttu-id="23e50-127">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-127">Parameter</span></span> | <span data-ttu-id="23e50-128">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-128">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| <span data-ttu-id="23e50-129">価格</span><span class="sxs-lookup"><span data-stu-id="23e50-129">price</span></span>     | <span data-ttu-id="23e50-130">アセットの購買価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-130">The purchase price of the asset.</span></span>                           |
| <span data-ttu-id="23e50-131">仕損</span><span class="sxs-lookup"><span data-stu-id="23e50-131">scrap</span></span>     | <span data-ttu-id="23e50-132">損金処理された資産の残存価値。</span><span class="sxs-lookup"><span data-stu-id="23e50-132">The residual value of the asset that has been written off.</span></span> |
| <span data-ttu-id="23e50-133">life</span><span class="sxs-lookup"><span data-stu-id="23e50-133">life</span></span>      | <span data-ttu-id="23e50-134">資産の予想有効期間。</span><span class="sxs-lookup"><span data-stu-id="23e50-134">The expected lifetime of the asset.</span></span>                        |
| <span data-ttu-id="23e50-135">期間</span><span class="sxs-lookup"><span data-stu-id="23e50-135">period</span></span>    | <span data-ttu-id="23e50-136">減価償却を計算する期間。</span><span class="sxs-lookup"><span data-stu-id="23e50-136">The period to calculate depreciation over.</span></span>                 |

### <a name="return-value"></a><span data-ttu-id="23e50-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-137">Return value</span></span>

<span data-ttu-id="23e50-138">資産の減価償却。</span><span class="sxs-lookup"><span data-stu-id="23e50-138">The depreciation of the asset.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-139">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-139">Remarks</span></span>

<span data-ttu-id="23e50-140">特定期間の簿価額は、購入価格から前期間の減価償却累計額を差し引いた額に等しい。</span><span class="sxs-lookup"><span data-stu-id="23e50-140">The book value for a specific period is equal to the purchase price minus the accumulated depreciation for previous periods:</span></span>

-   <span data-ttu-id="23e50-141">期間 1 の簿価額 = 価格</span><span class="sxs-lookup"><span data-stu-id="23e50-141">Book value for Period 1 = Price</span></span>
-   <span data-ttu-id="23e50-142">期間 2 の簿価額 = 期間 1 の簿価額 – 期間の減価償却 1</span><span class="sxs-lookup"><span data-stu-id="23e50-142">Book value for Period 2 = Book value for Period 1 – Depreciation for Period 1</span></span>
-   <span data-ttu-id="23e50-143">期間 n の簿価額 = 期間 (n–1) の簿価額 – 期間の減価償却 (n–1)</span><span class="sxs-lookup"><span data-stu-id="23e50-143">Book value for Period n = Book value for Period (n–1) – Depreciation for Period (n–1)</span></span>

<span data-ttu-id="23e50-144">減価償却費の計算には 3 つのバリエーションがあります。期間タイプ &gt; 耐用年数:</span><span class="sxs-lookup"><span data-stu-id="23e50-144">There are three variations for the calculation of depreciation: If Period &gt; Life:</span></span>

-   <span data-ttu-id="23e50-145">減価償却 = 0</span><span class="sxs-lookup"><span data-stu-id="23e50-145">Depreciation = 0</span></span>

<span data-ttu-id="23e50-146">If (期間 n の簿価額) – ((期間 n の簿価額) × 2 ÷ ライフ) &lt; 残存価額:</span><span class="sxs-lookup"><span data-stu-id="23e50-146">If (Book value for Period n) – ((Book value for Period n) × 2 ÷ Life) &lt; Residual value:</span></span>

-   <span data-ttu-id="23e50-147">減価償却 = (期間 n の簿価額) – 残存価額</span><span class="sxs-lookup"><span data-stu-id="23e50-147">Depreciation = (Book value for Period n) – Residual value</span></span>

<span data-ttu-id="23e50-148">その他の場合: 減価償却 = (期間 n の簿価額) × 2 ÷ 耐用年数、**syd** および **sln** 関数も、資産の減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-148">In all other cases: Depreciation = (Book value for Period n) × 2 ÷ Life The **syd** and **sln** functions also calculate the depreciation of an asset.</span></span> <span data-ttu-id="23e50-149">**syd** および **ddb** 関数を使用すると、早い年の減価償却を高くできますが、**sln** は直線的な減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-149">The **syd** and **ddb** functions enables higher depreciation for the earlier years, whereas **sln** calculates a linear depreciation.</span></span>

    ddb(12000,2000,10,1); //Returns the value 2400.
    ddb(12000,2000,10,3); //Returns the value 1536.

<a name="dg"></a><span data-ttu-id="23e50-150">dg</span><span class="sxs-lookup"><span data-stu-id="23e50-150">dg</span></span>
--

<span data-ttu-id="23e50-151">販売価格および購買価格に基づいて利益率を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-151">Calculates the contribution ratio, which is based on the sales price and the purchase price.</span></span> <span data-ttu-id="23e50-152">*売上*パラメーターの値が **0.0** である場合、計算を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="23e50-152">If the value of the *sale* parameter is **0.0**, the calculation can't be done.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-153">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-153">Syntax</span></span>

    real dg(real sale, real purchase)

### <a name="parameters"></a><span data-ttu-id="23e50-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-154">Parameters</span></span>

| <span data-ttu-id="23e50-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-155">Parameter</span></span> | <span data-ttu-id="23e50-156">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-156">Description</span></span>         |
|-----------|---------------------|
| <span data-ttu-id="23e50-157">販売</span><span class="sxs-lookup"><span data-stu-id="23e50-157">sale</span></span>      | <span data-ttu-id="23e50-158">販売価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-158">The sale price.</span></span>     |
| <span data-ttu-id="23e50-159">購買</span><span class="sxs-lookup"><span data-stu-id="23e50-159">purchase</span></span>  | <span data-ttu-id="23e50-160">購買価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-160">The purchase price.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-161">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-161">Return value</span></span>

<span data-ttu-id="23e50-162">利益率。</span><span class="sxs-lookup"><span data-stu-id="23e50-162">The contribution ratio.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-163">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-163">Remarks</span></span>

    dg(1000,300); //Returns the value 0.7.
    dg(100,30); //Returns the value 0.7.
    dg(20000, 11000); //Returns the value 0.45.

<a name="fv"></a><span data-ttu-id="23e50-164">fV</span><span class="sxs-lookup"><span data-stu-id="23e50-164">fV</span></span>
--

<span data-ttu-id="23e50-165">投資の未来価値を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-165">Calculates the future value of an investment.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-166">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-166">Syntax</span></span>

    real fV(real amount, real interest, real life)

### <a name="parameters"></a><span data-ttu-id="23e50-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-167">Parameters</span></span>

| <span data-ttu-id="23e50-168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-168">Parameter</span></span> | <span data-ttu-id="23e50-169">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-169">Description</span></span>                                     |
|-----------|-------------------------------------------------|
| <span data-ttu-id="23e50-170">金額</span><span class="sxs-lookup"><span data-stu-id="23e50-170">amount</span></span>    | <span data-ttu-id="23e50-171">各期間中に支払われた金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-171">The amount that was paid in during each period.</span></span> |
| <span data-ttu-id="23e50-172">利息</span><span class="sxs-lookup"><span data-stu-id="23e50-172">interest</span></span>  | <span data-ttu-id="23e50-173">利率。</span><span class="sxs-lookup"><span data-stu-id="23e50-173">The interest rate.</span></span>                              |
| <span data-ttu-id="23e50-174">life</span><span class="sxs-lookup"><span data-stu-id="23e50-174">life</span></span>      | <span data-ttu-id="23e50-175">投資期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-175">The number of investment periods.</span></span>               |

### <a name="return-value"></a><span data-ttu-id="23e50-176">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-176">Return value</span></span>

<span data-ttu-id="23e50-177">投資の将来の値。</span><span class="sxs-lookup"><span data-stu-id="23e50-177">The future value of the investment.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-178">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-178">Remarks</span></span>

    fV(100,0.14,10); //Returns the value 1933.73.
    fV(400,0.10,5); //Returns the value 2442.04.

<a name="idg"></a><span data-ttu-id="23e50-179">idg</span><span class="sxs-lookup"><span data-stu-id="23e50-179">idg</span></span>
---

<span data-ttu-id="23e50-180">利益率および購買価格に基づいて販売価格を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-180">Calculates the sale price, based on the purchase price and the contribution ratio.</span></span>

    real idg(real purchase, real contribution_ratio)

### <a name="parameters"></a><span data-ttu-id="23e50-181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-181">Parameters</span></span>

| <span data-ttu-id="23e50-182">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-182">Parameter</span></span>           | <span data-ttu-id="23e50-183">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-183">Description</span></span>             |
|---------------------|-------------------------|
| <span data-ttu-id="23e50-184">購買</span><span class="sxs-lookup"><span data-stu-id="23e50-184">purchase</span></span>            | <span data-ttu-id="23e50-185">購買価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-185">The purchase price.</span></span>     |
| <span data-ttu-id="23e50-186">contribution\_ratio</span><span class="sxs-lookup"><span data-stu-id="23e50-186">contribution\_ratio</span></span> | <span data-ttu-id="23e50-187">利益率。</span><span class="sxs-lookup"><span data-stu-id="23e50-187">The contribution ratio.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-188">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-188">Return value</span></span>

<span data-ttu-id="23e50-189">販売価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-189">The sale price.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-190">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-190">Remarks</span></span>

<span data-ttu-id="23e50-191">利益率が **1.0** と等しい場合は、計算を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="23e50-191">If the contribution ratio is equal to **1.0**, the calculation can't be done.</span></span> <span data-ttu-id="23e50-192">**idg** 関数は、**dg** 関数の逆です。</span><span class="sxs-lookup"><span data-stu-id="23e50-192">The **idg** function is the inverse of the **dg** function.</span></span>

    idg(300,0.7); //Returns the value 1000.
    idg(11000,0.45); //Returns the value 20000.

## <a name="intvmax"></a><span data-ttu-id="23e50-193">intvMax</span><span class="sxs-lookup"><span data-stu-id="23e50-193">intvMax</span></span>
<span data-ttu-id="23e50-194">期間が *func* パラメーターによって指定された部分に分割されているとき、指定された期間の間隔の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="23e50-194">Retrieves the number of intervals for the specified period when the period is divided into parts as specified by the *func* parameter.</span></span>

    int intvMax(date input_date, date ref_date, int func)

### <a name="parameters"></a><span data-ttu-id="23e50-195">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-195">Parameters</span></span>

| <span data-ttu-id="23e50-196">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-196">Parameter</span></span>   | <span data-ttu-id="23e50-197">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-197">Description</span></span>                                                                |
|-------------|----------------------------------------------------------------------------|
| <span data-ttu-id="23e50-198">input\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-198">input\_date</span></span> | <span data-ttu-id="23e50-199">期間の終了日は、*ref\_date* パラメーターよりも後でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="23e50-199">The end of the period, which must be later than the *ref\_date* parameter.</span></span> |
| <span data-ttu-id="23e50-200">ref\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-200">ref\_date</span></span>   | <span data-ttu-id="23e50-201">期間の開始日。</span><span class="sxs-lookup"><span data-stu-id="23e50-201">The start of the period.</span></span>                                                   |
| <span data-ttu-id="23e50-202">func</span><span class="sxs-lookup"><span data-stu-id="23e50-202">func</span></span>        | <span data-ttu-id="23e50-203">**IntvScale** は、部門単位を示すシステム列挙値です。</span><span class="sxs-lookup"><span data-stu-id="23e50-203">A **IntvScale** system enumeration value that indicates the division unit.</span></span> |

### <a name="remarks"></a><span data-ttu-id="23e50-204">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-204">Remarks</span></span>

<span data-ttu-id="23e50-205">*func* パラメータの使用可能な値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="23e50-205">Here are the possible values for the *func* parameter:</span></span>

-   <span data-ttu-id="23e50-206">None</span><span class="sxs-lookup"><span data-stu-id="23e50-206">None</span></span>
-   <span data-ttu-id="23e50-207">YearMonthDay</span><span class="sxs-lookup"><span data-stu-id="23e50-207">YearMonthDay</span></span>
-   <span data-ttu-id="23e50-208">YearMonth</span><span class="sxs-lookup"><span data-stu-id="23e50-208">YearMonth</span></span>
-   <span data-ttu-id="23e50-209">年</span><span class="sxs-lookup"><span data-stu-id="23e50-209">Year</span></span>
-   <span data-ttu-id="23e50-210">MonthDay</span><span class="sxs-lookup"><span data-stu-id="23e50-210">MonthDay</span></span>
-   <span data-ttu-id="23e50-211">月</span><span class="sxs-lookup"><span data-stu-id="23e50-211">Month</span></span>
-   <span data-ttu-id="23e50-212">曜日</span><span class="sxs-lookup"><span data-stu-id="23e50-212">Day</span></span>
-   <span data-ttu-id="23e50-213">YearQuarter</span><span class="sxs-lookup"><span data-stu-id="23e50-213">YearQuarter</span></span>
-   <span data-ttu-id="23e50-214">四半期</span><span class="sxs-lookup"><span data-stu-id="23e50-214">Quarter</span></span>
-   <span data-ttu-id="23e50-215">YearWeek</span><span class="sxs-lookup"><span data-stu-id="23e50-215">YearWeek</span></span>
-   <span data-ttu-id="23e50-216">週</span><span class="sxs-lookup"><span data-stu-id="23e50-216">Week</span></span>
-   <span data-ttu-id="23e50-217">WeekDay</span><span class="sxs-lookup"><span data-stu-id="23e50-217">WeekDay</span></span>

### <a name="example"></a><span data-ttu-id="23e50-218">例</span><span class="sxs-lookup"><span data-stu-id="23e50-218">Example</span></span>

    static void intvMaxExample()
    {
        date refDate = str2Date("4/9/2007", 213);
        date inputDate = str2Date("10/5/2007", 213);
        int numberOfIntervals;
        ;
        numberOfIntervals = intvMax(inputDate, refDate, intvScale::YearMonth);
        print numberOfIntervals;
        pause;
    }

## <a name="intvname"></a><span data-ttu-id="23e50-219">intvName</span><span class="sxs-lookup"><span data-stu-id="23e50-219">intvName</span></span>
<span data-ttu-id="23e50-220">指定した日付から指定した間隔数先の間隔の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="23e50-220">Returns the name of the interval that is the specified number of intervals ahead of the specified date.</span></span>

    str intvName(date input_date, int col, enum func)

### <a name="parameters"></a><span data-ttu-id="23e50-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-221">Parameters</span></span>

| <span data-ttu-id="23e50-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-222">Parameter</span></span>   | <span data-ttu-id="23e50-223">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-223">Description</span></span>                                                                                 |
|-------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e50-224">input\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-224">input\_date</span></span> | <span data-ttu-id="23e50-225">最初の間隔の日付です。</span><span class="sxs-lookup"><span data-stu-id="23e50-225">A date in the first interval.</span></span>                                                               |
| <span data-ttu-id="23e50-226">col</span><span class="sxs-lookup"><span data-stu-id="23e50-226">col</span></span>         | <span data-ttu-id="23e50-227">*input\_date* パラメーターで指定された日付より前の間隔の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-227">The number of intervals ahead of the date that is specified by the *input\_date* parameter.</span></span> |
| <span data-ttu-id="23e50-228">func</span><span class="sxs-lookup"><span data-stu-id="23e50-228">func</span></span>        | <span data-ttu-id="23e50-229">**intvScale** 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="23e50-229">An **intvScale** enumeration value.</span></span>                                                         |

### <a name="return-value"></a><span data-ttu-id="23e50-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-230">Return value</span></span>

<span data-ttu-id="23e50-231">間隔の名前。</span><span class="sxs-lookup"><span data-stu-id="23e50-231">The name of the interval.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-232">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-232">Remarks</span></span>

<span data-ttu-id="23e50-233">たとえば、*func* パラメーターが、**IntvScale::WeekDay** 列挙値である場合、このメソッドは平日の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="23e50-233">For example, if the *func* parameter is the **IntvScale::WeekDay** enumeration value, this method returns the name of the weekday.</span></span> <span data-ttu-id="23e50-234">*func* パラメーターが、**IntvScale::Week** 列挙値である場合、このメソッドは週の数が含まれている文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="23e50-234">If the *func* parameter is the **IntvScale::Week** enumeration value, this method returns a string that contains the number of the week.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-235">例</span><span class="sxs-lookup"><span data-stu-id="23e50-235">Example</span></span>

    static void intvNameExample(Args _args)
    {
        date refDate = 2672010;
        str name;
        ;
        name = intvName(refDate, 3,  intvScale::WeekDay);
        Global::info(strfmt("%1 is the output, which indicates the day of the week 3 days after 26\7\2010.", name));
    }
    /**** Infolog display.
    Message (09:56:55 am)
    Thu is the output, which indicates the day of the week 3 days after 2672010.
    ****/

## <a name="intvno"></a><span data-ttu-id="23e50-236">intvNo</span><span class="sxs-lookup"><span data-stu-id="23e50-236">intvNo</span></span>
<span data-ttu-id="23e50-237">指定した間隔に時間を分割するとき、2 つの日付間の間隔の数を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-237">Calculates the number of intervals between two dates when you divide the time into the specified intervals.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-238">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-238">Syntax</span></span>

    int intvNo(date input_date, date ref_date, int func)

### <a name="parameters"></a><span data-ttu-id="23e50-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-239">Parameters</span></span>

| <span data-ttu-id="23e50-240">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-240">Parameter</span></span>   | <span data-ttu-id="23e50-241">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-241">Description</span></span>                                    |
|-------------|------------------------------------------------|
| <span data-ttu-id="23e50-242">input\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-242">input\_date</span></span> | <span data-ttu-id="23e50-243">期間の終了を示す日付</span><span class="sxs-lookup"><span data-stu-id="23e50-243">A date that indicates the end of the period</span></span>    |
| <span data-ttu-id="23e50-244">ref\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-244">ref\_date</span></span>   | <span data-ttu-id="23e50-245">期間の開始を示す日付です。</span><span class="sxs-lookup"><span data-stu-id="23e50-245">A date that indicates the start of the period.</span></span> |
| <span data-ttu-id="23e50-246">func</span><span class="sxs-lookup"><span data-stu-id="23e50-246">func</span></span>        | <span data-ttu-id="23e50-247">**intvScale** 列挙値です。</span><span class="sxs-lookup"><span data-stu-id="23e50-247">An **intvScale** enumeration value.</span></span>            |

### <a name="return-value"></a><span data-ttu-id="23e50-248">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-248">Return value</span></span>

<span data-ttu-id="23e50-249">*ref\_date* および *input\_date* パラメーターで指定された日付間の間隔の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-249">The number of intervals between the dates that are specified by the *ref\_date* and *input\_date* parameters.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-250">例</span><span class="sxs-lookup"><span data-stu-id="23e50-250">Example</span></span>

    static void intvNoExample(Args _args)
    {
        date inputDate = str2Date("1/1/2007", 213);
        date refDate = str2Date("3/1/2007", 213);
        int noOfIntervals;
        ;
        noOfIntervals = intvNo(refDate, inputDate, intvScale::Month);
        print noOfIntervals;
        pause;
        //noOfIntervals now holds the difference in months between March and January (2).
    }

## <a name="intvnorm"></a><span data-ttu-id="23e50-251">intvNorm</span><span class="sxs-lookup"><span data-stu-id="23e50-251">intvNorm</span></span>
<span data-ttu-id="23e50-252">期間の正規化日を返します。</span><span class="sxs-lookup"><span data-stu-id="23e50-252">Returns the normalized date for the period.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-253">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-253">Syntax</span></span>

    date intvNorm(date input_date, date ref_date, int func)

### <a name="parameters"></a><span data-ttu-id="23e50-254">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-254">Parameters</span></span>

| <span data-ttu-id="23e50-255">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-255">Parameter</span></span>   | <span data-ttu-id="23e50-256">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-256">Description</span></span>                                                                                              |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e50-257">input\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-257">input\_date</span></span> | <span data-ttu-id="23e50-258">期間の終了日は、*ref\_date* パラメーターが指定した日付よりも後でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="23e50-258">The end of the period, which must be later than the date that is specified by the *ref\_date* parameter.</span></span> |
| <span data-ttu-id="23e50-259">ref\_date</span><span class="sxs-lookup"><span data-stu-id="23e50-259">ref\_date</span></span>   | <span data-ttu-id="23e50-260">期間の開始日。</span><span class="sxs-lookup"><span data-stu-id="23e50-260">The start of the period.</span></span>                                                                                 |
| <span data-ttu-id="23e50-261">func</span><span class="sxs-lookup"><span data-stu-id="23e50-261">func</span></span>        | <span data-ttu-id="23e50-262">**intvScale** は、間隔区分単位を示す列挙値です。</span><span class="sxs-lookup"><span data-stu-id="23e50-262">An **intvScale** enumeration value that indicates the interval division unit.</span></span>                            |

### <a name="return-value"></a><span data-ttu-id="23e50-263">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-263">Return value</span></span>

<span data-ttu-id="23e50-264">期間の正規化日</span><span class="sxs-lookup"><span data-stu-id="23e50-264">The normalized date for the period.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-265">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-265">Remarks</span></span>

<span data-ttu-id="23e50-266">返される日付は、*ref\_date* パラメーターで指定された日付が存在する区間の、最初の日の日付になります。</span><span class="sxs-lookup"><span data-stu-id="23e50-266">The returned date will equal the date of the first day in the interval in which the date that is specified by the *ref\_date* parameter exists.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-267">例</span><span class="sxs-lookup"><span data-stu-id="23e50-267">Example</span></span>

    static void example()
    {
        print intvNorm(today(), today()-1, IntVScale::WeekDay);
        pause;
    }

<a name="pmt"></a><span data-ttu-id="23e50-268">pmt</span><span class="sxs-lookup"><span data-stu-id="23e50-268">pmt</span></span>
---

<span data-ttu-id="23e50-269">ローンを返済するために毎回支払われなければならない金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-269">Calculates the amount that must be paid every period to repay a loan.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-270">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-270">Syntax</span></span>

    real pmt(real principal, real interest, real life)

### <a name="parameters"></a><span data-ttu-id="23e50-271">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-271">Parameters</span></span>

| <span data-ttu-id="23e50-272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-272">Parameter</span></span> | <span data-ttu-id="23e50-273">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-273">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="23e50-274">principal</span><span class="sxs-lookup"><span data-stu-id="23e50-274">principal</span></span> | <span data-ttu-id="23e50-275">最初に借り入れた金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-275">The amount that was originally borrowed.</span></span>                                  |
| <span data-ttu-id="23e50-276">利息</span><span class="sxs-lookup"><span data-stu-id="23e50-276">interest</span></span>  | <span data-ttu-id="23e50-277">各期間に借用した金額に適用される利息。</span><span class="sxs-lookup"><span data-stu-id="23e50-277">The interest that is applied each period to the amount that was borrowed.</span></span> |
| <span data-ttu-id="23e50-278">life</span><span class="sxs-lookup"><span data-stu-id="23e50-278">life</span></span>      | <span data-ttu-id="23e50-279">ローンが返済される期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-279">The number of periods that the loan is repaid over.</span></span>                       |

### <a name="return-value"></a><span data-ttu-id="23e50-280">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-280">Return value</span></span>

<span data-ttu-id="23e50-281">期間ごとに支払われる必要のある金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-281">The amount that must be paid every period.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-282">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-282">Remarks</span></span>

<span data-ttu-id="23e50-283">*life* および *interest* パラメーターは、同じ時間単位で表される必要があります。</span><span class="sxs-lookup"><span data-stu-id="23e50-283">The *life* and *interest* parameters must be expressed in the same time units.</span></span> <span data-ttu-id="23e50-284">*life* パラメーターの値は、**0.0** を超える必要があります。</span><span class="sxs-lookup"><span data-stu-id="23e50-284">The value of the *life* parameter must be more than **0.0**.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-285">例</span><span class="sxs-lookup"><span data-stu-id="23e50-285">Example</span></span>

    pmt(4000,0.14,4); //Returns the value 1372.82.
    pmt(10000,0.10,20); //Returns the value 1174.60.

<a name="pt"></a><span data-ttu-id="23e50-286">pt</span><span class="sxs-lookup"><span data-stu-id="23e50-286">pt</span></span>
--

<span data-ttu-id="23e50-287">その番号の指定された割合と数値の合計を取得します。</span><span class="sxs-lookup"><span data-stu-id="23e50-287">Retrieves the sum of a number plus a specified percentage of that number.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-288">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-288">Syntax</span></span>

    real pt(real amount, real percentage)

### <a name="parameters"></a><span data-ttu-id="23e50-289">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-289">Parameters</span></span>

| <span data-ttu-id="23e50-290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-290">Parameter</span></span>  | <span data-ttu-id="23e50-291">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-291">Description</span></span>                |
|------------|----------------------------|
| <span data-ttu-id="23e50-292">金額</span><span class="sxs-lookup"><span data-stu-id="23e50-292">amount</span></span>     | <span data-ttu-id="23e50-293">元の番号。</span><span class="sxs-lookup"><span data-stu-id="23e50-293">The original number.</span></span>       |
| <span data-ttu-id="23e50-294">パーセント</span><span class="sxs-lookup"><span data-stu-id="23e50-294">percentage</span></span> | <span data-ttu-id="23e50-295">パーセント補足。</span><span class="sxs-lookup"><span data-stu-id="23e50-295">The percentage supplement.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-296">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-296">Return value</span></span>

<span data-ttu-id="23e50-297">((<em>amount *× *percentage</em>) + <em>amount</em>) に等しい数。</span><span class="sxs-lookup"><span data-stu-id="23e50-297">The number that is equal to ((<em>amount *× *percentage</em>) + <em>amount</em>).</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-298">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-298">Remarks</span></span>

    pt(2000.0,0.10); //Returns the value 2200.0.
    pt(20.0,0.10); //Returns the value 22.0.

<a name="pv"></a><span data-ttu-id="23e50-299">pv</span><span class="sxs-lookup"><span data-stu-id="23e50-299">pv</span></span>
--

<span data-ttu-id="23e50-300">年金の現在価値を計算します。金額は複数の期間にわたり支払われ、利息は期間ごとに控除されます。</span><span class="sxs-lookup"><span data-stu-id="23e50-300">Calculates the present value of an annuity, where an amount is received over multiple periods and the interest rate is deducted for each period.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-301">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-301">Syntax</span></span>

    real pv(real amount, real interest, real life)

### <a name="parameters"></a><span data-ttu-id="23e50-302">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-302">Parameters</span></span>

| <span data-ttu-id="23e50-303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-303">Parameter</span></span> | <span data-ttu-id="23e50-304">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-304">Description</span></span>                                                                             |
|-----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e50-305">金額</span><span class="sxs-lookup"><span data-stu-id="23e50-305">amount</span></span>    | <span data-ttu-id="23e50-306">各期間中に支払われる金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-306">The amount that is paid during each period.</span></span>                                             |
| <span data-ttu-id="23e50-307">利息</span><span class="sxs-lookup"><span data-stu-id="23e50-307">interest</span></span>  | <span data-ttu-id="23e50-308">利率。</span><span class="sxs-lookup"><span data-stu-id="23e50-308">The interest rate.</span></span>                                                                      |
| <span data-ttu-id="23e50-309">life</span><span class="sxs-lookup"><span data-stu-id="23e50-309">life</span></span>      | <span data-ttu-id="23e50-310">*amount* パラメーターで指定された値が支払われた回数。</span><span class="sxs-lookup"><span data-stu-id="23e50-310">The number of times that the value that is specified by the *amount* parameter is paid.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-311">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-311">Return value</span></span>

<span data-ttu-id="23e50-312">年金の現在の値。</span><span class="sxs-lookup"><span data-stu-id="23e50-312">The current value of an annuity.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-313">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-313">Remarks</span></span>

    pv(300,0.14,4); //Returns the value 874.11.

## <a name="rate"></a><span data-ttu-id="23e50-314">レート</span><span class="sxs-lookup"><span data-stu-id="23e50-314">rate</span></span>
<span data-ttu-id="23e50-315">現在の投資価値が指定された期間の数にわたって未来価値を達成するために必要な利子を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-315">Calculates the interest that is required for the current investment value to attain the future value over the specified number of periods.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-316">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-316">Syntax</span></span>

    real rate(real _future_value, real _current_value, real _terms)

### <a name="parameters"></a><span data-ttu-id="23e50-317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-317">Parameters</span></span>

| <span data-ttu-id="23e50-318">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-318">Parameter</span></span>        | <span data-ttu-id="23e50-319">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-319">Description</span></span>                                      |
|------------------|--------------------------------------------------|
| <span data-ttu-id="23e50-320">\_将来\_値</span><span class="sxs-lookup"><span data-stu-id="23e50-320">\_future\_value</span></span>  | <span data-ttu-id="23e50-321">投資の将来の値。</span><span class="sxs-lookup"><span data-stu-id="23e50-321">The future value of the investment.</span></span>              |
| <span data-ttu-id="23e50-322">\_現在\_値</span><span class="sxs-lookup"><span data-stu-id="23e50-322">\_current\_value</span></span> | <span data-ttu-id="23e50-323">投資の現在の値。</span><span class="sxs-lookup"><span data-stu-id="23e50-323">The current value of the investment.</span></span>             |
| <span data-ttu-id="23e50-324">\_使用条件</span><span class="sxs-lookup"><span data-stu-id="23e50-324">\_terms</span></span>          | <span data-ttu-id="23e50-325">投資がわたる期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-325">The number of periods that the investment spans.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-326">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-326">Return value</span></span>

<span data-ttu-id="23e50-327">計算済利率。</span><span class="sxs-lookup"><span data-stu-id="23e50-327">The calculated interest rate.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-328">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-328">Remarks</span></span>

    rate(10000,1000,20); //Returns the value 0.12.

<a name="sln"></a><span data-ttu-id="23e50-329">sln</span><span class="sxs-lookup"><span data-stu-id="23e50-329">sln</span></span>
---

<span data-ttu-id="23e50-330">減価償却期間ごとに指定された資産の固定の減価償却金額を取得します。</span><span class="sxs-lookup"><span data-stu-id="23e50-330">Retrieves the constant depreciation amount for the specified asset for each depreciation period.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-331">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-331">Syntax</span></span>

    real sln(real price, real scrap, real life)

### <a name="parameters"></a><span data-ttu-id="23e50-332">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-332">Parameters</span></span>

| <span data-ttu-id="23e50-333">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-333">Parameter</span></span> | <span data-ttu-id="23e50-334">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-334">Description</span></span>                                              |
|-----------|----------------------------------------------------------|
| <span data-ttu-id="23e50-335">価格</span><span class="sxs-lookup"><span data-stu-id="23e50-335">price</span></span>     | <span data-ttu-id="23e50-336">アセットの購買価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-336">The purchase price of the asset.</span></span>                         |
| <span data-ttu-id="23e50-337">仕損</span><span class="sxs-lookup"><span data-stu-id="23e50-337">scrap</span></span>     | <span data-ttu-id="23e50-338">資産の仕損価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-338">The scrap value of the asset.</span></span>                            |
| <span data-ttu-id="23e50-339">life</span><span class="sxs-lookup"><span data-stu-id="23e50-339">life</span></span>      | <span data-ttu-id="23e50-340">資産の予想期限における期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-340">The number of periods in the expected life of the asset.</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-341">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-341">Return value</span></span>

<span data-ttu-id="23e50-342">減価償却金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-342">The depreciation amount.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-343">例</span><span class="sxs-lookup"><span data-stu-id="23e50-343">Example</span></span>

    static void slnExample(Args _arg)
    {
        real r;
        ;
        r = sln(100.00, 50.00, 50.00);
        print r;
        pause;
    }

<a name="syd"></a><span data-ttu-id="23e50-344">syd</span><span class="sxs-lookup"><span data-stu-id="23e50-344">syd</span></span>
---

<span data-ttu-id="23e50-345">指定した期間にわたる資産の減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-345">Calculates the depreciation of an asset over a specified period.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-346">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-346">Syntax</span></span>

    real syd(real _price, real _scrap, real _life, int _period)

### <a name="parameters"></a><span data-ttu-id="23e50-347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-347">Parameters</span></span>

| <span data-ttu-id="23e50-348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-348">Parameter</span></span> | <span data-ttu-id="23e50-349">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-349">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="23e50-350">\_価格</span><span class="sxs-lookup"><span data-stu-id="23e50-350">\_price</span></span>   | <span data-ttu-id="23e50-351">アセットの購買価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-351">The purchase price of the asset.</span></span>                        |
| <span data-ttu-id="23e50-352">\_仕損</span><span class="sxs-lookup"><span data-stu-id="23e50-352">\_scrap</span></span>   | <span data-ttu-id="23e50-353">資産の仕損価格。</span><span class="sxs-lookup"><span data-stu-id="23e50-353">The scrap value of the asset.</span></span>                           |
| <span data-ttu-id="23e50-354">\_期限</span><span class="sxs-lookup"><span data-stu-id="23e50-354">\_life</span></span>    | <span data-ttu-id="23e50-355">資産の予想期限 (期間数)。</span><span class="sxs-lookup"><span data-stu-id="23e50-355">The expected life of the asset (the number of periods).</span></span> |
| <span data-ttu-id="23e50-356">\_期間</span><span class="sxs-lookup"><span data-stu-id="23e50-356">\_period</span></span>  | <span data-ttu-id="23e50-357">減価償却を計算する期間。</span><span class="sxs-lookup"><span data-stu-id="23e50-357">The period to calculate depreciation for.</span></span>               |

### <a name="return-value"></a><span data-ttu-id="23e50-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-358">Return value</span></span>

<span data-ttu-id="23e50-359">指定した期間での減価償却の金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-359">The amount of depreciation over the specified period.</span></span>

### <a name="remarks"></a><span data-ttu-id="23e50-360">備考</span><span class="sxs-lookup"><span data-stu-id="23e50-360">Remarks</span></span>

<span data-ttu-id="23e50-361">**sln** 関数とは対照的に、**syd** 関数は資産の増加償却を可能にします。</span><span class="sxs-lookup"><span data-stu-id="23e50-361">In contrast to the **sln** function, the **syd** function can allow for an accelerated depreciation of the asset.</span></span> <span data-ttu-id="23e50-362">**ddb** 関数と同様に、資産の耐用年数の初期段階におけるよりも高い減価償却が可能になります。</span><span class="sxs-lookup"><span data-stu-id="23e50-362">As with the **ddb** function, this enables higher depreciation during the early periods of the life of an asset.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-363">例</span><span class="sxs-lookup"><span data-stu-id="23e50-363">Example</span></span>

<span data-ttu-id="23e50-364">次の例では、定期的な減価償却が 10,000 の購買価格、2,000 の仕損価格、および 5 の耐用年数の資産に対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="23e50-364">In the following examples, the periodic depreciation is calculated for an asset that has a purchase price of 10,000, a scrap value of 2,000, and a life of 5.</span></span> <span data-ttu-id="23e50-365">比較では、**sln(10000,2000,5)** は各期間ごとに 1600.00 を算出します。</span><span class="sxs-lookup"><span data-stu-id="23e50-365">In comparison, **sln(10000,2000,5)** would calculate 1600.00 for each period.</span></span>

    // Returns the value 2666.67 (for the 1st period).
    syd(10000,2000,5,1);
    // Returns the value 2133.33 (for the 2nd period).
    syd(10000,2000,5,2);
    // Returns the value 1600.00 (for the 3rd period).
    syd(10000,2000,5,3);
    // Returns the value 1066.67 (for the 4th period).
    syd(10000,2000,5,4);
    // Returns the value 533.33 (for 5th - and final- period).
    syd(10000,2000,5,5);

## <a name="term"></a><span data-ttu-id="23e50-366">term</span><span class="sxs-lookup"><span data-stu-id="23e50-366">term</span></span>
<span data-ttu-id="23e50-367">投資が実行されなければならない期間の数を計算します。</span><span class="sxs-lookup"><span data-stu-id="23e50-367">Calculates the number of periods that an investment must run for.</span></span>

### <a name="syntax"></a><span data-ttu-id="23e50-368">構文</span><span class="sxs-lookup"><span data-stu-id="23e50-368">Syntax</span></span>

    real term(real amount, real interest, real future_value)

### <a name="parameters"></a><span data-ttu-id="23e50-369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-369">Parameters</span></span>

| <span data-ttu-id="23e50-370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23e50-370">Parameter</span></span>     | <span data-ttu-id="23e50-371">説明</span><span class="sxs-lookup"><span data-stu-id="23e50-371">Description</span></span>                                             |
|---------------|---------------------------------------------------------|
| <span data-ttu-id="23e50-372">金額</span><span class="sxs-lookup"><span data-stu-id="23e50-372">amount</span></span>        | <span data-ttu-id="23e50-373">定期的な投資の金額。</span><span class="sxs-lookup"><span data-stu-id="23e50-373">The amount of the periodic investment.</span></span>                  |
| <span data-ttu-id="23e50-374">利息</span><span class="sxs-lookup"><span data-stu-id="23e50-374">interest</span></span>      | <span data-ttu-id="23e50-375">各期間の利率。</span><span class="sxs-lookup"><span data-stu-id="23e50-375">The interest rate for each period.</span></span>                      |
| <span data-ttu-id="23e50-376">future\_value</span><span class="sxs-lookup"><span data-stu-id="23e50-376">future\_value</span></span> | <span data-ttu-id="23e50-377">投資に予想される将来の価値</span><span class="sxs-lookup"><span data-stu-id="23e50-377">The future value that is anticipated for the investment</span></span> |

### <a name="return-value"></a><span data-ttu-id="23e50-378">戻り値</span><span class="sxs-lookup"><span data-stu-id="23e50-378">Return value</span></span>

<span data-ttu-id="23e50-379">投資が実行されなければならない期間の数。</span><span class="sxs-lookup"><span data-stu-id="23e50-379">The number of periods that the investment must run for.</span></span>

### <a name="example"></a><span data-ttu-id="23e50-380">例</span><span class="sxs-lookup"><span data-stu-id="23e50-380">Example</span></span>

    static void termExample(Args _args)
    {
        print term(400,0.08,5000);  //returns the value '9.01'.
        print term(100,0.14,3000);  //returns the value '12.58'.
        pause;
    }




