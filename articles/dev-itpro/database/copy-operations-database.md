---
title: 後で復元する Finance and Operations のデータベースのコピーをエクスポートする
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースをファイルにエクスポートしてから、そのファイルをアプリケーションの同じインスタンスかまたは別のインスタンスに再インポートする方法を説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 12/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 269254
ms.assetid: 7464b180-8ace-4b65-8b53-ba608d0611e1
ms.search.region: Global
ms.author: LaneSwenka
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: c6aa023502ed05a58e1cb2eb8a0cea3e9d1dac08
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537110"
---
# <a name="export-copies-of-finance-and-operations-databases-to-restore-later"></a>後で復元する Finance and Operations のデータベースのコピーをエクスポートする

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースをファイルにエクスポートしてから、そのファイルをアプリケーションの同じインスタンスかまたは別のインスタンスに再インポートする方法を説明します。 このステップは、非実稼働環境でのみ使用できます。

> [!NOTE]
> このトピックは、サンド ボックスのユーザー受け入れテスト (UAT) 環境に接続されている Microsoft Azure SQL データベースに適用されます。

Finance and Operations データベース プロセスのコピーを保持する場合がいくつかあります。

- 後で復元できる戦略的なバックアップを作成する必要があります。 たとえば、主要コード更新の前または後に、後に参照に使用できるようコピーします。
- 破壊試験の前にデータベースをバックアップし、テストの完了後にデータベースを復元する必要があります。
- Finance and Operations の新しいメジャー リリースへのアップグレードのとき、このプロセスを使用して、古いテスト データベースをエクスポートし、新しいバージョンに持ち出すことができます。

Microsoft は Azure SQL データベース環境を過去 35 日間以内の特定の時点に復元できる標準機能も提供しています。 この復元はサービス要求を介して行われます。 詳細については、[非実稼働環境でのポイントインタイム データベース復元の要求](request-point-in-time-restore.md) を参照してください。

> [!NOTE]
> このプロセスでは、レベル 2 以上の環境でリモート デスクトップへのアクセスを必要としていましたが、必要なくなりました。 これらの操作を実行するには、Lifecycle Services でセルフ サービス アクションを使用します。

## <a name="self-service-database-export"></a>データベースのセルフ サービス エクスポート

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-finance-and-operations-database"></a>Finance and Operations データベースのインポート

### <a name="stop-services"></a>サービスの停止

リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。 これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。

- ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)
- Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)
- Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)

### <a name="import-the-bacpac-file"></a>.bacpac ファイルのインポート

エクスポート ステップ中に生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。 パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。

管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure DSQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=<See below>
```

パラメータの説明を以下に示します。

- **tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。 名前はデータベース アカウントの環境ページの LCS で見つけることができます。 接尾語 **database.windows.net** を追加します。
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

### <a name="run-a-script-to-update-the-finance-and-operations-database"></a>Finance and Operations データベースを更新するスクリプトを実行する

ソースとターゲット環境の SQL ユーザーのパスワードが異なる場合は、次のスクリプトを実行する必要があります。 パスワードとは異なるかどうかが不明な場合は、このスクリプトを実行することも必要です。 インポートされたデータベースに対して、スクリプトを実行します。 スクリプトは、データベース ユーザーを削除してから、ターゲット環境の正しいパスワードを持つように再作成します。

```
ALTER AUTHORIZATION ON Fulltext Catalog::[<name of the full text catalog in your database] TO [dbo];

declare @userSQL varchar(1000)
set quoted_identifier off

declare userCursor CURSOR for
select 'DROP USER ' + name
from sys.sysusers
where issqlrole = 0 and hasdbaccess = 1 and name <> 'dbo'

OPEN userCursor
FETCH userCursor into @userSQL
WHILE @@Fetch_Status = 0
BEGIN
exec(@userSQL)
FETCH userCursor into @userSQL
END
CLOSE userCursor
DEALLOCATE userCursor

CREATE USER axdeployuser FROM LOGIN axdeployuser
EXEC sp_addrolemember 'db_owner', 'axdeployuser'

CREATE USER axdbadmin WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'db_owner', 'axdbadmin'

CREATE USER axruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'db_datareader', 'axruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axruntimeuser'

CREATE USER axmrruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'ReportingIntegrationUser', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datareader', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axmrruntimeuser'

CREATE USER axretaildatasyncuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'DataSyncUsersRole', 'axretaildatasyncuser'

CREATE USER axretailruntimeuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'UsersRole', 'axretailruntimeuser'
EXEC sp_addrolemember 'ReportUsersRole', 'axretailruntimeuser'

CREATE USER axdeployextuser WITH PASSWORD = '<password from LCS>'
EXEC sp_addrolemember 'DeployExtensibilityRole', 'axdeployextuser'



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

2. bacpac インポートが実行された AOS コンピューターで、Management Studio の次のスクリプトを実行します。 このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。 この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。

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

5. この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。 アプリケーションが予期したとおりに動作することを確認します。 次に、bacpac のインポートを実行した AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。

    ```
    DROP DATABASE [axdb_123456789_original]
    ```


### <a name="re-provision-retail-components-in-the-target-environment"></a>対象となる環境で Retail コンポーネントを再プロビジョニング

データベースを別の環境で復元またはインポートする場合のみ再プロビジョニングが必要です。

[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="limitations"></a>制限
データベースをインポートすると、Azure Blob Storage に保管されているデータベースおよびドキュメント処理のドキュメント間のリンクが破損している可能性があります。 X++ **FileUpload** クラスを使用して BLOB ストレージにファイルを格納するカスタム コードがある場合、それらのファイルへのリンクも壊れる可能性があります。
