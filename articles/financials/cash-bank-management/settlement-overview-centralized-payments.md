---
title: "集中支払の決済の概要"
description: "複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。 これにより、複数の法人内の同一トランザクションを入力する必要がなくなり、集中支払の支払提案プロセス、決済プロセス、未処理トランザクションの編集、および決算済トランザクションの編集を効率化することで時間を節約できます。"
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b76b141531acfc2d1d7553a3e7a13f165373921b
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="settlement-overview-for-centralized-payments"></a><span data-ttu-id="9b780-104">集中支払の決済の概要</span><span class="sxs-lookup"><span data-stu-id="9b780-104">Settlement overview for centralized payments</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9b780-105">複数の法人を含む組織では、すべての支払を処理する法人を使用して支払を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-105">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="9b780-106">これにより、複数の法人内の同一トランザクションを入力する必要がなくなり、集中支払の支払提案プロセス、決済プロセス、未処理トランザクションの編集、および決算済トランザクションの編集を効率化することで時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-106">This eliminates the need to enter the same transaction in multiple legal entities and saves time by streamlining the payment proposal process, the settlement process, open transaction editing, and closed transaction editing for centralized payments.</span></span> 

<span data-ttu-id="9b780-107">顧客または仕入先支払が 1 件の法人に入力され、別の法人で入力した請求書とともに決済される場合、適切な決済、適切な借りトランザクションおよび借しトランザクションが、各法人に対して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-107">When a customer or vendor payment is entered in one legal entity and is settled with an invoice that was entered in another legal entity, the applicable settlement, due-to, and due-from transactions are automatically generated for each legal entity.</span></span> <span data-ttu-id="9b780-108">決済レコードは、トランザクション内の請求書および支払いの各組み合わせに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-108">A settlement record is created for each combination of invoice and payment in the transaction.</span></span> <span data-ttu-id="9b780-109">各決済レコードには、新しい伝票番号が割り当てられます。それは顧客に対しての [**売掛金勘定パラメータ**] ページおよび仕入先に対しての [**買掛金勘定パラメータ**] ページで指定された支払伝票の番号の順序シリーズに基づいています。</span><span class="sxs-lookup"><span data-stu-id="9b780-109">Each settlement record is assigned a new voucher number, which is based on the payment voucher number sequence series that is specified on the **Accounts receivable parameters** page for customers and on the **Accounts payable parameters** page for vendors.</span></span> 

<span data-ttu-id="9b780-110">追加決済レコードが、現金割引、外貨再評価、少額差分、過剰支払、または過少支払に対して生成された場合、それらに、後日の支払または請求トランザクションが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9b780-110">If additional settlement records are generated for cash discounts, foreign currency revaluations, penny differences, overpayments, or underpayments, they are assigned the later date of the payment or invoice transaction.</span></span> <span data-ttu-id="9b780-111">支払の転記後に決済が発生した場合、 決済レコードでは [**未処理トランザクションの決済**] ページで指定された決済転記日が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-111">If settlement occurs after the payment is posted, the settlement records use the settlement posting date that is specified on the **Settle open transactions** page.</span></span>
<span data-ttu-id="9b780-112">転記タイプ、トランザクション タイプ、および既定の説明</span><span class="sxs-lookup"><span data-stu-id="9b780-112">Posting types, transaction types, and default descriptions</span></span>
----------------------------------------------------------

<span data-ttu-id="9b780-113">会社間決済伝票トランザクションは、会社間決済の転記タイプ、会社間顧客決済、および会社間仕入先の決済トランザクション タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-113">Intercompany settlement voucher transactions use the intercompany settlement posting type, intercompany customer settlement, and intercompany vendor settlement transaction types.</span></span> <span data-ttu-id="9b780-114">トランザクション タイプの情報を [**既定の説明**] ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-114">You can set up information for the transaction type on the **Default descriptions** page.</span></span> 

<span data-ttu-id="9b780-115">単一会社決済と会社間決済では、次のトランザクション タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-115">The following transaction types are available for use in single-company and cross-company settlements:</span></span>

