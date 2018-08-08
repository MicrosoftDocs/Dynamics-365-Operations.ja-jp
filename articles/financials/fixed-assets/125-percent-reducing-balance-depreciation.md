---
title: "125% 逓減残高による減価償却"
description: "この記事は、減価償却の 125% 逓減残高法の概要を示します。"
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f7af5413376a98c3b2b7ded46c757c9156a3fadf
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="d6826-103">125% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="d6826-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6826-104">この記事は、減価償却の 125% 逓減残高法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="d6826-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="d6826-105">固定資産減価償却プロファイルを設定し、[減価償却プロファイル] ページの [方法] フィールドで [125% 逓減残高] を選択すると、この減価償却プロファイルが割り当てられる固定資産の減価償却に、各減価償却期間で同じ比率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="d6826-106">この比率は資産の耐用年数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="d6826-107">たとえば、資産の耐用年数が 5 年の場合は、比率が 25% (125% ÷ 5) として計算されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="d6826-108">125% 逓減残高による減価償却を設定するには、[減価償却プロファイル] ページの [償却年] フィールドと [期間の頻度] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d6826-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d6826-109">[期間の頻度] フィールドで使用できるオプションは、[償却年] フィールドで選択した値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d6826-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d6826-110">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="d6826-110">Select a depreciation year</span></span>
<span data-ttu-id="d6826-111">[減価償却プロファイル] ページの [償却年] フィールドで [暦年] または [会計年度] のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d6826-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d6826-112">既定値は [暦年] です。</span><span class="sxs-lookup"><span data-stu-id="d6826-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="d6826-113">この選択により、[期間の頻度] フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="d6826-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="d6826-114">このフィールドによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="d6826-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="d6826-115">Calendar</span></span>

<span data-ttu-id="d6826-116">[償却年] フィールドの既定値である [暦年] をそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6826-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="d6826-117">[暦年] 選択すると、毎年 1 月 1 日に償却基礎額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="d6826-118">通常、償却基礎額は、正味簿価額から仕損価格を差し引いた額です。</span><span class="sxs-lookup"><span data-stu-id="d6826-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="d6826-119">このトピックの後の例では、計算列の最初の式の分子が減価償却基準です。</span><span class="sxs-lookup"><span data-stu-id="d6826-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d6826-120">償却年として [暦年] を選択すると、[期間の頻度] フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6826-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d6826-121">[年 1 回] を選択すると、12 月 31 日に金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="d6826-122">[月 1 回] を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d6826-123">[四半期に 1 回] を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d6826-124">[半期に 1 回] を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d6826-125">[毎日] を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d6826-126">会計年度</span><span class="sxs-lookup"><span data-stu-id="d6826-126">Fiscal</span></span>

