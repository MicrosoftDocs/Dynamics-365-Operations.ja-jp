<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="export-database.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>export-database.4cdcb2.d604f485b3c5656cd3aee8a9a0ae70fa9993310f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d604f485b3c5656cd3aee8a9a0ae70fa9993310f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\export-database.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Export a database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to export a database for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをエクスポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Export a database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use Microsoft Dynamics Lifecycle Services (LCS) to export a database for Microsoft Dynamics 365 for Finance and Operations from a sandbox user acceptance testing (UAT) environment to the Asset library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへの Microsoft Dynamics 365 for Finance and Operations のデータベースのエクスポートの実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Self-service export database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セルフ サービスエクスポート データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Export operation failure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート操作失敗</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If the export operation isn't successful, you can do a <bpt id="p1">*</bpt>rollback<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート操作が正常に行われない場合は、<bpt id="p1">*</bpt>ロールバック<ept id="p1">*</ept>できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you select the <bpt id="p1">**</bpt>Rollback<ept id="p1">**</ept> option after the initial failure of the operation, your source sandbox environment is restored to the state that it was in before the export began.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作が最初に失敗した後に<bpt id="p1">**</bpt>ロールバック<ept id="p1">**</ept> オプションをクリックすると、ソース サンドボックス環境がエクスポートの開始前の状態に戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To determine the root cause of the failure, download the runbook logs by using the available buttons before you start the rollback operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Data elements that aren't exported</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされないデータ要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When you export a database backup from an environment, some elements of the database aren't exported in the backup file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Here are some examples:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか例を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Email addresses in the LogisticsElectronicAddress table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LogisticsElectronicAddress テーブル内の電子メール アドレス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>SMTP password in the SysEmailSMTPPassword table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailSMTPPassword テーブルの SMTP パスワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>SMTP Relay server in the SysEmailParameters table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysEmailParameters テーブルの SMTP 中継サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Document attachments in the DocuValue table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DocuValue テーブル内のドキュメント添付ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Additionally, all users except the admin are disabled, and all batch jobs are set to a status of <bpt id="p1">**</bpt>Withhold<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、管理者以外のすべてのユーザーが無効になり、すべてのバッチ ジョブのステータスが <bpt id="p1">**</bpt>保留<ept id="p1">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Export ran for some time and then reached a "Preparation failed" state</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The export process can time out on Azure SQL Database when large databases are involved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In some cases, the export process can be recovered by using the <bpt id="p1">**</bpt>Resume<ept id="p1">**</ept> action from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、LCS から <bpt id="p1">**</bpt>再開<ept id="p1">**</ept> アクションを使用してエクスポート プロセスを復元することができます、</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The Lifecycle Services team is working to identify known error codes, so that it can add them to the logs for the export database operation to help guide users toward a resolution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services チームは、ユーザーが解決策を見つけるため、データベースのエクスポート操作のログに追加できるように、既知のエラー コードを識別するよう努めています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>These known error codes will be added in a future release of LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Export doesn't show any progress in LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートで LCS に進捗状況が表示されない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The export process differs from other database movement operations and also general package deployment in that it doesn't use a runbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート プロセスは、runbook を使用しないという点で、他のデータベースの移動操作や一般的なパッケージ配置とも異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, the progress indicator in LCS doesn't show any output, as it would typically show in other scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、LCS の進行状況インジケーターには、それ以外のシナリオのような出力が表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Lifecycle Services team is working to improve this behavior in a future release of LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services チームは、LCS の将来のリリースではこの動作が改善されるよう努めています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>