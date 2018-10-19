---
title: "Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを SQL Server をベースとした開発、ビルド、またはデモ環境 (第 1 層または ワンボックス) から Azure SQL データベースをベースしたサンドボックス UAT 環境 (第 2 層以上) に移動する方法について説明します。"
author: maertenm
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 256464
ms.assetid: 4cc5f2aa-dd4e-4981-9607-e75fd1d57941
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: 514f31c1b46707be1df0b28582535131ada46adf
ms.contentlocale: ja-jp
ms.lasthandoff: 09/20/2018

---

# <a name="copy-finance-and-operations-databases-from-sql-server-to-production-azure-sql-database-environments"></a><span data-ttu-id="10823-103">Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする</span><span class="sxs-lookup"><span data-stu-id="10823-103">Copy Finance and Operations databases from SQL Server to production Azure SQL Database environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10823-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを、Microsoft SQL Serverをベースとする環境 (開発、ビルド、またはデモ環境、第 1 層またはワンボックス環境とも呼ばれます) から Microsoft Azure SQL データベースをベースとする環境 (サンドボックス ユーザー受け入れテストの \[UAT\] 環境、第 2 層以上) に移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="10823-104">This topic explains how to move a Microsoft Dynamics 365 for Finance and Operations database from an environment that is based on Microsoft SQL Server (a development, build or demo environment, which is also known as a Tier 1 or one-box environment) to an environment that is based on a Microsoft Azure SQL database (a sandbox user acceptance testing \[UAT\] environment, Tier 2 or higher).</span></span>

<span data-ttu-id="10823-105">通常、このプロセスは稼動前に完了し、システム構成データのみを含むゴールデン (またはシード) データベースを実稼働環境に移行します。</span><span class="sxs-lookup"><span data-stu-id="10823-105">Typically, this process is completed before go-live, to bring a golden (or seed) database that contains only system configuration data into a production environment.</span></span> <span data-ttu-id="10823-106">このプロセスは、すべての状況に適しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="10823-106">This process isn't suitable for all situations.</span></span> <span data-ttu-id="10823-107">たとえば、既存の実際の展開に対して新しい法人のデータをインポートするためには、このプロセスを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="10823-107">For example, you should not use this process to import data for a new legal entity for an existing live deployment.</span></span> <span data-ttu-id="10823-108">このタイプの場合、[プロセス データ パッケージ](../lcs-solutions/process-data-packages-lcs-solutions.md)または[データ エンティティ データ パッケージ](../data-entities/data-entities-data-packages.md)を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10823-108">In situations of this type, we recommend that you use [process data packages](../lcs-solutions/process-data-packages-lcs-solutions.md) or [data entity data packages](../data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="10823-109">ゴールデン データベースを実稼働環境に移行するためにサポートされている手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="10823-109">Here is the supported procedure for bringing a golden database into a production environment.</span></span>

1. <span data-ttu-id="10823-110">顧客やパートナーは、SQL Server のデータベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-110">A customer or partner exports the database from SQL Server.</span></span>
2. <span data-ttu-id="10823-111">顧客またはパートナーは、データベースを Azure SQL データベース上で実行されるサンドボックス環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-111">The customer or partner imports the database into a sandbox environment that runs on an Azure SQL database.</span></span>
3. <span data-ttu-id="10823-112">Microsoft Dynamics Lifecycle Services (LCS) では、顧客またはパートナーが**その他の要求**タイプのサービス要求を送信して、Microsoft Dynamics のサポート エンジニアリング (DSE) チームにサンドボックス データベースを実稼動環境に移動してもらうよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="10823-112">In Microsoft Dynamics Lifecycle Services (LCS), the customer or partner submits a service request of the **Other request** type to ask that the Microsoft Dynamics Support Engineering (DSE) team move the sandbox database to the production environment.</span></span>
4. <span data-ttu-id="10823-113">DSE チームでは、データベースをサンドボックス環境から実稼働環境にコピーします。</span><span class="sxs-lookup"><span data-stu-id="10823-113">The DSE team copies the database from the sandbox environment to the production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="10823-114">Microsoft は、運用する前にのみデータベースを実稼働環境にコピーする要求を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="10823-114">Microsoft accepts requests to copy a database into a production environment only before go-live.</span></span>

<span data-ttu-id="10823-115">データベースの移動中に、sqlpackage.exe コマンド ライン ツールを使用して、SQL Server からデータベースをエクスポートし、Azure SQL データベースにインポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-115">During the process for moving a database, the sqlpackage.exe command-line tool is used to export the database from SQL Server and import it into an Azure SQL database.</span></span> <span data-ttu-id="10823-116">エクスポートされたデータ ファイルのファイル名拡張子は .bacpac なので、プロセスは多くの場合 *bacpac プロセス*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="10823-116">Because the file name extension for the exported data file is .bacpac, the process is often referred to as the *bacpac process*.</span></span>

