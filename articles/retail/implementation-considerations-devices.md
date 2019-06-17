<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="implementation-considerations-devices.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>implementation-considerations-devices.1ea83b.1d8aebb147d710760360ad5e04f10fcea5edc339.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1d8aebb147d710760360ad5e04f10fcea5edc339</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\implementation-considerations-devices.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Device management implementation guidance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイス管理実装ガイダンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic is intended for people who implement functionality that is related to device management in a retail environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、小売環境においてデバイス管理に関連する機能を実装するユーザーを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It gives implementation tips and guidance that you should consider as you plan your implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装を計画する際に考慮する必要がある実装上のヒントとガイダンスを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Device management implementation guidance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイス管理実装ガイダンス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic is intended for people who implement functionality that is related to device management in a retail environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、小売環境においてデバイス管理に関連する機能を実装するユーザーを対象としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It gives implementation tips and guidance that you should consider as you plan your implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装を計画する際に考慮する必要がある実装上のヒントとガイダンスを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A <bpt id="p1">*</bpt>device<ept id="p1">*</ept> is an instrument on which a point of sale (POS) application can be installed, configured, and used to perform operations that are required in order to run or help run the business that owns that instrument.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>デバイス<ept id="p1">*</ept>は、販売時点管理 (POS) をインストール、設定、使用して、その機器を所有するビジネスの実行または実行を助けるのに必要とされる操作を行うための機器です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In other words, a device is a piece of technology that runs a POS application to help run a business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、デバイスは、業務を実行するために POS アプリケーションを実行する 1 つのテクノロジです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This business doesn't have to be exclusively a retail operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この業務は、専ら小売操作である必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For example, a hospital has a gift shop, a warehouse manages inventory, and a law firm generates invoices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、病院にはギフト ショップがあり、倉庫は在庫を管理し、法律事務所が請求書を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>What is important is that the application that the device runs makes business operations simpler, more efficient, or just better managed and recorded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要なことは、デバイスが実行するアプリケーションによって、事業運営がより単純化され、より効率化され、またはいっそうよく管理および記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Regardless of the scenario that they are used in, devices are critical elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるシナリオに関係なく、デバイスは重要な要素です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>As the number of devices that are used increases, it becomes more valuable to put processes in place to track and manage those devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるデバイスの数が増えると、それらのデバイスを追跡して管理するためにプロセスを配置することがより重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Together, these processes are known as <bpt id="p1">*</bpt>device management<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロセスはまとめて <bpt id="p1">*</bpt>デバイス管理<ept id="p1">*</ept> として知られています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The POS application that this topic discusses is Retail Modern POS (MPOS) in Microsoft Dynamics 365 for Finance and Operations, or Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックに記載されているPOSアプリケーションは、 Microsoft Dynamics 365 for Finance and Operations の Retail Modern POS(MPOS)、またはMicrosoft Dynamics 365 for Retail です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>MPOS lets users complete business operations quickly, efficiently, and simply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS で、ユーザーは迅速かつ効率的でシンプルに業務の執行を完了できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It also helps the retail organization manage the many devices that run MPOS across the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、小売企業が業務全体で MPOS を実行する数多くのデバイスを管理するのにも役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Although this topic discusses many aspects of an MPOS device, the two critical aspects are the business-oriented <bpt id="p1">*</bpt>register<ept id="p1">*</ept> and the physical concept of a <bpt id="p2">*</bpt>device<ept id="p2">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックではビジネス指向の 2 つの重要な側面である<bpt id="p1">*</bpt>レジスター<ept id="p1">*</ept>および<bpt id="p2">*</bpt>デバイス<ept id="p2">*</ept>の物理的概念である多くの MPOS デバイス について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>Registers<ept id="p1">**</ept> page is the virtual tracking mechanism for the business-oriented details of an instance of the MPOS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>登録<ept id="p1">**</ept> ページは、MPOS アプリケーションのインスタンスのビジネス指向の詳細に関する仮想追跡メカニズムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These details include the visual profile that is used, the automatic sign-out time, and the store that the register is a part of.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの詳細には、使用されるビジュアル プロファイル、自動サインアウト時間、レジスターが一部であるストアが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>All these details are stored in the virtual register.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらすべての詳細は仮想レジスターに格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When the register is correctly set up and configured, it's linked to a virtual device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスターは、正しく設定および構成されているときは、仮想デバイスにリンクされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The <bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> page is the virtual tracking mechanism for the physical concept of a device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> ページは、デバイスの物理的な概念の仮想追跡メカニズムです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The business-oriented register is linked here to complete the configuration and prepare for installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス指向のレジスターはここでリンクされ、設定を完了し、インストールの準備を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The virtual device stores details such as the validation status, when the POS application was activated, and the version that will be installed or the version that is currently installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想デバイスには、検証状態、POS アプリケーションがアクティブ化された時期、インストールされるバージョン、現在インストールされているバージョンなどの詳細が格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>As more registers are generated and then linked to the appropriate devices, both physical and virtual management become critically important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より多くのレジスターが生成され適切なデバイスにリンクされると、現物と仮想の両方の管理は非常に重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For example, a business has one physical device, a Microsoft Surface that will run MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ビジネスは物理デバイス、MPOS を実行する Microsoft Surface を持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The Surface must be configured for the business, because it might be on a domain or require additional software that is specific to that business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン上にある可能性も、そのビジネスに固有の追加ソフトウェアを必要とすることもあるため、Surface はビジネスに合わせて構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>MPOS must also be installed and activated on the Surface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS は Surface にもインストールして有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Over time, the device might require servicing or replacement, or it might even be stolen.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間の経過と共に、デバイスの修理または交換が必要になったり、盗難の可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If the business doesn't have just one device, but dozens, hundreds, or even thousands, processes must be put in place to appropriately watch, manage, and verify the status of all the devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">企業は、1 つのデバイスが、何十、何、数百、または膨大に割り当てられていない場合は、すべてのデバイスの状態を適切に監視し、管理し、検証するためのプロセスを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>These devices include both devices that are currently used and devices that aren't currently used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのデバイスには、現在使用されているデバイスと現在使用されていないデバイスの両方が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Finance and Operations and Retail already provide the basic requirements for device management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations および Retail は既に、デバイス管理の基本要求を提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>As you plan your implementation, you must make sure that you take all the appropriate considerations, to help minimize pain and maximize benefit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装を計画するには、問題を最小化して利益を最大化するために、すべての適切な考慮事項が取られるよう確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Implementation considerations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装の考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>This section describes some things that you should consider as you plan to implement features that are related to inventory management in your retail store and distribution locations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、小売店や配送場所での在庫管理に関連する機能を実装する際に考慮すべき事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Generate the physical topology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">物理的トポロジを生成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Planning is the most critical requirement for successful implementation of an enterprise resource planning (ERP) solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画は、エンタープライズ リソース プランニング (ERP) ソリューションの実装を成功させるために最も重要な要件です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>One of the main deliverables of this planning should be a <bpt id="p1">*</bpt>physical topology<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この計画の主な成果物の 1 つは、<bpt id="p1">*</bpt>物理的なトポロジ<ept id="p1">*</ept>である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The physical topology is a visualization of many details about a company, from the lowest POS device to the highest network connections at the headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">物理トポロジは、最下位の POS デバイスから本社の最上位のネットワーク接続までの、会社の多くの詳細の視覚化です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>At a minimum, the following deliverables should be completed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">少なくとも、次の成果物を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Store templates<ept id="p1">**</ept> – A store template consists of one or more diagrams that show the layout of a physical location, such as a brick-and-mortar retail store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>店舗 テンプレート<ept id="p1">**</ept> – 店舗 テンプレートは、ブリック アンド モルタル 小売店舗などの物理的な場所のレイアウトを示す 1 つ以上の図面で構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In the long term, these diagrams help you easily implement future locations and quickly assess how you can fix or improve any issues that are found.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">長期的に、これらの図により、今後の場所を実装しやすくなり、発見された問題を修正または改善する方法を迅速に評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The store template should include the following details:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストア テンプレートには、次の詳細が含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Location<ept id="p1">**</ept> – The physical layout of a location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>場所<ept id="p1">**</ept> – 場所の物理的な配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Details should include the position of all devices that exist in the location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細には、その場所に存在するすべてのデバイスの位置が含まれている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Network<ept id="p1">**</ept> – The internal layout of the network infrastructure and details about internet connectivity (for example, bandwidth up and down, thread count, and latency to the headquarters or other important internet locations).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ネットワーク<ept id="p1">**</ept> – ネットワーク インフラストラクチャの内部レイアウトとインターネット接続に関する詳細 (帯域幅の増減、スレッド数、本社またはその他の重要なインターネットロケーションへの遅延など)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Device<ept id="p1">**</ept> – The details of all devices that exist in a location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> - 場所に存在するすべてのデバイスの詳細。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>These details include the device specifications or some type of associable tag that lets you quickly find the details about a device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの詳細には、デバイスの仕様や、デバイスの詳細をすばやく見つけることができる関連タグのタイプが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Peripheral<ept id="p1">**</ept> – A list of all peripherals that are attached to a device, a count of peripherals, and physical location of all peripherals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>周辺機器<ept id="p1">**</ept> – デバイスに接続されているすべての周辺機器のリスト、周辺機器の数、すべての周辺機器の物理的な位置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Often, there should also be an associable tag that lets you quickly find details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、詳細をすばやく見つけることができる関連付けられたタグも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Naming methodology<ept id="p1">**</ept> – For any implementation, it's important that you maintain naming conventions across all devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前付けの方法<ept id="p1">**</ept> – どの実装でも、すべてのデバイスで命名規則を管理することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Generate the rules that govern the naming conventions, and follow those rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付け規則を決定するルールを生成し、これらの規則に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When you generate the naming methodology, we recommend that the name of a register be the same as, or very similar to, the name of the device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付け方法を生成するとき、レジスターの名前をデバイスの名前と同じにするか、よく似た名前にすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The name of the device, in turn, should be the same as, or very similar to, the friendly name of the physical computer that the register works on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスの名前は、レジスターが動作する物理コンピューターのフレンドリ名と同じか、よく似ていなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>Procedures plan<ept id="p1">**</ept> – The more a business grows, the more important it becomes that procedures remain in place to help maintain enough order so that the business can run efficiently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>手順計画<ept id="p1">**</ept> – ビジネスが成長すればするほど、業務が効率的に実行されるように、十分な注文を維持するための手続きの維持がますます重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>You should consider your plan a living document that you must be maintained and appended often.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ご自分の計画は、頻繁に管理し追加する必要のある随時更新文書だと考えてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>This plan should explain how to perform almost every action that will be repeated in the stores that make up a company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この計画では、企業を構成する店舗で繰り返されるほとんどすべてのアクションをどのように実行するかを説明する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Servicing plan<ept id="p1">**</ept> – As business continues, servicing becomes more critical.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>計画のサービス<ept id="p1">**</ept> – ビジネスが継続するにつれて、サービスはより重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>You must decide when you will replace devices, when you will update devices and peripherals (both the applications and the operating systems), and how you will perform these tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスを交換するとき、デバイスおよび周辺機器 (アプリケーションおよびオペレーティング システムの両方) を更新するとき、およびこれらのタスクを実行する方法を決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The answers will vary from business to business, but these tasks should be planned for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">回答は企業によって異なりますが、これらの作業を計画する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Disaster plan<ept id="p1">**</ept> – If something can go wrong, it should be planned for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>障害計画<ept id="p1">**</ept> - 問題が生じる場合に備えて、計画をする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>As planning proceeds, make a note of risks and potential mitigations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画が進行するにつれて、リスクと潜在的な軽減策を記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Generate a plan that explains how to fix a problematic situation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">疑わしい状態を修正する方法を説明する計画を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>After planning is completed and all potential details are known, you will eventually have a list of stores and, for each store, a list of associated registers and devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画が完了し、すべての潜在的な詳細が分かったら、最終的に店舗のリストと各店舗に関連するレジスターとデバイスのリストを持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The next question that you must answer is how you will deploy all the various devices that are listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">答える必要のある次の質問は、記載されているさまざまなデバイスをすべてどのように配置するかということです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Distributed deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配分配置</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>As the number of devices increases into the hundreds or even thousands, manual configuration, installation, and activation of the POS application quickly becomes impractical.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスの数が数百または数千に増えると、 POS アプリケーションの手動構成、インストール、および有効化が迅速に実行できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>There are several concepts that you can use to alleviate this issue and to manage or help manage devices on a large scale:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を軽減し、大規模なデバイスの管理や管理に役立ついくつかの概念があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">**</bpt>Devices page<ept id="p1">**</ept> – When you use MPOS, the page that shows the details of a device includes information about the POS client that should be used on the device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイス ページ<ept id="p1">**</ept> - MPOS を使用すると、デバイスの詳細を示すページには、デバイス上で使用する必要がある POS クライアントに関する情報が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Under the <bpt id="p1">**</bpt>Register package<ept id="p1">**</ept> subheading, there are four fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レジスター パッケージ<ept id="p1">**</ept> 小見出しの下には、4 つのフィールドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The first three fields (<bpt id="p1">**</bpt>Package name<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Package description<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Version number<ept id="p3">**</ept>) provide information about the version of the MPOS package that should be installed on the device either now or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の 3 つのフィールド (<bpt id="p1">**</bpt>パッケージ名<ept id="p1">**</ept>、<bpt id="p2">**</bpt>パッケージの説明<ept id="p2">**</ept>、<bpt id="p3">**</bpt>バージョン番号<ept id="p3">**</ept>) は、現在または後でデバイスにインストールする必要がある MPOS パッケージのバージョンに関する情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The fourth field shows the version of MPOS that is currently installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 番目のフィールドには、現在インストールされている MPOS のバージョンが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Therefore, you can easily find this information for any device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、どのデバイスでもこの情報を簡単に見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>Channel deployment workspace<ept id="p1">**</ept> – This workspace lets you quickly view a large, filterable set of stores, registers, devices, and more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャンネル配置ワークスペース<ept id="p1">**</ept> - このワークスペースを使用すると、大規模でフィルター設定可能な一連の店舗、レジスター、デバイスなどをすばやく表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This workspace also provides options for mass deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワークスペースには、大規模な展開のオプションも用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>(For more information, see <bpt id="p1">[</bpt>Mass Deployment<ept id="p1">](dev-itpro/retail-mass-deployment.md)</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(詳細については、<bpt id="p1">[</bpt>一括配置<ept id="p1">](dev-itpro/retail-mass-deployment.md)</ept> を参照してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This workspace gives you quick access to important pages, can help decrease validation times when you do status checks are a deployment, and helps you efficiently manage device statuses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワークスペースを使用すると、重要なページにすばやくアクセスしたり、展開時のステータス チェックを減らしたり、デバイス状態を効率的に管理したりするのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Mass deployment<ept id="p1">**</ept> – Microsoft Dynamics 365 customers who use MPOS and other client-side components can silently perform various actions to help with installation, configuration, and servicing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一括配置<ept id="p1">**</ept> – MPOS およびその他のクライアント側コンポーネントを使用する Microsoft Dynamics 365 の顧客は、インストール、コンフィギュレーション、およびサービスを支援するさまざまなアクションをサイレントで実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>By running basic commands at a command prompt, you might be able to deploy and service (that is, update) retail components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド プロンプトで基本的なコマンドを実行すると、小売コンポーネントを配置してサービスする (つまり、更新する) ことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This basic method of skipping the installer's manual user interface can reduce the time that is required for installation and servicing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーの手動ユーザー インターフェイスをスキップするこの基本的な方法は、インストールおよびサービスに必要な時間を短縮できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The log files remain the same and can be viewed for installation details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ログ ファイルは同じままであり、インストールの詳細を表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">**</bpt>Scripting<ept id="p1">**</ept> – Based on the mass deployment functionality, scripts can be generated and set up to run automatically to install or update retail components such as MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スクリプティング<ept id="p1">**</ept> – 大規模な展開機能に基づいて、スクリプトは生成され、インストールまたは MPOS などの小売コンポーネントの更新を自動的に実行するために設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>These basic scripts can be entered as a scheduled task on a device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの基本スクリプトは、デバイス上でスケジュールされたタスクとして入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The task then runs at a predetermined time and return the logs and results to a predetermined location, where they can be viewed as time permits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、タスクは所定の時間に実行され、ログおよび結果を所定の場所に返します。ここでは、時間が許す限り閲覧することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source><bpt id="p1">**</bpt>Systems management solution<ept id="p1">**</ept> – A systems management solution can help increase the amount of known data about the devices that are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理ソリューション<ept id="p1">**</ept> – システム管理ソリューションは、使用されているデバイスに関する既知のデータ量を増やすのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>It can also decrease the time that is required in order to get that data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、そのデータを取得するために必要な時間を減少させることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Examples of systems management solutions include Microsoft System Center and Microsoft InTune.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム管理ソリューションの例には、Microsoft System Center および Microsoft InTune が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>By using a systems management solution together with mass deployment and scripting, you can configure and install retail components much more quickly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一括配置とスクリプトと共にシステム管理ソリューションを使用することで、小売コンポーネントをより迅速に設定およびインストールすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In addition, you can more efficiently validate status after deployment or servicing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、配置または処理後のステータスをより効率的に検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Microsoft has published a document specifically about device management via System Center Configuration Manager, <bpt id="p1">[</bpt>Choose a device management solution for System Center Configuration Manager<ept id="p1">](https://docs.microsoft.com/sccm/core/plan-design/choose-a-device-management-solution)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、System Center Configuration Manager 経由でのデバイス管理に関する具体的なドキュメントである <bpt id="p1">[</bpt>System Center Configuration Manager のデバイス管理ソリューションの選択<ept id="p1">](https://docs.microsoft.com/sccm/core/plan-design/choose-a-device-management-solution)</ept>を発行しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For more information that will help you better understand distributed deployment, see <bpt id="p1">[</bpt>Retail Modern POS configuration and installation<ept id="p1">](retail-modern-pos-device-activation.md)</ept> and <bpt id="p2">[</bpt>Mass Deployment<ept id="p2">](dev-itpro/retail-mass-deployment.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配分配置をより理解するのに役立つ情報の詳細については、「<bpt id="p1">[</bpt>Retail Modern POS のコンフィギュレーションとインストール<ept id="p1">](retail-modern-pos-device-activation.md)</ept>」および「<bpt id="p2">[</bpt>一括配置<ept id="p2">](dev-itpro/retail-mass-deployment.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Servicing devices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスの保守</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Although deployment is an important topic that has many nuances, the ongoing nature of business requires that you consider servicing early, and that you plan for it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開は重要なトピックで多くのニュアンスを持ってはいますが、ビジネスの継続的な特性は早い段階でサービスを考慮すること、またそれを計画をすることが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In that way, you can maximize efficiency and speed of completion every time that servicing is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、そのサービスの提供が必要な場合はいつでも完了の効率性と速度を最大限にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Servicing becomes even more important when you understand that, not only do applications have to be serviced, but the operating system and peripherals might also require updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスは、アプリケーションを保守するだけでなく、オペレーティング システムと周辺機器の更新も求められることを理解すると、さらに重要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>As we mentioned earlier, this process can be even more difficult when it's time to replace devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先に述べたように、このプロセスはデバイスの置換時期になるとさらに困難になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In general, you should consider all the following factors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、次のすべての要因を考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> – The process of servicing a device involves more than just determining whether servicing has been completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> - デバイスをサービスするプロセスは、サービスが完了したかどうかを判断するだけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Instead, many aspects of the device must be reviewed and updated, either individually or as part of a group of devices at the same time:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、デバイスのさまざまな側面を個別または同時にデバイスのグループの一部として確認および更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The information on the <bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> page, or in the <bpt id="p2">**</bpt>Channel deployment<ept id="p2">**</ept> workspace, in Microsoft Dynamics 365 headquarters can help you validate the current status and version of MPOS or other self-service components, such as hardware station or Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 バックオフィスの<bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> ページまたは<bpt id="p2">**</bpt>チャンネル配置<ept id="p2">**</ept>ワークスペースの情報は、MPOS またはハードウェア ステーションや Retail Store Scale Unit などのその他のセルフサービス コンポーネントの現在のステータスとバージョンを検証するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>It's very useful if you know the version of Microsoft Windows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows のバージョンがわかっている場合は非常に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>In scenarios where a systems management solution isn't used, you can use the <bpt id="p1">**</bpt>winver<ept id="p1">**</ept> command in a Command Prompt window to quickly learn the specific version of Windows that is currently installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム管理ソリューションが使用されていないシナリオでは、コマンド プロンプト ウィンドウで <bpt id="p1">**</bpt>winver<ept id="p1">**</ept> コマンドを使用して現在インストールされている Windows の特定のバージョンをすぐに確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>By comparing the version number against the <bpt id="p1">[</bpt>Windows version list<ept id="p1">](https://technet.microsoft.com/windows/release-info.aspx)</ept>, you can easily learn what updates a computer is missing at a service pack level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Windows のバージョン リスト<ept id="p1">](https://technet.microsoft.com/windows/release-info.aspx)</ept>と照らしてバージョン番号を比較することにより、サービス パック レベルでコンピューターの更新に不足しているものが何かを容易に理解できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Internal and peripheral drivers must be checked for version updates too.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内部および周辺機器ドライバーもバージョンの更新を確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You should include and monitor this information in the device and peripheral lists that you created as part of the store templates during the planning phase, as explained earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本トピックの前半で説明したように、計画フェーズ中にストア テンプレートの一部として作成したこの情報を、デバイスと周辺機器のリストに収録して監視する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Always track when a computer goes out of service (warranty or service plan).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常にコンピューターがサービス (保証またはサービス プラン) を停止した場合に追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In this way, you can quickly determine when a computer should be replaced instead of being sent out for servicing (warranty or service plan).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、サービス (保証またはサービス プラン) に送信せずに、いつコンピューターを置換する必要があるかをすばやく決定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">**</bpt>Peripherals<ept id="p1">**</ept> – The peripherals that are attached to a device or to the network must be monitored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>周辺機器<ept id="p1">**</ept> – デバイスまたはネットワークに関連付けられている周辺機器を監視する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>As part of this process, you must also monitor the network devices themselves.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスの一環として、ネットワーク デバイス自体も監視する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>(Routers, switches, firewalls, and all other network devices also have firmware that requires occasional updates to maintain security and compatibility, and to comply with servicing terms.) If appropriate planning has occurred, the process of watching for service dates and correctly updating peripherals should become a simplified task within the larger servicing flow for device management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ルーター、スイッチ、ファイアウォール、およびその他のネットワーク デバイスには、セキュリティと互換性を維持し、サービス条件に準拠するために、時折更新が必要なファームウェアもあります。) 適切な計画が立てられた場合、サービスの日付を監視し、周辺機器を正しく更新するプロセスは、デバイス管理のためのより大きなサービス フローの中で簡略化されたタスクになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">**</bpt>Replacements<ept id="p1">**</ept> – Eventually, devices and peripherals either fail or reach a point where servicing just isn't enough.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>交換<ept id="p1">**</ept> – 最終的にデバイスおよび周辺機器は、不合格またはサービスに不十分な状態となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>In general, we highly recommended that you have a replacement system that is ready before this situation arises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、この状況が発生する前に代替システムを準備することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Based on the procedures and servicing plans that you created during the planning phase, this process can be very fast and efficient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画フェーズ中に作成した手順とサービス計画に基づいて、このプロセスは非常に迅速かつ効率的に行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>For a device that runs MPOS, you can generically prepare the replacement device and install MPOS on it long before you either send the unit on-site or store it on-site, depending on the approach that works best for the business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS を実行するデバイスで、通常ビジネスに最も適した方法に応じて、単位をオンサイトに送信するか保存するよりずっと以前に交換用デバイスを準備し、MPOS をインストールすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>At the time of replacement, MPOS can "reactivate" a device that is already active.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">交換時に MPOS は既に有効になっているデバイスを「再有効化」することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Therefore, you can handle special cases where a system stops responding and must be replaced, because it can't be repaired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、システムが応答を停止し、修復できないため交換する必要がある特殊なケースを処理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>However, you must make sure that the replacement is correctly up to date, and that it has recently been serviced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、交換品が正確に最新のものとなっており、最近修理されたことを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">**</bpt>Systems management solution<ept id="p1">**</ept> – A systems management solution can dramatically improve how servicing works and when servicing is done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理ソリューション<ept id="p1">**</ept> – システム管理ソリューションはサービスの方法やサービスが完了する時を大幅に向上します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>These solutions include telemetry tools that monitor all the systems that are being used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのソリューションには、使用されているすべてのシステムを監視する遠隔測定ツールが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Because of these telemetry tools and the device information data that is constantly stored and available, servicing should become proactive instead of reactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのテレメトリ ツールと常に保存され利用可能なデバイスの情報データにより、サービスはリアクティブではなくプロアクティブになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>In this best-case scenario, appropriate plans exist for procedures and servicing, and the alerts and the known data about a system can let you know about impending servicing or an impending replacement before an issue occurs and becomes a critical task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この最良のシナリオでは、適切なプランが手順およびサービスに対して存在し、システムに関する警告および既知のデータによって、問題が発生して重要なタスクになる前に間もなく稼働または交換が発生することを把握できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Worst-case scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最悪のシナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Unfortunately, things sometimes go wrong.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ときには問題が生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>It's important that you consider worst-case scenarios and put mitigation plans in place (per the disaster plan that you created during the planning phase) to help resolve issues that arise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最悪のシナリオを検討し、発生する問題の解決に役立つ軽減計画を (計画フェーズで作成した障害計画に従って) 配置することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>In Finance and Operations and Retail, the <bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> page can at least help with device management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations および Retail で、<bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> ページは少なくともデバイス管理に役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source><bpt id="p1">**</bpt>Lost/stolen device<ept id="p1">**</ept> – When a device is lost or stolen, it becomes a critical issue, because private data can end up in the hands of a malicious person.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイスの紛失または盗難<ept id="p1">**</ept> – プライベートなデータが悪意のある人の手に渡ってしまう可能性があるため、デバイスを紛失または盗難すると重大な問題になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The first step is to deactivate any lost or stolen device on the <bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> page in Microsoft Dynamics 365 headquarters, to immediately prevent sign-on to that device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まず、Microsoft Dynamics 365 バックオフィスの <bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> ページでデバイスの紛失または盗難を無効にし、すぐにそのデバイスにはサインオンできないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If you created a disaster plan, follow the rest of the guidelines to complete all tasks that are required in order to tag the device as gone, file all important documents (which might include documents for insurance and the police), and work to replace the device and continue business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">災害対策を作成した場合は、残りのガイドラインに従って、デバイスにタグを付けるために必要なすべての作業を完了し、重要なすべての文書 (保険証書と警察用の文書が含まれている可能性があります) を提出し、デバイスを交換しビジネスを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>If appropriate procedures have been created, a replacement device should already be ready.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な手順が作成された場合は、交換用のデバイスの準備が完了している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source><bpt id="p1">**</bpt>Infrastructure issues<ept id="p1">**</ept> – Network equipment might go bad, the store layout might have to be altered, or, as a part of a store update, the devices might be changed from desktops to tablets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャの問題<ept id="p1">**</ept> – ネットワーク機器に不具合が発生したり、店舗レイアウトを変更する必要があるか、店舗アップデートの一環として、デバイスがデスクトップからタブレットに変更される可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>When issues arise that can affect the management of devices, it can be difficult to react appropriately and fix the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスの管理に影響する可能性のある問題が発生したとき、問題に適切に対応し、問題を修正することが困難なことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>In the best-case scenario, you've already discussed these issues and listed then in the procedures, servicing, and disaster plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最良のシナリオでは、既にこれらの問題について話し合い、手順、サービス、および障害計画にリストされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>At a minimum, before something is done that affects the layout of a business location, you should update the store layout documents to reflect the new layout, so that fewer surprises are met.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">少なくとも、業務場所のレイアウトに影響を与える何かが行われる前に、新しいレイアウトを反映するように店舗レイアウト ドキュメントを更新することで意外性を少なくすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>As we mentioned earlier, for issues that affect MPOS specifically, the ability to reactivate should help mitigate downtime and should help with change management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先に述べたように、具体的に MPOS に影響を与える問題に対して、再有効化する機能はダウンタイムを軽減するのに役立ち、変更管理に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>If you're concerned about outages of network equipment, or if outages occur, the MPOS client can support offline databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワーク装置の停止が懸念される場合、または停止が発生した場合、MPOS クライアントでオフライン データベースをサポートすることは可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>This functionality can help mitigate the impact that outages have on business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、障害が業務に与える影響を軽減するために役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source><bpt id="p1">**</bpt>Disaster<ept id="p1">**</ept> – When a disaster occurs, everything is affected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>障害<ept id="p1">**</ept> - 障害が発生すると、すべてが影響を受けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If the disaster is environmental, the employees should always be the highest priority.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">災害が環境にある場合、従業員が常に最優先される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>However, eventually, you must handle the management of the internal systems, and those systems must be repaired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、最終的には、内部システムの管理を処理する必要があり、それらのシステムを修復する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Unfortunately, no simple advice or specific considerations can be listed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、単純な通知または特定の考慮事項は表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Instead, you should plan early in a more general way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、より一般的な形で早く計画する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>What sorts of disasters could affect the business?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのような災害が業務に影響を与える恐れがありますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Utilities such as water and power can have devastating effects on equipment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">水や電力などの公共事業は、設備に致命的な影響を与える可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>How can you mitigate the effects on employees, locations, and equipment in various disasters?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな災害下で従業員、場所、および設備への影響をどのように緩和できますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Keep in mind concepts such as the data that is stored in the location, and when and how it's backed up and secured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場所に格納されているデータ、およびいつどのようにバックアップしてセキュリティで保護されたかなどに留意してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>