---
title: "買掛金勘定の集中支払"
description: "複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。 したがって、同じ支払を複数の法人に入力する必要はありません。 この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 54329582abd36a8ca896ce731ce06ca4de58bbb0
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="centralized-payments-for-accounts-payable"></a><span data-ttu-id="4ed89-105">買掛金勘定の集中支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-105">Centralized payments for Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4ed89-106">複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="4ed89-107">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4ed89-107">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="4ed89-108">この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="4ed89-109">複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="4ed89-110">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4ed89-110">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="4ed89-111">また、組織では、支払プロセスが合理化されるため、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-111">Additionally, the organization saves time, because the payment process is streamlined.</span></span>

<span data-ttu-id="4ed89-112">集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの仕入先請求書を管理します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-112">In a centralized payments organization, there are many legal entities for operations, and each operating legal entity manages its own vendor invoices.</span></span> <span data-ttu-id="4ed89-113">事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人から行われます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-113">Payments for all the operating legal entities are generated from a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="4ed89-114">決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="4ed89-115">組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、会社間支払に関連する現金割引トランザクションの処理方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a cross-company payment are handled.</span></span> 

<span data-ttu-id="4ed89-116">次の各例で、さまざまなシナリオにおける転記の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="4ed89-117">これらすべての例について、次の構成が想定されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="4ed89-118">法人は Fabrikam、Fabrikam East、および Fabrikam West です。</span><span class="sxs-lookup"><span data-stu-id="4ed89-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="4ed89-119">支払は、Fabrikam で構成されています。</span><span class="sxs-lookup"><span data-stu-id="4ed89-119">Payments are made from Fabrikam.</span></span>
-   <span data-ttu-id="4ed89-120">[**会社間会計**] ページの [**現金割引の転記**] フィールドには**請求書の法人**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="4ed89-121">[**会社間会計**] ページの [**為替差益または差損の転記**] フィールドには**請求書の支払**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="4ed89-122">仕入先の Fourth Coffee は、各法人の仕入先として設定されています。</span><span class="sxs-lookup"><span data-stu-id="4ed89-122">The vendor Fourth Coffee is set up as a vendor in each legal entity.</span></span> <span data-ttu-id="4ed89-123">異なる法人の仕入先は同一のグローバル アドレス帳 ID を共有するため、同じ仕入先として識別されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-123">The vendors from the various legal entities are identified as the same vendor because they share the same global address book ID.</span></span>

| <span data-ttu-id="4ed89-124">ディレクトリ ID</span><span class="sxs-lookup"><span data-stu-id="4ed89-124">Directory ID</span></span> | <span data-ttu-id="4ed89-125">仕入先</span><span class="sxs-lookup"><span data-stu-id="4ed89-125">Vendor account</span></span> | <span data-ttu-id="4ed89-126">氏名</span><span class="sxs-lookup"><span data-stu-id="4ed89-126">Name</span></span>          | <span data-ttu-id="4ed89-127">個法</span><span class="sxs-lookup"><span data-stu-id="4ed89-127">Legal entity</span></span>  |
|--------------|----------------|---------------|---------------|
| <span data-ttu-id="4ed89-128">1050</span><span class="sxs-lookup"><span data-stu-id="4ed89-128">1050</span></span>         | <span data-ttu-id="4ed89-129">3004</span><span class="sxs-lookup"><span data-stu-id="4ed89-129">3004</span></span>           | <span data-ttu-id="4ed89-130">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="4ed89-130">Fourth Coffee</span></span> | <span data-ttu-id="4ed89-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="4ed89-131">Fabrikam</span></span>      |
| <span data-ttu-id="4ed89-132">1050</span><span class="sxs-lookup"><span data-stu-id="4ed89-132">1050</span></span>         | <span data-ttu-id="4ed89-133">100</span><span class="sxs-lookup"><span data-stu-id="4ed89-133">100</span></span>            | <span data-ttu-id="4ed89-134">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="4ed89-134">Fourth Coffee</span></span> | <span data-ttu-id="4ed89-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="4ed89-135">Fabrikam East</span></span> |
| <span data-ttu-id="4ed89-136">1050</span><span class="sxs-lookup"><span data-stu-id="4ed89-136">1050</span></span>         | <span data-ttu-id="4ed89-137">3004</span><span class="sxs-lookup"><span data-stu-id="4ed89-137">3004</span></span>           | <span data-ttu-id="4ed89-138">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="4ed89-138">Fourth Coffee</span></span> | <span data-ttu-id="4ed89-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="4ed89-139">Fabrikam West</span></span> |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="4ed89-140">例 1 : 別の法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-140">Example 1: Vendor payment of invoice from another legal entity</span></span>
<span data-ttu-id="4ed89-141">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="4ed89-141">Fabrikam East has an open invoice for vendor account 100, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-142">Fabrikam は、支払を入力し、Fabrikam 仕入先 3004 の Fourth Coffee に転記します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-142">Fabrikam enters and posts a payment to Fabrikam vendor account 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-143">支払は、未処理請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-143">The payment is settled with the open invoice.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="4ed89-144">仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="4ed89-144">Invoice is posted in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="4ed89-145">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-145">Account</span></span>                          | <span data-ttu-id="4ed89-146">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-146">Debit amount</span></span> | <span data-ttu-id="4ed89-147">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-147">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-148">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-148">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="4ed89-149">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-149">600.00</span></span>       |               |
| <span data-ttu-id="4ed89-150">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-150">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="4ed89-151">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-151">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="4ed89-152">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-152">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="4ed89-153">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-153">Account</span></span>                     | <span data-ttu-id="4ed89-154">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-154">Debit amount</span></span> | <span data-ttu-id="4ed89-155">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-155">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-156">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-156">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-157">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-157">600.00</span></span>       |               |
| <span data-ttu-id="4ed89-158">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-158">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="4ed89-159">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-159">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="4ed89-160">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-160">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="4ed89-161">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-161">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-162">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-162">Account</span></span>                           | <span data-ttu-id="4ed89-163">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-163">Debit amount</span></span> | <span data-ttu-id="4ed89-164">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-164">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-165">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-165">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="4ed89-166">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-166">600.00</span></span>       |               |
| <span data-ttu-id="4ed89-167">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-167">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="4ed89-168">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-168">600.00</span></span>        |

