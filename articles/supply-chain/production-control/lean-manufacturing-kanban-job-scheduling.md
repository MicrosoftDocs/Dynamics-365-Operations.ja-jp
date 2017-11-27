---
title: "リーン生産でのかんばん作業のスケジューリング"
description: "この記事は、かんばん作業のスケジューリングにおける視覚コントロールおよびさまざまな方法に関する情報を提供します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6ac4c1afecb72d4007d830a9927bd3171ddd48ec
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a><span data-ttu-id="8dc83-103">リーン生産でのかんばん作業のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="8dc83-103">Kanban job scheduling for lean manufacturing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8dc83-104">この記事は、かんばん作業のスケジューリングにおける視覚コントロールおよびさまざまな方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-104">This article provides information about visual control over kanban job scheduling and various ways to schedule kanban jobs.</span></span>  

<span data-ttu-id="8dc83-105">**かんばん作業のスケジューリング**ページでは、リーン生産の作業セルのスケジュールを視覚的にコントロールできます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-105">The **Kanban job scheduling** page provides visual control over the schedules of lean manufacturing work cells.</span></span> <span data-ttu-id="8dc83-106">すべてのかんばん作業の概要が示されており、複数のフィルタ処理機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="8dc83-106">It gives an overview of all kanban jobs and provides multiple filtering capabilities.</span></span> <span data-ttu-id="8dc83-107">このページから、かんばんコンフィギュレーションと実行に関連した他のすべてのページに移動できます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-107">From this page, you can move to all other pages that are related to kanban configuration and execution.</span></span>

## <a name="automatic-scheduling-of-kanban-jobs"></a><span data-ttu-id="8dc83-108">かんばん作業の自動スケジューリング</span><span class="sxs-lookup"><span data-stu-id="8dc83-108">Automatic scheduling of kanban jobs</span></span>
<span data-ttu-id="8dc83-109">スケジューリングは、かんばんルールの**自動計画数量**パラメーターを設定することにより自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-109">Scheduling can be triggered automatically if you set the **Automatic planning quantity** parameter on the kanban rule.</span></span> <span data-ttu-id="8dc83-110">**自動計画数量**を**1**に設定した場合、各かんばん作業は作成後すぐに計画されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-110">If you set **Automatic planning quantity** to **1**, each kanban job is planned immediately when it's created.</span></span> <span data-ttu-id="8dc83-111">結果は、一連の最初のプル、最初のサービス操作です。</span><span class="sxs-lookup"><span data-stu-id="8dc83-111">The result is a series of first pull, first serve operations.</span></span> <span data-ttu-id="8dc83-112">**自動計画数量**に 1 を超える値をセットした場合、かんばん作業は計画前にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-112">If you set **Automatic planning quantity** to a value that is more than 1, kanban jobs are grouped before they are planned.</span></span> 

<span data-ttu-id="8dc83-113">このコンセプトにより、かんばんのサイズを実際の経済的なバッチサイズより低くすることができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-113">This concept enables kanban sizes to be reduced below the actual economic batch sizes.</span></span> <span data-ttu-id="8dc83-114">たとえば、特定の品目 (または品目ファミリ) の経済的なバッチ サイズは 30 です。</span><span class="sxs-lookup"><span data-stu-id="8dc83-114">For example, the economic batch size for a specific item (or item family) is 30.</span></span> <span data-ttu-id="8dc83-115">製品数量を 30 にしてかんばんを作成する代わりに、かんばんルールを設定して製品数量を 10 にし、**自動計画数量** の値を **3** にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-115">Instead of creating kanbans that use the product quantity, 30, you can configure the kanban rule so that it has a product quantity of 10 and an **Automatic planning quantity** value of **3**.</span></span> <span data-ttu-id="8dc83-116">3 つの予定外のジョブがある場合にのみ自動計画は、作業セルにかんばん作業をスケジュールしますが、スケジューリングをする人と作業現場の監督者には、2 つの予定外のジョブが実行待ちかもしれないことははっきりと分かります。</span><span class="sxs-lookup"><span data-stu-id="8dc83-116">Although automatic planning schedules the kanban jobs for the work cell only when three unplanned jobs exist, it's fully transparent to the planner and the shop floor supervisor that two unplanned jobs might be awaiting execution.</span></span> <span data-ttu-id="8dc83-117">スケジューリングをする人やマネージャーは、手動でその作業をスケジュールするか、追加のかんばんを作成することでそれら 2 つの作業の生産を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-117">The planner or shop floor manager can then take those two jobs into production by manually planning them or creating additional kanbans.</span></span>

