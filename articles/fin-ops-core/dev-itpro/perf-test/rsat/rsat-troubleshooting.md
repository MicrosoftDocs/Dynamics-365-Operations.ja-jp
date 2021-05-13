---
title: Regression Suite Automation Tool のトラブルシューティング
description: このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ecb4375a6d20c21acd59d0221e4a2a1ce6ab7e3
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866170"
---
# <a name="troubleshoot-the-regression-suite-automation-tool"></a><span data-ttu-id="86cf7-103">Regression Suite Automation Tool のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="86cf7-103">Troubleshoot the Regression suite automation tool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86cf7-104">このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-104">This topic contains information about how to troubleshoot the Regression suite automation tool (RSAT).</span></span>

## <a name="playback-logs"></a><span data-ttu-id="86cf7-105">再生ログ</span><span class="sxs-lookup"><span data-stu-id="86cf7-105">Playback logs</span></span>

<span data-ttu-id="86cf7-106">テスト ケースの再生中に発生する問題のトラブル シューティングを行うには、**[RSAT の作業ディレクトリ]\\[テスト ケース ID]\\playback\\[TestName]Log.txt** にある開発者向けエラーログを開いてください。</span><span class="sxs-lookup"><span data-stu-id="86cf7-106">To troubleshoot issues that happen during playback of a test case, open the developer error log located at **[RSAT working directory]\\[test case ID]\\playback\\[TestName]Log.txt**.</span></span> <span data-ttu-id="86cf7-107">RSAT の作業ディレクトリは、RSATの [設定] ダイアログで指定されているディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="86cf7-107">The RSAT working directory is the directory specified in the RSAT settings dialog.</span></span>
<span data-ttu-id="86cf7-108">エラーメッセージを分析して、エラーが発生する可能性がある原因を特定します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-108">Analyze the error message to determine the possible cause of a failure.</span></span>

> [!NOTE]
> <span data-ttu-id="86cf7-109">RSAT のバージョンが 1.210 よりも古い場合、ログは **C:\\ユーザー\\[YourUserName]\\AppData\\Roaming\\regressionTool\\playback\\[TestName]ログ .txt** に格納されます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-109">For RSAT versions prior to 1.210, the log is located at **C:\\Users\\[YourUserName]\\AppData\\Roaming\\regressionTool\\playback\\[TestName]Log.txt**.</span></span>

## <a name="generator-logs"></a><span data-ttu-id="86cf7-110">ジェネレーター ログ</span><span class="sxs-lookup"><span data-stu-id="86cf7-110">Generator logs</span></span>

<span data-ttu-id="86cf7-111">テストの実行およびパラメータ ファイル生成時のエラーのトラブル シューティングを行うには、ジェネレーター ログ を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86cf7-111">To troubleshoot errors when generating test execution and parameter files, enable generator logs.</span></span>

<span data-ttu-id="86cf7-112">RSAT のインストール フォルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) 配下にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-112">Open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

```xml
<add key="LogGeneration" value="true" />
```

<span data-ttu-id="86cf7-113">テストの実行ファイルが生成されると、ログファイルが **[RSATの作業ディレクトリ]\\[テストケースID]\\generatorLogs** 配下に生成されます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-113">After test execution files are generated, you can find the log file under **[RSAT working directory]\\[test case ID]\\generatorLogs**</span></span>

> [!NOTE]
> <span data-ttu-id="86cf7-114">RSAT のバージョンが 1.210 よりも古い場合、ログは **C:\\ユーザー\\[Username]\\AppData\\Roaming\\regressionTool\\generatorLogs** に生成されます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-114">For RSAT versions prior to 1.210, the logs are generated under **C:\\Users\\[Username]\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

## <a name="authentication-certificate-and-installation"></a><span data-ttu-id="86cf7-115">認証証明書およびインストール</span><span class="sxs-lookup"><span data-stu-id="86cf7-115">Authentication certificate and installation</span></span>

+ <span data-ttu-id="86cf7-116">認証証明書は、RSAT がインストールされているのと同じコンピューター上の管理者によって作成およびインストールされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-116">The authentication certificate must be created and installed by an administrator on the same computer where RSAT is installed.</span></span> <span data-ttu-id="86cf7-117">管理者によって作成されていない場合は、テスト ケースを実行しようとすると次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-117">If it is not created by an admin, you will encounter the following error message when you try to run a test case.</span></span>

```Plaintext
Cannot access Finance and Operations environment. Verify your settings and make sure the environment is available.
```

+ <span data-ttu-id="86cf7-118">同じコンピューターで以前のバージョンの RSAT を使用した場合は、新しいバージョンをインストールする前に、そのバージョンを閉じてアンインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="86cf7-118">If you have used a previous version of RSAT on the same computer, close it and uninstall it before installing a new version.</span></span>

## <a name="screen-resolution-when-using-internet-explorer"></a><span data-ttu-id="86cf7-119">Internet Explorer 使用時の画面解像度</span><span class="sxs-lookup"><span data-stu-id="86cf7-119">Screen resolution when using Internet Explorer</span></span>

