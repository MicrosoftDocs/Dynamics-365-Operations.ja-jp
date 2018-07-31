---
title: "Microsoft Dynamics 365 for Finance and Operations のトラブルシューティング (オンプレミス)"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。"
author: sarvanisathish
manager: AnnBe
ms.date: 05/15/2018
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
ms.sourcegitcommit: 6c6c7c3f63b7a49820811a7ec80248b09b6e3acf
ms.openlocfilehash: b923eb0116feb052e8a9fda230f5b28191cf1b8d
ms.contentlocale: ja-jp
ms.lasthandoff: 06/19/2018

---
# <a name="troubleshoot-microsoft-dynamics-365-for-finance-and-operations-on-premises"></a><span data-ttu-id="8149e-103">Microsoft Dynamics 365 for Finance and Operations のトラブルシューティング (オンプレミス)</span><span class="sxs-lookup"><span data-stu-id="8149e-103">Troubleshoot Microsoft Dynamics 365 for Finance and Operations (on-premises)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8149e-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8149e-104">This topic provides troubleshooting information for on-premises deployments of Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="access-service-fabric-explorer"></a><span data-ttu-id="8149e-105">Service Fabric Explorer へのアクセス</span><span class="sxs-lookup"><span data-stu-id="8149e-105">Access Service Fabric Explorer</span></span>
<span data-ttu-id="8149e-106">Service Fabric Explorer には、Web ブラウザーと既定のアドレス `https://sf.d365ffo.onprem.contoso.com:19080` を使ってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8149e-106">You can access Service Fabric Explorer in a web browser by using the default address, `https://sf.d365ffo.onprem.contoso.com:19080`.</span></span>

