---
title: "財務報告のデータ マートのリセット"
description: "財務報告データ マートをリセットする方法について説明します。"
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: ja-jp
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>財務報告のデータ マートのリセット

[!include[banner](../includes/banner.md)]

このトピックでは、次のバージョンの財務報告データ マートをリセットする方法について説明します:

- Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.2.6.0 以降のリリース
- Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.0.10000.4 以降のリリース
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (オンプレミス)

Finance and Operations 財務諸表 7.2.6.0 のリリースを取得するには、<https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514> から KB 4052514 をダウンロードしてください。

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Finance and Operations 財務諸表 7.2.6.0 以降のリリースの財務報告のデータ マートのリセット

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>レポート デザイナーからの財務報告のデータ マートのリセット

> [!NOTE]
> このプロセスのステップは、Finance and Operations 財務諸表 7.2.6.0 以降のリリースでサポートされています。 以前のリリースを持っている場合は、サポート チームに問い合わせてください。

特定のシナリオでは、場合によっては財務諸表のデータ マートをリセットする必要があります。 レポート デザイナーのクライアントでこのタスクを実行することができます。 データ マートをリセットする必要があるかもしれない、いくつかのシナリオを次に示します:

- Finance and Operations データベースが復元されましたが、データ マート データベースは復元されませんでした。
- 期間の誤ったデータが表示されます。
- トラブルシューティング手順の一部として、サポートはデータ マートをリセットするように指示します。

データ マートのリセットは、データベースの処理の量が小さい時間帯にのみ実行してください。 財務諸表は、リセット プロセス中は使用できません。

#### <a name="reset-the-data-mart"></a>データ マートのリセット

データ マートをリセットするには、レポート デザイナーの、[**ツール**] メニューにある、[**データ マートのリセット**] を選択してください。 表示されるダイアログ ボックスには2つのセクションがあります: [**統計**] および [**リセット**]。

