---
title: 標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベース エクスポート シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a1e4fb959d89ab135954e811d8055bb1a9aa9eeb
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/14/2019
ms.locfileid: "842953"
---
# <a name="export-a-copy-of-the-standard-user-acceptance-testing-uat-database"></a><span data-ttu-id="f37f5-103">標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート</span><span class="sxs-lookup"><span data-stu-id="f37f5-103">Export a copy of the standard user acceptance testing (UAT) database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f37f5-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="f37f5-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="f37f5-105">このチュートリアルでは、サンドボックス標準ユーザー受け入れテスト (UAT) からすべてのデータおよびトランザクションをエクスポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-105">This tutorial shows how to export all the data and transactions from a sandbox standard user acceptance testing (UAT) environment.</span></span>

<span data-ttu-id="f37f5-106">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-106">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="f37f5-107">UAT 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-107">Refresh the UAT environment.</span></span>
> * <span data-ttu-id="f37f5-108">Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリへのエクスポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-108">Run the export to the Asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
> * <span data-ttu-id="f37f5-109">データベース バックアップをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-109">Download the database backup.</span></span>
> * <span data-ttu-id="f37f5-110">データベースをインポートし、開発者環境で使用できるようにそれを準備します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-110">Import the database, and prepare it so that it can be used in a developer environment.</span></span>

<span data-ttu-id="f37f5-111">このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations を既に稼働している顧客が、開発環境に生産トランザクションの最新のコピーを読み込もうとしています。</span><span class="sxs-lookup"><span data-stu-id="f37f5-111">As an example of this scenario, a customer who has already gone live with Microsoft Dynamics 365 for Finance and Operations wants to load a recent copy of production transactions into his or her development environment.</span></span> <span data-ttu-id="f37f5-112">これにより、顧客は特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-112">In this way, the customer will be able to debug specific transactions, or develop new features and reports by using realistic datasets.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="f37f5-113">既知の制限</span><span class="sxs-lookup"><span data-stu-id="f37f5-113">Known limitations</span></span>

<span data-ttu-id="f37f5-114">Microsoft Azure SQL データベース プラットフォームによる最新の制限があるため、200 GB よりも大きい場合はデータベースのエクスポートをお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f37f5-114">Because of recent restrictions by the Microsoft Azure SQL Database platform, we don't recommend that you export your database if it's larger than 200 gigabytes (GB).</span></span> <span data-ttu-id="f37f5-115">大規模なデータベースをエクスポートする必要がある場合、SQL データベースが大規模なエクスポートをサポートするまで[レガシー ドキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/b86878500e79f0fe0488c9aedf3fd38b30749fd4/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-115">If you must export a larger database, we recommend that you use the [legacy documentation](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/b86878500e79f0fe0488c9aedf3fd38b30749fd4/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md) until SQL Database can support larger exports.</span></span> <span data-ttu-id="f37f5-116">この推奨事項は、更新操作ではなくエクスポート操作に適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f37f5-116">Note that this recommendation applies to export operations, not refresh operations.</span></span> <span data-ttu-id="f37f5-117">更新操作は、サイズが最大 4 TB のデータベースをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-117">Refresh operations can support databases that are up to 4 terabytes (TB) in size.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f37f5-118">必要条件</span><span class="sxs-lookup"><span data-stu-id="f37f5-118">Prerequisites</span></span>

<span data-ttu-id="f37f5-119">更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-119">To do a refresh operation, you must have your production environment deployed, or you must have a minimum of two standard UAT environments.</span></span> <span data-ttu-id="f37f5-120">このチュートリアルを完了するには、開発者環境が配置されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-120">To complete this tutorial, you must have a developer environment deployed.</span></span>

## <a name="refresh-the-uat-environment"></a><span data-ttu-id="f37f5-121">UAT 環境を更新</span><span class="sxs-lookup"><span data-stu-id="f37f5-121">Refresh the UAT environment</span></span>

<span data-ttu-id="f37f5-122">この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-122">This refresh operation overwrites the UAT environment with the latest copy of the production database.</span></span> <span data-ttu-id="f37f5-123">この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f37f5-123">To complete this step, follow the instructions in [Refresh for training purposes](dbmovement-scenario-general-refresh.md).</span></span>

