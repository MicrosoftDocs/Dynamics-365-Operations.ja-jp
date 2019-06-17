<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="build-navigation.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>build-navigation.c1cdc2.653ed097932674e9a78e6363c69f473207cc6eae.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>653ed097932674e9a78e6363c69f473207cc6eae</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\build-navigation.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build navigation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーションの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you will add navigational elements to a workspace and the navigation pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、ワークスペースとナビゲーション ウィンドウにナビゲーション要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Build navigation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーションの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In this tutorial, you will add navigational elements to a workspace and the navigation pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、ワークスペースとナビゲーション ウィンドウにナビゲーション要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For this tutorial, you need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For more information, see <bpt id="p1">[</bpt>Access Instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A <bpt id="p1">*</bpt>workspace<ept id="p1">*</ept> is an overview page that is specific to a particular subject area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ワークスペース<ept id="p1">*</ept>は、特定のサブジェクト領域固有の概要ページです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Workspaces are common to all users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースはすべてのユーザーに共通です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In this tutorial, you will add content into an existing workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、既存のワークスペースにコンテンツを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The <bpt id="p1">*</bpt>dashboard<ept id="p1">*</ept> is the default home page for each user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ダッシュボード<ept id="p1">*</ept>は、ユーザーごとの既定のホーム ページです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">*</bpt>Tiles<ept id="p1">*</ept> are securable objects that can be shown on a workspace or the dashboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>タイル<ept id="p1">*</ept>はワークスペースまたはダッシュボードに表示できるセキュリティ保護可能なオブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>They can be secured by using menu items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、メニュー項目を使用して保護できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">段取り</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If this is the first tutorial that you are working on, review <bpt id="p1">[</bpt>Access Instances<ept id="p1">](../dev-tools/access-instances.md)</ept> and make sure that you provision your administrator user if you are working on a local VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが作業する最初のチュートリアルである場合は、<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Import the tutorial project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If you have already imported the Fleet management tutorial project, skip to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアル プロジェクトを既にインポートした場合は、次のセクションに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Download the Fleet Management sample from <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph>, save it to <bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept>, and unzip it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理のサンプルを <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph> からダウンロードし、<bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept> に保存してから解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In Visual Studio, on the <bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Import Project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の、<bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>プロジェクトのインポート<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> window, next to the <bpt id="p2">**</bpt>Filename<ept id="p2">**</ept> text box, click the ellipsis button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>ファイル名<ept id="p2">**</ept>テキスト ボックスの隣にある、省略記号ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In the <bpt id="p1">**</bpt>Select the file to import<ept id="p1">**</ept> window, browse to <bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept>, click <bpt id="p3">**</bpt>FMTutorialDataModel.axpp,<ept id="p3">**</ept> and then click <bpt id="p4">**</bpt>Open<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポートするファイルの選択<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept> を参照して <bpt id="p3">**</bpt>FMTutorialDataModel.axpp<ept id="p3">**</ept> をクリックしてから<bpt id="p4">**</bpt>開く<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In the Project file location text box, enter <bpt id="p1">**</bpt>C:\FMLab.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト ファイルの場所テキスト ボックスに、<bpt id="p1">**</bpt>C:\FMLab<ept id="p1">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Select the <bpt id="p1">**</bpt>Overwrite Elements<ept id="p1">**</ept> option, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要素の上書き<ept id="p1">**</ept> オプションをオンにし、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Import transactional data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In Visual Studio, open the <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the <bpt id="p1">**</bpt>Open Project<ept id="p1">**</ept> dialog box, browse to C:\FMLab\FMTutorial, and then click FMTutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトを開く<ept id="p1">**</ept>ダイアログ ボックスで、C:\FMLab\FMTutorial を参照してから FMTutorial をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> project appears in <bpt id="p2">**</bpt>Solution Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> プロジェクトが<bpt id="p2">**</bpt>ソリューション エクスプローラー<ept id="p2">**</ept>に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Use the FMTDataHelper class to load data for the Fleet Management tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアルのデータを読み込むには、FMTDataHelper クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, in the FMTutorial project, expand <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept>, right-click <bpt id="p3">**</bpt>FMTDataHelper<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Set as Startup Object<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の FMTutorial プロジェクトで、<bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>を展開して、<bpt id="p3">**</bpt>FMTDataHelper<ept id="p3">**</ept> を右クリックしてから、<bpt id="p4">**</bpt>スタートアップ オブジェクトとして設定<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>From the <bpt id="p1">**</bpt>BUILD<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Rebuild Solution<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューから、<bpt id="p2">**</bpt>ソリューションの再構築<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>You use the rebuild to update the timestamps of the imported artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたアーティファクトのタイムスタンプを更新するには、リビルドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can view the build progress in the <bpt id="p1">**</bpt>Output<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力<ept id="p1">**</ept> ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project and load the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行し、データを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Add a tile to the tutorial workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル ワークスペースへのタイルの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>First, we will add a new tile to the form FMTClerkWorkspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、FMTClerkWorkspace のフォームに新しいタイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, expand <bpt id="p2">**</bpt>Forms<ept id="p2">**</ept> and then double-click <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>フォーム<ept id="p2">**</ept>を展開してから、<bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>In the designer, expand <bpt id="p1">**</bpt>PanoramaBody<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>PanoramaBody<ept id="p1">**</ept> を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Right-click <bpt id="p1">**</bpt>TileContainer<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Tile Button.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TileContainer<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>ボタンを並べて表示<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Specify the following properties for the new tile button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタイル ボタンの次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Test tile</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイルをテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Tile</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>FMTAllCustomersTile</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTAllCustomersTile</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This will create a duplicate of the existing <bpt id="p1">**</bpt>All customers<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、既存の<bpt id="p1">**</bpt>すべての顧客<ept id="p1">**</ept>タイルの複製が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Forms<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept>, right-click, and then select <bpt id="p4">**</bpt>Set as Start-up Object<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>フォーム<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> とクリックし、右クリックしてから<bpt id="p4">**</bpt>スタートアップ オブジェクトとして設定<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Setting a start-up object is necessary to allow Visual Studio to launch when you press Ctrl+F5 in step 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタートアップ オブジェクトを設定することは、手順 7 で Ctrl + F5 キーを押すと Visual Studio が起動するために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Setting this form as the start-up object will cause the work-in-progress Fleet management clerk workspace to appear after you press Ctrl+F5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">起動オブジェクトとしてこのフォームを設定すると、Ctrl + F5 キーを押した後に、進行中のフリート管理係ワークスペースが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>We will preview this form again later in detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で再度このフォームを詳細にプレビュー表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Rebuild<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>再ビルド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>After you build and run the project, the Fleet management clerk workspace will launch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをビルドして実行すると、フリート管理係ワークスペースが起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The new tile named, <bpt id="p1">**</bpt>Test tile<ept id="p1">**</ept>, that you created will be included in the first section of the workspace, at the end of the set of tiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成した <bpt id="p1">**</bpt>テスト タイル<ept id="p1">**</ept> という名前の新しいタイルは、タイルのセットの最後にある、ワークスペースの最初のセクションに含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav1<ept id="p1">](./media/nav1.png)](./media/nav1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav1<ept id="p1">](./media/nav1.png)](./media/nav1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The tile will not navigate anywhere when clicked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイルがクリックされたとき、どこにも移動しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>To enable this, you can define a Menu Item Name on FMTAllCustomersTile, under <bpt id="p1">**</bpt>Tiles<ept id="p1">**</ept> in <bpt id="p2">**</bpt>Solution Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを有効にするには、<bpt id="p2">**</bpt>ソリューション エクスプローラー<ept id="p2">**</ept> の<bpt id="p1">**</bpt>タイル<ept id="p1">**</ept>の下にあるメニュー項目名を FMTAllCustomersTile に定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Add a new workspace to the navigation pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション ウィンドウへの新しいワークスペースの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Next, we will add the FMTClerkWorkspace form to the navigation pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、FMTClerkWorkspace フォームをナビゲーション ウィンドウに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>We will do this in two locations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを次の 2 つの場所で実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The <bpt id="p1">**</bpt>All workspaces<ept id="p1">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべてのワークスペース<ept id="p1">**</ept> リスト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>A new item in the area list containing a menu structure that shows the workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースを示すメニュー構造を含む領域のリストにある新しい項目。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Create a menu item that points to the FMTClerkWorkspace workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTClerkWorkspace ワークスペースを指すメニュー項目を作成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>New Item<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>追加<ept id="p2">**</ept> をポイントしてから <bpt id="p3">**</bpt>新しい項目<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Click <bpt id="p1">**</bpt>AX Artifacts<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Display Menu Item<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AX アーティファクト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>表示メニュー項目<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property, enter <bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>プロパティで、<bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Specify the following properties for the new menu item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメニュー項目の次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Reservation management tutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予約管理チュートリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>FMTClerkWorkspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTClerkWorkspace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Create a tile that points to the FMTClerkWorkspace workspace menu item</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTClerkWorkspace ワークスペース メニュー項目をポイントするタイルを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>New Item<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>追加<ept id="p2">**</ept> をポイントしてから <bpt id="p3">**</bpt>新しい項目<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Click <bpt id="p1">**</bpt>AX Artifacts<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Tile<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AX アーティファクト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>タイル<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property, enter <bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>プロパティで、<bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Specify the following properties for the new tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタイルの次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>MenuItemName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MenuItemName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>FMTClerkWorkspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTClerkWorkspace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Add a menu extension for the navigation pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション ウィンドウのメニューの拡張機能を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>In <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Menus<ept id="p3">**</ept>, right-click <bpt id="p4">**</bpt>NavPaneMenu<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>Create extension<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>メニュー<ept id="p3">**</ept>とクリックし、<bpt id="p4">**</bpt>NavPaneMenu<ept id="p4">**</ept> を右クリックしてから<bpt id="p5">**</bpt>拡張機能を作成<ept id="p5">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>NavPaneMenu.Extension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>NavPaneMenu.Extension<ept id="p2">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In the designer, right-click <bpt id="p1">**</bpt>NavPaneMenu.Extension<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Submenu<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>NavPaneMenu.Extension<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>をポイントしてから<bpt id="p3">**</bpt>サブメニュー<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Select the new submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいサブメニューを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property, enter <bpt id="p2">**</bpt>NavPaneMenuFleetTutorial<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>プロパティで、<bpt id="p2">**</bpt>NavPaneMenuFleetTutorial<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>, locate the <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> tile, and drag it onto the newly created submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>または<bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> タイルを探し、新しく作成されたサブメニューにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Rebuild<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>再ビルド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>After you build and run the project, the navigation pane will contain a link to the new workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをビルドして実行すると、ナビゲーション ウィンドウに新しいワークスペースへのリンクが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Open the navigation pane by clicking the navigation pane button (three lines) at the top right of the application window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ウィンドウの右上にある、ナビゲーション ウィンドウのボタン (3 つの明細行) をクリックして、ナビゲーション ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav2<ept id="p1">](./media/nav2.png)](./media/nav2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav2<ept id="p1">](./media/nav2.png)](./media/nav2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>When you open the navigation pane, select <bpt id="p1">**</bpt>All workspaces<ept id="p1">**</ept>, and scroll down in the list after it opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション ウィンドウを開いたら、<bpt id="p1">**</bpt>すべてのワークスペース<ept id="p1">**</ept> を選択し、それを開いた後、一覧を下方向にスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>You should see the following new Reservation management tutorial workspace in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の新しい予約管理チュートリアル ワークスペースが一覧に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav3<ept id="p1">](./media/nav3.png)](./media/nav3.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav3<ept id="p1">](./media/nav3.png)](./media/nav3.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Add the form to the main menu structure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン メニュー構造へのフォームの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Now you’ll add a new main menu section that contains a tile that points to the tutorial workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、チュートリアル ワークスペースを示すタイルを含む新しいメイン メニュー セクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>You will then add a link to the same form in this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、このセクションの同じフォームにリンクを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>This will demonstrate the appearance of a non-workspace form link.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、非ワークスペースのフォーム リンクの外観を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>In Visual Studio, in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept>, point to <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>New Item<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の、<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> を右クリックして、<bpt id="p3">**</bpt>追加<ept id="p3">**</ept> をポイントしてから、<bpt id="p4">**</bpt>新しい項目<ept id="p4">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Click <bpt id="p1">**</bpt>AX Artifacts<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Menu<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AX アーティファクト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>メニュー<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property, enter <bpt id="p2">**</bpt>FleetManagementTutorial<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>プロパティで、<bpt id="p2">**</bpt>FleetManagementTutorial<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click the new menu <bpt id="p2">**</bpt>FleetManagementTutorial<ept id="p2">**</ept> if it isn’t already open.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、新しいメニュー <bpt id="p2">**</bpt>FleetManagementTutorial<ept id="p2">**</ept> をまだ開いていない場合はダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In the properties list, set the <bpt id="p1">**</bpt>Label<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Fleet management tutorial<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ リストで、<bpt id="p1">**</bpt>ラベル<ept id="p1">**</ept> プロパティを<bpt id="p2">**</bpt>フリート管理のチュートリアル<ept id="p2">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>In the designer, right-click <bpt id="p1">**</bpt>FleetManagementTutorial<ept id="p1">**</ept>, and click <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Submenu<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>FleetManagementTutorial<ept id="p1">**</ept> を右クリックして、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>サブメニュー<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Specify the following properties for the new submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいサブメニューの次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>, locate the <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> display menu item and drag it onto the new <bpt id="p4">**</bpt>Workspaces<ept id="p4">**</ept> submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>または<bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> 表示メニュー項目を探し、新しい<bpt id="p4">**</bpt>ワークスペース<ept id="p4">**</ept> サブメニューにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>In the designer, right-click <bpt id="p1">**</bpt>FleetManagementTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Submenu<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>FleetManagementTutorial<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>サブメニュー<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Specify the following properties for the new submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいサブメニューの次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Common</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共通</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Label</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Common</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共通</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>, locate the <bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> display menu item and drag it onto the new <bpt id="p4">**</bpt>Common<ept id="p4">**</ept> submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>または<bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>FMTClerkWorkspace<ept id="p3">**</ept> 表示メニュー項目を探し、新しい<bpt id="p4">**</bpt>共通<ept id="p4">**</ept>サブメニューにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>In <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>User Interface<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Menus<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>MainMenu<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>ユーザー インターフェイス<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>メニュー<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>MainMenu<ept id="p4">**</ept> とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Right-click <bpt id="p1">**</bpt>MainMenu<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Create extension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MainMenu<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>拡張子の作成<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, locate and open the new extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で新しい拡張機能を探して開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Select and double-click <bpt id="p1">**</bpt>MainMenu.Extension<ept id="p1">**</ept> to open it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MainMenu.Extension<ept id="p1">**</ept> を選択し、ダブルクリックして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In the designer, right click <bpt id="p1">**</bpt>MainMenu.Extension<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Menu reference<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>MainMenu.Extension<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>をポイントしてから<bpt id="p3">**</bpt>メニュー参照<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Specify the following properties for the new menu reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメニュー参照の次のプロパティを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>FleetManagementTutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetManagementTutorial</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Menu Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>FleetManagementTutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetManagementTutorial</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Build<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>ビルド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Go to the main menu section you just modified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更したメイン メニューのセクションに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Open the navigation pane and scroll down until you see the new top-level <bpt id="p1">**</bpt>Fleet management tutorial<ept id="p1">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション ウィンドウを開いて、新しいトップレベルの<bpt id="p1">**</bpt>フリート管理のチュートリアル<ept id="p1">**</ept>メニューが表示されるまでスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>You may need to clear your browser cache by pressing <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> を押して、ブラウザー キャッシュをクリアすることが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav4<ept id="p1">](./media/nav4.png)](./media/nav4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav4<ept id="p1">](./media/nav4.png)](./media/nav4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Click <bpt id="p1">**</bpt>Fleet management tutorial<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Workspaces<ept id="p2">**</ept> to expand that submenu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのサブメニューを展開するには、<bpt id="p1">**</bpt>フリート管理のチュートリアル<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ワークスペース<ept id="p2">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Your navigation pane should look like the following.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション ウィンドウは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav5<ept id="p1">](./media/nav5.png)](./media/nav5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Nav5<ept id="p1">](./media/nav5.png)](./media/nav5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If you click on the <bpt id="p1">**</bpt>Common<ept id="p1">**</ept> submenu, you will see the menu item that you modeled there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一般的な<ept id="p1">**</ept> サブメニューをクリックすると、モデル化されているメニュー項目が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>You can click either of these links to check that you have set up the references correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのリンクのいずれかをクリックして、参照を正しく設定したか確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>If you have set up the references correctly, the tutorial workspace you’re working on should open when clicked on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照を正しく設定した場合は、作成中のチュートリアル ワークスペースをクリックすると、開きます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>