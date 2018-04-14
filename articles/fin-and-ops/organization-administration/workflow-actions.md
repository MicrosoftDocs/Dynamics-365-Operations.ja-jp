---
title: "ワークフロー アクション"
description: "この記事は、ワークフローの承認プロセスで各参加者が実行できるアクションを説明します。"
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 910e954f98165eb6605f1c4055bfb0a40c81f00b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="workflow-actions"></a><span data-ttu-id="fe217-103">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="fe217-103">Workflow actions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fe217-104">この記事は、ワークフローの承認プロセスで各参加者が実行できるアクションを説明します。</span><span class="sxs-lookup"><span data-stu-id="fe217-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="fe217-105">ワークフローには、作成者、タスクの割り当て対象者、意志決定者、承認者といった複数のグループのユーザーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fe217-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="fe217-106">たとえば、次の経費精算書ワークフローでは、康介が作成者で、キューのメンバーがタスクの割り当て対象者で、ジョンが意思決定者で、卓也、政美、および綾が承認者です。</span><span class="sxs-lookup"><span data-stu-id="fe217-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="fe217-107">[![ワークフロー\_手動決定を含む](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="fe217-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="fe217-108">以下のセクションでは、各ユーザー グループが実行できるワークフロー アクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fe217-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="fe217-109">作成者が実行できるアクション</span><span class="sxs-lookup"><span data-stu-id="fe217-109">Actions that an originator can perform</span></span>
<span data-ttu-id="fe217-110">作成者は、処理対象のドキュメントを送信することによって、ワークフロー インスタンスを開始します。</span><span class="sxs-lookup"><span data-stu-id="fe217-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="fe217-111">たとえば、康介が経費精算書を送信するには、康介が**経費精算書**ページで [**送信**] ボタンをクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="fe217-112">タスク割り当て対象者が実行できるアクション</span><span class="sxs-lookup"><span data-stu-id="fe217-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="fe217-113">タスクは、複数のユーザーに割り当てることも、複数のユーザーが監視する作業項目キューに割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="fe217-114">ただし、タスクを完了できるユーザーは 1 人だけです。</span><span class="sxs-lookup"><span data-stu-id="fe217-114">However, only one person can complete a task.</span></span> <span data-ttu-id="fe217-115">たとえば、康介が経費精算書を送信し、確認用の領収書を組織の経費精算書部門に提出したとします。</span><span class="sxs-lookup"><span data-stu-id="fe217-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="fe217-116">Adventure Works の経費精算書部門のメンバーは、キューを監視します。</span><span class="sxs-lookup"><span data-stu-id="fe217-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="fe217-117">その部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="fe217-118">これで彼女は、完了、却下、変更依頼、再割り当て、リリースのいずれかのアクションを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fe217-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="fe217-119">**注記:** 実行可能なアクションは、ソフトウェア開発者がタスクをどのように設計したかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe217-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="fe217-120">完了</span><span class="sxs-lookup"><span data-stu-id="fe217-120">Complete</span></span>

