---
title: ローカル エージェントの更新
description: このトピックでは、ローカル エージェントを更新する方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 07/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-12-05
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4624d97d79cf8cd9706cf2a9d85560b48cc2e2ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369014"
---
# <a name="update-the-local-agent"></a><span data-ttu-id="0e530-103">ローカル エージェントの更新</span><span class="sxs-lookup"><span data-stu-id="0e530-103">Update the local agent</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e530-104">このトピックでは、ローカル エージェントを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0e530-104">This topic explains how to update the local agent.</span></span> <span data-ttu-id="0e530-105">ローカル エージェントの最新バージョンはバージョン 2.0.0で、2018 年 3 月にリリースされました。</span><span class="sxs-lookup"><span data-stu-id="0e530-105">The latest version of the local agent is version 2.0.0, which was released in March 2018.</span></span>

| <span data-ttu-id="0e530-106">ローカル エージェントのバージョン</span><span class="sxs-lookup"><span data-stu-id="0e530-106">Local agent version</span></span> | <span data-ttu-id="0e530-107">能力</span><span class="sxs-lookup"><span data-stu-id="0e530-107">Capability</span></span> | 
|---------------------|------------|
| <span data-ttu-id="0e530-108">Null</span><span class="sxs-lookup"><span data-stu-id="0e530-108">Null</span></span>                | <span data-ttu-id="0e530-109">この初期バージョンでは、Platform update 8 が導入されています。</span><span class="sxs-lookup"><span data-stu-id="0e530-109">This initial version deploys Platform update 8.</span></span> |
| <span data-ttu-id="0e530-110">1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e530-110">1.0.0</span></span>               | <span data-ttu-id="0e530-111">このバージョンでは、展開が失敗した場合のために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e530-111">This version enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) for failed deployments.</span></span> |
| <span data-ttu-id="0e530-112">1.1.0</span><span class="sxs-lookup"><span data-stu-id="0e530-112">1.1.0</span></span>               | <span data-ttu-id="0e530-113">このバージョンでは、正常に展開するために[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)が有効になり、複数モデルのパッケージ展開が可能になり、プラットフォーム更新プログラム 8 および 11 が展開されます。</span><span class="sxs-lookup"><span data-stu-id="0e530-113">This version enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md)  for successful deployments, enables multi-model package deployments, and deploys Platform update 8 and 11.</span></span> | 
| <span data-ttu-id="0e530-114">200</span><span class="sxs-lookup"><span data-stu-id="0e530-114">2.0.0</span></span>               | <span data-ttu-id="0e530-115">このバージョンでは、サービス フローが可能になり、プラットフォーム更新プログラム 12 が展開されます。</span><span class="sxs-lookup"><span data-stu-id="0e530-115">This version enables servicing flows and deploys Platform update 12.</span></span> |
| <span data-ttu-id="0e530-116">2.1.0</span><span class="sxs-lookup"><span data-stu-id="0e530-116">2.1.0</span></span>               | <span data-ttu-id="0e530-117">このバージョンでは、**準備**および**更新**が 2 つの個別のステップである 2 段階サービスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="0e530-117">This version enables two-phased servicing where **Preparation** and **Update** are two separate steps.</span></span> |

## <a name="whats-new-in-local-agent-210"></a><span data-ttu-id="0e530-118">Local agent 2.1.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="0e530-118">What's new in local agent 2.1.0?</span></span>
- <span data-ttu-id="0e530-119">ローカル エージェント 2.1.0 では、**環境の準備**および**環境の更新**が 2 つの異なる手順および明示的アクションである 2 フェーズのサービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0e530-119">Local agent 2.1.0 enables the two-phased servicing where **Environment preparation** and **Environment update** are two distinct steps and explicit actions.</span></span> <span data-ttu-id="0e530-120">事前準備を行い、ユーザーが準備中に環境を使用できるようにし、実際の更新環境アクションが発生する際にダウンタイムを通知することで、オンプレミス環境に更新プログラムを適用する場合に顧客が取る必要があるダウンタイムの合計が削減されます。</span><span class="sxs-lookup"><span data-stu-id="0e530-120">This reduces the total downtime customers must take when applying updates to their on-premises environments by preparing upfront and allowing users to use the environment during preparation and then communicating the downtime when the actual update environment action is triggered.</span></span>

