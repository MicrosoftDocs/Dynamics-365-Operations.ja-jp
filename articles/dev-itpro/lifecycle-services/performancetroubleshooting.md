<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="performancetroubleshooting.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>performancetroubleshooting.faeffb.4b0e958ea98d972fe999a6188038a844fec7387d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4b0e958ea98d972fe999a6188038a844fec7387d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\performancetroubleshooting.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Performance troubleshooting using tools in Lifecycle Services (LCS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) 内のツールを使用した、パフォーマンスのトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the various tools that Microsoft Dynamics Lifecycle Services (LCS) provides to help you diagnose and mitigate performance issues in your sandbox and production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) がサンドボックスと生産環境でのパフォーマンスの問題を診断して緩和できるようにするために提供するさまざまなツールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Performance troubleshooting using tools in Lifecycle Services (LCS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) 内のツールを使用した、パフォーマンスのトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how you can troubleshoot and mitigate performance issues using the tools available in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) で使用可能なツールを使用してパフォーマンスの問題をトラブルシューティングおよび緩和する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Common feedback from customers and partners has been that they are unable to successfully diagnose performance issues using the tools in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客およびパートナーからよくあるフィードバックは、LCS のツールを使用してパフォーマンスの問題を正常に診断することができないというものでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>We have addressed this feedback by creating a more reliable way to collect performance metrics on demand.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求時にパフォーマンス測定基準を収集する信頼性の高い方法を作成することで、このフィードバックに対処しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This enables customers and partners to execute a predefined set of actions that can be used to mitigate issues in a sandbox or production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、顧客やパートナーは、サンドボックスまたは生産環境での問題を軽減するために使用できる事前に定義された一連のアクションを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This feature queries SQL Server directly, so you get query store metrics in near real-time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、直接 SQL Server を照会するため、ほぼリアルタイムでクエリ ストア指標が取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>We have also added an audit trail on the action performed so that you can easily determine who performed the action and when it was performed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションが実行されたときにアクションを実行したユーザーを容易に判断できるように、実行されるアクションに監査証跡も追加しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>All SQL performance tools in LCS are available under the <bpt id="p1">**</bpt>SQL Insights<ept id="p1">**</ept> tab on the <bpt id="p2">**</bpt>Environment Monitoring<ept id="p2">**</ept> page for a specific environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のすべての SQL パフォーマンス ツールは、特定の環境の <bpt id="p2">**</bpt>環境の監視<ept id="p2">**</ept> ページにある <bpt id="p1">**</bpt>SQL インサイト<ept id="p1">**</ept> タブから使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following tabs are available:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のタブがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Live View<ept id="p1">**</ept> – Shows current DTU, executing statements, and blocking statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ライブ ビュー<ept id="p1">**</ept> – 現在の DTU、実行中のステートメント、ブロックしているステートメントを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The current <bpt id="p1">**</bpt>SQL Now<ept id="p1">**</ept> page that shows performance issues will be replaced with <bpt id="p2">**</bpt>Live View<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスの問題を示す現在の <bpt id="p1">**</bpt>SQL Now<ept id="p1">**</ept> ページは、<bpt id="p2">**</bpt>ライブ ビュー<ept id="p2">**</ept>に置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Live View<ept id="p1">](./media/LiveView.JPG)](./media/LiveView.JPG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ライブ ビュー<ept id="p1">](./media/LiveView.JPG)](./media/LiveView.JPG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Queries<ept id="p1">**</ept> – Shows a list of predefined queries that can be used to retrieve metrics on demand.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ<ept id="p1">**</ept> – 必要に応じてメトリックを取得するために使用される定義済みのクエリの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Examples of queries include a current blocking tree, a list of active plan guides, and a list of most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの例には、現在のブロック ツリー、有効な計画ガイドのリスト、および最も高価なクエリの一覧が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Queries<ept id="p1">](./media/Queries.JPG)](./media/Queries.JPG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>クエリ<ept id="p1">](./media/Queries.JPG)](./media/Queries.JPG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>To help guarantee that the query results are returned instantaneously, most of the queries are run synchronously.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ結果が即座に返されることを保証するために、ほとんどのクエリは同期的に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, if there is an ongoing performance issue, synchronous query execution might cause a time-out error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、パフォーマンスに問題が発生している場合は、同期クエリの実行によってタイム アウト エラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>To address this issue, a new <bpt id="p1">**</bpt>Use Fast Query<ept id="p1">**</ept> option has been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題に対処するために、新しい <bpt id="p1">**</bpt>高速クエリの使用<ept id="p1">**</ept> オプションが追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>By default, this option is turned on for most queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定で、ほとんどのクエリでこのオプションが有効になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>If you receive a time-out error after you run a query, turn the <bpt id="p1">**</bpt>Use Fast Query<ept id="p1">**</ept> option off, and then try to run the query again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの実行後にタイム アウト エラーが発生する場合は、<bpt id="p1">**</bpt>高速クエリの使用<ept id="p1">**</ept> オプションをオフにして再度クエリの実行を試みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The query will now run asynchronously.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリは非同期に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> – Shows a list of predefined actions that should be taken to mitigate issues in the sandbox and production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション<ept id="p1">**</ept> – サンド ボックスと製造環境での問題を緩和するために実行する必要がある定義済みアクションの一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Examples of actions include adding/dropping an index, updating stats on a table, rebuilding indexes, and terminating a blocking statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションの例としては、インデックスの追加または削除、テーブルでの統計の更新、インデックスの再構築、ブロック ステートメントの終了があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Any time that an action is performed, the environment history for an environment will show a record for the action performed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを実行するといつでも、環境の環境履歴に実行されるアクションの記録が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>A history record is created only for actions and not when queries are executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">履歴レコードは、クエリの実行時ではなく、アクションにのみ作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Actions<ept id="p1">](./media/Actions.JPG)](./media/Actions.JPG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>アクション<ept id="p1">](./media/Actions.JPG)](./media/Actions.JPG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Performance Metrics<ept id="p1">**</ept> – Shows the most expensive queries that were run in the system during the selected period, based on logical I/O, execution count, duration, CPU time, and wait count.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パフォーマンス メトリックス<ept id="p1">**</ept> - 論理入出力、実行カウント、期間、CPU 時間、および待機数に基づいて、選択した期間にシステムで実行された最もコストのかかったクエリが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This data is queried from the SQL query store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータは SQL クエリ ストアからクエリされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The data is retained for 30 days, and the tool runs its data collection every day at 10:00 PM Coordinated Universal Time (UTC).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データは 30 日間保持され、ツールは毎日、協定世界時 (UTC) の午後 10 時にデータ収集を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To use the tool, select a period during the last 30 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールを使用するには、過去 30 日間の期間を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>When the query results appear, select the bar in the duration chart to highlight where the query falls on other metrics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ結果が表示されたら、期間グラフ内のバーを選択して、クエリが他の基準に該当する場所を強調表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>On the <bpt id="p1">**</bpt>Statement<ept id="p1">**</ept> tab, view the query, or download the query execution plan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステートメント<ept id="p1">**</ept>タブで、クエリを表示、またはクエリの実行計画をダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Performance Metrics<ept id="p1">](./media/perfmetrics.JPG)](./media/perfmetrics.JPG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>パフォーマンス メトリックス<ept id="p1">](./media/perfmetrics.JPG)](./media/perfmetrics.JPG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Index Analysis<ept id="p1">**</ept> – Shows aggregated index and table information, based on user scans, user seeks, user updates, and row count.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インデックス分析<ept id="p1">**</ept> – ユーザーのスキャン、ユーザーのシーク、ユーザーの更新プログラム、および行の数に基づいて、集計インデックスとテーブル情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Like performance metrics, this tool shows the trend for the selected index along with additional table metrics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス測定基準と同様に、このツールは追加のテーブル メトリックスと共に選択したインデックスのトレンドを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Index Analysis<ept id="p1">](./media/IndexAnalysis.JPG)](./media/IndexAnalysis.JPG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>インデックス分析<ept id="p1">](./media/IndexAnalysis.JPG)](./media/IndexAnalysis.JPG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Queries<ept id="p1">**</ept> tab and <bpt id="p2">**</bpt>Actions<ept id="p2">**</ept> tab – For details about the queries that are shown on the <bpt id="p3">**</bpt>Queries<ept id="p3">**</ept> and <bpt id="p4">**</bpt>Actions<ept id="p4">**</ept> tabs, see the <bpt id="p5">[</bpt>Query cookbook<ept id="p5">](querycookbook.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ<ept id="p1">**</ept> タブと <bpt id="p2">**</bpt>アクション<ept id="p2">**</ept> タブ – <bpt id="p3">**</bpt>クエリ<ept id="p3">**</ept> および <bpt id="p4">**</bpt>アクション<ept id="p4">**</ept> タブに表示されるクエリの詳細については、<bpt id="p5">[</bpt>クックブックの照会<ept id="p5">](querycookbook.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>How do I use this feature?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使う方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Go to your project in LCS and open the environment details page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクトに移動し、環境の詳細ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select the <bpt id="p1">**</bpt>Environment Monitoring<ept id="p1">**</ept> link in the <bpt id="p2">**</bpt>Monitoring<ept id="p2">**</ept> section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>監視<ept id="p2">**</ept> セクションで <bpt id="p1">**</bpt>環境監視<ept id="p1">**</ept> リンクを選択します。。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Select the <bpt id="p1">**</bpt>SQL Insights<ept id="p1">**</ept> tab to access this feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL インサイト<ept id="p1">**</ept> タブを選択してこの機能にアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You can navigate to each of the tabs (<bpt id="p1">**</bpt>Live View<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Queries<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Actions<ept id="p3">**</ept>, <bpt id="p4">**</bpt>Performance Metrics<ept id="p4">**</ept>, <bpt id="p5">**</bpt>Index<ept id="p5">**</ept>, <bpt id="p6">**</bpt>Analysis<ept id="p6">**</ept>) to view or query for more information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各タブ (<bpt id="p1">**</bpt>ライブ ビュー<ept id="p1">**</ept>、<bpt id="p2">**</bpt>クエリ<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>アクション<ept id="p3">**</ept>、<bpt id="p4">**</bpt>パフォーマンス メトリックス<ept id="p4">**</ept>、<bpt id="p5">**</bpt>インデックス<ept id="p5">**</ept>、<bpt id="p6">**</bpt>分析<ept id="p6">**</ept>) に移動し、詳細を表示またはクエリ実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You have the option to search or export to Excel any of results from the query execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの実行による結果を検索したり、Excel にエクスポートしたりするオプションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>After you have narrowed down the reason for the performance issue, you can use a predefined action to mitigate the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスの問題の原因を絞り込んだら、事前に定義されたアクションを使用して問題を軽減できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After an action is performed, an entry is made on the <bpt id="p1">**</bpt>Environment History<ept id="p1">**</ept> page, which shows the details of the action, the parameters that were passed in, a timestamp, and who triggered the action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクションを実行すると、<bpt id="p1">**</bpt>環境履歴<ept id="p1">**</ept> ページにエントリが作成されます。アクションの詳細、渡されたパラメーター、タイムスタンプ、アクションをトリガーしたユーザーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Sample flow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル フロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Scenario<ept id="p1">**</ept>: Users report slow performance when using the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>シナリオ<ept id="p1">**</ept>: ユーザーは、システムを使用する場合にパフォーマンスの低下を報告します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>One issue could be a blocking statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの問題はブロック ステートメントの可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Blocking by itself is typical in a healthy system and is only a problem when it becomes excessive or starts degrading business activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正常なシステムでは単独でブロックするのが通常であり、過剰になったり、営業活動に悪影響を及ぼし始めたときのみ問題となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Go to the <bpt id="p1">**</bpt>Live View<ept id="p1">**</ept> tab and check if there are any blocking statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ライブ ビュー<ept id="p1">**</ept> タブに移動し、ブロック ステートメントがないか確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If there is a blocking statement, copy the blocking query ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロック ステートメントがある場合、ブロック クエリ ID をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Open the <bpt id="p1">**</bpt>Queries<ept id="p1">**</ept> tab and select the <bpt id="p2">**</bpt>Current Blocking Tree<ept id="p2">**</ept> query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ<ept id="p1">**</ept> タブを開き、<bpt id="p2">**</bpt>現在のブロック ツリー<ept id="p2">**</ept> クエリを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This will return the root blocker that is blocking the SQL operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL 操作をブロックしているルート ブロッカーが返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To resolve the issue, you can either let it run and clear naturally, or end the process for the lead blocker, which will roll work back.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を解決するには、実行させて自然にクリアさせるか、リード ブロッカーのプロセスを終了して作業をロールバックすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Typically, you should only end the lead blocker process if you think that it will not clear naturally (such as a bad query plan), or in situations where a critical process is unable to run and needs to complete immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、自然にクリアしないとは思われる場合 (不適切なクエリ プランの場合など) や、重要なプロセスを実行できないためにすぐに完了する必要があるような状況でのみリード ブロッカーを終了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Confirm that it's okay to terminate the statements that are currently being executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在実行されているステートメントを終了しても問題がないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Open the <bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> tab and select the <bpt id="p2">**</bpt>End SQL Process<ept id="p2">**</ept> action and pass in the root blocker query ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション<ept id="p1">**</ept> タブを開き、<bpt id="p2">**</bpt>SQL プロセスの終了<ept id="p2">**</ept> アクションを選択して、ルート ブロッカー クエリ ID を渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This will execute a query against the SQL database to terminate the blocking statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ブロック ステートメントを終了するために SQL データベースに対してクエリを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Go to the <bpt id="p1">**</bpt>Queries<ept id="p1">**</ept> tab and run <bpt id="p2">**</bpt>Current blocking query<ept id="p2">**</ept> to verify if the blocking statement was terminated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ<ept id="p1">**</ept> タブに移動し、<bpt id="p2">**</bpt>現在ブロックしているクエリ<ept id="p2">**</ept> を実行して、ブロック ステートメントが終了したかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>You can also check the <bpt id="p1">**</bpt>Environment History<ept id="p1">**</ept> page to see details on what process was terminated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境履歴<ept id="p1">**</ept> ページで、どのプロセスが終了したかの詳細を確認することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To avoid this issue in the future, you should use indexes or plan guides, or turn off lock escalation, or use page locks if processes are blocking each other while operating on different records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来この問題を避けるため、インデックスまたはプラン ガイドを使用したり、ロック エスカレーションをオフにしたり、各種レコードでの操作中にプロセスが互いにブロックしている場合はページ ロックを使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>If processes are operating on the same records, the only way to avoid blocking is by refactoring or rescheduling the processes to not operate on the same records at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスが同じレコードで動作している場合、ブロックを回避するには、同時に同じレコード上で動作しないよう、プロセスをリファクタリングまたは再スケジューリングする必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>