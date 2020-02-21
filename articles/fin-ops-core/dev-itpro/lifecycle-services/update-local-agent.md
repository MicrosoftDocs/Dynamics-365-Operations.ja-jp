---
title: ローカル エージェントの更新
description: このトピックでは、ローカル エージェントを更新する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 161930d19f3408c2ebecd1b3796c94be69838ed3
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029420"
---
# <a name="update-the-local-agent"></a><span data-ttu-id="70793-103">ローカル エージェントの更新</span><span class="sxs-lookup"><span data-stu-id="70793-103">Update the local agent</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70793-104">このトピックでは、ローカル エージェントを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="70793-104">This topic explains how to update the local agent.</span></span> <span data-ttu-id="70793-105">ローカル エージェントの最新バージョンは、2019 年 12 月にリリースされたバージョン 2.4.0 です。</span><span class="sxs-lookup"><span data-stu-id="70793-105">The latest version of the local agent is version 2.4.0, which was released in December 2019.</span></span>

| <span data-ttu-id="70793-106">ローカル エージェントのバージョン</span><span class="sxs-lookup"><span data-stu-id="70793-106">Local agent version</span></span> | <span data-ttu-id="70793-107">能力</span><span class="sxs-lookup"><span data-stu-id="70793-107">Capability</span></span> | 
|---------------------|------------|
| <span data-ttu-id="70793-108">Null</span><span class="sxs-lookup"><span data-stu-id="70793-108">Null</span></span>                | <span data-ttu-id="70793-109">この初期バージョンでは、Platform update 8 が導入されています。</span><span class="sxs-lookup"><span data-stu-id="70793-109">This initial version deploys Platform update 8.</span></span> |
| <span data-ttu-id="70793-110">1.0.0</span><span class="sxs-lookup"><span data-stu-id="70793-110">1.0.0</span></span>               | <span data-ttu-id="70793-111">このバージョンでは、展開が失敗した場合のために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になります。</span><span class="sxs-lookup"><span data-stu-id="70793-111">This version enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) for failed deployments.</span></span> |
| <span data-ttu-id="70793-112">1.1.0</span><span class="sxs-lookup"><span data-stu-id="70793-112">1.1.0</span></span>               | <span data-ttu-id="70793-113">このバージョンでは、正常に展開するために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になり、複数モデルのパッケージ展開が可能になり、プラットフォーム更新プログラム 8 および 11 が展開されます。</span><span class="sxs-lookup"><span data-stu-id="70793-113">This version enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md)  for successful deployments, enables multi-model package deployments, and deploys Platform update 8 and 11.</span></span> | 
| <span data-ttu-id="70793-114">2.0.0</span><span class="sxs-lookup"><span data-stu-id="70793-114">2.0.0</span></span>               | <span data-ttu-id="70793-115">このバージョンでは、サービス フローが可能になり、プラットフォーム更新プログラム 12 が展開されます。</span><span class="sxs-lookup"><span data-stu-id="70793-115">This version enables servicing flows and deploys Platform update 12.</span></span> |
| <span data-ttu-id="70793-116">2.1.0</span><span class="sxs-lookup"><span data-stu-id="70793-116">2.1.0</span></span>               | <span data-ttu-id="70793-117">このバージョンでは、**準備**および**更新**が 2 つの個別のステップである 2 段階サービスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="70793-117">This version enables two-phased servicing where **Preparation** and **Update** are two separate steps.</span></span> |
| <span data-ttu-id="70793-118">2.1.1</span><span class="sxs-lookup"><span data-stu-id="70793-118">2.1.1</span></span>               | <span data-ttu-id="70793-119">このバージョンはダウンロードが失敗したときに発生する LCS 管理ボタンが利用できない問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="70793-119">This version fixes an issue that occurs when the download fails and the LCS Maintain button is not available.</span></span> <span data-ttu-id="70793-120">その他の変更には、Azure Storage との通信を改善し TLS 1.2 を有効にする Azure Storage ライブラリの更新を含みます。</span><span class="sxs-lookup"><span data-stu-id="70793-120">Additional changes include updates to Azure storage libraries to improve communication with Azure storage and enable TLS 1.2.</span></span>  |
| <span data-ttu-id="70793-121">2.1.2</span><span class="sxs-lookup"><span data-stu-id="70793-121">2.1.2</span></span>               | <span data-ttu-id="70793-122">このバージョンには、更新されたAzure依存関係が含まれており、ダウンロードの安定性を向上し、ファイルがダウンロードされた場合に正しく評価するロジックを使用</span><span class="sxs-lookup"><span data-stu-id="70793-122">This version contains updated Azure dependencies for improved download stability and logic to correctly evaluate if files are downloaded.</span></span> <span data-ttu-id="70793-123">これにより、ファイルが完全にダウンロードされるという問題が修正されますが、論理上数バイトが不足していると見なされ、ダウンロードに失敗します。</span><span class="sxs-lookup"><span data-stu-id="70793-123">This fixes an issue where files are fully downloaded, but the logic would still consider them as missing a few bytes and therefore fail the download.</span></span>  |
| <span data-ttu-id="70793-124">2.2.0</span><span class="sxs-lookup"><span data-stu-id="70793-124">2.2.0</span></span>               | <span data-ttu-id="70793-125">このバージョンでは、クリーンアップ中にロックされた dll を修正し、Office 365 でも使用される Active Directory フェデレーション サービス (ADFS) をサポートするための前提条件を有効にします。</span><span class="sxs-lookup"><span data-stu-id="70793-125">This version fixes locked dlls during cleanup and enables prerequisites for supporting Active Directory Federation Services (ADFS) that also is used for Office 365.</span></span> |
| <span data-ttu-id="70793-126">2.3.0</span><span class="sxs-lookup"><span data-stu-id="70793-126">2.3.0</span></span>               | <span data-ttu-id="70793-127">このバージョンに、配置前スクリプトと配置後スクリプトのサポートが追加されます。</span><span class="sxs-lookup"><span data-stu-id="70793-127">This version adds support for pre- and post-deployment scripts.</span></span>  |
| <span data-ttu-id="70793-128">2.3.1</span><span class="sxs-lookup"><span data-stu-id="70793-128">2.3.1</span></span>               | <span data-ttu-id="70793-129">このバージョンでは、一部の環境でのクリーンアップ中に発生する可能性があるオーケストレーション サービスのクラッシュを修正します。</span><span class="sxs-lookup"><span data-stu-id="70793-129">This version fixes orchestration service crashes that may occur during clean up on some environments.</span></span><br><br><span data-ttu-id="70793-130">プラットフォーム更新プログラム 29 以前のバージョン 10.0.5 を展開するには、FinancialReportingDeployer.exe.config. の自動更新に事前配置スクリプトを使用する必要があります。詳細については、[オンプレミス展開のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md#FREntityFramework)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70793-130">Deploying version 10.0.5 with Platform update 29 or earlier requires the use of pre-deployment scripts for automatic updating of FinancialReportingDeployer.exe.config. For more information, see [Troubleshoot on-premises deployments](../../dev-itpro/deployment/troubleshoot-on-prem.md#FREntityFramework).</span></span> |
| <span data-ttu-id="70793-131">2.4.0</span><span class="sxs-lookup"><span data-stu-id="70793-131">2.4.0</span></span>               | <span data-ttu-id="70793-132">このバージョンでは、展開の問題が修正され、ローカル エージェントのランタイムがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="70793-132">This version fixes a deployment issue and upgrades the runtime of the local agent.</span></span> |

## <a name="whats-new-in-local-agent-240"></a><span data-ttu-id="70793-133">ローカル エージェント 2.4.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="70793-133">What's new in local agent 2.4.0</span></span>

- <span data-ttu-id="70793-134">ローカル エージェント 2.4.0 では、Lifecycle Services (LCS) から最新の変更を取り込むために .Net Framework 4.8 が必要になりました。</span><span class="sxs-lookup"><span data-stu-id="70793-134">Local agent 2.4.0 now requires .Net Framework 4.8 to uptake the newest changes from Lifecycle Services (LCS).</span></span> <span data-ttu-id="70793-135">最新の要件を満たすために、LCS で利用可能な最新のインフラストラクチャ スクリプトを実行してください。</span><span class="sxs-lookup"><span data-stu-id="70793-135">Please be sure to run the latest Infrastructure Scripts available in LCS to meet the newest requirements.</span></span>
- <span data-ttu-id="70793-136">このリリースでは、AXSFType の展開時に展開が終了した AOSSetupHybridCloud.exe の 255/-1 終了エラーも修正されます。</span><span class="sxs-lookup"><span data-stu-id="70793-136">This release also fixes the 255/-1 exit error from the AOSSetupHybridCloud.exe where the deployment ended when deploying the AXSFType.</span></span>

## <a name="whats-new-in-local-agent-230"></a><span data-ttu-id="70793-137">ローカル エージェント 2.3.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="70793-137">What's new in local agent 2.3.0</span></span>

- <span data-ttu-id="70793-138">ローカル エージェント 2.3.0 は、カスタム実行を有効にします [配置前および配置後のスクリプト](../../dev-itpro/lifecycle-services/pre-post-scripts.md)。</span><span class="sxs-lookup"><span data-stu-id="70793-138">Local agent 2.3.0 enables the execution of custom [pre- and post- deployment scripts](../../dev-itpro/lifecycle-services/pre-post-scripts.md).</span></span>
- <span data-ttu-id="70793-139">これは、古いプラットフォーム更新プログラムの展開に関して 2.2.0 で採用された問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="70793-139">It fixes the problem introduced in 2.2.0 with regard to deploying older platform updates.</span></span>
- <span data-ttu-id="70793-140">このリリースでは、監視エージェントを削除して LBDTelemetry という新しいサービスを導入し、これを ETWManifests のインストールの際に使用します。</span><span class="sxs-lookup"><span data-stu-id="70793-140">This release removes the monitoring agent and introduces a new service called LBDTelemetry, which will be used to install the ETWManifests.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="70793-141">このリリースでは、LCS から新しいローカル エージェント構成ファイルをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="70793-141">This release requires that a new local agent configuration file be downloaded from LCS.</span></span> <span data-ttu-id="70793-142">問題が発生した場合は、[オンプレミス配置のトラブルシューティング](../../dev-itpro/deployment/troubleshoot-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70793-142">Refer to the [Troubleshoot on-premises deployments](../../dev-itpro/deployment/troubleshoot-on-prem.md) topic if you encounter problems.</span></span> 

## <a name="whats-new-in-local-agent-210"></a><span data-ttu-id="70793-143">ローカル エージェント 2.1.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="70793-143">What's new in local agent 2.1.0</span></span>
- <span data-ttu-id="70793-144">ローカル エージェント 2.1.0 では、**環境の準備**および**環境の更新**が 2 つの異なる手順および明示的アクションである 2 フェーズのサービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="70793-144">Local agent 2.1.0 enables the two-phased servicing where **Environment preparation** and **Environment update** are two distinct steps and explicit actions.</span></span> <span data-ttu-id="70793-145">事前準備を行い、ユーザーが準備中に環境を使用できるようにし、実際の更新環境アクションが発生する際にダウンタイムを通知することで、オンプレミス環境に更新プログラムを適用する場合に顧客が取る必要があるダウンタイムの合計が削減されます。</span><span class="sxs-lookup"><span data-stu-id="70793-145">This reduces the total downtime customers must take when applying updates to their on-premises environments by preparing upfront and allowing users to use the environment during preparation and then communicating the downtime when the actual update environment action is triggered.</span></span>

## <a name="whats-new-in-local-agent-200"></a><span data-ttu-id="70793-146">ローカル エージェント 2.0.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="70793-146">What's new in local agent 2.0.0</span></span>
- <span data-ttu-id="70793-147">ローカル エージェント 2.0.0 はプラットフォーム更新プログラム 12 を展開できます。</span><span class="sxs-lookup"><span data-stu-id="70793-147">Local agent 2.0.0 can deploy Platform update 12.</span></span>
- <span data-ttu-id="70793-148">プラットフォーム更新 12 の配置の初回成功まで、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は有効になります。</span><span class="sxs-lookup"><span data-stu-id="70793-148">It enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) until the first deployment of Platform update 12 succeeds.</span></span>
- <span data-ttu-id="70793-149">プラットフォーム更新 12 の配置の初回成功時は、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は無効になります。</span><span class="sxs-lookup"><span data-stu-id="70793-149">It disables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) on the first successful deployment of Platform update 12.</span></span> <span data-ttu-id="70793-150">配置が成功した後、定期的な更新エクスペリエンスを使用して環境を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="70793-150">After deployment succeeds, you can use the regular update experience to update the environment.</span></span>

