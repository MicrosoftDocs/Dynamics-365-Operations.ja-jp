---
title: 受取手形の設定
description: このトピックでは、為替手形を設定するための手順を説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7f5f62d33f6ffedb3fcefcdd9a83b922c1588df0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445089"
---
# <a name="set-up-bills-of-exchange"></a><span data-ttu-id="4af2f-103">受取手形の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-103">Set up bills of exchange</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4af2f-104">このトピックでは、為替手形を設定するための手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-104">This topic describes the steps for setting up bills of exchange.</span></span>

<span data-ttu-id="4af2f-105">為替手形は、記載されている金額を他者 (通常は銀行) が会社に支払うことを指示する、顧客からの文書注文または電子注文です。</span><span class="sxs-lookup"><span data-stu-id="4af2f-105">A bill of exchange is a written or electronic order from a customer that specifies that another party, usually a bank, should pay a stated amount to the company.</span></span> <span data-ttu-id="4af2f-106">為替手形を販売注文請求書または自由書式の請求書の支払に使用する場合は、顧客勘定の貸方に記入します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-106">When you use a bill of exchange as payment for a sales order invoice or free text invoice, you credit the customer account.</span></span> <span data-ttu-id="4af2f-107">この貸方は、顧客が銀行に為替手形を支払うまで、為替手形で担保が付けられます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-107">That credit is secured by the bill of exchange until the customer pays the bill of exchange to the bank.</span></span> <span data-ttu-id="4af2f-108">通常、為替手形による請求書の決済は期日までに完了します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-108">Typically, you will settle the invoice with the bill of exchange on the due date.</span></span> <span data-ttu-id="4af2f-109">銀行から為替手形の受取済通知を受領したら、為替手形を決済できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-109">When you receive notification from your bank that the bill of exchange has been honored, you can close the bill of exchange.</span></span> <span data-ttu-id="4af2f-110">以下の時点で銀行から為替手形を振出できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-110">You can draw a bill of exchange through your bank at either of the following times:</span></span>

-   <span data-ttu-id="4af2f-111">期日になったとき。</span><span class="sxs-lookup"><span data-stu-id="4af2f-111">On the due date.</span></span> <span data-ttu-id="4af2f-112">この方法を取立依頼と呼びます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-112">This approach is known as remit for collection.</span></span>
-   <span data-ttu-id="4af2f-113">期日前の、通常は顧客に対して設定された支払条件で指定された割引日。</span><span class="sxs-lookup"><span data-stu-id="4af2f-113">Before the due date, typically on the discount date that is specified in the terms of payment that are set up for the customer.</span></span> <span data-ttu-id="4af2f-114">トランザクションを転記すると、割引額が費用勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-114">When you post the transaction, the discount amount is posted to an expense account.</span></span> <span data-ttu-id="4af2f-115">残りの金額は銀行が顧客から支払を受けるまで負債になります。</span><span class="sxs-lookup"><span data-stu-id="4af2f-115">The remaining amount is a liability to you until the bank receives payment from the customer.</span></span> <span data-ttu-id="4af2f-116">この方法を割引依頼と呼びます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-116">This approach is known as remit for discount.</span></span>

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a><span data-ttu-id="4af2f-117">為替手形の転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-117">Set up posting profiles for bills of exchange</span></span>

<span data-ttu-id="4af2f-118">**顧客転記プロファイル** ページを使用して、為替手形、為替手形受取拒否、取立依頼、割引依頼に使用する転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-118">Use the **Customer posting profiles** page to set up posting profiles that you can use with bills of exchange, protest bills of exchange, remittances for collection, and remittances for discount.</span></span> <span data-ttu-id="4af2f-119">**集計勘定** フィールドで、為替手形の金額を転記する集計勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-119">In the **Summary account** field, select the summary account to post bill of exchange amounts to.</span></span> <span data-ttu-id="4af2f-120">この勘定は、受取手形トランザクションのタイプに応じて、借方または貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-120">This account is debited or credited, depending on the type of bill of exchange transaction:</span></span>
-   <span data-ttu-id="4af2f-121">為替手形の場合、この勘定では、為替手形を転記するときは借方に、割引依頼または取立依頼を転記するときは貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-121">For bills of exchange, this account is debited when a bill of exchange is posted, and it's credited when a remittance for discount or a remittance for collection is posted.</span></span>
-   <span data-ttu-id="4af2f-122">為替手形の受取拒否の場合、この勘定では、為替手形の受取拒否を転記するときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-122">For protest bills of exchange, this account is debited when a protest bill of exchange is posted.</span></span>
-   <span data-ttu-id="4af2f-123">取立依頼の場合、この勘定では、取立依頼を転記するときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-123">For remittances for collection, this account is debited when a remittance for collection is posted.</span></span>
-   <span data-ttu-id="4af2f-124">割引依頼の場合、この勘定では、割引依頼を転記するときに借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-124">For remittances for discount, this account is debited when a remittance for discount is posted.</span></span>