## <a name="back-up-to-the-asset-library"></a><span data-ttu-id="f37f5-124">資産ライブラリへのバックアップ</span><span class="sxs-lookup"><span data-stu-id="f37f5-124">Back up to the Asset Library</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-database"></a><span data-ttu-id="f37f5-125">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="f37f5-125">Import the database</span></span>

<span data-ttu-id="f37f5-126">データベース バックアップ (.bacpac) ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-126">After you've downloaded a database backup (.bacpac) file, you can begin the manual import operation on your Tier 1 environment.</span></span> <span data-ttu-id="f37f5-127">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-127">When you import the database, we recommend that you follow these guidelines:</span></span>

- <span data-ttu-id="f37f5-128">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-128">Keep a copy of the existing AxDB database, so that you can revert to it later if you must.</span></span>
- <span data-ttu-id="f37f5-129">**AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-129">Import the new database under a new name, such as **AxDB\_fromProd**.</span></span>

<span data-ttu-id="f37f5-130">最高のパフォーマンスを保証するには、\*.bacpac ファイルをインポート元のローカル コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-130">To help guarantee the best performance, copy the \*.bacpac file to the local computer that you're importing from.</span></span> <span data-ttu-id="f37f5-131">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-131">Open a **Command Prompt** window, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

<span data-ttu-id="f37f5-132">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-132">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="f37f5-133">**tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="f37f5-133">**tsn (target server name)** – The name of the Microsoft SQL Server instance to import into.</span></span>
- <span data-ttu-id="f37f5-134">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="f37f5-134">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="f37f5-135">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="f37f5-135">The database should **not** already exist.</span></span>
- <span data-ttu-id="f37f5-136">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="f37f5-136">**sf (source file)** – The path and name of the file to import from.</span></span>

> [!NOTE]
> <span data-ttu-id="f37f5-137">インポート中に、ユーザー名およびパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f37f5-137">During import, the user name and password aren't required.</span></span> <span data-ttu-id="f37f5-138">既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-138">By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</span></span>

## <a name="update-the-database"></a><span data-ttu-id="f37f5-139">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="f37f5-139">Update the database</span></span>

<span data-ttu-id="f37f5-140">インポートされたデータベースに対して、次の SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-140">Run the following SQL script against the imported database.</span></span> <span data-ttu-id="f37f5-141">このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL Server インスタンスの SQL のログインに正しくリンクします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-141">This script adds back the users that you deleted from the source database and correctly links them to the SQL logins for this SQL Server instance.</span></span> <span data-ttu-id="f37f5-142">スクリプトはまた、変更の追跡を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-142">The script also turns change tracking back on.</span></span> <span data-ttu-id="f37f5-143">必ず、データベースの名前を使用できるように、最後の **ALTER DATABASE** ステートメントを編集してください。</span><span class="sxs-lookup"><span data-stu-id="f37f5-143">Remember to edit the final **ALTER DATABASE** statement so that it uses the name of your database.</span></span>

