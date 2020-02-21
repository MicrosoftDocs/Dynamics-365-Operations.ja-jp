---
title: パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト
description: このトピックでは、タスク レコーダーから生成されたパフォーマンス テスト スクリプトと共に Microsoft Visual Studio とパフォーマンス SDK を使用してマルチユーザー テストを行う方法を説明します。
author: hasaid
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3819ffbc8fabeeb76bfac5011df2a0bc9b84b3
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029390"
---
# <a name="multi-user-testing-with-the-performance-sdk-and-a-local-test-controller"></a><span data-ttu-id="1e559-103">パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト</span><span class="sxs-lookup"><span data-stu-id="1e559-103">Multi-user testing with the Performance SDK and a local test controller</span></span>

[!include [banner](../includes/banner.md)]

 > [!IMPORTANT]
  > <span data-ttu-id="1e559-104">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</span><span class="sxs-lookup"><span data-stu-id="1e559-104">Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</span></span> <span data-ttu-id="1e559-105">将来的に、代替ソリューションの推奨を公開します。</span><span class="sxs-lookup"><span data-stu-id="1e559-105">In the future, we will publish some recommendations for alternative solutions.</span></span>  
  > - <span data-ttu-id="1e559-106">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="1e559-106">If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="1e559-107">そのサポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="1e559-107">You can continue using it until the end of the support cycle.</span></span> 
  > - <span data-ttu-id="1e559-108">クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="1e559-108">If you are using the cloud-based load testing service, it will continue to run through March 31, 2020.</span></span> <span data-ttu-id="1e559-109">それまでの間は、同サービスの全機能を継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="1e559-109">Until then, you can continue to use all of the experiences powered by this service without interruption.</span></span> <span data-ttu-id="1e559-110">また、オンプレミス負荷テストに切り替えることがも可能です。</span><span class="sxs-lookup"><span data-stu-id="1e559-110">Alternatively, you can switch to on-premises load testing.</span></span> <span data-ttu-id="1e559-111">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="1e559-111">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e559-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="1e559-112">Prerequisites</span></span>

<span data-ttu-id="1e559-113">このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:</span><span class="sxs-lookup"><span data-stu-id="1e559-113">Before you complete the steps in this topic, verify that the following prerequisites are met:</span></span>

