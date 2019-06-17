<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="database-refresh.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>database-refresh.da38f5.e7963926dd0d05e0c74819de46cd5981fbdff7b6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e7963926dd0d05e0c74819de46cd5981fbdff7b6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>c5edff04f35a067934fddebd166906edc003e7c5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/23/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\database-refresh.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Refresh database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to perform a refresh of a database for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースの更新を実行する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Refresh database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use Microsoft Dynamics Lifecycle Services (LCS) to perform a refresh of the database for  Dynamics 365 for Finance and Operations to a sandbox user acceptance testing (UAT) environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス ユーザー受け入れテスト (UAT) 環境への Dynamics 365 for Finance and Operations のデータベースの更新の実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A database refresh lets you copy the transactional and financial reporting databases of your production environment into the target, sandbox UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの更新対象となるサンド ボックス UAT 環境に、本番環境のトランザクションおよび財務報告データベースをコピーできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If you have another sandbox environment, you can also copy the databases from that environment to your target, sandbox UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス UAT 環境にデータベースをコピーすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Copying production data to your sandbox environment for the purpose of production reporting is not supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産報告を目的としてサンドボックス環境に生産のデータをコピーすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Self-service database refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのセルフ サービスエ更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>With the goal of providing Data Application Lifecycle Management (also referred to as <bpt id="p1">*</bpt>DataALM<ept id="p1">*</ept>) capabilities to our customers without relying on human or manual processes, the Lifecycle Services team has introduced an automated <bpt id="p2">**</bpt>Refresh database<ept id="p2">**</ept> action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">人手または手動のプロセスに依存しないでお客様にデータ アプリケーション ライフサイクル管理 (<bpt id="p1">*</bpt>DataALM<ept id="p1">*</ept> とも呼ばれます) 機能を提供することを目標として、Lifecycle Services チームは自動化された<bpt id="p2">**</bpt>データベースの更新<ept id="p2">**</ept>アクションを導入しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This process is outlined below:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスの概要を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Visit your target sandbox on the <bpt id="p1">**</bpt>Environment Details<ept id="p1">**</ept> page, and click the <bpt id="p2">**</bpt>Maintain<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>Move database<ept id="p3">**</ept> menu option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページで 対象のサンドボックスを確認し 、メニューオプションの <bpt id="p2">**</bpt>メンテナンス<ept id="p2">**</ept> <ph id="ph1">\&gt;</ph> <bpt id="p3">**</bpt>データベースの移動<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Select the <bpt id="p1">**</bpt>Refresh database<ept id="p1">**</ept> option and choose your source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データベースの選択<ept id="p1">**</ept> オプションを選択し、ソース環境を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Note the warnings and review the list of data elements that are not copied from the source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">警告に注意し、ソース環境からコピーされていないデータの要素の一覧を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The refresh operation will begin immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新操作がすぐに開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>After the refresh operation is completed, you must <bpt id="p1">**</bpt>sign off<ept id="p1">**</ept> on the operation before you can perform another servicing operation, such as package deployment, database movement, or upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新操作が完了したら、パッケージ展開、データベース移動、アップグレードなどの別のサービス操作を実行する前に、工程で<bpt id="p1">**</bpt>サインオフ<ept id="p1">**</ept>する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Refresh operation failed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新操作が失敗しました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In case of failure, the option to perform a rollback is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗した場合、ロールバックを実行するオプションを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>By clicking the <bpt id="p1">**</bpt>Rollback<ept id="p1">**</ept> option after the operation has initially failed, your target sandbox environment will be restored to the state it was before the refresh began.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程が最初に失敗した後に<bpt id="p1">**</bpt>ロールバック<ept id="p1">**</ept> オプションをクリックすると、対象となるサンドボックス環境が更新の開始前の状態に戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This is made possible by the Azure SQL point-in-time restore capability to restore the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL ポイントインタイム復元機能により、データベースを復元できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This is often required if a customization, that is present in the target sandbox, cannot complete a database synchronization with the newly refreshed data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく更新されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To determine the root cause of the failure, download the runbook logs using the available buttons before starting the rollback operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Data elements that aren't copied during refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新中にはコピーされないデータ要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When refreshing a production environment to a sandbox environment, or a sandbox environment to another sandbox environment, there are certain elements of the database that are not copied over to the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境をサンドボックス環境に、またはサンドボックス環境を別のサンドボックス環境に更新するときは、ターゲット環境にコピーされない特定のデータベース要素があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>These elements include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要素として次のものがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Email addresses in the LogisticsElectronicAddress table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LogisticsElectronicAddress テーブル内の電子メール アドレス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>SMTP password in the SysEmailSMTPPassword table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMTPPassword テーブルの SMTP パスワード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>SMTP Relay server in the SysEmailParameters table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailParameters テーブルの SMTP 中継サーバー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Document attachments in the DocuValue table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DocuValue テーブル内のドキュメント添付ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>All users except the admin will be set to <bpt id="p1">**</bpt>Disabled<ept id="p1">**</ept> status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者以外のすべてのユーザーは <bpt id="p1">**</bpt>無効<ept id="p1">**</ept> のステータスに設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>All batch jobs are set to <bpt id="p1">**</bpt>Withhold<ept id="p1">**</ept> status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバッチ ジョブは、 <bpt id="p1">**</bpt>保留<ept id="p1">**</ept> 状態に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Some of these elements aren't copied because they are environment-specific.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要素は、環境固有のものであるためコピーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Examples include BatchServerConfig and SysCorpNetPrinters records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例には、BatchServerConfigおよびSysCorpNetPrintersの各レコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Other elements aren't copied because of the volume of support tickets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>For example, duplicate emails might be sent because Simple Mail Transfer Protocol (SMTP) is still enabled in the UAT environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、簡易メール転送プロトコル (SMTP) はUAT環境でも有効になっているため、重複する電子メールが送信されてしまう可能性があります。また、バッチジョブも有効になっているため、無効な統合メッセージが送信されてしまう可能性もあるため、管理者がポストリフレッシュクリーンアップを行う前にユーザーが有効化されてしまう可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Environment administrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境管理者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The System Administrator account in the target environment (UserId of 'Admin') is reset to the value found in the web.config file on the target.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This should be the same value as that of the Administrator from Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Lifecycle Services の管理者と同じ値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To preview which account this will be, visit your target sandbox <bpt id="p1">**</bpt>Environment Details<ept id="p1">**</ept> page in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The value of the <bpt id="p1">**</bpt>Environment Administrator<ept id="p1">**</ept> field that was selected when the environment was first deployed is updated to be the System Administrator in the transactional database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が最初に展開されたときに選択された <bpt id="p1">**</bpt>環境管理者<ept id="p1">**</ept> フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This also means that the tenant of the environment will be that of the Environment Administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、環境のテナントが環境管理者のテナントとなることも意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you have used the Admin User Provisioning Tool on your environment to change the web.config file to a different value, it may not match what is in Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If you require a different account to be used, you will need to deallocate and delete the target sandbox, and redeploy selecting another account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>After this, you can perform another refresh database action to restore the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Conditions of a database refresh</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース更新の条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Here is the list of requirements and conditions of operation for a database refresh:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース更新の操作の要件および条件の一覧を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Any previous servicing operation, such as a package deployment or prior database refresh, <bpt id="p1">*</bpt>must be signed off<ept id="p1">*</ept> from your environment details page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの展開や事前データベース更新など、環境の詳細ページから以前のサービス操作を<bpt id="p1">*</bpt>サインオフする必要があります<ept id="p1">*</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>A refresh erases the existing database in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新により、ターゲット環境の既存のデータベースが消去されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The existing database can't be recovered after the refresh is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新が完了すると、既存のデータベースを復元することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The target environment will be unavailable until the refresh process is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新プロセスが完了するまで、ターゲット環境は使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The refresh will affect only the Finance and Operations and Financial Reporting databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リフレッシュは、Finance and Operations and Financial Reporting データベースにのみ影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Documents in Azure blob storage are not copied from one environment to another.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure blob storage のドキュメントは、ある環境から別の環境にコピーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>This means that attached document handling documents and templates won't be changed and will remain in their current state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、添付されたドキュメント処理ドキュメントとチームプレートは変更されず、現在の状態にとどまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>All users except the Admin user and other internal service user accounts will be unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This process allows the Admin user to delete or obfuscate data before allowing other users back into the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスにより、ほかのユーザーがシステムに復帰する前に管理者ユーザーがデータを削除または難読化できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All data management framework with recurring import and export jobs must be fully processed and stopped in the target system prior to initiating the restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期的なインポートおよびエクスポート ジョブを持つすべてのデータ管理フレームワークは完全に処理され復元が開始される前にターゲット システムで停止する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>In addition, we recommend that you select the database from the source after all recurring import and export jobs have been fully processed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、すべての定期的なインポートおよびエクスポート ジョブが完全に処理された後に、データベースをソースから選択することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This will ensure there are no orphaned files in Azure storage from either system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、いずれかのシステムから Azure ストレージにオーファン ファイルが存在しないことが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This is important because orphaned files cannot be processed after the database is restored in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、データベースがターゲット環境にリストアされた後にオーファン ファイルを処理できないため重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>After the restore, the integration jobs can be resumed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元後、統合ジョブを再開することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Any user with a role of Project owner or Environment manager in LCS will have access to the SQL and machine credentials for all non-production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクト所有者または環境マネージャーのロールを持つユーザーは、すべての非実稼働環境の SQL とマシンの資格情報にアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Steps to complete after a database refresh for environments that use Retail functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 機能を使用する環境のデータベース更新後に実行する手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Refresh is denied for environments running Platform update 12 or earlier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム アップデート 12 以前を実行する環境で更新が拒否される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The database refresh process can't be completed if the environment is running Microsoft Dynamics 365 for Finance and Operations, Enterprise edition platform update 12 (November 2017) or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations 、Enterprise Edition のプラットフォームアップデート 12 (2017年 11月) 更新版 またはそれ以前の環境で動作している場合は、データベース更新の処理を実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>For more information, see the <bpt id="p1">[</bpt>list of currently supported Platform updates<ept id="p1">](../migration-upgrade/versions-update-policy.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細は、<bpt id="p1">[</bpt>現在サポートされているプラットフォーム更新の一覧<ept id="p1">](../migration-upgrade/versions-update-policy.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Incompatible version of Financial Reporting between source and target environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境とターゲット環境間での財務報告の互換性のないバージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The database refresh process (self-service or via a service request) can't be completed successfully if the version of Financial Reporting in the target environment is earlier than the version in the source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行対象とする環境の財務報告のバージョンが実行元の環境よりも古い場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>To resolve this issue, update both environments so that they have the latest version of Financial Reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を解決するには、両方の環境で財務報告が最新バージョンとなるように更新を行ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>To determine the version you have installed in your source and target environments, visit the <bpt id="p1">**</bpt>View detailed version information<ept id="p1">**</ept> link on the <bpt id="p2">**</bpt>Environment Details<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行対象と実行元の環境でインストールしたバージョンを確認するには、 <bpt id="p1">**</bpt>詳細バージョン情報を表示<ept id="p1">**</ept> のリンクを確認します。これは <bpt id="p2">**</bpt>環境の詳細<ept id="p2">**</ept> ページにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Search for <bpt id="p1">**</bpt>MRApplicationService<ept id="p1">**</ept> and ensure that the target environment is greater than or equal to the source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MRApplicationService<ept id="p1">**</ept> を検索し、対象となる環境が実行元の環境と同等かそれ以上のバージョンあることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>For customers that are using version 8.1 or later:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8.1またはそれ以降のバージョンを使用しているお客様</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Go to the <bpt id="p1">**</bpt>Update<ept id="p1">**</ept> tiles for your UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept> のタイルメニューを開き、UAT環境を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Save the updates to your Project asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新内容をプロジェクトの資産ライブラリに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Apply this package to your UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパッケージをUAT環境に適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Verify that the error has been resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが解決されたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>For customers that are using version 8.0 or earlier:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8.0 またはそれ以前のバージョンを使用しているお客様</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Review the Environment history of your source environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行元環境の環境履歴を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Specifically, look for any "Platform and application binary package" that might have been deployed to the source environment and not the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、「プラットフォームおよびアプリケーションのバイナリ パッケージ」のいずれかが実行元の環境に展開されていることを確認します。対象の環境ではありませんのでご注意ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Apply this binary package to your target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このバイナリパッケージをUAT環境に適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Verify that the error has been resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーが解決されたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Incompatible application versions between source and target environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース環境とターゲット環境間での互換性のないアプリケーション バージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The database refresh process (self-service or via service request) cannot be completed if the Application release of your source and target environment are not the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースおよびターゲット環境のアプリケーション リリースが同じでない場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>This is because the data upgrade process is not executed by database movement operations such as refresh, and data loss can occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、データ アップグレード プロセスが、更新などのデータベース移動操作によって実行されず、データ損失が発生する可能性があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>If upgrading your sandbox UAT environment to a newer Application version (for example, 7.3 to 8.1), be sure to perform the database refresh action prior to starting the upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアプリケーション バージョンにサンドボックス UAT 環境をアップグレードする場合 (たとえば、7.3 から 8.1)、必ずアップグレードを開始する前にデータベースの更新アクションを実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>After your sandbox is upgraded to the newer version, you cannot restore an older production environment database in to the sandbox UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックスが新しいバージョンにアップグレードされると、サンドボックス UAT 環境に古い実稼働環境データベースを復元することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Conversely, if your production environment is newer than your target sandbox, you will need to either upgrade the target sandbox prior to the refresh or simply deallocate, delete, and redeploy prior to performing the refresh.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">逆に、実稼働環境がターゲット サンドボックスよりも新しい場合、更新前にターゲット サンドボックスをアップグレードするか、更新の実行前にそのまま割り当て解除、削除、および再展開する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>