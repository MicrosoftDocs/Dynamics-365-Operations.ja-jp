---
title: "Lifecycle Services (LCS) 内のツールを使用した、パフォーマンスのトラブルシューティング"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) がサンドボックスと生産環境でのパフォーマンスの問題を診断して緩和できるようにするために提供するさまざまなツールについて説明します。"
author: manalidongre
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: e6817ffbf83347b0407aed412267bb0481f55a8c
ms.contentlocale: ja-jp
ms.lasthandoff: 10/08/2018

---

# <a name="performance-troubleshooting-using-tools-in-lifecycle-services-lcs"></a><span data-ttu-id="598d1-103">Lifecycle Services (LCS) 内のツールを使用した、パフォーマンスのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="598d1-103">Performance troubleshooting using tools in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="598d1-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) で使用可能なツールを使用してパフォーマンスの問題をトラブルシューティングおよび緩和する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="598d1-104">This topic describes how you can troubleshoot and mitigate performance issues using the tools available in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="598d1-105">概要</span><span class="sxs-lookup"><span data-stu-id="598d1-105">Overview</span></span>
<span data-ttu-id="598d1-106">顧客およびパートナーからよくあるフィードバックは、LCS のツールを使用してパフォーマンスの問題を正常に診断することができないというものでした。</span><span class="sxs-lookup"><span data-stu-id="598d1-106">Common feedback from customers and partners has been that they are unable to successfully diagnose performance issues using the tools in LCS.</span></span> <span data-ttu-id="598d1-107">要求時にパフォーマンス測定基準を収集する信頼性の高い方法を作成することで、このフィードバックに対処しました。</span><span class="sxs-lookup"><span data-stu-id="598d1-107">We have addressed this feedback by creating a more reliable way to collect performance metrics on demand.</span></span> <span data-ttu-id="598d1-108">これにより、顧客やパートナーは、サンドボックスまたは生産環境での問題を軽減するために使用できる事前に定義された一連のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="598d1-108">This enables customers and partners to execute a pre-defined set of actions that can be used to mitigate issues in a sandbox or production environment.</span></span> <span data-ttu-id="598d1-109">この機能は、直接 SQL Server を照会するため、ほぼリアルタイムでクエリ ストア指標が取得されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-109">This feature queries SQL Server directly, so you get query store metrics in near real-time.</span></span> <span data-ttu-id="598d1-110">アクションが実行されたときにアクションを実行したユーザーを容易に判断できるように、実行されるアクションに監査証跡も追加しました。</span><span class="sxs-lookup"><span data-stu-id="598d1-110">We have also added an audit trail on the action performed so that you can easily determine who performed the action and when it was performed.</span></span>

## <a name="details"></a><span data-ttu-id="598d1-111">詳細情報</span><span class="sxs-lookup"><span data-stu-id="598d1-111">Details</span></span>
<span data-ttu-id="598d1-112">LCS のすべての SQL パフォーマンス ツールは、特定の環境の **環境の監視** ページにある **SQL インサイト** タブから使用できます。</span><span class="sxs-lookup"><span data-stu-id="598d1-112">All SQL performance tools in LCS are available under the **SQL Insights** tab on the **Environment Monitoring** page for a specific environment.</span></span> <span data-ttu-id="598d1-113">次のタブがあります。</span><span class="sxs-lookup"><span data-stu-id="598d1-113">The following tabs are available:</span></span>

- <span data-ttu-id="598d1-114">**ライブ ビュー** - 現在の DTU、実行中のステートメント、ブロックしているステートメントを示しています。</span><span class="sxs-lookup"><span data-stu-id="598d1-114">**Live View** - Shows current DTU, executing statements, and blocking statements.</span></span> <span data-ttu-id="598d1-115">パフォーマンスの問題を示す現在の **SQL Now** ページは、**ライブ ビュー**に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="598d1-115">The current **SQL Now** page that shows performance issues will be replaced with **Live View**.</span></span>

    <span data-ttu-id="598d1-116">[![ライブ ビュー](./media/LiveView.JPG
    )](./media/LiveView.JPG)</span><span class="sxs-lookup"><span data-stu-id="598d1-116">[![liveview](./media/LiveView.JPG
  )](./media/LiveView.JPG)</span></span>

