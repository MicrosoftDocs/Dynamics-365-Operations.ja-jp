---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成の方法について説明します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7379dc84de52942b4882f56af1a44d9549cc5f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745185"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a><span data-ttu-id="b23ab-103">Regression Suite Automation Tool のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="b23ab-103">Regression Suite Automation Tool installation and configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b23ab-104">このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-104">This topic contains information about how to install and configure the Regression suite automation tool (RSAT).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b23ab-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="b23ab-105">Prerequisites</span></span>

### <a name="test-environment-prerequisite"></a><span data-ttu-id="b23ab-106">テスト環境 (前提条件)</span><span class="sxs-lookup"><span data-stu-id="b23ab-106">Test environment (Prerequisite)</span></span>

<span data-ttu-id="b23ab-107">テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-107">Your test environment must be running Platform update 15 or newer.</span></span> <span data-ttu-id="b23ab-108">Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-108">The Regression suite automation tool must have access to your test environment via a web browser.</span></span>

### <a name="excel"></a><span data-ttu-id="b23ab-109">Excel</span><span class="sxs-lookup"><span data-stu-id="b23ab-109">Excel</span></span>

<span data-ttu-id="b23ab-110">テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-110">You need Microsoft Excel installed to generate and edit test parameters.</span></span>

### <a name="azure-devops-prerequisite"></a><span data-ttu-id="b23ab-111">Azure DevOps (前提条件)</span><span class="sxs-lookup"><span data-stu-id="b23ab-111">Azure DevOps (Prerequisite)</span></span>

