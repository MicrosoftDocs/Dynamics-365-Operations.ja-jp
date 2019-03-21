---
title: デバッグおよび診断
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデバッグや診断シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/28/2019
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
ms.openlocfilehash: 80490a3aff6ea52295fc4c4a21405c2eb1ff70f8
ms.sourcegitcommit: 2f7e06a3c8813dac773d075c9868e4cfc040a64c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/07/2019
ms.locfileid: "780158"
---
# <a name="debugging-and-diagnostics"></a><span data-ttu-id="17c20-103">デバッグおよび診断</span><span class="sxs-lookup"><span data-stu-id="17c20-103">Debugging and diagnostics</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17c20-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="17c20-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="17c20-105">このチュートリアルでは、更新操作とエクスポート操作を組み合わせて、デバッグの目的での生産データの最新のコピーを取得する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="17c20-105">This tutorial shows how to combine refresh with export operations to get a recent copy of production data for debugging purposes.</span></span>

<span data-ttu-id="17c20-106">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17c20-106">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="17c20-107">ユーザー受け入れテスト (UAT) 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="17c20-107">Refresh the user acceptance testing (UAT) environment.</span></span>
> * <span data-ttu-id="17c20-108">Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリへのエクスポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="17c20-108">Run the export to the Asset Library in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
> * <span data-ttu-id="17c20-109">データベース バックアップをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="17c20-109">Download the database backup.</span></span>
> * <span data-ttu-id="17c20-110">データベースをインポートし、開発者環境で使用できるようにそれを準備します。</span><span class="sxs-lookup"><span data-stu-id="17c20-110">Import the database and prepare it so that it can be used in a developer environment.</span></span>

<span data-ttu-id="17c20-111">このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations を既に稼働している顧客が、開発環境に生産トランザクションの最新のコピーを読み込もうとしています。</span><span class="sxs-lookup"><span data-stu-id="17c20-111">As an example of this scenario, a customer who has already gone live with Microsoft Dynamics 365 for Finance and Operations wants to load a recent copy of production transactions into his or her development environment.</span></span> <span data-ttu-id="17c20-112">これにより、顧客は特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。</span><span class="sxs-lookup"><span data-stu-id="17c20-112">In this way, the customer will be able to debug specific transactions or develop new features and reports by using realistic datasets.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17c20-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="17c20-113">Prerequisites</span></span>

<span data-ttu-id="17c20-114">更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-114">To do a refresh operation, you must have your production environment deployed, or you must have a minimum of two standard UAT environments.</span></span> <span data-ttu-id="17c20-115">このチュートリアルを完了するには、開発者環境が配置されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-115">To complete this tutorial, you must have a developer environment deployed.</span></span>

## <a name="refresh-the-uat-environment"></a><span data-ttu-id="17c20-116">UAT 環境を更新</span><span class="sxs-lookup"><span data-stu-id="17c20-116">Refresh the UAT environment</span></span>

<span data-ttu-id="17c20-117">この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。</span><span class="sxs-lookup"><span data-stu-id="17c20-117">This refresh operation will overwrite the UAT environment with the latest copy of the production database.</span></span> <span data-ttu-id="17c20-118">この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="17c20-118">To complete this step, follow the instructions in [Refresh for training purposes](dbmovement-scenario-general-refresh.md).</span></span>

## <a name="back-up-to-the-asset-library"></a><span data-ttu-id="17c20-119">資産ライブラリへのバックアップ</span><span class="sxs-lookup"><span data-stu-id="17c20-119">Back up to the Asset Library</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-database"></a><span data-ttu-id="17c20-120">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="17c20-120">Import the database</span></span>

<span data-ttu-id="17c20-121">データベース バックアップ (.bacpac) ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="17c20-121">After you've downloaded a database backup (.bacpac) file, you can begin the manual import operation on your Tier 1 environment.</span></span> <span data-ttu-id="17c20-122">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</span><span class="sxs-lookup"><span data-stu-id="17c20-122">When you import the database, we recommend that you follow these guidelines:</span></span>

- <span data-ttu-id="17c20-123">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="17c20-123">Keep a copy of the existing AxDB database, so that you can revert to it later if required.</span></span>
- <span data-ttu-id="17c20-124">**AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="17c20-124">Import the new database under a new name, such as **AxDB\_fromProd**.</span></span>

<span data-ttu-id="17c20-125">最高のパフォーマンスを保証するには、\*.bacpac ファイルをインポート元のローカル コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="17c20-125">To help guarantee the best performance, copy the \*.bacpac file to the local computer that you're importing from.</span></span> <span data-ttu-id="17c20-126">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17c20-126">Open a **Command Prompt** window, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

