---
title: 決済の概要
description: このトピックは、決済プロセスに関する一般情報を提供します。 決済できるトランザクションのタイプ、トランザクションの決済時期と決済方法、および決済プロセスの結果について説明します。
author: kweekley
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b8b25575d5956e1345934512a7fe6503202b67a9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178676"
---
# <a name="settlement-overview"></a><span data-ttu-id="945e5-104">決済の概要</span><span class="sxs-lookup"><span data-stu-id="945e5-104">Settlement overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="945e5-105">このトピックは、決済プロセスに関する一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="945e5-105">This topic provides general information about the settlement process.</span></span> <span data-ttu-id="945e5-106">決済できるトランザクションのタイプ、トランザクションの決済時期と決済方法、および決済プロセスの結果について説明します。</span><span class="sxs-lookup"><span data-stu-id="945e5-106">It describes the types of transactions that can be settled, when and how transactions can be settled, and the results of the settlement process.</span></span>

<span data-ttu-id="945e5-107">決済時に、1 通の文書のトランザクションが、別のドキュメントのトランザクションに適用され、各ドキュメントの残高が増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="945e5-107">During settlement, the transactions on one document are applied to the transactions on another document to increase or decrease the balance of each document.</span></span> <span data-ttu-id="945e5-108">たとえば、支払は請求書に適用できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-108">For example, a payment can be applied to an invoice.</span></span> <span data-ttu-id="945e5-109">さまざまなトランザクション タイプを、別々の時間に、さまざまな方法で決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-109">Various transaction types can be settled, at different times, and through various methods.</span></span> <span data-ttu-id="945e5-110">決済は、新しいトランザクションの生成につながることがあります。</span><span class="sxs-lookup"><span data-stu-id="945e5-110">Settlement can also cause new transactions to be generated.</span></span>

## <a name="what-transactions-can-be-settled"></a><span data-ttu-id="945e5-111">どのトランザクションが決済できるか</span><span class="sxs-lookup"><span data-stu-id="945e5-111">What transactions can be settled</span></span>
<span data-ttu-id="945e5-112">[買掛金勘定] 内の決済および [受取勘定] は、請求書、支払、クレジット メモ、手数料など、仕入先の残高または顧客残高に影響を与える任意のトランザクション タイプの間で発生します。</span><span class="sxs-lookup"><span data-stu-id="945e5-112">Settlement within Accounts payable and Account receivable can occur between any transaction types that affect the vendor balance or customer balance, such as invoices, payments, credit memos, and fees.</span></span> <span data-ttu-id="945e5-113">すべてのトランザクション タイプが、任意の他のトランザクション タイプに対して決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-113">Any transaction type can be settled against any other transaction type.</span></span> <span data-ttu-id="945e5-114">たとえば、請求書に対して支払、請求書に対してクレジット メモ、請求書に対して請求書、支払に対して支払を決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-114">For example, you can settle a payment against an invoice, a credit memo against an invoice, an invoice against an invoice, and a payment against a payment.</span></span> <span data-ttu-id="945e5-115">同じ法人または別の法人の中で、トランザクションに対して支払を決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-115">You can settle payments against a transaction in the same legal entity or in a different legal entity.</span></span> <span data-ttu-id="945e5-116">集中支払用のモデルを使用している組織では、[集中支払](set-up-centralized-payments.md) が支払プロセスを合理化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="945e5-116">In organizations that use a centralized payment model, [centralized payments](set-up-centralized-payments.md) can help streamline the payment process.</span></span>

