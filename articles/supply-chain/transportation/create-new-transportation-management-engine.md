<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-new-transportation-management-engine.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-new-transportation-management-engine.4eee11.745aaac9c69b885d9893a6a4bdb9c6ef33240dae.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>745aaac9c69b885d9893a6a4bdb9c6ef33240dae</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\transportation\create-new-transportation-management-engine.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create a new transportation management engine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい輸送管理エンジンの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes how to create a new transportation management engine in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations で新しい輸送管理エンジンを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create a new transportation management engine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい輸送管理エンジンの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes how to create a new transportation management engine in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations で新しい輸送管理エンジンを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Transportation management (TMS) engines define the logic that is used to generate and process transportation rates in Transportation management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸送管理 (TMS) エンジンは、輸送管理で配送率を生成およびプロセスするために使用するロジックを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Microsoft Dynamics 365 for Finance and Operations provides several different engine types that calculate different parameters, such as rates, transit times, and the number of zones that will be crossed during transit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations は、レート、輸送時間、および輸送中に越えるゾーンの数などのさまざまなパラメーターを計算する複数の異なるエンジン タイプを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article explains how to use the Microsoft Visual Studio development environment together with Finance and Operations development tools to create and deploy a new TMS engine, and then how to set up the engine in Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Visual Studio 開発環境と Finance and Operations 開発ツールを使用して新しい TMS エンジンを作成して展開する方法と、次に Operations でエンジンを設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For more information about the engines that Finance and Operations provides, see <bpt id="p1">[</bpt>Transportation management engines<ept id="p1">](transportation-management-engines.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations が提供するエンジンの詳細については、<bpt id="p1">[</bpt>輸送管理エンジン<ept id="p1">](transportation-management-engines.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Create a new TMS engine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい TMS エンジンを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This section explains how to create a class library that has a TMS engine implementation, and how to reference it from a Finance and Operations model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、TMS エンジン実装を持つクラス ライブラリを作成する方法と、Finance and Operations モデルからクラス ライブラリを参照する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To deploy your new engines, you must have a Finance and Operations model that will contain the engines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいエンジンを配置するには、エンジンを含む財務および工程のモデルが必要です。新しいエンジンを展開するには、エンジンを含む Finance and Operations モデルが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Model Management<ept id="p2">**</ept> menu, click <bpt id="p3">**</bpt>Create model<ept id="p3">**</ept> to create a new model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>モデル管理<ept id="p2">**</ept>メニューで、<bpt id="p3">**</bpt>モデルの作成<ept id="p3">**</ept>をクリックして、新しいモデルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>On the first page of the <bpt id="p1">**</bpt>Create model<ept id="p1">**</ept> wizard, name the model <bpt id="p2">**</bpt>TMSEngines<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの作成<ept id="p1">**</ept>ウィザードの最初のページで、モデル名を <bpt id="p2">**</bpt>TMSEngines<ept id="p2">**</ept> にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Creating a model<ept id="p1">](./media/012.png)](./media/012.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>モデルの作成<ept id="p1">](./media/012.png)](./media/012.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the next page, select <bpt id="p1">**</bpt>Create new package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、<bpt id="p1">**</bpt>新しいパッケージの作成<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Creating a new package<ept id="p1">](./media/021.png)](./media/021.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新規パッケージの作成<ept id="p1">](./media/021.png)](./media/021.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the next page, select the <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> model to reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、参照する <bpt id="p1">**</bpt>ApplicationSuite<ept id="p1">**</ept> モデルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>(The <bpt id="p1">**</bpt>ApplicationPlatform<ept id="p1">**</ept> model is preselected.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>ApplicationPlatform<ept id="p1">**</ept> モデルが事前に選択されています)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Selecting the model to reference<ept id="p1">](./media/032.png)](./media/032.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>参照するモデルの選択<ept id="p1">](./media/032.png)](./media/032.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>On the next page, click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept> to confirm the creation of a new model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept>をクリックして新しいモデルの作成を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Completing model creation<ept id="p1">](./media/042.png)](./media/042.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>モデル作成の完了<ept id="p1">](./media/042.png)](./media/042.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In a new solution, create a new Finance and Operations project, and name it <bpt id="p1">**</bpt>TMSThirdParty<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいソリューションで、新しい Finance and Operations プロジェクトを作成し、<bpt id="p1">**</bpt>TMSThirdParty<ept id="p1">**</ept> と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In the project properties, set the project's model to <bpt id="p1">**</bpt>TMSEngines<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト プロパティで、プロジェクトのモデルを <bpt id="p1">**</bpt>TMSEngines<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Add a new C<ph id="ph1">\#</ph> class library to your solution, and name it <bpt id="p1">**</bpt>ThirdPartyTMSEngines<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションに新しい C<ph id="ph1">\#</ph> クラス ライブラリを追加し、<bpt id="p1">**</bpt>ThirdPartyTMSEngines<ept id="p1">**</ept> という名前をつけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In the ThirdPartyTMSEngines project, add references to Finance and Operations–specific assemblies:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ThirdPartyTMSEngines プロジェクトで、Finance and Operations 固有のアセンブリへの参照を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Application assemblies that enable X++ types to be referenced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ タイプの参照を有効にするアプリケーション アセンブリ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>These assemblies can be found in the following locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアセンブリは、次の場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><ph id="ph1">\[</ph>Packages root<ph id="ph2">\]</ph> is the path of the location where all the deployed Dynamics 365 for Finance and Operations assemblies are placed, such as C:<ph id="ph3">\\</ph>Packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>パッケージ ルート<ph id="ph2">\]</ph> は、C:<ph id="ph3">\\</ph>パッケージなど、展開された Dynamics 365 for Finance and Operations アセンブリが配置されている場所のバスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Framework assemblies that enable access to data, LINQ, and auxiliary functions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ、LINQ、および補助機能へのアクセスを有効にするフレームワーク アセンブリ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>All these assembles can be found in <ph id="ph1">\[</ph>Packages root<ph id="ph2">\]</ph><ph id="ph3">\\</ph>bin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべてのアセンブリは <ph id="ph1">\[</ph>パッケージ ルート<ph id="ph2">\]</ph><ph id="ph3">\\</ph> 在庫置場で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The core TMS assembly (which contains engines) and the TMS base assembly (which contains helpers, constants, data transfer class definitions, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コア TMS アセンブリ (エンジンを含む) と TMS ベース アセンブリ (ヘルパー、定数、データ転送クラス定義などを含む)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>These assemblies can be found in the following locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアセンブリは、次の場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Rename the C<ph id="ph1">\#</ph> class that is automatically generated in the ThirdPartyTMSEngines project to <bpt id="p1">**</bpt>SampleRatingEngine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ThirdPartyTMSEngines プロジェクトで生成された C<ph id="ph1">\#</ph> クラスの名前を <bpt id="p1">**</bpt>SampleRatingEngine<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Implement the engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンジンを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Because we are creating a rate engine in this example, we inherit from the base class for rate engines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例ではレート エンジンを作成しているため、レート エンジンの基本クラスを継承しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The base class implements most of the rate engine interface (<bpt id="p1">**</bpt>TMSFwkIRateEngine<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスは、レート エンジン インターフェイス (<bpt id="p1">**</bpt>TMSFwkIRateEngine<ept id="p1">**</ept>) のほとんどを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>We just have to implement the rate method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レート法の実装が必要なだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To keep this example simple, we will make this method register a hard-coded rate of 100.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例を単純にするために、このメソッドではハードコーディングされたレートを 100 として登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can create engines that implement any of the engine interfaces, such as <bpt id="p1">**</bpt>TMSFwkIAccessorialEngine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TMSFwkIAccessorialEngine<ept id="p1">**</ept> などの、任意のエンジン インターフェイスを実装するエンジンを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>All the engine interfaces are defined in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのエンジン インターフェイスは X++ で定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Build the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Add a new reference to the TMSThirdParty project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TMSThirdParty プロジェクトに新しい参照を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The reference should point to the ThirdPartyTMSEngines project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照は、ThirdPartyTMSEngines プロジェクトを指す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>When you've finished, your solution should look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、ソリューションは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>The solution, which includes a reference to the TMSThirdParty project<ept id="p1">](./media/052.png)](./media/052.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>TMSThirdParty プロジェクトへの参照を含むソリューション<ept id="p1">](./media/052.png)](./media/052.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Build the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Verify that the new library appears in the <bpt id="p1">**</bpt>References<ept id="p1">**</ept> node in Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプ ローラーの <bpt id="p1">**</bpt>参照<ept id="p1">**</ept> ノードに新しいライブラリが表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>The new library in Application Explorer’s References node<ept id="p1">](./media/061.png)](./media/061.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>アプリケーション エクスプ ローラーの参照ノード内の新しいライブラリ<ept id="p1">](./media/061.png)](./media/061.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Deploy the TMS engine as a package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TMS エンジンをパッケージとして配置する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>One way to deploy third-party TMS engines is through a deployment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サードパーティの TMS エンジンを配置する 1 つの方法は、配置パッケージを介することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This approach is recommended in a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境では、この方法をお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In a development environment, you can manually copy the assemblies, as described in the next section, "Set up a TMS engine in Finance and Operations."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境では、次のセクション「Finance and Operations で TMS エンジンを設定する」で説明するように手動でアセンブリをコピーできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>To deploy the engine as a package, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンジンをパッケージとして展開するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Deploy<ept id="p2">**</ept> menu, click <bpt id="p3">&lt;strong&gt;</bpt>Create Deployment Package<ept id="p3">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>配置<ept id="p2">**</ept> メニューで、<bpt id="p3">&lt;strong&gt;</bpt>配置パッケージの作成<ept id="p3">&lt;/strong&gt;</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In the <bpt id="p1">**</bpt>Create Deployment Package<ept id="p1">**</ept> dialog box, select the TMSEngines model, and enter the path where you want to store your package files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配置パッケージの作成<ept id="p1">**</ept>ダイアログ ボックスで、TMSEngines モデルを選択し、パッケージ ファイルを格納する場所のパスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Selecting the TMSEngines model <ept id="p1">](./media/071.png)](./media/071.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>TMSEngines モデルの選択<ept id="p1">](./media/071.png)](./media/071.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You can now deploy the package to the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージをターゲット環境に展開することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For a tutorial, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../../dev-itpro/deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアルについては、<bpt id="p1">[</bpt>配置可能パッケージのインストール<ept id="p1">](../../dev-itpro/deployment/install-deployable-package.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Set up the TMS engine in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations で TMS エンジンを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This section explains how to set up Finance and Operations to use a TMS engine, and shows how the new engine that we have created is used in rate shopping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、TMS エンジンを使用するために Finance and Operations を設定する方法と、作成した新しいエンジンをレート ショッピングに使用する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The example in this section uses the USMF demo data company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションの例では、USMF デモ データ会社を使用しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Create a new engine as described in the "Create a new TMS engine" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「新しい TMS エンジンの作成」の説明に従って、新しいエンジンを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Build your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Copy the resulting assembly into the binary location of the Finance and Operations server, <ph id="ph1">\[</ph>AOSWebRoot<ph id="ph2">\]</ph>bin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果のアセンブリを Finance and Operations サーバーのバイナリの場所、<ph id="ph1">\[</ph>AOSWebRoot<ph id="ph2">\]</ph>bin にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> This step is relevant only in a development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このステップは、開発環境にのみ関連します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In a production environment, you should deploy through a deployment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境では、配置パッケージを介して配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For instructions, see the previous section, "Deploy the TMS engine as a package."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順については、前のセクションの「パッケージとして TMS エンジンを配置する」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In Finance and Operations, on the <bpt id="p1">**</bpt>Rate engines<ept id="p1">**</ept> page, create a new rating engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、<bpt id="p1">**</bpt>レート エンジン<ept id="p1">**</ept> ページで新しい評価エンジンを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The engine should point to the engine assembly that is produced by building the engine class library and the engine class that you implemented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンジンは、実装したエンジン クラス ライブラリとエンジン クラスを作成して生成されたエンジン アセンブリを指す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Creating a new rating engine on the Rate engines page<ept id="p1">](./media/081.png)](./media/081.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>レート エンジン ページで新規評価エンジンの作成<ept id="p1">](./media/081.png)](./media/081.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Create a shipping carrier that uses the Sample rate engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル レート エンジンを使用する配送業者を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Because our engine doesn't use any data in Finance and Operations, you don’t have to assign a rate master.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">当社のエンジンは Finance and Operations においていかなるデータも使用しないため、レート マスターを割り当てる必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Creating a new shipping carrier <ept id="p1">](./media/092.png)](./media/092.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新規出荷の配送業者の作成<ept id="p1">](./media/092.png)](./media/092.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>On the <bpt id="p1">**</bpt>Rate route workbench<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Rate shop<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>工順ワークベンチの評価<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>レート ショップ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>You should see a rate of 100.00 from SampleCarrier, as shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに示すように、SampleCarrier から 100.00 のレートが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In this example, we are rate shopping for a route from warehouse 24 to customer US-004.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、倉庫 24 から顧客 US-004 へのルートの輸送料を検索しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>However, but because the rate is hard-coded, you will always see a rate of 100.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、料金がハードコーディングされているために、100.00 の料金が常に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Rate route workbench<ept id="p1">](./media/101.png)](./media/101.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>工順ワークベンチの評価<ept id="p1">](./media/101.png)](./media/101.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Tips and tricks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヒントや秘訣</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If you’re using development tools for Finance and Operations, it's useful to add a new Finance and Operations project to your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の開発ツールを使用している場合、ソリューションに新しい Finance and Operations プロジェクトを追加すると便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>If you set this project as your startup project and start a debugging session, you can debug both X++ and C<ph id="ph1">\#</ph> code in the same debugging session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロジェクトをスタートアップ プロジェクトとして設定した場合、デバッグ セッションを開始すると、同じデバッグ セッションで X++ と C<ph id="ph1">\#</ph> コードの両方のコードをデバッグできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Every time that you change and recompile your ThirdPartyTMSEngines project, you must manually copy the resulting assembly to the Finance and Operations binary location or deploy through a deployment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ThirdPartyTMSEngines プロジェクトを変更して再コンパイルするたびに、アセンブリの結果を Finance and Operations バイナリの場所に手動でコピーするか、展開パッケージを通じて展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Otherwise, you might run by using a stale assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、古いアセンブリを使用して実行される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>After you execute TMS-specific operations in Finance and Operations, the Internet Information Services (IIS) worker process might lock the ThirdPartyTMSEngines assembly so that the assembly can’t be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations で TMS 固有の操作を実行した後、Internet Information Services (IIS) ワーカー プロセスによって ThirdPartyTMSEngines アセンブリが、ロックされアセンブリを更新することができなくなることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In this case, restart the w3svc process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、w3svc プロセスを再起動します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>