<span data-ttu-id="8149e-107">アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。</span><span class="sxs-lookup"><span data-stu-id="8149e-107">To verify the address, note the value that was used in the "Create DNS zones and add A records" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="8149e-108">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-108">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#createdns)
- [<span data-ttu-id="8149e-109">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-109">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#createdns)

<span data-ttu-id="8149e-110">クライアント証明書が、サイトにアクセスするマシンの証明書、cert:\\CurrentUser\\My に含まれている場合のみ、サイトにアクセスできます</span><span class="sxs-lookup"><span data-stu-id="8149e-110">You can access the site only if the client certificate is in cert:\\CurrentUser\\My on the machine that you're accessing the site on.</span></span> <span data-ttu-id="8149e-111">(証明書マネージャーで、**証明書 - 現在のユーザー** \> **個人** \> **証明書**に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149e-111">(In Certificate Manger, go to **Certificates - Current User** \> **Personal** \> **Certificates**.) When you access the site, select the client certificate when you're prompted.</span></span>

## <a name="monitor-the-deployment"></a><span data-ttu-id="8149e-112">配置の監視</span><span class="sxs-lookup"><span data-stu-id="8149e-112">Monitor the deployment</span></span>

### <a name="identify-the-primary-orchestrator"></a><span data-ttu-id="8149e-113">プライマリ オーケストレータを識別します。</span><span class="sxs-lookup"><span data-stu-id="8149e-113">Identify the primary orchestrator</span></span>
<span data-ttu-id="8149e-114">Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスであるマシンを判別するには、**クラスター** \> **アプリケーション** \> **\<*対象のアプリケーションの例*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="8149e-114">To determine the machine that is the primary instance for stateful services such as a local agent, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **\<*intended application example*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

<span data-ttu-id="8149e-115">プライマリ ノードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-115">The primary node is shown.</span></span> <span data-ttu-id="8149e-116">ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-116">For stateless services or the remaining applications, you must check all the nodes.</span></span>

<span data-ttu-id="8149e-117">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="8149e-117">Note the following points:</span></span>

- <span data-ttu-id="8149e-118">OrchestrationService は、Finance and Operations の配置およびサービス アクションを調整します。</span><span class="sxs-lookup"><span data-stu-id="8149e-118">OrchestrationService orchestrates the deployment and servicing actions for Finance and Operations.</span></span>
- <span data-ttu-id="8149e-119">ArtifactsManager は、ファイルを Microsoft Azure クラウド ストレージからローカル エージェント ファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8149e-119">ArtifactsManager downloads files from Microsoft Azure cloud storage to the local agent file share.</span></span> <span data-ttu-id="8149e-120">ファイルを必要な形式にも解凍します。</span><span class="sxs-lookup"><span data-stu-id="8149e-120">It also unzips the files into the required format.</span></span>

### <a name="review-the-orchestrator-event-logs"></a><span data-ttu-id="8149e-121">オーケストレータ イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="8149e-121">Review the orchestrator event logs</span></span>
<span data-ttu-id="8149e-122">プライマリ OrchestrationService オーケストレータ マシンから、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent** を確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-122">From the primary OrchestrationService orchestrator machine, in Event Viewer, review **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent**.</span></span>

<span data-ttu-id="8149e-123">完全なエラー メッセージを表示する**詳細**タブを選択する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-123">Note that you must select the **Details** tab to view the full error message.</span></span>

<span data-ttu-id="8149e-124">次のモジュールがインストールされます:</span><span class="sxs-lookup"><span data-stu-id="8149e-124">The following modules must be installed:</span></span>

- <span data-ttu-id="8149e-125">共通</span><span class="sxs-lookup"><span data-stu-id="8149e-125">Common</span></span>
- <span data-ttu-id="8149e-126">ReportingServices</span><span class="sxs-lookup"><span data-stu-id="8149e-126">ReportingServices</span></span>
- <span data-ttu-id="8149e-127">AOS</span><span class="sxs-lookup"><span data-stu-id="8149e-127">AOS</span></span>
- <span data-ttu-id="8149e-128">FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="8149e-128">FinancialReporting</span></span>

<span data-ttu-id="8149e-129">次のコマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-129">The following commands must be run:</span></span>

- <span data-ttu-id="8149e-130">段取り</span><span class="sxs-lookup"><span data-stu-id="8149e-130">Setup</span></span>
- <span data-ttu-id="8149e-131">Dvt (配置確認テスト)</span><span class="sxs-lookup"><span data-stu-id="8149e-131">Dvt (deployment verification test)</span></span>
- <span data-ttu-id="8149e-132">クリーンアップ (環境のサービスと削除のために使用)</span><span class="sxs-lookup"><span data-stu-id="8149e-132">Cleanup (used to service and delete an environment)</span></span>

<span data-ttu-id="8149e-133">次のフォルダには、追加の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8149e-133">The following folders contain additional information:</span></span>

- <span data-ttu-id="8149e-134">AX-SetupModuleEvents</span><span class="sxs-lookup"><span data-stu-id="8149e-134">AX-SetupModuleEvents</span></span> 
- <span data-ttu-id="8149e-135">AX-SetupInfrastructureEvents</span><span class="sxs-lookup"><span data-stu-id="8149e-135">AX-SetupInfrastructureEvents</span></span> 
- <span data-ttu-id="8149e-136">AX-BridgeService</span><span class="sxs-lookup"><span data-stu-id="8149e-136">AX-BridgeService</span></span> 

### <a name="service-fabric-explorer"></a><span data-ttu-id="8149e-137">Service Fabric Explorer</span><span class="sxs-lookup"><span data-stu-id="8149e-137">Service Fabric Explorer</span></span>
<span data-ttu-id="8149e-138">クラスタ、アプリケーション、およびノードの状態に注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-138">Note the state of the cluster, application, and nodes.</span></span> <span data-ttu-id="8149e-139">Service Fabric Explorer にアクセスする方法については、[Service Fabric Explorer にアクセスする](troubleshoot-on-prem.md#accessing-service-fabric-explorer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-139">For information about how to access Service Fabric Explorer, see [Accessing Service Fabric Explorer](troubleshoot-on-prem.md#accessing-service-fabric-explorer).</span></span>

#### <a name="error-partition-is-below-target-replica-or-instance-count"></a><span data-ttu-id="8149e-140">エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」</span><span class="sxs-lookup"><span data-stu-id="8149e-140">Error: "Partition is below target replica or instance count"</span></span>
<span data-ttu-id="8149e-141">このエラーはルート エラーではありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-141">This error isn't a root error.</span></span> <span data-ttu-id="8149e-142">各ノードのステータスが準備できていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-142">It indicates that the status of each node isn't ready.</span></span> <span data-ttu-id="8149e-143">AXSFType (AOS) では、ステータスがまだ **InBuild** である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-143">For AXSFType (AOS), the status might still be **InBuild**.</span></span>

<span data-ttu-id="8149e-144">エラー メッセージに関連するコンピューターでイベント ビューアーを使用して、最新の活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-144">Use Event Viewer on the machines related to the error message to view the latest activity.</span></span>

#### <a name="axsftype"></a><span data-ttu-id="8149e-145">AXSFType</span><span class="sxs-lookup"><span data-stu-id="8149e-145">AXSFType</span></span> 
<span data-ttu-id="8149e-146">AXSFType (AOS) では、**InBuild** ステータスが表示されている場合、DB Sync ステータスおよび Application Object Server (AOS) マシンからの他のイベントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-146">For AXSFType (AOS), if a status of **InBuild** is shown, review the DB Sync status and other events from Application Object Server (AOS) machines.</span></span>

<span data-ttu-id="8149e-147">エラーを診断するには、イベント ビューアーを使用して次のイベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-147">To diagnose errors, use Event Viewer to review the following event logs:</span></span>

- <span data-ttu-id="8149e-148">**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize**</span><span class="sxs-lookup"><span data-stu-id="8149e-148">**Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize**</span></span>
- <span data-ttu-id="8149e-149">**カスタム ビュー** \> **管理イベント**</span><span class="sxs-lookup"><span data-stu-id="8149e-149">**Custom Views** \> **Administrative Events**</span></span>

#### <a name="error-extractinstallerservice-failed-to-extract-cusersdynusercontosoappdatalocaltemp1blssblhw0nfabricinstallerservicecodefabricclientdll"></a><span data-ttu-id="8149e-150">エラー、「ExtractInstallerServiceは C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll の抽出に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="8149e-150">Error: "ExtractInstallerService failed to extract" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll.</span></span>
<span data-ttu-id="8149e-151">このエラーが発生した場合は、[Service Fabric](http://go.microsoft.com/fwlink/?LinkId=730690) の最新バージョンをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-151">If you receive this error, download the latest version of [Service Fabric](http://go.microsoft.com/fwlink/?LinkId=730690).</span></span> <span data-ttu-id="8149e-152">エラーでのユーザー名およびパスは、環境に基づいて変更されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-152">Note that the the username and path in the error will change according to your environment.</span></span>

#### <a name="service-fabric-logs"></a><span data-ttu-id="8149e-153">Service Fabric ログ</span><span class="sxs-lookup"><span data-stu-id="8149e-153">Service Fabric logs</span></span>
<span data-ttu-id="8149e-154">Azure Service Fabric アプリケーションの詳細については、次のログ ファイルを参照してください。C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log</span><span class="sxs-lookup"><span data-stu-id="8149e-154">You can find additional details about Azure Service Fabric applications in the log files at C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log.</span></span>

### <a name="lifecycle-services"></a><span data-ttu-id="8149e-155">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8149e-155">Lifecycle Services</span></span>
<span data-ttu-id="8149e-156">Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-156">Note the current deployment status for the environment in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="time-out-error-occurs-when-a-service-fabric-cluster-is-created"></a><span data-ttu-id="8149e-157">Service Fabric クラスターの作成時にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="8149e-157">Time-out error occurs when a Service Fabric cluster is created</span></span>
<span data-ttu-id="8149e-158">該当するセットアップ トピックの「スタンドアロン Service Fabric クラスターのセットアップ」セクションおよび環境の配置トピックにあるように Test-D365FOConfiguration.ps1 を実行し、エラーに注目します。</span><span class="sxs-lookup"><span data-stu-id="8149e-158">Run Test-D365FOConfiguration.ps1 as noted in the "Set up a standalone Service Fabric cluster" section of the appropriate setup and deployment topic for your environment, and note any errors:</span></span>

- [<span data-ttu-id="8149e-159">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-159">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [<span data-ttu-id="8149e-160">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-160">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

<span data-ttu-id="8149e-161">これらの手順を必ず実行してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-161">Be sure to complete these steps:</span></span>

- <span data-ttu-id="8149e-162">すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-162">Verify that the Service Fabric Server client certificate exists in the LocalMachine store on all Service Fabric nodes.</span></span>
- <span data-ttu-id="8149e-163">Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-163">Verify that the Service Fabric Server certificate has the access control list (ACL) for Network Service on all Service Fabric nodes.</span></span>
- <span data-ttu-id="8149e-164">[環境設定](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) で記載されているウイルス対策の除外を確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-164">Review the antivirus exclusions that are noted in [Environment setup](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="time-out-error-occurs-while-youre-waiting-for-installer-service-to-be-completed-for-machine-xxxx"></a><span data-ttu-id="8149e-165">インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="8149e-165">Time-out error occurs while you're waiting for Installer Service to be completed for machine x.x.x.x</span></span>
<span data-ttu-id="8149e-166">インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="8149e-166">Only one node type is supported for each Internet Protocol (IP) address (that is, for each machine).</span></span> <span data-ttu-id="8149e-167">ノードが同じマシン上で再利用されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-167">Check whether the nodes are being reused on the same machine.</span></span> <span data-ttu-id="8149e-168">たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-168">For example, AOS and ORCH must not be on the same machine, and ConfigTemplate.xml must be correctly defined.</span></span>

## <a name="remove-a-specific-application"></a><span data-ttu-id="8149e-169">特定のアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="8149e-169">Remove a specific application</span></span>
<span data-ttu-id="8149e-170">配置の削除またはクリーンアップに LCS を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8149e-170">We recommend that you use LCS to remove or clean up deployments.</span></span> <span data-ttu-id="8149e-171">ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8149e-171">However, you can also use Service Fabric Explorer to remove an application as you require.</span></span>

<span data-ttu-id="8149e-172">Service Fabric エクスプローラーで、**アプリケーション ノード** \> **アプリケーション** \> **MonitoringAgentAppType-Agent** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-172">In Service Fabric Explorer, go to **Application node** \> **Applications** \> **MonitoringAgentAppType-Agent**.</span></span> <span data-ttu-id="8149e-173">**ファブリック:/エージェント監視**の横にある省略記号 **...** をクリックし、アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-173">Select the ellipsis button [**...**] next to **fabric:/Agent-Monitoring**, and delete the application.</span></span> <span data-ttu-id="8149e-174">確認のためにアプリケーションの正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="8149e-174">Enter the full name of the application to confirm.</span></span>

<span data-ttu-id="8149e-175">また、省略記号ボタンの選択および**非引当タイプ**の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-175">You can also remove MonitoringAgentAppType-Agent by selecting the ellipsis button and then selecting **Unprovision Type**.</span></span> <span data-ttu-id="8149e-176">アプリケーションの削除を確認するために、正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="8149e-176">Enter the full name to confirm the removal of the application.</span></span>

## <a name="remove-all-applications-from-service-fabric"></a><span data-ttu-id="8149e-177">Service Fabric からすべてのアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="8149e-177">Remove all applications from Service Fabric</span></span>
<span data-ttu-id="8149e-178">次のスクリプトは、LocalAgent および LocalAgent の Monitoring エージェントを除く、すべての Service Fabric アプリケーションを削除およびプロビジョニング解除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-178">The following script removes and unprovisions all Service Fabric applications except the LocalAgent and Monitoring agent for the LocalAgent.</span></span> <span data-ttu-id="8149e-179">オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-179">You must run this script on an orchestrator virtual machine (VM).</span></span>

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

## <a name="remove-service-fabric"></a><span data-ttu-id="8149e-180">Service Fabric の削除</span><span class="sxs-lookup"><span data-stu-id="8149e-180">Remove Service Fabric</span></span>
<span data-ttu-id="8149e-181">Service Fabric クラスターを完全に削除するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-181">To completely remove the Service Fabric cluster, follow these steps.</span></span>

1. <span data-ttu-id="8149e-182">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-182">Run the following command.</span></span>

    ```powershell
    .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

2. <span data-ttu-id="8149e-183">エラーが発生した場合は、**CleanFabric.ps1**コマンドを使用して、クラスタ内の特定のノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-183">If an error occurs, remove a specific node on the cluster by using the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="8149e-184">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-184">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span>
3. <span data-ttu-id="8149e-185">既定の場所を使用している場合、**C:\\ProgramData\\SF** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-185">Remove the **C:\\ProgramData\\SF** folder, if you're using the default location.</span></span> <span data-ttu-id="8149e-186">それ以外の場合、指定したフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-186">Otherwise, remove the specified folder.</span></span>

    <span data-ttu-id="8149e-187">「アクセスが拒否されました」というエラーが表示された場合は、Microsoft Windows PowerShell またはマシンを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-187">If you receive an "access denied" error, restart Microsoft Windows PowerShell or the machine.</span></span>

## <a name="clean-up-an-existing-environment-and-redeploy"></a><span data-ttu-id="8149e-188">既存環境のクリーンアップと再配置</span><span class="sxs-lookup"><span data-stu-id="8149e-188">Clean up an existing environment and redeploy</span></span>

<span data-ttu-id="8149e-189">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-189">Follow these steps:</span></span>

1. <span data-ttu-id="8149e-190">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-190">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span>
    
    <span data-ttu-id="8149e-191">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="8149e-191">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="8149e-192">このプロセスは 1、2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="8149e-192">This process will take one to two minutes.</span></span>

2. <span data-ttu-id="8149e-193">LocalAgentCLI.exe を含むオーケストレーター マシンにアクセスし、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-193">Access the orchestrator machine that contains LocalAgentCLI.exe, and follow these steps:</span></span>

    1. <span data-ttu-id="8149e-194">ローカル エージェント クリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-194">Run local agent cleanup.</span></span>

        ```powershell
        .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
        ```

    2. <span data-ttu-id="8149e-195">Service Fabric を削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-195">Remove Service Fabric.</span></span>

        ```powershell
        .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
        ```

    3. <span data-ttu-id="8149e-196">ノードが失敗した場合、**CleanFabric.ps1** コマンドを実行してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-196">If any nodes fail, run the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="8149e-197">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-197">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span> 
    4. <span data-ttu-id="8149e-198">すべての Service Fabric ノードの **C:\\ProgramData\\SF\\** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-198">Remove the **C:\\ProgramData\\SF\\** folder on all Service Fabric nodes.</span></span>

        <span data-ttu-id="8149e-199">アクセスが拒否された場合は、マシンを再起動してからやり直します。</span><span class="sxs-lookup"><span data-stu-id="8149e-199">If access is denied, restart the machine, and try again.</span></span>

3. <span data-ttu-id="8149e-200">必要に応じて証明書を削除または更新します。</span><span class="sxs-lookup"><span data-stu-id="8149e-200">Remove or update certificates as required.</span></span>

    <span data-ttu-id="8149e-201">すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-201">Remove old certificates from all AOS, BI, ORCH, and DC nodes.</span></span>

    - <span data-ttu-id="8149e-202">証明書は、次の証明書ストアに存在します: Cert:\\CurrentUser\\My\\、Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root。</span><span class="sxs-lookup"><span data-stu-id="8149e-202">The certificates exist in the following certificate stores: Cert:\\CurrentUser\\My\\, Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root.</span></span>
    - <span data-ttu-id="8149e-203">Microsoft SQL Server 設定が変更される場合は、SQL サーバー証明書も削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-203">If the Microsoft SQL Server setup will be modified, remove the SQL Server certificates.</span></span>
    - <span data-ttu-id="8149e-204">Active Directory フェデレーション サービス (AD FS) の設定が変更される場合は、AD FS 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-204">If the Active Directory Federation Services (AD FS) settings will be modified, remove the AD FS certificate.</span></span>

4. <span data-ttu-id="8149e-205">必要に応じて、次の構成ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="8149e-205">Update the following configuration files as required:</span></span>

    - <span data-ttu-id="8149e-206">ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="8149e-206">ConfigTemplate.xml</span></span>
    - <span data-ttu-id="8149e-207">ClusterConfig.json</span><span class="sxs-lookup"><span data-stu-id="8149e-207">ClusterConfig.json</span></span>

    <span data-ttu-id="8149e-208">テンプレートのフィールドに正しく入力する方法については、ご使用の環境に適した設定と配置のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-208">For information about how to correctly fill in the fields in the templates, see the appropriate setup and deployment topic for your environment:</span></span>
    
    - [<span data-ttu-id="8149e-209">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-209">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md)
    - [<span data-ttu-id="8149e-210">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-210">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md)

5. <span data-ttu-id="8149e-211">LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。</span><span class="sxs-lookup"><span data-stu-id="8149e-211">In LCS, open the project, and update the LCS on-premises connector as required.</span></span>

    1. <span data-ttu-id="8149e-212">環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="8149e-212">Re-create the LCS on-premises connector for the environment, or edit the settings of an existing connector.</span></span>

        <span data-ttu-id="8149e-213">LCS の値を簡単にコピーするには、.\\Get-AgentConfiguration.ps1 script を使用します。</span><span class="sxs-lookup"><span data-stu-id="8149e-213">To obtain easy-to-copy values for LCS, use the .\\Get-AgentConfiguration.ps1 script.</span></span>

    2. <span data-ttu-id="8149e-214">最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8149e-214">Download the latest local agent configuration, localagent-config.json.</span></span>

<span data-ttu-id="8149e-215">[プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md) または[プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md) の配置ドキュメントに従って再度配置します。</span><span class="sxs-lookup"><span data-stu-id="8149e-215">Deploy again by following the deployment documentation for [Platform update 12](setup-deploy-on-premises-pu12.md) or for [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md).</span></span>

## <a name="find-the-local-agent-values-that-are-used"></a><span data-ttu-id="8149e-216">使用するローカル エージェント値の検索</span><span class="sxs-lookup"><span data-stu-id="8149e-216">Find the local agent values that are used</span></span>
<span data-ttu-id="8149e-217">ローカル エージェントの値は、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent** > で**詳細**を選択し、Service Fabric Explorer で確認できます。</span><span class="sxs-lookup"><span data-stu-id="8149e-217">You can find local agent values in Service Fabric Explorer, under **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent** > and then select **Details**.</span></span>

<span data-ttu-id="8149e-218">または、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-218">Alternatively, run the following Windows PowerShell command.</span></span>

```powershell
.\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml 
```

## <a name="install-upgrade-or-uninstall-a-local-agent"></a><span data-ttu-id="8149e-219">ローカル エージェントのインストール、アップグレード、アンインストール</span><span class="sxs-lookup"><span data-stu-id="8149e-219">Install, upgrade, or uninstall a local agent</span></span>
<span data-ttu-id="8149e-220">ローカル エージェントのインストールについての詳細は、ご使用の環境に適した設定と配置のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-220">For information about local agent installation, see the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="8149e-221">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-221">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md) 
- [<span data-ttu-id="8149e-222">プラットフォーム更新 8 またはプラットフォーム更新 11</span><span class="sxs-lookup"><span data-stu-id="8149e-222">Platform update 8 or Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md)

<span data-ttu-id="8149e-223">また、以下のアップグレードおよびアンインストール コマンドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-223">You can also use the following upgrade and uninstall commands:</span></span>

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Upgrade <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> <span data-ttu-id="8149e-224">**クリーンアップ**コマンドは、ファイル共有に配置された任意のファイルを削除しません。</span><span class="sxs-lookup"><span data-stu-id="8149e-224">The **cleanup** command doesn't remove any files that were put in the file share.</span></span> <span data-ttu-id="8149e-225">ファイル共有は再利用できます。</span><span class="sxs-lookup"><span data-stu-id="8149e-225">The file share can be reused.</span></span>

## <a name="an-error-occurs-when-local-agent-services-are-started"></a><span data-ttu-id="8149e-226">ローカル エージェント サービスを開始される際にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="8149e-226">An error occurs when local agent services are started</span></span>
<span data-ttu-id="8149e-227">ローカル エージェント サービスが開始されると、次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-227">When local agent services are started, you might receive the following error:</span></span>

> <span data-ttu-id="8149e-228">ファイル、アセンブリ 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'、もしくはその依存関係の 1 つをロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="8149e-228">Could not load file or assembly 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span>

<span data-ttu-id="8149e-229">このエラーは**厳密な名前**検証がオンになっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="8149e-229">This error means that the **Strong name** verification is turned on.</span></span> <span data-ttu-id="8149e-230">Configure-PreReqs.ps1 を使用して、この確認をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-230">You can turn off this verification by using Configure-PreReqs.ps1.</span></span> <span data-ttu-id="8149e-231">検証が有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-231">To validate that the verification is no longer turned on, run Test-D365FOConfiguration.ps1.</span></span>

## <a name="a-validation-in-progress-message-is-shown-for-several-minutes-in-lcs"></a><span data-ttu-id="8149e-232">「検証が進行中」のメッセージが LCS に数分表示</span><span class="sxs-lookup"><span data-stu-id="8149e-232">A "Validation in progress" message is shown for several minutes in LCS</span></span>
<span data-ttu-id="8149e-233">ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-233">Follow these steps to troubleshoot general issues with local agent validation.</span></span>

1. <span data-ttu-id="8149e-234">コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で **Configure-PreReqs.ps1** を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-234">Run **Configure-PreReqs.ps1** on all orchestrator machines to configure the machines correctly.</span></span>
2. <span data-ttu-id="8149e-235">Test-D365FOConfiguration.ps1 スクリプトがすべてのオーケストレータ マシンで通ることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-235">Verify that the Test-D365FOConfiguration.ps1 script passes on all the orchestrator machines.</span></span>
3. <span data-ttu-id="8149e-236">LocalAgentCLI.exe のインストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-236">Verify that the installation of LocalAgentCLI.exe is successfully completed.</span></span>
4. <span data-ttu-id="8149e-237">Service Fabric Explorer で、すべてのアプリケーションが正常であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-237">In Service Fabric Explorer, verify that all the applications are healthy.</span></span>
5. <span data-ttu-id="8149e-238">アプリケーションが正常でない場合は、障害が発生しているサービスのプライマリ ノードを探します。</span><span class="sxs-lookup"><span data-stu-id="8149e-238">If the applications aren't healthy, find the primary node for the service that is failing.</span></span> <span data-ttu-id="8149e-239">イベント ビューアーでは、次の場所でのイベントを検索します。</span><span class="sxs-lookup"><span data-stu-id="8149e-239">In Event Viewer, look for events in the following locations:</span></span>

    - <span data-ttu-id="8149e-240">**カスタム ビュー** \> **管理イベント**</span><span class="sxs-lookup"><span data-stu-id="8149e-240">**Custom Views** \> **Administrative Events**</span></span>
    - <span data-ttu-id="8149e-241">**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent**</span><span class="sxs-lookup"><span data-stu-id="8149e-241">**Applications and Services Log** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent**</span></span>

## <a name="local-agent-errors"></a><span data-ttu-id="8149e-242">ローカル エージェント エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-242">Local agent errors</span></span>

### <a name="issue"></a><span data-ttu-id="8149e-243">問題</span><span class="sxs-lookup"><span data-stu-id="8149e-243">Issue</span></span>
<span data-ttu-id="8149e-244">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-244">**Error:**</span></span>

<span data-ttu-id="8149e-245">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-245">You might receive the following errors:</span></span>

> <span data-ttu-id="8149e-246">コマンドを処理できません</span><span class="sxs-lookup"><span data-stu-id="8149e-246">Unable to process commands</span></span>

> <span data-ttu-id="8149e-247">チャンネル情報を取得できません</span><span class="sxs-lookup"><span data-stu-id="8149e-247">Unable to get the channel information</span></span>

> <span data-ttu-id="8149e-248">ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8149e-248">RunAsync failed due to an unhandled exception causing the host process to crash: System.ArgumentNullException: Value cannot be null.</span></span> <span data-ttu-id="8149e-249">パラメーター名: 証明書</span><span class="sxs-lookup"><span data-stu-id="8149e-249">Parameter name: certificate</span></span>

<span data-ttu-id="8149e-250">**理由:** これらのエラーは、OnPremLocalAgent 証明書に指定された証明書が有効でないか、またはテナントに対して正しく構成されていないために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="8149e-250">**Reason:** These errors can occur because the certificate that is specified for the OnPremLocalAgent certificate either isn't valid or isn't configured correctly for the tenant.</span></span>

<span data-ttu-id="8149e-251">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-251">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="8149e-252">すべてのオーケストレータ ノードで **Test-D365FOConfiguration.ps1** を実行し、すべてのチェックに合格することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-252">Run **Test-D365FOConfiguration.ps1** on all orchestrator nodes to make sure that all checks pass.</span></span>
2. <span data-ttu-id="8149e-253">ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-253">Verify that the certificate that is specified in the local agent configuration is correct.</span></span>

    - <span data-ttu-id="8149e-254">LCS および ConfigTemplate.xml ファイルで指定する拇印に特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-254">Make sure that the thumbprint that you specify in LCS and in the ConfigTemplate.xml file has no special characters.</span></span>
    - <span data-ttu-id="8149e-255">証明書は、infrastructure\\ConfigTemplate.xml の次のセクションで指定されているものと同じ証明書である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-255">The certificate should be the same certificate that is specified in the following section in infrastructure\\ConfigTemplate.xml.</span></span>

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. <span data-ttu-id="8149e-256">LCS のローカル エージェント コンフィギュレーションで指定される同じ証明書が、環境に対する適切な設定および配置トピックの「テナント用 LCS 接続の構成」セクションで手順の完了に使用されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-256">Make sure that the same certificate that is specified in the local agent configuration in LCS was used to complete the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="8149e-257">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-257">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="8149e-258">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-258">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. <span data-ttu-id="8149e-259">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-259">Uninstall the local agent.</span></span>
5. <span data-ttu-id="8149e-260">ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8149e-260">Specify the correct certificate in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="8149e-261">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-261">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="8149e-262">エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-262">Error</span></span>
<span data-ttu-id="8149e-263">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-263">**Error:**</span></span>

> <span data-ttu-id="8149e-264">パス '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' へアクセスすることは、拒否されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-264">Access to the path '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' is denied.</span></span>

<span data-ttu-id="8149e-265">**理由:** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。</span><span class="sxs-lookup"><span data-stu-id="8149e-265">**Reason:** The file share that is specified in the local agent configuration isn't valid.</span></span>

<span data-ttu-id="8149e-266">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-266">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="8149e-267">指定した共有が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-267">Verify that the specified share exists.</span></span>
2. <span data-ttu-id="8149e-268">ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-268">Verify that the local agent user has full permission on the share.</span></span> <span data-ttu-id="8149e-269">ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定されるドメイン ネーム システム (DNS) 名です。</span><span class="sxs-lookup"><span data-stu-id="8149e-269">The local agent user is the Domain Name System (DNS) name that is specified in the following section in ConfigTemplate.xml.</span></span>

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. <span data-ttu-id="8149e-270">適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-270">Make sure that the "Set up file storage" section of the appropriate setup and deployment topic for your environment is completed:</span></span>

    - [<span data-ttu-id="8149e-271">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-271">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
    - [<span data-ttu-id="8149e-272">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-272">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)

4. <span data-ttu-id="8149e-273">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-273">Uninstall the local agent.</span></span>
5. <span data-ttu-id="8149e-274">ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8149e-274">Specify the correct file share in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="8149e-275">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-275">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="8149e-276">エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-276">Error</span></span>
<span data-ttu-id="8149e-277">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-277">**Error:**</span></span>

> <span data-ttu-id="8149e-278">ユーザー 'D365\\svc-LocalAgent$' へのログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-278">Login failed for user 'D365\\svc-LocalAgent$'.</span></span> <span data-ttu-id="8149e-279">理由: 指定した名前に一致するログインが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="8149e-279">Reason: Could not find a login matching the name provided.</span></span> <span data-ttu-id="8149e-280">\[CLIENT: 10.0.2.23\]</span><span class="sxs-lookup"><span data-stu-id="8149e-280">\[CLIENT: 10.0.2.23\]</span></span>

<span data-ttu-id="8149e-281">**理由:** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="8149e-281">**Reason:** The local agent user can't connect to the orchestrator database.</span></span> <span data-ttu-id="8149e-282">ユーザーが削除され、Active Directory ドメイン サービス (AD DS) に再作成されているために、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-282">This issue can occur because users have been deleted and then re-created in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="8149e-283">したがって、ユーザーのセキュリティ識別子 (SID) が変更され、SQL Server またはデータベースのユーザーに与えられたアクセスは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="8149e-283">Therefore, the security identifier (SID) of the user has changed, and any access that was given to the user for the SQL Server or database no longer works.</span></span>

<span data-ttu-id="8149e-284">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-284">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="8149e-285">SQL Server インスタンスで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-285">Run the following script on the SQL Server instance.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    <span data-ttu-id="8149e-286">このスクリプトは、空のデータベースがまだ存在していない場合に、空のオーケストレータ データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-286">This script creates an empty orchestrator database, if an empty database doesn't already exist.</span></span> <span data-ttu-id="8149e-287">ローカル エージェント ユーザーをデータベースに追加し、データベース\_アクセス許可の所有者に渡します。</span><span class="sxs-lookup"><span data-stu-id="8149e-287">It then adds the local agent user to the database and gives it db\_owner permission.</span></span>

    <span data-ttu-id="8149e-288">適切なアクセス許可が付与された後、アプリケーションは自動的に正常な状態になります。</span><span class="sxs-lookup"><span data-stu-id="8149e-288">After the correct permissions are provided, the application should automatically go to a healthy state.</span></span>

2. <span data-ttu-id="8149e-289">SQL Server インスタンスの完全修飾ドメイン名 (FQDN)、データベース名、ローカル エージェント ユーザーなどの設定が LCS で間違って提供された場合は、設定を変更し、ローカル エージェントを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-289">If any settings, such as the fully qualified domain name (FQDN) of the SQL Server instance, the database name, or the local agent user, were provided incorrectly in LCS, change the settings, and then reinstall the local agent.</span></span>

<span data-ttu-id="8149e-290">上記の手順で問題が解決しない場合は、SQL Server インスタンスとデータベースからローカル エージェント ユーザーを手動で削除し、Initialize-Database スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-290">If the preceding steps don't resolve the issue, manually remove the local agent user from the SQL Server instance and the database, and then rerun the Initialize-Database script.</span></span>

<span data-ttu-id="8149e-291">AD DS でユーザーを再作成する場合、SID が変更されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-291">If you re-create a user in AD DS, remember that the SID will change.</span></span> <span data-ttu-id="8149e-292">この場合、ユーザーの以前の SID を削除し、新しい SID を追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-292">In this case, remove the previous SID for the user, and add a new SID.</span></span>

### <a name="issue"></a><span data-ttu-id="8149e-293">問題</span><span class="sxs-lookup"><span data-stu-id="8149e-293">Issue</span></span>
<span data-ttu-id="8149e-294">ローカル エージェント ユーザーは、SQL Server インスタンスまたはデータベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="8149e-294">The local agent user can't connect to the SQL Server instance or the database.</span></span>

<span data-ttu-id="8149e-295">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-295">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="8149e-296">SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-296">Delete the svc-LocalAgent user from the SQL Server primary node databases, and then remove the login from both servers.</span></span>
2. <span data-ttu-id="8149e-297">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-297">Run the following scripts.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

   <span data-ttu-id="8149e-298">これらのスクリプトは、**常時オン**に設定されているときは機能しません。</span><span class="sxs-lookup"><span data-stu-id="8149e-298">These scripts don't work when an **always-on** setup is used.</span></span> <span data-ttu-id="8149e-299">データベースは、最初にプライマリ ノードで作成されてから複製される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-299">The database must be created in the primary node first and then replicated.</span></span>

### <a name="error"></a><span data-ttu-id="8149e-300">エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-300">Error</span></span>
<span data-ttu-id="8149e-301">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-301">**Error:**</span></span>

> <span data-ttu-id="8149e-302">RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-302">RunAsync failed due to an unhandled exception causing the host process to crash: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span></span><span data-ttu-id="8149e-303"> ---\> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'</span><span class="sxs-lookup"><span data-stu-id="8149e-303"> ---\> System.Net.WebException: The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'</span></span>


<span data-ttu-id="8149e-304">**理由:** ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。</span><span class="sxs-lookup"><span data-stu-id="8149e-304">**Reason:** The local agent machines can't connect to lcsapi.lcs.dynamics.com.</span></span> <span data-ttu-id="8149e-305">「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-305">Review the AX-BridgeService event log for "The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'."</span></span>

<span data-ttu-id="8149e-306">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-306">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="8149e-307">**psping lcsapi.lcs.dynamics.com:80** を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-307">Run **psping lcsapi.lcs.dynamics.com:80**.</span></span>
2. <span data-ttu-id="8149e-308">上記のコマンドからの応答を受信しない場合は、組織の IT 部門に問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="8149e-308">If you don't receive a response from the above command, contact the IT department at your organization.</span></span> <span data-ttu-id="8149e-309">ファイアウォールが lcsapi へのアクセスをブロックしており、プロキシの問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="8149e-309">The firewall is blocking access to lcsapi, or proxy issues are occurring.</span></span>

    ```
    lcsapi.lcs.dynamics.com:443
    login.windows.net:443
    uswelcs1lcm.queue.core.windows.net:443
    www.office.com:443
    login.microsoftonline.com:443
    dc.services.visualstudio.com:443
    uswelcs1lcm.blob.core.windows.net:443
    uswedpl1catalog.blob.core.windows.net:443
    ```

## <a name="restart-applications-such-as-aos"></a><span data-ttu-id="8149e-310">アプリケーション (AOS など) を再起動</span><span class="sxs-lookup"><span data-stu-id="8149e-310">Restart applications (such as AOS)</span></span>
<span data-ttu-id="8149e-311">Service Fabric で、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード**の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="8149e-311">In Service Fabric, expand **Nodes** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **Code Packages** \> **Code**.</span></span> <span data-ttu-id="8149e-312">省略記号ボタン (**...**) を選択し、**再起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149e-312">Select the ellipsis button (**...**), and then select **Restart**.</span></span> <span data-ttu-id="8149e-313">求められたらコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="8149e-313">Enter the code when you're prompted.</span></span>

## <a name="upgrade-service-fabric"></a><span data-ttu-id="8149e-314">Service Fabric を更新します。</span><span class="sxs-lookup"><span data-stu-id="8149e-314">Upgrade Service Fabric</span></span>
<span data-ttu-id="8149e-315">Service Fabric Explorer に次に類似したメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-315">Service Fabric Explorer will display a message simillar to the following:</span></span>

> <span data-ttu-id="8149e-316">問題のあるイベント: SourceId=「System.UpgradeOrchestrationService」、プロパティ =「ClusterVersionSupport」、HealthState=「警告」、ConsiderWarningAsError=false。</span><span class="sxs-lookup"><span data-stu-id="8149e-316">Unhealthy event: SourceId='System.UpgradeOrchestrationService', Property='ClusterVersionSupport', HealthState='Warning', ConsiderWarningAsError=false.</span></span>
<span data-ttu-id="8149e-317">現在のクラスタ バージョン 6.1.467.9494 のサポートは、5/30/2018 12:00:00 AM に終了します。</span><span class="sxs-lookup"><span data-stu-id="8149e-317">The current cluster version 6.1.467.9494 support ends 5/30/2018 12:00:00 AM.</span></span> <span data-ttu-id="8149e-318">Get-ServiceFabricRegisteredClusterCodeVersion を使用して利用可能なアップグレードを表示し、Start-ServiceFabricClusterUpgrade を使用してアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-318">Please view available upgrades using Get-ServiceFabricRegisteredClusterCodeVersion and upgrade using Start-ServiceFabricClusterUpgrade.</span></span>

<span data-ttu-id="8149e-319">最小要件が 1 つの SQL Server Reporting Services (SSRS) ノードと 1 つの Management Reporter (MR) ノードであるため、PreUpgradeSafetyCheck をスキップするパラメータを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-319">Because the minimum requirement is one SQL Server Reporting Services (SSRS) node and one Management Reporter (MR) node, you must pass in a parameter to skip PreUpgradeSafetyCheck.</span></span>

<span data-ttu-id="8149e-320">Windows PowerShell で Service Fabric をアップグレードするために使用される手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-320">Here are the steps that are used to upgrade Service Fabric in Windows PowerShell.</span></span>

```powershell
#Connect to Service Fabric Cluster. Replace 123 with server/star thumbprint and use appropriate IP address
Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123

#Get latest version that was downloaded
Get-ServiceFabricRegisteredClusterCodeVersion

#Enter latest version from above for CodePackageVersion.
#Note UpgradeReplicaSetCheckTimeout is to skip over PreUpgradeSafetyCheck for SSRS and MR, see <https://github.com/Azure/service-fabric-issues/issues/595>
#May also want to use -UpgradeDomainTimeoutSec 600 -UpgradeTimeoutSec 1800, <https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-upgrade-parameters>
Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion 6.1.472.9494 -Monitored -FailureAction Rollback -UpgradeReplicaSetCheckTimeout 30

#Get upgrade status
Get-ServiceFabricClusterUpgrade
```

<span data-ttu-id="8149e-321">詳細については、[アプリケーション アップグレードのトラブルシューティング](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-321">For more information, see [Troubleshoot application upgrades](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-upgrade-troubleshooting).</span></span>

<span data-ttu-id="8149e-322">新しい Service Fabric リリースの時期については、[Azure Service Fabric チーム ブログ](https://blogs.msdn.microsoft.com/azureservicefabric/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-322">To learn when a new Service Fabric release comes out, see the [Azure Service Fabric team blog](https://blogs.msdn.microsoft.com/azureservicefabric/).</span></span>

<span data-ttu-id="8149e-323">アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録し、ノード、アプリケーション、およびコードの再起動を展開して再起動してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-323">If you receive a warning in Service Fabric Explorer after you upgrade, make a note of the node, and then restart via expanding nodes, application, and code restart.</span></span> <span data-ttu-id="8149e-324">手順については、[アプリケーションを再起動する方法 (たとえば、AOS)](troubleshoot-on-prem.md#how-to-restart-applications-example-aos) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-324">For instructions, see [How to restart applications (example AOS)](troubleshoot-on-prem.md#how-to-restart-applications-example-aos).</span></span>
 
## <a name="error-unable-to-load-dll-fabricclientdll"></a><span data-ttu-id="8149e-325">エラー、「DLL 'FabricClient.dll' を読み込むことができません」</span><span class="sxs-lookup"><span data-stu-id="8149e-325">Error: "Unable to load DLL 'FabricClient.dll'"</span></span>
<span data-ttu-id="8149e-326">このエラーが発生した場合は、閉じて、Windows PowerShell を再起動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-326">If you receive this error, close and restart Windows PowerShell.</span></span> <span data-ttu-id="8149e-327">エラーが引き続き発生する場合は、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-327">If the error persists, restart the machine.</span></span>

## <a name="what-cluster-id-should-be-used-in-the-agent-configuration"></a><span data-ttu-id="8149e-328">エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="8149e-328">What cluster ID should be used in the agent configuration?</span></span>
<span data-ttu-id="8149e-329">クラスタ ID は、任意のグローバル一意識別子 (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="8149e-329">The cluster ID can be any globally unique identifier (GUID).</span></span> <span data-ttu-id="8149e-330">この GUID は、追跡目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-330">This GUID is used for tracking purposes.</span></span>

## <a name="the-local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a><span data-ttu-id="8149e-331">ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します</span><span class="sxs-lookup"><span data-stu-id="8149e-331">The local agent stops working after the tenant for the project from LCS is changed</span></span>
<span data-ttu-id="8149e-332">更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-332">Follow these steps to configure the local agent with the updated tenant.</span></span>

1. <span data-ttu-id="8149e-333">既にコネクタがインストールされている LCS からすべての環境を削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-333">Remove all the environments from LCS that already have the connector installed.</span></span>
2. <span data-ttu-id="8149e-334">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-334">Uninstall the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

3. <span data-ttu-id="8149e-335">ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-335">Follow the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="8149e-336">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-336">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="8149e-337">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-337">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. <span data-ttu-id="8149e-338">新しいテナントに新しい LCS コネクタを作成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-338">Create a new LCS connector in the new tenant.</span></span>
5. <span data-ttu-id="8149e-339">**local-agent.config** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="8149e-339">Download the **local-agent.config** file.</span></span>
6. <span data-ttu-id="8149e-340">ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8149e-340">Install the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="encryption-errors"></a><span data-ttu-id="8149e-341">暗号化エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-341">Encryption errors</span></span>
<span data-ttu-id="8149e-342">暗号化エラーの例には AXBootstrapperAppType、Bootstrapper、AXDiagnostics、RTGatewayAppType、ゲートウェイの潜在的なエラー関連、Microsoft.D365.Gateways.ClusterGateway.exe などがあります。</span><span class="sxs-lookup"><span data-stu-id="8149e-342">Some encryption error examples include AXBootstrapperAppType, Bootstrapper, AXDiagnostics, RTGatewayAppType, Gateway potential failure related, and Microsoft.D365.Gateways.ClusterGateway.exe.</span></span>

<span data-ttu-id="8149e-343">AOS AccountPassword を暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="8149e-343">You might receive one of these errors if the data encipherment certificate that was used to encrypt the AOS AccountPassword wasn't installed on the machine.</span></span> <span data-ttu-id="8149e-344">この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-344">This certificate might be in the certificates (local computer), or the provider type might be incorrect.</span></span>

<span data-ttu-id="8149e-345">エラーを解決するには、credentials.json ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="8149e-345">To resolve the error, validate the credentials.json file.</span></span> <span data-ttu-id="8149e-346">次のコマンドを (AOS1 上に) 入力することによって、テキストが正しく復号化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-346">Verify that the text is decrypted correctly by entering the following command (on AOS1).</span></span>

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="8149e-347">このエラーも、**''** パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-347">This error can also occur if the **''** parameter isn't defined in the ApplicationManifest file.</span></span> <span data-ttu-id="8149e-348">イベント ビューアーで、このパラメータが定義されているどうかを確認するには、**カスタム ビュー** \> **管理イベント**の順に移動し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-348">To determine whether this parameter is defined, in Event Viewer, go to **Custom Views** \> **Administrative Events**, and verify the following information:</span></span>

- <span data-ttu-id="8149e-349">Credentials.json ファイルの資格情報の暗号化には、正しいレイアウト/構造があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-349">The encrypt credentials for the credentials.json file have the correct layout/structure.</span></span> <span data-ttu-id="8149e-350">詳細については、ご使用の環境に適した設定および配置のトピックの「資格情報の暗号化」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-350">For more information, see the "Encrypt credentials" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="8149e-351">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-351">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#encryptcred)
    - [<span data-ttu-id="8149e-352">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-352">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#encryptcred)

- <span data-ttu-id="8149e-353">決算引用符が線の終わりまたは次の線に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-353">A closing quotation mark appears at the end of the line or on the next line.</span></span>
- <span data-ttu-id="8149e-354">イベント ビューアーでは、**カスタム ビュー** > **管理イベント**で、**Microsoft-Service Fabric** ソース カテゴリでのエラーに注意します。</span><span class="sxs-lookup"><span data-stu-id="8149e-354">In Event Viewer, under **Custom Views** > **Administrative Events**, note any errors in the **Microsoft-Service Fabric** source category.</span></span>

## <a name="properties-to-create-a-dataencryption-certificate"></a><span data-ttu-id="8149e-355">DataEncryption 証明書を作成するためのプロパティ</span><span class="sxs-lookup"><span data-stu-id="8149e-355">Properties to create a DataEncryption certificate</span></span>
<span data-ttu-id="8149e-356">DataEncryption 証明書を作成するのにには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8149e-356">Use the following properties to create the DataEncryption certificate:</span></span>

- <span data-ttu-id="8149e-357">**自己署名証明書** – このパラメータは、自己署名証明書を使用する場合にのみ有効にします。</span><span class="sxs-lookup"><span data-stu-id="8149e-357">**Is self-signed certificate** – Enable this parameter only when you're using self-signed certificates.</span></span>
- <span data-ttu-id="8149e-358">**証明書の目的** – この証明書のすべての目的を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8149e-358">**Certificate purposes** – Enable all purposes for this certificate.</span></span>
- <span data-ttu-id="8149e-359">**署名アルゴリズム** – **sha256RSA** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-359">**Signature algorithm** – Specify **sha256RSA**.</span></span>
- <span data-ttu-id="8149e-360">**署名ハッシュ アルゴリズム** – **sha256** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-360">**Signature hash algorithm** – Specify **sha256**.</span></span>
- <span data-ttu-id="8149e-361">**発行者** – 指定 **CN = DataEncryptionCertificate**。</span><span class="sxs-lookup"><span data-stu-id="8149e-361">**Issuer** – Specify **CN = DataEncryptionCertificate**.</span></span>
- <span data-ttu-id="8149e-362">**公開キー** – **RSA (2048 ビット)** を指定します。</span><span class="sxs-lookup"><span data-stu-id="8149e-362">**Public Key** – Specify **RSA (2048 bits)**.</span></span>
- <span data-ttu-id="8149e-363">**Thumbprint アルゴリズム** – **sha1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="8149e-363">**Thumbprint algorithm** – Specify **sha1**.</span></span>

> [!WARNING]
> <span data-ttu-id="8149e-364">実稼働環境では、自己署名証明書を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8149e-364">Don't use self-signed certificates in production environments.</span></span> <span data-ttu-id="8149e-365">代わりに、証明書機関によって発行された証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="8149e-365">Instead, use certificates that are issued by certificate authorities.</span></span>

## <a name="the-certificate-and-private-key-to-use-for-decryption-cant-be-found-0x8009200c"></a><span data-ttu-id="8149e-366">暗号の解読に使用する証明書と秘密キーを見つけることができません (0x8009200C)</span><span class="sxs-lookup"><span data-stu-id="8149e-366">The certificate and private key to use for decryption can't be found (0x8009200C)</span></span>
<span data-ttu-id="8149e-367">証明書と ACL がない、または間違った拇印の入力がある場合は、特殊文字をチェックし、C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt で拇印を探します。</span><span class="sxs-lookup"><span data-stu-id="8149e-367">If you're missing a certificate and ACL, or if you have the wrong thumbprint entry, check for special characters, and look for thumbprints in C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt.</span></span>

<span data-ttu-id="8149e-368">次のコマンドを使用して暗号化されたテキストを検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="8149e-368">You can also validate the encrypted text by using the following command.</span></span>

```
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="8149e-369">「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-369">If you receive the message, "Cannot find the certificate and private key to use for decryption," verify the axdataenciphermentcert and svc-AXSF$ AXServiceUser ACLs.</span></span>

<span data-ttu-id="8149e-370">credentials.json ファイルが変更された場合は、LCS から環境を削除して再配置します。</span><span class="sxs-lookup"><span data-stu-id="8149e-370">If the credentials.json file has changed, delete and redeploy the environment from LCS.</span></span>

<span data-ttu-id="8149e-371">上記のソリューションのいずれも機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-371">If none of the preceding solutions work, follow these steps.</span></span>

1. <span data-ttu-id="8149e-372">ConfigTemplate.xml ファイルで指定されたドメイン名と Active Directory アカウント名が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-372">Verify that the domain name and Active Directory account names that are specified in the ConfigTemplate.xml file are correct.</span></span>
2. <span data-ttu-id="8149e-373">用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml ファイルで指定された拇印が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-373">Verify that the thumbprints that are specified in the ConfigTemplate.xml file are correct if the certificate wasn't generated by using the scripts that are provided.</span></span>
3. <span data-ttu-id="8149e-374">LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと拇印が一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-374">Make sure that the certificate thumbprints that are specified in LCS are correct, and that they match the thumbprints that are specified in ConfigTemplate.xml.</span></span> <span data-ttu-id="8149e-375">特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-375">Make sure that there are no special characters.</span></span> <span data-ttu-id="8149e-376">**.\\Get-DeploymentSettings.ps1** を実行して、コピーしやすい方法で拇印を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-376">You can run **.\\Get-DeploymentSettings.ps1** to obtain the thumbprints in an easy-to-copy manner.</span></span>
4. <span data-ttu-id="8149e-377">証明書が自己生成されない場合、プロバイダー名が次の証明書タイプと一致することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-377">If the certificates aren't self-generated, make sure that the provider names match for the following certificate types:</span></span>

    - <span data-ttu-id="8149e-378">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span><span class="sxs-lookup"><span data-stu-id="8149e-378">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span></span>
    - <span data-ttu-id="8149e-379">**その他のすべての証明書タイプ:** Microsoft の拡張された RSA および AES 暗号化プロバイダー</span><span class="sxs-lookup"><span data-stu-id="8149e-379">**All other certificate types:** Microsoft Enhanced RSA and AES Cryptographic Provider</span></span>

5. <span data-ttu-id="8149e-380">Set-CertificateAcls.ps1 および Test-D365FOConfiguration.ps1 スクリプトがすべての Service Fabric マシンで正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-380">Make sure that the Set-CertificateAcls.ps1 and Test-D365FOConfiguration.ps1 scripts were successfully run on all Service Fabric machines.</span></span>
6. <span data-ttu-id="8149e-381">Credentials.json ファイルが存在し、エントリが適切な値に復号化されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-381">Make sure that the credentials.json file exists, and that the entries are decrypted to correct values.</span></span>

    <span data-ttu-id="8149e-382">AOS マシンのいずれかで、データの暗号化証明書が正しいことを確認する次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-382">On one of the AOS machines, run the following command to verify that the data encryption certificate is correct.</span></span>

    ```powershell
    Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
    ```

7. <span data-ttu-id="8149e-383">いずれかの証明書を変更する必要がある場合、もしくは構成が間違っている場合は、次の手順を実行してください:</span><span class="sxs-lookup"><span data-stu-id="8149e-383">If any of the certificates must be changed, or if the configuration was wrong, follow these steps:</span></span>

    1. <span data-ttu-id="8149e-384">**ConfigTemplate.xml** ファイルを編集して、正しい値が出るようにします。</span><span class="sxs-lookup"><span data-stu-id="8149e-384">Edit the **ConfigTemplate.xml** file so that it has the correct values.</span></span>
    2. <span data-ttu-id="8149e-385">すべてのセットアップ スクリプトと **Test-D365FOConfiguration** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-385">Run all the setup scripts and the **Test-D365FOConfiguration** script.</span></span>

8. <span data-ttu-id="8149e-386">LCS に戻り、環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-386">Go back to LCS, and reconfigure the environment.</span></span>

## <a name="mr"></a><span data-ttu-id="8149e-387">MR</span><span class="sxs-lookup"><span data-stu-id="8149e-387">MR</span></span>
<span data-ttu-id="8149e-388">追加のログは、プロバイダーを登録することで実行できます。</span><span class="sxs-lookup"><span data-stu-id="8149e-388">Additional logging can be done by registering providers.</span></span> <span data-ttu-id="8149e-389">[ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) を **プライマリ**オーケストレータ マシン にダウンロードし、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-389">Download [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) to the **primary** orchestrator machine, and then run the following commands.</span></span> <span data-ttu-id="8149e-390">プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorerで、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="8149e-390">To determine which machine is the primary instance, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

> [!NOTE]
> <span data-ttu-id="8149e-391">イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-391">If results in Event Viewer don't appear correct (for example, if words are truncated), get the latest manifest and .dll file.</span></span> <span data-ttu-id="8149e-392">最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-392">To get the latest manifest and .dll file, go to the WP folder in the agent file share.</span></span> <span data-ttu-id="8149e-393">この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。</span><span class="sxs-lookup"><span data-stu-id="8149e-393">This share was created in the "Set up file storage" section of the appropriate setup and deployment topic for your environment:</span></span>
> 
> - [<span data-ttu-id="8149e-394">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-394">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
> - [<span data-ttu-id="8149e-395">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-395">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)
> 
> <span data-ttu-id="8149e-396">**例:** \[*エージェント共有*\]\\wp\\\[*配置名*\]\\StandaloneSetup-...\\アプリ\\ ETWManifests</span><span class="sxs-lookup"><span data-stu-id="8149e-396">**Example:** \[*Agent Share*\]\\wp\\\[*Deployment name*\]\\StandaloneSetup-...\\Apps\\ETWManifests</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

<span data-ttu-id="8149e-397">プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8149e-397">If you must unregister providers, use the following command.</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

<span data-ttu-id="8149e-398">プロバイダーが登録されると、新しい配置についての追加詳細は**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** でイベント ビューアーにログインされます。</span><span class="sxs-lookup"><span data-stu-id="8149e-398">After providers are registered, additional details about the new deployment are logged in Event Viewer, at **Applications and Services Logs** \> **Microsoft** \> **Dynamics**.</span></span> <span data-ttu-id="8149e-399">次のフォルダが表示されます:</span><span class="sxs-lookup"><span data-stu-id="8149e-399">The following folders will be displayed:</span></span>

- <span data-ttu-id="8149e-400">MR-Logger</span><span class="sxs-lookup"><span data-stu-id="8149e-400">MR-Logger</span></span>
- <span data-ttu-id="8149e-401">MR-Sql</span><span class="sxs-lookup"><span data-stu-id="8149e-401">MR-Sql</span></span>

<span data-ttu-id="8149e-402">新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-402">To see the new folders, you must close and reopen Event Viewer.</span></span> <span data-ttu-id="8149e-403">追加の詳細を表示するには、もう一度環境を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-403">To see additional details, you must deploy an environment again.</span></span>

### <a name="error-occurs-while-addaxdatabasechangetracking-is-running"></a><span data-ttu-id="8149e-404">AddAXDatabaseChangeTracking の実行中に発生するエラー</span><span class="sxs-lookup"><span data-stu-id="8149e-404">Error occurs while AddAXDatabaseChangeTracking is running</span></span>
<span data-ttu-id="8149e-405">Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-405">If you encounter an error while you run AddAXDatabaseChangeTracking at Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet), verify that the full path is correct.</span></span> <span data-ttu-id="8149e-406">完全なパスの例として、ax.d365ffo.onprem.contoso.com があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-406">An example of a full path is ax.d365ffo.onprem.contoso.com.</span></span>

<span data-ttu-id="8149e-407">アスタリスク (\*) 証明書での問題が原因でエラーが発生する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="8149e-407">The error might also occur because of an issue with the asterisk (\*) certificate.</span></span> <span data-ttu-id="8149e-408">たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-408">For example, the remote certificate CN=\*.d365ffo.onprem.contoso.com has a name that isn't valid or that doesn't match the host, ax.d365ffo.onprem.contoso.com.</span></span>

### <a name="run-the-initialize-database-script-and-validate-that-databases-have-correct-users"></a><span data-ttu-id="8149e-409">データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証</span><span class="sxs-lookup"><span data-stu-id="8149e-409">Run the initialize database script, and validate that databases have correct users</span></span>
<span data-ttu-id="8149e-410">AddAXDatabaseChangeTracking イベントのみを受け取った場合は、`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService` にアクセスし、Finance and Operations の MetadataService サービスにアクセスしてみてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-410">If you receive only the AddAXDatabaseChangeTracking event, try to reach the MetadataService service of Finance and Operations by going to `https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService`.</span></span>

<span data-ttu-id="8149e-411">次に、wif.config ファイルでサービスの証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-411">Next, check the certificates of the service in the wif.config file.</span></span> <span data-ttu-id="8149e-412">ファイルを検索するには、AOS マシンにサインインし、タスク マネージャーで **AxService.exe** を検索して右クリックし、**ファイルの場所を開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149e-412">To find the file, sign in to one of the AOS machines, and then, in Task Manager, find **AxService.exe**, right-click, and select **Open file location**.</span></span> <span data-ttu-id="8149e-413">wif.config ファイルでは、3 つの拇印を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-413">In the wif.config file, you should see three thumbprints.</span></span> <span data-ttu-id="8149e-414">これらの拇印に関する次の要件に注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-414">Note the following requirements for these thumbprints:</span></span>

- <span data-ttu-id="8149e-415">これらは異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-415">They must be different.</span></span>
- <span data-ttu-id="8149e-416">これらは、この順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-416">They must be in this order:</span></span>

    1. <span data-ttu-id="8149e-417">Financialreporting 拇印</span><span class="sxs-lookup"><span data-stu-id="8149e-417">Financialreporting Thumbprint</span></span>
    2. <span data-ttu-id="8149e-418">ReportingService 拇印</span><span class="sxs-lookup"><span data-stu-id="8149e-418">ReportingService Thumbprint</span></span>
    3. <span data-ttu-id="8149e-419">SessionAuthentication 拇印</span><span class="sxs-lookup"><span data-stu-id="8149e-419">SessionAuthentication Thumbprint</span></span>

<span data-ttu-id="8149e-420">拇印がこれらの要件の両方を満たしていない場合は、正しい拇印を使用して LCS から再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-420">If the thumbprints don't meet both of these requirements, you must redeploy from LCS by using correct thumbprints.</span></span>

### <a name="the-remote-name-cant-be-resolved"></a><span data-ttu-id="8149e-421">リモート名を解決できません</span><span class="sxs-lookup"><span data-stu-id="8149e-421">The remote name can't be resolved</span></span>
<span data-ttu-id="8149e-422">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-422">**Error:**</span></span>

> <span data-ttu-id="8149e-423">リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` をリッスンしていたエンドポイントはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="8149e-423">The remote name could not be resolved: 'x.d365fo.onprem.contoso.com' / There was no endpoint listening at `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` that could accept the message.</span></span>

<span data-ttu-id="8149e-424">**理由:** この問題は、通常正しくないアドレスまたは SOAP アクションによって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="8149e-424">**Reason:** This issue is often caused by an incorrect address or SOAP action.</span></span>

<span data-ttu-id="8149e-425">**ステップ:** URL を手動で開き、アドレスにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-425">**Steps:** Verify that the address can be reached by manually opening the URL.</span></span> <span data-ttu-id="8149e-426">詳細については、表示されている場合、イベント ビューアーで InnerException テキストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-426">For more details, see InnerException text in the Event Viewer, if it's present.</span></span>

### <a name="error-on-importdefaultreports"></a><span data-ttu-id="8149e-427">ImportDefaultReports のエラー</span><span class="sxs-lookup"><span data-stu-id="8149e-427">Error on ImportDefaultReports</span></span> 
<span data-ttu-id="8149e-428">配置中に MR レポートがチェックアウトされると、配置は失敗します。</span><span class="sxs-lookup"><span data-stu-id="8149e-428">If MR reports are checked out during deployment, the deployment will fail.</span></span> <span data-ttu-id="8149e-429">レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の**選択**明細書を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-429">To see whether reports are checked out, run the following **select** statements on the FinancialReporting database.</span></span>

```
select checkedoutto, * from Reporting.ControlReport where checkedoutto is not null
select checkedoutto, * from Reporting.ControlRowMaster where checkedoutto is not null
select checkedoutto, * from Reporting.ControlColumnMaster where checkedoutto is not null
```

<span data-ttu-id="8149e-430">どのユーザーがオブジェクトをチェック アウトするかを知るには、次の**選択**ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-430">To learn which user has objects checked out, you can run the following **select** statement.</span></span>

```
select * from Reporting.SecurityUser where UserID = ''
```

<span data-ttu-id="8149e-431">この問題を手動で解決するには、次の表を更新し、次のコマンドを使用して、**checkedoutto** を **null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8149e-431">To resolve this issue manually, update the following tables and set **checkedoutto** to **null** by using the following commands.</span></span>

```
update Reporting.ControlReport set checkedoutto = null where checkedoutto is not null
update Reporting.ControlRowMaster set checkedoutto = null where checkedoutto is not null
update Reporting.ControlColumnMaster set checkedoutto = null where checkedoutto is not null
```

## <a name="axdbadmin-cant-connect-to-the-database-server-sql-lscontosocom"></a><span data-ttu-id="8149e-432">axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。</span><span class="sxs-lookup"><span data-stu-id="8149e-432">axdbadmin can't connect to the database server SQL-LS.contoso.com</span></span>

<span data-ttu-id="8149e-433">**理由:** AXDB データベースに接続するためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-433">**Reason:** The user doesn't have permission to connect to the AXDB database.</span></span>

<span data-ttu-id="8149e-434">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="8149e-434">**Steps:**</span></span>

1. <span data-ttu-id="8149e-435">既に存在する場合は、データベースから axdbadmin ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-435">Remove the axdbadmin user from the database, if it already exists.</span></span>
2. <span data-ttu-id="8149e-436">**ConfigTemplate.xml** ファイルで、AXDB データベースに追加する必要があるユーザー名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-436">In the **ConfigTemplate.xml** file, specify the user name that must be added to the AXDB database.</span></span>

    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```

3. <span data-ttu-id="8149e-437">axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-437">Run the initialize database script again to add the axdbadmin user.</span></span>

## <a name="unable-to-resolve-the-xpath-value"></a><span data-ttu-id="8149e-438">xPath 値を解決することができません。</span><span class="sxs-lookup"><span data-stu-id="8149e-438">Unable to resolve the xPath value</span></span>
<span data-ttu-id="8149e-439">予想される動作では、次の **xPath** 値を解決することはできません。</span><span class="sxs-lookup"><span data-stu-id="8149e-439">In the expected behavior, the following **xPath** value can't be resolved:</span></span> 

<span data-ttu-id="8149e-440">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span><span class="sxs-lookup"><span data-stu-id="8149e-440">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span></span>

<span data-ttu-id="8149e-441">したがって、**xPath** 値を解決できないことは問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-441">Therefore, the inability to resolve the **xPath** value isn't an issue.</span></span> <span data-ttu-id="8149e-442">**xPath** 値は、AOS ランタイム ユーザーの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="8149e-442">The **xPath** value looks for AOS runtime user information.</span></span> <span data-ttu-id="8149e-443">ただし、セキュリティが統合されているため、その情報は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-443">However, because of integrated security, that information isn't required.</span></span> <span data-ttu-id="8149e-444">別の理由でエラーを調査する必要がある場合は、**xPath** 値を解決できないことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-444">The inability to resolve the **xPath** value is communicated in case the failure must be investigated for another reason.</span></span>

## <a name="ad-fs"></a><span data-ttu-id="8149e-445">AD FS</span><span class="sxs-lookup"><span data-stu-id="8149e-445">AD FS</span></span>
### <a name="the-sign-in-page-doesnt-redirect-you"></a><span data-ttu-id="8149e-446">サインイン ページにリダイレクトされません。</span><span class="sxs-lookup"><span data-stu-id="8149e-446">The sign-in page doesn't redirect you</span></span>
<span data-ttu-id="8149e-447">サインイン ページにはリダイレクトされない可能性がありますが、資格情報の確認を続行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-447">The sign-in page might not redirect you but continues to prompt for credentials.</span></span> <span data-ttu-id="8149e-448">また、リダイレクトの可能性がありますが、次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-448">Alternatively, you might be redirected but receive the following message:</span></span>

> <span data-ttu-id="8149e-449">エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-449">An error occurred.</span></span> <span data-ttu-id="8149e-450">詳細については、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-450">Contact your administrator for more information.</span></span>

<span data-ttu-id="8149e-451">そのような場合、問題を解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-451">In these cases, you can follow these steps to resolve the issue:</span></span>

- <span data-ttu-id="8149e-452">AD FS リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-452">Add the AD FS link to the list of trusted sites.</span></span>
- <span data-ttu-id="8149e-453">Dynamics 365 リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-453">Add the Dynamics 365 link to the list of trusted sites.</span></span>
- <span data-ttu-id="8149e-454">末尾にスラッシュ「/」を追加し、動作が変更されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-454">Add a trailing slash (/), and see whether the behavior changes.</span></span>

<span data-ttu-id="8149e-455">**ADFS** \> **アプリケーション グループ**の順に移動して、AD FS マネージャーを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-455">Verify the AD FS Manager by going to **ADFS** \> **Application groups**.</span></span> <span data-ttu-id="8149e-456">**Microsoft Dynamics 365 for Operations on-premises** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8149e-456">Double-click **Microsoft Dynamics 365 for Operations on-premises**.</span></span> <span data-ttu-id="8149e-457">その後、**ネイティブ アプリケーション**で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8149e-457">Then, under **Native application**, double-click **Microsoft Dynamics 365 for Operations on-premises - Native application**.</span></span>

<span data-ttu-id="8149e-458">**リダイレクト URI** 値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-458">Note the **Redirect URI** value.</span></span> <span data-ttu-id="8149e-459">Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-459">It should match the DNS forward lookup zone for Finance and Operations.</span></span>

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a><span data-ttu-id="8149e-460">エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」</span><span class="sxs-lookup"><span data-stu-id="8149e-460">Error: "Could not establish trust relationship for the SSL/TLS secure channel"</span></span>
<span data-ttu-id="8149e-461">このエラーが表示された場合、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-461">If you receive this error, follow these steps.</span></span>

1. <span data-ttu-id="8149e-462">Service Fabric で、**クラスタ** \> **アプリケーション** \> **AXSFType** \> **fabric:/AXSF** の順に移動し、**詳細**タブでスクロールし、**Aad\_AADMetadataLocationFormat** および **Aad\_FederationMetadataLocation** の URL に注意します。</span><span class="sxs-lookup"><span data-stu-id="8149e-462">In Service Fabric, go to **Cluster** \> **Applications** \> **AXSFType** \> **fabric:/AXSF**, and then, on the **Details** tab, scroll down and note the URLs for **Aad\_AADMetadataLocationFormat** and **Aad\_FederationMetadataLocation**.</span></span> <span data-ttu-id="8149e-463">次に、AOS からそれらの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="8149e-463">Next, browse to those URLs from AOS.</span></span>
2. <span data-ttu-id="8149e-464">詳細については、AOS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-464">On the AOS machine, in Event Viewer, go to **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** for details.</span></span>
3. <span data-ttu-id="8149e-465">AD FS 証明書が信頼されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-465">Verify that the AD FS certificate is trusted:</span></span>

    1. <span data-ttu-id="8149e-466">AD FS 証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-466">Verify the AD FS certificate.</span></span> <span data-ttu-id="8149e-467">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-467">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management**.</span></span>
    2. <span data-ttu-id="8149e-468">**AD FS** \> **サービス** \> **証明書** を展開し、証明書を記録しておきます。</span><span class="sxs-lookup"><span data-stu-id="8149e-468">Expand **AD FS** \> **Service** \> **Certificates**, and make a note of the certificates.</span></span> <span data-ttu-id="8149e-469">たとえば、1 つの証明書は、dc1.contoso.com の場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-469">For example, one certificate might be dc1.contoso.com.</span></span>
    3. <span data-ttu-id="8149e-470">AOS マシンの、Microsoft 管理コンソール証明書スナップインで、**証明書 (ローカル コンピューター)** \> **信頼済ルート証明機関** \> **証明書**の順に移動し、AD FS 証明書が一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-470">On the AOS machine, in the Microsoft Management Console Certificates snap-in, go to **Certificates (Local Computer)** \> **Trusted Root Certification Authorities** \> **Certificates**, and verify that the AD FS certificate is listed.</span></span>

<span data-ttu-id="8149e-471">サイトが安全でないことを示すメッセージが表示された場合は、AD FS の Secure Sockets Layer (SSL) 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="8149e-471">If you receive a message that states that the site isn't secure, you haven't added your Secure Sockets Layer (SSL) certificate for AD FS to the Trusted Root Certification Authorities store.</span></span>

### <a name="you-cant-connect-to-the-remote-server-in-some-locations"></a><span data-ttu-id="8149e-472">一部の地域ではリモート サーバーに接続できません</span><span class="sxs-lookup"><span data-stu-id="8149e-472">You can't connect to the remote server in some locations</span></span>
<span data-ttu-id="8149e-473">次の場所でリモート サーバーに接続できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-473">You might not be able to connect to the remote server at the following places:</span></span>

- <span data-ttu-id="8149e-474">System.Net.HttpWebRequest.GetResponse()</span><span class="sxs-lookup"><span data-stu-id="8149e-474">System.Net.HttpWebRequest.GetResponse()</span></span>
- <span data-ttu-id="8149e-475">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span><span class="sxs-lookup"><span data-stu-id="8149e-475">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span></span>
- <span data-ttu-id="8149e-476">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span><span class="sxs-lookup"><span data-stu-id="8149e-476">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span></span>

<span data-ttu-id="8149e-477">この場合、エラーを受け取る C:\\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\ ログ フォルダーに移動し、出力ファイルに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-477">In this case, go to the C:\\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\log folder where you receive the error and note the out file.</span></span> <span data-ttu-id="8149e-478">out ファイルには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8149e-478">The out file contains the following information:</span></span>

> <span data-ttu-id="8149e-479">System.Net.WebException: リモート サーバーに接続できません ---\></span><span class="sxs-lookup"><span data-stu-id="8149e-479">System.Net.WebException: Unable to connect to the remote server ---\></span></span>

> <span data-ttu-id="8149e-480">System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="8149e-480">System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond x.x.x.x:443</span></span>

<span data-ttu-id="8149e-481">Psping を使用してリモート サーバーに対する接続を試みることもできます。</span><span class="sxs-lookup"><span data-stu-id="8149e-481">You can also use Psping to try to reach the remote server.</span></span> <span data-ttu-id="8149e-482">Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-482">For information about Psping, see [Psping](/sysinternals/downloads/psping).</span></span>

### <a name="redirect-sign-in-questions-and-issues"></a><span data-ttu-id="8149e-483">サインイン時の質問および問題をリダイレクト</span><span class="sxs-lookup"><span data-stu-id="8149e-483">Redirect sign-in questions and issues</span></span>
<span data-ttu-id="8149e-484">サインイン時に問題が発生した場合は、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-484">If you're having issues when you sign-in, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="8149e-485">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-485">Here is an example:</span></span>

- <span data-ttu-id="8149e-486">**プロビジョニング \_AdminPrincipalName**: `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="8149e-486">**Provisioning\_AdminPrincipalName**: `AXServiceUser@contoso.com`</span></span>
- <span data-ttu-id="8149e-487">**プロビジョニング\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="8149e-487">**Provisioning\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span></span>

<span data-ttu-id="8149e-488">値が有効でない場合は、処理を続行できず、LCS から再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-488">If the values aren't valid, you won't be able to proceed, and you must redeploy from LCS.</span></span>

<span data-ttu-id="8149e-489">Reset-DatabaseUsers.ps1 を使用した場合、変更内容を有効にする前に、Dynamics サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-489">If you used Reset-DatabaseUsers.ps1, you must restart the Dynamics Service before your changes take effect.</span></span> <span data-ttu-id="8149e-490">引き続きサインインの問題がある場合は、USERINFO テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** の値を記録してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-490">If you still have sign-in issues, in the USERINFO table, note the **NETWORKDOMAIN** and **NETWORKALIAS** values.</span></span> <span data-ttu-id="8149e-491">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-491">Here is an example:</span></span>

- <span data-ttu-id="8149e-492">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="8149e-492">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span></span>
- <span data-ttu-id="8149e-493">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="8149e-493">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span></span>

<span data-ttu-id="8149e-494">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** \> **サービス**に移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-494">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management** \> **Service**.</span></span> <span data-ttu-id="8149e-495">**フェデレーション サービス プロパティの保守と編集** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="8149e-495">Right-click **Service and Edit Federation Service Properties**.</span></span> <span data-ttu-id="8149e-496">**フェデレーション サービスの識別子**は **USERINFO.NETWORKDOMAIN** 値と一致し、URL に HTTPS を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-496">The **Federation Service identifier** should match the **USERINFO.NETWORKDOMAIN** value and have HTTPS in the URL.</span></span> <span data-ttu-id="8149e-497">(例: `https://DC1.contoso.com/adfs`)。</span><span class="sxs-lookup"><span data-stu-id="8149e-497">(For example: `https://DC1.contoso.com/adfs`).</span></span> 

<span data-ttu-id="8149e-498">AD FS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **AD FS** \> **管理者**に移動してエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-498">On the AD FS machine, in Event Viewer, go to **Applications and Services Logs** \> **AD FS** \> **Admin**, and make a note of any errors.</span></span>

## <a name="sign-in-issues"></a><span data-ttu-id="8149e-499">サインインの問題</span><span class="sxs-lookup"><span data-stu-id="8149e-499">Sign-in issues</span></span>
<span data-ttu-id="8149e-500">サインインに関する問題が発生した場合には、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-500">If you or other users experience sign-in issues, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="8149e-501">値が有効な場合は、プライマリ SQL Server マシンで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-501">If the values are valid, run the following command on the primary SQL Server machine.</span></span>

```powershell
.\Reset-DatabaseUsers.ps1
```

<span data-ttu-id="8149e-502">タスク マネージャーの各 AOS マシンで、**AXService.exe** を選択し、**タスクの終了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8149e-502">On each AOS machine, in Task Manager, select **AXService.exe**, and then select **End task**.</span></span>

<span data-ttu-id="8149e-503">ユーザーがリセットされたことを確認するには、SQL AXDB で次の select クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-503">To verify that a user has been reset, run the following select query in the SQL AXDB.</span></span>

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> <span data-ttu-id="8149e-504">Azure Active Directory (Azure AD) 環境 (オンライン環境) では、SID はネットワーク エイリアスおよびネットワーク ドメインのハッシュです。</span><span class="sxs-lookup"><span data-stu-id="8149e-504">In an Azure Active Directory (Azure AD) environment (an online environment), the SID is a hash of a network alias and a network domain.</span></span> <span data-ttu-id="8149e-505">AD DS 環境 (オンプレミス環境) で、SID はネットワーク エイリアスのハッシュであり、プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="8149e-505">In an AD DS environment (an on-premises environment), the SID is a hash of a network alias and an identify provider.</span></span>

<span data-ttu-id="8149e-506">場合によっては、引き続きサインインできず、次のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-506">In some cases, you still might not be able to sign in and receive the following error:</span></span>

> <span data-ttu-id="8149e-507">現在の資格情報でログインする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-507">You are not authorized to login with your current credentials.</span></span> <span data-ttu-id="8149e-508">数秒でログイン ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="8149e-508">You will be redirected to the login page in a few seconds.</span></span>

<span data-ttu-id="8149e-509">このエラーが発生した場合は、このトピックの [AD FS](troubleshoot-on-prem.md#ad-fs) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-509">If this error occurs, see the [AD FS](troubleshoot-on-prem.md#ad-fs) section of this topic.</span></span>

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a><span data-ttu-id="8149e-510">System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)</span><span class="sxs-lookup"><span data-stu-id="8149e-510">System.Data.SqlClient.SqlException (0x80131904) and System.ComponentModel.Win32Exception (0x80004005)</span></span>
<span data-ttu-id="8149e-511">次のエラーのいずれかが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-511">You might receive one of the following errors:</span></span>

> <span data-ttu-id="8149e-512">System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、サインイン プロセス時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-512">System.Data.SqlClient.SqlException (0x80131904): A connection was successfully established with the server, but then an error occurred during the sign-in process.</span></span> <span data-ttu-id="8149e-513">(プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)</span><span class="sxs-lookup"><span data-stu-id="8149e-513">(provider: SSL Provider, error: 0 - The certificate chain was issued by an authority that is not trusted.)</span></span>

> <span data-ttu-id="8149e-514">System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました</span><span class="sxs-lookup"><span data-stu-id="8149e-514">System.ComponentModel.Win32Exception (0x80004005): The certificate chain was issued by an authority that is not trusted</span></span>

<span data-ttu-id="8149e-515">この場合、証明書がインストールされていないか、正しいユーザーにアクセス権が与えられていません。</span><span class="sxs-lookup"><span data-stu-id="8149e-515">In this case, the certificates haven't been installed or given access to the correct users.</span></span> <span data-ttu-id="8149e-516">このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-516">To resolve this error, add the public key SQL Server certificate to all the Service Fabric nodes.</span></span>

## <a name="keyset-doesnt-exist"></a><span data-ttu-id="8149e-517">Keyset が存在しません</span><span class="sxs-lookup"><span data-stu-id="8149e-517">Keyset doesn't exist</span></span>
<span data-ttu-id="8149e-518">キーセットが存在しないことがわかった場合、スクリプトがすべてのコンピューターで実行されなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="8149e-518">If you find that the keyset doesn't exist, scripts were not run on all machines.</span></span> <span data-ttu-id="8149e-519">適切な設定の「VM の設定」セクション、および環境の配置トピックを確認し完了します。</span><span class="sxs-lookup"><span data-stu-id="8149e-519">Review and complete the "Set up VMs" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="8149e-520">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-520">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupvms)
- [<span data-ttu-id="8149e-521">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-521">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupvms)

<span data-ttu-id="8149e-522">各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="8149e-522">Copy the scripts in each folder to the VMs that correspond to the folder name.</span></span>

<span data-ttu-id="8149e-523">また、正しいドメインを使うことを検証する .csv ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-523">Additionally, check the .csv file to verify that the correct domain is used.</span></span>

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a><span data-ttu-id="8149e-524">エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」</span><span class="sxs-lookup"><span data-stu-id="8149e-524">Error: "RunAsync failed due to an unhandled FabricException causing replica to fault"</span></span>
<span data-ttu-id="8149e-525">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-525">You might receive the following error:</span></span>

> <span data-ttu-id="8149e-526">未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-526">RunAsync failed due to an unhandled FabricException causing replica to fault: System.Fabric.FabricException: The first Fabric upgrade must specify both the code and config versions.</span></span> <span data-ttu-id="8149e-527">要求された値: 0.0.0.0:</span><span class="sxs-lookup"><span data-stu-id="8149e-527">Requested value: 0.0.0.0:</span></span>

<span data-ttu-id="8149e-528">この場合、ClusterConfig.json diagnosticsStore をネットワーク共有からローカル パスに変更します。</span><span class="sxs-lookup"><span data-stu-id="8149e-528">In this case, change the ClusterConfig.json diagnosticsStore from a network share to a local path.</span></span> <span data-ttu-id="8149e-529">たとえば、**\\\\サーバー\\パス**を、規定値の **C:\\ProgramData\\SF\\DiagnosticsStore** に変更します。</span><span class="sxs-lookup"><span data-stu-id="8149e-529">For example, change **\\\\server\\path** to a default value of **C:\\ProgramData\\SF\\DiagnosticsStore**.</span></span>

## <a name="service-fabric-aos-node-error-during-build-the-execution-time-out-expired"></a><span data-ttu-id="8149e-530">ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ</span><span class="sxs-lookup"><span data-stu-id="8149e-530">Service Fabric AOS node error during build: The execution time-out expired</span></span>
<span data-ttu-id="8149e-531">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-531">**Error:**</span></span>

> <span data-ttu-id="8149e-532">操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。</span><span class="sxs-lookup"><span data-stu-id="8149e-532">The timeout period elapsed prior to completion of the operation or the server is not responding.</span></span>  
> <span data-ttu-id="8149e-533">明細書は終了しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-533">The statement has been terminated.</span></span>

<span data-ttu-id="8149e-534">一度に 1 つの AOS マシンのみ DB Sync を実行できます。</span><span class="sxs-lookup"><span data-stu-id="8149e-534">Only one AOS machine can run DB Sync at a time.</span></span> <span data-ttu-id="8149e-535">AOS VM の 1 つが DB Sync を実行してされているため、および他の VM が実行できないという警告が表示されるため、このエラーは無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-535">You can safely ignore this error, because it means that one of the AOS VMs is running DB Sync, and therefore the other VMs produce a warning that they can't run it.</span></span> <span data-ttu-id="8149e-536">DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で**アプリケーションおよびサービスのログ** \> **Microsoft** \> **Dynamics** \> **AX DatabaseSynchronize/Operational** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-536">To verify that DB Sync is running, on the AOS VM that isn't producing warnings, in Event Viewer, go to **Applications and Services Log** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational**.</span></span>

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a><span data-ttu-id="8149e-537">エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」</span><span class="sxs-lookup"><span data-stu-id="8149e-537">Error: "RequireNonce is 'true' (default) but validationContext.Nonce is null"</span></span>
<span data-ttu-id="8149e-538">このエラーは、クライアントにサインインした後も Internet Explorer で HTTP エラー 500 として表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-538">This error also appears as an HTTP error 500 in Internet Explorer after you sign in to the client.</span></span> <span data-ttu-id="8149e-539">Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。</span><span class="sxs-lookup"><span data-stu-id="8149e-539">The nonce that is issued can't be validated if Internet Explorer is in Enhanced Security Configuration.</span></span>

<span data-ttu-id="8149e-540">クライアントにサインインするには、サーバー マネージャーを介して Internet Explorer のセキュリティ強化設定を無効にします。</span><span class="sxs-lookup"><span data-stu-id="8149e-540">To sign in to the client, disable Enhanced Security Configuration for Internet Explorer via Server Manager.</span></span>

## <a name="error-invalid-algorithm-specified--cryptography"></a><span data-ttu-id="8149e-541">エラー、「無効なアルゴリズムが指定されている/暗号化」</span><span class="sxs-lookup"><span data-stu-id="8149e-541">Error: "Invalid algorithm specified / Cryptography"</span></span>
<span data-ttu-id="8149e-542">このエラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-542">If you receive this error, you must use the Microsoft Enhanced RSA and AES Cryptographic Provider.</span></span> <span data-ttu-id="8149e-543">詳細については、証明書の要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-543">For more information, see the certificate requirements.</span></span> <span data-ttu-id="8149e-544">また、credentials.json ファイルの構造が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-544">Additionally, verify that the structure of the credentials.json file is correct.</span></span>

<span data-ttu-id="8149e-545">正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-545">If you must re-create the certificate by using the correct provider, follow these steps.</span></span>

1. <span data-ttu-id="8149e-546">正しいプロバイダーを使用して証明書を再度作成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-546">Create the certificate again by using the correct provider.</span></span>
2. <span data-ttu-id="8149e-547">**ConfigTemplate.xml** ファイルの変更。</span><span class="sxs-lookup"><span data-stu-id="8149e-547">Change the **ConfigTemplate.xml** file.</span></span>
3. <span data-ttu-id="8149e-548">クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、**Test-D365FOConfiguration.ps1** スクリプトに合格するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-548">Run the infrastructure scripts on all machines in the cluster, and make sure that the **Test-D365FOConfiguration.ps1** script passes.</span></span>
4. <span data-ttu-id="8149e-549">LCS から環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-549">Reconfigure the environment from LCS.</span></span>

## <a name="an-unable-to-find-certificate-error-occurs-when-you-run-test-d365foconfigurationps1"></a><span data-ttu-id="8149e-550">Test-D365FOConfiguration.ps1 を実行した際、「証明書を検出できません」エラーが発生</span><span class="sxs-lookup"><span data-stu-id="8149e-550">An "Unable to find certificate" error occurs when you run Test-D365FOConfiguration.ps1</span></span>
<span data-ttu-id="8149e-551">このエラーが表示された場合は、証明書もしくは拇印が複数の目的で結合されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-551">If you receive this error, check whether certificates or thumbprints are being combined for multiple purposes.</span></span> <span data-ttu-id="8149e-552">たとえば、クライアントと SessionAuthentication が結合される場合、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8149e-552">For example, if the client and SessionAuthentication are combined, you will receive this error.</span></span> <span data-ttu-id="8149e-553">証明書を結合しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8149e-553">We recommend that you not combine certificates.</span></span> <span data-ttu-id="8149e-554">詳細については、 証明書要件を参照し、domain.com\\ ユーザーとドメイン\\ユーザー (たとえば、NETBIOS 構造) の acl.csv ファイルを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-554">For more information, see the certificate requirements, and check the acl.csv file for domain.com\\user versus domain\\user (for example, NETBIOS structure).</span></span>

## <a name="the-client-and-server-cant-communicate-because-they-dont-have-a-common-algorithm"></a><span data-ttu-id="8149e-555">クライアントとサーバーは共通のアルゴリズムを持たないため通信できません</span><span class="sxs-lookup"><span data-stu-id="8149e-555">The client and server can't communicate because they don't have a common algorithm</span></span>
<span data-ttu-id="8149e-556">この問題が発生した場合は、使用している環境の適切な設定および配置のトピックの「計画と証明書の取得」の説明に従って、作成された証明書が指定したプロバイダーを使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-556">If this issue occurs, verify that the certificates that are created use the specified provider, as explained in the "Plan and acquire your certificates" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="8149e-557">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-557">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#plancert)
- [<span data-ttu-id="8149e-558">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-558">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts"></a><span data-ttu-id="8149e-559">グループ管理サービス アカウント の一覧の検索</span><span class="sxs-lookup"><span data-stu-id="8149e-559">Find a list of group managed service accounts</span></span>
<span data-ttu-id="8149e-560">すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-560">To find a list of all groups and hosts, run the following command.</span></span>

```
Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword
```

## <a name="addcerttoserviceprincipal-script-fails-on-import-module"></a><span data-ttu-id="8149e-561">Import-Module での AddCertToServicePrincipal スクリプトの失敗</span><span class="sxs-lookup"><span data-stu-id="8149e-561">AddCertToServicePrincipal script fails on Import-Module</span></span>
<span data-ttu-id="8149e-562">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-562">**Error:**</span></span>

> <span data-ttu-id="8149e-563">Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="8149e-563">AddCertToServicePrincipal script failing on Import-Module : Could not load file or assembly 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span> <span data-ttu-id="8149e-564">厳密な名前の検証に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="8149e-564">Strong name validation failed.</span></span> <span data-ttu-id="8149e-565">(HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-565">(Exception from HRESULT: 0x8013141A) may have multiple versions of the same module installed.</span></span>

<span data-ttu-id="8149e-566">**ステップ:** 問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-566">**Steps:** To resolve this issue, follow these steps.</span></span>

1. <span data-ttu-id="8149e-567">Windows PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-567">Run the following command in Windows PowerShell.</span></span>

```powershell
Uninstall-Module -Name AzureRM
Install-Module AzureRM
```

2. <span data-ttu-id="8149e-568">Windows PowerShell ウィンドウを閉じて、スクリプトを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-568">Close the Windows PowerShell window, and try to run the script again.</span></span>

## <a name="reportingservicessetupexe-error"></a><span data-ttu-id="8149e-569">ReportingServicesSetup.exe エラー</span><span class="sxs-lookup"><span data-stu-id="8149e-569">ReportingServicesSetup.exe error</span></span>
<span data-ttu-id="8149e-570">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="8149e-570">**Error:**</span></span>
> <span data-ttu-id="8149e-571">ReportingServicesSetup.exe エラー: 0 : アプリケーション fabric:/ReportingService は10分後から OK ではありません。</span><span class="sxs-lookup"><span data-stu-id="8149e-571">ReportingServicesSetup.exe Error: 0 : Application fabric:/ReportingService is not OK after 10 minutes</span></span>  
> <span data-ttu-id="8149e-572">アプリケーション: ReportingServicesBootstrapper.exe</span><span class="sxs-lookup"><span data-stu-id="8149e-572">Application: ReportingServicesBootstrapper.exe</span></span>  
> <span data-ttu-id="8149e-573">フレームワーク バージョン: v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="8149e-573">Framework Version: v4.0.30319</span></span>  
> <span data-ttu-id="8149e-574">説明: プロセスは未処理の例外によって中止されました。</span><span class="sxs-lookup"><span data-stu-id="8149e-574">Description: The process was terminated due to an unhandled exception.</span></span>

<span data-ttu-id="8149e-575">**理由:** このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効にされていますが、有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="8149e-575">**Reason:** If you receive this error, strong name validation is enabled in the Reporting server, but it should not be enabled.</span></span>

<span data-ttu-id="8149e-576">**ステップ:** 問題を解決するには、レポート サーバー マシンで **config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-576">**Steps:** To resolve this issue, run the **config-PreReq** script on the Reporting server machine.</span></span>

## <a name="the-requested-operation-requires-elevation"></a><span data-ttu-id="8149e-577">要求された操作には、昇格が必要です</span><span class="sxs-lookup"><span data-stu-id="8149e-577">The requested operation requires elevation</span></span>
<span data-ttu-id="8149e-578">AOS ユーザーはローカル管理者グループに属しておらず、ユーザー アカウント コントロール (UAC) が正しく無効化されていないために、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="8149e-578">This issue occurs because AOS users aren't in the local administrator group, and User Account Control (UAC) hasn't been disabled correctly.</span></span> <span data-ttu-id="8149e-579">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8149e-579">To resolve the issue, follow these steps.</span></span>

1. <span data-ttu-id="8149e-580">環境の適切な設定および配置トピックの「VMs とドメインを結合」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-580">Add AOS users as local admins, as described in the "Join VMs to the domain" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="8149e-581">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="8149e-581">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#joindomain)
    - [<span data-ttu-id="8149e-582">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="8149e-582">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#joindomain)

2. <span data-ttu-id="8149e-583">すべての AOS コンピューターで、**Config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-583">Run the **Config-PreReq** script on all the AOS machines.</span></span>
3. <span data-ttu-id="8149e-584">**テスト構成**スクリプトがパスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8149e-584">Make sure that the **Test-Configuration** script passes.</span></span>
4. <span data-ttu-id="8149e-585">UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-585">If UAC was changed, you must restart the machine before the changes take effect.</span></span>

## <a name="files-in-use-errors"></a><span data-ttu-id="8149e-586">使用中ファイルのエラー</span><span class="sxs-lookup"><span data-stu-id="8149e-586">Files in use errors</span></span>
<span data-ttu-id="8149e-587">これらのエラーが発生した場合は、Service Fabric より指示された除外ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="8149e-587">If these errors occur, set up the exclusion rules that are advised by Service Fabric.</span></span> <span data-ttu-id="8149e-588">詳細については、[環境設定](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-588">For information, see [Environment setup](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="apply-deployable-packages-during-deployment"></a><span data-ttu-id="8149e-589">配置中に配置可能パッケージを適用する</span><span class="sxs-lookup"><span data-stu-id="8149e-589">Apply deployable packages during deployment</span></span>
### <a name="package-deployment-fails-because-of-a-path-too-long-exception"></a><span data-ttu-id="8149e-590">「パスが長過ぎる」例外によってパッケージの展開が失敗する</span><span class="sxs-lookup"><span data-stu-id="8149e-590">Package deployment fails because of a "path too long" exception</span></span>
<span data-ttu-id="8149e-591">Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="8149e-591">Because of a 260-character limit in Microsoft Windows, deployment will fail if a package has a longer name, or if the on-premises share has the full FQDN path.</span></span> <span data-ttu-id="8149e-592">文字数の制限を超過した場合、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-592">If the character limit is exceeded, you receive the following error:</span></span>

> <span data-ttu-id="8149e-593">System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。</span><span class="sxs-lookup"><span data-stu-id="8149e-593">System.IO.PathTooLongException: The specified path, file name, or both are too long.</span></span> <span data-ttu-id="8149e-594">完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-594">The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters.</span></span> <span data-ttu-id="8149e-595">at System.IO.PathHelper.GetFullPathName</span><span class="sxs-lookup"><span data-stu-id="8149e-595">at System.IO.PathHelper.GetFullPathName</span></span>

<span data-ttu-id="8149e-596">この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。</span><span class="sxs-lookup"><span data-stu-id="8149e-596">To work around this issue, shorten the package name, and then apply the package again.</span></span> <span data-ttu-id="8149e-597">または、オンプレミス資産の共有パス全体の長さを短くしてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-597">Alternatively, shorten the overall length of the share path for the on-premises assets.</span></span>

### <a name="package-deployment-fails-because-of-a-serialization-error"></a><span data-ttu-id="8149e-598">シリアル化エラーが原因でパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="8149e-598">Package deployment fails because of a serialization error</span></span>
<span data-ttu-id="8149e-599">パッケージ配置中、次のエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-599">During package deployment, you might receive the following error:</span></span>

> <span data-ttu-id="8149e-600">シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-600">Serialization version mismatch detect, make sure the runtime DLLs are in sync with the deployed metadata.</span></span> <span data-ttu-id="8149e-601">「XXX」ファイルのバージョン</span><span class="sxs-lookup"><span data-stu-id="8149e-601">Version of file 'XXX'.</span></span> <span data-ttu-id="8149e-602">DLL 「XXX」のバージョン</span><span class="sxs-lookup"><span data-stu-id="8149e-602">Version of DLL 'XXX'</span></span>

<span data-ttu-id="8149e-603">この場合、パッケージが展開された環境のバージョンはパッケージが展開中の環境のバージョンとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-603">In this case, the version of the environment where the package was developed may differ from the version of the environment that the package is being deployed in.</span></span>

<span data-ttu-id="8149e-604">この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。</span><span class="sxs-lookup"><span data-stu-id="8149e-604">To work around this issue, keep the development or build environments on the same version as the deployed on-premises environment.</span></span> <span data-ttu-id="8149e-605">パッケージのアップロード先にあるアセット ライブラリの**追加の詳細**セクションをクリックすることにより、パッケージ バージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-605">You can confirm the package version by looking in the **Additional details** section in the Asset library where the package is uploaded.</span></span> <span data-ttu-id="8149e-606">エラーを修正するには、オンプレミス環境に配置されたバージョンと同じまたはそれ以前のバージョンにパッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="8149e-606">To fix the error, generate the package on a version that is the same as or earlier than the version that is deployed on the on-premises environment.</span></span>

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a><span data-ttu-id="8149e-607">欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="8149e-607">Package deployment fails because of dependencies on missing modules</span></span>
<span data-ttu-id="8149e-608">依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次と類似するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-608">If you try to apply a package that is missing dependent modules, package application will fail, and you will receive a message that resembles the following:</span></span>

> <span data-ttu-id="8149e-609">パッケージ \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="8149e-609">Package \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span></span>
>
> <span data-ttu-id="8149e-610">パッケージ \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="8149e-610">Package \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span></span>
>
> <span data-ttu-id="8149e-611">パッケージ \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span><span class="sxs-lookup"><span data-stu-id="8149e-611">Package \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span></span>

<span data-ttu-id="8149e-612">問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、**アプリケーションとサービス**を開き、**Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** の順で移動して、見つからないモジュールのあるイベントを表示します。</span><span class="sxs-lookup"><span data-stu-id="8149e-612">To confirm the issue and find the missing dependencies, in Event Viewer, open **Application and Services**, and then go to **Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** to view events that have missing modules.</span></span> <span data-ttu-id="8149e-613">たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。</span><span class="sxs-lookup"><span data-stu-id="8149e-613">For example, one of the modules that is typically missing is ApplicationFoundationFormAdaptor.</span></span>

<span data-ttu-id="8149e-614">この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="8149e-614">To fix this issue and successfully apply the package, either add dependent modules, or remove modules that require dependent modules.</span></span> <span data-ttu-id="8149e-615">依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-615">To add dependent modules, you must include the dependencies when you build the package.</span></span> <span data-ttu-id="8149e-616">モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。</span><span class="sxs-lookup"><span data-stu-id="8149e-616">To remove modules, you can use ModelUtil.exe to delete a module.</span></span> <span data-ttu-id="8149e-617">詳細については、「[モデルのエクスポートとインポート](../dev-tools/models-export-import.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8149e-617">For more information, see [Export and import a model](../dev-tools/models-export-import.md).</span></span>

### <a name="package-deployment-works-in-a-one-box-environment-but-not-in-the-sandbox-environment"></a><span data-ttu-id="8149e-618">パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない</span><span class="sxs-lookup"><span data-stu-id="8149e-618">Package deployment works in a one-box environment but not in the sandbox environment</span></span>
<span data-ttu-id="8149e-619">1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-619">A one-box environment might have all the modules installed, whereas the sandbox environment might have only the modules that are required in order to run your production environment.</span></span> <span data-ttu-id="8149e-620">開発環境で作成されたパッケージが、サンドボックス環境ではなく 1 ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。</span><span class="sxs-lookup"><span data-stu-id="8149e-620">If the package that was built in the dev environment has a dependency on the modules that are present in the one-box environment but not in the sandbox environment, the package won't work in the sandbox environment.</span></span>

<span data-ttu-id="8149e-621">この問題を解決するには、依存するすべてのモジュールを確認し、実稼動環境で不要なファーム アダプターまたはその他のモジュールをプルしないようにします。</span><span class="sxs-lookup"><span data-stu-id="8149e-621">To resolve this issue, look at all the modules that you're dependent on, and make sure that you don't pull any farm adapter or any other modules that aren't required in the production environment.</span></span> <span data-ttu-id="8149e-622">ビルド ボックスからパッケージを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8149e-622">The best practice is to take the package from the build box.</span></span>

## <a name="an-error-occurs-when-you-sign-in-to-on-premises-environments"></a><span data-ttu-id="8149e-623">オンプレミス環境へのログイン時にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="8149e-623">An error occurs when you sign in to on-premises environments</span></span>

<span data-ttu-id="8149e-624">**プラットフォーム更新 12:** **システム管理** \> **設定** \> **クライアント パフォーマンス オプション**に移動して、Skype 統合を無効にしてください。</span><span class="sxs-lookup"><span data-stu-id="8149e-624">**Platform update 12:** Turn off the Skype integration by going to **System administration** \> **Setup** \> **Client performance options**.</span></span> <span data-ttu-id="8149e-625">アプリに移動するとき、`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true` の例のように、**?debug=true** を URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-625">When you go to the app, append **?debug=true** to the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>

<span data-ttu-id="8149e-626">**プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:** 既知の Skype アプリケーション プログラミング インターフェイス (API) 問題は、オンプレミス環境へのサインイン機能に影響します。</span><span class="sxs-lookup"><span data-stu-id="8149e-626">**Platform update 8 and Platform update 11:** A known Skype application programming interface (API) issue affects the ability to sign in to on-premises environments.</span></span> <span data-ttu-id="8149e-627">この問題の解決方法を調査しています。</span><span class="sxs-lookup"><span data-stu-id="8149e-627">We are investigating a resolution for this issue.</span></span> <span data-ttu-id="8149e-628">この問題を回避するために、次の例のように URL の末尾に **?debug=true** を追加できます。`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span><span class="sxs-lookup"><span data-stu-id="8149e-628">To work around this issue, you can add **?debug=true** to the end of the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>

## <a name="additional-deployments-for-example-two-sandbox-deployments-or-a-sandbox-and-production-deployment"></a><span data-ttu-id="8149e-629">追加の配置 (たとえば、2 つのサンド ボックス展開、またはサンド ボックスおよび生産の配置)</span><span class="sxs-lookup"><span data-stu-id="8149e-629">Additional deployments (for example, two sandbox deployments, or a sandbox and production deployment)</span></span>

<span data-ttu-id="8149e-630">追加の環境を展開すると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-630">You will receive the following error when you deploy an additional environment:</span></span>

> <span data-ttu-id="8149e-631">\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: アプリケーション グループ ID は、AD FS コンフィギュレーションで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-631">.\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: The application group identifier must be unique in AD FS configuration.</span></span>

<span data-ttu-id="8149e-632">配備手順の次のセクションをスキップまたは変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8149e-632">You can skip or modify the following sections in the deployment instructions.</span></span>

### <a name="plan-and-acquire-your-certificates-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdplancert-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdplancert"></a><span data-ttu-id="8149e-633">証明書の計画と取得 ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#plancert) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="8149e-633">Plan and acquire your certificates (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#plancert) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#plancert))</span></span>
- <span data-ttu-id="8149e-634">同一のオンプレミスのローカル エージェント証明書を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-634">You must use the same on-premises local agent certificate.</span></span>
- <span data-ttu-id="8149e-635">同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。</span><span class="sxs-lookup"><span data-stu-id="8149e-635">You can use same star certificates (AOS SSL and Service Fabric).</span></span>
- <span data-ttu-id="8149e-636">残りの証明書は既存の環境の証明書とは異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-636">The remaining certificates should probably differ from the certificates for the existing environment.</span></span>

### <a name="download-setup-scripts-from-lcs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mddownloadscripts-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mddownloadscripts"></a><span data-ttu-id="8149e-637">LCS からのセットアップ スクリプトのダウンロード ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#downloadscripts) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="8149e-637">Download setup scripts from LCS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#downloadscripts) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts))</span></span>
- <span data-ttu-id="8149e-638">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-638">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="set-up-a-standalone-service-fabric-cluster-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdsetupsfcluster-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdsetupsfcluster"></a><span data-ttu-id="8149e-639">([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#setupsfcluster) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster) に記載されているように) スタンドアロン Service Fabric クラスタを設定します</span><span class="sxs-lookup"><span data-stu-id="8149e-639">Set up a standalone Service Fabric cluster (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#setupsfcluster) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster))</span></span>
- <span data-ttu-id="8149e-640">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-640">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="configure-lcs-connectivity-for-the-tenant-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigurelcs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigurelcs"></a><span data-ttu-id="8149e-641">テナント用 LCS 接続 のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configurelcs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="8149e-641">Configure LCS connectivity for the tenant (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configurelcs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs))</span></span>
- <span data-ttu-id="8149e-642">テナントに対して、このタスクを 1 回のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-642">You must complete this task only one time for the tenant.</span></span>

### <a name="configure-ad-fs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigureadfs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigureadfs"></a><span data-ttu-id="8149e-643">AD FS のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configureadfs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="8149e-643">Configure AD FS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configureadfs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs))</span></span>
- <span data-ttu-id="8149e-644">すでに完了しているので、スクリプト 1、スクリプト 2、スクリプト 3 はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="8149e-644">You can skip scripts 1, 2, and 3, because they have already been done.</span></span>
- <span data-ttu-id="8149e-645">新しい **hosturl** 値を使用している場合でも、.\\Publish-ADFSApplicationGroup.ps1 スクリプトは失敗します。</span><span class="sxs-lookup"><span data-stu-id="8149e-645">The .\\Publish-ADFSApplicationGroup.ps1 script will fail even when the new **hosturl** value is used.</span></span> <span data-ttu-id="8149e-646">したがって、この手順を手動で完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8149e-646">Therefore, you must manually complete these steps.</span></span>
- <span data-ttu-id="8149e-647">AD FS マネージャーで、**AD FS** \> **アプリケーション グループ**に移動し、**Microsoft Dynamics 365 for Operations オンプレミス**を開きます。</span><span class="sxs-lookup"><span data-stu-id="8149e-647">In AD FS Manager, go to **AD FS** \> **Application groups**, and open **Microsoft Dynamics 365 for Operations On-premises**.</span></span> <span data-ttu-id="8149e-648">次に、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-648">Then follow these steps:</span></span>

    1. <span data-ttu-id="8149e-649">ネイティブ アプリケーション **Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="8149e-649">Open the native application **Microsoft Dynamics 365 for Operations On-premises - Native application**.</span></span> <span data-ttu-id="8149e-650">新しい環境 (DNS) の リダイレクト URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-650">Add the redirect URI of the new environment (DNS).</span></span>
    2. <span data-ttu-id="8149e-651">ネイティブ アプリケーション **Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 - ネイティブ アプリケーション**を開きます。</span><span class="sxs-lookup"><span data-stu-id="8149e-651">Open the native application **Microsoft Dynamics 365 for Operations On-premises - Financial Reporting - Native application**.</span></span> <span data-ttu-id="8149e-652">新しい環境 (DNS) の リダイレクト URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-652">Add the redirect URI of the new environment (DNS).</span></span>

## <a name="redeploy-ssrs-reports"></a><span data-ttu-id="8149e-653">SSRS レポートを再配置する</span><span class="sxs-lookup"><span data-stu-id="8149e-653">Redeploy SSRS reports</span></span>
<span data-ttu-id="8149e-654">SF.SyncLog のエントリを削除して、AOS マシンの 1 つを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8149e-654">Delete the entry in SF.SyncLog, and then restart one of the AOS machines.</span></span> <span data-ttu-id="8149e-655">AOS コンピューターは DB 同期を再実行し、レポートを配置します。</span><span class="sxs-lookup"><span data-stu-id="8149e-655">The AOS machine will rerun DB Sync and then deploy reports.</span></span>

## <a name="add-axdbadmin-to-tempdb-after-a-sql-server-restart-via-a-stored-procedure"></a><span data-ttu-id="8149e-656">ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。</span><span class="sxs-lookup"><span data-stu-id="8149e-656">Add axdbadmin to tempdb after a SQL Server restart via a stored procedure</span></span>
<span data-ttu-id="8149e-657">SQL Server を再起動すると、tempdb データベースが再作成されます。</span><span class="sxs-lookup"><span data-stu-id="8149e-657">When SQL Server is restarted, the tempdb database is re-created.</span></span> <span data-ttu-id="8149e-658">結果として、アクセス許可が不足します。</span><span class="sxs-lookup"><span data-stu-id="8149e-658">As a result, there will be missing permissions.</span></span> <span data-ttu-id="8149e-659">マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="8149e-659">Run the following script to create a stored procedure on the master database.</span></span>

```
\-----

USE [master]

GO

CREATE procedure [dbo].[CREATETEMPDBPERMISSIONS] as begin exec ('USE tempdb; declare \@dbaccesscount int; exec sp_grantlogin ''axdbadmin''; select \@dbaccesscount = COUNT(\*) from master..syslogins where name = ''axdbadmin''; if (\@dbaccesscount \<\> 0) exec sp_grantdbaccess ''axdbadmin''; ALTER USER [axdbadmin] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''axdbadmin''; EXEC sp_addrolemember N''db_datawriter'', N''axdbadmin''; EXEC sp_addrolemember N''db_ddladmin'', N''axdbadmin''; exec sp_grantdbaccess ''contoso\\svc-AXSF\$''; ALTER USER [contoso\\svc-AXSF\$] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''contoso\\svc-AXSF\$''; EXEC sp_addrolemember N''db_datawriter'', N''contoso\\svc-AXSF\$''; EXEC sp_addrolemember N''db_ddladmin'', N''contoso\\svc-AXSF\$'';') end

GO

EXEC sp_procoption N'[dbo].[CREATETEMPDBPERMISSIONS]', 'startup', '1'

\-----
```

## <a name="error-updates-to-existing-credential-with-keyid-key-is-not-allowed"></a><span data-ttu-id="8149e-660">エラー、「KeyId『\<key\>』による既存の資格情報の更新は許可されていません」</span><span class="sxs-lookup"><span data-stu-id="8149e-660">Error: "Updates to existing credential with KeyId '\<key\>' is not allowed"</span></span>
> <span data-ttu-id="8149e-661">KeyId「\<key\>」による既存の資格情報の更新は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="8149e-661">Update to existing credential with KeyId '\<key\>' is not allowed.</span></span>
> 
> <span data-ttu-id="8149e-662">New-AzureRmADSpCredential : KeyId '\<key\>' による既存の資格情報の更新は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="8149e-662">New-AzureRmADSpCredential : Update to existing credential with KeyId '\<key\>' is not allowed.</span></span>  
> <span data-ttu-id="8149e-663">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span><span class="sxs-lookup"><span data-stu-id="8149e-663">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span></span>  
>  <span data-ttu-id="8149e-664">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span><span class="sxs-lookup"><span data-stu-id="8149e-664">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span></span>  
>  <span data-ttu-id="8149e-665">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span><span class="sxs-lookup"><span data-stu-id="8149e-665">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span></span>  
>  <span data-ttu-id="8149e-666">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span><span class="sxs-lookup"><span data-stu-id="8149e-666">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
```

