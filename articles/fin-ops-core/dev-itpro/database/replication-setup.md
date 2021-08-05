---
title: AX 2012 からのアップグレード - SQL トランザクション レプリケーション
description: このトピックでは、大量の Microsoft Dynamics AX 2012 データベースを Finance and Operations アプリにアップグレードする方法を説明します。
author: sarvanisathish
ms.date: 04/26/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: eccbd553702e128f8c7c8fff6177d3a81dc5c5a3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347858"
---
# <a name="upgrade-from-ax-2012---sql-transactional-replication"></a>AX 2012 からのアップグレード - SQL トランザクション レプリケーション 

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、大量の Microsoft Dynamics AX 2012 データベースを Finance and Operations アプリにアップグレードする方法を説明します。 このプロセスでは、SQL トランザクション レプリケーションを使用して、AX 2012 オンプレミス データベースからサンドボックス環境にスキーマとデータを取り込みます。

共有サンドボックス環境で実行する前に、開発環境でデータ アップグレード プロセスを実行することを強くお勧めします。 この方法を使用すると、データを正常にアップグレードするために必要な時間全体を削減することができます。 詳細については[AX 2012からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト](../migration-upgrade/prepare-data-upgrade.md) を参照してください。

## <a name="replication-setup"></a>レプリケーションの設定

レプリケーションとは、データとデータベース オブジェクトをデータベース間でコピーして配布し、データベース間で同期して整合性を維持するための一連のテクノロジーです。 この移行とコピーはソース システムのオンラインで行うので、レプリケーション プロセス中に Finance and Operations サービスのダウンタイムは不要です。 **Online Database Migration Toolkit** ではトランザクション レプリケーションを使用します。 通常、これはスケーラビリティと可用性を向上させるために高スループットを必要とするサーバー間のシナリオで使用されます。

**Online Database Migration Toolkit** では、**共有アセット ライブラリ > モデル** の Lifecycle Services (LCS) からダウンロードできます。

## <a name="prerequisites"></a>必要条件
**Online Database Migration Toolkit** には次の必要条件が必要です。

- ソース SQL Server には、インストールされ有効になっているレプリケーション機能が必要です。 レプリケーションが有効かどうかを確認するには、次の SQL スクリプトを実行します。

     ```sql
     -- If @installed is 0, replication must be added to the SQL Server installation. 
    USE master;
    GO  
    DECLARE @installed int;  
    EXEC @installed = sys.sp_MS_replication_installed;  
    SELECT @installed; 
     ```
     
    レプリケーション コンポーネントがインストールされていない場合は、[SQL Server レプリケーションのインストール](/sql/database-engine/install-windows/install-sql-server-replication?view=sql-server-ver15) の手順に従います。 

-   SQL Agent をソース データベース サーバーで実行する必要があります。

-   SA 認証: ユーザーにはソース データベースとターゲット データベースでの DB_Owner 特権が必要です。 ソース データベースで、ユーザーは masterDb および sourceDb にアクセスできる必要があります。

-   ソース IP の許可リストに従ってターゲット ファイアウォールを更新します。 これは LCS 経由で実行できます。 これによって 8 時間のアクセスのみが許可されます。 許可リストの後、8 時間以上のアクセス権があるターゲット データベースで次のストアド プロシージャを実行する必要があります。

     ```sql
     -- Create database-level firewall setting for IP a.b.c.d 
     EXECUTE sp_set_database_firewall_rule N'AX 2012 Upgrade', 'a.b.c.d', 'a.b.c.d'; 
     ```
- 以下はレプリケーションの待機時間/パフォーマンスを最適化するための、param.xml で更新できる微調整されたディストリビューターのパラメーターです。
    - MaxBcpThreads
    - NumberOfPublishers
    - ディストリビューター データベースのパス

- ターゲット環境で AOS サービスを停止して、ターゲット データベースのレプリケーションを効率的に行います。 ターゲットで AOS を実行すると、レプリケーション プロセスの速度が低下する可能性があります。 これにより、レプリケーション プロセスでスキーマ ロックやデッドロックが発生する可能性があります。

- ディストリビューターの設定時: このスクリプトにより、ソース サーバーにデータベースが作成されます。 十分なスペースがあることを確認します。 ソース データベースのサイズを最小限に抑えることが推奨されています。 params.xml では、指定されたパスでデータベースを作成できるようにディストリビューター データベースのパスを指定します。

