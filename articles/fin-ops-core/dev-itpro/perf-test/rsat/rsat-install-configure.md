---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9682d139a3dfa8b7c7db25614a0369326af34ebf
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282755"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a><span data-ttu-id="2b9ac-103">Regression Suite Automation Tool のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="2b9ac-103">Regression Suite Automation Tool installation and configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b9ac-104">このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-104">This topic contains information about how install and configure the Regression suite automation tool (RSAT).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b9ac-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="2b9ac-105">Prerequisites</span></span>

### <a name="test-environment"></a><span data-ttu-id="2b9ac-106">テスト環境</span><span class="sxs-lookup"><span data-stu-id="2b9ac-106">Test environment</span></span>
<span data-ttu-id="2b9ac-107">テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-107">Your test environment must be running Platform update 15 or newer.</span></span> <span data-ttu-id="2b9ac-108">Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-108">The Regression suite automation tool must have access to your test environment via a web browser.</span></span>  

### <a name="excel"></a><span data-ttu-id="2b9ac-109">Excel</span><span class="sxs-lookup"><span data-stu-id="2b9ac-109">Excel</span></span>
<span data-ttu-id="2b9ac-110">テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-110">You need Microsoft Excel installed to generate and edit test parameters.</span></span> 

### <a name="azure-devops"></a><span data-ttu-id="2b9ac-111">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="2b9ac-111">Azure DevOps</span></span>
<span data-ttu-id="2b9ac-112">テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-112">You must have an Azure DevOps project to store and manage your test cases, test plans, and test case results.</span></span> <span data-ttu-id="2b9ac-113">Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-113">You will need an Azure DevOps Test Manager or Test Plans license.</span></span> <span data-ttu-id="2b9ac-114">たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-114">For example, if you have a Visual Studio Enterprise subscription, you already have a license to Test Plans.</span></span> <span data-ttu-id="2b9ac-115">詳細については、[Azure DevOps サービス](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) の価格設定、または [Azure DevOps サーバーの価格設定](https://azure.microsoft.com/pricing/details/devops/server/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-115">For more information, see [Pricing for Azure DevOps Services](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) or [Pricing for Azure DevOps Server](https://azure.microsoft.com/pricing/details/devops/server/).</span></span>

### <a name="authentication-certificate"></a><span data-ttu-id="2b9ac-116">認証証明書</span><span class="sxs-lookup"><span data-stu-id="2b9ac-116">Authentication Certificate</span></span>
<span data-ttu-id="2b9ac-117">RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザーを介して環境にリモート接続するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-117">RSAT is designed to be installed on any Windows 10 computer and connect remotely via a web browser to an environment.</span></span>

![クライアント コンピュータと環境](media/client-environment.png)

<span data-ttu-id="2b9ac-119">セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-119">To enable secure authentication, RSAT requires a certificate to be installed on the RSAT client computer.</span></span> <span data-ttu-id="2b9ac-120">RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-120">The RSAT settings dialog box allows you to automatically create and install the authentication certificate.</span></span> <span data-ttu-id="2b9ac-121">また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-121">You will also need to configure the virtual machine (VM) to trust the connection.</span></span> <span data-ttu-id="2b9ac-122">RSATをインストールして構成するには、次のセクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-122">Follow the instructions in the next sections to install and configure RSAT.</span></span>

## <a name="installation"></a><span data-ttu-id="2b9ac-123">インストール</span><span class="sxs-lookup"><span data-stu-id="2b9ac-123">Installation</span></span>

### <a name="installer"></a><span data-ttu-id="2b9ac-124"> インストーラー</span><span class="sxs-lookup"><span data-stu-id="2b9ac-124">Installer</span></span>
<span data-ttu-id="2b9ac-125">[Regression Suite Automation Tool ダウンロード](https://www.microsoft.com/download/details.aspx?id=57357) からマシンに .msi ファイルをダウンロードし、ダブルクリックしてインストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-125">Download the .msi file from the [Regression Suite Automation Tool Download](https://www.microsoft.com/download/details.aspx?id=57357) to your machine and double-click it to run the installer.</span></span> 

> [!NOTE]
> <span data-ttu-id="2b9ac-126">Azure DevOps サーバーを使用している場合は、バージョン 1.210.48249.4 以降をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-126">If you're using Azure DevOps Server, download and install version 1.210.48249.4 or later.</span></span> 
 
### <a name="selenium-and-browser-drivers"></a><span data-ttu-id="2b9ac-127">Selenium およびブラウザー ドライバー</span><span class="sxs-lookup"><span data-stu-id="2b9ac-127">Selenium and Browser Drivers</span></span>
<span data-ttu-id="2b9ac-128">RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-128">RSAT requires Selenium and web browser driver libraries.</span></span> <span data-ttu-id="2b9ac-129">RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-129">RSAT will prompt you if needed libraries are missing and will automatically install them for you.</span></span> <span data-ttu-id="2b9ac-130">次の (または類似の) メッセージが表示されたら、はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-130">Select Yes when you see the following (or similar) messages.</span></span>
 
![Selenium ドライバー](media/driver-1.png)
 
![ブラウザー ドライバー](media/driver-2.png)

<span data-ttu-id="2b9ac-133">または、 [Selenium ドライバーのインストール](#install-selenium-drivers) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-133">Alternatively, refer to [Install Selenium Driver](#install-selenium-drivers).</span></span>

## <a name="configuration"></a><span data-ttu-id="2b9ac-134">構成</span><span class="sxs-lookup"><span data-stu-id="2b9ac-134">Configuration</span></span>

<span data-ttu-id="2b9ac-135">デスクトップから RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-135">Open RSAT from your desktop.</span></span>

![RSAT デスクトップ アイコン](media/desktop-icon.png)
 
<span data-ttu-id="2b9ac-137">RSATを構成するには、右上の **設定** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-137">Select **Settings** button in the upper right to configure RSAT.</span></span>

![RSAT 設定](media/rsat-settings.png)

### <a name="general-settings"></a><span data-ttu-id="2b9ac-139">一般設定</span><span class="sxs-lookup"><span data-stu-id="2b9ac-139">General settings</span></span>
<span data-ttu-id="2b9ac-140">これらの設定は必須です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-140">These settings are required.</span></span>

#### <a name="azure-devops"></a><span data-ttu-id="2b9ac-141">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="2b9ac-141">Azure DevOps</span></span>
<span data-ttu-id="2b9ac-142">Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-142">Configure your connection to the Azure DevOps project and test plan.</span></span>

+ <span data-ttu-id="2b9ac-143">**Azure DevOps URL** - これは、 Azure DevOps 組織のURLです。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-143">**Azure DevOps Url** - This is the URL of your Azure DevOps organization.</span></span> <span data-ttu-id="2b9ac-144">たとえば、`https://yourAzureDevOpsUrlHere.visualStudio.com`。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-144">For example, `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b9ac-145">Azure DevOps サーバーを使用している場合は、**/DefaultCollection** を Azure DevOps URL の末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-145">If you're using Azure DevOps Server, add **/DefaultCollection** to the end of your Azure DevOps URL.</span></span>

+ <span data-ttu-id="2b9ac-146">**アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-146">**Access Token** - The access token that allows the tool to connect to Azure DevOps.</span></span> <span data-ttu-id="2b9ac-147">個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-147">You need to create a Personal Access Token or use an existing one that you have saved.</span></span> <span data-ttu-id="2b9ac-148">詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-148">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span> 
+ <span data-ttu-id="2b9ac-149">**プロジェクト名** - Azure DevOps プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-149">**Project Name** - The name of your Azure DevOps project.</span></span> <span data-ttu-id="2b9ac-150">RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-150">RSAT will automatically detect project names and test plans available based the Azure DevOps URL specified.</span></span> <span data-ttu-id="2b9ac-151">その後、テスト プロジェクトおよびテスト計画を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-151">You can then select the Test Project and Test Plan.</span></span>
+ <span data-ttu-id="2b9ac-152">**テスト計画** - テスト ケースを含む Azure DevOps テスト計画</span><span class="sxs-lookup"><span data-stu-id="2b9ac-152">**Test Plan** - The Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="2b9ac-153">詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-153">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> 

<span data-ttu-id="2b9ac-154">**接続のテスト** を選択し、 Azure DevOps への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-154">Select **Test Connection** to test your connection to Azure DevOps.</span></span>

#### <a name="test-environment"></a><span data-ttu-id="2b9ac-155">テスト環境</span><span class="sxs-lookup"><span data-stu-id="2b9ac-155">Test environment</span></span>
<span data-ttu-id="2b9ac-156">テスト環境への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-156">Configure your connection to the test environment.</span></span>

+ <span data-ttu-id="2b9ac-157">**ホスト名** – myhost.cloudax.dynamics.com. などのテスト環境のホスト名。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-157">**Hostname** – The hostname of the test environment, such as myhost.cloudax.dynamics.com.</span></span> <span data-ttu-id="2b9ac-158">https:// または http:// の接頭語を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-158">Don't include the https:// or http:// prefix.</span></span>
+ <span data-ttu-id="2b9ac-159">**SOAP ホスト名** – テスト環境の SOAP ホスト名。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-159">**SOAP Hostname** – The SOAP hostname of the test environment.</span></span> <span data-ttu-id="2b9ac-160">通常は、ホスト名に **soap** の接尾語を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-160">Typically, you must add a **soap** suffix to the hostname.</span></span> <span data-ttu-id="2b9ac-161">たとえば、ホスト名が myhost.cloudax.dynamics.com の場合は、myhost**soap**.cloudax.dynamics.com を SOAP ホスト名として使用します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-161">For example, if your hostname is myhost.cloudax.dynamics.com, use myhost**soap**.cloudax.dynamics.com as the SOAP hostname.</span></span>

    + <span data-ttu-id="2b9ac-162">テスト環境の SOAP ホスト名がわからない場合は、Infrastructure.SoapServicesUrl の AOS サーバーの web.config ファイルで検索できます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-162">If you don't know the SOAP hostname of your test environment, you can find it in the web.config file for the AOS server in Infrastructure.SoapServicesUrl.</span></span>
    + <span data-ttu-id="2b9ac-163">テスト環境が、リモート デスクトップ アクセスを持たないセルフサービス ユーザー受け入れテスト (UAT) または高レベル サンドボックス環境 (つまり、Azure Service Fabricインフラストラクチャ上で実行されている環境) である場合、その SOAP ホスト名はホスト名と一致します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-163">If your test environment is a self-service user acceptance testing (UAT) or higher-tier sandbox environment that has no Remote Desktop access (that is, it's an environment that is running on the Azure Service Fabric infrastructure), the SOAP hostname matches the hostname.</span></span>

+ <span data-ttu-id="2b9ac-164">**管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-164">**Admin User Name** – The email address of an admin user in the test environment.</span></span>
+ <span data-ttu-id="2b9ac-165">**拇印** – 使用している認証証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-165">**Thumbprint** – The thumbprint of the authentication certificate that you're using.</span></span>

    1. <span data-ttu-id="2b9ac-166">新しい証明書を作成してインストールするには、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-166">Select **New** to create and install a new authentication certificate.</span></span> <span data-ttu-id="2b9ac-167">プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-167">When prompted, place the .cer file somewhere so you have it saved for your records.</span></span>
    2. <span data-ttu-id="2b9ac-168">プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート店舗にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-168">When the process completes, the new certification is installed in the local machine's trusted root store.</span></span>

        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. <span data-ttu-id="2b9ac-170">新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-170">The thumbprint of the newly created certificate is automatically inserted on this form.</span></span> <span data-ttu-id="2b9ac-171">この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-171">Copy this thumbprint, you will use it in the next section to configure the AOS to trust the connection.</span></span>

+ <span data-ttu-id="2b9ac-172">**会社名** – Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-172">**Company name** – Specify a company name to use as your default company during creation of Excel parameters files.</span></span> <span data-ttu-id="2b9ac-173">後でExcelファイルを編集して変更できます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-173">It can be changed later by editing an Excel file.</span></span>


#### <a name="run-setting"></a><span data-ttu-id="2b9ac-174">実行設定</span><span class="sxs-lookup"><span data-stu-id="2b9ac-174">Run setting</span></span>
<span data-ttu-id="2b9ac-175">ローカル設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-175">Configure your local settings.</span></span>

+ <span data-ttu-id="2b9ac-176">**作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-176">**Working directory** - Folder location for storing test automation files, including Excel test data files.</span></span> <span data-ttu-id="2b9ac-177">たとえば、 **C:\Temp\RegressionTool** のようになります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-177">For example: **C:\Temp\RegressionTool**.</span></span>
+ <span data-ttu-id="2b9ac-178">**既定のブラウザー** - テストの実行に使用するブラウザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-178">**Default browser** - Select the browser to use for test execution.</span></span>

<span data-ttu-id="2b9ac-179">**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-179">Select **Ok** to apply your settings and close the dialog box.</span></span> <span data-ttu-id="2b9ac-180">**キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-180">Select **Cancel** to cancel your changes and close the dialog.</span></span> <span data-ttu-id="2b9ac-181">**名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-181">The **Save As** and **Open** buttons allow you to save your settings for reuse later.</span></span> <span data-ttu-id="2b9ac-182">**名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-182">Select **Save As** to save your current settings into a configuration file on your computer.</span></span> <span data-ttu-id="2b9ac-183">**開く** を選択して、構成ファイルから設定を復元します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-183">Select **Open** to restore your settings from a configuration file.</span></span>

### <a name="optional-settings"></a><span data-ttu-id="2b9ac-184">オプション設定</span><span class="sxs-lookup"><span data-stu-id="2b9ac-184">Optional settings</span></span>
<span data-ttu-id="2b9ac-185">**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-185">Select the **Optional** tab to configure optional settings.</span></span>

+ <span data-ttu-id="2b9ac-186">**テストの実行の接頭語** – RSATはテストの実行結果を Azure DevOps に報告します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-186">**Test Run Prefix** – RSAT reports test run results to Azure DevOps.</span></span> <span data-ttu-id="2b9ac-187">テストの実行には、次の規則に従って名前が付けられます。**\<実行 ID\> \<接頭語\> \<テスト スイート\>**。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-187">Test runs are named using the following convention: **\<Run ID\> \<Prefix\> \<Test Suite\>**.</span></span> <span data-ttu-id="2b9ac-188">この設定を使用して、**\<接頭語\>** を設定します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-188">Use this setting to set the **\<Prefix\>**.</span></span>
+ <span data-ttu-id="2b9ac-189">**テストの実行タイムアウト** – テストの実行のタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-189">**Test Run Timeout** – The time-out (in minutes) of a test run.</span></span> <span data-ttu-id="2b9ac-190">このタイムアウトに達すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-190">All active windows are closed and pending test cases fail when this time-out is reached.</span></span>
+ <span data-ttu-id="2b9ac-191">**テスト アクションのタイムアウト** – 個々のテスト ステップのタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-191">**Test Action Timeout** – The time-out (in minutes) of individual test steps.</span></span> <span data-ttu-id="2b9ac-192">テストステップがタイムアウトになると、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-192">When a test step times out, the test case fails.</span></span>
+ <span data-ttu-id="2b9ac-193">**ステップ間の一時停止** – テストケースの自動実行中にテスト ステップ間で一時停止する秒数。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-193">**Pause between steps** – The number of seconds to pause between test steps during automated execution of a test case.</span></span> <span data-ttu-id="2b9ac-194">既定値は **0** (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-194">The default value is **0** (zero).</span></span> <span data-ttu-id="2b9ac-195">監査または調査のために、テストの実行中に強制的に一時停止するには、この値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-195">Set this value to force a pause during test execution, for auditing or investigative purposes.</span></span> <span data-ttu-id="2b9ac-196">テスト ケースの Excel パラメーター ファイルの**全般**タブにある、**ステップ間の一時停止 (秒)** パラメーターを変更することで、個々のテスト ケースに対して一時停止を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-196">You can also specify a pause for an individual test case by changing the **Pause between steps (Seconds)** parameter on the **General** tab of the Excel parameter file for the test case.</span></span>
+ <span data-ttu-id="2b9ac-197">**最初の検証エラーでテストに失敗** – 既定では、テスト ケースに複数の検証ステップがあり、検証に失敗した場合は、最初の失敗が発生するとテスト ケースの実行が停止します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-197">**Fail test on first validation error** – By default, if a test case has multiple validation steps, and there is a validation failure, the test case stops running when the first failure occurs.</span></span> <span data-ttu-id="2b9ac-198">テスト ケースは失敗としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-198">The test case is then marked as failed.</span></span> <span data-ttu-id="2b9ac-199">すべての検証が完了するまでテスト ケースを実行する場合は、このオプションをオフにします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-199">If you want test cases to continue to run until all validations are completed, clear this option.</span></span> <span data-ttu-id="2b9ac-200">その後、テスト ケースですべての検証を評価できます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-200">The test case can then evaluate all validations.</span></span>
+ <span data-ttu-id="2b9ac-201">**失敗時にテスト スイートの実行を中止する** – 既定では、いずれかのテスト ケースが失敗した場合でもテスト スイートの実行が続行されます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-201">**Abort test suite execution on failure** – By default, execution of a test suite continues even if one of the test cases fails.</span></span> <span data-ttu-id="2b9ac-202">このオプションを **True** に設定すると、テスト ケースが失敗した場合にテストの実行が中止されます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-202">If you set this option to **True**, the test run is aborted if a test case fails.</span></span> <span data-ttu-id="2b9ac-203">残りのすべてのテスト ケースのステータスは**未実行**になります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-203">All the remaining test cases will have a status of **Not Executed**.</span></span>
+ <span data-ttu-id="2b9ac-204">**クラウド プロバイダー** – テスト環境のクラウド テナントのプロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-204">**Cloud provider** – Select the provider of the cloud tenant of your test environment.</span></span> <span data-ttu-id="2b9ac-205">サポートされているプロバイダーは、**グローバル** (パブリッククラウド) および**中国** (主権クラウド) です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-205">Supported providers are **Global** (Public cloud) and **China** (Sovereign cloud).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2b9ac-206">Finance and Operations アプリが 21Vianet に配置されている場合、**クラウド プロバイダー** の設定が必要となり、選択された値が **中国** でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-206">The **Cloud provider** setting is required, and the selected value must be **China** if your Finance and Operations apps were deployed in 21Vianet.</span></span>

### <a name="configure-the-test-environment-to-trust-the-connection"></a><span data-ttu-id="2b9ac-207">接続を信頼するようにテスト環境を構成する</span><span class="sxs-lookup"><span data-stu-id="2b9ac-207">Configure the test environment to trust the connection</span></span>

#### <a name="if-your-aos-allows-for-remote-desktop-connections"></a><span data-ttu-id="2b9ac-208">AOS がリモート デスクトップ接続を許可している場合</span><span class="sxs-lookup"><span data-stu-id="2b9ac-208">If your AOS allows for Remote Desktop connections</span></span>

<span data-ttu-id="2b9ac-209">証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-209">After creating the certificate, configure AOS to trust the test automation connection.</span></span> <span data-ttu-id="2b9ac-210">マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-210">On a multi-AOS environment, repeat the following steps for all AOS machines.</span></span>

1.  <span data-ttu-id="2b9ac-211">AOSマシンへのリモート デスクトップ接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-211">Open a Remote Desktop connection to the AOS machine.</span></span>
2.  <span data-ttu-id="2b9ac-212">IIS を開き、サイトの一覧で AOSService を見つけます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-212">Open IIS and find AOSService in the list of sites.</span></span>

    ![IISでのAOSの検索](media/configure-aos.png)

3.  <span data-ttu-id="2b9ac-214">**AOSservice** を右クリックし、 **エクスプローラー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-214">Right-click **AOSService**, then click **Explore**.</span></span>
4.  <span data-ttu-id="2b9ac-215">ファイル **wif.config** を開き、検索します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-215">Open and find the file **wif.config**.</span></span>
  
    ![wif.config を開く](media/open-wif-config.png)

5.  <span data-ttu-id="2b9ac-217">次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-217">Update the **wif.config** file by adding a new authority entry, as shown in the following example.</span></span> <span data-ttu-id="2b9ac-218">機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-218">Use **127.0.0.1** for the authority name and paste your certificate thumbprint.</span></span>

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

#### <a name="if-you-have-no-remote-desktop-access-to-the-server"></a><span data-ttu-id="2b9ac-219">サーバーへのリモート デスクトップ アクセス権がない場合</span><span class="sxs-lookup"><span data-stu-id="2b9ac-219">If you have no Remote Desktop access to the server</span></span>

<span data-ttu-id="2b9ac-220">テスト環境でリモート デスクトップ アクセスが許可されていない場合は、次の手順に従って、RSAT 接続を信頼するように環境を構成します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-220">If your test environment doesn't allow for Remote Desktop access, follow these steps to configure the environment to trust the RSAT connection.</span></span> <span data-ttu-id="2b9ac-221">たとえば、セルフ サービス UAT またはそれ以上のサンドボックス環境 (つまり、 Service Fabric インフラストラクチャ上で実行されている環境) では、リモート デスクトップ アクセスが許可されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-221">An environment might not allow for Remote Desktop access if, for example, it's a self-service UAT or higher-tier sandbox environment (that is, it's an environment that is running on the Service Fabric infrastructure).</span></span>

1. <span data-ttu-id="2b9ac-222">このトピックで前述されているように、RSAT の設定ダイアログ ボックスの**新規**ボタンを使用して、RSAT 認証証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-222">Create the RSAT authentication certificate by using the **New** button in the RSAT settings dialog box, as described earlier in this topic.</span></span>
2. <span data-ttu-id="2b9ac-223">サポート要求を開き、サポート エンジニアに次の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-223">Open a support request, and provide the following information to the support engineer:</span></span>

    - <span data-ttu-id="2b9ac-224">環境 ID (Microsoft Dynamics Lifecycle Services \[LCS\] の環境ページでこの ID を確認できます。)</span><span class="sxs-lookup"><span data-stu-id="2b9ac-224">Your environment ID (You can find this ID on the environment page in Microsoft Dynamics Lifecycle Services \[LCS\].)</span></span>
    - <span data-ttu-id="2b9ac-225">RSAT によって生成された .cer ファイル</span><span class="sxs-lookup"><span data-stu-id="2b9ac-225">The .cer file that RSAT generated</span></span>
    - <span data-ttu-id="2b9ac-226">サンドボックス環境で許容できるダウンタイム ウィンドウ (ダウンタイムは分単位で表されます。)</span><span class="sxs-lookup"><span data-stu-id="2b9ac-226">An acceptable downtime window for the sandbox environment (Downtime is expressed in minutes.)</span></span>

### <a name="installation-of-rsat-on-multiple-computers"></a><span data-ttu-id="2b9ac-227">複数のコンピューターへの RSAT のインストール</span><span class="sxs-lookup"><span data-stu-id="2b9ac-227">Installation of RSAT on multiple computers</span></span>

<span data-ttu-id="2b9ac-228">テスト環境は、複数の RSAT 接続を信頼するように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-228">A test environment can be configured to trust more than one RSAT connection.</span></span> <span data-ttu-id="2b9ac-229">複数のコンピューターに RSAT をインストールする場合は、各 RSAT のインストールに対して新しい証明書を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-229">If you install RSAT on more than one computer, you must generate a new certificate for each RSAT installation.</span></span> <span data-ttu-id="2b9ac-230">証明書を生成し、RSATと同じコンピューターにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-230">The certificate must be generated and installed on the same computer as RSAT.</span></span> <span data-ttu-id="2b9ac-231">RSATがインストールされている複数のクライアントからの接続をAOSに信頼させる場合、AOS wif.config ファイルに複数の拇印エントリを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-231">You can have more than one thumbprint entry in the AOS wif.config file if you want your AOS to trust connections from more than one client where RSAT is installed.</span></span> <span data-ttu-id="2b9ac-232">次の例は、複数の拇印ノードを示しています。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-232">The following example shows multiple thumbprint nodes.</span></span>

```xml
<keys>
    <add thumbprint="ccbc124d0a119xxxxxxxxxxxxxxxxxxxx841e797" />
    <add thumbprint="bbbbbbbbbbbbbbxxxxxxxxxxxxxxxxxxxx999999" />
</keys>
```

## <a name="install-selenium-drivers"></a><span data-ttu-id="2b9ac-233">Selenium ドライバーのインストール</span><span class="sxs-lookup"><span data-stu-id="2b9ac-233">Install Selenium drivers</span></span>

<span data-ttu-id="2b9ac-234">Selenium ドライバーを手動でインストールするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-234">For manual installation of Selenium drivers, follow these steps:</span></span>
1. <span data-ttu-id="2b9ac-235">[Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-235">Download [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip).</span></span> <span data-ttu-id="2b9ac-236">または、 https://docs.seleniumhq.org/download に移動し、 **以前のリリース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-236">Or, go to https://docs.seleniumhq.org/download and click **Previous releases**.</span></span> <span data-ttu-id="2b9ac-237">**3.13** を選択して、 **selenium-dotnet-strongnamed-3.13.1.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-237">Choose **3.13** and download **selenium-dotnet-strongnamed-3.13.1.zip**.</span></span>
2. <span data-ttu-id="2b9ac-238">Selenium ライブラリをインストールします:</span><span class="sxs-lookup"><span data-stu-id="2b9ac-238">Install the Selenium libraries:</span></span>
    + <span data-ttu-id="2b9ac-239">ダウンロード ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-239">Unzip the downloaded file.</span></span> 
    + <span data-ttu-id="2b9ac-240">ファイル **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg** を展開します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-240">Unpack the file **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg**.</span></span> <span data-ttu-id="2b9ac-241">このファイルを展開するには、ファイルに .zip拡張子を追加して、解凍します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-241">To unpack this file, add the .zip suffix to the file and unzip it.</span></span> 
    + <span data-ttu-id="2b9ac-242">**Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** という名前のフォルダーの内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-242">Copy the contents of the folder named **Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>
3.  <span data-ttu-id="2b9ac-243">[Internet Explorer ドライバー バージョン 3.4.0](https://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-243">Download the [Internet Explorer driver version 3.4.0](https://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip).</span></span> <span data-ttu-id="2b9ac-244">または、ブラウザーに戻り、**3.4** フォルダを開いて、**IEDriverServer_x64_3.4.0.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-244">Or, go back in the browser, open the **3.4** folder, and download **IEDriverServer_x64_3.4.0.zip**.</span></span>
4.  <span data-ttu-id="2b9ac-245">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-245">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

<span data-ttu-id="2b9ac-246">Google Chromeをブラウザーとして使用するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="2b9ac-246">If you want to use Google Chrome as your browser, follow these steps:</span></span>
1. <span data-ttu-id="2b9ac-247">https://sites.google.com/a/chromium.org/chromedriver/downloads に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-247">Go to https://sites.google.com/a/chromium.org/chromedriver/downloads.</span></span> 
2. <span data-ttu-id="2b9ac-248">最新/現在のリリースから **chromedriver_win32.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-248">Download **chromedriver_win32.zip** from the latest/current release.</span></span>
3. <span data-ttu-id="2b9ac-249">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-249">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

## <a name="manual-configuration-of-authentication-certificates"></a><span data-ttu-id="2b9ac-250">認証証明書の手動構成</span><span class="sxs-lookup"><span data-stu-id="2b9ac-250">Manual configuration of authentication certificates</span></span>

<span data-ttu-id="2b9ac-251">必要に応じて、RSAT認証証明書を手動で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-251">Optionally, you can manually configure the RSAT authentication certificate.</span></span>

<span data-ttu-id="2b9ac-252">このプロセスに精通していない場合は、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-252">If you are not familiar with this process, get help from your system administrator.</span></span> <span data-ttu-id="2b9ac-253">Windows キットがコンピューターにインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-253">Make sure you have Windows Kits installed on your machine.</span></span> <span data-ttu-id="2b9ac-254">Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-254">If you do not have Windows Kits installed on your machine, you can download the Windows 10 SDK from [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> <span data-ttu-id="2b9ac-255">このドキュメントで説明されている手順には、これらのコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-255">You will need these components for the steps described in this document.</span></span>

+ <span data-ttu-id="2b9ac-256">デスクトップ アプリ用の Windows SDK 署名ツール</span><span class="sxs-lookup"><span data-stu-id="2b9ac-256">Windows SDK Signing Tools for Desktop Apps</span></span>
+ <span data-ttu-id="2b9ac-257">UWP マネージド アプリ用のWindows SDK。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-257">Windows SDK for UWP Managed Apps.</span></span>

### <a name="generate-the-certificate"></a><span data-ttu-id="2b9ac-258">証明書を生成する</span><span class="sxs-lookup"><span data-stu-id="2b9ac-258">Generate the certificate</span></span>

<span data-ttu-id="2b9ac-259">RSAT クライアント コンピュータで証明書ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-259">You must generate the certificate file on the RSAT client computer.</span></span> <span data-ttu-id="2b9ac-260">**証明書は、テスト ツールを実行している同じコンピュータで生成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="2b9ac-260">**The certificate must be generated on the same computer that the test tool is running on.**</span></span> <span data-ttu-id="2b9ac-261">証明書ファイルを生成するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="2b9ac-261">To generate the certificate file, follow these steps:</span></span>
1. <span data-ttu-id="2b9ac-262">コンピューター上にまだ存在しない場合は、 **C:\Temp** フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-262">Create the **C:\Temp** folder if it does not already exist on your computer.</span></span>
2. <span data-ttu-id="2b9ac-263">管理者としてコマンド ライン ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-263">Open a command line window as Administrator.</span></span>
3. <span data-ttu-id="2b9ac-264">Windows SDKをインストールしたフォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-264">Go to the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="2b9ac-265">正確なフォルダは、Windows SDKをインストールした場所によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-265">Your exact folder may be different, depending on where you have installed the windows SDK).</span></span> <span data-ttu-id="2b9ac-266">Windows キット 8.1を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-266">You can also use Windows Kits 8.1.</span></span>

    ```Console
    cd c:\Program Files (x86)\Windows Kits\10\bin\10.0.17763.0\x64
    ```

4. <span data-ttu-id="2b9ac-267">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-267">Run the following command.</span></span> <span data-ttu-id="2b9ac-268">秘密キー パスワードを要求するプロンプトが表示されたら、 **なし** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-268">When you are prompted to enter a private key password, enter **None**.</span></span> 

    ```Console
    makecert.exe -n "CN=127.0.0.1" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 c:\temp\authCert.cer
    ````

### <a name="install-the-certificate-to-the-trusted-root"></a><span data-ttu-id="2b9ac-269">信頼済ルートに証明書をインストールする</span><span class="sxs-lookup"><span data-stu-id="2b9ac-269">Install the certificate to the Trusted Root</span></span>

<span data-ttu-id="2b9ac-270">証明書をインストールするには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="2b9ac-270">To install the certificate, follow these steps:</span></span>

1. <span data-ttu-id="2b9ac-271">証明書をインストールするには、 **authCert.cer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-271">Double-click **authCert.cer** to install the certificate.</span></span>
2. <span data-ttu-id="2b9ac-272">**証明書のインストール** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-272">Click **Install Certificate**.</span></span>
3. <span data-ttu-id="2b9ac-273">**ローカルマシン > すべての証明書を次のストアにを配置 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-273">Select **Local Machine > Place all certificates in the following Store > Browse > Trusted Root Certification Authorities** and click **Next** through each screen.</span></span>
4. <span data-ttu-id="2b9ac-274">**パスワード** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-274">Leave the **Password** field blank.</span></span>
5. <span data-ttu-id="2b9ac-275">**証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-275">In the **Certificate** dialog box, browse to **Details** and look for **Thumbprint**.</span></span>

    ![拇印の一覧を示す証明書ダイアログ](media/certificate-dialog.png)
 
6. <span data-ttu-id="2b9ac-277">拇印をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-277">Copy and save the thumbprint.</span></span> <span data-ttu-id="2b9ac-278">このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b9ac-278">You will need it to configure the AOS as described earlier in this topic.</span></span>
