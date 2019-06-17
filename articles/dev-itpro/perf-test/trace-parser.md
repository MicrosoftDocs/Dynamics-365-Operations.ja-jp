<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-parser.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-parser.85a85e.fba6b140d68f5949429a2daa683db25294284964.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>fba6b140d68f5949429a2daa683db25294284964</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\trace-parser.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Diagnose issues and analyze performance by using Trace parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can use the Trace parser to consume traces and analyze performance in your deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トレース パーサーを使用してトレースを操作し、展開におけるパフォーマンスを分析する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Diagnose issues and analyze performance by using Trace parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser を使用した問題点の診断およびパフォーマンスの分析</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how you can use the Trace parser to consume traces and analyze performance in your Microsoft Dynamics 365 for Finance and Operations deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トレース パーサーを使用してトレースを操作し、Microsoft Dynamics 365 for Finance and Operations の展開におけるパフォーマンスを分析する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You can use the Trace Parser to find and diagnose various types of errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser を使用すると、さまざまな種類のエラーを見つけて診断することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can also use the tool to visualize execution of X++ methods, as well as the execution call tree.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">また、ツールを使用して X++ メソッドの実行、および実行コール ツリーを視覚化することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>There are many more features in the Trace parser are similar to Microsoft Dynamics AX 2012.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Trace parser には Microsoft Dynamics AX 2012 と類似する機能が多数あります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>See the <bpt id="p1">[</bpt>Dynamics Ax Performance Team Blog<ept id="p1">](https://blogs.msdn.com/axperf)</ept> for more information.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">詳細については、 <bpt id="p1">[</bpt>Dynamics Ax Performance チーム ブログ<ept id="p1">](https://blogs.msdn.com/axperf)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Finding the Trace parser</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Trace Parser の検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Trace parser should be preinstalled with your developer deployment or VHD.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">トレース パーサーには、開発者展開または VHD があらかじめインストールされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The install location is here: C:<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics AX<ph id="ph3">\\</ph>Microsoft.Dynamics.AX.Tracing.TraceParser.exe In case it is not installed you can find the "traceparser.msi" in C:<ph id="ph4">\\</ph>PerfSDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストール場所は次のとおりです。C:<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics AX<ph id="ph3">\\</ph>Microsoft.Dynamics.AX.Tracing.TraceParser.exe インストールされていない場合は、C:<ph id="ph4">\\</ph>PerfSDK に「traceparser.msi」が見つかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If the for any reason the PerfSDK is not installed you can find the .msi here: C:<ph id="ph1">\\</ph>Services<ph id="ph2">\\</ph>PerfSDK<ph id="ph3">\\</ph>Scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">何らかの理由で PerfSDK がインストールされていない場合は、ここで .msi を検索できます: c:<ph id="ph1">\\</ph>Services<ph id="ph2">\\</ph>PerfSDK<ph id="ph3">\\</ph>Scripts</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Capturing events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントのキャプチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>There are two ways that you can obtain the data that you will analyze in the Trace parser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレース パーサーで分析するデータを取得するには、2 つの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>They include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のものが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Capture events from the local installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカルのインストールからイベントをキャプチャします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the <bpt id="p1">**</bpt>Select Trace<ept id="p1">**</ept> window isn’t already open, go to the <bpt id="p2">**</bpt>File<ept id="p2">**</ept> menu and click <bpt id="p3">**</bpt>Open trace<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トレースの選択<ept id="p1">**</ept>ウィンドウが開いていない場合、<bpt id="p2">**</bpt>ファイル<ept id="p2">**</ept> メニューに移動し、<bpt id="p3">**</bpt>トレースを開く<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In the <bpt id="p1">**</bpt>Select Trace<ept id="p1">**</ept> window, click <bpt id="p2">**</bpt>Capture Events<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追跡の選択<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>イベントのキャプチャ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>After selecting your providers, click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーを選択して、<bpt id="p1">**</bpt>開始<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The Trace Parser tool will start listening to all the providers and capturing the events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser ツールは、すべてのプロバイダーのリッスンとイベントのキャプチャを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Capturing stops when you click <bpt id="p1">**</bpt>Stop and Import<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>停止およびインポート<ept id="p1">**</ept>をクリックするとキャプチャは停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Open an existing ETL (Windows Event) file that was captured using tools such as Logman.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Logman などのツールを使用してキャプチャされた、既存の ETL(Windows イベント) ファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>1<ph id="ph2">\_</ph>Desktop<ept id="p1">](./media/1_desktop.png)](./media/1_desktop.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>1<ph id="ph2">\_</ph>デスクトップ<ept id="p1">](./media/1_desktop.png)](./media/1_desktop.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Viewing traces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレースの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Timeline view<ept id="p1">**</ept> The Timeline tab is the first tab that you see after you import a trace into the Trace Parser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイムライン ビュー<ept id="p1">**</ept> タイムライン タブは、Trace Parser にトレースをインポートした後に表示される最初のタブです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This tab is shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタブは、次の図に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>2<ph id="ph2">\_</ph>Desktop<ept id="p1">](./media/2_desktop.png)](./media/2_desktop.png)</ept> The <bpt id="p2">**</bpt>Timeline<ept id="p2">**</ept> tab has the following major components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>2<ph id="ph2">\_</ph>デスクトップ<ept id="p1">](./media/2_desktop.png)](./media/2_desktop.png)</ept>、<bpt id="p2">**</bpt>タイムライン<ept id="p2">**</ept>タブには、次の主要なコンポーネントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The <bpt id="p1">**</bpt>Select Grouping<ept id="p1">**</ept> drop-down allows you to group based on a variety of categories, such as Customer ID, Username, Session Name, etc. Groupings will display maximum and minimum timestamp of events, total number of events, and lowest event level within the grouping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>グループ化を選択<ept id="p1">**</ept> ドロップダウンでは、さまざまなカテゴリ (顧客 ID、ユーザー名、セッション名など) に基づいてグループ化できます。[グループ化] には、イベントの最大および最小タイムスタンプ、イベントの合計数、グループ内の最下位イベント レベルが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>List of all events in a threaded or unthreaded view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スレッドまたはスレッドではないビューのすべてのイベントのリスト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Property grid displayed for the selected event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したイベントに表示されるプロパティ グリッド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Timeline chart for all the selected events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したすべてのイベントのタイムライン チャートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Filtering of events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントのフィルター処理。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Session analysis notes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セッション分析メモ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Call tree view<ept id="p1">**</ept> By selecting the <bpt id="p2">**</bpt>Call Tree<ept id="p2">**</ept> tab, you can see the call tree for all X++ methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>呼び出しツリーの表示<ept id="p1">**</ept> <bpt id="p2">**</bpt>呼び出しツリー<ept id="p2">**</ept>タブを選択すると、すべての X++ メソッドの呼び出しツリーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The tab is shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タブは、次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ph id="ph2">\_</ph>Desktop<ept id="p1">](./media/3_desktop.png)](./media/3_desktop.png)</ept> Similarly, you can display the <bpt id="p2">**</bpt>X++<ept id="p2">**</ept> tab to view a list of all the X++ methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>3<ph id="ph2">\_</ph>デスクトップ<ept id="p1">](./media/3_desktop.png)](./media/3_desktop.png)</ept>同様に、<bpt id="p2">**</bpt>X++<ept id="p2">**</ept> タブを表示し、すべての X++ メソッドの一覧を表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>They will be sorted by fields such as Inclusive/Exclusive durations, RPC, or Database calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">包括的/排他的な期間、RPC、データベース呼び出しなどのフィールドでソートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Note that these are similar to the corresponding tabs in Trace Parser and have the same behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは Trace Parser の対応するタブに類似しており、同じ動作をすることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt>Developer home page<ept id="p1">](../dev-tools/developer-home-page.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>開発者ホーム ページ<ept id="p1">](../dev-tools/developer-home-page.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>