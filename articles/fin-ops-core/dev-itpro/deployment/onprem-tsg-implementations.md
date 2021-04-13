---
title: オンプレミス環境の問題を解決するためのスクリプト
description: このトピックは、オンプレミス環境の問題を修正するために使用できるスクリプトの中央レポジトリとして機能します。
author: faix
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-11-30]
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: f125e974893c8eed8221c513308b57ae377482ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745321"
---
# <a name="scripts-for-resolving-issues-in-on-premises-environments"></a><span data-ttu-id="f23c4-103">オンプレミス環境の問題を解決するためのスクリプト</span><span class="sxs-lookup"><span data-stu-id="f23c4-103">Scripts for resolving issues in on-premises environments</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f23c4-104">このトピックは、オンプレミス環境の問題を修正するために使用できるスクリプトの中央レポジトリとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f23c4-104">This topic will serve as a central repository for scripts that you can use to fix issues in on-premises environments.</span></span> <span data-ttu-id="f23c4-105">通常、これらのスクリプトは配置前スクリプトまたは配置後スクリプトとして実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f23c4-105">These scripts must usually be run as pre-deployment or post-deployment scripts.</span></span>

<span data-ttu-id="f23c4-106">オンプレミス環境における問題の解決方法の詳細については、 [オンプレミス配置のトラブルシューティング](troubleshoot-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23c4-106">For more information about how to resolve issues in on-premises environments, see [Troubleshoot on-premises deployments](troubleshoot-on-prem.md).</span></span>

## <a name="prepare-your-environment-for-script-execution"></a><span data-ttu-id="f23c4-107">スクリプトの実行に関する環境の準備</span><span class="sxs-lookup"><span data-stu-id="f23c4-107">Prepare your environment for script execution</span></span>

1. <span data-ttu-id="f23c4-108">配置前スクリプトと配置後スクリプトの実行をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f23c4-108">Configure the execution of pre-deployment and post-deployment scripts.</span></span> <span data-ttu-id="f23c4-109">詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../lifecycle-services/pre-post-scripts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23c4-109">For more information, see [Local agent pre-deployment and post-deployment scripts](../lifecycle-services/pre-post-scripts.md).</span></span>
2. <span data-ttu-id="f23c4-110">次のコードを Predeployment.ps1 に追加します。</span><span class="sxs-lookup"><span data-stu-id="f23c4-110">Add the following code to your Predeployment.ps1 script.</span></span>

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
    
    #& $agentShare\scripts\TSG_RemoveFilesFromZip.ps1 -agentShare $agentShare -filesToRemove 'Packages\TaxEngine\bin\Microsoft.Dynamics365.ElectronicReportingMapping.dll','Packages\TaxEngine\bin\Microsoft.Dynamics365.ElectronicReportingMapping.pdb','Packages\TaxEngine\bin\Microsoft.Dynamics365.ElectronicReportingServiceContracts.dll','Packages\TaxEngine\bin\Microsoft.Dynamics365.ElectronicReportingServiceContracts.pdb','Packages\TaxEngine\bin\Microsoft.Dynamics.ElectronicReporting.Instrumentation.dll','Packages\TaxEngine\bin\Microsoft.Dynamics.ElectronicReporting.Instrumentation.pdb','Packages\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.dll','Packages\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.pdb','Packages\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFrameworkForAx.dll','Packages\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFrameworkForAx.pdb'
    ```

3. <span data-ttu-id="f23c4-111">このトピックの該当する部分から、問題を修正するために必要なコードをコピーし、新しいファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-111">From the relevant section of this topic, copy the code that you require to fix your issue, and paste it into a new file.</span></span> <span data-ttu-id="f23c4-112">このファイルを、 Predeployment.ps1 スクリプトが格納されているフォルダと同じフォルダに保存します。</span><span class="sxs-lookup"><span data-stu-id="f23c4-112">Save this file in the same folder where your Predeployment.ps1 script is stored.</span></span> <span data-ttu-id="f23c4-113">ファイル名は、コードをコピーしたセクションのタイトルと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f23c4-113">The file name must match the title of the section that you copied the code from.</span></span> <span data-ttu-id="f23c4-114">修正する必要があるその他の問題について、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f23c4-114">Repeat this step for other issues that you must fix.</span></span>
4. <span data-ttu-id="f23c4-115">Predeployment.ps1 スクリプトで、前に追加したコードで、使用するスクリプトを呼び出す行のコメントを解除します。</span><span class="sxs-lookup"><span data-stu-id="f23c4-115">In the Predeployment.ps1 script, in the code that you added earlier, uncomment the lines that invoke the scripts that you want to use.</span></span>

## <a name="tsg_sysclassrunnerps1"></a><a name="sysclassrunner"></a><span data-ttu-id="f23c4-116">TSG\_SysClassRunner.ps1</span><span class="sxs-lookup"><span data-stu-id="f23c4-116">TSG\_SysClassRunner.ps1</span></span>

<span data-ttu-id="f23c4-117">次のスクリプトは、プラットフォームの一部のバージョンで SysClassRunner が実行される場合に発生する問題を修正するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-117">The following script is used to fix an issue that occurs when SysClassRunner is run in some versions of the platform.</span></span> <span data-ttu-id="f23c4-118">この問題の詳細については、 [SysClassRunner が正常に実行されません](troubleshoot-on-prem.md#SysClassRunner) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23c4-118">For more information about this issue, see [SysClassRunner doesn't run successfully](troubleshoot-on-prem.md#SysClassRunner).</span></span>

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

## <a name="tsg_updatefrdeployerconfigps1"></a><a name="frdeployer"></a><span data-ttu-id="f23c4-119">TSG\_UpdateFRDeployerConfig.ps1</span><span class="sxs-lookup"><span data-stu-id="f23c4-119">TSG\_UpdateFRDeployerConfig.ps1</span></span>

<span data-ttu-id="f23c4-120">次のスクリプトは、プラットフォームの一部のバージョンで財務諸表が配置される場合に発生する問題を修正するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-120">The following script is used to fix an issue that occurs when Financial Reporting is deployed in some versions of the platform.</span></span> <span data-ttu-id="f23c4-121">この問題の詳細については、 [ファイルまたはアセンブリ EntityFramework を読み込めませんでした](troubleshoot-on-prem.md#FREntityFramework) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f23c4-121">For more information about this issue, see [Could not load file or assembly EntityFramework](troubleshoot-on-prem.md#FREntityFramework).</span></span>

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

## <a name="tsg_windowsazurestorageps1"></a><a name="azurestorage"></a><span data-ttu-id="f23c4-122">TSG\_WindowsAzureStorage.ps1</span><span class="sxs-lookup"><span data-stu-id="f23c4-122">TSG\_WindowsAzureStorage.ps1</span></span>

<span data-ttu-id="f23c4-123">次のスクリプトは、一部のバージョンのプラットフォームでファイルをダウンロードまたはエクスポートできない問題を解決するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-123">The following script is used to fix an issue where files can't be downloaded or exported in some versions of the platform.</span></span>

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


## <a name="tsg_removefilesfromzipps1"></a><a name="taxengine"></a><span data-ttu-id="f23c4-124">TSG\_RemoveFilesFromZip.ps1</span><span class="sxs-lookup"><span data-stu-id="f23c4-124">TSG\_RemoveFilesFromZip.ps1</span></span>

<span data-ttu-id="f23c4-125">次のスクリプトは、以前バージョン 10.0.5 から 10.0.9 を使用していた一部の顧客に発生する問題を修正するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-125">The following script is used to fix an issue that occurs for some customers who were previously on versions 10.0.5 through 10.0.9.</span></span> <span data-ttu-id="f23c4-126">準備プロセスの仕組みにより、TaxEngine フォルダーにはいくつかの古いバージョンの DLL が 残っていますが、新しいリリースでは、別のモジュールフォルダに移動されています。</span><span class="sxs-lookup"><span data-stu-id="f23c4-126">Due to how the prepare process works, there are some older versions of DLLs that remain in the TaxEngine folder, which in newer releases have been moved to different module folders.</span></span> <span data-ttu-id="f23c4-127">このスクリプトを使用すると、DLL が AOS ノードに配置される前に、ダウンロードした資産から削除されます。</span><span class="sxs-lookup"><span data-stu-id="f23c4-127">This script ensures that these DLLs are removed from the downloaded asset, before being deployed to the AOS nodes.</span></span>

```powershell
[CmdletBinding()]
param
(
    [Parameter(Mandatory)]
    [ValidateNotNullOrEmpty()]
    [ValidateScript({ Test-Path -Path $_ })]
    [string] $agentShare,

    [ValidateNotNullOrEmpty()]
    [string[]]$filesToRemove
)

#requires -Version 5
$ErrorActionPreference = 'Stop'
$InformationPreference = 'Continue'
$files = @()

[Reflection.Assembly]::LoadWithPartialName('System.IO.Compression')

if(! (Test-Path $AgentShare))
{
    throw "The path provided for the agentshare is not valid/accessible."
}

ForEach($file in $FilesToRemove)
{
    if(!$file.StartsWith('Packages'))
    {
        throw "The path of $file does not start with Packages."
    }
    $files += $file.Replace('\', '/')
} 

$basePath = Get-ChildItem $AgentShare\wp\*\StandaloneSetup-*\Apps | Select-Object -First 1 -Expand FullName

#Some customers experience an unexpected behavior with the previous command.
if($basePath -notmatch "\AOS")
{
    $basePath = Join-Path $basePath -ChildPath "\AOS" 
}

$basePath = Join-Path $basePath -ChildPath "AXServiceApp\AXSF\Code"
$zipfile = Join-Path $basePath -ChildPath "Packages.zip"

try
{
    $stream = New-Object IO.FileStream($zipfile, [IO.FileMode]::Open)
    $mode   = [IO.Compression.ZipArchiveMode]::Update
    $zip    = New-Object IO.Compression.ZipArchive($stream, $mode)

    ($zip.Entries | ? { $files -contains $_.FullName }) | % { $_.Delete() } | Write-Host
}
catch
{
    throw 'An Error Occurred'
}
finally
{
    $zip.Dispose()
    $stream.Close()
    $stream.Dispose() 
}

```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]