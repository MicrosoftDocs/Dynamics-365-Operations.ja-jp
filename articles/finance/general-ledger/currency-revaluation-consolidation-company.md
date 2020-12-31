---
title: 連結会社の通貨再評価
description: このトピックでは、連結会社の通貨を再評価する方法について説明します。
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4445355"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f890e-103">連結会社の通貨再評価</span><span class="sxs-lookup"><span data-stu-id="f890e-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f890e-104">1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f890e-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f890e-105">最初にデータを連結する場合、**為替換算** タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f890e-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f890e-106">新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f890e-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f890e-107">未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。</span><span class="sxs-lookup"><span data-stu-id="f890e-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f890e-108">次の例では、プロセス中に作成された勘定項目を示します。</span><span class="sxs-lookup"><span data-stu-id="f890e-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f890e-109">会社設定</span><span class="sxs-lookup"><span data-stu-id="f890e-109">Company setup</span></span>
-   <span data-ttu-id="f890e-110">**ソース / 営業会社 (USMF)** – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="f890e-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f890e-111">**連結会社 (CON)** – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="f890e-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f890e-112">**実現利益** – 勘定科目 801500</span><span class="sxs-lookup"><span data-stu-id="f890e-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f890e-113">**実現損失** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="f890e-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f890e-114">**未実現利益** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="f890e-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f890e-115">**未実現損失** – 勘定科目 801400</span><span class="sxs-lookup"><span data-stu-id="f890e-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f890e-116">元のトランザクション</span><span class="sxs-lookup"><span data-stu-id="f890e-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f890e-117">[USMF] の現金領収トランザクション</span><span class="sxs-lookup"><span data-stu-id="f890e-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f890e-118">日</span><span class="sxs-lookup"><span data-stu-id="f890e-118">Date</span></span>       | <span data-ttu-id="f890e-119">勘定科目</span><span class="sxs-lookup"><span data-stu-id="f890e-119">Ledger account</span></span>               | <span data-ttu-id="f890e-120">通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-120">Currency</span></span> | <span data-ttu-id="f890e-121">金額</span><span class="sxs-lookup"><span data-stu-id="f890e-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f890e-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f890e-122">10/11/2015</span></span> | <span data-ttu-id="f890e-123">110110 – 現金</span><span class="sxs-lookup"><span data-stu-id="f890e-123">110110 – Cash</span></span>                | <span data-ttu-id="f890e-124">USD</span><span class="sxs-lookup"><span data-stu-id="f890e-124">USD</span></span>      | <span data-ttu-id="f890e-125">500</span><span class="sxs-lookup"><span data-stu-id="f890e-125">500</span></span>    |
| <span data-ttu-id="f890e-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f890e-126">10/11/2015</span></span> | <span data-ttu-id="f890e-127">130100 – [売掛金勘定]</span><span class="sxs-lookup"><span data-stu-id="f890e-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f890e-128">USD</span><span class="sxs-lookup"><span data-stu-id="f890e-128">USD</span></span>      | <span data-ttu-id="f890e-129">-500</span><span class="sxs-lookup"><span data-stu-id="f890e-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f890e-130">為替レート</span><span class="sxs-lookup"><span data-stu-id="f890e-130">Exchange rates</span></span>

