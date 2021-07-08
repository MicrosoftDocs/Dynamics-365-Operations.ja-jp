---
title: パフォーマンス SDK によるマルチユーザー テストを実行する
description: このトピックでは、Microsoft Visual Studio、パフォーマンス ソフトウェア開発キット (SDK)、およびタスク レコーダー テスト スクリプトを使用してマルチユーザー テストを実行する方法について説明します。
author: kennysaelen
ms.date: 06/04/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: kesaelen
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 132629a82d03f915884d44ad62080c8fc4d17630
ms.sourcegitcommit: 55ca275705a624d446d2abb60b5d676b86fe7240
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2021
ms.locfileid: "6306788"
---
# <a name="run-multi-user-testing-by-using-the-performance-sdk"></a><span data-ttu-id="dc9af-103">パフォーマンス SDK によるマルチユーザー テストを実行する</span><span class="sxs-lookup"><span data-stu-id="dc9af-103">Run multi-user testing by using the Performance SDK</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc9af-104">このトピックでは、Microsoft Visual Studio、パフォーマンス ソフトウェア開発キット (SDK)、およびタスク レコーダー テスト スクリプトを使用してマルチユーザー テストを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-104">This topic explains how to run multi-user testing by using Microsoft Visual Studio, the Performance software development kit (SDK), and the Task recorder test scripts.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc9af-105">Visual Studio 2019 は Web パフォーマンスと負荷テスト機能を含む Visual Studio の最新バージョンです。</span><span class="sxs-lookup"><span data-stu-id="dc9af-105">Visual Studio 2019 will be the last version of Visual Studio that includes web performance and load testing features.</span></span> <span data-ttu-id="dc9af-106">Visual Studio および、オンプレミスでの負荷テストに向けたテスト コントローラー/テスト エージェントをご利用の場合、 Visual Studio 2019 が最新のバージョンになります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-106">If you're using the Visual Studio and Test Controller/Test Agent for on-premises load testing, Visual Studio 2019 will be the last version.</span></span> <span data-ttu-id="dc9af-107">そのサポート サイクルが終了するまで継続して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-107">You can continue to use it until the end of the support cycle.</span></span> <span data-ttu-id="dc9af-108">詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-108">For more information, see [Cloud-based load testing service end of life](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc9af-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="dc9af-109">Prerequisites</span></span>

<span data-ttu-id="dc9af-110">このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:</span><span class="sxs-lookup"><span data-stu-id="dc9af-110">Before you complete the steps in this topic, verify that the following prerequisites are met:</span></span>

