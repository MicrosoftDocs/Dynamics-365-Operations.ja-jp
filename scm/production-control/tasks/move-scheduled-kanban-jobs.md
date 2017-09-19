--- 
title: "スケジュール済みかんばん作業の移動"
description: "この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="8e066-103">スケジュール済みかんばん作業の移動</span><span class="sxs-lookup"><span data-stu-id="8e066-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e066-104">この手順は、計画済のプロセスかんばんジョブを別の期間に移動することに焦点をあてます。</span><span class="sxs-lookup"><span data-stu-id="8e066-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="8e066-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8e066-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e066-106">この手順は、かんばんを処理する作業現場の監督または生産計画担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8e066-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="8e066-107">スケジュール済みかんばんジョブを選択する</span><span class="sxs-lookup"><span data-stu-id="8e066-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="8e066-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="8e066-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="8e066-109">!MtCMR! [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e066-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="8e066-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="8e066-110">áçêìõý !</span></span>
3. <span data-ttu-id="8e066-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8e066-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="8e066-112">作業セル 1250 を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e066-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="8e066-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="8e066-113">Klik på Select.</span></span>
5. <span data-ttu-id="8e066-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="8e066-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="8e066-115">これは、スケジュール済のかんばんジョブのみを表示するジョブ一覧をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="8e066-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="8e066-116">別の期間へのジョブの移動</span><span class="sxs-lookup"><span data-stu-id="8e066-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="8e066-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8e066-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="8e066-118">たとえば、[計画期間] フィールドにある 2012 年 12 月 20 日にスケジュールされたジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e066-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="8e066-119">その後、ジョブを以前の期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e066-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="8e066-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="8e066-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="8e066-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="8e066-121">Klik på End.</span></span>
    * <span data-ttu-id="8e066-122">これにより、前の期間内にある最後のジョブとしてジョブ リストの最後にジョブが移動されます。</span><span class="sxs-lookup"><span data-stu-id="8e066-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="8e066-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8e066-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="8e066-124">たとえば、[計画期間] フィールドにある 2012 年 12 月 18 日にスケジュールされたジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e066-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="8e066-125">その後、ジョブを次の期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e066-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="8e066-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="8e066-126">Klik på Next period.</span></span>
6. <span data-ttu-id="8e066-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="8e066-127">Klik på Start.</span></span>
    * <span data-ttu-id="8e066-128">これにより、前の期間内にある最初のジョブとしてジョブ リストの最初にジョブが移動されます。</span><span class="sxs-lookup"><span data-stu-id="8e066-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="8e066-129">タスク: 期間内へのジョブの移動</span><span class="sxs-lookup"><span data-stu-id="8e066-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="8e066-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="8e066-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="8e066-131">たとえば、[計画期間] フィールドにある 2012 年 12 月 19 日にスケジュールされた 2 番目のジョブなど、ジョブ ステータスが計画済みとなっているジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e066-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="8e066-132">その後、計画期間内にジョブを移動します。</span><span class="sxs-lookup"><span data-stu-id="8e066-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="8e066-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="8e066-133">Klik på Forward.</span></span>
    * <span data-ttu-id="8e066-134">一覧でジョブが 1 行下へ移動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e066-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="8e066-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="8e066-135">Klik på Backward.</span></span>
    * <span data-ttu-id="8e066-136">一覧でジョブが 1 行上へ移動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e066-136">Notice that the job is moved one line up on the list.</span></span>  

