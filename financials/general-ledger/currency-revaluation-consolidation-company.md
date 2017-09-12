---
title: "連結会社の通貨再評価"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="00073-102">連結会社の通貨再評価</span><span class="sxs-lookup"><span data-stu-id="00073-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="00073-103">1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00073-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="00073-104">最初にデータを連結する場合、[**為替換算**] タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="00073-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="00073-105">新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00073-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="00073-106">未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。</span><span class="sxs-lookup"><span data-stu-id="00073-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="00073-107">次の例では、プロセス中に作成された勘定項目を示します。</span><span class="sxs-lookup"><span data-stu-id="00073-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="00073-108">会社設定</span><span class="sxs-lookup"><span data-stu-id="00073-108">Company setup</span></span>
-   <span data-ttu-id="00073-109">[**ソース / 営業会社 (USMF)**] – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="00073-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="00073-110">[**連結会社 (CON)**] – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="00073-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="00073-111">[**実現利益**] – 勘定科目 801500</span><span class="sxs-lookup"><span data-stu-id="00073-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="00073-112">[**実現損失**] – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="00073-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="00073-113">[**未実現利益**] – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="00073-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="00073-114">[**未実現損失**] – 勘定科目 801400</span><span class="sxs-lookup"><span data-stu-id="00073-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="00073-115">元のトランザクション</span><span class="sxs-lookup"><span data-stu-id="00073-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="00073-116">[USMF] の現金領収トランザクション</span><span class="sxs-lookup"><span data-stu-id="00073-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="00073-117">日</span><span class="sxs-lookup"><span data-stu-id="00073-117">Date</span></span>       | <span data-ttu-id="00073-118">勘定科目</span><span class="sxs-lookup"><span data-stu-id="00073-118">Ledger account</span></span>               | <span data-ttu-id="00073-119">通貨</span><span class="sxs-lookup"><span data-stu-id="00073-119">Currency</span></span> | <span data-ttu-id="00073-120">金額</span><span class="sxs-lookup"><span data-stu-id="00073-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="00073-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="00073-121">10/11/2015</span></span> | <span data-ttu-id="00073-122">110110 – 現金</span><span class="sxs-lookup"><span data-stu-id="00073-122">110110 – Cash</span></span>                | <span data-ttu-id="00073-123">USD</span><span class="sxs-lookup"><span data-stu-id="00073-123">USD</span></span>      | <span data-ttu-id="00073-124">500</span><span class="sxs-lookup"><span data-stu-id="00073-124">500</span></span>    |
| <span data-ttu-id="00073-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="00073-125">10/11/2015</span></span> | <span data-ttu-id="00073-126">130100 – [売掛金勘定]</span><span class="sxs-lookup"><span data-stu-id="00073-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="00073-127">USD</span><span class="sxs-lookup"><span data-stu-id="00073-127">USD</span></span>      | <span data-ttu-id="00073-128">-500</span><span class="sxs-lookup"><span data-stu-id="00073-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="00073-129">為替レート</span><span class="sxs-lookup"><span data-stu-id="00073-129">Exchange rates</span></span>
| <span data-ttu-id="00073-130">開始通貨</span><span class="sxs-lookup"><span data-stu-id="00073-130">From currency</span></span> | <span data-ttu-id="00073-131">終了通貨</span><span class="sxs-lookup"><span data-stu-id="00073-131">To currency</span></span> | <span data-ttu-id="00073-132">開始日</span><span class="sxs-lookup"><span data-stu-id="00073-132">Start date</span></span> | <span data-ttu-id="00073-133">為替レート</span><span class="sxs-lookup"><span data-stu-id="00073-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="00073-134">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-134">EUR</span></span>           | <span data-ttu-id="00073-135">USD</span><span class="sxs-lookup"><span data-stu-id="00073-135">USD</span></span>         | <span data-ttu-id="00073-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="00073-136">10/1/2015</span></span>  | <span data-ttu-id="00073-137">200</span><span class="sxs-lookup"><span data-stu-id="00073-137">200</span></span>           |
| <span data-ttu-id="00073-138">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-138">EUR</span></span>           | <span data-ttu-id="00073-139">USD</span><span class="sxs-lookup"><span data-stu-id="00073-139">USD</span></span>         | <span data-ttu-id="00073-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="00073-140">11/1/2015</span></span>  | <span data-ttu-id="00073-141">150</span><span class="sxs-lookup"><span data-stu-id="00073-141">150</span></span>           |
| <span data-ttu-id="00073-142">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-142">EUR</span></span>           | <span data-ttu-id="00073-143">USD</span><span class="sxs-lookup"><span data-stu-id="00073-143">USD</span></span>         | <span data-ttu-id="00073-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="00073-144">12/1/2012</span></span>  | <span data-ttu-id="00073-145">100</span><span class="sxs-lookup"><span data-stu-id="00073-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="00073-146">2015 年 10 月の連結を実行</span><span class="sxs-lookup"><span data-stu-id="00073-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="00073-147">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="00073-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="00073-148">勘定科目</span><span class="sxs-lookup"><span data-stu-id="00073-148">Ledger account</span></span> | <span data-ttu-id="00073-149">通貨</span><span class="sxs-lookup"><span data-stu-id="00073-149">Currency</span></span> | <span data-ttu-id="00073-150">金額</span><span class="sxs-lookup"><span data-stu-id="00073-150">Amount</span></span> | <span data-ttu-id="00073-151">計算</span><span class="sxs-lookup"><span data-stu-id="00073-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="00073-152">110110</span><span class="sxs-lookup"><span data-stu-id="00073-152">110110</span></span>         | <span data-ttu-id="00073-153">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-153">EUR</span></span>      | <span data-ttu-id="00073-154">250</span><span class="sxs-lookup"><span data-stu-id="00073-154">250</span></span>    | <span data-ttu-id="00073-155">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="00073-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="00073-156">130100</span><span class="sxs-lookup"><span data-stu-id="00073-156">130100</span></span>         | <span data-ttu-id="00073-157">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-157">EUR</span></span>      | <span data-ttu-id="00073-158">-250</span><span class="sxs-lookup"><span data-stu-id="00073-158">-250</span></span>   | <span data-ttu-id="00073-159">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="00073-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="00073-160">2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="00073-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="00073-161">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="00073-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="00073-162">勘定科目</span><span class="sxs-lookup"><span data-stu-id="00073-162">Ledger account</span></span> | <span data-ttu-id="00073-163">通貨</span><span class="sxs-lookup"><span data-stu-id="00073-163">Currency</span></span> | <span data-ttu-id="00073-164">金額</span><span class="sxs-lookup"><span data-stu-id="00073-164">Amount</span></span>  | <span data-ttu-id="00073-165">計算</span><span class="sxs-lookup"><span data-stu-id="00073-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="00073-166">110110</span><span class="sxs-lookup"><span data-stu-id="00073-166">110110</span></span>         | <span data-ttu-id="00073-167">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-167">EUR</span></span>      | <span data-ttu-id="00073-168">333.33</span><span class="sxs-lookup"><span data-stu-id="00073-168">333.33</span></span>  | <span data-ttu-id="00073-169">元の金額 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="00073-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="00073-170">130100</span><span class="sxs-lookup"><span data-stu-id="00073-170">130100</span></span>         | <span data-ttu-id="00073-171">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-171">EUR</span></span>      | <span data-ttu-id="00073-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="00073-172">-333.33</span></span> | <span data-ttu-id="00073-173">元の金額 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="00073-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="00073-174">801400</span><span class="sxs-lookup"><span data-stu-id="00073-174">801400</span></span>         | <span data-ttu-id="00073-175">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-175">EUR</span></span>      | <span data-ttu-id="00073-176">83.33</span><span class="sxs-lookup"><span data-stu-id="00073-176">83.33</span></span>   | <span data-ttu-id="00073-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="00073-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="00073-178">801600</span><span class="sxs-lookup"><span data-stu-id="00073-178">801600</span></span>         | <span data-ttu-id="00073-179">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-179">EUR</span></span>      | <span data-ttu-id="00073-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="00073-180">-83.33</span></span>  | <span data-ttu-id="00073-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="00073-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="00073-182">レポート通貨の金額に対する追加トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00073-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="00073-183">2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="00073-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="00073-184">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="00073-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="00073-185">勘定科目</span><span class="sxs-lookup"><span data-stu-id="00073-185">Ledger account</span></span> | <span data-ttu-id="00073-186">通貨</span><span class="sxs-lookup"><span data-stu-id="00073-186">Currency</span></span> | <span data-ttu-id="00073-187">金額</span><span class="sxs-lookup"><span data-stu-id="00073-187">Amount</span></span>  | <span data-ttu-id="00073-188">計算</span><span class="sxs-lookup"><span data-stu-id="00073-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="00073-189">110110</span><span class="sxs-lookup"><span data-stu-id="00073-189">110110</span></span>         | <span data-ttu-id="00073-190">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-190">EUR</span></span>      | <span data-ttu-id="00073-191">500.00</span><span class="sxs-lookup"><span data-stu-id="00073-191">500.00</span></span>  | <span data-ttu-id="00073-192">元の金額 500 × 1</span><span class="sxs-lookup"><span data-stu-id="00073-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="00073-193">130100</span><span class="sxs-lookup"><span data-stu-id="00073-193">130100</span></span>         | <span data-ttu-id="00073-194">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-194">EUR</span></span>      | <span data-ttu-id="00073-195">-500.00</span><span class="sxs-lookup"><span data-stu-id="00073-195">-500.00</span></span> | <span data-ttu-id="00073-196">元の金額 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="00073-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="00073-197">801400</span><span class="sxs-lookup"><span data-stu-id="00073-197">801400</span></span>         | <span data-ttu-id="00073-198">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-198">EUR</span></span>      | <span data-ttu-id="00073-199">250</span><span class="sxs-lookup"><span data-stu-id="00073-199">250</span></span>     | <span data-ttu-id="00073-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="00073-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="00073-201">801600</span><span class="sxs-lookup"><span data-stu-id="00073-201">801600</span></span>         | <span data-ttu-id="00073-202">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="00073-202">EUR</span></span>      | <span data-ttu-id="00073-203">-250</span><span class="sxs-lookup"><span data-stu-id="00073-203">-250</span></span>    | <span data-ttu-id="00073-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="00073-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