## <a name="whats-new-in-local-agent-200"></a><span data-ttu-id="0e530-121">Local agent 2.0.0 の新機能</span><span class="sxs-lookup"><span data-stu-id="0e530-121">What's new in local agent 2.0.0?</span></span>
- <span data-ttu-id="0e530-122">ローカル エージェント 2.0.0 はプラットフォーム更新プログラム 12 を展開できます。</span><span class="sxs-lookup"><span data-stu-id="0e530-122">Local agent 2.0.0 can deploy Platform update 12.</span></span>
- <span data-ttu-id="0e530-123">プラットフォーム更新 12 の配置の初回成功まで、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e530-123">It enables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) until the first deployment of Platform update 12 succeeds.</span></span>
- <span data-ttu-id="0e530-124">プラットフォーム更新 12 の配置の初回成功時は、[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は無効になります。</span><span class="sxs-lookup"><span data-stu-id="0e530-124">It disables the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) on the first successful deployment of Platform update 12.</span></span> <span data-ttu-id="0e530-125">配置が成功した後、定期的な更新エクスペリエンスを使用して環境を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="0e530-125">After deployment succeeds, you can use the regular update experience to update the environment.</span></span>

> [!NOTE]
> <span data-ttu-id="0e530-126">ローカル エージェント 2.0.0 は、プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11 を展開**できません**。</span><span class="sxs-lookup"><span data-stu-id="0e530-126">Local agent 2.0.0 **cannot** deploy Platform update 8 and Platform update 11.</span></span> <span data-ttu-id="0e530-127">プラットフォーム更新プログラムを展開するには、バージョン 1.1.0 が必要です。</span><span class="sxs-lookup"><span data-stu-id="0e530-127">You must have version 1.1.0 to deploy those platform updates.</span></span>

## <a name="download-the-latest-local-agent-and-configuration-from-lcs"></a><span data-ttu-id="0e530-128">LCS から最新のローカル エージェントおよびコンフィギュレーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="0e530-128">Download the latest local agent and configuration from LCS</span></span>

> [!NOTE]
> <span data-ttu-id="0e530-129">現在の配置では、ローカル エージェントの以前のバージョンを要求する場合は、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリからそれをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0e530-129">If you require an older version of the local agent for your current deployments, download it from the Asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0e530-130">ローカルエージェント v1.1.0 をダウンロードするには、**共用資産ライブラリ - >モデル に移動し、Dynamics 365 for Finance and Operations オンプレミス - ローカルエージェント v1.1.0 をクリックします。**</span><span class="sxs-lookup"><span data-stu-id="0e530-130">To download Local agent v1.1.0 navigate to **Shared Asset Library -> Model and click on Dynamics 365 for Finance and Operations on-premises - Local agent v1.1.0**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e530-131">プラットフォーム更新プログラム 12 の展開および更新プログラム フローの完成には、バージョン 2.0.0 かそれ以降のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="0e530-131">You must have version 2.0.0 or later to deploy Platform update 12 and complete update flows.</span></span>

1. <span data-ttu-id="0e530-132">LCS で、**プロジェクト設定** &gt; **オンプレミス コネクタ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e530-132">In LCS, select **Project settings** &gt; **On-prem connectors**.</span></span>
2. <span data-ttu-id="0e530-133">環境へのコネクタを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e530-133">Select the connector to your environment, and then select **Edit**.</span></span>
3. <span data-ttu-id="0e530-134">ページの左側にあるメニューの、**ホスト インフラストラクチャ設定**を選択し、**エージェント インストーラーのダウンロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e530-134">On the menu on the left side of the page, select **Setup host infrastructure**, and then select **Download agent installer**.</span></span>

    <span data-ttu-id="0e530-135">この時点で、ダウンロードする ZIP ファイルがブロックされていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e530-135">You must now verify that the zip file that is downloaded is unblocked.</span></span>

