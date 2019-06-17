<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-trace-tutorial.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-trace-tutorial.16d0f6.42768ff7b45d9051738e0ca26e3ab3b4eb7296e6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>42768ff7b45d9051738e0ca26e3ab3b4eb7296e6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\perf-test\trace-trace-tutorial.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Take traces by using Trace parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser を使用してトレースを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial provides guidelines on how to take traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、トレースする方法についてのガイドラインを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Take traces by using Trace parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser を使用してトレースを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial provides guidelines on how to take traces in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Microsoft Dynamics 365 for Finance and Operations でトレースする方法についてのガイドラインを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this tutorial, you'll take a tour of how to collect and download traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、トレースの収集およびダウンロード方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The trace analysis tool works largely similar to the Microsoft Dynamics AX 2012 version, but it is not backward compatible and can't be used to analyze AX 2012 traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレース分析ツールは、Microsoft Dynamics AX 2012 バージョンとほぼ同じように機能しますが、後方互換性はなく、AX 2012 トレースの分析には使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The trace parser tool can be found in the PerfSDK folder on your development deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレース パーサー ツールは、開発環境の PerfSDK フォルダーにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This tutorial requires that you access the environment as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、インスタンスの管理者として環境にアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The administrator can also grant rights to other users to take a trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、トレースを実行する権限を他のユーザーに付与することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In this way you can trace scenarios which can't be reproduced with administrative rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、管理者権限で再現できないシナリオを追跡することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Capture the trace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレースをキャプチャする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Before you trace make sure your scenario is in a "Warm" state meaning you executed the scenario you want to trace once before you take the trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレースする前にシナリオが「ウォーム」状態になっていることを確認します。トレースを取得する前に一度トレースするシナリオを実行したことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>That will prevent things like metadata loading and other possible warm up tasks from being in the trace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータの読み込みや他の考えられるウォームアップ タスクなどの操作が、トレースで行われることがなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the navigation bar, select <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Trace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション バーで、<bpt id="p1">**</bpt>設定<ept id="p1">**</ept>を選択して<bpt id="p2">**</bpt>トレース<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trace1<ept id="p1">](./media/trace1-300x176.jpg)](./media/trace1.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trace1<ept id="p1">](./media/trace1-300x176.jpg)](./media/trace1.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Name the trace that you are about to capture, and then click <bpt id="p1">**</bpt>Start trace<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプチャするトレースに名前を付けてから、<bpt id="p1">**</bpt>追跡の開始<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Perform actions that need to be analyzed like for example opening "Accounts payable <ph id="ph1">&amp;gt;</ph> Vendors <ph id="ph2">&amp;gt;</ph> All vendors".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば [買掛金勘定] <ph id="ph1">&amp;gt;</ph> [仕入先] <ph id="ph2">&amp;gt;</ph> [すべての仕入先] を開くなど、分析する必要があるアクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When you are finished, click <bpt id="p1">**</bpt>Stop trace<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、<bpt id="p1">**</bpt>追跡の停止<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Then, you can select one of the following options (for this tutorial, select the second option):</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、次のいずれかのオプションを選択できます (このチュートリアルでは、2 番目のオプションを選択します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Download trace<ept id="p1">**</ept> – Store the captured trace on a local machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トレースのダウンロード<ept id="p1">**</ept> - キャプチャしたトレースをローカル マシンに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You can analyze a downloaded trace with the desktop version of Trace Parser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser のデスクトップ バージョンでダウンロードしたトレースを分析することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: If you download a trace it will not be available for later uploading.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: トレースをダウンロードすると、後でアップロードすることができなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Upload trace<ept id="p1">**</ept> – Store the trace in the cloud for later downloading by for example the admin, it will be automatically deleted after 7 days and can also be deleted manually from the captured traces form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トレースのアップロード<ept id="p1">**</ept> – 管理者などによって後でダウンロードするためにクラウドに追跡が保存され、7 日後に自動的に削除され、キャプチャされたトレース フォームから手動でも削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Please note:<ept id="p1">**</ept> If your scenario takes more than 1-2 minutes it is better to try to take multiple smaller traces of 30 seconds each as the trace will likely get too big to be easily analyzed and there is a risk for losing data if the trace gets too big.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意してください:<ept id="p1">**</ept> シナリオが 1 〜 2 分以上かかる場合は、トレースが大きすぎて分析しにくく、トレースが大きくなりすぎるとデータを失う危険があるため、それぞれ 30 秒の複数の小さなトレースを取ることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Assign trace rights to user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーにトレース権限を割り当てます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>To give a user rights to capture a trace, go to "System administration <ph id="ph1">&amp;gt;</ph> Users <ph id="ph2">&amp;gt;</ph> Users".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーにトレースをキャプチャする権利を与えるには、"システム管理<ph id="ph1">&amp;gt;</ph>ユーザー<ph id="ph2">&amp;gt;</ph>ユーザー" を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Select the user and assign the "System tracing user" role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーを選択し、"システム追跡ユーザー" ロールを割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>trace2<ept id="p1">](./media/trace2-284x300.jpg)](./media/trace2.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>trace2<ept id="p1">](./media/trace2-284x300.jpg)](./media/trace2.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Remove the user role again once the user is done with tracing to avoid unwanted tracing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが不要なトレースを回避するために追跡を行ったら、ユーザー ロールを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Open captured trace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプチャされたトレースを開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the navigation bar, select <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Trace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション バーで、<bpt id="p1">**</bpt>設定<ept id="p1">**</ept>を選択して<bpt id="p2">**</bpt>トレース<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Click on Captured traces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプチャされたトレースをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The captured traces button can only be seen by users with administrative rights.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> キャプチャされたトレース ボタンは、管理者権限を持つユーザーだけが表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Click on the trace name to download to open and analyze it with the desktop version of trace parser or</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロードする追跡名をクリックして、デスクトップ バージョンの Trace Parser または で開いて分析します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Click on the user name to get to the user options.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー オプションを表示するには、ユーザー名をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Delete the trace if you want.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じてトレースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>You might do this if you have downloaded it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンロードした場合には、これを行う場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The trace will be deleted after 7 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> トレースは、7 日後に削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For more information about the desktop version of trace parser, see <bpt id="p1">[</bpt>Trace parser: Using the desktop version to diagnose problems and analyze performance issues<ept id="p1">](trace-parser.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser のデスクトップ バージョンの詳細については、<bpt id="p1">[</bpt>Trace parser: デスクトップ バージョンを使用した問題点の診断およびパフォーマンスの問題の分析<ept id="p1">](trace-parser.md)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>