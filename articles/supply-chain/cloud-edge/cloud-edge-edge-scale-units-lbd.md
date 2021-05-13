---
title: LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する (プレビュー)
description: このトピックでは、カスタム ハードウェアとローカル ビジネス データ (LBD) に基づく配置を使用して、オンプレミスのエッジ スケール ユニットをプロビジョニングする方法について説明します。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 23ae1892f410dcbf0de5e656e35b0291372877dc
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938264"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a><span data-ttu-id="86eb5-103">LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="86eb5-103">Deploy edge scale units on custom hardware using LBD (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="86eb5-104">エッジ スケール ユニットは、Supply Chain Management の分散ハイブリッド トポロジで重要な役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="86eb5-104">Edge scale units play an important role in the distributed hybrid topology for supply chain management.</span></span> <span data-ttu-id="86eb5-105">ハイブリッド トポロジでは、Supply Chain Management のクラウド ハブとクラウド内またはエッジ上の追加のスケール ユニットとの間でワークロードを配布できます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-105">In the hybrid topology you can distribute workloads between your Supply Chain Management cloud hub and additional scale units in the cloud or on the edge.</span></span>

<span data-ttu-id="86eb5-106">エッジ スケール ユニットは、ローカル ビジネス データ (LBD) [オンプレミス環境](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) を作成することで配置できます。 その後、Supply Chain Management の分散ハイブリッド トポロジで スケール ユニットとして機能するように構成します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-106">Edge scale units can be deployed by creating a local business data (LBD) [on-premises environment](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) and then configuring it to function as a scale unit in your distributed hybrid topology for supply chain management.</span></span> <span data-ttu-id="86eb5-107">これは、オンプレミスの LBD 環境を、ハブとして機能するように構成されたクラウド内の Supply Chain Management 環境に関連付けることで実現されます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-107">This is achieved by associating the on-premises LBD environment with a Supply Chain Management environment in the cloud, which has been configured to function as a hub.</span></span>  

