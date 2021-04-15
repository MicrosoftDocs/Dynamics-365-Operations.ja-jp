---
title: 輸送管理での運賃の調整
description: このトピックでは、運賃調整プロセスについて説明します。
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809089"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="9857f-103">輸送管理での運賃の調整</span><span class="sxs-lookup"><span data-stu-id="9857f-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9857f-104">このトピックでは、運賃調整プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9857f-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="9857f-105">運賃の調整は手動で行うか、あるいは自動的に実行するよう設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9857f-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="9857f-106">運賃の自動調整を使用する場合は、どの運賃請求書が自動的に照合されるかを決定する基準を定義する監査マスターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="9857f-107">運賃調整プロセス</span><span class="sxs-lookup"><span data-stu-id="9857f-107">The freight reconciliation process</span></span>

<span data-ttu-id="9857f-108">運賃は、関連する出荷配送業者に関連付けられているレート エンジンによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="9857f-109">積荷が確認されると、運賃請求書が生成され、そこに運賃が転送されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="9857f-110">運賃は通常の請求プロセスに使用される設定に応じて、関連する元伝票 (発注書、販売注文、または移動オーダー) に雑費として配賦されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="9857f-111">運賃調整プロセス (照合プロセスとも呼ばれます) は、出荷配送業者から運賃請求書が到着次第開始できます。</span><span class="sxs-lookup"><span data-stu-id="9857f-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="9857f-112">請求書は電子ファイルで、または紙面で受領することができます。</span><span class="sxs-lookup"><span data-stu-id="9857f-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="9857f-113">紙の請求書を受領した場合は、運賃請求書をテンプレートとして使用して電子請求書を生成できます。</span><span class="sxs-lookup"><span data-stu-id="9857f-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="9857f-114">[![運賃調整プロセス](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="9857f-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="9857f-115">手動調整</span><span class="sxs-lookup"><span data-stu-id="9857f-115">Manual reconciliation</span></span>

