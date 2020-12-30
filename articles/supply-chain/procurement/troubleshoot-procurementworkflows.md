---
title: 調達ワークフローに関するトラブルシューティング
description: このトピックでは、調達ワークフロー中に発生する可能性がある問題を修正する方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432389"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="921eb-103">調達ワークフローに関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="921eb-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="921eb-104">このトピックでは、調達ワークフロー中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="921eb-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="921eb-105">変更後に発注書をワークフローに再送信するときのエラー: "発注書 X に対する変更は、変更管理が有効になったときにのみ下書きの状態で許可されます"</span><span class="sxs-lookup"><span data-stu-id="921eb-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="921eb-106">この問題は、変更を要求する前に発注書が *確認済* 状態になっていた場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="921eb-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="921eb-107">発注書が *承認済* 状態になっている場合に変更を要求すると、ワークフローを正常に処理できます。</span><span class="sxs-lookup"><span data-stu-id="921eb-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="921eb-108">エラーの説明</span><span class="sxs-lookup"><span data-stu-id="921eb-108">Error description</span></span>

<span data-ttu-id="921eb-109">変更後に発注書を再送信すると、ワークフローで次のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="921eb-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="921eb-110">停止 (エラー): X + + 例外: 発注書 PO0000569 に対する変更は、変更管理が次で有効になっている場合にのみ [ドラフト] 状態でのみ許可されます。</span><span class="sxs-lookup"><span data-stu-id="921eb-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="921eb-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="921eb-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="921eb-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="921eb-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="921eb-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="921eb-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="921eb-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="921eb-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="921eb-115">問題の解決</span><span class="sxs-lookup"><span data-stu-id="921eb-115">Issue resolution</span></span>

<span data-ttu-id="921eb-116">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="921eb-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="921eb-117">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="921eb-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="921eb-118">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="921eb-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="921eb-119">この問題は、[この Microsoft サポート技術情報 (KB) の記事 ](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) を通じて修正されます。</span><span class="sxs-lookup"><span data-stu-id="921eb-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="921eb-120">1 つ以上の勘定配布が、過剰配布されているか、配布中であるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="921eb-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="921eb-121">この問題は、発注書の配分に不整合があるために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="921eb-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="921eb-122">この問題のブロックを解除して発注書を *ドラフト* 状態にリセットするには、**調達 \> 定期タスク \> クリーンアップ \> 発注書配送のリセット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="921eb-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="921eb-123">詳細については、ブログ投稿 [Dynamics 365 Supply Chain Management での PO 配分エラーを解決する](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="921eb-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="921eb-124">変更管理が有効になっている発注書で出荷更新待ちがキャンセルされた場合、発注書は確認済状態になります。</span><span class="sxs-lookup"><span data-stu-id="921eb-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="921eb-125">問題の説明</span><span class="sxs-lookup"><span data-stu-id="921eb-125">Issue description</span></span>

<span data-ttu-id="921eb-126">変更管理の対象となる発注書の場合、要求される唯一の変更が 1 つ以上の明細行の出荷残余の取消である場合、発注書は承認された時点で直接 *確認済* 状態になり、仕訳帳は作成されません。</span><span class="sxs-lookup"><span data-stu-id="921eb-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="921eb-127">問題の解決</span><span class="sxs-lookup"><span data-stu-id="921eb-127">Issue resolution</span></span>

<span data-ttu-id="921eb-128">配送残余をキャンセルしても、確認仕訳帳の内容には影響しません。</span><span class="sxs-lookup"><span data-stu-id="921eb-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="921eb-129">この機能は、明細行が部分的に入庫され、発注書が仕入先に対して確認された後に、プロセス ステップで残余品質をキャンセルする必要がある場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="921eb-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="921eb-130">この数量を発注書の確認書に反映する必要がある場合は、購買注文明細行で数量を調整して、確認が必要になるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="921eb-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="921eb-131">また、その明細行に何も入庫されていない場合は、数量を削除できます。</span><span class="sxs-lookup"><span data-stu-id="921eb-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="921eb-132">この場合、再確認が要求されます。</span><span class="sxs-lookup"><span data-stu-id="921eb-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="921eb-133">キャンセルされた発注書は、発注書準備ワークスペースの下書き一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="921eb-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="921eb-134">問題の説明</span><span class="sxs-lookup"><span data-stu-id="921eb-134">Issue description</span></span>

<span data-ttu-id="921eb-135">*確認済* 状態の発注書をキャンセルした後で、そのキャンセルされた発注書は、**発注書** 準備ワークスペースのドラフト発注書の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="921eb-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="921eb-136">問題の解決</span><span class="sxs-lookup"><span data-stu-id="921eb-136">Issue resolution</span></span>

<span data-ttu-id="921eb-137">この問題は、変更管理の対象になる発注書に対してのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="921eb-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="921eb-138">これは、このキャンセルに必要のある変更が懸念されることから発生します。</span><span class="sxs-lookup"><span data-stu-id="921eb-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="921eb-139">この承認は、システムによって自動的に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="921eb-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="921eb-140">したがって、このプロセスでは、キャンセルされた発注書を承認ワークフローに送信して、*承認済* 状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="921eb-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="921eb-141">この時点で、**発注書の準備** ワークスペースのドラフト発注書の一覧にその発注書が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="921eb-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

