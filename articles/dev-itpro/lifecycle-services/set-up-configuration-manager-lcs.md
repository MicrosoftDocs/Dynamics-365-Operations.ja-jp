<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-configuration-manager-lcs.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-configuration-manager-lcs.809007.360511d7485046ae14748f22c2d4eeb026273b35.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>360511d7485046ae14748f22c2d4eeb026273b35</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\set-up-configuration-manager-lcs.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up Configuration manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to set up the Configuration manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、構成マネージャーの設定方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up Configuration manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This feature is <bpt id="p1">**</bpt>not<ept id="p1">**</ept> supported for production use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、運用上の用途ではサポートされて<bpt id="p1">**</bpt>いません<ept id="p1">**</ept>。 </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Configuration manager (beta) relies on entities from the Data Import/Export Framework in your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Before you begin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Before you begin, your environment must include the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、環境には次のコンポーネントが含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A running version of AX 2012 R3 that has been configured for your business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務に合わせてコンフィギュレーションされた実行中の AX 2012 R3 のバージョン。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For more information about how to install AX 2012 R3, see <bpt id="p1">[</bpt>Install Microsoft Dynamics AX 2012<ept id="p1">](https://technet.microsoft.com/library/fbe52b68-1294-4398-b233-f8ec37c6d531(AX.60).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のインストール方法の詳細については、<bpt id="p1">[</bpt>Microsoft Dynamics AX 2012 のインストール<ept id="p1">](https://technet.microsoft.com/library/fbe52b68-1294-4398-b233-f8ec37c6d531(AX.60).aspx)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A running instance of the Data Import/Export Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行中のデータのインポート/エクスポート フレームワークのインスタンス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For more information about how to install the Data Import/Export Framework, see <bpt id="p1">[</bpt>Install the Data import/export framework (AX 2012)<ept id="p1">](./ax-2012/install-dixf.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワークをインストールする方法の詳細については、<bpt id="p1">[</bpt>データのインポート/エクスポート フレームワークをインストール (AX 2012)<ept id="p1">](./ax-2012/install-dixf.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>You must deploy the DMFEntityExecutionStatusService and DMFService service groups to enable to Configuration manager (beta) to connect to Data Import/Export Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワークへ接続するためには、構成マネージャー (ベータ) を有効にする DMFEntityExecutionStatusService および DMFService サービス グループを配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>An AX 2012 R3 project in Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services の AX 2012 R3 プロジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Copying configurations between environments can be a destructive operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境間でコンフィギュレーションをコピーすることは破壊的な操作になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>All project owners have the right to configure and perform these operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのプロジェクト所有者は構成およびこれらの操作を実行する権限を持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make sure that only trusted individuals are set as project owners.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">信頼されたユーザーのみがプロジェクト所有者として設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Create Data Import/Export Framework source data formats in AX 2012 R3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 でのデータのインポート/エクスポート フレームワーク ソース データ形式の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You must create both a Dynamics AX and a CSV source data format to manage configurations in all environments where you intend to export and import configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をエクスポートおよびインポートするすべての環境で構成を管理するには、Dynamics AX と CSV ソース データ形式の両方を作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create an AX source data format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX ソース データ フォーマットを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Complete the following procedure in the environment that you intend to export a configuration from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をエクスポートする環境で、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Click <bpt id="p1">**</bpt>Data import export framework<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Source data formats<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データのインポート/エクスポート フレームワーク<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ソース データ形式<ept id="p3">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>, and name the source AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>をクリックし、ソース AX の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Verify that the type is <bpt id="p1">**</bpt>AX.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイプが <bpt id="p1">**</bpt>AX<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Repeat this procedure in the environment that you intend to import the configuration to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成のインポート先の環境で、この手順を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a CSV source data format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSV ソース データ フォーマットを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Complete the following procedure in the environment that you intend to export a configuration from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をエクスポートする環境で、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Click <bpt id="p1">**</bpt>Data import export framework<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Source data formats<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データのインポート/エクスポート フレームワーク<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ソース データ形式<ept id="p3">**</ept>とクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>, and name the source CSV.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>をクリックし、ソース CSV の名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Verify that the type is <bpt id="p1">**</bpt>File<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイプが <bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>On the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab, set the following values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一般<ept id="p1">**</ept>タブで、次の値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Setting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">&lt;strong&gt;</bpt>File format<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ファイル形式<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Delimited</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">区切り</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">&lt;strong&gt;</bpt>First row header<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>先頭行のヘッダー<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Selected</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択済</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Row delimiter<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>行区切り<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>{CR}{LF}</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">{CR}{LF}</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Column delimiter<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>列区切り<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Vertical bar {</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">縦棒 {</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Text qualifier<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>テキスト修飾子<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Skip row<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>行をスキップ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Code page<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>コード ページ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>1252</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1252</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Language locale<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>言語ロケール<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>EN-US</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EN-US</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Multiple value separator<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>複数値の区切り<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>;</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">;</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>DIXF settings for Configuration manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーの DIXF 設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Repeat this procedure in the environment that you intend to import the configuration to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成のインポート先の環境で、この手順を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Install and configure the local component of the System diagnostics (Lifecycle Services)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断 (Lifecycle Services) のローカル コンポーネントのインストールと構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Complete the following procedure in the environment that you intend to export a configuration from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成をエクスポートする環境で、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you have already installed the local component of the System diagnostics for your project and environment, you must uninstall it by using <bpt id="p1">**</bpt>Add/Remove programs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトおよび環境のシステム診断のローカル コンポーネントを既にインストールしている場合、<bpt id="p1">**</bpt>プログラムの追加と削除<ept id="p1">**</ept>を使用し、アンインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Only one instance of Microsoft Dynamics AX Application Object Server (AOS) per environment can be used with Configuration management, regardless of the number of instances that are discovered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検出されたインスタンスの数にかかわらず、環境ごとに 1 つの Microsoft Dynamics AX Application Object Server (AOS) だけが、コンフィギュレーションの管理と共に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Install the local component of the System diagnostics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断のローカル コンポーネントをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For details, see <bpt id="p1">[</bpt>Install and run System diagnostics (Lifecycle Services)<ept id="p1">](./ax-2012/install-run-system-diagnostics-lcs.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>システム診断のインストールと実行 (Lifecycle Services)<ept id="p1">](./ax-2012/install-run-system-diagnostics-lcs.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Important: For this beta release, we require that you add the service account for the System diagnostics to the sysadmin role in AX 2012 R3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要: この beta リリースでは、システム診断のサービス アカウントを AX 2012 R3 の sysadmin ロールに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Click <bpt id="p1">**</bpt>Start<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Microsoft Dynamics AX Lifecycle Services Diagnostic Service Discovery<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Microsoft Dynamics AX Lifecycle Services 診断サービス検索の順にクリックします<ept id="p2">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the <bpt id="p1">**</bpt>Environment Discovery<ept id="p1">**</ept> window, enter a name for the environment, and the fully-qualified name of the Microsoft SQL Server instance and database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境の検出<ept id="p1">**</ept>ウィンドウに、環境の名前と Microsoft SQL Server のインスタンスとデータベースの完全修飾名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Then click Discover environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、[環境を検出] をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>After discovery is completed, enter the values in the <bpt id="p1">**</bpt>Configuration management (Beta)<ept id="p1">**</ept> section, click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Upload environment<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">探索を完了した後、<bpt id="p1">**</bpt>コンフィギュレーション管理 (ベータ)<ept id="p1">**</ept> セクションに値を入力し、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックして、<bpt id="p3">**</bpt>アップロード環境<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先頭値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">&lt;span class="ui"&gt;</bpt>Enable configuration overwrites<ept id="p1">&lt;/span&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;span class="ui"&gt;</bpt>コンフィギュレーションの上書きを有効にする<ept id="p1">&lt;/span&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Select this option to enable configurations to be copied and overwritten for the specified AOS instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">指定した AOS インスタンスのコンフィギュレーションをコピーし、上書きできるようにするには、このオプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Important:<ept id="p1">&lt;/strong&gt;</ept> We strongly recommend that you disable configuration overwrites when you have fully configured an environment.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;strong&gt;</bpt>重要:<ept id="p1">&lt;/strong&gt;</ept> 環境の設定が完了した際に、環境設定の上書きを無効にすることを強くお勧めします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">&lt;span class="ui"&gt;</bpt>AOS instance<ept id="p1">&lt;/span&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;span class="ui"&gt;</bpt>AOS インスタンス<ept id="p1">&lt;/span&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Specify the AOS instance that can be copied from or overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーまたは上書きが可能な AOS インスタンスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">&lt;span class="ui"&gt;</bpt>Storage location<ept id="p1">&lt;/span&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;span class="ui"&gt;</bpt>保存場所<ept id="p1">&lt;/span&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Specify the location where configurations are stored locally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成のローカルの格納場所を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The AOS service account and the Data Import/Export Framework service account must have read and write access to this location.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">AOS サービス アカウントとデータのインポート/エクスポート フレームワーク サービス アカウントには、この場所への書き込みアクセス権が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Important:<ept id="p1">&lt;/strong&gt;</ept> We strongly recommend that you use the same directory that is used for the Data Import/Export Framework.Be aware that the shared directory might contain sensitive data, depending on what you are importing and exporting.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;strong&gt;</bpt>重要:<ept id="p1">&lt;/strong&gt;</ept> データ インポート/エクスポート フレームワークに使用されているものと同じディレクトリを使用することを強く推奨します。インポートおよびエクスポートの内容によっては、共有ディレクトリに機密データが含まれていることがありますので注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Make sure that as few users as possible, in addition to the AOS service account and the Data Import/Export Framework service account, have access to the location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出来る限りの少数のユーザーが、AOS サービス アカウントおよびデータのインポート / エクスポート フレームワーク サービス アカウントに加えて、その場所にアクセスできることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>System diagnostic discovery for Config manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成マネージャーのシステム診断の検出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Repeat this procedure in the environment that you intend to import a configuration to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成のインポート先の環境で、この手順を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The environment is now ready for you to copy and manage configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境は、設定をコピーして管理するための準備が整いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>For more information, see <bpt id="p1">[</bpt>Copy a configuration (Lifecycle Services, LCS)<ept id="p1">](copy-configuration-lcs.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>コンフィギュレーションのコピー (Lifecycle Services、LCS)<ept id="p1">](copy-configuration-lcs.md)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>