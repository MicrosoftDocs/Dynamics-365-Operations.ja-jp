---
title: Regression Suite Automation Tool のトラブルシューティング
description: このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbc3dacedbe02f7fe4ae35760590b0b9f622de8c
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029388"
---
# <a name="troubleshoot-the-regression-suite-automation-tool"></a><span data-ttu-id="3c00d-103">Regression Suite Automation Tool のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3c00d-103">Troubleshoot the Regression suite automation tool</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c00d-104">このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-104">This topic contains information about how to troubleshoot the Regression suite automation tool (RSAT).</span></span>

## <a name="playback-logs"></a><span data-ttu-id="3c00d-105">再生ログ</span><span class="sxs-lookup"><span data-stu-id="3c00d-105">Playback logs</span></span>

<span data-ttu-id="3c00d-106">再生中にツールの問題のトラブルシューティングを行うには、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\playback\[TestName]Log.txt** にある開発者エラー ログを開きます。</span><span class="sxs-lookup"><span data-stu-id="3c00d-106">To troubleshoot issues with the tool during Playback operation, open the developer error log located at **C:\Users\$YourUserName\AppData\Roaming\regressionTool\playback\[TestName]Log.txt**.</span></span> <span data-ttu-id="3c00d-107">エラーメッセージを分析して、エラーが発生する可能性がある原因を特定します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-107">Analyze the error message to determine the possible cause of a failure.</span></span>

## <a name="authentication-certificate-and-installation"></a><span data-ttu-id="3c00d-108">認証証明書およびインストール</span><span class="sxs-lookup"><span data-stu-id="3c00d-108">Authentication certificate and installation</span></span>

+ <span data-ttu-id="3c00d-109">認証証明書は、RSAT がインストールされているのと同じコンピューター上の管理者によって作成およびインストールされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-109">The authentication certificate must be created and installed by an administrator on the same computer where RSAT is installed.</span></span> <span data-ttu-id="3c00d-110">管理者によって作成されていない場合は、テスト ケースを実行しようとすると次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c00d-110">If it is not created by an admin, you will encounter the following error message when you try to run a test case.</span></span>  

  ```Text
  Cannot access Finance and Operations environment. Verify your settings and make sure the environment is available.
  ```

+ <span data-ttu-id="3c00d-111">同じコンピューターで以前のバージョンの RSAT を使用した場合は、新しいバージョンをインストールする前に、そのバージョンを閉じてアンインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="3c00d-111">If you have used a previous version of RSAT on the same computer, close it and uninstall it before installing a new version.</span></span>

## <a name="screen-resolution"></a><span data-ttu-id="3c00d-112">画面の解像度</span><span class="sxs-lookup"><span data-stu-id="3c00d-112">Screen resolution</span></span>

<span data-ttu-id="3c00d-113">テストを正常に実行するには、デスクトップの解像度を 100% に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-113">Your desktop resolution should be set to 100% to run the tests successfully.</span></span> <span data-ttu-id="3c00d-114">設定を変更するには、次の図に示すように、Windows の **ディスプレイ設定 > 拡大縮小とレイアウト** を使用します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-114">To change the settings, use Windows **Display settings > Scale and layout**, as shown in the following image:</span></span>

![画面の解像度の設定](media/screen-resolution.png)
 
## <a name="test-playback-errors"></a><span data-ttu-id="3c00d-116">再生エラーのテスト</span><span class="sxs-lookup"><span data-stu-id="3c00d-116">Test playback errors</span></span>

### <a name="soap-or-http-request-errors"></a><span data-ttu-id="3c00d-117">SOAP または HTTP 要求のエラー</span><span class="sxs-lookup"><span data-stu-id="3c00d-117">SOAP or HTTP request errors</span></span>

<span data-ttu-id="3c00d-118">スタンダード承認テスト サンドボックス環境 (Tier2) またはその他のマルチ ボックス環境に対してテストしている場合は、テストの実行時に次のいずれかのエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-118">If you are testing against a Standard Acceptance Test Sandbox environment (Tier2) or any other multi-box environment, and you may receive one of the following errors when you run a test.</span></span>

