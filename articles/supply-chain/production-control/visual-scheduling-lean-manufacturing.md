---
title: リーン生産の視覚的スケジューリング
description: このトピックでは、生産計画担当者がかんばん作業の生産計画を制御し最適化するために使用できる、かんばんスケジュール ボードに関する情報を提供します。
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6710dcb1cb53e7221b03b35ceee5ac8e055b6dd2
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826409"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a><span data-ttu-id="d1a91-103">リーン生産の視覚的スケジューリング</span><span class="sxs-lookup"><span data-stu-id="d1a91-103">Visual scheduling for lean manufacturing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1a91-104">このトピックでは、生産計画担当者がかんばん作業の生産計画を制御し最適化するために使用できる、かんばんスケジュール ボードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-104">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="d1a91-105">このトピックでは、生産計画担当者がかんばん作業の生産計画を制御し最適化するために使用できる、かんばんスケジュール ボードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-105">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="d1a91-106">かんばんスケジュール ボードにより、生産計画担当者はかんばん作業の生産計画を制御し最適化できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-106">The Kanban schedule board lets the production planner control and optimize the production plan for kanban jobs.</span></span> <span data-ttu-id="d1a91-107">かんばん作業の流れを分かりやすくし、および生産計画担当者に、リーン生産作業セルの生産計画を最適化し調整するためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-107">It makes the flow of kanban jobs transparent, and gives the production planner a tool that optimizes and adjusts the production plan for the lean manufacturing work cell.</span></span>

## <a name="visual-scheduling-of-kanban-jobs"></a><span data-ttu-id="d1a91-108">かんばん作業の視覚的スケジューリング</span><span class="sxs-lookup"><span data-stu-id="d1a91-108">Visual scheduling of kanban jobs</span></span>
<span data-ttu-id="d1a91-109">かんばん作業は、1 つまたは複数のかんばん作業で構成できます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-109">A kanban job can consist of one or many kanban jobs.</span></span> <span data-ttu-id="d1a91-110">かんばん作業には、2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-110">There are two types of kanban jobs:</span></span>

-   <span data-ttu-id="d1a91-111">プロセス</span><span class="sxs-lookup"><span data-stu-id="d1a91-111">Process</span></span>
-   <span data-ttu-id="d1a91-112">転送</span><span class="sxs-lookup"><span data-stu-id="d1a91-112">Transfer</span></span>

<span data-ttu-id="d1a91-113">**プロセス** タイプのジョブのみスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-113">You can schedule only jobs of the **Process** type.</span></span> <span data-ttu-id="d1a91-114">かんばん作業と、活動時間などのプロパティは、生産かんばんフローで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-114">The kanban job and its properties, such as the activity time, are defined in the production kanban flow.</span></span> <span data-ttu-id="d1a91-115">生産かんばんフローでは、作業セルにもかんばん作業が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-115">In the production kanban flow, the kanban job is also assigned to a work cell.</span></span> <span data-ttu-id="d1a91-116">作業セルの 1 日あたりの能力はリソース グループに設定されている作業セルの能力に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-116">The work cell's daily capacity is calculated based on the work cell capacity that is set on the resource group.</span></span> <span data-ttu-id="d1a91-117">これは、関連するカレンダーの毎日の作業時間で調整されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-117">It's adjusted by the daily working time in the related calendar.</span></span> <span data-ttu-id="d1a91-118">かんばん作業をスケジュールすると、作業セルの能力がジョブに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-118">When a kanban job is scheduled, the job loads the capacity of the work cell.</span></span> <span data-ttu-id="d1a91-119">かんばんスケジュール ボードは、次の主な機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-119">The Kanban schedule board provides the following main features:</span></span>

-   <span data-ttu-id="d1a91-120">リーン作業セルでの生産計画のグラフィカルな概要。</span><span class="sxs-lookup"><span data-stu-id="d1a91-120">A graphical overview of the production plan in a lean work cell.</span></span> <span data-ttu-id="d1a91-121">この概要は、定義された期間内に計画されたかんばんプロセス ジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-121">This overview shows the planned kanban process jobs in the defined periods.</span></span>
-   <span data-ttu-id="d1a91-122">予定外のかんばん作業をスケジュールし、以前にスケジュールされたジョブを再スケジューリングできるツール。</span><span class="sxs-lookup"><span data-stu-id="d1a91-122">A tool that lets you schedule unplanned kanban jobs and reschedule previously scheduled jobs.</span></span>

