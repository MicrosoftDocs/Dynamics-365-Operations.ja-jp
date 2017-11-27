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

# <a name="centralized-payments-for-accounts-payable"></a><span data-ttu-id="edaa9-105">買掛金勘定の集中支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-105">Centralized payments for Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="edaa9-106">複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="edaa9-107">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="edaa9-107">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="edaa9-108">この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="edaa9-109">複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="edaa9-110">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="edaa9-110">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="edaa9-111">また、組織では、支払プロセスが合理化されるため、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-111">Additionally, the organization saves time, because the payment process is streamlined.</span></span>

<span data-ttu-id="edaa9-112">集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの仕入先請求書を管理します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-112">In a centralized payments organization, there are many legal entities for operations, and each operating legal entity manages its own vendor invoices.</span></span> <span data-ttu-id="edaa9-113">事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人から行われます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-113">Payments for all the operating legal entities are generated from a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="edaa9-114">決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="edaa9-115">組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、会社間支払に関連する現金割引トランザクションの処理方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a cross-company payment are handled.</span></span> 

<span data-ttu-id="edaa9-116">次の各例で、さまざまなシナリオにおける転記の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="edaa9-117">これらすべての例について、次の構成が想定されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="edaa9-118">法人は Fabrikam、Fabrikam East、および Fabrikam West です。</span><span class="sxs-lookup"><span data-stu-id="edaa9-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="edaa9-119">支払は、Fabrikam で構成されています。</span><span class="sxs-lookup"><span data-stu-id="edaa9-119">Payments are made from Fabrikam.</span></span>
-   <span data-ttu-id="edaa9-120">[**会社間会計**] ページの [**現金割引の転記**] フィールドには**請求書の法人**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="edaa9-121">[**会社間会計**] ページの [**為替差益または差損の転記**] フィールドには**請求書の支払**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="edaa9-122">仕入先の Fourth Coffee は、各法人の仕入先として設定されています。</span><span class="sxs-lookup"><span data-stu-id="edaa9-122">The vendor Fourth Coffee is set up as a vendor in each legal entity.</span></span> <span data-ttu-id="edaa9-123">異なる法人の仕入先は同一のグローバル アドレス帳 ID を共有するため、同じ仕入先として識別されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-123">The vendors from the various legal entities are identified as the same vendor because they share the same global address book ID.</span></span>

| <span data-ttu-id="edaa9-124">ディレクトリ ID</span><span class="sxs-lookup"><span data-stu-id="edaa9-124">Directory ID</span></span> | <span data-ttu-id="edaa9-125">仕入先</span><span class="sxs-lookup"><span data-stu-id="edaa9-125">Vendor account</span></span> | <span data-ttu-id="edaa9-126">氏名</span><span class="sxs-lookup"><span data-stu-id="edaa9-126">Name</span></span>          | <span data-ttu-id="edaa9-127">個法</span><span class="sxs-lookup"><span data-stu-id="edaa9-127">Legal entity</span></span>  |
|--------------|----------------|---------------|---------------|
| <span data-ttu-id="edaa9-128">1050</span><span class="sxs-lookup"><span data-stu-id="edaa9-128">1050</span></span>         | <span data-ttu-id="edaa9-129">3004</span><span class="sxs-lookup"><span data-stu-id="edaa9-129">3004</span></span>           | <span data-ttu-id="edaa9-130">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="edaa9-130">Fourth Coffee</span></span> | <span data-ttu-id="edaa9-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="edaa9-131">Fabrikam</span></span>      |
| <span data-ttu-id="edaa9-132">1050</span><span class="sxs-lookup"><span data-stu-id="edaa9-132">1050</span></span>         | <span data-ttu-id="edaa9-133">100</span><span class="sxs-lookup"><span data-stu-id="edaa9-133">100</span></span>            | <span data-ttu-id="edaa9-134">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="edaa9-134">Fourth Coffee</span></span> | <span data-ttu-id="edaa9-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="edaa9-135">Fabrikam East</span></span> |
| <span data-ttu-id="edaa9-136">1050</span><span class="sxs-lookup"><span data-stu-id="edaa9-136">1050</span></span>         | <span data-ttu-id="edaa9-137">3004</span><span class="sxs-lookup"><span data-stu-id="edaa9-137">3004</span></span>           | <span data-ttu-id="edaa9-138">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="edaa9-138">Fourth Coffee</span></span> | <span data-ttu-id="edaa9-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="edaa9-139">Fabrikam West</span></span> |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="edaa9-140">例 1 : 別の法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-140">Example 1: Vendor payment of invoice from another legal entity</span></span>
<span data-ttu-id="edaa9-141">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="edaa9-141">Fabrikam East has an open invoice for vendor account 100, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-142">Fabrikam は、支払を入力し、Fabrikam 仕入先 3004 の Fourth Coffee に転記します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-142">Fabrikam enters and posts a payment to Fabrikam vendor account 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-143">支払は、未処理請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-143">The payment is settled with the open invoice.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="edaa9-144">仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="edaa9-144">Invoice is posted in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="edaa9-145">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-145">Account</span></span>                          | <span data-ttu-id="edaa9-146">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-146">Debit amount</span></span> | <span data-ttu-id="edaa9-147">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-147">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-148">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-148">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="edaa9-149">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-149">600.00</span></span>       |               |
| <span data-ttu-id="edaa9-150">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-150">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="edaa9-151">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-151">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="edaa9-152">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-152">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="edaa9-153">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-153">Account</span></span>                     | <span data-ttu-id="edaa9-154">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-154">Debit amount</span></span> | <span data-ttu-id="edaa9-155">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-155">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-156">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-156">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-157">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-157">600.00</span></span>       |               |
| <span data-ttu-id="edaa9-158">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-158">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="edaa9-159">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-159">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="edaa9-160">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-160">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="edaa9-161">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-161">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-162">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-162">Account</span></span>                           | <span data-ttu-id="edaa9-163">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-163">Debit amount</span></span> | <span data-ttu-id="edaa9-164">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-164">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-165">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-165">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="edaa9-166">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-166">600.00</span></span>       |               |
| <span data-ttu-id="edaa9-167">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-167">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="edaa9-168">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-168">600.00</span></span>        |

