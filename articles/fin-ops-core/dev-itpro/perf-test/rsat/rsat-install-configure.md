---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 06/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6023715997e01c1eb9e316655514213558d4af75
ms.sourcegitcommit: 792a81ae86d4854e450c3c5006d2523dd721d522
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2020
ms.locfileid: "4723421"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a><span data-ttu-id="88de5-103">Regression Suite Automation Tool のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="88de5-103">Regression Suite Automation Tool installation and configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88de5-104">このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88de5-104">This topic contains information about how install and configure the Regression suite automation tool (RSAT).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88de5-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="88de5-105">Prerequisites</span></span>

### <a name="test-environment"></a><span data-ttu-id="88de5-106">テスト環境</span><span class="sxs-lookup"><span data-stu-id="88de5-106">Test environment</span></span>
<span data-ttu-id="88de5-107">テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-107">Your test environment must be running Platform update 15 or newer.</span></span> <span data-ttu-id="88de5-108">Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-108">The Regression suite automation tool must have access to your test environment via a web browser.</span></span>  

### <a name="excel"></a><span data-ttu-id="88de5-109">Excel</span><span class="sxs-lookup"><span data-stu-id="88de5-109">Excel</span></span>
<span data-ttu-id="88de5-110">テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-110">You need Microsoft Excel installed to generate and edit test parameters.</span></span> 

