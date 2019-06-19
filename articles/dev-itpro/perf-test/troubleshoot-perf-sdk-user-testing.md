---
title: パフォーマンスSDKを使用した、シングルユーザーまたはマルチユーザーテストのためのトラブルシューティングガイド
description: このトピックでは、パフォーマンスSDKを使用したシングルユーザーまたはマルチユーザーのテスト中に発生する可能性のある一般的な問題のトラブルシューティングについて説明します。
author: hasaid
manager: AnnBe
ms.date: 05/17/2019
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
ms.openlocfilehash: bb2c43ea125aa231458d791c6560e3bf33cfcb7d
ms.sourcegitcommit: c576b81dc3c93c09fb08fb0ba0c19f417360c5ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620471"
---
# <a name="troubleshooting-guide-for-single-user-or-multi-user-testing-with-the-performance-sdk"></a><span data-ttu-id="eca5e-103">パフォーマンスSDKを使用した、シングルユーザーまたはマルチユーザーテストのためのトラブルシューティングガイド</span><span class="sxs-lookup"><span data-stu-id="eca5e-103">Troubleshooting guide for single-user or multi-user testing with the Performance SDK</span></span>

[!include [banner](../includes/banner.md)]

## <a name="no-client-was-opened-in-the-time-out-period"></a><span data-ttu-id="eca5e-104">タイムアウト期間中クライアントが開かれていません</span><span class="sxs-lookup"><span data-stu-id="eca5e-104">No client was opened in the time-out period</span></span>

<span data-ttu-id="eca5e-105">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-105">This issue affects only single-user tests.</span></span> <span data-ttu-id="eca5e-106">テストの過程で、Webクライアントが起動するが、Webサイトが表示されません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-106">When the test is running, a web client is opened, but a website is never loaded.</span></span> <span data-ttu-id="eca5e-107">webクライアントには何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-107">Instead, there is an empty web client that has a white background.</span></span> <span data-ttu-id="eca5e-108">次のメッセージがページの上部に表示されます。「これはWebDriverサーバーの既定のスタートページです」。</span><span class="sxs-lookup"><span data-stu-id="eca5e-108">The following message appears at the top of the page, "This is the initial start page for the WebDriver server."</span></span> <span data-ttu-id="eca5e-109">テストは最終的にタイム アウトの後に失敗し、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-109">The test eventually times out and fails, and an error message is shown.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-110">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-110">Error example</span></span>

> <span data-ttu-id="eca5e-111">初期化メソッド \<テストクラス名\> TestSetupが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-111">Initialization method \<Test class name\>.TestSetup threw an exception.</span></span> <span data-ttu-id="eca5e-112">TimeoutException: TimeoutException: タイムアウト時間内にクライアントが開かれませんでした。</span><span class="sxs-lookup"><span data-stu-id="eca5e-112">System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-113">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-113">Solution</span></span>

