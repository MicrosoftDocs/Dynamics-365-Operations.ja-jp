---
title: 175% 逓減残高による減価償却
description: このトピックは、減価償却の 175% 逓減残高法の概要を示します。
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a63293dbf24c27733f8013947aeab5792fa0db9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "320170"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="49244-103">175% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="49244-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49244-104">このトピックは、減価償却の 175% 逓減残高法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="49244-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="49244-105">固定資産減価償却プロファイルを設定し、**減価償却プロファイル**ページの**方法**フィールドで、**175% 逓減残高**を選択すると、減価償却プロファイルが割り当てられる固定資産は各減価償却期間で適用される比率と同じ比率で減価償却されます。</span><span class="sxs-lookup"><span data-stu-id="49244-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="49244-106">175% 逓減残高による減価償却を設定するには、**減価償却プロファイル**ページの**償却年**フィールドと**期間の頻度**フィールドでオプションを選択する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="49244-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="49244-107">**期間の頻度**フィールドで使用できるオプションは、**償却年**フィールドで選択した値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="49244-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="49244-108">償却年の選択</span><span class="sxs-lookup"><span data-stu-id="49244-108">Select a depreciation year</span></span>
<span data-ttu-id="49244-109">**減価償却プロファイル**ページの**償却年**フィールドで**暦年**または**会計年度**のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="49244-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="49244-110">既定値は**暦年**です。</span><span class="sxs-lookup"><span data-stu-id="49244-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="49244-111">この選択により、**期間の頻度**フィールドで指定できるオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="49244-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="49244-112">このフィールドによって、暦年を通した償却発生額の転記日付と金額が定義されます。</span><span class="sxs-lookup"><span data-stu-id="49244-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="49244-113">カレンダー</span><span class="sxs-lookup"><span data-stu-id="49244-113">Calendar</span></span>

<span data-ttu-id="49244-114">**償却年**フィールドの既定値である**暦年**をそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="49244-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="49244-115">**暦年**選択すると、毎年 1 月 1 日に償却基礎額が更新されます。</span><span class="sxs-lookup"><span data-stu-id="49244-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="49244-116">通常、償却基礎額は、正味簿価額から仕損価格を差し引いた額です。</span><span class="sxs-lookup"><span data-stu-id="49244-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="49244-117">このトピックの後の例では、計算列の最初の式の分子が減価償却基準です。</span><span class="sxs-lookup"><span data-stu-id="49244-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="49244-118">償却年として**暦年**を選択すると、**期間の頻度**フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="49244-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="49244-119">**年 1 回**を選択すると、12 月 31 日に金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="49244-120">**月 1 回**を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="49244-121">**四半期に 1 回**を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="49244-122">**半期に 1 回**を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="49244-123">**毎日**を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="49244-124">会計年度</span><span class="sxs-lookup"><span data-stu-id="49244-124">Fiscal</span></span>

