---
title: Microsoft Power Platform 統合を有効にする
description: このトピックでは Finance and Operations アプリと Dataverse をMicrosoft Dynamics Lifecycle Services (LCS) に使用して Microsoft Power Platform 統合を有効にする方法について説明します。
author: jaredha
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-10-13
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: aa538ab30196459c24b58542aa4b9bf44bbfe285
ms.sourcegitcommit: ed43ceae9b2ef3f616b81127bcf4c4b0862e23f5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2021
ms.locfileid: "7714835"
---
# <a name="enable-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合を有効にする

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance and Operations アプリと Microsoft Power Platform の統合は Microsoft Dynamics Lifecycle Services (LCS) で新しい Finance and Operations アプリ環境を作成する時に有効にできます。 または、既存の Finance and Operations アプリ環境で Microsoft Power Platform を有効にすることもできます。 どちらのオプションでも、セットアップの前提条件を満たす必要があります。

## <a name="prerequisites-for-setting-up-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合を設定するための前提条件

次のリストは、Microsoft Power Platform 統合を設定するための前提条件を示しています。

- テナントで少なくとも 1 ギガバイト (GB) の Microsoft Power Platform データベース ストレージ容量スペースが使用可能であることを確認してください。 この領域が利用できない場合、設定は失敗します。 [Power Platform 管理センター](https://admin.powerplatform.microsoft.com/resources/capacity)で、容量を表示できます。 

- Finance and Operations アプリ環境管理者を識別します。 **環境の詳細** セクションにて、情報を確認できます。

    ![環境の詳細セクションの環境管理者情報。](media/EnvironmentDetails.png)

- Microsoft Power Platform 環境のガバナンス ポリシーを検証します。 この検証を行うには、**グローバル管理者** ロールまたは **Power Platform 管理者** ロールのいずれかが必要です。

    1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。
    2. ページの右上隅にある **設定** を選択して、**Power Platform 設定** ウィンドウを開きます。

        ![Power Platform 設定ウィンドウ。](media/PowerPlatformSettings.png)

-  Microsoft Power Platform 実稼働環境の作成を **全員に許可しない** 組織の場合、ご使用の環境の Finance and Operations アプリ環境管理者のアカウントを次の Microsoft Power Platform 管理ロールのいずれかに追加する必要があります。 この変更を行うには、**グローバル管理者** ロールが必要です。

    - Global 管理者
    - Dynamics 365 管理者
    - Microsoft Power Platform 管理者

    > [!NOTE]
    > 上記のロールは、Finance and Operations アプリ環境管理者アカウントに必要なものより多くのアクセス許可を提供する場合があります。 したがって、この統合にさらに制限されたロールが最終的に Azure Active Directory (Azure AD) に追加されます。 新しいロールに上記のロールは必要ではありません。 最小限の特権の管理者を維持する場合、一時的に上記のロールの 1 つを付与できます。 Microsoft Power Platform 統合が設定された後、そのロールを削除します。

- Microsoft Power Platform 環境を作成するすべてのユーザーはライセンスが必要です。 Microsoft 365 管理センターを使用して **Dynamics 365 Unified Operations プラン**、または **AX エンタープライズ** ライセンス、または **Dynamics 365 Finance** などのアプリケーション固有のライセンスを Finance and Operations アプリ環境の管理者アカウントに適用する必要があります。

## <a name="enable-integration-during-environment-deployment"></a><a name="enable-during-deploy"></a> 環境の配置中に統合を有効にする

LCS に新しい Finance and Operations アプリ環境を設定する際、配置ウィザードには値を設定することができる複数のセクションがあります。 それらセクションの 1 つが **Power Platform 統合** という名前です 。

![配置ウィザードの Power Platform 統合セクション。](media/powerplat_integration_step0.png)

**Power Platform 統合** セクションを構成するには、次の手順に従います。

1. **Power Platform 環境の構成** オプションを **はい** に設定します。 複数の追加設定が使用可能になります。
2. **Power Platform テンプレート** フィールドで、次のいずれかの値を選択します。

    - **Dynamics 365 標準** – この基本テンプレートは、すべての Finance and Operations アプリ環境に適用できます。 特定のテンプレートが必要ない場合、この値を選択します。
    - **Project Operations** – このテンプレートは、プロジェクト操作の Dynamics 365 Project Operations シナリオに固有のものです。 この値は、テナントが Project Operations のライセンスと資格を持っている場合にのみ利用できます。

3. DevTest またはクラウド ホスト環境を配置する場合、**環境の種類** フィールドが使用可能です。 そこで、作成およびリンクされる Dataverse 環境のタイプを選択できます。 それ以外の場合、既定では、環境の種類はレベル 2 から 5 の承認テスト環境の場合は **サンドボックス** に、運用環境の場合は **運用** に設定されます。
4. **同意** を選択して、統合の使用条件に同意することを示します。

> [!IMPORTANT]
> Finance and Operations アプリ環境に作成およびリンクされる Dataverse 環境の **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は米ドル (USD) になります。
>
> 既定値とは異なる値が必要な場合、Microsoft サポートに問い合わせください。 手動でプロビジョニングした既存の Dataverse 環境を Finance and Operations アプリ環境にリンクするサポートを提供できます。 最終的に、設定オプションとして言語と通貨のフィールドが追加され、手動で設定したり、既定値を受け入れることができるようになります。

## <a name="enable-integration-after-environment-deployment"></a><a name="enable-after-deploy"></a> 環境の配置後に統合を有効にする

Finance and Operations アプリ環境の配置中に Microsoft Power Platform が有効になっていない場合、配置後に LCS で有効にすることができます。 Finance and Operations アプリ環境が配置された後に設定するには、次の手順に従います。

1. Finance and Operations アプリ環境が LCS を介して配置された後、LCS の **環境詳細** ページが開きます。
2. **Power Platform 統合** セクションで、**設定** を選択します。

    ![Power Platform 統合セクションの設定ボタン。](media/powerplat_integration_step1.png) 

3. **Power Platform 環境設定** ダイアログ ボックスで契約条件に同意し、**設定** を選択します。

    > [!NOTE]
    > これで Dataverse ベースの環境が Power Platform 管理センターに準備されます。 この環境には通常 1 GB のデータベース ストレージ容量が必要で、Finance and Operations アプリ環境と同じ名前になります。 二重書き込みプラットフォーム レベルのコンポーネントはインストールされますが、二重書き込みアプリケーション コンポーネントは設定または有効化されません。 それらのアクションは別個のものです。

4. Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。

    **環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。

5. 数分後、**環境の詳細** ページが更新されます。
6. **Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。

    通常、設定は 60分 から 90分かかります。

    Dataverse 環境が準備された後、**新しいアドインのインストール** と **二重書き込みアプリケーション** ボタンが **Power Platform 統合** セクションで利用できるようになります。

    ![新しいアドイン ボタンをインストールします。](media/InstallANewAddIn.png)

    ![二重書き込みアプリケーション ボタン。](media/powerplat_integration_dwApp_button.png)

> [!IMPORTANT]
> Finance and Operations アプリ環境に作成およびリンクされる Dataverse 環境の **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は米ドル (USD) になります。
>
> 既定値とは異なる値が必要な場合、Microsoft サポートに問い合わせください。 手動でプロビジョニングした既存の Dataverse 環境を Finance and Operations アプリ環境にリンクするサポートを提供できます。 最終的に、設定オプションとして言語と通貨のフィールドが追加され、手動で設定したり、既定値を受け入れることができるようになります。

## <a name="enable-integration-with-an-existing-selected-microsoft-power-platform-environment"></a>選択した既存の Microsoft Power Platform 環境との統合を有効にする

LCS で Finance and Operations アプリ環境の Microsoft Power Platform 統合を有効にすると、配置中または配置後に、プロセスによって Dataverse 対応の新しい Microsoft Power Platform 環境が作成され、Finance and Operations アプリ環境が新しい Microsoft Power Platform 環境にリンクされます。 しかし、Finance and Operations アプリ環境を、配置中に自動的に作成された環境ではなく、既存の Microsoft Power Platform 環境にリンクさせて統合を有効化したい場合もあります。 Power Platform 統合を有効にする Power Platform 環境を選択するオプションは現在 LCS では利用できません。

既存の環境で Power Platform 統合を有効にする方法は、Finance and Operations アプリ環境にリンクされている Power Platform 環境の数によって異なります。 Power Platform 統合を有効にする前に、Finance and Operations アプリ環境が Power Platform 環境にリンクされているとみなす方法が複数あります。
- **配置リンク**: 新しい Finance and Operations 環境の配置中に、Power Platform 統合を有効にするオプションが選択されていない場合でも、新しい Power Platform 環境が作成され Finance and Operations 環境にリンクされます。 このリンクは、Power Platform 管理センターにある新しい Power Platform 環境の環境詳細の **Finance and Operations URL** フィールドに表示されます。
- **二重書き込み**: このオプションは、二重書き込み構成で、テナント上の任意の Power Platform 環境で Dataverse 環境へのリンクを作成できます。
- **仮想エンティティ**: Power Platform 環境の仮想エンティティ構成では、Finance and Operations 環境を選択することができます。

これら 3 つの構成は、必ずしも Finance and Operations アプリ環境を同じ Power Platform 環境にリンクするとは限りません。 Power Platform と既存の Microsoft Power Platform 環境の統合を有効にするシナリオは 2 つあります。

- **単一 Power Platform 環境**: このシナリオでは、単一の Power Platform 環境に一致したリンクが Finance and Operations アプリ環境にあります。 二重書き込みまたは仮想エンティティが Finance and Operations アプリ環境用に構成されている場合、Finance and Operations アプリ環境の配置中に作成されたのと同じ Power Platform 環境にリンクするように構成されます。 
- **複数 Power Platform 環境**: Finance and Operations アプリ環境と複数の Power Platform 環境の間の既存のリンクに、リンクの不一致があります。

### <a name="finance-and-operations-apps-connected-to-a-single-microsoft-power-platform-environment"></a>単一の Microsoft Power Platform 環境に接続された Finance and Operations アプリ

Finance and Operations アプリ環境が単一の Microsoft Power Platform 環境へのリンクで構成されている場合、これらの環境は 1 対 1 のリンクとして識別されます。 これらの環境では、Finance and Operations アプリ バージョン 10.0.22 (プラットフォーム update 46) で 1 対 1 のリンク環境が自動的に更新され、Finance and Operations アプリ環境での Microsoft Power Platform の完全な統合が可能になります。 

バージョン 10.0.22 では、Microsoft Power Platform 統合が自動的に有効になったことを、LCS の Finance and Operations アプリ環境の **環境詳細** ページの **Power Platform 統合** セクションを表示することで確認できます。 統合が正常に有効化された場合、**環境名** フィールドには統合された Microsoft Power Platform 環境の名前が表示され、**状態** フィールドは **設定は正常に完了しました** に設定されます。

> [!NOTE]
> 単一の Microsoft Power Platform 環境にすでに接続されており、ビジネス イベント機能をすでに使用している Finance and Operations アプリ環境に対しては Microsoft Power Platform 統合は自動的に有効になります。 ただし、これらの環境では、リリース 10.0.22 以降の新しいビジネス イベントおよびデータ イベント機能を使用できなくなります。 これらの環境で既に使用されているビジネス イベントのエンドポイントは、バージョン 10.0.23 の Dataverse プラットフォームに移行されます。 その時点で、新しいビジネス イベントとデータ イベントの機能が環境で利用可能になります。 それまでは、ビジネス イベントは現在の環境で構成されている通りに引き続き機能します。
> 
> これらの環境で移行が完了するまで遅延される新しいビジネス イベントおよびデータ イベント機能の詳細については、2021 年リリースのシステム インストール 2 プランの [Finance and Operations Dataverse のビジネス イベント](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-scenarios-enabled-power-platform-convergence#finance-and-operations-business-events-in-dataverse)と [Finance and Operations Dataverse の CUD イベント](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-scenarios-enabled-power-platform-convergence#finance-and-operations-cud-events-in-dataverse)を参照してください。 

### <a name="finance-and-operations-apps-connected-to-multiple-microsoft-power-platform-environments"></a>複数の Microsoft Power Platform 環境に接続された Finance and Operations アプリ

Finance and Operations アプリ環境が複数の Microsoft Power Platform 環境に手動でリンクされている場合、環境の Microsoft Power Platform 統合を有効にするプロセスを自動化することはできません。 システムは、Power Platform 統合のために Finance and Operations アプリ環境をどの Power Platform 環境にリンクする必要があるかを自動的に決定できません。

複数の Power Platform 環境へのリンクがある Finance and Operations 環境で Power Platform 統合を有効にするには、次の 2 つのオプションがあります。
- 二重書き込みまたは仮想エンティティ ソリューションを再構成して、Finance and Operations アプリ環境を配置時に作成された Power Platform 環境にリンクします。 単一の Power Platform 環境に対してすべてのリンクが構成されている場合、上記の[環境の配置後に統合を有効化する](enable-power-platform-integration.md#enable-after-deploy)セクションで説明されている手順に従って LCS の Power Platform 統合を有効化できます。 これは、Microsoft サポートなしで管理できるため、推奨されるソリューションです。
- Finance and Operations 環境の配置中に作成された Power Platform 環境以外のリンクされた Power Platform 環境との Power Platform 統合を有効にするには、FastTrack Solution Architect と協力するか、Microsoft サポートに連絡して選択した環境との Power Platform 統合を有効にします。

二重書き込み構成オプションの詳細については、[リンクの不一致](../data-entities/dual-write/lcs-setup.md#linking-mismatch)を参照してください。

## <a name="enable-the-integration-for-cloud-hosted-development-environments"></a>クラウド ホスト開発環境の統合を有効にする

このセクションの手順を完了することで、クラウド ホスト開発環境の Microsoft Power Platform 統合を手動で有効にできます。 クラウド開発環境の配置方法の詳細については、[開発環境の配置とアクセス](../dev-tools/access-instances.md)を参照してください。

### <a name="register-an-application-in-the-azure-portal"></a>Azure ポータルにアプリケーションを登録する

> [!IMPORTANT]
> Azure AD アプリケーションは、Finance and Operations アプリと同じテナントに作成する必要があります。

1. [Azure ポータル](https://portal.azure.com)を開きます。
2. **Azure Active Directory \> アプリの登録** に移動します。
3. **新しいアプリケーションの登録** を選択し、以下の情報を入力します。

    - **名前** – 一意の名前を入力します。
    - **勘定タイプ** – **任意の組織ディレクトリでのアカウント (任意の Azure AD ディレクトリ - マルチテナント)**。
    - **リダイレクト URI** – このフィールドは空白のままにします。

4. **登録** を選択します。
5. **アプリケーション (クライアント) ID** の値をメモします。 後に、この値を使用します。
6. アプリケーションの対称キーを作成します。

    1. 新しいアプリ登録の左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。
    2. **新しいクライアント シークレット** を選択します。
    3. 説明と有効期限を入力します。
    4. **保存** を選択します。
    5. 作成された **値** フィールドにキーをコピーします。 このキー値は後で必要になります。
 
### <a name="add-the-azure-ad-application-as-a-microsoft-power-platform-user"></a>Microsoft Power Platform ユーザーとして Azure AD アプリケーションを追加する

Azure AD アプリケーションを Azure ポータルで作成した後、Microsoft Power Platform アプリケーション ユーザーとして追加する必要があります。 

1. Power Platform 管理センターで、[アプリケーション ユーザーの作成](/power-platform/admin/manage-application-users#create-an-application-user)の手順に従ってアプリケーション ユーザーを作成します。
2. アプリケーション ユーザーに追加するセキュリティ ロールを選択するステップで、**Finance and Operations 統合ユーザー** を選択します。

### <a name="grant-app-permissions-in-finance-and-operations-apps"></a>Finance and Operations アプリのアクセス許可を付与する

Dataverseは、作成した Azure AD アプリケーションを使用して Finance and Operations アプリを呼び出します。 したがって、アプリケーションは Finance and Operations アプリによって信頼され、適切な権限を持つユーザー アカウントに関連付けられている必要があります。

1. Finance and Operations アプリで、**システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動します。
2. **新規** を選択してグリッドに行を追加し、次の情報を入力します。

    - **クライアント ID** – 既に作成した Azure AD アプリケーションの **アプリケーション (クライアント) ID** の値を入力します。
    - **名前** – **Dataverse 統合** (または統合で認識する別の名前) を入力します。
    - **ユーザー ID** – **PowerPlatformApp** を選択します。

> [!NOTE]
> 利用可能な **PowerPlatformApp** ユーザーは、Finance and Operations アプリとの Dataverse 統合のための適切なアクセス許可を持っています。 ただし、このユーザーが存在しない場合、または別のアプリケーション ユーザー アカウントを使用する場合は、次のいずれかのロールを持つ他のユーザーを作成または使用できます。**ビジネス イベントのセキュリティ ロール**、**Dataverse 仮想エンティティ アプリケーション**、**Dataverse 仮想エンティティ匿名ユーザー**、および **Dataverse 仮想エンティティ認証ユーザー**。

### <a name="configure-finance-and-operations-apps-to-use-the-azure-ad-application-to-connect-to-dataverse"></a>Azure AD アプリケーションを使用して Dataverse に接続するよう Finance and Operations アプリを構成します 

1. リモート デスクトップ プロトコル (RDP) を使用して、Finance and Operations 環境にサインインします。
2. 次の Windows PowerShell スクリプトをコピーし、Finance and Operations 環境の仮想マシン (VM) に .ps1 ファイルとして保存します。

    ```powershell
    param(
        [Parameter(Mandatory = $false)]
        [switch]$Relaunched
    )

    $isRelaunched = $false
    if ($PSBoundParameters.ContainsKey("Relaunched"))
    {
        $isRelaunched = $Relaunched.IsPresent
    }

    if (-not ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator))
    {
        # Relaunch as an elevated process:
        Start-Process powershell.exe "-File", ('"{0}"' -f $MyInvocation.MyCommand.Path), "-Relaunched" -Verb RunAs
        exit
    }

    $aosWebsiteName = "AOSService"

    function Get-AosWebSitePhysicalPath()
    {
        if (Get-Service W3SVC | Where-Object status -ne 'Running')
        {
            #IIS service is not running, starting IIS Service.
            Start-Service W3SVC
        }

        $webSitePhysicalPath = (Get-Website | Where-Object { $_.Name -eq $aosWebsiteName }).PhysicalPath

        return $webSitePhysicalPath
    }

    function Set-WebConfigValue($Key, [string]$Value)
    {
        $webroot = Get-AosWebSitePhysicalPath
        $webConfigPath = Join-Path $webroot "web.config"
        if (-not (Test-Path $webConfigPath))
        {
            Throw "Unable to find web.config file at '$($webConfigPath)'..."
        }

        [xml]$webConfigDocument = Get-Content $webConfigPath -ErrorAction stop
        $appSettingNode = $webConfigDocument.SelectSingleNode("/configuration/appSettings/add[@key='$($Key)']")
        if ($null -ne $appSettingNode)
        {
            Write-Host "Updating key '$($Key)' to value '$($Value)'..."
            $appSettingNode.Value = [string]$Value
        }
        else
        {
            Write-Host "Inserting new key '$($Key)' with value '$($Value)'..."
            $ns = New-Object System.Xml.XmlNamespaceManager($webConfigDocument.NameTable)
            $ns.AddNamespace("ns", $webConfigDocument.DocumentElement.NamespaceURI)
            $addElement = $webConfigDocument.CreateElement("add")
            $addElement.SetAttribute("key", $Key)
            $addElement.SetAttribute("value", $Value)
            $appSettings = $webConfigDocument.SelectSingleNode("//ns:appSettings", $ns)
            $appSettings.AppendChild($addElement) | Out-Null
        }

        $webConfigDocument.Save($webConfigPath)
        Write-Host
    }

    function Confirm-ValueOfType($Value, $Type)
    {
        if ($Type -eq "Uri")
        {
            try
            {
                New-Object System.Uri $Value | Out-Null
            }
            catch
            {
                Throw "Cannot parse '$($Value)' as a URL: $($_)"
            }
        }
        elseif ($Type -eq "Guid")
        {
            try
            {
                [Guid]::Parse($Value) | Out-Null
            }
            catch
            {
                Throw "Cannot parse '$($Value)' as a guid: $($_)"
            }
        }
        elseif ($Type -eq "String")
        {
            if ([string]::IsNullOrEmpty($Value))
            {
                Throw "String value cannot be empty."
            }
        }
    }

    function Update-WebConfigValueFromHost($Key, $Prompt, $Type)
    {
        $value = Read-Host -Prompt $Prompt
        Confirm-ValueOfType -Value $value -Type $Type
        Set-WebConfigValue -Key $Key -Value $value
    }

    function Enable-Flight($FlightName)
    {
        Write-Verbose "Enabling flight '$($FlightName)'..."
        $webroot = Get-AosWebSitePhysicalPath -ErrorAction stop
        $webrootBinPath = Join-Path $webroot "bin"
        $environmentDllPath = Join-Path $webrootBinPath 'Microsoft.Dynamics.ApplicationPlatform.Environment.dll'
        Add-Type -Path $environmentDllPath

        $config = [Microsoft.Dynamics.ApplicationPlatform.Environment.EnvironmentFactory]::GetApplicationEnvironment()

        $ServerName = $config.DataAccess.DbServer
        $DatabaseName = $config.DataAccess.Database
        $UserId = $config.DataAccess.SqlUser
        $Password = $config.DataAccess.SqlPwd
        $EnableFlightQuery = "DECLARE @flightName NVARCHAR(100) = '$($FlightName)';
        IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
            INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID, PARTITION)
            SELECT @flightName, 1, 12719367, RECID FROM DBO.[PARTITIONS];
        ELSE
            UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;"

        Invoke-Sqlcmd -ServerInstance $ServerName -Database $DatabaseName -Username $UserId -Password $Password -Query $EnableFlightQuery
        Write-Verbose "Flight '$($FlightName)' has been enabled."
    }

    function Test-Settings()
    {
        $cdsApiPath = "accounts";
        Write-Host "Testing setup by calling API '$($cdsApiPath)'..."
        $webroot = Get-AosWebSitePhysicalPath -ErrorAction stop
        $webrootBinPath = Join-Path $webroot "bin"
        $httpCommunicationDllPath = Join-Path $webrootBinPath "Microsoft.Dynamics.HttpCommunication.dll"
        Add-Type -Path $httpCommunicationDllPath

        try
        {
            $assembly = [System.Reflection.Assembly]::LoadFile($httpCommunicationDllPath)
            $loggerType = $assembly.GetType("Microsoft.Dynamics.HttpCommunication.Logging.InMemoryLogger")
            $bindingFlags = [System.Reflection.BindingFlags]::Instance -bor [System.Reflection.BindingFlags]::Public
            $loggerConstructor = $loggerType.GetConstructor($bindingFlags, $null, [System.Type]::EmptyTypes, $null)
            $logger = $loggerConstructor.Invoke($null)

            $cdsWebApiClient = New-Object Microsoft.Dynamics.HttpCommunication.Cds.CdsWebApiClient $logger;
            $bindingFlags = [System.Reflection.BindingFlags]::Instance -bor [System.Reflection.BindingFlags]::NonPublic
            $method = [Microsoft.Dynamics.HttpCommunication.Cds.CdsWebApiClient].GetMethod("GetWithStringResponse", $bindingFlags, $null, @([string]), $null)
            $task = $method.Invoke($cdsWebApiClient, @($cdsApiPath))
            $response = $task.GetAwaiter().GetResult()

            $logger.WriteInfo("Received response with length: $($response.Length)")
            Write-Verbose $logger.LogContent.ToString()
            Write-Host "Test complete."
        }
        catch
        {
            Write-Verbose $logger.LogContent.ToString()
            Throw "Failed while testing the new settings: $($_)"
        }
    }

    try
    {
        Update-WebConfigValueFromHost -Key "Infrastructure.CdsOrganizationUrl" -Prompt "Enter Dataverse Organization URL" -Type "Uri"
        Update-WebConfigValueFromHost -Key "Infrastructure.CdsOrganizationId" -Prompt "Enter Dataverse Organization id" -Type "Guid"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAadTenantId" -Prompt "Enter Dataverse AAD Tenant id (e.g. Contoso.OnMicrosoft.com)" -Type "String"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAppId" -Prompt "Enter Dataverse AAD App id" -Type "Guid"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAppSecret" -Prompt "Enter Dataverse AAD App secret" -Type "String"

        Enable-Flight -FlightName "BusinessEventsCDSIntegration"

        Write-Host "Restarting AOS..."
        Stop-Website -Name $aosWebSiteName
        Start-Website -Name $aosWebSiteName
        Write-Host "AOS has been restarted."

        Test-Settings
    }
    catch
    {
        Write-Error $_
    }

    if ($isRelaunched)
    {
        Write-Host "Press any key to continue..."
        [System.Console]::ReadKey() | Out-Null
    }
    ```

3. 指示に従って Windows PowerShell スクリプトを実行します。 次の情報を入力します。

    - **Dataverse 組織 URL** – Dataverse へのアクセスに使用する URL を入力します。 たとえば、「`https://contoso.crm.dynamics.com`」を入力します。 この URL は、Power Platform 管理センターの環境詳細にある **詳細** セクションの **環境 URL** フィールドで見つけることができます。
    - **Dataverse 組織 ID** – この ID は、Power Platform 管理センターの環境詳細にある **詳細** セクションの **組織 ID** フィールドに見つけることができます。
    - **Dataverse AAD テナント ドメイン** – Dataverse で使用される Azure AD テナントのプライマリ ドメインを入力します。 このドメインは、[Asure ポータル](https://portal.azure.com)の **ポータル設定** ページのディレクトリにある **ドメイン** フィールドに見つけることができます。 通常、管理者の電子メール アドレスのドメイン セグメントです。 たとえば、電子メール アドレスが `admin@contoso.onmicrosoft.com` の場合、ドメインは `contoso.onmicrosoft.com` です。
    - **Dataverse AAD アプリ ID** – 既に作成した Azure AD アプリケーションの **アプリケーション (クライアント) ID** の値を入力します。
    - **Dataverse AAD アプリ シークレット** – Azure AD アプリのために既に作成したシークレット キーの値を入力します。

## <a name="troubleshooting-the-setup"></a>設定のトラブルシューティング

設定は、Dataverse ベースの環境を配置するさまざまなステージで失敗する可能性があります。

設定が失敗するたびに、エラー メッセージが表示されます。 次の図は、二重書き込み設定に失敗した場合のエラー メッセージの例を示しています。

![二重書き込み設定に失敗した場合のエラー メッセージ。](media/Error.png)

エラー メッセージに基づいて、ライセンスや容量の問題への対処が必要となる場合があります。 これらの問題が修正されたら、LCS の **環境の詳細** ページの **Power Platform 統合** セクションにある **再開** を選択して設定を完了することができます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
