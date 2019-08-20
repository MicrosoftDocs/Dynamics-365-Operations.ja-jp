---
redirect_url: /dynamics365/unified-operations/dev-itpro/database/dbmovement-operations
title: Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを SQL Server をベースとした開発、ビルド、またはデモ環境 (第 1 層または ワンボックス) から Azure SQL データベースをベースしたサンドボックス UAT 環境 (第 2 層以上) に移動する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 10/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 256464
ms.assetid: 4cc5f2aa-dd4e-4981-9607-e75fd1d57941
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 84bb1ef34b02038a2b60ba0e6ec7deb3dea507d2
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848273"
---
# <a name="copy-finance-and-operations-databases-from-sql-server-to-production-azure-sql-database-environments"></a>Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを、Microsoft SQL Server をベースとした環境 (開発、ビルド、またはデモ環境。第 1 層またはワンボックス環境とも呼ばれます) から Microsoft Azure SQL データベースをベースとした環境 (サンドボックス ユーザー受け入れテストの \[UAT\] 環境。第 2 層以上) に移動する方法について説明します。

通常、このプロセスは稼動前に完了し、システム構成データのみを含むゴールデン (またはシード) データベースを実稼働環境に移行します。 このプロセスは、すべての状況に適しているわけではありません。 たとえば、既存の実際の展開に対して新しい法人のデータをインポートするためには、このプロセスを使用しないでください。 このタイプの場合、[プロセス データ パッケージ](../lcs-solutions/process-data-packages-lcs-solutions.md)または[データ エンティティ データ パッケージ](../data-entities/data-entities-data-packages.md)を使用することをお勧めします。

ゴールデン データベースを実稼働環境に移行するためにサポートされている手順を次に示します。

1. 顧客やパートナーは、SQL Server のデータベースをエクスポートします。
2. 顧客またはパートナーは、データベースを Azure SQL データベース上で実行されるサンドボックス環境にインポートします。
3. Microsoft Dynamics Lifecycle Services (LCS) では、顧客またはパートナーが**サンドボックスから実稼働環境**タイプのサービス要求を送信して、Microsoft Dynamics のサポート エンジニアリング (DSE) チームにサンドボックス データベースを実稼動環境に移動してもらうよう依頼します。
4. DSE チームでは、データベースをサンドボックス環境から実稼働環境にコピーします。

> [!NOTE]
> Microsoft は、運用する前にのみデータベースを実稼働環境にコピーする要求を受け入れます。

データベースの移動中に、sqlpackage.exe コマンド ライン ツールを使用して、SQL Server からデータベースをエクスポートし、Azure SQL データベースにインポートします。 エクスポートされたデータ ファイルのファイル名拡張子は .bacpac なので、プロセスは多くの場合 *bacpac プロセス*と呼ばれます。

データベース移動のための高レベルのプロセスを次に示します。

1. ソース データベースのコピーを作成します。
2. データベースの準備のためスクリプトを実行します。
3. SQL Server からデータベースをエクスポートします。
4. Azure SQL データベースにデータベースをインポートします。
5. データベースの更新のためスクリプトを実行します。

問題が発生する場合は、このトピックの最後にある「既知の問題と制限事項」を参照します。 トラブルシューティング方法について説明し、パフォーマンスのヒントを紹介して、コピー処理の制限について説明します。

## <a name="prerequisites"></a>前提条件