- <span data-ttu-id="598d1-117">**クエリ** - 必要に応じてメトリックを取得するために使用される定義済みのクエリの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="598d1-117">**Queries** - Shows a list of pre-defined queries that can be used to retrieve metrics on demand.</span></span> <span data-ttu-id="598d1-118">クエリの例には、現在のブロック ツリー、有効な計画ガイドのリスト、および最も高価なクエリの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="598d1-118">Examples of queries include a current blocking tree, a list of active plan guides, and a list of most expensive queries.</span></span>

    <span data-ttu-id="598d1-119">[![クエリ](./media/Queries.JPG)](./media/Queries.JPG)</span><span class="sxs-lookup"><span data-stu-id="598d1-119">[![queries](./media/Queries.JPG)](./media/Queries.JPG)</span></span>

- <span data-ttu-id="598d1-120">**アクション** - サンド ボックスと製造環境での問題を緩和するために実行する必要がある定義済みアクションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="598d1-120">**Actions** - Shows a list of pre-defined actions that should be taken to mitigate issues in the sandbox and production environments.</span></span> <span data-ttu-id="598d1-121">アクションの例としては、インデックスの追加または削除、テーブルでの統計の更新、インデックスの再構築、ブロック ステートメントの終了があります。</span><span class="sxs-lookup"><span data-stu-id="598d1-121">Examples of actions include adding/dropping an index, updating stats on a table, rebuilding indexes, and terminating a blocking statement.</span></span>  <span data-ttu-id="598d1-122">アクションを実行するといつでも、環境の環境履歴に実行されるアクションの記録が表示されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-122">Any time that an action is performed, the environment history for an environment will show a record for the action performed.</span></span> <span data-ttu-id="598d1-123">履歴レコードは、クエリの実行時ではなく、アクションにのみ作成されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-123">A history record is created only for actions and not when queries are executed.</span></span> 

    <span data-ttu-id="598d1-124">[![アクション](./media/Actions.JPG)](./media/Actions.JPG)</span><span class="sxs-lookup"><span data-stu-id="598d1-124">[![actions](./media/Actions.JPG)](./media/Actions.JPG)</span></span>

- <span data-ttu-id="598d1-125">**パフォーマンス メトリックス** - 論理入出力、実行カウント、期間、CPU 時間、および待機数に基づいて、選択した期間にシステムで実行された最もコストのかかったクエリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-125">**Performance Metrics** – Shows the most expensive queries that were run in the system during the selected period, based on logical I/O, execution count, duration, CPU time, and wait count.</span></span> <span data-ttu-id="598d1-126">このデータは SQL クエリ ストアからクエリされます。</span><span class="sxs-lookup"><span data-stu-id="598d1-126">This data is queried from the SQL query store.</span></span> <span data-ttu-id="598d1-127">データは 30 日間保持され、ツールは毎日、協定世界時 (UTC) の午後 10 時にデータ収集を実行します。</span><span class="sxs-lookup"><span data-stu-id="598d1-127">The data is retained for 30 days, and the tool runs its data collection every day at 10:00 PM Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="598d1-128">ツールを使用するには、過去 30 日間の期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="598d1-128">To use the tool, select a period during the last 30 days.</span></span> <span data-ttu-id="598d1-129">クエリ結果が表示されたら、期間グラフ内のバーを選択して、クエリが他の基準に該当する場所を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="598d1-129">When the query results appear, select the bar in the duration chart to highlight where the query falls on other metrics.</span></span> <span data-ttu-id="598d1-130">**ステートメント**タブで、クエリを表示、またはクエリの実行計画をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="598d1-130">On the **Statement** tab, view the query, or download the query execution plan.</span></span>

    <span data-ttu-id="598d1-131">[![パフォーマンス メトリックス](./media/perfmetrics.JPG)](./media/perfmetrics.JPG)</span><span class="sxs-lookup"><span data-stu-id="598d1-131">[![perfmetrics](./media/perfmetrics.JPG)](./media/perfmetrics.JPG)</span></span>

