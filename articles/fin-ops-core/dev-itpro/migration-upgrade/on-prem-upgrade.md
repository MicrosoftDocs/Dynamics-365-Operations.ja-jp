---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: f295dfcbdf36aa1a363c7db1aae5e3baf89c9e2c
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117404"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="c8c03-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="c8c03-103">In-place upgrade process for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c8c03-104">実稼働環境のアップグレードを実行する前に、サンドボックス環境のアップグレードを実行してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-104">Please perform the upgrade with your sandbox environment before upgrading your production environment.</span></span>

<span data-ttu-id="c8c03-105">このトピックでは、Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-105">This topic provides the detailed process for upgrading on-premises environments of Finance and Operations from version 7.x to 8.1.</span></span>  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-8-20-to-81"></a><span data-ttu-id="c8c03-106">7.x (プラットフォーム更新プログラム 8 ~ 20) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="c8c03-106">On-premises upgrade from version 7.x (with Platform update 8-20) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="c8c03-107">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-107">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="c8c03-108">7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-108">To upgrade from version 7.x to 8.1, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="c8c03-109">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="c8c03-109">An overview of each path is given below:</span></span>

-   <span data-ttu-id="c8c03-110">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-110">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="c8c03-111">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-111">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="c8c03-112">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-112">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="c8c03-113">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-113">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c03-114">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c8c03-114">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c8c03-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="c8c03-115">Prerequisites</span></span>

