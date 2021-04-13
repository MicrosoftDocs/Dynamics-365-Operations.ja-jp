---
title: オンプレミス環境のインプレース アップグレード プロセス
description: このトピックでは、 バージョン 7.x のオンプレミス環境を 10.0.x にアップグレードする詳細なプロセスを説明します。
author: laneswenka
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 10.0.x
ms.openlocfilehash: 40320d19b0e20e8199a2819051b83a3b8dac392e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746033"
---
# <a name="in-place-upgrade-process-for-on-premises-environments"></a><span data-ttu-id="5cd5d-103">オンプレミス環境のインプレース アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="5cd5d-103">In-place upgrade process for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cd5d-104">このトピックでは、 Finance and Operations のオンプレミス環境をバージョン 7.x から 10.0.x にアップグレードする詳細なプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-104">This topic provides the detailed process for upgrading on-premises environments of Finance and Operations from version 7.x to 10.0.x.</span></span>  

> [!NOTE]
> <span data-ttu-id="5cd5d-105">実稼働環境のアップグレードを実行する前に、サンドボックス環境のアップグレードを実行してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-105">Please perform the upgrade with your sandbox environment before upgrading your production environment.</span></span>

## <a name="on-premises-upgrade-from-version-7x-to-100x"></a><span data-ttu-id="5cd5d-106">バージョン7. x から10.0. x へのオンプレミスのアップグレード</span><span class="sxs-lookup"><span data-stu-id="5cd5d-106">On-premises upgrade from version 7.x to 10.0.x</span></span>

> [!NOTE]
> <span data-ttu-id="5cd5d-107">このアップグレード プロセスは完了に時間がかかり、データ アップグレード中はずっと Finance and Operations が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-107">Be aware that this upgrade process takes time to complete and Finance and Operations will be inaccessible for the entire duration of the data upgrade.</span></span>

<span data-ttu-id="5cd5d-108">7.x から 10.0.x にアップグレードするにあたって、現在対応している可能性のある 2 つのパスがあります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-108">To upgrade from version 7.x to 10.0.x, there are two possible paths that are currently supported.</span></span>

<span data-ttu-id="5cd5d-109">各パスの概要は下に記載されています。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-109">An overview of each path is given below:</span></span>

-   <span data-ttu-id="5cd5d-110">**VHD 内からのアップグレード** - このパスは、仮想ハード ディスク (VHD) に、データベースをコピーし、その中のアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-110">**Upgrading from within VHD** - This path involves copying your database into the virtual hard disk (VHD) and executing the upgrade inside it.</span></span> <span data-ttu-id="5cd5d-111">全体的に、この方法はよりシンプルです。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-111">Overall, this is the simpler method.</span></span>

-   <span data-ttu-id="5cd5d-112">**データベースを指す VHD でアップグレード** - このパスは VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-112">**Upgrading with VHD pointing to your database** - This path involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="5cd5d-113">アップグレード プロセスは、VHD 内からも実行されます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-113">The upgrade process is still executed from within the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="5cd5d-114">VHD では、アップグレード プロセスを実行するために外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-114">The VHD does not need external network access in order to carry out the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5cd5d-115">必要条件</span><span class="sxs-lookup"><span data-stu-id="5cd5d-115">Prerequisites</span></span>

1.  <span data-ttu-id="5cd5d-116">Lifecycle Services (LCS) では、共有資産ライブラリ (画面の右側にある) に移動します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-116">In Lifecycle Services (LCS), go to the Shared Assets Library (right side of the screen).</span></span>

2.  <span data-ttu-id="5cd5d-117">**資産タイプの選択** で、**ダウンロード可能な VHD** を選択し、オンプレミス環境でアップグレードする VHD パッケージ全体をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-117">Under **Select asset type**, choose **Downloadable VHD**, and download all parts of the VHD package that closely matches the version you will be upgrading to in your on-premises environment.</span></span> <span data-ttu-id="5cd5d-118">イメージには大量のディスク領域が必要となるため、十分な空き領域のあるドライブにダウンロードして展開してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-118">The image requires a high amount of disk space, so be sure to download and extract on a drive with adequate free space.</span></span> 

