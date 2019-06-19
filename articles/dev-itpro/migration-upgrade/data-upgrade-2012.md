---
title: AX 2012 からのアップグレード - 開発環境でのデータ アップグレード
description: このトピックでは、開発環境で Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations にアップグレードする詳細なプロセスを説明します。
author: tariqbell
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 52d87e047634e18585d0b5eb955b7f2a64bdff94
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595477"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-development-environments"></a><span data-ttu-id="8aee8-103">AX 2012 からのアップグレード - 開発環境でのデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="8aee8-103">Upgrade from AX 2012 - Data upgrade in development environments</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="8aee8-104">これは、アップグレード プロジェクトのエキサイティングな瞬間です。</span><span class="sxs-lookup"><span data-stu-id="8aee8-104">This is an exciting moment in the upgrade project.</span></span> <span data-ttu-id="8aee8-105">このタスクの出力は、Microsoft Dynamics 365 for Finance and Operations で、Microsoft Dynamics AX 2012 からアップグレードされた最初のデータセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-105">The output of this task  provides the first upgraded dataset from Microsoft Dynamics AX 2012 in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="8aee8-106">このプロセスを共有サンドボックス環境で実行する前に、開発環境で実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8aee8-106">Before you run this process in a shared sandbox environment, we recommend that you run it in a development environment.</span></span> <span data-ttu-id="8aee8-107">このアプローチには主に 2 つの理由があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-107">There are two main reasons for this approach:</span></span>

- <span data-ttu-id="8aee8-108">開発者がカスタム データ アップグレード スクリプトを書き込んでテストできるローカル データを提供します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-108">It provides local data that developers can write and test their custom data upgrade scripts against.</span></span>
- <span data-ttu-id="8aee8-109">これは、データ アップグレード プロセスの繰り返しに費やされる全体的な時間を短縮できます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-109">It helps reduce the overall time that is spent on iterations of the data upgrade process.</span></span> <span data-ttu-id="8aee8-110">開発環境では、問題を即座にデバッグし、コードを調整し、アップグレードを数分以内に再実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-110">In a development environment, an issue can be debugged immediately, code can be adjusted, and the upgrade can be rerun within minutes.</span></span> <span data-ttu-id="8aee8-111">ただし、より規模の大きいサンドボックス環境ではこの機敏性のレベルが許可されていません。</span><span class="sxs-lookup"><span data-stu-id="8aee8-111">However, larger sandbox environments don’t allow for this level of agility.</span></span> <span data-ttu-id="8aee8-112">それらの環境では、問題の修正やデバッグ、コードの更新、更新済コードの配置、およびアップグレードの再実行に少なくとも数時間を要します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-112">In those environments, a minimum of several hours will be required to debug and remediate issues, update code, deploy the updated code, and rerun the upgrade.</span></span>

<span data-ttu-id="8aee8-113">データのアップグレードを実行する前に、[アップグレード アナライザー](upgrade-analyzer-tool.md)を実行して、特定した問題に対応することを強くお勧めします。これは、データのアップグレードが迅速かつ容易になることを保証する手助けになります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-113">We strongly recommend that you run the [Upgrade analyzer](upgrade-analyzer-tool.md) and respond to the issues it identifies before running data upgrade - this will help ensure that your data upgrade is quicker and easier.</span></span>

> [!NOTE]
> <span data-ttu-id="8aee8-114">このプロセスを開始する前に、SQL Server Management Studio の最新バージョンをインストールすることが非常に重要です。[SQL Server Management Studio のダウンロード](/sql/ssms/download-sql-server-management-studio-ssms).</span><span class="sxs-lookup"><span data-stu-id="8aee8-114">It's very important that you install the latest version of SQL Server Management Studio before you start this process: [Download SQL Server Management Studio](/sql/ssms/download-sql-server-management-studio-ssms).</span></span> 

## <a name="end-to-end-data-upgrade-process"></a><span data-ttu-id="8aee8-115">エンド ツー エンド データのアップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="8aee8-115">End-to-end data upgrade process</span></span>

