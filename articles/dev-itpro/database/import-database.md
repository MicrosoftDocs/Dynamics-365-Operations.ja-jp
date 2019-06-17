<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="import-database.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>import-database.099a40.77c20b406567fcd732281dcafedf4fbc896543a4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>77c20b406567fcd732281dcafedf4fbc896543a4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\import-database.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Import a database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to import a database for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをインポートする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Import a database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use Microsoft Dynamics Lifecycle Services (LCS) to import a database for Microsoft Dynamics 365 for Finance and Operations into a sandbox user acceptance testing (UAT) environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス ユーザー受け入れテスト (UAT) 環境への Microsoft Dynamics 365 for Finance and Operations のデータベースのインポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Self-service import database</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セルフ サービス インポート データベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Import operation failure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート操作失敗</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If the import operation isn't successful, you can do a <bpt id="p1">*</bpt>rollback<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート操作が正常に行われない場合は、<bpt id="p1">*</bpt>ロールバック<ept id="p1">*</ept>できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you select the <bpt id="p1">**</bpt>Rollback<ept id="p1">**</ept> option after the initial failure of the operation, your target sandbox environment is restored to the state that it was in before the import began.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作が最初に失敗した後に<bpt id="p1">**</bpt>ロールバック<ept id="p1">**</ept> オプションをクリックすると、対象となるサンドボックス環境がインポートの開始前の状態に戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The rollback operation is made available by the Microsoft Azure SQL Database point-in-time restore capability for restoring the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロールバック操作は、データベースを復元するための Microsoft Azure SQL データベース ポイントインタイム復元機能により使用可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Rollback is often required if a customization that is present in the target sandbox can't complete a database synchronization with the newly imported data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット サンドボックスに存在するカスタマイズが、新しくインポートされたデータでデータベースの同期を完了できない場合、ロールバックがよく必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To determine the root cause of the failure, download the runbook logs by using the available buttons before you start the rollback operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Data elements that require attention after import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート後に注意が必要なデータの要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Specific activities must be completed when you import a database backup into a sandbox UAT environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのバックアップをサンド ボックスUAT環境にインポートするときは、特定の活動を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Here are some examples:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか例を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Make sure that email capabilities are correctly reconfigured or turned off, according to your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">お客様の要件に従って、電子メール機能が正しく再設定または無効になっていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Make sure that integration settings are turned on or off, according to your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">お客様の要件に従って、統合設定がオンまたはオフになっていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make sure that Application Object Server (AOS) servers are added back to required batch groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS) サーバーが必要なバッチ グループに追加されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Make sure that system Help and task guides are reconnected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム ヘルプとタスク ガイドに再接続されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Make sure that batch jobs are set to a status of <bpt id="p1">**</bpt>Waiting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブのステータスが<bpt id="p1">**</bpt>待機中<ept id="p1">**</ept>に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Make sure that users are re-enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが再度有効化されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Environment admin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境管理者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The system admin account in the target environment (<bpt id="p1">**</bpt>Admin<ept id="p1">**</ept> user ID) is reset to the value that is found in the web.config file in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となる環境のシステム管理者アカウント (<bpt id="p1">**</bpt>管理者<ept id="p1">**</ept>ユーザーID) が、その環境内の web.config ファイルに含まれる値にリセットされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This account should be the same as the admin account from LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアカウントは、LCS からの管理者アカウントと同じである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To preview which account this account will be, visit the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for your target sandbox in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアカウントがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The value that was selected in the <bpt id="p1">**</bpt>Environment Administrator<ept id="p1">**</ept> field when the environment was first deployed is updated to the system admin in the transactional database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が最初に展開されたときに <bpt id="p1">**</bpt>環境管理者<ept id="p1">**</ept> フィールドで選択された値は、トランザクション データベース内のシステム管理者となるように更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Therefore, the tenant of the environment will be the tenant of the environment admin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、環境のテナントが環境管理者のテナントになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If you've used the Admin User Provisioning Tool on your environment to change the web.config file, the value might not match the value in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">web.config ファイルを変更するために環境に管理者ユーザー プロビジョニング ツールを使用した場合、値が LCS の値と一致しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If you require that a different account be used, you must deallocate and delete the target sandbox, redeploy, and select another account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You can then do another database refresh action to restore the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Steps to complete after a database import for environments that use Retail functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 機能を使用する環境のデータベースインポート後に実行する手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Import is denied for environments that run Platform update 3 or earlier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム アップデート 3 以前を実行する環境でインポートが拒否される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The import database process can't be completed if the environment is running Platform update 3 or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境でプラットフォーム更新 3 以前を実行している場合は、データベース インポートの処理を実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>See the list of currently supported platform updates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在サポートされているプラットフォーム更新の一覧を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>