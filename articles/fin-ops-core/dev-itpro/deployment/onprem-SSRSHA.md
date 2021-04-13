---
title: SQL Server Reporting Services (SSRS) ノードの高可用性を構成する
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 展開用に Microsoft SQL Server Reporting Services (SSRS) ノードを構成する方法について説明します。
author: faix
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-03-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 94779fd90af4d25b792043db92c5d237372cab20
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745333"
---
# <a name="configure-high-availability-for-sql-server-reporting-services-ssrs-nodes"></a><span data-ttu-id="8ecdc-103">SQL Server Reporting Services (SSRS) ノードの高可用性を構成する</span><span class="sxs-lookup"><span data-stu-id="8ecdc-103">Configure high availability for SQL Server Reporting Services (SSRS) nodes</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8ecdc-104">このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 展開用に複数の Microsoft SQL Server Reporting Services (SSRS) ノードを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-104">This topic explains how to configure multiple Microsoft SQL Server Reporting Services (SSRS) nodes for Dynamics 365 Finance + Operations (on-premises) deployments.</span></span>

## <a name="high-availability-with-windows-failover-clusters"></a><span data-ttu-id="8ecdc-105">Windows フェールオーバー クラスターによる高可用性</span><span class="sxs-lookup"><span data-stu-id="8ecdc-105">High availability with Windows failover clusters</span></span>

<span data-ttu-id="8ecdc-106">このシナリオでは、Windows フェールオーバー クラスターを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-106">This scenario uses Windows failover clusters.</span></span> <span data-ttu-id="8ecdc-107">したがって、すべての要求を受信する 1 つのアクティブなノードと、1 つのアイドルなパッシブ ノードが必要になります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-107">Therefore, you will have one active node that receives all requests and one passive node that is idle.</span></span> <span data-ttu-id="8ecdc-108">アクティブなノードが使用できなくなると、クラスターはこのイベントを検出し、パッシブ ノードはすべてのネットワーク トラフィックの受信を開始します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-108">If the active node becomes unavailable, the cluster will detect this event, and the passive node will start to receive all network traffic.</span></span>

