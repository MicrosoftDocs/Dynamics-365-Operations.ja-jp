---
title: ER 構成で起こるトラブルシューティング パフォーマンスの問題
description: このトピックでは、電子申告 (ER) 構成で起こるパフォーマンスの問題を検索して修正する方法について説明します。
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216868"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="0f431-103">ER 構成で起こるトラブルシューティング パフォーマンスの問題</span><span class="sxs-lookup"><span data-stu-id="0f431-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="0f431-104">このトピックでは、[電子申告](general-electronic-reporting.md) (ER) [構成](general-electronic-reporting.md#Configuration) で起こるパフォーマンスの問題を検索して解決する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f431-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="0f431-105">通常、パフォーマンス調査は複数のステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0f431-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="0f431-106">データの [収集](#collecting-data)。</span><span class="sxs-lookup"><span data-stu-id="0f431-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="0f431-107">収集したデータを分析します。</span><span class="sxs-lookup"><span data-stu-id="0f431-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="0f431-108">分析結果に基づいて、ER 構成を使用して [変更する](#making-changes) か、データをさらに収集することを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f431-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="0f431-109">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="0f431-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="0f431-110">実行時間の分析</span><span class="sxs-lookup"><span data-stu-id="0f431-110">Analyze execution time</span></span>

<span data-ttu-id="0f431-111">実行時間は、同じ環境で実行されている他のタスクや、データを初めて呼び出したときにデータを使用するキャッシュなど、予測できない要因によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="0f431-112">そのため、実行と測定を数回繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="0f431-113">パフォーマンスの問題は、レポートで使用する ER 形式の構成が原因でない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="0f431-114">その場合は、ER 形式の構成を開くために使用する X++ コードが原因です。</span><span class="sxs-lookup"><span data-stu-id="0f431-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="0f431-115">[アクション センター](#infolog-time) または [イベント ログ](#event-log-time) で、レポートの実行時間を確認します。</span><span class="sxs-lookup"><span data-stu-id="0f431-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="0f431-116">レポートの実行時間とシナリオの合計実行時間を比較します。</span><span class="sxs-lookup"><span data-stu-id="0f431-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="0f431-117">レポートの実行時間が合計実行時間よりかなり短い場合は、レポートで処理されるデータ量を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="0f431-118">レポートで処理されるデータが少量の場合、問題は構成の読み込み時間に関係する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="0f431-119">レポートで処理されるデータが大量にある場合、問題は前処理の X++ に関係する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="0f431-120">[Trace Parser](#analyze-trace-parser-trace) を使用してこのケースを分析します。</span><span class="sxs-lookup"><span data-stu-id="0f431-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="0f431-121">その他のケースについては、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="0f431-122">異なる量のデータを含む複数のテストを実行して、実行時間がデータ量にどう影響されているかを判断します。</span><span class="sxs-lookup"><span data-stu-id="0f431-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="0f431-123">Trace Parser トレースの分析</span><span class="sxs-lookup"><span data-stu-id="0f431-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="0f431-124">小規模な例を準備するか、またはレポート生成時に複数のトレースをランダムに収集します。</span><span class="sxs-lookup"><span data-stu-id="0f431-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="0f431-125">次に、[Trace Parser](#trace-parser) で標準のボトムツーアップ分析を行い、次の質問に答えます。</span><span class="sxs-lookup"><span data-stu-id="0f431-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="0f431-126">時間消費に関して優れたメソッドは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0f431-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="0f431-127">これらのメソッドに必要な時間は、全体のどの時間ですか。</span><span class="sxs-lookup"><span data-stu-id="0f431-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="0f431-128">クエリに対して同じ質問に答えます。</span><span class="sxs-lookup"><span data-stu-id="0f431-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="0f431-129">メソッドの先頭に "ER" が付いている場合は、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="0f431-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="0f431-130">アプリケーション スイートで作成されたメソッドまたはクエリが表示された場合は、汎用的な最適化 (インデックスの作成など) を検討してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="0f431-131">呼び出し回数を分析します。</span><span class="sxs-lookup"><span data-stu-id="0f431-131">Analyze the number of calls.</span></span> <span data-ttu-id="0f431-132">この回数が予想よりも大幅に多い場合は、対応する構成ノードをキャッシュすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="0f431-133">データベース呼び出しの分析</span><span class="sxs-lookup"><span data-stu-id="0f431-133">Analyze database calls</span></span>

<span data-ttu-id="0f431-134">少量のデータを含む例を準備し、[ER トレース](#electronic-reporting-traces) を収集できるようにします 。</span><span class="sxs-lookup"><span data-stu-id="0f431-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="0f431-135">次に、ER モデル マッピング デザイナーでトレースを開き、ページの下部を確認します。</span><span class="sxs-lookup"><span data-stu-id="0f431-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="0f431-136">次の質問に答えます。</span><span class="sxs-lookup"><span data-stu-id="0f431-136">Answer the following questions:</span></span>

- <span data-ttu-id="0f431-137">重複したクエリはありますか。</span><span class="sxs-lookup"><span data-stu-id="0f431-137">Is there any query duplication?</span></span> <span data-ttu-id="0f431-138">ある場合は、次のいずれかの修正を検討してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="0f431-139">1 つの親レコード内に複数の呼び出しがあると思われる場合は、[キャッシュを使用する](#use-caching)。</span><span class="sxs-lookup"><span data-stu-id="0f431-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="0f431-140">異なるレコード内に同じ呼び出しがあると思われる場合は、[キャッシュされパラメータ化された計算フィールドを使用する](#cached-parameterized)。</span><span class="sxs-lookup"><span data-stu-id="0f431-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="0f431-141">データベースから多数の異なるレコードを読み取る必要がある場合、[**統合** データ ソースを使用します](#use-join-datasource)。</span><span class="sxs-lookup"><span data-stu-id="0f431-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="0f431-142">クエリおよびフェッチされたレコードの数は、データの合計数と一致しますか。</span><span class="sxs-lookup"><span data-stu-id="0f431-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="0f431-143">たとえば、ドキュメントに明細行が 10 ある場合、レポートが 10 または 1,000 の明細行を抽出したと統計に表示されていますか。</span><span class="sxs-lookup"><span data-stu-id="0f431-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="0f431-144">フェッチされるレコードが多数ある場合は、次のいずれかの方法で修正を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="0f431-145">[**場所** 機能の代わりに **フィルター** 機能を使用して](#filter) SQL サーバー側のデータを処理します。</span><span class="sxs-lookup"><span data-stu-id="0f431-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="0f431-146">キャッシュを使用して、同じデータをフェッチするのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="0f431-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="0f431-147">[収集したデータ機能を使用して](#collected-data)、要約処理に必要な同じデータをフェッチするのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="0f431-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="0f431-148">PerfView 追跡の分析</span><span class="sxs-lookup"><span data-stu-id="0f431-148">Analyze PerfView traces</span></span>

<span data-ttu-id="0f431-149">[PerfView](#perfview) は経験豊富な開発者のためのツールです。</span><span class="sxs-lookup"><span data-stu-id="0f431-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="0f431-150">次の手順の詳細については、[時計時刻調査の基本](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="0f431-151">スレッド時間を使用して追跡を収集します。</span><span class="sxs-lookup"><span data-stu-id="0f431-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="0f431-152">**runUnattended** を使用するスタックのみを含めて、構成が実行されているスレッドのみをフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="0f431-153">(**IncPats** の入力ボックスに **runUnattended** を追加します。)</span><span class="sxs-lookup"><span data-stu-id="0f431-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="0f431-154">すべての CPU、ネットワーク、およびブロックされた時間を折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="0f431-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="0f431-155">[PerfView 用の ER プリセット](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0f431-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="0f431-156">**ER** \> **その他のプリセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f431-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="0f431-157">名前を確認します。</span><span class="sxs-lookup"><span data-stu-id="0f431-157">Look at the names:</span></span>

    - <span data-ttu-id="0f431-158">ほとんどの時間を消費するプラットフォーム コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f431-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="0f431-159">ダブルタップ (またはダブルクリック) し、**呼び出し先** を上方向に移動して確認します。</span><span class="sxs-lookup"><span data-stu-id="0f431-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="0f431-160">接頭語 "ERExpression" を持つクラスおよび式に関連する関数のクラスがある場合は、クラス名に基づいて関数名を変更でき、ER レポジトリを参照して属性を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="0f431-161">修正</span><span class="sxs-lookup"><span data-stu-id="0f431-161">Fixes</span></span>

- <span data-ttu-id="0f431-162">クエリが CPU 時間の大部分を消費する場合は、クエリの数を減らしてください。</span><span class="sxs-lookup"><span data-stu-id="0f431-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="0f431-163">重複するクエリの [ER 追跡を確認します](#analyze-database-calls)。</span><span class="sxs-lookup"><span data-stu-id="0f431-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="0f431-164">フェッチされるレコード数を確認し、理論的にフェッチするデータの量を評価します。</span><span class="sxs-lookup"><span data-stu-id="0f431-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="0f431-165">使用している機能がほとんどの CPU 時間を消費する場合は、リソースを最も消費する構成で場所を探してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="0f431-166">データ収集機能が CPU 時間の大半を消費する場合、モデル マッピング側で *SQL グループ別* に置き換えることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="0f431-167">データ収集</span><span class="sxs-lookup"><span data-stu-id="0f431-167">Collecting data</span></span>

<span data-ttu-id="0f431-168">環境によっては、使用可能なデータを収集する方法がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="0f431-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="0f431-169">合計実行時間を確認する。</span><span class="sxs-lookup"><span data-stu-id="0f431-169">Get the total running time:</span></span>

    - <span data-ttu-id="0f431-170">アクション センターから</span><span class="sxs-lookup"><span data-stu-id="0f431-170">From the Action center</span></span>
    - <span data-ttu-id="0f431-171">イベント ログから</span><span class="sxs-lookup"><span data-stu-id="0f431-171">From the event log</span></span>

- <span data-ttu-id="0f431-172">実行をプロファイルする。</span><span class="sxs-lookup"><span data-stu-id="0f431-172">Profile the execution:</span></span>

    - <span data-ttu-id="0f431-173">ER ツールを使用</span><span class="sxs-lookup"><span data-stu-id="0f431-173">By using ER tools</span></span>
    - <span data-ttu-id="0f431-174">Trace Parser を使用</span><span class="sxs-lookup"><span data-stu-id="0f431-174">By using Trace parser</span></span>
    - <span data-ttu-id="0f431-175">PerfView を使用</span><span class="sxs-lookup"><span data-stu-id="0f431-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="0f431-176">運用環境でデータの収集</span><span class="sxs-lookup"><span data-stu-id="0f431-176">Collecting data in a production environment</span></span>

<span data-ttu-id="0f431-177">運用環境でのみ問題を再現できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="0f431-178">次の方法でデータを収集できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="0f431-179">[Trace Parser](../perf-test/trace-trace-tutorial.md) トレースを使用</span><span class="sxs-lookup"><span data-stu-id="0f431-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="0f431-180">[ER 実行](trace-execution-er-troubleshoot-perf.md) トレースを使用</span><span class="sxs-lookup"><span data-stu-id="0f431-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="0f431-181">合計実行時間を使用</span><span class="sxs-lookup"><span data-stu-id="0f431-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="0f431-182">開発環境でデータの収集</span><span class="sxs-lookup"><span data-stu-id="0f431-182">Collecting data in a development environment</span></span>

<span data-ttu-id="0f431-183">運用環境で使用できるツールの他に、開発環境で使用できるツールもあります。</span><span class="sxs-lookup"><span data-stu-id="0f431-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="0f431-184">イベント ログ (Microsoft-Dynamics-ElectronicReporting)。</span><span class="sxs-lookup"><span data-stu-id="0f431-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="0f431-185">このログを使用すると、合計実行時間を確認できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="0f431-186">一般的な .NETツール (PerfView など)。</span><span class="sxs-lookup"><span data-stu-id="0f431-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="0f431-187">また、開発環境では柔軟性が増すため、実験しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="0f431-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="0f431-188">たとえば、レポートの一部をオフにすると実行時間への影響を確認できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="0f431-189">ツール</span><span class="sxs-lookup"><span data-stu-id="0f431-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="0f431-190">アクション センターでの実行時間</span><span class="sxs-lookup"><span data-stu-id="0f431-190">Execution time in the Action center</span></span>

<span data-ttu-id="0f431-191">ER では、アクション センターで構成の実行時間を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="0f431-192">このオプションは、対話型セッションで特定のユーザーと会社に対してのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0f431-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="0f431-193">この機能を使用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0f431-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="0f431-194">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0f431-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="0f431-195">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f431-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="0f431-196">**ユーザー パラメーター** ダイアログ ボックスで、**ファイル生成時間の表示** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0f431-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="0f431-197">イベント ログでの実行時間</span><span class="sxs-lookup"><span data-stu-id="0f431-197">Execution time in the event log</span></span>

1. <span data-ttu-id="0f431-198">Windows イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f431-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="0f431-199">**アプリケーションとサービス ログ** で、**Microsoft-Dynamics-ElectronicReporting/Operational** を開きます。</span><span class="sxs-lookup"><span data-stu-id="0f431-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="0f431-200">**EventID=2** の **FormatMapingRun** イベントを検索します。これらのイベントには、経過時間に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0f431-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="0f431-201">Trace Parser トレース</span><span class="sxs-lookup"><span data-stu-id="0f431-201">Trace parser traces</span></span> 

<span data-ttu-id="0f431-202">ER は X++ に実装されているので、一般的な X++ ツールを使用してパフォーマンスを分析できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="0f431-203">詳細については、[Trace Parser を使用したトレースの取得](../perf-test/trace-trace-tutorial.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="0f431-204">この方法にはいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="0f431-205">ER の一部が C# に実装されているため、表示できない詳細があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="0f431-206">ただし、データの使用状況の詳細は表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-206">However, you can view the data usage details.</span></span> <span data-ttu-id="0f431-207">また、長いレポートを実行すると、トレースのストレージ制限を超える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="0f431-208">ER トレース</span><span class="sxs-lookup"><span data-stu-id="0f431-208">ER traces</span></span>

<span data-ttu-id="0f431-209">ER は独自のトレースを収集し、そのトレースには視覚化および分析ツールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0f431-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="0f431-210">詳細については、[電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング](trace-execution-er-troubleshoot-perf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="0f431-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="0f431-211">PerfView</span></span>

<span data-ttu-id="0f431-212">X++ と ER の両方が .NET プラットフォーム上に実装されているので、共通の .NET ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="0f431-213">たとえば、無料の [PerfView](https://github.com/Microsoft/perfview) ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="0f431-214">また、コマンド ラインからデータを収集することもできます。</span><span class="sxs-lookup"><span data-stu-id="0f431-214">You can also collect data from the command line.</span></span> <span data-ttu-id="0f431-215">たとえば、次の Windows PowerShell スクリプトは、マシンであらゆる形式の実行が停止されるまでの実行時間を収集します。</span><span class="sxs-lookup"><span data-stu-id="0f431-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="0f431-216">この方法にはいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="0f431-217">マシンへの管理アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f431-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="0f431-218">また、難易度がかなり高いため経験豊富な開発者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="0f431-219">変更の実行</span><span class="sxs-lookup"><span data-stu-id="0f431-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="0f431-220">キャッシュの使用</span><span class="sxs-lookup"><span data-stu-id="0f431-220">Use caching</span></span>

<span data-ttu-id="0f431-221">キャッシュによってデータの再フェッチに必要な時間が短縮されますが、メモリが必要です。</span><span class="sxs-lookup"><span data-stu-id="0f431-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="0f431-222">フェッチされたデータの量が大きくない場合は、キャッシュを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f431-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="0f431-223">キャッシュの使用方法の詳細と例については、[実行トレースの情報に基づいてモデル マッピングを改善する](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="0f431-224">キャッシュされパラメーター化された計算済フィールドの使用</span><span class="sxs-lookup"><span data-stu-id="0f431-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="0f431-225">値を繰り返し検索する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="0f431-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="0f431-226">例には、アカウント名やアカウント番号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0f431-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="0f431-227">時間を節約するために、トップ レベルのパラメーターを含む計算済フィールドを作成し、そのフィールドをキャッシュに追加します。</span><span class="sxs-lookup"><span data-stu-id="0f431-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="0f431-228">この方法は、キャッシュされたデータのサイズが小さい場合にのみ使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0f431-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="0f431-229">詳細については、[パラメーター化された計算済みフィールド データ ソースを追加して ER のパフォーマンスを向上させる](er-calculated-field-ds-performance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="0f431-230">結合データ ソースを作成する</span><span class="sxs-lookup"><span data-stu-id="0f431-230">Use a JOIN data source</span></span>

<span data-ttu-id="0f431-231">**結合** データ ソースを使用すると、接続されている複数のレコードを 1 つのクエリでフェッチすることができます。</span><span class="sxs-lookup"><span data-stu-id="0f431-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="0f431-232">接続されている各レコードをフェッチするために個別のクエリを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0f431-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="0f431-233">たとえば、行が 1,000 あり、リレーションごとに各行の品目データをフェッチすると、1,001 クエリ (= 1,000 + 1) になります。</span><span class="sxs-lookup"><span data-stu-id="0f431-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="0f431-234">**結合** データ ソースを使用する場合は、同じデータをフェッチするのに必要なクエリは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="0f431-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="0f431-235">詳細については、[ER モデル マッピングの結合データ ソースを使用して、複数のアプリケーション テーブルからデータを入手する](er-join-data-sources.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="0f431-236">WHERE 関数の代わりに FILTER 関数を使用します</span><span class="sxs-lookup"><span data-stu-id="0f431-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="0f431-237">**[FILTER](er-functions-list-filter.md)** 関数は、SQL Server で条件を実行しますが、**WHERE** 関数は一覧からすべてのデータをフェッチし (一度に 1 つのレコード) 各レコードの条件を適用します。</span><span class="sxs-lookup"><span data-stu-id="0f431-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="0f431-238">たとえば、1,000 あるレコードの中からレコードを 1 つ選択するとします。</span><span class="sxs-lookup"><span data-stu-id="0f431-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="0f431-239">**WHERE** を使用すると、1,000 のレコードすべてがフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="0f431-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="0f431-240">ただし、**FILTER** を使用すると、ちょうど 1 つのレコードがフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="0f431-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="0f431-241">**FILTER** では、データベース側でインデックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="0f431-242">収集されたデータ機能または累積データ ソースの使用</span><span class="sxs-lookup"><span data-stu-id="0f431-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="0f431-243">コンフィギュレーションに、以前にレポート別にフェッチされたデータを集計する *グループ化* コンポーネントがある場合、そのコンポーネントは、すべてのデータを再度フェッチします。</span><span class="sxs-lookup"><span data-stu-id="0f431-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="0f431-244">収集したデータ機能を使用すると、ER は最初のフェッチ時にデータを累積できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f431-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="0f431-245">詳細については、[集計と合計を実行するのに必要な ER 構成形式](tasks/er-format-counting-summing-2.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f431-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="0f431-246">X++ の構成の一部を再書き込みする</span><span class="sxs-lookup"><span data-stu-id="0f431-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="0f431-247">ER は、テーブルおよびクラスの呼び出しメソッド (拡張子を含む) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0f431-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="0f431-248">パフォーマンスを向上させるために、X++ でモデル マッピングの一部を再書き込みしてください。</span><span class="sxs-lookup"><span data-stu-id="0f431-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="0f431-249">ER は次のソースからデータを消費できます。</span><span class="sxs-lookup"><span data-stu-id="0f431-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="0f431-250">クラス (**オブジェクト** および **クラス** データ ソース)</span><span class="sxs-lookup"><span data-stu-id="0f431-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="0f431-251">テーブル (**テーブル** および **テーブル レコード** のデータ ソース)</span><span class="sxs-lookup"><span data-stu-id="0f431-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="0f431-252">[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) は、呼び出しコードから事前に計算されたデータを送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="0f431-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="0f431-253">アプリケーション スイートには、このアプローチの例が多数あります。</span><span class="sxs-lookup"><span data-stu-id="0f431-253">The application suite contains numerous examples of this approach.</span></span>
