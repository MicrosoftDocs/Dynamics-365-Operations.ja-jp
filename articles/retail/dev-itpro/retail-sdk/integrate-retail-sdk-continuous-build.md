<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="integrate-retail-sdk-continuous-build.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>integrate-retail-sdk-continuous-build.78d23e.7e6e5d0f37899269a4eb200e79074495238c4ba3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>7e6e5d0f37899269a4eb200e79074495238c4ba3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-sdk\integrate-retail-sdk-continuous-build.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Merge the build systems for Retail and Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail と Finance and Operations のビルド システムのマージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes the steps for merging the build systems for both Dynamics 365 for Finance and Operations, and Dynamics 365 for Retail using Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Azure DevOps を使用して Dynamics 365 for Finance and Operations および Dynamics 365 for Retail の両方のビルド システムをマージするためのステップを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Merge the build systems for Retail and Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail および Finance and Operations 用ビルド システムのマージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes the steps for merging the build systems for both Dynamics 365 for Finance and Operations, and Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Dynamics 365 for Finance and Operations および Dynamics 365 for Retail の両方のビルド システムをマージするためのステップを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The Lifecycle Services (LCS)-integrated build experience supports both code upgrades and new projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) に統合されたビルド エクスペリエンスは、コードのアップグレードと新しいプロジェクトの両方をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Retail SDK is a self-contained MSBuild-based build system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK は、自己完結型の MSBuild ベースのビルド システムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Many customizers want to make productive changes in both Microsoft Dynamics 365 for Finance and Operations and Retail components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くのカスタマイザーは、Microsoft Dynamics 365 for Finance and Operations および Retail の両方のコンポーネントに生産的な変更を加えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This article outlines the manual steps for merging both build systems using Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Azure DevOps を使用して両方のビルド システムをマージするための手動のステップを概説します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Enable the build system</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド システムの有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To get started, you must follow all the steps to get a full continuous build system up and running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始するには、すべてのステップを実行して、完全な連続ビルド システムを稼働させる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For information, see <bpt id="p1">[</bpt>Developer topology deployment with continuous build and test automation<ept id="p1">](../../../dev-itpro/perf-test/continuous-build-test-automation.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>継続的ビルドとテストの自動化を使用した開発者トポロジの展開<ept id="p1">](../../../dev-itpro/perf-test/continuous-build-test-automation.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>After deployment, you create the build definition and build steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置した後、ビルド定義とビルド ステップを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Build at least one time, so that you become familiar with it and are sure that you can build without errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それをよく理解してエラーなしでビルドできるように、少なくとも 1 回はビルドしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Then move to the next step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、次の手順に移ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Prepare the Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK を準備します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Getting the Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If you don't already have the Retail software development kit (SDK) in the same Microsoft Azure DevOps project, add it now.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Microsoft Azure DevOps プロジェクトで Retail ソフトウェア開発キット (SDK) がない場合は、ここで追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You will find the Retail SDK in any developer or build topology.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どの開発者トポロジまたはビルド トポロジでも、Retail SDK が存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Follow the branching documentation in <bpt id="p1">[</bpt>Retail SDK overview<ept id="p1">](retail-sdk-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail SDK の概要<ept id="p1">](retail-sdk-overview.md)</ept> の分岐ドキュメントに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>We recommend that you create your Retail SDK mirror and your Retail SDK customization branch at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で、Retail SDK ミラーと Retail SDK カスタマイズ分岐を作成することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>After your Retail SDK customization branch is ready, and it has been submitted in the same Azure DevOps project as Retail, you can start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK カスタマイズ分岐が準備できた後、Retail と同じ Azure DevOps プロジェクトで送信され開始できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Install NuGet.exe</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NuGet.exe のインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Some of the dependency packages and references have moved to NuGet packages to minimize the file merge and the size of the SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの結合およびSDKのサイズを最小限に抑えるため、いくつかの依存関係パッケージおよび参照を NuGet パッケージに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>These are available for download from the NuGet.org. When you build the Retail SDK these dependencies are automatically pulled from the NuGet.org based on the packages.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは NuGet.org からダウンロードできます。Retail SDK を作成すると、これらの依存関係は自動的に packages.config ファイルに基づいて NuGet.org から収集されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For this to work, you need to install the <bpt id="p1">[</bpt>NuGet command line interface<ept id="p1">](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)</ept> and add the nuget to the Windows path after downloading nuget.exe from NuGet.org. The following steps show how to add the nuget to the Windows path:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">このためには、「<bpt id="p1">[</bpt>NuGet コマンド ライン インターフェイス<ept id="p1">](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)</ept>」をインストールし、 NuGet.org から nuget.exe をダウンロードした後、nuget を Windows パスに追加する必要があります。次の手順は、Windows パスに nuget を追加する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Open the Windows menu and type <bpt id="p1">**</bpt>Path<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="98" state="translated" state-qualifier="leveraged-inherited">Windows メニューを開き、 <bpt id="p1">**</bpt>Path<ept id="p1">**</ept>と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The <bpt id="p1">**</bpt>Edit the system environment variables<ept id="p1">**</ept> will be available.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>システム環境変数を編集<ept id="p1">**</ept>を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In that menu, click <bpt id="p1">**</bpt>Environment variables<ept id="p1">**</ept> on the lower right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニューの右下の<bpt id="p1">**</bpt>環境変数<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>In the next window, under <bpt id="p1">**</bpt>System variables<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Path<ept id="p2">**</ept> and click <bpt id="p3">**</bpt>Edit<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のウィンドウで、<bpt id="p1">**</bpt>システム変数<ept id="p1">**</ept>の<bpt id="p2">**</bpt>パス<ept id="p2">**</ept>を選択し、<bpt id="p3">**</bpt>編集<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Add an entry for the folder where you would like to store the nuget.exe file or store the nuget.exe file in a folder that is already listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">nuget.exe ファイルを保存するフォルダーのエントリを追加するか、既に登録されているフォルダーに nuget.exe ファイルを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Add a repository mapping for the Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK のレポジトリ マッピングを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Edit the build definition so that it includes the location of the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の場所が含まれるように、ビルド定義を編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>(In other words, add a map.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">(言い換えれば、マップを追加します。)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Adding a repository mapping for the Retail SDK<ept id="p1">](./media/build-map-addition.png)](./media/build-map-addition.png)</ept></source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Retail SDK に対するレポジトリ マッピングの追加<ept id="p1">](./media/build-map-addition.png)](./media/build-map-addition.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Add a new build step to build the Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDKを構築するための新しいビルド ステップの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Add a new step at the beginning of the build pipeline, as shown in the following screen shot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリーン ショットに示すように、ビルド パイプラインの先頭に新しいステップを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Adding a new build step to build the Retail SDK<ept id="p1">](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>小売 SDK を構築するための新しいビルド ステップの追加<ept id="p1">](./media/new-build-step-1024x527.png)](./media/new-build-step.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Add a copy step for binaries from the Retail SDK to the Retail build</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Retail SDK から Retail ビルドへのバイナリのコピー ステップの追加</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>This build step enables Microsoft to copy the latest built Retail binaries to the Retail bin folder, if Microsoft shares files/binaries.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">このビルド ステップでは、Microsoft がファイル/バイナリを共有する場合、Microsoft は Retail bin フォルダに最新の構築済み Retail バイナリをコピーできます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Make sure that you complete this step immediately after you add a build step for the Retail SDK, as described in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションで説明したように、Retail SDK のビルド ステップを追加した直後にこのステップを完了することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Adding a copy step for binaries from the Retail SDK to the Dynamics 365 for Retail build<ept id="p1">](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Retail SDK から Dynamics 365 for Retail ビルドへのバイナリのコピー ステップの追加<ept id="p1">](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Add a copy step for all Retail packages</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">すべての Retail パッケージのコピー ステップの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Make sure that this step occurs after the "PowerShell: Generate packages" step (see image below).</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">このステップが "PowerShell: パッケージの生成" ステップ後に発生することを確認します (以下の図を参照してください)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Here are the arguments.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">その引数を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Adding a copy step for all Retail packages<ept id="p1">](./media/package-drop-1024x473.png)](./media/package-drop.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>すべての小売パッケージのコピー ステップの追加<ept id="p1">](./media/package-drop-1024x473.png)](./media/package-drop.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Optional: Referencing a Retail DLL from Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: Retail から Retail DLL を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You must complete this task only if you must add built Retail binaries to the Retail package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構築済み Retail バイナリを小売パッケージに追加する必要がある場合にのみ、このタスクを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, you must follow these three steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、これら 3 つの手順に従う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Use a normal AXReference in your Retail project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売プロジェクトでは通常の AXReference を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Add the corresponding AXReference folder and the XML file inside it to Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps に、対応する AXReference フォルダーとその中の XML ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Update the Copy-RetailBinaries.ps1 file with the appropriate file commands to get the binary file from the Retail SDK to the Retail bin folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Copy-RetailBinaries.ps1 ファイルを適切なファイル コマンドで更新し、バイナリ ファイルを Retail SDK から Retail bin フォルダーに取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The Microsoft Windows PowerShell file includes a sample that copies the PricingEngine.dll file into the ApplicationSuite bin folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows PowerShell ファイルには、ApplicationSuite bin フォルダーに PricingEngine.dll ファイルをコピーするサンプルが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Depending on the modules that you're building, the files and folders must be changed so that they are in a different location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドしているモジュールによっては、ファイルとフォルダーが異なる場所にあるように変更する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>