<span data-ttu-id="8ecdc-109">このトピックでは、Windows フェールオーバー クラスターの設定についてカバーしていません。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-109">This topic doesn't cover the setup of Windows failover clusters.</span></span> <span data-ttu-id="8ecdc-110">詳細については、[フェールオーバー クラスターを作成する](https://docs.microsoft.com/windows-server/failover-clustering/create-failover-cluster)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-110">For information, see [Create a failover cluster](https://docs.microsoft.com/windows-server/failover-clustering/create-failover-cluster).</span></span>

<span data-ttu-id="8ecdc-111">クラスターの設定後に、インストールを構成できます。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-111">After the cluster is set up, you can configure your installation.</span></span> <span data-ttu-id="8ecdc-112">以下の例は、次の図に表示される情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-112">The examples below will be based on the information displayed in the following illustration.</span></span>

![Windows フェールオーバー クラスター構成の例](./media/WFC.png)

1. <span data-ttu-id="8ecdc-114">構成ファイル (**ConfigTemplate.xml**) を更新します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-114">Update your configuration file (**ConfigTemplate.xml**):</span></span>

    1. <span data-ttu-id="8ecdc-115">レポート サービス ブートストラッパー サービスの **ADServiceAccount** を更新します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-115">Update **ADServiceAccount** for the reporting service bootstrapper service.</span></span>

        ```xml
        <ADServiceAccount type="gMSA" name="svc-ReportSvc$" refName="gmsaSSRS">
            <DNSHostName>svc-ReportSvc.contosoen05.com</DNSHostName>
        </ADServiceAccount>
        ```

    1. <span data-ttu-id="8ecdc-116">**ServiceFabricCluster** セクションの **ReportServerType** で、すべてのサーバーがリストされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-116">In the **ServiceFabricCluster** section, under **ReportServerType**, make sure that all your servers are listed.</span></span>

        ```xml
        <NodeType name="ReportServerType" primary="false" namePrefix="Rep" purpose="BI">
            <VMList>
                <VM name="LBDEN05FS1BI1" ipAddress="10.179.108.10" faultDomain="fd:/fd1" updateDomain="ud1"/>
                <VM name="LBDEN05FS1BI2" ipAddress="10.179.108.11" faultDomain="fd:/fd2" updateDomain="ud2"/>
            </VMList>
        </NodeType>
        ```

    1. <span data-ttu-id="8ecdc-117">**SSRSHTTPS** 証明書の設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-117">Update the **SSRSHTTPS** certificate settings.</span></span>
        
        <span data-ttu-id="8ecdc-118">この例は、上記のスクリーン ショットを使用して構成されています。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-118">This example has been configured using the screenshot shown above.</span></span> <span data-ttu-id="8ecdc-119">**件名** 属性は、クライアント アクセス名に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-119">The **Subject** attribute should be set to the client access name.</span></span> <span data-ttu-id="8ecdc-120">また、名前とファイル名を同じ値に設定すると便利です。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-120">Additionally, for convenience, we have set the name and file name to be the same value.</span></span> <span data-ttu-id="8ecdc-121">**DNSName** には、優先所有者ごとのエントリと、クライアント アクセス名があります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-121">For the **DNSName** we have an entry for each of the preferred owners, as well as the client access name.</span></span> 
        ```xml
        <Certificate type="SSRSHTTPS" exportable="true" generateSelfSignedCert="false" generateADCSCert="true">
            <!-- Specify the friendly name of the certificate during import operations. -->
            <Name>LBDEN05FS1BI</Name>
            <!-- Specify the file name of the pfx that will be used in export and import operations. If not specified, the name property will be used -->
            <FileName>LBDEN05FS1BI</FileName>
            <!-- Specify the DNS names for the listener, and of each of the report nodes in the cluster. -->
            <!-- The FQDNS will only be accessed from within the environment so it's not necessary to create external DNS entries for them. -->
            <DNSName>LBDEN05FS1BI;LBDEN05FS1BI1;LBDEN05FS1BI2</DNSName>
            <Subject>LBDEN05FS1BI</Subject>
            <Thumbprint></Thumbprint>
            <ProtectTo></ProtectTo>
        </Certificate>
        ```

    > [!IMPORTANT]
    > <span data-ttu-id="8ecdc-122">証明書を生成するために用意されているインフラストラクチャ スクリプトを使用しない場合でも、他のスクリプトはその情報に依存するため、証明書情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-122">Even if you won't be using the infrastructure scripts that are provided to generate the certificate, you should fill in the certificate information, because other scripts will rely on that information.</span></span>

1. <span data-ttu-id="8ecdc-123">セットアップ ガイドに従って、通常の方法で設定を完了します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-123">Follow the setup guide to complete the setup in your usual way.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8ecdc-124">Azure Service Fabric Cluster を既に作成している場合は、ノードがクラスターに追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-124">If you've already created the Azure Service Fabric cluster, make sure that the nodes are added to it.</span></span>
    >
    > <span data-ttu-id="8ecdc-125">Export-PfxFiles.ps1 スクリプトを再実行し、適切なマシンで Complete-Prereqs.ps1 スクリプトを再実行して、SSRS Web サーバーの証明書がすべての ReportServer ノードに配布されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-125">Rerun the Export-PfxFiles.ps1 script, and rerun the Complete-Prereqs.ps1 script on the appropriate machines, to ensure that the certificate for the SSRS web server is distributed to all the ReportServer nodes.</span></span>

## <a name="high-availability-with-load-balancers"></a><span data-ttu-id="8ecdc-126">ロード バランサの高可用性</span><span class="sxs-lookup"><span data-stu-id="8ecdc-126">High availability with load balancers</span></span>

<span data-ttu-id="8ecdc-127">このシナリオでは、使用可能な異なるノード間で要求を配分するようにロード バランサが構成されています。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-127">In this scenario, a load balancer is configured to distribute requests among the different nodes that are available.</span></span> <span data-ttu-id="8ecdc-128">これらの要求には、すべてのレポート生成要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-128">These requests include all report generation requests.</span></span>

<span data-ttu-id="8ecdc-129">この構成を設定する際は、セッション アフィニティを設定する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-129">When you set up this configuration, note that you must set up session affinity.</span></span> <span data-ttu-id="8ecdc-130">選択したソリューションは、この要件を **サポートしている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-130">The solution that you select **must** support this requirement.</span></span> <span data-ttu-id="8ecdc-131">必要なセッション アフィニティのタイプはクライアントによって異なります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-131">The type of session affinity that is required depends on the client.</span></span> <span data-ttu-id="8ecdc-132">Application Object Server (AOS) ノードが要求を行う場合、ロード バランサは、その AOS ノードに対するすべての要求を同じ SSRS ノードに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-132">When the Application Object Server (AOS) node makes a request, the load balancer should direct all requests for that AOS node to the same SSRS node.</span></span>

<span data-ttu-id="8ecdc-133">このトピックには、特定のソフトウェア ロード バランサまたはハードウェア ロード バランサを設定するための手順は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-133">This topic doesn't include instructions for setting up a specific software load balancer or hardware load balancer.</span></span>

<span data-ttu-id="8ecdc-134">このシナリオの一般的な概要は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-134">Here is a general overview of this scenario:</span></span>

1. <span data-ttu-id="8ecdc-135">負荷分散戦略または製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-135">Choose a load balancing strategy or product.</span></span>
1. <span data-ttu-id="8ecdc-136">ネットワーク トポロジに従って戦略または製品を構成します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-136">Configure the strategy or product according to your network topology.</span></span>
1. <span data-ttu-id="8ecdc-137">クライアント (ソース IP) アフィニティを設定したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-137">Make sure that you've set up client (source IP) affinity.</span></span>
1. <span data-ttu-id="8ecdc-138">**ConfigTemplate.xml** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-138">Update the **ConfigTemplate.xml** file.</span></span> <span data-ttu-id="8ecdc-139">前の例をガイドとして使用してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-139">Use the previous example as a guide.</span></span>
1. <span data-ttu-id="8ecdc-140">通常の方法でクラスターの設定を続行します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-140">Continue to set up the cluster in your usual way.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ecdc-141">Service Fabric Cluster を既に作成している場合は、追加ノードがクラスターに追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-141">If you've already created the Service Fabric cluster, make sure that the additional nodes are added to it.</span></span>
>
> <span data-ttu-id="8ecdc-142">Export-PfxFiles.ps1 スクリプトを再実行し、適切なマシンで Complete-Prereqs.ps1 スクリプトを再実行して、SSRS Web サーバーの証明書がすべての ReportServer ノードに配布されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-142">Rerun the Export-PfxFiles.ps1 script, and rerun the Complete-Prereqs.ps1 script on the appropriate machines, to ensure that the certificate for the SSRS web server is distributed to all the ReportServer nodes.</span></span>

## <a name="deployed-environments-where-the-base-deployment-is-earlier-than-platform-update-41"></a><span data-ttu-id="8ecdc-143">基本配置が Platform update 41 より前の配置環境</span><span class="sxs-lookup"><span data-stu-id="8ecdc-143">Deployed environments where the base deployment is earlier than Platform update 41</span></span>

> [!NOTE]
> <span data-ttu-id="8ecdc-144">この構成は、Platform update 41 以降の配置でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-144">This configuration is supported only for Platform update 41 and later deployments.</span></span>

<span data-ttu-id="8ecdc-145">既存の環境で SSRS ノードの高可用性を有効にする場合は、配置前スクリプトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-145">If you want to enable high availability for the SSRS nodes in existing environments, you can use a predeployment script.</span></span> <span data-ttu-id="8ecdc-146">配置前スクリプトの詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../lifecycle-services/pre-post-scripts.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-146">For more information about predeployment scripts, see [Local agent pre-deployment and post-deployment scripts](../lifecycle-services/pre-post-scripts.md).</span></span>

### <a name="predeployment-script"></a><span data-ttu-id="8ecdc-147">配置前スクリプト</span><span class="sxs-lookup"><span data-stu-id="8ecdc-147">Predeployment script</span></span>

#### <a name="invoke-command-example"></a><span data-ttu-id="8ecdc-148">コマンド例の呼び出し</span><span class="sxs-lookup"><span data-stu-id="8ecdc-148">Invoke command example</span></span>

```powershell
Configure-SSRSHA.ps1 -AgentShare "\\servername\D365FFOAgent" -Listener "LBDEN05FS1BI" -MachinesList "LBDEN05FS1BI1,LBDEN05FS1BI2" -TLSCertificateThumbprint "<cert thumbprint>" -ServiceAccount "contosoen05\svc-ReportSvc$"
```

> [!NOTE]
> <span data-ttu-id="8ecdc-149">これらの例の値は、[Windows フェールオーバー クラスターの高可用性](#high-availability-with-windows-failover-clusters)セクションの **ConfigTemplate.xml** ファイルで使用されている値に従って入力されています。</span><span class="sxs-lookup"><span data-stu-id="8ecdc-149">These example values have been filled out according to the values used in the **ConfigTemplate.xml** file from the [High availability with Windows failover clusters](#high-availability-with-windows-failover-clusters) section.</span></span>

#### <a name="configure-ssrshaps1-script"></a><span data-ttu-id="8ecdc-150">Configure-SSRSHA.ps1 スクリプト</span><span class="sxs-lookup"><span data-stu-id="8ecdc-150">Configure-SSRSHA.ps1 script</span></span>

```powershell
param (
    [Parameter(Mandatory=$true)]
    [string]
    $AgentShare,

    [Parameter(Mandatory=$true)]
    [string]
    $Listener,

    [Parameter(Mandatory=$true)]
    [string]
    $MachinesList,

    [Parameter(Mandatory=$true)]
    [string]
    $TLSCertificateThumbprint,

    [Parameter(Mandatory=$true)]
    [string]
    $ServiceAccount,

    [string]
    $ssrsServicePort = ""
)

$ErrorActionPreference = "Stop"

$basePath = Get-ChildItem $AgentShare\wp\*\StandaloneSetup-*\ |
    Select-Object -First 1 -Expand FullName

if(!(Test-Path $basePath))
{
    Write-Error "Basepath: $basePath , not found" -Exception InvalidOperation
}

$configJsonPath = "$basePath\config.json"

$configJson = Get-Content $configJsonPath | ConvertFrom-Json

$updatedComponents = @()
foreach ($component in $configJson.components)
{
    if($component.name -eq "AOS")
    {
        $component.parameters.biReporting.persistentVirtualMachineIPAddressSSRS.value = $Listener
        $component.parameters.biReporting.reportingServers.value = $MachinesList
        $component.parameters.biReporting.ssrsUseHttps.value = "True"
        $component.parameters.biReporting.ssrsHttpsPort.value = $ssrsServicePort
    }
    elseif($component.name -eq "ReportingServices")
    {
        $component.parameters.enableSecurity.value = "True"
        $component.parameters.ssrsSslCertificateThumbprint.value = $TLSCertificateThumbprint
        $component.parameters.ssrsServerFqdn.value = $Listener
        $component.parameters.principalUserAccountType.value = "ManagedServiceAccount"
        $component.parameters.principalUserAccountName.value = $ServiceAccount
        $component.parameters.reportingServers.value = $MachinesList
        $component.parameters.ssrsHttpsPort.value = $ssrsServicePort
    }

    $updatedComponents += $component
}

$configJson.components = $updatedComponents

$configJson | ConvertTo-Json -Depth 100 | Out-File $configJsonPath

Write-Host "Successfully updated the configuration for SSRS HA."
```
