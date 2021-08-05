---
title: 財務報告のデータ マートのリセット
description: このトピックでは、Microsoft Dynamics 365 Finance の財務報告データ マートをリセットする方法について説明します。
author: aprilolson
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: IT Pro, Developer
ms.reviewer: kfend
ms.custom: 261824
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e71a47620df36fa9c1d1dc250dcd4bad4d77195e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350120"
---
# <a name="reset-the-financial-reporting-data-mart"></a>財務報告のデータ マートのリセット

[!include [banner](../includes/banner.md)]

このトピックでは、 Microsoft Dynamics 365 Finance での Financial Reporting のリセット方法を説明します。 データマートは、ユーザーの役割 と クライアント や インフラストラクチャー へのアクセス権に応じて、複数の方法でリセットすることができます。

データマートのリセットは、データベース で あまり処理が行われていないときだけに留めるようにしてください。 財務諸表は、リセット プロセス中は使用できません。

> [!NOTE]
> データ マートのリセットが必要なことを確認するには、[データ マートをリセットする場合](when-to-reset-data-mart.md) を参照してください。

> データマートのリセットは、レポートの構造を定義しているレポートの定義には影響しません。 しかし、レポートのエクスポートを実行してバックアップを取っておくことをお勧めします。 レポート定義をエクスポートする手順は、このトピックの後半にあるレポート定義のエクスポートとインポートという名前のセクションの最後に記載されています。

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>レポート デザイナーからの財務報告のデータ マートのリセット

