<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="plan-2012-r3-deployment-azure.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>plan-2012-r3-deployment-azure.db6524.908ea8ea8d609de145c6d078203328d97682e6b1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>908ea8ea8d609de145c6d078203328d97682e6b1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\plan-2012-r3-deployment-azure.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Plan AX 2012 R3 deployments on Azure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 上での AX 2012 R3の 配置計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Before you can deploy Microsoft Dynamics AX 2012 R3 on Microsoft Azure, there are several things you must consider and decisions you must make.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This article guides you through the planning process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、計画プロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Plan AX 2012 R3 deployments on Azure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 上での AX 2012 R3の 配置計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Before you can deploy Microsoft Dynamics AX 2012 R3 on Microsoft Azure, there are several things you must consider and decisions you must make.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure に Microsoft Dynamics AX 2012 R3 を展開する前に、いくつかの点を考慮し決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This article guides you through the planning process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、計画プロセスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Deployments of AX 2012 R3 on Azure are supported by Microsoft in the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 上の AX 2012 R3 の配備は、Microsoft が次のシナリオでサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The deployment has been performed through Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置は、Microsoft Dynamics Lifecycle Services (LCS) を通じて実行されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Customer or partner-driven deployments that have been performed strictly adhering to the following guidance:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のガイダンスに厳密に従って実施された顧客またはパートナー主導配置。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>SQL is deployed in a High Availability topology (using SQL Clustering/Always On).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL は、(SQL クラスタリング/Always On を使用して) 可用性トポロジに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>SQL best practices have been followed for deployment in Azure, using the <bpt id="p1">[</bpt>Performance best practices for SQL Server in Azure Virtual Machines<ept id="p1">](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure に配置するために、<bpt id="p1">[</bpt>Azure 仮想マシンでの SQL Server のパフォーマンス ベスト プラクティス<ept id="p1">](/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)</ept>を使用して、SQL のベスト プラクティスに従っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Best practices for SQL Server configuration for AX 2012 have been followed, as specified in <bpt id="p1">[</bpt>Configure SQL Server and storage settings (TechNet)<ept id="p1">](https://technet.microsoft.com/en-us/library/dd309734.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SQL サーバーおよび記憶域の設定のコンフィギュレーション (TechNet)<ept id="p1">](https://technet.microsoft.com/en-us/library/dd309734.aspx)</ept> によって指定された AX 2012 の SQL Server コンフィギュレーションのベスト プラクティスに従っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The System diagnostic tool is installed and best practices are followed, as specified in <bpt id="p1">[</bpt>System diagnostics<ept id="p1">](system-diagnostics-lcs.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>システム診断<ept id="p1">](system-diagnostics-lcs.md)</ept>で指定されているように、システム診断ツールがインストールされ、ベスト プラクティスに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If you have an issue in an unsupported AX 2012 R3 on Azure environment, and can reproduce the same issue in an AX 2012 R3 environment that was either deployed to Azure through LCS, or deployed locally, Microsoft can provide support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 環境でサポートされていない AX 2012 R3 に問題があり、LCS 経由で Azure に展開された、またはローカルに展開された AX 2012 R3 環境で同じ問題を再現することができる場合、Microsoft がサポートを提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>AX 2012 R3 can also be deployed on-premises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 は、オンプレミスでも配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For details, see the topic <bpt id="p1">[</bpt>Install Microsoft Dynamics AX 2012<ept id="p1">](https://technet.microsoft.com/en-us/library/dd362138.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Microsoft Dynamics AX 2012 のインストール<ept id="p1">](https://technet.microsoft.com/en-us/library/dd362138.aspx)</ept> のトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Verify that you can log on to Lifecycle Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services にログオンできることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Lifecycle Services (LCS) is a cloud-based collaborative workspace that customers and partners can use to manage Microsoft Dynamics AX projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) は、顧客およびパートナーが Microsoft Dynamics AX プロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You’ll use the Cloud-hosted environments tool, available on the Lifecycle Services website, to deploy AX 2012 R3 on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 上に AX 2012 R3 を配置するには、Lifecycle Services Web サイトで利用できるクラウド ホスト環境ツールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Lifecycle Services is available to customers and partners as part of their support plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You can access it with your CustomerSource or PartnerSource credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource または PartnerSource の資格情報でアクセスすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">[</bpt>Verify that you can log on to Lifecycle Services<ept id="p1">](https://lcs.dynamics.com/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Lifecycle Services にログオンできることを確認する<ept id="p1">](https://lcs.dynamics.com/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Purchase an Azure subscription</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure サブスクリプションの購買</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To use Azure, you must purchase a subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure を使用するには、サブスクリプションを購入する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For information about subscription plans and pricing details, see the <bpt id="p1">[</bpt>Azure pricing<ept id="p1">](https://azure.microsoft.com/en-us/pricing/)</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクリプション プランおよび価格決定の詳細については、<bpt id="p1">[</bpt>Azure 価格決定<ept id="p1">](https://azure.microsoft.com/en-us/pricing/)</ept> ページを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Then follow the instructions on that page to purchase a subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、そのページの指示に従ってサブスクリプションを購入します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The subscription must be large enough to support the AX 2012 R3 environment that you want to deploy on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクリプションは、Azure に配備する AX 2012 R3 環境をサポートするのに十分な大きさでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The following table lists the types of AX 2012 R3 environments that you can deploy on Azure, and the number of cores required to deploy each environment in its default configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、Azure に配置できる AX 2012 R3 環境のタイプと、各環境を既定のコンフィギュレーションで配置するために必要なコアの数を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Keep in mind that when you deploy an environment, you can change the number and size of the virtual machines that are deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するときに、配置される仮想マシンの数とサイズを変更できることに留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>However, this table lists the number of cores required to deploy each environment in its <bpt id="p1">*</bpt>default<ept id="p1">*</ept> configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次のテーブルでは、その<bpt id="p1">*</bpt>既定<ept id="p1">*</ept>コンフィギュレーションで各環境を配置するために必要なコアの数を一覧にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Environment type:<ept id="p1">**</ept> - Demo</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境タイプ:<ept id="p1">**</ept> - デモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Environment name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Number of cores to deploy the environment in its default configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の構成で環境を配置するコアの数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>AX 2012 R3 demo</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 デモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>8 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>AX 2012 R3 CU8 demo</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 CU8 デモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>8 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Retail essentials demo</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials デモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>8 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Environment type:<ept id="p1">**</ept> - Dev/test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境タイプ:<ept id="p1">**</ept> - 開発/テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Environment name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Number of cores to deploy the environment in its default configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の構成で環境を配置するコアの数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Development</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>9 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">9 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Development with shared SQL Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有 SQL Server による開発</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>14 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">14 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>13 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">13 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Retail essentials dev/test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials 開発/テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>4 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Retail e-commerce dev/test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail E-commerce 開発/テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>4 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Retail mobility dev/test</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Mobility 開発/テスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>4 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">**</bpt>Environment type:<ept id="p1">**</ept> - High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境タイプ:<ept id="p1">**</ept> - 高可用性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Environment name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Number of cores to deploy the environment in its default configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の構成で環境を配置するコアの数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>High availability environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>45 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">45 コア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>If you already have an Azure subscription, note the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure のサブスクリプションを既に持っている場合、次に注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>To view the size of your subscription:<ept id="p1">**</ept> You can view the size of your subscription in the Azure management portal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>定期売買のサイズを表示する:<ept id="p1">**</ept>Azure 管理ポータルで、定期売買のサイズを表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>To do so, log on to the <bpt id="p1">[</bpt>Azure management portal<ept id="p1">](https://manage.windowsazure.com/)</ept>, and then click <bpt id="p2">**</bpt>Settings<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Usage<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、[<bpt id="p1">[</bpt>Azure管理ポータル<ept id="p1">](https://manage.windowsazure.com/)</ept>] にログオンし、<bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p3">**</bpt>使用<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>To increase the size of your subscription:<ept id="p1">**</ept> To increase the size of your subscription, you’ll need to create a support ticket with the Azure support team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>定期購読のサイズを増やす:<ept id="p1">**</ept> 定期売買のサイズを増やすには、Azure サポート チームにてサポート チケットを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To do so, go to the <bpt id="p1">[</bpt>Azure support options<ept id="p1">](http://azure.microsoft.com/en-us/support/options/)</ept> page, and then click <bpt id="p2">**</bpt>Get Support<ept id="p2">**</ept> to create the support ticket.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、[<bpt id="p1">[</bpt>Azure サポート オプション<ept id="p1">](http://azure.microsoft.com/en-us/support/options/)</ept>] ページに移動し、<bpt id="p2">**</bpt>サポートを受ける<ept id="p2">**</ept> をクリックしてサポート チケットを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>When creating the support ticket, be sure to indicate that the ticket is for billing support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート チケットを作成するとき、チケットが課金サポートに対応していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The Cloud Solution Provider (CSP) program is currently not supported with Lifecycle Services due to the Azure Resource Manager (ARM) requirement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ソリューション プロバイダー (CSP) プログラムは、Azure Resource Manager (ARM) 要件のため Lifecycle Services によって現在サポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Purchase and Azure support plan</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書および Azure サポート計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Azure support plans provide technical and billing support for Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure サポート計画では Azure の技術および課金サポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The Azure support plans offer flexible support options that will allow you to select the right level of support for your Azure deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure サポート プランは、Azure 展開のサポーの適切なレベルを選択できる柔軟なサポート オプションを提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The support options range from support services included with your Azure subscription at no charge to premier support services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート オプションには、Azure サブスクリプションに含まれているサポート サービスから、無料のサポート サービスまでさまざまです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>To learn about the available support plans and to purchase a plan, see the <bpt id="p1">[</bpt>Azure support plans<ept id="p1">](http://www.windowsazure.com/en-us/support/plans/)</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">利用可能なサポート プランについて学び、プランを購入するには、[<bpt id="p1">[</bpt>Azure サポート計画<ept id="p1">](http://www.windowsazure.com/en-us/support/plans/)</ept>] ページをご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Become familiar with the Azure management portal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 管理ポータルを使いこなせるようになります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The Azure management portal provides developers and IT professionals the ability to provision, configure, monitor, and manage their Azure components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 管理ポータルは、開発者および IT プロフェッショナルに、その Azure コンポーネントをプロビジョニング、構成、監視、および管理する機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>It’s important to become familiar with the management portal because you’ll use it to:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後使用するために、管理ポータルについてよく理解しておくことが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Upload a management certificate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理証明書をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>(The management certificate enables Lifecycle Services to deploy AX 2012 R3 environments on Azure on your behalf.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(管理証明書を使用すると、Lifecycle Services はユーザーに代わって Azure に AX 2012 R3 環境を配置できます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Connect to virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシンに接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Monitor the health and status of your AX 2012 R3 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 環境の正常性および状態を監視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>After you purchase an Azure subscription, you can access the management portal by clicking <bpt id="p1">[</bpt>here.<ept id="p1">](https://manage.windowsazure.com/?whr=live.com)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure サブスクリプションを購入した後、<bpt id="p1">[</bpt>ここ。<ept id="p1">](https://manage.windowsazure.com/?whr=live.com)</ept> をクリックして管理ポータルにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The following image shows the management portal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、管理ポータルを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>PlanYouAXR3DeploymentonAzure1<ept id="p1">](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>PlanYouAXR3DeploymentonAzure1<ept id="p1">](./media/planyouaxr3deploymentonazure1.jpg)](./media/planyouaxr3deploymentonazure1.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Become familiar with the Azure VM agent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure VM エージェントを使いこなせるようになります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The Azure VM Agent is now automatically deployed with every VM deployed via Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure VM エージェントは、Lifecycle Services を通じて展開されたすべての VM で自動的に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The Azure VM Agent is used to install, configure, manage and run Azure Virtual Machine Extensions (VM Extensions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure VM エージェントは、Azure 仮想マシン拡張 (VM 拡張) インストール、コンフィギュレーション、管理、実行するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>VM extensions can help you monitor and manage your VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM 拡張機能は、VM を監視および管理するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Consider Cloud Services resource requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド サービスのリソース要件を検討する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>When a topology is deployed, the deployment system will inspect the virtual machine (VM) SKUs that were selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トポロジが配置されると、配置システムは選択された仮想マシン (VM) の SKU を検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In order to ensure that Azure deploys these VMs to the proper clusters where the VMs are available, each level of VM SKU must have its own Azure Cloud Service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure がこれらの VM を VM が使用可能である適切なクラスターに配置していることを確認するために、VM SKU の各レベルに独自の Azure クラウド サービスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The VM SKU breakdown is as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM SKU の内訳は次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>SKU<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>最小在庫管理単位<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Size<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サイズ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">A</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Standard A’s <ph id="ph1">\[</ph>A0-A4<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 A の <ph id="ph1">\[</ph>A0-A4<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>AM</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">午前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Standard A's <ph id="ph1">\[</ph>A5-A7<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 A の <ph id="ph1">\[</ph>A5-A7<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>AL</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AL</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Standard A’s (large) <ph id="ph1">\[</ph>A8-A11<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 A の (大) <ph id="ph1">\[</ph>A8-A11<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>D</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">D</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Standard D’s <ph id="ph1">\[</ph>all D series<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 D の<ph id="ph1">\[</ph>すべての D シリーズ<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>DS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Standard DS’s <ph id="ph1">\[</ph>all DS series<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 DS の<ph id="ph1">\[</ph>すべての DS シリーズ<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>G</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">G</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Standard G’s <ph id="ph1">\[</ph>all G series<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準 G の<ph id="ph1">\[</ph>すべての G シリーズ<ph id="ph2">\]</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>A Cloud Service will be created with the following naming scheme: Version-Topology-EnvironmentName-SKU-GUID Please consider the Cloud Services resource requirements for your deployments and request additional Cloud Services capacity in your Azure Subscription from Azure Support if necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Version-Topology-EnvironmentName-SKU-GUID という名前付けスキームを含むクラウド サービスが作成されます。必要に応じて、配置のためのクラウド サービス リソース要件を検討し、Azure サポートから Azure サブスクリプションの追加クラウド サービス能力を要求してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Plan for storage accounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージ アカウントの計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>For each project created in Lifecycle Services, one or more distinct storage accounts will be created in the Azure subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services で作成された各プロジェクトについては、1 つまたは複数の個別のストレージ アカウントが Azure 定期売買で作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>A storage account is created when you connect your project to your Azure subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージ アカウントは、プロジェクトを Azure サブスクリプションに接続すると作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>This storage account is a Locally Redundant Storage (LRS) account, and is used to house scripts and VHDs which are required for deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このストレージ アカウントは、ローカル冗長ストレージ (LRS) アカウントであり、展開に必要なスクリプトと VHD を格納するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>An additional Premium storage account is created for each project when the first Premium storage-enabled topology is deployed from the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の Premium ストレージ有効トポロジがプロジェクトから配置されると、各プロジェクトが作成され Premium ストレージ アカウントが追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Storage accounts are not shared across Lifecycle Services projects, even if the deployments are to the same Azure subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージ アカウントは、配置が同じ Azure サブスクリプションに行われる場合でも、Lifecycle Services プロジェクト間で共有されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>When a Premium storage account is created, it too is created as LRS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium ストレージ アカウントが作成されると、それもまた LRS として作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>For more information about storage, click <bpt id="p1">[</bpt>here<ept id="p1">](http://azure.microsoft.com/en-us/pricing/details/storage)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストレージの詳細については、<bpt id="p1">[</bpt>ここ<ept id="p1">](http://azure.microsoft.com/en-us/pricing/details/storage)</ept> をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Consider which topologies and the number of environments that will be deployed into the same Lifecycle Services (LCS) project and Azure Connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Lifecycle Services (LCS) プロジェクトと Azure コネクタに展開されるトポロジと環境の数を検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Premium storage account aside, by default there is 1 storage account for each LCS project and Azure Connector.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium ストレージ アカウントとは別に、既定では、LCS プロジェクトおよび Azure コネクタごとにストレージ アカウントが 1 つ存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Be aware that Azure storage has <bpt id="p1">[</bpt>limits<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storage-limits)</ept>, specifically 20,000 IOPS (input/output operations per second) per standard storage account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Storage には<bpt id="p1">[</bpt>限度<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storage-limits)</ept>があるので注意してください。具体的には、標準ストレージ アカウントあたり 20,000 IOPS (秒単位の入力/出力オペレーション) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Combined with 500 IOPS per VHD, that leaves roughly 40 <bpt id="p1">***</bpt>highly utilized<ept id="p1">***</ept> VHDs before throttling occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VHD あたり 500 IOPS と組み合わせると、調整が発生する前に約 40 個の<bpt id="p1">***</bpt>利用効率が高い<ept id="p1">***</ept> VHDが残されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>To mitigate this, we recommend that you leverage multiple Azure Connectors and/or multiple LCS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを軽減するには、複数の Azure コネクタや複数の LCS プロジェクトを活用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>For example, consider having production environments in one LCS project, and Dev/Test environments in another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、1 つの LCS プロジェクトで製造環境を、別で開発/テスト環境を検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Not all VHDs that LCS deploys will be highly utilized, such as the installation VHD.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストール VHD など、LCS が配置するすべての VHD が高度に使用されるわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Plan your SQL Server configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 構成の計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Azure Premium Storage delivers high-performance, low-latency disk support for I/O intensive workloads running on Azure virtual machines (VMs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>With Premium Storage, your applications can have up to 32 TB of storage per VM, achieve 50,000 IOPS per VM, and have extremely low latencies for read operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS を達成し、読み取り操作での待機時間は非常に短くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Premium Storage is required for AX 2012 R3 deployments that will be used in a production capacity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium Storage は、生産能力で使用される AX 2012 R3 配置に必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Premium Storage is enabled by default for High Availability deployments when Azure DS-series VMs are selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DS シリーズ VM が選択されている場合、高可用性配置では Premium Storage が既定で有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Premium Storage is only offered on DS-series VMs at this time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium Storage は、現時点では DS シリーズ VM 上でのみ提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Premium Storage is enabled exclusively for the SQL Server AlwaysOn database servers, while non-Premium storage is used for all other storage needs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のすべての記憶域ニーズに非 Premium ストレージが使用されているとき、SQL Server AlwaysOn データベース サーバーだけで Premium Storage が有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>When a SQL Server AlwaysOn availability set is created, Lifecycle Services will attach a disk for every disk slot supported by the DS-series VM selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server AlwaysOn 可用性セットが作成されると、Lifecycle Services は、選択された DS シリーズ VM でサポートされているすべてのディスク スロットに対してディスクをアタッチします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>For more information about VM disk capacity, click <bpt id="p1">[</bpt>here<ept id="p1">](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM ディスク能力の詳細については、<bpt id="p1">[</bpt>ここ<ept id="p1">](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Different VM sizes will come with varying maximums for throughput and IOPS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なる VM サイズには、スループットと IOPS の最大値が変化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>As a result, when you are planning your SQL Server configuration, please be familiar with these limitations to ensure that you are deploying the most efficient and cost effective solution for your business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、 SQL Server の構成を計画しているときは、ビジネスに最も効率的でコスト効果の良いソリューションを展開するために、これらの制限に精通してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Please follow the guidance found in <bpt id="p1">[</bpt>Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)</ept>, particularly the section, <bpt id="p2">**</bpt>Throttling when using Premium Storage<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Premium Storage: Azure 仮想マシン ワークロード向け高性能ストレージ<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)</ept>に関するページ (特に、<bpt id="p2">**</bpt>Premium Storage の使用時の調整<ept id="p2">**</ept>に関するセッション) にあるガイドラインに従ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The SQL Server AlwaysOn availability set is created automatically through Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server AlwaysOn 可用性セットは、Lifecycle Services を通じて自動的に作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>It is important to consider your data and performance needs before deploying a High Availability topology for use with a production system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産システムで使用するための高可用性トポロジを配置する前に、データおよびパフォーマンスのニーズを考慮することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Please refer to Azure Premium Storage information <bpt id="p1">[</bpt>here<ept id="p1">](http://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Premium Storage については、<bpt id="p1">[</bpt>こちら<ept id="p1">](http://azure.microsoft.com/en-us/documentation/articles/storage-premium-storage-preview-portal/)</ept>をご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Once you have planned your deployment with Premium Storage, the High Availability topology provides configuration options to help you achieve your cost and performance objectives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium Storage で配置を計画すると、高可用性トポロジには、原価とパフォーマンスの目標を達成するためのコンフィギュレーション オプションが提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Under Advanced Settings for the High Availability topology, the following SQL Server configuration options appear:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性のトポロジの詳細設定では、次の SQL Server 構成オプションが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source><bpt id="p1">**</bpt>Customize the SQL Server image configuration<ept id="p1">**</ept> – This option allows the use of a custom SQL Server Enterprise image or an Azure Gallery SQL Server Enterprise image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server イメージ コンフィギュレーションのカスタマイズ<ept id="p1">**</ept> - このオプションを使用すると、カスタム SQL Server Enterprise イメージまたは Azure Gallery SQL Server Enterprise イメージを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Custom SQL Server image (default) – This image contains a trial edition of SQL Server Enterprise 2014.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム SQL Server イメージ (既定) - このイメージには、SQL Server Enterprise 2014の試用版が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The trial license is enabled for 3-6 months.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価版ライセンスは 3〜6 か月間有効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Use this option if you want to use an existing EA/etc. license.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の EA/etc. ライセンスを使用する場合は、このオプションを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Gallery SQL Server image – This image contains SQL Server Enterprise 2014 and uses consumption-based Azure pricing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギャラリー SQL Server イメージ – このイメージには SQL Server Enterprise 2014 が含まれており、消費に基づく Azure 価格決定を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>More information can be found on the <bpt id="p1">[</bpt>Azure Virtual Machines Pricing<ept id="p1">](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/#sql-server)</ept> page and the <bpt id="p2">[</bpt>SQL Server in Azure Virtual Machines<ept id="p2">](https://msdn.microsoft.com/library/azure/jj823132.aspx)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Azure 仮想マシンの価格決定<ept id="p1">](https://azure.microsoft.com/en-us/pricing/details/virtual-machines/#sql-server)</ept>ページと <bpt id="p2">[</bpt>Azure 仮想マシンの SQL Server<ept id="p2">](https://msdn.microsoft.com/library/azure/jj823132.aspx)</ept> で確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source><bpt id="p1">**</bpt>Customize the SQL Server storage space configuration<ept id="p1">**</ept> – You can specify the number and size of the disks that will be attached to the SQL Server VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SQL Server のストレージ領域コンフィギュレーションのカスタマイズ<ept id="p1">**</ept> - SQL Server VM に関連付けられるディスクの数とサイズを指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Keep the following points in mind when specifying the number of disks that should be used to create the storage space within SQL Server:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 内でストレージ領域の作成に使用する必要があるディスクの数を指定する場合は、次の点に留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The VM size that is selected for the database server dictates how many disks are supported by that VM SKU.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース サーバーのために選択されている VM サイズで、その VM SKU でサポートされるディスクの数が決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Information about the number of disks that are supported by each VM can be found <bpt id="p1">[</bpt>here<ept id="p1">](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 VM でサポートされているディスクの数に関する情報は、<bpt id="p1">[</bpt>ここ<ept id="p1">](https://msdn.microsoft.com/en-us/library/azure/dn197896.aspx)</ept>で確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>One of the available disk slots on the VM will be used by the Lifecycle Services deployment service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM で使用可能なディスク スロットの 1 つは、Lifecycle Services 配置サービスで使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>This means the VM’s maximum number of disks—minus 1—equals the available slots to fill.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、VM の最大ディスク数 (マイナス1) が、使用可能なスロットを満たすことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Leaving this setting blank will allow the deployment service to attach disks up to the maximum supported by the VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定を空白のままにすると、配置サービスによって VM でサポートされている最大までディスクを関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>It is recommended for production deployments that the maximum disks be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大のディスクが使用される運用配置の場合にお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Keep the following points in mind when specifying the size (in GB) of each disk attached to the VM:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM に関連付けられている各ディスクのサイズ (GB 単位) を指定する場合、次の点に留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Allowed values are 100 GB – 1024 GB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">100 GB – 1024 GB 値を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Default is 128 GB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値は 128 GB です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>The size of the disk used dictates the Premium Storage tier used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるディスクのサイズは、使用される Premium Storage 階層を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The Premium Storage tier dictates cost, IOPS per disk, and throughput of the system being deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Premium Storage 層は、原価、ディスクあたりの IPOPS、および展開されるシステムのスループットを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>For more information, click <bpt id="p1">[</bpt>here<ept id="p1">](http://azure.microsoft.com/en-us/pricing/details/storage/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>ここ<ept id="p1">](http://azure.microsoft.com/en-us/pricing/details/storage/)</ept> をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>All disks are formatted to 64k cluster size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのディスクは 64k クラスター サイズにフォーマットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This results in up to a 20% increase in performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、パフォーマンスが最大 20％ 向上します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>TempDB and logs are deployed onto storage spaces as to benefit from the performance gains.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TempDB とログは、パフォーマンスの向上のために記憶域上に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>One virtual disk is created over the number of disks configured for the storage space.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのストレージ領域にコンフィギュレーションされているディスクの数に対して、1 つの仮想ディスクが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The virtual disk is then partitioned as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、仮想ディスクは次のようにパーティション化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>SQL data = 1/2 of the total size of pool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL データ = プールの合計サイズの 1/2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>SQL logs = 1/4 of the total size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL ログ = 合計サイズの 1/4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>SQL Temp db = 1/8 of the total size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Temp db = 合計サイズの 1/8</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>SQL backup = remaining 1/8 of the total size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL バックアップ = 合計サイズの残り 1/8</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Other considerations to keep in mind:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の考慮事項を念頭に置く必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>When planning your deployment, ensure that Premium Storage is available in the Azure region you are targeting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置を計画するときは、対象とする Azure 領域で Premium Storage を使用できることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>For more information, click <bpt id="p1">[</bpt>here<ept id="p1">](http://azure.microsoft.com/en-us/services/preview/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>ここ<ept id="p1">](http://azure.microsoft.com/en-us/services/preview/)</ept> をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If you have a VPN/Express Route connection (or plan to) between your corporate network and Azure, please ensure this is done for an Azure region that supports Premium Storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社のネットワークと Azure の間で VPN/Express ルート接続 (または計画) がある場合、Premium ストレージ アカウントをサポートしている Azure 地域でこれが行われていることが確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Consult the <bpt id="p1">[</bpt>Azure Premium Storage documentation<ept id="p1">](http://azure.microsoft.com/en-us/documentation/services/storage/)</ept> to understand limitations of use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用に関する制限について理解するためには <bpt id="p1">[</bpt>Azure Premium Storage ドキュメント<ept id="p1">](http://azure.microsoft.com/en-us/documentation/services/storage/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>If non-Premium Storage VMs are deployed with the High Availability topologies, all of the above SQL Server configuration settings are applicable; however, Premium Storage benefits will not apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可用性トポロジーで非 Premium ストレージ VM がデプロイされている場合は、上記のすべての SQL Server のコンフィギュレーションを適用できますが、Premium ストレージのメリットは適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>When setting up your Lifecycle Services project for deployment, you must select a region that supports Premium Storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置ために Lifecycle Services プロジェクトを設定するとき、Premium Storage をサポートする地域を選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>SQL Server best practices implemented by the deployment service include those recommended by the SQL Server team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開サービスにより実装される SQL Server ベスト プラクティスには、SQL Server チームにより推奨されるベスト プラクティスが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>For more information, click <bpt id="p1">[</bpt>here<ept id="p1">](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>ここ<ept id="p1">](http://blogs.technet.com/b/dataplatforminsider/archive/2014/09/12/new-vm-images-optimized-for-transactional-and-dw-workloads-in-azure-vm-gallery.aspx)</ept> をクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>In addition, the following items are done:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、次の項目が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Multiple temp files (one per CPU core).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の一時ファイル (CPU コアごとに 1 つ)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set max memory for SQL Server to 90% of available machine RAM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server の最大メモリを使用可能なコンピューター RAM の 90% に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Set max degree of parallelism.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">並列処理の最大限度を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Enabled trace flags  -T1204, -T1222.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トレース フラグの有効  -T1204、 -T1222。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Estimate costs and understand the Azure billing process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">減価を見積もり、Azure 請求プロセスに同意</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>To help estimate the cost of your AX 2012 R3 deployment on Azure, use the <bpt id="p1">[</bpt>Azure pricing calculator<ept id="p1">](http://azure.microsoft.com/en-us/pricing/calculator/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure での AX 2012 R3 の展開コストを見積もるには、<bpt id="p1">[</bpt>Azure 価格計算ツール<ept id="p1">](http://azure.microsoft.com/en-us/pricing/calculator/)</ept>を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>It’s also important to understand the Azure billing process before you deploy AX 2012 R3 on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure に AX 2012 R3 を配置する前に、Azure 請求プロセスについて理解することも重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>For an overview of the Azure billing process, links to sample invoices, and information about how to download daily usage data for the current billing period, see <bpt id="p1">[</bpt>Understand your bill<ept id="p1">](http://azure.microsoft.com/en-us/support/understand-your-bill/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要については、<bpt id="p1">[</bpt>請求書を理解する<ept id="p1">](http://azure.microsoft.com/en-us/support/understand-your-bill/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>**Note: **Keep in mind, you can shut down an AX 2012 R3 environment that has been deployed on Azure when it’s not in use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">**注記:** 使用されていないときに Azure 上に配置されている AX 2012 R3 環境をシャット ダウンすることができることに留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>For example, you may want to shut down an environment on the weekends to reduce costs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、コスト削減のため週末に環境をシャット ダウンする場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>When you shut down an environment, the environment still exists; however, the virtual machines in the environment are shut down.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境をシャット ダウンすると、その環境はまだ存在します。ただし、その環境内の仮想マシンはシャット ダウンされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>You won’t be charged for the virtual machines when they’re not running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシンが実行されていないときは、それに対して課金されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>For more information, see “How do I shut down an environment?”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「環境をシャット ダウンする方法とは」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>in the <bpt id="p1">[</bpt>Manage your Microsoft Dynamics AX 2012 R3 deployment on Azure<ept id="p1">](manage-2012-r3-deployment-azure.md)</ept> article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での Microsoft Dynamics AX 2012 R3 配置の管理<ept id="p1">](manage-2012-r3-deployment-azure.md)</ept>という記事の中です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Consider legal and regulatory requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">法的および規制要件を考慮する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Microsoft runs Azure services with common operational practices and features across multiple geographies and jurisdictions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、複数の地域や税務署にわたる一般的な運用方法と機能で Azure サービスを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>However, it is ultimately up to you to determine if Microsoft services satisfy your regulatory needs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft サービスがユーザーの規制の必要を満たしているかどうかを判断するのは、最終的にはユーザー次第となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>To help provide you with up-to-date information, the <bpt id="p1">[</bpt>Azure trust center<ept id="p1">](http://azure.microsoft.com/en-us/support/trust-center/)</ept> provides the following information about security, privacy, and compliance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最新の情報を提供するために、<bpt id="p1">[</bpt>Azure セキュリティ センター<ept id="p1">](http://azure.microsoft.com/en-us/support/trust-center/)</ept> はセキュリティ、プライバシー、コンプライアンスに関する以下の情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source><bpt id="p1">**</bpt>Security<ept id="p1">**</ept> The <bpt id="p2">[</bpt>Azure security page<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/security/)</ept> provides an overview of the provisions Microsoft is taking to provide a secure environment within geographically dispersed datacenters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>、<bpt id="p2">[</bpt>Azure セキュリティ ページ<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/security/)</ept> は地理的に分散されているデータ センター内に安全な環境を提供するために Microsoft が取っている条項の概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Among the extensive list of security-related resources, the <bpt id="p1">[</bpt>Standard Response to Request for Information: Security and Privacy<ept id="p1">](https://www.microsoft.com/en-us/download/details.aspx?id=26647)</ept> white paper outlines how Azure meets the suggested principals and mapped them to the International Standards Organization (ISO) 27001:2005 and ISO 27002.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ関連リソースの広範なリストの中で、<bpt id="p1">[</bpt>情報の要求についての標準応答: セキュリティおよびプライバシー<ept id="p1">](https://www.microsoft.com/en-us/download/details.aspx?id=26647)</ept> ホワイト ペーパーがどのように Azure の提案されたプリンシパルを満たし、国際標準化機構 (ISO) 27001:2005 および ISO 27002 にマップされているかを概説します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source><bpt id="p1">**</bpt>Privacy<ept id="p1">**</ept> The <bpt id="p2">[</bpt>Azure privacy page<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/privacy/)</ept> includes links to multiple resources that describe privacy practices of the Azure environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライバシー<ept id="p1">**</ept> <bpt id="p2">[</bpt>Azure プライバシー ページ<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/privacy/)</ept> Azure 環境のプライバシーに関する取り組みを説明する複数のリソースへのリンクが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>It includes a link to the <bpt id="p1">[</bpt>Azure privacy statement<ept id="p1">](http://www.windowsazure.com/en-us/support/legal/privacy-statement/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure のプライバシーに関する声明<ept id="p1">](http://www.windowsazure.com/en-us/support/legal/privacy-statement/)</ept>へのリンクが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source><bpt id="p1">**</bpt>Compliance<ept id="p1">**</ept> The <bpt id="p2">[</bpt>Azure compliance page<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/compliance/)</ept> provides resources to help you comply with the specific laws and regulations applicable to your unique industry and use scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンプライアンス<ept id="p1">**</ept> <bpt id="p2">[</bpt>Azure コンプライアンス ページ<ept id="p2">](http://www.windowsazure.com/en-us/support/trust-center/compliance/)</ept>は、独自の業界に適用される特定の法律および規制を順守し、シナリオを使用するためのリソースを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Consider licensing requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス供与の要件の検討</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Licensing the various components of the AX 2012 R3 virtual machine environment is an important consideration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 仮想マシン環境のさまざまなコンポーネントのライセンス供与は、重要な考慮事項です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>For deployments on Azure, you will want to evaluate the special licensing terms specific to Azure and the impact that these terms have on the overall suitability of the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure での展開は、 Azure に固有な特別なライセンス条項であるか、およびそれらの条項がソリューションの全体的な適合性を備えているかを評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Licensing requirements vary based on the type of AX 2012 R3 virtual machine environment that you deploy on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス供与の要件は、Azure に配置する AX 2012 R3 仮想マシン環境の種類によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>The following table provides more information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに詳細を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Type of environment<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>環境のタイプ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Licensing requirements<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ライセンス要件<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Demo</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>The software that is included in the virtual machine environment is time-bound and licensed according to the terms in the Software License Terms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン環境に含まれるソフトウェアは、ソフトウェア ライセンス条項の項目に従って、時間制限付きで使用許諾されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>Software License Terms for the AX 2013 R3 demo environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>AX 2013 R3 デモ環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>Software License Terms for the AX 2013 R3 CU8 demo environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>AX 2013 R3 CU8 デモ環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>Software License Terms for the Retail essentials demo environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397371"&gt;</bpt>5. Retail Essentials デモ環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Dev/test and high availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発/テストおよび高可用性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>All software included in the virtual machine environment must be properly licensed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン環境を含めすべてのソフトウェアには適切なライセンスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Please investigate your licensing needs thoroughly with your partner and your Microsoft representative.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パートナーとマイクロソフトの担当者共に、ライセンスのニーズを十分に調査してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>You will need to investigate the terms for each piece of software that is included in the virtual machine environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン環境に含まれる個々のソフトウェアの条件を調査する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>For the complete list of software that is included in the virtual machine environment, review the Software License Terms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仮想マシン環境に含まれるソフトウェアの完全な一覧については、ソフトウェア ライセンス条項を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>Software License Terms for the development environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>開発環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>Software License Terms for the development with shared SQL Server environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>共有の SQL Server 環境による開発用のソフトウェア ライセンス条件<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>Software License Terms for the test environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>テスト環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;amp;clcid=0x409"&gt;</bpt>Software License Terms for the Retail essentials dev/test environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507496&amp;amp;amp;clcid=0x409"&gt;</bpt>5. Retail Essentials 開発/テスト環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507494"&gt;</bpt>Software License Terms for the Retail e-commerce dev/test environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507494"&gt;</bpt>5. Retail E-commerce 開発/テスト環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507496"&gt;</bpt>Software License Terms for the Retail mobility dev/test environment<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkID=507496"&gt;</bpt>5. Retail Mobility 開発/テスト環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>Software License Terms for the high availability environment<ept id="p1">&lt;/a&gt;</ept> When reviewing the licensing terms and requirements, you need to pay special attention to any terms that apply specifically to deploying on Azure, as well as terms that apply to your intended use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>高可用性環境のソフトウェア ライセンス条項<ept id="p1">&lt;/a&gt;</ept>ライセンス条項と要件を確認する際には、Azure に配置するために特に適用される条項、および使用目的に適用される条項に特に注意する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>For example, Microsoft Office has terms that are specific to Azure; but those terms vary depending on whether you deploy Office for development or test purposes, or whether you deploy Office for production purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、Microsoft Office は Azure に固有の条件を持ちますが、これらの条件は、開発またはテスト目的で Office を配置するか、または生産目的で Office を配置するかどうかによって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Some resources to help you get started are linked to below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始するうえで役立ついくつかのリソースを以下のリンクに示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Most of the resources that are linked to below contain links to in-depth information for several products and scenarios; however, you may need to review additional information, as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下にリンクされているリソースのほとんどに、複数の製品およびシナリオの詳細な情報へのリンクが含まれています。ただし、追加の情報を確認しなければならない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>This information is provided to help guide your authorized use of products you license; it is not your agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報は、ライセンスを取得した製品の承認済みの使用に関するガイドに役立つ情報です。 同意ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Your use of products licensed under your volume license agreement is governed by the terms and conditions of that agreement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボリューム ライセンス契約にもとづいてライセンスされている製品の使用は、その契約の条件によって支配されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>In the case of any conflict between information linked here and your agreement, the terms and conditions of your agreement control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここにリンクされている情報と契約に矛盾がある場合、契約の使用条件が有効となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Virtual machines licensing FAQ<ept id="p1">&lt;/strong&gt;</ept> Common questions regarding licensing on Azure virtual machines are answered on <bpt id="p2">&lt;a href="http://www.windowsazure.com/en-us/pricing/licensing-faq/"&gt;</bpt>this page<ept id="p2">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>仮想マシン ライセンスによく寄せられる質問<ept id="p1">&lt;/strong&gt;</ept> Azure 仮想マシンのライセンスに関するよくある質問は、<bpt id="p2">&lt;a href="http://www.windowsazure.com/en-us/pricing/licensing-faq/"&gt;</bpt>このページ<ept id="p2">&lt;/a&gt;</ept>で回答されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Microsoft Product Use Rights and Product List<ept id="p1">&lt;/strong&gt;</ept> Learn more about Microsoft Volume Licensing product licensing models, programs, scenarios, and terms and conditions to help you make effective business decisions and maximize the value of your IT purchases on <bpt id="p2">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>this page<ept id="p2">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Microsoft 製品の使用権限と製品リスト<ept id="p1">&lt;/strong&gt;</ept>ビジネス上の意思決定を効果的にし、IT 購入価値を最大化するために、<bpt id="p2">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>このページ<ept id="p2">&lt;/a&gt;</ept>で、Microsoft ボリューム ライセンス製品のライセンスモデル、プログラム、シナリオ、および使用条件について詳細を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source><bpt id="p1">&lt;strong&gt;</bpt>License Mobility through Software Assurance on Azure program<ept id="p1">&lt;/strong&gt;</ept> License Mobility through Software Assurance gives Microsoft volume licensing customers the flexibility to deploy eligible server applications with active Software Assurance on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Azure プログラムのソフトウェア保証によるライセンス モビリティ<ept id="p1">&lt;/strong&gt;</ept>ソフトウェア保証によるライセンス モビリティにより、Microsoft ボリューム ライセンスの顧客は、Azure でアクティブなソフトウェア保証を使用して、適格なサーバー アプリケーションを配置する柔軟性を得ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>With this Software Assurance benefit, there is no need to purchase new licenses and no associated mobility fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このソフトウェア保証給付金では、新しいライセンスを購入する必要がなく、関連するモビリティ費用がかかりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>This enables you to easily deploy existing licenses on the Azure cloud platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、既存のライセンスを Azure クラウド プラットフォームに簡単に展開できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For more information, see <bpt id="p1">&lt;a href="http://www.windowsazure.com/en-us/pricing/license-mobility/"&gt;</bpt>this page<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">&lt;a href="http://www.windowsazure.com/en-us/pricing/license-mobility/"&gt;</bpt>このページ<ept id="p1">&lt;/a&gt;</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>For Development, Test, and High Availability topologies trial versions of SharePoint, Visual Studio, SQL Server, and Office are provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発、テスト、および SharePoint の高可用性トポロジ トライアル版用に、Visual Studio、SQL Server および Office が提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>The trials range from 30-180 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価の範囲は 30〜180 日間です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Please apply licenses accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それに応じてライセンスを適用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Microsoft Dynamics AX volume licensing buyer’s guide<ept id="p1">&lt;/strong&gt;</ept> For an overview of key licensing options with Microsoft Dynamics AX, see <bpt id="p2">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>this page<ept id="p2">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Microsoft Dynamics AX ボリューム ライセンス バイヤー ガイド<ept id="p1">&lt;/strong&gt;</ept> Microsoft Dynamics AX を使用したキー ライセンス オプションの概要については、<bpt id="p2">&lt;a href="http://go.microsoft.com/fwlink/?LinkId=397363"&gt;</bpt>このページ<ept id="p2">&lt;/a&gt;</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Shared computer activation for Office 365 ProPlus<ept id="p1">&lt;/strong&gt;</ept> Shared computer activation lets you to deploy Office 365 ProPlus to a computer in your organization that is accessed by multiple users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Office 365 ProPlus の共有コンピュータの有効化<ept id="p1">&lt;/strong&gt;</ept> 共有コンピューターの有効化により、複数のユーザーがアクセスする組織内のコンピュータに Office 365 ProPlus を配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>For more information, see <bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/dn782860(v=office.15).aspx"&gt;</bpt>this page<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/dn782860(v=office.15).aspx"&gt;</bpt>このページ<ept id="p1">&lt;/a&gt;</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Select the AX 2012 R3 environment that you want to deploy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置する AX 2012 R3 環境を選択</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>You’ll use the Cloud-hosted environments tool in Lifecycle Services to deploy AX 2012 R3 environments on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 上に AX 2012 R3 環境を配置するには、Lifecycle Services のクラウド ホスト環境ツールを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>When you use the Cloud-hosted environments tool to deploy, you’ll need to select the type of environment that you want to deploy on Azure, such as a demo or development/test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ホスト環境ツールを使用して配置するとき、デモまたは開発/テスト環境などの、Azure 上に配置する環境のタイプを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Based on your selection, the Cloud-hosted environments tool provisions the appropriate number of virtual machines on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この選択に基づいて、クラウド ホスト環境ツールは Azure での仮想マシンの適切な数を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>These virtual machines have AX 2012 R3 components—and all of their prerequisites—already installed on them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの仮想マシンには、AX 2012 R3 コンポーネント (およびそれらの必要物すべて) がインストール済みです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>The following sections describe the AX 2012 R3 environments that you can deploy on Azure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、Azure に配置できる AX 2012 R3 環境について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>AX 2012 R3 and AX 2012 R3 CU8 demo environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Retail essentials demo environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials デモ環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Development environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Retail essentials dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Retail e-commerce dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail E-commerce 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Retail mobility dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail mobility 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>High availability environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>In these environments, SQL Server is configured to use the SQL<ph id="ph1">\_</ph>Latin1<ph id="ph2">\_</ph>General<ph id="ph3">\_</ph>CP1<ph id="ph4">\_</ph>CI<ph id="ph5">\_</ph>AS collation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような環境では、SQL Server は SQL<ph id="ph1">\_</ph>Latin1<ph id="ph2">\_</ph>General<ph id="ph3">\_</ph>CP1<ph id="ph4">\_</ph>CI<ph id="ph5">\_</ph>AS の照合順序を使用するよう構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>AX 2012 R3 and AX 2012 R3 CU8 demo environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 および AX 2012 R3 CU8 デモ環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>There are two AX 2012 R3 demo environments: one environment includes Cumulative Update 8, and the other does not.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの AX 2012 R3 デモ環境があります。1 方の環境には累積更新プログラム 8 があり、もう 1 つ方にはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>The following table lists details about each environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、それぞれの環境に関する詳細を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>The virtual machine included in each environment is a single-instance virtual machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各環境に含まれる仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Demo machine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ マシン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> DEMO-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>DEMO-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Active Directory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Domain Name Services (DNS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン名サービス (DNS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Remote Desktop Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Analysis Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Developer tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Microsoft SharePoint Server 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>Microsoft Office 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Office 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Web server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Enterprise Portal (EP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル (EP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Enterprise Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Help Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Business intelligence components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Reporting Services extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Analysis Services configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Analysis Services の構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Management Reporter components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Management Reporter server components</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter サーバー コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Management Reporter Report Designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter レポート デザイナー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Office add-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office アドイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Remote Desktop Services integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Developer tools:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Debugger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Visual Studio Tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Trace Parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Integration components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Web services on IIS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS 上の Web サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>.NET Business Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Management utilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Retail POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Retail Headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Synch Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Synch Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Real-time Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Async Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Retail Channel Configuration Utility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャンネル コンフィギュレーション ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Retail SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Retail online channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売オンライン チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>Retail Mass Deployment Toolkit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 一括配置ツールキット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Retail channel database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>RapidStart Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RapidStart Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Data Import/Export Framework components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワーク コンポーネント。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Data Import/Export Framework (DIXF) service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワーク (DIXF) サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>AOS component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Client component</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>Warehouse Mobile Devices Portal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫モバイル デバイス ポータル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>Connector for Microsoft Dynamics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Retail Essentials demo environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials デモ環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Deploy this environment to demo Retail essentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境を配置して、Retail Essentials をデモしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Retail essentials is a retail-centric configuration option for Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials は、Microsoft Dynamics AX の小売中心のコンフィギュレーション オプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>This environment includes one virtual machine, by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、既定で 1 台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>This virtual machine has Windows Server—and the software and sample data that you’ll need to demo Retail essentials—already installed on it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンには、Windows Server と、Retail Essentials をデモンストレーションするために必要なソフトウェアとサンプル データが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>The following table lists details about the default Retail essentials demo environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定の Retail Essentials デモ環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Retail essentials demo machine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials デモ コンピューター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> DEMO-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>DEMO-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Developer tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>AX 2012 R3 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Integration components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>.NET Business Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Retail Headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Real-time Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Async Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Retail channel database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Development environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Deploy these development environments when you need to quickly jumpstart a development effort for one to many developers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの開発者の開発努力を迅速に開始する必要がある場合は、これらの開発環境を配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Deploy a development virtual machine (VM) for each of your developers in a matter of hours instead of days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各開発者の開発用仮想マシン (VM) を数日ではなく数時間で展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>With a development environment, you have all the same domain and virtual network customizations that you have with the Test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境には、テスト環境と同じドメインおよび仮想ネットワーク カスタマイズすべてが用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Two topology options are provided for developer scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者シナリオには 2 つのトポロジ オプションが用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Development: Includes all-in-one VMs deployed with Active Directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発。Active Directory と共に展開されたオールインワンの VM を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>Development with shared SQL Server: Includes all-in-one VMs deployed with Active Directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有 SQL Server による開発。Active Directory と共に展開されたオールインワンの VM を含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>The database for each development VM instance will be deployed to a shared SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各開発 VM インスタンスのデータベースは、共有 SQL Server インスタンスに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>For those doing BI development you can deploy one instance for the purpose.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらの BI 開発の実行については、目的に対する 1 つのインスタンスを配置することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>All other instances will not deploy with BI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のすべてのインスタンスは BI で配置されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>The development VMs provided have all the AX 2012 R3 components installed with Visual Studio 2013 and AX 2012 R3 development tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">提供されている開発用 VM には、すべての AX 2012 R3 コンポーネントが Visual Studio 2013 および AX 2012 R3 開発ツールとともにインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>The VMs are joined to the Active Directory domain at deployment time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM は、展開時に Active Directory ドメインに結合されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>If you provided an Active Directory domain as a customization option, then the VMs will join to that domain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ オプションとして Active Directory ドメインを指定する場合は、VM はそのドメインに参加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Development VMs will be deployed up to the point of the AX 2012 R3 checklist, and have all the software installed that is listed in the Test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発 VM は、AX 2012 R3 チェックリストの時点まで配置され、すべてのソフトウェアがインストールされていることがテスト環境にリストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>This environment includes several virtual machines, by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、既定で数台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>These virtual machines have Windows Server—and the software that you’ll need for AX 2012 R3 testing purposes—already installed on them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの仮想マシンには、Windows Server と、AX 2012 R3 のテストに必要なすべてのソフトウェアが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source>The following table lists details about the default test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定のテスト環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source>Data Import/Export Framework (DIXF) components are not installed by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source>Domain controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D1: Basic compute tier (1 core, 3.5 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> AD-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>AD-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>Active Directory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source>Domain Name Services (DNS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン名サービス (DNS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>AOS server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> AOS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>AOS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>Microsoft Project Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Project Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Native Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネイティブ クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source>Office add-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office アドイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Remote Desktop Services integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>Integration components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>Web services on IIS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS 上の Web サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source>.NET Business Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>Management utilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>Retail Headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>Synch Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Synch Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Real-time Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>Async Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source>RapidStart Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RapidStart Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Database server/BI server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース サーバー/BIサーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> SQL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>SQL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source>Analysis Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source><bpt id="p1">
    &lt;strong&gt;</bpt>Note: <ept id="p1">&lt;/strong&gt;</ept> Reporting Services is configured to run in Native mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">
    &lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>To use Power View, you’ll need to complete additional configuration steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電源表示を使用するには、追加の構成手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source>For more information, see the prerequisites listed in <bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>Create a report by using Power View to connect to a cube<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>キューブに接続するための Power View を使用したレポートの作成<ept id="p1">&lt;/a&gt;</ept>に一覧表示された前提条件を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>Databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>Business intelligence components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source>Reporting Services extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Analysis Services configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Analysis Services の構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>Enterprise Portal server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> EP-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>EP-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>Microsoft SQL Server 2012 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2012 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source>Full-text Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フル テキスト検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Microsoft SharePoint Server 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source>Web server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Enterprise Portal (EP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル (EP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>Enterprise Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>Help Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source>Management Reporter components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>Management Reporter server components</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter サーバー コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Retail Online Channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売オンライン チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>Retail Channel Database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャンネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source>Retail Channel Configuration Utility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャンネル コンフィギュレーション ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Retail Hardware Station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail ハードウェア ステーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>Warehouse Mobile Devices Portal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫モバイル デバイス ポータル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>Connector for Microsoft Dynamics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>Client computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンピューター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> CLI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>CLI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source>Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>Developer tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>Microsoft SharePoint Server 2013 Client Components SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source>Microsoft Office 365 ProPlus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Office 365 ProPlus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>Management Reporter components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>Management Reporter Report Designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter レポート デザイナー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>Office add-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office アドイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>Remote Desktop Services integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source>Developer tools:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>Debugger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>Visual Studio Tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>Trace Parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source>Management utilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>Retail POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source>Remote Desktop Services server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> RDS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>RDS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source>Remote Desktop Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>Microsoft SQL Server 2012 Native Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2012 ネイティブ クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>Retail Essentials dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>Deploy this environment to develop or test features for Retail essentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境を配置して、Retail essentials の機能を開発またはテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source>This environment includes one virtual machine, by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、既定で 1 台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>This virtual machine has Windows Server—and the software that you’ll need for Retail essentials development and testing purposes—already installed on it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンには、Windows Server と、Retail Essentials の開発とテストで必要となるソフトウェアが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>The following table lists details about the default Retail essentials dev/test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定の Retail Essentials 開発/テスト環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>Retail essentials server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Essentials サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> ESSEN-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>ESSEN-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>Developer tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>AX 2012 R3 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>Databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source>Integration components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>.NET Business Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>Retail Headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Real-time Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>Async Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source>Retail channel database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>Retail ecommerce dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail E-commerce 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>Deploy this environment to create and test an online sales channel that is fully integrated with AX 2012 R3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境を配置して、AX 2012 R3 と完全に統合されたオンライン販売チャネルを作成し、テストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>This environment includes one virtual machine, by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、既定で 1 台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source>This virtual machine has Windows Server—and the software that you’ll need for Retail e-commerce—already installed on it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンには、Windows Server と、小売電子商取引に必要なソフトウェアが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>The following table lists details about the default Retail e-commerce dev/test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定の Retail E-commerce 開発/テスト環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>Retail e-commerce server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail E-commerce サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> E-COM-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>E-COM-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source>Microsoft SharePoint Server 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>AX 2012 R3 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>Retail online channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売オンライン チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>Retail channel database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source>Retail mobility dev/test environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail mobility 開発/テスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>Deploy this environment to enable your sales staff to process sales transactions, enter customer orders, and perform daily operations and inventory management with mobile devices anywhere in a store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境を配置することで、販売スタッフが販売トランザクションを処理し、顧客注文を入力し、店舗内のどこでもモバイル デバイスを使用して日々の操作と在庫管理を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>This environment includes one virtual machine, by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、既定で 1 台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>This virtual machine has Windows Server—and the software that you’ll need for Retail mobility—already installed on it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンには、Windows Server と、Retail mobilityに必要なソフトウェアが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source>The following table lists details about the default Retail mobility dev/test environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定の Retail Mobility 開発/テスト環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>The virtual machines in this environment are single-instance virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、単一インスタンスの仮想マシンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>Single-instance virtual machines are not covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シングル インスタンス仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>Retail server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> MOBIL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>MOBIL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source>AX 2012 R3 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>Retail channel database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>High availability environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高可用性環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>Deploy this environment to use AX 2012 R3 in an environment that can be configured for high availability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境を配置して、高可用性のためにコンフィギュレーションできる環境で AX 2012 R3 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source>This environment includes several virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境には、数台の仮想マシンが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>These virtual machines have Windows Server—and the software that you’ll need to use AX 2012 R3—already installed on them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの仮想マシンには、Windows Server と、AX 2012 R3 を使用するために必要なソフトウェアが既にインストールされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>The following table lists details about the default high availability environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルは、既定の高可用性環境の詳細を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>When you deploy the environment, you can add additional virtual machines to the environment, or change the size of the virtual machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を配置するとき、環境に追加の仮想マシンを追加する、または仮想マシンのサイズを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source>Azure Premium Storage is required for high availability environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Premium Storage は高可用性環境が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>For more information, see <bpt id="p1">[</bpt>Deploy a high availability environment on Azure<ept id="p1">](deploy-high-availability-environment-azure.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Azure での高可用性環境の配置<ept id="p1">](deploy-high-availability-environment-azure.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>The virtual machines in this environment are covered by an Azure <bpt id="p1">[</bpt>Service Level Agreement<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境の仮想マシンは、Azure <bpt id="p1">[</bpt>サービス レベル アグリーメント<ept id="p1">](http://azure.microsoft.com/en-us/support/legal/sla/)</ept>の対象となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>Data Import/Export Framework (DIXF) components are not installed by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート/エクスポート フレームワーク (DIXF) コンポーネントは既定ではインストールされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source>If you want to use DIXF, you must use your own SQL Server installation media to install SQL Server Integration Services (SSIS) on the SQL Server machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DIXF を使用する場合は、独自の SQL Server インストール メディアを使用して、SQL Server マシンに SQL Server Integration Services (SSIS) をインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source>After you install SSIS, you can use the Dynamics AX CD (available on a connected drive within the VMs) to install the DIXF components on the AOS and then client machines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSIS をインストールした後は、Dynamics AX CD (VM 内の接続されたドライブで利用可能) を使用し、DIXF コンポーネントを AOS およびクライアント マシンにインストールできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Number of virtual machines deployed by default<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>既定で配置される仮想マシンの数<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Description<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>説明<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size and name<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズと名前<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Software installed<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソフトウェア インストール済み<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>3<bpt id="p1">&lt;strong&gt;</bpt>Note: <ept id="p1">&lt;/strong&gt;</ept>Three domain controllers are deployed in this environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 <bpt id="p1">&lt;strong&gt;</bpt>注記:<ept id="p1">&lt;/strong&gt;</ept> 3 つのドメイン コントローラがこの環境に配置されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>If one domain controller fails, you must be left with two, online domain controllers in order to meet Azure’s <bpt id="p1">&lt;a href="http://azure.microsoft.com/en-us/support/legal/sla/"&gt;</bpt>Service Level Agreement<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのドメイン コントローラーが失敗すると、Azure の<bpt id="p1">&lt;a href="http://azure.microsoft.com/en-us/support/legal/sla/"&gt;</bpt>サービス レベル同意書<ept id="p1">&lt;/a&gt;</ept>に準拠するために、2 つのオンライン ドメイン コントローラーを残しておく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source>Domain controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン コントローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="701">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D1: Basic compute tier (1 core, 3.5 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> AD-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D1: 基本的な計算層 (1 コア、3.5 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>AD-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="702">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="703">
          <source>Active Directory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="704">
          <source>Domain Name Services (DNS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン名サービス (DNS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="705">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="706">
          <source>AOS server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="707">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> AOS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>AOS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="708">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="709">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="710">
          <source>Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="711">
          <source>Microsoft Project Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Project Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="712">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="713">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="714">
          <source>Native Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネイティブ クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="715">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="716">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="717">
          <source>Application Object Server (AOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="718">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="719">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="720">
          <source>Office add-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office アドイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="721">
          <source>Remote Desktop Services integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="722">
          <source>Integration components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="723">
          <source>Web services on IIS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS 上の Web サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="724">
          <source>.NET Business Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.NET Business Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="725">
          <source>Management utilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="726">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="727">
          <source>Retail Headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="728">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="729">
          <source>Synch Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Synch Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="730">
          <source>Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Real-time Service</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="731">
          <source>Async Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Server</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="732">
          <source>RapidStart Connector</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RapidStart Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="733">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="734">
          <source>Database server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="735">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> SQL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>SQL-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="736">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="737">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="738">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="739">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="740">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メモ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="741">
          <source>A Quorum server is also deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クォーラム サーバーも配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="742">
          <source>This virtual machine is a listener for the AlwaysOn availability group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンは、AlwaysOn 可用性グループのリスナーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="743">
          <source>This virtual machine:o    Is not represented in the High Availability VM list, but it is deployed with High Availability environments.o    Is named QRM-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この仮想マシンは、o    [高可用性 VM] ボックスの一覧には表示されませんが、高可用性環境で展開されます。o    QRM -<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph> という名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="744">
          <source>This name can’t be customized.o    Is an A2 virtual machine.o    Runs a gallery image of Windows Server 2012 R2.o    Post deployment, this VM appears as a “Database Server” when adding VMs to the High Availability environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この名前はカスタマイズできません。o    A2 仮想マシンです。o    Windows Server 2012 R2 のギャラリー画像を実行します。o    配置後には、この VM は、高可用性環境に VM を追加するときに「データベース サーバー」として表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="745">
          <source>The 3rd VM referenced here is the A2 Quorum Server which is explicitly not a SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで参照されている 3 番目の VM は、明示的に SQL Server ではない A2 Quorum Server です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="746">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メモ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="747">
          <source>Reporting Services is configured to run in Native mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="748">
          <source>To use Power View, you’ll need to complete additional configuration steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電源表示を使用するには、追加の構成手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="749">
          <source>For more information, see the prerequisites listed in <bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>Create a report by using Power View to connect to a cube<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>キューブに接続するための Power View を使用したレポートの作成<ept id="p1">&lt;/a&gt;</ept>に一覧表示された前提条件を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="750">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="751">
          <source>Databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="752">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="753">
          <source>Business intelligence (BI) server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス (BI) サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="754">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> BI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>BI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="755">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="756">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="757">
          <source>Database Engine Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース エンジン サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="758">
          <source>Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="759">
          <source>Analysis Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="760">
          <source>Management Studio</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="761">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Note<ept id="p1">&lt;/strong&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>メモ<ept id="p1">&lt;/strong&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="762">
          <source>Reporting Services is configured to run in Native mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services は、ネイティブモードで実行するようにコンフィギュレーションされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="763">
          <source>To use Power View, you’ll need to complete additional configuration steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電源表示を使用するには、追加の構成手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="764">
          <source>For more information, see the prerequisites listed in <bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>Create a report by using Power View to connect to a cube<ept id="p1">&lt;/a&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">&lt;a href="https://technet.microsoft.com/en-us/library/jj933492.aspx"&gt;</bpt>キューブに接続するための Power View を使用したレポートの作成<ept id="p1">&lt;/a&gt;</ept>に一覧表示された前提条件を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="765">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="766">
          <source>Business intelligence components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス インテリジェンス コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="767">
          <source>Reporting Services extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="768">
          <source>Analysis Services configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Analysis Services の構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="769">
          <source>0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="770">
          <source>Enterprise Portal server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="771">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> EP-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>EP-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="772">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="773">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="774">
          <source>Microsoft SQL Server 2012 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2012 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="775">
          <source>Full-text Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フル テキスト検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="776">
          <source>Microsoft SharePoint Server 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="777">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="778">
          <source>Server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="779">
          <source>Web server components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web サーバー コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="780">
          <source>Enterprise Portal (EP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ ポータル (EP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="781">
          <source>Enterprise Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズ検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="782">
          <source>Help Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="783">
          <source>Management Reporter components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="784">
          <source>Management Reporter server components</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter サーバー コンポーネント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="785">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="786">
          <source>Commerce Data Exchange components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="787">
          <source>Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="788">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="789">
          <source>Retail Online Channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売オンライン チャネル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="790">
          <source>Retail Channel Database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャンネル データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="791">
          <source>Retail Channel Configuration Utility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail チャンネル コンフィギュレーション ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="792">
          <source>Retail Hardware Station</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail ハードウェア ステーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="793">
          <source>Warehouse Mobile Devices Portal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">倉庫モバイル デバイス ポータル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="794">
          <source>Connector for Microsoft Dynamics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Connector</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="795">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="796">
          <source>Client computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンピューター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="797">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> CLI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>CLI-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="798">
          <source>Windows Server 2012 R2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Server 2012 R2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="799">
          <source>Microsoft Visual Studio 2013</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2013</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="800">
          <source>Microsoft SQL Server 2014 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="801">
          <source>Developer tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="802">
          <source>Microsoft SharePoint Server 2013 Client Components SDK</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SharePoint Server 2013 クライアント コンポーネント SDK</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="803">
          <source>Microsoft Office 365 ProPlus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Office 365 ProPlus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="804">
          <source>AX 2012 R3 or AX 2012 R3 CU8 components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 R3 または AX 2012 R3 CU8 のコンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="805">
          <source>Management Reporter components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="806">
          <source>Management Reporter Report Designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter レポート デザイナー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="807">
          <source>Client components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="808">
          <source>Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="809">
          <source>Office add-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Office アドイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="810">
          <source>Remote Desktop Services integration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス統合</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="811">
          <source>Developer tools:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツール:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="812">
          <source>Debugger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="813">
          <source>Visual Studio Tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="814">
          <source>Trace Parser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Trace Parser</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="815">
          <source>Management utilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ユーティリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="816">
          <source>Retail components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売コンポーネント:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="817">
          <source>Retail POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="818">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="819">
          <source>Remote Desktop Services server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="820">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Size:<ept id="p1">&lt;/strong&gt;</ept> D3: Standard compute tier (4 cores, 14 GB memory)<bpt id="p2">&lt;strong&gt;</bpt>Default name:<ept id="p2">&lt;/strong&gt;</ept> RDS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>サイズ:<ept id="p1">&lt;/strong&gt;</ept>D3: 標準計算層 (4 コア、14 GB メモリ) <bpt id="p2">&lt;strong&gt;</bpt>既定名:<ept id="p2">&lt;/strong&gt;</ept>RDS-<ph id="ph1">&amp;lt;</ph>GUID<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="821">
          <source>Windows Server 2012 R2, including:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次を含む Windows Server2012 R2:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="822">
          <source>Internet Information Services (IIS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="823">
          <source>Remote Desktop Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップ サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="824">
          <source>Microsoft SQL Server 2012 Native Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2012 ネイティブ クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="825">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="826">
          <source><bpt id="p1">[</bpt>Deploy an AX 2012 R3 or AX 2012 R3 CU8 demo environment on Azure<ept id="p1">](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure に AX 2012 R3 または AX 2012 R3 CU8 デモ環境を配置します<ept id="p1">](deploy-ax-2012-r3-ax-2012-r3-cu8-demo-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="827">
          <source><bpt id="p1">[</bpt>Deploy a Retail essentials demo environment on Azure<ept id="p1">](deploy-retail-essentials-demo-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での Retail Essentials デモ環境の配置<ept id="p1">](deploy-retail-essentials-demo-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="828">
          <source><bpt id="p1">[</bpt>Deploy a development environment on Azure<ept id="p1">](deploy-development-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での開発環境の配置<ept id="p1">](deploy-development-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="829">
          <source><bpt id="p1">[</bpt>Deploy a test environment on Azure<ept id="p1">](deploy-test-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure でのテスト環境の配置<ept id="p1">](deploy-test-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="830">
          <source><bpt id="p1">[</bpt>Deploy a Retail essentials dev/test environment on Azure<ept id="p1">](deploy-retail-essentials-devtest-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での Retail Essentials 開発/テスト環境の配置<ept id="p1">](deploy-retail-essentials-devtest-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="831">
          <source><bpt id="p1">[</bpt>Deploy a Retail e-commerce dev/test environment on Azure<ept id="p1">](deploy-retail-ecommerce-devtest-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での Retail E-commerce 開発/テスト環境の配置<ept id="p1">](deploy-retail-ecommerce-devtest-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="832">
          <source><bpt id="p1">[</bpt>Deploy a Retail mobility dev/test environment on Azure<ept id="p1">](deploy-retail-mobility-devtest-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure での Retail Mobility 開発/テスト環境の配置<ept id="p1">](deploy-retail-mobility-devtest-environment-azure.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="833">
          <source><bpt id="p1">[</bpt>Deploy a high availability environment on Azure<ept id="p1">](deploy-high-availability-environment-azure.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure に高可用性環境を配置する<ept id="p1">](deploy-high-availability-environment-azure.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>