---
title: Dynamics 365 Finance + Operations (オンプレミス) への AX 2012 のデータ アップグレード プロセス
description: このトピックでは、Microsoft Dynamics AX 2012 データベースを Dynamics 365 Finance  + Operations (オンプレミス) 10.0.X にアップグレードするプロセスについて説明します。
author: faix
manager: AnnBe
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 25ca380d0af7b88da56a1bc74654962c110a9ca2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503007"
---
# <a name="data-upgrade-process-for-ax-2012-to-dynamics-365-finance--operations-on-premises"></a><span data-ttu-id="28f0c-103">Dynamics 365 Finance + Operations (オンプレミス) への AX 2012 のデータ アップグレード プロセス</span><span class="sxs-lookup"><span data-stu-id="28f0c-103">Data upgrade process for AX 2012 to Dynamics 365 Finance + Operations (on-premises)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28f0c-104">このトピックでは、Microsoft Dynamics AX 2012 データベースを Dynamics 365 Finance  + Operations (オンプレミス) 10.0.X にアップグレードするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-104">This topic describes the process for upgrading Microsoft Dynamics AX 2012 databases to Dynamics 365 Finance + Operations (on-premises) version 10.0.x.</span></span> <span data-ttu-id="28f0c-105">現在、Dynamics AX 2012 R2 または Dynamics AX 2012 R3 のいずれかからのアップグレードのみ、サポートされています。</span><span class="sxs-lookup"><span data-stu-id="28f0c-105">Currently, upgrade is supported only from either Dynamics AX 2012 R2 or Dynamics AX 2012 R3.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="28f0c-106">このトピックでは、データ アップグレードを行う手順についてのみ説明します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-106">This topic explains the process for doing a data upgrade only.</span></span> <span data-ttu-id="28f0c-107">コード アップグレードを実行する方法の詳細については、クラウド バージョンで使用可能なアップグレード ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-107">For information about how to do a code upgrade, see the upgrade guides that are available for cloud versions.</span></span> <span data-ttu-id="28f0c-108">コード アップグレード ツールは、Microsoft Dynamics Lifecycle Services (LCS) を介してのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="28f0c-108">The code upgrade tooling is available only through Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="ax-2012-upgrade-to-dynamics-365-finance--operations-on-premises"></a><span data-ttu-id="28f0c-109">AX 2012 を Dynamics 365 Finance + Operations (オンプレミス) にアップグレードする</span><span class="sxs-lookup"><span data-stu-id="28f0c-109">AX 2012 upgrade to Dynamics 365 Finance + Operations (on-premises)</span></span>

<span data-ttu-id="28f0c-110">現在、サポートされているアップグレード方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-110">Two upgrade methods are currently supported:</span></span>

- <span data-ttu-id="28f0c-111">**VHD 内からのアップグレード** – この方法では、データベースを仮想ハード ディスク (VHD) にコピーし、VHD 内からアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-111">**Upgrade from inside the VHD** – This method involves copying your database into the virtual hard disk (VHD) and running the upgrade from inside the VHD.</span></span> <span data-ttu-id="28f0c-112">全体的に、この方法は簡単です。</span><span class="sxs-lookup"><span data-stu-id="28f0c-112">Overall, this method is easier.</span></span>
- <span data-ttu-id="28f0c-113">**データベースを指す VHD でアップグレード** – この方法は、VHD アップグレード プロセスをデータベースにポイントします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-113">**Upgrade where the VHD points to your database** – This method involves pointing the VHD upgrade process to your database.</span></span> <span data-ttu-id="28f0c-114">アップグレード プロセスは、VHD 内から実行されます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-114">The upgrade process is still run from inside the VHD.</span></span>

> [!NOTE]
> <span data-ttu-id="28f0c-115">VHDがアップグレード プロセスを実行するのに、外部のネットワーク アクセス権は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-115">The VHD doesn't require external network access to run the upgrade process.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="28f0c-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="28f0c-116">Prerequisites</span></span>

