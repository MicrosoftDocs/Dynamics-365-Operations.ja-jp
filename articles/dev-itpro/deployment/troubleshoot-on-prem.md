---
title: オンプレミス配置のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。
author: sarvanisathish
manager: AnnBe
ms.date: 05/30/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 2674b4c65d33369e0d4b96679c38bbffad3233fb
ms.sourcegitcommit: d1029dcf8d890278fb90abd9a96f70654586533b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/30/2019
ms.locfileid: "1614582"
---
# <a name="troubleshoot-on-premises-deployments"></a><span data-ttu-id="b9590-103">オンプレミス配置のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="b9590-103">Troubleshoot on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9590-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置のトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9590-104">This topic provides troubleshooting information for on-premises deployments of Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="access-service-fabric-explorer"></a><span data-ttu-id="b9590-105">Service Fabric Explorer へのアクセス</span><span class="sxs-lookup"><span data-stu-id="b9590-105">Access Service Fabric Explorer</span></span>

<span data-ttu-id="b9590-106">Service Fabric Explorer には、Web ブラウザーと既定のアドレス `https://sf.d365ffo.onprem.contoso.com:19080` を使ってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-106">You can access Service Fabric Explorer in a web browser by using the default address, `https://sf.d365ffo.onprem.contoso.com:19080`.</span></span>

