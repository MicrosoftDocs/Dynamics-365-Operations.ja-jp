---
title: "一部金額の支払"
description: "1 つの請求書の量より少ない支払いを仕入先に行う場合があります。 この記事は、この状況を処理するためのさまざまなオプションについて説明します。 利用できるオプションは、業務要件とコンフィギュレーションによって異なります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cc8e2864343b5e9fee8eaf058a51360d15e425a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="830ae-105">一部金額の支払</span><span class="sxs-lookup"><span data-stu-id="830ae-105">Vendor payments for a partial amount</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="830ae-106">1 つの請求書の量より少ない支払いを仕入先に行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="830ae-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="830ae-107">この記事は、この状況を処理するためのさまざまなオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="830ae-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="830ae-108">利用できるオプションは、業務要件とコンフィギュレーションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="830ae-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="830ae-109">現金割引金額</span><span class="sxs-lookup"><span data-stu-id="830ae-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="830ae-110">ベンダーは、期日までに請求書の支払いをする場合の現金割引を提供できます。</span><span class="sxs-lookup"><span data-stu-id="830ae-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="830ae-111">たとえば、請求書が 10 日以内に支払われた場合は 2% の現金割引が指定される 100.00 の請求書を入力します。</span><span class="sxs-lookup"><span data-stu-id="830ae-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="830ae-112">期日の条件は 30 日になります。</span><span class="sxs-lookup"><span data-stu-id="830ae-112">The due date terms are 30 days.</span></span> <span data-ttu-id="830ae-113">支払提案が、請求書を選択するための条件として現金割引を使用する場合、また提案が現金割引日かそれ以前に実行される場合、請求書が支払に選択され、98.00 の支払いが作成されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="830ae-114">現金割引は、手動で作成された 1 回限りの支払にも適用できます。</span><span class="sxs-lookup"><span data-stu-id="830ae-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="830ae-115">現金割引される一部支払</span><span class="sxs-lookup"><span data-stu-id="830ae-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="830ae-116">全額請求書を決済するために追加の一部支払を作成するつもりで、一部支払を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="830ae-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="830ae-117">一部支払の現金割引を適用するには、**買掛金勘定パラメーター** ページで **一部支払の現金割引を計算** オプションを、**はい** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="830ae-117">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments **option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="830ae-118">たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の割引が指定される現金割引を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="830ae-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="830ae-119">請求書に 100.00 が転記されています。</span><span class="sxs-lookup"><span data-stu-id="830ae-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="830ae-120">10 日以内に 49.00 の支払を行う場合、支払仕訳に 49.00 の借方金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="830ae-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="830ae-121">一部支払を **トランザクションの決済** ページで決済すると、**適用する現金割引金額** フィールドに **1.00** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="830ae-122">一部支払を入力して、[**決済金額**] フィールドに完全な請求金額を残す場合、[**適用する現金割引金額**] フィールドはトランザクションを転記するときに自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="830ae-123">現金割引の訂正票</span><span class="sxs-lookup"><span data-stu-id="830ae-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="830ae-124">請求書の品目の一部を返す場合、訂正票を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="830ae-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="830ae-125">現金割引が元の請求書に適用された場合、割引の値を差し引き、正しい量の返金を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="830ae-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="830ae-126">**買掛金管理パラメーター** ページの **訂正票に対する現金割引を計算** オプションが **はい** に設定されている場合、貸方票のために割引が自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-126">If the **Calculate cash discounts for credit notes **option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="830ae-127">たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の割引が指定される現金割引を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="830ae-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="830ae-128">請求書に 100.00 が転記されています。</span><span class="sxs-lookup"><span data-stu-id="830ae-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="830ae-129">品目を返品して貸方票を受け取る場合、クレジット メモで定義された 2% の現金割引とともに、元の請求書の総額 100.00 の貸方票を入力できます。</span><span class="sxs-lookup"><span data-stu-id="830ae-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="830ae-130">貸方票を **未処理トランザクションの決済** ページで表示する場合、**98.00** は **決済金額** フィールドに表示され、**-2.00** は **現金割引金額** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="830ae-131">割引量が現金割引勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="830ae-132">過剰支払/過少支払の量</span><span class="sxs-lookup"><span data-stu-id="830ae-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="830ae-133">一部支払い後に、決済する必要がある額がきわめて小さい場合があります。</span><span class="sxs-lookup"><span data-stu-id="830ae-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="830ae-134">たとえば、仕入先請求書が 1,000.00 で支払が 999.90 を支払うとします。</span><span class="sxs-lookup"><span data-stu-id="830ae-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="830ae-135">残りの金額が [**買掛金管理パラメーター**] ページの過剰支払または過小支払に指定される量より少ない場合、差額が過剰支払/過少支払の勘定科目に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="830ae-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="830ae-136">詳細については、[仕入先の支払概要](../cash-bank-management/tasks/vendor-payment-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="830ae-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