-   <span data-ttu-id="9b780-116">決済</span><span class="sxs-lookup"><span data-stu-id="9b780-116">Settlement</span></span>
-   <span data-ttu-id="9b780-117">現金割引</span><span class="sxs-lookup"><span data-stu-id="9b780-117">Cash discount</span></span>
-   <span data-ttu-id="9b780-118">外貨再評価 (実現および未実現の外貨再評価を含む)</span><span class="sxs-lookup"><span data-stu-id="9b780-118">Foreign currency revaluations (includes realized and unrealized foreign currency revaluations)</span></span>
-   <span data-ttu-id="9b780-119">少額差分</span><span class="sxs-lookup"><span data-stu-id="9b780-119">Penny difference</span></span>
-   <span data-ttu-id="9b780-120">過剰支払/過少支払</span><span class="sxs-lookup"><span data-stu-id="9b780-120">Overpayment/underpayment</span></span>

<span data-ttu-id="9b780-121">会社間決済伝票用の既定の説明も定義できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-121">You can also define default descriptions for intercompany settlement vouchers.</span></span>

<a name="currency-exchange-gains-or-losses"></a><span data-ttu-id="9b780-122">為替差益または差損</span><span class="sxs-lookup"><span data-stu-id="9b780-122">Currency exchange gains or losses</span></span>
---------------------------------

<span data-ttu-id="9b780-123">顧客トランザクションまたは仕入先トランザクションで使用される為替レートは、トランザクションと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-123">The exchange rate that is used for customer or vendor transactions is stored with the transaction.</span></span> <span data-ttu-id="9b780-124">通貨為替の実現差益または差損は、請求書の法人のための [**会社間会計**] ページの [**為替差益または差損の転記**] フィールドで選択されたオプションに基づき、請求書の法人または支払の法人に転記されます。 </span><span class="sxs-lookup"><span data-stu-id="9b780-124">Realized gains or losses for currency exchanges are posted to either the legal entity of the invoice or the legal entity of the payment, depending on the option that is selected in the **Post currency exchange gain or loss** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="9b780-125">この後の例では、次の通貨を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-125">The following examples use these currencies:</span></span>
-   <span data-ttu-id="9b780-126">支払会計通貨: EUR</span><span class="sxs-lookup"><span data-stu-id="9b780-126">Payment accounting currency: EUR</span></span>
-   <span data-ttu-id="9b780-127">請求書会計通貨: USD</span><span class="sxs-lookup"><span data-stu-id="9b780-127">Invoice accounting currency: USD</span></span>
-   <span data-ttu-id="9b780-128">支払トランザクションの通貨 : DKK</span><span class="sxs-lookup"><span data-stu-id="9b780-128">Payment transaction currency: DKK</span></span>
-   <span data-ttu-id="9b780-129">請求トランザクションの通貨 : CAD</span><span class="sxs-lookup"><span data-stu-id="9b780-129">Invoice transaction currency: CAD</span></span>

#### <a name="currency-calculations"></a><span data-ttu-id="9b780-130">通貨計算</span><span class="sxs-lookup"><span data-stu-id="9b780-130">Currency calculations</span></span>

<span data-ttu-id="9b780-131">ある法人に入力された請求書を、別の法人に入力された支払と共に決済する場合、支払トランザクションの通貨 (DKK) は、次の 3 つの手順で換算されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-131">When settling an invoice that is entered in one legal entity with a payment that is entered in another legal entity, the transaction currency of the payment (DKK) is converted in three steps:</span></span>
1.  <span data-ttu-id="9b780-132">支払する法人からの為替レートを使用して、支払の会計通貨 (EUR) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-132">Converted to the accounting currency of the payment (EUR), using the exchange rates from the legal entity of the payment.</span></span>
2.  <span data-ttu-id="9b780-133">請求書の会計通貨 (USD) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-133">Converted to the accounting currency of the invoice (USD).</span></span>
3.  <span data-ttu-id="9b780-134">請求書の法人からの為替レートを使用して、請求書のトランザクション通貨 (CAD) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-134">Converted to the transaction currency of the invoice (CAD), using the exchange rates from the legal entity of the invoice.</span></span>

