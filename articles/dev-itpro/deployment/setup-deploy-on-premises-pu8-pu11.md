<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="setup-deploy-on-premises-pu8-pu11.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>setup-deploy-on-premises-pu8-pu11.1139d0.c795d9eb499ffa07b2d6289627f8ef8f509ebdef.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c795d9eb499ffa07b2d6289627f8ef8f509ebdef</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\setup-deploy-on-premises-pu8-pu11.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up and deploy on-premises environments (Platform updates 8 and 11)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to plan, set up, and deploy an on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、オンプレミス環境の計画、設定、および展開方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up and deploy on-premises environments (Platform updates 8 and 11)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes how to plan your deployment, set up the infrastructure, and deploy Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises), Platform updates 8 and 11.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、展開を計画し、インフラストラクチャを設定し、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (オンプレミス)、プラットフォーム更新プログラム 8 および 11 を展開する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic applies only to deploying on-premises environments on Platform updates 8 and 11.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、プラットフォーム更新プログラム 8 および 11 にオンプレミス環境を展開する場合にのみ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For information about deploying to Platform update 12, see <bpt id="p1">[</bpt>Set up and deploy on premises environments (Platform update 12<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 12 への配置方法の詳細については、<bpt id="p1">[</bpt>オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12)<ept id="p1">](setup-deploy-on-premises-pu12.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Finance and Operations components</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のコンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The Finance and Operations application consists of three main components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Business Intelligence (BI)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス (BI)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Financial Reporting/Management Reporter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務レポート/管理レポーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>These components depend on the following system software:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのコンポーネントは、次のシステム ソフトウェアによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Microsoft Windows Server 2016</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows サーバー 2016</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Microsoft SQL Server 2016 SP1, which has the following features:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の特徴を有する Microsoft SQL Server2016 SP1:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Full-text index search is enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フルテキスト インデックス検索が有効にされている。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>SQL Server Reporting Services (SSRS) - This is deployed on BI virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>SQL Server Integration Services (SSIS) - This is deployed on AOS virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Full Text Search must be enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なテキスト検索を有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>SQL Server Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Standalone Microsoft Azure Service Fabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタンドアロン Microsoft Azure Service Fabric</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Microsoft Windows PowerShell 5.0 or later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows PowerShell 5.0 以降</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Active Directory Federation Services (AD FS) on Windows Server 2016</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2016 での Active Directory Federation Services (AD FS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Domain controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The domain controller must be Microsoft Windows Server 2012 R2 or later and must have a domain functional level of 2012 R2 or more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about domain functional levels, see the following topics:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン機能レベルの詳細については、次のトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>What Are Active Directory Functional Levels<ept id="p1">](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Active Directory 機能レベルとは<ept id="p1">](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Understanding Active Directory Domain Services Functional Levels<ept id="p1">](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Active Directory ドメイン サービス機能のレベルを理解する<ept id="p1">](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Lifecycle Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Finance and Operations bits are distributed through Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Before you can deploy, you must purchase license keys through the <bpt id="p1">[</bpt>Enterprise Agreements<ept id="p1">](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx)</ept> channel and set up an on-premises project in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置する前に、<bpt id="p1">[</bpt>エンタープライズ契約<ept id="p1">](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx)</ept> チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Deployments can be initiated only through LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS からのみ配置を開始することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For more information about how to set up on-premises projects in LCS, see <bpt id="p1">[</bpt>Create an on-premises project in Lifecycle Services<ept id="p1">](../lifecycle-services/lbd-create-lcs-on-prem-project.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でオンプレミス プロジェクトを設定する方法の詳細については、<bpt id="p1">[</bpt>Lifecycle Services でのオンプレミス プロジェクトの作成<ept id="p1">](../lifecycle-services/lbd-create-lcs-on-prem-project.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Authentication</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The on-premises application works with AD FS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス アプリケーションは AD FS で動作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To interact with LCS, you must also configure Azure Active Directory (AAD).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>And, to complete the deployment and configure the LCS Local agent, you will need AAD.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置を完了し LCS ローカル エージェントを構成するには、AAD が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Standalone Service Fabric</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Standalone Service Fabric</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Finance and Operations uses standalone Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は スタンドアロン Service Fabric を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For more information, see the <bpt id="p1">[</bpt>Service Fabric documentation<ept id="p1">](/azure/service-fabric/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Service Fabric ドキュメント<ept id="p1">](/azure/service-fabric/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Setup of Finance and Operations will deploy a set of applications inside Service Fabric (SF).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>During deployment, each node in the cluster will be defined via configuration to have one of the following node types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>AOSNodeType<ept id="p1">**</ept>: Hosts the application object server (business logic).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AOSNodeType<ept id="p1">**</ept>: アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept>: Functions as Service Fabric primary nodes, and hosts deployment- and servicing logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept>: Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>ReportServerType<ept id="p1">**</ept>: Hosts SSRS and reporting logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ReportServerType<ept id="p1">**</ept>: SSRS およびレポート ロジックをホストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>MRType<ept id="p1">**</ept>: Hosts management reporting logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MRType<ept id="p1">**</ept>: 管理レポート ロジックをホストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Infrastructure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インフラストラクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Finance and Operations is designed to work on a Hyper-V virtualized environment that is based on Windows Servers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、Windows Server に基づく Hyper-V 仮想化環境で作業するよう設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>On-premises deployments of Microsoft Dynamics 365 for Finance and Operations are not supported on any public cloud infrastructure, including Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The hardware configuration includes the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア構成には、次のコンポーネントが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Standalone Service Fabric cluster that is based on Windows Server 2016 virtual machines (VMs)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="2">Windows Server</ph> 2016 仮想マシン (VM) に基づく Standalone <ph id="1">Service Fabric Cluster</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Microsoft SQL Server (both Clustered SQL and Always-On are supported)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>AD FS for authentication</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証のための AD FS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Server Message Block (SMB) version 3 file share for storage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Optional: Microsoft Office Server 2017</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: Microsoft Office Server 2017</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For more information, see <bpt id="p1">[</bpt>System requirements<ept id="p1">](../../fin-and-ops/get-started/system-requirements-on-prem.md)</ept> and Sizing guidelines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>システム要求<ept id="p1">](../../fin-and-ops/get-started/system-requirements-on-prem.md)</ept> およびサイジングのガイドラインを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Hardware layout</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェア レイアウト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Plan your infrastructure and Service Fabric cluster based on the recommended sizing in <bpt id="p1">[</bpt>Hardware sizing for on-premises environments<ept id="p1">](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オンプレミス環境のハードウェア サイジング<ept id="p1">](../../fin-and-ops/get-started/hardware-sizing-on-premises-environments.md)</ept> で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric クラスターを計画します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For more information about how to plan the Service Fabric cluster, see <bpt id="p1">[</bpt>Plan and prepare your Service Fabric standalone cluster deployment<ept id="p1">](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターを計画する方法の詳細については、<bpt id="p1">[</bpt>Service Fabric のスタンドアロン クラスター展開の計画と準備<ept id="p1">](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The following table shows an example of a hardware layout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、ハードウェア レイアウトの例を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This example is used throughout this topic to illustrate the setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は、設定を説明するためにこのトピック全体で使用されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The Primary node of the Service Fabric cluster must have at least three nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In this example, <bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept> is designated as the Primary node type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では <bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept> を主要なノード タイプとして指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Machine purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マシンの目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>SF Node type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SF ノード タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Machine name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューター名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>IP address</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IP アドレス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Domain controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>DAX7SQLAODC1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAODC1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>10.179.108.2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>AD FS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>DAX7SQLAOADFS1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAOADFS1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>10.179.108.3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>File server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>DAX7SQLAOFILE1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAOFILE1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>10.179.108.4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>SQL Always-On cluster</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Always-On クラスター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>DAX7SQLAOSQLA01</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAOSQLA01</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>10.179.108.5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>DAX7SQLAOSQLA02</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAOSQLA02</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>10.179.108.6</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.6</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>DAX7SQLAOSQLA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DAX7SQLAOSQLA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>10.179.108.9</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.9</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>SQLAOCLIENT1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOCLIENT1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>10.179.108.11</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.11</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>AOS 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>AOSNodeType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOSNodeType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>SQLAOSF1AOS1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1AOS1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>10.179.108.12</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.12</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>AOS 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>AOSNodeType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOSNodeType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>SQLAOSF1AOS2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1AOS2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>10.179.108.13</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.13</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>AOS 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>AOSNodeType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOSNodeType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>SQLAOSF1AOS3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1AOS3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>10.179.108.14</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.14</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Orchestrator 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>OrchestratorType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestratorType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>SQLAOSF1ORCH1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1ORCH1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>10.179.108.15</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Orchestrator 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>OrchestratorType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestratorType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>SQLAOSF1ORCH2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1ORCH2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>10.179.108.16</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Orchestrator 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーケストレータ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>OrchestratorType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestratorType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>SQLAOSF1ORCH3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSF1ORCH3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>10.179.108.17</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.17</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Management Reporter node</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter ノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>MRType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MRType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>SQLAOSMR1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSMR1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>10.179.108.18</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.18</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>SSRS node</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSRS ノード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>ReportServerType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ReportServerType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>SQLAOSFBIN1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLAOSFBIN1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>10.179.108.10</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10.179.108.10</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">段取り</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Before you start the setup, the following prerequisites must be in place.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップを開始する前に、次の前提条件が満たされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The setup of these prerequisites is out of scope for this document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの前提条件の設定は、このドキュメントの範囲外です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Active Directory Domain Services (AD DS) must be installed and configured in your network.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>AD FS must be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS は、展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>SQL Server 2016 SP1 must be installed on the SSRS machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 2016 SP1 は SSRS コンピューターにインストールされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>SQL Server Reporting Services 2016 must be installed in <bpt id="p1">**</bpt>Native<ept id="p1">**</ept> mode on the SSRS machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services 2016 は、SSRS コンピューターに<bpt id="p1">**</bpt>ネイティブ<ept id="p1">**</ept> モードでインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The following prerequisite software is installed on the VMs by the infrastructure setup scripts downloaded from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Node type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノード タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>SNAC – ODBC driver</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SNAC – ODBC ドライバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft .NET Framework version 2.0–3.5 (CLR 2.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><bpt id="p1">**</bpt>Windows Features:<ept id="p1">**</ept> NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft .NET Framework version 4.0–4.6 (CLR 4.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source><bpt id="p1">**</bpt>Windows Features:<ept id="p1">**</ept> NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><bpt id="p1">**</bpt>Windows Features:<ept id="p1">**</ept> WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs, Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept>WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>SQL Server Management Studio 17.2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio 17.2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Microsoft Access Database Engine 2010 Redistributable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>BI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>.NET Framework version 2.0–3.5 (CLR 2.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Framework version 2.0–3.5 (CLR 2.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">**</bpt>Windows features:<ept id="p1">**</ept> NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>BI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>.NET Framework version 4.0–4.6 (CLR 4.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Framework version 4.0–4.6 (CLR 4.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source><bpt id="p1">**</bpt>Windows features:<ept id="p1">**</ept> NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>BI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>SQL Server Management Studio 17.2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio 17.2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>MR</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MR</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>.NET Framework version 2.0–3.5 (CLR 2.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Framework version 2.0–3.5 (CLR 2.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source><bpt id="p1">**</bpt>Windows features:<ept id="p1">**</ept> NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>MR</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MR</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>.NET Framework version 4.0–4.6 (CLR 4.0)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Framework version 4.0–4.6 (CLR 4.0)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Windows features:<ept id="p1">**</ept> NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Windows の機能:<ept id="p1">**</ept> NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>MR</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MR</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Visual C++ Redistributable Packages for Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The following steps must be completed to set up the infrastructure for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt>Plan your domain name and DNS zones<ept id="p1">](#plandomain)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ドメイン名と DNS ゾーンの計画<ept id="p1">](#plandomain)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">[</bpt>Plan and acquire your certificates<ept id="p1">](#plancert)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>証明書の計画と取得<ept id="p1">](#plancert)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source><bpt id="p1">[</bpt>Plan your users and service accounts<ept id="p1">](#plansvcacct)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ユーザーとサービス アカウントの計画<ept id="p1">](#plansvcacct)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source><bpt id="p1">[</bpt>Create DNS zones, and add A records<ept id="p1">](#createdns)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>DNS ゾーンの作成と A レコードの追加<ept id="p1">](#createdns)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">[</bpt>Join VMs to the domain<ept id="p1">](#joindomain)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>VM のドメインへの参加<ept id="p1">](#joindomain)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source><bpt id="p1">[</bpt>Download setup scripts from LCS<ept id="p1">](#downloadscripts)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS からセットアップ スクリプトのダウンロード<ept id="p1">](#downloadscripts)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source><bpt id="p1">[</bpt>Describe your configuration<ept id="p1">](#describeconfig)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>コンフィギュレーションの記述<ept id="p1">](#describeconfig)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source><bpt id="p1">[</bpt>Configure certificates<ept id="p1">](#configurecert)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>証明書の構成<ept id="p1">](#configurecert)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source><bpt id="p1">[</bpt>Setup VMs<ept id="p1">](#setupvms)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>VM を設定する<ept id="p1">](#setupvms)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">[</bpt>Set up a standalone Service Fabric cluster<ept id="p1">](#setupsfcluster)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>スタンドアロン Service Fabric クラスターの設定<ept id="p1">](#setupsfcluster)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source><bpt id="p1">[</bpt>Configure LCS connectivity for the tenant<ept id="p1">](#configurelcs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>テナント用 LCS 接続の構成<ept id="p1">](#configurelcs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt>Set up file storage<ept id="p1">](#setupfile)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ファイル ストレージの設定<ept id="p1">](#setupfile)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source><bpt id="p1">[</bpt>Set up SQL Server<ept id="p1">](#setupsql)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SQL Server の設定<ept id="p1">](#setupsql)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source><bpt id="p1">[</bpt>Configure the databases<ept id="p1">](#configuredb)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>データベースを構成する<ept id="p1">](#configuredb)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source><bpt id="p1">[</bpt>Encrypt credentials<ept id="p1">](#encryptcred)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>資格情報の暗号化<ept id="p1">](#encryptcred)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source><bpt id="p1">[</bpt>Set up SSIS<ept id="p1">](#setupssis)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>資産除去債務 (SSIS) の設定<ept id="p1">](#setupssis)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt>Set up SSRS<ept id="p1">](#setupssrs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>資産除去債務 (SSRS) の設定<ept id="p1">](#setupssrs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source><bpt id="p1">[</bpt>Configure AD FS<ept id="p1">](#configureadfs)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>AD FS のコンフィギュレーション<ept id="p1">](#configureadfs)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source><bpt id="p1">[</bpt>Configure a connector and install an on-premises local agent<ept id="p1">](#configureconnector)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>コネクタを構成し、オンプレミスのローカル エージェントをインストールする<ept id="p1">](#configureconnector)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source><bpt id="p1">[</bpt>Deploy your Finance and Operations (on-premises) environment from LCS<ept id="p1">](#deploy)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS から Finance and Operations (オンプレミス) 環境を配置する<ept id="p1">](#deploy)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source><bpt id="p1">[</bpt>Connect to your Finance and Operations (on-premises) environment<ept id="p1">](#connect)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Finance and Operations (オンプレミス) 環境に接続する<ept id="p1">](#connect)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source><bpt id="p1">&lt;a name="plandomain"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 1. Plan your domain name and DNS zones</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="plandomain"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 1. ドメイン名と DNS ゾーンの計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>We recommend that you use a publicly registered domain name for your production installation of AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>In that way, the installation can be accessed outside the network, if outside access is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>For example, if your company's domain is contoso.com, your zone for Finance and Operations (on-premises) might be d365ffo.onprem.contoso.com, and the host names might be as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、会社のドメインが contoso.com の場合、Finance and Operations (オンプレミス) は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>ax.d365ffo.onprem.contoso.com for AOS machines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS の機械の場合 ax.d365ffo.onprem.contoso.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>sf.d365ffo.onprem.contoso.com for the Service Fabric cluster</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source><bpt id="p1">&lt;a name="plancert"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 2. Plan and acquire your certificates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="plancert"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 2. 証明書の計画と取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Secure Sockets Layer (SSL) certificates are required in order to secure a Service Fabric cluster and all the applications that are deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>For your production and sandbox workloads, we recommend that you acquire certificates from a certificate authority (CA) such as <bpt id="p1">[</bpt>DigiCert<ept id="p1">](https://www.digicert.com/ssl-certificate/)</ept>, <bpt id="p2">[</bpt>Comodo<ept id="p2">](https://ssl.comodo.com/)</ept>, <bpt id="p3">[</bpt>Symantec<ept id="p3">](https://www.websecurity.symantec.com/ssl-certificate)</ept>, <bpt id="p4">[</bpt>GoDaddy<ept id="p4">](https://www.godaddy.com/web-security/ssl-certificate)</ept>, or <bpt id="p5">[</bpt>GlobalSign<ept id="p5">](https://www.globalsign.com/en/ssl/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロダクションとサンドボックスのワークロードについては、<bpt id="p1">[</bpt>DigiCert<ept id="p1">](https://www.digicert.com/ssl-certificate/)</ept>、<bpt id="p2">[</bpt>Comodo<ept id="p2">](https://ssl.comodo.com/)</ept>、<bpt id="p3">[</bpt>Symantec<ept id="p3">](https://www.websecurity.symantec.com/ssl-certificate)</ept>、<bpt id="p4">[</bpt>GoDaddy<ept id="p4">](https://www.godaddy.com/web-security/ssl-certificate)</ept>、または <bpt id="p5">[</bpt>GlobalSign<ept id="p5">](https://www.globalsign.com/en/ssl/)</ept> などの認証局から証明書を取得することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>If your domain is set up with <bpt id="p1">[</bpt>Active Directory Certificate Services<ept id="p1">](https://technet.microsoft.com/library/cc772393(v=ws.10).aspx)</ept> (AD CS), you can create the certificates through AD CS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメインが <bpt id="p1">[</bpt>Active Directory 証明書サービス<ept id="p1">](https://technet.microsoft.com/library/cc772393(v=ws.10).aspx)</ept> (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Each certificate must contain a private key that was created for key exchange, and it must be exportable to a Personal Information Exchange (.pfx) file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Self-signed certificates can be used only for testing purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自己署名証明書は、テスト目的でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>For convenience, the setup scripts include scripts that generate and export self-signed certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">便宜上、セットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>As we've mentioned, these certificates can be used for testing purposes only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">先に述べたように、これらの証明書はテスト目的でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Explanation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additional requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>SQL Server SSL certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server SSL 証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>This certificate is used to encrypt data that is transmitted across a network between an instance of SQL Server and a client application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>The domain name of the certificate should match the fully-qualified domain name (FQDN) of the SQL Server instance or listener.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の場合、ドメイン名は、SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>For example, if the SQL listener is hosted on the machine DAX7SQLAOSQLA, the certificate's DNS name is DAX7SQLAOSQLA.onprem.contoso.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.onprem.contoso.com です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Service Fabric Server certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Server 証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>This certificate is used to help secure the node-to-node communication between the Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>This certificate is also used as the Server certificate that is presented to the client that connects to the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>You can use the SSL wild card certificate of your domain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメインの SSL ワイルドカード証明書を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For example, <ph id="ph1">\*</ph>.contoso.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">\*</ph>.contoso.com です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note:<ept id="p1">&lt;/strong&gt;</ept> The wild card certificate allows you to secure only the first level subdomain of the domain to which it is issued.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>In this example, because your service fabric domain is sf.d365ffo.onprem.contoso.com, you must include this as a Subject Alternative Name (SAN) in the certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、Service Fabric ドメインが sf.d365ffo.onprem.contoso.com であるため、証明書にサブジェクト代替名 (SAN) としてこれを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>You will need to work with your certificate authority to acquire the additional SANs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明機関と連携して、追加の SAN を取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Service Fabric Client certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric Client 証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>This certificate is used by clients to view and manage the Service Fabric cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Encipherment Certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の暗号化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>This certificate is used to encrypt sensitive information such as the SQL Server password and user account passwords.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The certificate must be created by using the provider <bpt id="p1">**</bpt>Microsoft Enhanced Cryptographic Provider v1.0<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書は、プロバイダー <bpt id="p1">**</bpt>Microsoft Enhanced Cryptographic Provider v1.0<ept id="p1">**</ept> を使用して作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>The certificate key usage must include Data Encipherment (10) and should not include Server authentication or Client authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>For more information, see <bpt id="p1">[</bpt>Managing secrets in Service Fabric applications<ept id="p1">](/azure/service-fabric/service-fabric-application-secret-management)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Service Fabric アプリケーションでの機密情報の管理<ept id="p1">](/azure/service-fabric/service-fabric-application-secret-management)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>AOS SSL Certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS SSL 証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>This certificate is used as the Server certificate that is presented to the client for the AOS website.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>It's also used to enable Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can use the same wild card certificate that you used as the Service Fabric Server certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>In this example, the domain name ax.d365ffo.onprem.contoso.com must be added to the Subject Alternative Name (SAN) as in the Service  Fabric Server certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ドメイン名 ax.d365ffo.onprem.contoso.com を、Service Fabric Server 証明書としてサブジェクト代替名 (SAN) に追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Session Authentication certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セッション認証証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This certificate is used by AOS to help secure a user's session information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、AOS がユーザーのセッション情報を保護するために使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>This certificate is also the File Share certificate that will used at the time of deployment from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Data Encryption certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの暗号化証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>This certificate is used by the AOS to encrypt sensitive information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>This must be created using the provider <bpt id="p1">**</bpt>Microsoft Enhanced RSA and AES Cryptographic Provider<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはプロバイダー <bpt id="p1">**</bpt>Microsoft Enhanced RSA および AES Cryptographic Provider<ept id="p1">**</ept> を使用して作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Data Signing certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ署名の証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>This certificate is used by AOS to encrypt sensitive information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの証明書は、機密情報を暗号化するために AOS によって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>This is separate from the Data Encryption certificate and must be created using the provider <bpt id="p1">**</bpt>Microsoft Enhanced RSA and AES Cryptographic Provider<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、データ暗号化証明書とは別のもので、プロバイダー<bpt id="p1">**</bpt>Microsoft の拡張された RSA および AES 暗号化プロバイダー<ept id="p1">**</ept>を使用して作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Financial Reporting client certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務報告クライアント証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This certificate is used to help secure the communication between the Financial Reporting services and the AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Reporting certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">報告証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>This certificate is used to help secure the communication between SSRS and the AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書を使用して、SSRS と AOS 間の通信を保護します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source><bpt id="p1">**</bpt>Do not reuse the Financial Reporting Client certificate.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>財務報告クライアント証明書を再利用しないでください。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>On-Premise local agent certificate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス ローカル エージェント証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>This certificate is used to help secure the communication between a local agent that is hosted on-premises and on LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>This certificate enables the local agent to act on behalf of your Azure AD tenant, and to communicate with LCS to orchestrate and monitor deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note:<ept id="p1">&lt;/strong&gt;</ept> Only 1 on-premise local agent certificate is needed for a tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>The following is an example of a Service Fabric Server certificate combined with an AOS SSL Certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Subject name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">件名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Subject Alternative Names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">件名の代替名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source><bpt id="p1">&lt;a name="plansvcacct"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 3. Plan your users and service accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="plansvcacct"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 3. ユーザーとサービス アカウントの計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>You must create several user or service accounts for Finance and Operations (on-premises) to work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations (オンプレミス) を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>You must create a combination of group managed service accounts (gMSAs), domain accounts, and SQL accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>The following table shows the user accounts, their purpose, and example names that will be used in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>User account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>User name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Financial Reporting Application Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務レポート アプリケーション サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Contoso<ph id="ph1">\\</ph>svc-FRAS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>svc-FRAS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Financial Reporting Process Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務レポート プロセス サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Contoso<ph id="ph1">\\</ph>svc-FRPS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>svc-FRPS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Financial Reporting Click Once Designer Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務レポート クリック ワンス デザイナー サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Contoso<ph id="ph1">\\</ph>svc-FRCO$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>svc-FRCO$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>AOS Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>This user should be created for future-proofing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このユーザーは、将来校正するために作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>We plan to enable AOS to work with the gMSA in upcoming releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後のリリースでは、AOS を gMSA と連携させる予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>By creating this user at the time of setup, you will help to ensure a seamless transition to the gMSA.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Contoso<ph id="ph1">\\</ph>svc-AXSF$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>svc-AXSF$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>AOS Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Domain account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>AOS uses this user in the general availability (GA) release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS は、一般提供 (GA) リリースでこのユーザーを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Contoso<ph id="ph1">\\</ph>AXServiceUser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>AXServiceUser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>AOS SQL DB Admin user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS SQL DB 管理者ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>SQL user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Finance and Operations uses this user to authenticate with SQL<ph id="ph1">\*</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、このユーザーを使用して SQL<ph id="ph1">\*</ph> を認証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>This user will also be replaced by the gMSA user in upcoming releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>AXDBAdmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXDBAdmin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Local Deployment Agent Service Account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル配置エージェント サービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>This account is used by the local agent to orchestrate the deployment on various nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Contoso<ph id="ph1">\\</ph>Svc-LocalAgent$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Contoso<ph id="ph1">\\</ph>Svc-LocalAgent$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source><ph id="ph1">\*</ph> The SQL user name and password for SQL authentication are secured because they are encrypted and stored in the file share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph> SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source><bpt id="p1">&lt;a name="createdns"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 4. Create DNS zones and add A records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="createdns"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 4. DNS ゾーンの作成とレコードの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>DNS is integrated with AD DS, and lets you organize, manage, and find resources in a network.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Create a DNS forward lookup zone and A records for the AOS host name and the Service Fabric cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS ホスト名と Service Fabric クラスタの DNS 正引き検索ゾーンと A レコードを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>In this example setup, the DNS zone name is d365ffo.onprem.contoso.com, and the A records/host names are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source><bpt id="p1">**</bpt>ax<ept id="p1">**</ept>.d365ffo.onprem.contoso.com for AOS machines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS の機械の場合 <bpt id="p1">**</bpt>ax<ept id="p1">**</ept>.d365ffo.onprem.contoso.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source><bpt id="p1">**</bpt>sf<ept id="p1">**</ept>.d365ffo.onprem.contoso.com for the Service Fabric cluster</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスターの場合 <bpt id="p1">**</bpt>sf<ept id="p1">**</ept>.d365ffo.onprem.contoso.com</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Add a DNS zone</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DNS ゾーンの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Use the following procedure to add a DNS zone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DNS ゾーンを追加するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Sign in to the domain controller machine, select <bpt id="p1">**</bpt>Start<ept id="p1">**</ept>, and start DNS Manager by typing <bpt id="p2">**</bpt>dnsmgmt.msc<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー マシンにサインインし、<bpt id="p1">**</bpt>開始<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>dnsmgmt.msc<ept id="p2">**</ept> と入力して DNS マネージャーを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Right-click the domain controller name, and then select <bpt id="p1">**</bpt>New Zone<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー名を右クリックし、<bpt id="p1">**</bpt>新しいゾーン<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Select <bpt id="p1">**</bpt>Primary Zone<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライマリ ゾーン<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Leave the <bpt id="p1">**</bpt>Store the zone in Active Directory (available only if the DNS Server is a writeable domain controller<ept id="p1">**</ept> check box selected, and then select <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)<ept id="p1">**</ept> のチェック ボックスが選択されたままの状態で、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Select <bpt id="p1">**</bpt>To all DNS Servers running on Domain Controllers in this domain: Contoso.com<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Select <bpt id="p1">**</bpt>Forward Lookup Zone<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>前方参照ゾーン<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Enter the zone name for your setup, and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定するゾーン名を入力し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>For example, enter <bpt id="p1">**</bpt>d365ffo.onprem.contoso.com<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>d365ffo.onprem.contoso.com<ept id="p1">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Select <bpt id="p1">**</bpt>Do not allow dynamic updates<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>動的更新を許可しない<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Set up an A record for AOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS の A レコードを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>In the new DNS zone, create one A record that is named <bpt id="p1">**</bpt>ax.d365ffo.onprem.contoso.com<ept id="p1">**</ept> for <bpt id="p2">**</bpt>each<ept id="p2">**</ept> Service Fabric cluster node of the <bpt id="p3">**</bpt>AOSNodeType<ept id="p3">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい DNS ゾーンで、<bpt id="p3">**</bpt>AOSNodeType<ept id="p3">**</ept> タイプの Service Fabric クラスター ノード<bpt id="p2">**</bpt>ごと<ept id="p2">**</ept>に、<bpt id="p1">**</bpt>ax.d365ffo.onprem.contoso.com<ept id="p1">**</ept> という名前の 1 つの A レコードを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Don't create A records for the other node types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のノード タイプの A レコードは作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Right-click the new zone, and then select <bpt id="p1">**</bpt>New Host<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいゾーンを右クリックして、<bpt id="p1">**</bpt>新しいホスト<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Enter the name and IP address of the Service Fabric node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric ノードの 名前および IP アドレスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>(For example, enter <bpt id="p1">**</bpt>10.179.108.12<ept id="p1">**</ept> as the IP address.) Select <bpt id="p2">**</bpt>Add Host<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(たとえば、<bpt id="p1">**</bpt>10.179.108.12<ept id="p1">**</ept> を IP アドレスとして入力します。) <bpt id="p2">**</bpt>ホストの追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Set up an A record for the orchestrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Orchestrator の A レコードを設定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>In the new DNS zone, create an A record that is named <bpt id="p1">**</bpt>sf.d365ffo.onprem.contoso.com<ept id="p1">**</ept> for <bpt id="p2">**</bpt>each<ept id="p2">**</ept> Service Fabric cluster node of the <bpt id="p3">**</bpt>OrchestratorType<ept id="p3">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい DNS ゾーンで、<bpt id="p3">**</bpt>OrchestratorType<ept id="p3">**</ept> タイプの Service Fabric クラスター ノード<bpt id="p2">**</bpt>ごと<ept id="p2">**</ept>に、<bpt id="p1">**</bpt>sf.d365ffo.onprem.contoso.com<ept id="p1">**</ept> という名前の 1 つの A レコードを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Don't create A records for the other node types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のノード タイプの A レコードは作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Right-click the new zone, and then select <bpt id="p1">**</bpt>New Host<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいゾーンを右クリックして、<bpt id="p1">**</bpt>新しいホスト<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Enter the name and IP address of the Service Fabric node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric ノードの 名前および IP アドレスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>(For example, enter <bpt id="p1">**</bpt>10.179.108.15<ept id="p1">**</ept> as the IP address.) Select <bpt id="p2">**</bpt>Add Host<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(たとえば、<bpt id="p1">**</bpt>10.179.108.15<ept id="p1">**</ept> を IP アドレスとして入力します。) <bpt id="p2">**</bpt>ホストの追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source><bpt id="p1">&lt;a name="joindomain"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 5. Join VMs to the domain</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="joindomain"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 5. VM のドメインへの参加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Join each VM to the domain by completing the steps in <bpt id="p1">[</bpt>How to join Windows Server 2016 to an Active Directory domain<ept id="p1">](https://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 VM をドメインに参加させるには、<bpt id="p1">[</bpt>Windows Server 2016 を Active Directory ドメインに参加させる方法<ept id="p1">](https://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html)</ept> の各手順を完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Alternatively, use the following Windows PowerShell script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、次の Windows PowerShell スクリプトを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>You must restart the VMs after you join them to the domain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメインにそれらを結合させた後、VM を再起動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>After the VMs are joined to the domain, add the AOS Service Accounts, <bpt id="p1">**</bpt>Contoso\svc-AXSF$<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Contoso\AXServiceUser<ept id="p2">**</ept> to the local administrators group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM をドメインに参加させた後、ローカル管理者グループに AOS サービス アカウント <bpt id="p1">**</bpt>Contoso\svc-AXSF$<ept id="p1">**</ept> と <bpt id="p2">**</bpt>Contoso\AXServiceUser<ept id="p2">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>For more information, see <bpt id="p1">[</bpt>Add a member to local group<ept id="p1">](https://technet.microsoft.com/library/cc772524(v=ws.11).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>ローカル グループへのメンバーの追加<ept id="p1">](https://technet.microsoft.com/library/cc772524(v=ws.11).aspx)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source><bpt id="p1">&lt;a name="downloadscripts"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 6. Download setup scripts from LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="downloadscripts"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 6. LCS からのセットアップ スクリプトのダウンロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>The scripts must be executed from a computer in the same domain that the on-premises infrastructure is in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/v2)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/v2)</ept> にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>On the dashboard, select the <bpt id="p1">**</bpt>Shared asset library<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュボードで、<bpt id="p1">**</bpt>共有アセット ライブラリ<ept id="p1">**</ept>タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>On the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> tab, in the grid, select the <bpt id="p2">**</bpt>Dynamics 365 for Operations on-premises - Deployment scripts - Latest<ept id="p2">**</ept> row.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept>タブの、グリッドで、<bpt id="p2">**</bpt>Dynamics 365 for Operations オンプレミス - 配置スクリプト - 最新<ept id="p2">**</ept>行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Click the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> button, and then select <bpt id="p2">**</bpt>Version 1<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バージョン<ept id="p1">**</ept> ボタンをクリックし、<bpt id="p2">**</bpt>バージョン 1<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Right-click the zip file, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">zip ファイルを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>In the dialog box, select the <bpt id="p1">**</bpt>Unblock<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、<bpt id="p1">**</bpt>ブロック解除<ept id="p1">**</ept>チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Copy the zip file to the machine that will be used to execute the scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Unzip the files into a folder that is named <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> という名前のフォルダーにファイルを解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Ensure all edits are made to the ConfigTemplate.xml in this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフォルダーの ConfigTemplate.xml にすべての編集を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source><bpt id="p1">&lt;a name="describeconfig"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 7. Describe your configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="describeconfig"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 7. コンフィギュレーションの記述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>The infrastructure setup scripts use the following configuration files to drive the setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>infrastructure\ConfigTemplate.xml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">infrastructure\ConfigTemplate.xml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>infrastructure\D365FO-OP\NodeTopologyDefintion.xml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">infrastructure\D365FO-OP\NodeTopologyDefintion.xml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source><bpt id="p1">**</bpt>infrastructure\ConfigTemplate.xml<ept id="p1">**</ept> describes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>infrastructure\ConfigTemplate.xml<ept id="p1">**</ept> で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Service Accounts that are needed for the application to operate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが動作するために必要なサービス アカウント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Certificates necessary for securing communications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通信を保護するために必要な証明書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Database configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース コンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Service Fabric cluster configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Service Fabric クラスター構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>For each Service Fabric Node type, <bpt id="p1">**</bpt>infrastructure\D365FO-OP\NodeTopologyDefinition.xml<ept id="p1">**</ept> describes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 Service Fabric ノード タイプについて、<bpt id="p1">**</bpt>infrastructure\D365FO-OP\NodeTopologyDefinition.xml<ept id="p1">**</ept> で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>The mapping between each node type and the application, domain and service accounts, and certificates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Whether to enable the UAC</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UAC を有効にするかどうか</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Prerequisites for Windows features and system software</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows の機能とシステム ソフトウェアの前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Whether strong name validation should be enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">厳密な名前の検証を有効にするかどうか</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>List of firewall ports to be opened</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開くファイアウォール ポートのリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>For each database, <bpt id="p1">**</bpt>infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml<ept id="p1">**</ept> describes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各データベースについて、<bpt id="p1">**</bpt>infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml<ept id="p1">**</ept> で説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>The DB settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DB 設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>The mappings between users and roles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーとロールの間のマッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Create gMSA and domain user accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA およびドメイン ユーザー アカウントを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Navigate to the machine that has the unzipped infrastructure scripts in the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept> フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Copy the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder to the domain controller machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept>フォルダーをドメイン コントローラー マシンにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Start Windows PowerShell in elevated mode, change the directory to the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者特権モードで Windows PowerShell を起動し、ディレクトリを <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> フォルダーに変更して、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>If you must make changes to accounts or machines, update the ConfigTemplate.xml file in the original <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder, copy it to this machine and then run the following script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アカウントまたはマシンを変更する必要がある場合は、元の <bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept> フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source><bpt id="p1">&lt;a name="configurecert"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 8. Configure certificates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="configurecert"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 8. 証明書のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Navigate to the machine that has the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept> フォルダーがあるマシンに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>If you must generate self-signed certificates, run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自己署名証明書を生成する必要がある場合は、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>The script will create the certificates, put them in the CurrentUser\My certificate store on the machine, and update the thumbprints in the XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトは証明書を作成し、それらをコンピューターの「CurrentUser\My certificate store」に格納し、XML ファイルのサムプリントを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>If you must reuse any certificates and therefore don't have to generate certificates for them, set the <bpt id="p1">**</bpt>generateSelfSignedCert<ept id="p1">**</ept> tag to <bpt id="p2">**</bpt>false<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書を再利用する必要があるため、証明書を生成する必要がない場合は、<bpt id="p1">**</bpt>generateSelfSignedCert<ept id="p1">**</ept> タグを <bpt id="p2">**</bpt>false<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>If you're using SSL certificates that were already generated, skip the Certificate generation and update the thumbprints in the configTemplate.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルの拇印を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>The certificates need to be installed in the CurrentUser\My store and their private keys must be exportable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Because of a leading not-printable special character, which is difficult to determine when present, the cert manager should not be used to copy thumbprints.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>If the not-printable special character is present, you will get <bpt id="p1">**</bpt>X509 certificate not valid<ept id="p1">**</ept> error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非印刷可能な特殊文字が存在する場合、<bpt id="p1">**</bpt>X509 証明書が有効ではない<ept id="p1">**</ept>というエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>To retrieve the thumbprints, see results from PowerShell commands or run the following commands in PowerShell.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Specify a semi-colon separated list of users or groups in the <bpt id="p1">**</bpt>ProtectTo<ept id="p1">**</ept> tag for each certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各証明書の <bpt id="p1">**</bpt>ProtectTo<ept id="p1">**</ept> でユーザーまたはグループのセミコロンで区切られた一覧を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Only Active directory users and groups specified in the <bpt id="p1">**</bpt>ProtectTo<ept id="p1">**</ept> tag will have permissions to import the certificates that are exported using the scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProtectTo<ept id="p1">**</ept> タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Passwords are not supported by the script to protect the exported certificates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Export the certificates into .pfx files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書を .pfx ファイルにエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source><bpt id="p1">&lt;a name="setupvms"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 9. Setup VMs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupvms"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 9. VM の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Export the scripts that must be run on each VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 VM で実行する必要があるスクリプトをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Download the following Microsoft Windows Installers (MSIs) into a file share that is accessible by all VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>Component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>Download link</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リンクのダウンロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>SNAC – ODBC driver</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SNAC – ODBC ドライバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>Microsoft SQL Server Management Studio 17.2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL ServerManagement Studio 17.2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Microsoft Visual C++ Redistributable Packages for Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>Microsoft Access Database Engine 2010 Redistributable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Access データベース エンジン 2010 再頒布可能パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Follow these steps for each VM</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 VM について、これらのステップに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>Copy the contents of each infrastructure\VMs<ph id="ph1">\&lt;</ph>VMName&gt; folder into the corresponding VM, and then run the following scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 infrastructure\VMs<ph id="ph1">\&lt;</ph>VMName&gt; フォルダーのコンテンツを対応する VM にコピーし、次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Restart the machine each time you're prompted to restart it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再起動するように求められるたびにコンピューターを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Make sure that you rerun the <ph id="ph1">`.\Configure-PreReqs.ps1`</ph> script after each restart until all the prerequisites are installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再起動した後、すべての前提条件がインストールされるまで、<ph id="ph1">`.\Configure-PreReqs.ps1`</ph> スクリプトを再実行することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Run the following scripts, if they exist, in order to complete the VM setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>Run the following script to validate the VM setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを実行して VM のセットアップを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source><bpt id="p1">&lt;a name="setupsfcluster"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 10. Set up a standalone Service Fabric cluster</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupsfcluster"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 10. スタンドアロン Service Fabric クラスターの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Download the <bpt id="p1">[</bpt>Service Fabric standalone installation package<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=730690)</ept> onto one of your Service Fabric nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Service Fabric スタンドアロン インストール パッケージ<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=730690)</ept> を使用中の Service Fabric ノードのいずれかにダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>After the zip file is downloaded, unblock it by right-clicking the zip file and then selecting <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>を選択してブロックを解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>In the dialog box, select the <bpt id="p1">**</bpt>Unblock<ept id="p1">**</ept> check box in the lower right.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、右下の <bpt id="p1">**</bpt>ブロック解除<ept id="p1">**</ept> チェック ボックスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Copy the zip file to one of the nodes in the Service Fabric cluster, and unzip it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>Ensure the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder has access to this folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept>フォルダーが、このフォルダーにアクセスすることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Navigate to the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder and execute the following command to generate the Service Fabric ClusterConfig.json file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept> フォルダーに移動し、次のコマンドを実行して Service Fabric Cluster の ClusterConfig.json ファイルを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>For more information, see, <bpt id="p1">[</bpt>Step 1B: Create a multi-machine cluster<ept id="p1">](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)</ept>, <bpt id="p2">[</bpt>Secure a standalone cluster on Windows using X.509 certificates<ept id="p2">](/azure/service-fabric/service-fabric-windows-cluster-x509-security)</ept>, and <bpt id="p3">[</bpt>Create a standalone cluster running on Windows Server<ept id="p3">](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>手順 1B: 複数のマシンでクラスターを作成する<ept id="p1">](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)</ept>、<bpt id="p2">[</bpt>X.509 証明書を使用して Windows スタンドアロン クラスターを保護する<ept id="p2">](/azure/service-fabric/service-fabric-windows-cluster-x509-security)</ept>、および<bpt id="p3">[</bpt>Windows Server で実行されているスタンドアロン クラスターを作成する<ept id="p3">](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source>Copy the generated ClusterConfig.json file to the <ph id="ph1">\&lt;</ph>ServiceFabricStandaloneInstallerPath<ph id="ph2">\&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生成された ClusterConfig.json ファイルを <ph id="ph1">\&lt;</ph>ServiceFabricStandaloneInstallerPath<ph id="ph2">\&gt;</ph> にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>Navigate to the <ph id="ph1">\&lt;</ph>ServiceFabricStandaloneInstallerPath<ph id="ph2">\&gt;</ph> in Windows PowerShell by using elevated privileges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上位の権限を使用して Windows PowerShell で <ph id="ph1">\&lt;</ph>ServiceFabricStandaloneInstallerPath<ph id="ph2">\&gt;</ph> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>Run the following command to test ClusterConfig.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行して ClusterConfig をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>If the test is successful, run the following command to deploy the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストが成功した場合は、次のコマンドを実行してクラスターを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>After the cluster is created, open the Service Fabric explorer on any client machine to validate the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Install the Service Fabric client certificate in CurrentUser<ph id="ph1">\\</ph>My if it isn't already installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まだインストールされていない場合、CurrentUser<ph id="ph1">\\</ph>My に Service Fabric クライアント証明書をインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Go to <bpt id="p1">**</bpt>IE settings<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Compatibility Mode<ept id="p2">**</ept>, and clear the <bpt id="p3">**</bpt>Display Intranet sites in compatibility mode<ept id="p3">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IE 設定<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>互換モード<ept id="p2">**</ept> に移動し、<bpt id="p3">**</bpt>互換モードでイントラネット サイトを表示する<ept id="p3">**</ept> チェック ボックスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Go to <ph id="ph1">`https://sf.d365ffo.onprem.contoso.com:19080`</ph>, where sf.d365ffo.onprem.contoso.com is the host name of the Service Fabric cluster that is specified in the zone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`https://sf.d365ffo.onprem.contoso.com:19080`</ph> に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>If DNS name resolution isn't configured, use the IP address of the machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Select the client certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントの証明書を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>The <bpt id="p1">**</bpt>Service Fabric explorer<ept id="p1">**</ept> page appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Service Fabric エクスプローラー<ept id="p1">**</ept> ページが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source><bpt id="p1">&lt;a name="configurelcs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 11. Configure LCS connectivity for the tenant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="configurelcs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 11. テナント用 LCS 接続のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>Deployment and servicing of Finance and Operations is orchestrated through LCS by using an on-premises local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>To establish connectivity from LCS to the Finance and Operations tenant, you must configure a certificate that enables the local agent to act on behalf on your Azure AD tenant (for example, Contoso.onmicrosoft.com).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS から Finance and Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>Use the on-premises agent certificate that you acquired from a CA or the self-signed certificate that you generated by using scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>The on-premises agent certificate can be reused across multiple sandbox and production environments per tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>Only user accounts that have the Global Administrator directory role can add certificates to authorize LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>By default, the person who signs up for Microsoft Office 365 for your organization is the global administrator for the directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>You must configure the certificate exactly one time per tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テナントごとに証明書を正確に 1 回構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>All on-premises environments can use the same certificate to connect with LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Download and install the latest version of Azure PowerShell on a client machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>For more information, see <bpt id="p1">[</bpt>Installing the Azure PowerShell Service Management module<ept id="p1">](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azure-ps?view=azuresmps-4.0.0)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については <bpt id="p1">[</bpt>Azure PowerShell サービス管理モジュールのインストール<ept id="p1">](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azure-ps?view=azuresmps-4.0.0)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>Sign in to the <bpt id="p1">[</bpt>customer's Azure portal<ept id="p1">](https://portal.azure.com)</ept> to verify that you have the Global Administrator directory role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>顧客の Azure ポータル<ept id="p1">](https://portal.azure.com)</ept> にサインインして、グローバル管理者ディレクトリの役割があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>Run the following script from $(DownloadPath)<ph id="ph1">\\</ph>InfrastructureScripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">$(DownloadPath)<ph id="ph1">\\</ph>InfrastructureScripts から次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source><bpt id="p1">&lt;a name="setupfile"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 12. Set up file storage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupfile"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 12.ファイル ストレージの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>You must set up the following SMB 3.0 file shares:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の SMB 3.0 ファイル共有を設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>A file share that stores user documents that are uploaded to AOS (for example, <ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>aos-storage).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、<ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>aos-storage)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>A file share that stores the latest build and configuration files to orchestrate the deployment (for example, <ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>agent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、<ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>agent)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>Keep this file share path as short as possible to avoid exceeding the maximum path length on the files that will be put in the share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>For information about how to enable SMB 3.0, see <bpt id="p1">[</bpt>SMB Security Enhancements<ept id="p1">](https://technet.microsoft.com/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SMB 3.0 を有効にする方法については、<bpt id="p1">[</bpt>SMB セキュリティの強化<ept id="p1">](https://technet.microsoft.com/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Secure dialect negotiation can't detect or prevent downgrades from SMB 2.0 or 3.0 to SMB 1.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>Therefore, we strongly recommend that you disable the SMB 1.0 server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>By disabling the SMB 1.0 server, you can take advantage of the full capabilities of SMB encryption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>To help ensure that your data is protected while it's at rest in your environment, BitLocker Drive Encryption must be enabled on every machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>For information about how to enable BitLocker, see <bpt id="p1">[</bpt>BitLocker: How to deploy on Windows Server 2012 and later<ept id="p1">](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BitLocker を有効にする方法については、<bpt id="p1">[</bpt>BitLocker: Windows Server 2012 以降で配置する方法<ept id="p1">](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>On the file share machine, run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル共有マシンで、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>Follow these steps to set up the <ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>aos-storage file share:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>aos-storage ファイル共有を設定するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>In Server Manager, select <bpt id="p1">**</bpt>File and Storage Services<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Shares<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー マネージャーで、<bpt id="p1">**</bpt>ファイルと保管サービス<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>共有<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Select <bpt id="p1">**</bpt>Tasks<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>New Share<ept id="p2">**</ept> to create a new share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>新しい共有<ept id="p2">**</ept> を選択し、新しい共有を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>Name the share <bpt id="p1">**</bpt>aos-storage<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有に <bpt id="p1">**</bpt>aos-storage<ept id="p1">**</ept> と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>Grant <bpt id="p1">**</bpt>Modify<ept id="p1">**</ept> permissions for every machine in the Service Fabric cluster except OrchestratorType.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して<bpt id="p1">**</bpt>変更<ept id="p1">**</ept>許可を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>Grant <bpt id="p1">**</bpt>Modify<ept id="p1">**</ept> permissions for the user AOS domain user (contoso<ph id="ph1">\\</ph>AXServiceUser) and the gMSA user (contoso<ph id="ph2">\\</ph>svc-AXSF$).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS ドメイン ユーザー (contoso<ph id="ph1">\\</ph>AXServiceUser) と gMSA ユーザー (contoso<ph id="ph2">\\</ph>svc-AXSF$) に対して、<bpt id="p1">**</bpt>変更<ept id="p1">**</ept>アクセス許可を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Follow these steps to set up the <ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph>agent file share:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph><ph id="ph2">\\</ph>DAX7SQLAOFILE1<ph id="ph3">\\</ph> エージェント ファイル共有を設定するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>In Server Manager, select <bpt id="p1">**</bpt>File and Storage Services<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Shares<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー マネージャーで、<bpt id="p1">**</bpt>ファイルと保管サービス<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>共有<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Select <bpt id="p1">**</bpt>Tasks<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>New Share<ept id="p2">**</ept> to create a new share.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タスク<ept id="p1">**</ept><ph id="ph1">\&gt;</ph><bpt id="p2">**</bpt>新しい共有<ept id="p2">**</ept> を選択し、新しい共有を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Name the share <bpt id="p1">**</bpt>agent<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有に<bpt id="p1">**</bpt>エージェント<ept id="p1">**</ept>と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>Grant <bpt id="p1">**</bpt>Full-Control<ept id="p1">**</ept> permissions to the gMSA user for the local deployment agent (contoso<ph id="ph1">\\</ph>svc-LocalAgent$).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル展開エージェント (contoso<ph id="ph1">\\</ph>svc-LocalAgent$) の gMSA ユーザーに対して <bpt id="p1">**</bpt>フル コントロール<ept id="p1">**</ept> のアクセス許可を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source><bpt id="p1">&lt;a name="setupsql"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 13. Set up SQL Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupsql"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 13. SQL Server の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>Install SQL Server 2016 SP1 with high availability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性を備えた SQL Server 2016 SP1 をインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>(Unless you're deploying in a sandbox environment, where one instance of SQL Server is sufficient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>You may want to install SQL Server with high availability in sandbox enviornments to test high availability scenarios.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>You can install SQL Server with high availability either as SQL clusters that include a Storage Area Network (SAN) or in an Always-On configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Verify that the Database Engine, SSRS, Full-Text Search, and Management Tools are already installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Make sure that Always-On is set up as described in <bpt id="p1">[</bpt>Select Initial Data Synchronization Page (Always On Availability Group Wizards)<ept id="p1">](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards)</ept>, and follow the instructions in <bpt id="p2">[</bpt>To Prepare Secondary Databases Manually<ept id="p2">](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Always-On が <bpt id="p1">[</bpt>初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)<ept id="p1">](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards)</ept> で説明されているとおりに設定され、<bpt id="p2">[</bpt>セカンダリ データベースを手動で準備する<ept id="p2">](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)</ept> の指示に従っていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>Run the SQL service as a domain user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン ユーザーとして SQL サービスを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>Get an SSL certificate from a CA to configure Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations を構成するために CA から SSL 証明書を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source>For testing purposes, you can create and use a self-signed certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストの目的で、自己署名証明書を作成して使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source><bpt id="p1">**</bpt>Self-signed certificate for a Clustered SQL instance<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスター化された SQL インスタンスの自己署名証明書<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source><bpt id="p1">**</bpt>Self-signed certificate for an Always-On SQL instance<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Always-On SQL インスタンスの自己署名証明書<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source><bpt id="p1">**</bpt>Manual<ept id="p1">**</ept> creation of test certificates:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト証明書の<bpt id="p1">**</bpt>手動<ept id="p1">**</ept>作成。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>Use the certificate(s) to configure SSL on SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL サーバーで SSL を構成するには、証明書を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Follow the steps in <bpt id="p1">[</bpt>How to enable SSL encryption for an instance of SQL Server by using Microsoft Management Console<ept id="p1">](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法<ept id="p1">](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)</ept> の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>For each node of the SQL cluster, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL クラスターの各ノードに対して、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>Make sure that you make the changes on the non-active node, and that you fail over to it after changes are made.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非アクティブなノードで変更を加えて、変更が行われた後フェール オーバーするようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>Import the certificate into LocalMachine<ph id="ph1">\\</ph>My, unless you are setting up Always-On, in which case the certificate already exists on the node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LocalMachine<ph id="ph1">\\</ph>My に証明書をインポートします。Always-On を設定していない限り、証明書は既にノードに存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Grant certificate permissions to the service account that is used to run the SQL service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>In Microsoft Management Console (MMC), right-click the certificate (<bpt id="p1">**</bpt>certlm.msc<ept id="p1">**</ept>), and then select <bpt id="p2">**</bpt>Tasks<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>Manage Private Keys<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft 管理コンソール (MMC) で証明書 (<bpt id="p1">**</bpt>certlm.msc<ept id="p1">**</ept>) を右クリックし、<bpt id="p2">**</bpt>タスク<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>秘密キーの管理<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>Add the certificate thumbprint to HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>SOFTWARE<ph id="ph4">\\</ph>Microsoft<ph id="ph5">\\</ph>Microsoft SQL Server<ph id="ph6">\\</ph><bpt id="p1">*</bpt>MSSQL.x<ept id="p1">*</ept><ph id="ph7">\\</ph>MSSQLServer<ph id="ph8">\\</ph>SuperSocketNetLib<ph id="ph9">\\</ph>Certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の拇印を HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>SOFTWARE<ph id="ph4">\\</ph>Microsoft<ph id="ph5">\\</ph>Microsoft SQL Server<ph id="ph6">\\</ph><bpt id="p1">*</bpt>MSSQL.x<ept id="p1">*</ept><ph id="ph7">\\</ph>MSSQLServer<ph id="ph8">\\</ph>SuperSocketNetLib<ph id="ph9">\\</ph>Certificate に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>In Microsoft SQL Server Configuration Manager, set <bpt id="p1">**</bpt>ForceEncryption<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 構成マネージャーで、<bpt id="p1">**</bpt>ForceEncryption<ept id="p1">**</ept> を<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>Export the public key of the certificate (the .cer file), and install it in the trusted root of each Service Fabric node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source><bpt id="p1">&lt;a name="configuredb"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 14. Configure the databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="configuredb"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 14. データベースのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/v2)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/v2)</ept> にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>On the dashboard, select the <bpt id="p1">**</bpt>Shared asset library<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュボードで、<bpt id="p1">**</bpt>共有アセット ライブラリ<ept id="p1">**</ept>タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>On the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> tab, select the demo data for the release you want and download the zip file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept>タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Release</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リリース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Demo Data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>On-premises General Availability (GA) release</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミスの一般提供 (GA) リリース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Dynamics 365 for Operations (on-premises) - Demo data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Operations (オンプレミス) - デモ データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>On-premises Platform Update 11 Nov 2017 release</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>Dynamics 365 for Operations, Enterprise edition (on-premises) - Update 11 Demo data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Operations, Enterprise edition (オンプレミス) - 更新プログラム 11 デモ データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>The zip file contains empty and demo data .bak files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">zip ファイルには空のデモデータ .bak ファイルが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>Select .bak file, based on your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、.bak ファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>For example, if you require demo data, download the AxBootstrapDB_Demodata.bak file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>Ensure the database section in the infrastructure\ConfigTempate.xml is configured correctly with the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>The database name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>The db file and log settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db ファイルとログ設定。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>The db settings should not be lower than the defaults specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dbの設定は、指定された既定値以上にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>The path to the backup file downloaded from LCS Shared Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>The default name for the Finance and Operations database is AXDB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースの既定の名前は AXDB です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>The user running the SQL service and the user running the scripts should have READ access on the folder or share where the backup file is located.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>If a database with the same name exists, the database will be reused.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ名前のデータベースが存在する場合は、データベースが再利用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>Copy the <bpt id="p1">**</bpt>infrastructure<ept id="p1">**</ept> folder to the SQL Server machine and navigate to it in a PowerShell window with elevate privileges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インフラストラクチャ<ept id="p1">**</ept>フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>Configure the OrchestratorData database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OrchestratorData データベースのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Execute the following script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>The script will do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトは、次の操作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>Create an empty database named <bpt id="p1">**</bpt>OrchestratorData<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OrchestratorData<ept id="p1">**</ept> という名前の空のデータベースを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>This database is used by the on-premises local agent to orchestrate deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>Grant the local agent gMSA (svc-LocalAgent$) <bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>owner<ept id="p1">**</ept> permissions on the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースにローカル エージェント gMSA (svc-LocalAgent$) <bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>owner<ept id="p1">**</ept> アクセス許可を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>Configure the Finance and Operations database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースの構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>Execute the following scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>The <bpt id="p1">**</bpt>Initialize-Database.ps1<ept id="p1">**</ept> script will do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Initialize-Database.ps1<ept id="p1">**</ept> スクリプトは、次の操作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>Restore the database from the specified backup file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたバックアップ ファイルからデータベースを復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>Create a new user that has SQL authentication enabled (axdbadmin).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>Map users to database roles based on the following table for AXDB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXDB の次の表に基づくデータベース ロールにユーザーをマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>User</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Database role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>svc-AXSF$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-AXSF$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>svc-LocalAgent$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-LocalAgent$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>svc-FRPS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-FRPS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>svc-FRAS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-FRAS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>axdbadmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">axdbadmin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source>SqlUser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SqlUser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>Map users to database roles based on the following table for TempDB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TempDB の次の表に基づくデータベース ロールにユーザーをマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>User</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>Database role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>svc-AXSF$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-AXSF$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>db_datareader, db_datawriter, db_ddladmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db_datareader, db_datawriter, db_ddladmin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>axdbadmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">axdbadmin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>SqlUser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SqlUser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>db_datareader, db_datawriter, db_ddladmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db_datareader, db_datawriter, db_ddladmin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source>The <bpt id="p1">**</bpt>Configure-Database.ps1<ept id="p1">**</ept> script will do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Configure-Database.ps1<ept id="p1">**</ept> スクリプトは、次の操作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>Set READ_COMMITTED_SNAPSHOT ON</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">READ_COMMITTED_SNAPSHOT ON を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Set ALLOW_SNAPSHOT_ISOLATION ON</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ALLOW_SNAPSHOT_ISOLATION ON を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>Set the specified database file and log settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したデータベース ファイルとログの設定を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>GRANT VIEW SERVER STATE TO axdbadmin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー状態の表示を axdbadmin に付与</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>GRANT VIEW SERVER STATE TO [contoso\svc-AXSF$]</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー状態の表示を [contoso\svc AXSF$] に付与</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>Run the following command to reset the database users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ユーザーをリセットするには、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>Configure the Financial Reporting database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務レポート データベースのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>Execute the following script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>The script will do the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトは、次の操作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>Create an empty database named <bpt id="p1">**</bpt>FinancialReporting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FinancialReporting<ept id="p1">**</ept> という名前の空のデータベースを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>Map the users to database roles based on the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表に基づくデータベース ロールにユーザーをマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>User</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">種類</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>Database role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>svc-LocalAgent$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-LocalAgent$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>svc-FRPS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-FRPS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>svc-FRAS$</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">svc-FRAS$</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>gMSA</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">gMSA</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source>db<ph id="ph1">\_</ph>owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">db<ph id="ph1">\_</ph>owner</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source><bpt id="p1">&lt;a name="encryptcred"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 15. Encrypt credentials</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="encryptcred"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 15. 資格情報の暗号化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>On any client machine, install the encipherment certificate in the LocalMachine<ph id="ph1">\\</ph>My certificate store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のクライアント マシンで、LocalMachine<ph id="ph1">\\</ph>My certificate store に暗号化証明書をインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>Grant the current user read access to the private key of this certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>Create the Credentials.json file, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のようにして、Credentials.json ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source><bpt id="p1">**</bpt>AccountPassword<ept id="p1">**</ept> is the encrypted domain user password for the AOS domain user (contoso<ph id="ph1">\\</ph>axserviceuser).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AccountPassword<ept id="p1">**</ept> は、AOS ドメインユーザー (contoso<ph id="ph1">\\</ph>axserviceuser) の暗号化されたドメイン ユーザー パスワードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source><bpt id="p1">**</bpt>SqlUser<ept id="p1">**</ept> is the encrypted SQL user (axdbadmin) that has access to the Finance and Operations database (AXDB), and <bpt id="p2">**</bpt>SqlPassword<ept id="p2">**</ept> is the encrypted SQL password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SqlUser<ept id="p1">**</ept> は、Finance and Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、<bpt id="p2">**</bpt>SqlPassword<ept id="p2">**</ept> は暗号化された SQL パスワードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>Copy the .json file to the SMB file share, <ph id="ph1">\\</ph><ph id="ph2">\\</ph>AX7SQLAOFILE1<ph id="ph3">\\</ph>agent<ph id="ph4">\\</ph>Credentials<ph id="ph5">\\</ph>Credentials.json.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.json ファイルを SMB ファイル共有、<ph id="ph1">\\</ph><ph id="ph2">\\</ph>AX7SQLAOFILE1<ph id="ph3">\\</ph>agent<ph id="ph4">\\</ph>Credentials<ph id="ph5">\\</ph>Credentials.json にコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>Update the Credentials.json file with encrypted values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗号化された値で Credentials.json ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source><bpt id="p1">&lt;a name="setupssis"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 16. Set up SSIS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupssis"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 16. SSIS の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>To enable Data management and Integration workloads, SSIS must be installed on each of the AOS virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>Complete the following steps on each AOS virtual machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 AOS 仮想マシン上で、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>Verify that the machine has access to the SSIS installation and open the SSIS Setup Wizard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>In the <bpt id="p1">**</bpt>Feature Selection<ept id="p1">**</ept> window, in the <bpt id="p2">**</bpt>Features<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>Integration Services<ept id="p3">**</ept> and <bpt id="p4">**</bpt>SQL Client Connectivity SDK<ept id="p4">**</ept> check boxes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>機能の選択<ept id="p1">**</ept>ウィンドウの<bpt id="p2">**</bpt>機能<ept id="p2">**</ept>ウィンドウで、<bpt id="p3">**</bpt>Integration Services<ept id="p3">**</ept> および <bpt id="p4">**</bpt>SQL クライアント接続 SDK<ept id="p4">**</ept> のチェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>Complete the setup and verify that the installation was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップを完了し、インストールが正常に完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>For more information, see <bpt id="p1">[</bpt>Install integration services<ept id="p1">](https://docs.microsoft.com/sql/integration-services/install-windows/install-integration-services)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>統合サービスのインストール<ept id="p1">](https://docs.microsoft.com/sql/integration-services/install-windows/install-integration-services)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source><bpt id="p1">&lt;a name="setupssrs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 17. Set up SSRS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="setupssrs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 17. SSRS の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>Before you begin, make sure that the prerequisites that are listed at the beginning of this topic are installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>Follow the steps in <bpt id="p1">[</bpt>Configure SQL Server Reporting Services for an on-premises deployment<ept id="p1">](../analytics/configure-ssrs-on-premises.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション<ept id="p1">](../analytics/configure-ssrs-on-premises.md)</ept> の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source><bpt id="p1">&lt;a name="configureadfs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 18. Configure AD FS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="configureadfs"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>18. AD FS のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>Before you can complete this procedure, AD FS must be deployed on Windows Server 2016.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source>For information about how to deploy AD FS, see <bpt id="p1">[</bpt>Deployment Guide Windows Server 2016 and 2012 R2 AD FS Deployment Guide<ept id="p1">](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS を展開する方法については、<bpt id="p1">[</bpt>Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド<ept id="p1">](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>Finance and Operations requires additional configuration beyond the default out-of-box configuration of AD FS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>For the following steps, Windows PowerShell runs on a machine where the AD FS role service is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順では、Windows PowerShell は AD FS ロール サービスがインストールされているマシン上で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>The user account must have enough permissions to administer AD FS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source>For example, the user must have a domain administrator account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ユーザーには、ドメイン管理者アカウントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>Configure the AD FS identifier so that it matches the AD FS token issuer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source>You should disable Windows Integrated Authentication (WIA) for intranet authentication connections, unless you've configured AD FS for mixed environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>For more information about how to configure WIA so that it can be used with AD FS, see <bpt id="p1">[</bpt>Configure browsers to use Windows Integrated Authentication (WIA) with AD FS<ept id="p1">](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WIA を AD FS で使用できるように構成する方法の詳細については、<bpt id="p1">[</bpt>AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する<ept id="p1">](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source>For sign-in, the user's email address must be an acceptable authentication input.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>In order for AD FS to trust Finance and Operations for the exchange of authentication, various application entries must be registered in AD FS under an AD FS application group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AD FS が認証を交換するために Finance and Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>To speed up the setup process and help reduce errors, you can use the following script for registration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>Copy the Publish-ADFSApplicationGroup.ps1 script and D365FO-OP directory to a machine where the AD FS role service is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source>Then run the script by using a user account that has enough permissions to administer AD FS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>(For example, use an administrator account.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(たとえば、管理者アカウントを使用します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>For more information about how to use the script, see the documentation that is listed in the script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>Make a note of the client IDs that are specified in the output, because you will need this information in LCS in a later step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source>Should you lose the client IDs, log in to the machine which has AD FS installed, open <bpt id="p1">**</bpt>Server Manager<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Tools<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AD FS Management<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>Application Groups<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>Microsoft Dynamics 365 for Operations On-premises<ept id="p5">**</ept> and find the client IDs under the native applications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、<bpt id="p1">**</bpt>サーバー マネージャー<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>ツール<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>AD FS の管理<ept id="p3">**</ept> <ph id="ph3">\&gt;</ph> <bpt id="p4">**</bpt>アプリケーション グループ<ept id="p4">**</ept> <ph id="ph4">\&gt;</ph> <bpt id="p5">**</bpt>Microsoft Dynamics 365 for Operations On-premises<ept id="p5">**</ept>を開き、ネイティブ アプリケーションでクライアント ID を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>Application group properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション グループのプロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>Finally, make sure that you can access the AD FS OpenID Configuration URL on a Service Fabric node of the <bpt id="p1">**</bpt>AOSNodeType<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、<bpt id="p1">**</bpt>AOSNodeType<ept id="p1">**</ept> タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>To perform this check, try to open <ph id="ph1">`https://&lt;adfs-dns-name&gt;/adfs/.well-known/openid-configuration`</ph> in a web browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチェックを行うには、Web ブラウザーで <ph id="ph1">`https://&lt;adfs-dns-name&gt;/adfs/.well-known/openid-configuration`</ph> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source>If you receive a message that states that the site isn't secure, you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>This step is described in the AD FS deployment guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順については、「AD FS 展開ガイド」で説明されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>If you successfully access the URL, a JavaScript Object Notation (JSON) file is returned that contains your AD FS configuration, and you will see that your AD FS URL is trusted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>You've now completed the setup of the infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、インフラストラクチャの設定を完了しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source>The following sections describe how to navigate to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com)</ept> to set up your connector and deploy your Finance and Operations environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、<bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com)</ept> にアクセスしてコネクタを設定し、Finance and Operations 環境を配置する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source><bpt id="p1">&lt;a name="configureconnector"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 19. Configure a connector and install an on-premises local agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="configureconnector"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept>, and open the on-premises implementation project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept> にサインインし、オンプレミスの実装プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source>On the hamburger menu, select <bpt id="p1">**</bpt>Project settings<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンバーガー メニューで、<bpt id="p1">**</bpt>プロジェクト設定<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source>Project settings command</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト設定コマンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source>Select <bpt id="p1">**</bpt>On-premises connectors<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オンプレミス コネクタ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to create a new connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコネクタを作成するには、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>On the <bpt id="p1">**</bpt>Setup host infrastructure<ept id="p1">**</ept> tab, download the agent installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ホスト インフラストラクチャ設定<ept id="p1">**</ept> タブで、エージェント インストーラーをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source>Download agent installer button on the Setup host infrastructure tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="701">
          <source>Verify that the zip file is unblocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">zip ファイルがブロックされていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="702">
          <source>Right-click the file, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="703">
          <source>In the dialog box, select <bpt id="p1">**</bpt>Unblock<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで<bpt id="p1">**</bpt>ブロック解除<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="704">
          <source>Unzip the agent installer on one of the Service Fabric nodes of the <bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OrchestratorType<ept id="p1">**</ept> タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="705">
          <source>On the <bpt id="p1">**</bpt>Configure agent<ept id="p1">**</ept> tab, enter the configuration settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成エージェント<ept id="p1">**</ept> タブで、コンフィギュレーションの設定を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="706">
          <source>Save the configuration, and then select <bpt id="p1">**</bpt>Download configurations<ept id="p1">**</ept> to download the localagent-config.json configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーションを保存し、<bpt id="p1">**</bpt>コンフィギュレーションのダウンロード<ept id="p1">**</ept> を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="707">
          <source>Download configurations button on the Configure agent tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="708">
          <source>Copy the localagent-config.json file to the machine where the agent installer package is located.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="709">
          <source>In a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window, run the following command by navigating to the folder that contains the agent installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="710">
          <source>The user who runs this command must have <bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>owner<ept id="p1">**</ept> permissions on the OrchestratorData database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを実行するユーザーは、OrchestratorData データベースに対して <bpt id="p1">**</bpt>db<ph id="ph1">\_</ph>owner<ept id="p1">**</ept> のアクセス許可を持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="711">
          <source>After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="712">
          <source>On the <bpt id="p1">**</bpt>Validate setup<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Message agent<ept id="p2">**</ept> to test for LCS connectivity to your local agent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定の検証<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>メッセージ エージェント<ept id="p2">**</ept>を選択して、ローカル エージェントへの LCS 接続をテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="713">
          <source>When a connection is successfully established, the page will resemble the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続が正常に確立されると、ページは下図のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="714">
          <source>Validate the agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エージェントの検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="715">
          <source><bpt id="p1">&lt;a name="deploy"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 20. Deploy your Finance and Operations (on-premises) environment from LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="deploy"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 20. LCS から Finance and Operations (オンプレミス) 環境を配置する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="716">
          <source>In LCS, navigate to your on-premises project, go to <bpt id="p1">**</bpt>Environment<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Sandbox<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>Configure<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で、オンプレミス プロジェクトに移動し、<bpt id="p1">**</bpt>環境<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>サンドボックス<ept id="p2">**</ept>に移動してから<bpt id="p3">**</bpt>構成<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="717">
          <source>For new deployments, select your environment topology, and then complete the wizard to start your deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="718">
          <source>If you have an existing deployment, see the topic <bpt id="p1">[</bpt>Redeploy an on-premises environment<ept id="p1">](redeploy-on-prem.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の展開がある場合は、「<bpt id="p1">[</bpt>設置環境を再配置<ept id="p1">](redeploy-on-prem.md)</ept>」というトピックを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="719">
          <source>The local agent will pick up the deployment request, start the deployment, and communicate back to LCS when the environment is ready.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="720">
          <source>If the deployment fails, the <bpt id="p1">**</bpt>Reconfigure<ept id="p1">**</ept> button will become available for your environment in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開に失敗した場合、LCS のお客様の環境では、<bpt id="p1">**</bpt>再設定<ept id="p1">**</ept>ボタンは利用可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="721">
          <source>Fix the underlying issue, click <bpt id="p1">**</bpt>Reconfigure<ept id="p1">**</ept>, update any configuration changes, and click <bpt id="p2">**</bpt>Deploy<ept id="p2">**</ept> to retry the deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基になる問題を修正し、<bpt id="p1">**</bpt>再コンフィギュレーション<ept id="p1">**</ept>をクリックして、任意のコンフィギュレーションの変更を更新し、<bpt id="p2">**</bpt>配置<ept id="p2">**</ept>をクリックして配置を再試行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="722">
          <source><bpt id="p1">&lt;a name="connect"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 21. Connect to your Finance and Operations (on-premises) environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a name="connect"&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 21. Finance and Operations (オンプレミス) 環境に接続する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="723">
          <source>In your browser, navigate to https://[yourD365FOdomain]/namespaces/AXSF, where yourD365FOdomain is the domain name that you defined in the <bpt id="p1">[</bpt>Plan your domain name and DNS zones<ept id="p1">](#plandomain)</ept> section of this document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのドキュメントの<bpt id="p1">[</bpt>ドメイン名と DNS ゾーンの計画<ept id="p1">](#plandomain)</ept> セクションで定義したドメイン名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="724">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="725">
          <source><bpt id="p1">[</bpt>Apply updates to an on-premises deployment<ept id="p1">](apply-updates-on-premises.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オンプレミス配置への更新プログラムの適用<ept id="p1">](apply-updates-on-premises.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="726">
          <source><bpt id="p1">[</bpt>Redeploy an on-premises deployment<ept id="p1">](redeploy-on-prem.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>オンプレミス配置の再配置<ept id="p1">](redeploy-on-prem.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>