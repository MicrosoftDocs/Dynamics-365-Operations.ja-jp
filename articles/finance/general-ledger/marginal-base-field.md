---
title: 基準金額および計算方法に基づいた、売上税の税率
description: このトピックは、フィールドの基準金額および計算方法の値が、どのように販売および購買トランザクションの税率を決定するかを説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dcb51c730da3f2ad155675f06f5c1cd9e8476d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988656"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="638c2-103">基準金額および計算方法に基づいた、売上税の税率</span><span class="sxs-lookup"><span data-stu-id="638c2-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="638c2-104">このトピックは、フィールドの基準金額および計算方法の値が、どのように販売および購買トランザクションの税率を決定するかを説明します。</span><span class="sxs-lookup"><span data-stu-id="638c2-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="638c2-105">売上税コードのページのクイック タブの計算基準金額は、売上税コード値のページのレートから適切な税率をピッキングして、金額が使用されるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="638c2-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="638c2-106">計算方法フィールドで選択した方法と基準金額フィールドで設定した金額タイプの組み合わせにより、トランザクションの正確な税率を検索するロジックが決まります。</span><span class="sxs-lookup"><span data-stu-id="638c2-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="638c2-107">これらのフィールドの値のさまざまな組み合わせにより、以下の例のようにまったく異なる売上税計算が生成されます。</span><span class="sxs-lookup"><span data-stu-id="638c2-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="638c2-108">その例では、同じ税間隔の値を使用します。その値は売上税コード値のページで税コードごとに設定されます。</span><span class="sxs-lookup"><span data-stu-id="638c2-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="638c2-109">このページを開くには、[売上税コード] &gt; [売上税コードのページの値] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="638c2-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="638c2-110">基準金額が明細行または単位に基づいている 1 つ以上の売上税コードがある場合は、[総勘定元帳のパラメーター] ページの [計算方法] フィールドで値を [行] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="638c2-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="638c2-111">ラインごとの正味金額</span><span class="sxs-lookup"><span data-stu-id="638c2-111">Net amount per line</span></span>
<span data-ttu-id="638c2-112">他のすべての税を除外した請求明細行の正味金額に基づいて売上税の税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="638c2-113">例</span><span class="sxs-lookup"><span data-stu-id="638c2-113">Example</span></span>

<span data-ttu-id="638c2-114">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-115">金額間隔</span><span class="sxs-lookup"><span data-stu-id="638c2-115">Amount interval</span></span>    | <span data-ttu-id="638c2-116">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="638c2-117">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-117">0 - 50</span></span>             | <span data-ttu-id="638c2-118">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-118">30%</span></span>      |
| <span data-ttu-id="638c2-119">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-119">50 - 100</span></span>           | <span data-ttu-id="638c2-120">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-120">20%</span></span>      |
| <span data-ttu-id="638c2-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-122">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="638c2-123">最後の間隔の上限のゼロ (0) は、100 を超える金額がすべてこの間隔に含まれることを表します。</span><span class="sxs-lookup"><span data-stu-id="638c2-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="638c2-124">基準金額: **ラインごとの正味金額**</span><span class="sxs-lookup"><span data-stu-id="638c2-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="638c2-125">計算方法: **間隔**</span><span class="sxs-lookup"><span data-stu-id="638c2-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="638c2-126">1 つ 25.00 のランプを 8 つ購入します。</span><span class="sxs-lookup"><span data-stu-id="638c2-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="638c2-127">請求明細行の正味金額は 200.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="638c2-128">税の計算は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="638c2-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="638c2-129">売上税の合計 = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="638c2-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="638c2-130">請求金額の合計 = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="638c2-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="638c2-131">**バリエーション**</span><span class="sxs-lookup"><span data-stu-id="638c2-131">**Variation**</span></span> 

<span data-ttu-id="638c2-132">それぞれに 4 つの品目を含む 2 つの明細行がある請求書の場合、明細行ごとの正味金額が 100.00 になり、売上税の計算は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="638c2-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="638c2-133">明細行 1 の売上税 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="638c2-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="638c2-134">明細行 2 の売上税 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="638c2-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="638c2-135">売上税の合計 = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="638c2-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="638c2-136">請求金額の合計 = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="638c2-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="638c2-137">単位ごとの正味金額</span><span class="sxs-lookup"><span data-stu-id="638c2-137">Net amount per unit</span></span>
<span data-ttu-id="638c2-138">他のすべての税を除外した各単位の値に基づいて売上税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="638c2-139">単位に基づいている基準金額を選択した場合、単位も売上税コードに指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="638c2-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="638c2-140">例</span><span class="sxs-lookup"><span data-stu-id="638c2-140">Example</span></span>

<span data-ttu-id="638c2-141">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-142">金額</span><span class="sxs-lookup"><span data-stu-id="638c2-142">Amount</span></span>             | <span data-ttu-id="638c2-143">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="638c2-144">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-144">0 - 50</span></span>             | <span data-ttu-id="638c2-145">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-145">30%</span></span>      |
| <span data-ttu-id="638c2-146">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-146">50 - 100</span></span>           | <span data-ttu-id="638c2-147">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-147">20%</span></span>      |
| <span data-ttu-id="638c2-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-149">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-149">10%</span></span>      |

