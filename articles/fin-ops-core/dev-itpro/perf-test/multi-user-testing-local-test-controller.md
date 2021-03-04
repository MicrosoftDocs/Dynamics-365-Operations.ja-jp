---
title: ローカル テスト コントローラーを使用したマルチ ユーザー パフォーマンス SDK テスト
description: このトピックでは、Microsoft Visual Studio、パフォーマンス SDK、およびタスク レコーダー テスト スクリプトを使用してマルチユーザー テストを行う方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0446a90c39c32c36362637feac221a4fc782f3d2
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128371"
---
# <a name="multi-user-performance-sdk-testing-with-a-local-test-controller"></a><span data-ttu-id="9fd68-103">ローカル テスト コントローラーを使用したマルチ ユーザー パフォーマンス SDK テスト</span><span class="sxs-lookup"><span data-stu-id="9fd68-103">Multi-user Performance SDK testing with a local test controller</span></span>

[!include [banner](../includes/banner.md)]

 > [!IMPORTANT]
  > <span data-ttu-id="9fd68-104">Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。</span><span class="sxs-lookup"><span data-stu-id="9fd68-104">Visual Studio 2019 will be the last version of Visual Studio with web performance and load test features.</span></span> <span data-ttu-id="9fd68-105">将来的に、代替ソリューションの推奨を公開します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-105">In the future, we will publish some recommendations for alternative solutions.</span></span>  
  > - <span data-ttu-id="9fd68-106">Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-106">If you are using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="9fd68-107">そのサポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-107">You can continue using it until the end of the support cycle.</span></span> 
  > - <span data-ttu-id="9fd68-108">クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-108">If you are using the cloud-based load testing service, it will continue to run through March 31, 2020.</span></span> <span data-ttu-id="9fd68-109">それまでの間は、同サービスの全機能を継続してご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-109">Until then, you can continue to use all of the experiences powered by this service without interruption.</span></span> <span data-ttu-id="9fd68-110">また、オンプレミス負荷テストに切り替えることがも可能です。</span><span class="sxs-lookup"><span data-stu-id="9fd68-110">Alternatively, you can switch to on-premises load testing.</span></span> <span data-ttu-id="9fd68-111">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="9fd68-111">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9fd68-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="9fd68-112">Prerequisites</span></span>

<span data-ttu-id="9fd68-113">このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:</span><span class="sxs-lookup"><span data-stu-id="9fd68-113">Before you complete the steps in this topic, verify that the following prerequisites are met:</span></span>

