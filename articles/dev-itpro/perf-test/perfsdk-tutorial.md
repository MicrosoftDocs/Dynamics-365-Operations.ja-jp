---
title: "パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト"
description: "このトピックでは、Performance SDK について説明し、Visual Studio Online を使用してマルチユーザー テストを行う方法を示します。"
author: jujoh
manager: AnnBe
ms.date: 03/19/2018
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c0a50f3d520754fc5991b5be7a583c7952cbbcdb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="performance-sdk-and-multiuser-testing-via-visual-studio-online"></a><span data-ttu-id="d1018-103">パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="d1018-103">Performance SDK and multiuser testing via Visual Studio Online</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d1018-104">このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) について説明し、Microsoft Visual Studio Online を使用してマルチユーザー テストを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1018-104">This topic describes the Performance software development kit (SDK) and shows how to do multiuser testing via Microsoft Visual Studio Online.</span></span> <span data-ttu-id="d1018-105">また、タスク レコーダーで記録したシナリオをシングルユーザー テスト、そしてマルチユーザー テストに変換する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="d1018-105">It also describes how to convert a scenario that you recorded in Task recorder to a single-user test and then a multiuser test.</span></span>

> [!NOTE]
> <span data-ttu-id="d1018-106">管理者として環境を利用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-106">You must have access the environment as an administrator.</span></span> <span data-ttu-id="d1018-107">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1018-107">For more information, see [Access instances](../dev-tools/access-instances.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1018-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="d1018-108">Prerequisites</span></span>

- <span data-ttu-id="d1018-109">Microsoft Visual Studio 2015 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d1018-109">Microsoft Visual Studio 2015 Enterprise</span></span>
- <span data-ttu-id="d1018-110">数量データを含むデプロイメント</span><span class="sxs-lookup"><span data-stu-id="d1018-110">A deployment that has volume data</span></span>
- <span data-ttu-id="d1018-111">パフォーマンス SDK (環境に応じてドライブ C またはF で **PerfSDK** という名前のフォルダーを探します)。</span><span class="sxs-lookup"><span data-stu-id="d1018-111">The Performance SDK (Look for a folder that is named **PerfSDK** on drive C or F, depending on your environment.)</span></span>

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a><span data-ttu-id="d1018-112">XML 記録からシングル ユーザー C# テストを作成する</span><span class="sxs-lookup"><span data-stu-id="d1018-112">Create a single-user C# test from an XML recording</span></span>

<span data-ttu-id="d1018-113">単一ユーザー テストを作成する方法を説明するビデオを表示するには、[[https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3)] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1018-113">To view a video that shows how to create a single-user test, go to [https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3).</span></span>

1. <span data-ttu-id="d1018-114">タスク レコーダーを使用して、テストするシナリオの記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1018-114">Use Task recorder to create a recording of the scenario that you want to test.</span></span>
2. <span data-ttu-id="d1018-115">Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d1018-115">Start Microsoft Visual Studio as administrator, and build the **PerfSDKSample** project.</span></span> <span data-ttu-id="d1018-116">このプロジェクトは **PerfSDK** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d1018-116">This project is in the **PerfSDK** folder.</span></span> <span data-ttu-id="d1018-117">プロジェクトを既に構築している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="d1018-117">If you've already built the project, skip this step.</span></span>
3. <span data-ttu-id="d1018-118">**Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-118">Select **Dynamics 365** &gt; **Addins** &gt; **Create C# perf test from recording**.</span></span>
4. <span data-ttu-id="d1018-119">**タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-119">In the **Import Task Recording** dialog box, enter the required details, and then select **Import**.</span></span>

    <span data-ttu-id="d1018-120">[![インポート タスク記録 ダイアログ ボックス](./media/perf103a.png)](./media/perf103a.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-120">[![Import Task Recording dialog box](./media/perf103a.png)](./media/perf103a.png)</span></span>

    <span data-ttu-id="d1018-121">C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-121">A C# test is generated in the Generated folder for the project that you selected.</span></span>

## <a name="run-a-single-user-performance-test-by-using-the-performance-sdk"></a><span data-ttu-id="d1018-122">パフォーマンス SDK を使用して単一ユーザー パフォーマンス テストを実行</span><span class="sxs-lookup"><span data-stu-id="d1018-122">Run a single-user performance test by using the Performance SDK</span></span>

1. <span data-ttu-id="d1018-123">Microsoft Windows のコントロール パネルで、**システムとセキュリティ** &gt; **システム** &gt; **システムの詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-123">In Control Panel in Microsoft Windows, select **System and Security** &gt; **System** &gt; **Advanced System Settings**.</span></span> <span data-ttu-id="d1018-124">**TestRoot**環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-124">Verify that the **TestRoot** environment variable is set to the path of the PerfSDK folder.</span></span>

    <span data-ttu-id="d1018-125">[![TestRoot 環境変数が PerfSDK フォルダに設定](./media/testroot.jpg)](./media/testroot.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-125">[![TestRoot environment variable set to the PerfSDK folder](./media/testroot.jpg)](./media/testroot.jpg)</span></span>

2. <span data-ttu-id="d1018-126">[http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="d1018-126">Download the **selenium-dotnet-strongnamed-2.42.0.zip** and **IEDriverServer\_Win32\_2.42.0.zip** files from [http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/).</span></span>
3. <span data-ttu-id="d1018-127">ファイルを抽出し、ダイナミック リンク ライブラリ (DLL) を **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d1018-127">Extract the files, and copy the dynamic-link libraries (DLLs) to the **PerfSDK\\Common\\External\\Selenium** folder.</span></span> <span data-ttu-id="d1018-128">プロジェクトに **WebDriver.dll** への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1018-128">Add a reference to **WebDriver.dll** to your project.</span></span>

    <span data-ttu-id="d1018-129">[![PerfSDK\Common\External\Selenium フォルダーにある DLL](./media/perf103d.png)](./media/perf103d.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-129">[![DLLs in the PerfSDK\Common\External\Selenium folder](./media/perf103d.png)](./media/perf103d.png)</span></span>

4. <span data-ttu-id="d1018-130">証明書を生成しインストールします。</span><span class="sxs-lookup"><span data-stu-id="d1018-130">Generate and install a certificate.</span></span> <span data-ttu-id="d1018-131">証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d1018-131">To generate a certificate file, open a Command Prompt window as an administrator, and run the following commands.</span></span>

    ```
    C:\Program Files (x86)\Windows Kits\8.1\bin\x64>makecert -n "CN=TestAuthCert" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.2 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    C:\Program Files (x86)\Windows Kits\8.1\bin\x64>pvk2pfx -pvk c:\temp\authcert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="d1018-132">これらのコマンドでは次の要素を注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1018-132">Note the following elements in these commands:</span></span>

   - <span data-ttu-id="d1018-133">**-n "CN=TestAuthCert"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="d1018-133">**-n "CN=TestAuthCert"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="d1018-134">自分のシナリオに合わせて名前を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="d1018-134">You can adjust the name to suit your scenario.</span></span>
   - <span data-ttu-id="d1018-135">**-eku 1.3.6.1.5.5.7.3.2** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-135">**-eku 1.3.6.1.5.5.7.3.2** gives the purpose of the certificate.</span></span> <span data-ttu-id="d1018-136">この証明書は、コード署名証明書、暗号化証明書、またはその他の種類の証明書ではなく、クライアント認証証明書です。</span><span class="sxs-lookup"><span data-stu-id="d1018-136">This certificate is a client authentication certificate instead of a code signing certificate, an encryption certificate, or some other type of certificate.</span></span>

     <span data-ttu-id="d1018-137">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-137">When you're prompted for a private key password, select **None**.</span></span>

     <span data-ttu-id="d1018-138">次のファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-138">You should see the following files:</span></span>

   - <span data-ttu-id="d1018-139">authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="d1018-139">authcert.pfx</span></span>
   - <span data-ttu-id="d1018-140">authcert.cer</span><span class="sxs-lookup"><span data-stu-id="d1018-140">authcert.cer</span></span> 
   - <span data-ttu-id="d1018-141">authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="d1018-141">authcert.pvk</span></span>

5. <span data-ttu-id="d1018-142">**\*.pfx** 証明書ファイルをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d1018-142">Install the **\*.pfx** certificate file.</span></span> <span data-ttu-id="d1018-143">それをインストールするときは、**ローカル コンピューター** をかならず選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-143">When you install it, make sure that you select **Local Machine**.</span></span> <span data-ttu-id="d1018-144">その後 **PerfSDK** フォルダーにファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d1018-144">Then copy the file to the **PerfSDK** folder.</span></span>
6. <span data-ttu-id="d1018-145">管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。</span><span class="sxs-lookup"><span data-stu-id="d1018-145">Open a Microsoft Windows PowerShell window as an administrator, and run the following commands to get the thumbprint of the installed certificate.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=TestAuthCert" }
    ```

    <span data-ttu-id="d1018-146">[![インストールされている証明書の拇印](./media/get-thumbprint.jpg)](./media/get-thumbprint.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-146">[![Thumbprint of the installed certificate](./media/get-thumbprint.jpg)](./media/get-thumbprint.jpg)</span></span>

7. <span data-ttu-id="d1018-147">**CloudEnvironment.Config** ファイルで、**SelfSigningCertificateThumbprint** キーの値として拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1018-147">In the **CloudEnvironment.Config** file, enter the thumbprint as the value for the **SelfSigningCertificateThumbprint** key.</span></span>

    <span data-ttu-id="d1018-148">[![更新された CloudEnvironment.Config ファイル](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-148">[![Updated CloudEnvironment.Config file](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)</span></span>

8. <span data-ttu-id="d1018-149">**wif.config** ファイルを更新して Application Object Server (AOS) が証明書を信頼できるようにするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d1018-149">Follow these steps to update the **wif.config** file so that Application Object Server (AOS) trusts the certificate:</span></span>

    1. <span data-ttu-id="d1018-150">Microsoft インターネット インフォメーション サービス (IIS) を起動し、サイトの一覧で **Microsoft Dynamics 365 for Finance and Operations** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="d1018-150">Start Microsoft Internet Information Services (IIS), and find **Microsoft Dynamics 365 for Finance and Operations** in the list of sites.</span></span>
    2. <span data-ttu-id="d1018-151">**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d1018-151">Select **Explore**, and find the **wif.config** file.</span></span>

        <span data-ttu-id="d1018-152">[![wif.config ファイル](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-152">[![wif.config file](./media/wifconfig.jpg)](./media/wifconfig.jpg)</span></span>

    3. <span data-ttu-id="d1018-153">証明書と権限名を入力して、このファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="d1018-153">Update this file by entering the certificate and authority name.</span></span>

        <span data-ttu-id="d1018-154">[![更新された wif.config ファイル](./media/wif-updated.jpg)](./media/wif-updated.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-154">[![Updated wif.config file](./media/wif-updated.jpg)](./media/wif-updated.jpg)</span></span>

    4. <span data-ttu-id="d1018-155">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="d1018-155">Restart IIS.</span></span>

9. <span data-ttu-id="d1018-156">Visual Studio で、**PerfSDKSample** プロジェクトを開き、**PurchaseReq.cs** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d1018-156">In Visual Studio, open the **PerfSDKSample** project, and find the **PurchaseReq.cs** file.</span></span> <span data-ttu-id="d1018-157">このファイルは、サンプル シングルユーザー テストです。</span><span class="sxs-lookup"><span data-stu-id="d1018-157">This file is a sample single-user test.</span></span> <span data-ttu-id="d1018-158">ファイルで、次の行をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="d1018-158">In the file, comment out the following lines.</span></span>

    ```
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    <span data-ttu-id="d1018-159">[![PurchaseReq.cs でコメント アウトされた行](./media/perf103e.png)](./media/perf103e.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-159">[![Lines commented out in PurchaseReq.cs](./media/perf103e.png)](./media/perf103e.png)</span></span>

10. <span data-ttu-id="d1018-160">管理者のユーザー名を入力することによって **CloudEnvironment.Config** ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="d1018-160">Modify the **CloudEnvironment.Config** file by entering your admin user name.</span></span> <span data-ttu-id="d1018-161">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-161">Here is an example.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1018-162">**ConfigName** は **DEVFABRIC** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-162">**ConfigName** must be set to **DEVFABRIC**.</span></span> 

    <span data-ttu-id="d1018-163">[![更新された CloudEnvironment.Config ファイル](./media/perf103f.png)](./media/perf103f.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-163">[![Updated CloudEnvironment.Config file](./media/perf103f.png)](./media/perf103f.png)</span></span> 

11. <span data-ttu-id="d1018-164">**CloudEnvironment.Config** ファイルに、エンドポイントを入力します。</span><span class="sxs-lookup"><span data-stu-id="d1018-164">In the **CloudEnvironment.Config** file, enter your endpoint.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1018-165">環境をアプリケーション リクエスト ルーティング (ARR) に対して有効にするには、2 つのエンドポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="d1018-165">If the environment is enabled for Application Request Routing (ARR), you have two endpoints.</span></span> <span data-ttu-id="d1018-166">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-166">Here is an example:</span></span>
    >
    > - <span data-ttu-id="d1018-167">apr-arr8aos**soap**.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="d1018-167">apr-arr8aos**soap**.axcloud.test.dynamics.com</span></span>
    > - <span data-ttu-id="d1018-168">apr-arr8aos.axcloud.test.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="d1018-168">apr-arr8aos.axcloud.test.dynamics.com</span></span>
    >
    > <span data-ttu-id="d1018-169">この場合、CloudEnvironment.Config ファイルに両方のエンドポイントを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-169">In this case, you must enter both endpoints in the CloudEnvironment.Config file.</span></span>
    >
    > <span data-ttu-id="d1018-170">[![CloudEnvironment.Config のエンドポイント](./media/perf103upd.png)](./media/perf103upd.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-170">[![Endpoints in CloudEnvironment.Config](./media/perf103upd.png)](./media/perf103upd.png)</span></span>

12. <span data-ttu-id="d1018-171">**テスト** &gt; **テストの設定** を選択し、**既定のプロセッサ アーキテクチャ** を **x64** に設定してソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d1018-171">Select **Test** &gt; **Test settings**, set **Default processor architecture** to **x64**, and then build the solution.</span></span>
13. <span data-ttu-id="d1018-172">**テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-172">Select **Test** &gt; **Windows** &gt; **Test Explorer** to view the list of tests.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1018-173">場合によっては、Visual Studio でテストの一覧が更新されません。</span><span class="sxs-lookup"><span data-stu-id="d1018-173">Sometimes, Visual Studio might not update the list of tests.</span></span> <span data-ttu-id="d1018-174">この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="d1018-174">In this case, restart Visual Studio, and then reopen Test Explorer.</span></span>

    <span data-ttu-id="d1018-175">新しいテストに **TestMethod** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="d1018-175">Your new test will be named **TestMethod**.</span></span> <span data-ttu-id="d1018-176">**TestMethod** のメソッド名を変更すると、個々の名前がテストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-176">If you change the method name of **TestMethod**, your test will receive an individual name.</span></span> 

<span data-ttu-id="d1018-177">テストを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1018-177">You can now run the test.</span></span> <span data-ttu-id="d1018-178">テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。</span><span class="sxs-lookup"><span data-stu-id="d1018-178">When you run the test, Internet Explorer should be started, and it should replay the scenario that you recorded.</span></span>

## <a name="create-a-multiuser-test-from-a-single-user-test"></a><span data-ttu-id="d1018-179">シングル ユーザー テストからマルチ ユーザー テストを作成する</span><span class="sxs-lookup"><span data-stu-id="d1018-179">Create a multiuser test from a single-user test</span></span>

<span data-ttu-id="d1018-180">以前のセクションで情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="d1018-180">After you create a single-user test by using the information in the previous section, you can convert it to a multiuser test.</span></span> <span data-ttu-id="d1018-181">テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="d1018-181">Add **MS.Dynamics.TestTools.UIHelpers.Core;** to your test script, and find the following line in the **TestSetup** method.</span></span>

```
Client = DispatchedClient.DefaultInstance;
```

<span data-ttu-id="d1018-182">その行を以下の行に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d1018-182">Replace that line with the following lines.</span></span>

```
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

<span data-ttu-id="d1018-183">タスク記録が行われたときに入力した値がランダム化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-183">Make sure that the values that you entered when you made the task recording are randomized.</span></span> <span data-ttu-id="d1018-184">テスト データを生成するために、データ拡張ツールを最初に使用することが必要な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-184">You might have to use the Data Expansion Tool first to generate test data.</span></span>

## <a name="set-up-visual-studio-online-for-multiuser-testing"></a><span data-ttu-id="d1018-185">Visual Studio Online でマルチ ユーザー テストを設定</span><span class="sxs-lookup"><span data-stu-id="d1018-185">Set up Visual Studio Online for multiuser testing</span></span>

<span data-ttu-id="d1018-186">この例では、ユーザーは ProcureToPay.cs ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1018-186">For this example, you will use the ProcureToPay.cs file.</span></span> <span data-ttu-id="d1018-187">Visual Studio を開始するにサインインする必要があります、[[Visual Studio Online ポータル](https://app.vssps.visualstudio.com/profile/view)] にサインインし、**Visual Studioで開く** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-187">To start Visual Studio, you must sign in to the [Visual Studio Online portal](https://app.vssps.visualstudio.com/profile/view), and then select **Open in Visual Studio**.</span></span>

> [!NOTE]
> <span data-ttu-id="d1018-188">このステップは 1 回のみ完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-188">You must complete this step only one time.</span></span> <span data-ttu-id="d1018-189">Visual Studio Online にサインインした後、設定が保存されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-189">After you've signed in to Visual Studio Online, the settings are saved.</span></span>

<span data-ttu-id="d1018-190">[![Visual Studio で開きます](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-190">[![Open in Visual Studio](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)</span></span>

1. <span data-ttu-id="d1018-191">**PerfSDKSample** プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1018-191">Open the **PerfSDKSample** project.</span></span>
2. <span data-ttu-id="d1018-192"><strong>CloudEnvironment.Config</strong> ファイルで、<strong>UserFormat</strong> エントリを更新して、管理者ユーザー URL を反映します。</span><span class="sxs-lookup"><span data-stu-id="d1018-192">In the <strong>CloudEnvironment.Config</strong> file, update the <strong>UserFormat</strong> entry so that it reflects the admin user URL.</span></span> <span data-ttu-id="d1018-193">たとえば、`admin@example.com` に対して、ユーザー形式として <strong>TST\_{0}@example.com</strong> を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1018-193">For example, for `admin@example.com`, use <strong>TST\_{0}@example.com</strong> as the user format.</span></span> <span data-ttu-id="d1018-194">また、<strong>UserCount</strong> 値をパフォーマンス テストに含めるユーザーの数に変更します。</span><span class="sxs-lookup"><span data-stu-id="d1018-194">Additionally, change the <strong>UserCount</strong> value to the number of users that you want to have in your performance test.</span></span>

    <span data-ttu-id="d1018-195">[![更新された CloudEnvironment.Config ファイル](./media/vsonline-12.jpg)](./media/vsonline-12.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-195">[![Updated CloudEnvironment.Config file](./media/vsonline-12.jpg)](./media/vsonline-12.jpg)</span></span>

3. <span data-ttu-id="d1018-196">**PerfSDK** フォルダーで、次のコマンドを実行して環境のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1018-196">In the **PerfSDK** folder, run the following command to create test users for your environment.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe
    ```

    <span data-ttu-id="d1018-197">必要な数のユーザーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d1018-197">You can create as many users as you want.</span></span> <span data-ttu-id="d1018-198">たとえば、次のコマンドは、USMF 会社で 150 人のテスト ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1018-198">For example, the following command creates 150 test users for the USMF company.</span></span>

    ```
    MS.Dynamics.Performance.CreateUsers.exe 150 USMF
    ```

4. <span data-ttu-id="d1018-199">管理者ユーザーとしてエンドポイントにログインし、ユーザーがシステムで作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-199">Sign in to your endpoint as the admin user, and verify that users were created in the system.</span></span>

### <a name="test-the-sandbox-environment"></a><span data-ttu-id="d1018-200">サンドボックス環境をテスト</span><span class="sxs-lookup"><span data-stu-id="d1018-200">Test the sandbox environment</span></span>

<span data-ttu-id="d1018-201">ここまでは、これらの手順で、AOS マシンも開発マシンである開発者トポロジを使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="d1018-201">Up to this point, these instructions have made the assumption that you have a developer topology in which the AOS machine is also your development machine.</span></span>  <span data-ttu-id="d1018-202">Visual Studio Online で負荷テストを実行するためには、サンドボックス環境をテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-202">In order to run load tests on Visual Studio Online, you must be testing a sandbox environment.</span></span>  <span data-ttu-id="d1018-203">サンドボックスと負荷テストを実行しているコンピューターとの間の信頼関係を確立するために、完了する必要がある追加ステップがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="d1018-203">There are a few additional steps that must be completed to establish trust between the sanbox and the computer running the load tests.</span></span>  <span data-ttu-id="d1018-204">負荷テストを実行しているコンピューターは、開発マシンでも、Visual Studio Online で作成したテスト エージェントでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="d1018-204">The computer running the load tests may be either your development machine or the test agent created by Visual Studio Online.</span></span>

1. <span data-ttu-id="d1018-205">サンドボックス AOS マシンへのリモート デスクトップ の接続を確立し、**.cer** ファイルを上書きします。</span><span class="sxs-lookup"><span data-stu-id="d1018-205">Establish a Remote Desktop connection to your sandbox AOS machine, and copy over the **.cer** file.</span></span> <span data-ttu-id="d1018-206">ファイルをダブルクリックして、インストールします。</span><span class="sxs-lookup"><span data-stu-id="d1018-206">Double-click the file to install it.</span></span> <span data-ttu-id="d1018-207">証明書ストアの入力を要求するメッセージが表示されたら、**個人** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-207">When you're prompted for the certificate store, select **Personal**.</span></span>
2. <span data-ttu-id="d1018-208">IIS を起動し、サイトの一覧で **AOSService** を見つけます。</span><span class="sxs-lookup"><span data-stu-id="d1018-208">Start IIS, and find **AOSService** in the list of sites.</span></span> <span data-ttu-id="d1018-209">その後、**エクスプローラー** を選択して、**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="d1018-209">Then select **Explore**, and find the **wif.config** file.</span></span> <span data-ttu-id="d1018-210">証明書と権限名を入力して、このファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="d1018-210">Update this file by entering the certificate and authority name.</span></span> <span data-ttu-id="d1018-211">(以前に生成した証明書の値を使用します。)</span><span class="sxs-lookup"><span data-stu-id="d1018-211">(Use the values from the certificate that you generated earlier.)</span></span>

    <span data-ttu-id="d1018-212">[![更新された wif.config ファイル](./media/wif-updated.jpg)](./media/wif-updated.jpg)</span><span class="sxs-lookup"><span data-stu-id="d1018-212">[![Updated wif.config file](./media/wif-updated.jpg)](./media/wif-updated.jpg)</span></span>

3. <span data-ttu-id="d1018-213">IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="d1018-213">Restart IIS.</span></span>

<span data-ttu-id="d1018-214">トポロジに対してパフォーマンス テストを実行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d1018-214">You can now run performance tests against the topology.</span></span>

> [!NOTE]
> <span data-ttu-id="d1018-215">トポロジに複数の AOS マシンがある場合、証明書をインストールして、それぞれの wif.config ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-215">If your topology has multiple AOS machines, you must install the certificate and update the wif.config file on each of them.</span></span>

## <a name="run-the-performance-test"></a><span data-ttu-id="d1018-216">パフォーマンス テストの実行</span><span class="sxs-lookup"><span data-stu-id="d1018-216">Run the performance test</span></span>

1. <span data-ttu-id="d1018-217">Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d1018-217">In the Visual Studio editor, open the **ProcureToPay.cs** file, and append the following lines in the **TestSetup** method.</span></span>

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```
2. <span data-ttu-id="d1018-218">次のインストーラー ファイルは、PerfSDK ディレクトリにある **Visual Studio Online** フォルダーにダウンロードして配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-218">The following installer files must be downloaded and placed in the **Visual Studio Online** folder located within the PerfSDK directory:</span></span>
    - <span data-ttu-id="d1018-219">Visual Studio 2015 用 Visual C++ 再頒布可能パッケージ: https://www.microsoft.com/en-us/download/details.aspx?id=48145</span><span class="sxs-lookup"><span data-stu-id="d1018-219">Visual C++ redistributable for Visual Studio 2015: https://www.microsoft.com/en-us/download/details.aspx?id=48145</span></span>
    - <span data-ttu-id="d1018-220">SQL Server の Microsoft ODBC ドライバー 13 (64 ビット バージョン msi を選択): https://www.microsoft.com/en-us/download/details.aspx?id=50420</span><span class="sxs-lookup"><span data-stu-id="d1018-220">Microsoft ODBC Driver 13 for SQL Server (pick the 64 bit version msi): https://www.microsoft.com/en-us/download/details.aspx?id=50420</span></span>

3. <span data-ttu-id="d1018-221">**setup.cmd** のコンテンツにある、**Visual Studio Online** フォルダーを変更し、次と一致させます:</span><span class="sxs-lookup"><span data-stu-id="d1018-221">Change the contents of **setup.cmd** located in the **Visual Studio Online** folder to match the following:</span></span>

        setx testroot "%DeploymentDirectory%"
        ECHO Installing D365 prerequisites
        ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
        MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
        ECHO %DeploymentDirectory%\vc_redist.x64.exe /install /passive /norestart
        %DeploymentDirectory%\vc_redist.x64.exe /install /passive /norestart
        %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
        Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
        %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    
4. <span data-ttu-id="d1018-222">**CloudCtuFakeACSInstall.cmd** の内容を変更して、**インポート** コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。</span><span class="sxs-lookup"><span data-stu-id="d1018-222">Modify the contents of **CloudCtuFakeACSInstall.cmd** so that the **Import** command has an empty string instead of **'password'**.</span></span>  <span data-ttu-id="d1018-223">スクリプトの 3 行目は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d1018-223">The third line of the script should look like this:</span></span>

    <span data-ttu-id="d1018-224">set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....</span><span class="sxs-lookup"><span data-stu-id="d1018-224">set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....</span></span>

5. <span data-ttu-id="d1018-225">ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1018-225">In your solution files, double-click the **vsonline.testsettings** file to modify the test settings.</span></span>
6. <span data-ttu-id="d1018-226">**テストの設定**ダイアログ ボックスの**配置**タブで、次の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1018-226">In the **Test Settings** dialog box, on the **Deployment** tab, use the following settings:</span></span>

   - <span data-ttu-id="d1018-227">**展開の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="d1018-227">Select the **Enable deployment** check box.</span></span>
   - <span data-ttu-id="d1018-228">**配置する追加のファイルやディレクトリ** フィールドで、以下のファイルが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-228">In the **Additional files and directories to deploy** field, make sure that the following files are listed:</span></span>

     - <span data-ttu-id="d1018-229">&lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\</span><span class="sxs-lookup"><span data-stu-id="d1018-229">&lt;Solution Directory&gt;\\PerfSDKSample\\bin\\Debug\\</span></span>
     - <span data-ttu-id="d1018-230">C:\\PerfSDK\\CloudEnvironment.Config</span><span class="sxs-lookup"><span data-stu-id="d1018-230">C:\\PerfSDK\\CloudEnvironment.Config</span></span>
     - <span data-ttu-id="d1018-231">C:\\PerfSDK\\authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="d1018-231">C:\\PerfSDK\\authcert.pfx</span></span>
     - <span data-ttu-id="d1018-232">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span><span class="sxs-lookup"><span data-stu-id="d1018-232">C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config</span></span>
     - <span data-ttu-id="d1018-233">C:\\PerfSDK\\Visual Studio Online\\</span><span class="sxs-lookup"><span data-stu-id="d1018-233">C:\\PerfSDK\\Visual Studio Online\\</span></span>

       > [!NOTE]
       > <span data-ttu-id="d1018-234">PerfSDK フォルダーが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-234">Your PerfSDK folder might differ.</span></span>
        
7. <span data-ttu-id="d1018-235">**テストの設定**ダイアログ ボックスの**スクリプトの設定とクリーンアップ** タブで、PerfSDK ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-235">In the **Test Settings** dialog box, on the **Setup and Cleanup Scripts** tab, select **setup.cmd**, located in the **Visual Studio Online** folder within your PerfSDK directory.</span></span>

8. <span data-ttu-id="d1018-236">**テストの設定**ダイアログ ボックスの**追加設定**タブで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-236">In the **Test Settings** dialog box, on the **Additional Settings** tab, select **Run tests in 64 bit process on 64 bit machine**.</span></span>

9. <span data-ttu-id="d1018-237">テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1018-237">To run the test, open the **SampleLoadTest.loadtest** file, and select **Run Load Test**.</span></span>

    <span data-ttu-id="d1018-238">[![負荷テストの実行](./media/perf103u.png)](./media/perf103u.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-238">[![Run Load Test](./media/perf103u.png)](./media/perf103u.png)</span></span>

    <span data-ttu-id="d1018-239">テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-239">When the test has finished running, you should see a summary that shows transaction results.</span></span> <span data-ttu-id="d1018-240">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-240">Here is an example.</span></span>

    <span data-ttu-id="d1018-241">[![トランザクションの結果](./media/perf103v.png)](./media/perf103v.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-241">[![Transaction results](./media/perf103v.png)](./media/perf103v.png)</span></span>

10. <span data-ttu-id="d1018-242">テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="d1018-242">To view various indicators for the test controller and test scenario, you can switch to the **Graphs** view.</span></span>

     <span data-ttu-id="d1018-243">[![グラフ 表示](./media/perf103w.png)](./media/perf103w.png)</span><span class="sxs-lookup"><span data-stu-id="d1018-243">[![Graphs view](./media/perf103w.png)](./media/perf103w.png)</span></span>

     > [!NOTE]
     > <span data-ttu-id="d1018-244">テストの実行中、システムに関する情報はこのビューで利用することができません。</span><span class="sxs-lookup"><span data-stu-id="d1018-244">While tests are being run, information about your system isn't available in this view.</span></span> <span data-ttu-id="d1018-245">この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-245">To access this information, you must use Microsoft Dynamics Lifecycle Services (LCS) to monitor the CPU and memory usage of your AOS machine.</span></span> <span data-ttu-id="d1018-246">または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。</span><span class="sxs-lookup"><span data-stu-id="d1018-246">Alternatively, you can set up perfmon directly on the AOS machine and set up the Microsoft Azure portal to monitor Microsoft SQL Server usage of Database Transaction Units (DTUs).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d1018-247">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d1018-247">Troubleshooting</span></span>

### <a name="zoom-factor"></a><span data-ttu-id="d1018-248">ズーム係数</span><span class="sxs-lookup"><span data-stu-id="d1018-248">Zoom factor</span></span>

<span data-ttu-id="d1018-249">この問題はシングルユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="d1018-249">This issue only impacts single-user tests.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="d1018-250">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-250">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```
#### <a name="solution"></a><span data-ttu-id="d1018-251">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-251">Solution</span></span>

<span data-ttu-id="d1018-252">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="d1018-252">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="d1018-253">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="d1018-253">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="d1018-254">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="d1018-254">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="d1018-255">コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="d1018-255">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>
 
<span data-ttu-id="d1018-256">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-256">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="d1018-257">このフィールドは、Microsoft Windows の**表示設定**で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1018-257">This field is available in **Display settings** in Microsoft Windows.</span></span> 
 
<span data-ttu-id="d1018-258">これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="d1018-258">If those steps don't work, try to change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

### <a name="certificate-thumbprint-errors"></a><span data-ttu-id="d1018-259">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="d1018-259">Certificate thumbprint errors</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-260">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-260">Error example</span></span>

```
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a><span data-ttu-id="d1018-261">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-261">Solution</span></span>

<span data-ttu-id="d1018-262">次のいくつかの理由でエラー メッセージを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-262">You might receive the error message for several reasons:</span></span>

- <span data-ttu-id="d1018-263">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1018-263">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="d1018-264">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-264">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="d1018-265">たとえば、次の Unicode コンバーターを使用する場合があります: https://r12a.github.io/apps/conversion/</span><span class="sxs-lookup"><span data-stu-id="d1018-265">For example, you may use the following unicode converter: https://r12a.github.io/apps/conversion/</span></span>

    ![Unicode コードの変換](./media/sdk_unicode_code_converter.jpg)
 
- <span data-ttu-id="d1018-267">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="d1018-267">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="d1018-268">AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d1018-268">To verify that the certificate can be found on the AOS machine, run the following Windows PowerShell script.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    <span data-ttu-id="d1018-269">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。</span><span class="sxs-lookup"><span data-stu-id="d1018-269">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate can't be found.</span></span> <span data-ttu-id="d1018-270">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="d1018-270">To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</span></span>
 
- <span data-ttu-id="d1018-271">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-271">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="d1018-272">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-272">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>
 
    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード](./media/set_cloudctufakeacsinstall.jpg)
 
### <a name="no-endpoint-is-listening"></a><span data-ttu-id="d1018-274">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="d1018-274">No endpoint is listening</span></span>

<span data-ttu-id="d1018-275">この問題は、シングルユーザーまたはマルチユーザーのテストを実行する場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-275">This issue can occur when you run single-user or multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-276">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-276">Error example</span></span>

<span data-ttu-id="d1018-277">テストまたはユーザー作成プロセスが失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1018-277">The tests or user creation process fails, and the following error message is shown.</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a><span data-ttu-id="d1018-278">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-278">Solution</span></span>

<span data-ttu-id="d1018-279">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-279">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>
 
<span data-ttu-id="d1018-280">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-280">In the CloudEnvironment.Config file, review the values that are specified by the following keys.</span></span>

- <span data-ttu-id="d1018-281">&lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="d1018-281">&lt;ExecutionConfigurations Key="HostName" Value="&lt;web address of host&gt;" /&gt;</span></span>
- <span data-ttu-id="d1018-282">&lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;</span><span class="sxs-lookup"><span data-stu-id="d1018-282">&lt;ExecutionConfigurations Key="SoapHostName" Value="&lt;web address of SOAP&gt;" /&gt;</span></span>

<span data-ttu-id="d1018-283">これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-283">The web addresses that are specified by these keys must be the environment that you're testing.</span></span> <span data-ttu-id="d1018-284">開発者マシンから Web ブラウザーの **HostName** キーによって指定された Web アドレスを開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-284">Make sure that you can open the web address specified by the **HostName** key in a web browser from your developer machine.</span></span>

<span data-ttu-id="d1018-285">オンライン ロード テストについては、CloudEnvironment.Config ファイルの **HostName** フィールドで指定されている環境は、任意のマシンから公共的にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-285">For online load tests, the environment that is specified by the **HostName** field in the CloudEnvironment.Config file must be publicly accessible from any machine.</span></span> <span data-ttu-id="d1018-286">したがって、ワンボックス環境の外部でエンドポイントにアクセスできないため、Visual Studio Online を使用して負荷テストを実行し、ワンボックス環境をテストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d1018-286">Therefore, you won't be able to run the load test using Visual Studio Online to test a one-box environment since the endpoint won't be accessible outside of the one-box environment.</span></span>

### <a name="users-cant-be-enumerated"></a><span data-ttu-id="d1018-287">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="d1018-287">Users can't be enumerated</span></span>

<span data-ttu-id="d1018-288">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-288">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-289">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-289">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a><span data-ttu-id="d1018-290">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-290">Solution</span></span>

<span data-ttu-id="d1018-291">このエラーを引き起こす可能性のあるシナリオは 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="d1018-291">There are two scenarios that can cause this error:</span></span>
- <span data-ttu-id="d1018-292">**SelfMintingAdminUser** として指定されたユーザーは、システム管理者ロールのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-292">The user who is specified as **SelfMintingAdminUser** must be a member of the System Administrator role.</span></span> <span data-ttu-id="d1018-293">この問題は、**SelfMintingAdminUser** がシステム管理者の役割が割り当てられていないユーザーである場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-293">This issue occurs when the **SelfMintingAdminUser** is a user that is not assigned the System Administrator role.</span></span> <span data-ttu-id="d1018-294">適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d1018-294">To verify that you've specified the correct user, you can sign in to the endpoint and view the user's roles.</span></span>

![管理者ユーザー](./media/sdk_admin.png)

- <span data-ttu-id="d1018-296"><strong>SelfMintingAdminUser</strong> として指定されたユーザーは、「<https://sts.windows-ppe.net/>」または「<https://sts.windows.net/>」以外のプロバイダーを持ちます。</span><span class="sxs-lookup"><span data-stu-id="d1018-296">The user who is specified as <strong>SelfMintingAdminUser</strong> has a provider other than "<https://sts.windows-ppe.net/>" or "<https://sts.windows.net/>".</span></span> <span data-ttu-id="d1018-297">場合によっては、管理者ユーザーはプロバイダ フィールドに会社固有のドメインを含めます。</span><span class="sxs-lookup"><span data-stu-id="d1018-297">Sometimes the admin user will have a company specific domain included in the provider field.</span></span> <span data-ttu-id="d1018-298">この問題を回避するには、任意の名前と電子メールで AX ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1018-298">To work around this issue, create a user in AX with any name and email.</span></span> <span data-ttu-id="d1018-299">この新しいユーザーをシステム管理者ロールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d1018-299">Assign this new user the System Administrator role.</span></span>  <span data-ttu-id="d1018-300">このユーザーを実在の Azure Active Directory ユーザーにリンクする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d1018-300">You do not need to link this user to a real Azure Active Directory user.</span></span> <span data-ttu-id="d1018-301">CloudEnvironment.config で、この新しい管理者ユーザーを <strong>SelfMintingAdminUser</strong> として指定します。</span><span class="sxs-lookup"><span data-stu-id="d1018-301">Specify this new admin user as the <strong>SelfMintingAdminUser</strong> in the CloudEnvironment.config</span></span>

### <a name="request-was-forbidden-with-client-authentication-scheme-anonymous"></a><span data-ttu-id="d1018-302">クライアント認証方式 "Anonymous" によって要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="d1018-302">Request was forbidden with client authentication scheme 'Anonymous'</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-303">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-303">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'. ---> System.Net.WebException: The remote server returned an error: (403) Forbidden..
```

#### <a name="solution"></a><span data-ttu-id="d1018-304">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-304">Solution</span></span>

<span data-ttu-id="d1018-305">この問題は、CloudEnvironment.Config ファイルの **UserCount** フィールドで指定したユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えた場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-305">This issue can occur when the number of users that you specify in the **UserCount** field in the CloudEnvironment.Config file exceeds the number of test users that you created by running MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="d1018-306">CloudEnvironment.Config ファイルで要求する数を超えるテスト ユーザーを作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-306">Make sure that you created more test users than you request in the CloudEnvironment.Config file.</span></span>
 
![クラウド環境のコンフィギュレーション](./media/cloud-env-config.png)

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="d1018-308">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="d1018-308">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="d1018-309">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-309">This issue can occur when you run multiuser tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="d1018-310">AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-310">It tends to occur when the AOS machine differs from the developer machine.</span></span> 

#### <a name="error-example"></a><span data-ttu-id="d1018-311">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-311">Error example</span></span>

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a><span data-ttu-id="d1018-312">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-312">Solution</span></span>

<span data-ttu-id="d1018-313">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-313">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="d1018-314">2 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="d1018-314">There are two possible causes:</span></span>

- <span data-ttu-id="d1018-315">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="d1018-315">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="d1018-316">問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。</span><span class="sxs-lookup"><span data-stu-id="d1018-316">To fix the issue, copy and install the .cer file that you created earlier in this topic to the AOS machine.</span></span>
- <span data-ttu-id="d1018-317">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="d1018-317">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="d1018-318">問題を解決するには、wif.config ファイルに証明書を追加する方法の詳細について、[Performance SDK を使用してシングル ユーザーのパフォーマン ステストを実行する] の手順 8 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1018-318">To fix the issue, see step 8 of the "Run a single-user performance test by using the Performance SDK" section for details on how to add the certificate to the wif.config file.</span></span> <span data-ttu-id="d1018-319">wif.config ファイルを変更した後は、必ず IIS を再起動してください。</span><span class="sxs-lookup"><span data-stu-id="d1018-319">Be sure to restart IIS after you modify the wif.config file.</span></span>
 
### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="d1018-320">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="d1018-320">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="d1018-321">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-321">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-322">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-322">Error example</span></span>

```
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a><span data-ttu-id="d1018-323">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-323">Solution</span></span>

<span data-ttu-id="d1018-324">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-324">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="d1018-325">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-325">Verify whether the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span> 

<span data-ttu-id="d1018-326">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="d1018-326">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="d1018-327">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="d1018-327">If the file is missing, add it to the deployment items in the test settings.</span></span>
 
<span data-ttu-id="d1018-328">非常に似た名前を持つ 2 つのファイルがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1018-328">Note that there are two files that have very similar names.</span></span> <span data-ttu-id="d1018-329">1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1018-329">The name of one file ends in **\*.dll**, and the name of the other file ends in **\*.dll.config**. The **\*.dll.config** file must be in the deployment items in the test settings.</span></span>
 
### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="d1018-330">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="d1018-330">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="d1018-331">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-331">This issue usually occurs only when you run load tests.</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-332">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-332">Error example</span></span>

```
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a><span data-ttu-id="d1018-333">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-333">Solution</span></span>

<span data-ttu-id="d1018-334">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-334">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="d1018-335">この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-335">The issue typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="d1018-336">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d1018-336">Verify whether the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="d1018-337">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span><span class="sxs-lookup"><span data-stu-id="d1018-337">&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out</span></span>

<span data-ttu-id="d1018-338">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="d1018-338">If the file is missing, add it to the deployment items in the test settings.</span></span>

![テスト設定](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a><span data-ttu-id="d1018-340">InteractiveClientID は設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="d1018-340">InteractiveClientID wasn't specified in the settings</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-341">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-341">Error example</span></span>

```
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a><span data-ttu-id="d1018-342">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-342">Solution</span></span>

<span data-ttu-id="d1018-343">この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-343">This issue occurs when the **SelfSigningCertificateThumbprint** field is left blank in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="d1018-344">CloudEnvironment.Config ファイルで、作成してインストールした証明書の拇印を次の行に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d1018-344">In the CloudEnvironment.Config file, paste the thumbprint of the certificate that you created and installed in the following line.</span></span>

```
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="d1018-345">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="d1018-345">The remote host forcibly closed an existing connection</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-346">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-346">Error example</span></span>

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

#### <a name="solution"></a><span data-ttu-id="d1018-347">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-347">Solution</span></span>

<span data-ttu-id="d1018-348">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d1018-348">Run the following Windows PowerShell script on the development machine.</span></span>

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="d1018-349">コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="d1018-349">Service w3svc was not found on computer</span></span>

<span data-ttu-id="d1018-350">このエラーは、Visual Studio Online を使用してロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="d1018-350">This error only occurs when running load tests using Visual Studio Online.</span></span>

#### <a name="error-example"></a><span data-ttu-id="d1018-351">エラーの例</span><span class="sxs-lookup"><span data-stu-id="d1018-351">Error example</span></span>
```
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a><span data-ttu-id="d1018-352">ソリューション</span><span class="sxs-lookup"><span data-stu-id="d1018-352">Solution</span></span>

<span data-ttu-id="d1018-353">この問題を解決する修正プログラムがあります。</span><span class="sxs-lookup"><span data-stu-id="d1018-353">There is a hotfix available which resolves this issue.</span></span> <span data-ttu-id="d1018-354">KB 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="d1018-354">The KB number is 4095640.</span></span>