4. <span data-ttu-id="0e530-136">zip ファイルに移動し、右クリックして**プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e530-136">Navigate to the zip file, right-click it, and then select **Properties**.</span></span>
5. <span data-ttu-id="0e530-137">**プロパティ** ダイアログ ボックスで、**ブロック解除**を選択してから**適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e530-137">In the **Properties** dialog box, select **Unblock**, and then select **Apply**.</span></span>
6. <span data-ttu-id="0e530-138">**エージェントのコンフィギュレーション**タブで、**コンフィギュレーションのダウンロード**を選択し、localagent-config.json コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0e530-138">On the **Configure agent** tab, select **Download configurations** to download the localagent-config.json configuration file.</span></span>

## <a name="update-the-local-agent"></a><span data-ttu-id="0e530-139">ローカル エージェントの更新</span><span class="sxs-lookup"><span data-stu-id="0e530-139">Update the local agent</span></span>

1. <span data-ttu-id="0e530-140">ZIP ファイルと localagent-config.json ファイルを、**Orch1** 仮想マシン (VM) の **c:\\DynamicsAgent** などの、**Orchestrator** ノードの 1 つにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e530-140">Copy the zip file and the localagent-config.json file into one of the **Orchestrator** nodes, such as **c:\\DynamicsAgent** in the **Orch1** virtual machine (VM).</span></span>
2. <span data-ttu-id="0e530-141">エージェント インストーラを C:\\DynamicsAgent\\LocalAgent に解凍します。</span><span class="sxs-lookup"><span data-stu-id="0e530-141">Unzip the agent installer to C:\\DynamicsAgent\\LocalAgent.</span></span>
3. <span data-ttu-id="0e530-142">localagent-config.json ファイルを \\DynamicsAgent\\LocalAgent にコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e530-142">Copy the localagent-config.json file to C:\\DynamicsAgent\\LocalAgent.</span></span>
4. <span data-ttu-id="0e530-143">**コマンド プロンプト** ウィンドウで、C:\\DynamicsAgent\\LocalAgent に移動して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e530-143">In a **Command Prompt** window, navigate to C:\\DynamicsAgent\\LocalAgent, and run the following command.</span></span>

    ```
    LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

    > [!NOTE]
    > <span data-ttu-id="0e530-144">エージェントをクリーンアップするには、現在のエージェントのバイナリ ファイルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e530-144">You must use the current agent's binaries to clean up the agent.</span></span> <span data-ttu-id="0e530-145">現在のエージェントのバイナリ ファイルがない場合は、Service Fabric Explorer からローカル エージェント アプリケーションを削除できます。</span><span class="sxs-lookup"><span data-stu-id="0e530-145">If you don't have the current agent's binaries, you can delete the local agent application from Service Fabric Explorer.</span></span>

5. <span data-ttu-id="0e530-146">クリーンアップ操作を終了するには、任意のキーを押します。</span><span class="sxs-lookup"><span data-stu-id="0e530-146">Press any key to exit the cleanup operation.</span></span>
6. <span data-ttu-id="0e530-147">Service Fabric Explorer を調べ、**Orchestrator** ノードの **展開済みアプリケーション** セクションにアプリケーションがないことを確めて、ローカル エージェントが正常にクリーンアップされことを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e530-147">Verify that the local agent has been successfully cleaned up by looking in Service Fabric Explorer and making sure that there are no apps in the **Deployed Applications** section in the **Orchestrator** nodes.</span></span>
7. <span data-ttu-id="0e530-148">ローカル エージェントが正常にクリーンアップされた後は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e530-148">After the local agent is successfully cleaned up, run the following command.</span></span>

    ```
    LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

8. <span data-ttu-id="0e530-149">ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。</span><span class="sxs-lookup"><span data-stu-id="0e530-149">After the local agent is successfully installed, navigate back to your on-premises connector in LCS.</span></span>
9. <span data-ttu-id="0e530-150">**設定の検証**タブで、**メッセージ エージェント**を選択して、新しいローカル エージェントへの LCS 接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="0e530-150">On the **Validate setup** tab, select **Message agent** to test LCS connectivity to your new local agent.</span></span>
