---
title: マスター プランの実行の監視
description: このトピックでは、生産計画担当が、マスター プランの実行が進行中かどうかを確認する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999809"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="81a20-103">マスター プランの実行の監視</span><span class="sxs-lookup"><span data-stu-id="81a20-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="81a20-104">ガント チャートを使用して、マスター プランの進行状況を視覚化する</span><span class="sxs-lookup"><span data-stu-id="81a20-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="81a20-105">**マスター プランの進行状況の表示** ページで、マスター プランの実行履歴の詳細をガント チャートとして表示できます。</span><span class="sxs-lookup"><span data-stu-id="81a20-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="81a20-106">この機能は、マスター プランのさまざまなフェーズにかかる時間を理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="81a20-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="81a20-107">現在有効な計画ジョブの場合は、**マスター プランの進行状況の表示** ページを使用して進行状況を追跡し、見積った残り時間を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81a20-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="81a20-108">マスター プランの進行状況の視覚化機能を有効にして使用します。</span><span class="sxs-lookup"><span data-stu-id="81a20-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="81a20-109">この機能を使用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="81a20-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="81a20-110">**機能管理** ワークスペースの **新規** タブで、一覧から **マスター プランの進行状況の視覚化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="81a20-111">この機能が **新しい** タブに表示されない場合は、**無効** タブおよび **すべての** タブを確認します。</span><span class="sxs-lookup"><span data-stu-id="81a20-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="81a20-112">**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-112">Select **Enable now**.</span></span> <span data-ttu-id="81a20-113">または、**スケジュール** を選択し、機能を有効にする時間を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="81a20-114">**マスター プランの進行状況の表示** ページには、計画ジョブの履歴と有効な計画ジョブの両方を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81a20-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="81a20-115">計画ジョブの履歴を表示するには、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="81a20-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="81a20-116">**マスター プラン \> 設定 \> 計画 \> マスター プラン** の順に移動し、アクション ペインで **履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="81a20-117">目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="81a20-118">**マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、マスター プラン タイルで、**履歴** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81a20-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="81a20-119">目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="81a20-120">有効な計画ジョブを表示するには、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="81a20-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="81a20-121">**マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、アクション ペインで、**未完了の計画プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="81a20-122">目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="81a20-123">**マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、マスター プラン タイルで、**進捗状況の表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="81a20-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="81a20-124">目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="81a20-125">有効なジョブは、計画ジョブが処理中の場合にのみ表示できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="81a20-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="81a20-126">マスター プラン ジョブの分析</span><span class="sxs-lookup"><span data-stu-id="81a20-126">Analyze a master planning job</span></span>

<span data-ttu-id="81a20-127">ガント チャートでは、次の各計画プロセスを展開して、以下に対して費やされた時間に関する追加情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81a20-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="81a20-128">初期化</span><span class="sxs-lookup"><span data-stu-id="81a20-128">Initializing</span></span>
- <span data-ttu-id="81a20-129">データの削除と挿入</span><span class="sxs-lookup"><span data-stu-id="81a20-129">Deleting and inserting data</span></span>
- <span data-ttu-id="81a20-130">補充計画</span><span class="sxs-lookup"><span data-stu-id="81a20-130">Coverage planning</span></span>
- <span data-ttu-id="81a20-131">遅延</span><span class="sxs-lookup"><span data-stu-id="81a20-131">Delays</span></span>
- <span data-ttu-id="81a20-132">アクション メッセージ</span><span class="sxs-lookup"><span data-stu-id="81a20-132">Action messages</span></span>
- <span data-ttu-id="81a20-133">終了処理</span><span class="sxs-lookup"><span data-stu-id="81a20-133">Finalization</span></span>
- <span data-ttu-id="81a20-134">自動確定</span><span class="sxs-lookup"><span data-stu-id="81a20-134">Auto-firming</span></span>