```Text
There was no endpoint listening at https://<yourURL>soap.sandbox.operations.dynamics.com/Services/AxUserManagement/Service.svc/ws2007FedHttp that could accept the message. This is often caused by an incorrect address or SOAP action…

An error occurred while making the HTTP request to <Hostname>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused by a mismatch of the security binding between the client and the server.
```

<span data-ttu-id="3c00d-119">設定ダイアログ ボックスで正しい SOAP ホスト名を指定したと仮定する場合、テスト ツールがインストールされているクライアント コンピューターで、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-119">Assuming that you have specified the correct SOAP hostname in the settings dialog box, run the following PowerShell scripts on your client computer where the test tool is installed.</span></span>

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false

if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))  { Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false}
```

<span data-ttu-id="3c00d-120">レジストリ キーを手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3c00d-120">You can also manually set the registry keys.</span></span>

### <a name="cannot-enumerate-error"></a><span data-ttu-id="3c00d-121">エラーを列挙できません</span><span class="sxs-lookup"><span data-stu-id="3c00d-121">Cannot enumerate error</span></span>

<span data-ttu-id="3c00d-122">テスト ケースを実行すると、次のエラーが表示される場合があります。エラーの詳細には、次のメッセージが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-122">You may receive the following error when running a test case, or the error details may contain the following messages.</span></span>

```Text
<Message>The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</Message>
<Message>Could not enumerate AX users</Message>  (InnerError)`
```

![エラー メッセージ列挙ボックス](media/cannot-enumerate.png)
 
<span data-ttu-id="3c00d-124">このエラーを解決するには、RSAT の設定ダイアログ ボックスで指定されている **管理ユーザー名** を確認します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-124">To resolve this error, verify the **Admin user name** specified in the RSAT settings dialog box.</span></span> <span data-ttu-id="3c00d-125">**管理者ユーザー名**は、RSAT が接続している環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-125">The **Admin user name** must be the email address of a user that belongs to the System Administrator role on the environment that RSAT is connecting to.</span></span>

## <a name="browser"></a><span data-ttu-id="3c00d-126">ブラウザー</span><span class="sxs-lookup"><span data-stu-id="3c00d-126">Browser</span></span>

<span data-ttu-id="3c00d-127">Active Directory のセキュリティ設定が原因で、Chrome ブラウザーが Regression Suite Automation Tool で機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c00d-127">The Chrome browser may not work with the Regression suite automation tool due to your Active Directory security settings.</span></span> <span data-ttu-id="3c00d-128">この場合は、Internet Explorer ブラウザーを使用するように設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="3c00d-128">In this case, change your settings to use an Internet Explorer browser.</span></span>

## <a name="excel-data-tabs"></a><span data-ttu-id="3c00d-129">Excel のデータ タブ</span><span class="sxs-lookup"><span data-stu-id="3c00d-129">Excel data tabs</span></span>

<span data-ttu-id="3c00d-130">Microsoft Excel データ タブには、データ変数のシステム識別子が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c00d-130">Microsoft Excel data tabs display the system identifiers for data variables.</span></span> <span data-ttu-id="3c00d-131">Excel では、表示フレンドリ名は表示されません。</span><span class="sxs-lookup"><span data-stu-id="3c00d-131">Excel does not display friendly names.</span></span>

##  <a name="validating-blank-dates"></a><span data-ttu-id="3c00d-132">空白日付の検証</span><span class="sxs-lookup"><span data-stu-id="3c00d-132">Validating blank dates</span></span>
<span data-ttu-id="3c00d-133">日付/時刻の特定のコントロールが空白であることを確認する必要があるテスト ケースの場合は、"01/01/1900" というコントロールに対応する Excel のセルに次の値を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="3c00d-133">If your test case requires validation that a certain control of type Date/Time is blank, you can insert the following value into the Excel cell corresponding to this control: “01/01/1900”.</span></span>   