<span data-ttu-id="fe217-121">ユーザーがタスクを完了すると、処理対象として送信されたドキュメントは、ワークフロー内の次のユーザーに割り当てられます (次のユーザーが存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="fe217-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="fe217-122">追加の処理が必要ない場合、ワークフロー プロセスは終了となります。</span><span class="sxs-lookup"><span data-stu-id="fe217-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-123">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="fe217-124">ジュリーが自分の確認を実行すると、ドキュメントはジョンに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="fe217-125">拒否</span><span class="sxs-lookup"><span data-stu-id="fe217-125">Reject</span></span>

<span data-ttu-id="fe217-126">ユーザーがドキュメントを否認すると、ワークフロー プロセスは終了します。</span><span class="sxs-lookup"><span data-stu-id="fe217-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-127">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="fe217-128">ジュリーが経費報告書を拒否する場合、ワークフロー プロセスは終了します。</span><span class="sxs-lookup"><span data-stu-id="fe217-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-129">その後、康介は経費報告書を再送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fe217-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="fe217-130">最初に変更を加えることもできますが、またはオリジナル バージョンを再送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="fe217-131">康介が経費精算書を再送信した場合、ワークフロー プロセスは手動確認タスクから開始されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="fe217-132">デリゲート</span><span class="sxs-lookup"><span data-stu-id="fe217-132">Delegate</span></span>

<span data-ttu-id="fe217-133">ユーザーがタスクを委任すると、タスクは別のユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="fe217-134">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="fe217-135">ジュリーは、彼女のアシスタントであるティムにタスクを委任します。</span><span class="sxs-lookup"><span data-stu-id="fe217-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="fe217-136">そこで、ティムは、ジュリー代わりにタスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="fe217-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="fe217-137">つまり、ティムが確認を完了すると、ジュリーがタスクを完了した場合と同じように、ジョンに経費精算書が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="fe217-138">変更依頼</span><span class="sxs-lookup"><span data-stu-id="fe217-138">Request change</span></span>

<span data-ttu-id="fe217-139">ユーザーが送信されたドキュメントに対する変更を依頼すると、ドキュメントは作成者に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="fe217-140">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="fe217-141">ジュリーは、経費精算書に間違いがあることに気づき、精算書のレポートの変更を依頼します。</span><span class="sxs-lookup"><span data-stu-id="fe217-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="fe217-142">経費精算書は康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="fe217-143">その後、康介は経費報告書を再送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fe217-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="fe217-144">最初に変更を依頼することもできますが、またはオリジナル バージョンを再送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="fe217-145">康介が経費精算書を再送信した場合は、作業項目キューのメンバーが、経費精算書と領収書を再度確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="fe217-146">再割り当て</span><span class="sxs-lookup"><span data-stu-id="fe217-146">Reassign</span></span>

<span data-ttu-id="fe217-147">作業項目キューのメンバーは、そのキュー内のドキュメントを別のキューに再割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="fe217-148">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、キューを監視しています。</span><span class="sxs-lookup"><span data-stu-id="fe217-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="fe217-149">彼女は、作業負荷のバランスを取るために、経費精算書とそれに付属する領収書を別のキューに再割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="fe217-150">リリース</span><span class="sxs-lookup"><span data-stu-id="fe217-150">Release</span></span>

<span data-ttu-id="fe217-151">場合によっては、作業項目キューのメンバーがタスクを受け入れる可能性もありますが、その従業員がタスクを完了できないと判断します。</span><span class="sxs-lookup"><span data-stu-id="fe217-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="fe217-152">この場合、タスクを受け入れたユーザーが作業項目キューに戻すドキュメントをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="fe217-153">たとえば、Adventure Works の経費精算書部門のメンバーであるジュリーが、康介の経費精算書と領収書を確認するタスクを受け入れました。</span><span class="sxs-lookup"><span data-stu-id="fe217-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="fe217-154">ジュリーが、タスクを完了できないと判断した場合、彼女はドキュメントをリリースできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="fe217-155">経費精算書はキューに戻され、Adventure Works の経費精算書部門の他のメンバーがタスクを完了できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fe217-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="fe217-156">意志決定者が実行できるアクション</span><span class="sxs-lookup"><span data-stu-id="fe217-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="fe217-157">意思決定者が答える必要がある質問があるため、ドキュメントは通常、意思決定者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="fe217-158">質問に対する回答は、通常 [**はい**] または [**いいえ**] または [**True**] または [**False**] です。</span><span class="sxs-lookup"><span data-stu-id="fe217-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="fe217-159">意思決定者がそれらの選択肢をいずれも選択しない場合、意思決定者は決定を委任できます。</span><span class="sxs-lookup"><span data-stu-id="fe217-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="fe217-160">\[選択 1 \] または \[選択 2 \]</span><span class="sxs-lookup"><span data-stu-id="fe217-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="fe217-161">意思決定者は、ドキュメントに関連する質問に回答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="fe217-162">質問に対する回答は、通常 [**はい**] または [**いいえ**] または [**True**] または [**False**] です。</span><span class="sxs-lookup"><span data-stu-id="fe217-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="fe217-163">意思決定者が選択する回答によって、ドキュメントを処理するのに使用するワークフロー分岐が決まります。</span><span class="sxs-lookup"><span data-stu-id="fe217-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="fe217-164">たとえば、康介の経費精算書がジョンに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="fe217-165">一郎は、ドキュメントの情報を見て、康介のマネージャーに電話をかける必要があるかどうかを決定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fe217-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="fe217-166">電話の必要があると John が決定すると、経費精算書は Aretha に割り当てられ、その後、Aretha が康介のマネージャーに電話をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="fe217-167">電話は不要であると John が判断すると、経費精算書は承認のために卓也に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="fe217-168">委任</span><span class="sxs-lookup"><span data-stu-id="fe217-168">Delegate</span></span>

<span data-ttu-id="fe217-169">意志決定者が決定を委任すると、ドキュメントは別のユーザーに割り当てられ、そのユーザーが決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="fe217-170">たとえば、康介の経費精算書がジョンに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="fe217-171">ジョンは、アシスタントのマリアに決定を委任します。</span><span class="sxs-lookup"><span data-stu-id="fe217-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="fe217-172">すると、マリアはジョンの代わりに処理を行います。</span><span class="sxs-lookup"><span data-stu-id="fe217-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="fe217-173">康介のマネージャーに電話をする必要があると Maria が決定すると、経費精算書は Aretha に割り当てられ、その後、Aretha が康介のマネージャーに電話をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe217-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="fe217-174">通話が不要であるとマリアが判断した場合、経費精算書は承認のために卓也に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="fe217-175">承認者が実行できるアクション</span><span class="sxs-lookup"><span data-stu-id="fe217-175">Actions that an approver can perform</span></span>
<span data-ttu-id="fe217-176">ドキュメントが承認者に割り当てられると、承認者は承認、拒否、委任のいずれかのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="fe217-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="fe217-177">承認</span><span class="sxs-lookup"><span data-stu-id="fe217-177">Approve</span></span>

<span data-ttu-id="fe217-178">承認者がドキュメントを承認すると、ドキュメントは必要に応じてワークフロー内の次のユーザーに割り当てられます (次のユーザーが存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="fe217-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="fe217-179">追加の処理が必要ない場合、ワークフロー プロセスは終了となります。</span><span class="sxs-lookup"><span data-stu-id="fe217-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-180">たとえば、康介が USD 6,000 の経費精算書を提出し、このドキュメントが卓也に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="fe217-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="fe217-181">卓也がドキュメントを承認すると、次は承認のために政美に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="fe217-182">政美によって経費報告書が承認される場合、ワークフロー プロセスは終了します。</span><span class="sxs-lookup"><span data-stu-id="fe217-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="fe217-183">拒否</span><span class="sxs-lookup"><span data-stu-id="fe217-183">Reject</span></span>

<span data-ttu-id="fe217-184">承認者がドキュメントを否認すると、ワークフロー プロセスは終了します。</span><span class="sxs-lookup"><span data-stu-id="fe217-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-185">たとえば、康介が USD 12,000 の経費精算書を提出し、このドキュメントが政美に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="fe217-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="fe217-186">政美が経費精算書を拒否すると、ワークフロー プロセスは終了します。</span><span class="sxs-lookup"><span data-stu-id="fe217-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="fe217-187">その後、康介は経費報告書を再送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fe217-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="fe217-188">最初に変更を加えることもできますが、または経費精算書のオリジナル バージョンを再送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="fe217-189">康介が経費精算書を再送信した場合、ワークフロー プロセスは承認プロセスから開始されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="fe217-190">委任</span><span class="sxs-lookup"><span data-stu-id="fe217-190">Delegate</span></span>

<span data-ttu-id="fe217-191">承認者がドキュメントを委任すると、ドキュメントは承認を受けるために別のユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="fe217-192">たとえば、康介が USD 12,000 の経費精算書を提出し、このドキュメントが卓也に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="fe217-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="fe217-193">卓也は経費精算書を綾に委任します。</span><span class="sxs-lookup"><span data-stu-id="fe217-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="fe217-194">綾は、卓也の代わりにタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fe217-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="fe217-195">したがって、綾がドキュメントを承認すると、卓也が承認した場合と同じように、ドキュメントは承認のために政美に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fe217-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="fe217-196">ドキュメントは、政美が承認した後で、承認を受けるために綾に送信されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="fe217-197">変更依頼</span><span class="sxs-lookup"><span data-stu-id="fe217-197">Request change</span></span>

<span data-ttu-id="fe217-198">承認者がドキュメントに対する変更を依頼すると、ドキュメントは作成者に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="fe217-199">たとえば、康介が USD 12,000 の経費精算書を提出し、このドキュメントが政美に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="fe217-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="fe217-200">政美が変更を要求すると、経費精算書は康介に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="fe217-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="fe217-201">その後、康介は経費報告書を再送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fe217-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="fe217-202">最初に変更を依頼することもできますが、または経費精算書のオリジナル バージョンを再送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="fe217-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="fe217-203">康介が経費報告書を再送信すると、今度は承認プロセスの最初の承認者である卓也に承認のために送られます。</span><span class="sxs-lookup"><span data-stu-id="fe217-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




