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
ms.openlocfilehash: c375cd2b540af9f71c75a2d8dd1b60260d800dd8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191878"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="2cd16-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="2cd16-103">In-place upgrade process for on-premises environments</span></span>

> [!NOTE]
> <span data-ttu-id="2cd16-104">実稼働環境のアップグレードを実行する前に、サンドボックス環境のアップグレードを実行してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-104">Please perform the upgrade with your sandbox environment before upgrading your production environment.</span></span>

<span data-ttu-id="2cd16-105">このトピックでは、Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-105">This topic provides the detailed process for upgrading on-premises environments of Finance and Operations from version 7.x to 8.1.</span></span>  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-8-20-to-81"></a><span data-ttu-id="2cd16-106">7.x (プラットフォーム更新プログラム 8 ~ 20) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="2cd16-106">On-premises upgrade from version 7.x (with Platform update 8-20) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="2cd16-107">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-107">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="2cd16-108">7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-108">To upgrade from version 7.x to 8.1, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="2cd16-109">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2cd16-109">An overview of each path is given below:</span></span>

-   <span data-ttu-id="2cd16-110">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-110">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="2cd16-111">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-111">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="2cd16-112">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-112">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="2cd16-113">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-113">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="2cd16-114">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2cd16-114">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="2cd16-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="2cd16-115">Prerequisites</span></span>

