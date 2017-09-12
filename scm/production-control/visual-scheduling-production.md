---
title: "ジョブ スケジュールのガント チャート"
description: "ガント チャートは、生産のスケジューリング者を生産計画の制御および最適化のためにサポートするよう設計されています。 ガント チャートは、工程の流れを透明化し、材料またはリソースの不足を考慮しながら、生産スケジュールを調整しやすくします。 これにより、スケジューリング者の使用可能なリソースを最大限活用し、進行中の作業の最小化、および製造オーダーのスループットの時間を最適化できます。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: "JmgShopSupervisorWorkspace、ProdTable、ProdTableListPage"
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 71c95adbfe48c313bb0bfb23ada2cb69433bf0e1
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="gantt-chart-for-job-scheduling"></a><span data-ttu-id="43d79-106">ジョブ スケジュールのガント チャート</span><span class="sxs-lookup"><span data-stu-id="43d79-106">Gantt chart for job scheduling</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="43d79-107">ガント チャートは、生産のスケジューリング者を生産計画の制御および最適化のためにサポートするよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="43d79-107">The Gantt chart is designed to empower production planners to control and optimize the production plan.</span></span> <span data-ttu-id="43d79-108">ガント チャートは、工程の流れを透明化し、材料またはリソースの不足を考慮しながら、生産スケジュールを調整しやすくします。</span><span class="sxs-lookup"><span data-stu-id="43d79-108">The Gantt chart makes the flow of operations transparent and makes it easy to adjust the production schedule while taking into account material or resource shortages.</span></span> <span data-ttu-id="43d79-109">これにより、スケジューリング者の使用可能なリソースを最大限活用し、進行中の作業の最小化、および製造オーダーのスループットの時間を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-109">This helps planners make the best use of available resources, minimize work in progress, and optimize throughput times for production orders.</span></span>

<span data-ttu-id="43d79-110">ガント チャートは、生産のスケジューリング者を生産計画の制御および最適化のためにサポートするよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="43d79-110">The Gantt chart is designed to empower production planners to control and optimize the production plan.</span></span> <span data-ttu-id="43d79-111">ガント チャートは、工程の流れを透明化し、材料またはリソースの不足を考慮しながら、生産スケジュールを調整しやすくします。</span><span class="sxs-lookup"><span data-stu-id="43d79-111">The Gantt chart makes the flow of operations transparent and makes it easy to adjust the production schedule while taking into account material or resource shortages.</span></span> <span data-ttu-id="43d79-112">これにより、スケジューリング者の使用可能なリソースを最大限活用し、進行中の作業の最小化、および製造オーダーのスループットの時間を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-112">This helps planners make the best use of available resources, minimize work in progress, and optimize throughput times for production orders.</span></span>

<span data-ttu-id="43d79-113">ガント チャートは、定義された期間内でスケジュールされている活動の視覚表現です。</span><span class="sxs-lookup"><span data-stu-id="43d79-113">A Gantt chart is a visual representation of scheduled activities within a defined time interval.</span></span> <span data-ttu-id="43d79-114">活動は、能力カレンダーで定義されている能力を持つリソースにスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="43d79-114">The activities are scheduled on resources that have capacity defined by a capacity calendar.</span></span> <span data-ttu-id="43d79-115">ガント チャートには、次のタイプの活動を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-115">The following types of activities can be shown in the Gantt chart.</span></span>

-   <span data-ttu-id="43d79-116">ジョブ スケジュールに設定された製造オーダーからのジョブ。</span><span class="sxs-lookup"><span data-stu-id="43d79-116">Jobs from production orders that are job scheduled.</span></span>
-   <span data-ttu-id="43d79-117">計画製造オーダーからのジョブ。</span><span class="sxs-lookup"><span data-stu-id="43d79-117">Jobs from planned production orders.</span></span>
-   <span data-ttu-id="43d79-118">時間予測タイプのジョブ スケジューリング済のプロジェクト活動。</span><span class="sxs-lookup"><span data-stu-id="43d79-118">Job scheduled project activities of type Hour forecasts.</span></span>

