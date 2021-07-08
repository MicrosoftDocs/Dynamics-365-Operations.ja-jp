---
title: パフォーマンス SDK を使用したテストのトラブルシューティング ガイド
description: このトピックでは、パフォーマンス SDK を使用したシングル ユーザーまたはマルチ ユーザーのテスト中に発生する一般的な問題のトラブルシューティングについて説明します。
author: hasaid
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 076b899abadd8de64e9dfc672793f1f03791f772
ms.sourcegitcommit: 55ca275705a624d446d2abb60b5d676b86fe7240
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2021
ms.locfileid: "6306794"
---
# <a name="troubleshooting-guide-for-testing-with-the-performance-sdk"></a><span data-ttu-id="25d8f-103">パフォーマンス SDK を使用したテストのトラブルシューティング ガイド</span><span class="sxs-lookup"><span data-stu-id="25d8f-103">Troubleshooting guide for testing with the Performance SDK</span></span>

[!include [banner](../includes/banner.md)]

## <a name="no-client-was-opened-in-the-time-out-period"></a><span data-ttu-id="25d8f-104">タイムアウト期間中クライアントが開かれていません</span><span class="sxs-lookup"><span data-stu-id="25d8f-104">No client was opened in the time-out period</span></span>

<span data-ttu-id="25d8f-105">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-105">This issue affects only single-user tests.</span></span> <span data-ttu-id="25d8f-106">テストの過程で、Webクライアントが起動するが、Webサイトが表示されません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-106">When the test is running, a web client is opened, but a website is never loaded.</span></span> <span data-ttu-id="25d8f-107">webクライアントには何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-107">Instead, there is an empty web client that has a white background.</span></span> <span data-ttu-id="25d8f-108">次のメッセージがページの上部に表示されます。「これはWebDriverサーバーの既定のスタートページです」。</span><span class="sxs-lookup"><span data-stu-id="25d8f-108">The following message appears at the top of the page, "This is the initial start page for the WebDriver server."</span></span> <span data-ttu-id="25d8f-109">テストは最終的にタイム アウトの後に失敗し、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-109">The test eventually times out and fails, and an error message is shown.</span></span>

### <a name="error---no-client-was-opened-in-the-time-out-period"></a><span data-ttu-id="25d8f-110">エラー - タイムアウト時間内にクライアントが開かれませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-110">Error - No client was opened in the time-out period</span></span>

> <span data-ttu-id="25d8f-111">初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-111">Initialization method \<Test class name\>.TestSetup threw an exception.</span></span> <span data-ttu-id="25d8f-112">TimeoutException: TimeoutException: タイムアウト時間内にクライアントが開かれませんでした。</span><span class="sxs-lookup"><span data-stu-id="25d8f-112">System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.</span></span>

### <a name="solution"></a><span data-ttu-id="25d8f-113">ソリューション</span><span class="sxs-lookup"><span data-stu-id="25d8f-113">Solution</span></span>

