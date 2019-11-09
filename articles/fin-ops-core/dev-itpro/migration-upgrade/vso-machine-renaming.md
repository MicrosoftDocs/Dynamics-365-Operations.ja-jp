---
title: ローカル開発 (VHD) 環境の名前変更
description: このトピックでは、複数のコンピューター間で Microsoft Azure DevOps プロジェクトにアクセスし、1 つのバージョンのサービスの更新プログラムを正常にインストールできるように、ローカル開発 (VHD) 環境の名前を変更する方法について説明します。
author: MargoC
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25911
ms.assetid: 4f5ff29b-9ae5-4ba2-8b6e-1e5d94e004b3
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0f59c949afa1871bf7c36dfed8fc42d71d28cfa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183151"
---
# <a name="rename-a-local-development-vhd-environment"></a><span data-ttu-id="758b5-103">ローカル開発 (VHD) 環境の名前変更</span><span class="sxs-lookup"><span data-stu-id="758b5-103">Rename a local development (VHD) environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="758b5-104">ローカル開発 (VHD) 環境では、次のシナリオで名前を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="758b5-104">A local development (VHD) environment must be renamed for the following scenarios:</span></span>

* <span data-ttu-id="758b5-105">**複数のコンピューター間で 1 つの Microsoft Azure DevOps プロジェクトにアクセスする:** Azure DevOps がバージョン管理のために必要です。</span><span class="sxs-lookup"><span data-stu-id="758b5-105">**Accessing a single Microsoft Azure DevOps project across multiple machines:** Azure DevOps is required for version control.</span></span> <span data-ttu-id="758b5-106">以前は Visual Studio Online (VSO) または Visual Studio Team Services (VSTS) と呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="758b5-106">It was previously known as Visual Studio Online (VSO) or Visual Studio Team Services (VSTS).</span></span> <span data-ttu-id="758b5-107">開発トポロジでは、複数の仮想マシン (VM) が同じコンピューター名である場合、同じ Azure DevOps プロジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="758b5-107">In development topologies, multiple virtual machines (VMs) can't access the same Azure DevOps project if they have the same machine name.</span></span> <span data-ttu-id="758b5-108">Azure DevOps はマシン名を ID として使用します。</span><span class="sxs-lookup"><span data-stu-id="758b5-108">Azure DevOps uses the machine name for identification.</span></span> <span data-ttu-id="758b5-109">Microsoft Dynamics Lifecycle Services (LCS) からダウンロードされたローカル VM で開発する場合は、問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="758b5-109">If you're developing on local VMs that were downloaded from Microsoft Dynamics Lifecycle Services (LCS), you might encounter issues.</span></span>
* <span data-ttu-id="758b5-110">**1 つのバージョンのサービスの更新プログラムをインストールする:** 8.1.x などの 1 つのバージョンのサービス更新プログラムを、runbook を使用して VHD 環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="758b5-110">**Installing One Version service updates:** One Version service updates, such as 8.1.x, must be installed in VHD environments by using a runbook.</span></span> <span data-ttu-id="758b5-111">Runbook が正常に完了するようにするため、VHD 環境の名前を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="758b5-111">To help guarantee that the runbook is completed successfully, the VHD environments must be renamed.</span></span> <span data-ttu-id="758b5-112">このトピックに記載されているその他の手順を実行する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="758b5-112">Additional steps that are described in this topic must also be completed.</span></span>

## <a name="rename-the-machine"></a><span data-ttu-id="758b5-113">コンピューターの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="758b5-113">Rename the machine</span></span>
<span data-ttu-id="758b5-114">開発を開始するか Azure DevOps に接続する前にマシンの名前を変更してリブートします。</span><span class="sxs-lookup"><span data-stu-id="758b5-114">Rename and restart the machine before you start development or connect to Azure DevOps.</span></span> <span data-ttu-id="758b5-115">新しい名前が Azure DevOps プロジェクトで使用されるすべてのコンピューター間で一意であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="758b5-115">Make sure that the new name is unique among all the machines that are used with the Azure DevOps project.</span></span>