<span data-ttu-id="b9590-107">アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b9590-107">To verify the address, note the value that was used in the "Create DNS zones and add A records" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="b9590-108">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-108">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#createdns)
- [<span data-ttu-id="b9590-109">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-109">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#createdns)

<span data-ttu-id="b9590-110">クライアント証明書が、サイトにアクセスするマシンの証明書、cert:\\CurrentUser\\My に含まれている場合のみ、サイトにアクセスできます</span><span class="sxs-lookup"><span data-stu-id="b9590-110">You can access the site only if the client certificate is in cert:\\CurrentUser\\My on the machine that you're accessing the site on.</span></span> <span data-ttu-id="b9590-111">(証明書マネージャーで、**証明書 - 現在のユーザー** \> **個人** \> **証明書**に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-111">(In Certificate Manger, go to **Certificates - Current User** \> **Personal** \> **Certificates**.) When you access the site, select the client certificate when you're prompted.</span></span>

## <a name="monitor-the-deployment"></a><span data-ttu-id="b9590-112">配置の監視</span><span class="sxs-lookup"><span data-stu-id="b9590-112">Monitor the deployment</span></span>

### <a name="identify-the-primary-orchestrator"></a><span data-ttu-id="b9590-113">プライマリ オーケストレータを識別します。</span><span class="sxs-lookup"><span data-stu-id="b9590-113">Identify the primary orchestrator</span></span>

<span data-ttu-id="b9590-114">Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスであるマシンを判別するには、**クラスター** \> **アプリケーション** \> **\<*対象のアプリケーションの例*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="b9590-114">To determine the machine that is the primary instance for stateful services such as a local agent, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **\<*intended application example*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

<span data-ttu-id="b9590-115">プライマリ ノードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-115">The primary node is shown.</span></span> <span data-ttu-id="b9590-116">ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-116">For stateless services or the remaining applications, you must check all the nodes.</span></span>

<span data-ttu-id="b9590-117">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="b9590-117">Note the following points:</span></span>

- <span data-ttu-id="b9590-118">OrchestrationService は、Finance and Operations の配置およびサービス アクションを調整します。</span><span class="sxs-lookup"><span data-stu-id="b9590-118">OrchestrationService orchestrates the deployment and servicing actions for Finance and Operations.</span></span>
- <span data-ttu-id="b9590-119">ArtifactsManager は、ファイルを Microsoft Azure クラウド ストレージからローカル エージェント ファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-119">ArtifactsManager downloads files from Microsoft Azure cloud storage to the local agent file share.</span></span> <span data-ttu-id="b9590-120">ファイルを必要な形式にも解凍します。</span><span class="sxs-lookup"><span data-stu-id="b9590-120">It also unzips the files into the required format.</span></span>

### <a name="review-the-orchestrator-event-logs"></a><span data-ttu-id="b9590-121">オーケストレータ イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="b9590-121">Review the orchestrator event logs</span></span>

<span data-ttu-id="b9590-122">イベント ビューアー内の プライマリ OrchestrationService オーケストレータ マシンから、 **アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent** と移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-122">From the primary OrchestrationService orchestrator machine, in Event Viewer, go to **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9590-123">完全なエラー メッセージを表示するには、 **詳細** タブを選択してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-123">To view the full error message, you must select the **Details** tab.</span></span>

<span data-ttu-id="b9590-124">次のモジュールがインストールされます:</span><span class="sxs-lookup"><span data-stu-id="b9590-124">The following modules must be installed:</span></span>

- <span data-ttu-id="b9590-125">共通</span><span class="sxs-lookup"><span data-stu-id="b9590-125">Common</span></span>
- <span data-ttu-id="b9590-126">ReportingServices</span><span class="sxs-lookup"><span data-stu-id="b9590-126">ReportingServices</span></span>
- <span data-ttu-id="b9590-127">AOS</span><span class="sxs-lookup"><span data-stu-id="b9590-127">AOS</span></span>
- <span data-ttu-id="b9590-128">FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="b9590-128">FinancialReporting</span></span>

<span data-ttu-id="b9590-129">次のコマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-129">The following commands must be run:</span></span>

- <span data-ttu-id="b9590-130">**セットアップ**</span><span class="sxs-lookup"><span data-stu-id="b9590-130">**Setup**</span></span>
- <span data-ttu-id="b9590-131">**Dvt** – このコマンドは配置検証テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-131">**Dvt** – This command runs a deployment verification test.</span></span>
- <span data-ttu-id="b9590-132">**Cleanup** – このコマンドは環境のサービスと削除に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-132">**Cleanup** – This command is used to service and delete an environment.</span></span>

<span data-ttu-id="b9590-133">次のフォルダには、追加の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9590-133">The following folders contain additional information:</span></span>

- <span data-ttu-id="b9590-134">AX-SetupModuleEvents</span><span class="sxs-lookup"><span data-stu-id="b9590-134">AX-SetupModuleEvents</span></span>
- <span data-ttu-id="b9590-135">AX-SetupInfrastructureEvents</span><span class="sxs-lookup"><span data-stu-id="b9590-135">AX-SetupInfrastructureEvents</span></span>
- <span data-ttu-id="b9590-136">AX-BridgeService</span><span class="sxs-lookup"><span data-stu-id="b9590-136">AX-BridgeService</span></span>

<span data-ttu-id="b9590-137">イベント ビューアーで Microsoft Dynamics エントリを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-137">To review Microsoft Dynamics entries in Event Viewer, follow these steps.</span></span>

1. <span data-ttu-id="b9590-138">イベント ビューアーで **カスタム ビュー** を右クリックして、**カスタム ビューの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-138">In Event Viewer, right-click **Custom Views**, and then select **Create Custom View**.</span></span>

    ![カスタム表示の作成](media/Create-Custom-View.png)

2. <span data-ttu-id="b9590-140">**イベント ログ** フィールドで **Dynamics** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-140">In the **Event logs** field, select **Dynamics**.</span></span>

    ![Dynamics の選択](media/Select-Dynamics.png)

> [!NOTE]
> <span data-ttu-id="b9590-142">また、**カスタム ビュー** で **管理イベント** も確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-142">Also look at **Administrative Events** in **Custom Views**.</span></span>

### <a name="service-fabric-explorer"></a><span data-ttu-id="b9590-143">Service Fabric Explorer</span><span class="sxs-lookup"><span data-stu-id="b9590-143">Service Fabric Explorer</span></span>

<span data-ttu-id="b9590-144">クラスタ、アプリケーション、およびノードの状態に注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-144">Note the state of the cluster, application, and nodes.</span></span> <span data-ttu-id="b9590-145">Service Fabric Explorer にアクセスする方法については、[Service Fabric Explorer にアクセスする](troubleshoot-on-prem.md#access-service-fabric-explorer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-145">For information about how to access Service Fabric Explorer, see [Access Service Fabric Explorer](troubleshoot-on-prem.md#access-service-fabric-explorer).</span></span>

#### <a name="error-partition-is-below-target-replica-or-instance-count"></a><span data-ttu-id="b9590-146">エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」</span><span class="sxs-lookup"><span data-stu-id="b9590-146">Error: "Partition is below target replica or instance count"</span></span>

<span data-ttu-id="b9590-147">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-147">You might receive the following error:</span></span>

> <span data-ttu-id="b9590-148">パーティションがターゲット レプリカまたはインスタンス数を下回っています</span><span class="sxs-lookup"><span data-stu-id="b9590-148">Partition is below target replica or instance count</span></span>

<span data-ttu-id="b9590-149">このエラーはルート エラーではありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-149">This error isn't a root error.</span></span> <span data-ttu-id="b9590-150">各ノードのステータスが準備できていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-150">It indicates that the status of each node isn't ready.</span></span> <span data-ttu-id="b9590-151">AXSFType (AOS) では、ステータスがまだ **InBuild** である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-151">For AXSFType (AOS), the status might still be **InBuild**.</span></span>

<span data-ttu-id="b9590-152">エラー メッセージに関連するコンピューターで、イベント ビューアーを使用して最新の活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-152">On the machines that are related to the error message, use Event Viewer to view the latest activity.</span></span>

#### <a name="axsftype"></a><span data-ttu-id="b9590-153">AXSFType</span><span class="sxs-lookup"><span data-stu-id="b9590-153">AXSFType</span></span>

<span data-ttu-id="b9590-154">AXSFType (AOS) に **InBuild** のステータスが表示される場合、DB Sync ステータスおよび Application Object Server (AOS) コンピューターからの他のイベントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-154">If a status of **InBuild** is shown for AXSFType (AOS), review the DB Sync status and other events from Application Object Server (AOS) machines.</span></span>

<span data-ttu-id="b9590-155">エラーを診断するには、イベント ビューアーを使用して次のイベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-155">To diagnose errors, use Event Viewer to review the following event logs:</span></span>

- <span data-ttu-id="b9590-156">アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DatabaseSynchronize</span><span class="sxs-lookup"><span data-stu-id="b9590-156">Applications and Services Logs \> Microsoft \> Dynamics \> AX-DatabaseSynchronize</span></span>
- <span data-ttu-id="b9590-157">カスタム ビュー \> 管理イベント</span><span class="sxs-lookup"><span data-stu-id="b9590-157">Custom Views \> Administrative Events</span></span>

#### <a name="error-extractinstallerservice-failed-to-extract-cusersdynusercontosoappdatalocaltemp1blssblhw0nfabricinstallerservicecodefabricclientdll"></a><span data-ttu-id="b9590-158">エラー: "'ExtractInstallerService は抽出に失敗しました' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</span><span class="sxs-lookup"><span data-stu-id="b9590-158">Error: "'ExtractInstallerService failed to extract' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</span></span>

<span data-ttu-id="b9590-159">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-159">You might receive the following error:</span></span>

> <span data-ttu-id="b9590-160">"ExtractInstallerService は抽出に失敗しました" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll。</span><span class="sxs-lookup"><span data-stu-id="b9590-160">"ExtractInstallerService failed to extract" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll.</span></span>

<span data-ttu-id="b9590-161">このエラーが発生した場合は [Azure Service Fabric](https://go.microsoft.com/fwlink/?LinkId=730690) の最新バージョンをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-161">If you receive this error, download the latest version of [Azure Service Fabric](https://go.microsoft.com/fwlink/?LinkId=730690).</span></span> <span data-ttu-id="b9590-162">エラー メッセージのユーザー名およびパスは、環境によって変化することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-162">Note that the user name and path in the error message vary, depending on your environment.</span></span>

#### <a name="service-fabric-logs"></a><span data-ttu-id="b9590-163">Service Fabric ログ</span><span class="sxs-lookup"><span data-stu-id="b9590-163">Service Fabric logs</span></span>

<span data-ttu-id="b9590-164">Service Fabric アプリケーションのさらなる詳細については、C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log のログ ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-164">You can find more details about Service Fabric applications in the log files at C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log.</span></span>

### <a name="lifecycle-services"></a><span data-ttu-id="b9590-165">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b9590-165">Lifecycle Services</span></span>

<span data-ttu-id="b9590-166">Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-166">Note the current deployment status for the environment in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="a-time-out-error-occurs-when-a-service-fabric-cluster-is-created"></a><span data-ttu-id="b9590-167">Service Fabric cluster の作成時にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="b9590-167">A time-out error occurs when a Service Fabric cluster is created</span></span>

<span data-ttu-id="b9590-168">該当するセットアップ トピックの "スタンドアロン Service Fabric Cluster のセットアップ" セクションおよび環境の配置トピックに記載されているように Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-168">Run Test-D365FOConfiguration.ps1 as noted in the "Set up a standalone Service Fabric cluster" section of the appropriate setup and deployment topic for your environment.</span></span> <span data-ttu-id="b9590-169">エラーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-169">Note any errors.</span></span>

- [<span data-ttu-id="b9590-170">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-170">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [<span data-ttu-id="b9590-171">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-171">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

<span data-ttu-id="b9590-172">これらの手順を必ず実行してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-172">Be sure to complete these steps:</span></span>

- <span data-ttu-id="b9590-173">すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-173">Verify that the Service Fabric Server client certificate exists in the LocalMachine store on all Service Fabric nodes.</span></span>
- <span data-ttu-id="b9590-174">Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-174">Verify that the Service Fabric Server certificate has the access control list (ACL) for Network Service on all Service Fabric nodes.</span></span>
- <span data-ttu-id="b9590-175">[環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) で記載されているウイルス対策の除外を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-175">Review the antivirus exclusions that are noted in [Environment setup](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="a-time-out-error-occurs-while-youre-waiting-for-installer-service-to-be-completed-for-machine-xxxx"></a><span data-ttu-id="b9590-176">インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="b9590-176">A time-out error occurs while you're waiting for Installer Service to be completed for machine x.x.x.x</span></span>

<span data-ttu-id="b9590-177">インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b9590-177">Only one node type is supported for each Internet Protocol (IP) address (that is, for each machine).</span></span> <span data-ttu-id="b9590-178">ノードが同じマシン上で再利用されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-178">Check whether the nodes are being reused on the same machine.</span></span> <span data-ttu-id="b9590-179">たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-179">For example, AOS and ORCH must not be on the same machine, and ConfigTemplate.xml must be correctly defined.</span></span>

## <a name="remove-a-specific-application"></a><span data-ttu-id="b9590-180">特定のアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="b9590-180">Remove a specific application</span></span>

<span data-ttu-id="b9590-181">配置の削除またはクリーンアップに LCS を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9590-181">We recommend that you use LCS to remove or clean up deployments.</span></span> <span data-ttu-id="b9590-182">ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-182">However, you can also use Service Fabric Explorer to remove an application as you require.</span></span>

<span data-ttu-id="b9590-183">Service Fabric エクスプローラーで、**アプリケーション ノード** \> **アプリケーション** \> **MonitoringAgentAppType-Agent** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-183">In Service Fabric Explorer, go to **Application node** \> **Applications** \> **MonitoringAgentAppType-Agent**.</span></span> <span data-ttu-id="b9590-184">**ファブリック:/エージェント監視** の横にある省略記号ボタン (**...**) を選択し、アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-184">Select the ellipsis button (**...**) next to **fabric:/Agent-Monitoring**, and delete the application.</span></span> <span data-ttu-id="b9590-185">アプリケーションの完全な名前を入力して、アプリケーションの削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-185">Enter the full name of the application to confirm the deletion of the application.</span></span>

<span data-ttu-id="b9590-186">また、省略記号ボタンの選択および**非引当タイプ**の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-186">You can also remove MonitoringAgentAppType-Agent by selecting the ellipsis button and then selecting **Unprovision Type**.</span></span> <span data-ttu-id="b9590-187">アプリケーションの削除を確認するために、正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9590-187">Enter the full name to confirm the removal of the application.</span></span>

## <a name="remove-all-applications-from-service-fabric"></a><span data-ttu-id="b9590-188">Service Fabric からすべてのアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="b9590-188">Remove all applications from Service Fabric</span></span>

<span data-ttu-id="b9590-189">次のスクリプトは、LocalAgent および LocalAgent の監視エージェントを除く、すべての Service Fabric アプリケーションを削除してプロビジョニング解除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-189">The following script removes and unprovisions all Service Fabric applications except LocalAgent and the monitoring agent for LocalAgent.</span></span> <span data-ttu-id="b9590-190">オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-190">You must run this script on an orchestrator virtual machine (VM).</span></span>

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

## <a name="remove-service-fabric"></a><span data-ttu-id="b9590-191">Service Fabric の削除</span><span class="sxs-lookup"><span data-stu-id="b9590-191">Remove Service Fabric</span></span>

<span data-ttu-id="b9590-192">Service Fabric クラスターを完全に削除するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-192">To completely remove the Service Fabric cluster, follow these steps.</span></span>

1. <span data-ttu-id="b9590-193">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-193">Run the following command.</span></span>

    ```powershell
    .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

2. <span data-ttu-id="b9590-194">エラーが発生した場合は、**CleanFabric.ps1**コマンドを使用して、クラスタ内の特定のノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-194">If an error occurs, remove a specific node on the cluster by using the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="b9590-195">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-195">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span>
3. <span data-ttu-id="b9590-196">既定の場所を使用している場合、**C:\\ProgramData\\SF** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-196">Remove the **C:\\ProgramData\\SF** folder, if you're using the default location.</span></span> <span data-ttu-id="b9590-197">それ以外の場合、指定したフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-197">Otherwise, remove the specified folder.</span></span>

    <span data-ttu-id="b9590-198">"アクセス拒否" エラーが発生した場合は、Microsoft Windows PowerShell を再起動するか、マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-198">If you receive an "Access denied" error, restart Microsoft Windows PowerShell or the machine.</span></span>

## <a name="clean-up-an-existing-environment-and-redeploy"></a><span data-ttu-id="b9590-199">既存環境のクリーンアップと再配置</span><span class="sxs-lookup"><span data-stu-id="b9590-199">Clean up an existing environment and redeploy</span></span>

<span data-ttu-id="b9590-200">既存の環境をクリーンアップして再配置するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-200">To clean up an existing environment and redeploy, follow these steps.</span></span>

1. <span data-ttu-id="b9590-201">LCS でプロジェクトを開き、**環境**セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-201">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span>

    <span data-ttu-id="b9590-202">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b9590-202">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="b9590-203">このプロセスは 1、2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="b9590-203">This process will take one to two minutes.</span></span>

2. <span data-ttu-id="b9590-204">LocalAgentCLI.exe を含むオーケストレーター マシンにアクセスし、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-204">Access the orchestrator machine that contains LocalAgentCLI.exe, and follow these steps:</span></span>

    1. <span data-ttu-id="b9590-205">ローカル エージェント クリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-205">Run the local agent cleanup.</span></span>

        ```powershell
        .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
        ```

    2. <span data-ttu-id="b9590-206">Service Fabric を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-206">Remove Service Fabric.</span></span>

        ```powershell
        .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
        ```

    3. <span data-ttu-id="b9590-207">ノードが失敗した場合、**CleanFabric.ps1** コマンドを実行してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-207">If any nodes fail, run the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="b9590-208">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-208">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span>
    4. <span data-ttu-id="b9590-209">すべての Service Fabric ノードの **C:\\ProgramData\\SF\\** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-209">Remove the **C:\\ProgramData\\SF\\** folder on all Service Fabric nodes.</span></span>

        <span data-ttu-id="b9590-210">"アクセス拒否" エラーが発生した場合は、マシンを再起動してからもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-210">If you receive an "Access denied" error, restart the machine, and try again.</span></span>

3. <span data-ttu-id="b9590-211">必要に応じて証明書を削除または更新します。</span><span class="sxs-lookup"><span data-stu-id="b9590-211">Remove or update certificates as required.</span></span>

    <span data-ttu-id="b9590-212">すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-212">Remove old certificates from all AOS, BI, ORCH, and DC nodes.</span></span>

    - <span data-ttu-id="b9590-213">証明書は、次の証明書ストアに存在します: Cert:\\CurrentUser\\My\\、Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root。</span><span class="sxs-lookup"><span data-stu-id="b9590-213">The certificates exist in the following certificate stores: Cert:\\CurrentUser\\My\\, Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root.</span></span>
    - <span data-ttu-id="b9590-214">Microsoft SQL Server の設定が変更される場合は、SQL Server 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-214">If the setup of Microsoft SQL Server will be modified, remove the SQL Server certificates.</span></span>
    - <span data-ttu-id="b9590-215">Active Directory フェデレーション サービス (AD FS) の設定が変更される場合は、AD FS 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-215">If the settings for Active Directory Federation Services (AD FS) will be modified, remove the AD FS certificate.</span></span>

4. <span data-ttu-id="b9590-216">必要に応じて、次の構成ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="b9590-216">Update the following configuration files as required:</span></span>

    - <span data-ttu-id="b9590-217">ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="b9590-217">ConfigTemplate.xml</span></span>
    - <span data-ttu-id="b9590-218">ClusterConfig.json</span><span class="sxs-lookup"><span data-stu-id="b9590-218">ClusterConfig.json</span></span>

    <span data-ttu-id="b9590-219">テンプレートのフィールドに正しく入力する方法については、ご使用の環境に適した設定と配置のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-219">For information about how to correctly fill in the fields in the templates, see the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="b9590-220">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-220">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md)
    - [<span data-ttu-id="b9590-221">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-221">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md)

5. <span data-ttu-id="b9590-222">LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。</span><span class="sxs-lookup"><span data-stu-id="b9590-222">In LCS, open the project, and update the LCS on-premises connector as required.</span></span>

    1. <span data-ttu-id="b9590-223">環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="b9590-223">Re-create the LCS on-premises connector for the environment, or edit the settings of an existing connector.</span></span>

        <span data-ttu-id="b9590-224">LCS の値を簡単にコピーするには、.\\Get-AgentConfiguration.ps1 script を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-224">To obtain easy-to-copy values for LCS, use the .\\Get-AgentConfiguration.ps1 script.</span></span>

    2. <span data-ttu-id="b9590-225">最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-225">Download the latest local agent configuration, localagent-config.json.</span></span>

6. <span data-ttu-id="b9590-226">環境に適したセットアップと展開のトピックで次の指示に従って、再度展開します。</span><span class="sxs-lookup"><span data-stu-id="b9590-226">Deploy again by following the instructions in the appropriate setup and deployment topic for the environment:</span></span>

    - [<span data-ttu-id="b9590-227">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-227">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md)
    - <span data-ttu-id="b9590-228">[プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md)。</span><span class="sxs-lookup"><span data-stu-id="b9590-228">[Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md).</span></span>

## <a name="find-the-local-agent-values-that-are-used"></a><span data-ttu-id="b9590-229">使用するローカル エージェント値の検索</span><span class="sxs-lookup"><span data-stu-id="b9590-229">Find the local agent values that are used</span></span>

<span data-ttu-id="b9590-230">Service Fabric Explorer でローカル エージェント値を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-230">You can find local agent values in Service Fabric Explorer.</span></span> <span data-ttu-id="b9590-231">**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent** に移動して **詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-231">Go to **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent**, and then select **Details**.</span></span>

<span data-ttu-id="b9590-232">または、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-232">Alternatively, run the following Windows PowerShell command.</span></span>

```powershell
.\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

## <a name="install-upgrade-or-uninstall-a-local-agent"></a><span data-ttu-id="b9590-233">ローカル エージェントのインストール、アップグレード、アンインストール</span><span class="sxs-lookup"><span data-stu-id="b9590-233">Install, upgrade, or uninstall a local agent</span></span>

<span data-ttu-id="b9590-234">ローカルエージェントを更新する方法については、 [ローカルエージェントを更新する](../lifecycle-services/update-local-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-234">For information about how to update the local agent, see [Update the local agent](../lifecycle-services/update-local-agent.md).</span></span>

<span data-ttu-id="b9590-235">また、以下のアップグレードおよびアンインストール コマンドを使用することができます:</span><span class="sxs-lookup"><span data-stu-id="b9590-235">You can also use the following upgrade and uninstallation commands:</span></span>

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> <span data-ttu-id="b9590-236">**クリーンアップ** コマンドはファイル共有に配置された一切のファイルを削除しません。</span><span class="sxs-lookup"><span data-stu-id="b9590-236">The **Cleanup** command doesn't remove any files that were put in the file share.</span></span> <span data-ttu-id="b9590-237">ファイル共有は再利用できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-237">The file share can be reused.</span></span>

## <a name="an-error-occurs-when-local-agent-services-are-started"></a><span data-ttu-id="b9590-238">ローカル エージェント サービスを開始される際にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="b9590-238">An error occurs when local agent services are started</span></span>

<span data-ttu-id="b9590-239">ローカル エージェント サービスが開始されると、次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-239">When local agent services are started, you might receive the following error:</span></span>

> <span data-ttu-id="b9590-240">ファイル、アセンブリ 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'、もしくはその依存関係の 1 つをロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9590-240">Could not load file or assembly 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span>

<span data-ttu-id="b9590-241">このエラーは厳密な名前検証が有効になっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b9590-241">This error means that strong name verification is turned on.</span></span> <span data-ttu-id="b9590-242">Configure-PreReqs.ps1 を使用して、この確認をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-242">You can turn off this verification by using Configure-PreReqs.ps1.</span></span> <span data-ttu-id="b9590-243">厳密な名前検証がもう有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-243">To validate that strong name verification is no longer turned on, run Test-D365FOConfiguration.ps1.</span></span>

## <a name="a-validation-in-progress-message-is-shown-for-several-minutes-in-lcs"></a><span data-ttu-id="b9590-244">「検証が進行中」のメッセージが LCS に数分表示</span><span class="sxs-lookup"><span data-stu-id="b9590-244">A "Validation in progress" message is shown for several minutes in LCS</span></span>

<span data-ttu-id="b9590-245">ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-245">Follow these steps to troubleshoot general issues with local agent validation.</span></span>

1. <span data-ttu-id="b9590-246">コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で **Configure-PreReqs.ps1** を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-246">Run **Configure-PreReqs.ps1** on all orchestrator machines to configure the machines correctly.</span></span>
2. <span data-ttu-id="b9590-247">Test-D365FOConfiguration.ps1 スクリプトがすべてのオーケストレータ マシンで通ることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-247">Verify that the Test-D365FOConfiguration.ps1 script passes on all the orchestrator machines.</span></span>
3. <span data-ttu-id="b9590-248">LocalAgentCLI.exe のインストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-248">Verify that the installation of LocalAgentCLI.exe is successfully completed.</span></span>
4. <span data-ttu-id="b9590-249">Service Fabric Explorer で、すべてのアプリケーションが正常であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-249">In Service Fabric Explorer, verify that all the applications are healthy.</span></span>
5. <span data-ttu-id="b9590-250">アプリケーションが正常でない場合は、障害が発生しているサービスのプライマリ ノードを探します。</span><span class="sxs-lookup"><span data-stu-id="b9590-250">If the applications aren't healthy, find the primary node for the service that is failing.</span></span> <span data-ttu-id="b9590-251">イベント ビューアーでは、次の場所でのイベントを検索します。</span><span class="sxs-lookup"><span data-stu-id="b9590-251">In Event Viewer, look for events in the following locations:</span></span>

    - <span data-ttu-id="b9590-252">カスタム ビュー \> 管理イベント</span><span class="sxs-lookup"><span data-stu-id="b9590-252">Custom Views \> Administrative Events</span></span>
    - <span data-ttu-id="b9590-253">アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-LocalAgent</span><span class="sxs-lookup"><span data-stu-id="b9590-253">Applications and Services Log \> Microsoft \> Dynamics \> AX-LocalAgent</span></span>

## <a name="local-agent-errors"></a><span data-ttu-id="b9590-254">ローカル エージェント エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-254">Local agent errors</span></span>

### <a name="issue"></a><span data-ttu-id="b9590-255">出庫</span><span class="sxs-lookup"><span data-stu-id="b9590-255">Issue</span></span>

<span data-ttu-id="b9590-256">**エラー:** 次のエラーが表示される場合があります:</span><span class="sxs-lookup"><span data-stu-id="b9590-256">**Error:** You might receive the following errors:</span></span>

> <span data-ttu-id="b9590-257">コマンドを処理できません</span><span class="sxs-lookup"><span data-stu-id="b9590-257">Unable to process commands</span></span>

> <span data-ttu-id="b9590-258">チャンネル情報を取得できません</span><span class="sxs-lookup"><span data-stu-id="b9590-258">Unable to get the channel information</span></span>

> <span data-ttu-id="b9590-259">ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b9590-259">RunAsync failed due to an unhandled exception causing the host process to crash: System.ArgumentNullException: Value cannot be null.</span></span> <span data-ttu-id="b9590-260">パラメーター名: 証明書</span><span class="sxs-lookup"><span data-stu-id="b9590-260">Parameter name: certificate</span></span>

<span data-ttu-id="b9590-261">**理由:** これらのエラーは OnPremLocalAgent 証明書に指定された証明書が有効でないか、またはテナントに対して正しく構成されていないために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b9590-261">**Reason:** These errors can occur because the certificate that is specified for the OnPremLocalAgent certificate either isn't valid or isn't correctly configured for the tenant.</span></span>

<span data-ttu-id="b9590-262">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-262">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="b9590-263">すべてのオーケストレータ ノードで **Test-D365FOConfiguration.ps1** を実行し、すべてのチェックに合格することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-263">Run **Test-D365FOConfiguration.ps1** on all orchestrator nodes to make sure that all checks pass.</span></span>
2. <span data-ttu-id="b9590-264">ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-264">Verify that the certificate that is specified in the local agent configuration is correct.</span></span>

    - <span data-ttu-id="b9590-265">LCS および ConfigTemplate.xml ファイルで指定する拇印に特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-265">Make sure that the thumbprint that you specify in LCS and in the ConfigTemplate.xml file has no special characters.</span></span>
    - <span data-ttu-id="b9590-266">証明書は、infrastructure\\ConfigTemplate.xml の次のセクションで指定されているものと同じ証明書である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-266">The certificate should be the same certificate that is specified in the following section in infrastructure\\ConfigTemplate.xml.</span></span>

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. <span data-ttu-id="b9590-267">LCS のローカル エージェント コンフィギュレーションで指定される同じ証明書が、環境に対する適切な設定および配置トピックの「テナント用 LCS 接続の構成」セクションで手順の完了に使用されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-267">Make sure that the same certificate that is specified in the local agent configuration in LCS was used to complete the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="b9590-268">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-268">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="b9590-269">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-269">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. <span data-ttu-id="b9590-270">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-270">Uninstall the local agent.</span></span>
5. <span data-ttu-id="b9590-271">ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-271">Specify the correct certificate in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="b9590-272">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-272">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="b9590-273">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-273">Error</span></span>

<span data-ttu-id="b9590-274">**エラー:** サービス中に "資産をダウンロードできません" というエラーが表示され、詳細に "パッケージに提供された資格情報が認識されません" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-274">**Error:** During servicing, you receive an "Unable to download asset" error, and the details state, "The credentials supplied to the package were not recognized."</span></span>

<span data-ttu-id="b9590-275">**理由:** ACL が証明書で正しく定義されていません。</span><span class="sxs-lookup"><span data-stu-id="b9590-275">**Reason:** The ACL wasn't correctly defined on certificates.</span></span>

<span data-ttu-id="b9590-276">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="b9590-276">**Steps:**</span></span>

<span data-ttu-id="b9590-277">オーケストレータ マシンのクライアント証明書から ACL が削除されたかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-277">Check whether ACL was removed from client certificate on orchestrator machines.</span></span> <span data-ttu-id="b9590-278">オーケストレータ マシンの .\Test-D365FOConfiguration.ps1 スクリプトを実行し、ACL を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-278">Run the .\Test-D365FOConfiguration.ps1 script on orchestrator machines, and verify the ACL.</span></span>

<span data-ttu-id="b9590-279">エラーを解決するには、.\Set-CertificateAcls.ps1 スクリプトを実行して ACL をリセットします。</span><span class="sxs-lookup"><span data-stu-id="b9590-279">To resolve the error, run the .\Set-CertificateAcls.ps1 script to reset the ACLs.</span></span> 

### <a name="error"></a><span data-ttu-id="b9590-280">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-280">Error</span></span>

<span data-ttu-id="b9590-281">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-281">**Error:**</span></span>

> <span data-ttu-id="b9590-282">パス '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' へアクセスすることは、拒否されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-282">Access to the path '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' is denied.</span></span>

<span data-ttu-id="b9590-283">**理由:** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。</span><span class="sxs-lookup"><span data-stu-id="b9590-283">**Reason:** The file share that is specified in the local agent configuration isn't valid.</span></span>

<span data-ttu-id="b9590-284">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-284">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="b9590-285">指定した共有が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-285">Verify that the specified share exists.</span></span>
2. <span data-ttu-id="b9590-286">ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-286">Verify that the local agent user has full permission on the share.</span></span> <span data-ttu-id="b9590-287">ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定されるドメイン ネーム システム (DNS) 名です。</span><span class="sxs-lookup"><span data-stu-id="b9590-287">The local agent user is the Domain Name System (DNS) name that is specified in the following section in ConfigTemplate.xml.</span></span>

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. <span data-ttu-id="b9590-288">適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-288">Make sure that the "Set up file storage" section of the appropriate setup and deployment topic for your environment is completed:</span></span>

    - [<span data-ttu-id="b9590-289">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-289">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
    - [<span data-ttu-id="b9590-290">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-290">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)

4. <span data-ttu-id="b9590-291">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-291">Uninstall the local agent.</span></span>
5. <span data-ttu-id="b9590-292">ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-292">Specify the correct file share in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="b9590-293">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-293">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="b9590-294">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-294">Error</span></span>

<span data-ttu-id="b9590-295">**エラー:** サービス操作を行うと次のエラーが表示されます:</span><span class="sxs-lookup"><span data-stu-id="b9590-295">**Error:** When you do a servicing operation, you receive the following error:</span></span>

> <span data-ttu-id="b9590-296">コマンドの抽出セットアップ フォルダーを取得できません</span><span class="sxs-lookup"><span data-stu-id="b9590-296">Unable to get extract setup folder for command</span></span>

<span data-ttu-id="b9590-297">**理由:** そのファイル共有は削除または変更されました。</span><span class="sxs-lookup"><span data-stu-id="b9590-297">**Reason:** The file share has been removed or changed.</span></span>

<span data-ttu-id="b9590-298">**手順:** ファイル共有の設定内容を確認するには、Microsoft SQL Server Management Studio を開いてオーケストレータ データベースで次のクエリを実行します:</span><span class="sxs-lookup"><span data-stu-id="b9590-298">**Steps:** To see what the file share is set to, open Microsoft SQL Server Management Studio, and run the following query on the orchestrator database:</span></span>

```
select * from OrchestratorCommandArtifact where CommandId = 'xxx'
```

### <a name="error"></a><span data-ttu-id="b9590-299">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-299">Error</span></span>

<span data-ttu-id="b9590-300">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-300">**Error:**</span></span>

> <span data-ttu-id="b9590-301">ユーザー 'D365\\svc-LocalAgent$' へのログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-301">Login failed for user 'D365\\svc-LocalAgent$'.</span></span> <span data-ttu-id="b9590-302">理由: 指定した名前に一致するログインが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9590-302">Reason: Could not find a login matching the name provided.</span></span> <span data-ttu-id="b9590-303">\[CLIENT: 10.0.2.23\]</span><span class="sxs-lookup"><span data-stu-id="b9590-303">\[CLIENT: 10.0.2.23\]</span></span>

<span data-ttu-id="b9590-304">**理由:** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="b9590-304">**Reason:** The local agent user can't connect to the orchestrator database.</span></span> <span data-ttu-id="b9590-305">ユーザーが削除され、Active Directory ドメイン サービス (AD DS) に再作成されているために、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-305">This issue can occur because users have been deleted and then re-created in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="b9590-306">したがって、ユーザーのセキュリティ識別子 (SID) が変更され、SQL Server インスタンスまたはデータベースのユーザーに与えられたアクセスは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="b9590-306">Therefore, the security identifier (SID) of the user has changed, and any access that was given to the user for the SQL Server instance or the database no longer works.</span></span>

<span data-ttu-id="b9590-307">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-307">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="b9590-308">SQL Server インスタンスで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-308">Run the following script on the SQL Server instance.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    <span data-ttu-id="b9590-309">このスクリプトは、空のデータベースがまだ存在していない場合に、空のオーケストレータ データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="b9590-309">This script creates an empty orchestrator database, if an empty database doesn't already exist.</span></span> <span data-ttu-id="b9590-310">ローカル エージェント ユーザーをデータベースに追加し、データベース\_アクセス許可の所有者に渡します。</span><span class="sxs-lookup"><span data-stu-id="b9590-310">It then adds the local agent user to the database and gives it db\_owner permission.</span></span>

    <span data-ttu-id="b9590-311">適切なアクセス許可が付与された後、アプリケーションは自動的に正常な状態になります。</span><span class="sxs-lookup"><span data-stu-id="b9590-311">After the correct permissions are provided, the application should automatically go to a healthy state.</span></span>

2. <span data-ttu-id="b9590-312">SQL Server インスタンスの完全修飾ドメイン名 (FQDN)、データベース名、ローカル エージェント ユーザーなどの設定が LCS で間違って提供された場合は、設定を変更し、ローカル エージェントを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-312">If any settings, such as the fully qualified domain name (FQDN) of the SQL Server instance, the database name, or the local agent user, were provided incorrectly in LCS, change the settings, and then reinstall the local agent.</span></span>

<span data-ttu-id="b9590-313">上記の手順でエラーが解決しない場合は、SQL Server インスタンスとデータベースからローカル エージェント ユーザーを手動で削除し、Initialize-Database スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-313">If the preceding steps don't resolve the error, manually remove the local agent user from the SQL Server instance and the database, and then rerun the Initialize-Database script.</span></span>

<span data-ttu-id="b9590-314">AD DS でユーザーを再作成する場合、SID が変更されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-314">If you re-create a user in AD DS, remember that the SID will change.</span></span> <span data-ttu-id="b9590-315">この場合、ユーザーの以前の SID を削除し、新しい SID を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-315">In this case, remove the previous SID for the user, and add a new SID.</span></span>

### <a name="error"></a><span data-ttu-id="b9590-316">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-316">Error</span></span>

<span data-ttu-id="b9590-317">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-317">**Error:**</span></span> 
> <span data-ttu-id="b9590-318">データベースを移行できません</span><span class="sxs-lookup"><span data-stu-id="b9590-318">Unable to migrate database</span></span>

<span data-ttu-id="b9590-319">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="b9590-319">**Steps:**</span></span>

- <span data-ttu-id="b9590-320">SQL Server リスナーへのアクセスがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-320">Verify that you have access to the SQL Server listener.</span></span>
- <span data-ttu-id="b9590-321">テストをしている場合は、最初からやり直して空のオーケストレータ データベースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-321">If you're doing testing, you can start over and use an empty orchestrator database.</span></span>

### <a name="issue"></a><span data-ttu-id="b9590-322">問題点</span><span class="sxs-lookup"><span data-stu-id="b9590-322">Issue</span></span>

<span data-ttu-id="b9590-323">[データベースを構成する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb) プロシージャを実行するときに SQL Server インスタンスが名前付きインスタンスの場合は、**-DatabaseServer \[FQDN/Instancename\]** パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-323">When you performing the [Configure the databases](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb) procedure, if the SQL Server instance is a named instance, use the **-DatabaseServer \[FQDN/Instancename\]** parameter.</span></span>

### <a name="issue"></a><span data-ttu-id="b9590-324">問題点</span><span class="sxs-lookup"><span data-stu-id="b9590-324">Issue</span></span>

<span data-ttu-id="b9590-325">ローカル エージェント ユーザーは、SQL Server インスタンスまたはデータベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="b9590-325">The local agent user can't connect to the SQL Server instance or the database.</span></span>

<span data-ttu-id="b9590-326">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-326">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="b9590-327">SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-327">Delete the svc-LocalAgent user from the SQL Server primary node databases, and then remove the login from both servers.</span></span>
2. <span data-ttu-id="b9590-328">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-328">Run the following scripts.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="b9590-329">これらのスクリプトは、**常時オン**に設定されているときは機能しません。</span><span class="sxs-lookup"><span data-stu-id="b9590-329">These scripts don't work when an **always-on** setup is used.</span></span> <span data-ttu-id="b9590-330">データベースは最初にプライマリ ノードに作成されてから複製される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-330">The database must first be created in the primary node and then replicated.</span></span>

### <a name="error"></a><span data-ttu-id="b9590-331">エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-331">Error</span></span>

<span data-ttu-id="b9590-332">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-332">**Error:**</span></span>

> <span data-ttu-id="b9590-333">RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-333">RunAsync failed due to an unhandled exception causing the host process to crash: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span></span><span data-ttu-id="b9590-334"> ---\> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'</span><span class="sxs-lookup"><span data-stu-id="b9590-334"> ---\> System.Net.WebException: The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'</span></span>

<span data-ttu-id="b9590-335">**理由:** ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。</span><span class="sxs-lookup"><span data-stu-id="b9590-335">**Reason:** The local agent machines can't connect to lcsapi.lcs.dynamics.com.</span></span> <span data-ttu-id="b9590-336">「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-336">Review the AX-BridgeService event log for "The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'."</span></span>

<span data-ttu-id="b9590-337">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-337">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="b9590-338">**psping lcsapi.lcs.dynamics.com:80** を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-338">Run **psping lcsapi.lcs.dynamics.com:80**.</span></span>
2. <span data-ttu-id="b9590-339">前述のコマンドから応答を受信しない場合は、組織の IT 部門に問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="b9590-339">If you don't receive a response from the preceding command, contact the IT department at your organization.</span></span> <span data-ttu-id="b9590-340">ファイアウォールが lcsapi へのアクセスをブロックしているか、もしくはプロキシの問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="b9590-340">Either the firewall is blocking access to lcsapi, or proxy issues are occurring.</span></span>

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

## <a name="restart-applications-such-as-aos"></a><span data-ttu-id="b9590-341">アプリケーション (AOS など) を再起動</span><span class="sxs-lookup"><span data-stu-id="b9590-341">Restart applications (such as AOS)</span></span>

<span data-ttu-id="b9590-342">Service Fabric で、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード**の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="b9590-342">In Service Fabric, expand **Nodes** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **Code Packages** \> **Code**.</span></span> <span data-ttu-id="b9590-343">省略記号ボタン (**...**) を選択し、**再起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-343">Select the ellipsis button (**...**), and then select **Restart**.</span></span> <span data-ttu-id="b9590-344">求められたらコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="b9590-344">When you're prompted, enter the code.</span></span>

## <a name="upgrade-service-fabric"></a><span data-ttu-id="b9590-345">Service Fabric を更新します。</span><span class="sxs-lookup"><span data-stu-id="b9590-345">Upgrade Service Fabric</span></span>

<span data-ttu-id="b9590-346">Service Fabric Explorer は次のようなメッセージを表示します:</span><span class="sxs-lookup"><span data-stu-id="b9590-346">Service Fabric Explorer will show a message that resembles the following message:</span></span>

> <span data-ttu-id="b9590-347">問題のあるイベント: SourceId=「System.UpgradeOrchestrationService」、プロパティ =「ClusterVersionSupport」、HealthState=「警告」、ConsiderWarningAsError=false。</span><span class="sxs-lookup"><span data-stu-id="b9590-347">Unhealthy event: SourceId='System.UpgradeOrchestrationService', Property='ClusterVersionSupport', HealthState='Warning', ConsiderWarningAsError=false.</span></span>
<span data-ttu-id="b9590-348">現在のクラスタ バージョン 6.1.467.9494 のサポートは、5/30/2018 12:00:00 AM に終了します。</span><span class="sxs-lookup"><span data-stu-id="b9590-348">The current cluster version 6.1.467.9494 support ends 5/30/2018 12:00:00 AM.</span></span> <span data-ttu-id="b9590-349">Get-ServiceFabricRegisteredClusterCodeVersion を使用して利用可能なアップグレードを表示し、Start-ServiceFabricClusterUpgrade を使用してアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-349">Please view available upgrades using Get-ServiceFabricRegisteredClusterCodeVersion and upgrade using Start-ServiceFabricClusterUpgrade.</span></span>

<span data-ttu-id="b9590-350">最小要件が 1 つの Microsoft SQL Server Reporting Services (SSRS) ノードと 1 つの Management Reporter ノードであるため、PreUpgradeSafetyCheck をスキップするパラメータを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-350">Because the minimum requirement is one Microsoft SQL Server Reporting Services (SSRS) node and one Management Reporter node, you must pass in a parameter to skip PreUpgradeSafetyCheck.</span></span>

<span data-ttu-id="b9590-351">Windows PowerShell で Service Fabric をアップグレードするにはこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-351">Follow these steps to upgrade Service Fabric in Windows PowerShell.</span></span>

1. <span data-ttu-id="b9590-352">Service Fabric Cluster に接続します。</span><span class="sxs-lookup"><span data-stu-id="b9590-352">Connect to the Service Fabric cluster.</span></span> <span data-ttu-id="b9590-353">次のコマンドで **123** をサーバー / スター拇印に置き換えて、適切な IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-353">In the following command, replace **123** with the server/star thumbprint, and use the appropriate IP address.</span></span>

    ```powershell
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

2. <span data-ttu-id="b9590-354">ダウンロードされた最新バージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="b9590-354">Get the latest version that was downloaded.</span></span>

    ```powershell
    Get-ServiceFabricRegisteredClusterCodeVersion
    ```

3. <span data-ttu-id="b9590-355">アップグレードを開始します。</span><span class="sxs-lookup"><span data-stu-id="b9590-355">Start the upgrade.</span></span> <span data-ttu-id="b9590-356">**-CodePackageVersion** には、最新バージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="b9590-356">For **-CodePackageVersion**, enter the latest version.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b9590-357">**-UpgradeReplicaSetCheckTimeout** は SSRS と Management Reporter の PreUpgradeSafetyCheck をスキップするために使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-357">**-UpgradeReplicaSetCheckTimeout** is used to skip PreUpgradeSafetyCheck for SSRS and Management Reporter.</span></span> <span data-ttu-id="b9590-358">詳細については、[Service Fabric サービスのアップグレードが動作しない](https://github.com/Azure/service-fabric-issues/issues/595) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-358">For more information, see [Service Fabric service upgrade not working](https://github.com/Azure/service-fabric-issues/issues/595).</span></span> <span data-ttu-id="b9590-359">**UpgradeDomainTimeoutSec 600 UpgradeTimeoutSec 1800** を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-359">You might also want to use **-UpgradeDomainTimeoutSec 600 -UpgradeTimeoutSec 1800**.</span></span> <span data-ttu-id="b9590-360">詳細については、[アプリケーション アップグレード パラメーター](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-360">For more information, see [Application upgrade parameters](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters).</span></span>

    ```powershell
    Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion 6.1.472.9494 -Monitored -FailureAction Rollback -UpgradeReplicaSetCheckTimeout 30
    ```

4. <span data-ttu-id="b9590-361">アップグレードの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="b9590-361">Get the upgrade status.</span></span>

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

<span data-ttu-id="b9590-362">詳細については、[アプリケーション アップグレードのトラブルシューティング](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-362">For more information, see [Troubleshoot application upgrades](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting).</span></span>

<span data-ttu-id="b9590-363">新しい Service Fabric リリースの時期については、[Azure Service Fabric チームのブログ](https://blogs.msdn.microsoft.com/azureservicefabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-363">To learn when a new Service Fabric release comes out, see the [Azure Service Fabric team blog](https://blogs.msdn.microsoft.com/azureservicefabric/).</span></span>

<span data-ttu-id="b9590-364">アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録して、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** を展開して再起動してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-364">If you receive a warning in Service Fabric Explorer after you upgrade, make a note of the node, and then restart by expanding **Nodes** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **Code Packages** \> **Code**.</span></span> <span data-ttu-id="b9590-365">省略記号ボタン (**...**) を選択し、**再起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-365">Select the ellipsis button (**...**), and then select **Restart**.</span></span>
 
## <a name="error-unable-to-load-dll-fabricclientdll"></a><span data-ttu-id="b9590-366">エラー、「DLL 'FabricClient.dll' を読み込むことができません」</span><span class="sxs-lookup"><span data-stu-id="b9590-366">Error: "Unable to load DLL 'FabricClient.dll'"</span></span>

<span data-ttu-id="b9590-367">"DLL 'FabricClient.dll' をロードできません" というエラーが表示された場合は、Windows PowerShellを 閉じて再起動してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-367">If you receive an error that states, "Unable to load DLL 'FabricClient.dll'," close and restart Windows PowerShell.</span></span> <span data-ttu-id="b9590-368">エラーが引き続き発生する場合は、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-368">If the error persists, restart the machine.</span></span>

## <a name="what-cluster-id-should-be-used-in-the-agent-configuration"></a><span data-ttu-id="b9590-369">エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="b9590-369">What cluster ID should be used in the agent configuration?</span></span>

<span data-ttu-id="b9590-370">クラスタ ID は、任意のグローバル一意識別子 (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="b9590-370">The cluster ID can be any globally unique identifier (GUID).</span></span> <span data-ttu-id="b9590-371">この GUID は、追跡目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-371">This GUID is used for tracking purposes.</span></span>

## <a name="encryption-errors"></a><span data-ttu-id="b9590-372">暗号化エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-372">Encryption errors</span></span>

<span data-ttu-id="b9590-373">暗号化エラーの例は "AXBootstrapperAppType"、"Bootstrapper"、"AXDiagnostics"、"RTGatewayAppType"、"ゲートウェイの潜在的なエラー関連"、 "Microsoft.D365.Gateways.ClusterGateway.exe" を含みます。</span><span class="sxs-lookup"><span data-stu-id="b9590-373">Some examples of encryption errors include "AXBootstrapperAppType," "Bootstrapper," "AXDiagnostics," "RTGatewayAppType," "Gateway potential failure related," and "Microsoft.D365.Gateways.ClusterGateway.exe."</span></span>

<span data-ttu-id="b9590-374">AOS アカウント パスワードを暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b9590-374">You might receive one of these errors if the data encipherment certificate that was used to encrypt the AOS account password wasn't installed on the machine.</span></span> <span data-ttu-id="b9590-375">この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-375">This certificate might be in the certificates (local computer), or the provider type might be incorrect.</span></span>

<span data-ttu-id="b9590-376">エラーを解決するには、credentials.json ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="b9590-376">To resolve the error, validate the credentials.json file.</span></span> <span data-ttu-id="b9590-377">次のコマンドを (AOS1 上で) 入力することにより、テキストが正しく復号化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-377">Verify that the text is correctly decrypted by entering the following command (on AOS1).</span></span>

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="b9590-378">このエラーも、**''** パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-378">This error can also occur if the **''** parameter isn't defined in the ApplicationManifest file.</span></span> <span data-ttu-id="b9590-379">イベント ビューアーで、このパラメータが定義されているどうかを確認するには、**カスタム ビュー** \> **管理イベント**の順に移動し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-379">To determine whether this parameter is defined, in Event Viewer, go to **Custom Views** \> **Administrative Events**, and verify the following information:</span></span>

- <span data-ttu-id="b9590-380">Credentials.json ファイルの資格情報の暗号化には、正しいレイアウト/構造があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-380">The encrypt credentials for the credentials.json file have the correct layout/structure.</span></span> <span data-ttu-id="b9590-381">詳細については、ご使用の環境に適した設定および配置のトピックの「資格情報の暗号化」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-381">For more information, see the "Encrypt credentials" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="b9590-382">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-382">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#encryptcred)
    - [<span data-ttu-id="b9590-383">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-383">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#encryptcred)

- <span data-ttu-id="b9590-384">決算引用符が線の終わりまたは次の線に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-384">A closing quotation mark appears at the end of the line or on the next line.</span></span>

<span data-ttu-id="b9590-385">イベント ビューアーの **カスタム ビュー** \> **管理イベント** で、**Microsoft-Service Fabric** ソース カテゴリのエラーに注意します。</span><span class="sxs-lookup"><span data-stu-id="b9590-385">In Event Viewer, under **Custom Views** \> **Administrative Events**, note any errors in the **Microsoft-Service Fabric** source category.</span></span>

## <a name="properties-to-create-a-dataencryption-certificate"></a><span data-ttu-id="b9590-386">DataEncryption 証明書を作成するためのプロパティ</span><span class="sxs-lookup"><span data-stu-id="b9590-386">Properties to create a DataEncryption certificate</span></span>

<span data-ttu-id="b9590-387">DataEncryption 証明書を作成するのにには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-387">Use the following properties to create the DataEncryption certificate:</span></span>

- <span data-ttu-id="b9590-388">**自己署名証明書** – このパラメータは、自己署名証明書を使用する場合にのみ有効にします。</span><span class="sxs-lookup"><span data-stu-id="b9590-388">**Is self-signed certificate** – Enable this parameter only when you're using self-signed certificates.</span></span>
- <span data-ttu-id="b9590-389">**証明書の目的** – この証明書のすべての目的を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b9590-389">**Certificate purposes** – Enable all purposes for this certificate.</span></span>
- <span data-ttu-id="b9590-390">**署名アルゴリズム** – **sha256RSA** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-390">**Signature algorithm** – Specify **sha256RSA**.</span></span>
- <span data-ttu-id="b9590-391">**署名ハッシュ アルゴリズム** – **sha256** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-391">**Signature hash algorithm** – Specify **sha256**.</span></span>
- <span data-ttu-id="b9590-392">**発行者** – 指定 **CN = DataEncryptionCertificate**。</span><span class="sxs-lookup"><span data-stu-id="b9590-392">**Issuer** – Specify **CN = DataEncryptionCertificate**.</span></span>
- <span data-ttu-id="b9590-393">**公開キー** – **RSA (2048 ビット)** を指定します。</span><span class="sxs-lookup"><span data-stu-id="b9590-393">**Public Key** – Specify **RSA (2048 bits)**.</span></span>
- <span data-ttu-id="b9590-394">**Thumbprint アルゴリズム** – **sha1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="b9590-394">**Thumbprint algorithm** – Specify **sha1**.</span></span>

> [!WARNING]
> <span data-ttu-id="b9590-395">実稼働環境では、自己署名証明書を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="b9590-395">Don't use self-signed certificates in production environments.</span></span> <span data-ttu-id="b9590-396">代わりに、証明書機関によって発行された証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-396">Instead, use certificates that are issued by certificate authorities.</span></span>

## <a name="the-certificate-and-private-key-that-should-be-used-for-decryption-cant-be-found-0x8009200c"></a><span data-ttu-id="b9590-397">暗号の解読に使用すべき証明書と秘密キーを見つけることができません (0x8009200C)</span><span class="sxs-lookup"><span data-stu-id="b9590-397">The certificate and private key that should be used for decryption can't be found (0x8009200C)</span></span>

<span data-ttu-id="b9590-398">証明書と ACL がない、または間違った拇印の入力がある場合は、特殊文字をチェックし、C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt で拇印を探します。</span><span class="sxs-lookup"><span data-stu-id="b9590-398">If you're missing a certificate and ACL, or if you have the wrong thumbprint entry, check for special characters, and look for thumbprints in C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt.</span></span>

<span data-ttu-id="b9590-399">次のコマンドを使用して暗号化されたテキストを検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-399">You can also validate the encrypted text by using the following command.</span></span>

```
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="b9590-400">「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-400">If you receive the message, "Cannot find the certificate and private key to use for decryption," verify the axdataenciphermentcert and svc-AXSF$ AXServiceUser ACLs.</span></span>

<span data-ttu-id="b9590-401">credentials.json ファイルが変更された場合は、LCS から環境を削除して再配置します。</span><span class="sxs-lookup"><span data-stu-id="b9590-401">If the credentials.json file has changed, delete and redeploy the environment from LCS.</span></span>

<span data-ttu-id="b9590-402">上記のソリューションのいずれも機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-402">If none of the preceding solutions work, follow these steps.</span></span>

1. <span data-ttu-id="b9590-403">ConfigTemplate.xml ファイルで指定されたドメイン名と Active Directory アカウント名が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-403">Verify that the domain name and Active Directory account names that are specified in the ConfigTemplate.xml file are correct.</span></span>
2. <span data-ttu-id="b9590-404">用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml ファイルで指定された拇印が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-404">Verify that the thumbprints that are specified in the ConfigTemplate.xml file are correct if the certificate wasn't generated by using the scripts that are provided.</span></span>
3. <span data-ttu-id="b9590-405">LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと拇印が一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-405">Verify that the certificate thumbprints that are specified in LCS are correct, and that they match the thumbprints that are specified in ConfigTemplate.xml.</span></span> <span data-ttu-id="b9590-406">特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-406">Make sure that there are no special characters.</span></span> <span data-ttu-id="b9590-407">**.\\Get-DeploymentSettings.ps1** を実行して、コピーしやすい方法で拇印を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-407">You can run **.\\Get-DeploymentSettings.ps1** to obtain the thumbprints in an easy-to-copy manner.</span></span>
4. <span data-ttu-id="b9590-408">証明書が自己生成されない場合、プロバイダー名が次の証明書タイプと一致することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-408">If the certificates aren't self-generated, make sure that the provider names match for the following certificate types:</span></span>

    - <span data-ttu-id="b9590-409">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span><span class="sxs-lookup"><span data-stu-id="b9590-409">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span></span>
    - <span data-ttu-id="b9590-410">**その他のすべての証明書タイプ:** Microsoft の拡張された RSA および AES 暗号化プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b9590-410">**All other certificate types:** Microsoft Enhanced RSA and AES Cryptographic Provider</span></span>

5. <span data-ttu-id="b9590-411">Set-CertificateAcls.ps1 および Test-D365FOConfiguration.ps1 スクリプトがすべての Service Fabric マシンで正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-411">Verify that the Set-CertificateAcls.ps1 and Test-D365FOConfiguration.ps1 scripts were successfully run on all Service Fabric machines.</span></span>
6. <span data-ttu-id="b9590-412">Credentials.json ファイルが存在し、エントリが適切な値に復号化されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-412">Verify that the credentials.json file exists, and that the entries are decrypted to correct values.</span></span>

    <span data-ttu-id="b9590-413">AOS マシンのいずれかで、データの暗号化証明書が正しいことを確認する次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-413">On one of the AOS machines, run the following command to verify that the data encryption certificate is correct.</span></span>

    ```powershell
    Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
    ```

7. <span data-ttu-id="b9590-414">いずれかの証明書を変更する必要がある場合、もしくは構成が正しくない場合は、次の手順を実行してください:</span><span class="sxs-lookup"><span data-stu-id="b9590-414">If any of the certificates must be changed, or if the configuration was incorrect, follow these steps:</span></span>

    1. <span data-ttu-id="b9590-415">**ConfigTemplate.xml** ファイルを編集して、正しい値が出るようにします。</span><span class="sxs-lookup"><span data-stu-id="b9590-415">Edit the **ConfigTemplate.xml** file so that it has the correct values.</span></span>
    2. <span data-ttu-id="b9590-416">すべてのセットアップ スクリプトと **Test-D365FOConfiguration** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-416">Run all the setup scripts and the **Test-D365FOConfiguration** script.</span></span>

8. <span data-ttu-id="b9590-417">LCS で環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="b9590-417">In LCS, reconfigure the environment.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="b9590-418">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="b9590-418">Management Reporter</span></span>

<span data-ttu-id="b9590-419">追加のログは、プロバイダーを登録することで実行できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-419">Additional logging can be done by registering providers.</span></span> <span data-ttu-id="b9590-420">[ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) を **プライマリ**オーケストレータ マシン にダウンロードし、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-420">Download [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) to the **primary** orchestrator machine, and then run the following commands.</span></span> <span data-ttu-id="b9590-421">プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorerで、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="b9590-421">To determine which machine is the primary instance, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9590-422">イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-422">If results in Event Viewer don't appear correct (for example, if words are truncated), get the latest manifest and .dll files.</span></span> <span data-ttu-id="b9590-423">最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-423">To get the latest manifest and .dll files, go to the WP folder in the agent file share.</span></span> <span data-ttu-id="b9590-424">この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。</span><span class="sxs-lookup"><span data-stu-id="b9590-424">This share was created in the "Set up file storage" section of the appropriate setup and deployment topic for your environment:</span></span>
> 
> - [<span data-ttu-id="b9590-425">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-425">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
> - [<span data-ttu-id="b9590-426">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-426">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)
> 
> <span data-ttu-id="b9590-427">**例:** \[*エージェント共有*\]\\wp\\\[*配置名*\]\\StandaloneSetup-...\\アプリ\\ ETWManifests</span><span class="sxs-lookup"><span data-stu-id="b9590-427">**Example:** \[*Agent Share*\]\\wp\\\[*Deployment name*\]\\StandaloneSetup-...\\Apps\\ETWManifests</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

<span data-ttu-id="b9590-428">プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-428">If you must unregister providers, use the following command.</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

<span data-ttu-id="b9590-429">プロバイダーが登録されると、新しい配置についての追加詳細は**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** でイベント ビューアーにログインされます。</span><span class="sxs-lookup"><span data-stu-id="b9590-429">After providers are registered, additional details about the new deployment are logged in Event Viewer, at **Applications and Services Logs** \> **Microsoft** \> **Dynamics**.</span></span> <span data-ttu-id="b9590-430">次のフォルダが表示されます:</span><span class="sxs-lookup"><span data-stu-id="b9590-430">The following folders will be shown:</span></span>

- <span data-ttu-id="b9590-431">MR-Logger</span><span class="sxs-lookup"><span data-stu-id="b9590-431">MR-Logger</span></span>
- <span data-ttu-id="b9590-432">MR-Sql</span><span class="sxs-lookup"><span data-stu-id="b9590-432">MR-Sql</span></span>

<span data-ttu-id="b9590-433">新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-433">To see the new folders, you must close and reopen Event Viewer.</span></span> <span data-ttu-id="b9590-434">追加の詳細を表示するには、もう一度環境を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-434">To see additional details, you must deploy an environment again.</span></span>

### <a name="an-error-occurs-while-addaxdatabasechangetracking-is-running"></a><span data-ttu-id="b9590-435">AddAXDatabaseChangeTracking の実行中に発生するエラー</span><span class="sxs-lookup"><span data-stu-id="b9590-435">An error occurs while AddAXDatabaseChangeTracking is running</span></span>

<span data-ttu-id="b9590-436">Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-436">If you receive an error while you run AddAXDatabaseChangeTracking at Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet), verify that the full path is correct.</span></span> <span data-ttu-id="b9590-437">フル パスの例は **ax.d365ffo.onprem.contoso.com** です。</span><span class="sxs-lookup"><span data-stu-id="b9590-437">An example of a full path is **ax.d365ffo.onprem.contoso.com**.</span></span>

<span data-ttu-id="b9590-438">スター証明書での問題が原因でエラーが発生する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="b9590-438">The error might also occur because of an issue with the star certificate.</span></span> <span data-ttu-id="b9590-439">たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-439">For example, the remote certificate CN=\*.d365ffo.onprem.contoso.com has a name that isn't valid or that doesn't match the host, ax.d365ffo.onprem.contoso.com.</span></span>

### <a name="run-the-initialize-database-script-and-validate-that-databases-have-correct-users"></a><span data-ttu-id="b9590-440">データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証</span><span class="sxs-lookup"><span data-stu-id="b9590-440">Run the initialize database script, and validate that databases have correct users</span></span>

<span data-ttu-id="b9590-441">AddAXDatabaseChangeTracking イベントのみを受け取った場合は、`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService` にアクセスし、Finance and Operations の MetadataService サービスにアクセスしてみてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-441">If you receive only the AddAXDatabaseChangeTracking event, try to reach the MetadataService service for Finance and Operations by going to `https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService`.</span></span>

<span data-ttu-id="b9590-442">次に、wif.config ファイルでサービスの証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-442">Next, check the certificates of the service in the wif.config file.</span></span> <span data-ttu-id="b9590-443">ファイルを検索するには、AOS マシンにサインインし、タスク マネージャーで **AxService.exe** を探してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-443">To find the file, sign in to one of the AOS machines, and then, in Task Manager, find **AxService.exe**.</span></span> <span data-ttu-id="b9590-444">TimeZonePatcherを右クリックし、 **ファイルの場所を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-444">Right-click, and select **Open file location**.</span></span> <span data-ttu-id="b9590-445">wif.config ファイルでは、3 つの拇印を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-445">In the wif.config file, you should see three thumbprints.</span></span> <span data-ttu-id="b9590-446">これらの拇印に関する次の要件に注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-446">Note the following requirements for these thumbprints:</span></span>

- <span data-ttu-id="b9590-447">これらは異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-447">They must be different.</span></span>
- <span data-ttu-id="b9590-448">これらは、この順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-448">They must be in this order:</span></span>

    1. <span data-ttu-id="b9590-449">Financialreportingの拇印</span><span class="sxs-lookup"><span data-stu-id="b9590-449">Financialreporting thumbprint</span></span>
    2. <span data-ttu-id="b9590-450">ReportingServiceの拇印</span><span class="sxs-lookup"><span data-stu-id="b9590-450">ReportingService thumbprint</span></span>
    3. <span data-ttu-id="b9590-451">SessionAuthenticationの拇印</span><span class="sxs-lookup"><span data-stu-id="b9590-451">SessionAuthentication thumbprint</span></span>

<span data-ttu-id="b9590-452">拇印がこれらの要件の両方を満たしていない場合は、正しい拇印を使用して LCS から再配置をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-452">If the thumbprints don't meet both these requirements, you must redeploy from LCS by using correct thumbprints.</span></span>

### <a name="the-remote-name-cant-be-resolved"></a><span data-ttu-id="b9590-453">リモート名を解決できません</span><span class="sxs-lookup"><span data-stu-id="b9590-453">The remote name can't be resolved</span></span>

<span data-ttu-id="b9590-454">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-454">**Error:**</span></span>

> <span data-ttu-id="b9590-455">リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` をリッスンしていたエンドポイントはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9590-455">The remote name could not be resolved: 'x.d365fo.onprem.contoso.com' / There was no endpoint listening at `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` that could accept the message.</span></span>

<span data-ttu-id="b9590-456">**理由:** この問題は、通常正しくないアドレスまたは SOAP アクションによって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="b9590-456">**Reason:** This issue is often caused by an incorrect address or SOAP action.</span></span>

<span data-ttu-id="b9590-457">**手順:** URL を手動で開き、アドレスにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-457">**Steps:** Verify that the address can be reached, by manually opening the URL.</span></span> <span data-ttu-id="b9590-458">詳細については、イベント ビューアーで [InnerException] のテキストが存在するかどうか確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-458">For more details, see the "InnerException" text in the Event Viewer, if it's present.</span></span>

### <a name="error-on-importdefaultreports"></a><span data-ttu-id="b9590-459">ImportDefaultReports のエラー</span><span class="sxs-lookup"><span data-stu-id="b9590-459">Error on ImportDefaultReports</span></span>

<span data-ttu-id="b9590-460">配置中に Management Reporter レポートがチェックアウトされると、配置処理は失敗します。</span><span class="sxs-lookup"><span data-stu-id="b9590-460">If Management Reporter reports are checked out during deployment, the deployment will fail.</span></span> <span data-ttu-id="b9590-461">レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の**選択**明細書を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-461">To see whether reports are checked out, run the following **select** statements on the FinancialReporting database.</span></span>

```
select checkedoutto, * from Reporting.ControlReport where checkedoutto is not null
select checkedoutto, * from Reporting.ControlRowMaster where checkedoutto is not null
select checkedoutto, * from Reporting.ControlColumnMaster where checkedoutto is not null
```

<span data-ttu-id="b9590-462">どのユーザーがオブジェクトをチェック アウトするかを知るには、次の**選択**ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-462">To learn which user has objects checked out, you can run the following **select** statement.</span></span>

```
select * from Reporting.SecurityUser where UserID = ''
```

<span data-ttu-id="b9590-463">この問題を手動で解決するには、以下のテーブルを次のコマンドを使用して更新し、 **checkedoutto** を **null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b9590-463">To resolve this issue manually, update the following tables, and set **checkedoutto** to **null** by using the following commands.</span></span>

```
update Reporting.ControlReport set checkedoutto = null where checkedoutto is not null
update Reporting.ControlRowMaster set checkedoutto = null where checkedoutto is not null
update Reporting.ControlColumnMaster set checkedoutto = null where checkedoutto is not null
```

## <a name="axdbadmin-cant-connect-to-the-database-server-sql-lscontosocom"></a><span data-ttu-id="b9590-464">axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。</span><span class="sxs-lookup"><span data-stu-id="b9590-464">axdbadmin can't connect to the database server SQL-LS.contoso.com</span></span>

<span data-ttu-id="b9590-465">**理由:** AXDB データベースに接続するためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-465">**Reason:** The user doesn't have permission to connect to the AXDB database.</span></span>

<span data-ttu-id="b9590-466">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="b9590-466">**Steps:**</span></span>

1. <span data-ttu-id="b9590-467">既に存在する場合は、データベースから axdbadmin ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-467">Remove the axdbadmin user from the database, if it already exists.</span></span>
2. <span data-ttu-id="b9590-468">**ConfigTemplate.xml** ファイルで、AXDB データベースに追加する必要があるユーザー名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-468">In the **ConfigTemplate.xml** file, specify the user name that must be added to the AXDB database.</span></span>

    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```

3. <span data-ttu-id="b9590-469">axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-469">Run the initialize database script again to add the axdbadmin user.</span></span>

## <a name="unable-to-resolve-the-xpath-value"></a><span data-ttu-id="b9590-470">xPath 値を解決することができません。</span><span class="sxs-lookup"><span data-stu-id="b9590-470">Unable to resolve the xPath value</span></span>

<span data-ttu-id="b9590-471">予想される動作では、次の **xPath** 値を解決することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9590-471">In the expected behavior, the following **xPath** value can't be resolved:</span></span> 

<span data-ttu-id="b9590-472">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span><span class="sxs-lookup"><span data-stu-id="b9590-472">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span></span>

<span data-ttu-id="b9590-473">したがって、 **xPath** の値が解決できないことは問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-473">Therefore, the fact that the **xPath** value can't be resolved isn't an issue.</span></span> <span data-ttu-id="b9590-474">**xPath** 値は、AOS ランタイム ユーザーの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="b9590-474">The **xPath** value looks for AOS runtime user information.</span></span> <span data-ttu-id="b9590-475">ただし、セキュリティが統合されているため、その情報は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-475">However, because of integrated security, that information isn't required.</span></span> <span data-ttu-id="b9590-476">別の理由でエラーを調査する必要がある場合は、 **xPath** の値を解決できないと通知されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-476">The fact that the **xPath** value can't be resolved is communicated in case the failure must be investigated for another reason.</span></span>

## <a name="ad-fs"></a><span data-ttu-id="b9590-477">AD FS</span><span class="sxs-lookup"><span data-stu-id="b9590-477">AD FS</span></span>

### <a name="the-sign-in-page-doesnt-redirect-you"></a><span data-ttu-id="b9590-478">サインイン ページにリダイレクトされません。</span><span class="sxs-lookup"><span data-stu-id="b9590-478">The sign-in page doesn't redirect you</span></span>

<span data-ttu-id="b9590-479">サインイン ページにはリダイレクトされない可能性がありますが、資格情報の確認を続行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-479">The sign-in page might not redirect you but continues to prompt for credentials.</span></span> <span data-ttu-id="b9590-480">また、リダイレクトの可能性がありますが、次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-480">Alternatively, you might be redirected but receive the following message:</span></span>

> <span data-ttu-id="b9590-481">エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-481">An error occurred.</span></span> <span data-ttu-id="b9590-482">詳細については、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-482">Contact your administrator for more information.</span></span>

<span data-ttu-id="b9590-483">そのような場合、問題を解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-483">In these cases, you can follow these steps to resolve the issue:</span></span>

- <span data-ttu-id="b9590-484">AD FS リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-484">Add the AD FS link to the list of trusted sites.</span></span>
- <span data-ttu-id="b9590-485">Dynamics 365 リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-485">Add the Dynamics 365 link to the list of trusted sites.</span></span>
- <span data-ttu-id="b9590-486">末尾にスラッシュ「/」を追加し、動作が変更されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-486">Add a trailing slash (/), and see whether the behavior changes.</span></span>

<span data-ttu-id="b9590-487">**ADFS** \> **アプリケーション グループ**の順に移動して、AD FS マネージャーを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-487">Verify the AD FS Manager by going to **ADFS** \> **Application groups**.</span></span> <span data-ttu-id="b9590-488">**Microsoft Dynamics 365 for Operations オンプレミス**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9590-488">Double-click **Microsoft Dynamics 365 for Operations on-premises**.</span></span> <span data-ttu-id="b9590-489">その後、**ネイティブ アプリケーション**で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9590-489">Then, under **Native application**, double-click **Microsoft Dynamics 365 for Operations on-premises - Native application**.</span></span>

<span data-ttu-id="b9590-490">**リダイレクト URI** 値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-490">Note the **Redirect URI** value.</span></span> <span data-ttu-id="b9590-491">Finance and Operations の DNS 前方参照ゾーンに一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-491">It should match the DNS forward lookup zone for Finance and Operations.</span></span>

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a><span data-ttu-id="b9590-492">エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」</span><span class="sxs-lookup"><span data-stu-id="b9590-492">Error: "Could not establish trust relationship for the SSL/TLS secure channel"</span></span>

<span data-ttu-id="b9590-493">「SSL/TLS のセキュリティで保護されているチャネルに対する信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="b9590-493">If you receive an error that states, "Could not establish trust relationship for the SSL/TLS secure channel," follow these steps.</span></span>

1. <span data-ttu-id="b9590-494">Service Fabric で、**クラスタ** \> **アプリケーション** \> **AXSFType** \> **fabric:/AXSF** の順に移動し、**詳細**タブでスクロールし、**Aad\_AADMetadataLocationFormat** および **Aad\_FederationMetadataLocation** の URL に注意します。</span><span class="sxs-lookup"><span data-stu-id="b9590-494">In Service Fabric, go to **Cluster** \> **Applications** \> **AXSFType** \> **fabric:/AXSF**, and then, on the **Details** tab, scroll down and note the URLs for **Aad\_AADMetadataLocationFormat** and **Aad\_FederationMetadataLocation**.</span></span>
2. <span data-ttu-id="b9590-495">AOS からそれらの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="b9590-495">Browse to those URLs from AOS.</span></span>
3. <span data-ttu-id="b9590-496">詳細については、AOS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-496">On the AOS machine, in Event Viewer, go to **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** for details.</span></span>
4. <span data-ttu-id="b9590-497">AD FS 証明書が信頼されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-497">Verify that the AD FS certificate is trusted:</span></span>

    1. <span data-ttu-id="b9590-498">AD FS 証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-498">Verify the AD FS certificate.</span></span> <span data-ttu-id="b9590-499">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-499">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management**.</span></span>
    2. <span data-ttu-id="b9590-500">**AD FS** \> **サービス** \> **証明書** を展開し、証明書を記録しておきます。</span><span class="sxs-lookup"><span data-stu-id="b9590-500">Expand **AD FS** \> **Service** \> **Certificates**, and make a note of the certificates.</span></span> <span data-ttu-id="b9590-501">たとえば、1 つの証明書は、dc1.contoso.com の場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-501">For example, one certificate might be dc1.contoso.com.</span></span>
    3. <span data-ttu-id="b9590-502">AOS マシンの、Microsoft 管理コンソール証明書スナップインで、**証明書 (ローカル コンピューター)** \> **信頼済ルート証明機関** \> **証明書**の順に移動し、AD FS 証明書が一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-502">On the AOS machine, in the Microsoft Management Console Certificates snap-in, go to **Certificates (Local Computer)** \> **Trusted Root Certification Authorities** \> **Certificates**, and verify that the AD FS certificate is listed.</span></span>

<span data-ttu-id="b9590-503">サイトが安全でないことを示すメッセージが表示された場合は、AD FS の Secure Sockets Layer (SSL) 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="b9590-503">If you receive a message that states that the site isn't secure, you haven't added your Secure Sockets Layer (SSL) certificate for AD FS to the Trusted Root Certification Authorities store.</span></span>

### <a name="you-cant-connect-to-the-remote-server-in-some-locations"></a><span data-ttu-id="b9590-504">一部の地域ではリモート サーバーに接続できません</span><span class="sxs-lookup"><span data-stu-id="b9590-504">You can't connect to the remote server in some locations</span></span>

<span data-ttu-id="b9590-505">次の場所でリモート サーバーに接続できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-505">You might not be able to connect to the remote server at the following places:</span></span>

- <span data-ttu-id="b9590-506">System.Net.HttpWebRequest.GetResponse()</span><span class="sxs-lookup"><span data-stu-id="b9590-506">System.Net.HttpWebRequest.GetResponse()</span></span>
- <span data-ttu-id="b9590-507">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span><span class="sxs-lookup"><span data-stu-id="b9590-507">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span></span>
- <span data-ttu-id="b9590-508">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span><span class="sxs-lookup"><span data-stu-id="b9590-508">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span></span>

<span data-ttu-id="b9590-509">この場合は、エラーの受信元である C: \\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\ ログ フォルダーに移動し、出力ファイルを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-509">In this case, go to the C:\\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\log folder where you receive the error, and note the out file.</span></span> <span data-ttu-id="b9590-510">out ファイルには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9590-510">The out file contains the following information:</span></span>

> <span data-ttu-id="b9590-511">System.Net.WebException: リモート サーバーに接続できません ---\></span><span class="sxs-lookup"><span data-stu-id="b9590-511">System.Net.WebException: Unable to connect to the remote server ---\></span></span>
>
> <span data-ttu-id="b9590-512">System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="b9590-512">System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond x.x.x.x:443</span></span>

<span data-ttu-id="b9590-513">Psping を使用してリモート サーバーに対する接続を試みることもできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-513">You can also use Psping to try to reach the remote server.</span></span> <span data-ttu-id="b9590-514">Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-514">For information about Psping, see [Psping](/sysinternals/downloads/psping).</span></span>

### <a name="redirect-sign-in-questions-and-issues"></a><span data-ttu-id="b9590-515">サインイン時の質問および問題をリダイレクト</span><span class="sxs-lookup"><span data-stu-id="b9590-515">Redirect sign-in questions and issues</span></span>

<span data-ttu-id="b9590-516">サインイン時に問題が発生した場合は、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-516">If you're having issues when you sign-in, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="b9590-517">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-517">Here is an example:</span></span>

- <span data-ttu-id="b9590-518">**プロビジョニング \_AdminPrincipalName**: `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="b9590-518">**Provisioning\_AdminPrincipalName**: `AXServiceUser@contoso.com`</span></span>
- <span data-ttu-id="b9590-519">**プロビジョニング\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="b9590-519">**Provisioning\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span></span>

<span data-ttu-id="b9590-520">値が有効でない場合は、処理を続行できず、LCS から再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-520">If the values aren't valid, you won't be able to proceed, and you must redeploy from LCS.</span></span>

<span data-ttu-id="b9590-521">Reset-DatabaseUsers.ps1 を使用した場合、変更内容を有効にする前に、Dynamics サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-521">If you used Reset-DatabaseUsers.ps1, you must restart the Dynamics Service before your changes take effect.</span></span> <span data-ttu-id="b9590-522">引き続きサインインの問題がある場合は、USERINFO テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** の値を記録してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-522">If you still have sign-in issues, in the USERINFO table, note the **NETWORKDOMAIN** and **NETWORKALIAS** values.</span></span> <span data-ttu-id="b9590-523">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-523">Here is an example:</span></span>

- <span data-ttu-id="b9590-524">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="b9590-524">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span></span>
- <span data-ttu-id="b9590-525">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="b9590-525">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span></span>
- <span data-ttu-id="b9590-526">**IDENTITYPROVIDER:** これは **NETWORKDOMAIN** の内容と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-526">**IDENTITYPROVIDER:** This should match the **NETWORKDOMAIN** value.</span></span>

<span data-ttu-id="b9590-527">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** \> **サービス**に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-527">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management** \> **Service**.</span></span> <span data-ttu-id="b9590-528">**フェデレーション サービス プロパティの保守と編集** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="b9590-528">Right-click **Service and Edit Federation Service Properties**.</span></span> <span data-ttu-id="b9590-529">**フェデレーション サービスの識別子** は **USERINFO.NETWORKDOMAIN** の値と一致している必要があり、URL に **https** が入っている必要があります (たとえば `https://DC1.contoso.com/adfs`)。</span><span class="sxs-lookup"><span data-stu-id="b9590-529">The **Federation Service identifier** value should match the **USERINFO.NETWORKDOMAIN** value, and it should have **https** in the URL (for example, `https://DC1.contoso.com/adfs`).</span></span>

<span data-ttu-id="b9590-530">AD FS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **AD FS** \> **管理者**に移動してエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-530">On the AD FS machine, in Event Viewer, go to **Applications and Services Logs** \> **AD FS** \> **Admin**, and make a note of any errors.</span></span>

### <a name="fiddler"></a><span data-ttu-id="b9590-531">Fiddler</span><span class="sxs-lookup"><span data-stu-id="b9590-531">Fiddler</span></span>

<span data-ttu-id="b9590-532">追加のデバッグには Fiddler を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-532">Fiddler can be used for additional debugging.</span></span> <span data-ttu-id="b9590-533">Fiddler について詳しい情報は、 [AD FS 2.0: Fiddler Web デバッガーを使って WS フェデレーション パッシブ サインインを分析する方法](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) と [別の AD FS クレーム プロバイダーからの AD FS トークンのクラッキング](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b9590-533">For in-depth information about Fiddler, see [AD FS 2.0: How to Use Fiddler Web Debugger to Analyze a WS-Federation Passive Sign-In](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) and [Cracking the AD FS Token from another AD FS Claims Provider](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/).</span></span>

<span data-ttu-id="b9590-534">以下のセクションでは、 Microsoft Dynamics に返される要求に対する重点的なデバッグの手順を示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-534">The following sections provide focused debugging steps for claims that are returned to Microsoft Dynamics.</span></span>

#### <a name="repocapture"></a><span data-ttu-id="b9590-535">リポジトリ/キャプチャ</span><span class="sxs-lookup"><span data-stu-id="b9590-535">Repo/capture</span></span>

1. <span data-ttu-id="b9590-536">Fiddler を起動し、 **ツール \> オプション \> HTTPS** から **HTTPS トラフィックの復号化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-536">Open Fiddler, go to **Tools \> Options \> HTTPS**, and select **Decrypt HTTPS traffic**.</span></span>
2. <span data-ttu-id="b9590-537">トラフィックのキャプチャを開始します (ショートカット キーは F12 キーです)。</span><span class="sxs-lookup"><span data-stu-id="b9590-537">Start to capture traffic (the shortcut key is F12).</span></span> <span data-ttu-id="b9590-538">ツールの左下を確認すると、該当のトラフィックがキャプチャされていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-538">You can verify that that traffic is being captured by looking at the lower left of the tool.</span></span>
3. <span data-ttu-id="b9590-539">Internet Explorer の InPrivate モード、またはChrome の Incognito モードを使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-539">Open an InPrivate instance of Internet Explorer or an Incognito instance of Chrome.</span></span>
4. <span data-ttu-id="b9590-540">Finance and Operations を開きます (例 `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`).</span><span class="sxs-lookup"><span data-stu-id="b9590-540">Open Finance and Operations (for example, `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`).</span></span>
5. <span data-ttu-id="b9590-541">USERINFO.NETWORKALIAS のアカウントとパスワードを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="b9590-541">Sign in by using the USERINFO.NETWORKALIAS account and password.</span></span>
6. <span data-ttu-id="b9590-542">ログイン後、Fiddler によるトラフィックのキャプチャを停止してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-542">After you're signed in, stop Fiddler from capturing traffic.</span></span>

#### <a name="analyze"></a><span data-ttu-id="b9590-543">分析</span><span class="sxs-lookup"><span data-stu-id="b9590-543">Analyze</span></span>

<span data-ttu-id="b9590-544">Fiddler の右側のウィンドウには、リクエストとレスポンスが上段と下段にに分割されていることを留意してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-544">In the right pane of Fiddler, notice that a horizontal divider separates the request from the response.</span></span> <span data-ttu-id="b9590-545">リクエストとレスポンスとでそれぞれ別個のフレームを取得するようなネットワーク トレースとは異なり、Fiddler はリクエストとレスポンスの両方を1 つのフレームで提供します。</span><span class="sxs-lookup"><span data-stu-id="b9590-545">Unlike a network trace, where you typically get one frame for a request and another frame for a response, Fiddler provides one frame that contains both the request and the response.</span></span>

1. <span data-ttu-id="b9590-546">Fiddlerを起動し、画面右上隅の **Inspectors** \> **Raw** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-546">In Fiddler, in the upper-right corner, select **Inspectors** \> **Raw**.</span></span>
2. <span data-ttu-id="b9590-547">右下隅の **Cookie** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-547">In the lower-right corner, select **Cookies**.</span></span>
3. <span data-ttu-id="b9590-548">**MSISAuth** を検索します。</span><span class="sxs-lookup"><span data-stu-id="b9590-548">Do a search for **MSISAuth**.</span></span>
4. <span data-ttu-id="b9590-549">AD FS をホストするには、結果が **200** 件ある行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-549">Select the row that has a result of **200** for the AD FS host.</span></span>
5. <span data-ttu-id="b9590-550">上記で選択した上の行のなかで、 **302** 件の結果がある行を探します。</span><span class="sxs-lookup"><span data-stu-id="b9590-550">Look above the row that you just selected to find a row that has a result of **302**.</span></span> <span data-ttu-id="b9590-551">確認した行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-551">Select the row.</span></span>

    <span data-ttu-id="b9590-552">AD FS URL、ホスト、ユーザー名、およびパスワードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-552">You should see the AD FS URL, host, user name, and password.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="b9590-553">プライバシー保護のため、状況に応じて個人を特定できる情報を削除してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-553">For privacy, you might have to scrub personally identifiable information.</span></span>

    ![個人情報](media/Scrub-PII.png)

6. <span data-ttu-id="b9590-555">次は、結果が **302** 件ある行を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-555">Select the next row that has a result of **302**.</span></span> <span data-ttu-id="b9590-556">URL が、 **.../namespaces/AXSF/** となっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-556">The URL should be **.../namespaces/AXSF/**.</span></span>
7. <span data-ttu-id="b9590-557">上記で選択した行に示されているコード行を探してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-557">Find the code line that is shown on that row.</span></span> 

    ![コード行](media/Note-the-code.png)

8. <span data-ttu-id="b9590-559">等号 (=) の後に表示されているコード値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="b9590-559">Copy the value of code line after the equal sign (=).</span></span>
9. <span data-ttu-id="b9590-560"><https://www.base64decode.org/> に移動し、上記でコピーしたコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b9590-560">Go to <https://www.base64decode.org/>, and paste the code that you just copied.</span></span>
9. <span data-ttu-id="b9590-561">**Source charset** フィールドで、 **ASCII** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-561">In the **Source charset** field, select **ASCII**.</span></span>
10. <span data-ttu-id="b9590-562">**Decode** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-562">Select **Decode**.</span></span>
11. <span data-ttu-id="b9590-563">表示された結果をコピーし、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-563">Copy the results, and follow these steps:</span></span>

    - <span data-ttu-id="b9590-564">**upn** の値が、ユーザー名と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-564">Make sure that the **upn** value matches the user name.</span></span>
    - <span data-ttu-id="b9590-565">**unique_name** の値がテストで使用している Active Directoryユーザー名であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-565">Make sure that the **unique_name** value is the Active Directory user that is being tested.</span></span>
    - <span data-ttu-id="b9590-566">**Active Directory ユーザーとコンピューター** \> **ドメイン** \> **ユーザー** に移動し、テスト中のユーザーが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-566">Go to **Active Directory Users and Computers** \> **domain** \> **Users**, and make sure that this user is being tested.</span></span>

## <a name="sign-in-issues"></a><span data-ttu-id="b9590-567">サインインの問題</span><span class="sxs-lookup"><span data-stu-id="b9590-567">Sign-in issues</span></span>

<span data-ttu-id="b9590-568">サインインに関する問題が発生した場合には、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-568">If you or other users experience sign-in issues, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="b9590-569">値が有効な場合は、プライマリ SQL Server マシンで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-569">If the values are valid, run the following command on the primary SQL Server machine.</span></span>

```powershell
.\Reset-DatabaseUsers.ps1
```

<span data-ttu-id="b9590-570">タスク マネージャーの各 AOS マシンで、**AXService.exe** を選択し、**タスクの終了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-570">On each AOS machine, in Task Manager, select **AXService.exe**, and then select **End task**.</span></span>

<span data-ttu-id="b9590-571">ユーザーがリセットされたことを確認するには、AXDB SQL databaseで次の **select** 文を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-571">To verify that a user has been reset, run the following **select** query in the AXDB SQL database.</span></span>

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> <span data-ttu-id="b9590-572">Azure Active Directory (Azure AD) 環境 (オンライン環境) では、SID はネットワーク エイリアスおよびネットワーク ドメインのハッシュの役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="b9590-572">In an Azure Active Directory (Azure AD) environment (that is, an online environment), the SID is a hash of a network alias and a network domain.</span></span> <span data-ttu-id="b9590-573">AD DS 環境 (オンプレミス環境) では、SID はネットワーク エイリアスのハッシュとして機能し、プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="b9590-573">In an AD DS environment (that is, an on-premises environment), the SID is a hash of a network alias and an identify provider.</span></span>

<span data-ttu-id="b9590-574">場合によっては、引き続きサインインができず、次のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-574">In some cases, you still might not be able to sign in, and you might receive the following error:</span></span>

> <span data-ttu-id="b9590-575">現在の資格情報でログインする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-575">You are not authorized to login with your current credentials.</span></span> <span data-ttu-id="b9590-576">AD FS マシンで、サーバー マネージャー > ツール > AD FS の管理 に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-576">You will be redirected to the login page in a few seconds.</span></span>

<span data-ttu-id="b9590-577">このエラーが表示された場合は、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b9590-577">If this error occurs, follow these steps.</span></span>

1. <span data-ttu-id="b9590-578">AD FS マシンで、 **Server Manager** \> **Tools** \> **AD FS Management** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-578">On the AD FS machine, go to **Server Manager** \> **Tools** \> **AD FS Management**.</span></span>
2. <span data-ttu-id="b9590-579">**AD FS** を右クリックし、**フェデレーション サービス プロパティの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9590-579">Right-click **AD FS**, and then select **Edit Federation Service Properties**.</span></span>
3. <span data-ttu-id="b9590-580">**フェデレーション サービス 識別子** の値が、 **Userinfo.NetworkDomain** および **UserInfo.IdentityProvider** の値と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-580">Make sure that the **Federation Service Identifier** value matches the **Userinfo.NetworkDomain** and **UserInfo.IdentityProvider** values.</span></span>
4. <span data-ttu-id="b9590-581">AD FS マシンで、Windows PowerShell を開き、 **Get-AdfsProperties** を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-581">On the AD FS machine, open Windows PowerShell, and run **Get-AdfsProperties**.</span></span>
5. <span data-ttu-id="b9590-582">**IdTokenIssuer** の値が、手順3の **フェデレーション サービス 識別子** の値、および **Provisioning_AdminIdentityProvider** の値と一致していることを確認してください。 (これは **fabric:/AXSF Details** タブに表示されています。 **Service Fabric Explorer** \> **Cluster** \> **Applications** \> **AXSFType**)</span><span class="sxs-lookup"><span data-stu-id="b9590-582">Make sure that the **IdTokenIssuer** value matches the **Federation Service Identifier** value from step 3, and also the **Provisioning_AdminIdentityProvider** value on the **fabric:/AXSF Details** tab at **Service Fabric Explorer** \> **Cluster** \> **Applications** \> **AXSFType**.</span></span>
3. <span data-ttu-id="b9590-583">Service Fabric Explorer で、 **Provisioning\_AdminPrincipalName** 値と **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-583">In Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span>

<span data-ttu-id="b9590-584">上記の手順で問題が解決しない場合は、このトピックの 「 [AD FS](troubleshoot-on-prem.md#ad-fs) 」 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-584">If the preceding steps don't resolve the issue, see the [AD FS](troubleshoot-on-prem.md#ad-fs) section of this topic.</span></span>

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a><span data-ttu-id="b9590-585">System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)</span><span class="sxs-lookup"><span data-stu-id="b9590-585">System.Data.SqlClient.SqlException (0x80131904) and System.ComponentModel.Win32Exception (0x80004005)</span></span>

<span data-ttu-id="b9590-586">次のエラーのいずれかが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-586">You might receive one of the following errors:</span></span>

> <span data-ttu-id="b9590-587">System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、サインイン プロセス時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-587">System.Data.SqlClient.SqlException (0x80131904): A connection was successfully established with the server, but then an error occurred during the sign-in process.</span></span> <span data-ttu-id="b9590-588">(プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)</span><span class="sxs-lookup"><span data-stu-id="b9590-588">(provider: SSL Provider, error: 0 - The certificate chain was issued by an authority that is not trusted.)</span></span>

> <span data-ttu-id="b9590-589">System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました</span><span class="sxs-lookup"><span data-stu-id="b9590-589">System.ComponentModel.Win32Exception (0x80004005): The certificate chain was issued by an authority that is not trusted</span></span>

<span data-ttu-id="b9590-590">この場合、証明書がインストールされていないか、それらがしかるべきユーザーに結びついていません。</span><span class="sxs-lookup"><span data-stu-id="b9590-590">In this case, either the certificates haven't been installed, or they haven't given access to the correct users.</span></span> <span data-ttu-id="b9590-591">このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-591">To resolve this error, add the public key SQL Server certificate to all the Service Fabric nodes.</span></span>

## <a name="keyset-doesnt-exist"></a><span data-ttu-id="b9590-592">Keyset が存在しません</span><span class="sxs-lookup"><span data-stu-id="b9590-592">Keyset doesn't exist</span></span>

<span data-ttu-id="b9590-593">キーセットが存在しないことが判明した場合は、スクリプトがすべてのコンピューターで実行されなていなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="b9590-593">If you find that the keyset doesn't exist, scripts weren't run on all machines.</span></span> <span data-ttu-id="b9590-594">適切な設定の「VM の設定」セクション、および環境の配置トピックを確認し完了します。</span><span class="sxs-lookup"><span data-stu-id="b9590-594">Review and complete the "Set up VMs" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="b9590-595">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-595">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupvms)
- [<span data-ttu-id="b9590-596">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-596">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupvms)

<span data-ttu-id="b9590-597">各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b9590-597">Copy the scripts in each folder to the VMs that correspond to the folder name.</span></span>

<span data-ttu-id="b9590-598">また、正しいドメインを使うことを検証する .csv ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-598">Additionally, check the .csv file to verify that the correct domain is used.</span></span>

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a><span data-ttu-id="b9590-599">エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」</span><span class="sxs-lookup"><span data-stu-id="b9590-599">Error: "RunAsync failed due to an unhandled FabricException causing replica to fault"</span></span>

<span data-ttu-id="b9590-600">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-600">You might receive the following error:</span></span>

> <span data-ttu-id="b9590-601">未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-601">RunAsync failed due to an unhandled FabricException causing replica to fault: System.Fabric.FabricException: The first Fabric upgrade must specify both the code and config versions.</span></span> <span data-ttu-id="b9590-602">要求された値: 0.0.0.0:</span><span class="sxs-lookup"><span data-stu-id="b9590-602">Requested value: 0.0.0.0:</span></span>

<span data-ttu-id="b9590-603">この場合、ClusterConfig.json ファイルで、 **diagnosticsStore** をネットワーク共有からローカル パスに変更します。</span><span class="sxs-lookup"><span data-stu-id="b9590-603">In this case, in the ClusterConfig.json file, change **diagnosticsStore** from a network share to a local path.</span></span> <span data-ttu-id="b9590-604">たとえば、**\\\\サーバー\\パス**を、規定値の **C:\\ProgramData\\SF\\DiagnosticsStore** に変更します。</span><span class="sxs-lookup"><span data-stu-id="b9590-604">For example, change **\\\\server\\path** to a default value of **C:\\ProgramData\\SF\\DiagnosticsStore**.</span></span>

## <a name="service-fabric-aos-node-error-during-build-the-execution-time-out-expired"></a><span data-ttu-id="b9590-605">ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ</span><span class="sxs-lookup"><span data-stu-id="b9590-605">Service Fabric AOS node error during build: The execution time-out expired</span></span>

<span data-ttu-id="b9590-606">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-606">**Error:**</span></span>

> <span data-ttu-id="b9590-607">操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。</span><span class="sxs-lookup"><span data-stu-id="b9590-607">The timeout period elapsed prior to completion of the operation or the server is not responding.</span></span>  
> <span data-ttu-id="b9590-608">明細書は終了しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-608">The statement has been terminated.</span></span>

<span data-ttu-id="b9590-609">一度に 1 つの AOS マシンのみ DB Sync を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-609">Only one AOS machine can run DB Sync at a time.</span></span> <span data-ttu-id="b9590-610">このエラーは無視しても問題ありません。 AOS VM のいずれかが DB Sync で実行されているため、他の VM が実行できないという警告が表示されたためです。</span><span class="sxs-lookup"><span data-stu-id="b9590-610">You can safely ignore this error, because it means that one of the AOS VMs is running DB Sync. Therefore, the other VMs produce a warning that they can't run it.</span></span> <span data-ttu-id="b9590-611">DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で**アプリケーションおよびサービスのログ** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-611">To verify that DB Sync is running, on the AOS VM that isn't producing warnings, in Event Viewer, go to **Applications and Services Log** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational**.</span></span>

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a><span data-ttu-id="b9590-612">エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」</span><span class="sxs-lookup"><span data-stu-id="b9590-612">Error: "RequireNonce is 'true' (default) but validationContext.Nonce is null"</span></span>

<span data-ttu-id="b9590-613">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-613">You might receive the following error:</span></span>

> <span data-ttu-id="b9590-614">「RequireNonce が True (既定) となっていますが、validationContext.Nonce は Null となっています」</span><span class="sxs-lookup"><span data-stu-id="b9590-614">RequireNonce is 'true' (default) but validationContext.Nonce is null</span></span>

<span data-ttu-id="b9590-615">このエラーは、クライアントにサインインした後も Internet Explorer で HTTP エラー 500 として表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-615">This error also appears as an HTTP error 500 in Internet Explorer after you sign in to the client.</span></span> <span data-ttu-id="b9590-616">Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。</span><span class="sxs-lookup"><span data-stu-id="b9590-616">The nonce that is issued can't be validated if Internet Explorer is in Enhanced Security Configuration.</span></span>

<span data-ttu-id="b9590-617">クライアントにサインインするには、サーバー マネージャーを介して Internet Explorer のセキュリティ強化設定を無効にします。</span><span class="sxs-lookup"><span data-stu-id="b9590-617">To sign in to the client, disable Enhanced Security Configuration for Internet Explorer via Server Manager.</span></span>

## <a name="error-invalid-algorithm-specified--cryptography"></a><span data-ttu-id="b9590-618">エラー、「無効なアルゴリズムが指定されている/暗号化」</span><span class="sxs-lookup"><span data-stu-id="b9590-618">Error: "Invalid algorithm specified / Cryptography"</span></span>

<span data-ttu-id="b9590-619">"Invalid algorithm specified / Cryptography" エラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-619">If you receive an "Invalid algorithm specified / Cryptography" error, you must use the Microsoft Enhanced RSA and AES Cryptographic Provider.</span></span> <span data-ttu-id="b9590-620">詳細については、証明書の要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-620">For more information, see the certificate requirements.</span></span> <span data-ttu-id="b9590-621">また、credentials.json ファイルの構造が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-621">Additionally, verify that the structure of the credentials.json file is correct.</span></span>

<span data-ttu-id="b9590-622">正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-622">If you must re-create the certificate by using the correct provider, follow these steps.</span></span>

1. <span data-ttu-id="b9590-623">正しいプロバイダーを使用して証明書を再度作成します。</span><span class="sxs-lookup"><span data-stu-id="b9590-623">Create the certificate again by using the correct provider.</span></span>
2. <span data-ttu-id="b9590-624">**ConfigTemplate.xml** ファイルの変更。</span><span class="sxs-lookup"><span data-stu-id="b9590-624">Change the **ConfigTemplate.xml** file.</span></span>
3. <span data-ttu-id="b9590-625">クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、**Test-D365FOConfiguration.ps1** スクリプトに合格するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-625">Run the infrastructure scripts on all machines in the cluster, and make sure that the **Test-D365FOConfiguration.ps1** script passes.</span></span>
4. <span data-ttu-id="b9590-626">LCS から環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="b9590-626">Reconfigure the environment from LCS.</span></span>

## <a name="an-unable-to-find-certificate-error-occurs-when-you-run-test-d365foconfigurationps1"></a><span data-ttu-id="b9590-627">Test-D365FOConfiguration.ps1 を実行した際、「証明書を検出できません」エラーが発生</span><span class="sxs-lookup"><span data-stu-id="b9590-627">An "Unable to find certificate" error occurs when you run Test-D365FOConfiguration.ps1</span></span>

<span data-ttu-id="b9590-628">Test-D365FOConfiguration.ps1 を実行時に 「証明書を検出できません」 というエラーが発生した場合は、証明書または拇印がその他複数の用途で併用されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-628">If you receive an "Unable to find certificate" error when you run Test-D365FOConfiguration.ps1, check whether certificates or thumbprints are being combined for multiple purposes.</span></span> <span data-ttu-id="b9590-629">たとえば、クライアントと SessionAuthentication の証明書が併用されてされる場合、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b9590-629">For example, you will receive this error if the client certificate and the SessionAuthentication certificate are combined.</span></span> <span data-ttu-id="b9590-630">証明書を結合しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9590-630">We recommend that you not combine certificates.</span></span> <span data-ttu-id="b9590-631">詳細については、 証明書の必要要件を参照し、 **domain.com\\user** versus **domain\\user** 内 (たとえば、NETBIOS 構造) のacl.csv ファイルを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-631">For more information, see the certificate requirements, and check the acl.csv file for **domain.com\\user** versus **domain\\user** (for example, NETBIOS structure).</span></span>

## <a name="the-client-and-server-cant-communicate-because-they-dont-have-a-common-algorithm"></a><span data-ttu-id="b9590-632">クライアントとサーバーは共通のアルゴリズムを持たないため通信できません</span><span class="sxs-lookup"><span data-stu-id="b9590-632">The client and server can't communicate because they don't have a common algorithm</span></span>

<span data-ttu-id="b9590-633">クライアントとサーバーが疎通できない場合は双方のアルゴリズムが異なることが原因です。作成した証明書が指定したプロバーダーを使用しているか確認をしてください。これについては"Plan and acquire your certificates" の項目で解説しています。ご利用の環境に応じた適切な設定と配置を行ってください。</span><span class="sxs-lookup"><span data-stu-id="b9590-633">If the client and server can't communicate because they don't have a common algorithm, verify that the certificates that are created use the specified provider, as explained in the "Plan and acquire your certificates" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="b9590-634">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-634">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#plancert)
- [<span data-ttu-id="b9590-635">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-635">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts"></a><span data-ttu-id="b9590-636">グループ管理サービス アカウント の一覧の検索</span><span class="sxs-lookup"><span data-stu-id="b9590-636">Find a list of group managed service accounts</span></span>

<span data-ttu-id="b9590-637">すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-637">To find a list of all groups and hosts, run the following command.</span></span>

```
Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword
```

## <a name="addcerttoserviceprincipal-script-fails-on-import-module"></a><span data-ttu-id="b9590-638">Import-Module での AddCertToServicePrincipal スクリプトの失敗</span><span class="sxs-lookup"><span data-stu-id="b9590-638">AddCertToServicePrincipal script fails on Import-Module</span></span>

<span data-ttu-id="b9590-639">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-639">**Error:**</span></span>

> <span data-ttu-id="b9590-640">Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9590-640">AddCertToServicePrincipal script failing on Import-Module : Could not load file or assembly 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span> <span data-ttu-id="b9590-641">厳密な名前の検証に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-641">Strong name validation failed.</span></span> <span data-ttu-id="b9590-642">(HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-642">(Exception from HRESULT: 0x8013141A) may have multiple versions of the same module installed.</span></span>

<span data-ttu-id="b9590-643">**ステップ:** 問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-643">**Steps:** To resolve this issue, follow these steps.</span></span>

1. <span data-ttu-id="b9590-644">Windows PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-644">Run the following command in Windows PowerShell.</span></span>

    ```powershell
    Uninstall-Module -Name AzureRM
    Install-Module AzureRM
    ```

2. <span data-ttu-id="b9590-645">Windows PowerShell ウィンドウを閉じて、スクリプトを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-645">Close the Windows PowerShell window, and try to run the script again.</span></span>

## <a name="reportingservicessetupexe-error"></a><span data-ttu-id="b9590-646">ReportingServicesSetup.exe エラー</span><span class="sxs-lookup"><span data-stu-id="b9590-646">ReportingServicesSetup.exe error</span></span>

<span data-ttu-id="b9590-647">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-647">**Error:**</span></span>

> <span data-ttu-id="b9590-648">ReportingServicesSetup.exe エラー: 0 : アプリケーション fabric:/ReportingService は10分後から OK ではありません。</span><span class="sxs-lookup"><span data-stu-id="b9590-648">ReportingServicesSetup.exe Error: 0 : Application fabric:/ReportingService is not OK after 10 minutes</span></span>  
> <span data-ttu-id="b9590-649">アプリケーション: ReportingServicesBootstrapper.exe</span><span class="sxs-lookup"><span data-stu-id="b9590-649">Application: ReportingServicesBootstrapper.exe</span></span>  
> <span data-ttu-id="b9590-650">フレームワーク バージョン: v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="b9590-650">Framework Version: v4.0.30319</span></span>  
> <span data-ttu-id="b9590-651">説明: プロセスは未処理の例外によって中止されました。</span><span class="sxs-lookup"><span data-stu-id="b9590-651">Description: The process was terminated due to an unhandled exception.</span></span>

<span data-ttu-id="b9590-652">**理由:** このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効にされていますが、有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="b9590-652">**Reason:** If you receive this error, strong name validation is enabled in the Reporting server, but it should not be enabled.</span></span>

<span data-ttu-id="b9590-653">**ステップ:** 問題を解決するには、レポート サーバー マシンで **config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-653">**Steps:** To resolve this issue, run the **config-PreReq** script on the Reporting server machine.</span></span>

## <a name="the-requested-operation-requires-elevation"></a><span data-ttu-id="b9590-654">要求された操作には、昇格が必要です</span><span class="sxs-lookup"><span data-stu-id="b9590-654">The requested operation requires elevation</span></span>

<span data-ttu-id="b9590-655">AOS ユーザーはローカル管理者グループに属しておらず、ユーザー アカウント コントロール (UAC) が正しく無効化されていないために、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="b9590-655">This issue occurs because AOS users aren't in the local administrator group, and User Account Control (UAC) hasn't been disabled correctly.</span></span> <span data-ttu-id="b9590-656">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-656">To resolve the issue, follow these steps.</span></span>

1. <span data-ttu-id="b9590-657">環境の適切な設定および配置トピックの「VMs とドメインを結合」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-657">Add AOS users as local admins, as described in the "Join VMs to the domain" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="b9590-658">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-658">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#joindomain)
    - [<span data-ttu-id="b9590-659">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-659">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#joindomain)

2. <span data-ttu-id="b9590-660">すべての AOS コンピューターで、**Config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-660">Run the **Config-PreReq** script on all the AOS machines.</span></span>
3. <span data-ttu-id="b9590-661">**テスト構成**スクリプトがパスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-661">Make sure that the **Test-Configuration** script passes.</span></span>
4. <span data-ttu-id="b9590-662">UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-662">If UAC was changed, you must restart the machine before the changes take effect.</span></span>

## <a name="files-in-use-errors"></a><span data-ttu-id="b9590-663">使用中ファイルのエラー</span><span class="sxs-lookup"><span data-stu-id="b9590-663">Files in use errors</span></span>

<span data-ttu-id="b9590-664">「ファイルは使用中です」のエラーが発生した場合は、Service Fabric に示されている例外ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9590-664">If these "Files in use" errors occur, set up the exclusion rules that Service Fabric advises.</span></span> <span data-ttu-id="b9590-665">詳細については、[環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-665">For information, see [Environment setup](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="apply-deployable-packages-during-deployment"></a><span data-ttu-id="b9590-666">配置中に配置可能パッケージを適用する</span><span class="sxs-lookup"><span data-stu-id="b9590-666">Apply deployable packages during deployment</span></span>

### <a name="package-deployment-fails-because-of-a-path-too-long-exception"></a><span data-ttu-id="b9590-667">「パスが長過ぎる」例外によってパッケージの展開が失敗する</span><span class="sxs-lookup"><span data-stu-id="b9590-667">Package deployment fails because of a "path too long" exception</span></span>

<span data-ttu-id="b9590-668">Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="b9590-668">Because of a 260-character limit in Microsoft Windows, deployment will fail if a package has a longer name, or if the on-premises share has the full FQDN path.</span></span> <span data-ttu-id="b9590-669">文字数の制限を超過した場合、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-669">If the character limit is exceeded, you receive the following error:</span></span>

> <span data-ttu-id="b9590-670">System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。</span><span class="sxs-lookup"><span data-stu-id="b9590-670">System.IO.PathTooLongException: The specified path, file name, or both are too long.</span></span> <span data-ttu-id="b9590-671">完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-671">The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters.</span></span> <span data-ttu-id="b9590-672">at System.IO.PathHelper.GetFullPathName</span><span class="sxs-lookup"><span data-stu-id="b9590-672">at System.IO.PathHelper.GetFullPathName</span></span>

<span data-ttu-id="b9590-673">この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-673">To work around this issue, shorten the package name, and then apply the package again.</span></span> <span data-ttu-id="b9590-674">または、オンプレミス資産の共有パス全体の長さを短くしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-674">Alternatively, shorten the overall length of the share path for the on-premises assets.</span></span>

### <a name="package-deployment-fails-because-of-a-serialization-error"></a><span data-ttu-id="b9590-675">シリアル化エラーが原因でパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="b9590-675">Package deployment fails because of a serialization error</span></span>

<span data-ttu-id="b9590-676">パッケージ配置中、次のエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-676">During package deployment, you might receive the following error:</span></span>

> <span data-ttu-id="b9590-677">シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-677">Serialization version mismatch detect, make sure the runtime DLLs are in sync with the deployed metadata.</span></span> <span data-ttu-id="b9590-678">「XXX」ファイルのバージョン</span><span class="sxs-lookup"><span data-stu-id="b9590-678">Version of file 'XXX'.</span></span> <span data-ttu-id="b9590-679">DLL 「XXX」のバージョン</span><span class="sxs-lookup"><span data-stu-id="b9590-679">Version of DLL 'XXX'</span></span>

<span data-ttu-id="b9590-680">この場合は、パッケージが開発された環境のバージョンと、パッケージを配置する環境のバージョンが異なっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-680">In this case, the version of the environment where the package was developed might differ from the version of the environment that the package is being deployed in.</span></span>

<span data-ttu-id="b9590-681">この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。</span><span class="sxs-lookup"><span data-stu-id="b9590-681">To work around this issue, keep the development or build environments on the same version as the deployed on-premises environment.</span></span> <span data-ttu-id="b9590-682">パッケージのアップロード先にあるアセット ライブラリの**追加の詳細**セクションをクリックすることにより、パッケージ バージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-682">You can confirm the package version by looking in the **Additional details** section in the Asset library where the package is uploaded.</span></span> <span data-ttu-id="b9590-683">このエラーを修正するには、オンプレミス環境に配置されたバージョンと同じか、またはそれ以前のバージョンでパッケージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-683">To fix the error, generate the package on a version that is the same as or earlier than the version that is deployed in the on-premises environment.</span></span>

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a><span data-ttu-id="b9590-684">欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="b9590-684">Package deployment fails because of dependencies on missing modules</span></span>

<span data-ttu-id="b9590-685">依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次のようなメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-685">If you try to apply a package that is missing dependent modules, package application will fail, and you will receive a message that resembles the following message:</span></span>

> <span data-ttu-id="b9590-686">パッケージ \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="b9590-686">Package \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span></span>
>
> <span data-ttu-id="b9590-687">パッケージ \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="b9590-687">Package \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span></span>
>
> <span data-ttu-id="b9590-688">パッケージ \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span><span class="sxs-lookup"><span data-stu-id="b9590-688">Package \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span></span>

<span data-ttu-id="b9590-689">問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、**アプリケーションとサービス**を開き、**Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** の順で移動して、見つからないモジュールのあるイベントを表示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-689">To confirm the issue and find the missing dependencies, in Event Viewer, open **Application and Services**, and then go to **Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** to view events that have missing modules.</span></span> <span data-ttu-id="b9590-690">たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。</span><span class="sxs-lookup"><span data-stu-id="b9590-690">For example, one of the modules that is typically missing is ApplicationFoundationFormAdaptor.</span></span>

<span data-ttu-id="b9590-691">この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-691">To fix this issue and successfully apply the package, either add dependent modules, or remove modules that require dependent modules.</span></span> <span data-ttu-id="b9590-692">依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-692">To add dependent modules, you must include the dependencies when you build the package.</span></span> <span data-ttu-id="b9590-693">モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。</span><span class="sxs-lookup"><span data-stu-id="b9590-693">To remove modules, you can use ModelUtil.exe to delete a module.</span></span> <span data-ttu-id="b9590-694">詳細については、「[モデルのエクスポートとインポート](../dev-tools/models-export-import.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-694">For more information, see [Export and import a model](../dev-tools/models-export-import.md).</span></span>

### <a name="package-deployment-works-in-a-one-box-environment-but-not-in-the-sandbox-environment"></a><span data-ttu-id="b9590-695">パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない</span><span class="sxs-lookup"><span data-stu-id="b9590-695">Package deployment works in a one-box environment but not in the sandbox environment</span></span>

<span data-ttu-id="b9590-696">1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-696">A one-box environment might have all the modules installed, whereas the sandbox environment might have only the modules that are required in order to run your production environment.</span></span> <span data-ttu-id="b9590-697">開発環境で作成されたパッケージが、サンドボックス環境ではなく、ワン ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。</span><span class="sxs-lookup"><span data-stu-id="b9590-697">If the package that was built in the dev environment has a dependency on modules that are present in the one-box environment but not in the sandbox environment, the package won't work in the sandbox environment.</span></span>

<span data-ttu-id="b9590-698">この問題を解決するには、依存関係のあるすべてのモジュールを確認し、実稼動環境で不要なアダプターまたはその他のモジュールを使用しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-698">To resolve this issue, look at all the modules that you're dependent on, and make sure that you don't pull any farm adapter or any other module that isn't required in the production environment.</span></span> <span data-ttu-id="b9590-699">ビルド ボックスからパッケージを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9590-699">The best practice is to take the package from the build box.</span></span>

## <a name="an-error-occurs-when-you-sign-in-to-on-premises-environments"></a><span data-ttu-id="b9590-700">オンプレミス環境へのログイン時にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="b9590-700">An error occurs when you sign in to on-premises environments</span></span>

- <span data-ttu-id="b9590-701">**プラットフォーム更新 12:** **システム管理** \> **設定** \> **クライアント パフォーマンス オプション**に移動して、Skype 統合を無効にしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-701">**Platform update 12:** Turn off the Skype integration by going to **System administration** \> **Setup** \> **Client performance options**.</span></span> <span data-ttu-id="b9590-702">アプリに移動するとき、`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true` の例のように、**?debug=true** を URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-702">When you go to the app, append **?debug=true** to the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>
- <span data-ttu-id="b9590-703">**プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:** 確認されている問題は、 Skype の アプリケーション プログラミング インターフェイス (API) が、オンプレミス環境へのサインインする機能に影響を及ぼしているというものです。</span><span class="sxs-lookup"><span data-stu-id="b9590-703">**Platform update 8 and Platform update 11:** A known issue for the Skype application programming interface (API) affects the ability to sign in to on-premises environments.</span></span> <span data-ttu-id="b9590-704">Microsoftはこの問題の解決方法を調査しています。</span><span class="sxs-lookup"><span data-stu-id="b9590-704">Microsoft is investigating a resolution for this issue.</span></span> <span data-ttu-id="b9590-705">この問題を回避するために、次の例のように URL の末尾に **?debug=true** を追加できます。`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span><span class="sxs-lookup"><span data-stu-id="b9590-705">To work around this issue, you can add **?debug=true** to the end of the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>

## <a name="the-local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a><span data-ttu-id="b9590-706">ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します</span><span class="sxs-lookup"><span data-stu-id="b9590-706">The local agent stops working after the tenant for the project from LCS is changed</span></span>

<span data-ttu-id="b9590-707">更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-707">Follow these steps to configure the local agent with the updated tenant.</span></span>

1. <span data-ttu-id="b9590-708">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-708">Uninstall the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. <span data-ttu-id="b9590-709">ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-709">Follow the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="b9590-710">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="b9590-710">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="b9590-711">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="b9590-711">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

3. <span data-ttu-id="b9590-712">新しいテナントに新しい LCS コネクタを作成します。</span><span class="sxs-lookup"><span data-stu-id="b9590-712">Create a new LCS connector in the new tenant.</span></span>
4. <span data-ttu-id="b9590-713">**local-agent.config** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-713">Download the **local-agent.config** file.</span></span>
5. <span data-ttu-id="b9590-714">ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-714">Install the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="additional-deployments-for-example-two-sandbox-deployments-or-a-sandbox-and-production-deployment"></a><span data-ttu-id="b9590-715">追加の配置 (たとえば、2 つのサンド ボックス展開、またはサンド ボックスおよび生産の配置)</span><span class="sxs-lookup"><span data-stu-id="b9590-715">Additional deployments (for example, two sandbox deployments, or a sandbox and production deployment)</span></span>

<span data-ttu-id="b9590-716">追加の環境を展開すると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-716">You will receive the following error when you deploy an additional environment:</span></span>

> <span data-ttu-id="b9590-717">\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: アプリケーション グループ ID は、AD FS コンフィギュレーションで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-717">.\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: The application group identifier must be unique in AD FS configuration.</span></span>

<span data-ttu-id="b9590-718">配備手順の次のセクションをスキップまたは変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b9590-718">You can skip or modify the following sections in the deployment instructions.</span></span>

### <a name="plan-and-acquire-your-certificates-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdplancert-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdplancert"></a><span data-ttu-id="b9590-719">証明書の計画と取得 ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#plancert) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="b9590-719">Plan and acquire your certificates (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#plancert) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#plancert))</span></span>

- <span data-ttu-id="b9590-720">同一のオンプレミスのローカル エージェント証明書を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-720">You must use the same on-premises local agent certificate.</span></span>
- <span data-ttu-id="b9590-721">同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。</span><span class="sxs-lookup"><span data-stu-id="b9590-721">You can use same star certificates (AOS SSL and Service Fabric).</span></span>
- <span data-ttu-id="b9590-722">残りの証明書は既存の環境の証明書とは異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-722">The remaining certificates should probably differ from the certificates for the existing environment.</span></span>

### <a name="download-setup-scripts-from-lcs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mddownloadscripts-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mddownloadscripts"></a><span data-ttu-id="b9590-723">LCS からのセットアップ スクリプトのダウンロード ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#downloadscripts) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="b9590-723">Download setup scripts from LCS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#downloadscripts) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts))</span></span>

- <span data-ttu-id="b9590-724">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-724">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="set-up-a-standalone-service-fabric-cluster-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdsetupsfcluster-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdsetupsfcluster"></a><span data-ttu-id="b9590-725">([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#setupsfcluster) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster) に記載されているように) スタンドアロン Service Fabric クラスタを設定します</span><span class="sxs-lookup"><span data-stu-id="b9590-725">Set up a standalone Service Fabric cluster (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#setupsfcluster) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster))</span></span>

- <span data-ttu-id="b9590-726">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-726">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="configure-lcs-connectivity-for-the-tenant-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigurelcs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigurelcs"></a><span data-ttu-id="b9590-727">テナント用 LCS 接続 のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configurelcs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="b9590-727">Configure LCS connectivity for the tenant (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configurelcs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs))</span></span>

- <span data-ttu-id="b9590-728">テナントに対して、このタスクを 1 回のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-728">You must complete this task only one time for the tenant.</span></span>

### <a name="configure-ad-fs-as-documented-for-platform-update-12setup-deploy-on-premises-pu12mdconfigureadfs-or-platform-update-8-and-platform-update-11setup-deploy-on-premises-pu8-pu11mdconfigureadfs"></a><span data-ttu-id="b9590-729">AD FS のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configureadfs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="b9590-729">Configure AD FS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configureadfs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs))</span></span>

- <span data-ttu-id="b9590-730">すでに完了しているので、スクリプト 1、スクリプト 2、スクリプト 3 はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="b9590-730">You can skip scripts 1, 2, and 3, because they have already been done.</span></span>
- <span data-ttu-id="b9590-731">新しい **hosturl** 値を使用している場合でも、.\\Publish-ADFSApplicationGroup.ps1 スクリプトは失敗します。</span><span class="sxs-lookup"><span data-stu-id="b9590-731">The .\\Publish-ADFSApplicationGroup.ps1 script will fail even when the new **hosturl** value is used.</span></span> <span data-ttu-id="b9590-732">したがって、この手順を手動で完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-732">Therefore, you must manually complete these steps.</span></span>

    1. <span data-ttu-id="b9590-733">AD FS マネージャーで、**AD FS** \> **アプリケーション グループ**に移動し、**Microsoft Dynamics 365 for Operations オンプレミス**を開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-733">In AD FS Manager, go to **AD FS** \> **Application groups**, and open **Microsoft Dynamics 365 for Operations On-premises**.</span></span>
    2. <span data-ttu-id="b9590-734">**Microsoft Dynamics 365 for Operations  オンプレミス - ネイティブ アプリケーション** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-734">Open the **Microsoft Dynamics 365 for Operations On-premises - Native application** native application.</span></span> <span data-ttu-id="b9590-735">新しい環境 (DNS) の リダイレクト URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-735">Add the redirect URI of the new environment (DNS).</span></span>
    3. <span data-ttu-id="b9590-736">**Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 - ネイティブ アプリケーション** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-736">Open the **Microsoft Dynamics 365 for Operations On-premises - Financial Reporting - Native application** native application.</span></span> <span data-ttu-id="b9590-737">新しい環境 (DNS) の リダイレクト URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-737">Add the redirect URI of the new environment (DNS).</span></span>
    4. <span data-ttu-id="b9590-738">**Microsoft Dynamics 365 for Operations オンプレミス - Web AP I** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-738">Open the **Microsoft Dynamics 365 for Operations On-premises - Web API** Web API.</span></span> <span data-ttu-id="b9590-739">新しい環境 (DNS) のリダイレクト URI の 2 つのエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-739">Add the two entries of the redirect URI of the new environment (DNS).</span></span>
    5. <span data-ttu-id="b9590-740">**Microsoft Dynamics 365 for Operations オンプレミス - 財務諸表 Web API** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b9590-740">Open the **Microsoft Dynamics 365 for Operations On-premises - Financial Reporting Web API** Web API.</span></span> <span data-ttu-id="b9590-741">新しい環境 (DNS) の リダイレクト URI を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-741">Add the redirect URI of the new environment (DNS).</span></span>

## <a name="redeploy-ssrs-reports"></a><span data-ttu-id="b9590-742">SSRS レポートを再配置する</span><span class="sxs-lookup"><span data-stu-id="b9590-742">Redeploy SSRS reports</span></span>

<span data-ttu-id="b9590-743">SF.SyncLog のエントリを削除して、AOS マシンの 1 つを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-743">Delete the entry in SF.SyncLog, and then restart one of the AOS machines.</span></span> <span data-ttu-id="b9590-744">AOS コンピューターは DB 同期を再実行し、レポートを配置します。</span><span class="sxs-lookup"><span data-stu-id="b9590-744">The AOS machine will rerun DB Sync and then deploy reports.</span></span>

## <a name="add-axdbadmin-to-tempdb-after-a-sql-server-restart-via-a-stored-procedure"></a><span data-ttu-id="b9590-745">ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。</span><span class="sxs-lookup"><span data-stu-id="b9590-745">Add axdbadmin to tempdb after a SQL Server restart via a stored procedure</span></span>

<span data-ttu-id="b9590-746">SQL Server を再起動すると、tempdb データベースが再作成されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-746">When SQL Server is restarted, the tempdb database is re-created.</span></span> <span data-ttu-id="b9590-747">結果として、アクセス許可が不十分です。</span><span class="sxs-lookup"><span data-stu-id="b9590-747">Therefore, there will be missing permissions.</span></span> <span data-ttu-id="b9590-748">マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-748">Run the following script to create a stored procedure on the master database.</span></span>

```
\-----
USE [master]
GO
CREATE procedure [dbo].[CREATETEMPDBPERMISSIONS] as begin exec ('USE tempdb; declare @dbaccesscount int; select @dbaccesscount = COUNT(*) from master..syslogins where name = ''axdbadmin''; if (@dbaccesscount <> 0) exec sp_grantdbaccess ''axdbadmin''; ALTER USER [axdbadmin] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''axdbadmin''; EXEC sp_addrolemember N''db_datawriter'', N''axdbadmin''; EXEC sp_addrolemember N''db_ddladmin'', N''axdbadmin''; exec sp_grantdbaccess ''contoso\svc-AXSF$''; ALTER USER [contoso\svc-AXSF$] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_datawriter'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_ddladmin'', N''contoso\svc-AXSF$'';') end
GO
EXEC sp_procoption N'[dbo].[CREATETEMPDBPERMISSIONS]', 'startup', '1'
\-----
```

## <a name="error-updates-to-existing-credential-with-keyid-key-is-not-allowed"></a><span data-ttu-id="b9590-749">エラー、「KeyId『\<key\>』による既存の資格情報の更新は許可されていません」</span><span class="sxs-lookup"><span data-stu-id="b9590-749">Error: "Updates to existing credential with KeyId '\<key\>' is not allowed"</span></span>

<span data-ttu-id="b9590-750">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-750">You might receive the following error:</span></span>

> <span data-ttu-id="b9590-751">KeyId「\<key\>」を保持している既存の資格情報を更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9590-751">Updates to existing credential with KeyId '\<key\>' is not allowed</span></span>

<span data-ttu-id="b9590-752">この問題を解決するための手順は、オンプレミス プロジェクトのみをご利用しているか、オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用しているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b9590-752">The steps to resolve this issue depend on whether you have only an on-premises project, or whether you have both an online project and an on-premises project.</span></span>

### <a name="if-have-only-an-on-premises-project"></a><span data-ttu-id="b9590-753">場合設置プロジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="b9590-753">If have only an on-premises project</span></span>

<span data-ttu-id="b9590-754">オンプレミス プロジェクトのみの場合は、KeyId '\<key\>' を保持している既存の資格情報を更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9590-754">If have only an on-premises project, you can't update the existing credential with KeyId '\<key\>'.</span></span>

> <span data-ttu-id="b9590-755">New-AzureRmADSpCredential : KeyId '\<key\>' による既存の資格情報の更新は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="b9590-755">New-AzureRmADSpCredential : Update to existing credential with KeyId '\<key\>' is not allowed.</span></span>  
> <span data-ttu-id="b9590-756">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span><span class="sxs-lookup"><span data-stu-id="b9590-756">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span></span>  
> <span data-ttu-id="b9590-757">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span><span class="sxs-lookup"><span data-stu-id="b9590-757">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span></span>  
> <span data-ttu-id="b9590-758">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span><span class="sxs-lookup"><span data-stu-id="b9590-758">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span></span>  
> <span data-ttu-id="b9590-759">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span><span class="sxs-lookup"><span data-stu-id="b9590-759">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span></span>

<span data-ttu-id="b9590-760">この問題を解決するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-760">Run the following PowerShell command to resolve the issue.</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
```

### <a name="if-you-have-both-an-online-project-and-an-on-premises-project"></a><span data-ttu-id="b9590-761">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合</span><span class="sxs-lookup"><span data-stu-id="b9590-761">If you have both an online project and an on-premises project</span></span>

<span data-ttu-id="b9590-762">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合は、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b9590-762">If you have both an online project and an on-premises project, follow these steps.</span></span>

1. <span data-ttu-id="b9590-763">Microsoft .NET フレームワーク version 4.7.2 がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9590-763">Verify that the Microsoft .NET Framework version 4.7.2 is installed.</span></span>
2. <span data-ttu-id="b9590-764">以下のWindows PowerShell スクリプトを実行し、Azure PowerShell moduleをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9590-764">Run the following Windows PowerShell script to install the Azure PowerShell module.</span></span>

    ```powershell
    Install-Module -Name Az
    ```

3. <span data-ttu-id="b9590-765">以下のWindows PowerShellスクリプトを実行し、新規証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="b9590-765">Run the following Windows PowerShell script to upload the new certificate.</span></span>

    ```powershell
    Import-Module -Name Az.Accounts
    Import-Module -Name Az.Resources

    Connect-AzAccount

    $servicePrincipalName = "00000015-0000-0000-c000-000000000000";
    $CertificateThumbprint = <Thumbprint of Agent Certificate>
    $cert = Get-ChildItem -path Cert:\CurrentUser\my | Where-Object { $_.Thumbprint -eq $CertificateThumbprint }
    if (!$cert)
    {
        $cert = Get-ChildItem -path Cert:\LocalMachine\my | Where-Object { $_.Thumbprint -eq $CertificateThumbprint }
        if (!$cert)
        {
            throw "Unable to find the certificate in the Local machine or Current User store"
        }
    }

    $keyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
    $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName $servicePrincipalName
    if (!$servicePrincipal)
    {
        throw "Unable to find the service principal"
    }
    New-AzADSpCredential -ObjectId $servicePrincipal.Id -CertValue $keyValue -EndDate $cert.NotAfter -StartDate $cert.NotBefore
    Get-AzADSpCredential -ObjectId $servicePrincipal.Id
    ```

4. <span data-ttu-id="b9590-766">複数の証明書が存在する場合は、以下のコマンドを実行して重複する証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-766">Run the following command to remove the duplicate certificate, if more than one certificate exists.</span></span>

    ```powershell
    Remove-AzADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
    ```

## <a name="odbc-driver-17-is-required-for-platform-updates"></a><span data-ttu-id="b9590-767">プラットフォームの更新には ODBC ドライバー 17 が必要です</span><span class="sxs-lookup"><span data-stu-id="b9590-767">ODBC driver 17 is required for platform updates</span></span>

<span data-ttu-id="b9590-768">プラットフォーム バイナリを最新に更新するには、Open Database Connectivity ODBC ドライバー 17 を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9590-768">The latest platform binary update uses Open Database Connectivity (ODBC) driver 17.</span></span> <span data-ttu-id="b9590-769">このアップグレードでは、古いバージョンの ODBC ドライバーに関連する安定性の問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="b9590-769">This upgrade resolves stability issues that are linked to older ODBC drivers.</span></span> <span data-ttu-id="b9590-770">[追加の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) に関するドキュメントが更新されており、次の変更が記載されています。各AOSサーバーにはODBC ドライバー 17 がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-770">The [Setup perquisites](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) documentation has been updated to reflect the change in which ODBC driver 17 must be installed on each AOS server.</span></span> <span data-ttu-id="b9590-771">ODBC ドライバー 17 をインストールしない場合は、環境のメンテナンス処理中に DB 同期エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-771">If you don't install ODBC driver 17, you will receive DB Sync errors during servicing of the environment.</span></span>

<span data-ttu-id="b9590-772">エラーの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b9590-772">Here are some examples of errors:</span></span>

- <span data-ttu-id="b9590-773">Service Fabric で:</span><span class="sxs-lookup"><span data-stu-id="b9590-773">In Service Fabric:</span></span>

    > <span data-ttu-id="b9590-774">問題のあるイベント: SourceId=「System.RA」、プロパティ =「ReplicaOpenStatus」、HealthState=「警告」、ConsiderWarningAsError=false。</span><span class="sxs-lookup"><span data-stu-id="b9590-774">Unhealthy event: SourceId='System.RA', Property='ReplicaOpenStatus', HealthState='Warning', ConsiderWarningAsError=false.</span></span>  
    > <span data-ttu-id="b9590-775">レプリカで、AOS3 で開いているときに複数の障害が発生しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-775">Replica had multiple failures during open on AOS3.</span></span> <span data-ttu-id="b9590-776">API 呼び出し: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</span><span class="sxs-lookup"><span data-stu-id="b9590-776">API call: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</span></span>  
    > <span data-ttu-id="b9590-777">**DB の同期に失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="b9590-777">**DB sync failed.**</span></span>

- <span data-ttu-id="b9590-778">AOS コンピューターで:</span><span class="sxs-lookup"><span data-stu-id="b9590-778">On AOS machines:</span></span>

    - <span data-ttu-id="b9590-779">イベント ビューアー \> カスタム ビュー \> 管理イベント:</span><span class="sxs-lookup"><span data-stu-id="b9590-779">Event Viewer \> Custom Views \> Administrative Events:</span></span>

        > <span data-ttu-id="b9590-780">アプリケーション: Microsoft.Dynamics.AX.Deployment.Setup.exe フレームワーク バージョン: v4.0.30319 説明: プロセスは未処理の例外によって中止されました。</span><span class="sxs-lookup"><span data-stu-id="b9590-780">Application: Microsoft.Dynamics.AX.Deployment.Setup.exe Framework Version: v4.0.30319 Description: The process was terminated due to an unhandled exception.</span></span> <span data-ttu-id="b9590-781">例外情報: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String\[\])</span><span class="sxs-lookup"><span data-stu-id="b9590-781">Exception Info: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String\[\])</span></span>

    - <span data-ttu-id="b9590-782">C:\\ProgramData\\SF\\AOSx\\Fabric\\work\\Applications\\AXSFType\_Appxx\\log:</span><span class="sxs-lookup"><span data-stu-id="b9590-782">C:\\ProgramData\\SF\\AOSx\\Fabric\\work\\Applications\\AXSFType\_Appxx\\log:</span></span>

        > <span data-ttu-id="b9590-783">Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -metadatadir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</span><span class="sxs-lookup"><span data-stu-id="b9590-783">Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -metadatadir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</span></span>
        >
        > <span data-ttu-id="b9590-784">ハンドルされない例外: System.IO.FileNotFoundException: **ファイルまたはアセンブリ 'aoskernel.dll'、あるいはその依存関係のうちのいずれか 1 つを読み込めませんでした。指定されたモジュールが見つかりませんでした。**</span><span class="sxs-lookup"><span data-stu-id="b9590-784">Unhandled Exception: System.IO.FileNotFoundException: **Could not load file or assembly 'aoskernel.dll' or one of its dependencies. The specified module could not be found.**</span></span>
        > <span data-ttu-id="b9590-785">Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String\[\] args) にて</span><span class="sxs-lookup"><span data-stu-id="b9590-785">at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String\[\] args)</span></span>
        > 
        > <span data-ttu-id="b9590-786">**DB の同期に失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="b9590-786">**DB sync failed.**</span></span>

## <a name="a-no-subscription-found-in-the-context-error-occurs-when-you-run-add-certtoserviceprincipal"></a><span data-ttu-id="b9590-787">Add-CertToServicePrincipal を実行すると、"コンテキストにサブスクリプションが見つかりません" エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="b9590-787">A "No subscription found in the context" error occurs when you run Add-CertToServicePrincipal</span></span>

<span data-ttu-id="b9590-788">最新バージョンの Windows PowerShell が原因で "コンテキストにサブスクリプションが見つかりません" エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b9590-788">Recent versions of Windows PowerShell might cause a "No subscription found in the context" error.</span></span> <span data-ttu-id="b9590-789">この問題を解決するには、Windows PowerShellのバージョン5.7.0などの古いバージョンをインストールし、上書きしてください。</span><span class="sxs-lookup"><span data-stu-id="b9590-789">To resolve this issue, install and load an older version of Windows PowerShell, such as version 5.7.0.</span></span>

```powershell
# Install version 5.7.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 5.7.0

# Load version 5.7.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 5.7.0
```
## <a name="service-fabric-explorer-warnings-occur-after-you-restart-a-machine"></a><span data-ttu-id="b9590-790">コンピューターの再起動後に Service Fabric Explorer の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="b9590-790">Service Fabric Explorer warnings occur after you restart a machine</span></span>

<span data-ttu-id="b9590-791">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="b9590-791">**Error:**</span></span>

> <span data-ttu-id="b9590-792">エラー: event: SourceId='MonitoringAgentService', Property='ServiceState'.</span><span class="sxs-lookup"><span data-stu-id="b9590-792">Error event: SourceId='MonitoringAgentService', Property='ServiceState'.</span></span>  
> <span data-ttu-id="b9590-793">System.Management.Automation.RuntimeException: エラー: **渡された GUID は WMI データ プロバイダーにより有効と認識されませんでした。**</span><span class="sxs-lookup"><span data-stu-id="b9590-793">System.Management.Automation.RuntimeException: Error: **The GUID passed was not recognized as valid by a WMI data provider.**</span></span> <span data-ttu-id="b9590-794">(HRESULT からの例外: 0x80071068)。</span><span class="sxs-lookup"><span data-stu-id="b9590-794">(Exception from HRESULT: 0x80071068).</span></span> <span data-ttu-id="b9590-795">スタック トレース:</span><span class="sxs-lookup"><span data-stu-id="b9590-795">Stack trace:</span></span>

<span data-ttu-id="b9590-796">**手順:** この問題を解決するには、警告メッセージの原因であるアプリケーション パッケージを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b9590-796">**Steps:** To resolve this issue, restart the application package that generated the warning message.</span></span> <span data-ttu-id="b9590-797">詳しくは、 [アプリケーション(AOS など)を再起動してください](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/troubleshoot-on-prem#restart-applications-such-as-aos) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b9590-797">For more information, see [Restart applications (such as AOS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/troubleshoot-on-prem#restart-applications-such-as-aos).</span></span>

## <a name="the-internal-time-zone-version-number-that-is-stored-in-the-database-is-higher-than-the-version-that-is-supported-by-the-kernel-1312"></a><span data-ttu-id="b9590-798">データベースに格納されている内部タイム ゾーンのバージョン番号が、カーネル (13/12) でサポートされているバージョンよりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="b9590-798">The internal time zone version number that is stored in the database is higher than the version that is supported by the kernel (13/12)</span></span>

<span data-ttu-id="b9590-799">このデータベースの同期エラーにより、新しいビルド (プラットフォーム更新 15) があったデータベースの上に古いプラットフォーム ビルド (プラットフォーム更新 12) が配置されてしまう可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-799">This database synchronization error can cause an old platform build (Platform update 12) to be deployed on top of a database that had a newer build (Platform update 15).</span></span>

<span data-ttu-id="b9590-800">この問題を解決するには、 **SYSTIMEZONESVERSION** の値が重要になります。</span><span class="sxs-lookup"><span data-stu-id="b9590-800">To resolve this issue, note the **SYSTIMEZONESVERSION** value.</span></span>

```
select * from SQLSYSTEMVARIABLES where parm = 'SYSTIMEZONESVERSION'
```

<span data-ttu-id="b9590-801">エラー メッセージにて表示されたバージョンの値で [value] を更新します</span><span class="sxs-lookup"><span data-stu-id="b9590-801">Update the value to the version that was returned in the error message.</span></span>

```
update SQLSYSTEMVARIABLES set VALUE = 12 where parm = 'SYSTIMEZONESVERSION'
```

## <a name="printing-randomly-stops"></a><span data-ttu-id="b9590-802">印刷がランダムに停止する</span><span class="sxs-lookup"><span data-stu-id="b9590-802">Printing randomly stops</span></span>

<span data-ttu-id="b9590-803">AOS サーバーにインストールされているすべてのネットワーク プリンターが、AXService.EXE プロセスが実行されている Windows サービス アカウントとして実行されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-803">Make sure that all network printers that have been installed on the AOS server are running as the Windows service account that the AXService.EXE process is running as.</span></span>

## <a name="ax-databasesynchronize-isnt-populated-with-events"></a><span data-ttu-id="b9590-804">Ax-DatabaseSynchronize にイベントが設定されていません</span><span class="sxs-lookup"><span data-stu-id="b9590-804">Ax-DatabaseSynchronize isn't populated with events</span></span>

<span data-ttu-id="b9590-805">プラットフォームの更新 20 およびそれ以降では、データベース同期ログに問題があり、イベント ビューアーで同期ログが **Ax-DatabaseSynchronize** の下に作成されません。</span><span class="sxs-lookup"><span data-stu-id="b9590-805">In Platform update 20 and later, there is database synchronization log issue where the synchronization logs aren't written under **Ax-DatabaseSynchronize** in Event Viewer.</span></span>

<span data-ttu-id="b9590-806">この問題を解決するには、 \<SF-dir\>\\AOS\_\<x\>\\Fabric\\work\\Applications\\AXSFType\_App\<X\>\\log に移動してください。</span><span class="sxs-lookup"><span data-stu-id="b9590-806">To resolve this issue, go to \<SF-dir\>\\AOS\_\<x\>\\Fabric\\work\\Applications\\AXSFType\_App\<X\>\\log.</span></span> <span data-ttu-id="b9590-807">例えば次の場所に移動します。 C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log</span><span class="sxs-lookup"><span data-stu-id="b9590-807">For example, go to C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log.</span></span> <span data-ttu-id="b9590-808">ここでは、DatabaseSynchronize からの出力された内容を確認できます。 Code\_AXSF\_M\_\<X\>.out files.</span><span class="sxs-lookup"><span data-stu-id="b9590-808">Here, you can see the output from DatabaseSynchronize in the Code\_AXSF\_M\_\<X\>.out files.</span></span> <span data-ttu-id="b9590-809">このコンポーネントに関する問題をトラブルシューティングします。</span><span class="sxs-lookup"><span data-stu-id="b9590-809">Troubleshoot any issues that pertain to this component.</span></span>

## <a name="you-cant-access-finance-and-operations-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in"></a><span data-ttu-id="b9590-810">Finance and Operations にアクセスできません: 「AADSTS50058: サイレント サインインの要求が送信されましたが、ログインしているユーザーがいません」</span><span class="sxs-lookup"><span data-stu-id="b9590-810">You can't access Finance and Operations: "AADSTS50058: A silent sign-in request was sent but no user is signed in"</span></span>

<span data-ttu-id="b9590-811">Finance and Operations へのログイン資格情報を入力すると、ブラウザでアプリケーションのレイアウトが少しの間表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9590-811">After a user enters credentials to sign in to Finance and Operations, the browser briefly shows the application layout.</span></span> <span data-ttu-id="b9590-812">しかしその後、Finance and Operations外部へのリダイレクトを試みた結果、次のエラーが出て失敗します。</span><span class="sxs-lookup"><span data-stu-id="b9590-812">However, it then tries to redirect outside Finance and Operations, but fails with the following error:</span></span>

> <span data-ttu-id="b9590-813">AADSTS50058: サイレント サインイン要求が送信されましたが、ユーザーがログインしていません。</span><span class="sxs-lookup"><span data-stu-id="b9590-813">AADSTS50058: A silent sign-in request was sent but no user is signed in.</span></span>

<span data-ttu-id="b9590-814">ユーザーのセッションを表すために使用する Cookie が Azure AD への要求で送信されませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9590-814">The cookies that represent the user's session weren't sent in the request to Azure AD.</span></span> <span data-ttu-id="b9590-815">これは、 Internet Explorer または Microsoft Edge を使用している場合で、webアプリケーションが送信しているサイレント サインインのリクエストが Azure AD エンドポイント (login.microsoftonline.com)とは異なる IEのセキュリティ ゾーンに設定されている場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-815">This issue can occur if the user is using Internet Explorer or Microsoft Edge, and if the web app that sends the silent sign-in request is in a different IE security zone than the Azure AD endpoint (login.microsoftonline.com).</span></span>

<span data-ttu-id="b9590-816">この問題を解決するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-816">This issue occurs because there was a change in the Skype Presence API, and on-premises environments connect to this API by default.</span></span>

<span data-ttu-id="b9590-817">この問題を解決するには、次の SQL Server query を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-817">To resolve the issue, run the following SQL Server query.</span></span>

```
update [AXDB].[dbo].[SYSCLIENTPERF] set SkypeEnabled = 0
```

<span data-ttu-id="b9590-818">または、**クライアント パフォーマンス オプション** ページの **Skype プレゼンスが有効** オプションを無効にします (**システム管理** \> **設定** \> **クライアント パフォーマンス オプション**)。</span><span class="sxs-lookup"><span data-stu-id="b9590-818">Alternatively, turn off the **Skype presence enabled** option on the **Client performance options** page (**System administration** \> **Setup** \> **Client performance options**).</span></span> <span data-ttu-id="b9590-819">この方法を使用するには、Finance and Operations にログインできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-819">To use this approach, you must be able to sign in to Finance and Operations.</span></span> <span data-ttu-id="b9590-820">そのため、最初にブラウザのリダイレクトをブロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-820">Therefore, you must first block redirection in the browser.</span></span> <span data-ttu-id="b9590-821">Skypeのプレゼンス機能を無効にすると、リダイレクトのブロックを解除しても構いません。</span><span class="sxs-lookup"><span data-stu-id="b9590-821">After you disable the Skype presence, you can unblock redirection again.</span></span>

<span data-ttu-id="b9590-822">Chrome ブラウザーでは、最初からリダイレクトがブロックされています。</span><span class="sxs-lookup"><span data-stu-id="b9590-822">The Google Chrome browser blocks redirection by default.</span></span>

## <a name="error-there-was-an-error-during-codepackage-activation-service-host-failed-to-activate-error0x8007052e"></a><span data-ttu-id="b9590-823">エラー: CodePackage の有効化でエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-823">Error: "There was an error during CodePackage activation.</span></span> <span data-ttu-id="b9590-824">サービス ホストの有効化に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-824">Service host failed to activate.</span></span> <span data-ttu-id="b9590-825">エラー: 0x8007052e"</span><span class="sxs-lookup"><span data-stu-id="b9590-825">Error:0x8007052e"</span></span>

<span data-ttu-id="b9590-826">新規インストールの際に以下のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9590-826">You might receive the following error during a new installation:</span></span>

> <span data-ttu-id="b9590-827">エラー イベント: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'。</span><span class="sxs-lookup"><span data-stu-id="b9590-827">Error event: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'.</span></span> <span data-ttu-id="b9590-828">CodePackage の有効化でエラーが発生しました。サービス ホストの有効化に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="b9590-828">There was an error during CodePackage activation.Service host failed to activate.</span></span> <span data-ttu-id="b9590-829">エラー: 0x8007052e</span><span class="sxs-lookup"><span data-stu-id="b9590-829">Error:0x8007052e</span></span>

<span data-ttu-id="b9590-830">このエラーと同じエラーが、AXSFサービスでも発生します。</span><span class="sxs-lookup"><span data-stu-id="b9590-830">This error will cause the AXSF service to fail with the same error.</span></span>

<span data-ttu-id="b9590-831">この問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b9590-831">To resolve this issue, follow these steps.</span></span>

1. <span data-ttu-id="b9590-832">[エージェント共有パス](setup-deploy-on-premises-pu12.md#setupfile) にて、 **netstandard.dll** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="b9590-832">In the [agent share path](setup-deploy-on-premises-pu12.md#setupfile), find the **netstandard.dll** file.</span></span> <span data-ttu-id="b9590-833">このファイルは、例えば \\wp\\\<名\>\\StandaloneSetup -\<バージョン\>\\アプリケーション\\AOS\\AXServiceApp\\AXSF\\コード\\在庫置場\\netstandard.dll に多くの場合存在します。</span><span class="sxs-lookup"><span data-stu-id="b9590-833">For example, this file might be at \\wp\\\<name\>\\StandaloneSetup-\<ver\>\\Apps\\AOS\\AXServiceApp\\AXSF\\Code\\bin\\netstandard.dll.</span></span>
2. <span data-ttu-id="b9590-834">それぞれの AOS サーバーにて、管理者権限で コマンド プロンプトを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b9590-834">On each AOS server, open a Command Prompt window as an administrator, and run the following command.</span></span>

    ```
    "C:\Program Files (x86)\Microsoft SDKs\Windows\v8.1A\bin\NETFX 4.5.1 Tools\gacutil.exe" -i <path from step 1.>\netstandard.dll /f
    ```

3. <span data-ttu-id="b9590-835">Service Fabric から **AXBootstrapperApp** を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-835">Delete **AXBootstrapperApp** from Service Fabric.</span></span>

    1. <span data-ttu-id="b9590-836">**fabric:/Bootstrapper/AXBootstrapper** サービス を削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-836">Delete the **fabric:/Bootstrapper/AXBootstrapper** service.</span></span>
    2. <span data-ttu-id="b9590-837">**fabric:/Bootstrapper** アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-837">Delete the **fabric:/Bootstrapper** application.</span></span>
    3. <span data-ttu-id="b9590-838">**AXBootstrapperAppType** のプロヴィジョニングを解除します。</span><span class="sxs-lookup"><span data-stu-id="b9590-838">Unprovision the **AXBootstrapperAppType** type.</span></span>

4.  <span data-ttu-id="b9590-839">LCS から環境を再配置します。</span><span class="sxs-lookup"><span data-stu-id="b9590-839">Redeploy the environment from LCS.</span></span>

## <a name="sql-server-2016-service-pack-2-is-recommended-for-reporting-services-instances"></a><span data-ttu-id="b9590-840">Reporting Servicesのインスタンス には SQL Server 2016 service pack 2 を推奨します。</span><span class="sxs-lookup"><span data-stu-id="b9590-840">SQL Server 2016 service pack 2 is recommended for Reporting Services instances</span></span>

<span data-ttu-id="b9590-841">LCSにてサービス操作を行うと次のエラーが表示されることがあります:</span><span class="sxs-lookup"><span data-stu-id="b9590-841">When you go through LCS servicing operations, you might receive the following error:</span></span>

> <span data-ttu-id="b9590-842">プロセスが次のファイルにアクセスできません ' c:\\Program Files\\Microsoft SQL Server\\MSRS13.MSSQLSERVER\\Reporting Services\\ReportServer\\bin\\Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' 別のプロセスによって使用されています。</span><span class="sxs-lookup"><span data-stu-id="b9590-842">The process cannot access the file 'C:\\Program Files\\Microsoft SQL Server\\MSRS13.MSSQLSERVER\\Reporting Services\\ReportServer\\bin\\Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' because it is being used by another process.</span></span>

<span data-ttu-id="b9590-843">この問題は Reporting Services が Microsoft Dynamics .dllファイル をロックしているために発生します。</span><span class="sxs-lookup"><span data-stu-id="b9590-843">This issue occurs because Reporting Services has a lock on a Microsoft Dynamics .dll file.</span></span> <span data-ttu-id="b9590-844">Reporting Servicesのインスタンスには、SQL Server 2016 service pack 2をインストールすることを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="b9590-844">We currently recommend that you have SQL Server 2016 service pack 2 installed on Reporting Services instances.</span></span>

> [!NOTE]
> <span data-ttu-id="b9590-845">サービス パック2のインストールが必要し、累積的な更新を追加または修正プログラムをインストールする必要がないです。</span><span class="sxs-lookup"><span data-stu-id="b9590-845">You must have service pack 2 installed, and no additional cumulative updates or hotfixes must be installed.</span></span>