> [!NOTE]
> <span data-ttu-id="70793-151">ローカル エージェント 2.0.0 は、プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11 を展開**できません**。</span><span class="sxs-lookup"><span data-stu-id="70793-151">Local agent 2.0.0 **cannot** deploy Platform update 8 and Platform update 11.</span></span> <span data-ttu-id="70793-152">プラットフォーム更新プログラムを展開するには、バージョン 1.1.0 が必要です。</span><span class="sxs-lookup"><span data-stu-id="70793-152">You must have version 1.1.0 to deploy those platform updates.</span></span>

## <a name="download-the-latest-local-agent-and-configuration-from-lcs"></a><span data-ttu-id="70793-153">LCS から最新のローカル エージェントおよびコンフィギュレーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="70793-153">Download the latest local agent and configuration from LCS</span></span>

> [!NOTE]
> <span data-ttu-id="70793-154">現在の配置では、ローカル エージェントの以前のバージョンを要求する場合は、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリからそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="70793-154">If you require an older version of the local agent for your current deployments, download it from the Asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="70793-155">ローカル エージェント バージョン v1.1.0 をダウンロードするには、**共用資産ライブラリ - >モデル**に移動し、Dynamics 365 for Finance and Operations オンプレミス - ローカル エージェント v1.1.0\*\* をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70793-155">To download Local agent version 1.1.0, go to **Shared Asset Library -> Model** and click on Dynamics 365 for Finance and Operations on-premises - Local agent v1.1.0\*\*.</span></span>
>
> <span data-ttu-id="70793-156">プラットフォーム更新プログラム 12 の展開および更新プログラム フローの完成には、バージョン 2.0.0 かそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="70793-156">You must have version 2.0.0 or later to deploy Platform update 12 and complete update flows.</span></span>

