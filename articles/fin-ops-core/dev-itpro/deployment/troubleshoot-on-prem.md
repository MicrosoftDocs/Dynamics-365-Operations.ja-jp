---
title: オンプレミス配置のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) の配置に対するトラブルシューティング情報を提供します。
author: PeterRFriis
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 2ee5f7a34ba3fba3135321b9aeb30716e251677b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750980"
---
# <a name="troubleshoot-on-premises-deployments"></a><span data-ttu-id="a0be1-103">オンプレミス配置のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a0be1-103">Troubleshoot on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0be1-104">このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) の配置に対するトラブルシューティング情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-104">This topic provides troubleshooting information for deployments of Microsoft Dynamics 365 Finance + Operations (on-premises).</span></span>

## <a name="access-service-fabric-explorer"></a><span data-ttu-id="a0be1-105">Service Fabric Explorer へのアクセス</span><span class="sxs-lookup"><span data-stu-id="a0be1-105">Access Service Fabric Explorer</span></span>

<span data-ttu-id="a0be1-106">Service Fabric Explorer には、Web ブラウザーと既定のアドレス `https://sf.d365ffo.onprem.contoso.com:19080` を使ってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-106">You can access Service Fabric Explorer in a web browser by using the default address, `https://sf.d365ffo.onprem.contoso.com:19080`.</span></span>

