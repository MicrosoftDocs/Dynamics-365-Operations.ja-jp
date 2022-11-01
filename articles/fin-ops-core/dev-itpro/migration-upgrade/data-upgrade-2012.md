---
title: AX 2012 からのアップグレード - 開発環境でのデータ アップグレード
description: この記事では、Microsoft Dynamics AX 2012 から最新の財務と運用の開発環境にアップグレードする詳細なプロセスについて説明します。
author: laneswenka
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 80608cb64f8ab967b433af8682e5cdfa43fd104c
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702087"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-development-environments"></a>AX 2012 からのアップグレード - 開発環境でのデータ アップグレード

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

これは、アップグレード プロジェクトのエキサイティングな瞬間です。 このタスクの出力により、Microsoft Dynamics AX 2012 から最新の財務と運用開発環境にアップグレードされた最初のデータセットが提供されます。

このプロセスを共有サンドボックス環境で実行する前に、開発環境で実行することをお勧めします。 このアプローチには 2 つの理由があります。

- 開発者がカスタム データ アップグレード スクリプトを書き込んでテストできるローカル データを提供します。
- これは、データ アップグレード プロセスの繰り返しに費やされる全体的な時間を短縮できます。 開発環境では、問題を即座にデバッグし、コードを調整し、アップグレードを数分以内に再実行することができます。 ただし、より規模の大きいサンドボックス環境ではこの機敏性のレベルが許可されていません。 それらの環境では、問題の修正やデバッグ、コードの更新、更新済コードの配置、およびアップグレードの再実行に少なくとも数時間を要します。

データのアップグレードを実行する前に、[アップグレード アナライザー](upgrade-analyzer-tool.md)を実行して、特定した問題に対応することを強くお勧めします。これは、データのアップグレードが迅速かつ容易になることを保証する手助けになります。

## <a name="end-to-end-data-upgrade-process"></a>エンド ツー エンド データのアップグレード プロセス

![データ アップグレード プロセス。](media/endToEndDataUpgradeProcess.png)

### <a name="prerequisites"></a>必要条件

AX 2012 にてアップグレード前のチェックリストが完了済みである必要があります。 詳細については、[データ アップグレード用のアップグレード前チェックリスト](prepare-data-upgrade.md) を参照してください。

> [!IMPORTANT]
> アップグレードを実行する前に、使用している Dynamics 365 バージョンの最新の **品質更新プログラム** を適用してください。


### <a name="back-up-your-ax-2012-database"></a>AX 2012 データベースをバックアップします

AX 2012 データベースをバックアップするには、標準の Microsoft SQL Server プロセスを使用して BAK ファイルを作成します。 バックアップを作成するときに圧縮オプションを使用すると、ファイル サイズが小さくなり、Microsoft Azure Storage にアップロードおよびダウンロードするために必要な時間が短縮されます。

> [!NOTE]
> AX 2012 データベースの照合順序を、**SQL_Latin1_General_CP1_CI_AS** に変更する必要があります。 異なる照合順序を使用している場合は、Microsoft サポートに問い合わせてください。 

### <a name="upload-the-backup-to-azure-storage"></a>Azure ストレージにバックアップをアップロード

