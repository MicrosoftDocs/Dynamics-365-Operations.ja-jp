---
redirect_url: /dynamics365/unified-operations/dev-itpro/database/dbmovement-operations
title: "Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする"
description: "このトピックでは、 Microsoft Dynamics 365 for Finance and Operations のデータベースを Azure ベースの環境から SQL Server ベースの環境に移動する方法について説明します。"
author: laneswenka
manager: AnnBe
ms.date: 01/07/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 203764
ms.assetid: 45efdabf-1714-4ba4-9a9d-217143a6c6e0
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 20f399701df76bb4adf0948291732bca64fb8d5a
ms.openlocfilehash: 3ea81f46ca3e48578deca7e58cd794671f7e98e0
ms.contentlocale: ja-jp
ms.lasthandoff: 02/12/2019

---

# <a name="copy-finance-and-operations-databases-from-azure-sql-database-to-sql-server-environments"></a><span data-ttu-id="68572-103">Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする</span><span class="sxs-lookup"><span data-stu-id="68572-103">Copy Finance and Operations databases from Azure SQL Database to SQL Server environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68572-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを、Microsoft Azure に基づいた環境から Microsoft SQL Serverに基づく環境にエクスポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68572-104">This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database from an environment that is based on Microsoft Azure and import it into an environment that is based on Microsoft SQL Server.</span></span>

## <a name="overview"></a><span data-ttu-id="68572-105">概要</span><span class="sxs-lookup"><span data-stu-id="68572-105">Overview</span></span>

<span data-ttu-id="68572-106">データベースを移動するには、セルフ サービス アクションを使用して Azure SQL データベースからデータベースをエクスポートし、Microsoft SQL Server にインポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-106">To move a database, use the self-service action to export the database from Azure SQL Database and then import it into Microsoft SQL Server.</span></span> <span data-ttu-id="68572-107">エクスポートされたデータのファイル名拡張子は .bacpac なので、このプロセスは多くの場合 *bacpac プロセス*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="68572-107">Because the file name extension for the exported data is .bacpac, this process is often referred to as the *bacpac process*.</span></span>

<span data-ttu-id="68572-108">データベース移動の高レベルのプロセスには、次のフェーズが含まれます。</span><span class="sxs-lookup"><span data-stu-id="68572-108">The high-level process for a database move includes the following phases:</span></span>

1. <span data-ttu-id="68572-109">LCS 資産ライブラリにソース環境をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-109">Export your source environment to the LCS Asset Library.</span></span>
2. <span data-ttu-id="68572-110">SQL Server にデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-110">Import the database into SQL Server.</span></span>
3. <span data-ttu-id="68572-111">データベースの更新のため SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="68572-111">Run a SQL script to update the database.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68572-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="68572-112">Prerequisites</span></span>

<span data-ttu-id="68572-113">データベースを移動するには、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-113">The following prerequisites must be met before you can move a database:</span></span>

