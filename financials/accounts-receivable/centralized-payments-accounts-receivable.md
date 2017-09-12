---
title: "売掛金勘定の集中支払"
description: "複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じトランザクションを複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6327d9cab1651d22cd411f718f6e3a2f8733e13e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a><span data-ttu-id="04c5f-105">売掛金勘定の集中支払</span><span class="sxs-lookup"><span data-stu-id="04c5f-105">Centralized payments for Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04c5f-106">複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="04c5f-107">したがって、同じトランザクションを複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="04c5f-107">Therefore, the same transaction doesn't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="04c5f-108">この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="04c5f-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="04c5f-109">複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="04c5f-110">したがって、同じトランザクションを複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="04c5f-110">Therefore, the same transaction doesn't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="04c5f-111">また、組織は、支払提案、決済、および集中支払用の未処理および決算済トランザクションを編集するプロセスが合理化されるため、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-111">Additionally, the organization saves time, because the processes for payment proposals, settlements, and editing open and closed transactions for centralized payments are streamlined.</span></span> 

<span data-ttu-id="04c5f-112">集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの請求書売掛金情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="04c5f-112">In a centralized payment organization, there are many legal entities for operations, and each operating legal entity manages its own invoices receivable information.</span></span> <span data-ttu-id="04c5f-113">事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人が受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-113">Payments for all the operating legal entities are received by a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="04c5f-114">決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="04c5f-115">組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、集中支払に関連する現金割引トランザクションの処理方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a centralized payment are handled.</span></span> 

<span data-ttu-id="04c5f-116">次の各例で、さまざまなシナリオにおける転記の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="04c5f-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="04c5f-117">これらすべての例について、次の構成が想定されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="04c5f-118">法人は Fabrikam、Fabrikam East、および Fabrikam West です。</span><span class="sxs-lookup"><span data-stu-id="04c5f-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="04c5f-119">顧客支払が Fabrikam に入力されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-119">Customer payments are entered into Fabrikam.</span></span>
-   <span data-ttu-id="04c5f-120">[**会社間会計**] ページの [**現金割引の転記**] フィールドには**請求書の法人**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="04c5f-121">[**会社間会計**] ページの [**為替差益または差損の転記**] フィールドには**請求書の支払**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="04c5f-122">顧客の Northwind Traders は、各法人の顧客として設定されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-122">Customer Northwind Traders is set up as a customer in each legal entity.</span></span> <span data-ttu-id="04c5f-123">さまざまな法人の顧客は同一のグローバル アドレス帳 ID を共有するため、同じ顧客として識別されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-123">The customers from the various legal entities are identified as the same customer because they share the same global address book ID.</span></span>