- <span data-ttu-id="598d1-132">**インデックス分析** - ユーザーのスキャン、ユーザーのシーク、ユーザーの更新プログラム、および行の数に基づいて、集計インデックスとテーブル情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-132">**Index Analysis** - Shows aggregated index and table information, based on user scans, user seeks, user updates, and row count.</span></span> <span data-ttu-id="598d1-133">パフォーマンス測定基準と同様に、このツールは追加のテーブル メトリックスと共に選択したインデックスのトレンドを表示します。</span><span class="sxs-lookup"><span data-stu-id="598d1-133">Like performance metrics, this tool shows the trend for the selected index along with additional table metrics.</span></span>

    <span data-ttu-id="598d1-134">[![インデックス分析](./media/IndexAnalysis.JPG)](./media/IndexAnalysis.JPG)</span><span class="sxs-lookup"><span data-stu-id="598d1-134">[![IndexAnalysis](./media/IndexAnalysis.JPG)](./media/IndexAnalysis.JPG)</span></span>

#### <a name="queries-tab-and-actions-tab---for-details-on-queries-shown-on-the-queries-and-actions-tabs-see-the-query-cookbookquerycookbookmd"></a><span data-ttu-id="598d1-135">**クエリ** タブと **アクション** タブ - **クエリ** および **アクション** タブに表示されるクエリの詳細については、[クックブックの照会](querycookbook.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="598d1-135">**Queries** tab and **Actions** tab - For details on queries shown on the **Queries** and **Actions** tabs, see the [Query cookbook](querycookbook.md).</span></span>

## <a name="how-do-i-use-this-feature"></a><span data-ttu-id="598d1-136">この機能を使う方法</span><span class="sxs-lookup"><span data-stu-id="598d1-136">How do I use this feature?</span></span>

1. <span data-ttu-id="598d1-137">LCS でプロジェクトに移動し、環境の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="598d1-137">Go to your project in LCS and open the environment details page.</span></span> <span data-ttu-id="598d1-138">**監視** セクションで **環境監視** リンクを選択します。。</span><span class="sxs-lookup"><span data-stu-id="598d1-138">Select the **Environment Monitoring** link in the **Monitoring** section.</span></span> <span data-ttu-id="598d1-139">**SQL インサイト** タブをクリックしてこの機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="598d1-139">Click the **SQL Insights** tab to access this feature.</span></span>
2. <span data-ttu-id="598d1-140">各タブ (**ライブ ビュー**、**クエリ**、および**アクション**、**パフォーマンス メトリックス**、**インデックス**、**分析**) に移動し、詳細を表示またはクエリ実行できます。</span><span class="sxs-lookup"><span data-stu-id="598d1-140">You can navigate to each of the tabs (**Live View**, **Queries**, **Actions**, **Performance Metrics**, **Index**, **Analysis**) to view or query for more information.</span></span>
3. <span data-ttu-id="598d1-141">クエリの実行による結果を検索したり、Excel にエクスポートしたりするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="598d1-141">You have the option to search or export to Excel any of results from the query execution.</span></span>
4. <span data-ttu-id="598d1-142">パフォーマンスの問題の原因を絞り込んだら、事前に定義されたアクションを使用して問題を軽減できます。</span><span class="sxs-lookup"><span data-stu-id="598d1-142">After you have narrowed down the reason for the performance issue, you can use a predefined action to mitigate the issue.</span></span>
5. <span data-ttu-id="598d1-143">アクションを実行すると、**環境履歴** ページにエントリが作成されます。アクションの詳細、渡されたパラメーター、タイムスタンプ、アクションをトリガーしたユーザーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-143">After an action is performed, an entry is made on the **Environment History** page, which shows the details of the action, the parameters that were passed in, a timestamp, and who triggered the action.</span></span>

## <a name="sample-flow"></a><span data-ttu-id="598d1-144">サンプル フロー</span><span class="sxs-lookup"><span data-stu-id="598d1-144">Sample flow</span></span>

