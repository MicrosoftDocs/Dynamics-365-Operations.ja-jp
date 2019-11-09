---
title: 過剰支払の場合の現金割引の処理
description: この記事では、顧客が現金割引を受け、かつ過剰支払をしている場合の支払の処理方法を示すシナリオについて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 803cb478bb7631439ebde66ad96182193d3dd1ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188352"
---
# <a name="handling-cash-discounts-for-overpayments"></a><span data-ttu-id="e1338-103">過剰支払の場合の現金割引の処理</span><span class="sxs-lookup"><span data-stu-id="e1338-103">Handling cash discounts for overpayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1338-104">この記事では、顧客が現金割引を受け、かつ過剰支払をしている場合の支払の処理方法を示すシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e1338-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="e1338-105">請求書は、支払額が現金割引を差し引いた請求金額を超えると、過剰支払いと見なされます。</span><span class="sxs-lookup"><span data-stu-id="e1338-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="e1338-106">請求書が過剰支払された場合の取得可能な現金割引差額の処理方法を指定するには、**現金割引管理**ページと**売掛金勘定パラメーター**ページの**最大の過剰支払/過少支払**フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1338-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="e1338-107">次の例では、顧客の請求書が 0.50 過剰支払になっています。</span><span class="sxs-lookup"><span data-stu-id="e1338-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="e1338-108">請求合計</span><span class="sxs-lookup"><span data-stu-id="e1338-108">Invoice total</span></span> | <span data-ttu-id="e1338-109">利用可能な現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-109">Cash discount available</span></span> | <span data-ttu-id="e1338-110">支払額 (現金割引を含む)</span><span class="sxs-lookup"><span data-stu-id="e1338-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="e1338-111">顧客の実際の支払額</span><span class="sxs-lookup"><span data-stu-id="e1338-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="e1338-112">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-112">105.00</span></span>        | <span data-ttu-id="e1338-113">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-113">10.50</span></span>                   | <span data-ttu-id="e1338-114">94.50</span><span class="sxs-lookup"><span data-stu-id="e1338-114">94.50</span></span>                                               | <span data-ttu-id="e1338-115">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="e1338-116">現金割引管理オプション = 限定</span><span class="sxs-lookup"><span data-stu-id="e1338-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="e1338-117">**自動トランザクションの勘定**ページの**現金割引管理**フィールドで**特定**が選択されている場合、完全な現金割引が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="e1338-118">過剰支払い額は、現金割引差分勘定科目へ転記されるか、または顧客勘定の残高になります。</span><span class="sxs-lookup"><span data-stu-id="e1338-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="e1338-119">動作は、過剰支払の金額が 0.00 と**最大の過剰支払/過少支払**フィールドに入力されている額の間にあるか、または過剰支払金額が**最大の過剰支払/過少支払**額より大きいかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e1338-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="e1338-120">シナリオ 1</span><span class="sxs-lookup"><span data-stu-id="e1338-120">Scenario 1</span></span>

<span data-ttu-id="e1338-121">このシナリオでは、過剰支払い額が 0.00 と最大過剰支払または過少支払の間にあります。</span><span class="sxs-lookup"><span data-stu-id="e1338-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="e1338-122">105.00 の請求書が、請求書が 7 日以内に支払われた場合に現金割引されるという条件で入力されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="e1338-123">請求合計</span><span class="sxs-lookup"><span data-stu-id="e1338-123">Invoice total</span></span> | <span data-ttu-id="e1338-124">利用可能な現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-124">Cash discount available</span></span> | <span data-ttu-id="e1338-125">支払額 (現金割引を含む)</span><span class="sxs-lookup"><span data-stu-id="e1338-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="e1338-126">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-126">105.00</span></span>        | <span data-ttu-id="e1338-127">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-127">10.50</span></span>                   | <span data-ttu-id="e1338-128">94.50</span><span class="sxs-lookup"><span data-stu-id="e1338-128">94.50</span></span>                                               |

