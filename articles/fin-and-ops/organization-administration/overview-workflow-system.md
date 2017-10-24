---
title: "ワークフローの概要"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについて説明します。"
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6622f0e5ed6c38bb8131d13aa02061968862678b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="5ebce-103">ワークフローの概要</span><span class="sxs-lookup"><span data-stu-id="5ebce-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5ebce-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5ebce-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="5ebce-105">ワークフローについて</span><span class="sxs-lookup"><span data-stu-id="5ebce-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="5ebce-106">*ワークフロー*という用語は 2 とおりに定義できます。それは、システムとしての定義と、業務プロセスとしての定義です。</span><span class="sxs-lookup"><span data-stu-id="5ebce-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="5ebce-107">システムとしてのワークフロー</span><span class="sxs-lookup"><span data-stu-id="5ebce-107">Workflow is a system</span></span>

<span data-ttu-id="5ebce-108">ワークフローは、Finance および Operations と共にインストールされるシステムで、Application Object Server (AOS) で実行されます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="5ebce-109">ワークフロー システムによって提供される機能を使用して、個々のワークフローまたは業務プロセスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="5ebce-110">業務プロセスとしてのワークフロー</span><span class="sxs-lookup"><span data-stu-id="5ebce-110">Workflow is a business process</span></span>

<span data-ttu-id="5ebce-111">1 つのワークフローは 1 つの業務プロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="5ebce-111">A workflow represents a business process.</span></span> <span data-ttu-id="5ebce-112">ここでは、タスクを完了し、決定を下し、ドキュメントを承認するユーザーを示すことによって、システムにおけるドキュメントの流れ (移動) を定義します。</span><span class="sxs-lookup"><span data-stu-id="5ebce-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="5ebce-113">たとえば、次の図は経費精算書のワークフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="5ebce-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![ユーザーに割り当てられた要素を含むワークフロー](./media/workflow_user.gif) 

<span data-ttu-id="5ebce-115">このワークフローをよりよく理解するため、Sam が USD 7,000 の経費精算書を送信したと仮定します。</span><span class="sxs-lookup"><span data-stu-id="5ebce-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="5ebce-116">このシナリオでは、Sam から送られた領収書を Ivan が確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ebce-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="5ebce-117">その後、Frank と Sue が経費精算書を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ebce-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="5ebce-118">次に、Sam が USD 11,000 の経費精算書を送信したとします。</span><span class="sxs-lookup"><span data-stu-id="5ebce-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="5ebce-119">このシナリオでは、Ivan が領収書を確認する必要があり、Frank、Sue、および Ann が経費精算書を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ebce-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="5ebce-120">ワークフロー システムを使用する利点</span><span class="sxs-lookup"><span data-stu-id="5ebce-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="5ebce-121">組織でワークフロー システムを使用することにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="5ebce-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="5ebce-122">**一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントをどのように処理するか定義できます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="5ebce-123">ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="5ebce-124">**プロセスの可視性** – ワークフロー インスタンスの状態、履歴およびパフォーマンス測定方法を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="5ebce-125">これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="5ebce-126">**集中化された作業一覧** – ユーザーは、集中化された作業一覧を表示して、自分に割り当てられているワークフロー タスクおよび承認を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5ebce-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="5ebce-127">ワークフロー コンテンツ</span><span class="sxs-lookup"><span data-stu-id="5ebce-127">Workflow content</span></span>

+ [<span data-ttu-id="5ebce-128">ワークフロー アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="5ebce-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="5ebce-129">ワークフロー要素</span><span class="sxs-lookup"><span data-stu-id="5ebce-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="5ebce-130">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="5ebce-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="5ebce-131">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="5ebce-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="5ebce-132">ワークフロー プロパティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="5ebce-133">ワークフローでの手動タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="5ebce-134">ワークフローでの自動化タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="5ebce-135">ワークフローでの承認プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="5ebce-136">ワークフローでの承認ステップのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="5ebce-137">ワークフローでの手動決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="5ebce-138">ワークフローでの条件付き意思決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="5ebce-139">ワークフローでの並列活動のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="5ebce-140">ワークフローでの並列分岐コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="5ebce-141">品目ワークフローのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ebce-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