- params.xml の更新

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <! -- Database replication parameters for an AX 2012 to Dynamics 365 upgrade -->
    <Config>
      <!-- Edit the properties in this section for your source AX 2012 database -->
         <SourceDatabase>
                 <Server>SQLSERVERNAME\SQLINSTANCE</Server>
                 <Database>MicrosoftDynamicsAX</Database>
                  <UserName>ReplicationUser</UserName>
                  <Password>********************</Password>
         </SourceDatabase>
         <!-- Edit the properties in this section for your target Dynamics 365 database -->
         <TargetDatabase>
                  <Server>dbmigration.database.windows.net</Server>
                   <Database>dbms-prod</Database>
                   <UserName>axdbadmin</UserName>
                   <Password>*******************</Password>
        </TargetDatabase>
         <!-- Edit the properties in this section for your local SQL replication settings -->
        <SQLReplicationSettings>
        <!-- Ensure that you have enough space in the drive/path -->
        <SnapShotWorkingDir>D:\SQLServer\SnapShot</SnapShotWorkingDir>
             <DistributorDBDataFolder>D:\SQLServer\Data</DistributorDBDataFolder>
              <DistributorLogFolder>D:\SQLServer\Data</DistributorLogFolder>
              <!-- Based on the number of cores, you can set this, but the max this value can be is 8. This value should be between 4 to 8 -->
              <MaxBCPThreads>4</MaxBCPThreads>
              <!-- To increase the performance of the replication. This value should be between one and three. This value will be used to create the number of publishers for tables with primary keys. -->
              <NumberOfPublishers>2</NumberOfPublishers>
              <!-- Ignore DB objects xml file. The database objects listed in these files will be not be replicated. -->
               <IgnoreTablesList>\Data\ignoretables.xml</IgnoreTablesList>
               <IgnoreFunctionsList>\Data\ignorefunctions.xml</IgnoreFunctionsList>
        </SQLReplicationSettings>
    </Config>
    ```
    
- XML スキーマ: レプリケーション中に選択したテーブル、ビュー、および機能を無視するには、この情報を追加します。

    ```xml
    <IgnoreTables>                      <IgnoreFunctions>
        <Name>SYSDATABASELOG</Name>         <Name></Name>
    </IgnoreTables>                      </IgnoreFunctions>
    ```
    
## <a name="configuring-replication"></a>レプリケーションの構成

**SQLTransactionalReplication** フォルダーには、SQL トランサクション レプリケーションを構成するのに必要なすべての Windows PowerShell スクリプトがあります。 これらのスクリプトは、次の順序を使用して実行する必要があります。 プロセスが終了されるのを待つ必要があります。

1. **Replication_01_DataBaseCleanup.ps1** - ターゲット データベースが空になります。
2. **Replication_02_Distributor.ps1** - 完了時に、システム データベースの下のソース データベース サーバーで、ディストリビューター データベースが作成されます。
3. **Replication_03_PublisherTables.ps1** - パブリッシャー スクリプトが正常に実行されると、パブリケーションはレプリケーション フォルダーの下に作成されます。 これは完了するまでに少し時間がかかるので注意してください。 これにより、AXDB_PUB_TABLE_Obj_[*] というパブリッシャーが作成されます。

    > [!WARNING]
    > 切替スクリプトを実行する前に、データ レプリケーションが完了するまで待機します。 ステータスは次の方法で確認できます。
    > - レプリケーション モニター: ソース サーバーで、**レプリケーター** フォルダーを右クリックし、**レプリケーション モニターの起動** を選択します。 
    > - レプリケーション ツールキットに埋め込まれた GetStatus.ps1 スクリプトを実行します。 **DataReplicationStatus** は各 AXDB_PUB_TABLE_Obj_[*] パブリケーションに対して完了に設定する必要があります。
  
4. **Replication_04_PublisherOtherObjects.ps1** - 新しいパブリケーションを作成して機能をターゲット データベースにレプリケートします。 関数を移動しない場合は、この手順を省略できます。 これはすぐに完了することに注意してください。 これにより、AX_PUB_OtherObjects というパブリッシャーが作成されます。
5. **CutOver_01_PublisherNoPK**.ps1 - これによりレプリケートするために 2 つのパブリケーション - 主キーのないテーブル、およびパブリケーション名を持つロックされたテーブル: AX_PUB_NoPKTable, AXDB_PUB_TABLE_Locked が作成されます
7. **CutOver_02_PKDeletion_PostReplication.ps1** - これにより、主キーのない一時テーブルがクリーン アップされます。 AX_PUB_NoPKTable というパブリケーションを削除します。
8. **CutOver_03_RetrieveAndCreateNoPKConstraints.ps1** - これにより、ソースから主キーなしのテーブルの制約条件が抽出され、ターゲット データベースに作成されます。
9. **CutOver_04_RemoveReplication.ps1** - データベースのレプリケーションを正常に行った後、このスクリプトを実行してレプリケーション設定情報を削除できます。 スナップショット フォルダーをエラーなしで削除する場合は、ソース Db で次のストアド プロシージャを実行します。 そうしない場合、実行後に手動で削除する必要があるスナップショット フォルダーをシステムが削除できなかったというエラーが表示されます。

```sql
EXEC master.dbo.sp_configure 'show advanced options', 1
RECONFIGURE WITH OVERRIDE
EXEC master.dbo.sp_configure 'xp_cmdshell', 1
RECONFIGURE WITH OVERRIDE
```

レプリケーション設定時に、ソース データベースに次のパブリケーションが作成されます。

![レプリケーション設定時に、ソース データベースに作成されるパブリケーション。](media/Replication.png)

## <a name="find-the-replication-status-and-get-an-exception"></a>レプリケーション ステータスの検索と例外の取得

レプリケーションのステータスを検索して例外を取得するには、PowerShell スクリプトを実行し、終了するまで待機します。

**GetStatus.ps1** - このスクリプトを実行する場合、**レプリケーション ステータス** テーブルが、スキーマの AgentId、PublicationName、Job、LastSynced、JobStatus、ReplicationStatus、および Comments と共に一覧表示されます。

- AgentId - ジョブに関する例外の詳細をフェッチするために使用されます。
- PublicationName - データをレプリケートするために作成されたパブリケーション名です。 同じ情報は、レプリケーション フォルダーの下にある SQLServerExplorer で確認できます。
- Job - ジョブには、スナップショットとデータ レプリケーションの 2 つのタイプがあります。
- JobStatus - これにより、開始済、成功、処理中、アイドル、再試行、または失敗のステータスが表示されます。 スナップショット ジョブでは、ステータスが 「成功」 になった後は実行されません。 データ レプリケーション ジョブでは、データベースの更新情報に基づいてステータスが引き続き変更されます。
- ReplicationStatus - これはデータ レプリケーション ジョブにのみ適用されます。 ステータスには、待機中、処理中、および完了が含まれます。
- Comments - JobStatus が InProgress の場合、引き続き変更されます。
 
**GetException.ps1** - 例外を取得するために AgentId を指定します。 AgentId はステータスから取得できます。

## <a name="find-the-replication-configuration-and-status-via-sql-server-management-studio"></a>SQL Server Management Studio 経由でのレプリケーションの構成とステータスの検索
SQL Server Management Studio を使用してレプリケーション ステータスの構成とステータスを検索するには、次の手順に従います。

- レプリケーション機能が使用可能でサーバーにインストールされているかどうかを判断するには、オブジェクト エクスプローラーのレプリケーション フォルダーを表示する必要があります。
   
   ![レプリケーション フォルダー。](media/Replication1.png)

- **Replication_03_PublisherTables.ps1** スクリプトを実行した後、レプリケーション フォルダーの下に構成済みのパブリッシャーを表示する必要があります。
    
    ![レプリケーション フォルダーの下のパブリッシャーを表示します。](media/Replication2.png)

- レプリケーション ステータスを確認するには、**レプリケーション** フォルダーを右クリックし、**レプリケーション モニターの起動** を選択します。
   
   ![メニューのレプリケーション モニターの起動を選択します。](media/Replication3.png)

- **レプリケーション モニター** ウィンドウでは、レプリケーション用に作成されたすべてのパブリッシャーを表示できます。
    
    ![レプリケーション用に作成されたすべてのパブリッシャー。](media/Replication4.png)

- **スナップショット** タブを選択すると、スナップショットのステータスが表示されます。
  
  ![スナップショット タブを選択すると、スナップショットのステータスが表示されます。](media/Replication5.png)

- 詳細ログ/トランザクションを表示するには、品目をダブルクリックします。
   
   ![詳細ログ/トランザクションを表示するには、品目をダブルクリックします。](media/Replication6.png)

- ターゲットへのデータ レプリケーションを表示するには、**すべてのサブスクリプション** タブを選択し、品目のサブスクリプションをダブルクリックします。 

## <a name="troubleshooting"></a>トラブルシューティング

| **例外** | **解決/修正** |
|-------------------------|-------------------------|
| パブリケーションの作成後にスナップショットの作成に失敗し、次のエラーが発生した場合。<br></br><em>エラー メッセージ:</em></br><em>Source: Microsoft.SqlServer.Smo</em></br><em>Target Site: Void PrefetchObjectsImpl(System.Type, Microsoft.SqlServer.Management.Smo.ScriptingPreferences)</em></br><em>Message: Prefetch objects failed for Database 'AxDB_ASIA'.</em></br><em>Stack:    at Microsoft.SqlServer.Management.Smo.Database.PrefetchObjectsImpl(Type objectType, ScriptingPreferences scriptingPreferences)</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.ObjectPrefetchControl.DoPrefetch(Database database)</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.PrefetchObjects(ObjectPrefetchControl[] objectPrefetchControls)</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.DoPrefetchWithRetry()</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SmoScriptingManager.DoScripting()</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SqlServerSnapshotProvider.DoScripting()</em></br><em>   at Microsoft.SqlServer.Replication.Snapshot.SqlServerSnapshotProvider.GenerateSnapshot()</em></br><em>   at Microsoft.SqlServer.Replication.SnapshotGenerationAgent.InternalRun()</em></br><em>   at Microsoft.SqlServer.Replication.AgentCore.Run() (Source: Microsoft.SqlServer.Smo, Error number: 0)</em> | レプリケーション モニターからスナップショットの作成を再起動します。 |
| サブスクリプションは無効とマークされ、再初期化する必要があります。 NoSync サブスクリプションは削除して再作成する必要があります。 (Source: MSSQLServer, Error number: 21074) | 1) 次のクエリを使用してソース データベースのステータスを確認し、ステータスを特定のパブリケーションのために &quot;2&quot; に更新する</br><em><br>ステータスを確認して、この出力クエリから srvname を取得できる</em></br>**select** * **from** syssubscriptions **WHERE** status != 2</br><em><br>ステータスが !=2 の場合のみ更新</em></br>**Update** syssubscriptions **SET** status = 2 **where** srvname = 'your target server name'</br><br>2) 次のクエリを使用してディストリビューター データベースのステータスを確認し、ステータスを特定のパブリケーションのために &quot;2&quot; に更新する</br><em><br>publication_id を取得するために、次のクエリを使用し、自分のパブリケーション名と一致させる</em></br>**SELECT** * **FROM** MSpublications</br><em><br>次のクエリを使用してステータスを確認する</em></br>**SELECT** * **FROM** MSsubscriptions **WHERE** status !=2 publication_id = &lt;@publicationId&gt;</br><em><br>特定の publication_id に対するステータスが !-2 の時に更新</em></br>**Update** MSsubscriptions **SET** status = 2 **where** publication_id = &lt;@publicationId&gt; |
| エラー メッセージ:</br><em><br>このプロセスでは、「replicationsrv\MSSQLSERVER2016」 に対して 「sp_replcmds」 が実行できませんでした。 (Source: MSSQL_REPL, Error number: MSSQL_REPL20011)</em></br><em>ヘルプ: http://help/MSSQL_REPL20011</em></br><em><br>プリンシパル &quot; dbo &quot; は存在しておらず、このタイプのプリンシパルはアクセス許可を借用できないかまたはアクセス許可がないために、データベース プリンシパルとして実行することができません。 (Source: MSSQLServer, Error number: 15517)</em></br><em>ヘルプの取得: http://help/15517</em></br><em><br>このプロセスでは、「replicationsrv\MSSQLSERVER2016」 に対して 「sp_replcmds」 が実行できませんでした。 (Source: MSSQL_REPL, Error number: MSSQL_REPL22037)</em></br><em>ヘルプの取得: http://help/MSSQL_REPL22037</em> | ソース データベースでこれを実行し、パブリケーションの作成に使用した資格情報でサインインする</br>**EXEC** sp_changedbowner 'sa' |
| パブリケーションを削除するには | このストアド プロシージャをソース データベースで実行する;</br><em><br>サブスクリプションをクリーンアップする:</em></br>**exec** sp_subscription_cleanup @publisher = @publisherServer, @publisher_db = @publisherDb, @publication = @publicationName</br><em><br>サブスクリプションを削除する:</em></br>**exec** sp_dropsubscription @publication = @publicationName, @subscriber = N'all', @article = N'all'</br><em><br>パブリケーションを削除する:</em></br>**exec** sp_droppublication @publication = @publicationName |
| パブリケーションから記事を削除するには、[sp_dropsubscription (Transact-SQL)](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-dropsubscription-transact-sql?view=sql-server-ver15) を参照する | このストアド プロシージャをソース データベースで実行する:<br><br>**EXEC** sp_dropsubscription</br>@publication = @publication、</br>@article = N'All',</br>@subscriber = @subscriber;</br><em><br>例: </em></br>**EXEC** sp_dropsubscription @publication = N'OtherObjects_sp', @article = N'MaintainShipCarrierRole', @subscriber = N'SPARTAN-SRV-NAM-D365OPSDEV-D5E38124F9F8.DATABASE.WINDOWS.NET'; |