<span data-ttu-id="edaa9-169">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-169">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-170">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-170">Account</span></span>                          | <span data-ttu-id="edaa9-171">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-171">Debit amount</span></span> | <span data-ttu-id="edaa9-172">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-172">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-173">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-173">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-174">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-174">600.00</span></span>       |               |
| <span data-ttu-id="edaa9-175">Fabrikam への貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-175">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="edaa9-176">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-176">600.00</span></span>        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="edaa9-177">例 2 : 現金割引のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-177">Example 2: Vendor payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="edaa9-178">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="edaa9-178">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-179">請求書では、20.00 の現金割引を利用できます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="edaa9-180">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する 580.00 の支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-180">Fabrikam enters and posts a payment of 580.00 for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-181">支払は、未処理の Fabrikam East 請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-181">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="edaa9-182">現金割引が請求書、Fabrikam East の法人に転記されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-182">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="edaa9-183">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="edaa9-183">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="edaa9-184">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-184">Account</span></span>                          | <span data-ttu-id="edaa9-185">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-185">Debit amount</span></span> | <span data-ttu-id="edaa9-186">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-186">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-187">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-187">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="edaa9-188">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-188">600.00</span></span>       |               |
| <span data-ttu-id="edaa9-189">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-189">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="edaa9-190">600.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-190">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="edaa9-191">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-191">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="edaa9-192">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-192">Account</span></span>                     | <span data-ttu-id="edaa9-193">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-193">Debit amount</span></span> | <span data-ttu-id="edaa9-194">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-194">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-195">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-195">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-196">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-196">580.00</span></span>       |               |
| <span data-ttu-id="edaa9-197">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-197">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="edaa9-198">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-198">580.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="edaa9-199">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-199">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="edaa9-200">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-200">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-201">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-201">Account</span></span>                           | <span data-ttu-id="edaa9-202">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-202">Debit amount</span></span> | <span data-ttu-id="edaa9-203">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-203">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-204">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-204">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="edaa9-205">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-205">580.00</span></span>       |               |
| <span data-ttu-id="edaa9-206">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-206">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="edaa9-207">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-207">580.00</span></span>        |

