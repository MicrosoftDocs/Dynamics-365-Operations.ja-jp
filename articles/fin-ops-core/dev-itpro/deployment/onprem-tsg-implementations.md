---
title: オンプレミス環境の問題を解決するためのスクリプト
description: このトピックは、オンプレミス環境の問題を修正するために使用できるスクリプトの中央レポジトリとして機能します。
author: faix
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-11-30]
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: a53ceb54ca7119d7c13c574326a68cfcea6b4751
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774075"
---
# <a name="scripts-for-resolving-issues-in-on-premises-environments"></a>オンプレミス環境の問題を解決するためのスクリプト
[!include [banner](../includes/banner.md)]

このトピックは、オンプレミス環境の問題を修正するために使用できるスクリプトの中央レポジトリとして機能します。 通常、これらのスクリプトは配置前スクリプトまたは配置後スクリプトとして実行する必要があります。

オンプレミス環境における問題の解決方法の詳細については、 [オンプレミス配置のトラブルシューティング](troubleshoot-on-prem.md) を参照してください。

## <a name="prepare-your-environment-for-script-execution"></a>スクリプトの実行に関する環境の準備

1. 配置前スクリプトと配置後スクリプトの実行をコンフィギュレーションします。 詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../lifecycle-services/pre-post-scripts.md) を参照してください。
2. 次のコードを Predeployment.ps1 に追加します。

    ```powershell
    # This has to be filled out
    # $agentShare = '<Agent-share path>' # E.g '\\LBDContosoShare\agent''

    $agentShare = '\\servername\D365FFOAgent'
    Write-Output "AgentShare is set to $agentShare"

    # The scripts make the assumption that the wp folder only contains one folder for the environment name.
    # If you have multiple folders in there from older deployments, then please remove those.
    # It is not recommended to use the same agent share for multiple environments.

    #& $agentShare\scripts\TSG_UpdateFRDeployerConfig.ps1 -agentShare $agentShare

    #& $agentShare\scripts\TSG_WindowsAzureStorage.ps1 -agentShare $agentShare

    #& $agentShare\scripts\TSG_SysClassRunner.ps1 -agentShare $agentShare
    ```

3. このトピックの該当する部分から、問題を修正するために必要なコードをコピーし、新しいファイルに貼り付けます。 このファイルを、 Predeployment.ps1 スクリプトが格納されているフォルダと同じフォルダに保存します。 ファイル名は、コードをコピーしたセクションのタイトルと同じである必要があります。 修正する必要があるその他の問題について、この手順を繰り返します。
4. Predeployment.ps1 スクリプトで、前に追加したコードで、使用するスクリプトを呼び出す行のコメントを解除します。

## <a name="sysclassrunner"></a>TSG\_SysClassRunner.ps1

