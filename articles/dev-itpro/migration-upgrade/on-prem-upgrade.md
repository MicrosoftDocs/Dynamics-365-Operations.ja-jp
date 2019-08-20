---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。
author: laneswenka
manager: AnnBe
ms.date: 06/18/2019
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
ms.openlocfilehash: a95a3a6865632d3b0f2c288da794dccbcf6ac450
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741176"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="e683c-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="e683c-103">In-place upgrade process for on-premises environments</span></span>

> [!NOTE]
> <span data-ttu-id="e683c-104">実稼働環境のアップグレードを実行する前に、サンドボックス環境のアップグレードを実行してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-104">Please perform the upgrade with your sandbox environment before upgrading your production environment.</span></span>

<span data-ttu-id="e683c-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="e683c-105">This topic provides the detailed process for upgrading on-premises environments of Microsoft Dynamics 365 for Finance and Operations from version 7.x to 8.1.</span></span>  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-8-20-to-81"></a><span data-ttu-id="e683c-106">7.x (プラットフォーム更新プログラム 8 ~ 20) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="e683c-106">On-premises upgrade from version 7.x (with Platform update 8-20) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="e683c-107">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-107">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="e683c-108">7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-108">To upgrade from version 7.x to 8.1, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="e683c-109">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="e683c-109">An overview of each path is given below:</span></span>

-   <span data-ttu-id="e683c-110">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-110">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="e683c-111">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="e683c-111">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="e683c-112">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="e683c-112">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="e683c-113">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-113">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="e683c-114">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e683c-114">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e683c-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="e683c-115">Prerequisites</span></span>

