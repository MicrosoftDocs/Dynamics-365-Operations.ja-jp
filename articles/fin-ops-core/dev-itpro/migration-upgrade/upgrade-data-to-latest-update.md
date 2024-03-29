---
title: 開発環境またはデモ環境でデータをアップグレードする
description: この記事では、財務と運用アプリケーション リリースをアップグレードする方法について説明します。
author: laneswenka
ms.date: 11/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: fcf3a8fe246dc6d8bb6eb2e035262ed840267dc3
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124454"
---
# <a name="upgrade-data-in-development-or-demo-environments"></a>開発環境またはデモ環境でデータをアップグレードする

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> ここで説明されているプロセスは、財務と運用アプリの古いバージョンと最新バージョン間のデータ更新に対しては非推奨となりました。 Dynamic AX 2012 のアップグレードの詳細については、[AX 2012 から財務と運用へアップグレードする](upgrade-overview-2012.md)を参照してください。

この記事では、古いデータベースを最新の財務と運用アプリケーション リリースにアップグレードする方法について説明します。

記事では、レベル 1 環境の財務と運用データベースを最新の更新プログラムにアップグレードするプロセスについて説明します。 レベル 1 環境は、開発、1 ボックス、またはデモ環境とも呼ばれます。 

運用環境を含むレベル 2 以上の環境では、[最新バージョンへのセルフサービス アップグレード](self-service-upgrade.md) で説明されているセルフ サービスのアップグレード手順を実行します。

> [!IMPORTANT]
> - 財務と運用の最新の **プラットフォーム** を更新している場合、データベースをアップグレードする必要は **ありません**。 プラットフォーム更新プログラムには、下位互換性のあります。 この記事は、Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) から 財務と運用 8.0 へのアップグレードなど、財務と運用アプリケーションのリリース間でのアップグレードのプロセスに対してのみ適用されます。
> - このプロセスは、Microsoft Azure BLOB ストレージに保存されているドキュメント添付ファイルのアップグレードには適用されません。
> - アップグレードされたすべてのカスタム コードは、データ アップグレード プロセスを実行する前に環境に適用する必要があります。
> - バージョン 8.0 以降を使用している場合、アプリケーションのバージョンの間でデータのアップグレードは行われなくなりました。

## <a name="before-you-begin"></a>準備

1. 現在のデータベースをバックアップします。
1. 更新プログラムが既に正常に実行されている機能環境が必要です。
1. **ソース** 環境では、アップグレードする前のバージョンに応じて次の修正プログラムのいずれかをインストールする必要があります。 これらの修正プログラムは、SysSetupLog ロジックの問題を修正するため、アップグレード プロセスでアップグレード元のバージョンが検出されます。

   - **2016 年 11 月リリースからアップグレードする場合 (1611 または 7.1 とも呼ばれる、ビルド 7.1.1541.3036):** KB 4023686、"最新のアプリケーションリリースにアップグレードすると、'ソース システムのバージョン情報が見つかりませんでした' というエラーが表示されます。"
   - **2017 年 7 月リリース からアップグレードする場合 (7.2 とも呼ばれる、ビルド 7.2.11792.56024):** このバージョンに修正プログラムは必要ありません。
   - このステップで必要なアプリケーション修正プログラムをインストールした後は、完全なデータベース同期を実行します。 このステップは、ゴールデン データベース環境で特に重要です。 データベース全体の同期では、データベースをアップグレードするときに使用される SysSetupLog テーブルを設定します。 SysSetup インターフェイスはトリガーされないため、この手順で Microsoft Visual Studio からデータベース同期を実行しないでください。 SysSetup インターフェイスを起動するには、管理者の **コマンド プロンプト** ウィンドウで次のコマンドを実行します。

     ```Console
     cd J:\AosService\WebRoot\bin>

     Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "J:\AosService\PackagesLocalDirectory" -metadatadir        J:\AosService\PackagesLocalDirectory -sqluser axdeployuser -sqlserver localhost -sqldatabase axdb -setupmode sync -syncmode fullall -isazuresql false -sqlpwd \<password for axdeployuser\>
     ```