<span data-ttu-id="25d8f-114">[パフォーマンス SDK を使用したマルチユーザー テスト](perfsdk-multi-user-testing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-114">See [Multi-user testing using the Performance SDK](perfsdk-multi-user-testing.md).</span></span> <span data-ttu-id="25d8f-115">リンク先セクションでは、このタイプのテストにおいて正しい証明書を作成する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="25d8f-115">That topic explains how to create a correct certificate for this type of test.</span></span> <span data-ttu-id="25d8f-116">証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-116">It also explains how to add the thumbprint of the certificate to the wif.config file.</span></span>

## <a name="zoom-factor"></a><span data-ttu-id="25d8f-117">拡大率</span><span class="sxs-lookup"><span data-stu-id="25d8f-117">Zoom factor</span></span>

<span data-ttu-id="25d8f-118">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-118">This issue affects only single-user tests.</span></span>

### <a name="error---zoom-factor"></a><span data-ttu-id="25d8f-119">エラー - ズーム係数</span><span class="sxs-lookup"><span data-stu-id="25d8f-119">Error - Zoom factor</span></span>

> <span data-ttu-id="25d8f-120">初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-120">Initialization method \<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="25d8f-121">System.InvalidOperationException: System.InvalidOperationException: Internet Explorerで予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-121">System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer.</span></span> <span data-ttu-id="25d8f-122">ブラウザーのズームレベルが200% に設定されていました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-122">Browser zoom level was set to 200%.</span></span> <span data-ttu-id="25d8f-123">ズームレベルは100%に設定してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-123">It should be set to 100% (NoSuchDriver).</span></span>

### <a name="solution---zoom-factor"></a><span data-ttu-id="25d8f-124">ソリューション - ズーム係数</span><span class="sxs-lookup"><span data-stu-id="25d8f-124">Solution - Zoom factor</span></span>

<span data-ttu-id="25d8f-125">Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-125">In Internet Explorer, you can change the zoom factor to 100 percent by changing the following registry keys:</span></span>

- <span data-ttu-id="25d8f-126">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span><span class="sxs-lookup"><span data-stu-id="25d8f-126">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0</span></span>
- <span data-ttu-id="25d8f-127">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span><span class="sxs-lookup"><span data-stu-id="25d8f-127">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0</span></span>
- <span data-ttu-id="25d8f-128">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span><span class="sxs-lookup"><span data-stu-id="25d8f-128">Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000</span></span>

<span data-ttu-id="25d8f-129">使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-129">Depending on the version of the local machine that is used, before you start the Remote Desktop Protocol (RDP) session, you might have to select **Change the size of text, apps and other items**.</span></span> <span data-ttu-id="25d8f-130">このフィールドは、 Microsoft Windows の **表示設定** で使用できます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-130">This field is available in **Display settings** in Microsoft Windows.</span></span>

<span data-ttu-id="25d8f-131">これらの手順が機能しない場合は、RDP セッションを開始する前に Internet Explorer で既定のズーム レベルが 100 % になるよう、リモート デスクトップのサイズを変更するようにします。</span><span class="sxs-lookup"><span data-stu-id="25d8f-131">If those steps don't work, change the size of your remote desktop before you start the RDP session, so that the default zoom level in Internet Explorer is 100 percent.</span></span>

## <a name="certificate-thumbprint-errors"></a><span data-ttu-id="25d8f-132">証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="25d8f-132">Certificate thumbprint errors</span></span>

### <a name="error-example---certificate-thumbprint-errors"></a><span data-ttu-id="25d8f-133">エラーの例 - 証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="25d8f-133">Error example - Certificate thumbprint errors</span></span>

> <span data-ttu-id="25d8f-134">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup\*\* が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-134">Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup\*\* threw an exception.</span></span> <span data-ttu-id="25d8f-135">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-135">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-136"> --\> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 拇印によるトークン作成用の証明書の検索に失敗しました: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</span><span class="sxs-lookup"><span data-stu-id="25d8f-136"> --\> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e.</span></span>

### <a name="solution---certificate-thumbprint-errors"></a><span data-ttu-id="25d8f-137">ソリューション - 証明書の拇印のエラー</span><span class="sxs-lookup"><span data-stu-id="25d8f-137">Solution - Certificate thumbprint errors</span></span>

<span data-ttu-id="25d8f-138">以下に挙げるいずれかの理由でエラー メッセージが表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-138">You might receive the error message for one of the following reasons:</span></span>

- <span data-ttu-id="25d8f-139">CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="25d8f-139">The certificate thumbprint that you copied into the CloudEnvironment.Config and wif.config files includes invisible Unicode characters.</span></span> <span data-ttu-id="25d8f-140">拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-140">To determine whether the thumbprint contains invisible Unicode characters, paste it into a Unicode code converter, and see whether extra characters appear in the **HTML/XML** field.</span></span> <span data-ttu-id="25d8f-141">たとえば、 <https://r12a.github.io/apps/conversion/>にて提供されている Unicode コンバーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-141">For example, you can use the Unicode converter that is available at <https://r12a.github.io/apps/conversion/>.</span></span>

    <span data-ttu-id="25d8f-142">[![ユニコード変換](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-142">[![Unicode conversion](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)</span></span>

- <span data-ttu-id="25d8f-143">アプリケーション オブジェクト サーバー マシン (AOS) に証明書が 正しくインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-143">The certificate wasn't installed on the Application Object Server (AOS) machine.</span></span> <span data-ttu-id="25d8f-144">以下の Microsoft Windows PowerShell スクリプトを実行し、認証が必要となる証明書をAOSマシン内で検索します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-144">To verify that the certificate can be found on the AOS machine, run the following Microsoft Windows PowerShell script.</span></span>

    ```Console
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    <span data-ttu-id="25d8f-145">スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書をインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-145">If the thumbprint doesn't appear in the Windows PowerShell console after you run the script, the certificate isn't installed.</span></span> <span data-ttu-id="25d8f-146">この問題を修正するには、すべてのAOSマシンに .cerファイルをコピーしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="25d8f-146">To fix the issue, copy and install a .cer file on all AOS machines.</span></span>

- <span data-ttu-id="25d8f-147">負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-147">If this issue occurs when you run load tests, the setup scripts might not have installed the corresponding .pfx file correctly.</span></span> <span data-ttu-id="25d8f-148">CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-148">Verify that the password that is specified in the CloudCtuFakeACSInstall.cmd file matches the password that was set when the certificate was created.</span></span>

    <span data-ttu-id="25d8f-149">[![.cmd file のパスワード](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-149">[![Password in the .cmd file](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)</span></span>

## <a name="no-endpoint-is-listening"></a><span data-ttu-id="25d8f-150">リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="25d8f-150">No endpoint is listening</span></span>

<span data-ttu-id="25d8f-151">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-151">This issue can occur when you run single-user or multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

### <a name="error-example---no-endpoint-is-listening"></a><span data-ttu-id="25d8f-152">エラーの例 - リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="25d8f-152">Error example - No endpoint is listening</span></span>

<span data-ttu-id="25d8f-153">テスト、またはユーザー作成処理が失敗し、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-153">The tests fail, or the user creation process fails, and the following error message is shown:</span></span>

> <span data-ttu-id="25d8f-154">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-154">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-155"> ---\> System.ServiceModel.EndpointNotFoundException: \\\<web address\> にてメッセージを受領することができるエンドポイント リスニングがありません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-155"> ---\> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at \\\<web address\> that could accept the message.</span></span> <span data-ttu-id="25d8f-156">この事象は、正しくないアドレスまたは SOAP アクションによって引き起こされることがあります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-156">This is often caused by an incorrect address or SOAP action.</span></span>

### <a name="solution---no-endpoint-is-listening"></a><span data-ttu-id="25d8f-157">ソリューション - リッスンしているエンドポイントはありません</span><span class="sxs-lookup"><span data-stu-id="25d8f-157">Solution - No endpoint is listening</span></span>

<span data-ttu-id="25d8f-158">この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-158">This issue occurs when the host that is specified in the CloudEnvironment.Config file can't be accessed from the machine that is trying to run the tests or create users.</span></span>

<span data-ttu-id="25d8f-159">CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-159">In the CloudEnvironment.Config file, review the values that are specified by the following keys:</span></span>

- <span data-ttu-id="25d8f-160">\\\<ExecutionConfigurations Key="HostName" Value="\<web address of host\>" /\></span><span class="sxs-lookup"><span data-stu-id="25d8f-160">\\\<ExecutionConfigurations Key="HostName" Value="\<web address of host\>" /\></span></span>
- <span data-ttu-id="25d8f-161">\\\<ExecutionConfigurations Key="SoapHostName" Value="\<web address of SOAP\>" /\></span><span class="sxs-lookup"><span data-stu-id="25d8f-161">\\\<ExecutionConfigurations Key="SoapHostName" Value="\<web address of SOAP\>" /\></span></span>

<span data-ttu-id="25d8f-162">これらのキーに指定する Web アドレスは、現在テストを実施している環境である必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-162">The web addresses that are specified by these keys must be in the environment that you're testing.</span></span> <span data-ttu-id="25d8f-163">開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-163">In a web browser on your developer machine, make sure that you can open the web address that is specified by the **HostName** key.</span></span>

<span data-ttu-id="25d8f-164">オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-164">For online load tests, the environment that is specified by the **HostName** key in the CloudEnvironment.Config file must be publicly accessible from any machine.</span></span> <span data-ttu-id="25d8f-165">したがって、ワンボックス環境をテストする必要がある場合、Microsoft Visual Studio Online Online を使用して負荷テストを実行することはできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。</span><span class="sxs-lookup"><span data-stu-id="25d8f-165">Therefore, if you must test a one-box environment, you won't be able to run the load test by using Microsoft Visual Studio Online, because the endpoint won't be accessible outside the one-box environment.</span></span>

## <a name="users-cant-be-enumerated"></a><span data-ttu-id="25d8f-166">ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="25d8f-166">Users can't be enumerated</span></span>

<span data-ttu-id="25d8f-167">この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-167">This issue can occur when you run multi-user tests, or when you create users by using MS.Dynamics.Performance.CreateUsers.exe.</span></span>

### <a name="error-example---users-cant-be-enumerated"></a><span data-ttu-id="25d8f-168">エラーの例 - ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="25d8f-168">Error example - Users can't be enumerated</span></span>

> <span data-ttu-id="25d8f-169">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-169">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-170"> ---\> System.InvalidOperationException: AX のユーザーを列挙することができませんでした ---\> System.ServiceModel.FaultException'1\[System.ComponentModel.Win32Exception\]: 禁止されています</span><span class="sxs-lookup"><span data-stu-id="25d8f-170"> ---\> System.InvalidOperationException: Could not enumerate AX users ---\> System.ServiceModel.FaultException'1\[System.ComponentModel.Win32Exception\]: Forbidden</span></span>

### <a name="solution---users-cant-be-enumerated"></a><span data-ttu-id="25d8f-171">ソリューション - ユーザーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="25d8f-171">Solution - Users can't be enumerated</span></span>

<span data-ttu-id="25d8f-172">3 つのシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-172">Three scenarios can cause this error:</span></span>

- <span data-ttu-id="25d8f-173">CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーに、システム管理者ロールが割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-173">The System Administrator role isn't assigned to the user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span> <span data-ttu-id="25d8f-174">適切なユーザーが指定されていることを検証するには、エンドポイントにサインインし、ユーザーのロールを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-174">To verify that you've specified the correct user, sign in to the endpoint, and view the user's roles.</span></span>

    <span data-ttu-id="25d8f-175">[![ユーザーページ](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-175">[![Users page](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)</span></span>

- <span data-ttu-id="25d8f-176">CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーは、 `https://sts.windows-ppe.net/` または `https://sts.windows.net/` 以外のプロバイダーを持っています。</span><span class="sxs-lookup"><span data-stu-id="25d8f-176">The user who is specified as **SelfMintingAdminUser** in the CloudEnvironment.config file has a provider other than `https://sts.windows-ppe.net/` or `https://sts.windows.net/`.</span></span> <span data-ttu-id="25d8f-177">場合によっては、管理者ユーザーの **プロバイダ** フィールドに会社固有のドメインを含めます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-177">Sometimes, a company-specific domain is included in the **Provider** field for the admin user.</span></span>

- <span data-ttu-id="25d8f-178">Finance and Operations アプリが 21Vianet に配置されている場合、**NetworkDomain="https://sts.chinacloudapi.cn/"** を **SelfMintingSysUser** および **SelfMintingAdminUser** で指定したことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-178">If your Finance and Operations apps were deployed in 21Vianet, make sure that you have specified **NetworkDomain="https://sts.chinacloudapi.cn/"** in **SelfMintingSysUser** and **SelfMintingAdminUser**.</span></span>

<span data-ttu-id="25d8f-179">この問題を回避するには、任意の名前と電子メール アドレスを持つユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-179">To work around this issue, create a user who has any name and email address.</span></span> <span data-ttu-id="25d8f-180">**システム管理者** ロールを新しいユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-180">Assign the **System Administrator** role to the new user.</span></span> <span data-ttu-id="25d8f-181">ユーザーを実在の Microsoft Azure Active Directory (Azure AD) ユーザーにリンクする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-181">You don't have to link the user to a real Microsoft Azure Active Directory (Azure AD) user.</span></span> <span data-ttu-id="25d8f-182">CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-182">Specify this new admin user as **SelfMintingAdminUser** in the CloudEnvironment.config file.</span></span>

## <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a><span data-ttu-id="25d8f-183">クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="25d8f-183">The HTTP request was forbidden with client authentication scheme 'Anonymous'</span></span>

### <a name="error-example---the-http-request-was-forbidden"></a><span data-ttu-id="25d8f-184">エラーの例 - HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="25d8f-184">Error example - The HTTP request was forbidden</span></span>

> <span data-ttu-id="25d8f-185">初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-185">Initialization method \<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="25d8f-186">System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: クライアント認証スキーム'Anonymous'でHTTP要求が禁止されました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-186">System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'.</span></span><span data-ttu-id="25d8f-187"> ---\> System.Net.WebException: リモートサーバーからエラーが返されました: (403) 許可されていません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-187"> ---\> System.Net.WebException: The remote server returned an error: (403) Forbidden.</span></span>

### <a name="solution---the-http-request-was-forbidden"></a><span data-ttu-id="25d8f-188">ソリューション - HTTP 要求が禁止されました</span><span class="sxs-lookup"><span data-stu-id="25d8f-188">Solution - The HTTP request was forbidden</span></span>

<span data-ttu-id="25d8f-189">3 つの既知のシナリオで、このエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-189">Three known scenarios can cause this error:</span></span>

- <span data-ttu-id="25d8f-190">テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-190">The test users are created by running MS.Dynamics.Performance.CreateUsers.exe without any arguments.</span></span> <span data-ttu-id="25d8f-191">例えば、CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスが正しくフォーマットされません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-191">For example, if the CreateUsers script is run without any arguments, the email addresses of test users that are created won't be correctly formatted.</span></span> <span data-ttu-id="25d8f-192">これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-192">If these users are used to run the tests, the tests will generate the forbidden request error.</span></span> <span data-ttu-id="25d8f-193">このシナリオでユーザーを表示することによってエラーが発生することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-193">You can verify that this scenario is causing the error by viewing the users.</span></span> <span data-ttu-id="25d8f-194">テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-194">The incorrect email addresses of the test users will resemble the email addresses in the following illustration.</span></span>

    <span data-ttu-id="25d8f-195">[![誤りのあるユーザーの電子メールアドレスの一覧](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-195">[![List of incorrect user email addresses](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)</span></span>

    <span data-ttu-id="25d8f-196">問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-196">To resolve the issue, delete the test users who have incorrectly formatted email addresses.</span></span> <span data-ttu-id="25d8f-197">CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を特定します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-197">Rerun the CreateUsers script, and specify the user count and company.</span></span>

- <span data-ttu-id="25d8f-198">CloudEnvironment.Config ファイルの **UserCount** フィールドで指定しているユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えています。</span><span class="sxs-lookup"><span data-stu-id="25d8f-198">The number of users that you specify in the **UserCount** field in the CloudEnvironment.Config file exceeds the number of test users that you created by using MS.Dynamics.Performance.CreateUsers.exe.</span></span> <span data-ttu-id="25d8f-199">少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-199">Make sure that you created at least as many test users as you request in the CloudEnvironment.Config file.</span></span>

    <span data-ttu-id="25d8f-200">[![CloudEnvironment.config ファイル](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-200">[![CloudEnvironment.Config file](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)</span></span>

- <span data-ttu-id="25d8f-201">Finance and Operations アプリが 21Vianet に展開されている場合は、開発環境とパフォーマンス テスト環境が 10.0.11 以上のプラットフォーム更新にあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-201">If your Finance and Operations apps were deployed in 21Vianet, make sure that your development and performance testing environments are in Platform Update for 10.0.11 or above.</span></span>

## <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="25d8f-202">メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-202">At least one security token in the message could not be validated</span></span>

<span data-ttu-id="25d8f-203">この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成している場合、AOSマシンが開発用のマシンと異なる場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-203">This issue can occur when you run multi-user tests, when you create users by using MS.Dynamics.Performance.CreateUsers.exe, when the AOS machine differs from the developer machine.</span></span>

### <a name="error-example---at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="25d8f-204">エラーの例 - メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-204">Error example - At least one security token in the message could not be validated</span></span>

> <span data-ttu-id="25d8f-205">System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-205">System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-206"> ---\> System.ServiceModel.Security.MessageSecurityException: セキュリティで保護されていない、または正しく保護されていない障害を受信しました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-206"> ---\> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party.</span></span> <span data-ttu-id="25d8f-207">障害コードと詳細については、FaultException 内部を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-207">See the inner FaultException for the fault code and detail.</span></span><span data-ttu-id="25d8f-208"> ---\> System.ServiceModel.FaultException: メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-208"> ---\> System.ServiceModel.FaultException: At least one security token in the message could not be validated.</span></span>

### <a name="solution---at-least-one-security-token-in-the-message-could-not-be-validated"></a><span data-ttu-id="25d8f-209">ソリューション - メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-209">Solution - At least one security token in the message could not be validated</span></span>

<span data-ttu-id="25d8f-210">この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-210">This issue occurs when the AOS endpoint can't validate the thumbprint of the certificate that you created.</span></span> <span data-ttu-id="25d8f-211">2 つの原因が考えられます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-211">There are two possible causes:</span></span>

- <span data-ttu-id="25d8f-212">証明書が AOS マシンにインストールされていません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-212">The certificate wasn't installed on the AOS machine.</span></span> <span data-ttu-id="25d8f-213">この問題を修正するには、AOSマシンに .cerファイルをコピーしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="25d8f-213">To fix the issue, copy a .cer file to the AOS machine, and install it.</span></span>
- <span data-ttu-id="25d8f-214">証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。</span><span class="sxs-lookup"><span data-stu-id="25d8f-214">The thumbprint of the certificate wasn't added to the wif.config file on the AOS machine.</span></span> <span data-ttu-id="25d8f-215">この問題を修正するには、wifファイルに証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-215">To fix the issue, add the certificate to the wif.config file.</span></span> <span data-ttu-id="25d8f-216">Wifファイルを更新した後に、必ずMicrosoft インターネット インフォメーション サービス (IIS) を再起動してください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-216">Be sure to restart Microsoft Internet Information Services (IIS) after you change the wif.config file.</span></span>

## <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="25d8f-217">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています</span><span class="sxs-lookup"><span data-stu-id="25d8f-217">MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing from the deployment items</span></span>

<span data-ttu-id="25d8f-218">この問題は、通常、負荷 テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-218">This issue usually occurs when you run load tests.</span></span>

### <a name="error-example---msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing"></a><span data-ttu-id="25d8f-219">エラーの例 - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が不足しています</span><span class="sxs-lookup"><span data-stu-id="25d8f-219">Error example - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing</span></span>

> <span data-ttu-id="25d8f-220">\<Test class name\>.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-220">\<Test class name\>.TestSetup threw exception.</span></span> <span data-ttu-id="25d8f-221">InvalidOperationException: InvalidOperationException: ServiceModelクライアント構成セクションに名前'ClientCommunicationManager'および契約'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager'を持つエンドポイント要素が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="25d8f-221">System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section.</span></span> <span data-ttu-id="25d8f-222">これは、アプリケーションに対応する構成ファイルが見つからなかったか、またはこの名前と一致するエンドポイント要素がクライアント要素にて見つからないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="25d8f-222">This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element..</span></span> <span data-ttu-id="25d8f-223">SSystem.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors にて (ServiceEndpoint serviceEndpoint, String configurationName)</span><span class="sxs-lookup"><span data-stu-id="25d8f-223">at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)</span></span>

### <a name="solution---msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing"></a><span data-ttu-id="25d8f-224">ソリューション - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が不足しています</span><span class="sxs-lookup"><span data-stu-id="25d8f-224">Solution - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config is missing</span></span>

<span data-ttu-id="25d8f-225">この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-225">This issue occurs when the system can't find the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file when the load tests are run, because the file wasn't added as a deployment item.</span></span> <span data-ttu-id="25d8f-226">テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-226">Verify that the MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="25d8f-227">\<solution path\>\\TestResults\\\<your test run\>\\Out</span><span class="sxs-lookup"><span data-stu-id="25d8f-227">\<solution path\>\\TestResults\\\<your test run\>\\Out</span></span>

<span data-ttu-id="25d8f-228">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-228">If the file is missing, add it to the deployment items in the test settings.</span></span>

<span data-ttu-id="25d8f-229">非常に似た名前を持つ 2 つのファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-229">There are two files that have very similar names.</span></span> <span data-ttu-id="25d8f-230">一方は名前が \*.dll で終わるファイルで、もう一方は名前が \*.dll.configで終わるファイルです。 \*.dll.configファイルはテスト設定の配置項目に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-230">The name of one file ends in \*.dll, and the name of the other file ends in \*.dll.config. The \*.dll.config file must be in the deployment items in the test settings.</span></span>

## <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a><span data-ttu-id="25d8f-231">CloudEnvironment.Config が配置項目で見つかりません</span><span class="sxs-lookup"><span data-stu-id="25d8f-231">CloudEnvironment.Config is missing from the deployment items</span></span>

<span data-ttu-id="25d8f-232">この問題は、通常、ロード テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-232">This issue usually occurs only when you run load tests.</span></span>

### <a name="error-example---cloudenvironmentconfig-is-missing"></a><span data-ttu-id="25d8f-233">エラーの例 - CloudEnvironment.Config が見つかりません</span><span class="sxs-lookup"><span data-stu-id="25d8f-233">Error example - CloudEnvironment.Config is missing</span></span>

> <span data-ttu-id="25d8f-234">初期化メソッド \\\<Test class name\>.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-234">Initialization method \\\<Test class name\>.TestSetup threw exception.</span></span>
<span data-ttu-id="25d8f-235">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-235">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-236"> ---\> MS.Dynamics.TestTools.TestLogging.EvaluateException: アサートに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-236"> ---\> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed.</span></span> <span data-ttu-id="25d8f-237">DateTime="10/13/2017 14:42:55" "'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-237">DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".</span></span>

### <a name="solution---cloudenvironmentconfig-is-missing"></a><span data-ttu-id="25d8f-238">ソリューション - CloudEnvironment.Config が見つかりません</span><span class="sxs-lookup"><span data-stu-id="25d8f-238">Solution - CloudEnvironment.Config is missing</span></span>

<span data-ttu-id="25d8f-239">この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-239">This issue occurs when the CloudEnvironment.Config file isn't present when the tests are run.</span></span> <span data-ttu-id="25d8f-240">一般的に、この問題は負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-240">It typically occurs when you run load tests and the CloudEnvironment.Config file wasn't added as a deployment item.</span></span> <span data-ttu-id="25d8f-241">テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-241">Verify that the CloudEnvironment.Config file is in the Out folder for the test run:</span></span>

<span data-ttu-id="25d8f-242">\<solution path\>\\TestResults\\\<your test run\>\\Out</span><span class="sxs-lookup"><span data-stu-id="25d8f-242">\<solution path\>\\TestResults\\\<your test run\>\\Out</span></span>

<span data-ttu-id="25d8f-243">ファイルが欠落している場合は、テストの設定で配置項目に追加します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-243">If the file is missing, add it to the deployment items in the test settings.</span></span>

<span data-ttu-id="25d8f-244">[![テスト設定 ダイアログ ボックスの 配置 タブ](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-244">[![Deployment items in the Test Settings dialog box](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)</span></span>

## <a name="interactiveclientid-was-not-specified-in-the-settings"></a><span data-ttu-id="25d8f-245">InteractiveClientId が設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-245">InteractiveClientId was not specified in the settings</span></span>

### <a name="error-example---interactiveclientid-was-not-specified-in-the-settings"></a><span data-ttu-id="25d8f-246">エラーの例 - InteractiveClientId が設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-246">Error example - InteractiveClientId was not specified in the settings</span></span>

> <span data-ttu-id="25d8f-247">'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-247">The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.</span></span><span data-ttu-id="25d8f-248"> ---\> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientIdが設定で指定されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="25d8f-248"> ---\> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings.</span></span>

### <a name="solution---interactiveclientid-was-not-specified-in-the-settings"></a><span data-ttu-id="25d8f-249">ソリューション - InteractiveClientId が設定で指定されていませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-249">Solution - InteractiveClientId was not specified in the settings</span></span>

<span data-ttu-id="25d8f-250">この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-250">This issue occurs when the **SelfSigningCertificateThumbprint** field is left blank in the CloudEnvironment.Config file.</span></span> <span data-ttu-id="25d8f-251">CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-251">In the CloudEnvironment.Config file, find the following line, and paste in the thumbprint of the certificate that you created and installed.</span></span>

```xml
\<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

## <a name="the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="25d8f-252">リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="25d8f-252">The remote host forcibly closed an existing connection</span></span>

### <a name="error-example---the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="25d8f-253">エラーの例 - リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="25d8f-253">Error example - The remote host forcibly closed an existing connection</span></span>

> <span data-ttu-id="25d8f-254">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-254">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-255"> ---\> System.ServiceModel.CommunicationException: \\\<Host name\>/Services/AxUserManagement/Service.svc/ws2007FedHttp に HTTP 要求をした際にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-255"> ---\> System.ServiceModel.CommunicationException: An error occurred while making the HTTP request to \\\<Host name\>/Services/AxUserManagement/Service.svc/ws2007FedHttp.</span></span> <span data-ttu-id="25d8f-256">HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-256">This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case.</span></span> <span data-ttu-id="25d8f-257">これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="25d8f-257">This could also be caused by a mismatch of the security binding between the client and the server.</span></span><span data-ttu-id="25d8f-258"> ---\> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-258"> ---\> System.Net.WebException: The underlying connection was closed: An unexpected error occurred on a send.</span></span><span data-ttu-id="25d8f-259"> ---\> System.IO.IOException: 転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-259"> ---\> System.IO.IOException: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.</span></span><span data-ttu-id="25d8f-260"> ---\> System.Net.Sockets.SocketException: 既存の接続がリモートホストによって強制的に切断されました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-260"> ---\> System.Net.Sockets.SocketException: An existing connection was forcibly closed by the remote host.</span></span>

### <a name="solution---the-remote-host-forcibly-closed-an-existing-connection"></a><span data-ttu-id="25d8f-261">ソリューション - リモート ホストは、既存の接続を強制的に終了した</span><span class="sxs-lookup"><span data-stu-id="25d8f-261">Solution - The remote host forcibly closed an existing connection</span></span>

<span data-ttu-id="25d8f-262">開発コンピューターで次の Windows PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-262">Run the following Windows PowerShell script on the development machine.</span></span>

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

## <a name="service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="25d8f-263">コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-263">Service w3svc was not found on computer</span></span>

<span data-ttu-id="25d8f-264">このエラーは Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-264">This error occurs only when you run load tests by using Visual Studio Online.</span></span>

### <a name="error-example---service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="25d8f-265">エラーの例 - コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-265">Error example - Service w3svc was not found on computer</span></span>

> <span data-ttu-id="25d8f-266">テストメソッド MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend が例外をスローしました。System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement'のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-266">Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-267"> ---\> System.InvalidOperationException: コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-267"> ---\> System.InvalidOperationException: Service w3svc was not found on computer '.'.</span></span><span data-ttu-id="25d8f-268"> ---\> System.ComponentModel.Win32Exception: 指定されたサービスは、インストールされたサービスに存在しません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-268"> ---\> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service.</span></span>

### <a name="solution---service-w3svc-was-not-found-on-computer"></a><span data-ttu-id="25d8f-269">ソリューション - コンピューターでサービス w3svc が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-269">Solution - Service w3svc was not found on computer</span></span>

<span data-ttu-id="25d8f-270">この問題を解決する修正プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="25d8f-270">A hotfix is available that resolves this issue.</span></span> <span data-ttu-id="25d8f-271">Microsoft サポート技術情報 (KB) 番号は 4095640 です。</span><span class="sxs-lookup"><span data-stu-id="25d8f-271">The Microsoft Knowledge Base (KB) number is 4095640.</span></span>

## <a name="the-file-iedriverserverexe-does-not-exist"></a><span data-ttu-id="25d8f-272">The file IEDriverServer.exe ファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-272">The file IEDriverServer.exe does not exist</span></span>

<span data-ttu-id="25d8f-273">この問題はシングル ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-273">This issue affects only single-user tests.</span></span>

### <a name="error-example---the-file-iedriverserverexe-does-not-exist"></a><span data-ttu-id="25d8f-274">エラーの例 - IEDriverServer.exe ファイルが存在しません</span><span class="sxs-lookup"><span data-stu-id="25d8f-274">Error example - The file IEDriverServer.exe does not exist</span></span>

> <span data-ttu-id="25d8f-275">ファイル K:\\perfSDK\\PerfSDKLocalDirectory\\SampleProject\\TestResults\\Admin501201994c\_devae648d1909-1 2018-06-25 03\_40\_51\\Out\\Common\\External\\Selenium\\IEDriverServer.exe が存在しません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-275">The file K:\\perfSDK\\PerfSDKLocalDirectory\\SampleProject\\TestResults\\Admin501201994c\_devae648d1909-1 2018-06-25 03\_40\_51\\Out\\Common\\External\\Selenium\\IEDriverServer.exe does not exist.</span></span> <span data-ttu-id="25d8f-276">ドライバーは、 `https://selenium-release.storage.googleapis.com/index.html`にてダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-276">The driver can be downloaded at `https://selenium-release.storage.googleapis.com/index.html`.</span></span>

### <a name="solution---the-file-iedriverserverexe-does-not-exist"></a><span data-ttu-id="25d8f-277">ソリューション - IEDriverServer.exe ファイルが存在しません</span><span class="sxs-lookup"><span data-stu-id="25d8f-277">Solution - The file IEDriverServer.exe does not exist</span></span>

<span data-ttu-id="25d8f-278">**\<Your\_PerfSDK\_Folder\>** にある **Common\\External\\Selenium** フォルダーを **\<Your\_PerfSDK\_Folder>\\SampleProject\\ PerfSDKSample\\bin\\Debug** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="25d8f-278">Copy the **Common\\External\\Selenium** folder under **\<Your\_PerfSDK\_Folder\>** to the **\<Your\_PerfSDK\_Folder>\\SampleProject\\ PerfSDKSample\\bin\\Debug** folder.</span></span>

## <a name="failed-finding-the-certificate-for-minting-tokens-by-thumbprint-your-certificate-thumbprint"></a><span data-ttu-id="25d8f-279">拇印によるトークン作成用の証明書の検索に失敗しました: \<your certificate thumbprint\></span><span class="sxs-lookup"><span data-stu-id="25d8f-279">Failed finding the certificate for minting tokens by thumbprint: \<your certificate thumbprint\></span></span>

### <a name="error-example---failed-finding-the-certificate-for-minting-tokens-by-thumbprint"></a><span data-ttu-id="25d8f-280">エラーの例 - 拇印によるトークン作成用の証明書の検索に失敗しました</span><span class="sxs-lookup"><span data-stu-id="25d8f-280">Error example - Failed finding the certificate for minting tokens by thumbprint</span></span>

<span data-ttu-id="25d8f-281">[![エラーメッセージとエラースタックの追跡](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-281">[![Error message and error stack trace](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)</span></span>

### <a name="solution---failed-finding-the-certificate-for-minting-tokens-by-thumbprint"></a><span data-ttu-id="25d8f-282">ソリューション - 拇印によるトークン作成用の証明書の検索に失敗しました</span><span class="sxs-lookup"><span data-stu-id="25d8f-282">Solution - Failed finding the certificate for minting tokens by thumbprint</span></span>

<span data-ttu-id="25d8f-283">生成された証明書は、サンドボックス環境内の各AOSマシンにインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="25d8f-283">Make sure that you install the generated certificate on each AOS machine in your sandbox environment.</span></span>

## <a name="the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a><span data-ttu-id="25d8f-284">実行しようとしているアクションには、 Visual Studio チームサービスへの接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="25d8f-284">The action you are trying to perform requires a connection to Visual Studio Team Services</span></span>

<span data-ttu-id="25d8f-285">この問題はマルチ ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-285">This issue affects only multi-user tests.</span></span>

### <a name="error-example---the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a><span data-ttu-id="25d8f-286">エラーの例 - 実行しようとしているアクションには、Visual Studio チームサービスへの接続が必要です</span><span class="sxs-lookup"><span data-stu-id="25d8f-286">Error example - The action you are trying to perform requires a connection to Visual Studio Team Services</span></span>

<span data-ttu-id="25d8f-287">[![エラーメッセージの詳細](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-287">[![Error message details](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)</span></span>

### <a name="solution---the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a><span data-ttu-id="25d8f-288">ソリューション - 実行しようとしているアクションには、Visual Studio チームサービスへの接続が必要です</span><span class="sxs-lookup"><span data-stu-id="25d8f-288">Solution - The action you are trying to perform requires a connection to Visual Studio Team Services</span></span>

<span data-ttu-id="25d8f-289">Azure DevOps に接続するときは、**dev.azure.com/\<Azure\_DevOps\_Account\>** ではなく、古い URI 形式 (**\<Azure\_DevOps\_Account\>.visualstudio.com**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-289">When you connect to Azure DevOps, use the old URI format (**\<Azure\_DevOps\_Account\>.visualstudio.com**) instead of **dev.azure.com/\<Azure\_DevOps\_Account\>**.</span></span> <span data-ttu-id="25d8f-290">古いURIを使用して Azure DevOps を開き、 **Visual Studioで開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-290">Additionally, open Azure DevOps by using the old URI, and then select **Open in Visual Studio**.</span></span>

## <a name="could-not-load-file-or-assembly-aoskerneldll-or-one-of-its-dependencies"></a><span data-ttu-id="25d8f-291">ファイルまたはアセンブリ 'aoskernel.dll' 、あるいは依存関係を読み込みできませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-291">Could not load file or assembly 'aoskernel.dll' or one of its dependencies</span></span>

<span data-ttu-id="25d8f-292">このエラーはマルチ ユーザー テストにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-292">This error affects only multi-user tests.</span></span>

### <a name="error-example---could-not-load-file-or-assembly-aoskerneldll"></a><span data-ttu-id="25d8f-293">エラーの例 - ファイルまたはアセンブリ 'aoskernel.dll' を読み込むことができませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-293">Error example - Could not load file or assembly 'aoskernel.dll'</span></span>

<span data-ttu-id="25d8f-294">[![エラーメッセージとエラースタックの追跡,デバッグの追跡](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</span><span class="sxs-lookup"><span data-stu-id="25d8f-294">[![Error message, error stack trace, and debug trace](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)</span></span>

### <a name="solution---could-not-load-file-or-assembly-aoskerneldll"></a><span data-ttu-id="25d8f-295">ソリューション - ファイルまたはアセンブリ 'aoskernel.dll' を読み込むことができませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-295">Solution - Could not load file or assembly 'aoskernel.dll'</span></span>

<span data-ttu-id="25d8f-296">プラットフォーム更新プログラム20 またはそれ以降が稼働している環境で、Open Database Connectivity (ODBC) ドライバ17が使用されていることを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="25d8f-296">Make sure that you're using Open Database Connectivity (ODBC) Driver 17 in an environment that has Platform update 20 or later.</span></span>

## <a name="azureactivedirectoryconfiguration-node-is-missing-in-cloudenvironmentconfig"></a><span data-ttu-id="25d8f-297">CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-297">AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config</span></span>

### <a name="error-example---azureactivedirectoryconfiguration-node-is-missing"></a><span data-ttu-id="25d8f-298">エラーの例 - AzureActiveDirectoryConfiguration ノードが見つかりません</span><span class="sxs-lookup"><span data-stu-id="25d8f-298">Error example - AzureActiveDirectoryConfiguration node is missing</span></span>

> <span data-ttu-id="25d8f-299">初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup が例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-299">Initialization method MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup threw exception.</span></span> <span data-ttu-id="25d8f-300">System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-300">System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</span></span><span data-ttu-id="25d8f-301"> ---\> System.Reflection.TargetInvocationException: 呼び出しのターゲットによって例外がスローされました。</span><span class="sxs-lookup"><span data-stu-id="25d8f-301"> ---\> System.Reflection.TargetInvocationException: Exception has been thrown by the target of an invocation.</span></span><span data-ttu-id="25d8f-302"> ---\> System.MissingFieldException: CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-302"> ---\> System.MissingFieldException: AzureActiveDirectoryConfiguration node is missing in CloudEnvironment.config.</span></span>

### <a name="solution---azureactivedirectoryconfiguration-node-is-missing"></a><span data-ttu-id="25d8f-303">ソリューション - AzureActiveDirectoryConfiguration ノードが見つかりません</span><span class="sxs-lookup"><span data-stu-id="25d8f-303">Solution - AzureActiveDirectoryConfiguration node is missing</span></span>

<span data-ttu-id="25d8f-304">**"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"** のすべてのインスタンスを、CloudEnvironment.config ファイルの **AuthenticatorConfigurationCollection** セクションにある **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"** で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="25d8f-304">Replace all instances of **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"** with **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"** in the **AuthenticatorConfigurationCollection** section of the CloudEnvironment.config file.</span></span>

## <a name="multiple-warning-messages-before-and-after-multi-user-testing-that-uses-azure-devops"></a><span data-ttu-id="25d8f-305">Azure DevOpsを使用したマルチユーザーテストの開始前と後に複数の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="25d8f-305">Multiple warning messages before and after multi-user testing that uses Azure DevOps</span></span>

### <a name="error-example---multiple-warning-messages-before-and-after-multi-user-testing"></a><span data-ttu-id="25d8f-306">エラーの例 - マルチユーザー テストの開始前と後に複数の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="25d8f-306">Error example - Multiple warning messages before and after multi-user testing</span></span>

![負荷テストステータスの例](./media/troubleshoot-perf-sdk-10.jpg)

![負荷テスト結果の例](./media/troubleshoot-perf-sdk-11.jpg)<span data-ttu-id="25d8f-309">]</span><span class="sxs-lookup"><span data-stu-id="25d8f-309">]</span></span>

### <a name="solution---multiple-warning-messages-before-and-after-multi-user-testing"></a><span data-ttu-id="25d8f-310">ソリューション - マルチユーザー テストの開始前と後に複数の警告メッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="25d8f-310">Solution - Multiple warning messages before and after multi-user testing</span></span>

<span data-ttu-id="25d8f-311">影響はありません。メッセージを無視しても問題ありません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-311">There is no impact, and the messages can be ignored.</span></span>

## <a name="the-type-or-namespace-name-xxxx-could-not-be-found-are-you-missing-a-using-directive-or-an-assembly-reference"></a><span data-ttu-id="25d8f-312">タイプまたは名前空間名 'xxxx' が見つかりませんでした (using ディレクティブまたはアセンブリ参照が不足していないかどうか確認してください)。</span><span class="sxs-lookup"><span data-stu-id="25d8f-312">The type or namespace name 'xxxx' could not be found (are you missing a using directive or an assembly reference?)</span></span>

### <a name="error-example---the-type-or-namespace-name-xxxx-could-not-be-found"></a><span data-ttu-id="25d8f-313">エラーの例 - タイプまたは名前空間名 'xxxx' が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-313">Error example - The type or namespace name 'xxxx' could not be found</span></span>

<span data-ttu-id="25d8f-314">タイプまたは名前空間名 'InventTransferOrders' が見つかりませんでした (using ディレクティブまたはアセンブリ参照が不足していないかどうか確認してください)。</span><span class="sxs-lookup"><span data-stu-id="25d8f-314">The type or namespace name 'InventTransferOrders' could not be found (are you missing a using directive or an assembly reference?)</span></span>

### <a name="solution---the-type-or-namespace-name-xxxx-could-not-be-found"></a><span data-ttu-id="25d8f-315">ソリューション - タイプまたは名前空間名 'xxxx' が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="25d8f-315">Solution - The type or namespace name 'xxxx' could not be found</span></span>

<span data-ttu-id="25d8f-316">perfSDK を使用して出荷されたサンプル ソリューションは既に準備されており、パッケージの分割後に更新されていません。</span><span class="sxs-lookup"><span data-stu-id="25d8f-316">The sample solution shipped with the perfSDK was previously prepared and wasn't updated after the packages split.</span></span> <span data-ttu-id="25d8f-317">この問題を解決するには、アセンブリ **MS.Dynamics.TestTools.DirectoryProxyLibrary.dll** を \<Service volume\>:\\PerfSDK\\PerfSDKLocalDirectory に参照として追加します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-317">To resolve the issue, add the assembly **MS.Dynamics.TestTools.DirectoryProxyLibrary.dll** under \<Service volume\>:\\PerfSDK\\PerfSDKLocalDirectory as a reference.</span></span>

## <a name="assembly-was-built-against-the-netframeworkversionv46-framework"></a><span data-ttu-id="25d8f-318">アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました</span><span class="sxs-lookup"><span data-stu-id="25d8f-318">Assembly was built against the ".NETFramework,Version=v4.6" framework</span></span>

### <a name="error-example---assembly-was-built-against-the-netframeworkversionv46-framework"></a><span data-ttu-id="25d8f-319">エラーの例 - アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました</span><span class="sxs-lookup"><span data-stu-id="25d8f-319">Error example - Assembly was built against the ".NETFramework,Version=v4.6" framework</span></span>

<span data-ttu-id="25d8f-320">アセンブリ "MS.Dynamics.TestTools.DirectoryProxyLibrary, Version=7.0.0.0, Culture=neutral, PublicKeyToken=a7cf325ee2c8a9ff" which was built against the ".NETFramework,Version=v4.6" フレームワークに間接的な依存関係があるため、プライマリ参照 "MS.Dynamics.TestTools.ApplicationSuiteProxyLibrary" を解決できませんでした。</span><span class="sxs-lookup"><span data-stu-id="25d8f-320">The primary reference "MS.Dynamics.TestTools.ApplicationSuiteProxyLibrary" could not be resolved because it has an indirect dependency on the assembly "MS.Dynamics.TestTools.DirectoryProxyLibrary, Version=7.0.0.0, Culture=neutral, PublicKeyToken=a7cf325ee2c8a9ff" which was built against the ".NETFramework,Version=v4.6" framework.</span></span> <span data-ttu-id="25d8f-321">このバージョンは、現在対象のフレームワーク ".NETFramework,Version=v4.5" よりも新しいバージョンです。</span><span class="sxs-lookup"><span data-stu-id="25d8f-321">This is a higher version than the currently targeted framework ".NETFramework,Version=v4.5".</span></span>

### <a name="solution--assembly-was-built-against-the-netframeworkversionv46-framework"></a><span data-ttu-id="25d8f-322">ソリューション - アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました</span><span class="sxs-lookup"><span data-stu-id="25d8f-322">Solution- Assembly was built against the ".NETFramework,Version=v4.6" framework</span></span>

<span data-ttu-id="25d8f-323">プロパティ ウィンドウの **ターゲット フレームワーク** プロパティを .Net Framework 4.6 に変更します。</span><span class="sxs-lookup"><span data-stu-id="25d8f-323">Change the **Target framework** property in the properties window of PerfSDKSample to .Net Framework 4.6.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
