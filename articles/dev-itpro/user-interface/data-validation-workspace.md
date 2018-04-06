---
title: "データ検証ワークスペース"
description: "データ検証チェックリスト ワークスペースを使用して、会社、エリア、人員に対してデータ検証プロセスの追跡ができます。 チェックリストは新規実装中、更新後、または移行後に使用できます。"
author: bking
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: bbf4da5a33876973a376a0580fd553e15bd6febc
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="data-validation-workspace"></a><span data-ttu-id="78de7-104">データ検証ワークスペース</span><span class="sxs-lookup"><span data-stu-id="78de7-104">Data validation workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="78de7-105">このトピックでは、**データ検証チェックリスト ワークスペース** と関連するコンフィギュレーションの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="78de7-105">This topic provides an overview of the **Data validation checklist workspace** and the associated configuration.</span></span>

## <a name="data-validation-checklist-workspace"></a><span data-ttu-id="78de7-106">データ検証チェックリスト ワークスペース</span><span class="sxs-lookup"><span data-stu-id="78de7-106">Data validation checklist workspace</span></span>

<span data-ttu-id="78de7-107">**データ検証チェックリスト** ワークスペースを使用して、会社、エリア、人員に対してデータ検証プロセスの追跡ができます。</span><span class="sxs-lookup"><span data-stu-id="78de7-107">The **Data validation checklist** workspace lets you track data validation processes across companies, areas, and people.</span></span> <span data-ttu-id="78de7-108">チェックリストは新規実装中、更新後、または移行後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-108">The checklist can be used during a new implementation, after an upgrade, or after a migration.</span></span> <span data-ttu-id="78de7-109">**データ検証チェックリスト** ワークスペースのビューに応じて、データ検証プロジェクトに対するすべてのタスクおよび状態、または自分に割り当てられたタスクのみを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="78de7-109">Depending on your view of the **Data validation checklist** workspace, you'll see either all tasks and statuses for a data validation project, or just the tasks that are assigned to you.</span></span>

<span data-ttu-id="78de7-110">最初にワークスペースの先頭でデータ検証プロジェクトを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="78de7-110">You must first select a data validation project at the top of the workspace.</span></span> <span data-ttu-id="78de7-111">ワークスペースに表示されるすべてのデータは選択したデータ検証プロジェクトにより、フィルター処理されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-111">All data that is shown in the workspace is then filtered by the selected data validation project.</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="78de7-112">概要タイル</span><span class="sxs-lookup"><span data-stu-id="78de7-112">Summary tiles</span></span>

<span data-ttu-id="78de7-113">[概要] タイルはプロセスの概要を示し、インジケーターがデータ検証プロセスを順調に進めるのに役立ちます。そのプロセスについて、すべての残余タスク、完了タスク、進行中のタスク、および開始されていないタスクを表示できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-113">The **Summary** tiles provide an overview of the process, and indicators help you keep the data validation process on track. You can see all remaining tasks, completed tasks, in progress tasks, and not started tasks for the process.</span></span> <span data-ttu-id="78de7-114">この情報は、選択されたデータ検証プロジェクトに含まれるすべての会社で使用されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-114">This information is for all companies that are included in the selected data validation project.</span></span>

### <a name="tasks-and-status-section"></a><span data-ttu-id="78de7-115">タスクと状態のセクション</span><span class="sxs-lookup"><span data-stu-id="78de7-115">Tasks and status section</span></span>

<span data-ttu-id="78de7-116">[タスクと状態] セクションで、全体のデータ検証プロジェクトの状態が、法人ごと、領域ごと、またタスク リストごとの状態といったさまざまな方法で表示されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-116">In the **Tasks and status** section, the status of the overall data validation project is displayed in various ways: status by legal entity, by area, and by task list.</span></span> <span data-ttu-id="78de7-117">特定の会社の状態を表示するフィルターを選択できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-117">You can select the filter to view the status for a specific company.</span></span> <span data-ttu-id="78de7-118">各ステータスのタブは、完成した割合および残っているタスク数の両方で内訳を表示します。</span><span class="sxs-lookup"><span data-stu-id="78de7-118">Each status tab provides a breakdown by both the percentage that has been completed and the number of tasks that remain.</span></span>

