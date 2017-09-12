---
title: "耐用年数定額減価償却"
description: "この記事は、耐用年数定額減価償却方法の概要を示します。"
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="9d32e-103">耐用年数定額減価償却</span><span class="sxs-lookup"><span data-stu-id="9d32e-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9d32e-104">この記事は、耐用年数定額減価償却方法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="9d32e-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="9d32e-105">固定資産減価償却プロファイルを設定して [減価償却プロファイル] ページの [方式] フィールドで [定額法耐用年数] を選択すると、この減価償却プロファイルが割り当てられた固定資産は、その資産の耐用年数の合計に基づいて償却されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="9d32e-106">この場合は一般に、各減価償却期間の減価償却金額が同じになります。</span><span class="sxs-lookup"><span data-stu-id="9d32e-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="9d32e-107">耐用年数残減価償却と耐用年数定額減価償却における計算された減価償却量が異なるのは、資産に転記される調整がある場合です。</span><span class="sxs-lookup"><span data-stu-id="9d32e-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="9d32e-108">定額法耐用年数を設定するには、[減価償却プロファイル] ページの [償却年] フィールドと [期間の頻度] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9d32e-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="9d32e-109">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="9d32e-109">Select a depreciation year</span></span>
<span data-ttu-id="9d32e-110">[減価償却プロファイル] ページの [償却年] フィールドで [暦年] または [会計年度] のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="9d32e-111">この選択により、[期間の頻度] フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="9d32e-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="9d32e-112">既定のオプションは [暦年] です。</span><span class="sxs-lookup"><span data-stu-id="9d32e-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="9d32e-113">カレンダー</span><span class="sxs-lookup"><span data-stu-id="9d32e-113">Calendar</span></span>

<span data-ttu-id="9d32e-114">[カレンダー] を選択する場合、別の会計カレンダーを定義済みでも、1 月 1 日から 12 月 31 日の年が想定されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="9d32e-115">[カレンダー] オプションは各年の 1 月 1 日に減価償却基準を更新します。これは通常、正味簿価額から救済価格を差し引いた値です。</span><span class="sxs-lookup"><span data-stu-id="9d32e-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="9d32e-116">このトピックの後の例では、計算列の最初の式の分子が減価償却基準です。</span><span class="sxs-lookup"><span data-stu-id="9d32e-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="9d32e-117">[暦年] を選択すると、[期間の頻度] フィールドで次のオプションが使用できます。このオプションによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="9d32e-118">[年 1 回] を選択すると、12 月 31 日に金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="9d32e-119">[月 1 回] を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="9d32e-120">[四半期に 1 回] を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="9d32e-121">[半期に 1 回] を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="9d32e-122">[毎日] を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="9d32e-123">たとえば、[年 1 回] を選択すると、年次減価償却は年に 1 回、12 月 31 日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="9d32e-124">[月 1 回] を選択すると、月次の減価償却が年次減価償却金額の 12 分の 1 として毎月転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="9d32e-125">会計年度</span><span class="sxs-lookup"><span data-stu-id="9d32e-125">Fiscal</span></span>

<span data-ttu-id="9d32e-126">[償却年] フィールドで [会計年度] を選択した場合は、耐用年数定額減価償却が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="9d32e-127">これは、帳簿で指定された会計カレンダー、または [元帳] ページで選択された会計カレンダーで定義される会計年度に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="9d32e-128">会計カレンダーは、[会計カレンダー] ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="9d32e-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="9d32e-129">たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="9d32e-130">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="9d32e-131">減価償却は各会計年度期間に合わせて自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="9d32e-132">次の会計年度の期間の長さは、[会計カレンダー] フォームで新しい会計年度を作成するときに設定する会計年度期間に基づきます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="9d32e-133">[会計年度] を選択した場合、[期間の頻度] フィールドで次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="9d32e-134">[年 1 回] を選択すると、会計年度に対して計算された減価償却の合計金額が、会計年度の最終日に 1 つの金額として転記されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="9d32e-135">[会計年度期間] を選択すると、会計年度に対して計算された減価償却の合計額が、会計年度の [会計カレンダー] フォームに定義されている会計年度期間に見越し計上されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="9d32e-136">例: 変更されない固定資産の定額減価償却</span><span class="sxs-lookup"><span data-stu-id="9d32e-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="9d32e-137">固定資産に次の特性があるとします。</span><span class="sxs-lookup"><span data-stu-id="9d32e-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="9d32e-138">取得費用</span><span class="sxs-lookup"><span data-stu-id="9d32e-138">Acquisition cost</span></span>    | <span data-ttu-id="9d32e-139">11,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-139">11,000</span></span> |
| <span data-ttu-id="9d32e-140">救済価格</span><span class="sxs-lookup"><span data-stu-id="9d32e-140">Salvage value</span></span>       | <span data-ttu-id="9d32e-141">1.000</span><span class="sxs-lookup"><span data-stu-id="9d32e-141">1,000</span></span>  |
| <span data-ttu-id="9d32e-142">償却基礎額</span><span class="sxs-lookup"><span data-stu-id="9d32e-142">Depreciation base</span></span>   | <span data-ttu-id="9d32e-143">10,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-143">10,000</span></span> |
| <span data-ttu-id="9d32e-144">耐用年数</span><span class="sxs-lookup"><span data-stu-id="9d32e-144">Service life years</span></span>  | <span data-ttu-id="9d32e-145">5</span><span class="sxs-lookup"><span data-stu-id="9d32e-145">5</span></span>      |
| <span data-ttu-id="9d32e-146">年次減価償却</span><span class="sxs-lookup"><span data-stu-id="9d32e-146">Yearly depreciation</span></span> | <span data-ttu-id="9d32e-147">2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-147">2,000</span></span>  |

