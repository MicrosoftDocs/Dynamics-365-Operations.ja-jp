---
title: "連結会社の通貨再評価"
description: "このトピックでは、連結会社の通貨を再評価する方法について説明します。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="79b42-103">連結会社の通貨再評価</span><span class="sxs-lookup"><span data-stu-id="79b42-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="79b42-104">1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79b42-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="79b42-105">最初にデータを連結する場合、[**為替換算**] タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="79b42-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="79b42-106">新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79b42-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="79b42-107">未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。</span><span class="sxs-lookup"><span data-stu-id="79b42-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="79b42-108">次の例では、プロセス中に作成された勘定項目を示します。</span><span class="sxs-lookup"><span data-stu-id="79b42-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="79b42-109">会社設定</span><span class="sxs-lookup"><span data-stu-id="79b42-109">Company setup</span></span>
-   <span data-ttu-id="79b42-110">[**ソース / 営業会社 (USMF)**] – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="79b42-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="79b42-111">[**連結会社 (CON)**] – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="79b42-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="79b42-112">[**実現利益**] – 勘定科目 801500</span><span class="sxs-lookup"><span data-stu-id="79b42-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="79b42-113">[**実現損失**] – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="79b42-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="79b42-114">[**未実現利益**] – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="79b42-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="79b42-115">[**未実現損失**] – 勘定科目 801400</span><span class="sxs-lookup"><span data-stu-id="79b42-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="79b42-116">元のトランザクション</span><span class="sxs-lookup"><span data-stu-id="79b42-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="79b42-117">[USMF] の現金領収トランザクション</span><span class="sxs-lookup"><span data-stu-id="79b42-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="79b42-118">日</span><span class="sxs-lookup"><span data-stu-id="79b42-118">Date</span></span>       | <span data-ttu-id="79b42-119">勘定科目</span><span class="sxs-lookup"><span data-stu-id="79b42-119">Ledger account</span></span>               | <span data-ttu-id="79b42-120">通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-120">Currency</span></span> | <span data-ttu-id="79b42-121">金額</span><span class="sxs-lookup"><span data-stu-id="79b42-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="79b42-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="79b42-122">10/11/2015</span></span> | <span data-ttu-id="79b42-123">110110 – 現金</span><span class="sxs-lookup"><span data-stu-id="79b42-123">110110 – Cash</span></span>                | <span data-ttu-id="79b42-124">USD</span><span class="sxs-lookup"><span data-stu-id="79b42-124">USD</span></span>      | <span data-ttu-id="79b42-125">500</span><span class="sxs-lookup"><span data-stu-id="79b42-125">500</span></span>    |
| <span data-ttu-id="79b42-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="79b42-126">10/11/2015</span></span> | <span data-ttu-id="79b42-127">130100 – [売掛金勘定]</span><span class="sxs-lookup"><span data-stu-id="79b42-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="79b42-128">USD</span><span class="sxs-lookup"><span data-stu-id="79b42-128">USD</span></span>      | <span data-ttu-id="79b42-129">-500</span><span class="sxs-lookup"><span data-stu-id="79b42-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="79b42-130">為替レート</span><span class="sxs-lookup"><span data-stu-id="79b42-130">Exchange rates</span></span>
| <span data-ttu-id="79b42-131">開始通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-131">From currency</span></span> | <span data-ttu-id="79b42-132">終了通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-132">To currency</span></span> | <span data-ttu-id="79b42-133">開始日</span><span class="sxs-lookup"><span data-stu-id="79b42-133">Start date</span></span> | <span data-ttu-id="79b42-134">為替レート</span><span class="sxs-lookup"><span data-stu-id="79b42-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="79b42-135">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-135">EUR</span></span>           | <span data-ttu-id="79b42-136">USD</span><span class="sxs-lookup"><span data-stu-id="79b42-136">USD</span></span>         | <span data-ttu-id="79b42-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="79b42-137">10/1/2015</span></span>  | <span data-ttu-id="79b42-138">200</span><span class="sxs-lookup"><span data-stu-id="79b42-138">200</span></span>           |
| <span data-ttu-id="79b42-139">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-139">EUR</span></span>           | <span data-ttu-id="79b42-140">USD</span><span class="sxs-lookup"><span data-stu-id="79b42-140">USD</span></span>         | <span data-ttu-id="79b42-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="79b42-141">11/1/2015</span></span>  | <span data-ttu-id="79b42-142">150</span><span class="sxs-lookup"><span data-stu-id="79b42-142">150</span></span>           |
| <span data-ttu-id="79b42-143">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-143">EUR</span></span>           | <span data-ttu-id="79b42-144">USD</span><span class="sxs-lookup"><span data-stu-id="79b42-144">USD</span></span>         | <span data-ttu-id="79b42-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="79b42-145">12/1/2012</span></span>  | <span data-ttu-id="79b42-146">100</span><span class="sxs-lookup"><span data-stu-id="79b42-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="79b42-147">2015 年 10 月の連結を実行</span><span class="sxs-lookup"><span data-stu-id="79b42-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="79b42-148">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="79b42-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="79b42-149">勘定科目</span><span class="sxs-lookup"><span data-stu-id="79b42-149">Ledger account</span></span> | <span data-ttu-id="79b42-150">通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-150">Currency</span></span> | <span data-ttu-id="79b42-151">金額</span><span class="sxs-lookup"><span data-stu-id="79b42-151">Amount</span></span> | <span data-ttu-id="79b42-152">計算</span><span class="sxs-lookup"><span data-stu-id="79b42-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="79b42-153">110110</span><span class="sxs-lookup"><span data-stu-id="79b42-153">110110</span></span>         | <span data-ttu-id="79b42-154">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-154">EUR</span></span>      | <span data-ttu-id="79b42-155">250</span><span class="sxs-lookup"><span data-stu-id="79b42-155">250</span></span>    | <span data-ttu-id="79b42-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="79b42-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="79b42-157">130100</span><span class="sxs-lookup"><span data-stu-id="79b42-157">130100</span></span>         | <span data-ttu-id="79b42-158">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-158">EUR</span></span>      | <span data-ttu-id="79b42-159">-250</span><span class="sxs-lookup"><span data-stu-id="79b42-159">-250</span></span>   | <span data-ttu-id="79b42-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="79b42-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="79b42-161">2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="79b42-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="79b42-162">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="79b42-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="79b42-163">勘定科目</span><span class="sxs-lookup"><span data-stu-id="79b42-163">Ledger account</span></span> | <span data-ttu-id="79b42-164">通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-164">Currency</span></span> | <span data-ttu-id="79b42-165">金額</span><span class="sxs-lookup"><span data-stu-id="79b42-165">Amount</span></span>  | <span data-ttu-id="79b42-166">計算</span><span class="sxs-lookup"><span data-stu-id="79b42-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="79b42-167">110110</span><span class="sxs-lookup"><span data-stu-id="79b42-167">110110</span></span>         | <span data-ttu-id="79b42-168">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-168">EUR</span></span>      | <span data-ttu-id="79b42-169">333.33</span><span class="sxs-lookup"><span data-stu-id="79b42-169">333.33</span></span>  | <span data-ttu-id="79b42-170">元の金額 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="79b42-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="79b42-171">130100</span><span class="sxs-lookup"><span data-stu-id="79b42-171">130100</span></span>         | <span data-ttu-id="79b42-172">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-172">EUR</span></span>      | <span data-ttu-id="79b42-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="79b42-173">-333.33</span></span> | <span data-ttu-id="79b42-174">元の金額 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="79b42-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="79b42-175">801400</span><span class="sxs-lookup"><span data-stu-id="79b42-175">801400</span></span>         | <span data-ttu-id="79b42-176">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-176">EUR</span></span>      | <span data-ttu-id="79b42-177">83.33</span><span class="sxs-lookup"><span data-stu-id="79b42-177">83.33</span></span>   | <span data-ttu-id="79b42-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="79b42-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="79b42-179">801600</span><span class="sxs-lookup"><span data-stu-id="79b42-179">801600</span></span>         | <span data-ttu-id="79b42-180">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-180">EUR</span></span>      | <span data-ttu-id="79b42-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="79b42-181">-83.33</span></span>  | <span data-ttu-id="79b42-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="79b42-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="79b42-183">レポート通貨の金額に対する追加トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="79b42-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="79b42-184">2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="79b42-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="79b42-185">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="79b42-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="79b42-186">勘定科目</span><span class="sxs-lookup"><span data-stu-id="79b42-186">Ledger account</span></span> | <span data-ttu-id="79b42-187">通貨</span><span class="sxs-lookup"><span data-stu-id="79b42-187">Currency</span></span> | <span data-ttu-id="79b42-188">金額</span><span class="sxs-lookup"><span data-stu-id="79b42-188">Amount</span></span>  | <span data-ttu-id="79b42-189">計算</span><span class="sxs-lookup"><span data-stu-id="79b42-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="79b42-190">110110</span><span class="sxs-lookup"><span data-stu-id="79b42-190">110110</span></span>         | <span data-ttu-id="79b42-191">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-191">EUR</span></span>      | <span data-ttu-id="79b42-192">500.00</span><span class="sxs-lookup"><span data-stu-id="79b42-192">500.00</span></span>  | <span data-ttu-id="79b42-193">元の金額 500 × 1</span><span class="sxs-lookup"><span data-stu-id="79b42-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="79b42-194">130100</span><span class="sxs-lookup"><span data-stu-id="79b42-194">130100</span></span>         | <span data-ttu-id="79b42-195">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-195">EUR</span></span>      | <span data-ttu-id="79b42-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="79b42-196">-500.00</span></span> | <span data-ttu-id="79b42-197">元の金額 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="79b42-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="79b42-198">801400</span><span class="sxs-lookup"><span data-stu-id="79b42-198">801400</span></span>         | <span data-ttu-id="79b42-199">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-199">EUR</span></span>      | <span data-ttu-id="79b42-200">250</span><span class="sxs-lookup"><span data-stu-id="79b42-200">250</span></span>     | <span data-ttu-id="79b42-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="79b42-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="79b42-202">801600</span><span class="sxs-lookup"><span data-stu-id="79b42-202">801600</span></span>         | <span data-ttu-id="79b42-203">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="79b42-203">EUR</span></span>      | <span data-ttu-id="79b42-204">-250</span><span class="sxs-lookup"><span data-stu-id="79b42-204">-250</span></span>    | <span data-ttu-id="79b42-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="79b42-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






