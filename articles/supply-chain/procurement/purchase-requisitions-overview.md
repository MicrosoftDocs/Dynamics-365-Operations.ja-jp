---
title: 購買要求の概要
description: このトピックでは、購買要求ワークフローと、購買要求で発生する可能性のあるさまざまな状態について説明します。
author: mkirknel
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e09c4ebd3ee978076ac4f1d0b71041e7c1e954be
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826903"
---
# <a name="purchase-requisition-overview"></a><span data-ttu-id="c19fc-103">購買要求の概要</span><span class="sxs-lookup"><span data-stu-id="c19fc-103">Purchase requisition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c19fc-104">このトピックでは、購買要求ワークフローと、購買要求で発生する可能性のあるさまざまな状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-104">This topic describes the purchase requisition workflow and the different statuses that a purchase requisition can have.</span></span>

<span data-ttu-id="c19fc-105">組織の設定に基づいて、組織で使用される製品の購買要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-105">Depending on the setup of your organization, you can create purchase requisitions for products that your organization uses.</span></span> <span data-ttu-id="c19fc-106">購買要求は、購買部門が品目またはサービスを購入することを承認する内部ドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="c19fc-106">A purchase requisition is an internal document that authorizes the Purchasing department to buy items or services.</span></span>  

<span data-ttu-id="c19fc-107">購買要求が承認された後、購買要求を使用して発注書を生成できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-107">After a purchase requisition is approved, it can be used to generate a purchase order.</span></span> <span data-ttu-id="c19fc-108">発注書は、購買部門が仕入先に提出する外部ドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="c19fc-108">Purchase orders are the external documents that the Purchasing department submits to vendors.</span></span>

## <a name="creating-purchase-requisitions"></a><span data-ttu-id="c19fc-109">購買要求の作成</span><span class="sxs-lookup"><span data-stu-id="c19fc-109">Creating purchase requisitions</span></span>
<span data-ttu-id="c19fc-110">**自分の購買要求**ページで購買要求を作成して、必要な品目とサービスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-110">You can create a purchase requisition on the **My purchase requisitions** page, and select the items and services that you require.</span></span> <span data-ttu-id="c19fc-111">組織が作成した調達カタログから品目を選択するか、またはそのカタログに品目が見つからなかった場合は、調達カテゴリを選択し、製品の詳細を入力して品目を請求できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-111">You can select items from a procurement catalog that your organization has created, or you can request items that aren't found in a catalog by selecting a procurement category and entering the product details.</span></span>  

<span data-ttu-id="c19fc-112">購買要求をレビューのために送信する前に、ワークフローを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-112">Before you can submit a purchase requisition for review, workflows must be configured.</span></span> <span data-ttu-id="c19fc-113">ワークフローを使用して、確認プロセスを介して購買要求を**ドラフト**の最初のステータスから**承認済**の最後のステータスへ移動します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-113">You use a workflow to move a purchase requisition through the review process, from an initial status of **Draft** to a final status of **Approved**.</span></span>

### <a name="purchase-requisition-statuses"></a><span data-ttu-id="c19fc-114">購買要求のステータス</span><span class="sxs-lookup"><span data-stu-id="c19fc-114">Purchase requisition statuses</span></span>

<span data-ttu-id="c19fc-115">購買要求を作成すると、それにステータスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-115">When you create a purchase requisition, a status is assigned to it.</span></span> <span data-ttu-id="c19fc-116">購買要求に追加する各行にも、ステータスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-116">A status is also assigned to every line that you add to a purchase requisition.</span></span> <span data-ttu-id="c19fc-117">確認のために購買要求をワークフローに送信すると、明細行がワークフロー プロセスを移動するときに、購買要求のステータスと各明細行のステータスが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-117">When you submit a purchase requisition to a workflow for review, the status of the purchase requisition and the status of each line are updated as the lines move through the workflow process.</span></span>  