## <a name="kanban-schedule-board"></a><span data-ttu-id="d1a91-123">かんばんスケジュール ボード</span><span class="sxs-lookup"><span data-stu-id="d1a91-123">Kanban schedule board</span></span>
<span data-ttu-id="d1a91-124">**かんばんスケジュール ボード** ページには、次の図に示すように、7 つの主要な要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1a91-124">The **Kanban schedule board** page contains seven main elements, as shown in the following illustration.</span></span> 

![かんばんスケジュール ボード](./media/kanban-schedule-board-1024x554.png)
1.  <span data-ttu-id="d1a91-126">アクション ペイン</span><span class="sxs-lookup"><span data-stu-id="d1a91-126">Action Pane</span></span>
2.  <span data-ttu-id="d1a91-127">フィルター フィールド</span><span class="sxs-lookup"><span data-stu-id="d1a91-127">Filter fields</span></span>
3.  <span data-ttu-id="d1a91-128">予定外のジョブ用ボタン</span><span class="sxs-lookup"><span data-stu-id="d1a91-128">Button for unplanned jobs</span></span>
4.  <span data-ttu-id="d1a91-129">期間ノード</span><span class="sxs-lookup"><span data-stu-id="d1a91-129">Period node</span></span>
5.  <span data-ttu-id="d1a91-130">かんばん作業</span><span class="sxs-lookup"><span data-stu-id="d1a91-130">Kanban job</span></span>
6.  <span data-ttu-id="d1a91-131">能力バー</span><span class="sxs-lookup"><span data-stu-id="d1a91-131">Capacity bar</span></span>
7.  <span data-ttu-id="d1a91-132">タイム スケール</span><span class="sxs-lookup"><span data-stu-id="d1a91-132">Time scale</span></span>

### <a name="view-the-time-scale"></a><span data-ttu-id="d1a91-133">タイム スケールを表示</span><span class="sxs-lookup"><span data-stu-id="d1a91-133">View the time scale</span></span>

<span data-ttu-id="d1a91-134">ボードは、それぞれノード (4) として表される期間に分割されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-134">The board is divided into periods, each of which is represented as a node (4).</span></span> <span data-ttu-id="d1a91-135">期間ノードは垂直軸に表示され、水平方向のアクセスは、期間の長さを示すタイム スケール (7) を表します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-135">The period nodes are listed on the vertical axis, and the horizontal access represents a time scale (7) that shows the length of the period.</span></span> <span data-ttu-id="d1a91-136">期間は、1 日または 1 週間いずれかの長さです。</span><span class="sxs-lookup"><span data-stu-id="d1a91-136">A period has a length of either one day or one week.</span></span> <span data-ttu-id="d1a91-137">期間の長さは、かんばんスケジュール ボード (2) に対して選択された作業セルのコンフィギュレーションによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-137">The period length is determined by the configuration of the work cell that is selected for the Kanban schedule board (2).</span></span> <span data-ttu-id="d1a91-138">各期間ノードに対して、かんばんスケジュール ボードは、スケジュール済かんばん作業がどの程度期間を読み込むかを示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-138">For each period node, the Kanban schedule board indicates how much the scheduled kanban jobs are loading the period.</span></span> <span data-ttu-id="d1a91-139">期間の最大スループットの表示もあります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-139">There is also an indication of the maximum throughput for the period.</span></span> <span data-ttu-id="d1a91-140">スケジュールされたスループットが最大スループットを超える場合、期間は過負荷状態とみなされ、赤い警告記号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-140">If the scheduled throughput exceeds the maximum throughput, the period is considered as overloaded, and a red warning symbol appears.</span></span> <span data-ttu-id="d1a91-141">スケジュール済かんばんジョブは、スケジュール済の開始時刻と終了時刻 (5) を持つ期間に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-141">A scheduled kanban job appears in a period that has scheduled start and end times (5).</span></span> <span data-ttu-id="d1a91-142">ジョブの長さは、活動時間と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-142">The length of the job is equal to the activity time.</span></span> <span data-ttu-id="d1a91-143">かんばん作業は、作業セルのタクト タイムが活動時間を超えた場合、期間に重複として示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-143">Kanban jobs appear as overlapping in a period if their activity times exceed the takt time of the work cell.</span></span>

### <a name="view-job-status"></a><span data-ttu-id="d1a91-144">ジョブ ステータスを表示</span><span class="sxs-lookup"><span data-stu-id="d1a91-144">View job status</span></span>