1. <span data-ttu-id="70793-157">LCS で、**プロジェクト設定** > **オンプレミス コネクタ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="70793-157">In LCS, select **Project settings** > **On-prem connectors**.</span></span>
2. <span data-ttu-id="70793-158">環境へのコネクタを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70793-158">Select the connector to your environment, and then select **Edit**.</span></span>
3. <span data-ttu-id="70793-159">ページの左側にあるメニューの、**ホスト インフラストラクチャ設定**を選択し、**エージェント インストーラーのダウンロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="70793-159">On the menu on the left side of the page, select **Setup host infrastructure**, and then select **Download agent installer**.</span></span>

    <span data-ttu-id="70793-160">この時点で、zip ファイルがダウンロードされ、かつブロックされていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70793-160">You must now verify that the zip file that is downloaded and unblocked.</span></span>

4. <span data-ttu-id="70793-161">zip ファイルに移動し、右クリックして **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="70793-161">Go to the zip file, right-click it, and then select **Properties**.</span></span>
5. <span data-ttu-id="70793-162">**プロパティ** ダイアログ ボックスで、**ブロック解除**を選択してから**適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="70793-162">In the **Properties** dialog box, select **Unblock**, and then select **Apply**.</span></span>
6. <span data-ttu-id="70793-163">**エージェントのコンフィギュレーション**タブで、**コンフィギュレーションのダウンロード**を選択し、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="70793-163">On the **Configure agent** tab, select **Download configurations** to download the localagent-config.json configuration file.</span></span>