```
CREATE USER axdeployuser FROM LOGIN axdeployuser
EXEC sp_addrolemember 'db_owner', 'axdeployuser'

CREATE USER axdbadmin FROM LOGIN axdbadmin
EXEC sp_addrolemember 'db_owner', 'axdbadmin'

CREATE USER axmrruntimeuser FROM LOGIN axmrruntimeuser
EXEC sp_addrolemember 'db_datareader', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axmrruntimeuser'

CREATE USER axretaildatasyncuser FROM LOGIN axretaildatasyncuser
EXEC sp_addrolemember 'DataSyncUsersRole', 'axretaildatasyncuser'

CREATE USER axretailruntimeuser FROM LOGIN axretailruntimeuser
EXEC sp_addrolemember 'UsersRole', 'axretailruntimeuser'
EXEC sp_addrolemember 'ReportUsersRole', 'axretailruntimeuser'

CREATE USER axdeployextuser FROM LOGIN axdeployextuser
EXEC sp_addrolemember 'DeployExtensibilityRole', 'axdeployextuser'

CREATE USER [NT AUTHORITY\NETWORK SERVICE] FROM LOGIN [NT AUTHORITY\NETWORK SERVICE]
EXEC sp_addrolemember 'db_owner', 'NT AUTHORITY\NETWORK SERVICE'

UPDATE T1
SET T1.storageproviderid = 0
    , T1.accessinformation = ''
    , T1.modifiedby = 'Admin'
    , T1.modifieddatetime = getdate()
FROM docuvalue T1
WHERE T1.storageproviderid = 1 --Azure storage

DROP PROCEDURE IF EXISTS SP_ConfigureTablesForChangeTracking
DROP PROCEDURE IF EXISTS SP_ConfigureTablesForChangeTracking_V2
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

### <a name="turn-on-change-tracking"></a><span data-ttu-id="f37f5-144">変更追跡を有効にする</span><span class="sxs-lookup"><span data-stu-id="f37f5-144">Turn on change tracking</span></span>

<span data-ttu-id="f37f5-145">ソース データベースで変更追跡が有効になっている場合は、ターゲット環境の新たなプロビジョニング データベースで有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="f37f5-145">If change tracking was turned on in the source database, be sure to turn it on in the newly provisioned database in the target environment.</span></span> <span data-ttu-id="f37f5-146">変更追跡を有効にするには、**ALTER DATABASE** コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-146">To turn on change tracking, use the **ALTER DATABASE** command.</span></span>

```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

<span data-ttu-id="f37f5-147">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを保証するには、データ管理のデータ エンティティの変更追跡をオンまたはオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-147">To help guarantee that the current version of the store procedure that is related to change tracking is used in the new database, you must turn change tracking on or off for a data entity in Data management.</span></span> <span data-ttu-id="f37f5-148">任意のエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-148">You can choose any entity.</span></span> <span data-ttu-id="f37f5-149">ストアド プロシージャの更新を起動するには、この手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="f37f5-149">This step is required in order to trigger a refresh of the store procedure.</span></span>

## <a name="start-to-use-the-new-database"></a><span data-ttu-id="f37f5-150">新しいデータベースの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-150">Start to use the new database</span></span>

<span data-ttu-id="f37f5-151">環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-151">To switch environments and use the new database, first stop the following services:</span></span>

- <span data-ttu-id="f37f5-152">World Wide Web 公開サービス</span><span class="sxs-lookup"><span data-stu-id="f37f5-152">World Wide Web Publishing Service</span></span>
- <span data-ttu-id="f37f5-153">Microsoft Dynamics 365 Unified Operations: バッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="f37f5-153">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="f37f5-154">Management Reporter 2012 処理サービス</span><span class="sxs-lookup"><span data-stu-id="f37f5-154">Management Reporter 2012 Process Service</span></span>

<span data-ttu-id="f37f5-155">これらのサービスが停止した後、AxDB データベース **AxDB\_orig** の名前を変更し、新しくインポートしたデータベース **AxDB** の名前を変更し、そして 3 つのサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-155">After these services have been stopped, rename the AxDB database **AxDB\_orig**, rename your newly imported database **AxDB**, and then restart the three services.</span></span>

<span data-ttu-id="f37f5-156">元のデータベースに戻すには、このプロセスを逆にします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-156">To switch back to the original database, reverse this process.</span></span> <span data-ttu-id="f37f5-157">つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-157">In other words, stop the services, rename the databases, and then restart the services.</span></span>

### <a name="reprovision-the-target-environment"></a><span data-ttu-id="f37f5-158">対象の環境を再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="f37f5-158">Reprovision the target environment</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a><span data-ttu-id="f37f5-159">財務報告データベースのリセット</span><span class="sxs-lookup"><span data-stu-id="f37f5-159">Reset the Financial Reporting database</span></span>

<span data-ttu-id="f37f5-160">財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-160">If you're using Financial Reporting, you must reset the Financial Reporting database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span> <span data-ttu-id="f37f5-161">(財務報告は以前は Management Reporter という名前でした)</span><span class="sxs-lookup"><span data-stu-id="f37f5-161">(Financial Reporting was previously named Management Reporter.)</span></span>

