---
title: 耐用年数残減価償却について
description: この記事は、減価償却の定額法残余耐用年数の概要を示します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd7bc6d773d85a1ba02151b96bf80f970845d4a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818515"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="fa0ff-103">耐用年数残減価償却について</span><span class="sxs-lookup"><span data-stu-id="fa0ff-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa0ff-104">この記事は、減価償却の定額法残余耐用年数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="fa0ff-105">固定資産減価償却プロファイルを設定して **減価償却プロファイル** ページの **方式** フィールドで **定額法残余耐用年数** を選択すると、減価償却プロファイルに割り当てられた固定資産は、その資産の耐用年数の残りに基づいて償却されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="fa0ff-106">一般に、各減価償却期間の減価償却金額は同じになります。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="fa0ff-107">耐用年数残減価償却を設定するには、**減価償却プロファイル** ページの **償却年** フィールドと **期間の頻度** フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="fa0ff-108">**期間の頻度** フィールドで使用できるオプションは、**償却年** フィールドで選択した値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="fa0ff-109">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="fa0ff-109">Select a depreciation year</span></span>
<span data-ttu-id="fa0ff-110">**減価償却プロファイル** ページの **償却年** フィールドで **暦年** または **会計年度** のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="fa0ff-111">既定値は **暦年** です。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-111">The default value is **Calendar**.</span></span> <span data-ttu-id="fa0ff-112">この選択により、**期間の頻度** フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="fa0ff-113">このフィールドによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="fa0ff-114">カレンダー</span><span class="sxs-lookup"><span data-stu-id="fa0ff-114">Calendar</span></span>

<span data-ttu-id="fa0ff-115">**_償却年_*_フィールドで **カレンダー** を選択すると、会計カレンダーを別に定義した場合でも、1 年は 1 月 1 日から 12 月 31 日までとみなされます。_\* カレンダー*\* オプション を使用すると、毎年 1 月 1 日に償却基礎額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="fa0ff-116">通常、償却基礎額は、正味簿価額から救済価格を差し引いた額です。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="fa0ff-117">このトピックの後の例では、計算列の最初の式の分子が減価償却基準です。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="fa0ff-118">償却年として **暦年** を選択すると、**期間の頻度** フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="fa0ff-119">**年 1 回** を選択すると、12 月 31 日に金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="fa0ff-120">**月 1 回** を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="fa0ff-121">**四半期に 1 回** を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="fa0ff-122">**半期に 1 回** を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="fa0ff-123">**毎日** を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="fa0ff-124">たとえば、**年 1 回** を選択すると、年次減価償却は年に 1 回だけ 12 年 1 月 31 日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="fa0ff-125">**月 1 回** を選択すると、月次の減価償却が年次減価償却量の 12 分の 1 として毎月転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="fa0ff-126">会計年度</span><span class="sxs-lookup"><span data-stu-id="fa0ff-126">Fiscal</span></span>

<span data-ttu-id="fa0ff-127">**償却年** フィールドで **会計年度** を選択した場合は、耐用年数残減価償却が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="fa0ff-128">減価償却は会計年度の残りに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="fa0ff-129">たとえば、会計年度 2015 年 7 月 1 日から 2016 年 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="fa0ff-130">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="fa0ff-131">減価償却は各会計年度期間に合わせて調整されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="fa0ff-132">次の会計年度の長さは **会計カレンダー** ページで設定された会計年度期間で決定されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="fa0ff-133">償却年として **会計年度** を選択すると、**期間の頻度** フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="fa0ff-134">**年 1 回** を選択すると、会計年度に対して計算された減価償却の合計量が、会計年度の最終日に 1 つの量として転記されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="fa0ff-135">**会計年度期間** では、会計年度に対して減価償却の合計額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="fa0ff-136">この額は、帳簿で指定された会計カレンダーの **会計カレンダー** ページで定義された会計年度期間に見越し計上されます。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="fa0ff-137">変更されない固定資産の定額減価償却例</span><span class="sxs-lookup"><span data-stu-id="fa0ff-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="fa0ff-138">固定資産には次の特徴があります。</span><span class="sxs-lookup"><span data-stu-id="fa0ff-138">A fixed asset has the following characteristics.</span></span>

