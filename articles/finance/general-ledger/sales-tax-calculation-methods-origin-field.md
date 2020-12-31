---
title: '[発生元] フィールドでの売上税計算方法'
description: この記事は、[売上税コードの値] ページの [発生元] フィールドのオプション、および売上税が選択された売上税コードのオプションに基づいて計算される方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0eb3671051d9a3be9430050e2a0ad4227b17677e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445195"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="a312b-103">[発生元] フィールドでの売上税計算方法</span><span class="sxs-lookup"><span data-stu-id="a312b-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a312b-104">この記事は、[売上税コードの値] ページの [発生元] フィールドのオプション、および売上税が選択された売上税コードのオプションに基づいて計算される方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a312b-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="a312b-105">[売上税コード] ページで作成する売上税コードごとに、税基準額に適用する計算方法を [発生元] フィールドで選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a312b-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="a312b-106">正味金額の割合</span><span class="sxs-lookup"><span data-stu-id="a312b-106">Percentage of net amount</span></span>
<span data-ttu-id="a312b-107">[正味金額の割合] の計算方法は、[発生元] フィールドの既定値です。</span><span class="sxs-lookup"><span data-stu-id="a312b-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="a312b-108">売上税は、購入金額または売上金額の割合として計算され、その他の売上税はすべて除外されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="a312b-109">例</span><span class="sxs-lookup"><span data-stu-id="a312b-109">Example</span></span>

<span data-ttu-id="a312b-110">税率は 25% です。</span><span class="sxs-lookup"><span data-stu-id="a312b-110">The tax rate is 25%.</span></span> <span data-ttu-id="a312b-111">請求明細行に、単価 1.00 ドルの品目の数量が 10 と示されています。顧客には 10% の行割引が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="a312b-112">正味金額: (10 \* 1.00) - 10% = 9.00。売上税: 9.00 \* 25% = 2.25。合計金額: 9.00 + 2.25 = 11.25。</span><span class="sxs-lookup"><span data-stu-id="a312b-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="a312b-113">総額の割合</span><span class="sxs-lookup"><span data-stu-id="a312b-113">Percentage of gross amount</span></span>
<span data-ttu-id="a312b-114">[総額の割合] の方法を選択すると、売上税は、総売上金額の割合として計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="a312b-115">総額は、明細行正味金額に、明細行についてすべての税および手数料を、[発生元] = [総額の割合] となる税を除外して、足したものです。</span><span class="sxs-lookup"><span data-stu-id="a312b-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="a312b-116">例</span><span class="sxs-lookup"><span data-stu-id="a312b-116">Example</span></span>

<span data-ttu-id="a312b-117">税務当局から、ある品目に特別税が課せられました。</span><span class="sxs-lookup"><span data-stu-id="a312b-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="a312b-118">関税額は、売上税が計算される前に正味金額に加算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="a312b-119">次の売上税コードの場合:</span><span class="sxs-lookup"><span data-stu-id="a312b-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="a312b-120">DUTY 1 = 10%、[正味金額の割合] の計算方法を使用</span><span class="sxs-lookup"><span data-stu-id="a312b-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="a312b-121">DUTY 2 = 20%、[正味金額の割合] の計算方法を使用</span><span class="sxs-lookup"><span data-stu-id="a312b-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="a312b-122">SALESTAX = 25%、[総額の割合] の計算方法を使用</span><span class="sxs-lookup"><span data-stu-id="a312b-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="a312b-123">正味金額が 10.00 の場合は、DUTY 1 は 1.00 (10.00 \* 10%)で、DUTY 2 は 2.00 (10.00 \* 20%) です。</span><span class="sxs-lookup"><span data-stu-id="a312b-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="a312b-124">金額は次のとおりです: 総額: 正味金額 + DUTY 1 の金額 + DUTY 2 の金額 (10.00 + 1.00 + 2.00) = 13.00。SALESTAX = 13.00 \* 25% = 3.25。DUTIES と SALESTAXの合計: 1.00 + 2.00 + 3.25 = 6.25。合計金額: 10.00 + 6.25 = 16.25。</span><span class="sxs-lookup"><span data-stu-id="a312b-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="a312b-125">**メモ**</span><span class="sxs-lookup"><span data-stu-id="a312b-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a312b-126">[発生元] = [総額の割合] となっている税コードのみがトランザクションに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a312b-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="a312b-127">このような税コードがトランザクションに複数ある場合は、売上税が計算できないというエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="a312b-128">消費税率</span><span class="sxs-lookup"><span data-stu-id="a312b-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="a312b-129">[発生元] フィールドで [売上税の割合] を選択すると、[売上税の売上税] フィールドで選択されている売上税の割合として売上税が計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="a312b-130">[売上税の売上税] フィールドで選択した売上税が最初に計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="a312b-131">2 番目の売上税は、この最初の売上税額に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="a312b-132">例</span><span class="sxs-lookup"><span data-stu-id="a312b-132">Example</span></span>

