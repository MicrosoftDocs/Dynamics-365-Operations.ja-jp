---
title: "ワークフロー要素"
description: "この記事は、ワークフローを構成するさまざまな要素について説明します。"
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 255777651a45b899850fc870c9da288f65df702c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="57790-103">ワークフロー要素</span><span class="sxs-lookup"><span data-stu-id="57790-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="57790-104">この記事は、ワークフローを構成するさまざまな要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="57790-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="57790-105">ワークフローは "要素" から構成されます。</span><span class="sxs-lookup"><span data-stu-id="57790-105">A workflow consists of elements.</span></span> <span data-ttu-id="57790-106">次のセクションでは、要素の各タイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="57790-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="57790-107">タスク</span><span class="sxs-lookup"><span data-stu-id="57790-107">Tasks</span></span>
<span data-ttu-id="57790-108">*タスク*とは、実行する必要のある作業単位です。</span><span class="sxs-lookup"><span data-stu-id="57790-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="57790-109">ワークフローに追加できるタスクには、手動タスクと自動化タスクの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="57790-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="57790-110">手動タスク</span><span class="sxs-lookup"><span data-stu-id="57790-110">Manual task</span></span>

<span data-ttu-id="57790-111">*手動タスク*は、ユーザーが実行する必要がある作業単位です。</span><span class="sxs-lookup"><span data-stu-id="57790-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="57790-112">たとえば、経費精算書ワークフローの手動タスクの場合、担当ユーザーは、次のアクションを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57790-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="57790-113">経費精算書と共に提出された領収書の確認。</span><span class="sxs-lookup"><span data-stu-id="57790-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="57790-114">従業員の管理者への電話。</span><span class="sxs-lookup"><span data-stu-id="57790-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="57790-115">自動化タスク</span><span class="sxs-lookup"><span data-stu-id="57790-115">Automated task</span></span>

<span data-ttu-id="57790-116">*自動化タスク*は、システムが実行する必要がある作業単位です。</span><span class="sxs-lookup"><span data-stu-id="57790-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="57790-117">ユーザーの介在を必要としません。</span><span class="sxs-lookup"><span data-stu-id="57790-117">No human interaction is required.</span></span> <span data-ttu-id="57790-118">たとえば、販売注文ワークフローには、システムが完了しなければならない次のような自動化タスクがあります。</span><span class="sxs-lookup"><span data-stu-id="57790-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="57790-119">与信チェックの実行。</span><span class="sxs-lookup"><span data-stu-id="57790-119">Perform a credit check.</span></span>
-   <span data-ttu-id="57790-120">顧客の顧客レコードの作成 (レコードがまだ存在しない場合)。</span><span class="sxs-lookup"><span data-stu-id="57790-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="57790-121">承認プロセス</span><span class="sxs-lookup"><span data-stu-id="57790-121">Approval processes</span></span>
<span data-ttu-id="57790-122">*承認プロセス*は、複数のステップから構成されるプロセスです。</span><span class="sxs-lookup"><span data-stu-id="57790-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="57790-123">各承認ステップで、ユーザーは次の操作を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="57790-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="57790-124">ドキュメントの承認。</span><span class="sxs-lookup"><span data-stu-id="57790-124">Approve the document.</span></span>
-   <span data-ttu-id="57790-125">ドキュメントの否認。</span><span class="sxs-lookup"><span data-stu-id="57790-125">Reject the document.</span></span>
-   <span data-ttu-id="57790-126">ドキュメントに対する変更依頼。</span><span class="sxs-lookup"><span data-stu-id="57790-126">Request a change to the document.</span></span>
-   <span data-ttu-id="57790-127">別のユーザーへの承認対象ドキュメントの割り当て。</span><span class="sxs-lookup"><span data-stu-id="57790-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="57790-128">行項目ワークフローの要素</span><span class="sxs-lookup"><span data-stu-id="57790-128">Lineitem workflow elements</span></span>
<span data-ttu-id="57790-129">ワークフローを作成して、ドキュメントやドキュメントの行項目を処理できます。</span><span class="sxs-lookup"><span data-stu-id="57790-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="57790-130">たとえば、タイムシートの承認ワークフローが作成済みであるとします。</span><span class="sxs-lookup"><span data-stu-id="57790-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="57790-131">(このワークフローを*ドキュメント ワークフロー*と呼びます。) そのドキュメント ワークフローには、*行項目 ワークフロー* 要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="57790-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="57790-132">行項目要素の実行時には、ドキュメントの各行項目が処理のために送信されます。</span><span class="sxs-lookup"><span data-stu-id="57790-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="57790-133">すべての行項目を同じ行項目ワークフローで処理することも、各行項目を異なる行項目ワークフローで処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="57790-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="57790-134">従業員が、次の図のようなタイム シートを提出したとします。</span><span class="sxs-lookup"><span data-stu-id="57790-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![行項目を含むワークフロー](./media/workflow_lineitemworkflow.gif) 

<span data-ttu-id="57790-136">このシナリオの場合は、次のような行項目ワークフローを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="57790-136">In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="57790-137">**行項目ワークフロー 1** – このワークフローは、プロジェクト ID が 1111 の行項目の処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57790-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="57790-138">**行項目ワークフロー 2** – このワークフローは、プロジェクト ID が 2222 の行項目の処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57790-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="57790-139">**行項目ワークフロー 3** – このワークフローは、プロジェクト ID が 3333 の行項目の処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="57790-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="57790-140">フロー制御要素</span><span class="sxs-lookup"><span data-stu-id="57790-140">Flowcontrol elements</span></span>
<span data-ttu-id="57790-141">次の要素を使用すると、同時に実行される代替分岐または分岐があるワークフローを設計できます。</span><span class="sxs-lookup"><span data-stu-id="57790-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="57790-142">手動決定</span><span class="sxs-lookup"><span data-stu-id="57790-142">Manual decision</span></span>

<span data-ttu-id="57790-143">*手動決定*は、ワークフローが 2 つの分岐に分かれるポイントです。</span><span class="sxs-lookup"><span data-stu-id="57790-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="57790-144">ユーザーが判断を行い、その判断によって、提出済のドキュメントをどちらの分岐で処理するかが決定されます。</span><span class="sxs-lookup"><span data-stu-id="57790-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="57790-145">条件付き意思決定</span><span class="sxs-lookup"><span data-stu-id="57790-145">Conditional decision</span></span>

<span data-ttu-id="57790-146">*条件判断*も、ワークフローが 2 つの分岐に分かれるポイントです。</span><span class="sxs-lookup"><span data-stu-id="57790-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="57790-147">ただし、送信されたドキュメントを処理するのにどちらの分岐を使用するかはシステムが決定します。</span><span class="sxs-lookup"><span data-stu-id="57790-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="57790-148">この決定をするために、システムは文書を評価し、特定の条件を満たしているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="57790-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="57790-149">並列活動</span><span class="sxs-lookup"><span data-stu-id="57790-149">Parallel activity</span></span>

<span data-ttu-id="57790-150">*並列活動*とは、同時に実行する 2 つ以上のワークフロー分岐を含むワークフロー要素です。</span><span class="sxs-lookup"><span data-stu-id="57790-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="57790-151">サブワークフロー</span><span class="sxs-lookup"><span data-stu-id="57790-151">Subworkflow</span></span>

<span data-ttu-id="57790-152">*サブワークフロー*は、他のワークフローのコンテキストで実行するワークフローです。</span><span class="sxs-lookup"><span data-stu-id="57790-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