[![データ マートのダイアログ ボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>統合試行回数

[**統合試行回数**] グリッドは、システムがトランザクションの統合を試みた回数を表示します。 システムは、最初のいくつかの試行ができなかった場合は、日の期間にわたってデータを統合するまで続行されます。 試行回数が8回以上の場合、および分析コードの組み合わせやトランザクション レコードが多い場合、データ マートをリセットする必要があります。 このような状況では、データはレポートされません。

##### <a name="data-status"></a>データのステータス

[**データのステータス**] グリッドは、データ マート内のトランザクション、為替レート、および分析コード値のスナップショットを表示します。 古いレコードが多数ある場合、レコードに対して更新が数多く存在することになります。 このような場合、レポート生成に時間がかかることがあります。

##### <a name="misaligned-main-account-categories"></a>正しく整合されていない主勘定カテゴリ

Microsoft Dynamics 365 for Finance and Operations 財務諸表 7.2.1 以前のリリースを使用している場合で、勘定の名前を変更して勘定カテゴリの間で勘定を移動する場合、データ マートをリセットする必要がある場合があります。 これらのアクションにより、主勘定カテゴリが正しく整合されなくなることがあります。 [**正しく整合されていない主勘定カテゴリ**] フィールドには問題が発生しているかどうかが表示されます。

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Finance and Operations 財務諸表 7.2.6.0 のリリースで、データ マートをリセットします。

Finance and Operations 財務諸表 7.2.6.0 以前のリリースでデータ マートをリセットするには、[**データ マートのリセット**] ダイアログ ボックスで、[**データ マートのリセット**] のチェックボックスを選択し、[**OK**] を選択します。 データ マートのリセットは、スケジュール済ダウンタイム中にのみ行う必要があります。

[![Rデータ マートのチェックボックスをリセットします](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Microsoft Dynamics 365 for Finance and Operations Financial reporting 7.3.0 のリリースで、データ マートをリセットし、理由を選択してください。

データ マートのリセットが必要であると判断した場合は、[**データ マートのリセット**] チェック ボックスを選択し、[**理由**] フィールドで理由を選択します。  次のオプションを使用できます。

- **データが不足しているか、正しくありません** – 統計に基づき、決定したデータが存在しない可能性があります。 続行する前に、根本原因を判断するためにサポートを使用することをお勧めします。
- **データベースの復元** – Finance and Operations データベースが復元されましたが、財務諸表のデータ マートのデータベースは復元されませんでした。
- **その他** – 別の理由によりデータ マートをリセットしています。 問題があることを懸念する場合は、識別のためにサポートに問い合わせてください。

[![データ マートのリセット](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> リセットを開始する前に、すべてのデータ マート リセット タスクが初回の読み込みを完了したことを確認します。 **ツール** &gt; **統合の状態** を選択して、前回のランタイム列で値を探すことにより、これを確定できます。

#### <a name="clear-users-and-companies"></a>ユーザーと会社をクリア

データベースを復元しましたが、ユーザーまたは会社に変更を加えた場合は [**ユーザーと会社をクリア**] チェックボックスを選択します。 このチェックボックスをオンにすることはほとんどありません。

リセット プロセスを開始する準備ができたら、[**OK**] を選択します。 プロセスを開始する準備ができていることを確認するように求められます。 財務諸表は、リセット中およびその後に発生する最初のデータ統合中には使用できないことに注意してください。

統合の状態を確認する場合は、**ツール** &gt; **統合の状態** を選択し、統合が最後に実行された時刻と状態を表示します。

[![統合のステータスを表示](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> すべてのマッピングが RanToCompletion の状態を表示し、および統合の状態ウィンドウが左下隅で「統合が完了しました」と表示する場合、リセットが完了します。

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Finance and Operations 財務諸表 7.0.10000.4 以降のリリースの財務報告のデータ マートのリセット

Finance and Operations データベースをバックアップから復元したか別の環境からデータベースをコピーした場合、このセクションのステップに従って、財務諸表のデータ マートが復元したFinance and Operations データベースを正しく使用していることを保証する必要があります。

> [!NOTE]
> このプロセスの手順は、Microsoft Dynamics AX application version 7.0.1 (2016 年 5 月) (アプリケーション ビルド 7.0.1265.23014 および財務諸表ビルド 7.0.10000.4) およびそれ以降のリリースでサポートされています。 Finance and Operations の以前のバージョンを持っている場合は、サポート チームに問い合わせてください。

### <a name="export-report-definitions"></a>レポート定義のエクスポート

最初に、以下の手順を実行しレポート デザイナーからレポート デザインをエクスポートします。

1. レポート デザイナーで、[**会社**] &gt; [**レポート パーツ グループ**] を選択します。
2. エクスポートする構成要素グループを選択し、[**エクスポート**] を選択します。

    > [!NOTE]
    > Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。

3. エクスポートするレポート定義を選択します:

    - レポート定義および関連するレポート パーツのすべてをエクスポートするには、[**すべて選択**] を選択します。
    - 特定のレポート、行、列、ツリー、または分析コード セットをエクスポートするには、適切なタブを選択してエクスポートする項目を選択します。 タブ上の複数の項目を選択するには、Ctrl キーを押しながら選択します。エクスポートするレポートを選択したとき、関連する行、列、ツリー、分析コードセットが選択されます。

4. [**エクスポート**] の選択
5. ファイル名を入力し、エクスポートされたレポート定義を保存できる安全な場所を選択します。
6. [**保存**] を選択します。

ファイルを安全な場所にコピーまたはアップロードできます。 これにより、ファイルは後に異なった環境にもインポートできます。 Microsoft Azure ストレージ アカウントの使用方法に関する情報は、[AzCopy Command-Line Utility でデータを転送する](/azure/storage/storage-use-azcopy) を参照してください。

> [!NOTE]
> Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。 ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。

> [!WARNING]
> Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。 Dドライブに、エクスポートしたレポート パーツ グループを完全には保存しません。一時的なドライブの詳細については、次を参照してください。[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>サービスの停止

次のMicrosoft Windows サービスは、Finance and Operations データベースへの接続が提供されます。 したがって、Microsoft Remote Desktop を使用して環境内のすべてのコンピュータに接続し、services.msc を使用してこれらのサービスを停止する必要があります。

- ワールド ワイド ウェブ公開サービス (すべての Application Object Server [AOS] コンピュータ上)
- Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
- Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス [BI] コンピューターのみ)

### <a name="reset"></a>リセット

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>最新の MinorVersionDataUpgrade.zip パッケージをダウンロードする

最新の MinorVersionDataUpgrade.zip パッケージをダウンロードします。 データ アップグレード パッケージの適切なバージョンを検索しダウンロードする手順については、[最新のデータ アップグレード配置可能パッケージをダウンロードする](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package) を参照してください。 

MinorVersionDataUpgrade.zip パッケージをダウンロードするためにアップグレードは必要ありません。 したがって、そのトピックにある「最新のデータ アップグレード配置可能パッケージをダウンロードする」セクションの手順に従ってください。 トピックのその他のすべての手順をスキップできます。

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Finance and Operations データベースに対してスクリプトを実行する

財務諸表 データベースに対してではなく、Finance and Operations データベースに対して、次のスクリプトを実行します:

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

これらのスクリプトは、ユーザー、ロール、変更の追跡の設定が正しいことを保証する助けになります。

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>データベースをリセットするのには Windows PowerShell コマンドを実行します。

AOS コンピュータで、管理者として Microsoft Windows PowerShell を開始し、Finance and Operations と財務諸表との統合をリセットするために次のコマンドを実行します。

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

ここでは **Reset-DatamartIntegration** コマンドのパラメータについて説明します:

- **-Reason** の有効な値は、**SERVICING**、**BADDATA**、および **OTHER** です。
- **-ReasonDetail** パラメーターは自由書式です。
- 理由と理由の詳細はテレメトリーまたは環境モニタリングに記録されます。

> [!NOTE]
> コマンドを実行した後、データベースをリセットすることを確認するために [**Y**] を入力するように求められます。

#### <a name="restart-services"></a>サービスをリセット

services.msc を使用して、以前に停止したサービスを再起動します。

- ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
- Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)
- Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

#### <a name="import-report-definitions"></a>レポート定義のインポート

エクスポート中に作成されたファイルを使用して、レポート デザイナーからレポート デザインをインポートします。

1. レポート デザイナーで、[**会社**] &gt; [**レポート パーツ グループ**] を選択します。
2. エクスポートする構成要素グループを選択し、[**エクスポート**] を選択します。

    > [!NOTE]
    > Finance and Operations では、**既定** として 1 つの構成要素グループのみがサポートされます。

3. **既定** の構成要素を選択し、[**インポート**] をクリックします。
4. エクスポート済みのレポート定義を含むファイルを選択し、[**開く**] をクリックします。
5. [**インポート**] ダイアログ ボックスで、インポートするレポート定義を選択します。

    - レポート定義および関連するレポート パーツのすべてをインポートするには、[**すべて選択**] を選択します。
    - 特定のレポート、行、列、ツリー、または分析コードセットをインポートするには、インポートするレポート、行、列、ツリー、または分析コードセットを選択します。

6. [**インポート**] を選択します。

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Finance and Operations (オンプレミス) の財務諸表 データ マートをリセットします

1. レポート デザイナーおよび Finance and Operations の財務諸表エリアを終了するようすべてのユーザーに指示します。
2. 財務諸表データベース (MRDB) に対して、次のスクリプトを実行します。

    ```
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
    ```

3. Finance and Operations データベース (AXDB) にある FINANCIALREPORTS テーブルのすべてのレコードを切り捨て、または削除します。
4. FINANCIALREPORTVERSION テーブルが Finance and Operations データベースに存在する場合、このテーブルのすべてのレコードを切り捨て、または削除します。 テーブルが Finance and Operations データベースに存在しない場合、このステップを省略します。
5. 財務諸表データベースに対して、**ResetDatamart.sql** を実行します。 このスクリプトはデータ マートの統合を無効にし、すべてのデータ マートを削除し、その後データ マートの統合を再び有効にします。

    ```
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
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
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
        IF @tablename <> 'VersionHistory'
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
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
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
    ```

6. リセット後は、手動で財務諸表データベースに対して次のクエリを実行し、データの再読み込みを確認することができます。

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    すべての行の **LastRunTime** 値、およびその **StateType** が **5** に設定されていることを確認してください。 **5** の **StateType** 値はデータが正常に再読み込みされたことを示します。 **7** の値はエラー状態を示します。 組織階層マップは、初めて実行される時にこの状態になることがあります。 ただし、エラー状態は自動的に解決されます。