<span data-ttu-id="9b780-135">換算プロセスでは、支払日現在の為替レートを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-135">The conversion process uses the exchange rates as of the payment date.</span></span> <span data-ttu-id="9b780-136">換算後の請求トランザクションの通貨 (CAD) での支払金額が請求金額 (CAD) に等しい場合、請求書は全額が支払われたと見なされます。</span><span class="sxs-lookup"><span data-stu-id="9b780-136">If the resulting payment amount in the transaction currency of the invoice (CAD) is equal to the invoice amount (CAD), the invoice is considered fully paid.</span></span> 

<span data-ttu-id="9b780-137">支払金額が入力されなかった支払仕訳帳から [**未処理トランザクションの決済**] ページを開いた場合、決済される金額は、[**未処理トランザクションの決済**] ページで決済対象として選択された請求書に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-137">When the **Settle open transactions** page is opened from a payment journal where the payment amount was not entered, the amount to settle is calculated based on the invoices that are selected for settlement on the **Settle open transactions** page.</span></span> <span data-ttu-id="9b780-138">決済金額は、次の 3 つの手順で換算されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-138">The amount to settle is converted in three steps:</span></span>
1.  <span data-ttu-id="9b780-139">請求書の法人からの支払日現在の為替レートを使用して、請求書の会計通貨 (USD) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-139">Converted to the accounting currency of the invoice (USD), using the exchange rates from the legal entity of the invoice as of the payment date.</span></span>
2.  <span data-ttu-id="9b780-140">請求書の法人からの支払日現在の為替レートを使用して、支払の会計通貨 (EUR) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-140">Converted to the accounting currency of the payment (EUR), using the exchange rates from the legal entity of the invoice as of the payment date.</span></span>
3.  <span data-ttu-id="9b780-141">支払トランザクションの通貨 (DKK) に換算します。</span><span class="sxs-lookup"><span data-stu-id="9b780-141">Converted to the transaction currency of the payment (DKK).</span></span>

<span data-ttu-id="9b780-142">[**未処理トランザクションの決済**] ページを閉じたときに、換算後の支払金額が支払仕訳帳明細行に転送されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-142">The resulting payment amount is transferred to the payment journal line when you close the **Settle open transactions** page.</span></span>

#### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a><span data-ttu-id="9b780-143">異なる会計通貨に起因する差益または差損の転記</span><span class="sxs-lookup"><span data-stu-id="9b780-143">Posting for gain or loss because of different accounting currencies</span></span>

<span data-ttu-id="9b780-144">為替差益または差損が存在する場合、その差益または差損は、支払の法人のための [**会社間会計**] ページの [**為替差益または差損の転記**] フィールドで指定された法人に転記されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-144">If there is a currency exchange gain or loss, the gain or loss is posted to the legal entity that is specified for the **Post currency exchange gain or loss** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="9b780-145">差益または差損量が転記された法人の会計通貨に差益または差損量が、その法人に対して定義されている為替レートを使用して換算されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-145">The gain or loss amount is converted to the accounting currency of the legal entity where the gain or loss amount is posted, using the exchange rate that is defined for that legal entity.</span></span>

<a name="cash-discounts"></a><span data-ttu-id="9b780-146">現金割引</span><span class="sxs-lookup"><span data-stu-id="9b780-146">Cash discounts</span></span>
--------------

<span data-ttu-id="9b780-147">会社間決済プロセス中に生成された現金割引は、支払法人用の [**会社間会計**] ページの [**現金割引の転記**] フィールドで選択されたオプションに応じて、請求書の法人または支払法人のいずれかに転記されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-147">Cash discounts that are generated during the cross-company settlement process are posted to either the legal entity of the invoice or the legal entity of the payment, depending on the option that is selected for the **Post cash discount** field on the **Intercompany accounting** page for the legal entity of the payment.</span></span> <span data-ttu-id="9b780-148">対応する決済トランザクションは請求書の法人に生成されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-148">A corresponding settlement transaction is generated in the legal entity of the invoice.</span></span>