<span data-ttu-id="4af2f-125">**決済勘定** フィールドで、為替手形の金額を転記する現金勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-125">In the **Settle account** field, select the cash account to post bill of exchange amounts to.</span></span> <span data-ttu-id="4af2f-126">この勘定では、為替手形を決済するときに借方に記入されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-126">This account is debited when a bill of exchange is settled.</span></span> <span data-ttu-id="4af2f-127">**売上税の前払** フィールドで、為替手形で前払する売上税の金額を転記する集計勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-127">In the **Sales tax prepayments** field, select the summary account to post sales tax amounts to when bills of exchange are used for prepayments.</span></span> <span data-ttu-id="4af2f-128">**割引勘定負債** フィールドで、割引依頼の割引金額を転記する勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-128">In the **Liabilities for discount account** field, select the account to post the discount amount for remittances for discount to.</span></span> <span data-ttu-id="4af2f-129">この勘定では、割引依頼を転記するときに貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-129">This account is credited when a remittance for discount is posted.</span></span>

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a><span data-ttu-id="4af2f-130">受取手形の売掛金勘定パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-130">Set up Accounts receivable parameters for bills of exchange</span></span>

<span data-ttu-id="4af2f-131">**売掛金勘定パラメーター** ページで、受取手形の既定の転記プロファイルは **元帳と消費税** タブで入力されます。番号順序は **番号順序** で定義できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-131">On the **Accounts receivable parameters** page, the default posting profiles for bills of exchange are entered on the **Ledger and sales tax** tab. Number sequences are defined on the **Number sequences** tab.</span></span>

## <a name="set-up-journal-names-for-bills-of-exchange"></a><span data-ttu-id="4af2f-132">為替手形の仕訳帳名の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-132">Set up journal names for bills of exchange</span></span>


<span data-ttu-id="4af2f-133">**仕訳帳名** ページでは、為替手形に使用する仕訳帳名を 5 個以上作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-133">On the **Journals names** page, create at least five journal names to use for bills of exchange.</span></span> <span data-ttu-id="4af2f-134">仕訳帳のタイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-134">Here are the journal types:</span></span>
-   <span data-ttu-id="4af2f-135">**顧客振出受取手形** – 受取手形振出仕訳帳の仕訳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-135">**Customer draw bill of exchange** – Create a journal name for the Draw bill of exchange journal.</span></span>
-   <span data-ttu-id="4af2f-136">**顧客受取拒否受取手形** – 受取手形受取拒否仕訳帳の仕訳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-136">**Customer protest bill of exchange** – Create a journal name for the Protest bill of exchange journal.</span></span>
-   <span data-ttu-id="4af2f-137">**顧客再振出受取手形** – 受取手形再振出仕訳帳の仕訳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-137">**Customer redraw bill of exchange** – Create a journal name for the Redraw bill of exchange journal.</span></span>
-   <span data-ttu-id="4af2f-138">**顧客銀行送金為替** – 送金仕訳帳の仕訳帳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-138">**Customer bank remittance** – Create a journal name for the Remittance journal.</span></span>
-   <span data-ttu-id="4af2f-139">**顧客決済受取手形** – 受取手形決済仕訳帳の仕訳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-139">**Customer settle bill of exchange** – Create a journal name for the Settle bill of exchange journal.</span></span>

<span data-ttu-id="4af2f-140">それぞれの受取手形仕訳の仕訳伝票ページの、**受取手形** タブで受取手形に関する情報を入力します。転記済の為替手形仕訳帳明細行は、**受取手形仕訳帳照会** ページ、および **受取手形統計** ページで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-140">On the journal voucher page for each bill of exchange journal, enter information about the bill of exchange on the **Bill of exchange** tab. After the bill of exchange journal lines are posted, you can view them on the **Bill of exchange journal inquiry** page and the **Bills of exchange statistics** page.</span></span>

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a><span data-ttu-id="4af2f-141">為替手形の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-141">Set up methods of payment for bills of exchange</span></span>

