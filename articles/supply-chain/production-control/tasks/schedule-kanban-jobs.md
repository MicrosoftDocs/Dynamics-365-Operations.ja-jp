--- 
title: "かんばん作業のスケジューリング"
description: "この手順は、特定の作業セルに対してプロセスかんばん作業をスケジュールすることに焦点を当てています。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5170fecf0190591d74f45d35fecc4472e7f5e900
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="bb2cb-103">かんばん作業のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="bb2cb-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb2cb-104">この手順は、特定の作業セルに対してプロセスかんばん作業をスケジュールすることに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="bb2cb-105">「材料が利用可能な場合にプロセスかんばん作業を準備する」という手順は、この手順を作成するための前提条件です。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="bb2cb-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bb2cb-107">このタスクは、かんばんを処理する作業現場の監督と生産計画担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="bb2cb-108">作業セルにかんばん作業を選択する</span><span class="sxs-lookup"><span data-stu-id="bb2cb-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="bb2cb-109">[生産管理] > [かんばん] > [かんばん作業スケジューリング] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="bb2cb-110">[期間能力ファクト ボックス] の展開</span><span class="sxs-lookup"><span data-stu-id="bb2cb-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="bb2cb-111">「かんばん情報ボックス」を展開します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="bb2cb-112">[作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bb2cb-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bb2cb-114">作業セル 1250 を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-114">Select work cell 1250.</span></span> <span data-ttu-id="bb2cb-115">これによって、作業セル 1250 のジョブのみを表示するビューをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="bb2cb-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bb2cb-117">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="bb2cb-118">最初に作業可能な期間内にかんばん作業をスケジュールする</span><span class="sxs-lookup"><span data-stu-id="bb2cb-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="bb2cb-119">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bb2cb-120">ステータスが [未計画] になっている一覧の最初の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="bb2cb-121">[ジョブ ステータス] フィールドにある点を打たれたアイコンは、未計画を示します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="bb2cb-122">[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-122">Click Schedule.</span></span>
    * <span data-ttu-id="bb2cb-123">これにより、最初に作業可能な期間内にかんばん作業をスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="bb2cb-124">かんばん作業は今日から開始期間に追加されたため、かんばん作業をリストの最後に移動するように注意します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="bb2cb-125">今日の日付を起点として開始した期間が完全に予約されると、ジョブは最初に作業可能な期間に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="bb2cb-126">特定の日に 2 つのかんばん作業をスケジュールする</span><span class="sxs-lookup"><span data-stu-id="bb2cb-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="bb2cb-127">一覧で行 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="bb2cb-128">最初の行の [ジョブ ステータス] フィールドが [未計画] ステータスになっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="bb2cb-129">一覧で行 2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="bb2cb-130">2 番目の行の [ジョブ ステータス] フィールドが [未計画] ステータスになっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="bb2cb-131">ここで、最初の 2 つのジョブを選択しています。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="bb2cb-132">[スケジュール開始日] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="bb2cb-133">[書きの能力不足の反応] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="bb2cb-134">このオプションでは、既定能力不足に対する反応を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="bb2cb-135">[能力不足に対する反応] フィールドで、[要求された期間設定に追加] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="bb2cb-136">このオプションによって、作業セルが過負荷状態になっているかに関係なく、ジョブが要求された期間に追加されるようにします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="bb2cb-137">[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-137">Click Schedule.</span></span>
    * <span data-ttu-id="bb2cb-138">両方のジョブが目的としている期間に追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="bb2cb-139">[期間能力] セクションで、各期間の負荷を確認できます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="bb2cb-140">[消費] フィールドにはこの期間にスケジューリングされた消費が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="bb2cb-141">スケジュールされた消費がこの期間に使用可能な能力よりも高い場合、負荷状態にある消費が選択されます。</span><span class="sxs-lookup"><span data-stu-id="bb2cb-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


