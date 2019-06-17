<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="data-upgrade-2012.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>data-upgrade-2012.5f2896.52d87e047634e18585d0b5eb955b7f2a64bdff94.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>52d87e047634e18585d0b5eb955b7f2a64bdff94</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\data-upgrade-2012.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Data upgrade in development environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 開発環境でのデータ アップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains the end-to-end process for upgrading from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations in a development environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、開発環境で Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にアップグレードする詳細なプロセスを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Data upgrade in development environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 開発環境でのデータ アップグレード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This is an exciting moment in the upgrade project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、アップグレード プロジェクトのエキサイティングな瞬間です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The output of this task  provides the first upgraded dataset from Microsoft Dynamics AX 2012 in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクの出力は、Microsoft Dynamics 365 for Finance and Operations で、Microsoft Dynamics AX 2012 からアップグレードされた最初のデータセットを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Before you run this process in a shared sandbox environment, we recommend that you run it in a development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスを共有サンドボックス環境で実行する前に、開発環境で実行することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>There are two main reasons for this approach:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチには主に 2 つの理由があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>It provides local data that developers can write and test their custom data upgrade scripts against.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者がカスタム データ アップグレード スクリプトを書き込んでテストできるローカル データを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>It helps reduce the overall time that is spent on iterations of the data upgrade process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、データ アップグレード プロセスの繰り返しに費やされる全体的な時間を短縮できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In a development environment, an issue can be debugged immediately, code can be adjusted, and the upgrade can be rerun within minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境では、問題を即座にデバッグし、コードを調整し、アップグレードを数分以内に再実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>However, larger sandbox environments don’t allow for this level of agility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、より規模の大きいサンドボックス環境ではこの機敏性のレベルが許可されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In those environments, a minimum of several hours will be required to debug and remediate issues, update code, deploy the updated code, and rerun the upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらの環境では、問題の修正やデバッグ、コードの更新、更新済コードの配置、およびアップグレードの再実行に少なくとも数時間を要します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>We strongly recommend that you run the <bpt id="p1">[</bpt>Upgrade analyzer<ept id="p1">](upgrade-analyzer-tool.md)</ept> and respond to the issues it identifies before running data upgrade - this will help ensure that your data upgrade is quicker and easier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのアップグレードを実行する前に、<bpt id="p1">[</bpt>アップグレード アナライザー<ept id="p1">](upgrade-analyzer-tool.md)</ept>を実行して、特定した問題に対応することを強くお勧めします。これは、データのアップグレードが迅速かつ容易になることを保証する手助けになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It's very important that you install the latest version of SQL Server Management Studio before you start this process: <bpt id="p1">[</bpt>Download SQL Server Management Studio<ept id="p1">](/sql/ssms/download-sql-server-management-studio-ssms)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。<bpt id="p1">[</bpt>SQL Server Management Studio のダウンロード<ept id="p1">](/sql/ssms/download-sql-server-management-studio-ssms)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>End-to-end data upgrade process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンド ツー エンド データのアップグレード プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Data upgrade process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アップグレード プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Back up your AX 2012 database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 データベースをバックアップします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>To back up your AX 2012 database, use the standard Microsoft SQL Server process to produce a BAK file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 データベースをバックアップするには、標準の Microsoft SQL Server プロセスを使用して BAK ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If you use the compression option when you create the backup, the file size will be smaller, and less time is required in order upload it to and download it from Microsoft Azure Storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックアップを作成するときに圧縮オプションを使用すると、ファイル サイズが小さくなり、Microsoft Azure Storage にアップロードおよびダウンロードするために必要な時間が短縮されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Upload the backup to Azure Storage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージにバックアップをアップロード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If your developer environment is hosted as a VM locally or in Azure you will need to transfer the 2012 database backup to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境がローカルまたは Azure で VM としてホストされている場合、2012 データベースのバックアップをそれに転送する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>With a local VM you may be able to transfer the file directly across the network (if you have configured the virtual network to allow that) but for an Azure hosted VM we recommend that you upload your backup to Azure Storage (using your own secure file transfer service or SFTP is also a valid option).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル VM では、ネットワーク全体でファイルを直接転送することができますが (それを許可するように仮想ネットワークを構成済みの場合)、Azure でホストされた VM の場合バックアップを Azure Storage にアップロードすることをお勧めします (自分のセキュアな転送サービスまたは SFTP の使用も有効なオプションです)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>You would need to provide your own Azure storage account for this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これに対して、独自の Azure ストレージ アカウントを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>There are free tools to help you to move files between Azure storage, from a command line you can use <bpt id="p1">[</bpt>Azcopy<ept id="p1">](/azure/storage/storage-use-azcopy)</ept>, or for a GUI experience you can use <bpt id="p2">[</bpt>Microsoft Azure storage explorer<ept id="p2">](https://storageexplorer.com/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは <bpt id="p1">[</bpt>Azcopy<ept id="p1">](/azure/storage/storage-use-azcopy)</ept> を、GUI 操作からは <bpt id="p2">[</bpt>Microsoft Azure ストレージ エクスプローラー<ept id="p2">](https://storageexplorer.com/)</ept> を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use one of these tools to first upload the backup from your on-premises environment to Azure storage and then on your download it on your development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Download and restore the backup to the development environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発環境へのバックアップのダウンロードと復元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>When you restore the backup to your Dynamics 365 for Finance and Operations development environment, don’t overwrite the existing AXDB database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations の開発環境にバックアップを復元するときは、既存の AXDB データベースを上書きしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Instead, restore the AX 2012 database next to the original databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、元のデータベースの横にある AX 2012 データベースを復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You might also consider using drive D for the data and log files, to help improve performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンスを向上させるために、データおよびログ ファイルの D ドライブの使用も考慮する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>However, there is a potential downside to using drive D. If the underlying virtual machine (VM) is deallocated in Azure and then reallocated, drive D will be wiped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、D ドライブを使用することには潜在的な問題点があります。基になる仮想マシン (VM) が Azure で割り当て解除され、次に再割り当てされると、D ドライブが消去されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In practice, this scenario rarely occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、このシナリオが発生ことはほとんどありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Therefore, you might find that the risk is acceptable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、そのリスクは容認できる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>To learn more about how to use drive D, see <bpt id="p1">[</bpt>Understanding the temporary drive on Windows Azure Virtual Machines<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドライブ D の使用方法の詳細については、[<bpt id="p1">[</bpt>Windows Azure 仮想マシンでのテンポラリー ドライブを理解する<ept id="p1">](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</ept>] を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To speed up the database restore process, you can change the SQL Server service account to <bpt id="p1">**</bpt>axlocaladmin<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの復元プロセスをスピードアップするには、SQL Server サービスアカウントを <bpt id="p1">**</bpt>axlocaladmin<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The restore process can then use instant file initialization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元プロセスでは、インスタント ファイルの初期化を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For more information, see <bpt id="p1">[</bpt>Database Instant File Initialization<ept id="p1">](/sql/relational-databases/databases/database-instant-file-initialization)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>データベース インスタント ファイルの初期化<ept id="p1">](/sql/relational-databases/databases/database-instant-file-initialization)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>After the database is restored, stop the following services:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを復元した後、次のサービスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>World wide web publishing service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">World Wide Web 公開サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Dynamics 365 for Finance and Operations Batch Management service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations バッチ管理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Management Reporter 2012 Process service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 処理サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Next, rename the original AXDB database <bpt id="p1">**</bpt>AXDB_orig<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、元の AXDB データベースを <bpt id="p1">**</bpt>AXDB_orig<ept id="p1">**</ept> に名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This database might be useful as reference later, when you develop code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースは、後でコードを開発する際に参照する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Finally, rename the newly restored AX 2012 database <bpt id="p1">**</bpt>AXDB<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、新しく復元された AX 2012 データベース <bpt id="p1">**</bpt>AXDB<ept id="p1">**</ept> の名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Run the data upgrade deployable package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ アップグレード展開可能なパッケージを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>To get the latest data upgrade deployable package for a target environment that is running the latest Finance and Operations update, download the latest binary updates from Microsoft Dynamics Lifecycle Services (LCS) Shared asset library.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">最新の Finance and Operations 更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept> にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Select the <bpt id="p1">**</bpt>Shared asset library<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>共有資産ライブラリ<ept id="p1">**</ept> タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In the <bpt id="p1">**</bpt>Shared asset<ept id="p1">**</ept> library, under <bpt id="p2">**</bpt>Select asset type<ept id="p2">**</ept>, select <bpt id="p3">**</bpt>Software deployable package<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>共有アセット<ept id="p1">**</ept> ライブラリの<bpt id="p2">**</bpt>アセット タイプの選択<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>ソフトウェア配置可能パッケージ<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In the list of deployable package files, find the data upgrade package that corresponds to your upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>For example, if you're upgrading from AX 2012, the package name starts with AX2012DataUpgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Select the package that corresponds to the release you are upgrading to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードするリリースに対応するパッケージを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>For example: AX2012DataUpgrade-July2017.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: AX2012DataUpgrade-July2017。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>For more information, see <bpt id="p1">[</bpt>Upgrade data in development, demo, or sandbox environments<ept id="p1">](upgrade-data-to-latest-update.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>開発、デモ、またはサンドボックス環境でのデータのアップグレード<ept id="p1">](upgrade-data-to-latest-update.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Troubleshooting data upgrade script errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード スクリプト エラーのトラブルシューティング データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>There are options that you let you resume the data upgrade where it last stopped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に停止した場所で、データのアップグレードを再開できるようにするオプションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>You can also record any data upgrade script errors with call stacks to a table in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、データベース内のテーブルに、コール スタック付きでデータ アップグレード スクリプト エラーを記録することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For development scenarios, you can skip failed scripts and continue to run the upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発のシナリオでは、失敗したスクリプトをスキップし、継続してアップグレードを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For more details, see the <bpt id="p1">[</bpt>main data upgrade topic<ept id="p1">](upgrade-data-to-latest-update.md#troubleshoot-upgrade-script-errors)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>主要データのアップグレード トピック<ept id="p1">](upgrade-data-to-latest-update.md#troubleshoot-upgrade-script-errors)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Recommendation for the first data upgrade run</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のデータ アップグレードを実行するための推奨事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>When you run the data upgrade against your dataset for the first time, and especially when there many customizations or many custom data upgrade scripts, you might find the <bpt id="p1">[</bpt>feature to skip failed scripts<ept id="p1">](upgrade-data-to-latest-update.md)</ept> useful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">初めてデータセットのデータのアップグレードを実行するとき、特に多くのカスタマイズまたは多くのカスタム データのアップグレード スクリプトが存在するとき、<bpt id="p1">[</bpt>失敗したスクリプトをスキップする機能<ept id="p1">](upgrade-data-to-latest-update.md)</ept> が役に立つ場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>By using this feature, you gain visibility into as many errors as possible in one run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用すると、1 回の実行で可能な限り多くのエラーを可視化できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Otherwise, only one critical issue is discovered per run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、実行あたり 1 つだけの重要な問題が検出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Be aware that, because dependencies exist between scripts, you might receive errors in related child scripts if you skip the parent script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト間には依存関係が存在するため、親スクリプトをスキップすると関連する子スクリプトにエラーが発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>These errors occur only because the parent wasn’t run correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのエラーは、親が正しく実行されなかったためにのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>They will be resolved when the issue in the parent script is resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">親スクリプト内の問題が解決されると、解決されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>