<span data-ttu-id="598d1-145">**シナリオ**: ユーザーは、システムを使用する場合にパフォーマンスの低下を報告します。</span><span class="sxs-lookup"><span data-stu-id="598d1-145">**Scenario**: Users report slow performance when using the system.</span></span> <span data-ttu-id="598d1-146">1 つの問題はブロック ステートメントの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="598d1-146">One issue could be a blocking statement.</span></span> <span data-ttu-id="598d1-147">正常なシステムでは単独でブロックするのが通常であり、過剰になったり、営業活動に悪影響を及ぼし始めたときのみ問題となります。</span><span class="sxs-lookup"><span data-stu-id="598d1-147">Blocking by itself is typical in a healthy system and is only a problem when it becomes excessive or starts degrading business activities.</span></span>

1. <span data-ttu-id="598d1-148">**ライブ ビュー** タブに移動し、ブロック ステートメントがないか確認します。</span><span class="sxs-lookup"><span data-stu-id="598d1-148">Go to the **Live View** tab and check if there are any blocking statements.</span></span> <span data-ttu-id="598d1-149">ブロック ステートメントがある場合、ブロック クエリ ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="598d1-149">If there is a blocking statement, copy the blocking query ID.</span></span>
2. <span data-ttu-id="598d1-150">**クエリ** タブを開き、**現在のブロック ツリー** クエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="598d1-150">Open the **Queries** tab and select the **Current Blocking Tree** query.</span></span> <span data-ttu-id="598d1-151">SQL 操作をブロックしているルート ブロッカーが返されます。</span><span class="sxs-lookup"><span data-stu-id="598d1-151">This will return the root blocker that is blocking the SQL operation.</span></span>
3. <span data-ttu-id="598d1-152">問題を解決するには、実行させて自然にクリアさせるか、リード ブロッカーのプロセスを終了して作業をロールバックすることができます。</span><span class="sxs-lookup"><span data-stu-id="598d1-152">To resolve the issue, you can either let it run and clear naturally, or end the process for the lead blocker, which will roll work back.</span></span> <span data-ttu-id="598d1-153">一般に、自然にクリアしないとは思われない場合 (不適切なクエリ プランの場合など) や、重要なプロセスを実行できないためにすぐに完了する必要があるような状況でのみリード ブロッカーを終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="598d1-153">Typically, you should only end the lead blocker process if you do not think that it will not clear naturally (such as a bad query plan), or in situations where a critical process is unable to run and needs to complete immediately.</span></span>
4. <span data-ttu-id="598d1-154">現在実行されているステートメントを終了しても問題がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="598d1-154">Confirm that it's okay to terminate the statements that are currently being executed.</span></span>
5. <span data-ttu-id="598d1-155">**アクション** タブを開き、**SQL プロセスの終了** アクションを選択して、ルート ブロッカー クエリ ID を渡します。</span><span class="sxs-lookup"><span data-stu-id="598d1-155">Open the **Actions** tab and select the **End SQL Process** action and pass in the root blocker query ID.</span></span> <span data-ttu-id="598d1-156">これは、ブロック ステートメントを終了するために SQL データベースに対してクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="598d1-156">This will execute a query against the SQL database to terminate the blocking statement.</span></span>
6. <span data-ttu-id="598d1-157">**クエリ** タブに移動し、**現在ブロックしているクエリ** を実行して、ブロック ステートメントが終了したかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="598d1-157">Go to the **Queries** tab and run **Current blocking query** to verify if the blocking statement was terminated.</span></span>
7. <span data-ttu-id="598d1-158">**環境履歴** ページで、どのプロセスが終了したかの詳細を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="598d1-158">You can also check the **Environment History** page to see details on what process was terminated.</span></span>
8. <span data-ttu-id="598d1-159">将来この問題を避けるため、インデックスまたはプラン ガイドを使用したり、ロック エスカレーションをオフにしたり、各種レコードでの操作中にプロセスが互いにブロックしている場合はページ ロックを使用してください。</span><span class="sxs-lookup"><span data-stu-id="598d1-159">To avoid this issue in the future, you should use indexes or plan guides, or turn off lock escalation, or use page locks if processes are blocking each other while operating on different records.</span></span> <span data-ttu-id="598d1-160">プロセスが同じレコードで動作している場合、ブロックを回避するには、同時に同じレコード上で動作しないよう、プロセスをリファクタリングまたは再スケジューリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="598d1-160">If processes are operating on the same records, the only way to avoid blocking is by refactoring or rescheduling the processes to not operate on the same records at the same time.</span></span>


