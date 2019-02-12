---
redirect_url: /dynamics365/unified-operations/dev-itpro/database/dbmovement-operations
title: "Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを SQL Server をベースとした開発、ビルド、またはデモ環境 (第 1 層または ワンボックス) から Azure SQL データベースをベースしたサンドボックス UAT 環境 (第 2 層以上) に移動する方法について説明します。"
author: laneswenka
manager: AnnBe
ms.date: 10/26/2018
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
ms.author: laneswenka
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 20f399701df76bb4adf0948291732bca64fb8d5a
ms.openlocfilehash: e081cdd84dc37f9211047a5dba74e5b993ebdc2d
ms.contentlocale: ja-jp
ms.lasthandoff: 02/12/2019

---

# <a name="copy-finance-and-operations-databases-from-sql-server-to-production-azure-sql-database-environments"></a><span data-ttu-id="b5d19-103">Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする</span><span class="sxs-lookup"><span data-stu-id="b5d19-103">Copy Finance and Operations databases from SQL Server to production Azure SQL Database environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5d19-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations データベースを、Microsoft SQL Serverをベースとする環境 (開発、ビルド、またはデモ環境、第 1 層またはワンボックス環境とも呼ばれます) から Microsoft Azure SQL データベースをベースとする環境 (サンドボックス ユーザー受け入れテストの \[UAT\] 環境、第 2 層以上) に移動する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-104">This topic explains how to move a Microsoft Dynamics 365 for Finance and Operations database from an environment that is based on Microsoft SQL Server (a development, build or demo environment, which is also known as a Tier 1 or one-box environment) to an environment that is based on a Microsoft Azure SQL database (a sandbox user acceptance testing \[UAT\] environment, Tier 2 or higher).</span></span>

<span data-ttu-id="b5d19-105">通常、このプロセスは稼動前に完了し、システム構成データのみを含むゴールデン (またはシード) データベースを実稼働環境に移行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-105">Typically, this process is completed before go-live, to bring a golden (or seed) database that contains only system configuration data into a production environment.</span></span> <span data-ttu-id="b5d19-106">このプロセスは、すべての状況に適しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-106">This process isn't suitable for all situations.</span></span> <span data-ttu-id="b5d19-107">たとえば、既存の実際の展開に対して新しい法人のデータをインポートするためには、このプロセスを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-107">For example, you should not use this process to import data for a new legal entity for an existing live deployment.</span></span> <span data-ttu-id="b5d19-108">このタイプの場合、[プロセス データ パッケージ](../lcs-solutions/process-data-packages-lcs-solutions.md)または[データ エンティティ データ パッケージ](../data-entities/data-entities-data-packages.md)を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-108">In situations of this type, we recommend that you use [process data packages](../lcs-solutions/process-data-packages-lcs-solutions.md) or [data entity data packages](../data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="b5d19-109">ゴールデン データベースを実稼働環境に移行するためにサポートされている手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-109">Here is the supported procedure for bringing a golden database into a production environment.</span></span>

1. <span data-ttu-id="b5d19-110">顧客やパートナーは、SQL Server のデータベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-110">A customer or partner exports the database from SQL Server.</span></span>
2. <span data-ttu-id="b5d19-111">顧客またはパートナーは、データベースを Azure SQL データベース上で実行されるサンドボックス環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-111">The customer or partner imports the database into a sandbox environment that runs on an Azure SQL database.</span></span>
3. <span data-ttu-id="b5d19-112">Microsoft Dynamics Lifecycle Services (LCS) では、顧客またはパートナーが**サンドボックスから実稼働環境**タイプのサービス要求を送信して、Microsoft Dynamics のサポート エンジニアリング (DSE) チームにサンドボックス データベースを実稼動環境に移動してもらうよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-112">In Microsoft Dynamics Lifecycle Services (LCS), the customer or partner submits a service request of the **Sandbox to Production** type to ask that the Microsoft Dynamics Support Engineering (DSE) team move the sandbox database to the production environment.</span></span>
4. <span data-ttu-id="b5d19-113">DSE チームでは、データベースをサンドボックス環境から実稼働環境にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-113">The DSE team copies the database from the sandbox environment to the production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="b5d19-114">Microsoft は、運用する前にのみデータベースを実稼働環境にコピーする要求を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-114">Microsoft accepts requests to copy a database into a production environment only before go-live.</span></span>

<span data-ttu-id="b5d19-115">データベースの移動中に、sqlpackage.exe コマンド ライン ツールを使用して、SQL Server からデータベースをエクスポートし、Azure SQL データベースにインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-115">During the process for moving a database, the sqlpackage.exe command-line tool is used to export the database from SQL Server and import it into an Azure SQL database.</span></span> <span data-ttu-id="b5d19-116">エクスポートされたデータ ファイルのファイル名拡張子は .bacpac なので、プロセスは多くの場合 *bacpac プロセス*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-116">Because the file name extension for the exported data file is .bacpac, the process is often referred to as the *bacpac process*.</span></span>

