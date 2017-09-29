---
title: "売上税コードの合計額と間隔計算オプション"
description: "この記事は、売上税コードの [計算方法] フィールドのオプションと、範囲金額および合計額の売上税計算方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 55cb0f20dbd671e39d0f409a87cec93efd9ce4d6
ms.openlocfilehash: bab0f6ca21f4216b70cccf24f5781e0dbf48b7f8
ms.contentlocale: ja-jp
ms.lasthandoff: 07/07/2017


---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="6687d-103">売上税コードの合計額と間隔計算オプション</span><span class="sxs-lookup"><span data-stu-id="6687d-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



<span data-ttu-id="6687d-104">この記事は、売上税コードの [計算方法] フィールドのオプションと、範囲金額および合計額の売上税計算方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6687d-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="6687d-105">売上税コードは、合計額と範囲金額のいずれかで計算する設定ができます。</span><span class="sxs-lookup"><span data-stu-id="6687d-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="6687d-106">[売上税コード] ページで、[計算] クイック タブの [計算方法] フィールドで売上税コードの計算方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="6687d-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
-   <span data-ttu-id="6687d-107">[合計額] – 課税対象額全体に税率が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6687d-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
-   <span data-ttu-id="6687d-108">[間隔] – 課税対象額が複数に分かれ、それぞれ特定の売上税率の範囲に分かれます。</span><span class="sxs-lookup"><span data-stu-id="6687d-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="6687d-109">所定の範囲に分類された部分的金額は、その範囲の税率で課税されます。</span><span class="sxs-lookup"><span data-stu-id="6687d-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="6687d-110">各金額間隔に対して計算された税額の合計が売上税となります。</span><span class="sxs-lookup"><span data-stu-id="6687d-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
> [!NOTE]                                                                                                                              
> <span data-ttu-id="6687d-111">[間隔] オプションは、[総勘定元帳パラメーター] ページの [売上税] の領域の [計算方法] フィールドで [行] を選択した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6687d-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="6687d-112">間隔は、[売上税コード値] ページで税率ごとの最小および最大の限度額を入力して設定します。</span><span class="sxs-lookup"><span data-stu-id="6687d-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="6687d-113">選択した方法に関係なく、すべての課税対象額について税額を計算するには、次のルールに従って範囲を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6687d-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="6687d-114">最初の範囲の下限はゼロとします。</span><span class="sxs-lookup"><span data-stu-id="6687d-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="6687d-115">最後の範囲の上限は無限を示すゼロとします。</span><span class="sxs-lookup"><span data-stu-id="6687d-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="6687d-116">範囲の最大値は、次の範囲の最小値未満に設定します。</span><span class="sxs-lookup"><span data-stu-id="6687d-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="6687d-117">ある金額が前の範囲の上限で、次の範囲の下限の場合、最初の範囲の税率が金額に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6687d-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="6687d-118">金額が上限と下限で定義した範囲の外になる場合、税率 0 が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6687d-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="6687d-119">例: 合計額による計算方法</span><span class="sxs-lookup"><span data-stu-id="6687d-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="6687d-120">[売上税コード値] ページで、売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="6687d-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>
|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="6687d-121">**最小値**</span><span class="sxs-lookup"><span data-stu-id="6687d-121">**Minimum limit**</span></span> | <span data-ttu-id="6687d-122">**上限**</span><span class="sxs-lookup"><span data-stu-id="6687d-122">**Maximum limit**</span></span> | <span data-ttu-id="6687d-123">**税率**</span><span class="sxs-lookup"><span data-stu-id="6687d-123">**Tax rate**</span></span> |
| <span data-ttu-id="6687d-124">0.00</span><span class="sxs-lookup"><span data-stu-id="6687d-124">0.00</span></span>              | <span data-ttu-id="6687d-125">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-125">50.00</span></span>             | <span data-ttu-id="6687d-126">30%</span><span class="sxs-lookup"><span data-stu-id="6687d-126">30%</span></span>          |
| <span data-ttu-id="6687d-127">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-127">50.00</span></span>             | <span data-ttu-id="6687d-128">100.00</span><span class="sxs-lookup"><span data-stu-id="6687d-128">100.00</span></span>            | <span data-ttu-id="6687d-129">20%</span><span class="sxs-lookup"><span data-stu-id="6687d-129">20%</span></span>          |
| <span data-ttu-id="6687d-130">100.00</span><span class="sxs-lookup"><span data-stu-id="6687d-130">100.00</span></span>            | <span data-ttu-id="6687d-131">0.00</span><span class="sxs-lookup"><span data-stu-id="6687d-131">0.00</span></span>              | <span data-ttu-id="6687d-132">10%</span><span class="sxs-lookup"><span data-stu-id="6687d-132">10%</span></span>          |