| <span data-ttu-id="f890e-131">開始通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-131">From currency</span></span> | <span data-ttu-id="f890e-132">終了通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-132">To currency</span></span> | <span data-ttu-id="f890e-133">開始日</span><span class="sxs-lookup"><span data-stu-id="f890e-133">Start date</span></span> | <span data-ttu-id="f890e-134">為替レート</span><span class="sxs-lookup"><span data-stu-id="f890e-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f890e-135">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-135">EUR</span></span>           | <span data-ttu-id="f890e-136">USD</span><span class="sxs-lookup"><span data-stu-id="f890e-136">USD</span></span>         | <span data-ttu-id="f890e-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="f890e-137">10/1/2015</span></span>  | <span data-ttu-id="f890e-138">200</span><span class="sxs-lookup"><span data-stu-id="f890e-138">200</span></span>           |
| <span data-ttu-id="f890e-139">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-139">EUR</span></span>           | <span data-ttu-id="f890e-140">USD</span><span class="sxs-lookup"><span data-stu-id="f890e-140">USD</span></span>         | <span data-ttu-id="f890e-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="f890e-141">11/1/2015</span></span>  | <span data-ttu-id="f890e-142">150</span><span class="sxs-lookup"><span data-stu-id="f890e-142">150</span></span>           |
| <span data-ttu-id="f890e-143">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-143">EUR</span></span>           | <span data-ttu-id="f890e-144">USD</span><span class="sxs-lookup"><span data-stu-id="f890e-144">USD</span></span>         | <span data-ttu-id="f890e-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="f890e-145">12/1/2012</span></span>  | <span data-ttu-id="f890e-146">100</span><span class="sxs-lookup"><span data-stu-id="f890e-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f890e-147">2015 年 10 月の連結を実行</span><span class="sxs-lookup"><span data-stu-id="f890e-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f890e-148">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="f890e-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f890e-149">勘定科目</span><span class="sxs-lookup"><span data-stu-id="f890e-149">Ledger account</span></span> | <span data-ttu-id="f890e-150">通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-150">Currency</span></span> | <span data-ttu-id="f890e-151">金額</span><span class="sxs-lookup"><span data-stu-id="f890e-151">Amount</span></span> | <span data-ttu-id="f890e-152">計算</span><span class="sxs-lookup"><span data-stu-id="f890e-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f890e-153">110110</span><span class="sxs-lookup"><span data-stu-id="f890e-153">110110</span></span>         | <span data-ttu-id="f890e-154">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-154">EUR</span></span>      | <span data-ttu-id="f890e-155">250</span><span class="sxs-lookup"><span data-stu-id="f890e-155">250</span></span>    | <span data-ttu-id="f890e-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f890e-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f890e-157">130100</span><span class="sxs-lookup"><span data-stu-id="f890e-157">130100</span></span>         | <span data-ttu-id="f890e-158">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-158">EUR</span></span>      | <span data-ttu-id="f890e-159">-250</span><span class="sxs-lookup"><span data-stu-id="f890e-159">-250</span></span>   | <span data-ttu-id="f890e-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="f890e-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f890e-161">2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="f890e-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f890e-162">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="f890e-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f890e-163">勘定科目</span><span class="sxs-lookup"><span data-stu-id="f890e-163">Ledger account</span></span> | <span data-ttu-id="f890e-164">通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-164">Currency</span></span> | <span data-ttu-id="f890e-165">金額</span><span class="sxs-lookup"><span data-stu-id="f890e-165">Amount</span></span>  | <span data-ttu-id="f890e-166">計算</span><span class="sxs-lookup"><span data-stu-id="f890e-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f890e-167">110110</span><span class="sxs-lookup"><span data-stu-id="f890e-167">110110</span></span>         | <span data-ttu-id="f890e-168">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-168">EUR</span></span>      | <span data-ttu-id="f890e-169">333.33</span><span class="sxs-lookup"><span data-stu-id="f890e-169">333.33</span></span>  | <span data-ttu-id="f890e-170">元の金額 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="f890e-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f890e-171">130100</span><span class="sxs-lookup"><span data-stu-id="f890e-171">130100</span></span>         | <span data-ttu-id="f890e-172">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-172">EUR</span></span>      | <span data-ttu-id="f890e-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="f890e-173">-333.33</span></span> | <span data-ttu-id="f890e-174">元の金額 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="f890e-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f890e-175">801400</span><span class="sxs-lookup"><span data-stu-id="f890e-175">801400</span></span>         | <span data-ttu-id="f890e-176">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-176">EUR</span></span>      | <span data-ttu-id="f890e-177">83.33</span><span class="sxs-lookup"><span data-stu-id="f890e-177">83.33</span></span>   | <span data-ttu-id="f890e-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="f890e-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f890e-179">801600</span><span class="sxs-lookup"><span data-stu-id="f890e-179">801600</span></span>         | <span data-ttu-id="f890e-180">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-180">EUR</span></span>      | <span data-ttu-id="f890e-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="f890e-181">-83.33</span></span>  | <span data-ttu-id="f890e-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f890e-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f890e-183">レポート通貨の金額に対する追加トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f890e-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f890e-184">2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="f890e-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f890e-185">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="f890e-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f890e-186">勘定科目</span><span class="sxs-lookup"><span data-stu-id="f890e-186">Ledger account</span></span> | <span data-ttu-id="f890e-187">通貨</span><span class="sxs-lookup"><span data-stu-id="f890e-187">Currency</span></span> | <span data-ttu-id="f890e-188">金額</span><span class="sxs-lookup"><span data-stu-id="f890e-188">Amount</span></span>  | <span data-ttu-id="f890e-189">計算</span><span class="sxs-lookup"><span data-stu-id="f890e-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f890e-190">110110</span><span class="sxs-lookup"><span data-stu-id="f890e-190">110110</span></span>         | <span data-ttu-id="f890e-191">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-191">EUR</span></span>      | <span data-ttu-id="f890e-192">500.00</span><span class="sxs-lookup"><span data-stu-id="f890e-192">500.00</span></span>  | <span data-ttu-id="f890e-193">元の金額 500 × 1</span><span class="sxs-lookup"><span data-stu-id="f890e-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f890e-194">130100</span><span class="sxs-lookup"><span data-stu-id="f890e-194">130100</span></span>         | <span data-ttu-id="f890e-195">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-195">EUR</span></span>      | <span data-ttu-id="f890e-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="f890e-196">-500.00</span></span> | <span data-ttu-id="f890e-197">元の金額 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f890e-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f890e-198">801400</span><span class="sxs-lookup"><span data-stu-id="f890e-198">801400</span></span>         | <span data-ttu-id="f890e-199">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-199">EUR</span></span>      | <span data-ttu-id="f890e-200">250</span><span class="sxs-lookup"><span data-stu-id="f890e-200">250</span></span>     | <span data-ttu-id="f890e-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="f890e-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f890e-202">801600</span><span class="sxs-lookup"><span data-stu-id="f890e-202">801600</span></span>         | <span data-ttu-id="f890e-203">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="f890e-203">EUR</span></span>      | <span data-ttu-id="f890e-204">-250</span><span class="sxs-lookup"><span data-stu-id="f890e-204">-250</span></span>    | <span data-ttu-id="f890e-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="f890e-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