## <a name="reenter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a><span data-ttu-id="f37f5-162">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</span><span class="sxs-lookup"><span data-stu-id="f37f5-162">Reenter data from encrypted and environment-specific fields in the target database</span></span>

<span data-ttu-id="f37f5-163">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-163">In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</span></span> <span data-ttu-id="f37f5-164">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-164">The following fields are affected.</span></span> <span data-ttu-id="f37f5-165">フィールド名は *Table.Field* 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-165">The field names are given in *Table.Field* format.</span></span>

| <span data-ttu-id="f37f5-166">フィールド名</span><span class="sxs-lookup"><span data-stu-id="f37f5-166">Field name</span></span>                                               | <span data-ttu-id="f37f5-167">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="f37f5-167">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="f37f5-168">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="f37f5-168">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="f37f5-169">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-169">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="f37f5-170">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="f37f5-170">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="f37f5-171">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-171">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="f37f5-172">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="f37f5-172">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="f37f5-173">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-173">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="f37f5-174">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="f37f5-174">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="f37f5-175">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-175">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="f37f5-176">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="f37f5-176">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="f37f5-177">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-177">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="f37f5-178">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-178">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="f37f5-179">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="f37f5-179">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="f37f5-180">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="f37f5-180">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="f37f5-181">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。</span><span class="sxs-lookup"><span data-stu-id="f37f5-181">It was previously in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="f37f5-182">SysEmailSMTPPassword.Password</span><span class="sxs-lookup"><span data-stu-id="f37f5-182">SysEmailSMTPPassword.Password</span></span>                            | <span data-ttu-id="f37f5-183">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-183">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="f37f5-184">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="f37f5-184">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="f37f5-185">このフィールドは、アプリケーション オブジェクト サーバー (AOS) により内部で使用されています。</span><span class="sxs-lookup"><span data-stu-id="f37f5-185">This field is used internally by Application Object Server (AOS).</span></span> <span data-ttu-id="f37f5-186">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-186">It can be ignored.</span></span> |
| <span data-ttu-id="f37f5-187">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="f37f5-187">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="f37f5-188">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-188">This field is used internally by AOS.</span></span> <span data-ttu-id="f37f5-189">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-189">It can be ignored.</span></span> |

## <a name="community-tools"></a><span data-ttu-id="f37f5-190">コミュニティ ツール</span><span class="sxs-lookup"><span data-stu-id="f37f5-190">Community tools</span></span>

<span data-ttu-id="f37f5-191">開発者環境にバックアップ ファイルをインポートするための他のツールをお探しですか。</span><span class="sxs-lookup"><span data-stu-id="f37f5-191">Are you looking for more tools to help you import backup files into your developer environments?</span></span> <span data-ttu-id="f37f5-192">他の情報源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-192">Here are some other sources of information:</span></span>