| <span data-ttu-id="fa0ff-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="fa0ff-139">Field</span></span>               | <span data-ttu-id="fa0ff-140">先頭値</span><span class="sxs-lookup"><span data-stu-id="fa0ff-140">Value</span></span>  |
|---------------------|--------|
| <span data-ttu-id="fa0ff-141">取得価額</span><span class="sxs-lookup"><span data-stu-id="fa0ff-141">Acquisition cost</span></span>    | <span data-ttu-id="fa0ff-142">11,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-142">11,000</span></span> |
| <span data-ttu-id="fa0ff-143">救済価格</span><span class="sxs-lookup"><span data-stu-id="fa0ff-143">Salvage value</span></span>       | <span data-ttu-id="fa0ff-144">1.000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-144">1,000</span></span>  |
| <span data-ttu-id="fa0ff-145">償却基礎額</span><span class="sxs-lookup"><span data-stu-id="fa0ff-145">Depreciation base</span></span>   | <span data-ttu-id="fa0ff-146">10,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-146">10,000</span></span> |
| <span data-ttu-id="fa0ff-147">耐用年数</span><span class="sxs-lookup"><span data-stu-id="fa0ff-147">Service life years</span></span>  | <span data-ttu-id="fa0ff-148">5</span><span class="sxs-lookup"><span data-stu-id="fa0ff-148">5</span></span>      |
| <span data-ttu-id="fa0ff-149">年次減価償却</span><span class="sxs-lookup"><span data-stu-id="fa0ff-149">Yearly depreciation</span></span> | <span data-ttu-id="fa0ff-150">2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-150">2,000</span></span>  |

<span data-ttu-id="fa0ff-151">減価償却金額は毎年同じです。 (取得原価 - 救済価格) ÷ 耐用年数</span><span class="sxs-lookup"><span data-stu-id="fa0ff-151">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="fa0ff-152">期間</span><span class="sxs-lookup"><span data-stu-id="fa0ff-152">Period</span></span> | <span data-ttu-id="fa0ff-153">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="fa0ff-153">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="fa0ff-154">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="fa0ff-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="fa0ff-155">年 1</span><span class="sxs-lookup"><span data-stu-id="fa0ff-155">Year 1</span></span> | <span data-ttu-id="fa0ff-156">(11,000 – 1,000) ÷ 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-156">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="fa0ff-157">9,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-157">9,000</span></span>                                 |
| <span data-ttu-id="fa0ff-158">年 2</span><span class="sxs-lookup"><span data-stu-id="fa0ff-158">Year 2</span></span> | <span data-ttu-id="fa0ff-159">(9,000 – 1,000) ÷ 4 = 2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-159">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="fa0ff-160">7,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-160">7,000</span></span>                                 |
| <span data-ttu-id="fa0ff-161">年 3</span><span class="sxs-lookup"><span data-stu-id="fa0ff-161">Year 3</span></span> | <span data-ttu-id="fa0ff-162">(7,000 – 1,000) ÷ 3 = 2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-162">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="fa0ff-163">5,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-163">5,000</span></span>                                 |
| <span data-ttu-id="fa0ff-164">年 4</span><span class="sxs-lookup"><span data-stu-id="fa0ff-164">Year 4</span></span> | <span data-ttu-id="fa0ff-165">(5,000 – 1,000) ÷ 2 = 2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-165">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="fa0ff-166">3,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-166">3,000</span></span>                                 |
| <span data-ttu-id="fa0ff-167">年 5</span><span class="sxs-lookup"><span data-stu-id="fa0ff-167">Year 5</span></span> | <span data-ttu-id="fa0ff-168">(3,000 – 1,000) ÷ 1 = 2,000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-168">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="fa0ff-169">1.000</span><span class="sxs-lookup"><span data-stu-id="fa0ff-169">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]