<span data-ttu-id="e1338-129">顧客が現金割引期間内に 95.00 の支払を送信します。</span><span class="sxs-lookup"><span data-stu-id="e1338-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="e1338-130">支払は、105.00 の請求書に対して決済されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="e1338-131">請求書と支払が決済されると、次のトランザクションは顧客の売掛金勘定で作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="e1338-132">トランザクション</span><span class="sxs-lookup"><span data-stu-id="e1338-132">Transaction</span></span>   | <span data-ttu-id="e1338-133">金額</span><span class="sxs-lookup"><span data-stu-id="e1338-133">Amount</span></span> | <span data-ttu-id="e1338-134">残高</span><span class="sxs-lookup"><span data-stu-id="e1338-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="e1338-135">請求書</span><span class="sxs-lookup"><span data-stu-id="e1338-135">Invoice</span></span>       | <span data-ttu-id="e1338-136">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-136">105.00</span></span> | <span data-ttu-id="e1338-137">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-137">0.00</span></span>    |
| <span data-ttu-id="e1338-138">支払</span><span class="sxs-lookup"><span data-stu-id="e1338-138">Payment</span></span>       | <span data-ttu-id="e1338-139">-95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-139">-95.00</span></span> | <span data-ttu-id="e1338-140">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-140">0.00</span></span>    |
| <span data-ttu-id="e1338-141">現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-141">Cash discount</span></span> | <span data-ttu-id="e1338-142">-10.50</span><span class="sxs-lookup"><span data-stu-id="e1338-142">-10.50</span></span> | <span data-ttu-id="e1338-143">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-143">0.00</span></span>    |

<span data-ttu-id="e1338-144">次の勘定項目が、支払および決済に生成されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="e1338-145">**支払**</span><span class="sxs-lookup"><span data-stu-id="e1338-145">**Payment**</span></span>

| <span data-ttu-id="e1338-146">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-146">Account</span></span>             | <span data-ttu-id="e1338-147">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-147">Debit amount</span></span> | <span data-ttu-id="e1338-148">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="e1338-149">現金</span><span class="sxs-lookup"><span data-stu-id="e1338-149">Cash</span></span>                | <span data-ttu-id="e1338-150">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-150">95.00</span></span>        |               |
| <span data-ttu-id="e1338-151">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-151">Accounts receivable</span></span> |              | <span data-ttu-id="e1338-152">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-152">95.00</span></span>         |

<span data-ttu-id="e1338-153">**決済**</span><span class="sxs-lookup"><span data-stu-id="e1338-153">**Settlement**</span></span>

| <span data-ttu-id="e1338-154">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-154">Account</span></span>                                                                                                          | <span data-ttu-id="e1338-155">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-155">Debit amount</span></span> | <span data-ttu-id="e1338-156">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="e1338-157">現金割引 (**現金割引**ページの**顧客割引の主勘定**フィールド)</span><span class="sxs-lookup"><span data-stu-id="e1338-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="e1338-158">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-158">10.50</span></span>        |               |
| <span data-ttu-id="e1338-159">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="e1338-160">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-160">10.50</span></span>         |
| <span data-ttu-id="e1338-161">顧客現金割引 (**自動トランザクションの勘定**ページの**顧客現金割引**フィールド)</span><span class="sxs-lookup"><span data-stu-id="e1338-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="e1338-162">0.50</span><span class="sxs-lookup"><span data-stu-id="e1338-162">0.50</span></span>          |
| <span data-ttu-id="e1338-163">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="e1338-164">0.50</span><span class="sxs-lookup"><span data-stu-id="e1338-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="e1338-165">シナリオ 2</span><span class="sxs-lookup"><span data-stu-id="e1338-165">Scenario 2</span></span>

<span data-ttu-id="e1338-166">このシナリオでは、過剰支払い額が最大過剰支払または過少支払を超えています。</span><span class="sxs-lookup"><span data-stu-id="e1338-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="e1338-167">105.00 の請求書が、請求書が 7 日以内に支払われた場合に現金割引されるという条件で入力されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="e1338-168">請求合計</span><span class="sxs-lookup"><span data-stu-id="e1338-168">Invoice total</span></span> | <span data-ttu-id="e1338-169">利用可能な現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-169">Cash discount available</span></span> | <span data-ttu-id="e1338-170">支払額 (現金割引を含む)</span><span class="sxs-lookup"><span data-stu-id="e1338-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="e1338-171">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-171">105.00</span></span>        | <span data-ttu-id="e1338-172">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-172">10.50</span></span>                   | <span data-ttu-id="e1338-173">94.50</span><span class="sxs-lookup"><span data-stu-id="e1338-173">94.50</span></span>                                               |

