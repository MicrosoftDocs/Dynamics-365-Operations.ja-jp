---
title: 売上税コードの合計額と間隔計算オプション
description: この記事は、売上税コードの [計算方法] フィールドのオプションと、範囲金額および合計額の売上税計算方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0414f835b7797d2ed554f8d9dbd95b2ad47bba43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234120"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="e4c87-103">売上税コードの合計額と間隔計算オプション</span><span class="sxs-lookup"><span data-stu-id="e4c87-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4c87-104">この記事は、売上税コードの [計算方法] フィールドのオプションと、範囲金額および合計額の売上税計算方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="e4c87-105">売上税コードは、合計額と範囲金額のいずれかで計算する設定ができます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="e4c87-106">[売上税コード] ページで、[計算] クイック タブの [計算方法] フィールドで売上税コードの計算方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="e4c87-107">[合計額] – 課税対象額全体に税率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="e4c87-108">[間隔] – 課税対象額が複数に分かれ、それぞれ特定の売上税率の範囲に分かれます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="e4c87-109">所定の範囲に分類された部分的金額は、その範囲の税率で課税されます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="e4c87-110">各金額間隔に対して計算された税額の合計が売上税となります。</span><span class="sxs-lookup"><span data-stu-id="e4c87-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="e4c87-111">[間隔] オプションは、[総勘定元帳パラメーター] ページの [売上税] の領域の [計算方法] フィールドで [行] を選択した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="e4c87-112">間隔は、[売上税コード値] ページで税率ごとの最小および最大の限度額を入力して設定します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="e4c87-113">選択した方法に関係なく、すべての課税対象額について税額を計算するには、次のルールに従って範囲を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4c87-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="e4c87-114">最初の範囲の下限はゼロとします。</span><span class="sxs-lookup"><span data-stu-id="e4c87-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="e4c87-115">最後の範囲の上限は無限を示すゼロとします。</span><span class="sxs-lookup"><span data-stu-id="e4c87-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="e4c87-116">範囲の最大値は、次の範囲の最小値未満に設定します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="e4c87-117">ある金額が前の範囲の上限で、次の範囲の下限の場合、最初の範囲の税率が金額に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="e4c87-118">金額が上限と下限で定義した範囲の外になる場合、税率 0 が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e4c87-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="e4c87-119">例: 合計額による計算方法</span><span class="sxs-lookup"><span data-stu-id="e4c87-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="e4c87-120">[売上税コード値] ページで、売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="e4c87-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="e4c87-121">**最小値**</span><span class="sxs-lookup"><span data-stu-id="e4c87-121">**Minimum limit**</span></span> | <span data-ttu-id="e4c87-122">**上限**</span><span class="sxs-lookup"><span data-stu-id="e4c87-122">**Maximum limit**</span></span> | <span data-ttu-id="e4c87-123">**税率**</span><span class="sxs-lookup"><span data-stu-id="e4c87-123">**Tax rate**</span></span> |
| <span data-ttu-id="e4c87-124">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-124">0.00</span></span>              | <span data-ttu-id="e4c87-125">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-125">50.00</span></span>             | <span data-ttu-id="e4c87-126">30%</span><span class="sxs-lookup"><span data-stu-id="e4c87-126">30%</span></span>          |
| <span data-ttu-id="e4c87-127">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-127">50.00</span></span>             | <span data-ttu-id="e4c87-128">100.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-128">100.00</span></span>            | <span data-ttu-id="e4c87-129">20%</span><span class="sxs-lookup"><span data-stu-id="e4c87-129">20%</span></span>          |
| <span data-ttu-id="e4c87-130">100.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-130">100.00</span></span>            | <span data-ttu-id="e4c87-131">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-131">0.00</span></span>              | <span data-ttu-id="e4c87-132">10%</span><span class="sxs-lookup"><span data-stu-id="e4c87-132">10%</span></span>          |

