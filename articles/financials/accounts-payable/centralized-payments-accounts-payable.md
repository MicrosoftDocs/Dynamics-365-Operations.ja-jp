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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 49d5242168cd43e78dd4b0c63da363f91f680904
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="centralized-payments-for-accounts-payable"></a><span data-ttu-id="c77b5-105">買掛金勘定の集中支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-105">Centralized payments for Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c77b5-106">複数の法人を含む組織では、すべての支払を処理する単一の法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="c77b5-107">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c77b5-107">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="c77b5-108">この記事は、集中支払に対する転記がさまざまなシナリオで処理される方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="c77b5-109">複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="c77b5-110">したがって、同じ支払を複数の法人に入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c77b5-110">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="c77b5-111">また、組織では、支払プロセスが合理化されるため、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-111">Additionally, the organization saves time, because the payment process is streamlined.</span></span>

<span data-ttu-id="c77b5-112">集中支払組織では、事業を行うために多くの法人があり、事業を行っている各法人がそれぞれの仕入先請求書を管理します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-112">In a centralized payments organization, there are many legal entities for operations, and each operating legal entity manages its own vendor invoices.</span></span> <span data-ttu-id="c77b5-113">事業を行っているすべての法人の支払は、支払の法人として知られている 1 つの法人から行われます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-113">Payments for all the operating legal entities are generated from a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="c77b5-114">決済プロセス中に、適切な借りトランザクションと貸しトランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="c77b5-115">組織内のどの法人が実利益トランザクションと実損失トランザクションを受け取るか、また、会社間支払に関連する現金割引トランザクションの処理方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a cross-company payment are handled.</span></span> 

<span data-ttu-id="c77b5-116">次の各例で、さまざまなシナリオにおける転記の処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="c77b5-117">これらすべての例について、次の構成が想定されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="c77b5-118">法人は Fabrikam、Fabrikam East、および Fabrikam West です。</span><span class="sxs-lookup"><span data-stu-id="c77b5-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="c77b5-119">支払は、Fabrikam で構成されています。</span><span class="sxs-lookup"><span data-stu-id="c77b5-119">Payments are made from Fabrikam.</span></span>
-   <span data-ttu-id="c77b5-120">[**会社間会計**] ページの [**現金割引の転記**] フィールドには**請求書の法人**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="c77b5-121">[**会社間会計**] ページの [**為替差益または差損の転記**] フィールドには**請求書の支払**が設定されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="c77b5-122">仕入先の Fourth Coffee は、各法人の仕入先として設定されています。</span><span class="sxs-lookup"><span data-stu-id="c77b5-122">The vendor Fourth Coffee is set up as a vendor in each legal entity.</span></span> <span data-ttu-id="c77b5-123">異なる法人の仕入先は同一のグローバル アドレス帳 ID を共有するため、同じ仕入先として識別されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-123">The vendors from the various legal entities are identified as the same vendor because they share the same global address book ID.</span></span>

