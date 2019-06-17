<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="build-customer-form.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>build-customer-form.9b20ff.a0b71da3ba67604138cdef3ab2dc3abcf96a7647.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a0b71da3ba67604138cdef3ab2dc3abcf96a7647</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\build-customer-form.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build the Customer form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客フォームの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this lab you’ll create a Master Details form and apply the appropriate form pattern and subpatterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このラボでは、マスター詳細フォームを作成し、適切なフォームのパターンおよびサブパターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>A Master Details form shows primary data that has many fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター詳細フォームには、多数のフィールドが含まれるプライマリ データが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104" restype="x-metadata">
          <source>For example, the form that you create will show customer information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、作成するフォームは、顧客情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Build the Customer form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客フォームの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In this lab you’ll create a Master Details form and apply the appropriate form pattern and subpatterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このラボでは、マスター詳細フォームを作成し、適切なフォームのパターンおよびサブパターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>A Master Details form shows primary data that has many fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター詳細フォームには、多数のフィールドが含まれるプライマリ データが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, the form that you create will show customer information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、作成するフォームは、顧客情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For this tutorial, you will need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see <bpt id="p1">[</bpt>Access Instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To create the form, you’ll start from the existing form, <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームを作成するには、既存のフォーム <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> から開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The form represents the old Master Details template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームは、古いマスター詳細テンプレートをテーブルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>As a part of the tutorial, you’ll apply the Master Details pattern, which will enforce a consistent structure for this form type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルの一環として、このフォーム タイプに一貫した構造を実行するマスターの詳細パターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The following illustration shows the <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> starting artifact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> 開始コンポーネントを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm1<ept id="p1">](./media/custform1.png)](./media/custform1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm1<ept id="p1">](./media/custform1.png)](./media/custform1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Create a Master Details form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター詳細フォームを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Apply a form pattern to a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームにフォーム パターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Use the Visual Studio pattern add-ins to get information about form/model pattern coverage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio のパターン アドインを使用して、フォーム/モデル パターンのカバレッジに関する情報を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Apply subpatterns to form controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム コントロールにサブパターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>View the form using Visual Studio and a browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio とブラウザーを使用してフォームを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Determine the amount of remaining patterns work in a model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル内で残っているパターンの作業の量を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Import the tutorial project and transactional data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトおよびトランザクション データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Use Visual Studio to import the tutorial project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The tutorial project includes the artifacts you will use to complete this tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>You will use the FMTDataHelper class to load data for the Fleet Management tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアルのデータを読み込むために、FMTDataHelper クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>If this is the first tutorial you are working on, review <bpt id="p1">[</bpt>Access Instances<ept id="p1">](../dev-tools/access-instances.md)</ept> and make sure you provision your administrator user if you’re working on a local VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが作業する最初のチュートリアルである場合は、<bpt id="p1">[</bpt>アクセス インスタンス<ept id="p1">](../dev-tools/access-instances.md)</ept>を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Download the Fleet Management sample from <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph>, save it to <bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept>, and unzip it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理のサンプルを <ph id="ph1">&lt;https://github.com/Microsoft/FMLab&gt;</ph> からダウンロードし、<bpt id="p1">**</bpt>C:<ph id="ph2">\\</ph><ept id="p1">**</ept> に保存してから解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the desktop, double-click the Visual Studio shortcut to open the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>On the <bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Import Project<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>プロジェクトのインポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In the <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> window, next to the <bpt id="p2">**</bpt>Filename<ept id="p2">**</ept> text box, click the ellipsis button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトのインポート<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>ファイル名<ept id="p2">**</ept>テキスト ボックスの隣にある、省略記号ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the <bpt id="p1">**</bpt>Select the file to import<ept id="p1">**</ept> window, browse to <bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept>, click FMTutorialDataModel.axpp, and then click <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インポートするファイルの選択<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept> を参照して FMTutorialDataModel.axpp をクリックしてから<bpt id="p3">**</bpt>開く<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In the <bpt id="p1">**</bpt>Project file location<ept id="p1">**</ept> text box, enter <bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト ファイルの場所<ept id="p1">**</ept>テキスト ボックスに、<bpt id="p2">**</bpt>C:\FMLab<ept id="p2">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Select the <bpt id="p1">**</bpt>Overwrite Elements<ept id="p1">**</ept> option and the <bpt id="p2">**</bpt>Current solution<ept id="p2">**</ept> radio button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要素の上書き<ept id="p1">**</ept> オプションをオンにし、<bpt id="p2">**</bpt>現在のソリューション<ept id="p2">**</ept> ラジオ オプションをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The following illustration shows the completed <bpt id="p1">**</bpt>Import Project<ept id="p1">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、完了した <bpt id="p1">**</bpt>インポート プロジェクト<ept id="p1">**</ept> ダイアログ ボックスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>CustForm2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustForm2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, expand <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept>, and under the <bpt id="p3">**</bpt>FMTutorial<ept id="p3">**</ept> project, right-click <bpt id="p4">**</bpt>FMTDataHelper<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>Set as Startup Object<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>クラス<ept id="p2">**</ept>を展開して、<bpt id="p3">**</bpt>FMTutorial<ept id="p3">**</ept> プロジェクトで <bpt id="p4">**</bpt>FMTDataHelper<ept id="p4">**</ept> を右クリックしてから、<bpt id="p5">**</bpt>スタートアップ オブジェクトとして設定<ept id="p5">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>On the <bpt id="p1">**</bpt>Build<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Rebuild Solution<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>ソリューションの再構築<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You use the rebuild to make sure all files in the project are built regardless of timestamps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can view the build progress in the Output window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出力ウィンドウでビルドの進行状況を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>After the build completes, press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドが完了すると、<bpt id="p1">**</bpt>Ctrl + F5<ept id="p1">**</ept> を押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The browser will open and run the class that imports the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーが開き、データをインポートするクラスが実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Open the FMTutorial project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTutorial プロジェクトを開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Use Visual Studio to open the FMTutorial project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用して FMTutorial プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the development environment is not already open, on the Desktop, double-click the Visual Studio shortcut to open the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境がまだ開いていない場合は、デスクトップで開発環境への Visual Studio ショートカットをダブルクリックして開発環境を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In the <bpt id="p1">**</bpt>Open Project<ept id="p1">**</ept> dialog box, browse to C:\FmLab\FMTutorial, select the <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> solution, and then click <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクトを開く<ept id="p1">**</ept>ダイアログ ボックスで、C:\FmLab\FMTutorial を参照し、<bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> ソリューションを選択してから<bpt id="p3">**</bpt>開く<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The FMTutorial project appears in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTutorial プロジェクトが<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Use a template to create the form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを使用してフォームを作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Use Visual Studio to create the <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用して <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> フォームを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You’ll use a template to create a new master details form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートを使用して、新しいマスターの詳細フォームを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The data source for this tutorial is provided by the starter form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルのデータ ソースは、スターター形式によって提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>However, you’ll add fields to the grid and details view and apply the Master Details form pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、グリッドと詳細ビューにフィールドを追加し、マスター詳細フォーム パターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click the <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> project, point to <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Existing Item<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> プロジェクトを右クリックして<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をポイントしてから<bpt id="p4">**</bpt>既存の項目<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the <bpt id="p1">**</bpt>Add Existing Item<ept id="p1">**</ept> window, browse to C:\FmLab, select <bpt id="p2">**</bpt>AxForm<ph id="ph1">\_</ph>FmtCustomer<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既存の品目を追加<ept id="p1">**</ept>ウィンドウで、C:\FmLab を参照し、<bpt id="p2">**</bpt>AxForm<ph id="ph1">\_</ph>FmtCustomer<ept id="p2">**</ept> を選択してから<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> form appears at the bottom of the <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> project in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーの <bpt id="p2">**</bpt>FMTutorial<ept id="p2">**</ept> プロジェクトの下に <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> フォームが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In Solution Explorer, double-click <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、<bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The form opens in the form designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In the Form designer, click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, specify the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、次の値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>FmtCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FmtCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Caption</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Customers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In the Form designer, click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageGrid<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>MainGrid<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>MainGrid<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイナーで、<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageGrid<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>MainGrid<ept id="p4">**</ept> とクリックしてから <bpt id="p5">**</bpt>MainGrid<ept id="p5">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, click <bpt id="p2">**</bpt>Data Source<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>FmtCustomer<ept id="p3">**</ept> to bind the <bpt id="p4">**</bpt>FmtCustomer<ept id="p4">**</ept> table to the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept>をクリックしてから <bpt id="p3">**</bpt>FmtCustomer<ept id="p3">**</ept> を選択して <bpt id="p4">**</bpt>FmtCustomer<ept id="p4">**</ept> テーブルをグリッドにバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>You can now use the fields from the data source to add columns to the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースからのフィールドを使用して、グリッドに列を追加できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Click <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fields<ept id="p3">**</ept> to add fields to the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>フィールド<ept id="p3">**</ept>とクリックし、グリッドにフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Click <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>, press and hold the <bpt id="p2">**</bpt>Ctrl<ept id="p2">**</ept> key, and then select the following additional fields in the order shown:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>Ctrl<ept id="p2">**</ept>キーを押しながら、表示された順序で次の追加フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>CellPhone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CellPhone</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>DriverLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DriverLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Drag the highlighted fields to <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageGrid<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>MainGrid<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">協調表示されたフィールドを <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageGrid<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>MainGrid<ept id="p4">**</ept> にドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The following illustration shows the grid after expanding the grid node and adding the fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、グリッド ノードを展開してフィールドを追加した後のグリッドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>CustForm3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustForm3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageDetails<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>TitleGroup<ept id="p4">**</ept> to add the record header to the details view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageDetails<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>TitleGroup<ept id="p4">**</ept> の順にクリックし、レコード ヘッダーを詳細ビューに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Click <bpt id="p1">**</bpt>HeaderTitle<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HeaderTitle<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, specify the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、次の値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Data Source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>FmtCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FmtCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Data Method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>titleFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">titleFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageDetails<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>DetailsBodyTab<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>General<ept id="p5">**</ept> to add content to the details view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビューにコンテンツを追加するには、<bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>TabPageDetails<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>DetailsBodyTab<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>一般<ept id="p5">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Click <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>FmtCustomer<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Fields<ept id="p4">**</ept>, press and hold the Ctrl key, and then select the following fields:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>FmtCustomer<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>フィールド<ept id="p4">**</ept>とクリックし、Ctrl キーを押したまま、次のフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>CellPhone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CellPhone</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>DriverLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DriverLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Drag the highlighted fields onto <bpt id="p1">**</bpt>General<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">協調表示されたフィールドを<bpt id="p1">**</bpt>一般<ept id="p1">**</ept>にドラッグし、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>View the form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Run the form to verify that it loads correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しく読み込まれることを確認するためにフォームを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Set as Startup Object<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept> を右クリックしてから、<bpt id="p3">**</bpt>スタートアップ オブジェクトとして設定<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The grid view should render like the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド ビューは、次の図のように表示する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm4<ept id="p1">](./media/custform4-1024x567.png)](./media/custform4.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm4<ept id="p1">](./media/custform4-1024x567.png)](./media/custform4.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>On the application bar, click <bpt id="p1">**</bpt>Open in Microsoft Office<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Export to Excel <ph id="ph2">&amp;gt;</ph> Customers<ept id="p2">**</ept> to send the information in the grid view to a Microsoft Excel spreadsheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション バーで、<bpt id="p1">**</bpt>Microsoft Office を開く<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Excel にエクスポート <ph id="ph2">&amp;gt;</ph> 顧客<ept id="p2">**</ept> をクリックして、グリッド ビューの情報を Microsoft Excel スプレッドシートに送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>(If a dialog appears asking if you’re sure you want to leave the page, click “Leave this page”.) When asked, click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept> to view the data in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ページを終了するかどうかを確認するダイアログが表示されたら、「このページを終了」をクリックします。) 求められたら、<bpt id="p1">**</bpt>開く<ept id="p1">**</ept>をクリックして Excel でデータを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Close Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel を閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Click <bpt id="p1">**</bpt>Tony<ept id="p1">**</ept> to navigate to the details view for that record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Tony<ept id="p1">**</ept> をクリックしてそのレコードの詳細ビューに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm5<ept id="p1">](./media/custform5-1024x567.png)](./media/custform5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm5<ept id="p1">](./media/custform5-1024x567.png)](./media/custform5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept>  (or the browser Back button) to go back to the grid view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>またはブラウザーの 戻る ボタンをクリックすると、グリッド ビューに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Apply a pattern to the form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームにパターンを適用します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Use Visual Studio to apply the Master Details form pattern to the <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を使用して <bpt id="p1">**</bpt>顧客<ept id="p1">**</ept> フォームに Master Details のフォーム パターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Applying a form pattern ensures your form has the expected structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム パターンを適用すると、フォームに期待される構造が確実に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>It also simplifies the design experience by automatically setting the values of properties in the nodes that are part of the pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、パターンの一部であるノードでプロパティの値を自動的に設定することでデザイン体験を簡素化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Right-click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Apply pattern,<ept id="p2">**</ept> and then click <bpt id="p3">**</bpt>Details Master<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>パターンの適用<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>詳細マスター<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm6<ept id="p1">](./media/custform6.png)](./media/custform6.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm6<ept id="p1">](./media/custform6.png)](./media/custform6.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm7<ept id="p1">](./media/custform7.png)](./media/custform7.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm7<ept id="p1">](./media/custform7.png)](./media/custform7.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Add the missing Navigation List group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">欠落しているナビゲーション リスト グループを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The red highlighting in the Patterns Information Panel indicates that this control is missing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターン情報パネルが赤色でハイライトされると、このコントロールがないことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Right-click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Group<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をクリックし、<bpt id="p3">**</bpt>グループ<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> property, enter <bpt id="p3">**</bpt>SidePanel<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウの<bpt id="p2">**</bpt>名前<ept id="p2">**</ept>プロパティに、<bpt id="p3">**</bpt>SidePanel<ept id="p3">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Click <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept>, and press <bpt id="p2">**</bpt>Alt+Up<ept id="p2">**</ept> to move this group above the <bpt id="p3">**</bpt>GridDetailsTab (Tab)<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>Alt + ↑<ept id="p2">**</ept>を押してこのグループを <bpt id="p3">**</bpt>GridDetailsTab (タブ)<ept id="p3">**</ept> の上の移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept>を再度クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The yellow highlighting around the <bpt id="p1">**</bpt>Navigation List<ept id="p1">**</ept> and the <bpt id="p2">**</bpt>Panel Tab<ept id="p2">**</ept> indicate that there are problems that need to be resolved under each of these nodes before the pattern can be successfully applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ナビゲーション リスト<ept id="p1">**</ept>と<bpt id="p2">**</bpt>パネル タブ<ept id="p2">**</ept>の周りの黄色のハイライトは、パターンが正常に適用される前にこれらの各ノードの下で解決する必要のある問題があることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm8<ept id="p1">](./media/custform8.png)](./media/custform8.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm8<ept id="p1">](./media/custform8.png)](./media/custform8.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm9<ept id="p1">](./media/custform9.png)](./media/custform9.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm9<ept id="p1">](./media/custform9.png)](./media/custform9.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In the Patterns Information Panel, click <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターン情報パネルで <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm10<ept id="p1">](./media/custform10.png)](./media/custform10.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm10<ept id="p1">](./media/custform10.png)](./media/custform10.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm11<ept id="p1">](./media/custform11.png)](./media/custform11.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm11<ept id="p1">](./media/custform11.png)](./media/custform11.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Add the missing controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">欠落しているコントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Right-click <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>QuickFilter<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をクリックし、<bpt id="p3">**</bpt>QuickFilter<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, specify the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、次の値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>SidePanelQuickFilter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SidePanelQuickFilter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Target Control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>MainGrid <bpt id="p1">*</bpt>This QuickFilter should have the same columns available for filtering as the main grid on the form<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MainGrid <bpt id="p1">*</bpt>この QuickFilter には、フォーム上の主要なグリッドと同じフィルター処理に使用できる列が必要です<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Right-click <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Grid.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をクリックし、<bpt id="p3">**</bpt>グリッド<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>NavigationList</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NavigationList</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Datasource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>FmtCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FmtCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Add identifying fields to the Navigation list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション リストに識別するフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Right-click <bpt id="p1">**</bpt>NavigationList<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>String<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NavigationList<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>文字列<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, specify the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、次の値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>DataSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataSource</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>FmtCustomer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FmtCustomer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>DataMethod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataMethod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>fullName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">fullName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>FmtCustomer<ph id="ph1">\_</ph>FullName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FmtCustomer<ph id="ph1">\_</ph>FullName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Expand <bpt id="p1">**</bpt>Data Sources<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Fields<ept id="p3">**</ept> to add phone numbers to the Simple list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電話番号を簡易リストに追加するには、<bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>FmtCustomer<ept id="p2">**</ept><ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>フィールド<ept id="p3">**</ept>を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Drag the <bpt id="p1">**</bpt>CellPhone<ept id="p1">**</ept> field onto the grid under <bpt id="p2">**</bpt>Design <ph id="ph1">&amp;gt;</ph> SidePanel <ph id="ph2">&amp;gt;</ph> NavigationList<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CellPhone<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>Design <ph id="ph1">&amp;gt;</ph> SidePanel <ph id="ph2">&amp;gt;</ph> NavigationList<ept id="p2">**</ept> の下のグリッドにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Click <bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SidePanel<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Notice the <bpt id="p1">**</bpt>Patterns Information Panel<ept id="p1">**</ept> is now indicating that the controls in this subtree are in full compliance with the pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パターン情報パネル<ept id="p1">**</ept>は、このサブツリーのコントロールがパターンに完全に準拠していることを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>CustForm12</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustForm12</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>CustForm13</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustForm13</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Click <bpt id="p1">**</bpt>Design<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイン<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>GridDetailsTab<ept id="p2">**</ept> とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>The yellow highlighting around the subnodes indicates that there are problems that need to be resolved under both nodes before the form pattern can be successfully applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブノードの周りの黄色のハイライトは、フォーム パターンが正常に適用される前に両方のノードの下で解決する必要のある問題があることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm14<ept id="p1">](./media/custform14.png)](./media/custform14.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm14<ept id="p1">](./media/custform14.png)](./media/custform14.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm15<ept id="p1">](./media/custform15.png)](./media/custform15.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm15<ept id="p1">](./media/custform15.png)](./media/custform15.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Notice that the pattern expects the <bpt id="p1">**</bpt>Grid Panel<ept id="p1">**</ept> to be after the <bpt id="p2">**</bpt>Details Panel.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターンは<bpt id="p1">**</bpt>グリッド パネル<ept id="p1">**</ept>が<bpt id="p2">**</bpt>詳細パネル<ept id="p2">**</ept>の後に配置されることを期待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Click <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> and press <bpt id="p2">**</bpt>Alt+Down<ept id="p2">**</ept> to move that tab below the <bpt id="p3">**</bpt>Details Panel<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>Alt + ↓<ept id="p2">**</ept>キーを押してそのタブを<bpt id="p3">**</bpt>詳細パネル<ept id="p3">**</ept>の下に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Click <bpt id="p1">**</bpt>GridDetailsTab<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GridDetailsTab<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The <bpt id="p1">**</bpt>TabPageDetails<ept id="p1">**</ept> tab page now adheres to the pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TabPageDetails<ept id="p1">**</ept> タブ ページはパターンに準拠するようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>However, the <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> tab page needs additional attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> タブ ページには更なる注意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm16<ept id="p1">](./media/custform16.png)](./media/custform16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm16<ept id="p1">](./media/custform16.png)](./media/custform16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm17<ept id="p1">](./media/custform17.png)](./media/custform17.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm17<ept id="p1">](./media/custform17.png)](./media/custform17.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Click <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Focus in the designer is now on <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept>, and the <bpt id="p2">**</bpt>Patterns Information Panel<ept id="p2">**</ept> has been updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーでフォーカスがすぐに <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> がオンになり、<bpt id="p2">**</bpt>パターン情報パネル<ept id="p2">**</ept>が更新されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm18<ept id="p1">](./media/custform18.png)](./media/custform18.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm18<ept id="p1">](./media/custform18.png)](./media/custform18.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm19<ept id="p1">](./media/custform19.png)](./media/custform19.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm19<ept id="p1">](./media/custform19.png)](./media/custform19.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>The <bpt id="p1">**</bpt>Patterns Information Panel<ept id="p1">**</ept> now indicates a missing Group control at the top of the <bpt id="p2">**</bpt>TabPageGrid<ept id="p2">**</ept> container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パターン情報パネル<ept id="p1">**</ept> には、<bpt id="p2">**</bpt>TabPageGrid<ept id="p2">**</ept> コンテナーの上部で欠落しているグループ コントロールが表示されるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Right-click <bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Group<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TabPageGrid<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>グループ<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Press <bpt id="p1">**</bpt>Alt+Up<ept id="p1">**</ept> two times to position the group as the first control in the group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Alt+上方向<ept id="p1">**</ept>キーを 2 回押して、そのグループをグループの最初のコントロールとして配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> property, enter <bpt id="p3">**</bpt>GridCustomFilterGroup<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウの<bpt id="p2">**</bpt>名前<ept id="p2">**</ept>プロパティに、<bpt id="p3">**</bpt>GridCustomFilterGroup<ept id="p3">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm20<ept id="p1">](./media/custform20.png)](./media/custform20.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm20<ept id="p1">](./media/custform20.png)](./media/custform20.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>The pattern is looking for a subpattern to be applied to <bpt id="p1">**</bpt>GridCustomFilterGroup<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターンが、<bpt id="p1">**</bpt>GridCustomFilterGroup<ept id="p1">**</ept> に適用されるサブパターンをお探しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Right-click <bpt id="p1">**</bpt>GridCustomFilterGroup,<ept id="p1">**</ept> point to <bpt id="p2">**</bpt>Apply pattern<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Custom and Quick Filters<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GridCustomFilterGroup<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>パターンの適用<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>カスタムおよびクイック フィルター<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm21<ept id="p1">](./media/custform21.png)](./media/custform21.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm21<ept id="p1">](./media/custform21.png)](./media/custform21.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm22<ept id="p1">](./media/custform22.png)](./media/custform22.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm22<ept id="p1">](./media/custform22.png)](./media/custform22.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>The <bpt id="p1">**</bpt>Custom and Quick Filters<ept id="p1">**</ept> subpattern requires a QuickFilter control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カスタムおよびクイック フィルター<ept id="p1">**</ept> サブパターンには、QuickFilter コントロールが必須です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Right-click <bpt id="p1">**</bpt>GridCustomFilterGroup<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>QuickFilter<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GridCustomFilterGroup<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をクリックし、<bpt id="p3">**</bpt>QuickFilter<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, specify the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、次の値を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">氏名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>MainGridQuickFilter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MainGridQuickFilter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Target Control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>MainGrid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MainGrid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Browse up the control tree to design and notice how the <bpt id="p1">**</bpt>Patterns Information Panel<ept id="p1">**</ept> now shows no issues under each of the controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール ツリーを参照して設計し、各コントロールで<bpt id="p1">**</bpt>パターン情報パネル<ept id="p1">**</ept>に問題が表示されなくなった方法に注意てください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> to save the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押してフォームを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>View the details form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細フォームの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the form to see the Details view and the Grid view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ビューとグリッド ビューに表示するフォームを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>The following illustration shows how the grid view appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、グリッド ビューの表示方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm23<ept id="p1">](./media/custform23-1024x599.png)](./media/custform23.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm23<ept id="p1">](./media/custform23-1024x599.png)](./media/custform23.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Click <bpt id="p1">**</bpt>Phil<ept id="p1">**</ept> to go to the details view for that record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Phil<ept id="p1">**</ept> をクリックしてそのレコードの詳細ビューに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm24<ept id="p1">](./media/custform24-1024x599.png)](./media/custform24.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm24<ept id="p1">](./media/custform24-1024x599.png)](./media/custform24.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Click the <bpt id="p1">**</bpt>Show list<ept id="p1">**</ept> button on the left side of the form to open the navigation list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション リストを開くには、フォームの左側にある<bpt id="p1">**</bpt>リストを表示<ept id="p1">**</ept>ボタンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm25<ept id="p1">](./media/custform25-1024x597.png)](./media/custform25.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm25<ept id="p1">](./media/custform25-1024x597.png)](./media/custform25.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>To go back to the grid view, click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> (or the browser Back button).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド表示に戻るには、<bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept> (またはブラウザーの [戻る] ボタン) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Return to Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Add subpatterns</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブパターンの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>In Visual Studio, in the Form designer, right-click <bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Addins<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Form statistics<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の、フォーム デザイナーで、<bpt id="p1">**</bpt>FmtCustomer<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept> をポイントしてから、<bpt id="p3">**</bpt>フォーム統計情報<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm26<ept id="p1">](./media/custform26.png)](./media/custform26.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm26<ept id="p1">](./media/custform26.png)](./media/custform26.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>The <bpt id="p1">**</bpt>Form Statistics<ept id="p1">**</ept> add-in provides several useful data points about the state of the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フォーム統計<ept id="p1">**</ept> アドインは、フォームの状態に関するいくつかの役に立つデータ ポイントを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>This includes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、次のものが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><bpt id="p1">**</bpt>Pattern=Unspecified count<ept id="p1">**</ept> – The number of nodes for which no form pattern or subpattern has been applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パターン = 未指定のカウント<ept id="p1">**</ept> – フォーム パターンまたはサブパターンが適用されていないノードの数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source><bpt id="p1">**</bpt>Pattern=Custom count<ept id="p1">**</ept> – The number of nodes for which a custom pattern was applied, meaning the structure did not fit with any existing pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パターン = カスタム カウント<ept id="p1">**</ept> – カスタム パターンが適用されたノードの数。構造が既存のパターンに適合しなかったことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source><bpt id="p1">**</bpt>Pattern coverage<ept id="p1">**</ept> – The percentage of controls on the form that are covered by the form pattern or a subpattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パターン カバレッジ<ept id="p1">**</ept> – フォーム上のコントロールのうち、フォーム パターンまたはサブパターンの対象となるものの割合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>A value of 100% indicates a fully-covered form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">100% の値は、完全に対象となるフォームを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm27<ept id="p1">](./media/custform27.png)](./media/custform27.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm27<ept id="p1">](./media/custform27.png)](./media/custform27.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>To complete pattern coverage for this form, the Pattern=Unspecified count should be zero.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフォームのパターン カバレッジを完成させるには、Pattern = Unspecified カウントをゼロにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Use the Visual Studio form search to find all instances of “unspecified “in the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio のフォーム検索を使用して、フォーム内の「指定されていない」すべてのインスタンスを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm28<ept id="p1">](./media/custform28.png)](./media/custform28.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm28<ept id="p1">](./media/custform28.png)](./media/custform28.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Because the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab page contains only input controls and no custom layout is required for this FastTab, the Fields and Field Groups pattern should be applied to guarantee a responsive layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一般<ept id="p1">**</ept>タブ ページには入力コントロールのみが含まれており、このクイックタブにはカスタム レイアウトが不要なため、応答レイアウトを保証するためにフィールドおよびフィールド グループのパターンを適用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Right-click <bpt id="p1">**</bpt>General<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Apply pattern<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Fields and Field Groups<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>全般<ept id="p1">**</ept> を右クリックして <bpt id="p2">**</bpt>パターンの適用<ept id="p2">**</ept> をポイントし、<bpt id="p3">**</bpt>フィールドおよびフィールド グループ<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>On the far right of the screen, click <bpt id="p1">**</bpt>Clear search<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面の右端で、<bpt id="p1">**</bpt>検索のクリア<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm29<ept id="p1">](./media/custform29.png)](./media/custform29.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm29<ept id="p1">](./media/custform29.png)](./media/custform29.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> to save the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押してフォームを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Repeat step 1 to run the <bpt id="p1">**</bpt>Form Statistics<ept id="p1">**</ept> add-in a second time to verify the form is fully-covered by patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1 を繰り返して <bpt id="p1">**</bpt>フォーム統計<ept id="p1">**</ept> アドインを再度実行し、フォームがパターンによって完全にカバーされていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm30<ept id="p1">](./media/custform30.png)](./media/custform30.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm30<ept id="p1">](./media/custform30.png)](./media/custform30.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the project and see the updated form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してプロジェクトを実行し、更新されたフォームを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Click <bpt id="p1">**</bpt>Adrian<ept id="p1">**</ept> to go to the details view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>里美 (サンプル)<ept id="p1">**</ept> をクリックし、詳細ビューに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The following illustration shows how the details view now appears after applying the Fields and Field Groups subpattern so that the fields lay out responsively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、フィールドおよびフィールド グループのサブパターンを適用し、フィールドが反応しやすいようにレイアウトした後に詳細ビューがどのように表示されるかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>By changing the browser width, you’ll see how the field layout adjusts to better fill the width of the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーの幅を変更することで、ブラウザーの幅を十分に埋めるためにフィールド レイアウトがどのように調整されるのかが分かります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm31<ept id="p1">](./media/custform31-1024x674.png)](./media/custform31.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm31<ept id="p1">](./media/custform31-1024x674.png)](./media/custform31.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Return to Visual Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio に戻る</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Determine the amount of remaining patterns work in a model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル内で残っているパターンの作業の量を決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Click <bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept>, point to <bpt id="p2">**</bpt>Addins<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Run form patterns report<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>アドイン<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>フォーム パターン レポートを実行<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm32<ept id="p1">](./media/custform32-1024x469.png)](./media/custform32.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm32<ept id="p1">](./media/custform32-1024x469.png)](./media/custform32.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>A notification dialog will be shown when the form patterns report has been generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのパターン レポートが生成されたときに表示される通知ダイアログです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm33<ept id="p1">](./media/custform33.png)](./media/custform33.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm33<ept id="p1">](./media/custform33.png)](./media/custform33.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Open the PatternsReport file in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PatternsReport ファイルを Excel で開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Filter the report to the Fleet Management Tutorial model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアル モデルへのレポートをフィルター処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Click <bpt id="p1">**</bpt>Data<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Filter<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>フィルター<ept id="p2">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Filter the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> column to FleetMgmntTutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetMgmntTutorial への<bpt id="p1">**</bpt>モデル<ept id="p1">**</ept>列をフィルター処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm34<ept id="p1">](./media/custform34-1024x422.png)](./media/custform34.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>CustForm34<ept id="p1">](./media/custform34-1024x422.png)](./media/custform34.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>The report shows pattern-related information regarding the forms in this model including the top-level form pattern currently applied, and the percentage of controls on the form covered by patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートには、現在適用されている最上位のフォーム パターンと、パターンでカバーされているフォーム上のコントロールの割合など、このモデルのフォームに関するパターン関連の情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>This can be used to track the remaining patterns work in one or more models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、1 つまたは複数のモデルの残りのパターンの作業を追跡するために使用できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>