<span data-ttu-id="17c20-127">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="17c20-127">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="17c20-128">**tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="17c20-128">**tsn (target server name)** – The name of the Microsoft SQL Server instance to import into.</span></span>
- <span data-ttu-id="17c20-129">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="17c20-129">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="17c20-130">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="17c20-130">The database should **not** already exist.</span></span>
- <span data-ttu-id="17c20-131">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="17c20-131">**sf (source file)** – The path and name of the file to import from.</span></span>

> [!NOTE]
> <span data-ttu-id="17c20-132">インポート中に、ユーザー名およびパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="17c20-132">During import, the user name and password aren't required.</span></span> <span data-ttu-id="17c20-133">既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="17c20-133">By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</span></span>

## <a name="update-the-database"></a><span data-ttu-id="17c20-134">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="17c20-134">Update the database</span></span>

<span data-ttu-id="17c20-135">インポートされたデータベースに対して、次の SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="17c20-135">Run the following SQL script against the imported database.</span></span> <span data-ttu-id="17c20-136">このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL インスタンスの SQL のログインに正しくリンクします。</span><span class="sxs-lookup"><span data-stu-id="17c20-136">This script adds back the users that you deleted from the source database and correctly links them to the SQL logins for this SQL instance.</span></span> <span data-ttu-id="17c20-137">スクリプトはまた、変更の追跡を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="17c20-137">The script also turns change tracking back on.</span></span> <span data-ttu-id="17c20-138">必ず、データベースの名前を使用できるように、最後の **ALTER DATABASE** ステートメントを編集してください。</span><span class="sxs-lookup"><span data-stu-id="17c20-138">Remember to edit the final **ALTER DATABASE** statement so that it uses the name of your database.</span></span>

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

GO
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

### <a name="turn-on-change-tracking"></a><span data-ttu-id="17c20-139">変更追跡を有効にする</span><span class="sxs-lookup"><span data-stu-id="17c20-139">Turn on change tracking</span></span>

<span data-ttu-id="17c20-140">ソース データベースで変更追跡が有効になっている場合は、**ALTER DATABASE** コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="17c20-140">If change tracking was turned on in the source database, be sure to turn it on in the newly provisioned database in the target environment by using the **ALTER DATABASE** command.</span></span>

