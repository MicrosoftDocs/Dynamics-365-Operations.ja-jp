---
title: ゴールデン コンフィギュレーション プロモーション
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のゴールデン コンフィギュレーション プロモーションについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: 3418fc37315905391b5fed45d2736152914b5be0
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537094"
---
# <a name="golden-configuration-promotion"></a><span data-ttu-id="0210a-103">ゴールデン コンフィギュレーション プロモーション</span><span class="sxs-lookup"><span data-stu-id="0210a-103">Golden configuration promotion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0210a-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="0210a-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="0210a-105">「ゴールデン コンフィギュレーション」は、開発者環境が構成ストアとして使用されている Microsoft Dynamics エコシステムにおける顧客とパートナーの間での一般的な方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0210a-105">"Golden configuration" refers to a common practice among customers and partners in the Microsoft Dynamics ecosystem, where a developer environment is used as a configuration store.</span></span> <span data-ttu-id="0210a-106">この方法では、実装プロジェクトは、後で会議室パイロット、モック Go-Live、Go-Live の基準とできる際集荷されたグローバルおよび会社固有の設定をデータベースに保存できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-106">In this way, implementation projects can store finalized global and company-specific settings in a database that can later become a baseline for Conference Room Pilots, mock go-lives, and go-lives.</span></span> <span data-ttu-id="0210a-107">このチュートリアルでは、ゴールデン構成データベースを準備し、ターゲット ユーザー受け入れテスト (UAT) 環境に取り込む方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0210a-107">This tutorial shows how to prepare a golden configuration database and hydrate a target user acceptance testing (UAT) environment.</span></span>

<span data-ttu-id="0210a-108">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0210a-108">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="0210a-109">Microsoft Azure SQL データベースのゴールデン構成データベースを準備する。</span><span class="sxs-lookup"><span data-stu-id="0210a-109">Prepare the golden configuration database for Microsoft Azure SQL Database.</span></span>
> * <span data-ttu-id="0210a-110">ターゲット UAT 環境のインポートを実行する。</span><span class="sxs-lookup"><span data-stu-id="0210a-110">Run the import to the target UAT environment.</span></span>
> * <span data-ttu-id="0210a-111">実稼働環境に UAT 環境をコピーする。</span><span class="sxs-lookup"><span data-stu-id="0210a-111">Copy the UAT environment into a production environment.</span></span>

<span data-ttu-id="0210a-112">このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations で Go-Live していない顧客が、代わりに会議室パイロット、モック Go-Live、Go-Live を準備します。</span><span class="sxs-lookup"><span data-stu-id="0210a-112">As an example of this scenario, a customer who hasn't gone live with Microsoft Dynamics 365 for Finance and Operations is instead preparing for a Conference Room Pilot, mock go-live, or go-live.</span></span> <span data-ttu-id="0210a-113">このシナリオでは、開発者環境からのベースライン ゴールド ・ データベースを UAT 環境に昇格し、最終的を生産環境をサポートすることをします。</span><span class="sxs-lookup"><span data-stu-id="0210a-113">This scenario supports promoting a baseline golden database from a developer environment to a UAT environment and eventually to production.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0210a-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="0210a-114">Prerequisites</span></span>

<span data-ttu-id="0210a-115">このチュートリアルを完了するには、ゴールデン コンフィギュレーション データベースとして管理されるデータベースに配置されている開発者環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="0210a-115">To complete this tutorial, you must have a developer environment that is deployed with a database that is curated as a golden configuration database.</span></span> <span data-ttu-id="0210a-116">少なくとも 1 つの標準 UAT 環境が展開されていることと、必要に応じて、実稼働環境が 1 つ以上必要です。</span><span class="sxs-lookup"><span data-stu-id="0210a-116">You must also have at least one standard UAT environment deployed and, optionally, a production environment.</span></span>

<span data-ttu-id="0210a-117">開発環境は、ターゲット UAT 環境と同じ Finance and Operations の*アプリケーションのバージョン*を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-117">The developer environment must run the same *application version* of Finance and Operations as the target UAT environment.</span></span> <span data-ttu-id="0210a-118">加えて、開発者環境の*プラットフォーム バージョン*は、ターゲット UAT 環境のプラットフォーム バージョン以前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0210a-118">In addition, the *platform version* of the developer environment must be earlier than or the same as the platform version in the target UAT environment.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0210a-119">準備</span><span class="sxs-lookup"><span data-stu-id="0210a-119">Before you begin</span></span>