<span data-ttu-id="86cf7-120">ブラウザーに Internet Explorer を使用している場合、テストを正常に実行するには、デスクトップの解像度を100% に設定している必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-120">If you have selected Internet Explorer as your browser, your desktop resolution should be set to 100% to run the tests successfully.</span></span> <span data-ttu-id="86cf7-121">設定を変更するには、次の図に示すように、Windows の **ディスプレイ設定 > 拡大縮小とレイアウト** を使用します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-121">To change the settings, use Windows **Display settings > Scale and layout**, as shown in the following image:</span></span>

![画面の解像度の設定](media/screen-resolution.png)

## <a name="test-playback-errors"></a><span data-ttu-id="86cf7-123">再生エラーのテスト</span><span class="sxs-lookup"><span data-stu-id="86cf7-123">Test playback errors</span></span>

### <a name="soap-or-http-request-errors"></a><span data-ttu-id="86cf7-124">SOAP または HTTP 要求のエラー</span><span class="sxs-lookup"><span data-stu-id="86cf7-124">SOAP or HTTP request errors</span></span>

<span data-ttu-id="86cf7-125">スタンダード承認テスト サンドボックス環境 (Tier2) またはその他のマルチ ボックス環境に対してテストしている場合は、テストの実行時に次のいずれかのエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-125">If you are testing against a Standard Acceptance Test Sandbox environment (Tier2) or any other multi-box environment, and you may receive one of the following errors when you run a test.</span></span>

```Plaintext
There was no endpoint listening at https://<yourURL>soap.sandbox.operations.dynamics.com/Services/AxUserManagement/Service.svc/ws2007FedHttp that could accept the message. This is often caused by an incorrect address or SOAP action…

An error occurred while making the HTTP request to <Hostname>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused by a mismatch of the security binding between the client and the server.
```

<span data-ttu-id="86cf7-126">RSAT 設定ダイアログ ボックスで正しい SOAP ホスト名を指定したと仮定する場合、テスト ツールがインストールされているクライアント コンピューターで、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-126">Assuming that you have specified the correct SOAP hostname in the RSAT settings dialog box, run the following PowerShell scripts on your client computer where the test tool is installed.</span></span>

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false

if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))  { Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false}
```

<span data-ttu-id="86cf7-127">レジストリ キーを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-127">You can also manually set the registry keys.</span></span>

### <a name="cannot-enumerate-ax-users-error"></a><span data-ttu-id="86cf7-128">AX ユーザーを列挙できないエラー</span><span class="sxs-lookup"><span data-stu-id="86cf7-128">Cannot enumerate AX users error</span></span>

<span data-ttu-id="86cf7-129">テスト ケースを実行すると、次のエラーが表示される場合があります。エラーの詳細には、次のメッセージが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-129">You may receive the following error when running a test case, or the error details may contain the following messages.</span></span>

```Xml
<Message>The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</Message>
<Message>Could not enumerate AX users</Message>  (InnerError)`
```

![エラー メッセージ列挙ボックス](media/cannot-enumerate.png)

<span data-ttu-id="86cf7-131">このエラーを解決するには、RSAT の設定ダイアログ ボックスで指定されている **管理ユーザー名** を確認します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-131">To resolve this error, verify the **Admin user name** specified in the RSAT settings dialog box.</span></span> <span data-ttu-id="86cf7-132">**管理者ユーザー名** は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-132">The **Admin user name** must be the email address of a user that belongs to the System Administrator role on the Finance and Operations test environment that RSAT is connecting to.</span></span> <span data-ttu-id="86cf7-133">また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-133">The user account (e-mail address) must also belong to the same tenant as the test environment.</span></span> <span data-ttu-id="86cf7-134">たとえば、テスト環境のテナントが **contoso.com** 場合、管理ユーザーは **\@constoso.com** で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-134">For example, if your test environment's tenant is **contoso.com**, the admin user must end with **\@constoso.com**.</span></span>

### <a name="unsecured-fault-exception"></a><span data-ttu-id="86cf7-135">セキュリティ保護されていな障害の例外</span><span class="sxs-lookup"><span data-stu-id="86cf7-135">Unsecured fault exception</span></span>

<span data-ttu-id="86cf7-136">次のエラーでテスト ケースが一貫性なく失敗する場合は、通常、AOS 仮想マシン上の認証サムプリントの設定が不完全であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="86cf7-136">If a test case inconsistently fails with the following error, this usually indicates an incomplete configuration of the authentication thumbprints on the AOS virtual machines.</span></span>

```Xml
<Message>An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail.</Message>
<Message>At least one security token in the message could not be validated.</Message>
```

