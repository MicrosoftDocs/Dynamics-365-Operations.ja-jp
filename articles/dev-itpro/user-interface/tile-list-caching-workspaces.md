<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="tile-list-caching-workspaces.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>tile-list-caching-workspaces.6c418d.4569a016ebea7ac87d68ee0fb398d06aa09c3272.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4569a016ebea7ac87d68ee0fb398d06aa09c3272</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\tile-list-caching-workspaces.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Tile and list caching for workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのタイルおよびリストのキャッシュ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>It's important that workspaces perform well, and that they be responsive (that is, the data that appears in a workspace is refreshed as expected and kept up to date).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースが正常に機能し、応答可能である (つまり、ワークスペースに表示されるデータが期待どおりに更新され、最新の状態である) ことが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This topic discusses framework support for caching data that is used for tiles and lists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、タイルとリストに使用されるデータをキャッシュするためのフレームワークのサポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Tile and list caching for workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのタイルおよびリストのキャッシュ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It's important that workspaces perform well, and that they be responsive (that is, the data that appears in a workspace is refreshed as expected and kept up to date).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースが正常に機能し、応答可能である (つまり、ワークスペースに表示されるデータが期待どおりに更新され、最新の状態である) ことが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic discusses framework support for caching data that is used for tiles and lists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、タイルとリストに使用されるデータをキャッシュするためのフレームワークのサポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Introduction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はじめに</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Workspaces are intended to be the hub of activity for most users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースは大半のユーザーにとって活動のハブとなるように意図されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>They display a wealth of information that is collected from various sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな情報源から収集された豊富な情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Therefore, you must make sure that workspaces perform well and are responsive (that is, the data shown in the workspace is refreshed as expected and/or kept up to date).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ワークスペースが正常に動作し、応答性があることを確認する必要があります (つまり、ワークスペースに表示されたデータが予想どおりに更新され、最新の状態に維持される)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Caching can help guarantee great workspace performance when data comes from poorly performing queries, and is especially useful when multiple users require access to the same set of data at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュは、パフォーマンスの低いクエリからのデータが得られた場合にワークスペースの優れたパフォーマンスを保証できるようにします。また、複数のユーザーが同じデータ セットに同時にアクセスする必要がある場合に特に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For example, if a grid on a form uses a complex (that is, low-performing) query, you can cache the results so that they are available for subsequent loads of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フォーム上のグリッドが複合 (つまり、低いパフォーマンス) クエリを使用する場合、フォームの以後の積荷に使用できるように結果をキャッシュすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This article discusses framework support for caching data that is used for tiles and lists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、タイルとリストに使用されるデータをキャッシュするためのフレームワークのサポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In terms of a responsive workspace, when users navigate to a workspace (or return to it), they expect that the data in the workspace will be relatively up to date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">応答しやすいワークスペースの観点から、ユーザーがワークスペースに移動した (またはそこに戻った) ときに、ワークスペース内のデータが比較的に最新の状態であることを期待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, if a user takes an action that changes the data for a list or tile in a workspace, the workspace should reflect that change immediately after the action is performed (if the action was taken directly from the workspace) or when the user returns to the workspace form (if the action was taken on a different form).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ユーザーがワークスペースでリストまたはタイルのデータを変更するアクションを実行する場合、ワークスペースはアクションが実行された直後 (アクションがワークスペースから直接実行された場合)、またはユーザーがワークスペース フォームに返す際に (アクションが異なるフォームで実行された場合)、その変更を反映する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This article describes techniques for making sure that this type of data refresh occurs (both metadata and code) for both tiles and lists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、タイルとリストの両方について、このタイプのデータ更新が (メタデータとコードの両方で) 行われるようにするための手法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Count tiles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カウント タイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Automatic data caching</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動データ キャッシング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The framework automatically sets up data caching behind any defined count tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワークは、定義されたカウント タイルの背後に自動的にデータ キャッシングを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Therefore, no extra code is required in this case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この場合には余分なコードは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>A <bpt id="p1">**</bpt>Refresh Frequency<ept id="p1">**</ept> metadata property on Tiles determines how often the count on the tile is automatically updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイル内の<bpt id="p1">**</bpt>更新頻度<ept id="p1">**</ept>のメタデータ プロパティは、タイルのカウントが自動的に更新される頻度を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The following table describes the options and guidance for this property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルでは、このプロパティのオプションとガイダンスについて説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When to use</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用時</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>As Fast As Permissible (5 seconds)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">できる限り速く (5 秒)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Query execution time is 25 ms or less, and there is demand to see the updated value all the time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの実行時間は 25 ミリ秒以下であり、常に更新された値を表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>10 Minutes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10 分</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Query execution time is less than 250 ms, and updated data must be seen periodically</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの実行時間は 250 ミリ秒未満であり、更新されたデータを定期的に表示する必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>24 Hours</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">24 時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Query execution time is less than 2000 ms, and/or the count isn't expected to change often or up-to-date counts are vital.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの実行時間は 2000 ミリ秒未満であり、カウントの変更は予期されていないか、最新のカウントが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Refresh management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Count tiles that show values that represent pending work should be fairly responsive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保留中の作業を表す値を示すカウント タイルは、かなり反応的でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Ideally, the fastest possible refresh frequency should be defined for these tiles, so that the count that appears on a workspace tile is always within five seconds of being up to date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理想的には、ワークスペース タイルに表示されるカウントが常に最新の 5 秒以内になるように、可能な限り早いリフレッシュ頻度をこれらのタイルに対して定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Because this quick refresh rate should be set only on performant queries (queries that have an execution time of less than 25 ms), the first recommendation is that you work on query performance for count tiles, to try to get query execution under the 25-ms threshold.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクイック更新頻度はパフォーマンス クエリ (実行時間が 25 ミリ秒未満のクエリ) でのみ設定する必要があるため、最初の推奨事項はカウント タイルのクエリのパフォーマンスを操作して、25 ミリ秒のしきい値未満でクエリの実行を取得するために試行することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In general, achieving this execution speed requires two things:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、この実行速度を実現するためには、次の 2 つが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A selective WHERE condition on the query Preferably, the conditions on the query should reduce the result set to fewer than ~500 records, and ideally to fewer than ~100 rows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリで選択的な WHERE 条件であるクエリの条件は、できれば結果セットを 500 レコード未満に、理想的には 100 行未満に減らす必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>An index structure that can act on the selective WHERE condition</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択的な WHERE 条件に対応できるインデックス構造</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>See the "Common mistakes and tips for query optimization" section for details about how to evaluate and improve query performance to achieve these execution speeds.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの実行速度を達成するためにクエリのパフォーマンスを改善する方法については、「よくある間違いとクエリを最適化するためのヒント」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For tiles that have backing queries and can't meet the 25-ms execution speed threshold, the refresh frequency on the tile should be set to one of the lower values (for example, 10 minutes or 24 hours).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリのバッキングがあり、25 ミリ秒実行速度のしきい値を満たすことができないタイルについては、タイルでの更新頻度を低い値のいずれかに設定する必要があります (たとえば、10 分または 24 時間)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>If the values must be updated more frequently for tiles that have less-efficient queries (which should be rare), you can add the following code to manually refresh the cache when an action is taken that will affect the cached set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より効率の低いクエリ (まれである) を持つタイルの値を頻繁に更新する必要がある場合は、次のコードを追加して、キャッシュされたセットに影響するアクションが発生したときにキャッシュを手動で更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>An example of a data set that might not change often is products that have no configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">頻繁に変更されないデータ セットの例としては、コンフィギュレーションがない製品です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>A tile that shows this count might have a refresh frequency of 10 minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカウントを示すタイルは、10 分の更新頻度があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>However, the tile count might still appear responsive if the products form is instrumented to force-refresh the data cache when a configuration is defined for a product that previously had no configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、以前にコンフィギュレーションされていなかった製品に対するコンフィギュレーションが定義される場合、データ キャッシュを強制更新するよう商品フォームが計測されると、タイル カウントは依然として応答しているように見える場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Workspace lists</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース リスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Although the framework automatically sets up data caches for count tiles, manual setup is required for lists that must use data caching.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フレームワークは自動的にカウント タイルのためのデータ キャッシュを設定しますが、データ キャッシュを使用する必要のあるリストでは手動の設定が必須です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Here are the high-level steps for introducing cached data for a list:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧のキャッシュされたデータを導入するための高レベルの手順を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Create a query that references all the columns that you want in the cached data set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュされたデータ セットに必要なすべての列を参照するクエリを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Create a table that contains all the fields that you want to cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュするすべてのフィールドを含むテーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Create a class that defines a mapping between the cache query and cache table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ クエリとキャッシュ テーブルの間のマッピングを定義するクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Add/reference the cached table as a data source on your form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデータ ソースとしてキャッシュされたテーブルを追加/参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Each of these steps is described in detail in the following sections and is paired with an example from the Fleet workspace (Reservation Management).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順はそれぞれ、次のセクションで詳細が説明され、フリート ワークスペース (予約管理) の例と対になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Cache query</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ クエリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>First, you must create a query that will be used to populate the cache table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、キャッシュ テーブルを設定するために使用するクエリを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This query should have the following characteristics:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリには、次の特性が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>It should be against the tables that you want to get your cache data from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはキャッシュ データを取得するテーブルに対して設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It should limit the results to the results that you’re actually interested in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際に興味のある結果に結果を制限する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>It should select only the fields that you want to cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュするフィールドのみを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> Each data source should have <bpt id="p2">**</bpt>DynamicFields<ept id="p2">**</ept><ph id="ph1">=</ph><bpt id="p3">**</bpt>No<ept id="p3">**</ept> to avoid extraneous fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 無関係のフィールドを避けるには、各データソースで <bpt id="p2">**</bpt>DynamicFields<ept id="p2">**</ept><ph id="ph1">=</ph><bpt id="p3">**</bpt>いいえ<ept id="p3">**</ept>とする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Cache table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Next, you must define a table that contains a set of fields that match the fields from the cache query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、キャッシュ クエリのフィールドと一致するフィールドのセットが含まれるテーブルを定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In addition to those fields, you must also add a field that is named <bpt id="p1">**</bpt>SysDataCacheContextId<ept id="p1">**</ept> (Int64).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフィールドに加えて、<bpt id="p1">**</bpt>SysDataCacheContextId<ept id="p1">**</ept> (Int64) という名前のフィールドも追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This field is used to map the cache row to the base cache tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、キャッシュ行を基本キャッシュ テーブルにマッピングするために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>You'll define a mapping on the table, between the SysDataSetCacheTableMap table’s <bpt id="p1">**</bpt>Id<ept id="p1">**</ept> and <bpt id="p2">**</bpt>SysDataCacheContextId<ept id="p2">**</ept> fields and the cache table’s <bpt id="p3">**</bpt>RecId<ept id="p3">**</ept> and <bpt id="p4">**</bpt>SysDataCacheContextId<ept id="p4">**</ept> fields, respectively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysDataSetCacheTableMap テーブルの <bpt id="p1">**</bpt>Id<ept id="p1">**</ept> と <bpt id="p2">**</bpt>SysDataCacheContextId<ept id="p2">**</ept> フィールド間、およびキャッシュ テーブルの <bpt id="p3">**</bpt>RecId<ept id="p3">**</ept> と <bpt id="p4">**</bpt>SysDataCacheContextId<ept id="p4">**</ept> フィールド間のそれぞれのマッピングを、テーブル上で定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>You can also define relations between this table and others, in addition to data methods that use the cached fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、キャッシュされるフィールドを使用するデータ メソッドに加え、このテーブルと他のテーブル間の関係を定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Cache class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The third step is to create a class that defines the relationship between the cache query and the cache table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 番目のステップは、キャッシュ クエリとキャッシュ テーブルの間のリレーションシップを定義するクラスを作成することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This class requires that a few attributes be defined, and it must also extend and implement the appropriate framework data caching classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスでは、いくつかの属性を定義する必要があり、適切なフレームワーク データ キャッシング クラスを拡張して実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The following code shows the corresponding class from the Reservation Management workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードは、予約管理ワークスペースの対応するクラスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In some circumstances, you might also have to implement the <bpt id="p1">**</bpt>parmQueryableToCacheMapping()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">状況によっては、<bpt id="p1">**</bpt>parmQueryableToCacheMapping()<ept id="p1">**</ept> メソッドを実装しなければならない場合もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This method is required when at least one column name in your cache table doesn't match the name of the corresponding column in the backing table (for example, if you must add two fields that have the same name but are from different tables).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、キャッシュ テーブル内の少なくとも 1 つの列名が、バッキング テーブル内の対応する列の名前と一致しない場合に必要です (たとえば、名前は同じですが異なるテーブルの 2 つのフィールドを追加する必要がある場合など)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>In this case, you can implement this method to define the column mapping between the cache table and the backing tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、キャッシュ テーブルとバッキング テーブルの間で列マッピングを定義するためにこのメソッドを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The syntax is the same as the syntax for the <bpt id="p1">**</bpt>Query::Insert<ph id="ph1">\_</ph>RecordSet()<ept id="p1">**</ept> method (<ph id="ph2">&lt;https://msdn.microsoft.com/en-us/library/query.insert_recordset.aspx&gt;</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文は、<bpt id="p1">**</bpt>Query::Insert<ph id="ph1">\_</ph>RecordSet()<ept id="p1">**</ept> メソッド (<ph id="ph2">&lt;https://msdn.microsoft.com/en-us/library/query.insert_recordset.aspx&gt;</ph>) の構文と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Form implementation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>After you've built your cache query, table, and class, you’re ready to use the cache on your form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュ クエリ、テーブル、およびクラスを作成した後、フォーム上でキャッシュを使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Add the cache table to your form as a data source, and reference it just as you would reference any other data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースとして、フォームにキャッシュ テーブルを追加し、その他のデータ ソースを参照する場合と同様に、それを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In order for the form to correctly take advantage of caching, some code is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームが正しくキャッシュを利用するには、いくつかのコードが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>In a <bpt id="p1">**</bpt>registerDatasourceOnQueryingEvent()<ept id="p1">**</ept> method, add an event handler to the data source’s <bpt id="p2">**</bpt>OnQueryExecuting<ept id="p2">**</ept> event that calls <bpt id="p3">**</bpt>prepareDataSet<ept id="p3">**</ept>,.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>registerDatasourceOnQueryingEvent()<ept id="p1">**</ept> メソッドで、<bpt id="p3">**</bpt>prepareDataSet<ept id="p3">**</ept> を呼び出すデータ ソースの <bpt id="p2">**</bpt>OnQueryExecuting<ept id="p2">**</ept> イベントにイベント ハンドラーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>This requires that the form class implement <bpt id="p1">**</bpt>SysIDataSetConsumerForm<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、フォーム クラスが <bpt id="p1">**</bpt>SysIDataSetConsumerForm<ept id="p1">**</ept> を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>If you want the form to use filtering, as provided by a workspace-wide filter, in a <bpt id="p1">**</bpt>registerDatasourceOnQueryingEvent()<ept id="p1">**</ept> method, register <bpt id="p2">**</bpt>applyFilter<ept id="p2">**</ept> on the <bpt id="p3">**</bpt>OnQueryExecuting<ept id="p3">**</ept> event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>registerDatasourceOnQueryingEvent()<ept id="p1">**</ept> メソッドで、フォームでフィルタリングを使用するようにするには、<bpt id="p3">**</bpt>OnQueryExecuting<ept id="p3">**</ept> イベントで <bpt id="p2">**</bpt>applyFilter<ept id="p2">**</ept> を登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This requires that the form class implement <bpt id="p1">**</bpt>SysIFilterConsumerForm<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、フォーム クラスが <bpt id="p1">**</bpt>SysIFilterConsumerForm<ept id="p1">**</ept> を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>If the form must react when a parent form’s filters change (for example, a workspace-wide filter), implement <bpt id="p1">**</bpt>SysIFilterEventHandler<ept id="p1">**</ept> on the form class, and include an <bpt id="p2">**</bpt>onFilterChanged()<ept id="p2">**</ept> method that calls <bpt id="p3">**</bpt>executeQuery()<ept id="p3">**</ept> on the cache data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームが、親フォームのフィルター (例えば、ワークスペース全体のフィルター) の変更時に対応する必要がある場合、<bpt id="p1">**</bpt>SysIFilterEventHandler<ept id="p1">**</ept> をフォーム クラスに含め、キャッシュ データ ソースで <bpt id="p3">**</bpt>executeQuery()<ept id="p3">**</ept> メソッドを呼び出す <bpt id="p2">**</bpt>onFilterChanged()<ept id="p2">**</ept> を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The following code is an example from the <bpt id="p1">**</bpt>FMPickingUpTodayPart<ept id="p1">**</ept> form, which is one of the tabbed lists on the Reservation Management workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードは、<bpt id="p1">**</bpt>FMPickingUpTodayPart<ept id="p1">**</ept> フォームの例です。これは、予約管理ワークスペースのタブ付きリストの1つです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Additional examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In addition to the previous examples, you can refer to <bpt id="p1">**</bpt>SysFoundationTestOpenHeaderDataset<ept id="p1">**</ept>, which is used on <bpt id="p2">**</bpt>SysFoundationTestOpenHeadersFormPart<ept id="p2">**</ept> (which is itself referenced in <bpt id="p3">**</bpt>SysFoundationTestWorkspace<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の例に加えて、<bpt id="p1">**</bpt>SysFoundationTestOpenHeaderDataset<ept id="p1">**</ept> を参照でき、これは <bpt id="p2">**</bpt>SysFoundationTestOpenHeadersFormPart<ept id="p2">**</ept> (<bpt id="p3">**</bpt>SysFoundationTestWorkspace<ept id="p3">**</ept> で参照されているそのもの) で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>This form uses the same method that is described earlier, but also includes some caching of a query aggregate count.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフォームは、前述の同じメソッドを使用しますが、クエリ集計カウントのキャッシュも含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Refresh management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Lists of data in workspaces should also be responsive to user actions, especially if those actions cause records to no longer meet the criteria for appearing in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース内のデータのリストは、特にユーザー アクションによってレコードがリストで表示する基準を満たさなくなった場合に、ユーザー アクションに対して応答する必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>For example, you have a list of car rentals that are scheduled to start today.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、今日開始予定のレンタカーの一覧があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Every time that an employee initiates a rental record from that list with a customer, that record should no longer appear in the workspace list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従業員が顧客と一緒にそのリストからレンタル・レコードを開始するたびに、そのレコードはワークスペース・リストに表示されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Two mechanisms are available for keeping this list up to date:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この一覧を最新の状態に保つために、2 つのメカニズムが利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>If the user takes an action that removes the record from the list, code can be added to guarantee that the list is immediately updated by refreshing the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが、一覧からレコードを削除するアクションをとると、データ ソースを更新することで、リストが直ちに更新されることを保証するコードを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If the data source is a cache data source, and the refresh frequency is slow, you might want to delete the corresponding records from the cache data source before you call <bpt id="p1">**</bpt>refresh<ept id="p1">**</ept>, to avoid having to force-refresh the cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースがキャッシュのデータ ソースであり、更新の頻度が遅い場合は、<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>を呼び出す前に、キャッシュ データ ソースから対応するレコードを削除すれば、キャッシュを強制的にリフレッシュする必要がなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>If the first option doesn't meet your requirements, you can asynchronously refresh form parts at a time interval.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のオプションが要件を満たしていない場合は、時間間隔でフォーム パーツを非同期で更新できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>This option can be set up by using the <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> property on the FormPart control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、FormPart コントロールの <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> プロパティを使用して設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For workspaces that have user interaction, the cache refresh frequency should be set based on query performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー操作のあるワークスペースについては、キャッシュの更新頻度をクエリ パフォーマンスに基づいて設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In this case, the current recommendation is to not set the <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、現在の推奨は <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> を設定しないことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Instead, rely on the user to manually refresh the workspace to bring in more data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、ユーザーに依存してより多くのデータをもたらすためにワークスペースを手動で更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Alternatively, you consider using an infrequent auto-refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、頻度の低い自動更新の使用を考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>However, in this case, the user’s current selection will not be retained if the list is updated while the user is interacting with it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この場合は、ユーザーがやり取りしている間にリストが更新される場合、ユーザーの現在の選択内容は保持されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>A small percentage of workspaces are intended for viewing purposes only (no user interaction).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの小さなパーセンテージは、表示のみを目的としています (ユーザーの操作なし)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>These workspaces should use set the <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> property programmatically to match the current refresh frequency of the backing cache.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのワークスペースでは、<bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> プロパティをプログラムで設定して、バックアップ キャッシュの現在の更新頻度を一致させる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>(Use <bpt id="p1">**</bpt>SysIDataCacheConfiguration.parmRefreshFrequency()<ept id="p1">**</ept> to retrieve the current refresh frequency of a cache, because it can be modified by the system administrator at run time.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(実行時にシステム管理者によって変更できるため、<bpt id="p1">**</bpt>SysIDataCacheConfiguration.parmRefreshFrequency()<ept id="p1">**</ept> を使用してキャッシュの現在の更新頻度を取得します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>FormParts that have Charts should set the <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> property to periodically show updated chart data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グラフがある FormParts は <bpt id="p1">**</bpt>AutoRefreshInterval<ept id="p1">**</ept> プロパティを設定し、定期的に更新されたグラフ データをを表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Common mistakes and tips for query optimization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの最適化に関するよくある間違いやヒント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Here a few general guidelines to consider when you optimize queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリを最適化するときに考慮するいくつかの一般的なガイドラインを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>This isn't an extensive guide to query optimization but provides just a few simple guiding principles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、クエリ最適化の広範なガイドではありませんが、いくつかの簡単なガイドラインを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>Trace the statement by using SQL Profiler.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL プロファイラーを使用して、明細書を追跡してください。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Attach the Microsoft SQL Server Profiler to the database, and capture the SQL statement that you want to optimize.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server プロファイラーをデータ ベースに接続し、最適化する SQL ステートメントをキャプチャします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can use the tuning template that is provided in a default installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のインストールで提供されている調整テンプレートを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Don’t forget to disable tracing after you've obtained the statement that you're interested in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">興味のある明細書を入手した際は、トレースを無効にすることを忘れないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For more information, see <ph id="ph1">&lt;https://msdn.microsoft.com/en-us/library/ms175047.aspx&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<ph id="ph1">&lt;https://msdn.microsoft.com/en-us/library/ms175047.aspx&gt;</ph>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">**</bpt>Always look at the query plan.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ計画を常に確認します。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In Microsoft SQL Server Management Studio, make sure that you've enabled <bpt id="p1">**</bpt>Include actual Execution Plan<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Management Studio で、<bpt id="p1">**</bpt>実際の実行計画を含む<ept id="p1">**</ept>を有効にしたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Look at the query plan, and watch out for any warnings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ プランを確認し、警告に注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The thickness of the arrows indicate how many rows have been fetched and brought to the next step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">矢印の太さは、フェッチされて次のステップに移動された行の数を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>Compare CPU milliseconds and logical I/O.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CPU のミリ秒と論理 I/O を比較します。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>One good way to determine whether a change to a given SQL statement improved the statement is to look at the logical I/O and CPU milliseconds.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の SQL ステートメントへの変更が、ステートメントを改善したかどうかを決定する良い方法の 1 つは、論理 I/O と CPU のミリ秒を確認することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>To obtain these numbers, use the following statements in the query editor:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの数値を取得するには、クエリ エディターで次のステートメントを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>set statistics time on</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">set statistics time on</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>set statistics io on</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">set statistics io on</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">**</bpt>Always clear caches when you measure a statement.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>明細書を測定するときは、常にキャッシュをクリアします。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>To make sure that Microsoft SQL Server isn't using a cached execution plan, it's advisable that you flush the cache when you rerun a statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server がキャッシュされた実行計画を使用していないことを確認するには、命令文を再実行するときにキャッシュをフラッシュすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>To flush the cache, run the following two commands:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャッシュをフラッシュするには、次の 2 つのコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>dbcc dropCleanBuffers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dbcc dropCleanBuffers</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>dbcc freeProcCache</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dbcc freeProcCache</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">**</bpt>Here are some common patterns to watch out for:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意すべきいくつかの一般的なパターンを次に示します。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">**</bpt>Missing index:<ept id="p1">**</ept> Analyze your WHERE conditions, and make sure that a selective index exists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インデックスがありません:<ept id="p1">**</ept> WHERE 条件を分析して、選択したインデックスが存在するかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source><bpt id="p1">**</bpt>Processing the same table/row many times:<ept id="p1">**</ept> Especially when you do joins, try not to repeat yourself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>同じテーブル/行の多数の処理:<ept id="p1">**</ept> 特に結合するときは、繰り返しをしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Minimize the number of times that the same table/row must be processed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じテーブル/行を処理する必要がある回数を最小化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If you have tables that must be part of the result set but aren't used to narrow down the result set, move them as far out as possible (especially in union queries).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果セットの一部であるはずのテーブルがあり、結果セットを絞り込むために使用されていない場合は、(特にユニオン クエリーでは) それらを可能な限り遠くに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><bpt id="p1">**</bpt>Test on volume data.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データの量をテスト。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>To identify issues in your query, always run it on volume data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリの問題を特定するには、常にボリューム データに対して実行します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>