<span data-ttu-id="43d79-119">ガント チャートは、**注文の表示** および **リソース ビュー**[の 2 つの異なるビューで開くことができます。](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true) **注文の表示** では、活動は製造オーダーの下にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-119">The Gantt chart can be opened in two different views, **Order view** and **Resource view**[.](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true)In **Order view**, activities are grouped under production orders.</span></span> <span data-ttu-id="43d79-120">これは、たとえば、同じ注文に属するすべてのジョブの概要を管理したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="43d79-120">This can be useful, for example, if you want to maintain an overview of all the jobs belonging to the same orders.</span></span> <span data-ttu-id="43d79-121">**リソース ビュー** では、すべてのジョブが個々のリソースの下にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-121">In **Resource view** all jobs are grouped under individual resources.</span></span> <span data-ttu-id="43d79-122">たとえば、機械や機械のグループなど、リソース レベルでの計画の最適化を行う場合、このビューは役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="43d79-122">This view can be useful when optimizing the plan at a resource level, for example, a machine or a group of machines.</span></span> <span data-ttu-id="43d79-123">次に示す図で、ガント チャートは次の主要な要素とともに **注文の表示** および **リソース ビュー** を表示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-123">The Gantt charts shown in the illustrations below show **Order view** and **Resource view** with these key elements:</span></span>

1.  <span data-ttu-id="43d79-124">ガント チャートの活動</span><span class="sxs-lookup"><span data-stu-id="43d79-124">Gantt chart activity</span></span>
2.  <span data-ttu-id="43d79-125">材料不足アイコン</span><span class="sxs-lookup"><span data-stu-id="43d79-125">Material shortage icon</span></span>
3.  <span data-ttu-id="43d79-126">材料の使用可能性アイコン</span><span class="sxs-lookup"><span data-stu-id="43d79-126">Material availability icon</span></span>
4.  <span data-ttu-id="43d79-127">注文発送日アイコン</span><span class="sxs-lookup"><span data-stu-id="43d79-127">Order delivery date icon</span></span>
5.  <span data-ttu-id="43d79-128">能力バー</span><span class="sxs-lookup"><span data-stu-id="43d79-128">Capacity bar</span></span>

## <a name="order-view"></a><span data-ttu-id="43d79-129">注文の表示</span><span class="sxs-lookup"><span data-stu-id="43d79-129">Order view</span></span>