<span data-ttu-id="49244-125">**償却年**フィールドで**会計年度**を選択すると、175% 逓減残高による減価償却は、帳簿で指定した会計カレンダーまたは**元帳**ページで選択した会計カレンダーの会計年度に基づいて計算します。</span><span class="sxs-lookup"><span data-stu-id="49244-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="49244-126">会計カレンダーは、**会計カレンダー**ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="49244-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="49244-127">詳細については、[会計カレンダー、会計年度、および期間](../budgeting/fiscal-calendars-fiscal-years-periods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49244-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="49244-128">たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。</span><span class="sxs-lookup"><span data-stu-id="49244-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="49244-129">会計年度の期間は 12 か月よりも長くすることも短くすることもできます。</span><span class="sxs-lookup"><span data-stu-id="49244-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="49244-130">減価償却は各期間に合わせて自動的に調整され、次の会計年度の長さは、**会計カレンダー**ページで設定された期間で決定されます。</span><span class="sxs-lookup"><span data-stu-id="49244-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="49244-131">償却年として**会計年度**を選択すると、**期間の頻度**フィールドで次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="49244-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="49244-132">**年 1 回**を選択すると、会計年度に対して計算された減価償却の合計額が、会計年度の最終日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="49244-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="49244-133">**会計年度期間**では、会計年度における減価償却の合計額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="49244-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="49244-134">この金額は**会計カレンダー**ページで定義された会計年度期間に見越計上されます。</span><span class="sxs-lookup"><span data-stu-id="49244-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="49244-135">175% 逓減残高による減価償却の例</span><span class="sxs-lookup"><span data-stu-id="49244-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="49244-136">取得価額</span><span class="sxs-lookup"><span data-stu-id="49244-136">Acquisition cost</span></span>               | <span data-ttu-id="49244-137">11,000</span><span class="sxs-lookup"><span data-stu-id="49244-137">11,000</span></span> |
| <span data-ttu-id="49244-138">救済価格</span><span class="sxs-lookup"><span data-stu-id="49244-138">Salvage value</span></span>                  | <span data-ttu-id="49244-139">1.000</span><span class="sxs-lookup"><span data-stu-id="49244-139">1,000</span></span>  |
| <span data-ttu-id="49244-140">償却基礎額</span><span class="sxs-lookup"><span data-stu-id="49244-140">Depreciation base</span></span>              | <span data-ttu-id="49244-141">10,000</span><span class="sxs-lookup"><span data-stu-id="49244-141">10,000</span></span> |
| <span data-ttu-id="49244-142">耐用年数</span><span class="sxs-lookup"><span data-stu-id="49244-142">Service life years</span></span>             | <span data-ttu-id="49244-143">5</span><span class="sxs-lookup"><span data-stu-id="49244-143">5</span></span>      |
| <span data-ttu-id="49244-144">年次減価償却率</span><span class="sxs-lookup"><span data-stu-id="49244-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="49244-145">35%</span><span class="sxs-lookup"><span data-stu-id="49244-145">35%</span></span>    |

<span data-ttu-id="49244-146">175% 逓減残高による減価償却法では、175% を耐用年数で除算します。</span><span class="sxs-lookup"><span data-stu-id="49244-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="49244-147">この比率は、資産の正味簿価額で乗算され、各年の減価償却金額が決まります。</span><span class="sxs-lookup"><span data-stu-id="49244-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="49244-148">期間</span><span class="sxs-lookup"><span data-stu-id="49244-148">Period</span></span> | <span data-ttu-id="49244-149">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="49244-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="49244-150">簿価額</span><span class="sxs-lookup"><span data-stu-id="49244-150">Book value</span></span>                  | <span data-ttu-id="49244-151">年末の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="49244-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="49244-152">年 1</span><span class="sxs-lookup"><span data-stu-id="49244-152">Year 1</span></span> | <span data-ttu-id="49244-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="49244-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="49244-154">11,000 - 3,500 = 7,500</span><span class="sxs-lookup"><span data-stu-id="49244-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="49244-155">11,000 – 1,000 – 3,500 = 6,500</span><span class="sxs-lookup"><span data-stu-id="49244-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="49244-156">年 2</span><span class="sxs-lookup"><span data-stu-id="49244-156">Year 2</span></span> | <span data-ttu-id="49244-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="49244-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="49244-158">7,500 - 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="49244-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="49244-159">6,500 - 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="49244-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="49244-160">年 3</span><span class="sxs-lookup"><span data-stu-id="49244-160">Year 3</span></span> | <span data-ttu-id="49244-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="49244-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="49244-162">5,225 - 1,478.75 = 3,746.25</span><span class="sxs-lookup"><span data-stu-id="49244-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="49244-163">4,225 - 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="49244-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="49244-164">通常、175% 逓減残高による減価償却方法を使用して計算される金額が、定額法を使用して計算された金額より低くなる場合、残余耐用期間では定額法への換算が行われます。</span><span class="sxs-lookup"><span data-stu-id="49244-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



