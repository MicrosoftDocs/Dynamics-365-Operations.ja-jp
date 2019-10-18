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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178621"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="8ddcb-103">連結会社の通貨再評価</span><span class="sxs-lookup"><span data-stu-id="8ddcb-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ddcb-104">1 つの会計通貨から別の会計通貨にデータを連結する場合、為替レートに変更があれば、勘定残高が正しく再評価されるように通貨再評価を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="8ddcb-105">最初にデータを連結する場合、**為替換算**タブを使用して、連結プロセス中の換算のために、最初の為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="8ddcb-106">新しい為替レートが入力された後 (たとえば、翌月に) に、勘定残高を再評価する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="8ddcb-107">未実現差益または差損は、新しい為替レートと日付に基づいて、適宜更新されます。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="8ddcb-108">次の例では、プロセス中に作成された勘定項目を示します。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="8ddcb-109">会社設定</span><span class="sxs-lookup"><span data-stu-id="8ddcb-109">Company setup</span></span>
-   <span data-ttu-id="8ddcb-110">**ソース / 営業会社 (USMF)** – 米ドル (USD) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="8ddcb-111">**連結会社 (CON)** – ユーロ (EUR) は、会計通貨およびレポート通貨として使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="8ddcb-112">**実現利益** – 勘定科目 801500</span><span class="sxs-lookup"><span data-stu-id="8ddcb-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="8ddcb-113">**実現損失** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="8ddcb-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="8ddcb-114">**未実現利益** – 勘定科目 801600</span><span class="sxs-lookup"><span data-stu-id="8ddcb-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="8ddcb-115">**未実現損失** – 勘定科目 801400</span><span class="sxs-lookup"><span data-stu-id="8ddcb-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="8ddcb-116">元のトランザクション</span><span class="sxs-lookup"><span data-stu-id="8ddcb-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="8ddcb-117">[USMF] の現金領収トランザクション</span><span class="sxs-lookup"><span data-stu-id="8ddcb-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="8ddcb-118">日</span><span class="sxs-lookup"><span data-stu-id="8ddcb-118">Date</span></span>       | <span data-ttu-id="8ddcb-119">勘定科目</span><span class="sxs-lookup"><span data-stu-id="8ddcb-119">Ledger account</span></span>               | <span data-ttu-id="8ddcb-120">通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-120">Currency</span></span> | <span data-ttu-id="8ddcb-121">金額</span><span class="sxs-lookup"><span data-stu-id="8ddcb-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="8ddcb-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="8ddcb-122">10/11/2015</span></span> | <span data-ttu-id="8ddcb-123">110110 – 現金</span><span class="sxs-lookup"><span data-stu-id="8ddcb-123">110110 – Cash</span></span>                | <span data-ttu-id="8ddcb-124">USD</span><span class="sxs-lookup"><span data-stu-id="8ddcb-124">USD</span></span>      | <span data-ttu-id="8ddcb-125">500</span><span class="sxs-lookup"><span data-stu-id="8ddcb-125">500</span></span>    |
| <span data-ttu-id="8ddcb-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="8ddcb-126">10/11/2015</span></span> | <span data-ttu-id="8ddcb-127">130100 – [売掛金勘定]</span><span class="sxs-lookup"><span data-stu-id="8ddcb-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="8ddcb-128">USD</span><span class="sxs-lookup"><span data-stu-id="8ddcb-128">USD</span></span>      | <span data-ttu-id="8ddcb-129">-500</span><span class="sxs-lookup"><span data-stu-id="8ddcb-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="8ddcb-130">為替レート</span><span class="sxs-lookup"><span data-stu-id="8ddcb-130">Exchange rates</span></span>