| <span data-ttu-id="c77b5-124">ディレクトリ ID</span><span class="sxs-lookup"><span data-stu-id="c77b5-124">Directory ID</span></span> | <span data-ttu-id="c77b5-125">仕入先</span><span class="sxs-lookup"><span data-stu-id="c77b5-125">Vendor account</span></span> | <span data-ttu-id="c77b5-126">氏名</span><span class="sxs-lookup"><span data-stu-id="c77b5-126">Name</span></span>          | <span data-ttu-id="c77b5-127">個法</span><span class="sxs-lookup"><span data-stu-id="c77b5-127">Legal entity</span></span>  |
|--------------|----------------|---------------|---------------|
| <span data-ttu-id="c77b5-128">1050</span><span class="sxs-lookup"><span data-stu-id="c77b5-128">1050</span></span>         | <span data-ttu-id="c77b5-129">3004</span><span class="sxs-lookup"><span data-stu-id="c77b5-129">3004</span></span>           | <span data-ttu-id="c77b5-130">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="c77b5-130">Fourth Coffee</span></span> | <span data-ttu-id="c77b5-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c77b5-131">Fabrikam</span></span>      |
| <span data-ttu-id="c77b5-132">1050</span><span class="sxs-lookup"><span data-stu-id="c77b5-132">1050</span></span>         | <span data-ttu-id="c77b5-133">100</span><span class="sxs-lookup"><span data-stu-id="c77b5-133">100</span></span>            | <span data-ttu-id="c77b5-134">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="c77b5-134">Fourth Coffee</span></span> | <span data-ttu-id="c77b5-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="c77b5-135">Fabrikam East</span></span> |
| <span data-ttu-id="c77b5-136">1050</span><span class="sxs-lookup"><span data-stu-id="c77b5-136">1050</span></span>         | <span data-ttu-id="c77b5-137">3004</span><span class="sxs-lookup"><span data-stu-id="c77b5-137">3004</span></span>           | <span data-ttu-id="c77b5-138">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="c77b5-138">Fourth Coffee</span></span> | <span data-ttu-id="c77b5-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="c77b5-139">Fabrikam West</span></span> |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="c77b5-140">例 1 : 別の法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-140">Example 1: Vendor payment of invoice from another legal entity</span></span>
<span data-ttu-id="c77b5-141">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="c77b5-141">Fabrikam East has an open invoice for vendor account 100, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-142">Fabrikam は、支払を入力し、Fabrikam 仕入先 3004 の Fourth Coffee に転記します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-142">Fabrikam enters and posts a payment to Fabrikam vendor account 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-143">支払は、未処理請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-143">The payment is settled with the open invoice.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="c77b5-144">仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="c77b5-144">Invoice is posted in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="c77b5-145">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-145">Account</span></span>                          | <span data-ttu-id="c77b5-146">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-146">Debit amount</span></span> | <span data-ttu-id="c77b5-147">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-147">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-148">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-148">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="c77b5-149">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-149">600.00</span></span>       |               |
| <span data-ttu-id="c77b5-150">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-150">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="c77b5-151">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-151">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="c77b5-152">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-152">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="c77b5-153">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-153">Account</span></span>                     | <span data-ttu-id="c77b5-154">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-154">Debit amount</span></span> | <span data-ttu-id="c77b5-155">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-155">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-156">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-156">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-157">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-157">600.00</span></span>       |               |
| <span data-ttu-id="c77b5-158">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-158">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="c77b5-159">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-159">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="c77b5-160">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-160">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="c77b5-161">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-161">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-162">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-162">Account</span></span>                           | <span data-ttu-id="c77b5-163">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-163">Debit amount</span></span> | <span data-ttu-id="c77b5-164">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-164">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-165">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-165">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="c77b5-166">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-166">600.00</span></span>       |               |
| <span data-ttu-id="c77b5-167">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-167">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="c77b5-168">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-168">600.00</span></span>        |

<span data-ttu-id="c77b5-169">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-169">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-170">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-170">Account</span></span>                          | <span data-ttu-id="c77b5-171">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-171">Debit amount</span></span> | <span data-ttu-id="c77b5-172">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-172">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-173">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-173">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-174">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-174">600.00</span></span>       |               |
| <span data-ttu-id="c77b5-175">Fabrikam への貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-175">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="c77b5-176">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-176">600.00</span></span>        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="c77b5-177">例 2 : 現金割引のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-177">Example 2: Vendor payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="c77b5-178">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="c77b5-178">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-179">請求書では、20.00 の現金割引を利用できます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="c77b5-180">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する 580.00 の支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-180">Fabrikam enters and posts a payment of 580.00 for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-181">支払は、未処理の Fabrikam East 請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-181">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="c77b5-182">現金割引が請求書、Fabrikam East の法人に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-182">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="c77b5-183">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="c77b5-183">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="c77b5-184">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-184">Account</span></span>                          | <span data-ttu-id="c77b5-185">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-185">Debit amount</span></span> | <span data-ttu-id="c77b5-186">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-186">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-187">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-187">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="c77b5-188">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-188">600.00</span></span>       |               |
| <span data-ttu-id="c77b5-189">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-189">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="c77b5-190">600.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-190">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="c77b5-191">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-191">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="c77b5-192">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-192">Account</span></span>                     | <span data-ttu-id="c77b5-193">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-193">Debit amount</span></span> | <span data-ttu-id="c77b5-194">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-194">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-195">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-195">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-196">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-196">580.00</span></span>       |               |
| <span data-ttu-id="c77b5-197">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-197">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="c77b5-198">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-198">580.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="c77b5-199">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-199">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="c77b5-200">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-200">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-201">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-201">Account</span></span>                           | <span data-ttu-id="c77b5-202">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-202">Debit amount</span></span> | <span data-ttu-id="c77b5-203">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-203">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-204">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-204">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="c77b5-205">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-205">580.00</span></span>       |               |
| <span data-ttu-id="c77b5-206">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-206">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="c77b5-207">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-207">580.00</span></span>        |