* <span data-ttu-id="f37f5-193">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) には、コミュニティによって作成された多くの貴重なツールがあります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-193">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) provides many valuable tools that have been created by the community.</span></span>
* <span data-ttu-id="f37f5-194">[GitHub でコミュニティによって提供されたオープン ソース プロジェクト](https://github.com/search?q=dynamics+365+finance+operations&s=stars)。</span><span class="sxs-lookup"><span data-stu-id="f37f5-194">[Community-provided open source projects on GitHub](https://github.com/search?q=dynamics+365+finance+operations&s=stars).</span></span>

## <a name="known-issues"></a><span data-ttu-id="f37f5-195">既知の問題</span><span class="sxs-lookup"><span data-stu-id="f37f5-195">Known issues</span></span>

### <a name="the-export-database-is-in-a-preparation-failed-state"></a><span data-ttu-id="f37f5-196">エクスポート データベースが「準備に失敗しました」状態</span><span class="sxs-lookup"><span data-stu-id="f37f5-196">The export database is in a "Preparation failed" state</span></span>

<span data-ttu-id="f37f5-197">LCS からのオートメーションがタイムアウトした場合、エクスポート データベースの状態が **準備に失敗しました** に変わります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-197">If the automation from LCS times out, the state of the export database is changed to **Preparation failed**.</span></span> <span data-ttu-id="f37f5-198">アセット ライブラリにエクスポートするエクスポート操作は、引き続き SQL データベースで実行されています。</span><span class="sxs-lookup"><span data-stu-id="f37f5-198">The export operation to export to the Asset library is still running in SQL Database.</span></span> <span data-ttu-id="f37f5-199">この問題を解決するには、**再開** を使用してプロセスと SQL データベースを再接続できます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-199">To resolve this issue, you can use the **Resume** button to reconnect the process with SQL Database.</span></span> <span data-ttu-id="f37f5-200">その後、プロセスが正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-200">The process should then be successfully completed.</span></span>

### <a name="the-export-database-takes-a-very-long-time"></a><span data-ttu-id="f37f5-201">エクスポート データベースに時間が非常にかかる</span><span class="sxs-lookup"><span data-stu-id="f37f5-201">The export database takes a very long time</span></span>

<span data-ttu-id="f37f5-202">最近、Azure SQL チームは、サイズが 200 GB を超えるデータベースの場合、LCS が使用するインポート/エクスポート アプリケーション プログラミング インターフェイス (API) の実行時間が変化すると発表しました。</span><span class="sxs-lookup"><span data-stu-id="f37f5-202">The Azure SQL team recently announced that the Import/Export application programming interface (API) that LCS uses has variable execution times for any database that is over 200 GB in size.</span></span> <span data-ttu-id="f37f5-203">この問題が発生した場合、[UAT データベースに直接 DevTest 環境を接続](dbmovement-scenario-debugdiag.md)するか、[レガシー ドキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/b86878500e79f0fe0488c9aedf3fd38b30749fd4/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)に従うことができます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-203">If you encounter this issue, you can either [connect your DevTest environment directly to the UAT database](dbmovement-scenario-debugdiag.md) or follow the [legacy documentation](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/b86878500e79f0fe0488c9aedf3fd38b30749fd4/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md).</span></span> <span data-ttu-id="f37f5-204">ポイントインタイム復元機能が使用可能であり、環境に含まれているため、バックアップ目的でデータベースをエクスポートすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="f37f5-204">We don't recommend that you export databases for backup purposes, because the Point-in-time restore functionality is available and included with your environment.</span></span>

<span data-ttu-id="f37f5-205">Lifecycle Services チームは、インポート/エクスポート API のパフォーマンスを改善するために Azure SQL チームと直接協力しており、LCS の将来のリリースで修正する予定です。</span><span class="sxs-lookup"><span data-stu-id="f37f5-205">The Lifecycle Services team is working directly with the Azure SQL team to increase the performance of the Import/Export API and will make improvements in upcoming releases of LCS.</span></span>

### <a name="i-cant-download-management-studio-installation-files"></a><span data-ttu-id="f37f5-206">Management Studio インストール ファイルをダウンロードできません</span><span class="sxs-lookup"><span data-stu-id="f37f5-206">I can't download Management Studio installation files</span></span>

<span data-ttu-id="f37f5-207">Microsoft SQL Server Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-207">When you try to download the Microsoft SQL Server Management Studio installer, you might receive the following error message:</span></span>

> <span data-ttu-id="f37f5-208">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f37f5-208">Your current security settings do not allow this file to be downloaded.</span></span>

<span data-ttu-id="f37f5-209">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-209">To work around this issue, follow these steps to enable file downloads.</span></span>

1. <span data-ttu-id="f37f5-210">Web ブラウザーで**インターネット オプション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-210">In your web browser, open **Internet options**.</span></span>
2. <span data-ttu-id="f37f5-211">**セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-211">On the **Security** tab, select the **Internet** zone, and then select **Custom level**.</span></span>
3. <span data-ttu-id="f37f5-212">**ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-212">Scroll to **Downloads**, and then, under **File download**, select the **Enable** option.</span></span>

### <a name="database-synchronization-fails"></a><span data-ttu-id="f37f5-213">データベース同期の失敗</span><span class="sxs-lookup"><span data-stu-id="f37f5-213">Database synchronization fails</span></span>

<span data-ttu-id="f37f5-214">データベースを Microsoft Visual Studio から新しくインポートされたデータベースと同期させると、その同期は失敗することがあり、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-214">When you sync the database against the newly imported database from Microsoft Visual Studio, the synchronization might fail, and you might receive the following error message:</span></span>

> <span data-ttu-id="f37f5-215">コード 1 で終了した SQL connection syncengine.exe のオープンに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="f37f5-215">Failed to open SQL connection syncengine.exe exited with code -1.</span></span>

<span data-ttu-id="f37f5-216">この場合、次のメッセージも Windows アプリケーション ログのイベント ID 140 で記録されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-216">In this case, the following message is also logged under event ID 140 in the Windows application log:</span></span>

> <span data-ttu-id="f37f5-217">オブジェクト サーバー データベース シンクロナイザー: データベースに格納されている内部システム テーブル バージョン番号が、カーネル (141/138) でサポートされているバージョンよりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="f37f5-217">Object Server Database Synchronizer: The internal system table version number stored in the database is higher than the version supported by the kernel (141/138).</span></span> <span data-ttu-id="f37f5-218">新しい Microsoft Dynamics カーネルを使用するか、-REPAIR コマンドライン パラメーターを使用して Microsoft Dynamics を起動し、同期を強制します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-218">Use a newer Microsoft Dynamics kernel, or start Microsoft Dynamics using the -REPAIR command line parameter to enforce synchronization.</span></span>

<span data-ttu-id="f37f5-219">この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f37f5-219">This issue can occur when the platform build number of the current environment is lower than the platform build number of the source environment.</span></span> <span data-ttu-id="f37f5-220">問題を解決するには、状況に応じて、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-220">To resolve the issue, follow one of these steps, depending on your circumstances:</span></span>

- <span data-ttu-id="f37f5-221">LCS で環境ページの **更新** タイルを使用し、ソース環境のプラットフォームに一致するように現在の環境のプラットフォームをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-221">Use the **Updates** tiles on the environment page in LCS to upgrade the platform in the current environment so that it matches the platform in the source environment.</span></span>
- <span data-ttu-id="f37f5-222">データベースで必要なバージョンを調整する次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-222">Run the following query to adjust the expected version in the database.</span></span>

    ```
    UPDATE SQLSYSTEMVARIABLES

    SET VALUE = 138

    WHERE PARM = 'SYSTABVERSION'
    ```

    > [!NOTE]
    > <span data-ttu-id="f37f5-223">このクエリの値 **138** は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-223">The value **138** in this query is taken from the event log message, where version 138 was expected in this particular environment.</span></span>

### <a name="performance"></a><span data-ttu-id="f37f5-224">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="f37f5-224">Performance</span></span>

<span data-ttu-id="f37f5-225">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-225">The following guidelines can help you achieve optimal performance:</span></span>

- <span data-ttu-id="f37f5-226">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</span><span class="sxs-lookup"><span data-stu-id="f37f5-226">Always import the .bacpac file locally on the computer that runs the SQL Server instance.</span></span> <span data-ttu-id="f37f5-227">リモート マシンで Management Studio からインポートしないでください。</span><span class="sxs-lookup"><span data-stu-id="f37f5-227">Don't import it from Management Studio on a remote machine.</span></span>
- <span data-ttu-id="f37f5-228">Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-228">In a Finance and Operations one-box environment that is hosted in Azure, put the .bacpac file on drive D when you import it.</span></span> <span data-ttu-id="f37f5-229">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure 仮想マシン (VM) 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f37f5-229">(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure virtual machines (VMs), see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) blog post.</span></span>
- <span data-ttu-id="f37f5-230">SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/library/ms175935.aspx) を実行するアカウントに権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="f37f5-230">Grant the account that runs the SQL Server Windows service [Instance File Initialization](https://msdn.microsoft.com/library/ms175935.aspx) rights.</span></span> <span data-ttu-id="f37f5-231">この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-231">In this way, you can help improve the speed of the import process and the speed of a restore from a \*.bak file.</span></span> <span data-ttu-id="f37f5-232">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="f37f5-232">For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</span></span>