<a name="overpayments-and-underpayments"></a><span data-ttu-id="9b780-149">過剰支払および過少支払</span><span class="sxs-lookup"><span data-stu-id="9b780-149">Overpayments and underpayments</span></span>
------------------------------

<span data-ttu-id="9b780-150">過剰支払、過少支払、および少額差分の許容範囲は、過剰支払の場合は支払法人に、過少支払の場合は請求書の法人に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-150">Overpayment, underpayment, and penny difference tolerances are determined based on the legal entity of the payment for overpayments, and on the legal entity of the invoice for underpayments.</span></span> <span data-ttu-id="9b780-151">使用される顧客の転記勘定は、顧客に対する [**売掛金勘定パラメータ**] ページの [**現金割引管理**] フィールド、および仕入先に対する [**買掛金勘定パラメータ**] ページの [**現金割引管理**] フィールドでの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="9b780-151">The posting account that is used is determined by the setting in the **Cash discount administration** field on the **Accounts receivable parameters** page for customers, and the **Cash discount administration** field on the **Accounts payable parameters** page for vendors.</span></span>

-   <span data-ttu-id="9b780-152">現金割引管理設定が [限定] の場合、または設定が [非限定] で、適用可能な現金割引が過剰支払法人とは別の法人に転記される場合は、顧客現金割引、仕入先現金割引、または会計通貨での小額差分に対して自動アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-152">If the cash discount administration setting is Specific, or if the setting is Unspecific and the applicable cash discount is posted in a different legal entity from the overpayment, the automatic account for Customer cash discount, Vendor cash discount, or Penny difference in accounting currency is used.</span></span> <span data-ttu-id="9b780-153">[**自動トランザクションの勘定**] ページでこれらの勘定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9b780-153">You can specify these accounts on the **Accounts for automatic transactions** page.</span></span>
-   <span data-ttu-id="9b780-154">現金割引管理設定が [非限定] であり、現金割引が過剰支払法人と同じ法人 (支払法人と請求書の法人が同じ) に転記される場合は、現金割引口座が調整されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-154">If the cash discount administration setting is Unspecific and the cash discount is posted in the same legal entity as the overpayment (the legal entity of the payment and the legal entity of the invoice are the same), the cash discount account is adjusted.</span></span> <span data-ttu-id="9b780-155">たとえば、3.00 の現金割引が使用できる 100.00 の請求書が  98.00 で決済された場合、現金割引勘定で 1.00 の調整が行われます。</span><span class="sxs-lookup"><span data-stu-id="9b780-155">For example, if an invoice for 100.00 with an available cash discount of 3.00 is settled with a payment for 98.00, the cash discount account is adjusted for 1.00.</span></span> <span data-ttu-id="9b780-156">正味割引金額は 2.00 になります。</span><span class="sxs-lookup"><span data-stu-id="9b780-156">The net discount amount is 2.00.</span></span>
-   <span data-ttu-id="9b780-157">現金割引管理設定が [非限定] の場合、現金割引は、過剰支払法人と同じ法人に転記され、過剰支払または過少支払は、現金割引がある複数の請求書で決済され、最後の請求書の現金割引勘定が調整されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-157">If the cash discount administration setting is Unspecific, the cash discount is posted in the same legal entity as the overpayment, and the overpayment or underpayment is settled with multiple invoices with cash discounts, the cash discount account for the last invoice is adjusted.</span></span>

<span data-ttu-id="9b780-158">選択した現金割引管理が [非限定] の場合、次のような状況でのみ、非限定支払決済ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-158">If the cash discount administration selection is Unspecific, unspecific payment settlement rules apply only in the following situations:</span></span>
-   <span data-ttu-id="9b780-159">過剰支払が存在する。</span><span class="sxs-lookup"><span data-stu-id="9b780-159">There is an overpayment.</span></span>
-   <span data-ttu-id="9b780-160">過剰支払が、現金割引がある 1 枚以上の請求書で決済される。</span><span class="sxs-lookup"><span data-stu-id="9b780-160">The overpayment is settled with one or more invoices that has a cash discount.</span></span>
-   <span data-ttu-id="9b780-161">現金割引が、過剰支払法人と同じ法人に転記される。</span><span class="sxs-lookup"><span data-stu-id="9b780-161">The cash discount is posted in the same legal entity as the overpayment.</span></span>