<span data-ttu-id="a312b-133">次の売上税コードの場合:</span><span class="sxs-lookup"><span data-stu-id="a312b-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="a312b-134">DUTY 1 = 10%、[正味金額の割合] の方法を使用</span><span class="sxs-lookup"><span data-stu-id="a312b-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="a312b-135">DUTY 2 = 20%、[売上税率] の方法を使用、かつ [売上税の売上税] フィールドで Duty 1 を選択</span><span class="sxs-lookup"><span data-stu-id="a312b-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="a312b-136">SALESTAX = 25%、[総額の割合] の方法を使用</span><span class="sxs-lookup"><span data-stu-id="a312b-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="a312b-137">正味金額: 10.00。DUTY 1: 10.00 \* 10% = 1.00。DUTY 2: 1.00 \* 20% = 0.20。総額: 10.00 + 1.00 + 0.20 = 11.20。SALESTAX: 11.20 \* 25% = 2.80。DUTIES と SALESTAXの合計: 1.00 + 0.20 + 2.80 = 4.00。合計金額: 10.00 + 4.00 = 14.00。</span><span class="sxs-lookup"><span data-stu-id="a312b-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="a312b-138">**メモ**</span><span class="sxs-lookup"><span data-stu-id="a312b-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a312b-139">税の計算で複数レベルの税は使用できません。</span><span class="sxs-lookup"><span data-stu-id="a312b-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="a312b-140">税は、 既に別の税に基づいて計算されている税に基づいて計算することはできません。</span><span class="sxs-lookup"><span data-stu-id="a312b-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="a312b-141">税コードが単一レベルの複数の税は、トランザクションにおいて計算できます。</span><span class="sxs-lookup"><span data-stu-id="a312b-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="a312b-142">単位ごとの金額</span><span class="sxs-lookup"><span data-stu-id="a312b-142">Amount per unit</span></span>
<span data-ttu-id="a312b-143">[発生元] フィールドで [単位ごとの金額] を選択すると、売上税はドキュメント明細行で入力する数量で乗算する単位ごとの固定金額として計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="a312b-144">単位は [単位] フィールドで選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a312b-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="a312b-145">単位ごとの金額は、[売上税コードの値] ページで指定します。</span><span class="sxs-lookup"><span data-stu-id="a312b-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="a312b-146">例</span><span class="sxs-lookup"><span data-stu-id="a312b-146">Example</span></span>

<span data-ttu-id="a312b-147">売上税コードは次のように設定されます: 単位ごとに USD 1.20 = 箱。売上請求書明細行で 25 箱の品目が販売された。売上税は 25 \* 1.20 = 30.00 と計算。</span><span class="sxs-lookup"><span data-stu-id="a312b-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="a312b-148">**メモ**</span><span class="sxs-lookup"><span data-stu-id="a312b-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a312b-149">トランザクションが売上税コードで指定された単位とは別の単位で入力される場合、[単位換算] ページで設定された単位換算に基づいて自動的に換算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="a312b-150">単位ごとの金額の追加オプション</span><span class="sxs-lookup"><span data-stu-id="a312b-150">Amount per unit, additional option</span></span>

<span data-ttu-id="a312b-151">[計算] タブでは、単位ごとの金額で計算される税が他の税コードより前に計算され、[発生元] = [正味金額の割合] となっている他の税コードが計算される前に正味金額に加算されるかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a312b-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="a312b-152">例</span><span class="sxs-lookup"><span data-stu-id="a312b-152">Examples</span></span>

<span data-ttu-id="a312b-153">あるトランザクションで、2 つの税コードを計算するとします。</span><span class="sxs-lookup"><span data-stu-id="a312b-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="a312b-154">DUTY: [発生元] = [単位ごとの金額] と売上税で、単位あたり 5.00 = 個の値に設定</span><span class="sxs-lookup"><span data-stu-id="a312b-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="a312b-155">SALESTAX: [発生元] = 次の例の通りで、値は 25% に設定</span><span class="sxs-lookup"><span data-stu-id="a312b-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="a312b-156">品目 1 個を単価 10.00 で販売</span><span class="sxs-lookup"><span data-stu-id="a312b-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="a312b-157">例 1</span><span class="sxs-lookup"><span data-stu-id="a312b-157">Example 1</span></span>

<span data-ttu-id="a312b-158">SALESTAX: [発生元] = [総額の割合] の方法。SALESTAX は総額の割合として計算されるため、[売上税の前に計算] オプションは効果がない。</span><span class="sxs-lookup"><span data-stu-id="a312b-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="a312b-159">DUTY: 1 \* 5.00 = 5.00。総額: 10.00 + 5.00 = 15.00。SALESTAX: 15.00 \* 25% = 3.75。売上税の合計: 5.00 + 3.75 = 8.75。合計金額: 10.00 + 8.75 = 18.75。</span><span class="sxs-lookup"><span data-stu-id="a312b-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="a312b-160">例 2</span><span class="sxs-lookup"><span data-stu-id="a312b-160">Example 2</span></span>