| <span data-ttu-id="04c5f-124">アドレス帳 ID</span><span class="sxs-lookup"><span data-stu-id="04c5f-124">Address book ID</span></span> | <span data-ttu-id="04c5f-125">顧客口座</span><span class="sxs-lookup"><span data-stu-id="04c5f-125">Customer account</span></span> | <span data-ttu-id="04c5f-126">氏名</span><span class="sxs-lookup"><span data-stu-id="04c5f-126">Name</span></span>              | <span data-ttu-id="04c5f-127">個法</span><span class="sxs-lookup"><span data-stu-id="04c5f-127">Legal entity</span></span>  |
|-----------------|------------------|-------------------|---------------|
| <span data-ttu-id="04c5f-128">4050</span><span class="sxs-lookup"><span data-stu-id="04c5f-128">4050</span></span>            | <span data-ttu-id="04c5f-129">4000</span><span class="sxs-lookup"><span data-stu-id="04c5f-129">4000</span></span>             | <span data-ttu-id="04c5f-130">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="04c5f-130">Northwind Traders</span></span> | <span data-ttu-id="04c5f-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="04c5f-131">Fabrikam</span></span>      |
| <span data-ttu-id="04c5f-132">4050</span><span class="sxs-lookup"><span data-stu-id="04c5f-132">4050</span></span>            | <span data-ttu-id="04c5f-133">4000</span><span class="sxs-lookup"><span data-stu-id="04c5f-133">4000</span></span>             | <span data-ttu-id="04c5f-134">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="04c5f-134">Northwind Traders</span></span> | <span data-ttu-id="04c5f-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="04c5f-135">Fabrikam East</span></span> |
| <span data-ttu-id="04c5f-136">4050</span><span class="sxs-lookup"><span data-stu-id="04c5f-136">4050</span></span>            | <span data-ttu-id="04c5f-137">10000</span><span class="sxs-lookup"><span data-stu-id="04c5f-137">10000</span></span>            | <span data-ttu-id="04c5f-138">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="04c5f-138">Northwind Traders</span></span> | <span data-ttu-id="04c5f-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="04c5f-139">Fabrikam West</span></span> |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="04c5f-140">例 1: 別の法人からの請求書の顧客支払</span><span class="sxs-lookup"><span data-stu-id="04c5f-140">Example 1: Customer payment of invoice from another legal entity</span></span>
<span data-ttu-id="04c5f-141">Fabrikam は、Fabrikam 顧客 ID 4000 の Northwind Traders について 600.00 の支払を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-141">Fabrikam receives a payment of 600.00 for Fabrikam customer account 4000, Northwind Traders.</span></span> <span data-ttu-id="04c5f-142">支払は、Fabrikam East の顧客 ID 4000 に対する未処理請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-142">The payment is settled with an open invoice for customer account 4000 in Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a><span data-ttu-id="04c5f-143">顧客 4000 について請求書が Fabrikam East で転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-143">Invoice is posted in Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="04c5f-144">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-144">Account</span></span>                             | <span data-ttu-id="04c5f-145">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-145">Debit amount</span></span> | <span data-ttu-id="04c5f-146">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-146">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-147">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-147">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-148">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-148">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-149">売上 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-149">Sales (Fabrikam East)</span></span>               |              | <span data-ttu-id="04c5f-150">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-150">600.00</span></span>        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a><span data-ttu-id="04c5f-151">顧客 4000 について支払が Fabrikam で受領および転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-151">Payment is received and posted in Fabrikam for customer 4000</span></span>

