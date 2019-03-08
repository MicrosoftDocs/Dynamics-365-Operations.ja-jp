---
title: 連結会社の通貨再評価
description: このトピックでは、連結会社の通貨を再評価する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "338754"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="af276-103">連結会社の通貨再評価</span><span class="sxs-lookup"><span data-stu-id="af276-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af276-104">1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af276-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="af276-105">最初にデータを連結する場合、**為替換算**タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="af276-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="af276-106">新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af276-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="af276-107">未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。</span><span class="sxs-lookup"><span data-stu-id="af276-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="af276-108">次の例では、プロセス中に作成された勘定項目を示します。</span><span class="sxs-lookup"><span data-stu-id="af276-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="af276-109">会社設定</span><span class="sxs-lookup"><span data-stu-id="af276-109">Company setup</span></span>
-   <span data-ttu-id="af276-110">**ソース / 営業会社 (USMF)** – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="af276-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="af276-111">**連結会社 (CON)** – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="af276-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="af276-112">**実現利益** – 勘定科目 801500</span><span class="sxs-lookup"><span data-stu-id="af276-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="af276-113">**実現損失** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="af276-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="af276-114">**未実現利益** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="af276-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="af276-115">**未実現損失** – 勘定科目 801400</span><span class="sxs-lookup"><span data-stu-id="af276-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="af276-116">元のトランザクション</span><span class="sxs-lookup"><span data-stu-id="af276-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="af276-117">[USMF] の現金領収トランザクション</span><span class="sxs-lookup"><span data-stu-id="af276-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="af276-118">日</span><span class="sxs-lookup"><span data-stu-id="af276-118">Date</span></span>       | <span data-ttu-id="af276-119">勘定科目</span><span class="sxs-lookup"><span data-stu-id="af276-119">Ledger account</span></span>               | <span data-ttu-id="af276-120">通貨</span><span class="sxs-lookup"><span data-stu-id="af276-120">Currency</span></span> | <span data-ttu-id="af276-121">金額</span><span class="sxs-lookup"><span data-stu-id="af276-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="af276-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="af276-122">10/11/2015</span></span> | <span data-ttu-id="af276-123">110110 – 現金</span><span class="sxs-lookup"><span data-stu-id="af276-123">110110 – Cash</span></span>                | <span data-ttu-id="af276-124">USD</span><span class="sxs-lookup"><span data-stu-id="af276-124">USD</span></span>      | <span data-ttu-id="af276-125">500</span><span class="sxs-lookup"><span data-stu-id="af276-125">500</span></span>    |
| <span data-ttu-id="af276-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="af276-126">10/11/2015</span></span> | <span data-ttu-id="af276-127">130100 – [売掛金勘定]</span><span class="sxs-lookup"><span data-stu-id="af276-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="af276-128">USD</span><span class="sxs-lookup"><span data-stu-id="af276-128">USD</span></span>      | <span data-ttu-id="af276-129">-500</span><span class="sxs-lookup"><span data-stu-id="af276-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="af276-130">為替レート</span><span class="sxs-lookup"><span data-stu-id="af276-130">Exchange rates</span></span>