開発環境がローカルまたは Azure で VM としてホストされている場合、2012 データベースのバックアップをそれに転送する必要があります。 ローカル VM では、ネットワーク全体でファイルを直接転送することができますが (それを許可するように仮想ネットワークを構成済みの場合)、Azure でホストされた VM の場合バックアップを Azure Storage にアップロードすることをお勧めします (自分のセキュアな転送サービスまたは SFTP の使用も有効なオプションです)。 これに対して、独自の Azure ストレージ アカウントを指定する必要があります。 Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure Storage Explorer](https://storageexplorer.com/) を使用できます。 これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。

### <a name="download-and-restore-the-backup-to-the-customer-managed-development-environment"></a>顧客管理の開発環境へのバックアップのダウンロードと復元

> [!NOTE]
> 開発環境は、顧客管理の[クラウド ホスト環境](../dev-tools/access-instances.md)としてのみサポートされます。 クラウドホスト環境を使用することで、独自の仕様に合うようにドライブの容量を増やすことができます。

新しい開発環境にバックアップを復元する場合、既存の AXDB データベースを上書きしないでください。 代わりに、元のデータベースの横にある AX 2012 データベースを復元します。 また、アップグレード プロセスは非常にディスクを大量に使用する機能なので、Premium Storage を使用して、クラウドホスト環境を配置してパフォーマンスとタイミングを向上させることができます。

データベースの復元プロセスをスピードアップするには、SQL Server サービスアカウントを **BuiltIn\\Admin** ユーザーに変更します。 ユーザー アカウントについては、Microsoft Dynamics Lifecycle Services (LCS) の環境ページで確認できます。 復元プロセスでは、インスタント ファイルの初期化を使用できます。 詳細については、[データベース インスタント ファイルの初期化](/sql/relational-databases/databases/database-instant-file-initialization) を参照してください。

データベースを復元した後、次のサービスを停止します。

- Management Reporter 2012 処理サービス
- Microsoft Dynamics 365 Unified Operations: Batch 管理サービス
- Microsoft Dynamics 365 Unified Operations: データ インポート エクスポート フレームワーク サービス
- Microsoft Dynamics Lifecycle Services 診断サービス
- World Wide Web 公開サービス


次に、元の AXDB データベースを **AXDB_orig** に名前を変更します。 このデータベースは、後でコードを開発する際に参照する場合があります。
```sql
ALTER DATABASE AXDB SET SINGLE_USER WITH ROLLBACK IMMEDIATE
GO
ALTER DATABASE AXDB MODIFY NAME = AXDB_Orig
GO
ALTER DATABASE AXDB_Orig SET MULTI_USER
GO
```

最後に、新しく復元された AX 2012 データベース **AXDB** の名前を変更します。

### <a name="run-the-data-upgrade-deployable-package"></a>データ アップグレード展開可能なパッケージを実行 

最新の更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、LCS 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。

1. [LCS](https://lcs.dynamics.com/) にサインインします。
2. **共有資産ライブラリ** タイルを選択します。
3. **共有アセット** ライブラリの **アセット タイプの選択** で、**ソフトウェア配置可能パッケージ** を選択します。
4. すべてのデータ アップグレード パッケージは、**AX2012DataUpgrade** で開始されます。 一覧で、特定の Dynamics 365 バージョンに対応するデータ アップグレード パッケージを検索します。

    たとえば、バージョン 10.0.26 からアップグレードする場合、パッケージ名は **AX2012DataUpgrade-10.0.26** となります。

5. ダウンロードするデータ アップグレード パッケージを選択し、クラウドホスト環境で **C:\\Temp** フォルダーに保存 \ コピーします。
6. ダウンロードを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。
7. **解除** チェックボックスで **OK** を選び、ファイルを展開します。 
8. 管理者として PowerShell プロンプトを開き、配置可能なパッケージ フォルダーを変更します (例、**C:\\Temp\\AX2012DataUpgrade 10.0.26**)。
9. 次のスクリプトを使用して、配置可能パッケージを実行します。 スクリプト内の Runbook ID とファイル名を編集できます。

    ```PowerShell
    .\AXUpdateInstaller.exe generate -runbookid="MajorVersionDataUpgrade-runbook" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="MajorVersionDataUpgrade-runbook.xml"
    .\AXUpdateInstaller.exe import -runbookfile="MajorVersionDataUpgrade-runbook.xml"
    .\AXUpdateInstaller.exe execute -runbookid="MajorVersionDataUpgrade-runbook"
    ```

> [!NOTE]
> データのアップグレードには数時間かかる場合があります。

### <a name="monitoring-the-data-upgrade"></a>データ アップグレードの監視

配置可能パッケージには、アップグレード全体を処理する 1 つ のRunbook ステップがあります。 ただし、このステップはバックグラウンドで実行される次のサブステップで構成されます。

- **PreReq** – この手順は、SQL ディクショナリを構成し、システム シーケンスではなく SQL 順序を適用し、ユーザー情報とシステム変数を変更し、システム テーブルのデータベース同期を行い、新しいテーブルの機能を同期化します。
- **PreSync** – 最初のアップグレード ジョブ セットをバッチ処理によって呼び出す場合、主に固有インデックスを無効にします。
- **DBSync** – この手順では、最初の完全同期が実行されます。 PreSync ステップ中に無効となった固有のインデックスは、この手順で作成されません。
- **PostSync** – この手順では、メイン データ変換ジョブをバッチ処理経由で実行します。
- **FinalDBSync** – この手順では、データベースの残りの全オブジェクトを同期化する最終的なデータベース同期を行います。

アップグレード サービスの実行手順を決定するために、AXDB データベースで次の SQL クエリを実行できます。

```SQL
SELECT StartTime, EndTime, Steps, SubSteps, Status
FROM [DBUPGRADE].[DATAUPGRADESTATUS]
ORDER BY EndTime DESC
```

結果は次の例のようになります。 ここで指定された日時は、説明用のみに使用されます。 この時間は、データ量および AX 2012 年に使用されるモジュールによって異なります。

| StartTime | EndTime | ステップ | SubSteps | 状態 |
|---|---|---|---|---|
| 2022-05-20 17:16:07.097 | 2022-05-20 17:16:07.097 | FinalDbSync | DisableDataUpgradeFlag | 完了 |
| 2022-05-20 17:16:06.997 | 2022-05-20 17:16:06.997 | FinalDbSync | EnableDbLogTriggers | 完了 |
| 2022-05-20 17:16:06.937 | 2022-05-20 17:16:06.937 | FinalDbSync | DisableSafeMode | 完了 |
| 2022-05-20 16:48:49.390 | 2022-05-20 17:16:06.802 | FinalDbSync | SyncSchema | 完了 |
| 2022-05-20 16:48:49.333 | 2022-05-20 16:48:49.333 | FinalDbSync | EnableSafeMode | 完了 |
| 2022-05-20 16:47:30.860 | 2022-05-20 16:48:49.169 | PostSync | RestoreBatchConfiguration | 完了 |
| 2022-05-20 16:46:15.207 | 2022-05-20 16:47:30.738 | PostSync | EnableBatchPriorityScheduling | 完了 |
| 2022-05-20 16:44:43.403 | 2022-05-20 16:46:15.091 | PostSync | DisableSysDeletedObjects | 完了 |
| 2022-05-20 16:44:40.497 | 2022-05-20 16:44:40.497 | PostSync | ImportIsvLicenses | 完了 |
| 2022-05-20 16:44:09.190 | 2022-05-20 16:44:40.379 | PostSync | StopBatch | 完了 |
| 2022-05-20 15:49:38.207 | 2022-05-20 16:44:09.070 | PostSync | WaitForBatch | 完了 |
| 2022-05-20 15:49:37.517 | 2022-05-20 15:49:38.108 | PostSync | StartBatch | 完了 |
| 2022-05-20 15:48:31.517 | 2022-05-20 15:49:37.421 | PostSync | ScheduleScripts | 完了 |
| 2022-05-20 15:47:13.403 | 2022-05-20 15:48:31.431 | PostSync | StartAos | 完了 |
| 2022-05-20 15:47:12.667 | 2022-05-20 16:44:43.286 | PostSync | ExecuteScripts | 完了 |
| 2022-05-20 15:47:12.550 | 2022-05-20 15:47:12.550 | DbSync | DisableSafeMode | 完了 |
| 2022-05-20 07:49:40.827 | 2022-05-20 15:47:12.466 | DbSync | SyncSchema | 完了 |
| 2022-05-20 07:49:40.760 | 2022-05-20 15:31:05.716 | DbSync | EnableSafeMode | 完了 |
| 2022-05-20 07:49:06.673 | 2022-05-20 07:49:37.862 | PreSync | StopBatch | 完了 |
| 2022-05-20 07:46:59.667 | 2022-05-20 07:49:06.528 | PreSync | WaitForBatch | 完了 |
| 2022-05-20 07:46:58.637 | 2022-05-20 07:46:59.529 | PreSync | StartBatch | 完了 |
| 2022-05-20 07:46:31.317 | 2022-05-20 07:46:58.497 | PreSync | ScheduleScripts | 完了 |
| 2022-05-20 07:45:31.900 | 2022-05-20 07:46:31.180 | PreSync | StartAos | 完了 |
| 2022-05-20 07:45:31.780 | 2022-05-20 07:45:31.780 | PreSync | ConfigureBatch | 完了 |
| 2022-05-20 07:45:31.220 | 2022-05-20 07:49:40.519 | PreSync | ExecuteScripts | 完了 |
| 2022-05-20 07:44:18.410 | 2022-05-20 07:45:31.092 | PreSync | DisaleBatchPriorityScheduling | 完了 |
| 2022-05-20 07:43:14.880 | 2022-05-20 07:44:18.273 | PreSync | SaveBatchConfiguration | 完了 |
| 2022-05-20 07:42:05.350 | 2022-05-20 07:43:14.749 | PreSync | EnableSysDeletedObjects | 完了 |
| 2022-05-20 07:40:44.340 | 2022-05-20 07:42:05.211 | PreSync | CleanupDataUpgradeTables | 完了 |
| 2022-05-20 07:40:44.250 | 2022-05-20 07:40:44.250 | PreReqs | DisableSafeMode | 完了 |
| 2022-05-20 07:38:29.060 | 2022-05-20 07:40:44.110 | PreReqs | PartialDbSync | 完了 |
| 2022-05-20 06:30:01.693 | 2022-05-20 07:38:28.908 | PreReqs | AdditiveDbSync | 完了 |
| 2022-05-20 06:30:01.647 | 2022-05-20 06:30:01.647 | PreReqs | EnableSafeMode | 完了 |
| 2022-05-20 06:30:01.590 | 2022-05-20 06:30:01.590 | PreReqs | ClearSysLastValue | 完了 |
| 2022-05-20 06:30:01.523 | 2022-05-20 06:30:01.523 | PreReqs | ResetAdminUser | 完了 |
| 2022-05-20 06:30:01.477 | 2022-05-20 06:30:01.477 | PreReqs | PatchSqlSystemVariables | 完了 |
| 2022-05-20 06:30:01.273 | 2022-05-20 06:30:01.367 | PreReqs | PatchUserInfo | 完了 |
| 2022-05-20 06:30:00.930 | 2022-05-20 06:30:01.164 | PreReqs | PatchSqlDictionaryPass2 | 完了 |
| 2022-05-20 06:30:00.150 | 2022-05-20 06:30:00.820 | PreReqs | PatchSqlDictionaryPass1 | 完了 |
| 2022-05-20 06:30:00.043 | 2022-05-20 06:30:00.043 | PreReqs | UpdateKernelSchema | 完了 |
| 2022-05-20 06:28:01.157 | 2022-05-20 06:29:59.929 | PreReqs | CreateSqlSequences | 完了 |
| 2022-05-20 06:28:01.020 | 2022-05-20 06:28:01.020 | PreReqs | DisableDbLogTriggers | 完了 |

## <a name="troubleshooting-data-upgrade-errors"></a>データ アップグレードのエラーに関するトラブルシューティング

### <a name="rerun-the-runbook-after-a-failure"></a>失敗後、Runbook を再実行

データ アップグレードの Runbook が失敗した場合は、次の例に示すように、**-rerunstep** オプションを使用して最後のステップを再試行できます。 必要に応じてステップ番号を編集します。

```PowerShell
.\AXUpdateInstaller.exe execute -runbookid="MajorVersionDataUpgrade-runbook" -rerunstep=3
```

### <a name="review-the-runbook-logs"></a>Runbook ログを確認

ログは、配置可能パッケージの下のサブフォルダに格納されます。 現在の Runbook ステップのログを見つけるログ フォルダを表示し、エラーを確認します。

### <a name="view-details-about-a-presync-or-postsync-upgrade-job"></a>PreSync アップグレード ジョブまたは PostSync アップグレード ジョブに関する詳細の表示

アップグレード PreSync と PostSync スクリプトは、データ アップグレードのプロセスが開始しているバッチ プロセスを使い、X++ by で実行します。 Visual Studio のアプリケーション エクスプローラーでは、表示できる一部のクラスの前に **ReleaseUpdate** が付いています。 Runbook プロセス中にアップグレード スクリプトが失敗した場合、SQL Server Management Studio を開き、次のコードを実行して ReleaseUpdateScriptsErrorLog をクエリすることでエラーの原因をさらに確認できます。

```SQL
select * from RELEASEUPDATESCRIPTSERRORLOG
```

### <a name="additional-resources"></a>追加リソース

トラブルシューティングについては、次の記事を参照してください。

- [アップグレード中の開発環境のトラブルシューティング](troubleshoot-dev-env.md)
- [PreSync と PostSync アップグレード スクリプトのトラブルシューティング](pre-post-upgrade-scripts.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