- <span data-ttu-id="dc9af-111">開発環境には **Visual Studio Enterprise Edition** があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-111">You have **Visual Studio Enterprise edition** in a development environment.</span></span> <span data-ttu-id="dc9af-112">負荷テストを作成するには、Enterprise Edition が必要です。</span><span class="sxs-lookup"><span data-stu-id="dc9af-112">Enterprise edition is required to create load tests.</span></span> <span data-ttu-id="dc9af-113">Microsoft Dynamics Lifecycle Services (LCS) を通じてクラウド ホスト環境として開発ボックスを配置する場合は、配置する適切な Visual Studio バージョンを選択してください 。</span><span class="sxs-lookup"><span data-stu-id="dc9af-113">If you're deploying your development box as a cloud-hosted environment through Microsoft Dynamics Lifecycle Services (LCS), be sure to select the appropriate Visual Studio version to deploy.</span></span>
- <span data-ttu-id="dc9af-114">Visual Studio Web パフォーマンスおよび負荷テスト ツールは、[負荷テストコ ンポーネントのインストール](/visualstudio/test/quickstart-create-a-load-test-project#install-the-load-testing-component) の説明に従ってインストールされます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-114">The Visual Studio web performance and load testing tools are installed as described in [Install the load testing component](/visualstudio/test/quickstart-create-a-load-test-project#install-the-load-testing-component).</span></span>
- <span data-ttu-id="dc9af-115">開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-115">You have a tier-2 or higher sandbox environment that has the same release (application version and platform update) as your development environment.</span></span>
- <span data-ttu-id="dc9af-116">[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従って開発環境を構成しました。</span><span class="sxs-lookup"><span data-stu-id="dc9af-116">You've configured your development environment by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>
- <span data-ttu-id="dc9af-117">エンド ツー エンド (E2E) シナリオ用に C\# パフォーマンス テスト クラスが生成され、[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従ってシングルユーザー テストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-117">C\# performance testing classes have been generated for your end-to-end (E2E) scenarios, and you can run a single-user test by following the steps in [Single-user testing with Task recorder and the Performance SDK](single-user-test-perf-sdk.md).</span></span>

## <a name="configure-a-development-environment-for-multi-user-testing"></a><span data-ttu-id="dc9af-118">マルチ ユーザー テストのための開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dc9af-118">Configure a development environment for multi-user testing</span></span>

<span data-ttu-id="dc9af-119">次のコンフィギュレーションは、テスト コントローラーおよびエージェントをローカルにホストするために使用される開発マシンで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-119">The following configurations must be set up on the development machine that is used to locally host the testing controller and agent.</span></span>

> [!NOTE]
> <span data-ttu-id="dc9af-120">Microsoft が管理するすべてのサンドボックスおよびセルフサービス タイプのサンドボックスについて、Microsoft はご使用の環境の証明書を生成し、事前に構成します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-120">For all Microsoft-managed sandboxes and sandboxes of the self-service type, Microsoft will generate the certificate for your environment and preconfigure it.</span></span>

1. <span data-ttu-id="dc9af-121">**TestRoot** という名前の環境変数を作成し、Windows PowerShell で次のコマンドレットを実行して **PerfSDK** フォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-121">Create an environmental variable that is named **TestRoot**, and point it to the **PerfSDK** folder by running the following cmdlet in Windows PowerShell.</span></span>

    ```powershell
    [ENVIRONMENT]::SETENVIRONMENTVARIABLE("TESTROOT", "K:\PERFSDK\PERFSDKLOCALDIRECTORY", "USER")
    ```

    <span data-ttu-id="dc9af-122">変数を検証するには、Windows PowerShell 次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-122">To verify the variable, run the following command in Windows PowerShell.</span></span>

    ```powershell
    [ENVIRONMENT]::GETENVIRONMENTVARIABLE("TESTROOT", "USER") | Write-Host
    ```

2. <span data-ttu-id="dc9af-123">LCS で、ターゲット サンドボックス環境の **環境の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-123">In LCS, open the **Environment details** page for your target sandbox environment.</span></span>

    <span data-ttu-id="dc9af-124">**環境の詳細** ページの **管理** メニューには、次の 2 つの新しいコマンドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-124">On the **Environment details** page, the **Maintain** menu includes two new commands:</span></span>

    - <span data-ttu-id="dc9af-125">RSAT 証明書のダウンロード</span><span class="sxs-lookup"><span data-stu-id="dc9af-125">Download RSAT certificate</span></span>
    - <span data-ttu-id="dc9af-126">RSAT 証明書を再生成する</span><span class="sxs-lookup"><span data-stu-id="dc9af-126">Regenerate RSAT certificate</span></span>

    ![RSAT 証明書のダウンロードと RSAT 証明書の再生成コマンド](rsat/media/rsat-lcs1.png)

3. <span data-ttu-id="dc9af-128">**RSAT 証明書をダウンロード** を選択して、証明書バンドルを ZIP ファイルとして取得します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-128">Select **Download RSAT certificate** to retrieve the certificate bundle as a zip file.</span></span>
4. <span data-ttu-id="dc9af-129">クリアテキストのパスワードが画面に表示されるという警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-129">You're warned that a clear-text password will be shown on screen.</span></span> <span data-ttu-id="dc9af-130">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-130">Select **Yes** to continue.</span></span>
5. <span data-ttu-id="dc9af-131">後で必要になるため、クリアテキストのパスワードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-131">Copy the clear-text password, because you will need it later.</span></span>
6. <span data-ttu-id="dc9af-132">ZIP ファイルをダウンロードした後、解凍します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-132">After the zip file is downloaded, unzip it.</span></span> <span data-ttu-id="dc9af-133">内部には、証明書 (.cer) ファイルと個人情報交換 (.pfx) ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-133">Inside, you should find a certificate (.cer) file and a personal information exchange (.pfx) file.</span></span>
7. <span data-ttu-id="dc9af-134">証明書 (.cer) ファイルをダブルタップ (またはダブルクリック) して開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-134">Double-tap (or double-click) the certificate (.cer) file to open it, and then select **Install**.</span></span> <span data-ttu-id="dc9af-135">この証明書をローカル コンピューターにインストールしてから、**個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-135">Install this certificate on your local machine, and then browse to the **Personal** store.</span></span> <span data-ttu-id="dc9af-136">ローカル コンピューターの場所に対してこの手順を繰り返し、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-136">Repeat this process for the local machine location, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>
8. <span data-ttu-id="dc9af-137">個人情報交換 (.pfx) ファイルをダブルタップ (またはダブルクリック) して開き、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-137">Double-tap (or double-click) the personal information exchange (.pfx) file to open it, and then select **Install**.</span></span> <span data-ttu-id="dc9af-138">この証明書をローカル コンピューターにインストールしてから、手順 5 でコピーしたパスワードを入力して、**個人** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-138">Install this certificate on your local machine, enter the password that you copied in step 5, and then browse to the **Personal** store.</span></span> <span data-ttu-id="dc9af-139">ローカル コンピューターの場所に対してこの手順を繰り返し、手順 5 でコピーしたパスワードを入力して、特定の **信頼済ルート証明機関** ストアを参照します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-139">Repeat this process for the local machine location, enter the password that you copied in step 5, and browse specifically to the **Trusted Root Certification Authorities** store.</span></span>
9. <span data-ttu-id="dc9af-140">証明書ファイルをダブルタップ (またはダブルクリック) して、開きます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-140">Double-tap (or double-click) the certificate file to open it.</span></span> <span data-ttu-id="dc9af-141">**詳細** タブで、**拇印** セクションが見つかるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-141">On the **Details** tab, scroll down until you find the **Thumbprint** section.</span></span> <span data-ttu-id="dc9af-142">**拇印** を選択し、テキスト ボックスに ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-142">Select **Thumbprint**, and copy the ID in the text box.</span></span> <span data-ttu-id="dc9af-143">この拇印を保存し、パフォーマンス SDK に対して **CloudEnvironment.config** 拇印を更新します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-143">Save this thumbprint to update the **CloudEnvironment.config** thumbprint for the Performance SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="dc9af-144">Microsoft は、有効期限が切れる前に証明書を自動的にローテーションします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-144">Microsoft will automatically rotate the certificate before it expires.</span></span> <span data-ttu-id="dc9af-145">その時点で、証明書の新しいバージョンをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-145">At that time, you must download a new version of the certificate.</span></span> <span data-ttu-id="dc9af-146">セルフ サービス環境では、証明書は有効期限に最も近いダウンタイム ウィンドウで 90 日ごとにローテーションされます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-146">For self-service environments, the certificate will be rotated every 90 days, during a downtime window that is closest to the expiry.</span></span> <span data-ttu-id="dc9af-147">ダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-147">Downtime windows include customer-initiated package deployment, and database movement operations that target the environment.</span></span>

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a><span data-ttu-id="dc9af-148">マルチユーザー テスト用の PerfSDKSample ソリューションの準備</span><span class="sxs-lookup"><span data-stu-id="dc9af-148">Prepare the PerfSDKSample solution for multi-user testing</span></span>

<span data-ttu-id="dc9af-149">次の手順に従って、パフォーマンス テスト用のサンプル ソリューションを準備します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-149">Follow these steps to prepare the sample solution for performance testing.</span></span> <span data-ttu-id="dc9af-150">サンプル ソリューションは、開発環境の Performance SDK フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-150">You can find the sample solution in the Performance SDK folder in your development environment.</span></span> <span data-ttu-id="dc9af-151">既定では、フォルダは K:\\PerfSDK\\PerfSDKLocalDirectory です。</span><span class="sxs-lookup"><span data-stu-id="dc9af-151">By default, the folder is at K:\\PerfSDK\\PerfSDKLocalDirectory.</span></span>

1. <span data-ttu-id="dc9af-152">上位のアクセス許可で次のコマンドレットを実行して、以前にインストールした証明書が正しくインストールされていること、および以前に保存した拇印がローカル コンピューターの **個人** ストアにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-152">Run the following cmdlets with elevated permissions to verify that the certificate that you installed earlier is correctly installed, and that the thumbprint that you saved earlier is in the **Personal** store on the local machine.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    <span data-ttu-id="dc9af-153">次の図は、サンプル結果を示します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-153">The following illustration shows a sample result.</span></span> <span data-ttu-id="dc9af-154">以前に保存した拇印がリストにあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-154">Make sure that the thumbprint that you saved earlier is in the list.</span></span>

    ![コマンド プロンプト ウィンドウの拇印](media/perfsdk-multi-user-testing-01.png)

2. <span data-ttu-id="dc9af-156">Performance SDK フォルダーの **CloudEnvironment.config** 構成ファイルを更新し、対象の環境を記述します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-156">Update the **CloudEnvironment.config** configuration file in the Performance SDK folder to describe the targeted environment.</span></span> <span data-ttu-id="dc9af-157">この更新プログラムの一部として、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-157">As part of this update, follow these steps:</span></span>

    1. <span data-ttu-id="dc9af-158">**HostName** と **SOAPHostName** の設定が階層 2 以上のサンドボックス環境と一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-158">Verify that the settings for **HostName** and **SOAPHostName** match your tier-2 or higher sandbox environment.</span></span>
    2. <span data-ttu-id="dc9af-159">**SelfSigningCertateThumbprint** の値として以前に保存した拇印を追加します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-159">Add the thumbprint that you saved earlier as the value for **SelfSigningCertificateThumbprint**.</span></span> <span data-ttu-id="dc9af-160">構成ファイルにエントリがない場合は、次の図に示すように追加できます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-160">If the entry is missing from your configuration file, you can add it as shown in the illustration that follows.</span></span>
    3. <span data-ttu-id="dc9af-161">**UserCount** の設定を更新して、ケースのテスト ユーザーの数と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-161">Update the setting of **UserCount** so that it matches the number of test users in your case.</span></span>
    4. <span data-ttu-id="dc9af-162">**UserFormat** の設定を更新して、テスト ユーザーの名前付け規則と一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-162">Update the setting of **UserFormat** so that it matches your naming convention for test users.</span></span>
    5. <span data-ttu-id="dc9af-163">**AuthenticatorConfigurationCollection** 要素の下の各 **AuthenticatorConfiguration** 要素で、**MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAadAuthenticator** を  **MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator** で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-163">In each **AuthenticatorConfiguration** element under the **AuthenticatorConfigurationCollection** element, replace **MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAadAuthenticator** with **MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator**.</span></span>
    6. <span data-ttu-id="dc9af-164">**AzureActiveDirectoryConfiguration** 要素と **KeyVaultConfigurations** 要素をコメント行にします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-164">Comment out the **AzureActiveDirectoryConfiguration** and **KeyVaultConfigurations** elements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc9af-165">Finance and Operations アプリが 21Vianet に配置されている場合、必ず `NetworkDomain="https://sts.chinacloudapi.cn/"` を **SelfMintingSysUser** および **SelfMintingAdminUser** で指定してください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-165">If your Finance and Operations apps were deployed in 21Vianet, be sure to specify `NetworkDomain="https://sts.chinacloudapi.cn/"` for **SelfMintingSysUser** and **SelfMintingAdminUser**.</span></span>

    <span data-ttu-id="dc9af-166">結果は次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-166">The result should resemble the following example.</span></span>

    ![更新された CloudEnvironment.config ファイル](./media/perfsdk-multi-user-testing-02.png)

3. <span data-ttu-id="dc9af-168">**vsonline.testsettings** ファイルの名前を **local.testsettings** に変更します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-168">Rename the **vsonline.testsettings** file **local.testsettings**.</span></span>
4. <span data-ttu-id="dc9af-169">Visual Studio で **local.testsettings** ファイルを開き、次の手順に従って変更します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-169">Open the **local.testsettings** file in Visual Studio, and modify it by following these steps:</span></span>

    1. <span data-ttu-id="dc9af-170">**テストの設定** ダイアログ ボックスの **一般** タブの **テストの実行場所** フィールド グループで **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-170">In the **Test Settings** dialog box, on the **General** tab, in the **Test run Location** field group, select the **Run tests using local computer or a test controller** option.</span></span>
    2. <span data-ttu-id="dc9af-171">**配置** タブで **配置を有効にする** チェック ボックスを選択し、**ディレクトリの追加** ボタンを使用して **bin\debug** を **配置する追加のファイルやディレクトリ** フィールドに追加します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-171">On the **Deployment** tab, select the **Enable deployment** checkbox, and then use the **Add Directory** button to add the **bin\debug** folder to the **Additional files and directories to deploy** field.</span></span>

        ![[テストの設定] ダイアログ ボックスの [配置] タブ](./media/perfsdk-multi-user-testing-04.png)

    3. <span data-ttu-id="dc9af-173">**ホスト** タブの **32 ビットまたは 64 ビット プロセスでテストを実行** フィールドで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-173">On the **Hosts** tab, in the **Run tests in 32 bits or 64 bits process** field, select **Run test in 64 bits process on 64 bits machine**.</span></span>
    4. <span data-ttu-id="dc9af-174">**適用** を選択して **テストの設定** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-174">Select **Apply**, and then close the **Test Settings** dialog box.</span></span>
    5. <span data-ttu-id="dc9af-175">プロジェクト コンフィギュレーションを開き、**ターゲット フレームワーク** を **.NET Framework 4.6.2** に設定して変更します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-175">Open your project configuration, and modify it by setting **Target Framework** to **.NET Framework 4.6.2**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc9af-176">Microsoft Dynamics 365 アドインを使用してタスク記録から C\# パフォーマンス テストを生成するたびに、ソリューション全体を再度開くのではなく、プロジェクトを Visual Studio に再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="dc9af-176">Whenever you use the Microsoft Dynamics 365 Add-in to generate a C\# performance test from a task recording, it will reload the project in Visual Studio instead of reopening the whole solution.</span></span> <span data-ttu-id="dc9af-177">負荷テストを実行する前に、必ずソリューションを再読み込みして、テスト設定ファイルが表示されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-177">Be sure to reload the solution before you run any load tests, to ensure that the test settings file is visible.</span></span>

## <a name="modify-the-performance-test-sources"></a><span data-ttu-id="dc9af-178">パフォーマンス テスト ソースの変更</span><span class="sxs-lookup"><span data-stu-id="dc9af-178">Modify the performance test sources</span></span>

<span data-ttu-id="dc9af-179">ソリューションで生成された各パフォーマンス テストごとに、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dc9af-179">Follow these steps for each generated performance test in your solution.</span></span>

1. <span data-ttu-id="dc9af-180">**使用** ディレクティブ セクションの上部に、次のステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-180">Add the following statement at the top in the **using** directives section.</span></span>

    ```csharp
    using MS.Dynamics.TestTools.UIHelpers.Core;
    ```

2. <span data-ttu-id="dc9af-181">全体を次の行に置き換えて、**TestSetup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-181">Modify the **TestSetup** method by replacing the whole body with the following lines.</span></span>

    ```csharp
    private DispatchedClient Client;
    private UserContext _userContext;
    private TimerProvider timerProvider;
    [TestInitialize]
    public void TestSetup()
    {
        if (this.TestContext != null)
        {
            timerProvider = new TimerProvider(this.TestContext);
        }
        SetupData();
        Client = new DispatchedClientHelper().GetClient();
        Client.ForceEditMode = false;
        Client.Company = WellKnownCompanyID.USMF.ToString();
        Client.Open();
    }
    ```

3. <span data-ttu-id="dc9af-182">次の例と同様に **TestCleanup** メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-182">Modify the **TestCleanup** method so that it resembles the following example.</span></span>

    ```csharp
    public void TestCleanup()
    {
        Client.Close();
        Client.Dispose();
        Client = Null;
    }
    ```

4. <span data-ttu-id="dc9af-183">ソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-183">Build your solution.</span></span>

## <a name="add-a-test-to-the-load-test-mix"></a><span data-ttu-id="dc9af-184">負荷テスト ミックスにテストの追加</span><span class="sxs-lookup"><span data-stu-id="dc9af-184">Add a test to the load test mix</span></span>

<span data-ttu-id="dc9af-185">次の手順に従って、テスト ミックスにパフォーマンス テストを追加します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-185">Follow these steps to add a performance test to the test mix.</span></span>

1. <span data-ttu-id="dc9af-186">**SampleLoadTest.loadtest** ファイルを開き、**テスト ミックス** ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-186">Open the **SampleLoadTest.loadtest** file, and find the **Test Mix** node.</span></span>
2. <span data-ttu-id="dc9af-187">**テスト ミックス** ノードを選択し、保留 (または右クリック) し、**テスト ミックスの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-187">Select and hold (or right-click) the **Test Mix** node, and then select **Edit Test Mix**.</span></span>
3. <span data-ttu-id="dc9af-188">**テスト ミックスの編集** ダイアログ ボックスで、**追加** を選択してテストをミックスに追加します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-188">In the **Edit Test Mix** dialog box, select **Add** to add your tests to the mix.</span></span>

    ![[テスト ミックスの編集] ダイアログ ボックス](./media/perfsdk-multi-user-testing-06.png)

4. <span data-ttu-id="dc9af-190">**実行設定** ノードで、プロパティを変更し、**実行設定 1** の **タイミング** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-190">In the **Run Settings** node, modify the properties, and update the **Timing** fields for **Run Settings1**.</span></span> <span data-ttu-id="dc9af-191">これらのフィールドは **ウォームアップ期間**、**実行期間**、**クールダウン期間** を含みます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-191">These fields include **Warm-up Duration**, **Run Duration**, and **Cool-down Duration**.</span></span>

    ![タイミング フィールド](./media/perfsdk-multi-user-testing-07.png)

5. <span data-ttu-id="dc9af-193">**シナリオ** ノードで、必ず **負荷パターン** プロパティを更新し、**定数ユーザー数** パラメーターをテストの実行に使用するユーザーの総数に設定してください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-193">In the **Scenarios** node, be sure to update the **Load Pattern** property, and set the **Constant User Count** parameter to the total number of users that you want to use to run the test.</span></span>

    ![定数ユーザー数パラメーター](./media/perfsdk-multi-user-testing-08.png)

## <a name="create-test-users"></a><span data-ttu-id="dc9af-195">新規ユーザーのテスト</span><span class="sxs-lookup"><span data-stu-id="dc9af-195">Create test users</span></span>

<span data-ttu-id="dc9af-196">テスト ユーザーは、ターゲット環境に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-196">Test users must be added to the target environment.</span></span> <span data-ttu-id="dc9af-197">名前付けパターンは **CloudEnvironment.config** 構成ファイルで指定されたパターンと一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-197">The naming pattern must match the pattern that is specified in the **CloudEnvironment.config** configuration file.</span></span> <span data-ttu-id="dc9af-198">Microsoft Dynamics 365 環境でユーザーを手動で作成するか、Performance SDK フォルダーの **MS.Dynamics.Performance.CreateUsers.exe** コンソール アプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc9af-198">You can either manually create the users in a Microsoft Dynamics 365 environment or use the **MS.Dynamics.Performance.CreateUsers.exe** console application in the Performance SDK folder.</span></span>

<span data-ttu-id="dc9af-199">ユーザーを手動で作成する場合は、各ユーザーに **システム管理者** セキュリティ ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc9af-199">If you manually create the users, make sure that the **System Administrator** security role is assigned to each user.</span></span>

<span data-ttu-id="dc9af-200">コンソール アプリケーションを使用してユーザーを作成することをお勧めします。コンソール アプリケーションは構成ファイルを読み取り、適切なサービス エンドポイントを呼び出すためです。</span><span class="sxs-lookup"><span data-stu-id="dc9af-200">We recommend that you use the console application to create the users, because it reads the configuration files and calls the appropriate service endpoints.</span></span>

## <a name="run-multi-user-testing-by-using-a-local-test-controller"></a><span data-ttu-id="dc9af-201">ローカル テスト コントローラーを使用したマルチユーザー テストの実行</span><span class="sxs-lookup"><span data-stu-id="dc9af-201">Run multi-user testing by using a local test controller</span></span>

1. <span data-ttu-id="dc9af-202">Visual Studio プロジェクトで、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-202">In the Visual Studio project, open the **SampleLoadTest.loadtest** file, and select **Run Load Test**.</span></span>
2. <span data-ttu-id="dc9af-203">テスト出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="dc9af-203">Review the test output.</span></span>

    ![テストの出力](./media/perfsdk-multi-user-testing-10.png)

## <a name="troubleshooting"></a><span data-ttu-id="dc9af-205">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="dc9af-205">Troubleshooting</span></span>

<span data-ttu-id="dc9af-206">パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc9af-206">For more information about single-user or multi-user testing that uses the Performance SDK, see [Troubleshooting guide for single-user or multi-user testing with the Performance SDK](troubleshoot-perf-sdk-user-testing.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