## <a name="update-the-server-name-in-sql-server"></a><span data-ttu-id="758b5-116">SQL Server でサーバー名を更新する</span><span class="sxs-lookup"><span data-stu-id="758b5-116">Update the server name in SQL Server</span></span>
<span data-ttu-id="758b5-117">次のコマンドを実行して、Microsoft SQL Server 2016 でサーバー名を更新します。</span><span class="sxs-lookup"><span data-stu-id="758b5-117">Update the server name in Microsoft SQL Server 2016 by running the following commands.</span></span> 

    sp_dropserver [old_name];
    GO
    sp_addserver [new_name], local;
    GO

<span data-ttu-id="758b5-118">これらのコマンドでは、必ず **old\_name** をサーバーの古い名前に、**new\_name** を新しい名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="758b5-118">In these commands, be sure to replace **old\_name** with the old name of the server and **new\_name** with the new name.</span></span> <span data-ttu-id="758b5-119">既定では、古い名前は **MININT-F36S5EH** ですが、**select @@servername** を実行して古い名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="758b5-119">By default, the old name is **MININT-F36S5EH**, but you can run **select @@servername** to get the old name.</span></span> <span data-ttu-id="758b5-120">また、コマンドの実行が完了した後、必ず SQL Server サービスを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="758b5-120">Additionally, be sure to restart the SQL Server service after the commands have finished running.</span></span>

## <a name="update-sql-server-reporting-services"></a><span data-ttu-id="758b5-121">SQL Server Reporting Services の更新</span><span class="sxs-lookup"><span data-stu-id="758b5-121">Update SQL Server Reporting Services</span></span>
<span data-ttu-id="758b5-122">Reporting Services 構成マネージャーを使用して、SQL Server Reporting Service (SSRS) データベースを更新します。</span><span class="sxs-lookup"><span data-stu-id="758b5-122">Update the SQL Server Reporting Service (SSRS) database by using the Reporting Services Configuration Manager.</span></span> <span data-ttu-id="758b5-123">**データベース** を選択し、**データベースの変更** を選択して新しいサーバー名を使用します。</span><span class="sxs-lookup"><span data-stu-id="758b5-123">Select **Database**, select **Change Database**, and use the new server name.</span></span> <span data-ttu-id="758b5-124">必ず、SQL Server 2016 用の Reporting Services 構成マネージャーを使用してください。</span><span class="sxs-lookup"><span data-stu-id="758b5-124">Make sure that you use Reporting Services Configuration Manager for SQL Server 2016.</span></span>

## <a name="additional-steps-to-install-one-version-service-updates"></a><span data-ttu-id="758b5-125">1 つのバージョンのサービスの更新プログラムをインストールする追加の手順</span><span class="sxs-lookup"><span data-stu-id="758b5-125">Additional steps to install One Version service updates</span></span>
<span data-ttu-id="758b5-126">VHD 環境で 1 つのバージョンのサービスの更新プログラムをインストールするには、次の追加手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="758b5-126">The following additional steps are required in order to install One Version service updates in a VHD environment.</span></span>

### <a name="update-the-azure-storage-emulator"></a><span data-ttu-id="758b5-127">Azure Storage エミュレーター を更新する</span><span class="sxs-lookup"><span data-stu-id="758b5-127">Update the Azure Storage Emulator</span></span>
<span data-ttu-id="758b5-128">Azure Storage エミュレーターを更新し、それが実行されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="758b5-128">Update the Azure Storage Emulator, and make sure that it's running.</span></span> <span data-ttu-id="758b5-129">**スタート** メニューで、**Microsoft Azure Storage エミュレーター - v4.0** を開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="758b5-129">From the **Start** menu, open **Microsoft Azure Storage Emulator - v4.0**, and run the following commands.</span></span>

