---
title: パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト
description: このトピックでは、パフォーマンス SDK および、 Visual Studio Online Online を使用したマルチユーザー テストを行う方法について解説します。
author: hasaid
manager: AnnBe
ms.date: 03/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 923c38d18c414fc3a0b0164e55ae1b652fe555d3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537476"
---
# <a name="performance-sdk-and-multiuser-testing-via-visual-studio-online"></a><span data-ttu-id="4799f-103">パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="4799f-103">Performance SDK and multiuser testing via Visual Studio Online</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4799f-104">このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) および、Microsoft Visual Studio Online Online を使用したマルチユーザー テストを行う方法について解説します。</span><span class="sxs-lookup"><span data-stu-id="4799f-104">This topic describes the Performance software development kit (SDK) and shows how to do multiuser testing via Microsoft Visual Studio Online.</span></span> <span data-ttu-id="4799f-105">また、タスク レコーダーで記録したシナリオをシングルユーザー テスト、そしてマルチユーザー テストに変換する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="4799f-105">It also describes how to convert a scenario that you recorded in Task recorder to a single-user test and then a multiuser test.</span></span>

   > [!IMPORTANT]
  > <span data-ttu-id="4799f-106">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</span><span class="sxs-lookup"><span data-stu-id="4799f-106">Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</span></span> <span data-ttu-id="4799f-107">将来的には、代替ソリューションに向けた推奨案の提案に取り組んでいきます。</span><span class="sxs-lookup"><span data-stu-id="4799f-107">In the future, we will be publishing some recommendations for alternative solutions.</span></span>
  
  > - <span data-ttu-id="4799f-108">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="4799f-108">If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="4799f-109">サポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4799f-109">You can continue using it until the end of support cycle.</span></span> 
 
 >  - <span data-ttu-id="4799f-110">クラウド ベースの負荷テストサービスをご利用の場合は、同サービスは2020年3月31日までの間、継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="4799f-110">If you are using the cloud-based load testing service, the cloud-based load testing service will continue to run through March 31, 2020.</span></span> <span data-ttu-id="4799f-111">それまでの間は、同サービスの全機能を継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="4799f-111">Until then, you can continue to use all of the experiences powered by this service without interruption.</span></span> <span data-ttu-id="4799f-112">また、オンプレミス負荷テストに切り替えることがも可能です。</span><span class="sxs-lookup"><span data-stu-id="4799f-112">Alternatively, you can switch to on-premises load testing.</span></span> 
   
   > <span data-ttu-id="4799f-113">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="4799f-113">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>