<span data-ttu-id="43d79-130">[![オーダー ビュー](./media/orderview.png)](./media/orderview.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-130">[![orderview](./media/orderview.png)](./media/orderview.png)</span></span>

## <a name="resource-view"></a><span data-ttu-id="43d79-131">リソース ビュー</span><span class="sxs-lookup"><span data-stu-id="43d79-131">Resource view</span></span>
<span data-ttu-id="43d79-132">[![リソース ビュー](./media/resview.png)](./media/resview.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-132">[![resview](./media/resview.png)](./media/resview.png)</span></span>

## <a name="activities"></a><span data-ttu-id="43d79-133">活動</span><span class="sxs-lookup"><span data-stu-id="43d79-133">Activities</span></span>
<span data-ttu-id="43d79-134">活動はバーとして表示され、予定された開始時刻および終了時刻とともにタイム スケール グリッドで整理され、バーの長さは活動を完了させるのに必要な時間に比例します。</span><span class="sxs-lookup"><span data-stu-id="43d79-134">The activities appear as bars and are organized in a time scale grid with a scheduled start and end time, making the length of the bars proportional to the time that is necessary to complete the activity.</span></span> <span data-ttu-id="43d79-135">活動はタイム スケールに従って表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-135">The activities are shown according to a time scale.</span></span> <span data-ttu-id="43d79-136">開始日と終了日、および、時間または日数などの時間単位を選択するメニューから、タイム スケールを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-136">You can adjust the time scale on the menu where you select a start and end date and a time unit, for example, hours or days.</span></span> <span data-ttu-id="43d79-137">タイム スケールを調整することによって、活動を管理したい時間間隔にフォーカスできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-137">By adjusting the time scale you can set focus on a time interval in which you want to manage activities.</span></span> 

<span data-ttu-id="43d79-138">概要を分かりやすくするため、活動の色を制御するためのさまざまなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="43d79-138">To get a better overview, there are different options for controlling the color of the activities.</span></span> <span data-ttu-id="43d79-139">活動ごとに個別の色が設定でき、アプリケーションに使用される一般配色テーマのテーマ色を使用したり、製造オーダーの色コードに基づいて制御される色を設定できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-139">You can configure an individual color for activities, use the theme color that is the general color theme used for the application, or set up the color to be controlled by the color code for production orders.</span></span> 

<span data-ttu-id="43d79-140">活動の時間間隔は背景シェードで表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-140">The time interval for activities has a background shade.</span></span> <span data-ttu-id="43d79-141">白いシェードの期間は、活動のためのリソースに基づく定義された能力を持つ時間間隔を示し、グレー シェードの期間は定義されていない能力を持つ時間間隔を示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-141">Periods with a white shade indicate a time interval with defined capacity on the resource for the activity, whereas periods with a grey shade indicate time intervals with no capacity defined.</span></span> 

<span data-ttu-id="43d79-142">チャートの左側には、活動が予定されているリソースと製造オーダー番号など、活動についての追加情報があります。</span><span class="sxs-lookup"><span data-stu-id="43d79-142">On the left side of the chart there is additional information about the activity, for example, the resource on which the activity is scheduled and production order number.</span></span> <span data-ttu-id="43d79-143">同じ注文に属するジョブ間の関係は矢印で表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-143">The connection between jobs belonging to the same order is shown with an arrow.</span></span> 

<span data-ttu-id="43d79-144">活動に関する詳細情報は、活動ダイアログ ボックスで入手できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-144">You can get more information about an activity in the activity dialog box.</span></span> <span data-ttu-id="43d79-145">ダイアログ ボックスを開くには、活動をダブルクリックするか、**情報** メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="43d79-145">To open the dialog box, double-click the activity or select the **information** menu.</span></span> <span data-ttu-id="43d79-146">活動のダイアログでは、スケジュールされた開始日と終了日、およびどの材料が活動に使用されるかに関する時間情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-146">In the activity dialog you can see the scheduled start and end date, and time information about which materials the activity is planned to consume.</span></span> 

<span data-ttu-id="43d79-147">活動は、グループ化レベルでグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-147">The activities can be grouped in Grouping levels.</span></span> <span data-ttu-id="43d79-148">グループ化レベルは階層的で、活動の論理グループ構成のために使用できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-148">The Grouping levels are hierarchical and can be used to make a logical grouping of activities.</span></span> <span data-ttu-id="43d79-149">たとえば、製造活動がサイト、生産単位、リソース グループ、およびリソース別にグループ化されたレイアウトがある場合、そのレイアウトに従って活動をグループ化するグループ化レベルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-149">For example, if you have a layout where manufacturing activities are grouped by Site, Production units, Resource groups, and Resources, you can use the Grouping levels to group the activities according to that layout.</span></span> <span data-ttu-id="43d79-150">グループ化レベルは、メニューの **すべて展開** および **すべて折りたたむ** ボタンで、個別のグループ化レベルまたはチャート内のすべてのレベルを展開し折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-150">The grouping levels can be expanded and collapsed either on the individual grouping level or for all levels in the chart by using the **Expand all** and **Collapse all** buttons on the menu.</span></span> <span data-ttu-id="43d79-151">チャートを開いたとき展開または折りたたむようにグループ化レベルを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-151">You can also configure the grouping levels to be expanded or collapsed when the chart is opened.</span></span>

### <a name="material-availability"></a><span data-ttu-id="43d79-152">材料の使用可能性</span><span class="sxs-lookup"><span data-stu-id="43d79-152">Material availability</span></span>

<span data-ttu-id="43d79-153">ガント チャートでは、スケジューリング者に個々の活動の材料のステータスに関する詳細な情報を提供するよう設定できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-153">The Gantt chart can be set up to provide the planner with detailed information about material status for the individual activities.</span></span> <span data-ttu-id="43d79-154">これはたとえば、材料が遅延し生産計画に影響を与える場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="43d79-154">For example, this can be helpful if material is delayed and is affecting the production plan.</span></span> <span data-ttu-id="43d79-155">この場合、スケジューリング者が影響を理解し、必要な調整を行うために、材料の問題がガント チャートで強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-155">In this case, the material issues will be highlighted in the Gantt chart to help the planner to understand consequences and make necessary adjustments.</span></span> 

<span data-ttu-id="43d79-156">ジョブのスケジュール開始日が、ジョブによって消費される材料の使用可能日より後の場合には、ジョブが材料不足アイコンとともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-156">A job will appear with a material shortage icon if the schedule start date of the job is later than the material availability date for materials consumed by the job.</span></span> <span data-ttu-id="43d79-157">使用可能日は、動的マスター プランのペギング情報に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-157">The material availability date is calculated based on the pegging information in the dynamic master plan.</span></span> <span data-ttu-id="43d79-158">材料不足アイコンは、ジョブの予定開始日以降に受入のある発注書に対して固定された材料を消費しているジョブなどに表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-158">The material shortage icon will for example appear on a job that is consuming a material that is pegged against a purchase order that has a receipt that is later than the planned start date of the job.</span></span>

### <a name="indicator-of-material-availability-date"></a><span data-ttu-id="43d79-159">材料使用可能日のインジケータ</span><span class="sxs-lookup"><span data-stu-id="43d79-159">Indicator of material availability date</span></span>

<span data-ttu-id="43d79-160">ジョブの材料不足を表示するようチャートを設定した場合、ジョブの材料使用可能日を示すアイコンも表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-160">When you set up the chart to show jobs with material shortages an icon for showing the material availability date for the job can also be shown.</span></span> <span data-ttu-id="43d79-161">アイコンは、材料使用可能日がチャートの定義済の時間間隔内であるときのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-161">The icon will only be shown if the material availability date is within the defined time interval of the chart.</span></span> <span data-ttu-id="43d79-162">材料使用可能日が定義された時間間隔外に存在する場合、ジョブのダイアログ ボックスにある材料のリストから、材料の使用可能性に関するより詳細な情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-162">If the material availability date lies outside the defined time interval, then more detailed material availability information can be retrieved from the material list in the job dialog box.</span></span> <span data-ttu-id="43d79-163">一覧には、ジョブに対して材料が遅延していることを示すアイコンもあります。</span><span class="sxs-lookup"><span data-stu-id="43d79-163">In the list there is also an icon showing late materials for the job.</span></span> <span data-ttu-id="43d79-164">材料使用可能日を開始日として使用して、ジョブを再スケジューリングすることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-164">You can reschedule a job using the material availability date as a start date.</span></span>

### <a name="indicator-of-order-delivery-date"></a><span data-ttu-id="43d79-165">注文出荷日のインジケータ</span><span class="sxs-lookup"><span data-stu-id="43d79-165">Indicator of order delivery date</span></span>

<span data-ttu-id="43d79-166">このアイコンは、製造オーダーの出荷日を示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-166">This icon indicates the delivery date for a production order.</span></span> <span data-ttu-id="43d79-167">アイコンは、注文の表示にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-167">The icon is only visible in the Order view.</span></span>

### <a name="capacity-bar"></a><span data-ttu-id="43d79-168">能力バー</span><span class="sxs-lookup"><span data-stu-id="43d79-168">Capacity bar</span></span>

<span data-ttu-id="43d79-169">チャートにリソースの能力バーを表示するよう設定することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-169">You can configure the chart to show a resource capacity bar.</span></span> <span data-ttu-id="43d79-170">このバーは、チャートの定義済の時間間隔における活動のための、リソース能力の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-170">This bar provides an overview of the resource capacity for an activity in the defined time interval of the chart.</span></span> <span data-ttu-id="43d79-171">リソースが予約されていない期間については、能力バーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="43d79-171">The capacity bar is not shown for periods of the time where the resource is not booked.</span></span> <span data-ttu-id="43d79-172">リソースが能力に予約されている期間は、能力バーが実線で表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-172">In periods where the resource is booked to capacity, the capacity bar is shown as a solid bar.</span></span> <span data-ttu-id="43d79-173">リソースが予約を超過している期間は、バーが太く赤色で表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-173">In periods where the resource is overbooked, the bar will appear thicker and in a red color.</span></span> <span data-ttu-id="43d79-174">たとえば、2 つのジョブが重複する場合、能力バーは重複が存在する時間間隔が予約超過していることを示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-174">For example, if two jobs overlap, the capacity bar will indicate an overbooking in the time interval where there is an overlap.</span></span> <span data-ttu-id="43d79-175">ジョブをスケジューリングすると、能力バーは動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-175">The capacity bar is updated dynamically when you schedule a job.</span></span> <span data-ttu-id="43d79-176">**能力バーの表示** メニューで能力バーを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-176">You enable the capacity bar on the **Show capacity bar** menu.</span></span> <span data-ttu-id="43d79-177">**リソース ビュー** にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-177">It can only be shown in **Resource view**.</span></span> <span data-ttu-id="43d79-178">リソースの最大能力負荷についての詳細を取得したい場合は、メニューまたは選択した活動のコンテキスト メニューから開くことができる **最大能力負荷** チャートを使用します。</span><span class="sxs-lookup"><span data-stu-id="43d79-178">If you want to get a more detailed view of the capacity load on a resource, use the **Capacity load** chart, which can be opened from the menu or the context menu for a selected activity.</span></span>

## <a name="job-scheduling-in-the-gantt-chart"></a><span data-ttu-id="43d79-179">ガント チャートでのジョブのスケジューリング</span><span class="sxs-lookup"><span data-stu-id="43d79-179">Job scheduling in the Gantt chart</span></span>
<span data-ttu-id="43d79-180">ガント チャートには、生産計画を調整するためのさまざまなオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="43d79-180">The Gantt chart offers different options for making adjustments to the production plan.</span></span> <span data-ttu-id="43d79-181">ガント チャートでは、ドラッグ アンド ドロップ操作で、またはスケジュール メニューから、活動を再スケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-181">In the Gantt chart, you can re-schedule activities as a drag-and-drop interaction or from a schedule menu.</span></span> <span data-ttu-id="43d79-182">計画プロセスでは、リソース能力、リソースの機能、および材料の制約を考慮に入れることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-182">In the planning process, you can take resource capacity, resource capabilities, and material constraints into account.</span></span>

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a><span data-ttu-id="43d79-183">ドラッグ アンド ドロップ操作でジョブをスケジューリング</span><span class="sxs-lookup"><span data-stu-id="43d79-183">Schedule a job as a drag-and-drop interaction</span></span>

<span data-ttu-id="43d79-184">ドラッグ アンド ドロップ操作で、定義された期間内でジョブを再スケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-184">You can re-schedule job within the defined time interval as a drag-and-drop interaction.</span></span> <span data-ttu-id="43d79-185">同じリソースのジョブのみが再スケジュールでき、一度にスケジュールすることができるジョブは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="43d79-185">You can only re-schedule the job on the same resource, and you can only schedule one job at a time.</span></span>

### <a name="schedule-a-job-from-the-menu"></a><span data-ttu-id="43d79-186">メニューからジョブをスケジューリングする</span><span class="sxs-lookup"><span data-stu-id="43d79-186">Schedule a job from the menu</span></span>

<span data-ttu-id="43d79-187">**ジョブのスケジュール設定** メニューで、スケジューリング指示とスケジューリング日時に基づき、チャート内の 1 つ以上の選択したジョブをスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-187">On the **Schedule jobs** menu, you can schedule one or more selected job in the chart based on a scheduling direction and a scheduling date time.</span></span> <span data-ttu-id="43d79-188">使用可能なスケジューリング指示は 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="43d79-188">There are three available schedule directions.</span></span>

-   <span data-ttu-id="43d79-189">スケジューリングの日付からフォワード</span><span class="sxs-lookup"><span data-stu-id="43d79-189">Forward from scheduling date</span></span>
-   <span data-ttu-id="43d79-190">スケジューリングの日付からバックワード</span><span class="sxs-lookup"><span data-stu-id="43d79-190">Backward from scheduling date</span></span>
-   <span data-ttu-id="43d79-191">材料の使用可能日以降</span><span class="sxs-lookup"><span data-stu-id="43d79-191">Forward from material availability date</span></span>

<span data-ttu-id="43d79-192">ガント チャートの定義された期間外にジョブをスケジューリングすることはできません。</span><span class="sxs-lookup"><span data-stu-id="43d79-192">It is not possible to schedule a job outside the defined time interval of the Gantt chart.</span></span> <span data-ttu-id="43d79-193">これを行った場合は、ジョブが未スケジュールのままになり、「読み込まれた期間内にジョブをスケジュールできませんでした。」というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-193">If you do that, the job will be left unscheduled and you will receive the error message, "Could not schedule the job within the loaded time period."</span></span>

### <a name="schedule-previous-jobs"></a><span data-ttu-id="43d79-194">前のジョブのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="43d79-194">Schedule previous jobs</span></span>

<span data-ttu-id="43d79-195">同じ製造オーダーに所属するジョブなどの活動のネットワーク内で、**前のジョブのスケジュール設定** 機能を使用して、ネットワーク内で選択したジョブに関連する前のジョブをスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-195">In a network of activities, such as jobs belonging to the same production order, you can use the **Schedule previous jobs** function to schedule the previous jobs relative to a selected job in the network.</span></span> <span data-ttu-id="43d79-196">次の例では、強調表示された活動が選択したジョブです。</span><span class="sxs-lookup"><span data-stu-id="43d79-196">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="43d79-197">以前</span><span class="sxs-lookup"><span data-stu-id="43d79-197">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/schprevjob3.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="43d79-198">変更後</span><span class="sxs-lookup"><span data-stu-id="43d79-198">After</span></span>
</td>
</tr>
</table>

### <a name="schedule-next-jobs"></a><span data-ttu-id="43d79-199">次のジョブのスケジュール設定</span><span class="sxs-lookup"><span data-stu-id="43d79-199">Schedule next jobs</span></span>

<span data-ttu-id="43d79-200">**次のジョブのスケジュール設定** 機能を使用して、活動のネットワーク内で選択したジョブに関連する次のジョブをスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-200">You can use the **Schedule next jobs** function to schedule the next jobs relative to a selected job in a network of activities.</span></span> <span data-ttu-id="43d79-201">次の例では、強調表示された活動が選択したジョブです。</span><span class="sxs-lookup"><span data-stu-id="43d79-201">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="43d79-202">以前</span><span class="sxs-lookup"><span data-stu-id="43d79-202">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/schnxtjob.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="43d79-203">変更後</span><span class="sxs-lookup"><span data-stu-id="43d79-203">After</span></span>
</td>
</tr>
</table>

### <a name="schedule-around-job"></a><span data-ttu-id="43d79-204">ジョブに関するスケジュール</span><span class="sxs-lookup"><span data-stu-id="43d79-204">Schedule around job</span></span>

<span data-ttu-id="43d79-205">**ジョブに関するスケジュール** 機能を使用して、活動のネットワーク内で選択したジョブに関連する次のジョブと前のジョブをスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-205">You can use the **Schedule around job** function to schedule the next job and the previous job relative to a selected job in a network of activities.</span></span> <span data-ttu-id="43d79-206">次の例では、強調表示された活動が選択したジョブです。</span><span class="sxs-lookup"><span data-stu-id="43d79-206">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="43d79-207">以前</span><span class="sxs-lookup"><span data-stu-id="43d79-207">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/scharoundjob1.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="43d79-208">変更後</span><span class="sxs-lookup"><span data-stu-id="43d79-208">After</span></span>
</td>
</tr>
</table>

### <a name="arrange-jobs"></a><span data-ttu-id="43d79-209">ジョブの調整</span><span class="sxs-lookup"><span data-stu-id="43d79-209">Arrange jobs</span></span>

<span data-ttu-id="43d79-210">**調整** 機能を使用して、同じリソースで選択した活動を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-210">You can use the **Arrange** function to arrange selected activities on the same resource.</span></span> <span data-ttu-id="43d79-211">これらの活動は活動の同じネットワーク内にありますが、別のネットワークに属していることも可能です。</span><span class="sxs-lookup"><span data-stu-id="43d79-211">These activities can be in the same network of activities, but can also belong to different networks.</span></span> <span data-ttu-id="43d79-212">調整機能を使用すると、選択した活動間の時間のギャップが削除されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-212">When you use the arrange function the time gaps between the selected activities will be eliminated.</span></span> <span data-ttu-id="43d79-213">この機能を使用して、リソースの能力利用を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-213">You can use this function to optimize the capacity utilization of the resources.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="43d79-214">以前</span><span class="sxs-lookup"><span data-stu-id="43d79-214">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/arrangejobs1.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="43d79-215">変更後</span><span class="sxs-lookup"><span data-stu-id="43d79-215">After</span></span>
</td>
</tr>
</table>

### <a name="reassign-activities-from-one-resource-to-another"></a><span data-ttu-id="43d79-216">活動を 1 つのリソースから別のリソースに再割り当てする</span><span class="sxs-lookup"><span data-stu-id="43d79-216">Reassign activities from one resource to another</span></span>

<span data-ttu-id="43d79-217">ジョブを 1 つのリソースから別のリソースに再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-217">You can reassign a job from one resource to another.</span></span> <span data-ttu-id="43d79-218">これは、機械が故障または予約超過しており、ジョブを実行できる他の使用可能リソースを検索する必要があるような状況で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="43d79-218">This can be useful in situations where a machine is out of order or overbooked, and you need to find another available resource that can do the job.</span></span>

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a><span data-ttu-id="43d79-219">ドラッグ アンド ドロップ操作で活動を再割り当てする</span><span class="sxs-lookup"><span data-stu-id="43d79-219">Reassigning an activity as a drag-and-drop interaction</span></span>

<span data-ttu-id="43d79-220">**リソース** ビューで、ガント チャートの別のリソースにドラッグ アンド ドロップ操作で活動を再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-220">In the **Resource** view, you can reassign an activity to a different resource in the Gantt chart as a drag-and-drop interaction.</span></span> <span data-ttu-id="43d79-221">活動がスケジューリングされている行を選択して操作を行います。</span><span class="sxs-lookup"><span data-stu-id="43d79-221">You do that by selecting the row in which the activity is scheduled.</span></span> <span data-ttu-id="43d79-222">行を選択した後、別のリソースのグループ化レベルの下にグループ化されたチャート内のリソースに、行をドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-222">After the row is selected you can drag the row to the resource in the chart grouped under a different resource grouping level.</span></span>

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a><span data-ttu-id="43d79-223">ジョブのスケジュール設定メニューから活動を再割り当てする</span><span class="sxs-lookup"><span data-stu-id="43d79-223">Reassigning an activity from the Schedule jobs menu</span></span>

<span data-ttu-id="43d79-224">**ジョブのスケジュール** メニューから開かれた **ジョブのスケジュール** ダイアログ ボックスから、ジョブを再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-224">You can reassign a job from the **Schedule job** dialog box opened from the **Schedule job** menu.</span></span> <span data-ttu-id="43d79-225">このメニューからは、既にガント チャートに読み込まれているリソースにのみジョブを再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-225">From this menu you can only reassign a job to a resource that is already loaded to the Gantt chart.</span></span> <span data-ttu-id="43d79-226">1 つのジョブのみを選択した場合、リソースのドロップダウンは、適用可能なリソース別に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="43d79-226">If you only select one job, then the drop down for the resource will be sorted by applicable resources.</span></span> <span data-ttu-id="43d79-227">さらにジョブを選択した場合、リソース リストからの適用可能なリソースに関する情報は表示されません。</span><span class="sxs-lookup"><span data-stu-id="43d79-227">If you select more jobs, then there will be no information about applicable resources from the resource list.</span></span>

## <a name="load-additional-resources-to-the-gantt-chart"></a><span data-ttu-id="43d79-228">ガント チャートにその他のリソースを読み込む</span><span class="sxs-lookup"><span data-stu-id="43d79-228">Load additional resources to the Gantt chart</span></span>
<span data-ttu-id="43d79-229">**リソース ビュー** では、ガント チャートにその他のリソースを読み込むためのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="43d79-229">In the **Resource view**, you have an option to load additional resources to the Gantt chart.</span></span> <span data-ttu-id="43d79-230">これは、予約超過または故障した機械にスケジュールされているジョブの代替リソースを検索したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="43d79-230">This can be useful if you want to find an alternative resource for a job that is scheduled on a machine that is overbooked or broken down.</span></span> <span data-ttu-id="43d79-231">**追加のリソースを読み込み** ページで、リストを開いた日付の時点で日付が有効なリソースの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-231">On the **Load additional resources** page, you will get a list of resources that are date efficient as of the date the list is opened.</span></span> <span data-ttu-id="43d79-232">ガント チャートで選択したジョブに関連する、適用可能なリソースが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-232">Applicable resources, relative to a selected job in the Gantt chart, will be listed first.</span></span> <span data-ttu-id="43d79-233">リストを開く前にジョブが複数選択されている場合は、適用可能なリソースは表示されません。</span><span class="sxs-lookup"><span data-stu-id="43d79-233">If you have multiple jobs selected, prior to opening the list, no indication of applicable resources will be shown.</span></span> <span data-ttu-id="43d79-234">**その他のリソースの読み込み** ページで、選択内容を確定するときガント チャートに読み込まれる、1 つ以上のリソースを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-234">On the **Load additional resources** page, you can select one or more resources, that will be loaded to the Gantt chart when you confirm your selection.</span></span> <span data-ttu-id="43d79-235">ガント チャートの期間内の、選択されているリソースにスケジュールされたジョブが何もない場合、リソースはガント チャートの活動一覧の最後にある、リソースのグループ化レベルの下に配置されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-235">If there are no jobs scheduled on the selected resource in the time interval of the Gantt chart, then the resource will be placed under a resource grouping level in the bottom of the list of activities in the Gantt chart.</span></span>

### <a name="access-the-gantt-chart"></a><span data-ttu-id="43d79-236">ガント チャートにアクセスする</span><span class="sxs-lookup"><span data-stu-id="43d79-236">Access the Gantt chart</span></span>

<span data-ttu-id="43d79-237">ガント チャートは、次のページから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-237">The Gantt chart can be opened from the following pages.</span></span>

| <span data-ttu-id="43d79-238">**ページ**</span><span class="sxs-lookup"><span data-stu-id="43d79-238">**Page**</span></span>                                                                                     | <span data-ttu-id="43d79-239">**説明**</span><span class="sxs-lookup"><span data-stu-id="43d79-239">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d79-240">**製造オーダー リストと詳細**</span><span class="sxs-lookup"><span data-stu-id="43d79-240">**Production order list and detail**</span></span>                                                         | <span data-ttu-id="43d79-241">**製造オーダー リストと詳細** ページで、1 つ以上の選択した注文からガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-241">On the **Production order list and detail** page, you can open the Gantt chart from one or more selected orders.</span></span> <span data-ttu-id="43d79-242">**ガント チャート** メニュー項目からチャートを開くと、選択した製造オーダーに関連するすべてのジョブだけでなく、同じリソースにスケジュールされている他の製造オーダーからのジョブも読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43d79-242">Opening the chart from the **Gantt chart** menu item will load all jobs related to the selected production orders, but also jobs from other production orders that are scheduled on the same resources.</span></span> <span data-ttu-id="43d79-243">**ガント チャート - 高速ビュー** メニュー項目からチャートを開くと、選択した製造オーダーに関連するジョブのみが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43d79-243">Opening the chart from the **Gantt chart – Fast view** menu item will only load jobs related to the selected production orders.</span></span> <span data-ttu-id="43d79-244">このビューでは、ジョブをスケジューリングすることはできません。</span><span class="sxs-lookup"><span data-stu-id="43d79-244">In this view, it is not possible to schedule jobs.</span></span> |
| <span data-ttu-id="43d79-245">**リソース**</span><span class="sxs-lookup"><span data-stu-id="43d79-245">**Resource**</span></span>                                                                                 | <span data-ttu-id="43d79-246">**リソース** ページで、メニュー項目 **ガント チャート** からガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-246">On the **Resource** page, you can open the Gantt chart from the menu item **Gantt chart**.</span></span> <span data-ttu-id="43d79-247">選択すると、選択された期間内にリソースにスケジュールされているすべてのジョブがチャートに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43d79-247">When selected, all the jobs scheduled on the resource in a selected time interval will be loaded to the chart.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="43d79-248">**リソース グループ**</span><span class="sxs-lookup"><span data-stu-id="43d79-248">**Resource group**</span></span>                                                                           | <span data-ttu-id="43d79-249">**リソース グループ** ページで、メニュー項目 **ガント** チャートからガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-249">On the **Resource group** page, you can open the Gantt chart from the menu item **Gantt** chart.</span></span> <span data-ttu-id="43d79-250">選択すると、リソース グループのリソースにスケジュールされているすべてのジョブが選択された期間内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-250">When selected, all the jobs scheduled on the resources in the resource group will be shown in a selected time interval.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="43d79-251">**ガント チャート**</span><span class="sxs-lookup"><span data-stu-id="43d79-251">**Gantt charts**</span></span>                                                                             | <span data-ttu-id="43d79-252">**ガント チャート** ページでは、リソースおよびリソース グループごとにガント チャートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="43d79-252">On the **Gantt charts** page you can configure Gantt charts by resources and resource groups.</span></span> <span data-ttu-id="43d79-253">たとえば、特定のリソース セットまたはリソース グループの生産活動を制御したい場合、**ガント チャート** ページでこれらの個別の設定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-253">For example, if you want to control production activities for specific sets of resources or resource groups, then you can make individual configurations of those on the **Gantt charts** page.</span></span> <span data-ttu-id="43d79-254">各設定からガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-254">You can then open the Gantt chart from each configuration.</span></span>                                                                                                                                                    |
| <span data-ttu-id="43d79-255">**時間予測** (プロジェクト)</span><span class="sxs-lookup"><span data-stu-id="43d79-255">**Hour forecasts** (project)</span></span>                                                                 | <span data-ttu-id="43d79-256">**時間予測** タイプのプロジェクト活動をリソースにジョブ スケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="43d79-256">Project activities of type **Hour forecast** can be job scheduled on resources.</span></span> <span data-ttu-id="43d79-257">**スケジューリング** メニューの **時間予測** ページで、ジョブ スケジューリングされた時間予測タイプのプロジェクト活動を確認するため、オーダーのガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-257">On the **Hour forecast** page on the **Scheduling** menu you can open the Gantt chart on a order to see job scheduled project activities of type hour forecast.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="43d79-258">**完了するジョブ** (**生産フロアの管理** ワークスペースに表示)</span><span class="sxs-lookup"><span data-stu-id="43d79-258">**Job to complete** (List in **Production floor management** workspace)</span></span>                      | <span data-ttu-id="43d79-259">**生産フロアの管理で表示される完了するジョブ** ワークスペースは、ワークスペース用に選択されたリソースで進行中の、製造オーダーおよびバッチ オーダーからのジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="43d79-259">The **Jobs to complete list in the Production floor management** workspace shows jobs from production and batch orders that are in progress on the selected resources for the workspace.</span></span> <span data-ttu-id="43d79-260">**ガント チャート** メニュー項目でガント チャートを開くことができ、一覧で選択されたすべてのジョブがチャートに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="43d79-260">On the **Gantt chart** menu item you can open the Gantt chart, where all the jobs selected in the list will be loaded to the chart.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="43d79-261">**リリースする製造オーダー** (**生産フロアの管理** ワークスペースから開く)</span><span class="sxs-lookup"><span data-stu-id="43d79-261">**Production orders to release** (Opened from the **Production floor management** workspace)</span></span> | <span data-ttu-id="43d79-262">リリースする製造オーダー ページは、**生産フロアの管理** ワークスペースから開きます。</span><span class="sxs-lookup"><span data-stu-id="43d79-262">The production orders to release page is opened from the **Production floor management** workspace.</span></span> <span data-ttu-id="43d79-263">このページでは、スケジュールされているリリース保留中状態の製造オーダーおよびバッチ オーダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="43d79-263">This page shows scheduled production and batch orders pending release.</span></span> <span data-ttu-id="43d79-264">このページでは、選択した製造オーダーのガント チャートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="43d79-264">On this page you can open the Gantt chart for selected production orders.</span></span>                                                                                                                                                                                                                                                        |




