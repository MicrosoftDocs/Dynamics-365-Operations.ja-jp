<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="build-extensible-control.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>build-extensible-control.abbbca.073c13cd083f6053b1e59011dd4c8c4a57e924de.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>073c13cd083f6053b1e59011dd4c8c4a57e924de</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\build-extensible-control.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build extensible controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コントロールの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to create new application controls that have a property sheet in Visual Studio and have server-side business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Visual Studio にプロパティ シートを持ち、サーバーサイドのビジネス ロジックを持つ新しいアプリケーション コントロールを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Build extensible controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how to create new application controls that have a property sheet in Visual Studio and have server-side business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Visual Studio にプロパティ シートを持ち、サーバーサイドのビジネス ロジックを持つ新しいアプリケーション コントロールを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For this tutorial, you must access the environment by using Remote Desktop, and you must be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For more information, see <bpt id="p1">[</bpt>Access development instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>開発インスタンスへのアクセス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The Control Extensibility Framework lets you create new application controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール拡張フレームワークを使用すると、新しいアプリケーション コントロールを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can use the same tools that Microsoft uses to build controls that are already present in the program, such as the chart control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft では、グラフ コントロールなど、プログラムで既に記述されている制御を構築するために使用するのと同じツールを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Three important artifacts are involved in the process of developing an extensible control:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールを開発するプロセスには、次の 3 つの重要なアーティファクトが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>The X++ build class<ept id="p1">**</ept> – The build class lets a developer define the properties that appear in the Microsoft Visual Studio property sheet for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>X++ ビルド クラス<ept id="p1">**</ept> – ビルド クラスにより開発者は、コントロールの Microsoft Visual Studio のプロパティ シートに表示されるプロパティを定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The developer can also define the modeling behavior for the control when it's used in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、コントロールがフォーム デザイナーで使用されているときに、コントロールのモデリング動作を定義することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The build class is consumed by the run-time class to initialize the state of the control based on the value of properties in the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド クラスは、プロパティ シートのプロパティの値に基づいてコントロールの状態を初期化するために、ランタイム クラスによって消費されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>The X++ run-time class<ept id="p1">**</ept> – The run-time class lets a developer define server-side business logic and data access patterns for an extensible control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>X++ ランタイム クラス<ept id="p1">**</ept> – ランタイム クラスにより開発者は、拡張可能なコントロールのサーバー側のビジネス ロジックとデータへのアクセスのパターンを定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Two concepts that are specific to building extensible controls are the <bpt id="p1">*</bpt>properties<ept id="p1">*</ept> and <bpt id="p2">*</bpt>commands<ept id="p2">*</ept> that the X++ class defines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールのビルドに特有の概念には、X++ クラスで定義される<bpt id="p1">*</bpt>プロパティ<ept id="p1">*</ept>と<bpt id="p2">*</bpt>コマンド<ept id="p2">*</ept>の 2 つがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Each property and command that is defined is serialized into a JavaScript view model at run time, and can be consumed by the client parts of the extensible control (the HTML and JavaScript).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義されている各プロパティとコマンドは、実行時に JavaScript ビュー モデルにシリアル化され、拡張可能なコントロール (HTML および JavaScript) のクライアント部分によって消費される可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These properties and commands are the main channels for moving information between the server-side and client-side parts of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロパティとコマンドは、コントロールのサーバー側とクライアント側の間で情報を移動するための主要なチャネルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>The control HTML and JavaScript<ept id="p1">**</ept> – Each control uses HTML, JavaScript, and CSS files to define control visualization and client-side interaction patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール HTML および JavaScript<ept id="p1">**</ept> – 各コントロールは、視覚化およびクライアント側の相互作用パターンの制御を定義するために HTML、JavaScript および CSS ファイルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>By using the Microsoft Dynamics HTML binding syntax together with jQuery, a developer can consume the properties and commands that are defined in X++ to design powerful data-driven UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">jQuery と共に Microsoft Dynamics HTML バインディング構文を使用することで、開発者は強力なデータ駆動型 UI を設計するために X++ で定義されているプロパティとコマンドを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>All three artifacts of extensible control development are explained in more detail in the following sections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コントロール開発のすべての 3 つのコンポーネントについては、以降のセクションで詳しく説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Defining an extensible control's design-time behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールのデザイン時の動作を定義する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Defining an extensible control's run-time behavior</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な実行デザイン時の動作を定義する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Defining an extensible control's view by using HTML and CSS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML と CSS を使用して、拡張可能なコントロールのビューを定義する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Defining an extensible control's view model by using JavaScript</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JavaScript を使用して拡張可能なコントロールのビュー モデルを定義する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Import the tutorial project and transactional data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトおよびトランザクション データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Use Visual Studio to import the tutorial project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The tutorial project includes the artifacts that you will use to complete this tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You will use the <bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> class to load data for the Fleet Management tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアルのデータを読み込むために、<bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Download the Fleet Management sample from <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph>, save it to <bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept>, and unzip it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理のサンプルを <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph> からダウンロードし、<bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept> に保存してから解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>On the desktop, double-click the Visual Studio shortcut to open the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>On the <bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **menu, click **Import Project<ept id="p1">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **メニューで、**プロジェクトのインポート<ept id="p1">&lt;/strong&gt;</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> dialog box, next to the <bpt id="p2">**</bpt>File name<ept id="p2">**</ept> text box, click the ellipsis button (...).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>ファイル名<ept id="p2">**</ept>テキスト ボックスの隣にある、省略記号ボタン (...) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In the <bpt id="p1">**</bpt>Select the file to import<ept id="p1">**</ept> dialog box, browse to <bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept>, click <bpt id="p3">**</bpt>FMTutorialDataModel.axpp<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Open<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポートするファイルの選択<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept> を参照して <bpt id="p3">**</bpt>FMTutorialDataModel.axpp<ept id="p3">**</ept> をクリックしてから<bpt id="p4">**</bpt>開く<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In the <bpt id="p1">**</bpt>Project file location<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト ファイルの場所<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Select the <bpt id="p1">**</bpt>Overwrite Elements<ept id="p1">**</ept> check box and the <bpt id="p2">**</bpt>Current solution<ept id="p2">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要素の上書き<ept id="p1">**</ept> チェック ボックスをオンにし、<bpt id="p2">**</bpt>現在のソリューション<ept id="p2">**</ept> オプションをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The following screen shot shows the completed <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、完了した <bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ダイアログボックスを示しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext1<ept id="p1">](./media/ext1.png)](./media/ext1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext1<ept id="p1">](./media/ext1.png)](./media/ext1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In Solution Explorer, under the <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> project, expand <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーの <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> プロジェクトで<bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Right-click <bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Set as Startup Object<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>スタートアップ オブジェクトとして設定<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>On the <bpt id="p1">**</bpt>BUILD<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Rebuild Solution<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>ソリューションの再構築<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You use the rebuild to make sure that all the files in the project are built, regardless of timestamps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You can view the build progress in the <bpt id="p1">**</bpt>Output<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力<ept id="p1">**</ept> ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>After the build is completed, press Ctrl+F5 to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドが完了した後、Ctrl + F5 を押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>Login<ept id="p1">**</ept> form closes when authentication succeeds, and then the data is loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ログイン<ept id="p1">**</ept> フォームは、認証が成功すると閉じ、データが読み込まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Set up aggregate data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集計データの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Use FMTAggregateMeasurements to populate the Microsoft SQL Server Analysis Services database with aggregate data.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">FMTAggregateMeasurements を使用して、Microsoft SQL Server Analysis Services データベースに集計データを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>These steps must be completed immediately after you use the <bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> class to import data.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">これらの手順は <bpt id="p1">**</bpt>FMTDataHelper<ept id="p1">**</ept> クラスを使用してデータをインポートした直後に完了する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>You may <bpt id="p1">**</bpt>NOT<ept id="p1">**</ept> need to do these steps if the <bpt id="p2">[</bpt>aggregate measure is "InMemoryRealTime"<ept id="p2">](../analytics/model-aggregate-data.md)</ept>, depending on what tutorial files you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所持しているチュートリアル ファイルに応じて、<bpt id="p2">[</bpt>集計尺度が "InMemoryRealTime"<ept id="p2">](../analytics/model-aggregate-data.md)</ept> の場合に、これらのステップを実行する必要が <bpt id="p1">**</bpt>ない<ept id="p1">**</ept> 場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In Solution Explorer, under <bpt id="p1">**</bpt>Analytics<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーの<bpt id="p1">**</bpt>分析<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTAggregateMeasurement<ept id="p2">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In the designer, right-click <bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Deploy and Process<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、<bpt id="p1">**</bpt>FMTAggregateMeasurement<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>配置と処理<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Preview the clerk workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラーク ワークスペースをプレビュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Before you begin to build the contact control, look at the appearance of the current implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールの構築を開始する前に、現在の実装の外観を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the following sections, you will use the Control Extensibility Framework to enrich the visualization of the controls and the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、コントロール拡張フレームワークを使用して、コントロールとフォームの視覚化を強化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In Solution Explorer, expand <bpt id="p1">**</bpt>Forms<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Set as Startup Object<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>FMTClerkWorkspace<ept id="p2">**</ept> を右クリックしてから、<bpt id="p3">**</bpt>スタートアップ オブジェクトとして設定<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Press Ctrl+F5 to open the <bpt id="p1">**</bpt>Fleet management clerk<ept id="p1">**</ept> page in Internet Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+F5 キーを押して、Internet Explorer で <bpt id="p1">**</bpt>フリート管理係<ept id="p1">**</ept> ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>As the following screen shot shows, the data on this page appears as a simple grid in a list style that contains several string and date controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに示されているように、複数の文字列および日付を含むリスト スタイルの単純なグリッドとしてこのページではデータが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext2<ept id="p1">](./media/ext2-1024x515.png)](./media/ext2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext2<ept id="p1">](./media/ext2-1024x515.png)](./media/ext2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Exit Internet Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Modify the build class for the contact control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールのビルド クラスの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To save time, you will work on a partially completed extensible control that is named the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間を節約するために、連絡先コントロールと呼ばれる部分的に完了した拡張可能なコントロールで作業します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>You will extend the contact control to complete its design, run-time, and visualization behaviors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールを拡張して、そのデザイン、実行時、および視覚化の動作を完成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The partially completed contact control already supports multiple title fields, subfields, and action buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">部分的に完了した連絡先コントロールは、複数のタイトル フィールド、サブフィールド、およびアクション ボタンを既にサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>However, it doesn't currently support an image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、現在画像はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To add image support, you must extend the design experience for the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ サポートを追加するには、連絡先管理のデザイン エクスペリエンスを拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>You will add a data field that can specify image data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ データを指定可能なデータ フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Technical overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>To see an example of a build class, in Solution Explorer, expand <bpt id="p1">**</bpt>Classes<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>View Code<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド クラスの例を表示するには、ソリューション エクスプローラーで <bpt id="p1">**</bpt>クラス<ept id="p1">**</ept> を展開し、<bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> を右クリックして、<bpt id="p3">**</bpt>コードを表示<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The class code appears in the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターにクラス コードが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> is the build class for the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> は連絡先コントロールのビルド クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>For each extensible control, the build class defines the properties that the control shows in the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各拡張可能コントロールについては、ビルド クラスは、コントロールがプロパティ シートに表示されるプロパティを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The build class also defines the modeling experience for the control in the Visual Studio form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド クラスは、Visual Studio フォーム デザイナーのコントロールのモデリング経験も定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>There are three primary design-time behaviors that you can define for an extensible control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールには、3 つの主要なデザイン時のビヘイビアを定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Each behavior is declaratively defined by using a <bpt id="p1">**</bpt>FormDesign<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各動作では、<bpt id="p1">**</bpt>FormDesign<ept id="p1">**</ept> 属性を使用して宣言的に定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Here are the design-time behaviors that you can define:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義できるデザイン時の動作を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> – You can specify the control name that appears in the form designer when you add the control to a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept> – コントロールをフォームに追加すると、フォーム デザイナに表示されるコントロール名を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>To specify the name, add a <bpt id="p1">**</bpt>FormDesignControlAttribute<ept id="p1">**</ept> attribute to the build class declaration of the extensible control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前を指定するには、拡張可能コントロールのビルド クラス宣言に <bpt id="p1">**</bpt>FormDesignControlAttribute<ept id="p1">**</ept> 属性を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For example, the following declaration of the <bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> class shows the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の <bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> クラスの申告は、属性を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x1<ept id="p1">](./media/x1.png)](./media/x1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x1<ept id="p1">](./media/x1.png)](./media/x1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">**</bpt>Designer properties<ept id="p1">**</ept> – These are the properties that you see in the property sheet when you add the control to a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイナー プロパティ<ept id="p1">**</ept> - これらは、コントロールをフォームに追加すると、プロパティ シートに表示されるプロパティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>There are several attributes that let you add various types of designer properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまなタイプのデザイナー プロパティを追加できる属性がいくつかあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>For example, the <bpt id="p1">**</bpt>FormDesignPropertyAttribute<ept id="p1">**</ept> attribute adds a property to the property sheet, and the property name and the section are supplied as arguments to the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>FormDesignPropertyAttribute<ept id="p1">**</ept> 属性はプロパティ シートにプロパティを追加し、プロパティ名およびセクションが属性への引数として指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For example, the following code adds the <bpt id="p1">**</bpt>Action Name<ept id="p1">**</ept> property to the <bpt id="p2">**</bpt>FMTContactControlAction<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のコードは、<bpt id="p1">**</bpt>アクション名<ept id="p1">**</ept>プロパティを <bpt id="p2">**</bpt>FMTContactControlAction<ept id="p2">**</ept> クラスに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x2<ept id="p1">](./media/x2.png)](./media/x2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x2<ept id="p1">](./media/x2.png)](./media/x2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The following screen shot shows how this property appears in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、このプロパティが Visual Studio の <bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウにどのように表示されるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext3<ept id="p1">](./media/ext3.png)](./media/ext3.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext3<ept id="p1">](./media/ext3.png)](./media/ext3.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Child design components<ept id="p1">**</ept> – These are child nodes that you see after you add the control to a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>子デザイン コンポーネント<ept id="p1">**</ept> - これらは、コントロールをフォームに追加した後に表示される子ノードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>There are two types of child design components: leaf and leaf collection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子の設計コンポーネントには、リーフとリーフ コレクションの 2 つのタイプがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>A leaf is defined by using a <bpt id="p1">**</bpt>FormDesignComponentAttribute<ept id="p1">**</ept> attribute on an X++ method that accepts or returns another build class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リーフは、別のビルド クラスを受け入れるか、返す X++ メソッドの <bpt id="p1">**</bpt>FormDesignComponentAttribute<ept id="p1">**</ept> 属性を使用して定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The build class determines the properties that the leaf has in the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド クラスは、リーフがプロパティ シートに持つプロパティを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>A leaf collection is defined by using a <bpt id="p1">**</bpt>FormDesignComponentCollectionAttribute<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormDesignComponentCollectionAttribute<ept id="p1">**</ept> 属性を使用して定義されるリーフ コレクション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The allowable leaf types for the collection are defined by using <bpt id="p1">**</bpt>FormDesignComponentValidChildAttribute<ept id="p1">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コレクションの許容リーフ タイプは、<bpt id="p1">**</bpt>FormDesignComponentValidChildAttribute<ept id="p1">**</ept> 属性を使用して定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For example, the following code adds a leaf collection that is named <bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> for the <bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次のコードは、<bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> クラスの<bpt id="p1">**</bpt>アクション<ept id="p1">**</ept>という名前のリーフ コレクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x3<ept id="p1">](./media/x3.png)](./media/x3.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x3<ept id="p1">](./media/x3.png)](./media/x3.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The following screen shot shows how the specified child design component appears when you add the control to a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットは、コントロールをフォームに追加する場合に、指定された子デザイン コンポーネントがどのように表示されるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext4<ept id="p1">](./media/ext4.png)](./media/ext4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext4<ept id="p1">](./media/ext4.png)](./media/ext4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Tutorial steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルの手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Check that the code for the <bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> class appears in the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターで表示される <bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> クラスのコードを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>If it doesn't, in Solution Explorer, expand <bpt id="p1">**</bpt>Classes<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>View Code<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうされない場合は、ソリューション エクスプローラーで<bpt id="p1">**</bpt>クラス<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> を右クリックして、<bpt id="p3">**</bpt>コードを表示<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Add a child design component to the FMTBuildContactControl class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子デザイン コンポーネントを FMTBuildContactControl クラスに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>A child design component lets a developer who places the control in a form to specify the image that appears on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">子デザイン コンポーネントを使用すると、フォームにコントロールを設置した開発者は、コントロールに表示されるイメージを指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>In this step, you will add the <bpt id="p1">**</bpt>FormDesignComponentAttribute<ept id="p1">**</ept> attribute to create a new entry in the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、<bpt id="p1">**</bpt>FormDesignComponentAttribute<ept id="p1">**</ept> 属性を追加して、プロパティ シートに新しいエントリを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You will then add the <bpt id="p1">**</bpt>FormDesignPropertyDataFieldAttribute<ept id="p1">**</ept> attribute, which indicates that the new designer property enables the selection of a data field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p1">**</bpt>FormDesignPropertyDataFieldAttribute<ept id="p1">**</ept> 属性を追加します。この属性は、新しいデザイナー プロパティがデータ フィールドの選択を使用可能にすることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Add the highlighted code that follows to the declarations for the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの申告に次の強調表示されたコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This code adds the <bpt id="p1">**</bpt>FormBindingDataField<ept id="p1">**</ept> field to the X++ that the <bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> class is using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、<bpt id="p2">**</bpt>FMTBuildContactControl<ept id="p2">**</ept> クラスが使用している X++ に <bpt id="p1">**</bpt>FormBindingDataField<ept id="p1">**</ept> フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x4<ept id="p1">](./media/x4.png)](./media/x4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x4<ept id="p1">](./media/x4.png)](./media/x4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Add the following code to the <bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTBuildContactControl<ept id="p1">**</ept> クラスに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Add this method after the designer property for the data source.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">データ ソースのデザイナー プロパティの後に、このメソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x5<ept id="p1">](./media/x5.png)](./media/x5.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x5<ept id="p1">](./media/x5.png)](./media/x5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The child design component will show the properties that are available on the <bpt id="p1">**</bpt>FormBindingDataField<ept id="p1">**</ept> build class.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">子デザイン コンポーネントは <bpt id="p1">**</bpt>FormBindingDataField<ept id="p1">**</ept> ビルド クラスで使用可能なプロパティを表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>This is appropriate, because you want to enable image data binding to a data field and data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、データ フィールドとデータ ソースへのイメージ データのバインドを有効にするために適しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>This is all that is required to add a designer property to the build class of the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、連絡先コントロールのビルド クラスにデザイナー プロパティを追加するために必要なものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Press Ctrl+S to save your changes, and then close the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+S キーを押して変更を保存し、コード エディターを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>In Solution Explorer, right-click <bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Build<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMTutorial<ept id="p1">**</ept> を右クリックしてから<bpt id="p2">**</bpt>ビルド<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the <bpt id="p1">**</bpt>FMTPickingUpTodayPart<ept id="p1">**</ept> form isn't already open, expand <bpt id="p2">**</bpt>Forms<ept id="p2">**</ept>, and then double-click <bpt id="p3">**</bpt>FMTPickingUpTodayPart<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTPickingUpTodayPart<ept id="p1">**</ept> フォームが既に開かれている場合、<bpt id="p2">**</bpt>フォーム<ept id="p2">**</ept>を展開し、<bpt id="p3">**</bpt>FMTPickingUpTodayPart<ept id="p3">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The form opens in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In the form designer, expand <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>PickingUpTodayGrid<ept id="p2">**</ept>, and then select and delete the controls that currently appear in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>PickingUpTodayGrid<ept id="p2">**</ept> を展開してから、グリッドに表示されているコントロールを選択して削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Right-click <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>FMTContactControl<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>FMTContactControl<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Expand the <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> node, and notice that <bpt id="p2">**</bpt>Image<ept id="p2">**</ept> appears as a new child design component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> ノードを展開し、<bpt id="p2">**</bpt>画像<ept id="p2">**</ept>が新しい子デザイン コンポーネントとして表示されることを通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following illustration shows the contact control in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、フォーム デザイナーの連絡先コントロールを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext5<ept id="p1">](./media/ext5.png)](./media/ext5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext5<ept id="p1">](./media/ext5.png)](./media/ext5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>You must also update the run-time class for the contact control to consume the design-time changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時の変更を使用する連絡先管理のための実行時クラスを更新することも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>You will revisit adding the control to the form and specifying data bindings and property values later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームにコントロールを追加し、後でデータ バインドとプロパティ値を指定することを再検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Press Ctrl+S to save your changes, and then close the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+S キーを押して変更を保存し、フォーム デザイナーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Modify the runtime class for the contact control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールのランタイム クラスの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Next, you must modify the run-time class to read the data source and data field for the image from the build class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、ランタイム クラスを変更して、ビルド クラスからイメージのデータ ソースとデータ フィールドを読み取る必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>You must also create a run-time property, so that the image data is available to the control's client HTML and JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ データがコントロールのクライアント HTML と JavaScript で利用できるように、実行時プロパティを作成することも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Technical overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To see an example of the run-time class, in Solution Explorer, expand <bpt id="p1">**</bpt>Classes<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>View Code<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム クラスの例を表示するには、ソリューション エクスプローラーで <bpt id="p1">**</bpt>クラス<ept id="p1">**</ept> を展開し、<bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept>を右クリックして、<bpt id="p3">**</bpt>コードを表示<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The class opens in the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスがコード エディターで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source><bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> is the run-time class for the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> はコンタクト コントロールのランタイム クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The class defines the run-time behavior of the contact control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、連絡先コントロールのランタイム動作を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The run-time class typically contains X++ for data access or business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、ランタイム クラスには、データ アクセスまたはビジネス ロジック用の X++ が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In addition, there are two primary run-time behaviors that are related to extensible controls that you define in the run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、ランタイム クラスで定義した拡張可能コントロールに関連する 2 つの主なランタイム動作があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Each behavior is declaratively defined by using an attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各動作では、属性を使用して宣言的に定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><bpt id="p1">**</bpt>Run-time properties of the control<ept id="p1">**</ept> – These properties can be of two types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロールの実行時のプロパティ<ept id="p1">**</ept> – これらのプロパティには 2 つのタイプがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source><bpt id="p1">*</bpt>Static properties<ept id="p1">*</ept>, which are set via code or initialized with values from designer properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>静的プロパティ<ept id="p1">*</ept>は、コードを介して設定されるか、デザイナーのプロパティからの値で初期化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><bpt id="p1">*</bpt>Bindable properties<ept id="p1">*</ept>, for which the run-time value is determined by a binding to a data source and data field combination.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>バインド可能なプロパティ<ept id="p1">*</ept>、ランタイム値は、データ ソースおよびデータ フィールドの組み合わせへのバインディングによって決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Run-time properties are declared by using <bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> 属性を使用してランタイム プロパティが宣言されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The following example shows a property declaration in <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> のプロパティ宣言を示しています。.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x6<ept id="p1">](./media/x6.png)](./media/x6.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x6<ept id="p1">](./media/x6.png)](./media/x6.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The <bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> attribute accepts two arguments:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> 属性は、2 つの引数を受け取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>The first argument indicates to the framework the kind of JavaScript view model property to create.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の引数は、作成する JavaScript ビュー モデル プロパティの種類をフレームワークに示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>If you supply <bpt id="p1">**</bpt>BindableValue<ept id="p1">**</ept>, a <bpt id="p2">**</bpt>ReferenceProperty<ept id="p2">**</ept> is generated in the JavaScript view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BindableValue<ept id="p1">**</ept> を指定した場合、<bpt id="p2">**</bpt>ReferenceProperty<ept id="p2">**</ept> が JavaScript ビュー モデルに生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>A <bpt id="p1">**</bpt>ReferenceProperty<ept id="p1">**</ept> updates itself when data changes in the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ReferenceProperty<ept id="p1">**</ept>は、データ ソース内のデータが変更されたときに更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If you supply <bpt id="p1">**</bpt>Value<ept id="p1">**</ept>, a <bpt id="p2">**</bpt>ValueProperty<ept id="p2">**</ept> is generated in the JavaScript view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Value<ept id="p1">**</ept> を指定した場合、<bpt id="p2">**</bpt>ValueProperty<ept id="p2">**</ept> が JavaScript ビュー モデルに生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>A developer must write code to update the value of a <bpt id="p1">**</bpt>ValueProperty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、<bpt id="p1">**</bpt>ValueProperty<ept id="p1">**</ept> の値を更新するためのコードを記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The second argument of the attribute sets the name for the property as it will be defined in the JavaScript view model.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">属性の第 2 引数は、JavaScript ビュー モデルで定義されるプロパティの名前を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Don't be concerned if <bpt id="p1">**</bpt>TitleFields<ept id="p1">**</ept> don't seem to be bound to data because the example uses a <bpt id="p2">**</bpt>Value<ept id="p2">**</ept> property.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">この例では <bpt id="p2">**</bpt>値<ept id="p2">**</ept> プロパティを使用するため、<bpt id="p1">**</bpt>TitleFields<ept id="p1">**</ept> がデータにバインドされていないように見える場合にも問題はありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>The <bpt id="p1">**</bpt>TitleFields<ept id="p1">**</ept> property returns a List that contains <bpt id="p2">**</bpt>FormBindingDataFields<ept id="p2">**</ept>, each of which is data-bound.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TitleFields<ept id="p1">**</ept> プロパティは、それぞれデータ バインドされた <bpt id="p2">**</bpt>FormBindingDataFields<ept id="p2">**</ept> を含むリストを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The X++ method that has the <bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> attribute is a simple getter/setter that uses a <bpt id="p2">**</bpt>FormProperty<ept id="p2">**</ept> as the backing field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> 属性を持つ X++ メソッドは、<bpt id="p2">**</bpt>FormProperty<ept id="p2">**</ept> をバッキング フィールドとして使用する単純なゲッター/セッターです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>The <bpt id="p1">**</bpt>FormProperty<ept id="p1">**</ept> contains the logic for updating the property, based on value or data source changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormProperty<ept id="p1">**</ept> には、値またはデータ ソースの変更に基づく、プロパティを更新するためのロジックが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>It also serves as the backing field for the property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティのバッキング フィールドとしても機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Run-time commands for the control<ept id="p1">**</ept> – Commands enable the client parts of the control to trigger X++ logic, based on client-side user interactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロールの実行時コマンド<ept id="p1">**</ept> – コマンドはクライアント側のユーザーとのやり取りに基づく、トリガー X++ ロジックのクライアント部分のコントロールを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Commands are declared by using a <bpt id="p1">**</bpt>FormCommandAttribute<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドは <bpt id="p1">**</bpt>FormCommandAttribute<ept id="p1">**</ept> 属性を使用して宣言されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The single argument specifies the name of the command as it will appear in the JavaScript view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一の引数は、JavaScript ビューモデルに表示されるコマンドの名前を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The following example shows a command declaration in <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> のコマンド宣言を示しています。.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x7<ept id="p1">](./media/x7.png)](./media/x7.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x7<ept id="p1">](./media/x7.png)](./media/x7.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Tutorial steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルの手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Verify that the <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> class is open in the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターで <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> が開いていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>If it isn't, in Solution Explorer, expand <bpt id="p1">**</bpt>Classes<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>View Code<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうされていない場合は、ソリューション エクスプローラーで<bpt id="p1">**</bpt>クラス<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept> を右クリックして、<bpt id="p3">**</bpt>コードを表示<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Add a run-time property for the image data to <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> に画像データの実行時プロパティを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>In the <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> class, declare a <bpt id="p2">**</bpt>FormProperty<ept id="p2">**</ept> that is named <bpt id="p3">**</bpt>imageFieldProperty<ept id="p3">**</ept>, as shown by the highlighted line in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> クラスで、次の例で強調表示された行で示すように <bpt id="p3">**</bpt>imageFieldProperty<ept id="p3">**</ept> という <bpt id="p2">**</bpt>FormProperty<ept id="p2">**</ept> を宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x8<ept id="p1">](./media/x8.png)](./media/x8.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x8<ept id="p1">](./media/x8.png)](./media/x8.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Add the following X++ method after the <bpt id="p1">**</bpt>parmDataSource<ept id="p1">**</ept> X++ method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmDataSource<ept id="p1">**</ept> X++ メソッドの後に、次の X++ メソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The new method will serve as the getter/setter for <bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">新しいメソッドは、<bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept> のゲッター/セッターとして機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>You don't return the value of the image data here, because the framework will let you bind to the data in the client, as you will see later.</source><target logoport:matchpercent="96" state="translated" state-qualifier="fuzzy-match">後で見るように、フレームワークはクライアントのデータにバインドさせるため、ここでは画像データの値を返しません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x9<ept id="p1">](./media/x9.png)](./media/x9.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x9<ept id="p1">](./media/x9.png)](./media/x9.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Initialize <bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept> by adding the highlighted line in the following example to the new method of <bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept> は、次の例で強調表示された行を <bpt id="p2">**</bpt>FMTContactControl<ept id="p2">**</ept> の新しいメソッドに追加することで初期化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x10<ept id="p1">](./media/x10.png)](./media/x10.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x10<ept id="p1">](./media/x10.png)](./media/x10.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Now supply the binding to <bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept> by adding the highlighted line in the following example to the <bpt id="p2">**</bpt>applyBuild<ept id="p2">**</ept> method of <bpt id="p3">**</bpt>FMTContactControl<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、次の例で強調表示された行を <bpt id="p3">**</bpt>FMTContactControl<ept id="p3">**</ept> の <bpt id="p2">**</bpt>applyBuild<ept id="p2">**</ept> メソッドに追加することで <bpt id="p1">**</bpt>imageFieldProperty<ept id="p1">**</ept> へのバインディングを供給します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x11<ept id="p1">](./media/x11.png)](./media/x11.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x11<ept id="p1">](./media/x11.png)](./media/x11.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Press Ctrl+S to save the changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl + S を押して変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>You've now finished modifying the run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、実行時クラスの変更が完了しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Next, you will update the HTML view to display the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、画像を表示する HTML ビューを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Modify the HTML for the contact control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールの HTML の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>The HTML of the contact control is where you add UI elements, such as text boxes, images, and buttons, that interact with the properties and commands that are defined in the run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールの HTML では、テキスト ボックス、画像、およびボタンなど、ランタイム クラスで定義されているプロパティとコマンドを操作する UI 要素を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Extensible controls use a declarative HTML-based binding syntax to bind HTML element behaviors to properties, commands, JavaScript expressions, and JavaScript functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールでは、宣言的な HTML ベースのバインド構文を使用して、HTML 要素の動作をプロパティ、コマンド、JavaScript 式、および JavaScript 関数にバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>These bindings are parsed at run time, and the resulting HTML is injected into the DOM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのバインディングは実行時に解析され、結果の HTML が DOM に注入されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The following section explains a few of the bindings that are used in FMTContactControl.htm to add an image to the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、コントロールに画像を追加するために FMTContactControl.htm で使用されるバインディングのいくつかについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Technical overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The <bpt id="p1">**</bpt>bind<ept id="p1">**</ept> attribute, together with the <bpt id="p2">**</bpt>text<ept id="p2">**</ept> binding handler enables binding to the <bpt id="p3">**</bpt>text<ept id="p3">**</ept> property of an HTML element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>bind<ept id="p1">**</ept> 属性と <bpt id="p2">**</bpt>text<ept id="p2">**</ept> バインディング ハンドラーを組み合わせると、HTML 要素の <bpt id="p3">**</bpt>text<ept id="p3">**</ept> プロパティへのバインディングが有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>For example, the following HTML uses the <bpt id="p1">**</bpt>bind<ept id="p1">**</ept> attribute and the <bpt id="p2">**</bpt>text<ept id="p2">**</ept> binding handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の HTML は<bpt id="p1">**</bpt>バインド<ept id="p1">**</ept>属性および<bpt id="p2">**</bpt>テキスト<ept id="p2">**</ept>バインディング ハンドラーを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x12<ept id="p1">](./media/x12.png)](./media/x12.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x12<ept id="p1">](./media/x12.png)](./media/x12.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>The preceding HTML is equivalent to the following HTML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の HTML は、次の HTML と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x13<ept id="p1">](./media/x13.png)](./media/x13.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x13<ept id="p1">](./media/x13.png)](./media/x13.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>You will see the benefits of the binding when you bind to properties or commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティまたはコマンドにバインドするとき、バインドの利点が分かります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>For example, if you have a view model property that is named <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>, you can bind to it as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>名<ept id="p1">**</ept>という名前のビュー モデル プロパティある場合、次の例に示すようにそれをバインドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Here, <bpt id="p1">**</bpt>$data<ept id="p1">**</ept> is the object that contains the view model properties and commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、<bpt id="p1">**</bpt>$data<ept id="p1">**</ept> はビュー モデル プロパティおよびコマンドを含むオブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x14<ept id="p1">](./media/x14.png)](./media/x14.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x14<ept id="p1">](./media/x14.png)](./media/x14.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>The HTML output changes, based on the current value of <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML 出力は、<bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> の現在の値に基づいて変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The following example shows the output if <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> has a value of <bpt id="p2">**</bpt>John<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>名<ept id="p1">**</ept> の値が <bpt id="p2">**</bpt>John<ept id="p2">**</ept> の場合の出力を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source><bpt id="p1">[</bpt><bpt id="p2">**</bpt><ph id="ph1">![</ph>x15<ept id="p2">](./media/x15.png)**</ept><ept id="p1">](./media/x15.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><bpt id="p2">**</bpt><ph id="ph1">![</ph>x15<ept id="p2">](./media/x15.png)**</ept><ept id="p1">](./media/x15.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>If the value of the <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> property changes for some reason (for example, X++ or JavaScript was run to update the property), the binding is automatically reevaluated, and the HTML output immediately reflects the change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">何らかの理由で <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept> プロパティが変更した場合 (たとえば、X++ または JavaScript がプロパティを更新するために実行された)、バインドは自動的に再評価され、HTML 出力により変更がすぐに反映されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>All binding handlers follow this pattern of automatic reevaluation when the binding value changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインド値が変更されるとすべてのバインディング ハンドラーは自動再評価のパターンに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>The <bpt id="p1">**</bpt>if<ept id="p1">**</ept> and <bpt id="p2">**</bpt>foreach<ept id="p2">**</ept> binding handlers are unique in that they perform DOM manipulation based on the binding values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>if<ept id="p1">**</ept> および <bpt id="p2">**</bpt>foreach<ept id="p2">**</ept> バインディング ハンドラーは、バインディング値に基づいて DOM 操作を実行するという点で独自です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>To conditionally add an element to the DOM, use the <bpt id="p1">**</bpt>if<ept id="p1">**</ept> binding handler and supply the condition under which the element should be added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件付きで DOM に要素を追加するには、<bpt id="p1">**</bpt>if<ept id="p1">**</ept> バインド ハンドラを使用し、要素を追加する条件を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>If the condition is false, the element isn't added to or removed from the DOM, and no bindings that are associated with the element are evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件が false の場合は、要素を DOM に追加されたり、DOM から削除されることはなく、要素に関連付けられているバインドは評価されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Of course, if the binding value that is supplied to <bpt id="p1">**</bpt>if<ept id="p1">**</ept> changes, an element that was removed will be added to the DOM again, and the bindings will be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もちろん、<bpt id="p1">**</bpt>場合<ept id="p1">**</ept>の変更に提供される値バインディングの場合、削除された要素がもう一度 DOM に追加され、バインディングは評価されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>To iterate over an array of elements, use the <bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> binding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要素の配列を反復処理するには、<bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> バインドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>This is useful when nearly identical HTML elements must be displayed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ほぼ同一の HTML 要素を表示する必要がある場合に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>The following table shows some of the other binding handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、その他のバインディング ハンドラーの一部を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Binding handler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインディング ハンドラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>css</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">css</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Specify a CSS class, based on a condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件に基づいて、CSS クラスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>style</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">style</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Apply CSS styles, and bind the values to properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSS スタイルを適用し、値をプロパティにバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>attr</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">attr</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Bind an HTML attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML 属性をバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>In addition to using HTML elements inside the HTML for your control, you can also add framework controls such as CheckBox, Group, Tile, SectionContainer, Label, and List to your control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの HTML 内での HTML 要素の使用に加えて、CheckBox、Group、Tile、SectionContainer、Label、および List などのフレームワーク コントロールをコントロールに追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Instead of binding handlers, each framework control enables binding values to be passed to its view model properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインディング ハンドラーの代わりに、各フレームワーク コントロールでバインド値をビュー モデル プロパティに渡すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>For example, a <bpt id="p1">**</bpt>CommandButton<ept id="p1">**</ept> is added by using the <bpt id="p2">**</bpt>role<ept id="p2">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>CommandButton<ept id="p1">**</ept> は<bpt id="p2">**</bpt>ロール<ept id="p2">**</ept>属性を使用して追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x16<ept id="p1">](./media/x16.png)](./media/x16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x16<ept id="p1">](./media/x16.png)](./media/x16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>In this case, <bpt id="p1">**</bpt>ActionCommand<ept id="p1">**</ept> can be supplied with a JavaScript function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>ActionCommand<ept id="p1">**</ept> は JavaScript 機能とともに提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x17<ept id="p1">](./media/x17.png)](./media/x17.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x17<ept id="p1">](./media/x17.png)](./media/x17.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>One additional feature of the HTML binding syntax is the context-aware nature of bindings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML バインディング構文の追加機能の 1 つは、バインディングのコンテキスト認識の性質です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>By default, the context of all HTML elements is set to the JavaScript view model for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、すべての HTML 要素のコンテキストはコントロールの JavaScript ビュー モデルに設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>However, the context changes in certain circumstances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、コンテキストは特定の状況で変化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>For example, for a <bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> binding, every child element that is nested inside the hosting element (the element that has the <bpt id="p2">**</bpt>foreach<ept id="p2">**</ept> binding) obtains the current item in the loop as the context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> バインディングに対して、ホスト要素 (<bpt id="p2">**</bpt>foreach<ept id="p2">**</ept> バインディングを持つ要素) 内に入れ子になったすべての子要素は、コンテキストとしてループで現在の品目を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>To access the context of the parent element when you're inside of a <bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> binding, use the <bpt id="p2">**</bpt>$parent<ept id="p2">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> バインドの内部にあるときに親要素のコンテキストにアクセスするには、<bpt id="p2">**</bpt>$parent<ept id="p2">**</ept> オブジェクトを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>The following example from FTMContactControl.htm will help make this point clearer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FTMContactControl.htm の次の例は、この点を明確にするのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x18<ept id="p1">](./media/x18.png)](./media/x18.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x18<ept id="p1">](./media/x18.png)](./media/x18.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source><bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> is a List property that is available on the control's JavaScript view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション<ept id="p1">**</ept> コントロールの JavaScript ビュー モデルで使用可能なリスト プロパティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>This property was defined in the <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、<bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> ランタイム クラスで定義されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Each action in the <bpt id="p1">**</bpt>Actions<ept id="p1">**</ept> list has <bpt id="p2">**</bpt>Data Source<ept id="p2">**</ept>, <bpt id="p3">**</bpt>Data Field<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>Action Name<ept id="p4">**</ept> properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション<ept id="p1">**</ept>リストの各アクションには、<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept>、<bpt id="p3">**</bpt>データ フィールド<ept id="p3">**</ept>、および<bpt id="p4">**</bpt>アクション名<ept id="p4">**</ept>プロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Within the <bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> loop, <bpt id="p2">**</bpt>$data<ept id="p2">**</ept> refers to the current action, and <bpt id="p3">**</bpt>$data.ActionName<ept id="p3">**</ept> cam retrieve the <bpt id="p4">**</bpt>ActionName<ept id="p4">**</ept> property from the current action in the loop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>foreach<ept id="p1">**</ept> ループ内で、<bpt id="p2">**</bpt>$data<ept id="p2">**</ept> は現在のアクションを参照し、<bpt id="p3">**</bpt>$data.ActionName<ept id="p3">**</ept> カムはループ内の現在のアクションから <bpt id="p4">**</bpt>ActionName<ept id="p4">**</ept> プロパティを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Within the loop, view model properties on the control aren't accessible via <bpt id="p1">**</bpt>$data<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ループ内では、コントロール上のビュー モデル プロパティは <bpt id="p1">**</bpt>$data<ept id="p1">**</ept> 経由でアクセスすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Instead, <bpt id="p1">**</bpt>$parent<ept id="p1">**</ept> can be used to retrieve the view model properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>$parent<ept id="p1">**</ept> を使用してビュー モデル プロパティを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Tutorial steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルの手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Add the HTML for the <bpt id="p1">**</bpt>ImageField<ept id="p1">**</ept> property that you created in the run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム クラスで作成した <bpt id="p1">**</bpt>ImageField<ept id="p1">**</ept> プロパティの HTML を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>In Solution Explorer, expand the <bpt id="p1">**</bpt>Resources<ept id="p1">**</ept> folder under the <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> project, and double-click <bpt id="p3">**</bpt>FMTContactControlHTM<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> プロジェクトの<bpt id="p1">**</bpt>リソース<ept id="p1">**</ept> フォルダーを展開し、<bpt id="p3">**</bpt>FMTContactControlHTM<ept id="p3">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>The FMTContactControl.htm file opens in the HTML editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTContactControl.htm ファイルは、HTML エディターで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Add the following HTML to the FMTContactControl.htm HTML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTContactControl.htm HTML に、次の HTML を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The gray text is shown just for placement context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">灰色のテキストは、配置コンテキストにのみ表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x19<ept id="p1">](./media/x19.png)](./media/x19.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x19<ept id="p1">](./media/x19.png)](./media/x19.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Press Ctrl+S to save the changes to FMTContactControl.htm.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+S を押し、FMTContactControl.htm の変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>In the preceding example, you use the framework image control to render the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の例では、イメージを表示するためにフレームワーク イメージ コントロールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept> is a property that is defined on the Image control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>はイメージ コントロールで定義されているプロパティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>This property lets you specify the value for the image data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティを使用すると、画像データの値を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>The image control supports several kinds of image types, but for this example, you’re concerned with only two possible types: URLs and Base64 strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ コントロールはいくつかの種類のイメージ タイプをサポートしていますが、この例では、URL と Base64 文字列の 2 つのタイプのみを考慮しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Because the image type depends on data that is known only at run time, you will use a property that derives this information, <bpt id="p1">**</bpt>ImageValue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ タイプは実行時にのみ認識されるデータに依存するため、この情報を取得するプロパティ、<bpt id="p1">**</bpt>ImageValue<ept id="p1">**</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>You might notice that no such property is defined in the run-time class for <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのようなプロパティが <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> の実行時クラスで定義されていないことが通知される可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Therefore, this property isn't part of the automatically generated JavaScript view model for that control, and it also isn't defined on <bpt id="p1">**</bpt>$data<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このプロパティは、そのコントロールの自動生成された JavaScript ビュー モデルの一部ではなく、&lt;<bpt id="p1">**</bpt>$data<ept id="p1">**</ept> にも定義されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>To make the <bpt id="p1">**</bpt>ImageValue<ept id="p1">**</ept> property accessible via <bpt id="p2">**</bpt>$data<ept id="p2">**</ept>, you must extend the automatically generated JavaScript view model to add the property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>$data<ept id="p2">**</ept> 経由で <bpt id="p1">**</bpt>ImageValue<ept id="p1">**</ept> プロパティにアクセスできるようにするには、自動的に生成された JavaScript ビュー モデルを拡張してプロパティを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Review the JavaScript for the contact control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">連絡先コントロールの JavaScript を確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>As was mentioned earlier, for every X++ method that has either a <bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> or <bpt id="p2">**</bpt>FormCommandAttribute<ept id="p2">**</ept> attribute, a JavaScript property or command is generated and made accessible to an extensible control's HTML via the view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前述したように、<bpt id="p1">**</bpt>FormPropertyAttribute<ept id="p1">**</ept> または <bpt id="p2">**</bpt>FormCommandAttribute<ept id="p2">**</ept> 属性を持つすべての X++ メソッドに対して、JavaScript プロパティまたはコマンドが生成され、ビュー モデルを介して拡張可能コントロールの HTML にアクセスできるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>You can extend this view model with additional properties and commands that are defined only on the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント上でのみ定義される追加プロパティおよびコマンドで、このビュー モデルを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>In other words, the properties and commands have no associated X++ methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、プロパティやコマンドに関連付けられている X++ メソッドはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>After you extend the view model, the additional client-only properties and commands can be used in bindings via the <bpt id="p1">**</bpt>$data<ept id="p1">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビュー モデルを拡張した後、追加のクライアントのみ <bpt id="p1">**</bpt>$data<ept id="p1">**</ept> オブジェクト経由でバインディングのプロパティおよびコマンドを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Technical overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>The Control Extensibility Framework offers many functions that help with data bindings and data access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール拡張フレームワークには、データ バインドおよびデータ アクセスを支援する多くの機能が用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Some of the functions that are used in FMTContactControl.htm, such as <bpt id="p1">**</bpt>$field<ept id="p1">**</ept> or <bpt id="p2">**</bpt>$model<ept id="p2">**</ept>, make it easy to access the data source and its fields from the HTML bindings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTContactControl.htm で使用されるいくつかの関数 (<bpt id="p1">**</bpt>$field$<ept id="p1">**</ept> や <bpt id="p2">**</bpt>$model<ept id="p2">**</ept> など) を使うと、HTML バインドからデータ ソースとそのフィールドにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>These functions are functional aliases that are used in the HTML bindings for JavaScript functions that are defined by the framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの関数は、フレームワークによって定義された JavaScript 関数の HTML バインディングで使用される関数別名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Within the extended JavaScript view model, the equivalent, non-aliased functions are <bpt id="p1">**</bpt>$dyn.getField<ept id="p1">**</ept> and <bpt id="p2">**</bpt>$dyn.getModel<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張された JavaScript ビュー モデル内では、等価の、非エイリアス関数は <bpt id="p1">**</bpt>$dyn.getField<ept id="p1">**</ept> および <bpt id="p2">**</bpt>$dyn.getModel<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>You can also use jQuery within the extended JavaScript view model by using the <bpt id="p1">**</bpt><ph id="ph1">$</ph><ept id="p1">**</ept> symbol.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt><ph id="ph1">$</ph><ept id="p1">**</ept> シンボルを使用して、拡張 JavaScript ビュー モデル内で jQuery を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>The following example shows the standard pattern that is used to define a constructor for the extended JavaScript view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、拡張 JavaScript ビュー モデルのコンストラクターを定義するために使用される標準パターンを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>In this example, you save a reference to <bpt id="p1">**</bpt>this<ept id="p1">**</ept>, apply the base <bpt id="p2">**</bpt>Control<ept id="p2">**</ept> class behaviors, and then combine the automatically generated properties and commands with the properties and command from the extended view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>this<ept id="p1">**</ept> への参照を保存し、基本<bpt id="p2">**</bpt>コントロール<ept id="p2">**</ept> クラスの動作を適用してから、自動的に生成されたプロパティおよびコマンドと、拡張表示モデルからのプロパティおよびコマンドを結合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x20<ept id="p1">](./media/x20.png)](./media/x20.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x20<ept id="p1">](./media/x20.png)](./media/x20.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>The <bpt id="p1">**</bpt>self<ept id="p1">**</ept> variable now contains all properties and commands that are generated from the X++ run-time class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>self<ept id="p1">**</ept> 変数には、X++ ランタイム クラスから生成されたすべてのプロパティとコマンドが含まれるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>The following example shows how to add a client-only property to extend the view model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、ビュー モデルを拡張するためのクライアント専用のプロパティを追加する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>x21<ept id="p1">](./media/x21.png)](./media/x21.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>x21<ept id="p1">](./media/x21.png)](./media/x21.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>The <bpt id="p1">**</bpt>self<ept id="p1">**</ept> variable will then contain all the properties and commands that are generated from the X++ run-time class, and also the <bpt id="p2">**</bpt>ActionTypes<ept id="p2">**</ept> property that was added as a client-only property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>self<ept id="p1">**</ept> 変数に、X++ の実行時クラスから生成されたすべてのプロパティおよびコマンドと、クライアント専用プロパティとして追加された <bpt id="p2">**</bpt>ActionTypes<ept id="p2">**</ept> プロパティも含まれるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>There are many more topics that are related to building view models for controls, but they are outside the scope of this tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのビュー モデルを構築することに関連するトピックは他にもたくさんありますが、このチュートリアルの範囲外です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>For this tutorial, we don’t need to make any changes to the view model for <bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、<bpt id="p1">**</bpt>FMTContactControl<ept id="p1">**</ept> のビュー モデルに変更を加える必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Therefore, you can close the FMTContactControl.js file and proceed to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、FMTContactControl.js ファイルを閉じて次のセクションに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Add the extensible control to the Fleet Management workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理ワークスペースへの拡張可能コントロールの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>You will now update the <bpt id="p1">**</bpt>Fleet Management Clerk<ept id="p1">**</ept> workspace so that it uses the contact control that you just completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、<bpt id="p1">**</bpt>フリート管理クラーク<ept id="p1">**</ept> ワークスペースを更新します。これにより、このワークスペースで、完成したところの連絡先コントロールが使用されるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>In Solution Explorer, expand <bpt id="p1">**</bpt>Forms<ept id="p1">**</ept>, and then double-click <bpt id="p2">**</bpt>FMTPickingUpTodayPart<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>を展開してから、<bpt id="p2">**</bpt>FMTPickingUpTodayPart<ept id="p2">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>The form opens in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>In the form designer, expand <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>PickingUpTodayGrid<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>PickingUpTodayGrid<ept id="p2">**</ept> と展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>If there is an existing contact control, delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の連絡コントロールがある場合は、それを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>You must remove and then re-add the control, so that the form designer picks up the X++ changes that you made.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ に対して行われた変更をフォーム デザイナーが取得できるように、コントロールを削除して再度追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Right-click the existing control, and then click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコントロールを右クリックし、<bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Right-click <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>FMT Contact Control<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>FMT 連絡先コントロール<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Click the <bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept> node that you just added, and set the <bpt id="p2">**</bpt>Data Source<ept id="p2">**</ept> property to <bpt id="p3">**</bpt>FMTCustomer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加したばかりの <bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> プロパティを <bpt id="p3">**</bpt>FMTCustomer<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Expand the <bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept> node, click <bpt id="p2">**</bpt>Image<ept id="p2">**</ept>, and then, in the <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept> ノードを展開し、<bpt id="p2">**</bpt>画像<ept id="p2">**</ept>をクリックし、その後<bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept>ウィンドウに次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>FMTCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Create new title fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタイトル フィールドを作成する:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Right-click <bpt id="p1">**</bpt>Title Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Title Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Click the <bpt id="p1">**</bpt>Title Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>タイトル フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>FMTCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Right-click <bpt id="p1">**</bpt>Title Fields<ept id="p1">**</ept> again, and then click <bpt id="p2">**</bpt>New Title Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイトル フィールド<ept id="p1">**</ept> をもう一度右クリックし、<bpt id="p2">**</bpt>新しいタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Click the <bpt id="p1">**</bpt>Title Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>タイトル フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>FMTCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Create new subtitle fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい字幕フィールドを作成する:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Right-click <bpt id="p1">**</bpt>Subtitle Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Subtitle Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブタイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいサブタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>StartDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StartDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>FMTRental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTRental</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>StartDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StartDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>Formatting Expression</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマット式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Pickup <ph id="ph1">{0}</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">集荷 <ph id="ph1">{0}</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Right-click <bpt id="p1">*</bpt><bpt id="p2">&lt;strong&gt;</bpt><bpt id="p3">&lt;em&gt;</bpt>Subtitle Fields<ept id="p3">&lt;/em&gt;</ept><ept id="p2">&lt;/strong&gt;</ept><ept id="p1">*</ept> again, and then click <bpt id="p4">*</bpt><bpt id="p5">&lt;strong&gt;</bpt><bpt id="p6">&lt;em&gt;</bpt>New Subtitle Field<ept id="p6">&lt;/em&gt;</ept><ept id="p5">*</ept>.<ept id="p4">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt><bpt id="p2">&lt;strong&gt;</bpt><bpt id="p3">&lt;em&gt;</bpt>サブタイトル フィールド<ept id="p3">&lt;/em&gt;</ept><ept id="p2">&lt;/strong&gt;</ept><ept id="p1">*</ept> をもう一度右クリックし、<bpt id="p4">*</bpt><bpt id="p5">&lt;strong&gt;</bpt><bpt id="p6">&lt;em&gt;</bpt>新しいサブタイトル フィールド<ept id="p6">&lt;/em&gt;</ept><ept id="p5">*</ept><ept id="p4">&lt;/strong&gt;</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>EndDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EndDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>FMTRental</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTRental</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>EndDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EndDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Formatting Expression</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマット式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Return <ph id="ph1">{0}</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品<ph id="ph1">{0}</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Right-click <bpt id="p1">**</bpt>Subtitle Fields<ept id="p1">**</ept> again, and then click <bpt id="p2">**</bpt>New Subtitle Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブタイトル フィールド<ept id="p1">**</ept> をもう一度右クリックし、<bpt id="p2">**</bpt>新しいサブタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>VehicleDescription</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VehicleDescription</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>FMTVehicle</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTVehicle</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Press Ctrl+S to save your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl + S を押して変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Copy <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> by right-clicking in the grid and clicking <bpt id="p2">**</bpt>Copy<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドを右クリックし、<bpt id="p2">**</bpt>コピー<ept id="p2">**</ept>をクリックして <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>In Solution Explorer, click <bpt id="p1">**</bpt>Forms<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FMTReturningTodayPart<ept id="p2">**</ept>, and then double-click <bpt id="p3">**</bpt>FMTReturningTodayPart<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FMTReturningTodayPart<ept id="p2">**</ept> をクリックしてから、<bpt id="p3">**</bpt>FMTReturningTodayPart<ept id="p3">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>The form opens in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>Expand <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>ReturningTodayGrid<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Delete<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>ReturningTodayGrid<ept id="p2">**</ept> を右クリックし、その後<bpt id="p3">**</bpt>削除<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Right-click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Paste<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>貼り付け<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Select the <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> grid that you just added to the <bpt id="p2">**</bpt>FMTReturningTodayPart<ept id="p2">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>FMTReturningTodayPart<ept id="p2">**</ept> フォームに追加したばかりの <bpt id="p1">**</bpt>PickingUpTodayGrid<ept id="p1">**</ept> グリッドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Set the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>ReturningTodayGrid<ept id="p2">**</ept>, and then press Ctrl+S to save the changes to the <bpt id="p3">**</bpt>EMTReturningTodayPart<ept id="p3">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>ReturningTodayGrid<ept id="p2">**</ept> に設定し、Ctrl+S を押して変更を <bpt id="p3">**</bpt>EMTReturningTodayPart<ept id="p3">**</ept> フォームに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>In Solution Explorer, find the <bpt id="p1">**</bpt>FMTRentalRatesPart<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMTRentalRatesPart<ept id="p1">**</ept> フォームを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Double-click the form to open it in the form designer, and then click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>RentalRatesGrid<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームをダブルクリックして、フォームデザイナーで開き、<bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>RentalRatesGrid<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Delete each field from <bpt id="p1">**</bpt>RentalRatesGrid<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RentalRatesGrid<ept id="p1">**</ept> から各フィールドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>To remove the fields, click the first field, hold down the Shift key while you click the last field, and then press Delete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを削除するには、最初のフィールドをクリックし、Shift キーを押しながら最後のフィールドをクリックし、Del キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Right-click in the grid, point to <bpt id="p1">**</bpt>New<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>FMT Contact Control<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド内を右クリックして <bpt id="p1">**</bpt>新規<ept id="p1">**</ept> をポイントし、<bpt id="p2">**</bpt>FMT 連絡先コントロール<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>Expand <bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Image<ept id="p2">**</ept>, and then, in the <bpt id="p3">**</bpt>Properties<ept id="p3">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTContactControl1<ept id="p1">**</ept> を展開し、<bpt id="p2">**</bpt>画像<ept id="p2">**</ept>をクリックし、その後<bpt id="p3">**</bpt>プロパティ<ept id="p3">**</ept>ウィンドウに次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>FMTVehicleModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTVehicleModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>Image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Right-click <bpt id="p1">**</bpt>Title Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Title Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Click the title field node that you just created, and then, in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりのタイトル フィールド ノードをクリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>VehicleModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VehicleModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>FMTVehicleModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTVehicleModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>Model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>Right-click <bpt id="p1">**</bpt>Subtitle Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Subtitle Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブタイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいサブタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>VehicleMake</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VehicleMake</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>FMTVehicleMake</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTVehicleMake</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>Make</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製造業者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>Right-click <bpt id="p1">**</bpt>Subtitle Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Subtitle Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブタイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいサブタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>RatePerDay</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RatePerDay</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>FMTModelRate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTModelRate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>RaterPerDay</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">RaterPerDay</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note:<ept id="p1">&lt;/strong&gt;</ept> The <bpt id="p2">&lt;strong&gt;</bpt>Data Field<ept id="p2">&lt;/strong&gt;</ept> value must match the table field name.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;strong&gt;</bpt>注:<ept id="p1">&lt;/strong&gt;</ept> <bpt id="p2">&lt;strong&gt;</bpt>データ フィールド<ept id="p2">&lt;/strong&gt;</ept> 値はテーブル フィールド名と一致する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>If you correct the spelling error, the values won't match, and you will receive a run-time error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スペル エラーを修正すると、値が一致しない場合は、ランタイム エラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>Formatting Expression</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマット式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>$<ph id="ph1">{0}</ph> per day</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 日当たりの $<ph id="ph1">{0}</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Right-click <bpt id="p1">**</bpt>Subtitle Fields<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>New Subtitle Field<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブタイトル フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新しいサブタイトル フィールド<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Click the <bpt id="p1">**</bpt>Subtitle Field<ept id="p1">**</ept> node that you just created, and then, in the <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept> pane, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成したばかりの<bpt id="p1">**</bpt>字幕フィールド<ept id="p1">**</ept> ノードをクリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> ウィンドウで次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Property</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>RatePerWeek</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RatePerWeek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>FMTModelRate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTModelRate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>Data Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>RatePerWeek</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RatePerWeek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>Formatting Expression</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーマット式</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>$<ph id="ph1">{0}</ph> per week</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">週ごとの $<ph id="ph1">{0}</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Press Ctrl+S to save your changes to <bpt id="p1">**</bpt>FMTRentalRatesPart<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl+S を押し、変更を <bpt id="p1">**</bpt>FMTRentalRatesPart<ept id="p1">**</ept> に保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>In Solution Explorer, right-click the <bpt id="p1">**</bpt>FMTClerkWorkspace<ept id="p1">**</ept> form, and then click <bpt id="p2">**</bpt>Set as Startup Object<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FMTClerkWorkspace<ept id="p1">**</ept> フォームを右クリックしてから、<bpt id="p2">**</bpt>スタートアップ オブジェクトとして設定<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Press Ctrl+F5 to open the updated contact control in Internet Explorer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ctrl+F5 キーを押し、Internet Explorer で更新された連絡先コントロールを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>If you receive a JavaScript error, you might have to clear the Internet Explorer cache, so that the browser loads the new JavaScript file:</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">JavaScript エラーが発生した場合は、ブラウザーが新しい JavaScript ファイルを読み込むように Internet Explorer のキャッシュをクリアする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>When you're prompted to open the debugger, click <bpt id="p1">**</bpt>No<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガーを開くように求めるメッセージが表示されたら、<bpt id="p1">**</bpt>いいえ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>While Internet Explorer is open, press F12 (or click <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>F12 Developer Tools<ept id="p2">**</ept>), and then press Ctrl+R.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer が開いているときに、F12 キーを押し (または <bpt id="p1">**</bpt>設定<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>F12 開発者ツール<ept id="p2">**</ept> をクリックし)、Ctrl+R を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>In the <bpt id="p1">**</bpt>Clear Browser Cache<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブラウザー キャッシュのクリア<ept id="p1">**</ept> ダイアログ ボックスで、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Reload the page by pressing Ctrl+F5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ctrl + F5 キーを押して、ページを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext6<ept id="p1">](./media/ext6-1024x428.png)](./media/ext6.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Ext6<ept id="p1">](./media/ext6-1024x428.png)](./media/ext6.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>In this tutorial, you've seen how you can use X++ when you define the design-time and server-side behaviors for a control, and how you can consume a powerful HTML-based and JavaScript-based framework when you design the UI and user interaction patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、コントロールのデザイン時とサーバー側の動作を定義するときに X++ を使用する方法、および UI およびユーザー操作パターンをデザインするときに HTML および JavaScript ベースの強力なフレームワークを使用する方法について説明しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>The Control Extensibility Framework helps provide a separation between the modeled behavior of a control and its physical manifestation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール拡張フレームワークは、コントロールのモデル化された動作とその物理的なマニフェストの区切りを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>As a best practice, you should try to maintain this loose coupling between data, metadata, and UI when you build extensible controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスは、拡張可能コントロールを作成するときにデータ、メタデータ、および UI の間の疎結合を管理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Bidirectional or right-to-left support</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">双方向または右から左へのサポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>To validate right-to-left (RTL) support for your extensible control, you simply need to set the <bpt id="p1">**</bpt>dir<ept id="p1">**</ept> (direction) attribute on the HTML document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コントロールの右から左 (RTL) サポートを検証するには、HTML ドキュメントの<bpt id="p1">**</bpt>dir<ept id="p1">**</ept> (方向) 属性を設定するだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>When this attribute is changed, the browser will automatically change the layout direction of your control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この属性が変更されると、ブラウザーは、コントロールのレイアウトの方向を自動的に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>You should make sure that your control doesn’t implement any styling which interferes with this layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレイアウトと競合するすべてのスタイルがコントロールで実装されていないことを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Instead of setting this attribute manually, you can also validate by placing your control on a form, and then selecting a RTL language.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この属性を手動で設定するのではなく、フォームにコントロールを配置して、右から左へ読み書きする言語を選択することでも検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Selecting a RTL language will cause the client to also update the <bpt id="p1">**</bpt>dir<ept id="p1">**</ept> attribute appropriately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RTL 言語を選択すると、クライアントは <bpt id="p1">**</bpt>dir<ept id="p1">**</ept> 属性も適切に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>For more information, see <bpt id="p1">[</bpt>dir attribute<ept id="p1">](https://www.w3.org/TR/html5/dom.html#the-dir-attribute)</ept> in the HTML standards.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、HTML 標準で <bpt id="p1">[</bpt>ディレクトリ属性<ept id="p1">](https://www.w3.org/TR/html5/dom.html#the-dir-attribute)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>