<span data-ttu-id="e1338-174">顧客が現金割引期間内に 95.00 の支払を送信します。</span><span class="sxs-lookup"><span data-stu-id="e1338-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="e1338-175">支払は、105.00 の請求書に対して決済されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="e1338-176">請求書と支払が決済されると、次のトランザクションは顧客の売掛金勘定で作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="e1338-177">トランザクション</span><span class="sxs-lookup"><span data-stu-id="e1338-177">Transaction</span></span>   | <span data-ttu-id="e1338-178">金額</span><span class="sxs-lookup"><span data-stu-id="e1338-178">Amount</span></span> | <span data-ttu-id="e1338-179">残高</span><span class="sxs-lookup"><span data-stu-id="e1338-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="e1338-180">請求書</span><span class="sxs-lookup"><span data-stu-id="e1338-180">Invoice</span></span>       | <span data-ttu-id="e1338-181">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-181">105.00</span></span> | <span data-ttu-id="e1338-182">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-182">0.00</span></span>    |
| <span data-ttu-id="e1338-183">支払</span><span class="sxs-lookup"><span data-stu-id="e1338-183">Payment</span></span>       | <span data-ttu-id="e1338-184">-95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-184">-95.00</span></span> | <span data-ttu-id="e1338-185">-0.50</span><span class="sxs-lookup"><span data-stu-id="e1338-185">-0.50</span></span>   |
| <span data-ttu-id="e1338-186">現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-186">Cash discount</span></span> | <span data-ttu-id="e1338-187">-10.50</span><span class="sxs-lookup"><span data-stu-id="e1338-187">-10.50</span></span> | <span data-ttu-id="e1338-188">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-188">0.00</span></span>    |

<span data-ttu-id="e1338-189">0.50 の支払超過分の金額は、支払の未処理残高として残り、異なる請求書に対して決済することができます。</span><span class="sxs-lookup"><span data-stu-id="e1338-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="e1338-190">次の勘定項目が、支払および決済に生成されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="e1338-191">**支払**</span><span class="sxs-lookup"><span data-stu-id="e1338-191">**Payment**</span></span>

| <span data-ttu-id="e1338-192">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-192">Account</span></span>             | <span data-ttu-id="e1338-193">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-193">Debit amount</span></span> | <span data-ttu-id="e1338-194">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="e1338-195">現金</span><span class="sxs-lookup"><span data-stu-id="e1338-195">Cash</span></span>                | <span data-ttu-id="e1338-196">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-196">95.00</span></span>        |               |
| <span data-ttu-id="e1338-197">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-197">Accounts receivable</span></span> |              | <span data-ttu-id="e1338-198">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-198">95.00</span></span>         |

<span data-ttu-id="e1338-199">**決済**</span><span class="sxs-lookup"><span data-stu-id="e1338-199">**Settlement**</span></span>

| <span data-ttu-id="e1338-200">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-200">Account</span></span>                                                                                          | <span data-ttu-id="e1338-201">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-201">Debit amount</span></span> | <span data-ttu-id="e1338-202">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="e1338-203">現金割引 (**現金割引**ページの**顧客割引の主勘定**フィールド)</span><span class="sxs-lookup"><span data-stu-id="e1338-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="e1338-204">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-204">10.50</span></span>        |               |
| <span data-ttu-id="e1338-205">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="e1338-206">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="e1338-207">現金割引管理 = 非限定</span><span class="sxs-lookup"><span data-stu-id="e1338-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="e1338-208">**自動トランザクションの勘定**ページの**現金割引管理**フィールドで**非限定**が選択されている場合、現金割引金額が過剰支払金額によって減額されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="e1338-209">この動作は、過剰支払の金額がまたはフィールドに入れられる金額未満であるかどうかに関係なく、常に **最大の超過/不足支払** 適用されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="e1338-210">シナリオ 3</span><span class="sxs-lookup"><span data-stu-id="e1338-210">Scenario 3</span></span>

<span data-ttu-id="e1338-211">このシナリオでは 105.00 の請求書が、請求書が 7 日以内に支払われた場合に現金割引されるという条件で入力されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="e1338-212">請求合計</span><span class="sxs-lookup"><span data-stu-id="e1338-212">Invoice total</span></span> | <span data-ttu-id="e1338-213">利用可能な現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-213">Cash discount available</span></span> | <span data-ttu-id="e1338-214">支払額 (現金割引を含む)</span><span class="sxs-lookup"><span data-stu-id="e1338-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="e1338-215">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-215">105.00</span></span>        | <span data-ttu-id="e1338-216">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-216">10.50</span></span>                   | <span data-ttu-id="e1338-217">94.50</span><span class="sxs-lookup"><span data-stu-id="e1338-217">94.50</span></span>                                               |

