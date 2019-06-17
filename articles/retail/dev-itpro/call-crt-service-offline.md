<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="call-crt-service-offline.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>call-crt-service-offline.c5299b.26644fa2c9f4b4ff29573a4d15d315d10b516746.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>26644fa2c9f4b4ff29573a4d15d315d10b516746</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\call-crt-service-offline.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Call the Commerce runtime (CRT) service in offline mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Runtime (CRT) サービスをオフライン モードで呼び出す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how provide offline support for point of sale (POS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Call the Commerce runtime (CRT) service in offline mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Runtime (CRT) サービスをオフライン モードで呼び出す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This implementation is not supported for versions 7.2 and higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For those versions, follow the extension model without overlayering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic describes how provide offline support for point of sale (POS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>When a point of sale (POS) device goes offline (in other words, when it isn't connected to Retail Server), the POS automatically switches to the local commerce runtime (CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) デバイスがオフラインになると (すなわち、Retail サーバーに接続されていないとき)、その POS はローカル商業ランタイム (CRT) に自動的に切り替わります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS client communicates with the local CRT by using the Retail proxy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS クライアントは、Retail プロキシを使用して、ローカル CRT と通信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To enable the proxy to understand your custom service, you must extend the Retail proxy project to support your request type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロキシがカスタム サービスを理解できるようにするには、Retail プロキシ プロジェクトを拡張して要求タイプをサポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In Microsoft Visual Studio, from the Retail SDK<ph id="ph1">\\</ph>Proxies folder, open Proxies.RetailProxy.csproj.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio で、Retail SDK<ph id="ph1">\\</ph>プロキシ フォルダーから Proxies.RetailProxy.csproj を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Update RetailSDK<ph id="ph1">\\</ph>Proxies<ph id="ph2">\\</ph>RetailProxy<ph id="ph3">\\</ph>Adapters<ph id="ph4">\\</ph>UsingStatements.Extensions with the new namespace that you defined for the new entity/complex types that were introduced in CRT extension projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailSDK<ph id="ph1">\\</ph>Proxies<ph id="ph2">\\</ph>RetailProxy<ph id="ph3">\\</ph>Adapters<ph id="ph4">\\</ph>UsingStatements.Extensions を、CRT 拡張プロジェクトで導入された新しいエンティティ/複合型に対して定義した新しい名前空間で更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These projects or dynamics-link libraries (DLLs) must first be referenced by Proxies.RetailProxy.csproj.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロジェクトまたはダイナミクス リンク ライブラリ (DLL) は、まず Proxies.RetailProxy.csproj によって参照される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Compile the Proxies.RetailProxy project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proxies.RetailProxy プロジェクトをコンパイルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>During compilation, Adapters<ph id="ph1">\\</ph>Interfaces.g.cs is updated with your new entity and interface information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル中に、アダプタ <ph id="ph1">\\</ph>Interfaces.g.cs は、新しいエンティティおよびインターフェイスの情報で更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Don't modify this automatically generated class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動的に生成されたクラスを変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Add your new manager class to the Adapters folder, and call your CRT service from that manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アダプタ フォルダーに新しいマネージャー クラスを追加し、そのマネージャーから CRT サービスを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The standard entity manager classes, such as <bpt id="p1">**</bpt>SalesOrderManager<ept id="p1">**</ept> and <bpt id="p2">**</bpt>PurchaseOrderManager<ept id="p2">**</ept>, are available in the Adapters folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesOrderManager<ept id="p1">**</ept> や <bpt id="p2">**</bpt>PurchaseOrderManager<ept id="p2">**</ept> などの標準エンティティ マネージャー クラスは、[Adapters] フォルダーにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> All the libraries that are used in the project must be portable and signed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> プロジェクトで使用されるすべてのライブラリは、移動可能で署名されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>(Any custom CRT service that is referenced must be a portable library.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(参照されるカスタムの CRT サービスは、移動可能なライブラリである必要があります。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Update the public key in the CRT configuration file, because a new public key is generated after compilation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル後に新しい公開キーが生成されるため、CRT 構成ファイルの公開キーを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Build and replace the new proxy DLL in the Microsoft Dynamics AX<ph id="ph1">\\</ph>70<ph id="ph2">\\</ph>Retail Modern POS<ph id="ph3">\\</ph>ClientBroker folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX<ph id="ph1">\\</ph>70<ph id="ph2">\\</ph>Retail Modern POS<ph id="ph3">\\</ph>ClientBroker フォルダで、新しいプロキシ DLL をビルドして置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Additionally, drop the custom CRT extension library into the Microsoft Dynamics AX<ph id="ph1">\\</ph>70<ph id="ph2">\\</ph>Retail Modern POS<ph id="ph3">\\</ph>ClientBroker folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム CRT 拡張ライブラリを、Microsoft DynamicsAX<ph id="ph1">\\</ph>70<ph id="ph2">\\</ph>Retail Modern POS<ph id="ph3">\\</ph>ClientBroker フォルダへドロップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>(All libraries that are referenced should be dropped into this folder.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(参照されるすべてのライブラリは、このフォルダにドロップする必要があります)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In the DllHost.exe.config file, update <bpt id="p1">**</bpt>RetailProxyAssemblyName<ept id="p1">**</ept> and <bpt id="p2">**</bpt>AdaptorCallerFullTypeName<ept id="p2">**</ept> with the new proxy DLL and adapter name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DllHost.exe.config ファイルで、<bpt id="p1">**</bpt>RetailProxyAssemblyName<ept id="p1">**</ept> および <bpt id="p2">**</bpt>AdaptorCallerFullTypeName<ept id="p2">**</ept> を新しいプロキシ DLL およびアダプタ名に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the CommerceRuntime.MPOSOffline.config file, in the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>composition<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> element, update the new CRT DLL information as for the commerceRuntime.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime.MPOSOffline.config ファイルの <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>構成<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> 要素で、commerceRuntime.config ファイルに関する新しい CRT DLL 情報を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Restart dllhost.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dllhost.exe を再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>(You should restart the dllhost.exe for MPOS to read the new config file, this will be required even when you do any upgrade if it has config file changes.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(新しい構成ファイルを読むために MPOS の dllhost.exe を再起動する必要があります。構成ファイルの変更がある場合、アップグレードをする際に必要になります。)</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>