## <a name="manual-scheduling"></a><span data-ttu-id="8dc83-118">手動のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="8dc83-118">Manual scheduling</span></span>
<span data-ttu-id="8dc83-119">手動のスケジューリングについては、Microsoft Dynamics AX 2012 では、かんばんスケジューリング ボードが導入されています。</span><span class="sxs-lookup"><span data-stu-id="8dc83-119">For manual scheduling, Microsoft Dynamics AX 2012 introduced the kanban scheduling board.</span></span> <span data-ttu-id="8dc83-120">手動スケジューリングは、自動スケジューリングと組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-120">Manual scheduling can be combined with automatic scheduling.</span></span> <span data-ttu-id="8dc83-121">かんばんスケジューリング ボードでは、作業の計画や削除、順序の変更、または期間の変更などができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-121">The kanban scheduling board lets you plan and unplan jobs, moved them in sequence, or move them from period to period.</span></span> <span data-ttu-id="8dc83-122">かんばんルールに基づく作業のうち、**自動計画**の値が **0** より大きい場合は、手動で計画の削除ができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-122">Jobs that are based on a kanban rule where the **Automatic planning** value is more than **0** can be manually unplanned.</span></span> <span data-ttu-id="8dc83-123">ただし、これらの作業は、次の自動計画のイベントが発生したとき (つまり、新しいかんばんが作成されたとき) には変更されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-123">However, these jobs will be replanned when the next automatic planning event occurs (that is, when a new kanban is created).</span></span> <span data-ttu-id="8dc83-124">次のオプションが手動スケジューリングで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-124">The following options are available for manual scheduling:</span></span>

-   <span data-ttu-id="8dc83-125">[**スケジュール**] 期日に従って、選択された作業がスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-125">**Schedule** schedules the selected jobs according to their due date.</span></span> <span data-ttu-id="8dc83-126">(このオプションは自動計画に似ています)</span><span class="sxs-lookup"><span data-stu-id="8dc83-126">(This option resembles automatic planning.)</span></span>
-   <span data-ttu-id="8dc83-127">[**日付から順方向でスケジュール**] 選択された作業を期日に従ってスケジュールしますが、指定された最も早い作業開始日を使用して結果を制御します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-127">**Schedule forward from date** tries to schedule the selected jobs according to their due date but constrains the result by using the specified earliest start date.</span></span>
-   <span data-ttu-id="8dc83-128">[**バックワード**] 選択されたスケジュール作業順序を期間内でバックさせます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-128">**Backward** moves the selected scheduled jobs back in the sequence within the period.</span></span>
-   <span data-ttu-id="8dc83-129">[**フォワード**] 選択されたスケジュール作業順序を期間内で進めます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-129">**Forward** moves the selected scheduled jobs forward in the sequence with the period.</span></span>
-   <span data-ttu-id="8dc83-130">[**前の期間**] 選択したスケジュール作業を前の期間の最初か最後に移動します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-130">**Previous period** moves the selected scheduled jobs to the start or end of the previous period.</span></span>
-   <span data-ttu-id="8dc83-131">[**次の期間**] 選択したスケジュール作業を次の期間の最初か最後に移動します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-131">**Next period** moves the selected scheduled jobs to the start or end of the next period.</span></span>
-   <span data-ttu-id="8dc83-132">[**計画**] &gt; [**ジョブ状態を元に戻す**] は、スケジュールされたジョブを取り消します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-132">**Plan** &gt; **Revert job status** lets you unschedule a scheduled job.</span></span>

## <a name="lean-scheduling-groups"></a><span data-ttu-id="8dc83-133">リーン スケジューリング グループ</span><span class="sxs-lookup"><span data-stu-id="8dc83-133">Lean scheduling groups</span></span>
<span data-ttu-id="8dc83-134">各色は、リーン スケジューリング グループを表します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-134">Each color represents a lean scheduling group.</span></span> <span data-ttu-id="8dc83-135">リーン スケジューリング グループは、一般的なグループ、または 1 つの作業セルに属するグループとして自由に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-135">Lean scheduling groups can be freely defined as generic groups or as groups that belong to a single work cell.</span></span> <span data-ttu-id="8dc83-136">品目と分析コードはスケジューリング グループに自由に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-136">Items and dimensions can be freely assigned to the scheduling groups.</span></span> <span data-ttu-id="8dc83-137">たとえば、色付きのセルで、スケジュール グループは製品の色を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-137">For example, in a Painting cell, a schedule group can represent a color of the product.</span></span> <span data-ttu-id="8dc83-138">特定の工具が必要な作業には、品目は工具の要件によってグループ化できます。また、梱包の作業セルでは、梱包のテンプレートによって品目をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-138">In work that is driven by specific tooling requirements, items might be grouped by tool requirement, and a packaging work cell might group items by packaging template.</span></span> <span data-ttu-id="8dc83-139">リーン スケジューリング グループの色の使用はオプションで選択できますが、推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="8dc83-139">The use of colors for lean scheduling groups is optional but recommended.</span></span> <span data-ttu-id="8dc83-140">これにより、計画のステータスの可視性が向上します。</span><span class="sxs-lookup"><span data-stu-id="8dc83-140">It improves visibility into the status of the plan.</span></span> <span data-ttu-id="8dc83-141">たとえば、どの色がどの日に製造されるかがすぐに分かり、その作業を最適化する方法が一目で分かります。</span><span class="sxs-lookup"><span data-stu-id="8dc83-141">For example, it's very easy to see which colors are produced on which day, and you can tell at a glance how this work can be optimized.</span></span>

