---
title: "後で復元する Finance and Operations のデータベースのコピーをエクスポートする"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations database のデータベースをファイルにエクスポートし、そのファイルを同じインスタンスまたはアプリケーションの別のインスタンスに再度インポートする方法について説明します。"
author: LaneSwenka
manager: AnnBe
ms.date: 10/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 269254
ms.assetid: 7464b180-8ace-4b65-8b53-ba608d0611e1
ms.search.region: Global
ms.author: LaneSwenka
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 3aec4a71d49ac09e8237f2ebf763de7f103dec61
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="export-copies-of-finance-and-operations-databases-to-restore-later"></a><span data-ttu-id="fd5f7-103">後で復元する Finance and Operations のデータベースのコピーをエクスポートする</span><span class="sxs-lookup"><span data-stu-id="fd5f7-103">Export copies of Finance and Operations databases to restore later</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd5f7-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations database のデータベースをファイルにエクスポートし、そのファイルを同じインスタンスまたはアプリケーションの別のインスタンスに再度インポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-104">This topic explains how to export a Microsoft Dynamics 365 for Finance and Operations database to a file, and then reimport that file into the same instance or another instance of the application.</span></span> <span data-ttu-id="fd5f7-105">このステップは、非実稼働環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-105">This procedure can be used only in non-production environments.</span></span>

> [!NOTE]
> <span data-ttu-id="fd5f7-106">このトピックは、サンド ボックスのユーザー受け入れテスト (UAT) 環境に接続されている Microsoft Azure SQL データベースに適用されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-106">This topic applies to Microsoft Azure SQL databases that are connected to sandbox user acceptance testing (UAT) environments.</span></span>

<span data-ttu-id="fd5f7-107">Finance and Operations データベース プロセスのコピーを保持する場合がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-107">There are several situations where you might want to keep a copy of a Finance and Operations database process:</span></span>

- <span data-ttu-id="fd5f7-108">後で復元できる戦略的なバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-108">You want to make strategic backups that you can restore to later.</span></span> <span data-ttu-id="fd5f7-109">たとえば、主要コード更新の前または後に、後に参照に使用できるようコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-109">For example, before or after a major code update, you might want copies that you can use for reference later.</span></span>
- <span data-ttu-id="fd5f7-110">破壊試験の前にデータベースをバックアップし、テストの完了後にデータベースを復元する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-110">You want to back up a database before destructive testing and then restore it after the testing is completed.</span></span>
- <span data-ttu-id="fd5f7-111">Finance and Operations の新しいメジャー リリースへのアップグレードのとき、このプロセスを使用して、古いテスト データベースをエクスポートし、新しいバージョンに持ち出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-111">When you upgrade to a new major release of Finance and Operations, you can use this process to export your old test database and bring it forward to the new version.</span></span>