<span data-ttu-id="86eb5-108">エッジ スケール ユニットは、現在プレビュー中です。</span><span class="sxs-lookup"><span data-stu-id="86eb5-108">Edge scale units are currently in preview.</span></span> <span data-ttu-id="86eb5-109">したがって、このタイプの環境は、[プレビュー条件](https://aka.ms/scmcnepreviewterms) に従ってのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-109">Therefore, you may use an environment of this type only according to the [preview terms](https://aka.ms/scmcnepreviewterms).</span></span>

<span data-ttu-id="86eb5-110">このトピックでは、オンプレミスの LBD 環境をエッジ スケール ユニットとして設定し、それをハブに関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-110">This topic describes how to set up an on-premises LBD environment as an edge scale unit and then associate it with a hub.</span></span>

## <a name="deployment-overview"></a><span data-ttu-id="86eb5-111">配置の概要</span><span class="sxs-lookup"><span data-stu-id="86eb5-111">Deployment overview</span></span>

<span data-ttu-id="86eb5-112">次に配置の手順の概要について示します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-112">Here is an overview of the deployment steps.</span></span>

1. <span data-ttu-id="86eb5-113">**Microsoft Dynamics Lifecycle Services (LCS) で LBD プロジェクトの LBD スロットを有効にします。**</span><span class="sxs-lookup"><span data-stu-id="86eb5-113">**Enable an LBD slot in your LBD project in Microsoft Dynamics Lifecycle Services (LCS).**</span></span>

    <span data-ttu-id="86eb5-114">プレビュー時に、LBD エッジ スケール ユニットは既存の LBD 顧客をターゲットとしています。</span><span class="sxs-lookup"><span data-stu-id="86eb5-114">During preview, LBD edge scale units target existing LBD customers.</span></span> <span data-ttu-id="86eb5-115">追加の 60 日間限定 LBD サンドボックス スロットは、特定の顧客の状況でにのみ提供されます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-115">An additional 60-day limited LBD sandbox slot will be provided in only specific customer situations.</span></span>

1. <span data-ttu-id="86eb5-116">***空* のデータベースを使用して LBD 環境を設定および配置します。**</span><span class="sxs-lookup"><span data-stu-id="86eb5-116">**Set up and deploy an LBD environment with an *empty* database.**</span></span>

    <span data-ttu-id="86eb5-117">LCS を使用して、最新のトポロジと空のデータベースで LBD 環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-117">Use LCS to deploy the LBD environment with the latest topology and an empty database.</span></span> <span data-ttu-id="86eb5-118">詳細については、このトピックの後半にある[空のデータベースを使用して LBD 環境の設定および配置](#set-up-deploy) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-118">For more information, see the [Setup and deploy an LBD environment with empty database](#set-up-deploy) section later in this topic.</span></span> <span data-ttu-id="86eb5-119">ハブおよびスケール ユニット環境間で、プラットフォーム更新プログラム 43 以上を備えた Supply Chain Management バージョン 10.0.19 を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-119">You must use Supply Chain Management version 10.0.19 with platform update 43 or higher across hub and scale unit environments.</span></span>

1. <span data-ttu-id="86eb5-120">**LCS でターゲット パッケージを LBD プロジェクト資産にアップロードします。**</span><span class="sxs-lookup"><span data-stu-id="86eb5-120">**Upload target packages into LBD project assets in LCS.**</span></span>

    <span data-ttu-id="86eb5-121">アプリケーション、プラットフォーム、およびハブとエッジ スケール ユニット間で使用するカスタマイズ パッケージを準備します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-121">Prepare application, platform, and customization packages that you use across the hub and the edge scale unit.</span></span> <span data-ttu-id="86eb5-122">詳細については、このトピックの後半にある[LCS でターゲット パッケージを LBD プロジェクト資産にアップロード](#upload-packages) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-122">For more information, see the [Upload target packages into LBD project assets in LCS](#upload-packages) section later in this topic.</span></span>

1. <span data-ttu-id="86eb5-123">**ターゲット パッケージを使用して LBD 環境にサービスを提供します。**</span><span class="sxs-lookup"><span data-stu-id="86eb5-123">**Service the LBD environment with the target packages.**</span></span>

    <span data-ttu-id="86eb5-124">この手順により、同じビルドとカスタマイズがハブとスポークに配置されます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-124">This step ensures that the same build and customizations are deployed on the hub and the spoke.</span></span> <span data-ttu-id="86eb5-125">詳細については、このトピックの後半にある[ターゲット パッケージを使用して LBD 環境にサービスを提供](#service-target-packages) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-125">For more information, see the [Service the LBD environment with target packages](#service-target-packages) section later in this topic.</span></span>

1. <span data-ttu-id="86eb5-126">**スケール ユニットの構成とワークロードの割り当てを完了します。**</span><span class="sxs-lookup"><span data-stu-id="86eb5-126">**Complete the scale unit configuration and workload assignment.**</span></span>

    <span data-ttu-id="86eb5-127">詳細については、このトピックの後半の[LBD エッジ スケール ユニットをハブに割り当てる](#assign-edge-to-hub) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-127">For more information, see the [Assign your LBD edge scale unit to a hub](#assign-edge-to-hub) section later in this topic.</span></span>

<span data-ttu-id="86eb5-128">このトピックの残りのセクションでは、これらの手順を完了する方法に関する詳細をさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-128">The remaining sections of this topic provide more details about how to complete these steps.</span></span>

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a> <span data-ttu-id="86eb5-129">空のデータベースを使用して LBD 環境を設定および配置</span><span class="sxs-lookup"><span data-stu-id="86eb5-129">Set up and deploy an LBD environment with an empty database</span></span>

<span data-ttu-id="86eb5-130">この手順により、機能的な LBD 環境が作成されます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-130">This step creates a functional LBD environment.</span></span> <span data-ttu-id="86eb5-131">ただし、環境はアプリケーションとプラットフォーム バージョンがハブ環境と同じである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="86eb5-131">However, the environment doesn't necessarily have the same application and platform versions as the hub environment.</span></span> <span data-ttu-id="86eb5-132">また、カスタマイズされていないので、スケール ユニットとして機能することはまだ有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="86eb5-132">Additionally, it's still missing the customizations, and it hasn't yet been enabled to work as a scale unit.</span></span>

1. <span data-ttu-id="86eb5-133">[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="86eb5-133">Follow the instructions in [Setup and deploy on-premises environments (Platform update 41 and later)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).</span></span> <span data-ttu-id="86eb5-134">ハブおよびスケール ユニット環境間で、プラットフォーム更新プログラム 43 以上を備えた Supply Chain Management バージョン 10.0.19 を使用する必要がある</span><span class="sxs-lookup"><span data-stu-id="86eb5-134">You must use Supply Chain Management version 10.0.19 with platform update 43 or higher across hub and scale unit environments</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="86eb5-135">このトピックの手順を完了する **前** に、このセクションの残りの部分を読みます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-135">Read the rest of this section **before** you complete the steps in that topic.</span></span>

1. <span data-ttu-id="86eb5-136">infrastructure\\ConfigTemplate.xml ファイルで構成を説明する前に、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-136">Before you describe your configuration in the infrastructure\\ConfigTemplate.xml file, run the following script:</span></span>

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > <span data-ttu-id="86eb5-137">このスクリプトは、エッジ スケール ユニットの配置に必要ない構成を削除します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-137">This script will remove any configuration that is not needed for deploying edge scale units.</span></span>

1. <span data-ttu-id="86eb5-138">[データベースの構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) で説明されているように、空のデータを含むデータベースを設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-138">Set up a database that contains empty data, as described in [Configure databases](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).</span></span> <span data-ttu-id="86eb5-139">この手順では空の data.bak ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-139">Use the empty data.bak file for this step.</span></span>
1. <span data-ttu-id="86eb5-140">配置前スクリプトを設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-140">Set up the pre-deployment script.</span></span> <span data-ttu-id="86eb5-141">詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-141">For more information, see [Local agent pre-deployment and post-deployment scripts](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).</span></span>

    1. <span data-ttu-id="86eb5-142">**インフラストラクチャ スクリプト** の **ScaleUnit** フォルダーから、環境で設定されたエージェント ファイル ファイル ストレージ共有の **スクリプト** フォルダーに内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="86eb5-142">Copy the contents from the **ScaleUnit** folder in **Infrastructure Scripts** to the **Scripts** folder in the agent file storage share that was set up in the environment.</span></span> <span data-ttu-id="86eb5-143">通常、パスは  \\\\lbdiscsi01\\agent\\Scripts です。</span><span class="sxs-lookup"><span data-stu-id="86eb5-143">A typical path is \\\\lbdiscsi01\\agent\\Scripts.</span></span>
    2. <span data-ttu-id="86eb5-144">必要なパラメータを使用してスクリプトを呼び出す **PreDeployment.ps1** スクリプトを作成します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-144">Create the **PreDeployment.ps1** script that will invoke the scripts by using the required parameters.</span></span> <span data-ttu-id="86eb5-145">配置前スクリプトは、エージェント ファイルストレージ共有の **スクリプト** フォルダーに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-145">The pre-deployment script must be put in the **Scripts** folder in the agent file storage share.</span></span> <span data-ttu-id="86eb5-146">そうしない場合は実行されません。</span><span class="sxs-lookup"><span data-stu-id="86eb5-146">Otherwise, it can't be run.</span></span> <span data-ttu-id="86eb5-147">通常、パスは \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1 です。</span><span class="sxs-lookup"><span data-stu-id="86eb5-147">A typical path is \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.</span></span>

        <span data-ttu-id="86eb5-148">PreDeployment.ps1 スクリプトの内容は、次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-148">The contents of the PreDeployment.ps1 script will resemble the following example.</span></span>

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > <span data-ttu-id="86eb5-149">InstanceId パラメータは、2 文字にのみにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-149">The InstanceId parameter should be only two characters.</span></span> <span data-ttu-id="86eb5-150">最初の文字は @ で、2 番目の文字は英語のアルファベットの任意の大文字にできます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-150">The first character is @ and the second can be any capital letter in the English alphabet.</span></span>
        >
        > - <span data-ttu-id="86eb5-151">有効な値:</span><span class="sxs-lookup"><span data-stu-id="86eb5-151">Valid values:</span></span>
        >   - <span data-ttu-id="86eb5-152">@D</span><span class="sxs-lookup"><span data-stu-id="86eb5-152">@D</span></span>
        >   - <span data-ttu-id="86eb5-153">@X</span><span class="sxs-lookup"><span data-stu-id="86eb5-153">@X</span></span>
        > - <span data-ttu-id="86eb5-154">無効な値:</span><span class="sxs-lookup"><span data-stu-id="86eb5-154">Not valid values:</span></span>
        >   - <span data-ttu-id="86eb5-155">@a</span><span class="sxs-lookup"><span data-stu-id="86eb5-155">@a</span></span>
        >   - <span data-ttu-id="86eb5-156">@4</span><span class="sxs-lookup"><span data-stu-id="86eb5-156">@4</span></span>
        >   - @#

1. <span data-ttu-id="86eb5-157">使用可能な最新の基準トポロジを使用して環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-157">Deploy the environment by using the latest base topology that is available.</span></span>

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a> <span data-ttu-id="86eb5-158">LCS でターゲット パッケージを LBD プロジェクト資産にアップロード</span><span class="sxs-lookup"><span data-stu-id="86eb5-158">Upload target packages into LBD project assets in LCS</span></span>

<span data-ttu-id="86eb5-159">この手順では、LBD スケール ユニット環境に移行するアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズを準備します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-159">This step prepares the application version, platform version, and customizations that will be transitioned to your LBD scale unit environment.</span></span>

1. <span data-ttu-id="86eb5-160">ハブ環境に適用されたものと同じ、結合されたアプリケーション/プラットフォーム パッケージを、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="86eb5-160">Upload the same combined application/platform package that was applied to the hub environment into the asset library of the LCS on-premises project.</span></span>
1. <span data-ttu-id="86eb5-161">ハブ環境に適用されたカスタム配置可能パッケージのコピーを取得し、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="86eb5-161">Get a copy of the custom deployable package that was applied to the hub environment, and upload it into the asset library of the LCS on-premises project.</span></span>

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a> <span data-ttu-id="86eb5-162">ターゲット パッケージを使用して LBD 環境にサービスを提供</span><span class="sxs-lookup"><span data-stu-id="86eb5-162">Service the LBD environment with target packages</span></span>

<span data-ttu-id="86eb5-163">この手順では、LBD スケール ユニット環境のアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズをハブに対応するようになります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-163">This step aligns the application version, platform version, and customizations in your LBD scale unit environment with the hub.</span></span>

1. <span data-ttu-id="86eb5-164">前の手順でアップロードした結合されたアプリケーション/プラットフォーム パッケージを使用して、LBD 環境にサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-164">Service the LBD environment with the combined application/platform package that you uploaded in the previous step.</span></span>
1. <span data-ttu-id="86eb5-165">前の手順でアップロードしたカスタム配置可能パッケージを使用して、LBD 環境にサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-165">Service the LBD environment with the custom deployable package that you uploaded in the previous step.</span></span>

    <span data-ttu-id="86eb5-166">![管理を選択 > LCS で更新プログラムを適用](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "管理を選択 > LCS で更新プログラムを適用")</span><span class="sxs-lookup"><span data-stu-id="86eb5-166">![Selecting Maintain > Apply updates in LCS](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Selecting Maintain > Apply updates in LCS")</span></span>

    <span data-ttu-id="86eb5-167">![カスタマイズ パッケージの選択](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "カスタマイズ パッケージの選択")</span><span class="sxs-lookup"><span data-stu-id="86eb5-167">![Selecting your customization package](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Selecting your customization package")</span></span>

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a> <span data-ttu-id="86eb5-168">LBD エッジ スケール ユニットをハブに割り当てる</span><span class="sxs-lookup"><span data-stu-id="86eb5-168">Assign your LBD edge scale unit to a hub</span></span>

<span data-ttu-id="86eb5-169">エッジ スケール ユニットがまだプレビューされている間に、GitHub で利用可能な [スケール ユニット配置および構成ツール](https://github.com/microsoft/SCMScaleUnitDevTools) を使用して、LBD エッジ スケール ユニットをハブに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-169">While edge scale units are still in preview, you must use the [scale unit deployment and configuration tools](https://github.com/microsoft/SCMScaleUnitDevTools) that are available on GitHub to assign your LBD edge scale unit to a hub.</span></span> <span data-ttu-id="86eb5-170">このプロセスにより、LBD 構成をエッジ スケール ユニットとして機能させ、ハブに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-170">The process enables an LBD configuration to function as an edge scale unit and associates it with the hub.</span></span> <span data-ttu-id="86eb5-171">このプロセスは、1 ボックス開発環境の構成に似ています。</span><span class="sxs-lookup"><span data-stu-id="86eb5-171">The process is similar to configuring a one-box development environment.</span></span>

1. <span data-ttu-id="86eb5-172">[SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) の最新のリリースをダウンロードし、ファイルの内容を解凍します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-172">Download the latest release of [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) and unzip the contents of the file.</span></span>
1. <span data-ttu-id="86eb5-173">`UserConfig.sample.xml` ファイルのコピーを作成し、`UserConfig.xml` と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="86eb5-173">Create a copy of the `UserConfig.sample.xml` file and name it `UserConfig.xml`.</span></span>
1. <span data-ttu-id="86eb5-174">[スケール ユニットとワークロードの配置ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations) で説明したように、Azure AD テナントに Microsoft Azure Active Directory (Azure AD) アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-174">Create a Microsoft Azure Active Directory (Azure AD) application in your Azure AD tenant, as mentioned in [Deployment guide for scale unit and workloads](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).</span></span>
    1. <span data-ttu-id="86eb5-175">作成されると、ハブの Azure AD アプリケーション フォーム (SysAADClientTable) に移動します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-175">Once created, navigate to the Azure AD applications form (SysAADClientTable) on your hub.</span></span>
    1. <span data-ttu-id="86eb5-176">新しいエントリを作成し、作成したアプリケーションの ID に **クライアント ID** を設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-176">Create a new entry and set the **Client ID** to the ID of the application you created.</span></span> <span data-ttu-id="86eb5-177">**名前** を *ScaleUnits*、**ユーザー ID** を *管理者* に設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-177">Set the **Name** to *ScaleUnits* and the **User ID** to *Admin*.</span></span>

1. <span data-ttu-id="86eb5-178">[スケール ユニットとワークロードの配置ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations) で説明したように、Active Directory フェデレーション サービス (AD FS) アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-178">Create an Active Directory Federation Service (AD FS) application as mentioned in [Deployment guide for scale unit and workloads](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).</span></span>
    1. <span data-ttu-id="86eb5-179">作成されると、エッジ スケール ユニットの Azure AD アプリケーション フォーム (SysAADClientTable) に移動します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-179">Once created, navigate to the Azure AD applications form (SysAADClientTable) on your edge scale unit.</span></span>
    1. <span data-ttu-id="86eb5-180">新しいエントリを作成し、作成したアプリケーションの ID に **クライアント ID** を設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-180">Create a new entry and set the **Client ID** to the ID of the application you created.</span></span> <span data-ttu-id="86eb5-181">**ユーザー ID** を *管理者* に設定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-181">Set the **User ID** to *Admin*.</span></span>

1. <span data-ttu-id="86eb5-182">`UserConfig.xml` ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-182">Modify the `UserConfig.xml` file.</span></span>
    1. <span data-ttu-id="86eb5-183">`InterAOSAADConfiguration` セクションで、以前作成した Azure AD アプリケーションからの情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-183">Under the `InterAOSAADConfiguration` section, enter the information from the Azure AD application you created previously.</span></span>
        - <span data-ttu-id="86eb5-184">`AppId` 要素に、Azure アプリケーションのアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-184">In the `AppId` element, enter the application ID of the Azure application.</span></span>
        - <span data-ttu-id="86eb5-185">`AppSecret` 要素に、Azure アプリケーションのアプリケーション シークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-185">In the `AppSecret` element, enter the application secret of the Azure application.</span></span>
        - <span data-ttu-id="86eb5-186">`Authority` 要素には、テナントのセキュリティ オーソリティを指定する URL が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-186">The `Authority` element must contain the URL specifying the security authority for your tenant.</span></span>

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. <span data-ttu-id="86eb5-187">`ScaleUnitConfiguration` セクションの最初の `ScaleUnitInstance` セクションで、`AuthConfiguration` セクションを変更します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-187">Under the `ScaleUnitConfiguration` section, for the first `ScaleUnitInstance`, modify the `AuthConfiguration` section.</span></span>
        - <span data-ttu-id="86eb5-188">`AppId` 要素に、Azure アプリケーションのアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-188">In the `AppId` element, enter the application ID of the Azure application.</span></span>
        - <span data-ttu-id="86eb5-189">`AppSecret` 要素に、Azure アプリケーションのアプリケーション シークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-189">In the `AppSecret` element, enter the application secret of the Azure application.</span></span>
        - <span data-ttu-id="86eb5-190">`Authority` 要素には、テナントのセキュリティ オーソリティを指定する URL が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-190">The `Authority` element must contain the URL specifying the security authority for your tenant.</span></span>

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. <span data-ttu-id="86eb5-191">また、これと同じ `ScaleUnitInstance` に、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="86eb5-191">Additionally, for this same `ScaleUnitInstance`, set the following values:</span></span>
        - <span data-ttu-id="86eb5-192">`Domain` 要素で、ハブの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-192">In the `Domain` element, specify the URL of your hub.</span></span> <span data-ttu-id="86eb5-193">例: `https://cloudhub.sandbox.operations.dynamics.com/`</span><span class="sxs-lookup"><span data-stu-id="86eb5-193">For example: `https://cloudhub.sandbox.operations.dynamics.com/`</span></span>
        - <span data-ttu-id="86eb5-194">`EnvironmentType` 要素で、値が `LCSHosted` に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-194">In the `EnvironmentType` element, ensure the value `LCSHosted` is set.</span></span>

    1. <span data-ttu-id="86eb5-195">`ScaleUnitConfiguration` セクションの 2 つ目の `ScaleUnitInstance` セクションで、`AuthConfiguration` セクションを変更します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-195">Under the `ScaleUnitConfiguration` section, for the second `ScaleUnitInstance`, modify the `AuthConfiguration` section.</span></span>
        - <span data-ttu-id="86eb5-196">`AppId` 要素に、AD FS アプリケーションのアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-196">In the `AppId` element, enter the application ID of the AD FS application.</span></span>
        - <span data-ttu-id="86eb5-197">`AppSecret` 要素に、ADFS アプリケーションのアプリケーション シークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-197">In the `AppSecret` element, enter the application secret of the ADFS application.</span></span>
        - <span data-ttu-id="86eb5-198">`Authority` 要素には、AD FS インスタンスの URL が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-198">The `Authority` element must contain the URL of your AD FS instance.</span></span>

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. <span data-ttu-id="86eb5-199">また、これと同じ `ScaleUnitInstance` に、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="86eb5-199">Additionally, for this same `ScaleUnitInstance`, set the following values:</span></span>
        - <span data-ttu-id="86eb5-200">`Domain` 要素で、エッジ スケール ユニットの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-200">In the `Domain` element, specify the URL of your edge scale unit.</span></span> <span data-ttu-id="86eb5-201">例: https://ax.contoso.com/</span><span class="sxs-lookup"><span data-stu-id="86eb5-201">For example: https://ax.contoso.com/</span></span>
        - <span data-ttu-id="86eb5-202">`EnvironmentType` 要素で、値が LBD に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-202">In the `EnvironmentType` element, ensure the value LBD is set.</span></span>
        - <span data-ttu-id="86eb5-203">`ScaleUnitId` 要素には、`Configure-CloudandEdge.ps1`  配置前スクリプトの構成時に `InstanceId` に指定した値と同じ値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-203">In the `ScaleUnitId` element, input the same value you specified for the `InstanceId` when configuring the `Configure-CloudandEdge.ps1` pre-deployment script.</span></span>

        > [!NOTE]
        > <span data-ttu-id="86eb5-204">既定の ID (@A) を使用しない場合、ワークロード セクションの各 ConfiguredWorkload に対して ScaleUnitId を更新してください。</span><span class="sxs-lookup"><span data-stu-id="86eb5-204">If you don't use the default Id (@A), ensure you update the ScaleUnitId for each ConfiguredWorkload under the Workloads section.</span></span>

1. <span data-ttu-id="86eb5-205">PowerShell を開き、`UserConfig.xml` ファイルを含むフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-205">Open PowerShell and navigate to the folder containing the `UserConfig.xml` file.</span></span>

1. <span data-ttu-id="86eb5-206">このコマンドを使用してツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-206">Run the tool with this command.</span></span>

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > <span data-ttu-id="86eb5-207">すべてのアクションの後、ツールを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86eb5-207">After every action you will have to start the tool again.</span></span>

1. <span data-ttu-id="86eb5-208">このツールで **2. ワークロードのインストールのための環境を準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-208">In the tool, select **2. Prepare environments for workload installation**.</span></span> <span data-ttu-id="86eb5-209">次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="86eb5-209">Then run the following steps:</span></span>
    1. <span data-ttu-id="86eb5-210">**1. ハブを準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-210">Select **1. Prepare the Hub**.</span></span>
    1. <span data-ttu-id="86eb5-211">**2. スケール ユニットを準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-211">Select **2. Prepare the Scale Unit**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86eb5-212">このコマンドをクリーン インストールから実行していない場合にエラーが発生した場合は、次の操作を行います:</span><span class="sxs-lookup"><span data-stu-id="86eb5-212">If you are not running this command from a clean installation and it fails, do the following actions:</span></span>
    >
    > - <span data-ttu-id="86eb5-213">`aos-storage` フォルダーからすべてのフォルダーを削除します (`GACAssemblies` を除く)。</span><span class="sxs-lookup"><span data-stu-id="86eb5-213">Remove all folders from the `aos-storage` folder (except for `GACAssemblies`).</span></span>
    > - <span data-ttu-id="86eb5-214">ビジネス データ データベース (AXDB) で次の SQL コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-214">Run the following SQL command on your business database (AXDB):</span></span>
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. <span data-ttu-id="86eb5-215">ビジネス データ データベース (AXDB) で次の SQL コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-215">Run the following SQL commands on your business database (AXDB):</span></span>

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. <span data-ttu-id="86eb5-216">ビジネス データベース (AXDB) で変更追跡が有効になっていることを確認</span><span class="sxs-lookup"><span data-stu-id="86eb5-216">Verify that change tracking has been enabled on your business database (AXDB)</span></span>
    1. <span data-ttu-id="86eb5-217">SQL Server Management Studio (SSMS) を開始します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-217">Start SQL Server Management Studio (SSMS).</span></span>
    1. <span data-ttu-id="86eb5-218">ビジネス データベース (AXDB) を右クリックし、プロパティ を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-218">Right-click your business database (AXDB) and select properties.</span></span>
    1. <span data-ttu-id="86eb5-219">開くウィンドウで **変更追跡** を選択し、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="86eb5-219">In the window that opens, select **Change Tracking** and make the following settings:</span></span>

        - <span data-ttu-id="86eb5-220">**変更追跡:** *True*</span><span class="sxs-lookup"><span data-stu-id="86eb5-220">**Change Tracking:** *True*</span></span>
        - <span data-ttu-id="86eb5-221">**留保期間:** *7*</span><span class="sxs-lookup"><span data-stu-id="86eb5-221">**Retention Period:** *7*</span></span>
        - <span data-ttu-id="86eb5-222">**留保単位:** *Days*</span><span class="sxs-lookup"><span data-stu-id="86eb5-222">**Retention Units:** *Days*</span></span>
        - <span data-ttu-id="86eb5-223">**自動クリーンアップ:** *True*</span><span class="sxs-lookup"><span data-stu-id="86eb5-223">**Auto Cleanup:** *True*</span></span>

1. <span data-ttu-id="86eb5-224">ツールで **3. ワークロードをインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-224">In the tool, select **3. Install workloads**.</span></span> <span data-ttu-id="86eb5-225">次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="86eb5-225">Then run the following steps:</span></span>
    1. <span data-ttu-id="86eb5-226">**1. ハブでインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-226">Select **1. Install on Hub**.</span></span>
    1. <span data-ttu-id="86eb5-227">**2. スケール ユニットでインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86eb5-227">Select **2. Install on Scale Unit**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
