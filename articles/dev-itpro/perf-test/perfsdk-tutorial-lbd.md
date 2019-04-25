---
title: オンプレミス環境でのパフォーマンス SDK およびマルチユーザー テスト
description: このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) を使用して、オンプレミス環境でマルチユーザー負荷テストを実行する方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 03/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: Platform update 19
ms.openlocfilehash: 0985bae74ed1032b8dfdef58fa7d4fa224d99c26
ms.sourcegitcommit: c19d9cb1f1e77ce96ac4ec6e3212bc3c06288a7d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2019
ms.locfileid: "892571"
---
# <a name="performance-sdk-and-multiuser-testing-in-on-premises-environments"></a><span data-ttu-id="fd1d0-103">オンプレミス環境でのパフォーマンス SDK およびマルチユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="fd1d0-103">Performance SDK and multiuser testing in on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd1d0-104">このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) を使用して、オンプレミス環境でマルチユーザー負荷テストを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-104">This topic explains how to use the Performance software development kit (SDK) to do multiuser load testing in an on-premises environment.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="fd1d0-105">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-105">Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</span></span> <span data-ttu-id="fd1d0-106">将来的には、代替ソリューションに向けた推奨案の提案に取り組んでいきます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-106">In the future, we will be publishing some recommendations for alternative solutions.</span></span>  
  
  > - <span data-ttu-id="fd1d0-107">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-107">If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="fd1d0-108">サポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-108">You can continue using it until the end of support cycle.</span></span> 
 
 >  - <span data-ttu-id="fd1d0-109">クラウド ベースの負荷テストサービスをご利用の場合は、同サービスは2020年3月31日までの間、継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-109">If you are using the cloud-based load testing service, the cloud-based load testing service will continue to run through March 31, 2020.</span></span> <span data-ttu-id="fd1d0-110">それまでの間は、同サービスの全機能を継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-110">Until then, you can continue to use all of the experiences powered by this service without interruption.</span></span> <span data-ttu-id="fd1d0-111">また、オンプレミス負荷テストに切り替えることがも可能です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-111">Alternatively, you can switch to on-premises load testing.</span></span> 
 
 > <span data-ttu-id="fd1d0-112">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-112">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>


## <a name="prerequisites"></a><span data-ttu-id="fd1d0-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="fd1d0-113">Prerequisites</span></span>

- <span data-ttu-id="fd1d0-114">数量データのあるオンプレミス環境</span><span class="sxs-lookup"><span data-stu-id="fd1d0-114">An on-premises environment that has volume data</span></span>
- <span data-ttu-id="fd1d0-115">以下の特性を持つ開発環境。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-115">A development environment that has the following characteristics:</span></span>

    - <span data-ttu-id="fd1d0-116">Microsoft Visual Studio 2015 Enterprise 以降のバージョンがインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-116">Microsoft Visual Studio 2015 Enterprise or a later version is installed.</span></span>
    - <span data-ttu-id="fd1d0-117">パフォーマンス SDK をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-117">The Performance SDK is installed.</span></span> <span data-ttu-id="fd1d0-118">(SDK は K:\\PerfSDK\\PerfSDKLocalDirectory にある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-118">(The SDK will likely be in K:\\PerfSDK\\PerfSDKLocalDirectory.</span></span> <span data-ttu-id="fd1d0-119">ただし、環境によっては C:\\PerfSDK のような別の場所にある可能性があります。)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-119">However, depending on your environment, it might be in another location, such as C:\\PerfSDK.)</span></span>
    - <span data-ttu-id="fd1d0-120">オンプレミス環境は、Web ブラウザーでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-120">The on-premises environment can be accessed in a web browser.</span></span> <span data-ttu-id="fd1d0-121">(オンプレミス環境と同じドメインに開発仮想マシン [VM]が、またはオンプレミス環境には、パブリックに登録済みのドメイン名がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-121">(The development virtual machine [VM] might be in the same domain as the on-premises environment, or the on-premises environment might have a publicly registered domain name.)</span></span>

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a><span data-ttu-id="fd1d0-122">XML 記録からシングル ユーザー C# テストを作成する</span><span class="sxs-lookup"><span data-stu-id="fd1d0-122">Create a single-user C# test from an XML recording</span></span>

<!--To view a video that shows how to create a single-user test, go to [https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3).-->

1. <span data-ttu-id="fd1d0-123">タスク レコーダーを使用して、テストするシナリオの記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-123">Use Task recorder to create a recording of the scenario that you want to test.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fd1d0-124">タスク記録は、既定のダッシュボード ページで開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-124">Your task recording must start on the default dashboard page.</span></span> <span data-ttu-id="fd1d0-125">それ以外の場合は、テストを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-125">Otherwise, the test won't be able to run.</span></span>

