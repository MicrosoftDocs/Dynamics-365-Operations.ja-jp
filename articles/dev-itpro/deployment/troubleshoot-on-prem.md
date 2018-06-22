---
title: "Dynamics 365 for Finance and Operations (オンプレミス) のトラブルシューティング"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のトラブルシューティング情報を提供します。"
author: sarvanisathish
manager: AnnBe
ms.date: 03/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: f05da8a79dd07fcd8bf98bfd8a5e510d81b61384
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="troubleshoot-dynamics-365-for-finance-and-operations-on-premises"></a><span data-ttu-id="00678-103">Dynamics 365 for Finance and Operations (オンプレミス) のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="00678-103">Troubleshoot Dynamics 365 for Finance and Operations on-premises</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="00678-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations におけるオンプレミス展開のトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="00678-104">This topic provides troubleshooting information for on-premises deployments of Dynamics 365 for Finance and Operations.</span></span>

## <a name="error-when-signing-in-to-on-premises-environments"></a><span data-ttu-id="00678-105">オンプレミス環境へのログイン時のエラー</span><span class="sxs-lookup"><span data-stu-id="00678-105">Error when signing in to on-premises environments</span></span>

<span data-ttu-id="00678-106">PU12 [システム管理] > [設定] > [クライアントのパフォーマンス フォーム オプション] に移動して、"Skype 統合" を無効にしてください。</span><span class="sxs-lookup"><span data-stu-id="00678-106">PU12 Please turn off the "Skype Integration" by navigating to the System Administration > Setup > Client performance options form.</span></span>
<span data-ttu-id="00678-107">アプリに移動するとき、https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true の例のように、?debug=true を追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-107">When navigating to the app, append ?debug=true as shown in the following example https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true</span></span>

<span data-ttu-id="00678-108">PU8 および PU11 オンプレミス環境へのサインイン機能に影響を与える Skype API の問題が検出されました。</span><span class="sxs-lookup"><span data-stu-id="00678-108">PU8 and PU11 A Skype API issue has been discovered that is impacting the ability to sign in to on-premises environments.</span></span> <span data-ttu-id="00678-109">この問題の解決方法を調査しています。</span><span class="sxs-lookup"><span data-stu-id="00678-109">We are investigating a resolution for this issue.</span></span> <span data-ttu-id="00678-110">しばらくは、この問題を回避するために、次の例のように URL の末尾に **?debug = true** を追加できます。</span><span class="sxs-lookup"><span data-stu-id="00678-110">In the meantime, to work around this issue, you can add **?debug=true** to the end of your URL, as shown in the following example:</span></span>

`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`

## <a name="service-fabric"></a><span data-ttu-id="00678-111">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="00678-111">Service Fabric</span></span> 
<span data-ttu-id="00678-112">Service Fabric は、オンプレミス展開のためにインストールおよび構成する初期コンポーネントの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="00678-112">Service Fabric is one of the initial components to install and configure for your on-premises deployment.</span></span> <span data-ttu-id="00678-113">Service Fabric は、オーケストレータ、Application Object Server (AOS)、SSRS、および MR ノードで使用されます。</span><span class="sxs-lookup"><span data-stu-id="00678-113">Service Fabric is used by the Orchestrator, Application Object Server (AOS), SSRS and MR nodes.</span></span>

## <a name="access-service-fabric-explorer"></a><span data-ttu-id="00678-114">Service Fabric Explorer へのアクセス</span><span class="sxs-lookup"><span data-stu-id="00678-114">Access Service Fabric Explorer</span></span>
<span data-ttu-id="00678-115">Service Fabric Explorer には、ブラウザーと既定のアドレス https://sf.d365ffo.onprem.contoso.com:19080 を使ってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="00678-115">Service Fabric Explorer can be accessed by using a browser and the default address, https://sf.d365ffo.onprem.contoso.com:19080.</span></span>

