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
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75daeed0d0e979165d3669e83e98cf278d7fb736
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="f824b-104">調達ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f824b-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f824b-105">組織によっては、取引を入力した個人以外のユーザーが購買要求と発注書を承認することを要求している場合があります。</span><span class="sxs-lookup"><span data-stu-id="f824b-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="f824b-106">承認プロセスを設定するには、ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="f824b-107">1 つのワークフローは 1 つの業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="f824b-107">A workflow represents a business process.</span></span> <span data-ttu-id="f824b-108">ここでは、ドキュメントの処理および承認に携わるべきユーザーを示すことによって、システムにおけるドキュメントの流れを定義します。</span><span class="sxs-lookup"><span data-stu-id="f824b-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="f824b-109">組織でワークフロー システムを使用することにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="f824b-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="f824b-110">**一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントの承認プロセスを定義できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="f824b-111">ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。</span><span class="sxs-lookup"><span data-stu-id="f824b-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="f824b-112">**プロセスの可視性** - 特定のワークフロー インスタンスのステータス、履歴およびパフォーマンス測定方法を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="f824b-113">これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f824b-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="f824b-114">**集中化された作業一覧** ユーザーはワークフローに参加するすべてのユーザーに割り当てられているワークフロー タスクおよび承認を表示するには、集中化された作業一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="f824b-115">これは、[作業項目] ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="f824b-116">作成できるワークフローのタイプ</span><span class="sxs-lookup"><span data-stu-id="f824b-116">The types of workflows that you can create</span></span>
<span data-ttu-id="f824b-117">調達には、次のワークフロー タイプが使用できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f824b-118">**タイプ**</span><span class="sxs-lookup"><span data-stu-id="f824b-118">**Type**</span></span>                         | <span data-ttu-id="f824b-119">**このタイプは次の目的で使用します。**</span><span class="sxs-lookup"><span data-stu-id="f824b-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="f824b-120">購買要求の確認</span><span class="sxs-lookup"><span data-stu-id="f824b-120">Purchase requisition review</span></span>      | <span data-ttu-id="f824b-121">購買要求の確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="f824b-122">購買要求明細行の確認</span><span class="sxs-lookup"><span data-stu-id="f824b-122">Purchase requisition line review</span></span> | <span data-ttu-id="f824b-123">購買要求の明細行の確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="f824b-124">発注書ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f824b-124">Purchase order workflow</span></span>          | <span data-ttu-id="f824b-125">発注書の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="f824b-126">購買注文明細行ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f824b-126">Purchase order line workflow</span></span>     | <span data-ttu-id="f824b-127">発注書明細行の確認および承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="f824b-128">仕入先追加申請ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f824b-128">Vendor add application workflow</span></span>  | <span data-ttu-id="f824b-129">仕入先要求経由で新しい仕入先を追加するための確認と承認ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="f824b-130">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="f824b-130">Creating a workflow</span></span>
<span data-ttu-id="f824b-131">ワークフローを作成するには、[購買および調達 &gt; 設定 &gt; 購買および調達ワークフロー] に移動し、ワークフローのタイプを選択して新しいワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="f824b-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="f824b-132">ワークフローのキャンバスにワークフロー要素をデザイナーにドラッグし、要素をフローにリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="f824b-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="f824b-133">ワークフロー要素はコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f824b-133">The workflow elements should be configured.</span></span> <span data-ttu-id="f824b-134">承認とタスクのワークフロー要素において、どの参加者がアクションを実行する必要があるかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f824b-134">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="f824b-135">参加者のタイプ</span><span class="sxs-lookup"><span data-stu-id="f824b-135">Types of participants</span></span>
----------------------

<span data-ttu-id="f824b-136">参加者の次のグループに承認ステップを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f824b-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="f824b-137">ユーザー グループ</span><span class="sxs-lookup"><span data-stu-id="f824b-137">User group</span></span>    | <span data-ttu-id="f824b-138">説明</span><span class="sxs-lookup"><span data-stu-id="f824b-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f824b-139">参加者</span><span class="sxs-lookup"><span data-stu-id="f824b-139">Participant</span></span>   | <span data-ttu-id="f824b-140">グループまたはロールのメンバに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f824b-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="f824b-141">階層</span><span class="sxs-lookup"><span data-stu-id="f824b-141">Hierarchy</span></span>     | <span data-ttu-id="f824b-142">承認ステップを特定の組織階層のユーザーに割り当てます</span><span class="sxs-lookup"><span data-stu-id="f824b-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="f824b-143">ワークフロー ユーザー</span><span class="sxs-lookup"><span data-stu-id="f824b-143">Workflow user</span></span> | <span data-ttu-id="f824b-144">このワークフローのユーザーに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f824b-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="f824b-145">キュー</span><span class="sxs-lookup"><span data-stu-id="f824b-145">Queue</span></span>         | <span data-ttu-id="f824b-146">作業項目キューに承認ステップを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f824b-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="f824b-147">ユーザー</span><span class="sxs-lookup"><span data-stu-id="f824b-147">User</span></span>          | <span data-ttu-id="f824b-148">承認ステップを特定のユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f824b-148">Assign the approval step to specific users.</span></span>                               |



<a name="additional-resources"></a><span data-ttu-id="f824b-149">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f824b-149">Additional resources</span></span>
--------

[<span data-ttu-id="f824b-150">購買要求のビジネス プロセスのワークフローの定義</span><span class="sxs-lookup"><span data-stu-id="f824b-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="f824b-151">購買要求ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f824b-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

[<span data-ttu-id="f824b-152">オンボーディングの仕入先</span><span class="sxs-lookup"><span data-stu-id="f824b-152">Onboarding vendors</span></span>](vendor-onboarding.md)