<span data-ttu-id="c19fc-118">購買要求ワークフロー プロセスは、購買要求を 1 つのドキュメントとして確認プロセス内を移動するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-118">You can configure the purchase requisition workflow process to route a purchase requisition through the review process as a single document.</span></span> <span data-ttu-id="c19fc-119">また、購買要求の明細行は、適切なレビュー担当者に個々にルーティングすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-119">Alternatively, the lines on a purchase requisition can be routed individually to the appropriate reviewers.</span></span> <span data-ttu-id="c19fc-120">購買要求の明細行が個々に確認される場合は、購買要求明細行が確認プロセス内を移動するときに各明細行のステータスを更新できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-120">If the purchase requisition lines are reviewed individually, the status of each purchase requisition line can be updated as the line moves through the review process.</span></span> <span data-ttu-id="c19fc-121">すべての明細行の確認プロセスが完了し、購買要求に対する確認ステップが残っていなければ、購買要求全体のステータスが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-121">When all lines have completed the review process and no review steps remain for the purchase requisition, the status of the whole purchase requisition is updated.</span></span>

### <a name="purchase-requisition-workflow"></a><span data-ttu-id="c19fc-122">購買要求ワークフロー</span><span class="sxs-lookup"><span data-stu-id="c19fc-122">Purchase requisition workflow</span></span>

<span data-ttu-id="c19fc-123">次の図は、購買要求と購買要求明細行がワークフロー プロセス内を移動するときに割り当てられるステータスを示しています。</span><span class="sxs-lookup"><span data-stu-id="c19fc-123">The following diagram shows the statuses that are assigned to a purchase requisition and a purchase requisition line as they move through the workflow process.</span></span>  