> [!NOTE]
> <span data-ttu-id="4799f-114">管理者として環境を利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-114">You must have access the environment as an administrator.</span></span> <span data-ttu-id="4799f-115">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4799f-115">For more information, see [Access instances](../dev-tools/access-instances.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4799f-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="4799f-116">Prerequisites</span></span>

- <span data-ttu-id="4799f-117">Microsoft Visual Studio 2015 年エンタープライズ</span><span class="sxs-lookup"><span data-stu-id="4799f-117">Microsoft Visual Studio 2015 Enterprise</span></span>
- <span data-ttu-id="4799f-118">数量データを含むデプロイメント</span><span class="sxs-lookup"><span data-stu-id="4799f-118">A deployment that has volume data</span></span>
- <span data-ttu-id="4799f-119">パフォーマンス SDK (SDK は K:\\PerfSDK\\PerfSDKLocalDirectory にある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-119">The Performance SDK (The SDK will likely be in K:\\PerfSDK\\PerfSDKLocalDirectory.</span></span> <span data-ttu-id="4799f-120">ただし、環境によっては C:\\PerfSDK にある可能性があります。)</span><span class="sxs-lookup"><span data-stu-id="4799f-120">However, depending on your environment, it might be in C:\\PerfSDK.)</span></span>

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a><span data-ttu-id="4799f-121">XML 記録からシングル ユーザー C# テストを作成する</span><span class="sxs-lookup"><span data-stu-id="4799f-121">Create a single-user C# test from an XML recording</span></span>

<!--To view a video that shows how to create a single-user test, go to [https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3).-->

1. <span data-ttu-id="4799f-122">タスク レコーダーを使用して、テストするシナリオの記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="4799f-122">Use Task recorder to create a recording of the scenario that you want to test.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="4799f-123">既定のダッシュ ボード ページでレコードが起動しない場合、テストを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="4799f-123">If your recording doesn't start on the default dashboard page, the test won't be able to run.</span></span>

2. <span data-ttu-id="4799f-124">Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4799f-124">Start Microsoft Visual Studio as an administrator, and build the **PerfSDKSample** project.</span></span> <span data-ttu-id="4799f-125">このプロジェクトは **PerfSDK** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-125">This project is in the **PerfSDK** folder.</span></span> <span data-ttu-id="4799f-126">プロジェクトを既に構築している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="4799f-126">If you've already built the project, skip this step.</span></span>
3. <span data-ttu-id="4799f-127">**Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-127">Select **Dynamics 365** &gt; **Addins** &gt; **Create C# perf test from recording**.</span></span>
4. <span data-ttu-id="4799f-128">**タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-128">In the **Import Task Recording** dialog box, enter the required details, and then select **Import**.</span></span>

    <span data-ttu-id="4799f-129">[![インポート タスク記録 ダイアログ ボックス](./media/perf103a.png)](./media/perf103a.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-129">[![Import Task Recording dialog box](./media/perf103a.png)](./media/perf103a.png)</span></span>

    <span data-ttu-id="4799f-130">C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-130">A C# test is generated in the Generated folder for the project that you selected.</span></span>

## <a name="run-a-single-user-performance-test-by-using-the-performance-sdk"></a><span data-ttu-id="4799f-131">パフォーマンス SDK を使用して単一ユーザー パフォーマンス テストを実行</span><span class="sxs-lookup"><span data-stu-id="4799f-131">Run a single-user performance test by using the Performance SDK</span></span>

1. <span data-ttu-id="4799f-132">Microsoft Windows のコントロール パネルで、**システムとセキュリティ**  &gt; **システム** &gt; **システムの詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-132">In Control Panel in Microsoft Windows, select **System and Security** &gt; **System** &gt; **Advanced System Settings**.</span></span> <span data-ttu-id="4799f-133">**TestRoot**環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-133">Verify that the **TestRoot** environment variable is set to the path of the PerfSDK folder.</span></span>

    <span data-ttu-id="4799f-134">[![EnvironmentVariable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-134">[![EnvironmentVariable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span></span>

2. <span data-ttu-id="4799f-135">[http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4799f-135">Download the **selenium-dotnet-strongnamed-2.42.0.zip** and **IEDriverServer\_Win32\_2.42.0.zip** files from [http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/).</span></span>
3. <span data-ttu-id="4799f-136">ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="4799f-136">Extract the files.</span></span> <span data-ttu-id="4799f-137">動的リンク ライブラリ (DLL) を、**selenium-dotnet-strongnamed-2.42.0.zip\net40** フォルダから **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4799f-137">Copy the dynamic-link libraries (DLLs) from the **selenium-dotnet-strongnamed-2.42.0.zip\net40** folder to the **PerfSDK\\Common\\External\\Selenium** folder.</span></span>  <span data-ttu-id="4799f-138">**IEDriverServer.exe** を、**IEDriverServer_Win32_2.42.0.zip** から **PerfSDK\\Common\\External\\Selenium** フォルダにもコピーします。</span><span class="sxs-lookup"><span data-stu-id="4799f-138">Copy the **IEDriverServer.exe** from the **IEDriverServer_Win32_2.42.0.zip** to the **PerfSDK\\Common\\External\\Selenium** folder as well.</span></span>

    <span data-ttu-id="4799f-139">[![PerfSDK\Common\External\Selenium フォルダーにある DLL](./media/perf103d.png)](./media/perf103d.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-139">[![DLLs in the PerfSDK\Common\External\Selenium folder](./media/perf103d.png)](./media/perf103d.png)</span></span>

4. <span data-ttu-id="4799f-140">**PerfSDK\\Common\\External\\Selenium** フォルダーの **WebDriver.dll** への参照を、Visual Studio プロジェクトへ追加します。</span><span class="sxs-lookup"><span data-stu-id="4799f-140">Add a reference to the **WebDriver.dll** in the **PerfSDK\\Common\\External\\Selenium** folder to your Visual Studio project.</span></span>    

5. <span data-ttu-id="4799f-141">証明書を生成しインストールします。</span><span class="sxs-lookup"><span data-stu-id="4799f-141">Generate and install a certificate.</span></span> <span data-ttu-id="4799f-142">証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4799f-142">To generate a certificate file, open a Command Prompt window as an administrator, and run the following commands.</span></span> <span data-ttu-id="4799f-143">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-143">When you're prompted for a private key password, select **None**.</span></span>

    ```
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="4799f-144">これらのコマンドでは次の要素を注意してください。</span><span class="sxs-lookup"><span data-stu-id="4799f-144">Note the following elements in these commands:</span></span>

    - <span data-ttu-id="4799f-145">**-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="4799f-145">**-n "CN=127.0.0.1"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="4799f-146">この証明書の名前が **127.0.0.1** であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="4799f-146">It's very important that the name of this certificate be **127.0.0.1**.</span></span> <span data-ttu-id="4799f-147">それ以外の場合は、単一ユーザー テストは実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="4799f-147">Otherwise, the single-user tests won't be able to run.</span></span>
    - <span data-ttu-id="4799f-148">**-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-148">**-eku 1.3.6.1.5.5.7.3.1** gives the purpose of the certificate.</span></span> <span data-ttu-id="4799f-149">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-149">It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</span></span>

    <span data-ttu-id="4799f-150">スクリプトの実行が終了した後、**c:\\Temp** で以下のファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-150">After the script has finished running, you should see the following files in **C:\\Temp**:</span></span>

    - <span data-ttu-id="4799f-151">authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="4799f-151">authcert.pfx</span></span>
    - <span data-ttu-id="4799f-152">authcert.cer</span><span class="sxs-lookup"><span data-stu-id="4799f-152">authcert.cer</span></span> 
    - <span data-ttu-id="4799f-153">authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="4799f-153">authcert.pvk</span></span>

6. <span data-ttu-id="4799f-154">**authcert.pfx** および **authcert.cer** 証明書ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="4799f-154">Install the **authcert.pfx** and **authcert.cer** certificate files.</span></span> <span data-ttu-id="4799f-155">これらのファイルをインストールするときは、**ローカル コンピューター**をかならず選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-155">When you install these files, make sure that you select **Local Machine**.</span></span> <span data-ttu-id="4799f-156">**authcert.pfx** ファイルを **PerfSDK** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4799f-156">Copy the **authcert.pfx** file to the **PerfSDK** folder.</span></span>
7. <span data-ttu-id="4799f-157">管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。</span><span class="sxs-lookup"><span data-stu-id="4799f-157">Open a Microsoft Windows PowerShell window as an administrator, and run the following commands to get the thumbprint of the installed certificate.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

8. <span data-ttu-id="4799f-158">**CloudEnvironment.Config** ファイルで、**SelfSigningCertificateThumbprint** キーの値として拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="4799f-158">In the **CloudEnvironment.Config** file, enter the thumbprint as the value for the **SelfSigningCertificateThumbprint** key.</span></span>

    <span data-ttu-id="4799f-159">[![更新された CloudEnvironment.Config ファイル](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span><span class="sxs-lookup"><span data-stu-id="4799f-159">[![Updated CloudEnvironment.Config file](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span></span>

9. <span data-ttu-id="4799f-160">**wif.config** ファイルを更新して Application Object Server (AOS) が証明書を信頼できるようにするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4799f-160">Follow these steps to update the **wif.config** file so that Application Object Server (AOS) trusts the certificate:</span></span>

    1. <span data-ttu-id="4799f-161">Microsoft インターネット インフォメーション サービス (IIS) を起動し、サイトの一覧にある **Microsoft Dynamics 365 for Finance and Operations** を検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-161">Start Microsoft Internet Information Services (IIS), and find **Microsoft Dynamics 365 for Finance and Operations** in the list of sites.</span></span>
    2. <span data-ttu-id="4799f-162">**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-162">Select **Explore**, and find the **wif.config** file.</span></span>

        <span data-ttu-id="4799f-163">[![wif.config ファイル](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span><span class="sxs-lookup"><span data-stu-id="4799f-163">[![wif.config file](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span></span>

    3. <span data-ttu-id="4799f-164">**Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-164">In the **wif.config** file, find the authority that is named **AxTokenIssuer**.</span></span> <span data-ttu-id="4799f-165">この権限の捺印のリストに捺印を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-165">You must add your thumbprint to the list of thumbprints for this authority.</span></span>

        <span data-ttu-id="4799f-166">[![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-166">[![Thumbprint added to the list of authorities for AxTokenIssuer](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span></span>

    4. <span data-ttu-id="4799f-167">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="4799f-167">Restart IIS.</span></span>

10. <span data-ttu-id="4799f-168">Visual Studio で **PerfSDKSample** プロジェクトを開き、**PurchaseReq.cs** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-168">In Visual Studio, open the **PerfSDKSample** project, and find the **PurchaseReq.cs** file.</span></span> <span data-ttu-id="4799f-169">このファイルは、サンプル シングルユーザー テストです。</span><span class="sxs-lookup"><span data-stu-id="4799f-169">This file is a sample single-user test.</span></span> <span data-ttu-id="4799f-170">ファイルで、次の行をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="4799f-170">In the file, comment out the following lines.</span></span>

    ```
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    <span data-ttu-id="4799f-171">[![PurchaseReq.cs でコメント アウトされた行](./media/perf103e.png)](./media/perf103e.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-171">[![Lines commented out in PurchaseReq.cs](./media/perf103e.png)](./media/perf103e.png)</span></span>

11. <span data-ttu-id="4799f-172">管理者のユーザー名を入力することによって **CloudEnvironment.Config** ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="4799f-172">Modify the **CloudEnvironment.Config** file by entering your admin user name.</span></span> <span data-ttu-id="4799f-173">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-173">Here is an example.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4799f-174">**ConfigName** は **DEVFABRIC** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-174">**ConfigName** must be set to **DEVFABRIC**.</span></span> 

    <span data-ttu-id="4799f-175">[![変更された CloudEnvironment.Config ファイル](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-175">[![Modified CloudEnvironment.Config file](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</span></span> 

12. <span data-ttu-id="4799f-176">**CloudEnvironment.Config** ファイルに、エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="4799f-176">In the **CloudEnvironment.Config** file, enter your endpoint.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4799f-177">環境をアプリケーション リクエスト ルーティング (ARR) に対して有効にするには、2 つのエンドポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-177">If the environment is enabled for Application Request Routing (ARR), you have two endpoints.</span></span> <span data-ttu-id="4799f-178">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-178">Here is an example:</span></span>
    >
    > - <span data-ttu-id="4799f-179">apr-arr8aos**soap**.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="4799f-179">apr-arr8aos**soap**.axcloud.test.dynamics.com</span></span>
    > - <span data-ttu-id="4799f-180">apr-arr8aos.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="4799f-180">apr-arr8aos.axcloud.test.dynamics.com</span></span>
    >
    > <span data-ttu-id="4799f-181">この場合、CloudEnvironment.Config ファイルに両方のエンドポイントを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-181">In this case, you must enter both endpoints in the CloudEnvironment.Config file.</span></span>
    >
    > <span data-ttu-id="4799f-182">[![CloudEnvironment.Config のエンドポイント](./media/perf103upd.png)](./media/perf103upd.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-182">[![Endpoints in CloudEnvironment.Config](./media/perf103upd.png)](./media/perf103upd.png)</span></span>

13. <span data-ttu-id="4799f-183">**テスト** &gt; **テストの設定** を選択し、**既定のプロセッサ アーキテクチャ** を **x64** に設定してソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4799f-183">Select **Test** &gt; **Test settings**, set **Default processor architecture** to **x64**, and then build the solution.</span></span>
14. <span data-ttu-id="4799f-184">**テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-184">Select **Test** &gt; **Windows** &gt; **Test Explorer** to view the list of tests.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4799f-185">場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-185">Sometimes, Visual Studio might not update the list of tests after you create a test script from a task recording.</span></span> <span data-ttu-id="4799f-186">この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="4799f-186">In this case, restart Visual Studio, and then reopen Test Explorer.</span></span>

    <span data-ttu-id="4799f-187">新しいテストに **TestMethod** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="4799f-187">Your new test will be named **TestMethod**.</span></span> <span data-ttu-id="4799f-188">TestMethod のメソッド名を変更すると、個々の名前がテストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-188">If you change the method name of TestMethod, your test will receive an individual name.</span></span> 

<span data-ttu-id="4799f-189">テストを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4799f-189">You can now run the test.</span></span> <span data-ttu-id="4799f-190">テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。</span><span class="sxs-lookup"><span data-stu-id="4799f-190">When you run the test, Internet Explorer should be started, and it should replay the scenario that you recorded.</span></span>

## <a name="create-a-multiuser-test-from-a-single-user-test"></a><span data-ttu-id="4799f-191">シングル ユーザー テストからマルチ ユーザー テストを作成する</span><span class="sxs-lookup"><span data-stu-id="4799f-191">Create a multiuser test from a single-user test</span></span>

<span data-ttu-id="4799f-192">以前のセクションで情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="4799f-192">After you create a single-user test by using the information in the previous section, you can convert it to a multiuser test.</span></span> <span data-ttu-id="4799f-193">テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="4799f-193">Add **MS.Dynamics.TestTools.UIHelpers.Core;** to your test script, and find the following line in the **TestSetup** method.</span></span>

```
Client = DispatchedClient.DefaultInstance;
```

<span data-ttu-id="4799f-194">その行を以下の行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4799f-194">Replace that line with the following lines.</span></span>

```
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

<span data-ttu-id="4799f-195">タスクのインポーターによって生成されたテスト スクリプトには、**TestSetup** メソッドの次の明細行と似ている明細行が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-195">The test script that was generated by the Task Importer might contain a line that resembles the following line in the **TestSetup** method.</span></span>

```
UserContext _context = new UserContext(UserManagement.AdminUser);
```

<span data-ttu-id="4799f-196">さらに、**TestCleanup** メソッドから次の行を削除する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-196">You must also remove the following line from the **TestCleanup** method.</span></span>

```
_userContext.Dispose();
```

<span data-ttu-id="4799f-197">ロード テストとして実行される任意のテストからこれらの明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="4799f-197">Remove these lines from any tests that will be run as load tests.</span></span> <span data-ttu-id="4799f-198">このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-198">This code is required only for single-user tests and has a negative effect on the performance of load tests.</span></span>

<span data-ttu-id="4799f-199">タスク記録が行われたときに入力した値がランダム化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-199">Make sure that the values that you entered when you made the task recording are randomized.</span></span> <span data-ttu-id="4799f-200">テスト データを生成するために、データ拡張ツールを最初に使用することが必要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-200">You might have to use the Data Expansion Tool first to generate test data.</span></span>

## <a name="set-up-azure-devops-for-multiuser-testing"></a><span data-ttu-id="4799f-201">Azure DevOps でマルチ ユーザー テストを設定</span><span class="sxs-lookup"><span data-stu-id="4799f-201">Set up Azure DevOps for multiuser testing</span></span>

<span data-ttu-id="4799f-202">この例では、ユーザーは ProcureToPay.cs ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4799f-202">For this example, you will use the ProcureToPay.cs file.</span></span> <span data-ttu-id="4799f-203">Visual Studio を開始するにサインインする必要があります、[Azure DevOps ポータル](https://app.vssps.visualstudio.com/profile/view)にサインインし、**Visual Studio で開く**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-203">To start Visual Studio, you must sign in to the [Azure DevOps portal](https://app.vssps.visualstudio.com/profile/view), and then select **Open in Visual Studio**.</span></span>

> [!NOTE]
> <span data-ttu-id="4799f-204">このステップは 1 回のみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-204">You must complete this step only one time.</span></span> <span data-ttu-id="4799f-205">Azure DevOps にサインインした後、設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-205">After you've signed in to Azure DevOps, the settings are saved.</span></span>

<span data-ttu-id="4799f-206">[![Visual Studio で開く](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="4799f-206">[![Open in Visual Studio](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span></span>

1. <span data-ttu-id="4799f-207">**PerfSDKSample** プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4799f-207">Open the **PerfSDKSample** project.</span></span>
2. <span data-ttu-id="4799f-208">**CloudEnvironment.Config** ファイルで、**UserFormat** エントリを更新して、管理者ユーザー URL を反映します。</span><span class="sxs-lookup"><span data-stu-id="4799f-208">In the **CloudEnvironment.Config** file, update the **UserFormat** entry so that it reflects the admin user URL.</span></span> <span data-ttu-id="4799f-209">たとえば、`admin@example.com` に対して、ユーザー形式として **TST\_{0}@example.com** を使用します。</span><span class="sxs-lookup"><span data-stu-id="4799f-209">For example, for `admin@example.com`, use **TST\_{0}@example.com** as the user format.</span></span> <span data-ttu-id="4799f-210">また、**UserCount** 値をパフォーマンス テストに含めるユーザーの数に変更します。</span><span class="sxs-lookup"><span data-stu-id="4799f-210">Additionally, change the **UserCount** value to the number of users that you want to have in your performance test.</span></span>

    <span data-ttu-id="4799f-211">[![更新された CloudEnvironment.Config ファイル](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-211">[![Updated CloudEnvironment.Config file](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</span></span>

3. <span data-ttu-id="4799f-212">管理者モードでコマンド プロンプトを開き、**PerfSDK** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="4799f-212">Open a Command Prompt window as an administrator, and navigate to the **PerfSDK** folder.</span></span> <span data-ttu-id="4799f-213">次のコマンドを実行して環境のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4799f-213">Run the following command to create test users for your environment.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

    <span data-ttu-id="4799f-214">必要な数のユーザーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4799f-214">You can create as many users as you want.</span></span> <span data-ttu-id="4799f-215">たとえば、次のコマンドは、USMF 会社で 150 人のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4799f-215">For example, the following command creates 150 test users for the USMF company.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe 150 USMF
    ```

4. <span data-ttu-id="4799f-216">管理者ユーザーとしてエンドポイントにログインし、ユーザーがシステムで作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-216">Sign in to your endpoint as the admin user, and verify that users were created in the system.</span></span>

### <a name="test-the-sandbox-environment"></a><span data-ttu-id="4799f-217">サンドボックス環境をテスト</span><span class="sxs-lookup"><span data-stu-id="4799f-217">Test the sandbox environment</span></span>

<span data-ttu-id="4799f-218">ここまでは、手順で、AOS マシンが開発マシンでもある開発者トポロジを使用していることを前提としていました。</span><span class="sxs-lookup"><span data-stu-id="4799f-218">Up to this point, the instructions have assumed that you have a developer topology where the AOS machine is also your development machine.</span></span> <span data-ttu-id="4799f-219">Azure DevOps でロード テストを実行するには、テスト環境がサンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-219">To run load tests in Azure DevOps, the environment that you test must be a sandbox environment.</span></span> <span data-ttu-id="4799f-220">サンドボックス環境と負荷テストを実行するコンピューター間の信頼関係を確立するには、いくつかの追加手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-220">You must complete a few additional steps to establish trust between the sandbox environment and the computer that runs the load tests.</span></span> <span data-ttu-id="4799f-221">負荷テストを実行できるコンピューターは、開発マシンまたは Visual Studio Online  にて作成したテスト エージェントのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4799f-221">The computer that runs the load tests can be either your development machine or the test agent that is created by Visual Studio Online.</span></span>

1. <span data-ttu-id="4799f-222">サンドボックス AOS マシンへのリモート デスクトップ の接続を確立し、**.cer** ファイルを上書きします。</span><span class="sxs-lookup"><span data-stu-id="4799f-222">Establish a Remote Desktop connection to your sandbox AOS machine, and copy over the **.cer** file.</span></span> <span data-ttu-id="4799f-223">ファイルをダブルクリックして、インストールします。</span><span class="sxs-lookup"><span data-stu-id="4799f-223">Double-click the file to install it.</span></span> <span data-ttu-id="4799f-224">証明書ストアの入力を要求するメッセージが表示されたら、**個人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-224">When you're prompted for the certificate store, select **Personal**.</span></span>
2. <span data-ttu-id="4799f-225">IIS を起動し、サイトの一覧で **AOSService** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="4799f-225">Start IIS, and find **AOSService** in the list of sites.</span></span> <span data-ttu-id="4799f-226">その後、**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-226">Then select **Explore**, and find the **wif.config** file.</span></span> <span data-ttu-id="4799f-227">**Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。</span><span class="sxs-lookup"><span data-stu-id="4799f-227">In the **wif.config** file, find the authority that is named **AxTokenIssuer**.</span></span> <span data-ttu-id="4799f-228">この権限の捺印のリストに捺印を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-228">You must add your thumbprint to the list of thumbprints for this authority.</span></span> <span data-ttu-id="4799f-229">(以前に生成した証明書の値を使用します。)</span><span class="sxs-lookup"><span data-stu-id="4799f-229">(Use the values from the certificate that you generated earlier.)</span></span>

    <span data-ttu-id="4799f-230">[![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-230">[![Thumbprint added to the list of authorities for AxTokenIssuer](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span></span>

3. <span data-ttu-id="4799f-231">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="4799f-231">Restart IIS.</span></span>

<span data-ttu-id="4799f-232">トポロジに対してパフォーマンス テストを実行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4799f-232">You can now run performance tests against the topology.</span></span>

> [!NOTE]
> <span data-ttu-id="4799f-233">トポロジに複数の AOS マシンがある場合、証明書をインストールして、各 AOS マシンの wif.config ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-233">If your topology has multiple AOS machines, you must install the certificate and update the wif.config file on every AOS machine.</span></span>

## <a name="run-the-performance-test"></a><span data-ttu-id="4799f-234">パフォーマンス テストの実行</span><span class="sxs-lookup"><span data-stu-id="4799f-234">Run the performance test</span></span>

1. <span data-ttu-id="4799f-235">Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="4799f-235">In the Visual Studio editor, open the **ProcureToPay.cs** file, and append the following lines in the **TestSetup** method.</span></span>

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

2. <span data-ttu-id="4799f-236">[https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420)から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4799f-236">Download the installer (.msi) file for Microsoft ODBC Driver 13 for SQL Server from [https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420).</span></span> <span data-ttu-id="4799f-237">(64 ビット バージョンの .msi ファイルを選択します。) ファイルを **PerfSDK** ディレクトリの **Visual Studio Online** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="4799f-237">(Select the 64-bit version of the .msi file.) Put the file in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
3. <span data-ttu-id="4799f-238">**Visual Studio Online** フォルダ内の **setup.cmd** ファイル内容を次のコードと一致するように変更します。</span><span class="sxs-lookup"><span data-stu-id="4799f-238">Modify the contents of the **setup.cmd** file in the **Visual Studio Online** folder so that they match the following code.</span></span>

    ```
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

4. <span data-ttu-id="4799f-239">**CloudCtuFakeACSInstall.cmd** ファイルの内容を変更して、**インポート**コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。</span><span class="sxs-lookup"><span data-stu-id="4799f-239">Modify the contents of the **CloudCtuFakeACSInstall.cmd** file so that the **Import** command has an empty string instead of **'password'**.</span></span> <span data-ttu-id="4799f-240">スクリプトの 3 行目は、次の行に似ているはずです。</span><span class="sxs-lookup"><span data-stu-id="4799f-240">The third line of the script should resemble the following line.</span></span>

    ```
    set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....
    ```

5. <span data-ttu-id="4799f-241">ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="4799f-241">In your solution files, double-click the **vsonline.testsettings** file to modify the test settings.</span></span>
6. <span data-ttu-id="4799f-242">**テストの設定**ダイアログ ボックスの**配置**タブで、次の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="4799f-242">In the **Test Settings** dialog box, on the **Deployment** tab, use the following settings:</span></span>

    - <span data-ttu-id="4799f-243">**展開の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4799f-243">Select the **Enable deployment** check box.</span></span>
    - <span data-ttu-id="4799f-244">**配置する追加のファイルやディレクトリ** フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-244">In the **Additional files and directories to deploy** field, make sure that the following files and directories are listed:</span></span>

        - <span data-ttu-id="4799f-245">&lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\</span><span class="sxs-lookup"><span data-stu-id="4799f-245">&lt;Solution Directory&gt;\\PerfSDKSample\\bin\\Debug\\</span></span>
        - <span data-ttu-id="4799f-246">C:\\PerfSDK\\CloudEnvironment.Config</span><span class="sxs-lookup"><span data-stu-id="4799f-246">C:\\PerfSDK\\CloudEnvironment.Config</span></span>
        - <span data-ttu-id="4799f-247">C:\\PerfSDK\\authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="4799f-247">C:\\PerfSDK\\authcert.pfx</span></span>
        - <span data-ttu-id="4799f-248">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span><span class="sxs-lookup"><span data-stu-id="4799f-248">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span></span>
        - <span data-ttu-id="4799f-249">C:\\PerfSDK\\ Visual Studio Online\\</span><span class="sxs-lookup"><span data-stu-id="4799f-249">C:\\PerfSDK\\Visual Studio Online\\</span></span>

        <span data-ttu-id="4799f-250">[![フィールドを配置するための追加ファイルおよびディレクトリ](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-250">[![Additional files and directories to deploy field](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span></span>

        > [!NOTE]
        > <span data-ttu-id="4799f-251">PerfSDK フォルダーが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-251">Your PerfSDK folder might differ.</span></span>

7. <span data-ttu-id="4799f-252">**設定とクリーンアップ** タブで、 **PerfSDK** ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-252">On the **Setup and Cleanup Scripts** tab, select the **setup.cmd** file that is in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
8. <span data-ttu-id="4799f-253">**追加設定**タブで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-253">On the **Additional Settings** tab, select **Run tests in 64 bit process on 64 bit machine**.</span></span>
9. <span data-ttu-id="4799f-254">テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4799f-254">To run the test, open the **SampleLoadTest.loadtest** file, and select **Run Load Test**.</span></span>

    <span data-ttu-id="4799f-255">[![負荷テストの実行](./media/perf103u.png)](./media/perf103u.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-255">[![Run Load Test](./media/perf103u.png)](./media/perf103u.png)</span></span>

    <span data-ttu-id="4799f-256">テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-256">When the test has finished running, you should see a summary that shows transaction results.</span></span> <span data-ttu-id="4799f-257">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-257">Here is an example.</span></span>

    <span data-ttu-id="4799f-258">[![トランザクションの結果](./media/perf103v.png)](./media/perf103v.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-258">[![Transaction results](./media/perf103v.png)](./media/perf103v.png)</span></span>

10. <span data-ttu-id="4799f-259">テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="4799f-259">To view various indicators for the test controller and test scenario, you can switch to the **Graphs** view.</span></span>

    <span data-ttu-id="4799f-260">[![グラフ 表示](./media/perf103w.png)](./media/perf103w.png)</span><span class="sxs-lookup"><span data-stu-id="4799f-260">[![Graphs view](./media/perf103w.png)](./media/perf103w.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="4799f-261">テストの実行中、システムに関する情報はこのビューで利用することができません。</span><span class="sxs-lookup"><span data-stu-id="4799f-261">While tests are being run, information about your system isn't available in this view.</span></span> <span data-ttu-id="4799f-262">この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-262">To access this information, you must use Microsoft Dynamics Lifecycle Services (LCS) to monitor the CPU and memory usage of your AOS machine.</span></span> <span data-ttu-id="4799f-263">または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。</span><span class="sxs-lookup"><span data-stu-id="4799f-263">Alternatively, you can set up perfmon directly on the AOS machine and set up the Microsoft Azure portal to monitor Microsoft SQL Server usage of Database Transaction Units (DTUs).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="4799f-264">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4799f-264">Troubleshooting</span></span>

### <a name="no-client-was-opened-in-the-time-out-period"></a><span data-ttu-id="4799f-265">タイムアウト期間中クライアントが開かれていません</span><span class="sxs-lookup"><span data-stu-id="4799f-265">No client was opened in the time-out period</span></span>
<span data-ttu-id="4799f-266">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="4799f-266">This issue affects only single-user tests.</span></span> <span data-ttu-id="4799f-267">テストが実行されているとき、Web クライアントを開きますが、Web サイトが読み込まれることはありません。</span><span class="sxs-lookup"><span data-stu-id="4799f-267">When the test is running, a web client opens, but a website is never loaded.</span></span> <span data-ttu-id="4799f-268">代わりに、白い画面を持つ空の Web クライアントがある場合、ページの上部で次のメッセージが表示されます: 「これは WebDriver サーバーの初期開始ページです。」</span><span class="sxs-lookup"><span data-stu-id="4799f-268">Instead, there is an empty web client that has a white screen, and the following message appears at the top of the page: "This is the initial start page for the WebDriver server."</span></span> <span data-ttu-id="4799f-269">テストは最終的にタイム アウトおよび失敗し、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-269">The test will eventually time out and fail, and an error message will be shown.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-270">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-270">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.
```

#### <a name="solution"></a><span data-ttu-id="4799f-271">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-271">Solution</span></span>
<span data-ttu-id="4799f-272">このトピックの「パフォーマンス SDK を使用してシングル ユーザー パフォーマンス テストを実行する」セクションの、手順 4 から 8 を実行します。</span><span class="sxs-lookup"><span data-stu-id="4799f-272">Follow steps 4 through 8 in the "Run a single-user performance test by using the Performance SDK" section of this topic.</span></span> <span data-ttu-id="4799f-273">そのセクションでは、このタイプのテストの正しい証明書を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4799f-273">That section explains how to create a correct certificate for this type of test.</span></span> <span data-ttu-id="4799f-274">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="4799f-274">It also explains how to add the thumbprint of the certificate to the wif.config file.</span></span>

### <a name="zoom-factor"></a><span data-ttu-id="4799f-275">ズーム係数</span><span class="sxs-lookup"><span data-stu-id="4799f-275">Zoom factor</span></span>

<span data-ttu-id="4799f-276">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="4799f-276">This issue affects only single-user tests.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="4799f-277">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-277">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```

#### <a name="solution"></a><span data-ttu-id="4799f-278">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-278">Solution</span></span>

<span data-ttu-id="4799f-279">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="4799f-279">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="4799f-280">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="4799f-280">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="4799f-281">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="4799f-281">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="4799f-282">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="4799f-282">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>
 
<span data-ttu-id="4799f-283">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-283">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="4799f-284">このフィールドは、Windows の**表示設定**で使用できます。</span><span class="sxs-lookup"><span data-stu-id="4799f-284">This field is available in **Display settings** in Windows.</span></span> 
 
<span data-ttu-id="4799f-285">これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="4799f-285">If those steps don't work, try to change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

### <a name="certificate-thumbprint-errors"></a><span data-ttu-id="4799f-286">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="4799f-286">Certificate thumbprint errors</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-287">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-287">Error example</span></span>

```
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a><span data-ttu-id="4799f-288">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-288">Solution</span></span>

<span data-ttu-id="4799f-289">次のいくつかの理由でエラー メッセージを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-289">You might receive the error message for several reasons:</span></span>

- <span data-ttu-id="4799f-290">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4799f-290">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="4799f-291">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-291">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="4799f-292">たとえば、[https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/) で使用可能な Unicode コンバーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4799f-292">For example, you can use the  Unicode converter that is available at [https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/).</span></span>

    ![Unicode コードの変換](./media/sdk_unicode_code_converter.jpg)
 
- <span data-ttu-id="4799f-294">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="4799f-294">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="4799f-295">AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4799f-295">To verify that the certificate can be found on the AOS machine, run the following Windows PowerShell script.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    <span data-ttu-id="4799f-296">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。</span><span class="sxs-lookup"><span data-stu-id="4799f-296">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate can't be found.</span></span> <span data-ttu-id="4799f-297">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="4799f-297">To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</span></span>
 
- <span data-ttu-id="4799f-298">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-298">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="4799f-299">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-299">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>
 
    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード](./media/set_cloudctufakeacsinstall.jpg)
 
### <a name="no-endpoint-is-listening"></a><span data-ttu-id="4799f-301">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="4799f-301">No endpoint is listening</span></span>

<span data-ttu-id="4799f-302">この問題は、シングルユーザーまたはマルチユーザーのテストを実行する場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-302">This issue can occur when you run single-user or multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-303">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-303">Error example</span></span>

<span data-ttu-id="4799f-304">テストまたはユーザー作成プロセスが失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-304">The tests or user creation process fails, and the following error message is shown.</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a><span data-ttu-id="4799f-305">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-305">Solution</span></span>

<span data-ttu-id="4799f-306">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-306">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>
 
<span data-ttu-id="4799f-307">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-307">In the CloudEnvironment.Config file, review the values that are specified by the following keys:</span></span>

- <span data-ttu-id="4799f-308">&lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="4799f-308">&lt;ExecutionConfigurations Key="HostName" Value="&lt;web address of host&gt;" /&gt;</span></span>
- <span data-ttu-id="4799f-309">&lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="4799f-309">&lt;ExecutionConfigurations Key="SoapHostName" Value="&lt;web address of SOAP&gt;" /&gt;</span></span>

<span data-ttu-id="4799f-310">これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-310">The web addresses that are specified by these keys must be the environment that you're testing.</span></span> <span data-ttu-id="4799f-311">開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-311">In a web browser on your developer machine, make sure that you can open the web address that is specified by the **HostName** key.</span></span>

<span data-ttu-id="4799f-312">オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-312">For online load tests, the environment that is specified by the **HostName** key in the CloudEnvironment.Config file must be publicly accessible from any machine.</span></span> <span data-ttu-id="4799f-313">したがって、ワンボックス開発環境をテストする必要がある場合、 Visual Studio Online Online を使用した負荷テストの実行はできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。</span><span class="sxs-lookup"><span data-stu-id="4799f-313">Therefore, if you must test a one-box environment, you won't be able to run the load test by using Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</span></span>

### <a name="users-cant-be-enumerated"></a><span data-ttu-id="4799f-314">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="4799f-314">Users can't be enumerated</span></span>

<span data-ttu-id="4799f-315">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-315">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-316">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-316">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a><span data-ttu-id="4799f-317">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-317">Solution</span></span>

<span data-ttu-id="4799f-318">2 つのシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-318">Two scenarios can cause this error:</span></span>

- <span data-ttu-id="4799f-319">CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーはシステム管理者ロールを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-319">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file must have the System Administrator role.</span></span> <span data-ttu-id="4799f-320">この問題は、**SelfMintingAdminUser** として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-320">This issue occurs when the System Administrator role isn't assigned to the user who is specified as **SelfMintingAdminUser**.</span></span> <span data-ttu-id="4799f-321">適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-321">To verify that you've specified the correct user, you can sign in to the endpoint and view the user's roles.</span></span>

    ![管理者ユーザー](./media/sdk_admin.png)

- <span data-ttu-id="4799f-323">CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーは、`"<https://sts.windows-ppe.net/>"` または `"<https://sts.windows.net/>"` 以外の**プロバイダー**を持ちます。</span><span class="sxs-lookup"><span data-stu-id="4799f-323">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file has a **Provider** other than `"<https://sts.windows-ppe.net/>"` or `"<https://sts.windows.net/>"`.</span></span> <span data-ttu-id="4799f-324">場合によっては、管理者ユーザーの**プロバイダ**フィールドに会社固有のドメインを含めます。</span><span class="sxs-lookup"><span data-stu-id="4799f-324">Sometimes, a company-specific domain is included in the **Provider** field for the admin user.</span></span> <span data-ttu-id="4799f-325">この問題を回避するには、Finance and Operations で、任意の名前と電子メール アドレスを持つユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4799f-325">To work around this issue, in Finance and Operations, create a user who has any name and email address.</span></span> <span data-ttu-id="4799f-326">システム管理者ロールを新しいユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4799f-326">Assign the System Administrator role to the new user.</span></span> <span data-ttu-id="4799f-327">ユーザーを実在の Azure Active Directory ユーザーにリンクする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4799f-327">You don't have to link the user to a real Azure Active Directory user.</span></span> <span data-ttu-id="4799f-328">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。</span><span class="sxs-lookup"><span data-stu-id="4799f-328">Specify this new admin user as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span>

### <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a><span data-ttu-id="4799f-329">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="4799f-329">The HTTP request was forbidden with client authentication scheme 'Anonymous'</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-330">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-330">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'. ---> System.Net.WebException: The remote server returned an error: (403) Forbidden..
```

#### <a name="solution"></a><span data-ttu-id="4799f-331">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-331">Solution</span></span>

<span data-ttu-id="4799f-332">既知の 2 つのシナリオでは、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-332">Two known scenarios can cause this error:</span></span>

- <span data-ttu-id="4799f-333">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</span><span class="sxs-lookup"><span data-stu-id="4799f-333">The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</span></span> <span data-ttu-id="4799f-334">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4799f-334">Here is an example.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe
    ```

    <span data-ttu-id="4799f-335">CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスは正しくフォーマットされません。</span><span class="sxs-lookup"><span data-stu-id="4799f-335">If the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</span></span> <span data-ttu-id="4799f-336">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="4799f-336">If these users are used to run the tests, the tests will generate the forbidden request error.</span></span> <span data-ttu-id="4799f-337">このシナリオで Microsoft Dynamics 365 for Finance and Operations のユーザーを表示することによってエラーが発生することを確認できますします。</span><span class="sxs-lookup"><span data-stu-id="4799f-337">You can verify that this scenario is causing the error by viewing the users in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="4799f-338">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</span><span class="sxs-lookup"><span data-stu-id="4799f-338">The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</span></span>

    <span data-ttu-id="4799f-339">[![電子メール アドレスの設定が正しくない](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</span><span class="sxs-lookup"><span data-stu-id="4799f-339">[![Incorrectly formatted email addresses](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</span></span>

    <span data-ttu-id="4799f-340">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4799f-340">To resolve the issue, delete the test users who have incorrectly formatted email addresses.</span></span> <span data-ttu-id="4799f-341">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を指定します。</span><span class="sxs-lookup"><span data-stu-id="4799f-341">Rerun the CreateUsers script, and specify the user count and company as shown here.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

- <span data-ttu-id="4799f-342">CloudEnvironment.Config ファイルの **UserCount** フィールドで指定したユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えます。</span><span class="sxs-lookup"><span data-stu-id="4799f-342">The number of users that you specify in the **UserCount** field in the CloudEnvironment.Config file exceeds the number of test users that you created by running MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="4799f-343">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-343">Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</span></span>
 
    ![クラウド環境のコンフィギュレーション](./media/cloud-env-config.png)

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="4799f-345">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="4799f-345">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="4799f-346">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-346">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="4799f-347">AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-347">It tends to occur when the AOS machine differs from the developer machine.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="4799f-348">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-348">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a><span data-ttu-id="4799f-349">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-349">Solution</span></span>

<span data-ttu-id="4799f-350">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-350">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="4799f-351">2 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="4799f-351">There are two possible causes:</span></span>

- <span data-ttu-id="4799f-352">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="4799f-352">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="4799f-353">問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、インストールします。</span><span class="sxs-lookup"><span data-stu-id="4799f-353">To fix the issue, copy the .cer file that you created earlier in this topic to the AOS machine, and install it.</span></span>
- <span data-ttu-id="4799f-354">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="4799f-354">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="4799f-355">問題を解決するには、wif.config ファイルに証明書を追加する方法について、「パフォーマンス SDK を使用してシングル ユーザーのパフォーマンス テストを実行する」の手順 8 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4799f-355">To fix the issue, see step 8 in the "Run a single-user performance test by using the Performance SDK" section for information about how to add the certificate to the wif.config file.</span></span> <span data-ttu-id="4799f-356">wif.config ファイルを変更した後は、必ず IIS を再起動してください。</span><span class="sxs-lookup"><span data-stu-id="4799f-356">Be sure to restart IIS after you modify the wif.config file.</span></span>
 
### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="4799f-357">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="4799f-357">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="4799f-358">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-358">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-359">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-359">Error example</span></span>

```
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a><span data-ttu-id="4799f-360">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-360">Solution</span></span>

<span data-ttu-id="4799f-361">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-361">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="4799f-362">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-362">Verify whether the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span> 

<span data-ttu-id="4799f-363">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="4799f-363">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="4799f-364">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="4799f-364">If the file is missing, add it to the deployment items in the test settings.</span></span>
 
> [!IMPORTANT]
> <span data-ttu-id="4799f-365">非常に似た名前を持つ 2 つのファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="4799f-365">There are two files that have very similar names.</span></span> <span data-ttu-id="4799f-366">1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4799f-366">The name of one file ends in **\*.dll**, and the name of the other file ends in **\*.dll.config**. The **\*.dll.config** file must be in the deployment items in the test settings.</span></span>
 
### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="4799f-367">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="4799f-367">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="4799f-368">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-368">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-369">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-369">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a><span data-ttu-id="4799f-370">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-370">Solution</span></span>

<span data-ttu-id="4799f-371">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-371">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="4799f-372">この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-372">The issue typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="4799f-373">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4799f-373">Verify whether the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="4799f-374">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="4799f-374">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="4799f-375">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="4799f-375">If the file is missing, add it to the deployment items in the test settings.</span></span>

![テスト設定](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a><span data-ttu-id="4799f-377">InteractiveClientId は設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="4799f-377">InteractiveClientId wasn't specified in the settings</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-378">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-378">Error example</span></span>

```
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a><span data-ttu-id="4799f-379">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-379">Solution</span></span>

<span data-ttu-id="4799f-380">この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-380">This issue occurs when the **SelfSigningCertificateThumbprint** field is left blank in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="4799f-381">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4799f-381">In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</span></span>

```
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="4799f-382">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="4799f-382">The remote host forcibly closed an existing connection</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-383">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-383">Error example</span></span>

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

#### <a name="solution"></a><span data-ttu-id="4799f-384">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-384">Solution</span></span>

<span data-ttu-id="4799f-385">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4799f-385">Run the following Windows PowerShell script on the development machine.</span></span>

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="4799f-386">コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="4799f-386">Service w3svc was not found on computer</span></span>

<span data-ttu-id="4799f-387">このエラーは、 Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="4799f-387">This error only occurs when you run load tests by using Visual Studio Online.</span></span>

#### <a name="error-example"></a><span data-ttu-id="4799f-388">エラーの例</span><span class="sxs-lookup"><span data-stu-id="4799f-388">Error example</span></span>
```
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a><span data-ttu-id="4799f-389">ソリューション</span><span class="sxs-lookup"><span data-stu-id="4799f-389">Solution</span></span>

<span data-ttu-id="4799f-390">この問題を解決する修正プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="4799f-390">A hotfix is available that resolves this issue.</span></span> <span data-ttu-id="4799f-391">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="4799f-391">The Microsoft Knowledge Base (KB) number is 4095640.</span></span>
