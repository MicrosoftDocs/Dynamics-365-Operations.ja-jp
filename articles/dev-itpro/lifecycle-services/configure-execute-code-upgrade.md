<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-execute-code-upgrade.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-execute-code-upgrade.4f4eb0.d4ea5a558eeb04d227f7f59d736379657a1a55b3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d4ea5a558eeb04d227f7f59d736379657a1a55b3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\configure-execute-code-upgrade.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure the code upgrade service in Lifecycle Services (LCS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) で、コード アップグレード サービスを構成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure the <bpt id="p1">&lt;strong&gt;</bpt>Code upgrade <ept id="p1">&lt;/strong&gt;</ept>tile in Lifecycle Services (LCS) to migrate your solution to the latest version of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Lifecycle Services (LCS) の <bpt id="p1">&lt;strong&gt;</bpt>コード アップグレード<ept id="p1">&lt;/strong&gt;</ept> タイルを構成して、ソリューションを最新バージョンの Finance and Operations に移行する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure the code upgrade service in Lifecycle Services (LCS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) で、コード アップグレード サービスを構成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to configure the <bpt id="p1">&lt;strong&gt;</bpt>Code upgrade <ept id="p1">&lt;/strong&gt;</ept>tile in Lifecycle Services (LCS) to migrate your solution to the latest version of Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Lifecycle Services (LCS) の<bpt id="p1">&lt;strong&gt;</bpt>コード アップグレード<ept id="p1">&lt;/strong&gt;</ept> タイルを構成して、ソリューションを最新バージョンの Dynamics 365 for Finance and Operations に移行する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The code upgrade tool operates by connecting to your Azure DevOps project, locating your Trunk<ph id="ph1">\\</ph>Main branch, branching to a new branch which will be named as Releases<ph id="ph2">\\</ph><ph id="ph3">\&lt;</ph>version number<ph id="ph4">\&gt;</ph>, and then performing the code upgrade there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのアップグレード ツールは、Azure DevOps プロジェクトに接続し、トランク<ph id="ph1">\\</ph>メインブランチを検索し、リリース<ph id="ph2">\\</ph><ph id="ph3">\&lt;</ph>バージョン番号<ph id="ph4">\&gt;</ph>という名前の新しいブランチに分岐してから、コードのアップグレードを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>After this process is complete you can synchronize your Finance and Operations developer environment to this new branch under Releases<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>version number<ph id="ph3">\&gt;</ph> and resolve conflicts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスが完了した後、Finance and Operations 開発環境を、リリース <ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>バージョン番号<ph id="ph3">\&gt;</ph> 下の新しいブランチに同期させ、競合を解決できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>When you have compiled and tested your upgraded code you can merge the new branch back into Trunk<ph id="ph1">\\</ph>Main, using source control explorer in Visual Studio and the process is complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード後のコードをコンパイルしてテストしたとき、新しいブランチを Visual Studio のソース管理エクスプ ローラーを使用して Trunk<ph id="ph1">\\</ph>Main にマージすると、プロセスが完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Dynamics 365 for Finance and Operations version 8.0 and newer, does not allow customization via overlayering of Microsoft models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations バージョン 8.0 およびそれ以降では、Microsoft モデルをオーバーレイしてカスタマイズすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Before you upgrade, you must have have a plan to refactor your customizations into extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードする前に、カスタマイズを拡張機能にリファクターする計画が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For more information, see the <bpt id="p1">[</bpt>Extensibility homepage<ept id="p1">](../extensibility/extensibility-home-page.md)</ept> and <bpt id="p2">[</bpt>Refactor overlayering on 8.0 environments<ept id="p2">](../extensibility/refactoring-over-layering.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>拡張機能のホームページ<ept id="p1">](../extensibility/extensibility-home-page.md)</ept>および <bpt id="p2">[</bpt>8.0 環境でオーバーレイをリファクタリングする<ept id="p2">](../extensibility/refactoring-over-layering.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Create the Trunk<ph id="ph1">\\</ph>Main folder structure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランク<ph id="ph1">\\</ph>メイン フォルダー構造を作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For the code upgrade service to recognize your source code, your Azure DevOps project must contain a Team Foundation Version Control (TFVC) code repository.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース コードを識別するコード アップグレード サービスについては、Azure DevOps プロジェクトには Team Foundation バージョン管理 (TFVC) コード リポジトリが含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, the code repository folder structure must conform to the following strict pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、コード リポジトリ フォルダー構造は、次の厳密なパターンに準拠している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For code and metadata: /<ph id="ph1">&lt;DevOps project name&gt;</ph>/Trunk/Main/Metadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードおよびメタデータ: /<ph id="ph1">&lt;DevOps project name&gt;</ph>/Trunk/Main/Metadata</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For Visual Studio project and solution files: /<ph id="ph1">&lt;DevOps project name&gt;</ph>/Trunk/Main/Projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio プロジェクトおよびソリューション ファイル: /<ph id="ph1">&lt;DevOps project name&gt;</ph>/Trunk/Main/Projects</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You can create new folders directly in the Azure DevOps web interface under <bpt id="p1">**</bpt>Repos<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフォルダーは、Azure DevOps Web インターフェイスの <bpt id="p1">**</bpt>リポジトリ<ept id="p1">**</ept> で直接作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Folder names are case sensitive, that is, you must use Main and not MAIN, or the code upgrade service will not recognize the folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォルダー名は大文字と小文字を区別していて、つまり、メインおよびメインでない、またはコードのアップグレード サービスはフォルダーを認識しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Azure DevOps projects use Git version control by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトは、既定で Git バージョン管理を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You will need to add a TFVC repository.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TFVC リポジトリを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Go to Project settings then Repositories.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト設定へ移動し、リポジトリに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select New repository.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[新しいリポジトリ] を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In the Type field, select TFVC, and then click Create</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[種類] フィールドで、[TFVC] を選択し、[作成] をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Create a personal access token</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個人用アクセス トークンを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>To connect to a Azure DevOps project, LCS is authenticated using a personal access token.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Use the following steps to create a personal access token in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で個人用アクセス トークンを作成するには、以下の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If you have already configured your LCS project to connect to your Azure DevOps project, you can skip this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトを Azure DevOps プロジェクトへ接続できるように構成する場合、このセクションを省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Sign in to visualstudio.com and locate your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">visualstudio.com にログインし、Azure DevOps プロジェクトを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In the top right corner, hover over your name, a menu appears, select <bpt id="p1">**</bpt>Security<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅で、名前をポイントするとメニューが表示され、<bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to create a new personal access token, give it a name, and then enter the amount of time that you want the token to last for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックして、新しい個人用アクセス トークンを作成し、名前を付けて、トークンが使用できる期間を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Click <bpt id="p1">**</bpt>Create Token<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トークンの作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Code upgrade create token<ept id="p1">](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コード アップグレードのトークンの作成<ept id="p1">](./media/codeupgrademaketoken.png)](./media/codeupgrademaketoken.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Copy the token to your clipboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トークンをクリップボードにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You will not be able to find the token details after this step is completed, so be sure that you have copied the token before navigating away from this page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップが完了したら、トークンの詳細情報を見つけることはできません。したがって、このページから移動する前に、かならずトークンをコピーしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Configure your Lifecycle Services project to connect to Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services プロジェクトをコンフィギュレーションして Azure DevOps に接続する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In your LCS project, go to the <bpt id="p1">**</bpt>Project settings<ept id="p1">**</ept> tile, select <bpt id="p2">**</bpt>Visual Studio Team Services<ept id="p2">**</ept>, and then select the <bpt id="p3">**</bpt>Setup Visual Studio Team Services<ept id="p3">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトで、<bpt id="p1">**</bpt>プロジェクト設定<ept id="p1">**</ept>タイルに移動し、<bpt id="p2">**</bpt>Visual Studio Team Services<ept id="p2">**</ept> を選択してから、<bpt id="p3">**</bpt>Visual Studio Team Services の設定<ept id="p3">**</ept>ボタンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This configuration is needed by many LCS tools, if you have already configured LCS to connect to your Azure DevOps project, you can skip this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成は多くの LCS ツールで必要になります。すでに Azure DevOps プロジェクトに接続するように LCS を設定している場合は、このセクションをスキップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS VSTS setup<ept id="p1">](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS VSTS の設定<ept id="p1">](./media/lcs_vsts_setup.png)](./media/lcs_vsts_setup.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Enter the root URL for your Azure DevOps account and the access token created earlier, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps アカウントのルート URL および以前に作成したアクセス トークンを入力し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS token<ept id="p1">](./media/lcstoken.png)](./media/lcstoken.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS トークン<ept id="p1">](./media/lcstoken.png)](./media/lcstoken.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Select the project within your Azure DevOps account that you want to connect to, and select <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続する Azure DevOps アカウント内のプロジェクトを選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS select project<ept id="p1">](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS がプロジェクトを選択<ept id="p1">](./media/lcs_selectproject.png)](./media/lcs_selectproject.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>On the <bpt id="p1">**</bpt>Review and save<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>確認および保存<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Create an ax7.version file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ax7.version ファイルを作成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>If you are migrating from AX 2012, you can skip this step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 から移行する場合は、この手順を省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The code upgrade tile in LCS automatically finds the version of Finance and Operations that you are migrating from, by reading the ax7.version file under the Main folder in your source control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のコードのアップグレード タイルは、移行元の Finance and Operations のバージョンを自動的に検出します。ソース管理のメイン フォルダの ax7.version ファイルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>You must create this file manually, either in Visual Studio or through the Azure DevOps web portal, as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に示すように、Visual Studio または Azure DevOps Web ポータルを通じて、このファイルを手動で作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This file is not needed if you are migrating your code from Dynamics AX 2012 R3 or an earlier version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 R3 またはそれ以前のバージョンからコードを移行する場合、このファイルは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The version number entered here must be the application version (not the platform version).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここに入力するバージョン番号は、アプリケーションのバージョン (プラットフォームのバージョンではない) である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Take care to enter the correct version number here as entering an incorrect version number in this file may cause your code upgrade run to fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルに無効なバージョン番号を入力するとしてのコード アップグレードの実行に失敗する可能性があるため、ここには必ず正しいバージョン番号を入力してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ax7 version file<ept id="p1">](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ax7 バージョン ファイル<ept id="p1">](./media/ax7_versionfile.png)](./media/ax7_versionfile.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>For more information about how to identify which application version you have, see <bpt id="p1">[</bpt>Overview of Microsoft Dynamics AX build numbers<ept id="p1">](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのアプリケーション バージョンを持っているか識別する方法の詳細については、<bpt id="p1">[</bpt>Microsoft Dynamics AX ビルド番号の概要<ept id="p1">](https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Execute the code upgrade tile</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード タイルを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In your LCS project, select the <bpt id="p1">**</bpt>Code upgrade<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトで、<bpt id="p1">**</bpt>コードのアップグレード<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Code upgrade tile<ept id="p1">](./media/codeupgradetile.png)](./media/codeupgradetile.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コード アップグレード タイル<ept id="p1">](./media/codeupgradetile.png)](./media/codeupgradetile.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In the bottom left corner of the screen, click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and then enter a name and description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面の左下隅で、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックしてから名前と説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Select the version you are upgrading from as Microsoft Dynamics AX 7, and then click <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード元のバージョンとして Microsoft Dynamics AX 7 を選択し、<bpt id="p1">**</bpt>作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If you are upgrading your code from Dynamics AX 2012 R3, select the version you are upgrading from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 R3 からコードをアップグレードする場合は、アップグレード元のバージョンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>You will be prompted to upload a zipped version of your Dynamics AX 2012 R3 model store file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">圧縮バージョンの Dynamics AX 2012 R3 モデル ストア ファイルをアップロードするように要求されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>If the <bpt id="p1">**</bpt>Estimation Only<ept id="p1">**</ept> check box is selected, the tool only generates a report and does not check in or create a new code branch in Azure DevOps for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>見積のみ<ept id="p1">**</ept>チェック ボックスがオンになっている場合、ツールはレポートのみを生成し、チェックインや Azure DevOps の新しいコード分岐の作成を行いません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>You should use this option if you want to evaluate the potential size of the work involved in upgrading before you commit to the actual upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際のアップグレードをコミットする前に、アップグレードに必要な作業の潜在的なサイズを評価する場合、このオプションを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>New code branch<ept id="p1">](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新規コード ブランチ<ept id="p1">](./media/codeupgrade_new.png)](./media/codeupgrade_new.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Click <bpt id="p1">**</bpt>Analyze code<ept id="p1">**</ept> in the bottom right corner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右下にある<bpt id="p1">**</bpt>コードの分析<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The code upgrade process will start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのアップグレード プロセスが開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>This typically takes 40 minutes for a large solution to complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、大規模なソリューションが完了するまでに通常 40 分かかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>When complete, return to the <bpt id="p1">**</bpt>Code upgrade<ept id="p1">**</ept> tile in LCS to view the results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、LCS の <bpt id="p1">**</bpt>コードのアップグレード<ept id="p1">**</ept> タイルに戻り、結果を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The code upgrade service creates a new branch and checks in the upgraded code to your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのアップグレード サービスは、新しいブランチを作成し、アップグレードされたコードを Azure DevOps プロジェクトにチェックインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>After the upgrade process is complete, your code will exist in a new branch under the <bpt id="p1">**</bpt>Releases<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード プロセスが完了した後、コードは<bpt id="p1">**</bpt>リリース<ept id="p1">**</ept>フォルダ下の新しいブランチに存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The branch name is suffixed with the date and time of the upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分岐名の後には、アップグレードの日時が付いています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Code upgrade branch<ept id="p1">](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コード アップグレード ブランチ<ept id="p1">](./media/codeupgradebranch-300x192.png)](./media/codeupgradebranch.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Merge Releases back into Trunk<ph id="ph1">\\</ph>Main</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリースを Trunk<ph id="ph1">\\</ph>Main にマージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Once the upgraded code in Releases<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>version number<ph id="ph3">\&gt;</ph> compiles sucessfully and you have completed your code migration and testing, you are ready to merge this branch back into Trunk<ph id="ph4">\\</ph>Main.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリース<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>バージョン番号<ph id="ph3">\&gt;</ph>のアップグレードされたコードが正常にコンパイルされ、コード移行とテストを完了したら、このブランチをトランク<ph id="ph4">\\</ph>メインにマージする準備が整いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>To do this, on your development environment in Visual Studio open the Source control explorer pane then right-click on the <bpt id="p1">**</bpt>Releases<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>version number<ph id="ph3">\&gt;</ph><ept id="p1">**</ept> branch and in the context menu go to <bpt id="p2">**</bpt>Branching and Merging<ept id="p2">**</ept> and then on the sub-menu select <bpt id="p3">**</bpt>Merge<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、Visual Studio の開発環境で、ソース管理エクスプローラー ウィンドウを開き、<bpt id="p1">**</bpt>リリース<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>バージョン番号<ph id="ph3">\&gt;</ph><ept id="p1">**</ept>分岐を右クリックし、コンテキスト メニューで<bpt id="p2">**</bpt>分岐とマージ<ept id="p2">**</ept>に進み、サブ メニューで<bpt id="p3">**</bpt>マージ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Merge release branch<ept id="p1">](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>リリース ブランチのマージ<ept id="p1">](./media/MergeReleasesBranch.PNG)](./media/MergeReleasesBranch.PNG)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This will open the <bpt id="p1">[</bpt>Source Control Merge Wizard<ept id="p1">](https://www.visualstudio.com/en-us/docs/tfvc/merge-folders-files#sourcecontrolwizard)</ept> which will guide you through merging the Releases<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>version number<ph id="ph3">\&gt;</ph> branch back into Trunk<ph id="ph4">\\</ph>Main.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、[<bpt id="p1">[</bpt>ソース管理マージ ウィザード<ept id="p1">](https://www.visualstudio.com/en-us/docs/tfvc/merge-folders-files#sourcecontrolwizard)</ept>] が開きます。これは、リリース<ph id="ph1">\\</ph><ph id="ph2">\&lt;</ph>のバージョン番号<ph id="ph3">\&gt;</ph>のブランチをトランク<ph id="ph4">\\</ph>メインにマージする手順を案内します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>