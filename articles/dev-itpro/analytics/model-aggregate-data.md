<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="model-aggregate-data.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>model-aggregate-data.878a8d.1a3f5fba3c3b1309834e9ee3a13651d9d6784753.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1a3f5fba3c3b1309834e9ee3a13651d9d6784753</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\model-aggregate-data.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Model aggregate data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの集計モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial will walk you through the process of modeling aggregate data .</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、集計データをモデリングするプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Model aggregate data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの集計モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial will walk you through the process of modeling aggregate data .</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、集計データをモデリングするプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial requires you to access the environment using Remote Desktop, and be provisioned as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For more information, see the topic named <bpt id="p1">[</bpt>Access Microsoft Dynamics 365 for Finance and Operations instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>Microsoft Dynamics 365 for Finance and Operations インスタンスにアクセス<ept id="p1">](../dev-tools/access-instances.md)</ept>」というトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Aggregate measurements<ept id="p1">**</ept>, similar to <bpt id="p2">**</bpt>perspectives<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Cubes<ept id="p3">**</ept> from earlier versions, enable you to model and consume aggregate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>集計の測定<ept id="p1">**</ept>は、以前のバージョンの<bpt id="p2">**</bpt>分析視点<ept id="p2">**</ept>および<bpt id="p3">**</bpt>キューブ<ept id="p3">**</ept>と同様に、集計データをモデル化して使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Key Performance Indicators (KPIs)<ept id="p1">**</ept> are a form of analytic controls that track organizational performance against the current status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>主要業績評価指標 (KPI)<ept id="p1">**</ept> は、現在の状態と照らし合わせて組織のパフォーマンスを追跡する分析コントロールの形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>KPIs are represented as tiles in a <bpt id="p1">**</bpt>workspace<ept id="p1">**</ept> or the <bpt id="p2">**</bpt>dashboard<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI は、<bpt id="p1">**</bpt>ワークスペース<ept id="p1">**</ept>または<bpt id="p2">**</bpt>ダッシュボード<ept id="p2">**</ept>でタイルとして表されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this tutorial, you will model a KPI in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Visual Studio で KPI をモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>KPIs that are modeled in Visual Studio can be modified in the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio でモデル化される KPI は、クライアントで変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>A user also has the ability to model new KPIs using the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、ユーザーは、クライアントを使用して新しい KPI をモデル化することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>A <bpt id="p1">**</bpt>workspace<ept id="p1">**</ept> is an overview page that is specific to a particular subject area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ワークスペース<ept id="p1">**</ept>は、特定のサブジェクト領域固有の概要ページです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Workspaces are common to all users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースはすべてのユーザーに共通です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>dashboard<ept id="p1">**</ept> is the default home page for each user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダッシュボード<ept id="p1">**</ept>は、ユーザーごとの既定のホーム ページです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Tiles<ept id="p1">**</ept> are securable objects that can be pinned to a workspace or the dashboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイル<ept id="p1">**</ept>ワークスペースまたはダッシュ ボードに固定できる、セキュリティ保護可能なオブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>KPIs and aggregate data that are shown on the dashboard, or a workspace, can be secured by using menu items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュボードまたはワークスペースに表示される KPI と集計データは、メニュー項目を使用してセキュリティで保護することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Aggregate data can be consumed in building charts and other controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計データはグラフやその他のコントロールの作成に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Using the model driven approach, you have the ability to create data entities by directly referencing aggregate measurements and aggregate dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル駆動方式を使用して、集計の測定と集計分析コードを直接参照することによって、データ エンティティを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>These entities are referred to as <bpt id="p1">**</bpt>Aggregate data entities<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのエンティティは、<bpt id="p1">**</bpt>データ エンティティの集計<ept id="p1">**</ept>と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Aggregate data entities are read-only data entities used for reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計データ エンティティはレポート用に使用される読み取り専用データ エンティティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>The aggregate programming model<ept id="p1">**</ept> enables a developer to consume aggregate data programmatically using either X++ or C<ph id="ph1">\#</ph> code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>集計のプログラミング モデル<ept id="p1">**</ept> により、開発者は、X++ または C<ph id="ph1">\#</ph> コードのいずれかを使用してプログラムを使用して集計データを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Data retrieved using the aggregate programming model can be used as a data source in forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計プログラミング モデルを使用して取得されたデータは、フォーム内のデータ ソースとして使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Method expressions<ept id="p1">**</ept> enable a developer to build rich expressions using aggregate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドの式<ept id="p1">**</ept>は、開発者が集計データを使用して豊富な式を構築できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Method expressions are an X++ class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの式は、X++ クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>KPIs can be modeled using method expressions, thereby eliminating the need to build MDX expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI はメソッドの式によってモデル化でき、MDX 式を構築する必要がなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Contextual BI<ept id="p1">**</ept> refers to providing required insights as part of the user experience such that the user has relevant insights to not only achieve the task at hand, but be highly-productive during the course of the day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンテキスト BI<ept id="p1">**</ept> は、ユーザー体験の一部として必要な洞察を提供することを指します。ユーザーは、当面のタスクを達成するだけでなく、1 日の間に非常に生産的な洞察を得ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Embedded BI<ept id="p1">**</ept> refers to analytic content being embedded within the user experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組み込み型 BI<ept id="p1">**</ept> は、ユーザー エクスペリエンス内に埋め込まれた分析コンテンツを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Contextual BI and embedded BI teams are closely related.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト BI および組み込み BI チームは密接に関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Contextual BI implies the added notion that the context of analytic context revolves around the data or the task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト BI は、分析コンテキストのコンテキストがデータまたはタスクを中心に展開する追加された概念を意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Self-service BI<ept id="p1">**</ept> refers to enabling a user to tweak existing and/or create new analytic content such as reports, KPIs, and dashboards.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セルフ サービス BI<ept id="p1">**</ept> ユーザーが既存のものを微調整したり、または新しくレポート、KPI、ダッシュボードなどの分析コンテンツを作成できるように参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Set up</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If this is the first tutorial you are working on, make sure you have configured the administrator user if you are running on a local VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが作業している最初のチュートリアルである場合は、ローカル VM で実行している場合、管理者ユーザーを構成していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Import the tutorial project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you have already imported the Fleet management tutorial project, skip to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアル プロジェクトを既にインポートした場合は、次のセクションに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In Visual Studio, on the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Import Project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>プロジェクトのインポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Download the Fleet Management sample from <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph>, save it to <bpt id="p1">**</bpt>c:<ph id="ph2">\\</ph><ept id="p1">**</ept>, and unzip it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理のサンプルを <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph> からダウンロードし、<bpt id="p1">**</bpt>c:<ph id="ph2">\\</ph><ept id="p1">**</ept> に保存してから解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>In the <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> window, next to the <bpt id="p2">**</bpt>Filename<ept id="p2">**</ept> text box, click the ellipsis button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>ファイル名<ept id="p2">**</ept>テキスト ボックスの隣にある、省略記号ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the <bpt id="p1">**</bpt>Select the file to import<ept id="p1">**</ept> window, browse to the location of the <bpt id="p2">**</bpt>FMLab<ept id="p2">**</ept> folder, click <bpt id="p3">**</bpt>FMTutorialDataModel.axpp<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Open<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポートするファイルの選択<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>FMLab<ept id="p2">**</ept> フォルダーの場所を参照して <bpt id="p3">**</bpt>FMTutorialDataModel.axpp<ept id="p3">**</ept> をクリックしてから<bpt id="p4">**</bpt>開く<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>Project file location<ept id="p1">**</ept> text box, enter <bpt id="p2">**</bpt>C:<ph id="ph1">\\</ph>FMLab<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト ファイルの場所<ept id="p1">**</ept>テキスト ボックスに、<bpt id="p2">**</bpt>C:<ph id="ph1">\\</ph>FMLab<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Select the <bpt id="p1">**</bpt>Overwrite Elements<ept id="p1">**</ept> check box, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要素の上書き<ept id="p1">**</ept> チェック ボックスをオンにし、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Open the tutorial project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトを開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In Visual Studio, open the <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the <bpt id="p1">**</bpt>Open Project<ept id="p1">**</ept> dialog box, browse to C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>FMTutorial, and then click FMTutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトを開く<ept id="p1">**</ept>ダイアログ ボックスで、C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>FMTutorial を参照してから FMTutorial をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> project appears in <bpt id="p2">**</bpt>Solution Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> プロジェクトが<bpt id="p2">**</bpt>ソリューション エクスプローラー<ept id="p2">**</ept>に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use the FMTDataHelper class to load data for the Fleet Management tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアルのデータを読み込むには、FMTDataHelper クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, in the FMTutorial project, expand <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の FMTutorial プロジェクトで<bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Right-click <bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Set as Startup Object<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>スタートアップ オブジェクトとして設定<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>On the <bpt id="p1">**</bpt>Build<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Rebuild Solution<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>ソリューションの再構築<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You use the rebuild to update the timestamps of the imported artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたアーティファクトのタイムスタンプを更新するには、リビルドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>You can view the build progress in the <bpt id="p1">**</bpt>Output<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力<ept id="p1">**</ept> ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Press Ctrl+F5 to run the project and load the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+F5 キーを押してプロジェクトを実行し、データを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Model an aggregate measurement for rental charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル料金の集計の測定をモデルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Often, when a user asks for additional information, you get a request for one or more new reports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが追加情報を求める場合、1 つまたは複数の新しいレポートを要求されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Imagine that the manager of a rental car company has called and asked for a report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタカー会社の管理者が電話をかけ、レポートを依頼した場合を考えてみましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>She is interested in finding out how the rental business is performing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">彼女は、レンタル業務を行う方法を知ることに関心を持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>She wants a report that shows rental revenue by month.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">彼女は、月別のレンタル収益を示すレポートを必要としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>You soon find out that she is interested in a breakdown of rental revenues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">彼女がレンタル収益の詳細に関心を持っていることがすぐ分かるでしょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>She wants to know whether the rental revenue is high in cases where they have sold additional services, for example, car seats, GPS, re-fueling, as opposed to the base rental charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">彼女は、基本レンタル料とは対照的に、追加サービス (車のシート、GPS、燃料補給など) を販売した場合に求レンタル収益高くなるかどうかを知りたいと思っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>As it turns out, she suspects that specific customer groups are driving revenue up, and this is why she wanted the report in the first place.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結論からいうと、彼女が最初のレポートを望んだ理由は、特定の顧客グループが収益を上げていると思っていたからです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>She insists on adding Customer group to the report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">彼女は、レポートに顧客グループを追加すると主張しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Because the revenue must be considered in relation to the number of rentals, she doesn’t want a few large corporate rentals to skew her analysis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">収益はレンタル数と関連して考慮する必要があるため、いくつかの大規模な法人レンタルの解析を歪曲させたくはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You both agree that the number of rentals needs to be shown along with revenue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両者は収益とともにレンタル数を表示する必要があることに同意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>We could represent this requirement as a set of business questions using a matrix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要件を行列を使用して業務上の質問のセットとして表現することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Rows indicate the <bpt id="p1">**</bpt>measures<ept id="p1">**</ept> (or numbers) and the columns indicate the <bpt id="p2">**</bpt>dimensions<ept id="p2">**</ept> (or slicers).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行は、<bpt id="p1">**</bpt>メジャー<ept id="p1">**</ept> (または数値) を示し、列は<bpt id="p2">**</bpt>分析コード<ept id="p2">**</ept> (またはスライサー) を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>An "X" in the intersection between a measure and a dimension indicates that the measure needs to be "grouped by" the dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定および分析コード間で交差する「X」は、測定が分析コードによって「グループ化」される必要があることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Rental date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル日付</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Customer group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Rental charge type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル料金のタイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>Revenue<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>収益<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>Number of rentals<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レンタルの数<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">x</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Next, we will model an aggregate measurement to answer this business question.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、この業務上の質問に回答する集計の測定をモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Add a measure group for rental charges by using an existing view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のビューを使用してレンタル料金のメジャー グループを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In this section you will add a new measure group to an existing aggregate measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、既存の集計測定に新しいメジャー グループを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, expand the <bpt id="p2">**</bpt>Analytics<ept id="p2">**</ept> folder of the project, and then double-click the aggregate measurement, <bpt id="p3">**</bpt>FMTAggregateMeasurement<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>でプロジェクトの<bpt id="p2">**</bpt>分析<ept id="p2">**</ept>フォルダーを展開してから、集計の測定 <bpt id="p3">**</bpt>FMTAggregateMeasurement<ept id="p3">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The aggregate measurement will be launched in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計の測定はデザイナーで起動されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Notice that the existing aggregate measurement contains two measure groups related to vehicle inventory and rental details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の集計の測定に、車両の在庫やレンタルの詳細に関連する 2 つのメジャー グループが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You will create a new measure group related to rental charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル料金に関連する新しいメジャー グループを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTAggregateMeasurement<ept id="p1">](./media/fmtaggregatemeasurement.png)](./media/fmtaggregatemeasurement.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTAggregateMeasurement<ept id="p1">](./media/fmtaggregatemeasurement.png)](./media/fmtaggregatemeasurement.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, expand the <bpt id="p2">**</bpt>Views<ept id="p2">**</ept> folder of the project, and then select the <bpt id="p3">**</bpt>FMTRentalChargeExtendedView<ept id="p3">**</ept> view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>でプロジェクトの<bpt id="p2">**</bpt>表示<ept id="p2">**</ept>フォルダーを展開してから、<bpt id="p3">**</bpt>FMTRentalChargeExtendedView<ept id="p3">**</ept> の表示を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Drag-and-drop the <bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> into the root node of the <bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept> aggregate measurement in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> をデザイナーの <bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept> 集計測定のルート ノードにドラッグ アンド ドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Notice that a new measure group is created and the values of properties have been applied as follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメジャー グループが作成され、プロパティの値が次のように適用されたことに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>FMRentalChargeExtendedView</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMRentalChargeExtendedView</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>FMRentalChargeExtendedView</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMRentalChargeExtendedView</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click the <bpt id="p2">**</bpt>FMRentalChargeExtendedView<ept id="p2">**</ept> view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMRentalChargeExtendedView<ept id="p2">**</ept> の表示をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>When the designer form opens, expand the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナー フォームが開いたら、<bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Select the <bpt id="p1">**</bpt>ExtendedAmount<ept id="p1">**</ept> and <bpt id="p2">**</bpt>RentalID<ept id="p2">**</ept> fields, and then drag-and-drop the two fields onto the <bpt id="p3">**</bpt>Measures<ept id="p3">**</ept> node of the newly created <bpt id="p4">**</bpt>FMAggregateMeasurement<ept id="p4">**</ept> measure group called <bpt id="p5">**</bpt>FMRentalChargeExtendedView<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExtendedAmount<ept id="p1">**</ept> および <bpt id="p2">**</bpt>RentalID<ept id="p2">**</ept> フィールドを選択した後、2 つのフィールドを <bpt id="p5">**</bpt>FMRentalChargeExtendedView<ept id="p5">**</ept> と呼ばれる新たに作成された <bpt id="p4">**</bpt>FMAggregateMeasurement<ept id="p4">**</ept> メジャー グループの <bpt id="p3">**</bpt>Measures<ept id="p3">**</ept> ノードにドラッグ アンド ドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>As you drag the fields, hover your cursor over the <bpt id="p1">**</bpt>FMAggregateMeasurement<ept id="p1">**</ept> tab to access the <bpt id="p2">**</bpt>Measures<ept id="p2">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドをドラッグする際、<bpt id="p1">**</bpt>FMAggregateMeasurement<ept id="p1">**</ept> タブにカーソルを置き、<bpt id="p2">**</bpt>メジャー<ept id="p2">**</ept> ノードにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>By default, when you drag-and-drop the fields, the system assumes that you want counts of the measures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、フィールドをドラッグ アンド ドロップするときに、メジャーのカウントが必要と見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>In this case, you need to modify default properties for the <bpt id="p1">**</bpt>ExtendedAmount<ept id="p1">**</ept> and <bpt id="p2">**</bpt>RentalId<ept id="p2">**</ept> measures as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、次のように <bpt id="p1">**</bpt>ExtendedAmount<ept id="p1">**</ept> および <bpt id="p2">**</bpt>RentalId<ept id="p2">**</ept> 測定値の既定のプロパティを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Property (ExtendedAmount)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ (ExtendedAmount)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Default Aggregate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の集計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Sum<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SUM<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>ExtendedAmount (no change required)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExtendedAmount (変更の必要なし)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Revenue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">収益</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Property (RentalId)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ (RentalId)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Default Aggregate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の集計</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>DistinctCount<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DistinctCount<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>RentalId (no change required)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RentalId (変更の必要なし)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>NumRentals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NumRentals</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Next let's create another measure which calculates <bpt id="p1">**</bpt>Revenue per Rental<ept id="p1">**</ept> by copying an existing measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、既存の測定単位をコピーして、<bpt id="p1">**</bpt>レンタルあたりの収益<ept id="p1">**</ept>を計算する別の測定単位を作成してみましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Select the <bpt id="p1">**</bpt>TotalRevenue<ept id="p1">**</ept> measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TotalRevenue<ept id="p1">**</ept> 測定を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Right-click and select <bpt id="p1">**</bpt>Copy<ept id="p1">**</ept> from the <bpt id="p2">**</bpt>Context<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p2">**</bpt>コンテキスト<ept id="p2">**</ept> メニューから <bpt id="p1">**</bpt>コピー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Select the <bpt id="p1">**</bpt>FMRentalDetails<ept id="p1">**</ept> measure group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRentalDetails<ept id="p1">**</ept> メジャー グループを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Right-click and select paste.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、貼り付けを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Rename the newly created measure to <bpt id="p1">**</bpt>RevenuePerRental<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新たに作成された測定の名前を <bpt id="p1">**</bpt>RevenuePerRental<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Modify the aggregation function to <bpt id="p1">**</bpt>Average<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計関数を <bpt id="p1">**</bpt>Average<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Model an aggregate dimension charge type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計分析コード料金のタイプをモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To analyze rental revenue by the different charge types, you need to be able to slice revenue by the charge type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな料金のタイプによってレンタル収益を分析するには、料金タイプごとに収益をスライスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>For this purpose, you will first model a charge type dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このためには、最初に管理タイプ分析コードをモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, under <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept>, right-click <bpt id="p3">**</bpt>Analytics<ept id="p3">**</ept>, point to <bpt id="p4">**</bpt>Add<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>New Item<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> で<bpt id="p3">**</bpt>分析<ept id="p3">**</ept>を右クリックして、<bpt id="p4">**</bpt>追加<ept id="p4">**</ept>をポイントしてから<bpt id="p5">**</bpt>新しい項目<ept id="p5">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Select <bpt id="p1">**</bpt>Dynamics 365 Artifacts<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Analytics<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Aggregate Dimension<ept id="p3">**</ept> from the list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">項目の一覧から <bpt id="p1">**</bpt>Dynamics 365 コンポーネント<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>分析<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>分析コードの集計<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property, enter <bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>プロパティで、<bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>This is the name of the aggregate dimension that will be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、作成される集計分析コードの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>This name must be unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この名前は一意でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The new dimension will appear in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コードは、Visual Studio に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept>, expand the <bpt id="p2">**</bpt>AOT<ept id="p2">**</ept> and click <bpt id="p3">**</bpt>Data Model<ept id="p3">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p4">**</bpt>Tables<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>AOT<ept id="p2">**</ept> を展開して<bpt id="p3">**</bpt>データ モデル<ept id="p3">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p4">**</bpt>テーブル<ept id="p4">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Drag-and-drop the <bpt id="p1">**</bpt>FMTChargeType<ept id="p1">**</ept> table from <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> onto the root node of the newly created <bpt id="p3">**</bpt>FMTChargeType<ept id="p3">**</ept> dimension in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTChargeType<ept id="p1">**</ept> テーブルを <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> からデザイナーで新しく作成された <bpt id="p3">**</bpt>FMTChargeType<ept id="p3">**</ept> 分析コードのルート ノードにドラッグ アンド ドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Notice that dimension attributes and corresponding keys have been added using the AutoReport field group of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの属性と対応するキーがテーブルの AutoReport フィールド グループを使用して追加されたことに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Expand the <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept> node of the new dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コードの<bpt id="p1">**</bpt>属性<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Notice that several attributes have been created for you by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの属性は既定で作成されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>The system has also created a dimension key based on unique indexes of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、テーブルの一意のインデックスに基づいて分析コード キーが作成されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>You can add additional fields by dragging and dropping them into the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> ノードにドラッグ アンド ドロップすることにより、さらにフィールドを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTChargeType<ept id="p1">](./media/fmtchargetype.png)](./media/fmtchargetype.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTChargeType<ept id="p1">](./media/fmtchargetype.png)](./media/fmtchargetype.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Save the new dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コードを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>You may get a warning asking you to rename the field name Description to avoid the MDX reserved word.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MDX 予約ワードを回避するためにフィールド名の説明を変更するように求める警告が表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Even though the aggregate dimension may not be deployed to SSAS in this aggregate measurement, it's possible that this dimension may be used by an aggregate measurement deployed to SSAS in the future.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集約分析コードは、集計測定で SSAS に配置されない場合がありますが、今後 SSAS に配置される集計測定でこの分析コードが使用される可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>To avoid potential issues in the future, rename the field name <bpt id="p1">**</bpt>Description<ept id="p1">**</ept> to <bpt id="p2">**</bpt>ChargeDescription<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来の潜在的な問題を避けるために、フィールド名 <bpt id="p1">**</bpt>Description<ept id="p1">**</ept> の名前を <bpt id="p2">**</bpt>ChargeDescription<ept id="p2">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Model dimension references for customer profile and charge type dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客プロファイルの分析コードの参照と料金のタイプの分析コードのモデル化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Next, create dimension references to new and existing dimensions so that revenue can be sliced by customer as well as charge type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、新規および既存の分析コードに分析コードの参照を作成して、収益を顧客および料金のタイプでスライスできるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept> or, if you have it open, navigate to it in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept> をダブルクリックするか、開いている場合はデザイナーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, select the dimensions <bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept> and <bpt id="p3">**</bpt>FMTCustomerProfile<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、分析コード <bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept> および <bpt id="p3">**</bpt>FMTCustomerProfile<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Drag-and-drop them into the <bpt id="p1">**</bpt>Dimensions<ept id="p1">**</ept> node of the <bpt id="p2">**</bpt>FMTRentalChargeExtendedView<ept id="p2">**</ept> measure group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>FMTRentalChargeExtendedView<ept id="p2">**</ept> 測定グループの<bpt id="p1">**</bpt>分析コード<ept id="p1">**</ept>ノードにドラッグ アンド ドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Notice that dimension references have been created along with relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの参照が関係とともに作成されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Save changes to <bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept> の変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Review the property sheet for the dimension relation and notice that the <bpt id="p1">**</bpt>Use Table relations<ept id="p1">**</ept> property is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの関係のプロパティ シートを確認して、<bpt id="p1">**</bpt>テーブル関係の使用<ept id="p1">**</ept> プロパティが <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Notice that the drag-and-drop operation created relationships between the measure group dimensions <bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> and <bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>FMTCustomerProfile<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドラッグ アンド ドロップ操作によって、メジャー グループ分析コード <bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> および <bpt id="p2">**</bpt>FMTChargeType<ept id="p2">**</ept>、<bpt id="p3">**</bpt>FMTCustomerProfile<ept id="p3">**</ept> の間に関係が作成されたことに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Review the property sheet for the dimension relation and notice that the <bpt id="p1">**</bpt>Use Table relations<ept id="p1">**</ept> property is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードの関係のプロパティ シートを確認して、<bpt id="p1">**</bpt>テーブル関係の使用<ept id="p1">**</ept> プロパティが <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTChargeType2<ept id="p1">](./media/fmtchargetype2.png)](./media/fmtchargetype2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTChargeType2<ept id="p1">](./media/fmtchargetype2.png)](./media/fmtchargetype2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>In platform update 1611 and later, <bpt id="p1">**</bpt>UseTableRelations<ept id="p1">**</ept> property has been removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 1611 以降では、<bpt id="p1">**</bpt>UseTableRelations<ept id="p1">**</ept> プロパティが削除されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>When a new dimension reference is created, system will default existing relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コード参照が作成されるとき、既存のリレーションシップが既定値に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>You can continue to provide an explicit relationship by changing the relationship field that was defaulted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定に設定されているリレーションシップ フィールドを変更することにより、明示的リレーションシップの提供を継続することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Providing an explicit relationship is equal to setting <bpt id="p1">**</bpt>UseTableRelationship<ept id="p1">**</ept> to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明示的な関係を提供することは、<bpt id="p1">**</bpt>UseTableRelationship<ept id="p1">**</ept> を <bpt id="p2">**</bpt>No<ept id="p2">**</ept> に設定することと同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Expand the Dimension relations node for the <bpt id="p1">**</bpt>FMTCustomerProfile<ept id="p1">**</ept> dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTCustomerProfile<ept id="p1">**</ept> 分析コードの分析コード関係ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Notice that the <bpt id="p1">**</bpt>UseTableRelations<ept id="p1">**</ept> property is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>UseTableRelations<ept id="p1">**</ept> プロパティが<bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept>に設定されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>In this case, the system has not been able to find a suitable relationship between the Measure group and dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、システムはメジャー グループおよび分析コードの間に適切な関係を発見できませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>You will need to specify one manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動で指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Expand the <bpt id="p1">**</bpt>FMTCustomerProfile<ept id="p1">**</ept> dimension reference if you have not done so already.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未処理の場合は、<bpt id="p1">**</bpt>FMTCustomerProfile<ept id="p1">**</ept> 分析コードの参照を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select the node <bpt id="p1">**</bpt>FMTCustomerExtendedView<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノード <bpt id="p1">**</bpt>FMTCustomerExtendedView<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Right-click and see the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、プロパティ シートを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>CustomerID<ept id="p1">**</ept> as the value for property <bpt id="p2">**</bpt>DimensionAttribute<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ <bpt id="p2">**</bpt>DimensionAttribute<ept id="p2">**</ept> の値として <bpt id="p1">**</bpt>CustomerID<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Select the relationship shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に表示された関係を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> for the property value <bpt id="p2">**</bpt>RelatedField<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ値 <bpt id="p2">**</bpt>RelatedField<ept id="p2">**</ept> に <bpt id="p1">**</bpt>顧客<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Save changes to <bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept> の変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT4<ept id="p1">](./media/fmt4.png)](./media/fmt4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT4<ept id="p1">](./media/fmt4.png)](./media/fmt4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>In this scenario, we specified a relationship because the system was unable to find one.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、システムが関係を検出できなかったため、関係を指定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>You could also specify a different relationship if you want to override the system choice by setting <bpt id="p1">**</bpt>Use Table Relations property<ept id="p1">**</ept> to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル関係プロパティを使用する<ept id="p1">**</ept> を <bpt id="p2">**</bpt>いいえ<ept id="p2">**</ept> に設定してシステムの選択をオーバーライドする場合、異なるリレーションシップを指定することもできました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Model dimension references for the date dimension's rental start date and transaction date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付分析コードのレンタルの開始日とトランザクションの日付の分析コードの参照のモデル化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Assume that for analysis purposes, you want to enable slicing by the start date of the rental; but for accounting purposes, you want to enable slicing by the transaction date for each of the charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析の目的で、レンタルの開始日までにスライスを有効にすると仮定しますが、会計処理のために、各請求のトランザクションの日付にスライスを有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>To do this, you need to associate the rental charges measure group with two date dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、レンタル料金測定値グループを 2つ の日付の分析コードに関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In the BI world, this pattern is known as <bpt id="p1">**</bpt>Role Playing dimensions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BI では、このパターンは<bpt id="p1">**</bpt>ロール プレイの分析コード<ept id="p1">**</ept>と知られています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>By default, a date dimension is added to the measure group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、メジャー グループに日付分析コードが追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can rename the default name appropriately and add new date dimensions as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、既定の名前を適切に変更して新しい日付分析コードを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Expand the <bpt id="p1">**</bpt>Dimensions<ept id="p1">**</ept> node of the <bpt id="p2">**</bpt>FMTRentalChargeExtendedView<ept id="p2">**</ept> measure group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>FMTRentalChargeExtendedView<ept id="p2">**</ept> 測定グループの<bpt id="p1">**</bpt>分析コード<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Notice that the <bpt id="p1">**</bpt>Date<ph id="ph1">\_</ph><ept id="p1">**</ept> dimension has already been included as dimension slicers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Date<ph id="ph1">\_</ph><ept id="p1">**</ept> 分析コードが既に分析コードのスライサーとして含まれていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>If the table or the view used to model the measure group is a Company-specific table, for example it contains DATAAREAID as part of the key), a <bpt id="p1">**</bpt>Company<ept id="p1">**</ept> dimension relation will be created by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メジャー グループをモデル化するために使用されるテーブルまたはビューが会社固有のテーブル、たとえば、キーの一部として DATAAREAID を含む場合、既定では、<bpt id="p1">**</bpt>会社<ept id="p1">**</ept>分析コードの関係が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>In this case, the view we used is not a company specific one.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、使用したビューは会社固有のものではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT5<ept id="p1">](./media/fmt5.png)](./media/fmt5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT5<ept id="p1">](./media/fmt5.png)](./media/fmt5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Select the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> dimension and specify the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept> 分析コードを選択し、次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>RentalStartDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RentalStartDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Use Table Relations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル リレーションの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>No (This is the default – no need to change)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いいえ (これは既定値です – 変更する必要はありません)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Define the table relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル関係を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Expand <bpt id="p1">**</bpt>RentalStartDate<ept id="p1">**</ept>, and then expand the <bpt id="p2">**</bpt>Date<ept id="p2">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RentalStartDate<ept id="p1">**</ept> を展開し、その後<bpt id="p2">**</bpt>日付<ept id="p2">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select the Relationship shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示された関係を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Right-click and select the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、プロパティ シートを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Select <bpt id="p1">**</bpt>StartDate<ept id="p1">**</ept> for the value of <bpt id="p2">**</bpt>Related field<ept id="p2">**</ept> property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Related field<ept id="p2">**</ept> プロパティの値として <bpt id="p1">**</bpt>StartDate<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>The relationship you defined should look like the following screenshot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義した関係は、次のスクリーン ショットのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>FMT6</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMT6</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Next, enable slicing of measures by the TransactionDate dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、TransactionDate 分析コード別のメジャーのスライスを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>TransactionDate is also a date dimension, so you will add another reference to the date dimension and associate that with the corresponding field that contains the transaction date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransactionDate は日付分析コードでもあるため、日付分析コードに別の参照を追加し、トランザクション日付を含む対応するフィールドに関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>When more than one date dimension is used as a slicer, each date dimension is known as a <bpt id="p1">**</bpt>Role playing date dimension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の日付分析コードがスライサーとして使用されるとき、各日付分析コードは <bpt id="p1">**</bpt>ロールプレイング日付分析コード<ept id="p1">**</ept> と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Under the <bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> measure group, right-click the <bpt id="p2">**</bpt>Dimensions<ept id="p2">**</ept> node, and then click <bpt id="p3">**</bpt>New Dimension<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTRentalChargeExtendedView<ept id="p1">**</ept> メジャー グループで、<bpt id="p2">**</bpt>分析コード<ept id="p2">**</ept> ノードを右クリックし、<bpt id="p3">**</bpt>新しい分析コード<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>A new dimension will be added to the list of dimension references.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コードが分析コード参照のリストに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Specify the following properties for the new dimension reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい分析コード参照の次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Dimension Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Date<ph id="ph1">\_</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日<ph id="ph1">\_</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>If you select the Dimension Name in the wrong order, it will reset the other values you already set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">間違った順序で分析コードの名前を選択した場合は、既に設定したその他の値がリセットされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>TransactionDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransactionDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Use table relations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル リレーションの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Tags</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>RolePlayingDate; Fleet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RolePlayingDate。フリート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Notice the new property called <bpt id="p1">**</bpt>Tags<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Tags<ept id="p1">**</ept> と呼ばれる新しいプロパティに注目してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>This property enables the discovery of patterns within code and metadata from within the Visual studio environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを使用すると、Visual studio 環境内のコードとメタデータ内のパターンを検出できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>You can enter any number of tags and they can be searched using the hot keys or the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のタグの番号を入力することができます。これらはホット キーまたは Visual Studio の <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューを使用して検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Define the table relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル関係を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Right-click <bpt id="p1">**</bpt>TransactionDate<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Relation<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TransactionDate<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しい関係<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>You do not need to specify any properties in the DimensionsRelation at this point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で、DimensionsRelation のプロパティを指定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Expand <bpt id="p1">**</bpt>BIDateDimensionValue<ept id="p1">**</ept>, and then select the <bpt id="p2">**</bpt>Relationship<ept id="p2">**</ept> <bpt id="p3">**</bpt>Constraint<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BIDateDimensionValue<ept id="p1">**</ept> を展開し、次に<bpt id="p2">**</bpt>リレーションシップ<ept id="p2">**</ept> <bpt id="p3">**</bpt>制約<ept id="p3">**</ept>を選びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Right-click and select the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、プロパティ シートを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Specify the following properties for the BIDateDimensionsView relation constraint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BIDateDimensionsView 関係制約の次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Related Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>TranDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TranDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>The relationship you defined should look like the following screenshot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義した関係は、次のスクリーン ショットのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMY7<ept id="p1">](./media/fmy7.png)](./media/fmy7.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMY7<ept id="p1">](./media/fmy7.png)](./media/fmy7.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Save the aggregate measurement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計測定を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Deploy the newly generated aggregate measurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新たに生成され集計の測定を配置する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Now that you have completed modeling the aggregate measurement, you can deploy the aggregate measurement and continue with building KPIs and visualizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計の測定のモデリングが完了したので、集計の測定を配置して KPI の構築と視覚化を続行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>You have 2 deployment choices as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のように配置には 2 つの選択肢があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Considerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注意事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>In-memory real-time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモリ内リアルタイム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>This option will leverage the In-memory Column store indexes of SQL Server database to deploy Aggregate Measurements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、SQL Server データベースのメモリ内縦棒ストア インデックスを利用して、集計の測定を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>This option is recommended when the Aggregate measurement is used for embedded analytics within the client where you need <bpt id="p1">**</bpt>real-time analytics<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、<bpt id="p1">**</bpt>リアルタイム分析<ept id="p1">**</ept>が必要なクライアント内の埋め込み分析に集計の測定を使用する場合に推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>For an overview of concepts on real-time analytics, see <bpt id="p1">[</bpt>Analytics, aggregate measurements, and KPI modeling<ept id="p1">](analytics.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム分析の概念の概要については、<bpt id="p1">[</bpt>分析、集計測定、および KPI モデリング<ept id="p1">](analytics.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Stage in Entity Store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納のステージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>This option leverages Entity store, the operational data store that enables <bpt id="p1">**</bpt>near real-time PowerBI reporting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、<bpt id="p1">**</bpt>near real-time PowerBI reporting<ept id="p1">**</ept> を有効にする運用データストアであるエンティティ ストアを利用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>If you choose this option, Aggregate measurement can be deployed to Entity store and you can schedule the data to be refreshed periodically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションを選択する場合は、集計測定をエンティティ店舗に配置でき、データを定期的に更新するためにスケジューリングできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>For an overview of this approach, refer to the blog post here: <bpt id="p1">[</bpt><ph id="ph1">https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/</ph><ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチの概要については、このブログ投稿を参照してください: <bpt id="p1">[</bpt><ph id="ph1">https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/</ph><ept id="p1">](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source><bpt id="p1">**</bpt>SSAS Cube<ept id="p1">**</ept> option is no longer supported when modeling aggregate measurements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計測定をモデル化する場合、<bpt id="p1">**</bpt>SSAS キューブ<ept id="p1">**</ept> オプションは、サポートされなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Select the <bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept> ノードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Right-click and select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Select <bpt id="p1">**</bpt>InMemoryRealTime<ept id="p1">**</ept> as the value for the property <bpt id="p2">**</bpt>Usage<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ <bpt id="p2">**</bpt>Usage<ept id="p2">**</ept> の値として <bpt id="p1">**</bpt>InMemoryRealTime<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT9<ept id="p1">](./media/fmt9.png)](./media/fmt9.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMT9<ept id="p1">](./media/fmt9.png)](./media/fmt9.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>InMemoryRealTime aggregate models are deployed to SQL Server using Non-Clustered Column Store Index (NCCI) technology.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InMemoryRealTime 集計モデルは、非集合縦棒ストア インデックス (NCCI) 技術を使用して SQL Server に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>NCCIs is an in-memory technology that enables analytical and operational workloads to be served from SQL server database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NCCI は、分析および運用のワークロードを SQL Server データベースから供給できるメモリ内テクノロジーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>NCCI indexes can be defined on tables similar to any other index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NCCI インデックスは、他のインデックスのようなテーブルで定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>While NCCI indexes can be defined manually, framework has the ability to analyze index requirements and add them to underlying tables where necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NCCI インデックスは手動で定義することができますが、フレームワークにはインデックスの要件を分析して必要に応じて基になるテーブルに追加する機能があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Right-click <bpt id="p1">**</bpt>FMAggregateMeasurement<ept id="p1">**</ept> in Solution Explorer, and then click <bpt id="p2">**</bpt>Add Column store indices option<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで <bpt id="p1">**</bpt>FMAggregateMeasurement<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>列ストア インデックス オプション<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>You will notice several new indexes being added by the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の新しいインデックスがシステムによって追加されていることが分かります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Save and build the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを保存してビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>InMemoryRealTime aggregate models do not require data processing as the models are queried real-time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InMemoryRealTime 集計モデルは、モデルがリアルタイムで照会されるためデータの処理を必要としません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>If you have not enabled database synchronization along with the build, manually synchronize the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドと共にデータベースの同期が無効の場合は手動でデータベースを同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Model a KPI to show revenue per rental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI をモデル化してレンタルあたりの収益を表示する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Model a KPI in Visual Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio での KPI のモデル化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Model a KPI definition in Visual Studio by using the aggregate measurement you defined above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上で定義した集計の測定を使用して Visual Studio で KPI の定義をモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept>, point to <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>New Item<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> を右クリックして<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をポイントしてから<bpt id="p4">**</bpt>新しい項目<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Select <bpt id="p1">**</bpt>Dynamics 365 Artifacts<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Analytics<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Key Performance Indicator<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365コンポーネント<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>分析<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>主要業績評価指標<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Enter FMTRevenuePerRental as the name of the KPI, and then click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI の名前として FMTRevenuePerRental と入力し、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>The name must be unique across KPIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前は、KPI 間で一意でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>The KPI is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Select <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept>, and specify the <bpt id="p2">**</bpt>Measurement<ept id="p2">**</ept> Leave the default values for the other properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>測定<ept id="p2">**</ept> を指定します。その他のプロパティは既定値のままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Measurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">測定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>FMTAggregateMeasurement</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTAggregateMeasurement</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Bad Threshold</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なしきい値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Good Threshold</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なしきい値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Scoring Pattern</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スコアリング パターン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>MoreIsBetter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MoreIsBetter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Show Goal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目標の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Show Status and Trend</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステータスと傾向を表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Yes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Threshold Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しきい値タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Define the expression for the KPI value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI 値の式を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Under <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Value<ept id="p2">**</ept>, and specify the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept> で <bpt id="p2">**</bpt>値<ept id="p2">**</ept> を選択し、次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>The values must be entered in the order they appear in the table:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値はテーブルに表示されている順序で入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Value Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Value タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>BasedOnMeasure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BasedOnMeasure</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Measure Group</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メジャー グループ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>FMTRentalChargeExtendedView</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTRentalChargeExtendedView</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Measure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基準</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>RevenuePerRental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RevenuePerRental</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Define the expression for the KPI Goal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI 目標の式を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Select <bpt id="p1">**</bpt>Goal<ept id="p1">**</ept>, and specify the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>目標<ept id="p1">**</ept> を選択し、次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Goal Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目標タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>BasedOnValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BasedOnValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>250</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">250</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>You could have defined a goal based on an aggregate measure as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計測定に基づく目標を定義することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>In this case, we will define a number as the goal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、目標として番号を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Save the KPI definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI 定義を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Preview KPI in client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントで KPI をプレビュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Next you will preview the KPI definition in the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、クライアントで KPI 定義をプレビューします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Re-Build<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>再ビルド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>On completion of the build, select the <bpt id="p1">**</bpt>Synchronize ... database<ept id="p1">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドの完了時に、<bpt id="p1">**</bpt>同期...データベース<ept id="p1">**</ept>オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Open Internet Explorer, and navigate to your Rainier instance base URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を開き、Rainier インスタンスの基本 URL に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Navigate to the <bpt id="p1">**</bpt>Reservation Management workspace<ept id="p1">**</ept> under <bpt id="p2">**</bpt>App links<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Fleet Management<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Workspaces<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>Reservation Management<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>アプリのリンク<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>フリート管理<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>ワークスペース<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>予約管理<ept id="p5">**</ept>の <bpt id="p1">**</bpt>Reservation Management workspace<ept id="p1">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Select the KPI tile <bpt id="p1">**</bpt>Total Revenue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>総収益<ept id="p1">**</ept> KPI タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>KPI details page for T<bpt id="p1">**</bpt>otal Revenue<ept id="p1">**</ept> KPI will be displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>収益合計<ept id="p1">**</ept> KPI の KPI に関する詳細ページが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>To navigate to the newly defined KPI, select the <bpt id="p1">**</bpt>Show list<ept id="p1">**</ept> icon on top left.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく定義した KPI に移動するには、左上の <bpt id="p1">**</bpt>リストを表示<ept id="p1">**</ept> アイコンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>From the list of KPIs shown, select <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示される KPI のリストから <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept> を選択します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Notice that the KPI details page for the new KPI, <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept> is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい KPI の KPI に関する詳細ページ <bpt id="p1">**</bpt>FMTRevenuePerRental<ept id="p1">**</ept> が表示されることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Even though we did not define trend charts, the system created a set of charts based on the limited metadata defined by the developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレン グラフは定義しませんでしたが、開発者が定義した限定されたメタデータに基づいて一連のグラフが作成されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Users have the ability to modify KPI definitions and create new ones in the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、KPI 定義を変更して、クライアントに新しい定義を作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Next, you will modify the newly defined KPI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、新たに定義された KPI を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>To demonstrate this capability, you can change the KPI Goal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を示すために、KPI 目標を変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Click the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button on top left, and enter 900 as the Goal Value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左上の<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタンをクリックし、目標値として 900 を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Modify the threshold properties as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のようにしきい値のプロパティを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Threshold Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しきい値タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Percentage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーセンテージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Red if less than</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の値未満の場合に赤</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>90</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">90</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Green if more than</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の値を超えた場合に緑</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>110</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">110</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> on the bottom left to save changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存するには、左下の<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Notice that the KPI status color has changed in the KPI tile shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KPI の状態の色が表示される KPI タイルで変更されたことに注意します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>