<span data-ttu-id="c77b5-208">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-208">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-209">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-209">Account</span></span>                          | <span data-ttu-id="c77b5-210">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-210">Debit amount</span></span> | <span data-ttu-id="c77b5-211">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-211">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-212">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-212">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-213">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-213">580.00</span></span>       |               |
| <span data-ttu-id="c77b5-214">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-214">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="c77b5-215">580.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-215">580.00</span></span>        |
| <span data-ttu-id="c77b5-216">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-216">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-217">20.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-217">20.00</span></span>        |               |
| <span data-ttu-id="c77b5-218">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-218">Cash discount (Fabrikam East)</span></span>    |              | <span data-ttu-id="c77b5-219">20.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-219">20.00</span></span>         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a><span data-ttu-id="c77b5-220">例 3 : 実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-220">Example 3: Vendor payment of invoice from another legal entity with realized exchange rate loss</span></span>
<span data-ttu-id="c77b5-221">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="c77b5-221">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-222">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を入力して転記します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-222">Fabrikam enters and posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-223">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-223">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="c77b5-224">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-224">A currency exchange loss transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="c77b5-225">請求日時点でのユーロ (EUR) から米国ドル (USD) への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="c77b5-225">Exchange rate for euros (EUR) to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="c77b5-226">支払日時点での EUR から USD への為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="c77b5-226">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="c77b5-227">Fabrikam East の仕入先 100 に対して Fabrikam East で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="c77b5-227">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="c77b5-228">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-228">Account</span></span>                          | <span data-ttu-id="c77b5-229">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-229">Debit amount</span></span>            | <span data-ttu-id="c77b5-230">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-230">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-231">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-231">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="c77b5-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-232">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="c77b5-233">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-233">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="c77b5-234">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-234">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="c77b5-235">Fabrikam の仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-235">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="c77b5-236">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-236">Account</span></span>                     | <span data-ttu-id="c77b5-237">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-237">Debit amount</span></span>            | <span data-ttu-id="c77b5-238">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-238">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-239">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-239">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-240">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="c77b5-241">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-241">Cash (Fabrikam)</span></span>             |                         | <span data-ttu-id="c77b5-242">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-242">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="c77b5-243">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-243">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="c77b5-244">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-244">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-245">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-245">Account</span></span>                           | <span data-ttu-id="c77b5-246">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-246">Debit amount</span></span>            | <span data-ttu-id="c77b5-247">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-247">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-248">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-248">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="c77b5-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-249">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="c77b5-250">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-250">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="c77b5-251">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-251">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="c77b5-252">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-252">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="c77b5-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-253">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="c77b5-254">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-254">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="c77b5-255">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-255">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="c77b5-256">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-256">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-257">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-257">Account</span></span>                          | <span data-ttu-id="c77b5-258">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-258">Debit amount</span></span>            | <span data-ttu-id="c77b5-259">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-259">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-260">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-260">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-261">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="c77b5-262">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-262">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="c77b5-263">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-263">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="c77b5-264">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-264">Due to Fabrikam (Fabrikam East)</span></span>  | <span data-ttu-id="c77b5-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-265">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="c77b5-266">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-266">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="c77b5-267">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-267">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a><span data-ttu-id="c77b5-268">例 4 : 現金割引と実現為替差損のある別法人からの請求書の仕入先支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-268">Example 4: Vendor payment of invoice from another legal entity with cash discount and realized exchange rate loss</span></span>
<span data-ttu-id="c77b5-269">Fabrikam East には、仕入先 100 の Fourth Coffee に対する未処理請求書があります。</span><span class="sxs-lookup"><span data-stu-id="c77b5-269">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-270">請求書には現金割引があり、売上税トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-270">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="c77b5-271">Fabrikam は、Fabrikam 仕入先 3004 の Fourth Coffee に対する支払を転記します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-271">Fabrikam posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-272">支払は、未処理の Fabrikam East の請求書で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-272">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="c77b5-273">決済プロセスの間に、為替差損トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-273">A currency exchange loss transaction is generated during the settlement process.</span></span> <span data-ttu-id="c77b5-274">現金割引が請求の法人 (Fabrikam East) に転記され、通貨為替差損が支払の法人 (Fabrikam) に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-274">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange loss is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="c77b5-275">請求日時点での EUR から USD への為替レート : 1.2062</span><span class="sxs-lookup"><span data-stu-id="c77b5-275">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="c77b5-276">支払日時点での USD に対する EUR の為替レート : 1.2277</span><span class="sxs-lookup"><span data-stu-id="c77b5-276">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="c77b5-277">仕入先 100 に対して Fabrikam East で転記される請求書および生成される税トランザクション</span><span class="sxs-lookup"><span data-stu-id="c77b5-277">Invoice is posted and a tax transaction is generated in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="c77b5-278">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-278">Account</span></span>                          | <span data-ttu-id="c77b5-279">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-279">Debit amount</span></span>            | <span data-ttu-id="c77b5-280">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-280">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-281">経費 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-281">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="c77b5-282">564.07 EUR / 680.38 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-282">564.07 EUR / 680.38 USD</span></span> |                         |
| <span data-ttu-id="c77b5-283">売上税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-283">Sales tax (Fabrikam East)</span></span>        | <span data-ttu-id="c77b5-284">35.93 EUR / 43.34 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-284">35.93 EUR / 43.34 USD</span></span>   |                         |
| <span data-ttu-id="c77b5-285">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-285">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="c77b5-286">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-286">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="c77b5-287">仕入先 3004 に対して Fabrikam で生成および転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-287">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="c77b5-288">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-288">Account</span></span>                     | <span data-ttu-id="c77b5-289">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-289">Debit amount</span></span>            | <span data-ttu-id="c77b5-290">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-290">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-291">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-291">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-292">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-292">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="c77b5-293">現金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-293">Cash (Fabrikam East)</span></span>        |                         | <span data-ttu-id="c77b5-294">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-294">588.72 EUR / 722.77 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="c77b5-295">Fabrikam East の請求書で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-295">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="c77b5-296">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-296">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-297">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-297">Account</span></span>                           | <span data-ttu-id="c77b5-298">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-298">Debit amount</span></span>            | <span data-ttu-id="c77b5-299">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-299">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-300">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-300">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="c77b5-301">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-301">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="c77b5-302">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-302">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="c77b5-303">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-303">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="c77b5-304">実現損失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-304">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="c77b5-305">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-305">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="c77b5-306">Fabrikam East 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-306">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="c77b5-307">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-307">0.00 EUR / 12.66 USD</span></span>    |

