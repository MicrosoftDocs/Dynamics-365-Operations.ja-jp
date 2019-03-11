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
ms.openlocfilehash: 62e0d3fcea6c1de70c6d2a328c5395befa891f16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368951"
---
# <a name="export-copies-of-finance-and-operations-databases-to-restore-later"></a><span data-ttu-id="cff07-103">後で復元する Finance and Operations のデータベースのコピーをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="cff07-103">Export copies of Finance and Operations databases to restore later</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cff07-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースをファイルにエクスポートしてから、そのファイルをアプリケーションの同じインスタンスかまたは別のインスタンスに再インポートする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cff07-104">This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database to a file, and then reimport that file into the same instance or another instance of the application.</span></span> <span data-ttu-id="cff07-105">このステップは、非実稼働環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cff07-105">This procedure can be used only in non-production environments.</span></span>

> [!NOTE]
> <span data-ttu-id="cff07-106">このトピックは、サンド ボックスのユーザー受け入れテスト (UAT) 環境に接続されている Microsoft Azure SQL データベースに適用されます。</span><span class="sxs-lookup"><span data-stu-id="cff07-106">This topic applies to Microsoft Azure SQL databases that are connected to sandbox user acceptance testing (UAT) environments.</span></span>

<span data-ttu-id="cff07-107">Finance and Operations データベース プロセスのコピーを保持する場合がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="cff07-107">There are several situations where you might want to keep a copy of a Finance and Operations database process:</span></span>

- <span data-ttu-id="cff07-108">後で復元できる戦略的なバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff07-108">You want to make strategic backups that you can restore to later.</span></span> <span data-ttu-id="cff07-109">たとえば、主要コード更新の前または後に、後に参照に使用できるようコピーします。</span><span class="sxs-lookup"><span data-stu-id="cff07-109">For example, before or after a major code update, you might want copies that you can use for reference later.</span></span>
- <span data-ttu-id="cff07-110">破壊試験の前にデータベースをバックアップし、テストの完了後にデータベースを復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff07-110">You want to back up a database before destructive testing and then restore it after the testing is completed.</span></span>
- <span data-ttu-id="cff07-111">Finance and Operations の新しいメジャー リリースへのアップグレードのとき、このプロセスを使用して、古いテスト データベースをエクスポートし、新しいバージョンに持ち出すことができます。</span><span class="sxs-lookup"><span data-stu-id="cff07-111">When you upgrade to a new major release of Finance and Operations, you can use this process to export your old test database and bring it forward to the new version.</span></span>