1.  <span data-ttu-id="c8c03-116">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-116">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="c8c03-117">**資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-117">Under **Select asset type**, choose **Downloadable VHD**, and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="c8c03-118">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-118">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="c8c03-119">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-119">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="c8c03-120">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-120">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="c8c03-121">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-121">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="c8c03-122">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="c8c03-122">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="c8c03-123">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-123">Connect to the VM.</span></span> <span data-ttu-id="c8c03-124">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-124">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="c8c03-125">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-125">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="c8c03-126">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-126">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="c8c03-127">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="c8c03-127">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="c8c03-128">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-128">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="c8c03-129">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-129">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="c8c03-130">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-130">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="c8c03-131">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-131">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="c8c03-132">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-132">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="c8c03-133">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="c8c03-133">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="c8c03-134">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-134">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="c8c03-135">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-135">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="c8c03-136">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-136">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="c8c03-137">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-137">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > <span data-ttu-id="c8c03-138">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-138">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="c8c03-139">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-139">If you would like to edit more values, refer to  Appendix A.</span></span>

    <span data-ttu-id="c8c03-140">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-140">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="c8c03-141">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-141">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="c8c03-142">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-142">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="c8c03-143">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-143">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="c8c03-144">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-144">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="c8c03-145">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-145">During the execution of cleanup for data upgrade you may encounter an error:</span></span> 
    
    `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`
    
    <span data-ttu-id="c8c03-146">これを解決するには、次のコマンドのステップを再実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-146">To resolve this, re-run the step with this command:</span></span> 
    
    `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  <span data-ttu-id="c8c03-147">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-147">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="c8c03-148">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-148">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="c8c03-149">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-149">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="c8c03-150">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-150">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="c8c03-151">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-151">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="c8c03-152">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-152">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="c8c03-153">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-153">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="c8c03-154">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-154">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="c8c03-155">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-155">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="c8c03-156">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-156">If you had customizations:</span></span>

    <span data-ttu-id="c8c03-157">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-157">a.</span></span>  <span data-ttu-id="c8c03-158">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-158">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="c8c03-159">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-159">b.</span></span>  <span data-ttu-id="c8c03-160">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-160">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="c8c03-161">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-161">c.</span></span>  <span data-ttu-id="c8c03-162">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-162">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="c8c03-163">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-163">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="c8c03-164">d.</span><span class="sxs-lookup"><span data-stu-id="c8c03-164">d.</span></span>  <span data-ttu-id="c8c03-165">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-165">The database will need to be configured.</span></span> <span data-ttu-id="c8c03-166">[Finance and Operations データベースのコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-166">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="c8c03-167">e.</span><span class="sxs-lookup"><span data-stu-id="c8c03-167">e.</span></span>  <span data-ttu-id="c8c03-168">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-168">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="c8c03-169">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-169">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="c8c03-170">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-170">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="c8c03-171">f.</span><span class="sxs-lookup"><span data-stu-id="c8c03-171">f.</span></span>  <span data-ttu-id="c8c03-172">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-172">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="c8c03-173">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-173">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="c8c03-174">g.</span><span class="sxs-lookup"><span data-stu-id="c8c03-174">g.</span></span>  <span data-ttu-id="c8c03-175">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-175">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="c8c03-176">h.</span><span class="sxs-lookup"><span data-stu-id="c8c03-176">h.</span></span>  <span data-ttu-id="c8c03-177">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-177">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="c8c03-178">i.</span><span class="sxs-lookup"><span data-stu-id="c8c03-178">i.</span></span>  <span data-ttu-id="c8c03-179">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-179">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="c8c03-180">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-180">If you didn't have customizations:</span></span>

    <span data-ttu-id="c8c03-181">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-181">a.</span></span>  <span data-ttu-id="c8c03-182">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-182">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="c8c03-183">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-183">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="c8c03-184">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-184">b.</span></span>  <span data-ttu-id="c8c03-185">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-185">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="c8c03-186">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-186">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="c8c03-187">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-187">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="c8c03-188">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="c8c03-188">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="c8c03-189">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-189">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="c8c03-190">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-190">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="c8c03-191">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-191">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="c8c03-192">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-192">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="c8c03-193">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-193">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="c8c03-194">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-194">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="c8c03-195">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-195">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="c8c03-196">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="c8c03-196">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="c8c03-197">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-197">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="c8c03-198">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-198">Open a new PowerShell as Administrator and execute:</span></span>
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="c8c03-199">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-199">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="c8c03-200">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-200">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="c8c03-201">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-201">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="c8c03-202">SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-202">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="c8c03-203">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-203">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="c8c03-204">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-204">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="c8c03-205">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-205">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="c8c03-206">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-206">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="c8c03-207">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-207">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="c8c03-208">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-208">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="c8c03-209">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-209">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="c8c03-210">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-210">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="c8c03-211">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-211">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="c8c03-212">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span><span class="sxs-lookup"><span data-stu-id="c8c03-212">During the execution of Cleanup for data upgrade you may encounter an error: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span></span>

    <span data-ttu-id="c8c03-213">これを解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span><span class="sxs-lookup"><span data-stu-id="c8c03-213">To resolve this, re-run the step with this command: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span></span>

9.  <span data-ttu-id="c8c03-214">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-214">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="c8c03-215">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-215">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="c8c03-216">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-216">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="c8c03-217">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-217">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="c8c03-218">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-218">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="c8c03-219">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-219">If you had customizations:</span></span>

    <span data-ttu-id="c8c03-220">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-220">a.</span></span>  <span data-ttu-id="c8c03-221">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-221">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="c8c03-222">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-222">b.</span></span>  <span data-ttu-id="c8c03-223">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-223">Under **Select asset type** choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="c8c03-224">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-224">c.</span></span>  <span data-ttu-id="c8c03-225">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-225">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="c8c03-226">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-226">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="c8c03-227">d.</span><span class="sxs-lookup"><span data-stu-id="c8c03-227">d.</span></span>  <span data-ttu-id="c8c03-228">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-228">The database will need to be configured.</span></span> <span data-ttu-id="c8c03-229">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-229">Follow the steps under [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

    <span data-ttu-id="c8c03-230">e.</span><span class="sxs-lookup"><span data-stu-id="c8c03-230">e.</span></span>  <span data-ttu-id="c8c03-231">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-231">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="c8c03-232">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-232">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="c8c03-233">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-233">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="c8c03-234">f.</span><span class="sxs-lookup"><span data-stu-id="c8c03-234">f.</span></span>  <span data-ttu-id="c8c03-235">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-235">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="c8c03-236">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-236">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="c8c03-237">g.</span><span class="sxs-lookup"><span data-stu-id="c8c03-237">g.</span></span>  <span data-ttu-id="c8c03-238">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-238">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="c8c03-239">h.</span><span class="sxs-lookup"><span data-stu-id="c8c03-239">h.</span></span>  <span data-ttu-id="c8c03-240">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-240">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="c8c03-241">i.</span><span class="sxs-lookup"><span data-stu-id="c8c03-241">i.</span></span>  <span data-ttu-id="c8c03-242">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-242">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="c8c03-243">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-243">If you didn't have customizations:</span></span>

    <span data-ttu-id="c8c03-244">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-244">a.</span></span>  <span data-ttu-id="c8c03-245">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-245">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="c8c03-246">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-246">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="c8c03-247">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-247">b.</span></span>  <span data-ttu-id="c8c03-248">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-248">Setup a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="c8c03-249">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-249">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="c8c03-250">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-250">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a><span data-ttu-id="c8c03-251">7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="c8c03-251">On-premises upgrade from version 7.x (with Platform update 21 or later) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="c8c03-252">このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-252">Be aware that this upgrade process takes time complete and Finance and Operations will be inaccessible for the entire duration.</span></span>

<span data-ttu-id="c8c03-253">オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-253">To upgrade from on-premises 7.x to on-premises 8.1 there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="c8c03-254">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="c8c03-254">An overview of each path is given below:</span></span>

-   <span data-ttu-id="c8c03-255">**VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-255">**Upgrading from within VHD** - This path involves copying your database into the VHD and executing the upgrade inside it.</span></span> <span data-ttu-id="c8c03-256">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-256">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="c8c03-257">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-257">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="c8c03-258">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-258">The upgrade process is still executed from within the VHD.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c8c03-259">VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c8c03-259">The VHD does not need external network access in order to carry out the data upgrade process.</span></span>


### <a name="prerequisites"></a><span data-ttu-id="c8c03-260">必要条件</span><span class="sxs-lookup"><span data-stu-id="c8c03-260">Prerequisites</span></span>

1.  <span data-ttu-id="c8c03-261">LCS では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-261">In LCS, go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="c8c03-262">**資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-262">Under **Select asset type**, choose downloadable VHD and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="c8c03-263">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-263">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="c8c03-264">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-264">The files you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="c8c03-265">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-265">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="c8c03-266">Hyper-V を使用して、VM を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-266">Using Hyper-V launch a VM and attach the VHD.</span></span> <span data-ttu-id="c8c03-267">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="c8c03-267">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="c8c03-268">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-268">Connect to the VM.</span></span> <span data-ttu-id="c8c03-269">資格情報についてはこちらをご覧ください。https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span><span class="sxs-lookup"><span data-stu-id="c8c03-269">You can find the credentials here: https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span></span>

6.  <span data-ttu-id="c8c03-270">続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-270">Before proceeding it will be necessary to upgrade the platform version of the VHD so that it is in the same state as the one in your environment.</span></span> <span data-ttu-id="c8c03-271">基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-271">You basically want the version number of the platform in the VHD to match exactly to the version number in your environment.</span></span> <span data-ttu-id="c8c03-272">これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-272">In order to do this you can check your environments history in LCS to see which packages have been applied from your asset library.</span></span> <span data-ttu-id="c8c03-273">VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-273">Keep in mind that the VHD is already in Platform update 20 (7.0.5030.35333) so it will probably already contain some packages that you installed manually into your environment, but may not include the latest binary updates that you applied to your environment.</span></span>

7.  <span data-ttu-id="c8c03-274">パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-274">After you have located the package or packages that have to be applied, download them into the VHD from LCS.</span></span>

8.  <span data-ttu-id="c8c03-275">各パッケージについては、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-275">For each package do the following:</span></span>

    <span data-ttu-id="c8c03-276">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-276">a.</span></span>  <span data-ttu-id="c8c03-277">c:\\D365FFOUpgrade\\ などのパッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-277">Extract the package, such as c:\\D365FFOUpgrade\\</span></span>

    <span data-ttu-id="c8c03-278">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-278">b.</span></span>  <span data-ttu-id="c8c03-279">管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-279">Open a Command Prompt as Administrator and change directory to the unzipped folder.</span></span>

    <span data-ttu-id="c8c03-280">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-280">c.</span></span>  <span data-ttu-id="c8c03-281">実行</span><span class="sxs-lookup"><span data-stu-id="c8c03-281">Execute</span></span>

       1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

       2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

       3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

9.  <span data-ttu-id="c8c03-282">アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-282">If you have any application extensions or customizations install them now into the VHD, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="c8c03-283">アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-283">Check with your ISV or VAR if you need to prepare your environment in any way before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="c8c03-284">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="c8c03-284">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="c8c03-285">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-285">Shut down On-Premises AOSs, BI and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="c8c03-286">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-286">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="c8c03-287">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-287">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="c8c03-288">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-288">In the VHD go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="c8c03-289">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-289">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="c8c03-290">例 c:\\D365FFOUpgrade</span><span class="sxs-lookup"><span data-stu-id="c8c03-290">Eg c:\\D365FFOUpgrade</span></span>\\

5.  <span data-ttu-id="c8c03-291">管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-291">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 4.</span></span>

6.  <span data-ttu-id="c8c03-292">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-292">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="c8c03-293">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-293">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="c8c03-294">(オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-294">(Optional) If the name of your restored database is not AXDB, using PowerShell with Administrator privileges execute:</span></span>
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > <span data-ttu-id="c8c03-295">(通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-295">Substitute \<DB-Name\> with the appropriate value in your case (typically AXDB).</span></span> <span data-ttu-id="c8c03-296">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-296">If you would like to edit more values, refer to Appendix A.</span></span>

    <span data-ttu-id="c8c03-297">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-297">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="c8c03-298">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-298">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="c8c03-299">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-299">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="c8c03-300">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-300">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="c8c03-301">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-301">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="c8c03-302">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span><span class="sxs-lookup"><span data-stu-id="c8c03-302">During the execution of Cleanup for data upgrade you may encounter an error: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span></span>

    <span data-ttu-id="c8c03-303">これを解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span><span class="sxs-lookup"><span data-stu-id="c8c03-303">To resolve this, re-run the step with this command: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span></span>

9.  <span data-ttu-id="c8c03-304">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-304">Once the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="c8c03-305">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-305">If you have customizations from ISVs or VARs check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="c8c03-306">実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-306">Restore the database into your environment with a different name from the production one (typically AXDBupgraded).</span></span>

11. <span data-ttu-id="c8c03-307">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-307">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="c8c03-308">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-308">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="c8c03-309">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-309">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="c8c03-310">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-310">This process may take longer depending on the number of nodes that you have.</span></span>

13. <span data-ttu-id="c8c03-311">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-311">In LCS, go to the Shared Assets Library.</span></span>

14. <span data-ttu-id="c8c03-312">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-312">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

15. <span data-ttu-id="c8c03-313">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-313">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="c8c03-314">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-314">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

16. <span data-ttu-id="c8c03-315">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-315">The database will need to be configured.</span></span> <span data-ttu-id="c8c03-316">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-316">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

17. <span data-ttu-id="c8c03-317">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-317">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="c8c03-318">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-318">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="c8c03-319">配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-319">When you deploy, the database that you should specify should be the one created in step 15 (typically AXDB).</span></span>

18. <span data-ttu-id="c8c03-320">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-320">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="c8c03-321">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-321">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

19. <span data-ttu-id="c8c03-322">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-322">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

20. <span data-ttu-id="c8c03-323">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-323">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

21. <span data-ttu-id="c8c03-324">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-324">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

22. <span data-ttu-id="c8c03-325">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-325">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="c8c03-326">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="c8c03-326">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="c8c03-327">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-327">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="c8c03-328">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-328">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="c8c03-329">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-329">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="c8c03-330">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-330">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="c8c03-331">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-331">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="c8c03-332">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-332">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="c8c03-333">C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-333">Paste the file wherever you want and unzip it, such as C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="c8c03-334">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-334">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="c8c03-335">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-335">Open a new PowerShell as Administrator and execute:</span></span>

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="c8c03-336">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-336">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="c8c03-337">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-337">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="c8c03-338">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-338">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="c8c03-339">SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-339">You will need to add the Certificate Authority certificate that signed your SQL server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="c8c03-340">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-340">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span> 
    >
    > - <span data-ttu-id="c8c03-341">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-341">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database that you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="c8c03-342">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-342">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="c8c03-343">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-343">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="c8c03-344">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-344">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="c8c03-345">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-345">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="c8c03-346">a.</span><span class="sxs-lookup"><span data-stu-id="c8c03-346">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="c8c03-347">b.</span><span class="sxs-lookup"><span data-stu-id="c8c03-347">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="c8c03-348">c.</span><span class="sxs-lookup"><span data-stu-id="c8c03-348">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="c8c03-349">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span><span class="sxs-lookup"><span data-stu-id="c8c03-349">During the execution of Cleanup for data upgrade you may encounter an error: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span></span>

    <span data-ttu-id="c8c03-350">この問題を解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span><span class="sxs-lookup"><span data-stu-id="c8c03-350">To resolve this issue, re-run the step with this command: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span></span>

9.  <span data-ttu-id="c8c03-351">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-351">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="c8c03-352">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-352">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="c8c03-353">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-353">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="c8c03-354">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-354">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="c8c03-355">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-355">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="c8c03-356">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-356">In LCS, go to the Shared Assets Library.</span></span>

13. <span data-ttu-id="c8c03-357">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-357">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

14. <span data-ttu-id="c8c03-358">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-358">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="c8c03-359">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-359">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

15. <span data-ttu-id="c8c03-360">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-360">The database will need to be configured.</span></span> <span data-ttu-id="c8c03-361">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c8c03-361">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

16. <span data-ttu-id="c8c03-362">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-362">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="c8c03-363">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8c03-363">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="c8c03-364">配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-364">When you deploy, the database that you should specify should be the one created in step 14 (typically AXDB).</span></span>

17. <span data-ttu-id="c8c03-365">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-365">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="c8c03-366">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="c8c03-366">Otherwise when the environment initially synchs  with the database it will delete any customization or extensions related data.</span></span>

18. <span data-ttu-id="c8c03-367">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-367">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

19. <span data-ttu-id="c8c03-368">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-368">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

20. <span data-ttu-id="c8c03-369">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-369">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

21. <span data-ttu-id="c8c03-370">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-370">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a><span data-ttu-id="c8c03-371">付録 A</span><span class="sxs-lookup"><span data-stu-id="c8c03-371">Appendix A</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="c8c03-372">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="c8c03-372">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="c8c03-373">このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="c8c03-373">This script is only meant to be run from a Onebox VHD environment.</span></span>
>
> <span data-ttu-id="c8c03-374">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="c8c03-374">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="c8c03-375">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-375">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="c8c03-376">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-376">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="c8c03-377">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8c03-377">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="c8c03-378">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-378">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="c8c03-379">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="c8c03-379">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="c8c03-380">**-DatabaseServer** - Finance and Operations (オンプレミス) データベースが含まれているデータベース サーバーです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-380">**-DatabaseServer** - Database server containing Finance and Operations (on-premises) database.</span></span>

-   <span data-ttu-id="c8c03-381">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="c8c03-381">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="c8c03-382">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="c8c03-382">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="c8c03-383">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-383">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="c8c03-384">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c8c03-384">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="c8c03-385">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="c8c03-385">**Configure-On-Premises-Upgrade.ps1**</span></span>

```powershell
<#
.Synopsis
   Configures a Onebox deployment to upgrade an OnPrem 7.x database to OnPrem 8.x 