<span data-ttu-id="10823-117">データベース移動のための高レベルのプロセスを次に示します。</span><span class="sxs-lookup"><span data-stu-id="10823-117">Here is the high-level process for a database move.</span></span>

1. <span data-ttu-id="10823-118">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="10823-118">Create a copy of the source database.</span></span>
2. <span data-ttu-id="10823-119">データベースの準備のためスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-119">Run a script to prepare the database.</span></span>
3. <span data-ttu-id="10823-120">SQL Server からデータベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-120">Export the database from SQL Server.</span></span>
4. <span data-ttu-id="10823-121">Azure SQL データベースにデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-121">Import the database into an Azure SQL database.</span></span>
5. <span data-ttu-id="10823-122">データベースの更新のためスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-122">Run a script to update the database.</span></span>

<span data-ttu-id="10823-123">問題が発生する場合は、このトピックの最後にある「既知の問題と制限事項」を参照します。</span><span class="sxs-lookup"><span data-stu-id="10823-123">If you encounter issues, see the "Known issues and limitations" section at the end of this topic.</span></span> <span data-ttu-id="10823-124">トラブルシューティング方法について説明し、パフォーマンスのヒントを紹介して、コピー処理の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="10823-124">It explains how to troubleshoot, gives performance tips, and explains limitations of the copy process.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10823-125">前提条件</span><span class="sxs-lookup"><span data-stu-id="10823-125">Prerequisites</span></span>