<span data-ttu-id="9d32e-148">毎年同じ減価償却金額を取得します。</span><span class="sxs-lookup"><span data-stu-id="9d32e-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="9d32e-149">(取得原価 - 救済価格)/耐用年数</span><span class="sxs-lookup"><span data-stu-id="9d32e-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="9d32e-150">期間</span><span class="sxs-lookup"><span data-stu-id="9d32e-150">Period</span></span> | <span data-ttu-id="9d32e-151">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="9d32e-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="9d32e-152">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="9d32e-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="9d32e-153">年 1</span><span class="sxs-lookup"><span data-stu-id="9d32e-153">Year 1</span></span> | <span data-ttu-id="9d32e-154">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="9d32e-155">9,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-155">9,000</span></span>                                 |
| <span data-ttu-id="9d32e-156">年 2</span><span class="sxs-lookup"><span data-stu-id="9d32e-156">Year 2</span></span> | <span data-ttu-id="9d32e-157">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="9d32e-158">7,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-158">7,000</span></span>                                 |
| <span data-ttu-id="9d32e-159">年 3</span><span class="sxs-lookup"><span data-stu-id="9d32e-159">Year 3</span></span> | <span data-ttu-id="9d32e-160">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="9d32e-161">5,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-161">5,000</span></span>                                 |
| <span data-ttu-id="9d32e-162">年 4</span><span class="sxs-lookup"><span data-stu-id="9d32e-162">Year 4</span></span> | <span data-ttu-id="9d32e-163">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="9d32e-164">3,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-164">3,000</span></span>                                 |
| <span data-ttu-id="9d32e-165">年 5</span><span class="sxs-lookup"><span data-stu-id="9d32e-165">Year 5</span></span> | <span data-ttu-id="9d32e-166">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="9d32e-167">1.000</span><span class="sxs-lookup"><span data-stu-id="9d32e-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="9d32e-168">例: 変更された固定資産の定額減価償却</span><span class="sxs-lookup"><span data-stu-id="9d32e-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="9d32e-169">年 2 に 4,000 の取得原価調整を同じ固定資産に追加するものとします。</span><span class="sxs-lookup"><span data-stu-id="9d32e-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="9d32e-170">取得原価調整の耐用年数は固定資産の耐用年数と同じで、取得時から開始されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="9d32e-171">正味簿価額が年 5 の年末に残り、取得原価調整の正味簿価額に対応します。</span><span class="sxs-lookup"><span data-stu-id="9d32e-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="9d32e-172">期間の減価償却は、以下の表に示すように計算されます。</span><span class="sxs-lookup"><span data-stu-id="9d32e-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="9d32e-173">期間</span><span class="sxs-lookup"><span data-stu-id="9d32e-173">Period</span></span> | <span data-ttu-id="9d32e-174">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="9d32e-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="9d32e-175">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="9d32e-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="9d32e-176">年 1</span><span class="sxs-lookup"><span data-stu-id="9d32e-176">Year 1</span></span> | <span data-ttu-id="9d32e-177">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="9d32e-178">11,000 - 2,000 = 9,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="9d32e-179">年 2</span><span class="sxs-lookup"><span data-stu-id="9d32e-179">Year 2</span></span> | <span data-ttu-id="9d32e-180">4,000 (取得原価調整)</span><span class="sxs-lookup"><span data-stu-id="9d32e-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="9d32e-181">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="9d32e-182">年 2</span><span class="sxs-lookup"><span data-stu-id="9d32e-182">Year 2</span></span> | <span data-ttu-id="9d32e-183">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="9d32e-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="9d32e-184">13,000 - 2,800 = 10,200</span><span class="sxs-lookup"><span data-stu-id="9d32e-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="9d32e-185">年 3</span><span class="sxs-lookup"><span data-stu-id="9d32e-185">Year 3</span></span> | <span data-ttu-id="9d32e-186">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="9d32e-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="9d32e-187">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="9d32e-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="9d32e-188">年 4</span><span class="sxs-lookup"><span data-stu-id="9d32e-188">Year 4</span></span> | <span data-ttu-id="9d32e-189">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="9d32e-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="9d32e-190">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="9d32e-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="9d32e-191">年 5</span><span class="sxs-lookup"><span data-stu-id="9d32e-191">Year 5</span></span> | <span data-ttu-id="9d32e-192">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="9d32e-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="9d32e-193">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="9d32e-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="9d32e-194">年 6</span><span class="sxs-lookup"><span data-stu-id="9d32e-194">Year 6</span></span> | <span data-ttu-id="9d32e-195">残余 800\*</span><span class="sxs-lookup"><span data-stu-id="9d32e-195">Remaining 800\*</span></span>                           | <span data-ttu-id="9d32e-196">1,800 – 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="9d32e-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="9d32e-197">\* 残余量は減価償却量を下回るため、残余量から救済量を差し引いた金額だけとなります。</span><span class="sxs-lookup"><span data-stu-id="9d32e-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