1.  <span data-ttu-id="2cd16-116">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-116">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="2cd16-117">**資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-117">Under **Select asset type**, choose **Downloadable VHD**, and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="2cd16-118">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-118">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="2cd16-119">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-119">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="2cd16-120">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-120">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="2cd16-121">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-121">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="2cd16-122">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="2cd16-122">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="2cd16-123">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-123">Connect to the VM.</span></span> <span data-ttu-id="2cd16-124">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-124">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="2cd16-125">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-125">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="2cd16-126">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-126">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="2cd16-127">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="2cd16-127">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="2cd16-128">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-128">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="2cd16-129">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-129">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="2cd16-130">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-130">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="2cd16-131">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-131">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="2cd16-132">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-132">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="2cd16-133">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="2cd16-133">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="2cd16-134">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-134">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="2cd16-135">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-135">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="2cd16-136">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-136">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="2cd16-137">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-137">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > <span data-ttu-id="2cd16-138">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-138">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="2cd16-139">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-139">If you would like to edit more values, refer to  Appendix A.</span></span>

    <span data-ttu-id="2cd16-140">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-140">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="2cd16-141">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-141">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="2cd16-142">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-142">a.</span></span>  <span data-ttu-id="2cd16-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="2cd16-144">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-144">b.</span></span>  <span data-ttu-id="2cd16-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="2cd16-146">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-146">c.</span></span>  <span data-ttu-id="2cd16-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="2cd16-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="2cd16-148">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-148">During the execution of cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span> 
    
    <span data-ttu-id="2cd16-149">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="2cd16-149">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="2cd16-150">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-150">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="2cd16-151">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-151">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="2cd16-152">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-152">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="2cd16-153">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-153">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="2cd16-154">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-154">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="2cd16-155">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-155">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="2cd16-156">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-156">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="2cd16-157">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-157">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="2cd16-158">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-158">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="2cd16-159">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-159">If you had customizations:</span></span>

    <span data-ttu-id="2cd16-160">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-160">a.</span></span>  <span data-ttu-id="2cd16-161">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-161">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="2cd16-162">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-162">b.</span></span>  <span data-ttu-id="2cd16-163">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-163">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="2cd16-164">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-164">c.</span></span>  <span data-ttu-id="2cd16-165">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-165">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="2cd16-166">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-166">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="2cd16-167">d.</span><span class="sxs-lookup"><span data-stu-id="2cd16-167">d.</span></span>  <span data-ttu-id="2cd16-168">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-168">The database will need to be configured.</span></span> <span data-ttu-id="2cd16-169">[Finance and Operations データベースを構成](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-169">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="2cd16-170">e.</span><span class="sxs-lookup"><span data-stu-id="2cd16-170">e.</span></span>  <span data-ttu-id="2cd16-171">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-171">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="2cd16-172">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-172">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="2cd16-173">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-173">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="2cd16-174">f.</span><span class="sxs-lookup"><span data-stu-id="2cd16-174">f.</span></span>  <span data-ttu-id="2cd16-175">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-175">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="2cd16-176">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-176">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="2cd16-177">g.</span><span class="sxs-lookup"><span data-stu-id="2cd16-177">g.</span></span>  <span data-ttu-id="2cd16-178">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-178">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="2cd16-179">h.</span><span class="sxs-lookup"><span data-stu-id="2cd16-179">h.</span></span>  <span data-ttu-id="2cd16-180">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-180">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="2cd16-181">i.</span><span class="sxs-lookup"><span data-stu-id="2cd16-181">i.</span></span>  <span data-ttu-id="2cd16-182">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-182">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="2cd16-183">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-183">If you didn't have customizations:</span></span>

    <span data-ttu-id="2cd16-184">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-184">a.</span></span>  <span data-ttu-id="2cd16-185">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-185">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="2cd16-186">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-186">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="2cd16-187">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-187">b.</span></span>  <span data-ttu-id="2cd16-188">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-188">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="2cd16-189">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-189">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="2cd16-190">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-190">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="2cd16-191">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="2cd16-191">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="2cd16-192">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-192">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="2cd16-193">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-193">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="2cd16-194">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-194">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="2cd16-195">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-195">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="2cd16-196">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-196">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="2cd16-197">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-197">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="2cd16-198">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-198">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="2cd16-199">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="2cd16-199">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="2cd16-200">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-200">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="2cd16-201">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-201">Open a new PowerShell as Administrator and execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="2cd16-202">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-202">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="2cd16-203">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-203">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="2cd16-204">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-204">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="2cd16-205">SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-205">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="2cd16-206">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-206">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="2cd16-207">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-207">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="2cd16-208">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-208">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="2cd16-209">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-209">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="2cd16-210">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-210">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="2cd16-211">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-211">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="2cd16-212">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-212">a.</span></span>  <span data-ttu-id="2cd16-213">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-213">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="2cd16-214">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-214">b.</span></span>  <span data-ttu-id="2cd16-215">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-215">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="2cd16-216">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-216">c.</span></span>  <span data-ttu-id="2cd16-217">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="2cd16-217">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="2cd16-218">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-218">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="2cd16-219">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="2cd16-219">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="2cd16-220">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-220">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="2cd16-221">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-221">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="2cd16-222">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-222">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="2cd16-223">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-223">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="2cd16-224">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-224">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="2cd16-225">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-225">If you had customizations:</span></span>

    <span data-ttu-id="2cd16-226">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-226">a.</span></span>  <span data-ttu-id="2cd16-227">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-227">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="2cd16-228">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-228">b.</span></span>  <span data-ttu-id="2cd16-229">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-229">Under **Select asset type** choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="2cd16-230">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-230">c.</span></span>  <span data-ttu-id="2cd16-231">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-231">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="2cd16-232">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-232">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="2cd16-233">d.</span><span class="sxs-lookup"><span data-stu-id="2cd16-233">d.</span></span>  <span data-ttu-id="2cd16-234">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-234">The database will need to be configured.</span></span> <span data-ttu-id="2cd16-235">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-235">Follow the steps under [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

    <span data-ttu-id="2cd16-236">e.</span><span class="sxs-lookup"><span data-stu-id="2cd16-236">e.</span></span>  <span data-ttu-id="2cd16-237">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-237">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="2cd16-238">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-238">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="2cd16-239">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-239">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="2cd16-240">f.</span><span class="sxs-lookup"><span data-stu-id="2cd16-240">f.</span></span>  <span data-ttu-id="2cd16-241">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-241">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="2cd16-242">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-242">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="2cd16-243">g.</span><span class="sxs-lookup"><span data-stu-id="2cd16-243">g.</span></span>  <span data-ttu-id="2cd16-244">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-244">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="2cd16-245">h.</span><span class="sxs-lookup"><span data-stu-id="2cd16-245">h.</span></span>  <span data-ttu-id="2cd16-246">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-246">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="2cd16-247">i.</span><span class="sxs-lookup"><span data-stu-id="2cd16-247">i.</span></span>  <span data-ttu-id="2cd16-248">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-248">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="2cd16-249">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-249">If you didn't have customizations:</span></span>

    <span data-ttu-id="2cd16-250">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-250">a.</span></span>  <span data-ttu-id="2cd16-251">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-251">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="2cd16-252">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-252">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="2cd16-253">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-253">b.</span></span>  <span data-ttu-id="2cd16-254">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-254">Setup a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="2cd16-255">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-255">For more information, see [Set up and deploy on-premises environments ](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="2cd16-256">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-256">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a><span data-ttu-id="2cd16-257">7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="2cd16-257">On-premises upgrade from version 7.x (with Platform update 21 or later) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="2cd16-258">このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-258">Be aware that this upgrade process takes time complete and Finance and Operations will be inaccessible for the entire duration.</span></span>

<span data-ttu-id="2cd16-259">オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-259">To upgrade from on-premises 7.x to on-premises 8.1 there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="2cd16-260">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="2cd16-260">An overview of each path is given below:</span></span>

-   <span data-ttu-id="2cd16-261">**VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-261">**Upgrading from within VHD** - This path involves copying your database into the VHD and executing the upgrade inside it.</span></span> <span data-ttu-id="2cd16-262">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-262">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="2cd16-263">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-263">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="2cd16-264">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-264">The upgrade process is still executed from within the VHD.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2cd16-265">VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2cd16-265">The VHD does not need external network access in order to carry out the data upgrade process.</span></span>


### <a name="prerequisites"></a><span data-ttu-id="2cd16-266">必要条件</span><span class="sxs-lookup"><span data-stu-id="2cd16-266">Prerequisites</span></span>

1.  <span data-ttu-id="2cd16-267">LCS では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-267">In LCS, go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="2cd16-268">**資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-268">Under **Select asset type**, choose downloadable VHD and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="2cd16-269">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-269">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="2cd16-270">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-270">The files you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="2cd16-271">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-271">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="2cd16-272">Hyper-V を使用して、VM を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-272">Using Hyper-V launch a VM and attach the VHD.</span></span> <span data-ttu-id="2cd16-273">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="2cd16-273">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="2cd16-274">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-274">Connect to the VM.</span></span> <span data-ttu-id="2cd16-275">資格情報についてはこちらをご覧ください。https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span><span class="sxs-lookup"><span data-stu-id="2cd16-275">You can find the credentials here: https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span></span>

6.  <span data-ttu-id="2cd16-276">続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-276">Before proceeding it will be necessary to upgrade the platform version of the VHD so that it is in the same state as the one in your environment.</span></span> <span data-ttu-id="2cd16-277">基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-277">You basically want the version number of the platform in the VHD to match exactly to the version number in your environment.</span></span> <span data-ttu-id="2cd16-278">これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-278">In order to do this you can check your environments history in LCS to see which packages have been applied from your asset library.</span></span> <span data-ttu-id="2cd16-279">VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-279">Keep in mind that the VHD is already in Platform update 20 (7.0.5030.35333) so it will probably already contain some packages that you installed manually into your environment, but may not include the latest binary updates that you applied to your environment.</span></span>

7.  <span data-ttu-id="2cd16-280">パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-280">After you have located the package or packages that have to be applied, download them into the VHD from LCS.</span></span>

8.  <span data-ttu-id="2cd16-281">各パッケージについては、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-281">For each package do the following:</span></span>

    <span data-ttu-id="2cd16-282">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-282">a.</span></span>  <span data-ttu-id="2cd16-283">c:\\D365FFOUpgrade\\ などのパッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-283">Extract the package, such as c:\\D365FFOUpgrade\\</span></span>

    <span data-ttu-id="2cd16-284">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-284">b.</span></span>  <span data-ttu-id="2cd16-285">管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-285">Open a Command Prompt as Administrator and change directory to the unzipped folder.</span></span>

    <span data-ttu-id="2cd16-286">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-286">c.</span></span>  <span data-ttu-id="2cd16-287">実行</span><span class="sxs-lookup"><span data-stu-id="2cd16-287">Execute</span></span>

        A.  AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml

        B.  AxUpdateInstaller.exe import -runbookfile=upgrade.xml

        C.  AxUpdateInstaller.exe execute -runbookid=upgrade

9.  <span data-ttu-id="2cd16-288">アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-288">If you have any application extensions or customizations install them now into the VHD, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="2cd16-289">アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-289">Check with your ISV or VAR if you need to prepare your environment in any way before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="2cd16-290">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="2cd16-290">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="2cd16-291">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-291">Shut down On-Premises AOSs, BI and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="2cd16-292">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-292">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="2cd16-293">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-293">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="2cd16-294">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-294">In the VHD go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="2cd16-295">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-295">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="2cd16-296">例 c:\\D365FFOUpgrade</span><span class="sxs-lookup"><span data-stu-id="2cd16-296">Eg c:\\D365FFOUpgrade</span></span>\\

5.  <span data-ttu-id="2cd16-297">管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-297">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 4.</span></span>

6.  <span data-ttu-id="2cd16-298">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-298">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="2cd16-299">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-299">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="2cd16-300">(オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-300">(Optional) If the name of your restored database is not AXDB, using PowerShell with Administrator privileges execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > <span data-ttu-id="2cd16-301">(通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-301">Substitute \<DB-Name\> with the appropriate value in your case (typically AXDB).</span></span> <span data-ttu-id="2cd16-302">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-302">If you would like to edit more values, refer to Appendix A.</span></span>

    <span data-ttu-id="2cd16-303">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-303">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="2cd16-304">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-304">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="2cd16-305">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-305">a.</span></span>  <span data-ttu-id="2cd16-306">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-306">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="2cd16-307">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-307">b.</span></span>  <span data-ttu-id="2cd16-308">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-308">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="2cd16-309">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-309">c.</span></span>  <span data-ttu-id="2cd16-310">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="2cd16-310">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="2cd16-311">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-311">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="2cd16-312">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="2cd16-312">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="2cd16-313">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-313">Once the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="2cd16-314">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-314">If you have customizations from ISVs or VARs check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="2cd16-315">実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-315">Restore the database into your environment with a different name from the production one (typically AXDBupgraded).</span></span>

11. <span data-ttu-id="2cd16-316">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-316">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="2cd16-317">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-317">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="2cd16-318">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-318">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="2cd16-319">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-319">This process may take longer depending on the number of nodes that you have.</span></span>

13. <span data-ttu-id="2cd16-320">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-320">In LCS, go to the Shared Assets Library.</span></span>

14. <span data-ttu-id="2cd16-321">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-321">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

15. <span data-ttu-id="2cd16-322">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-322">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="2cd16-323">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-323">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

16. <span data-ttu-id="2cd16-324">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-324">The database will need to be configured.</span></span> <span data-ttu-id="2cd16-325">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-325">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

17. <span data-ttu-id="2cd16-326">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-326">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="2cd16-327">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-327">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="2cd16-328">配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-328">When you deploy, the database that you should specify should be the one created in step 15 (typically AXDB).</span></span>

18. <span data-ttu-id="2cd16-329">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-329">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="2cd16-330">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-330">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

19. <span data-ttu-id="2cd16-331">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-331">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

20. <span data-ttu-id="2cd16-332">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-332">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

21. <span data-ttu-id="2cd16-333">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-333">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

22. <span data-ttu-id="2cd16-334">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-334">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="2cd16-335">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="2cd16-335">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="2cd16-336">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-336">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="2cd16-337">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-337">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="2cd16-338">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-338">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="2cd16-339">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-339">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="2cd16-340">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-340">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="2cd16-341">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-341">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="2cd16-342">C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-342">Paste the file wherever you want and unzip it, such as C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="2cd16-343">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-343">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="2cd16-344">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-344">Open a new PowerShell as Administrator and execute:</span></span>

    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="2cd16-345">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-345">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="2cd16-346">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-346">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="2cd16-347">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-347">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="2cd16-348">SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-348">You will need to add the Certificate Authority certificate that signed your SQL server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="2cd16-349">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-349">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span> 
    >
    > - <span data-ttu-id="2cd16-350">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-350">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database that you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="2cd16-351">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-351">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="2cd16-352">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-352">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="2cd16-353">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-353">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="2cd16-354">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-354">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="2cd16-355">a.</span><span class="sxs-lookup"><span data-stu-id="2cd16-355">a.</span></span>  <span data-ttu-id="2cd16-356">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-356">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="2cd16-357">b.</span><span class="sxs-lookup"><span data-stu-id="2cd16-357">b.</span></span>  <span data-ttu-id="2cd16-358">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="2cd16-358">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="2cd16-359">c.</span><span class="sxs-lookup"><span data-stu-id="2cd16-359">c.</span></span>  <span data-ttu-id="2cd16-360">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="2cd16-360">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="2cd16-361">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-361">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="2cd16-362">この問題を解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="2cd16-362">To resolve this issue, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="2cd16-363">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-363">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="2cd16-364">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-364">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="2cd16-365">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-365">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="2cd16-366">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-366">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="2cd16-367">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-367">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="2cd16-368">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-368">In LCS, go to the Shared Assets Library.</span></span>

13. <span data-ttu-id="2cd16-369">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-369">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

14. <span data-ttu-id="2cd16-370">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-370">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="2cd16-371">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-371">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

15. <span data-ttu-id="2cd16-372">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-372">The database will need to be configured.</span></span> <span data-ttu-id="2cd16-373">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2cd16-373">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

16. <span data-ttu-id="2cd16-374">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-374">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="2cd16-375">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cd16-375">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="2cd16-376">配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-376">When you deploy, the database that you should specify should be the one created in step 14 (typically AXDB).</span></span>

17. <span data-ttu-id="2cd16-377">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-377">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="2cd16-378">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="2cd16-378">Otherwise when the environment initially synchs  with the database it will delete any customization or extensions related data.</span></span>

18. <span data-ttu-id="2cd16-379">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-379">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

19. <span data-ttu-id="2cd16-380">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-380">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

20. <span data-ttu-id="2cd16-381">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-381">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

21. <span data-ttu-id="2cd16-382">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-382">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a><span data-ttu-id="2cd16-383">付録 A</span><span class="sxs-lookup"><span data-stu-id="2cd16-383">Appendix A</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="2cd16-384">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="2cd16-384">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="2cd16-385">このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="2cd16-385">This script is only meant to be run from a Onebox VHD environment.</span></span>
>
> <span data-ttu-id="2cd16-386">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="2cd16-386">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="2cd16-387">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-387">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="2cd16-388">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-388">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="2cd16-389">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cd16-389">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="2cd16-390">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-390">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="2cd16-391">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="2cd16-391">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="2cd16-392">**-DatabaseServer** - Finance and Operations (オンプレミス) データベースが含まれているデータベース サーバー。</span><span class="sxs-lookup"><span data-stu-id="2cd16-392">**-DatabaseServer** - Database server containing Finance and Operations (on-premises) database.</span></span>

-   <span data-ttu-id="2cd16-393">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="2cd16-393">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="2cd16-394">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="2cd16-394">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="2cd16-395">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-395">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="2cd16-396">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2cd16-396">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="2cd16-397">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="2cd16-397">**Configure-On-Premises-Upgrade.ps1**</span></span>
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

### <a name="troubleshooting"></a><span data-ttu-id="2cd16-398">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2cd16-398">Troubleshooting</span></span>

-   <span data-ttu-id="2cd16-399">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="2cd16-399">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="2cd16-400">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="2cd16-400">The login failed.</span></span> <span data-ttu-id="2cd16-401">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="2cd16-401">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="2cd16-402">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="2cd16-402">Could not establish a connection.</span></span> <span data-ttu-id="2cd16-403">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="2cd16-403">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="2cd16-404">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="2cd16-404">The server was not found or was not accessible.</span></span> <span data-ttu-id="2cd16-405">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2cd16-405">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="2cd16-406">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="2cd16-406">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="2cd16-407">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="2cd16-407">Login credentials are not correct.</span></span> <span data-ttu-id="2cd16-408">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="2cd16-408">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>