<span data-ttu-id="9857f-116">運賃を手動で調整する場合は、請求書の各明細行を、運賃請求書の明細行または請求対象となっている積荷の明細行と照合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="9857f-117">この照合は **運賃請求書と請求書の照合** ページで行います。</span><span class="sxs-lookup"><span data-stu-id="9857f-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="9857f-118">請求明細行の金額が運賃請求書の金額と一致しない場合は、差額を調整する理由を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="9857f-119">調整する理由が複数ある場合は、一致しない金額をそれら全体に分割できます。</span><span class="sxs-lookup"><span data-stu-id="9857f-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="9857f-120">調整の理由によって、差額の総勘定元帳への転記方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="9857f-121">請求書の全額の調整が明確にされると、承認のため送信され、仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="9857f-122">次の図で、運賃請求書の生成および運賃調整の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9857f-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="9857f-123">[![運賃調整のタスク](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="9857f-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="9857f-124">自動調整</span><span class="sxs-lookup"><span data-stu-id="9857f-124">Automatic reconciliation</span></span>

<span data-ttu-id="9857f-125">自動調整を使用する場合は、調整のスケジュール、および請求書や使用する出荷配送業者を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="9857f-126">請求明細行と運賃請求書の照合は、監査マスターの設定および運賃請求書タイプに従って行われます。</span><span class="sxs-lookup"><span data-stu-id="9857f-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="9857f-127">自動調整の実行後、システムが照合できないすべての請求書を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="9857f-128">支払に向けすべての請求書を転記する前に、これらの請求書を手動で処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="9857f-129">自動または手動の調整を使用した運賃請求書との運賃請求書の照合</span><span class="sxs-lookup"><span data-stu-id="9857f-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="9857f-130">*照合* は、各運賃請求書に対応する運賃請求書を探すプロセスです。</span><span class="sxs-lookup"><span data-stu-id="9857f-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="9857f-131">請求書明細行を 1 対 1 で照合するか (手動照合) するか、利用可能なすべての請求書を一度に照合します (自動照合)。</span><span class="sxs-lookup"><span data-stu-id="9857f-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="9857f-132">自動照合</span><span class="sxs-lookup"><span data-stu-id="9857f-132">Auto matching</span></span>

<span data-ttu-id="9857f-133">複数の運賃請求書を同じ運賃請求書に照合する場合は、自動照合のプロセスは次のように機能します。</span><span class="sxs-lookup"><span data-stu-id="9857f-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="9857f-134">一致しない運賃請求書はすべて金額で並べ替えされ、最大金額が最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="9857f-135">運賃請求書は、運賃請求書の金額が正の金額が残るまで、1 対 1 で照合されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="9857f-136">監査マスターの設定と運賃請求書の残額に応じて、残りの金額が設定されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="9857f-137">手動による照合</span><span class="sxs-lookup"><span data-stu-id="9857f-137">Manual matching</span></span>

<span data-ttu-id="9857f-138">正の金額を持つすべての運賃請求書を照合できます。</span><span class="sxs-lookup"><span data-stu-id="9857f-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="9857f-139">自動照合と同様に、ユーザーは運賃請求書を負の金額と完全に一致しない運賃請求書と照合することができます。</span><span class="sxs-lookup"><span data-stu-id="9857f-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="9857f-140">例</span><span class="sxs-lookup"><span data-stu-id="9857f-140">Example</span></span>

<span data-ttu-id="9857f-141">金額が 1500 の運賃請求書 (FB) がある場合に、次の設定に従って各請求書に1つの請求明細を含む 3 件の運賃請求書を作成したとします。</span><span class="sxs-lookup"><span data-stu-id="9857f-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="9857f-142">元の運賃請求書 (BS) : 金額 1500</span><span class="sxs-lookup"><span data-stu-id="9857f-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="9857f-143">請求書 1 (Inv1): 金額 1000</span><span class="sxs-lookup"><span data-stu-id="9857f-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="9857f-144">請求書 2 (Inv2): 金額 600</span><span class="sxs-lookup"><span data-stu-id="9857f-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="9857f-145">請求書 3 (Inv3): 金額 -100</span><span class="sxs-lookup"><span data-stu-id="9857f-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="9857f-146">自動照合結果</span><span class="sxs-lookup"><span data-stu-id="9857f-146">Automatic matching result</span></span>

<span data-ttu-id="9857f-147">自動照合は次の順序で実行されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="9857f-148">すべての運賃請求書を金額で降順に並べ替える: Inv1 -> Inv2 -> Inv3。</span><span class="sxs-lookup"><span data-stu-id="9857f-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="9857f-149">Inv1 と FB を照合します。</span><span class="sxs-lookup"><span data-stu-id="9857f-149">Match Inv1 with FB.</span></span> <span data-ttu-id="9857f-150">Inv1 の一致金額が 1000、残りの金額が 500 の場合、ステータスは *部分的に一致* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9857f-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="9857f-151">Inv2 と FB を照合します。</span><span class="sxs-lookup"><span data-stu-id="9857f-151">Match Inv2 with FB.</span></span> <span data-ttu-id="9857f-152">Inv2 の一致金額が 500、残りの金額が 0 の場合、ステータスは *完全に一致* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9857f-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="9857f-153">FB は完全に一致するので、EDV3 は処理されません。</span><span class="sxs-lookup"><span data-stu-id="9857f-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="9857f-154">手動照合結果</span><span class="sxs-lookup"><span data-stu-id="9857f-154">Manual matching result</span></span>

<span data-ttu-id="9857f-155">手動照合の場合、次の例に示す順序で結果が異なります。</span><span class="sxs-lookup"><span data-stu-id="9857f-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="9857f-156">手動照合ケース 1</span><span class="sxs-lookup"><span data-stu-id="9857f-156">Manual matching case 1</span></span>

<span data-ttu-id="9857f-157">この例で手動照合を行う 1 つの方法は、次のように処理します。</span><span class="sxs-lookup"><span data-stu-id="9857f-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="9857f-158">Inv1 と FB を照合します。</span><span class="sxs-lookup"><span data-stu-id="9857f-158">Match FB with Inv1.</span></span> <span data-ttu-id="9857f-159">FB の残金額が 500 ある場合、ステータスは *部分的に一致* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9857f-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="9857f-160">Inv2 と FB を照合します。</span><span class="sxs-lookup"><span data-stu-id="9857f-160">Match Inv2 with FB.</span></span> <span data-ttu-id="9857f-161">Inv2 の一致金額が 500、残りの金額が 0 の場合、ステータスは *完全に一致* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9857f-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="9857f-162">Inv3 と手動照合を行う場合は、一致しない運賃請求書は見つかりません。</span><span class="sxs-lookup"><span data-stu-id="9857f-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="9857f-163">このケースは基本的に自動照合と同じです</span><span class="sxs-lookup"><span data-stu-id="9857f-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="9857f-164">手動照合ケース 2</span><span class="sxs-lookup"><span data-stu-id="9857f-164">Manual matching case 2</span></span>

<span data-ttu-id="9857f-165">この例で手動照合を行うもう一つの方法は、次のように処理します。</span><span class="sxs-lookup"><span data-stu-id="9857f-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="9857f-166">Inv3 と FB を照合します。</span><span class="sxs-lookup"><span data-stu-id="9857f-166">Match Inv3 with FB.</span></span> <span data-ttu-id="9857f-167">これで、残額が 1600 で、1500 を超える金額から負の 100 が差し引かれた金額になります。</span><span class="sxs-lookup"><span data-stu-id="9857f-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="9857f-168">FB と Inv3 の両方が -100 と一致します。</span><span class="sxs-lookup"><span data-stu-id="9857f-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="9857f-169">INv1 と Inv 2 を FB と一つずつ一致させます。</span><span class="sxs-lookup"><span data-stu-id="9857f-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="9857f-170">FB は完全に一致します。</span><span class="sxs-lookup"><span data-stu-id="9857f-170">FB is fully matched.</span></span>

<span data-ttu-id="9857f-171">この例に示すように、運賃請求書と負の金額の照合は手動でのみ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9857f-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="9857f-172">これにより、照合順序を制御できるので、運賃請求書を負の金額と完全に照合できない運賃請求書と照合することができます。</span><span class="sxs-lookup"><span data-stu-id="9857f-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]