1. Dynamics 365 Finance バージョン 10.0.9 または 10.0.10 にアップグレードする場合、データのアップグレードを実行する前に、品質更新プログラムを移行先の環境にインストールします。
1. 標準デモ データのデータベースとして開始されるデータベースをアップグレードする場合も、次のスクリプトも実行する必要があります。 このステップは、デモ データにカーネル X++ クラスの不適切なレコードが含まれているため必要です。

    ```sql
    delete from classidtable where id >= 0xf000 and id <= 0xffff
    ```

1. Commerce Data Exchange (CDX) のすべてのジョブが正常に実行され、チャネル データベースのクラウド バージョンで同期されていないトランザクション データがないことを確認してください。

## <a name="select-the-correct-data-upgrade-deployable-package"></a>適切なデータ アップグレード展開可能なパッケージを選択

最新の更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード配置可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共有アセット ライブラリからダウンロードします。
1. [LCS](https://lcs.dynamics.com/) にサインインします。
2. **共有資産** ライブラリ タイルを選択します。
3. 共有アセット ライブラリの **アセット タイプの選択** で、**ソフトウェア配置可能パッケージ** を選択します。
4. 配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。

    - AX 2012 をアップグレードする場合、パッケージ名は **AX2012DataUpgrade** から始まります。 アップグレードするリリースに対応するパッケージを選択します。 たとえば、**AX2012DataUpgrade-10-0**。
    - 以前のリリースから最新の 10.0.X リリースにアップグレードする場合、パッケージ名は **DataUpgrade-10-0** です。 
    - 以前のリリースからプレビュー リリースにアップグレードする場合は、パッケージ名に PREVIEW が含まれます。 たとえば、**DataUpgrade-10-0-2-PREVIEW** です。
5. アップグレードする先のリリースに対応するパッケージを選択します。 

## <a name="upgrade-the-database"></a>データベースのアップグレード

1. 配置可能なデータ アップグレード パッケージを、**c:\\Temp** または任意の場所に展開します。
   > [!NOTE] 
   > これが LCS に接続されている開発環境であり LCS から直接データ アップグレード プロセスを実行する予定がある場合は、この手順を省略します。

2. アップグレード対象の最新の更新プログラムが既に実行されているデモ環境または開発環境に、ソース データベース (アップグレードするデータベース) のバックアップをインポートまたは復元します。 既存のデータベースをそのままにして、新しいデータベースに **imported\_new** という名前を付けます。

    > [!NOTE]
    > 以前のリリースで実行されている運用データベースのデータのアップグレードを検査する場合: 運用環境からデモまたは開発環境にデータベースをコピーするには [標準ユーザー受け入れテスト (UAT) データベースのコピーのエクスポート](../database/dbmovement-scenario-exportuat.md) の手順に従ってください。   
    > 
    > Azure 仮想マシン (VM) 間でアップロード/ダウンロードの速度を向上するには、AzCopy を使用することをお勧めします。 AzCopy をダウンロードする方法、およびそれを使用して Azure blob ストアにコピーまたは Azure blob ストアからコピーする方法については、[AzCopy Command-Line Utility でデータを転送する](/azure/storage/common/storage-use-azcopy-v10) を参照してください。

3. 接尾語 **\_orig** を追加することによって、元のデータベースの名前を変更します。 元のデータベースと同じ名前になるように、新しく復元したデータベースの名前を変更します。 この方法で、2 つのデータベースが場所を切り替えます。

    ```sql
    ALTER DATABASE <original Dynamics 365 database> MODIFY NAME = <original Dynamics 365 database>_ORIG
    ALTER DATABASE imported_new MODIFY NAME = <original Dynamics 365 database>
    ```

4. 元のデータベースに戻す必要がある場合に備えて、ソース データベースのバックアップを作成します。 次のステップでソース データベースを変更するためこのステップは重要です。

5. **c:\\Temp\\DataUpgrade** フォルダー (展開可能なパッケージを以前に展開した場所) からデータ アップグレード パッケージを実行します。 データ アップグレード パッケージの実行は、ソフトウェア展開可能パッケージのインストールと同様です。 詳細な指示については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md#generate-a-runbook-from-the-topology)を参照してください。 **トポロジから Runbook を生成します** というセクションで開始し、**配置可能パッケージのインストール** セクションの手順を実行します。 

> [!NOTE]
> 開発環境上のデータベースをアップグレードする場合は、代わりに **管理 > 適用更新** サービス機能を使用して、LCS 環境ページから直接データ アップグレード パッケージを実行できます。 これは、ユーザーが開発用 VM のローカル管理者である必要はありません。 これは LCS の[2 月](https://blogs.msdn.microsoft.com/lcs/2018/02/13/lcs-february-2018-release-1-release-notes/)リリースから利用可能です。 
>
> これにより、財務と運用のデータベース、チャネルのデータベースが更新され、財務報告データベースがリセットされます。

## <a name="re-enable-sql-change-tracking"></a>SQL 変更履歴の再有効化

データベース レベルで変更追跡が有効であるかどうかを確認するため、アップグレードされたデータベースに対して次の SQL を実行します。 お使いのデータベースの、**データベースの変更** コマンド名を指定する必要があります。

```sql
ALTER DATABASE [<your AX database name>] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON)
```

## <a name="refresh-the-data-entities-list"></a>データ エンティティの一覧を更新

プラットフォーム更新プログラム 14 またはそれ以降にアップグレードした場合は、データ管理ワークスペース のデータ エンティティ リスト (**データ管理** > **フレームワーク パラメーター** > **エンティティ設定** > **エンティティ リストを更新**) を更新し、エンティティ リストが最新のプラットフォームで再構築され、必要なメタデータがデータ管理操作に使用できることを確認す必要があります。 

## <a name="troubleshoot-upgrade-script-errors"></a>アップグレード スクリプト エラーのトラブルシューティング

このセクションでは、さまざまな問題のトラブルシューティングに役立つ情報を提供します。

### <a name="rerun-the-runbook-after-a-data-upgrade-script-failure"></a>データ アップグレード スクリプトの失敗後、runbook を再実行

デプロイ可能なデータ アップグレード パッケージでは、標準的なデプロイ可能なパッケージよりも細かい粒度で Runbook を再実行できます。 データ アップグレード スクリプトは、Runbook のステップ 5 で実行されます。 手順 5 で障害が発生した場合は、コマンド ウィンドウで出力を表示し、どのサブステップに到達したかが分かります。 たとえば、サブステップ 5.3 に達した場合、そのサブステップから返す次のコマンドを使用します。

```Console
AXUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=5.3
```

デバッグしているときは、データアップグレード部分全体とデータベースの同期を再実行する必要はありません。 失敗したスクリプトだけを再実行し続けることができます。

### <a name="view-more-details-about-a-script-error"></a>スクリプト エラーに関するより詳細を表示します。

runbook インストーラが起動するバッチ プロセスを使用して、X++ でアップグレード スクリプトを実行します。 Visual Studio のアプリケーション エクスプローラーでは、表示できる一部のクラスの前に **ReleaseUpdate** が付いています。 runbook プロセス中にアップグレード スクリプトが失敗した場合、Microsoft SQL Server Management Studio を開き、次のコードを実行して ReleaseUpdateScriptsErrorLog を照会することでエラーの原因をさらに確認できます。

```sql
select \* from RELEASEUPDATESCRIPTSERRORLOG
```

このコードを Visual Studio 内の新しい実行可能なクラスに追加して、その動作を直接観察、デバッグ、および再作業することができます。

### <a name="skip-failed-scripts"></a>失敗したスクリプトをスキップ

> [!IMPORTANT]
> このプロセスは、開発シナリオでのみ使用することを目的としています。

指定回数失敗したすべてのスクリプトをスキップして、次の実行可能なスクリプトに移動することができます。 この機能は、トラブルシューティング プロセスに役立ちます。 意図的に、プロセスは手動であるため、誤ってスクリプトをスキップする可能性は低くなります。

ReleaseUpdateConfiguration のテーブルに、**ScriptRetryCount** という新しいフィールドがあります。 このフィールドの値は、runbook プロセスがスクリプトを無視する前にスクリプトを再実行する回数を制御します。 Runbook が実行されると、システムは、特定のスクリプトが失敗するたびに **ReleaseUpdateScriptsErrorLog.ErrorCount** フィールドを更新します。 各スクリプトの新しい行が作成されます。

DataUpgrade パッケージ フォルダーの ..\\AosServices\\Scripts\\ に、IgnoreBlockingScripts.ps1 というスクリプトがあります。 管理者 Windows PowerShell ウィンドウからこのスクリプトを実行し、**ScriptRetryCount**=**ErrorCount** となっているすべてのスクリプトをスキップします。 次に、スクリプトが無視されるように、失敗した Runbook ステップを再実行します。 **ReleaseUpdateScriptsErrorLog.Ignored** フィールドは、スキップされる各スクリプトにも設定されます。 そのため、後でスキップされたスクリプトを簡単に識別できます。

### <a name="monitor-the-duration-of-scripts-that-are-run"></a>実行されるスクリプトの存続期間の監視

正常に実行されたすべてのスクリプトでは、**ReleaseUpdateScriptsLog.DurationMins** 列で取得した分数を記録します したがって、データ アップグレード プロセスのパフォーマンスを調整しようとしているときに、最も実行時間が長いスクリプトを簡単に識別できます。 期間は各スクリプトが実行にかかる時間であることに注意してください。 ただし、複数のスクリプトが並列実行されるため、**DurationMins** 列の値の合計は、アップグレード プロセスの全体的な期間を超えます。

## <a name="known-issues"></a>既知の問題
### <a name="a-duplicate-key-was-found-for-the-object-that-is-named-dboresourcesetup"></a>dbo.RESOURCESETUP という名前のオブジェクトのキーの重複が見つかりました。

データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。

> データベースの実行に失敗しました: オブジェクト名「dbo.RESOURCESETUP」およびインデックス名「I\_6716AK」の重複キーが検出されたため、CREATE UNIQUE INDEX ステートメントが終了しました。

この問題は、今後の修正プログラムで解決される既知の問題です。 この問題を回避するには、Management Studio からデータベースに対して次の SQL スクリプトを実行し、テーブルから重複した列を削除します。

```sql
delete RS from ResourceSetup as RS
join ResResourceIdentifier as RRI on RRI.RecId = RS.Resource_
join WrkCtrTable as WCT on WCT.RecId = RRI.RefRecId
join DirPartyTable as DPT on DPT.DataArea = WCT.DataAreaId
where DPT.DataArea != '' and RS.LegalEntity != DPT.RecId
```

### <a name="a-record-cant-be-selected-in-dimension-hierarchy-nodes-camdatadimensionhierarchynode"></a>レコードは、分析コード階層ノード (CAMDataDimensionHierarchyNode) で選択することはできません。

データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。

> 分析コード階層ノード (CAMDataDimensionHierarchyNode) でレコードを選択することはできません。 分析コード階層: 0。 SQL データベースによってエラーが出されました。 オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[ODBC Driver 13 for SQL Server\]\[SQL Server\] 無効な列名「RELATIONTYPE」です。 

この問題は、将来のリリースで解決される既知の問題です。 この問題を回避するには、Management Studio からデータベースに対して次の SQL スクリプトを実行し、いくつかのテーブルに欠落したフィールドを作成します。

```sql
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
DROP PROCEDURE IF EXISTS [DBO].PATCHRELATIONTYPE
GO 

CREATE PROCEDURE [DBO].PATCHRELATIONTYPE
        @TABLENAME SYSNAME
    AS
    BEGIN
        DECLARE @TABLEID        INT ;
        DECLARE @FIELDID        INT ;
        DECLARE @FIELDNAME      SYSNAME;
        DECLARE @SQLTATEMENT NVARCHAR(1024);
        DECLARE @TOTALRECORDS   INT;
        DECLARE @ParmDefinition         NVARCHAR(150);

        SET NOCOUNT ON;

        SELECT @FIELDNAME = 'RELATIONTYPE';
        SELECT @FIELDID = 61453; --Hardcoded in code DBFIELD_DISCRIMINATOR
        IF OBJECT_ID(@TABLENAME, 'U') IS NULL 
        BEGIN
            PRINT @TABLENAME + ' table does not exists. Please provide a base table';
            RETURN;
        END

        IF EXISTS(SELECT 1 FROM SYS.COLUMNS
            WHERE NAME = @FIELDNAME
            AND OBJECT_ID = OBJECT_ID(@TABLENAME))
        BEGIN
            PRINT @TABLENAME + ' table contains RelationType. No patching needed.';
            RETURN;
        END
        PRINT @TABLENAME + ' table does not contain RelationType.';
        SELECT @TABLEID = ID FROM TABLEIDTABLE WHERE NAME = @TABLENAME;
        IF @@ROWCOUNT <> 1
        BEGIN
            PRINT @TABLENAME + ' was not present in TABLEIDTABLE. Cannot proceed!!';
            RETURN;
        END 

        -- Ensure that instancerelationtype is added. We don't want to randomly add relationtype to any table.
        IF NOT EXISTS (SELECT \* FROM SQLDICTIONARY WHERE TABLEID = @TABLEID AND NAME = 'InstanceRelationType')     
        BEGIN
            PRINT @TABLENAME + ' table does not exist. Please provide a base table';
            RETURN;
        END

        -- Ensure SQLDictionary is populated
        IF NOT EXISTS (SELECT \* FROM SQLDICTIONARY WHERE TABLEID = @TABLEID AND FIELDID = @FIELDID)
        BEGIN
            INSERT INTO SQLDICTIONARY (TABLEID, FIELDID, ARRAY, NAME, SQLNAME, FIELDTYPE, STRSIZE, SHADOW, RIGHTJUSTIFY, NULLABLE, FLAGS, RECVERSION)
            VALUES (@TABLEID,@FIELDID,1, @FIELDNAME, @FIELDNAME, 49, 0, 0, 0, 0, 0, 1);
            PRINT 'Inserted into SqlDictionary';
        END

        -- Actual alter statement
        SELECT @SQLTATEMENT = 'ALTER TABLE ' + @TABLENAME +  ' ADD ' + @FIELDNAME + ' BIGINT NOT NULL DEFAULT 0';
        PRINT 'Issuing ' + @SQLTATEMENT;
        EXEC (@SQLTATEMENT);

        SELECT @SQLTATEMENT = 'UPDATE ' + @TABLENAME +  ' SET RELATIONTYPE = 0';
        PRINT 'Issuing ' + @SQLTATEMENT;
        EXEC (@SQLTATEMENT);
    END;
GO
exec PatchRelationType  'CAMDATADIMENSIONHIERARCHYNODE'
exec PatchRelationType  'CAMDataJournal'
exec PatchRelationType  'CAMDataCostAccountingLedgerSourceEntryProvider'
exec PatchRelationType  'CAMDataImportedDimensionMember'
```

### <a name="an-index-cant-be-created-on-inventdistinctproduct"></a>InventDistinctProduct にインデックスを作成することはできません

データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。

> InventDistinctProduct 索引を作成できません。製品列に重複キーが存在します。

この問題は、将来のリリースで解決される既知の問題です。 この問題を回避するには、InventDistinctProduct テーブルのすべてのレコードを削除してから、現在のステップから Runbook を再開します。 InventDistinctProduct テーブル内のレコードは破棄できます。 財務と運用が初めて開始されたとき、項目が登録されたとき、または MRP が実行されたときに再生成されます。 InventDistinctProduct のすべてのレコードを削除するには、Management Studio から現在のデータベースに対して次のクエリを実行します。

```sql
truncate table InventDistinctProduct
```

現在のステップから runbook を再開するには、次のコマンドを実行します。

```Console
axupdateinstaller execute -runbookid=<your runbook name> -rerunstep=<the last step number>
```

たとえば、このコマンドを使用できます。

```Console
axupdateinstaller execute -runbookid=dataupgrade -rerunstep=5.4
```

### <a name="an-exchange-rate-cant-be-found-when-demo-data-is-upgraded"></a>デモ データがアップグレードされている場合為替レートは見つかりません

デモ データベースをアップグレードするとき、データ アップグレード パッケージを配置するときに、次のエラー メッセージが表示される場合があります。

> 交換日 2014 年 12 月 1 日時点の通貨 INR と BRL 間の為替レート タイプ既定に対する為替レートが見つかりません。

デモ データをアップグレードするため、経費明細行がある TrvUnreconciledExpenseTransaction テーブルを確認します。 通貨を **USD** に変更します。 (データはデモ データなので、この経費行を保存するのに注意する必要はありません。)

```sql
update TrvUnreconciledExpenseTransaction
set transactioncurrencycode = 'USD'
where transactioncurrencycode = 'INR'
```

または、データが元の環境 (旧バージョンなど) から元の環境に移動し、失われた為替レートを **総勘定元帳** &gt; **通貨** &gt; **通貨の為替レート** に追加します。 2014 をカバーするインド ルピー (INR) およびブラジル レアル (BRL) のレコードを追加する必要があります。 次に、そのデータベースを新しい環境に持ち込み、そのデータベースに対してアップグレードを開始します。

### <a name="the-interpreter-evaluation-stack-has-grown-during-a-call-to-the-kernel"></a>インタプリター評価スタックは、カーネルの呼び出し中に増加しました

UserInfom などのカーネル テーブルでデータベース ログを有効にした場合、次のエラー メッセージが表示される可能性があります。

> 実行ステップ: 5.1  
> データ アップグレードの必要条件  
> データ アップグレードの必要条件  
> 未処理の例外の詳細情報: インタープリター評価スタックは、カーネル メソッド xRecord::Delete ()、height before call: 0、height after call: 3 の呼び出し中に増加しました。 未処理の例外の詳細情報: KernelInstance: カーネルが削除されたメモリにアクセスしています  
> 失敗したステップ

この問題を解決するには、**システム管理**&gt;**設定**&gt;**データベース ログ設定** でデータベース ログの設定を確認してください。 必要に応じてカーネル テーブルのレコードを削除します。

### <a name="the-batch-process-fails-to-start"></a>バッチ処理を開始できません

コンフィギュレーション キーが変更された後に環境が[メンテナンス モード](../sysadmin/maintenance-mode.md)のままになっていると、バッチ処理が失敗することがあります。 この問題を解決するには、メンテナンス モードをオフにしてから、runbook プロセスを再開します。

### <a name="the-system-fails-to-locate-or-generate-a-user-guid"></a>システムは検索したりユーザー GUID を生成したりできません。

次のエラー メッセージが表示される場合があります。

> …ハンドルされない例外の追加情報: システムはユーザー GUIDの検索または生成に失敗しました…

この問題を解決するのには、失敗した runbook ステップを再実行します。 次に、継続することができます。

### <a name="pre-sync-or-post-sync-errors-on-releaseupdatedb71_ledgerperiodclose"></a>ReleaseUpdateDB71\_LedgerPeriodClose で事前同期または事後同期エラー

**ReleaseUpdateDB71\_LedgerPeriodClose** クラスの **preSyncLedgerPeriodCloseTemplateTask**、**updateMenuItemTypeForCurrencyReval**、または **updateLedgerPeriodCloseTemplateTask** メソッドでは、次のエラー メッセージの 1 つを受け取る可能性があります。

> 必要なデータベース操作を実行できません。 SQL データベースによってエラーが出されました。 オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「TEMPLATE」です。 INSERT INTO LedgerPeriodCloseTemplateTaskTmp (TEMPLATE、AREA, NAME、MENUITEM、MENUITEMTYPE、 TARGETDAYSFROMPROJECTCOMPLETE、DUETIME、LEGALENTITYSELECTION、RECVERSION、PARTITION、RECID、CLOSINGROLE、LINENUM) SELECT T1.TEMPLATE、T1.AREA、T1.NAME、T1.MENUITEM、T1.MENUITEMTYPE、T1.TARGETDAYSFROMPROJECTCOMPLETE、T1.DUETIME、 T1.LEGALENTITYSELECTION、T1.RECVERSION、T1.PARTITIONT1.RECID、T1.CLOSINGROLE、0 FROM LedgerPeriodCloseTemplateTask T1 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: Cannot execute the required database operation。 SQL データベースによってエラーが出されました。
> 
> 必要なデータベース操作を実行できません。 SQL データベースによってエラーが出されました。 オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「MENUITEMTYPE」です。 UPDATE LedgerPeriodCloseTemplateTaskTmp SET MENUITEMTYPE = 0 WHERE MENUITEMTYPE = 2 AND MENUITEM = 'LedgerExchAdj' AND PARTITION = 5637144576 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: 必要なデータベース操作を実行できません。 SQL データベースによってエラーが出されました。
> 
> 必要なデータベース操作を実行できません。 SQL データベースによってエラーが出されました。 オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「TEMPLATE」です。 INSERT INTO LedgerPeriodCloseTemplateTask (TEMPLATE、AREA、NAME、MENUITEM、MENUITEMTYPE、TARGETDAYSFROMPROJECTCOMPLETE、DUETIME、LEGALENTITYSELECTION、RECVERSION、PARTITION、RECID、CLOSINGROLE、LINENUM) SELECT T1.TEMPLATE、T1.AREA、T1.NAME、 T1.MENUITEM、T1.MENUITEMTYPE、T1.TARGETDAYSFROMPROJECTCOMPLETE、T1.DUETIME、T1.LEGALENTITYSELECTION、T1.RECVERSION、 T1.PARTITION、T1.RECID、T1.CLOSINGROLE、T1.LINENUM FROM LedgerPeriodCloseTemplateTaskTmp T1 session 1013 (Admin)

この問題を解決するには、Management Studio を使用して、データベースから LedgerPeriodCloseTemplateTaskTmp テーブルを手動でドロップします。 Runbook ステップを返します。 この問題は、将来の修正プログラムで修正されます。

### <a name="table-sync-failed-for-table-warrantygroupconfigurationitem"></a>テーブルでのテーブル同期に失敗しました: WarrantyGroupConfigurationItem

Dynamics 365 Finance バージョン 10.0.9 または 10.0.10 にアップグレードする場合、データのアップグレード中に次のエラー メッセージが表示されることがあります。

> テーブルでのテーブル同期に失敗しました: WarrantyGroupConfigurationItem

この問題を解決するには、データベースのアップグレードをロールバックし、移行先環境で品質更新プログラムをインストールしてから、データのアップグレードを再実行します。 

### <a name="kb-number-3170386"></a>KB 番号 3170386

KB 番号 3170386 がインストールされていない場合、次のエラー メッセージが表示されます。

> サービス モデルの GlobalUpdate スクリプト: マシンでの AOSService …. その他 …. UpgradeServiceHelper::WaitForDataUpgradeToComplete(Object\[\]… 失敗したステップ

このエラーは、データ アップグレードの事前同期または事後同期のサブステップに障害が起こったために発生します。 どのサブステップが失敗したかおよび失敗の詳細を特定するには、これらの手順に従います。

> [!NOTE]
> 事前同期または事後同期サブステップが手動で完了するまで障害が発生した Runbook ステップを再度実行することはできず、AutoDataUpgrade.config ファイルが更新されて、既に実行されているサブステップをスキップします。

1. ファイル エクスプローラーの **DataUpgradeAosServiceScripts** フォルダーで、ファイルが最後に変更された日付を降順に並べ替えてから、どの手順が失敗したかを特定するためにリストの上部にあるファイルを確認します。

    - 一番上のファイルの名前が **dbUpgrade *PreSync* Monitor.error.log** と付けられている場合は、同期前サブステップが失敗します。
    - 一番上のファイルの名前が **dbUpgrade *PostSync* Monitor.error.log** と付けられている場合は、同期後サブステップが失敗します。

2. Management Studio で、次の **SELECT** ステートメントを実行します。

    ```sql
    SELECT * FROM RELEASEUPDATELOG
    ```

    結果セットの最後から 2 番目のレコードには、すべての失敗のエラーとコール スタックがあります。

### <a name="dmf-errors"></a>DMF エラー

次のデータ移行フレームワーク (DMF) エラーのいずれかの方法が表示される場合は、修正プログラム サポート技術情報番号 3170386 をダウンロードし、アップグレード プロセスを再開します。

#### <a name="dmf-pre-sync-error"></a>DMF 事後同期エラー

> バッチ エラー: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPreSync (バッチ: AOS-F01B9F0CCC8、 9、情報、エラー、):\[\[1\]\[3、必要なデータベース操作を実行できません。 SQL データベースがエラーを発行しました。\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]'GO' 付近に正しくない構文があります。\]\[3,

#### <a name="dmf-post-sync-error"></a>DMF 事後同期エラー

> バッチ エラー: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPostSync(バッチ: AOS-F01B9F0CCC8、 9、情報、エラー、):\[\[1\]\[3、必要なデータベース操作を実行できません。 SQL データベースがエラーを発行しました。\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]'GO' 付近に正しくない構文があります。\]\[3,

## <a name="encrypted-fields-in-demo-data"></a>デモ データの暗号化されたフィールド

アップグレード後、データベースの暗号化されたフィールドの値は読み取れません。 ただし、アップグレード後にこれらのフィールドに入力される新しい値は読み取り可能になります。 この動作は、データ暗号化に使用される証明書に関連する技術的な制限のために発生します。 次のテーブルに、影響を受けるフィールドを示します。

| Table.Field                                                      | デモ データにデータが存在します |
|------------------------------------------------------------------|--------------------------|
| CreditCardAccountSetup.SecureMerchantProperties                  | 有                      |
| ExchangeRateProviderConfigurationDetails.Value                   | 有                      |
| RetailChannelPaymentConnectorLine.SecureMerchantProperties       | 有                      |
| RetailConnDatabaseProfile.ConnectionString                       | 有                      |
| RetailHardwareProfile.SecureMerchantProperties                   | 有                      |
| RetailHardwareProfileMerchantInfoEntity.SecureMerchantProperties | 有                      |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                         | 無                       |
| FiscalEstablishmentEntity.CSC                                    | 無                       |
| FiscalEstablishmentStaging.CSC                                   | 無                       |
| HcmPersonIdentificationNumber.PersonIdentificationNumber         | 無                       |
| HcmWorkerActionHire.PersonIdentificationNumber                   | 無                       |
| SysEmailSMPTPassword.Password                                    | 無                       |
| SysOAuthUserTokens.EncryptedAccessToken                          | 無                       |
| SysOAuthUserTokens.EncryptedRefreshToken                         | 無                       |

## <a name="additional-resources"></a>追加リソース

[財務と運用の最新更新プログラムへの移行の処理](/dynamics365/unified-operations/dev-itpro/migration-upgrade/upgrade-latest-update)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