.DESCRIPTION
   This must be executed before the upgrade process is carried out.

.EXAMPLE
   .\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB'

   .\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB' -DatabaseServer '127.0.0.1' -DatabaseUser 'axdbadmin' -DatabasePassword 'secretPass'
#>
[CmdletBinding()]
param
(
    # Database server containing Microsoft Dynamics 365 for Operations, on-premises database.
    [AllowNull()]
    [string] $DatabaseServer,

    # Database name that you want to upgrade.
    [Parameter(Mandatory = $true)]
    [string] $DatabaseName,

    # Username for SQL Authentication.
    [AllowNull()]
    [string] $DatabaseUser,

    # Password for SQL Authentication.
    [AllowNull()]
    [string] $DatabasePassword
)

$webroot = "C:\AOSService\webroot"

$commandParameter = " -decrypt `"$webroot\web.config`""

$command = Resolve-Path "$webroot\bin\Microsoft.Dynamics.AX.Framework.ConfigEncryptor.exe"

Start-Process $command $commandParameter -PassThru -Wait

if([string]::IsNullOrEmpty($DatabaseUser) -and [string]::IsNullOrEmpty($DatabasePassword) -and [string]::IsNullOrEmpty($DatabaseServer)) { 
  
    [xml]$web = Get-Content $webroot\web.config

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value = [string]$DatabaseName
        
}
else { 

    if([string]::IsNullOrEmpty($DatabaseServer)){

        $DatabaseServer = if($value = Read-Host 'What is the IP or FQDN of the Database server? [127.0.0.1]') {$value} else {'127.0.0.1'}

    }

    if([string]::IsNullOrEmpty($DatabaseUser)){

        $DatabaseUser = if($value = Read-Host 'What is the SQL Authentication username? [axdbadmin]') {$value} else {'axdbadmin'}
    
    }

    if([string]::IsNullOrEmpty($DatabasePassword)){
    
        $dbPassEn = if($value = Read-Host 'What is the SQL Authentication password?' -AsSecureString) {$value} else {''}

        $BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($dbPassEn) 
    
        $DatabasePassword = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
        
    } 

    [xml]$web = Get-Content $webroot\web.config

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.DbServer']").value = [string]$DatabaseServer

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value = [string]$DatabaseName

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlUser']").value = [string]$DatabaseUser

    $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlPwd']").value = [string]$DatabasePassword

}
#Save Configuration to webroot config
$web.Save("$webroot\web.config")

#Reloading the configuration to run test
[xml]$web = Get-Content $webroot\web.config

$TestDbServer = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.DbServer']").value

$TestDbName = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.Database']").value

$TestDbUser = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlUser']").value

$TestDbPass = $web.SelectSingleNode("configuration/appSettings/add[@key='DataAccess.SqlPwd']").value

#Setting up connection test.

$dbConn = New-Object System.Data.SqlClient.SqlConnection

$dbConn.ConnectionString = "Data Source=$TestDbServer;User ID=$TestDbUser;Password=`"$TestDbPass`";Database=$TestDbName"