<span data-ttu-id="4ed89-169">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-169">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-170">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-170">Account</span></span>                          | <span data-ttu-id="4ed89-171">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-171">Debit amount</span></span> | <span data-ttu-id="4ed89-172">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-172">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-173">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-173">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-174">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-174">600.00</span></span>       |               |
| <span data-ttu-id="4ed89-175">Fabrikam への貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-175">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="4ed89-176">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-176">600.00</span></span>        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="4ed89-177">例 2 : 現金割引のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-177">Example 2: Vendor payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="4ed89-178">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="4ed89-178">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-179">請求書では、20.00 の現金割引を利用できます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="4ed89-180">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する 580.00 の支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-180">Fabrikam enters and posts a payment of 580.00 for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-181">支払は、未処理の Fabrikam East 請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-181">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="4ed89-182">現金割引が請求書、Fabrikam East の法人に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-182">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="4ed89-183">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="4ed89-183">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="4ed89-184">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-184">Account</span></span>                          | <span data-ttu-id="4ed89-185">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-185">Debit amount</span></span> | <span data-ttu-id="4ed89-186">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-186">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-187">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-187">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="4ed89-188">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-188">600.00</span></span>       |               |
| <span data-ttu-id="4ed89-189">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-189">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="4ed89-190">600.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-190">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="4ed89-191">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-191">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="4ed89-192">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-192">Account</span></span>                     | <span data-ttu-id="4ed89-193">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-193">Debit amount</span></span> | <span data-ttu-id="4ed89-194">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-194">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-195">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-195">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-196">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-196">580.00</span></span>       |               |
| <span data-ttu-id="4ed89-197">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-197">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="4ed89-198">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-198">580.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="4ed89-199">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-199">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="4ed89-200">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-200">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-201">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-201">Account</span></span>                           | <span data-ttu-id="4ed89-202">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-202">Debit amount</span></span> | <span data-ttu-id="4ed89-203">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-203">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-204">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-204">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="4ed89-205">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-205">580.00</span></span>       |               |
| <span data-ttu-id="4ed89-206">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-206">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="4ed89-207">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-207">580.00</span></span>        |