<span data-ttu-id="edaa9-208">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-208">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-209">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-209">Account</span></span>                          | <span data-ttu-id="edaa9-210">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-210">Debit amount</span></span> | <span data-ttu-id="edaa9-211">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-211">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-212">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-212">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-213">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-213">580.00</span></span>       |               |
| <span data-ttu-id="edaa9-214">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-214">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="edaa9-215">580.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-215">580.00</span></span>        |
| <span data-ttu-id="edaa9-216">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-216">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-217">20.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-217">20.00</span></span>        |               |
| <span data-ttu-id="edaa9-218">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-218">Cash discount (Fabrikam East)</span></span>    |              | <span data-ttu-id="edaa9-219">20.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-219">20.00</span></span>         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a><span data-ttu-id="edaa9-220">例 3 : 実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-220">Example 3: Vendor payment of invoice from another legal entity with realized exchange rate loss</span></span>
<span data-ttu-id="edaa9-221">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="edaa9-221">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-222">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-222">Fabrikam enters and posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-223">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-223">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="edaa9-224">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-224">A currency exchange loss transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="edaa9-225">請求日時点でのユーロ (EUR) から米国ドル (USD) への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="edaa9-225">Exchange rate for euros (EUR) to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="edaa9-226">支払日時点での EUR から USD への為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="edaa9-226">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="edaa9-227">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="edaa9-227">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="edaa9-228">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-228">Account</span></span>                          | <span data-ttu-id="edaa9-229">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-229">Debit amount</span></span>            | <span data-ttu-id="edaa9-230">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-230">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-231">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-231">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="edaa9-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-232">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="edaa9-233">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-233">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="edaa9-234">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-234">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="edaa9-235">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-235">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="edaa9-236">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-236">Account</span></span>                     | <span data-ttu-id="edaa9-237">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-237">Debit amount</span></span>            | <span data-ttu-id="edaa9-238">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-238">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-239">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-239">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-240">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="edaa9-241">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-241">Cash (Fabrikam)</span></span>             |                         | <span data-ttu-id="edaa9-242">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-242">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="edaa9-243">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-243">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="edaa9-244">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-244">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-245">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-245">Account</span></span>                           | <span data-ttu-id="edaa9-246">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-246">Debit amount</span></span>            | <span data-ttu-id="edaa9-247">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-247">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-248">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-248">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="edaa9-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-249">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="edaa9-250">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-250">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="edaa9-251">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-251">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="edaa9-252">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-252">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="edaa9-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-253">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="edaa9-254">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-254">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="edaa9-255">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-255">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="edaa9-256">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-256">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-257">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-257">Account</span></span>                          | <span data-ttu-id="edaa9-258">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-258">Debit amount</span></span>            | <span data-ttu-id="edaa9-259">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-259">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-260">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-260">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-261">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="edaa9-262">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-262">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="edaa9-263">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-263">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="edaa9-264">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-264">Due to Fabrikam (Fabrikam East)</span></span>  | <span data-ttu-id="edaa9-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-265">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="edaa9-266">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-266">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="edaa9-267">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-267">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a><span data-ttu-id="edaa9-268">例 4 : 現金割引と実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-268">Example 4: Vendor payment of invoice from another legal entity with cash discount and realized exchange rate loss</span></span>
<span data-ttu-id="edaa9-269">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="edaa9-269">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-270">請求書には現金割引があり、売上税トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-270">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="edaa9-271">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を転記します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-271">Fabrikam posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-272">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-272">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="edaa9-273">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-273">A currency exchange loss transaction is generated during the settlement process.</span></span> <span data-ttu-id="edaa9-274">現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差損が支払の法人 (Fabrikam) に転記されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-274">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange loss is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="edaa9-275">請求日時点での EUR から USD への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="edaa9-275">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="edaa9-276">支払日時点での USD に対する EUR の為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="edaa9-276">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="edaa9-277">仕入先 100 に対して Fabrikam East で転記される請求書および生成される税トランザクション</span><span class="sxs-lookup"><span data-stu-id="edaa9-277">Invoice is posted and a tax transaction is generated in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="edaa9-278">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-278">Account</span></span>                          | <span data-ttu-id="edaa9-279">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-279">Debit amount</span></span>            | <span data-ttu-id="edaa9-280">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-280">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-281">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-281">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="edaa9-282">564.07 EUR / 680.38 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-282">564.07 EUR / 680.38 USD</span></span> |                         |
| <span data-ttu-id="edaa9-283">売上税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-283">Sales tax (Fabrikam East)</span></span>        | <span data-ttu-id="edaa9-284">35.93 EUR / 43.34 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-284">35.93 EUR / 43.34 USD</span></span>   |                         |
| <span data-ttu-id="edaa9-285">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-285">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="edaa9-286">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-286">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="edaa9-287">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-287">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="edaa9-288">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-288">Account</span></span>                     | <span data-ttu-id="edaa9-289">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-289">Debit amount</span></span>            | <span data-ttu-id="edaa9-290">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-290">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-291">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-291">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-292">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-292">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="edaa9-293">現金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-293">Cash (Fabrikam East)</span></span>        |                         | <span data-ttu-id="edaa9-294">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-294">588.72 EUR / 722.77 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="edaa9-295">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-295">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="edaa9-296">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-296">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-297">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-297">Account</span></span>                           | <span data-ttu-id="edaa9-298">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-298">Debit amount</span></span>            | <span data-ttu-id="edaa9-299">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-299">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-300">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-300">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="edaa9-301">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-301">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="edaa9-302">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-302">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="edaa9-303">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-303">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="edaa9-304">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-304">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="edaa9-305">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-305">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="edaa9-306">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-306">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="edaa9-307">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-307">0.00 EUR / 12.66 USD</span></span>    |

