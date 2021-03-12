---
title: リース承認ワークフローの使用
description: このトピックでは、ワークフローを使用して資産リースを承認する方法、およびワークフローのステータスと履歴を追跡する方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1086231c65a726df5162d3593419a129d6ae5655
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992761"
---
# <a name="use-lease-approval-workflows"></a><span data-ttu-id="2a608-103">リース承認ワークフローの使用</span><span class="sxs-lookup"><span data-stu-id="2a608-103">Use lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a608-104">このトピックでは、ワークフローを使用して資産リースを承認する方法、およびワークフローのステータスと履歴を追跡する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2a608-104">This topic explains how to use workflows to approve asset leases, and how to track the status and history of the workflows.</span></span> <span data-ttu-id="2a608-105">ワークフローは、標準の承認ステップのセットを提供し、プロセスの各手順を承認する特定のユーザーを割り当てることによって、リース承認の管理に一貫性を持たせるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2a608-105">Workflows help bring consistency to the management of lease approvals by providing a standard set of approval steps and assigning specific users who approve each step of the process.</span></span> <span data-ttu-id="2a608-106">承認者は、リースを承認、否認し、変更を依頼するか、または承認を別のユーザーに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2a608-106">An approver can approve a lease, reject it, request a change to it, or assign it to another user for approval.</span></span> <span data-ttu-id="2a608-107">ワークフローでは、ワークフローのステータスと履歴を追跡することにより、承認プロセスをより詳細に表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a608-107">Workflows can also bring more visibility into the approval process by letting you track their status and history.</span></span> <span data-ttu-id="2a608-108">さらに、特定の承認者に割り当てられているタスクと承認を一覧表示する集中的なワークリストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="2a608-108">Additionally, you can view a centralized worklist that lists the tasks and approvals that are assigned to specific approvers.</span></span>

<span data-ttu-id="2a608-109">この手順を使用する前に、少なくともリース承認ワークフローが作成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2a608-109">Before you use this procedure, make sure that at least on lease approval workflow has been created.</span></span> <span data-ttu-id="2a608-110">ワークフローが存在しない場合は作成します。</span><span class="sxs-lookup"><span data-stu-id="2a608-110">If no workflow exists, create one.</span></span> <span data-ttu-id="2a608-111">ワークフローの設定方法の詳細については、[リース承認ワークフローの設定](set-up-lease-wrkflw.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a608-111">For information about how to set up a workflow, see [Set up lease approval workflows](set-up-lease-wrkflw.md).</span></span>

1. <span data-ttu-id="2a608-112">承認のためにリースを送信します。</span><span class="sxs-lookup"><span data-stu-id="2a608-112">Submit a lease for approval.</span></span> <span data-ttu-id="2a608-113">リースの **帳簿の詳細** ページで、**ワークフロー** を選択し、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-113">On the **Book details** page for the lease, select **Workflow**, and then select **Submit**.</span></span>
2. <span data-ttu-id="2a608-114">表示されるダイアログ ボックスで、コメントを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2a608-114">In the dialog box that appears, you can add a comment.</span></span> <span data-ttu-id="2a608-115">指定された承認者は、このコメントをリースと共に表示します。</span><span class="sxs-lookup"><span data-stu-id="2a608-115">The designated approver will see this comment together with the lease.</span></span> <span data-ttu-id="2a608-116">コメントの入力が完了したら、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-116">When you've finished entering the comment, select **Submit**.</span></span> <span data-ttu-id="2a608-117">リースがワークフロー システムに送信され、承認を受けるために承認者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2a608-117">The lease is submitted to the workflow system, and the approver receives it for approval.</span></span>
3. <span data-ttu-id="2a608-118">承認対象として指定されているリースを表示するには、**モジュール \> 共通 \> 作業項目 \> 自分自身に割り当てられた作業項目** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a608-118">To view the leases that they are designated for approval, go to **Modules \> Common \> Work items \> Work items assigned to me**.</span></span>
4. <span data-ttu-id="2a608-119">**自分自身に割り当てられた作業項目** ページで、表示するリースの **リース ID** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-119">On the **Work items assigned to me** page, select the **Lease ID** link for the lease that you want to view.</span></span> <span data-ttu-id="2a608-120">表示されるページは、アクセスできるリース帳簿とリースの詳細によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2a608-120">The page that appears depends on the lease books and lease details that you have access to.</span></span>
5. <span data-ttu-id="2a608-121">リースを表示したら、**ワークフロー** を選択し、どのアクションを実行するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2a608-121">When you've finish viewing the lease, select **Workflow**, and decide what action should be taken.</span></span> <span data-ttu-id="2a608-122">オプションには、**承認**、**拒否**、**要求の変更**、**委任**、および **キャンセル済み** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a608-122">The options include **Approve**, **Rejected**, **Request change**, **Delegate**, and **Canceled**.</span></span> <span data-ttu-id="2a608-123">選択したリースの承認履歴を表示するには、**履歴の表示** を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a608-123">You can also select **View history** to view the approval history for the selected lease.</span></span>
6. <span data-ttu-id="2a608-124">アクションを選択したら、アクションを説明するコメントを入力します。</span><span class="sxs-lookup"><span data-stu-id="2a608-124">After you've selected an action, enter a comment to describe the action.</span></span> <span data-ttu-id="2a608-125">コメントの入力が完了したら、一覧から **承認済** アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-125">When you've finished entering the comment, select the **Approved** action in the list.</span></span>
7. <span data-ttu-id="2a608-126">承認アクションを表示するには、**リースの概要** ページの **リースの詳細** ページに戻り、**ワークフロー \> ビュー履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-126">To view the approval actions, go back to the **Lease details** page from the **Lease summary** page, and then select **Workflow \> View history**.</span></span>

    <span data-ttu-id="2a608-127">ワークフロー活動は、**ワークフロー履歴** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="2a608-127">You can view the workflow activities on the **Workflow history** page.</span></span> <span data-ttu-id="2a608-128">このページには、特定のリースに対して実行されたワークフロー ステップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a608-128">This page shows the workflow steps that have been taken on the specific lease.</span></span> <span data-ttu-id="2a608-129">**作業項目** フィールドを使用して、割り当てられた作業項目のステータスを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a608-129">You can also use the **Work items** field to view the status of the assigned work items.</span></span>

8. <span data-ttu-id="2a608-130">ワークフローを停止するには、**ワークフロー履歴** ページで **リコール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-130">To stop a workflow, on the **Workflow history** page, select **Recall**.</span></span> <span data-ttu-id="2a608-131">表示されるダイアログ ボックスで、コメントを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-131">In the dialog box that appears, enter a comment, and then select **OK**.</span></span>
9. <span data-ttu-id="2a608-132">ワークフローを無効にする場合、または作成済みのワークフローを有効にする場合は、**資産リース \> 設定 \> リース ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a608-132">To inactivate a workflow, or to activate a workflow that was previously created, go to **Asset leasing \> Setup \> Lease workflow**.</span></span> <span data-ttu-id="2a608-133">次に、**リース ワークフロー** ページで、**ワークフロー \> バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-133">Then, on the **Lease workflow** page, select **Workflow \> Versions**.</span></span> <span data-ttu-id="2a608-134">現在のワークフローを非アクティブにするには、リース バージョン ダイアログ ボックスで有効なリースを選択し、**無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-134">To make a current workflow inactive, select the active lease in the lease version dialog box, and then select **Make inactive**.</span></span> <span data-ttu-id="2a608-135">既存のワークフローを有効にするには、ワークフローを選択し、**有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a608-135">To make an existing workflow active, select the workflow, and then select **Make active**.</span></span>
