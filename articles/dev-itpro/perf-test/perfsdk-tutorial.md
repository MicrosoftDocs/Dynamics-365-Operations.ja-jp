---
title: "パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト"
description: "このトピックでは、Performance SDK について説明し、Visual Studio Online を使用してマルチユーザー テストを行う方法を示します。"
author: jujoh
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f2e3a40f58b57785079e1940b2d24a3598a3ad1b
ms.openlocfilehash: a67ba9129c8c6aed252da83d0018358868da97b7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="performance-sdk-and-multiuser-testing-via-visual-studio-online"></a><span data-ttu-id="fb7ae-103">パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="fb7ae-103">Performance SDK and multiuser testing via Visual Studio Online</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb7ae-104">このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) について説明し、Microsoft Visual Studio Online を使用してマルチユーザー テストを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-104">This topic describes the Performance software development kit (SDK) and shows how to do multiuser testing via Microsoft Visual Studio Online.</span></span> <span data-ttu-id="fb7ae-105">また、タスク レコーダーで記録したシナリオをシングルユーザー テスト、そしてマルチユーザー テストに変換する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-105">It also describes how to convert a scenario that you recorded in Task recorder to a single-user test and then a multiuser test.</span></span>

> [!NOTE]
> <span data-ttu-id="fb7ae-106">管理者として環境を利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-106">You must have access the environment as an administrator.</span></span> <span data-ttu-id="fb7ae-107">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-107">For more information, see [Access instances](../dev-tools/access-instances.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fb7ae-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="fb7ae-108">Prerequisites</span></span>

- <span data-ttu-id="fb7ae-109">Microsoft Visual Studio 2015 Enterprise</span><span class="sxs-lookup"><span data-stu-id="fb7ae-109">Microsoft Visual Studio 2015 Enterprise</span></span>
- <span data-ttu-id="fb7ae-110">数量データを含むデプロイメント</span><span class="sxs-lookup"><span data-stu-id="fb7ae-110">A deployment that has volume data</span></span>
- <span data-ttu-id="fb7ae-111">パフォーマンス SDK (SDK は K:\\PerfSDK\\PerfSDKLocalDirectory にある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-111">The Performance SDK (The SDK will likely be in K:\\PerfSDK\\PerfSDKLocalDirectory.</span></span> <span data-ttu-id="fb7ae-112">ただし、環境によっては C:\\PerfSDK にある可能性があります。)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-112">However, depending on your environment, it might be in C:\\PerfSDK.)</span></span>

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a><span data-ttu-id="fb7ae-113">XML 記録からシングル ユーザー C# テストを作成する</span><span class="sxs-lookup"><span data-stu-id="fb7ae-113">Create a single-user C# test from an XML recording</span></span>

<!--To view a video that shows how to create a single-user test, go to [https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3).-->

1. <span data-ttu-id="fb7ae-114">タスク レコーダーを使用して、テストするシナリオの記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-114">Use Task recorder to create a recording of the scenario that you want to test.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="fb7ae-115">既定のダッシュ ボード ページでレコードが起動しない場合、テストを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-115">If your recording doesn't start on the default dashboard page, the test won't be able to run.</span></span>

2. <span data-ttu-id="fb7ae-116">Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-116">Start Microsoft Visual Studio as an administrator, and build the **PerfSDKSample** project.</span></span> <span data-ttu-id="fb7ae-117">このプロジェクトは **PerfSDK** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-117">This project is in the **PerfSDK** folder.</span></span> <span data-ttu-id="fb7ae-118">プロジェクトを既に構築している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-118">If you've already built the project, skip this step.</span></span>
3. <span data-ttu-id="fb7ae-119">**Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-119">Select **Dynamics 365** &gt; **Addins** &gt; **Create C# perf test from recording**.</span></span>
4. <span data-ttu-id="fb7ae-120">**タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-120">In the **Import Task Recording** dialog box, enter the required details, and then select **Import**.</span></span>

    <span data-ttu-id="fb7ae-121">[![インポート タスク記録 ダイアログ ボックス](./media/perf103a.png)](./media/perf103a.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-121">[![Import Task Recording dialog box](./media/perf103a.png)](./media/perf103a.png)</span></span>

    <span data-ttu-id="fb7ae-122">C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-122">A C# test is generated in the Generated folder for the project that you selected.</span></span>

## <a name="run-a-single-user-performance-test-by-using-the-performance-sdk"></a><span data-ttu-id="fb7ae-123">パフォーマンス SDK を使用して単一ユーザー パフォーマンス テストを実行</span><span class="sxs-lookup"><span data-stu-id="fb7ae-123">Run a single-user performance test by using the Performance SDK</span></span>

1. <span data-ttu-id="fb7ae-124">Microsoft Windows のコントロール パネルで、**システムとセキュリティ** &gt; **システム** &gt; **システムの詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-124">In Control Panel in Microsoft Windows, select **System and Security** &gt; **System** &gt; **Advanced System Settings**.</span></span> <span data-ttu-id="fb7ae-125">**TestRoot**環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-125">Verify that the **TestRoot** environment variable is set to the path of the PerfSDK folder.</span></span>

    <span data-ttu-id="fb7ae-126">[![EnvironmentVariable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-126">[![EnvironmentVariable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)</span></span>

2. <span data-ttu-id="fb7ae-127">[http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-127">Download the **selenium-dotnet-strongnamed-2.42.0.zip** and **IEDriverServer\_Win32\_2.42.0.zip** files from [http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/).</span></span>
3. <span data-ttu-id="fb7ae-128">ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-128">Extract the files.</span></span> <span data-ttu-id="fb7ae-129">動的リンク ライブラリ (DLL) を、**selenium-dotnet-strongnamed-2.42.0.zip\net40** フォルダから **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-129">Copy the dynamic-link libraries (DLLs) from the **selenium-dotnet-strongnamed-2.42.0.zip\net40** folder to the **PerfSDK\\Common\\External\\Selenium** folder.</span></span>  <span data-ttu-id="fb7ae-130">**IEDriverServer.exe** を、**IEDriverServer_Win32_2.42.0.zip** から **PerfSDK\\Common\\External\\Selenium** フォルダにもコピーします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-130">Copy the **IEDriverServer.exe** from the **IEDriverServer_Win32_2.42.0.zip** to the **PerfSDK\\Common\\External\\Selenium** folder as well.</span></span>

    <span data-ttu-id="fb7ae-131">[![PerfSDK\Common\External\Selenium フォルダーにある DLL](./media/perf103d.png)](./media/perf103d.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-131">[![DLLs in the PerfSDK\Common\External\Selenium folder](./media/perf103d.png)](./media/perf103d.png)</span></span>

4. <span data-ttu-id="fb7ae-132">**PerfSDK\\Common\\External\\Selenium** フォルダーの **WebDriver.dll** への参照を、Visual Studio プロジェクトへ追加します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-132">Add a reference to the **WebDriver.dll** in the **PerfSDK\\Common\\External\\Selenium** folder to your Visual Studio project.</span></span>    

5. <span data-ttu-id="fb7ae-133">証明書を生成しインストールします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-133">Generate and install a certificate.</span></span> <span data-ttu-id="fb7ae-134">証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-134">To generate a certificate file, open a Command Prompt window as an administrator, and run the following commands.</span></span> <span data-ttu-id="fb7ae-135">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-135">When you're prompted for a private key password, select **None**.</span></span>

    ```
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="fb7ae-136">これらのコマンドでは次の要素を注意してください。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-136">Note the following elements in these commands:</span></span>

    - <span data-ttu-id="fb7ae-137">**-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-137">**-n "CN=127.0.0.1"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="fb7ae-138">この証明書の名前が **127.0.0.1** であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-138">It's very important that the name of this certificate be **127.0.0.1**.</span></span> <span data-ttu-id="fb7ae-139">それ以外の場合は、単一ユーザー テストは実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-139">Otherwise, the single-user tests won't be able to run.</span></span>
    - <span data-ttu-id="fb7ae-140">**-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-140">**-eku 1.3.6.1.5.5.7.3.1** gives the purpose of the certificate.</span></span> <span data-ttu-id="fb7ae-141">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-141">It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</span></span>

    <span data-ttu-id="fb7ae-142">スクリプトの実行が終了した後、**c:\\Temp** で以下のファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-142">After the script has finished running, you should see the following files in **C:\\Temp**:</span></span>

    - <span data-ttu-id="fb7ae-143">authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="fb7ae-143">authcert.pfx</span></span>
    - <span data-ttu-id="fb7ae-144">authcert.cer</span><span class="sxs-lookup"><span data-stu-id="fb7ae-144">authcert.cer</span></span> 
    - <span data-ttu-id="fb7ae-145">authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="fb7ae-145">authcert.pvk</span></span>

6. <span data-ttu-id="fb7ae-146">**authcert.pfx** および **authcert.cer** 証明書ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-146">Install the **authcert.pfx** and **authcert.cer** certificate files.</span></span> <span data-ttu-id="fb7ae-147">これらのファイルをインストールするときは、**ローカル コンピューター**をかならず選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-147">When you install these files, make sure that you select **Local Machine**.</span></span> <span data-ttu-id="fb7ae-148">**authcert.pfx** ファイルを **PerfSDK** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-148">Copy the **authcert.pfx** file to the **PerfSDK** folder.</span></span>
7. <span data-ttu-id="fb7ae-149">管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-149">Open a Microsoft Windows PowerShell window as an administrator, and run the following commands to get the thumbprint of the installed certificate.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

8. <span data-ttu-id="fb7ae-150">**CloudEnvironment.Config** ファイルで、**SelfSigningCertificateThumbprint** キーの値として拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-150">In the **CloudEnvironment.Config** file, enter the thumbprint as the value for the **SelfSigningCertificateThumbprint** key.</span></span>

    <span data-ttu-id="fb7ae-151">[![更新された CloudEnvironment.Config ファイル](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-151">[![Updated CloudEnvironment.Config file](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span></span>

9. <span data-ttu-id="fb7ae-152">**wif.config** ファイルを更新して Application Object Server (AOS) が証明書を信頼できるようにするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-152">Follow these steps to update the **wif.config** file so that Application Object Server (AOS) trusts the certificate:</span></span>

    1. <span data-ttu-id="fb7ae-153">Microsoft インターネット インフォメーション サービス (IIS) を起動し、サイトの一覧で **Microsoft Dynamics 365 for Finance and Operations** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-153">Start Microsoft Internet Information Services (IIS), and find **Microsoft Dynamics 365 for Finance and Operations** in the list of sites.</span></span>
    2. <span data-ttu-id="fb7ae-154">**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-154">Select **Explore**, and find the **wif.config** file.</span></span>

        <span data-ttu-id="fb7ae-155">[![wif.config ファイル](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-155">[![wif.config file](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span></span>

    3. <span data-ttu-id="fb7ae-156">**Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-156">In the **wif.config** file, find the authority that is named **AxTokenIssuer**.</span></span> <span data-ttu-id="fb7ae-157">この権限の捺印のリストに捺印を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-157">You must add your thumbprint to the list of thumbprints for this authority.</span></span>

        <span data-ttu-id="fb7ae-158">[![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-158">[![Thumbprint added to the list of authorities for AxTokenIssuer](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span></span>

    4. <span data-ttu-id="fb7ae-159">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-159">Restart IIS.</span></span>

10. <span data-ttu-id="fb7ae-160">Visual Studio で、**PerfSDKSample** プロジェクトを開き、**PurchaseReq.cs** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-160">In Visual Studio, open the **PerfSDKSample** project, and find the **PurchaseReq.cs** file.</span></span> <span data-ttu-id="fb7ae-161">このファイルは、サンプル シングルユーザー テストです。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-161">This file is a sample single-user test.</span></span> <span data-ttu-id="fb7ae-162">ファイルで、次の行をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-162">In the file, comment out the following lines.</span></span>

    ```
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    <span data-ttu-id="fb7ae-163">[![PurchaseReq.cs でコメント アウトされた行](./media/perf103e.png)](./media/perf103e.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-163">[![Lines commented out in PurchaseReq.cs](./media/perf103e.png)](./media/perf103e.png)</span></span>

11. <span data-ttu-id="fb7ae-164">管理者のユーザー名を入力することによって **CloudEnvironment.Config** ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-164">Modify the **CloudEnvironment.Config** file by entering your admin user name.</span></span> <span data-ttu-id="fb7ae-165">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-165">Here is an example.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb7ae-166">**ConfigName** は **DEVFABRIC** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-166">**ConfigName** must be set to **DEVFABRIC**.</span></span> 

    <span data-ttu-id="fb7ae-167">[![変更された CloudEnvironment.Config ファイル](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-167">[![Modified CloudEnvironment.Config file](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG)</span></span> 

12. <span data-ttu-id="fb7ae-168">**CloudEnvironment.Config** ファイルに、エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-168">In the **CloudEnvironment.Config** file, enter your endpoint.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb7ae-169">環境をアプリケーション リクエスト ルーティング (ARR) に対して有効にするには、2 つのエンドポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-169">If the environment is enabled for Application Request Routing (ARR), you have two endpoints.</span></span> <span data-ttu-id="fb7ae-170">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-170">Here is an example:</span></span>
    >
    > - <span data-ttu-id="fb7ae-171">apr-arr8aos**soap**.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="fb7ae-171">apr-arr8aos**soap**.axcloud.test.dynamics.com</span></span>
    > - <span data-ttu-id="fb7ae-172">apr-arr8aos.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="fb7ae-172">apr-arr8aos.axcloud.test.dynamics.com</span></span>
    >
    > <span data-ttu-id="fb7ae-173">この場合、CloudEnvironment.Config ファイルに両方のエンドポイントを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-173">In this case, you must enter both endpoints in the CloudEnvironment.Config file.</span></span>
    >
    > <span data-ttu-id="fb7ae-174">[![CloudEnvironment.Config のエンドポイント](./media/perf103upd.png)](./media/perf103upd.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-174">[![Endpoints in CloudEnvironment.Config](./media/perf103upd.png)](./media/perf103upd.png)</span></span>

13. <span data-ttu-id="fb7ae-175">**テスト** &gt; **テストの設定** を選択し、**既定のプロセッサ アーキテクチャ** を **x64** に設定してソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-175">Select **Test** &gt; **Test settings**, set **Default processor architecture** to **x64**, and then build the solution.</span></span>
14. <span data-ttu-id="fb7ae-176">**テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-176">Select **Test** &gt; **Windows** &gt; **Test Explorer** to view the list of tests.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb7ae-177">場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-177">Sometimes, Visual Studio might not update the list of tests after you create a test script from a task recording.</span></span> <span data-ttu-id="fb7ae-178">この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-178">In this case, restart Visual Studio, and then reopen Test Explorer.</span></span>

    <span data-ttu-id="fb7ae-179">新しいテストに **TestMethod** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-179">Your new test will be named **TestMethod**.</span></span> <span data-ttu-id="fb7ae-180">TestMethod のメソッド名を変更すると、個々の名前がテストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-180">If you change the method name of TestMethod, your test will receive an individual name.</span></span> 

<span data-ttu-id="fb7ae-181">テストを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-181">You can now run the test.</span></span> <span data-ttu-id="fb7ae-182">テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-182">When you run the test, Internet Explorer should be started, and it should replay the scenario that you recorded.</span></span>

## <a name="create-a-multiuser-test-from-a-single-user-test"></a><span data-ttu-id="fb7ae-183">シングル ユーザー テストからマルチ ユーザー テストを作成する</span><span class="sxs-lookup"><span data-stu-id="fb7ae-183">Create a multiuser test from a single-user test</span></span>

<span data-ttu-id="fb7ae-184">以前のセクションで情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-184">After you create a single-user test by using the information in the previous section, you can convert it to a multiuser test.</span></span> <span data-ttu-id="fb7ae-185">テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-185">Add **MS.Dynamics.TestTools.UIHelpers.Core;** to your test script, and find the following line in the **TestSetup** method.</span></span>

```
Client = DispatchedClient.DefaultInstance;
```

<span data-ttu-id="fb7ae-186">その行を以下の行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-186">Replace that line with the following lines.</span></span>

```
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

<span data-ttu-id="fb7ae-187">タスクのインポーターによって生成されたテスト スクリプトには次の明細行と似ている明細行が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-187">The test script that was generated by the Task Importer might contain a line that resembles the following line.</span></span>

```
UserContextRole _context = new UserContextRole(UserManagement.AdminUser);
```

<span data-ttu-id="fb7ae-188">ロード テストとして実行される任意のテストからこの明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-188">Remove this line from any tests that will be run as load tests.</span></span> <span data-ttu-id="fb7ae-189">このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-189">This code is required only for single-user tests and has a negative effect on the performance of load tests.</span></span>

<span data-ttu-id="fb7ae-190">タスク記録が行われたときに入力した値がランダム化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-190">Make sure that the values that you entered when you made the task recording are randomized.</span></span> <span data-ttu-id="fb7ae-191">テスト データを生成するために、データ拡張ツールを最初に使用することが必要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-191">You might have to use the Data Expansion Tool first to generate test data.</span></span>

## <a name="set-up-visual-studio-team-services-for-multiuser-testing"></a><span data-ttu-id="fb7ae-192">Visual Studio Team Services でマルチ ユーザー テストを設定</span><span class="sxs-lookup"><span data-stu-id="fb7ae-192">Set up Visual Studio Team Services for multiuser testing</span></span>

<span data-ttu-id="fb7ae-193">この例では、ユーザーは ProcureToPay.cs ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-193">For this example, you will use the ProcureToPay.cs file.</span></span> <span data-ttu-id="fb7ae-194">Visual Studio を開始するには、[Visual Studio Team Services portal ポータル](https://app.vssps.visualstudio.com/profile/view) にサインインし、**Visual Studio で開く**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-194">To start Visual Studio, you must sign in to the [Visual Studio Team Services portal](https://app.vssps.visualstudio.com/profile/view), and then select **Open in Visual Studio**.</span></span>

> [!NOTE]
> <span data-ttu-id="fb7ae-195">このステップは 1 回のみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-195">You must complete this step only one time.</span></span> <span data-ttu-id="fb7ae-196">Visual Studio Team Services にサインインした後、設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-196">After you've signed in to Visual Studio Team Services, the settings are saved.</span></span>

<span data-ttu-id="fb7ae-197">[![Visual Studio で開きます](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-197">[![Open in Visual Studio](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span></span>

1. <span data-ttu-id="fb7ae-198">**PerfSDKSample** プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-198">Open the **PerfSDKSample** project.</span></span>
2. <span data-ttu-id="fb7ae-199">**CloudEnvironment.Config** ファイルで、**UserFormat** エントリを更新して、管理者ユーザー URL を反映します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-199">In the **CloudEnvironment.Config** file, update the **UserFormat** entry so that it reflects the admin user URL.</span></span> <span data-ttu-id="fb7ae-200">たとえば、`admin@example.com` に対して、ユーザー形式として **TST\_{0}@example.com** を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-200">For example, for `admin@example.com`, use **TST\_{0}@example.com** as the user format.</span></span> <span data-ttu-id="fb7ae-201">また、**UserCount** 値をパフォーマンス テストに含めるユーザーの数に変更します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-201">Additionally, change the **UserCount** value to the number of users that you want to have in your performance test.</span></span>

    <span data-ttu-id="fb7ae-202">[![更新された CloudEnvironment.Config ファイル](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-202">[![Updated CloudEnvironment.Config file](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)</span></span>

3. <span data-ttu-id="fb7ae-203">管理者モードでコマンド プロンプトを開き、**PerfSDK** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-203">Open a Command Prompt window as an administrator, and navigate to the **PerfSDK** folder.</span></span> <span data-ttu-id="fb7ae-204">次のコマンドを実行して環境のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-204">Run the following command to create test users for your environment.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

    <span data-ttu-id="fb7ae-205">必要な数のユーザーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-205">You can create as many users as you want.</span></span> <span data-ttu-id="fb7ae-206">たとえば、次のコマンドは、USMF 会社で 150 人のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-206">For example, the following command creates 150 test users for the USMF company.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe 150 USMF
    ```

4. <span data-ttu-id="fb7ae-207">管理者ユーザーとしてエンドポイントにログインし、ユーザーがシステムで作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-207">Sign in to your endpoint as the admin user, and verify that users were created in the system.</span></span>

### <a name="test-the-sandbox-environment"></a><span data-ttu-id="fb7ae-208">サンドボックス環境をテスト</span><span class="sxs-lookup"><span data-stu-id="fb7ae-208">Test the sandbox environment</span></span>

<span data-ttu-id="fb7ae-209">ここまでは、手順で、AOS マシンが開発マシンでもある開発者トポロジを使用していることを前提としていました。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-209">Up to this point, the instructions have assumed that you have a developer topology where the AOS machine is also your development machine.</span></span> <span data-ttu-id="fb7ae-210">Visual Studio Team Services でロード テストを実行するには、テスト環境がサンドボックス環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-210">To run load tests in Visual Studio Team Services, the environment that you test must be a sandbox environment.</span></span> <span data-ttu-id="fb7ae-211">サンドボックス環境と負荷テストを実行するコンピューター間の信頼関係を確立するには、いくつかの追加手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-211">You must complete a few additional steps to establish trust between the sandbox environment and the computer that runs the load tests.</span></span> <span data-ttu-id="fb7ae-212">負荷テストを実行するコンピューターは、開発マシンまたは Visual Studio Online で作成されたテスト エージェントのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-212">The computer that runs the load tests can be either your development machine or the test agent that is created by Visual Studio Online.</span></span>

1. <span data-ttu-id="fb7ae-213">サンドボックス AOS マシンへのリモート デスクトップ の接続を確立し、**.cer** ファイルを上書きします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-213">Establish a Remote Desktop connection to your sandbox AOS machine, and copy over the **.cer** file.</span></span> <span data-ttu-id="fb7ae-214">ファイルをダブルクリックして、インストールします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-214">Double-click the file to install it.</span></span> <span data-ttu-id="fb7ae-215">証明書ストアの入力を要求するメッセージが表示されたら、**個人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-215">When you're prompted for the certificate store, select **Personal**.</span></span>
2. <span data-ttu-id="fb7ae-216">IIS を起動し、サイトの一覧で **AOSService** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-216">Start IIS, and find **AOSService** in the list of sites.</span></span> <span data-ttu-id="fb7ae-217">その後、**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-217">Then select **Explore**, and find the **wif.config** file.</span></span> <span data-ttu-id="fb7ae-218">**Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-218">In the **wif.config** file, find the authority that is named **AxTokenIssuer**.</span></span> <span data-ttu-id="fb7ae-219">この権限の捺印のリストに捺印を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-219">You must add your thumbprint to the list of thumbprints for this authority.</span></span> <span data-ttu-id="fb7ae-220">(以前に生成した証明書の値を使用します。)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-220">(Use the values from the certificate that you generated earlier.)</span></span>

    <span data-ttu-id="fb7ae-221">[![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-221">[![Thumbprint added to the list of authorities for AxTokenIssuer](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)</span></span>

3. <span data-ttu-id="fb7ae-222">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-222">Restart IIS.</span></span>

<span data-ttu-id="fb7ae-223">トポロジに対してパフォーマンス テストを実行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-223">You can now run performance tests against the topology.</span></span>

> [!NOTE]
> <span data-ttu-id="fb7ae-224">トポロジに複数の AOS マシンがある場合、証明書をインストールして、各 AOS マシンの wif.config ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-224">If your topology has multiple AOS machines, you must install the certificate and update the wif.config file on every AOS machine.</span></span>

## <a name="run-the-performance-test"></a><span data-ttu-id="fb7ae-225">パフォーマンス テストの実行</span><span class="sxs-lookup"><span data-stu-id="fb7ae-225">Run the performance test</span></span>

1. <span data-ttu-id="fb7ae-226">Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-226">In the Visual Studio editor, open the **ProcureToPay.cs** file, and append the following lines in the **TestSetup** method.</span></span>

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

2. <span data-ttu-id="fb7ae-227">[https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420)から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-227">Download the installer (.msi) file for Microsoft ODBC Driver 13 for SQL Server from [https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420).</span></span> <span data-ttu-id="fb7ae-228">(64 ビット バージョンの .msi ファイルを選択します。) ファイルを **PerfSDK** ディレクトリの **Visual Studio Online** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-228">(Select the 64-bit version of the .msi file.) Put the file in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
3. <span data-ttu-id="fb7ae-229">**Visual Studio Online** フォルダで **setup.cmd** ファイルの内容を変更し、次のコードと一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-229">Modify the contents of the **setup.cmd** file in the **Visual Studio Online** folder so that they match the following code.</span></span>

    ```
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

4. <span data-ttu-id="fb7ae-230">**CloudCtuFakeACSInstall.cmd** ファイルの内容を変更して、**インポート**コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-230">Modify the contents of the **CloudCtuFakeACSInstall.cmd** file so that the **Import** command has an empty string instead of **'password'**.</span></span> <span data-ttu-id="fb7ae-231">スクリプトの 3 行目は、次の行に似ているはずです。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-231">The third line of the script should resemble the following line.</span></span>

    ```
    set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....
    ```

5. <span data-ttu-id="fb7ae-232">ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-232">In your solution files, double-click the **vsonline.testsettings** file to modify the test settings.</span></span>
6. <span data-ttu-id="fb7ae-233">**テストの設定**ダイアログ ボックスの**配置**タブで、次の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-233">In the **Test Settings** dialog box, on the **Deployment** tab, use the following settings:</span></span>

    - <span data-ttu-id="fb7ae-234">**展開の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-234">Select the **Enable deployment** check box.</span></span>
    - <span data-ttu-id="fb7ae-235">**配置する追加のファイルやディレクトリ** フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-235">In the **Additional files and directories to deploy** field, make sure that the following files and directories are listed:</span></span>

        - <span data-ttu-id="fb7ae-236">&lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\</span><span class="sxs-lookup"><span data-stu-id="fb7ae-236">&lt;Solution Directory&gt;\\PerfSDKSample\\bin\\Debug\\</span></span>
        - <span data-ttu-id="fb7ae-237">C:\\PerfSDK\\CloudEnvironment.Config</span><span class="sxs-lookup"><span data-stu-id="fb7ae-237">C:\\PerfSDK\\CloudEnvironment.Config</span></span>
        - <span data-ttu-id="fb7ae-238">C:\\PerfSDK\\authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="fb7ae-238">C:\\PerfSDK\\authcert.pfx</span></span>
        - <span data-ttu-id="fb7ae-239">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span><span class="sxs-lookup"><span data-stu-id="fb7ae-239">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span></span>
        - <span data-ttu-id="fb7ae-240">C:\\PerfSDK\\Visual Studio Online\\</span><span class="sxs-lookup"><span data-stu-id="fb7ae-240">C:\\PerfSDK\\Visual Studio Online\\</span></span>

        <span data-ttu-id="fb7ae-241">[![フィールドを配置するための追加ファイルおよびディレクトリ](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-241">[![Additional files and directories to deploy field](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)</span></span>

        > [!NOTE]
        > <span data-ttu-id="fb7ae-242">PerfSDK フォルダーが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-242">Your PerfSDK folder might differ.</span></span>

7. <span data-ttu-id="fb7ae-243">**スクリプトの設定とクリーンアップ**タブで、**PerfSDK** ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-243">On the **Setup and Cleanup Scripts** tab, select the **setup.cmd** file that is in the **Visual Studio Online** folder in the **PerfSDK** directory.</span></span>
8. <span data-ttu-id="fb7ae-244">**追加設定**タブで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-244">On the **Additional Settings** tab, select **Run tests in 64 bit process on 64 bit machine**.</span></span>
9. <span data-ttu-id="fb7ae-245">テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-245">To run the test, open the **SampleLoadTest.loadtest** file, and select **Run Load Test**.</span></span>

    <span data-ttu-id="fb7ae-246">[![負荷テストの実行](./media/perf103u.png)](./media/perf103u.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-246">[![Run Load Test](./media/perf103u.png)](./media/perf103u.png)</span></span>

    <span data-ttu-id="fb7ae-247">テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-247">When the test has finished running, you should see a summary that shows transaction results.</span></span> <span data-ttu-id="fb7ae-248">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-248">Here is an example.</span></span>

    <span data-ttu-id="fb7ae-249">[![トランザクションの結果](./media/perf103v.png)](./media/perf103v.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-249">[![Transaction results](./media/perf103v.png)](./media/perf103v.png)</span></span>

10. <span data-ttu-id="fb7ae-250">テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-250">To view various indicators for the test controller and test scenario, you can switch to the **Graphs** view.</span></span>

    <span data-ttu-id="fb7ae-251">[![グラフ 表示](./media/perf103w.png)](./media/perf103w.png)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-251">[![Graphs view](./media/perf103w.png)](./media/perf103w.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb7ae-252">テストの実行中、システムに関する情報はこのビューで利用することができません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-252">While tests are being run, information about your system isn't available in this view.</span></span> <span data-ttu-id="fb7ae-253">この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-253">To access this information, you must use Microsoft Dynamics Lifecycle Services (LCS) to monitor the CPU and memory usage of your AOS machine.</span></span> <span data-ttu-id="fb7ae-254">または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-254">Alternatively, you can set up perfmon directly on the AOS machine and set up the Microsoft Azure portal to monitor Microsoft SQL Server usage of Database Transaction Units (DTUs).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fb7ae-255">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="fb7ae-255">Troubleshooting</span></span>

### <a name="no-client-was-opened-in-the-time-out-period"></a><span data-ttu-id="fb7ae-256">タイムアウト期間中クライアントが開かれていません</span><span class="sxs-lookup"><span data-stu-id="fb7ae-256">No client was opened in the time-out period</span></span>
<span data-ttu-id="fb7ae-257">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-257">This issue affects only single-user tests.</span></span> <span data-ttu-id="fb7ae-258">テストが実行されているとき、Web クライアントを開きますが、Web サイトが読み込まれることはありません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-258">When the test is running, a web client opens, but a website is never loaded.</span></span> <span data-ttu-id="fb7ae-259">代わりに、白い画面を持つ空の Web クライアントがある場合、ページの上部で次のメッセージが表示されます: 「これは WebDriver サーバーの初期開始ページです。」</span><span class="sxs-lookup"><span data-stu-id="fb7ae-259">Instead, there is an empty web client that has a white screen, and the following message appears at the top of the page: "This is the initial start page for the WebDriver server."</span></span> <span data-ttu-id="fb7ae-260">テストは最終的にタイム アウトおよび失敗し、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-260">The test will eventually time out and fail, and an error message will be shown.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-261">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-261">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-262">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-262">Solution</span></span>
<span data-ttu-id="fb7ae-263">このトピックの「パフォーマンス SDK を使用してシングル ユーザー パフォーマンス テストを実行する」セクションの、手順 4 から 8 を実行します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-263">Follow steps 4 through 8 in the "Run a single-user performance test by using the Performance SDK" section of this topic.</span></span> <span data-ttu-id="fb7ae-264">そのセクションでは、このタイプのテストの正しい証明書を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-264">That section explains how to create a correct certificate for this type of test.</span></span> <span data-ttu-id="fb7ae-265">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-265">It also explains how to add the thumbprint of the certificate to the wif.config file.</span></span>

### <a name="zoom-factor"></a><span data-ttu-id="fb7ae-266">ズーム係数</span><span class="sxs-lookup"><span data-stu-id="fb7ae-266">Zoom factor</span></span>

<span data-ttu-id="fb7ae-267">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-267">This issue affects only single-user tests.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="fb7ae-268">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-268">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-269">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-269">Solution</span></span>

<span data-ttu-id="fb7ae-270">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-270">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="fb7ae-271">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="fb7ae-271">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="fb7ae-272">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="fb7ae-272">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="fb7ae-273">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="fb7ae-273">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>
 
<span data-ttu-id="fb7ae-274">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-274">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="fb7ae-275">このフィールドは、Windows の**表示設定**で使用できます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-275">This field is available in **Display settings** in Windows.</span></span> 
 
<span data-ttu-id="fb7ae-276">これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-276">If those steps don't work, try to change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

### <a name="certificate-thumbprint-errors"></a><span data-ttu-id="fb7ae-277">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="fb7ae-277">Certificate thumbprint errors</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-278">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-278">Error example</span></span>

```
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-279">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-279">Solution</span></span>

<span data-ttu-id="fb7ae-280">次のいくつかの理由でエラー メッセージを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-280">You might receive the error message for several reasons:</span></span>

- <span data-ttu-id="fb7ae-281">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-281">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="fb7ae-282">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-282">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="fb7ae-283">たとえば、[https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/) で使用可能な Unicode コンバーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-283">For example, you can use the  Unicode converter that is available at [https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/).</span></span>

    ![Unicode コードの変換](./media/sdk_unicode_code_converter.jpg)
 
- <span data-ttu-id="fb7ae-285">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-285">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="fb7ae-286">AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-286">To verify that the certificate can be found on the AOS machine, run the following Windows PowerShell script.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    <span data-ttu-id="fb7ae-287">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-287">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate can't be found.</span></span> <span data-ttu-id="fb7ae-288">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-288">To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</span></span>
 
- <span data-ttu-id="fb7ae-289">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-289">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="fb7ae-290">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-290">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>
 
    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード](./media/set_cloudctufakeacsinstall.jpg)
 
### <a name="no-endpoint-is-listening"></a><span data-ttu-id="fb7ae-292">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="fb7ae-292">No endpoint is listening</span></span>

<span data-ttu-id="fb7ae-293">この問題は、シングルユーザーまたはマルチユーザーのテストを実行する場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-293">This issue can occur when you run single-user or multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-294">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-294">Error example</span></span>

<span data-ttu-id="fb7ae-295">テストまたはユーザー作成プロセスが失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-295">The tests or user creation process fails, and the following error message is shown.</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-296">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-296">Solution</span></span>

<span data-ttu-id="fb7ae-297">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-297">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>
 
<span data-ttu-id="fb7ae-298">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-298">In the CloudEnvironment.Config file, review the values that are specified by the following keys:</span></span>

- <span data-ttu-id="fb7ae-299">&lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="fb7ae-299">&lt;ExecutionConfigurations Key="HostName" Value="&lt;web address of host&gt;" /&gt;</span></span>
- <span data-ttu-id="fb7ae-300">&lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="fb7ae-300">&lt;ExecutionConfigurations Key="SoapHostName" Value="&lt;web address of SOAP&gt;" /&gt;</span></span>

<span data-ttu-id="fb7ae-301">これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-301">The web addresses that are specified by these keys must be the environment that you're testing.</span></span> <span data-ttu-id="fb7ae-302">開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-302">In a web browser on your developer machine, make sure that you can open the web address that is specified by the **HostName** key.</span></span>

<span data-ttu-id="fb7ae-303">オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-303">For online load tests, the environment that is specified by the **HostName** key in the CloudEnvironment.Config file must be publicly accessible from any machine.</span></span> <span data-ttu-id="fb7ae-304">したがって、1 ボックス環境をテストする必要がある場合、Visual Studio Online を使用して負荷テストを実行することはできません。これは、エンドポイントが 1 ボックス環境の外部にアクセスできないためです。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-304">Therefore, if you must test a one-box environment, you won't be able to run the load test by using Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</span></span>

### <a name="users-cant-be-enumerated"></a><span data-ttu-id="fb7ae-305">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="fb7ae-305">Users can't be enumerated</span></span>

<span data-ttu-id="fb7ae-306">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-306">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-307">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-307">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-308">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-308">Solution</span></span>

<span data-ttu-id="fb7ae-309">2 つのシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-309">Two scenarios can cause this error:</span></span>

- <span data-ttu-id="fb7ae-310">CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーはシステム管理者ロールを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-310">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file must have the System Administrator role.</span></span> <span data-ttu-id="fb7ae-311">この問題は、**SelfMintingAdminUser** として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-311">This issue occurs when the System Administrator role isn't assigned to the user who is specified as **SelfMintingAdminUser**.</span></span> <span data-ttu-id="fb7ae-312">適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-312">To verify that you've specified the correct user, you can sign in to the endpoint and view the user's roles.</span></span>

    ![管理者ユーザー](./media/sdk_admin.png)

- <span data-ttu-id="fb7ae-314">CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーは、`"<https://sts.windows-ppe.net/>"` または `"<https://sts.windows.net/>"` 以外の**プロバイダー**を持ちます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-314">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file has a **Provider** other than `"<https://sts.windows-ppe.net/>"` or `"<https://sts.windows.net/>"`.</span></span> <span data-ttu-id="fb7ae-315">場合によっては、管理者ユーザーの**プロバイダ**フィールドに会社固有のドメインを含めます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-315">Sometimes, a company-specific domain is included in the **Provider** field for the admin user.</span></span> <span data-ttu-id="fb7ae-316">この問題を回避するには、Finance and Operations で、任意の名前と電子メール アドレスを持つユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-316">To work around this issue, in Finance and Operations, create a user who has any name and email address.</span></span> <span data-ttu-id="fb7ae-317">システム管理者ロールを新しいユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-317">Assign the System Administrator role to the new user.</span></span> <span data-ttu-id="fb7ae-318">ユーザーを実在の Azure Active Directory ユーザーにリンクする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-318">You don't have to link the user to a real Azure Active Directory user.</span></span> <span data-ttu-id="fb7ae-319">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-319">Specify this new admin user as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span>

### <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a><span data-ttu-id="fb7ae-320">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="fb7ae-320">The HTTP request was forbidden with client authentication scheme 'Anonymous'</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-321">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-321">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'. ---> System.Net.WebException: The remote server returned an error: (403) Forbidden..
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-322">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-322">Solution</span></span>

<span data-ttu-id="fb7ae-323">既知の 2 つのシナリオでは、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-323">Two known scenarios can cause this error:</span></span>

- <span data-ttu-id="fb7ae-324">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-324">The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</span></span> <span data-ttu-id="fb7ae-325">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-325">Here is an example.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe
    ```

    <span data-ttu-id="fb7ae-326">CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスは正しくフォーマットされません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-326">If the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</span></span> <span data-ttu-id="fb7ae-327">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-327">If these users are used to run the tests, the tests will generate the forbidden request error.</span></span> <span data-ttu-id="fb7ae-328">このシナリオがエラーの原因であることを確認するには、Microsoft Dynamics 365 for Finance and Operations でユーザーを表示します</span><span class="sxs-lookup"><span data-stu-id="fb7ae-328">You can verify that this scenario is causing the error by viewing the users in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fb7ae-329">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-329">The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</span></span>

    <span data-ttu-id="fb7ae-330">[![電子メール アドレスの設定が正しくない](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-330">[![Incorrectly formatted email addresses](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)</span></span>

    <span data-ttu-id="fb7ae-331">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-331">To resolve the issue, delete the test users who have incorrectly formatted email addresses.</span></span> <span data-ttu-id="fb7ae-332">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-332">Rerun the CreateUsers script, and specify the user count and company as shown here.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

- <span data-ttu-id="fb7ae-333">CloudEnvironment.Config ファイルの **UserCount** フィールドで指定したユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-333">The number of users that you specify in the **UserCount** field in the CloudEnvironment.Config file exceeds the number of test users that you created by running MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="fb7ae-334">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-334">Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</span></span>
 
    ![クラウド環境のコンフィギュレーション](./media/cloud-env-config.png)

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="fb7ae-336">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="fb7ae-336">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="fb7ae-337">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-337">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="fb7ae-338">AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-338">It tends to occur when the AOS machine differs from the developer machine.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="fb7ae-339">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-339">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-340">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-340">Solution</span></span>

<span data-ttu-id="fb7ae-341">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-341">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="fb7ae-342">2 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-342">There are two possible causes:</span></span>

- <span data-ttu-id="fb7ae-343">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-343">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="fb7ae-344">問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、インストールします。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-344">To fix the issue, copy the .cer file that you created earlier in this topic to the AOS machine, and install it.</span></span>
- <span data-ttu-id="fb7ae-345">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-345">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="fb7ae-346">問題を解決するには、wif.config ファイルに証明書を追加する方法について、「パフォーマンス SDK を使用してシングル ユーザーのパフォーマンス テストを実行する」の手順 8 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-346">To fix the issue, see step 8 in the "Run a single-user performance test by using the Performance SDK" section for information about how to add the certificate to the wif.config file.</span></span> <span data-ttu-id="fb7ae-347">wif.config ファイルを変更した後は、必ず IIS を再起動してください。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-347">Be sure to restart IIS after you modify the wif.config file.</span></span>
 
### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="fb7ae-348">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="fb7ae-348">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="fb7ae-349">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-349">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-350">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-350">Error example</span></span>

```
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-351">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-351">Solution</span></span>

<span data-ttu-id="fb7ae-352">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-352">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="fb7ae-353">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-353">Verify whether the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span> 

<span data-ttu-id="fb7ae-354">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="fb7ae-354">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="fb7ae-355">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-355">If the file is missing, add it to the deployment items in the test settings.</span></span>
 
> [!IMPORTANT]
> <span data-ttu-id="fb7ae-356">非常に似た名前を持つ 2 つのファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-356">There are two files that have very similar names.</span></span> <span data-ttu-id="fb7ae-357">1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-357">The name of one file ends in **\*.dll**, and the name of the other file ends in **\*.dll.config**. The **\*.dll.config** file must be in the deployment items in the test settings.</span></span>
 
### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="fb7ae-358">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="fb7ae-358">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="fb7ae-359">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-359">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-360">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-360">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-361">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-361">Solution</span></span>

<span data-ttu-id="fb7ae-362">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-362">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="fb7ae-363">この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-363">The issue typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="fb7ae-364">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-364">Verify whether the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="fb7ae-365">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="fb7ae-365">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="fb7ae-366">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-366">If the file is missing, add it to the deployment items in the test settings.</span></span>

![テスト設定](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a><span data-ttu-id="fb7ae-368">InteractiveClientId は設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="fb7ae-368">InteractiveClientId wasn't specified in the settings</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-369">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-369">Error example</span></span>

```
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-370">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-370">Solution</span></span>

<span data-ttu-id="fb7ae-371">この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-371">This issue occurs when the **SelfSigningCertificateThumbprint** field is left blank in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="fb7ae-372">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-372">In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</span></span>

```
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="fb7ae-373">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="fb7ae-373">The remote host forcibly closed an existing connection</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-374">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-374">Error example</span></span>

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

#### <a name="solution"></a><span data-ttu-id="fb7ae-375">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-375">Solution</span></span>

<span data-ttu-id="fb7ae-376">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-376">Run the following Windows PowerShell script on the development machine.</span></span>

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="fb7ae-377">コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="fb7ae-377">Service w3svc was not found on computer</span></span>

<span data-ttu-id="fb7ae-378">このエラーは、Visual Studio Online を使用してロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-378">This error only occurs when you run load tests by using Visual Studio Online.</span></span>

#### <a name="error-example"></a><span data-ttu-id="fb7ae-379">エラーの例</span><span class="sxs-lookup"><span data-stu-id="fb7ae-379">Error example</span></span>
```
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a><span data-ttu-id="fb7ae-380">ソリューション</span><span class="sxs-lookup"><span data-stu-id="fb7ae-380">Solution</span></span>

<span data-ttu-id="fb7ae-381">この問題を解決する修正プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-381">A hotfix is available that resolves this issue.</span></span> <span data-ttu-id="fb7ae-382">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="fb7ae-382">The Microsoft Knowledge Base (KB) number is 4095640.</span></span>