<span data-ttu-id="4af2f-142">**支払方法** ページでは、受取手形の支払方法を少なくとも 1 つ設定します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-142">On the **Methods of payment** page, set up at least one method of payment for bills of exchange.</span></span> <span data-ttu-id="4af2f-143">複数の銀行を利用している場合は、各銀行の所定の受取手形送金形式に対応した支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-143">If you do business with more than one bank, set up a method of payment that corresponds to the remittance format that each bank requires for bills of exchange.</span></span>

## <a name="set-up-payment-fees-for-bills-of-exchange"></a><span data-ttu-id="4af2f-144">為替手形の支払手数料の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-144">Set up payment fees for bills of exchange</span></span>

<span data-ttu-id="4af2f-145">支払手数料は、顧客からの支払の回収プロセスに関連付けられた請求金額です。</span><span class="sxs-lookup"><span data-stu-id="4af2f-145">A payment fee is a charge that is associated with the process of collecting payments from customers.</span></span> <span data-ttu-id="4af2f-146">各支払手数料に複数の支払手数料設定明細行を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-146">Multiple payment fee setup lines can be associated each payment fee.</span></span> <span data-ttu-id="4af2f-147">設定明細行で、支払手数料の既定の金額の計算方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-147">You can use setup lines to control how default amounts for payment fees are calculated.</span></span> <span data-ttu-id="4af2f-148">たとえば、支払方法、支払仕様、通貨、および期間を設定する明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-148">For example, you can create setup lines for methods of payment, payment specifications, currencies, and time periods.</span></span> <span data-ttu-id="4af2f-149">また、日数間隔に基づいた割合や金額を設定する明細行も作成できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-149">You can also create setup lines for a percentage or amount that is based on day intervals.</span></span> <span data-ttu-id="4af2f-150">たとえば、支払が延滞した期間の長さに基づく利率を設定できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-150">For example, you can set up an interest percentage that is based on the length of time a payment is overdue.</span></span> <span data-ttu-id="4af2f-151">取引銀行が、**取立** や **割引** など送金タイプに応じて異なる手数料を課している場合は、送金タイプごとに別の支払明細行を設定します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-151">If the bank charges different fees for different remittance types, such as **Collection** or **Discount**, set up a separate payment fee line for each remittance type.</span></span>

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a><span data-ttu-id="4af2f-152">銀行送金ファイルの送金手数料の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-152">Set up remittance fees for bank remittance files</span></span>

<span data-ttu-id="4af2f-153">**銀行口座** ページでは、生成された各送金ファイルに銀行から請求される送金手数料を設定できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-153">On the **Bank accounts** page, you can set up remittance fees that a bank charges for each remittance file that is generated.</span></span> <span data-ttu-id="4af2f-154">送金手数料は送金が確認され、実際の手数料金額が判明した時点で転記されます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-154">The remittance fees are posted when the remittance has been confirmed and the realized fee amounts are known.</span></span> <span data-ttu-id="4af2f-155">送金手数料は、顧客から回収されて仕訳明細行に関連付けられる支払手数料とは異なります。</span><span class="sxs-lookup"><span data-stu-id="4af2f-155">Remittance fees differ from payment fees, which are collected from customers and attached to journal lines.</span></span>

## <a name="set-up-document-layouts-for-bills-of-exchange"></a><span data-ttu-id="4af2f-156">為替手形のドキュメント レイアウトの設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-156">Set up document layouts for bills of exchange</span></span>

<span data-ttu-id="4af2f-157">**銀行口座** ページでは、**設定** をクリックし、受取手形ドキュメントを印刷する必要がある各銀行口座のドキュメント レイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="4af2f-157">On the **Bank accounts** page, click **Set up**, and specify the document layout that is required for each bank account that you will generate printed bills of exchange documents for.</span></span>

## <a name="set-up-customers-for-bills-of-exchange"></a><span data-ttu-id="4af2f-158">為替手形の顧客の設定</span><span class="sxs-lookup"><span data-stu-id="4af2f-158">Set up customers for bills of exchange</span></span>

<span data-ttu-id="4af2f-159">**顧客** ページでは、為替手形で支払を行う契約をした各顧客に対する為替手形の既定の支払方法を **支払の既定値** タブで設定できます。</span><span class="sxs-lookup"><span data-stu-id="4af2f-159">On the **Customers** page, for each customer who has agreed to pay by using a bill of exchange, you can set up a default method of payment for bills of exchange on the **Payment defaults** tab.</span></span>