<span data-ttu-id="fd5f7-112">Microsoft は Azure SQL データベース環境を過去 35 日間以内の特定の時点に復元できる標準機能も提供しています。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-112">Be aware that Microsoft also provides a standard feature that lets you restore an Azure SQL database environment to a specific point in time within the last 35 days.</span></span> <span data-ttu-id="fd5f7-113">この復元はサービス要求を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-113">This restore is done via a service request.</span></span> <span data-ttu-id="fd5f7-114">詳細については、[非実稼働環境でのポイントインタイム データベース復元の要求](request-point-in-time-restore.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-114">For more information, see [Request a point-in-time database restore on a non-production environment](request-point-in-time-restore.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd5f7-115">このトピックでは、Finance and Operations データベースのコピーを保持する、サポートされている唯一の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-115">This topic documents the only supported method of retaining a copy of a Finance and Operations database.</span></span> <span data-ttu-id="fd5f7-116">Finance and Operations 環境で、Azure SQL データベースのコピーを実行し続けることはできません。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-116">In a Finance and Operations environment, no copies of Azure SQL database may be kept running.</span></span> <span data-ttu-id="fd5f7-117">したがって、CREATE DATABASE AS COPY OF ステートメントの使用は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-117">Therefore, use of the CREATE DATABASE AS COPY OF statement is disallowed.</span></span> <span data-ttu-id="fd5f7-118">7 日以上前の Azure SQL データベースのサポートされていないコピーは警告なしに削除されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-118">Any unsupported copies of Azure SQL databases older than 7 days will be deleted without warning.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd5f7-119">前提条件</span><span class="sxs-lookup"><span data-stu-id="fd5f7-119">Prerequisites</span></span>
<span data-ttu-id="fd5f7-120">サンドボックス環境からデータベースをエクスポートするには、その環境で Application Object Server (AOS) を実行しているコンピュータに、最新バージョンの Microsoft SQL Server Management Studio for Microsoft SQL Server 2016 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-120">To export a database from a sandbox environment, you must install the latest version of Microsoft SQL Server Management Studio for Microsoft SQL Server 2016 on the computer that runs Application Object Server (AOS) in that environment.</span></span> <span data-ttu-id="fd5f7-121">その後、AOS コンピューターで、エクスポートを実行してください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-121">You must then do the export on that AOS computer.</span></span> <span data-ttu-id="fd5f7-122">この要件は 2 つの理由があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-122">There are two reasons for this requirement:</span></span>

- <span data-ttu-id="fd5f7-123">Microsoft SQL Server のサンドボックス インスタンスに対するインターネット プロトコル (IP) アクセス制限のため、その環境内のコンピューターからのみ接続が許可されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-123">Because of an Internet Protocol (IP) access restriction on the sandbox instance of Microsoft SQL Server, connections are allowed only from a computer in that environment.</span></span>
- <span data-ttu-id="fd5f7-124">既定でインストールされる Management Studio のバージョンは、以前のバージョンの SQL Server 用であり、必要なタスクを実行できません。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-124">The version of Management Studio that is installed by default is for a previous version of SQL Server and can't perform the required tasks.</span></span>

## <a name="export-the-finance-and-operations-database"></a><span data-ttu-id="fd5f7-125">Finance and Operations データベースをエキスポート</span><span class="sxs-lookup"><span data-stu-id="fd5f7-125">Export the Finance and Operations database</span></span>

### <a name="stop-services"></a><span data-ttu-id="fd5f7-126">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="fd5f7-126">Stop services</span></span>

<span data-ttu-id="fd5f7-127">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-127">Use Remote Desktop to connect to all the computers in the environment, and stop the following Microsoft Windows services by using services.msc.</span></span> <span data-ttu-id="fd5f7-128">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-128">These services will have open connections to the Finance and Operations database.</span></span>

- <span data-ttu-id="fd5f7-129">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-129">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="fd5f7-130">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="fd5f7-131">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-131">Management Reporter 2012 Process Service (on business intelligence \[BI\] computers only)</span></span>

### <a name="run-sqlpackage-to-export-the-finance-and-operations-database"></a><span data-ttu-id="fd5f7-132">Finance and Operations データベースをエクスポートする sqlpackage を実行する</span><span class="sxs-lookup"><span data-stu-id="fd5f7-132">Run sqlpackage to export the Finance and Operations database</span></span>

<span data-ttu-id="fd5f7-133">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-133">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin

SqlPackage.exe /a:export /ssn:<server>.database.windows.net /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false /sp:<SQL password> /su:<SQL user>
```

<span data-ttu-id="fd5f7-134">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-134">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="fd5f7-135">**ssn(ソース サーバー名)** – エクスポートする Azure SQL データベース サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-135">**ssn (source server name)** – The name of the Azure SQL Database server to export from.</span></span>
- <span data-ttu-id="fd5f7-136">**sdn(ソース データベース名)** – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-136">**sdn (source database name)** – The name of the database to export.</span></span>
- <span data-ttu-id="fd5f7-137">**tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-137">**tf (target file)** – The path and name of the file to export to.</span></span>
- <span data-ttu-id="fd5f7-138">**sp(ソース パスワード)** – ソース SQL Server の SQL パスワード。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-138">**sp (source password)** – The SQL password for the source SQL Server.</span></span>
- <span data-ttu-id="fd5f7-139">**su(ソース ユーザー)** – ソース SQL Server の SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-139">**su (source user)** – The SQL user name for the source SQL Server.</span></span> <span data-ttu-id="fd5f7-140">**sqladmin** ユーザーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-140">We recommend that you use the **sqladmin** user.</span></span> <span data-ttu-id="fd5f7-141">このユーザーは、展開中にすべての SQLインスタンスで作成されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-141">This user is created on every SQL instance during deployment.</span></span> <span data-ttu-id="fd5f7-142">このユーザーのパスワードは、Microsoft Dynamics Lifecycle Services (LCS) 内のプロジェクトから取得することができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-142">You can retrieve the password for this user from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fd5f7-143">このコマンドは、D:\\Exportedbacpac フォルダに .bacpac ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-143">The command creates a .bacpac file in the D:\\Exportedbacpac folder.</span></span> <span data-ttu-id="fd5f7-144">このファイルを安全な場所にコピーまたはアップロードすることにより、後で別の環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-144">By copying or uploading this file to secure location, you can import it into another environment later.</span></span> <span data-ttu-id="fd5f7-145">AzCopy コマンドライン ユーティリティを使用すると、Azure ストレージ アカウントにファイルをアップロードして、対象となる AOS コンピューターにダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-145">You can use the AzCopy command-line utility to upload the file to an Azure storage account and then download it to the target AOS computer.</span></span> <span data-ttu-id="fd5f7-146">詳細については、[Azure ストレージ アカウントへのファイルのコピーまたはアップロード](/azure/storage/storage-use-azcopy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-146">For more information, see [Copy or upload the file to an Azure storage account](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="fd5f7-147">Microsoft は、Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-147">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="fd5f7-148">ストレージ アカウントを購入するか、別の Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-148">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd5f7-149">Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-149">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="fd5f7-150">このドライブにエクスポートされたデータベース ファイルを完全には保存しないでください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-150">Don't permanently store your exported database files on this drive.</span></span> <span data-ttu-id="fd5f7-151">それ以外の場合、それらが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-151">Otherwise, you might lose them.</span></span> <span data-ttu-id="fd5f7-152">詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-152">For more information, see the [Understanding the temporary drive on Windows Azure virtual machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) blog post.</span></span>

### <a name="start-services"></a><span data-ttu-id="fd5f7-153">サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-153">Start services</span></span>

<span data-ttu-id="fd5f7-154">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-154">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="fd5f7-155">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-155">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="fd5f7-156">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-156">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="fd5f7-157">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-157">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-the-finance-and-operations-database"></a><span data-ttu-id="fd5f7-158">Finance and Operations データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="fd5f7-158">Import the Finance and Operations database</span></span>

### <a name="stop-services"></a><span data-ttu-id="fd5f7-159">サービスの停止</span><span class="sxs-lookup"><span data-stu-id="fd5f7-159">Stop services</span></span>

<span data-ttu-id="fd5f7-160">リモート デスクトップを使用して、環境内のすべてのコンピュータに接続し、services.msc を使用して次の Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-160">Use Remote Desktop to connect to all the computers in the environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="fd5f7-161">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-161">These services will have open connections to the Finance and Operations database.</span></span>

- <span data-ttu-id="fd5f7-162">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-162">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="fd5f7-163">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-163">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="fd5f7-164">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-164">Management Reporter 2012 Process Service (on BI computers only)</span></span>

### <a name="import-the-bacpac-file"></a><span data-ttu-id="fd5f7-165">.bacpac ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="fd5f7-165">Import the .bacpac file</span></span>

<span data-ttu-id="fd5f7-166">エクスポート ステップ中に生成された .bacpac ファイルをターゲット環境の AOS コンピュータにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-166">Copy the .bacpac file that was generated during the export step to the AOS computer in the target environment.</span></span> <span data-ttu-id="fd5f7-167">パフォーマンス上の理由から、.bacpac ファイルを AOS コンピューターの D ドライブに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-167">For performance reasons, we recommend that you put the .bacpac file on drive D on the AOS computer.</span></span>

<span data-ttu-id="fd5f7-168">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-168">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<Azure DSQL database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<new database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=<See below>
```

<span data-ttu-id="fd5f7-169">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-169">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="fd5f7-170">**tsn(ターゲット サーバー名)** – インポートする Azure SQL データベース サーバーの名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-170">**tsn (target server name)** – The name of the Azure SQL Database server to import into.</span></span> <span data-ttu-id="fd5f7-171">名前はデータベース アカウントの環境ページの LCS で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-171">You can find the name in LCS on the environment page under Database Accounts.</span></span> <span data-ttu-id="fd5f7-172">接尾語 **database.windows.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-172">Add the suffix **database.windows.net** to it.</span></span>
- <span data-ttu-id="fd5f7-173">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-173">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="fd5f7-174">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-174">The database should **not** already exist.</span></span> <span data-ttu-id="fd5f7-175">インポート処理が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-175">The import process will create it.</span></span>
- <span data-ttu-id="fd5f7-176">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-176">**sf (source file)** – The path and name of the file to import from.</span></span>
- <span data-ttu-id="fd5f7-177">**tu(ターゲット ユーザー)** – ターゲットの Azure SQL データベース インスタンスの SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-177">**tu (target user)** – The SQL user name for the target Azure SQL database instance.</span></span> <span data-ttu-id="fd5f7-178">標準の **sqladmin** ユーザーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-178">We recommend that you use the standard **sqladmin** user.</span></span> <span data-ttu-id="fd5f7-179">LCS プロジェクトからは、このユーザーのパスワードを取得できます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-179">You can retrieve the password for this user from your LCS project.</span></span>
- <span data-ttu-id="fd5f7-180">**tp(ターゲット パスワード)** – ターゲットの Azure SQL データベース ユーザーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-180">**tp (target password)** – The password for the target Azure SQL database user.</span></span>
- <span data-ttu-id="fd5f7-181">**DatabaseServiceObjective** – S1、P2、P4 などのデータベースのパフォーマンス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-181">**DatabaseServiceObjective** – Specifies the performance level of the database such as S1, P2 or P4.</span></span> <span data-ttu-id="fd5f7-182">パフォーマンス要件を満たし、サービス契約を遵守するには、現在の Finance and Operations データベース (AXDB) と同じサービス目標レベルをこの環境で使用します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-182">To meet performance requirements and comply with your service agreement, use the same service objective level as the current Finance and Operations database (AXDB) on this environment.</span></span> <span data-ttu-id="fd5f7-183">現在のデータベースのサービス レベル目標を照会するには、次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-183">To query the service level objective of the current database, run the following query.</span></span>

    ```
    SELECT  d.name,   
        slo.*    
    FROM sys.databases d   
    JOIN sys.database_service_objectives slo    
    ON d.database_id = slo.database_id;  
    ```

### <a name="run-a-script-to-update-the-finance-and-operations-database"></a><span data-ttu-id="fd5f7-184">Finance and Operations データベースを更新するスクリプトを実行する</span><span class="sxs-lookup"><span data-stu-id="fd5f7-184">Run a script to update the Finance and Operations database</span></span>

<span data-ttu-id="fd5f7-185">ソースとターゲット環境の SQL ユーザーのパスワードが異なる場合は、次のスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-185">If the source and target environments have different SQL user passwords, you must run the following script.</span></span> <span data-ttu-id="fd5f7-186">パスワードとは異なるかどうかが不明な場合は、このスクリプトを実行することも必要です。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-186">You must also run this script if you aren't sure whether the passwords differ.</span></span> <span data-ttu-id="fd5f7-187">インポートされたデータベースに対して、スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-187">Run the script against the imported database.</span></span> <span data-ttu-id="fd5f7-188">スクリプトは、データベース ユーザーを削除してから、ターゲット環境の正しいパスワードを持つように再作成します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-188">The script drops the database users and then re-creates them so that they have the correct passwords for the target environment.</span></span>

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
## <a name="synchronize-the-database"></a><span data-ttu-id="fd5f7-189">データベースの同期</span><span class="sxs-lookup"><span data-stu-id="fd5f7-189">Synchronize the database</span></span>

1. <span data-ttu-id="fd5f7-190">リモート デスクトップを使用して、ターゲット環境内のすべてのコンピュータに接続し、services.msc を使用して次の Microsoft Windows サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-190">Use Remote Desktop to connect to all the computers in the target environment, and stop the following Windows services by using services.msc.</span></span> <span data-ttu-id="fd5f7-191">これらのサービスでは、Finance and Operations のデータベースへの接続が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-191">These services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="fd5f7-192">サービスを停止した後に、既存の Finance and Operations データベースを新しくインポートされたデータベースに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-192">After you stop the services, you can replace the existing Finance and Operations database with the newly imported database.</span></span>

    - <span data-ttu-id="fd5f7-193">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-193">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="fd5f7-194">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-194">Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="fd5f7-195">Management Reporter 2012 のプロセス サービス (ビジネス インテリジェンス \[BI\] コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-195">Management Reporter 2012 Process service (on business intelligence \[BI\] computers only)</span></span>

2. <span data-ttu-id="fd5f7-196">bacpac インポートが実行された AOS コンピューターで、Management Studio の次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-196">On the AOS computer where the bacpac import was performed, run the following script in Management Studio.</span></span> <span data-ttu-id="fd5f7-197">このスクリプトは、元のデータベースの名前を変更し、新しくインポートされたデータベースの名前を変更して元のデータベース名を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-197">This script renames the original database and then renames the newly imported database so that it uses the original database name.</span></span> <span data-ttu-id="fd5f7-198">この例では、元のデータベースは axdb\_123456789 という名前が付けられ、新しくインポートされたデータベースは importeddb という名前が付けられました。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-198">In this example, the original database was named axdb\_123456789, and the newly imported database was named importeddb.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd5f7-199">Management Studio の SQL Server 2016 バージョンを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-199">Make sure that you're using the SQL Server 2016 version of Management Studio.</span></span>

    ```
    ALTER DATABASE [axdb_123456789] MODIFY NAME = [axdb_123456789_original]
    ALTER DATABASE [importeddb] MODIFY NAME = [axdb_123456789]
    ```

3. <span data-ttu-id="fd5f7-200">データベースを同期させます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-200">Synchronize the database.</span></span> <span data-ttu-id="fd5f7-201">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-201">Open a **Command Prompt** window as an administrator, and run the following commands.</span></span>

    ```
    cd F:\AosService\WebRoot\bin

    Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "F:\AosService\PackagesLocalDirectory" -metadatadir F:\AosService\PackagesLocalDirectory -sqluser axdbadmin -sqlserver <Azure SQL database server name>.database.windows.net -sqldatabase <database name> -setupmode sync -syncmode fullall -isazuresql true -sqlpwd <SQL password> >log.txt 2>&1
    ```

4. <span data-ttu-id="fd5f7-202">services.msc を使用して、以前に停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-202">Use services.msc to restart the services that you stopped earlier:</span></span>

    - <span data-ttu-id="fd5f7-203">ワールド ワイド ウェブ公開サービス (すべての AOS コンピュータ上)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-203">World wide web publishing service (on all AOS computers)</span></span>
    - <span data-ttu-id="fd5f7-204">Microsoft Dynamics 365 for Finance and Operations バッチ管理サービス (非プライベート AOS コンピュータ上のみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-204">Microsoft Dynamics 365 for Finance and Operations Batch Management service (on non-private AOS computers only)</span></span>
    - <span data-ttu-id="fd5f7-205">Management Reporter 2012 のプロセス サービス (BI コンピューターのみ)</span><span class="sxs-lookup"><span data-stu-id="fd5f7-205">Management Reporter 2012 Process service (on BI computers only)</span></span>

5. <span data-ttu-id="fd5f7-206">この時点で、Finance and Operations アプリケーション URL を開いてサイン インすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-206">At this point, you can open the Finance and Operations application URL and sign in.</span></span> <span data-ttu-id="fd5f7-207">アプリケーションが予期したとおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-207">Verify that the application works as you expect.</span></span> <span data-ttu-id="fd5f7-208">次に、bacpac のインポートを実行した AOS コンピューターの Management Studio で以下のスクリプトを実行して、元のデータベースを削除します。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-208">Then drop the original database by running the following script in Management Studio on the AOS computer where you performed the bacpac import.</span></span>

    ```
    DROP DATABASE [axdb_123456789_original]
    ```


### <a name="re-provision-retail-components-in-the-target-environment"></a><span data-ttu-id="fd5f7-209">対象となる環境で Retail コンポーネントを再プロビジョニング</span><span class="sxs-lookup"><span data-stu-id="fd5f7-209">Re-provision Retail components in the target environment</span></span>

<span data-ttu-id="fd5f7-210">データベースを別の環境で復元またはインポートする場合のみ再プロビジョニングが必要です。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-210">Reprovisioning is only required if you are restoring or importing the database on another environment.</span></span>

[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="limitations"></a><span data-ttu-id="fd5f7-211">制限</span><span class="sxs-lookup"><span data-stu-id="fd5f7-211">Limitations</span></span>
<span data-ttu-id="fd5f7-212">データベースをインポートすると、Azure Blob Storage に保管されているデータベースおよびドキュメント処理のドキュメント間のリンクが破損している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-212">After you import a database, the link between the database and document handling documents that are stored in Azure blob storage might be broken.</span></span> <span data-ttu-id="fd5f7-213">X++ **FileUpload** クラスを使用して BLOB ストレージにファイルを格納するカスタム コードがある場合、それらのファイルへのリンクも壊れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f7-213">If you have custom code that uses the X++ **FileUpload** class to put files in blob storage, the links to those files might also be broken.</span></span>

