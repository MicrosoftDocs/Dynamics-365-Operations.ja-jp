---
title: Dynamics 365 Finance + Operations セルフサービス環境へのアップグレードのトラブルシューティング
description: このトピックでは、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) セルフサービス環境へのアップグレードに関するトラブルシューティング ガイドを提供します。
author: ttreen
ms.date: 04/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: f378826245e758454cdf47a518c8e11ead94d1cd
ms.sourcegitcommit: 5130446fd5327595b2d67e67cbd1b5661bb2983c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648752"
---
# <a name="troubleshoot-upgrades-to-dynamics-365-finance--operations-self-service-environments"></a>Dynamics 365 Finance + Operations セルフサービス環境へのアップグレードのトラブルシューティング

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) セルフサービス環境へのアップグレードに関するトラブルシューティング ガイドを提供します。

## <a name="scenario-1-the-migration-app-prompts-you-to-enter-project-id-and-environment-id-values"></a>シナリオ 1: 移行アプリでプロジェクト ID と環境 ID を入力するよう求めるメッセージが表示されます。

**ソリューション**

アップグレードするユーザーはプロジェクトに参加し、**ProjectOwner**、**EnvironmentAdmin**、または **OperationsAdmin** のいずれかのロールを割り当てられる必要があります。

## <a name="scenario-2-migration-app-database-connectivity-failed-for-the-source-database-server-or-the-target-database-server"></a>シナリオ 2: ソース データベース サーバーまたはターゲット データベース サーバーに対するアプリのデータベース接続の移行が失敗しました。

**ソリューション**