<span data-ttu-id="78de7-119">最後のタブは、詳細なタスクのリストのためにあります。</span><span class="sxs-lookup"><span data-stu-id="78de7-119">The last tab is for the detailed task list.</span></span> <span data-ttu-id="78de7-120">この一覧は、すべてのタスク リストを表示します。</span><span class="sxs-lookup"><span data-stu-id="78de7-120">This list shows the full task list.</span></span>
<span data-ttu-id="78de7-121">複数の方法でタスク リストをフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-121">You can filter the task list in several ways.</span></span> <span data-ttu-id="78de7-122">[タスクの編集] をクリックしてタスクの状態を変更するかタスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="78de7-122">Click **Edit task** to change the status of a task or assign a task.</span></span> <span data-ttu-id="78de7-123">[添付ファイル] をクリックしてタスクの添付ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="78de7-123">Click **Attachments** to view attachments for a task.</span></span>

<span data-ttu-id="78de7-124">タスク名はユーザーが作業を完了するために閲覧する必要がある Microsoft Dynamics 365 for Finance and Operations ページへのハイパーリンクです。</span><span class="sxs-lookup"><span data-stu-id="78de7-124">The task name is a hyperlink to the Microsoft Dynamics 365 for Finance and Operations page where the user must go to complete the work.</span></span> <span data-ttu-id="78de7-125">[データ検証プロジェクトのコンフィギュレーション] フォームからタスクを編集または作成する際に [メニュー項目名] フィールド を使用してこのハイパーリンクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-125">You can set this hyperlink by using the **Menu item name** field when you edit or create a task from the **Configure data validation project** form.</span></span>

<span data-ttu-id="78de7-126">[添付ファイル] アクションを使用して、ファイル、注記、画像、URL を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="78de7-126">You can attach files, notes, images, and URLs to a task by using the **Attachments** action.</span></span> <span data-ttu-id="78de7-127">たとえば、タスクに対して印刷されたレポート ファイルを添付することができます。</span><span class="sxs-lookup"><span data-stu-id="78de7-127">For example, you can attach a report file that was printed for a task.</span></span> <span data-ttu-id="78de7-128">添付ファイルが存在する場合には、[添付ファイル] 列にアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-128">An icon appears in the **Attachment** column for the task if an attachment is present.</span></span>

<span data-ttu-id="78de7-129">[完了処理実施者] オプションには、作業が完了した後にタスクを完了した作業者の名前が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-129">The **Completed by** option will be automatically filled after the task is completed with the name of the worker who completed the task.</span></span> <span data-ttu-id="78de7-130">タスクが完了としてマークされると、[完了日] フィールドが、現在の日時に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="78de7-130">When a task is marked as completed, the **Completed date** field is automatically updated to the current date and time.</span></span>

### <a name="configure-data-validation-project-page"></a><span data-ttu-id="78de7-131">データ検証プロジェクト ページのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="78de7-131">Configure data validation project page</span></span>

<span data-ttu-id="78de7-132">**データ検証チェックリスト** ワークスペースを使用する前に [データ検証プロジェクトのコンフィギュレーション] ページを使用してプロセスをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="78de7-132">Before you can use the **Data validation checklist** workspace, you must configure the process by using the **Configure data validation project** page.</span></span> <span data-ttu-id="78de7-133">([ワークスペース] \> [データ検証チェックリスト] \> [データ検証プロジェクトのコンフィギュレーション] をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="78de7-133">(Click **Workspaces** \> **Data validation checklist** \> **Configure data validation project**.)</span></span>

### <a name="task-areas"></a><span data-ttu-id="78de7-134">タスク領域</span><span class="sxs-lookup"><span data-stu-id="78de7-134">Task areas</span></span>

<span data-ttu-id="78de7-135">タスク領域を使用して、データ検証タスクを組織内の所有権の論理領域にグループ化します。</span><span class="sxs-lookup"><span data-stu-id="78de7-135">You use task areas to group data validation tasks into logical areas of ownership within your organization.</span></span> <span data-ttu-id="78de7-136">たとえば、買掛金勘定、売掛金勘定、または総勘定元帳がタスク領域として使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="78de7-136">For example, Accounts payable, Accounts receivable, or General ledger might be used as task areas.</span></span>

<span data-ttu-id="78de7-137">[メニュー項目名] はタスク作業工数に関連付けられており、ワークスペースのタスク リンクから関連するページに直接移動するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="78de7-137">The **Menu item name** is associated with the task work effort and can be used to go directly to the associated page from the task link in the workspace.</span></span> <span data-ttu-id="78de7-138">たとえば、買掛金勘定の **買掛金勘定エイジング** レポートを実行するデータ検証タスクは、[買掛金勘定エイジング レポート] ページにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="78de7-138">For example, a data validation task to run the **Accounts payable aging** report for Accounts payable can be linked to the **Accounts payable aging report** page.</span></span>