<span data-ttu-id="4ed89-208">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-208">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-209">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-209">Account</span></span>                          | <span data-ttu-id="4ed89-210">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-210">Debit amount</span></span> | <span data-ttu-id="4ed89-211">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-211">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-212">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-212">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-213">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-213">580.00</span></span>       |               |
| <span data-ttu-id="4ed89-214">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-214">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="4ed89-215">580.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-215">580.00</span></span>        |
| <span data-ttu-id="4ed89-216">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-216">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-217">20.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-217">20.00</span></span>        |               |
| <span data-ttu-id="4ed89-218">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-218">Cash discount (Fabrikam East)</span></span>    |              | <span data-ttu-id="4ed89-219">20.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-219">20.00</span></span>         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a><span data-ttu-id="4ed89-220">例 3 : 実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-220">Example 3: Vendor payment of invoice from another legal entity with realized exchange rate loss</span></span>
<span data-ttu-id="4ed89-221">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="4ed89-221">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-222">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-222">Fabrikam enters and posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-223">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-223">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="4ed89-224">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-224">A currency exchange loss transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="4ed89-225">請求日時点でのユーロ (EUR) から米国ドル (USD) への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="4ed89-225">Exchange rate for euros (EUR) to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="4ed89-226">支払日時点での EUR から USD への為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="4ed89-226">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="4ed89-227">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="4ed89-227">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="4ed89-228">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-228">Account</span></span>                          | <span data-ttu-id="4ed89-229">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-229">Debit amount</span></span>            | <span data-ttu-id="4ed89-230">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-230">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-231">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-231">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="4ed89-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-232">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="4ed89-233">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-233">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="4ed89-234">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-234">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="4ed89-235">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-235">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="4ed89-236">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-236">Account</span></span>                     | <span data-ttu-id="4ed89-237">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-237">Debit amount</span></span>            | <span data-ttu-id="4ed89-238">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-238">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-239">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-239">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-240">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="4ed89-241">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-241">Cash (Fabrikam)</span></span>             |                         | <span data-ttu-id="4ed89-242">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-242">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="4ed89-243">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-243">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="4ed89-244">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-244">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-245">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-245">Account</span></span>                           | <span data-ttu-id="4ed89-246">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-246">Debit amount</span></span>            | <span data-ttu-id="4ed89-247">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-247">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-248">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-248">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="4ed89-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-249">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="4ed89-250">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-250">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="4ed89-251">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-251">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="4ed89-252">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-252">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="4ed89-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-253">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="4ed89-254">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-254">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="4ed89-255">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-255">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="4ed89-256">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-256">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-257">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-257">Account</span></span>                          | <span data-ttu-id="4ed89-258">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-258">Debit amount</span></span>            | <span data-ttu-id="4ed89-259">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-259">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-260">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-260">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-261">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="4ed89-262">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-262">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="4ed89-263">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-263">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="4ed89-264">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-264">Due to Fabrikam (Fabrikam East)</span></span>  | <span data-ttu-id="4ed89-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-265">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="4ed89-266">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-266">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="4ed89-267">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-267">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a><span data-ttu-id="4ed89-268">例 4 : 現金割引と実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-268">Example 4: Vendor payment of invoice from another legal entity with cash discount and realized exchange rate loss</span></span>
<span data-ttu-id="4ed89-269">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="4ed89-269">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-270">請求書には現金割引があり、売上税トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-270">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="4ed89-271">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を転記します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-271">Fabrikam posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-272">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-272">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="4ed89-273">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-273">A currency exchange loss transaction is generated during the settlement process.</span></span> <span data-ttu-id="4ed89-274">現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差損が支払の法人 (Fabrikam) に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-274">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange loss is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="4ed89-275">請求日時点での EUR から USD への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="4ed89-275">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="4ed89-276">支払日時点での USD に対する EUR の為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="4ed89-276">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="4ed89-277">仕入先 100 に対して Fabrikam East で転記される請求書および生成される税トランザクション</span><span class="sxs-lookup"><span data-stu-id="4ed89-277">Invoice is posted and a tax transaction is generated in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="4ed89-278">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-278">Account</span></span>                          | <span data-ttu-id="4ed89-279">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-279">Debit amount</span></span>            | <span data-ttu-id="4ed89-280">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-280">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-281">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-281">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="4ed89-282">564.07 EUR / 680.38 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-282">564.07 EUR / 680.38 USD</span></span> |                         |
| <span data-ttu-id="4ed89-283">売上税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-283">Sales tax (Fabrikam East)</span></span>        | <span data-ttu-id="4ed89-284">35.93 EUR / 43.34 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-284">35.93 EUR / 43.34 USD</span></span>   |                         |
| <span data-ttu-id="4ed89-285">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-285">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="4ed89-286">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-286">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="4ed89-287">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-287">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="4ed89-288">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-288">Account</span></span>                     | <span data-ttu-id="4ed89-289">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-289">Debit amount</span></span>            | <span data-ttu-id="4ed89-290">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-290">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-291">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-291">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-292">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-292">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="4ed89-293">現金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-293">Cash (Fabrikam East)</span></span>        |                         | <span data-ttu-id="4ed89-294">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-294">588.72 EUR / 722.77 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="4ed89-295">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-295">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="4ed89-296">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-296">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-297">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-297">Account</span></span>                           | <span data-ttu-id="4ed89-298">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-298">Debit amount</span></span>            | <span data-ttu-id="4ed89-299">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-299">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-300">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-300">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="4ed89-301">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-301">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="4ed89-302">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-302">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="4ed89-303">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-303">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="4ed89-304">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-304">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="4ed89-305">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-305">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="4ed89-306">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-306">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="4ed89-307">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-307">0.00 EUR / 12.66 USD</span></span>    |