レポート デザイナーのバージョンを検索するには、次のビデオをご覧ください: [レポート デザイナーのバージョンを検索する方法](https://www.youtube.com/watch?v=icfA5Q3kp4w)

レポート デザイナーでデータマートをリセットするには、 以下の図に示されているように、 **ツール** メニューで **データマートのリセット** を選択します。 表示されるダイアログ ボックスには2つのセクションがあります: **統計** および **リセット**。

[![データ マートのダイアログ ボックスをリセットします。](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>統合試行回数

**統合試行回数** グリッドは、システムがトランザクションの統合を試みた回数を表示します。 システムは、最初のいくつかの試行ができなかった場合は、日の期間にわたってデータを統合するまで続行されます。 試行回数が8回以上の場合、および分析コードの組み合わせやトランザクション レコードが多い場合、データ マートをリセットする必要があります。 このような状況では、データはレポートされません。

##### <a name="data-status"></a>データのステータス

**データのステータス** グリッドは、データ マート内のトランザクション、為替レート、および分析コード値のスナップショットを表示します。 古いレコードが多数ある場合、レコードに対して更新が数多く存在することになります。 この場合は、レポートの生成に要する時間が長くなることがあります。

##### <a name="misaligned-main-account-categories"></a>正しく整合されていない主勘定カテゴリ

財務報告 7.2.1 以前のリリースを使用している場合で、勘定の名前を変更して勘定カテゴリの間で勘定を移動する場合、データ マートをリセットする必要がある場合があります。 これらのアクションにより、主勘定カテゴリが正しく整合されなくなることがあります。 **正しく整合されていない主勘定カテゴリ** フィールドには問題が発生しているかどうかが表示されます。

### <a name="reset-the-data-mart-and-select-a-reason"></a>データマートをリセットし、理由をひとつ選択してください

データ マートのリセットが必要であると判断した場合は、**データ マートのリセット** チェック ボックスを選択し、**理由** フィールドで理由を選択します。  次のオプションを使用できます。

- **データが不足しているか、正しくありません** – 統計に基づき、決定したデータが存在しない可能性があります。 続行する前に、根本原因を判断するためにサポートを使用することをお勧めします。
- **データベースの復元** – データベースが復元されましたが、財務報告のデータ マートのデータベースは復元されませんでした。
- **その他** – 別の理由によりデータ マートをリセットしています。 問題があることを懸念する場合は、識別のためにサポートに問い合わせてください。

[![データ マートをリセットします。](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> リセットを開始する前に、すべてのデータ マート リセット タスクが初回の読み込みを完了したことを確認します。 **ツール** &gt; **統合の状態** を選択して、前回のランタイム列で値を探すことにより、これを確定できます。

#### <a name="clear-users-and-companies"></a>ユーザーと会社をクリア

データベースの復元後にユーザーまたは会社を変更した場合は、 **ユーザーと企業の削除** チェックボックスを選択します。 このチェックボックスをオンにすることはほとんどありません。

リセット プロセスを開始する準備ができたら、**OK** を選択します。 プロセスを開始する準備ができていることを確認するように求められます。 財務諸表は、リセット中およびその後に発生する最初のデータ統合中には使用できないことに注意してください。

統合の状態を確認する場合は、**ツール** &gt; **統合の状態** を選択し、統合が最後に実行された時刻と状態を表示します。

[![統合のステータスを表示します。](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> すべてのマッピングの状態が **RanToCompletion** と表示され、 **統合の状態** ダイアログボックスの左下隅に「統合が完了しました」というメッセージが表示されたら、リセットは完了です。

## <a name="reset-the-financial-reporting-data-mart-through-windows-powershell"></a>Windows PowerShell を介して Financial Reporting の データマートをリセットする

データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このセクションのステップに従って、財務報告のデータ マートが復元したデータベースを正しく使用していることを保証する必要があります。

### <a name="stop-services"></a>サービスの停止

次の Microsoft Windows サービスでは、Finance and Operations データベースへの接続が提供されます。 したがって、Microsoft Remote Desktop を使用して環境内のすべてのコンピュータに接続し、services.msc を使用してこれらのサービスを停止する必要があります。

- ワールド ワイド Web パブリッシング サービス (すべての アプリケーション オブジェクト サーバー (AOS) \[AOS\] の コンピューター)
- バッチ管理サービス (非プライベート AOS コンピューター上のみ)
- Management Reporter 2012 プロセス サービス (ビジネス インテリジェンス \[BI\] の コンピューター のみ)

### <a name="reset"></a>リセット

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>最新の MinorVersionDataUpgrade.zip パッケージをダウンロードする

最新の MinorVersionDataUpgrade.zip パッケージをダウンロードします。 データ更新パッケージの正しいバージョンを検索およびダウンロードする方法については、開発、デモ、またはサンド ボックス環境でデータを更新するトピックの [開発環境またはデモ環境でデータを更新する](../migration-upgrade/upgrade-data-to-latest-update.md#select-the-correct-data-upgrade-deployable-package) を参照してください。

MinorVersionDataUpgrade.zip パッケージをダウンロードするためにアップグレードは必要ありません。 そのため、当該トピックの 「最新のデータ アップグレード 展開可が能なパッケージをダウンロードする」 セクションの手順に従う必要があります。 トピックのその他のすべての手順をスキップできます。

#### <a name="run-prerequisite-sql-scripts-against-the-database"></a>データベースに対して 前提となる SQL スクリプトを実行する

財務報告データベースに対してではなく、データベースに対して、次のスクリプトを実行します:

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAxViewChangeTracking.sql

これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを保証する助けになります。

#### <a name="run-a-windows-powershell-script-to-reset-the-database"></a>Windows PowerShell スクリプトを実行してデータベースのリセットをする

AOS コンピュータで、管理者として Microsoft Windows PowerShell を開始し、アプリケーションと財務報告との統合をリセットするために次のコマンドを実行します。

```powershell
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>" -SkipMRTableReset
```

> [!NOTE]
> - SkipMRTableReset を使用している場合は、ツリーユニットのセキュリティが維持されます。
> - SkipMRTableReset に一致するパラメーターが見つからないエラーが発生する場合は、パラメーターを削除して、もう一度行うことができます (以降のバージョンは、このスイッチを含めるための既定の動作更新が完了)。

ここでは **Reset-DatamartIntegration** コマンドのパラメータについて説明します:

- **-Reason** の有効な値は、**SERVICING**、**BADDATA**、および **OTHER** です。
- **-ReasonDetail** パラメーターは自由書式です。
- 理由と理由の詳細はテレメトリーまたは環境モニタリングに記録されます。

> [!NOTE]
> コマンドを実行した後、データベースをリセットすることを確認するために **Y** を入力するように求められます。

#### <a name="restart-services"></a>サービスをリセット

services.msc を使用して、以前に停止したサービスを再起動します。

- ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
- バッチ管理サービス (非プライベート AOS コンピューター上のみ)
- Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

## <a name="reset-the-financial-reporting-data-mart-for-dynamics-365-finance--operations-on-premises-through-sql-server-management-studio"></a>SQL Server Management Studio を介して、 Dynamics 365 Finance と Operations (on-premises) の Financial Reporting データマート をリセットする

作業を開始する前に、すべてのユーザーがレポート デザイナーを閉じて、財務報告エリアを終了していることを確認してください。

1. MRDB とも呼ばれる SQL Server 内の ManagementReporter という名前の財務報告に使用されるデータベースで、次のスクリプトを実行します。 2020 年 4 月 9 日更新: Reset Datamart Begin.txt

    ```sql
    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------
    --setup for servicing mode

    BEGIN TRANSACTION
    IF NOT EXISTS(SELECT SCHEMA_NAME FROM INFORMATION_SCHEMA.SCHEMATA WHERE SCHEMA_NAME = 'Servicing')
    BEGIN 
        EXEC ('CREATE SCHEMA Servicing') 
    END

    IF (DATABASE_PRINCIPAL_ID('GeneralUser') IS NULL)
    BEGIN
        CREATE ROLE [GeneralUser] AUTHORIZATION [dbo];
    END
    ALTER AUTHORIZATION ON SCHEMA::Servicing TO [GeneralUser]

    IF NOT EXISTS(SELECT NAME FROM SYS.TABLES WHERE Name = 'ServicingLock')
    BEGIN 
        CREATE TABLE [Servicing].[ServicingLock] ([Name] nvarchar(255) not null, [Value] int not null, [LastServiceTimestamp] datetime null)
    END

    IF NOT EXISTS(SELECT 1 FROM [Servicing].[ServicingLock])
    BEGIN 
        INSERT INTO [Servicing].[ServicingLock] (Name, Value) VALUES ('ServicingLockMode', 0)
    END
    COMMIT TRANSACTION


    PRINT 'Entering servicing mode'
    DECLARE @result int;
    EXEC @result = sp_getapplock @DbPrincipal='public', @Resource='ServicingLock', @LockMode='Exclusive', @LockOwner='Session', @LockTimeout=300000;
    IF @result < 0 RAISERROR ('Unable to acquire SQL applock. Result: %d', 16, 1, @result);

    BEGIN TRY
    IF EXISTS(SELECT TOP 1 1 FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_SCHEMA = 'Scheduling' COLLATE DATABASE_DEFAULT AND TABLE_NAME = 'SchedulerRegister' COLLATE DATABASE_DEFAULT AND COLUMN_NAME = 'ServicingMode' COLLATE DATABASE_DEFAULT)
    BEGIN       
           UPDATE Scheduling.SchedulerRegister SET ServicingMode = 1 WHERE ServicingMode = 0        
           UPDATE [Servicing].[ServicingLock] SET Name = 'SchedulerServicingMode', Value = 1, LastServiceTimestamp = GETUTCDATE() WHERE Value = 0
    END
    PRINT 'Acquired servicing locks'

    --Disable maps
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)

    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------
    ------------------------------------------------------------------------------------------


    ------------------------------
    PRINT 'Save and Drop Indexes Of FactAttributeValue and DimensionValueAttributeValue'
    ------------------------------

    IF EXISTS(SELECT 1 FROM sys.procedures WHERE object_id = OBJECT_ID('[Datamart].[SaveAndDropAttributeValueIndexes]'))
    BEGIN
        IF (NOT EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'AttributeValueIndexesBackUp'))
        BEGIN
            --create table to store indexses
            -- Indexes of different table can have same index_id,but we need unique index id
            Create table [Datamart].[AttributeValueIndexesBackUp]
            (
                IndexID INT not null IDENTITY(1,1) PRIMARY KEY,
                IndexName NVARCHAR(255),
                IsUnique BIT,
                IndexType NVARCHAR(60),
                FilterDefinition NVARCHAR(max),
                KeyColumns NVARCHAR(max),
                IncludedColumns NVARCHAR(max),
                IndexRetry INT,
                IndexStatus NVARCHAR(60),
                AttributeType INT,
            )
        END

        IF (EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'FactAttributeValue')) 
        BEGIN
            --truncate table to increase index drop performance
            PRINT('TRUNCATE TABLE [Datamart].[FactAttributeValue]')
            EXEC('TRUNCATE TABLE [Datamart].[FactAttributeValue]')
            EXEC [Datamart].[SaveAndDropAttributeValueIndexes] 'FACTID','[Datamart].[FactAttributeValue]'
        END

        IF (EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND  TABLE_NAME = 'DimensionValueAttributeValue')) 
        BEGIN
            --truncate table to increase index drop performance
            PRINT('TRUNCATE TABLE [Datamart].[DimensionValueAttributeValue]')
            EXEC('TRUNCATE TABLE [Datamart].[DimensionValueAttributeValue]')
            EXEC [Datamart].[SaveAndDropAttributeValueIndexes] 'DIMENSIONVALUEID','[Datamart].[DimensionValueAttributeValue]'
        END
    End

    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @stagingTableName nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT t.TABLE_NAME as TableName
    FROM INFORMATION_SCHEMA.TABLES t WITH (NOLOCK)
    WHERE t.TABLE_SCHEMA = 'Datamart' and (t.TABLE_NAME like 'FactStaging[0-9]%' or t.TABLE_NAME like 'DimensionCombinationStaging[0-9]%')
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @stagingTableName
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP TABLE IF EXISTS [Datamart].' + @stagingTableName)
        FETCH NEXT FROM dropCursor INTO @stagingTableName
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor

    ------------------------------
    PRINT 'Dropping tables with dynamic columns'
    ------------------------------
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationProcessing
    DROP TABLE IF EXISTS [Datamart].DimensionCombination
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationResolving
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationStaging
    DROP TABLE IF EXISTS [Datamart].DimensionCombinationUnreferenced
    DROP TABLE IF EXISTS [Datamart].DimensionValueAttributeValue
    DROP TABLE IF EXISTS [Datamart].FactAttributeValue
    DROP TABLE IF EXISTS [Datamart].TranslatedPeriodBalance
    DROP TABLE IF EXISTS [Datamart].TranslatedPeriodBalanceChanges

    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
    FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables

    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory' and @tablename <> 'AttributeValueIndexesBackUp'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
                EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
                INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
                WHERE o.[type] = 'V'
                AND referenced_schema_name = @schemaname
                AND referenced_entity_name = @tablename))
            BEGIN
                PRINT 'deleting from ' + @tablename
                EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
                PRINT 'truncating from ' + @tablename
                EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables

    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------

    -- Rebuild the tables with dynamic columns
    IF EXISTS(SELECT 1 FROM sys.procedures WHERE object_id = OBJECT_ID('[Datamart].[AddDynamicTables]'))
        BEGIN
            EXEC [Datamart].AddDynamicTables
        END
    ELSE
        BEGIN
            ---- Basically a copy of sproc AddDynamicTables
            IF NOT EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationStaging' AND TABLE_SCHEMA = 'Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationStaging](
                    [Id] [bigint] NOT NULL,
                    [OrganizationId] [int] NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NOT NULL,
                    [OrganizationKey] [nvarchar](100) NULL,
                    [FreshnessDate][datetime2] NULL default sysutcdatetime())

                CREATE STATISTICS [stat_dcs_org] ON [Datamart].DimensionCombinationStaging (OrganizationKey)
            END

            IF NOT EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationResolving' AND TABLE_SCHEMA = 'Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationResolving]
                (
                    [Id] [BIGINT] NOT NULL,
                    [Description] [NVARCHAR](51) NULL,
                    [SourceKey] [NVARCHAR](100) NULL,
                    [OrganizationId] [INT] NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='DimensionCombination' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombination](
                    [Id] [bigint] NOT NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NULL,
                    [OrganizationId] [int] NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='FactAttributeValue' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[FactAttributeValue](
                    [FactId] [bigint] NOT NULL
                )
            END

            IF NOT EXISTS(SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='DimensionValueAttributeValue' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionValueAttributeValue](
                    [DimensionValueId] [bigint] NOT NULL
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='PeriodExchangeRate' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[PeriodExchangeRate]
                (
                    [PeriodId] INT NOT NULL,
                    [FromUnitOfMeasureId] INT NOT NULL,
                    [CurrencyMethod] TINYINT NOT NULL,
                    [ExchangeRateTypeId] INT NOT NULL,
                    CONSTRAINT [PK_PeriodExchangeRates] PRIMARY KEY ([FromUnitOfMeasureId], [PeriodId], [CurrencyMethod], [ExchangeRateTypeId])
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='TranslatedPeriodBalance' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[TranslatedPeriodBalance](
                    [PeriodId] [INT] NOT NULL,
                    [DimensionsId] [BIGINT] NOT NULL,
                    [ScenarioId] [INT] NOT NULL,
                    [FactType] [SMALLINT] NOT NULL,
                    [PostingLayerId] [INT] NULL
                )
            END

            IF NOT EXISTS(SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE ='BASE TABLE' AND TABLE_NAME='TranslatedPeriodBalanceChanges' AND TABLE_SCHEMA='Datamart')
            BEGIN
                CREATE TABLE [Datamart].TranslatedPeriodBalanceChanges(PeriodId bigint, DimensionsId bigint, ScenarioId int, PostingLayerId int null, FactType smallint,
                        constraint [IDX_BC1] unique Clustered (PeriodId, DimensionsId, ScenarioId, PostingLayerId, FactType DESC))
            END

            IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_NAME = 'DimensionCombinationArchive' AND TABLE_SCHEMA='Datamart')
            BEGIN
                IF EXISTS (SELECT TOP 1 * FROM [Datamart].[DimensionCombinationArchive])
                BEGIN
                    -- move archived combinations from the obsolete DimensionCombinationArchive table to a new table in the archive
                    -- and set its generation to 5, so it will run in 4 hours (which is how long the archived combinations were attempted originally before moving to the archive table).
                    DECLARE @archiveId INT = 0
                    INSERT INTO [Datamart].[Archive] (Generation, NextAttempt) VALUES (5, DATEADD(MINUTE, POWER(3, 5), SYSUTCDATETIME()))
                    SET @archiveId = SCOPE_IDENTITY()

                    DECLARE @comboArchiveTableName nvarchar(100) = 'DimensionCombinationStaging' + CAST(@archiveId as nvarchar(10))
                    EXEC sp_rename 'Datamart.DimensionCombinationArchive', @comboArchiveTableName

                    DECLARE @factArchiveTableName nvarchar(100) = 'FactStaging' + CAST(@archiveId as nvarchar(10))
                    EXEC ('select top 0 * into Datamart.' + @factArchiveTableName + ' from Datamart.FactStaging')
                END
                ELSE
                BEGIN
                    DROP TABLE [Datamart].[DimensionCombinationArchive]
                END
            END

            IF NOT EXISTS (SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_TYPE='BASE TABLE' AND TABLE_NAME = 'DimensionCombinationUnreferenced' and TABLE_SCHEMA ='Datamart')
            BEGIN
                CREATE TABLE [Datamart].[DimensionCombinationUnreferenced]
                (
                    [Id] [bigint] NOT NULL,
                    [Description] [nvarchar](51) NULL,
                    [SourceKey] [nvarchar](100) NULL,
                    [OrganizationId] [int] NULL
                )

                DECLARE @columnIndex int
                DECLARE @idColumn nvarchar(128)
                DECLARE columnCursor CURSOR LOCAL FAST_FORWARD FOR SELECT DISTINCT ColumnIndex FROM [Datamart].DimensionDefinition ORDER BY ColumnIndex
                OPEN columnCursor
                FETCH NEXT FROM columnCursor INTO @columnIndex
                WHILE (@@FETCH_STATUS <> -1)
                BEGIN
                    SET @idColumn = 'Dimension' + CAST(@columnIndex as nvarchar(3)) + 'Id'
                    EXEC [Datamart].AddColumn @schemaName = 'Datamart', @tableName = 'DimensionCombinationUnreferenced', @columnName = @idColumn, @columnType = 'bigint NULL'
                    FETCH NEXT FROM columnCursor INTO @columnIndex
                END
                CLOSE columnCursor
                DEALLOCATE columnCursor


                DECLARE @dcColumnList nvarchar(max) = ''
                DECLARE @rowsCopied bigint
                DECLARE @columnName nvarchar(100)
                DECLARE columnNameCursor cursor local fast_forward for select distinct Name from sys.columns c where c.object_id = OBJECT_ID('DimensionCombination')
                OPEN columnNameCursor
                FETCH NEXT FROM columnNameCursor INTO @columnName
                WHILE (@@FETCH_STATUS <> -1)
                BEGIN
                    IF @dcColumnList <> ''
                        SET @dcColumnList = @dcColumnList + ', '

                    SET @dcColumnList = @dcColumnList + @columnName
                    FETCH NEXT FROM columnNameCursor INTO @columnName
                END
                CLOSE columnNameCursor
                DEALLOCATE columnNameCursor

                if @dcColumnList <> ''
                BEGIN
                    exec ('
                        insert into [Datamart].DimensionCombinationUnreferenced (' + @dcColumnList + ')
                        select ' + @dcColumnList + ' from [Datamart].DimensionCombination dc
                        where dc.Id not in (Select distinct DimensionsId from [Datamart].Fact)')

                    SET @rowsCopied = @@ROWCOUNT
                    IF @rowsCopied > 0
                    BEGIN
                        DECLARE @comboCount bigint
                        EXEC [Datamart].GetRowCount 'DimensionCombination', @comboCount

                        IF (@rowsCopied * 2) > @comboCount
                        BEGIN
                            -- most of the combinations in the combination table were unreferenced, so it would be faster to move the referenced out, truncate the table, then move back
                            SELECT * INTO #referencedCombos from [Datamart].DimensionCombination dc
                            WHERE dc.Id NOT IN (SELECT Id from [Datamart].DimensionCombinationUnreferenced)

                            TRUNCATE TABLE [Datamart].[DimensionCombination]

                            INSERT INTO [Datamart].[DimensionCombination]
                            SELECT * FROM #referencedCombos

                            DROP TABLE #referencedCombos
                        END
                        ELSE
                        BEGIN
                            -- we didn't find many unreferenced combinations, so delete them
                            DELETE FROM [Datamart].[DimensionCombination] WHERE Id in (SELECT Id FROM [Datamart].[DimensionCombinationUnreferenced])
                        END
                    END
                END
            END
        END



    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    
    EXEC sys.sp_releaseapplock @Resource='ServicingLock', @LockOwner='Session'
    END TRY
    BEGIN CATCH
    EXEC sys.sp_releaseapplock @Resource='ServicingLock', @LockOwner='Session'
    ;THROW;
    END CATCH
    

2. (Optional) On the MRDB, execute the following script, which was last updated February 25, 2020: ResetUsersAndCompanies.txt
> [!NOTE]
> Do not run this script unless you need to delete all users and companies. This script will remove user references from previously generated reports, and remove users from their assigned security groups. This step is not required in most cases.

```sql
-- Attempt to delete integrated users
    DECLARE @userId nvarchar(max)
    DECLARE removeUserCursor CURSOR LOCAL FAST_FORWARD FOR
    select UserID from Reporting.SecurityUser where UserID <> '00000000-0000-0000-0000-000000000002'
    OPEN removeUserCursor
    FETCH NEXT FROM removeUserCursor INTO @userId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        BEGIN TRY
           exec Reporting.SecurityUserDeleteRelatedEntities @userId
           delete from Reporting.SecurityGroupUser where UserID = @userId
           delete from Reporting.SecurityUser where UserID = @userId
        END TRY
        BEGIN CATCH
        -- Just skip if we cannot delete a user, integration should take care of it
        END CATCH
        FETCH NEXT FROM removeUserCursor INTO @userId
    END
    CLOSE removeUserCursor
    DEALLOCATE removeUserCursor

-- Attempt to delete integrated companies
    DECLARE @companyId nvarchar(max)
    DECLARE removeCompanyCursor CURSOR LOCAL FAST_FORWARD FOR
    select cc.ID from Reporting.ControlCompany cc join Reporting.ControlCompanyIntegration cci on cc.ID = cci.ID
    OPEN removeCompanyCursor
    FETCH NEXT FROM removeCompanyCursor INTO @companyId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        BEGIN TRY
           delete from Reporting.ControlCompany where ID = @companyId
        END TRY
        BEGIN CATCH
        -- Just skip if we cannot delete a company
        END CATCH
        FETCH NEXT FROM removeCompanyCursor INTO @companyId
    END
    CLOSE removeCompanyCursor
    DEALLOCATE removeCompanyCursor
```

3. AXDB と呼ばれる Dynamics 365 Finance のためのデータベースでは、2019 年 2 月 25 日に更新された次のスクリプトを使用して財務報告の関連テーブルをクリアします: Reset Datamart AXDB.txt

```sql
IF EXISTS (SELECT 1 FROM [INFORMATION_SCHEMA].[TABLES] WHERE [TABLE_SCHEMA] = 'dbo' and [TABLE_NAME] = 'FINANCIALREPORTS') 
BEGIN 
    TRUNCATE TABLE [dbo].[FINANCIALREPORTS] 
END 
IF EXISTS (SELECT 1 FROM [INFORMATION_SCHEMA].[TABLES] WHERE [TABLE_SCHEMA] = 'dbo' and [TABLE_NAME] = 'FINANCIALREPORTVERSION') 
BEGIN 
    TRUNCATE TABLE [dbo].[FINANCIALREPORTVERSION] 
END  
```


4. MRDB では、次の最後に更新されたスクリプトを使用して統合とエンド サービス モードを再び有効にし、2019 年 2 月 25 日に更新された次のスクリプトを使用して財務報告の関連テーブルをクリアします: Reset Datamart END.txt



```sql
DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
------------------------------------------
------------------------------------------
PRINT 'Reset the map tokens'
UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
PRINT 'Reset the tasks'
UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
FROM [Scheduling].[Task] t with(nolock)
JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
PRINT 'Enable integration tasks, RunImmediately'
UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
PRINT 'Enable the Maintenance Task'
UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
(SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
------------------------------------------
------------------------------------------

UPDATE [Servicing].[ServicingLock] SET [Value] = 0 WHERE [Value] = 1
IF EXISTS(SELECT TOP 1 1 FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_SCHEMA = 'Scheduling' COLLATE DATABASE_DEFAULT AND TABLE_NAME = 'SchedulerRegister' COLLATE DATABASE_DEFAULT AND COLUMN_NAME = 'ServicingMode' COLLATE DATABASE_DEFAULT)
BEGIN
       UPDATE Scheduling.SchedulerRegister SET ServicingMode = 0
END
```


5. リセット後は、手動で財務諸表データベースに対して次のクエリを実行し、データの再読み込みを確認することができます。

    ```sql
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

すべての行の **LastRunTime** 値、およびその **StateType** が **5** に設定されていることを確認してください。 **5** の **StateType** 値はデータが正常に再読み込みされたことを示します。 **7** の値はエラー状態を示します。 組織階層マップは、初めて実行される時にこの状態になることがあります。 ただし、エラー状態は自動的に解決されます。

## <a name="export-and-import-report-definitions"></a>レポートの定義を エクスポート/インポートする

データ マートのリセットは、どのレポート定義にも影響しませんが、データ移動のアクティビティによってはレポート定義が失われる場合があります。 ユーザー受け入れテスト(UAT)テスト環境で新しいレポートを作成する場合は、UAT環境を本番環境のコピーで上書きするなどして、データ移動アクティビティを実行の際には十分に注意してください。 レポート定義をエクスポートすると、定義を復元する必要が生じた場合に、バックアップを作成できます。 

### <a name="export-report-definitions"></a>レポート定義のエクスポート

最初に、以下の手順を実行しレポート デザイナーからレポート デザインをエクスポートします。

1. レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。
2. エクスポートする構成要素グループを選択し、**エクスポート** を選択します。

    > [!NOTE]
    > Finance and Operations に関しては、1 つの構成要素グループのみがサポートされています: **既定**。

3. エクスポートするレポート定義を選択します:

    - レポート定義および関連するレポート パーツのすべてをエクスポートするには、**すべて選択** を選択します。
    - 特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブを選択してエクスポートする項目を選択します。 タブにて複数のレコードを選択するには、キーボードの **Ctrl キー** を押しながら選択します。 エクスポートをするレポートを選択すると、関連する行、列、ツリー、各要素のセットが選択されます。

4. **エクスポート** の選択
5. ファイル名を入力し、エクスポートしたレポート定義を保存する保護された安全な場所を選択します。
6. **保存** を選択します。

ファイルを安全な場所にコピーまたはアップロードできます。

> [!WARNING]
> Microsoft Azure Virtual Machines (VMs) の Dドライブ の挙動には気をつけてください。 Dドライブに、エクスポートしたレポート パーツ グループを完全には保存しません。一時的なドライブの詳細については、次を参照してください。[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](/archive/blogs/mast/understanding-the-temporary-drive-on-windows-azure-virtual-machines).

### <a name="import-report-definitions"></a>レポート定義のインポート

次に、エクスポートの課程で作成されたファイルを使用して、レポート デザイナー から レポートのデザイン を インポートします。

1. レポート デザイナーで、**会社** &gt; **レポート パーツ グループ** を選択します。
2. **既定** の構成要素を選択し、**インポート** をクリックします。
3. エクスポート済みのレポート定義を含むファイルを選択し、**開く** をクリックします。
4. **インポート** ダイアログ ボックスで、インポートするレポート定義を選択します。

    - レポート定義および関連するレポート パーツのすべてをインポートするには、**すべて選択** を選択します。
    - 特定のレポートをインポートするには、行、列、ツリー、あるいは必要な要素を選択してください。

5. **インポート** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
