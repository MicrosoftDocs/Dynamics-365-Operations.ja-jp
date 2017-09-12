---
title: "調達ワークフロー"
description: "組織によっては、取引を入力した個人以外のユーザーが購買要求と発注書を承認することを要求している場合があります。 承認プロセスを設定するには、ワークフローを作成できます。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="b7f08-104">調達ワークフロー</span><span class="sxs-lookup"><span data-stu-id="b7f08-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b7f08-105">組織によっては、取引を入力した個人以外のユーザーが購買要求と発注書を承認することを要求している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7f08-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="b7f08-106">承認プロセスを設定するには、ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="b7f08-107">1 つのワークフローは 1 つの業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-107">A workflow represents a business process.</span></span> <span data-ttu-id="b7f08-108">ここでは、ドキュメントの処理および承認に携わるべきユーザーを示すことによって、システムにおけるドキュメントの流れを定義します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b7f08-109">組織でワークフロー システムを使用することにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="b7f08-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="b7f08-110">**一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントの承認プロセスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b7f08-111">ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="b7f08-112">**プロセスの可視性** - 特定のワークフロー インスタンスのステータス、履歴およびパフォーマンス測定方法を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b7f08-113">これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="b7f08-114">[**集中化された作業一覧**] ユーザーはワークフローに参加するすべてのユーザーに割り当てられているワークフロー タスクおよび承認を表示するには、集中化された作業一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="b7f08-115">これは、[作業項目] ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="b7f08-116">作成できるワークフローのタイプ</span><span class="sxs-lookup"><span data-stu-id="b7f08-116">The types of workflows that you can create</span></span>
<span data-ttu-id="b7f08-117">調達には、次のワークフロー タイプが使用できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7f08-118">**タイプ**</span><span class="sxs-lookup"><span data-stu-id="b7f08-118">**Type**</span></span>                         | <span data-ttu-id="b7f08-119">**このタイプは次の目的で使用します。**</span><span class="sxs-lookup"><span data-stu-id="b7f08-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="b7f08-120">購買要求の確認</span><span class="sxs-lookup"><span data-stu-id="b7f08-120">Purchase requisition review</span></span>      | <span data-ttu-id="b7f08-121">購買要求の確認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="b7f08-122">購買要求明細行の確認</span><span class="sxs-lookup"><span data-stu-id="b7f08-122">Purchase requisition line review</span></span> | <span data-ttu-id="b7f08-123">購買要求明細行の確認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="b7f08-124">発注書ワークフロー</span><span class="sxs-lookup"><span data-stu-id="b7f08-124">Purchase order workflow</span></span>          | <span data-ttu-id="b7f08-125">発注書の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="b7f08-126">購買注文明細行ワークフロー</span><span class="sxs-lookup"><span data-stu-id="b7f08-126">Purchase order line workflow</span></span>     | <span data-ttu-id="b7f08-127">発注書明細行の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="b7f08-128">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="b7f08-128">Creating a workflow</span></span>
<span data-ttu-id="b7f08-129">ワークフローを作成するには、[購買および調達 &gt; 設定 &gt; 購買および調達ワークフロー] に移動し、ワークフローのタイプを選択して新しいワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7f08-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="b7f08-130">ワークフローのキャンバスにワークフロー要素をデザイナーにドラッグし、要素をフローにリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="b7f08-131">ワークフロー要素はコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7f08-131">The workflow elements should be configured.</span></span> <span data-ttu-id="b7f08-132">承認とタスクのワークフロー要素において、どの参加者がアクションを実行する必要があるかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="b7f08-133">参加者のタイプ</span><span class="sxs-lookup"><span data-stu-id="b7f08-133">Types of participants</span></span>
----------------------

<span data-ttu-id="b7f08-134">参加者の次のグループに承認ステップを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="b7f08-135">ユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="b7f08-135">User group</span></span>    | <span data-ttu-id="b7f08-136">説明</span><span class="sxs-lookup"><span data-stu-id="b7f08-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b7f08-137">参加者</span><span class="sxs-lookup"><span data-stu-id="b7f08-137">Participant</span></span>   | <span data-ttu-id="b7f08-138">グループまたはロールのメンバに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="b7f08-139">階層</span><span class="sxs-lookup"><span data-stu-id="b7f08-139">Hierarchy</span></span>     | <span data-ttu-id="b7f08-140">承認ステップを特定の組織階層のユーザーに割り当てます</span><span class="sxs-lookup"><span data-stu-id="b7f08-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="b7f08-141">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="b7f08-141">Workflow user</span></span> | <span data-ttu-id="b7f08-142">このワークフローのユーザーに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="b7f08-143">キュー</span><span class="sxs-lookup"><span data-stu-id="b7f08-143">Queue</span></span>         | <span data-ttu-id="b7f08-144">作業項目キューに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="b7f08-145">ユーザー</span><span class="sxs-lookup"><span data-stu-id="b7f08-145">User</span></span>          | <span data-ttu-id="b7f08-146">承認ステップを特定のユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b7f08-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="b7f08-147">参照</span><span class="sxs-lookup"><span data-stu-id="b7f08-147">See also</span></span>
--------

[<span data-ttu-id="b7f08-148">購買要求のビジネス プロセスのワークフローの定義</span><span class="sxs-lookup"><span data-stu-id="b7f08-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="b7f08-149">購買要求ワークフロー</span><span class="sxs-lookup"><span data-stu-id="b7f08-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