<span data-ttu-id="a0be1-107">アドレスを確認するには、環境の適切なセットアップおよび配置トピックの「DNS ゾーンの作成と A レコードの追加」セクションで使用されていた値をメモします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-107">To verify the address, note the value that was used in the "Create DNS zones and add A records" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="a0be1-108">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-108">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#createdns)
- [<span data-ttu-id="a0be1-109">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-109">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#createdns)

<span data-ttu-id="a0be1-110">クライアント証明書が、サイトにアクセスするマシンの証明書、cert:\\CurrentUser\\My に含まれている場合のみ、サイトにアクセスできます</span><span class="sxs-lookup"><span data-stu-id="a0be1-110">You can access the site only if the client certificate is in cert:\\CurrentUser\\My on the machine that you're accessing the site on.</span></span> <span data-ttu-id="a0be1-111">(証明書マネージャーで、**証明書 - 現在のユーザー** \> **個人** \> **証明書** に移動します。) サイトにアクセスしたとき、メッセージが表示されたら、クライアント証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-111">(In Certificate Manger, go to **Certificates - Current User** \> **Personal** \> **Certificates**.) When you access the site, select the client certificate when you're prompted.</span></span>

## <a name="monitor-the-deployment"></a><span data-ttu-id="a0be1-112">配置の監視</span><span class="sxs-lookup"><span data-stu-id="a0be1-112">Monitor the deployment</span></span>

### <a name="identify-the-primary-orchestrator"></a><span data-ttu-id="a0be1-113">プライマリ オーケストレータを識別します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-113">Identify the primary orchestrator</span></span>

<span data-ttu-id="a0be1-114">Service Fabric Explorer でローカル エージェントなどのステートフル サービスのプライマリ インスタンスとなっているマシンを判別するには、**クラスター** \> **アプリケーション** \> **\<*intended application example*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-114">To determine the machine that is the primary instance for stateful services such as a local agent, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **\<*intended application example*\> LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

<span data-ttu-id="a0be1-115">プライマリ ノードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-115">The primary node is shown.</span></span> <span data-ttu-id="a0be1-116">ステートレス サービスまたは残りのアプリケーションについては、すべてのノードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-116">For stateless services or the remaining applications, you must check all the nodes.</span></span>

<span data-ttu-id="a0be1-117">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-117">Note the following points:</span></span>

- <span data-ttu-id="a0be1-118">OrchestrationService は、Finance + Operations の配置およびサービス アクションを調整します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-118">OrchestrationService orchestrates the deployment and servicing actions for Finance + Operations.</span></span>
- <span data-ttu-id="a0be1-119">ArtifactsManager は、ファイルを Microsoft Azure クラウド ストレージからローカル エージェント ファイル共有にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-119">ArtifactsManager downloads files from Microsoft Azure cloud storage to the local agent file share.</span></span> <span data-ttu-id="a0be1-120">ファイルを必要な形式にも解凍します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-120">It also unzips the files into the required format.</span></span>

### <a name="review-the-orchestrator-event-logs"></a><span data-ttu-id="a0be1-121">オーケストレータ イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="a0be1-121">Review the orchestrator event logs</span></span>

<span data-ttu-id="a0be1-122">イベント ビューアー内の プライマリ OrchestrationService オーケストレータ マシンから、 **アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent** と移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-122">From the primary OrchestrationService orchestrator machine, in Event Viewer, go to **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-LocalAgent**.</span></span>

> [!NOTE]
> <span data-ttu-id="a0be1-123">完全なエラー メッセージを表示するには、 **詳細** タブを選択してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-123">To view the full error message, you must select the **Details** tab.</span></span>

<span data-ttu-id="a0be1-124">次のモジュールがインストールされます:</span><span class="sxs-lookup"><span data-stu-id="a0be1-124">The following modules must be installed:</span></span>

- <span data-ttu-id="a0be1-125">共通</span><span class="sxs-lookup"><span data-stu-id="a0be1-125">Common</span></span>
- <span data-ttu-id="a0be1-126">ReportingServices</span><span class="sxs-lookup"><span data-stu-id="a0be1-126">ReportingServices</span></span>
- <span data-ttu-id="a0be1-127">AOS</span><span class="sxs-lookup"><span data-stu-id="a0be1-127">AOS</span></span>
- <span data-ttu-id="a0be1-128">FinancialReporting</span><span class="sxs-lookup"><span data-stu-id="a0be1-128">FinancialReporting</span></span>

<span data-ttu-id="a0be1-129">次のコマンドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-129">The following commands must be run:</span></span>

- <span data-ttu-id="a0be1-130">**セットアップ**</span><span class="sxs-lookup"><span data-stu-id="a0be1-130">**Setup**</span></span>
- <span data-ttu-id="a0be1-131">**Dvt** – このコマンドは配置検証テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-131">**Dvt** – This command runs a deployment verification test.</span></span>
- <span data-ttu-id="a0be1-132">**Cleanup** – このコマンドは環境のサービスと削除に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-132">**Cleanup** – This command is used to service and delete an environment.</span></span>

<span data-ttu-id="a0be1-133">次のフォルダには、追加の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-133">The following folders contain additional information:</span></span>

- <span data-ttu-id="a0be1-134">AX-SetupModuleEvents</span><span class="sxs-lookup"><span data-stu-id="a0be1-134">AX-SetupModuleEvents</span></span>
- <span data-ttu-id="a0be1-135">AX-SetupInfrastructureEvents</span><span class="sxs-lookup"><span data-stu-id="a0be1-135">AX-SetupInfrastructureEvents</span></span>
- <span data-ttu-id="a0be1-136">AX-BridgeService</span><span class="sxs-lookup"><span data-stu-id="a0be1-136">AX-BridgeService</span></span>

<span data-ttu-id="a0be1-137">イベント ビューアーで Microsoft Dynamics エントリを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-137">To review Microsoft Dynamics entries in Event Viewer, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-138">イベント ビューアーで **カスタム ビュー** を右クリックして、**カスタム ビューの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-138">In Event Viewer, right-click **Custom Views**, and then select **Create Custom View**.</span></span>

    ![カスタム表示の作成](media/Create-Custom-View.png)

2. <span data-ttu-id="a0be1-140">**イベント ログ** フィールドで **Dynamics** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-140">In the **Event logs** field, select **Dynamics**.</span></span>

    ![Dynamics の選択](media/Select-Dynamics.png)

> [!NOTE]
> <span data-ttu-id="a0be1-142">また、**カスタム ビュー** で **管理イベント** も確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-142">Also look at **Administrative Events** in **Custom Views**.</span></span>

### <a name="service-fabric-explorer"></a><span data-ttu-id="a0be1-143">Service Fabric Explorer</span><span class="sxs-lookup"><span data-stu-id="a0be1-143">Service Fabric Explorer</span></span>

<span data-ttu-id="a0be1-144">クラスタ、アプリケーション、およびノードの状態に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-144">Note the state of the cluster, application, and nodes.</span></span> <span data-ttu-id="a0be1-145">Service Fabric Explorer にアクセスする方法については、[Service Fabric Explorer にアクセスする](troubleshoot-on-prem.md#access-service-fabric-explorer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-145">For information about how to access Service Fabric Explorer, see [Access Service Fabric Explorer](troubleshoot-on-prem.md#access-service-fabric-explorer).</span></span>

#### <a name="error-partition-is-below-target-replica-or-instance-count"></a><span data-ttu-id="a0be1-146">エラー、「パーティションがターゲット レプリカまたはインスタンス数を下回っています」</span><span class="sxs-lookup"><span data-stu-id="a0be1-146">Error: "Partition is below target replica or instance count"</span></span>

<span data-ttu-id="a0be1-147">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-147">You might receive the following error:</span></span>

> <span data-ttu-id="a0be1-148">パーティションがターゲット レプリカまたはインスタンス数を下回っています</span><span class="sxs-lookup"><span data-stu-id="a0be1-148">Partition is below target replica or instance count</span></span>

<span data-ttu-id="a0be1-149">このエラーはルート エラーではありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-149">This error isn't a root error.</span></span> <span data-ttu-id="a0be1-150">各ノードのステータスが準備できていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-150">It indicates that the status of each node isn't ready.</span></span> <span data-ttu-id="a0be1-151">AXSFType (AOS) では、ステータスがまだ **InBuild** である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-151">For AXSFType (AOS), the status might still be **InBuild**.</span></span>

<span data-ttu-id="a0be1-152">エラー メッセージに関連するコンピューターで、イベント ビューアーを使用して最新の活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-152">On the machines that are related to the error message, use Event Viewer to view the latest activity.</span></span>

#### <a name="axsftype"></a><span data-ttu-id="a0be1-153">AXSFType</span><span class="sxs-lookup"><span data-stu-id="a0be1-153">AXSFType</span></span>

<span data-ttu-id="a0be1-154">AXSFType (AOS) に **InBuild** のステータスが表示される場合、DB Sync ステータスおよび Application Object Server (AOS) コンピューターからの他のイベントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-154">If a status of **InBuild** is shown for AXSFType (AOS), review the DB Sync status and other events from Application Object Server (AOS) machines.</span></span>

<span data-ttu-id="a0be1-155">エラーを診断するには、イベント ビューアーを使用して次のイベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-155">To diagnose errors, use Event Viewer to review the following event logs:</span></span>

- <span data-ttu-id="a0be1-156">アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DatabaseSynchronize</span><span class="sxs-lookup"><span data-stu-id="a0be1-156">Applications and Services Logs \> Microsoft \> Dynamics \> AX-DatabaseSynchronize</span></span>
- <span data-ttu-id="a0be1-157">カスタム ビュー \> 管理イベント</span><span class="sxs-lookup"><span data-stu-id="a0be1-157">Custom Views \> Administrative Events</span></span>

#### <a name="error-extractinstallerservice-failed-to-extract-cusersdynusercontosoappdatalocaltemp1blssblhw0nfabricinstallerservicecodefabricclientdll"></a><span data-ttu-id="a0be1-158">エラー: "'ExtractInstallerService は抽出に失敗しました' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</span><span class="sxs-lookup"><span data-stu-id="a0be1-158">Error: "'ExtractInstallerService failed to extract' C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll"</span></span>

<span data-ttu-id="a0be1-159">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-159">You might receive the following error:</span></span>

> <span data-ttu-id="a0be1-160">"ExtractInstallerService は抽出に失敗しました" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll。</span><span class="sxs-lookup"><span data-stu-id="a0be1-160">"ExtractInstallerService failed to extract" C:\Users\dynuser.CONTOSO\AppData\Local\Temp\1blssblh.w0n\FabricInstallerService.Code\FabricClient.dll.</span></span>

<span data-ttu-id="a0be1-161">このエラーが発生した場合は [Azure Service Fabric](https://go.microsoft.com/fwlink/?LinkId=730690) の最新バージョンをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-161">If you receive this error, download the latest version of [Azure Service Fabric](https://go.microsoft.com/fwlink/?LinkId=730690).</span></span> <span data-ttu-id="a0be1-162">エラー メッセージのユーザー名およびパスは、環境によって変化することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-162">Note that the user name and path in the error message vary, depending on your environment.</span></span>

#### <a name="service-fabric-logs"></a><span data-ttu-id="a0be1-163">Service Fabric ログ</span><span class="sxs-lookup"><span data-stu-id="a0be1-163">Service Fabric logs</span></span>

<span data-ttu-id="a0be1-164">Service Fabric アプリケーションのさらなる詳細については、 C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log のログファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-164">You can find more details about Service Fabric applications in the log files at C:\\ProgramData\\SF\\\<OrchestratorMachineName\>\\Fabric\\work\\Applications\\LocalAgentType\_App\<N\>\\log.</span></span>

### <a name="lifecycle-services"></a><span data-ttu-id="a0be1-165">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a0be1-165">Lifecycle Services</span></span>

<span data-ttu-id="a0be1-166">Microsoft Dynamics Lifecycle Services (LCS) で環境のに対する現在の配置ステータスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-166">Note the current deployment status for the environment in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="a-time-out-error-occurs-when-a-service-fabric-cluster-is-created"></a><span data-ttu-id="a0be1-167">Service Fabric cluster の作成時にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="a0be1-167">A time-out error occurs when a Service Fabric cluster is created</span></span>

<span data-ttu-id="a0be1-168">該当するセットアップ トピックの "スタンドアロン Service Fabric Cluster のセットアップ" セクションおよび環境の配置トピックに記載されているように Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-168">Run Test-D365FOConfiguration.ps1 as noted in the "Set up a standalone Service Fabric cluster" section of the appropriate setup and deployment topic for your environment.</span></span> <span data-ttu-id="a0be1-169">エラーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-169">Note any errors.</span></span>

- [<span data-ttu-id="a0be1-170">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-170">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupsfcluster)
- [<span data-ttu-id="a0be1-171">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-171">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster)

<span data-ttu-id="a0be1-172">これらの手順を必ず実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-172">Be sure to complete these steps:</span></span>

- <span data-ttu-id="a0be1-173">すべての Service Fabric ノード上の LocalMachine ストアに Service Fabric Server クライント証明書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-173">Verify that the Service Fabric Server client certificate exists in the LocalMachine store on all Service Fabric nodes.</span></span>
- <span data-ttu-id="a0be1-174">Service Fabric Server 証明書にすべての Service Fabric ノード上にネットワーク サービス用アクセス制御リスト (ACL) が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-174">Verify that the Service Fabric Server certificate has the access control list (ACL) for Network Service on all Service Fabric nodes.</span></span>
- <span data-ttu-id="a0be1-175">[環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) で記載されているウイルス対策の除外を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-175">Review the antivirus exclusions that are noted in [Environment setup](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="a-time-out-error-occurs-while-youre-waiting-for-installer-service-to-be-completed-for-machine-xxxx"></a><span data-ttu-id="a0be1-176">インストーラー サービスがマシン x.x.x.x で完了するのを待つ間にタイムアウト エラーが発生する</span><span class="sxs-lookup"><span data-stu-id="a0be1-176">A time-out error occurs while you're waiting for Installer Service to be completed for machine x.x.x.x</span></span>

<span data-ttu-id="a0be1-177">インターネット プロトコル (IP) アドレスごとに (つまり、コンピューターごとに) 1 つのノード タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-177">Only one node type is supported for each Internet Protocol (IP) address (that is, for each machine).</span></span> <span data-ttu-id="a0be1-178">ノードが同じマシン上で再利用されているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-178">Check whether the nodes are being reused on the same machine.</span></span> <span data-ttu-id="a0be1-179">たとえば、AOS および ORCH は、同一のマシン上に存在してはならず、ConfigTemplate.xml が正しく定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-179">For example, AOS and ORCH must not be on the same machine, and ConfigTemplate.xml must be correctly defined.</span></span>

## <a name="remove-a-specific-application"></a><span data-ttu-id="a0be1-180">特定のアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="a0be1-180">Remove a specific application</span></span>

<span data-ttu-id="a0be1-181">配置の削除またはクリーンアップに LCS を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-181">We recommend that you use LCS to remove or clean up deployments.</span></span> <span data-ttu-id="a0be1-182">ただし、必要に応じて、アプリケーションを削除する Service Fabric Explorer を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-182">However, you can also use Service Fabric Explorer to remove an application as you require.</span></span>

<span data-ttu-id="a0be1-183">Service Fabric エクスプローラーで、**アプリケーション ノード** \> **アプリケーション** \> **MonitoringAgentAppType-Agent** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-183">In Service Fabric Explorer, go to **Application node** \> **Applications** \> **MonitoringAgentAppType-Agent**.</span></span> <span data-ttu-id="a0be1-184">**ファブリック:/エージェント監視** の横にある省略記号ボタン (**...**) を選択し、アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-184">Select the ellipsis button (**...**) next to **fabric:/Agent-Monitoring**, and delete the application.</span></span> <span data-ttu-id="a0be1-185">アプリケーションの完全な名前を入力して、アプリケーションの削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-185">Enter the full name of the application to confirm the deletion of the application.</span></span>

<span data-ttu-id="a0be1-186">また、省略記号ボタンの選択および **非引当タイプ** の順に選択することにより、MonitoringAgentAppType-Agent を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-186">You can also remove MonitoringAgentAppType-Agent by selecting the ellipsis button and then selecting **Unprovision Type**.</span></span> <span data-ttu-id="a0be1-187">アプリケーションの削除を確認するために、正式名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-187">Enter the full name to confirm the removal of the application.</span></span>

## <a name="remove-all-applications-from-service-fabric"></a><span data-ttu-id="a0be1-188">Service Fabric からすべてのアプリケーションを削除</span><span class="sxs-lookup"><span data-stu-id="a0be1-188">Remove all applications from Service Fabric</span></span>

<span data-ttu-id="a0be1-189">次のスクリプトは、LocalAgent および LocalAgent の監視エージェントを除く、すべての Service Fabric アプリケーションを削除してプロビジョニング解除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-189">The following script removes and unprovisions all Service Fabric applications except LocalAgent and the monitoring agent for LocalAgent.</span></span> <span data-ttu-id="a0be1-190">オーケストレータ仮想マシン (VM) 上でこのスクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-190">You must run this script on an orchestrator virtual machine (VM).</span></span>

```powershell
$applicationNamesToIgnore = @('fabric:/LocalAgent', 'fabric:/Agent-Monitoring', 'fabric:/Agent-LBDTelemetry')
$applicationTypeNamesToIgnore = @('MonitoringAgentAppType-Agent', 'LocalAgentType', 'LBDTelemetryType-Agent')

Get-ServiceFabricApplication | `
    Where-Object { $_.ApplicationName -notin $applicationNamesToIgnore } | `
    Remove-ServiceFabricApplication -Force

Get-ServiceFabricApplicationType | `
    Where-Object { $_.ApplicationTypeName -notin $applicationTypeNamesToIgnore } | `
    Unregister-ServiceFabricApplicationType -Force
```

## <a name="remove-service-fabric"></a><span data-ttu-id="a0be1-191">Service Fabric の削除</span><span class="sxs-lookup"><span data-stu-id="a0be1-191">Remove Service Fabric</span></span>

<span data-ttu-id="a0be1-192">Service Fabric クラスターを完全に削除するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-192">To completely remove the Service Fabric cluster, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-193">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-193">Run the following command.</span></span>

    ```powershell
    .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

2. <span data-ttu-id="a0be1-194">エラーが発生した場合は、**CleanFabric.ps1** コマンドを使用して、クラスタ内の特定のノードを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-194">If an error occurs, remove a specific node on the cluster by using the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="a0be1-195">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-195">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span>
3. <span data-ttu-id="a0be1-196">既定の場所を使用している場合、**C:\\ProgramData\\SF** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-196">Remove the **C:\\ProgramData\\SF** folder, if you're using the default location.</span></span> <span data-ttu-id="a0be1-197">それ以外の場合、指定したフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-197">Otherwise, remove the specified folder.</span></span>

    <span data-ttu-id="a0be1-198">"アクセス拒否" エラーが発生した場合は、Microsoft Windows PowerShell を再起動するか、マシンを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-198">If you receive an "Access denied" error, restart Microsoft Windows PowerShell or the machine.</span></span>

## <a name="clean-up-an-existing-environment-and-redeploy"></a><span data-ttu-id="a0be1-199">既存環境のクリーンアップと再配置</span><span class="sxs-lookup"><span data-stu-id="a0be1-199">Clean up an existing environment and redeploy</span></span>

<span data-ttu-id="a0be1-200">既存の環境をクリーンアップして再配置するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-200">To clean up an existing environment and redeploy, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-201">LCS でプロジェクトを開き、**環境** セクションで展開を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-201">In LCS, open the project, and then, in the **Environments** section, delete the deployment.</span></span>

    <span data-ttu-id="a0be1-202">アプリケーションが環境の Service Fabric Explorer から表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-202">The applications should start to disappear from Service Fabric Explorer in the environment.</span></span> <span data-ttu-id="a0be1-203">このプロセスは 1、2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-203">This process will take one to two minutes.</span></span>

2. <span data-ttu-id="a0be1-204">LocalAgentCLI.exe を含むオーケストレーター マシンにアクセスし、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-204">Access the orchestrator machine that contains LocalAgentCLI.exe, and follow these steps:</span></span>

    1. <span data-ttu-id="a0be1-205">ローカル エージェント クリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-205">Run the local agent cleanup.</span></span>

        ```powershell
        .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
        ```

    2. <span data-ttu-id="a0be1-206">Service Fabric を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-206">Remove Service Fabric.</span></span>

        ```powershell
        .\RemoveServiceFabricCluster.ps1 -ClusterConfigFilePath '<path of ClusterConfig.json>'
        ```

    3. <span data-ttu-id="a0be1-207">ノードが失敗した場合、**CleanFabric.ps1** コマンドを実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-207">If any nodes fail, run the **CleanFabric.ps1** command.</span></span> <span data-ttu-id="a0be1-208">このコマンドは、C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code で検索することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-208">You can find this command in C:\\Program Files\\Microsoft Service Fabric\\bin\\fabric\\fabric.code.</span></span>
    4. <span data-ttu-id="a0be1-209">すべての Service Fabric ノードの **C:\\ProgramData\\SF\\** フォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-209">Remove the **C:\\ProgramData\\SF\\** folder on all Service Fabric nodes.</span></span>

        <span data-ttu-id="a0be1-210">"アクセス拒否" エラーが発生した場合は、マシンを再起動してからもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-210">If you receive an "Access denied" error, restart the machine, and try again.</span></span>

3. <span data-ttu-id="a0be1-211">必要に応じて証明書を削除または更新します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-211">Remove or update certificates as required.</span></span>

    <span data-ttu-id="a0be1-212">すべての AOS、BI、ORCH、および DC ノードから古い証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-212">Remove old certificates from all AOS, BI, ORCH, and DC nodes.</span></span>

    - <span data-ttu-id="a0be1-213">証明書は、次の証明書ストアに存在します: Cert:\\CurrentUser\\My\\、Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root。</span><span class="sxs-lookup"><span data-stu-id="a0be1-213">The certificates exist in the following certificate stores: Cert:\\CurrentUser\\My\\, Cert:\\LocalMachine\\My, and Cert:\\LocalMachine\\Root.</span></span>
    - <span data-ttu-id="a0be1-214">Microsoft SQL Server の設定が変更される場合は、SQL Server 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-214">If the setup of Microsoft SQL Server will be modified, remove the SQL Server certificates.</span></span>
    - <span data-ttu-id="a0be1-215">Active Directory フェデレーション サービス (AD FS) の設定が変更される場合は、AD FS 証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-215">If the settings for Active Directory Federation Services (AD FS) will be modified, remove the AD FS certificate.</span></span>

4. <span data-ttu-id="a0be1-216">必要に応じて、次の構成ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-216">Update the following configuration files as required:</span></span>

    - <span data-ttu-id="a0be1-217">ConfigTemplate.xml</span><span class="sxs-lookup"><span data-stu-id="a0be1-217">ConfigTemplate.xml</span></span>
    - <span data-ttu-id="a0be1-218">ClusterConfig.json</span><span class="sxs-lookup"><span data-stu-id="a0be1-218">ClusterConfig.json</span></span>

    <span data-ttu-id="a0be1-219">テンプレートのフィールドに正しく入力する方法については、ご使用の環境に適した設定と配置のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-219">For information about how to correctly fill in the fields in the templates, see the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="a0be1-220">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-220">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md)
    - [<span data-ttu-id="a0be1-221">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-221">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md)

5. <span data-ttu-id="a0be1-222">LCS でプロジェクトを開き、必要に応じて LCS のオンプレミス コネクタを更新します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-222">In LCS, open the project, and update the LCS on-premises connector as required.</span></span>

    1. <span data-ttu-id="a0be1-223">環境の LCS オンプレミス コネクタを再作成するか、または既存のコネクタの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-223">Re-create the LCS on-premises connector for the environment, or edit the settings of an existing connector.</span></span>

        <span data-ttu-id="a0be1-224">LCS の値を簡単にコピーするには、.\\Get-AgentConfiguration.ps1 script を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-224">To obtain easy-to-copy values for LCS, use the .\\Get-AgentConfiguration.ps1 script.</span></span>

    2. <span data-ttu-id="a0be1-225">最新のローカル エージェント コンフィギュレーション、localagent config.json をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-225">Download the latest local agent configuration, localagent-config.json.</span></span>

6. <span data-ttu-id="a0be1-226">環境に適したセットアップと展開のトピックで次の指示に従って、再度展開します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-226">Deploy again by following the instructions in the appropriate setup and deployment topic for the environment:</span></span>

    - [<span data-ttu-id="a0be1-227">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-227">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md)
    - <span data-ttu-id="a0be1-228">[プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-228">[Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md).</span></span>

## <a name="find-the-local-agent-values-that-are-used"></a><span data-ttu-id="a0be1-229">使用するローカル エージェント値の検索</span><span class="sxs-lookup"><span data-stu-id="a0be1-229">Find the local agent values that are used</span></span>

<span data-ttu-id="a0be1-230">Service Fabric Explorer でローカル エージェント値を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-230">You can find local agent values in Service Fabric Explorer.</span></span> <span data-ttu-id="a0be1-231">**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent** に移動して **詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-231">Go to **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent**, and then select **Details**.</span></span>

<span data-ttu-id="a0be1-232">または、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-232">Alternatively, run the following Windows PowerShell command.</span></span>

```powershell
.\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

## <a name="install-upgrade-or-uninstall-a-local-agent"></a><span data-ttu-id="a0be1-233">ローカル エージェントのインストール、アップグレード、アンインストール</span><span class="sxs-lookup"><span data-stu-id="a0be1-233">Install, upgrade, or uninstall a local agent</span></span>

<span data-ttu-id="a0be1-234">ローカルエージェントを更新する方法については、 [ローカルエージェントを更新する](../lifecycle-services/update-local-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-234">For information about how to update the local agent, see [Update the local agent](../lifecycle-services/update-local-agent.md).</span></span>

<span data-ttu-id="a0be1-235">また、以下のアップグレードおよびアンインストール コマンドを使用することができます:</span><span class="sxs-lookup"><span data-stu-id="a0be1-235">You can also use the following upgrade and uninstallation commands:</span></span>

```powershell
LocalAgentCLI.exe Install <path of localagent-config.json>
LocalAgentCLI.exe Cleanup <path of localagent-config.json>
```

> [!NOTE]
> <span data-ttu-id="a0be1-236">**クリーンアップ** コマンドはファイル共有に配置された一切のファイルを削除しません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-236">The **Cleanup** command doesn't remove any files that were put in the file share.</span></span> <span data-ttu-id="a0be1-237">ファイル共有は再利用できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-237">The file share can be reused.</span></span>

## <a name="an-error-occurs-when-local-agent-services-are-started"></a><span data-ttu-id="a0be1-238">ローカル エージェント サービスを開始される際にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="a0be1-238">An error occurs when local agent services are started</span></span>

<span data-ttu-id="a0be1-239">ローカル エージェント サービスが開始されると、次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-239">When local agent services are started, you might receive the following error:</span></span>

> <span data-ttu-id="a0be1-240">ファイル、アセンブリ 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35'、もしくはその依存関係の 1 つをロードできませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0be1-240">Could not load file or assembly 'Lcs.DeploymentAgent.Proxy.Contract, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span>

<span data-ttu-id="a0be1-241">このエラーは厳密な名前検証が有効になっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-241">This error means that strong name verification is turned on.</span></span> <span data-ttu-id="a0be1-242">Configure-PreReqs.ps1 を使用して、この確認をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-242">You can turn off this verification by using Configure-PreReqs.ps1.</span></span> <span data-ttu-id="a0be1-243">厳密な名前検証がもう有効になっていないことを確認するには、Test-D365FOConfiguration.ps1 を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-243">To validate that strong name verification is no longer turned on, run Test-D365FOConfiguration.ps1.</span></span>

## <a name="a-validation-in-progress-message-is-shown-for-several-minutes-in-lcs"></a><span data-ttu-id="a0be1-244">「検証が進行中」のメッセージが LCS に数分表示</span><span class="sxs-lookup"><span data-stu-id="a0be1-244">A "Validation in progress" message is shown for several minutes in LCS</span></span>

<span data-ttu-id="a0be1-245">ローカル エージェントの検証に関する一般的な問題をトラブルシューティングするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-245">Follow these steps to troubleshoot general issues with local agent validation.</span></span>

1. <span data-ttu-id="a0be1-246">コンピューターを正しくコンフィギュレーションするすべてのオーケストレータ機械で **Configure-PreReqs.ps1** を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-246">Run **Configure-PreReqs.ps1** on all orchestrator machines to configure the machines correctly.</span></span>
2. <span data-ttu-id="a0be1-247">Test-D365FOConfiguration.ps1 スクリプトがすべてのオーケストレータ マシンで通ることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-247">Verify that the Test-D365FOConfiguration.ps1 script passes on all the orchestrator machines.</span></span>
3. <span data-ttu-id="a0be1-248">LocalAgentCLI.exe のインストールが正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-248">Verify that the installation of LocalAgentCLI.exe is successfully completed.</span></span>
4. <span data-ttu-id="a0be1-249">Service Fabric Explorer で、すべてのアプリケーションが正常であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-249">In Service Fabric Explorer, verify that all the applications are healthy.</span></span>
5. <span data-ttu-id="a0be1-250">アプリケーションが正常でない場合は、障害が発生しているサービスのプライマリ ノードを探します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-250">If the applications aren't healthy, find the primary node for the service that is failing.</span></span> <span data-ttu-id="a0be1-251">イベント ビューアーでは、次の場所でのイベントを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-251">In Event Viewer, look for events in the following locations:</span></span>

    - <span data-ttu-id="a0be1-252">カスタム ビュー \> 管理イベント</span><span class="sxs-lookup"><span data-stu-id="a0be1-252">Custom Views \> Administrative Events</span></span>
    - <span data-ttu-id="a0be1-253">アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-LocalAgent</span><span class="sxs-lookup"><span data-stu-id="a0be1-253">Applications and Services Log \> Microsoft \> Dynamics \> AX-LocalAgent</span></span>

## <a name="local-agent-errors"></a><span data-ttu-id="a0be1-254">ローカル エージェント エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-254">Local agent errors</span></span>

### <a name="issue"></a><span data-ttu-id="a0be1-255">問題点</span><span class="sxs-lookup"><span data-stu-id="a0be1-255">Issue</span></span>

<span data-ttu-id="a0be1-256">**エラー :** ローカル エージェントをインストールすると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-256">**Error:** When you install the local agent, you receive the following error.</span></span>

```stacktrace
LocalAgentCLI.exe Error: 0 : Exception System.InvalidOperationException: unable to get settings for telemetry setup component
    at LBDTelemetryCommon.LBDTelemetrySetupManager.GetComponentSettings()
    at LBDTelemetryCommon.LBDTelemetrySetupManager.ApplyParameters()
    at LocalAgentCLI.Program.Main(String[] args)
Press any key to exit
```

<span data-ttu-id="a0be1-257">**理由:** ローカル エージェント バージョン 2.3.0 またはそれ以降のバージョンをインストールしようとしていますが、使用している localagent-config.json ファイルが最新ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-257">**Reason:** You're trying to install local agent version 2.3.0 or later, but the localagent-config.json file that you're using isn't up to date.</span></span>

<span data-ttu-id="a0be1-258">**手順:** [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector) の 「コネクタ構成とオンプレミスのローカル エージェントのインストール」 セクションの手順に従って、localagent-config.json ファイルの新しいバージョンを LCS から入手します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-258">**Steps:** Get the new version of the localagent-config.json file from LCS by following the instructions in the "Configure a connector and install an on-premises local agent" section of [Set up and deploy on-premises environments](setup-deploy-on-premises-pu12.md#configureconnector).</span></span>

<span data-ttu-id="a0be1-259">localagent-configjson ファイルの **コンポーネント** セクションで次の値を手動で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-259">You can also manually add the following values in the **components** section of the localagent-config.json file.</span></span>
```json
{
    "name": "LBDTelemetry",
    "placementCriteria": "(IsOrchestratorEnabled == True)",
    "parameters": {
        "applicationPackagePath": {
            "value": "Applications\\LBDTelemetry"
        }
    }
},
```

### <a name="issue"></a><span data-ttu-id="a0be1-260">問題点</span><span class="sxs-lookup"><span data-stu-id="a0be1-260">Issue</span></span>

<span data-ttu-id="a0be1-261">**エラー:** 次のエラーが表示される場合があります:</span><span class="sxs-lookup"><span data-stu-id="a0be1-261">**Error:** You might receive the following errors:</span></span>

> <span data-ttu-id="a0be1-262">コマンドを処理できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-262">Unable to process commands</span></span>

> <span data-ttu-id="a0be1-263">チャンネル情報を取得できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-263">Unable to get the channel information</span></span>

> <span data-ttu-id="a0be1-264">ホスト プロセスがクラッシュする処理されない例外が原因で RunAsync が失敗しました: System.ArgumentNullException: 値を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-264">RunAsync failed due to an unhandled exception causing the host process to crash: System.ArgumentNullException: Value cannot be null.</span></span> <span data-ttu-id="a0be1-265">パラメーター名: 証明書</span><span class="sxs-lookup"><span data-stu-id="a0be1-265">Parameter name: certificate</span></span>

<span data-ttu-id="a0be1-266">**理由:** これらのエラーは OnPremLocalAgent 証明書に指定された証明書が有効でないか、またはテナントに対して正しく構成されていないために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-266">**Reason:** These errors can occur because the certificate that is specified for the OnPremLocalAgent certificate either isn't valid or isn't correctly configured for the tenant.</span></span>

<span data-ttu-id="a0be1-267">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-267">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="a0be1-268">すべてのオーケストレータ ノードで **Test-D365FOConfiguration.ps1** を実行し、すべてのチェックに合格することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-268">Run **Test-D365FOConfiguration.ps1** on all orchestrator nodes to make sure that all checks pass.</span></span>
2. <span data-ttu-id="a0be1-269">ローカル エージェント コンフィギュレーションに指定された証明書が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-269">Verify that the certificate that is specified in the local agent configuration is correct.</span></span>

    - <span data-ttu-id="a0be1-270">LCS および ConfigTemplate.xml ファイルで指定する拇印に特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-270">Make sure that the thumbprint that you specify in LCS and in the ConfigTemplate.xml file has no special characters.</span></span>
    - <span data-ttu-id="a0be1-271">証明書は、infrastructure\\ConfigTemplate.xml の次のセクションで指定されているものと同じ証明書である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-271">The certificate should be the same certificate that is specified in the following section in infrastructure\\ConfigTemplate.xml.</span></span>

        ```xml
        <Certificate type="Orchestrator" exportable="true" generateSelfSignedCert="true">
            <Name>OnPremLocalAgent</Name>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

3. <span data-ttu-id="a0be1-272">LCS のローカル エージェント コンフィギュレーションで指定される同じ証明書が、環境に対する適切な設定および配置トピックの「テナント用 LCS 接続の構成」セクションで手順の完了に使用されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-272">Make sure that the same certificate that is specified in the local agent configuration in LCS was used to complete the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="a0be1-273">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-273">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="a0be1-274">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-274">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

4. <span data-ttu-id="a0be1-275">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-275">Uninstall the local agent.</span></span>
5. <span data-ttu-id="a0be1-276">ローカル エージェント コンフィギュレーションで正しい証明書を指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-276">Specify the correct certificate in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="a0be1-277">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-277">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="a0be1-278">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-278">Error</span></span>

<span data-ttu-id="a0be1-279">**エラー:** サービス中に "資産をダウンロードできません" というエラーが表示され、詳細に "パッケージに提供された資格情報が認識されません" と表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-279">**Error:** During servicing, you receive an "Unable to download asset" error, and the details state, "The credentials supplied to the package were not recognized."</span></span>

<span data-ttu-id="a0be1-280">**理由:** ACL が証明書で正しく定義されていません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-280">**Reason:** The ACL wasn't correctly defined on certificates.</span></span>

<span data-ttu-id="a0be1-281">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-281">**Steps:**</span></span>

<span data-ttu-id="a0be1-282">オーケストレータ マシンのクライアント証明書から ACL が削除されたかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-282">Check whether ACL was removed from client certificate on orchestrator machines.</span></span> <span data-ttu-id="a0be1-283">オーケストレータ マシンの .\Test-D365FOConfiguration.ps1 スクリプトを実行し、ACL を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-283">Run the .\Test-D365FOConfiguration.ps1 script on orchestrator machines, and verify the ACL.</span></span>

<span data-ttu-id="a0be1-284">エラーを解決するには、.\Set-CertificateAcls.ps1 スクリプトを実行して ACL をリセットします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-284">To resolve the error, run the .\Set-CertificateAcls.ps1 script to reset the ACLs.</span></span> 

### <a name="error"></a><span data-ttu-id="a0be1-285">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-285">Error</span></span>

<span data-ttu-id="a0be1-286">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-286">**Error:**</span></span>

> <span data-ttu-id="a0be1-287">パス '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' へアクセスすることは、拒否されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-287">Access to the path '\\...\\agent\\assets\\StandAloneSetup-76308-1.zip' is denied.</span></span>

<span data-ttu-id="a0be1-288">**理由:** ローカル エージェント コンフィギュレーションで指定されたファイル共有が無効です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-288">**Reason:** The file share that is specified in the local agent configuration isn't valid.</span></span>

<span data-ttu-id="a0be1-289">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-289">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="a0be1-290">指定した共有が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-290">Verify that the specified share exists.</span></span>
2. <span data-ttu-id="a0be1-291">ローカル エージェント ユーザーが共有への完全なアクセス許可を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-291">Verify that the local agent user has full permission on the share.</span></span> <span data-ttu-id="a0be1-292">ローカル エージェント ユーザーは、次のセクションの ConfigTemplate.xml で指定されるドメイン ネーム システム (DNS) 名です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-292">The local agent user is the Domain Name System (DNS) name that is specified in the following section in ConfigTemplate.xml.</span></span>

    ```xml
    <ADServiceAccount type="gMSA" name="svc-LocalAgent$" refName="gmsaLocalAgent">
        <DNSHostName>svc-LocalAgent.d365ffo.onprem.contoso.com</DNSHostName>
    </ADServiceAccount>
    ```

3. <span data-ttu-id="a0be1-293">適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックが完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-293">Make sure that the "Set up file storage" section of the appropriate setup and deployment topic for your environment is completed:</span></span>

    - [<span data-ttu-id="a0be1-294">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-294">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
    - [<span data-ttu-id="a0be1-295">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-295">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)

4. <span data-ttu-id="a0be1-296">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-296">Uninstall the local agent.</span></span>
5. <span data-ttu-id="a0be1-297">ローカル エージェント コンフィギュレーションで正しいファイル共有指定し、もう一度コンフィギュレーション ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-297">Specify the correct file share in the local agent configuration, and download the configuration file again.</span></span>
6. <span data-ttu-id="a0be1-298">新しい構成ファイルを使用してもう一度ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-298">Install the local agent again by using the new configuration file.</span></span>

### <a name="error"></a><span data-ttu-id="a0be1-299">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-299">Error</span></span>

<span data-ttu-id="a0be1-300">**エラー:** サービス操作を行うと次のエラーが表示されます:</span><span class="sxs-lookup"><span data-stu-id="a0be1-300">**Error:** When you do a servicing operation, you receive the following error:</span></span>

> <span data-ttu-id="a0be1-301">コマンドの抽出セットアップ フォルダーを取得できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-301">Unable to get extract setup folder for command</span></span>

<span data-ttu-id="a0be1-302">**理由:** そのファイル共有は削除または変更されました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-302">**Reason:** The file share has been removed or changed.</span></span>

<span data-ttu-id="a0be1-303">**手順:** ファイル共有の設定内容を確認するには、Microsoft SQL Server Management Studio を開いてオーケストレータ データベースで次のクエリを実行します:</span><span class="sxs-lookup"><span data-stu-id="a0be1-303">**Steps:** To see what the file share is set to, open Microsoft SQL Server Management Studio, and run the following query on the orchestrator database:</span></span>

```sql
select * from OrchestratorCommandArtifact where CommandId = 'xxx'
```

### <a name="error"></a><span data-ttu-id="a0be1-304">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-304">Error</span></span>

<span data-ttu-id="a0be1-305">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-305">**Error:**</span></span>

> <span data-ttu-id="a0be1-306">ユーザー 'D365\\svc-LocalAgent$' へのログインが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-306">Login failed for user 'D365\\svc-LocalAgent$'.</span></span> <span data-ttu-id="a0be1-307">理由: 指定した名前に一致するログインが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0be1-307">Reason: Could not find a login matching the name provided.</span></span> <span data-ttu-id="a0be1-308">\[CLIENT: 10.0.2.23\]</span><span class="sxs-lookup"><span data-stu-id="a0be1-308">\[CLIENT: 10.0.2.23\]</span></span>

<span data-ttu-id="a0be1-309">**理由:** ローカル エージェント ユーザーはオーケストレーション データベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-309">**Reason:** The local agent user can't connect to the orchestrator database.</span></span> <span data-ttu-id="a0be1-310">ユーザーが削除され、Active Directory ドメイン サービス (AD DS) に再作成されているために、この問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-310">This issue can occur because users have been deleted and then re-created in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="a0be1-311">したがって、ユーザーのセキュリティ識別子 (SID) が変更され、SQL Server インスタンスまたはデータベースのユーザーに与えられたアクセスは機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-311">Therefore, the security identifier (SID) of the user has changed, and any access that was given to the user for the SQL Server instance or the database no longer works.</span></span>

<span data-ttu-id="a0be1-312">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-312">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="a0be1-313">SQL Server インスタンスで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-313">Run the following script on the SQL Server instance.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    <span data-ttu-id="a0be1-314">このスクリプトは、空のデータベースがまだ存在していない場合に、空のオーケストレータ データベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-314">This script creates an empty orchestrator database, if an empty database doesn't already exist.</span></span> <span data-ttu-id="a0be1-315">ローカル エージェント ユーザーをデータベースに追加し、データベース\_アクセス許可の所有者に渡します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-315">It then adds the local agent user to the database and gives it db\_owner permission.</span></span>

    <span data-ttu-id="a0be1-316">適切なアクセス許可が付与された後、アプリケーションは自動的に正常な状態になります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-316">After the correct permissions are provided, the application should automatically go to a healthy state.</span></span>

2. <span data-ttu-id="a0be1-317">SQL Server インスタンスの完全修飾ドメイン名 (FQDN)、データベース名、ローカル エージェント ユーザーなどの設定が LCS で間違って提供された場合は、設定を変更し、ローカル エージェントを再インストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-317">If any settings, such as the fully qualified domain name (FQDN) of the SQL Server instance, the database name, or the local agent user, were provided incorrectly in LCS, change the settings, and then reinstall the local agent.</span></span>

<span data-ttu-id="a0be1-318">上記の手順でエラーが解決しない場合は、SQL Server インスタンスとデータベースからローカル エージェント ユーザーを手動で削除し、Initialize-Database スクリプトを再実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-318">If the preceding steps don't resolve the error, manually remove the local agent user from the SQL Server instance and the database, and then rerun the Initialize-Database script.</span></span>

<span data-ttu-id="a0be1-319">AD DS でユーザーを再作成する場合、SID が変更されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-319">If you re-create a user in AD DS, remember that the SID will change.</span></span> <span data-ttu-id="a0be1-320">この場合、ユーザーの以前の SID を削除し、新しい SID を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-320">In this case, remove the previous SID for the user, and add a new SID.</span></span>

### <a name="error"></a><span data-ttu-id="a0be1-321">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-321">Error</span></span>

<span data-ttu-id="a0be1-322">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-322">**Error:**</span></span> 
> <span data-ttu-id="a0be1-323">データベースを移行できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-323">Unable to migrate database</span></span>

<span data-ttu-id="a0be1-324">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-324">**Steps:**</span></span>

- <span data-ttu-id="a0be1-325">SQL Server リスナーへのアクセスがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-325">Verify that you have access to the SQL Server listener.</span></span>
- <span data-ttu-id="a0be1-326">テストをしている場合は、最初からやり直して空のオーケストレータ データベースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-326">If you're doing testing, you can start over and use an empty orchestrator database.</span></span>

### <a name="issue"></a><span data-ttu-id="a0be1-327">問題点</span><span class="sxs-lookup"><span data-stu-id="a0be1-327">Issue</span></span>

<span data-ttu-id="a0be1-328">[データベースを構成する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb) プロシージャを実行するときに SQL Server インスタンスが名前付きインスタンスの場合は、**-DatabaseServer \[FQDN/Instancename\]** パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-328">When you performing the [Configure the databases](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#configuredb) procedure, if the SQL Server instance is a named instance, use the **-DatabaseServer \[FQDN/Instancename\]** parameter.</span></span>

### <a name="issue"></a><span data-ttu-id="a0be1-329">問題点</span><span class="sxs-lookup"><span data-stu-id="a0be1-329">Issue</span></span>

<span data-ttu-id="a0be1-330">ローカル エージェント ユーザーは、SQL Server インスタンスまたはデータベースに接続できません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-330">The local agent user can't connect to the SQL Server instance or the database.</span></span>

<span data-ttu-id="a0be1-331">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-331">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="a0be1-332">SQL Server のプライマリ ノード データベースから svc-LocalAgent ユーザーを削除し、両方のサーバーからログインを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-332">Delete the svc-LocalAgent user from the SQL Server primary node databases, and then remove the login from both servers.</span></span>
2. <span data-ttu-id="a0be1-333">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-333">Run the following scripts.</span></span>

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="a0be1-334">これらのスクリプトは、**常時オン** に設定されているときは機能しません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-334">These scripts don't work when an **always-on** setup is used.</span></span> <span data-ttu-id="a0be1-335">データベースは最初にプライマリ ノードに作成されてから複製される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-335">The database must first be created in the primary node and then replicated.</span></span>

### <a name="error"></a><span data-ttu-id="a0be1-336">エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-336">Error</span></span>

<span data-ttu-id="a0be1-337">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-337">**Error:**</span></span>

> <span data-ttu-id="a0be1-338">RunAsync は、処理されていない例外が原因でホスト プロセスがクラッシュするため、失敗しました。System.Net.Http.HttpRequestException: 要求の送信中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-338">RunAsync failed due to an unhandled exception causing the host process to crash: System.Net.Http.HttpRequestException: An error occurred while sending the request.</span></span><span data-ttu-id="a0be1-339"> ---\> System.Net.WebException: リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'</span><span class="sxs-lookup"><span data-stu-id="a0be1-339"> ---\> System.Net.WebException: The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'</span></span>

<span data-ttu-id="a0be1-340">**理由:** ローカル エージェント マシンは lcsapi.lcs.dynamics.com に接続できません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-340">**Reason:** The local agent machines can't connect to lcsapi.lcs.dynamics.com.</span></span> <span data-ttu-id="a0be1-341">「リモート名を解決できませんでした: 'lcsapi.lcs.dynamics.com'」に対する AX-BridgeService イベント ログを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-341">Review the AX-BridgeService event log for "The remote name could not be resolved: 'lcsapi.lcs.dynamics.com'."</span></span>

<span data-ttu-id="a0be1-342">**ステップ:** エラーを解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-342">**Steps:** Follow these steps to resolve the error.</span></span>

1. <span data-ttu-id="a0be1-343">**psping lcsapi.lcs.dynamics.com:80** を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-343">Run **psping lcsapi.lcs.dynamics.com:80**.</span></span>
2. <span data-ttu-id="a0be1-344">前述のコマンドから応答を受信しない場合は、組織の IT 部門に問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-344">If you don't receive a response from the preceding command, contact the IT department at your organization.</span></span> <span data-ttu-id="a0be1-345">ファイアウォールが lcsapi へのアクセスをブロックしているか、もしくはプロキシの問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-345">Either the firewall is blocking access to lcsapi, or proxy issues are occurring.</span></span>

    ```Console
    lcsapi.lcs.dynamics.com:443
    login.windows.net:443
    uswelcs1lcm.queue.core.windows.net:443
    www.office.com:443
    login.microsoftonline.com:443
    dc.services.visualstudio.com:443
    uswelcs1lcm.blob.core.windows.net:443
    uswedpl1catalog.blob.core.windows.net:443
    ```

## <a name="infrastructure-scripts-errors"></a><span data-ttu-id="a0be1-346">インフラストラクチャ スクリプト エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-346">Infrastructure scripts errors</span></span>

### <a name="issue"></a><span data-ttu-id="a0be1-347">出庫</span><span class="sxs-lookup"><span data-stu-id="a0be1-347">Issue</span></span>

<span data-ttu-id="a0be1-348">**エラー:** Test-D365FOConfiguration.ps1 or Test-D365FOConfiguration-AllVMs.ps1 を実行すると、メッセージを受信します:</span><span class="sxs-lookup"><span data-stu-id="a0be1-348">**Error:** When you run Test-D365FOConfiguration.ps1 or Test-D365FOConfiguration-AllVMs.ps1, you receive the message:</span></span>

```stacktrace
"Get-LocalGroupMember : Failed to compare two elements in the array.
At C:\Infrastructure\Scripts\Test-D365FOConfiguration.ps1:79 char:9
+         Get-LocalGroupMember -Group 'Administrators' | `
+         ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Get-LocalGroupMember], InvalidOperationException
    + FullyQualifiedErrorId : An unspecified error occurred.,Microsoft.PowerShell.Commands.GetLocalGroupMemberCommand" 
```

<span data-ttu-id="a0be1-349">**理由:** PowerShell コマンドレット Get-LocalGroupMember にバグがあり、無効なエントリがあると失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-349">**Reason:** There is a bug in the PowerShell commandlet, Get-LocalGroupMember, which causes it to fail when there are entries that not valid.</span></span>

<span data-ttu-id="a0be1-350">**ステップ:** スクリプトが失敗しているマシンで、**ローカル ユーザーとグループ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-350">**Steps:** On the machine where the script is failing, open **local users and groups**.</span></span> <span data-ttu-id="a0be1-351">管理者グループに移動し、次の画像で強調表示されているようなエントリを持つエントリをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-351">Go to the administrators group and remove any entries that have an entry like the one highlighted in the following image.</span></span>

![無効な SID](media/InvalidSID.png)

<span data-ttu-id="a0be1-353">このエラーを受け取ったすべてのマシンでこれを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-353">Do this on all of the machines that receive this error.</span></span> <span data-ttu-id="a0be1-354">変更が完了したら、スクリプトを再実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-354">After the changes are complete, try running the script again.</span></span>

## <a name="restart-applications-such-as-aos"></a><a name="restartapplications"></a><span data-ttu-id="a0be1-355">アプリケーション (AOS など) を再起動</span><span class="sxs-lookup"><span data-stu-id="a0be1-355">Restart applications (such as AOS)</span></span>

<span data-ttu-id="a0be1-356">Service Fabric で、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-356">In Service Fabric, expand **Nodes** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **Code Packages** \> **Code**.</span></span> <span data-ttu-id="a0be1-357">省略記号ボタン (**...**) を選択し、**再起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-357">Select the ellipsis button (**...**), and then select **Restart**.</span></span> <span data-ttu-id="a0be1-358">求められたらコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-358">When you're prompted, enter the code.</span></span>

## <a name="upgrade-service-fabric"></a><span data-ttu-id="a0be1-359">Service Fabric を更新します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-359">Upgrade Service Fabric</span></span>

<span data-ttu-id="a0be1-360">Service Fabric Explorer は次のようなメッセージを表示します:</span><span class="sxs-lookup"><span data-stu-id="a0be1-360">Service Fabric Explorer will show a message that resembles the following message:</span></span>

> <span data-ttu-id="a0be1-361">問題のあるイベント: SourceId=「System.UpgradeOrchestrationService」、プロパティ =「ClusterVersionSupport」、HealthState=「警告」、ConsiderWarningAsError=false。</span><span class="sxs-lookup"><span data-stu-id="a0be1-361">Unhealthy event: SourceId='System.UpgradeOrchestrationService', Property='ClusterVersionSupport', HealthState='Warning', ConsiderWarningAsError=false.</span></span>
<span data-ttu-id="a0be1-362">現在のクラスタ バージョン 6.1.467.9494 のサポートは、5/30/2018 12:00:00 AM に終了します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-362">The current cluster version 6.1.467.9494 support ends 5/30/2018 12:00:00 AM.</span></span> <span data-ttu-id="a0be1-363">Get-ServiceFabricRegisteredClusterCodeVersion を使用して利用可能なアップグレードを表示し、Start-ServiceFabricClusterUpgrade を使用してアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-363">Please view available upgrades using Get-ServiceFabricRegisteredClusterCodeVersion and upgrade using Start-ServiceFabricClusterUpgrade.</span></span>

<span data-ttu-id="a0be1-364">最小要件が 1 つの Microsoft SQL Server Reporting Services (SSRS) ノードと 1 つの Management Reporter ノードであるため、PreUpgradeSafetyCheck をスキップするパラメータを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-364">Because the minimum requirement is one Microsoft SQL Server Reporting Services (SSRS) node and one Management Reporter node, you must pass in a parameter to skip PreUpgradeSafetyCheck.</span></span>

<span data-ttu-id="a0be1-365">Windows PowerShell で Service Fabric をアップグレードするにはこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-365">Follow these steps to upgrade Service Fabric in Windows PowerShell.</span></span>

1. <span data-ttu-id="a0be1-366">Service Fabric Cluster に接続します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-366">Connect to the Service Fabric cluster.</span></span> <span data-ttu-id="a0be1-367">次のコマンドで **123** をサーバー / スター拇印に置き換えて、適切な IP アドレスを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-367">In the following command, replace **123** with the server/star thumbprint, and use the appropriate IP address.</span></span>

    ```powershell
    Connect-ServiceFabricCluster -connectionEndpoint 10.0.0.12:19000 -X509Credential -FindType FindByThumbprint -FindValue 123 -ServerCertThumbprint 123
    ```

2. <span data-ttu-id="a0be1-368">ダウンロードされた最新バージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-368">Get the latest version that was downloaded.</span></span>

    ```powershell
    Get-ServiceFabricRegisteredClusterCodeVersion
    ```

3. <span data-ttu-id="a0be1-369">アップグレードを開始します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-369">Start the upgrade.</span></span> <span data-ttu-id="a0be1-370">**-CodePackageVersion** には、最新バージョンを入力します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-370">For **-CodePackageVersion**, enter the latest version.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0be1-371">**-UpgradeReplicaSetCheckTimeout** は SSRS と Management Reporter の PreUpgradeSafetyCheck をスキップするために使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-371">**-UpgradeReplicaSetCheckTimeout** is used to skip PreUpgradeSafetyCheck for SSRS and Management Reporter.</span></span> <span data-ttu-id="a0be1-372">詳細については、[Service Fabric サービスのアップグレードが動作しない](https://github.com/Azure/service-fabric-issues/issues/595) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-372">For more information, see [Service Fabric service upgrade not working](https://github.com/Azure/service-fabric-issues/issues/595).</span></span> <span data-ttu-id="a0be1-373">**UpgradeDomainTimeoutSec 600 UpgradeTimeoutSec 1800** を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-373">You might also want to use **-UpgradeDomainTimeoutSec 600 -UpgradeTimeoutSec 1800**.</span></span> <span data-ttu-id="a0be1-374">詳細については、[アプリケーション アップグレード パラメーター](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-374">For more information, see [Application upgrade parameters](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-parameters).</span></span>

    ```powershell
    Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion 6.1.472.9494 -Monitored -FailureAction Rollback -UpgradeReplicaSetCheckTimeout 30
    ```

4. <span data-ttu-id="a0be1-375">アップグレードの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-375">Get the upgrade status.</span></span>

    ```powershell
    Get-ServiceFabricClusterUpgrade
    ```

<span data-ttu-id="a0be1-376">詳細については、[アプリケーション アップグレードのトラブルシューティング](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-376">For more information, see [Troubleshoot application upgrades](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-upgrade-troubleshooting).</span></span>

<span data-ttu-id="a0be1-377">新しい Service Fabric リリースの時期については、[Azure Service Fabric チームのブログ](https://blogs.msdn.microsoft.com/azureservicefabric/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-377">To learn when a new Service Fabric release comes out, see the [Azure Service Fabric team blog](https://blogs.msdn.microsoft.com/azureservicefabric/).</span></span>

<span data-ttu-id="a0be1-378">アップグレード後に Service Fabric Explorer で警告が表示された場合は、ノードを記録して、**ノード** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **コード パッケージ** \> **コード** を展開して再起動してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-378">If you receive a warning in Service Fabric Explorer after you upgrade, make a note of the node, and then restart by expanding **Nodes** \> **AOSx** \> **fabric:/AXSF** \> **AXSF** \> **Code Packages** \> **Code**.</span></span> <span data-ttu-id="a0be1-379">省略記号ボタン (**...**) を選択し、**再起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-379">Select the ellipsis button (**...**), and then select **Restart**.</span></span>
 
## <a name="error-unable-to-load-dll-fabricclientdll"></a><span data-ttu-id="a0be1-380">エラー、「DLL 'FabricClient.dll' を読み込むことができません」</span><span class="sxs-lookup"><span data-stu-id="a0be1-380">Error: "Unable to load DLL 'FabricClient.dll'"</span></span>

<span data-ttu-id="a0be1-381">"DLL 'FabricClient.dll' をロードできません" というエラーが表示された場合は、Windows PowerShellを 閉じて再起動してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-381">If you receive an error that states, "Unable to load DLL 'FabricClient.dll'," close and restart Windows PowerShell.</span></span> <span data-ttu-id="a0be1-382">エラーが引き続き発生する場合は、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-382">If the error persists, restart the machine.</span></span>

## <a name="what-cluster-id-should-be-used-in-the-agent-configuration"></a><span data-ttu-id="a0be1-383">エージェント コンフィギュレーションでどのようなクラスター ID を使用する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="a0be1-383">What cluster ID should be used in the agent configuration?</span></span>

<span data-ttu-id="a0be1-384">クラスタ ID は、任意のグローバル一意識別子 (GUID) です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-384">The cluster ID can be any globally unique identifier (GUID).</span></span> <span data-ttu-id="a0be1-385">この GUID は、追跡目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-385">This GUID is used for tracking purposes.</span></span>

## <a name="encryption-errors"></a><span data-ttu-id="a0be1-386">暗号化エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-386">Encryption errors</span></span>

<span data-ttu-id="a0be1-387">暗号化エラーの例は "AXBootstrapperAppType"、"Bootstrapper"、"AXDiagnostics"、"RTGatewayAppType"、"ゲートウェイの潜在的なエラー関連"、 "Microsoft.D365.Gateways.ClusterGateway.exe" を含みます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-387">Some examples of encryption errors include "AXBootstrapperAppType," "Bootstrapper," "AXDiagnostics," "RTGatewayAppType," "Gateway potential failure related," and "Microsoft.D365.Gateways.ClusterGateway.exe."</span></span>

<span data-ttu-id="a0be1-388">AOS アカウント パスワードを暗号化するために使用されたデータ暗号化証明書がマシンにインストールされていない場合、これらのエラーのいずれかが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-388">You might receive one of these errors if the data encipherment certificate that was used to encrypt the AOS account password wasn't installed on the machine.</span></span> <span data-ttu-id="a0be1-389">この証明書が証明書 (ローカル コンピューター) に含まれているか、プロバイダーの種類が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-389">This certificate might be in the certificates (local computer), or the provider type might be incorrect.</span></span>

<span data-ttu-id="a0be1-390">エラーを解決するには、credentials.json ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-390">To resolve the error, validate the credentials.json file.</span></span> <span data-ttu-id="a0be1-391">次のコマンドを (AOS1 上で) 入力することにより、テキストが正しく復号化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-391">Verify that the text is correctly decrypted by entering the following command (on AOS1).</span></span>

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="a0be1-392">このエラーも、**''** パラメーターが ApplicationManifest ファイルで定義されていない場合にも発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-392">This error can also occur if the **''** parameter isn't defined in the ApplicationManifest file.</span></span> <span data-ttu-id="a0be1-393">イベント ビューアーで、このパラメータが定義されているどうかを確認するには、**カスタム ビュー** \> **管理イベント** の順に移動し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-393">To determine whether this parameter is defined, in Event Viewer, go to **Custom Views** \> **Administrative Events**, and verify the following information:</span></span>

- <span data-ttu-id="a0be1-394">Credentials.json ファイルの資格情報の暗号化には、正しいレイアウト/構造があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-394">The encrypt credentials for the credentials.json file have the correct layout/structure.</span></span> <span data-ttu-id="a0be1-395">詳細については、ご使用の環境に適した設定および配置のトピックの「資格情報の暗号化」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-395">For more information, see the "Encrypt credentials" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="a0be1-396">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-396">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#encryptcred)
    - [<span data-ttu-id="a0be1-397">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-397">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#encryptcred)

- <span data-ttu-id="a0be1-398">決算引用符が線の終わりまたは次の線に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-398">A closing quotation mark appears at the end of the line or on the next line.</span></span>

<span data-ttu-id="a0be1-399">イベント ビューアーの **カスタム ビュー** \> **管理イベント** で、**Microsoft-Service Fabric** ソース カテゴリのエラーに注意します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-399">In Event Viewer, under **Custom Views** \> **Administrative Events**, note any errors in the **Microsoft-Service Fabric** source category.</span></span>

## <a name="properties-to-create-a-dataencryption-certificate"></a><span data-ttu-id="a0be1-400">DataEncryption 証明書を作成するためのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0be1-400">Properties to create a DataEncryption certificate</span></span>

<span data-ttu-id="a0be1-401">DataEncryption 証明書を作成するのにには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-401">Use the following properties to create the DataEncryption certificate:</span></span>

- <span data-ttu-id="a0be1-402">**自己署名証明書** – このパラメータは、自己署名証明書を使用する場合にのみ有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-402">**Is self-signed certificate** – Enable this parameter only when you're using self-signed certificates.</span></span>
- <span data-ttu-id="a0be1-403">**証明書の目的** – この証明書のすべての目的を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-403">**Certificate purposes** – Enable all purposes for this certificate.</span></span>
- <span data-ttu-id="a0be1-404">**署名アルゴリズム** – **sha256RSA** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-404">**Signature algorithm** – Specify **sha256RSA**.</span></span>
- <span data-ttu-id="a0be1-405">**署名ハッシュ アルゴリズム** – **sha256** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-405">**Signature hash algorithm** – Specify **sha256**.</span></span>
- <span data-ttu-id="a0be1-406">**発行者** – 指定 **CN = DataEncryptionCertificate**。</span><span class="sxs-lookup"><span data-stu-id="a0be1-406">**Issuer** – Specify **CN = DataEncryptionCertificate**.</span></span>
- <span data-ttu-id="a0be1-407">**公開キー** – **RSA (2048 ビット)** を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-407">**Public Key** – Specify **RSA (2048 bits)**.</span></span>
- <span data-ttu-id="a0be1-408">**Thumbprint アルゴリズム** – **sha1** を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-408">**Thumbprint algorithm** – Specify **sha1**.</span></span>

> [!WARNING]
> <span data-ttu-id="a0be1-409">実稼働環境では、自己署名証明書を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-409">Don't use self-signed certificates in production environments.</span></span> <span data-ttu-id="a0be1-410">代わりに、証明書機関によって発行された証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-410">Instead, use certificates that are issued by certificate authorities.</span></span>

## <a name="the-certificate-and-private-key-that-should-be-used-for-decryption-cant-be-found-0x8009200c"></a><span data-ttu-id="a0be1-411">暗号の解読に使用すべき証明書と秘密キーを見つけることができません (0x8009200C)</span><span class="sxs-lookup"><span data-stu-id="a0be1-411">The certificate and private key that should be used for decryption can't be found (0x8009200C)</span></span>

<span data-ttu-id="a0be1-412">証明書 や ACL が見つからない、拇印の入力が間違っている場合は、特殊文字を確認し、C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt で拇印を検索してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-412">If you're missing a certificate and ACL, or if you have the wrong thumbprint entry, check for special characters, and look for thumbprints in C:\\ProgramData\\SF\\\<AOSMachineName\>\\Fabric\\work\\Applications\\AXBootstrapperAppType\_App\<N\>\\log\\ConfigureCertificates-\<timestamp\>.txt.</span></span>

<span data-ttu-id="a0be1-413">次のコマンドを使用して暗号化されたテキストを検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-413">You can also validate the encrypted text by using the following command.</span></span>

```powershell
Invoke-ServiceFabricDecryptText -CipherText 'longstring' -StoreLocation LocalMachine | Set-Clipboard
```

<span data-ttu-id="a0be1-414">「暗号の解読に使用する証明書と秘密キーを見つけることができません」というメッセージを受信した場合は、axdataenciphermentcert と svc-AXSF$ AXServiceUser ACLs を確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-414">If you receive the message, "Cannot find the certificate and private key to use for decryption," verify the axdataenciphermentcert and svc-AXSF$ AXServiceUser ACLs.</span></span>

<span data-ttu-id="a0be1-415">credentials.json ファイルが変更された場合、実行する必要のあるアクションは、LCS の環境ステータスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-415">If the credentials.json file has changed, the action you should take depends on the status of the environment in LCS.</span></span>

- <span data-ttu-id="a0be1-416">環境が LCS に配置されている場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-416">If your environment appears to be deployed in LCS, do the following:</span></span>
    1. <span data-ttu-id="a0be1-417">環境ページに移動して、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-417">Go to your environment page and select **Maintain**.</span></span>
    1. <span data-ttu-id="a0be1-418">**更新プログラムの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-418">Select **Update settings**.</span></span>
    1. <span data-ttu-id="a0be1-419">設定は変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-419">Do not change any settings.</span></span> <span data-ttu-id="a0be1-420">**準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-420">Select **Prepare**.</span></span>
    1. <span data-ttu-id="a0be1-421">数分後に環境が準備されたら、**配置** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-421">After a few minutes your environment will be prepared and you can select **Deploy**.</span></span>

- <span data-ttu-id="a0be1-422">LCS で環境が失敗状態の場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-422">If your environment is in a failed state in LCS, do the following:</span></span>
    1. <span data-ttu-id="a0be1-423">**再試行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-423">Select **Retry**.</span></span> <span data-ttu-id="a0be1-424">新しい Credentials.json ファイルは、再試行操作中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-424">The new Credentials.json file will be used during the retry operation.</span></span>

<span data-ttu-id="a0be1-425">上記のソリューションのいずれも機能しない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-425">If none of the preceding solutions work, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-426">ConfigTemplate.xml ファイルで指定されたドメイン名と Active Directory アカウント名が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-426">Verify that the domain name and Active Directory account names that are specified in the ConfigTemplate.xml file are correct.</span></span>
2. <span data-ttu-id="a0be1-427">用意されたスクリプトを使用して証明書が生成されなかった場合に ConfigTemplate.xml ファイルで指定された拇印が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-427">Verify that the thumbprints that are specified in the ConfigTemplate.xml file are correct if the certificate wasn't generated by using the scripts that are provided.</span></span>
3. <span data-ttu-id="a0be1-428">LCS で指定された証明書の拇印が正しく、ConfigTemplate.xml で指定されたものと拇印が一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-428">Verify that the certificate thumbprints that are specified in LCS are correct, and that they match the thumbprints that are specified in ConfigTemplate.xml.</span></span> <span data-ttu-id="a0be1-429">特殊文字がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-429">Make sure that there are no special characters.</span></span> <span data-ttu-id="a0be1-430">**.\\Get-DeploymentSettings.ps1** を実行して、コピーしやすい方法で拇印を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-430">You can run **.\\Get-DeploymentSettings.ps1** to obtain the thumbprints in an easy-to-copy manner.</span></span>
4. <span data-ttu-id="a0be1-431">証明書が自己生成されない場合、プロバイダー名が次の証明書タイプと一致することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-431">If the certificates aren't self-generated, make sure that the provider names match for the following certificate types:</span></span>

    - <span data-ttu-id="a0be1-432">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span><span class="sxs-lookup"><span data-stu-id="a0be1-432">**ServiceFabricEncryption type:** Microsoft Enhanced Cryptographic Provider v1.0</span></span>
    - <span data-ttu-id="a0be1-433">**その他のすべての証明書タイプ:** Microsoft の拡張された RSA および AES 暗号化プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a0be1-433">**All other certificate types:** Microsoft Enhanced RSA and AES Cryptographic Provider</span></span>

5. <span data-ttu-id="a0be1-434">Set-CertificateAcls.ps1 および Test-D365FOConfiguration.ps1 スクリプトがすべての Service Fabric マシンで正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-434">Verify that the Set-CertificateAcls.ps1 and Test-D365FOConfiguration.ps1 scripts were successfully run on all Service Fabric machines.</span></span>
6. <span data-ttu-id="a0be1-435">Credentials.json ファイルが存在し、エントリが適切な値に復号化されるよう確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-435">Verify that the credentials.json file exists, and that the entries are decrypted to correct values.</span></span>

    <span data-ttu-id="a0be1-436">AOS マシンのいずれかで、データの暗号化証明書が正しいことを確認する次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-436">On one of the AOS machines, run the following command to verify that the data encryption certificate is correct.</span></span>

    ```powershell
    Invoke-ServiceFabricDecryptText '<encrypted string>' -StoreLocation LocalMachine
    ```

7. <span data-ttu-id="a0be1-437">いずれかの証明書を変更する必要がある場合、もしくは構成が正しくない場合は、次の手順を実行してください:</span><span class="sxs-lookup"><span data-stu-id="a0be1-437">If any of the certificates must be changed, or if the configuration was incorrect, follow these steps:</span></span>

    1. <span data-ttu-id="a0be1-438">**ConfigTemplate.xml** ファイルを編集して、正しい値が出るようにします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-438">Edit the **ConfigTemplate.xml** file so that it has the correct values.</span></span>
    2. <span data-ttu-id="a0be1-439">すべてのセットアップ スクリプトと **Test-D365FOConfiguration** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-439">Run all the setup scripts and the **Test-D365FOConfiguration** script.</span></span>

8. <span data-ttu-id="a0be1-440">LCS で環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-440">In LCS, reconfigure the environment.</span></span>

## <a name="gateway-fails-to-deploy"></a><span data-ttu-id="a0be1-441">ゲートウェイで配置に失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-441">Gateway fails to deploy</span></span>

<span data-ttu-id="a0be1-442">**問題:** イベント ビューアー ログに次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-442">**Issue:** You receive the following error in the event viewer logs.</span></span>

```stacktrace
Message Module aos failed Detail System.InvalidOperationException: Gateway app and Bootstrapper app are not healthy at AOSSetupHybridCloud.Program.Main(String[] args) 
at System.AppDomain._nExecuteAssembly(RuntimeAssembly assembly, String[] args) 
at System.AppDomain.ExecuteAssembly(String assemblyFile, String[] args) 
at System.AppDomain.ExecuteAssembly(String assemblyFile, String[] args) 
at SetupCore.SetupManager.LaunchProcessInAppDomain(String startupExe, String workingDir, String currentFolder, String[] moduleArgs) 
at SetupCore.SetupManager.<>c__DisplayClass12_1.<InvokeModules>b__6()
```

<span data-ttu-id="a0be1-443">ゲートウェイ アプリケーションの SFExplorer には、次のエラー メッセージも表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-443">You also receive the following error message in the SFExplorer for the Gateway application.</span></span>

```stacktrace
'System.RA' reported Warning for property 'ReplicaOpenStatus'.
Replica had multiple failures during open on AOS_13. API call: IStatelessServiceInstance.Open(); Error = System.InvalidOperationException (-2146233079)
Category does not exist.
   at System.Diagnostics.PerformanceCounterLib.CounterExists(String machine, String category, String counter)
   at System.Diagnostics.PerformanceCounter.InitializeImpl()
   at System.Diagnostics.PerformanceCounter..ctor(String categoryName, String counterName, String instanceName, Boolean readOnly)
   at System.Diagnostics.PerformanceCounter..ctor(String categoryName, String counterName, String instanceName)
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.Helpers.CpuPerfCounter..ctor()
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.GzipContentDelegatingHandler..ctor()
   at Microsoft.Dynamics.LBD.Gateways.ClusterGateway.ClusterGateway.ConfigureApp(IAppBuilder appBuilder)
   at Microsoft.Owin.Hosting.Engine.HostingEngine.Start(StartContext context)
   at Microsoft.Dynamics.LBD.Gateways.Common.OwinCommunicationListener.b__9_0()
   at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.d__10`2.MoveNext()
```

<span data-ttu-id="a0be1-444">**理由:** ゲートウェイで必要となるパフォーマンス カウンターへのポインターが破損している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-444">**Reason:** The pointers to the performance counter that the gateway needs may be corrupt.</span></span>

<span data-ttu-id="a0be1-445">**解決 :** ゲートウェイが正常でないすべての AOS ノードの、管理者として実行されているコマンド プロンプト ウインドウで **lodctr /R** を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-445">**Resolution:** Run **lodctr /R** in a Command Prompt window that you open as administrator in all AOS nodes where the gateway is unhealthy.</span></span> <span data-ttu-id="a0be1-446">パフォーマンス カウンターを再構築できないことを示すエラーメッセージが表示された場合は、コマンドを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-446">If you receive an error message that states that the performance counters can't be rebuilt, try to run the command again.</span></span> 

## <a name="management-reporter"></a><span data-ttu-id="a0be1-447">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="a0be1-447">Management Reporter</span></span>

<span data-ttu-id="a0be1-448">追加のログは、プロバイダーを登録することで実行できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-448">Additional logging can be done by registering providers.</span></span> <span data-ttu-id="a0be1-449">[ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) を **プライマリ** オーケストレータ マシン にダウンロードし、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-449">Download [ETWManifest.zip](https://go.microsoft.com/fwlink/?linkid=864672) to the **primary** orchestrator machine, and then run the following commands.</span></span> <span data-ttu-id="a0be1-450">プライマリ インスタンスであるマシンを判別するには、Service Fabric Explorerで、**クラスター** \> **アプリケーション** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-450">To determine which machine is the primary instance, in Service Fabric Explorer, expand **Cluster** \> **Applications** \> **LocalAgentType** \> **fabric:/LocalAgent/OrchestrationService** \> **(GUID)**.</span></span>

> [!NOTE]
> <span data-ttu-id="a0be1-451">イベント ビューアーの結果が正しく表示されない場合 (たとえば、単語が切り詰められた場合など)、最新のマニフェストおよび .dll ファイルを取得してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-451">If results in Event Viewer don't appear correct (for example, if words are truncated), get the latest manifest and .dll files.</span></span> <span data-ttu-id="a0be1-452">最新のマニフェストと .dll ファイルを取得するには、エージェント ファイル共有の WP フォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-452">To get the latest manifest and .dll files, go to the WP folder in the agent file share.</span></span> <span data-ttu-id="a0be1-453">この共有は、適切な設定の「ファイル ストレージの設定」セクション、および環境の配置トピックで作成されました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-453">This share was created in the "Set up file storage" section of the appropriate setup and deployment topic for your environment:</span></span>
> 
> - [<span data-ttu-id="a0be1-454">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-454">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupfile)
> - [<span data-ttu-id="a0be1-455">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-455">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupfile)
> 
> <span data-ttu-id="a0be1-456">**例:** \[*エージェント共有*\]\\wp\\\[*配置名*\]\\StandaloneSetup-...\\アプリ\\ ETWManifests</span><span class="sxs-lookup"><span data-stu-id="a0be1-456">**Example:** \[*Agent Share*\]\\wp\\\[*Deployment name*\]\\StandaloneSetup-...\\Apps\\ETWManifests</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"}
```

<span data-ttu-id="a0be1-457">プロバイダーの登録を解除する必要がある場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-457">If you must unregister providers, use the following command.</span></span>

```powershell
.\RegisterETW.ps1 -ManifestsAndDll @{"C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.man" = "C:\Files\ETWManifest\Microsoft.Dynamics.Reporting.Instrumentation.dll"} -Unregister
```

<span data-ttu-id="a0be1-458">プロバイダーが登録されると、新しい配置についての追加詳細は **アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** でイベント ビューアーにログインされます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-458">After providers are registered, additional details about the new deployment are logged in Event Viewer, at **Applications and Services Logs** \> **Microsoft** \> **Dynamics**.</span></span> <span data-ttu-id="a0be1-459">次のフォルダが表示されます:</span><span class="sxs-lookup"><span data-stu-id="a0be1-459">The following folders will be shown:</span></span>

- <span data-ttu-id="a0be1-460">MR-Logger</span><span class="sxs-lookup"><span data-stu-id="a0be1-460">MR-Logger</span></span>
- <span data-ttu-id="a0be1-461">MR-Sql</span><span class="sxs-lookup"><span data-stu-id="a0be1-461">MR-Sql</span></span>

<span data-ttu-id="a0be1-462">新しいフォルダーを表示するには、イベント ビューアーを終了して、再表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-462">To see the new folders, you must close and reopen Event Viewer.</span></span> <span data-ttu-id="a0be1-463">追加の詳細を表示するには、もう一度環境を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-463">To see additional details, you must deploy an environment again.</span></span>

###  <a name="could-not-load-file-or-assembly-entityframework"></a><a name="FREntityFramework"></a> <span data-ttu-id="a0be1-464">ファイルまたはアセンブリ EntityFramework を読み込めませんでした</span><span class="sxs-lookup"><span data-stu-id="a0be1-464">Could not load file or assembly EntityFramework</span></span>

<span data-ttu-id="a0be1-465">**問題**: ローカル エージェント バージョン 2.3.1 以降を実行していて、プラットフォーム更新プログラム 29 またはそれ以前を含むパッケージを展開しているときに、イベント ログで次の stacktrace を受け取りました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-465">**Issue**: You are running Local Agent version 2.3.1 or later and you received the following stacktrace in the event logs while deploying a package that contains Platform update 29 or earlier:</span></span>

```stacktrace
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation. --->
System.IO.FileNotFoundException: Could not load file or assembly 'EntityFramework, Version=6.0.0.0,
Culture=neutral, PublicKeyToken=b77a5c561934e089' or one of its dependencies. The system cannot find the file
specified. at Microsoft.Dynamics.Integration.Service.Utility.AdapterProvider.RefreshAdapters()
--- End of inner exception stack trace ---
 ```

<span data-ttu-id="a0be1-466">**解決策**: TSG\_UpdateFRDeployerConfig.ps1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-466">**Resolution:** Use TSG\_UpdateFRDeployerConfig.ps1.</span></span> <span data-ttu-id="a0be1-467">詳細については、[TSG_UpdateFRDeployerConfig.ps1](onprem-tsg-implementations.md#frdeployer)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-467">For more information, see [TSG_UpdateFRDeployerConfig.ps1](onprem-tsg-implementations.md#frdeployer).</span></span>

### <a name="unable-to-deploy-financial-reporting-service"></a><span data-ttu-id="a0be1-468">財務報告サービスを配置できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-468">Unable to deploy Financial Reporting Service</span></span>

<span data-ttu-id="a0be1-469">**問題:** 次のエラーが Service Fabric のアプリケーション ログにあるため、財務報告に対するプラットフォーム更新プログラム 26 以降の配置を完了できません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-469">**Issue:** You are unable to finish deployment of Platform update 26 and later for Financial Reporting because the following error is in the application log for Service Fabric.</span></span>

```stacktrace
Application: FinancialReportingDeployer.exe Framework Version: v4.0.30319  
Description: The process was terminated due to an unhandled exception. 
Exception  Info: System.DllNotFoundException at  
Microsoft.Cloud.InstrumentationFramework.NativeIfxInterop.InitializeIfxFromCloudAgentConfigureSamplingAndTracing_x64(System.String,  System.String, UInt32, UInt32, Boolean) at  Microsoft.Cloud.InstrumentationFramework.IfxInitializer.IfxInitialize(System.String,  Microsoft.Cloud.InstrumentationFramework.InstrumentationSpecification,  Microsoft.Cloud.InstrumentationFramework.AuditSpecification) at  Microsoft.Dynamics.Performance.Logger.IfxLogger..cctor() Exception Info:  System.TypeInitializationException at  
Microsoft.Dynamics.Performance.Logger.IfxLogger..ctor(System.String,  Microsoft.Dynamics.Performance.Logger.IfxLoggerOptions) at  
Microsoft.Dynamics.Performance.Logger.IfxLoggerProvider.CreateLogger(System.String)  at  
Microsoft.Extensions.Logging.Logger..ctor(Microsoft.Extensions.Logging.LoggerFactory,  System.String) at  
```

<span data-ttu-id="a0be1-470">**理由:** Visual Studio 2013 の Microsoft Visual C++ 再頒布可能パッケージが正しくインストールされていないか、MR ノードの一部またはすべてが破損しています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-470">**Reason:** The Microsoft Visual C++ Redistributable Package for Visual Studio 2013 was not correctly installed or is corrupt in some or all of the MR nodes.</span></span>

<span data-ttu-id="a0be1-471">**手順:** Visual Studio 2013 の Microsoft Visual C++ 再頒布可能パッケージのインストールを再実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-471">**Steps:** Re-run the installation of the Microsoft Visual C++ Redistributable Package for Visual Studio 2013.</span></span>

### <a name="an-error-occurs-while-addaxdatabasechangetracking-is-running"></a><span data-ttu-id="a0be1-472">AddAXDatabaseChangeTracking の実行中に発生するエラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-472">An error occurs while AddAXDatabaseChangeTracking is running</span></span>

<span data-ttu-id="a0be1-473">Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet) で AddAXDatabaseChangeTracking を実行しているときにエラーが発生した場合は、フル パスが正しいことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-473">If you receive an error while you run AddAXDatabaseChangeTracking at Microsoft.Dynamics.Performance.Deployment.FinancialReportingDeployer.Utility.InvokeCmdletAndValidateSuccess(DeploymentCmdlet cmdlet), verify that the full path is correct.</span></span> <span data-ttu-id="a0be1-474">フル パスの例は **ax.d365ffo.onprem.contoso.com** です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-474">An example of a full path is **ax.d365ffo.onprem.contoso.com**.</span></span>

<span data-ttu-id="a0be1-475">スター証明書での問題が原因でエラーが発生する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-475">The error might also occur because of an issue with the star certificate.</span></span> <span data-ttu-id="a0be1-476">たとえば、リモート証明書 CN=\*.d365ffo.onprem.contoso.com には、無効な、またはホストの ax.d365ffo.onprem.contoso.com と一致しない名前があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-476">For example, the remote certificate CN=\*.d365ffo.onprem.contoso.com has a name that isn't valid or that doesn't match the host, ax.d365ffo.onprem.contoso.com.</span></span>

### <a name="run-the-initialize-database-script-and-validate-that-databases-have-correct-users"></a><span data-ttu-id="a0be1-477">データベース初期化スクリプトを実行し、データベースのユーザーが適切であることを検証</span><span class="sxs-lookup"><span data-stu-id="a0be1-477">Run the initialize database script, and validate that databases have correct users</span></span>

<span data-ttu-id="a0be1-478">AddAXDatabaseChangeTracking イベントのみを受け取った場合は、`https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService` にアクセスし、Finance + Operations の MetadataService サービスにアクセスしてみてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-478">If you receive only the AddAXDatabaseChangeTracking event, try to reach the MetadataService service for Finance + Operations by going to `https://ax.d365ffo.contoso.com/namespaces/AXSF/services/MetadataService`.</span></span>

<span data-ttu-id="a0be1-479">次に、wif.config ファイルでサービスの証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-479">Next, check the certificates of the service in the wif.config file.</span></span> <span data-ttu-id="a0be1-480">ファイルを検索するには、AOS マシンにサインインし、タスク マネージャーで **AxService.exe** を探してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-480">To find the file, sign in to one of the AOS machines, and then, in Task Manager, find **AxService.exe**.</span></span> <span data-ttu-id="a0be1-481">TimeZonePatcherを右クリックし、 **ファイルの場所を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-481">Right-click, and select **Open file location**.</span></span> <span data-ttu-id="a0be1-482">wif.config ファイルでは、3 つの拇印を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-482">In the wif.config file, you should see three thumbprints.</span></span> <span data-ttu-id="a0be1-483">これらの拇印に関する次の要件に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-483">Note the following requirements for these thumbprints:</span></span>

- <span data-ttu-id="a0be1-484">これらは異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-484">They must be different.</span></span>
- <span data-ttu-id="a0be1-485">これらは、この順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-485">They must be in this order:</span></span>

    1. <span data-ttu-id="a0be1-486">Financialreportingの拇印</span><span class="sxs-lookup"><span data-stu-id="a0be1-486">Financialreporting thumbprint</span></span>
    2. <span data-ttu-id="a0be1-487">ReportingServiceの拇印</span><span class="sxs-lookup"><span data-stu-id="a0be1-487">ReportingService thumbprint</span></span>
    3. <span data-ttu-id="a0be1-488">SessionAuthenticationの拇印</span><span class="sxs-lookup"><span data-stu-id="a0be1-488">SessionAuthentication thumbprint</span></span>

<span data-ttu-id="a0be1-489">拇印がこれらの要件の両方を満たしていない場合は、正しい拇印を使用して LCS から再配置をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-489">If the thumbprints don't meet both these requirements, you must redeploy from LCS by using correct thumbprints.</span></span>

### <a name="the-remote-name-cant-be-resolved"></a><span data-ttu-id="a0be1-490">リモート名を解決できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-490">The remote name can't be resolved</span></span>

<span data-ttu-id="a0be1-491">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-491">**Error:**</span></span>

> <span data-ttu-id="a0be1-492">リモート名を解決できませんでした。'x.d365fo.onprem.contoso.com' / メッセージを承認できなかった `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` をリッスンしていたエンドポイントはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0be1-492">The remote name could not be resolved: 'x.d365fo.onprem.contoso.com' / There was no endpoint listening at `https://x.d365fo.onprem.contoso.com/namespaces/AXSF/services/MetadataService` that could accept the message.</span></span>

<span data-ttu-id="a0be1-493">**理由:** この問題は、通常正しくないアドレスまたは SOAP アクションによって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-493">**Reason:** This issue is often caused by an incorrect address or SOAP action.</span></span>

<span data-ttu-id="a0be1-494">**手順:** URL を手動で開き、アドレスにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-494">**Steps:** Verify that the address can be reached, by manually opening the URL.</span></span> <span data-ttu-id="a0be1-495">詳細については、イベント ビューアーで "InnerException" のテキストが存在するかどうか確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-495">For more details, see the "InnerException" text in the Event Viewer, if it's present.</span></span>

### <a name="error-on-importdefaultreports"></a><span data-ttu-id="a0be1-496">ImportDefaultReports のエラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-496">Error on ImportDefaultReports</span></span>

<span data-ttu-id="a0be1-497">配置中に Management Reporter レポートがチェックアウトされると、配置処理は失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-497">If Management Reporter reports are checked out during deployment, the deployment will fail.</span></span> <span data-ttu-id="a0be1-498">レポートがチェック アウトされているかどうかを表示するには、FinancialReporting データベースで次の **選択** 明細書を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-498">To see whether reports are checked out, run the following **select** statements on the FinancialReporting database.</span></span>

```sql
select checkedoutto, * from Reporting.ControlReport where checkedoutto is not null
select checkedoutto, * from Reporting.ControlRowMaster where checkedoutto is not null
select checkedoutto, * from Reporting.ControlColumnMaster where checkedoutto is not null
```

<span data-ttu-id="a0be1-499">どのユーザーがオブジェクトをチェック アウトするかを知るには、次の **選択** ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-499">To learn which user has objects checked out, you can run the following **select** statement.</span></span>

```sql
select * from Reporting.SecurityUser where UserID = ''
```

<span data-ttu-id="a0be1-500">この問題を手動で解決するには、以下のテーブルを次のコマンドを使用して更新し、 **checkedoutto** を **null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-500">To resolve this issue manually, update the following tables, and set **checkedoutto** to **null** by using the following commands.</span></span>

```sql
update Reporting.ControlReport set checkedoutto = null where checkedoutto is not null
update Reporting.ControlRowMaster set checkedoutto = null where checkedoutto is not null
update Reporting.ControlColumnMaster set checkedoutto = null where checkedoutto is not null
```

## <a name="axdbadmin-cant-connect-to-the-database-server-sql-lscontosocom"></a><span data-ttu-id="a0be1-501">axdbadmin は SQL-LS.contoso.com データベース サーバーに接続することができません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-501">axdbadmin can't connect to the database server SQL-LS.contoso.com</span></span>

<span data-ttu-id="a0be1-502">**理由:** AXDB データベースに接続するためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-502">**Reason:** The user doesn't have permission to connect to the AXDB database.</span></span>

<span data-ttu-id="a0be1-503">**ステップ:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-503">**Steps:**</span></span>

1. <span data-ttu-id="a0be1-504">既に存在する場合は、データベースから axdbadmin ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-504">Remove the axdbadmin user from the database, if it already exists.</span></span>
2. <span data-ttu-id="a0be1-505">**ConfigTemplate.xml** ファイルで、AXDB データベースに追加する必要があるユーザー名を指定してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-505">In the **ConfigTemplate.xml** file, specify the user name that must be added to the AXDB database.</span></span>

    ```xml
    <Security>
        <User refName="axdbadmin" type="SqlUser" userName="axdbadmin" />
    </Security>
    ```

3. <span data-ttu-id="a0be1-506">axdbadmin ユーザーを追加するには、もう一度初期化データベース スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-506">Run the initialize database script again to add the axdbadmin user.</span></span>

## <a name="unable-to-resolve-the-xpath-value"></a><span data-ttu-id="a0be1-507">xPath 値を解決することができません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-507">Unable to resolve the xPath value</span></span>

<span data-ttu-id="a0be1-508">予想される動作では、次の **xPath** 値を解決することはできません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-508">In the expected behavior, the following **xPath** value can't be resolved:</span></span> 

<span data-ttu-id="a0be1-509">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span><span class="sxs-lookup"><span data-stu-id="a0be1-509">\[TopologyInstance/CustomizationGroup\[@name='ServiceConfiguration'\]/Group\[@name='AOSServicePrincipalUser'\]/Customizations/Customization\[@fieldName='PrincipalUserAccountPassword'\]/@selectedValue</span></span>

<span data-ttu-id="a0be1-510">したがって、 **xPath** の値が解決できないことは問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-510">Therefore, the fact that the **xPath** value can't be resolved isn't an issue.</span></span> <span data-ttu-id="a0be1-511">**xPath** 値は、AOS ランタイム ユーザーの情報を検索します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-511">The **xPath** value looks for AOS runtime user information.</span></span> <span data-ttu-id="a0be1-512">ただし、セキュリティが統合されているため、その情報は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-512">However, because of integrated security, that information isn't required.</span></span> <span data-ttu-id="a0be1-513">別の理由でエラーを調査する必要がある場合は、 **xPath** の値を解決できないと通知されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-513">The fact that the **xPath** value can't be resolved is communicated in case the failure must be investigated for another reason.</span></span>

## <a name="ad-fs"></a><span data-ttu-id="a0be1-514">AD FS</span><span class="sxs-lookup"><span data-stu-id="a0be1-514">AD FS</span></span>

### <a name="the-sign-in-page-doesnt-redirect-you"></a><span data-ttu-id="a0be1-515">サインイン ページにリダイレクトされません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-515">The sign-in page doesn't redirect you</span></span>

<span data-ttu-id="a0be1-516">サインイン ページにはリダイレクトされない可能性がありますが、資格情報の確認を続行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-516">The sign-in page might not redirect you but continues to prompt for credentials.</span></span> <span data-ttu-id="a0be1-517">また、リダイレクトの可能性がありますが、次のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-517">Alternatively, you might be redirected but receive the following message:</span></span>

> <span data-ttu-id="a0be1-518">エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-518">An error occurred.</span></span> <span data-ttu-id="a0be1-519">詳細については、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-519">Contact your administrator for more information.</span></span>

<span data-ttu-id="a0be1-520">そのような場合、問題を解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-520">In these cases, you can follow these steps to resolve the issue:</span></span>

- <span data-ttu-id="a0be1-521">AD FS リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-521">Add the AD FS link to the list of trusted sites.</span></span>
- <span data-ttu-id="a0be1-522">Dynamics 365 リンクを信頼されているサイトの一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-522">Add the Dynamics 365 link to the list of trusted sites.</span></span>
- <span data-ttu-id="a0be1-523">末尾にスラッシュ「/」を追加し、動作が変更されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-523">Add a trailing slash (/), and see whether the behavior changes.</span></span>

<span data-ttu-id="a0be1-524">**ADFS** \> **アプリケーション グループ** の順に移動して、AD FS マネージャーを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-524">Verify the AD FS Manager by going to **ADFS** \> **Application groups**.</span></span> <span data-ttu-id="a0be1-525">**Microsoft Dynamics 365 for Operations オンプレミス** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-525">Double-click **Microsoft Dynamics 365 for Operations on-premises**.</span></span> <span data-ttu-id="a0be1-526">その後、**ネイティブ アプリケーション** で、**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-526">Then, under **Native application**, double-click **Microsoft Dynamics 365 for Operations on-premises - Native application**.</span></span>

<span data-ttu-id="a0be1-527">**リダイレクト URI** 値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-527">Note the **Redirect URI** value.</span></span> <span data-ttu-id="a0be1-528">Finance + Operations の DNS 前方参照ゾーンに一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-528">It should match the DNS forward lookup zone for Finance + Operations.</span></span>

### <a name="error-could-not-establish-trust-relationship-for-the-ssltls-secure-channel"></a><span data-ttu-id="a0be1-529">エラー、「SSL/TLS セキュリティ チャネルの信頼関係を確立できませんでした」</span><span class="sxs-lookup"><span data-stu-id="a0be1-529">Error: "Could not establish trust relationship for the SSL/TLS secure channel"</span></span>

<span data-ttu-id="a0be1-530">「SSL/TLS のセキュリティで保護されているチャネルに対する信頼関係を確立できませんでした」というエラーが表示された場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-530">If you receive an error that states, "Could not establish trust relationship for the SSL/TLS secure channel," follow these steps.</span></span>

1. <span data-ttu-id="a0be1-531">Service Fabric で、**クラスタ** \> **アプリケーション** \> **AXSFType** \> **fabric:/AXSF** の順に移動し、**詳細** タブでスクロールし、**Aad\_AADMetadataLocationFormat** および **Aad\_FederationMetadataLocation** の URL に注意します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-531">In Service Fabric, go to **Cluster** \> **Applications** \> **AXSFType** \> **fabric:/AXSF**, and then, on the **Details** tab, scroll down and note the URLs for **Aad\_AADMetadataLocationFormat** and **Aad\_FederationMetadataLocation**.</span></span>
2. <span data-ttu-id="a0be1-532">AOS からそれらの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-532">Browse to those URLs from AOS.</span></span>
3. <span data-ttu-id="a0be1-533">詳細については、AOS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-533">On the AOS machine, in Event Viewer, go to **Applications and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-SystemRuntime** for details.</span></span>
4. <span data-ttu-id="a0be1-534">AD FS 証明書が信頼されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-534">Verify that the AD FS certificate is trusted:</span></span>

    1. <span data-ttu-id="a0be1-535">AD FS 証明書を確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-535">Verify the AD FS certificate.</span></span> <span data-ttu-id="a0be1-536">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-536">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management**.</span></span>
    2. <span data-ttu-id="a0be1-537">**AD FS** \> **サービス** \> **証明書** を展開し、証明書を記録しておきます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-537">Expand **AD FS** \> **Service** \> **Certificates**, and make a note of the certificates.</span></span> <span data-ttu-id="a0be1-538">たとえば、1 つの証明書は、dc1.contoso.com の場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-538">For example, one certificate might be dc1.contoso.com.</span></span>
    3. <span data-ttu-id="a0be1-539">AOS マシンの、Microsoft 管理コンソール証明書スナップインで、**証明書 (ローカル コンピューター)** \> **信頼済ルート証明機関** \> **証明書** の順に移動し、AD FS 証明書が一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-539">On the AOS machine, in the Microsoft Management Console Certificates snap-in, go to **Certificates (Local Computer)** \> **Trusted Root Certification Authorities** \> **Certificates**, and verify that the AD FS certificate is listed.</span></span>

<span data-ttu-id="a0be1-540">サイトが安全でないことを示すメッセージが表示された場合は、AD FS の Secure Sockets Layer (SSL) 証明書が信頼済ルート証明機関ストアに追加されていません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-540">If you receive a message that states that the site isn't secure, you haven't added your Secure Sockets Layer (SSL) certificate for AD FS to the Trusted Root Certification Authorities store.</span></span>

### <a name="you-cant-connect-to-the-remote-server-in-some-locations"></a><span data-ttu-id="a0be1-541">一部の地域ではリモート サーバーに接続できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-541">You can't connect to the remote server in some locations</span></span>

<span data-ttu-id="a0be1-542">次の場所でリモート サーバーに接続できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-542">You might not be able to connect to the remote server at the following places:</span></span>

- <span data-ttu-id="a0be1-543">System.Net.HttpWebRequest.GetResponse()</span><span class="sxs-lookup"><span data-stu-id="a0be1-543">System.Net.HttpWebRequest.GetResponse()</span></span>
- <span data-ttu-id="a0be1-544">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span><span class="sxs-lookup"><span data-stu-id="a0be1-544">System.Xml.XmlDownloadManager.GetNonFileStream(Uri uri, ICredentials credentials, IWebProxy proxy, RequestCachePolicy cachePolicy)</span></span>
- <span data-ttu-id="a0be1-545">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span><span class="sxs-lookup"><span data-stu-id="a0be1-545">System.Xml.XmlUrlResolver.GetEntity(Uri absoluteUri, String role, Type ofObjectToReturn)</span></span>

<span data-ttu-id="a0be1-546">この場合は、エラーの受信元である C: \\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\ ログ フォルダーに移動し、出力ファイルを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-546">In this case, go to the C:\\ProgramData\\SF\\AOS\_1\\Fabric\\work\\Applications\\AXSFType\_App35\\log folder where you receive the error, and note the out file.</span></span> <span data-ttu-id="a0be1-547">out ファイルには、次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-547">The out file contains the following information:</span></span>

> <span data-ttu-id="a0be1-548">System.Net.WebException: リモート サーバーに接続できません ---\></span><span class="sxs-lookup"><span data-stu-id="a0be1-548">System.Net.WebException: Unable to connect to the remote server ---\></span></span>
>
> <span data-ttu-id="a0be1-549">System.Net.Sockets.SocketException: 接続した当事者が一定時間適切に応答しなかったため接続試行に失敗したか、接続したホストが x.x.x.x:443 に応答できなかったため確立された接続に失敗しました</span><span class="sxs-lookup"><span data-stu-id="a0be1-549">System.Net.Sockets.SocketException: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond x.x.x.x:443</span></span>

<span data-ttu-id="a0be1-550">Psping を使用してリモート サーバーに対する接続を試みることもできます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-550">You can also use Psping to try to reach the remote server.</span></span> <span data-ttu-id="a0be1-551">Psping の詳細については、[Psping](/sysinternals/downloads/psping) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-551">For information about Psping, see [Psping](/sysinternals/downloads/psping).</span></span>

### <a name="redirect-sign-in-questions-and-issues"></a><span data-ttu-id="a0be1-552">サインイン時の質問および問題をリダイレクト</span><span class="sxs-lookup"><span data-stu-id="a0be1-552">Redirect sign-in questions and issues</span></span>

<span data-ttu-id="a0be1-553">サインイン時に問題が発生した場合は、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-553">If you're having issues when you sign-in, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="a0be1-554">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-554">Here is an example:</span></span>

- <span data-ttu-id="a0be1-555">**プロビジョニング \_AdminPrincipalName**: `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="a0be1-555">**Provisioning\_AdminPrincipalName**: `AXServiceUser@contoso.com`</span></span>
- <span data-ttu-id="a0be1-556">**プロビジョニング\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="a0be1-556">**Provisioning\_AdminIdentityProvider**: `https://DC1.contoso.com/adfs`</span></span>

<span data-ttu-id="a0be1-557">値が有効でない場合は、処理を続行できず、LCS から再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-557">If the values aren't valid, you won't be able to proceed, and you must redeploy from LCS.</span></span>

<span data-ttu-id="a0be1-558">Reset-DatabaseUsers.ps1 を使用した場合、変更内容を有効にする前に、Dynamics サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-558">If you used Reset-DatabaseUsers.ps1, you must restart the Dynamics Service before your changes take effect.</span></span> <span data-ttu-id="a0be1-559">引き続きサインインの問題がある場合は、USERINFO テーブルで、**NETWORKDOMAIN** および **NETWORKALIAS** の値を記録してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-559">If you still have sign-in issues, in the USERINFO table, note the **NETWORKDOMAIN** and **NETWORKALIAS** values.</span></span> <span data-ttu-id="a0be1-560">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-560">Here is an example:</span></span>

- <span data-ttu-id="a0be1-561">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span><span class="sxs-lookup"><span data-stu-id="a0be1-561">**NETWORKDOMAIN:** `https://DC1.contoso.com/adfs`</span></span>
- <span data-ttu-id="a0be1-562">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span><span class="sxs-lookup"><span data-stu-id="a0be1-562">**NETWORKALIAS:** `AXServiceUser@contoso.com`</span></span>
- <span data-ttu-id="a0be1-563">**IDENTITYPROVIDER:** これは **NETWORKDOMAIN** の内容と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-563">**IDENTITYPROVIDER:** This should match the **NETWORKDOMAIN** value.</span></span>

<span data-ttu-id="a0be1-564">AD FS マシンの、サーバー マネージャーで、**ツール** \> **AD FS の管理** \> **サービス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-564">On the AD FS machine, in Server Manager, go to **Tools** \> **AD FS Management** \> **Service**.</span></span> <span data-ttu-id="a0be1-565">**フェデレーション サービス プロパティの保守と編集** を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-565">Right-click **Service and Edit Federation Service Properties**.</span></span> <span data-ttu-id="a0be1-566">**フェデレーション サービスの識別子** は **USERINFO.NETWORKDOMAIN** の値と一致している必要があり、URL に **https** が入っている必要があります (たとえば `https://DC1.contoso.com/adfs`)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-566">The **Federation Service identifier** value should match the **USERINFO.NETWORKDOMAIN** value, and it should have **https** in the URL (for example, `https://DC1.contoso.com/adfs`).</span></span>

<span data-ttu-id="a0be1-567">AD FS マシンの、イベント ビューアーで、**アプリケーションとサービス ログ** \> **AD FS** \> **管理者** に移動してエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-567">On the AD FS machine, in Event Viewer, go to **Applications and Services Logs** \> **AD FS** \> **Admin**, and make a note of any errors.</span></span>

### <a name="fiddler"></a><span data-ttu-id="a0be1-568">Fiddler</span><span class="sxs-lookup"><span data-stu-id="a0be1-568">Fiddler</span></span>

<span data-ttu-id="a0be1-569">追加のデバッグには Fiddler を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-569">Fiddler can be used for additional debugging.</span></span> <span data-ttu-id="a0be1-570">Fiddler について詳しい情報は、 [AD FS 2.0: Fiddler Web デバッガーを使って WS フェデレーション パッシブ サインインを分析する方法](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) と [別の AD FS クレーム プロバイダーからの AD FS トークンのクラッキング](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-570">For in-depth information about Fiddler, see [AD FS 2.0: How to Use Fiddler Web Debugger to Analyze a WS-Federation Passive Sign-In](https://social.technet.microsoft.com/wiki/contents/articles/3286.ad-fs-2-0-how-to-use-fiddler-web-debugger-to-analyze-a-ws-federation-passive-sign-in.aspx) and [Cracking the AD FS Token from another AD FS Claims Provider](https://blogs.technet.microsoft.com/tangent_thoughts/2014/06/04/cracking-the-ad-fs-token-from-another-ad-fs-claims-provider/).</span></span>

<span data-ttu-id="a0be1-571">以下のセクションでは、 Microsoft Dynamics に返される要求に対する重点的なデバッグの手順を示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-571">The following sections provide focused debugging steps for claims that are returned to Microsoft Dynamics.</span></span>

#### <a name="repocapture"></a><span data-ttu-id="a0be1-572">リポジトリ/キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a0be1-572">Repo/capture</span></span>

1. <span data-ttu-id="a0be1-573">Fiddler を起動し、 **ツール \> オプション \> HTTPS** から **HTTPS トラフィックの復号化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-573">Open Fiddler, go to **Tools \> Options \> HTTPS**, and select **Decrypt HTTPS traffic**.</span></span>
2. <span data-ttu-id="a0be1-574">トラフィックのキャプチャを開始します (ショートカット キーは F12 キーです)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-574">Start to capture traffic (the shortcut key is F12).</span></span> <span data-ttu-id="a0be1-575">ツールの左下を確認すると、該当のトラフィックがキャプチャされていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-575">You can verify that that traffic is being captured by looking at the lower left of the tool.</span></span>
3. <span data-ttu-id="a0be1-576">Internet Explorer の InPrivate モード、またはChrome の Incognito モードを使用して開きます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-576">Open an InPrivate instance of Internet Explorer or an Incognito instance of Chrome.</span></span>
4. <span data-ttu-id="a0be1-577">Finance + Operations を開きます (例 `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-577">Open Finance + Operations (for example, `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/`).</span></span>
5. <span data-ttu-id="a0be1-578">USERINFO.NETWORKALIAS のアカウントとパスワードを使用してログオンします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-578">Sign in by using the USERINFO.NETWORKALIAS account and password.</span></span>
6. <span data-ttu-id="a0be1-579">ログイン後、Fiddler によるトラフィックのキャプチャを停止してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-579">After you're signed in, stop Fiddler from capturing traffic.</span></span>

#### <a name="analyze"></a><span data-ttu-id="a0be1-580">分析</span><span class="sxs-lookup"><span data-stu-id="a0be1-580">Analyze</span></span>

<span data-ttu-id="a0be1-581">Fiddler の右側のウィンドウには、リクエストとレスポンスが上段と下段にに分割されていることを留意してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-581">In the right pane of Fiddler, notice that a horizontal divider separates the request from the response.</span></span> <span data-ttu-id="a0be1-582">リクエストとレスポンスとでそれぞれ別個のフレームを取得するようなネットワーク トレースとは異なり、Fiddler はリクエストとレスポンスの両方を1 つのフレームで提供します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-582">Unlike a network trace, where you typically get one frame for a request and another frame for a response, Fiddler provides one frame that contains both the request and the response.</span></span>

1. <span data-ttu-id="a0be1-583">Fiddlerを起動し、画面右上隅の **Inspectors** \> **Raw** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-583">In Fiddler, in the upper-right corner, select **Inspectors** \> **Raw**.</span></span>
2. <span data-ttu-id="a0be1-584">右下隅の **Cookie** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-584">In the lower-right corner, select **Cookies**.</span></span>
3. <span data-ttu-id="a0be1-585">**MSISAuth** を検索します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-585">Do a search for **MSISAuth**.</span></span>
4. <span data-ttu-id="a0be1-586">AD FS をホストするには、結果が **200** 件ある行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-586">Select the row that has a result of **200** for the AD FS host.</span></span>
5. <span data-ttu-id="a0be1-587">上記で選択した上の行のなかで、 **302** 件の結果がある行を探します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-587">Look above the row that you just selected to find a row that has a result of **302**.</span></span> <span data-ttu-id="a0be1-588">確認した行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-588">Select the row.</span></span>

    <span data-ttu-id="a0be1-589">AD FS URL、ホスト、ユーザー名、およびパスワードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-589">You should see the AD FS URL, host, user name, and password.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a0be1-590">プライバシー保護のため、状況に応じて個人を特定できる情報を削除してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-590">For privacy, you might have to scrub personally identifiable information.</span></span>

    ![個人情報](media/Scrub-PII.png)

6. <span data-ttu-id="a0be1-592">次は、結果が **302** 件ある行を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-592">Select the next row that has a result of **302**.</span></span> <span data-ttu-id="a0be1-593">URL が、 **.../namespaces/AXSF/** となっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-593">The URL should be **.../namespaces/AXSF/**.</span></span>
7. <span data-ttu-id="a0be1-594">上記で選択した行に示されているコード行を探してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-594">Find the code line that is shown on that row.</span></span> 

    ![コード行](media/Note-the-code.png)

8. <span data-ttu-id="a0be1-596">等号 (=) の後に表示されているコード値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-596">Copy the value of code line after the equal sign (=).</span></span>
9. <span data-ttu-id="a0be1-597"><https://www.base64decode.org/> に移動し、上記でコピーしたコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-597">Go to <https://www.base64decode.org/>, and paste the code that you just copied.</span></span>
9. <span data-ttu-id="a0be1-598">**Source charset** フィールドで、 **ASCII** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-598">In the **Source charset** field, select **ASCII**.</span></span>
10. <span data-ttu-id="a0be1-599">**Decode** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-599">Select **Decode**.</span></span>
11. <span data-ttu-id="a0be1-600">表示された結果をコピーし、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-600">Copy the results, and follow these steps:</span></span>

    - <span data-ttu-id="a0be1-601">**upn** の値が、ユーザー名と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-601">Make sure that the **upn** value matches the user name.</span></span>
    - <span data-ttu-id="a0be1-602">**unique_name** の値がテストで使用している Active Directoryユーザー名であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-602">Make sure that the **unique_name** value is the Active Directory user that is being tested.</span></span>
    - <span data-ttu-id="a0be1-603">**Active Directory ユーザーとコンピューター** \> **ドメイン** \> **ユーザー** に移動し、テスト中のユーザーが表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-603">Go to **Active Directory Users and Computers** \> **domain** \> **Users**, and make sure that this user is being tested.</span></span>

## <a name="sign-in-issues"></a><span data-ttu-id="a0be1-604">サインインの問題</span><span class="sxs-lookup"><span data-stu-id="a0be1-604">Sign-in issues</span></span>

<span data-ttu-id="a0be1-605">サインインに関する問題が発生した場合には、Service Fabric Explorer で、**Provisioning\_AdminPrincipalName** および **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-605">If you or other users experience sign-in issues, in Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span> <span data-ttu-id="a0be1-606">値が有効な場合は、プライマリ SQL Server マシンで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-606">If the values are valid, run the following command on the primary SQL Server machine.</span></span>

```powershell
.\Reset-DatabaseUsers.ps1
```

<span data-ttu-id="a0be1-607">タスク マネージャーの各 AOS マシンで、**AXService.exe** を選択し、**タスクの終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-607">On each AOS machine, in Task Manager, select **AXService.exe**, and then select **End task**.</span></span>

<span data-ttu-id="a0be1-608">ユーザーがリセットされたことを確認するには、AXDB SQL databaseで次の **select** 文を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-608">To verify that a user has been reset, run the following **select** query in the AXDB SQL database.</span></span>

```sql
select SID, NETWORKDOMAIN, NETWORKALIAS, * from AXDB.dbo.USERINFO where id = 'admin'
```

> [!NOTE]
> <span data-ttu-id="a0be1-609">Azure Active Directory (Azure AD) 環境 (オンライン環境) では、SID はネットワーク エイリアスおよびネットワーク ドメインのハッシュの役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-609">In an Azure Active Directory (Azure AD) environment (that is, an online environment), the SID is a hash of a network alias and a network domain.</span></span> <span data-ttu-id="a0be1-610">AD DS 環境 (オンプレミス環境) では、SID はネットワーク エイリアスのハッシュとして機能し、プロバイダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-610">In an AD DS environment (that is, an on-premises environment), the SID is a hash of a network alias and an identify provider.</span></span>

<span data-ttu-id="a0be1-611">場合によっては、引き続きサインインができず、次のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-611">In some cases, you still might not be able to sign in, and you might receive the following error:</span></span>

> <span data-ttu-id="a0be1-612">現在の資格情報でログインする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-612">You are not authorized to login with your current credentials.</span></span> <span data-ttu-id="a0be1-613">AD FS マシンで、サーバー マネージャー > ツール > AD FS の管理 に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-613">You will be redirected to the login page in a few seconds.</span></span>

<span data-ttu-id="a0be1-614">このエラーが表示された場合は、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-614">If this error occurs, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-615">AD FS マシンで、 **Server Manager** \> **Tools** \> **AD FS Management** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-615">On the AD FS machine, go to **Server Manager** \> **Tools** \> **AD FS Management**.</span></span>
2. <span data-ttu-id="a0be1-616">**AD FS** を右クリックし、**フェデレーション サービス プロパティの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-616">Right-click **AD FS**, and then select **Edit Federation Service Properties**.</span></span>
3. <span data-ttu-id="a0be1-617">**フェデレーション サービス 識別子** の値が、 **Userinfo.NetworkDomain** および **UserInfo.IdentityProvider** の値と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-617">Make sure that the **Federation Service Identifier** value matches the **Userinfo.NetworkDomain** and **UserInfo.IdentityProvider** values.</span></span>
4. <span data-ttu-id="a0be1-618">AD FS マシンで、Windows PowerShell を開き、 **Get-AdfsProperties** を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-618">On the AD FS machine, open Windows PowerShell, and run **Get-AdfsProperties**.</span></span>
5. <span data-ttu-id="a0be1-619">**IdTokenIssuer** の値が、手順3の **フェデレーション サービス 識別子** の値、および **Provisioning_AdminIdentityProvider** の値と一致していることを確認してください。 (これは **fabric:/AXSF Details** タブに表示されています。 **Service Fabric Explorer** \> **Cluster** \> **Applications** \> **AXSFType**)</span><span class="sxs-lookup"><span data-stu-id="a0be1-619">Make sure that the **IdTokenIssuer** value matches the **Federation Service Identifier** value from step 3, and also the **Provisioning_AdminIdentityProvider** value on the **fabric:/AXSF Details** tab at **Service Fabric Explorer** \> **Cluster** \> **Applications** \> **AXSFType**.</span></span>
3. <span data-ttu-id="a0be1-620">Service Fabric Explorer で、 **Provisioning\_AdminPrincipalName** 値と **Provisioning\_AdminIdentityProvider** の値が有効であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-620">In Service Fabric Explorer, verify that the **Provisioning\_AdminPrincipalName** and **Provisioning\_AdminIdentityProvider** values are valid.</span></span>

<span data-ttu-id="a0be1-621">上記の手順で問題が解決しない場合は、このトピックの 「 [AD FS](troubleshoot-on-prem.md#ad-fs) 」 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-621">If the preceding steps don't resolve the issue, see the [AD FS](troubleshoot-on-prem.md#ad-fs) section of this topic.</span></span>

## <a name="systemdatasqlclientsqlexception-0x80131904-and-systemcomponentmodelwin32exception-0x80004005"></a><span data-ttu-id="a0be1-622">System.Data.SqlClient.SqlException (0x80131904) および System.ComponentModel.Win32Exception (0x80004005)</span><span class="sxs-lookup"><span data-stu-id="a0be1-622">System.Data.SqlClient.SqlException (0x80131904) and System.ComponentModel.Win32Exception (0x80004005)</span></span>

<span data-ttu-id="a0be1-623">次のエラーのいずれかが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-623">You might receive one of the following errors:</span></span>

> <span data-ttu-id="a0be1-624">System.Data.SqlClient.SqlException (0x80131904): 接続がサーバーで正常に確立されましたが、サインイン プロセス時にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-624">System.Data.SqlClient.SqlException (0x80131904): A connection was successfully established with the server, but then an error occurred during the sign-in process.</span></span> <span data-ttu-id="a0be1-625">(プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは、信頼されていない機関によって発行されました。)</span><span class="sxs-lookup"><span data-stu-id="a0be1-625">(provider: SSL Provider, error: 0 - The certificate chain was issued by an authority that is not trusted.)</span></span>

> <span data-ttu-id="a0be1-626">System.ComponentModel.Win32Exception (0x80004005): 証明書チェーンは、信頼されていない機関によって発行されました</span><span class="sxs-lookup"><span data-stu-id="a0be1-626">System.ComponentModel.Win32Exception (0x80004005): The certificate chain was issued by an authority that is not trusted</span></span>

<span data-ttu-id="a0be1-627">この場合、証明書がインストールされていないか、それらがしかるべきユーザーに結びついていません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-627">In this case, either the certificates haven't been installed, or they haven't given access to the correct users.</span></span> <span data-ttu-id="a0be1-628">このエラーを解決するには、公開キー SQL サーバー証明書をすべての Service Fabric ノードに追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-628">To resolve this error, add the public key SQL Server certificate to all the Service Fabric nodes.</span></span>

## <a name="keyset-doesnt-exist"></a><span data-ttu-id="a0be1-629">Keyset が存在しません</span><span class="sxs-lookup"><span data-stu-id="a0be1-629">Keyset doesn't exist</span></span>

<span data-ttu-id="a0be1-630">キーセットが存在しないことが判明した場合は、スクリプトがすべてのコンピューターで実行されなていなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-630">If you find that the keyset doesn't exist, scripts weren't run on all machines.</span></span> <span data-ttu-id="a0be1-631">適切な設定の「VM の設定」セクション、および環境の配置トピックを確認し完了します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-631">Review and complete the "Set up VMs" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="a0be1-632">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-632">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#setupvms)
- [<span data-ttu-id="a0be1-633">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-633">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#setupvms)

<span data-ttu-id="a0be1-634">各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-634">Copy the scripts in each folder to the VMs that correspond to the folder name.</span></span>

<span data-ttu-id="a0be1-635">また、正しいドメインを使うことを検証する .csv ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-635">Additionally, check the .csv file to verify that the correct domain is used.</span></span>

## <a name="error-runasync-failed-due-to-an-unhandled-fabricexception-causing-replica-to-fault"></a><span data-ttu-id="a0be1-636">エラー、「未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました」</span><span class="sxs-lookup"><span data-stu-id="a0be1-636">Error: "RunAsync failed due to an unhandled FabricException causing replica to fault"</span></span>

<span data-ttu-id="a0be1-637">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-637">You might receive the following error:</span></span>

> <span data-ttu-id="a0be1-638">未処理の FabricException がレプリカに障害を引き起こしたため、RunAsync が失敗しました: System.Fabric.FabricException: 最初の Fabric アップグレードではコード バージョンと設定バージョンの両方を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-638">RunAsync failed due to an unhandled FabricException causing replica to fault: System.Fabric.FabricException: The first Fabric upgrade must specify both the code and config versions.</span></span> <span data-ttu-id="a0be1-639">要求された値: 0.0.0.0:</span><span class="sxs-lookup"><span data-stu-id="a0be1-639">Requested value: 0.0.0.0:</span></span>

<span data-ttu-id="a0be1-640">この場合、ClusterConfig.json ファイルで、 **diagnosticsStore** をネットワーク共有からローカル パスに変更します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-640">In this case, in the ClusterConfig.json file, change **diagnosticsStore** from a network share to a local path.</span></span> <span data-ttu-id="a0be1-641">たとえば、**\\\\サーバー\\パス** を、規定値の **C:\\ProgramData\\SF\\DiagnosticsStore** に変更します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-641">For example, change **\\\\server\\path** to a default value of **C:\\ProgramData\\SF\\DiagnosticsStore**.</span></span>

## <a name="service-fabric-aos-node-error-during-build-the-execution-time-out-expired"></a><span data-ttu-id="a0be1-642">ビルド中に Service Fabric AOS ノード エラー: 実行タイムアウトが期限切れ</span><span class="sxs-lookup"><span data-stu-id="a0be1-642">Service Fabric AOS node error during build: The execution time-out expired</span></span>

<span data-ttu-id="a0be1-643">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-643">**Error:**</span></span>

> <span data-ttu-id="a0be1-644">操作を完了する前にタイムアウト期間が経過したか、サーバーが応答していません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-644">The timeout period elapsed prior to completion of the operation or the server is not responding.</span></span>  
> <span data-ttu-id="a0be1-645">明細書は終了しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-645">The statement has been terminated.</span></span>

<span data-ttu-id="a0be1-646">一度に 1 つの AOS マシンのみ DB Sync を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-646">Only one AOS machine can run DB Sync at a time.</span></span> <span data-ttu-id="a0be1-647">このエラーは無視しても問題ありません。 AOS VM のいずれかが DB Sync で実行されているため、他の VM が実行できないという警告が表示されたためです。</span><span class="sxs-lookup"><span data-stu-id="a0be1-647">You can safely ignore this error, because it means that one of the AOS VMs is running DB Sync. Therefore, the other VMs produce a warning that they can't run it.</span></span> <span data-ttu-id="a0be1-648">DB Sync が実行されていることを確認するには、イベント ビューアの、警告を生成していない AOS VM で **アプリケーションおよびサービスのログ** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-648">To verify that DB Sync is running, on the AOS VM that isn't producing warnings, in Event Viewer, go to **Applications and Services Log** \> **Microsoft** \> **Dynamics** \> **AX-DatabaseSynchronize/Operational**.</span></span>

## <a name="error-requirenonce-is-true-default-but-validationcontextnonce-is-null"></a><span data-ttu-id="a0be1-649">エラー、「RequireNonce が True (既定) ですが、validationContext.Nonce は Null です」</span><span class="sxs-lookup"><span data-stu-id="a0be1-649">Error: "RequireNonce is 'true' (default) but validationContext.Nonce is null"</span></span>

<span data-ttu-id="a0be1-650">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-650">You might receive the following error:</span></span>

> <span data-ttu-id="a0be1-651">「RequireNonce が True (既定) となっていますが、validationContext.Nonce は Null となっています」</span><span class="sxs-lookup"><span data-stu-id="a0be1-651">RequireNonce is 'true' (default) but validationContext.Nonce is null</span></span>

<span data-ttu-id="a0be1-652">このエラーは、クライアントにサインインした後も Internet Explorer で HTTP エラー 500 として表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-652">This error also appears as an HTTP error 500 in Internet Explorer after you sign in to the client.</span></span> <span data-ttu-id="a0be1-653">Internet Explorer がセキュリティ強化の構成になっている場合、発行された nonce は検証できません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-653">The nonce that is issued can't be validated if Internet Explorer is in Enhanced Security Configuration.</span></span>

<span data-ttu-id="a0be1-654">クライアントにサインインするには、サーバー マネージャーを介して Internet Explorer のセキュリティ強化設定を無効にします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-654">To sign in to the client, disable Enhanced Security Configuration for Internet Explorer via Server Manager.</span></span>

## <a name="error-invalid-algorithm-specified--cryptography"></a><span data-ttu-id="a0be1-655">エラー、「無効なアルゴリズムが指定されている/暗号化」</span><span class="sxs-lookup"><span data-stu-id="a0be1-655">Error: "Invalid algorithm specified / Cryptography"</span></span>

<span data-ttu-id="a0be1-656">"Invalid algorithm specified / Cryptography" エラーが発生した場合は、Microsoft Enhanced RSA および AES Cryptographic Provider を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-656">If you receive an "Invalid algorithm specified / Cryptography" error, you must use the Microsoft Enhanced RSA and AES Cryptographic Provider.</span></span> <span data-ttu-id="a0be1-657">詳細については、証明書の要件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-657">For more information, see the certificate requirements.</span></span> <span data-ttu-id="a0be1-658">また、credentials.json ファイルの構造が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-658">Additionally, verify that the structure of the credentials.json file is correct.</span></span>

<span data-ttu-id="a0be1-659">正しいプロバイダーを使用して証明書を再作成する必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-659">If you must re-create the certificate by using the correct provider, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-660">正しいプロバイダーを使用して証明書を再度作成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-660">Create the certificate again by using the correct provider.</span></span>
2. <span data-ttu-id="a0be1-661">**ConfigTemplate.xml** ファイルの変更。</span><span class="sxs-lookup"><span data-stu-id="a0be1-661">Change the **ConfigTemplate.xml** file.</span></span>
3. <span data-ttu-id="a0be1-662">クラスター内のすべてのコンピューターでインフラストラクチャ スクリプトを実行し、**Test-D365FOConfiguration.ps1** スクリプトに合格するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-662">Run the infrastructure scripts on all machines in the cluster, and make sure that the **Test-D365FOConfiguration.ps1** script passes.</span></span>
4. <span data-ttu-id="a0be1-663">LCS から環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-663">Reconfigure the environment from LCS.</span></span>

## <a name="an-unable-to-find-certificate-error-occurs-when-you-run-test-d365foconfigurationps1"></a><span data-ttu-id="a0be1-664">Test-D365FOConfiguration.ps1 を実行した際、「証明書を検出できません」エラーが発生</span><span class="sxs-lookup"><span data-stu-id="a0be1-664">An "Unable to find certificate" error occurs when you run Test-D365FOConfiguration.ps1</span></span>

<span data-ttu-id="a0be1-665">Test-D365FOConfiguration.ps1 を実行時に 「証明書を検出できません」 というエラーが発生した場合は、証明書または拇印がその他複数の用途で併用されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-665">If you receive an "Unable to find certificate" error when you run Test-D365FOConfiguration.ps1, check whether certificates or thumbprints are being combined for multiple purposes.</span></span> <span data-ttu-id="a0be1-666">たとえば、クライアントと SessionAuthentication の証明書が併用されてされる場合、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-666">For example, you will receive this error if the client certificate and the SessionAuthentication certificate are combined.</span></span> <span data-ttu-id="a0be1-667">証明書を結合しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-667">We recommend that you not combine certificates.</span></span> <span data-ttu-id="a0be1-668">詳細については、 証明書の必要要件を参照し、 **domain.com\\user** versus **domain\\user** 内 (たとえば、NETBIOS 構造) のacl.csv ファイルを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-668">For more information, see the certificate requirements, and check the acl.csv file for **domain.com\\user** versus **domain\\user** (for example, NETBIOS structure).</span></span>

## <a name="the-client-and-server-cant-communicate-because-they-dont-have-a-common-algorithm"></a><span data-ttu-id="a0be1-669">クライアントとサーバーは共通のアルゴリズムを持たないため通信できません</span><span class="sxs-lookup"><span data-stu-id="a0be1-669">The client and server can't communicate because they don't have a common algorithm</span></span>

<span data-ttu-id="a0be1-670">クライアントとサーバーが疎通できない場合は双方のアルゴリズムが異なることが原因です。作成した証明書が指定したプロバーダーを使用しているか確認をしてください。これについては"Plan and acquire your certificates" の項目で解説しています。ご利用の環境に応じた適切な設定と配置を行ってください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-670">If the client and server can't communicate because they don't have a common algorithm, verify that the certificates that are created use the specified provider, as explained in the "Plan and acquire your certificates" section of the appropriate setup and deployment topic for your environment:</span></span>

- [<span data-ttu-id="a0be1-671">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-671">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#plancert)
- [<span data-ttu-id="a0be1-672">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-672">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#plancert)

## <a name="find-a-list-of-group-managed-service-accounts"></a><span data-ttu-id="a0be1-673">グループ管理サービス アカウント の一覧の検索</span><span class="sxs-lookup"><span data-stu-id="a0be1-673">Find a list of group managed service accounts</span></span>

<span data-ttu-id="a0be1-674">すべてのグループとホストの一覧を検索するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-674">To find a list of all groups and hosts, run the following command.</span></span>

```powershell
Get-ADServiceAccount -Identity svc-LocalAgent$ -Properties PrincipalsAllowedToRetrieveManagedPassword
```

## <a name="addcerttoserviceprincipal-script-fails-on-import-module"></a><span data-ttu-id="a0be1-675">Import-Module での AddCertToServicePrincipal スクリプトの失敗</span><span class="sxs-lookup"><span data-stu-id="a0be1-675">AddCertToServicePrincipal script fails on Import-Module</span></span>

<span data-ttu-id="a0be1-676">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-676">**Error:**</span></span>

> <span data-ttu-id="a0be1-677">Import-Module での AddCertToServicePrincipal スクリプトの失敗: ファイルまたはアセンブリ 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' またはその依存関係のうちのいずれか 1 つを読み込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0be1-677">AddCertToServicePrincipal script failing on Import-Module : Could not load file or assembly 'Commands.Common.Graph.RBAC, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' or one of its dependencies.</span></span> <span data-ttu-id="a0be1-678">厳密な名前の検証に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-678">Strong name validation failed.</span></span> <span data-ttu-id="a0be1-679">(HRESULT からの例外: 0x8013141A) には、同じモジュールの複数のバージョンがインストールされている場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-679">(Exception from HRESULT: 0x8013141A) may have multiple versions of the same module installed.</span></span>

<span data-ttu-id="a0be1-680">**ステップ:** 問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-680">**Steps:** To resolve this issue, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-681">Windows PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-681">Run the following command in Windows PowerShell.</span></span>

    ```powershell
    Uninstall-Module -Name AzureRM
    Install-Module AzureRM
    ```

2. <span data-ttu-id="a0be1-682">Windows PowerShell ウィンドウを閉じて、スクリプトを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-682">Close the Windows PowerShell window, and try to run the script again.</span></span>

## <a name="reportingservicessetupexe-error"></a><span data-ttu-id="a0be1-683">ReportingServicesSetup.exe エラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-683">ReportingServicesSetup.exe error</span></span>

<span data-ttu-id="a0be1-684">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-684">**Error:**</span></span>

> <span data-ttu-id="a0be1-685">ReportingServicesSetup.exe エラー: 0 : アプリケーション fabric:/ReportingService は10分後から OK ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-685">ReportingServicesSetup.exe Error: 0 : Application fabric:/ReportingService is not OK after 10 minutes</span></span>  
> <span data-ttu-id="a0be1-686">アプリケーション: ReportingServicesBootstrapper.exe</span><span class="sxs-lookup"><span data-stu-id="a0be1-686">Application: ReportingServicesBootstrapper.exe</span></span>  
> <span data-ttu-id="a0be1-687">フレームワーク バージョン: v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="a0be1-687">Framework Version: v4.0.30319</span></span>  
> <span data-ttu-id="a0be1-688">説明: プロセスは未処理の例外によって中止されました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-688">Description: The process was terminated due to an unhandled exception.</span></span>

<span data-ttu-id="a0be1-689">**理由:** このエラーが発生した場合、厳密な名前検証はレポート サーバーで有効にされていますが、有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-689">**Reason:** If you receive this error, strong name validation is enabled in the Reporting server, but it should not be enabled.</span></span>

<span data-ttu-id="a0be1-690">**ステップ:** 問題を解決するには、レポート サーバー マシンで **config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-690">**Steps:** To resolve this issue, run the **config-PreReq** script on the Reporting server machine.</span></span>

## <a name="the-requested-operation-requires-elevation"></a><span data-ttu-id="a0be1-691">要求された操作には、昇格が必要です</span><span class="sxs-lookup"><span data-stu-id="a0be1-691">The requested operation requires elevation</span></span>

<span data-ttu-id="a0be1-692">AOS ユーザーはローカル管理者グループに属しておらず、ユーザー アカウント コントロール (UAC) が正しく無効化されていないために、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-692">This issue occurs because AOS users aren't in the local administrator group, and User Account Control (UAC) hasn't been disabled correctly.</span></span> <span data-ttu-id="a0be1-693">問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-693">To resolve the issue, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-694">環境の適切な設定および配置トピックの「VMs とドメインを結合」のセクションで説明されているように、ローカル管理者として AOS ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-694">Add AOS users as local admins, as described in the "Join VMs to the domain" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="a0be1-695">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-695">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#joindomain)
    - [<span data-ttu-id="a0be1-696">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-696">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#joindomain)

2. <span data-ttu-id="a0be1-697">すべての AOS コンピューターで、**Config-PreReq** スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-697">Run the **Config-PreReq** script on all the AOS machines.</span></span>
3. <span data-ttu-id="a0be1-698">**テスト構成** スクリプトがパスすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-698">Make sure that the **Test-Configuration** script passes.</span></span>
4. <span data-ttu-id="a0be1-699">UAC が変更された場合は、変更を有効にする前にマシンを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-699">If UAC was changed, you must restart the machine before the changes take effect.</span></span>

## <a name="files-in-use-errors"></a><span data-ttu-id="a0be1-700">使用中ファイルのエラー</span><span class="sxs-lookup"><span data-stu-id="a0be1-700">Files in use errors</span></span>

<span data-ttu-id="a0be1-701">「ファイルは使用中です」のエラーが発生した場合は、Service Fabric に示されている例外ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-701">If these "Files in use" errors occur, set up the exclusion rules that Service Fabric advises.</span></span> <span data-ttu-id="a0be1-702">詳細については、[環境設定](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-702">For information, see [Environment setup](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup).</span></span>

## <a name="apply-deployable-packages-during-deployment"></a><span data-ttu-id="a0be1-703">配置中に配置可能パッケージを適用する</span><span class="sxs-lookup"><span data-stu-id="a0be1-703">Apply deployable packages during deployment</span></span>

### <a name="package-deployment-fails-because-of-a-path-too-long-exception"></a><span data-ttu-id="a0be1-704">「パスが長過ぎる」例外によってパッケージの展開が失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-704">Package deployment fails because of a "path too long" exception</span></span>

<span data-ttu-id="a0be1-705">Microsoft Windows では 260 文字の制限があるため、パッケージの名前が長い場合やオンプレミス共有に完全な FQDN パスがある場合は、展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-705">Because of a 260-character limit in Microsoft Windows, deployment will fail if a package has a longer name, or if the on-premises share has the full FQDN path.</span></span> <span data-ttu-id="a0be1-706">文字数の制限を超過した場合、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-706">If the character limit is exceeded, you receive the following error:</span></span>

> <span data-ttu-id="a0be1-707">System.IO.PathTooLongException: 指定されたパス、ファイル名、またはその両方が長すぎます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-707">System.IO.PathTooLongException: The specified path, file name, or both are too long.</span></span> <span data-ttu-id="a0be1-708">完全に記述されたファイル名は 260 文字未満である必要があり、ディレクトリ名は 248 文字未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-708">The fully qualified file name must be less than 260 characters, and the directory name must be less than 248 characters.</span></span> <span data-ttu-id="a0be1-709">at System.IO.PathHelper.GetFullPathName</span><span class="sxs-lookup"><span data-stu-id="a0be1-709">at System.IO.PathHelper.GetFullPathName</span></span>

<span data-ttu-id="a0be1-710">この問題を回避するには、パッケージ名を短くし、パッケージをもう一度適用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-710">To work around this issue, shorten the package name, and then apply the package again.</span></span> <span data-ttu-id="a0be1-711">または、オンプレミス資産の共有パス全体の長さを短くしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-711">Alternatively, shorten the overall length of the share path for the on-premises assets.</span></span>

### <a name="package-deployment-fails-because-of-a-serialization-error"></a><span data-ttu-id="a0be1-712">シリアル化エラーが原因でパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-712">Package deployment fails because of a serialization error</span></span>

<span data-ttu-id="a0be1-713">パッケージ配置中、次のエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-713">During package deployment, you might receive the following error:</span></span>

> <span data-ttu-id="a0be1-714">シリアル化バージョンの不一致が検出されたので、ランタイム DLL が配置されたメタデータと同期していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-714">Serialization version mismatch detect, make sure the runtime DLLs are in sync with the deployed metadata.</span></span> <span data-ttu-id="a0be1-715">「XXX」ファイルのバージョン</span><span class="sxs-lookup"><span data-stu-id="a0be1-715">Version of file 'XXX'.</span></span> <span data-ttu-id="a0be1-716">DLL 「XXX」のバージョン</span><span class="sxs-lookup"><span data-stu-id="a0be1-716">Version of DLL 'XXX'</span></span>

<span data-ttu-id="a0be1-717">この場合は、パッケージが開発された環境のバージョンと、パッケージを配置する環境のバージョンが異なっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-717">In this case, the version of the environment where the package was developed might differ from the version of the environment that the package is being deployed in.</span></span>

<span data-ttu-id="a0be1-718">この問題を回避するには、展開されたオンプレミス環境と同じバージョンで開発環境またはビルド環境を維持します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-718">To work around this issue, keep the development or build environments on the same version as the deployed on-premises environment.</span></span> <span data-ttu-id="a0be1-719">パッケージのアップロード先にあるアセット ライブラリの **追加の詳細** セクションをクリックすることにより、パッケージ バージョンを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-719">You can confirm the package version by looking in the **Additional details** section in the Asset library where the package is uploaded.</span></span> <span data-ttu-id="a0be1-720">このエラーを修正するには、オンプレミス環境に配置されたバージョンと同じか、またはそれ以前のバージョンでパッケージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-720">To fix the error, generate the package on a version that is the same as or earlier than the version that is deployed in the on-premises environment.</span></span>

### <a name="package-deployment-fails-because-of-dependencies-on-missing-modules"></a><span data-ttu-id="a0be1-721">欠落しているモジュールの依存関係が原因でがパッケージの展開に失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-721">Package deployment fails because of dependencies on missing modules</span></span>

<span data-ttu-id="a0be1-722">依存モジュールがないパッケージを適用しようとすると、パッケージ アプリケーションが失敗して、次のようなメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-722">If you try to apply a package that is missing dependent modules, package application will fail, and you will receive a message that resembles the following message:</span></span>

> <span data-ttu-id="a0be1-723">パッケージ \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="a0be1-723">Package \[dynamicsax-My\_commonextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-publicsectorformadaptor\]\]</span></span>
>
> <span data-ttu-id="a0be1-724">パッケージ \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span><span class="sxs-lookup"><span data-stu-id="a0be1-724">Package \[dynamicsax-My\_coreextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests;dynamicsax-generalledgerformadaptor;dynamicsax-publicsectorformadaptor;dynamicsax-retailformadaptor\]\]</span></span>
>
> <span data-ttu-id="a0be1-725">パッケージ \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg に依存関係がありません: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span><span class="sxs-lookup"><span data-stu-id="a0be1-725">Package \[dynamicsax-My\_uiextension.7.0.4679.35176.nupkg has missing dependencies: \[dynamicsax-demodatasuite;dynamicsax-financialreportingadaptors;dynamicsax-fiscalbooksformadaptor;dynamicsax-fleetmanagement;dynamicsax-fleetmanagementextension;dynamicsax-fleetmanagementunittests\]\]</span></span>

<span data-ttu-id="a0be1-726">問題を確認し、欠落している依存関係を見つけるには、イベント ビューアーで、**アプリケーションとサービス** を開き、**Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** の順で移動して、見つからないモジュールのあるイベントを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-726">To confirm the issue and find the missing dependencies, in Event Viewer, open **Application and Services**, and then go to **Microsoft** \> **Dynamics** \> **AX-SetupModuleEvents** to view events that have missing modules.</span></span> <span data-ttu-id="a0be1-727">たとえば、一般的に見つからないモジュールの 1 つは、ApplicationFoundationFormAdaptor です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-727">For example, one of the modules that is typically missing is ApplicationFoundationFormAdaptor.</span></span>

<span data-ttu-id="a0be1-728">この問題を修正してパッケージを正常に適用するには、依存モジュールを追加するか、依存モジュールが必要なモジュールを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-728">To fix this issue and successfully apply the package, either add dependent modules, or remove modules that require dependent modules.</span></span> <span data-ttu-id="a0be1-729">依存するモジュールを追加するには、パッケージをビルドするときに依存関係を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-729">To add dependent modules, you must include the dependencies when you build the package.</span></span> <span data-ttu-id="a0be1-730">モジュールを削除するには、ModelUtil.exe を使用してモジュールを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-730">To remove modules, you can use ModelUtil.exe to delete a module.</span></span> <span data-ttu-id="a0be1-731">詳細については、 [モデルのエクスポートとインポート](../dev-tools/models-export-import.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-731">For more information, see [Export and import models](../dev-tools/models-export-import.md).</span></span>

### <a name="package-deployment-works-in-a-one-box-environment-but-not-in-the-sandbox-environment"></a><span data-ttu-id="a0be1-732">パッケージの展開がワン ボックス環境で機能するが、サンドボックス環境で機能しない</span><span class="sxs-lookup"><span data-stu-id="a0be1-732">Package deployment works in a one-box environment but not in the sandbox environment</span></span>

<span data-ttu-id="a0be1-733">1 ボックス環境にはすべてのモジュールがインストールされている可能性があり、一方ではサンドボックス環境には実稼働環境で実行するために必要なモジュールのみがインストールされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-733">A one-box environment might have all the modules installed, whereas the sandbox environment might have only the modules that are required in order to run your production environment.</span></span> <span data-ttu-id="a0be1-734">開発環境で作成されたパッケージが、サンドボックス環境ではなく、ワン ボックス環境にあるモジュールに依存する場合、パッケージはサンドボックス環境では動作しません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-734">If the package that was built in the dev environment has a dependency on modules that are present in the one-box environment but not in the sandbox environment, the package won't work in the sandbox environment.</span></span>

<span data-ttu-id="a0be1-735">この問題を解決するには、依存関係のあるすべてのモジュールを確認し、実稼動環境で不要なアダプターまたはその他のモジュールを使用しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-735">To resolve this issue, look at all the modules that you're dependent on, and make sure that you don't pull any farm adapter or any other module that isn't required in the production environment.</span></span> <span data-ttu-id="a0be1-736">ビルド ボックスからパッケージを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-736">The best practice is to take the package from the build box.</span></span>

## <a name="an-error-occurs-when-you-sign-in-to-on-premises-environments"></a><span data-ttu-id="a0be1-737">オンプレミス環境へのログイン時にエラーが発生</span><span class="sxs-lookup"><span data-stu-id="a0be1-737">An error occurs when you sign in to on-premises environments</span></span>

- <span data-ttu-id="a0be1-738">**プラットフォーム更新 12:** **システム管理** \> **設定** \> **クライアント パフォーマンス オプション** に移動して、Skype 統合を無効にしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-738">**Platform update 12:** Turn off the Skype integration by going to **System administration** \> **Setup** \> **Client performance options**.</span></span> <span data-ttu-id="a0be1-739">アプリに移動するとき、`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true` の例のように、**?debug=true** を URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-739">When you go to the app, append **?debug=true** to the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>
- <span data-ttu-id="a0be1-740">**プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11:** 確認されている問題は、 Skype の アプリケーション プログラミング インターフェイス (API) が、オンプレミス環境へのサインインする機能に影響を及ぼしているというものです。</span><span class="sxs-lookup"><span data-stu-id="a0be1-740">**Platform update 8 and Platform update 11:** A known issue for the Skype application programming interface (API) affects the ability to sign in to on-premises environments.</span></span> <span data-ttu-id="a0be1-741">Microsoftはこの問題の解決方法を調査しています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-741">Microsoft is investigating a resolution for this issue.</span></span> <span data-ttu-id="a0be1-742">この問題を回避するために、次の例のように URL の末尾に **?debug=true** を追加できます。`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span><span class="sxs-lookup"><span data-stu-id="a0be1-742">To work around this issue, you can add **?debug=true** to the end of the URL, as shown in the following example: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/?debug=true`</span></span>

## <a name="the-local-agent-stops-working-after-the-tenant-for-the-project-from-lcs-is-changed"></a><span data-ttu-id="a0be1-743">ローカル エージェントは、LCS からのプロジェクトのテナントが変更されると作業を停止します</span><span class="sxs-lookup"><span data-stu-id="a0be1-743">The local agent stops working after the tenant for the project from LCS is changed</span></span>

<span data-ttu-id="a0be1-744">更新されたテナントでローカル エージェントを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-744">Follow these steps to configure the local agent with the updated tenant.</span></span>

1. <span data-ttu-id="a0be1-745">ローカル エージェントをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-745">Uninstall the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. <span data-ttu-id="a0be1-746">ユーザーの環境での適切なセットアップと配置トピックの「テナントの LCS 接続のコンフィギュレーション」セクションにある手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-746">Follow the steps in the "Configure LCS connectivity for the tenant" section of the appropriate setup and deployment topic for your environment:</span></span>

    - [<span data-ttu-id="a0be1-747">プラットフォーム update 12</span><span class="sxs-lookup"><span data-stu-id="a0be1-747">Platform update 12</span></span>](setup-deploy-on-premises-pu12.md#configurelcs)
    - [<span data-ttu-id="a0be1-748">プラットフォーム更新プログラム 8 とプラットフォーム更新プログラム 11</span><span class="sxs-lookup"><span data-stu-id="a0be1-748">Platform update 8 and Platform update 11</span></span>](setup-deploy-on-premises-pu8-pu11.md#configurelcs)

3. <span data-ttu-id="a0be1-749">新しいテナントに新しい LCS コネクタを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-749">Create a new LCS connector in the new tenant.</span></span>
4. <span data-ttu-id="a0be1-750">**local-agent.config** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-750">Download the **local-agent.config** file.</span></span>
5. <span data-ttu-id="a0be1-751">ローカル エージェントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-751">Install the local agent.</span></span>

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="additional-deployments-for-example-two-sandbox-deployments-or-a-sandbox-and-production-deployment"></a><span data-ttu-id="a0be1-752">追加の配置 (たとえば、2 つのサンド ボックス展開、またはサンド ボックスおよび生産の配置)</span><span class="sxs-lookup"><span data-stu-id="a0be1-752">Additional deployments (for example, two sandbox deployments, or a sandbox and production deployment)</span></span>

<span data-ttu-id="a0be1-753">追加の環境を展開すると、次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-753">You will receive the following error when you deploy an additional environment:</span></span>

> <span data-ttu-id="a0be1-754">\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: アプリケーション グループ ID は、AD FS コンフィギュレーションで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-754">.\\Publish-ADFSApplicationGroup.ps1 -HostUrl `https://ax.d365ffo.onprem.contoso.com` New-AdfsApplicationGroup : MSIS9908: The application group identifier must be unique in AD FS configuration.</span></span>

<span data-ttu-id="a0be1-755">配備手順の次のセクションをスキップまたは変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-755">You can skip or modify the following sections in the deployment instructions.</span></span>

### <a name="plan-and-acquire-your-certificates-as-documented-for-platform-update-12-or-platform-update-8-and-platform-update-11"></a><span data-ttu-id="a0be1-756">証明書の計画と取得 ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#plancert) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#plancert) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="a0be1-756">Plan and acquire your certificates (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#plancert) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#plancert))</span></span>

- <span data-ttu-id="a0be1-757">同一のオンプレミスのローカル エージェント証明書を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-757">You must use the same on-premises local agent certificate.</span></span>
- <span data-ttu-id="a0be1-758">同一のスター証明書を使用することができます(AOS SSL および Service Fabric)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-758">You can use same star certificates (AOS SSL and Service Fabric).</span></span>
- <span data-ttu-id="a0be1-759">残りの証明書は既存の環境の証明書とは異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-759">The remaining certificates should probably differ from the certificates for the existing environment.</span></span>

### <a name="download-setup-scripts-from-lcs-as-documented-for-platform-update-12-or-platform-update-8-and-platform-update-11"></a><span data-ttu-id="a0be1-760">LCS からのセットアップ スクリプトのダウンロード ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#downloadscripts) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="a0be1-760">Download setup scripts from LCS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#downloadscripts) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#downloadscripts))</span></span>

- <span data-ttu-id="a0be1-761">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-761">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="set-up-a-standalone-service-fabric-cluster-as-documented-for-platform-update-12-or-platform-update-8-and-platform-update-11"></a><span data-ttu-id="a0be1-762">([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#setupsfcluster) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster) に記載されているように) スタンドアロン Service Fabric クラスタを設定します</span><span class="sxs-lookup"><span data-stu-id="a0be1-762">Set up a standalone Service Fabric cluster (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#setupsfcluster) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#setupsfcluster))</span></span>

- <span data-ttu-id="a0be1-763">ダウンロードしたスクリプトを、新しいフォルダーにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-763">The scripts that are downloaded should be copied into a new folder.</span></span>

### <a name="configure-lcs-connectivity-for-the-tenant-as-documented-for-platform-update-12-or-platform-update-8-and-platform-update-11"></a><span data-ttu-id="a0be1-764">テナント用 LCS 接続 のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configurelcs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="a0be1-764">Configure LCS connectivity for the tenant (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configurelcs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configurelcs))</span></span>

- <span data-ttu-id="a0be1-765">テナントに対して、このタスクを 1 回のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-765">You must complete this task only one time for the tenant.</span></span>

### <a name="configure-ad-fs-as-documented-for-platform-update-12-or-platform-update-8-and-platform-update-11"></a><span data-ttu-id="a0be1-766">AD FS のコンフィギュレーション ([プラットフォーム更新プログラム 12](setup-deploy-on-premises-pu12.md#configureadfs) または [プラットフォーム更新プログラム 8 およびプラットフォーム更新プログラム 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs) で記載されたものとして)</span><span class="sxs-lookup"><span data-stu-id="a0be1-766">Configure AD FS (as documented for [Platform update 12](setup-deploy-on-premises-pu12.md#configureadfs) or [Platform update 8 and Platform update 11](setup-deploy-on-premises-pu8-pu11.md#configureadfs))</span></span>

- <span data-ttu-id="a0be1-767">[複数環境の同じ AD FS インスタンスの再使用](./onprem-reuseadfs.md) ガイドに従って AD FS を構成します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-767">Configure AD FS according to the [Reuse the same AD FS instance for multiple environments](./onprem-reuseadfs.md) guide.</span></span>

## <a name="redeploy-ssrs-reports"></a><span data-ttu-id="a0be1-768">SSRS レポートを再配置する</span><span class="sxs-lookup"><span data-stu-id="a0be1-768">Redeploy SSRS reports</span></span>

#### <a name="version-10013-or-later"></a><span data-ttu-id="a0be1-769">バージョン 10.0.13 、またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="a0be1-769">Version 10.0.13 or later</span></span>

<span data-ttu-id="a0be1-770">ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-770">Run the following command against your business data database (AXDB):</span></span>

```sql
    UPDATE SF.synclog SET STATE=5, SyncStepName = 'ReportSyncstarted' WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CREATIONDATE DESC)
```

#### <a name="version-10012-or-earlier"></a><span data-ttu-id="a0be1-771">バージョン 10.0.12、または以前</span><span class="sxs-lookup"><span data-stu-id="a0be1-771">Version 10.0.12 or earlier</span></span>

<span data-ttu-id="a0be1-772">ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-772">Run the following command against your business data database (AXDB):</span></span>

```sql
    DELETE FROM SF.synclog WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CODEPACKAGEVERSION DESC)
```

>[!NOTE]
> <span data-ttu-id="a0be1-773">バージョン 10.0.12、またはそれ以前のバージョンを使用している場合は、データベース全体が同期されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-773">If you are using version 10.0.12 or earlier, a full database synchronization will be executed.</span></span>

<span data-ttu-id="a0be1-774">コマンドを実行した後、Service Fabric エクスプローラを使用して AOS ノードの 1 つを再起動するか、ノードが実行されている VM を再起動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-774">After running the command, restart one of your AOS nodes through Service Fabric Explorer or restart the VM that the node is running on.</span></span>

## <a name="add-axdbadmin-to-tempdb-after-a-sql-server-restart-via-a-stored-procedure"></a><span data-ttu-id="a0be1-775">ストアド プロシージャ経由で SQL Server を再起動した後、tempdb に axdbadmin を追加します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-775">Add axdbadmin to tempdb after a SQL Server restart via a stored procedure</span></span>

<span data-ttu-id="a0be1-776">SQL Server を再起動すると、tempdb データベースが再作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-776">When SQL Server is restarted, the tempdb database is re-created.</span></span> <span data-ttu-id="a0be1-777">結果として、アクセス許可が不十分です。</span><span class="sxs-lookup"><span data-stu-id="a0be1-777">Therefore, there will be missing permissions.</span></span> <span data-ttu-id="a0be1-778">マスター データベースでストアド プロシージャを作成する次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-778">Run the following script to create a stored procedure on the master database.</span></span>

```sql
\-----
USE [master]
GO
CREATE procedure [dbo].[CREATETEMPDBPERMISSIONS] as begin exec ('USE tempdb; declare @dbaccesscount int; select @dbaccesscount = COUNT(*) from master..syslogins where name = ''axdbadmin''; if (@dbaccesscount <> 0) exec sp_grantdbaccess ''axdbadmin''; ALTER USER [axdbadmin] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''axdbadmin''; EXEC sp_addrolemember N''db_datawriter'', N''axdbadmin''; EXEC sp_addrolemember N''db_ddladmin'', N''axdbadmin''; exec sp_grantdbaccess ''contoso\svc-AXSF$''; ALTER USER [contoso\svc-AXSF$] WITH DEFAULT_SCHEMA=dbo; EXEC sp_addrolemember N''db_datareader'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_datawriter'', N''contoso\svc-AXSF$''; EXEC sp_addrolemember N''db_ddladmin'', N''contoso\svc-AXSF$'';') end
GO
EXEC sp_procoption N'[dbo].[CREATETEMPDBPERMISSIONS]', 'startup', '1'
\-----
```

## <a name="error-updates-to-existing-credential-with-keyid-key-is-not-allowed"></a><span data-ttu-id="a0be1-779">エラー : 「KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません」</span><span class="sxs-lookup"><span data-stu-id="a0be1-779">Error: "Updates to existing credential with KeyId '\<key\>' is not allowed"</span></span>

<span data-ttu-id="a0be1-780">次のエラーが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-780">You might receive the following error:</span></span>

> <span data-ttu-id="a0be1-781">KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません</span><span class="sxs-lookup"><span data-stu-id="a0be1-781">Updates to existing credential with KeyId '\<key\>' is not allowed</span></span>

<span data-ttu-id="a0be1-782">この問題を解決するための手順は、オンプレミス プロジェクトのみをご利用しているか、オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用しているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-782">The steps to resolve this issue depend on whether you have only an on-premises project, or whether you have both an online project and an on-premises project.</span></span>

### <a name="if-have-only-an-on-premises-project"></a><span data-ttu-id="a0be1-783">場合設置プロジェクトのみ</span><span class="sxs-lookup"><span data-stu-id="a0be1-783">If have only an on-premises project</span></span>

<span data-ttu-id="a0be1-784">オンプレミス プロジェクトのみの場合は、KeyId '\<key\>' を使用して既存の資格情報を更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-784">If have only an on-premises project, you can't update the existing credential with KeyId '\<key\>'.</span></span>

> <span data-ttu-id="a0be1-785">New-AzureRmADSpCredential : KeyId '\<key\>' を使用した既存の資格情報の更新は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-785">New-AzureRmADSpCredential : Update to existing credential with KeyId '\<key\>' is not allowed.</span></span>  
> <span data-ttu-id="a0be1-786">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span><span class="sxs-lookup"><span data-stu-id="a0be1-786">At C:\\InfrastructureScripts\\Add-CertToServicePrincipal.ps1:62 char:1</span></span>  
> <span data-ttu-id="a0be1-787">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span><span class="sxs-lookup"><span data-stu-id="a0be1-787">New-AzureRmADSpCredential -ObjectId $servicePrincipal.Id -CertValue $ ...</span></span>  
> <span data-ttu-id="a0be1-788">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span><span class="sxs-lookup"><span data-stu-id="a0be1-788">CategoryInfo : InvalidOperation: (:) \[New-AzureRmADSpCredential\], Exception</span></span>  
> <span data-ttu-id="a0be1-789">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span><span class="sxs-lookup"><span data-stu-id="a0be1-789">FullyQualifiedErrorId : Microsoft.Azure.Commands.ActiveDirectory.NewAzureADSpCredentialCommand</span></span>

<span data-ttu-id="a0be1-790">この問題を解決するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-790">Run the following PowerShell command to resolve the issue.</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
```

### <a name="if-you-have-both-an-online-project-and-an-on-premises-project"></a><span data-ttu-id="a0be1-791">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合</span><span class="sxs-lookup"><span data-stu-id="a0be1-791">If you have both an online project and an on-premises project</span></span>

<span data-ttu-id="a0be1-792">オンライン プロジェクトとオンプレミス プロジェクトの両方をご利用の場合は、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-792">If you have both an online project and an on-premises project, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-793">Microsoft .NET フレームワーク version 4.7.2 がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-793">Verify that the Microsoft .NET Framework version 4.7.2 is installed.</span></span>
2. <span data-ttu-id="a0be1-794">以下のWindows PowerShell スクリプトを実行し、Azure PowerShell moduleをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-794">Run the following Windows PowerShell script to install the Azure PowerShell module.</span></span>

    ```powershell
    Install-Module -Name Az
    ```

3. <span data-ttu-id="a0be1-795">以下のWindows PowerShellスクリプトを実行し、新規証明書をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-795">Run the following Windows PowerShell script to upload the new certificate.</span></span>

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

4. <span data-ttu-id="a0be1-796">複数の証明書が存在する場合は、以下のコマンドを実行して重複する証明書を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-796">Run the following command to remove the duplicate certificate, if more than one certificate exists.</span></span>

    ```powershell
    Remove-AzADSpCredential -ServicePrincipalName "00000015-0000-0000-c000-000000000000" -KeyId <key>
    ```

## <a name="odbc-driver-17-is-required-for-platform-updates"></a><span data-ttu-id="a0be1-797">プラットフォームの更新には ODBC ドライバー 17 が必要です</span><span class="sxs-lookup"><span data-stu-id="a0be1-797">ODBC driver 17 is required for platform updates</span></span>

<span data-ttu-id="a0be1-798">プラットフォーム バイナリを最新に更新するには、Open Database Connectivity ODBC ドライバー 17 を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-798">The latest platform binary update uses Open Database Connectivity (ODBC) driver 17.</span></span> <span data-ttu-id="a0be1-799">このアップグレードでは、古いバージョンの ODBC ドライバーに関連する安定性の問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-799">This upgrade resolves stability issues that are linked to older ODBC drivers.</span></span> <span data-ttu-id="a0be1-800">[追加の設定](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) に関するドキュメントが更新されており、次の変更が記載されています。各AOSサーバーにはODBC ドライバー 17 がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-800">The [Setup perquisites](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#prerequisites) documentation has been updated to reflect the change in which ODBC driver 17 must be installed on each AOS server.</span></span> <span data-ttu-id="a0be1-801">ODBC ドライバー 17 をインストールしない場合は、環境のメンテナンス処理中に DB 同期エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-801">If you don't install ODBC driver 17, you will receive DB Sync errors during servicing of the environment.</span></span>

<span data-ttu-id="a0be1-802">エラーの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-802">Here are some examples of errors:</span></span>

- <span data-ttu-id="a0be1-803">Service Fabric で:</span><span class="sxs-lookup"><span data-stu-id="a0be1-803">In Service Fabric:</span></span>

    > <span data-ttu-id="a0be1-804">問題のあるイベント: SourceId=「System.RA」、プロパティ =「ReplicaOpenStatus」、HealthState=「警告」、ConsiderWarningAsError=false。</span><span class="sxs-lookup"><span data-stu-id="a0be1-804">Unhealthy event: SourceId='System.RA', Property='ReplicaOpenStatus', HealthState='Warning', ConsiderWarningAsError=false.</span></span>  
    > <span data-ttu-id="a0be1-805">レプリカで、AOS3 で開いているときに複数の障害が発生しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-805">Replica had multiple failures during open on AOS3.</span></span> <span data-ttu-id="a0be1-806">API 呼び出し: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</span><span class="sxs-lookup"><span data-stu-id="a0be1-806">API call: IStatelessServiceInstance.Open(); Error = System.Exception (-2146233088)</span></span>  
    > <span data-ttu-id="a0be1-807">**DB の同期に失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="a0be1-807">**DB sync failed.**</span></span>

- <span data-ttu-id="a0be1-808">AOS コンピューターで:</span><span class="sxs-lookup"><span data-stu-id="a0be1-808">On AOS machines:</span></span>

    - <span data-ttu-id="a0be1-809">イベント ビューアー \> カスタム ビュー \> 管理イベント:</span><span class="sxs-lookup"><span data-stu-id="a0be1-809">Event Viewer \> Custom Views \> Administrative Events:</span></span>

        > <span data-ttu-id="a0be1-810">アプリケーション: Microsoft.Dynamics.AX.Deployment.Setup.exe フレームワーク バージョン: v4.0.30319 説明: プロセスは未処理の例外によって中止されました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-810">Application: Microsoft.Dynamics.AX.Deployment.Setup.exe Framework Version: v4.0.30319 Description: The process was terminated due to an unhandled exception.</span></span> <span data-ttu-id="a0be1-811">例外情報: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String\[\])</span><span class="sxs-lookup"><span data-stu-id="a0be1-811">Exception Info: System.IO.FileNotFoundException at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(System.String\[\])</span></span>

    - <span data-ttu-id="a0be1-812">C:\\ProgramData\\SF\\AOSx\\Fabric\\work\\Applications\\AXSFType\_Appxx\\log:</span><span class="sxs-lookup"><span data-stu-id="a0be1-812">C:\\ProgramData\\SF\\AOSx\\Fabric\\work\\Applications\\AXSFType\_Appxx\\log:</span></span>

        > <span data-ttu-id="a0be1-813">Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -metadatadir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</span><span class="sxs-lookup"><span data-stu-id="a0be1-813">Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -metadatadir "C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App18\\AXSF.Code.1.0.20180831174152\\Packages" -sqluser "axdbadmin" -sqlserver "SQL-LS.contoso.com" -sqldatabase "AXDB" -setupmode servicesync -syncmode fullall -onprem</span></span>
        >
        > <span data-ttu-id="a0be1-814">ハンドルされない例外: System.IO.FileNotFoundException: **ファイルまたはアセンブリ 'aoskernel.dll'、あるいはその依存関係のうちのいずれか 1 つを読み込めませんでした。指定されたモジュールが見つかりませんでした。**</span><span class="sxs-lookup"><span data-stu-id="a0be1-814">Unhandled Exception: System.IO.FileNotFoundException: **Could not load file or assembly 'aoskernel.dll' or one of its dependencies. The specified module could not be found.**</span></span>
        > <span data-ttu-id="a0be1-815">Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String\[\] args) にて</span><span class="sxs-lookup"><span data-stu-id="a0be1-815">at Microsoft.Dynamics.AX.Deployment.Setup.Program.Main(String\[\] args)</span></span>
        > 
        > <span data-ttu-id="a0be1-816">**DB の同期に失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="a0be1-816">**DB sync failed.**</span></span>

## <a name="a-no-subscription-found-in-the-context-error-occurs-when-you-run-add-certtoserviceprincipal"></a><span data-ttu-id="a0be1-817">Add-CertToServicePrincipal を実行すると、"コンテキストにサブスクリプションが見つかりません" エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="a0be1-817">A "No subscription found in the context" error occurs when you run Add-CertToServicePrincipal</span></span>

<span data-ttu-id="a0be1-818">最新バージョンの Windows PowerShell が原因で "コンテキストにサブスクリプションが見つかりません" エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-818">Recent versions of Windows PowerShell might cause a "No subscription found in the context" error.</span></span> <span data-ttu-id="a0be1-819">この問題を解決するには、Windows PowerShellのバージョン5.7.0などの古いバージョンをインストールし、上書きしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-819">To resolve this issue, install and load an older version of Windows PowerShell, such as version 5.7.0.</span></span>

```powershell
# Install version 5.7.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 5.7.0

# Load version 5.7.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 5.7.0
```
## <a name="service-fabric-explorer-warnings-occur-after-you-restart-a-machine"></a><span data-ttu-id="a0be1-820">コンピューターの再起動後に Service Fabric Explorer の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="a0be1-820">Service Fabric Explorer warnings occur after you restart a machine</span></span>

<span data-ttu-id="a0be1-821">**エラー:**</span><span class="sxs-lookup"><span data-stu-id="a0be1-821">**Error:**</span></span>

> <span data-ttu-id="a0be1-822">エラー: event: SourceId='MonitoringAgentService', Property='ServiceState'.</span><span class="sxs-lookup"><span data-stu-id="a0be1-822">Error event: SourceId='MonitoringAgentService', Property='ServiceState'.</span></span>  
> <span data-ttu-id="a0be1-823">System.Management.Automation.RuntimeException: エラー: **渡された GUID は WMI データ プロバイダーにより有効と認識されませんでした。**</span><span class="sxs-lookup"><span data-stu-id="a0be1-823">System.Management.Automation.RuntimeException: Error: **The GUID passed was not recognized as valid by a WMI data provider.**</span></span> <span data-ttu-id="a0be1-824">(HRESULT からの例外: 0x80071068)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-824">(Exception from HRESULT: 0x80071068).</span></span> <span data-ttu-id="a0be1-825">スタック トレース:</span><span class="sxs-lookup"><span data-stu-id="a0be1-825">Stack trace:</span></span>

<span data-ttu-id="a0be1-826">**手順:** この問題を解決するには、警告メッセージの原因であるアプリケーション パッケージを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-826">**Steps:** To resolve this issue, restart the application package that generated the warning message.</span></span> <span data-ttu-id="a0be1-827">詳しくは、 [アプリケーション(AOS など)を再起動してください](./troubleshoot-on-prem.md#restartapplications) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-827">For more information, see [Restart applications (such as AOS)](./troubleshoot-on-prem.md#restartapplications).</span></span>

## <a name="the-internal-time-zone-version-number-that-is-stored-in-the-database-is-higher-than-the-version-that-is-supported-by-the-kernel-1312"></a><span data-ttu-id="a0be1-828">データベースに格納されている内部タイム ゾーンのバージョン番号が、カーネル (13/12) でサポートされているバージョンよりも大きくなっています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-828">The internal time zone version number that is stored in the database is higher than the version that is supported by the kernel (13/12)</span></span>

<span data-ttu-id="a0be1-829">このデータベースの同期エラーにより、新しいビルド (プラットフォーム更新 15) があったデータベースの上に古いプラットフォーム ビルド (プラットフォーム更新 12) が配置されてしまう可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-829">This database synchronization error can cause an old platform build (Platform update 12) to be deployed on top of a database that had a newer build (Platform update 15).</span></span>

<span data-ttu-id="a0be1-830">この問題を解決するには、 **SYSTIMEZONESVERSION** の値が重要になります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-830">To resolve this issue, note the **SYSTIMEZONESVERSION** value.</span></span>

```sql
select * from SQLSYSTEMVARIABLES where parm = 'SYSTIMEZONESVERSION'
```

<span data-ttu-id="a0be1-831">エラー メッセージにて表示されたバージョンの値で [value] を更新します</span><span class="sxs-lookup"><span data-stu-id="a0be1-831">Update the value to the version that was returned in the error message.</span></span>

```sql
update SQLSYSTEMVARIABLES set VALUE = 12 where parm = 'SYSTIMEZONESVERSION'
```

## <a name="printing-randomly-stops"></a><span data-ttu-id="a0be1-832">印刷がランダムに停止する</span><span class="sxs-lookup"><span data-stu-id="a0be1-832">Printing randomly stops</span></span>

<span data-ttu-id="a0be1-833">AOS サーバーにインストールされているすべてのネットワーク プリンターが、AXService.EXE プロセスが実行されている Windows サービス アカウントとして実行されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-833">Make sure that all network printers that have been installed on the AOS server are running as the Windows service account that the AXService.EXE process is running as.</span></span>

<span data-ttu-id="a0be1-834">オンプレミス環境でのネットワーク プリンターの構成方法の詳細については、[オンプレミス環境でのネットワーク プリンター デバイスのインストール](../analytics/install-network-printer-onprem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-834">For more information about how to configure network printers in on-premises environments, see [Install network printer devices in on-premises environments](../analytics/install-network-printer-onprem.md).</span></span>

## <a name="ax-databasesynchronize-isnt-populated-with-events"></a><span data-ttu-id="a0be1-835">Ax-DatabaseSynchronize にイベントが設定されていません</span><span class="sxs-lookup"><span data-stu-id="a0be1-835">Ax-DatabaseSynchronize isn't populated with events</span></span>

<span data-ttu-id="a0be1-836">プラットフォームの更新 20 およびそれ以降では、データベース同期ログに問題があり、イベント ビューアーで同期ログが **Ax-DatabaseSynchronize** の下に作成されません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-836">In Platform update 20 and later, there is database synchronization log issue where the synchronization logs aren't written under **Ax-DatabaseSynchronize** in Event Viewer.</span></span>

<span data-ttu-id="a0be1-837">この問題を解決するには、  \<SF-dir\>\\AOS\_\<x\>\\ファブリック\\ワーク\\アプリケーション\\AXSFType\_アプリ\<X\>\\log にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-837">To resolve this issue, go to \<SF-dir\>\\AOS\_\<x\>\\Fabric\\work\\Applications\\AXSFType\_App\<X\>\\log.</span></span> <span data-ttu-id="a0be1-838">例えば次の場所に移動します。 C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log</span><span class="sxs-lookup"><span data-stu-id="a0be1-838">For example, go to C:\\ProgramData\\SF\\AOS\_11\\Fabric\\work\\Applications\\AXSFType\_App183\\log.</span></span> <span data-ttu-id="a0be1-839">ここに、Code\_AXSF\_M\_\<X\>.out ファイル内の DatabaseSynchronize からの出力を示します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-839">Here, you can see the output from DatabaseSynchronize in the Code\_AXSF\_M\_\<X\>.out files.</span></span> <span data-ttu-id="a0be1-840">このコンポーネントに関する問題をトラブルシューティングします。</span><span class="sxs-lookup"><span data-stu-id="a0be1-840">Troubleshoot any issues that pertain to this component.</span></span>

## <a name="you-cant-access-finance--operations-aadsts50058-a-silent-sign-in-request-was-sent-but-no-user-is-signed-in"></a><span data-ttu-id="a0be1-841">Finance + Operations にアクセスできません: 「AADSTS50058: サイレント サインインの要求が送信されましたが、ログインしているユーザーがいません」</span><span class="sxs-lookup"><span data-stu-id="a0be1-841">You can't access Finance + Operations: "AADSTS50058: A silent sign-in request was sent but no user is signed in"</span></span>

<span data-ttu-id="a0be1-842">Finance + Operations へのログイン資格情報を入力すると、ブラウザでアプリケーションのレイアウトが少しの間表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-842">After a user enters credentials to sign in to Finance + Operations, the browser briefly shows the application layout.</span></span> <span data-ttu-id="a0be1-843">しかしその後、Finance + Operations外部へのリダイレクトを試みた結果、次のエラーが出て失敗します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-843">However, it then tries to redirect outside Finance + Operations, but fails with the following error:</span></span>

> <span data-ttu-id="a0be1-844">AADSTS50058: サイレント サインイン要求が送信されましたが、ユーザーがログインしていません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-844">AADSTS50058: A silent sign-in request was sent but no user is signed in.</span></span>

<span data-ttu-id="a0be1-845">ユーザーのセッションを表すために使用する Cookie が Azure AD への要求で送信されませんでした。</span><span class="sxs-lookup"><span data-stu-id="a0be1-845">The cookies that represent the user's session weren't sent in the request to Azure AD.</span></span> <span data-ttu-id="a0be1-846">これは、 Internet Explorer または Microsoft Edge を使用している場合で、webアプリケーションが送信しているサイレント サインインのリクエストが Azure AD エンドポイント (login.microsoftonline.com)とは異なる IEのセキュリティ ゾーンに設定されている場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-846">This issue can occur if the user is using Internet Explorer or Microsoft Edge, and if the web app that sends the silent sign-in request is in a different IE security zone than the Azure AD endpoint (login.microsoftonline.com).</span></span>

<span data-ttu-id="a0be1-847">この問題を解決するには、次の PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-847">This issue occurs because there was a change in the Skype Presence API, and on-premises environments connect to this API by default.</span></span>

<span data-ttu-id="a0be1-848">この問題を解決するには、次の SQL Server query を実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-848">To resolve the issue, run the following SQL Server query.</span></span>

```sql
update [AXDB].[dbo].[SYSCLIENTPERF] set SkypeEnabled = 0
```

<span data-ttu-id="a0be1-849">または、**クライアント パフォーマンス オプション** ページの **Skype プレゼンスが有効** オプションを無効にします (**システム管理** \> **設定** \> **クライアント パフォーマンス オプション**)。</span><span class="sxs-lookup"><span data-stu-id="a0be1-849">Alternatively, turn off the **Skype presence enabled** option on the **Client performance options** page (**System administration** \> **Setup** \> **Client performance options**).</span></span> <span data-ttu-id="a0be1-850">この方法を使用するには、Finance + Operations にログインできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-850">To use this approach, you must be able to sign in to Finance + Operations.</span></span> <span data-ttu-id="a0be1-851">そのため、最初にブラウザのリダイレクトをブロックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-851">Therefore, you must first block redirection in the browser.</span></span> <span data-ttu-id="a0be1-852">Skypeのプレゼンス機能を無効にすると、リダイレクトのブロックを解除しても構いません。</span><span class="sxs-lookup"><span data-stu-id="a0be1-852">After you disable the Skype presence, you can unblock redirection again.</span></span>

<span data-ttu-id="a0be1-853">Chrome ブラウザーでは、最初からリダイレクトがブロックされています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-853">The Google Chrome browser blocks redirection by default.</span></span>

## <a name="error-there-was-an-error-during-codepackage-activation-service-host-failed-to-activate-error0x8007052e"></a><span data-ttu-id="a0be1-854">エラー: CodePackage の有効化でエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-854">Error: "There was an error during CodePackage activation.</span></span> <span data-ttu-id="a0be1-855">サービス ホストの有効化に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-855">Service host failed to activate.</span></span> <span data-ttu-id="a0be1-856">エラー: 0x8007052e"</span><span class="sxs-lookup"><span data-stu-id="a0be1-856">Error:0x8007052e"</span></span>

<span data-ttu-id="a0be1-857">新規インストールの際に以下のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-857">You might receive the following error during a new installation:</span></span>

> <span data-ttu-id="a0be1-858">エラー イベント: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'。</span><span class="sxs-lookup"><span data-stu-id="a0be1-858">Error event: SourceId='System.Hosting', Property='CodePackageActivation:Code:EntryPoint'.</span></span> <span data-ttu-id="a0be1-859">CodePackage の有効化でエラーが発生しました。サービス ホストの有効化に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="a0be1-859">There was an error during CodePackage activation.Service host failed to activate.</span></span> <span data-ttu-id="a0be1-860">エラー: 0x8007052e</span><span class="sxs-lookup"><span data-stu-id="a0be1-860">Error:0x8007052e</span></span>

<span data-ttu-id="a0be1-861">このエラーと同じエラーが、AXSFサービスでも発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-861">This error will cause the AXSF service to fail with the same error.</span></span>

<span data-ttu-id="a0be1-862">この問題を解決するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0be1-862">To resolve this issue, follow these steps.</span></span>

1. <span data-ttu-id="a0be1-863">[エージェント共有パス](setup-deploy-on-premises-pu12.md#setupfile) にて、 **netstandard.dll** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="a0be1-863">In the [agent share path](setup-deploy-on-premises-pu12.md#setupfile), find the **netstandard.dll** file.</span></span> <span data-ttu-id="a0be1-864">このファイルは、例えば \\wp\\\<name\>\\StandaloneSetup-\<ver\>\\Apps\\AOS\\AXServiceApp\\AXSF\\Code\\bin\\netstandard.dll に存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-864">For example, this file might be at \\wp\\\<name\>\\StandaloneSetup-\<ver\>\\Apps\\AOS\\AXServiceApp\\AXSF\\Code\\bin\\netstandard.dll.</span></span>
2. <span data-ttu-id="a0be1-865">それぞれの AOS サーバーにて、管理者権限で コマンド プロンプトを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-865">On each AOS server, open a Command Prompt window as an administrator, and run the following command.</span></span>

    ```Console
    "C:\Program Files (x86)\Microsoft SDKs\Windows\v8.1A\bin\NETFX 4.5.1 Tools\gacutil.exe" -i <path from step 1.>\netstandard.dll /f
    ```

3. <span data-ttu-id="a0be1-866">Service Fabric から **AXBootstrapperApp** を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-866">Delete **AXBootstrapperApp** from Service Fabric.</span></span>

    1. <span data-ttu-id="a0be1-867">**fabric:/Bootstrapper/AXBootstrapper** サービス を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-867">Delete the **fabric:/Bootstrapper/AXBootstrapper** service.</span></span>
    2. <span data-ttu-id="a0be1-868">**fabric:/Bootstrapper** アプリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-868">Delete the **fabric:/Bootstrapper** application.</span></span>
    3. <span data-ttu-id="a0be1-869">**AXBootstrapperAppType** のプロヴィジョニングを解除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-869">Unprovision the **AXBootstrapperAppType** type.</span></span>

4.  <span data-ttu-id="a0be1-870">LCS から環境を再配置します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-870">Redeploy the environment from LCS.</span></span>

## <a name="sql-server-2016-service-pack-2-is-recommended-for-reporting-services-instances"></a><span data-ttu-id="a0be1-871">Reporting Servicesのインスタンス には SQL Server 2016 service pack 2 を推奨します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-871">SQL Server 2016 service pack 2 is recommended for Reporting Services instances</span></span>

<span data-ttu-id="a0be1-872">LCSにてサービス操作を行うと次のエラーが表示されることがあります:</span><span class="sxs-lookup"><span data-stu-id="a0be1-872">When you go through LCS servicing operations, you might receive the following error:</span></span>

> <span data-ttu-id="a0be1-873">プロセスが次のファイルにアクセスできません ' c:\\Program Files\\Microsoft SQL Server\\MSRS13.MSSQLSERVER\\Reporting Services\\ReportServer\\bin\\Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' 別のプロセスによって使用されています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-873">The process cannot access the file 'C:\\Program Files\\Microsoft SQL Server\\MSRS13.MSSQLSERVER\\Reporting Services\\ReportServer\\bin\\Microsoft.Dynamics.AX.Framework.Services.Platform.Client.dll' because it is being used by another process.</span></span>

<span data-ttu-id="a0be1-874">この問題は Reporting Services が Microsoft Dynamics .dllファイル をロックしているために発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-874">This issue occurs because Reporting Services has a lock on a Microsoft Dynamics .dll file.</span></span> <span data-ttu-id="a0be1-875">Reporting Servicesのインスタンスには、SQL Server 2016 service pack 2をインストールすることを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="a0be1-875">We currently recommend that you have SQL Server 2016 service pack 2 installed on Reporting Services instances.</span></span>

> [!NOTE]
> <span data-ttu-id="a0be1-876">サービス パック2のインストールが必要し、累積的な更新を追加または修正プログラムをインストールする必要がないです。</span><span class="sxs-lookup"><span data-stu-id="a0be1-876">You must have service pack 2 installed, and no additional cumulative updates or hotfixes must be installed.</span></span>

## <a name="sysclassrunner-doesnt-run-successfully"></a><a name="SysClassRunner"></a><span data-ttu-id="a0be1-877">SysClassRunner は正常に実行されません</span><span class="sxs-lookup"><span data-stu-id="a0be1-877">SysClassRunner doesn't run successfully</span></span>

<span data-ttu-id="a0be1-878">**問題:** プラットフォーム更新プログラム 29 の SysClassRunner をプラットフォーム更新プログラム 31 を使用して実行しようとすると、次の例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-878">**Issue:** When you try to run SysClassRunner on Platform update 29 through Platform update 31, you get the following exception:</span></span>

```stacktrace 
Microsoft.Dynamics.Ax.Xpp.ClrErrorException: TypeInitializationExeption ---> 
System.TypeInitializationException: The type initializer for 'Microsoft.Dynamics.Ax.Metadata.XppCompiler.CompilerTracer' threw an exception. ---> 
System.TypeInitializationException: The type initializer for 'Microsoft.Dynamics.Ax.DesignTime.Telemetry.OneDS' threw an exception. ---> 
System.IO.FileLoedAxception: Could not load file or assembly 'Microsoft.Diagnostics.Tracing.TraceEvent, Version=2.0.43.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a' or one of its dependencies. 
The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) at Microsoft.Dynamics.Ax.DesignTime.Telemetry.OneDS.cctor() 
--- End of inner exception stack trace ---
```

<span data-ttu-id="a0be1-879">**理由:** ランタイムとアプリケーションとの間に .dll の不一致があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-879">**Reason:** There is a .dll mismatch between the runtime and the application.</span></span>

<span data-ttu-id="a0be1-880">**解決策** : TSG\_SysClassRunner.ps1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-880">**Resolution:** Use TSG\_SysClassRunner.ps1.</span></span> <span data-ttu-id="a0be1-881">詳細については、[TSG_SysClassRunner.ps1](onprem-tsg-implementations.md#sysclassrunner)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-881">For more information, see [TSG_SysClassRunner.ps1](onprem-tsg-implementations.md#sysclassrunner).</span></span>

## <a name="dbsync-fails-with-peap-app-version-1009-platform-update-33"></a><span data-ttu-id="a0be1-882">DBSync が PEAP APP バージョン 10.0.9 プラットフォーム更新プログラム 33 で失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-882">DBSync fails with PEAP APP version 10.0.9 Platform update 33</span></span>
<span data-ttu-id="a0be1-883">**問題:** APP 10.0.9 PU33 PEAP パッケージの配置中に、AXSF アプリケーションの配置が Service Fabric エクスプローラーで「Inbuild」ステータスになると失敗する。</span><span class="sxs-lookup"><span data-stu-id="a0be1-883">**Issue:** During deployment of the APP 10.0.9 PU33 PEAP-package, the deployment fails with the AXSF applications staying in "InBuild" status in Service Fabric explorer.</span></span> <span data-ttu-id="a0be1-884">AXSF ノードの作業ディレクトリのログを確認すると、次の DBSync エラーが見つかります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-884">When reviewing the logs on the AXSF nodes's work directories, the following DBSync error can be found.</span></span> 

<span data-ttu-id="a0be1-885">DBSync からのエラー メッセージ:</span><span class="sxs-lookup"><span data-stu-id="a0be1-885">Error message from DBSync:</span></span>
 ```stacktrace
 Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "C:\ProgramData\SF\LBDEN08FS1AOS03\Fabric\work\Applications\AXSFType_App398\AXSF.Code.1.0.20200123151456\Packages" -metadatadir "C:\ProgramData\SF\LBDEN08FS1AOS03\Fabric\work\Applications\AXSFType_App398\AXSF.Code.1.0.20200123151456\Packages" -sqluser "" -sqlserver "" -sqldatabase "" -setupmode servicesync -syncmode fullall -onprem 
Stack trace: Invalid attempt to call  running in CIL on the client.
   at Microsoft.Dynamics.Ax.MSIL.Interop.throwException(Int32 ExceptionValue, interpret* ip)
   at Microsoft.Dynamics.Ax.MSIL.Interop.ThrowCQLError(IL_CQL_ERR cqlErr, String p1)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrow(Exception exception)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrowFormattedMessage(Exception exception, String typeName, String elementName)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.LogOrRethrowFormattedMessage(Exception exception, String typeName, Int32 typeId)
   at Microsoft.Dynamics.AX.Kernel.ApplicationId.ApplicationIdBridge.LoadTableById(ApplicationIdBridge* , Int32 id, ObjectIdDelegate* cb)
   at cqlClass.callEx(cqlClass* , Char* , interpret* )
   at Microsoft.Dynamics.Ax.MSIL.cqlClassIL.Call(IntPtr c, String methodName, Object[] parameters, Type[] types, Object[] varargs, Type[] varargsTypes)
   at Microsoft.Dynamics.Ax.Xpp.XppObjectBase.Call(String methodName, Object[] parameters, Type[] types, Object[] varargs)
   at Microsoft.Dynamics.Ax.Xpp.DictTable.Supportinheritance()
   at Dynamics.AX.Application.SysDictTable.`getRootTable(Int32 _tabid) in xppSource://Source/ApplicationPlatform\AxClass_SysDictTable.xpp:line 1498
   at Dynamics.AX.Application.SysDictTable.getRootTable(Int32 _tabid)
   at Dynamics.AX.Application.SysDataBaseLog.`ConfigureSqlLogging() in xppSource://Source/ApplicationPlatform\AxTable_SysDataBaseLog.xpp:line 60
   at Dynamics.AX.Application.SysDataBaseLog.ConfigureSqlLogging()
   at SysDataBaseLog::ConfigureSqlLogging(Object[] , Boolean& )
   at Microsoft.Dynamics.Ax.Xpp.ReflectionCallHelper.MakeStaticCall(Type type, String MethodName, Object[] parameters)
 
DB sync failed.
```

<span data-ttu-id="a0be1-886">**理由:** この問題が発生するのは、SQL DatabaseLog テーブルに、パッケージ内のメタデータと競合するデータが含まれているためです。</span><span class="sxs-lookup"><span data-stu-id="a0be1-886">**Reason:** This issue occurs because there is data in the SQL DatabaseLog table that conflicts with the metadata in the package.</span></span>

<span data-ttu-id="a0be1-887">**解決策:** AXDB 上で次のクエリを実行して DatabaseLog テーブルをクリーンアップしてから、配置を再試行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-887">**Resolution:** Run the following query on AXDB to clean the DatabaseLog table and retry the deployment.</span></span>

```sql
select * into databaselog_bak from databaselog
truncate table databaselog
```

## <a name="dbsync-fails-to-start"></a><span data-ttu-id="a0be1-888">DBSync が起動に失敗する</span><span class="sxs-lookup"><span data-stu-id="a0be1-888">DBSync fails to start</span></span>

<span data-ttu-id="a0be1-889">**問題 :** AXSF アプリケーションが Service Fabric explorer で "InBuild" の状態のままとなり、配置が失敗する。</span><span class="sxs-lookup"><span data-stu-id="a0be1-889">**Issue:** During deployment, the deployment fails with the AXSF applications staying in "InBuild" status in Service Fabric explorer.</span></span> <span data-ttu-id="a0be1-890">AXSF ノードの作業ディレクトリのログを確認すると、次の DBSync エラーが見つかります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-890">When reviewing the logs on the AXSF nodes's work directories, the following DBSync error can be found.</span></span>

```stacktrace
Microsoft.Dynamics.AX.InitializationException: Database login failed. Please check SQL credentials and try again.
   at Microsoft.Dynamics.AX.AOS.StartupInternal(String[] Arguments)
   at Microsoft.Dynamics.AX.AOS.Startup()
   at Microsoft.Dynamics.AX.AosConfig.?A0xb5100bbf.GetAosConfig()
   at Microsoft.Dynamics.AX.AosConfig.Config.InitInternal()
   at Microsoft.Dynamics.AX.AosConfig.Config.InitOnce(Boolean isOfflineMode)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.StartAosCode(SyncOptions syncOptions, String sqlConnectionString)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.ExecuteWithinAOS(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Func`1 func, Action`1 errorHandler)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.NOTE_LeavingSynchronizer_CallStackAboveThisLineIsCustomCode(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Action`1 a)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.LegacyCodepath.RunCustomAction(SyncOptions syncOptions, String sqlConnectionString, IMetadataProvider metadataProvider, Action`1 a)
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.PreTableSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.FullSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.RunSync()
   at Microsoft.Dynamics.AX.Framework.Database.Tools.SyncEngine.Run(String metadataDirectory, String sqlConnectionString, SyncOptions options)
```

<span data-ttu-id="a0be1-891">**理由 :** この問題は、SQL パスワードに特殊文字が含まれていることが原因で発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0be1-891">**Reason:** This issue may occur because the SQL password contains special characters.</span></span>

<span data-ttu-id="a0be1-892">**解決策 :** SQL ユーザーのパスワードを更新し、特殊文字を削除します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-892">**Resolution:** Update the password of the SQL user and remove the special characters.</span></span> <span data-ttu-id="a0be1-893">続いて、新しいパスワードを使用して Credentials.json ファイルを更新し、LCS から配置作業を再試行します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-893">Then, update the Credentials.json file with the new password and retry the deployment from LCS.</span></span>

## <a name="dbsync-fails-with-peap-and-first-release-app-version-10014-platform-update-38"></a><span data-ttu-id="a0be1-894">DBSync は PEAP と 初回リリースの APP のバージョン 10.0.14、更新プログラム 38 でエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="a0be1-894">DBSync fails with PEAP and first release APP version 10.0.14 Platform update 38</span></span>

<span data-ttu-id="a0be1-895">**問題 :** AXSF アプリケーションが Service Fabric explorer で "InBuild" の状態のままとなり、配置が失敗する。</span><span class="sxs-lookup"><span data-stu-id="a0be1-895">**Issue:** During deployment, the deployment fails with the AXSF applications staying in "InBuild" status in Service Fabric explorer.</span></span> <span data-ttu-id="a0be1-896">AXSF ノードの作業ディレクトリでログを確認する場合、以下の DBSync エラーが複数回発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-896">When reviewing the logs on the AXSF nodes's work directories, the following DBSync error is present multiple times.</span></span>

```stacktrace
10/01/2020 14:49:25: Failed when creating deadlock capture session event System.Data.SqlClient.SqlException (0x80131904): User does not have permission to perform this action.
   at System.Data.SqlClient.SqlConnection.OnError(SqlException exception, Boolean breakConnection, Action`1 wrapCloseInAction)
   at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj, Boolean callerHasConnectionLock, Boolean asyncClose)
   at System.Data.SqlClient.TdsParser.TryRun(RunBehavior runBehavior, SqlCommand cmdHandler, SqlDataReader dataStream, BulkCopySimpleResultSet bulkCopyHandler, TdsParserStateObject stateObj, Boolean& dataReady)
   at System.Data.SqlClient.SqlCommand.RunExecuteNonQueryTds(String methodName, Boolean async, Int32 timeout, Boolean asyncWrite)
   at System.Data.SqlClient.SqlCommand.InternalExecuteNonQuery(TaskCompletionSource`1 completion, String methodName, Boolean sendToPipe, Int32 timeout, Boolean& usedCache, Boolean asyncWrite, Boolean inRetry)
   at System.Data.SqlClient.SqlCommand.ExecuteNonQuery()
   at Microsoft.Dynamics.AX.Framework.Database.Monitor.DeadlockMonitor.CreateDeadlockTrackingSystemEvent()
```

<span data-ttu-id="a0be1-897">**理由:** この問題は、Finance+Operations で使用している SQL Server アカウントに操作を実行するための十分な権限がないことによって発生します。</span><span class="sxs-lookup"><span data-stu-id="a0be1-897">**Reason:** This issue occurs because the SQL Server account used by Finance + Operations does not have sufficient permissions to execute the operation.</span></span>

<span data-ttu-id="a0be1-898">**解決:** SQL Server で下記のコマンドを実行してください。</span><span class="sxs-lookup"><span data-stu-id="a0be1-898">**Resolution:** Execute the following command in your SQL Server:</span></span>

```sql
use master
GRANT ALTER ANY EVENT SESSION to axdbadmin;
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