<span data-ttu-id="e1338-218">顧客が現金割引の日付内に 95.00 の支払を送信します。</span><span class="sxs-lookup"><span data-stu-id="e1338-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="e1338-219">支払は、105.00 の請求書に対して決済されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="e1338-220">請求書と支払が決済されると、次のトランザクションは顧客の売掛金勘定で作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1338-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="e1338-221">トランザクション</span><span class="sxs-lookup"><span data-stu-id="e1338-221">Transaction</span></span>   | <span data-ttu-id="e1338-222">金額</span><span class="sxs-lookup"><span data-stu-id="e1338-222">Amount</span></span> | <span data-ttu-id="e1338-223">残高</span><span class="sxs-lookup"><span data-stu-id="e1338-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="e1338-224">請求書</span><span class="sxs-lookup"><span data-stu-id="e1338-224">Invoice</span></span>       | <span data-ttu-id="e1338-225">105.00</span><span class="sxs-lookup"><span data-stu-id="e1338-225">105.00</span></span> | <span data-ttu-id="e1338-226">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-226">0.00</span></span>    |
| <span data-ttu-id="e1338-227">支払</span><span class="sxs-lookup"><span data-stu-id="e1338-227">Payment</span></span>       | <span data-ttu-id="e1338-228">-95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-228">-95.00</span></span> | <span data-ttu-id="e1338-229">-0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-229">-0.00</span></span>   |
| <span data-ttu-id="e1338-230">現金割引</span><span class="sxs-lookup"><span data-stu-id="e1338-230">Cash discount</span></span> | <span data-ttu-id="e1338-231">-10.00</span><span class="sxs-lookup"><span data-stu-id="e1338-231">-10.00</span></span> | <span data-ttu-id="e1338-232">0.00</span><span class="sxs-lookup"><span data-stu-id="e1338-232">0.00</span></span>    |

<span data-ttu-id="e1338-233">現金割引金額は 10.50 から 10.00 に減少します。</span><span class="sxs-lookup"><span data-stu-id="e1338-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="e1338-234">支払と請求書が決済済みと見なされます。</span><span class="sxs-lookup"><span data-stu-id="e1338-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="e1338-235">**支払**</span><span class="sxs-lookup"><span data-stu-id="e1338-235">**Payment**</span></span>

| <span data-ttu-id="e1338-236">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-236">Account</span></span>             | <span data-ttu-id="e1338-237">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-237">Debit amount</span></span> | <span data-ttu-id="e1338-238">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="e1338-239">現金</span><span class="sxs-lookup"><span data-stu-id="e1338-239">Cash</span></span>                | <span data-ttu-id="e1338-240">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-240">95.00</span></span>        |               |
| <span data-ttu-id="e1338-241">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-241">Accounts receivable</span></span> |              | <span data-ttu-id="e1338-242">95.00</span><span class="sxs-lookup"><span data-stu-id="e1338-242">95.00</span></span>         |

<span data-ttu-id="e1338-243">**決済**</span><span class="sxs-lookup"><span data-stu-id="e1338-243">**Settlement**</span></span>

| <span data-ttu-id="e1338-244">口座</span><span class="sxs-lookup"><span data-stu-id="e1338-244">Account</span></span>                                                                                          | <span data-ttu-id="e1338-245">借方金額</span><span class="sxs-lookup"><span data-stu-id="e1338-245">Debit amount</span></span> | <span data-ttu-id="e1338-246">クレジット金額</span><span class="sxs-lookup"><span data-stu-id="e1338-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="e1338-247">現金割引 (**現金割引**ページの**顧客割引の主勘定**フィールド)</span><span class="sxs-lookup"><span data-stu-id="e1338-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="e1338-248">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-248">10.50</span></span>        |               |
| <span data-ttu-id="e1338-249">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="e1338-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="e1338-250">1050</span><span class="sxs-lookup"><span data-stu-id="e1338-250">10.50</span></span>         |