### <a name="azure-devops"></a><span data-ttu-id="88de5-111">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="88de5-111">Azure DevOps</span></span>
<span data-ttu-id="88de5-112">テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="88de5-112">You must have an Azure DevOps project to store and manage your test cases, test plans, and test case results.</span></span> <span data-ttu-id="88de5-113">Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="88de5-113">You will need an Azure DevOps Test Manager or Test Plans license.</span></span> <span data-ttu-id="88de5-114">たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。</span><span class="sxs-lookup"><span data-stu-id="88de5-114">For example, if you have a Visual Studio Enterprise subscription, you already have a license to Test Plans.</span></span> <span data-ttu-id="88de5-115">詳細については、[Azure DevOps サービス](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) の価格設定、または [Azure DevOps サーバーの価格設定](https://azure.microsoft.com/pricing/details/devops/server/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-115">For more information, see [Pricing for Azure DevOps Services](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) or [Pricing for Azure DevOps Server](https://azure.microsoft.com/pricing/details/devops/server/).</span></span>

### <a name="authentication-certificate"></a><span data-ttu-id="88de5-116">認証証明書</span><span class="sxs-lookup"><span data-stu-id="88de5-116">Authentication Certificate</span></span>
<span data-ttu-id="88de5-117">RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザーを介して環境にリモート接続するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="88de5-117">RSAT is designed to be installed on any Windows 10 computer and connect remotely via a web browser to an environment.</span></span>

![クライアント コンピュータと環境](media/client-environment.png)

<span data-ttu-id="88de5-119">セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-119">To enable secure authentication, RSAT requires a certificate to be installed on the RSAT client computer.</span></span> <span data-ttu-id="88de5-120">RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。</span><span class="sxs-lookup"><span data-stu-id="88de5-120">The RSAT settings dialog box allows you to automatically create and install the authentication certificate.</span></span> <span data-ttu-id="88de5-121">また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-121">You will also need to configure the virtual machine (VM) to trust the connection.</span></span> <span data-ttu-id="88de5-122">RSATをインストールして構成するには、次のセクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="88de5-122">Follow the instructions in the next sections to install and configure RSAT.</span></span>

## <a name="installation"></a><span data-ttu-id="88de5-123">インストール</span><span class="sxs-lookup"><span data-stu-id="88de5-123">Installation</span></span>

### <a name="installer"></a><span data-ttu-id="88de5-124"> インストーラー</span><span class="sxs-lookup"><span data-stu-id="88de5-124">Installer</span></span>
<span data-ttu-id="88de5-125">[Regression Suite Automation Tool ダウンロード](https://www.microsoft.com/download/details.aspx?id=57357) からマシンに .msi ファイルをダウンロードし、ダブルクリックしてインストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="88de5-125">Download the .msi file from the [Regression Suite Automation Tool Download](https://www.microsoft.com/download/details.aspx?id=57357) to your machine and double-click it to run the installer.</span></span> 

> [!NOTE]
> <span data-ttu-id="88de5-126">Azure DevOps サーバーを使用している場合は、バージョン 1.210.48249.4 以降をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="88de5-126">If you're using Azure DevOps Server, download and install version 1.210.48249.4 or later.</span></span> 
 
### <a name="selenium-and-browser-drivers"></a><span data-ttu-id="88de5-127">Selenium およびブラウザー ドライバー</span><span class="sxs-lookup"><span data-stu-id="88de5-127">Selenium and Browser Drivers</span></span>
<span data-ttu-id="88de5-128">RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。</span><span class="sxs-lookup"><span data-stu-id="88de5-128">RSAT requires Selenium and web browser driver libraries.</span></span> <span data-ttu-id="88de5-129">RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="88de5-129">RSAT will prompt you if needed libraries are missing and will automatically install them for you.</span></span> <span data-ttu-id="88de5-130">次の (または類似の) メッセージが表示されたら、はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-130">Select Yes when you see the following (or similar) messages.</span></span>
 
![Selenium ドライバー](media/driver-1.png)
 
![ブラウザー ドライバー](media/driver-2.png)

<span data-ttu-id="88de5-133">または、 [Selenium ドライバーのインストール](#install-selenium-drivers) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-133">Alternatively, refer to [Install Selenium Driver](#install-selenium-drivers).</span></span>

## <a name="configuration"></a><span data-ttu-id="88de5-134">構成</span><span class="sxs-lookup"><span data-stu-id="88de5-134">Configuration</span></span>

<span data-ttu-id="88de5-135">デスクトップから RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="88de5-135">Open RSAT from your desktop.</span></span>

![RSAT デスクトップ アイコン](media/desktop-icon.png)
 
<span data-ttu-id="88de5-137">RSATを構成するには、右上の **設定** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-137">Select **Settings** button in the upper right to configure RSAT.</span></span>

![RSAT 設定](media/rsat-settings.png)

### <a name="general-settings"></a><span data-ttu-id="88de5-139">一般設定</span><span class="sxs-lookup"><span data-stu-id="88de5-139">General settings</span></span>
<span data-ttu-id="88de5-140">これらの設定は必須です。</span><span class="sxs-lookup"><span data-stu-id="88de5-140">These settings are required.</span></span>

#### <a name="azure-devops"></a><span data-ttu-id="88de5-141">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="88de5-141">Azure DevOps</span></span>
<span data-ttu-id="88de5-142">Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-142">Configure your connection to the Azure DevOps project and test plan.</span></span>

+ <span data-ttu-id="88de5-143">**Azure DevOps URL** - これは、 Azure DevOps 組織の URL です。</span><span class="sxs-lookup"><span data-stu-id="88de5-143">**Azure DevOps URL** - This is the URL of your Azure DevOps organization.</span></span> <span data-ttu-id="88de5-144">たとえば、`https://yourAzureDevOpsUrlHere.visualStudio.com`。</span><span class="sxs-lookup"><span data-stu-id="88de5-144">For example, `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88de5-145">Azure DevOps サーバーを使用している場合は、**/DefaultCollection** を Azure DevOps URL の末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="88de5-145">If you're using Azure DevOps Server, add **/DefaultCollection** to the end of your Azure DevOps URL.</span></span>

+ <span data-ttu-id="88de5-146">**アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。</span><span class="sxs-lookup"><span data-stu-id="88de5-146">**Access Token** - The access token that allows the tool to connect to Azure DevOps.</span></span> <span data-ttu-id="88de5-147">個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-147">You need to create a personal access token or use an existing one that you have saved.</span></span> <span data-ttu-id="88de5-148">詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-148">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span> 
+ <span data-ttu-id="88de5-149">**プロジェクト名** - Azure DevOps プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="88de5-149">**Project Name** - The name of your Azure DevOps project.</span></span> <span data-ttu-id="88de5-150">RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。</span><span class="sxs-lookup"><span data-stu-id="88de5-150">RSAT will automatically detect project names and test plans available based the Azure DevOps URL specified.</span></span> <span data-ttu-id="88de5-151">その後、テスト プロジェクトおよびテスト計画を選択できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-151">You can then select the Test Project and Test Plan.</span></span>
+ <span data-ttu-id="88de5-152">**テスト計画** - テスト ケースを含む Azure DevOps テスト計画</span><span class="sxs-lookup"><span data-stu-id="88de5-152">**Test Plan** - The Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="88de5-153">詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-153">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> 

<span data-ttu-id="88de5-154">**接続のテスト** を選択し、 Azure DevOps への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="88de5-154">Select **Test Connection** to test your connection to Azure DevOps.</span></span>

#### <a name="test-environment"></a><span data-ttu-id="88de5-155">テスト環境</span><span class="sxs-lookup"><span data-stu-id="88de5-155">Test environment</span></span>
<span data-ttu-id="88de5-156">テスト環境への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-156">Configure your connection to the test environment.</span></span>

+ <span data-ttu-id="88de5-157">**ホスト名** – myhost.cloudax.dynamics.com. などのテスト環境のホスト名。</span><span class="sxs-lookup"><span data-stu-id="88de5-157">**Hostname** – The hostname of the test environment, such as myhost.cloudax.dynamics.com.</span></span> <span data-ttu-id="88de5-158">https:// または http:// の接頭語を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="88de5-158">Don't include the https:// or http:// prefix.</span></span>
+ <span data-ttu-id="88de5-159">**SOAP ホスト名** – テスト環境の SOAP ホスト名。</span><span class="sxs-lookup"><span data-stu-id="88de5-159">**SOAP Hostname** – The SOAP hostname of the test environment.</span></span> <span data-ttu-id="88de5-160">通常は、ホスト名に **soap** の接尾語を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-160">Typically, you must add a **soap** suffix to the hostname.</span></span> <span data-ttu-id="88de5-161">たとえば、ホスト名が myhost.cloudax.dynamics.com の場合は、myhost **soap**.cloudax.dynamics.com を SOAP ホスト名として使用します。</span><span class="sxs-lookup"><span data-stu-id="88de5-161">For example, if your hostname is myhost.cloudax.dynamics.com, use myhost **soap**.cloudax.dynamics.com as the SOAP hostname.</span></span>

    + <span data-ttu-id="88de5-162">テスト環境の SOAP ホスト名がわからない場合は、Infrastructure.SoapServicesUrl の AOS サーバーの web.config ファイルで検索できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-162">If you don't know the SOAP hostname of your test environment, you can find it in the web.config file for the AOS server in Infrastructure.SoapServicesUrl.</span></span>
    + <span data-ttu-id="88de5-163">テスト環境が、リモート デスクトップ アクセスがないユーザー受け入れテスト (user acceptance testing: UAT) または上位層サンドボックス環境である場合、この SOAP ホスト名はホスト名に一致します。</span><span class="sxs-lookup"><span data-stu-id="88de5-163">If your test environment is a user acceptance testing (UAT) or higher-tier sandbox environment that has no Remote Desktop access, the SOAP hostname matches the hostname.</span></span>

+ <span data-ttu-id="88de5-164">**管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="88de5-164">**Admin User Name** – The email address of an admin user in the test environment.</span></span> <span data-ttu-id="88de5-165">管理者ユーザー名は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-165">The admin user name must be the email address of a user who belongs to the System Administrator role on the Finance and Operations test environment that RSAT is connecting to.</span></span> <span data-ttu-id="88de5-166">また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-166">The user account (email address) must also belong to the same tenant as the test environment.</span></span> <span data-ttu-id="88de5-167">たとえば、テスト環境の既定のテナントが contoso.com である場合、管理ユーザーは @constoso.com で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-167">For example, if your test environment's default tenant is contoso.com, the admin user must end with @constoso.com.</span></span>

+ <span data-ttu-id="88de5-168">**拇印** – 使用している認証証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="88de5-168">**Thumbprint** – The thumbprint of the authentication certificate that you're using.</span></span>
 <span data-ttu-id="88de5-169">使用している環境にリモート デスクトップ プロトコル (RDP) でアクセスできない場合は、この記事で後述する手順に従って、Lifecycle Services から証明書をダウンロードし、拇印をここに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="88de5-169">If you don't have Remote Desktop Protocol (RDP) access to your environment, follow the steps lower in this article to download the certificate from Lifecycle Services and paste the thumbprint here.</span></span>
 <span data-ttu-id="88de5-170">環境に RDP でアクセスできる場合は、次の手順に従って自己署名証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="88de5-170">Otherwise, if you do have RDP access to the environment, follow these steps to generate a self-signed certificate.</span></span> 

    1. <span data-ttu-id="88de5-171">新しい証明書を作成してインストールするには、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-171">Select **New** to create and install a new authentication certificate.</span></span> <span data-ttu-id="88de5-172">プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。</span><span class="sxs-lookup"><span data-stu-id="88de5-172">When prompted, place the .cer file somewhere so you have it saved for your records.</span></span>
    2. <span data-ttu-id="88de5-173">プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート店舗にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="88de5-173">When the process completes, the new certification is installed in the local machine's trusted root store.</span></span>

        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. <span data-ttu-id="88de5-175">新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-175">The thumbprint of the newly created certificate is automatically inserted on this form.</span></span> <span data-ttu-id="88de5-176">この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-176">Copy this thumbprint, you will use it in the next section to configure the AOS to trust the connection.</span></span>

+ <span data-ttu-id="88de5-177">**会社名** – Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。</span><span class="sxs-lookup"><span data-stu-id="88de5-177">**Company name** – Specify a company name to use as your default company during creation of Excel parameters files.</span></span> <span data-ttu-id="88de5-178">後でExcelファイルを編集して変更できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-178">It can be changed later by editing an Excel file.</span></span>


#### <a name="run-setting"></a><span data-ttu-id="88de5-179">実行設定</span><span class="sxs-lookup"><span data-stu-id="88de5-179">Run setting</span></span>
<span data-ttu-id="88de5-180">ローカル設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-180">Configure your local settings.</span></span>

+ <span data-ttu-id="88de5-181">**作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。</span><span class="sxs-lookup"><span data-stu-id="88de5-181">**Working directory** - Folder location for storing test automation files, including Excel test data files.</span></span> <span data-ttu-id="88de5-182">たとえば、 **C:\Temp\RegressionTool** のようになります。</span><span class="sxs-lookup"><span data-stu-id="88de5-182">For example: **C:\Temp\RegressionTool**.</span></span>
+ <span data-ttu-id="88de5-183">**既定のブラウザー** - テストの実行に使用するブラウザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-183">**Default browser** - Select the browser to use for test execution.</span></span> <span data-ttu-id="88de5-184">RSAT は (新しい) Microsoft Edge、Microsoft Internet Explorer および Google Chrome をサポートします。</span><span class="sxs-lookup"><span data-stu-id="88de5-184">RSAT supports (the new) Microsoft Edge, Microsoft Internet Explorer and Google Chrome.</span></span> <span data-ttu-id="88de5-185">[新しい Microsoft Edge の概要](https://www.microsoft.com/edge)から Microsoft Edge ダウンロードすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88de5-185">We recommend Microsoft Edge, which you can download from [Introducing the new Microsoft Edge](https://www.microsoft.com/edge).</span></span> 

<span data-ttu-id="88de5-186">**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88de5-186">Select **Ok** to apply your settings and close the dialog box.</span></span> <span data-ttu-id="88de5-187">**キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88de5-187">Select **Cancel** to cancel your changes and close the dialog.</span></span> <span data-ttu-id="88de5-188">**名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-188">The **Save As** and **Open** buttons allow you to save your settings for reuse later.</span></span> <span data-ttu-id="88de5-189">**名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="88de5-189">Select **Save As** to save your current settings into a configuration file on your computer.</span></span> <span data-ttu-id="88de5-190">**開く** を選択して、構成ファイルから設定を復元します。</span><span class="sxs-lookup"><span data-stu-id="88de5-190">Select **Open** to restore your settings from a configuration file.</span></span>

### <a name="optional-settings"></a><span data-ttu-id="88de5-191">オプション設定</span><span class="sxs-lookup"><span data-stu-id="88de5-191">Optional settings</span></span>
<span data-ttu-id="88de5-192">**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-192">Select the **Optional** tab to configure optional settings.</span></span>

+ <span data-ttu-id="88de5-193">**テストの実行の接頭語** – RSATはテストの実行結果を Azure DevOps に報告します。</span><span class="sxs-lookup"><span data-stu-id="88de5-193">**Test Run Prefix** – RSAT reports test run results to Azure DevOps.</span></span> <span data-ttu-id="88de5-194">テストの実行には、次の規則: **\<Run ID\> \<Prefix\> \<Test Suite\>** に従って名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="88de5-194">Test runs are named using the following convention: **\<Run ID\> \<Prefix\> \<Test Suite\>**.</span></span> <span data-ttu-id="88de5-195">この設定を使用して **\<Prefix\>** を設定します。</span><span class="sxs-lookup"><span data-stu-id="88de5-195">Use this setting to set the **\<Prefix\>**.</span></span>
+ <span data-ttu-id="88de5-196">**テストの実行タイムアウト** – テストの実行のタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="88de5-196">**Test Run Timeout** – The time-out (in minutes) of a test run.</span></span> <span data-ttu-id="88de5-197">このタイムアウトに達すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="88de5-197">All active windows are closed and pending test cases fail when this time-out is reached.</span></span>
+ <span data-ttu-id="88de5-198">**テスト アクションのタイムアウト** – 個々のテスト ステップのタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="88de5-198">**Test Action Timeout** – The time-out (in minutes) of individual test steps.</span></span> <span data-ttu-id="88de5-199">テストステップがタイムアウトになると、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="88de5-199">When a test step times out, the test case fails.</span></span>
+ <span data-ttu-id="88de5-200">**ステップ間の一時停止** – テストケースの自動実行中にテスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="88de5-200">**Pause between steps** – The number of seconds to pause between test steps during automated execution of a test case.</span></span> <span data-ttu-id="88de5-201">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="88de5-201">The default value is **0** (zero).</span></span> <span data-ttu-id="88de5-202">監査または調査のために、テストの実行中に強制的に一時停止するには、この値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88de5-202">Set this value to force a pause during test execution, for auditing or investigative purposes.</span></span> <span data-ttu-id="88de5-203">テスト ケースの Excel パラメーター ファイルの **全般** タブにある、**ステップ間の一時停止 (秒)** パラメーターを変更することで、個々のテスト ケースに対して一時停止を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="88de5-203">You can also specify a pause for an individual test case by changing the **Pause between steps (Seconds)** parameter on the **General** tab of the Excel parameter file for the test case.</span></span>
+ <span data-ttu-id="88de5-204">**最初の検証エラーでテストに失敗** – 既定では、テスト ケースに複数の検証ステップがあり、検証に失敗した場合は、最初の失敗が発生するとテスト ケースの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="88de5-204">**Fail test on first validation error** – By default, if a test case has multiple validation steps, and there is a validation failure, the test case stops running when the first failure occurs.</span></span> <span data-ttu-id="88de5-205">テスト ケースは失敗としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="88de5-205">The test case is then marked as failed.</span></span> <span data-ttu-id="88de5-206">すべての検証が完了するまでテスト ケースを実行する場合は、このオプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="88de5-206">If you want test cases to continue to run until all validations are completed, clear this option.</span></span> <span data-ttu-id="88de5-207">その後、テスト ケースですべての検証を評価できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-207">The test case can then evaluate all validations.</span></span>
+ <span data-ttu-id="88de5-208">**失敗時にテスト スイートの実行を中止する** – 既定では、いずれかのテスト ケースが失敗した場合でもテスト スイートの実行が続行されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-208">**Abort test suite execution on failure** – By default, execution of a test suite continues even if one of the test cases fails.</span></span> <span data-ttu-id="88de5-209">このオプションを **True** に設定すると、テスト ケースが失敗した場合にテストの実行が中止されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-209">If you set this option to **True**, the test run is aborted if a test case fails.</span></span> <span data-ttu-id="88de5-210">残りのすべてのテスト ケースのステータスは **未実行** になります。</span><span class="sxs-lookup"><span data-stu-id="88de5-210">All the remaining test cases will have a status of **Not Executed**.</span></span>
+ <span data-ttu-id="88de5-211">**クラウド プロバイダー** – テスト環境のクラウド テナントのプロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-211">**Cloud provider** – Select the provider of the cloud tenant of your test environment.</span></span> <span data-ttu-id="88de5-212">サポートされているプロバイダーは、**グローバル** (パブリッククラウド) および **中国** (主権クラウド) です。</span><span class="sxs-lookup"><span data-stu-id="88de5-212">Supported providers are **Global** (Public cloud) and **China** (Sovereign cloud).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="88de5-213">Finance and Operations アプリが 21Vianet に配置されている場合、**クラウド プロバイダー** の設定が必要となり、選択された値は **中国** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-213">The **Cloud provider** setting is required, and the selected value must be **China** if your Finance and Operations apps were deployed in 21Vianet.</span></span>
+ <span data-ttu-id="88de5-214">**Retail POS のコンフィギュレーション** - Microsoft Dynamics 365 Commerce の一部であるクラウド POS の自動テストのために RSAT をコンフィギュレーションするには、このボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-214">**Configure Retail POS** - Select this box to configure RSAT for automated testing of cloud POS, part of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="88de5-215">有効にすると、**設定** ダイアログ メニューに **Retail POS** という名前のタブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-215">Once enabled, a tab named **Retail POS** appears on the **Settings** dialog menu.</span></span> <span data-ttu-id="88de5-216">RSAT とクラウド POS の詳細については、[クラウド POS 用のレコーダーおよび Regression Suite Automation Tool のテスト](../../../../commerce/dev-itpro/pos-rsat.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-216">For more information about RSAT with cloud POS, see [Test recorder and Regression suite automation tool for Cloud POS](../../../../commerce/dev-itpro/pos-rsat.md).</span></span>

### <a name="configure-the-test-environment-to-trust-the-connection"></a><span data-ttu-id="88de5-217">接続を信頼するようにテスト環境を構成する</span><span class="sxs-lookup"><span data-stu-id="88de5-217">Configure the test environment to trust the connection</span></span>

#### <a name="if-your-aos-allows-for-remote-desktop-connections"></a><span data-ttu-id="88de5-218">AOS がリモート デスクトップ接続を許可している場合</span><span class="sxs-lookup"><span data-stu-id="88de5-218">If your AOS allows for Remote Desktop connections</span></span>

<span data-ttu-id="88de5-219">証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-219">After creating the certificate, configure AOS to trust the test automation connection.</span></span> <span data-ttu-id="88de5-220">マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="88de5-220">On a multi-AOS environment, repeat the following steps for all AOS machines.</span></span>

1.  <span data-ttu-id="88de5-221">AOSマシンへのリモート デスクトップ接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="88de5-221">Open a Remote Desktop connection to the AOS machine.</span></span>
2.  <span data-ttu-id="88de5-222">IIS を開き、サイトの一覧で AOSService を見つけます。</span><span class="sxs-lookup"><span data-stu-id="88de5-222">Open IIS and find AOSService in the list of sites.</span></span>

    ![IISでのAOSの検索](media/configure-aos.png)

3.  <span data-ttu-id="88de5-224">**AOSservice** を右クリックし、 **エクスプローラー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-224">Right-click **AOSService**, then click **Explore**.</span></span>
4.  <span data-ttu-id="88de5-225">ファイル **wif.config** を開き、検索します。</span><span class="sxs-lookup"><span data-stu-id="88de5-225">Open and find the file **wif.config**.</span></span>
  
    ![wif.config を開く](media/open-wif-config.png)

5.  <span data-ttu-id="88de5-227">次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="88de5-227">Update the **wif.config** file by adding a new authority entry, as shown in the following example.</span></span> <span data-ttu-id="88de5-228">機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="88de5-228">Use **127.0.0.1** for the authority name and paste your certificate thumbprint.</span></span>

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

#### <a name="if-you-have-no-remote-desktop-access-to-the-server"></a><span data-ttu-id="88de5-229">サーバーへのリモート デスクトップ アクセス権がない場合</span><span class="sxs-lookup"><span data-stu-id="88de5-229">If you have no Remote Desktop access to the server</span></span>

<span data-ttu-id="88de5-230">Microsoft が管理するサンドボックス、またはセルフ サービス タイプ サンドボックスなど、リモート デスクトップ プロトコル (RDP) アクセスが削除された場合、Microsoft は環境に応じた証明書を生成し、事前にコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="88de5-230">In cases where your Remote Desktop Protocol (RDP) access is removed, such as Microsoft-managed or self-service type sandboxes, Microsoft will generate the certificate for your environment and have it pre-configured.</span></span> <span data-ttu-id="88de5-231">RSAT 証明書を取得して使用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88de5-231">Follow these steps to retrieve the RSAT certificate and use it.</span></span>

1. <span data-ttu-id="88de5-232">Lifecycle Services の環境詳細ページの **管理** の下に、2 つの新しいオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-232">Under **Maintain** on your environment details page in Lifecycle Services you'll see two new options.</span></span>
  - <span data-ttu-id="88de5-233">RSAT 証明書のダウンロード</span><span class="sxs-lookup"><span data-stu-id="88de5-233">Download RSAT certificate</span></span>
  - <span data-ttu-id="88de5-234">RSAT 証明書を再生成する</span><span class="sxs-lookup"><span data-stu-id="88de5-234">Regenerate RSAT certificate</span></span>

![RSAT 証明書のオプションのダウンロードと再生成](media/rsat-lcs1.png)

<span data-ttu-id="88de5-236">**ダウンロード** ボタンを使用して、証明書バンドルを .zip ファイルとして取得します。</span><span class="sxs-lookup"><span data-stu-id="88de5-236">Use the **Download** button to retrieve the certificate bundle as a .zip file.</span></span>

2. <span data-ttu-id="88de5-237">クリアテキスト パスワードが画面に表示されるという警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88de5-237">You'll receive a warning that a clear-text password will be displayed on your screen.</span></span> <span data-ttu-id="88de5-238">このパスワードは、後の手順で必要となるため、メモしておきます。</span><span class="sxs-lookup"><span data-stu-id="88de5-238">Be sure to write this password down as you will need it in subsequent steps.</span></span>  <span data-ttu-id="88de5-239">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="88de5-239">Select **Yes** to continue.</span></span>

3. <span data-ttu-id="88de5-240">クリアテキスト パスワードを後で使用できるようにコピーします。</span><span class="sxs-lookup"><span data-stu-id="88de5-240">Copy the clear-text password for later use.</span></span> <span data-ttu-id="88de5-241">.zip ファイルがダウンロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88de5-241">You'll see the .zip file has been downloaded.</span></span> <span data-ttu-id="88de5-242">.zip ファイルの内部には、証明書 (.cer) と個人情報交換 (.pfx) ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="88de5-242">Inside the .zip file is a certificate (.cer) and a personal information exchange (.pfx) file.</span></span> <span data-ttu-id="88de5-243">ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="88de5-243">Unzip the file.</span></span>

4. <span data-ttu-id="88de5-244">証明書をダブルクリックして開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-244">Double-click the certificate to open it, and then select **Install**.</span></span> <span data-ttu-id="88de5-245">この証明書をローカル コンピューターにインストールしてから、**個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="88de5-245">Install this certificate to your local machine, and then browse to the **Personal** store.</span></span> <span data-ttu-id="88de5-246">ローカル コンピューターに対してこの手順を繰り返し、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="88de5-246">Repeat this process for the local machine, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>

5. <span data-ttu-id="88de5-247">個人情報交換 (.pfx) ファイルをダブルクリックして開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88de5-247">Double-click the personal information exchange (.pfx) file to open it, and select **Install**.</span></span> <span data-ttu-id="88de5-248">この証明書をローカル コンピューターにインストールしてから、手順 2 で保存したパスワードを入力して **個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="88de5-248">Install this certificate to your local machine, enter the password saved in step 2, and browse to the **Personal** store.</span></span> <span data-ttu-id="88de5-249">ローカル コンピューターの場所に対してこの手順を繰り返し、手順 2 で保存したパスワードを入力して、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="88de5-249">Repeat this process for the local machine location, enter the password saved in step 2, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>

6. <span data-ttu-id="88de5-250">証明書ファイルをダブルクリックして、開きます。</span><span class="sxs-lookup"><span data-stu-id="88de5-250">Double-click the certificate file to open it.</span></span> <span data-ttu-id="88de5-251">**詳細** タブを参照し、**拇印** セクションが表示されるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="88de5-251">Browse to the **Details** tab, and scroll down until you see the **Thumbprint** section.</span></span> <span data-ttu-id="88de5-252">**拇印** を選択し、テキスト ボックスに ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="88de5-252">Select **Thumbprint**, and copy the ID in the text box.</span></span> <span data-ttu-id="88de5-253">この拇印を RSAT に使用します。</span><span class="sxs-lookup"><span data-stu-id="88de5-253">Use this thumbprint for RSAT.</span></span>
<span data-ttu-id="88de5-254">![拇印の設定](media/rsat-lcs4.png)</span><span class="sxs-lookup"><span data-stu-id="88de5-254">![Thumbprint settings](media/rsat-lcs4.png)</span></span>

<span data-ttu-id="88de5-255">これで、この証明書を使用して環境に対してテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88de5-255">You can now run your tests against the environment using this certificate.</span></span> <span data-ttu-id="88de5-256">証明書は期限が切れる前に Microsoft によって自動的にローテーションされます。その後、上記の手順 1 からこの証明書の新しいバージョンをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-256">The certificate will be auto-rotated by Microsoft before it expires, at which time you will need to download a new version of this certificate starting from step 1 above.</span></span> <span data-ttu-id="88de5-257">セルフ サービス環境では、有効期限に最も近いダウンタイム ウィンドウで 90 日ごとにローテーションされます。</span><span class="sxs-lookup"><span data-stu-id="88de5-257">For self-service environments this will be rotated every 90 days during a downtime window that is closest to the expiry.</span></span> <span data-ttu-id="88de5-258">これらのダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="88de5-258">These downtime windows include customer initiated package deployment, and database movement operations that target the environment.</span></span>

## <a name="install-selenium-drivers"></a><span data-ttu-id="88de5-259">Selenium ドライバーのインストール</span><span class="sxs-lookup"><span data-stu-id="88de5-259">Install Selenium drivers</span></span>

<span data-ttu-id="88de5-260">Selenium ドライバーを手動でインストールするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88de5-260">For manual installation of Selenium drivers, follow these steps:</span></span>
1. <span data-ttu-id="88de5-261">[Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88de5-261">Download [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip).</span></span> <span data-ttu-id="88de5-262">または、 https://docs.seleniumhq.org/download に移動し、 **以前のリリース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-262">Or, go to https://docs.seleniumhq.org/download and click **Previous releases**.</span></span> <span data-ttu-id="88de5-263">**3.13** を選択して、 **selenium-dotnet-strongnamed-3.13.1.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88de5-263">Choose **3.13** and download **selenium-dotnet-strongnamed-3.13.1.zip**.</span></span>
2. <span data-ttu-id="88de5-264">Selenium ライブラリをインストールします:</span><span class="sxs-lookup"><span data-stu-id="88de5-264">Install the Selenium libraries:</span></span>
    + <span data-ttu-id="88de5-265">ダウンロード ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="88de5-265">Unzip the downloaded file.</span></span> 
    + <span data-ttu-id="88de5-266">ファイル **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg** を展開します。</span><span class="sxs-lookup"><span data-stu-id="88de5-266">Unpack the file **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg**.</span></span> <span data-ttu-id="88de5-267">このファイルを展開するには、ファイルに .zip拡張子を追加して、解凍します。</span><span class="sxs-lookup"><span data-stu-id="88de5-267">To unpack this file, add the .zip suffix to the file and unzip it.</span></span> 
    + <span data-ttu-id="88de5-268">**Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** という名前のフォルダーの内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="88de5-268">Copy the contents of the folder named **Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>
3.  <span data-ttu-id="88de5-269">[Internet Explorer ドライバー バージョン 3.4.0](https://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88de5-269">Download the [Internet Explorer driver version 3.4.0](https://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip).</span></span> <span data-ttu-id="88de5-270">または、ブラウザーに戻り、**3.4** フォルダを開いて、**IEDriverServer_x64_3.4.0.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88de5-270">Or, go back in the browser, open the **3.4** folder, and download **IEDriverServer_x64_3.4.0.zip**.</span></span>
4.  <span data-ttu-id="88de5-271">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="88de5-271">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

<span data-ttu-id="88de5-272">Google Chromeをブラウザーとして使用するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="88de5-272">If you want to use Google Chrome as your browser, follow these steps:</span></span>
1. <span data-ttu-id="88de5-273">https://sites.google.com/a/chromium.org/chromedriver/downloads に移動します。</span><span class="sxs-lookup"><span data-stu-id="88de5-273">Go to https://sites.google.com/a/chromium.org/chromedriver/downloads.</span></span> 
2. <span data-ttu-id="88de5-274">最新/現在のリリースから **chromedriver_win32.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88de5-274">Download **chromedriver_win32.zip** from the latest/current release.</span></span>
3. <span data-ttu-id="88de5-275">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="88de5-275">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

## <a name="manual-configuration-of-authentication-certificates"></a><span data-ttu-id="88de5-276">認証証明書の手動構成</span><span class="sxs-lookup"><span data-stu-id="88de5-276">Manual configuration of authentication certificates</span></span>

<span data-ttu-id="88de5-277">必要に応じて、RSAT認証証明書を手動で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="88de5-277">Optionally, you can manually configure the RSAT authentication certificate.</span></span>

<span data-ttu-id="88de5-278">このプロセスに精通していない場合は、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="88de5-278">If you are not familiar with this process, get help from your system administrator.</span></span> <span data-ttu-id="88de5-279">Windows キットがコンピューターにインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="88de5-279">Make sure you have Windows Kits installed on your machine.</span></span> <span data-ttu-id="88de5-280">Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="88de5-280">If you do not have Windows Kits installed on your machine, you can download the Windows 10 SDK from [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> <span data-ttu-id="88de5-281">このドキュメントで説明されている手順には、これらのコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="88de5-281">You will need these components for the steps described in this document.</span></span>

+ <span data-ttu-id="88de5-282">デスクトップ アプリ用の Windows SDK 署名ツール</span><span class="sxs-lookup"><span data-stu-id="88de5-282">Windows SDK Signing Tools for Desktop Apps</span></span>
+ <span data-ttu-id="88de5-283">UWP マネージド アプリ用のWindows SDK。</span><span class="sxs-lookup"><span data-stu-id="88de5-283">Windows SDK for UWP Managed Apps.</span></span>

### <a name="generate-the-certificate"></a><span data-ttu-id="88de5-284">証明書を生成する</span><span class="sxs-lookup"><span data-stu-id="88de5-284">Generate the certificate</span></span>

<span data-ttu-id="88de5-285">RSAT クライアント コンピュータで証明書ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-285">You must generate the certificate file on the RSAT client computer.</span></span> <span data-ttu-id="88de5-286">**証明書は、テスト ツールを実行している同じコンピュータで生成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="88de5-286">**The certificate must be generated on the same computer that the test tool is running on.**</span></span> <span data-ttu-id="88de5-287">証明書ファイルを生成するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="88de5-287">To generate the certificate file, follow these steps:</span></span>
1. <span data-ttu-id="88de5-288">コンピューター上にまだ存在しない場合は、 **C:\Temp** フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="88de5-288">Create the **C:\Temp** folder if it does not already exist on your computer.</span></span>
2. <span data-ttu-id="88de5-289">管理者としてコマンド ライン ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="88de5-289">Open a command line window as Administrator.</span></span>
3. <span data-ttu-id="88de5-290">Windows SDKをインストールしたフォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="88de5-290">Go to the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="88de5-291">正確なフォルダは、Windows SDKをインストールした場所によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-291">Your exact folder may be different, depending on where you have installed the windows SDK).</span></span> <span data-ttu-id="88de5-292">Windows キット 8.1を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="88de5-292">You can also use Windows Kits 8.1.</span></span>

    ```Console
    cd c:\Program Files (x86)\Windows Kits\10\bin\10.0.17763.0\x64
    ```

4. <span data-ttu-id="88de5-293">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="88de5-293">Run the following command.</span></span> <span data-ttu-id="88de5-294">秘密キー パスワードを要求するプロンプトが表示されたら、 **なし** を入力します。</span><span class="sxs-lookup"><span data-stu-id="88de5-294">When you are prompted to enter a private key password, enter **None**.</span></span> 

    ```Console
    makecert.exe -n "CN=127.0.0.1" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 c:\temp\authCert.cer
    ````

### <a name="install-the-certificate-to-the-trusted-root"></a><span data-ttu-id="88de5-295">信頼済ルートに証明書をインストールする</span><span class="sxs-lookup"><span data-stu-id="88de5-295">Install the certificate to the Trusted Root</span></span>

<span data-ttu-id="88de5-296">証明書をインストールするには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="88de5-296">To install the certificate, follow these steps:</span></span>

1. <span data-ttu-id="88de5-297">証明書をインストールするには、 **authCert.cer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-297">Double-click **authCert.cer** to install the certificate.</span></span>
2. <span data-ttu-id="88de5-298">**証明書のインストール** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-298">Click **Install Certificate**.</span></span>
3. <span data-ttu-id="88de5-299">**ローカルマシン > すべての証明書を次のストアにを配置 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88de5-299">Select **Local Machine > Place all certificates in the following Store > Browse > Trusted Root Certification Authorities** and click **Next** through each screen.</span></span>
4. <span data-ttu-id="88de5-300">**パスワード** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="88de5-300">Leave the **Password** field blank.</span></span>
5. <span data-ttu-id="88de5-301">**証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。</span><span class="sxs-lookup"><span data-stu-id="88de5-301">In the **Certificate** dialog box, browse to **Details** and look for **Thumbprint**.</span></span>

    ![拇印の一覧を示す証明書ダイアログ](media/certificate-dialog.png)
 
6. <span data-ttu-id="88de5-303">拇印をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="88de5-303">Copy and save the thumbprint.</span></span> <span data-ttu-id="88de5-304">このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88de5-304">You will need it to configure the AOS as described earlier in this topic.</span></span>
