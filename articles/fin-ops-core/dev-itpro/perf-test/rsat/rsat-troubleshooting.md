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
ms.openlocfilehash: dc1a3fc262ec7254890d66ed967cb7ebd2b6fa64
ms.sourcegitcommit: 5cbb5c6c13075fcea220cbc5cc207366fe44268e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2020
ms.locfileid: "3387402"
---
# <a name="troubleshoot-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool のトラブルシューティング 

[!include [banner](../../includes/banner.md)]

このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。

## <a name="playback-logs"></a>再生ログ

テスト ケースの再生中に発生する問題のトラブル シューティングを行うには、**[RSAT の作業ディレクトリ]\\[テスト ケース ID]\\playback\\[TestName]Log.txt** にある開発者向けエラーログを開いてください。 RSAT の作業ディレクトリは、RSATの [設定] ダイアログで指定されているディレクトリです。
エラーメッセージを分析して、エラーが発生する可能性がある原因を特定します。

> [!NOTE]
> RSAT のバージョンが 1.210 よりも古い場合、ログは **C:\\ユーザー\\[YourUserName]\\AppData\\Roaming\\regressionTool\\playback\\[TestName]ログ .txt**に格納されます。

## <a name="generator-logs"></a>ジェネレーター ログ

テストの実行およびパラメータ ファイル生成時のエラーのトラブル シューティングを行うには、ジェネレーター ログ を有効にします。

RSAT のインストール フォルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) 配下にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。

```xml
<add key="LogGeneration" value="true" />
```

テストの実行ファイルが生成されると、ログファイルが **[RSATの作業ディレクトリ]\\[テストケースID]\\generatorLogs** 配下に生成されます。

> [!NOTE]
> RSAT のバージョンが 1.210 よりも古い場合、ログは **C:\\ユーザー\\[Username]\\AppData\\Roaming\\regressionTool\\generatorLogs** に生成されます。

## <a name="authentication-certificate-and-installation"></a>認証証明書およびインストール

+ 認証証明書は、RSAT がインストールされているのと同じコンピューター上の管理者によって作成およびインストールされる必要があります。 管理者によって作成されていない場合は、テスト ケースを実行しようとすると次のエラー メッセージが表示されます。  

```Plaintext
Cannot access Finance and Operations environment. Verify your settings and make sure the environment is available.
```

+ 同じコンピューターで以前のバージョンの RSAT を使用した場合は、新しいバージョンをインストールする前に、そのバージョンを閉じてアンインストールしてください。

## <a name="screen-resolution-when-using-internet-explorer"></a>Internet Explorer 使用時の画面解像度

ブラウザーに Internet Explorer を使用している場合、テストを正常に実行するには、デスクトップの解像度を100% に設定している必要があります。 設定を変更するには、次の図に示すように、Windows の **ディスプレイ設定 > 拡大縮小とレイアウト** を使用します。

![画面の解像度の設定](media/screen-resolution.png)
 
## <a name="test-playback-errors"></a>再生エラーのテスト

### <a name="soap-or-http-request-errors"></a>SOAP または HTTP 要求のエラー

スタンダード承認テスト サンドボックス環境 (Tier2) またはその他のマルチ ボックス環境に対してテストしている場合は、テストの実行時に次のいずれかのエラーが表示されることがあります。

```Plaintext
There was no endpoint listening at https://<yourURL>soap.sandbox.operations.dynamics.com/Services/AxUserManagement/Service.svc/ws2007FedHttp that could accept the message. This is often caused by an incorrect address or SOAP action…

An error occurred while making the HTTP request to <Hostname>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused by a mismatch of the security binding between the client and the server.
```

RSAT 設定ダイアログ ボックスで正しい SOAP ホスト名を指定したと仮定する場合、テスト ツールがインストールされているクライアント コンピューターで、次の PowerShell スクリプトを実行します。

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false

if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))  { Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false}
```

レジストリ キーを手動で設定することもできます。

### <a name="cannot-enumerate-ax-users-error"></a>AX ユーザーを列挙できないエラー

テスト ケースを実行すると、次のエラーが表示される場合があります。エラーの詳細には、次のメッセージが含まれている場合があります。

```Xml
<Message>The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</Message>
<Message>Could not enumerate AX users</Message>  (InnerError)`
```

![エラー メッセージ列挙ボックス](media/cannot-enumerate.png)
 
このエラーを解決するには、RSAT の設定ダイアログ ボックスで指定されている **管理ユーザー名** を確認します。 **管理者ユーザー名**は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。 また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。 たとえば、テスト環境のテナントが **contoso.com** 場合、管理ユーザーは **\@constoso.com** で終了する必要があります。

### <a name="unsecured-fault-exception"></a>セキュリティ保護されていな障害の例外

次のエラーでテスト ケースが一貫性なく失敗する場合は、通常、AOS 仮想マシン上の認証サムプリントの設定が不完全であることを示しています。

```Xml
<Message>An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail.</Message>
<Message>At least one security token in the message could not be validated.</Message>
```
通常、このエラーは、テスト ケースがスタンダード承認テスト環境 (Tier 2以上) に対して実行されていて、AOS 仮想マシン上で認証サムプリントを設定していない場合に発生します。 すべての AOS マシン上の **wif.config** にサムプリントを適切に追加してください。 詳細については、[接続を信頼するようにテスト環境を構成する](rsat-install-configure.md#configure-the-test-environment-to-trust-the-connection) を参照してください。

## <a name="google-chrome-browser"></a>Google Chrome ブラウザー

Active Directory のセキュリティ設定が原因で、Google Chrome ブラウザーが Regression Suite Automation Tool で機能しない場合があります。 この場合、新しい Microsoft Edge または Internet Explorer を使用するように RSAT 設定を変更し ます。

## <a name="excel-data-tabs"></a>Excel のデータ タブ

Microsoft Excel データ タブには、データ変数のシステム識別子が表示されます。 Excel では、表示フレンドリ名は表示されません。

##  <a name="validating-blank-dates"></a>空白日付の検証
日付/時刻の特定のコントロールが空白であることを確認する必要があるテスト ケースの場合は、"01/01/1900" というコントロールに対応する Excel のセルに次の値を挿入できます。