- <span data-ttu-id="9fd68-114">Microsoft Azure サブスクリプションに、プラットフォーム更新プログラム 21 以降の開発環境があります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-114">You have a development environment that has Platform update 21 or later in your Microsoft Azure subscription.</span></span>
> [!IMPORTANT]
> <span data-ttu-id="9fd68-115">Finance and Operations アプリが 21Vianet に配置された場合、環境のプラットフォーム更新プログラムは 10.0.11 またはそれ以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-115">If your Finance and Operations apps were deployed in 21Vianet, the platform update of your environment must be Platform Update for 10.0.11 or above.</span></span>
- <span data-ttu-id="9fd68-116">開発環境には Microsoft Visual Studio Enterprise Edition があります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-116">You have Microsoft Visual Studio Enterprise edition in a development environment.</span></span>
- <span data-ttu-id="9fd68-117">開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-117">You have a tier-2 or above sandbox environment that has the same release (application version and platform update) as your development environment.</span></span>
- <span data-ttu-id="9fd68-118">[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従って開発環境を構成しました。</span><span class="sxs-lookup"><span data-stu-id="9fd68-118">You've configured your development environment by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>
- <span data-ttu-id="9fd68-119">エンド ツー エンド (E2E) シナリオ用に C\# パフォーマンス テスト クラスが生成され、[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従ってシングルユーザー テストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-119">C\# performance testing classes have been generated for your end-to-end (E2E) scenarios, and you can run a single-user test by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>

## <a name="configure-a-development-environment-for-multi-user-testing"></a><span data-ttu-id="9fd68-120">マルチ ユーザー テストのための開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9fd68-120">Configure a development environment for multi-user testing</span></span>

1. <span data-ttu-id="9fd68-121">[SQL Server の ODBC ドライバー 17](https://docs.microsoft.com/sql/connect/odbc/download-odbc-driver-for-sql-server) をダウンロードして、ダウンロードしたファイルを **msodbcsql** に名前を変更して、それを **PerfSDK** フォルダーの **Visual Studio Online** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-121">Download [ODBC Driver 17 for SQL Server](https://docs.microsoft.com/sql/connect/odbc/download-odbc-driver-for-sql-server), rename the download file **msodbcsql**, and copy it to the **Visual Studio Online** folder under the **PerfSDK** folder.</span></span>

    <span data-ttu-id="9fd68-122">[![Visual Studio Online フォルダーの msodbcsql ファイル](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-122">[![msodbcsql file in Visual Studio Online folder](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)</span></span>

2. <span data-ttu-id="9fd68-123">**TestRoot** という名前の環境変数を作成し、Microsoft Windows PowerShell で次のコマンドレットを実行して **PerfSDK** フォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-123">Create an environment variable that is named **TestRoot**, and point it to the **PerfSDK** folder by running the following cmdlet in Microsoft Windows PowerShell.</span></span>

    ```Console
    [ENVIRONMENT]::SETENVIRONMENTVARIABLE("TESTROOT", "K:\PERFSDK\PERFSDKLOCALDIRECTORY", "USER")
    ```

    <span data-ttu-id="9fd68-124">新しい環境変数を表示するには、**システム プロパティ** ダイアログ ボックスの **詳細** タブで **環境変数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-124">To view the new environment variable, in the **System Properties** dialog box, on the **Advanced** tab, select **Environment Variables**.</span></span>

    <span data-ttu-id="9fd68-125">[![[環境変数とシステム プロパティ] ダイアログ ボックス](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-125">[![Environment Variables and System Properties dialog boxes](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)</span></span>
    
3. <span data-ttu-id="9fd68-126">管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを入力して必要な証明書を生成してインストールします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-126">Open a **Command Prompt** window as an admin, and enter the following commands to generate and install the required certificate.</span></span> <span data-ttu-id="9fd68-127">プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-127">When you're prompted for a private key password, select **None**.</span></span>

    ```Console
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    <span data-ttu-id="9fd68-128">上記のコマンドの要素について説明します:</span><span class="sxs-lookup"><span data-stu-id="9fd68-128">Here is an explanation of the elements in preceding commands:</span></span>

    - <span data-ttu-id="9fd68-129">**-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-129">**-n "CN=127.0.0.1"** gives a human-readable name to the certificate.</span></span> <span data-ttu-id="9fd68-130">この証明書の名前が **127.0.0.1** であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="9fd68-130">It's very important that the name of this certificate be **127.0.0.1**.</span></span> <span data-ttu-id="9fd68-131">それ以外の場合は、単一ユーザー テストは実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="9fd68-131">Otherwise, the single-user tests won't be able to run.</span></span>
    - <span data-ttu-id="9fd68-132">**-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-132">**-eku 1.3.6.1.5.5.7.3.1** gives the purpose of the certificate.</span></span> <span data-ttu-id="9fd68-133">証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-133">It indicates that the certificate can be used as a Secure Sockets Layer (SSL) server certificate.</span></span>

    <span data-ttu-id="9fd68-134">これらのコマンドは次の証明書を生成し C:\\Temp に保存します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-134">The commands generate the following certificates and save them in C:\\Temp:</span></span>

    - <span data-ttu-id="9fd68-135">Authcert.pvk</span><span class="sxs-lookup"><span data-stu-id="9fd68-135">Authcert.pvk</span></span>
    - <span data-ttu-id="9fd68-136">Authcert.cer</span><span class="sxs-lookup"><span data-stu-id="9fd68-136">Authcert.cer</span></span>
    - <span data-ttu-id="9fd68-137">Authcert.pfx</span><span class="sxs-lookup"><span data-stu-id="9fd68-137">Authcert.pfx</span></span>

4. <span data-ttu-id="9fd68-138">**ローカル コンピューター\\個人** 証明書ストアで **authcert.pfx** と **authcert.cer** 証明書をインストールします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-138">Install the **authcert.pfx** and **authcert.cer** certificates in the **Local Machine\\Personal** certificate store.</span></span>

    <span data-ttu-id="9fd68-139">[![ローカル コンピューター\個人証明書ストア](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-139">[![Local Machine\Personal certificate store](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)</span></span>

5. <span data-ttu-id="9fd68-140">**PerfSDK\\PerfSDKLocalDirectory** フォルダーに **authcert.pfx** 証明書をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-140">Copy the **authcert.pfx** certificate to the **PerfSDK\\PerfSDKLocalDirectory** folder.</span></span>

    <span data-ttu-id="9fd68-141">[![PerfSDK の証明書 \\ PerfS フォルダー](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-141">[![Certificate in PerfSDK\\PerfS folder](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)</span></span>

6. <span data-ttu-id="9fd68-142">以下で、**Visual Studio Online** フォルダーの **setup.md** ファイルを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-142">Replace the **setup.md** file in the **Visual Studio Online** folder with the following.</span></span>

    ```Console
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

7. <span data-ttu-id="9fd68-143">**Visual Studio Online** フォルダーの **CloudCtuFakeACSInstall.cmd** ファイルで、**インポート** コマンドから **%TestCertPassword%** を削除します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-143">In the **Visual Studio Online** folder, in the **CloudCtuFakeACSInstall.cmd** file, remove **%TestCertPassword%** from the **Import** command.</span></span>

    <span data-ttu-id="9fd68-144">[![CloudCtuFakeACSInstall.cmd インポート コマンド](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-144">[![CloudCtuFakeACSInstall.cmd Import command](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)</span></span>

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a><span data-ttu-id="9fd68-145">マルチユーザー テスト用の PerfSDKSample ソリューションの準備</span><span class="sxs-lookup"><span data-stu-id="9fd68-145">Prepare the PerfSDKSample solution for multi-user testing</span></span>

1. <span data-ttu-id="9fd68-146">Microsoft Visual Studio の **テスト** メニューで、**テストの設定** にポイントして、**既定のプロセッサ アーキテクチャ** にポイントして、そして **x64** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-146">In Microsoft Visual Studio, on the **Test** menu, point to **Test settings**, point to **Default processor architecture**, and then select **x64**.</span></span>
2. <span data-ttu-id="9fd68-147">管理者として次のコマンドレットを実行して、開発環境の **authcert.pfx** 証明書の拇印を取得します。階層 2 以上のサンドボックス環境を構成するときに必要になるため、拇印をどこかに保存します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-147">Retrieve the thumbprint of the **authcert.pfx** certificate in your development environment by running the following cmdlets as an admin. Save the thumbprint somewhere, because you will need it when you configure the tier-2 or above sandbox environment.</span></span>

    ```Console
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    <span data-ttu-id="9fd68-148">次の図は、これらのコマンドレットが返す拇印の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9fd68-148">The following illustration shows an example of a thumbprint that these cmdlets return.</span></span>

    <span data-ttu-id="9fd68-149">[![コマンド プロンプト ウィンドウの拇印](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-149">[![Thumbprint in the Command Prompt window](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fd68-150">プラットフォーム更新プログラム 21 以降の環境では、発行者として **127.0.0.1** を持つ証明書が自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-150">In an environment that has Platform update 21 or later, a certificate that has **127.0.0.1** as the issuer is automatically installed.</span></span> <span data-ttu-id="9fd68-151">生成した証明書の拇印を取得したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-151">Verify that you retrieve the thumbprint of the certificate that you generated.</span></span>

3. <span data-ttu-id="9fd68-152">**CloudEnvironment.config** ファイルを更新してコンフィギュレーションを反映します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-152">Update the **CloudEnvironment.config** file to reflect your configurations.</span></span> <span data-ttu-id="9fd68-153">この更新プログラムの一部として、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-153">As part of this update, follow these steps:</span></span>

    - <span data-ttu-id="9fd68-154">**HostName** と **SOAPHostName** が階層 2 以上のサンドボックス環境と一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-154">Verify that **HostName** and **SOAPHostName** match your tier-2 or above sandbox environment.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9fd68-155">テスト環境の **HostName** または **SOAPHostName** がわからない場合は、**Infrastructure.HostUrl** または **Infrastructure.SoapServicesUrl** の AOS サーバーの web.config ファイルで検索できます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-155">If you don't know the **HostName** or **SOAPHostName** of your test environment, you can find it in the web.config file for the AOS server in **Infrastructure.HostUrl** or **Infrastructure.SoapServicesUrl**.</span></span>
    
    - <span data-ttu-id="9fd68-156">**authcert.pfx** 証明書の拇印を **SelfSigningCertificateThumbprint** の値として追加します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-156">Add the thumbprint of the **authcert.pfx** certificate as a value of **SelfSigningCertificateThumbprint**.</span></span>
    - <span data-ttu-id="9fd68-157">**UserCount** を更新して、このケースでテスト ユーザーの数を反映します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-157">Update **UserCount** to reflect the number of test users in your case.</span></span>
    - <span data-ttu-id="9fd68-158">**UserFormat** を更新して、テスト ユーザーの命名規則を反映します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-158">Update **UserFormat** to reflect your naming convention for test users.</span></span>

    <span data-ttu-id="9fd68-159">[![更新された CloudEnvironment.config ファイル](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-159">[![Updated CloudEnvironment.config file](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)</span></span>

    - <span data-ttu-id="9fd68-160">Finance and Operations アプリが 21Vianet に配置された場合、**SelfMintingSysUser** および **SelfMintingAdminUser** で **NetworkDomain="https://sts.chinacloudapi.cn/"** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="9fd68-160">If your Finance and Operations apps were deployed in 21Vianet, make sure to specify **NetworkDomain="https://sts.chinacloudapi.cn/"** in **SelfMintingSysUser** and **SelfMintingAdminUser**.</span></span>

4. <span data-ttu-id="9fd68-161">**vsonline.testsettings** を構成します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-161">Configure **vsonline.testsettings**.</span></span> <span data-ttu-id="9fd68-162">**テストの設定** ダイアログ ボックスの **一般** タブの **テストの実行場所** フィールド グループで **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-162">In the **Test Settings** dialog box, on the **General** tab, in the **Test run Location** field group, select the **Run tests using local computer or a test controller** option.</span></span>

    <span data-ttu-id="9fd68-163">[![[テストの設定] ダイアログボックスの [一般] タブ](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-163">[![General tab of the Test Settings dialog box](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fd68-164">**vsonline.testsettings** が表示されない場合は、ソリューションをもう一度開きます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-164">If you don't see **vsonline.testsettings**, reopen the solution.</span></span>

5. <span data-ttu-id="9fd68-165">**配置** タブで **配置を有効にする** チェック ボックスを選択し、**ディレクトリの追加** と **ファイルの追加** ボタンを使用して **配置する追加のファイルやディレクトリ** フィールドにフォルダーとファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-165">On the **Deployment** tab, select the **Enable deployment** check box, and then use the **Add Directory** and **Add File** buttons to add the following folders and files to the **Additional files and directories to deploy** field.</span></span>

    - <span data-ttu-id="9fd68-166">**K:\\PerfSDK\\PerfSDKLocalDirectory\\SampleProject\\PerfSDKSample\\bin\\Debug** フォルダー</span><span class="sxs-lookup"><span data-stu-id="9fd68-166">**K:\\PerfSDK\\PerfSDKLocalDirectory\\SampleProject\\PerfSDKSample\\bin\\Debug** folder</span></span>
    - <span data-ttu-id="9fd68-167">**K:\\PerfSDK\\PerfSDKLocalDirectory\\Visual Studio Online** フォルダー</span><span class="sxs-lookup"><span data-stu-id="9fd68-167">**K:\\PerfSDK\\PerfSDKLocalDirectory\\Visual Studio Online** folder</span></span>
    - <span data-ttu-id="9fd68-168">**K:\\PerfSDK\\PerfSDKLocalDirectory\\CloudEnvironment.Config** ファイル</span><span class="sxs-lookup"><span data-stu-id="9fd68-168">**K:\\PerfSDK\\PerfSDKLocalDirectory\\CloudEnvironment.Config** file</span></span>
    - <span data-ttu-id="9fd68-169">**K:\\PerfSDK\\PerfSDKLocalDirectory\\authcert.pfx** ファイル</span><span class="sxs-lookup"><span data-stu-id="9fd68-169">**K:\\PerfSDK\\PerfSDKLocalDirectory\\authcert.pfx** file</span></span>
    - <span data-ttu-id="9fd68-170">**K:\\PerfSDK\\PerfSDKLocalDirectory\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config** ファイル</span><span class="sxs-lookup"><span data-stu-id="9fd68-170">**K:\\PerfSDK\\PerfSDKLocalDirectory\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config** file</span></span>

    <span data-ttu-id="9fd68-171">[![[テストの設定] ダイアログ ボックスの [配置] タブ](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-171">[![Deployment tab of the Test Settings dialog box](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fd68-172">"展開項目がソリューション フォルダにありません" という警告が表示されたら **OK** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-172">When you receive a warning that states, "Deployment item not in solution folder," select **OK** to continue.</span></span>

6. <span data-ttu-id="9fd68-173">**ホスト** タブの **32 ビットまたは 64 ビット プロセスでテストを実行** フィールドで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-173">On the **Hosts** tab, in the **Run tests in 32 bits or 64 bits process** field, select **Run test in 64 bits process on 64 bits machine**.</span></span>
7. <span data-ttu-id="9fd68-174">**適用** を選択して **テストの設定** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-174">Select **Apply**, and then close the **Test Settings** dialog box.</span></span>
8. <span data-ttu-id="9fd68-175">C\# パフォーマンス テストに次のステートメントを追加して、C\# パフォーマンス クラスを変更します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-175">Modify your C\# performance class by adding the following statement to your C\# performance tests.</span></span>

    ```csharp
    using MS.Dynamics.TestTools.UIHelpers.Core;
    ```

    <span data-ttu-id="9fd68-176">[![MS.Dynamics.TestTools.UIHelpers.Core の使用; コマンド プロンプト ウィンドウのステートメント](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-176">[![using MS.Dynamics.TestTools.UIHelpers.Core; statement in the Command Prompt window](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)</span></span>

9. <span data-ttu-id="9fd68-177">**TestSetup()** メソッドの先頭に次の行を追加して **TestSetup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-177">Modify the **TestSetup** method by adding the following lines to the beginning of the **TestSetup()** method.</span></span>

    ```csharp
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir");
    if (string.IsNullOrEmpty(testroot))
    {
        testroot = System.IO.Directory.GetCurrentDirectory();
    }
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

    <span data-ttu-id="9fd68-178">[![TestSetup メソッドに追加された行](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-178">[![Lines added to the TestSetup method](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)</span></span>

10. <span data-ttu-id="9fd68-179">**TestSetup** メソッドで "マルチユーザーの場合は以下の行をコメント解除" というコードの行をコメント解除して、次の行をコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-179">In the **TestSetup** method, uncomment lines in the code titled "for multi-user uncomment following lines", and comment out the following line.</span></span>

    ```csharp
    Client = DispatchedClient.DefaultInstance;
    ```

    <span data-ttu-id="9fd68-180">[![変更されたコード](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-180">[![Modified code](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)</span></span>

11. <span data-ttu-id="9fd68-181">次の例と同様に **TestCleanup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-181">Modify the **TestCleanup** method so that it resembles the following example.</span></span>

    ```csharp
    public void TestCleanup()
    {
        Client.Close();
        Client.Dispose();
        Client = Null;
        //_userContext.Dispose();
    }
    ```

12. <span data-ttu-id="9fd68-182">持っているすべての C\# パフォーマンス テスト クラスについてステップ 2 から 11 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-182">Repeat steps 2 through 11 for all the C\# performance test classes that you have.</span></span>
13. <span data-ttu-id="9fd68-183">完了したらソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-183">When you've finished, build the solution.</span></span>
14. <span data-ttu-id="9fd68-184">**SampleLoadTest.loadtest** で **テスト ミックス** の下のテスト クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-184">In **SampleLoadTest.loadtest**, select your test class under **Test Mix**.</span></span>

    <span data-ttu-id="9fd68-185">[![[テスト ミックスの編集] ダイアログ ボックス](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-185">[![Edit Test Mix dialog box](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)</span></span>

14. <span data-ttu-id="9fd68-186">**SampleLoadTest.loadtest** で **実行設定 1 \[有効\]** の **タイミング** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-186">In **SampleLoadTest.loadtest**, update the **Timing** fields of **Run Settings1 \[Active\]**.</span></span> <span data-ttu-id="9fd68-187">これらのフィールドは **ウォームアップ期間**、**実行期間**、**クールダウン期間** を含みます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-187">These fields include **Warm-up Duration**, **Run Duration**, and **Cool-down Duration**.</span></span>

    <span data-ttu-id="9fd68-188">[![タイミング フィールド](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-188">[![Timing fields](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)</span></span>

15. <span data-ttu-id="9fd68-189">**定数負荷パターン** で、テストの実行に使用するユーザーの総数に **定数ユーザー数** パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-189">In **Constant Load Pattern**, set the **Constant User Count** parameter to the total number of users that you want to use to run the test.</span></span>

    <span data-ttu-id="9fd68-190">[![定数ユーザー数パラメーター](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-190">[![Constant User Count parameter](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)</span></span>
    
## <a name="configure-a-tier-2-or-above-sandbox-environment-for-multi-user-testing"></a><span data-ttu-id="9fd68-191">マルチユーザー テスト用に階層 2 以上のサンドボックス環境を構成する</span><span class="sxs-lookup"><span data-stu-id="9fd68-191">Configure a tier-2 or above sandbox environment for multi-user testing</span></span>

### <a name="if-your-aos-allows-remote-desktop-connections"></a><span data-ttu-id="9fd68-192">AOS がリモート デスクトップ接続を許可している場合</span><span class="sxs-lookup"><span data-stu-id="9fd68-192">If your AOS allows Remote Desktop connections</span></span>

1. <span data-ttu-id="9fd68-193">**管理ツール** から Microsoft インターネット インフォメーション サービス (IIS) マネージャを開き、**サイト** から **AOSService** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-193">Open Microsoft Internet Information Services (IIS) Manager from **Administrative Tools**, and then, under **Sites**, select **AOSService**.</span></span>
2. <span data-ttu-id="9fd68-194">右側で **アクションの確認** を選択し、次にウィンドウの一番下から **wif.config** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-194">On the right, select **Explore in Actions**, and then find the **wif.config** file at the bottom of the window.</span></span>
3. <span data-ttu-id="9fd68-195">**authcert.pfx** 証明書の拇印を `https://fakeacs.accesscontrol.windows.net/` オーソリティの下部に追加し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-195">Add the thumbprint of the **authcert.pfx** certificate to the bottom of the `https://fakeacs.accesscontrol.windows.net/` authority and save the change.</span></span>

    <span data-ttu-id="9fd68-196">[![生成された証明書から追加された拇印](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-22.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-196">[![Thumbprint added from the generated certificate](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-22.png)</span></span>

4. <span data-ttu-id="9fd68-197">各 AOS コンピューターで手順 1 ～ 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-197">Repeat steps 1 through 3 on each AOS computer.</span></span>
5. <span data-ttu-id="9fd68-198">すべての AOS インスタンスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-198">Restart all AOS instances.</span></span>

### <a name="if-you-do-not-have-remote-desktop-access-to-the-server"></a><span data-ttu-id="9fd68-199">サーバーへのリモート デスクトップ アクセス権がない場合</span><span class="sxs-lookup"><span data-stu-id="9fd68-199">If you do not have Remote Desktop access to the server</span></span>

<span data-ttu-id="9fd68-200">Microsoft が管理するサンドボックス、またはセルフ サービス タイプ サンドボックスなど、リモート デスクトップ プロトコル (RDP) アクセスが削除された場合、Microsoft は環境に応じた証明書を生成し、事前にコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-200">In cases where your Remote Desktop Protocol (RDP) access is removed, such as Microsoft-managed or self-service type sandboxes, Microsoft will generate the certificate for your environment and have it pre-configured.</span></span> <span data-ttu-id="9fd68-201">次の手順に従って、PerfSDK での使用に必要な RSAT 証明書を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-201">Follow these steps to retrieve the RSAT certificate, which is necessary to use with PerfSDK.</span></span>

1. <span data-ttu-id="9fd68-202">Lifecycle Services の環境詳細ページの **管理** の下に、2 つの新しいオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-202">Under **Maintain** on your environment details page in Lifecycle Services you'll see two new options.</span></span>
  - <span data-ttu-id="9fd68-203">RSAT 証明書のダウンロード</span><span class="sxs-lookup"><span data-stu-id="9fd68-203">Download RSAT certificate</span></span>
  - <span data-ttu-id="9fd68-204">RSAT 証明書を再生成する</span><span class="sxs-lookup"><span data-stu-id="9fd68-204">Regenerate RSAT certificate</span></span>

![RSAT 証明書のオプションのダウンロードと再生成](rsat/media/rsat-lcs1.png)

<span data-ttu-id="9fd68-206">**ダウンロード** ボタンを使用して、証明書バンドルを .zip ファイルとして取得します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-206">Use the **Download** button to retrieve the certificate bundle as a .zip file.</span></span>

2. <span data-ttu-id="9fd68-207">クリアテキスト パスワードが画面に表示されるという警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-207">You'll receive a warning that a clear-text password will be displayed on your screen.</span></span> <span data-ttu-id="9fd68-208">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-208">Select **Yes** to continue.</span></span>

3. <span data-ttu-id="9fd68-209">クリアテキスト パスワードを後で使用できるようにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-209">Copy the clear-text password for later use.</span></span> <span data-ttu-id="9fd68-210">.zip ファイルがダウンロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-210">You'll see the .zip file has been downloaded.</span></span> <span data-ttu-id="9fd68-211">.zip ファイルの内部には、証明書 (.cer) と個人情報交換 (.pfx) ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-211">Inside the .zip file is a certificate (.cer) and a personal information exchange (.pfx) file.</span></span> <span data-ttu-id="9fd68-212">ファイルを解凍します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-212">Unzip the file.</span></span>

4. <span data-ttu-id="9fd68-213">証明書をダブルクリックして開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-213">Double-click the certificate to open it, and then select **Install**.</span></span> <span data-ttu-id="9fd68-214">この証明書をローカル コンピューターにインストールしてから、**個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-214">Install this certificate to your local machine, and then browse to the **Personal** store.</span></span> <span data-ttu-id="9fd68-215">ローカル コンピューターに対してこの手順を繰り返し、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-215">Repeat this process for the local machine, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>

5. <span data-ttu-id="9fd68-216">個人情報交換 (.pfx) ファイルをダブルクリックして開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-216">Double-click the personal information exchange (.pfx) file to open it, and select **Install**.</span></span> <span data-ttu-id="9fd68-217">この証明書をローカル コンピューターにインストールしてから、手順 2 で保存したパスワードを入力して **個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-217">Install this certificate to your local machine, enter the password saved in step 2, and browse to the **Personal** store.</span></span> <span data-ttu-id="9fd68-218">ローカル コンピューターの場所に対してこの手順を繰り返し、手順 2 で保存したパスワードを入力して、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-218">Repeat this process for the local machine location, enter the password saved in step 2, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>

6. <span data-ttu-id="9fd68-219">証明書ファイルをダブルクリックして、開きます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-219">Double-click the certificate file to open it.</span></span> <span data-ttu-id="9fd68-220">**詳細** タブを参照し、**拇印** セクションが表示されるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-220">Browse to the **Details** tab, and scroll down until you see the **Thumbprint** section.</span></span> <span data-ttu-id="9fd68-221">**拇印** を選択し、テキスト ボックスに ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-221">Select **Thumbprint**, and copy the ID in the text box.</span></span> <span data-ttu-id="9fd68-222">RSAT に対してこの拇印を使用し、PerfSDK **CloudEnvironment.config** 拇印を更新します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-222">Use this thumbprint for RSAT and to update your PerfSDK **CloudEnvironment.config** thumbprint.</span></span>
<span data-ttu-id="9fd68-223">![拇印の設定](rsat/media/rsat-lcs4.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-223">![Thumbprint settings](rsat/media/rsat-lcs4.png)</span></span>

<span data-ttu-id="9fd68-224">これで、この証明書を使用して環境に対してテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-224">You can now run your tests against the environment using this certificate.</span></span> <span data-ttu-id="9fd68-225">証明書は期限が切れる前に Microsoft によって自動的にローテーションされます。その後、上記の手順 1 からこの証明書の新しいバージョンをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fd68-225">The certificate will be auto-rotated by Microsoft before it expires, at which time you will need to download a new version of this certificate starting from step 1 above.</span></span> <span data-ttu-id="9fd68-226">セルフ サービス環境では、有効期限に最も近いダウンタイム ウィンドウで 90 日ごとにローテーションされます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-226">For self-service environments this will be rotated every 90 days during a downtime window that is closest to the expiry.</span></span> <span data-ttu-id="9fd68-227">これらのダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-227">These downtime windows include customer initiated package deployment, and database movement operations that target the environment.</span></span>

## <a name="create-test-users"></a><span data-ttu-id="9fd68-228">新規ユーザーのテスト</span><span class="sxs-lookup"><span data-stu-id="9fd68-228">Create test users</span></span>

<span data-ttu-id="9fd68-229">**SampleLoadTest.load** テストを開き、テスト ユーザーを作成してターゲット環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="9fd68-229">Open the **SampleLoadTest.load** test to create test users and import them into your target environment.</span></span> <span data-ttu-id="9fd68-230">次に各ユーザーに **システム管理者** セキュリティ ロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-230">Then assign the **System Administrator** security role to each user.</span></span>

![ターゲット環境のユーザー ページ](./media/multi-user-test-local-23.png)

> [!NOTE]
> <span data-ttu-id="9fd68-232">**MS.Dynamics.Performance.CreateUsers.exe** を実行してテスト ユーザーを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="9fd68-232">You can also create test users by running **MS.Dynamics.Performance.CreateUsers.exe**.</span></span> <span data-ttu-id="9fd68-233">この場合、IISRESET を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9fd68-233">In this case, you don't have to use IISRESET.</span></span>

## <a name="run-multi-user-testing-by-using-a-local-test-controller"></a><span data-ttu-id="9fd68-234">ローカル テスト コントローラーを使用したマルチユーザー テストの実行</span><span class="sxs-lookup"><span data-stu-id="9fd68-234">Run multi-user testing by using a local test controller</span></span>

1. <span data-ttu-id="9fd68-235">devbox 上の Visual Studio で **負荷テストの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-235">On the devbox, in Visual Studio, select **Run Load Test**.</span></span>

    <span data-ttu-id="9fd68-236">[![負荷テストの実行](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-236">[![Run Load Test](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)</span></span>

2. <span data-ttu-id="9fd68-237">テスト出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="9fd68-237">Review the test output.</span></span>

    <span data-ttu-id="9fd68-238">[![テストの出力](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</span><span class="sxs-lookup"><span data-stu-id="9fd68-238">[![Test output](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9fd68-239">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="9fd68-239">Troubleshooting</span></span>

<span data-ttu-id="9fd68-240">パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fd68-240">For information about single-user or multi-user testing that uses the Performance SDK, see [Troubleshooting guide for single-user or multi-user testing with the Performance SDK](troubleshoot-perf-sdk-user-testing.md).</span></span>
