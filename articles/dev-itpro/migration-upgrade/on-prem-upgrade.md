---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。
author: laneswenka
manager: AnnBe
ms.date: 03/07/2019
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
ms.openlocfilehash: 296d394562eb3d345a2fc37659076b29ab4c3015
ms.sourcegitcommit: ab88de98a1958734213eb9d9b1988508b055f748
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538762"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="1fd22-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="1fd22-103">In-place upgrade process for on-premises environments</span></span>

<span data-ttu-id="1fd22-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 7.x のオンプレミス環境を 8.1 にアップグレードする詳細プロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-104">This topic provides the detailed process for upgrading on-premises environments of Microsoft Dynamics 365 for Finance and Operations from version 7.x to 8.1.</span></span>  

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-8-20-to-81"></a><span data-ttu-id="1fd22-105">7.x (プラットフォーム更新プログラム 8 ~ 20) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="1fd22-105">On-premises upgrade from version 7.x (with Platform update 8-20) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="1fd22-106">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-106">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="1fd22-107">7.x から 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-107">To upgrade from version 7.x to 8.1, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="1fd22-108">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="1fd22-108">An overview of each path is given below:</span></span>

-   <span data-ttu-id="1fd22-109">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-109">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="1fd22-110">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-110">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="1fd22-111">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-111">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="1fd22-112">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-112">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="1fd22-113">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1fd22-113">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1fd22-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="1fd22-114">Prerequisites</span></span>

