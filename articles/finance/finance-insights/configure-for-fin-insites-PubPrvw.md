---
title: Finance Insights の構成 - バージョン 10.0.20 以降
description: この記事では、バージョン 10.0.20 以降の Finance Insights で利用可能な機能を使用するために、システムを設定する方法について説明します。
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e6b9c34ee68a25ac9613a65cf63443751a39c576
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868521"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Finance Insights の構成 - バージョン 10.0.20 以降

[!include [banner](../includes/banner.md)]



Finance Insights では、Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、組織に強力な予測ツールを提供します。 この記事では、Dynamics 365 Finance のバージョン 10.0.20 を設定して、システムが Finance Insights で利用可能な機能を使用できるようにする方法について説明します。

> [!NOTE]
> この記事で説明する構成手順は、Finance のバージョン 10.0.20 以降にのみ適用されます。 バージョン 10.0.19 およびそれ以前で Finance Insights を設定するには、[Finance Insights の構成 - バージョン 10.0.19 まで](configure-for-fin-insites.md)を参照してください。

## <a name="deploy-finance"></a>Finance のデプロイ

環境をデプロイするには、これらの手順に従います。

1. Microsoft Dynamics Lifecycle Services (LCS) で、 Finance 環境を作成、または更新します。 この環境では、財務と運用アプリのバージョン 10.0.20 以降が必要です。
2. この環境は、サンドボックスの高可用性 (HA) 環境である必要があります。 (このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。
3. サンドボックス環境で Finance insights を構成している場合は、予測を機能させるには、運用データをその環境にコピーする必要がある場合があります。 予測モデルでは、複数年分のデータを用いて予測値を構築します。 Contoso のデモ データには、予測モデルを適切にトレーニングさせるだけの過去のデータが十分に含まれていません。 

## <a name="configure-dataverse"></a>Dataverse のコンフィギュレーション

以下の手順で、Finance insights に Dataverse を構成します。

1. LCS で、環境のページを開き、**Power Platform 統合** のセクションがすでに設定されていることを確認します。

    - 既に設定されている場合、 Finance 環境にリンクされている Dataverse の環境名が表示されます。
    - まだ設定されていない場合は、次の手順に従います。

        1. **Power Platform の統合** セクションで、**設定** を選択します。 環境の設定には最大で 1 時間ほどかかる場合があります。
        2. Dataverse 環境が正常に設定されている場合、Finance 環境にリンクされている Dataverse の環境名が表示されます。

        > [!NOTE]
        > 環境の設定が完了した後は、**CDS for Apps へのリンク** を選択 **しないでください**。 このボタンは、Finance Insights には必要ありません。 このオプションを選択すると、LCS で必要となる環境アドインを構成することができます。

## <a name="configure-azure"></a>Azure の構成

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Azure Cloud Shell を使用した Finance insights Data Lake リソースの設定

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell スクリプトを使用する](#tab/use-a-powershell-script)

Windows PowerShell スクリプトが用意されているので、[Azure Data Lake へのエクスポートの構成](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) で説明されているように Azure のリソースを簡単に設定することができます。 手動による設定を行う場合は、この手順を省略して、[手動設定](#manual-setup) に記載の手順を完了してください。

> [!NOTE]
> 以下の手順で Windows PowerShell スクリプトを実行します。 Azure CLI の **Try it** オプションを使用した場合や、コンピュータ上でスクリプトを実行した場合は、設定がうまくいかないことがあります。

以下の手順で、Windows PowerShell スクリプトを使用して Azure を構成します。 Azure リソース グループ、Azure リソース、 Azure AD アプリケーションを作成する権限を持っている必要があります。 必要なアクセス許可については、[Azure AD のアクセス許可の確認](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)を参照してください。

1. [Azure portal](https://portal.azure.com)で、対象の Azure サブスクリプションにアクセスします。
2. **検索** フィールドの右側にある **Cloud Shell** を選択します。
3. **PowerShell** を選択します。
4. ストレージの作成を促された場合は、作成します。
5. **Azure CLI** タブで、**コピー** を選択します。
6. メモ帳で新しいファイルを開き、Windows PowerShell スクリプトに貼り付けます。
7. ファイルを **ConfigureDataLake.ps1** として保存します。
8. Windows PowerShell スクリプトをセッションにアップロードするには、Cloud Shell のメニュー オプションであるアップロードを使用します。
9. **.\ConfigureDataLake.ps1** スクリプトを実行します。
10. プロンプトに従ってスクリプトを実行します。
11. スクリプト出力の情報を使用して、LCS に Data Lake にエクスポートするアドインをインストールします。

### <a name="manual-setup"></a>手動設定

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Azure AD テナントへのアプリケーションの追加

1. [Azure ポータル](https://portal.azure.com)で **Azure Active Directory** にアクセスします。
2. **管理 \> エンタープライズ アプリケーション** を選択します。
3. 次のアプリケーションをアプリ ID で検索します。

    | 申請書                              | アプリ ID                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP マイクロサービス     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP マイクロサービス CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder の承認サービス         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

前述のアプリケーションが見つからない場合は、次の手順を実行します。

1. ローカル コンピューターで、**スタート** メニューを開き、**powershell** を検索します。
2. **Windows PowerShell** を右クリックし、**管理者として実行** を選択します。
3. 以下のコマンドを実行して **AzureAD** モジュールをインストールします。

    `Install-Module -Name AzureAD`

4. NuGet プロバイダーを続行する必要がある場合は、**Y** を選択してインストールします。
5. 「信頼できないリポジトリ」のメッセージが表示された場合は、**Y** を選択して続行します。
6. 追加の必要がある各アプリケーションについては、以下のコマンドを実行してアプリケーションを Azure AD に追加します。 プロンプトが表示されたら、管理者で Azure AD にログインします。

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure リソースの作成

> [!NOTE]
> Dataverse 環境と同じ Azure AD インスタンスに以下のリソースが作成されていることを確認してください。 別の Azure AD インスタンスのリソースを使用することはできません。

1. ストレージ アカウントを作成します。

    1. [Azure ポータル](https://portal.azure.com)で、新しいストレージ アカウントを作成します。
    2. **ストレージ アカウントの作成** ダイアログ ボックスで、次のフィールドを設定します。

        - **場所** - ご利用の環境が設置されているデータセンターを選択します。
        - **パフォーマンス** - **標準** を選択することをお勧めします。
        - **アカウントの種類** - 必ず **Storage V2** を選択してください。

    3. **詳細オプション** ダイアログボックスの **Data Lake storage Gen2** オプションで、**階層型名前空間** 機能配下の **有効** を選択します。 この機能を有効にしない場合は、財務と運用アプリで書き込んだデータを Power BI データ フローなどのサービスから使用できません。
    4. **確認して作成** を選択します。 デプロイが完了したら、新しいリソースが Azure ポータルに表示されます。
    5. 作成したストレージ アカウントに移動します。
    6. 左側のメニューで、**アクセス キー** を選択します。
    7. ストレージのアカウント名をコピーして保存し ます。 後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。

2. キー コンテナーの作成:

    1. [Azure portal](https://portal.azure.com)で、新しいキー コンテナーを作成します。
    2. **Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。
    3. キー コンテナーの作成後、**キー コンテナーの概要** に移動し、DNS 名をコピーして保存します。 後続の処理でData Lake アドインを設定する際に、このシークレットの値を入力する必要があります。

3. Azure AD アプリケーションを作成、登録します。

    1. [Azure portal](https://portal.azure.com) で、**Azure Active Directory** にアクセスし、**App registrations** を選択します。
    2. **新規アプリケーションの登録** を選択し、次のフィールドを設定します。

        - **名前** - アプリの名前を入力します。
        - **アプリケーション タイプ** - **Web API** を選択します。
        - **リダイレクト URI の設定** - Dynamics 365 インスタンスの URL を入力します (例: `https://yourdynamicsinstance.dynamics.com/auth` )。

    3. 作成したアプリに移動し、**アプリケーション (クライアント) ID** の値をコピーして保存します。 後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。
    4. **API アクセス許可** に移動し、次の手順に従います。

        1. **アクセス許可の追加** を選択します。
        2. **Azure Key vault** を選択します。
        3. [委任されたアクセス許可] を選択した後、**ユーザー\_なりすまし** を選択します。
        4. **アクセス許可の追加** を選択します。

    5. アプリのメニューで、**証明書\&シークレット** を選択し、次の手順に従ってキー コンテナーのシークレットを作成します。

        1. **新しいクライアント シークレット** を選択します。
        2. **キーの説明** フィールドに、名前を入力します。
        3. 期間を選択し、**追加** を選択します。 シークレットが **値** フィールドに生成されます。
        4. クライアントのシークレットの値をコピーして保存します。 後続の処理でキー コンテナーを設定する際に、このシークレットの値を入力する必要があります。

4. 新しいキー コンテナーの作成:

    1. 前述の手順で作成したキー コンテナーに移動し、**シークレット** を選択します。
    2. 次の表の各シークレットに対して、次の手順を実行します。

        1. **生成/インポート** を選択します。
        2. **シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。
        3. 次の表から、シークレットの名前と値を作成します。
        4. **有効** を選択し、**作成** を選択します。 シークレットが作成され、Key Vault に追加されます。

        | シークレット名                       | シークレットの値                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | アプリ ID                            | 先ほど作成したアプリケーションのアプリ ID です。                                      |
        | アプリのシークレット                        | 先ほど保存したクライアント シークレットです。                                                    |
        | storage-account-name              | 前に作成したストレージ アカウントの名前です (例: **sstorageaccount1**)。       |

5. アプリケーションを承認してキー コンテナーにアクセスする方法:

    1. [Azure portal](https://portal.azure.com)で、作成済のキー コンテナーを開きます。
    2. アクセス ポリシーを選択します。
    3. 次のアプリケーションに対して、次の手順を実行します。

        1. **アクセス ポリシー** を選択し、アクセス ポリシーを作成します。
        2. **シークレットのアクセス許可** フィールドで、テーブルからアクセス許可を選択します。
        3. **プリンシパルの選択** フィールドで、テーブルからアプリケーションの表示名を検索します。
        4. **選択** を選択します。
        5. **追加** を選択します。
        6. **保存** を選択します。

        | 申請書                                              | アクセス許可 |
        |----------------------------------------------------------|-------------|
        | 作成した新しいアプリケーションの表示名称 | 取得、リスト表示   |
        | **Microsoft Dynamics ERP マイクロサービス**                 | 取得、リスト表示   |

6. ストレージ アカウントにアクセスするロールを割り当てるには、次の操作を行います:

    1. [Azure ポータル](https://portal.azure.com)で、作成済のストレージ アカウントを開きます。
    2. **アクセスの制御 (IAM)** を選択し 、**ロールの割り当て** を選択します。
    3. **追加、 ロールの割り当ての追加** を選択します。
    4. 次のアプリケーションに対して、次の手順を実行します。

        1. テーブルからロールを選択します。
        2. **アクセス権の割り当て先** シールドは、**Azure AD ユーザー、グループ、またはサービス プリンシパル** のままにします。
        3. **選択** フィールドで、テーブルからアプリケーションを入力します。
        4. **保存** を選択します。

        | 申請書                                              | 役割                        |
        |----------------------------------------------------------|-----------------------------|
        | 作成した新しいアプリケーションの表示名称 | 所有者                       |
        | 作成した新しいアプリケーションの表示名称 | 寄稿者                 |
        | 作成した新しいアプリケーションの表示名称 | ストレージ アカウントの共同作成者 |
        | 作成した新しいアプリケーションの表示名称 | ストレージ BLOB データの所有者     |
        | **AI Builder の承認サービス**                     | ストレージ BLOB データの読み取り    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Data Lake アドインへのエクスポートの構成

LCS を使用して Data Lake アドインを環境へのエクスポートを追加するには、次の手順に従います。

1. LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。
2. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。
3. **Data Lake へのエクスポート** アドインを選択します。
4. 次の値を入力します。

    | 先頭値                                                              | 説明 |
    |--------------------------------------------------------------------|-------------|
    | キーの保管場所がある Azure サブスクリプションのテナント ID | ストレージ アカウント、アプリ、キーコンテナーが配置されているテナント ID です。 この値を取得するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。 |
    | Key Vault の DNS 名を指定する                             | キー コンテナーの DNS 名 (例:  `https://customkeyvault.vault.azure.net/`)。 |
    | ストレージ アカウントの名前を含むシークレットを指定します   | **storage-account-name** |
    | Data Lake へのアクセスに使用するアプリ ID のシークレット名          | **アプリの ID** |
    | アプリケーションのクライアント シークレットのシークレット名                                  | **アプリのシークレット** |

5. 条件に同意し、**インストール** を選択し ます。

このアドインは数分以内にインストールされます。

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights アドインの構成

> [!NOTE]
> 既に Get insights アドインをインストールしていた場合は、アンインストールしてから次の手順を実行してください。

以下の手順で Finance insights アドインをインストールします。

1. LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。
2. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。
3. **Finance insights** アドインを選択します。
4. 条件に同意し、**インストール** を選択し ます。

アドインのインストールに数分かかる場合があります。

## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックをお寄せくださるか、サポートが必要な場合は、[Finance Insights](mailto:fiap@microsoft.com) にメールでお問い合わせください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