<span data-ttu-id="e4c87-133">売上税は全課税対象額で計算します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="e4c87-134">課税対象額 (価格)</span><span class="sxs-lookup"><span data-stu-id="e4c87-134">Taxable amount (price)</span></span> | <span data-ttu-id="e4c87-135">計算</span><span class="sxs-lookup"><span data-stu-id="e4c87-135">Calculation</span></span>    | <span data-ttu-id="e4c87-136">消費税</span><span class="sxs-lookup"><span data-stu-id="e4c87-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="e4c87-137">35.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-137">35.00</span></span>                  | <span data-ttu-id="e4c87-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="e4c87-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="e4c87-139">10.50</span><span class="sxs-lookup"><span data-stu-id="e4c87-139">10.50</span></span>     |
| <span data-ttu-id="e4c87-140">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-140">50.00</span></span>                  | <span data-ttu-id="e4c87-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="e4c87-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="e4c87-142">15.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-142">15.00</span></span>     |
| <span data-ttu-id="e4c87-143">85.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-143">85.00</span></span>                  | <span data-ttu-id="e4c87-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="e4c87-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="e4c87-145">17.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-145">17.00</span></span>     |
| <span data-ttu-id="e4c87-146">305.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-146">305.00</span></span>                 | <span data-ttu-id="e4c87-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="e4c87-147">305.00 \* 0.10</span></span> | <span data-ttu-id="e4c87-148">30.50</span><span class="sxs-lookup"><span data-stu-id="e4c87-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="e4c87-149">例: 範囲間隔による計算方法</span><span class="sxs-lookup"><span data-stu-id="e4c87-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="e4c87-150">[値] ページで、売上税率を以下の間隔の範囲で設定します。</span><span class="sxs-lookup"><span data-stu-id="e4c87-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="e4c87-151">**最小値**</span><span class="sxs-lookup"><span data-stu-id="e4c87-151">**Minimum limit**</span></span> | <span data-ttu-id="e4c87-152">**上限**</span><span class="sxs-lookup"><span data-stu-id="e4c87-152">**Maximum limit**</span></span> | <span data-ttu-id="e4c87-153">**税率**</span><span class="sxs-lookup"><span data-stu-id="e4c87-153">**Tax rate**</span></span> |
| <span data-ttu-id="e4c87-154">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-154">0.00</span></span>              | <span data-ttu-id="e4c87-155">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-155">50.00</span></span>             | <span data-ttu-id="e4c87-156">30%</span><span class="sxs-lookup"><span data-stu-id="e4c87-156">30%</span></span>          |
| <span data-ttu-id="e4c87-157">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-157">50.00</span></span>             | <span data-ttu-id="e4c87-158">100.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-158">100.00</span></span>            | <span data-ttu-id="e4c87-159">20%</span><span class="sxs-lookup"><span data-stu-id="e4c87-159">20%</span></span>          |
| <span data-ttu-id="e4c87-160">100.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-160">100.00</span></span>            | <span data-ttu-id="e4c87-161">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-161">0.00</span></span>              | <span data-ttu-id="e4c87-162">10%</span><span class="sxs-lookup"><span data-stu-id="e4c87-162">10%</span></span>          |

<span data-ttu-id="e4c87-163">各金額間隔に対して計算された税額の合計が売上税となります。</span><span class="sxs-lookup"><span data-stu-id="e4c87-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="e4c87-164">課税対象額 (価格)</span><span class="sxs-lookup"><span data-stu-id="e4c87-164">Taxable amount (price)</span></span> | <span data-ttu-id="e4c87-165">計算</span><span class="sxs-lookup"><span data-stu-id="e4c87-165">Calculation</span></span>                                                               | <span data-ttu-id="e4c87-166">消費税</span><span class="sxs-lookup"><span data-stu-id="e4c87-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e4c87-167">35.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-167">35.00</span></span>                  | <span data-ttu-id="e4c87-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="e4c87-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="e4c87-169">10.50</span><span class="sxs-lookup"><span data-stu-id="e4c87-169">10.50</span></span>     |
| <span data-ttu-id="e4c87-170">50.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-170">50.00</span></span>                  | <span data-ttu-id="e4c87-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="e4c87-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="e4c87-172">15.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-172">15.00</span></span>     |
| <span data-ttu-id="e4c87-173">85.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-173">85.00</span></span>                  | <span data-ttu-id="e4c87-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="e4c87-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="e4c87-175">22.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-175">22.00</span></span>     |
| <span data-ttu-id="e4c87-176">305.00</span><span class="sxs-lookup"><span data-stu-id="e4c87-176">305.00</span></span>                 | <span data-ttu-id="e4c87-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="e4c87-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="e4c87-178">45.50</span><span class="sxs-lookup"><span data-stu-id="e4c87-178">45.50</span></span>     |



<span data-ttu-id="e4c87-179">詳細については、[基準金額および計算方法フィールドに基づいた、売上税の税率](marginal-base-field.md) を参照して下さい。</span><span class="sxs-lookup"><span data-stu-id="e4c87-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]