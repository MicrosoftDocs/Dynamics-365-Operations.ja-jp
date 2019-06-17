<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="database-point-in-time-restore.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>database-point-in-time-restore.58fc47.a75100be6f5e7382d203897e84eaec86a2d0cf1b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a75100be6f5e7382d203897e84eaec86a2d0cf1b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\database-point-in-time-restore.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Database point-in-time restore (PITR)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ポイントインタイム復元 (PITR)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to perform a point-in-time restore of a database for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースのポイントインタイム復元を実行する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Database point-in-time restore (PITR)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース ポイントインタイム復元 (PITR)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can use Microsoft Dynamics Lifecycle Services (LCS) to perform the point-in-time restore (PITR) for a Dynamics 365 for Finance and Operations sandbox user acceptance testing (UAT) environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) を使用し、Dynamics 365 for Finance and Operations サンドボックス ユーザー受け入れテスト (UAT) 環境のポイントインタイム復元 (PITR) を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Self-service point-in-time restore</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セルフサービスポイントインタイム復元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Restore operation failed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗した操作の復元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In case of failure, the option to perform a <bpt id="p1">**</bpt>Rollback<ept id="p1">**</ept> is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗した場合、<bpt id="p1">**</bpt>ロールバック<ept id="p1">**</ept>を実行するオプションを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>By clicking the rollback option after the operation has initially failed, your target sandbox environment will be restored to the state it was before the restore began.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程が最初に失敗した後にロールバック オプションをクリックすると、対象となるサンドボックス環境が復元の開始前の状態に戻されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This will restore the previous database from the deleted databases storage on the Azure SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、以前のデータベースが Azure SQL Server の削除されたデータベースの記憶域から復元されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This is often required if a customization is present in the target sandbox that cannot complete a database synchronization with the newly-restored data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しく復元されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To determine the root cause of the failure, download the runbook logs using the available buttons before starting the rollback operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Data elements that need attention after restore</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元後に注意が必要なデータの要素</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>When restoring a database from a previous point-in-time, keep in mind that the database is provided as-was.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の時点からデータベースを復元する場合は、データベースがそのまま提供されることに留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This means that batch jobs and other data elements in the system could be in an in-progress state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、システム内のバッチ ジョブとその他のデータ要素は進行中の状態の可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>These will require manual review.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、手動の確認が必要となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Environment administrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境管理者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The System Administrator account in the target environment (UserId of 'Admin') is reset to the value found in the web.config file on the target.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This should be the same value as that of the Administrator from Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Lifecycle Services の管理者と同じ値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To preview which account this will be, go to your target sandbox <bpt id="p1">**</bpt>Environment Details<ept id="p1">**</ept> page in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの <bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept> ページにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The value of the <bpt id="p1">**</bpt>Environment Administrator<ept id="p1">**</ept> field that was selected when the environment was first deployed is updated to be the System Administrator in the transactional database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が最初に展開されたときに選択された <bpt id="p1">**</bpt>環境管理者<ept id="p1">**</ept> フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>This also means that the tenant of the environment will be that of the Environment Administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、環境のテナントが環境管理者のテナントとなることも意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>If you have used the Admin User Provisioning Tool on your environment to change the web.config file to a different value, it may not match what is in Lifecycle Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If you require a different account, you will need to deallocate and delete the target sandbox, and redeploy by selecting another account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別のアカウントを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>After this, you can perform another refresh database action to restore the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Steps to complete after a database restore for environments that use Retail functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 機能を使用する環境のデータベース復元後に実行する手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Point-in-time restore breaks the chain of available restore points</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元により利用可能な復元ポイントのチェーンが壊れる</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The restore database process always creates a new database based on a previous point-in-time snapshot.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元データベース処理は、常に前の時点のスナップショットに基づいて新しいデータベースを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Because of this, the new database does not have any restore history, but does begin to accrue new restore points going forward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このため、新しいデータベースには、復元の履歴はありませんが、今後使用される新しい復元ポイントを取得し始めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This means that after performing point-in-time restore you will not be able to do so again using the same restore date and time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、ポイントインタイム復元を実行した後、同じ復元日時を使って復元することはできなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Going forward, the Lifecycle Services team will work to improve point-in-time restore by leveraging the restore history of deleted databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後、Lifecycle Services チームは、削除されたデータベースの復元履歴を活用することで時点でポイントインタイム復元を向上させるよう努めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This will allow continual restore back to the same point-in-time for scenarios such as destructive testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これによって、破壊試験などのシナリオで同じ時点に継続的に復元できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>This will be fixed in an upcoming release of LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、LCS の今後のリリースで修正されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Restore is denied for environments running Platform update 3 or earlier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム アップデート 3 以前を実行する環境で復元が拒否される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The restore database process cannot be completed if the environment is running Platform update 3 or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境でプラットフォーム更新 3 以前を実行している場合は、データベース復元の処理を実行することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For more information, see the <bpt id="p1">[</bpt>list of currently supported Platform updates<ept id="p1">](..//migration-upgrade/versions-update-policy.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細は、<bpt id="p1">[</bpt>現在サポートされているプラットフォーム更新の一覧<ept id="p1">](..//migration-upgrade/versions-update-policy.md)</ept>を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>