---
title: 200% 逓減残高による減価償却
description: この記事は、減価償却の 200% 逓減残高法の概要を示します。
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187432"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="a3cd0-103">200% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="a3cd0-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3cd0-104">この記事は、減価償却の 200% 逓減残高法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="a3cd0-105">固定資産減価償却プロファイルを設定し、**減価償却プロファイル** ページの**方法**フィールドで **200% 逓減残高**を選択すると、この減価償却プロファイルが割り当てられる固定資産の減価償却に、各減価償却期間で同じ比率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="a3cd0-106">この比率は資産の耐用年数に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="a3cd0-107">たとえば、資産の耐用年数が 5 年の場合は、比率が 40% (200% ÷ 5) として計算されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="a3cd0-108">この方法は倍額定率法とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="a3cd0-109">200% 逓減残高による減価償却を設定するには、**減価償却プロファイル** ページの**償却年**フィールドと**期間の頻度**フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a3cd0-110">**期間の頻度**フィールドで使用できるオプションは、**償却年**フィールドで選択した値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="a3cd0-111">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="a3cd0-111">Select a depreciation year</span></span>
<span data-ttu-id="a3cd0-112">**減価償却プロファイル**ページの**償却年**フィールドで**暦年**または**会計年度**のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a3cd0-113">既定値は**暦年**です。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="a3cd0-114">この選択により、**期間の頻度**フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="a3cd0-115">このフィールドによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="a3cd0-116">カレンダー</span><span class="sxs-lookup"><span data-stu-id="a3cd0-116">Calendar</span></span>

<span data-ttu-id="a3cd0-117">**償却年**フィールドの既定値である**暦年**をそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="a3cd0-118">**暦年**選択すると、毎年 1 月 1 日に償却基礎額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="a3cd0-119">通常、減価償却は、正味簿価額から仕損価格を差し引いた額です。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="a3cd0-120">このトピックの後の例では、計算列の最初の式の分子が減価償却基準です。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="a3cd0-121">償却年として**暦年**を選択すると、**期間の頻度**フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a3cd0-122">**年 1 回**を選択すると、12 月 31 日に金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="a3cd0-123">**月 1 回**を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="a3cd0-124">**四半期に 1 回**を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="a3cd0-125">**半期に 1 回**を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="a3cd0-126">**毎日**を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="a3cd0-127">会計年度</span><span class="sxs-lookup"><span data-stu-id="a3cd0-127">Fiscal</span></span>

<span data-ttu-id="a3cd0-128">**償却**年フィールドで**会計年度**を選択した場合、200% 逓減残高による減価償却は、帳簿で指定した会計カレンダーまたは**元帳**ページで選択した会計カレンダーの会計年度に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="a3cd0-129">会計カレンダーは、**会計カレンダー**ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="a3cd0-130">たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="a3cd0-131">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="a3cd0-132">減価償却は各年度期間に合わせて調整されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="a3cd0-133">次の会計年度の長さは**会計カレンダー**ページで設定された期間で決定されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="a3cd0-134">償却年として**会計年度**を選択すると、**期間の頻度**フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a3cd0-135">**年 1 回**を選択すると、会計年度に対して計算された減価償却の合計量が、会計年度の最終日に 1 つの量として転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="a3cd0-136">**会計年度期間**では、会計年度に対して計算された減価償却の合計額が会計年度の最終日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="a3cd0-137">この金額は**会計カレンダー**ページで定義された会計年度期間に見越計上されます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="a3cd0-138">200% 逓減残高による減価償却の例</span><span class="sxs-lookup"><span data-stu-id="a3cd0-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="a3cd0-139">取得価額</span><span class="sxs-lookup"><span data-stu-id="a3cd0-139">Acquisition cost</span></span>               | <span data-ttu-id="a3cd0-140">11,000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-140">11,000</span></span> |
| <span data-ttu-id="a3cd0-141">救済価格</span><span class="sxs-lookup"><span data-stu-id="a3cd0-141">Salvage value</span></span>                  | <span data-ttu-id="a3cd0-142">1, 000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-142">1, 000</span></span> |
| <span data-ttu-id="a3cd0-143">償却基礎額</span><span class="sxs-lookup"><span data-stu-id="a3cd0-143">Depreciation base</span></span>              | <span data-ttu-id="a3cd0-144">10,000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-144">10,000</span></span> |
| <span data-ttu-id="a3cd0-145">耐用年数</span><span class="sxs-lookup"><span data-stu-id="a3cd0-145">Service life years</span></span>             | <span data-ttu-id="a3cd0-146">5</span><span class="sxs-lookup"><span data-stu-id="a3cd0-146">5</span></span>      |
| <span data-ttu-id="a3cd0-147">年次減価償却率</span><span class="sxs-lookup"><span data-stu-id="a3cd0-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="a3cd0-148">40%</span><span class="sxs-lookup"><span data-stu-id="a3cd0-148">40%</span></span>    |

<span data-ttu-id="a3cd0-149">200% 低減残高法では、200% を耐用年数で除算します。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="a3cd0-150">この比率は、資産の正味簿価額で乗算され、各年の減価償却金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="a3cd0-151">期間</span><span class="sxs-lookup"><span data-stu-id="a3cd0-151">Period</span></span> | <span data-ttu-id="a3cd0-152">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="a3cd0-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="a3cd0-153">簿価額</span><span class="sxs-lookup"><span data-stu-id="a3cd0-153">Book value</span></span>             | <span data-ttu-id="a3cd0-154">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="a3cd0-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="a3cd0-155">年 1</span><span class="sxs-lookup"><span data-stu-id="a3cd0-155">Year 1</span></span> | <span data-ttu-id="a3cd0-156">(11,000 – 1,000) × 40% = 4,000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="a3cd0-157">11,000 – 4,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="a3cd0-158">11,000 – 1,000 – 4,000 = 6,000</span><span class="sxs-lookup"><span data-stu-id="a3cd0-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="a3cd0-159">年 2</span><span class="sxs-lookup"><span data-stu-id="a3cd0-159">Year 2</span></span> | <span data-ttu-id="a3cd0-160">6,000 × 40% = 2,400</span><span class="sxs-lookup"><span data-stu-id="a3cd0-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="a3cd0-161">7,000 – 2,400 = 4,600</span><span class="sxs-lookup"><span data-stu-id="a3cd0-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="a3cd0-162">6,000 – 2,400 = 3,600</span><span class="sxs-lookup"><span data-stu-id="a3cd0-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="a3cd0-163">年 3</span><span class="sxs-lookup"><span data-stu-id="a3cd0-163">Year 3</span></span> | <span data-ttu-id="a3cd0-164">3,600 × 40% = 1,440</span><span class="sxs-lookup"><span data-stu-id="a3cd0-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="a3cd0-165">4,600 – 1,440 = 3,160</span><span class="sxs-lookup"><span data-stu-id="a3cd0-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="a3cd0-166">3,600 – 1,440 = 2,160</span><span class="sxs-lookup"><span data-stu-id="a3cd0-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="a3cd0-167">通常、200% 逓減残高による減価償却方法を使用して計算される金額が、定額法を使用して計算された金額より低くなる場合、残余耐用期間では定額法への換算が行われます。</span><span class="sxs-lookup"><span data-stu-id="a3cd0-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