次のスクリプトは、プラットフォームの一部のバージョンで SysClassRunner が実行される場合に発生する問題を修正するために使用されます。 この問題の詳細については、 [SysClassRunner が正常に実行されません](troubleshoot-on-prem.md#SysClassRunner) を参照してください。

```powershell
param (
    [Parameter(Mandatory=$true)]
    [string]
    $agentShare = ''
)

$delete = @("Microsoft.Diagnostics.Tracing.TraceEvent.dll", "Microsoft.AI.Agent.Intercept.dll", "Microsoft.AI.DependencyCollector.dll", "Microsoft.AI.DependencyCollector.xml", "Microsoft.AI.PerfCounterCollector.dll", "Microsoft.AI.ServerTelemetryChannel.dll", "Microsoft.AI.ServerTelemetryChannel.xml", "Microsoft.AI.Web.dll", "Microsoft.AI.Web.xml", "Microsoft.AI.WindowsServer.dll","Microsoft.AI.WindowsServer.xml", "Microsoft.ApplicationInsights.dll", "Microsoft.ApplicationInsights.xml")

$ErrorActionPreference = "Stop"

$basePath = Get-ChildItem $agentShare\wp\*\StandaloneSetup-*\Apps |
    Select-Object -First 1 -Expand FullName

#Some customers experience an unexpected behavior with the previous command.
if($basePath -notmatch "\AOS")
{
    $basePath = Join-Path $basePath -ChildPath "\AOS" 
}

$basePath = Join-Path $basePath -ChildPath "AXServiceApp\AXSF\Code" 

if(!(Test-Path $basePath))
{
    Write-Error "Basepath: $basePath , not found" -Exception InvalidOperation
}

foreach( $file in $delete)
{
    if(Test-Path -Path "$basePath\$file")
    {
        Remove-Item -Path "$basePath\$file"
    }
}

$axConfig = Join-Path $basePath -ChildPath "AXService.exe.config"

if(!(Test-Path $axConfig))
{
    Write-Error "Unable to find AxService.exe.config in path: $axConfig" -Exception InvalidOperation
}

Write-Output "Found config: $axConfig"

[xml]$xml = get-content $axConfig
$xml.SelectNodes("//*[@name = 'Microsoft.AI.Agent.Intercept']/..") | ForEach-Object {
    $_.bindingRedirect.oldVersion = "0.0.0.0-2.4.0.0"
    $_.bindingRedirect.newVersion = "2.4.0.0"
}

if($xml.SelectNodes("//*[@name = 'Microsoft.ApplicationInsights']").Count -eq 0)
{
    [xml]$newNode = @"
    <dependentAssembly xmlns="urn:schemas-microsoft-com:asm.v1">
        <assemblyIdentity name="Microsoft.ApplicationInsights" publicKeyToken="31bf3856ad364e35" culture="neutral" />
        <bindingRedirect oldVersion="0.0.0.0-2.9.0.0" newVersion="2.9.0.0" />
    </dependentAssembly>
"@
    $xml.configuration.runtime.assemblyBinding.AppendChild($xml.ImportNode($newNode.dependentAssembly, $true))
    
}

$xml.save($axConfig)

Write-Output "TSG SysClassRunner script succeeded"
```

## <a name="frdeployer"></a>TSG\_UpdateFRDeployerConfig.ps1

次のスクリプトは、プラットフォームの一部のバージョンで財務諸表が配置される場合に発生する問題を修正するために使用されます。 この問題の詳細については、 [ファイルまたはアセンブリ EntityFramework を読み込めませんでした](troubleshoot-on-prem.md#FREntityFramework) を参照してください。

```powershell
param (
    [Parameter(Mandatory=$true)]
    [string]
    $agentShare = ''
)

$frConfig = Get-ChildItem $agentShare\wp\*\StandaloneSetup-*\Apps\FR\Deployment\FinancialReportingDeployer.exe.config |
    Select-Object -First 1 -Expand FullName

if( -not $frConfig)
{
    Write-Output "Unable to find FinancialReportingDeployer.exe.Config"
    return
}

Write-Output "Found config: $frConfig"

[xml]$xml = get-content $frConfig

$nodeList = $xml.GetElementsByTagName("loadFromRemoteSources")

if($nodeList.Count -eq 0)
{
    # Create the node 
    $newNode = $xml.CreateNode("element","loadFromRemoteSources","")
    $newNode.SetAttribute("enabled","true")
    # Find the parent
    $nodeList = $xml.GetElementsByTagName("runtime")
    $runtimeNode = $nodeList[0]
    $runtimeNode.AppendChild($newNode)
    # Save doc
    $xml.save($frConfig)
    Write-Output "Inserted new node: "$newNode.Name
}
else
{
    $node = $nodeList[0]

    $attribute = $node.Attributes.GetNamedItem("enabled")

    if($attribute.Value -eq "true")
    {
        Write-Output "Node already exists: "$node.Name
    }

    else
    {
        Write-Output "Node already exists but attribute is incorrect: " $attribute.Name "is" $attribute.Value
    }
}
```

## <a name="azurestorage"></a>TSG\_WindowsAzureStorage.ps1

次のスクリプトは、一部のバージョンのプラットフォームでファイルをダウンロードまたはエクスポートできない問題を解決するために使用されます。

```powershell
param (
    [Parameter(Mandatory=$true)]
    [string]
    $agentShare = ''
)
$ErrorActionPreference = "Stop"

$delete = @("Microsoft.WindowsAzure.Storage.dll", "Microsoft.WindowsAzure.Storage.xml")

$basePath = Get-ChildItem $agentShare\wp\*\StandaloneSetup-*\Apps |
    Select-Object -First 1 -Expand FullName

#Some customers experience an unexpected behavior with the previous command.
if($basePath -notmatch "\AOS")
{
    $basePath = Join-Path $basePath -ChildPath "\AOS" 
}

$basePath = Join-Path $basePath -ChildPath "AXServiceApp\AXSF\Code" 

if(!(Test-Path $basePath))
{
    Write-Error "Basepath: $basePath , not found" -Exception InvalidOperation
}

foreach( $file in $delete)
{
    if(Test-Path -Path "$basePath\$file")
    {
        Remove-Item -Path "$basePath\$file"
    }
}

Write-Output "TSG WindowsAzureStorage script succeeded"
```