### <a name="supported-sql-server-collation"></a><span data-ttu-id="0210a-120">サポートされる SQL Server の照合順序</span><span class="sxs-lookup"><span data-stu-id="0210a-120">Supported SQL Server collation</span></span>

<span data-ttu-id="0210a-121">クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。</span><span class="sxs-lookup"><span data-stu-id="0210a-121">The only supported collation for Finance and Operations databases in the cloud is **SQL\_Latin1\_General\_CP1\_CI\_AS**.</span></span> <span data-ttu-id="0210a-122">開発環境の Microsoft SQL Server とデータベース照合順序がこの値に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0210a-122">Make sure that your Microsoft SQL Server and database collations in development environments are set to this value.</span></span> <span data-ttu-id="0210a-123">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこの照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0210a-123">Also make sure that any configuration environments that are published to sandbox have this collation.</span></span>

### <a name="document-the-values-of-encrypted-fields"></a><span data-ttu-id="0210a-124">暗号化されたフィールドの値を文書化</span><span class="sxs-lookup"><span data-stu-id="0210a-124">Document the values of encrypted fields</span></span>

<span data-ttu-id="0210a-125">暗号化された環境固有の値を新しい環境にインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0210a-125">Encrypted and environment-specific values can't be imported into a new environment.</span></span> <span data-ttu-id="0210a-126">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-126">After you've completed the import, you must reenter some data from your source environment in your target environment.</span></span>

<span data-ttu-id="0210a-127">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="0210a-127">Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</span></span> <span data-ttu-id="0210a-128">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-128">Therefore, after an import, you must manually delete and reenter values that are stored in encrypted fields.</span></span> <span data-ttu-id="0210a-129">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="0210a-129">New values that are entered in encrypted fields after an import will be readable.</span></span> <span data-ttu-id="0210a-130">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-130">The following fields are affected.</span></span> <span data-ttu-id="0210a-131">フィールド名は *Table.Field* 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-131">The field names are given in *Table.Field* format.</span></span>