<span data-ttu-id="638c2-150">基準金額: **単位ごとの正味金額**</span><span class="sxs-lookup"><span data-stu-id="638c2-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="638c2-151">計算方法: **合計額**</span><span class="sxs-lookup"><span data-stu-id="638c2-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="638c2-152">1 つ 25.00 のランプを 8 つ購入します。</span><span class="sxs-lookup"><span data-stu-id="638c2-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="638c2-153">請求明細行の正味金額は 200.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="638c2-154">税は次のように計算されます: 単位ごとの売上税 = 25.00 x 30% = 7.50 売上の合計 = 7.50 x 8 単位 = 60.00 請求金額の合計 = 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="638c2-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="638c2-155">請求書残高の正味金額</span><span class="sxs-lookup"><span data-stu-id="638c2-155">Net amount of invoice balance</span></span>

<span data-ttu-id="638c2-156">他のすべての税を除外した請求書の合計値に基づいて売上税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="638c2-157">例</span><span class="sxs-lookup"><span data-stu-id="638c2-157">Example</span></span>

<span data-ttu-id="638c2-158">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-159">金額</span><span class="sxs-lookup"><span data-stu-id="638c2-159">Amount</span></span>            | <span data-ttu-id="638c2-160">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="638c2-161">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-161">0 - 50</span></span>            | <span data-ttu-id="638c2-162">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-162">30%</span></span>      |
| <span data-ttu-id="638c2-163">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-163">50 - 100</span></span>          | <span data-ttu-id="638c2-164">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-164">20%</span></span>      |
| <span data-ttu-id="638c2-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-166">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-166">10%</span></span>      |

<span data-ttu-id="638c2-167">基準金額: **請求書残高の正味金額**</span><span class="sxs-lookup"><span data-stu-id="638c2-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="638c2-168">計算方法: **間隔** 売上請求書には各行に 1 つ 25.00 の 4 つのランプを含む 2 つの明細行があります。</span><span class="sxs-lookup"><span data-stu-id="638c2-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="638c2-169">請求書残高の正味金額は 4 x 25.00 + 4 x 25.00 = 200.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="638c2-170">税は次のように計算されます: 売上税の合計 = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 請求金額の合計 = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="638c2-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="638c2-171">ラインごとの総額</span><span class="sxs-lookup"><span data-stu-id="638c2-171">Gross amount per line</span></span>

<span data-ttu-id="638c2-172">その明細行においては、その他のすべての税を含む明細行の値に基づいて売上税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="638c2-173">[基準金額] フィールドでこの値を選択できる売上税コードは売上税グループで 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="638c2-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="638c2-174">例</span><span class="sxs-lookup"><span data-stu-id="638c2-174">Example</span></span>

<span data-ttu-id="638c2-175">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-176">金額</span><span class="sxs-lookup"><span data-stu-id="638c2-176">Amount</span></span>             | <span data-ttu-id="638c2-177">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="638c2-178">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-178">0 - 50</span></span>             | <span data-ttu-id="638c2-179">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-179">30%</span></span>      |
| <span data-ttu-id="638c2-180">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-180">50 - 100</span></span>           | <span data-ttu-id="638c2-181">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-181">20%</span></span>      |
| <span data-ttu-id="638c2-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-183">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-183">10%</span></span>      |

<span data-ttu-id="638c2-184">基準金額: **ラインごとの総額** 計算方法: **間隔** また、それぞれ 5.00 のランプの特別税に対して計算された別のコードがあります。</span><span class="sxs-lookup"><span data-stu-id="638c2-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="638c2-185">この関税は、売上税が計算される前に正味金額に加算されます。</span><span class="sxs-lookup"><span data-stu-id="638c2-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="638c2-186">1 つ 25.00 のランプを 8 つ購入します。</span><span class="sxs-lookup"><span data-stu-id="638c2-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="638c2-187">請求明細行の正味金額は 200.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="638c2-188">請求明細行の総額は、8 x 25.00 + 8 x 5.00 = 240.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="638c2-189">税は次のように計算されます: 売上税の合計 = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 関税の合計 = 5.00 x 8 = 40.00請求金額の合計 = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="638c2-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="638c2-190">**バリエーション**</span><span class="sxs-lookup"><span data-stu-id="638c2-190">**Variation**</span></span> 

<span data-ttu-id="638c2-191">それぞれに 4 つの品目を含む 2 つの請求明細行を使用して請求書を作成すると、請求明細行ごとの正味金額が 100.00 になります。</span><span class="sxs-lookup"><span data-stu-id="638c2-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="638c2-192">請求明細行ごとの総額 (4 x 5.00 の関税を含む) が 120.00 になり、売上税は次のように作成されます: 請求明細行 1 の売上税 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 売上税の請求明細行 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 売上税の合計 = 27.00 + 27.00 = 54.00 関税の合計 = 5.00 x 8 = 40.00 請求金額の合計 = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="638c2-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="638c2-193">単位ごとの総額</span><span class="sxs-lookup"><span data-stu-id="638c2-193">Gross amount per unit</span></span>