<span data-ttu-id="d1a91-145">かんばん作業についての詳細は、ジョブの上にポインターを移動すると表示されるツールヒントで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="d1a91-145">More information about a kanban job is available in the tooltip that appears when you hover the pointer over the job.</span></span> <span data-ttu-id="d1a91-146">記号は、ジョブのステータスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-146">A symbol provides information about the status of the job.</span></span> <span data-ttu-id="d1a91-147">たとえば、時計アイコンは、かんばん作業が期限切れであることを示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-147">For example, a clock symbol indicates that the kanban job is overdue.</span></span>

### <a name="use-colors-to-view-the-kanban-schedule-board"></a><span data-ttu-id="d1a91-148">色を使用してかんばんスケジュール ボードを表示</span><span class="sxs-lookup"><span data-stu-id="d1a91-148">Use colors to view the Kanban schedule board</span></span>

<span data-ttu-id="d1a91-149">かんばんスケジュール ボードが提供する概要を機能強化するため、かんばん作業を区別するために色を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-149">To enhance the overview that the Kanban schedule board provides, you can use colors to distinguish kanban jobs.</span></span> <span data-ttu-id="d1a91-150">かんばん作業の色はリーン スケジュール グループで設定され、同じ順序で生産される製品を集計することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-150">The color of a kanban job is configured in the lean schedule group, where you can aggregate the products that should be produced in the same sequence.</span></span> <span data-ttu-id="d1a91-151">アクション ペインの **ボード** タブにある **テーマ カラーを使用する** ボタンを使用して、アプリケーションのテーマ カラーとリーン スケジュール グループで設定された色を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-151">The **Use theme colors** button on the **Board** tab of the Action Pane lets you switch between the application theme colors and the colors that are configured in the lean schedule group.</span></span> <span data-ttu-id="d1a91-152">各期間で、能力バー (6) は、期間に対して利用可能な時間数がかんばん作業にどれほど読み込まれているかを示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-152">For each period, a capacity bar (6) indicates how many of the available hours for the period have been loaded with kanban jobs.</span></span> <span data-ttu-id="d1a91-153">期間が過負荷状態になる場合は、能力バーが太く赤色で表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-153">If the period is overloaded, the capacity bar appears thicker and in red.</span></span> <span data-ttu-id="d1a91-154">これらすべての機能は、**かんばんスケジュール ボード** ページの上部にある、アクション ペイン (1) の **ボード** タブで利用できます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-154">All these functions are available on the **Board** tab of the Action Pane (1) at the top of the **Kanban schedule board** page.</span></span>

## <a name="plan-unplanned-jobs"></a><span data-ttu-id="d1a91-155">予定外のジョブの計画</span><span class="sxs-lookup"><span data-stu-id="d1a91-155">Plan unplanned jobs</span></span>
<span data-ttu-id="d1a91-156">**予定外のジョブの計画** ダイアログ ボックスから、予定外のかんばん作業をスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-156">You can schedule unplanned kanban jobs from the **Plan unplanned jobs** dialog box.</span></span> <span data-ttu-id="d1a91-157">このダイアログ ボックスを開くには、**予定外のジョブ** ボタンをクリックして、予定外のジョブの現在の番号を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-157">To open this dialog box, click the **Unplanned jobs** button that shows the current number of unplanned jobs.</span></span> <span data-ttu-id="d1a91-158">または、アクション ペインの **ボード** タブで **予定外のジョブの計画** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1a91-158">Alternatively, click **Plan unplanned jobs** on the **Board** tab of the Action Pane.</span></span> <span data-ttu-id="d1a91-159">ダイアログ ボックスは、作業セルに対し予定外のかんばん作業の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-159">The dialog box shows a list of the unplanned kanban jobs for the work cell.</span></span> <span data-ttu-id="d1a91-160">**フィルター** フィールドを使用して、グリッド内のすべてのフィールドをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-160">You can use the **Filter** field to filter on all fields in the grid.</span></span> <span data-ttu-id="d1a91-161">たとえば、特定の製品のためにかんばん作業をフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-161">For example, you can filter on kanban jobs for a specific product.</span></span> <span data-ttu-id="d1a91-162">スケジュールしたいジョブのフィルタ処理されたリストができたら、それらのジョブをリストから選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1a91-162">After you have a filtered list of the jobs that you want to schedule, select them in the list, and then click **OK**.</span></span> <span data-ttu-id="d1a91-163">自動計画を使用してジョブをスケジュールするには、**自動計画** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-163">To use automatic planning to schedule the jobs, set the **Automatic planning** option to **Yes**.</span></span> <span data-ttu-id="d1a91-164">この場合、ジョブは期日に従って期間にスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-164">In this case, the jobs are scheduled into a period according to their due date.</span></span> <span data-ttu-id="d1a91-165">期間別にジョブをスケジュールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-165">You can also schedule the jobs by period.</span></span> <span data-ttu-id="d1a91-166">**期間** フィールドで期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-166">Just select a period in the **Period** field.</span></span> <span data-ttu-id="d1a91-167">次の図は、**予定外のジョブの計画** ダイアログ ボックスの例を示します。</span><span class="sxs-lookup"><span data-stu-id="d1a91-167">The following illustration shows an example of the **Plan unplanned jobs** dialog box.</span></span> 