<span data-ttu-id="81a20-135">アクション メッセージを使用した場合の影響を表示する場合は、ガント チャートは役に立つツールです。</span><span class="sxs-lookup"><span data-stu-id="81a20-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="81a20-136">ガント チャートのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="81a20-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="81a20-137">選択したグループを展開して詳細を表示するには、ツリー ビューでプラス符号 (**+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="81a20-138">選択したグループを折りたたむには、ツリービューのマイナス記号 (**-**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="81a20-139">キーボードを使用してナビゲーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="81a20-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="81a20-140">**上方向** キーと **下方向** キーを使用して行間を移動します。</span><span class="sxs-lookup"><span data-stu-id="81a20-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="81a20-141">**右矢印** キーと **左矢印** キーを使用してグループを展開したり折りたたんだりします。</span><span class="sxs-lookup"><span data-stu-id="81a20-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="81a20-142">ガント チャートのすべてのレベルを開くか閉じるかするには、**すべて展開** または **すべて折りたたむ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="81a20-143">関連する処理時間を表示するには、タスク上にポイントします。</span><span class="sxs-lookup"><span data-stu-id="81a20-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="81a20-144">(タスクは、ガント チャートの最下位レベルです。)</span><span class="sxs-lookup"><span data-stu-id="81a20-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="81a20-145">追加のマスター プランの実行を表示してジョブを比較する</span><span class="sxs-lookup"><span data-stu-id="81a20-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="81a20-146">**追加のマスター プランの実行を表示** フィールドでマスター プラン ジョブを選択することにより、ガント チャートで追加のマスター プランの実行を表示し、2 つのジョブを比較することができます。</span><span class="sxs-lookup"><span data-stu-id="81a20-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="81a20-147">BOM-レベルの表示</span><span class="sxs-lookup"><span data-stu-id="81a20-147">BOM-level display</span></span>

<span data-ttu-id="81a20-148">部品表 (BOM) レベルは、補充計画、遅延、アクション、および確定に対して異なる方法で表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="81a20-149">**補充計画** – BOM レベルが予想どおりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="81a20-150">これらは、トップダウン方式で計算されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="81a20-151">**例:** BOM レベル 0、1、2</span><span class="sxs-lookup"><span data-stu-id="81a20-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="81a20-152">**遅延** – BOM レベルは、補充計画 BOM レベルに –1 を掛けた値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="81a20-153">(つまり、マイナス記号が付けられています。)</span><span class="sxs-lookup"><span data-stu-id="81a20-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="81a20-154">**例:** BOM レベル –2、–1、0</span><span class="sxs-lookup"><span data-stu-id="81a20-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="81a20-155">**アクション メッセージ** – BOM レベルが予想どおりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="81a20-156">これらは、トップダウン方式で計算されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="81a20-157">**例:** BOM レベル 0、1、2</span><span class="sxs-lookup"><span data-stu-id="81a20-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="81a20-158">**自動確定** – BOM レベルは、999 から、補充計画 BOM レベルを差し引いた値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="81a20-159">**例:** BOM レベル 999、998、997</span><span class="sxs-lookup"><span data-stu-id="81a20-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="81a20-160">次の表で、この動作が要約されています。</span><span class="sxs-lookup"><span data-stu-id="81a20-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="81a20-161">表示される BOM レベル</span><span class="sxs-lookup"><span data-stu-id="81a20-161">BOM level that is shown</span></span> | <span data-ttu-id="81a20-162">最終品目</span><span class="sxs-lookup"><span data-stu-id="81a20-162">End item</span></span> | <span data-ttu-id="81a20-163">サブコンポーネント</span><span class="sxs-lookup"><span data-stu-id="81a20-163">Subcomponent</span></span> | <span data-ttu-id="81a20-164">原材料</span><span class="sxs-lookup"><span data-stu-id="81a20-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="81a20-165">補充計画</span><span class="sxs-lookup"><span data-stu-id="81a20-165">Coverage planning</span></span> | <span data-ttu-id="81a20-166">0</span><span class="sxs-lookup"><span data-stu-id="81a20-166">0</span></span> | <span data-ttu-id="81a20-167">1</span><span class="sxs-lookup"><span data-stu-id="81a20-167">1</span></span> | <span data-ttu-id="81a20-168">2</span><span class="sxs-lookup"><span data-stu-id="81a20-168">2</span></span> |
| <span data-ttu-id="81a20-169">遅延</span><span class="sxs-lookup"><span data-stu-id="81a20-169">Delays</span></span> | <span data-ttu-id="81a20-170">0</span><span class="sxs-lookup"><span data-stu-id="81a20-170">0</span></span> | <span data-ttu-id="81a20-171">–1</span><span class="sxs-lookup"><span data-stu-id="81a20-171">–1</span></span> | <span data-ttu-id="81a20-172">–2</span><span class="sxs-lookup"><span data-stu-id="81a20-172">–2</span></span> |
| <span data-ttu-id="81a20-173">アクション メッセージ</span><span class="sxs-lookup"><span data-stu-id="81a20-173">Action message</span></span> | <span data-ttu-id="81a20-174">0</span><span class="sxs-lookup"><span data-stu-id="81a20-174">0</span></span> | <span data-ttu-id="81a20-175">1</span><span class="sxs-lookup"><span data-stu-id="81a20-175">1</span></span> | <span data-ttu-id="81a20-176">2</span><span class="sxs-lookup"><span data-stu-id="81a20-176">2</span></span> |
| <span data-ttu-id="81a20-177">自動確定</span><span class="sxs-lookup"><span data-stu-id="81a20-177">Auto-firming</span></span> | <span data-ttu-id="81a20-178">999</span><span class="sxs-lookup"><span data-stu-id="81a20-178">999</span></span> | <span data-ttu-id="81a20-179">998</span><span class="sxs-lookup"><span data-stu-id="81a20-179">998</span></span> | <span data-ttu-id="81a20-180">997</span><span class="sxs-lookup"><span data-stu-id="81a20-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="81a20-181">進行状況の視覚化</span><span class="sxs-lookup"><span data-stu-id="81a20-181">Visualize progress</span></span>

<span data-ttu-id="81a20-182">現在実行中のマスター プラン ジョブを表示する場合は、ガント チャートの色によって進行状況が表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="81a20-183">次の色は、青のテーマに適用されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="81a20-184">他の色のテーマでは、色が異なります。</span><span class="sxs-lookup"><span data-stu-id="81a20-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="81a20-185">**濃い青** – プラン タスクが完了しました。</span><span class="sxs-lookup"><span data-stu-id="81a20-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="81a20-186">**オレンジ** – 現在処理中のタスク。</span><span class="sxs-lookup"><span data-stu-id="81a20-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="81a20-187">**ライト ブルー** – 残りのタスクの見積。</span><span class="sxs-lookup"><span data-stu-id="81a20-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="81a20-188">色は、ガント チャートの最下位レベルにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="81a20-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="81a20-189">**すべて展開** を選択して、マスター プラン ジョブのすべてのタスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="81a20-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="81a20-190">残りのタスクの見積は、マスター プラン ジョブの履歴に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="81a20-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="81a20-191">マスター プランの実行と処理時間の追跡</span><span class="sxs-lookup"><span data-stu-id="81a20-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="81a20-192">既定のダッシュボードで、**マスター プラン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="81a20-193">**計画** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="81a20-194">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-194">Select **Run**.</span></span>
1. <span data-ttu-id="81a20-195">**処理時間の追跡** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="81a20-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="81a20-196">**スレッド数** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="81a20-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="81a20-197">**対象に含めるレコード** クイック タブで、**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="81a20-198">グリッドで、**フィールド** フィールドが **品目番号** に設定されている行を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="81a20-199">**基準** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="81a20-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="81a20-200">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="81a20-200">Select **OK**.</span></span>