- ソース環境 (ソース データベースが作成された環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。
- サンドボックス環境からデータベースをインポートするには、データベースをインポートする環境で同じバージョンの SQL Server Management Studio を実行している必要があります。 これにより、サンドボックス環境で Application Object Server (AOS) を実行するコンピューターに [SQL Server Management Studio の最新バージョン](https://msdn.microsoft.com/library/mt238290.aspx)をインストールする必要が生じる場合があります。 AOS コンピューターで、bacpac エクスポートを実行することができます。 この要件は 2 つの理由があります。

    - SQL Server のサンドボックス インスタンスに対するインターネット プロトコル (IP) アクセス制限のため、その環境内のコンピュータのみがインスタンスに接続できます。
    - エクスポートされた \*.bacpac ファイルは、Management Studio のバージョン固有の機能に依存する可能性があります。

> [!IMPORTANT]
> 環境に、Microsoft Dynamics 365 for Retail コンポーネントが含まれている場合、開始する前に、一部の環境固有の値を手動で保存する必要があります。 詳細については、「小売環境の追加手順」セクションを参照してください。

## <a name="before-you-begin"></a>準備

### <a name="supported-sql-server-collation"></a>サポートされる SQL Server の照合順序

クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、**SQL_Latin1_General_CP1_CI_AS** です。 開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。

### <a name="document-the-values-of-encrypted-fields"></a>暗号化されたフィールドの値を文書化

暗号化された環境固有の値を新しい環境にインポートすることはできません。 インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。

データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。 したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。 インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。 次のフィールドが影響されます。 フィールド名は Table.Field 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。 |
| SysEmailSMPTPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a>小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。

次のページの値は、環境固有またはデータベースで暗号化されています。 したがって、インポートされた値はすべて正しくありません。

- 支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。
- ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)

## <a name="create-a-copy-of-the-source-database"></a>ソース データベースのコピーを作成します。

ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。 元のデータベースを修正する代わりに、コピーで作業することができます。 次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。 このスクリプトを使用するには、最初に D:\\backups のパスが存在することを確認します。

```
BACKUP DATABASE [AxDB] TO DISK = N'D:\Backups\axdb_golden.bak' WITH NOFORMAT, NOINIT,
NAME = N'AxDB_golden-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION, STATS = 10
GO
RESTORE DATABASE [AxDB_CopyForExport] FROM DISK = N'D:\Backups\axdb_golden.bak' WITH FILE = 1,
MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_CopyForExport.mdf',
MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForExport_Log.ldf',
NOUNLOAD, STATS = 5
```

## <a name="prepare-the-database"></a>データベースの準備

次のスクリプトを、前のセクションで作成した AxDB\_CopyForExport データベースに対して実行します。 このスクリプトは、次の変更を行います。

- **SysGlobalConfiguration** フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。
- XU\_DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。 Azure SQL データベースでは、tempDB の参照が許可されていません。 データベース同期プロセスは後で照会を再作成します。
- Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。 他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。
- 暗号化されたハードウェア プロファイルの merchand プロパティの消去

データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。

```
update sysglobalconfiguration
set value = 'SQLAZURE'
where name = 'BACKENDDB'

update sysglobalconfiguration
set value = 1
where name = 'TEMPTABLEINAXDB'

drop procedure XU_DisableEnableNonClusteredIndexes
drop procedure if exists SP_ConfigureTablesForChangeTracking
drop procedure if exists SP_ConfigureTablesForChangeTracking_V2
drop schema [NT AUTHORITY\NETWORK SERVICE]
drop user [NT AUTHORITY\NETWORK SERVICE]
drop user axdbadmin
drop user axdeployuser
drop user axmrruntimeuser
drop user axretaildatasyncuser
drop user axretailruntimeuser
drop user axdeployextuser
-- Clear encrypted hardware profile merchand properties
update dbo.RETAILHARDWAREPROFILE set SECUREMERCHANTPROPERTIES = null where SECUREMERCHANTPROPERTIES is not null
```

## <a name="export-the-database-from-sql-server"></a>SQL Server からデータベースをエクスポート

**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

> [!IMPORTANT]
> **140** フォルダーは、現在のバージョンを反映しており、サンドボックス環境で使用可能なバージョンを使用する必要があります。 これにより、開発環境に [Management Studio の最新バージョン](https://msdn.microsoft.com/library/mt238290.aspx) をインストールする必要が生じる場合があります。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\
SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

パラメータの説明を以下に示します。

- **ssn(ソース サーバー名)** – エクスポートする SQL Server の名前。 このトピックでは、名前は常に **localhost** である必要があります。
- **sdn(ソース データベース名)** – エクスポートするデータベースの名前。
- **tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。 フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。

## <a name="import-the-database-into-an-azure-sql-database"></a>Azure SQL データベースへのデータベースのインポート

前のセクションで生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。 ゴールデン データベースの標準的な .bacpac ファイルは、100 MB より小さくなります。 したがって、リモート デスクトップ プロトコル (RDP) ウィンドウを使用してファイルをコピーして貼り付けることができます。 .Bacpac ファイルが 100 MB よりも大きい場合、[Azure ストレージ アカウントにアップロード](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/)し、対象となる AOS コンピューターにダウンロードします。

> [!NOTE]
> Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。 ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。 パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。 (詳細については、「既知の問題と制限事項」セクションを参照してください。)

**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

> [!IMPORTANT]
> SqlPackage.exe のバージョンは、.bacpac ファイルのエクスポートに使用するバージョンと一致する必要があります。 [Management Studio の最新バージョン](https://msdn.microsoft.com/library/mt238290.aspx) のインストールが必要な場合があります。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure SQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P2
```

パラメータの説明を以下に示します。

- **tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。 名前を LCS で見つけることができます。 接尾語 **database.windows.net** を追加します。
- **tdn(ターゲット データベース名)** – インポートするデータベースの名前。 データベースが既に存在していては**いけません**。 インポート処理が作成されます。
- **sf(ソース ファイル)** – インポートするファイルのパスと名前。
- **tu(ターゲット ユーザー)** – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。 標準の **sqladmin** ユーザーを使用することをお勧めします。 LCS プロジェクトからは、このユーザーのパスワードを取得できます。
- **tp(ターゲット パスワード)** – ターゲットの Azure SQL データベース ユーザーのパスワード。
- **DatabaseServiceObjective** – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。 パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。 現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。

    ```
    SELECT  d.name,   
        slo.*    
    FROM sys.databases d   
    JOIN sys.database_service_objectives slo    
    ON d.database_id = slo.database_id;  
    ```

次の警告メッセージを受け取ります。 これは無視してかまいません。

> ターゲット プラットフォームとして SQL Server 2016 を指定するプロジェクトでは、Microsoft Azure SQL データベース v12 で互換性の問題が発生する可能性があります。

> [!WARNING] 
> どの Finance and Operations 環境でも、長期間にわたってデータベースのコピーを保持することはできません。 Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。

## <a name="update-the-database"></a>データベースの更新

インポートされたデータベースに対して、次のスクリプトを実行します。 スクリプトでは次のアクションを実行します。

- データベース ユーザーを再作成します。
- 適切な実績パラメーターを設定します。
- SQL Query Store 機能を有効にします。

> [!NOTE]
> テナント ID を最後の 3 つのクエリに追加する必要があります。 この値はターゲット環境内の既存のデータベースで SysServiceConfigurationSetting テーブルをクエリすることにより見つけることができます。

```
CREATE USER axdeployuser FROM LOGIN axdeployuser
EXEC sp_addrolemember 'db_owner', 'axdeployuser'

CREATE USER axdeployextuser WITH PASSWORD = '<password from LCS>'
IF EXISTS (select * from sys.database_principals where type = 'R' and name = 'DeployExtensibilityRole')
BEGIN
    EXEC sp_addrolemember 'DeployExtensibilityRole', 'axdeployextuser'
END

CREATE USER axdbadmin WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'db_owner', 'axdbadmin'

CREATE USER axruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'db_datareader', 'axruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axruntimeuser'

CREATE USER axmrruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'ReportingIntegrationUser', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datareader', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axmrruntimeuser'

CREATE USER axretailruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'UsersRole', 'axretailruntimeuser'
EXEC sp_addrolemember 'ReportUsersRole', 'axretailruntimeuser'

CREATE USER axretaildatasyncuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'DataSyncUsersRole', 'axretaildatasyncuser'

ALTER DATABASE SCOPED CONFIGURATION  SET MAXDOP=2
ALTER DATABASE SCOPED CONFIGURATION  SET LEGACY_CARDINALITY_ESTIMATION=ON
ALTER DATABASE SCOPED CONFIGURATION  SET PARAMETER_SNIFFING= ON
ALTER DATABASE SCOPED CONFIGURATION  SET QUERY_OPTIMIZER_HOTFIXES=OFF

ALTER DATABASE <imported database name> SET COMPATIBILITY_LEVEL = 130;
ALTER DATABASE <imported database name> SET QUERY_STORE = ON;

update [dbo].[SYSSERVICECONFIGURATIONSETTING]
set value ='<tenant ID from existing database>'
where name = 'TENANTID'

update dbo.POWERBICONFIG
set TENANTID = '<tenant ID from existing database>'

update dbo.PROVISIONINGMESSAGETABLE
set TENANTID = '<tenant ID from existing database>'
GO
-- Begin Refresh Retail FullText Catalogs
DECLARE @RFTXNAME NVARCHAR(MAX);
DECLARE @RFTXSQL NVARCHAR(MAX);
DECLARE retail_ftx CURSOR FOR
SELECT OBJECT_SCHEMA_NAME(object_id) + '.' + OBJECT_NAME(object_id) fullname FROM SYS.FULLTEXT_INDEXES
    WHERE FULLTEXT_CATALOG_ID = (SELECT TOP 1 FULLTEXT_CATALOG_ID FROM SYS.FULLTEXT_CATALOGS WHERE NAME = 'COMMERCEFULLTEXTCATALOG');
OPEN retail_ftx;
FETCH NEXT FROM retail_ftx INTO @RFTXNAME;

BEGIN TRY
    WHILE @@FETCH_STATUS = 0  
    BEGIN  
        PRINT 'Refreshing Full Text Index ' + @RFTXNAME;
        EXEC SP_FULLTEXT_TABLE @RFTXNAME, 'activate';
        SET @RFTXSQL = 'ALTER FULLTEXT INDEX ON ' + @RFTXNAME + ' START FULL POPULATION';
        EXEC SP_EXECUTESQL @RFTXSQL;
        FETCH NEXT FROM retail_ftx INTO @RFTXNAME;
    END
END TRY
BEGIN CATCH

PRINT error_message()
END CATCH

CLOSE retail_ftx;  
DEALLOCATE retail_ftx; 
-- End Refresh Retail FullText Catalogs
```

## <a name="synchronize-the-database"></a>データベースの同期

1. リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。 これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。 サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。

    - ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
    - Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)
    - Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)

2. bacpac インポートが行われた AOS コンピューターで、Management Studio の次のスクリプトを実行します。 このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。 この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。

    > [!NOTE]
    > Management Studio の SQL Server 2016 バージョンを使用していることを確認します。

    ```
    ALTER DATABASE [axdb_123456789] MODIFY NAME = [axdb_123456789_original]
    ALTER DATABASE [importeddb] MODIFY NAME = [axdb_123456789]
    ```

3. データベースを同期させます。 管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

    ```
    cd F:\AosService\WebRoot\bin

    Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "F:\AosService\PackagesLocalDirectory" -metadatadir F:\AosService\PackagesLocalDirectory -sqluser axdbadmin -sqlserver <Azure SQL database server name>.database.windows.net -sqldatabase <database name> -setupmode sync -syncmode fullall -isazuresql true -sqlpwd <SQL password> >log.txt 2>&1
    ```

4. services.msc を使用して、以前に停止したサービスを再起動します。

    - ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
    - Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)
    - Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

5. この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。 アプリケーションが予期したとおりに動作することを確認します。 次に、bacpac のインポートを行った AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。

    ```
    DROP DATABASE [axdb_123456789_original]
    ```

### <a name="enable-change-tracking"></a>変更追跡の有効化
ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。
```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。 これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。

### <a name="re-provision-the-target-environment"></a>対象の環境を再プロビジョニング

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a>財務報告データベースのリセット

Management Reporter という以前の名前を持った財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります

## <a name="submit-a-service-request-to-copy-the-database"></a>データベースをコピーするサービス要求を送信

ゴールデン データベースを実稼働環境にコピーするには、LCS に **サンドボックスから実稼働環境** タイプのサービス要求を送信する必要があります。 この要求では、Microsoft がコピー操作を実行することを求めます。

> [!NOTE]
> 要求には実稼働環境へのコピーが含まれるので、**データベースを最新の情報に更新要求** タイプの要求を使用することはできません。

1. LCS のプロジェクト ホーム ページで、**サービス要求** を選択します。
2. **サービス要求** ページで、**追加** を選択し、**サンドボックスから実稼働環境** を選択します。
3. **サンドボックスから実稼働環境** ダイアログ ボックスで、次の手順に従います。

    1. **環境名**フィールドで、実稼動環境を選択します。
    2. **ダウンタイム開始日を優先** および **ダウンタイム終了日を優先** フィールドを設定します。 サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。 要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。
    3. 下部にあるチェック ボックスをオンにして、条項に同意します。

## <a name="additional-steps-for-retail-environments"></a>小売環境の追加手順

環境に、Retail のコンポーネントが含まれている場合、追加の手順を実行して、データベースのインポート後に環境が機能することを保証する必要があります。

### <a name="re-enter-encrypted-and-environment-specific-values-in-the-target-database"></a>ターゲット データベースの暗号化された環境固有の値を再入力

次のページの値は、データベースで暗号化されています。 したがって、インポートされた値はすべて正しくありません。

- 支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。
- ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)

ターゲット システムで、これらのページを開き、前に記録した値を入力します。

## <a name="re-enter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a>ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力

Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。 次のフィールドが影響されます。 フィールド名は Table.Field 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは DIXF で使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。 |
| SysEmailSMPTPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

## <a name="known-issues-and-limitations"></a>既知の問題と制限事項

### <a name="i-cant-download-the-management-studio-installer"></a>Management Studio インストーラーをダウンロードできません

Management Studio インストーラーをダウンロードしようとすると、次のメッセージが表示される場合があります。

> 現在のセキュリティ設定では、このファイルをダウンロードすることはできません。

この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。

1. Web ブラウザーで**インターネット オプション**を開きます。
2. **セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。
3. **ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。

### <a name="performance"></a>パフォーマンス

次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。

- 常に Azure SQL データベース インスタンスと同じ Azure データ センター内にあるコンピューターからエクスポートします。 実際、このガイドラインはサンドボックス データベースのコピーをエクスポートするときに、サンドボックス AOS コンピューターからエクスポートする必要があることを意味します。
- 常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。 リモート コンピューターで Management Studio からインポートしないでください。
- Azure でホストされている 1 ボックス環境では、エクスポートするときに D ドライブに .bacpac ファイルを配置します。 (ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure コンピューター 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) Azure サポート チームのブログ投稿を参照してください。
- SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/library/ms175935.aspx) を実行するアカウントに権限を付与します。 この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。 開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。
- Management Studio の Azure SQL データベースからエクスポートおよびインポートするオプションを使用しないことをお勧めします。 (このオプションは、**データ層アプリケーションのエクスポート**とも呼ばれます。) 大規模なデータベースにはメモリーの制限があるため、このオプションは使用しないでください。