<span data-ttu-id="eca5e-114">[パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト](multi-user-testing-local-test-controller.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eca5e-114">See [Multi-user testing with the Performance SDK and a local test controller](multi-user-testing-local-test-controller.md).</span></span> <span data-ttu-id="eca5e-115">リンク先セクションでは、このタイプのテストにおいて正しい証明書を作成する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="eca5e-115">That topic explains how to create a correct certificate for this type of test.</span></span> <span data-ttu-id="eca5e-116">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-116">It also explains how to add the thumbprint of the certificate to the wif.config file.</span></span>

## <a name="zoom-factor"></a><span data-ttu-id="eca5e-117">ズーム係数</span><span class="sxs-lookup"><span data-stu-id="eca5e-117">Zoom factor</span></span>

<span data-ttu-id="eca5e-118">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-118">This issue affects only single-user tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-119">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-119">Error example</span></span>

> <span data-ttu-id="eca5e-120">初期化メソッド \<テストクラス名\> TestSetupが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-120">Initialization method \<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="eca5e-121">System.InvalidOperationException: System.InvalidOperationException: Internet Explorerで予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-121">System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer.</span></span> <span data-ttu-id="eca5e-122">ブラウザーのズームレベルが200% に設定されていました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-122">Browser zoom level was set to 200%.</span></span> <span data-ttu-id="eca5e-123">ズームレベルは100%に設定してください。</span><span class="sxs-lookup"><span data-stu-id="eca5e-123">It should be set to 100% (NoSuchDriver).</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-124">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-124">Solution</span></span>

<span data-ttu-id="eca5e-125">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-125">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="eca5e-126">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="eca5e-126">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="eca5e-127">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="eca5e-127">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="eca5e-128">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="eca5e-128">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>

<span data-ttu-id="eca5e-129">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-129">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="eca5e-130">このフィールドは、 Microsoft Windows の **表示設定** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-130">This field is available in **Display settings** in Microsoft Windows.</span></span>

<span data-ttu-id="eca5e-131">これらの手順が機能しない場合は、RDP セッションを開始する前に Internet Explorer で既定のズーム レベルが 100 % になるよう、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="eca5e-131">If those steps don't work, change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

## <a name="certificate-thumbprint-errors"></a><span data-ttu-id="eca5e-132">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="eca5e-132">Certificate thumbprint errors</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-133">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-133">Error example</span></span>

> <span data-ttu-id="eca5e-134">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup\*\* が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-134">Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup\*\* threw an exception.</span></span> <span data-ttu-id="eca5e-135">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-135">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-136"> --\> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 拇印によるトークン作成用の証明書の検索に失敗しました: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</span><span class="sxs-lookup"><span data-stu-id="eca5e-136"> --\> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-137">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-137">Solution</span></span>

<span data-ttu-id="eca5e-138">以下に挙げるいずれかの理由でエラー メッセージが表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-138">You might receive the error message for one of the following reasons:</span></span>

- <span data-ttu-id="eca5e-139">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eca5e-139">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="eca5e-140">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-140">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="eca5e-141">たとえば、 <https://r12a.github.io/apps/conversion/>にて提供されている Unicode コンバーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-141">For example, you can use the Unicode converter that is available at <https://r12a.github.io/apps/conversion/>.</span></span>

    <span data-ttu-id="eca5e-142">[![ユニコード変換](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-142">[![Unicode conversion](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</span></span>

- <span data-ttu-id="eca5e-143">アプリケーション オブジェクト サーバー マシン (AOS) に証明書が 正しくインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-143">The certificate wasn't installed on the Application Object Server (AOS) machine.</span></span> <span data-ttu-id="eca5e-144">以下の Microsoft Windows PowerShell スクリプトを実行し、認証が必要となる証明書をAOSマシン内で検索します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-144">To verify that the certificate can be found on the AOS machine, run the following Microsoft Windows PowerShell script.</span></span>

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    <span data-ttu-id="eca5e-145">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書をインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-145">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate isn't installed.</span></span> <span data-ttu-id="eca5e-146">この問題を修正するには、すべてのAOSマシンに .cerファイルをコピーしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="eca5e-146">To fix the issue, copy and install a .cer file on all AOS machines.</span></span>

- <span data-ttu-id="eca5e-147">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-147">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="eca5e-148">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-148">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>

    <span data-ttu-id="eca5e-149">[![.cmd file のパスワード](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-149">[![Password in the .cmd file](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</span></span>

## <a name="no-endpoint-is-listening"></a><span data-ttu-id="eca5e-150">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="eca5e-150">No endpoint is listening</span></span>

<span data-ttu-id="eca5e-151">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-151">This issue can occur when you run single-user or multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-152">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-152">Error example</span></span>

<span data-ttu-id="eca5e-153">テスト、またはユーザー作成処理が失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-153">The tests fail, or the user creation process fails, and the following error message is shown:</span></span>

> <span data-ttu-id="eca5e-154">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-154">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-155"> ---\>System.ServiceModel.EndpointNotFoundException: \\\<web address\> にてメッセージを受領することができるエンドポイント リスニングがありません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-155"> ---\> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at \\\<web address\> that could accept the message.</span></span> <span data-ttu-id="eca5e-156">この事象は、正しくないアドレスまたは SOAP アクションによって引き起こされることがあります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-156">This is often caused by an incorrect address or SOAP action.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-157">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-157">Solution</span></span>

<span data-ttu-id="eca5e-158">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-158">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>

<span data-ttu-id="eca5e-159">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-159">In the CloudEnvironment.Config file, review the values that are specified by the following keys:</span></span>

- <span data-ttu-id="eca5e-160">\\\<ExecutionConfigurations Key="ホスト名" Value="\<ホストのWebアドレス\>" /\></span><span class="sxs-lookup"><span data-stu-id="eca5e-160">\\\<ExecutionConfigurations Key="HostName" Value="\<web address of host\>" /\></span></span>
- <span data-ttu-id="eca5e-161">\\\<ExecutionConfigurations Key="SoapHostName" Value="\<SOAPのWebアドレス\>" /\></span><span class="sxs-lookup"><span data-stu-id="eca5e-161">\\\<ExecutionConfigurations Key="SoapHostName" Value="\<web address of SOAP\>" /\></span></span>

<span data-ttu-id="eca5e-162">これらのキーに指定する Web アドレスは、現在テストを実施している環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-162">The web addresses that are specified by these keys must be in the environment that you're testing.</span></span> <span data-ttu-id="eca5e-163">開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-163">In a web browser on your developer machine, make sure that you can open the web address that is specified by the **HostName** key.</span></span>

<span data-ttu-id="eca5e-164">オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-164">For online load tests, the environment that is specified by the **HostName** key in the CloudEnvironment.Config file must be publicly accessible from any machine.</span></span> <span data-ttu-id="eca5e-165">したがって、ワンボックス環境をテストする必要がある場合、Microsoft Visual Studio Online Online を使用して負荷テストを実行することはできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。</span><span class="sxs-lookup"><span data-stu-id="eca5e-165">Therefore, if you must test a one-box environment, you won't be able to run the load test by using Microsoft Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</span></span>

## <a name="users-cant-be-enumerated"></a><span data-ttu-id="eca5e-166">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="eca5e-166">Users can't be enumerated</span></span>

<span data-ttu-id="eca5e-167">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-167">This issue can occur when you run multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-168">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-168">Error example</span></span>

> <span data-ttu-id="eca5e-169">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-169">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-170"> ---\> System.InvalidOperationException: AX のユーザーを列挙することができませんでした ---\> System.ServiceModel.FaultException'1\[System.ComponentModel.Win32Exception\]: 禁止されています</span><span class="sxs-lookup"><span data-stu-id="eca5e-170"> ---\> System.InvalidOperationException: Could not enumerate AX users ---\> System.ServiceModel.FaultException'1\[System.ComponentModel.Win32Exception\]: Forbidden</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-171">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-171">Solution</span></span>

<span data-ttu-id="eca5e-172">2 つのシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-172">Two scenarios can cause this error:</span></span>

- <span data-ttu-id="eca5e-173">CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーに、システム管理者ロールが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-173">The System Administrator role isn't assigned to the user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span> <span data-ttu-id="eca5e-174">適切なユーザーが指定されていることを検証するには、エンドポイントにサインインし、ユーザーのロールを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-174">To verify that you've specified the correct user, sign in to the endpoint, and view the user's roles.</span></span>

    <span data-ttu-id="eca5e-175">[![ユーザーページ](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-175">[![Users page](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</span></span>

- <span data-ttu-id="eca5e-176">CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーは、 `https://sts.windows-ppe.net/` または `https://sts.windows.net/` 以外のプロバイダーを持っています。</span><span class="sxs-lookup"><span data-stu-id="eca5e-176">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file has a provider other than `https://sts.windows-ppe.net/` or `https://sts.windows.net/`.</span></span> <span data-ttu-id="eca5e-177">場合によっては、管理者ユーザーの**プロバイダ**フィールドに会社固有のドメインを含めます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-177">Sometimes, a company-specific domain is included in the **Provider** field for the admin user.</span></span> 

<span data-ttu-id="eca5e-178">Microsoft Dynamics 365 for Finance and Operations にてこの問題を回避するには、任意の名前と電子メール アドレスを持つユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-178">To work around this issue, in Microsoft Dynamics 365 for Finance and Operations, create a user who has any name and email address.</span></span> <span data-ttu-id="eca5e-179">**システム管理者** ロールを新しいユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-179">Assign the **System Administrator** role to the new user.</span></span> <span data-ttu-id="eca5e-180">ユーザーを実在の Microsoft Azure Active Directory (Azure AD) ユーザーにリンクする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-180">You don't have to link the user to a real Microsoft Azure Active Directory (Azure AD) user.</span></span> <span data-ttu-id="eca5e-181">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-181">Specify this new admin user as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span>

## <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a><span data-ttu-id="eca5e-182">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="eca5e-182">The HTTP request was forbidden with client authentication scheme 'Anonymous'</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-183">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-183">Error example</span></span>

> <span data-ttu-id="eca5e-184">初期化メソッド \<テストクラス名\> TestSetupが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-184">Initialization method \<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="eca5e-185">System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: クライアント認証スキーム'Anonymous'でHTTP要求が禁止されました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-185">System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'.</span></span><span data-ttu-id="eca5e-186"> ---\> System.Net.WebException: リモートサーバーからエラーが返されました: (403) 許可されていません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-186"> ---\> System.Net.WebException: The remote server returned an error: (403) Forbidden.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-187">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-187">Solution</span></span>

<span data-ttu-id="eca5e-188">既知の 2 つのシナリオでは、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-188">Two known scenarios can cause this error:</span></span>

- <span data-ttu-id="eca5e-189">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-189">The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</span></span> <span data-ttu-id="eca5e-190">例えば、CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスが正しくフォーマットされません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-190">For example, if the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</span></span> <span data-ttu-id="eca5e-191">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-191">If these users are used to run the tests, the tests will generate the forbidden request error.</span></span> <span data-ttu-id="eca5e-192">このシナリオがエラーの原因であることを確認するには、Finance and Operations のユーザーを表示します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-192">You can verify that this scenario is causing the error by viewing the users in Finance and Operations.</span></span> <span data-ttu-id="eca5e-193">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-193">The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</span></span>

    <span data-ttu-id="eca5e-194">[![誤りのあるユーザーの電子メールアドレスの一覧](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-194">[![List of incorrect user email addresses](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</span></span>

    <span data-ttu-id="eca5e-195">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-195">To resolve the issue, delete the test users who have incorrectly formatted email addresses.</span></span> <span data-ttu-id="eca5e-196">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を特定します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-196">Rerun the CreateUsers script, and specify the user count and company.</span></span>

- <span data-ttu-id="eca5e-197">CloudEnvironment.Config ファイルの **UserCount** フィールドで指定しているユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えています。</span><span class="sxs-lookup"><span data-stu-id="eca5e-197">The number of users that you specify in the **UserCount** field in the CloudEnvironment.Config file exceeds the number of test users that you created by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="eca5e-198">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-198">Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</span></span>

    <span data-ttu-id="eca5e-199">[![CloudEnvironment.config ファイル](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-199">[![CloudEnvironment.Config file](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</span></span>

## <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="eca5e-200">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-200">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="eca5e-201">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成している場合、AOSマシンが開発用のマシンと異なる場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-201">This issue can occur when you run multi-user tests, when you create users by using MS.Dynamics.Performance.CreateUsers.exe, when the AOS machine differs from the developer machine.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-202">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-202">Error example</span></span>

> <span data-ttu-id="eca5e-203">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-203">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-204"> ---\> System.ServiceModel.Security.MessageSecurityException: セキュリティで保護されていない、または正しく保護されていない障害を受信しました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-204"> ---\> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party.</span></span> <span data-ttu-id="eca5e-205">障害コードと詳細については、FaultException 内部を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eca5e-205">See the inner FaultException for the fault code and detail.</span></span><span data-ttu-id="eca5e-206"> ---\> System.ServiceModel.FaultException: メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-206"> ---\> System.ServiceModel.FaultException: At least one security token in the message could not be validated.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-207">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-207">Solution</span></span>

<span data-ttu-id="eca5e-208">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-208">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="eca5e-209">2 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-209">There are two possible causes:</span></span>

- <span data-ttu-id="eca5e-210">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-210">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="eca5e-211">この問題を修正するには、AOSマシンに .cerファイルをコピーしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="eca5e-211">To fix the issue, copy a .cer file to the AOS machine, and install it.</span></span>
- <span data-ttu-id="eca5e-212">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="eca5e-212">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="eca5e-213">この問題を修正するには、wifファイルに証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-213">To fix the issue, add the certificate to the wif.config file.</span></span> <span data-ttu-id="eca5e-214">Wifファイルを更新した後に、必ずMicrosoft インターネット インフォメーション サービス (IIS) を再起動してください。</span><span class="sxs-lookup"><span data-stu-id="eca5e-214">Be sure to restart Microsoft Internet Information Services (IIS) after you change the wif.config file.</span></span>

## <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="eca5e-215">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="eca5e-215">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="eca5e-216">この問題は、通常、負荷 テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-216">This issue usually occurs when you run load tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-217">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-217">Error example</span></span>

> <span data-ttu-id="eca5e-218">\<テストクラス名\> TestSetupが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-218">\<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="eca5e-219">InvalidOperationException: InvalidOperationException: ServiceModelクライアント構成セクションに名前'ClientCommunicationManager'および契約'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager'を持つエンドポイント要素が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="eca5e-219">System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section.</span></span> <span data-ttu-id="eca5e-220">これは、アプリケーションに対応する構成ファイルが見つからなかったか、またはこの名前と一致するエンドポイント要素がクライアント要素にて見つからないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="eca5e-220">This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element..</span></span> <span data-ttu-id="eca5e-221">SSystem.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors にて (ServiceEndpoint serviceEndpoint, String configurationName)</span><span class="sxs-lookup"><span data-stu-id="eca5e-221">at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-222">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-222">Solution</span></span>

<span data-ttu-id="eca5e-223">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-223">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="eca5e-224">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-224">Verify that the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="eca5e-225">\<solution path\>\\TestResults\\\<your test run\>\\Out</span><span class="sxs-lookup"><span data-stu-id="eca5e-225">\<solution path\>\\TestResults\\\<your test run\>\\Out</span></span>

<span data-ttu-id="eca5e-226">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-226">If the file is missing, add it to the deployment items in the test settings.</span></span>

<span data-ttu-id="eca5e-227">非常に似た名前を持つ 2 つのファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-227">There are two files that have very similar names.</span></span> <span data-ttu-id="eca5e-228">一方は名前が \*.dll で終わるファイルで、もう一方は名前が \*.dll.configで終わるファイルです。 \*.dll.configファイルはテスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-228">The name of one file ends in \*.dll, and the name of the other file ends in \*.dll.config. The \*.dll.config file must be in the deployment items in the test settings.</span></span>

## <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="eca5e-229">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="eca5e-229">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="eca5e-230">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-230">This issue usually occurs only when you run load tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-231">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-231">Error example</span></span>

> <span data-ttu-id="eca5e-232">初期化メソッド \\\<Test class name\>. TestSetupが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-232">Initialization method \\\<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="eca5e-233">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-233">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-234"> ---\> MS.Dynamics.TestTools.TestLogging.EvaluateException: アサートに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-234"> ---\> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed.</span></span> <span data-ttu-id="eca5e-235">DateTime="10/13/2017 14:42:55" "'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-235">DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-236">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-236">Solution</span></span>

<span data-ttu-id="eca5e-237">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-237">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="eca5e-238">一般的に、この問題は負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-238">It typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="eca5e-239">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-239">Verify that the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="eca5e-240">\<solution path\>\\TestResults\\\<your test run\>\\Out</span><span class="sxs-lookup"><span data-stu-id="eca5e-240">\<solution path\>\\TestResults\\\<your test run\>\\Out</span></span>

<span data-ttu-id="eca5e-241">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-241">If the file is missing, add it to the deployment items in the test settings.</span></span>

<span data-ttu-id="eca5e-242">[![テスト設定 ダイアログ ボックスの 配置 タブ](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-242">[![Deployment items in the Test Settings dialog box](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</span></span>

## <a name="interactiveclientid-was-not-specified-in-the-settings"></a><span data-ttu-id="eca5e-243">InteractiveClientId が設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-243">InteractiveClientId was not specified in the settings</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-244">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-244">Error example</span></span>

> <span data-ttu-id="eca5e-245">'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-245">The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.</span></span><span data-ttu-id="eca5e-246"> ---\> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientIdが設定で指定されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="eca5e-246"> ---\> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-247">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-247">Solution</span></span>

<span data-ttu-id="eca5e-248">この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-248">This issue occurs when the **SelfSigningCertificateThumbprint** field is left blank in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="eca5e-249">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-249">In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</span></span>

```
\<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

## <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="eca5e-250">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="eca5e-250">The remote host forcibly closed an existing connection</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-251">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-251">Error example</span></span>

> <span data-ttu-id="eca5e-252">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-252">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-253"> ---\> System.ServiceModel.CommunicationException: \\\<Host name\>/Services/AxUserManagement/Service.svc/ws2007FedHttp.にHTTP要求をした際にエラーが発生しました</span><span class="sxs-lookup"><span data-stu-id="eca5e-253"> ---\> System.ServiceModel.CommunicationException: An error occurred while making the HTTP request to \\\<Host name\>/Services/AxUserManagement/Service.svc/ws2007FedHttp.</span></span> <span data-ttu-id="eca5e-254">HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-254">This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case.</span></span> <span data-ttu-id="eca5e-255">これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="eca5e-255">This could also be caused by a mismatch of the security binding between the client and the server.</span></span><span data-ttu-id="eca5e-256"> ---\> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-256"> ---\> System.Net.WebException: The underlying connection was closed: An unexpected error occurred on a send.</span></span><span data-ttu-id="eca5e-257"> ---\> System.IO.IOException: 転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-257"> ---\> System.IO.IOException: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.</span></span><span data-ttu-id="eca5e-258"> ---\> System.Net.Sockets.SocketException: 既存の接続がリモートホストによって強制的に切断されました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-258"> ---\> System.Net.Sockets.SocketException: An existing connection was forcibly closed by the remote host.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-259">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-259">Solution</span></span>

<span data-ttu-id="eca5e-260">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-260">Run the following Windows PowerShell script on the development machine.</span></span>

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

## <a name="service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="eca5e-261">コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-261">Service w3svc was not found on computer</span></span>

<span data-ttu-id="eca5e-262">このエラーは Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-262">This error occurs only when you run load tests by using Visual Studio Online.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-263">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-263">Error example</span></span>

> <span data-ttu-id="eca5e-264">テストメソッド MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend が例外をスローしました。System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement'のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-264">Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-265"> ---\> System.InvalidOperationException: コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-265"> ---\> System.InvalidOperationException: Service w3svc was not found on computer '.'.</span></span><span data-ttu-id="eca5e-266"> ---\> System.ComponentModel.Win32Exception: 指定されたサービスは、インストールされたサービスに存在しません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-266"> ---\> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-267">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-267">Solution</span></span>

<span data-ttu-id="eca5e-268">この問題を解決する修正プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="eca5e-268">A hotfix is available that resolves this issue.</span></span> <span data-ttu-id="eca5e-269">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="eca5e-269">The Microsoft Knowledge Base (KB) number is 4095640.</span></span>

## <a name="the-file-iedriverserverexe-does-not-exist"></a><span data-ttu-id="eca5e-270">The file IEDriverServer.exe ファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-270">The file IEDriverServer.exe does not exist</span></span>

<span data-ttu-id="eca5e-271">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-271">This issue affects only single-user tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-272">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-272">Error example</span></span>

> <span data-ttu-id="eca5e-273">ファイル K:\\perfSDK\\PerfSDKLocalDirectory\\SampleProject\\TestResults\\Admin501201994c\_devae648d1909-1 2018-06-25 03\_40\_51\\Out\\Common\\External\\Selenium\\IEDriverServer.exe が存在しません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-273">The file K:\\perfSDK\\PerfSDKLocalDirectory\\SampleProject\\TestResults\\Admin501201994c\_devae648d1909-1 2018-06-25 03\_40\_51\\Out\\Common\\External\\Selenium\\IEDriverServer.exe does not exist.</span></span> <span data-ttu-id="eca5e-274">ドライバーは、 `http://selenium-release.storage.googleapis.com/index.html`にてダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-274">The driver can be downloaded at `http://selenium-release.storage.googleapis.com/index.html`.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-275">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-275">Solution</span></span>

<span data-ttu-id="eca5e-276">**\<ご利用の\_PerfSDK\_フォルダ\>** 配下の **Common\\External\\Selenium** フォルダを **\<ご利用の\_PerfSDK\_Folder>\\SampleProject\\ PerfSDKSample\\bin\\Debug** フォルダにコピーします。</span><span class="sxs-lookup"><span data-stu-id="eca5e-276">Copy the **Common\\External\\Selenium** folder under **\<Your\_PerfSDK\_Folder\>** to the **\<Your\_PerfSDK\_Folder>\\SampleProject\\ PerfSDKSample\\bin\\Debug** folder.</span></span>

## <a name="failed-finding-the-certificate-for-minting-tokens-by-thumbprint-your-certificate-thumbprint"></a><span data-ttu-id="eca5e-277">拇印によるトークン作成用の証明書の検索に失敗しました \<ご利用の証明書の拇印\></span><span class="sxs-lookup"><span data-stu-id="eca5e-277">Failed finding the certificate for minting tokens by thumbprint: \<your certificate thumbprint\></span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-278">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-278">Error example</span></span>

<span data-ttu-id="eca5e-279">[![エラーメッセージとエラースタックの追跡](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-279">[![Error message and error stack trace](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-280">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-280">Solution</span></span>

<span data-ttu-id="eca5e-281">生成された証明書は、サンドボックス環境内の各AOSマシンにインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="eca5e-281">Make sure that you install the generated certificate on each AOS machine in your sandbox environment.</span></span>

## <a name="the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a><span data-ttu-id="eca5e-282">実行しようとしているアクションには、 Visual Studio チームサービスへの接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="eca5e-282">The action you are trying to perform requires a connection to Visual Studio Team Services</span></span>

<span data-ttu-id="eca5e-283">この問題はマルチ ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-283">This issue affects only multi-user tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-284">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-284">Error example</span></span>

<span data-ttu-id="eca5e-285">[![エラーメッセージの詳細](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-285">[![Error message details](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-286">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-286">Solution</span></span>

<span data-ttu-id="eca5e-287">Azure DevOps に接続するときは、 **dev.azure.com/\<Azure\_DevOps\_Account\>** ではなく、古いURI形式 (**\<Azure\_DevOps\_Account\>.visualstudio.com**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-287">When you connect to Azure DevOps, use the old URI format (**\<Azure\_DevOps\_Account\>.visualstudio.com**) instead of **dev.azure.com/\<Azure\_DevOps\_Account\>**.</span></span> <span data-ttu-id="eca5e-288">古いURIを使用して Azure DevOps を開き、 **Visual Studioで開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-288">Additionally, open Azure DevOps by using the old URI, and then select **Open in Visual Studio**.</span></span>

## <a name="could-not-load-file-or-assembly-aoskerneldll-or-one-of-its-dependencies"></a><span data-ttu-id="eca5e-289">ファイルまたはアセンブリ 'aoskernel.dll' 、あるいは依存関係を読み込みできませんでした</span><span class="sxs-lookup"><span data-stu-id="eca5e-289">Could not load file or assembly 'aoskernel.dll' or one of its dependencies</span></span>

<span data-ttu-id="eca5e-290">このエラーはマルチ ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="eca5e-290">This error affects only multi-user tests.</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-291">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-291">Error example</span></span>

<span data-ttu-id="eca5e-292">[![エラーメッセージとエラースタックの追跡,デバッグの追跡](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-292">[![Error message, error stack trace, and debug trace](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-293">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-293">Solution</span></span>

<span data-ttu-id="eca5e-294">プラットフォーム更新プログラム20 またはそれ以降が稼働している環境で、Open Database Connectivity (ODBC) ドライバ17が使用されていることを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="eca5e-294">Make sure that you're using Open Database Connectivity (ODBC) Driver 17 in an environment that has Platform update 20 or later.</span></span>

## <a name="azureactivedirectoryconfiguration-node-is-missing-in-cloudenvironmentconfig"></a><span data-ttu-id="eca5e-295">CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-295">AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-296">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-296">Error example</span></span>

> <span data-ttu-id="eca5e-297">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-297">Initialization method MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup threw exception.</span></span> <span data-ttu-id="eca5e-298">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-298">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="eca5e-299"> ---\> System.Reflection.TargetInvocationException: 呼び出しのターゲットによって例外がスローされました。</span><span class="sxs-lookup"><span data-stu-id="eca5e-299"> ---\> System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation.</span></span><span data-ttu-id="eca5e-300"> ---\> System.MissingFieldException: CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-300"> ---\> System.MissingFieldException: AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config.</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-301">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-301">Solution</span></span>

<span data-ttu-id="eca5e-302">**"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"** のすべてのインスタンスを、CloudEnvironment.config ファイルの **AuthenticatorConfigurationCollection** セクションにある **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"** で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="eca5e-302">Replace all instances of **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"** with **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"** in the **AuthenticatorConfigurationCollection** section of the CloudEnvironment.config file.</span></span>

## <a name="multiple-warning-messages-before-and-after-multi-user-testing-that-uses-azure-devops"></a><span data-ttu-id="eca5e-303">Azure DevOpsを使用したマルチユーザーテストの開始前と後に複数の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="eca5e-303">Multiple warning messages before and after multi-user testing that uses Azure DevOps</span></span>

### <a name="error-example"></a><span data-ttu-id="eca5e-304">エラーの例</span><span class="sxs-lookup"><span data-stu-id="eca5e-304">Error example</span></span>

<span data-ttu-id="eca5e-305">[![負荷テストステータスの例](./media/troubleshoot-perf-sdk-10.jpg)](./media/troubleshoot-perf-sdk-10.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-305">[![Sample load test status](./media/troubleshoot-perf-sdk-10.jpg)](./media/troubleshoot-perf-sdk-10.jpg)</span></span>

<span data-ttu-id="eca5e-306">[![負荷テスト結果の例](./media/troubleshoot-perf-sdk-11.jpg)](./media/troubleshoot-perf-sdk-11.jpg)</span><span class="sxs-lookup"><span data-stu-id="eca5e-306">[![Sample load test output](./media/troubleshoot-perf-sdk-11.jpg)](./media/troubleshoot-perf-sdk-11.jpg)</span></span>

### <a name="solution"></a><span data-ttu-id="eca5e-307">ソリューション</span><span class="sxs-lookup"><span data-stu-id="eca5e-307">Solution</span></span>

<span data-ttu-id="eca5e-308">影響はありません。メッセージを無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="eca5e-308">There is no impact, and the messages can be ignored.</span></span>