<span data-ttu-id="00678-116">アドレスを確認するには、[DNS ゾーンの作成] セクションで使用した内容をメモし、環境に適したトピックに A レコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-116">To verify the address, note what was used in the section Create DNS zones and add A records in the appropriate topic for your environment:</span></span> 
- <span data-ttu-id="00678-117">[プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#createdns).</span><span class="sxs-lookup"><span data-stu-id="00678-117">[Platform update 12](setup-deploy-on-premises-pu12.md#createdns).</span></span>
- <span data-ttu-id="00678-118">[プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#createdns)</span><span class="sxs-lookup"><span data-stu-id="00678-118">[Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#createdns).</span></span>

<span data-ttu-id="00678-119">サイトにアクセスするには、クライアント証明書がサイトにアクセスしているマシンの `cert:\CurrentUser\My` (**証明書 - 現在のユーザー** > **個人** > **証明書**) にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-119">To access the site, the client certificate needs to be in `cert:\CurrentUser\My` (**Certificates - Current User** > **Personal** > **Certificates**) of the machine that is accessing the site.</span></span> <span data-ttu-id="00678-120">サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="00678-120">When you access the site, select the client certificate when prompted.</span></span>

## <a name="locate-logs-for-deployment-diagnostics"></a><span data-ttu-id="00678-121">配置の診断のログを検索します。</span><span class="sxs-lookup"><span data-stu-id="00678-121">Locate logs for deployment diagnostics</span></span>

<span data-ttu-id="00678-122">LocalAgent が稼動する各オーケストレーター マシンの責任を調べるには、[[ログ レビューのためのノードの特定方法]](#stateful-and-stateless-services-how-to-identify-nodes-for-log-review) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-122">To find out what responsibility each of the orchestrator machines (on which the LocalAgent runs on) have, please see the ["how to identify nodes for log review" section](#stateful-and-stateless-services-how-to-identify-nodes-for-log-review).</span></span>

### <a name="deployment-failure-logs"></a><span data-ttu-id="00678-123">配置の失敗ログ</span><span class="sxs-lookup"><span data-stu-id="00678-123">Deployment failure logs</span></span>

#### <a name="orchestrator-machine-failures"></a><span data-ttu-id="00678-124">オーケストレータ コンピューター エラー</span><span class="sxs-lookup"><span data-stu-id="00678-124">Orchestrator machine failures</span></span>

<span data-ttu-id="00678-125">展開中の `fabric:/LocalAgent/ArtifactsManager` および `fabric:/LocalAgent/OrchestrationService` 下の主要なノードは、最上位の利息です。</span><span class="sxs-lookup"><span data-stu-id="00678-125">During deployment, the primary nodes under `fabric:/LocalAgent/ArtifactsManager` and `fabric:/LocalAgent/OrchestrationService` are of the highest interest.</span></span> <span data-ttu-id="00678-126">それぞれで、イベント ビューアーを開き、展開済みの配置プロセスに関する情報およびエラーについては、`Applications and Services Logs\Microsoft\Dynamics\AX-LocalAgent\Operational` に移動してください。</span><span class="sxs-lookup"><span data-stu-id="00678-126">On each of them, open the Event Viewer and go to `Applications and Services Logs\Microsoft\Dynamics\AX-LocalAgent\Operational` for information and errors about the deployment process as it unfolds.</span></span>

<span data-ttu-id="00678-127">特に、`OrchestrationService` の場合、次のイベントの場所は AX のインストール中に展開に失敗した場合に調査する必要があります: `Applications and Services Logs\Microsoft\Dynamics\AX-SetupModuleEvents\Operational`。</span><span class="sxs-lookup"><span data-stu-id="00678-127">Particularly for the `OrchestrationService`, the following event location should be studied in the case of a deployment failure during AX installation: `Applications and Services Logs\Microsoft\Dynamics\AX-SetupModuleEvents\Operational`.</span></span>

#### <a name="ax-deployment-failures"></a><span data-ttu-id="00678-128">AX の配置の失敗</span><span class="sxs-lookup"><span data-stu-id="00678-128">AX deployment failures</span></span>

<span data-ttu-id="00678-129">AX が Service Fabric で "InBuild" のときは、データベースが最新の状態ではないことが検出された場合、AX は DbSync を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-129">When AX is "InBuild" in Service Fabric, it will execute a DbSync if it finds that the database is not up to date.</span></span> <span data-ttu-id="00678-130">DbSync は、さまざまな理由で失敗する可能性があります。その多くについてはこの記事で扱います。</span><span class="sxs-lookup"><span data-stu-id="00678-130">The DbSync can fail for a number of reasons, of which many are covered by this article.</span></span>

<span data-ttu-id="00678-131">DbSync エラーを診断するには、`Applications and Services Logs\Microsoft\Dynamics\AX-DatabaseSynchronize\Operational` にあるイベント ログを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-131">To diagnose DbSync errors, please see the event log located at: `Applications and Services Logs\Microsoft\Dynamics\AX-DatabaseSynchronize\Operational`.</span></span> <span data-ttu-id="00678-132">エラーの詳細は、この記事で役立つセクションを見つけるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="00678-132">The error details will help you find useful sections in this article.</span></span>

## <a name="stateful-and-stateless-services-how-to-identify-nodes-for-log-review"></a><span data-ttu-id="00678-133">ステートフルおよびステートレス サービス。ログ レビューのノードを識別する方法</span><span class="sxs-lookup"><span data-stu-id="00678-133">Stateful and stateless services, how to identify nodes for log review</span></span>
<span data-ttu-id="00678-134">どんなマシンがローカル エージェントのようなステートフル サービスのプライマリ インスタンスであるかを確認するには、Service Fabric Explorer を開き、**クラスタ** > **アプリケーション** > **(目的のアプリケーション ex) LocalAgentType** > **fabric:/LocalAgent** > **Fabric:/LocalAgent/ArtifactsManager** > **(guid)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="00678-134">To determine what machine is the primary instance for stateful services, like a local agent, go to Service Fabric Explorer, expand **Cluster** > **Applications** > **(intended application ex) LocalAgentType** > **fabric:/LocalAgent** > **Fabric:/LocalAgent/ArtifactsManager** > **(guid)**.</span></span>

<span data-ttu-id="00678-135">プライマリ ノードに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00678-135">Note the primary node.</span></span> <span data-ttu-id="00678-136">ステートレス サービス、または他のアプリケーションについては、すべてのノードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-136">For stateless services, or the rest of the applications, you need to check all of the nodes.</span></span>

## <a name="timeout-error-received-when-creating-a-service-fabric-cluster"></a><span data-ttu-id="00678-137">Service Fabric クラスターの作成時に受信したタイムアウト エラー</span><span class="sxs-lookup"><span data-stu-id="00678-137">Timeout error received when creating a Service Fabric cluster</span></span>
<span data-ttu-id="00678-138">該当するセットアップ トピックにあるスタンドアロン Service Fabric クラスターのセットアップにあるように Test-D365FOConfiguration.ps1 を実行し、エラーに注目します。</span><span class="sxs-lookup"><span data-stu-id="00678-138">Run Test-D365FOConfiguration.ps1 as noted in the set up a standalone Service Fabric cluster in the appropriate setup topic and note any errors:</span></span> 
- [<span data-ttu-id="00678-139">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-139">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [<span data-ttu-id="00678-140">プラットフォーム更新プログラム 8 および 11</span><span class="sxs-lookup"><span data-stu-id="00678-140">Platform update 8 and 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

<span data-ttu-id="00678-141">すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-141">Verify that the Service Fabric Server client certificate exists in the LocalMachine store on all service fabric nodes.</span></span>
<span data-ttu-id="00678-142">Service Fabric Server 証明書にすべての Service Fabric ノード上のネットワーク サービス 用 ACL が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-142">Verify that the Service Fabric Server certificate has the ACL for Network Service on all service fabric nodes.</span></span>

## <a name="time-out-while-waiting-for-installer-service-to-complete-for-machine-xxxx"></a><span data-ttu-id="00678-143">インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウトしました</span><span class="sxs-lookup"><span data-stu-id="00678-143">Time out while waiting for Installer Service to complete for machine x.x.x.x</span></span>
<span data-ttu-id="00678-144">IP アドレス (マシン) ごとにノード タイプを 1 つのみ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="00678-144">You can only have one node type for each IP address (machine).</span></span> <span data-ttu-id="00678-145">ノードが同じマシン上で再利用されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00678-145">Check to see if the nodes are being reused on the same machine.</span></span> <span data-ttu-id="00678-146">たとえば、AOS および ORCH は、同一のマシン上にある必要があり、ConfigTemplate.xml が正しく定義される必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-146">For example, AOS and ORCH must be on the same machine and ConfigTemplate.xml must be correctly defined.</span></span>

## <a name="remove-a-specific-application"></a><span data-ttu-id="00678-147">特定のアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="00678-147">Remove a specific application</span></span>
<span data-ttu-id="00678-148">配置の削除またはクリーンアップに Lifecycle Services (LCS) を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00678-148">We recommend that you use Lifecycle Services (LCS) to remove or clean up deployments.</span></span> <span data-ttu-id="00678-149">ただし、追加の手順が必要な場合は、アプリケーションを削除する Service Fabric Explorer を使用できます。</span><span class="sxs-lookup"><span data-stu-id="00678-149">However, if additional steps are needed, you can use Service Fabric Explorer to remove an application.</span></span>

<span data-ttu-id="00678-150">Service Fabric エクスプローラーで、**アプリケーション ノード** > **アプリケーション** > **MonitoringAgentAppType-Agent** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-150">In Service Fabric Explorer, go to **Application node** > **Applications** > **MonitoringAgentAppType-Agent**.</span></span> <span data-ttu-id="00678-151">**ファブリック:/エージェント監視**で省略記号をクリックし、アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-151">Click the ellipses by **fabric:/Agent-Monitoring** and delete the application.</span></span> <span data-ttu-id="00678-152">確認のためにアプリケーションの正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="00678-152">Enter the full name of the application to confirm.</span></span>
<span data-ttu-id="00678-153">また、省略記号および **非引当タイプ** の順にクリックすることにより、**MonitoringAgentAppType-Agent** を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="00678-153">You can also remove the **MonitoringAgentAppType-Agent** by clicking the ellipses and then **Unprovision Type**.</span></span> <span data-ttu-id="00678-154">確認のために正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="00678-154">Enter the full name to confirm.</span></span>

### <a name="remove-all-ax-applications-from-service-fabric"></a><span data-ttu-id="00678-155">Service Fabric からすべての AX アプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="00678-155">Remove all AX applications from Service Fabric</span></span>

<span data-ttu-id="00678-156">次のスクリプトは、LocalAgent および LocalAgent の Monitoring エージェントを除く、すべての SF アプリケーションを削除およびプロビジョニング解除します。</span><span class="sxs-lookup"><span data-stu-id="00678-156">The following script will remove and unprovision all SF applications, except the LocalAgent and Monitoring agent for the LocalAgent.</span></span> <span data-ttu-id="00678-157">これは、オーケストレータ VM で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-157">It must be executed on a orchestrator VM.</span></span>

```powershell
$applicationNamesToIgnore = @('fabric:/LocalAgent', 'fabric:/Agent-Monitoring')
$applicationTypeNamesToIgnore = @('MonitoringAgentAppType-Agent', 'LocalAgentType')

Get-ServiceFabricApplication | `
    Where-Object { $_.ApplicationName -notin $applicationNamesToIgnore } | `
    Remove-ServiceFabricApplication -Force

Get-ServiceFabricApplicationType | `
    Where-Object { $_.ApplicationTypeName -notin $applicationTypeNamesToIgnore } | `
    Unregister-ServiceFabricApplicationType -Force
```

## <a name="remove-service-fabric"></a><span data-ttu-id="00678-158">Service Fabric の削除</span><span class="sxs-lookup"><span data-stu-id="00678-158">Remove Service Fabric</span></span>
<span data-ttu-id="00678-159">Service Fabric クラスターを完全に削除するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-159">To remove the Service Fabric cluster completely, execute:</span></span>

```powershell
.\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
```

<span data-ttu-id="00678-160">これによりエラーが発生する場合は、ノードで次のスクリプトを使用してそのクラスターで特定のノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-160">If this results in an error, remove a specific node on that cluster using the following script on the node:</span></span>

```powershell
& "C:\Program Files\Microsoft Service Fabric\bin\fabric\fabric.code\CleanFabric.ps1"
```

<span data-ttu-id="00678-161">次に、既定値を使用する場合、`C:\ProgramData\SF` のフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-161">Next, remove the folder `C:\ProgramData\SF`, if using the default.</span></span> <span data-ttu-id="00678-162">それ以外の場合、指定したフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-162">Otherwise, remove the specified folder.</span></span>
<span data-ttu-id="00678-163">アクセス拒否エラーが発生した場合は、PowerShell を再起動するか、マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="00678-163">If you receive an access denied error, restart PowerShell or restart the machine.</span></span>

## <a name="clean-up-an-existing-environment-and-start-over"></a><span data-ttu-id="00678-164">既存の環境をクリーンアップしてやり直す</span><span class="sxs-lookup"><span data-stu-id="00678-164">Clean up an existing environment and start over</span></span>

<span data-ttu-id="00678-165">最初からやり直すために、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="00678-165">Follow the steps below in order to start over:</span></span>

1. <span data-ttu-id="00678-166">LCS のプロジェクトへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="00678-166">Access the project in LCS.</span></span>
    1. <span data-ttu-id="00678-167">[環境] で、展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-167">Under Environments, Delete the deployment.</span></span>
    1. <span data-ttu-id="00678-168">アプリケーションが環境の Service Fabric Explorer から表示されなくなることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00678-168">Note that the applications should start disappearing from Service Fabric Explorer on the environment.</span></span> <span data-ttu-id="00678-169">これには 1 〜 2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="00678-169">This will take a minute or two.</span></span>
2. <span data-ttu-id="00678-170">`LocalAgentCLI.exe` を含むオーケストレーター マシンへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="00678-170">Access the orchestrator machine that contains `LocalAgentCLI.exe`.</span></span>
   1. <span data-ttu-id="00678-171">ローカル エージェント クリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-171">Run Local Agent cleanup:</span></span>
       ```powershell
       .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
       ```
   2. <span data-ttu-id="00678-172">Service Fabric の削除:</span><span class="sxs-lookup"><span data-stu-id="00678-172">Remove Service Fabric:</span></span>
       ```powershell
       .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
       ```
   3. <span data-ttu-id="00678-173">いずれかのノードが Service Fabric をアンインストールするのに失敗した場合は、各障害が発生したノードに対して、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-173">If any of the nodes fail to uninstall Service Fabric, run the following on each failing node:</span></span>
       ```powershell
       & "C:\Program Files\Microsoft Service Fabric\bin\fabric\fabric.code\CleanFabric.ps1"
       ```
   4. <span data-ttu-id="00678-174">すべての Service Fabric ノードの `C:\ProgramData\SF\` フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-174">Remove `C:\ProgramData\SF\` folder on all Service Fabric nodes.</span></span>
       - <span data-ttu-id="00678-175">アクセスが拒否された場合は、マシンを再起動してからやり直します。</span><span class="sxs-lookup"><span data-stu-id="00678-175">If access denied, restart the machine and try again.</span></span>
3. <span data-ttu-id="00678-176">証明を削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-176">Remove certificates.</span></span>
   1. <span data-ttu-id="00678-177">すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-177">Remove old certificates from all AOS, BI, ORCH and DC nodes.</span></span>
       - <span data-ttu-id="00678-178">証明書は、次の証明書ストアに存在します。`Cert:\CurrentUser\My\`、`Cert:\LocalMachine\My` および `Cert:\LocalMachine\Root`。</span><span class="sxs-lookup"><span data-stu-id="00678-178">The certificates exist in the following certificate stores: `Cert:\CurrentUser\My\`, `Cert:\LocalMachine\My` and `Cert:\LocalMachine\Root`.</span></span>
   2. <span data-ttu-id="00678-179">SQL サーバー設定が変更される場合は、SQL サーバー証明書も削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-179">If the SQL server setup will be modified, remove the SQL server certificates as well.</span></span>
   3. <span data-ttu-id="00678-180">ADFS 設定が変更される場合は、ADFS 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-180">If the ADFS settings will be modified, remove the ADFS certificate as well.</span></span>

4. <span data-ttu-id="00678-181">更新プログラム構成ファイル。</span><span class="sxs-lookup"><span data-stu-id="00678-181">Update configuration files.</span></span> <span data-ttu-id="00678-182">テンプレートのフィールドを適切に入力するには、[プラットフォーム更新 12](setup-deploy-on-premises-pu12.md) または[プラットフォーム更新8 または 11](setup-deploy-on-premises-pu8-pu11.md) の該当する展開ドキュメントをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="00678-182">Refer to the appropriate deployment documentation for [Platform update 12](setup-deploy-on-premises-pu12.md) or for [Platform update 8 or 11](setup-deploy-on-premises-pu8-pu11.md) to properly fill out the fields in the templates:</span></span> 
    - <span data-ttu-id="00678-183">ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="00678-183">ConfigTemplate.xml</span></span>
    - <span data-ttu-id="00678-184">ClusterConfig.json</span><span class="sxs-lookup"><span data-stu-id="00678-184">ClusterConfig.json</span></span>
5. <span data-ttu-id="00678-185">LCS のプロジェクトへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="00678-185">Access the project in LCS.</span></span>
    1. <span data-ttu-id="00678-186">環境の LCS コネクタを再作成するか、または既存のコネクタの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="00678-186">Recreate the LCS connector for the environment, or edit the settings of an existing one.</span></span>
        - <span data-ttu-id="00678-187">LCS の値を簡単にコピーするには、`.\Get-AgentConfiguration.ps1`script を使用します。</span><span class="sxs-lookup"><span data-stu-id="00678-187">Use the `.\Get-AgentConfiguration.ps1` script to obtain easy to copy values for LCS.</span></span>
    1. <span data-ttu-id="00678-188">最新のローカル エージェント コンフィギュレーション `localagent-config.json` をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="00678-188">Download the latest local agent configuration, `localagent-config.json`.</span></span>

<span data-ttu-id="00678-189">ここで、[プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md) または[プラットフォーム更新プログラム 8 または 11](setup-deploy-on-premises-pu8-pu11.md) の適切な配置のドキュメントから再び開始します。</span><span class="sxs-lookup"><span data-stu-id="00678-189">Now start again with the appropriate deployment documentation for [Platform update 12](setup-deploy-on-premises-pu12.md) or for [Platform update 8 or 11](setup-deploy-on-premises-pu8-pu11.md).</span></span>

## <a name="local-agent"></a><span data-ttu-id="00678-190">ローカル エージェント</span><span class="sxs-lookup"><span data-stu-id="00678-190">Local agent</span></span>
<span data-ttu-id="00678-191">ローカル エージェントは、LCS との通信、インストールするコンポーネントのダウンロード、Dynamics 365 for Finance and Operations のインストール、管理、削除を担当するフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="00678-191">Local agent is the framework that is responsible for communicating with LCS, downloading components to be installed, installation, and maintaining and removing Dynamics 365 for Finance and Operations.</span></span>

## <a name="how-to-find-the-local-agent-values-that-are-used"></a><span data-ttu-id="00678-192">使用するローカル エージェント値を検索する方法</span><span class="sxs-lookup"><span data-stu-id="00678-192">How to find the local agent values that are used</span></span>
<span data-ttu-id="00678-193">ローカル エージェントの値は、**クラスター** > **アプリケーション** > **LocalAgentType** > **fabric:/LocalAgent、詳細/** の Service Fabric Explorer で確認できます。</span><span class="sxs-lookup"><span data-stu-id="00678-193">Local agent values can be found in Service Fabric Explorer under **Cluster** > **Applications** > **LocalAgentType** > **fabric:/LocalAgent, Details**.</span></span>

## <a name="install-upgrade-or-uninstall-local-agent"></a><span data-ttu-id="00678-194">ローカル エージェントのインストール、アップグレード、アンインストール</span><span class="sxs-lookup"><span data-stu-id="00678-194">Install, upgrade, or uninstall local agent</span></span>
<span data-ttu-id="00678-195">ローカル エージェントのインストールは、適切なプラットフォーム更新プログラムに関するオンプレミス環境の設定と配置で説明します。</span><span class="sxs-lookup"><span data-stu-id="00678-195">Local agent installation is discussed in the Set up and deploy on-premises environments topic for the appropriate platform update:</span></span> 
- [<span data-ttu-id="00678-196">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-196">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md) 
- [<span data-ttu-id="00678-197">プラットフォーム更新プログラム 8 もしくは 11</span><span class="sxs-lookup"><span data-stu-id="00678-197">Platform update 8 or 11</span></span>](setup-deploy-on-premises-pu8-pu11.md)

<span data-ttu-id="00678-198">また、以下のアップグレードおよびアンインストール コマンドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="00678-198">You can also use the following upgrade and uninstall commands:</span></span>

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Upgrade <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> <span data-ttu-id="00678-199">クリーンアップ コマンドは、ファイル共有に配置されたファイルを削除しません。</span><span class="sxs-lookup"><span data-stu-id="00678-199">The cleanup command doesn't remove any of the files that were placed in the file share.</span></span> <span data-ttu-id="00678-200">ファイル共有は再利用できます。</span><span class="sxs-lookup"><span data-stu-id="00678-200">The file share can be reused.</span></span>

## <a name="error-occurs-when-starting-up-local-agent-services"></a><span data-ttu-id="00678-201">ローカル エージェント サービスを開始するときにエラーが発生</span><span class="sxs-lookup"><span data-stu-id="00678-201">Error occurs when starting up local agent services</span></span>
<span data-ttu-id="00678-202">「'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' というファイルまたはアセンブリ、またはその依存関係のいずれかをロードできませんでした」というエラーが発生した場合、**厳密な名前**検証は有効化できなくなります。</span><span class="sxs-lookup"><span data-stu-id="00678-202">If you receive the error, "Could not load file or assembly 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies", this means that the **Strong name** verification should no longer be enabled.</span></span> <span data-ttu-id="00678-203">これは、Configure-PreReqs.ps1 を使用して行います。</span><span class="sxs-lookup"><span data-stu-id="00678-203">This is done by using Configure-PreReqs.ps1.</span></span> <span data-ttu-id="00678-204">検証が有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-204">To validate that the verification is no longer enabled, run Test-D365FOConfiguration.ps1.</span></span>

## <a name="validation-in-progress-message-displays-for-several-minutes-in-lcs"></a><span data-ttu-id="00678-205">「検証が進行中」のメッセージが LCS に数分表示されます。</span><span class="sxs-lookup"><span data-stu-id="00678-205">"Validation in progress" message displays for several minutes in LCS</span></span>
<span data-ttu-id="00678-206">ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-206">Complete the following steps to troubleshoot general issues with local agent validation.</span></span>
1. <span data-ttu-id="00678-207">コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で Configure-PreReqs.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-207">Run Configure-PreReqs.ps1 on all the Orchestrator machines to configure the machines correctly.</span></span>
2. <span data-ttu-id="00678-208">Test-D365FOConfiguration.ps1 スクリプトがすべての Orchestrator マシンで通ることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-208">Verify that the script Test-D365FOConfiguration.ps1 passes on all of the Orchestrator machines.</span></span>
3. <span data-ttu-id="00678-209">LocalAgentCLI.exe のインストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-209">Verify that the installation of LocalAgentCLI.exe completed successfully.</span></span>
4. <span data-ttu-id="00678-210">Service Fabric Explorer に移動し、アプリケーションがすべてが正常であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-210">Go to Service Fabric Explorer and verify that the applications are all healthy.</span></span>
5. <span data-ttu-id="00678-211">アプリケーションが正常な場合は、障害が発生したサービスの基本ノードを探します。</span><span class="sxs-lookup"><span data-stu-id="00678-211">If the applications are not healthy, locate the primary node for the failing service.</span></span> <span data-ttu-id="00678-212">次からイベントを検索します。</span><span class="sxs-lookup"><span data-stu-id="00678-212">Look for events in:</span></span>
    - <span data-ttu-id="00678-213">**イベント ビューアー** > **カスタム ビュー** > **管理イベント**</span><span class="sxs-lookup"><span data-stu-id="00678-213">**Event Viewer** > **Custom Views** > **Administrative Events**</span></span>
    - <span data-ttu-id="00678-214">**イベント ビューアー** > **アプリケーションおよびサービス ログ** > **Microsoft** > **Dynamics** > **AX-LocalAgent**</span><span class="sxs-lookup"><span data-stu-id="00678-214">**Event Viewer** > **Applications and Services Log** > **Microsoft** > **Dynamics** > **AX-LocalAgent**</span></span>

<span data-ttu-id="00678-215">**一般的なエラー**</span><span class="sxs-lookup"><span data-stu-id="00678-215">**Common errors**</span></span>

<span data-ttu-id="00678-216">次のような一般的なエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-216">The following are common errors that you may encounter:</span></span>

- <span data-ttu-id="00678-217">「コマンドを処理できません」または「チャンネル情報を取得できません」</span><span class="sxs-lookup"><span data-stu-id="00678-217">"Unable to process commands" or "Unable to get the channel information"</span></span>
- <span data-ttu-id="00678-218">「ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="00678-218">"RunAsync failed due to an unhandled exception causing the host process to crash: System.ArgumentNullException: Value cannot be null.</span></span> <span data-ttu-id="00678-219">パラメーター名: 証明書"</span><span class="sxs-lookup"><span data-stu-id="00678-219">Parameter name: certificate"</span></span>

<span data-ttu-id="00678-220">**理由** これらのエラーは、OnPremLocalAgent 証明書に指定された証明書が有効でないか、テナントに対して正しく構成されていないために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="00678-220">**Reason** These errors may occur because the certificate specified for the OnPremLocalAgent certificate is not valid or is not configured correctly for the tenant.</span></span>

<span data-ttu-id="00678-221">**ステップ**エラーを解決するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="00678-221">**Steps** Complete the following steps to resolve the error.</span></span>
1. <span data-ttu-id="00678-222">すべてのオーケストレータ ノードで Test-D365FOConfiguration.ps1 を実行し、すべてのチェックに合格することを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-222">Run Test-D365FOConfiguration.ps1 on all Orchestrator nodes to ensure all checks pass.</span></span>
2. <span data-ttu-id="00678-223">ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-223">Verify that the certificate specified in local agent configuration is correct.</span></span>
    - <span data-ttu-id="00678-224">LCS および ConfigTemplate.xml で拇印を指定する際に、特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-224">Make sure there are no special characters while specifying the thumbprint in LCS and the ConfigTemplate.xml.</span></span>
    - <span data-ttu-id="00678-225">証明書は、次のような infrastructure\ConfigTemplate.xml で指定されているものと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-225">The certificate should be the same as what is specified in infrastructure\ConfigTemplate.xml for the following.</span></span>

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. <span data-ttu-id="00678-226">テナント用 LCS 接続のコンフィギュレーションが、LCS のローカル エージェントコンフィギュレーションで指定されているのと同じ証明書を使用して完了したことを、確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-226">Ensure that the steps in Configure LCS connectivity for the tenant were completed using the same certificate that is specified in the local agent configuration in LCS:</span></span> 
    - [<span data-ttu-id="00678-227">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-227">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="00678-228">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="00678-228">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)
4. <span data-ttu-id="00678-229">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-229">Uninstall the local agent.</span></span>
5. <span data-ttu-id="00678-230">ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="00678-230">Specify the correct certificate in the local agent configuration and download the configuration file again.</span></span>
6. <span data-ttu-id="00678-231">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-231">Install the local agent again with the new configuration file.</span></span>

<span data-ttu-id="00678-232">**エラー** `'\\...\agent\assets\StandAloneSetup-76308-1.zip'` パスへのアクセスは拒否されます。</span><span class="sxs-lookup"><span data-stu-id="00678-232">**Error** Access to the path `'\\...\agent\assets\StandAloneSetup-76308-1.zip'` is denied.</span></span>

<span data-ttu-id="00678-233">**理由** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。</span><span class="sxs-lookup"><span data-stu-id="00678-233">**Reason** The file share specified in local agent configuration is not valid.</span></span>

<span data-ttu-id="00678-234">**ステップ**エラーを解決するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="00678-234">**Steps** Complete the following steps to resolve the error.</span></span>
1. <span data-ttu-id="00678-235">指定した共有が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-235">Verify that the specified share exists.</span></span>
2. <span data-ttu-id="00678-236">ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-236">Verify that the local agent user has full permission on the share.</span></span> <span data-ttu-id="00678-237">ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定された DNS 名です。</span><span class="sxs-lookup"><span data-stu-id="00678-237">The local agent user is the DNS name specified in ConfigTemplate.xml in the following section.</span></span>

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. <span data-ttu-id="00678-238">設定文書の設定ファイル共有セクションが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-238">Ensure that the Setup file share section in the setup document is completed.</span></span>
4. <span data-ttu-id="00678-239">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-239">Uninstall the local agent.</span></span>
5. <span data-ttu-id="00678-240">ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="00678-240">Specify the correct file share in local agent configuration and download the configuration file again.</span></span>
6. <span data-ttu-id="00678-241">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-241">Install local agent again with the new configuration file.</span></span>

<span data-ttu-id="00678-242">**エラー**ユーザー「D365\svc LocalAgent$」へのログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="00678-242">**Error** Login failed for user 'D365\svc-LocalAgent$'.</span></span> <span data-ttu-id="00678-243">理由: 指定した名前に一致するログインが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="00678-243">Reason: Could not find a login matching the name provided.</span></span> <span data-ttu-id="00678-244">[CLIENT: 10.0.2.23]</span><span class="sxs-lookup"><span data-stu-id="00678-244">[CLIENT: 10.0.2.23]</span></span>

<span data-ttu-id="00678-245">**理由** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="00678-245">**Reason** The local agent user is not able to connect to the orchestration database.</span></span> <span data-ttu-id="00678-246">これは、ユーザーが削除されて AD で再作成された可能性があるために発生します。つまり、ユーザーの SID が変更されたことを意味します。</span><span class="sxs-lookup"><span data-stu-id="00678-246">This could happen because users may have been deleted and then recreated in the AD, which means the SID of the user has changed.</span></span> <span data-ttu-id="00678-247">SQL Server またはデータベースのユーザーに与えられたアクセスは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="00678-247">Any access given to the user for the SQL Server or database will no longer work.</span></span>

<span data-ttu-id="00678-248">**ステップ**エラーを解決するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="00678-248">**Steps** Complete the following steps to resolve the error.</span></span>

1. <span data-ttu-id="00678-249">SQL Server でスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-249">Run the script on the SQL server.</span></span>
    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    <span data-ttu-id="00678-250">空の Orchestrator データベースが存在しない場合は作成され、db\_owner 権限を持つデータベースにローカル エージェント ユーザーが追加されます。</span><span class="sxs-lookup"><span data-stu-id="00678-250">This creates an empty Orchestrator database, if one does not already exist, and adds the local agent user to the database with db\_owner permission.</span></span>

2. <span data-ttu-id="00678-251">アプリケーションは、適切なアクセス許可が付与された後は、自動的に正常な状態になります。</span><span class="sxs-lookup"><span data-stu-id="00678-251">The application should automatically go to healthy state after the correct permissions are provided.</span></span>
3. <span data-ttu-id="00678-252">SQL FQDN、データベース名、およびローカル エージェント ユーザーなどの、設定のいずれかが LCS に正しく記載されていない場合、設定を変更し、ローカル エージェントを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-252">If any of the settings, such as the SQL FQDN, database name, and local agent user was provided incorrectly in LCS, change the settings and reinstall local agent.</span></span>
4. <span data-ttu-id="00678-253">最初の 3 つの手順を実行しても問題が解決しない場合は、SQL server とデータベースからローカル エージェント ユーザーを手動で削除し、初期化データベース スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-253">If the first three steps do not resolve the issue, manually remove the local agent user from the SQL server and the database, and then re-run the Initialize-Database script.</span></span>
5. <span data-ttu-id="00678-254">AD でユーザーを再作成する場合、SID は変更されないことを留意します。</span><span class="sxs-lookup"><span data-stu-id="00678-254">If you recreate a user in AD, remember that the SID will change.</span></span> <span data-ttu-id="00678-255">ユーザーの以前の SID を削除し、新しい SID を追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-255">Remove the previous SID for the user and add a new SID.</span></span>

<span data-ttu-id="00678-256">**追加シナリオ**ローカル エージェント ユーザーは、SQL Server またはデータベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="00678-256">**Additional scenario** The local agent user can't connect to the SQL server or database.</span></span>

<span data-ttu-id="00678-257">**ステップ**エラーを解決するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="00678-257">**Steps** Complete the following steps to resolve the error.</span></span>

1. <span data-ttu-id="00678-258">SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-258">Delete the svc-LocalAgent user from the SQL server primary node databases and then remove the login from both servers.</span></span>
2. <span data-ttu-id="00678-259">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-259">Run the following scripts.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

   <span data-ttu-id="00678-260">これらのスクリプトは、**常時オン**設定では機能しません。</span><span class="sxs-lookup"><span data-stu-id="00678-260">These scripts do not work with **always-on** setup.</span></span> <span data-ttu-id="00678-261">データベースは、最初にプライマリ ノードで作成し、その後、複製する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-261">The database needs to be created first in the primary node and then replicated.</span></span>

<span data-ttu-id="00678-262">**エラー** RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="00678-262">**Error** RunAsync failed due to an unhandled exception causing the host process to crash: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span></span> <span data-ttu-id="00678-263">---> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'</span><span class="sxs-lookup"><span data-stu-id="00678-263">---> System.Net.WebException: The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'</span></span>

<span data-ttu-id="00678-264">**理由** ローカル エージェントマシンは lcsapi.lcs.dynamics.com に接続できません。AX-BridgeService のイベントログで「リモート名を解決できませんでした: lcsapi.lcs.dynamics.com」を確認してください。</span><span class="sxs-lookup"><span data-stu-id="00678-264">**Reason** The local agent machines can't connect to lcsapi.lcs.dynamics.com. Review the AX-BridgeService event log for "The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'".</span></span>

<span data-ttu-id="00678-265">**ステップ**エラーを解決するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="00678-265">**Steps** Complete the following steps to resolve the error.</span></span>
1. <span data-ttu-id="00678-266">`psping lcsapi.lcs.dynamics.com:80` を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-266">Run `psping lcsapi.lcs.dynamics.com:80`.</span></span>
2. <span data-ttu-id="00678-267">応答を受信しない場合は、組織の IT 部門に問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="00678-267">If you don't receive a reply, contact the IT department at your organization.</span></span> <span data-ttu-id="00678-268">ファイアウォールが lcsapi またはプロキシの問題へのアクセスをブロックしています。</span><span class="sxs-lookup"><span data-stu-id="00678-268">The firewall is blocking access to lcsapi or proxy issues.</span></span>

        lcsapi.lcs.dynamics.com:443
        login.windows.net:443
        uswelcs1lcm.queue.core.windows.net:443
        www.office.com:443
        login.microsoftonline.com:443
        dc.services.visualstudio.com:443
        uswelcs1lcm.blob.core.windows.net:443
        uswedpl1catalog.blob.core.windows.net:443 

## <a name="error-unable-to-load-dll-fabricclientdll"></a><span data-ttu-id="00678-269">エラー、「DLL 'FabricClient.dll' を読み込むことができません」</span><span class="sxs-lookup"><span data-stu-id="00678-269">Error "Unable to load DLL 'FabricClient.dll'"</span></span>
<span data-ttu-id="00678-270">このエラーが発生した場合は、閉じて、PowerShell を再表示します。</span><span class="sxs-lookup"><span data-stu-id="00678-270">If you receive this error, close and reopen PowerShell.</span></span> <span data-ttu-id="00678-271">エラーがまだ発生する場合は、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="00678-271">If the error still occurs, restart the machine.</span></span>

## <a name="what-cluster-id-in-agent-config-should-be-used"></a><span data-ttu-id="00678-272">エージェント構成でどのようなクラスター ID を使用する必要がありますか</span><span class="sxs-lookup"><span data-stu-id="00678-272">What Cluster ID in Agent config should be used</span></span>
<span data-ttu-id="00678-273">クラスター ID は、任意の GUID にすることができます。</span><span class="sxs-lookup"><span data-stu-id="00678-273">The Cluster ID can be any GUID.</span></span> <span data-ttu-id="00678-274">この GUID は、追跡目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="00678-274">This GUID is used for tracking purposes.</span></span>

## <a name="local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a><span data-ttu-id="00678-275">ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します</span><span class="sxs-lookup"><span data-stu-id="00678-275">Local agent stops working after the tenant for the project from LCS is changed</span></span>
<span data-ttu-id="00678-276">更新されたテナントでローカル エージェントを構成するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-276">Complete the following steps to configure local agent with updated tenant.</span></span>
1. <span data-ttu-id="00678-277">既にコネクタがインストールされている LCS からすべての環境を削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-277">Remove all of the environments from LCS that already have the connector installed.</span></span>
2. <span data-ttu-id="00678-278">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-278">Uninstall the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

3. <span data-ttu-id="00678-279">手順 11 の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-279">Complete the steps in step 11.</span></span> <span data-ttu-id="00678-280">環境のテナントに LCS 接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="00678-280">Configure LCS connectivity for the tenant for your environment:</span></span>
    - [<span data-ttu-id="00678-281">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-281">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="00678-282">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="00678-282">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. <span data-ttu-id="00678-283">新しいテナントに新しい LCS コネクタを作成します。</span><span class="sxs-lookup"><span data-stu-id="00678-283">Create a new LCS connector in the new tenant.</span></span>
5. <span data-ttu-id="00678-284">local-agent.config file をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="00678-284">Download the local-agent.config file.</span></span>
6. <span data-ttu-id="00678-285">ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="00678-285">Install local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="monitor-deployment-locally"></a><span data-ttu-id="00678-286">ローカルでの配置の監視</span><span class="sxs-lookup"><span data-stu-id="00678-286">Monitor deployment locally</span></span>
<span data-ttu-id="00678-287">プライマリ オーケストレータ コンピューターとコンポーネント マネージャー、およびブリッジ サービス AX LocalAgent (全体的なインストール プロセス) のイベント ビューアー ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-287">Review the event viewer logs for the primary orchestrator machine and artifacts manager, and the bridge service AX-LocalAgent (overall installation process).</span></span>

- <span data-ttu-id="00678-288">モジュール</span><span class="sxs-lookup"><span data-stu-id="00678-288">Modules</span></span>
    - <span data-ttu-id="00678-289">共通</span><span class="sxs-lookup"><span data-stu-id="00678-289">Common</span></span>
    - <span data-ttu-id="00678-290">Reportingservices</span><span class="sxs-lookup"><span data-stu-id="00678-290">Reportingservices</span></span>
    - <span data-ttu-id="00678-291">AOS</span><span class="sxs-lookup"><span data-stu-id="00678-291">AOS</span></span>
    - <span data-ttu-id="00678-292">Financialreporting</span><span class="sxs-lookup"><span data-stu-id="00678-292">Financialreporting</span></span>
- <span data-ttu-id="00678-293">コマンド</span><span class="sxs-lookup"><span data-stu-id="00678-293">Command</span></span>
    - <span data-ttu-id="00678-294">段取り</span><span class="sxs-lookup"><span data-stu-id="00678-294">Setup</span></span>
    - <span data-ttu-id="00678-295">Dvt - 配置確認テスト</span><span class="sxs-lookup"><span data-stu-id="00678-295">Dvt - Deployment verification test</span></span>

<span data-ttu-id="00678-296">AX SetupModuleEvents (モジュールの追加の詳細情報) AX SetupInfrastructureEvents (Service Fabric との対話がある場合の追加の詳細)</span><span class="sxs-lookup"><span data-stu-id="00678-296">AX-SetupModuleEvents (additional details for Module details) AX-SetupInfrastructureEvents (additional details when interactions with Service Fabric)</span></span>

## <a name="aos-machines"></a><span data-ttu-id="00678-297">AOS マシン</span><span class="sxs-lookup"><span data-stu-id="00678-297">AOS machines</span></span>
<span data-ttu-id="00678-298">**イベント ビューアー** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** > **AX DatabaseSynchronize**
**イベント ビューアー** > **カスタム ビュー** > **管理イベント**</span><span class="sxs-lookup"><span data-stu-id="00678-298">**Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize**
**Event Viewer** > **Custom Views** > **Administrative Events**</span></span>

## <a name="to-view-the-entire-error-message"></a><span data-ttu-id="00678-299">エラー メッセージ全体を表示するには</span><span class="sxs-lookup"><span data-stu-id="00678-299">To view the entire error message</span></span>
<span data-ttu-id="00678-300">**詳細** タブをクリックし、完全なエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="00678-300">Click the **Details** tab to view the full error message.</span></span>

## <a name="service-fabric-failing"></a><span data-ttu-id="00678-301">Service Fabric の障害</span><span class="sxs-lookup"><span data-stu-id="00678-301">Service Fabric failing</span></span>
<span data-ttu-id="00678-302">失敗しているサービスをメモして、対応するアプリケーション ディレクトリを開きます。</span><span class="sxs-lookup"><span data-stu-id="00678-302">Note the service that is failing and open the corresponding application directory.</span></span> <span data-ttu-id="00678-303">例: `C:\ProgramData\SF\<OrchestratorMachineName>\Fabric\work\Applications\LocalAgentType_App<N>\log`</span><span class="sxs-lookup"><span data-stu-id="00678-303">For example: `C:\ProgramData\SF\<OrchestratorMachineName>\Fabric\work\Applications\LocalAgentType_App<N>\log`</span></span>

## <a name="encryption-errors"></a><span data-ttu-id="00678-304">暗号化エラー</span><span class="sxs-lookup"><span data-stu-id="00678-304">Encryption errors</span></span>
<span data-ttu-id="00678-305">暗号化エラーの例には、AXBootstrapperAppType、Bootstrapper、AXDiagnostics、RTGatewayAppType、ゲートウェイの潜在的なエラー関連、Microsoft.D365.Gateways.ClusterGateway.exe などがあります。</span><span class="sxs-lookup"><span data-stu-id="00678-305">Some encryption error examples include, AXBootstrapperAppType, Bootstrapper, AXDiagnostics, RTGatewayAppType, Gateway potential failure related, and Microsoft.D365.Gateways.ClusterGateway.exe.</span></span>

<span data-ttu-id="00678-306">データの暗号化証明書がマシンにインストールされていない AOS AccountPassword を暗号化するために使用される場合、これらのエラーのいずれかを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-306">You might receive one of these errors if the data encipherment certificate is used to encrypt AOS AccountPassword was not installed on the machine.</span></span> <span data-ttu-id="00678-307">この証明書が証明書 (ローカル コンピューター) に存在する可能性があります。または、プロバイダーの種類が間違っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-307">This certificate could be in the certificates (local computer) or it could be that the provider type is incorrect.</span></span>

<span data-ttu-id="00678-308">エラーを解決するには、credentials.json ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="00678-308">To resolve the error, validate the credentials.json file.</span></span> <span data-ttu-id="00678-309">次のメッセージを (AOS1 上に) 入力することによって、テキストの暗号化が正しく解除されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-309">Verify that the text is decrypting correctly by entering the following message (on AOS1).</span></span>

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="00678-310">このエラーは、パラメーター **''** が ApplicationManifest ファイルで定義されていない場合にも発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-310">This error may also occur if the parameter **''** is not defined in the ApplicationManifest file.</span></span> <span data-ttu-id="00678-311">これを確認するには、**イベント ビューア** > **ユーザー設定ビュー** > **管理イベント** に移動し、次を確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-311">To verify this, go to **Event Viewer** > **Custom Views** > **Administrative Events** and check for the following:</span></span>

- <span data-ttu-id="00678-312">credentials.json ファイルの適切なレイアウト/構造は、資格情報を暗号化します。</span><span class="sxs-lookup"><span data-stu-id="00678-312">Proper layout/structure of credentials.json file encrypt credentials.</span></span> <span data-ttu-id="00678-313">詳細については、「環境の資格情報の暗号化」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-313">For more information, see Encrypt credentials for your environment:</span></span>
    - [<span data-ttu-id="00678-314">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-314">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#encryptcred)
    - [<span data-ttu-id="00678-315">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="00678-315">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#encryptcred)
- <span data-ttu-id="00678-316">行末または次の行での終了引用符です。</span><span class="sxs-lookup"><span data-stu-id="00678-316">An end quote at the end of the line or on the next line.</span></span>
- <span data-ttu-id="00678-317">Microsoft-Service Fabric ソースでエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="00678-317">Error on Microsoft-Service Fabric source.</span></span>

## <a name="properties-to-create-a-dataencryption-certificate"></a><span data-ttu-id="00678-318">DataEncryption 証明書を作成するためのプロパティ</span><span class="sxs-lookup"><span data-stu-id="00678-318">Properties to create a DataEncryption certificate</span></span>
<span data-ttu-id="00678-319">DataEncryption 証明書を作成するのにには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="00678-319">Use the following properties to create the DataEncryption certificate:</span></span>

- <span data-ttu-id="00678-320">**自己署名証明書:** 自己署名証明書を使用する場合にのみ有効にします。</span><span class="sxs-lookup"><span data-stu-id="00678-320">**Is self-signed certificate:** Enable only when using self-signed certificates</span></span>
- <span data-ttu-id="00678-321">**証明書の目的:** この証明書のすべての目的を有効にします。</span><span class="sxs-lookup"><span data-stu-id="00678-321">**Certificate purposes:** Enable all purposes for this certificate</span></span>
- <span data-ttu-id="00678-322">**署名アルゴリズム:** sha256RSA</span><span class="sxs-lookup"><span data-stu-id="00678-322">**Signature algorithm:** sha256RSA</span></span>
- <span data-ttu-id="00678-323">**署名ハッシュ アルゴリズム:** sha256</span><span class="sxs-lookup"><span data-stu-id="00678-323">**Signature hash algorithm:** sha256</span></span>
- <span data-ttu-id="00678-324">**発行者:** CN = DataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="00678-324">**Issuer:** CN = DataEncryptionCertificate</span></span>
- <span data-ttu-id="00678-325">**公開キー:** RSA (2048 ビット)</span><span class="sxs-lookup"><span data-stu-id="00678-325">**Public Key:** RSA (2048 bits)</span></span>
- <span data-ttu-id="00678-326">**拇印アルゴリズム:** sha1</span><span class="sxs-lookup"><span data-stu-id="00678-326">**Thumbprint algorithm:** sha1</span></span>

> [!WARNING]
> <span data-ttu-id="00678-327">製造環境では、自己署名証明書を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="00678-327">Do not use self-signed certificates in production environments.</span></span> <span data-ttu-id="00678-328">代わりに、証明書機関によって発行された証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="00678-328">Instead, use certificates that are issued by Certificate authorities.</span></span>

## <a name="cant-find-the-certificate-and-private-key-to-use-for-decryption-0x8009200c"></a><span data-ttu-id="00678-329">暗号の解読に使用する証明書と秘密キーを見つけることができません (0x8009200C)</span><span class="sxs-lookup"><span data-stu-id="00678-329">Can't find the certificate and private key to use for decryption (0x8009200C)</span></span>
<span data-ttu-id="00678-330">証明書と ACL がない場合、または間違った拇印エントリがある場合は、特殊文字を確認し、拇印に対して `C:\ProgramData\SF\<AOSMachineName>\Fabric\work\Applications\AXBootstrapperAppType_App<N>\log\ConfigureCertificates-<timestamp>.txt` をチェックインします。</span><span class="sxs-lookup"><span data-stu-id="00678-330">If you are missing a certificate and ACL, or you have the wrong thumbprint entry, check for special characters and check in `C:\ProgramData\SF\<AOSMachineName>\Fabric\work\Applications\AXBootstrapperAppType_App<N>\log\ConfigureCertificates-<timestamp>.txt` for thumbprints.</span></span>
<span data-ttu-id="00678-331">また、`Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard` を使用してテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="00678-331">You can also test by using the `Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard`.</span></span> <span data-ttu-id="00678-332">「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACL を確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-332">If you receive the message, "Cannot find the certificate and private key to use for decryption", verify axdataenciphermentcert and svc-AXSF$ AXServiceUser ACL.</span></span>

<span data-ttu-id="00678-333">Credentials.json が変更された場合は、削除し、LCS から再配置します。</span><span class="sxs-lookup"><span data-stu-id="00678-333">If the credentials.json have changed, delete and redeploy from LCS.</span></span>

<span data-ttu-id="00678-334">上のどれも動作しない場合:</span><span class="sxs-lookup"><span data-stu-id="00678-334">If none of the above works:</span></span>

1. <span data-ttu-id="00678-335">ConfigTemplate.xml で指定されたドメイン名と AD アカウント名前が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-335">Verify that the domain name and AD account names specified in the ConfigTemplate.xml are correct.</span></span>
1. <span data-ttu-id="00678-336">用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml で指定された拇印が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-336">Verify that the thumbprints specified in the ConfigTemplate.xml are correct if the certificate was not generated using the scripts provided.</span></span>
1. <span data-ttu-id="00678-337">LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-337">Make sure the certificate thumbprints specified in LCS are correct and match those specified in ConfigTemplate.xml.</span></span> <span data-ttu-id="00678-338">特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-338">Make sure there are no special characters.</span></span> <span data-ttu-id="00678-339">`.\Get-DeploymentSettings.ps1` を実行して、コピーしやすい方法で拇印を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="00678-339">You can run `.\Get-DeploymentSettings.ps1` to get the thumbprints in an easy to copy manner.</span></span>
1. <span data-ttu-id="00678-340">証明書が生成されない場合、確認プロバイダー名は、次の証明書タイプと一致します。</span><span class="sxs-lookup"><span data-stu-id="00678-340">If the certificates are not self-generated, make sure the provider names match for the following certificate types:</span></span>
    - <span data-ttu-id="00678-341">ServiceFabricEncryption - Microsoft Enhanced Cryptographic Provider v1.0</span><span class="sxs-lookup"><span data-stu-id="00678-341">ServiceFabricEncryption - Microsoft Enhanced Cryptographic Provider v1.0</span></span>
    - <span data-ttu-id="00678-342">その他のすべての証明書タイプ - Microsoft の拡張された RSA および AES 暗号化プロバイダー</span><span class="sxs-lookup"><span data-stu-id="00678-342">All other certificate types - Microsoft Enhanced RSA and AES Cryptographic Provider</span></span>
1. <span data-ttu-id="00678-343">`Set-CertificateAcls.ps1` および `Test-D365FOConfiguration.ps1` スクリプトが Service Fabric マシンで正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-343">Make sure `Set-CertificateAcls.ps1` and `Test-D365FOConfiguration.ps1` scripts were run on all Service Fabric machines successfully.</span></span>
1. <span data-ttu-id="00678-344">`credential.json` が存在し、エントリが適切な値に復号化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-344">Make sure that the `credential.json` exists and the entries decrypt to correct values.</span></span>
    1. <span data-ttu-id="00678-345">AOS マシンのいずれかに移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-345">Go to one of the AOS machines.</span></span>
    1. <span data-ttu-id="00678-346">データ暗号化証明書が正しいことを確認するためのコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-346">Run the command to verify that the data encryption certificate is correct:</span></span>

        ```powershell
        Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
        ```
1. <span data-ttu-id="00678-347">変更するために必要な証明書のいずれかまたはコンフィギュレーションが間違っていた場合:</span><span class="sxs-lookup"><span data-stu-id="00678-347">If any of the certificates needed to be changed or the configuration was wrong:</span></span>
    1. <span data-ttu-id="00678-348">正しい値で、ConfigTemplate.xml を編集します。</span><span class="sxs-lookup"><span data-stu-id="00678-348">Edit the ConfigTemplate.xml with the correct values.</span></span>
    1. <span data-ttu-id="00678-349">すべてのセットアップ スクリプトと Test-D365FOConfiguration を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-349">Run all the setup scripts and Test-D365FOConfiguration script.</span></span>
    <span data-ttu-id="00678-350">LCS に戻り、環境を再コンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="00678-350">Go back to LCS and reconfigure the environment.</span></span>

## <a name="mr"></a><span data-ttu-id="00678-351">MR</span><span class="sxs-lookup"><span data-stu-id="00678-351">MR</span></span>
<span data-ttu-id="00678-352">追加のログは、プロバイダーを登録することで実行できます。</span><span class="sxs-lookup"><span data-stu-id="00678-352">Additional logging can be done by registering providers.</span></span> <span data-ttu-id="00678-353">[ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) をプライマリ オーケストレータ マシンにダウンロードし、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-353">Download the [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) to the primary orchestrator machine and run the following commands.</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

<span data-ttu-id="00678-354">登録を解除する必要がある場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="00678-354">If you need to unregister, use the following command.</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

<span data-ttu-id="00678-355">プロバイダーが登録されると、追加の詳細は、**イベント ビューア** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** の新しい配置について記録されます。</span><span class="sxs-lookup"><span data-stu-id="00678-355">After providers are registered, additional details will be logged about the new deployment in **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Dynamics**.</span></span>

- <span data-ttu-id="00678-356">MR-Logger</span><span class="sxs-lookup"><span data-stu-id="00678-356">MR-Logger</span></span>
- <span data-ttu-id="00678-357">MR-Sql</span><span class="sxs-lookup"><span data-stu-id="00678-357">MR-Sql</span></span>

### <a name="error-while-executing-addaxdatabasechangetracking"></a><span data-ttu-id="00678-358">AddAXDatabaseChangeTracking の実行中のエラー</span><span class="sxs-lookup"><span data-stu-id="00678-358">Error while executing AddAXDatabaseChangeTracking</span></span>
<span data-ttu-id="00678-359">AddAXDatabaseChangeTracking を Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess (DeploymentCmdlet) での実行中にエラーが発生した場合は、フル パスが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-359">If you encounter an error while executing AddAXDatabaseChangeTracking at Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet), verify that the full path is correct.</span></span> <span data-ttu-id="00678-360">たとえば、ax.d365ffo.onprem.contoso.com。エラーはスター/\* 証明書の問題が原因で発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-360">For example, ax.d365ffo.onprem.contoso.com. The error may have also occurred because of an issue with the star/\* certificate.</span></span> <span data-ttu-id="00678-361">たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効なまたはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。</span><span class="sxs-lookup"><span data-stu-id="00678-361">For example, the remote certificate CN=\*.d365ffo.onprem.contoso.com has a name that is not valid or does not match the host ax.d365ffo.onprem.contoso.com.</span></span>

### <a name="remote-name-cant-be-resolved"></a><span data-ttu-id="00678-362">リモート名を解決できません</span><span class="sxs-lookup"><span data-stu-id="00678-362">Remote name can't be resolved</span></span>
<span data-ttu-id="00678-363">リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService をリッスンしていたエンドポイントはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="00678-363">The remote name could not be resolved: 'x.d365fo.onprem.contoso.com' / There was no endpoint listening at https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService that could accept the message.</span></span> <span data-ttu-id="00678-364">これは、しばしば正しくないアドレスまたは SOAP アクションによって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="00678-364">This is often caused by an incorrect address or SOAP action.</span></span> <span data-ttu-id="00678-365">URL を手動で参照することによってアドレスに到達可能なことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-365">Verify that the address is reachable by manually browsing to the URL.</span></span> <span data-ttu-id="00678-366">詳細については、存在する場合は InnerException を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-366">See InnerException, if present, for more details.</span></span>

### <a name="run-initialize-database-script-and-validate-dbs-have-correct-users"></a><span data-ttu-id="00678-367">データベース初期化スクリプトを実行し、DB のユーザーが適切であることを検証</span><span class="sxs-lookup"><span data-stu-id="00678-367">Run initialize database script and validate DBs have correct users</span></span>
<span data-ttu-id="00678-368">AddAXDatabaseChangeTracking イベントのみを受け取った場合は、https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService にアクセスし、Dynamics 365 for Finance and Operations の Metadataservice にアクセスしてみてください。</span><span class="sxs-lookup"><span data-stu-id="00678-368">If you only receive the AddAXDatabaseChangeTracking event, try to reach the Metadataservice of Dynamics 365 for Finance and Operations by going to https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService.</span></span>
<span data-ttu-id="00678-369">次に、wif.config ファイルでサービスの証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-369">Next, check the certificates of the service in the wif.config file.</span></span> <span data-ttu-id="00678-370">ファイルを検索するには、AOS ボックスにログオンし、タスク マネージャを使用して **AxService.exe** を右クリックし、**ファイルの場所を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00678-370">To find the file, log on to one of the AOS boxes and, using Task manager, locate **AxService.exe**, right-click and select **Open file location**.</span></span> <span data-ttu-id="00678-371">wif.config ファイルでは、3 つの拇印を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-371">In the wif.config file, you should see 3 thumbprints.</span></span> <span data-ttu-id="00678-372">これらの拇印に関する次の要件に注意してください。</span><span class="sxs-lookup"><span data-stu-id="00678-372">Note the following requirements for these thumbprints:</span></span>

- <span data-ttu-id="00678-373">これらは別にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-373">They need to be different.</span></span>
- <span data-ttu-id="00678-374">これらは、この順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-374">They need to be in this order:</span></span>
    1. <span data-ttu-id="00678-375">Financialreporting 拇印</span><span class="sxs-lookup"><span data-stu-id="00678-375">Financialreporting Thumbprint</span></span>
    2. <span data-ttu-id="00678-376">ReportingService 拇印</span><span class="sxs-lookup"><span data-stu-id="00678-376">ReportingService Thumbprint</span></span>
    3. <span data-ttu-id="00678-377">SessionAuthentication 拇印</span><span class="sxs-lookup"><span data-stu-id="00678-377">SessionAuthentication Thumbprint</span></span>

<span data-ttu-id="00678-378">拇印が要件のリストにない場合は、適切な拇印で LCS から再展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-378">If the thumbprints do not follow the list of requirements, you must redeploy from LCS with proper thumbprints.</span></span>

## <a name="axdbadmin-is-unable-to-connect-to-the-database-server-sql-lscontosocom"></a><span data-ttu-id="00678-379">axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。</span><span class="sxs-lookup"><span data-stu-id="00678-379">axdbadmin is unable to connect to the database server SQL-LS.contoso.com</span></span>

<span data-ttu-id="00678-380">理由: AX データベースに接続するためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="00678-380">Reason: The user does not have permission to connect to the AX database.</span></span>

<span data-ttu-id="00678-381">解決する手順:</span><span class="sxs-lookup"><span data-stu-id="00678-381">Steps to resolve:</span></span>

1. <span data-ttu-id="00678-382">既に存在する場合はデータベースから axdbadmin ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-382">Remove the axdbadmin user from the database if it already exists.</span></span>
2. <span data-ttu-id="00678-383">ConfigTemplate.xml ファイルの AX データベースに追加する必要があるユーザー名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="00678-383">Make sure you specify the username that needs to be added to the AX database in the ConfigTemplate.xml file.</span></span>
    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```
3. <span data-ttu-id="00678-384">axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-384">Run the initialize database script again to add the axdbadmin user.</span></span>

## <a name="unable-to-resolve-the-xpath-value"></a><span data-ttu-id="00678-385">xPath 値を解決することができません。</span><span class="sxs-lookup"><span data-stu-id="00678-385">Unable to resolve the xPath value</span></span>
<span data-ttu-id="00678-386">[TopologyInstance/CustomizationGroup[@name='ServiceConfiguration']/Group[@name='AOSServicePrincipalUser']/Customizations/Customization[@"fieldName="'PrincipalUserAccountPassword']/@selectedValue の xPath 値を解決できないことは、期待される動作であり問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="00678-386">Not being able to resolve the xPath value of [TopologyInstance/CustomizationGroup[@name='ServiceConfiguration']/Group[@name='AOSServicePrincipalUser']/Customizations/Customization[@"fieldName="'PrincipalUserAccountPassword']/@selectedValue is expected behavior and is not an issue.</span></span> <span data-ttu-id="00678-387">xPath 値は AOS ランタイム ユーザー情報を検索しますが、セキュリティが統合されているため、情報は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="00678-387">The xPath value is looking for AOS runtime user information, however, because of integrated security, the information is not needed.</span></span> <span data-ttu-id="00678-388">別の理由でエラーを調査する必要がある場合は、xPath を解決できないことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="00678-388">The inability to resolve the xPath is communicated in case the failure needs to be investigated for another reason.</span></span>

## <a name="adfs"></a><span data-ttu-id="00678-389">ADFS</span><span class="sxs-lookup"><span data-stu-id="00678-389">ADFS</span></span>
### <a name="login-page-not-redirecting"></a><span data-ttu-id="00678-390">リダイレクトしないログイン ページ</span><span class="sxs-lookup"><span data-stu-id="00678-390">Login page not redirecting</span></span>
<span data-ttu-id="00678-391">ログイン ページがリダイレクトされず、資格情報の入力を求められている場合、またはリダイレクトされているが、"エラーが発生しています" というメッセージを受信する場合。</span><span class="sxs-lookup"><span data-stu-id="00678-391">If the Login page is not redirecting and is still prompting for credentials, or you are being redirected but receive the message, "An error occurred.</span></span> <span data-ttu-id="00678-392">詳細については、管理者にお問い合わせください」は、次の操作を実行して問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="00678-392">Contact your administrator for more information.", you can do the following to resolve the issue:</span></span>

- <span data-ttu-id="00678-393">信頼済サイトに ADFS リンクを追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-393">Add ADFS link to trusted sites.</span></span>
- <span data-ttu-id="00678-394">信頼済サイトに Dynamics 365 リンクを追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-394">Add Dynamics 365 link to trusted sites.</span></span>
- <span data-ttu-id="00678-395">末尾にスラッシュ「/」を追加して、動作が変更されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-395">Try adding a trailing slash '/' to see if the behavior changes.</span></span>

<span data-ttu-id="00678-396">**ADFS** > **アプリケーション グループ** に順に移動して、AD FS マネージャーを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-396">Verify the AD FS Manager by going to **ADFS** > **Application groups**.</span></span> <span data-ttu-id="00678-397">**Microsoft Dynamics 365 for Operations on-premises** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="00678-397">Double-click **Microsoft Dynamics 365 for Operations on-premises**.</span></span> <span data-ttu-id="00678-398">**ネイティブ アプリケーション** で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="00678-398">Under **Native application**, double-click **Microsoft Dynamics 365 for Operations on-premises - Native application**.</span></span>
- <span data-ttu-id="00678-399">リダイレクト URI に注意してください。</span><span class="sxs-lookup"><span data-stu-id="00678-399">Note the Redirect URI.</span></span> <span data-ttu-id="00678-400">Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-400">It should match the DNS forward lookup zone for Finance and Operations.</span></span>

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a><span data-ttu-id="00678-401">エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」</span><span class="sxs-lookup"><span data-stu-id="00678-401">Error "Could not establish trust relationship for the SSL/TLS secure channel"</span></span>
<span data-ttu-id="00678-402">「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="00678-402">If you receive the error, "Could not establish trust relationship for the SSL/TLS secure channel", do the following:</span></span>

1. <span data-ttu-id="00678-403">**Service Fabric** > **クラスタ** > **アプリケーション** > **AXSFType** > **fabric:/AXSF** > **詳細**タブの順に移動し、 Aad\_AADMetadataLocationFormat / - Aad\_FederationMetadataLocation に移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-403">Go to **Service Fabric** > **Cluster** > **Applications** > **AXSFType** > **fabric:/AXSF** > **Details** tab and Aad\_AADMetadataLocationFormat / - Aad\_FederationMetadataLocation.</span></span> <span data-ttu-id="00678-404">次に、AOS からその URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="00678-404">Next, browse to that URL from AOS.</span></span>
2. <span data-ttu-id="00678-405">詳細については、**AOS イベント ビューアー** > **アプリケーションとサービス ログ**s > **Microsoft** > **Dynamics** > **AX-SystemRuntime** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-405">Go to **AOS Event Viewer** > **Applications and Services Log**s > **Microsoft** > **Dynamics** > **AX-SystemRuntime** for details.</span></span>
3. <span data-ttu-id="00678-406">ADFS 証明書が信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-406">Check to see if ADFS certificate is trusted:</span></span>
    1. <span data-ttu-id="00678-407">**ADFS マシン** > **サーバー マネージャー** > **ツール** > **AD FS 管理** に移動して、ADFS 証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-407">Verify ADFS certificate by going to **ADFS machine** > **Server Manager** > **Tools** > **AD FS Management**.</span></span>
    2. <span data-ttu-id="00678-408">**AD FS** > **サービス** > **証明書**展開し、証明書を注記します。</span><span class="sxs-lookup"><span data-stu-id="00678-408">Expand **AD FS** > **Service** > **Certificates** and note the certificates.</span></span> <span data-ttu-id="00678-409">たとえば、ex。</span><span class="sxs-lookup"><span data-stu-id="00678-409">For example, ex.</span></span> <span data-ttu-id="00678-410">dc1.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="00678-410">dc1.contoso.com.</span></span>
    3. <span data-ttu-id="00678-411">AOS コンピューターで、証明書マネージャーに移動し、**証明書** (ローカル コンピューター) > **信頼済ルート証明機関** > **証明書**および ADFS 証明書が表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-411">On the AOS machine, go to the Cert manager, **Certificates** (Local Computer) > **Trusted Root Certification Authorities** > **Certificates**  and verify that the ADFS certificate is listed.</span></span>
<span data-ttu-id="00678-412">サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていないからです。</span><span class="sxs-lookup"><span data-stu-id="00678-412">If you receive a message that the site isn't secure, this is because you haven't added your AD FS SSL certificate to the Trusted Root Certification Authorities store.</span></span>

### <a name="cant-connect-to-remote-server-in-some-locations"></a><span data-ttu-id="00678-413">一部の地域ではリモート サーバーに接続できません</span><span class="sxs-lookup"><span data-stu-id="00678-413">Can't connect to remote server in some locations</span></span>
<span data-ttu-id="00678-414">次の場所でリモート サーバーに接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="00678-414">If you are unable to connect to the remote server at the following places:</span></span>

- <span data-ttu-id="00678-415">System.Net.HttpWebRequest.GetResponse()</span><span class="sxs-lookup"><span data-stu-id="00678-415">System.Net.HttpWebRequest.GetResponse()</span></span>
- <span data-ttu-id="00678-416">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span><span class="sxs-lookup"><span data-stu-id="00678-416">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span></span>
- <span data-ttu-id="00678-417">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn) `C:\ProgramData\SF\AOS_1\Fabric\work\Applications\AXSFType_App35\log` フォルダーに移動すると、エラーおよび出力ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="00678-417">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn) Go to the `C:\ProgramData\SF\AOS_1\Fabric\work\Applications\AXSFType_App35\log` folder where you get the error and out files.</span></span>
<span data-ttu-id="00678-418">out ファイルには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="00678-418">The out file contains the following information:</span></span>

- <span data-ttu-id="00678-419">System.Net.WebException: リモート サーバーに接続できません ---></span><span class="sxs-lookup"><span data-stu-id="00678-419">System.Net.WebException: Unable to connect to the remote server ---></span></span>
- <span data-ttu-id="00678-420">System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="00678-420">System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond x.x.x.x:443</span></span>

<span data-ttu-id="00678-421">Psping を使用してリモート サーバーに対する接続を試みることもできます。</span><span class="sxs-lookup"><span data-stu-id="00678-421">You can also use Psping to try to reach the remote server.</span></span> <span data-ttu-id="00678-422">Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-422">For information about Psping, see [Psping](/sysinternals/downloads/psping).</span></span>

### <a name="redirect-login-questions-and-issues"></a><span data-ttu-id="00678-423">ログイン時の質問および問題をリダイレクト</span><span class="sxs-lookup"><span data-stu-id="00678-423">Redirect login questions and issues</span></span>
<span data-ttu-id="00678-424">ログインに問題が発生した場合は、Service Fabric Explorer で **Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-424">If you are having issues with login, verify in Service Fabric Explorer that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** are valid.</span></span> <span data-ttu-id="00678-425">次にその例を示します。</span><span class="sxs-lookup"><span data-stu-id="00678-425">For example,</span></span>

- <span data-ttu-id="00678-426">**Provisioning\_AdminPrincipalName** は AXServiceUser@contoso.com になります</span><span class="sxs-lookup"><span data-stu-id="00678-426">**Provisioning\_AdminPrincipalName** would be AXServiceUser@contoso.com</span></span>
- <span data-ttu-id="00678-427">**Provisioning\_AdminIdentityProvider** は https://DC1.contoso.com/adfs になります</span><span class="sxs-lookup"><span data-stu-id="00678-427">**Provisioning\_AdminIdentityProvider** would be https://DC1.contoso.com/adfs</span></span>

<span data-ttu-id="00678-428">有効でない場合は、続行することはできませんし、LCS から再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-428">If they are not valid, you will not be able to proceed and you will need to redeploy from LCS.</span></span>

<span data-ttu-id="00678-429">**Reset-DatabaseUsers.ps1** を使用した場合、変更内容を有効にするには、Dynamics サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-429">If you used **Reset-DatabaseUsers.ps1**, you will need to restart the Dynamics Service for your changes to take effect.</span></span> <span data-ttu-id="00678-430">ログインの問題がまだある場合は、**USERINFO** テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** を記録します。</span><span class="sxs-lookup"><span data-stu-id="00678-430">If you are still having login issues, in the **USERINFO** table, note the **NETWORKDOMAIN** and **NETWORKALIAS**.</span></span> <span data-ttu-id="00678-431">次にその例を示します。</span><span class="sxs-lookup"><span data-stu-id="00678-431">For example,</span></span>

- <span data-ttu-id="00678-432">NETWORKDOMAIN の例 https://DC1.contoso.com/adfs</span><span class="sxs-lookup"><span data-stu-id="00678-432">NETWORKDOMAIN example https://DC1.contoso.com/adfs</span></span>
- <span data-ttu-id="00678-433">NETWORKALIAS の例 AXServiceUser@contoso.com</span><span class="sxs-lookup"><span data-stu-id="00678-433">NETWORKALIAS example AXServiceUser@contoso.com</span></span>

<span data-ttu-id="00678-434">ADFS マシンで、**サーバー マネージャー** > **ツール** > **AD FS の管理** > **サービス**に移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-434">In the ADFS machine, go to **Server Manager** > **Tools** > **AD FS Management** > **Service**.</span></span> <span data-ttu-id="00678-435">**フェデレーション サービス プロパティの保守と編集** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="00678-435">Right-click **Service and Edit Federation Service Properties**.</span></span> <span data-ttu-id="00678-436">フェデレーション サービスの識別子は、**USERINFO.NETWORKDOMAIN (https://DC1.contoso.com/adfs)** と一致させる必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00678-436">Note the Federation Service identifier, which should match the **USERINFO.NETWORKDOMAIN (https://DC1.contoso.com/adfs)**.</span></span> <span data-ttu-id="00678-437">両方とも **USERINFO** の HTTPS であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-437">Verify that both are HTTPS in **USERINFO**.</span></span>

<span data-ttu-id="00678-438">ADFS マシンで、**イベント ビューアー** > **アプリケーションとサービス ログ** > **AD FS** > **管理者**に移動してエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-438">In the ADFS machine, go to **Event Viewer** > **Applications and Services Logs** > **AD FS** > **Admin** and note any errors.</span></span>

## <a name="login-issues"></a><span data-ttu-id="00678-439">ログインの問題</span><span class="sxs-lookup"><span data-stu-id="00678-439">Login issues</span></span>
<span data-ttu-id="00678-440">ユーザーや他のユーザーがログインの問題を経験している場合は、Service Fabric Explorer で Provisioning\_AdminPrincipalName および Provisioning\_AdminIdentityProvider が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-440">If you or others are experiencing login issues, verify in Service Fabric Explorer that Provisioning\_AdminPrincipalName and Provisioning\_AdminIdentityProvider is valid.</span></span> <span data-ttu-id="00678-441">有効な場合は、主要 SQL Server マシンで次を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-441">If it is valid, then on the primary SQL Server machine, run the following.</span></span>

```powershell
.\Reset-DatabaseUsers.ps1
```

<span data-ttu-id="00678-442">各 AOS で、タスク マネージャーを開き、AXService.exe を選択し、**タスクの終了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00678-442">On each AOS, open Task Manager, select AXService.exe, and then click **End task**.</span></span>
<span data-ttu-id="00678-443">ユーザーがリセットされたことを確認するには、SQL AXDB で次の select クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-443">To verify that a user has been reset, run the following select query in the SQL AXDB.</span></span>

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> <span data-ttu-id="00678-444">AAD 環境 (オンライン) の SID は、ネットワーク エイリアスとネットワーク ドメインのハッシュです。</span><span class="sxs-lookup"><span data-stu-id="00678-444">SID in AAD environment (online) is a hash of network alias and network domain.</span></span> <span data-ttu-id="00678-445">AD 環境 (オンプレミス) の SID は、ネットワーク エイリアスのハッシュであり、プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="00678-445">SID in AD environment (on-premises) is a hash of network alias and identify provider.</span></span>

<span data-ttu-id="00678-446">まだログインできず、"現在の資格情報でログインする権限がありません" というエラー メッセージが表示されている場合。</span><span class="sxs-lookup"><span data-stu-id="00678-446">If you are still unable to log in and you are receiving the error, "You are not authorized to login with your current credentials.</span></span> <span data-ttu-id="00678-447">数秒すると、ログイン ページにリダイレクトされます。このトピックの [ADFS](#ADFS) のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-447">You will be redirected to the login page in a few seconds", see the section, [ADFS](#ADFS) in this topic.</span></span>

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a><span data-ttu-id="00678-448">System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)</span><span class="sxs-lookup"><span data-stu-id="00678-448">System.Data.SqlClient.SqlException (0x80131904) and System.ComponentModel.Win32Exception (0x80004005)</span></span>
<span data-ttu-id="00678-449">次のエラーのいずれかが表示された場合:</span><span class="sxs-lookup"><span data-stu-id="00678-449">If you receive one of the following errors:</span></span>

- <span data-ttu-id="00678-450">System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、ログイン プロセス時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="00678-450">System.Data.SqlClient.SqlException (0x80131904): A connection was successfully established with the server, but then an error occurred during the login process.</span></span> <span data-ttu-id="00678-451">(プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)</span><span class="sxs-lookup"><span data-stu-id="00678-451">(provider: SSL Provider, error: 0 - The certificate chain was issued by an authority that is not trusted.)</span></span>
- <span data-ttu-id="00678-452">System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました</span><span class="sxs-lookup"><span data-stu-id="00678-452">System.ComponentModel.Win32Exception (0x80004005): The certificate chain was issued by an authority that is not trusted</span></span>

<span data-ttu-id="00678-453">証明書がインストールされていないか、正しいユーザーにアクセス権が与えられていません。</span><span class="sxs-lookup"><span data-stu-id="00678-453">The certificates have not been installed or given access to the correct users.</span></span> <span data-ttu-id="00678-454">このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-454">To resolve this error, add the public key SQL server certificate to all of the Service Fabric nodes.</span></span>

## <a name="keyset-doesnt-exist"></a><span data-ttu-id="00678-455">Keyset が存在しません</span><span class="sxs-lookup"><span data-stu-id="00678-455">Keyset doesn't exist</span></span>
<span data-ttu-id="00678-456">キーセットが存在しないことを検索する場合は、すべてのコンピューターでスクリプトが実行されなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="00678-456">If you find that the keyset doesn't exist, this means that scripts were not run on all machines.</span></span> <span data-ttu-id="00678-457">環境の VM の設定を確認および完了します。</span><span class="sxs-lookup"><span data-stu-id="00678-457">Review and complete Set up VMs for your environments.</span></span>
- [<span data-ttu-id="00678-458">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-458">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupvms)
- [<span data-ttu-id="00678-459">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="00678-459">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupvms)

<span data-ttu-id="00678-460">各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="00678-460">Copy the scripts in each folder to the VMs that correspond to the folder name.</span></span>

<span data-ttu-id="00678-461">また正しいドメインを使用していることを確認する .csv ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-461">Also check the .csv file to verify that the correct domain is being used.</span></span>

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a><span data-ttu-id="00678-462">エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」</span><span class="sxs-lookup"><span data-stu-id="00678-462">Error "RunAsync failed due to an unhandled FabricException causing replica to fault"</span></span>
<span data-ttu-id="00678-463">「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException:」というこのエラーが発生した場合は、最初の織物アップグレードでは、コード バージョンと設定バージョンの両方を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-463">If you receive this error, "RunAsync failed due to an unhandled FabricException causing replica to fault: System.Fabric.FabricException: The first Fabric upgrade must specify both the code and config versions.</span></span> <span data-ttu-id="00678-464">要求された値: 0.0.0.0:"。ClusterConfig.json 診断を変更します。ネットワーク共有からローカル パスに保存します。`\\server\path` から既定値の `C:\ProgramData\SF\DiagnosticsStore` など。</span><span class="sxs-lookup"><span data-stu-id="00678-464">Requested value: 0.0.0.0:", change the ClusterConfig.json diagnosticsStore from network share to local path such as, `\\server\path` to default of `C:\ProgramData\SF\DiagnosticsStore`.</span></span>

## <a name="error-dbsync-db-sync-issues"></a><span data-ttu-id="00678-465">エラー、Dbsync (DB 同期) の問題</span><span class="sxs-lookup"><span data-stu-id="00678-465">Error Dbsync (DB sync) issues</span></span>
<span data-ttu-id="00678-466">データベースの同期の問題が発生した場合、AOS の作業ディレクトリ、ex `C:\ProgramData\SF\AOS1\Fabric\work\Applications\AXSFType_App8\log` を参照し、すべての AOS コンピューターで次の確認を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-466">If you are having database sync issues, look at AOS working directory, ex `C:\ProgramData\SF\AOS1\Fabric\work\Applications\AXSFType_App8\log` and complete a review of the following on all AOS machines:</span></span>

- <span data-ttu-id="00678-467">**イベント ビューアー** > **カスタム ビュー** > **管理イベント**</span><span class="sxs-lookup"><span data-stu-id="00678-467">**Event Viewer** > **Custom Views** > **Administrative Events**</span></span>
- <span data-ttu-id="00678-468">**イベント ビューアー** > **アプリケーションおよびサービス ログ** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize**</span><span class="sxs-lookup"><span data-stu-id="00678-468">**Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize**</span></span>

## <a name="service-fabric-aos-node-error-during-build-execution-timeout-expired"></a><span data-ttu-id="00678-469">ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ</span><span class="sxs-lookup"><span data-stu-id="00678-469">Service Fabric AOS Node Error during build: Execution Timeout Expired</span></span>
<span data-ttu-id="00678-470">エラー メッセージ:</span><span class="sxs-lookup"><span data-stu-id="00678-470">Error message:</span></span>

```
The timeout period elapsed prior to completion of the operation or the server is not responding.
The statement has been terminated.
```

<span data-ttu-id="00678-471">一度に 1 つの AOS マシンのみ DB Sync できます。</span><span class="sxs-lookup"><span data-stu-id="00678-471">Only one AOS machine can DB Sync at a time.</span></span> <span data-ttu-id="00678-472">これは、AOS VM の 1 つが DB Sync を実行していて、他が警告を出すことができないために、このエラー メッセージは無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="00678-472">This error message is safe to ignore, as it means that one of the AOS VMs is running DB Sync, and the others yield a warning that they cannot.</span></span> <span data-ttu-id="00678-473">DB の同期が実行されているという事実は、警告を発していない AOS VM の **イベント ビューアー** > **アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize/Operational** の順に確認して検証できます。</span><span class="sxs-lookup"><span data-stu-id="00678-473">The fact that DB Sync is running can be verified by checking **Event Viewer** > **Applications and Services Log** > **Microsoft** > **Dynamics** > **AX-DatabaseSynchronize/Operational** on the AOS VM that is not yielding warnings.</span></span>

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a><span data-ttu-id="00678-474">エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」</span><span class="sxs-lookup"><span data-stu-id="00678-474">Error "RequireNonce is 'true' (default) but validationContext.Nonce is null"</span></span>
<span data-ttu-id="00678-475">AX にログイン後 Internet Explorer で HTTP エラー 500 としても表示されます。</span><span class="sxs-lookup"><span data-stu-id="00678-475">Also shows as a HTTP Error 500 in Internet Explorer after logging in to AX.</span></span> <span data-ttu-id="00678-476">Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。</span><span class="sxs-lookup"><span data-stu-id="00678-476">The issued nonce can not be validated if Internet Explorer is in Enhanced Security Configuration.</span></span>

<span data-ttu-id="00678-477">AX にログインするには、サーバー マネージャーを使用して Internet Explorer のセキュリティ強化設定を無効にします。</span><span class="sxs-lookup"><span data-stu-id="00678-477">Disable Enhanced Security Configuration for Internet Explorer via the Server Manager, in order to log in to AX.</span></span>

## <a name="error-invalid-algorithm-specified--cryptography"></a><span data-ttu-id="00678-478">エラー、「無効なアルゴリズムが指定されている/暗号化」</span><span class="sxs-lookup"><span data-stu-id="00678-478">Error "Invalid algorithm specified / Cryptography"</span></span>
<span data-ttu-id="00678-479">このエラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-479">If you receive this error, you need to be using the Microsoft Enhanced RSA and AES Cryptographic Provider.</span></span> <span data-ttu-id="00678-480">詳細については、証明書の要求を確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-480">For more information, review the certificates requirements.</span></span> <span data-ttu-id="00678-481">また、credentials.json ファイルの構造が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-481">Additionally, verify that the structure of the credentials.json file is correct.</span></span>

<span data-ttu-id="00678-482">正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="00678-482">If you need to re-create the certificate using the correct provider, follow these steps:</span></span>

1. <span data-ttu-id="00678-483">正しいプロバイダーを使用して証明書を再度作成します。</span><span class="sxs-lookup"><span data-stu-id="00678-483">Create the certificate again with the correct provider.</span></span>
1. <span data-ttu-id="00678-484">ConfigTemplate.xml の変更</span><span class="sxs-lookup"><span data-stu-id="00678-484">Change ConfigTemplate.xml</span></span>
1. <span data-ttu-id="00678-485">クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、Test-D365FOConfiguration.ps1 スクリプトに合格するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-485">Run the infrastructure scripts on all machines in the cluster, and make sure the Test-D365FOConfiguration.ps1 script passes.</span></span>
1. <span data-ttu-id="00678-486">LCS から環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="00678-486">Reconfigure the environment from LCS.</span></span>

## <a name="error-partition-is-below-target-replica-or-instance-count"></a><span data-ttu-id="00678-487">エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」</span><span class="sxs-lookup"><span data-stu-id="00678-487">Error "Partition is below target replica or instance count"</span></span>
<span data-ttu-id="00678-488">これはルート エラーではありません。</span><span class="sxs-lookup"><span data-stu-id="00678-488">This is not a root error.</span></span> <span data-ttu-id="00678-489">このエラーは、各ノードのステータスが準備できていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="00678-489">This error means that the status of each node is not ready.</span></span> <span data-ttu-id="00678-490">AXSF/AOS で、ステータスがまだ inBuild である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-490">For AXSF/AOS, the status could still be inBuild.</span></span>
<span data-ttu-id="00678-491">イベント ビューアーに移動してルート エラーを取得します。</span><span class="sxs-lookup"><span data-stu-id="00678-491">Navigate to the Event Viewer to get root error.</span></span>

## <a name="error-unable-to-find-certificate-when-running-test-d365foconfigurationps1"></a><span data-ttu-id="00678-492">エラー、「証明書を検出できません」 Test-D365FOConfiguration.ps1 を実行した場合</span><span class="sxs-lookup"><span data-stu-id="00678-492">Error "Unable to find certificate" when running Test-D365FOConfiguration.ps1</span></span>
<span data-ttu-id="00678-493">このエラーが表示された場合は、証明書/拇印が複数の目的で結合されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00678-493">If you receive this error, check to see if certificates/thumbprints are being combined for multiple purposes.</span></span> <span data-ttu-id="00678-494">たとえば、クライアントおよび SessionAuthentication が結合される場合、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="00678-494">For example, if the client and SessionAuthentication is combined, you will receive this error.</span></span> <span data-ttu-id="00678-495">証明書を結合しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00678-495">We recommend that you do not to combine certificates.</span></span> <span data-ttu-id="00678-496">詳細については、「証明書の要件および domain.com\user 対 domain\user (ex の acl.csv を確認する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-496">For more information, see the certificate requirements and check acl.csv for domain.com\user vs. domain\user (ex.</span></span> <span data-ttu-id="00678-497">NETBIOS 構造体)。</span><span class="sxs-lookup"><span data-stu-id="00678-497">NETBIOS structure).</span></span>

## <a name="client-and-server-cant-communicate-because-they-do-not-have-a-common-algorithm"></a><span data-ttu-id="00678-498">クライアントとサーバーは共通のアルゴリズムを持たないため通信できません</span><span class="sxs-lookup"><span data-stu-id="00678-498">Client and server can't communicate because they do not have a common algorithm</span></span>
<span data-ttu-id="00678-499">これが発生した場合、作成された証明書で、手順 2 で説明されているように指定されたプロバイダーが使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-499">If this occurs, verify that the certificates created are using the specified provider as explained in step 2.</span></span> <span data-ttu-id="00678-500">環境の証明書を計画し、取得します。</span><span class="sxs-lookup"><span data-stu-id="00678-500">Plan and acquire your certificates for your environment.</span></span> 
- [<span data-ttu-id="00678-501">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="00678-501">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#plancert)
- [<span data-ttu-id="00678-502">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="00678-502">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts-gmsa"></a><span data-ttu-id="00678-503">グループ管理サービス アカウント (gMSA) の一覧を検索します</span><span class="sxs-lookup"><span data-stu-id="00678-503">Find a list of group managed service accounts (gMSA)</span></span>
<span data-ttu-id="00678-504">すべてのグループとホストの一覧を検索するには、`Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-504">To find a list of all groups and hosts, see `Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword`</span></span>

## <a name="addcerttoserviceprincipal-script-failing-on-import-module"></a><span data-ttu-id="00678-505">Import-Module での AddCertToServicePrincipal スクリプトの失敗</span><span class="sxs-lookup"><span data-stu-id="00678-505">AddCertToServicePrincipal script failing on Import-Module</span></span>
<span data-ttu-id="00678-506">Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="00678-506">AddCertToServicePrincipal script failing on Import-Module : Could not load file or assembly 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span> <span data-ttu-id="00678-507">厳密な名前の検証に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="00678-507">Strong name validation failed.</span></span> <span data-ttu-id="00678-508">(HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="00678-508">(Exception from HRESULT: 0x8013141A) may have multiple versions of the same module installed.</span></span>

<span data-ttu-id="00678-509">この問題を解決するには、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-509">To resolve this issue, run the following command in PowerShell.</span></span>

```powershell
Uninstall-Module -Name AzureRM
Install-Module AzureRM
```

<span data-ttu-id="00678-510">PowerShell ウィンドウを閉じて、もう一度やり直してください。</span><span class="sxs-lookup"><span data-stu-id="00678-510">Close the PowerShell window and try again.</span></span>

## <a name="reportingservicessetupexe-error"></a><span data-ttu-id="00678-511">ReportingServicesSetup.exe エラー</span><span class="sxs-lookup"><span data-stu-id="00678-511">ReportingServicesSetup.exe Error</span></span>
<span data-ttu-id="00678-512">ReportingServicesSetup.exe エラー: 0 : アプリケーション ファブリック:/10 分後、ReportingService は OK ではありません。アプリケーション: ReportingServicesBootstrapper.exe フレームワーク バージョン v4.0.30319 説明: 未処理の例外により、プロセスが中止されました。</span><span class="sxs-lookup"><span data-stu-id="00678-512">ReportingServicesSetup.exe Error: 0 : Application fabric:/ReportingService is not OK after 10 minutes Application: ReportingServicesBootstrapper.exe Framework Version: v4.0.30319 Description: The process was terminated due to an unhandled exception.</span></span>

<span data-ttu-id="00678-513">このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効化されます。</span><span class="sxs-lookup"><span data-stu-id="00678-513">If you receive this error, the strong name validation is enabled in the Reporting server and should not be.</span></span> <span data-ttu-id="00678-514">これを解決するには、レポート サーバー マシンで config-PreReq スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-514">To resolve this, run the config-PreReq script on the Reporting server machine.</span></span>

## <a name="requested-operation-requires-elevation"></a><span data-ttu-id="00678-515">要求された操作には、昇格が必要です</span><span class="sxs-lookup"><span data-stu-id="00678-515">Requested operation requires elevation</span></span>
<span data-ttu-id="00678-516">AOS ユーザーは、ローカル管理者グループに属しておらず、UAC は、正しく無効化されていません。</span><span class="sxs-lookup"><span data-stu-id="00678-516">AOS users are not in the local administrator group and the UAC has not been disabled correctly.</span></span> <span data-ttu-id="00678-517">この問題を解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-517">To resolve the issue, complete the following steps.</span></span>
1. <span data-ttu-id="00678-518">「VM のドメインへの参加」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="00678-518">Add AOS users as local admins as described in the section "Join VMs to the domain."</span></span>
2. <span data-ttu-id="00678-519">すべての AOS コンピューターで、Config-PreReq スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="00678-519">Run the Config-PreReq script on all the AOS machines.</span></span>
3. <span data-ttu-id="00678-520">テスト構成スクリプトがパスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00678-520">Make sure Test-Configuration script passes.</span></span>
4. <span data-ttu-id="00678-521">UAC が変更された場合は、有効にするマシンを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-521">If UAC was changed, you need to restart the machine to take effect.</span></span>

## <a name="files-in-use-errors"></a><span data-ttu-id="00678-522">使用中ファイルのエラー</span><span class="sxs-lookup"><span data-stu-id="00678-522">Files in use errors</span></span>
<span data-ttu-id="00678-523">Service Fabric により指示された除外ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="00678-523">Set up exclusion rules that are advised by Service Fabric.</span></span> <span data-ttu-id="00678-524">詳細については、「[Service Fabric のスタンドアロン クラスター展開の計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-524">For information, see [Plan and prepare your Service Fabric Standalone cluster deployment](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="apply-deployable-packages-during-deployment"></a><span data-ttu-id="00678-525">配置中に配置可能パッケージを適用する</span><span class="sxs-lookup"><span data-stu-id="00678-525">Apply deployable packages during deployment</span></span>
### <a name="package-deployment-fails-due-to-path-too-long-exception"></a><span data-ttu-id="00678-526">「パスが長過ぎる」例外によってパッケージの展開が失敗する</span><span class="sxs-lookup"><span data-stu-id="00678-526">Package deployment fails due to "path too long" exception</span></span>
<span data-ttu-id="00678-527">Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="00678-527">Because of a 260-character limit in Windows, deployment will fail if a package has a longer name, or if the on-premises share has the full FQDN path.</span></span> <span data-ttu-id="00678-528">文字数の制限を超過した場合、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00678-528">If the character limit is exceeded, you will receive the following error:</span></span>

<span data-ttu-id="00678-529">**System.IO.PathTooLongException: 指定したファイル パス、ファイル名、またはその両方が長すぎます。System.IO.PathHelper.GetFullPathName では、完全修飾ファイル名は 260 文字未満で、ディレクトリ名は 248 文字未満でなければなりません。**</span><span class="sxs-lookup"><span data-stu-id="00678-529">**System.IO.PathTooLongException: The specified path, file name, or both are too long. The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters. at System.IO.PathHelper.GetFullPathName**</span></span>

<span data-ttu-id="00678-530">このエラーを回避するには、パッケージ名を短くしてパッケージを再度適用するか、オンプレミス資産の共有パスの全長を短くします。</span><span class="sxs-lookup"><span data-stu-id="00678-530">To work around the error, shorten the package name and then apply the package again, or shorten the overall length of the share path for the on-premises assets.</span></span>

### <a name="package-deployment-fails-because-of-serialization-error"></a><span data-ttu-id="00678-531">シリアル化エラーが原因でがパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="00678-531">Package deployment fails because of serialization error</span></span>
<span data-ttu-id="00678-532">パッケージの配置中に、**シリアル化バージョンの不一致が検出。ランタイム DLLs が配置されたメタデータと同期していることを確認してください。ファイル「XXX」のバージョン。DLL 「XXX」のバージョン**というエラーが発生した場合、パッケージが配置されている環境とは異なるバージョンの環境でパッケージが開発された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-532">During package deployment, if you receive the error, **Serialization version mismatch detect, make sure the runtime DLLs are in sync with the deployed metadata. Version of file 'XXX'. Version of DLL 'XXX'**, it is likely that the package was developed on an environment that has a different version than the environment that the package is being deployed on.</span></span>
<span data-ttu-id="00678-533">この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。</span><span class="sxs-lookup"><span data-stu-id="00678-533">To work around this issue, keep the development or build environments on the same version as the deployed on-premises environment.</span></span> <span data-ttu-id="00678-534">パッケージのアップロード先にあるアセット ライブラリの **追加の詳細** セクションをクリックすることにより、パッケージ バージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="00678-534">You can confirm the package version by checking the **Additional details** section in the Asset library where the package is uploaded.</span></span> <span data-ttu-id="00678-535">エラーを修正するには、オンプレミス環境に展開されたバージョンと同じバージョンまたはそれ以前のバージョンにパッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="00678-535">To fix the error, generate the package on the same version or an earlier version as the version deployed on the on-premises environment.</span></span>

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a><span data-ttu-id="00678-536">欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="00678-536">Package deployment fails because of dependencies on missing modules</span></span>
<span data-ttu-id="00678-537">依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次と類似するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00678-537">If you are trying to apply a package that is missing dependent modules, the package application will fail with a message that is similar to the following:</span></span>

<span data-ttu-id="00678-538">**パッケージ [dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor]]**</span><span class="sxs-lookup"><span data-stu-id="00678-538">**Package [dynamicsax-My\_commonextension.7.0.4679.35176.nupkg has missing dependencies: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor]]**</span></span>

<span data-ttu-id="00678-539">**パッケージ [dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor]]**</span><span class="sxs-lookup"><span data-stu-id="00678-539">**Package [dynamicsax-My\_coreextension.7.0.4679.35176.nupkg has missing dependencies: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor]]**</span></span>

<span data-ttu-id="00678-540">**パッケージ [dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests]]**</span><span class="sxs-lookup"><span data-stu-id="00678-540">**Package [dynamicsax-My\_uiextension.7.0.4679.35176.nupkg has missing dependencies: [dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests]]**</span></span>

<span data-ttu-id="00678-541">問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーにログインし、アプリケーションとサービスを開き、**Microsoft** > **Dynamics** > **AX SetupModuleEvents** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00678-541">To confirm the issue and find the missing dependencies, log in to the Event Viewer, open the Application and Services, and go to **Microsoft** > **Dynamics** > **AX-SetupModuleEvents**.</span></span> <span data-ttu-id="00678-542">これにより、モジュールがないイベントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00678-542">This will show events that have missing modules.</span></span> <span data-ttu-id="00678-543">たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor モジュールです。</span><span class="sxs-lookup"><span data-stu-id="00678-543">For example, one of the common missing modules is the ApplicationFoundationFormAdaptor module.</span></span>
<span data-ttu-id="00678-544">この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-544">To fix this issue and apply the package successfully, add dependent modules or remove modules that require dependent modules.</span></span> <span data-ttu-id="00678-545">依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="00678-545">To add the dependent modules, you will need to include the dependencies when building the package.</span></span> <span data-ttu-id="00678-546">モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="00678-546">To remove the modules, you can use ModelUtil.exe to delete the module.</span></span> <span data-ttu-id="00678-547">詳細については、「[モデルのエクスポートとインポート](../dev-tools/models-export-import.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00678-547">For more information, see [Export and import a model](../dev-tools/models-export-import.md).</span></span>

### <a name="package-deployment-works-on-one-box-environment-but-not-in-the-sandbox-environment"></a><span data-ttu-id="00678-548">パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない</span><span class="sxs-lookup"><span data-stu-id="00678-548">Package deployment works on one-box environment but not in the sandbox environment</span></span>
<span data-ttu-id="00678-549">1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、サンドボックスには実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="00678-549">A one-box environment might have all of the modules installed and the sandbox only has the modules that are needed to run your production environment.</span></span> <span data-ttu-id="00678-550">パッケージを開発環境で構築が1つのシステムで環境に格納されているモジュールにこの依存関係いないサンド ボックス環境で、パッケージでは動作しませんサンド ボックス環境場合。</span><span class="sxs-lookup"><span data-stu-id="00678-550">If the package built in the dev environment takes a dependency on the modules that are present in the one-box environment but not in the sandbox environment, the package won't work in the sandbox environment.</span></span>
<span data-ttu-id="00678-551">この問題を解決するには、依存するすべてのモジュールを確認し、実稼動環境で不要なファーム アダプターまたはその他のモジュールをプルしないようにします。</span><span class="sxs-lookup"><span data-stu-id="00678-551">To resolve this issue, look at all of the modules that you are dependent on and ensure that you do not pull any farm adapter or any other modules that are not needed in the production environment.</span></span> <span data-ttu-id="00678-552">ビルド ボックスからパッケージを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00678-552">The best practice is to take the package from the build box.</span></span>