3.  <span data-ttu-id="5cd5d-119">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-119">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="5cd5d-120">十分な空き容量が確保されている場所にに VHD を展開してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-120">Extract the VHD to a location with a good amount of free space.</span></span>

4.  <span data-ttu-id="5cd5d-121">Hyper-V を使用して、仮想マシン (VM) を起動し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-121">Using Hyper-V, launch a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="5cd5d-122">(マシンはジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="5cd5d-122">(Note that the machine must be Generation 1.)</span></span>

5.  <span data-ttu-id="5cd5d-123">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-123">Connect to the VM.</span></span> <span data-ttu-id="5cd5d-124">資格情報を[仮想マシン (VM) をローカルで実行](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally)から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-124">You can find the credentials in [Running the Virtual Machine (VM) locally](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/access-instances#running-the-virtual-machine-vm-locally).</span></span>

6.  <span data-ttu-id="5cd5d-125">オンプレミスで予定されている 10.0.x のターゲット バージョンとダウンロードした VHD イメージによっては、 **アセットタイプの選択** と **ソフトウェアで展開可能なパッケージ** 配下にある共有アセット ライブラリから必要なアプリケーションとプラットフォーム更新プログラムをダウンロードして適用することが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-125">Depending on your planned on-premises target version of 10.0.x and the VHD image you downloaded, you may need to download and apply the required Application and Platform Update from the Shared Asset Library under **Select asset type** and **Software deployable package**.</span></span> <span data-ttu-id="5cd5d-126">詳細な情報については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-126">For more information, see [Install deployable packages from the command line](../deployment/install-deployable-package.md).</span></span>

7.  <span data-ttu-id="5cd5d-127">拡張機能やカスタマイズを VHD にインストールしている場合は、アップグレード プロセスによって、カスタマイズに関連するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-127">If you have any extensions or customizations install them into the VHD now, otherwise the upgrade process will remove any data related to customizations.</span></span> <span data-ttu-id="5cd5d-128">アップグレード前に、環境を準備する必要がある場合は、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-128">Check with your independent software vendor (ISV) or value-added reseller (VAR) if you need to prepare your environment before the upgrade.</span></span>

### <a name="upgrading-from-within-vhd"></a><span data-ttu-id="5cd5d-129">VHD 内からのアップグレード</span><span class="sxs-lookup"><span data-stu-id="5cd5d-129">Upgrading from within VHD</span></span>

1.  <span data-ttu-id="5cd5d-130">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または各ノードで Service Fabric Host Service を停止し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-130">Shut-down on-premises AOS, BI, and MR servers or stop the Service Fabric Host Service in each of the nodes and set to disabled.</span></span>

2.  <span data-ttu-id="5cd5d-131">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-131">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="5cd5d-132">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-132">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="5cd5d-133">VHD で C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-133">In the VHD, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

4.  <span data-ttu-id="5cd5d-134">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-134">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="5cd5d-135">たとえば、c:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-135">For example: c:\\D365FFOUpgrade\\</span></span>

5.  <span data-ttu-id="5cd5d-136">管理者としてコマンド プロンプトを開き、手順 4 で展開していないフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-136">Open a Command Prompt as Administrator and change the directory to the unzipped folder in step 4.</span></span>

6.  <span data-ttu-id="5cd5d-137">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-137">Restore the backup that you created into the OneBox VM.</span></span> <span data-ttu-id="5cd5d-138">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-138">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

7.  <span data-ttu-id="5cd5d-139">オプション: 復元したデータベースの名前が AXDB ではない場合は、管理者権限を持つ PowerShell を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-139">Optional: If the name of your restored database is not AXDB, using PowerShell with administrator privileges, execute:</span></span>
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```
    > [!NOTE] 
    > <span data-ttu-id="5cd5d-140">(たとえば、AXDB などの) 適切な値に <DB-Name> を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-140">Substitute <DB-Name> with the appropriate value in your case (for example, AXDB).</span></span> <span data-ttu-id="5cd5d-141">値をさらに編集する場合は、このトピックの付録を参照します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-141">If you would like to edit more values, refer to the appendix of this topic.</span></span>

    <span data-ttu-id="5cd5d-142">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-142">The script will run a database connection test to check that the information you provide is valid.</span></span>

8.  <span data-ttu-id="5cd5d-143">手順 5 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-143">Using the Command Prompt from step 5, execute the following commands:</span></span>

    <span data-ttu-id="5cd5d-144">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-144">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="5cd5d-145">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-145">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="5cd5d-146">c.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-146">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="5cd5d-147">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-147">During the execution of cleanup for data upgrade you may encounter an error:</span></span> 
    
    `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`
    
    <span data-ttu-id="5cd5d-148">これを解決するには、次のコマンドのステップを再実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-148">To resolve this, re-run the step with this command:</span></span> 
    
    `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`

9.  <span data-ttu-id="5cd5d-149">アップグレード プロセスが正常に完了したら、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-149">When the upgrade process has finished successfully, back up the newly upgraded database.</span></span> <span data-ttu-id="5cd5d-150">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-150">If you have customizations from ISVs or VARs, check if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="5cd5d-151">実稼働環境用から (たとえば、AXDBupgraded など) 別の名前を使用して環境に、データベースを復元します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-151">Restore the database into your environment with a different name from the production one (for example, AXDBupgraded).</span></span>

11. <span data-ttu-id="5cd5d-152">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-152">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

12. <span data-ttu-id="5cd5d-153">LCS でプロジェクトを開き、**環境** セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-153">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="5cd5d-154">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-154">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="5cd5d-155">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-155">This process may take longer depending on the number of nodes that you have.</span></span> <span data-ttu-id="5cd5d-156">新しい環境を配置する前に、Service Fabric Explorer を確認し、すべての申請が削除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-156">Check the service fabric explorer to verify that all applications have been deleted before deploying a new environment.</span></span> <span data-ttu-id="5cd5d-157">実際のプロセスが完了する前に、LCS では環境が削除されていることを示す場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-157">Note that LCS might indicate that the environment is deleted before the actual process is finished.</span></span>

13. <span data-ttu-id="5cd5d-158">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-158">If you had customizations:</span></span>

    <span data-ttu-id="5cd5d-159">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-159">a.</span></span>  <span data-ttu-id="5cd5d-160">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-160">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="5cd5d-161">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-161">b.</span></span>  <span data-ttu-id="5cd5d-162">**資産タイプを選択** 配下で、**モデル** を選択し、Dynamics 365 for Finance and Operations オンプレミスのバージョン 10.0.x デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-162">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Version 10.0.x Demo Data.</span></span> <span data-ttu-id="5cd5d-163">設置型のベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-163">Select the version closest to the 10.0.x environment that you will deploy as the on-premises baseline.</span></span>

    <span data-ttu-id="5cd5d-164">c.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-164">c.</span></span>  <span data-ttu-id="5cd5d-165">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-165">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="5cd5d-166">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-166">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
     
    <span data-ttu-id="5cd5d-167">d.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-167">d.</span></span>  <span data-ttu-id="5cd5d-168">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-168">The database will need to be configured.</span></span> <span data-ttu-id="5cd5d-169">[Finance and Operations データベースのコンフィギュレーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-169">Follow the steps in [Configure the Finance and Operations database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configure-the-finance-and-operations-database).</span></span>

    <span data-ttu-id="5cd5d-170">e.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-170">e.</span></span>  <span data-ttu-id="5cd5d-171">LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-171">In LCS, set up a new environment and deploy it with version 10.0.x (Redeploy).</span></span> <span data-ttu-id="5cd5d-172">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-172">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="5cd5d-173">配置する場合、指定するデータベースは手順 13 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-173">When you deploy, the database that you specify should be the one created in step 13c (typically AXDB).</span></span>

    <span data-ttu-id="5cd5d-174">f.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-174">f.</span></span>  <span data-ttu-id="5cd5d-175">新たに作成した 10.0.x 環境にカスタマイズを適用し、 ISV/VAR モジュールにも適用します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-175">Apply your own customizations as well as ISV/VAR modules, to your newly created 10.0.x environment.</span></span> <span data-ttu-id="5cd5d-176">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-176">Otherwise, when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="5cd5d-177">g.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-177">g.</span></span>  <span data-ttu-id="5cd5d-178">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-178">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="5cd5d-179">h.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-179">h.</span></span>  <span data-ttu-id="5cd5d-180">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-180">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name that the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="5cd5d-181">i.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-181">i.</span></span>  <span data-ttu-id="5cd5d-182">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-182">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

14. <span data-ttu-id="5cd5d-183">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-183">If you didn't have customizations:</span></span>

    <span data-ttu-id="5cd5d-184">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-184">a.</span></span>  <span data-ttu-id="5cd5d-185">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-185">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="5cd5d-186">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-186">Make sure that in the next step you input the name of the upgraded DB.</span></span>

    <span data-ttu-id="5cd5d-187">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-187">b.</span></span>  <span data-ttu-id="5cd5d-188">LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-188">In LCS, set up a new environment and deploy it with version 10.0.x (Redeploy).</span></span> <span data-ttu-id="5cd5d-189">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-189">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

15. <span data-ttu-id="5cd5d-190">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-190">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

### <a name="upgrading-with-vhd-pointing-to-your-database"></a><span data-ttu-id="5cd5d-191">データベースを指す VHD でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="5cd5d-191">Upgrading with VHD pointing to your database</span></span>

1.  <span data-ttu-id="5cd5d-192">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-192">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

2.  <span data-ttu-id="5cd5d-193">オンプレミス環境 (通常は AXDB) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-193">Back up your database from your on-premises environment (typically AXDB).</span></span> <span data-ttu-id="5cd5d-194">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-194">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017).</span></span>

3.  <span data-ttu-id="5cd5d-195">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (AXDBtoupgrade) を付けます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-195">Restore the backup that you just created into the database server and give it a different name (AXDBtoupgrade).</span></span> <span data-ttu-id="5cd5d-196">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-196">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

4.  <span data-ttu-id="5cd5d-197">接続されたら、C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage に移動し、MinorVersionDataUpgrade zip ファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-197">Once connected, go to C:\\AOSService\\PackagesLocalDirectory\\Bin\\CustomDeployablePackage and copy the MinorVersionDataUpgrade zip file.</span></span>

5.  <span data-ttu-id="5cd5d-198">任意の場所にファイルを貼り付け、展開します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-198">Paste the file wherever you want and unzip it.</span></span> <span data-ttu-id="5cd5d-199">たとえば、C:\\D365FFOUpgrade\\ です。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-199">For example: C:\\D365FFOUpgrade\\</span></span>

6.  <span data-ttu-id="5cd5d-200">管理者としてコマンド プロンプトを開き、手順 5 で展開したフォルダーへディレクトリを変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-200">Open a Command Prompt as Administrator and change the directory to the unzipped folder from step 5.</span></span>

7.  <span data-ttu-id="5cd5d-201">管理者として新しい PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-201">Open a new PowerShell as Administrator and execute:</span></span>
    
    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > <span data-ttu-id="5cd5d-202">\<\*\> を必要な値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-202">Substitute \<\*\> with the values you require.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="5cd5d-203">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-203">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="5cd5d-204">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-204">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2017).</span></span>
    >
    > - <span data-ttu-id="5cd5d-205">SQL Server 証明書に署名した証明書を、 OneBox の信頼された証明機関に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-205">You will need to add the Certificate Authority certificate that signed your SQL Server certificate to the OneBox trusted certificate authorities.</span></span> <span data-ttu-id="5cd5d-206">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-206">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    >
    > - <span data-ttu-id="5cd5d-207">使用するデータベースのユーザーに、sysadmin サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくともすべての特権があり、tempDB にアクセスする許可があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-207">Make sure the database user you use has the sysadmin server role assigned or at least All Privileges on the database you want to upgrade and has permissions to access tempDB.</span></span> <span data-ttu-id="5cd5d-208">これが該当しない場合は、アップグレード プロセスの手順 6 で失敗します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-208">Step 6 of the upgrade process will fail if this is not true.</span></span>
    >
    > - <span data-ttu-id="5cd5d-209">Onebox で証明機関をインストールする場合、FQDN または IP を使用して表示されているデータベースに接続することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-209">When you install the Certificate Authority in the OneBox, make sure you use the FQDN or IP for connecting to the database that appears there.</span></span> <span data-ttu-id="5cd5d-210">そのサーバーを指していないため、データベースにドメイン名を使用してアクセスできない場合は、ホスト ファイルを編集して、DN を追加し、解決する必要がある IP 追加します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-210">If you can't access it by using the domain name because it doesn't point to that server, edit your hosts file and add the DN and the IP it should resolve to.</span></span>

8.  <span data-ttu-id="5cd5d-211">手順 6 からコマンド プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-211">Using the Command Prompt from step 6, execute the following commands:</span></span>

    <span data-ttu-id="5cd5d-212">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-212">a.</span></span>  `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`

    <span data-ttu-id="5cd5d-213">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-213">b.</span></span>  `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`

    <span data-ttu-id="5cd5d-214">c.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-214">c.</span></span>  `AxUpdateInstaller.exe execute -runbookid=upgrade`

    <span data-ttu-id="5cd5d-215">データ アップグレードのクリーンアップの実行中に、エラーが発生する場合があります: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span><span class="sxs-lookup"><span data-stu-id="5cd5d-215">During the execution of Cleanup for data upgrade you may encounter an error: `Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.\' on category \'Error\'.`</span></span>

    <span data-ttu-id="5cd5d-216">これを解決するには、次のコマンドのステップを再実行します: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span><span class="sxs-lookup"><span data-stu-id="5cd5d-216">To resolve this, re-run the step with this command: `AxUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=\<failed-step\>`</span></span>

9.  <span data-ttu-id="5cd5d-217">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-217">If you have customizations from ISVs or VARs, verify if you have to run some post data upgrade scripts.</span></span>

10. <span data-ttu-id="5cd5d-218">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-218">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

11. <span data-ttu-id="5cd5d-219">LCS でプロジェクトを開き、**環境** セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-219">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span> <span data-ttu-id="5cd5d-220">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-220">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="5cd5d-221">このプロセスは、持っているノードの数に応じて、時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-221">This process may take longer depending on the number of nodes you have.</span></span>

12. <span data-ttu-id="5cd5d-222">カスタマイズする場合、次の事項を行います。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-222">If you had customizations:</span></span>

    <span data-ttu-id="5cd5d-223">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-223">a.</span></span>  <span data-ttu-id="5cd5d-224">LCS では、共有資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-224">In LCS, go to the Shared Assets Library.</span></span>

    <span data-ttu-id="5cd5d-225">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-225">b.</span></span>  <span data-ttu-id="5cd5d-226">**資産タイプを選択** 配下で、**モデル** を選択し、Dynamics 365 for Finance and Operations オンプレミスのバージョン 10.0.x デモ データをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-226">Under **Select asset type**, choose **Model** and download: Dynamics 365 for Finance and Operations on-premises, Version 10.0.x Demo Data.</span></span> <span data-ttu-id="5cd5d-227">設置型のベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-227">Select the version closest to the 10.0.x environment that you will deploy as the on-premises baseline.</span></span>

    <span data-ttu-id="5cd5d-228">c.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-228">c.</span></span>  <span data-ttu-id="5cd5d-229">SQL serverから復元バックアップ オプションを使用して、新しいデータベース (通常はAXDB) を作成するのにには、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-229">Use this file to create a new database (typically AXDB) using the restore backup option from SQL server.</span></span> <span data-ttu-id="5cd5d-230">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-230">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>

    <span data-ttu-id="5cd5d-231">d.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-231">d.</span></span>  <span data-ttu-id="5cd5d-232">データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-232">The database will need to be configured.</span></span> <span data-ttu-id="5cd5d-233">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-233">Follow the steps under [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>

    <span data-ttu-id="5cd5d-234">e.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-234">e.</span></span>  <span data-ttu-id="5cd5d-235">LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-235">In LCS, set up a new environment and deploy it with version 10.0.x (Redeploy).</span></span> <span data-ttu-id="5cd5d-236">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-236">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="5cd5d-237">配置する場合、指定する必要があるデータベースは手順 12 c (通常は AXDB) で作成したものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-237">When you deploy, the database that you should specify should be the one created in step 12c (typically AXDB).</span></span>

    <span data-ttu-id="5cd5d-238">f.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-238">f.</span></span>  <span data-ttu-id="5cd5d-239">新たに作成した 10.0.x 環境にカスタマイズを適用し、 ISV/VAR モジュールにも適用します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-239">Apply your own customizations as well as ISV/VAR modules, to your newly created 10.0.x environment.</span></span> <span data-ttu-id="5cd5d-240">それ以外の場合、この環境が最初にデータベースと同期される時に、カスタマイズまたは拡張機能の関連データが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-240">Otherwise when the environment initially syncs with the database it will delete any customization or extensions related data.</span></span>

    <span data-ttu-id="5cd5d-241">g.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-241">g.</span></span>  <span data-ttu-id="5cd5d-242">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-242">Shut-down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>

    <span data-ttu-id="5cd5d-243">h.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-243">h.</span></span>  <span data-ttu-id="5cd5d-244">名前を変更するか、配置で使用されるデモ データベース (通常は AXDB) を削除して、新しいデータベース (通常は AXDBupgraded) の名前を、デモ データベースにあった名前 (通常は AXDB) に変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-244">Rename or delete the demo database (typically AXDB) used in the deploy and then rename your new database (typically AXDBupgraded) to the name the demo database had (typically AXDB).</span></span>

    <span data-ttu-id="5cd5d-245">i.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-245">i.</span></span>  <span data-ttu-id="5cd5d-246">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-246">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

13. <span data-ttu-id="5cd5d-247">カスタマイズを持っていない場合は、次の事項を実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-247">If you didn't have customizations:</span></span>

    <span data-ttu-id="5cd5d-248">a.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-248">a.</span></span>  <span data-ttu-id="5cd5d-249">(省略可) 既存のデータベース (通常は AXDBold) の名前を変更し、新しいデータベース (通常は AXDB) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-249">(Optional) Rename your old database (typically AXDBold) and then rename your new database (typically AXDB).</span></span> <span data-ttu-id="5cd5d-250">次の手順で、アップグレードされたデータベースの名前を入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-250">Make sure that in the next step you input the name of the upgraded database.</span></span>

    <span data-ttu-id="5cd5d-251">b.</span><span class="sxs-lookup"><span data-stu-id="5cd5d-251">b.</span></span>  <span data-ttu-id="5cd5d-252">新しい環境を設定し、バージョン 10.0.x で配置します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-252">Set up a new environment and deploy it with version 10.0.x.</span></span> <span data-ttu-id="5cd5d-253">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-253">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

14. <span data-ttu-id="5cd5d-254">(省略可) 新しい環境 (通常 AXDB) を使用しているデータベースでの財務レポート モジュールが失敗したために配置が失敗した場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-254">(Optional) If deployment fails because the financial reporting module failed, on the database that you are using for the new environment (typically AXDB), run the following command:</span></span>

    ```sql
    ALTER TABLE RETAILTERMINALTABLE ADD CONSTRAINT PK_RecId PRIMARY KEY
    CLUSTERED (RECID)
    ```

## <a name="appendix"></a><span data-ttu-id="5cd5d-255">付録</span><span class="sxs-lookup"><span data-stu-id="5cd5d-255">Appendix</span></span>

### <a name="configure-on-premises-upgradeps1-usage"></a><span data-ttu-id="5cd5d-256">Configure-On-Premises-Upgrade.ps1 の使用状況</span><span class="sxs-lookup"><span data-stu-id="5cd5d-256">Configure-On-Premises-Upgrade.ps1 usage</span></span>

> [!Important]
> <span data-ttu-id="5cd5d-257">このスクリプトは、OneBox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-257">This script is only meant to be run from a OneBox VHD environment.</span></span>
>
> <span data-ttu-id="5cd5d-258">スクリプトは、少なくとも DatabaseName パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-258">The script requires that you pass at least the DatabaseName parameter.</span></span> <span data-ttu-id="5cd5d-259">渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-259">If you don't pass it, the script will automatically request it.</span></span>

<span data-ttu-id="5cd5d-260">DatabaseServer または DatabaseUser のような追加のパラメーターを渡す場合は、これを行うことができますが、スクリプトはすべての追加のパラメータを要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-260">If you want to pass an additional parameter like DatabaseServer, or DatabaseUser you can do so but this will cause the script to ask you for all additional parameters.</span></span> <span data-ttu-id="5cd5d-261">これは、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するため起こりますが、これらのパラメーターは、正しく接続を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-261">This happens because the script will assume that you want to point the database connection to a machine outside the VM and those parameters will be required to correctly establish the connection.</span></span>

<span data-ttu-id="5cd5d-262">スクリプトに渡することができるパラメーターは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-262">The parameters that can be passed to the script are:</span></span>

-   <span data-ttu-id="5cd5d-263">**-DatabaseName** - アップグレードするデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-263">**-DatabaseName** - Database name that you want to upgrade.</span></span>

-   <span data-ttu-id="5cd5d-264">**-DatabaseServer** - Finance and Operations (オンプレミス) データベースが含まれているデータベース サーバーです。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-264">**-DatabaseServer** - Database server containing Finance and Operations (on-premises) database.</span></span>

-   <span data-ttu-id="5cd5d-265">**-DatabaseUser** - SQL 認証のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-265">**-DatabaseUser** - Username for SQL Authentication.</span></span>

-   <span data-ttu-id="5cd5d-266">**-DatabasePassword** - SQL 認証のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-266">**-DatabasePassword** - Password for SQL Authentication.</span></span>

<span data-ttu-id="5cd5d-267">コンフィギュレーションが渡された後に、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-267">After configuration has been passed, the script will execute a database connection test with the new parameters.</span></span> <span data-ttu-id="5cd5d-268">スクリプトが接続されない場合は、Microsoft SQL Server Management Studio を使用するか、またはその他のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-268">If the script is unable to connect we recommend that you use Microsoft SQL Server Management Studio or some other tool to debug the connection from there.</span></span>

<span data-ttu-id="5cd5d-269">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="5cd5d-269">**Configure-On-Premises-Upgrade.ps1**</span></span>

```powershell
<#
.Synopsis
   Configures a Onebox deployment to upgrade an OnPrem 7.x database to OnPrem 10.0.x 

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

### <a name="troubleshooting"></a><span data-ttu-id="5cd5d-270">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5cd5d-270">Troubleshooting</span></span>

-   <span data-ttu-id="5cd5d-271">データベース名が間違っているまたはユーザーがそのデータベースにアクセスできない場合は、例外を呼び出します。\"0\" 引数で\"開きます\"。\"ログインによって要求されたデータベース \"AxDB1\" を開くことができません。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-271">Wrong database name or user doesn't have access to that database: Exception calling \"Open\" with \"0\" argument(s): \"Cannot open database \"AxDB1\" requested by the login.</span></span> <span data-ttu-id="5cd5d-272">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-272">The login failed.</span></span> <span data-ttu-id="5cd5d-273">ユーザー、\'axdbadmin\'.\" のログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-273">Login failed for user \'axdbadmin\'.\"</span></span>

-   <span data-ttu-id="5cd5d-274">接続が確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-274">Could not establish a connection.</span></span> <span data-ttu-id="5cd5d-275">Ip/fqdn とポートを確認します。例外を呼び出します。\"0\" 引数で\"開きます\"。\"SQL Server への接続を確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-275">Check ip/fqdn and ports: Exception calling \"Open\" with \"0\" argument(s): \"A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="5cd5d-276">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-276">The server was not found or was not accessible.</span></span> <span data-ttu-id="5cd5d-277">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-277">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="5cd5d-278">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした)\"</span><span class="sxs-lookup"><span data-stu-id="5cd5d-278">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)\"</span></span>

-   <span data-ttu-id="5cd5d-279">ログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="5cd5d-279">Login credentials are not correct.</span></span> <span data-ttu-id="5cd5d-280">例外 の呼び出し: \"0\" 引数で\"開きます\"。\"ユーザー \'axdbadmin\' のログインが失敗しました。\"</span><span class="sxs-lookup"><span data-stu-id="5cd5d-280">Exception calling \"Open\" with \"0\" argument(s): \"Login failed for user \'axdbadmin\'.\"</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]