1. <span data-ttu-id="28f0c-117">[LCS トライアルまたはパートナー プロジェクトにサインアップ](upgrade-overview-2012.md#sign-up-for-a-lifecycle-services-trial-or-partner-project) します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-117">[Sign up for an LCS trial or partner project](upgrade-overview-2012.md#sign-up-for-a-lifecycle-services-trial-or-partner-project).</span></span>
1. <span data-ttu-id="28f0c-118">各 AX 2012 リリースについては、Finance + Operations アプリケーションの最新リリースにアップグレードする前に、利用可能な最新の累積更新プログラムに更新します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-118">For each AX 2012 release, update to the most recent cumulative update that is available before you upgrade to the most recent Finance + Operations application release.</span></span>
1. <span data-ttu-id="28f0c-119">アップグレード前のチェックリストをインストールします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-119">Install the pre-upgrade checklist.</span></span> <span data-ttu-id="28f0c-120">詳細については、[インストール](prepare-data-upgrade.md#installation) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-120">For more information, see [Installation](prepare-data-upgrade.md#installation).</span></span>
1. <span data-ttu-id="28f0c-121">データ アップグレードの準備手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-121">Go through the data upgrade preparation steps.</span></span> <span data-ttu-id="28f0c-122">「ユーザー マッピングの設定」の手順はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-122">You can skip the "Set up user mapping" step.</span></span> <span data-ttu-id="28f0c-123">この手順は、クラウドでホストされているアップグレードのみ関連しています。</span><span class="sxs-lookup"><span data-stu-id="28f0c-123">This step is relevant only for cloud-hosted upgrades.</span></span>
1. <span data-ttu-id="28f0c-124">データベースのバックアップを作成します (MicrosoftDynamicsAX)。</span><span class="sxs-lookup"><span data-stu-id="28f0c-124">Make a backup of your database (MicrosoftDynamicsAX).</span></span> <span data-ttu-id="28f0c-125">詳細については、「[フル データベース バックアップの作成](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-125">For more information, see [Create a Full Database Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016).</span></span>
1. <span data-ttu-id="28f0c-126">LCS で、ページの右側にあるタイルを選択して、共有アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-126">In LCS, go to the Shared asset library by selecting the tile on the right side of the page.</span></span> <span data-ttu-id="28f0c-127">**資産タイプの選択**の下の**ダウンロード可能な VHD** を選択し、オンプレミス環境でアップグレードするバージョンに最も適合する VHD パッケージ全体をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-127">Then, under **Select asset type**, select **Downloadable VHD**, and download all parts of the VHD package that most closely matches the version that you will upgrade to in your on-premises environment.</span></span> <span data-ttu-id="28f0c-128">画像は大量のディスク容量を必要とします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-128">The image requires a large amount of disk space.</span></span> <span data-ttu-id="28f0c-129">したがって、十分な空き領域のあるドライブでパッケージをダウンロードし、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-129">Therefore, be sure to download and extract the package on a drive that has enough free space.</span></span> 
1. <span data-ttu-id="28f0c-130">ダウンロードしたファイルは、自己展開する zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="28f0c-130">The files that you downloaded are a self-extracting zip file.</span></span> <span data-ttu-id="28f0c-131">十分な空き容量が確保されている場所に VHD を展開してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-131">Extract the VHD to a location that has a good amount of free space.</span></span>
1. <span data-ttu-id="28f0c-132">Hyper-V を使用して、仮想マシン (VM) を開始し、VHD を接続します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-132">Use Hyper-V to start a virtual machine (VM) and attach the VHD.</span></span> <span data-ttu-id="28f0c-133">(VM はジェネレーション 1 である必要があります。)</span><span class="sxs-lookup"><span data-stu-id="28f0c-133">(Note that the VM must be Generation 1.)</span></span>
1. <span data-ttu-id="28f0c-134">VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-134">Connect to the VM.</span></span> <span data-ttu-id="28f0c-135">資格情報の詳細については、[ローカルで仮想マシン (VM) を実行する](../dev-tools/access-instances.md#running-the-virtual-machine-locally) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-135">For information about the credentials, see [Running the Virtual Machine (VM) locally](../dev-tools/access-instances.md#running-the-virtual-machine-locally).</span></span>
1. <span data-ttu-id="28f0c-136">オンプレミスで予定されている 10.0.x のターゲット バージョンとダウンロードした VHD イメージによっては、 共有アセット ライブラリから必要なアプリケーション更新プログラムとプラットフォーム更新プログラムをダウンロードして適用することが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-136">Depending on your planned on-premises target version of 10.0.x and the VHD image that you downloaded, you might have to download and apply the required application update and platform update from the Shared asset library.</span></span> <span data-ttu-id="28f0c-137">**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-137">Under **Select asset type**, select **Software deployable package**.</span></span> <span data-ttu-id="28f0c-138">詳細な情報については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-138">For more information, see [Install deployable packages from the command line](../deployment/install-deployable-package.md).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="28f0c-139">いずれの場合でも、最新の品質更新プログラムが VHD に適用されていることを確認し、データ アップグレードを実行するための最新の修正プログラムが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-139">In any case, make sure that you've applied the most recent quality update to your VHD, to ensure that it contains the most recent fixes for doing data upgrades.</span></span> 

1. <span data-ttu-id="28f0c-140">拡張機能またはカスタマイズがある場合、今 VHD にインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-140">If you have any extensions or customizations, install them on the VHD now.</span></span> <span data-ttu-id="28f0c-141">それ以外の場合、アップグレード プロセスは、カスタマイズに関連するデータをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-141">Otherwise, the upgrade process will remove any data that is related to customizations.</span></span> <span data-ttu-id="28f0c-142">アップグレードの前に、環境を準備する必要がある場合、独立系ソフトウェア ベンダー (ISV) または付加価値再販業者 (VAR) に確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-142">If you must prepare your environment before the upgrade, check with your independent software vendor (ISV) or value-added reseller (VAR).</span></span>

### <a name="upgrade-from-inside-the-vhd"></a><span data-ttu-id="28f0c-143">VHD 内からアップグレードする</span><span class="sxs-lookup"><span data-stu-id="28f0c-143">Upgrade from inside the VHD</span></span>

1. <span data-ttu-id="28f0c-144">Onebox VM に作成したバックアップを復元します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-144">Restore the backup that you created to the OneBox VM.</span></span> <span data-ttu-id="28f0c-145">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-145">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016).</span></span>
1. <span data-ttu-id="28f0c-146">オプション: 復元したデータベースの名前が **axdb** でない場合、管理者として Windows PowerShell を開き、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-146">Optional: If the name of your restored database isn't **AXDB**, open Windows PowerShell as an administrator, and run the following script.</span></span>

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>'
    ```

    > [!NOTE] 
    > <span data-ttu-id="28f0c-147">**\<DB-name\>** をデータベースの名前 (**AXDB** など) で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-147">Replace **\<DB-name\>** with the name of your database (for example, **AXDB**).</span></span> <span data-ttu-id="28f0c-148">多くの値を編集する場合、このトピックの [付録](#appendix) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-148">If you want to edit more values, see the [appendix](#appendix) later in this topic.</span></span>

    <span data-ttu-id="28f0c-149">スクリプトは、データベース接続のテストを実行し、入力した情報が有効であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-149">The script will run a database connection test to verify that the information that you provided is valid.</span></span>

1. <span data-ttu-id="28f0c-150">LCS では、共有アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-150">In LCS, go to the Shared asset library.</span></span> <span data-ttu-id="28f0c-151">**アセット タイプの選択**で**ソフトウェア配置可能パッケージ**を選択し、**AX2012DataUpgrade-10-0-8** を選択して、**MajorVersionDataUpgrade.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-151">Under **Select asset type**, select **Software deployable package**, and then select **AX2012DataUpgrade-10-0-8** to download the **MajorVersionDataUpgrade.zip** file.</span></span>
1. <span data-ttu-id="28f0c-152">ファイルをコピーして目的の場所に貼り付け (**c:\\D365FFOUpgrade\\** など)、展開します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-152">Copy the file, paste it in the desired location (for example: **c:\\D365FFOUpgrade\\**), and unzip it.</span></span>
1. <span data-ttu-id="28f0c-153">管理者としてコマンド プロンプト ウィンドウを開き、展開したフォルダーへディレクトリを変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-153">Open a Command Prompt window as an administrator, change the directory to the folder that you just unzipped, and run the following commands.</span></span>

    1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`
    2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`
    3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

1. <span data-ttu-id="28f0c-154">アップグレード プロセスが正常に完了した後、新たにアップグレードしたデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-154">After the upgrade process is successfully completed, back up the newly upgraded database.</span></span> <span data-ttu-id="28f0c-155">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-155">If you have customizations from ISVs or VARs, check whether you must run some post–data upgrade scripts.</span></span>
1. <span data-ttu-id="28f0c-156">データベースをオンプレミス環境の SQL Server に復元し、AX 2012 データベースの名前とは異なる名前 (**AXDBupgraded** など) を付けます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-156">Restore the database into your on-premises environment's SQL Server, but give it a name that differs from the name of the AX 2012 database (for example, name it **AXDBupgraded**).</span></span> <span data-ttu-id="28f0c-157">復元したデータベースはコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-157">The restored database must be configured.</span></span> <span data-ttu-id="28f0c-158">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-158">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>
1. <span data-ttu-id="28f0c-159">新しい Dynamics 365 Finance + Operations (オンプレミス) 環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-159">Deploy a new Dynamics 365 Finance + Operations (on-premises) environment.</span></span>

    - <span data-ttu-id="28f0c-160">カスタマイズがある場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-160">If you have customizations, follow these steps:</span></span>

        1. <span data-ttu-id="28f0c-161">LCS では、共有アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-161">In LCS, go to the Shared asset library.</span></span>
        1. <span data-ttu-id="28f0c-162">**資産タイプの選択**の下で、**モデル**を選択し、**Dynamics 365 Finance + Operations オンプレミスのバージョン 10.0.x デモ データ**をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-162">Under **Select asset type**, select **Model**, and then download **Dynamics 365 Finance + Operations on-premises, Version 10.0.x Demo Data**.</span></span> <span data-ttu-id="28f0c-163">オンプレミスのベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-163">Select the version that is closest to the 10.0.x environment that you will deploy as the on-premises baseline.</span></span>
        1. <span data-ttu-id="28f0c-164">このファイルから新しいデータベースを作成するのには、SQL Server に対して復元バックアップ オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-164">Use the restore backup option for SQL Server to create a new database from this file.</span></span> <span data-ttu-id="28f0c-165">(通常、このデータベースには **AXDB** という名前が付けられます。) 詳細については、[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-165">(Typically, this database is named **AXDB**.) For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017).</span></span>
        1. <span data-ttu-id="28f0c-166">デモ データベースはコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-166">The demo database must be configured.</span></span> <span data-ttu-id="28f0c-167">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-167">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>
        1. <span data-ttu-id="28f0c-168">LCS で新しい環境を設定し、バージョン 10.0.x で配置します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-168">In LCS, set up a new environment, and deploy it with version 10.0.x.</span></span> <span data-ttu-id="28f0c-169">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-169">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="28f0c-170">環境を配置する場合、事前に作成したデータベースの名前 (通常は **AXDB**) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-170">When you deploy the environment, the name of the database that you specify should be the name of the database that you created earlier (typically **AXDB**).</span></span>
        1. <span data-ttu-id="28f0c-171">新たに作成した 10.0.x 環境と ISV および VAR モジュールにカスタマイズを適用します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-171">Apply your own customizations, and ISV and VAR modules, to the newly created 10.0.x environment.</span></span> <span data-ttu-id="28f0c-172">それ以外の場合、この環境が最初にデータベースと同期される時、カスタマイズ関連または拡張機能関連のデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-172">Otherwise, when the environment is initially synced with the database, it will delete any customization-related or extension-related data.</span></span>
        1. <span data-ttu-id="28f0c-173">オンプレミスの Application Object Server (AOS)、ビジネス インテリジェンス (BI)、および Management Reporter (MR) サーバーをシャットダウンするか、または**無効化 (再起動)** を選択して、Azure Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-173">Shut down on-premises Application Object Server (AOS), Business Intelligence (BI), and Management Reporter (MR) servers, or stop the services from the Azure Service Fabric portal by selecting **Deactivate (Restart)**.</span></span>
        1. <span data-ttu-id="28f0c-174">名前を変更するか、配置で使用したデモ データベース (通常は **AXDB**) を削除して、新しいデータベース (通常は **AXDBupgraded**) の名前を、デモ データベースが使用していた名前 (通常は **AXDB**) に変更します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-174">Rename or delete the demo database (typically **AXDB**) that you used for deployment, and then rename your new database (typically **AXDBupgraded**) to the name that the demo database had (typically **AXDB**).</span></span>
        1. <span data-ttu-id="28f0c-175">名前を変更したデータベースはコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-175">The renamed database must be configured.</span></span> <span data-ttu-id="28f0c-176">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-176">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>
        1. <span data-ttu-id="28f0c-177">オンプレミス AOS、BI、および MR サーバーを開始するか、または**有効化**を選択して Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-177">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal by selecting **Activate**.</span></span>

            > [!NOTE]
            > <span data-ttu-id="28f0c-178">AOS ノードの開始時にデータベースの同期プロセスがトリガーされますが、プロセスが完了するまで環境は使用できません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-178">The Database synchronization process will be triggered when the AOS nodes start up, and your environment will be unavailable until the process is completed.</span></span>

    - <span data-ttu-id="28f0c-179">カスタマイズがない場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-179">If you don't have customizations, follow these steps:</span></span>

        1. <span data-ttu-id="28f0c-180">オプション: 既存のデータベース (通常は **AXDBold**) の名前を変更し、新しいデータベース (通常は **AXDB**) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-180">Optional: Rename your old database (typically **AXDBold**), and then rename your new database (typically **AXDB**).</span></span> <span data-ttu-id="28f0c-181">次の手順で、アップグレードされたデータベース名の入力を確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-181">In the next step, make sure that you enter the name of the upgraded database.</span></span>
        2. <span data-ttu-id="28f0c-182">LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-182">In LCS, set up a new environment, and deploy it with version 10.0.x (Redeploy).</span></span> <span data-ttu-id="28f0c-183">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-183">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

### <a name="upgrade-where-the-vhd-points-to-your-database"></a><span data-ttu-id="28f0c-184">VHD がデータベースをポイントする場所でアップグレードする</span><span class="sxs-lookup"><span data-stu-id="28f0c-184">Upgrade where the VHD points to your database</span></span>

1. <span data-ttu-id="28f0c-185">オンプレミス環境 (通常は **AXDB**) から、データベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-185">Back up the database from your on-premises environment (typically **AXDB**).</span></span> <span data-ttu-id="28f0c-186">詳細については、「[フル データベース バックアップの作成 (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-186">For more information, see [Create a Full Database Backup (SQL Server)](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2016).</span></span>
1. <span data-ttu-id="28f0c-187">先ほど作成したバックアップをデータベース サーバーを復元し、別の名前 (**AXDBtoupgrade** など) を付けます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-187">Restore the backup that you just created into the database server, and give it a different name (for example, **AXDBtoupgrade**).</span></span> <span data-ttu-id="28f0c-188">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-188">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016).</span></span>
1. <span data-ttu-id="28f0c-189">管理者として Windows PowerShell を開き、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-189">Open Windows PowerShell as an administrator, and run the following script.</span></span>

    ```powershell
    .\Configure-On-Premises-Upgrade.ps1 -DatabaseName '<DB-name>' -DatabaseServer '<SqlServerName>' -DatabaseUser '<User>' -DatabasePassword '<Password>'
    ```

    > [!NOTE]
    > - <span data-ttu-id="28f0c-190">**\<DB-name\>**、**\<SqlServerName\>**、**\<User\>**、および **\<Password\>** を必要な値に置換します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-190">Replace **\<DB-name\>**, **\<SqlServerName\>**, **\<User\>**, and **\<Password\>** with the values that you require.</span></span>
    > - <span data-ttu-id="28f0c-191">SQL Server 認証のみが、このアップグレードで正式にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-191">Only SQL Server authentication is officially supported for this upgrade.</span></span> <span data-ttu-id="28f0c-192">詳細については、「[データベース ユーザーの作成](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-192">For more information, see [Create a Database User](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-database-user?view=sql-server-2016).</span></span>
    > - <span data-ttu-id="28f0c-193">SQL Server 証明書に署名した証明機関の証明書を、OneBox VHD の信頼された証明機関ストアに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-193">You must add the certificate authority certificate that signed your SQL Server certificate to the trusted certificate authorities store in your Onebox VHD.</span></span> <span data-ttu-id="28f0c-194">詳細については、「[信頼されたルート証明書をインストールする](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-194">For more information, see [Installing the trusted root certificate](https://docs.microsoft.com/skype-sdk/sdn/articles/installing-the-trusted-root-certificate).</span></span>
    > - <span data-ttu-id="28f0c-195">使用するデータベースのユーザーに、**sysadmin** サーバー ロールが割り当てられているか、またはアップグレードするデータベースに少なくとも**すべての特権**があるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-195">Make sure that the database user that you use has the **sysadmin** server role, or at least **All Privileges**, assigned on the database that you want to upgrade.</span></span> <span data-ttu-id="28f0c-196">また、ユーザーに tempDB にアクセスするためのアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-196">Also make sure that the user has permissions to access tempDB.</span></span> <span data-ttu-id="28f0c-197">これらの条件を満たしていない場合、アップグレード プロセスのステップ 6 は失敗します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-197">Step 6 of the upgrade process will fail if these conditions aren't met.</span></span>
    > - <span data-ttu-id="28f0c-198">証明機関の証明書を OneBox VHD にインストールする場合、そこに表示されるデータベースへ接続するには完全修飾ドメイン名 (FQDN) または IP アドレスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-198">When you install the certificate authority certificate in the OneBox VHD, make sure that you use the fully qualified domain name (FQDN) or IP address to connect to the database that appears there.</span></span> <span data-ttu-id="28f0c-199">サーバーを指していないため、ドメイン名を使用してデータベースにアクセスできない場合は、ホスト ファイルを編集して FQDN が解決する必要がある FQDN と IP アドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-199">If you can't access the database by using the domain name, because it doesn't point to that server, edit your hosts file, and add the FQDN and the IP address that the FQDN should be resolved to.</span></span>

1. <span data-ttu-id="28f0c-200">LCS では、共有アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-200">In LCS, go to the Shared asset library.</span></span> <span data-ttu-id="28f0c-201">**アセット タイプの選択**で**ソフトウェア配置可能パッケージ**を選択し、**AX2012DataUpgrade-10-0-8** を選択して、**MajorVersionDataUpgrade.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-201">Under **Select asset type**, select **Software deployable package**, and then select **AX2012DataUpgrade-10-0-8** to download the **MajorVersionDataUpgrade.zip** file.</span></span>
1. <span data-ttu-id="28f0c-202">ファイルをコピーして目的の場所に貼り付け (**c:\\D365FFOUpgrade\\** など)、展開します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-202">Copy the file, paste it in the desired location (for example: **c:\\D365FFOUpgrade\\**), and unzip it.</span></span>
1. <span data-ttu-id="28f0c-203">管理者としてコマンド プロンプト ウィンドウを開き、展開したフォルダーへディレクトリを変更して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-203">Open a Command Prompt window as an administrator, change the directory to the folder that you just unzipped, and run the following commands.</span></span>

    1. `AxUpdateInstaller.exe generate -runbookid=upgrade -runbookfile=upgrade.xml -topologyfile=defaulttopologydata.xml -servicemodelfile=defaultservicemodeldata.xml`
    2. `AxUpdateInstaller.exe import -runbookfile=upgrade.xml`
    3. `AxUpdateInstaller.exe execute -runbookid=upgrade`

1. <span data-ttu-id="28f0c-204">ISV または VAR からカスタマイズする場合は、いくつかの投稿データのアップグレード スクリプトを実行する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-204">If you have customizations from ISVs or VARs, check whether you must run some post–data upgrade scripts.</span></span>
1. <span data-ttu-id="28f0c-205">このトピックの後半にある [VHD データベースのリセット (オプション)](#resetting-the-vhd-database-optional) セクションで記述されている値を使用して **Configure-OnpremUpgrade.ps1** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-205">Run the **Configure-OnpremUpgrade.ps1** script by using the values that are stated in the [Resetting the VHD database (Optional)](#resetting-the-vhd-database-optional) section later in this topic.</span></span>
1. <span data-ttu-id="28f0c-206">[Finance + Operations データベースのコンフィギュレーション](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database) の手順に従って、Finance + Operations に対してアップグレードしたデータベースをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-206">Configure your upgraded database for Finance + Operations by following the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>
1. <span data-ttu-id="28f0c-207">新しい Dynamics 365 Finance + Operations (オンプレミス) 環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-207">Deploy a new Dynamics 365 Finance + Operations (on-premises) environment.</span></span>

    - <span data-ttu-id="28f0c-208">カスタマイズがある場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-208">If you have customizations, follow these steps:</span></span>

        1. <span data-ttu-id="28f0c-209">LCS では、共有アセット ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-209">In LCS, go to the Shared asset library.</span></span>
        1. <span data-ttu-id="28f0c-210">**資産タイプの選択**の下で、**モデル**を選択し、**Dynamics 365 Finance + Operations オンプレミスのバージョン 10.0.x デモ データ**をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-210">Under **Select asset type**, select **Model**, and then download **Dynamics 365 Finance + Operations on-premises, Version 10.0.x Demo Data**.</span></span> <span data-ttu-id="28f0c-211">オンプレミスのベースラインとして展開する 10.0.x 環境に最も近いバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-211">Select the version that is closest to the 10.0.x environment that you will deploy as the on-premises baseline.</span></span>
        1. <span data-ttu-id="28f0c-212">SQL Server に対して復元バックアップ オプションを使用して、このファイルから新しいデータベース (通常は **AXDB**) を作成します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-212">Use the restore backup option for SQL Server to create a new database (typically **AXDB**) from this file.</span></span> <span data-ttu-id="28f0c-213">詳細については、「[SSMS を使用したデータベース バックアップの復元](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-213">For more information, see [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2016).</span></span>
        1. <span data-ttu-id="28f0c-214">デモ データベースはコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-214">The demo database must be configured.</span></span> <span data-ttu-id="28f0c-215">[Finance + Operations データベースを構成](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-215">Follow the steps in [Configure the Finance + Operations database](../deployment/setup-deploy-on-premises-pu12.md#configure-the-finance--operations-database).</span></span>
        1. <span data-ttu-id="28f0c-216">LCS にて、新たな環境を設定し、バージョン 10.0.x (再展開) を展開します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-216">In LCS, set up a new environment, and deploy it with version 10.0.x (Redeploy).</span></span> <span data-ttu-id="28f0c-217">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-217">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span> <span data-ttu-id="28f0c-218">環境を配置する場合、事前にコンフィギュレーションしたデータベースの名前 (通常は **AXDB**) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-218">When you deploy the environment, the database that you should specify should be the database that you configured earlier (typically **AXDB**).</span></span>
        1. <span data-ttu-id="28f0c-219">新たに作成した 10.0.x 環境と ISV および VAR モジュールにカスタマイズを適用します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-219">Apply your own customizations, and ISV and VAR modules, to the newly created 10.0.x environment.</span></span> <span data-ttu-id="28f0c-220">それ以外の場合、この環境が最初にデータベースと同期される時、カスタマイズ関連または拡張機能関連のデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-220">Otherwise, when the environment is initially synced with the database, it will delete any customization-related or extension-related data.</span></span>
        1. <span data-ttu-id="28f0c-221">オンプレミス AOS、BI、および MR サーバーをシャットダウンするか、または Service Fabric ポータルからサービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-221">Shut down on-premises AOS, BI, and MR servers, or stop the services from the Service Fabric portal.</span></span>
        1. <span data-ttu-id="28f0c-222">名前を変更するか、配置で使用したデモ データベース (通常は **AXDB**) を削除して、新しいデータベース (通常は **AXDBupgraded**) の名前を、デモ データベースが使用していた名前 (通常は **AXDB**) に変更します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-222">Rename or delete the demo database (typically **AXDB**) that you used for deployment, and then rename your new database (typically **AXDBupgraded**) to the name that the demo database had (typically **AXDB**).</span></span>
        1. <span data-ttu-id="28f0c-223">オンプレミス AOS、BI、および MR サーバーを開始するか、または Service Fabric ポータルからサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-223">Start on-premises AOS, BI, and MR servers, or start the services from the Service Fabric portal.</span></span>

            > [!NOTE]
            > <span data-ttu-id="28f0c-224">AOS ノードの開始時にデータベースの同期プロセスがトリガーされますが、プロセスが完了するまで環境は使用できません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-224">The Database synchronization process will be triggered when the AOS nodes start up, and your environment will be unavailable until the process is completed.</span></span>

    - <span data-ttu-id="28f0c-225">カスタマイズがない場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28f0c-225">If you don't have customizations, follow these steps:</span></span>

        1. <span data-ttu-id="28f0c-226">オプション: 既存のデータベース (通常は **AXDBold**) の名前を変更し、新しいデータベース (通常は **AXDB**) の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-226">Optional: Rename your old database (typically **AXDBold**), and then rename your new database (typically **AXDB**).</span></span> <span data-ttu-id="28f0c-227">次の手順で、アップグレードされたデータベース名の入力を確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-227">In the next step, make sure that you enter the name of the upgraded database.</span></span>
        2. <span data-ttu-id="28f0c-228">新しい環境を設定し、バージョン 10.0.x で配置します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-228">Set up a new environment, and deploy it with version 10.0.x.</span></span> <span data-ttu-id="28f0c-229">詳細については、 [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 以降)](../deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28f0c-229">For more information, see [Set up and deploy on-premises environments (Platform update 12 and later)](../deployment/setup-deploy-on-premises-pu12.md).</span></span>

### <a name="configuring-existing-users"></a><span data-ttu-id="28f0c-230">既存のユーザーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="28f0c-230">Configuring existing users</span></span>

<span data-ttu-id="28f0c-231">以前の手順のいずれかに従った場合、LCS で指定した管理者ユーザーを使用してサインインできます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-231">If you followed either of the previous procedures, you can sign in by using the Administrator user that you specified in LCS.</span></span> <span data-ttu-id="28f0c-232">ただし、他のユーザーは、新しいシステム用にコンフィギュレーションされるまで、サインインできません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-232">However, none of your other users can sign in until they have been configured for the new system.</span></span> <span data-ttu-id="28f0c-233">USERINFO テーブルに対して **Select** ステートメントを実行し、管理者ユーザーの **NETWORKDOMAIN** フィールドの値 (`https://adfs.contoso.com/adfs` または `http://adfs.contoso.com/adfs/services/trust` など) をメモしておき ます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-233">Run a **Select** statement against your USERINFO table, and make a note of the value in the **NETWORKDOMAIN** field for the Administrator user (for example, `https://adfs.contoso.com/adfs` or `http://adfs.contoso.com/adfs/services/trust`).</span></span> <span data-ttu-id="28f0c-234">サインインできる必要のあるすべての対話型ユーザーについて、**NETWORKDOMAIN** フィールドに管理者ユーザーと同じ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-234">Then, for all interactive users who should be able to sign in, set the **NETWORKDOMAIN** field to the same value that the Administrator user has.</span></span> <span data-ttu-id="28f0c-235">**NETWORKALIAS** フィールドも変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28f0c-235">The **NETWORKALIAS** field must also be modified.</span></span> <span data-ttu-id="28f0c-236">Finance + Operations において、このフィールドにはユーザーの電子メールアドレス (`testuser@contoso.com` など) が設定され ます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-236">In Finance + Operations, this field is set to the user's email address (for example, `testuser@contoso.com`).</span></span>

### <a name="resetting-the-vhd-database-optional"></a><span data-ttu-id="28f0c-237">VHD データベースのリセット (オプション)</span><span class="sxs-lookup"><span data-stu-id="28f0c-237">Resetting the VHD database (Optional)</span></span>

<span data-ttu-id="28f0c-238">**Configure-On-Premises-Upgrade.ps1** スクリプトを使用した場合、次のコマンドを実行してデータベースを既定のコンフィギュレーションにリセットします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-238">If you used the **Configure-On-Premises-Upgrade.ps1** script, run the following command to reset your database to the default configuration.</span></span>

```powershell
.\Configure-OnPremUpgrade.ps1 -DatabaseName 'AxDB' -DatabaseServer 'localhost' -DatabaseUser 'axdbadmin' -DatabasePassword 'AOSWebSite@123'
```

## <a name="appendix"></a><span data-ttu-id="28f0c-239">付録</span><span class="sxs-lookup"><span data-stu-id="28f0c-239">Appendix</span></span>

### <a name="using-the-configure-on-premises-upgradeps1-script"></a><span data-ttu-id="28f0c-240">Configure-On-Premises-Upgrade.ps1 スクリプトを使用する</span><span class="sxs-lookup"><span data-stu-id="28f0c-240">Using the Configure-On-Premises-Upgrade.ps1 script</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28f0c-241">このスクリプトは、OneBox VHD 環境からの実行のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="28f0c-241">This script is intended to be run only from a OneBox VHD environment.</span></span>
>
> <span data-ttu-id="28f0c-242">スクリプトは、少なくとも **DatabaseName** パラメーターを渡すことを必要としています。</span><span class="sxs-lookup"><span data-stu-id="28f0c-242">The script requires that you pass at least the **DatabaseName** parameter.</span></span> <span data-ttu-id="28f0c-243">このパラメーターを渡さないと、スクリプトは自動的に要求します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-243">If you don't pass this parameter, the script automatically requests it.</span></span>

<span data-ttu-id="28f0c-244">必要に応じて、**DatabaseServer** または **DatabaseUser** などの追加のパラメーターを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-244">You can pass an additional parameter, such as **DatabaseServer** or **DatabaseUser**, if you want.</span></span> <span data-ttu-id="28f0c-245">ただし、この場合は、スクリプトはすべての追加のパラメーターを要求します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-245">However, in this case, the script will request all additional parameters.</span></span> <span data-ttu-id="28f0c-246">この現象は、スクリプトが VM 外のマシンにデータベース接続を指定する必要があると想定するために発生します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-246">This behavior occurs because the script will assume that you want to point the database connection to a machine outside the VM.</span></span> <span data-ttu-id="28f0c-247">したがって、これらのパラメータは接続を正しく確立するのに必要です。</span><span class="sxs-lookup"><span data-stu-id="28f0c-247">Therefore, those parameters are required to correctly establish the connection.</span></span>

<span data-ttu-id="28f0c-248">次のパラメーターをスクリプトに渡することができます。</span><span class="sxs-lookup"><span data-stu-id="28f0c-248">The following parameters can be passed to the script:</span></span>

- <span data-ttu-id="28f0c-249">**-DatabaseName** – アップグレードするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="28f0c-249">**-DatabaseName** – The name of the database to upgrade.</span></span>
- <span data-ttu-id="28f0c-250">**-DatabaseServer** – Finance + Operations データベースが含まれているデータベース サーバー。</span><span class="sxs-lookup"><span data-stu-id="28f0c-250">**-DatabaseServer** – The database server that contains the Finance + Operations database.</span></span>
- <span data-ttu-id="28f0c-251">**-DatabaseUser** – SQL Server 認証のためのユーザー名。</span><span class="sxs-lookup"><span data-stu-id="28f0c-251">**-DatabaseUser** – The user name for SQL Server Authentication.</span></span>
- <span data-ttu-id="28f0c-252">**-DatabasePassword** – SQL Server 認証のためのパスワードです。</span><span class="sxs-lookup"><span data-stu-id="28f0c-252">**-DatabasePassword** – The password for SQL Server Authentication.</span></span>

<span data-ttu-id="28f0c-253">コンフィギュレーションが渡された後、スクリプトは新しいパラメーターを使用してデータベース接続のテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-253">After the configuration has been passed, the script uses the new parameters to run a database connection test.</span></span> <span data-ttu-id="28f0c-254">スクリプトがデータベースに接続できない場合は、SQL Server Management Studio または別のツールを使用して、接続をデバッグすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="28f0c-254">If the script can't connect to the database, we recommend that you debug the connection from SQL Server Management Studio or another tool.</span></span>

<span data-ttu-id="28f0c-255">**Configure-On-Premises-Upgrade.ps1**</span><span class="sxs-lookup"><span data-stu-id="28f0c-255">**Configure-On-Premises-Upgrade.ps1**</span></span>

```powershell
<#
.Synopsis
    Configures a OneBox deployment to upgrade an OnPrem 7.x database to OnPrem 10.0.x 

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

### <a name="troubleshooting"></a><span data-ttu-id="28f0c-256">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="28f0c-256">Troubleshooting</span></span>

- <span data-ttu-id="28f0c-257">"0" 引数を使用した "Open" の呼び出しで例外が発生しました: 「ログインによって要求されたデータベース「AxDB1」を開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-257">Exception calling "Open" with "0" argument(s): "Cannot open database "AxDB1" requested by the login.</span></span> <span data-ttu-id="28f0c-258">ログインに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="28f0c-258">The login failed.</span></span> <span data-ttu-id="28f0c-259">ユーザー 'axdbadmin' のログインが失敗しました。」データベース名が間違っている、またはユーザーにデータベースへのアクセスがありません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-259">Login failed for user 'axdbadmin'." You supplied the Wrong database name or the user doesn't have access to that database.</span></span> 
- <span data-ttu-id="28f0c-260">"0" 引数を使用した "Open" の呼び出しで例外が発生しました: SQL Server への接続の確立中に、ネットワーク関連またはインスタンス固有のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="28f0c-260">Exception calling "Open" with "0" argument(s): "A network-related or instance-specific error occurred while establishing a connection to SQL Server.</span></span> <span data-ttu-id="28f0c-261">サーバーが見つからない、またはアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="28f0c-261">The server was not found or was not accessible.</span></span> <span data-ttu-id="28f0c-262">インスタンス名が正しいかを確認し、さらに SQL Server が構成されリモート接続が許可されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-262">Verify that the instance name is correct and that SQL Server is configured to allow remote connections.</span></span> <span data-ttu-id="28f0c-263">(プロバイダー: 名前付きパイプ プロバイダー、エラー: 40 - SQL Server への接続を開けませんでした)。</span><span class="sxs-lookup"><span data-stu-id="28f0c-263">(provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)".</span></span> <span data-ttu-id="28f0c-264">スクリプトは、指定された SQL Server との接続を確立できませんでした。</span><span class="sxs-lookup"><span data-stu-id="28f0c-264">The script could not establish a connection with the SQL Server specified.</span></span> <span data-ttu-id="28f0c-265">使用した IP/FQDN およびポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="28f0c-265">Check the ip/fqdn and port that you used.</span></span>  
- <span data-ttu-id="28f0c-266">"0" 引数を使用した "Open" の呼び出しで例外が発生しました: 「ユーザー 'axdbadmin' のログインが失敗しました。」指定されたログイン資格情報が正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="28f0c-266">Exception calling "Open" with "0" argument(s): "Login failed for user 'axdbadmin'." The supplied login credentials are not correct.</span></span>
