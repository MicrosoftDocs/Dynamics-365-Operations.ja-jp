---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 2e2907cb7eb684bce1c09ed9171ed91ffd0acbdd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183090"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a><span data-ttu-id="7bcba-103">Regression Suite Automation Tool のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="7bcba-103">Regression Suite Automation Tool installation and configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7bcba-104">このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-104">This topic contains information about how install and configure the Regression suite automation tool (RSAT).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7bcba-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="7bcba-105">Prerequisites</span></span>

### <a name="test-environment"></a><span data-ttu-id="7bcba-106">テスト環境</span><span class="sxs-lookup"><span data-stu-id="7bcba-106">Test environment</span></span>
<span data-ttu-id="7bcba-107">テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-107">Your test environment must be running Platform update 15 or newer.</span></span> <span data-ttu-id="7bcba-108">Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-108">The Regression suite automation tool must have access to your test environment via a web browser.</span></span>  

### <a name="excel"></a><span data-ttu-id="7bcba-109">Excel</span><span class="sxs-lookup"><span data-stu-id="7bcba-109">Excel</span></span>
<span data-ttu-id="7bcba-110">テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-110">You need Microsoft Excel installed to generate and edit test parameters.</span></span> 

### <a name="azure-devops"></a><span data-ttu-id="7bcba-111">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="7bcba-111">Azure DevOps</span></span>
<span data-ttu-id="7bcba-112">テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bcba-112">You must have an Azure DevOps project to store and manage your test cases, test plans, and test case results.</span></span> <span data-ttu-id="7bcba-113">Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bcba-113">You will need an Azure DevOps Test Manager or Test Plans license.</span></span> <span data-ttu-id="7bcba-114">たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。</span><span class="sxs-lookup"><span data-stu-id="7bcba-114">For example, if you have a Visual Studio Enterprise subscription, you already have a license to Test Plans.</span></span> <span data-ttu-id="7bcba-115">詳細については、 [Azure DevOps の価格設定](https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-115">For more information, see [Pricing for Azure DevOps](https://azure.microsoft.com/en-us/pricing/details/devops/azure-devops-services/).</span></span>

### <a name="authentication-certificate"></a><span data-ttu-id="7bcba-116">認証証明書</span><span class="sxs-lookup"><span data-stu-id="7bcba-116">Authentication Certificate</span></span>
<span data-ttu-id="7bcba-117">RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザを介して環境にリモート接続するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="7bcba-117">RSAT is designed to be installed on any Windows 10 computer and connect remotely via a web browser to a an environment.</span></span>

![クライアント コンピュータと環境](media/client-environment.png)

<span data-ttu-id="7bcba-119">セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-119">To enable secure authentication, RSAT requires a certificate to be installed on the RSAT client computer.</span></span> <span data-ttu-id="7bcba-120">RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-120">The RSAT settings dialog box allows you to automatically create and install the authentication certificate.</span></span> <span data-ttu-id="7bcba-121">また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-121">You will also need to configure the virtual machine (VM) to trust the connection.</span></span> <span data-ttu-id="7bcba-122">RSATをインストールして構成するには、次のセクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-122">Follow the instructions in the next sections to install and configure RSAT.</span></span>

## <a name="installation"></a><span data-ttu-id="7bcba-123">インストール</span><span class="sxs-lookup"><span data-stu-id="7bcba-123">Installation</span></span>

### <a name="installer"></a><span data-ttu-id="7bcba-124"> インストーラー</span><span class="sxs-lookup"><span data-stu-id="7bcba-124">Installer</span></span>
<span data-ttu-id="7bcba-125">**Regression Suite Automation Tool.msi** をマシンにダウンロードし、ダブルクリックして、インストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-125">Download **Regression Suite Automation Tool.msi** to your machine and double-click it to run the installer.</span></span> 

![ インストーラー](media/download-msi.png)
 
### <a name="selenium-and-browser-drivers"></a><span data-ttu-id="7bcba-127">Selenium およびブラウザー ドライバー</span><span class="sxs-lookup"><span data-stu-id="7bcba-127">Selenium and Browser Drivers</span></span>
<span data-ttu-id="7bcba-128">RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bcba-128">RSAT requires Selenium and web browser driver libraries.</span></span> <span data-ttu-id="7bcba-129">RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-129">RSAT will prompt you if needed libraries are missing and will automatically install them for you.</span></span> <span data-ttu-id="7bcba-130">次の (または類似の) メッセージが表示されたら、はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-130">Select Yes when you see the following (or similar) messages.</span></span>
 
![Selenium ドライバー](media/driver-1.png)
 
![ブラウザー ドライバー](media/driver-2.png)

<span data-ttu-id="7bcba-133">または、 [Selenium ドライバーのインストール](#install-selenium-drivers) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-133">Alternatively, refer to [Install Selenium Driver](#install-selenium-drivers).</span></span>

## <a name="configuration"></a><span data-ttu-id="7bcba-134">構成</span><span class="sxs-lookup"><span data-stu-id="7bcba-134">Configuration</span></span>

<span data-ttu-id="7bcba-135">デスクトップから RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-135">Open RSAT from your desktop.</span></span>

![RSAT デスクトップ アイコン](media/desktop-icon.png)
 
<span data-ttu-id="7bcba-137">RSATを構成するには、右上の **設定** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-137">Select **Settings** button in the upper right to configure RSAT.</span></span>

![RSAT 設定](media/rsat-settings.png)

### <a name="general-settings"></a><span data-ttu-id="7bcba-139">一般設定</span><span class="sxs-lookup"><span data-stu-id="7bcba-139">General settings</span></span>
<span data-ttu-id="7bcba-140">これらの設定は必須です。</span><span class="sxs-lookup"><span data-stu-id="7bcba-140">These settings are required.</span></span>

#### <a name="azure-devops"></a><span data-ttu-id="7bcba-141">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="7bcba-141">Azure DevOps</span></span>
<span data-ttu-id="7bcba-142">Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-142">Configure your connection to the Azure DevOps project and test plan.</span></span>

+ <span data-ttu-id="7bcba-143">**Azure DevOps URL** - これは、 Azure DevOps 組織のURLです。</span><span class="sxs-lookup"><span data-stu-id="7bcba-143">**Azure DevOps Url** - This is the URL of your Azure DevOps organization.</span></span> <span data-ttu-id="7bcba-144">たとえば、https://yourAzureDevOpsUrlHere.visualStudio.com。</span><span class="sxs-lookup"><span data-stu-id="7bcba-144">For example, https://yourAzureDevOpsUrlHere.visualStudio.com.</span></span>
+ <span data-ttu-id="7bcba-145">**アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。</span><span class="sxs-lookup"><span data-stu-id="7bcba-145">**Access Token** - The access token that allows the tool to connect to Azure DevOps.</span></span> <span data-ttu-id="7bcba-146">個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-146">You need to create a Personal Access Token or use an existing one that you have saved.</span></span> <span data-ttu-id="7bcba-147">詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/en-us/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-147">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/en-us/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span> 
+ <span data-ttu-id="7bcba-148">**プロジェクト名** - Azure DevOps プロジェクトの名前。</span><span class="sxs-lookup"><span data-stu-id="7bcba-148">**Project Name** - The name of your Azure DevOps project.</span></span> <span data-ttu-id="7bcba-149">RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-149">RSAT will automatically detect project names and test plans available based the Azure DevOps URL specified.</span></span> <span data-ttu-id="7bcba-150">その後、テスト プロジェクトおよびテスト計画を選択できます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-150">You can then select the Test Project and Test Plan.</span></span>
+ <span data-ttu-id="7bcba-151">**テスト計画** - テスト ケースを含む Azure DevOps テスト計画</span><span class="sxs-lookup"><span data-stu-id="7bcba-151">**Test Plan** - The Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="7bcba-152">詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/en-us/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-152">For more information, see [Create test plans and test suites](https://www.visualstudio.com/en-us/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> 

<span data-ttu-id="7bcba-153">**接続のテスト** を選択し、 Azure DevOps への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-153">Select **Test Connection** to test your connection to Azure DevOps.</span></span>

#### <a name="test-environment"></a><span data-ttu-id="7bcba-154">テスト環境</span><span class="sxs-lookup"><span data-stu-id="7bcba-154">Test Environment</span></span>
<span data-ttu-id="7bcba-155">テスト環境への接続をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-155">Configure your connection to the test environment.</span></span>

+ <span data-ttu-id="7bcba-156">**ホスト名** - テスト環境のホスト名。</span><span class="sxs-lookup"><span data-stu-id="7bcba-156">**Hostname** - Hostname of the test environment.</span></span> <span data-ttu-id="7bcba-157">たとえば、 <myaos>.cloudax.dynamics.comのようになります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-157">For example, <myaos>.cloudax.dynamics.com.</span></span> <span data-ttu-id="7bcba-158">https:// または http:/ の接頭辞を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-158">Do not include the https:// or http:/ prefix.</span></span>
+ <span data-ttu-id="7bcba-159">**SOAP ホスト名** - テスト環境のSOAP ホスト名。</span><span class="sxs-lookup"><span data-stu-id="7bcba-159">**SOAP Host Name** - SOAP Hostname of the test environment.</span></span> <span data-ttu-id="7bcba-160">通常、SOAP ホスト名は、soapの接尾語が付いたホスト名と同じです。</span><span class="sxs-lookup"><span data-stu-id="7bcba-160">The SOAP hostname is typically the same as the Hostname with a soap suffix.</span></span> <span data-ttu-id="7bcba-161">たとえば、 <myaos>soap.cloudax.dynamics.comのようになります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-161">For example, <myaos>soap.cloudax.dynamics.com.</span></span> <span data-ttu-id="7bcba-162">https:// または http:/ の接頭辞を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-162">Do not include the https:// or http:/ prefix.</span></span>
+ <span data-ttu-id="7bcba-163">**管理者ユーザー名** - テスト環境での管理者ユーザーの電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="7bcba-163">**Admin User Name** - Email address of an admin user on the test environment.</span></span>
+ <span data-ttu-id="7bcba-164">**拇印**: 使用している認証証明書の拇印。</span><span class="sxs-lookup"><span data-stu-id="7bcba-164">**Thumbprint**: Thumbprint of the authentication certificate you are using.</span></span>
    1. <span data-ttu-id="7bcba-165">新しい証明書を作成してインストールするには、 **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-165">Select **New** to create and install a new authentication certificate.</span></span> <span data-ttu-id="7bcba-166">プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-166">When prompted, place the .cer file somewhere so you have it saved for your records.</span></span>
    2. <span data-ttu-id="7bcba-167">プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート ストアにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-167">When the process completes, the new certification is installed in the local machine’s trusted root store.</span></span>
        
        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. <span data-ttu-id="7bcba-169">新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-169">The thumbprint of the newly created certificate is automatically inserted on this form.</span></span> <span data-ttu-id="7bcba-170">この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-170">Copy this thumbprint, you will use it in the next section to configure the AOS to trust the connection.</span></span>

+ <span data-ttu-id="7bcba-171">**会社名** - Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-171">**Company name** - Specify a company name to use as your default company during creation of Excel pParameters files.</span></span> <span data-ttu-id="7bcba-172">後でExcelファイルを編集して変更できます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-172">It can be changed later by editing an Excel file.</span></span>


#### <a name="run-setting"></a><span data-ttu-id="7bcba-173">実行設定</span><span class="sxs-lookup"><span data-stu-id="7bcba-173">Run setting</span></span>
<span data-ttu-id="7bcba-174">ローカル設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-174">Configure your local settings.</span></span>

+ <span data-ttu-id="7bcba-175">**作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。</span><span class="sxs-lookup"><span data-stu-id="7bcba-175">**Working directory** - Folder location for storing test automation files, including Excel test data files.</span></span> <span data-ttu-id="7bcba-176">たとえば、 **C:\Temp\RegressionTool** のようになります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-176">For example: **C:\Temp\RegressionTool**.</span></span>
+ <span data-ttu-id="7bcba-177">**既定のブラウザー** - テストの実行に使用するブラウザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-177">**Default browser** - Select the browser to use for test execution.</span></span>

<span data-ttu-id="7bcba-178">**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-178">Select **Ok** to apply your settings and close the dialog box.</span></span> <span data-ttu-id="7bcba-179">**キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-179">Select **Cancel** to cancel your changes and close the dialog.</span></span> <span data-ttu-id="7bcba-180">**名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-180">The **Save As** and **Open** buttons allow you to save your settings for reuse later.</span></span> <span data-ttu-id="7bcba-181">**名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-181">Select **Save As** to save your current settings into a configuration file on your computer.</span></span> <span data-ttu-id="7bcba-182">**開く** を選択して、構成ファイルから設定を復元します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-182">Select **Open** to restore your settings from a configuration file.</span></span>

### <a name="optional-settings"></a><span data-ttu-id="7bcba-183">オプション設定</span><span class="sxs-lookup"><span data-stu-id="7bcba-183">Optional Settings</span></span>
<span data-ttu-id="7bcba-184">**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-184">Select the **Optional** tab to configure optional settings.</span></span>

+ <span data-ttu-id="7bcba-185">**テスト実行 プレフィックス** - RSATはテストの実行結果を Azure DevOps に報告します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-185">**Test Run Prefix** - RSAT reports test run results to Azure DevOps.</span></span> <span data-ttu-id="7bcba-186">テストの実行には、次の規則: **<Run ID> <Prefix> <Test Suite>** に従って名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-186">Test runs are named using the following convention: **<Run ID> <Prefix> <Test Suite>**.</span></span> <span data-ttu-id="7bcba-187">この設定を使用して **<Prefix>** を設定します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-187">Use this setting to set the **<Prefix>**.</span></span>
+ <span data-ttu-id="7bcba-188">**テスト実行 タイムアウト** - テストの実行のタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="7bcba-188">**Test Run Timeout** - Timeout (in minutes) of a test run.</span></span> <span data-ttu-id="7bcba-189">このタイムアウトに達すると、すべてのアクティブなウィンドウは閉じられ、保留中のテスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-189">All active windows are closed and pending test cases fail when this timeout is reached.</span></span>
+ <span data-ttu-id="7bcba-190">**テスト アクション タイムアウト** - 個々のテスト ステップのタイムアウト (分単位)。</span><span class="sxs-lookup"><span data-stu-id="7bcba-190">**Test Action Timeout** - Timeout (in minutes) of individual test steps.</span></span> <span data-ttu-id="7bcba-191">テストステップがタイムアウトになると、テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-191">When a test step times out, the test case fails.</span></span>

### <a name="configure-the-aos-machine-to-trust-the-connection"></a><span data-ttu-id="7bcba-192">接続を信頼するように AOS マシンを構成する</span><span class="sxs-lookup"><span data-stu-id="7bcba-192">Configure the AOS machine to trust the connection</span></span>
<span data-ttu-id="7bcba-193">証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-193">After creating the certificate, configure AOS to trust the test automation connection.</span></span> <span data-ttu-id="7bcba-194">マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-194">On a multi-AOS environment, repeat the following steps for all AOS machines.</span></span>

1.  <span data-ttu-id="7bcba-195">AOSマシンへのリモート デスクトップ接続を開きます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-195">Open a Remote Desktop connection to the AOS machine.</span></span>
2.  <span data-ttu-id="7bcba-196">IIS を開き、サイトの一覧で AOSService を見つけます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-196">Open IIS and find AOSService in the list of sites.</span></span>

    ![IISでのAOSの検索](media/configure-aos.png)

3.  <span data-ttu-id="7bcba-198">**AOSservice** を右クリックし、 **エクスプローラー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-198">Right-click **AOSService**, then click **Explore**.</span></span>
4.  <span data-ttu-id="7bcba-199">ファイル **wif.config** を開き、検索します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-199">Open and find the file **wif.config**.</span></span>
  
    ![wif.config を開く](media/open-wif-config.png)

5.  <span data-ttu-id="7bcba-201">次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-201">Update the **wif.config** file by adding a new authority entry, as shown in the following example.</span></span> <span data-ttu-id="7bcba-202">機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-202">Use **127.0.0.1** for the authority name and paste your certificate thumbprint.</span></span>

```
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

## <a name="installation-on-multiple-machines"></a><span data-ttu-id="7bcba-203">複数のマシンへのインストール</span><span class="sxs-lookup"><span data-stu-id="7bcba-203">Installation on multiple machines</span></span>
<span data-ttu-id="7bcba-204">複数のコンピューターにRSATをインストールする場合は、RSATインストールごとに新しい証明書を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-204">If you install RSAT on more than one computer, you need to generate a new certificate for every RSAT installation.</span></span> <span data-ttu-id="7bcba-205">証明書を生成し、RSATと同じコンピューターにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-205">The certificate must be generated and installed on the same computer as RSAT.</span></span> <span data-ttu-id="7bcba-206">RSATがインストールされている複数のクライアントからの接続をAOSに信頼させる場合、AOS wif.config ファイルに複数の拇印エントリを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-206">You can have more than one thumbprint entry in the AOS wif.config file if you want your AOS to trust connections from more than one client where RSAT is installed.</span></span> <span data-ttu-id="7bcba-207">次の例は、複数の拇印ノードを示しています。</span><span class="sxs-lookup"><span data-stu-id="7bcba-207">The following example shows multiple thumbprints nodes.</span></span>

```
<keys>
    <add thumbprint="ccbc124d0a119xxxxxxxxxxxxxxxxxxxx841e797" />
    <add thumbprint="bbbbbbbbbbbbbbxxxxxxxxxxxxxxxxxxxx999999" />
</keys>
```

## <a name="install-selenium-drivers"></a><span data-ttu-id="7bcba-208">Selenium ドライバーのインストール</span><span class="sxs-lookup"><span data-stu-id="7bcba-208">Install Selenium drivers</span></span>

<span data-ttu-id="7bcba-209">Selenium ドライバーを手動でインストールするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7bcba-209">For manual installation of Selenium drivers, follow these steps:</span></span>
1. <span data-ttu-id="7bcba-210">[Selenium 3.13.1](http://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-210">Download [Selenium 3.13.1](http://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip).</span></span> <span data-ttu-id="7bcba-211">または、 http://docs.seleniumhq.org/download に移動し、 **以前のリリース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-211">Or, go to http://docs.seleniumhq.org/download and click **Previous releases**.</span></span> <span data-ttu-id="7bcba-212">**3.13** を選択して、 **selenium-dotnet-strongnamed-3.13.1.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-212">Choose **3.13** and download **selenium-dotnet-strongnamed-3.13.1.zip**.</span></span>
2. <span data-ttu-id="7bcba-213">Selenium ライブラリをインストールします:</span><span class="sxs-lookup"><span data-stu-id="7bcba-213">Install the Selenium libraries:</span></span>
    + <span data-ttu-id="7bcba-214">ダウンロード ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-214">Unzip the downloaded file.</span></span> 
    + <span data-ttu-id="7bcba-215">ファイル **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg** を展開します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-215">Unpack the file **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg**.</span></span> <span data-ttu-id="7bcba-216">このファイルを展開するには、ファイルに .zip拡張子を追加して、解凍します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-216">To unpack this file, add the .zip suffix to the file and unzip it.</span></span> 
    + <span data-ttu-id="7bcba-217">**Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** という名前のフォルダーの内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-217">Copy the contents of the folder named **Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>
3.  <span data-ttu-id="7bcba-218">[Internet Explorer ドライバー バージョン 3.4.0](http://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-218">Download the [Internet Explorer driver version 3.4.0](http://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip).</span></span> <span data-ttu-id="7bcba-219">または、ブラウザーに戻り、 **3.4** フォルダを開いて、 **IEDriverServer_x64_3.4.0.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-219">Or, go back in the browser, open the **3.4** folder and download **IEDriverServer_x64_3.4.0.zip**.</span></span>
4.  <span data-ttu-id="7bcba-220">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-220">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

<span data-ttu-id="7bcba-221">Google Chromeをブラウザーとして使用するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="7bcba-221">If you want to use Google Chrome as your browser, follow these steps:</span></span>
1. <span data-ttu-id="7bcba-222">https://sites.google.com/a/chromium.org/chromedriver/downloads に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-222">Go to https://sites.google.com/a/chromium.org/chromedriver/downloads.</span></span> 
2. <span data-ttu-id="7bcba-223">最新/現在のリリースから **chromedriver_win32.zip** をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-223">Download **chromedriver_win32.zip** from the latest/current release.</span></span>
3. <span data-ttu-id="7bcba-224">ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-224">Unzip the downloaded file and move the contents to **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium**.</span></span>

## <a name="manual-configuration-of-authentication-certificates"></a><span data-ttu-id="7bcba-225">認証証明書の手動構成</span><span class="sxs-lookup"><span data-stu-id="7bcba-225">Manual configuration of authentication certificates</span></span>

<span data-ttu-id="7bcba-226">必要に応じて、RSAT認証証明書を手動で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-226">Optionally, you can manually configure the RSAT authentication certificate.</span></span>

<span data-ttu-id="7bcba-227">このプロセスに精通していない場合は、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-227">If you are not familiar with this process, get help from your system administrator.</span></span> <span data-ttu-id="7bcba-228">Windows キットがコンピューターにインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bcba-228">Make sure you have Windows Kits installed on your machine.</span></span> <span data-ttu-id="7bcba-229">Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-229">If you do not have Windows Kits installed on your machine, you can download the Windows 10 SDK from [Windows 10 SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk).</span></span> <span data-ttu-id="7bcba-230">このドキュメントで説明されている手順には、これらのコンポーネントが必要です。</span><span class="sxs-lookup"><span data-stu-id="7bcba-230">You will need these components for the steps described in this document.</span></span>

+ <span data-ttu-id="7bcba-231">デスクトップ アプリ用の Windows SDK 署名ツール</span><span class="sxs-lookup"><span data-stu-id="7bcba-231">Windows SDK Signing Tools for Desktop Apps</span></span>
+ <span data-ttu-id="7bcba-232">UWP マネージド アプリ用のWindows SDK。</span><span class="sxs-lookup"><span data-stu-id="7bcba-232">Windows SDK for UWP Managed Apps.</span></span>

### <a name="generate-the-certificate"></a><span data-ttu-id="7bcba-233">証明書を生成する</span><span class="sxs-lookup"><span data-stu-id="7bcba-233">Generate the certificate</span></span>

<span data-ttu-id="7bcba-234">RSAT クライアント コンピュータで証明書ファイルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-234">You must generate the certificate file on the RSAT client computer.</span></span> <span data-ttu-id="7bcba-235">**証明書は、テスト ツールを実行している同じコンピュータで生成する必要があります。**</span><span class="sxs-lookup"><span data-stu-id="7bcba-235">**The certificate must be generated on the same computer that the test tool is running on.**</span></span> <span data-ttu-id="7bcba-236">証明書ファイルを生成するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="7bcba-236">To generate the certificate file, follow these steps:</span></span>
1. <span data-ttu-id="7bcba-237">コンピューター上にまだ存在しない場合は、 **C:\Temp** フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-237">Create the **C:\Temp** folder if it does not already exist on your computer.</span></span>
2. <span data-ttu-id="7bcba-238">管理者としてコマンド ライン ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-238">Open a command line window as Administrator.</span></span>
3. <span data-ttu-id="7bcba-239">Windows SDKをインストールしたフォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-239">Go to the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="7bcba-240">正確なフォルダは、Windows SDKをインストールした場所によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-240">Your exact folder may be different, depending on where you have installed the windows SDK).</span></span> <span data-ttu-id="7bcba-241">Windows キット 8.1を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="7bcba-241">You can also use Windows Kits 8.1.</span></span>

    ```
    cd c:\Program Files (x86)\Windows Kits\10\bin\10.0.17763.0\x64
    ```

4. <span data-ttu-id="7bcba-242">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-242">Run the following command.</span></span> <span data-ttu-id="7bcba-243">秘密キー パスワードを要求するプロンプトが表示されたら、 **なし** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-243">When you are prompted to enter a private key password, enter **None**.</span></span> 

    ```
    makecert.exe -n "CN=127.0.0.1" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 c:\temp\authCert.cer
    ````

### <a name="install-the-certificate-to-the-trusted-root"></a><span data-ttu-id="7bcba-244">信頼済ルートに証明書をインストールする</span><span class="sxs-lookup"><span data-stu-id="7bcba-244">Install the certificate to the Trusted Root</span></span>

<span data-ttu-id="7bcba-245">証明書をインストールするには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="7bcba-245">To install the certificate, follow these steps:</span></span>

1. <span data-ttu-id="7bcba-246">証明書をインストールするには、 **authCert.cer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-246">Double-click **authCert.cer** to install the certificate.</span></span>
2. <span data-ttu-id="7bcba-247">**証明書のインストール** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-247">Click **Install Certificate**.</span></span>
3. <span data-ttu-id="7bcba-248">**ローカルマシン > すべての証明書を次のストアにを配置 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-248">Select **Local Machine > Place all certificates in the following Store > Browse > Trusted Root Certification Authorities** and click **Next** through each screen.</span></span>
4. <span data-ttu-id="7bcba-249">**パスワード** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="7bcba-249">Leave the **Password** field blank.</span></span>
5. <span data-ttu-id="7bcba-250">**証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-250">In the **Certificate** dialog box, browse to **Details** and look for **Thumbprint**.</span></span>

    ![拇印の一覧が表示された証明書ダイアログ](media/certificate-dialog.png)
 
6. <span data-ttu-id="7bcba-252">拇印をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="7bcba-252">Copy and save the thumbprint.</span></span> <span data-ttu-id="7bcba-253">このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bcba-253">You will need it to configure the AOS as described earlier in this topic.</span></span>