<span data-ttu-id="b23ab-112">テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-112">You must have an Azure DevOps project to store and manage your test cases, test plans, and test case results.</span></span> <span data-ttu-id="b23ab-113">Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-113">You will need an Azure DevOps Test Manager or Test Plans license.</span></span> <span data-ttu-id="b23ab-114">たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。</span><span class="sxs-lookup"><span data-stu-id="b23ab-114">For example, if you have a Visual Studio Enterprise subscription, you already have a license to Test Plans.</span></span> <span data-ttu-id="b23ab-115">詳細については、[Azure DevOps サービス](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) の価格設定、または [Azure DevOps サーバーの価格設定](https://azure.microsoft.com/pricing/details/devops/server/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-115">For more information, see [Pricing for Azure DevOps Services](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) or [Pricing for Azure DevOps Server](https://azure.microsoft.com/pricing/details/devops/server/).</span></span>

### <a name="authentication-certificate"></a><span data-ttu-id="b23ab-116">認証証明書</span><span class="sxs-lookup"><span data-stu-id="b23ab-116">Authentication Certificate</span></span>

<span data-ttu-id="b23ab-117">RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザーを介して環境にリモート接続するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b23ab-117">RSAT is designed to be installed on any Windows 10 computer and connect remotely via a web browser to an environment.</span></span>

![クライアント コンピュータと環境](media/client-environment.png)

<span data-ttu-id="b23ab-119">セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-119">To enable secure authentication, RSAT requires a certificate to be installed on the RSAT client computer.</span></span> <span data-ttu-id="b23ab-120">RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-120">The RSAT settings dialog box allows you to automatically create and install the authentication certificate.</span></span> <span data-ttu-id="b23ab-121">また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-121">You will also need to configure the virtual machine (VM) to trust the connection.</span></span> <span data-ttu-id="b23ab-122">RSATをインストールして構成するには、次のセクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-122">Follow the instructions in the next sections to install and configure RSAT.</span></span>

## <a name="installation"></a><span data-ttu-id="b23ab-123">インストール</span><span class="sxs-lookup"><span data-stu-id="b23ab-123">Installation</span></span>

### <a name="installer"></a><span data-ttu-id="b23ab-124"> インストーラー</span><span class="sxs-lookup"><span data-stu-id="b23ab-124">Installer</span></span>

<span data-ttu-id="b23ab-125">[Regression Suite Automation Tool ダウンロード](https://www.microsoft.com/download/details.aspx?id=57357) からマシンに .msi ファイルをダウンロードし、ダブルクリックしてインストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-125">Download the .msi file from the [Regression Suite Automation Tool Download](https://www.microsoft.com/download/details.aspx?id=57357) to your machine and double-click it to run the installer.</span></span>

> [!NOTE]
> <span data-ttu-id="b23ab-126">Azure DevOps サーバーを使用している場合は、バージョン 1.210.48249.4 以降をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-126">If you're using Azure DevOps Server, download and install version 1.210.48249.4 or later.</span></span>

### <a name="selenium-and-browser-drivers"></a><span data-ttu-id="b23ab-127">Selenium およびブラウザー ドライバー</span><span class="sxs-lookup"><span data-stu-id="b23ab-127">Selenium and Browser Drivers</span></span>

<span data-ttu-id="b23ab-128">RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-128">RSAT requires Selenium and web browser driver libraries.</span></span> <span data-ttu-id="b23ab-129">RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-129">RSAT will prompt you if needed libraries are missing and will automatically install them for you.</span></span> <span data-ttu-id="b23ab-130">次の (または類似の) メッセージが表示されたら、はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-130">Select Yes when you see the following (or similar) messages.</span></span>

![Selenium ドライバー](media/driver-1.png)

![ブラウザー ドライバー](media/driver-2.png)

<span data-ttu-id="b23ab-133">RSAT は [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-133">RSAT uses [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip).</span></span> <span data-ttu-id="b23ab-134">WebDriver ライブラリおよびブラウザー固有のドライバーは **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-134">The Webdriver library and browser-specific drivers are downloaded to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

## <a name="configuration"></a><span data-ttu-id="b23ab-135">構成</span><span class="sxs-lookup"><span data-stu-id="b23ab-135">Configuration</span></span>

1. <span data-ttu-id="b23ab-136">デスクトップから RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-136">Open RSAT from your desktop.</span></span>

    ![RSAT デスクトップ アイコン](media/desktop-icon.png)

2. <span data-ttu-id="b23ab-138">右上にある **設定** ボタンを選択して、RSAT を構成します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-138">Select the **Settings** tab on the upper left to configure RSAT.</span></span>

    ![RSAT 設定](media/rsat-settings.png)

### <a name="general-settings"></a><span data-ttu-id="b23ab-140">一般設定</span><span class="sxs-lookup"><span data-stu-id="b23ab-140">General settings</span></span>

<span data-ttu-id="b23ab-141">これらの設定は必須です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-141">These settings are required.</span></span>

#### <a name="azure-devops-general-settings"></a><span data-ttu-id="b23ab-142">Azure DevOps (一般設定)</span><span class="sxs-lookup"><span data-stu-id="b23ab-142">Azure DevOps (General settings)</span></span>

<span data-ttu-id="b23ab-143">Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-143">Configure your connection to the Azure DevOps project and test plan.</span></span>

+ <span data-ttu-id="b23ab-144">**Azure DevOps URL** - これは、 Azure DevOps 組織の URL です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-144">**Azure DevOps URL** - This is the URL of your Azure DevOps organization.</span></span> <span data-ttu-id="b23ab-145">たとえば、`https://yourAzureDevOpsUrlHere.visualStudio.com`。</span><span class="sxs-lookup"><span data-stu-id="b23ab-145">For example, `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b23ab-146">Azure DevOps サーバーを使用している場合は、**/DefaultCollection** を Azure DevOps URL の末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-146">If you're using Azure DevOps Server, add **/DefaultCollection** to the end of your Azure DevOps URL.</span></span>

+ <span data-ttu-id="b23ab-147">**アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。</span><span class="sxs-lookup"><span data-stu-id="b23ab-147">**Access Token** - The access token that allows the tool to connect to Azure DevOps.</span></span> <span data-ttu-id="b23ab-148">個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-148">You need to create a personal access token or use an existing one that you have saved.</span></span> <span data-ttu-id="b23ab-149">詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-149">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
+ <span data-ttu-id="b23ab-150">**プロジェクト名** - Azure DevOps プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="b23ab-150">**Project Name** - The name of your Azure DevOps project.</span></span> <span data-ttu-id="b23ab-151">RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-151">RSAT will automatically detect project names and test plans available based the Azure DevOps URL specified.</span></span> <span data-ttu-id="b23ab-152">その後、テスト プロジェクトおよびテスト計画を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-152">You can then select the Test Project and Test Plan.</span></span>
+ <span data-ttu-id="b23ab-153">**テスト計画** - テスト ケースを含む Azure DevOps テスト計画</span><span class="sxs-lookup"><span data-stu-id="b23ab-153">**Test Plan** - The Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="b23ab-154">詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-154">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span>

<span data-ttu-id="b23ab-155">**接続のテスト** を選択し、 Azure DevOps への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-155">Select **Test Connection** to test your connection to Azure DevOps.</span></span>

#### <a name="test-environment-general-settings"></a><span data-ttu-id="b23ab-156">テスト環境 (一般設定)</span><span class="sxs-lookup"><span data-stu-id="b23ab-156">Test environment (General settings)</span></span>

<span data-ttu-id="b23ab-157">テスト環境への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-157">Configure your connection to the test environment.</span></span>

+ <span data-ttu-id="b23ab-158">**ホスト名** – myhost.cloudax.dynamics.com. などのテスト環境のホスト名。</span><span class="sxs-lookup"><span data-stu-id="b23ab-158">**Hostname** – The hostname of the test environment, such as myhost.cloudax.dynamics.com.</span></span> <span data-ttu-id="b23ab-159">https:// または http:// の接頭語を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-159">Don't include the https:// or http:// prefix.</span></span>
+ <span data-ttu-id="b23ab-160">**SOAP ホスト名** – テスト環境の SOAP ホスト名。</span><span class="sxs-lookup"><span data-stu-id="b23ab-160">**SOAP Hostname** – The SOAP hostname of the test environment.</span></span>
    + <span data-ttu-id="b23ab-161">デモおよび開発環境 (1 ボックス環境とも呼ばれる) については、ホスト名に接尾語 **soap** を追加します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-161">For demo and development environments (also known as one-box environments), add a **soap** suffix to the hostname.</span></span> <span data-ttu-id="b23ab-162">たとえば、ホスト名が `myhost.cloudax.dynamics.com` の場合、`myhost.soap.cloudax.dynamics.com` を SOAP ホスト名として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-162">For example, if your hostname is `myhost.cloudax.dynamics.com`, use `myhost.soap.cloudax.dynamics.com` as the SOAP hostname.</span></span>
    + <span data-ttu-id="b23ab-163">テスト環境の SOAP ホスト名がわからない場合は、Infrastructure.SoapServicesUrl の AOS サーバーの web.config ファイルで検索できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-163">If you don't know the SOAP hostname of your test environment, you can find it in the web.config file for the AOS server in Infrastructure.SoapServicesUrl.</span></span>
    + <span data-ttu-id="b23ab-164">テスト環境が、リモート デスクトップ アクセスがないユーザー受け入れテスト (user acceptance testing: UAT) または上位層サンドボックス環境である場合、この SOAP ホスト名はホスト名と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-164">If your test environment is a user acceptance testing (UAT) or higher-tier sandbox environment that has no Remote Desktop access, the SOAP hostname is equal to the hostname.</span></span>

+ <span data-ttu-id="b23ab-165">**管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="b23ab-165">**Admin User Name** – The email address of an admin user in the test environment.</span></span> <span data-ttu-id="b23ab-166">管理者ユーザー名は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-166">The admin user name must be the email address of a user who belongs to the System Administrator role on the Finance and Operations test environment that RSAT is connecting to.</span></span> <span data-ttu-id="b23ab-167">また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-167">The user account (email address) must also belong to the same tenant as the test environment.</span></span> <span data-ttu-id="b23ab-168">たとえば、テスト環境の既定のテナントが contoso.com である場合、管理ユーザーは @constoso.com で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-168">For example, if your test environment's default tenant is contoso.com, the admin user must end with @constoso.com.</span></span>

+ <span data-ttu-id="b23ab-169">**拇印** – 使用している認証証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="b23ab-169">**Thumbprint** – The thumbprint of the authentication certificate that you're using.</span></span>
 <span data-ttu-id="b23ab-170">使用している環境にリモート デスクトップ プロトコル (RDP) でアクセスできない場合は、この記事で後述する手順に従って、Lifecycle Services から証明書をダウンロードし、拇印をここに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-170">If you don't have Remote Desktop Protocol (RDP) access to your environment, follow the steps lower in this article to download the certificate from Lifecycle Services and paste the thumbprint here.</span></span>
 <span data-ttu-id="b23ab-171">環境に RDP でアクセスできる場合は、次の手順に従って自己署名証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-171">Otherwise, if you do have RDP access to the environment, follow these steps to generate a self-signed certificate.</span></span>

    1. <span data-ttu-id="b23ab-172">新しい証明書を作成してインストールするには、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-172">Select **New** to create and install a new authentication certificate.</span></span> <span data-ttu-id="b23ab-173">プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-173">When prompted, place the .cer file somewhere so you have it saved for your records.</span></span>
    2. <span data-ttu-id="b23ab-174">プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート店舗にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-174">When the process completes, the new certification is installed in the local machine's trusted root store.</span></span>

        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. <span data-ttu-id="b23ab-176">新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-176">The thumbprint of the newly created certificate is automatically inserted on this form.</span></span> <span data-ttu-id="b23ab-177">この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-177">Copy this thumbprint, you will use it in the next section to configure the AOS to trust the connection.</span></span>

+ <span data-ttu-id="b23ab-178">**会社名** – Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-178">**Company name** – Specify a company name to use as your default company during creation of Excel parameters files.</span></span> <span data-ttu-id="b23ab-179">後でExcelファイルを編集して変更できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-179">It can be changed later by editing an Excel file.</span></span>

#### <a name="run-setting"></a><span data-ttu-id="b23ab-180">実行設定</span><span class="sxs-lookup"><span data-stu-id="b23ab-180">Run setting</span></span>

<span data-ttu-id="b23ab-181">ローカル設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-181">Configure your local settings.</span></span>

+ <span data-ttu-id="b23ab-182">**作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。</span><span class="sxs-lookup"><span data-stu-id="b23ab-182">**Working directory** - Folder location for storing test automation files, including Excel test data files.</span></span> <span data-ttu-id="b23ab-183">たとえば、 **C:\Temp\RegressionTool** のようになります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-183">For example: **C:\Temp\RegressionTool**.</span></span>
+ <span data-ttu-id="b23ab-184">**既定のブラウザー** - テストの実行に使用するブラウザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-184">**Default browser** - Select the browser to use for test execution.</span></span> <span data-ttu-id="b23ab-185">RSAT は (新しい) Microsoft Edge、Microsoft Internet Explorer、 および Google Chrome をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-185">RSAT supports (the new) Microsoft Edge, Microsoft Internet Explorer, and Google Chrome.</span></span> <span data-ttu-id="b23ab-186">[新しい Microsoft Edge の概要](https://www.microsoft.com/edge)から Microsoft Edge ダウンロードすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-186">We recommend Microsoft Edge, which you can download from [Introducing the new Microsoft Edge](https://www.microsoft.com/edge).</span></span>

<span data-ttu-id="b23ab-187">**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-187">Select **Ok** to apply your settings and close the dialog box.</span></span> <span data-ttu-id="b23ab-188">**キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-188">Select **Cancel** to cancel your changes and close the dialog.</span></span> <span data-ttu-id="b23ab-189">**名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-189">The **Save As** and **Open** buttons allow you to save your settings for reuse later.</span></span> <span data-ttu-id="b23ab-190">**名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-190">Select **Save As** to save your current settings into a configuration file on your computer.</span></span> <span data-ttu-id="b23ab-191">**開く** を選択して、構成ファイルから設定を復元します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-191">Select **Open** to restore your settings from a configuration file.</span></span>

### <a name="optional-settings"></a><span data-ttu-id="b23ab-192">オプション設定</span><span class="sxs-lookup"><span data-stu-id="b23ab-192">Optional settings</span></span>

<span data-ttu-id="b23ab-193">**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-193">Select the **Optional** tab to configure optional settings.</span></span>

+ <span data-ttu-id="b23ab-194">**テストの実行の接頭語** – RSATはテストの実行結果を Azure DevOps に報告します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-194">**Test Run Prefix** – RSAT reports test run results to Azure DevOps.</span></span> <span data-ttu-id="b23ab-195">テストの実行には、次の規則: **\<Run ID\> \<Prefix\> \<Test Suite\>** に従って名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-195">Test runs are named using the following convention: **\<Run ID\> \<Prefix\> \<Test Suite\>**.</span></span> <span data-ttu-id="b23ab-196">この設定を使用して **\<Prefix\>** を設定します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-196">Use this setting to set the **\<Prefix\>**.</span></span>
+ <span data-ttu-id="b23ab-197">**テストの実行タイムアウト** – テストの実行のタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="b23ab-197">**Test Run Timeout** – The time-out (in minutes) of a test run.</span></span> <span data-ttu-id="b23ab-198">このタイムアウトに達すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-198">All active windows are closed and pending test cases fail when this time-out is reached.</span></span>
+ <span data-ttu-id="b23ab-199">**テスト アクションのタイムアウト** – 個々のテスト ステップのタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="b23ab-199">**Test Action Timeout** – The time-out (in minutes) of individual test steps.</span></span> <span data-ttu-id="b23ab-200">テストステップがタイムアウトになると、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-200">When a test step times out, the test case fails.</span></span>
+ <span data-ttu-id="b23ab-201">**ステップ間の一時停止** – テストケースの自動実行中にテスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="b23ab-201">**Pause between steps** – The number of seconds to pause between test steps during automated execution of a test case.</span></span> <span data-ttu-id="b23ab-202">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-202">The default value is **0** (zero).</span></span> <span data-ttu-id="b23ab-203">監査または調査のために、テストの実行中に強制的に一時停止するには、この値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-203">Set this value to force a pause during test execution, for auditing or investigative purposes.</span></span> <span data-ttu-id="b23ab-204">テスト ケースの Excel パラメーター ファイルの **全般** タブにある、**ステップ間の一時停止 (秒)** パラメーターを変更することで、個々のテスト ケースに対して一時停止を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-204">You can also specify a pause for an individual test case by changing the **Pause between steps (Seconds)** parameter on the **General** tab of the Excel parameter file for the test case.</span></span>
+ <span data-ttu-id="b23ab-205">**最初の検証エラーでテストに失敗** – 既定では、テスト ケースに複数の検証ステップがあり、検証に失敗した場合は、最初の失敗が発生するとテスト ケースの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-205">**Fail test on first validation error** – By default, if a test case has multiple validation steps, and there is a validation failure, the test case stops running when the first failure occurs.</span></span> <span data-ttu-id="b23ab-206">テスト ケースは失敗としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-206">The test case is then marked as failed.</span></span> <span data-ttu-id="b23ab-207">すべての検証が完了するまでテスト ケースを実行する場合は、このオプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-207">If you want test cases to continue to run until all validations are completed, clear this option.</span></span> <span data-ttu-id="b23ab-208">その後、テスト ケースですべての検証を評価できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-208">The test case can then evaluate all validations.</span></span>
+ <span data-ttu-id="b23ab-209">**情報ログのエラーでテストに失敗** - このオプションをチェックし、テスト ケースの実行中に Finance and Operations 情報ログでエラーが発生した場合、テスト ケースが強制的に失敗するようにします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-209">**Fail test on Infolog error** - Check this option to force test cases to fail when an error is encountered in the Finance and Operations Infolog during test case execution.</span></span>
+ <span data-ttu-id="b23ab-210">**失敗時にテスト スイートの実行を中止する** – 既定では、テスト ケースのいずれかが失敗した場合でもテスト スイートの実行が続行されます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-210">**Abort test suite execution on failure** – By default, a test suite run continues even if one of the test cases fails.</span></span> <span data-ttu-id="b23ab-211">この設定をチェックすると、テスト ケースが失敗した場合にテストの実行が中止されます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-211">If you check this setting, the test run is aborted if a test case fails.</span></span> <span data-ttu-id="b23ab-212">残りのすべてのテスト ケースのステータスは **未実行** になります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-212">All the remaining test cases will have a status of **Not Executed**.</span></span>
+ <span data-ttu-id="b23ab-213">**ローカル ファイルの検証ルールを有効にする** - この設定をチェックして、テスト ケースの実行準備が整っているかどうかを検証します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-213">**Enable local file validation rules** - Check this setting to validate whether your test cases are ready for execution.</span></span> <span data-ttu-id="b23ab-214">詳細については、[テスト自動化ファイルの準備状況の検証](rsat-run.md#validate-readiness-of-test-automation-files) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-214">See [Validate readiness of test automation files](rsat-run.md#validate-readiness-of-test-automation-files) for more details.</span></span>
+ <span data-ttu-id="b23ab-215">**Azure DevOps へのアップロードを有効にする** - Azure DevOps へ偶発的にアップロードされる (したがってプロジェクト全体の記録と自動化ファイルが上書きされます) のを回避するために、この設定をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-215">**Enable upload to Azure DevOps** - To prevent accidental upload to Azure DevOps (therefore overriding project-wide recordings and automation files), you can uncheck this setting.</span></span> <span data-ttu-id="b23ab-216">これは、RSAT が実行目的でのみクライアント マシンに配置されていて、ユーザーがテスト ケースを永続的に変更することを回避したい場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-216">This is especially useful when RSAT is deployed on a client machine for execution purposes only, and you want to prevent users from making permanent changes to the test cases.</span></span>
+ <span data-ttu-id="b23ab-217">**クラウド プロバイダー** – テスト環境のクラウド テナントのプロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-217">**Cloud provider** – Select the provider of the cloud tenant of your test environment.</span></span> <span data-ttu-id="b23ab-218">サポートされているプロバイダーは、**グローバル** (パブリッククラウド) および **中国** (主権クラウド) です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-218">Supported providers are **Global** (Public cloud) and **China** (Sovereign cloud).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b23ab-219">Finance and Operations アプリが 21Vianet に配置されている場合、**クラウド プロバイダー** の設定が必要となり、選択された値は **中国** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-219">The **Cloud provider** setting is required, and the selected value must be **China** if your Finance and Operations apps were deployed in 21Vianet.</span></span>

### <a name="configure-the-test-environment-to-trust-the-connection"></a><span data-ttu-id="b23ab-220">接続を信頼するようにテスト環境を構成する</span><span class="sxs-lookup"><span data-stu-id="b23ab-220">Configure the test environment to trust the connection</span></span>

#### <a name="if-your-aos-allows-for-remote-desktop-connections"></a><span data-ttu-id="b23ab-221">AOS がリモート デスクトップ接続を許可している場合</span><span class="sxs-lookup"><span data-stu-id="b23ab-221">If your AOS allows for Remote Desktop connections</span></span>

<span data-ttu-id="b23ab-222">証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-222">After creating the certificate, configure AOS to trust the test automation connection.</span></span> <span data-ttu-id="b23ab-223">マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-223">On a multi-AOS environment, repeat the following steps for all AOS machines.</span></span>

1. <span data-ttu-id="b23ab-224">AOSマシンへのリモート デスクトップ接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-224">Open a Remote Desktop connection to the AOS machine.</span></span>
2. <span data-ttu-id="b23ab-225">IIS を開き、サイトの一覧で AOSService を見つけます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-225">Open IIS and find AOSService in the list of sites.</span></span>

    ![IISでのAOSの検索](media/configure-aos.png)

3. <span data-ttu-id="b23ab-227">**AOSService** を右クリックし、**エクスプローラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-227">Right-click **AOSService**, then select **Explore**.</span></span>
4. <span data-ttu-id="b23ab-228">ファイル **wif.config** を開き、検索します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-228">Open and find the file **wif.config**.</span></span>

    ![wif.config を開く](media/open-wif-config.png)

5. <span data-ttu-id="b23ab-230">次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-230">Update the **wif.config** file by adding a new authority entry, as shown in the following example.</span></span> <span data-ttu-id="b23ab-231">機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-231">Use **127.0.0.1** for the authority name and paste your certificate thumbprint.</span></span>

    ```xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry, Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="ccbc124d0a119xxxxxxxxxxxxxxxxxxxx841e797" />
            </keys>
                <validIssuers>
                    <add name="CN=127.0.0.1" />
                </validIssuers>
        </authority>
    ```

#### <a name="if-you-have-no-remote-desktop-access-to-the-server"></a><span data-ttu-id="b23ab-232">サーバーへのリモート デスクトップ アクセス権がない場合</span><span class="sxs-lookup"><span data-stu-id="b23ab-232">If you have no Remote Desktop access to the server</span></span>

<span data-ttu-id="b23ab-233">Microsoft が管理するサンドボックス、またはセルフ サービス タイプ サンドボックスなど、リモート デスクトップ プロトコル (RDP) アクセスが削除された場合、Microsoft は環境に応じた証明書を生成し、事前にコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-233">In cases where your Remote Desktop Protocol (RDP) access is removed, such as Microsoft-managed or self-service type sandboxes, Microsoft will generate the certificate for your environment and have it pre-configured.</span></span> <span data-ttu-id="b23ab-234">RSAT 証明書を取得して使用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b23ab-234">Follow these steps to retrieve the RSAT certificate and use it.</span></span>

1. <span data-ttu-id="b23ab-235">Lifecycle Services の環境詳細ページの **管理** の下に、2 つの新しいオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-235">Under **Maintain** on your environment details page in Lifecycle Services you'll see two new options.</span></span>

    - <span data-ttu-id="b23ab-236">RSAT 証明書のダウンロード</span><span class="sxs-lookup"><span data-stu-id="b23ab-236">Download RSAT certificate</span></span>
    - <span data-ttu-id="b23ab-237">RSAT 証明書を再生成する</span><span class="sxs-lookup"><span data-stu-id="b23ab-237">Regenerate RSAT certificate</span></span>

![RSAT 証明書のオプションのダウンロードと再生成](media/rsat-lcs1.png)

<span data-ttu-id="b23ab-239">**ダウンロード** ボタンを使用して、証明書バンドルを .zip ファイルとして取得します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-239">Use the **Download** button to retrieve the certificate bundle as a .zip file.</span></span>

2. <span data-ttu-id="b23ab-240">クリアテキスト パスワードが画面に表示されるという警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-240">You'll receive a warning that a clear-text password will be displayed on your screen.</span></span> <span data-ttu-id="b23ab-241">後の手順でパスワードが必要になります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-241">You will need the password in subsequent steps.</span></span>  <span data-ttu-id="b23ab-242">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-242">Select **Yes** to continue.</span></span>

3. <span data-ttu-id="b23ab-243">クリアテキスト パスワードを後で使用できるようにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-243">Copy the clear-text password for later use.</span></span> <span data-ttu-id="b23ab-244">.zip ファイルがダウンロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-244">You'll see the .zip file has been downloaded.</span></span> <span data-ttu-id="b23ab-245">.zip ファイルの内部には、証明書 (.cer) と個人情報交換 (.pfx) ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-245">Inside the .zip file is a certificate (.cer) and a personal information exchange (.pfx) file.</span></span> <span data-ttu-id="b23ab-246">ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-246">Unzip the file.</span></span>

4. <span data-ttu-id="b23ab-247">ローカル コンピューターの信頼されたルート ストアに証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-247">Install the certificate in the local machine's trusted root store:</span></span>
    + <span data-ttu-id="b23ab-248">証明書 (.cer) をダブルクリックして開き、**証明書のインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-248">Double-click the certificate (.cer) to open it, and then select **Install Certificate**.</span></span> 
    + <span data-ttu-id="b23ab-249">**ローカル コンピューター** を選択し、**信頼済ルート証明機関** ストアを参照して、信頼されたルート ストアにインストールします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-249">Select **local machine**, and then browse to the **Trusted Root Certification Authorities** store to install it in the trusted root store.</span></span>

5. <span data-ttu-id="b23ab-250">ローカル コンピューターの個人ストアに pfx ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-250">Install the pfx file in the local machine's personal store:</span></span>
   + <span data-ttu-id="b23ab-251">個人情報交換 (.pfx) ファイルをダブルクリックして開き、**ローカル コンピューター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-251">Double-click the personal information exchange (.pfx) file to open it, and select **Local Machine**.</span></span> 
   + <span data-ttu-id="b23ab-252">手順 2 で保存したパスワードを入力し、**個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-252">Enter the password saved in step 2, and browse to the **Personal** store.</span></span>

6. <span data-ttu-id="b23ab-253">証明書ファイルをダブルクリックして、開きます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-253">Double-click the certificate file to open it.</span></span> <span data-ttu-id="b23ab-254">**詳細** タブを参照し、**拇印** セクションが表示されるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-254">Browse to the **Details** tab, and scroll down until you see the **Thumbprint** section.</span></span> <span data-ttu-id="b23ab-255">**拇印** を選択し、テキスト ボックスの ID に注意します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-255">Select **Thumbprint**, and note the ID in the text box.</span></span> <span data-ttu-id="b23ab-256">この捺印を選択するか、RSAT 設定に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-256">Select or paste this thumbprint in RSAT settings.</span></span>
<span data-ttu-id="b23ab-257">![拇印の設定](media/rsat-lcs4.png)</span><span class="sxs-lookup"><span data-stu-id="b23ab-257">![Thumbprint settings](media/rsat-lcs4.png)</span></span>

<span data-ttu-id="b23ab-258">これで、この証明書を使用して環境に対してテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-258">You can now run your tests against the environment using this certificate.</span></span> <span data-ttu-id="b23ab-259">証明書は期限が切れる前に Microsoft によって自動的にローテーションされます。その後、上記の手順 1 からこの証明書の新しいバージョンをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-259">The certificate will be autorotated by Microsoft before it expires, at which time you will need to download a new version of this certificate starting from step 1 above.</span></span> <span data-ttu-id="b23ab-260">セルフ サービス環境では、有効期限に最も近いダウンタイム ウィンドウで 90 日ごとにローテーションされます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-260">For self-service environments, this will be rotated every 90 days during a downtime window that is closest to the expiry.</span></span> <span data-ttu-id="b23ab-261">これらのダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-261">These downtime windows include customer initiated package deployment, and database movement operations that target the environment.</span></span>

## <a name="manual-configuration-of-authentication-certificates"></a><span data-ttu-id="b23ab-262">認証証明書の手動構成</span><span class="sxs-lookup"><span data-stu-id="b23ab-262">Manual configuration of authentication certificates</span></span>

<span data-ttu-id="b23ab-263">必要に応じて、RSAT認証証明書を手動で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-263">Optionally, you can manually configure the RSAT authentication certificate.</span></span>

<span data-ttu-id="b23ab-264">このプロセスに精通していない場合は、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-264">If you are not familiar with this process, get help from your system administrator.</span></span> <span data-ttu-id="b23ab-265">Windows キットがコンピューターにインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b23ab-265">Make sure you have Windows Kits installed on your machine.</span></span> <span data-ttu-id="b23ab-266">Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-266">If you do not have Windows Kits installed on your machine, you can download the Windows 10 SDK from [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> <span data-ttu-id="b23ab-267">このドキュメントで説明されている手順には、これらのコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="b23ab-267">You will need these components for the steps described in this document.</span></span>

+ <span data-ttu-id="b23ab-268">デスクトップ アプリ用の Windows SDK 署名ツール</span><span class="sxs-lookup"><span data-stu-id="b23ab-268">Windows SDK Signing Tools for Desktop Apps</span></span>
+ <span data-ttu-id="b23ab-269">UWP マネージド アプリ用の Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="b23ab-269">Windows SDK for UWP-Managed Apps.</span></span>

### <a name="generate-the-certificate"></a><span data-ttu-id="b23ab-270">証明書を生成する</span><span class="sxs-lookup"><span data-stu-id="b23ab-270">Generate the certificate</span></span>

<span data-ttu-id="b23ab-271">RSAT クライアント コンピュータで証明書ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-271">You must generate the certificate file on the RSAT client computer.</span></span> <span data-ttu-id="b23ab-272">**証明書は、テスト ツールを実行している同じコンピュータで生成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="b23ab-272">**The certificate must be generated on the same computer that the test tool is running on.**</span></span> <span data-ttu-id="b23ab-273">証明書ファイルを生成するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="b23ab-273">To generate the certificate file, follow these steps:</span></span>

1. <span data-ttu-id="b23ab-274">コンピューター上にまだ存在しない場合は、 **C:\Temp** フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-274">Create the **C:\Temp** folder if it does not already exist on your computer.</span></span>
2. <span data-ttu-id="b23ab-275">管理者としてコマンド ライン ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-275">Open a command-line window as Administrator.</span></span>
3. <span data-ttu-id="b23ab-276">Windows SDKをインストールしたフォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-276">Go to the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="b23ab-277">正確なフォルダは、Windows SDKをインストールした場所によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-277">Your exact folder may be different, depending on where you have installed the windows SDK).</span></span> <span data-ttu-id="b23ab-278">Windows キット 8.1を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b23ab-278">You can also use Windows Kits 8.1.</span></span>

    ```Console
    cd c:\Program Files (x86)\Windows Kits\10\bin\10.0.17763.0\x64
    ```

4. <span data-ttu-id="b23ab-279">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-279">Run the following command.</span></span> <span data-ttu-id="b23ab-280">秘密キー パスワードを要求するプロンプトが表示されたら、 **なし** を入力します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-280">When you are prompted to enter a private key password, enter **None**.</span></span>

    ```Console
    makecert.exe -n "CN=127.0.0.1" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 c:\temp\authCert.cer
    ````

### <a name="install-the-certificate-to-the-trusted-root"></a><span data-ttu-id="b23ab-281">信頼済ルートに証明書をインストールする</span><span class="sxs-lookup"><span data-stu-id="b23ab-281">Install the certificate to the Trusted Root</span></span>

<span data-ttu-id="b23ab-282">証明書をインストールするには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="b23ab-282">To install the certificate, follow these steps:</span></span>

1. <span data-ttu-id="b23ab-283">証明書をインストールするには、 **authCert.cer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-283">Double-click **authCert.cer** to install the certificate.</span></span>
2. <span data-ttu-id="b23ab-284">**証明書のインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-284">Select **Install Certificate**.</span></span>
3. <span data-ttu-id="b23ab-285">**ローカル コンピューター > 次の店舗で証明書を確定 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-285">Select **Local Machine > Place all certificates in the following Store > Browse > Trusted Root Certification Authorities** and select **Next** through each screen.</span></span>
4. <span data-ttu-id="b23ab-286">**パスワード** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b23ab-286">Leave the **Password** field blank.</span></span>
5. <span data-ttu-id="b23ab-287">**証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-287">In the **Certificate** dialog box, browse to **Details** and look for **Thumbprint**.</span></span>

    ![拇印の一覧を示す証明書ダイアログ](media/certificate-dialog.png)

6. <span data-ttu-id="b23ab-289">拇印をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="b23ab-289">Copy and save the thumbprint.</span></span> <span data-ttu-id="b23ab-290">このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b23ab-290">You will need it to configure the AOS as described earlier in this topic.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]