<span data-ttu-id="4ed89-308">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-308">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-309">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-309">Account</span></span>                          | <span data-ttu-id="4ed89-310">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-310">Debit amount</span></span>            | <span data-ttu-id="4ed89-311">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-311">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="4ed89-312">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-312">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-313">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-313">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="4ed89-314">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-314">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="4ed89-315">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-315">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="4ed89-316">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-316">Due to Fabrikam (Fabrikam East</span></span>   | <span data-ttu-id="4ed89-317">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-317">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="4ed89-318">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-318">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="4ed89-319">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-319">0.00 EUR / 12.66 USD</span></span>    |
| <span data-ttu-id="4ed89-320">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-320">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-321">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-321">11.28 EUR / 13.61 USD</span></span>   |                         |
| <span data-ttu-id="4ed89-322">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-322">Cash discount (Fabrikam East)</span></span>    |                         | <span data-ttu-id="4ed89-323">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="4ed89-323">11.28 EUR / 13.61 USD</span></span>   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a><span data-ttu-id="4ed89-324">例 5 : 基本支払のある仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="4ed89-324">Example 5: Vendor credit note with primary payment</span></span>
<span data-ttu-id="4ed89-325">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-325">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-326">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-326">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="4ed89-327">支払は、**トランザクションの決済** ページで基本支払として選択されています。</span><span class="sxs-lookup"><span data-stu-id="4ed89-327">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="4ed89-328">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="4ed89-328">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="4ed89-329">口座</span><span class="sxs-lookup"><span data-stu-id="4ed89-329">Account</span></span>                          | <span data-ttu-id="4ed89-330">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-330">Debit amount</span></span> | <span data-ttu-id="4ed89-331">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-331">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-332">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-332">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="4ed89-333">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-333">100.00</span></span>       |               |
| <span data-ttu-id="4ed89-334">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-334">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="4ed89-335">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-335">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="4ed89-336">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="4ed89-336">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="4ed89-337">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-337">Account</span></span>                          | <span data-ttu-id="4ed89-338">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-338">Debit amount</span></span> | <span data-ttu-id="4ed89-339">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-339">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-340">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-340">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-341">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-341">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-342">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-342">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="4ed89-343">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-343">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="4ed89-344">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-344">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="4ed89-345">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-345">Account</span></span>                     | <span data-ttu-id="4ed89-346">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-346">Debit amount</span></span> | <span data-ttu-id="4ed89-347">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-347">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-348">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-348">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-349">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-349">75.00</span></span>        |               |
| <span data-ttu-id="4ed89-350">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-350">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="4ed89-351">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-351">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="4ed89-352">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-352">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="4ed89-353">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-353">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-354">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-354">Account</span></span>                           | <span data-ttu-id="4ed89-355">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-355">Debit amount</span></span> | <span data-ttu-id="4ed89-356">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-356">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-357">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-357">Accounts payable (Fabrikam)</span></span>       | <span data-ttu-id="4ed89-358">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-358">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-359">Fabrikam East 借り (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-359">Due to Fabrikam East (Fabrikam)</span></span>   |              | <span data-ttu-id="4ed89-360">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-360">25.00</span></span>         |
| <span data-ttu-id="4ed89-361">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-361">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="4ed89-362">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-362">100.00</span></span>       |               |
| <span data-ttu-id="4ed89-363">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-363">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="4ed89-364">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-364">100.00</span></span>        |

<span data-ttu-id="4ed89-365">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-365">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-366">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-366">Account</span></span>                           | <span data-ttu-id="4ed89-367">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-367">Debit amount</span></span> | <span data-ttu-id="4ed89-368">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-368">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-369">Fabrikam 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-369">Due from Fabrikam (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-370">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-370">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-371">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-371">Accounts payable (Fabrikam East)</span></span>  |              | <span data-ttu-id="4ed89-372">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-372">25.00</span></span>         |

<span data-ttu-id="4ed89-373">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-373">**Fabrikam West posting**</span></span>

| <span data-ttu-id="4ed89-374">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-374">Account</span></span>                          | <span data-ttu-id="4ed89-375">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-375">Debit amount</span></span> | <span data-ttu-id="4ed89-376">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-376">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-377">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-377">Accounts payable (Fabrikam West)</span></span> | <span data-ttu-id="4ed89-378">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-378">100.00</span></span>       |               |
| <span data-ttu-id="4ed89-379">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-379">Due to Fabrikam (Fabrikam West)</span></span>  |              | <span data-ttu-id="4ed89-380">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-380">100.00</span></span>        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a><span data-ttu-id="4ed89-381">例 6 : 基本支払のない仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="4ed89-381">Example 6: Vendor credit note without primary payment</span></span>
<span data-ttu-id="4ed89-382">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="4ed89-382">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="4ed89-383">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="4ed89-383">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="4ed89-384">支払は、**トランザクションの決済** ページでは基本支払として選択されません。</span><span class="sxs-lookup"><span data-stu-id="4ed89-384">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="4ed89-385">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="4ed89-385">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="4ed89-386">口座</span><span class="sxs-lookup"><span data-stu-id="4ed89-386">Account</span></span>                          | <span data-ttu-id="4ed89-387">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-387">Debit amount</span></span> | <span data-ttu-id="4ed89-388">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-388">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-389">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-389">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="4ed89-390">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-390">100.00</span></span>       |               |
| <span data-ttu-id="4ed89-391">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-391">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="4ed89-392">100.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-392">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="4ed89-393">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="4ed89-393">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="4ed89-394">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-394">Account</span></span>                          | <span data-ttu-id="4ed89-395">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-395">Debit amount</span></span> | <span data-ttu-id="4ed89-396">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-396">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-397">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-397">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-398">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-398">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-399">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-399">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="4ed89-400">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-400">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="4ed89-401">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-401">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="4ed89-402">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-402">Account</span></span>                     | <span data-ttu-id="4ed89-403">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-403">Debit amount</span></span> | <span data-ttu-id="4ed89-404">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-404">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-405">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-405">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="4ed89-406">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-406">75.00</span></span>        |               |
| <span data-ttu-id="4ed89-407">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-407">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="4ed89-408">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-408">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="4ed89-409">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="4ed89-409">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="4ed89-410">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-410">**Fabrikam posting**</span></span>

| <span data-ttu-id="4ed89-411">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-411">Account</span></span>                           | <span data-ttu-id="4ed89-412">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-412">Debit amount</span></span> | <span data-ttu-id="4ed89-413">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-413">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-414">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-414">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="4ed89-415">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-415">75.00</span></span>        |               |
| <span data-ttu-id="4ed89-416">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="4ed89-416">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="4ed89-417">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-417">75.00</span></span>         |

<span data-ttu-id="4ed89-418">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-418">**Fabrikam East posting**</span></span>

| <span data-ttu-id="4ed89-419">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-419">Account</span></span>                                | <span data-ttu-id="4ed89-420">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-420">Debit amount</span></span> | <span data-ttu-id="4ed89-421">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-421">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-422">Fabrikam West 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-422">Due from Fabrikam West (Fabrikam East)</span></span> | <span data-ttu-id="4ed89-423">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-423">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-424">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="4ed89-424">Accounts payable (Fabrikam East)</span></span>       |              | <span data-ttu-id="4ed89-425">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-425">25.00</span></span>         |

<span data-ttu-id="4ed89-426">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="4ed89-426">**Fabrikam West posting**</span></span>

| <span data-ttu-id="4ed89-427">勘定</span><span class="sxs-lookup"><span data-stu-id="4ed89-427">Account</span></span>                              | <span data-ttu-id="4ed89-428">借方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-428">Debit amount</span></span> | <span data-ttu-id="4ed89-429">貸方金額</span><span class="sxs-lookup"><span data-stu-id="4ed89-429">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="4ed89-430">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-430">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="4ed89-431">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-431">75.00</span></span>        |               |
| <span data-ttu-id="4ed89-432">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-432">Due to Fabrikam (Fabrikam West)</span></span>      |              | <span data-ttu-id="4ed89-433">75.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-433">75.00</span></span>         |
| <span data-ttu-id="4ed89-434">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-434">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="4ed89-435">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-435">25.00</span></span>        |               |
| <span data-ttu-id="4ed89-436">Fabrikam East 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="4ed89-436">Due to Fabrikam East (Fabrikam West)</span></span> |              | <span data-ttu-id="4ed89-437">25.00</span><span class="sxs-lookup"><span data-stu-id="4ed89-437">25.00</span></span>         |






