---
title: オンプレミス環境でのネットワーク プリンター デバイスのインストール
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。
author: RichdiMSFT
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 0f9b76e3a6a814e90d0a98d68db7e3288ac7f82a
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924218"
---
# <a name="install-network-printer-devices-in-on-premises-environments"></a><span data-ttu-id="c2a85-103">オンプレミス環境でのネットワーク プリンター デバイスのインストール</span><span class="sxs-lookup"><span data-stu-id="c2a85-103">Install network printer devices in on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2a85-104">このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-104">This topic explains how to connect an on-premises deployment of Microsoft Dynamics 365 Finance + Operations (on-premises) to existing network printer devices.</span></span> <span data-ttu-id="c2a85-105">オンプレミス アプリケーションでのネットワーク印刷は、Microsoft Windows Server 2016 の「[印刷およびドキュメント サービス](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831468(v=ws.11))」機能でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-105">Network printing in the on-premises application is supported by the [Print and Document Services](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831468(v=ws.11)) feature in Microsoft Windows Server 2016.</span></span> <span data-ttu-id="c2a85-106">この機能を使用すると、プリンター管理に関連するタスクを集中管理できます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-106">This feature lets you centralize tasks that are related to printer management.</span></span> <span data-ttu-id="c2a85-107">印刷およびドキュメント サービスをインストールして構成するには、Application Object Server (AOS) のプライマリー インスタンスをホストするサーバーへの管理アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="c2a85-107">To install and configure Print and Document Services, you must have administrative access to the server that hosts the primary instance of Application Object Server (AOS).</span></span>

<span data-ttu-id="c2a85-108">ネットワーク印刷サービスの構成には、次の 2 つの役割があります。</span><span class="sxs-lookup"><span data-stu-id="c2a85-108">Two roles are associated with the configuration of network printing services:</span></span>

- <span data-ttu-id="c2a85-109">**サービス管理者** – この役割を持つ担当者は、インストールやプラットフォーム インフラストラクチャのコンポーネントのコンフィギュレーションを担当します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-109">**Service Administrator** – The person who has this role is responsible for installing and configuring components of the platform infrastructure.</span></span> <span data-ttu-id="c2a85-110">従来、この役割は昇格したドメイン権限を持った Active Directory アカウントです。</span><span class="sxs-lookup"><span data-stu-id="c2a85-110">Traditionally, this role is an Active Directory account that has elevated domain privileges.</span></span> <span data-ttu-id="c2a85-111">Microsoft Windows Server のコンポーネントのインストールに必要な権限があります。</span><span class="sxs-lookup"><span data-stu-id="c2a85-111">It has enough privileges to install components of Microsoft Windows Server.</span></span>
- <span data-ttu-id="c2a85-112">**組織の管理者** – このロールを持つユーザーはアプリケーション セキュリティ権限を管理します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-112">**Organization Administrator** – The person who has this role manages application security privileges.</span></span> <span data-ttu-id="c2a85-113">この Active Directory アカウントは、**システム管理者** ロールに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="c2a85-113">This Active Directory account is assigned to the **System Administrator** role.</span></span>

<span data-ttu-id="c2a85-114">組織の管理者がネットワーク プリンターの追加を開始する前に、サービス管理者はプライマリ AOS インスタンスをホストするサーバーに印刷およびドキュメント サービスをインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2a85-114">Before the organization administrator can begin to add network printers, the service administrator must install and configure Print and Document Services on the server that hosts the primary AOS instance.</span></span> <span data-ttu-id="c2a85-115">組織の管理者は、組み込みツールを使用してネットワーク プリンター デバイスの設定を開始できます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-115">The organization administrator can then begin to use built-in tools to configure network printer devices.</span></span>

## <a name="install-and-configure-print-and-document-services"></a><span data-ttu-id="c2a85-116">印刷およびドキュメント サービスのインストールと構成</span><span class="sxs-lookup"><span data-stu-id="c2a85-116">Install and configure Print and Document Services</span></span>

<span data-ttu-id="c2a85-117">環境管理者は、このセクションの情報を使用してネットワーク印刷サービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-117">The environment administrator uses the information in this section to enable network printing services.</span></span>