## <a name="when-to-settle-transactions"></a><span data-ttu-id="945e5-117">トランザクションを決済する時期</span><span class="sxs-lookup"><span data-stu-id="945e5-117">When to settle transactions</span></span>
<span data-ttu-id="945e5-118">トランザクションは、支払入力時に決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-118">Transactions can be settled at the time of payment entry.</span></span> <span data-ttu-id="945e5-119">たとえば、仕入先への支払を行う場合、通常、支払を行う請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="945e5-119">For example, when you make a payment to a vendor, you typically select the invoices to pay.</span></span> <span data-ttu-id="945e5-120">請求書を選択することによって、支払に対して決済のマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="945e5-120">By selecting invoices, you mark them for settlement against the payment.</span></span> <span data-ttu-id="945e5-121">売掛金勘定支払係が顧客支払を記録すると、顧客支払に含まれる情報に基づいて、決済する適切な請求書にマークを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-121">When Accounts Receivable payment clerks record a customer payment, they can mark the appropriate invoices for settlement, based on the information that is included with the customer's payment.</span></span> <span data-ttu-id="945e5-122">**トランザクションの決済**ページで、決済するトランザクションをマークします。</span><span class="sxs-lookup"><span data-stu-id="945e5-122">The **Settle transactions** page is used to mark transactions for settlement.</span></span> <span data-ttu-id="945e5-123">このページは、未転記の請求書または支払から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-123">This page can be opened from any unposted invoice or payment.</span></span> <span data-ttu-id="945e5-124">トランザクションが転記されると、決済も転記されます。</span><span class="sxs-lookup"><span data-stu-id="945e5-124">When the transaction is posted, the settlement is also posted.</span></span> <span data-ttu-id="945e5-125">トランザクションの決済は、転記後に行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="945e5-125">Transactions can also be settled after they are posted.</span></span> <span data-ttu-id="945e5-126">任意の請求書に対して、決済せずに、顧客支払の入力および転記を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-126">You can enter and post a customer payment without settling it against any invoices.</span></span> <span data-ttu-id="945e5-127">ただし、正しい請求書に対して支払が決済されるように、先に調査を行う必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="945e5-127">However, you might have to do research first, to make sure that the payment is settled against the correct invoice.</span></span> <span data-ttu-id="945e5-128">**トランザクションの決済** ページは、**すべての顧客** または **すべての仕入先**ページから開くことができます。また、任意の顧客または仕入先の**トランザクション** ページから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-128">The **Settle transactions** page can be opened from the **All customers** or **All vendors** page, or from the **Transactions** page for any customer or vendor.</span></span> <span data-ttu-id="945e5-129">また、発注書または販売注文に対して決済の支払をマークすると、請求書の転記された前払の引当を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-129">You can also reserve posted prepayments for an invoice by marking the payment for settlement against a purchase order or sales order.</span></span> <span data-ttu-id="945e5-130">この場合、支払にまだ未処理残高がありますが、他の請求書に対しては決済できません。</span><span class="sxs-lookup"><span data-stu-id="945e5-130">In this case, the payment will still have an open balance, but it can't be settled against another invoice.</span></span> <span data-ttu-id="945e5-131">支払は、発注書または販売注文から作成された請求書に対して自動的に決済されます。</span><span class="sxs-lookup"><span data-stu-id="945e5-131">The payment will be automatically settled against the invoice that is created from the purchase order or sales order.</span></span>

## <a name="how-to-settle-transactions"></a><span data-ttu-id="945e5-132">トランザクションの決済方法</span><span class="sxs-lookup"><span data-stu-id="945e5-132">How to settle transactions</span></span>
<span data-ttu-id="945e5-133">トランザクションは、手動、自動、またはこれらの組み合わせで決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-133">Transactions can be settled manually, automatically, or by using a combination of the two methods.</span></span> <span data-ttu-id="945e5-134">決済方法の選択は、[買掛金勘定パラメーター] と [売掛金勘定パラメーター] の決済の設定によって実行できる業務プロセスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="945e5-134">The choice of a settlement method depends on business processes, which can then be implemented through the setup of settlement in Accounts payable parameters and Accounts receivable parameters.</span></span> <span data-ttu-id="945e5-135">支払提案を使用して、支払を行う請求書を選択することにより、仕入先支払および顧客の口座引落支払を作成できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-135">You can create vendor payments and customer direct debit payments by using a payment proposal, which is used to select invoices to pay.</span></span> <span data-ttu-id="945e5-136">支払提案は手動で開始され、Dynamics 365 Financeは支払の作成時に、決済を選択した請求書を自動的にマークします。</span><span class="sxs-lookup"><span data-stu-id="945e5-136">The payment proposal is manually initiated, and then Dynamics 365 Finance automatically marks the selected invoices for settlement when the payments are created.</span></span> <span data-ttu-id="945e5-137">支払を手動で作成した場合、**トランザクションの決済**ページを使用して、決済する請求書を選択できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-137">If payments are created manually, you can use the **Settle transactions** page to select invoices for settlement.</span></span> <span data-ttu-id="945e5-138">請求書は手動で選択できます。また、**優先順位別にマーク** オプションを使用して、請求書を自動的に決済用にマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-138">You can manually select the invoices, or you can use the **Mark by priority** option to have invoices automatically marked for settlement.</span></span> <span data-ttu-id="945e5-139">**優優先順位別にマーク** オプションは、[売掛金勘定] にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-139">The **Mark by priority** option is available only for Accounts receivable.</span></span> <span data-ttu-id="945e5-140">このオプションを有効にするには、売掛金勘定パラメーターの**決済の優先順位**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="945e5-140">To enable this option, use the **Settlement priority** page in Accounts receivable parameters.</span></span> <span data-ttu-id="945e5-141">支払係が支払の入力は行い、転記前にその支払の決済を行っていない場合は、支払は自動的に決済できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-141">If a payment clerk enters a payment but doesn’t settle that payment before it is posted, the payment can be automatically settled.</span></span> <span data-ttu-id="945e5-142">[売掛金勘定パラメータ] および [買掛金勘定パラメータ] の自動決済を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="945e5-142">You can enable automatic settlement in Accounts receivable parameters and Accounts payable parameters.</span></span> <span data-ttu-id="945e5-143">自動決済は、同じ法人内でトランザクションを決済し、複数の法人間で決済することはありません。</span><span class="sxs-lookup"><span data-stu-id="945e5-143">Automatic settlement settles transactions within the same legal entity and does not settle across multiple legal entities.</span></span> <span data-ttu-id="945e5-144">自動決済を使用すると、事前に定義された決済順序を使用できます。また、[売掛金勘定パラメーター] で独自の決済の優先順位を定義できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-144">When you use automatic settlement, you can use the predefined settlement order, or you can define your own settlement priority order in Accounts receivable parameters.</span></span> <span data-ttu-id="945e5-145">この機能は、[売掛金勘定] にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-145">This functionality is available only for Accounts receivable.</span></span>

