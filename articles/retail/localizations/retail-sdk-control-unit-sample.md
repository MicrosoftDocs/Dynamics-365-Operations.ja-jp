<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-sdk-control-unit-sample.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-sdk-control-unit-sample.c6e347.cba9f2fec7bdc4cafabb1cc86ae7752e16d65809.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>cba9f2fec7bdc4cafabb1cc86ae7752e16d65809</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\localizations\retail-sdk-control-unit-sample.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Sample for Retail POS integration with control units for Sweden</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スウェーデン用の管理単位との Retail POS の統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic is the building and installation guide for the sample for control unit integration for Sweden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、スウェーデンの管理単位統合サンプルのビルドとインストールのガイドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Sample for Retail POS integration with control units for Sweden</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スウェーデン用の管理単位との Retail POS の統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source><bpt id="p1">**</bpt>SAMPLE CODE NOTICE<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サンプル コードの通知<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>THIS SAMPLE CODE IS MADE AVAILABLE AS IS.  MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.  THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source><bpt id="p1">**</bpt>NO TECHNICAL SUPPORT IS PROVIDED.  YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This sample shows how to create Microsoft Dynamics 365 for Retail extensions to integrate Retail Modern POS or Cloud POS with a fiscal register.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Microsoft Dynamics 365 for Retail 拡張機能を作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Specifically, this sample includes the code for integrating Microsoft Dynamics for Retail POS with control units for Sweden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特に、このサンプルには Microsoft Dynamics for Retail POS をスウェーデンの管理単位と統合するコードが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>As an example, this sample uses the application programming interface (API) of the CleanCash® Type A control unit by Retail Innovation HTT AB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Version 1.1.4 of the CleanCash® API is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CleanCash® API のバージョン1.1.4 が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For the integration package that includes the API and documentation, contact the manufacturer of the device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This sample is a part of the Retail software development kit (SDK).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For information about how to install and use the Retail SDK, see the <bpt id="p1">[</bpt>Retail SDK documentation<ept id="p1">](../dev-itpro/retail-sdk/retail-sdk-overview.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK をダウンロードして使用する方法については、<bpt id="p1">[</bpt>Retail SDK ドキュメント<ept id="p1">](../dev-itpro/retail-sdk/retail-sdk-overview.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This sample consists of extensions for the Hardware station, commerce runtime (CRT), and point of sale (POS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルは、ハードウェア ステーション、<ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>)、および 販売時点管理 (POS) で構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To run this sample, you must modify and build the Hardware station, CRT, and POS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Some steps in the procedures in this topic differ, depending on the version of Microsoft Dynamics 365 for Retail that you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用している Microsoft Dynamics 365 for Retail のバージョンによって、このトピックの手順の一部が異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For more information, see <bpt id="p1">[</bpt>What's new or changed in Dynamics 365 for Retail<ept id="p1">](../get-started/whats-new.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、 <bpt id="p1">[</bpt>Dynamics 365 for Retail の新機能および変更された機能<ept id="p1">](../get-started/whats-new.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Development environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Follow these steps to set up a development environment so that you can test and extend the sample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Extend the Hardware station component:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーション コンポーネントを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the Hardware station solution under <bpt id="p1">**</bpt>RetailSDK<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>HardwareStation<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>RetailSDK<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>HardwareStation<ept id="p1">**</ept>から ハードウェア ステーション ソリューションを開きます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Find the <bpt id="p1">**</bpt>HardwareStation.Extension.FiscalRegisterSample.csproj<ept id="p1">**</ept> extension project, and compile it.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HardwareStation.Extension.FiscalRegisterSample.csproj<ept id="p1">**</ept> 拡張機能プロジェクトを検索し、コンパイルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Find extension assemblies and configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能アセンブリおよび設定を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>Retail 7.3 and earlier<ept id="p1">](#tab/retail-7-3)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3 以前<ept id="p1">](#tab/retail-7-3)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Find the following files in <bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept>:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept> から以下のファイルを検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> assembly</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> アセンブリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> configuration</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The <bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> assembly</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> アセンブリ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">[</bpt>Retail 7.3.1 and later<ept id="p1">](#tab/retail-7-3-1)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3.1 およびそれ以降<ept id="p1">](#tab/retail-7-3-1)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Find the following files in <bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept> から以下のファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> assembly</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> アセンブリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> configuration</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The <bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> assembly</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> アセンブリ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">[</bpt>Retail 10.0 and later<ept id="p1">](#tab/retail-10-0)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 10.0 およびそれ以降<ept id="p1">](#tab/retail-10-0)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Find the following files in <bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Extension.FiscalRegisterSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p1">**</ept> から以下のファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> assembly</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll<ept id="p1">**</ept> アセンブリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The <bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> configuration</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config<ept id="p1">**</ept> コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Find the following file in <bpt id="p1">**</bpt>RetailSDK<ph id="ph1">\\</ph>References<ph id="ph2">\\</ph>Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1<ph id="ph3">\\</ph>lib<ph id="ph4">\\</ph>net451<ept id="p1">**</ept>:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>RetailSDK<ph id="ph1">\\</ph>References<ph id="ph2">\\</ph>Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1<ph id="ph3">\\</ph>lib<ph id="ph4">\\</ph>net451<ept id="p1">**</ept> にて次のファイルを検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The <bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> assembly</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Interop.CleanCash<ph id="ph1">\_</ph>1<ph id="ph2">\_</ph>1.dll<ept id="p1">**</ept> アセンブリ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Copy the files to a deployed Hardware station machine:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ファイルを配置した ハードウェア ステーション マシンにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Remote Hardware station:<ept id="p1">**</ept> Copy the files to the <bpt id="p2">**</bpt>bin<ept id="p2">**</ept> folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リモート ハードウェア ステーション:<ept id="p1">**</ept> ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の <bpt id="p2">**</bpt>bin<ept id="p2">**</ept> フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Local Hardware station:<ept id="p1">**</ept> Copy the files to the Modern POS client broker location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル ハードウェア ステーション:<ept id="p1">**</ept> Modern POS クライアント ブローカーの場所にファイルをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Find the configuration file for Hardware station's extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">[</bpt>Retail 7.3 and earlier<ept id="p1">](#tab/retail-7-3)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3 以前<ept id="p1">](#tab/retail-7-3)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Remote Hardware station:<ept id="p1">**</ept> The file is named <bpt id="p2">**</bpt>hardwarestation.shared.config<ept id="p2">**</ept>, and it's under the IIS Hardware station site location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リモート ハードウェア ステーション:<ept id="p1">**</ept> ファイルの名前は <bpt id="p2">**</bpt>hardwarestation.shared.config<ept id="p2">**</ept>で、IIS ハードウェア ステーション サイトの場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Local Hardware station:<ept id="p1">**</ept> The file is named <bpt id="p2">**</bpt>HardwareStation.Dedicated.config<ept id="p2">**</ept>, and it's under the Modern POS client broker location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル ハードウェア ステーション:<ept id="p1">**</ept> ファイルの名前は <bpt id="p2">**</bpt>HardwareStation.Dedicated.config<ept id="p2">**</ept>で、Modern POS クライアント ブローカーの場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">[</bpt>Retail 7.3.1 and later<ept id="p1">](#tab/retail-7-3-1)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3.1 およびそれ以降<ept id="p1">](#tab/retail-7-3-1)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The file is named <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの名前は <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Remote Hardware station:<ept id="p1">**</ept> The file is located under the IIS Hardware station site location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リモート ハードウェア ステーション:<ept id="p1">**</ept> ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Local Hardware station:<ept id="p1">**</ept> The file is located under the Modern POS client broker location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル ハードウェア ステーション:<ept id="p1">**</ept> ファイルは Modern POS クライアント ブローカーの場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">[</bpt>Retail 10.0 and later<ept id="p1">](#tab/retail-10-0)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 10.0 およびそれ以降<ept id="p1">](#tab/retail-10-0)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The file is named <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept>:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの名前は <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">**</bpt>Remote Hardware station:<ept id="p1">**</ept> The file is located under the IIS Hardware station site location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リモート ハードウェア ステーション:<ept id="p1">**</ept> ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Local Hardware station:<ept id="p1">**</ept> The file is located under the Modern POS client broker location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル ハードウェア ステーション:<ept id="p1">**</ept> ファイルは Modern POS クライアント ブローカーの場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Add the following section to the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section of the config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルの <bpt id="p1">**</bpt>構成<ept id="p1">**</ept> セクションに、次のセクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">[</bpt>Retail 7.3 and earlier<ept id="p1">](#tab/retail-7-3)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3 以前<ept id="p1">](#tab/retail-7-3)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt>Retail 7.3.1 and later<ept id="p1">](#tab/retail-7-3-1)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3.1 およびそれ以降<ept id="p1">](#tab/retail-7-3-1)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">[</bpt>Retail 10.0 and later<ept id="p1">](#tab/retail-10-0)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 10.0 およびそれ以降<ept id="p1">](#tab/retail-10-0)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Restart the Hardware station service:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーション サービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Remote Hardware station:<ept id="p1">**</ept> Restart the Hardware station site from IIS Manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リモート ハードウェア ステーション:<ept id="p1">**</ept> IIS マネージャーからハードウェア ステーション サイトを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Local Hardware station:<ept id="p1">**</ept> End the <bpt id="p2">**</bpt>dllhost.exe<ept id="p2">**</ept> process in Task Manager, and then restart Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル ハードウェア ステーション:<ept id="p1">**</ept> タスク マネージャーで <bpt id="p2">**</bpt>dllhost.exe<ept id="p2">**</ept> プロセスを終了して、Modern POS を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Extend the CRT component:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT コンポーネントの拡張。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Open the CRT solution, <bpt id="p1">**</bpt>CommerceRuntimeSamples.sln<ept id="p1">**</ept>, under <bpt id="p2">**</bpt>RetailSdk<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>CommerceRuntime<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p2">**</bpt>RetailSdk<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>CommerceRuntime<ept id="p2">**</ept> 配下の、 CRT ソリューション、 <bpt id="p1">**</bpt>CommerceRuntimeSamples.sln<ept id="p1">**</ept> を開きます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Find the <bpt id="p1">**</bpt>Runtime.Extensions.FiscalRegisterReceiptSample<ept id="p1">**</ept> project, and build it.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Runtime.Extensions.FiscalRegisterReceiptSample<ept id="p1">**</ept> プロジェクトを探して、構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Find the ext.config file for CRT:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT の ext.config ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Retail Server:<ept id="p1">**</ept> The file is named <bpt id="p2">**</bpt>commerceRuntime.ext.config<ept id="p2">**</ept>, and it's under the <bpt id="p3">**</bpt>bin<ph id="ph1">\\</ph>ext<ept id="p3">**</ept> folder under the IIS Retail server site location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Retail Server:<ept id="p1">**</ept> : ファイルは IIS 小売サーバー が格納されている場所の <bpt id="p3">**</bpt>bin<ph id="ph1">\\</ph>ext<ept id="p3">**</ept> フォルダー 配下に <bpt id="p2">**</bpt>commerceRuntime.ext.config<ept id="p2">**</ept> という名前で作成されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Local CRT on Modern POS:<ept id="p1">**</ept> The file is named <bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p2">**</ept>, and it's under the <bpt id="p3">**</bpt>bin<ph id="ph1">\\</ph>ext<ept id="p3">**</ept> folder under the local CRT client broker location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Modern POS上のローカル CRT :<ept id="p1">**</ept> ファイルは、ローカル CRT クライアントブローカーが格納されている場所の <bpt id="p3">**</bpt>bin<ph id="ph1">\\</ph>ext<ept id="p3">**</ept> フォルダ配下に、 <bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p2">**</ept> という名前で作成されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Register the CRT change in the configuration file.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルで CRT の変更を登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Do <bpt id="p1">**</bpt>not<ept id="p1">**</ept> edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては<bpt id="p1">**</bpt>いけません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>These files aren't intended for any customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのファイルはカスタマイズのためのものではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Find the <bpt id="p1">**</bpt>Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll<ept id="p1">**</ept> assembly file in <bpt id="p2">**</bpt>Extensions.FiscalRegisterReceiptSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p2">**</bpt>Extensions.FiscalRegisterReceiptSample<ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>Debug<ept id="p2">**</ept> で、 <bpt id="p1">**</bpt>Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll<ept id="p1">**</ept> アセンブリを検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Copy the assembly to the CRT extensions folder:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">アセンブリを CRT 拡張機能フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">**</bpt>Retail Server:<ept id="p1">**</ept> Copy the assembly to the <bpt id="p2">**</bpt><ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>ext<ept id="p2">**</ept> folder under the IIS Retail server site location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>小売りサーバー:<ept id="p1">**</ept> アセンブリを IIS Retail Server が格納されている場所の配下にある <bpt id="p2">**</bpt><ph id="ph1">\\</ph>bin<ph id="ph2">\\</ph>ext<ept id="p2">**</ept> フォルダーにコピーします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Local CRT on Modern POS:<ept id="p1">**</ept> Copy the assembly to the <bpt id="p2">**</bpt><ph id="ph1">\\</ph>ext<ept id="p2">**</ept> folder under the local CRT client broker location.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Local CRT on Modern POS:<ept id="p1">**</ept> アセンブリをローカル CRT クライアント ブローカーがある場所の下の <bpt id="p2">**</bpt><ph id="ph1">\\</ph>\ext<ept id="p2">**</ept> フォルダーにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>All the code changes for CRT and Retail Server are all part of RetailSdk<ph id="ph1">\\</ph>SampleExtensions.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">CRT および Retail サーバーに対するコードの変更はすべて、RetailSdk<ph id="ph1">\\</ph>SampleExtensions の一部となります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, the preceding steps show how to build, deploy, and test these code changes.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Extend the Modern POS component:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Modern POS コンポーネントの拡張。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Open the solution at <bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>ModernPOS.sln<ept id="p1">**</ept>, and make sure that it can be compiled without errors.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>ModernPOS.sln<ept id="p1">**</ept> でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Also make sure that Modern POS can be run from Microsoft Visual Studio using the <bpt id="p1">**</bpt>Run<ept id="p1">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、Modern POS が <bpt id="p1">**</bpt>Run<ept id="p1">**</ept> コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>(Modern POS must not be customized.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">(Modern POS をカスタマイズしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>You must enable User Account Control <ph id="ph1">\[</ph>UAC<ph id="ph2">\]</ph>, and you must uninstall previously installed instances of Modern POS as required.)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ユーザー アカウント制御 <ph id="ph1">\[</ph>UAC<ph id="ph2">\]</ph> を有効にし、必要に応じて既にインストールされている Modern POS のインスタンスをアンインストールする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Include <bpt id="p1">**</bpt>FiscalRegisterSample<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Pos.Extensions<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Pos.Extensions<ept id="p2">**</ept> プロジェクトの <bpt id="p1">**</bpt>FiscalRegisterSample<ept id="p1">**</ept> を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Enable the extension to be compiled in <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> by removing the <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> folder from the exclude list.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">除外リストから <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> フォルダーを削除して、<bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> でコンパイルされる拡張機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Enable the extension in <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> by adding the following lines in the appropriate place.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">以下の行を適切な場所に追加することで、 <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> の拡張機能を有効にします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Rebuild the solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Run Modern POS in the debugger, and test the functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガーでModern POS を実行し、機能をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Extend the Cloud POS component:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">クラウド POS コンポーネントの拡張。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Open the solution at <bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>CloudPOS.sln<ept id="p1">**</ept>, and make sure that it can be compiled without errors.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>CloudPOS.sln<ept id="p1">**</ept> でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Include <bpt id="p1">**</bpt>FiscalRegisterSample<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Pos.Extensions<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>Pos.Extensions<ept id="p2">**</ept> プロジェクトの <bpt id="p1">**</bpt>FiscalRegisterSample<ept id="p1">**</ept> を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Enable the extension to be compiled in <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> by removing the <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> folder from the exclude list.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">除外リストから <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> フォルダーを削除して、<bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> でコンパイルされる拡張機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Enable the extension in <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> by adding the following lines in the appropriate place.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">以下の行を適切な場所に追加することで、 <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> の拡張機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Rebuild the solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Run the solution by using the <bpt id="p1">**</bpt>Run<ept id="p1">**</ept> command and following the steps in the Retail SDK handbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実行<ept id="p1">**</ept>コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Test the functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Set up the fiscal register configuration and other required parameters in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、会計登録構成と、その他の必要なパラメーターを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>For more information, see <bpt id="p1">[</bpt>Cash registers for Sweden<ept id="p1">](emea-swe-cash-registers.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>スウェーデンのキャッシュ レジスター<ept id="p1">](emea-swe-cash-registers.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Production environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Follow these steps to create and apply deployable packages that contain Retail components in a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順に従い、実稼働環境で小売コンポーネントを含む配置可能パッケージを作成して適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Extend the POS component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS コンポーネントの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Enable the extension to be compiled in <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> by removing the <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> folder from the exclude list.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">除外リストから <bpt id="p2">**</bpt>FiscalRegisterSample<ept id="p2">**</ept> フォルダーを削除して、<bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> でコンパイルされる拡張機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Enable the extension in <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> by adding the following lines in the appropriate place.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">以下の行を適切な場所に追加することで、 <bpt id="p1">**</bpt>Extensions<ph id="ph1">\\</ph>extensions.json<ept id="p1">**</ept> の拡張機能を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Make the following changes in the package config files under the <bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>Assets<ept id="p1">**</ept> folder:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>RetailSdk<ph id="ph1">\\</ph>Assets<ept id="p1">**</ept> フォルダのパッケージ構成ファイルに、次の変更を加えます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Add the following section to the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section of the <bpt id="p2">**</bpt>commerceruntime.ext.config<ept id="p2">**</ept> and <bpt id="p3">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p3">**</ept> config files.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>commerceruntime.ext.config<ept id="p2">**</ept> および <bpt id="p3">**</bpt>CommerceRuntime.MPOSOffline.Ext.config<ept id="p3">**</ept> 構成ファイルの <bpt id="p1">**</bpt>構成<ept id="p1">**</ept> セクションに、次のセクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Add the following section to the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section of the Hardware station configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーション構成ファイルの <bpt id="p1">**</bpt>構成<ept id="p1">**</ept> セクションに、次のセクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">[</bpt>Retail 7.3 and earlier<ept id="p1">](#tab/retail-7-3)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3 以前<ept id="p1">](#tab/retail-7-3)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Modify the <bpt id="p1">**</bpt>HardwareStation.Shared.config<ept id="p1">**</ept> and <bpt id="p2">**</bpt>HardwareStation.Dedicated.config<ept id="p2">**</ept> configuration files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HardwareStation.Shared.config<ept id="p1">**</ept> および <bpt id="p2">**</bpt>HardwareStation.Dedicated.config<ept id="p2">**</ept> 構成ファイルを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">[</bpt>Retail 7.3.1 and later<ept id="p1">](#tab/retail-7-3-1)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 7.3.1 およびそれ以降<ept id="p1">](#tab/retail-7-3-1)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Modify the <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> configuration file:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> 構成ファイルを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">[</bpt>Retail 10.0 and later<ept id="p1">](#tab/retail-10-0)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Retail 10.0 およびそれ以降<ept id="p1">](#tab/retail-10-0)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Modify the <bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> configuration file:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HardwareStation.Extension.config<ept id="p1">**</ept> 構成ファイルを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Run <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> for the whole Retail SDK to create deployable packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK 全体で <bpt id="p1">**</bpt>msbuild<ept id="p1">**</ept> を実行し、配置可能なパッケージを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For more information, see <bpt id="p1">[</bpt>Retail SDK packaging<ept id="p1">](../dev-itpro/retail-sdk/retail-sdk-packaging.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Retail SDK パッケージ<ept id="p1">](../dev-itpro/retail-sdk/retail-sdk-packaging.md)</ept> を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>