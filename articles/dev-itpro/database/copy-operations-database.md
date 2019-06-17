<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="copy-operations-database.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>copy-operations-database.d0a416.62e0d3fcea6c1de70c6d2a328c5395befa891f16.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>62e0d3fcea6c1de70c6d2a328c5395befa891f16</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\copy-operations-database.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Export copies of Finance and Operations databases to restore later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で復元する Finance and Operations のデータベースのコピーをエクスポートする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database to a file, and then reimport that file into the same instance or another instance of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースをファイルにエクスポートしてから、そのファイルをアプリケーションの同じインスタンスかまたは別のインスタンスに再インポートする方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Export copies of Finance and Operations databases to restore later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で復元する Finance and Operations のデータベースのコピーをエクスポートする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database to a file, and then reimport that file into the same instance or another instance of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースをファイルにエクスポートしてから、そのファイルをアプリケーションの同じインスタンスかまたは別のインスタンスに再インポートする方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This procedure can be used only in non-production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは、非実稼働環境でのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic applies to Microsoft Azure SQL databases that are connected to sandbox user acceptance testing (UAT) environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、サンド ボックスのユーザー受け入れテスト (UAT) 環境に接続されている Microsoft Azure SQL データベースに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>There are several situations where you might want to keep a copy of a Finance and Operations database process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベース プロセスのコピーを保持する場合がいくつかあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You want to make strategic backups that you can restore to later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で復元できる戦略的なバックアップを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, before or after a major code update, you might want copies that you can use for reference later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、主要コード更新の前または後に、後に参照に使用できるようコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You want to back up a database before destructive testing and then restore it after the testing is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">破壊試験の前にデータベースをバックアップし、テストの完了後にデータベースを復元する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When you upgrade to a new major release of Finance and Operations, you can use this process to export your old test database and bring it forward to the new version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の新しいメジャー リリースへのアップグレードのとき、このプロセスを使用して、古いテスト データベースをエクスポートし、新しいバージョンに持ち出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Be aware that Microsoft also provides a standard feature that lets you restore an Azure SQL database environment to a specific point in time within the last 35 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は Azure SQL データベース環境を過去 35 日間以内の特定の時点に復元できる標準機能も提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This restore is done via a service request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この復元はサービス要求を介して行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>For more information, see <bpt id="p1">[</bpt>Request a point-in-time database restore on a non-production environment<ept id="p1">](request-point-in-time-restore.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>非実稼働環境でのポイントインタイム データベース復元の要求<ept id="p1">](request-point-in-time-restore.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This process used to require Remote Desktop access on your Tier-2 or higher environments but no longer does.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスでは、レベル 2 以上の環境でリモート デスクトップへのアクセスを必要としていましたが、必要なくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>These operations can be performed using the Self-service actions in Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの操作を実行するには、Lifecycle Services でセルフ サービス アクションを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Self-service database export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのセルフ サービス エクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Import the Finance and Operations database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Stop services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスの停止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Use Remote Desktop to connect to all the computers in the environment, and stop the following Windows services by using services.msc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These services will have open connections to the Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>World wide web publishing service (on all AOS computers)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Management Reporter 2012 Process Service (on BI computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Import the .bacpac file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.bacpac ファイルのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Copy the .bacpac file that was generated during the export step to the AOS computer in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート ステップ中に生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Here is an explanation of the parameters:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメータの説明を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>tsn (target server name)<ept id="p1">**</ept> – The name of the Azure SQL Database server to import into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsn(ターゲット サーバー名)<ept id="p1">**</ept> – インポートする Azure SQL データベース サーバーの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You can find the name in LCS on the environment page under Database Accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前はデータベース アカウントの環境ページの LCS で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Add the suffix <bpt id="p1">**</bpt>database.windows.net<ept id="p1">**</ept> to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接尾語 <bpt id="p1">**</bpt>database.windows.net<ept id="p1">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>tdn (target database name)<ept id="p1">**</ept> – The name of the database to import into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tdn(ターゲット データベース名)<ept id="p1">**</ept> – インポートするデータベースの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The database should <bpt id="p1">**</bpt>not<ept id="p1">**</ept> already exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースが既に存在していては<bpt id="p1">**</bpt>いけません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The import process will create it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート処理が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>sf (source file)<ept id="p1">**</ept> – The path and name of the file to import from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>sf(ソース ファイル)<ept id="p1">**</ept> – インポートするファイルのパスと名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>tu (target user)<ept id="p1">**</ept> – The SQL user name for the target Azure SQL database instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tu(ターゲット ユーザー)<ept id="p1">**</ept> – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>We recommend that you use the standard <bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept> user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準の <bpt id="p1">**</bpt>sqladmin<ept id="p1">**</ept> ユーザーを使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can retrieve the password for this user from your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>tp (target password)<ept id="p1">**</ept> – The password for the target Azure SQL database user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tp(ターゲット パスワード)<ept id="p1">**</ept> – ターゲットの Azure SQL データベース ユーザーのパスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>DatabaseServiceObjective<ept id="p1">**</ept> – Specifies the performance level of the database such as S1, P2 or P4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DatabaseServiceObjective<ept id="p1">**</ept> – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>To query the service level objective of the current database, run the following query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Run a script to update the Finance and Operations database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations データベースを更新するスクリプトを実行する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the source and target environments have different SQL user passwords, you must run the following script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースとターゲット環境の SQL ユーザーのパスワードが異なる場合は、次のスクリプトを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You must also run this script if you aren't sure whether the passwords differ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パスワードとは異なるかどうかが不明な場合は、このスクリプトを実行することも必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Run the script against the imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータベースに対して、スクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The script drops the database users and then re-creates them so that they have the correct passwords for the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプトは、データベース ユーザーを削除してから、ターゲット環境の正しいパスワードを持つように再作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Synchronize the database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>These services will have open connections to the Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>World wide web publishing service (on all AOS computers)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Management Reporter 2012 Process service (on business intelligence <ph id="ph1">\[</ph>BI<ph id="ph2">\]</ph> computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス <ph id="ph1">\[</ph>BI<ph id="ph2">\]</ph> コンピューターのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>On the AOS computer where the bacpac import was performed, run the following script in Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bacpac インポートが実行された AOS コンピューターで、Management Studio の次のスクリプトを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This script renames the original database and then renames the newly imported database so that it uses the original database name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In this example, the original database was named axdb<ph id="ph1">\_</ph>123456789, and the newly imported database was named importeddb.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、元のデータベースは axdb<ph id="ph1">\_</ph>123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Make sure that you're using the SQL Server 2016 version of Management Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Synchronize the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを同期させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, and run the following commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として <bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Use services.msc to restart the services that you stopped earlier:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">services.msc を使用して、以前に停止したサービスを再起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>World wide web publishing service (on all AOS computers)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Management Reporter 2012 Process service (on BI computers only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>At this point, you can open the Finance and Operations application URL and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Verify that the application works as you expect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションが予期したとおりに動作することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Then drop the original database by running the following script in Management Studio on the AOS computer where you performed the bacpac import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、bacpac のインポートを実行した AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Re-provision Retail components in the target environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となる環境で Retail コンポーネントを再プロビジョニング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Reprovisioning is only required if you are restoring or importing the database on another environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを別の環境で復元またはインポートする場合のみ再プロビジョニングが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Limitations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">制限</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>After you import a database, the link between the database and document handling documents that are stored in Azure blob storage might be broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをインポートすると、Azure Blob Storage に保管されているデータベースおよびドキュメント処理のドキュメント間のリンクが破損している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>If you have custom code that uses the X++ <bpt id="p1">**</bpt>FileUpload<ept id="p1">**</ept> class to put files in blob storage, the links to those files might also be broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ <bpt id="p1">**</bpt>FileUpload<ept id="p1">**</ept> クラスを使用して BLOB ストレージにファイルを格納するカスタム コードがある場合、それらのファイルへのリンクも壊れる可能性があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>