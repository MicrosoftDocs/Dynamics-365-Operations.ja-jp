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
ms.openlocfilehash: b3915097b6f70cc1b2df91fdbfeb39bf51c7a0f6
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914758"
---
# <a name="troubleshoot-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool のトラブルシューティング 

[!include [banner](../../includes/banner.md)]

このトピックでは、Regression Suite Automation Tool (RSAT) のトラブルシューティング方法について説明します。

## <a name="playback-logs"></a>再生ログ

再生中にツールの問題のトラブルシューティングを行うには、**C:\Users\$YourUserName\AppData\Roaming\regressionTool\playback\[TestName]Log.txt** にある開発者エラー ログを開きます。 エラーメッセージを分析して、エラーが発生する可能性がある原因を特定します。

## <a name="authentication-certificate-and-installation"></a>認証証明書およびインストール

+ 認証証明書は、RSAT がインストールされているのと同じコンピューター上の管理者によって作成およびインストールされる必要があります。 管理者によって作成されていない場合は、テスト ケースを実行しようとすると次のエラー メッセージが表示されます。  
  ```
  Cannot access Finance and Operations environment. Verify your settings and make sure the environment is available.
  ```
+ 同じコンピューターで以前のバージョンの RSAT を使用した場合は、新しいバージョンをインストールする前に、そのバージョンを閉じてアンインストールしてください。

## <a name="screen-resolution"></a>画面の解像度

テストを正常に実行するには、デスクトップの解像度を 100% に設定する必要があります。 設定を変更するには、次の図に示すように、Windows の **ディスプレイ設定 > 拡大縮小とレイアウト** を使用します。

![画面の解像度の設定](media/screen-resolution.png)
 
## <a name="test-playback-errors"></a>再生エラーのテスト

### <a name="soap-or-http-request-errors"></a>SOAP または HTTP 要求のエラー

スタンダード承認テスト サンドボックス環境 (Tier2) またはその他のマルチ ボックス環境に対してテストしている場合は、テストの実行時に次のいずれかのエラーが表示されることがあります。

```
There was no endpoint listening at https://<yourURL>soap.sandbox.operations.dynamics.com/Services/AxUserManagement/Service.svc/ws2007FedHttp that could accept the message. This is often caused by an incorrect address or SOAP action…

An error occurred while making the HTTP request to <Hostname>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused by a mismatch of the security binding between the client and the server.
```

設定ダイアログ ボックスで正しい SOAP ホスト名を指定したと仮定する場合、テスト ツールがインストールされているクライアント コンピューターで、次の PowerShell スクリプトを実行します。

```PowerShell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false

if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))  { Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false}
```

レジストリ キーを手動で設定することもできます。

### <a name="cannot-enumerate-error"></a>エラーを列挙できません

テスト ケースを実行すると、次のエラーが表示される場合があります。エラーの詳細には、次のメッセージが含まれている場合があります。

```
<Message>The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception.</Message>
<Message>Could not enumerate AX users</Message>  (InnerError)`
```

![エラー メッセージ列挙ボックス](media/cannot-enumerate.png)
 
このエラーを解決するには、RSAT の設定ダイアログ ボックスで指定されている **管理ユーザー名** を確認します。 **管理ユーザー名**は、RSAT が接続している Finance and Operations 環境のシステム管理者ロールに属するユーザーの電子メール アドレスである必要があります。

## <a name="browser"></a>ブラウザー

Active Directory のセキュリティ設定が原因で、Chrome ブラウザーが Regression Suite Automation Tool で機能しない場合があります。 この場合は、Internet Explorer ブラウザーを使用するように設定を変更します。

## <a name="excel-data-tabs"></a>Excel のデータ タブ

Microsoft Excel データ タブには、データ変数のシステム識別子が表示されます。 Excel では、表示フレンドリ名は表示されません。

##  <a name="validating-blank-dates"></a>空白日付の検証
日付/時刻の特定のコントロールが空白であることを確認する必要があるテスト ケースの場合は、"01/01/1900" というコントロールに対応する Excel のセルに次の値を挿入できます。   