| <span data-ttu-id="04c5f-152">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-152">Account</span></span>                        | <span data-ttu-id="04c5f-153">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-153">Debit amount</span></span> | <span data-ttu-id="04c5f-154">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-154">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-155">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-155">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-156">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-156">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-157">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-157">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-158">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-158">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="04c5f-159">Fabrikam の支払が Fabrikam East の請求書で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-159">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="04c5f-160">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-160">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-161">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-161">Account</span></span>                         | <span data-ttu-id="04c5f-162">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-162">Debit amount</span></span> | <span data-ttu-id="04c5f-163">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-163">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-164">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-164">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="04c5f-165">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-165">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-166">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-166">Due to Fabrikam East (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-167">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-167">600.00</span></span>        |

<span data-ttu-id="04c5f-168">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-168">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-169">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-169">Account</span></span>                             | <span data-ttu-id="04c5f-170">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-170">Debit amount</span></span> | <span data-ttu-id="04c5f-171">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-171">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-172">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-172">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="04c5f-173">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-173">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-174">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-174">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-175">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-175">600.00</span></span>        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="04c5f-176">例 2: 現金割引のある別の法人からの請求書の顧客支払</span><span class="sxs-lookup"><span data-stu-id="04c5f-176">Example 2: Customer payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="04c5f-177">Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について 580.00 の支払を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-177">Fabrikam receives a payment of 580.00 for Fabrikam customer 4000, Northwind Traders.</span></span> <span data-ttu-id="04c5f-178">Fabrikam East には、顧客 4000 の未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-178">Fabrikam East has an open invoice for customer 4000.</span></span> <span data-ttu-id="04c5f-179">請求書には 20.00 の現金割引があります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="04c5f-180">支払は、未処理の Fabrikam East 請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-180">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="04c5f-181">現金割引が請求書、Fabrikam East の法人に転記されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-181">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a><span data-ttu-id="04c5f-182">Fabrikam East の顧客 4000 について請求書が Fabrikam East で転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-182">Invoice is posted in Fabrikam East for Fabrikam East customer 4000</span></span>

| <span data-ttu-id="04c5f-183">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-183">Account</span></span>                             | <span data-ttu-id="04c5f-184">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-184">Debit amount</span></span> | <span data-ttu-id="04c5f-185">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-185">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-186">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-186">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-187">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-187">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-188">売上 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-188">Sales (Fabrikam East)</span></span>               |              | <span data-ttu-id="04c5f-189">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-189">600.00</span></span>        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a><span data-ttu-id="04c5f-190">Fabrikam 顧客 4000 について支払が Fabrikam で受領および転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-190">Payment is received and posted in Fabrikam for Fabrikam customer 4000</span></span>

| <span data-ttu-id="04c5f-191">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-191">Account</span></span>                        | <span data-ttu-id="04c5f-192">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-192">Debit amount</span></span> | <span data-ttu-id="04c5f-193">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-193">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-194">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-194">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-195">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-195">600.00</span></span>       |               |
| <span data-ttu-id="04c5f-196">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-196">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-197">600.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-197">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="04c5f-198">Fabrikam の支払が Fabrikam East の請求書で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-198">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="04c5f-199">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-199">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-200">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-200">Account</span></span>                         | <span data-ttu-id="04c5f-201">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-201">Debit amount</span></span> | <span data-ttu-id="04c5f-202">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-202">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-203">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-203">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="04c5f-204">580.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-204">580.00</span></span>       |               |
| <span data-ttu-id="04c5f-205">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-205">Due to Fabrikam East (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-206">580.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-206">580.00</span></span>        |

<span data-ttu-id="04c5f-207">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-207">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-208">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-208">Account</span></span>                             | <span data-ttu-id="04c5f-209">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-209">Debit amount</span></span> | <span data-ttu-id="04c5f-210">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-210">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-211">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-211">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="04c5f-212">580.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-212">580.00</span></span>       |               |
| <span data-ttu-id="04c5f-213">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-213">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-214">580.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-214">580.00</span></span>        |
| <span data-ttu-id="04c5f-215">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-215">Cash discount (Fabrikam East)</span></span>       | <span data-ttu-id="04c5f-216">20.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-216">20.00</span></span>        |               |
| <span data-ttu-id="04c5f-217">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-217">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-218">20.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-218">20.00</span></span>         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a><span data-ttu-id="04c5f-219">例 3: 実為替レート差益のある別の法人からの請求書の顧客支払</span><span class="sxs-lookup"><span data-stu-id="04c5f-219">Example 3: Customer payment of invoice from another legal entity with realized exchange rate gain</span></span>
<span data-ttu-id="04c5f-220">Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について 600.00 EUR の支払を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-220">Fabrikam receives a payment of 600.00 euros (EUR) for Fabrikam customer 4000, Northwind Traders.</span></span> <span data-ttu-id="04c5f-221">支払は、Fabrikam East の顧客 4000 に対する未処理請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-221">The payment is settled with an open invoice for customer 4000 in Fabrikam East.</span></span> <span data-ttu-id="04c5f-222">決済プロセス時に、通貨為替差益トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-222">A currency exchange gain transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="04c5f-223">請求日時点での EUR から米国ドル (USD) への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="04c5f-223">Exchange rate for EUR to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="04c5f-224">支払日時点での EUR から USD への為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="04c5f-224">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a><span data-ttu-id="04c5f-225">Fabrikam East の顧客 4000 について請求書が Fabrikam East で転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-225">Invoice is posted in Fabrikam East for Fabrikam East customer 4000</span></span>

| <span data-ttu-id="04c5f-226">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-226">Account</span></span>                             | <span data-ttu-id="04c5f-227">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-227">Debit amount</span></span>            | <span data-ttu-id="04c5f-228">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-228">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-229">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-229">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-230">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-230">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="04c5f-231">売上 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-231">Sales (Fabrikam East)</span></span>               |                         | <span data-ttu-id="04c5f-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-232">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a><span data-ttu-id="04c5f-233">Fabrikam の顧客 4000 について支払が Fabrikam で受領および転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-233">Payment is received and posted in Fabrikam for Fabrikam customer 4000</span></span>

| <span data-ttu-id="04c5f-234">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-234">Account</span></span>                        | <span data-ttu-id="04c5f-235">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-235">Debit amount</span></span>            | <span data-ttu-id="04c5f-236">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-236">Credit amount</span></span>           |
|--------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-237">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-237">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-238">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-238">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="04c5f-239">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-239">Accounts receivable (Fabrikam)</span></span> |                         | <span data-ttu-id="04c5f-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-240">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="04c5f-241">Fabrikam の支払が Fabrikam East の請求書で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-241">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="04c5f-242">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-242">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-243">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-243">Account</span></span>                         | <span data-ttu-id="04c5f-244">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-244">Debit amount</span></span>            | <span data-ttu-id="04c5f-245">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-245">Credit amount</span></span>           |
|---------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-246">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-246">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="04c5f-247">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-247">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="04c5f-248">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-248">Due to Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="04c5f-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-249">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="04c5f-250">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-250">Due to Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="04c5f-251">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-251">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="04c5f-252">実利益 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-252">Realized gain (Fabrikam)</span></span>        |                         | <span data-ttu-id="04c5f-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-253">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="04c5f-254">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-254">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-255">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-255">Account</span></span>                             | <span data-ttu-id="04c5f-256">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-256">Debit amount</span></span>            | <span data-ttu-id="04c5f-257">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-257">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-258">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-258">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="04c5f-259">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-259">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="04c5f-260">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-260">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="04c5f-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-261">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="04c5f-262">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-262">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-263">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-263">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="04c5f-264">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-264">Due from Fabrikam (Fabrikam East)</span></span>   |                         | <span data-ttu-id="04c5f-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-265">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a><span data-ttu-id="04c5f-266">例 4: 現金割引と実為替レート差益のある別の法人からの請求書の顧客支払</span><span class="sxs-lookup"><span data-stu-id="04c5f-266">Example 4: Customer payment of invoice from another legal entity with cash discount and realized exchange rate gain</span></span>
<span data-ttu-id="04c5f-267">Fabrikam は、Fabrikam 顧客 4000 の Northwind Traders について、Fabrikam East での未処理請求書の支払を転記します。</span><span class="sxs-lookup"><span data-stu-id="04c5f-267">Fabrikam posts a payment for Fabrikam customer 4000, Northwind Traders, for an open invoice in Fabrikam East.</span></span> <span data-ttu-id="04c5f-268">請求書には現金割引があり、売上税トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-268">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="04c5f-269">支払は、未処理の Fabrikam East 請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-269">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="04c5f-270">決済プロセス時に、通貨為替差益トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-270">A currency exchange gain transaction is generated during the settlement process.</span></span> <span data-ttu-id="04c5f-271">現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差益が支払の法人 (Fabrikam) に転記されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-271">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange gain is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="04c5f-272">請求日時点での EUR から USD への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="04c5f-272">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="04c5f-273">支払日時点での EUR から USD への為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="04c5f-273">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a><span data-ttu-id="04c5f-274">顧客 4000 について、Fabrikam East で自由書式の請求書が転記され、税金トランザクションが生成される</span><span class="sxs-lookup"><span data-stu-id="04c5f-274">Free text invoice is posted and a tax transaction is generated in Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="04c5f-275">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-275">Account</span></span>                             | <span data-ttu-id="04c5f-276">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-276">Debit amount</span></span>            | <span data-ttu-id="04c5f-277">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-277">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-278">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-278">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-279">638.22 EUR / 769.82 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-279">638.22 EUR / 769.82 USD</span></span> |                         |
| <span data-ttu-id="04c5f-280">売上 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-280">Sales (Fabrikam East)</span></span>               |                         | <span data-ttu-id="04c5f-281">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-281">600.00 EUR / 723.72 USD</span></span> |
| <span data-ttu-id="04c5f-282">売上税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-282">Sales tax (Fabrikam East)</span></span>           |                         | <span data-ttu-id="04c5f-283">38.22 EUR / 46.10 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-283">38.22 EUR / 46.10 USD</span></span>   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a><span data-ttu-id="04c5f-284">顧客 4000 について支払が Fabrikam で受領および転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-284">Payment is received and posted in Fabrikam for customer 4000</span></span>

| <span data-ttu-id="04c5f-285">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-285">Account</span></span>                        | <span data-ttu-id="04c5f-286">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-286">Debit amount</span></span>            | <span data-ttu-id="04c5f-287">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-287">Credit amount</span></span>           |
|--------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-288">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-288">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-289">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-289">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="04c5f-290">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-290">Accounts receivable (Fabrikam)</span></span> |                         | <span data-ttu-id="04c5f-291">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-291">626.22 EUR / 768.81 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="04c5f-292">Fabrikam の支払が Fabrikam East の請求書で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-292">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="04c5f-293">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-293">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-294">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-294">Account</span></span>                         | <span data-ttu-id="04c5f-295">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-295">Debit amount</span></span>            | <span data-ttu-id="04c5f-296">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-296">Credit amount</span></span>           |
|---------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-297">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-297">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="04c5f-298">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-298">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="04c5f-299">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-299">Due to Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="04c5f-300">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-300">626.22 EUR / 768.81 USD</span></span> |
| <span data-ttu-id="04c5f-301">Fabrikam East への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-301">Due to Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="04c5f-302">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-302">0.00 EUR / 13.46 USD</span></span>    |                         |
| <span data-ttu-id="04c5f-303">実利益 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-303">Realized gain (Fabrikam)</span></span>        |                         | <span data-ttu-id="04c5f-304">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-304">0.00 EUR / 13.46 USD</span></span>    |

<span data-ttu-id="04c5f-305">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-305">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-306">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-306">Account</span></span>                             | <span data-ttu-id="04c5f-307">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-307">Debit amount</span></span>            | <span data-ttu-id="04c5f-308">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-308">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="04c5f-309">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-309">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="04c5f-310">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-310">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="04c5f-311">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-311">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="04c5f-312">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-312">626.22 EUR / 768.81 USD</span></span> |
| <span data-ttu-id="04c5f-313">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-313">Accounts receivable (Fabrikam East</span></span>  | <span data-ttu-id="04c5f-314">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-314">0.00 EUR / 13.46 USD</span></span>    |                         |
| <span data-ttu-id="04c5f-315">Fabrikam からの借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-315">Due from Fabrikam (Fabrikam East)</span></span>   |                         | <span data-ttu-id="04c5f-316">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-316">0.00 EUR / 13.46 USD</span></span>    |
| <span data-ttu-id="04c5f-317">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-317">Cash discount (Fabrikam East)</span></span>       | <span data-ttu-id="04c5f-318">12.00 EUR / 14.47 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-318">12.00 EUR / 14.47 USD</span></span>   |                         |
| <span data-ttu-id="04c5f-319">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-319">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="04c5f-320">12.00 EUR / 14.47 USD</span><span class="sxs-lookup"><span data-stu-id="04c5f-320">12.00 EUR / 14.47 USD</span></span>   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a><span data-ttu-id="04c5f-321">例 5 : 基本支払のある顧客貸方票</span><span class="sxs-lookup"><span data-stu-id="04c5f-321">Example 5: Customer credit note with primary payment</span></span>
<span data-ttu-id="04c5f-322">Fabrikam は、顧客 4000 の Northwind Traders について 75.00 の支払を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-322">Fabrikam receives a payment of 75.00 from customer 4000, Northwind Traders.</span></span> <span data-ttu-id="04c5f-323">支払は、Fabrikam West の顧客 10000 に対する未処理請求書および Fabrikam East の顧客 4000 に対する未処理の貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-323">The payment is settled with an open invoice for Fabrikam West customer 10000 and an open credit note for Fabrikam East customer 4000.</span></span> <span data-ttu-id="04c5f-324">支払は、**トランザクションの決済** ページで基本支払として選択されています。</span><span class="sxs-lookup"><span data-stu-id="04c5f-324">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a><span data-ttu-id="04c5f-325">顧客 10000 について請求書が Fabrikam West に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-325">Invoice is posted to Fabrikam West for customer 10000</span></span>

| <span data-ttu-id="04c5f-326">口座</span><span class="sxs-lookup"><span data-stu-id="04c5f-326">Account</span></span>                             | <span data-ttu-id="04c5f-327">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-327">Debit amount</span></span> | <span data-ttu-id="04c5f-328">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-328">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-329">売掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-329">Accounts receivable (Fabrikam West)</span></span> | <span data-ttu-id="04c5f-330">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-330">100.00</span></span>       |               |
| <span data-ttu-id="04c5f-331">売上 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-331">Sales (Fabrikam West)</span></span>               |              | <span data-ttu-id="04c5f-332">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-332">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a><span data-ttu-id="04c5f-333">顧客 4000 について貸方票が Fabrikam East に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-333">Credit note is posted to Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="04c5f-334">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-334">Account</span></span>                             | <span data-ttu-id="04c5f-335">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-335">Debit amount</span></span> | <span data-ttu-id="04c5f-336">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-336">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-337">売上返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-337">Sales returns (Fabrikam East)</span></span>       | <span data-ttu-id="04c5f-338">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-338">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-339">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-339">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-340">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-340">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a><span data-ttu-id="04c5f-341">顧客 4000 について支払が Fabrikam に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-341">Payment is posted to Fabrikam for customer 4000</span></span>

| <span data-ttu-id="04c5f-342">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-342">Account</span></span>                        | <span data-ttu-id="04c5f-343">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-343">Debit amount</span></span> | <span data-ttu-id="04c5f-344">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-344">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-345">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-345">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-346">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-346">75.00</span></span>        |               |
| <span data-ttu-id="04c5f-347">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-347">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-348">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-348">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="04c5f-349">Fabrikam の支払が、Fabrikam West の請求書と Fabrikam East の貸方票で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-349">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="04c5f-350">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-350">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-351">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-351">Account</span></span>                           | <span data-ttu-id="04c5f-352">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-352">Debit amount</span></span> | <span data-ttu-id="04c5f-353">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-353">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-354">Fabrikam East からの借り (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-354">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="04c5f-355">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-355">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-356">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-356">Accounts receivable (Fabrikam)</span></span>    |              | <span data-ttu-id="04c5f-357">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-357">25.00</span></span>         |
| <span data-ttu-id="04c5f-358">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-358">Accounts receivable (Fabrikam)</span></span>    | <span data-ttu-id="04c5f-359">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-359">100.00</span></span>       |               |
| <span data-ttu-id="04c5f-360">Fabrikam West への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-360">Due to Fabrikam West (Fabrikam)</span></span>   |              | <span data-ttu-id="04c5f-361">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-361">100.00</span></span>        |

<span data-ttu-id="04c5f-362">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-362">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-363">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-363">Account</span></span>                             | <span data-ttu-id="04c5f-364">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-364">Debit amount</span></span> | <span data-ttu-id="04c5f-365">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-365">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-366">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-366">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="04c5f-367">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-367">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-368">Fabrikam への貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-368">Due to Fabrikam (Fabrikam East)</span></span>     |              | <span data-ttu-id="04c5f-369">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-369">25.00</span></span>         |

<span data-ttu-id="04c5f-370">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-370">**Fabrikam West posting**</span></span>

| <span data-ttu-id="04c5f-371">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-371">Account</span></span>                             | <span data-ttu-id="04c5f-372">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-372">Debit amount</span></span> | <span data-ttu-id="04c5f-373">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-373">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-374">Fabrikam からの借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-374">Due from Fabrikam (Fabrikam West)</span></span>   | <span data-ttu-id="04c5f-375">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-375">100.00</span></span>       |               |
| <span data-ttu-id="04c5f-376">売掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-376">Accounts receivable (Fabrikam West)</span></span> |              | <span data-ttu-id="04c5f-377">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-377">100.00</span></span>        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a><span data-ttu-id="04c5f-378">例 6 : 基本支払のない顧客貸方票</span><span class="sxs-lookup"><span data-stu-id="04c5f-378">Example 6: Customer credit note without primary payment</span></span>
<span data-ttu-id="04c5f-379">Fabrikam は、顧客 4000 の Northwind Traders について 75.00 の支払を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="04c5f-379">Fabrikam receives a payment of 75.00 from customer 4000, Northwind Traders.</span></span> <span data-ttu-id="04c5f-380">支払は、Fabrikam West の顧客 10000 に対する未処理請求書および Fabrikam East の顧客 4000 に対する未処理の貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="04c5f-380">The payment is settled with an open invoice for Fabrikam West customer 10000 and an open credit note for Fabrikam East customer 4000.</span></span> <span data-ttu-id="04c5f-381">支払は、**トランザクションの決済** ページでは基本支払として選択されません。</span><span class="sxs-lookup"><span data-stu-id="04c5f-381">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a><span data-ttu-id="04c5f-382">顧客 10000 について請求書が Fabrikam West に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-382">Invoice is posted to Fabrikam West for customer 10000</span></span>

| <span data-ttu-id="04c5f-383">口座</span><span class="sxs-lookup"><span data-stu-id="04c5f-383">Account</span></span>                             | <span data-ttu-id="04c5f-384">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-384">Debit amount</span></span> | <span data-ttu-id="04c5f-385">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-385">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-386">売掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-386">Accounts receivable (Fabrikam West)</span></span> | <span data-ttu-id="04c5f-387">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-387">100.00</span></span>       |               |
| <span data-ttu-id="04c5f-388">売上 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-388">Sales (Fabrikam West)</span></span>               |              | <span data-ttu-id="04c5f-389">100.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-389">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a><span data-ttu-id="04c5f-390">顧客 4000 について貸方票が Fabrikam East に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-390">Credit note is posted to Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="04c5f-391">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-391">Account</span></span>                             | <span data-ttu-id="04c5f-392">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-392">Debit amount</span></span> | <span data-ttu-id="04c5f-393">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-393">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-394">売上返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-394">Sales returns (Fabrikam East)</span></span>       | <span data-ttu-id="04c5f-395">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-395">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-396">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-396">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-397">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-397">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a><span data-ttu-id="04c5f-398">顧客 4000 について支払が Fabrikam に転記される</span><span class="sxs-lookup"><span data-stu-id="04c5f-398">Payment is posted to Fabrikam for customer 4000</span></span>

| <span data-ttu-id="04c5f-399">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-399">Account</span></span>                        | <span data-ttu-id="04c5f-400">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-400">Debit amount</span></span> | <span data-ttu-id="04c5f-401">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-401">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-402">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-402">Cash (Fabrikam)</span></span>                | <span data-ttu-id="04c5f-403">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-403">75.00</span></span>        |               |
| <span data-ttu-id="04c5f-404">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-404">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-405">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-405">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="04c5f-406">Fabrikam の支払が、Fabrikam West の請求書と Fabrikam East の貸方票で決済される</span><span class="sxs-lookup"><span data-stu-id="04c5f-406">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="04c5f-407">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-407">**Fabrikam posting**</span></span>

| <span data-ttu-id="04c5f-408">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-408">Account</span></span>                         | <span data-ttu-id="04c5f-409">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-409">Debit amount</span></span> | <span data-ttu-id="04c5f-410">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-410">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-411">売掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-411">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="04c5f-412">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-412">75.00</span></span>        |               |
| <span data-ttu-id="04c5f-413">Fabrikam West への貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="04c5f-413">Due to Fabrikam West (Fabrikam)</span></span> |              | <span data-ttu-id="04c5f-414">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-414">75.00</span></span>         |

<span data-ttu-id="04c5f-415">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-415">**Fabrikam East posting**</span></span>

| <span data-ttu-id="04c5f-416">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-416">Account</span></span>                              | <span data-ttu-id="04c5f-417">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-417">Debit amount</span></span> | <span data-ttu-id="04c5f-418">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-418">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-419">売掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-419">Accounts receivable (Fabrikam East)</span></span>  | <span data-ttu-id="04c5f-420">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-420">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-421">Fabrikam West への貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="04c5f-421">Due to Fabrikam West (Fabrikam East)</span></span> |              | <span data-ttu-id="04c5f-422">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-422">25.00</span></span>         |

<span data-ttu-id="04c5f-423">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="04c5f-423">**Fabrikam West posting**</span></span>

| <span data-ttu-id="04c5f-424">アカウント</span><span class="sxs-lookup"><span data-stu-id="04c5f-424">Account</span></span>                                | <span data-ttu-id="04c5f-425">借方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-425">Debit amount</span></span> | <span data-ttu-id="04c5f-426">貸方金額</span><span class="sxs-lookup"><span data-stu-id="04c5f-426">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="04c5f-427">Fabrikam からの借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-427">Due from Fabrikam (Fabrikam West)</span></span>      | <span data-ttu-id="04c5f-428">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-428">75.00</span></span>        |               |
| <span data-ttu-id="04c5f-429">売掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-429">Accounts receivable (Fabrikam West)</span></span>    |              | <span data-ttu-id="04c5f-430">75.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-430">75.00</span></span>         |
| <span data-ttu-id="04c5f-431">Fabrikam East からの借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-431">Due from Fabrikam East (Fabrikam West)</span></span> | <span data-ttu-id="04c5f-432">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-432">25.00</span></span>        |               |
| <span data-ttu-id="04c5f-433">売掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="04c5f-433">Accounts receivable (Fabrikam West)</span></span>    |              | <span data-ttu-id="04c5f-434">25.00</span><span class="sxs-lookup"><span data-stu-id="04c5f-434">25.00</span></span>         |






