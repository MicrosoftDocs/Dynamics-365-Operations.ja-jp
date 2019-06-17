<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="vso-machine-renaming.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>vso-machine-renaming.1f7b39.9d424ad3e911fcd7b98e1a14c7c7226b6710774a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>9d424ad3e911fcd7b98e1a14c7c7226b6710774a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\vso-machine-renaming.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Rename a local development (VHD) environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル開発 (VHD) 環境の名前変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to rename a local development (VHD) environment so that you can access a Microsoft Azure DevOps project across multiple machines and successfully install One Version service updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、複数のコンピューター間で Microsoft Azure DevOps プロジェクトにアクセスし、1 つのバージョンのサービスの更新プログラムを正常にインストールできるように、ローカル開発 (VHD) 環境の名前を変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Rename a local development (VHD) environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル開発 (VHD) 環境の名前変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>A local development (VHD) environment must be renamed for the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル開発 (VHD) 環境では、次のシナリオで名前を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source><bpt id="p1">**</bpt>Accessing a single Microsoft Azure DevOps project across multiple machines:<ept id="p1">**</ept> Azure DevOps is required for version control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>複数のコンピューター間で 1 つの Microsoft Azure DevOps プロジェクトにアクセスする:<ept id="p1">**</ept> Azure DevOps がバージョン管理のために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It was previously known as Visual Studio Online (VSO) or Visual Studio Team Services (VSTS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は Visual Studio Online (VSO) または Visual Studio Team Services (VSTS) と呼ばれていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In development topologies, multiple virtual machines (VMs) can't access the same Azure DevOps project if they have the same machine name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発トポロジでは、複数の仮想マシン (VM) が同じコンピューター名である場合、同じ Azure DevOps プロジェクトにアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Azure DevOps uses the machine name for identification.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps はマシン名を ID として使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you're developing on local VMs that were downloaded from Microsoft Dynamics Lifecycle Services (LCS), you might encounter issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) からダウンロードされたローカル VM で開発する場合は、問題が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Installing One Version service updates:<ept id="p1">**</ept> One Version service updates, such as 8.1.x, must be installed in VHD environments by using a runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 つのバージョンのサービスの更新プログラムをインストールする:<ept id="p1">**</ept> 8.1.x などの 1 つのバージョンのサービス更新プログラムを、runbook を使用して VHD 環境にインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To help guarantee that the runbook is completed successfully, the VHD environments must be renamed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Runbook が正常に完了するようにするため、VHD 環境の名前を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Additional steps that are described in this topic must also be completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックに記載されているその他の手順を実行する必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Rename the machine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターの名前を変更する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Rename and restart the machine before you start development or connect to Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発を開始するか Azure DevOps に接続する前にマシンの名前を変更してリブートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Make sure that the new name is unique among all the machines that are used with the Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい名前が Azure DevOps プロジェクトで使用されるすべてのコンピューター間で一意であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Update the server name in SQL Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server でサーバー名を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Update the server name in Microsoft SQL Server 2016 by running the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコマンドを実行して、Microsoft SQL Server 2016 でサーバー名を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In these commands, be sure to replace <bpt id="p1">**</bpt>old<ph id="ph1">\_</ph>name<ept id="p1">**</ept> with the old name of the server and <bpt id="p2">**</bpt>new<ph id="ph2">\_</ph>name<ept id="p2">**</ept> with the new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのコマンドでは、必ず <bpt id="p1">**</bpt>old<ph id="ph1">\_</ph>name<ept id="p1">**</ept> をサーバーの古い名前に、<bpt id="p2">**</bpt>new<ph id="ph2">\_</ph>name<ept id="p2">**</ept> を新しい名前に置き換えてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>By default, the old name is <bpt id="p1">**</bpt>MININT-F36S5EH<ept id="p1">**</ept>, but you can run <bpt id="p2">**</bpt>select @@servername<ept id="p2">**</ept> to get the old name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、古い名前は <bpt id="p1">**</bpt>MININT-F36S5EH<ept id="p1">**</ept> ですが、<bpt id="p2">**</bpt>select @@servername<ept id="p2">**</ept> を実行して古い名前を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Additionally, be sure to restart the SQL Server service after the commands have finished running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、コマンドの実行が完了した後、必ず SQL Server サービスを再起動してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Update SQL Server Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Reporting Services の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Update the SQL Server Reporting Service (SSRS) database by using the Reporting Services Configuration Manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Reporting Services 構成マネージャーを使用して、SQL Server Reporting Service (SSRS) データベースを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select <bpt id="p1">**</bpt>Database<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Change Database<ept id="p2">**</ept>, and use the new server name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データベース<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>データベースの変更<ept id="p2">**</ept> を選択して新しいサーバー名を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Make sure that you use Reporting Services Configuration Manager for SQL Server 2016.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、SQL Server 2016 用の Reporting Services 構成マネージャーを使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Additional steps to install One Version service updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのバージョンのサービスの更新プログラムをインストールする追加の手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The following additional steps are required in order to install One Version service updates in a VHD environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VHD 環境で 1 つのバージョンのサービスの更新プログラムをインストールするには、次の追加手順が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Update the Azure Storage Emulator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Storage エミュレーター を更新する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Update the Azure Storage Emulator, and make sure that it's running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Storage エミュレーターを更新し、それが実行されているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>From the <bpt id="p1">**</bpt>Start<ept id="p1">**</ept> menu, open <bpt id="p2">**</bpt>Microsoft Azure Storage Emulator - v4.0<ept id="p2">**</ept>, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スタート<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>Microsoft Azure Storage エミュレーター - v4.0<ept id="p2">**</ept> を開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This command starts the emulator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、エミュレーターを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>This command verifies that the emulator is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドは、エミュレーターが実行されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Try the <bpt id="p1">**</bpt>init<ept id="p1">**</ept> option with the <bpt id="p2">**</bpt>-server<ept id="p2">**</ept> switch or the <bpt id="p3">**</bpt>-forcecreate<ept id="p3">**</ept> switch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>-server<ept id="p2">**</ept> スイッチまたは <bpt id="p3">**</bpt>-forcecreate<ept id="p3">**</ept> スイッチを使用して <bpt id="p1">**</bpt>init<ept id="p1">**</ept>オプションを試してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Be sure to replace <bpt id="p1">**</bpt>new<ph id="ph1">\_</ph>name<ept id="p1">**</ept> with the new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、<bpt id="p1">**</bpt>new<ph id="ph1">\_</ph>name<ept id="p1">**</ept> を新しい名前に置き換えてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If the <bpt id="p1">**</bpt>init<ept id="p1">**</ept> command fails, delete the storage emulator database by using SQL Server Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>init<ept id="p1">**</ept> コマンドが失敗した場合、SQL Server Management Studio を使用してストレージ エミュレーター データベースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Then try the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、次のコマンドを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>When you run this command, you might receive the following error message: "Error: Cannot create database."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを実行すると、次のエラー メッセージが表示される場合があります: "エラー: データベースを作成できません。"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>However, the emulator will usually still start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、通常、エミュレーターは引き続き起動されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>You just need the emulator to start.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エミュレーターを起動するだけでかまいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Update financial reporting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務諸表の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Update the server name for financial reporting by using a script that is included in the One Version service update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのバージョンのサービスの更新プログラムに含まれるスクリプトを使用して、財務報告のためのサーバー名を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To get the command, you must download and expand the One Version service update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドを取得するには、1 つのバージョンのサービスの更新をダウンロードして展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Open a Microsoft Windows PowerShell command window as an admin, and run the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として Microsoft Windows PowerShell コマンド ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This command contains the default passwords that might have to be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドには、更新する必要がある既定のパスワードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Be sure to replace <bpt id="p1">**</bpt>new<ph id="ph1">\_</ph>name<ept id="p1">**</ept> with the new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必ず、<bpt id="p1">**</bpt>new<ph id="ph1">\_</ph>name<ept id="p1">**</ept> を新しい名前に置き換えてください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>