<span data-ttu-id="d6826-127">[償却年] フィールドで [会計年度] を選択すると、125% 逓減残高による減価償却は、帳簿で指定した会計カレンダーまたは [元帳] ページで選択した会計カレンダーの会計年度に基づいて計算します。</span><span class="sxs-lookup"><span data-stu-id="d6826-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="d6826-128">会計カレンダーは、[会計カレンダー] ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="d6826-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d6826-129">たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d6826-130">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d6826-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d6826-131">減価償却は各期間に合わせて自動的に調整され、次の会計年度の長さは、[会計カレンダー] ページで設定された期間で決定されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d6826-132">償却年として [会計年度] を選択すると、[期間の頻度] フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="d6826-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d6826-133">[年 1 回] を選択すると、会計年度に対して計算された減価償却の合計量が、会計年度の最終日に 1 つの量として転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d6826-134">**会計年度期間**では、会計年度に対して計算された減価償却の合計額が会計年度の最終日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="d6826-135">この金額は [会計カレンダー] ページで定義された会計年度期間に見越計上されます。</span><span class="sxs-lookup"><span data-stu-id="d6826-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="d6826-136">125% 逓減残高による減価償却の例</span><span class="sxs-lookup"><span data-stu-id="d6826-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="d6826-137">取得価額</span><span class="sxs-lookup"><span data-stu-id="d6826-137">Acquisition cost</span></span>               | <span data-ttu-id="d6826-138">11,000</span><span class="sxs-lookup"><span data-stu-id="d6826-138">11,000</span></span> |
| <span data-ttu-id="d6826-139">救済価格</span><span class="sxs-lookup"><span data-stu-id="d6826-139">Salvage value</span></span>                  | <span data-ttu-id="d6826-140">1.000</span><span class="sxs-lookup"><span data-stu-id="d6826-140">1,000</span></span>  |
| <span data-ttu-id="d6826-141">償却基礎額</span><span class="sxs-lookup"><span data-stu-id="d6826-141">Depreciation base</span></span>              | <span data-ttu-id="d6826-142">10,000</span><span class="sxs-lookup"><span data-stu-id="d6826-142">10,000</span></span> |
| <span data-ttu-id="d6826-143">耐用年数</span><span class="sxs-lookup"><span data-stu-id="d6826-143">Service life years</span></span>             | <span data-ttu-id="d6826-144">5</span><span class="sxs-lookup"><span data-stu-id="d6826-144">5</span></span>      |
| <span data-ttu-id="d6826-145">年次減価償却率</span><span class="sxs-lookup"><span data-stu-id="d6826-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="d6826-146">25%</span><span class="sxs-lookup"><span data-stu-id="d6826-146">25%</span></span>    |

<span data-ttu-id="d6826-147">125% 低減残高法では、125% を耐用年数で除算します。</span><span class="sxs-lookup"><span data-stu-id="d6826-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="d6826-148">この比率は、資産の正味簿価額で乗算され、各年の減価償却金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="d6826-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="d6826-149">期間</span><span class="sxs-lookup"><span data-stu-id="d6826-149">Period</span></span> | <span data-ttu-id="d6826-150">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="d6826-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d6826-151">簿価額</span><span class="sxs-lookup"><span data-stu-id="d6826-151">Book value</span></span>                    | <span data-ttu-id="d6826-152">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="d6826-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="d6826-153">年 1</span><span class="sxs-lookup"><span data-stu-id="d6826-153">Year 1</span></span> | <span data-ttu-id="d6826-154">(11,000 – 1,000) × 25% = 2,500</span><span class="sxs-lookup"><span data-stu-id="d6826-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="d6826-155">11,000 - 2,500 = 8,500</span><span class="sxs-lookup"><span data-stu-id="d6826-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="d6826-156">(11,000 – 1,000 – 2,500) = 7,500</span><span class="sxs-lookup"><span data-stu-id="d6826-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="d6826-157">年 2</span><span class="sxs-lookup"><span data-stu-id="d6826-157">Year 2</span></span> | <span data-ttu-id="d6826-158">7,500 × 25% = 1,875</span><span class="sxs-lookup"><span data-stu-id="d6826-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="d6826-159">(8,500 – 1,875) = 6,625</span><span class="sxs-lookup"><span data-stu-id="d6826-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="d6826-160">(7,500 – 1,875) = 5,625</span><span class="sxs-lookup"><span data-stu-id="d6826-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="d6826-161">年 3</span><span class="sxs-lookup"><span data-stu-id="d6826-161">Year 3</span></span> | <span data-ttu-id="d6826-162">5,625 × 25% = 1,406.25</span><span class="sxs-lookup"><span data-stu-id="d6826-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="d6826-163">(6,625 – 1,406.25) = 5,218.75</span><span class="sxs-lookup"><span data-stu-id="d6826-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="d6826-164">(5,625 – 1,406.25) = 4,218.75</span><span class="sxs-lookup"><span data-stu-id="d6826-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="d6826-165">通常、125% 逓減残高による減価償却方法を使用して計算される金額が、定額法を使用して計算された金額より低くなる場合、残余耐用期間では定額法への換算が行われます。</span><span class="sxs-lookup"><span data-stu-id="d6826-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




