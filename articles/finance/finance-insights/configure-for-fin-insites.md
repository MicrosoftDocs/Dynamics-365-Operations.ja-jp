---
title: Finance Insights の構成 (プレビュー版)
description: このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664093"
---
# <a name="configuration-for-finance-insights-preview"></a>Finance Insights の構成 (プレビュー版)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance insights では、Common Data Service を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、強力な予測ツールを提供します。 このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance のデプロイ

環境をデプロイするには、次の手順に従います。

1. Microsoft Dynamics Lifecycle Services (LCS) で、Dynamics 365 Finance 環境を作成または更新します。 この環境では、アプリ バージョン10.0.11/プラットフォーム更新プログラム 35またはそれ以降が必要となります。
2. この環境は、サンドボックスの高可用性 (HA) 環境である必要があります。 (このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。
3. Contoso のデモデータを使用している場合は、顧客支払予測、キャッシュフロー予測、予算予測機能の使用にあたり、追加のサンプルデータが必要になります。 

## <a name="configure-common-data-service"></a>Common Data Service のコンフィギュレーション

以下の手動構成ステップを完了するか、提供されている Windows PowerShell スクリプトを使用すると設定のプロセスを高速化することができます。 PowerShell スクリプトの実行が完了すると、Finance insights の構成に使用する値が提供されます。 

> [!NOTE]
> スクリプトを実行するには、PCで PowerShell を開きます。 PowerShell バージョン5 が必要となる場合があります。 Microsoft Azure CLI の "Try it" オプションが機能しない場合があります。

# <a name="manual-configuration-steps"></a>[手動構成の手順](#tab/configuration-steps)

1. [Power Platform 管理センター ](https://admin.powerplatform.microsoft.com/)を開き、次の手順に従って、同じ Active Directory テナントに新しい Common Data Service 環境を作成します。

    1. **環境** ページを開きます。

        [![ 環境ページ](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. **新しい環境** を選択します。
    3. **タイプ** フィールドで、**サンドボックス** を選択します。
    4. **データベースの作成** オプションを、**はい** に設定します。
    5. **次へ** を選択します。
    6. 組織で使用する言語と通貨を選択します。
    7. その他のすべてのフィールドで使用する規定値を受け入れます。
    8. **保存** を選択します。
    9. **環境** ページを更新します。
    10. **状態** フィールドの値が **準備完了** に更新されるまで待機します。
    11. Common Data Service コンテナ― ID をメモします。
    12. 環境を選択し、**設定** を選択します。
    13. **リソース \> すべてのレガシー設定** を選択します。
    14. トップ ナビゲーションバーで、**設定** を選択し、**カスタマイズ** を選択します。
    15. **開発者リソース** を選択します。
    16. **インスタンス参照情報の ID** フィールドを、前述の手順でメモした  Common Data Service 組織 ID の値に設定します。
    17. ブラウザーのアドレスバーで、Common Data Service 組織の URL をメモします。 URL は次のようなものになるでしょう: [`https://org42b2b3d3.crm.dynamics.com`]。

2. キャッシュフロー予測機能や予算予測機能を使用する場合は、次の手順に従って、注釈の制限を少なくとも 50 メガバイト (MB) に更新してください。

    1. [Power Apps ポータル](https://make.powerapps.com)を開きます。
    2. 作成した環境を選択し、 **詳細設定** を選択します。
    3. **設定 \> 電子メールの構成** を選択します。
    4. **最大ファイルサイズ** フィールドの値を **51,200** に変更します。 (値は、キロバイト \[KB\] で表されます。)
    5. **OK** を選択して変更を保存します。

# <a name="windows-powershell-configuration-script"></a>[Windows PowerShell 構成スクリプト](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>Azure の設定を構成する

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a>Common Data Service ディレクトリ ID とユーザーの Azure AD オブジェクト ID を入力します

1. Common Data Service ディレクトリ ID を入力します。

    1. [Azure ポータル](https://portal.azure.com)を開きます。
    2. Common Data Service 環境の作成に使用したユーザー ID を使用してログインします。
    3. **Azure Active Directory** に移動します。
    4. **テナント ID** の値をコピーします。

2. ユーザーの Azure Active Directory (Azure AD) オブジェクト ID を入力します。

    1. [Azure portal](https://portal.azure.com)で、**ユーザー** に移動して電子メールアドレスでユーザーを検索します。
    2. ユーザーの名前を選択します。
    3. **オブジェクト ID** の値をコピーします。

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Azure Cloud Shell を使用した Finance insights Data Lake リソースの設定

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell スクリプトを使用する](#tab/use-a-powershell-script)

Windows PowerShell スクリプトが指定されているため、[Azure Data Lakeへのエクスポートの構成](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake)で説明されているように Azure リソースを簡単に設定できます。 手動による設定を行う場合は、この手順を省略して、[手動設定](#manual-setup)の手順に進みます。

> [!NOTE]
> PowerShell スクリプトを実行するには、次の手順を実行します。 Azure CLI の "Try it" オプション、または PC 上でのスクリプト実行ができない場合があります。

Windows PowerShell スクリプトを使用して Azure をコ構成するには、次の手順に従います。 Azure リソース グループ、Azure リソース、 Azure AD アプリケーションを作成する権限を持っている必要があります。 必要なアクセス許可については、[Azure AD のアクセス許可の確認](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)を参照してください。

1. [Azure portal](https://portal.azure.com)で、対象の Azure サブスクリプションにアクセスします。 **検索** フィールドの右側にある **Cloud Shell** ボタンを選択します。
2. **PowerShell** を選択します。
3. プロンプトが表示された場合は、ストレージを作成します。 その後、Windows PowerShell スクリプトをセッションにアップロードします。
4. スクリプトを実行します。
5. プロンプトに従ってスクリプトを実行します。
6. スクリプト出力の情報を使用して、LCS に **Data Lake にエクスポートする** アドインをインストールします。
7. スクリプト出力の情報を使用して、Finance (**システム管理 \> システムパラメーター \> データ接続**) の **データ接続** ページのエンティティストアを有効にします。

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

1. ローカル コンピューターで、**スタート**  メニューを選択し、**powershell** を検索します。
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
> Common Data Service 環境と同じ Azure AD インスタンスで次のリソースを作成してください。 別の Azure AD インスタンスのリソースを使用することはできません。

1. 新しいストレージ アカウントを作成する方法:

    1. [Azure ポータル](https://portal.azure.com)で、新しいストレージ アカウントを作成します。
    2. **ストレージ アカウントの作成** ダイアログ ボックスで、次のフィールドを設定します。

        - **場所** - ご利用の環境が設置されているデータセンターを選択します。
        - **パフォーマンス** - **標準** を選択することをお勧めします。
        - **アカウントの種類** - 必ず **Storage V2** を選択してください。

    3. **詳細オプション** ダイアログボックスの **Data Lake storage Gen2** オプションで、**階層型名前空間** 機能配下の **有効** を選択します。 この機能を無効にすると、Power BI データ フローなどのサービスを含む Finance and Operations アプリが書き込んだデータを使用することができません。
    4. **確認して作成** を選択します。 配置が完了したら、新しいリソースが Azure ポータルに表示されます。
    5. 作成したストレージ アカウントに移動します。
    6. 左側のメニューで、**アクセス キー** を選択します。
    7. **Key1** または **Key2** の接続文字列をコピーして保存します。
    8. ストレージアカウント名をコピーして保存し ます。

2. 新しいキー コンテナーの作成:

    1. [Azure portal](https://portal.azure.com)で、新しいキー コンテナーを作成します。
    2. **Key Vault の作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。
    3. キー コンテナーが作成されたら、一覧で選択し、**シークレット** を選択します。
    4. **生成/インポート** を選択します。
    5. **シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。
    6. シークレットの名前を入力します。 その後で指定する必要があるため、名前をメモします。
    7. **値** フィールドに、前述の手順でストレージ アカウントから取得した接続文字列を入力します。
    8. **有効** を選択し、**作成** を選択します。 シークレットが作成され、Key Vault に追加されます。
    9. **キー コンテナーの概要** を開き、DNS 名を控えておきます。

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
        4. シークレットの値をコピーして保存します。

4. 新しいキー コンテナーの作成:

    1. 前述の手順で作成したキー コンテナーに移動し、**シークレット** を選択します。
    2. 次の表の各シークレットに対して、次の手順を実行します。

        1. **生成/インポート** を選択します。
        2. **シークレットを作成** ダイアログ ボックスの **アップロード オプション** フィールドで、**手動** を選択します。
        3. 次の表から、シークレットの名前と値を作成します。
        4. **有効** を選択し、**作成** を選択します。 シークレットが作成され、Key Vault に追加されます。

        | シークレット名                       | シークレットの値                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | アプリ ID                            | 作成済みのアプリケーション アプリ ID                                      |
        | アプリのシークレット                        | 前述の手順で保存したクライアント シークレット                                                    |
        | storage-account-name              | 前に作成したストレージアカウントの名前 (例: **sstorageaccount1**)       |
        | ストレージ - アカウント - 接続 - 文字列 | ストレージ アカウントの **アクセス キー** ページからコピーした接続文字列 |

5. アプリケーションを承認してキー コンテナーにアクセスする方法:

    1. [Azure portal](https://portal.azure.com)で、作成済のキー コンテナーを開きます。
    2. アクセス ポリシーを選択します。
    3. 次のアプリケーションに対して、次の手順を実行します。

        1. **アクセス ポリシー** を選択し、アクセス ポリシーを作成します。
        2. **シークレットのアクセス許可** フィールドで、次の表からアクセス許可を選択します。
        3. **プリンシパルの選択** フィールドで、次の表からアプリケーションの表示名を検索します。
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

        1. 以下の表からロールを選択します。
        2. **アクセス権の割り当て先** シールドは、**Azure AD ユーザー、グループ、またはサービス プリンシパル** のままにします。
        3. **選択** フィールドで、次の表からアプリケーションを入力します。
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
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
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

## <a name="configure-the-entity-store"></a>エンティティの保存を構成する

Finance 環境でエンティティの保存を設定するには、次の手順に従います。

1. **システム管理 \> 設定 \> システム パラメーター \> データ接続** に移動します。
2. **Data Lake 統合の有効化** オプションを **はい** に設定します。
3. 次のキー コンテナー フィールドを設定します。

    - **アプリケーション (クライアント) ID**: 以前に作成したアプリケーションクライアント ID を入力します。
    - **アプリケーションのシークレット** - 以前に作成したアプリケーションで使用する保存済みのシークレットを入力します。
    - **DNS 名** - ドメイン ネーム システム (DNS) 名は、前述の手順で作成したアプリケーションの [アプリケーションの詳細] ページで確認できます。
    - **シークレット名** - **ストレージ アカウントの接続文字列** を入力します。

## <a name="configure-the-data-lake"></a>Data Lake を構成する

LCS を使用して Azure Data Lake アドインを環境に追加するには、次の手順に従います。

1. LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。
2. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。
3. **Data Lake へのエクスポート** アドインを選択します。
4. 次の値を入力します。

    | 先頭値                                                              | 説明 |
    |--------------------------------------------------------------------|-------------|
    | キーの保管場所がある Azure サブスクリプションのテナント ID | ストレージ アカウント、アプリ、キーコンテナーが配置されているテナント ID です。 この値を検索するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。 |
    | Key Vault の DNS 名を指定する                             | キー コンテナーの DNS 名 (例:  `https://customkeyvault.vault.azure.net/`)。 (この値は、エンティティ ストアで使用されている DNS 名と同一のものです。) |
    | ストレージ アカウントの名前を含むシークレットを指定します   | **storage-account-name** |
    | Data Lake へのアクセスに使用するアプリ ID のシークレット名          | **アプリの ID** |
    | アプリの ID に使用するシークレット名                                 | **アプリのシークレット** |

5. 条件に同意し、**インストール** を選択し ます。

このアドインは数分以内にインストールされます。

## <a name="configure-ai-builder"></a>AI Builder の構成

1. LCS にサインインし、**環境の詳細** ページを開きます。
2. **環境アドイン** セクションまでスクロールします。 この環境に既にインストールされているアドインが表示されます。 **Data Lake にエクスポートする** アドインがない場合は、このアドインを構成します。
3. **分析情報の取得** アドインを選択します。
4. **分析情報の取得** アドインの詳細ページで、次の値を入力します。

    | 先頭値                                                    | 説明 |
    |----------------------------------------------------------|-------------|
    | CDS 組織の URL                                     | Common Data Service インスタンスの Common Data Service 組織の URL です。 この値を見つけるするには、[Power Apps ポータル](https://make.powerapps.com)を開き、右上隅にある **設定** ボタン (歯車記号) を選択し、**詳細設定** を選択して、URLをコピーします。 URL の末尾には "dynamics.com" が付きます |
    | CDS Org ID                                               | Common Data Service インスタンスの環境 ID を入力します。 この値を見つけるするには、[Power Apps ポータル](https://make.powerapps.com)を開き、右上隅にある **設定** ボタン (歯車記号) を選択し、**カスタマイズ \> 開発者リソース \> インスタンスの参照情報** を選択し、**ID** 値をコピーします。 |
    | CDS テナント ID (AAD のディレクトリ ID)               | Common Data Service インスタンスのテナント ID です。 この値を検索するには、[Azure portal](https://portal.azure.com) を開き、**Azure Active Directory** に移動し、**テナント ID** の値をコピーします。 |
    | システム管理者ロールを持つユーザー オブジェクトの ID を指定します | Azure AD のユーザーの Common Data Service ユーザーのオブジェクト ID です。 このユーザーは、Common Data Service インスタンスのシステム管理者である必要があります。 この値を検索するには、[Azure portal](https://portal.azure.com)を開き、**Azure Active Directory\>** ユーザーに移動し、ユーザーを選択して、**ID** セクションで **オブジェクト ID** 値をコピーします。 |
    | これはテナントの既定の CD 環境ですか？      | Common Data Service インスタンスが最初に作成された運用インスタンスの場合は、このチェックボックスを選択します。 Common Data Service インスタンスが手動で作成された場合は、このチェックボックスをオフにします。 |

## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックの提供またはサポートが必要な場合は、[顧客支払い分析情報 (プレビュー)](mailto:fiap@microsoft.com) に電子メールを送信してください。

## <a name="privacy-notice"></a>プライバシー通知

プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。