- <span data-ttu-id="68572-114">ソース環境 (つまりソース データベースに接続されている環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-114">The source environment (that is, the environment that is connected to the source database) must run a version of the Finance and Operations platform that is earlier than or the same as the version of the platform that the destination environment runs.</span></span>
- <span data-ttu-id="68572-115">サンドボックス環境データベースのみをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="68572-115">Only a sandbox environment database can be exported.</span></span> <span data-ttu-id="68572-116">実稼働環境をコピーする必要がある場合は、最初に、その環境をサンド ボックス環境に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-116">If you must copy the production environment, you must first refresh that environment to the sandbox environment.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="68572-117">このトピックでは、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 以上)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="68572-117">In this topic, the term *sandbox* is used to refer to a Standard or Premier Acceptance Testing (Tier 2+) or higher environment connected to a SQL Azure database.</span></span>

- <span data-ttu-id="68572-118">出力先の SQL Server 環境では、SQL Server 2016 Release to Manufacturing (RTM) (13.00.1601.5) 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-118">The destination SQL Server environment must run SQL Server 2016 Release to Manufacturing (RTM) (13.00.1601.5) or later.</span></span> <span data-ttu-id="68572-119">SQL Server 2016 の Community Technology Preview (CTP) バージョンでは、インポート処理中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="68572-119">The Community Technology Preview (CTP) versions of SQL Server 2016 might cause errors during the import process.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="68572-120">準備</span><span class="sxs-lookup"><span data-stu-id="68572-120">Before you begin</span></span>

<span data-ttu-id="68572-121">暗号化された環境固有の値を新しい環境にインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="68572-121">Encrypted and environment-specific values can't be imported into a new environment.</span></span> <span data-ttu-id="68572-122">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-122">After you've completed the import, you must re-enter some data from your source environment in your target environment.</span></span>

### <a name="document-the-values-of-encrypted-fields"></a><span data-ttu-id="68572-123">暗号化されたフィールドの値を文書化</span><span class="sxs-lookup"><span data-stu-id="68572-123">Document the values of encrypted fields</span></span>

<span data-ttu-id="68572-124">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="68572-124">Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</span></span> <span data-ttu-id="68572-125">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-125">Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</span></span> <span data-ttu-id="68572-126">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="68572-126">New values that are entered in encrypted fields after an import will be readable.</span></span> <span data-ttu-id="68572-127">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="68572-127">The following fields are affected.</span></span> <span data-ttu-id="68572-128">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="68572-128">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="68572-129">フィールド名</span><span class="sxs-lookup"><span data-stu-id="68572-129">Field name</span></span>                                               | <span data-ttu-id="68572-130">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="68572-130">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="68572-131">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="68572-131">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="68572-132">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-132">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="68572-133">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="68572-133">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="68572-134">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-134">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="68572-135">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="68572-135">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="68572-136">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68572-136">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="68572-137">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="68572-137">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="68572-138">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-138">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="68572-139">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="68572-139">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="68572-140">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-140">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="68572-141">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-141">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="68572-142">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="68572-142">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="68572-143">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="68572-143">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="68572-144">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。</span><span class="sxs-lookup"><span data-stu-id="68572-144">It was previously in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="68572-145">SysEmailSMTPPassword.Password</span><span class="sxs-lookup"><span data-stu-id="68572-145">SysEmailSMTPPassword.Password</span></span>                            | <span data-ttu-id="68572-146">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-146">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="68572-147">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="68572-147">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="68572-148">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-148">This field is used internally by AOS.</span></span> <span data-ttu-id="68572-149">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="68572-149">It can be ignored.</span></span> |
| <span data-ttu-id="68572-150">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="68572-150">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="68572-151">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-151">This field is used internally by AOS.</span></span> <span data-ttu-id="68572-152">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="68572-152">It can be ignored.</span></span> |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a><span data-ttu-id="68572-153">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</span><span class="sxs-lookup"><span data-stu-id="68572-153">If you're running Retail components, document encrypted and environment-specific values</span></span>

<span data-ttu-id="68572-154">次のページの値は、環境固有またはデータベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="68572-154">The values on the following pages are either environment-specific or encrypted in the database.</span></span> <span data-ttu-id="68572-155">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="68572-155">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="68572-156">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="68572-156">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="68572-157">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="68572-157">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

## <a name="self-service-database-export"></a><span data-ttu-id="68572-158">データベースのセルフ サービスエクスポート</span><span class="sxs-lookup"><span data-stu-id="68572-158">Self-service database export</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-database"></a><span data-ttu-id="68572-159">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="68572-159">Import the database</span></span>

<span data-ttu-id="68572-160">.bacpac ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="68572-160">After you have downloaded a .bacpac file, you can begin the manual import operation on your Tier 1 environment.</span></span> <span data-ttu-id="68572-161">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</span><span class="sxs-lookup"><span data-stu-id="68572-161">When you import the database, we recommend that you follow these guidelines:</span></span>

- <span data-ttu-id="68572-162">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="68572-162">Retain a copy of the existing AxDB database so that you can revert to it later, if needed.</span></span>
- <span data-ttu-id="68572-163">**AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-163">Import the new database under a new name, such as **AxDB\_fromProd**.</span></span>

<span data-ttu-id="68572-164">最高のパフォーマンスを確保するには、\*.bacpac ファイルをインポート元のローカル コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="68572-164">To help ensure the best performance, copy the \*.bacpac file to the local computer that you're importing from.</span></span> <span data-ttu-id="68572-165">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="68572-165">Open a **Command Prompt** window and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=2400
```

<span data-ttu-id="68572-166">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="68572-166">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="68572-167">**tsn(ターゲット サーバー名)** – インポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="68572-167">**tsn (target server name)** – The name of the SQL Server to import into.</span></span>
- <span data-ttu-id="68572-168">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="68572-168">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="68572-169">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="68572-169">The database should **not** already exist.</span></span>
- <span data-ttu-id="68572-170">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="68572-170">**sf (source file)** – The path and name of the file to import from.</span></span>

> [!NOTE]
> <span data-ttu-id="68572-171">インポート中に、ユーザー名およびパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="68572-171">During import, the user name and password aren't required.</span></span> <span data-ttu-id="68572-172">既定では、SQL Server は現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="68572-172">By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</span></span>

## <a name="update-the-database"></a><span data-ttu-id="68572-173">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="68572-173">Update the database</span></span>

<span data-ttu-id="68572-174">インポートされたデータベースに対して、次の SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="68572-174">Run the following SQL script against the imported database.</span></span> <span data-ttu-id="68572-175">このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL インスタンスの SQL のログインに正しくリンクします。</span><span class="sxs-lookup"><span data-stu-id="68572-175">This script adds back the users that you deleted from the source database and correctly links them to the SQL logins for this SQL instance.</span></span> <span data-ttu-id="68572-176">スクリプトはまた、変更の追跡を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="68572-176">The script also turns change tracking back on.</span></span> <span data-ttu-id="68572-177">必ず、データベースの名前を使用できるように、最後の **ALTER DATABASE** ステートメントを編集してください。</span><span class="sxs-lookup"><span data-stu-id="68572-177">Remember to edit the final **ALTER DATABASE** statement so that it uses the name of your database.</span></span>

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

ALTER DATABASE [<your AX database name>] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON)
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

### <a name="enable-change-tracking"></a><span data-ttu-id="68572-178">変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="68572-178">Enable change tracking</span></span>
<span data-ttu-id="68572-179">ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="68572-179">If change tracking was enabled in the source database, ensure to enable change tracking again in the newly provisioned database in the target environment using the ALTER DATABASE command.</span></span>

```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

<span data-ttu-id="68572-180">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="68572-180">To ensure that the current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</span></span> <span data-ttu-id="68572-181">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="68572-181">This can be done on any entity, as this is needed to trigger the refresh of store procedure.</span></span>

## <a name="start-to-use-the-new-database"></a><span data-ttu-id="68572-182">新しいデータベースの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="68572-182">Start to use the new database</span></span>

<span data-ttu-id="68572-183">環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="68572-183">To switch the environment and use the new database, first stop the following services:</span></span>

- <span data-ttu-id="68572-184">World Wide Web 公開サービス</span><span class="sxs-lookup"><span data-stu-id="68572-184">World Wide Web Publishing Service</span></span>
- <span data-ttu-id="68572-185">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="68572-185">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="68572-186">Management Reporter 2012 処理サービス</span><span class="sxs-lookup"><span data-stu-id="68572-186">Management Reporter 2012 Process Service</span></span>

<span data-ttu-id="68572-187">サービスが停止した後、AxDB データベース **AxDB\_orig** の名前を変更し、新しくインポートしたデータベース **AxDB** の名前を変更し、そして 3 つのサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="68572-187">After the services have been stopped, rename the AxDB database **AxDB\_orig**, rename your newly imported database **AxDB**, and then restart the three services.</span></span>

<span data-ttu-id="68572-188">データベースの名前を変更するには、次の ALTER DATABASE コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="68572-188">To rename the database, use the following ALTER DATABASE command:</span></span>
```
ALTER DATABASE [your database name] MODIFY NAME = [new database name];
```

<span data-ttu-id="68572-189">元のデータベースに戻すには、このプロセスを逆にします。</span><span class="sxs-lookup"><span data-stu-id="68572-189">To switch back to the original database, reverse this process.</span></span> <span data-ttu-id="68572-190">つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="68572-190">In other words, stop the services, rename the databases, and then restart the services.</span></span>

### <a name="re-provision-the-target-environment"></a><span data-ttu-id="68572-191">対象の環境を再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="68572-191">Re-provision the target environment</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a><span data-ttu-id="68572-192">財務報告データベースのリセット</span><span class="sxs-lookup"><span data-stu-id="68572-192">Reset the Financial Reporting database</span></span>

<span data-ttu-id="68572-193">Management Reporter という以前の名前を持った財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります</span><span class="sxs-lookup"><span data-stu-id="68572-193">If you're using Financial Reporting, which was previously named Management Reporter, you must reset the Financial Reporting database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span>

## <a name="re-enter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a><span data-ttu-id="68572-194">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</span><span class="sxs-lookup"><span data-stu-id="68572-194">Re-enter data from encrypted and environment-specific fields in the target database</span></span>

<span data-ttu-id="68572-195">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68572-195">In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</span></span> <span data-ttu-id="68572-196">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="68572-196">The following fields are affected.</span></span> <span data-ttu-id="68572-197">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="68572-197">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="68572-198">フィールド名</span><span class="sxs-lookup"><span data-stu-id="68572-198">Field name</span></span>                                               | <span data-ttu-id="68572-199">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="68572-199">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="68572-200">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="68572-200">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="68572-201">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-201">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="68572-202">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="68572-202">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="68572-203">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-203">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="68572-204">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="68572-204">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="68572-205">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68572-205">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="68572-206">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="68572-206">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="68572-207">このフィールドは DIXF で使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-207">This field is used by DIXF.</span></span> |
| <span data-ttu-id="68572-208">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="68572-208">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="68572-209">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-209">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="68572-210">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-210">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="68572-211">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="68572-211">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="68572-212">このフィールドは、AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="68572-212">This field has been obsolete since AX 7.0 (February 2016).</span></span> <span data-ttu-id="68572-213">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。</span><span class="sxs-lookup"><span data-stu-id="68572-213">It was previously in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="68572-214">SysEmailSMTPPassword.Password</span><span class="sxs-lookup"><span data-stu-id="68572-214">SysEmailSMTPPassword.Password</span></span>                            | <span data-ttu-id="68572-215">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-215">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="68572-216">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="68572-216">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="68572-217">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-217">This field is used internally by AOS.</span></span> <span data-ttu-id="68572-218">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="68572-218">It can be ignored.</span></span> |
| <span data-ttu-id="68572-219">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="68572-219">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="68572-220">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="68572-220">This field is used internally by AOS.</span></span> <span data-ttu-id="68572-221">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="68572-221">It can be ignored.</span></span> |

## <a name="known-issues"></a><span data-ttu-id="68572-222">既知の問題</span><span class="sxs-lookup"><span data-stu-id="68572-222">Known issues</span></span>

### <a name="i-cant-download-management-studio-installation-files"></a><span data-ttu-id="68572-223">Management Studio インストール ファイルをダウンロードできません</span><span class="sxs-lookup"><span data-stu-id="68572-223">I can't download Management Studio installation files</span></span>

<span data-ttu-id="68572-224">Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="68572-224">When you try to download the Management Studio installer, you might receive the following error message:</span></span>

> <span data-ttu-id="68572-225">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="68572-225">Your current security settings do not allow this file to be downloaded.</span></span>

<span data-ttu-id="68572-226">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="68572-226">To work around this issue, follow these steps to enable file downloads.</span></span>

1. <span data-ttu-id="68572-227">Web ブラウザーで**インターネット オプション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="68572-227">In your web browser, open **Internet options**.</span></span>
2. <span data-ttu-id="68572-228">**セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-228">On the **Security** tab, select the **Internet** zone, and then select **Custom level**.</span></span>
3. <span data-ttu-id="68572-229">**ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="68572-229">Scroll to **Downloads**, and then, under **File download**, select the **Enable** option.</span></span>

### <a name="database-synchronization-fails"></a><span data-ttu-id="68572-230">データベース同期の失敗</span><span class="sxs-lookup"><span data-stu-id="68572-230">Database synchronization fails</span></span>

<span data-ttu-id="68572-231">データベースを Microsoft Visual Studio から新しくインポートされたデータベースと同期させると、その同期は失敗することがあり、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="68572-231">When you synchronize the database against the newly imported database from Microsoft Visual Studio, the synchronization might fail, and you might receive the following error message:</span></span>

> <span data-ttu-id="68572-232">コード 1 で終了した SQL connection syncengine.exe のオープンに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="68572-232">Failed to open SQL connection syncengine.exe exited with code -1.</span></span>

<span data-ttu-id="68572-233">この場合、次のメッセージも Windows アプリケーション ログのイベント ID 140 で記録されます。</span><span class="sxs-lookup"><span data-stu-id="68572-233">In this case, the following message is also logged under event ID 140 in the Windows application log:</span></span>

> <span data-ttu-id="68572-234">オブジェクト サーバー データベース シンクロナイザー: データベースに格納されている内部システム テーブル バージョン番号が、カーネル (141/138) でサポートされているバージョンよりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="68572-234">Object Server Database Synchronizer: The internal system table version number stored in the database is higher than the version supported by the kernel (141/138).</span></span> <span data-ttu-id="68572-235">新しい Microsoft Dynamics カーネルを使用するか、-REPAIR コマンドライン パラメーターを使用して Microsoft Dynamics を起動し、同期を強制します。</span><span class="sxs-lookup"><span data-stu-id="68572-235">Use a newer Microsoft Dynamics kernel, or start Microsoft Dynamics using the -REPAIR command line parameter to enforce synchronization.</span></span>

<span data-ttu-id="68572-236">この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="68572-236">This issue can occur when the platform build number of the current environment is lower than the platform build number of the source environment.</span></span> <span data-ttu-id="68572-237">状況に応じて、LCS **環境**ページの**更新**タイルを使用して、現在の環境のプラットフォームをソース環境のプラットフォームと一致するようにアップグレードするか、次のクエリを実行してデータベースの必要なバージョンを調整します。</span><span class="sxs-lookup"><span data-stu-id="68572-237">Depending on your circumstances, either use the **Updates** tiles on the LCS **Environment** page to upgrade the platform in the current environment so that it matches the platform in the source environment, or run the following query to adjust the expected version in the database.</span></span>

```
UPDATE SQLSYSTEMVARIABLES

SET VALUE = 138

WHERE PARM = 'SYSTABVERSION'
```

> [!NOTE]
> <span data-ttu-id="68572-238">前のクエリの値 **138** は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。</span><span class="sxs-lookup"><span data-stu-id="68572-238">The value **138** in the preceding query is taken from the event log message, where version 138 was expected in this particular environment.</span></span>

### <a name="performance"></a><span data-ttu-id="68572-239">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="68572-239">Performance</span></span>

<span data-ttu-id="68572-240">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="68572-240">The following guidelines can help you achieve optimal performance:</span></span>

- <span data-ttu-id="68572-241">常に Azure SQL データベースと同じ Azure データ センター内にある仮想マシン (VM) からデータベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-241">Always export a database from a virtual machine (VM) that is in the same Azure datacenter as the Azure SQL database.</span></span> <span data-ttu-id="68572-242">サンドボックス データベースのコピーをエクスポートする場合は、サンド ボックス AOS コンピューターからエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-242">If you're exporting a copy of your sandbox database, export it from the sandbox AOS computer.</span></span>
- <span data-ttu-id="68572-243">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</span><span class="sxs-lookup"><span data-stu-id="68572-243">Always import the .bacpac file locally on the computer that runs the SQL Server instance.</span></span> <span data-ttu-id="68572-244">リモート マシンで Management Studio からインポートしないでください。</span><span class="sxs-lookup"><span data-stu-id="68572-244">Don't import it from Management Studio on a remote machine.</span></span>
- <span data-ttu-id="68572-245">Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="68572-245">In a Finance and Operations one-box environment that is hosted in Azure, put the .bacpac file on drive D when you import it.</span></span> <span data-ttu-id="68572-246">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure Vm 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68572-246">(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure VMs, see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) blog post.</span></span>
- <span data-ttu-id="68572-247">SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/en-us/library/ms175935.aspx) を実行するアカウントに権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="68572-247">Grant the account that runs the SQL Server Windows service [Instance File Initialization](https://msdn.microsoft.com/en-us/library/ms175935.aspx) rights.</span></span> <span data-ttu-id="68572-248">この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="68572-248">In this way, you can help improve the speed of the import process and the speed of a restore from a \*.bak file.</span></span> <span data-ttu-id="68572-249">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="68572-249">For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</span></span>
- <span data-ttu-id="68572-250">大きなデータベースのメモリ制限が存在する場合があるので、Azure SQLデータベースから、**Management Studio でデータ層アプリケーションのエクスポート**を選択しないでください。</span><span class="sxs-lookup"><span data-stu-id="68572-250">From Azure SQL Database, don't select **Export data tier application in Management Studio**, because there can be a memory limitation for larger databases.</span></span>