- <span data-ttu-id="10823-126">ソース環境 (ソース データベースが作成された環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-126">The source environment (the environment where the source database was created) must run a version of the Finance and Operations platform that is earlier than or the same as the version of the platform that the destination environment runs.</span></span>
- <span data-ttu-id="10823-127">サンドボックス環境からデータベースをインポートするには、データベースをインポートする環境で同じバージョンの SQL Server Management Studio を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-127">To import a database from a sandbox environment, you must be running the same version of SQL Server Management Studio that is in the environment you will be importing the database to.</span></span> <span data-ttu-id="10823-128">これにより、サンドボックス環境で Application Object Server (AOS) を実行するコンピューターに [SQL Server Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx)をインストールする必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="10823-128">This may require you to install the [latest version of SQL Server Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx) on the computer that runs Application Object Server (AOS) in the sandbox environment.</span></span> <span data-ttu-id="10823-129">AOS コンピューターで、bacpac エクスポートを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="10823-129">You can then do the bacpac export on that AOS computer.</span></span> <span data-ttu-id="10823-130">この要件は 2 つの理由があります。</span><span class="sxs-lookup"><span data-stu-id="10823-130">There are two reasons for this requirement:</span></span>

    - <span data-ttu-id="10823-131">SQL Server のサンドボックス インスタンスに対するインターネット プロトコル (IP) アクセス制限のため、その環境内のコンピュータのみがインスタンスに接続できます。</span><span class="sxs-lookup"><span data-stu-id="10823-131">Because of an Internet Protocol (IP) access restriction on the sandbox instance of SQL Server, only computers in that environment can connect to the instance.</span></span>
    - <span data-ttu-id="10823-132">エクスポートされた \*.bacpac ファイルは、Management Studio のバージョン固有の機能に依存する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10823-132">The exported \*.bacpac file may be dependent on version specific features of Management Studio.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10823-133">環境に、Microsoft Dynamics 365 for Retail コンポーネントが含まれている場合、開始する前にいくつかの環境固有の値を手動で保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-133">If your environment includes Microsoft Dynamics 365 for Retail components, you must manually store some environment-specific values before you begin.</span></span> <span data-ttu-id="10823-134">詳細については、「小売環境の追加手順」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10823-134">For more information, see the "Additional steps for Retail environments" section.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="10823-135">準備</span><span class="sxs-lookup"><span data-stu-id="10823-135">Before you begin</span></span>

<span data-ttu-id="10823-136">暗号化された環境固有の値を新しい環境にインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="10823-136">Encrypted and environment-specific values can't be imported into a new environment.</span></span> <span data-ttu-id="10823-137">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-137">After you've completed the import, you must re-enter some data from your source environment in your target environment.</span></span>

### <a name="document-the-values-of-encrypted-fields"></a><span data-ttu-id="10823-138">暗号化されたフィールドの値を文書化</span><span class="sxs-lookup"><span data-stu-id="10823-138">Document the values of encrypted fields</span></span>

<span data-ttu-id="10823-139">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="10823-139">Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</span></span> <span data-ttu-id="10823-140">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-140">Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</span></span> <span data-ttu-id="10823-141">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="10823-141">New values that are entered in encrypted fields after an import will be readable.</span></span> <span data-ttu-id="10823-142">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="10823-142">The following fields are affected.</span></span> <span data-ttu-id="10823-143">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="10823-143">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="10823-144">フィールド名</span><span class="sxs-lookup"><span data-stu-id="10823-144">Field name</span></span>                                               | <span data-ttu-id="10823-145">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="10823-145">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="10823-146">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="10823-146">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="10823-147">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-147">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="10823-148">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="10823-148">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="10823-149">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-149">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="10823-150">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="10823-150">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="10823-151">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="10823-151">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="10823-152">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="10823-152">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="10823-153">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-153">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="10823-154">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="10823-154">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="10823-155">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-155">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="10823-156">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-156">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="10823-157">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="10823-157">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="10823-158">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="10823-158">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="10823-159">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。</span><span class="sxs-lookup"><span data-stu-id="10823-159">It previously appeared in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="10823-160">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="10823-160">SysEmailSMPTPassword.Password</span></span>                            | <span data-ttu-id="10823-161">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-161">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="10823-162">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="10823-162">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="10823-163">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-163">This field is used internally by AOS.</span></span> <span data-ttu-id="10823-164">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="10823-164">It can be ignored.</span></span> |
| <span data-ttu-id="10823-165">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="10823-165">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="10823-166">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-166">This field is used internally by AOS.</span></span> <span data-ttu-id="10823-167">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="10823-167">It can be ignored.</span></span> |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a><span data-ttu-id="10823-168">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</span><span class="sxs-lookup"><span data-stu-id="10823-168">If you're running Retail components, document encrypted and environment-specific values</span></span>

<span data-ttu-id="10823-169">次のページの値は、環境固有またはデータベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="10823-169">The values on the following pages are either environment-specific or encrypted in the database.</span></span> <span data-ttu-id="10823-170">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="10823-170">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="10823-171">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="10823-171">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="10823-172">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="10823-172">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

## <a name="create-a-copy-of-the-source-database"></a><span data-ttu-id="10823-173">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="10823-173">Create a copy of the source database</span></span>

<span data-ttu-id="10823-174">ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。</span><span class="sxs-lookup"><span data-stu-id="10823-174">Because you must delete database users before you can export the source SQL Server database, you should create a copy of that database.</span></span> <span data-ttu-id="10823-175">元のデータベースを修正する代わりに、コピーで作業することができます。</span><span class="sxs-lookup"><span data-stu-id="10823-175">You can then work with the copy instead of modifying the original database.</span></span> <span data-ttu-id="10823-176">次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。</span><span class="sxs-lookup"><span data-stu-id="10823-176">The following script backs up the default AxDB database and then restores it to the same instance under a new name.</span></span> <span data-ttu-id="10823-177">このスクリプトを使用するには、最初に D:\\backups のパスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="10823-177">To use this script, first verify that the path D:\\backups exists.</span></span>

```
BACKUP DATABASE [AxDB] TO DISK = N'D:\Backups\axdb_golden.bak' WITH NOFORMAT, NOINIT,
NAME = N'AxDB_golden-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION, STATS = 10
GO
RESTORE DATABASE [AxDB_CopyForExport] FROM DISK = N'D:\Backups\axdb_golden.bak' WITH FILE = 1,
MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_CopyForExport.mdf',
MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForExport_Log.ldf',
NOUNLOAD, STATS = 5
```

## <a name="prepare-the-database"></a><span data-ttu-id="10823-178">データベースの準備</span><span class="sxs-lookup"><span data-stu-id="10823-178">Prepare the database</span></span>

<span data-ttu-id="10823-179">次のスクリプトを、前のセクションで作成した AxDB\_CopyForExport データベースに対して実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-179">Run the following script against the AxDB\_CopyForExport database that you created in the previous section.</span></span> <span data-ttu-id="10823-180">このスクリプトは、次の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="10823-180">This script makes the following changes:</span></span>

- <span data-ttu-id="10823-181">**SysGlobalConfiguration** フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。</span><span class="sxs-lookup"><span data-stu-id="10823-181">Set the **SysGlobalConfiguration** flag to inform Finance and Operations that the database is Azure-based.</span></span>
- <span data-ttu-id="10823-182">XU\_DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="10823-182">Remove a reference to tempDB in the XU\_DisableEnableNonClusteredIndexes procedure.</span></span> <span data-ttu-id="10823-183">Azure SQL データベースでは、tempDB の参照が許可されていません。</span><span class="sxs-lookup"><span data-stu-id="10823-183">References to tempDB aren't allowed in an Azure SQL database.</span></span> <span data-ttu-id="10823-184">データベース同期プロセスは後で照会を再作成します。</span><span class="sxs-lookup"><span data-stu-id="10823-184">The database synchronization process will re-create the reference later.</span></span>
- <span data-ttu-id="10823-185">Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。</span><span class="sxs-lookup"><span data-stu-id="10823-185">Drop users, because Microsoft Windows users are forbidden in Azure SQL databases.</span></span> <span data-ttu-id="10823-186">他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-186">Other users must be re-created later, so that they're correctly linked to the appropriate sign-in on the target server.</span></span>
- <span data-ttu-id="10823-187">暗号化されたハードウェア プロファイルの merchand プロパティの消去</span><span class="sxs-lookup"><span data-stu-id="10823-187">Clear encrypted hardware profile merchand properties</span></span>

<span data-ttu-id="10823-188">データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="10823-188">A successful export and import of the database requires all these changes.</span></span>

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

## <a name="export-the-database-from-sql-server"></a><span data-ttu-id="10823-189">SQL Server からデータベースをエクスポート</span><span class="sxs-lookup"><span data-stu-id="10823-189">Export the database from SQL Server</span></span>

<span data-ttu-id="10823-190">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-190">Open a **Command Prompt** window and run the following commands.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10823-191">**140** フォルダーは、現在のバージョンを反映しており、サンドボックス環境で使用可能なバージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-191">The **140** folder reflects the current version, you are required to use the version that is available in your sandbox environment.</span></span> <span data-ttu-id="10823-192">これにより、開発環境に [Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx) をインストールする必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="10823-192">This may require you to install the [latest version of Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx) in your development environment.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\
SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

<span data-ttu-id="10823-193">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="10823-193">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="10823-194">**ssn(ソース サーバー名)** – エクスポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="10823-194">**ssn (source server name)** – The name of the SQL Server to export from.</span></span> <span data-ttu-id="10823-195">このトピックでは、名前は常に **localhost** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-195">For the purposes of this topic, the name should always be **localhost**.</span></span>
- <span data-ttu-id="10823-196">**sdn(ソース データベース名)** – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="10823-196">**sdn (source database name)** – The name of the database to export.</span></span>
- <span data-ttu-id="10823-197">**tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="10823-197">**tf (target file)** – The path and name of the file to export to.</span></span> <span data-ttu-id="10823-198">フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="10823-198">The folder should already exist, but the export process will create the file.</span></span>

## <a name="import-the-database-into-an-azure-sql-database"></a><span data-ttu-id="10823-199">Azure SQL データベースへのデータベースのインポート</span><span class="sxs-lookup"><span data-stu-id="10823-199">Import the database into an Azure SQL database</span></span>

<span data-ttu-id="10823-200">前のセクションで生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</span><span class="sxs-lookup"><span data-stu-id="10823-200">Copy the .bacpac file that was generated in the previous section to the AOS computer in the target environment.</span></span> <span data-ttu-id="10823-201">ゴールデン データベースの標準的な .bacpac ファイルは、100 MB より小さくなります。</span><span class="sxs-lookup"><span data-stu-id="10823-201">A typical .bacpac file for a golden database will be smaller than 100 MB.</span></span> <span data-ttu-id="10823-202">したがって、リモート デスクトップ プロトコル (RDP) ウィンドウを使用してファイルをコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-202">Therefore, you can copy and paste the file through a Remote Desktop Protocol (RDP) window.</span></span> <span data-ttu-id="10823-203">.Bacpac ファイルが 100 MB よりも大きい場合、[Azure ストレージ アカウントにアップロード](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/)し、対象となる AOS コンピューターにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="10823-203">If the .bacpac file is much larger than 100 MB, [upload it to an Azure storage account](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/), and then download it to the target AOS computer.</span></span>

> [!NOTE]
> <span data-ttu-id="10823-204">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="10823-204">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="10823-205">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-205">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> <span data-ttu-id="10823-206">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10823-206">For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</span></span> <span data-ttu-id="10823-207">(詳細については、「既知の問題と制限事項」セクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="10823-207">(For more information, see the "Known issues and limitations" section.)</span></span>

<span data-ttu-id="10823-208">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-208">Open a **Command Prompt** window and run the following commands.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10823-209">SqlPackage.exe のバージョンは、.bacpac ファイルのエクスポートに使用するバージョンと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-209">The version of SqlPackage.exe must match the version used to export the .bacpac file.</span></span> <span data-ttu-id="10823-210">[Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx) のインストールが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="10823-210">You may be required to install the [latest version of Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx).</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure SQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P2
```

<span data-ttu-id="10823-211">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="10823-211">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="10823-212">**tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="10823-212">**tsn (target server name)** – The name of the Azure SQL Database server to import to.</span></span> <span data-ttu-id="10823-213">名前を LCS で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-213">You can find the name in LCS.</span></span> <span data-ttu-id="10823-214">接尾語 **database.windows.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="10823-214">Add the suffix **database.windows.net** to it.</span></span>
- <span data-ttu-id="10823-215">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="10823-215">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="10823-216">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="10823-216">The database should **not** already exist.</span></span> <span data-ttu-id="10823-217">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="10823-217">The import process will create it.</span></span>
- <span data-ttu-id="10823-218">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="10823-218">**sf (source file)** – The path and name of the file to import from.</span></span>
- <span data-ttu-id="10823-219">**tu(ターゲット ユーザー)** – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="10823-219">**tu (target user)** – The SQL user name for the target Azure SQL database instance.</span></span> <span data-ttu-id="10823-220">標準の **sqladmin** ユーザーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10823-220">We recommend that you use the standard **sqladmin** user.</span></span> <span data-ttu-id="10823-221">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="10823-221">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="10823-222">**tp(ターゲット パスワード)** – ターゲットの Azure SQL データベース ユーザーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="10823-222">**tp (target password)** – The password for the target Azure SQL database user.</span></span>
- <span data-ttu-id="10823-223">**DatabaseServiceObjective** – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="10823-223">**DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2, or P4.</span></span> <span data-ttu-id="10823-224">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</span><span class="sxs-lookup"><span data-stu-id="10823-224">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="10823-225">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-225">To query the service level objective of the current database, run the following query.</span></span>

    ```
    SELECT  d.name,   
        slo.*    
    FROM sys.databases d   
    JOIN sys.database_service_objectives slo    
    ON d.database_id = slo.database_id;  
    ```

<span data-ttu-id="10823-226">次の警告メッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="10823-226">You will receive the following warning message.</span></span> <span data-ttu-id="10823-227">これは無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="10823-227">You can safely ignore it.</span></span>

> <span data-ttu-id="10823-228">ターゲット プラットフォームとして SQL Server 2016 を指定するプロジェクトは、Microsoft Azure SQL データベース v12 で互換性の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10823-228">A project which specifies SQL Server 2016 as the target platform may experience compatibility issues with Microsoft Azure SQL Database v12.</span></span>

> [!WARNING] 
> <span data-ttu-id="10823-229">どの Finance and Operations 環境でも、長期間にわたってデータベースのコピーを保持することはできません。</span><span class="sxs-lookup"><span data-stu-id="10823-229">Retaining copies of the database for an extended period is not allowed in any Finance and Operations environment.</span></span> <span data-ttu-id="10823-230">Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。</span><span class="sxs-lookup"><span data-stu-id="10823-230">Microsoft reserves the right to delete any copies of the database older than 7 days without any prior notice.</span></span>

## <a name="update-the-database"></a><span data-ttu-id="10823-231">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="10823-231">Update the database</span></span>

<span data-ttu-id="10823-232">インポートされたデータベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-232">Run the following script against the imported database.</span></span> <span data-ttu-id="10823-233">スクリプトでは次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-233">The script performs the following actions:</span></span>

- <span data-ttu-id="10823-234">データベース ユーザーを再作成します。</span><span class="sxs-lookup"><span data-stu-id="10823-234">Re-create database users.</span></span>
- <span data-ttu-id="10823-235">適切な実績パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="10823-235">Set the correct performance parameters.</span></span>
- <span data-ttu-id="10823-236">SQL Query Store 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="10823-236">Enable the SQL Query Store feature.</span></span>

> [!NOTE]
> <span data-ttu-id="10823-237">テナント ID を最後の 3 つのクエリに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-237">You must add the tenant ID to the last three queries.</span></span> <span data-ttu-id="10823-238">この値はターゲット環境内の既存のデータベースで SysServiceConfigurationSetting テーブルをクエリすることにより見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-238">You can find this value by querying the SysServiceConfigurationSetting table in an existing database in the target environment.</span></span>

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

ALTER DATABASE SCOPED CONFIGURATION  SET MAXDOP=2
ALTER DATABASE SCOPED CONFIGURATION  SET LEGACY_CARDINALITY_ESTIMATION=ON
ALTER DATABASE SCOPED CONFIGURATION  SET PARAMETER_SNIFFING= ON
ALTER DATABASE SCOPED CONFIGURATION  SET QUERY_OPTIMIZER_HOTFIXES=OFF

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

## <a name="synchronize-the-database"></a><span data-ttu-id="10823-239">データベースの同期</span><span class="sxs-lookup"><span data-stu-id="10823-239">Synchronize the database</span></span>

1. <span data-ttu-id="10823-240">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="10823-240">Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="10823-241">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="10823-241">These services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="10823-242">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-242">After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</span></span>

    - <span data-ttu-id="10823-243">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="10823-243">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="10823-244">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="10823-244">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="10823-245">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="10823-245">Management Reporter 2012 Process Service (on business intelligence \[BI\] computers only)</span></span>

2. <span data-ttu-id="10823-246">bacpac インポートが行われた AOS コンピューターで、Management Studio の次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-246">On the AOS computer where the bacpac import was done, run the following script in Management Studio.</span></span> <span data-ttu-id="10823-247">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="10823-247">This script renames the original database and then renames the newly imported database so that it uses the original database name.</span></span> <span data-ttu-id="10823-248">この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</span><span class="sxs-lookup"><span data-stu-id="10823-248">In this example, the original database was named axdb\_123456789, and the newly imported database was named importeddb.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10823-249">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="10823-249">Make sure that the you're using the SQL Server 2016 version of Management Studio.</span></span>

    ```
    ALTER DATABASE [axdb_123456789] MODIFY NAME = [axdb_123456789_original]
    ALTER DATABASE [importeddb] MODIFY NAME = [axdb_123456789]
    ```

3. <span data-ttu-id="10823-250">データベースを同期させます。</span><span class="sxs-lookup"><span data-stu-id="10823-250">Synchronize the database.</span></span> <span data-ttu-id="10823-251">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="10823-251">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

    ```
    cd F:\AosService\WebRoot\bin

    Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "F:\AosService\PackagesLocalDirectory" -metadatadir F:\AosService\PackagesLocalDirectory -sqluser axdbadmin -sqlserver <Azure SQL database server name>.database.windows.net -sqldatabase <database name> -setupmode sync -syncmode fullall -isazuresql true -sqlpwd <SQL password> >log.txt 2>&1
    ```

4. <span data-ttu-id="10823-252">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="10823-252">Use services.msc to restart the services that you stopped earlier:</span></span>

    - <span data-ttu-id="10823-253">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="10823-253">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="10823-254">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="10823-254">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="10823-255">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="10823-255">Management Reporter 2012 Process Service (on BI computers only)</span></span>

5. <span data-ttu-id="10823-256">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-256">At this point, you can open the Finance and Operations application URL and sign in.</span></span> <span data-ttu-id="10823-257">アプリケーションが予期したとおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="10823-257">Verify that the application works as you expect.</span></span> <span data-ttu-id="10823-258">次に、bacpac のインポートを行った AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</span><span class="sxs-lookup"><span data-stu-id="10823-258">Then drop the original database by running the following script in Management Studio on the AOS computer where you did the bacpac import.</span></span>

    ```
    DROP DATABASE [axdb_123456789_original]
    ```

### <a name="enable-change-tracking"></a><span data-ttu-id="10823-259">変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="10823-259">Enable change tracking</span></span>
<span data-ttu-id="10823-260">ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="10823-260">If change tracking was enabled in the source database, ensure to enable change tracking again in the newly provisioned database in the target environment using the ALTER DATABASE command.</span></span>
```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

<span data-ttu-id="10823-261">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-261">To ensure current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</span></span> <span data-ttu-id="10823-262">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="10823-262">This can be done on any entity as this is needed to trigger the refresh of store procedure.</span></span>

### <a name="re-provision-the-target-environment"></a><span data-ttu-id="10823-263">対象の環境を再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="10823-263">Re-provision the target environment</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a><span data-ttu-id="10823-264">財務報告データベースのリセット</span><span class="sxs-lookup"><span data-stu-id="10823-264">Reset the Financial Reporting database</span></span>

<span data-ttu-id="10823-265">Management Reporter という以前の名前を持った財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります</span><span class="sxs-lookup"><span data-stu-id="10823-265">If you're using Financial Reporting, which was previously named Management Reporter, you must reset the Financial Reporting database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span>

## <a name="submit-a-service-request-to-copy-the-database"></a><span data-ttu-id="10823-266">データベースをコピーするサービス要求を送信</span><span class="sxs-lookup"><span data-stu-id="10823-266">Submit a service request to copy the database</span></span>

<span data-ttu-id="10823-267">ゴールデン データベースを実稼働環境にコピーするには、LCS に **Other request** タイプのサービス要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-267">To copy the golden database to a production environment, you must submit a service request of the **Other request** type in LCS.</span></span> <span data-ttu-id="10823-268">この要求では、Microsoft がコピー操作を実行することを求めます。</span><span class="sxs-lookup"><span data-stu-id="10823-268">In this request, you ask that Microsoft run the copy action.</span></span>

> [!NOTE]
> <span data-ttu-id="10823-269">要求には実稼働環境へのコピーが含まれるので、**データベースを最新の情報に更新要求** タイプの要求を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="10823-269">You can't use a request of the **Database refresh request** type, because the request involves copying to a production environment.</span></span>

1. <span data-ttu-id="10823-270">LCS で、ハンバーガー アイコンを選択してから、**作業項目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-270">In LCS, select the hamburger icon, and then select **Work items**.</span></span>

    <span data-ttu-id="10823-271">[![作業項目](./media/lcsworkitemsmenu.png)](./media/lcsworkitemsmenu.png)</span><span class="sxs-lookup"><span data-stu-id="10823-271">[![Work items](./media/lcsworkitemsmenu.png)](./media/lcsworkitemsmenu.png)</span></span>

2. <span data-ttu-id="10823-272">**作業項目**ページで、**追加**を選択し、**その他の要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-272">On the **Work items** page, select **Add**, and then select **Other request**.</span></span>
3. <span data-ttu-id="10823-273">**その他の要求**ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="10823-273">In the **Other requests** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="10823-274">**環境名**フィールドで、実稼動環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-274">In the **Environment name** field, select the production environment.</span></span>
    2. <span data-ttu-id="10823-275">**ダウンタイム開始日を優先** および **ダウンタイム終了日を優先** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="10823-275">Set the **Preferred downtime start date** and **Preferred downtime end date** fields.</span></span> <span data-ttu-id="10823-276">サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="10823-276">The end date must be at least one hour after the start date.</span></span> <span data-ttu-id="10823-277">要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。</span><span class="sxs-lookup"><span data-stu-id="10823-277">To help guarantee that resources are available to run the request, submit your request at least 24 hours before your preferred downtime window.</span></span>
    3. <span data-ttu-id="10823-278">**要求**フィールドに次の詳細を入力します。**これはサンドボックス環境 &lt;ソース サンドボックス環境名&gt; から実稼働へのゴールデン データベースのコピーに関する要求です。これにより、実稼働中のデータベースが上書きされることを承認します。**</span><span class="sxs-lookup"><span data-stu-id="10823-278">In the **Request** field, enter the following details: **This is a request for a golden database copy from the sandbox environment &lt;source sandbox environment name&gt; to production. I acknowledge that this will overwrite the database currently in production.**</span></span>
    4. <span data-ttu-id="10823-279">下部にあるチェック ボックスをオンにして、条項に同意します。</span><span class="sxs-lookup"><span data-stu-id="10823-279">Select the check boxes at the bottom to agree to the terms.</span></span>

## <a name="additional-steps-for-retail-environments"></a><span data-ttu-id="10823-280">小売環境の追加手順</span><span class="sxs-lookup"><span data-stu-id="10823-280">Additional steps for Retail environments</span></span>

<span data-ttu-id="10823-281">環境に、Retail のコンポーネントが含まれている場合、追加の手順を実行して、データベースのインポート後に環境が機能することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10823-281">If your environment includes Retail components, you must perform additional steps to help guarantee that the environment will work after the database import.</span></span>

### <a name="re-enter-encrypted-and-environment-specific-values-in-the-target-database"></a><span data-ttu-id="10823-282">ターゲット データベースの暗号化された環境固有の値を再入力</span><span class="sxs-lookup"><span data-stu-id="10823-282">Re-enter encrypted and environment-specific values in the target database</span></span>

<span data-ttu-id="10823-283">次のページの値は、データベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="10823-283">The values on the following pages are encrypted in the database.</span></span> <span data-ttu-id="10823-284">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="10823-284">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="10823-285">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="10823-285">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="10823-286">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="10823-286">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

<span data-ttu-id="10823-287">ターゲット システムで、これらのページを開き、前に記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10823-287">In the target system, open these pages, and enter the values that you documented earlier.</span></span>

## <a name="re-enter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a><span data-ttu-id="10823-288">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</span><span class="sxs-lookup"><span data-stu-id="10823-288">Re-enter data from encrypted and environment-specific fields in the target database</span></span>

<span data-ttu-id="10823-289">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10823-289">In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</span></span> <span data-ttu-id="10823-290">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="10823-290">The following fields are affected.</span></span> <span data-ttu-id="10823-291">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="10823-291">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="10823-292">フィールド名</span><span class="sxs-lookup"><span data-stu-id="10823-292">Field name</span></span>                                               | <span data-ttu-id="10823-293">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="10823-293">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="10823-294">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="10823-294">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="10823-295">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-295">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="10823-296">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="10823-296">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="10823-297">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-297">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="10823-298">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="10823-298">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="10823-299">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="10823-299">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="10823-300">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="10823-300">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="10823-301">このフィールドは DIXF で使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-301">This field is used by DIXF.</span></span> |
| <span data-ttu-id="10823-302">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="10823-302">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="10823-303">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-303">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="10823-304">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-304">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="10823-305">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="10823-305">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="10823-306">このフィールドは、AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="10823-306">This field has been obsolete since AX 7.0 (February 2016).</span></span> <span data-ttu-id="10823-307">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。</span><span class="sxs-lookup"><span data-stu-id="10823-307">It previously appeared in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="10823-308">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="10823-308">SysEmailSMPTPassword.Password</span></span>                            | <span data-ttu-id="10823-309">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-309">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="10823-310">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="10823-310">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="10823-311">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-311">This field is used internally by AOS.</span></span> <span data-ttu-id="10823-312">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="10823-312">It can be ignored.</span></span> |
| <span data-ttu-id="10823-313">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="10823-313">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="10823-314">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="10823-314">This field is used internally by AOS.</span></span> <span data-ttu-id="10823-315">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="10823-315">It can be ignored.</span></span> |

## <a name="known-issues-and-limitations"></a><span data-ttu-id="10823-316">既知の問題と制限事項</span><span class="sxs-lookup"><span data-stu-id="10823-316">Known issues and limitations</span></span>

### <a name="i-cant-download-the-management-studio-installer"></a><span data-ttu-id="10823-317">Management Studio インストーラーをダウンロードできません</span><span class="sxs-lookup"><span data-stu-id="10823-317">I can't download the Management Studio installer</span></span>

<span data-ttu-id="10823-318">Management Studio インストーラーをダウンロードしようとすると、次のメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="10823-318">When you try to download the Management Studio installer, you might receive the following message:</span></span>

> <span data-ttu-id="10823-319">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="10823-319">Your current security settings do not allow this file to be downloaded.</span></span>

<span data-ttu-id="10823-320">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="10823-320">To work around this issue, follow these steps to enable file downloads.</span></span>

1. <span data-ttu-id="10823-321">Web ブラウザーで**インターネット オプション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="10823-321">In your web browser, open **Internet options**.</span></span>
2. <span data-ttu-id="10823-322">**セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-322">On the **Security** tab, select the **Internet** zone, and then select **Custom level**.</span></span>
3. <span data-ttu-id="10823-323">**ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="10823-323">Scroll to **Downloads**, and then, under **File download**, select the **Enable** option.</span></span>

### <a name="performance"></a><span data-ttu-id="10823-324">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="10823-324">Performance</span></span>

<span data-ttu-id="10823-325">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="10823-325">The following guidelines can help you achieve optimal performance:</span></span>

- <span data-ttu-id="10823-326">常に Azure SQL データベース インスタンスと同じ Azure データ センター内にあるコンピューターからエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-326">Always export from a computer that is in the same Azure datacenter as the Azure SQL database instance.</span></span> <span data-ttu-id="10823-327">実際、このガイドラインはサンドボックス データベースのコピーをエクスポートするときに、サンドボックス AOS コンピューターからエクスポートする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="10823-327">In practice, this guideline means that when you export a copy of your sandbox database, you should export it from the sandbox AOS computer.</span></span>
- <span data-ttu-id="10823-328">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</span><span class="sxs-lookup"><span data-stu-id="10823-328">Always import the .bacpac file locally on the computer that runs the SQL Server instance.</span></span> <span data-ttu-id="10823-329">リモート コンピューターで Management Studio からインポートしないでください。</span><span class="sxs-lookup"><span data-stu-id="10823-329">Don't import it from Management Studio on a remote computer.</span></span>
- <span data-ttu-id="10823-330">Azure でホストされている 1 ボックス環境では、エクスポートするときに D ドライブに .bacpac ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="10823-330">In a one-box environment that is hosted in Azure, put the .bacpac file on drive D when you export it.</span></span> <span data-ttu-id="10823-331">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure コンピューター 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) Azure サポート チームのブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10823-331">(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure computers, see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) post on the Azure Support Team blog.</span></span>
- <span data-ttu-id="10823-332">SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/en-us/library/ms175935.aspx) を実行するアカウントに権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="10823-332">Grant the account that runs the SQL Server Windows service [Instance File Initialization](https://msdn.microsoft.com/en-us/library/ms175935.aspx) rights.</span></span> <span data-ttu-id="10823-333">この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="10823-333">In this way, you can help improve the speed of the import process and the speed of a restore from a \*.bak file.</span></span> <span data-ttu-id="10823-334">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="10823-334">For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</span></span>
- <span data-ttu-id="10823-335">Management Studio の Azure SQL データベースからエクスポートおよびインポートするオプションを使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="10823-335">We recommend that you not use the option to export and import from Azure SQL Database in Management Studio.</span></span> <span data-ttu-id="10823-336">(このオプションは、**データ層アプリケーションのエクスポート**とも呼ばれます。) 大規模なデータベースにはメモリーの制限があるため、このオプションは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="10823-336">(This option is also known as **Export data tier application**.) You should not use this option because there can be memory limitations for larger databases.</span></span>