![データ アップグレード プロセス](media/endToEndDataUpgradeProcess.png)

### <a name="back-up-your-ax-2012-database"></a><span data-ttu-id="8aee8-117">AX 2012 データベースをバックアップします</span><span class="sxs-lookup"><span data-stu-id="8aee8-117">Back up your AX 2012 database</span></span>

<span data-ttu-id="8aee8-118">AX 2012 データベースをバックアップするには、標準の Microsoft SQL Server プロセスを使用して BAK ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-118">To back up your AX 2012 database, use the standard Microsoft SQL Server process to produce a BAK file.</span></span> <span data-ttu-id="8aee8-119">バックアップを作成するときに圧縮オプションを使用すると、ファイル サイズが小さくなり、Microsoft Azure Storage にアップロードおよびダウンロードするために必要な時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-119">If you use the compression option when you create the backup, the file size will be smaller, and less time is required in order upload it to and download it from Microsoft Azure Storage.</span></span>

### <a name="upload-the-backup-to-azure-storage"></a><span data-ttu-id="8aee8-120">Azure ストレージにバックアップをアップロード</span><span class="sxs-lookup"><span data-stu-id="8aee8-120">Upload the backup to Azure Storage</span></span>

<span data-ttu-id="8aee8-121">開発環境がローカルまたは Azure で VM としてホストされている場合、2012 データベースのバックアップをそれに転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-121">If your developer environment is hosted as a VM locally or in Azure you will need to transfer the 2012 database backup to it.</span></span> <span data-ttu-id="8aee8-122">ローカル VM では、ネットワーク全体でファイルを直接転送することができますが (それを許可するように仮想ネットワークを構成済みの場合)、Azure でホストされた VM の場合バックアップを Azure Storage にアップロードすることをお勧めします (自分のセキュアな転送サービスまたは SFTP の使用も有効なオプションです)。</span><span class="sxs-lookup"><span data-stu-id="8aee8-122">With a local VM you may be able to transfer the file directly across the network (if you have configured the virtual network to allow that) but for an Azure hosted VM we recommend that you upload your backup to Azure Storage (using your own secure file transfer service or SFTP is also a valid option).</span></span> <span data-ttu-id="8aee8-123">これに対して、独自の Azure ストレージ アカウントを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-123">You would need to provide your own Azure storage account for this.</span></span> <span data-ttu-id="8aee8-124">Azure ストレージ間でファイルを移動するのに役立つ無料のツールがあります。コマンド ラインからは [Azcopy](/azure/storage/storage-use-azcopy) を、GUI 操作からは [Microsoft Azure ストレージ エクスプローラー](https://storageexplorer.com/) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-124">There are free tools to help you to move files between Azure storage, from a command line you can use [Azcopy](/azure/storage/storage-use-azcopy), or for a GUI experience you can use [Microsoft Azure storage explorer](https://storageexplorer.com/).</span></span> <span data-ttu-id="8aee8-125">これらのツールのいずれかを使用して、オンプレミス環境から Azure ストレージにバックアップをアップロードしてから、開発環境にダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-125">Use one of these tools to first upload the backup from your on-premises environment to Azure storage and then on your download it on your development environment.</span></span>

### <a name="download-and-restore-the-backup-to-the-development-environment"></a><span data-ttu-id="8aee8-126">開発環境へのバックアップのダウンロードと復元</span><span class="sxs-lookup"><span data-stu-id="8aee8-126">Download and restore the backup to the development environment</span></span>

<span data-ttu-id="8aee8-127">Dynamics 365 for Finance and Operations の開発環境にバックアップを復元するときは、既存の AXDB データベースを上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-127">When you restore the backup to your Dynamics 365 for Finance and Operations development environment, don’t overwrite the existing AXDB database.</span></span> <span data-ttu-id="8aee8-128">代わりに、元のデータベースの横にある AX 2012 データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-128">Instead, restore the AX 2012 database next to the original databases.</span></span> <span data-ttu-id="8aee8-129">パフォーマンスを向上させるために、データおよびログ ファイルの D ドライブの使用も考慮する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-129">You might also consider using drive D for the data and log files, to help improve performance.</span></span> <span data-ttu-id="8aee8-130">ただし、D ドライブを使用することには潜在的な問題点があります。基になる仮想マシン (VM) が Azure で割り当て解除され、次に再割り当てされると、D ドライブが消去されます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-130">However, there is a potential downside to using drive D. If the underlying virtual machine (VM) is deallocated in Azure and then reallocated, drive D will be wiped.</span></span> <span data-ttu-id="8aee8-131">実際、このシナリオが発生ことはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="8aee8-131">In practice, this scenario rarely occurs.</span></span> <span data-ttu-id="8aee8-132">したがって、そのリスクは容認できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-132">Therefore, you might find that the risk is acceptable.</span></span> <span data-ttu-id="8aee8-133">ドライブ D の使用方法の詳細については、[[Windows Azure 仮想マシンでのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-133">To learn more about how to use drive D, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

<span data-ttu-id="8aee8-134">データベースの復元プロセスをスピードアップするには、SQL Server サービスアカウントを **axlocaladmin** に変更します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-134">To speed up the database restore process, you can change the SQL Server service account to **axlocaladmin**.</span></span> <span data-ttu-id="8aee8-135">復元プロセスでは、インスタント ファイルの初期化を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-135">The restore process can then use instant file initialization.</span></span> <span data-ttu-id="8aee8-136">詳細については、[データベース インスタント ファイルの初期化](/sql/relational-databases/databases/database-instant-file-initialization) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-136">For more information, see [Database Instant File Initialization](/sql/relational-databases/databases/database-instant-file-initialization).</span></span>

<span data-ttu-id="8aee8-137">データベースを復元した後、次のサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-137">After the database is restored, stop the following services:</span></span>

- <span data-ttu-id="8aee8-138">World Wide Web 公開サービス</span><span class="sxs-lookup"><span data-stu-id="8aee8-138">World wide web publishing service</span></span>
- <span data-ttu-id="8aee8-139">Dynamics 365 for Finance and Operations バッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="8aee8-139">Dynamics 365 for Finance and Operations Batch Management service</span></span>
- <span data-ttu-id="8aee8-140">Management Reporter 2012 処理サービス</span><span class="sxs-lookup"><span data-stu-id="8aee8-140">Management Reporter 2012 Process service</span></span>

<span data-ttu-id="8aee8-141">次に、元の AXDB データベースを **AXDB_orig** に名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-141">Next, rename the original AXDB database **AXDB_orig**.</span></span> <span data-ttu-id="8aee8-142">このデータベースは、後でコードを開発する際に参照する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-142">This database might be useful as reference later, when you develop code.</span></span>

<span data-ttu-id="8aee8-143">最後に、新しく復元された AX 2012 データベース **AXDB** の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-143">Finally, rename the newly restored AX 2012 database **AXDB**.</span></span>

### <a name="run-the-data-upgrade-deployable-package"></a><span data-ttu-id="8aee8-144">データ アップグレード展開可能なパッケージを実行</span><span class="sxs-lookup"><span data-stu-id="8aee8-144">Run the data upgrade deployable package</span></span> 

<span data-ttu-id="8aee8-145">最新の Finance and Operations 更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード展開可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共用資産ライブラリから最新のバイナリ更新プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8aee8-145">To get the latest data upgrade deployable package for a target environment that is running the latest Finance and Operations update, download the latest binary updates from Microsoft Dynamics Lifecycle Services (LCS) Shared asset library.</span></span>

1. <span data-ttu-id="8aee8-146">[LCS](https://lcs.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8aee8-146">Sign in to [LCS](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="8aee8-147">**共有資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-147">Select the **Shared asset library** tile.</span></span>
3. <span data-ttu-id="8aee8-148">**共有アセット** ライブラリの**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-148">In the **Shared asset** library, under **Select asset type**, select **Software deployable package**.</span></span>
4. <span data-ttu-id="8aee8-149">配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-149">In the list of deployable package files, find the data upgrade package that corresponds to your upgrade.</span></span> <span data-ttu-id="8aee8-150">たとえば、AX 2012 からアップグレードする場合、パッケージ名は AX2012DataUpgrade から始まります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-150">For example, if you're upgrading from AX 2012, the package name starts with AX2012DataUpgrade.</span></span> <span data-ttu-id="8aee8-151">アップグレードするリリースに対応するパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-151">Select the package that corresponds to the release you are upgrading to.</span></span> <span data-ttu-id="8aee8-152">例: AX2012DataUpgrade-July2017。</span><span class="sxs-lookup"><span data-stu-id="8aee8-152">For example: AX2012DataUpgrade-July2017.</span></span>

<span data-ttu-id="8aee8-153">詳細については、[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-153">For more information, see [Upgrade data in development, demo, or sandbox environments](upgrade-data-to-latest-update.md).</span></span> 

## <a name="troubleshooting-data-upgrade-script-errors"></a><span data-ttu-id="8aee8-154">アップグレード スクリプト エラーのトラブルシューティング データ</span><span class="sxs-lookup"><span data-stu-id="8aee8-154">Troubleshooting data upgrade script errors</span></span>

<span data-ttu-id="8aee8-155">最後に停止した場所で、データのアップグレードを再開できるようにするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-155">There are options that you let you resume the data upgrade where it last stopped.</span></span> <span data-ttu-id="8aee8-156">また、データベース内のテーブルに、コール スタック付きでデータ アップグレード スクリプト エラーを記録することができます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-156">You can also record any data upgrade script errors with call stacks to a table in the database.</span></span> <span data-ttu-id="8aee8-157">開発のシナリオでは、失敗したスクリプトをスキップし、継続してアップグレードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-157">For development scenarios, you can skip failed scripts and continue to run the upgrade.</span></span>

<span data-ttu-id="8aee8-158">詳細については、[主要データのアップグレード トピック](upgrade-data-to-latest-update.md#troubleshoot-upgrade-script-errors) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8aee8-158">For more details, see the [main data upgrade topic](upgrade-data-to-latest-update.md#troubleshoot-upgrade-script-errors).</span></span>

### <a name="recommendation-for-the-first-data-upgrade-run"></a><span data-ttu-id="8aee8-159">最初のデータ アップグレードを実行するための推奨事項</span><span class="sxs-lookup"><span data-stu-id="8aee8-159">Recommendation for the first data upgrade run</span></span>

<span data-ttu-id="8aee8-160">初めてデータセットのデータのアップグレードを実行するとき、特に多くのカスタマイズまたは多くのカスタム データのアップグレード スクリプトが存在するとき、[失敗したスクリプトをスキップする機能](upgrade-data-to-latest-update.md) が役に立つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-160">When you run the data upgrade against your dataset for the first time, and especially when there many customizations or many custom data upgrade scripts, you might find the [feature to skip failed scripts](upgrade-data-to-latest-update.md) useful.</span></span> <span data-ttu-id="8aee8-161">この機能を使用すると、1 回の実行で可能な限り多くのエラーを可視化できます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-161">By using this feature, you gain visibility into as many errors as possible in one run.</span></span> <span data-ttu-id="8aee8-162">それ以外の場合、実行あたり 1 つだけの重要な問題が検出されます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-162">Otherwise, only one critical issue is discovered per run.</span></span> <span data-ttu-id="8aee8-163">スクリプト間には依存関係が存在するため、親スクリプトをスキップすると関連する子スクリプトにエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="8aee8-163">Be aware that, because dependencies exist between scripts, you might receive errors in related child scripts if you skip the parent script.</span></span> <span data-ttu-id="8aee8-164">これらのエラーは、親が正しく実行されなかったためにのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="8aee8-164">These errors occur only because the parent wasn’t run correctly.</span></span> <span data-ttu-id="8aee8-165">親スクリプト内の問題が解決されると、解決されます。</span><span class="sxs-lookup"><span data-stu-id="8aee8-165">They will be resolved when the issue in the parent script is resolved.</span></span>
