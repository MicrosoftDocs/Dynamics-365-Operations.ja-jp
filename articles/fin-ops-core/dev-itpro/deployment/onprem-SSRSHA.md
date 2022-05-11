---
title: SQL Server Reporting Services (SSRS) ノードの高可用性を構成する
description: このトピックでは、Dynamics 365 Finance + Operations (on-premises) 展開用に Microsoft SQL Server Reporting Services (SSRS) ノードを構成する方法について説明します。
author: faix
ms.date: 02/22/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-03-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0cdedfa3c904ed2719af738d54211b96080c72ab
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565948"
---
# <a name="configure-high-availability-for-sql-server-reporting-services-ssrs-nodes"></a>SQL Server Reporting Services (SSRS) ノードの高可用性を構成する

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance + Operations (on-premises) 展開用に複数の Microsoft SQL Server Reporting Services (SSRS) ノードを構成する方法について説明します。

## <a name="high-availability-with-windows-failover-clusters"></a>Windows フェールオーバー クラスターによる高可用性

このシナリオでは、Windows フェールオーバー クラスターを使用します。 したがって、すべての要求を受信する 1 つのアクティブなノードと、1 つのアイドルなパッシブ ノードが必要になります。 アクティブなノードが使用できなくなると、クラスターはこのイベントを検出し、パッシブ ノードはすべてのネットワーク トラフィックの受信を開始します。

このトピックでは、Windows フェールオーバー クラスターの設定についてカバーしていません。 詳細については、[フェールオーバー クラスターを作成する](/windows-server/failover-clustering/create-failover-cluster)を参照してください。

クラスターの設定後に、インストールを構成できます。 以下の例は、次の図に表示される情報に基づいています。

![Windows フェールオーバー クラスター構成の例。](./media/WFC.png)

1. 構成ファイル (**ConfigTemplate.xml**) を更新します。

    1. レポート サービス ブートストラッパー サービスの **ADServiceAccount** を更新します。

        ```xml
        <ADServiceAccount type="gMSA" name="svc-ReportSvc$" refName="gmsaSSRS">
            <DNSHostName>svc-ReportSvc.contosoen05.com</DNSHostName>
        </ADServiceAccount>
        ```

    1. **ServiceFabricCluster** セクションの **ReportServerType** で、すべてのサーバーがリストされていることを確認します。

        ```xml
        <NodeType name="ReportServerType" primary="false" namePrefix="Rep" purpose="BI">
            <VMList>
                <VM name="LBDEN05FS1BI1" ipAddress="10.179.108.10" faultDomain="fd:/fd1" updateDomain="ud1"/>
                <VM name="LBDEN05FS1BI2" ipAddress="10.179.108.11" faultDomain="fd:/fd2" updateDomain="ud2"/>
            </VMList>
        </NodeType>
        ```

    1. **SSRSHTTPS** 証明書の設定を更新します。
        
        この例は、上記のスクリーン ショットを使用して構成されています。 **件名** 属性は、クライアント アクセス名に設定する必要があります。 また、名前とファイル名を同じ値に設定すると便利です。 **DNSName** には、優先所有者ごとのエントリと、クライアント アクセス名があります。 
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
    > 証明書を生成するために用意されているインフラストラクチャ スクリプトを使用しない場合でも、他のスクリプトはその情報に依存するため、証明書情報を入力する必要があります。

1. セットアップ ガイドに従って、通常の方法で設定を完了します。

    > [!IMPORTANT]
    > Azure Service Fabric Cluster を既に作成している場合は、ノードがクラスターに追加されていることを確認してください。
    >
    > Export-PfxFiles.ps1 スクリプトを再実行し、適切なマシンで Complete-Prereqs.ps1 スクリプトを再実行して、SSRS Web サーバーの証明書がすべての ReportServer ノードに配布されていることを確認します。

## <a name="high-availability-with-load-balancers"></a>ロード バランサの高可用性

このシナリオでは、使用可能な異なるノード間で要求を配分するようにロード バランサが構成されています。 これらの要求には、すべてのレポート生成要求が含まれます。

この構成を設定する際は、セッション アフィニティを設定する必要があることに注意してください。 選択したソリューションは、この要件を **サポートしている必要があります**。 必要なセッション アフィニティのタイプはクライアントによって異なります。 Application Object Server (AOS) ノードが要求を行う場合、ロード バランサは、その AOS ノードに対するすべての要求を同じ SSRS ノードに送信する必要があります。

このトピックには、特定のソフトウェア ロード バランサまたはハードウェア ロード バランサを設定するための手順は含まれていません。

このシナリオの一般的な概要は次のとおりです。

1. 負荷分散戦略または製品を選択します。
1. ネットワーク トポロジに従って戦略または製品を構成します。
1. クライアント (ソース IP) アフィニティを設定したことを確認します。
1. **ConfigTemplate.xml** ファイルを更新します。 前の例をガイドとして使用してください。
1. 通常の方法でクラスターの設定を続行します。

> [!IMPORTANT]
> Service Fabric Cluster を既に作成している場合は、追加ノードがクラスターに追加されていることを確認してください。
>
> Export-PfxFiles.ps1 スクリプトを再実行し、適切なマシンで Complete-Prereqs.ps1 スクリプトを再実行して、SSRS Web サーバーの証明書がすべての ReportServer ノードに配布されていることを確認します。

## <a name="deployed-environments-where-the-base-deployment-is-earlier-than-platform-update-41"></a>基本配置が Platform update 41 より前の配置環境

> [!NOTE]
> この構成は、Platform update 41 以降の配置でのみサポートされます。

既存の環境で SSRS ノードの高可用性を有効にする場合は、配置前スクリプトを使用できます。 配置前スクリプトの詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../lifecycle-services/pre-post-scripts.md)を参照してください。

### <a name="predeployment-script"></a>配置前スクリプト

#### <a name="invoke-command-example"></a>コマンド例の呼び出し

```powershell
Configure-SSRSHA.ps1 -AgentShare "\\servername\D365FFOAgent" -Listener "LBDEN05FS1BI" -MachinesList "LBDEN05FS1BI1,LBDEN05FS1BI2" -TLSCertificateThumbprint "<cert thumbprint>" -ServiceAccount "contosoen05\svc-ReportSvc$"
```

> [!NOTE]
> これらの例の値は、[Windows フェールオーバー クラスターの高可用性](#high-availability-with-windows-failover-clusters)セクションの **ConfigTemplate.xml** ファイルで使用されている値に従って入力されています。

#### <a name="configure-ssrshaps1-script"></a>Configure-SSRSHA.ps1 スクリプト

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
    $SsrsServicePort = "443"
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
        $component.parameters.biReporting.ssrsHttpsPort.value = $SsrsServicePort
    }
    elseif($component.name -eq "ReportingServices")
    {
        $component.parameters.enableSecurity.value = "True"
        $component.parameters.ssrsSslCertificateThumbprint.value = $TLSCertificateThumbprint
        $component.parameters.ssrsServerFqdn.value = $Listener
        $component.parameters.principalUserAccountType.value = "ManagedServiceAccount"
        $component.parameters.principalUserAccountName.value = $ServiceAccount
        $component.parameters.reportingServers.value = $MachinesList
        $component.parameters.ssrsHttpsPort.value = $SsrsServicePort
    }

    $updatedComponents += $component
}

$configJson.components = $updatedComponents

$configJson | ConvertTo-Json -Depth 100 | Out-File $configJsonPath

Write-Host "Successfully updated the configuration for SSRS HA."
```