1.  <span data-ttu-id="e683c-116">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-116">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="e683c-117">**資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-117">Under **Select asset type**, choose **Downloadable VHD**, and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="e683c-118">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="e683c-118">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="e683c-119">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="e683c-119">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="e683c-120">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-120">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="e683c-121">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="e683c-121">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="e683c-122">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="e683c-122">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="e683c-123">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="e683c-123">Connect to the VM.</span></span> <span data-ttu-id="e683c-124">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="e683c-124">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="e683c-125">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-125">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="e683c-126">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-126">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="e683c-127">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="e683c-127">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="e683c-128">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="e683c-128">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="e683c-129">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-129">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="e683c-130">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-130">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="e683c-131">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e683c-131">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="e683c-132">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-132">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="e683c-133">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="e683c-133">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="e683c-134">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-134">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="e683c-135">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="e683c-135">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="e683c-136">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-136">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="e683c-137">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-137">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > <span data-ttu-id="e683c-138">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e683c-138">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="e683c-139">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="e683c-139">If you would like to edit more values, refer to  Appendix A.</span></span>

    <span data-ttu-id="e683c-140">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-140">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="e683c-141">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-141">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="e683c-142">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-142">a.</span></span>  <span data-ttu-id="e683c-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="e683c-144">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-144">b.</span></span>  <span data-ttu-id="e683c-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="e683c-146">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-146">c.</span></span>  <span data-ttu-id="e683c-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="e683c-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="e683c-148">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e683c-148">During the execution of cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span> 
    
    <span data-ttu-id="e683c-149">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="e683c-149">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="e683c-150">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-150">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="e683c-151">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-151">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="e683c-152">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="e683c-152">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="e683c-153">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-153">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="e683c-154">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="e683c-154">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="e683c-155">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-155">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="e683c-156">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-156">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="e683c-157">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-157">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="e683c-158">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-158">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="e683c-159">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="e683c-159">If you had customizations:</span></span>

    <span data-ttu-id="e683c-160">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-160">a.</span></span>  <span data-ttu-id="e683c-161">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-161">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="e683c-162">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-162">b.</span></span>  <span data-ttu-id="e683c-163">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-163">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="e683c-164">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-164">c.</span></span>  <span data-ttu-id="e683c-165">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-165">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="e683c-166">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-166">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="e683c-167">d.</span><span class="sxs-lookup"><span data-stu-id="e683c-167">d.</span></span>  <span data-ttu-id="e683c-168">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-168">The database will need to be configured.</span></span> <span data-ttu-id="e683c-169">[Finance and Operations データベースを構成](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e683c-169">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="e683c-170">e.</span><span class="sxs-lookup"><span data-stu-id="e683c-170">e.</span></span>  <span data-ttu-id="e683c-171">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-171">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="e683c-172">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-172">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="e683c-173">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-173">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="e683c-174">f.</span><span class="sxs-lookup"><span data-stu-id="e683c-174">f.</span></span>  <span data-ttu-id="e683c-175">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-175">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="e683c-176">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-176">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="e683c-177">g.</span><span class="sxs-lookup"><span data-stu-id="e683c-177">g.</span></span>  <span data-ttu-id="e683c-178">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-178">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="e683c-179">h.</span><span class="sxs-lookup"><span data-stu-id="e683c-179">h.</span></span>  <span data-ttu-id="e683c-180">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-180">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="e683c-181">i.</span><span class="sxs-lookup"><span data-stu-id="e683c-181">i.</span></span>  <span data-ttu-id="e683c-182">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-182">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="e683c-183">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-183">If you didn't have customizations:</span></span>

    <span data-ttu-id="e683c-184">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-184">a.</span></span>  <span data-ttu-id="e683c-185">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-185">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="e683c-186">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-186">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="e683c-187">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-187">b.</span></span>  <span data-ttu-id="e683c-188">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-188">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="e683c-189">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-189">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="e683c-190">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-190">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="e683c-191">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="e683c-191">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="e683c-192">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-192">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="e683c-193">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-193">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="e683c-194">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-194">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="e683c-195">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="e683c-195">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="e683c-196">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-196">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="e683c-197">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e683c-197">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="e683c-198">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-198">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="e683c-199">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="e683c-199">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="e683c-200">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-200">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="e683c-201">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-201">Open a new PowerShell as Administrator and execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="e683c-202">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e683c-202">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="e683c-203">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e683c-203">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="e683c-204">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-204">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="e683c-205">SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-205">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="e683c-206">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="e683c-206">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="e683c-207">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-207">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="e683c-208">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="e683c-208">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="e683c-209">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-209">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="e683c-210">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="e683c-210">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="e683c-211">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-211">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="e683c-212">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-212">a.</span></span>  <span data-ttu-id="e683c-213">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-213">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="e683c-214">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-214">b.</span></span>  <span data-ttu-id="e683c-215">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-215">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="e683c-216">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-216">c.</span></span>  <span data-ttu-id="e683c-217">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="e683c-217">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="e683c-218">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e683c-218">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="e683c-219">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="e683c-219">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="e683c-220">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-220">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="e683c-221">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-221">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="e683c-222">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="e683c-222">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="e683c-223">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-223">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="e683c-224">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-224">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="e683c-225">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="e683c-225">If you had customizations:</span></span>

    <span data-ttu-id="e683c-226">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-226">a.</span></span>  <span data-ttu-id="e683c-227">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-227">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="e683c-228">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-228">b.</span></span>  <span data-ttu-id="e683c-229">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-229">Under **Select asset type** choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="e683c-230">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-230">c.</span></span>  <span data-ttu-id="e683c-231">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-231">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="e683c-232">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-232">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="e683c-233">d.</span><span class="sxs-lookup"><span data-stu-id="e683c-233">d.</span></span>  <span data-ttu-id="e683c-234">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-234">The database will need to be configured.</span></span> <span data-ttu-id="e683c-235">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e683c-235">Follow the steps under [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="e683c-236">e.</span><span class="sxs-lookup"><span data-stu-id="e683c-236">e.</span></span>  <span data-ttu-id="e683c-237">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-237">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="e683c-238">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-238">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="e683c-239">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-239">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="e683c-240">f.</span><span class="sxs-lookup"><span data-stu-id="e683c-240">f.</span></span>  <span data-ttu-id="e683c-241">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-241">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="e683c-242">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-242">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="e683c-243">g.</span><span class="sxs-lookup"><span data-stu-id="e683c-243">g.</span></span>  <span data-ttu-id="e683c-244">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-244">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="e683c-245">h.</span><span class="sxs-lookup"><span data-stu-id="e683c-245">h.</span></span>  <span data-ttu-id="e683c-246">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-246">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="e683c-247">i.</span><span class="sxs-lookup"><span data-stu-id="e683c-247">i.</span></span>  <span data-ttu-id="e683c-248">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-248">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="e683c-249">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-249">If you didn't have customizations:</span></span>

    <span data-ttu-id="e683c-250">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-250">a.</span></span>  <span data-ttu-id="e683c-251">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-251">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="e683c-252">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-252">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="e683c-253">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-253">b.</span></span>  <span data-ttu-id="e683c-254">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="e683c-254">Setup a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="e683c-255">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-255">For more information, see [Set up and deploy on-premises environments ](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="e683c-256">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-256">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a><span data-ttu-id="e683c-257">7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="e683c-257">On-premises upgrade from version 7.x (with Platform update 21 or later) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="e683c-258">このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-258">Be aware that this upgrade process takes time complete and Finance and Operations will be inaccessible for the entire duration.</span></span>

<span data-ttu-id="e683c-259">オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-259">To upgrade from on-premises 7.x to on-premises 8.1 there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="e683c-260">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="e683c-260">An overview of each path is given below:</span></span>

-   <span data-ttu-id="e683c-261">**VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-261">**Upgrading from within VHD** - This path involves copying your database into the VHD and executing the upgrade inside it.</span></span> <span data-ttu-id="e683c-262">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="e683c-262">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="e683c-263">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="e683c-263">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="e683c-264">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-264">The upgrade process is still executed from within the VHD.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e683c-265">VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e683c-265">The VHD does not need external network access in order to carry out the data upgrade process.</span></span>


### <a name="prerequisites"></a><span data-ttu-id="e683c-266">必要条件</span><span class="sxs-lookup"><span data-stu-id="e683c-266">Prerequisites</span></span>

1.  <span data-ttu-id="e683c-267">LCS では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-267">In LCS, go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="e683c-268">**資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-268">Under **Select asset type**, choose downloadable VHD and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="e683c-269">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="e683c-269">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="e683c-270">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="e683c-270">The files you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="e683c-271">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-271">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="e683c-272">Hyper-V を使用して、VM を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="e683c-272">Using Hyper-V launch a VM and attach the VHD.</span></span> <span data-ttu-id="e683c-273">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="e683c-273">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="e683c-274">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="e683c-274">Connect to the VM.</span></span> <span data-ttu-id="e683c-275">資格情報についてはこちらをご覧ください。https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span><span class="sxs-lookup"><span data-stu-id="e683c-275">You can find the credentials here: https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span></span>

6.  <span data-ttu-id="e683c-276">続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-276">Before proceeding it will be necessary to upgrade the platform version of the VHD so that it is in the same state as the one in your environment.</span></span> <span data-ttu-id="e683c-277">基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-277">You basically want the version number of the platform in the VHD to match exactly to the version number in your environment.</span></span> <span data-ttu-id="e683c-278">これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="e683c-278">In order to do this you can check your environments history in LCS to see which packages have been applied from your asset library.</span></span> <span data-ttu-id="e683c-279">VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-279">Keep in mind that the VHD is already in Platform update 20 (7.0.5030.35333) so it will probably already contain some packages that you installed manually into your environment, but may not include the latest binary updates that you applied to your environment.</span></span>

7.  <span data-ttu-id="e683c-280">パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-280">After you have located the package or packages that have to be applied, download them into the VHD from LCS.</span></span>

8.  <span data-ttu-id="e683c-281">各パッケージについては、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="e683c-281">For each package do the following:</span></span>

    <span data-ttu-id="e683c-282">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-282">a.</span></span>  <span data-ttu-id="e683c-283">c:\\D365FFOUpgrade\\ などのパッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-283">Extract the package, such as c:\\D365FFOUpgrade\\</span></span>

    <span data-ttu-id="e683c-284">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-284">b.</span></span>  <span data-ttu-id="e683c-285">管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-285">Open a Command Prompt as Administrator and change directory to the unzipped folder.</span></span>

    <span data-ttu-id="e683c-286">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-286">c.</span></span>  <span data-ttu-id="e683c-287">実行</span><span class="sxs-lookup"><span data-stu-id="e683c-287">Execute</span></span>

        A.  AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml

        B.  AxUpdateInstaller.exe import -runbookfile=upgrade.xml

        C.  AxUpdateInstaller.exe execute -runbookid=upgrade

9.  <span data-ttu-id="e683c-288">アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-288">If you have any application extensions or customizations install them now into the VHD, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="e683c-289">アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-289">Check with your ISV or VAR if you need to prepare your environment in any way before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="e683c-290">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="e683c-290">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="e683c-291">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-291">Shut down On-Premises AOSs, BI and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="e683c-292">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-292">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="e683c-293">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-293">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="e683c-294">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e683c-294">In the VHD go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="e683c-295">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-295">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="e683c-296">例 c:\\D365FFOUpgrade</span><span class="sxs-lookup"><span data-stu-id="e683c-296">Eg c:\\D365FFOUpgrade</span></span>\\

5.  <span data-ttu-id="e683c-297">管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-297">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 4.</span></span>

6.  <span data-ttu-id="e683c-298">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="e683c-298">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="e683c-299">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-299">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="e683c-300">(オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-300">(Optional) If the name of your restored database is not AXDB, using PowerShell with Administrator privileges execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > <span data-ttu-id="e683c-301">(通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e683c-301">Substitute \<DB-Name\> with the appropriate value in your case (typically AXDB).</span></span> <span data-ttu-id="e683c-302">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="e683c-302">If you would like to edit more values, refer to Appendix A.</span></span>

    <span data-ttu-id="e683c-303">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-303">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="e683c-304">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-304">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="e683c-305">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-305">a.</span></span>  <span data-ttu-id="e683c-306">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-306">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="e683c-307">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-307">b.</span></span>  <span data-ttu-id="e683c-308">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-308">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="e683c-309">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-309">c.</span></span>  <span data-ttu-id="e683c-310">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="e683c-310">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="e683c-311">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e683c-311">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="e683c-312">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="e683c-312">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="e683c-313">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-313">Once the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="e683c-314">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-314">If you have customizations from ISVs or VARs check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="e683c-315">実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="e683c-315">Restore the database into your environment with a different name from the production one (typically AXDBupgraded).</span></span>

11. <span data-ttu-id="e683c-316">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-316">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="e683c-317">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="e683c-317">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="e683c-318">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-318">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="e683c-319">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-319">This process may take longer depending on the number of nodes that you have.</span></span>

13. <span data-ttu-id="e683c-320">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-320">In LCS, go to the Shared Assets Library.</span></span>

14. <span data-ttu-id="e683c-321">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-321">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

15. <span data-ttu-id="e683c-322">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-322">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="e683c-323">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-323">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

16. <span data-ttu-id="e683c-324">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-324">The database will need to be configured.</span></span> <span data-ttu-id="e683c-325">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e683c-325">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

17. <span data-ttu-id="e683c-326">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-326">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="e683c-327">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-327">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="e683c-328">配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-328">When you deploy, the database that you should specify should be the one created in step 15 (typically AXDB).</span></span>

18. <span data-ttu-id="e683c-329">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-329">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="e683c-330">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-330">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

19. <span data-ttu-id="e683c-331">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-331">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

20. <span data-ttu-id="e683c-332">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-332">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

21. <span data-ttu-id="e683c-333">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-333">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

22. <span data-ttu-id="e683c-334">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-334">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="e683c-335">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="e683c-335">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="e683c-336">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-336">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="e683c-337">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="e683c-337">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="e683c-338">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-338">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="e683c-339">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="e683c-339">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="e683c-340">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-340">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="e683c-341">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e683c-341">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="e683c-342">C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e683c-342">Paste the file wherever you want and unzip it, such as C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="e683c-343">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-343">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="e683c-344">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-344">Open a new PowerShell as Administrator and execute:</span></span>

    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="e683c-345">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e683c-345">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="e683c-346">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e683c-346">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="e683c-347">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-347">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="e683c-348">SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-348">You will need to add the Certificate Authority certificate that signed your SQL server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="e683c-349">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="e683c-349">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span> 
    >
    > - <span data-ttu-id="e683c-350">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-350">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database that you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="e683c-351">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="e683c-351">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="e683c-352">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-352">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="e683c-353">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="e683c-353">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="e683c-354">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-354">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="e683c-355">a.</span><span class="sxs-lookup"><span data-stu-id="e683c-355">a.</span></span>  <span data-ttu-id="e683c-356">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-356">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="e683c-357">b.</span><span class="sxs-lookup"><span data-stu-id="e683c-357">b.</span></span>  <span data-ttu-id="e683c-358">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="e683c-358">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="e683c-359">c.</span><span class="sxs-lookup"><span data-stu-id="e683c-359">c.</span></span>  <span data-ttu-id="e683c-360">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="e683c-360">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="e683c-361">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e683c-361">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="e683c-362">この問題を解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="e683c-362">To resolve this issue, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="e683c-363">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-363">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="e683c-364">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-364">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="e683c-365">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="e683c-365">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="e683c-366">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="e683c-366">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="e683c-367">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e683c-367">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="e683c-368">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="e683c-368">In LCS, go to the Shared Assets Library.</span></span>

13. <span data-ttu-id="e683c-369">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e683c-369">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

14. <span data-ttu-id="e683c-370">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-370">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="e683c-371">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-371">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

15. <span data-ttu-id="e683c-372">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-372">The database will need to be configured.</span></span> <span data-ttu-id="e683c-373">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e683c-373">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

16. <span data-ttu-id="e683c-374">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="e683c-374">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="e683c-375">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e683c-375">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="e683c-376">配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-376">When you deploy, the database that you should specify should be the one created in step 14 (typically AXDB).</span></span>

17. <span data-ttu-id="e683c-377">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="e683c-377">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="e683c-378">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e683c-378">Otherwise when the environment initially synchs  with the database it will delete any customization or extensions related data.</span></span>

18. <span data-ttu-id="e683c-379">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="e683c-379">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

19. <span data-ttu-id="e683c-380">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="e683c-380">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

20. <span data-ttu-id="e683c-381">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e683c-381">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

21. <span data-ttu-id="e683c-382">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-382">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a><span data-ttu-id="e683c-383">付録 A</span><span class="sxs-lookup"><span data-stu-id="e683c-383">Appendix A</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="e683c-384">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="e683c-384">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="e683c-385">このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="e683c-385">This script is only meant to be run from a Onebox VHD environment.</span></span>
>
> <span data-ttu-id="e683c-386">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="e683c-386">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="e683c-387">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="e683c-387">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="e683c-388">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="e683c-388">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="e683c-389">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e683c-389">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="e683c-390">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="e683c-390">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="e683c-391">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="e683c-391">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="e683c-392">**-DatabaseServer** - Microsoft Dynamics 365 for Finance and Operations、オンプレミス データベースが含まれているデータベース サーバーです。</span><span class="sxs-lookup"><span data-stu-id="e683c-392">**-DatabaseServer** - Database server containing Microsoft Dynamics 365 for Finance and Operations, on-premises database.</span></span>

-   <span data-ttu-id="e683c-393">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="e683c-393">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="e683c-394">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="e683c-394">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="e683c-395">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="e683c-395">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="e683c-396">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e683c-396">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="e683c-397">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="e683c-397">**Configure-On-Premises-Upgrade.ps1**</span></span>
```
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

### <a name="troubleshooting"></a><span data-ttu-id="e683c-398">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e683c-398">Troubleshooting</span></span>

-   <span data-ttu-id="e683c-399">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="e683c-399">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="e683c-400">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="e683c-400">The login failed.</span></span> <span data-ttu-id="e683c-401">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="e683c-401">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="e683c-402">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e683c-402">Could not establish a connection.</span></span> <span data-ttu-id="e683c-403">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="e683c-403">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="e683c-404">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="e683c-404">The server was not found or was not accessible.</span></span> <span data-ttu-id="e683c-405">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e683c-405">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="e683c-406">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="e683c-406">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="e683c-407">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="e683c-407">Login credentials are not correct.</span></span> <span data-ttu-id="e683c-408">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="e683c-408">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>