![予定外のジョブの計画ダイアログ ボックス](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a><span data-ttu-id="d1a91-169">同じ期間内でのかんばん作業の順序付け</span><span class="sxs-lookup"><span data-stu-id="d1a91-169">Sequence kanban jobs within the same period</span></span>
<span data-ttu-id="d1a91-170">期間内の 1 つまたは複数の選択したジョブの順序を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-170">You can change the sequence of one or more selected jobs within a period.</span></span> <span data-ttu-id="d1a91-171">この機能は、期間内で一部のジョブに優先順位を設定したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-171">This capability can be useful if you want to prioritize some jobs within the period.</span></span> <span data-ttu-id="d1a91-172">または、ジョブの実行を最適化するために、同じ製品属性を持つジョブを順序付けしたいことがあります。</span><span class="sxs-lookup"><span data-stu-id="d1a91-172">Alternatively, you might want to sequence jobs that have the same product attributes, to optimize job execution.</span></span> <span data-ttu-id="d1a91-173">ドラッグ アンド ドロップ操作で、またはアクション ペインの **ボード** タブの **前** および **次** メニュー項目を使用して、順序を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-173">You can change the sequence through a drag-and-drop operation, or by using the **Backward** and **Forward** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="reassign-kanban-jobs-across-periods"></a><span data-ttu-id="d1a91-174">複数の期間にかんばん作業を再割り当てする</span><span class="sxs-lookup"><span data-stu-id="d1a91-174">Reassign kanban jobs across periods</span></span>
<span data-ttu-id="d1a91-175">ジョブは、1 つの期間から別の期間へ再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-175">Jobs can be reassigned from one period to another.</span></span> <span data-ttu-id="d1a91-176">この機能は、期間が過負荷状態になり、余裕がある期間へ負荷をレベルしたい場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-176">This capability can be useful if a period is overloaded and you want to level the load to periods that have spare capacity.</span></span> <span data-ttu-id="d1a91-177">ドラッグ アンド ドロップ操作で、またはアクション ペインの **ボード** タブの **次の期間** および **前の期間** メニュー項目を使用して、再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-177">You can reassign jobs through a drag-and-drop operation, or by using the **Next period** and **Previous period** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="open-the-kanban-schedule-board"></a><span data-ttu-id="d1a91-178">かんばんスケジュール ボードを開く</span><span class="sxs-lookup"><span data-stu-id="d1a91-178">Open the Kanban schedule board</span></span>
<span data-ttu-id="d1a91-179">次のページのメニュー項目を使用して、かんばんスケジュール ボードを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d1a91-179">You can open the Kanban schedule board by using the menu item on the following pages:</span></span>

-   <span data-ttu-id="d1a91-180">**生産領域** ページ</span><span class="sxs-lookup"><span data-stu-id="d1a91-180">**Production area** page</span></span>
-   <span data-ttu-id="d1a91-181">**かんばん作業のスケジューリング** ページ</span><span class="sxs-lookup"><span data-stu-id="d1a91-181">**Kanban jobs scheduling** page</span></span>
-   <span data-ttu-id="d1a91-182">**生産フローの視覚化** ページ</span><span class="sxs-lookup"><span data-stu-id="d1a91-182">**Production flow visualization** page</span></span>


<a name="additional-resources"></a><span data-ttu-id="d1a91-183">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d1a91-183">Additional resources</span></span>
--------

[<span data-ttu-id="d1a91-184">リーン生産のかんばん作業のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="d1a91-184">Kanban job scheduling for lean manufacturing</span></span>](lean-manufacturing-kanban-job-scheduling.md)