## <a name="results-of-settlement"></a><span data-ttu-id="945e5-146">決済の結果</span><span class="sxs-lookup"><span data-stu-id="945e5-146">Results of settlement</span></span>
<span data-ttu-id="945e5-147">トランザクションを決済すると、各トランザクションの未払残高はそれに応じて増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="945e5-147">As transactions are settled, the outstanding balance of each transaction is increased or decreased as appropriate.</span></span> <span data-ttu-id="945e5-148">請求書や支払が決済される一般的なシナリオでは、各トランザクションの状態や残高は次のルールに従って更新されます。</span><span class="sxs-lookup"><span data-stu-id="945e5-148">In a typical scenario, where an invoice and payment are settled, the status and balance of each transaction is updated according to the following rules:</span></span>

-   <span data-ttu-id="945e5-149">支払金額が請求金額を超える場合、請求書残高は 0.00 に減少し、請求書は終了済になります。</span><span class="sxs-lookup"><span data-stu-id="945e5-149">If the payment amount is more than the invoice amount, the invoice balance is reduced to 0.00, and the invoice is closed.</span></span> <span data-ttu-id="945e5-150">支払は未処理のままで、残高は、支払が請求金額を超えた金額になります。</span><span class="sxs-lookup"><span data-stu-id="945e5-150">The payment remains open, and the balance is the amount by which the payment exceeds the invoice amount.</span></span>
-   <span data-ttu-id="945e5-151">支払金額が請求金額に満たない場合、支払残高は 0.00 に減少し、支払は終了済になります。</span><span class="sxs-lookup"><span data-stu-id="945e5-151">If the payment amount is less than the invoice amount, the payment balance is reduced to 0.00, and the payment is closed.</span></span> <span data-ttu-id="945e5-152">請求書は未処理のままで、残高は、請求書の過少支払の金額になります。</span><span class="sxs-lookup"><span data-stu-id="945e5-152">The invoice remains open, and the balance is the amount by which the payment underpaid the invoice.</span></span>
-   <span data-ttu-id="945e5-153">支払金額が請求金額と等しい場合は、支払と請求書の両方が閉じ、両方の残高は 0.00 になります。</span><span class="sxs-lookup"><span data-stu-id="945e5-153">If the payment amount equals the invoice amount, both the payment and the invoice are closed, and the balance of both is 0.00.</span></span>

<span data-ttu-id="945e5-154">現金割引、控除、過少支払により[支払が請求金額より少ない](../accounts-payable/vendor-payments-partial-amount.md)場合、[買掛金勘定パラメーター] および [売掛金勘定パラメーター] の決済の設定によっては、請求書と支払が終了済になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="945e5-154">If a [payment is less than the invoice amount](../accounts-payable/vendor-payments-partial-amount.md) because of a cash discount, write-off, or underpayment, the invoice and payment might still be closed, depending on the setup of settlement in Accounts payable parameters and Accounts receivable parameters.</span></span> <span data-ttu-id="945e5-155">決済は、トランザクションを生成できます。</span><span class="sxs-lookup"><span data-stu-id="945e5-155">Settlement can also generate transactions.</span></span> <span data-ttu-id="945e5-156">たとえば、請求書および支払の決済で、現金割引、実現利益や損失、売上税の調整、控除、小額差分を生成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="945e5-156">For example, the settlement of an invoice and payment might produce a cash discount, realized gain or loss, sales tax adjustments, write-offs, or penny differences.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="945e5-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="945e5-157">Additional resources</span></span>
- [<span data-ttu-id="945e5-158">残余決済</span><span class="sxs-lookup"><span data-stu-id="945e5-158">Settle remainder</span></span>](settle-remainder.md)