| <span data-ttu-id="0210a-132">フィールド名</span><span class="sxs-lookup"><span data-stu-id="0210a-132">Field name</span></span>                                               | <span data-ttu-id="0210a-133">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="0210a-133">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="0210a-134">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="0210a-134">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="0210a-135">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-135">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="0210a-136">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="0210a-136">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="0210a-137">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-137">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="0210a-138">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="0210a-138">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="0210a-139">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0210a-139">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="0210a-140">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="0210a-140">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="0210a-141">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-141">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="0210a-142">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="0210a-142">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="0210a-143">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-143">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="0210a-144">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-144">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="0210a-145">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="0210a-145">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="0210a-146">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="0210a-146">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="0210a-147">これは以前、**すべての作業者アクション** ページ (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。</span><span class="sxs-lookup"><span data-stu-id="0210a-147">It previously appeared on the **All worker actions** page (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="0210a-148">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="0210a-148">SysEmailSMPTPassword.Password</span></span>                            | <span data-ttu-id="0210a-149">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-149">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="0210a-150">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="0210a-150">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="0210a-151">このフィールドは、アプリケーション オブジェクト サーバー (AOS) により内部で使用されています。</span><span class="sxs-lookup"><span data-stu-id="0210a-151">This field is used internally by Application Object Server (AOS).</span></span> <span data-ttu-id="0210a-152">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-152">It can be ignored.</span></span> |
| <span data-ttu-id="0210a-153">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="0210a-153">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="0210a-154">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-154">This field is used internally by AOS.</span></span> <span data-ttu-id="0210a-155">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-155">It can be ignored.</span></span> |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a><span data-ttu-id="0210a-156">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</span><span class="sxs-lookup"><span data-stu-id="0210a-156">If you're running Retail components, document encrypted and environment-specific values</span></span>

<span data-ttu-id="0210a-157">次のページの値は、環境固有またはデータベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="0210a-157">The values on the following pages are either environment-specific or encrypted in the database.</span></span> <span data-ttu-id="0210a-158">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="0210a-158">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="0210a-159">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="0210a-159">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="0210a-160">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="0210a-160">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

## <a name="create-a-copy-of-the-source-database"></a><span data-ttu-id="0210a-161">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="0210a-161">Create a copy of the source database</span></span>

<span data-ttu-id="0210a-162">ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。</span><span class="sxs-lookup"><span data-stu-id="0210a-162">Because you must delete database users before you can export the source SQL Server database, you should create a copy of that database.</span></span> <span data-ttu-id="0210a-163">元のデータベースを修正する代わりに、コピーで作業することができます。</span><span class="sxs-lookup"><span data-stu-id="0210a-163">You can then work with the copy instead of modifying the original database.</span></span> <span data-ttu-id="0210a-164">次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。</span><span class="sxs-lookup"><span data-stu-id="0210a-164">The following script backs up the default AxDB database and then restores it to the same instance under a new name.</span></span> <span data-ttu-id="0210a-165">このスクリプトを使用するには、最初に D:\\backups のパスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0210a-165">To use this script, first verify that the path D:\\backups exists.</span></span>

```
BACKUP DATABASE [AxDB] TO DISK = N'D:\Backups\axdb_golden.bak' WITH NOFORMAT, NOINIT,
NAME = N'AxDB_golden-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION, STATS = 10
GO
RESTORE DATABASE [AxDB_CopyForExport] FROM DISK = N'D:\Backups\axdb_golden.bak' WITH FILE = 1,
MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_CopyForExport.mdf',
MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForExport_Log.ldf',
NOUNLOAD, STATS = 5
```

## <a name="prepare-the-database"></a><span data-ttu-id="0210a-166">データベースの準備</span><span class="sxs-lookup"><span data-stu-id="0210a-166">Prepare the database</span></span>

<span data-ttu-id="0210a-167">次のスクリプトを、前のセクションで作成した AxDB\_CopyForExport データベースに対して実行します。</span><span class="sxs-lookup"><span data-stu-id="0210a-167">Run the following script against the AxDB\_CopyForExport database that you created in the previous section.</span></span> <span data-ttu-id="0210a-168">このスクリプトは、次の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="0210a-168">This script makes the following changes:</span></span>

- <span data-ttu-id="0210a-169">**SysGlobalConfiguration** フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。</span><span class="sxs-lookup"><span data-stu-id="0210a-169">Set the **SysGlobalConfiguration** flag to inform Finance and Operations that the database is Azure-based.</span></span>
- <span data-ttu-id="0210a-170">XU\_DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="0210a-170">Remove a reference to tempDB in the XU\_DisableEnableNonClusteredIndexes procedure.</span></span> <span data-ttu-id="0210a-171">Azure SQL データベースでは、tempDB の参照が許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0210a-171">References to tempDB aren't allowed in an Azure SQL database.</span></span> <span data-ttu-id="0210a-172">データベース同期プロセスは後で照会を再作成します。</span><span class="sxs-lookup"><span data-stu-id="0210a-172">The database synchronization process will re-create the reference later.</span></span>
- <span data-ttu-id="0210a-173">Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。</span><span class="sxs-lookup"><span data-stu-id="0210a-173">Drop users, because Microsoft Windows users are forbidden in Azure SQL databases.</span></span> <span data-ttu-id="0210a-174">他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-174">Other users must be re-created later, so that they're correctly linked to the appropriate sign-in on the target server.</span></span>
- <span data-ttu-id="0210a-175">暗号化されたハードウェア プロファイルの商社プロパティの消去。</span><span class="sxs-lookup"><span data-stu-id="0210a-175">Clear encrypted hardware profile merchant properties.</span></span>

<span data-ttu-id="0210a-176">データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="0210a-176">A successful export and import of the database requires all these changes.</span></span>

```
update sysglobalconfiguration
set value = 'SQLAZURE'
where name = 'BACKENDDB'

update sysglobalconfiguration
set value = 1
where name = 'TEMPTABLEINAXDB'

drop procedure if exists XU_DisableEnableNonClusteredIndexes
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
-- Clear encrypted hardware profile merchant properties
update dbo.RETAILHARDWAREPROFILE set SECUREMERCHANTPROPERTIES = null where SECUREMERCHANTPROPERTIES is not null
```

## <a name="export-the-database-from-sql-server"></a><span data-ttu-id="0210a-177">SQL Server からデータベースをエクスポート</span><span class="sxs-lookup"><span data-stu-id="0210a-177">Export the database from SQL Server</span></span>

<span data-ttu-id="0210a-178">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0210a-178">Open a **Command Prompt** window, and run the following commands.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0210a-179">140 フォルダに現在のバージョンが反映されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-179">The 140 folder reflects the current version.</span></span> <span data-ttu-id="0210a-180">サンドボックス環境で使用可能なバージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-180">You must use the version that is available in your sandbox environment.</span></span> <span data-ttu-id="0210a-181">したがって、開発環境に [Microsoft SQL Server Management Studio の最新バージョン](https://msdn.microsoft.com/library/mt238290.aspx)をインストールする必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-181">Therefore, you might have to install the [latest version of Microsoft SQL Server Management Studio](https://msdn.microsoft.com/library/mt238290.aspx) in your development environment.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\
SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

<span data-ttu-id="0210a-182">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="0210a-182">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="0210a-183">**ssn(ソース サーバー名)** – エクスポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="0210a-183">**ssn (source server name)** – The name of the SQL Server to export from.</span></span> <span data-ttu-id="0210a-184">このトピックでは、名前は常に **localhost** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-184">For the purposes of this topic, the name should always be **localhost**.</span></span>
- <span data-ttu-id="0210a-185">**sdn(ソース データベース名)** – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="0210a-185">**sdn (source database name)** – The name of the database to export.</span></span>
- <span data-ttu-id="0210a-186">**tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="0210a-186">**tf (target file)** – The path and name of the file to export to.</span></span> <span data-ttu-id="0210a-187">フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0210a-187">The folder should already exist, but the export process will create the file.</span></span>

## <a name="import-the-database"></a><span data-ttu-id="0210a-188">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="0210a-188">Import the database</span></span>

<span data-ttu-id="0210a-189">前の手順で作成された .bacpac ファイルを、LCS プロジェクトの資産ライブラリ内の **データベースのバックアップ** セクションにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="0210a-189">Upload the .bacpac file that was created in the previous step to the **Database backup** section in your LCS project's Asset Library.</span></span> <span data-ttu-id="0210a-190">次に、インポートを開始します。</span><span class="sxs-lookup"><span data-stu-id="0210a-190">Then begin the import.</span></span> <span data-ttu-id="0210a-191">対象となる UAT 環境のデータベースは、ゴールデン構成データベースによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="0210a-191">The target UAT environment's databases will be overwritten by the golden configuration database.</span></span>

[!include [dbmovement-import](../includes/dbmovement-import.md)]

## <a name="perform-master-data-migration"></a><span data-ttu-id="0210a-192">マスター データを移行します。</span><span class="sxs-lookup"><span data-stu-id="0210a-192">Perform master data migration</span></span>

<span data-ttu-id="0210a-193">UAT 環境にゴールデン コンフィギュレーションが適用され、マスター データの移行を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="0210a-193">Now that the UAT environment is hydrated with the golden configuration, you can begin to migrate master data.</span></span> <span data-ttu-id="0210a-194">[データ エンティティを使用して](../data-entities/develop-entity-for-data-migration.md)、このデータの移行を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0210a-194">You can do this data migration by [using data entities](../data-entities/develop-entity-for-data-migration.md).</span></span> <span data-ttu-id="0210a-195">UAT 環境を生産環境にコピーする前にデータ移行アクティビティを完了することをお勧めします。トラブルシューティングのために UAT 環境のデータベースにアクセスするためです。</span><span class="sxs-lookup"><span data-stu-id="0210a-195">We recommend that you complete your data migration activities before you copy the UAT environment to production, because you will have access to the database in the UAT environment for troubleshooting.</span></span>

## <a name="copy-the-sandbox-database-to-production"></a><span data-ttu-id="0210a-196">サンドボックス データベースを生産環境にコピーします。</span><span class="sxs-lookup"><span data-stu-id="0210a-196">Copy the sandbox database to production</span></span>

<span data-ttu-id="0210a-197">モック Go-Live または実際の Go-Live を行う準備ができたら、生産環境に UAT 環境をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="0210a-197">When you're ready to do a mock go-live or actual go-live, you can copy the UAT environment to production.</span></span> <span data-ttu-id="0210a-198">このプロセスは、*切替*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0210a-198">This process is often referred to as *cutover*.</span></span> <span data-ttu-id="0210a-199">実際の Go-Live には複数回切り替えることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0210a-199">We recommend that you do a cutover more than one time before your actual go-live.</span></span> <span data-ttu-id="0210a-200">この方法では、Microsoft にコピー操作の実行を依頼する**生産へのサンドボックス** サービス要求を送信するステップを含む、プロセスの各ステップで詳細な時間見積を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-200">In this way, you can get detailed time estimates for each step of the process, including the step where you submit a **Sandbox to Production** service request to ask that Microsoft run the copy action.</span></span>

> [!NOTE]
> <span data-ttu-id="0210a-201">要求には実稼働環境へのコピーが含まれるので、**データベースを最新の情報に更新要求** タイプの要求を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="0210a-201">You can't use a request of the **Database refresh request** type, because the request involves copying to a production environment.</span></span>

1. <span data-ttu-id="0210a-202">LCS のプロジェクト ホーム ページで、**サービス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-202">In LCS, on the project home page, select **Service requests**.</span></span>
2. <span data-ttu-id="0210a-203">**サービス要求** ページで、**追加** を選択し、**サンドボックスから実稼働環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-203">On the **Service requests** page, select **Add**, and then select **Sandbox to Production**.</span></span>
3. <span data-ttu-id="0210a-204">**サンドボックスから実稼働環境** ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0210a-204">In the **Sandbox to Production** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="0210a-205">**環境名**フィールドで、実稼動環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="0210a-205">In the **Environment name** field, select the production environment.</span></span>
    2. <span data-ttu-id="0210a-206">**ダウンタイム開始日を優先** および **ダウンタイム終了日を優先** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="0210a-206">Set the **Preferred downtime start date** and **Preferred downtime end date** fields.</span></span> <span data-ttu-id="0210a-207">サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0210a-207">The end date must be at least one hour after the start date.</span></span> <span data-ttu-id="0210a-208">要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。</span><span class="sxs-lookup"><span data-stu-id="0210a-208">To help guarantee that resources are available to run the request, submit your request at least 24 hours before your preferred downtime window.</span></span>
    3. <span data-ttu-id="0210a-209">下部にあるチェック ボックスをオンにして、条項に同意します。</span><span class="sxs-lookup"><span data-stu-id="0210a-209">Select the check boxes at the bottom to agree to the terms.</span></span>

## <a name="reconfigure-environment-specific-settings"></a><span data-ttu-id="0210a-210">環境の固有の設定を変更</span><span class="sxs-lookup"><span data-stu-id="0210a-210">Reconfigure environment specific settings</span></span>

<span data-ttu-id="0210a-211">更新が完了した後、LCS で**サインオフ** ボタンを使用し、操作を閉じます。</span><span class="sxs-lookup"><span data-stu-id="0210a-211">After the refresh is completed, use the **Sign off** button in LCS to close out of the operation.</span></span> <span data-ttu-id="0210a-212">その後、環境固有の設定のコンフィギュレーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-212">You then can start to configure the environment-specific settings.</span></span>

<span data-ttu-id="0210a-213">まず、環境にログインします。LCS の**環境の詳細**ページにある管理者アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="0210a-213">First, sign in to the environment by using the admin account that can be found on the **Environment details** page in LCS.</span></span> <span data-ttu-id="0210a-214">再設定の標準的な領域をいくつか次に示します。</span><span class="sxs-lookup"><span data-stu-id="0210a-214">Here are some typical areas of reconfiguration.</span></span> <span data-ttu-id="0210a-215">設定およびインストールされている独立系ソフトウェア ベンダー (ISV) ソリューションによっては、追加の再設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="0210a-215">You might require additional reconfiguration, based on your setup and the independent software vendor (ISV) solutions that are installed:</span></span>

* <span data-ttu-id="0210a-216">**システム管理**\>**設定**\>**バッチ グループ:** 必要なバッチ サーバー グループにさまざまな AOS インスタンスを追加します。</span><span class="sxs-lookup"><span data-stu-id="0210a-216">**System administration** \> **Setup** \> **Batch groups:** Add the various AOS instances to the batch server groups that you require.</span></span>
* <span data-ttu-id="0210a-217">**システム管理**\>**設定**\>**エンティティ店舗:** Microsoft Power BI レポートに必要なさまざまなエンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="0210a-217">**System administration** \> **Setup** \> **Entity Store:** Update the various entities that you require for Microsoft Power BI reporting.</span></span>
* <span data-ttu-id="0210a-218">**システム管理**\>**設定**\>**システム パラメーター:** タスク ガイドの LCS ヘルプ コンフィギュレーションに環境を再接続します。</span><span class="sxs-lookup"><span data-stu-id="0210a-218">**System administration** \> **Setup** \> **System parameters:** Reconnect the environment to the LCS Help configuration for task guides.</span></span>
* <span data-ttu-id="0210a-219">**システム管理**\>**設定**\>**電子メール**\>**パラメータを電子メールで送信:** UAT 環境内で電子メールを使用する場合は、簡易メール転送プロトコル (SMTP) の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="0210a-219">**System administration** \> **Setup** \> **Email** \> **Email parameters:** Enter the Simple Mail Transfer Protocol (SMTP) settings if you use email in your UAT environment.</span></span>
* <span data-ttu-id="0210a-220">**システム管理**\>**照会**\>**バッチ ジョブ:** UAT 環境で実行するジョブを選択し、ステータスを **待機中** に更新します。</span><span class="sxs-lookup"><span data-stu-id="0210a-220">**System administration** \> **Inquiries** \> **Batch jobs:** Select the jobs that you want to run in your UAT environment, and update the status to **Waiting**.</span></span>

> [!NOTE]
> <span data-ttu-id="0210a-221">ベスト プラクティスとして、定期的なアイテムで実行されるすべてのミッション クリティカル バッチ ジョブが作成され、管理者アカウントで実行される必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-221">As a best practice, all mission-critical batch jobs that will run with recurrence should be created and run by the admin account.</span></span> <span data-ttu-id="0210a-222">管理者は、`erp@customer.com` など一般的なユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0210a-222">The admin should be a generic user such as `erp@customer.com`.</span></span> <span data-ttu-id="0210a-223">特定の従業員の Azure Active Directory(Azure AD) アカウントにリンクしないでください。従業員が退職すると、そのアカウントは使用できなくなる可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="0210a-223">It should not be linked to a specific employee's Azure Active Directory (Azure AD) account, because that account might be disabled later if the employee leaves the company.</span></span>

## <a name="open-the-environment-to-users"></a><span data-ttu-id="0210a-224">ユーザーに環境を開く</span><span class="sxs-lookup"><span data-stu-id="0210a-224">Open the environment to users</span></span>

<span data-ttu-id="0210a-225">必要に応じて、システムを構成する場合は、選択したユーザーが環境にアクセスできるようにできます。</span><span class="sxs-lookup"><span data-stu-id="0210a-225">When the system is configured as you require, you can enable selected users to access the environment.</span></span> <span data-ttu-id="0210a-226">デフォルトでは、管理者と Microsoft サービス アカウントを除くすべてのユーザーが無効になります。</span><span class="sxs-lookup"><span data-stu-id="0210a-226">By default, all users except the admin and Microsoft service accounts are disabled.</span></span>

<span data-ttu-id="0210a-227">**システム管理**\>**ユーザー**\>**ユーザー** に移動し、UAT 環境へのアクセスが必要なユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0210a-227">Go to **System administration** \> **Users** \> **Users**, and enable the users that should have access to the UAT environment.</span></span> <span data-ttu-id="0210a-228">多くのユーザーを有効にする必要がある場合、[Microsoft Excel アドイン](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#open-entity-data-in-excel-when-you-start-from-finance-and-operations)を使用してこのタスクをすばやく完了できます。</span><span class="sxs-lookup"><span data-stu-id="0210a-228">If many users must be enabled, you can complete this task more quickly by using the [Microsoft Excel Add-In](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#open-entity-data-in-excel-when-you-start-from-finance-and-operations).</span></span>

## <a name="community-tools"></a><span data-ttu-id="0210a-229">コミュニティ ツール</span><span class="sxs-lookup"><span data-stu-id="0210a-229">Community tools</span></span>

<span data-ttu-id="0210a-230">開発者環境からバックアップ ファイルを準備するための他のツールをお探しですか。</span><span class="sxs-lookup"><span data-stu-id="0210a-230">Are you looking for more tools to help you prepare backup files from your developer environments?</span></span> <span data-ttu-id="0210a-231">他の情報源を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0210a-231">Here are some other sources of information:</span></span>

* <span data-ttu-id="0210a-232">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) には、コミュニティによって作成された多くの貴重なツールがあります。</span><span class="sxs-lookup"><span data-stu-id="0210a-232">[D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) provides many valuable tools that are created by the community.</span></span>
* <span data-ttu-id="0210a-233">[GitHub でコミュニティによって提供されたオープン ソース プロジェクト](https://github.com/search?q=dynamics+365+finance+operations&s=stars)。</span><span class="sxs-lookup"><span data-stu-id="0210a-233">[Community-provided open source projects on GitHub](https://github.com/search?q=dynamics+365+finance+operations&s=stars).</span></span>