<span data-ttu-id="86cf7-137">通常このエラーは、RSAT が認証に使用している証明書を信頼するようにテスト環境が構成されていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-137">Typically, this error happens when the test environment has not been configured to trust the certificate that RSAT is using for authentication.</span></span> <span data-ttu-id="86cf7-138">(証明書は、RSAT の設定で指定された拇印によって識別されます。) たとえば、テスト環境の AOS 仮想マシンの wif.config ファイルに拇印が欠落している場合があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-138">(The certificate is identified by the thumbprint specified in your RSAT settings.) For example, the thumbprint could be missing in the wif.config file on the AOS virtual machine of the test environment.</span></span> <span data-ttu-id="86cf7-139">標準承認テスト環境 (Tier 2 以上) に対して実行している場合は、すべての AOS 仮想マシン上で認証拇印を構成していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-139">If you are running against a standard acceptance test environment (Tier 2 or higher), you might not have configured the authentication thumbprint on all of the AOS virtual machines.</span></span> <span data-ttu-id="86cf7-140">すべての AOS マシン上の **wif.config** にサムプリントを適切に追加してください。</span><span class="sxs-lookup"><span data-stu-id="86cf7-140">Make sure you properly add the thumbprint to the **wif.config** file on all of the AOS machines.</span></span> <span data-ttu-id="86cf7-141">詳細については、[接続を信頼するようにテスト環境を構成する](rsat-install-configure.md#configure-the-test-environment-to-trust-the-connection) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86cf7-141">For more information, see [Configure the test environment to trust the connection](rsat-install-configure.md#configure-the-test-environment-to-trust-the-connection).</span></span>

<span data-ttu-id="86cf7-142">このエラーは、RSAT がインストールされているクライアント コンピューターと Finance and Operations 環境との間で UTC 時間に不一致がある場合にも発生します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-142">We have also seen this error when there is a mismatch between the UTC time between the client computer (where RSAT is installed) and the Finance and Operations environment.</span></span> <span data-ttu-id="86cf7-143">これはまれなケースであり、管理者が UTC 時間を正しく構成していない場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-143">This is a rare case and only happens if your administrator has incorrectly configured the UTC time.</span></span> <span data-ttu-id="86cf7-144">クライアント コンピューターと Finance and Operations 環境は異なるタイム ゾーンに設定できますが、認証メカニズムはこの比較に依存しているため、両方の環境の UTC 時間は一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-144">The client computer and Finance and Operations environment can be on different time zones; however, the UTC time on both environments must match because the authentication mechanism relies on this comparison.</span></span>

## <a name="google-chrome-browser"></a><span data-ttu-id="86cf7-145">Google Chrome ブラウザー</span><span class="sxs-lookup"><span data-stu-id="86cf7-145">Google Chrome Browser</span></span>

<span data-ttu-id="86cf7-146">Active Directory のセキュリティ設定が原因で、Google Chrome ブラウザーが Regression Suite Automation Tool で機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="86cf7-146">The Google Chrome browser may not work with the Regression suite automation tool due to your Active Directory security settings.</span></span> <span data-ttu-id="86cf7-147">この場合、新しい Microsoft Edge または Internet Explorer を使用するように RSAT 設定を変更し ます。</span><span class="sxs-lookup"><span data-stu-id="86cf7-147">In this case, change your RSAT settings to use the new Microsoft Edge or Internet Explorer.</span></span>

## <a name="validating-blank-dates"></a><span data-ttu-id="86cf7-148">空白日付の検証</span><span class="sxs-lookup"><span data-stu-id="86cf7-148">Validating blank dates</span></span>

<span data-ttu-id="86cf7-149">日付/時刻の特定のコントロールが空白であることを確認する必要があるテスト ケースの場合は、このコントロールに対応する Excel のセルに次の値を挿入できます: 「01/01/1900」。</span><span class="sxs-lookup"><span data-stu-id="86cf7-149">If your test case requires validation that a certain control of type Date/Time is blank, you can insert the following value into the Excel cell corresponding to this control: "01/01/1900".</span></span>

## <a name="azure-devops-connectivity"></a><span data-ttu-id="86cf7-150">Azure DevOps 接続</span><span class="sxs-lookup"><span data-stu-id="86cf7-150">Azure DevOps connectivity</span></span>

<span data-ttu-id="86cf7-151">RSAT の設定で目的の Azure DevOps プロジェクトを選択すると、このエラーが表示される場合があります: 「構造のパス \<iteration path\> が無効です。</span><span class="sxs-lookup"><span data-stu-id="86cf7-151">You might you see this error when you select the desired Azure DevOps project in RSAT settings: "The structure path \<iteration path\> is not valid.</span></span> <span data-ttu-id="86cf7-152">設定を確認してから、もう一度お試しください。」</span><span class="sxs-lookup"><span data-stu-id="86cf7-152">Verify your settings and try again".</span></span> <span data-ttu-id="86cf7-153">このエラーを解決するには、Azure DevOps でプロジェクトを開き、テスト計画に移動します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-153">To resolve this error, open the project in Azure DevOps and navigate to the Test Plans.</span></span> <span data-ttu-id="86cf7-154">各テスト計画に定義されているイテレーション パスを確認します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-154">Verify the iteration path defined for each test plan.</span></span> <span data-ttu-id="86cf7-155">イテレーション パスがエラーで示されているものと似ている場合は、既存のイテレーション パスを削除し、テスト計画に新しいイテレーション パスを追加してから保存します。</span><span class="sxs-lookup"><span data-stu-id="86cf7-155">If the iteration path is similar to what is shown in the error, remove the existing iteration path and add a new one for the test plan and save.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]