移行アプリで、[データ更新の準備: 環境の設定活動](data-upgrade-self-service.md#complete-the-data-replication-and-upgrade) 手順の手順 1 を完了します。

## <a name="scenario-3-the-snapshot-for-any-of-the-publications-failed-and-the-failure-can-be-tracked-in-replication-monitor"></a>シナリオ 3: いずれかのパブリケーションのスナップショットが失敗し、レプリケーション モニターでその失敗を追跡することができます。

**ソリューション**

SQL Server レプリケーション モニターの **エージェント** タブで、失敗したパブリケーションを選択します。 スナップショット エージェントを選択したまま (または右クリックして)、**エージェントの開始** を選択して、スナップショットを生成します。

## <a name="scenario-4-one-of-the-steps-fails-in-the-migration-app-and-you-must-rerun-that-step"></a>シナリオ 4: 移行アプリでステップの 1 つが失敗し、その手順を再実行する必要があります。

移行アプリでステップの 1 つが失敗し、その手順を再実行する必要がある場合、次の手順に従います。

1. 移行アプリを閉じます。
1. 移行アプリ フォルダーで、**データ** フォルダーを探します。
1. **データ** フォルダーで、**ReplicationMenu.json** ファイルを開きます。
1. **ReplicationMenu.json** ファイルでは、ID 順序が同じすべてのメニュー オプションが表示されます。 再実行するステップを見つけ、それから **ステータス** の値を **0** に更新します。

    > [!IMPORTANT]
    > **ReplicationMenu.json** ファイルで何も変更しないでください。 また、ファイルを更新する場合は、移行アプリの変更が実行状態ではないことを確認します。

1. 移行アプリを開き、手順を再実行します。

## <a name="scenario-5-after-the-publication-is-created-the-replication-job-fails-and-exceptions-occur"></a>シナリオ 5: パブリケーション作成後、レプリケーション ジョブが失敗し、例外が発生します。

パブリケーション作成後、レプリケーション ジョブが失敗し、次の例外が発生します。

**例外 1:**

> プリンシパル 「dbo」 は存在しておらず、このタイプのプリンシパルはアクセス許可を借用できないかまたはアクセス許可がないために、データベース プリンシパルとして実行することができません。 (Source: MSSQLServer, Error number: 15517)  
ヘルプの取得: `http://help/15517`

**例外 2:**

> このプロセスでは、「replicationsrv\\MSSQLSERVER2016」に対して「sp\_replcmds」が実行できませんでした。 (ソース: MSSQL\_REPL、エラー番号: MSSQL\_REPL20011)  
ヘルプの取得: `http://help/MSSQL_REPL20011`
>
> プリンシパル 「dbo」 は存在しておらず、このタイプのプリンシパルはアクセス許可を借用できないかまたはアクセス許可がないために、データベース プリンシパルとして実行することができません。 (Source: MSSQLServer, Error number: 15517)  
ヘルプの取得: `http://help/15517`

**ソリューション**

SQL Server Management Studio (SSMS) で、クエリ ウィンドウを開き、ソース データベースに接続して、次の SQL コマンドを実行します。

```sql
EXEC sp_changedbowner 'sa'
```

## <a name="scenario-6-the-microsoft-dynamics-lifecycle-service-status-is-failed-but-the-data-upgrade-trigger-is-successful-in-the-migration-app"></a>シナリオ 6: Microsoft Dynamics Lifecycle Service のステータスは「失敗」ですが、移行アプリでデータ アップグレード トリガーは成功しています。

**ソリューション**

移行アプリで **'ds'** オプションを実行します。 このオプションは、すべてのステップおよびサブステップの Microsoft Dynamics Lifecycle Services (LCS) 環境のステータスおよびデータ アップグレード ステータスを読み取ります。

> [!NOTE]
> データ アップグレード ステータスと LCS 環境のステータスが両方とも **失敗** の場合、[データ レプリケーションおよびアップグレードの実施](data-upgrade-self-service.md#complete-the-data-replication-and-upgrade) の手順のステップ 10 のステータスは **再開** に更新されます。 その後、アップグレード プロセスが失敗した時点から操作を再開できます。

## <a name="scenario-7-you-want-to-skip-a-manually-run-step-that-failed-and-move-on-to-other-steps"></a>シナリオ 7: 手動で実行した失敗したステップをスキップし、他の手順に進みます。

手動で実行した失敗したステップをスキップし、他の手順に進むには、次の手順に従います。

1. 移行アプリを閉じます。
1. 移行アプリ フォルダーで、**データ** フォルダーを探します。
1. **データ** フォルダーで、**ReplicationMenu.json** ファイルを開きます。
1. **ReplicationMenu.json** ファイルでは、ID 順序が同じすべてのメニュー オプションが表示されます。 再実行するステップを見つけ、**ステータス** の値を **1** に更新します。 この方法で、ステップを完了としてマークします。

    > [!IMPORTANT]
    > **ReplicationMenu.json** ファイルで何も変更しないでください。 また、ファイルを更新する場合は、移行アプリの変更が実行状態ではないことを確認します。

## <a name="scenario-8-you-want-to-migrate-from-an-old-version-of-the-console-app-to-the-new-version"></a>シナリオ 8: コンソール アプリの古いバージョンから新しいバージョンに移行したいとします。

コンソール アプリの古いバージョンから新しいバージョンに移行するには、次の手順に従います。

1. コンソール アプリの最新バージョンを LCS からダウンロードします。
1. コンソール アプリの古いバージョンから **paramsdata.txt** および **/Data/ReplicationMenu.json** ファイルを取得し、新しいバージョンのコンソール アプリで同じパスに設定します。
1. アプリを再実行します。

## <a name="scenario-9-the-replication-status-for-any-of-the-publications-is-shown-as-waiting-for-snapshot-to-complete-for-more-than-two-hours"></a>シナリオ 9: すべてのパブリケーションのレプリケーション ステータスが 2 時間以上も「スナップショットの終了の待機」と表示されています。

**ソリューション**

レプリケーション モニターで、パブリケーションを選択したまま (または右クリックして)、**サブスクリプションの再初期化** を選択します。

## <a name="scenario-10-you-want-to-resume-the-data-upgrade"></a>シナリオ 10: データ アップグレードを再開する必要があります。

**ソリューション**

コンソール アプリでデータ アップグレード ステータスが更新されていない可能性があります。

データ アップグレードを再開するには、次の手順に従います。

1. コンソール アプリのステータスを確認するには、**ヘルプ** オプションを使用してください。 このオプションには、すべてのメニュー オプションが一覧表示され、現在の状態が表示されます。
1. [データ レプリケーションおよびアップグレードの実施](data-upgrade-self-service.md#complete-the-data-replication-and-upgrade) のステップ 10 のステータスが **成功** の場合、移行アプリで **'ds'** オプションを実行します。 このオプションにより、データ アップグレード ステータスが更新されます。

**'ds'** オプションの実行後、LCS 環境の状態とデータ アップグレード ステータスの 2 つのステータスが一覧表示されます。

- **ケース 1:** LCS 環境の状態が **失敗** で、データ アップグレードの最後のステップが **失敗** の場合、ステップ 10 に **再開** オプションが表示されます。
- **ケース 2:** LCS 環境の状態が **失敗** で、データ アップグレードの最後のステップが **完了** の場合、ステップ 10 に **再開** オプションが表示されます。
- **ケース 3:** LCS 環境の状態が **配置済み** で、データ アップグレードの最後のステップが **完了** の場合、ステップ 10 には **成功** と表示されます。
- **ケース 4:** LCS 環境ステータスが **配置済** で、データ アップグレードの最後のステップが **処理中** の場合、データ アップグレード ジョブはバックグラウンドで実行されるので、ステップ 10 は **成功** と表示されます。

## <a name="scenario-11-after-the-publication-is-created-snapshot-creation-fails-with-errors"></a>シナリオ 11: パブリケーションの作成後にスナップショットの作成に失敗し、エラーが発生します。

パブリケーションの作成後にスナップショットの作成に失敗し、次のエラーがスローされます。

> エラー メッセージ:  
Source: Microsoft.SqlServer.Smo  
Target Site: Void PrefetchObjectsImpl(System.Type, Microsoft.SqlServer.Management.Smo.ScriptingPreferences)  
メッセージ: データベース 'AxDB\_ASIA' のオブジェクトのプリフェッチに失敗しました。  
Stack:    at Microsoft.SqlServer.Management.Smo.Database.PrefetchObjectsImpl(Type objectType, ScriptingPreferences scriptingPreferences)  
             at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.ObjectPrefetchControl.DoPrefetch(Database database)  
          at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.PrefetchObjects(ObjectPrefetchControl\[\] objectPrefetchControls)  
             at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.DoPrefetchWithRetry()  
             at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.DoScripting()  
             at Microsoft.SqlServer.Replication.Snapshot.SqlServerSnapshotProvider.DoScripting()  
             at Microsoft.SqlServer.Replication.Snapshot.SqlServerSnapshotProvider.GenerateSnapshot()  
             at Microsoft.SqlServer.Replication.SnapshotGenerationAgent.InternalRun()  
             at Microsoft.SqlServer.Replication.AgentCore.Run() (Source: Microsoft.SqlServer.Smo, Error number: 0)

**ソリューション**

レプリケーション モニターで、失敗したパブリケーションを選択したまま (または右クリックして)、**スナップショットの生成** を選択します。

## <a name="scenario-12-data-upgrade-presync-and-postsync-processes-are-taking-a-long-time-and-you-want-to-determine-which-process-or-job-is-taking-more-time"></a>シナリオ 12: データ アップグレード PreSync プロセスと PostSync プロセスの時間が長く、どのプロセスまたはジョブに時間がかかっているのを判断する必要があります。

**ソリューション**

**ReleaseUpgradeDB** フレームワークでは、各スクリプトの実行が **ReleaseUpdateScriptsLog** テーブルにログされます。 データ アップグレード プロセスのパフォーマンスを調整するときに、実行されるスクリプトの存続期間を監視できます。 このテーブルで、最も長く実行されるプロセスまたはジョブを簡単に識別できます。