<span data-ttu-id="b5d19-117">データベース移動のための高レベルのプロセスを次に示します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-117">Here is the high-level process for a database move.</span></span>

1. <span data-ttu-id="b5d19-118">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-118">Create a copy of the source database.</span></span>
2. <span data-ttu-id="b5d19-119">データベースの準備のためスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-119">Run a script to prepare the database.</span></span>
3. <span data-ttu-id="b5d19-120">SQL Server からデータベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-120">Export the database from SQL Server.</span></span>
4. <span data-ttu-id="b5d19-121">Azure SQL データベースにデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-121">Import the database into an Azure SQL database.</span></span>
5. <span data-ttu-id="b5d19-122">データベースの更新のためスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-122">Run a script to update the database.</span></span>

<span data-ttu-id="b5d19-123">問題が発生する場合は、このトピックの最後にある「既知の問題と制限事項」を参照します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-123">If you encounter issues, see the "Known issues and limitations" section at the end of this topic.</span></span> <span data-ttu-id="b5d19-124">トラブルシューティング方法について説明し、パフォーマンスのヒントを紹介して、コピー処理の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-124">It explains how to troubleshoot, gives performance tips, and explains limitations of the copy process.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5d19-125">前提条件</span><span class="sxs-lookup"><span data-stu-id="b5d19-125">Prerequisites</span></span>