<span data-ttu-id="9b780-162">そのほかのすべての状況では、過剰支払または過少支払は、顧客現金割引、仕入先現金割引、または会計通貨での小額差分に対する自動勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-162">In all other situations, overpayments or underpayments are posted to the automatic account for Customer cash discount, Vendor cash discount, or Penny difference in accounting currency.</span></span>

## <a name="sales-tax"></a><span data-ttu-id="9b780-163">消費税</span><span class="sxs-lookup"><span data-stu-id="9b780-163">Sales tax</span></span>
<span data-ttu-id="9b780-164">売上税トランザクションは、最初に転記された法人に残ります。</span><span class="sxs-lookup"><span data-stu-id="9b780-164">Sales tax transactions remain in the legal entity where they were originally posted.</span></span> 

<span data-ttu-id="9b780-165">売上税が前払に対して転記された場合、会社間決済では、前払法人で前払にかかる売上税をリバースします。</span><span class="sxs-lookup"><span data-stu-id="9b780-165">If sales tax was posted for a prepayment, the cross-company settlement reverses the sales tax on the prepayment in the legal entity of the prepayment.</span></span> <span data-ttu-id="9b780-166">請求書の法人の税は、請求書の法人に残ります。</span><span class="sxs-lookup"><span data-stu-id="9b780-166">The taxes in the legal entity of the invoice remain in the legal entity of the invoice.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="9b780-167">会計分析コード</span><span class="sxs-lookup"><span data-stu-id="9b780-167">Financial dimensions</span></span>
<span data-ttu-id="9b780-168">顧客支払の場合、支払法人の借トランザクションと貸トランザクションは、決済される支払の売掛金集計勘定用に指定された会計分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-168">For customer payments, the due-to and due-from transactions in the legal entity of the payment use the financial dimensions that are specified for the accounts receivable summary account from the payment that is being settled.</span></span> <span data-ttu-id="9b780-169">請求書の法人では、借トランザクションと貸トランザクションは、決済される請求書の売掛金集計勘定用に指定された会計分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-169">In the legal entity of the invoice, due-to and due-from transactions use the financial dimensions that are specified for the accounts receivable summary account from the invoice that is being settled.</span></span> 

<span data-ttu-id="9b780-170">仕入先支払の場合、支払法人の借トランザクションと貸トランザクションは、決済される支払の買掛金集計勘定用に指定された会計分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-170">For vendor payments, the due-to and due-from transactions in the legal entity of the payment use the financial dimensions that are specified for the accounts payable summary account from the payment that is being settled.</span></span> <span data-ttu-id="9b780-171">請求書の法人では、借トランザクションと貸トランザクションは、決済される請求書の買掛金集計勘定用に指定された会計分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b780-171">In the legal entity of the invoice, due-to and due-from transactions use the financial dimensions that are specified for the accounts payable summary account from the invoice that is being settled.</span></span>

## <a name="withholding-tax"></a><span data-ttu-id="9b780-172">源泉徴収税</span><span class="sxs-lookup"><span data-stu-id="9b780-172">Withholding tax</span></span>
<span data-ttu-id="9b780-173">請求書に関連付けられている仕入先口座は、源泉徴収税計算するかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-173">The vendor account that is associated with the invoice is used to determine whether withholding tax should be calculated.</span></span> <span data-ttu-id="9b780-174">源泉徴収税を適用する場合は、請求書に関連付けられている法人で計算されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-174">If withholding tax applies, it is calculated in the legal entity that is associated with the invoice.</span></span> <span data-ttu-id="9b780-175">法人が異なる通貨を使用すると、請求書に関連付けられている法人の為替レートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b780-175">If the legal entities use different currencies, the exchange rate from the legal entity that is associated with the invoice is used.</span></span>






