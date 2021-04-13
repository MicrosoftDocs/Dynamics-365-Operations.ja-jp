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
ms.openlocfilehash: 9a2e98a93478f4bad1179d192f4ac8b68c141b9b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745179"
---
# <a name="troubleshoot-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool のトラブルシューティング

[!include [banner](../../includes/banner.md)]

このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。

## <a name="playback-logs"></a>再生ログ

テスト ケースの再生中に発生する問題のトラブル シューティングを行うには、**[RSAT の作業ディレクトリ]\\[テスト ケース ID]\\playback\\[TestName]Log.txt** にある開発者向けエラーログを開いてください。 RSAT の作業ディレクトリは、RSATの [設定] ダイアログで指定されているディレクトリです。
エラーメッセージを分析して、エラーが発生する可能性がある原因を特定します。

> [!NOTE]
> RSAT のバージョンが 1.210 よりも古い場合、ログは **C:\\ユーザー\\[YourUserName]\\AppData\\Roaming\\regressionTool\\playback\\[TestName]ログ .txt** に格納されます。

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

このエラーを解決するには、RSAT の設定ダイアログ ボックスで指定されている **管理ユーザー名** を確認します。 **管理者ユーザー名** は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。 また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。 たとえば、テスト環境のテナントが **contoso.com** 場合、管理ユーザーは **\@constoso.com** で終了する必要があります。

### <a name="unsecured-fault-exception"></a>セキュリティ保護されていな障害の例外

次のエラーでテスト ケースが一貫性なく失敗する場合は、通常、AOS 仮想マシン上の認証サムプリントの設定が不完全であることを示しています。

```Xml
<Message>An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail.</Message>
<Message>At least one security token in the message could not be validated.</Message>
```

通常このエラーは、RSAT が認証に使用している証明書を信頼するようにテスト環境が構成されていない場合に発生します。 (証明書は、RSAT の設定で指定された拇印によって識別されます。) たとえば、テスト環境の AOS 仮想マシンの wif.config ファイルに拇印が欠落している場合があります。 標準承認テスト環境 (Tier 2 以上) に対して実行している場合は、すべての AOS 仮想マシン上で認証拇印を構成していない場合があります。 すべての AOS マシン上の **wif.config** にサムプリントを適切に追加してください。 詳細については、[接続を信頼するようにテスト環境を構成する](rsat-install-configure.md#configure-the-test-environment-to-trust-the-connection) を参照してください。

このエラーは、RSAT がインストールされているクライアント コンピューターと Finance and Operations 環境との間で UTC 時間に不一致がある場合にも発生します。 これはまれなケースであり、管理者が UTC 時間を正しく構成していない場合にのみ発生します。 クライアント コンピューターと Finance and Operations 環境は異なるタイム ゾーンに設定できますが、認証メカニズムはこの比較に依存しているため、両方の環境の UTC 時間は一致している必要があります。

## <a name="google-chrome-browser"></a>Google Chrome ブラウザー

Active Directory のセキュリティ設定が原因で、Google Chrome ブラウザーが Regression Suite Automation Tool で機能しない場合があります。 この場合、新しい Microsoft Edge または Internet Explorer を使用するように RSAT 設定を変更し ます。

## <a name="validating-blank-dates"></a>空白日付の検証

日付/時刻の特定のコントロールが空白であることを確認する必要があるテスト ケースの場合は、このコントロールに対応する Excel のセルに次の値を挿入できます: 「01/01/1900」。

## <a name="azure-devops-connectivity"></a>Azure DevOps 接続

RSAT の設定で目的の Azure DevOps プロジェクトを選択すると、このエラーが表示される場合があります: 「構造のパス \<iteration path\> が無効です。 設定を確認してから、もう一度お試しください。」 このエラーを解決するには、Azure DevOps でプロジェクトを開き、テスト計画に移動します。 各テスト計画に定義されているイテレーション パスを確認します。 イテレーション パスがエラーで示されているものと似ている場合は、既存のイテレーション パスを削除し、テスト計画に新しいイテレーション パスを追加してから保存します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]