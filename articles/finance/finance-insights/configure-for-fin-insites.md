---
title: Finance Insights の構成 (プレビュー版)
description: このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908833"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="ed71a-103">Finance Insights の構成 (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="ed71a-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ed71a-104">Finance insights では、Microsoft Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、強力な予測ツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="ed71a-105">このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="ed71a-106">Dynamics 365 Finance のデプロイ</span><span class="sxs-lookup"><span data-stu-id="ed71a-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="ed71a-107">環境をデプロイするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed71a-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="ed71a-108">Microsoft Dynamics Lifecycle Services (LCS) で、Dynamics 365 Finance 環境を作成または更新します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="ed71a-109">この環境では、アプリ バージョン10.0.11/プラットフォーム更新プログラム 35またはそれ以降が必要となります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="ed71a-110">この環境は、サンドボックスの高可用性 (HA) 環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="ed71a-111">(このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="ed71a-112">Contoso のデモ データを使用している場合は、顧客支払予測、キャッシュ フロー予測、予算予測機能の使用にあたり、追加のサンプル データが必要になります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="ed71a-113">Dataverse のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ed71a-113">Configure Dataverse</span></span>

<span data-ttu-id="ed71a-114">以下の手動構成ステップを完了するか、提供されている Windows PowerShell スクリプトを使用すると設定のプロセスを高速化することができます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="ed71a-115">PowerShell スクリプトの実行が完了すると、Finance insights の構成に使用する値が提供されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="ed71a-116">スクリプトを実行するには、PCで PowerShell を開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="ed71a-117">PowerShell バージョン5 が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="ed71a-118">Microsoft Azure CLI の "Try it" オプションが機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="ed71a-119">手動構成の手順</span><span class="sxs-lookup"><span data-stu-id="ed71a-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="ed71a-120">[Power Platform 管理センター ](https://admin.powerplatform.microsoft.com/)を開き、次の手順に従って、同じ Active Directory テナントに新しい Dataverse 環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="ed71a-121">**環境** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="ed71a-122">[![ 環境ページ](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="ed71a-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="ed71a-123">**新しい環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="ed71a-124">**タイプ** フィールドで、**サンドボックス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="ed71a-125">**データベースの作成** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="ed71a-126">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-126">Select **Next**.</span></span>
    6. <span data-ttu-id="ed71a-127">組織で使用する言語と通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="ed71a-128">その他のすべてのフィールドで使用する規定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="ed71a-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-129">Select **Save**.</span></span>
    9. <span data-ttu-id="ed71a-130">**環境** ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="ed71a-131">**状態** フィールドの値が **準備完了** に更新されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="ed71a-132">Dataverse コンテナ― ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="ed71a-133">環境を選択し、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="ed71a-134">**リソース \> すべてのレガシー設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="ed71a-135">トップ ナビゲーションバーで、**設定** を選択し、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="ed71a-136">**開発者リソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="ed71a-137">**Dataverse 組織 ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-137">Copy the **Dataverse organization ID** value.</span></span>
    17. <span data-ttu-id="ed71a-138">ブラウザーのアドレスバーで、Dataverse 組織の URL をメモします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="ed71a-139">URL は次のようなものになるでしょう: [`https://org42b2b3d3.crm.dynamics.com`]。</span><span class="sxs-lookup"><span data-stu-id="ed71a-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="ed71a-140">キャッシュフロー予測機能や予算予測機能を使用する場合は、次の手順に従って、注釈の制限を少なくとも 50 メガバイト (MB) に更新してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="ed71a-141">[Power Apps ポータル](https://make.powerapps.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="ed71a-142">作成した環境を選択し、 **詳細設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="ed71a-143">**設定 \> 電子メールの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="ed71a-144">**最大ファイルサイズ** フィールドの値を **51,200** に変更します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="ed71a-145">(値は、キロバイト \[KB\] で表されます。)</span><span class="sxs-lookup"><span data-stu-id="ed71a-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="ed71a-146">**OK** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="ed71a-147">Windows PowerShell 構成スクリプト</span><span class="sxs-lookup"><span data-stu-id="ed71a-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="ed71a-148">Azure の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="ed71a-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="ed71a-149">Dataverse ディレクトリ ID とユーザーの Azure AD オブジェクト ID を入力します</span><span class="sxs-lookup"><span data-stu-id="ed71a-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="ed71a-150">Dataverse ディレクトリ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="ed71a-151">[Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="ed71a-152">Dataverse 環境の作成に使用したユーザー ID を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="ed71a-153">**Azure Active Directory** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="ed71a-154">**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="ed71a-155">ユーザーの Azure Active Directory (Azure AD) オブジェクト ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="ed71a-156">[Azure portal](https://portal.azure.com)で、**ユーザー** に移動して電子メールアドレスでユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="ed71a-157">ユーザーの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-157">Select the user's name.</span></span>
    3. <span data-ttu-id="ed71a-158">**オブジェクト ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="ed71a-159">Azure Cloud Shell を使用した Finance insights Data Lake リソースの設定</span><span class="sxs-lookup"><span data-stu-id="ed71a-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="ed71a-160">Windows PowerShell スクリプトを使用する</span><span class="sxs-lookup"><span data-stu-id="ed71a-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="ed71a-161">Windows PowerShell スクリプトが指定されているため、[Azure Data Lakeへのエクスポートの構成](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)で説明されているように Azure リソースを簡単に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="ed71a-162">手動による設定を行う場合は、この手順を省略して、[手動設定](#manual-setup)の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="ed71a-163">PowerShell スクリプトを実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="ed71a-164">Azure CLI の "Try it" オプション、または PC 上でのスクリプト実行ができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="ed71a-165">Windows PowerShell スクリプトを使用して Azure をコ構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed71a-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="ed71a-166">Azure リソース グループ、Azure リソース、 Azure AD アプリケーションを作成する権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="ed71a-167">必要なアクセス許可については、[Azure AD のアクセス許可の確認](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-167">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="ed71a-168">[Azure portal](https://portal.azure.com)で、対象の Azure サブスクリプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="ed71a-169">**検索** フィールドの右側にある **Cloud Shell** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="ed71a-170">**PowerShell** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="ed71a-171">プロンプトが表示された場合は、ストレージを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="ed71a-172">その後、Windows PowerShell スクリプトをセッションにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="ed71a-173">スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-173">Run the script.</span></span>
5. <span data-ttu-id="ed71a-174">プロンプトに従ってスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="ed71a-175">スクリプト出力の情報を使用して、LCS に **Data Lake にエクスポートする** アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="ed71a-176">スクリプト出力の情報を使用して、Finance (**システム管理 \> システムパラメーター \> データ接続**) の **データ接続** ページのエンティティストアを有効にします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="ed71a-177">手動設定</span><span class="sxs-lookup"><span data-stu-id="ed71a-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="ed71a-178">Azure AD テナントへのアプリケーションの追加</span><span class="sxs-lookup"><span data-stu-id="ed71a-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="ed71a-179">[Azure ポータル](https://portal.azure.com)で **Azure Active Directory** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="ed71a-180">**管理 \> エンタープライズ アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="ed71a-181">次のアプリケーションをアプリ ID で検索します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="ed71a-182">申請書</span><span class="sxs-lookup"><span data-stu-id="ed71a-182">Application</span></span>                              | <span data-ttu-id="ed71a-183">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="ed71a-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="ed71a-184">Microsoft Dynamics ERP マイクロサービス</span><span class="sxs-lookup"><span data-stu-id="ed71a-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="ed71a-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="ed71a-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="ed71a-186">Microsoft Dynamics ERP マイクロサービス CDS</span><span class="sxs-lookup"><span data-stu-id="ed71a-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="ed71a-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="ed71a-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="ed71a-188">AI Builder の承認サービス</span><span class="sxs-lookup"><span data-stu-id="ed71a-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="ed71a-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="ed71a-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="ed71a-190">前述のアプリケーションが見つからない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="ed71a-191">ローカル コンピューターで、**スタート**  メニューを選択し、**powershell** を検索します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="ed71a-192">**Windows PowerShell** を右クリックし、**管理者として実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="ed71a-193">以下のコマンドを実行して **AzureAD** モジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="ed71a-194">NuGet プロバイダーを続行する必要がある場合は、**Y** を選択してインストールします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="ed71a-195">「信頼できないリポジトリ」のメッセージが表示された場合は、**Y** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="ed71a-196">追加の必要がある各アプリケーションについては、以下のコマンドを実行してアプリケーションを Azure AD に追加します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="ed71a-197">プロンプトが表示されたら、管理者で Azure AD にログインします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="ed71a-198">Azure リソースの作成</span><span class="sxs-lookup"><span data-stu-id="ed71a-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="ed71a-199">Dataverse 環境と同じ Azure AD インスタンスで次のリソースを作成してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="ed71a-200">別の Azure AD インスタンスのリソースを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ed71a-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="ed71a-201">新しいストレージ アカウントを作成する方法:</span><span class="sxs-lookup"><span data-stu-id="ed71a-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="ed71a-202">[Azure ポータル](https://portal.azure.com)で、新しいストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="ed71a-203">**ストレージ アカウントの作成** ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="ed71a-204">**場所** - ご利用の環境が設置されているデータセンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="ed71a-205">**パフォーマンス** - **標準** を選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="ed71a-206">**アカウントの種類** - 必ず **Storage V2** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="ed71a-207">**詳細オプション** ダイアログボックスの **Data Lake storage Gen2** オプションで、**階層型名前空間** 機能配下の **有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="ed71a-208">この機能を無効にすると、Power BI データ フローなどのサービスを含む Finance and Operations アプリが書き込んだデータを使用することができません。</span><span class="sxs-lookup"><span data-stu-id="ed71a-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="ed71a-209">**確認して作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-209">Select **Review and create**.</span></span> <span data-ttu-id="ed71a-210">配置が完了したら、新しいリソースが Azure ポータルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="ed71a-211">作成したストレージ アカウントに移動します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="ed71a-212">左側のメニューで、**アクセス キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="ed71a-213">**Key1** または **Key2** の接続文字列をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="ed71a-214">ストレージアカウント名をコピーして保存し ます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="ed71a-215">新しいキー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="ed71a-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="ed71a-216">[Azure portal](https://portal.azure.com)で、新しいキー コンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="ed71a-217">**Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="ed71a-218">キー コンテナーが作成されたら、一覧で選択し、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="ed71a-219">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="ed71a-220">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="ed71a-221">シークレットの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-221">Enter a name for the secret.</span></span> <span data-ttu-id="ed71a-222">その後で指定する必要があるため、名前をメモします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="ed71a-223">**値** フィールドに、前述の手順でストレージ アカウントから取得した接続文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="ed71a-224">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="ed71a-225">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="ed71a-226">**キー コンテナーの概要** を開き、DNS 名を控えておきます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="ed71a-227">Azure AD アプリケーションを作成、登録します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="ed71a-228">[Azure portal](https://portal.azure.com) で、**Azure Active Directory** にアクセスし、**App registrations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="ed71a-229">**新規アプリケーションの登録** を選択し、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="ed71a-230">**名前** - アプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="ed71a-231">**アプリケーション タイプ** - **Web API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="ed71a-232">**リダイレクト URI の設定** - Dynamics 365 インスタンスの URL を入力します (例: `https://yourdynamicsinstance.dynamics.com/auth` )。</span><span class="sxs-lookup"><span data-stu-id="ed71a-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="ed71a-233">作成したアプリに移動し、**アプリケーション (クライアント) ID** の値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="ed71a-234">後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="ed71a-235">**API アクセス許可** に移動し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed71a-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="ed71a-236">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="ed71a-237">**Azure Key vault** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="ed71a-238">[委任されたアクセス許可] を選択した後、**ユーザー\_なりすまし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="ed71a-239">**アクセス許可の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="ed71a-240">アプリのメニューで、**証明書\&シークレット** を選択し、次の手順に従ってキー コンテナーのシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="ed71a-241">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="ed71a-242">**キーの説明** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="ed71a-243">期間を選択し、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="ed71a-244">シークレットが **値** フィールドに生成されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="ed71a-245">シークレットの値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="ed71a-246">新しいキー コンテナーの作成:</span><span class="sxs-lookup"><span data-stu-id="ed71a-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="ed71a-247">前述の手順で作成したキー コンテナーに移動し、**シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="ed71a-248">次の表の各シークレットに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ed71a-249">**生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="ed71a-250">**シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="ed71a-251">次の表から、シークレットの名前と値を作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="ed71a-252">**有効** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="ed71a-253">シークレットが作成され、Key Vault に追加されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="ed71a-254">シークレット名</span><span class="sxs-lookup"><span data-stu-id="ed71a-254">Secret name</span></span>                       | <span data-ttu-id="ed71a-255">シークレットの値</span><span class="sxs-lookup"><span data-stu-id="ed71a-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="ed71a-256">アプリ ID</span><span class="sxs-lookup"><span data-stu-id="ed71a-256">app-id</span></span>                            | <span data-ttu-id="ed71a-257">作成済みのアプリケーション アプリ ID</span><span class="sxs-lookup"><span data-stu-id="ed71a-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="ed71a-258">アプリのシークレット</span><span class="sxs-lookup"><span data-stu-id="ed71a-258">app-secret</span></span>                        | <span data-ttu-id="ed71a-259">前述の手順で保存したクライアント シークレット</span><span class="sxs-lookup"><span data-stu-id="ed71a-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="ed71a-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="ed71a-260">storage-account-name</span></span>              | <span data-ttu-id="ed71a-261">前に作成したストレージアカウントの名前 (例: **sstorageaccount1**)</span><span class="sxs-lookup"><span data-stu-id="ed71a-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="ed71a-262">ストレージ - アカウント - 接続 - 文字列</span><span class="sxs-lookup"><span data-stu-id="ed71a-262">storage-account-connection-string</span></span> | <span data-ttu-id="ed71a-263">ストレージ アカウントの **アクセス キー** ページからコピーした接続文字列</span><span class="sxs-lookup"><span data-stu-id="ed71a-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="ed71a-264">アプリケーションを承認してキー コンテナーにアクセスする方法:</span><span class="sxs-lookup"><span data-stu-id="ed71a-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="ed71a-265">[Azure portal](https://portal.azure.com)で、作成済のキー コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="ed71a-266">アクセス ポリシーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-266">Select the access policies.</span></span>
    3. <span data-ttu-id="ed71a-267">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ed71a-268">**アクセス ポリシー** を選択し、アクセス ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="ed71a-269">**シークレットのアクセス許可** フィールドで、次の表からアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="ed71a-270">**プリンシパルの選択** フィールドで、次の表からアプリケーションの表示名を検索します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="ed71a-271">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-271">Select **Select**.</span></span>
        5. <span data-ttu-id="ed71a-272">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-272">Select **Add**.</span></span>
        6. <span data-ttu-id="ed71a-273">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-273">Select **Save**.</span></span>

        | <span data-ttu-id="ed71a-274">申請書</span><span class="sxs-lookup"><span data-stu-id="ed71a-274">Application</span></span>                                              | <span data-ttu-id="ed71a-275">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="ed71a-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="ed71a-276">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="ed71a-276">The display name of the new application that you created</span></span> | <span data-ttu-id="ed71a-277">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="ed71a-277">Get, List</span></span>   |
        | <span data-ttu-id="ed71a-278">**Microsoft Dynamics ERP マイクロサービス**</span><span class="sxs-lookup"><span data-stu-id="ed71a-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="ed71a-279">取得、リスト表示</span><span class="sxs-lookup"><span data-stu-id="ed71a-279">Get, List</span></span>   |

6. <span data-ttu-id="ed71a-280">ストレージ アカウントにアクセスするロールを割り当てるには、次の操作を行います:</span><span class="sxs-lookup"><span data-stu-id="ed71a-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="ed71a-281">[Azure ポータル](https://portal.azure.com)で、作成済のストレージ アカウントを開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="ed71a-282">**アクセスの制御 (IAM)** を選択し 、**ロールの割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="ed71a-283">**追加、 ロールの割り当ての追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="ed71a-284">次のアプリケーションに対して、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ed71a-285">以下の表からロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="ed71a-286">**アクセス権の割り当て先** シールドは、**Azure AD ユーザー、グループ、またはサービス プリンシパル** のままにします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="ed71a-287">**選択** フィールドで、次の表からアプリケーションを入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="ed71a-288">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-288">Select **Save**.</span></span>

        | <span data-ttu-id="ed71a-289">申請書</span><span class="sxs-lookup"><span data-stu-id="ed71a-289">Application</span></span>                                              | <span data-ttu-id="ed71a-290">役割</span><span class="sxs-lookup"><span data-stu-id="ed71a-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="ed71a-291">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="ed71a-291">The display name of the new application that you created</span></span> | <span data-ttu-id="ed71a-292">所有者</span><span class="sxs-lookup"><span data-stu-id="ed71a-292">Owner</span></span>                       |
        | <span data-ttu-id="ed71a-293">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="ed71a-293">The display name of the new application that you created</span></span> | <span data-ttu-id="ed71a-294">寄稿者</span><span class="sxs-lookup"><span data-stu-id="ed71a-294">Contributor</span></span>                 |
        | <span data-ttu-id="ed71a-295">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="ed71a-295">The display name of the new application that you created</span></span> | <span data-ttu-id="ed71a-296">ストレージ アカウントの共同作成者</span><span class="sxs-lookup"><span data-stu-id="ed71a-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="ed71a-297">作成した新しいアプリケーションの表示名称</span><span class="sxs-lookup"><span data-stu-id="ed71a-297">The display name of the new application that you created</span></span> | <span data-ttu-id="ed71a-298">ストレージ BLOB データの所有者</span><span class="sxs-lookup"><span data-stu-id="ed71a-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="ed71a-299">**AI Builder の承認サービス**</span><span class="sxs-lookup"><span data-stu-id="ed71a-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="ed71a-300">ストレージ BLOB データの読み取り</span><span class="sxs-lookup"><span data-stu-id="ed71a-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="ed71a-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="ed71a-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="ed71a-302">Data Lake を構成する</span><span class="sxs-lookup"><span data-stu-id="ed71a-302">Configure the data lake</span></span>

<span data-ttu-id="ed71a-303">LCS を使用して Azure Data Lake アドインを環境に追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed71a-303">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="ed71a-304">LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-304">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="ed71a-305">**環境アドイン** セクションで、**新しいアドインのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-305">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="ed71a-306">**Data Lake へのエクスポート** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-306">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="ed71a-307">次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-307">Enter the following values.</span></span>

    | <span data-ttu-id="ed71a-308">先頭値</span><span class="sxs-lookup"><span data-stu-id="ed71a-308">Value</span></span>                                                              | <span data-ttu-id="ed71a-309">説明</span><span class="sxs-lookup"><span data-stu-id="ed71a-309">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="ed71a-310">キーの保管場所がある Azure サブスクリプションのテナント ID</span><span class="sxs-lookup"><span data-stu-id="ed71a-310">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="ed71a-311">ストレージ アカウント、アプリ、キーコンテナーが配置されているテナント ID です。</span><span class="sxs-lookup"><span data-stu-id="ed71a-311">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="ed71a-312">この値を検索するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-312">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="ed71a-313">Key Vault の DNS 名を指定する</span><span class="sxs-lookup"><span data-stu-id="ed71a-313">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="ed71a-314">キー コンテナーの DNS 名 (例:  `https://customkeyvault.vault.azure.net/`)。</span><span class="sxs-lookup"><span data-stu-id="ed71a-314">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="ed71a-315">(この値は、エンティティ ストアで使用されている DNS 名と同一のものです。)</span><span class="sxs-lookup"><span data-stu-id="ed71a-315">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="ed71a-316">ストレージ アカウントの名前を含むシークレットを指定します</span><span class="sxs-lookup"><span data-stu-id="ed71a-316">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="ed71a-317">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="ed71a-317">**storage-account-name**</span></span> |
    | <span data-ttu-id="ed71a-318">Data Lake へのアクセスに使用するアプリ ID のシークレット名</span><span class="sxs-lookup"><span data-stu-id="ed71a-318">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="ed71a-319">**アプリの ID**</span><span class="sxs-lookup"><span data-stu-id="ed71a-319">**app-id**</span></span> |
    | <span data-ttu-id="ed71a-320">アプリの ID に使用するシークレット名</span><span class="sxs-lookup"><span data-stu-id="ed71a-320">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="ed71a-321">**アプリのシークレット**</span><span class="sxs-lookup"><span data-stu-id="ed71a-321">**app-secret**</span></span> |

5. <span data-ttu-id="ed71a-322">条件に同意し、**インストール** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-322">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="ed71a-323">このアドインは数分以内にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-323">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="ed71a-324">AI Builder の構成</span><span class="sxs-lookup"><span data-stu-id="ed71a-324">Configure AI Builder</span></span>

1. <span data-ttu-id="ed71a-325">LCS にサインインし、**環境の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-325">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="ed71a-326">**環境アドイン** セクションまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-326">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="ed71a-327">この環境に既にインストールされているアドインが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-327">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="ed71a-328">**Data Lake にエクスポートする** アドインがない場合は、このアドインを構成します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-328">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="ed71a-329">**分析情報の取得** アドインを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-329">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="ed71a-330">**分析情報の取得** アドインの詳細ページで、次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-330">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="ed71a-331">先頭値</span><span class="sxs-lookup"><span data-stu-id="ed71a-331">Value</span></span>                                                    | <span data-ttu-id="ed71a-332">説明</span><span class="sxs-lookup"><span data-stu-id="ed71a-332">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="ed71a-333">CDS 組織の URL</span><span class="sxs-lookup"><span data-stu-id="ed71a-333">CDS Organization URL</span></span>                                     | <span data-ttu-id="ed71a-334">Dataverse インスタンスの Dataverse 組織の URL です。</span><span class="sxs-lookup"><span data-stu-id="ed71a-334">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="ed71a-335">この値を見つけるするには、[Power Apps ポータル](https://make.powerapps.com)を開き、右上隅にある **設定** ボタン (歯車記号) を選択し、**詳細設定** を選択して、URLをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-335">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="ed71a-336">URL の末尾には "dynamics.com" が付きます</span><span class="sxs-lookup"><span data-stu-id="ed71a-336">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="ed71a-337">CDS Org ID</span><span class="sxs-lookup"><span data-stu-id="ed71a-337">CDS Org ID</span></span>                                               | <span data-ttu-id="ed71a-338">Dataverse インスタンスの環境 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-338">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="ed71a-339">この値を見つけるするには、[Power Apps ポータル](https://make.powerapps.com)を開き、右上隅にある **設定** ボタン (歯車記号) を選択し、**カスタマイズ \> 開発者リソース \> インスタンスの参照情報** を選択し、**ID** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-339">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="ed71a-340">CDS テナント ID (AAD のディレクトリ ID)</span><span class="sxs-lookup"><span data-stu-id="ed71a-340">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="ed71a-341">Dataverse インスタンスのテナント ID です。</span><span class="sxs-lookup"><span data-stu-id="ed71a-341">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="ed71a-342">この値を検索するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-342">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="ed71a-343">システム管理者ロールを持つユーザー オブジェクトの ID を指定します</span><span class="sxs-lookup"><span data-stu-id="ed71a-343">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="ed71a-344">Azure AD のユーザーの Dataverse ユーザーのオブジェクト ID です。</span><span class="sxs-lookup"><span data-stu-id="ed71a-344">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="ed71a-345">このユーザーは、Dataverse インスタンスのシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed71a-345">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="ed71a-346">この値を検索するには、[Azure portal](https://portal.azure.com)を開き、**Azure Active Directory\>** ユーザーに移動し、ユーザーを選択して、**ID** セクションで **オブジェクト ID** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-346">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="ed71a-347">これはテナントの既定の CD 環境ですか？</span><span class="sxs-lookup"><span data-stu-id="ed71a-347">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="ed71a-348">Dataverse インスタンスが最初に作成された運用インスタンスの場合は、このチェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-348">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="ed71a-349">Dataverse インスタンスが手動で作成された場合は、このチェックボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="ed71a-349">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="configure-the-entity-store"></a><span data-ttu-id="ed71a-350">エンティティの保存を構成する</span><span class="sxs-lookup"><span data-stu-id="ed71a-350">Configure the entity store</span></span>

<span data-ttu-id="ed71a-351">Finance 環境でエンティティの保存を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed71a-351">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="ed71a-352">**システム管理 \> 設定 \> システム パラメーター \> データ接続** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-352">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="ed71a-353">**Data Lake 統合の有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-353">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="ed71a-354">次のキー コンテナー フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-354">Set the following key vault fields:</span></span>

    - <span data-ttu-id="ed71a-355">**アプリケーション (クライアント) ID**: 以前に作成したアプリケーションクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-355">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="ed71a-356">**アプリケーションのシークレット** - 以前に作成したアプリケーションで使用する保存済みのシークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-356">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="ed71a-357">**DNS 名** - ドメイン ネーム システム (DNS) 名は、前述の手順で作成したアプリケーションの [アプリケーションの詳細] ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-357">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="ed71a-358">**シークレット名** - **ストレージ アカウントの接続文字列** を入力します。</span><span class="sxs-lookup"><span data-stu-id="ed71a-358">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="ed71a-359">フィードバックとサポート</span><span class="sxs-lookup"><span data-stu-id="ed71a-359">Feedback and support</span></span>

<span data-ttu-id="ed71a-360">フィードバックの提供またはサポートが必要な場合は、[顧客支払い分析情報 (プレビュー)](mailto:fiap@microsoft.com) に電子メールを送信してください。</span><span class="sxs-lookup"><span data-stu-id="ed71a-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ed71a-361">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="ed71a-361">Privacy notice</span></span>

<span data-ttu-id="ed71a-362">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="ed71a-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