<span data-ttu-id="edaa9-308">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-308">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-309">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-309">Account</span></span>                          | <span data-ttu-id="edaa9-310">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-310">Debit amount</span></span>            | <span data-ttu-id="edaa9-311">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-311">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="edaa9-312">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-312">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-313">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-313">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="edaa9-314">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-314">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="edaa9-315">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-315">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="edaa9-316">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-316">Due to Fabrikam (Fabrikam East</span></span>   | <span data-ttu-id="edaa9-317">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-317">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="edaa9-318">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-318">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="edaa9-319">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-319">0.00 EUR / 12.66 USD</span></span>    |
| <span data-ttu-id="edaa9-320">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-320">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-321">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-321">11.28 EUR / 13.61 USD</span></span>   |                         |
| <span data-ttu-id="edaa9-322">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-322">Cash discount (Fabrikam East)</span></span>    |                         | <span data-ttu-id="edaa9-323">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="edaa9-323">11.28 EUR / 13.61 USD</span></span>   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a><span data-ttu-id="edaa9-324">例 5 : 基本支払のある仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="edaa9-324">Example 5: Vendor credit note with primary payment</span></span>
<span data-ttu-id="edaa9-325">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-325">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-326">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-326">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="edaa9-327">支払は、**トランザクションの決済** ページで基本支払として選択されています。</span><span class="sxs-lookup"><span data-stu-id="edaa9-327">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="edaa9-328">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="edaa9-328">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="edaa9-329">口座</span><span class="sxs-lookup"><span data-stu-id="edaa9-329">Account</span></span>                          | <span data-ttu-id="edaa9-330">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-330">Debit amount</span></span> | <span data-ttu-id="edaa9-331">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-331">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-332">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-332">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="edaa9-333">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-333">100.00</span></span>       |               |
| <span data-ttu-id="edaa9-334">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-334">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="edaa9-335">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-335">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="edaa9-336">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="edaa9-336">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="edaa9-337">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-337">Account</span></span>                          | <span data-ttu-id="edaa9-338">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-338">Debit amount</span></span> | <span data-ttu-id="edaa9-339">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-339">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-340">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-340">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-341">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-341">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-342">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-342">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="edaa9-343">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-343">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="edaa9-344">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-344">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="edaa9-345">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-345">Account</span></span>                     | <span data-ttu-id="edaa9-346">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-346">Debit amount</span></span> | <span data-ttu-id="edaa9-347">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-347">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-348">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-348">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-349">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-349">75.00</span></span>        |               |
| <span data-ttu-id="edaa9-350">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-350">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="edaa9-351">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-351">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="edaa9-352">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-352">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="edaa9-353">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-353">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-354">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-354">Account</span></span>                           | <span data-ttu-id="edaa9-355">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-355">Debit amount</span></span> | <span data-ttu-id="edaa9-356">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-356">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-357">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-357">Accounts payable (Fabrikam)</span></span>       | <span data-ttu-id="edaa9-358">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-358">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-359">Fabrikam East 借り (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-359">Due to Fabrikam East (Fabrikam)</span></span>   |              | <span data-ttu-id="edaa9-360">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-360">25.00</span></span>         |
| <span data-ttu-id="edaa9-361">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-361">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="edaa9-362">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-362">100.00</span></span>       |               |
| <span data-ttu-id="edaa9-363">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-363">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="edaa9-364">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-364">100.00</span></span>        |

<span data-ttu-id="edaa9-365">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-365">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-366">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-366">Account</span></span>                           | <span data-ttu-id="edaa9-367">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-367">Debit amount</span></span> | <span data-ttu-id="edaa9-368">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-368">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-369">Fabrikam 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-369">Due from Fabrikam (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-370">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-370">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-371">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-371">Accounts payable (Fabrikam East)</span></span>  |              | <span data-ttu-id="edaa9-372">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-372">25.00</span></span>         |

<span data-ttu-id="edaa9-373">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-373">**Fabrikam West posting**</span></span>

| <span data-ttu-id="edaa9-374">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-374">Account</span></span>                          | <span data-ttu-id="edaa9-375">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-375">Debit amount</span></span> | <span data-ttu-id="edaa9-376">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-376">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-377">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-377">Accounts payable (Fabrikam West)</span></span> | <span data-ttu-id="edaa9-378">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-378">100.00</span></span>       |               |
| <span data-ttu-id="edaa9-379">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-379">Due to Fabrikam (Fabrikam West)</span></span>  |              | <span data-ttu-id="edaa9-380">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-380">100.00</span></span>        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a><span data-ttu-id="edaa9-381">例 6 : 基本支払のない仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="edaa9-381">Example 6: Vendor credit note without primary payment</span></span>
<span data-ttu-id="edaa9-382">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="edaa9-382">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="edaa9-383">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="edaa9-383">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="edaa9-384">支払は、**トランザクションの決済** ページでは基本支払として選択されません。</span><span class="sxs-lookup"><span data-stu-id="edaa9-384">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="edaa9-385">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="edaa9-385">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="edaa9-386">口座</span><span class="sxs-lookup"><span data-stu-id="edaa9-386">Account</span></span>                          | <span data-ttu-id="edaa9-387">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-387">Debit amount</span></span> | <span data-ttu-id="edaa9-388">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-388">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-389">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-389">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="edaa9-390">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-390">100.00</span></span>       |               |
| <span data-ttu-id="edaa9-391">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-391">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="edaa9-392">100.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-392">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="edaa9-393">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="edaa9-393">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="edaa9-394">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-394">Account</span></span>                          | <span data-ttu-id="edaa9-395">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-395">Debit amount</span></span> | <span data-ttu-id="edaa9-396">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-396">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-397">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-397">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-398">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-398">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-399">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-399">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="edaa9-400">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-400">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="edaa9-401">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-401">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="edaa9-402">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-402">Account</span></span>                     | <span data-ttu-id="edaa9-403">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-403">Debit amount</span></span> | <span data-ttu-id="edaa9-404">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-404">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-405">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-405">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="edaa9-406">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-406">75.00</span></span>        |               |
| <span data-ttu-id="edaa9-407">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-407">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="edaa9-408">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-408">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="edaa9-409">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="edaa9-409">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="edaa9-410">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-410">**Fabrikam posting**</span></span>

| <span data-ttu-id="edaa9-411">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-411">Account</span></span>                           | <span data-ttu-id="edaa9-412">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-412">Debit amount</span></span> | <span data-ttu-id="edaa9-413">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-413">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-414">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-414">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="edaa9-415">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-415">75.00</span></span>        |               |
| <span data-ttu-id="edaa9-416">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="edaa9-416">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="edaa9-417">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-417">75.00</span></span>         |

<span data-ttu-id="edaa9-418">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-418">**Fabrikam East posting**</span></span>

| <span data-ttu-id="edaa9-419">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-419">Account</span></span>                                | <span data-ttu-id="edaa9-420">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-420">Debit amount</span></span> | <span data-ttu-id="edaa9-421">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-421">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-422">Fabrikam West 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-422">Due from Fabrikam West (Fabrikam East)</span></span> | <span data-ttu-id="edaa9-423">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-423">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-424">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="edaa9-424">Accounts payable (Fabrikam East)</span></span>       |              | <span data-ttu-id="edaa9-425">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-425">25.00</span></span>         |

<span data-ttu-id="edaa9-426">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="edaa9-426">**Fabrikam West posting**</span></span>

| <span data-ttu-id="edaa9-427">勘定</span><span class="sxs-lookup"><span data-stu-id="edaa9-427">Account</span></span>                              | <span data-ttu-id="edaa9-428">借方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-428">Debit amount</span></span> | <span data-ttu-id="edaa9-429">貸方金額</span><span class="sxs-lookup"><span data-stu-id="edaa9-429">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="edaa9-430">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-430">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="edaa9-431">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-431">75.00</span></span>        |               |
| <span data-ttu-id="edaa9-432">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-432">Due to Fabrikam (Fabrikam West)</span></span>      |              | <span data-ttu-id="edaa9-433">75.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-433">75.00</span></span>         |
| <span data-ttu-id="edaa9-434">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-434">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="edaa9-435">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-435">25.00</span></span>        |               |
| <span data-ttu-id="edaa9-436">Fabrikam East 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="edaa9-436">Due to Fabrikam East (Fabrikam West)</span></span> |              | <span data-ttu-id="edaa9-437">25.00</span><span class="sxs-lookup"><span data-stu-id="edaa9-437">25.00</span></span>         |






