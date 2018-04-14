---
title: "逓減残高による減価償却"
description: "この記事は、減価償却の逓減残高法の概要を示します。"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe7332eae681ea4e89a4fda0e97f85e6fc2f7d05
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="fc0af-103">逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="fc0af-103">Reduce balance depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fc0af-104">この記事は、減価償却の逓減残高法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="fc0af-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="fc0af-105">固定資産減価償却プロファイルを設定し、[減価償却プロファイル] ページの [方法] フィールドで [逓減残高] を選択すると、この減価償却プロファイルが割り当てられる資産の減価償却に、各減価償却期間で同じ比率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="fc0af-106">逓減残高による減価償却を設定するには、[減価償却プロファイル] ページの [一般] クイック タブのフィールドでも選択を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="fc0af-107">最初に、[償却年] フィールドで年を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc0af-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="fc0af-108">次のセクションで説明されている通り、選択に応じて、さまざまなオプションが [期間の頻度] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="fc0af-109">また、減価償却プロファイルの [割合] フィールドに値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="fc0af-110">[完全な償却] オプションを選択すると、残りの償却基礎額が最後の償却期間に組み込まれ、大きな金額になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="fc0af-111">一部の国または地域では定額法への切り替えが使用されません。</span><span class="sxs-lookup"><span data-stu-id="fc0af-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="fc0af-112">代替減価償却方式の量が基本減価償却プロファイルの量と等しいかまたはそれ以上になる場合切り替えが発生し、取得された減価償却量が代替方式の量になります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="fc0af-113">比率計算に基づくと資産が完全に償却されないため、資産を完全に償却するには [完全な償却] オプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="fc0af-114">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="fc0af-114">Select a depreciation year</span></span>
<span data-ttu-id="fc0af-115">[減価償却プロファイル] ページの [償却年] フィールドで [暦年] または [会計年度] のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="fc0af-116">この選択により、[期間の頻度] フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="fc0af-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="fc0af-117">既定のオプションは [暦年] です。</span><span class="sxs-lookup"><span data-stu-id="fc0af-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="fc0af-118">カレンダー</span><span class="sxs-lookup"><span data-stu-id="fc0af-118">Calendar</span></span>

<span data-ttu-id="fc0af-119">[カレンダー] オプションは各年の 1 月 1 日に減価償却基準を更新します。これは通常、正味簿価額から仕損価格を差し引いた値です。</span><span class="sxs-lookup"><span data-stu-id="fc0af-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="fc0af-120">このトピックの後半にある逓減残高による減価償却の例では、計算列における最初の式の分子が償却基礎額です。</span><span class="sxs-lookup"><span data-stu-id="fc0af-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="fc0af-121">[暦年] を選択すると、[期間の頻度] フィールドで次のオプションが使用できます。このオプションによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="fc0af-122">[年 1 回] を選択すると、12 月 31 日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="fc0af-123">[月 1 回] を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="fc0af-124">[四半期に 1 回] を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="fc0af-125">[半期に 1 回] を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="fc0af-126">[毎日] を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="fc0af-127">たとえば、[年 1 回] を選択すると、年次減価償却は年に 1 回、12 月 31 日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="fc0af-128">[月 1 回] を選択すると、月次の減価償却が年次減価償却金額の 12 分の 1 として毎月転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="fc0af-129">会計年度</span><span class="sxs-lookup"><span data-stu-id="fc0af-129">Fiscal</span></span>

<span data-ttu-id="fc0af-130">[償却年] フィールドで [会計年度] を選択した場合は、定額減価償却方法が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="fc0af-131">これは [元帳] ページで選択された、会計カレンダーの [会計カレンダー] ページで設定された会計年度に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="fc0af-132">たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="fc0af-133">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="fc0af-134">減価償却は各会計年度期間に合わせて調整されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="fc0af-135">次の会計年度の期間の長さは、[会計カレンダー] ページで新しい会計年度を作成するときに設定する会計年度期間に基づきます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="fc0af-136">[会計年度] を選択した場合、[期間の頻度] フィールドで次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="fc0af-137">[年 1 回] を選択すると、会計年度に対して計算された減価償却の合計額が、会計年度の最終日に 1 つの金額として転記されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="fc0af-138">[会計年度期間] を選択すると、会計年度の減価償却計算の合計量が転記されます。これは [元帳] ページで選択された会計カレンダー、または固定資産の帳簿で選択された会計カレンダーのために定義される、会計年度期間に費用が発生します。</span><span class="sxs-lookup"><span data-stu-id="fc0af-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="fc0af-139">逓減残高による減価償却の例</span><span class="sxs-lookup"><span data-stu-id="fc0af-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="fc0af-140">固定資産取得額が 11,000、仕損価格が 1,000、償却率の係数が 30 であるとします。</span><span class="sxs-lookup"><span data-stu-id="fc0af-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="fc0af-141">逓減残高方法を使用すると、償却基礎額 (正味簿価額から仕損価格を差し引いた値) の 30% が前の減価償却期間終了時に計算されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="fc0af-142">最初の 3 年の減価償却が次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc0af-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="fc0af-143">期間</span><span class="sxs-lookup"><span data-stu-id="fc0af-143">Period</span></span> | <span data-ttu-id="fc0af-144">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="fc0af-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="fc0af-145">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="fc0af-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="fc0af-146">年 1</span><span class="sxs-lookup"><span data-stu-id="fc0af-146">Year 1</span></span> | <span data-ttu-id="fc0af-147">(11,000 - 1,000) \* 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="fc0af-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="fc0af-148">(11,000 - 1,000) - 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="fc0af-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="fc0af-149">年 2</span><span class="sxs-lookup"><span data-stu-id="fc0af-149">Year 2</span></span> | <span data-ttu-id="fc0af-150">(7,000 - 1,000) \* 30% = 1,800</span><span class="sxs-lookup"><span data-stu-id="fc0af-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="fc0af-151">(7,000 -1,800) = 5,200</span><span class="sxs-lookup"><span data-stu-id="fc0af-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="fc0af-152">年 3</span><span class="sxs-lookup"><span data-stu-id="fc0af-152">Year 3</span></span> | <span data-ttu-id="fc0af-153">(5,200 - 1,000) \* 30% = 1,260</span><span class="sxs-lookup"><span data-stu-id="fc0af-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="fc0af-154">(5,200 - 1,260) = 3,940</span><span class="sxs-lookup"><span data-stu-id="fc0af-154">(5,200 - 1,260) = 3,940</span></span>               |


-