| <span data-ttu-id="af276-131">開始通貨</span><span class="sxs-lookup"><span data-stu-id="af276-131">From currency</span></span> | <span data-ttu-id="af276-132">終了通貨</span><span class="sxs-lookup"><span data-stu-id="af276-132">To currency</span></span> | <span data-ttu-id="af276-133">開始日</span><span class="sxs-lookup"><span data-stu-id="af276-133">Start date</span></span> | <span data-ttu-id="af276-134">為替レート</span><span class="sxs-lookup"><span data-stu-id="af276-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="af276-135">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-135">EUR</span></span>           | <span data-ttu-id="af276-136">USD</span><span class="sxs-lookup"><span data-stu-id="af276-136">USD</span></span>         | <span data-ttu-id="af276-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="af276-137">10/1/2015</span></span>  | <span data-ttu-id="af276-138">200</span><span class="sxs-lookup"><span data-stu-id="af276-138">200</span></span>           |
| <span data-ttu-id="af276-139">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-139">EUR</span></span>           | <span data-ttu-id="af276-140">USD</span><span class="sxs-lookup"><span data-stu-id="af276-140">USD</span></span>         | <span data-ttu-id="af276-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="af276-141">11/1/2015</span></span>  | <span data-ttu-id="af276-142">150</span><span class="sxs-lookup"><span data-stu-id="af276-142">150</span></span>           |
| <span data-ttu-id="af276-143">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-143">EUR</span></span>           | <span data-ttu-id="af276-144">USD</span><span class="sxs-lookup"><span data-stu-id="af276-144">USD</span></span>         | <span data-ttu-id="af276-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="af276-145">12/1/2012</span></span>  | <span data-ttu-id="af276-146">100</span><span class="sxs-lookup"><span data-stu-id="af276-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="af276-147">2015 年 10 月の連結を実行</span><span class="sxs-lookup"><span data-stu-id="af276-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="af276-148">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="af276-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="af276-149">勘定科目</span><span class="sxs-lookup"><span data-stu-id="af276-149">Ledger account</span></span> | <span data-ttu-id="af276-150">通貨</span><span class="sxs-lookup"><span data-stu-id="af276-150">Currency</span></span> | <span data-ttu-id="af276-151">金額</span><span class="sxs-lookup"><span data-stu-id="af276-151">Amount</span></span> | <span data-ttu-id="af276-152">計算</span><span class="sxs-lookup"><span data-stu-id="af276-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="af276-153">110110</span><span class="sxs-lookup"><span data-stu-id="af276-153">110110</span></span>         | <span data-ttu-id="af276-154">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-154">EUR</span></span>      | <span data-ttu-id="af276-155">250</span><span class="sxs-lookup"><span data-stu-id="af276-155">250</span></span>    | <span data-ttu-id="af276-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="af276-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="af276-157">130100</span><span class="sxs-lookup"><span data-stu-id="af276-157">130100</span></span>         | <span data-ttu-id="af276-158">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-158">EUR</span></span>      | <span data-ttu-id="af276-159">-250</span><span class="sxs-lookup"><span data-stu-id="af276-159">-250</span></span>   | <span data-ttu-id="af276-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="af276-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="af276-161">2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="af276-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="af276-162">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="af276-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="af276-163">勘定科目</span><span class="sxs-lookup"><span data-stu-id="af276-163">Ledger account</span></span> | <span data-ttu-id="af276-164">通貨</span><span class="sxs-lookup"><span data-stu-id="af276-164">Currency</span></span> | <span data-ttu-id="af276-165">金額</span><span class="sxs-lookup"><span data-stu-id="af276-165">Amount</span></span>  | <span data-ttu-id="af276-166">計算</span><span class="sxs-lookup"><span data-stu-id="af276-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="af276-167">110110</span><span class="sxs-lookup"><span data-stu-id="af276-167">110110</span></span>         | <span data-ttu-id="af276-168">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-168">EUR</span></span>      | <span data-ttu-id="af276-169">333.33</span><span class="sxs-lookup"><span data-stu-id="af276-169">333.33</span></span>  | <span data-ttu-id="af276-170">元の金額 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="af276-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="af276-171">130100</span><span class="sxs-lookup"><span data-stu-id="af276-171">130100</span></span>         | <span data-ttu-id="af276-172">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-172">EUR</span></span>      | <span data-ttu-id="af276-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="af276-173">-333.33</span></span> | <span data-ttu-id="af276-174">元の金額 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="af276-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="af276-175">801400</span><span class="sxs-lookup"><span data-stu-id="af276-175">801400</span></span>         | <span data-ttu-id="af276-176">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-176">EUR</span></span>      | <span data-ttu-id="af276-177">83.33</span><span class="sxs-lookup"><span data-stu-id="af276-177">83.33</span></span>   | <span data-ttu-id="af276-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="af276-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="af276-179">801600</span><span class="sxs-lookup"><span data-stu-id="af276-179">801600</span></span>         | <span data-ttu-id="af276-180">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-180">EUR</span></span>      | <span data-ttu-id="af276-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="af276-181">-83.33</span></span>  | <span data-ttu-id="af276-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="af276-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="af276-183">レポート通貨の金額に対する追加トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="af276-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="af276-184">2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="af276-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="af276-185">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="af276-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="af276-186">勘定科目</span><span class="sxs-lookup"><span data-stu-id="af276-186">Ledger account</span></span> | <span data-ttu-id="af276-187">通貨</span><span class="sxs-lookup"><span data-stu-id="af276-187">Currency</span></span> | <span data-ttu-id="af276-188">金額</span><span class="sxs-lookup"><span data-stu-id="af276-188">Amount</span></span>  | <span data-ttu-id="af276-189">計算</span><span class="sxs-lookup"><span data-stu-id="af276-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="af276-190">110110</span><span class="sxs-lookup"><span data-stu-id="af276-190">110110</span></span>         | <span data-ttu-id="af276-191">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-191">EUR</span></span>      | <span data-ttu-id="af276-192">500.00</span><span class="sxs-lookup"><span data-stu-id="af276-192">500.00</span></span>  | <span data-ttu-id="af276-193">元の金額 500 × 1</span><span class="sxs-lookup"><span data-stu-id="af276-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="af276-194">130100</span><span class="sxs-lookup"><span data-stu-id="af276-194">130100</span></span>         | <span data-ttu-id="af276-195">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-195">EUR</span></span>      | <span data-ttu-id="af276-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="af276-196">-500.00</span></span> | <span data-ttu-id="af276-197">元の金額 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="af276-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="af276-198">801400</span><span class="sxs-lookup"><span data-stu-id="af276-198">801400</span></span>         | <span data-ttu-id="af276-199">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-199">EUR</span></span>      | <span data-ttu-id="af276-200">250</span><span class="sxs-lookup"><span data-stu-id="af276-200">250</span></span>     | <span data-ttu-id="af276-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="af276-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="af276-202">801600</span><span class="sxs-lookup"><span data-stu-id="af276-202">801600</span></span>         | <span data-ttu-id="af276-203">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="af276-203">EUR</span></span>      | <span data-ttu-id="af276-204">-250</span><span class="sxs-lookup"><span data-stu-id="af276-204">-250</span></span>    | <span data-ttu-id="af276-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="af276-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





