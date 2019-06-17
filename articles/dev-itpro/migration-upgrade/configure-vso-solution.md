<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-vso-solution.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-vso-solution.c083da.0713fc3868acff11f2fabf59a492ed6bfa86fd7d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>0713fc3868acff11f2fabf59a492ed6bfa86fd7d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\configure-vso-solution.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure the Azure DevOps mapping during code migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード移行中の Azure DevOps マッピングのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial shows how to map your development box to the Azure DevOps project after the LCS code upgrade service has completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure the Azure DevOps mapping during code migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード移行中の Azure DevOps マッピングのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial shows how to map your development box to the Azure DevOps project after the LCS code upgrade service has completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The LCS code upgrade service automatically checks your upgraded code into Azure DevOps (formerly called Visual Studio Online).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS コードのアップグレード サービスでは、Azure DevOps (旧 Visual Studio Online) にアップグレードされたコードが自動的に確認されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You will then need to map your development box to the upgrade folder/branch in your Azure DevOps project (The name of the upgrade folder/branch depends on the version you migrated to).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、 開発ボックスを、Azure DevOps プロジェクト内のアップグレード フォルダー/ブランチにマップする必要があります (アップグレード フォルダー/ブランチの名前は移行するバージョンによって異なります)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Within your upgraded folder, you will find three folders:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードされたフォルダー内には、3 つのフォルダーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Metadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Export<ept id="p1">**</ept> is the project that contains the XML files after exporting from Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Export<ept id="p1">**</ept> は、Microsoft Dynamics AX 2012 からのエクスポート後、XML ファイルを含んでいるプロジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This is your metadata in XML format before it is upgraded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはアップグレード前の XML 形式のメタデータです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This is only relevant if you are upgrading from Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Dynamics AX 2012 からアップグレードする場合にのみ関係があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Metadata<ept id="p1">**</ept> is your upgraded code (metadata XML file) on the latest version of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Metadata<ept id="p1">**</ept> は、Microsoft Dynamics 365 for Finance and Operations の最新バージョン上のアップグレード後のコード (メタデータ XML ファイル) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>Projects<ept id="p1">**</ept> are two solutions that you can use during upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト<ept id="p1">**</ept>は、アップグレード中に使用できる 2 つのソリューションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>One solution, CodeMergeSolution, is the solution that contains projects with the elements that have conflicts and need to be resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのソリューションである CodeMergeSolution は、競合し、また解決する必要がある要素を伴うプロジェクトを含むソリューションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The other solution, UpgradedSolution, contains a collection of projects, one for each upgraded model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう 1 つのソリューション、UpgradedSolution には、アップグレードされたモデルごとに 1 つのプロジェクトのコレクションが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, in Azure DevOps, you should see something like the following structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、Azure DevOps で、以下の構造のようなものを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Project<ept id="p1">](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>プロジェクト<ept id="p1">](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Map Azure DevOps to your development box</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps の開発ボックスへのマップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In Visual Studio, connect to your account by going to <bpt id="p1">**</bpt>Team explorer <ph id="ph1">&amp;gt;</ph> Select Team Projects <ph id="ph2">&amp;gt;</ph> Servers <ph id="ph3">&amp;gt;</ph> Add.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>チーム エクスプローラー <ph id="ph1">&amp;gt;</ph> チーム プロジェクトの選択 <ph id="ph2">&amp;gt;</ph> サーバー <ph id="ph3">&amp;gt;</ph> 追加<ept id="p1">**</ept>と進んでアカウントに接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Enter the URL to your team project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チーム プロジェクトに URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure the Azure DevOps account shows up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps アカウントが表示されることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>On the right, choose the project that you want to work on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右側で、作業するプロジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Click <bpt id="p1">**</bpt>Connect<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>接続<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Now you need to map your workspace to the Azure DevOps folders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、ワークスペースを Azure DevOps フォルダーにマップする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Go to the <bpt id="p1">**</bpt>Source Code Explorer<ept id="p1">**</ept> and do this mapping:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソース コード エクスプ ローラ<ept id="p1">**</ept>に移動し、このマッピングを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Projects <ph id="ph1">&amp;gt;</ph> C:<ph id="ph2">\\</ph>Users<ph id="ph3">\\</ph><ph id="ph4">&amp;lt;</ph>username<ph id="ph5">&amp;gt;</ph><ph id="ph6">\\</ph>Documents<ph id="ph7">\\</ph>Visual Studio 2015<ph id="ph8">\\</ph>Projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト <ph id="ph1">&amp;gt;</ph> C:<ph id="ph2">\\</ph>Users<ph id="ph3">\\</ph><ph id="ph4">&amp;lt;</ph>username<ph id="ph5">&amp;gt;</ph><ph id="ph6">\\</ph>Documents<ph id="ph7">\\</ph>Visual Studio 2015<ph id="ph8">\\</ph>Projects</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Metadata <ph id="ph1">&amp;gt;</ph> C:<ph id="ph2">\\</ph>AOSService<ph id="ph3">\\</ph>PackagesLocalDirectory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ <ph id="ph1">&amp;gt;</ph> C:<ph id="ph2">\\</ph>AOSService<ph id="ph3">\\</ph>PackagesLocalDirectory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>On cloud VMs, this folder is located on the I:<ph id="ph1">\\</ph> or J:<ph id="ph2">\\</ph> drive</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド VMs で、このフォルダーは I:<ph id="ph1">\\</ph>または J:<ph id="ph2">\\</ph> ドライブに保管</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On earlier versions, this folder is C:<ph id="ph1">\\</ph>packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンで、このフォルダーは C:<ph id="ph1">\\</ph>パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Important<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>重要<ept id="p1">**</ept>:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you are migrating from Dynamics AX 2012 R3 or earlier, you will be mapping to the metadata folder under the <bpt id="p1">**</bpt>Main<ept id="p1">**</ept> branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 R3 またはそれ以前のバージョンから移行する場合は、<bpt id="p1">**</bpt>メイン<ept id="p1">**</ept>分岐の下のメタデータ フォルダにマッピングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If you are migrating between 2 versions of the new Dynamics AX (Finance and Operations), you will be mapping to the metadata folder under one of the <bpt id="p1">**</bpt>Releases<ept id="p1">**</ept> branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Dynamics AX (Finance and Operations) の 2 つのバージョン間で移行する場合は、いずれかの<bpt id="p1">**</bpt>リリース<ept id="p1">**</ept>の分岐の下のメタデータ フォルダーにマッピングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>vstsmapping<ept id="p1">](./media/vstsmapping.png)](./media/vstsmapping.png)</ept> Once you have mapped these folders, you can synchronize the code to your local box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>vstsmapping<ept id="p1">](./media/vstsmapping.png)](./media/vstsmapping.png)</ept> これらのフォルダーをマップしたら、ローカル ボックスにコードを同期させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Right-click on Metadata and select <bpt id="p1">**</bpt>Get latest<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータを右クリックし、<bpt id="p1">**</bpt>最新バージョンを取得<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Similarly synchronize the Projects folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、プロジェクト フォルダーを同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>After synchronizing the metadata folder, refresh your models in Visual Studio from <bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Model Management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Refresh Models<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ フォルダーを同期した後、<bpt id="p1">**</bpt>Finance and Operations<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>モデル管理<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>モデルの更新<ept id="p3">**</ept> から Visual Studio でモデルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>VSRefreshModels<ept id="p1">](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png)</ept> You are now ready to open your projects, resolve conflicts, build, test and complete your code migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>VSRefreshModels<ept id="p1">](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png)</ept> これで、プロジェクトを立ち上げ、競合を解決し、コードの移行を構築、テスト、および実行する準備が整いました。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>