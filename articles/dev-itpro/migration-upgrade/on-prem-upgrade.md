---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。
author: laneswenka
manager: AnnBe
ms.date: 01/31/2019
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
ms.openlocfilehash: f6e9ad5c64fe728f1f0022bba30f62d152d3a5a3
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2019
ms.locfileid: "373428"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="0db27-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="0db27-103">In-place upgrade process for on-premises environments</span></span>

<span data-ttu-id="0db27-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="0db27-104">This topic provides the detailed process for upgrading on-premises environments of Microsoft Dynamics 365 for Finance and Operations from version 7.x to 8.1.</span></span>  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-15-20-to-81"></a><span data-ttu-id="0db27-105">7.x (プラットフォーム更新プログラム 15 ~ 20) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="0db27-105">On-premises upgrade from version 7.x (with Platform update 15-20) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="0db27-106">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-106">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="0db27-107">7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-107">To upgrade from version 7.x to 8.1, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="0db27-108">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="0db27-108">An overview of each path is given below:</span></span>

-   <span data-ttu-id="0db27-109">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-109">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="0db27-110">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="0db27-110">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="0db27-111">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="0db27-111">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="0db27-112">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-112">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="0db27-113">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="0db27-113">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0db27-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="0db27-114">Prerequisites</span></span>

