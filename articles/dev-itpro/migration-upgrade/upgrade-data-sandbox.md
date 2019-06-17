<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="upgrade-data-sandbox.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>upgrade-data-sandbox.a730b6.bfa2b12898b05691ca16e9d72f05932f33691c44.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bfa2b12898b05691ca16e9d72f05932f33691c44</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\upgrade-data-sandbox.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Data upgrade in sandbox environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to perform a data upgrade from Dynamics AX 2012 to Dynamics 365 for Finance and Operations in a sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サンドボックス環境で Dynamics AX 2012 から Dynamics 365 for Finance and Operations にデータ アップグレードを実行する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Data upgrade in sandbox environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The output of this task is an upgraded database that you can use in a sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクの出力は、サンドボックス環境で使用できるデータベースのアップグレードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this article, we use the term <bpt id="p1">*</bpt>sandbox<ept id="p1">*</ept> to refer to a Standard or Premier Acceptance Testing (Tier 2/3) or higher environment connected to a SQL Azure database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、<bpt id="p1">*</bpt>サンドボックス<ept id="p1">*</ept> という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2/3)、またはより高度な環境を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>On this environment business users and functional team members can validate application functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この環境では、ビジネス ユーザーと機能チームのメンバーがアプリケーション機能を検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This functionality includes customizations and the data that was brought forward from Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 から継承されたデータが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>We strongly recommend that you run the data upgrade process in a development environment before you run it in a shared sandbox environment, because this approach will help reduce the overall time that is required for a successful data upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、データを正常にアップグレードするのに必要な全体的な時間の短縮に役立つため、共有サンドボックス環境で実行する前に開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For more information, see <bpt id="p1">[</bpt>Data upgrade in a development environment<ept id="p1">](prepare-data-upgrade.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>開発環境でのデータ アップグレード<ept id="p1">](prepare-data-upgrade.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>It's very important that you install the latest version of SQL Server Management Studio before you start this process: <bpt id="p1">[</bpt>Download SQL Server Management Studio<ept id="p1">](/sql/ssms/download-sql-server-management-studio-ssms)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。<bpt id="p1">[</bpt>SQL Server Management Studio のダウンロード<ept id="p1">](/sql/ssms/download-sql-server-management-studio-ssms)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Overview of the sandbox data upgrade process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス データ アップグレード プロセスの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Before you start to upgrade data in a sandbox environment, you will have already upgraded data in a development environment, as explained in <bpt id="p1">[</bpt>Data upgrade in a development environment<ept id="p1">](prepare-data-upgrade.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境でのデータのアップグレードを開始する前に、<bpt id="p1">[</bpt>開発環境でのデータ アップグレード<ept id="p1">](prepare-data-upgrade.md)</ept> で説明しているように、開発環境で既にデータがアップグレードされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The two processes are very similar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つのプロセスはよく似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The main difference is that a sandbox environment uses Microsoft Azure SQL Database for data storage, whereas a development environment uses Microsoft SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主な違いは、サンドボックス環境では Microsoft Azure SQL データベースをデータ保管に使用し、開発環境では Microsoft SQL Server を使用する点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This technical difference in the database layer requires that you  modify the data upgrade procedure slightly in a sandbox environment, because a backup from the AX 2012 database instance can't just be restored to SQL Database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベース レイヤーの技術的な違いにより、AX 2012 データベース インスタンスからのバックアップを SQL データベースに復元できないため、サンドボックス環境でデータのアップグレード手順を少し変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Sandbox data upgrade process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス データのアップグレード プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Here are the high-level steps in the upgrade process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード プロセスの高レベルの手順を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Turn off the AX 2012 AOS instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 AOS インスタンスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Create a copy of the AX 2012 database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 データベースのコピーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>We strongly recommend that you use a copy, because you must delete some objects in the copy that will be exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするコピーの一部のオブジェクトを削除する必要があるため、コピーを使用することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Export the copied database to a bacpac file by using a free SQL Server tool that is named SQLPackage.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLPackage.exe という名前の無料の SQL Server ツールを使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This tool provides a special type of database backup that can be imported into SQL Database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Upload the bacpac file to Azure storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージに bacpac ファイルをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Download the bacpac file to the Application Object Server (AOS) machine in the sandbox environment, and then import it by using SQLPackage.exe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境で bacpac ファイルを Application Object Server (AOS) コンピューターにダウンロードし、SQLPackage.exe を使用してインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You must then run a script against the imported database to reset the SQL database users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL データベースのユーザーをリセットするには、インポートされたデータベースに対してスクリプトを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Run the appropriate data upgrade package against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して適切なデータ アップグレード パッケージを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Turn off the AX 2012 AOS instances</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 AOS インスタンスをオフにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This task involves the AX 2012 system administrator and the server administrators.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクには、AX 2012 のシステム管理者とサーバー管理者が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Before you turn off AOS instances, you must stop all batch jobs that are running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS インスタンスをオフにする前に、実行しているすべてのバッチ ジョブを停止する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A long-running batch job that has already started to run will prevent the system from stopping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に稼働し始めている実行時間の長いバッチ ジョブでは、システムが停止しないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Plan ahead, so that you can stop your AOS instances when needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合は AOS インスタンスを停止できるように、事前に計画してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You might have to schedule batches so that they're completed some time before you turn off AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 をオフにする前にバッチが完了するよう、バッチをスケジュールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>You might have other systems that are integrated with the AX 2012 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 環境と統合されている他のシステムをお持ちかもしれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>You must also factor these systems into your plan to turn off AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 をオフにするための計画には、これらのシステムも考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, you might have to turn off the integrated systems some time before you turn off AX 2012 itself, so that any remaining in-flight transactions can be completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、AX 2012 自体をオフにする前に、統合システムをしばらくオフにして、残りのインフライト トランザクションを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The requirements for integrated systems vary widely from business to business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合システムの要件は、企業間で広く異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Therefore, your team of experts must plan for this scenario independently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、専門家チームはこのシナリオを個別に計画する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Create a copy of the AX 2012 database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 データベースのコピーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You must create a copy of the AX 2012 database that you're upgrading, because you must delete some objects from the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースから一部のオブジェクトを削除する必要があるため、アップグレードを実行している AX 2012 データベースのコピーを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>These objects include any Microsoft Windows authentication users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのオブジェクトには、Microsoft Windows 認証ユーザーが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>These changes make the modified database unusable for AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更により、変更されたデータベースは AX 2012 で使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>During this step, you will create a copy of the database and delete these objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、データベースのコピーを作成してこれらのオブジェクトを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This step must be done by the database administrator (DBA) or a person who has similar knowledge and experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順は、データベース管理者 (DBA) または同様の知識と経験を持っている人物が行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>To create a database copy, make a backup of the original database, and restore it under a new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのコピーを作成するには、元のデータベースのバックアップを作成し、新しい名前で復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Make sure that enough space is available for both databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方のデータベースに十分なスペースがあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You can create the copy on a different server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のサーバーでコピーを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The version of the SQL Server instance that runs the database isn't important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを実行する SQL Server インスタンスのバージョンは重要ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Here is an example of the code that creates a database copy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのコピーを作成するコードの例を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>You must modify this example to reflect your specific database names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のデータベース名を反映するよう、この例を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Run the T-SQL script to prepare the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの準備のため T-SQL スクリプトを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This script prepares the database by removing users, removing procedures related to the AX 2012 RTM model store, cleaning up schemas, dropping views, and dropping references to tempDB.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、ユーザーを削除、AX 2012 RTM モデル ストアに関連するステップを削除、スキーマをクリーンアップ、ビューを削除、および tempDB への参照を削除によってデータベースを準備します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>After the copy is created, run the following Transact-SQL (T-SQL) script against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーが作成されたら、次の Transact-SQL (T-SQL) スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Export the copied database to a bacpac file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コピーしたデータベースを bacpac ファイルにエクスポートする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Export the copied database to a bacpac file by using the SQLPackage.exe tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLPackage.exe ツールを使用して、コピーしたデータベースを bacpac ファイルにエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>This step should be done by the DBA or a team member who has equivalent knowledge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順は、DBA または同等の知識を持っているチーム メンバーが行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's very important that you install the latest version of SQL Server Management Studio before you start this step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順を開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Although SQLPackage is present in earlier versions of Management Studio, it won't work correctly for this step unless you first install the latest version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLPackage は以前のバージョンの Management Studio に存在しますが、まず最新バージョンをインストールしない限り、このステップでは正しく動作しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This step is important, because the export will have to be done again during the downtime before go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順は重要です。稼動前のダウンタイム中にエクスポートを再度実行する必要があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Here are some tips:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのヒントを以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The bacpac process is very I/O and CPU intensive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac プロセスでは、I/O および CPU に非常に負荷がかかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Therefore, run the export on a high-powered machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、高性能コンピューターでエクスポートを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>SQLPackage should be run locally on the machine that hosts the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLPackage は、データベースをホストするコンピューターにローカルで実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Don't run SQLPackage on a local laptop that you connect to the database machine, because this process is also network intensive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この処理もネットワーク集中型であるため、データベース コンピューターに接続するローカルのラップトップで SQLPackage を実行しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Next, open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>ssn<ept id="p1">**</ept> (source server name) – The name of the SQL Server to export from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ssn<ept id="p1">**</ept> (ソース サーバー名) – エクスポートする SQL Server の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For our process, this parameter should always be set to <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスでは、このパラメータは常に <bpt id="p1">**</bpt>localhost<ept id="p1">**</ept> に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>sdn<ept id="p1">**</ept> (source database name) – The name of the database to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sdn<ept id="p1">**</ept> (ソース データベース名) – エクスポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>tf<ept id="p1">**</ept> (target file) – The path and name of the file to export to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tf<ept id="p1">**</ept> (ターゲット ファイル) – エクスポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The folder should already exist, but the file will be created by the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォルダーが既に存在するはずですが、ファイルはプロセスによって作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">**</bpt>/p:CommandTimeout<ept id="p1">**</ept> – The per-query timeout value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>/p:CommandTimeout<ept id="p1">**</ept> – クエリあたりのタイムアウト値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>This parameter enables larger tables to be exported without hitting a timeout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Upload the bacpac file to Azure storage or the LCS Asset Library</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージまたは LCS アセット ライブラリに bacpac ファイルをアップロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The bacpac file you have created will need to be copied to the AOS machine in your Azure hosted sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成した bacpac ファイルは、Azure でホストされたサンドボックス環境の AOS マシンにコピーする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>There are several reasons for this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを引当するためのいくつかの理由があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The Azure SQL Database instance used by your Tier 2 (or higher) sandbox environment has firewall rules preventing access from outside of the environment itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レベル 2 (またはそれ以上) サンドボックス環境により使用される Azure SQL データベース インスタンスには、環境自体の外からのアクセスを防ぐファイアウォール ルールがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Performance of bacpac import is multiple times faster when importing from a machine within the same Azure datacenter as the Azure SQL database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bacpac インポートのパフォーマンスは、Azure SQL データベース インスタンスとし同じ Azure データセンター コンピューターからインポートした場合、何倍も向上します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You can choose how you would like to move the bacpac file to the AOS machine - you may have your own SFTP or other secure file transfer service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac ファイルを AOS マシンに移動する方法を選択することができます。自分の SFTP または他のセキュアな転送サービスがある可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>We recommend to use our Azure storage, which would require that you acquire your own Azure storage account on your own Azure subscription (this is not provided within the Dynamics subscription itself).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージを使用することをお勧めします。Azure ストレージを使用するには、ユーザー自身のサブスクリプション (Dynamics サブスクリプション自体に含まれていません)で独自の Azure ストレージ アカウントを取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>There are free tools to help you to move files between Azure storage, from a command line you can use <bpt id="p1">[</bpt>Azcopy<ept id="p1">](/azure/storage/storage-use-azcopy)</ept>, or for a GUI experience you can use <bpt id="p2">[</bpt>Microsoft Azure storage explorer<ept id="p2">](https://storageexplorer.com/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは <bpt id="p1">[</bpt>Azcopy<ept id="p1">](/azure/storage/storage-use-azcopy)</ept> を、GUI 操作からは <bpt id="p2">[</bpt>Microsoft Azure ストレージ エクスプローラー<ept id="p2">](https://storageexplorer.com/)</ept> を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Use one of these tools to first upload the backup from your on-premises environment to Azure storage and then on your download it on your development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Another (free) option is to use the LCS asset library, however, the upload and download will take longer than Azure storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう 1 つの (無料) オプションは、LCS 資産ライブラリを使用することですが、アップロードやダウンロードは Azure ストレージよりも時間がかかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>To use this option:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションを使用するには、次のようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Log into your project in LCS and go to your Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクトにログインし、アセット ライブラリに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Select the Database backup tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース バックアップ タブを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Upload the bacpac file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac ファイルをアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You can later download the bacpac onto the sandbox AOS VM by logging into LCS on that VM and downloading it from the LCS Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その VM から LCS にログインして LCS アセット ライブラリからダウンロードすることにより、後から bacpac をサンドボックス AOS VM にダウンロードすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Import the bacpac file into SQL Database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac ファイルを SQL Database にインポートする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>During this step, you will import the exported bacpac file to the SQL Database instance that your sandbox environment uses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順では、エクスポートした bacpac ファイルを、サンドボックス環境で使用する SQL データベース インスタンスにインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>You must first install the latest version of Management Studio on your sandbox AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まず、サンドボックス AOS コンピューターに Management Studio の最新バージョンをインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You will then import the file by using the SQLPackage.exe tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後 SQLPackage.exe ツールを使用してファイルをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>You will perform these tasks directly on the AOS machine in your sandbox environment, because there are firewall rules that restrict access to the SQL Database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL データベース インスタンスへのアクセスを制限するファイアウォール規則があるため、サンドボックス環境の AOS コンピューターでこれらのタスクを直接実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>However, by using the AOS machine, you can gain access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、AOS コンピューターを使用すると、アクセス許可を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>As for the export step, you must have the latest version of Management Studio before you start the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートの手順に関しては、インポートを開始する前に、Management Studio の最新バージョンが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>This step won't work if you have an older version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンを使用している場合、この手順は機能しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>For performance reasons, we recommend that you put the bacpac file on drive D on the AOS machine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス上の理由から、bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>On Azure virtual machines (VMs), drive D is a physical disk that typically has higher performance than other available disks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 仮想マシン (VM) では、ドライブ D は通常、他の利用可能なディスクよりも高いパフォーマンスを持つ物理ディスクです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>tsn<ept id="p1">**</ept> (target server name) – The name of the SQL Azure server to import to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsn<ept id="p1">**</ept> (ターゲット サーバー名) – インポートする SQL Azure サーバーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The name can be found in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前は LCS で確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Suffix it with <bpt id="p1">**</bpt>.database.windows.net<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">末尾に <bpt id="p1">**</bpt>.database.windows.net<ept id="p1">**</ept> を付け加えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>tdn<ept id="p1">**</ept> (target database name) – The name of the database to import to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tdn<ept id="p1">**</ept> (ターゲット データベース名) – インポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The database should not already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースが既に存在していない必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The import process will create it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート処理が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>sf<ept id="p1">**</ept> (source file) – The path and name of the file to import from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sf<ept id="p1">**</ept> (ソース ファイル) – インポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>tp<ept id="p1">**</ept> (target password) – The SQL password for the target SQL Database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tp<ept id="p1">**</ept> (ターゲット パスワード) – ターゲット SQL データベース インスタンスの SQL パスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>tu<ept id="p1">**</ept> (target user) – The SQL user name for the target SQL Database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tu<ept id="p1">**</ept> (ターゲット ユーザー) – ターゲット SQL データベース インスタンスの SQL ユーザー名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>We recommend that you use <bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept> を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>You can retrieve the password for this user from your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">**</bpt>/p:CommandTimeout<ept id="p1">**</ept> – The per-query timeout value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>/p:CommandTimeout<ept id="p1">**</ept> – クエリあたりのタイムアウト値。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>This parameter enables larger tables to be exported without hitting a timeout.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパラメータによって、タイムアウトを起こさずに大きなテーブルをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">**</bpt>/p:DatabaseServiceObjective<ept id="p1">**</ept> – Specifies the performance level of the database such as S1, P2 or P4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>/p:DatabaseServiceObjective<ept id="p1">**</ept> - S1、P2、P4 など、データベースのパフォーマンス レベルを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this envrironment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>You can check the value for the existing database by using Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio を使用して、既存のデータベースの値を確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Right-click the database, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>After you run the commands, you may see the following warning.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドを実行すると、次の警告が表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>You can safely ignore it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは無視してかまいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Sandbox error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Run a T-SQL script to update the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新のため T-SQL スクリプトを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Run the following script against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して、次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The script performs the following actions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトでは次のアクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Recreates database users</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ユーザーを再作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sets the correct performance parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な実績パラメーターを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Enables the SQL Query Store feature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Query Store 機能の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Run the data upgrade deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アップグレード展開可能なパッケージを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>To get the latest data upgrade deployable package for a target environment that is running the latest Finance and Operations update, download the latest binary updates from Microsoft Dynamics Lifecycle Services (LCS) Shared asset library.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">最新の Finance and Operations 更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept></source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept>にサインインします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Select the <bpt id="p1">**</bpt>Shared asset library<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>共有資産ライブラリ<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In the <bpt id="p1">**</bpt>Shared asset<ept id="p1">**</ept> library, under <bpt id="p2">**</bpt>Select asset type<ept id="p2">**</ept>, select <bpt id="p3">**</bpt>Software deployable package<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>共有アセット<ept id="p1">**</ept> ライブラリの<bpt id="p2">**</bpt>アセット タイプの選択<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>ソフトウェア配置可能パッケージ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In the list of deployable package files, find the data upgrade package that corresponds to your upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>For example, if you're upgrading from AX 2012, the package name starts with AX2012DataUpgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Select the package that corresponds to the release you are upgrading to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードするリリースに対応するパッケージを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>For example: AX2012DataUpgrade-July2017.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: AX2012DataUpgrade-July2017。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>For more information, see <bpt id="p1">[</bpt>Upgrade data in development, demo, or sandbox environments<ept id="p1">](upgrade-data-to-latest-update.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>開発、デモ、またはサンドボックス環境でのデータのアップグレード<ept id="p1">](upgrade-data-to-latest-update.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Upgrade a copy of the database in a development environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのコピーを開発環境でアップグレードする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>It is highly recommended to have upgraded the same database in a development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境で同じデータベースをアップグレードすることを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>If you have a copy of the database available for development environments, it will be much easier to investigate bugs that are found in the upgraded sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境で利用できるデータベースのコピーを使用する場合は、アップグレードされたサンドボックス環境で検出されるバグを調査する方がはるかに簡単です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>