- <span data-ttu-id="1e559-114">自身の Microsoft Azure サブスクリプションに、プラットフォーム更新プログラム 21 以降の開発環境があります。</span><span class="sxs-lookup"><span data-stu-id="1e559-114">You have a development environment that has Platform update 21 or later in own your Microsoft Azure subscription.</span></span>
- <span data-ttu-id="1e559-115">開発環境に Microsoft Visual Studio 2015 Enterprise edition がある</span><span class="sxs-lookup"><span data-stu-id="1e559-115">You have Microsoft Visual Studio 2015 Enterprise edition in a development environment.</span></span>
- <span data-ttu-id="1e559-116">開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。</span><span class="sxs-lookup"><span data-stu-id="1e559-116">You have a tier-2 or above sandbox environment that has the same release (application version and platform update) as your development environment.</span></span>
- <span data-ttu-id="1e559-117">[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従って開発環境を構成しました。</span><span class="sxs-lookup"><span data-stu-id="1e559-117">You've configured your development environment by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>
- <span data-ttu-id="1e559-118">エンド ツー エンド (E2E) シナリオ用に C\# パフォーマンス テスト クラスが生成され、[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従ってシングルユーザー テストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="1e559-118">C\# performance testing classes have been generated for your end-to-end (E2E) scenarios, and you can run a single-user test by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>

## <a name="configure-a-development-environment-for-multi-user-testing"></a><span data-ttu-id="1e559-119">マルチ ユーザー テストのための開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1e559-119">Configure a development environment for multi-user testing</span></span>

1. <span data-ttu-id="1e559-120">[SQL Server の ODBC ドライバー 17](https://download.microsoft.com/download/E/6/B/E6BFDC7A-5BCD-4C51-9912-635646DA801E/en-US/msodbcsql_17.2.0.1_x64.msi) をダウンロードして、ダウンロードしたファイルを **msodbcsql** に名前を変更して、それを **PerfSDK** フォルダーの **Visual Studio Online** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1e559-120">Download [ODBC Driver 17 for SQL Server](https://download.microsoft.com/download/E/6/B/E6BFDC7A-5BCD-4C51-9912-635646DA801E/en-US/msodbcsql_17.2.0.1_x64.msi), rename the download file **msodbcsql**, and copy it to the **Visual Studio Online** folder under the **PerfSDK** folder.</span></span>

    <span data-ttu-id="1e559-121">[![Visual Studio Online フォルダーの msodbcsql ファイル](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-121">[![msodbcsql file in Visual Studio Online folder](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</span></span>

2. <span data-ttu-id="1e559-122">**TestRoot** という名前の環境変数を作成し、Microsoft Windows PowerShell で次のコマンドレットを実行して **PerfSDK** フォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="1e559-122">Create an environment variable that is named **TestRoot**, and point it to the **PerfSDK** folder by running the following cmdlet in Microsoft Windows PowerShell.</span></span>

    ```Console
    [ENVIRONMENT]::SETENVIRONMENTVARIABLE("TESTROOT", "K:\PERFSDK\PERFSDKLOCALDIRECTORY", "USER")
    ```

    <span data-ttu-id="1e559-123">新しい環境変数を表示するには、**システム プロパティ** ダイアログ ボックスの **詳細** タブで **環境変数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-123">To view the new environment variable, in the **System Properties** dialog box, on the **Advanced** tab, select **Environment Variables**.</span></span>

    <span data-ttu-id="1e559-124">[![[環境変数とシステム プロパティ] ダイアログ ボックス](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-124">[![Environment Variables and System Properties dialog boxes](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</span></span>
    
3. <span data-ttu-id="1e559-125">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを入力して必要な証明書を生成してインストールします。</span><span class="sxs-lookup"><span data-stu-id="1e559-125">Open a **Command Prompt** window as an admin, and enter the following commands to generate and install the required certificate.</span></span> <span data-ttu-id="1e559-126">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-126">When you're prompted for a private key password, select **None**.</span></span>

    ```Console
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="1e559-127">上記のコマンドの要素について説明します:</span><span class="sxs-lookup"><span data-stu-id="1e559-127">Here is an explanation of the elements in preceding commands:</span></span>

    - <span data-ttu-id="1e559-128">**-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="1e559-128">**-n "CN=127.0.0.1"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="1e559-129">この証明書の名前が **127.0.0.1** であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="1e559-129">It's very important that the name of this certificate be **127.0.0.1**.</span></span> <span data-ttu-id="1e559-130">それ以外の場合は、単一ユーザー テストは実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="1e559-130">Otherwise, the single-user tests won't be able to run.</span></span>
    - <span data-ttu-id="1e559-131">**-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="1e559-131">**-eku 1.3.6.1.5.5.7.3.1** gives the purpose of the certificate.</span></span> <span data-ttu-id="1e559-132">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="1e559-132">It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</span></span>

    <span data-ttu-id="1e559-133">これらのコマンドは次の証明書を生成し C:\\Temp に保存します。</span><span class="sxs-lookup"><span data-stu-id="1e559-133">The commands generate the following certificates and save them in C:\\Temp:</span></span>

    - <span data-ttu-id="1e559-134">Authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="1e559-134">Authcert.pvk</span></span>
    - <span data-ttu-id="1e559-135">Authcert.cer</span><span class="sxs-lookup"><span data-stu-id="1e559-135">Authcert.cer</span></span>
    - <span data-ttu-id="1e559-136">Authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="1e559-136">Authcert.pfx</span></span>

4. <span data-ttu-id="1e559-137">**ローカル コンピューター\\個人** 証明書ストアで **authcert.pfx** と **authcert.cer** 証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="1e559-137">Install the **authcert.pfx** and **authcert.cer** certificates in the **Local Machine\\Personal** certificate store.</span></span>

    <span data-ttu-id="1e559-138">[![ローカル コンピューター\個人証明書ストア](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-138">[![Local Machine\Personal certificate store](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</span></span>

5. <span data-ttu-id="1e559-139">**PerfSDK\\PerfSDKLocalDirectory** フォルダーに **authcert.pfx** 証明書をコピーします。</span><span class="sxs-lookup"><span data-stu-id="1e559-139">Copy the **authcert.pfx** certificate to the **PerfSDK\\PerfSDKLocalDirectory** folder.</span></span>

    <span data-ttu-id="1e559-140">[![PerfSDK の証明書 \\ PerfS フォルダー](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-140">[![Certificate in PerfSDK\\PerfS folder](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</span></span>

6. <span data-ttu-id="1e559-141">以下で、**Visual Studio Online** フォルダーの **setup.md** ファイルを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1e559-141">Replace the **setup.md** file in the **Visual Studio Online** folder with the following.</span></span>

    ```Console
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

7. <span data-ttu-id="1e559-142">**Visual Studio Online** フォルダーの **CloudCtuFakeACSInstall.cmd** ファイルで、**インポート** コマンドから **%TestCertPassword%** を削除します。</span><span class="sxs-lookup"><span data-stu-id="1e559-142">In the **Visual Studio Online** folder, in the **CloudCtuFakeACSInstall.cmd** file, remove **%TestCertPassword%** from the **Import** command.</span></span>

    <span data-ttu-id="1e559-143">[![CloudCtuFakeACSInstall.cmd インポート コマンド](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-143">[![CloudCtuFakeACSInstall.cmd Import command](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</span></span>

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a><span data-ttu-id="1e559-144">マルチユーザー テスト用の PerfSDKSample ソリューションの準備</span><span class="sxs-lookup"><span data-stu-id="1e559-144">Prepare the PerfSDKSample solution for multi-user testing</span></span>

1. <span data-ttu-id="1e559-145">Microsoft Visual Studio の **テスト** メニューで、**テストの設定** にポイントして、**既定のプロセッサ アーキテクチャ** にポイントして、そして **x64** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-145">In Microsoft Visual Studio, on the **Test** menu, point to **Test settings**, point to **Default processor architecture**, and then select **x64**.</span></span>
2. <span data-ttu-id="1e559-146">管理者として次のコマンドレットを実行して、開発環境の **authcert.pfx** 証明書の拇印を取得します。階層 2 以上のサンドボックス環境を構成するときに必要になるため、拇印をどこかに保存します。</span><span class="sxs-lookup"><span data-stu-id="1e559-146">Retrieve the thumbprint of the **authcert.pfx** certificate in your development environment by running the following cmdlets as an admin. Save the thumbprint somewhere, because you will need it when you configure the tier-2 or above sandbox environment.</span></span>

    ```Console
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    <span data-ttu-id="1e559-147">次の図は、これらのコマンドレットが返す拇印の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e559-147">The following illustration shows an example of a thumbprint that these cmdlets return.</span></span>

    <span data-ttu-id="1e559-148">[![コマンド プロンプト ウィンドウの拇印](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-148">[![Thumbprint in the Command Prompt window](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e559-149">プラットフォーム更新プログラム 21 以降の環境では、発行者として **127.0.0.1** を持つ証明書が自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="1e559-149">In an environment that has Platform update 21 or later, a certificate that has **127.0.0.1** as the issuer is automatically installed.</span></span> <span data-ttu-id="1e559-150">生成した証明書の拇印を取得したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e559-150">Verify that you retrieve the thumbprint of the certificate that you generated.</span></span>

3. <span data-ttu-id="1e559-151">**CloudEnvironment.config** ファイルを更新してコンフィギュレーションを反映します。</span><span class="sxs-lookup"><span data-stu-id="1e559-151">Update the **CloudEnvironment.config** file to reflect your configurations.</span></span> <span data-ttu-id="1e559-152">この更新プログラムの一部として、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e559-152">As part of this update, follow these steps:</span></span>

    - <span data-ttu-id="1e559-153">**HostName** と **SOAPHostName** が階層 2 以上のサンドボックス環境と一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e559-153">Verify that **HostName** and **SOAPHostName** match your tier-2 or above sandbox environment.</span></span>
    - <span data-ttu-id="1e559-154">**authcert.pfx** 証明書の拇印を **SelfSigningCertificateThumbprint** の値として追加します。</span><span class="sxs-lookup"><span data-stu-id="1e559-154">Add the thumbprint of the **authcert.pfx** certificate as a value of **SelfSigningCertificateThumbprint**.</span></span>
    - <span data-ttu-id="1e559-155">**UserCount** を更新して、このケースでテスト ユーザーの数を反映します。</span><span class="sxs-lookup"><span data-stu-id="1e559-155">Update **UserCount** to reflect the number of test users in your case.</span></span>
    - <span data-ttu-id="1e559-156">**UserFormat** を更新して、テスト ユーザーの命名規則を反映します。</span><span class="sxs-lookup"><span data-stu-id="1e559-156">Update **UserFormat** to reflect your naming convention for test users.</span></span>

    <span data-ttu-id="1e559-157">[![更新された CloudEnvironment.config ファイル](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-157">[![Updated CloudEnvironment.config file](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</span></span>

4. <span data-ttu-id="1e559-158">**vsonline.testsettings** を構成します。</span><span class="sxs-lookup"><span data-stu-id="1e559-158">Configure **vsonline.testsettings**.</span></span> <span data-ttu-id="1e559-159">**テストの設定** ダイアログ ボックスの **一般** タブの **テストの実行場所** フィールド グループで **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-159">In the **Test Settings** dialog box, on the **General** tab, in the **Test run Location** field group, select the **Run tests using local computer or a test controller** option.</span></span>

    <span data-ttu-id="1e559-160">[![[テストの設定] ダイアログボックスの [一般] タブ](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-160">[![General tab of the Test Settings dialog box](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e559-161">**vsonline.testsettings** が表示されない場合は、ソリューションをもう一度開きます。</span><span class="sxs-lookup"><span data-stu-id="1e559-161">If you don't see **vsonline.testsettings**, reopen the solution.</span></span>

5. <span data-ttu-id="1e559-162">**配置** タブで **配置を有効にする** チェック ボックスを選択し、**ディレクトリの追加** と **ファイルの追加** ボタンを使用して **配置する追加のファイルやディレクトリ** フィールドにフォルダーとファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="1e559-162">On the **Deployment** tab, select the **Enable deployment** check box, and then use the **Add Directory** and **Add File** buttons to add the following folders and files to the **Additional files and directories to deploy** field.</span></span>

    - <span data-ttu-id="1e559-163">**K:\\PerfSDK\\PerfSDKLocalDirectory\\SampleProject\\PerfSDKSample\\bin\\Debug** フォルダー</span><span class="sxs-lookup"><span data-stu-id="1e559-163">**K:\\PerfSDK\\PerfSDKLocalDirectory\\SampleProject\\PerfSDKSample\\bin\\Debug** folder</span></span>
    - <span data-ttu-id="1e559-164">**K:\\PerfSDK\\PerfSDKLocalDirectory\\Visual Studio Online** フォルダー</span><span class="sxs-lookup"><span data-stu-id="1e559-164">**K:\\PerfSDK\\PerfSDKLocalDirectory\\Visual Studio Online** folder</span></span>
    - <span data-ttu-id="1e559-165">**K:\\PerfSDK\\PerfSDKLocalDirectory\\CloudEnvironment.Config** ファイル</span><span class="sxs-lookup"><span data-stu-id="1e559-165">**K:\\PerfSDK\\PerfSDKLocalDirectory\\CloudEnvironment.Config** file</span></span>
    - <span data-ttu-id="1e559-166">**K:\\PerfSDK\\PerfSDKLocalDirectory\\authcert.pfx** ファイル</span><span class="sxs-lookup"><span data-stu-id="1e559-166">**K:\\PerfSDK\\PerfSDKLocalDirectory\\authcert.pfx** file</span></span>
    - <span data-ttu-id="1e559-167">**K:\\PerfSDK\\PerfSDKLocalDirectory\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config** ファイル</span><span class="sxs-lookup"><span data-stu-id="1e559-167">**K:\\PerfSDK\\PerfSDKLocalDirectory\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config** file</span></span>

    <span data-ttu-id="1e559-168">[![[テストの設定] ダイアログ ボックスの [配置] タブ](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-168">[![Deployment tab of the Test Settings dialog box](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e559-169">"展開項目がソリューション フォルダにありません" という警告が表示されたら **OK** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="1e559-169">When you receive a warning that states, "Deployment item not in solution folder," select **OK** to continue.</span></span>

6. <span data-ttu-id="1e559-170">**ホスト** タブの **32 ビットまたは 64 ビット プロセスでテストを実行** フィールドで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-170">On the **Hosts** tab, in the **Run tests in 32 bits or 64 bits process** field, select **Run test in 64 bits process on 64 bits machine**.</span></span>
7. <span data-ttu-id="1e559-171">**適用** を選択して **テストの設定** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1e559-171">Select **Apply**, and then close the **Test Settings** dialog box.</span></span>
8. <span data-ttu-id="1e559-172">C\# パフォーマンス テストに次のステートメントを追加して、C\# パフォーマンス クラスを変更します。</span><span class="sxs-lookup"><span data-stu-id="1e559-172">Modify your C\# performance class by adding the following statement to your C\# performance tests.</span></span>

    ```csharp
    using MS.Dynamics.TestTools.UIHelpers.Core;
    ```

    <span data-ttu-id="1e559-173">[![MS.Dynamics.TestTools.UIHelpers.Core の使用; コマンド プロンプト ウィンドウのステートメント](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-173">[![using MS.Dynamics.TestTools.UIHelpers.Core; statement in the Command Prompt window](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</span></span>

9. <span data-ttu-id="1e559-174">**TestSetup()** メソッドの先頭に次の行を追加して **TestSetup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="1e559-174">Modify the **TestSetup** method by adding the following lines to the beginning of the **TestSetup()** method.</span></span>

    ```csharp
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir");
    if (string.IsNullOrEmpty(testroot))
    {
        testroot = System.IO.Directory.GetCurrentDirectory();
    }
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

    <span data-ttu-id="1e559-175">[![TestSetup メソッドに追加された行](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-175">[![Lines added to the TestSetup method](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</span></span>

10. <span data-ttu-id="1e559-176">**TestSetup** メソッドで "マルチユーザーの場合は以下の行をコメント解除" というコードの行をコメント解除して、次の行をコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="1e559-176">In the **TestSetup** method, uncomment lines in the code titled "for multi-user uncomment following lines", and comment out the following line.</span></span>

    ```csharp
    Client = DispatchedClient.DefaultInstance;
    ```

    <span data-ttu-id="1e559-177">[![変更されたコード](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-177">[![Modified code](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</span></span>

11. <span data-ttu-id="1e559-178">次の例と同様に **TestCleanup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="1e559-178">Modify the **TestCleanup** method so that it resembles the following example.</span></span>

    ```csharp
    public void TestCleanup()
    {
        Client.Close();
        Client.Dispose();
        Client = Null;
        //_userContext.Dispose();
    }
    ```

12. <span data-ttu-id="1e559-179">持っているすべての C\# パフォーマンス テスト クラスについてステップ 2 から 11 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1e559-179">Repeat steps 2 through 11 for all the C\# performance test classes that you have.</span></span>
13. <span data-ttu-id="1e559-180">完了したらソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="1e559-180">When you've finished, build the solution.</span></span>
14. <span data-ttu-id="1e559-181">**SampleLoadTest.loadtest** で **テスト ミックス** の下のテスト クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-181">In **SampleLoadTest.loadtest**, select your test class under **Test Mix**.</span></span>

    <span data-ttu-id="1e559-182">[![[テスト ミックスの編集] ダイアログ ボックス](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-182">[![Edit Test Mix dialog box](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</span></span>

14. <span data-ttu-id="1e559-183">**SampleLoadTest.loadtest** で **実行設定 1 \[有効\]** の **タイミング** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="1e559-183">In **SampleLoadTest.loadtest**, update the **Timing** fields of **Run Settings1 \[Active\]**.</span></span> <span data-ttu-id="1e559-184">これらのフィールドは **ウォームアップ期間**、**実行期間**、**クールダウン期間** を含みます。</span><span class="sxs-lookup"><span data-stu-id="1e559-184">These fields include **Warm-up Duration**, **Run Duration**, and **Cool-down Duration**.</span></span>

    <span data-ttu-id="1e559-185">[![タイミング フィールド](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-185">[![Timing fields](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</span></span>

15. <span data-ttu-id="1e559-186">**定数負荷パターン** で、テストの実行に使用するユーザーの総数に **定数ユーザー数** パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="1e559-186">In **Constant Load Pattern**, set the **Constant User Count** parameter to the total number of users that you want to use to run the test.</span></span>

    <span data-ttu-id="1e559-187">[![定数ユーザー数パラメーター](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-187">[![Constant User Count parameter](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</span></span>
    
## <a name="configure-a-tier-2-or-above-sandbox-environment-for-multi-user-testing"></a><span data-ttu-id="1e559-188">マルチユーザー テスト用に階層 2 以上のサンドボックス環境を構成する</span><span class="sxs-lookup"><span data-stu-id="1e559-188">Configure a tier-2 or above sandbox environment for multi-user testing</span></span>

1. <span data-ttu-id="1e559-189">各 Application Object Server (AOS) コンピューターの **ローカル コンピュータ\\パーソナル** の下に **authcert.pfx** と **authcert.cer** 証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="1e559-189">On each Application Object Server (AOS) computer, install the **authcert.pfx** and **authcert.cer** certificates under **Local Machine\\Personal**.</span></span>

    <span data-ttu-id="1e559-190">[![インストールした証明書](./media/multi-user-test-local-21.png)](./media/multi-user-test-local-21.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-190">[![Certificates installed](./media/multi-user-test-local-21.png)](./media/multi-user-test-local-21.png)</span></span>

2. <span data-ttu-id="1e559-191">**authcert.pfx** 証明書の拇印を階層 2 以上のサンドボックス環境の **wif.config** ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="1e559-191">Add the thumbprint of the **authcert.pfx** certificate in the **wif.config** file of your tier-2 or above sandbox environment.</span></span>
3. <span data-ttu-id="1e559-192">**管理ツール** から Microsoft インターネット インフォメーション サービス (IIS) マネージャを開き、**サイト** から **AOSService** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-192">Open Microsoft Internet Information Services (IIS) Manager from **Administrative Tools**, and then, under **Sites**, select **AOSService**.</span></span>
4. <span data-ttu-id="1e559-193">右側で **アクションの確認** を選択し、次にウィンドウの一番下から **wif.config** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="1e559-193">On the right, select **Explore in Actions**, and then find the **wif.config** file at the bottom of the window.</span></span>
5. <span data-ttu-id="1e559-194">生成された証明書の拇印を `https://fakeacs.accesscontrol.windows.net/` 認証局の末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="1e559-194">Add the thumbprint of the generated certificate to the bottom of the `https://fakeacs.accesscontrol.windows.net/` authority.</span></span>

    <span data-ttu-id="1e559-195">[![生成された証明書から追加された拇印](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-21.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-195">[![Thumbprint added from the generated certificate](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-21.png)</span></span>

6. <span data-ttu-id="1e559-196">変更を保存して IIRESET を実行します。</span><span class="sxs-lookup"><span data-stu-id="1e559-196">Save the change, and do an IIRESET.</span></span>
7. <span data-ttu-id="1e559-197">各 AOS コンピューターで手順 3 ～ 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1e559-197">Repeat steps 3 through 6 on each AOS computer.</span></span>
8. <span data-ttu-id="1e559-198">**SampleLoadTest.load** テストを開き、テスト ユーザーを作成してターゲット環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e559-198">Open the **SampleLoadTest.load** test to create test users and import them into your target environment.</span></span> <span data-ttu-id="1e559-199">次に各ユーザーに **システム管理者** セキュリティ ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1e559-199">Then assign the **System Administrator** security role to each user.</span></span>

    <span data-ttu-id="1e559-200">[![ターゲット環境のユーザー ページ](./media/multi-user-test-local-23.png)](./media/multi-user-test-local-22.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-200">[![Users page in the target environment](./media/multi-user-test-local-23.png)](./media/multi-user-test-local-22.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e559-201">**MS.Dynamics.Performance.CreateUsers.exe** を実行してテスト ユーザーを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="1e559-201">You can also create test users by running **MS.Dynamics.Performance.CreateUsers.exe**.</span></span> <span data-ttu-id="1e559-202">この場合、IISRESET を実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1e559-202">In this case, you don't have to do an IISRESET.</span></span>

## <a name="run-multi-user-testing-by-using-a-local-test-controller"></a><span data-ttu-id="1e559-203">ローカル テスト コントローラーを使用したマルチユーザー テストの実行</span><span class="sxs-lookup"><span data-stu-id="1e559-203">Run multi-user testing by using a local test controller</span></span>

1. <span data-ttu-id="1e559-204">devbox 上の Visual Studio で **負荷テストの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e559-204">On the devbox, in Visual Studio, select **Run Load Test**.</span></span>

    <span data-ttu-id="1e559-205">[![負荷テストの実行](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-205">[![Run Load Test](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</span></span>

2. <span data-ttu-id="1e559-206">テスト出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="1e559-206">Review the test output.</span></span>

    <span data-ttu-id="1e559-207">[![テストの出力](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</span><span class="sxs-lookup"><span data-stu-id="1e559-207">[![Test output](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e559-208">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1e559-208">Troubleshooting</span></span>

<span data-ttu-id="1e559-209">パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e559-209">For information about single-user or multi-user testing that uses the Performance SDK, see [Troubleshooting guide for single-user or multi-user testing with the Performance SDK](troubleshoot-perf-sdk-user-testing.md).</span></span>