<span data-ttu-id="cff07-112">Microsoft は Azure SQL データベース環境を過去 35 日間以内の特定の時点に復元できる標準機能も提供しています。</span><span class="sxs-lookup"><span data-stu-id="cff07-112">Be aware that Microsoft also provides a standard feature that lets you restore an Azure SQL database environment to a specific point in time within the last 35 days.</span></span> <span data-ttu-id="cff07-113">この復元はサービス要求を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="cff07-113">This restore is done via a service request.</span></span> <span data-ttu-id="cff07-114">詳細については、[非実稼働環境でのポイントインタイム データベース復元の要求](request-point-in-time-restore.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cff07-114">For more information, see [Request a point-in-time database restore on a non-production environment](request-point-in-time-restore.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cff07-115">このプロセスでは、レベル 2 以上の環境でリモート デスクトップへのアクセスを必要としていましたが、必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="cff07-115">This process used to require Remote Desktop access on your Tier-2 or higher environments but no longer does.</span></span> <span data-ttu-id="cff07-116">これらの操作を実行するには、Lifecycle Services でセルフ サービス アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="cff07-116">These operations can be performed using the Self-service actions in Lifecycle Services.</span></span>

## <a name="self-service-database-export"></a><span data-ttu-id="cff07-117">データベースのセルフ サービス エクスポート</span><span class="sxs-lookup"><span data-stu-id="cff07-117">Self-service database export</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-finance-and-operations-database"></a><span data-ttu-id="cff07-118">Finance and Operations データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="cff07-118">Import the Finance and Operations database</span></span>

### <a name="stop-services"></a><span data-ttu-id="cff07-119">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="cff07-119">Stop services</span></span>

<span data-ttu-id="cff07-120">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="cff07-120">Use Remote Desktop to connect to all the computers in the environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="cff07-121">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="cff07-121">These services will have open connections to the Finance and Operations database.</span></span>

- <span data-ttu-id="cff07-122">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="cff07-122">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="cff07-123">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-123">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="cff07-124">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-124">Management Reporter 2012 Process Service (on BI computers only)</span></span>

### <a name="import-the-bacpac-file"></a><span data-ttu-id="cff07-125">.bacpac ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="cff07-125">Import the .bacpac file</span></span>

<span data-ttu-id="cff07-126">エクスポート ステップ中に生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</span><span class="sxs-lookup"><span data-stu-id="cff07-126">Copy the .bacpac file that was generated during the export step to the AOS computer in the target environment.</span></span> <span data-ttu-id="cff07-127">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cff07-127">For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</span></span>

<span data-ttu-id="cff07-128">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff07-128">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure DSQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=<See below>
```

<span data-ttu-id="cff07-129">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="cff07-129">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="cff07-130">**tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="cff07-130">**tsn (target server name)** – The name of the Azure SQL Database server to import into.</span></span> <span data-ttu-id="cff07-131">名前はデータベース アカウントの環境ページの LCS で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cff07-131">You can find the name in LCS on the environment page under Database Accounts.</span></span> <span data-ttu-id="cff07-132">接尾語 **database.windows.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="cff07-132">Add the suffix **database.windows.net** to it.</span></span>
- <span data-ttu-id="cff07-133">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="cff07-133">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="cff07-134">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="cff07-134">The database should **not** already exist.</span></span> <span data-ttu-id="cff07-135">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cff07-135">The import process will create it.</span></span>
- <span data-ttu-id="cff07-136">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="cff07-136">**sf (source file)** – The path and name of the file to import from.</span></span>
- <span data-ttu-id="cff07-137">**tu(ターゲット ユーザー)** – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="cff07-137">**tu (target user)** – The SQL user name for the target Azure SQL database instance.</span></span> <span data-ttu-id="cff07-138">標準の **sqladmin** ユーザーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cff07-138">We recommend that you use the standard **sqladmin** user.</span></span> <span data-ttu-id="cff07-139">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cff07-139">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="cff07-140">**tp(ターゲット パスワード)** – ターゲットの Azure SQL データベース ユーザーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="cff07-140">**tp (target password)** – The password for the target Azure SQL database user.</span></span>
- <span data-ttu-id="cff07-141">**DatabaseServiceObjective** – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="cff07-141">**DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2 or P4.</span></span> <span data-ttu-id="cff07-142">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</span><span class="sxs-lookup"><span data-stu-id="cff07-142">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="cff07-143">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff07-143">To query the service level objective of the current database, run the following query.</span></span>

    ```
    SELECT  d.name,   
        slo.*    
    FROM sys.databases d   
    JOIN sys.database_service_objectives slo    
    ON d.database_id = slo.database_id;  
    ```

### <a name="run-a-script-to-update-the-finance-and-operations-database"></a><span data-ttu-id="cff07-144">Finance and Operations データベースを更新するスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="cff07-144">Run a script to update the Finance and Operations database</span></span>

<span data-ttu-id="cff07-145">ソースとターゲット環境の SQL ユーザーのパスワードが異なる場合は、次のスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff07-145">If the source and target environments have different SQL user passwords, you must run the following script.</span></span> <span data-ttu-id="cff07-146">パスワードとは異なるかどうかが不明な場合は、このスクリプトを実行することも必要です。</span><span class="sxs-lookup"><span data-stu-id="cff07-146">You must also run this script if you aren't sure whether the passwords differ.</span></span> <span data-ttu-id="cff07-147">インポートされたデータベースに対して、スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff07-147">Run the script against the imported database.</span></span> <span data-ttu-id="cff07-148">スクリプトは、データベース ユーザーを削除してから、ターゲット環境の正しいパスワードを持つように再作成します。</span><span class="sxs-lookup"><span data-stu-id="cff07-148">The script drops the database users and then re-creates them so that they have the correct passwords for the target environment.</span></span>

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
## <a name="synchronize-the-database"></a><span data-ttu-id="cff07-149">データベースの同期</span><span class="sxs-lookup"><span data-stu-id="cff07-149">Synchronize the database</span></span>

1. <span data-ttu-id="cff07-150">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="cff07-150">Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="cff07-151">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="cff07-151">These services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="cff07-152">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="cff07-152">After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</span></span>

    - <span data-ttu-id="cff07-153">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="cff07-153">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="cff07-154">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-154">Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="cff07-155">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-155">Management Reporter 2012 Process service (on business intelligence \[BI\] computers only)</span></span>

2. <span data-ttu-id="cff07-156">bacpac インポートが実行された AOS コンピューターで、Management Studio の次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff07-156">On the AOS computer where the bacpac import was performed, run the following script in Management Studio.</span></span> <span data-ttu-id="cff07-157">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="cff07-157">This script renames the original database and then renames the newly imported database so that it uses the original database name.</span></span> <span data-ttu-id="cff07-158">この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</span><span class="sxs-lookup"><span data-stu-id="cff07-158">In this example, the original database was named axdb\_123456789, and the newly imported database was named importeddb.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cff07-159">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cff07-159">Make sure that you're using the SQL Server 2016 version of Management Studio.</span></span>

    ```
    ALTER DATABASE [axdb_123456789] MODIFY NAME = [axdb_123456789_original]
    ALTER DATABASE [importeddb] MODIFY NAME = [axdb_123456789]
    ```

3. <span data-ttu-id="cff07-160">データベースを同期させます。</span><span class="sxs-lookup"><span data-stu-id="cff07-160">Synchronize the database.</span></span> <span data-ttu-id="cff07-161">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff07-161">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

    ```
    cd F:\AosService\WebRoot\bin

    Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "F:\AosService\PackagesLocalDirectory" -metadatadir F:\AosService\PackagesLocalDirectory -sqluser axdbadmin -sqlserver <Azure SQL database server name>.database.windows.net -sqldatabase <database name> -setupmode sync -syncmode fullall -isazuresql true -sqlpwd <SQL password> >log.txt 2>&1
    ```

4. <span data-ttu-id="cff07-162">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="cff07-162">Use services.msc to restart the services that you stopped earlier:</span></span>

    - <span data-ttu-id="cff07-163">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="cff07-163">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="cff07-164">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピューター上のみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-164">Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="cff07-165">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="cff07-165">Management Reporter 2012 Process service (on BI computers only)</span></span>

5. <span data-ttu-id="cff07-166">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="cff07-166">At this point, you can open the Finance and Operations application URL and sign in.</span></span> <span data-ttu-id="cff07-167">アプリケーションが予期したとおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="cff07-167">Verify that the application works as you expect.</span></span> <span data-ttu-id="cff07-168">次に、bacpac のインポートを実行した AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</span><span class="sxs-lookup"><span data-stu-id="cff07-168">Then drop the original database by running the following script in Management Studio on the AOS computer where you performed the bacpac import.</span></span>

    ```
    DROP DATABASE [axdb_123456789_original]
    ```


### <a name="re-provision-retail-components-in-the-target-environment"></a><span data-ttu-id="cff07-169">対象となる環境で Retail コンポーネントを再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="cff07-169">Re-provision Retail components in the target environment</span></span>

<span data-ttu-id="cff07-170">データベースを別の環境で復元またはインポートする場合のみ再プロビジョニングが必要です。</span><span class="sxs-lookup"><span data-stu-id="cff07-170">Reprovisioning is only required if you are restoring or importing the database on another environment.</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="limitations"></a><span data-ttu-id="cff07-171">制限</span><span class="sxs-lookup"><span data-stu-id="cff07-171">Limitations</span></span>
<span data-ttu-id="cff07-172">データベースをインポートすると、Azure Blob Storage に保管されているデータベースおよびドキュメント処理のドキュメント間のリンクが破損している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cff07-172">After you import a database, the link between the database and document handling documents that are stored in Azure blob storage might be broken.</span></span> <span data-ttu-id="cff07-173">X++ **FileUpload** クラスを使用して BLOB ストレージにファイルを格納するカスタム コードがある場合、それらのファイルへのリンクも壊れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cff07-173">If you have custom code that uses the X++ **FileUpload** class to put files in blob storage, the links to those files might also be broken.</span></span>
