<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-sdk-packaging.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-sdk-packaging.bcd1d1.544c3c42ce542fef345da0f959b082aeaa74857e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>544c3c42ce542fef345da0f959b082aeaa74857e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-sdk\retail-sdk-packaging.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create retail deployable packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能小売パッケージの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to create a retail deployable package for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の配置可能小売パッケージを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create retail deployable packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能な小売パッケージの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to create a Retail deployable package (which is a package that contain all the extensions) for the following Retail components and deploy the package to your environment by using Microsoft Dynamics Lifecycle Services (LCS):</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、次の小売コンポーネントに展開可能な小売パッケージ (すべての拡張機能を含む) の作成し、 Microsoft Dynamics Lifecycle Services (LCS) を使用して、このパッケージをご利用の環境に展開する方法を解説します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Commerce runtime (CRT)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Retail proxy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail プロキシ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Hardware station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hardware Station</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Channel database scripts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース スクリプト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Payment connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Hybrid app (IOS and Android POS app)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハイブリッド アプリ (IOS および Android POS アプリ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Retail deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能 Retail パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A retail deployable package is one combined package that contains all your customizations together with all the metadata that is required for deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売可能なパッケージは、配置に必要なすべてのメタデータと共に、すべてのカスタマイズを含む 1 つの結合されたパッケージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can use this retail deployable package to deploy your customizations to various environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この小売展開可能パッケージを使用して、カスタマイズをさまざまな環境に展開できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You can do the deployment by using the automated flow in LCS, or you can do it manually by using the scripts that are provided inside the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で自動フローを使用して、配置を行うことができます。またはパッケージ内に用意されているスクリプトを使用して手動で行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This topic guides you through the process of generating the retail deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、配置可能小売パッケージを生成するプロセスを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>All customizations for the Retail components are packaged as a single retail deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail コンポーネントのすべてのカスタマイズは、1 つの配置可能なパッケージとして提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Finance and Operations doesn't support separate packages for individual Retail components, such as Modern POS, Cloud POS, Retail Store Scale Unit, CRT, and Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、Modern POS、Cloud POS、Retail Store Scale Unit、CRT、Retail Server といった、個々の Retail コンポーネントの個別のパッケージをサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>You must package all extensions as a single retail deployable package, even if you must merge or combine extensions from independent software vendors (ISVs) or various partners.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">独立したソフトウェア ベンダー (ISV) またはさまざまなパートナーの拡張機能をマージまたは結合する必要がある場合でも、すべての拡張機能を単一の小売展開可能パッケージとしてパッケージする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If your customizations were built and packaged as individual Retail component packages by using a version of the Retail software development kit (SDK) that is older than application version 7.1.1541.3036, the packages are no longer supported for deployment in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション バージョン 7.1.1541.3036 よりも古い Retail ソフトウェア開発キット (SDK) のバージョンを使用して、カスタマイズが個々の Retail コンポーネント パッケージとして構築されパッケージ化された場合、パッケージは LCS の展開に対してサポートされなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>You must uptake the hotfix in <bpt id="p1">[</bpt>KB 4015062<ept id="p1">](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download)</ept>, and then rebuild and repackage your customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>KB 4015062<ept id="p1">](https://fix.lcs.dynamics.com/Home/Index/0/kb/4015062?permission=Download)</ept> で修正プログラムを取得する必要があります。その際、カスタマイズはリビルドおよび再梱包されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For detailed information about the Retail SDK, see <bpt id="p1">[</bpt>Retail SDK overview<ept id="p1">](retail-sdk-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の詳細情報は、<bpt id="p1">[</bpt>Retail SDK 概要<ept id="p1">](retail-sdk-overview.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Steps to create a retail deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売展開可能パッケージを作成する手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>There are two ways to generate a retail deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売展開可能パッケージを生成するには、2 つの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You can use the Retail build automation, or you can generate the package manually by using the build tools in the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail ビルドの自動化を使用することができます。または Retail SDK のビルド ツールを使用し、手動でパッケージを生成することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>This topic focuses on the manual method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、手動メソッドを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Customize or add functionality to the Retail stack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売スタックに機能をカスタマイズまたは追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Use the build tools to identify the customized installation package, code-sign it, and specify the customized CRT, Retail Server, and Hardware station assemblies, and customized database scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド ツールを使用して、カスタマイズされたインストール パッケージを識別して、コードサインし、カスタマイズされた CRT、Retail サーバー、ハードウェア ステーション アセンブリ、カスタマイズされたデータベース スクリプトを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>After all the settings have been specified in the <bpt id="p1">**</bpt>Customization.settings<ept id="p1">**</ept> file in the <bpt id="p2">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>BuildTools<ept id="p2">**</ept> folder, run <bpt id="p3">**</bpt>msbuild /t:rebuild<ept id="p3">**</ept> on the root of the Retail SDK folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての設定が <bpt id="p2">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>BuildTools<ept id="p2">**</ept> フォルダーの <bpt id="p1">**</bpt>Customization.settings<ept id="p1">**</ept> ファイルで指定された後、Retail SDK フォルダーのルートで <bpt id="p3">**</bpt>msbuild /t:rebuild<ept id="p3">**</ept> を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You can use either the MSBuild build tool or the Microsoft Visual Studio developer command-line tool to generate the retail deployable packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能小売パッケージを生成するために、MSBuild ビルド ツールまたは Microsoft Visual Studio 開発者コマンド ライン ツールのいずれかを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Before you build the package, put all the customized assemblies in the <bpt id="p1">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>References<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを作成する前に、すべてのカスタマイズされたアセンブリを、<bpt id="p1">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>References<ept id="p1">**</ept> フォルダに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Additionally, put the modified configuration files, such as <bpt id="p1">**</bpt>CommerceRuntime.Ext.config<ept id="p1">**</ept>, <bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p2">**</ept>, <bpt id="p3">**</bpt>HardwareStation.Extension.config<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p4">**</ept>, in the <bpt id="p5">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>Assets<ept id="p5">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、<bpt id="p5">**</bpt>...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>Assets<ept id="p5">**</ept> フォルダーの <bpt id="p1">**</bpt>CommerceRuntime.Ext.config<ept id="p1">**</ept>、<bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p2">**</ept>、 <bpt id="p3">**</bpt>HardwareStation.Extension.config<ept id="p3">**</ept>、および <bpt id="p4">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p4">**</ept> のような変更済の構成ファイルを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Retail SDK build tools – Customization settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK ビルド ツール: カスタマイズ設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Most of the configuration values that the Retail SDK uses to build and package customizations are set in the BuildTools<ph id="ph1">\\</ph>Customization.setting files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズを構築しパッケージ化するために Retail SDK が使用するコンフィギュレーション値のほとんどが BuildTools<ph id="ph1">\\</ph>Customization.setting files で設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>These values define metadata that controls how binaries, components, and packages are named, versioned, and code-signed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの値は、バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御するメタデータを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>After you define this metadata, the Retail SDK build system uses it to identify the customization assets and package them for all the Retail components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメタデータを定義した後、Retail SDK ビルド システムはカスタマイズ資産を識別し、すべての Retail コンポーネントのためにカスタマイズ資産をパッケージ化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The following configuration settings are available in the Customization.settings file:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコンフィギュレーション設定は、 Customization.settings ファイルで使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>AssemblyNamePrefix<ept id="p1">**</ept> – Specify the prefix name for the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AssemblyNamePrefix<ept id="p1">**</ept> - アセンブリの接頭語名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>When you build the Retail SDK, all the assemblies are prefixed with this name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK を作成するときは、すべてのアセンブリに接頭辞としてこの名前が付きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>CustomAssemblyVersion<ept id="p1">**</ept> – Specify the custom assembly version for all assemblies that are built by using the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomAssemblyVersion<ept id="p1">**</ept> - Retail SDK を使用して作成されたすべてのアセンブリのカスタム アセンブリ バージョンを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>CustomVersion<ept id="p1">**</ept> – Specify the custom file version for all assemblies that are built by using the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomVersion<ept id="p1">**</ept> - Retail SDK を使用して作成されたすべてのアセンブリのカスタム ファイル バージョンを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>CustomName<ept id="p1">**</ept> – Specify the custom name for the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomName<ept id="p1">**</ept> - アセンブリのカスタム名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>CustomDescription<ept id="p1">**</ept> – Specify the description for the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomDescription<ept id="p1">**</ept> - アセンブリの説明を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>CustomPublisher<ept id="p1">**</ept> – Specify the publisher for the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomPublisher<ept id="p1">**</ept> – アセンブリの発行元を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>CustomPublisherDisplayName<ept id="p1">**</ept> – Specify the copyright for the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomPublisherDisplayName<ept id="p1">**</ept> - アセンブリの著作権を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>SignAssembly<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>True<ept id="p2">**</ept> to sign the assembly during the build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SignAssembly<ept id="p1">**</ept> – ビルド時にアセンブリに署名するには<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>を指定してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">**</bpt>DelaySign<ept id="p1">**</ept> – Specify <bpt id="p2">**</bpt>True<ept id="p2">**</ept> to delay signing of the assets during the build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DelaySign<ept id="p1">**</ept> – ビルド中にアセットの署名を延期するには <bpt id="p2">**</bpt>True<ept id="p2">**</ept> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>AssemblyOriginatorKeyFile<ept id="p1">**</ept> – Specify the strong name key to use to sign the assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AssemblyOriginatorKeyFile<ept id="p1">**</ept> - アセンブリに署名するために使用する厳密な名前キーを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>ModernPOSPackageCertificateKeyFile<ept id="p1">**</ept> – Specify the Personal Information Exchange (PFX) file to use to sign Modern POS and Hardware station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModernPOSPackageCertificateKeyFile<ept id="p1">**</ept> – Modern POS とハードウェア ステーションの署名に使用する個人情報交換 (PFX) ファイルを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>RetailServerLibraryPathForProxyGeneration<ept id="p1">**</ept> – Specify the customized Retail Server assembly to use for proxy generation (both TypeScript and C<ph id="ph1">\#</ph> proxies).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailServerLibraryPathForProxyGeneration<ept id="p1">**</ept> – プロキシの生成に使用するカスタマイズされたRetail サーバー アセンブリを指定します (TypeScript と C<ph id="ph1">\#</ph> プロキシの両方)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For 7.1 and earlier versions, you must specify the name of the Retail Server assembly here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.1 以前のバージョンでは、ここで Retail サーバー アセンブリの名前を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For 7.2 and later versions, use the commerce generator tool for proxy generation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">7.2 以降のバージョンでは、プロキシ生成の commerce ジェネレーター ツールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>However, if you're using the proxy on the e-commerce client side, specify the assembly name here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、E コマース クライアント側でプロキシを使用している場合は、ここでアセンブリ名を指定してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>ItemGroup<ept id="p1">**</ept> section includes the following settings:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ItemGroup<ept id="p1">**</ept> セクションには、次の設定が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>CommerceRuntime<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – Specify the details of all the customized CRT assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>CommerceRuntime<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – すべてのカスタマイズされた CRT アセンブリの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can have multiple entries, one for each CRT assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 CRT アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>RetailServer<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – Specify the details of all the customized Retail Server assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>RetailServer<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – カスタマイズされたすべての Retail サーバー アセンブリの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>You can have multiple entries, one for each Retail Server assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 Retail サーバー アセンブリに対して 1 つの、複数のエントリを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>RetailProxy<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – Specify the details of all the customized Retail proxy assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>RetailProxy<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – カスタマイズされたすべての Retail プロキシ アセンブリの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can have multiple entries, one for each Retail proxy assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 Retail プロキシ アセンブリに対して 1 つの、複数のエントリを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>HardwareStation<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – Specify the details of all the customized Hardware station assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>HardwareStation<ph id="ph2">\_</ph>CustomizableFile<ept id="p1">**</ept> – カスタマイズされたすべてのハードウェア ステーション アセンブリの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>You can have multiple entries, one for each customized Hardware station assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズされた各ハードウェア ステーション アセンブリに対して 1 つずつ、複数のエントリを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>CustomDatabaseFile<ph id="ph2">\_</ph>Upgrade<ph id="ph3">\_</ph>Custom<ept id="p1">**</ept> – Specify the details of all the customized database scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ISV<ph id="ph1">\_</ph>CustomDatabaseFile<ph id="ph2">\_</ph>アップグレード<ph id="ph3">\_</ph>カスタム<ept id="p1">**</ept> – カスタマイズされたすべてのデータベース スクリプトの詳細を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Before you start the build process, you must put extension assemblies in ...<ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>References and custom database scripts under ...<ph id="ph3">\\</ph>RetailSDK<ph id="ph4">\\</ph>Database\Upgrade<ph id="ph5">\\</ph>Custom.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド プロセスを開始する前に、拡張アセンブリを <ph id="ph1">\\</ph>Retail SDK<ph id="ph2">\\</ph>References に、カスタム データベース スクリプトを <ph id="ph3">\\</ph>RetailSDK<ph id="ph4">\\</ph>Database\Upgrade<ph id="ph5">\\</ph>Custom に配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Database scripts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース スクリプト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Database scripts are packaged together with the Retail Server and Modern POS Offline packages, and are run when Retail Server and Modern POS are installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース スクリプトは、Retail サーバーおよび Modern POS オフライン パッケージとともにパッケージ化され、Retail Server および Modern POS がインストールされたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>If there are multiple custom database scripts, they are run in alphabetical order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のカスタム データベース スクリプトがある場合は、アルファベット順に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Therefore, to run the scripts in a specific order, you must name them accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、スクリプトを特定の順序で実行したい場合は、それに応じて名前を付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The CRT.RETAILUPGRADEHISTORY table tracks the scripts that are already applied to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT.RETAILUPGRADEHISTORY テーブルは、データベースに既に適用されているスクリプトを追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, the next package upgrade runs only the upgrade scripts that don't have an entry in the CRT.RETAILUPGRADEHISTORY table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、次のパッケージ アップグレードは、CRT.RETAILUPGRADEHISTORY テーブルに項目がないアップグレード スクリプトのみを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>For more details about Channel database extensions, see <bpt id="p1">[</bpt>Channel database extensions<ept id="p1">](../channel-db-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース拡張機能の詳細については、<bpt id="p1">[</bpt>チャネル データベース拡張機能<ept id="p1">](../channel-db-extensions.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Update the extension configuration files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の構成ファイルを更新します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>If you have any new extensions in CRT, Retail Server, Hardware station, or proxy, you should register the details of the extension assemblies in the <ph id="ph1">\&lt;</ph>composition<ph id="ph2">\&gt;</ph> section of the relevant extension configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT、Retail Server、ハードウェア ステーション、またはプロキシに新しい拡張機能がある場合は、関連する拡張構成ファイルの<ph id="ph1">\&lt;</ph>構成<ph id="ph2">\&gt;</ph>セクションに拡張アセンブリの詳細を登録する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can find all the extension configuration files in the ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Assets folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張設定ファイルは次で見つけることができます。<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>資産フォルダ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Because all extensions are loaded based on the information in the extension configuration files, you must register your assemblies there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての拡張機能は拡張ファイルの情報に基づいて読み込まれるため、アセンブリを登録する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Before you do the package, you must update the following configuration files if you have any customization in that area:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを行う前に、次の構成ファイルを更新する必要があります (この領域でカスタマイズがある場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>CommerceRuntime.Ext.config<ept id="p1">**</ept> – Register all your CRT extension assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CommerceRuntime.Ext.config<ept id="p1">**</ept> – すべての CRT 拡張アセンブリを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p1">**</ept> – Register all your CRT extensions for offline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p1">**</ept> – オフラインで、すべての CRT 拡張機能を登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> – Register all your Hardware station extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> – すべてのハードウェア ステーション拡張機能を登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p1">**</ept> – Register all your retail proxy extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailProxy.MPOSOffline.ext.config<ept id="p1">**</ept> – すべての小売プロキシ拡張機能を登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Retail Server extension assemblies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの拡張機能アセンブリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Before you start the package, you must add an entry for the Retail Server extension assemblies in the <ph id="ph1">\&lt;</ph>extensionComposition<ph id="ph2">\&gt;</ph> of the Retail Server web.config file, so that the assemblies are loaded and used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージを開始する前に、Retail Server web.config file の <ph id="ph1">\&lt;</ph>extensionComposition<ph id="ph2">\&gt;</ph> に、Retail Server 拡張アセンブリのエントリを追加する必要があります。これにより、アセンブリがロードされ、使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>You can find the web.config file in the Retail SDK<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>RetailServer<ph id="ph3">\\</ph>Code folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">web.config ファイルは、Retail SDK<ph id="ph1">\\</ph>パッケージ<ph id="ph2">\\</ph>RetailServer<ph id="ph3">\\</ph> コード フォルダーで検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>The following illustration shows an example of a Retail Server web.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、Retail サーバーの Web.config ファイルの例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Retail Server web.config file<ept id="p1">](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Retail サーバーの Web.config ファイル<ept id="p1">](./media/retail-server-web-config.png)](./media/retail-server-web-config.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You should not add or change any custom settings in the above mentioned example or in any of the channel config files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の例、またはチャネル構成ファイルのいずれかで、カスタム設定を追加したり変更したりしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The only supported modification is adding custom assemblies details in the composition section.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">対応している変更は、構成セクションでのカスタム アセンブリの詳細の追加のみです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Also, as part of your extension or package, do not edit any of the following config files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、拡張機能またはパッケージの一部として、構成ファイルのいずれも編集しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>These config files will be updated with the latest file from core Microsoft package during deployment and your changes will be lost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの構成ファイルは、配置の際にコア Microsoft パッケージの最新のファイルで更新され、変更内容は失われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>CommerceRuntime.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>dllhost.exe.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dllhost.exe.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>HardwareStation.Dedicated.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HardwareStation.Dedicated.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>HardwareStation.Shared.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HardwareStation.Shared.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>workflowFoundation.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">workflowFoundation.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Hardware station - Web.config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーション - Web.config</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Install NuGet.exe</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">NuGet.exe のインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Some of the dependency packages and references have moved to NuGet packages to minimize the file merge and the size of the SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの結合およびSDKのサイズを最小限に抑えるため、いくつかの依存関係パッケージおよび参照を NuGet パッケージに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>These are available for download from the NuGet.org. When you build the Retail SDK these dependencies are automatically pulled from the NuGet.org based on the packages.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは NuGet.org からダウンロードできます。Retail SDK を作成すると、これらの依存関係は自動的に packages.config ファイルに基づいて NuGet.org から収集されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>For this to work, you need to install the <bpt id="p1">[</bpt>NuGet command line interface<ept id="p1">](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)</ept> and add the nuget to the Windows path after downloading nuget.exe from NuGet.org. The following steps show how to add the nuget to the Windows path:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">このためには、「<bpt id="p1">[</bpt>NuGet コマンド ライン インターフェイス<ept id="p1">](https://docs.microsoft.com/nuget/tools/nuget-exe-cli-reference#installing-nugetexe)</ept>」をインストールし、 NuGet.org から nuget.exe をダウンロードした後、nuget を Windows パスに追加する必要があります。次の手順は、Windows パスに nuget を追加する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Open the Windows menu and type <bpt id="p1">**</bpt>Path<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Windows メニューを開き、 <bpt id="p1">**</bpt>Path<ept id="p1">**</ept>と入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>The <bpt id="p1">**</bpt>Edit the system environment variables<ept id="p1">**</ept> will be available.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム環境変数を編集<ept id="p1">**</ept>を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>In that menu, click <bpt id="p1">**</bpt>Environment variables<ept id="p1">**</ept> on the lower right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニューの右下の<bpt id="p1">**</bpt>環境変数<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>In the next window, under <bpt id="p1">**</bpt>System variables<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Path<ept id="p2">**</ept> and click <bpt id="p3">**</bpt>Edit<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のウィンドウで、<bpt id="p1">**</bpt>システム変数<ept id="p1">**</ept>の<bpt id="p2">**</bpt>パス<ept id="p2">**</ept>を選択し、<bpt id="p3">**</bpt>編集<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Add an entry for the folder where you would like to store the nuget.exe file or store the nuget.exe file in a folder that is already listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">nuget.exe ファイルを保存するフォルダーのエントリを追加するか、既に登録されているフォルダーに nuget.exe ファイルを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Generate a retail deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能小売パッケージを生成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>To generate the retail deployable package, open the MSBuild build Command Prompt window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能小売パッケージを生成するには、MSBuild ビルド コマンド プロンプト ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>(On the developer virtual machine, search for <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Start<ept id="p2">**</ept> menu.) Then run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(開発者仮想マシンの、<bpt id="p2">**</bpt>開始<ept id="p2">**</ept>メニューで <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> を検索します。) そして、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>You can also run the same command in the Microsoft Visual Studio 2015 developer command-line tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 開発者コマンド ライン ツールで同じコマンドを実行することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">梱包</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>After the build is completed, retail deployable packages are generated as a zip file (RetailDeployablePackage.zip) in the Retail SDK<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>RetailDeployablePackage folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルドが完了した後、Retail SDK<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>RetailDeployablePackage フォルダーに、配置可能小売パッケージ が zip ファイルとして (RetailDeployablePackage.zip) が生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>There won't be separate packages the various Retail components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな Retail コンポーネントを別々のパッケージにすることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>All the packages will be combined into one bundle package that is named RetailDeployablePackage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのパッケージは、RetailDeployablePackage という名の 1 つのバンドル パッケージに結合されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Deploy the retail deployable packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売展開可能パッケージを配置する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>For information about how to deploy the packages either manually or by using the automated flow in LCS, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../../../dev-itpro/deployment/apply-deployable-package-system.md)</ept> and <bpt id="p2">[</bpt>Install a deployable package<ept id="p2">](../../../dev-itpro/deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動または LCS 自動化フローを使用してパッケージを配置する方法については、<bpt id="p1">[</bpt>配置可能なパッケージを適用する<ept id="p1">](../../../dev-itpro/deployment/apply-deployable-package-system.md)</ept>および<bpt id="p2">[</bpt>配置可能なパッケージをインストールする<ept id="p2">](../../../dev-itpro/deployment/install-deployable-package.md)</ept>を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>