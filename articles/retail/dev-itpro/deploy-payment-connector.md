<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="deploy-payment-connector.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>deploy-payment-connector.04636e.9368f5e529594a23b05f83b8d2d59cb903c6b661.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9368f5e529594a23b05f83b8d2d59cb903c6b661</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\deploy-payment-connector.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Deploy payment connectors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタの配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to deploy a payment connector package to the appropriate components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、支払コネクタ パッケージを適切なコンポーネントに配置する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Deploy payment connectors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタの配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic guides retail IT professionals or value-added resellers (VARs) through the process of deploying a payment connector to the appropriate components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでガイドretail ITプロフェッショナルまたは支払コネクタを適切なコンポーネントに展開するプロセスを通じて付加価値再販業者 (Var)。このトピックでは、小売 IT プロフェッショナルまたは付加価値再販業者 (VARs) が支払コネクタを適切なコンポーネントに展開するプロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>We assume that the payment connector has been implemented and tested by the payment provider or the payment independent software vendor (ISV), and that it's ready for validation and subsequent production deployment in a customer environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタが支払プロバイダーまたは支払独立系ソフトウェア ベンダー (ISV) によって実装されてテスト済みであり、また顧客環境での検証とそれに続く実稼働配置の準備ができていると仮定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic doesn't include information about how to package a payment connector by using the Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックには、Retail ソフトウェア開発キット (SDK) を使用して支払コネクタをパッケージ化する方法に関する情報は含まれていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For information about how to download the SDK, see <bpt id="p1">[</bpt>Retail SDK overview<ept id="p1">](retail-sdk/retail-sdk-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SDK をダウンロードする方法については、<bpt id="p1">[</bpt>Retail SDK 概要<ept id="p1">](retail-sdk/retail-sdk-overview.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For guidelines about how to package a payment connector, see the Retail SDK packaging document in the downloaded SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタをパッケージ化する方法のガイドラインについては、ダウンロードした SDK の Retail SDK パッケージ ドキュメントを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This topic also doesn't include information about how to deploy the payment web application, payment front-end processor, or payment back-end processor, because those applications are managed by payment providers or payment ISVs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックには、支払 Web アプリケーション、支払フロントエンド プロセッサ、または支払バックエンド プロセッサの配置方法に関する情報も含まれています。それは、これらのアプリケーションが支払プロバイダーまたは支払 ISV によって管理されているためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If you're using Microsoft Dynamics AX 7.0 (February 2016), you must apply KB 3183058 before you create the Retail deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 7.0 (2016 年 2 月) を使用している場合は、配置可能小売パッケージを作成する前に KB 3183058 を適用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Payment packaging folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払パッケージ フォルダ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>A payment provider or a payment ISV creates a payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払プロバイダーまたは支払 ISV は、支払コネクタを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The payment connector will include some or all of the following folders:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクターには、次のフォルダーの一部または全部が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You can find these folders in ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>PaymentExternals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフォルダーは <ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>PaymentExternals で検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>IPaymentProcessor Assemblies<ept id="p1">**</ept> – This folder contains the assembly that implements the IPaymentProcessor interface, and its dependent assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPaymentProcessor Assemblies<ept id="p1">**</ept> – このフォルダーには、IPaymentProcessor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Payment Web Files<ept id="p1">**</ept> – This folder contains the callback HTML, JavaScript, or CSS files that are required in order to enable the payment accepting page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払 Web ファイル<ept id="p1">**</ept> – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML、JavaScript、または CSS ファイルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Payment connector developers will provide these web files if their payment accepting page requires them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払い受付ページで求められる場合、支払コネクタ開発者がこれらの Web ファイルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>IPaymentDevice Assemblies<ept id="p1">**</ept> – This folder contains the assembly that implements the IPaymentDevice interface and payment request handlers, and the interface's dependent assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPaymentDevice Assemblies<ept id="p1">**</ept> – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリと支払要求ハンドラー、およびインターフェイス依存アセンブリが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>These assemblies are used in Retail Hardware station and Retail Modern Point of Sale (Modern POS) to communicate with payment terminal devices, such as VeriFone MX925.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアセンブリは、VeriFone MX925 などの決済端末デバイスと通信するために、Retail ハードウェア ステーションおよび Retail Modern 販売時点管理 (Modern POS) で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If you don't have a payment terminal device, you don't need these files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払のターミナル デバイスがない場合は、これらのファイルは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>To package the payment connector files, the payment provider or payment ISV must copy the payment assemblies to the correct folder in ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>PaymentExternals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ ファイルをパッケージ化するには、支払プロバイダーまたは支払 ISV は <ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>PaymentExternals の正しいフォルダーへ支払アセンブリをコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>After the payment assemblies are copied, use <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> from the root of the Retail SDK folder to generate the deployable packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払アセンブリがコピーされた後、Retail SDK フォルダーのルートから <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> を使用し、配置可能なパッケージを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>After the <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> operation is completed, you can find the following deployable package in ...<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Packages<ph id="ph3">\\</ph>RetailDeployablePackage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MsBuild<ept id="p1">**</ept> 工程が完了後、<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>パッケージ<ph id="ph3">\\</ph>RetailDeployablePackage で以下の配置可能パッケージを検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In versions that are earlier than AX 7.0, the deployable package will be in <ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Packages<ph id="ph3">\\</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 7.0 より前のバージョンでは、配置可能パッケージは <ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Packages<ph id="ph3">\\</ph> になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Application Object Server (AOS) payment package<ept id="p1">**</ept> – <bpt id="p2">***</bpt>The AOS payment package is obsolete and is no longer supported. If you upload the AOS payment package to Microsoft Dynamics Lifecycle Service (LCS), you will receive an unsupported package error. Use the new Retail deployable package instead.<ept id="p2">***</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Application Object Server (AOS) 支払パッケージ<ept id="p1">**</ept> – <bpt id="p2">***</bpt>AOS 支払パッケージは廃止され、サポートされなくなりました。AOS 支払パッケージを Microsoft Dynamics Lifecycle Service (LCS) にアップロードする場合、サポートされていないパッケージのエラーが表示されます。代わりに新しい配置可能小売パッケージを使用してください。<ept id="p2">***</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If you're using AX 7.0, apply the latest binary hotfix before you generate the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 7.0 を使用している場合は、パッケージを生成する前に最新のバイナリ修正プログラムを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In newer versions, we won't generate an AOS payment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいバージョンでは、AOS 支払パッケージは生成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Retail deployable package<ept id="p1">**</ept> – This package includes payment plus all the other channel components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配置可能小売パッケージ<ept id="p1">**</ept> – このパッケージには、支払とその他のすべてのチャネル コンポーネントが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This package is this combined package for all retail extension components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパッケージは、すべての小売拡張子コンポーネントの結合されたパッケージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Before you start, you must have these items:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、次の品目が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Payment connector files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Retail deployable packages that are built by using the Retail SDK (see the list earlier in this topic)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK を使用して作成された小売展開可能パッケージ (このトピックの前のリストを参照)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Access to your cloud-hosted environment on LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS のクラウド ホスト環境にアクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Retail deployable packages (automated deployment)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売配置可能パッケージ (自動展開)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A Retail deployable package is an asset that can be consumed by the LCS deployment service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail デプロイ可能なパッケージは、LCS デプロイメント サービスで利用可能なアセットです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>When you package a payment connector and other extensions as a deployable package, you can either install the payment connector as a customization to an existing solution or slipstream it as part of a new deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタおよびその他の拡張機能を配置可能なパッケージとして作成するときは、支払コネクタを既存のソリューションにカスタマイズとしていずれかをインストール、または新しい配置の一部としてスリップ ストリームすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The following types of packages can contain payment connectors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のタイプのパッケージには、支払コネクタが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>AOSPaymentPackage<ept id="p1">**</ept> – This type of package deploys one or more payment connectors to AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOSPaymentPackage<ept id="p1">**</ept> - このタイプのパッケージは、AOS に 1 つ以上の支払コネクタを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>(<bpt id="p1">**</bpt>The AOS payment package is obsolete and is no longer supported.<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>AOS 支払パッケージは廃止され、サポートされなくなりました。<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>RetailDeployablePackage<ept id="p1">**</ept> – This type of package deploys one or more payment connectors to the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailDeployablePackage<ept id="p1">**</ept> – このタイプのパッケージは、以下のコンポーネントに 1 つまたは複数の支払いコネクタを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Retail Server, Commerce runtime, and database scripts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー、<ph id="1">Commerce Runtime</ph>、およびデータベース スクリプト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Self-service installer, which enables installation of the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のインストールを可能にするセルフ サービス インストーラー:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Hardware station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Upload and deploy deployable packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開可能なパッケージのアップロードと展開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Open your LCS project page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクト ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In the <bpt id="p1">**</bpt>More tools<ept id="p1">**</ept> section, click <bpt id="p2">**</bpt>Asset library<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加ツール<ept id="p1">**</ept> セクションで、<bpt id="p2">**</bpt>アセット ライブラリ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Select <bpt id="p1">**</bpt>Software package<ept id="p1">**</ept>, and then click the plus sign (<bpt id="p2">**</bpt><ph id="ph1">+</ph><ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソフトウェア パッケージ<ept id="p1">**</ept> を選択し、プラス記号をクリックします (<bpt id="p2">**</bpt><ph id="ph1">+</ph><ept id="p2">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Enter a name and description, and select the correct package type, as described in the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前と説明を入力し、次の表に示すように、適切なパッケージ タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Deployable package type in LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の配置可能パッケージ タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>AOSPaymentPackage (<bpt id="p1">**</bpt>Not supported<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOSPaymentPackage (<bpt id="p1">**</bpt>サポートされていない<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Binary hotfix</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ修正プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>RetailDeployablePackage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailDeployablePackage</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Combined retail package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結合された小売パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Click <bpt id="p1">**</bpt>Upload<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アップロード<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Select the zipped package, upload it, and then click <bpt id="p1">**</bpt>Confirm<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">圧縮済みのパッケージを選択してアップロードし、<bpt id="p1">**</bpt>確定<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>After you've uploaded your deployable packages to the LCS asset library, you can deploy them to your environments through the LCS portal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージを LCS 資産ライブラリにアップロードした後、LCS ポータルを通じて環境に配置することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>After you've validated your deployment in your sandbox environment, you can create a service request to deploy it to your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境内の配置を検証した後は、実稼働環境を配置するサービス要求を作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For more information, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../../dev-itpro/deployment/apply-deployable-package-system.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>配置可能パッケージの適用<ept id="p1">](../../dev-itpro/deployment/apply-deployable-package-system.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Download and run installers on client computers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンピューターでインストーラーをダウンロードして実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The self-service package contains the installers for both Hardware station and Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セルフサービス パッケージには、ハードウェア ステーションと Modern POS の両方のインストーラーが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>After your deployable packages have been applied to your environment, you can download the updated Hardware station and Modern POS installers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージが環境に適用された後、更新されたハードウェア ステーションと Modern POS インストーラーをダウンロードすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For information about how to download Hardware station and Modern POS, and install them on client computers, see <bpt id="p1">[</bpt>Retail Modern POS configuration and installation<ept id="p1">](../retail-modern-pos-device-activation.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションおよび Modern POS をダウンロードし、クライアント コンピューターにインストールする方法については、<bpt id="p1">[</bpt>Retail Modern POS のコンフィギュレーションとインストール<ept id="p1">](../retail-modern-pos-device-activation.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Manual deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動での配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>This section describes how to manually deploy a payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、支払コネクタを手動で展開する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use a manual deployment to test locally in a developer environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動による展開を使用して、開発環境でローカルにテストすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This developer environment can be either cloud-hosted or on a downloadable virtual hard disk (VHD).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この開発環境は、クラウドホスト型でも、ダウンロード可能な仮想ハード ディスク (VHD) 上でも構いません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Put the payment connector assemblies and files in the correct locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ アセンブリとファイルを正しい場所に配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Payment connectors are pluggable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタはプラグ可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In a development environment, you can put the correct files in the correct locations on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境では、サーバーの適切な場所に適切なファイルを配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The following table shows which files should go in which location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、どのファイルをどの場所に置くべきかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Contents of the IPaymentProcessor Assemblies folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPaymentProcessor Assemblies フォルダーのコンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Contents of the Payment Web Files folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払い Web ファイル フォルダーのコンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Contents of the IPaymentDevice Assemblies folder</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IPaymentDevice Assemblies フォルダーのコンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.PackageDirectory<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/Connectors/ <ph id="ph3">&amp;lt;</ph><bpt id="p2">*</bpt>Aos.WebRoot<ept id="p2">*</ept><ph id="ph4">&amp;gt;</ph>/bin/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.PackageDirectory<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/Connectors/ <ph id="ph3">&amp;lt;</ph><bpt id="p2">*</bpt>Aos.WebRoot<ept id="p2">*</ept><ph id="ph4">&amp;gt;</ph>/bin/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>RS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>RS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>CPOS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>CPOS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Remote Hardware Station (Internet Information Services <ph id="ph1">\[</ph>IIS<ph id="ph2">\]</ph>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート ハードウェア ステーション (インターネット インフォメーション サービス <ph id="ph1">\[</ph>IIS<ph id="ph2">\]</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/bin/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Modern POS Local Hard Station (Information Protection and Control <ph id="ph1">\[</ph>IPC<ph id="ph2">\]</ph>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS のローカルのハード ステーション (情報の保護とコントロール <ph id="ph1">\[</ph>IPC<ph id="ph2">\]</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/ClientBroker/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/ClientBroker/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/ClientBroker/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/ClientBroker/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>E-commerce</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">E コマース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>ECOM.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>ECOM.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph>/Connectors/</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Not applicable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当なし</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Here is a key to the preceding table:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のテーブルへのキーを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.PackageDirectory<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the package directory of AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.PackageDirectory<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> は AOS のパッケージ ディレクトリです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You can find the path from the web.config file for AOS (key = <bpt id="p1">**</bpt>Aos.PackageDirectory<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パスは AOS の web.config ファイルから見つけることができます (key = <bpt id="p1">**</bpt>Aos.PackageDirectory<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the web application root of AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>Aos.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> は AOS の Web アプリケーション ルートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>RS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the web application root of Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>RS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> は Retail サーバーの Web アプリケーション ルートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the web application root of a remote Hardware Station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>HWS.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> はリモート ハードウェア ステーションの Web アプリケーション ルートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the app installation folder of Modern POS (for example, C:<ph id="ph3">\\</ph>Program Files (x86)<ph id="ph4">\\</ph>Microsoft Dynamics AX70<ph id="ph5">\\</ph>Retail Modern POS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>MPOS.AppRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> は Modern POS (例えば、<ph id="ph3">\\</ph>C:Program Files (x86)<ph id="ph4">\\</ph>Microsoft Dynamics AX70<ph id="ph5">\\</ph>Retail Modern POS) のアプリ インストール フォルダーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>ECOM.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> is the web application root of an e-commerce website.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph><bpt id="p1">*</bpt>ECOM.WebRoot<ept id="p1">*</ept><ph id="ph2">&amp;gt;</ph> は電子商取引 Web サイト の Web アプリケーション ルートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The Payment Web Files folder usually contains a subfolder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払 Web ファイル フォルダーには通常、サブフォルダーが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Be sure to copy the whole subfolder to the target locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブフォルダー全体をターゲットの場所にコピーしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use a payment connector with an e-commerce site</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子商取引サイトで支払コネクタを使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>E-commerce sites aren't deployed in LCS-managed environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">E コマース サイトは、LCS の管理された環境では配置されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>You should work with your partner to decide how to host an e-commerce site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パートナーと連携して、電子商取引サイトをホストする方法を決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If the payment connector requires payment web files, you must deploy those web files to your e-commerce site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタに支払 Web ファイルが必要とされる場合は、電子商取引にこれらの Web ファイルを配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>If your payment connector doesn't require payment web files, no additional steps are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタが、支払 Web ファイルを必要としない場合、追加の手順は必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>For information about how to deploy payment web files to an e-commerce site, see the <bpt id="p1">[</bpt>Put the payment connector assemblies and files in the correct locations<ept id="p1">](deploy-payment-connector.md#put-the-payment-connector-assemblies-and-files-in-the-correct-locations)</ept> section earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払 Web ファイルを電子商取引サイトに配置する方法については、このトピックの前半にある<bpt id="p1">[</bpt>支払コネクタ アセンブリとファイルを正しい場所に配置する<ept id="p1">](deploy-payment-connector.md#put-the-payment-connector-assemblies-and-files-in-the-correct-locations)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">[</bpt>Guide to implementing a payment connector and a payment device<ept id="p1">](https://download.microsoft.com/download/4/D/7/4D7C6B05-0C23-4C6C-BA13-AB62ED08AA61/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device.docx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>支払コネクタと支払デバイスの実装ガイド<ept id="p1">](https://download.microsoft.com/download/4/D/7/4D7C6B05-0C23-4C6C-BA13-AB62ED08AA61/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device.docx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">[</bpt>Retail SDK packaging<ept id="p1">](retail-sdk/retail-sdk-packaging.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail SDK 小売パッケージ<ept id="p1">](retail-sdk/retail-sdk-packaging.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>