## <a name="update-the-local-agent"></a><span data-ttu-id="70793-164">ローカル エージェントの更新</span><span class="sxs-lookup"><span data-stu-id="70793-164">Update the local agent</span></span>

1. <span data-ttu-id="70793-165">ZIP ファイルと localagent-config.json ファイルを、**Orch1** 仮想マシン (VM) の **c:\\DynamicsAgent** などの、**Orchestrator** ノードの 1 つにコピーします。</span><span class="sxs-lookup"><span data-stu-id="70793-165">Copy the zip file and the localagent-config.json file into one of the **Orchestrator** nodes, such as **c:\\DynamicsAgent** in the **Orch1** virtual machine (VM).</span></span>
2. <span data-ttu-id="70793-166">エージェント インストーラを C:\\DynamicsAgent\\LocalAgent に解凍します。</span><span class="sxs-lookup"><span data-stu-id="70793-166">Unzip the agent installer to C:\\DynamicsAgent\\LocalAgent.</span></span>
3. <span data-ttu-id="70793-167">localagent-config.json ファイルを \\DynamicsAgent\\LocalAgent にコピーします。</span><span class="sxs-lookup"><span data-stu-id="70793-167">Copy the localagent-config.json file to C:\\DynamicsAgent\\LocalAgent.</span></span>
4. <span data-ttu-id="70793-168">**コマンド プロンプト** ウィンドウで、C:\\DynamicsAgent\\LocalAgent に移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70793-168">In a **Command Prompt** window, go to C:\\DynamicsAgent\\LocalAgent, and run the following command.</span></span>

    ```Console
    LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="70793-169">エージェントをクリーンアップするには、現在のエージェントのバイナリ ファイルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70793-169">You must use the current agent's binaries to clean up the agent.</span></span> <span data-ttu-id="70793-170">現在のエージェントのバイナリ ファイルがない場合は、Service Fabric Explorer からローカル エージェント アプリケーションを削除できます。</span><span class="sxs-lookup"><span data-stu-id="70793-170">If you don't have the current agent's binaries, you can delete the local agent application from Service Fabric Explorer.</span></span>

5. <span data-ttu-id="70793-171">クリーンアップ操作を終了するには、任意のキーを押します。</span><span class="sxs-lookup"><span data-stu-id="70793-171">Press any key to exit the cleanup operation.</span></span>
6. <span data-ttu-id="70793-172">Service Fabric Explorer を調べ、**Orchestrator** ノードの **展開済みアプリケーション** セクションにアプリケーションがないことを確めて、ローカル エージェントが正常にクリーンアップされことを確認します。</span><span class="sxs-lookup"><span data-stu-id="70793-172">Verify that the local agent has been successfully cleaned up by looking in Service Fabric Explorer and making sure that there are no apps in the **Deployed Applications** section in the **Orchestrator** nodes.</span></span>
7. <span data-ttu-id="70793-173">ローカル エージェントが正常にクリーンアップされた後は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="70793-173">After the local agent is successfully cleaned up, run the following command.</span></span>

    ```Console
    LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

8. <span data-ttu-id="70793-174">ローカル エージェントが正常にインストールされてから、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="70793-174">After the local agent is successfully installed, go back to your on-premises connector in LCS.</span></span>
9. <span data-ttu-id="70793-175">**設定の検証**タブで、**メッセージ エージェント**を選択して、新しいローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="70793-175">On the **Validate setup** tab, select **Message agent** to test LCS connectivity to your new local agent.</span></span>