<span data-ttu-id="6687d-133">売上税は全課税対象額で計算します。</span><span class="sxs-lookup"><span data-stu-id="6687d-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="6687d-134">課税対象額 (価格)</span><span class="sxs-lookup"><span data-stu-id="6687d-134">Taxable amount (price)</span></span> | <span data-ttu-id="6687d-135">計算</span><span class="sxs-lookup"><span data-stu-id="6687d-135">Calculation</span></span>    | <span data-ttu-id="6687d-136">消費税</span><span class="sxs-lookup"><span data-stu-id="6687d-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="6687d-137">35.00</span><span class="sxs-lookup"><span data-stu-id="6687d-137">35.00</span></span>                  | <span data-ttu-id="6687d-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="6687d-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="6687d-139">1050</span><span class="sxs-lookup"><span data-stu-id="6687d-139">10.50</span></span>     |
| <span data-ttu-id="6687d-140">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-140">50.00</span></span>                  | <span data-ttu-id="6687d-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="6687d-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="6687d-142">15.00</span><span class="sxs-lookup"><span data-stu-id="6687d-142">15.00</span></span>     |
| <span data-ttu-id="6687d-143">85.00</span><span class="sxs-lookup"><span data-stu-id="6687d-143">85.00</span></span>                  | <span data-ttu-id="6687d-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="6687d-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="6687d-145">17.00</span><span class="sxs-lookup"><span data-stu-id="6687d-145">17.00</span></span>     |
| <span data-ttu-id="6687d-146">305.00</span><span class="sxs-lookup"><span data-stu-id="6687d-146">305.00</span></span>                 | <span data-ttu-id="6687d-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="6687d-147">305.00 \* 0.10</span></span> | <span data-ttu-id="6687d-148">30.50</span><span class="sxs-lookup"><span data-stu-id="6687d-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="6687d-149">例: 範囲間隔による計算方法</span><span class="sxs-lookup"><span data-stu-id="6687d-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="6687d-150">[値] ページで、売上税率を以下の間隔の範囲で設定します。</span><span class="sxs-lookup"><span data-stu-id="6687d-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="6687d-151">**最小値**</span><span class="sxs-lookup"><span data-stu-id="6687d-151">**Minimum limit**</span></span> | <span data-ttu-id="6687d-152">**上限**</span><span class="sxs-lookup"><span data-stu-id="6687d-152">**Maximum limit**</span></span> | <span data-ttu-id="6687d-153">**税率**</span><span class="sxs-lookup"><span data-stu-id="6687d-153">**Tax rate**</span></span> |
| <span data-ttu-id="6687d-154">0.00</span><span class="sxs-lookup"><span data-stu-id="6687d-154">0.00</span></span>              | <span data-ttu-id="6687d-155">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-155">50.00</span></span>             | <span data-ttu-id="6687d-156">30%</span><span class="sxs-lookup"><span data-stu-id="6687d-156">30%</span></span>          |
| <span data-ttu-id="6687d-157">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-157">50.00</span></span>             | <span data-ttu-id="6687d-158">100.00</span><span class="sxs-lookup"><span data-stu-id="6687d-158">100.00</span></span>            | <span data-ttu-id="6687d-159">20%</span><span class="sxs-lookup"><span data-stu-id="6687d-159">20%</span></span>          |
| <span data-ttu-id="6687d-160">100.00</span><span class="sxs-lookup"><span data-stu-id="6687d-160">100.00</span></span>            | <span data-ttu-id="6687d-161">0.00</span><span class="sxs-lookup"><span data-stu-id="6687d-161">0.00</span></span>              | <span data-ttu-id="6687d-162">10%</span><span class="sxs-lookup"><span data-stu-id="6687d-162">10%</span></span>          |

<span data-ttu-id="6687d-163">各金額間隔に対して計算された税額の合計が売上税となります。</span><span class="sxs-lookup"><span data-stu-id="6687d-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="6687d-164">課税対象額 (価格)</span><span class="sxs-lookup"><span data-stu-id="6687d-164">Taxable amount (price)</span></span> | <span data-ttu-id="6687d-165">計算</span><span class="sxs-lookup"><span data-stu-id="6687d-165">Calculation</span></span>                                                               | <span data-ttu-id="6687d-166">消費税</span><span class="sxs-lookup"><span data-stu-id="6687d-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6687d-167">35.00</span><span class="sxs-lookup"><span data-stu-id="6687d-167">35.00</span></span>                  | <span data-ttu-id="6687d-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="6687d-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="6687d-169">1050</span><span class="sxs-lookup"><span data-stu-id="6687d-169">10.50</span></span>     |
| <span data-ttu-id="6687d-170">50.00</span><span class="sxs-lookup"><span data-stu-id="6687d-170">50.00</span></span>                  | <span data-ttu-id="6687d-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="6687d-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="6687d-172">15.00</span><span class="sxs-lookup"><span data-stu-id="6687d-172">15.00</span></span>     |
| <span data-ttu-id="6687d-173">85.00</span><span class="sxs-lookup"><span data-stu-id="6687d-173">85.00</span></span>                  | <span data-ttu-id="6687d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="6687d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="6687d-175">22.00</span><span class="sxs-lookup"><span data-stu-id="6687d-175">22.00</span></span>     |
| <span data-ttu-id="6687d-176">305.00</span><span class="sxs-lookup"><span data-stu-id="6687d-176">305.00</span></span>                 | <span data-ttu-id="6687d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="6687d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="6687d-178">45.50</span><span class="sxs-lookup"><span data-stu-id="6687d-178">45.50</span></span>     |

 

<span data-ttu-id="6687d-179">詳細については、[[基準金額] および [計算方法] フィールドに基づいた、売上税の税率の決定](marginal-base-field.md) を、参照して下さい。</span><span class="sxs-lookup"><span data-stu-id="6687d-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






