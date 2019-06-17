<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="hardware-station-extensibility.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>hardware-station-extensibility.bce075.5dfaea195248edb7b22b59ca9b85812d6e70d400.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5dfaea195248edb7b22b59ca9b85812d6e70d400</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\hardware-station-extensibility.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Hardware Station extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hardware Station 拡張性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to extend Hardware Station to add support for new devices and new device types for existing devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Hardware Station extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hardware Station 拡張性</target></trans-unit>
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
          <source>This topic explains how to extend Hardware Station to add support for new devices and new device types for existing devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Retail Hardware Station overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station の概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Retail Hardware Station is used by Retail Modern POS and Cloud POS to connect to retail hardware peripherals such as printers, cash drawers, scanners, and payment terminals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station は、プリンター、キャッシュ ドロワー、スキャナー、および支払ターミナルなどの小売ハードウェア周辺機器に接続するために Retail Modern POS および Cloud POS で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>HWS-Local-Traditional<ept id="p1">](./media/hws-local-300x236.png)](./media/hws-local.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>HWS-Local-Traditional<ept id="p1">](./media/hws-local-300x236.png)](./media/hws-local.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>HWS-Shared<ept id="p1">](./media/hws-shared-300x224.png)](./media/hws-shared.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>HWS-Shared<ept id="p1">](./media/hws-shared-300x224.png)](./media/hws-shared.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Retail Hardware Station setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Before you start, use the information in <bpt id="p1">[</bpt>Retail hardware station configuration and installation<ept id="p1">](../retail-hardware-station-configuration-installation.md)</ept> to install Hardware Station, and to get a feel of what hardware is and how it's installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、<bpt id="p1">[</bpt>Retail ハードウェア ステーションのコンフィギュレーションとインストール<ept id="p1">](../retail-hardware-station-configuration-installation.md)</ept>の情報を使用してハードウェア ステーションをインストールし、ハードウェアがどのようなものでインストールがどのようにされているかを知ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Retail Hardware Station architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station アーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Hardware Station exposes Web API for Hardware Station application programming interfaces (APIs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションは、ハードウェア ステーション アプリケーション プログラミング インターフェイス (API) 用の Web API を公開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Hardware Station can be extended either by implementing a new controller for a new device (for example, a cash dispenser) or by overriding an existing controller for an existing device type (for example, a new Audio Jack magnetic stripe reader (MSR) implementation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデバイス (たとえば、現金自動支払機) の新しいコントローラーを実装するか、または既存のデバイス タイプ (たとえば、新しいオーディオ ジャック磁気ストライプ リーダー (MSR) の実装) の既存のコント ローラーを上書きするかのいずれかによって、ハードウェア ステーションを拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Hardware Station Architecture<ept id="p1">](./media/hardware-station-architecture-1024x764.png)](./media/hardware-station-architecture.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ハードウェア ステーション アーキテクチャ<ept id="p1">](./media/hardware-station-architecture-1024x764.png)](./media/hardware-station-architecture.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Retail Hardware Station extensibility scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station 拡張性シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Extensibility in Hardware Station is achieved by using <bpt id="p1">[</bpt>Managed Extensibility Framework (MEF)<ept id="p1">](https://msdn.microsoft.com/en-us/library/dd460648(v=vs.110).aspx)</ept>, which is supported by .NET.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NTE にサポートされている <bpt id="p1">[</bpt>Managed Extensibility Framework (MEF)<ept id="p1">](https://msdn.microsoft.com/en-us/library/dd460648(v=vs.110).aspx)</ept> を使用して、ハードウェア ステーションの拡張性が獲得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Extensibility guideline:<ept id="p1">**</ept> Always write your extension in your own extension assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張性の規定:<ept id="p1">**</ept> 拡張機能アセンブリで、常に、拡張機能の書き込みをします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>That way, you're writing a true extension, and upgrades will be much easier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのようにして、実際の拡張機能を記述し、アップグレードがかなり簡単になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>There are two basic scenarios for extension:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張のための 2 つの基本的なシナリオがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Adding a new device<ept id="p1">**</ept> – The out-of-box Hardware Station doesn't already support the device (for example, a cash dispenser).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいデバイスを追加する<ept id="p1">**</ept> - 最初から用意されているハードウェア ステーションはデバイス (現金自動支払機など) をまだサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Therefore, you must add support for the new device in Hardware Station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ハードウェア ステーションで新しいデバイスのサポートを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Adding a new device type for an existing device<ept id="p1">**</ept> – The out-of-box Hardware Station implementation already supports the device (for example, an MSR), but you must add support for a specific device type (for example, an Audio Jack MSR implementation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既存のデバイスに対する新しいデバイス タイプを追加する<ept id="p1">**</ept> - 最初から用意されているハードウェア ステーションの実装ではすでにデバイス (MSR など) がサポートされていますが、特定のデバイス タイプ (オーディオ ジャック MSR 実装) のサポートを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Scenario 1: Adding a new device</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ 1: 新しいデバイスを追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For this scenario, we will add support for a cash dispenser device in Hardware Station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、ハードウェア ステーションで、現金自動支払機装置のサポートを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In our example, we will create a fake cash dispenser that dispenses cash in the Notepad file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、メモ帳ファイルで現金を分配する疑似現金自動支払機を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>However, this example will help you understand the end-to-end extensibility of Hardware Station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この例はハードウェア ステーションのエンド ツー エンドの拡張機能を理解するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Retail software development kit (SDK) has a cash dispenser sample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail ソフトウェア開発キット (SDK) には、現金自動支払機のサンプルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>See RetailSdk<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>HardwareStation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailSdk<ph id="ph1">\\</ph>SampleExtensions<ph id="ph2">\\</ph>HardwareStation を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In this case, we must add a new Web API controller and helper properties/methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、新しい Web API コントローラーおよびヘルパー プロパティ/メソッドを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The new <bpt id="p1">**</bpt>CashDispenser<ept id="p1">**</ept> controller must extend <bpt id="p2">**</bpt>ApiController<ept id="p2">**</ept> and <bpt id="p3">**</bpt>IHardwareStationController<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい <bpt id="p1">**</bpt>CashDispenser<ept id="p1">**</ept> コントローラーは、<bpt id="p2">**</bpt>ApiController<ept id="p2">**</ept> と <bpt id="p3">**</bpt>IHardwareStationController<ept id="p3">**</ept> を拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> attribute string here specifies the device that this controller is used for: <ph id="ph1">\[</ph>Export("CASHDISPENSER", typeof(IHardwareStationController))<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここの <bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> 属性文字列は、このコントローラーが使用されるデバイスを指定します: <ph id="ph1">\[</ph>Export("CASHDISPENSER", typeof(IHardwareStationController))<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Scenario 2: Adding a new device type for an existing device</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ 2: 既存のデバイスの新しいデバイス タイプを追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For this scenario, we will add support for a new device type for an existing device (an Audio Jack MSR implementation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、既存のデバイス (オーディオ ジャック MSR 実装) に対する新しいデバイス タイプのサポートを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> attribute string specifies the device that this controller is used for: <ph id="ph1">\[</ph>Export("MSR", typeof(IHardwareStationController))<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept> 属性文字列は、このコントローラーが使用されるデバイスを指定します: <ph id="ph1">\[</ph>Export("MSR", typeof(IHardwareStationController))<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Because there will be multiple controllers for MSRs, Hardware Station uses the configuration file to determine which implementation to use at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MSR に対して複数のコントローラーが存在するため、ハードウェア ステーションは構成ファイルを使用して実行時にどの実装を使用するかを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For more information, see the "Retail Hardware Station extensibility configuration" section later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、この記事の後半の「Retail ハードウェア ステーションの拡張機能コンフィギュレーション」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Retail Hardware Station extensibility configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Hardware Station 拡張性コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Configuration for IIS-hosted Hardware Station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS でホストされているハードウェア ステーションのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Before Hardware Station can consume your extension, the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section in the Hardware Station Web.config file must be updated so that it includes an entry for your extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア ステーションが拡張機能を使用する前に、拡張機能のエントリが含まれるようにハードウェア ステーション Web.config ファイルの<bpt id="p1">**</bpt>合成<ept id="p1">**</ept>セクションを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The order of the composition targets in the configuration file determines precedence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Hardware Station Web Config<ept id="p1">](./media/hws-webconfig.png)](./media/hws-webconfig.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ハードウェア ステーション Web コンフィギュレーション<ept id="p1">](./media/hws-webconfig.png)](./media/hws-webconfig.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Configuration for local IPC-based Hardware Station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル IPC ベースのハードウェア ステーションのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Before local Hardware Station can consume your extension, the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section in the Modern POS DLLHost.exe.config file (C:<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics AX<ph id="ph3">\\</ph>70<ph id="ph4">\\</ph>Retail Modern POS<ph id="ph5">\\</ph>ClientBroker) must be updated so that it includes an entry for your extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカルのハードウェア ステーションが拡張機能を使用する前に、拡張機能用のエントリが含まれるように Modern POS DllHost.exe.config ファイル (C:<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics AX<ph id="ph3">\\</ph>70<ph id="ph4">\\</ph>Retail Modern POS<ph id="ph5">\\</ph>ClientBroker) の<bpt id="p1">**</bpt>合成<ept id="p1">**</ept>セクションを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The order of the composition targets in the configuration file determines precedence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>[</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Local Hardware station config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル ハードウェア ステーションのコンフィギュレーション</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>