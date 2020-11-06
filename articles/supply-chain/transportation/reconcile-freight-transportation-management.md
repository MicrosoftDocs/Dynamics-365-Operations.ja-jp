---
title: 輸送管理での運賃の調整
description: このトピックでは、運賃調整プロセスについて説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSFBDetailReconcile, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8472094ba532d531b15dc4e9f120646b2c3bbe96
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017302"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="5365b-103">輸送管理での運賃の調整</span><span class="sxs-lookup"><span data-stu-id="5365b-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5365b-104">このトピックでは、運賃調整プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5365b-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="5365b-105">運賃の調整は手動で行うか、あるいは自動的に実行するよう設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5365b-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="5365b-106">運賃の自動調整を使用する場合は、どの運賃請求書が自動的に照合されるかを決定する基準を定義する監査マスターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="5365b-107">運賃調整プロセス</span><span class="sxs-lookup"><span data-stu-id="5365b-107">The freight reconciliation process</span></span>
<span data-ttu-id="5365b-108">運賃は、関連する出荷配送業者に関連付けられているレート エンジンによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="5365b-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="5365b-109">積荷が確認されると、運賃請求書が生成され、そこに運賃が転送されます。</span><span class="sxs-lookup"><span data-stu-id="5365b-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="5365b-110">運賃は通常の請求プロセスに使用される設定に応じて、関連する元伝票 (発注書、販売注文、または移動オーダー) に雑費として配賦されます。</span><span class="sxs-lookup"><span data-stu-id="5365b-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="5365b-111">運賃調整プロセス (照合プロセスとも呼ばれます) は、出荷配送業者から運賃請求書が到着次第開始できます。</span><span class="sxs-lookup"><span data-stu-id="5365b-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="5365b-112">請求書は電子ファイルで、または紙面で受領することができます。</span><span class="sxs-lookup"><span data-stu-id="5365b-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="5365b-113">紙の請求書を受領した場合は、運賃請求書をテンプレートとして使用して電子請求書を生成できます。</span><span class="sxs-lookup"><span data-stu-id="5365b-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="5365b-114">[![運賃調整プロセス](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="5365b-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="5365b-115">手動調整</span><span class="sxs-lookup"><span data-stu-id="5365b-115">Manual reconciliation</span></span>
<span data-ttu-id="5365b-116">運賃を手動で調整する場合は、請求書の各明細行を、運賃請求書の明細行または請求対象となっている積荷の明細行と照合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="5365b-117">この照合は **運賃請求書と請求書の照合** ページで行います。</span><span class="sxs-lookup"><span data-stu-id="5365b-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="5365b-118">請求明細行の金額が運賃請求書の金額と一致しない場合は、差額を調整する理由を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="5365b-119">調整する理由が複数ある場合は、一致しない金額をそれら全体に分割できます。</span><span class="sxs-lookup"><span data-stu-id="5365b-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="5365b-120">調整の理由によって、差額の総勘定元帳への転記方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="5365b-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="5365b-121">請求書の全額の調整が明確にされると、承認のため送信され、仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="5365b-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="5365b-122">次の図で、運賃請求書の生成および運賃調整の方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5365b-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="5365b-123">[![運賃調整のタスク](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="5365b-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="5365b-124">自動調整</span><span class="sxs-lookup"><span data-stu-id="5365b-124">Automatic reconciliation</span></span>
<span data-ttu-id="5365b-125">自動調整を使用する場合は、調整のスケジュール、および請求書や使用する出荷配送業者を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="5365b-126">請求明細行と運賃請求書の照合は、監査マスターの設定および運賃請求書タイプに従って行われます。</span><span class="sxs-lookup"><span data-stu-id="5365b-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="5365b-127">自動調整の実行後、システムが照合できないすべての請求書を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="5365b-128">支払に向けすべての請求書を転記する前に、これらの請求書を手動で処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5365b-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



