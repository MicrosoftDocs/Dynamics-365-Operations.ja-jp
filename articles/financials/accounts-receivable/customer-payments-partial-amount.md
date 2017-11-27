---
title: "一部金額の顧客支払"
description: "顧客は、請求金額未満の支払を行う場合があります。 この記事は、この状況を処理するためのさまざまなオプションについて説明します。 利用できるオプションは、業務要件とコンフィギュレーションによって異なります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c2ba17b97bf7a00ff111e72314e98f5af7aaed80
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="customer-payments-for-a-partial-amount"></a><span data-ttu-id="ef436-105">一部金額の顧客支払</span><span class="sxs-lookup"><span data-stu-id="ef436-105">Customer payments for a partial amount</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef436-106">顧客は、請求金額未満の支払を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-106">Sometimes, customers make a payment that is less than the amount of an invoice.</span></span> <span data-ttu-id="ef436-107">この記事は、この状況を処理するためのさまざまなオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ef436-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="ef436-108">利用できるオプションは、業務要件とコンフィギュレーションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ef436-108">The options that are available to you depend on your business requirements and configuration.</span></span>

<a name="partial-payment-with-no-discount"></a><span data-ttu-id="ef436-109">割引のない一部支払</span><span class="sxs-lookup"><span data-stu-id="ef436-109">Partial payment with no discount</span></span>
--------------------------------

<span data-ttu-id="ef436-110">顧客が請求書の全額を支払う現金の手持ちがどうしてもないため、または請求書の品目に関して争議があるために一部支払を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-110">Customers might make a partial payment because they just don't have enough cash on hand to pay the invoice in full, or because there is a dispute about an item on the invoice.</span></span> <span data-ttu-id="ef436-111">この場合、支払いにより請求書は部分的に決済できます。</span><span class="sxs-lookup"><span data-stu-id="ef436-111">In this situation, the invoice can be partially settled with the payment.</span></span> <span data-ttu-id="ef436-112">請求書は未処理のままで残り、残高を表示します。</span><span class="sxs-lookup"><span data-stu-id="ef436-112">The invoice will remain open and will show a balance.</span></span>

## <a name="discount-amounts"></a><span data-ttu-id="ef436-113">割引金額</span><span class="sxs-lookup"><span data-stu-id="ef436-113">Discount amounts</span></span>
<span data-ttu-id="ef436-114">期日までに請求書の支払いをする場合の現金割引を顧客に提供できます。</span><span class="sxs-lookup"><span data-stu-id="ef436-114">You can offer customers a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="ef436-115">たとえば、請求書が 10 日以内に支払われた場合は 2% の現金割引が指定される 100.00 の請求書を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef436-115">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="ef436-116">期日の条件は 30 日になります。</span><span class="sxs-lookup"><span data-stu-id="ef436-116">The due-date terms are 30 days.</span></span> <span data-ttu-id="ef436-117">10 日以内に 98.00 の支払を受け取った場合、98.00 の支払を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef436-117">If you receive a payment of 98.00 within 10 days, you enter the payment for 98.00.</span></span> <span data-ttu-id="ef436-118">請求書が決済の対象としてマークされている場合、自動的に現金割引が実行されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-118">Then, when the invoice is marked for settlement, the cash discount it taken automatically.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="ef436-119">現金割引される一部支払</span><span class="sxs-lookup"><span data-stu-id="ef436-119">Partial payments with cash discounts</span></span>
<span data-ttu-id="ef436-120">顧客は全額請求書を決済するために追加の一部支払を作成するつもりで、一部支払を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-120">When customers make a partial payment, they might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="ef436-121">一部支払の現金割引を適用するには、**売掛金勘定パラメーター** ページで [**一部支払の現金割引を計算**] オプションを [**はい**] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-121">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments **option to **Yes** on the **Accounts receivable parameters** page.</span></span> 