<span data-ttu-id="c77b5-308">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-308">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-309">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-309">Account</span></span>                          | <span data-ttu-id="c77b5-310">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-310">Debit amount</span></span>            | <span data-ttu-id="c77b5-311">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-311">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="c77b5-312">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-312">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-313">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-313">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="c77b5-314">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-314">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="c77b5-315">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-315">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="c77b5-316">Fabrikam 借り (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-316">Due to Fabrikam (Fabrikam East</span></span>   | <span data-ttu-id="c77b5-317">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-317">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="c77b5-318">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-318">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="c77b5-319">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-319">0.00 EUR / 12.66 USD</span></span>    |
| <span data-ttu-id="c77b5-320">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-320">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-321">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-321">11.28 EUR / 13.61 USD</span></span>   |                         |
| <span data-ttu-id="c77b5-322">現金割引 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-322">Cash discount (Fabrikam East)</span></span>    |                         | <span data-ttu-id="c77b5-323">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="c77b5-323">11.28 EUR / 13.61 USD</span></span>   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a><span data-ttu-id="c77b5-324">例 5 : 基本支払のある仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="c77b5-324">Example 5: Vendor credit note with primary payment</span></span>
<span data-ttu-id="c77b5-325">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-325">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-326">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-326">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="c77b5-327">支払は、**トランザクションの決済** ページで基本支払として選択されています。</span><span class="sxs-lookup"><span data-stu-id="c77b5-327">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="c77b5-328">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="c77b5-328">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="c77b5-329">口座</span><span class="sxs-lookup"><span data-stu-id="c77b5-329">Account</span></span>                          | <span data-ttu-id="c77b5-330">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-330">Debit amount</span></span> | <span data-ttu-id="c77b5-331">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-331">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-332">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-332">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="c77b5-333">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-333">100.00</span></span>       |               |
| <span data-ttu-id="c77b5-334">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-334">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="c77b5-335">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-335">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="c77b5-336">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="c77b5-336">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="c77b5-337">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-337">Account</span></span>                          | <span data-ttu-id="c77b5-338">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-338">Debit amount</span></span> | <span data-ttu-id="c77b5-339">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-339">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-340">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-340">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-341">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-341">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-342">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-342">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="c77b5-343">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-343">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="c77b5-344">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-344">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="c77b5-345">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-345">Account</span></span>                     | <span data-ttu-id="c77b5-346">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-346">Debit amount</span></span> | <span data-ttu-id="c77b5-347">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-347">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-348">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-348">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-349">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-349">75.00</span></span>        |               |
| <span data-ttu-id="c77b5-350">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-350">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="c77b5-351">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-351">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="c77b5-352">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-352">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="c77b5-353">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-353">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-354">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-354">Account</span></span>                           | <span data-ttu-id="c77b5-355">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-355">Debit amount</span></span> | <span data-ttu-id="c77b5-356">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-356">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-357">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-357">Accounts payable (Fabrikam)</span></span>       | <span data-ttu-id="c77b5-358">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-358">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-359">Fabrikam East 借り (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-359">Due to Fabrikam East (Fabrikam)</span></span>   |              | <span data-ttu-id="c77b5-360">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-360">25.00</span></span>         |
| <span data-ttu-id="c77b5-361">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-361">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="c77b5-362">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-362">100.00</span></span>       |               |
| <span data-ttu-id="c77b5-363">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-363">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="c77b5-364">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-364">100.00</span></span>        |

<span data-ttu-id="c77b5-365">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-365">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-366">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-366">Account</span></span>                           | <span data-ttu-id="c77b5-367">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-367">Debit amount</span></span> | <span data-ttu-id="c77b5-368">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-368">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-369">Fabrikam 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-369">Due from Fabrikam (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-370">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-370">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-371">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-371">Accounts payable (Fabrikam East)</span></span>  |              | <span data-ttu-id="c77b5-372">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-372">25.00</span></span>         |

<span data-ttu-id="c77b5-373">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-373">**Fabrikam West posting**</span></span>

| <span data-ttu-id="c77b5-374">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-374">Account</span></span>                          | <span data-ttu-id="c77b5-375">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-375">Debit amount</span></span> | <span data-ttu-id="c77b5-376">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-376">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-377">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-377">Accounts payable (Fabrikam West)</span></span> | <span data-ttu-id="c77b5-378">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-378">100.00</span></span>       |               |
| <span data-ttu-id="c77b5-379">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-379">Due to Fabrikam (Fabrikam West)</span></span>  |              | <span data-ttu-id="c77b5-380">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-380">100.00</span></span>        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a><span data-ttu-id="c77b5-381">例 6 : 基本支払のない仕入先貸方票</span><span class="sxs-lookup"><span data-stu-id="c77b5-381">Example 6: Vendor credit note without primary payment</span></span>
<span data-ttu-id="c77b5-382">Fabrikam は、仕入先 3004 の Fourth Coffee に対する 75.00 の支払を生成します。</span><span class="sxs-lookup"><span data-stu-id="c77b5-382">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="c77b5-383">支払は、Fabrikam West の仕入先 3004 に対する未処理請求書および Fabrikam East の仕入先 100 に対する未処理貸方票で決済されます。</span><span class="sxs-lookup"><span data-stu-id="c77b5-383">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="c77b5-384">支払は、**トランザクションの決済** ページでは基本支払として選択されません。</span><span class="sxs-lookup"><span data-stu-id="c77b5-384">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="c77b5-385">仕入先 3004 に対して Fabrikam West で転記される請求書</span><span class="sxs-lookup"><span data-stu-id="c77b5-385">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="c77b5-386">口座</span><span class="sxs-lookup"><span data-stu-id="c77b5-386">Account</span></span>                          | <span data-ttu-id="c77b5-387">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-387">Debit amount</span></span> | <span data-ttu-id="c77b5-388">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-388">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-389">経費 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-389">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="c77b5-390">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-390">100.00</span></span>       |               |
| <span data-ttu-id="c77b5-391">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-391">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="c77b5-392">100.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-392">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="c77b5-393">仕入先 100 に対して Fabrikam East に転記される貸方票</span><span class="sxs-lookup"><span data-stu-id="c77b5-393">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="c77b5-394">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-394">Account</span></span>                          | <span data-ttu-id="c77b5-395">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-395">Debit amount</span></span> | <span data-ttu-id="c77b5-396">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-396">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-397">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-397">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-398">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-398">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-399">購買返品 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-399">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="c77b5-400">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-400">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="c77b5-401">仕入先 3004 に対して Fabrikam に転記される支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-401">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="c77b5-402">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-402">Account</span></span>                     | <span data-ttu-id="c77b5-403">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-403">Debit amount</span></span> | <span data-ttu-id="c77b5-404">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-404">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-405">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-405">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="c77b5-406">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-406">75.00</span></span>        |               |
| <span data-ttu-id="c77b5-407">現金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-407">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="c77b5-408">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-408">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="c77b5-409">Fabrikam West の請求書および Fabrikam East の貸方票で決済される Fabrikam の支払</span><span class="sxs-lookup"><span data-stu-id="c77b5-409">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="c77b5-410">**Fabrikam の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-410">**Fabrikam posting**</span></span>

| <span data-ttu-id="c77b5-411">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-411">Account</span></span>                           | <span data-ttu-id="c77b5-412">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-412">Debit amount</span></span> | <span data-ttu-id="c77b5-413">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-413">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-414">Fabrikam West 貸し (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-414">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="c77b5-415">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-415">75.00</span></span>        |               |
| <span data-ttu-id="c77b5-416">買掛金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="c77b5-416">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="c77b5-417">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-417">75.00</span></span>         |

<span data-ttu-id="c77b5-418">**Fabrikam East の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-418">**Fabrikam East posting**</span></span>

| <span data-ttu-id="c77b5-419">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-419">Account</span></span>                                | <span data-ttu-id="c77b5-420">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-420">Debit amount</span></span> | <span data-ttu-id="c77b5-421">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-421">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-422">Fabrikam West 貸し (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-422">Due from Fabrikam West (Fabrikam East)</span></span> | <span data-ttu-id="c77b5-423">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-423">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-424">買掛金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="c77b5-424">Accounts payable (Fabrikam East)</span></span>       |              | <span data-ttu-id="c77b5-425">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-425">25.00</span></span>         |

<span data-ttu-id="c77b5-426">**Fabrikam West の転記**</span><span class="sxs-lookup"><span data-stu-id="c77b5-426">**Fabrikam West posting**</span></span>

| <span data-ttu-id="c77b5-427">勘定</span><span class="sxs-lookup"><span data-stu-id="c77b5-427">Account</span></span>                              | <span data-ttu-id="c77b5-428">借方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-428">Debit amount</span></span> | <span data-ttu-id="c77b5-429">貸方金額</span><span class="sxs-lookup"><span data-stu-id="c77b5-429">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="c77b5-430">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-430">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="c77b5-431">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-431">75.00</span></span>        |               |
| <span data-ttu-id="c77b5-432">Fabrikam 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-432">Due to Fabrikam (Fabrikam West)</span></span>      |              | <span data-ttu-id="c77b5-433">75.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-433">75.00</span></span>         |
| <span data-ttu-id="c77b5-434">買掛金 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-434">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="c77b5-435">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-435">25.00</span></span>        |               |
| <span data-ttu-id="c77b5-436">Fabrikam East 借り (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="c77b5-436">Due to Fabrikam East (Fabrikam West)</span></span> |              | <span data-ttu-id="c77b5-437">25.00</span><span class="sxs-lookup"><span data-stu-id="c77b5-437">25.00</span></span>         |






