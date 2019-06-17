<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="install-network-printer-onprem.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>install-network-printer-onprem.fc793b.a65db6abd3c11fa168fc788fb4a3bf1d30f13bcc.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a65db6abd3c11fa168fc788fb4a3bf1d30f13bcc</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\install-network-printer-onprem.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Install network printer devices in on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境でのネットワーク プリンター デバイスのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to connect an on-premises deployment of Microsoft Dynamics 365 for Finance and Operations, to existing network printer devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス展開を既存のネットワーク プリンタ デバイスに接続する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Install network printer devices in on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境でのネットワーク プリンター デバイスのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to connect an on-premises deployment of Microsoft Dynamics 365 for Finance and Operations to existing network printer devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス展開を既存のネットワーク プリンタ デバイスに接続する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Network printing in the on-premises application is supported by the <bpt id="p1">[</bpt>Print and Document Services<ept id="p1">](https://technet.microsoft.com/en-us/library/hh831468(v=ws.11).aspx)</ept> feature in Microsoft Windows Server 2016.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス アプリケーションでのネットワーク印刷は、Microsoft Windows Server 2016 の「<bpt id="p1">[</bpt>印刷およびドキュメント サービス<ept id="p1">](https://technet.microsoft.com/en-us/library/hh831468(v=ws.11).aspx)</ept>」機能でサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This feature lets you centralize tasks that are related to printer management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用すると、プリンター管理に関連するタスクを集中管理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To install and configure Print and Document Services, you must have administrative access to the server that hosts the primary instance of Application Object Server (AOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷およびドキュメント サービスをインストールして構成するには、Application Object Server (AOS) のプライマリー インスタンスをホストするサーバーへの管理アクセス権が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Two roles are associated with the configuration of network printing services:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワーク印刷サービスの構成には、次の 2 つの役割があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Service Administrator<ept id="p1">**</ept> – The person who has this role is responsible for installing and configuring components of the platform infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サービス管理者<ept id="p1">**</ept> – この役割を持つ担当者は、インストールやプラットフォーム インフラストラクチャのコンポーネントのコンフィギュレーションを担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Traditionally, this role is an Active Directory account that has elevated domain privileges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従来、この役割は昇格したドメイン権限を持った Active Directory アカウントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>It has enough privileges to install components of Microsoft Windows Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows Server のコンポーネントのインストールに必要な権限があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Organization Administrator<ept id="p1">**</ept> – The person who has this role manages application security privileges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織の管理者<ept id="p1">**</ept> – このロールを持つユーザーはアプリケーション セキュリティ権限を管理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This Active Directory account is assigned to the <bpt id="p1">**</bpt>System Administrator<ept id="p1">**</ept> role in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この Active Directory アカウントは、Finance and Operations の <bpt id="p1">**</bpt>システム管理者<ept id="p1">**</ept> ロールに割り当てられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Before the organization administrator can begin to add network printers, the service administrator must install and configure Print and Document Services on the server that hosts the primary AOS instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織の管理者がネットワーク プリンターの追加を開始する前に、サービス管理者はプライマリ AOS インスタンスをホストするサーバーに印刷およびドキュメント サービスをインストールして構成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The organization administrator can then begin to use built-in tools to configure network printer devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織の管理者は、組み込みツールを使用してネットワーク プリンター デバイスの設定を開始できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Install and configure Print and Document Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷およびドキュメント サービスのインストールと構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The environment administrator uses the information in this section to enable network printing services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境管理者は、このセクションの情報を使用してネットワーク印刷サービスを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Install Print and Document Services by following the instructions in <bpt id="p1">[</bpt>Install Print and Document Services<ept id="p1">](https://technet.microsoft.com/en-us/library/jj134159(v=ws.11).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>印刷およびドキュメント サービスのインストール<ept id="p1">](https://technet.microsoft.com/en-us/library/jj134159(v=ws.11).aspx)</ept>の手順に従って印刷およびドキュメント サービスをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Configure Print and Document Services by following the instructions in <bpt id="p1">[</bpt>Configure Print and Document Services<ept id="p1">](https://technet.microsoft.com/en-us/library/jj134163(v=ws.11).aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順に従って印刷およびドキュメント サービスをコンフィギュレーションします <bpt id="p1">[</bpt>印刷およびドキュメント サービスのコンフィギュレーション<ept id="p1">](https://technet.microsoft.com/en-us/library/jj134163(v=ws.11).aspx)</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Follow these steps for each server that is used to host the AXService application:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXService アプリケーションをホストするために使用する各サーバーに対して、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>On the local server, start the <bpt id="p1">**</bpt>Local Users and Groups<ept id="p1">**</ept> manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル サーバーで、<bpt id="p1">**</bpt>ローカル ユーザーとグループ<ept id="p1">**</ept>マネージャーを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Select the <bpt id="p1">**</bpt>Groups<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>グループ<ept id="p1">**</ept> ノードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Right-click <bpt id="p1">**</bpt>Print Operators<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Add to Group<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>出力演算子<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>グループへの追加<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Add the network Active Directory account that is used to run the AXService application to the group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グループに AXService アプリケーションを実行するために使用されるネットワーク Active Directory アカウントを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Install network printers by using the AXService user account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXService ユーザー アカウントを使用してネットワーク プリンターをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This step helps guarantee that the printer driver is available to the AXService user account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップにより、プリンター ドライバーが AXService ユーザー アカウントで使用できることが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Print a test page on the installed printers to make sure that all the connections are correctly configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての接続が正しく構成されていることを確認するため、インストールされているプリンターのテスト ページを印刷します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Restart the AXService application to help guarantee that the user's profile is correctly loaded so that it can look up the printer driver.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーのプロファイルが正しく読み込まれることを保証し、プリンターを参照できるようにするために、AXService アプリケーションを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Manage network printers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワーク プリンターの管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The system administrator of Finance and Operations uses the information in this section to define network printers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のシステム管理者は、このセクションの情報を使用してネットワーク プリンタを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Go to <bpt id="p1">**</bpt>Organization administration<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>Network printers<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>組織管理<ept id="p1">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">\&gt;</ph> <bpt id="p3">**</bpt>ネットワーク プリンター<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>On the <bpt id="p1">**</bpt>Network printers<ept id="p1">**</ept> page, add new printers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ネットワーク プリンター<ept id="p1">**</ept>ページで、新しいプリンターを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>For each printer, specify a name, description, path, and status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各プリンターで、名前、説明、パス、およびステータスを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Make sure that the printer path matches the network path of the installed printer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリンター パスがインストールされているプリンターのネットワーク パスと一致していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Items that are marked <bpt id="p1">**</bpt>Active<ept id="p1">**</ept> immediately become available to application users, so that they can begin to print document-style reports on network printer devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept>とマークされている項目は、すぐにアプリケーションのユーザーによって利用できるようになるので、ネットワーク プリンター デバイスで文書スタイル レポートの印刷を開始できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>