1.  <span data-ttu-id="0db27-115">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-115">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="0db27-116">**資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-116">Under **Select asset type**, choose **Downloadable VHD**, and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="0db27-117">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="0db27-117">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="0db27-118">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0db27-118">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="0db27-119">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-119">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="0db27-120">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="0db27-120">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="0db27-121">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="0db27-121">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="0db27-122">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="0db27-122">Connect to the VM.</span></span> <span data-ttu-id="0db27-123">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="0db27-123">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="0db27-124">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-124">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="0db27-125">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-125">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="0db27-126">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="0db27-126">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="0db27-127">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="0db27-127">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="0db27-128">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-128">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="0db27-129">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-129">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="0db27-130">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0db27-130">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="0db27-131">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-131">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="0db27-132">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="0db27-132">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="0db27-133">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-133">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="0db27-134">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="0db27-134">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="0db27-135">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-135">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="0db27-136">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-136">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>

    <span data-ttu-id="0db27-137">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\'</span><span class="sxs-lookup"><span data-stu-id="0db27-137">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\'</span></span>

    > [!NOTE] 
    > <span data-ttu-id="0db27-138">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0db27-138">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="0db27-139">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="0db27-139">If you would like to edit more values, refer to  Appendix A.</span></span>

    <span data-ttu-id="0db27-140">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-140">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="0db27-141">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-141">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="0db27-142">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-142">a.</span></span>  <span data-ttu-id="0db27-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-143">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="0db27-144">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-144">b.</span></span>  <span data-ttu-id="0db27-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-145">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="0db27-146">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-146">c.</span></span>  <span data-ttu-id="0db27-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="0db27-147">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="0db27-148">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0db27-148">During the execution of cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span> 
    
    <span data-ttu-id="0db27-149">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="0db27-149">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="0db27-150">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-150">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="0db27-151">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-151">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="0db27-152">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="0db27-152">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="0db27-153">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-153">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="0db27-154">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="0db27-154">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="0db27-155">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-155">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="0db27-156">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-156">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="0db27-157">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-157">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="0db27-158">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-158">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="0db27-159">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="0db27-159">If you had customizations:</span></span>

    <span data-ttu-id="0db27-160">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-160">a.</span></span>  <span data-ttu-id="0db27-161">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-161">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="0db27-162">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-162">b.</span></span>  <span data-ttu-id="0db27-163">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-163">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="0db27-164">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-164">c.</span></span>  <span data-ttu-id="0db27-165">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-165">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="0db27-166">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-166">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="0db27-167">d.</span><span class="sxs-lookup"><span data-stu-id="0db27-167">d.</span></span>  <span data-ttu-id="0db27-168">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-168">The database will need to be configured.</span></span> <span data-ttu-id="0db27-169">[Finance and Operations データベースを構成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0db27-169">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="0db27-170">e.</span><span class="sxs-lookup"><span data-stu-id="0db27-170">e.</span></span>  <span data-ttu-id="0db27-171">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-171">Set up a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-172">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-172">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="0db27-173">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-173">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="0db27-174">f.</span><span class="sxs-lookup"><span data-stu-id="0db27-174">f.</span></span>  <span data-ttu-id="0db27-175">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-175">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="0db27-176">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-176">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="0db27-177">g.</span><span class="sxs-lookup"><span data-stu-id="0db27-177">g.</span></span>  <span data-ttu-id="0db27-178">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-178">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="0db27-179">h.</span><span class="sxs-lookup"><span data-stu-id="0db27-179">h.</span></span>  <span data-ttu-id="0db27-180">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-180">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="0db27-181">i.</span><span class="sxs-lookup"><span data-stu-id="0db27-181">i.</span></span>  <span data-ttu-id="0db27-182">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-182">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="0db27-183">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-183">If you didn't have customizations:</span></span>

    <span data-ttu-id="0db27-184">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-184">a.</span></span>  <span data-ttu-id="0db27-185">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-185">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="0db27-186">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-186">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="0db27-187">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-187">b.</span></span>  <span data-ttu-id="0db27-188">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-188">Set up a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-189">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-189">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="0db27-190">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-190">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK\_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="0db27-191">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="0db27-191">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="0db27-192">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-192">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="0db27-193">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-193">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="0db27-194">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-194">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="0db27-195">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="0db27-195">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="0db27-196">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-196">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="0db27-197">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0db27-197">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="0db27-198">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-198">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="0db27-199">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="0db27-199">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="0db27-200">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-200">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="0db27-201">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-201">Open a new PowerShell as Administrator and execute:</span></span>

    <span data-ttu-id="0db27-202">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\' -DatabaseServer \'\<SqlServerName\>\' -DatabaseUser \'\<User\>\' -DatabasePassword \'\<Password\>\'</span><span class="sxs-lookup"><span data-stu-id="0db27-202">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\' -DatabaseServer \'\<SqlServerName\>\' -DatabaseUser \'\<User\>\' -DatabasePassword \'\<Password\>\'</span></span>

    > [!NOTE]
    > <span data-ttu-id="0db27-203">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0db27-203">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="0db27-204">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0db27-204">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="0db27-205">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-205">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="0db27-206">SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-206">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="0db27-207">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="0db27-207">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="0db27-208">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-208">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="0db27-209">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="0db27-209">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="0db27-210">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-210">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="0db27-211">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="0db27-211">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="0db27-212">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-212">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="0db27-213">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-213">a.</span></span>  <span data-ttu-id="0db27-214">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-214">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="0db27-215">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-215">b.</span></span>  <span data-ttu-id="0db27-216">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-216">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="0db27-217">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-217">c.</span></span>  <span data-ttu-id="0db27-218">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="0db27-218">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="0db27-219">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0db27-219">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="0db27-220">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="0db27-220">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="0db27-221">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-221">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="0db27-222">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-222">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="0db27-223">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="0db27-223">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="0db27-224">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-224">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="0db27-225">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-225">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="0db27-226">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="0db27-226">If you had customizations:</span></span>

    <span data-ttu-id="0db27-227">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-227">a.</span></span>  <span data-ttu-id="0db27-228">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-228">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="0db27-229">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-229">b.</span></span>  <span data-ttu-id="0db27-230">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-230">Under **Select asset type** choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="0db27-231">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-231">c.</span></span>  <span data-ttu-id="0db27-232">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-232">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="0db27-233">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-233">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="0db27-234">d.</span><span class="sxs-lookup"><span data-stu-id="0db27-234">d.</span></span>  <span data-ttu-id="0db27-235">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-235">The database will need to be configured.</span></span> <span data-ttu-id="0db27-236">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0db27-236">Follow the steps under [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="0db27-237">e.</span><span class="sxs-lookup"><span data-stu-id="0db27-237">e.</span></span>  <span data-ttu-id="0db27-238">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-238">Set up a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-239">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-239">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="0db27-240">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-240">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="0db27-241">f.</span><span class="sxs-lookup"><span data-stu-id="0db27-241">f.</span></span>  <span data-ttu-id="0db27-242">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-242">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="0db27-243">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-243">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="0db27-244">g.</span><span class="sxs-lookup"><span data-stu-id="0db27-244">g.</span></span>  <span data-ttu-id="0db27-245">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-245">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="0db27-246">h.</span><span class="sxs-lookup"><span data-stu-id="0db27-246">h.</span></span>  <span data-ttu-id="0db27-247">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-247">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="0db27-248">i.</span><span class="sxs-lookup"><span data-stu-id="0db27-248">i.</span></span>  <span data-ttu-id="0db27-249">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-249">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="0db27-250">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-250">If you didn't have customizations:</span></span>

    <span data-ttu-id="0db27-251">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-251">a.</span></span>  <span data-ttu-id="0db27-252">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-252">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="0db27-253">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-253">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="0db27-254">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-254">b.</span></span>  <span data-ttu-id="0db27-255">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-255">Setup a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-256">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-256">For more information, see [Set up and deploy on-premises environments ](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="0db27-257">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-257">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK\_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a><span data-ttu-id="0db27-258">7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="0db27-258">On-premises upgrade from version 7.x (with Platform update 21 or later) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="0db27-259">このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-259">Be aware that this upgrade process takes time complete and Finance and Operations will be inaccessible for the entire duration.</span></span>

<span data-ttu-id="0db27-260">オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-260">To upgrade from on-premises 7.x to on-premises 8.1 there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="0db27-261">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="0db27-261">An overview of each path is given below:</span></span>

-   <span data-ttu-id="0db27-262">**VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-262">**Upgrading from within VHD** - This path involves copying your database into the VHD and executing the upgrade inside it.</span></span> <span data-ttu-id="0db27-263">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="0db27-263">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="0db27-264">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="0db27-264">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="0db27-265">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-265">The upgrade process is still executed from within the VHD.</span></span>
    
> [!NOTE]
> <span data-ttu-id="0db27-266">VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="0db27-266">The VHD does not need external network access in order to carry out the data upgrade process.</span></span>


### <a name="prerequisites"></a><span data-ttu-id="0db27-267">必要条件</span><span class="sxs-lookup"><span data-stu-id="0db27-267">Prerequisites</span></span>

1.  <span data-ttu-id="0db27-268">LCS では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-268">In LCS, go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="0db27-269">**資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-269">Under **Select asset type**, choose downloadable VHD and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="0db27-270">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="0db27-270">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="0db27-271">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="0db27-271">The files you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="0db27-272">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-272">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="0db27-273">Hyper-V を使用して、VM を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="0db27-273">Using Hyper-V launch a VM and attach the VHD.</span></span> <span data-ttu-id="0db27-274">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="0db27-274">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="0db27-275">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="0db27-275">Connect to the VM.</span></span> <span data-ttu-id="0db27-276">資格情報についてはこちらをご覧ください。https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span><span class="sxs-lookup"><span data-stu-id="0db27-276">You can find the credentials here: https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span></span>

6.  <span data-ttu-id="0db27-277">続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-277">Before proceeding it will be necessary to upgrade the platform version of the VHD so that it is in the same state as the one in your environment.</span></span> <span data-ttu-id="0db27-278">基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-278">You basically want the version number of the platform in the VHD to match exactly to the version number in your environment.</span></span> <span data-ttu-id="0db27-279">これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="0db27-279">In order to do this you can check your environments history in LCS to see which packages have been applied from your asset library.</span></span> <span data-ttu-id="0db27-280">VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-280">Keep in mind that the VHD is already in Platform update 20 (7.0.5030.35333) so it will probably already contain some packages that you installed manually into your environment, but may not include the latest binary updates that you applied to your environment.</span></span>

7.  <span data-ttu-id="0db27-281">パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-281">After you have located the package or packages that have to be applied, download them into the VHD from LCS.</span></span>

8.  <span data-ttu-id="0db27-282">各パッケージについては、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0db27-282">For each package do the following:</span></span>

    <span data-ttu-id="0db27-283">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-283">a.</span></span>  <span data-ttu-id="0db27-284">c:\\D365FFOUpgrade\\ などのパッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-284">Extract the package, such as c:\\D365FFOUpgrade\\</span></span>

    <span data-ttu-id="0db27-285">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-285">b.</span></span>  <span data-ttu-id="0db27-286">管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-286">Open a Command Prompt as Administrator and change directory to the unzipped folder.</span></span>

    <span data-ttu-id="0db27-287">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-287">c.</span></span>  <span data-ttu-id="0db27-288">実行</span><span class="sxs-lookup"><span data-stu-id="0db27-288">Execute</span></span>

        A.  AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml

        B.  AxUpdateInstaller.exe import -runbookfile=upgrade.xml

        C.  AxUpdateInstaller.exe execute -runbookid=upgrade

9.  <span data-ttu-id="0db27-289">アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-289">If you have any application extensions or customizations install them now into the VHD, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="0db27-290">アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-290">Check with your ISV or VAR if you need to prepare your environment in any way before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="0db27-291">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="0db27-291">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="0db27-292">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-292">Shut down On-Premises AOSs, BI and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="0db27-293">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-293">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="0db27-294">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-294">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="0db27-295">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0db27-295">In the VHD go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="0db27-296">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="0db27-296">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="0db27-297">例 c:\\D365FFOUpgrade\\</span><span class="sxs-lookup"><span data-stu-id="0db27-297">Eg c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="0db27-298">管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-298">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 4.</span></span>

6.  <span data-ttu-id="0db27-299">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="0db27-299">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="0db27-300">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-300">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="0db27-301">(オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-301">(Optional) If the name of your restored database is not AXDB, using PowerShell with Administrator privileges execute:</span></span>

    <span data-ttu-id="0db27-302">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\'</span><span class="sxs-lookup"><span data-stu-id="0db27-302">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\'</span></span>

    > [!NOTE] 
    > <span data-ttu-id="0db27-303">(通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0db27-303">Substitute \<DB-Name\> with the appropriate value in your case (typically AXDB).</span></span> <span data-ttu-id="0db27-304">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="0db27-304">If you would like to edit more values, refer to Appendix A.</span></span>

    <span data-ttu-id="0db27-305">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-305">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="0db27-306">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-306">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="0db27-307">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-307">a.</span></span>  <span data-ttu-id="0db27-308">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-308">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="0db27-309">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-309">b.</span></span>  <span data-ttu-id="0db27-310">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-310">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="0db27-311">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-311">c.</span></span>  <span data-ttu-id="0db27-312">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="0db27-312">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="0db27-313">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0db27-313">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="0db27-314">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="0db27-314">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="0db27-315">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-315">Once the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="0db27-316">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-316">If you have customizations from ISVs or VARs check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="0db27-317">実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="0db27-317">Restore the database into your environment with a different name from the production one (typically AXDBupgraded).</span></span>

11. <span data-ttu-id="0db27-318">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-318">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="0db27-319">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="0db27-319">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="0db27-320">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-320">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="0db27-321">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-321">This process may take longer depending on the number of nodes that you have.</span></span>

13. <span data-ttu-id="0db27-322">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-322">In LCS, go to the Shared Assets Library.</span></span>

14. <span data-ttu-id="0db27-323">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-323">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

15. <span data-ttu-id="0db27-324">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-324">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="0db27-325">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-325">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

16. <span data-ttu-id="0db27-326">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-326">The database will need to be configured.</span></span> <span data-ttu-id="0db27-327">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0db27-327">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

17. <span data-ttu-id="0db27-328">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-328">Set up a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-329">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-329">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="0db27-330">配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-330">When you deploy, the database that you should specify should be the one created in step 15 (typically AXDB).</span></span>

18. <span data-ttu-id="0db27-331">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-331">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="0db27-332">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-332">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

19. <span data-ttu-id="0db27-333">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-333">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

20. <span data-ttu-id="0db27-334">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-334">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

21. <span data-ttu-id="0db27-335">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-335">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

22. <span data-ttu-id="0db27-336">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-336">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK\_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="0db27-337">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="0db27-337">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="0db27-338">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-338">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="0db27-339">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="0db27-339">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="0db27-340">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-340">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="0db27-341">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="0db27-341">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="0db27-342">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-342">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="0db27-343">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0db27-343">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="0db27-344">C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="0db27-344">Paste the file wherever you want and unzip it, such as C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="0db27-345">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-345">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="0db27-346">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-346">Open a new PowerShell as Administrator and execute:</span></span>

    <span data-ttu-id="0db27-347">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\' -DatabaseServer \'\<SqlServerName\>\' -DatabaseUser \'\<User\>\' -DatabasePassword \'\<Password\>\'</span><span class="sxs-lookup"><span data-stu-id="0db27-347">.\\Configure-On-Premises-Upgrade.ps1 -DatabaseName \'\<DB-name\>\' -DatabaseServer \'\<SqlServerName\>\' -DatabaseUser \'\<User\>\' -DatabasePassword \'\<Password\>\'</span></span>

    > [!NOTE]
    > <span data-ttu-id="0db27-348">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0db27-348">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="0db27-349">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0db27-349">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="0db27-350">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-350">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="0db27-351">SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-351">You will need to add the Certificate Authority certificate that signed your SQL server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="0db27-352">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="0db27-352">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span> 
    >
    > - <span data-ttu-id="0db27-353">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-353">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database that you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="0db27-354">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="0db27-354">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="0db27-355">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-355">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="0db27-356">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="0db27-356">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="0db27-357">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-357">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="0db27-358">a.</span><span class="sxs-lookup"><span data-stu-id="0db27-358">a.</span></span>  <span data-ttu-id="0db27-359">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-359">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="0db27-360">b.</span><span class="sxs-lookup"><span data-stu-id="0db27-360">b.</span></span>  <span data-ttu-id="0db27-361">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="0db27-361">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="0db27-362">c.</span><span class="sxs-lookup"><span data-stu-id="0db27-362">c.</span></span>  <span data-ttu-id="0db27-363">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="0db27-363">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="0db27-364">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0db27-364">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="0db27-365">この問題を解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="0db27-365">To resolve this issue, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="0db27-366">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-366">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="0db27-367">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-367">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="0db27-368">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="0db27-368">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="0db27-369">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0db27-369">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="0db27-370">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="0db27-370">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="0db27-371">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="0db27-371">In LCS, go to the Shared Assets Library.</span></span>

13. <span data-ttu-id="0db27-372">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0db27-372">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

14. <span data-ttu-id="0db27-373">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-373">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="0db27-374">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-374">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

15. <span data-ttu-id="0db27-375">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-375">The database will need to be configured.</span></span> <span data-ttu-id="0db27-376">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0db27-376">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

16. <span data-ttu-id="0db27-377">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="0db27-377">Set up a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="0db27-378">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0db27-378">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="0db27-379">配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-379">When you deploy, the database that you should specify should be the one created in step 14 (typically AXDB).</span></span>

17. <span data-ttu-id="0db27-380">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="0db27-380">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="0db27-381">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0db27-381">Otherwise when the environment initially synchs  with the database it will delete any customization or extensions related data.</span></span>

18. <span data-ttu-id="0db27-382">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="0db27-382">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

19. <span data-ttu-id="0db27-383">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="0db27-383">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

20. <span data-ttu-id="0db27-384">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="0db27-384">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

21. <span data-ttu-id="0db27-385">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-385">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK\_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a><span data-ttu-id="0db27-386">付録 A</span><span class="sxs-lookup"><span data-stu-id="0db27-386">Appendix A</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="0db27-387">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="0db27-387">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="0db27-388">このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="0db27-388">This script is only meant to be run from a Onebox VHD environment.</span></span>
>
> <span data-ttu-id="0db27-389">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="0db27-389">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="0db27-390">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="0db27-390">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="0db27-391">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="0db27-391">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="0db27-392">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0db27-392">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="0db27-393">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="0db27-393">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="0db27-394">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="0db27-394">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="0db27-395">**-DatabaseServer** - Microsoft Dynamics 365 for Finance and Operations、オンプレミス データベースが含まれているデータベース サーバーです。</span><span class="sxs-lookup"><span data-stu-id="0db27-395">**-DatabaseServer** - Database server containing Microsoft Dynamics 365 for Finance and Operations, on-premises database.</span></span>

-   <span data-ttu-id="0db27-396">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="0db27-396">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="0db27-397">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="0db27-397">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="0db27-398">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="0db27-398">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="0db27-399">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0db27-399">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="0db27-400">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="0db27-400">**Configure-On-Premises-Upgrade.ps1**</span></span>
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

### <a name="troubleshooting"></a><span data-ttu-id="0db27-401">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="0db27-401">Troubleshooting</span></span>

-   <span data-ttu-id="0db27-402">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="0db27-402">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="0db27-403">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="0db27-403">The login failed.</span></span> <span data-ttu-id="0db27-404">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="0db27-404">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="0db27-405">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="0db27-405">Could not establish a connection.</span></span> <span data-ttu-id="0db27-406">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="0db27-406">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="0db27-407">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="0db27-407">The server was not found or was not accessible.</span></span> <span data-ttu-id="0db27-408">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0db27-408">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="0db27-409">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="0db27-409">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="0db27-410">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="0db27-410">Login credentials are not correct.</span></span> <span data-ttu-id="0db27-411">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="0db27-411">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>