<span data-ttu-id="758b5-130">このコマンドは、エミュレーターを起動します。</span><span class="sxs-lookup"><span data-stu-id="758b5-130">This command starts the emulator.</span></span>

    AzureStorageEmulator.exe start

<span data-ttu-id="758b5-131">このコマンドは、エミュレーターが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="758b5-131">This command verifies that the emulator is running.</span></span>

    AzureStorageEmulator.exe status

<span data-ttu-id="758b5-132">**-server** スイッチまたは **-forcecreate** スイッチを使用して **init**オプションを試してください。</span><span class="sxs-lookup"><span data-stu-id="758b5-132">Try the **init** option with the **-server** switch or the **-forcecreate** switch.</span></span> <span data-ttu-id="758b5-133">必ず、**new\_name** を新しい名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="758b5-133">Be sure to replace **new\_name** with the new name.</span></span>

    AzureStorageEmulator.exe init -server new_name
    AzureStorageEmulator.exe init -forcecreate

<span data-ttu-id="758b5-134">**init** コマンドが失敗した場合、SQL Server Management Studio を使用してストレージ エミュレーター データベースを削除します。</span><span class="sxs-lookup"><span data-stu-id="758b5-134">If the **init** command fails, delete the storage emulator database by using SQL Server Management Studio.</span></span> <span data-ttu-id="758b5-135">次に、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="758b5-135">Then try the following command.</span></span>

    AzureStorageEmulator.exe init

<span data-ttu-id="758b5-136">このコマンドを実行すると、次のエラー メッセージが表示される場合があります: "エラー: データベースを作成できません。"</span><span class="sxs-lookup"><span data-stu-id="758b5-136">When you run this command, you might receive the following error message: "Error: Cannot create database."</span></span> <span data-ttu-id="758b5-137">ただし、通常、エミュレーターは引き続き起動されます。</span><span class="sxs-lookup"><span data-stu-id="758b5-137">However, the emulator will usually still start.</span></span> <span data-ttu-id="758b5-138">エミュレーターを起動するだけでかまいません。</span><span class="sxs-lookup"><span data-stu-id="758b5-138">You just need the emulator to start.</span></span>

### <a name="update-financial-reporting"></a><span data-ttu-id="758b5-139">財務諸表の更新</span><span class="sxs-lookup"><span data-stu-id="758b5-139">Update financial reporting</span></span>
<span data-ttu-id="758b5-140">1 つのバージョンのサービスの更新プログラムに含まれるスクリプトを使用して、財務報告のためのサーバー名を更新します。</span><span class="sxs-lookup"><span data-stu-id="758b5-140">Update the server name for financial reporting by using a script that is included in the One Version service update.</span></span> <span data-ttu-id="758b5-141">コマンドを取得するには、1 つのバージョンのサービスの更新をダウンロードして展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="758b5-141">To get the command, you must download and expand the One Version service update.</span></span>

<span data-ttu-id="758b5-142">管理者として Microsoft Windows PowerShell コマンド ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="758b5-142">Open a Microsoft Windows PowerShell command window as an admin, and run the following command.</span></span> <span data-ttu-id="758b5-143">このコマンドには、更新する必要がある既定のパスワードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="758b5-143">This command contains the default passwords that might have to be updated.</span></span> <span data-ttu-id="758b5-144">必ず、**new\_name** を新しい名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="758b5-144">Be sure to replace **new\_name** with the new name.</span></span>

    cd <update folder>\MROneBox\Scripts\Update
    .\ConfigureMRDatabase.ps1 -NewAosDatabaseName AxDB -NewAosDatabaseServerName new_name -NewMRDatabaseName ManagementReporter -NewAxAdminUserPassword AOSWebSite@123 -NewMRAdminUserName MRUser -NewMRAdminUserPassword MRWebSite@123 -NewMRRuntimeUserName MRUSer -NewMRRuntimeUserPassword MRWebSite@123 -NewAxMRRuntimeUserName MRUser -NewAxMRRuntimeUserPassword MRWebSite@123