| <span data-ttu-id="8ddcb-131">開始通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-131">From currency</span></span> | <span data-ttu-id="8ddcb-132">終了通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-132">To currency</span></span> | <span data-ttu-id="8ddcb-133">開始日</span><span class="sxs-lookup"><span data-stu-id="8ddcb-133">Start date</span></span> | <span data-ttu-id="8ddcb-134">為替レート</span><span class="sxs-lookup"><span data-stu-id="8ddcb-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="8ddcb-135">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-135">EUR</span></span>           | <span data-ttu-id="8ddcb-136">USD</span><span class="sxs-lookup"><span data-stu-id="8ddcb-136">USD</span></span>         | <span data-ttu-id="8ddcb-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="8ddcb-137">10/1/2015</span></span>  | <span data-ttu-id="8ddcb-138">200</span><span class="sxs-lookup"><span data-stu-id="8ddcb-138">200</span></span>           |
| <span data-ttu-id="8ddcb-139">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-139">EUR</span></span>           | <span data-ttu-id="8ddcb-140">USD</span><span class="sxs-lookup"><span data-stu-id="8ddcb-140">USD</span></span>         | <span data-ttu-id="8ddcb-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="8ddcb-141">11/1/2015</span></span>  | <span data-ttu-id="8ddcb-142">150</span><span class="sxs-lookup"><span data-stu-id="8ddcb-142">150</span></span>           |
| <span data-ttu-id="8ddcb-143">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-143">EUR</span></span>           | <span data-ttu-id="8ddcb-144">USD</span><span class="sxs-lookup"><span data-stu-id="8ddcb-144">USD</span></span>         | <span data-ttu-id="8ddcb-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="8ddcb-145">12/1/2012</span></span>  | <span data-ttu-id="8ddcb-146">100</span><span class="sxs-lookup"><span data-stu-id="8ddcb-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="8ddcb-147">2015 年 10 月の連結を実行</span><span class="sxs-lookup"><span data-stu-id="8ddcb-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8ddcb-148">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="8ddcb-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="8ddcb-149">勘定科目</span><span class="sxs-lookup"><span data-stu-id="8ddcb-149">Ledger account</span></span> | <span data-ttu-id="8ddcb-150">通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-150">Currency</span></span> | <span data-ttu-id="8ddcb-151">金額</span><span class="sxs-lookup"><span data-stu-id="8ddcb-151">Amount</span></span> | <span data-ttu-id="8ddcb-152">計算</span><span class="sxs-lookup"><span data-stu-id="8ddcb-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="8ddcb-153">110110</span><span class="sxs-lookup"><span data-stu-id="8ddcb-153">110110</span></span>         | <span data-ttu-id="8ddcb-154">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-154">EUR</span></span>      | <span data-ttu-id="8ddcb-155">250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-155">250</span></span>    | <span data-ttu-id="8ddcb-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="8ddcb-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="8ddcb-157">130100</span><span class="sxs-lookup"><span data-stu-id="8ddcb-157">130100</span></span>         | <span data-ttu-id="8ddcb-158">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-158">EUR</span></span>      | <span data-ttu-id="8ddcb-159">-250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-159">-250</span></span>   | <span data-ttu-id="8ddcb-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="8ddcb-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="8ddcb-161">2015 年 10 月1 日から 2015 年 11 月 30 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="8ddcb-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8ddcb-162">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="8ddcb-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="8ddcb-163">勘定科目</span><span class="sxs-lookup"><span data-stu-id="8ddcb-163">Ledger account</span></span> | <span data-ttu-id="8ddcb-164">通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-164">Currency</span></span> | <span data-ttu-id="8ddcb-165">金額</span><span class="sxs-lookup"><span data-stu-id="8ddcb-165">Amount</span></span>  | <span data-ttu-id="8ddcb-166">計算</span><span class="sxs-lookup"><span data-stu-id="8ddcb-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="8ddcb-167">110110</span><span class="sxs-lookup"><span data-stu-id="8ddcb-167">110110</span></span>         | <span data-ttu-id="8ddcb-168">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-168">EUR</span></span>      | <span data-ttu-id="8ddcb-169">333.33</span><span class="sxs-lookup"><span data-stu-id="8ddcb-169">333.33</span></span>  | <span data-ttu-id="8ddcb-170">元の金額 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="8ddcb-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="8ddcb-171">130100</span><span class="sxs-lookup"><span data-stu-id="8ddcb-171">130100</span></span>         | <span data-ttu-id="8ddcb-172">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-172">EUR</span></span>      | <span data-ttu-id="8ddcb-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="8ddcb-173">-333.33</span></span> | <span data-ttu-id="8ddcb-174">元の金額 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="8ddcb-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="8ddcb-175">801400</span><span class="sxs-lookup"><span data-stu-id="8ddcb-175">801400</span></span>         | <span data-ttu-id="8ddcb-176">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-176">EUR</span></span>      | <span data-ttu-id="8ddcb-177">83.33</span><span class="sxs-lookup"><span data-stu-id="8ddcb-177">83.33</span></span>   | <span data-ttu-id="8ddcb-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="8ddcb-179">801600</span><span class="sxs-lookup"><span data-stu-id="8ddcb-179">801600</span></span>         | <span data-ttu-id="8ddcb-180">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-180">EUR</span></span>      | <span data-ttu-id="8ddcb-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="8ddcb-181">-83.33</span></span>  | <span data-ttu-id="8ddcb-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="8ddcb-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="8ddcb-183">レポート通貨の金額に対する追加トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ddcb-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="8ddcb-184">2015 年 10 月1 日から 2015 年 12 月 31 日の勘定の通貨再評価を実行</span><span class="sxs-lookup"><span data-stu-id="8ddcb-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="8ddcb-185">連結会社の残高</span><span class="sxs-lookup"><span data-stu-id="8ddcb-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="8ddcb-186">勘定科目</span><span class="sxs-lookup"><span data-stu-id="8ddcb-186">Ledger account</span></span> | <span data-ttu-id="8ddcb-187">通貨</span><span class="sxs-lookup"><span data-stu-id="8ddcb-187">Currency</span></span> | <span data-ttu-id="8ddcb-188">金額</span><span class="sxs-lookup"><span data-stu-id="8ddcb-188">Amount</span></span>  | <span data-ttu-id="8ddcb-189">計算</span><span class="sxs-lookup"><span data-stu-id="8ddcb-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="8ddcb-190">110110</span><span class="sxs-lookup"><span data-stu-id="8ddcb-190">110110</span></span>         | <span data-ttu-id="8ddcb-191">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-191">EUR</span></span>      | <span data-ttu-id="8ddcb-192">500.00</span><span class="sxs-lookup"><span data-stu-id="8ddcb-192">500.00</span></span>  | <span data-ttu-id="8ddcb-193">元の金額 500 × 1</span><span class="sxs-lookup"><span data-stu-id="8ddcb-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="8ddcb-194">130100</span><span class="sxs-lookup"><span data-stu-id="8ddcb-194">130100</span></span>         | <span data-ttu-id="8ddcb-195">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-195">EUR</span></span>      | <span data-ttu-id="8ddcb-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="8ddcb-196">-500.00</span></span> | <span data-ttu-id="8ddcb-197">元の金額 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="8ddcb-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="8ddcb-198">801400</span><span class="sxs-lookup"><span data-stu-id="8ddcb-198">801400</span></span>         | <span data-ttu-id="8ddcb-199">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-199">EUR</span></span>      | <span data-ttu-id="8ddcb-200">250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-200">250</span></span>     | <span data-ttu-id="8ddcb-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="8ddcb-202">801600</span><span class="sxs-lookup"><span data-stu-id="8ddcb-202">801600</span></span>         | <span data-ttu-id="8ddcb-203">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="8ddcb-203">EUR</span></span>      | <span data-ttu-id="8ddcb-204">-250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-204">-250</span></span>    | <span data-ttu-id="8ddcb-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="8ddcb-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