<span data-ttu-id="ef436-122">たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の割引が指定される現金割引を提供します。</span><span class="sxs-lookup"><span data-stu-id="ef436-122">For example, you offer a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="ef436-123">請求書に 100.00 が転記されています。</span><span class="sxs-lookup"><span data-stu-id="ef436-123">An invoice is posted for 100.00.</span></span> <span data-ttu-id="ef436-124">10 日以内に 49.00 の支払を受け取る場合、支払仕訳帳に 49.00 の貸方を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef436-124">If you receive a payment of 49.00 within 10 days, you enter a credit of 49.00 in a payment journal.</span></span> <span data-ttu-id="ef436-125">一部支払を [**トランザクションの決済**] ページで決済すると、[**適用する現金割引金額**] フィールドに **1.00** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-125">When you settle the partial payment on the **Settle transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> <span data-ttu-id="ef436-126">割引量が現金割引勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-126">The discount amount is posted to a cash discount account.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ef436-127">一部支払を入力して、[**決済金額**] フィールドに完全な請求金額を残す場合、[**適用する現金割引金額**] フィールドはトランザクションを転記するときに自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-127">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-discounts"></a><span data-ttu-id="ef436-128">割引の訂正票</span><span class="sxs-lookup"><span data-stu-id="ef436-128">Credit notes with discounts</span></span>
<span data-ttu-id="ef436-129">顧客が請求書の品目の一部を返す場合、訂正票を発行する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-129">If customers return some of the items on an invoice, you might issue a credit note.</span></span> <span data-ttu-id="ef436-130">現金割引が元の請求書に適用された場合、顧客へのクレジット メモは、顧客が履修した現金割引の正味である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-130">If a cash discount was taken on the original invoice, the credit memo to the customer should be net of the cash discount that was taken by the customer.</span></span> <span data-ttu-id="ef436-131">[**売掛金勘定パラメーター**] ページの [**訂正票に対する現金割引を計算**] オプション [**はい**] に設定されている場合、貸方票のために割引が自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-131">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts receivable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="ef436-132">たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の現金割引が指定される支払条件を提供します。</span><span class="sxs-lookup"><span data-stu-id="ef436-132">For example, you offered terms of payment that specify a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="ef436-133">請求書に 100.00 が転記され、顧客が現金割引を適用しました。</span><span class="sxs-lookup"><span data-stu-id="ef436-133">An invoice for 100.00 was posted, and the customer took the cash discount.</span></span> <span data-ttu-id="ef436-134">顧客が品目を返品したときに訂正票を発行した場合、-100.00 の訂正票を入力できます。</span><span class="sxs-lookup"><span data-stu-id="ef436-134">If the customer returns the goods and you issue a credit note, you can enter the credit note for -100.00.</span></span> <span data-ttu-id="ef436-135">貸方票を [**未処理トランザクションの決済**] ページで表示する場合、**98.00**は [**決済金額**] フィールドに表示され、  **-2.00** は [**現金割引金額**] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-135">When you view the credit note on the **Settle open transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="ef436-136">割引量が現金割引勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-136">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="ef436-137">過剰支払/過少支払の量</span><span class="sxs-lookup"><span data-stu-id="ef436-137">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="ef436-138">顧客が支払を行うと、まだ決済する必要があるきわめて小さな額がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-138">When customers make a payment, there might be a very small amount that must still be settled.</span></span> <span data-ttu-id="ef436-139">たとえば、顧客に 1,000.00 を請求し、顧客は 999.90 を支払います。</span><span class="sxs-lookup"><span data-stu-id="ef436-139">For example, you invoice the customer for 1,000.00, and the customer pays 999.90.</span></span> <span data-ttu-id="ef436-140">残りの金額が [**売掛金勘定パラメーター**] ページの過剰支払または過小支払に指定される量より少ない場合、差額が過剰支払/過少支払の勘定科目に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-140">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts receivable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>

## <a name="full-settlement"></a><span data-ttu-id="ef436-141">全額決済</span><span class="sxs-lookup"><span data-stu-id="ef436-141">Full settlement</span></span>
<span data-ttu-id="ef436-142">顧客は、残り金額は支払われないものの**買掛金勘定パラメーター** ページで指定された過少支払金額よりも大きな一部支払を行う場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef436-142">Customers might make a partial payment where the remaining amount won't be paid but is greater than the underpayment amount that is specified on the **Account payable parameters** page.</span></span> <span data-ttu-id="ef436-143">完全に決済されるように請求書にマークするには、**トランザクションの決済**ページの [**全額決済**] オプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ef436-143">If you want to mark the invoice as fully settled, you can use the **Full settlement** option on the **Settle transaction** page.</span></span> <span data-ttu-id="ef436-144">(コンフィギュレーション キーを使用して全額決済機能を有効にできます)。 たとえば、請求書に 1,000.00 が転記され、顧客は 990.00 の支払を行います。</span><span class="sxs-lookup"><span data-stu-id="ef436-144">(You can enable the full settlement functionality by using a configuration key.) For example, an invoice is posted for 1,000.00, and the customer makes a payment of 990.00.</span></span> <span data-ttu-id="ef436-145">顧客が残りの 10.00 を支払う必要がないことに合意します。</span><span class="sxs-lookup"><span data-stu-id="ef436-145">You've agreed that the customer doesn't have to pay the remaining 10.00.</span></span> <span data-ttu-id="ef436-146">決済の請求書にマークした後、選択をマーク**全額決済**することができます。</span><span class="sxs-lookup"><span data-stu-id="ef436-146">After you mark the invoice for settlement, you can also mark select **Full settlement**.</span></span> <span data-ttu-id="ef436-147">請求書は、完全に決済されたとみなされます。</span><span class="sxs-lookup"><span data-stu-id="ef436-147">The invoice will then be considered fully settled.</span></span> <span data-ttu-id="ef436-148">差額 10.00 が、追加の現金割引量として現金割引口座に転記されます。</span><span class="sxs-lookup"><span data-stu-id="ef436-148">The 10.00 difference is posted to a cash discount account as an additional cash discount amount.</span></span>


<span data-ttu-id="ef436-149">詳細については、「[顧客支払の預金](tasks/deposit-customer-payments.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef436-149">For more information, see [Deposit customer payments](tasks/deposit-customer-payments.md).</span></span>

