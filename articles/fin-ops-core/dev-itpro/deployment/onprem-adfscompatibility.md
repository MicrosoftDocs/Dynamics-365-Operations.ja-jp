---
title: AD FS Microsoft 365 の互換性
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 0659b0be8799ac5f78d41440324a856e75d07e49
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685459"
---
# <a name="ad-fs-microsoft-365-compatibility"></a><span data-ttu-id="7247d-103">AD FS Microsoft 365 の互換性</span><span class="sxs-lookup"><span data-stu-id="7247d-103">AD FS Microsoft 365 compatibility</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="7247d-104">この機能は、アプリケーション更新プログラム 10.0.8、プラットフォーム更新プログラム 32、および LocalAgent 2.2.0 でのみ完全にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7247d-104">This feature is only fully supported starting with application update 10.0.8, Platform update 32, and LocalAgent 2.2.0.</span></span> <span data-ttu-id="7247d-105">詳細については、[部分的サポート](#partialsupport) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7247d-105">For details, see [Partial support](#partialsupport).</span></span> 

<span data-ttu-id="7247d-106">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7247d-106">This topic explains how to use the same instance of Active Directory Federation Services (AD FS) for a Dynamics 365 Finance + Operations (on-premises) environment and for Microsoft 365.</span></span>

## <a name="existing-deployments"></a><span data-ttu-id="7247d-107">既存の配置</span><span class="sxs-lookup"><span data-stu-id="7247d-107">Existing deployments</span></span>

1. <span data-ttu-id="7247d-108">Microsoft Dynamics Lifecycle Services (LCS) から新しいローカル エージェント バージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7247d-108">Download the new local agent version from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7247d-109">バージョン 2.2.0 またはそれ以降である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7247d-109">It should be version 2.2.0 or later.</span></span>
2. <span data-ttu-id="7247d-110">この機能に必要な追加の構成が含まれているので、ローカル エージェント構成ファイルの新しいバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7247d-110">Download the new version of the local agent configuration file, because it has additional configuration that is required for this functionality.</span></span>
3. <span data-ttu-id="7247d-111">新しいローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7247d-111">Modify the new local agent configuration file, and set the **office365AdfsCompatibility** value to **True**.</span></span>
4. <span data-ttu-id="7247d-112">次のコマンドを実行して、古いローカル エージェント バージョンをクラスターからアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="7247d-112">Run the following command to uninstall the old local agent version from your cluster.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
    ```

5. <span data-ttu-id="7247d-113">次のコマンドを実行して、新しいローカル エージェント バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7247d-113">Run the following command to install the new local agent version.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install '<path of localagent-config.json>'
    ```

6. <span data-ttu-id="7247d-114">新しい構成を使用できるようにするには、プラットフォーム更新プログラム 28 またはそれ以降を使用したサービス操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7247d-114">Perform any servicing operation with Platform update 28 or later to make the new configuration available.</span></span>
7. <span data-ttu-id="7247d-115">サービス操作が完了したら、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7247d-115">After servicing is completed, run the following script.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="7247d-116">このステップを省略すると、プライマリ管理者ユーザーはサインインできなくなります。</span><span class="sxs-lookup"><span data-stu-id="7247d-116">If you skip this step, the primary admin user won't be able to sign in.</span></span>

8. <span data-ttu-id="7247d-117">Service Fabric Explorer を使用して、[アプリケーション (AOS など) を再起動](troubleshoot-on-prem.md#restartapplications) します。</span><span class="sxs-lookup"><span data-stu-id="7247d-117">Use Service Fabric Explorer to [Restart applications (such as AOS)](troubleshoot-on-prem.md#restartapplications).</span></span>
9. <span data-ttu-id="7247d-118">配置中に指定されたシステム管理者ユーザーで製品にサインインできることを検証します。</span><span class="sxs-lookup"><span data-stu-id="7247d-118">Verify that you are able to sign in to the product with the system administrator user that was specified during deployment.</span></span> 
10. <span data-ttu-id="7247d-119">LCS 共有アセット ライブラリから、インフラストラクチャ スクリプトの最新バージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7247d-119">Download the newest version of the infrastructure scripts from the LCS Shared asset library.</span></span>
11. <span data-ttu-id="7247d-120">ダウンロードしたインフラストラクチャ スクリプト フォルダーからの Reset-SID.ps1 スクリプトを AOS コンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7247d-120">Copy the Reset-SID.ps1 script from the downloaded infrastructure scripts folder into one of your AOS machines.</span></span>
12. <span data-ttu-id="7247d-121">Reset-Sid.ps1 スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="7247d-121">Execute the Reset-Sid.ps1 script.</span></span>
    
    ```powershell
    .\Reset-SID.ps1 -AxsfCodePath 'C:\ProgramData\SF\AOS_13\Fabric\work\Applications\AXSFType_App184\AXSF.Code.1.0.20190902'
    ```

## <a name="new-deployments"></a><span data-ttu-id="7247d-122">新しい配置</span><span class="sxs-lookup"><span data-stu-id="7247d-122">New deployments</span></span>

1. <span data-ttu-id="7247d-123">[オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って、ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7247d-123">Follow the instructions for installing the local agent in the "Configure a connector and install an on-premises local agent" section of [Set up and deploy on-premises environments](setup-deploy-on-premises-pu12.md#configureconnector).</span></span> <span data-ttu-id="7247d-124">ただし、ローカル エージェントを実際にインストールする前に、この手順のステップ 2 を完了してください。</span><span class="sxs-lookup"><span data-stu-id="7247d-124">However, before you actually install the local agent, complete step 2 of this procedure.</span></span>
2. <span data-ttu-id="7247d-125">ローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7247d-125">Modify the local agent configuration file, and set the **office365AdfsCompatibility** value to **True**.</span></span>
3. <span data-ttu-id="7247d-126">[オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って作業を続行し、プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンを配置します。</span><span class="sxs-lookup"><span data-stu-id="7247d-126">Continue to follow the instructions in the "Configure a connector and install an on-premises local agent" section of [Set up and deploy on-premises environments](setup-deploy-on-premises-pu12.md#configureconnector), and deploy a base version that runs Platform update 28 or later.</span></span> <span data-ttu-id="7247d-127">プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンがない場合は、使用可能な最新の基準バージョンを配置します。</span><span class="sxs-lookup"><span data-stu-id="7247d-127">If there is no base version that runs Platform update 28 or later, deploy the latest base version that is available.</span></span> <span data-ttu-id="7247d-128">次に、プラットフォーム更新プログラム 28 が最上位に配置されるようにサービスを処理します。</span><span class="sxs-lookup"><span data-stu-id="7247d-128">Then service it so that Platform update 28 is deployed on top.</span></span>

## <a name="partial-support"></a><a name="partialsupport"></a> <span data-ttu-id="7247d-129">部分的サポート</span><span class="sxs-lookup"><span data-stu-id="7247d-129">Partial support</span></span>

<span data-ttu-id="7247d-130">部分的サポートとして、ローカル エージェント 2.2.0 またはそれ以降がインストールされていて、プラットフォーム更新プログラム 28 またはそれ以降でサービスを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7247d-130">For partial support, it is necessary to have Local Agent 2.2.0 or later installed and to update the service with Platform update 28 or later.</span></span>

<span data-ttu-id="7247d-131">部分的サポートでは、Financial Reporting サービスに対する認証はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7247d-131">With partial support, authentication against the Financial Reporting service is not supported.</span></span>  