```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

<span data-ttu-id="17c20-141">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを保証するには、データ管理のデータ エンティティの変更追跡をオンまたはオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-141">To help guarantee that the current version of the store procedure that is related to change tracking is used in the new database, you must turn change tracking on or off for a data entity in data management.</span></span> <span data-ttu-id="17c20-142">任意のエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-142">You can choose any entity.</span></span> <span data-ttu-id="17c20-143">ストアド プロシージャの更新を起動するには、この手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="17c20-143">This step is required to trigger the refresh of the store procedure.</span></span>

## <a name="start-to-use-the-new-database"></a><span data-ttu-id="17c20-144">新しいデータベースの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="17c20-144">Start to use the new database</span></span>

<span data-ttu-id="17c20-145">環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="17c20-145">To switch environments and use the new database, first stop the following services:</span></span>

- <span data-ttu-id="17c20-146">World Wide Web 公開サービス</span><span class="sxs-lookup"><span data-stu-id="17c20-146">World Wide Web Publishing Service</span></span>
- <span data-ttu-id="17c20-147">Microsoft Dynamics 365 Unified Operations: バッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="17c20-147">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="17c20-148">Management Reporter 2012 処理サービス</span><span class="sxs-lookup"><span data-stu-id="17c20-148">Management Reporter 2012 Process Service</span></span>

<span data-ttu-id="17c20-149">これらのサービスが停止した後、AxDB データベース **AxDB\_orig** の名前を変更し、新しくインポートしたデータベース **AxDB** の名前を変更し、そして 3 つのサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="17c20-149">After these services have been stopped, rename the AxDB database **AxDB\_orig**, rename your newly imported database **AxDB**, and then restart the three services.</span></span>

<span data-ttu-id="17c20-150">元のデータベースに戻すには、このプロセスを逆にします。</span><span class="sxs-lookup"><span data-stu-id="17c20-150">To switch back to the original database, reverse this process.</span></span> <span data-ttu-id="17c20-151">つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="17c20-151">In other words, stop the services, rename the databases, and then restart the services.</span></span>

### <a name="reprovision-the-target-environment"></a><span data-ttu-id="17c20-152">対象の環境を再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="17c20-152">Reprovision the target environment</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a><span data-ttu-id="17c20-153">財務報告データベースのリセット</span><span class="sxs-lookup"><span data-stu-id="17c20-153">Reset the Financial Reporting database</span></span>

<span data-ttu-id="17c20-154">財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-154">If you're using Financial Reporting, you must reset the Financial Reporting database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span> <span data-ttu-id="17c20-155">(財務報告は以前は Management Reporter という名前でした)</span><span class="sxs-lookup"><span data-stu-id="17c20-155">(Financial Reporting was previously named Management Reporter.)</span></span>

## <a name="reenter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a><span data-ttu-id="17c20-156">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</span><span class="sxs-lookup"><span data-stu-id="17c20-156">Reenter data from encrypted and environment-specific fields in the target database</span></span>

<span data-ttu-id="17c20-157">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="17c20-157">In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</span></span> <span data-ttu-id="17c20-158">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-158">The following fields are affected.</span></span> <span data-ttu-id="17c20-159">フィールド名は *Table.Field* 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-159">The field names are given in *Table.Field* format.</span></span>

| <span data-ttu-id="17c20-160">フィールド名</span><span class="sxs-lookup"><span data-stu-id="17c20-160">Field name</span></span>                                               | <span data-ttu-id="17c20-161">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="17c20-161">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="17c20-162">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="17c20-162">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="17c20-163">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-163">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="17c20-164">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="17c20-164">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="17c20-165">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-165">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="17c20-166">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="17c20-166">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="17c20-167">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="17c20-167">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="17c20-168">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="17c20-168">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="17c20-169">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-169">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="17c20-170">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="17c20-170">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="17c20-171">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-171">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="17c20-172">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-172">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="17c20-173">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="17c20-173">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="17c20-174">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="17c20-174">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="17c20-175">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。</span><span class="sxs-lookup"><span data-stu-id="17c20-175">It was previously in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="17c20-176">SysEmailSMTPPassword.Password</span><span class="sxs-lookup"><span data-stu-id="17c20-176">SysEmailSMTPPassword.Password</span></span>                            | <span data-ttu-id="17c20-177">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-177">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="17c20-178">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="17c20-178">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="17c20-179">このフィールドは、アプリケーション オブジェクト サーバー (AOS) により内部で使用されています。</span><span class="sxs-lookup"><span data-stu-id="17c20-179">This field is used internally by Application Object Server (AOS).</span></span> <span data-ttu-id="17c20-180">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="17c20-180">It can be ignored.</span></span> |
| <span data-ttu-id="17c20-181">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="17c20-181">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="17c20-182">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-182">This field is used internally by AOS.</span></span> <span data-ttu-id="17c20-183">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="17c20-183">It can be ignored.</span></span> |

## <a name="community-tools"></a><span data-ttu-id="17c20-184">コミュニティ ツール</span><span class="sxs-lookup"><span data-stu-id="17c20-184">Community tools</span></span>

<span data-ttu-id="17c20-185">開発者環境にバックアップ ファイルをインポートするための他のツールをお探しですか。</span><span class="sxs-lookup"><span data-stu-id="17c20-185">Are you looking for more tools to help with importing backup files to your developer environments?</span></span> <span data-ttu-id="17c20-186">他の情報源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="17c20-186">Here are some other sources of information:</span></span>

* <span data-ttu-id="17c20-187">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) には、コミュニティによって作成された多くの貴重なツールがあります。</span><span class="sxs-lookup"><span data-stu-id="17c20-187">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) provides many valuable tools that have been created by the community.</span></span>
* <span data-ttu-id="17c20-188">[GitHub でコミュニティによって提供されたオープン ソース プロジェクト](https://github.com/search?q=dynamics+365+finance+operations&s=stars)。</span><span class="sxs-lookup"><span data-stu-id="17c20-188">[Community provided open source projects on GitHub](https://github.com/search?q=dynamics+365+finance+operations&s=stars).</span></span>

## <a name="known-issues"></a><span data-ttu-id="17c20-189">既知の問題</span><span class="sxs-lookup"><span data-stu-id="17c20-189">Known issues</span></span>

### <a name="i-cant-download-management-studio-installation-files"></a><span data-ttu-id="17c20-190">Management Studio インストール ファイルをダウンロードできません</span><span class="sxs-lookup"><span data-stu-id="17c20-190">I can't download Management Studio installation files</span></span>

<span data-ttu-id="17c20-191">Microsoft SQL Server Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-191">When you try to download the Microsoft SQL Server Management Studio installer, you might receive the following error message:</span></span>

> <span data-ttu-id="17c20-192">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="17c20-192">Your current security settings do not allow this file to be downloaded.</span></span>

<span data-ttu-id="17c20-193">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="17c20-193">To work around this issue, follow these steps to enable file downloads.</span></span>

1. <span data-ttu-id="17c20-194">Web ブラウザーで**インターネット オプション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="17c20-194">In your web browser, open **Internet options**.</span></span>
2. <span data-ttu-id="17c20-195">**セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-195">On the **Security** tab, select the **Internet** zone, and then select **Custom level**.</span></span>
3. <span data-ttu-id="17c20-196">**ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="17c20-196">Scroll to **Downloads**, and then, under **File download**, select the **Enable** option.</span></span>

### <a name="database-synchronization-fails"></a><span data-ttu-id="17c20-197">データベース同期の失敗</span><span class="sxs-lookup"><span data-stu-id="17c20-197">Database synchronization fails</span></span>

<span data-ttu-id="17c20-198">データベースを Microsoft Visual Studio から新しくインポートされたデータベースと同期させると、その同期は失敗することがあり、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-198">When you sync the database against the newly imported database from Microsoft Visual Studio, the synchronization might fail, and you might receive the following error message:</span></span>

> <span data-ttu-id="17c20-199">コード 1 で終了した SQL connection syncengine.exe のオープンに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="17c20-199">Failed to open SQL connection syncengine.exe exited with code -1.</span></span>

<span data-ttu-id="17c20-200">この場合、次のメッセージも Windows アプリケーション ログのイベント ID 140 で記録されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-200">In this case, the following message is also logged under event ID 140 in the Windows application log:</span></span>

> <span data-ttu-id="17c20-201">オブジェクト サーバー データベース シンクロナイザー: データベースに格納されている内部システム テーブル バージョン番号が、カーネル (141/138) でサポートされているバージョンよりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="17c20-201">Object Server Database Synchronizer: The internal system table version number stored in the database is higher than the version supported by the kernel (141/138).</span></span> <span data-ttu-id="17c20-202">新しい Microsoft Dynamics カーネルを使用するか、-REPAIR コマンドライン パラメーターを使用して Microsoft Dynamics を起動し、同期を強制します。</span><span class="sxs-lookup"><span data-stu-id="17c20-202">Use a newer Microsoft Dynamics kernel, or start Microsoft Dynamics using the -REPAIR command line parameter to enforce synchronization.</span></span>

<span data-ttu-id="17c20-203">この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="17c20-203">This issue can occur when the platform build number of the current environment is lower than the platform build number of the source environment.</span></span> <span data-ttu-id="17c20-204">状況に応じて、LCS の環境ページの**更新**タイルを使用して、現在の環境のプラットフォームをソース環境のプラットフォームと一致するようにアップグレードするか、次のクエリを実行してデータベースの必要なバージョンを調整します。</span><span class="sxs-lookup"><span data-stu-id="17c20-204">Depending on your circumstances, either use the **Updates** tiles on the environment page in LCS to upgrade the platform in the current environment so that it matches the platform in the source environment, or run the following query to adjust the expected version in the database.</span></span>

```
UPDATE SQLSYSTEMVARIABLES