1. <span data-ttu-id="c2a85-118">[印刷およびドキュメント サービスのインストール](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134159(v=ws.11))の手順に従って印刷およびドキュメント サービスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-118">Install Print and Document Services by following the instructions in [Install Print and Document Services](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134159(v=ws.11)).</span></span>
2. <span data-ttu-id="c2a85-119">次の手順に従って印刷およびドキュメント サービスをコンフィギュレーションします [印刷およびドキュメント サービスのコンフィギュレーション](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134163(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="c2a85-119">Configure Print and Document Services by following the instructions in [Configure Print and Document Services](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134163(v=ws.11)).</span></span>
3. <span data-ttu-id="c2a85-120">AXService アプリケーションをホストするために使用する各サーバーに対して、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2a85-120">Follow these steps for each server that is used to host the AXService application:</span></span>
    1. <span data-ttu-id="c2a85-121">ローカル サーバーで、**ローカル ユーザーとグループ** マネージャーを開始します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-121">On the local server, start the **Local Users and Groups** manager.</span></span>
    2. <span data-ttu-id="c2a85-122">**グループ** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-122">Select the **Groups** node.</span></span>
    3. <span data-ttu-id="c2a85-123">**出力演算子** を右クリックし、**グループへの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-123">Right-click **Print Operators**, and then select **Add to Group**.</span></span>
    4. <span data-ttu-id="c2a85-124">グループに AXService アプリケーションを実行するために使用されるネットワーク Active Directory アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-124">Add the network Active Directory account that is used to run the AXService application to the group.</span></span>

> [!NOTE]
> <span data-ttu-id="c2a85-125">インフラストラクチャ スクリプトのバージョン 2.9.0 移行、アカウントは自動的に適切なグループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-125">Starting with version 2.9.0 of the infrastructure scripts, the accounts are automatically added to the appropriate group.</span></span>

### <a name="install-printers-on-nodes-where-axservice-is-executing-under-a-domain-account"></a><span data-ttu-id="c2a85-126">AXService がドメイン アカウントで実行されているノードにプリンターをインストール</span><span class="sxs-lookup"><span data-stu-id="c2a85-126">Install printers on nodes where AXService is executing under a domain account</span></span>
<span data-ttu-id="c2a85-127">AXService がドメイン アカウントで実行されているノードにプリンターをインストールするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2a85-127">To install printers on nodes where AXService is executing under a domain account, follow these steps:</span></span>

1. <span data-ttu-id="c2a85-128">AXService ユーザー アカウントを使用してネットワーク プリンターをインストールします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-128">Install network printers by using the AXService user account.</span></span> <span data-ttu-id="c2a85-129">このステップにより、プリンター ドライバーが AXService ユーザー アカウントで使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-129">This step helps to ensure that the printer driver is available to the AXService user account.</span></span>
2. <span data-ttu-id="c2a85-130">すべての接続が正しく構成されていることを確認するため、インストールされているプリンターのテスト ページを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-130">Print a test page on the installed printers to make sure that all the connections are correctly configured.</span></span>
3. <span data-ttu-id="c2a85-131">ユーザーのプロファイルが正しく読み込まれることを確認し、プリンターを見つけるために、AXService アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-131">Restart the AXService application to help ensure that the user's profile is correctly loaded so that it can locate the printer driver.</span></span>

### <a name="install-printers-on-nodes-where-axservice-is-executing-under-a-group-managed-service-account-gmsa"></a><span data-ttu-id="c2a85-132">AXService がグループ管理サービス アカウント (gMSA) で実行されているノードにプリンターをインストール</span><span class="sxs-lookup"><span data-stu-id="c2a85-132">Install printers on nodes where AXService is executing under a group Managed Service Account (gMSA)</span></span>
<span data-ttu-id="c2a85-133">AXService が gMSA で実行されているノードにプリンターをインストールするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2a85-133">To install printers on nodes where AXService is executing under a gMSA, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2a85-134">このセクションには、少なくともバージョン 2.9.0 のインフラストラクチャ スクリプトが必要です。</span><span class="sxs-lookup"><span data-stu-id="c2a85-134">This section requires at least version 2.9.0 of the infrastructure scripts.</span></span>
> <span data-ttu-id="c2a85-135">また 、[SysInternals Suite](https://docs.microsoft.com/sysinternals/downloads/) をダウンロードする必要があります 。</span><span class="sxs-lookup"><span data-stu-id="c2a85-135">Additionally, you need to download the [SysInternals Suite](https://docs.microsoft.com/sysinternals/downloads/).</span></span>

1. <span data-ttu-id="c2a85-136">AOS が使用可能になる各プリンタのネットワーク上の場所を追加して、Printers.json ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-136">Update the Printers.json file by adding the network location of each printer that should be made available to the AOS.</span></span> <span data-ttu-id="c2a85-137">例のエントリを必ず削除してください。</span><span class="sxs-lookup"><span data-stu-id="c2a85-137">Ensure that you remove the example entries.</span></span> 
2. <span data-ttu-id="c2a85-138">インフラストラクチャ スクリプト フォルダから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-138">Run the following command from the Infrastructure Scripts folder.</span></span>

```powershell
# Exports the script files to be executed on each VM into a directory VMs\<VMName>.
.\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml    
```

3. <span data-ttu-id="c2a85-139">各 infrastructure\VMs\<VMName> フォルダーの内容を、対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-139">Copy the contents of each infrastructure\VMs\<VMName> folder to the corresponding VM.</span></span> <span data-ttu-id="c2a85-140">(リモート処理スクリプトを使用している場合は、コンテンツが自動的に対象の VM にコピーされます。) 続いて、次のコマンドを管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-140">(If the remoting scripts are used, they will automatically copy the contents to the target VMs.) Then run the following command as an administrator.</span></span>

> [!NOTE]
> - <span data-ttu-id="c2a85-141">次の手順では、複数の VM での実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="c2a85-141">The following procedure requires execution on multiple VMs.</span></span> <span data-ttu-id="c2a85-142">ただし、プロセスを簡略化するために、提供されるリモート処理スクリプトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-142">However, to simplify the process, you can use the remoting scripts that are provided.</span></span> <span data-ttu-id="c2a85-143">これらのスクリプトを使用すると、**.\\Export-Scripts.ps1** コマンドの実行に使用されるのと同じコンピューターなど、単一のコンピューターから必要なスクリプトを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-143">These scripts let you run the required scripts from a single machine, such as the same machine that is used to run the **.\\Export-Scripts.ps1** command.</span></span> <span data-ttu-id="c2a85-144">リモート処理スクリプトが利用可能な場合、Windows PowerShell セクションの **\# If Remoting** コメントの後に宣言されます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-144">When the remoting scripts are available, they are declared after a **\# If Remoting** comment in the Windows PowerShell sections.</span></span>
> - <span data-ttu-id="c2a85-145">リモート処理では [WinRM](/windows/win32/winrm/portal?redirectedfrom=MSDN) を使用します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-145">Remoting uses [WinRM](/windows/win32/winrm/portal?redirectedfrom=MSDN).</span></span> <span data-ttu-id="c2a85-146">場合によっては、[CredSSP](/windows/win32/secauthn/credential-security-support-provider?redirectedfrom=MSDN) を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2a85-146">In some cases, it requires that [CredSSP](/windows/win32/secauthn/credential-security-support-provider?redirectedfrom=MSDN) be enabled.</span></span> <span data-ttu-id="c2a85-147">リモート処理モジュールでは、実行ごとに CredSSP を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-147">The remoting module enables and disables CredSSP on an execution-by-execution basis.</span></span> <span data-ttu-id="c2a85-148">使用しない場合は、CredSSP を無効にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c2a85-148">We recommend that you disable CredSSP when it isn't used.</span></span> <span data-ttu-id="c2a85-149">そうしないと、資格情報の盗難リスクが伴います。</span><span class="sxs-lookup"><span data-stu-id="c2a85-149">Otherwise, there is a risk of credential theft.</span></span> <span data-ttu-id="c2a85-150">設定が完了したら、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-150">When you've completed the setup, run the following command.</span></span>
> 
> ```powershell
> .\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml.
> ```

```powershell
# If Remoting, execute
# .\Install-PrintersOnGmsa-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -SysInternalsFolderLocation \\networkshare\SysInternalsSuite -ForcePushLBDScripts

.\Install-PrintersOnGmsa.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -SysInternalsFolderLocation \\networkshare\SysInternalsSuite
```

## <a name="manage-network-printers"></a><span data-ttu-id="c2a85-151">ネットワーク プリンターの管理</span><span class="sxs-lookup"><span data-stu-id="c2a85-151">Manage network printers</span></span>

<span data-ttu-id="c2a85-152">システム管理者は、このセクションの情報を使用してネットワーク プリンターを定義します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-152">The system administrator uses the information in this section to define network printers.</span></span>

1. <span data-ttu-id="c2a85-153">**組織管理** \> **設定** \> **ネットワーク プリンター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-153">Go to **Organization administration** \> **Setup** \> **Network printers**.</span></span>
2. <span data-ttu-id="c2a85-154">**ネットワーク プリンター** ページで、新しいプリンターを追加します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-154">On the **Network printers** page, add new printers.</span></span> <span data-ttu-id="c2a85-155">各プリンターで、名前、説明、パス、およびステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-155">For each printer, specify a name, description, path, and status.</span></span> <span data-ttu-id="c2a85-156">プリンター パスがインストールされているプリンターのネットワーク パスと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c2a85-156">Make sure that the printer path matches the network path of the installed printer.</span></span>

<span data-ttu-id="c2a85-157">**有効** とマークされている項目は、すぐにアプリケーションのユーザーによって利用できるようになるので、ネットワーク プリンター デバイスで文書スタイル レポートの印刷を開始できます。</span><span class="sxs-lookup"><span data-stu-id="c2a85-157">Items that are marked **Active** immediately become available to application users, so that they can begin to print document-style reports on network printer devices.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