## <a name="work-cell-capacity-and-period-capacity"></a><span data-ttu-id="8dc83-142">作業セルの能力と期間能力</span><span class="sxs-lookup"><span data-stu-id="8dc83-142">Work cell capacity and period capacity</span></span>
<span data-ttu-id="8dc83-143">リーン作業セルの能力は常に並行な能力です。</span><span class="sxs-lookup"><span data-stu-id="8dc83-143">The capacity of a lean work cell is always concurrent capacity.</span></span> <span data-ttu-id="8dc83-144">つまり、複数のジョブを、作業セルで同時に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-144">In other words, multiple jobs can be active in a work cell at the same time.</span></span> <span data-ttu-id="8dc83-145">能力は、スループット モードと時刻モードで追跡できます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-145">The capacity can be tracked in two modes: throughput and hours.</span></span>

### <a name="throughput"></a><span data-ttu-id="8dc83-146">スループット</span><span class="sxs-lookup"><span data-stu-id="8dc83-146">Throughput</span></span>

<span data-ttu-id="8dc83-147">作業セルの能力は、参照期間 (標準的な作業日、週、または月) の平均スループットの数量により定義されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-147">The capacity of a work cell is defined by the average throughput quantity of a reference period (standard workday, week, or month).</span></span> <span data-ttu-id="8dc83-148">1 日または週あたりの実際の能力は、作業セルに割り当てられたカレンダーの作業時間に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-148">The actual capacity per day or week is then calculated based on the working times of the calendar that is assigned to the work cell.</span></span> <span data-ttu-id="8dc83-149">ジョブによって読み込まれる能力は、作業セルの品目のスループットの割合によって調整されたジョブの数量です。</span><span class="sxs-lookup"><span data-stu-id="8dc83-149">The capacity that is loaded by job is the quantity of the job, adjusted by the throughput ratio of the item in the work cell.</span></span>

### <a name="hours"></a><span data-ttu-id="8dc83-150">時間</span><span class="sxs-lookup"><span data-stu-id="8dc83-150">Hours</span></span>

<span data-ttu-id="8dc83-151">日または週単位に使用可能な能力は、作業セルに割り当てられたカレンダーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-151">The available capacity by day or week is defined by the calendar that is assigned to the work cell.</span></span> <span data-ttu-id="8dc83-152">ジョブによって読み込まれる能力は、数量 (デフォルトの活動数量対実際のジョブ数量) と作業セルの品目のスループットの割合によって調整された活動のサイクル時間です。</span><span class="sxs-lookup"><span data-stu-id="8dc83-152">The capacity that is loaded by job is the cycle time of the activity, adjusted by the quantity (default activity quantity versus actual job quantity) and the throughput ratio of the item in the work cell.</span></span>

#### <a name="period-capacity-factbox"></a><span data-ttu-id="8dc83-153">期間能力情報ボックス</span><span class="sxs-lookup"><span data-stu-id="8dc83-153">Period capacity FactBox</span></span>

<span data-ttu-id="8dc83-154">**かんばん作業スケジューリング** リスト ページには、選択した作業セルの使用可能な能力と予約された期間の能力を示す情報ボックスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-154">The **Kanban job scheduling** list page contains a FactBox that shows the available and booked period capacity for the selected work cell.</span></span> <span data-ttu-id="8dc83-155">生産フロー モデルの選択されたスケジュールの期間によって、期間の日数または週が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8dc83-155">Depending on the selected schedule periods in the production flow model, the periods show days or weeks.</span></span>

<a name="see-also"></a><span data-ttu-id="8dc83-156">参照</span><span class="sxs-lookup"><span data-stu-id="8dc83-156">See also</span></span>
--------