2. <span data-ttu-id="fd1d0-126">Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-126">Start Microsoft Visual Studio as an administrator, and build the **PerfSDKSample** project.</span></span> <span data-ttu-id="fd1d0-127">このプロジェクトは **PerfSDK** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-127">This project is in the **PerfSDK** folder.</span></span> <span data-ttu-id="fd1d0-128">プロジェクトを既に構築している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-128">If you've already built the project, skip this step.</span></span>
3. <span data-ttu-id="fd1d0-129">**Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-129">Select **Dynamics 365** &gt; **Addins** &gt; **Create C# perf test from recording**.</span></span>
4. <span data-ttu-id="fd1d0-130">**タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-130">In the **Import Task Recording** dialog box, enter the required details, and then select **Import**.</span></span>

    <span data-ttu-id="fd1d0-131">[![インポート タスク記録 ダイアログ ボックス](./media/perf103a.png)](./media/perf103a.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-131">[![Import Task Recording dialog box](./media/perf103a.png)](./media/perf103a.png)</span></span>

    <span data-ttu-id="fd1d0-132">C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-132">A C# test is generated in the Generated folder for the project that you selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd1d0-133">コンパイルの問題を解決するために、生成されたテストは編集される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-133">The test that is generated might have to be edited to resolve any compilation issues.</span></span>

## <a name="run-a-single-user-test-by-using-the-performance-sdk"></a><span data-ttu-id="fd1d0-134">パフォーマンス SDK を使用して単一のユーザーテストを実行</span><span class="sxs-lookup"><span data-stu-id="fd1d0-134">Run a single-user test by using the Performance SDK</span></span>

### <a name="prepare-the-development-environment"></a><span data-ttu-id="fd1d0-135">開発環境の準備</span><span class="sxs-lookup"><span data-stu-id="fd1d0-135">Prepare the development environment</span></span>
<span data-ttu-id="fd1d0-136">開発環境でこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-136">Follow these steps in the development environment.</span></span>

1. <span data-ttu-id="fd1d0-137">Microsoft Windows のコントロール パネルで、**システムとセキュリティ**  &gt; **システム** &gt; **システムの詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-137">In Control Panel in Microsoft Windows, select **System and Security** &gt; **System** &gt; **Advanced System Settings**.</span></span> <span data-ttu-id="fd1d0-138">**TestRoot**環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-138">Verify that the **TestRoot** environment variable is set to the path of the PerfSDK folder.</span></span>

    <span data-ttu-id="fd1d0-139">[![TestRoot 環境変数](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-139">[![TestRoot environment variable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span></span>

2. <span data-ttu-id="fd1d0-140">[http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードし、ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-140">Download the **selenium-dotnet-strongnamed-2.42.0.zip** and **IEDriverServer\_Win32\_2.42.0.zip** files from [http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/), and extract the files.</span></span>
3. <span data-ttu-id="fd1d0-141">動的リンク ライブラリ (DLL) を、**selenium-dotnet-strongnamed-2.42.0.zip\net40** フォルダから **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-141">Copy the dynamic-link libraries (DLLs) from the **selenium-dotnet-strongnamed-2.42.0.zip\net40** folder to the **PerfSDK\\Common\\External\\Selenium** folder.</span></span> <span data-ttu-id="fd1d0-142">**IEDriverServer.exe** を **IEDriverServer\_Win32\_2.42.0.zip** から **PerfSDK\\Common\\External\\Selenium** フォルダーにもコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-142">Also copy the **IEDriverServer.exe** from the **IEDriverServer\_Win32\_2.42.0.zip** to the **PerfSDK\\Common\\External\\Selenium** folder.</span></span>

    <span data-ttu-id="fd1d0-143">[![PerfSDK\Common\External\Selenium フォルダーにある DLL](./media/perf103d.png)](./media/perf103d.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-143">[![DLLs in the PerfSDK\Common\External\Selenium folder](./media/perf103d.png)](./media/perf103d.png)</span></span>

4. <span data-ttu-id="fd1d0-144">テストの認証に使用する証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-144">Generate a certificate to use for authentication for the tests.</span></span> <span data-ttu-id="fd1d0-145">証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-145">To generate a certificate file, open a Command Prompt window as an administrator, and run the following commands.</span></span> <span data-ttu-id="fd1d0-146">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-146">When you're prompted for a private key password, select **None**.</span></span>

    ```
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="fd1d0-147">これらのコマンドでは次の要素を注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-147">Note the following elements in these commands:</span></span>

    - <span data-ttu-id="fd1d0-148">**-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-148">**-n "CN=127.0.0.1"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="fd1d0-149">証明書の名前には、**127.0.0.1** が必要です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-149">The name of this certificate must be **127.0.0.1**.</span></span> <span data-ttu-id="fd1d0-150">それ以外の場合は、単一ユーザー テストは実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-150">Otherwise, the single-user tests won't be able to run.</span></span>
    - <span data-ttu-id="fd1d0-151">**-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-151">**-eku 1.3.6.1.5.5.7.3.1** gives the purpose of the certificate.</span></span> <span data-ttu-id="fd1d0-152">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-152">It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</span></span>

    <span data-ttu-id="fd1d0-153">スクリプトの実行が終了した後、**c:\\Temp** で以下のファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-153">After the script has finished running, you should see the following files in **C:\\Temp**:</span></span>

    - <span data-ttu-id="fd1d0-154">authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="fd1d0-154">authcert.pfx</span></span>
    - <span data-ttu-id="fd1d0-155">authcert.cer</span><span class="sxs-lookup"><span data-stu-id="fd1d0-155">authcert.cer</span></span>
    - <span data-ttu-id="fd1d0-156">authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="fd1d0-156">authcert.pvk</span></span>

5. <span data-ttu-id="fd1d0-157">**authcert.pfx** 証明書ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-157">Install the **authcert.pfx** certificate file.</span></span> <span data-ttu-id="fd1d0-158">ファイルをインストールするときは、**ローカル コンピューター**を必ず選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-158">When you install the file, make sure that you select **Local Machine**.</span></span>
6. <span data-ttu-id="fd1d0-159">**authcert.pfx** ファイルを **PerfSDK** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-159">Copy the **authcert.pfx** file to the **PerfSDK** folder.</span></span>
7. <span data-ttu-id="fd1d0-160">管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-160">Open a Microsoft Windows PowerShell window as an administrator, and run the following commands to get the thumbprint of the installed certificate.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

8. <span data-ttu-id="fd1d0-161">Visual Studio で、**PerfSDK** フォルダにある **PerfSDKSample** プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-161">In Visual Studio, open the **PerfSDKSample** project that is in the **PerfSDK** folder.</span></span>
9. <span data-ttu-id="fd1d0-162">Visual Studio プロジェクトでは **PerfSDK\\Common\\External\\Selenium** フォルダーで **WebDriver.dll** への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-162">In the Visual Studio project, add a reference to the **WebDriver.dll** file in the **PerfSDK\\Common\\External\\Selenium** folder.</span></span>
10. <span data-ttu-id="fd1d0-163">**CloudEnvironment.Config** ファイルを開き、コンテンツを次のテンプレートに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-163">Open the **CloudEnvironment.Config** file, and replace the contents with the following template.</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <EnvironmentalConfigSettings xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <EnvironmentalConfigSettingsCollection>
            <EnvironmentalConfigSetting ConfigName="DEVFABRIC">
                <!-- NOTE: the HostName value needs to be specified -->
                <ExecutionConfigurations Key="HostName" Value="[yourD365FOdomain]/namespaces/AXSF" />
                <ExecutionConfigurations Key="SoapHostName" Value="[yourD365FOdomain]/namespaces/AXSF" />
                <ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="[ThumbprintFromPowerShell]" />
                <ExecutionConfigurations Key="AdminAuthenticatorConfigurationId" Value="SelfMintingAdminUser" />
                <ExecutionConfigurations Key="DefaultBrowser" Value="InternetExplorer" />
                <ExecutionConfigurations Key="FederationRealm" Value="spn:00000015-0000-0000-c000-000000000000" />
                <ExecutionConfigurations Key="DefaultDispatcher" Value="Microsoft.Dynamics.TestTools.Dispatcher.JsDispatcher, Microsoft.Dynamics.TestTools.Dispatcher.JsDispatcher" />
                <ExecutionConfigurationsNodes ConfigurationName="SVC">
                    <ConfigurationSpecificDetails Key="AppConfig" Value="DEVFABRIC.Config" />
                </ExecutionConfigurationsNodes>
                <ExecutionConfigurationsNodes ConfigurationName="PRF">
                    <ConfigurationSpecificDetails Key="IsAdfs" Value="True" />
                    <ConfigurationSpecificDetails Key="UserCount" Value="2" />
                    <ConfigurationSpecificDetails Key="UserFormat" Value="[AdminUserEmail]" />
                    <ConfigurationSpecificDetails Key="UserPassword" Value="[AdminUserPassword]" />
                    <ConfigurationSpecificDetails Key="UserRole" Value="-SYSADMIN-" />
                    <ConfigurationSpecificDetails Key="ThinkTime" Value="0" />
                    <ConfigurationSpecificDetails Key="Company" Value="USMF" />
                </ExecutionConfigurationsNodes>
            </EnvironmentalConfigSetting>
        </EnvironmentalConfigSettingsCollection>
        <AuthenticatorConfigurationCollection>
            <AuthenticatorConfiguration Id="SelfMintingRunnerUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <Credentials IsFromKeyVault="false" Username="daxrunneruser@daxmdsrunner.com" NetworkDomain="urn:Microsoft:Dynamics:Cloud:DaxRunner" />
            </AuthenticatorConfiguration>
            <AuthenticatorConfiguration Id="SelfMintingSysUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <Credentials IsFromKeyVault="false" Username="testuser@microsoft.com" />
            </AuthenticatorConfiguration>
            <AuthenticatorConfiguration Id="SelfMintingAdminUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <!-- NOTE: admin username needs to be specified -->
                <Credentials IsFromKeyVault="false" Username="[AdminUserEmail]" NetworkDomain="[AdfsUrl]" />
            </AuthenticatorConfiguration>
        </AuthenticatorConfigurationCollection>
    </EnvironmentalConfigSettings
    ```

11. <span data-ttu-id="fd1d0-164">**CloudEnvironment.Config** ファイルで、次のキーの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-164">In the **CloudEnvironment.Config** file, specify values for the following keys.</span></span> <span data-ttu-id="fd1d0-165">これらの値は、テンプレートの角かっこ内のプレース ホルダーの値を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-165">These values replace the placeholder values in square brackets in the template.</span></span>

    - <span data-ttu-id="fd1d0-166">**ホスト名** – Microsoft Dynamics 365 for Finance and Operations 設置環境へのアクセスに使用する URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-166">**HostName** – Specify the URL that is used to access your Microsoft Dynamics 365 for Finance and Operations on-premises environment.</span></span> <span data-ttu-id="fd1d0-167">URL は、**\[yourD365FOdomain\]/namespaces/AXSF** です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-167">The URL should be **\[yourD365FOdomain\]/namespaces/AXSF**.</span></span>
    - <span data-ttu-id="fd1d0-168">**SoapHostName** –**HostName** に指定したものと同じ URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-168">**SoapHostName** – Specify the same URL that you specified for **HostName**.</span></span>
    - <span data-ttu-id="fd1d0-169">**SelfSigningCertificateThumbprint** – 手順 7 で Windows PowerShell から取得した拇印を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-169">**SelfSigningCertificateThumbprint** – Specify the thumbprint that you retrieved from Windows PowerShell in step 7.</span></span>
    - <span data-ttu-id="fd1d0-170">**UserFormat** – Finance and Operations のオンプレミス環境でシステム管理者の役割を持つユーザーの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-170">**UserFormat** – Specify the email address of a user who has the System Administrator role in your Finance and Operations on-premises environment.</span></span> <span data-ttu-id="fd1d0-171">ユーザーは、Active Directory フェデレーション サービス (AD FS) ユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-171">The user must be an Active Directory Federation Services (AD FS) user.</span></span>
    - <span data-ttu-id="fd1d0-172">**UserPassword** –  **UserFormat** に指定した電子メール アドレスのユーザーのパスワードを指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-172">**UserPassword** – Specify the password of the user whose email address you specified for **UserFormat**.</span></span>
    - <span data-ttu-id="fd1d0-173">**Username** – **UserFormat** に指定したものと同じ電子メール アドレスを指定してください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-173">**Username** – Specify the same email address that you specified for **UserFormat**.</span></span>
    - <span data-ttu-id="fd1d0-174">**NetworkDomain** – AD FS ID プロバイダーの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-174">**NetworkDomain** – Specify the URL of the AD FS identity provider.</span></span> <span data-ttu-id="fd1d0-175">オンプレミス配置の **AXDB** データベースに対して次の SQL クエリを実行することにより、この値を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-175">You can find this value by running the following SQL query against the **AXDB** database of your on-premises deployment.</span></span>

        ```sql
        select NETWORKDOMAIN, NETWORKALIAS from USERINFO where NETWORKALIAS='[AdminUserEmail]'
        ```

### <a name="prepare-the-on-premises-environment"></a><span data-ttu-id="fd1d0-176">オンプレミス環境の準備</span><span class="sxs-lookup"><span data-stu-id="fd1d0-176">Prepare the on-premises environment</span></span>
<span data-ttu-id="fd1d0-177">オンプレミス配置の各アプリケーション オブジェクト サーバー (AOS) VM で以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-177">Follow these steps on each Application Object Server (AOS) VM in the on-premises deployment.</span></span>

1. <span data-ttu-id="fd1d0-178">このトピックの[開発環境の準備](#prepare-the-development-environment)セクションで作成した **authcert.cer** ファイルを AOS VM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-178">Copy the **authcert.cer** file that you created in the [Prepare the development environment](#prepare-the-development-environment) section of this topic to the AOS VM.</span></span>
2. <span data-ttu-id="fd1d0-179">**authcert.cer** 証明書ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-179">Install the **authcert.cer** certificate file.</span></span> <span data-ttu-id="fd1d0-180">証明書をインストールするときは、**ローカル コンピューター**を必ず選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-180">When you install the certificate, make sure that you select **Local Machine**.</span></span> <span data-ttu-id="fd1d0-181">証明書を**信頼済ルート証明機関**ストアに置くようにしてください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-181">Also make sure that you put the certificate in the **Trusted Root Certification Authorities** store.</span></span>
3. <span data-ttu-id="fd1d0-182">**wif.config** ファイルをテキスト エディタで開きます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-182">Open the **wif.config** file in a text editor.</span></span> <span data-ttu-id="fd1d0-183">ファイルのパスは、**C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App19\\AXSF.Code.1.0.20180717001108** のようになります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-183">The path of the file will resemble **C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App19\\AXSF.Code.1.0.20180717001108**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd1d0-184">ファイル パスでは、使用している AOS ノードによって AOS 番号 (この例では**AOS1**) が異なります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-184">In the file path, the AOS number (**AOS1** in this example) will vary, depending on the AOS node that you're on.</span></span> <span data-ttu-id="fd1d0-185">さらに、**ProgramData** フォルダーは隠しフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-185">Additionally, the **ProgramData** folder is a hidden folder.</span></span> <span data-ttu-id="fd1d0-186">したがって、ファイル エクスプローラーでフォルダを表示するには、非表示のアイテムを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-186">Therefore, to see the folder in File Explorer, you must enable hidden items.</span></span>

4. <span data-ttu-id="fd1d0-187">**wif.config** ファイルで、`https://fakeacs.accesscontrol.windows.net` という機関を検索します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-187">In the **wif.config** file, find the authority that is named `https://fakeacs.accesscontrol.windows.net`.</span></span> <span data-ttu-id="fd1d0-188">この権限に対する拇印の一覧で、[開発環境の準備](#prepare-the-development-environment)セクションで作成した証明書の拇印を追加します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-188">In the list of thumbprints for this authority, add the thumbprint of the certificate that you created in the [Prepare the development environment](#prepare-the-development-environment) section.</span></span> <span data-ttu-id="fd1d0-189">次の例では、4 番目の拇印が `https://fakeacs.accesscontrol.windows.net` 権限に追加されました。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-189">In the following example, the fourth thumbprint has been added to the `https://fakeacs.accesscontrol.windows.net` authority.</span></span>

    ```xml
    <authority name="https://fakeacs.accesscontrol.windows.net/">
        <keys>
            <add thumbprint="9567B0F32F4B312FEE44ACE88A9CAAA13B7FBB86" />
            <add thumbprint="B8F659E2FDD2A6811CD72BE753FF7ACB64351AC1" />
            <add thumbprint="B51C394E6EE9578D8C54AE0A9927D8B6DCEFF84B" />
            <add thumbprint="F9112DE3D4DE65CBE39601EBDC7FBB1F8F525DED" />
        </keys>
        <validIssuers>
            <add name="https://fakeacs.accesscontrol.windows.net/" />
        </validIssuers>
    </authority>
    ```

5. <span data-ttu-id="fd1d0-190">**AXService.exe.config** ファイルをテキスト エディタで開きます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-190">Open the **AXService.exe.config** file in a text editor.</span></span> <span data-ttu-id="fd1d0-191">このファイルは、**wif.config** ファイルと同じディレクトリにあります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-191">You can find this file in the same directory as the **wif.config** file.</span></span>
6. <span data-ttu-id="fd1d0-192">**"Aos.AosRole"** の **AXService.exe.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-192">Search the **AXService.exe.config** file for **"Aos.AosRole"**.</span></span> <span data-ttu-id="fd1d0-193">**"Aos.AosRole"** を含む行を次の行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-193">Replace the line that contains **"Aos.AosRole"** with the following line.</span></span>

    ```xml
    <add key="Aos.AosRole" value="AosRoleUnknown" />
    ```

    > [!NOTE]
    > <span data-ttu-id="fd1d0-194">**AosRole** を **AosRoleUnknown** に設定すると、ユーザーごとの Web セッションの数の制限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-194">Setting the **AosRole** to **AosRoleUnknown** disables the limit on the number of web sessions per user.</span></span> <span data-ttu-id="fd1d0-195">負荷テストでは、単一のユーザーに対して多数のセッションが作成されるため、これは大規模なユーザー負荷で負荷テストを完了するために必要です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-195">This is necessary to complete load testing with a large user load because the load test will create many sessions for a single user.</span></span> <span data-ttu-id="fd1d0-196">負荷テストが完了したら、この値を **"AosRoleWeb"** にリセットします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-196">Once you are finished with your load testing, reset this value to **"AosRoleWeb"**.</span></span>


7. <span data-ttu-id="fd1d0-197">Service Fabric Explorer では、Microsoft Dynamics AX Application Object Server (AOS) ノードのための **Code** パッケージを検索し、省略記号ボタン (**...**) を選択し、Finance and Operations アプリケーションを再起動させるため**再起動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-197">In Service Fabric Explorer, find the **Code** package for the AOS node, select the ellipse button (**...**), and then select **Restart** to restart the Finance and Operations application.</span></span>

    ![Service Fabric Explorer から Finance and Operations を再起動](./media/ServiceFabricExplorerRestart.png)

### <a name="run-the-single-user-test"></a><span data-ttu-id="fd1d0-199">単一ユーザー テストを実行</span><span class="sxs-lookup"><span data-stu-id="fd1d0-199">Run the single-user test</span></span>

1. <span data-ttu-id="fd1d0-200">**PerfSDKSample** プロジェクトで、**PurchaseReq.cs** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-200">In the **PerfSDKSample** project, find the **PurchaseReq.cs** file.</span></span> <span data-ttu-id="fd1d0-201">このファイルは、サンプル シングルユーザー テストです。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-201">This file is a sample single-user test.</span></span> <span data-ttu-id="fd1d0-202">ファイルで、次の行をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-202">In the file, comment out the following lines.</span></span>

    ```
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    <span data-ttu-id="fd1d0-203">[![PurchaseReq.cs でコメント アウトされた行](./media/perf103e.png)](./media/perf103e.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-203">[![Lines commented out in PurchaseReq.cs](./media/perf103e.png)](./media/perf103e.png)</span></span>

2. <span data-ttu-id="fd1d0-204">**テスト** &gt; **テスト設定**を選択し、**既定のプロセッサ アーキテクチャ** フィールドを **x64** に設定して、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-204">Select **Test** &gt; **Test settings**, set the **Default processor architecture** field to **x64**, and then build the solution.</span></span>
3. <span data-ttu-id="fd1d0-205">**テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-205">Select **Test** &gt; **Windows** &gt; **Test Explorer** to view the list of tests.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd1d0-206">場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-206">Sometimes, Visual Studio might not update the list of tests after you create a test script from a task recording.</span></span> <span data-ttu-id="fd1d0-207">この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-207">In this case, restart Visual Studio, and then reopen Test Explorer.</span></span>

4. <span data-ttu-id="fd1d0-208">**CreatePurchReq** を右クリックして、サンプル シングルユーザー テストを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-208">Run the sample single-user test by right-clicking **CreatePurchReq**.</span></span> <span data-ttu-id="fd1d0-209">または、タスク記録から作成したテストを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-209">Alternatively, you can run the test that you created from your task recording.</span></span> <span data-ttu-id="fd1d0-210">テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-210">When you run the test, Internet Explorer should be started, and it should replay the scenario that you recorded.</span></span>

## <a name="run-a-multiuser-load-test-by-using-the-performance-sdk"></a><span data-ttu-id="fd1d0-211">パフォーマンス SDK を使用してマルチユーザー負荷テストを実行</span><span class="sxs-lookup"><span data-stu-id="fd1d0-211">Run a multiuser load test by using the Performance SDK</span></span>

### <a name="create-a-multiuser-test-from-a-single-user-test"></a><span data-ttu-id="fd1d0-212">シングル ユーザー テストからマルチ ユーザー テストを作成する</span><span class="sxs-lookup"><span data-stu-id="fd1d0-212">Create a multiuser test from a single-user test</span></span>

<span data-ttu-id="fd1d0-213">このトピックの前半の情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-213">After you create a single-user test by using the information earlier in this topic, you can convert it to a multiuser test.</span></span> <span data-ttu-id="fd1d0-214">テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-214">Add **MS.Dynamics.TestTools.UIHelpers.Core;** to your test script, and find the following line in the **TestSetup** method.</span></span>

```
Client = DispatchedClient.DefaultInstance;
```

<span data-ttu-id="fd1d0-215">その行を以下の行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-215">Replace that line with the following lines.</span></span>

```
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

<span data-ttu-id="fd1d0-216">タスクのインポーターによって生成されたテスト スクリプトには次の明細行と似ている明細行が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-216">The test script that was generated by the Task Importer might contain a line that resembles the following line.</span></span>

```
UserContextRole _context = new UserContextRole(UserManagement.AdminUser);
```

<span data-ttu-id="fd1d0-217">ロード テストとして実行される任意のテストからこの明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-217">Remove this line from any tests that will be run as load tests.</span></span> <span data-ttu-id="fd1d0-218">このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-218">This code is required only for single-user tests and has a negative effect on the performance of load tests.</span></span>

<span data-ttu-id="fd1d0-219">タスク記録が行われたときに入力した値がランダム化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-219">Make sure that the values that you entered when you made the task recording are randomized.</span></span>

### <a name="run-the-multiuser-load-test"></a><span data-ttu-id="fd1d0-220">マルチユーザー負荷テストを実行</span><span class="sxs-lookup"><span data-stu-id="fd1d0-220">Run the multiuser load test</span></span>

1. <span data-ttu-id="fd1d0-221">Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-221">In the Visual Studio editor, open the **ProcureToPay.cs** file, and append the following lines in the **TestSetup** method.</span></span>

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

2. <span data-ttu-id="fd1d0-222">[https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420)から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-222">Download the installer (.msi) file for Microsoft ODBC Driver 13 for SQL Server from [https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420).</span></span> <span data-ttu-id="fd1d0-223">(64 ビット バージョンの .msi ファイルを選択します。) ファイルを **PerfSDK** ディレクトリの **Visual Studio Online** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-223">(Select the 64-bit version of the .msi file.) Put the file in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
3. <span data-ttu-id="fd1d0-224">**Visual Studio Online** フォルダ内の **setup.cmd** ファイル内容を次のコードと一致するように変更します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-224">Modify the contents of the **setup.cmd** file in the **Visual Studio Online** folder so that they match the following code.</span></span>

    ```
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

4. <span data-ttu-id="fd1d0-225">**CloudCtuFakeACSInstall.cmd** ファイルの内容を変更して、**インポート**コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-225">Modify the contents of the **CloudCtuFakeACSInstall.cmd** file so that the **Import** command has an empty string instead of **'password'**.</span></span> <span data-ttu-id="fd1d0-226">スクリプトの 3 行目は、次の行に似ているはずです。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-226">The third line of the script should resemble the following line.</span></span>

    ```
    set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....
    ```

5. <span data-ttu-id="fd1d0-227">ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-227">In your solution files, double-click the **vsonline.testsettings** file to modify the test settings.</span></span>
6. <span data-ttu-id="fd1d0-228">**一般**タブの**テストの設定**ダイアログ ボックスで、**テストの実行場所**フィールドを**ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行**に設定します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-228">In the **Test Settings** dialog box, on the **General** tab, set the **Test run location** field to **Run tests using local computer or a test controller**.</span></span>
7. <span data-ttu-id="fd1d0-229">**配置**タブで、次の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-229">On the **Deployment** tab, use the following settings:</span></span>

    - <span data-ttu-id="fd1d0-230">**展開の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-230">Select the **Enable deployment** check box.</span></span>
    - <span data-ttu-id="fd1d0-231">**配置する追加のファイルやディレクトリ** フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-231">In the **Additional files and directories to deploy** field, make sure that the following files and directories are listed:</span></span>

        - <span data-ttu-id="fd1d0-232">&lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\</span><span class="sxs-lookup"><span data-stu-id="fd1d0-232">&lt;Solution Directory&gt;\\PerfSDKSample\\bin\\Debug\\</span></span>
        - <span data-ttu-id="fd1d0-233">C:\\PerfSDK\\CloudEnvironment.Config</span><span class="sxs-lookup"><span data-stu-id="fd1d0-233">C:\\PerfSDK\\CloudEnvironment.Config</span></span>
        - <span data-ttu-id="fd1d0-234">C:\\PerfSDK\\authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="fd1d0-234">C:\\PerfSDK\\authcert.pfx</span></span>
        - <span data-ttu-id="fd1d0-235">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span><span class="sxs-lookup"><span data-stu-id="fd1d0-235">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span></span>
        - <span data-ttu-id="fd1d0-236">C:\\PerfSDK\\ Visual Studio Online\\</span><span class="sxs-lookup"><span data-stu-id="fd1d0-236">C:\\PerfSDK\\Visual Studio Online\\</span></span>

        <span data-ttu-id="fd1d0-237">[![フィールドを配置するための追加ファイルおよびディレクトリ](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-237">[![Additional files and directories to deploy field](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span></span>

        > [!NOTE]
        > <span data-ttu-id="fd1d0-238">PerfSDK フォルダーが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-238">Your PerfSDK folder might differ.</span></span>

8. <span data-ttu-id="fd1d0-239">**設定とクリーンアップ** タブで、 **PerfSDK** ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-239">On the **Setup and Cleanup Scripts** tab, select the **setup.cmd** file that is in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
9. <span data-ttu-id="fd1d0-240">**ホスト**タブについて、**64 ビット コンピューターで 64 ビット プロセスのテストを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-240">On the **Hosts** tab, select **Run tests in 64 bit process on 64 bit machine**.</span></span>
10. <span data-ttu-id="fd1d0-241">テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-241">To run the test, open the **SampleLoadTest.loadtest** file, and select **Run Load Test**.</span></span>

    <span data-ttu-id="fd1d0-242">[![負荷テストの実行](./media/perf103u.png)](./media/perf103u.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-242">[![Run Load Test](./media/perf103u.png)](./media/perf103u.png)</span></span>

    <span data-ttu-id="fd1d0-243">テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-243">When the test has finished running, you should see a summary that shows transaction results.</span></span> <span data-ttu-id="fd1d0-244">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-244">Here is an example.</span></span>

    <span data-ttu-id="fd1d0-245">[![トランザクションの結果](./media/perf103v.png)](./media/perf103v.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-245">[![Transaction results](./media/perf103v.png)](./media/perf103v.png)</span></span>

11. <span data-ttu-id="fd1d0-246">テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-246">To view various indicators for the test controller and test scenario, you can switch to the **Graphs** view.</span></span>

    <span data-ttu-id="fd1d0-247">[![グラフ 表示](./media/perf103w.png)](./media/perf103w.png)</span><span class="sxs-lookup"><span data-stu-id="fd1d0-247">[![Graphs view](./media/perf103w.png)](./media/perf103w.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd1d0-248">テストの実行中、システムに関する情報はこのビューで利用することができません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-248">While tests are being run, information about your system isn't available in this view.</span></span> <span data-ttu-id="fd1d0-249">この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-249">To access this information, you must use Microsoft Dynamics Lifecycle Services (LCS) to monitor the CPU and memory usage of your AOS machine.</span></span> <span data-ttu-id="fd1d0-250">または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-250">Alternatively, you can set up perfmon directly on the AOS machine and set up the Microsoft Azure portal to monitor Microsoft SQL Server usage of Database Transaction Units (DTUs).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fd1d0-251">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="fd1d0-251">Troubleshooting</span></span>

### <a name="zoom-factor"></a><span data-ttu-id="fd1d0-252">ズーム係数</span><span class="sxs-lookup"><span data-stu-id="fd1d0-252">Zoom factor</span></span>

<span data-ttu-id="fd1d0-253">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-253">This issue affects only single-user tests.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="fd1d0-254">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-254">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-255">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-255">Solution</span></span>

<span data-ttu-id="fd1d0-256">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-256">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="fd1d0-257">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="fd1d0-257">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="fd1d0-258">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="fd1d0-258">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="fd1d0-259">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="fd1d0-259">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>

<span data-ttu-id="fd1d0-260">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-260">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="fd1d0-261">このフィールドは、Windows の**表示設定**で使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-261">This field is available in **Display settings** in Windows.</span></span> 

<span data-ttu-id="fd1d0-262">これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-262">If those steps don't work, try to change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

### <a name="certificate-thumbprint-errors"></a><span data-ttu-id="fd1d0-263">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="fd1d0-263">Certificate thumbprint errors</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-264">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-264">Error example</span></span>

```
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-265">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-265">Solution</span></span>

<span data-ttu-id="fd1d0-266">次のいくつかの理由でエラー メッセージを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-266">You might receive the error message for several reasons:</span></span>

- <span data-ttu-id="fd1d0-267">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-267">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="fd1d0-268">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-268">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="fd1d0-269">たとえば、[https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/) で使用可能な Unicode コンバーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-269">For example, you can use the Unicode converter that is available at [https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/).</span></span>

    ![Unicode コードの変換](./media/sdk_unicode_code_converter.jpg)

- <span data-ttu-id="fd1d0-271">証明書が AOS マシンに正しくインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-271">The certificate wasn't installed correctly on the AOS machine.</span></span> <span data-ttu-id="fd1d0-272">AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-272">To verify that the certificate can be found on the AOS machine, run the following Windows PowerShell script.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    <span data-ttu-id="fd1d0-273">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-273">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate can't be found.</span></span> <span data-ttu-id="fd1d0-274">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-274">To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</span></span>

- <span data-ttu-id="fd1d0-275">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-275">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="fd1d0-276">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-276">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>

    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード](./media/set_cloudctufakeacsinstall.jpg)

### <a name="no-endpoint-is-listening"></a><span data-ttu-id="fd1d0-278">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="fd1d0-278">No endpoint is listening</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-279">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-279">Error example</span></span>

<span data-ttu-id="fd1d0-280">テストが失敗すると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-280">The tests process fails, and the following error message is shown.</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-281">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-281">Solution</span></span>

<span data-ttu-id="fd1d0-282">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-282">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>

<span data-ttu-id="fd1d0-283">CloudEnvironment.Config ファイルで、次のキーに対して指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-283">In the CloudEnvironment.Config file, review the values that are specified for the following keys:</span></span>

- <span data-ttu-id="fd1d0-284">&lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="fd1d0-284">&lt;ExecutionConfigurations Key="HostName" Value="&lt;web address of host&gt;" /&gt;</span></span>
- <span data-ttu-id="fd1d0-285">&lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="fd1d0-285">&lt;ExecutionConfigurations Key="SoapHostName" Value="&lt;web address of SOAP&gt;" /&gt;</span></span>

<span data-ttu-id="fd1d0-286">これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-286">The web addresses that are specified by these keys must be the environment that you're testing.</span></span> <span data-ttu-id="fd1d0-287">開発者マシンの Web ブラウザで、**HostName** キーに対して指定された Web アドレスを開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-287">In a web browser on your developer machine, make sure that you can open the web address that is specified for the **HostName** key.</span></span>

### <a name="users-cant-be-enumerated"></a><span data-ttu-id="fd1d0-288">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="fd1d0-288">Users can't be enumerated</span></span>

<span data-ttu-id="fd1d0-289">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-289">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-290">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-290">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-291">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-291">Solution</span></span>

<span data-ttu-id="fd1d0-292">2 つのシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-292">Two scenarios can cause this error:</span></span>

- <span data-ttu-id="fd1d0-293">CloudEnvironment.Config ファイルで **SelfMintingAdminUser** として指定されたユーザーはシステム管理者ロールを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-293">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.Config file must have the System Administrator role.</span></span> <span data-ttu-id="fd1d0-294">この問題は、**SelfMintingAdminUser** として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-294">This issue occurs when the System Administrator role isn't assigned to the user who is specified as **SelfMintingAdminUser**.</span></span> <span data-ttu-id="fd1d0-295">適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-295">To verify that you've specified the correct user, you can sign in to the endpoint and view the user's roles.</span></span>

    ![管理者ユーザー](./media/sdk_admin.png)

- <span data-ttu-id="fd1d0-297">正しくない **NetworkDomain** 値が CloudEnvironment.Config ファイルで **SelfMintingAdminUser** として指定されているユーザーに指定されました。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-297">An incorrect **NetworkDomain** value was specified for the user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="fd1d0-298">オンプレミス配置の **AXDB** データベースに対して次の SQL クエリを実行することにより、正しい値を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-298">You can find the correct value by running the following SQL query against the **AXDB** database of your on-premises deployment.</span></span>

    ```sql
    select NETWORKDOMAIN, NETWORKALIAS from USERINFO where NETWORKALIAS='[AdminUserEmail]'
    ```

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="fd1d0-299">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="fd1d0-299">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="fd1d0-300">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-300">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="fd1d0-301">AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-301">It tends to occur when the AOS machine differs from the developer machine.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="fd1d0-302">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-302">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-303">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-303">Solution</span></span>

<span data-ttu-id="fd1d0-304">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-304">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="fd1d0-305">3 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-305">There are three possible causes:</span></span>

- <span data-ttu-id="fd1d0-306">CloudEnvironment.Config ファイルで、**IsAdfs** キーの値が指定されていないか、または **False** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-306">In the CloudEnvironment.Config file, either a value isn't specified for the **IsAdfs** key, or the value is set to **False**.</span></span> <span data-ttu-id="fd1d0-307">**IsAdfs** キーの値が **True** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-307">Make sure that the value for the **IsAdfs** key is set to **True**.</span></span>
- <span data-ttu-id="fd1d0-308">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-308">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="fd1d0-309">問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-309">To fix the issue, copy the .cer file that you created earlier in this topic to the AOS machine, and install the certificate.</span></span>
- <span data-ttu-id="fd1d0-310">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-310">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="fd1d0-311">問題を解決するには、wif.config ファイルに証明書を追加する方法について、[パフォーマンス SDK を使用してシングル ユーザー テストを実行する](#run-a-single-user-test-by-using-the-performance-sdk) の手順 8 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-311">To fix the issue, see step 8 in the [Run a single-user test by using the Performance SDK](#run-a-single-user-test-by-using-the-performance-sdk) section for information about how to add the certificate to the wif.config file.</span></span> <span data-ttu-id="fd1d0-312">wif.config ファイルを変更した後は、Service Fabric Explorer のエクスプローラー使用してアプリケーションを再起動することを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-312">After you modify the wif.config file, be sure to restart the application through Service Fabric Explorer.</span></span>

### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="fd1d0-313">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="fd1d0-313">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="fd1d0-314">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-314">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-315">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-315">Error example</span></span>

```
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-316">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-316">Solution</span></span>

<span data-ttu-id="fd1d0-317">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-317">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="fd1d0-318">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-318">Verify that the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span> 

<span data-ttu-id="fd1d0-319">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="fd1d0-319">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="fd1d0-320">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-320">If the file is missing, add it to the deployment items in the test settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd1d0-321">非常に似た名前を持つ 2 つのファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-321">There are two files that have very similar names.</span></span> <span data-ttu-id="fd1d0-322">1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-322">The name of one file ends in **\*.dll**, and the name of the other file ends in **\*.dll.config**. The **\*.dll.config** file must be in the deployment items in the test settings.</span></span>

### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="fd1d0-323">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="fd1d0-323">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="fd1d0-324">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-324">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-325">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-325">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-326">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-326">Solution</span></span>

<span data-ttu-id="fd1d0-327">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-327">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="fd1d0-328">この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-328">The issue typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="fd1d0-329">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-329">Verify that the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="fd1d0-330">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="fd1d0-330">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="fd1d0-331">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-331">If the file is missing, add it to the deployment items in the test settings.</span></span>

![テスト設定](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a><span data-ttu-id="fd1d0-333">InteractiveClientId は設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="fd1d0-333">InteractiveClientId wasn't specified in the settings</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-334">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-334">Error example</span></span>

```
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-335">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-335">Solution</span></span>

<span data-ttu-id="fd1d0-336">この問題は、CloudEnvironment.Config ファイルで **SelfSigningCertificateThumbprint** キーの値が指定されていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-336">This issue occurs when no value is specified for the **SelfSigningCertificateThumbprint** key in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="fd1d0-337">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-337">In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</span></span>

```
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="fd1d0-338">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="fd1d0-338">The remote host forcibly closed an existing connection</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-339">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-339">Error example</span></span>

```
System.TypeInitializationException: System.TypeInitializationException: The type initializer for
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --->
System.ServiceModel.CommunicationException: An error occurred while making the HTTP request to
<Host name>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact 
that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused 
by a mismatch of the security binding between the client and the server.** ---> System.Net.WebException: 
The underlying connection was closed: An unexpected error occurred on a send. ---> System.IO.IOException: 
Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host. ---> 
System.Net.Sockets.SocketException: An existing connection was forcibly closed by the remote host. 
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-340">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-340">Solution</span></span>

<span data-ttu-id="fd1d0-341">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-341">Run the following Windows PowerShell script on the development machine.</span></span>

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="the-w3svc-service-wasnt-found-on-the-computer"></a><span data-ttu-id="fd1d0-342">コンピューターで w3svc サービスが見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="fd1d0-342">The w3svc service wasn't found on the computer</span></span>

<span data-ttu-id="fd1d0-343">このエラーは、Microsoft Visual Studio Online を使用してロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-343">This error only occurs when you run load tests by using Microsoft Visual Studio Online.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fd1d0-344">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fd1d0-344">Error example</span></span>
```
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a><span data-ttu-id="fd1d0-345">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fd1d0-345">Solution</span></span>

<span data-ttu-id="fd1d0-346">この問題を解決する修正プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-346">A hotfix is available that resolves this issue.</span></span> <span data-ttu-id="fd1d0-347">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="fd1d0-347">The Microsoft Knowledge Base (KB) number is 4095640.</span></span>