try{

    $dbConn.Open()

    $result = $true

}

catch{

    $result = $_.Exception.Message

}
Finally{

    $dbConn.Close()

}

$commandParameter = " -encrypt `"$webroot\web.config`""

Start-Process $command $commandParameter -PassThru -Wait

if($result -ne $true){

    Write-Host "`nThe connection to the Database Server failed:" -ForegroundColor Red
    Write-Host $result -ForegroundColor Red

}
else{

    Write-Host "`nThe connection to the Database Server was successful!" -ForegroundColor Green

}
```

### <a name="troubleshooting"></a><span data-ttu-id="c8c03-386">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c8c03-386">Troubleshooting</span></span>

-   <span data-ttu-id="c8c03-387">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="c8c03-387">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="c8c03-388">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="c8c03-388">The login failed.</span></span> <span data-ttu-id="c8c03-389">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="c8c03-389">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="c8c03-390">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="c8c03-390">Could not establish a connection.</span></span> <span data-ttu-id="c8c03-391">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="c8c03-391">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="c8c03-392">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="c8c03-392">The server was not found or was not accessible.</span></span> <span data-ttu-id="c8c03-393">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c8c03-393">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="c8c03-394">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="c8c03-394">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="c8c03-395">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="c8c03-395">Login credentials are not correct.</span></span> <span data-ttu-id="c8c03-396">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="c8c03-396">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>