SET VALUE = 138

WHERE PARM = 'SYSTABVERSION'
```

> [!NOTE]
> <span data-ttu-id="17c20-205">前のクエリの値 **138** は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。</span><span class="sxs-lookup"><span data-stu-id="17c20-205">The value **138** in the preceding query is taken from the event log message, where version 138 was expected in this particular environment.</span></span>

### <a name="performance"></a><span data-ttu-id="17c20-206">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="17c20-206">Performance</span></span>

<span data-ttu-id="17c20-207">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="17c20-207">The following guidelines can help you achieve optimal performance:</span></span>

- <span data-ttu-id="17c20-208">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</span><span class="sxs-lookup"><span data-stu-id="17c20-208">Always import the .bacpac file locally on the computer that runs the SQL Server instance.</span></span> <span data-ttu-id="17c20-209">リモート マシンで Management Studio からインポートしないでください。</span><span class="sxs-lookup"><span data-stu-id="17c20-209">Don't import it from Management Studio on a remote machine.</span></span>
- <span data-ttu-id="17c20-210">Microsoft Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="17c20-210">In a Finance and Operations one-box environment that is hosted in Microsoft Azure, put the .bacpac file on drive D when you import it.</span></span> <span data-ttu-id="17c20-211">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure 仮想マシン (VM) 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17c20-211">(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure virtual machines (VMs), see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) blog post.</span></span>
- <span data-ttu-id="17c20-212">SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/library/ms175935.aspx) を実行するアカウントに権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="17c20-212">Grant the account that runs the SQL Server Windows service [Instance File Initialization](https://msdn.microsoft.com/library/ms175935.aspx) rights.</span></span> <span data-ttu-id="17c20-213">この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="17c20-213">In this way, you can help improve the speed of the import process and the speed of a restore from a \*.bak file.</span></span> <span data-ttu-id="17c20-214">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="17c20-214">For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</span></span>
