<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-windows-installer-payment-connector.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-windows-installer-payment-connector.7c56eb.5e36c1085d708342490a09bdd4ad88379011e4f9.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5e36c1085d708342490a09bdd4ad88379011e4f9</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\create-windows-installer-payment-connector.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create Windows installers for payment connectors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ用の Windows インストーラーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to create a Windows installer for a payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、支払コネクタの Windows インストーラーを作成する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create Windows installers for payment connectors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタ用の Windows インストーラーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how to create a Windows installer for a payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、支払コネクタの Windows インストーラーを作成する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic is targeted at developers working for or with a payment connector provider, for example, MasterCard or Visa, to describe how to package a payment connector, which can then be shared with implementation partners working for specific customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、支払いコネクタをパッケージ化する方法を説明するために、MasterCard や Visa などの支払コネクタ プロバイダで作業する開発者を対象にしています。支払コネクタは特定顧客向けに作業する実装パートナーと共有できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>After you've implemented and tested your payment connector in the development environment, you must create an installer to transfer the payment connector to a retailer IT professional or a value-added reseller (VAR) for production deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境で支払いコネクタを実装してテストした後、生産の配置のため小売業者 IT プロフェッショナルに支払コネクタまたは付加価値再販業者 (VAR) を転送するインストーラーを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For more information, see <bpt id="p1">[</bpt>Payment integration with a payment terminal<ept id="p1">](end-to-end-payment-extension.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>支払ターミナルと支払の統合<ept id="p1">](end-to-end-payment-extension.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Windows Installer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows インストーラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Microsoft Windows Installer (MSI) is the application and configuration service for Microsoft Windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows インストーラー (MSI) は、Microsoft Windows 用のアプリケーションおよび構成サービスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You must create an installer that contains all the files that are required in order to deploy a payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタを配置するために必要なすべてのファイルが含まれるインストーラーを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The installer itself doesn't deploy the payment connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラー自体は支払コネクタを配置しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It just unzips and copies the connector files to a designated folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したフォルダーにコネクタ ファイルを解凍してコピーするだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The next section of this topic defines the contents of that folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの次のセクションでは、そのフォルダーの内容を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>You can configure the installer to require that customers accept a user agreement before they can continue with the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールを続行する前に顧客がユーザー契約の受け入れを要求するように、インストーラーを構成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You can also choose your preferred format for the installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、インストーラーに対して優先する形式を選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For example, you can have an .exe file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、.exe ファイルを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Installer contents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーの内容</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The installer must install the required files in the following structure:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーは、次の構造で必要なファイルをインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You can find these folders in <bpt id="p1">**</bpt>...\RetailSDK\PaymentExternals<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフォルダーは <bpt id="p1">**</bpt>...\RetailSDK\PaymentExternals<ept id="p1">**</ept> で検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>PaymentExternals<ept id="p1">**</ept> – This folder contains up to three subfolders:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PaymentExternals<ept id="p1">**</ept> – このフォルダには、最大 3 つのサブフォルダーが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>IPaymentDevice Assemblies<ept id="p1">**</ept> – This folder contains the assembly that implements the IPaymentDevice interface and its dependent assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPaymentDevice Assemblies<ept id="p1">**</ept> – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>These assemblies are used in Hardware station and Retail Modern POS to communicate with payment terminal devices, such as VeriFone MX925.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのアセンブリは、VeriFone MX925 などの決済端末デバイスと通信するために、ハードウェア ステーションおよび Retail Modern POS で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If you don’t support a payment terminal device, you can omit this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払のターミナル デバイスをサポートしていない場合は、このフォルダを省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>IPaymentProcessor Assemblies<ept id="p1">**</ept> – This folder contains the assembly that implements the IPaymentProcesor interface and its dependent assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPaymentProcessor Assemblies<ept id="p1">**</ept> – このフォルダーには、IPaymentProcesor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Payment Web Files<ept id="p1">**</ept> – This folder contains the callback HTML/JavaScript/CSS files that are required in order to enable the payment accepting page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払 Web ファイル<ept id="p1">**</ept> – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML/JavaScript/CSS ファイルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If the payment accepting web app follows the Microsoft implementation guide, these payment web files aren't required, and you can omit this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払い受諾ウェブ アプリケーションが Microsoft の導入ガイドに従っている場合、これらの支払いウェブ ファイルは必須ではなく、このフォルダを省略することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In some cases, the payment accepting page requires that a callback page be deployed to the host application server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、支払受け入れページでは、コールバック ページをホスト アプリケーション サーバーに配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In that case, you must include a folder for the callback page:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合、コールバック ページのフォルダーを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Payment<ph id="ph2">\_</ph>Connector<ph id="ph3">\_</ph>Name<ph id="ph4">&amp;gt;</ph><ept id="p1">**</ept> – To avoid file conflicts from different payment connectors, the payment web files must be placed inside subfolders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>支払<ph id="ph2">\_</ph>コネクタ<ph id="ph3">\_</ph>名<ph id="ph4">&amp;gt;</ph><ept id="p1">**</ept> - 異なる支払コネクタからのファイルの競合を避けるためには、支払い Web ファイルをサブフォルダ内に配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>We recommend that you use the connector name as the name of the subfolder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブフォルダーの名前としてコネクタ名を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Other utility tools<ept id="p1">**</ept> – If you have other utility tools, such as a configuration utility for a payment terminal device, you can include them here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>その他のユーティリティ ツール<ept id="p1">**</ept> – 決済端末装置用の構成ユーティリティなど、他のユーティリティツールがある場合は、ここに含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If you don’t support any payment terminal devices, you can omit these files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払のターミナル デバイスをサポートしていない場合は、これらのフォルダを省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The utility tool should be designed to interact only with the payment terminal devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーティリティー ツールは、支払のターミナル デバイスとのみ対話するように設計する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>It should not interact with anything in Hardware station or Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションまたは Modern POS 内のものを操作しないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Hardware station and Modern POS will be packaged together with files from the Payment Connector folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションおよび Modern POS は支払コネクタ フォルダーからファイルと共にパッケージ化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>README.txt<ept id="p1">**</ept> – This file describes the contents of the folder and how to use any utilities that are included.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>README.txt<ept id="p1">**</ept> – このファイルには、フォルダの内容と、含まれているユーティリティの使用方法が記載されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The file must also include the payment page URLs that are required in the Cloud POS web.config and Modern POS package.appxmanifest files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルには、Cloud POS web.config および Modern POS package.appxmanifest ファイルに必要な支払いページの URL も含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>If you support any payment terminal devices, the file must also mention the name of the assembly that implements the IPaymentDevice interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払ターミナル デバイスをサポートする場合、このファイルには、IPaymentDevice インターフェイスを実装しているアセンブリの名前も記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The assembly will be registered in the Hardware Station .config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセンブリは、ハードウェア ステーション .config ファイルに登録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The following illustration shows the file structure for a connector that is named TestConnector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、TestConnector という名前のコネクタのファイル構造を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>File structure for TestConnector<ept id="p1">](./media/paymentconnectorinstaller.png)](./media/paymentconnectorinstaller.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>TestConnector のファイル構造<ept id="p1">](./media/paymentconnectorinstaller.png)](./media/paymentconnectorinstaller.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>