<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="gantt-development-guide.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>gantt-development-guide.f6a98e.90659ea7fb0eb6cbfa6ac7ce7e0deedcfab2e7c4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>90659ea7fb0eb6cbfa6ac7ce7e0deedcfab2e7c4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\gantt-development-guide.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Gantt control development guide</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガント管理作成ガイド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to create new forms by using the Gantt control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Gantt コントロールを使用して新しいフォームを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Gantt control development guide</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガント管理作成ガイド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how to create new forms by using the Gantt control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Gantt コントロールを使用して新しいフォームを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>We highly recommend that you look at the code in the Tutorial_Gantt form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tutorial_Gantt フォームにあるコードを調べることを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This code demonstrates the full capabilities of the Gantt control, and shows how to load data and work with the application programming interface (API).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、Gantt コントロールのすべての機能を示し、データをロードしてアプリケーション プログラミング インターフェイス (API) を操作する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>What’s new for Gantt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガント チャートの新機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In Microsoft Dynamics AX 2012, the client was a Win32 application, and extensions used Microsoft ActiveX, WinForm, or Microsoft Windows Presentation Foundation (WPF) controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、クライアントは Win32 アプリケーションで、拡張機能は Microsoft ActiveX、WinForm、または Microsoft Windows Presentation Foundation (WPF) のコントロールを使用していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>ActiveX and ManagedHost controls can no longer be used to add custom controls, because they are incompatible with the HTML-based platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ActiveX と ManagedHost コントロールは、HTML ベースのプラットフォームと互換性がないため、カスタム コントロールを追加するためには使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Instead, a new extensible control framework lets you add controls by using HTML and JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、新しい拡張可能コントロール フレームワークで HTML と JavaScript を使用してコントロールを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new Gantt control is implemented by using this framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいガント管理は、このフレームワークを使用して実装されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Note that, unlike in earlier versions, you don't have to pay an additional license fee to use the control in your own forms or to extend the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンとは異なり、独自のフォームの使用およびコントロールの拡張に追加のライセンス手数料を支払う必要はないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>High-level overview of the control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの高レベルの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The following illustration shows the visual elements of the Gantt control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、ガント管理の視覚的要素を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Elements of the Gantt<ept id="p1">](./media/ganttchartelements.png)](./media/ganttchartelements.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ガントの要素<ept id="p1">](./media/ganttchartelements.png)](./media/ganttchartelements.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>To add the control to a new form, just right-click the top node in the form design, and then select <bpt id="p1">**</bpt>Add new<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Gantt<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールを新しいフォームに追加するには、フォーム デザインの一番上のノードを右クリックし、<bpt id="p1">**</bpt>新規追加<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>Gantt<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>After you set the <bpt id="p1">**</bpt>Height<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Width<ept id="p2">**</ept> properties to <bpt id="p3">**</bpt>SizeToAvailable<ept id="p3">**</ept>, there are no other properties that must be set in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>高さ<ept id="p1">**</ept>および<bpt id="p2">**</bpt>幅<ept id="p2">**</ept>プロパティを <bpt id="p3">**</bpt>SizeToAvailable<ept id="p3">**</ept> に設定した後、デザイナーで設定する必要がある他のプロパティはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Unlike many other controls, Gantt controls can't be bound to data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の多くのコントロールとは異なり、Gantt コントロールはデータ ソースにバインドすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Instead, you must add all data to the control from code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、コードからコントロールにすべてのデータを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Adding activities, links, and milestone markers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動、リンク、マイルストーン マーカーの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The most basic element of a Gantt chart is the task activity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガント チャートの最も基本的な要素はタスク活動です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Each activity is allocated its own row in the chart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各活動は、個々の行がグラフに割り当てられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Activities can form a hierarchy, like a tree, by referencing a parent activity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動は、親活動を参照することによって、ツリーのような階層を形成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Additionally, any two activities can be connected to each other through links (across hierarchies).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、任意の 2 つの活動は、リンクを使用して (階層間で) 互いに接続できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>To add data to the control, you build up a list that contains the instances of the element that you want to add.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールにデータを追加するには、追加する要素のインスタンスを含むリストを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You then assign the list to the control by using a <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを使用して、リストをコントロールに割り当てます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Note that, when you modify data, you can't just modify the content of the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データを変更するときに、リストの内容だけの変更はできないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>To notify the client that data has changed, and to trigger a refresh, you must reassign the list to the control by using the <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データが変更されたことをクライアントに通知し、リフレッシュをトリガーするには、<bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを使用してリストをコントロールに再割り当てする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>API for activities and links<ept id="p1">](./media/ganttchartactivitiesapi.png)](./media/ganttchartactivitiesapi.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>活動およびリンクの API<ept id="p1">](./media/ganttchartactivitiesapi.png)](./media/ganttchartactivitiesapi.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Each activity must have a unique ID across all activity types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各活動は、すべてのアクティビティ タイプに固有の ID を持つ必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>This ID is required in order to build the hierarchy and the links.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この ID は、階層とリンクをビルドするために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The ID is also used to identify the activity when the server is notified after a user interaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID は、ユーザー操作後にサーバーに通知されたときに活動を識別するためにも使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>There are two types of milestones: the milestone activity is a stand-alone activity that receives its own row in the chart and can be referenced from the links, whereas the milestone markers appear on the same row as the related activity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイルストーンには 2 つのタイプがあります。マイルストーン アクティビティは、チャート内で独自の行を受け取り、リンクから参照できるスタンドアロン アクティビティです。マイルストーン マーカーは関連するアクティビティと同じ行に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Both types of markers are represented by using symbols from the Dynamics Symbol font.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方のタイプのマーカーは、Dynamics Symbol フォントの記号を使用して表されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Column headers and content</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列のヘッダーとコンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the “grid” on the left side of the control, you can arrange the data into columns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの左側にある「グリッド」で、データを列に配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The column definitions are provided through the <bpt id="p1">**</bpt>GanttControl.parmColumns<ept id="p1">**</ept> property, which is a list of <bpt id="p2">**</bpt>GanttControlColumn<ept id="p2">**</ept> objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列の定義は、<bpt id="p2">**</bpt>GanttControlColumn<ept id="p2">**</ept> オブジェクトのリストである <bpt id="p1">**</bpt>GanttControl.parmColumns<ept id="p1">**</ept> プロパティを使用して提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The content of the columns is given as a simple <bpt id="p1">**</bpt>List<ept id="p1">**</ept> object that contains the text strings for an activity through the <bpt id="p2">**</bpt>GanttControlActivity.parmColumnTexts<ept id="p2">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列の内容は、<bpt id="p2">**</bpt>GanttControlActivity.parmColumnTexts<ept id="p2">**</ept> プロパティを通じてアクティビティのテキスト文字列を含む単純な<bpt id="p1">**</bpt>リスト<ept id="p1">**</ept> オブジェクトとして指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Note that the values in the column list must be strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列リスト内の値は文字列でなければならないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Therefore, any formatting of numbers, enumerations, dates, and so on, must occur on the server side.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、数字、列挙型、日付などの書式は、サーバー側で発生する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The formatting of <bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> must take into account the user's preferred time zone, because that time zone will be used when the Gantt chart is rendered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>utcdatetime<ept id="p1">**</ept> の書式設定では、ユーザーの優先時間帯を考慮する必要があります。これは、ガント チャートが表示されるときにその時間帯が使用されるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>API for configuring the control<ept id="p1">](./media/ganttchartconfigurationapi.png)](./media/ganttchartconfigurationapi.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コントロールを構成するための API<ept id="p1">](./media/ganttchartconfigurationapi.png)](./media/ganttchartconfigurationapi.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Working times</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>An activity can reference a calendar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動はカレンダーを参照できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>A calendar is basically a list of working time intervals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カレンダーは基本的に、作業時間間隔のリストです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>A calendar is used to visually separate working time from non-working time by giving the “cells” (intersections of a row and a time scale interval) a different background color.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カレンダーを使用すると、「セル」(行とタイム スケール間隔の交差) に異なる背景色を付けることによって、作業時間を非作業時間から視覚的に区別することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Note that these working time intervals don't have to come from the standard calendar tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの作業時間間隔は、標準カレンダー テーブルから取得する必要はないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The intervals are just data that you can load from anywhere.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">間隔は、どこからでも読み込むことができる単なるデータです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Although calendars are a nice feature that can give you a good overview, there are some performance issues that you must consider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カレンダーは良い概要を与えることができる素晴らしい機能ですが、いくつかのパフォーマンスの問題を考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>When you turn calendars on (by setting <bpt id="p1">**</bpt>GanttControlConfiguration.parmUseCalendars<ept id="p1">**</ept> to <bpt id="p2">**</bpt>true<ept id="p2">**</ept>), each “cell” is rendered in HTML by using a DIV element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カレンダーを有効にすると (<bpt id="p1">**</bpt>GanttControlConfiguration.parmUseCalendars<ept id="p1">**</ept> を <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定して)、各「セル」は HTML 形式で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If a calendar shows lots of activities for a long period at a very granular minor timescale, there will be many DIV elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カレンダーが非常に粒度の細かいタイムスケールで長期間にわたり多くの活動を示している場合は、多くの DIV 要素が存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Depending on the browser and hardware, the large number of DIV elements can cause performance issues for the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザおよびハードウェアによっては、多数の DIV 要素がユーザーにパフォーマンスの問題を引き起こす可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In this case, you might have to turn calendars off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、カレンダーをオフにしなければならない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this way, you significantly reduce the number of DIV elements that must be rendered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、表示する必要がある DIV 要素の数を大幅に削減します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The control can't turn off calendars by itself to improve performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールでは、カレンダーをオフにしてパフォーマンスを向上させることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Based on the specific scenario, you must determine what will be best for the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のシナリオに基づいて、ユーザーに最適なものを決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Color use</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">色の使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Elements such as the activities and milestone markers have a color property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動およびマイルス トーン マーカーなどの要素には、色プロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Typically, either the int value for a specific color is calculated by using the <bpt id="p1">**</bpt>WinAPI::RGB2int<ept id="p1">**</ept> method, or the user sets the value by using the color picker (which is opened by calling <bpt id="p2">**</bpt>ColorSelection::selectColor<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、<bpt id="p1">**</bpt>WinAPI::RGB2int<ept id="p1">**</ept> メソッドを使用して特定の色の整数値を計算するか、カラー ピッカーを使用して値を設定します (カラー ピッカーは <bpt id="p2">**</bpt>ColorSelection::selectColor<ept id="p2">**</ept> メソッドを使用して開きます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Instead of controlling the colors yourself, you can specify that the colors should adhere to the current theme.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自身で色を制御するではなく、色が現在のテーマに従うことを指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When you set the <bpt id="p1">**</bpt>GanttControlConfiguration.parmUseThemeColors<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>true<ept id="p2">**</ept>, if any color values have been set that aren't part of the current theme, they are overridden (no colors have to be specified manually).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GanttControlConfiguration.parmUseThemeColors<ept id="p1">**</ept> オプションを <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定すると、現在のテーマにはない色の値が設定されている場合、それらはオーバーライドされます (どの色も手動では指定できません)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>When theme colors are used, the <bpt id="p1">**</bpt>parmIsActive<ept id="p1">**</ept> flag on an activity is used to determine whether the activity should appear in a dark color or a light color.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーマ色を使用するときは、活動を暗色または明色のいずれで表示するかを決定するために、<bpt id="p1">**</bpt>parmIsActive<ept id="p1">**</ept> フラグが活動に対して使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Interactions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">相互関係</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Whenever the user interacts with the Gantt, an event is raised to notify the server-side code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがガント チャートにかかわるたびに、サーバー側のコードを通知するためにイベントが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The following events are currently available:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、以下のイベントが利用可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>onActivitySelected(str <ph id="ph1">\_</ph>activityId, GanttControlActivityIdCollection <ph id="ph2">\_</ph>allSelectedActivityIds)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onActivitySelected(str <ph id="ph1">\_</ph>activityId, GanttControlActivityIdCollection <ph id="ph2">\_</ph>allSelectedActivityIds)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>onActivityDblClick(str <ph id="ph1">\_</ph>activityId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onActivityDblClick(str <ph id="ph1">\_</ph>activityId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>onSummaryActivityExpand(str <ph id="ph1">\_</ph>activityId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onSummaryActivityExpand(str <ph id="ph1">\_</ph>activityId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>onSummaryActivityCollapse(str <ph id="ph1">\_</ph>activityId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onSummaryActivityCollapse(str <ph id="ph1">\_</ph>activityId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>onActivityChanged(GanttControlActivityModification <ph id="ph1">\_</ph>modification, GanttControlActivityModificationResponse <ph id="ph2">\_</ph>response)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onActivityChanged(GanttControlActivityModification <ph id="ph1">\_</ph>modification, GanttControlActivityModificationResponse <ph id="ph2">\_</ph>response)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>All these events are one-way notifications from the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべてのイベントはクライアントからの一方向の通知です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>However, the <bpt id="p1">**</bpt>onActivityChanged<ept id="p1">**</ept> event is somewhat special, because you can set a response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、応答を設定できるため、<bpt id="p1">**</bpt>onActivityChanged<ept id="p1">**</ept> イベントは多少特殊なものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Typically, when a user makes a modification (for example, he or she drags an activity to a new time), either other activities must also be updated or some adjustments must be made to the activity itself (for example, the column texts must be changed).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、ユーザーが変更を加えた場合 (たとえば、アクティビティを新しい時間にドラッグする)、他のアクティビティも更新するか、アクティビティ自体を調整する必要があります (たとえば、列テキストを変更する必要がある)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>GanttControlActivityModificationResponse<ept id="p1">**</ept> response, you can provide a list of activities that must be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GanttControlActivityModificationResponse<ept id="p1">**</ept> 応答で、更新する必要のあるアクティビティの一覧を提示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>If the change that the user makes is just accepted as is, no response must be set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーによる変更がそのまま受け入れられる場合、応答を設定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>However, at the very least, the column texts of the current activity must be updated in most cases, to guarantee that the new from and to dates appear.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、少なくとも、新しい開始日と終了日を表示するよう保証するため、ほとんどの場合現在の活動の列テキストは更新される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On an activity, the <bpt id="p1">**</bpt>parmAllowMove<ept id="p1">**</ept> flag determines whether the activity can be moved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動で、<bpt id="p1">**</bpt>parmAllowMove<ept id="p1">**</ept> フラグは、活動が移動できるかどうかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>However, higher-level flags on <bpt id="p1">**</bpt>GanttControlConfiguration<ept id="p1">**</ept> determine whether any activity can be moved (<bpt id="p2">**</bpt>parmAllowMoveActivities<ept id="p2">**</ept>) or resized (<bpt id="p3">**</bpt>parmAllowResizeActivities<ept id="p3">**</ept>), or whether the completion percentage for the activity can be changed (<bpt id="p4">**</bpt>parmAllowCompletionChange<ept id="p4">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>GanttControlConfiguration<ept id="p1">**</ept> の高レベルのフラグは、任意の活動を移動 (<bpt id="p2">**</bpt>parmAllowMoveActivities<ept id="p2">**</ept>) またはサイズを変更 (<bpt id="p3">**</bpt>parmAllowResizeActivities<ept id="p3">**</ept>) できるかどうか、または、活動の完了率を変更 (<bpt id="p4">**</bpt>parmAllowCompletionChange<ept id="p4">**</ept>) できるかどうかを決定します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>