<span data-ttu-id="c19fc-124">[![購買要求のヘッダーと明細行のステータス](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span><span class="sxs-lookup"><span data-stu-id="c19fc-124">[![Purchase requisition header and line statuses](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)</span></span>

### <a name="purchase-requisition-header-and-line-status-relationships"></a><span data-ttu-id="c19fc-125">購買要求のヘッダーと明細行の状態の関係</span><span class="sxs-lookup"><span data-stu-id="c19fc-125">Purchase requisition header and line status relationships</span></span>

<span data-ttu-id="c19fc-126">購買要求の全般的なステータスは購買要求明細行のステータスによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-126">The overall status of a purchase requisition is determined by the status of the purchase requisition lines.</span></span> <span data-ttu-id="c19fc-127">したがって、すべての購買要求明細行の確認プロセスが完了しなければ、購買要求全体に対する確認プロセスは完了できません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-127">Therefore, the review process must be completed for all purchase requisition lines before the review process for the whole purchase requisition can be completed.</span></span> <span data-ttu-id="c19fc-128">次の表に、購買要求がワークフロー プロセスを移動するときに、購買要求のヘッダーと明細行に割り当てられるステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-128">The following table describes the statuses that are assigned to a purchase requisition header and lines as the purchase requisition moves through the workflow process.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c19fc-129">購買要求の状態</span><span class="sxs-lookup"><span data-stu-id="c19fc-129">Purchase requisition status</span></span></th>
<th><span data-ttu-id="c19fc-130">購買要求明細行の状態</span><span class="sxs-lookup"><span data-stu-id="c19fc-130">Purchase requisition line status</span></span></th>
<th><span data-ttu-id="c19fc-131">説明</span><span class="sxs-lookup"><span data-stu-id="c19fc-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c19fc-132">ドラフト</span><span class="sxs-lookup"><span data-stu-id="c19fc-132">Draft</span></span></td>
<td><span data-ttu-id="c19fc-133">ドラフト</span><span class="sxs-lookup"><span data-stu-id="c19fc-133">Draft</span></span></td>
<td><span data-ttu-id="c19fc-134">購買要求と購買要求明細行は作成済ですが、確認を受けるための送信は行われていません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-134">The purchase requisition and purchase requisition line have been created, but they haven&#39;t been submitted for review.</span></span> <span data-ttu-id="c19fc-135"><strong>ドラフト</strong> のステータスを持つ購買依頼と購買依頼行は変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-135">Purchase requisitions and purchase requisition lines that have a status of <strong>Draft</strong> can be modified.</span></span> <span data-ttu-id="c19fc-136">購買依頼または購買依頼行は、リコールされたがレビュー用に再送信されていない場合は、<strong>ドラフト</strong>のステータスも持っています。</span><span class="sxs-lookup"><span data-stu-id="c19fc-136">A purchase requisition or purchase requisition line also has a status of <strong>Draft</strong> if it has been recalled but hasn&#39;t been resubmitted for review.</span></span> <span data-ttu-id="c19fc-137"><strong>注意:</strong> 伝票レベルで購買要求を送信または呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-137"><strong>Note:</strong> You can submit or recall a purchase requisition at the document level.</span></span> <span data-ttu-id="c19fc-138">ただし、購買要求明細行を一行のみ送信または取り消すことはできません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-138">However, you can&#39;t submit or recall a single purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c19fc-139">確認中</span><span class="sxs-lookup"><span data-stu-id="c19fc-139">In review</span></span></td>
<td><ul>
<li><span data-ttu-id="c19fc-140">確認中</span><span class="sxs-lookup"><span data-stu-id="c19fc-140">In review</span></span></li>
<li><span data-ttu-id="c19fc-141">拒否済</span><span class="sxs-lookup"><span data-stu-id="c19fc-141">Rejected</span></span></li>
</ul></td>
<td><span data-ttu-id="c19fc-142">購買要求明細行を個々のレビュー担当者に転送するようにワークフローがコンフィギュレーションされている場合、各行は<strong>確認中</strong>または<strong>拒否済</strong>のステータスになることができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-142">If the workflow has been configured to route purchase requisition lines to individual reviewers, each line can have a status of <strong>In review</strong> or <strong>Rejected</strong>.</span></span> <span data-ttu-id="c19fc-143">すべての購買要求明細行の確認プロセスが完了し、購買要求に対する確認ステップが残っていなければ、購買要求のステータスが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-143">The purchase requisition status is updated when the review process is completed for all purchase requisition lines and no review steps remain for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="c19fc-144"><strong>確認中</strong> – 購買要求明細行が確認のために送信されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-144"><strong>In review</strong> – The purchase requisition lines have been submitted for review.</span></span> <span data-ttu-id="c19fc-145">購買要求明細行のワークフロー プロセスが完了しても、その明細行のステータスは、残りすべての購買要求明細行の確認が終了するまでは<strong>確認中</strong>のままです。</span><span class="sxs-lookup"><span data-stu-id="c19fc-145">When the workflow process is completed for a purchase requisition line, the status of that line remains <strong>In review</strong> until all remaining purchase requisition lines have been reviewed.</span></span></li>
<li><span data-ttu-id="c19fc-146"><strong>否認済</strong> – 購買要求明細行が否認されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-146"><strong>Rejected</strong> – A purchase requisition line has been rejected.</span></span> <span data-ttu-id="c19fc-147">否認された購買要求明細行は修正し、再送信できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-147">Purchase requisition lines that are rejected can be modified and resubmitted.</span></span></li>
</ul>
<span data-ttu-id="c19fc-148">否認された購買要求明細行を再送信すると、購買要求の明細行でまだ確認中のすべての明細行について、確認プロセスが最初からやり直しになります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-148">If you resubmit a purchase requisition line that has been rejected, the review process starts over for all lines in the purchase requisition that are still in review.</span></span> </br><span data-ttu-id="c19fc-149"><strong>注記:</strong> 送信済の購買要求を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-149"><strong>Note:</strong> You can recall a purchase requisition that has already been submitted.</span></span> <span data-ttu-id="c19fc-150">購買要求を取り消すと、他のすべての購買要求明細行も取り消されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-150">When you recall a purchase requisition, all other purchase requisition lines are also recalled.</span></span> <span data-ttu-id="c19fc-151">取り消した購買要求明細行は削除できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-151">Purchase requisition lines that have been recalled can be deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c19fc-152">拒否済</span><span class="sxs-lookup"><span data-stu-id="c19fc-152">Rejected</span></span></td>
<td><span data-ttu-id="c19fc-153">拒否済</span><span class="sxs-lookup"><span data-stu-id="c19fc-153">Rejected</span></span></td>
<td><span data-ttu-id="c19fc-154">購買要求、およびすべての購買要求明細行が拒否されています。</span><span class="sxs-lookup"><span data-stu-id="c19fc-154">The purchase requisition and all purchase requisition lines have been rejected.</span></span> <span data-ttu-id="c19fc-155">否認された購買要求と購買要求明細行は再送信できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-155">Purchase requisitions and purchase requisition lines that have been rejected can be resubmitted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c19fc-156">承認済</span><span class="sxs-lookup"><span data-stu-id="c19fc-156">Approved</span></span></td>
<td><ul>
<li><span data-ttu-id="c19fc-157">承認済</span><span class="sxs-lookup"><span data-stu-id="c19fc-157">Approved</span></span></li>
<li><span data-ttu-id="c19fc-158">取消済</span><span class="sxs-lookup"><span data-stu-id="c19fc-158">Cancelled</span></span></li>
<li><span data-ttu-id="c19fc-159">クローズ</span><span class="sxs-lookup"><span data-stu-id="c19fc-159">Closed</span></span></li>
</ul></td>
<td><span data-ttu-id="c19fc-160">すべての購買要求明細行で確認プロセスが完了しており、購買要求の確認ステップはこれ以上ありません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-160">All purchase requisition lines have completed the review process, and there are no more review steps for the purchase requisition.</span></span>
<ul>
<li><span data-ttu-id="c19fc-161"><strong>承認済</strong> – 購買要求明細行は確認プロセスを完了し、承認済です。</span><span class="sxs-lookup"><span data-stu-id="c19fc-161"><strong>Approved</strong> – The review process for a purchase requisition line has been completed, and the line is approved.</span></span></li>
<li><span data-ttu-id="c19fc-162"><strong>取消済</strong> – 購買要求明細行は承認されましたが、不要になったためキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-162"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it&#39;s no longer required.</span></span> <span data-ttu-id="c19fc-163">承認済の購買要求のみをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-163">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
<li><span data-ttu-id="c19fc-164"><strong>クローズ</strong> – 購買要求明細行が承認され、要求目的に応じてドキュメントが生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-164"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="c19fc-165">要求目的が消費の場合、発注書が購買要求明細行に対して生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-165">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="c19fc-166">要求目的が補充の場合、1 つ以上の処理のドキュメントが生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-166">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c19fc-167">取消済</span><span class="sxs-lookup"><span data-stu-id="c19fc-167">Cancelled</span></span></td>
<td><span data-ttu-id="c19fc-168">取消済</span><span class="sxs-lookup"><span data-stu-id="c19fc-168">Cancelled</span></span></td>
<td><span data-ttu-id="c19fc-169">購買要求、およびすべての購買要求明細行がキャンセルされています。</span><span class="sxs-lookup"><span data-stu-id="c19fc-169">The purchase requisition and all purchase requisition lines have been canceled.</span></span></br> <span data-ttu-id="c19fc-170"><strong>注意:</strong> 購買要求明細行の品目が不要になった場合、承認済であれば購買要求明細行をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-170"><strong>Note:</strong> If you no longer require an item that is on a purchase requisition line, you must cancel the purchase requisition line if it has already been approved.</span></span> <span data-ttu-id="c19fc-171">承認済の購買要求のみをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-171">Only purchase requisition lines that have been approved can be canceled.</span></span> <span data-ttu-id="c19fc-172">確認中の購買要求明細行がある場合は、購買要求のステータスは<strong>確認中</strong>になります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-172">If any purchase requisition lines are in review, the purchase requisition will have a status of <strong>In review</strong>.</span></span> <span data-ttu-id="c19fc-173">この場合、購買要求を取り消すと、適切な購買要求明細行を削除できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-173">In this case, you can recall the purchase requisition and delete the appropriate purchase requisition line.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c19fc-174">クローズ</span><span class="sxs-lookup"><span data-stu-id="c19fc-174">Closed</span></span></td>
<td><ul>
<li><span data-ttu-id="c19fc-175">クローズ</span><span class="sxs-lookup"><span data-stu-id="c19fc-175">Closed</span></span></li>
<li><span data-ttu-id="c19fc-176">取消済</span><span class="sxs-lookup"><span data-stu-id="c19fc-176">Cancelled</span></span></li>
</ul></td>
<td><span data-ttu-id="c19fc-177">購買要求が決済され、一つ以上の処理のドキュメントが生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-177">The purchase requisition is closed, and one or more fulfillment documents have been generated.</span></span>
<ul>
<li><span data-ttu-id="c19fc-178"><strong>クローズ</strong> – 購買要求明細行が承認され、要求目的に応じてドキュメントが生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-178"><strong>Closed</strong> – The purchase requisition line was approved, and documents have been generated, depending on the requisition purpose.</span></span>
<ul>
<li><span data-ttu-id="c19fc-179">要求目的が消費の場合、発注書が購買要求明細行に対して生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-179">If the requisition purpose is consumption, a purchase order has been generated for the purchase requisition line.</span></span></li>
<li><span data-ttu-id="c19fc-180">要求目的が補充の場合、1 つ以上の処理のドキュメントが生成されました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-180">If the requisition purpose is replenishment, one or more fulfillment documents have been generated.</span></span></li>
</ul></li>
<li><span data-ttu-id="c19fc-181"><strong>取消済</strong> – 購買要求明細行は承認されましたが、不要になったためキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="c19fc-181"><strong>Cancelled</strong> – The purchase requisition line was approved, but it has been canceled because it&#39;s no longer required.</span></span> <span data-ttu-id="c19fc-182">承認済の購買要求のみをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-182">Only purchase requisition lines that have been approved can be canceled.</span></span></li>
</ul><span data-ttu-id="c19fc-183">
<strong>注記:</strong> 終了済の購買要求明細行の品目が不要になった場合は、その購買要求明細行に対して生成された処理のドキュメントの明細行をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-183">
<strong>Note:</strong> If you no longer require an item on a purchase requisition line that has been closed, you must cancel the line on the fulfillment document that was generated for the purchase requisition line.</span></span></td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a><span data-ttu-id="c19fc-184">複数の財務勘定に原価配分</span><span class="sxs-lookup"><span data-stu-id="c19fc-184">Distributing costs to multiple financial accounts</span></span>
<span data-ttu-id="c19fc-185">購買要求に含まれている製品の原価を複数の財務勘定に配分できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-185">You can distribute the cost of a product that is included in a purchase requisition to multiple financial accounts.</span></span> <span data-ttu-id="c19fc-186">原価部門などの分析コードを組織で使用している場合は、製品の原価を財務勘定の分析コードに配分できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-186">If your organization uses dimensions, such as cost centers and departments, you can distribute the cost of a product to dimensions for financial accounts.</span></span>

## <a name="requisition-purposes"></a><span data-ttu-id="c19fc-187">要求目的</span><span class="sxs-lookup"><span data-stu-id="c19fc-187">Requisition purposes</span></span>
<span data-ttu-id="c19fc-188">要求目的によって、要求を実現するプロセスがより柔軟になります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-188">Requisition purposes make the process of fulfilling requisition demand more flexible.</span></span> <span data-ttu-id="c19fc-189">要求を作成する際に、消費または補充のいずれかの目的をその要求に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-189">When you create a requisition, you can assign one of two purposes to it: consumption or replenishment.</span></span> <span data-ttu-id="c19fc-190">要求の需要は、要求目的と組織の設定に基づいて発注書、移動オーダー、製造オーダー、またはかんばんによって満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-190">Depending on the requisition purpose and the setup of your organization, requisition demand can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="c19fc-191">調達ポリシーでは、要求が組織に対して作成されたときに使用できる要求目的を制御できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-191">In the procurement policies, you can control the requisition purposes that are available when a requisition is created for your organization.</span></span>

### <a name="requisitions-that-have-a-purpose-of-consumption"></a><span data-ttu-id="c19fc-192">消費目的の要求</span><span class="sxs-lookup"><span data-stu-id="c19fc-192">Requisitions that have a purpose of consumption</span></span>

<span data-ttu-id="c19fc-193">消費目的の要求は、組織で内部的に使用される品目またはサービスの需要を表します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-193">A requisition that has a purpose of consumption represents demand for items or services that will be used internally by your organization.</span></span> <span data-ttu-id="c19fc-194">この種類の要求によって作成される需要は、常に発注書によって満たされます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-194">The demand that is created by this kind of requisition is always fulfilled by a purchase order.</span></span> <span data-ttu-id="c19fc-195">Supply Chain Management が発注書を自動的に作成するように設定されている場合、購買要求が承認された後に発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-195">If Supply Chain Management is set up to automatically generate purchase orders, purchase orders are created after the purchase requisition is approved.</span></span>

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a><span data-ttu-id="c19fc-196">補充目的の要求</span><span class="sxs-lookup"><span data-stu-id="c19fc-196">Requisitions that have a purpose of replenishment</span></span>

<span data-ttu-id="c19fc-197">補充目的の要求は、在庫を補充するための需要を表します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-197">A requisition that has a purpose of replenishment represents demand to replenish inventory.</span></span> <span data-ttu-id="c19fc-198">たとえば、特定の小売の場所で特定の時間に品目を販売できるように、品目を補充するための要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-198">For example, you create a requisition to replenish items so that they can be sold at a specific retail location at a specific time.</span></span> <span data-ttu-id="c19fc-199">この種類の要求によって作成される需要は、発注書、移動オーダー、製造オーダー、またはかんばんによって満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-199">The demand that is created by this kind of requisition can be fulfilled by a purchase order, transfer order, production order, or kanban.</span></span>  

<span data-ttu-id="c19fc-200">要求目的が補充である場合、需要は金額ではなく数量で表されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-200">When the requisition purpose is replenishment, demand is expressed as a quantity instead of a monetary amount.</span></span> <span data-ttu-id="c19fc-201">したがって、債務会計、予算管理、固定資産確認のためのビジネス ルール (BRAD)、プロジェクト会計、および関連するルールは適用されません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-201">Therefore, encumbrance accounting, budgetary control, business rules for fixed asset determination (BRAD), project accounting, and any related rules don't apply.</span></span> <span data-ttu-id="c19fc-202">指定した法人に対して保管およびリリースされている製品のみが補充要求の需要を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-202">Only products that are stocked and released to the specified legal entity can fulfill replenishment requisition demand.</span></span> <span data-ttu-id="c19fc-203">要求目的が補充であるときに使用できる製品を定義するには、**補充のカテゴリ アクセス ポリシー ルール** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-203">To define the products that are available when the requisition purpose is replenishment, use the **Replenishment category access policy rule** page.</span></span>  

<span data-ttu-id="c19fc-204">補充目的の購買要求を使用するには、要求の需要を含めるようにマスター スケジューリングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-204">To use purchase requisitions that have a purpose of replenishment, you must set up master scheduling to include requisition demand.</span></span> <span data-ttu-id="c19fc-205">この種類の要求によって作成された需要を満たす方法が、組織の品目に設定され、マスター スケジューリングを使用して計画されている供給ポリシーに基づいて自動的に決定されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-205">The fulfillment method for the demand that is created by this kind of requisition is then determined automatically, based on the supply policies that have been set up for the items in your organization and planned by using master scheduling.</span></span>

## <a name="purchase-requisitions-and-requests-for-quotation"></a><span data-ttu-id="c19fc-206">購買要求と見積の要求</span><span class="sxs-lookup"><span data-stu-id="c19fc-206">Purchase requisitions and requests for quotation</span></span>
<span data-ttu-id="c19fc-207">場合によっては、見積依頼 (RFQ) のプロセスを開始して、購買要求で要求される製品の仕入先および価格を識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-207">In some cases, you must start a request for quotation (RFQ) process to identify the vendor and price for products that are requested in a purchase requisition.</span></span> <span data-ttu-id="c19fc-208">購買要求が確認中である場合、RFQ を生成できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-208">An RFQ can be generated when the purchase requisition is in review.</span></span> <span data-ttu-id="c19fc-209">入札を承認すると、仕入先、価格などに関する情報が要求に転送されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-209">When you accept a bid, information about the vendor, price, and so on, is transferred to the requisition.</span></span>  

<span data-ttu-id="c19fc-210">**購買要求の詳細** ページの **保留** チェック ボックスを選択すると、購買要求を保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-210">You can put a purchase requisition on hold by selecting the **On hold** check box on the **Purchase requisition details** page.</span></span> <span data-ttu-id="c19fc-211">購買要求の処理は、チェック ボックスをオフにして、保留を解除した後にのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-211">Processing of the purchase requisition can continue only after you remove the hold by clearing the check box.</span></span>  

> [!NOTE]
> <span data-ttu-id="c19fc-212">e-procurement では、仕入先は購買要求の RFQ によって代替明細行を追加できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-212">In e-procurement, the RFQ for your purchase requisition might allow vendors to add alternate lines.</span></span> <span data-ttu-id="c19fc-213">この場合、購買要求は、承認された代替明細行に反映します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-213">In this case, your purchase requisition will reflect approved alternates.</span></span>

## <a name="demand-consolidation"></a><span data-ttu-id="c19fc-214">需要連結</span><span class="sxs-lookup"><span data-stu-id="c19fc-214">Demand consolidation</span></span>
<span data-ttu-id="c19fc-215">複数の購買要求からの購買要求明細行を連結すると、仕入先との交渉力が高まり、有利な商品価格決定、配送費用および手数料の低減、間接費の削減を実現できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-215">By consolidating purchase requisition lines from multiple purchase requisitions, you can increase your negotiating power with your vendors to achieve better pricing, lower shipping and handling costs, and reduced overhead costs.</span></span>  

<span data-ttu-id="c19fc-216">購買要求明細行は、次の条件が true の場合にのみ需要連結に適用できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-216">Purchase requisition lines are eligible for demand consolidation only if the following statements are true:</span></span>

-   <span data-ttu-id="c19fc-217">購買要求が承認されている。</span><span class="sxs-lookup"><span data-stu-id="c19fc-217">The purchase requisition has been approved.</span></span>
-   <span data-ttu-id="c19fc-218">購買要求が手動処理および連結需要の購買ポリシー ルールの条件を満たしている。</span><span class="sxs-lookup"><span data-stu-id="c19fc-218">The purchase requisition meets the purchasing policy rule criteria for manual processing and demand consolidation.</span></span>

<span data-ttu-id="c19fc-219">手動処理の条件を満たす承認済購買要求明細行の一覧は、**承認済購買要求のリリース** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-219">Approved purchase requisition lines that meet the criteria for manual processing are listed on the **Release approved purchase requisitions** page.</span></span> <span data-ttu-id="c19fc-220">購買要求明細行が需要連結の条件も満たしている場合は、その明細行を連結機会に追加できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-220">If a purchase requisition line also meets the criteria for demand consolidation, the line can be added to a consolidation opportunity.</span></span>  

<span data-ttu-id="c19fc-221">連結機会とは、購買担当者が仕入先と最良の取引を交渉できるようにグループ化される一連の購買要求明細行です。</span><span class="sxs-lookup"><span data-stu-id="c19fc-221">A consolidation opportunity is a set of purchase requisition lines that are grouped together, so that the purchasing professional can negotiate the best deal with vendors.</span></span> <span data-ttu-id="c19fc-222">連結機会に対して選択した購買要求明細行は**購買要求連結**ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-222">Purchase requisition lines that you select for a consolidation opportunity appear on the **Purchase requisition consolidation** page.</span></span> <span data-ttu-id="c19fc-223">変更が必要な場合、このページで明細行を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-223">You can modify the lines on this page, if changes are required.</span></span> <span data-ttu-id="c19fc-224">また、新しい明細行を連結機会に追加したり、既存の明細行を削除したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-224">You can also add new lines to the consolidation opportunity or remove existing lines.</span></span>  

<span data-ttu-id="c19fc-225">要求明細行を連結機会に追加して必要な変更を行うと、連結購買要求明細行の発注書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-225">After you add requisition lines to a consolidation opportunity and make any changes that you require, you can create a purchase order for the consolidated purchase requisition lines.</span></span>  

> [!NOTE]
> <span data-ttu-id="c19fc-226">**購買要求連結**ページで購買要求明細行に対して行った変更は、作成した発注書に反映されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-226">Changes that you make to a purchase requisition line on the **Purchase requisition consolidation** page are reflected on the purchase order that you create.</span></span> <span data-ttu-id="c19fc-227">ただし、購買要求では履歴を保持するように明細行は変更されません。</span><span class="sxs-lookup"><span data-stu-id="c19fc-227">However, the line remains unchanged in the purchase requisition, so that its history is preserved.</span></span>  

<span data-ttu-id="c19fc-228">需要連結を適用できない購買要求明細行の発注書、または連結機会に対して選択されていない購買要求明細行の発注書を作成するには、手動で処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c19fc-228">To create a purchase order for purchase requisition lines that aren't eligible for demand consolidation or aren't selected for a consolidation opportunity, you must process the lines manually.</span></span>

### <a name="consolidating-purchase-requisition-lines"></a><span data-ttu-id="c19fc-229">購買要求明細行の連結</span><span class="sxs-lookup"><span data-stu-id="c19fc-229">Consolidating purchase requisition lines</span></span>

<span data-ttu-id="c19fc-230">予算管理が組織用に構成されている場合、かつ予算引当や事前債務が記録され、購買要求がワークフローで承認されている場合、需要連結のプロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c19fc-230">The process for demand consolidation starts when a purchase requisition is approved in a workflow and, if budget control is configured for your organization, when the budget reservations and pre-encumbrances have been recorded.</span></span> <span data-ttu-id="c19fc-231">次の図は、需要連結のプロセス フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="c19fc-231">The following diagram shows the process flow for demand consolidation.</span></span>  

<span data-ttu-id="c19fc-232">[![需要連結のプロセス フロー](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span><span class="sxs-lookup"><span data-stu-id="c19fc-232">[![Process flow for demand consolidation](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)</span></span>  

<span data-ttu-id="c19fc-233">承認済購買要求明細行を連結するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c19fc-233">To consolidate approved purchase requisition lines, follow these steps:</span></span>

1.  <span data-ttu-id="c19fc-234">手動処理のために保持され、需要連結に適用できる承認済要求明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-234">Review approved requisition lines that have been held for manual processing, and that are eligible for demand consolidation.</span></span>
2.  <span data-ttu-id="c19fc-235">明細行を選択して連結機会に追加します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-235">Select lines to add to a consolidation opportunity.</span></span>
3.  <span data-ttu-id="c19fc-236">新しい連結機会を作成するか、既存の連結機会に要求明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-236">Create a new consolidation opportunity, or add requisition lines to an existing consolidation opportunity.</span></span>
4.  <span data-ttu-id="c19fc-237">要求明細行に必要な変更を行い、連結機会に含めない要求明細行品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-237">Make any required changes to the requisition lines, and remove requisition line items that you no longer want to include in the consolidation opportunity.</span></span>
5.  <span data-ttu-id="c19fc-238">連結機会の連結要求明細行または購買要求明細行の発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c19fc-238">Create purchase orders for consolidated requisition lines or for purchase requisition lines in a consolidation opportunity.</span></span>


<a name="additional-resources"></a><span data-ttu-id="c19fc-239">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c19fc-239">Additional resources</span></span>
--------

[<span data-ttu-id="c19fc-240">消費要求の作成</span><span class="sxs-lookup"><span data-stu-id="c19fc-240">Create a requisition for consumption</span></span>](tasks/create-requisition-consumption.md)

[<span data-ttu-id="c19fc-241">購買要求ワークフロー</span><span class="sxs-lookup"><span data-stu-id="c19fc-241">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)