- <span data-ttu-id="b5d19-126">ソース環境 (ソース データベースが作成された環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-126">The source environment (the environment where the source database was created) must run a version of the Finance and Operations platform that is earlier than or the same as the version of the platform that the destination environment runs.</span></span>
- <span data-ttu-id="b5d19-127">サンドボックス環境からデータベースをインポートするには、データベースをインポートする環境で同じバージョンの SQL Server Management Studio を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-127">To import a database from a sandbox environment, you must be running the same version of SQL Server Management Studio that is in the environment you will be importing the database to.</span></span> <span data-ttu-id="b5d19-128">これにより、サンドボックス環境で Application Object Server (AOS) を実行するコンピューターに [SQL Server Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx)をインストールする必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-128">This may require you to install the [latest version of SQL Server Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx) on the computer that runs Application Object Server (AOS) in the sandbox environment.</span></span> <span data-ttu-id="b5d19-129">AOS コンピューターで、bacpac エクスポートを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-129">You can then do the bacpac export on that AOS computer.</span></span> <span data-ttu-id="b5d19-130">この要件は 2 つの理由があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-130">There are two reasons for this requirement:</span></span>

    - <span data-ttu-id="b5d19-131">SQL Server のサンドボックス インスタンスに対するインターネット プロトコル (IP) アクセス制限のため、その環境内のコンピュータのみがインスタンスに接続できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-131">Because of an Internet Protocol (IP) access restriction on the sandbox instance of SQL Server, only computers in that environment can connect to the instance.</span></span>
    - <span data-ttu-id="b5d19-132">エクスポートされた \*.bacpac ファイルは、Management Studio のバージョン固有の機能に依存する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-132">The exported \*.bacpac file may be dependent on version specific features of Management Studio.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5d19-133">環境に、Microsoft Dynamics 365 for Retail コンポーネントが含まれている場合、開始する前にいくつかの環境固有の値を手動で保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-133">If your environment includes Microsoft Dynamics 365 for Retail components, you must manually store some environment-specific values before you begin.</span></span> <span data-ttu-id="b5d19-134">詳細については、「小売環境の追加手順」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-134">For more information, see the "Additional steps for Retail environments" section.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b5d19-135">準備</span><span class="sxs-lookup"><span data-stu-id="b5d19-135">Before you begin</span></span>

### <a name="supported-sql-server-collation"></a><span data-ttu-id="b5d19-136">サポートされる SQL Server の照合順序</span><span class="sxs-lookup"><span data-stu-id="b5d19-136">Supported SQL Server collation</span></span>

<span data-ttu-id="b5d19-137">クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、**SQL_Latin1_General_CP1_CI_AS** です。</span><span class="sxs-lookup"><span data-stu-id="b5d19-137">The only supported collation for Finance and Operations databases in the cloud is **SQL_Latin1_General_CP1_CI_AS**.</span></span> <span data-ttu-id="b5d19-138">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-138">Please ensure that your SQL Server and database collations in development environments are set to this.</span></span> <span data-ttu-id="b5d19-139">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-139">Also ensure that any configuration environments that are published to Sandbox have this same collation.</span></span>

### <a name="document-the-values-of-encrypted-fields"></a><span data-ttu-id="b5d19-140">暗号化されたフィールドの値を文書化</span><span class="sxs-lookup"><span data-stu-id="b5d19-140">Document the values of encrypted fields</span></span>

<span data-ttu-id="b5d19-141">暗号化された環境固有の値を新しい環境にインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-141">Encrypted and environment-specific values can't be imported into a new environment.</span></span> <span data-ttu-id="b5d19-142">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-142">After you've completed the import, you must re-enter some data from your source environment in your target environment.</span></span>

<span data-ttu-id="b5d19-143">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-143">Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</span></span> <span data-ttu-id="b5d19-144">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-144">Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</span></span> <span data-ttu-id="b5d19-145">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-145">New values that are entered in encrypted fields after an import will be readable.</span></span> <span data-ttu-id="b5d19-146">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-146">The following fields are affected.</span></span> <span data-ttu-id="b5d19-147">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-147">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="b5d19-148">フィールド名</span><span class="sxs-lookup"><span data-stu-id="b5d19-148">Field name</span></span>                                               | <span data-ttu-id="b5d19-149">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="b5d19-149">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="b5d19-150">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="b5d19-150">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="b5d19-151">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-151">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="b5d19-152">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="b5d19-152">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="b5d19-153">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-153">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="b5d19-154">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="b5d19-154">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="b5d19-155">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-155">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="b5d19-156">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="b5d19-156">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="b5d19-157">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-157">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="b5d19-158">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="b5d19-158">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="b5d19-159">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-159">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="b5d19-160">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-160">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="b5d19-161">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="b5d19-161">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="b5d19-162">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="b5d19-162">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="b5d19-163">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。</span><span class="sxs-lookup"><span data-stu-id="b5d19-163">It previously appeared in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="b5d19-164">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="b5d19-164">SysEmailSMPTPassword.Password</span></span>                            | <span data-ttu-id="b5d19-165">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-165">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="b5d19-166">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="b5d19-166">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="b5d19-167">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-167">This field is used internally by AOS.</span></span> <span data-ttu-id="b5d19-168">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-168">It can be ignored.</span></span> |
| <span data-ttu-id="b5d19-169">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="b5d19-169">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="b5d19-170">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-170">This field is used internally by AOS.</span></span> <span data-ttu-id="b5d19-171">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-171">It can be ignored.</span></span> |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a><span data-ttu-id="b5d19-172">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-172">If you're running Retail components, document encrypted and environment-specific values</span></span>

<span data-ttu-id="b5d19-173">次のページの値は、環境固有またはデータベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="b5d19-173">The values on the following pages are either environment-specific or encrypted in the database.</span></span> <span data-ttu-id="b5d19-174">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-174">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="b5d19-175">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-175">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="b5d19-176">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="b5d19-176">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

## <a name="create-a-copy-of-the-source-database"></a><span data-ttu-id="b5d19-177">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-177">Create a copy of the source database</span></span>

<span data-ttu-id="b5d19-178">ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-178">Because you must delete database users before you can export the source SQL Server database, you should create a copy of that database.</span></span> <span data-ttu-id="b5d19-179">元のデータベースを修正する代わりに、コピーで作業することができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-179">You can then work with the copy instead of modifying the original database.</span></span> <span data-ttu-id="b5d19-180">次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-180">The following script backs up the default AxDB database and then restores it to the same instance under a new name.</span></span> <span data-ttu-id="b5d19-181">このスクリプトを使用するには、最初に D:\\backups のパスが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-181">To use this script, first verify that the path D:\\backups exists.</span></span>

```
BACKUP DATABASE [AxDB] TO DISK = N'D:\Backups\axdb_golden.bak' WITH NOFORMAT, NOINIT,
NAME = N'AxDB_golden-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION, STATS = 10
GO
RESTORE DATABASE [AxDB_CopyForExport] FROM DISK = N'D:\Backups\axdb_golden.bak' WITH FILE = 1,
MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_CopyForExport.mdf',
MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForExport_Log.ldf',
NOUNLOAD, STATS = 5
```

## <a name="prepare-the-database"></a><span data-ttu-id="b5d19-182">データベースの準備</span><span class="sxs-lookup"><span data-stu-id="b5d19-182">Prepare the database</span></span>

<span data-ttu-id="b5d19-183">次のスクリプトを、前のセクションで作成した AxDB\_CopyForExport データベースに対して実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-183">Run the following script against the AxDB\_CopyForExport database that you created in the previous section.</span></span> <span data-ttu-id="b5d19-184">このスクリプトは、次の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="b5d19-184">This script makes the following changes:</span></span>

- <span data-ttu-id="b5d19-185">**SysGlobalConfiguration** フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-185">Set the **SysGlobalConfiguration** flag to inform Finance and Operations that the database is Azure-based.</span></span>
- <span data-ttu-id="b5d19-186">XU\_DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-186">Remove a reference to tempDB in the XU\_DisableEnableNonClusteredIndexes procedure.</span></span> <span data-ttu-id="b5d19-187">Azure SQL データベースでは、tempDB の参照が許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-187">References to tempDB aren't allowed in an Azure SQL database.</span></span> <span data-ttu-id="b5d19-188">データベース同期プロセスは後で照会を再作成します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-188">The database synchronization process will re-create the reference later.</span></span>
- <span data-ttu-id="b5d19-189">Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-189">Drop users, because Microsoft Windows users are forbidden in Azure SQL databases.</span></span> <span data-ttu-id="b5d19-190">他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-190">Other users must be re-created later, so that they're correctly linked to the appropriate sign-in on the target server.</span></span>
- <span data-ttu-id="b5d19-191">暗号化されたハードウェア プロファイルの merchand プロパティの消去</span><span class="sxs-lookup"><span data-stu-id="b5d19-191">Clear encrypted hardware profile merchand properties</span></span>

<span data-ttu-id="b5d19-192">データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="b5d19-192">A successful export and import of the database requires all these changes.</span></span>

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

## <a name="export-the-database-from-sql-server"></a><span data-ttu-id="b5d19-193">SQL Server からデータベースをエクスポート</span><span class="sxs-lookup"><span data-stu-id="b5d19-193">Export the database from SQL Server</span></span>

<span data-ttu-id="b5d19-194">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-194">Open a **Command Prompt** window and run the following commands.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5d19-195">**140** フォルダーは、現在のバージョンを反映しており、サンドボックス環境で使用可能なバージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-195">The **140** folder reflects the current version, you are required to use the version that is available in your sandbox environment.</span></span> <span data-ttu-id="b5d19-196">これにより、開発環境に [Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx) をインストールする必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-196">This may require you to install the [latest version of Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx) in your development environment.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\
SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

<span data-ttu-id="b5d19-197">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-197">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="b5d19-198">**ssn(ソース サーバー名)** – エクスポートする SQL Server の名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-198">**ssn (source server name)** – The name of the SQL Server to export from.</span></span> <span data-ttu-id="b5d19-199">このトピックでは、名前は常に **localhost** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-199">For the purposes of this topic, the name should always be **localhost**.</span></span>
- <span data-ttu-id="b5d19-200">**sdn(ソース データベース名)** – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-200">**sdn (source database name)** – The name of the database to export.</span></span>
- <span data-ttu-id="b5d19-201">**tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-201">**tf (target file)** – The path and name of the file to export to.</span></span> <span data-ttu-id="b5d19-202">フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-202">The folder should already exist, but the export process will create the file.</span></span>

## <a name="import-the-database-into-an-azure-sql-database"></a><span data-ttu-id="b5d19-203">Azure SQL データベースへのデータベースのインポート</span><span class="sxs-lookup"><span data-stu-id="b5d19-203">Import the database into an Azure SQL database</span></span>

<span data-ttu-id="b5d19-204">前のセクションで生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-204">Copy the .bacpac file that was generated in the previous section to the AOS computer in the target environment.</span></span> <span data-ttu-id="b5d19-205">ゴールデン データベースの標準的な .bacpac ファイルは、100 MB より小さくなります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-205">A typical .bacpac file for a golden database will be smaller than 100 MB.</span></span> <span data-ttu-id="b5d19-206">したがって、リモート デスクトップ プロトコル (RDP) ウィンドウを使用してファイルをコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-206">Therefore, you can copy and paste the file through a Remote Desktop Protocol (RDP) window.</span></span> <span data-ttu-id="b5d19-207">.Bacpac ファイルが 100 MB よりも大きい場合、[Azure ストレージ アカウントにアップロード](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/)し、対象となる AOS コンピューターにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-207">If the .bacpac file is much larger than 100 MB, [upload it to an Azure storage account](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/), and then download it to the target AOS computer.</span></span>

> [!NOTE]
> <span data-ttu-id="b5d19-208">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-208">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="b5d19-209">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-209">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> <span data-ttu-id="b5d19-210">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-210">For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</span></span> <span data-ttu-id="b5d19-211">(詳細については、「既知の問題と制限事項」セクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="b5d19-211">(For more information, see the "Known issues and limitations" section.)</span></span>

<span data-ttu-id="b5d19-212">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-212">Open a **Command Prompt** window and run the following commands.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5d19-213">SqlPackage.exe のバージョンは、.bacpac ファイルのエクスポートに使用するバージョンと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-213">The version of SqlPackage.exe must match the version used to export the .bacpac file.</span></span> <span data-ttu-id="b5d19-214">[Management Studio の最新バージョン](https://msdn.microsoft.com/en-us/library/mt238290.aspx) のインストールが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-214">You may be required to install the [latest version of Management Studio](https://msdn.microsoft.com/en-us/library/mt238290.aspx).</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure SQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P2
```

<span data-ttu-id="b5d19-215">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-215">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="b5d19-216">**tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-216">**tsn (target server name)** – The name of the Azure SQL Database server to import to.</span></span> <span data-ttu-id="b5d19-217">名前を LCS で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-217">You can find the name in LCS.</span></span> <span data-ttu-id="b5d19-218">接尾語 **database.windows.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-218">Add the suffix **database.windows.net** to it.</span></span>
- <span data-ttu-id="b5d19-219">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-219">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="b5d19-220">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="b5d19-220">The database should **not** already exist.</span></span> <span data-ttu-id="b5d19-221">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-221">The import process will create it.</span></span>
- <span data-ttu-id="b5d19-222">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="b5d19-222">**sf (source file)** – The path and name of the file to import from.</span></span>
- <span data-ttu-id="b5d19-223">**tu(ターゲット ユーザー)** – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="b5d19-223">**tu (target user)** – The SQL user name for the target Azure SQL database instance.</span></span> <span data-ttu-id="b5d19-224">標準の **sqladmin** ユーザーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-224">We recommend that you use the standard **sqladmin** user.</span></span> <span data-ttu-id="b5d19-225">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-225">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="b5d19-226">**tp(ターゲット パスワード)** – ターゲットの Azure SQL データベース ユーザーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="b5d19-226">**tp (target password)** – The password for the target Azure SQL database user.</span></span>
- <span data-ttu-id="b5d19-227">**DatabaseServiceObjective** – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-227">**DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2, or P4.</span></span> <span data-ttu-id="b5d19-228">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-228">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="b5d19-229">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-229">To query the service level objective of the current database, run the following query.</span></span>

    ```
    SELECT  d.name,   
        slo.*    
    FROM sys.databases d   
    JOIN sys.database_service_objectives slo    
    ON d.database_id = slo.database_id;  
    ```

<span data-ttu-id="b5d19-230">次の警告メッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-230">You will receive the following warning message.</span></span> <span data-ttu-id="b5d19-231">これは無視してかまいません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-231">You can safely ignore it.</span></span>

> <span data-ttu-id="b5d19-232">ターゲット プラットフォームとして SQL Server 2016 を指定するプロジェクトは、Microsoft Azure SQL データベース v12 で互換性の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-232">A project which specifies SQL Server 2016 as the target platform may experience compatibility issues with Microsoft Azure SQL Database v12.</span></span>

> [!WARNING] 
> <span data-ttu-id="b5d19-233">どの Finance and Operations 環境でも、長期間にわたってデータベースのコピーを保持することはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-233">Retaining copies of the database for an extended period is not allowed in any Finance and Operations environment.</span></span> <span data-ttu-id="b5d19-234">Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-234">Microsoft reserves the right to delete any copies of the database older than 7 days without any prior notice.</span></span>

## <a name="update-the-database"></a><span data-ttu-id="b5d19-235">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="b5d19-235">Update the database</span></span>

<span data-ttu-id="b5d19-236">インポートされたデータベースに対して、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-236">Run the following script against the imported database.</span></span> <span data-ttu-id="b5d19-237">スクリプトでは次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-237">The script performs the following actions:</span></span>

- <span data-ttu-id="b5d19-238">データベース ユーザーを再作成します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-238">Re-create database users.</span></span>
- <span data-ttu-id="b5d19-239">適切な実績パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-239">Set the correct performance parameters.</span></span>
- <span data-ttu-id="b5d19-240">SQL Query Store 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-240">Enable the SQL Query Store feature.</span></span>

> [!NOTE]
> <span data-ttu-id="b5d19-241">テナント ID を最後の 3 つのクエリに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-241">You must add the tenant ID to the last three queries.</span></span> <span data-ttu-id="b5d19-242">この値はターゲット環境内の既存のデータベースで SysServiceConfigurationSetting テーブルをクエリすることにより見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-242">You can find this value by querying the SysServiceConfigurationSetting table in an existing database in the target environment.</span></span>

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

## <a name="synchronize-the-database"></a><span data-ttu-id="b5d19-243">データベースの同期</span><span class="sxs-lookup"><span data-stu-id="b5d19-243">Synchronize the database</span></span>

1. <span data-ttu-id="b5d19-244">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-244">Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="b5d19-245">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-245">These services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="b5d19-246">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-246">After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</span></span>

    - <span data-ttu-id="b5d19-247">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="b5d19-247">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="b5d19-248">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="b5d19-248">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="b5d19-249">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="b5d19-249">Management Reporter 2012 Process Service (on business intelligence \[BI\] computers only)</span></span>

2. <span data-ttu-id="b5d19-250">bacpac インポートが行われた AOS コンピューターで、Management Studio の次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-250">On the AOS computer where the bacpac import was done, run the following script in Management Studio.</span></span> <span data-ttu-id="b5d19-251">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-251">This script renames the original database and then renames the newly imported database so that it uses the original database name.</span></span> <span data-ttu-id="b5d19-252">この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</span><span class="sxs-lookup"><span data-stu-id="b5d19-252">In this example, the original database was named axdb\_123456789, and the newly imported database was named importeddb.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5d19-253">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-253">Make sure that the you're using the SQL Server 2016 version of Management Studio.</span></span>

    ```
    ALTER DATABASE [axdb_123456789] MODIFY NAME = [axdb_123456789_original]
    ALTER DATABASE [importeddb] MODIFY NAME = [axdb_123456789]
    ```

3. <span data-ttu-id="b5d19-254">データベースを同期させます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-254">Synchronize the database.</span></span> <span data-ttu-id="b5d19-255">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-255">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

    ```
    cd F:\AosService\WebRoot\bin

    Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "F:\AosService\PackagesLocalDirectory" -metadatadir F:\AosService\PackagesLocalDirectory -sqluser axdbadmin -sqlserver <Azure SQL database server name>.database.windows.net -sqldatabase <database name> -setupmode sync -syncmode fullall -isazuresql true -sqlpwd <SQL password> >log.txt 2>&1
    ```

4. <span data-ttu-id="b5d19-256">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-256">Use services.msc to restart the services that you stopped earlier:</span></span>

    - <span data-ttu-id="b5d19-257">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="b5d19-257">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="b5d19-258">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="b5d19-258">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="b5d19-259">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="b5d19-259">Management Reporter 2012 Process Service (on BI computers only)</span></span>

5. <span data-ttu-id="b5d19-260">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-260">At this point, you can open the Finance and Operations application URL and sign in.</span></span> <span data-ttu-id="b5d19-261">アプリケーションが予期したとおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-261">Verify that the application works as you expect.</span></span> <span data-ttu-id="b5d19-262">次に、bacpac のインポートを行った AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-262">Then drop the original database by running the following script in Management Studio on the AOS computer where you did the bacpac import.</span></span>

    ```
    DROP DATABASE [axdb_123456789_original]
    ```

### <a name="enable-change-tracking"></a><span data-ttu-id="b5d19-263">変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="b5d19-263">Enable change tracking</span></span>
<span data-ttu-id="b5d19-264">ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-264">If change tracking was enabled in the source database, ensure to enable change tracking again in the newly provisioned database in the target environment using the ALTER DATABASE command.</span></span>
```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

<span data-ttu-id="b5d19-265">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-265">To ensure current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</span></span> <span data-ttu-id="b5d19-266">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-266">This can be done on any entity as this is needed to trigger the refresh of store procedure.</span></span>

### <a name="re-provision-the-target-environment"></a><span data-ttu-id="b5d19-267">対象の環境を再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="b5d19-267">Re-provision the target environment</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a><span data-ttu-id="b5d19-268">財務報告データベースのリセット</span><span class="sxs-lookup"><span data-stu-id="b5d19-268">Reset the Financial Reporting database</span></span>

<span data-ttu-id="b5d19-269">Management Reporter という以前の名前を持った財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります</span><span class="sxs-lookup"><span data-stu-id="b5d19-269">If you're using Financial Reporting, which was previously named Management Reporter, you must reset the Financial Reporting database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span>

## <a name="submit-a-service-request-to-copy-the-database"></a><span data-ttu-id="b5d19-270">データベースをコピーするサービス要求を送信</span><span class="sxs-lookup"><span data-stu-id="b5d19-270">Submit a service request to copy the database</span></span>

<span data-ttu-id="b5d19-271">ゴールデン データベースを実稼働環境にコピーするには、LCS に **サンドボックスから実稼働環境** タイプのサービス要求を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-271">To copy the golden database to a production environment, you must submit a service request of the **Sandbox to Production** type in LCS.</span></span> <span data-ttu-id="b5d19-272">この要求では、Microsoft がコピー操作を実行することを求めます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-272">In this request, you ask that Microsoft run the copy action.</span></span>

> [!NOTE]
> <span data-ttu-id="b5d19-273">要求には実稼働環境へのコピーが含まれるので、**データベースを最新の情報に更新要求** タイプの要求を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-273">You can't use a request of the **Database refresh request** type, because the request involves copying to a production environment.</span></span>

1. <span data-ttu-id="b5d19-274">LCS のプロジェクト ホーム ページで、**サービス要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-274">In LCS, on the Project home page, select **Service requests**.</span></span>
2. <span data-ttu-id="b5d19-275">**サービス要求** ページで、**追加** を選択し、**サンドボックスから実稼働環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-275">On the **Service requests** page, select **Add**, and then select **Sandbox to Production**.</span></span>
3. <span data-ttu-id="b5d19-276">**サンドボックスから実稼働環境** ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b5d19-276">In the **Sandbox to Production** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b5d19-277">**環境名**フィールドで、実稼動環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-277">In the **Environment name** field, select the production environment.</span></span>
    2. <span data-ttu-id="b5d19-278">**ダウンタイム開始日を優先** および **ダウンタイム終了日を優先** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-278">Set the **Preferred downtime start date** and **Preferred downtime end date** fields.</span></span> <span data-ttu-id="b5d19-279">サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-279">The end date must be at least one hour after the start date.</span></span> <span data-ttu-id="b5d19-280">要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-280">To help guarantee that resources are available to run the request, submit your request at least 24 hours before your preferred downtime window.</span></span>
    3. <span data-ttu-id="b5d19-281">下部にあるチェック ボックスをオンにして、条項に同意します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-281">Select the check boxes at the bottom to agree to the terms.</span></span>

## <a name="additional-steps-for-retail-environments"></a><span data-ttu-id="b5d19-282">小売環境の追加手順</span><span class="sxs-lookup"><span data-stu-id="b5d19-282">Additional steps for Retail environments</span></span>

<span data-ttu-id="b5d19-283">環境に、Retail のコンポーネントが含まれている場合、追加の手順を実行して、データベースのインポート後に環境が機能することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-283">If your environment includes Retail components, you must perform additional steps to help guarantee that the environment will work after the database import.</span></span>

### <a name="re-enter-encrypted-and-environment-specific-values-in-the-target-database"></a><span data-ttu-id="b5d19-284">ターゲット データベースの暗号化された環境固有の値を再入力</span><span class="sxs-lookup"><span data-stu-id="b5d19-284">Re-enter encrypted and environment-specific values in the target database</span></span>

<span data-ttu-id="b5d19-285">次のページの値は、データベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="b5d19-285">The values on the following pages are encrypted in the database.</span></span> <span data-ttu-id="b5d19-286">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-286">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="b5d19-287">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-287">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="b5d19-288">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="b5d19-288">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

<span data-ttu-id="b5d19-289">ターゲット システムで、これらのページを開き、前に記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-289">In the target system, open these pages, and enter the values that you documented earlier.</span></span>

## <a name="re-enter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a><span data-ttu-id="b5d19-290">ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力</span><span class="sxs-lookup"><span data-stu-id="b5d19-290">Re-enter data from encrypted and environment-specific fields in the target database</span></span>

<span data-ttu-id="b5d19-291">Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-291">In the Finance and Operations client, enter the values that you documented for the encrypted and environment-specific fields.</span></span> <span data-ttu-id="b5d19-292">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-292">The following fields are affected.</span></span> <span data-ttu-id="b5d19-293">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-293">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="b5d19-294">フィールド名</span><span class="sxs-lookup"><span data-stu-id="b5d19-294">Field name</span></span>                                               | <span data-ttu-id="b5d19-295">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="b5d19-295">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="b5d19-296">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="b5d19-296">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="b5d19-297">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-297">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="b5d19-298">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="b5d19-298">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="b5d19-299">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-299">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="b5d19-300">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="b5d19-300">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="b5d19-301">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-301">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="b5d19-302">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="b5d19-302">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="b5d19-303">このフィールドは DIXF で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-303">This field is used by DIXF.</span></span> |
| <span data-ttu-id="b5d19-304">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="b5d19-304">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="b5d19-305">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-305">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="b5d19-306">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-306">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="b5d19-307">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="b5d19-307">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="b5d19-308">このフィールドは、AX 7.0 以降 (2016 年 2 月) に廃止されました。</span><span class="sxs-lookup"><span data-stu-id="b5d19-308">This field has been obsolete since AX 7.0 (February 2016).</span></span> <span data-ttu-id="b5d19-309">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。</span><span class="sxs-lookup"><span data-stu-id="b5d19-309">It previously appeared in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="b5d19-310">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="b5d19-310">SysEmailSMPTPassword.Password</span></span>                            | <span data-ttu-id="b5d19-311">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-311">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="b5d19-312">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="b5d19-312">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="b5d19-313">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-313">This field is used internally by AOS.</span></span> <span data-ttu-id="b5d19-314">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-314">It can be ignored.</span></span> |
| <span data-ttu-id="b5d19-315">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="b5d19-315">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="b5d19-316">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-316">This field is used internally by AOS.</span></span> <span data-ttu-id="b5d19-317">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-317">It can be ignored.</span></span> |

## <a name="known-issues-and-limitations"></a><span data-ttu-id="b5d19-318">既知の問題と制限事項</span><span class="sxs-lookup"><span data-stu-id="b5d19-318">Known issues and limitations</span></span>

### <a name="i-cant-download-the-management-studio-installer"></a><span data-ttu-id="b5d19-319">Management Studio インストーラーをダウンロードできません</span><span class="sxs-lookup"><span data-stu-id="b5d19-319">I can't download the Management Studio installer</span></span>

<span data-ttu-id="b5d19-320">Management Studio インストーラーをダウンロードしようとすると、次のメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b5d19-320">When you try to download the Management Studio installer, you might receive the following message:</span></span>

> <span data-ttu-id="b5d19-321">現在のセキュリティ設定では、このファイルをダウンロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d19-321">Your current security settings do not allow this file to be downloaded.</span></span>

<span data-ttu-id="b5d19-322">この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-322">To work around this issue, follow these steps to enable file downloads.</span></span>

1. <span data-ttu-id="b5d19-323">Web ブラウザーで**インターネット オプション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-323">In your web browser, open **Internet options**.</span></span>
2. <span data-ttu-id="b5d19-324">**セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-324">On the **Security** tab, select the **Internet** zone, and then select **Custom level**.</span></span>
3. <span data-ttu-id="b5d19-325">**ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-325">Scroll to **Downloads**, and then, under **File download**, select the **Enable** option.</span></span>

### <a name="performance"></a><span data-ttu-id="b5d19-326">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="b5d19-326">Performance</span></span>

<span data-ttu-id="b5d19-327">次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-327">The following guidelines can help you achieve optimal performance:</span></span>

- <span data-ttu-id="b5d19-328">常に Azure SQL データベース インスタンスと同じ Azure データ センター内にあるコンピューターからエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-328">Always export from a computer that is in the same Azure datacenter as the Azure SQL database instance.</span></span> <span data-ttu-id="b5d19-329">実際、このガイドラインはサンドボックス データベースのコピーをエクスポートするときに、サンドボックス AOS コンピューターからエクスポートする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-329">In practice, this guideline means that when you export a copy of your sandbox database, you should export it from the sandbox AOS computer.</span></span>
- <span data-ttu-id="b5d19-330">常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-330">Always import the .bacpac file locally on the computer that runs the SQL Server instance.</span></span> <span data-ttu-id="b5d19-331">リモート コンピューターで Management Studio からインポートしないでください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-331">Don't import it from Management Studio on a remote computer.</span></span>
- <span data-ttu-id="b5d19-332">Azure でホストされている 1 ボックス環境では、エクスポートするときに D ドライブに .bacpac ファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-332">In a one-box environment that is hosted in Azure, put the .bacpac file on drive D when you export it.</span></span> <span data-ttu-id="b5d19-333">(ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure コンピューター 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) Azure サポート チームのブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-333">(A one-box environment is also known as a Tier 1 environment.) For more information about the temporary drive on Azure computers, see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) post on the Azure Support Team blog.</span></span>
- <span data-ttu-id="b5d19-334">SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/en-us/library/ms175935.aspx) を実行するアカウントに権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="b5d19-334">Grant the account that runs the SQL Server Windows service [Instance File Initialization](https://msdn.microsoft.com/en-us/library/ms175935.aspx) rights.</span></span> <span data-ttu-id="b5d19-335">この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-335">In this way, you can help improve the speed of the import process and the speed of a restore from a \*.bak file.</span></span> <span data-ttu-id="b5d19-336">開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b5d19-336">For a developer environment, you can easily make sure that the account that runs the SQL Server service has these rights by setting SQL Server to run as the axlocaladmin account.</span></span>
- <span data-ttu-id="b5d19-337">Management Studio の Azure SQL データベースからエクスポートおよびインポートするオプションを使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b5d19-337">We recommend that you not use the option to export and import from Azure SQL Database in Management Studio.</span></span> <span data-ttu-id="b5d19-338">(このオプションは、**データ層アプリケーションのエクスポート**とも呼ばれます。) 大規模なデータベースにはメモリーの制限があるため、このオプションは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="b5d19-338">(This option is also known as **Export data tier application**.) You should not use this option because there can be memory limitations for larger databases.</span></span>