<span data-ttu-id="a312b-161">SALESTAX: [発生元] = [正味金額の割合]。[売上税の前に計算] オプションは DUTY 計算に選択されていない。</span><span class="sxs-lookup"><span data-stu-id="a312b-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="a312b-162">正味金額: 10.00。DUTY: 1 \* 5.00 = 5.00。SALESTAX: 10.00 \* 25% = 2.50。売上税の合計: 5.00 + 2.50 = 7.50。合計金額: 10.00 + 7.50 = 17.50。</span><span class="sxs-lookup"><span data-stu-id="a312b-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="a312b-163">例 3</span><span class="sxs-lookup"><span data-stu-id="a312b-163">Example 3</span></span>

<span data-ttu-id="a312b-164">SALESTAX: [発生元] = [正味金額の割合]。[売上税の前に計算] オプションは DUTY 計算に選択されている。</span><span class="sxs-lookup"><span data-stu-id="a312b-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="a312b-165">正味金額: 10.00。DUTY: 1 \* 5.00 = 5.00。SALESTAX: (10.00 + 5.00) \* 25% = 3.75。売上税の合計: 5.00 + 3.75 = 8.75。合計金額: 10.00 + 8.75 = 18.75。</span><span class="sxs-lookup"><span data-stu-id="a312b-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="a312b-166">例 4</span><span class="sxs-lookup"><span data-stu-id="a312b-166">Example 4</span></span>

<span data-ttu-id="a312b-167">関税が 1 種類しかないため、例 3 と例 1 の結果は同じになります。</span><span class="sxs-lookup"><span data-stu-id="a312b-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="a312b-168">2 つの DUTIES があり、売上税計算で正味金額にはそれらの 1 のみが含まれるとします。DUTY 1: 5.00、[単位ごとの金額] の方法を使用、[売上税の前に計算] オプションがオン。DUTY 2: 2.50、[単位ごとの金額] の方法を使用、[売上税の前に計算] オプションはオフ。売上税: 25%、[正味金額の割合] の方法を使用。賞味金額: 10.00。DUTY 1: 1 \* 5.00 = 5.00。DUTY 2: 1 \* 2.50 = 2.50。売上税の対象となる正味金額: 10.00 + 5.00 = 15.00。SALESTAX: 15.00 \* 25% = 3.75。関税を含めた売上税の合計: 5.00 + 2.50 + 3.75 = 11.25。合計金額: 10.00 + 11.25 = 21.25。25% のSALESTAX は、賞味金額 (10.00) + DUTY 1 (5.00) = 15.00 の合計として計算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="a312b-169">DUTY 2 は、売上税が計算された後の税額に加算されます。</span><span class="sxs-lookup"><span data-stu-id="a312b-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="a312b-170">計算済正味金額の割合</span><span class="sxs-lookup"><span data-stu-id="a312b-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="a312b-171">[計算済正味金額の割合] は、文書または仕訳帳での [金額に売上税を含める] パラメーターの設定により、異なる税の計算を行います。</span><span class="sxs-lookup"><span data-stu-id="a312b-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="a312b-172">例 1</span><span class="sxs-lookup"><span data-stu-id="a312b-172">Example 1</span></span>

<span data-ttu-id="a312b-173">文書や仕訳帳での [金額に売上税を含める] = [はい]。トランザクション明細行の金額: 10.00。税率: 25%。売上税: トランザクション明細行の金額 \* 税率 (10.00 \* 25%) = 2.50。税基準額 (発生元の金額): トランザクション明細行の金額 -売上税 (10.00 - 2.50) = 7.50。</span><span class="sxs-lookup"><span data-stu-id="a312b-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="a312b-174">例 2</span><span class="sxs-lookup"><span data-stu-id="a312b-174">Example 2</span></span>

<span data-ttu-id="a312b-175">文書や仕訳帳での [金額に売上税を含める] = [いいえ]。トランザクション明細行の金額: 10.00。税率: 25%。売上税: (トランザクション明細行の金額 \* 税率) / (100 - 税率) (10.00 \* 25%) / (100% - 25%) = 3.33。税基準額 (発生元の金額): トランザクション明細行の金額 = 10.00。</span><span class="sxs-lookup"><span data-stu-id="a312b-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="a312b-176">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a312b-176">Additional resources</span></span>
--------

[<span data-ttu-id="a312b-177">基準金額および計算方法に基づいた、売上税の税率</span><span class="sxs-lookup"><span data-stu-id="a312b-177">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)

[<span data-ttu-id="a312b-178">消費税コードの合計額と間隔計算オプション</span><span class="sxs-lookup"><span data-stu-id="a312b-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