1.  <span data-ttu-id="1fd22-115">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-115">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="1fd22-116">**資産タイプの選択**で、**ダウンロード可能な VHD** を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-116">Under **Select asset type**, choose **Downloadable VHD**, and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="1fd22-117">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-117">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="1fd22-118">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-118">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="1fd22-119">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-119">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="1fd22-120">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-120">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="1fd22-121">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="1fd22-121">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="1fd22-122">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-122">Connect to the VM.</span></span> <span data-ttu-id="1fd22-123">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-123">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="1fd22-124">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-124">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="1fd22-125">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-125">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="1fd22-126">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="1fd22-126">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="1fd22-127">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-127">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="1fd22-128">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-128">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="1fd22-129">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-129">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="1fd22-130">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-130">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="1fd22-131">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-131">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="1fd22-132">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="1fd22-132">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="1fd22-133">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-133">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="1fd22-134">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-134">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="1fd22-135">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-135">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="1fd22-136">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-136">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > <span data-ttu-id="1fd22-137">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-137">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="1fd22-138">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-138">If you would like to edit more values, refer to  Appendix A.</span></span>

    <span data-ttu-id="1fd22-139">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-139">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="1fd22-140">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-140">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="1fd22-141">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-141">a.</span></span>  <span data-ttu-id="1fd22-142">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-142">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="1fd22-143">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-143">b.</span></span>  <span data-ttu-id="1fd22-144">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-144">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="1fd22-145">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-145">c.</span></span>  <span data-ttu-id="1fd22-146">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="1fd22-146">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="1fd22-147">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-147">During the execution of cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span> 
    
    <span data-ttu-id="1fd22-148">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="1fd22-148">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="1fd22-149">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-149">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="1fd22-150">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-150">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="1fd22-151">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-151">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="1fd22-152">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-152">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="1fd22-153">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-153">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="1fd22-154">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-154">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="1fd22-155">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-155">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="1fd22-156">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-156">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="1fd22-157">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-157">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="1fd22-158">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-158">If you had customizations:</span></span>

    <span data-ttu-id="1fd22-159">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-159">a.</span></span>  <span data-ttu-id="1fd22-160">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-160">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="1fd22-161">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-161">b.</span></span>  <span data-ttu-id="1fd22-162">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-162">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="1fd22-163">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-163">c.</span></span>  <span data-ttu-id="1fd22-164">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-164">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="1fd22-165">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-165">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/en-us/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="1fd22-166">d.</span><span class="sxs-lookup"><span data-stu-id="1fd22-166">d.</span></span>  <span data-ttu-id="1fd22-167">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-167">The database will need to be configured.</span></span> <span data-ttu-id="1fd22-168">[Finance and Operations データベースを構成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-168">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="1fd22-169">e.</span><span class="sxs-lookup"><span data-stu-id="1fd22-169">e.</span></span>  <span data-ttu-id="1fd22-170">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-170">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="1fd22-171">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-171">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="1fd22-172">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-172">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="1fd22-173">f.</span><span class="sxs-lookup"><span data-stu-id="1fd22-173">f.</span></span>  <span data-ttu-id="1fd22-174">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-174">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="1fd22-175">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-175">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="1fd22-176">g.</span><span class="sxs-lookup"><span data-stu-id="1fd22-176">g.</span></span>  <span data-ttu-id="1fd22-177">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-177">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="1fd22-178">h.</span><span class="sxs-lookup"><span data-stu-id="1fd22-178">h.</span></span>  <span data-ttu-id="1fd22-179">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-179">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="1fd22-180">i.</span><span class="sxs-lookup"><span data-stu-id="1fd22-180">i.</span></span>  <span data-ttu-id="1fd22-181">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-181">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="1fd22-182">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-182">If you didn't have customizations:</span></span>

    <span data-ttu-id="1fd22-183">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-183">a.</span></span>  <span data-ttu-id="1fd22-184">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-184">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="1fd22-185">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-185">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="1fd22-186">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-186">b.</span></span>  <span data-ttu-id="1fd22-187">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-187">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="1fd22-188">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-188">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="1fd22-189">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-189">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="1fd22-190">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1fd22-190">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="1fd22-191">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-191">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="1fd22-192">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-192">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="1fd22-193">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-193">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="1fd22-194">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-194">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="1fd22-195">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-195">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="1fd22-196">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-196">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="1fd22-197">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-197">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="1fd22-198">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="1fd22-198">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="1fd22-199">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-199">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="1fd22-200">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-200">Open a new PowerShell as Administrator and execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="1fd22-201">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-201">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="1fd22-202">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-202">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="1fd22-203">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-203">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="1fd22-204">SQL Server 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-204">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="1fd22-205">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-205">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="1fd22-206">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-206">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="1fd22-207">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-207">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="1fd22-208">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-208">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="1fd22-209">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-209">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="1fd22-210">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-210">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="1fd22-211">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-211">a.</span></span>  <span data-ttu-id="1fd22-212">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-212">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="1fd22-213">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-213">b.</span></span>  <span data-ttu-id="1fd22-214">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-214">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="1fd22-215">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-215">c.</span></span>  <span data-ttu-id="1fd22-216">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="1fd22-216">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="1fd22-217">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-217">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="1fd22-218">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="1fd22-218">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="1fd22-219">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-219">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="1fd22-220">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-220">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="1fd22-221">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-221">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="1fd22-222">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-222">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="1fd22-223">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-223">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="1fd22-224">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-224">If you had customizations:</span></span>

    <span data-ttu-id="1fd22-225">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-225">a.</span></span>  <span data-ttu-id="1fd22-226">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-226">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="1fd22-227">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-227">b.</span></span>  <span data-ttu-id="1fd22-228">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-228">Under **Select asset type** choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

    <span data-ttu-id="1fd22-229">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-229">c.</span></span>  <span data-ttu-id="1fd22-230">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-230">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="1fd22-231">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-231">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="1fd22-232">d.</span><span class="sxs-lookup"><span data-stu-id="1fd22-232">d.</span></span>  <span data-ttu-id="1fd22-233">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-233">The database will need to be configured.</span></span> <span data-ttu-id="1fd22-234">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-234">Follow the steps under [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="1fd22-235">e.</span><span class="sxs-lookup"><span data-stu-id="1fd22-235">e.</span></span>  <span data-ttu-id="1fd22-236">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-236">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="1fd22-237">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-237">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="1fd22-238">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-238">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="1fd22-239">f.</span><span class="sxs-lookup"><span data-stu-id="1fd22-239">f.</span></span>  <span data-ttu-id="1fd22-240">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-240">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="1fd22-241">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-241">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="1fd22-242">g.</span><span class="sxs-lookup"><span data-stu-id="1fd22-242">g.</span></span>  <span data-ttu-id="1fd22-243">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-243">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="1fd22-244">h.</span><span class="sxs-lookup"><span data-stu-id="1fd22-244">h.</span></span>  <span data-ttu-id="1fd22-245">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-245">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="1fd22-246">i.</span><span class="sxs-lookup"><span data-stu-id="1fd22-246">i.</span></span>  <span data-ttu-id="1fd22-247">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-247">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="1fd22-248">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-248">If you didn't have customizations:</span></span>

    <span data-ttu-id="1fd22-249">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-249">a.</span></span>  <span data-ttu-id="1fd22-250">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-250">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="1fd22-251">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-251">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="1fd22-252">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-252">b.</span></span>  <span data-ttu-id="1fd22-253">新しい環境を設定し、バージョン 8.1 で配置します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-253">Setup a new environment and deploy it with version 8.1.</span></span> <span data-ttu-id="1fd22-254">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-254">For more information, see [Set up and deploy on-premises environments ](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="1fd22-255">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-255">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="on-premises-upgrade-from-version-7x-with-platform-update-21-or-later-to-81"></a><span data-ttu-id="1fd22-256">7.x (プラットフォーム更新プログラム 21 以降) から 8.1 へのオンプレミス アップグレード</span><span class="sxs-lookup"><span data-stu-id="1fd22-256">On-premises upgrade from version 7.x (with Platform update 21 or later) to 8.1</span></span>

> [!NOTE]
> <span data-ttu-id="1fd22-257">このアップグレード プロセスは完了に時間がかかり、プロセス中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-257">Be aware that this upgrade process takes time complete and Finance and Operations will be inaccessible for the entire duration.</span></span>

<span data-ttu-id="1fd22-258">オンプレミス 7.x からオンプレミス 8.1 にアップグレードする上で、現在サポートされている可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-258">To upgrade from on-premises 7.x to on-premises 8.1 there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="1fd22-259">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="1fd22-259">An overview of each path is given below:</span></span>

-   <span data-ttu-id="1fd22-260">**VHD 内からのアップグレード** - このパスは、VHD にデータベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-260">**Upgrading from within VHD** - This path involves copying your database into the VHD and executing the upgrade inside it.</span></span> <span data-ttu-id="1fd22-261">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-261">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="1fd22-262">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-262">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="1fd22-263">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-263">The upgrade process is still executed from within the VHD.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1fd22-264">VHD では、データ アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1fd22-264">The VHD does not need external network access in order to carry out the data upgrade process.</span></span>


### <a name="prerequisites"></a><span data-ttu-id="1fd22-265">必要条件</span><span class="sxs-lookup"><span data-stu-id="1fd22-265">Prerequisites</span></span>

1.  <span data-ttu-id="1fd22-266">LCS では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-266">In LCS, go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="1fd22-267">**資産タイプの選択**で、ダウンロード可能な VHD を選択し、FinOps8.1 パッケージのすべての 13 部分をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-267">Under **Select asset type**, choose downloadable VHD and download all 13 parts of the FinOps8.1 package.</span></span> <span data-ttu-id="1fd22-268">すべてのパーツをダウンロードするには、合計で 36 GB の空き領域が必要となります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-268">You will need a total of 36 GB of free space to download all the parts.</span></span>

3.  <span data-ttu-id="1fd22-269">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-269">The files you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="1fd22-270">少なくとも 86 GBの空き領域に VHD を展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-270">Extract the VHD to a location with at least 86 GB of free space.</span></span>

4.  <span data-ttu-id="1fd22-271">Hyper-V を使用して、VM を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-271">Using Hyper-V launch a VM and attach the VHD.</span></span> <span data-ttu-id="1fd22-272">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="1fd22-272">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="1fd22-273">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-273">Connect to the VM.</span></span> <span data-ttu-id="1fd22-274">資格情報についてはこちらをご覧ください。https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span><span class="sxs-lookup"><span data-stu-id="1fd22-274">You can find the credentials here: https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally</span></span>

6.  <span data-ttu-id="1fd22-275">続行する前に、VHD のプラットフォームのバージョンを、環境にあるものと同じ状態になるようにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-275">Before proceeding it will be necessary to upgrade the platform version of the VHD so that it is in the same state as the one in your environment.</span></span> <span data-ttu-id="1fd22-276">基本的には、環境内のバージョン番号と正確に一致するように VHD 内のプラットフォームのバージョン数を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-276">You basically want the version number of the platform in the VHD to match exactly to the version number in your environment.</span></span> <span data-ttu-id="1fd22-277">これを行うには、LCS で環境の履歴を確認し、資産ライブラリからどのパッケージが適用されているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-277">In order to do this you can check your environments history in LCS to see which packages have been applied from your asset library.</span></span> <span data-ttu-id="1fd22-278">VHD が既にプラットフォーム更新 プログラム 20 (7.0.5030.35333) に含まれているため、環境に手動でインストールした一部のパッケージが既に含まれていますが、環境に適用した最新のバイナリ更新プログラムが含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-278">Keep in mind that the VHD is already in Platform update 20 (7.0.5030.35333) so it will probably already contain some packages that you installed manually into your environment, but may not include the latest binary updates that you applied to your environment.</span></span>

7.  <span data-ttu-id="1fd22-279">パッケージまたは適用する必要があるパッケージを検索した後に、LCS から VHD にそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-279">After you have located the package or packages that have to be applied, download them into the VHD from LCS.</span></span>

8.  <span data-ttu-id="1fd22-280">各パッケージについては、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-280">For each package do the following:</span></span>

    <span data-ttu-id="1fd22-281">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-281">a.</span></span>  <span data-ttu-id="1fd22-282">c:\\D365FFOUpgrade\\ などのパッケージを展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-282">Extract the package, such as c:\\D365FFOUpgrade\\</span></span>

    <span data-ttu-id="1fd22-283">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-283">b.</span></span>  <span data-ttu-id="1fd22-284">管理者としてコマンド プロンプトを開き、展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-284">Open a Command Prompt as Administrator and change directory to the unzipped folder.</span></span>

    <span data-ttu-id="1fd22-285">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-285">c.</span></span>  <span data-ttu-id="1fd22-286">実行</span><span class="sxs-lookup"><span data-stu-id="1fd22-286">Execute</span></span>

        A.  AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml

        B.  AxUpdateInstaller.exe import -runbookfile=upgrade.xml

        C.  AxUpdateInstaller.exe execute -runbookid=upgrade

9.  <span data-ttu-id="1fd22-287">アプリケーションの拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-287">If you have any application extensions or customizations install them now into the VHD, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="1fd22-288">アップグレード前に、どんな方法でも環境を準備する必要がある場合は、ISV または VAR に確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-288">Check with your ISV or VAR if you need to prepare your environment in any way before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="1fd22-289">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="1fd22-289">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="1fd22-290">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-290">Shut down On-Premises AOSs, BI and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="1fd22-291">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-291">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="1fd22-292">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-292">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="1fd22-293">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-293">In the VHD go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="1fd22-294">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-294">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="1fd22-295">例 c:\\D365FFOUpgrade\\</span><span class="sxs-lookup"><span data-stu-id="1fd22-295">Eg c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="1fd22-296">管理者としてコマンド プロンプトを開き、手順 4 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-296">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 4.</span></span>

6.  <span data-ttu-id="1fd22-297">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-297">Restore the backup that you created into the Onebox VM.</span></span> <span data-ttu-id="1fd22-298">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-298">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="1fd22-299">(オプション) 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-299">(Optional) If the name of your restored database is not AXDB, using PowerShell with Administrator privileges execute:</span></span>
    
    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > <span data-ttu-id="1fd22-300">(通常、AXDB などの) 適切な値に \<DB-Name\> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-300">Substitute \<DB-Name\> with the appropriate value in your case (typically AXDB).</span></span> <span data-ttu-id="1fd22-301">値をさらに編集する場合は、付録 A を参照します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-301">If you would like to edit more values, refer to Appendix A.</span></span>

    <span data-ttu-id="1fd22-302">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-302">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="1fd22-303">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-303">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="1fd22-304">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-304">a.</span></span>  <span data-ttu-id="1fd22-305">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-305">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="1fd22-306">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-306">b.</span></span>  <span data-ttu-id="1fd22-307">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-307">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="1fd22-308">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-308">c.</span></span>  <span data-ttu-id="1fd22-309">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="1fd22-309">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="1fd22-310">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-310">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="1fd22-311">これを解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="1fd22-311">To resolve this, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="1fd22-312">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-312">Once the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="1fd22-313">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-313">If you have customizations from ISVs or VARs check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="1fd22-314">実稼働環境用から (通常、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-314">Restore the database into your environment with a different name from the production one (typically AXDBupgraded).</span></span>

11. <span data-ttu-id="1fd22-315">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-315">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="1fd22-316">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-316">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="1fd22-317">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-317">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="1fd22-318">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-318">This process may take longer depending on the number of nodes that you have.</span></span>

13. <span data-ttu-id="1fd22-319">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-319">In LCS, go to the Shared Assets Library.</span></span>

14. <span data-ttu-id="1fd22-320">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-320">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

15. <span data-ttu-id="1fd22-321">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-321">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="1fd22-322">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-322">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

16. <span data-ttu-id="1fd22-323">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-323">The database will need to be configured.</span></span> <span data-ttu-id="1fd22-324">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-324">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

17. <span data-ttu-id="1fd22-325">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-325">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="1fd22-326">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-326">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="1fd22-327">配置する場合、指定する必要があるデータベースは手順 15 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-327">When you deploy, the database that you should specify should be the one created in step 15 (typically AXDB).</span></span>

18. <span data-ttu-id="1fd22-328">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-328">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="1fd22-329">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-329">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

19. <span data-ttu-id="1fd22-330">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-330">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

20. <span data-ttu-id="1fd22-331">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-331">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

21. <span data-ttu-id="1fd22-332">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-332">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

22. <span data-ttu-id="1fd22-333">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-333">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="1fd22-334">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="1fd22-334">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="1fd22-335">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-335">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="1fd22-336">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-336">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="1fd22-337">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-337">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="1fd22-338">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-338">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="1fd22-339">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-339">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="1fd22-340">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-340">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="1fd22-341">C:\\D365FFOUpgrade\\ など、任意の展開場所にファイルを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-341">Paste the file wherever you want and unzip it, such as C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="1fd22-342">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-342">Open Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="1fd22-343">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-343">Open a new PowerShell as Administrator and execute:</span></span>

    ```
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="1fd22-344">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-344">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="1fd22-345">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-345">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="1fd22-346">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-346">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="1fd22-347">SQL サーバー 証明書に署名した証明書証明機関を、信頼された Onebox 証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-347">You will need to add the Certificate Authority certificate that signed your SQL server certificate to the Onebox trusted certificate authorities.</span></span> <span data-ttu-id="1fd22-348">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-348">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span> 
    >
    > - <span data-ttu-id="1fd22-349">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-349">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database that you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="1fd22-350">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-350">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="1fd22-351">Onebox で証明機関をインストールする場合、表示されているデータベースに接続するための FQDN または IP を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-351">When you install the Certificate Authority in the Onebox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="1fd22-352">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-352">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="1fd22-353">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-353">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="1fd22-354">a.</span><span class="sxs-lookup"><span data-stu-id="1fd22-354">a.</span></span>  <span data-ttu-id="1fd22-355">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-355">AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml</span></span>

    <span data-ttu-id="1fd22-356">b.</span><span class="sxs-lookup"><span data-stu-id="1fd22-356">b.</span></span>  <span data-ttu-id="1fd22-357">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span><span class="sxs-lookup"><span data-stu-id="1fd22-357">AxUpdateInstaller.exe import -runbookfile=upgrade.xml</span></span>

    <span data-ttu-id="1fd22-358">c.</span><span class="sxs-lookup"><span data-stu-id="1fd22-358">c.</span></span>  <span data-ttu-id="1fd22-359">AxUpdateInstaller.exe execute -runbookid=upgrade</span><span class="sxs-lookup"><span data-stu-id="1fd22-359">AxUpdateInstaller.exe execute -runbookid=upgrade</span></span>

    <span data-ttu-id="1fd22-360">データ アップグレードのクリーンアップの実行中にエラーが発生する可能性があります。スタック トレース: \'カテゴリで\'エラー\'で最初に TTSBEGIN を呼び出さずに TTSCOMMIT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-360">During the execution of Cleanup for data upgrade you may encounter an error: Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.</span></span>

    <span data-ttu-id="1fd22-361">この問題を解決するには、このコマンドを使用して、次の通りにステップを再実行します。AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span><span class="sxs-lookup"><span data-stu-id="1fd22-361">To resolve this issue, re-run the step with this command: AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\></span></span>

9.  <span data-ttu-id="1fd22-362">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-362">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="1fd22-363">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-363">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="1fd22-364">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-364">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="1fd22-365">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-365">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="1fd22-366">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-366">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="1fd22-367">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-367">In LCS, go to the Shared Assets Library.</span></span>

13. <span data-ttu-id="1fd22-368">**資産タイプを選択**では、**モデル**を選択し、Dynamics 365 for Finance and Operations オンプレミス、アプリケーション バージョン 8.1 デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-368">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Application Version 8.1 Demo Data.</span></span>

14. <span data-ttu-id="1fd22-369">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-369">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="1fd22-370">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-370">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

15. <span data-ttu-id="1fd22-371">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-371">The database will need to be configured.</span></span> <span data-ttu-id="1fd22-372">[Finance and Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1fd22-372">Follow the steps in [Configure the Finance and Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance-and-operations-database).</span></span>

16. <span data-ttu-id="1fd22-373">LCS で、新しい環境をセットアップし、それをバージョン 8.1 (再配置) で展開します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-373">In LCS, set up a new environment and deploy it with version 8.1 (Redeploy).</span></span> <span data-ttu-id="1fd22-374">詳細については、[オンプレミス環境での設定と配置](../deployment/setup-deploy-on-premises-pu12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1fd22-374">For more information, see [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="1fd22-375">配置する場合、指定する必要があるデータベースは手順 14 (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-375">When you deploy, the database that you should specify should be the one created in step 14 (typically AXDB).</span></span>

17. <span data-ttu-id="1fd22-376">独自のカスタマイズと同様に ISV/VAR モジュールを、新たに作成された 8.1 環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-376">Apply your own customizations as well as ISV/VAR modules, to your newly created 8.1 environment.</span></span> <span data-ttu-id="1fd22-377">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1fd22-377">Otherwise when the environment initially synchs  with the database it will delete any customization or extensions related data.</span></span>

18. <span data-ttu-id="1fd22-378">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-378">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

19. <span data-ttu-id="1fd22-379">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-379">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

20. <span data-ttu-id="1fd22-380">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-380">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

21. <span data-ttu-id="1fd22-381">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-381">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix-a"></a><span data-ttu-id="1fd22-382">付録 A</span><span class="sxs-lookup"><span data-stu-id="1fd22-382">Appendix A</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="1fd22-383">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="1fd22-383">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="1fd22-384">このスクリプトは、Onebox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="1fd22-384">This script is only meant to be run from a Onebox VHD environment.</span></span>
>
> <span data-ttu-id="1fd22-385">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="1fd22-385">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="1fd22-386">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-386">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="1fd22-387">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-387">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="1fd22-388">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fd22-388">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="1fd22-389">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-389">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="1fd22-390">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="1fd22-390">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="1fd22-391">**-DatabaseServer** - Microsoft Dynamics 365 for Finance and Operations、オンプレミス データベースが含まれているデータベース サーバーです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-391">**-DatabaseServer** - Database server containing Microsoft Dynamics 365 for Finance and Operations, on-premises database.</span></span>

-   <span data-ttu-id="1fd22-392">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="1fd22-392">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="1fd22-393">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="1fd22-393">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="1fd22-394">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-394">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="1fd22-395">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1fd22-395">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="1fd22-396">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="1fd22-396">**Configure-On-Premises-Upgrade.ps1**</span></span>
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

### <a name="troubleshooting"></a><span data-ttu-id="1fd22-397">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1fd22-397">Troubleshooting</span></span>

-   <span data-ttu-id="1fd22-398">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="1fd22-398">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="1fd22-399">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="1fd22-399">The login failed.</span></span> <span data-ttu-id="1fd22-400">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="1fd22-400">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="1fd22-401">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="1fd22-401">Could not establish a connection.</span></span> <span data-ttu-id="1fd22-402">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="1fd22-402">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="1fd22-403">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="1fd22-403">The server was not found or was not accessible.</span></span> <span data-ttu-id="1fd22-404">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fd22-404">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="1fd22-405">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="1fd22-405">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="1fd22-406">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="1fd22-406">Login credentials are not correct.</span></span> <span data-ttu-id="1fd22-407">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="1fd22-407">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>
