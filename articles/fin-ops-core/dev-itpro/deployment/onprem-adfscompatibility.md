---
title: AD FS Office 365の互換性
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft Office 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: dc858034cfa5e6929966eb211c3c7372dc8ee0cf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249316"
---
# <a name="ad-fs-office-365-compatibility"></a><span data-ttu-id="3961f-103">AD FS Office 365 の互換性</span><span class="sxs-lookup"><span data-stu-id="3961f-103">AD FS Office 365 compatibility</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="3961f-104">現在、この機能は財務報告と互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="3961f-104">Currently this feature is not compatible with Financial Reporting.</span></span> 

> <span data-ttu-id="3961f-105">ローカル エージェント 2.2.0 またはそれ以降がインストールされていて、プラットフォーム更新プログラム 28 またはそれ以降でサービスを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3961f-105">It is necessary to have Local Agent 2.2.0 or greater installed and to service with Platform update 28 or later.</span></span>

<span data-ttu-id="3961f-106">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft Office 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3961f-106">This topic explains how to use the same instance of Active Directory Federation Services (AD FS) for a Dynamics 365 Finance + Operations (on-premises) environment and for Microsoft Office 365.</span></span>

## <a name="existing-deployments"></a><span data-ttu-id="3961f-107">既存の配置</span><span class="sxs-lookup"><span data-stu-id="3961f-107">Existing deployments</span></span>

1. <span data-ttu-id="3961f-108">Microsoft Dynamics Lifecycle Services (LCS) から新しいローカル エージェント バージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="3961f-108">Download the new local agent version from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3961f-109">バージョン 2.2.0 またはそれ以降である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3961f-109">It should be version 2.2.0 or later.</span></span>
2. <span data-ttu-id="3961f-110">この機能に必要な追加の構成が含まれているので、ローカル エージェント構成ファイルの新しいバージョンをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="3961f-110">Download the new version of the local agent configuration file, because it has additional configuration that is required for this functionality.</span></span>
3. <span data-ttu-id="3961f-111">新しいローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3961f-111">Modify the new local agent configuration file, and set the **office365AdfsCompatibility** value to **True**.</span></span>
4. <span data-ttu-id="3961f-112">次のコマンドを実行して、古いローカル エージェント バージョンをクラスターからアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="3961f-112">Run the following command to uninstall the old local agent version from your cluster.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
    ```

5. <span data-ttu-id="3961f-113">次のコマンドを実行して、新しいローカル エージェント バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="3961f-113">Run the following command to install the new local agent version.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install '<path of localagent-config.json>'
    ```

6. <span data-ttu-id="3961f-114">新しい構成を使用できるようにするには、プラットフォーム更新プログラム 28 またはそれ以降を使用したサービス操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="3961f-114">Perform any servicing operation with Platform update 28 or later to make the new configuration available.</span></span>
7. <span data-ttu-id="3961f-115">サービス操作が完了したら、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="3961f-115">After servicing is completed, run the following script.</span></span>

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="3961f-116">このステップを省略すると、プライマリ管理者ユーザーはサインインできなくなります。</span><span class="sxs-lookup"><span data-stu-id="3961f-116">If you skip this step, the primary admin user won't be able to sign in.</span></span>

8. <span data-ttu-id="3961f-117">Service Fabric Explorer を使用して、[Application Object Server (AOS) ノードを再起動](troubleshoot-on-prem.md#restartapplications)します。</span><span class="sxs-lookup"><span data-stu-id="3961f-117">Use Service Fabric Explorer to [restart an Application Object Server (AOS) node](troubleshoot-on-prem.md#restartapplications).</span></span>
9. <span data-ttu-id="3961f-118">USERINFO テーブルで SQL クエリを実行して **NETWORKDOMAIN** フィールドを変更します。</span><span class="sxs-lookup"><span data-stu-id="3961f-118">Run a SQL query on the USERINFO table to modify the **NETWORKDOMAIN** field.</span></span> <span data-ttu-id="3961f-119">古い構成が `https://ax.contoso.com/adfs` だった場合は、すべてのユーザー エントリを `http://ax.contoso.com/adfs/services/trust` に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3961f-119">If your old configuration was `https://ax.contoso.com/adfs`, you should change all your user entries to `http://ax.contoso.com/adfs/services/trust`.</span></span>

## <a name="new-deployments"></a><span data-ttu-id="3961f-120">新しい配置</span><span class="sxs-lookup"><span data-stu-id="3961f-120">New deployments</span></span>

1. <span data-ttu-id="3961f-121">[オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って、ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="3961f-121">Follow the instructions for installing the local agent in the "Configure a connector and install an on-premises local agent" section of [Set up and deploy on-premises environments](setup-deploy-on-premises-pu12.md#configureconnector).</span></span> <span data-ttu-id="3961f-122">ただし、ローカル エージェントを実際にインストールする前に、この手順のステップ 2 を完了してください。</span><span class="sxs-lookup"><span data-stu-id="3961f-122">However, before you actually install the local agent, complete step 2 of this procedure.</span></span>
2. <span data-ttu-id="3961f-123">ローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3961f-123">Modify the local agent configuration file, and set the **office365AdfsCompatibility** value to **True**.</span></span>
3. <span data-ttu-id="3961f-124">[オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って作業を続行し、プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンを配置します。</span><span class="sxs-lookup"><span data-stu-id="3961f-124">Continue to follow the instructions in the "Configure a connector and install an on-premises local agent" section of [Set up and deploy on-premises environments](setup-deploy-on-premises-pu12.md#configureconnector), and deploy a base version that runs Platform update 28 or later.</span></span> <span data-ttu-id="3961f-125">プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンがない場合は、使用可能な最新の基準バージョンを配置します。</span><span class="sxs-lookup"><span data-stu-id="3961f-125">If there is no base version that runs Platform update 28 or later, deploy the latest base version that is available.</span></span> <span data-ttu-id="3961f-126">次に、プラットフォーム更新プログラム 28 が最上位に配置されるようにサービスを処理します。</span><span class="sxs-lookup"><span data-stu-id="3961f-126">Then service it so that Platform update 28 is deployed on top.</span></span>
