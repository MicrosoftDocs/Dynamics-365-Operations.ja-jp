<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-data-model-elements.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-data-model-elements.0d1bb9.ff58bb6067cd516bf3fb5054879ca78fc458ce09.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ff58bb6067cd516bf3fb5054879ca78fc458ce09</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\create-data-model-elements.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create models and data model elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルとデータ モデル要素の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you'll use Visual Studio's Dynamics 365 menu to create a new model named Fleet Management tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、フリート管理チュートリアルという名前の新しいモデルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>You'll also create and edit new model elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいモデルの要素を作成および編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Create models and data model elements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルとデータ モデル要素の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this tutorial, you'll use Visual Studio's Dynamics 365 menu to create a new model named Fleet Management tutorial in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、Microsoft Dynamics 365 for Finance and Operations でフリート管理チュートリアルという名前の新しいモデルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You'll also create and edit new model elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しいモデルの要素を作成および編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This tutorial requires that you have access to a Finance and Operations environment, and that you be provisioned as an administrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Finance and Operations 環境にアクセスし、管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Keywords</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キーワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Model<ept id="p1">**</ept> - You configure your model to refer to two other models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept> - 他の 2 つのモデルを参照するモデルをコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This enables your model to reference metadata and code elements that are in other packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、モデルは他のパッケージにあるメタデータとコード要素を参照できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Project<ept id="p1">**</ept> - You create a <bpt id="p2">**</bpt>Unified Operations<ept id="p2">**</ept> project, and you associate your project to your new model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト<ept id="p1">**</ept> -<bpt id="p2">**</bpt>Unified Operations<ept id="p2">**</ept> プロジェクトを作成し、プロジェクトを新しいモデルに関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You add elements to your project, which are also added to your model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要素をプロジェクトに追加します。これはモデルにも追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Specifically, you add an extended data type (EDT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、拡張データ型 (EDT) を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You also add a table that you populate with fields and a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、フィールドおよびメソッドで入力するテーブルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> - Each time you add an item to your project, a designer is displayed that is tailored to the item type you selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept> - プロジェクトに品目を追加するたびに、選択した品目タイプに合わせたデザイナーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window adjusts each time a different node of the designer is highlighted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウは、デザイナーの異なるノードが強調表示されるたびに調整されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You make updates in the designers and in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーおよび <bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで更新を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>EDT<ept id="p1">**</ept> - Extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EDT<ept id="p1">**</ept> - 拡張データ型。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create the Fleet Management tutorial model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理チュートリアル モデルを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Start Visual Studio using <bpt id="p1">**</bpt>Run as administrator<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>管理者として実行<ept id="p1">**</ept> を使用して Visual Studio を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>From the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>Model Management <ph id="ph1">&amp;gt;</ph> Create model<ept id="p2">**</ept> to open the <bpt id="p3">**</bpt>Create model<ept id="p3">**</ept> wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> ウィンドウから、<bpt id="p2">**</bpt>モデル管理 <ph id="ph1">&amp;gt;</ph> モデルの作成<ept id="p2">**</ept>を選択して、<bpt id="p3">**</bpt>モデルの作成<ept id="p3">**</ept>ウィザードを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Enter the following values for model parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル パラメーターの以下の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Model name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>FleetMgmntTutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetMgmntTutorial</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Model publisher<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル発行元<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Microsoft Corp</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Corp</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Layer<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レイヤー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>isv</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">isv</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Model description<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの説明<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>This tutorial shows how to build the Fleet Management application by using the Microsoft Dynamics AX  development tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、Microsoft Dynamics AX の開発ツールを使用して、フリート管理 アプリケーションを構築する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Model display name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの表示名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Fleet Management Tutorial</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理のチュートリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Your model name must be <bpt id="p1">**</bpt>FleetMgmntTutorial<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの名前は <bpt id="p1">**</bpt>FleetMgmntTutorial<ept id="p1">**</ept> である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Don't use any other name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の名前は使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In other tutorials, you'll overwrite model elements in this model by importing a project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のチュートリアルでは、プロジェクトをインポートすることでこのモデル内のモデル要素を上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If the model you create in this tutorial isn't named <bpt id="p1">**</bpt>FleetMgmntTutorial<ept id="p1">**</ept>, you may not be able to correctly import the project in other tutorials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルで作成したモデルに <bpt id="p1">**</bpt>FleetMgmntTutorial<ept id="p1">**</ept> という名前が付けられていない場合、その他のチュートリアルでプロジェクトが正しくインポートできない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to advance to the next page, and then select <bpt id="p2">**</bpt>Create New Package<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックして次のページに移動し、次に<bpt id="p2">**</bpt>新しいパッケージの作成<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The model you're creating will have its own package and build its own .NET assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成しているモデルは独自のパッケージを持ち、独自の .NET アセンブリを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Package<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/package_datamodel.png)](./media/package_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Package<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/package_datamodel.png)](./media/package_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to advance to the <bpt id="p2">**</bpt>Select referenced models<ept id="p2">**</ept> step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>参照モデルを選択<ept id="p2">**</ept>ステップに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select <bpt id="p1">**</bpt>Application Platform<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Application Foundation<ept id="p2">**</ept> as referenced models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照されるモデルとして <bpt id="p1">**</bpt>アプリケーション プラットフォーム<ept id="p1">**</ept> および <bpt id="p2">**</bpt>アプリケーション基盤<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ReferenceModels<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ReferenceModels<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Verify that you've selected the correct referenced models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しい参照モデルを選択していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to advance to the <bpt id="p2">**</bpt>Summary<ept id="p2">**</ept> step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>概要<ept id="p2">**</ept>ステップに進みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Verify the information on the summary page, and then select the <bpt id="p1">**</bpt>Create new project<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Make this my default model for new projects<ept id="p2">**</ept> check boxes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要ページの情報を確認してから、<bpt id="p1">**</bpt>新規プロジェクトの作成<ept id="p1">**</ept> および <bpt id="p2">**</bpt>これを新規プロジェクトの自分の既定のモデルにする<ept id="p2">**</ept> チェック ボックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Summary<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/summary_datamodel.png)](./media/summary_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Summary<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/summary_datamodel.png)](./media/summary_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The <bpt id="p1">**</bpt>New Project<ept id="p1">**</ept> dialog box opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいプロジェクト<ept id="p1">**</ept> ダイアログ ボックスが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Under <bpt id="p1">**</bpt>Templates<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Dynamics 365<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テンプレート<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>Dynamics 365<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Select the <bpt id="p1">**</bpt>Unified Operations<ept id="p1">**</ept> template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Unified Operations<ept id="p1">**</ept> テンプレートを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Enter the following values in the fields in the dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスのフィールドに次の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>Name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>FMTDataModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTDataModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt>Location<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保管場所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>C:<ph id="ph1">\\</ph>FMLab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>FMLab</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Solution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Add to solution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションへの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>NewProject<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>NewProject<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to create the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを作成するには、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Create the FMTAddress extended data type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTAddress の拡張データ型を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept>, point to <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>New Item<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> を右クリックして<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をポイントしてから<bpt id="p4">**</bpt>新しい項目<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Under <bpt id="p1">**</bpt>Dynamics 365 Items<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Data Types<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365 品目<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>データ型<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Click <bpt id="p1">**</bpt>EDT String<ept id="p1">**</ept> to select the new item type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EDT 文字列<ept id="p1">**</ept>をクリックし、を新しい項目の種類を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>FMTAddress<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>FMTAddress<ept id="p2">**</ept> と入力してから<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>NewItem<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>NewItem<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>This adds a new EDT model element to the project, and opens the EDT designer for the new element, as shown in the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、新しい EDT モデル要素をプロジェクトに追加され、次の図に示すように、新しい要素の EDT デザイナーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>EDTelement<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EDTelement<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Select the root node of <bpt id="p1">**</bpt>FMTAddress<ept id="p1">**</ept> in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで <bpt id="p1">**</bpt>FMTAddress<ept id="p1">**</ept> ルート ノードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, in the <bpt id="p2">**</bpt>Appearance section<ept id="p2">**</ept>, set the following properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウの<bpt id="p2">**</bpt>外観セクション<ept id="p2">**</ept>で、次のプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">**</bpt>Property<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>Help Text<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヘルプ テキスト<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Check online help.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンライン ヘルプをチェックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Label<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドレス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>String Size<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列サイズ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>75</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">75</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>EDTProperty<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>EDTProperty<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> to save the EDT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押して EDT を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Add existing model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のモデルの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Add the other required model element files to the current model and project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のモデルとプロジェクトに他の必要なモデル要素ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You can do this quickly by using the <bpt id="p1">**</bpt>Add existing item<ept id="p1">**</ept> feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既存の品目を追加<ept id="p1">**</ept> フィーチャーを使用することにより、これを素早く実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In the <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept>, point to <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Existing Item<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> を右クリックして<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をポイントしてから<bpt id="p4">**</bpt>既存の項目<ept id="p4">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Browse to C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>EDT<ph id="ph3">\\</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:<ph id="ph1">\\</ph>FMLab<ph id="ph2">\\</ph>EDT<ph id="ph3">\\</ph> を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ExistingItem<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ExistingItem<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Press <bpt id="p1">**</bpt>Ctrl+A<ept id="p1">**</ept> to select all of the files, and then click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+A<ept id="p1">**</ept> を押してすべてのファイルを選択し、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Create the FMTCustomer table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer テーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Add <ph id="ph1">&amp;gt;</ph> New Item<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> を右クリックしてから<bpt id="p3">**</bpt>追加 <ph id="ph1">&amp;gt;</ph> 新しい項目<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In the left pane, expand <bpt id="p1">**</bpt>Installed<ept id="p1">**</ept>, expand <bpt id="p2">**</bpt>Dynamics 365 Items<ept id="p2">**</ept> and then click <bpt id="p3">**</bpt>Data Model<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左ウィンドウで、<bpt id="p1">**</bpt>インストール済み<ept id="p1">**</ept>を展開し、<bpt id="p2">**</bpt>Dynamics 365 品目<ept id="p2">**</ept>を展開してから、<bpt id="p3">**</bpt>データ モデル<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the list of artifacts, select <bpt id="p1">**</bpt>Table<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーティファクトの一覧で<bpt id="p1">**</bpt>テーブル<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>FMTCustomer<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>FMTCustomer<ept id="p2">**</ept> と入力してから<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The table designer opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル デザイナーが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Add<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/add_datamodel.png)](./media/add_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Add<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/add_datamodel.png)](./media/add_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Add fields to the FMTCustomer table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer テーブルへのフィールドの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>In the table designer for FMTCustomer, you now add several fields to the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTCustomer のテーブル デザイナーで、テーブルに複数のフィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>AddFields<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>AddFields<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>To add each field, right-click <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then select a type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各フィールドを追加するには、<bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept> をクリックして、タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>As you add each field, you must specify the field name and certain other values in the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, as described in the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各フィールドを追加すると、次の表に示すように、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウでフィールド名とその他の特定の値を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><bpt id="p1">**</bpt>Type<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイプ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Property values<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>Date<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>CCExpiryDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CCExpiryDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Extended Data Type = FMTCCExpiryDate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = FMTCCExpiryDate</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドレス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extended Data Type = FMTAddressHelp Text = Help text for the address field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = FMTAddressHelp テキスト = アドレス フィールドのヘルプ テキスト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>CellPhone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CellPhone</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Extended Data Type = Phone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = 電話</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>CreditCardNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CreditCardNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Extended Data Type = FMTCreditCardNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = FMTCreditCardNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>DriversLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DriversLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Extended Data Type = FMTDriversLicense</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = FMTDriversLicense</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>String Size = 80Label = Email</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズ = 80Label = 電子メール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Extended Data Type = FirstName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = FirstName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">姓</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Extended Data Type = LastName</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型 = LastName</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>License</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>String Size = 100Label = License</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズ = 100Label = ライセンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><bpt id="p1">**</bpt>String<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Thumbnail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">縮小版</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>String Size = 100Label = Thumbnail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列サイズ = 100Label = サムネイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>For all new fields in the table that reference an EDT, you can create the field by simply dragging the EDT element from <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept> and dropping it on the <bpt id="p3">**</bpt>Fields<ept id="p3">**</ept> node of the <bpt id="p4">**</bpt>FMTCustomer<ept id="p4">**</ept> table in the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT を参照するテーブル内のすべての新しいフィールドでは、<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>または<bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>から EDT エレメントをドラッグし、デザイナーの <bpt id="p4">**</bpt>FMTCustomer<ept id="p4">**</ept> テーブルの<bpt id="p3">**</bpt>フィールド<ept id="p3">**</ept>ノードをドロップするだけで、フィールドを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>AdministratorArrow<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>AdministratorArrow<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> to save the new fields on the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押して、テーブルに新しいフィールドを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Add fields to field groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド グループへのフィールドの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Prepare to add some of the fields to the <bpt id="p1">**</bpt>AutoSummary<ept id="p1">**</ept> field group by selecting the fields in the following list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の一覧のフィールドを選択して、一部の不フィールドを <bpt id="p1">**</bpt>AutoSummary<ept id="p1">**</ept> フィールド グループに追加する準備をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>To select multiple fields, hold down the Ctrl key while you click each field:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source><bpt id="p1">**</bpt>Address<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>住所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source><bpt id="p1">**</bpt>CCExpiryDate<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CCExpiryDate<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source><bpt id="p1">**</bpt>CellPhone<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CellPhone<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><bpt id="p1">**</bpt>CreditCardNum<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CreditCardNum<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">**</bpt>DriversLicense<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DriversLicense<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source><bpt id="p1">**</bpt>Email<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>電子メール<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">**</bpt>LastName<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>姓<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Expand the <bpt id="p1">**</bpt>Field Groups<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド グループ<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Drag the selected fields to the <bpt id="p1">**</bpt>AutoSummary<ept id="p1">**</ept> node</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したフィールドを <bpt id="p1">**</bpt>AutoSummary<ept id="p1">**</ept> ノードにドラッグします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Use the same technique to add the fields <bpt id="p1">**</bpt>FirstName<ept id="p1">**</ept>, <bpt id="p2">**</bpt>LastName<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>CellPhone<ept id="p3">**</ept> to the <bpt id="p4">**</bpt>AutoReport<ept id="p4">**</ept> field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ方法を使用して、<bpt id="p1">**</bpt>氏名<ept id="p1">**</ept>、<bpt id="p2">**</bpt>姓<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>携帯<ept id="p3">**</ept>フィールドを<bpt id="p4">**</bpt>自動レポート<ept id="p4">**</ept>フィールド グループに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Save the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Add a method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Add the X++ method named <bpt id="p1">**</bpt>fullName<ept id="p1">**</ept> to the <bpt id="p2">**</bpt>FMTCustomer<ept id="p2">**</ept> table by right-clicking the <bpt id="p3">**</bpt>Methods<ept id="p3">**</ept> node, and then clicking <bpt id="p4">**</bpt>New Method<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>Methods<ept id="p3">**</ept> ノードを右クリックし、<bpt id="p4">**</bpt>New Method<ept id="p4">**</ept> をクリックして、<bpt id="p2">**</bpt>FMTCustomer<ept id="p2">**</ept> テーブルに <bpt id="p1">**</bpt>fullName<ept id="p1">**</ept> という名前の X++ メソッドを 追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>In the code editor, replace the default method code with the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターで、既定のメソッドのコードを次のコードに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>When you type “this.”, choose the field from the IntelliSense list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「this.」を入力するとき、IntelliSense リストからフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Save the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Update the FMTAddress EDT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTAddress EDT の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, expand the <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> プロジェクトを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Right-click <bpt id="p1">**</bpt>FMTAddress<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMTAddress<ept id="p1">**</ept> を右クリックしてから、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>The <bpt id="p1">**</bpt>EDT designer<ept id="p1">**</ept> opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EDT デザイナー<ept id="p1">**</ept>が開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>In the <bpt id="p1">**</bpt>EDT designer<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>FMTAddress<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EDT デザイナー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTAddress<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, in the <bpt id="p2">**</bpt>Reference Table<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>FMTCustomer<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウの<bpt id="p2">**</bpt>参照テーブル<ept id="p2">**</ept> フィールドで、<bpt id="p3">**</bpt>FMTCustomer<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">**</bpt>Tip:<ept id="p1">**</ept> Click the drop-down list, and then type the prefix "FMT" in the search box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヒント:<ept id="p1">**</ept> ドロップダウン リストをクリックし、検索ボックスに、接頭語「FMT」を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>This filters the drop-down list to only show tables that contain "FMT" in their name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、名前に「FMT」が含まれている表のみが表示されるように、ドロップダウン リストがフィルター処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Select the <bpt id="p1">**</bpt>FMTCustomer<ept id="p1">**</ept> table from the list of filtered entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルター処理されたエントリの一覧から <bpt id="p1">**</bpt>FMTCustomer<ept id="p1">**</ept> テーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>SearchFMT<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>SearchFMT<ph id="ph2">\_</ph>DataModel<ept id="p1">](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Save the EDT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Build the FMTDataModel project and the Fleet Management tutorial model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMTDataModel プロジェクトと フリート管理チュートリアル モデルの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Rebuild<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMTDataModel<ept id="p2">**</ept> を右クリックしてから<bpt id="p3">**</bpt>リビルド<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>To do a full build of the entire model, on the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Build models<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル全体の完全なビルドを行うには、<bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>モデルをビルド<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Clear the check box for all models except for <bpt id="p1">**</bpt>Fleet Management Tutorial<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート管理チュートリアル<ept id="p1">**</ept>以外のすべてのモデルのチェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>On the <bpt id="p1">**</bpt>Options<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Run Best practice checks<ept id="p2">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オプション<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>推奨チェックの実行<ept id="p2">**</ept>チェック ボックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Note that other options available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能なその他のオプションに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>On the <bpt id="p1">**</bpt>Models<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Build<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>ビルド<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept>  in the dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで <bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>On the <bpt id="p1">**</bpt>Window<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Close All Documents<ept id="p2">**</ept>, to close all open documents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ウィンドウ<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>すべてのドキュメントを閉じる<ept id="p2">**</ept>をクリックして、開いているすべてのドキュメントを閉じます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>