<span data-ttu-id="638c2-194">他のすべての税を含む単位の値に基づいて売上税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="638c2-195">[基準金額] フィールドでこの値を選択できる売上税コードは売上税グループで 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="638c2-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="638c2-196">例</span><span class="sxs-lookup"><span data-stu-id="638c2-196">Example</span></span>

<span data-ttu-id="638c2-197">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-198">金額</span><span class="sxs-lookup"><span data-stu-id="638c2-198">Amount</span></span>             | <span data-ttu-id="638c2-199">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="638c2-200">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-200">0 - 50</span></span>             | <span data-ttu-id="638c2-201">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-201">30%</span></span>      |
| <span data-ttu-id="638c2-202">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-202">50 - 100</span></span>           | <span data-ttu-id="638c2-203">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-203">20%</span></span>      |
| <span data-ttu-id="638c2-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-205">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-205">10%</span></span>      |

<span data-ttu-id="638c2-206">基準金額: **単位ごとの総額** ランプにはそれぞれ 5.00 の特別税が課せられます。</span><span class="sxs-lookup"><span data-stu-id="638c2-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="638c2-207">この関税は、売上税が計算される前に正味金額に加算されます。</span><span class="sxs-lookup"><span data-stu-id="638c2-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="638c2-208">1 つ 25.00 のランプを 8 つ購入します。</span><span class="sxs-lookup"><span data-stu-id="638c2-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="638c2-209">単位ごとの総額は 30.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="638c2-210">税は次のように計算されます: 単位ごとの売上税 = 30 x 30% = 9.00 売上税の合計 = 9.00 x 8 = 72.00 関税の合計 = 5.00 x 8 = 40.00 合計請求金額 = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="638c2-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="638c2-211">請求合計には他の売上税金額が含まれています</span><span class="sxs-lookup"><span data-stu-id="638c2-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="638c2-212">他のすべての税を含む請求書の合計値に基づいて売上税率を決定する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="638c2-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="638c2-213">[基準金額] フィールドでこの値を選択できる売上税コードは売上税グループで 1 つだけです</span><span class="sxs-lookup"><span data-stu-id="638c2-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="638c2-214">例</span><span class="sxs-lookup"><span data-stu-id="638c2-214">Example</span></span>

<span data-ttu-id="638c2-215">売上税率が次の間隔で設定されています。</span><span class="sxs-lookup"><span data-stu-id="638c2-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="638c2-216">金額</span><span class="sxs-lookup"><span data-stu-id="638c2-216">Amount</span></span>             | <span data-ttu-id="638c2-217">税率</span><span class="sxs-lookup"><span data-stu-id="638c2-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="638c2-218">0 ～ 50</span><span class="sxs-lookup"><span data-stu-id="638c2-218">0 - 50</span></span>             | <span data-ttu-id="638c2-219">30%</span><span class="sxs-lookup"><span data-stu-id="638c2-219">30%</span></span>      |
| <span data-ttu-id="638c2-220">50 ～ 100</span><span class="sxs-lookup"><span data-stu-id="638c2-220">50 - 100</span></span>           | <span data-ttu-id="638c2-221">20%</span><span class="sxs-lookup"><span data-stu-id="638c2-221">20%</span></span>      |
| <span data-ttu-id="638c2-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="638c2-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="638c2-223">10%</span><span class="sxs-lookup"><span data-stu-id="638c2-223">10%</span></span>      |

<span data-ttu-id="638c2-224">基準金額: **その他の売上税金額を含む請求合計** 計算方法: **間隔** </span><span class="sxs-lookup"><span data-stu-id="638c2-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="638c2-225">ランプにはそれぞれ 5.00 の特別税が課せられます。</span><span class="sxs-lookup"><span data-stu-id="638c2-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="638c2-226">この関税は、売上税が計算される前に正味金額に加算されます。</span><span class="sxs-lookup"><span data-stu-id="638c2-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="638c2-227">1 つ 25.00 のランプを 8 つ購入します。</span><span class="sxs-lookup"><span data-stu-id="638c2-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="638c2-228">請求書の正味金額は 200.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="638c2-229">請求書の総額は、200.00 + (8 x 5.00) = 240.00 です。</span><span class="sxs-lookup"><span data-stu-id="638c2-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="638c2-230">税は次のように計算されます: 売上税の合計 = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 関税の合計 = 5.00 x 8 = 40.00請求金額の合計 = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="638c2-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="638c2-231">詳細については「[売上税コードの合計額と間隔計算オプション](whole-amount-interval-options-sales-tax-codes.md) および [発生元フィールドでの売上税計算方法](sales-tax-calculation-methods-origin-field.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="638c2-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



