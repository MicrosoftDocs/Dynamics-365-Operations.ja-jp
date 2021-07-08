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
# <a name="troubleshooting-guide-for-testing-with-the-performance-sdk"></a>パフォーマンス SDK を使用したテストのトラブルシューティング ガイド

[!include [banner](../includes/banner.md)]

## <a name="no-client-was-opened-in-the-time-out-period"></a>タイムアウト期間中クライアントが開かれていません

この問題はシングル ユーザー テストにのみ影響します。 テストの過程で、Webクライアントが起動するが、Webサイトが表示されません。 webクライアントには何も表示されません。 次のメッセージがページの上部に表示されます。「これはWebDriverサーバーの既定のスタートページです」。 テストは最終的にタイム アウトの後に失敗し、エラー メッセージが表示されます。

### <a name="error---no-client-was-opened-in-the-time-out-period"></a>エラー - タイムアウト時間内にクライアントが開かれませんでした

> 初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。 TimeoutException: TimeoutException: タイムアウト時間内にクライアントが開かれませんでした。

### <a name="solution"></a>ソリューション

[パフォーマンス SDK を使用したマルチユーザー テスト](perfsdk-multi-user-testing.md) を参照してください。 リンク先セクションでは、このタイプのテストにおいて正しい証明書を作成する方法について説明しています。 証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。

## <a name="zoom-factor"></a>拡大率

この問題はシングル ユーザー テストにのみ影響します。

### <a name="error---zoom-factor"></a>エラー - ズーム係数

> 初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。 System.InvalidOperationException: System.InvalidOperationException: Internet Explorerで予期しないエラーが発生しました。 ブラウザーのズームレベルが200% に設定されていました。 ズームレベルは100%に設定してください。

### <a name="solution---zoom-factor"></a>ソリューション - ズーム係数

Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。

- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0
- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0
- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000

使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更** を選択する必要があります。 このフィールドは、 Microsoft Windows の **表示設定** で使用できます。

これらの手順が機能しない場合は、RDP セッションを開始する前に Internet Explorer で既定のズーム レベルが 100 % になるよう、リモート デスクトップのサイズを変更するようにします。

## <a name="certificate-thumbprint-errors"></a>証明書の拇印のエラー

### <a name="error-example---certificate-thumbprint-errors"></a>エラーの例 - 証明書の拇印のエラー

> 初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup** が例外をスローしました。 System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 --\> MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 拇印によるトークン作成用の証明書の検索に失敗しました: b4f01d2fc42718198852cd23957fc60a3e4bca2e.

### <a name="solution---certificate-thumbprint-errors"></a>ソリューション - 証明書の拇印のエラー

以下に挙げるいずれかの理由でエラー メッセージが表示される可能性があります。

- CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。 拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。 たとえば、 <https://r12a.github.io/apps/conversion/>にて提供されている Unicode コンバーターを使用できます。

    [![ユニコード変換](./media/troubleshoot-perf-sdk-01.jpg)](./media/troubleshoot-perf-sdk-01.jpg)

- アプリケーション オブジェクト サーバー マシン (AOS) に証明書が 正しくインストールされていません。 以下の Microsoft Windows PowerShell スクリプトを実行し、認証が必要となる証明書をAOSマシン内で検索します。

    ```Console
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書をインストールすることはできません。 この問題を修正するには、すべてのAOSマシンに .cerファイルをコピーしてインストールします。

- 負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。 CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。

    [![.cmd file のパスワード](./media/troubleshoot-perf-sdk-02.jpg)](./media/troubleshoot-perf-sdk-02.jpg)

## <a name="no-endpoint-is-listening"></a>リッスンしているエンドポイントはありません

この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。

### <a name="error-example---no-endpoint-is-listening"></a>エラーの例 - リッスンしているエンドポイントはありません

テスト、またはユーザー作成処理が失敗し、次のエラー メッセージが表示されます。

> System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> System.ServiceModel.EndpointNotFoundException: \\\<web address\> にてメッセージを受領することができるエンドポイント リスニングがありません。 この事象は、正しくないアドレスまたは SOAP アクションによって引き起こされることがあります。

### <a name="solution---no-endpoint-is-listening"></a>ソリューション - リッスンしているエンドポイントはありません

この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。

CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。

- \\\<ExecutionConfigurations Key="HostName" Value="\<web address of host\>" /\>
- \\\<ExecutionConfigurations Key="SoapHostName" Value="\<web address of SOAP\>" /\>

これらのキーに指定する Web アドレスは、現在テストを実施している環境である必要があります。 開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。

オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。 したがって、ワンボックス環境をテストする必要がある場合、Microsoft Visual Studio Online Online を使用して負荷テストを実行することはできません。これは、エンドポイントが ワンボックス環境の外部にアクセスできないためです。

## <a name="users-cant-be-enumerated"></a>ユーザーを列挙できません

この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。

### <a name="error-example---users-cant-be-enumerated"></a>エラーの例 - ユーザーを列挙できません

> System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> System.InvalidOperationException: AX のユーザーを列挙することができませんでした ---\> System.ServiceModel.FaultException'1\[System.ComponentModel.Win32Exception\]: 禁止されています

### <a name="solution---users-cant-be-enumerated"></a>ソリューション - ユーザーを列挙できません

3 つのシナリオで、このエラーが発生することがあります。

- CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーに、システム管理者ロールが割り当てられていません。 適切なユーザーが指定されていることを検証するには、エンドポイントにサインインし、ユーザーのロールを確認します。

    [![ユーザーページ](./media/troubleshoot-perf-sdk-03.jpg)](./media/troubleshoot-perf-sdk-03.jpg)

- CloudEnvironment.config ファイルにて **SelfMintingAdminUser** として指定されているユーザーは、 `https://sts.windows-ppe.net/` または `https://sts.windows.net/` 以外のプロバイダーを持っています。 場合によっては、管理者ユーザーの **プロバイダ** フィールドに会社固有のドメインを含めます。

- Finance and Operations アプリが 21Vianet に配置されている場合、**NetworkDomain="https://sts.chinacloudapi.cn/"** を **SelfMintingSysUser** および **SelfMintingAdminUser** で指定したことを確認してください。

この問題を回避するには、任意の名前と電子メール アドレスを持つユーザーを作成します。 **システム管理者** ロールを新しいユーザーに割り当てます。 ユーザーを実在の Microsoft Azure Active Directory (Azure AD) ユーザーにリンクする必要はありません。 CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。

## <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a>クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました

### <a name="error-example---the-http-request-was-forbidden"></a>エラーの例 - HTTP 要求が禁止されました

> 初期化メソッド \<Test class name\>.TestSetup が例外をスローしました。 System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: クライアント認証スキーム'Anonymous'でHTTP要求が禁止されました。 ---\> System.Net.WebException: リモートサーバーからエラーが返されました: (403) 許可されていません。

### <a name="solution---the-http-request-was-forbidden"></a>ソリューション - HTTP 要求が禁止されました

3 つの既知のシナリオで、このエラーが発生することがあります。

- テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。 例えば、CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスが正しくフォーマットされません。 これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。 このシナリオでユーザーを表示することによってエラーが発生することを確認できます。 テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。

    [![誤りのあるユーザーの電子メールアドレスの一覧](./media/troubleshoot-perf-sdk-04.jpg)](./media/troubleshoot-perf-sdk-04.jpg)

    問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。 CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を特定します。

- CloudEnvironment.Config ファイルの **UserCount** フィールドで指定しているユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えています。 少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。

    [![CloudEnvironment.config ファイル](./media/troubleshoot-perf-sdk-05.jpg)](./media/troubleshoot-perf-sdk-05.jpg)

- Finance and Operations アプリが 21Vianet に展開されている場合は、開発環境とパフォーマンス テスト環境が 10.0.11 以上のプラットフォーム更新にあることを確認してください。

## <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a>メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

この問題は、シングルユーザーテストまたはマルチユーザーのテストを行っている場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成している場合、AOSマシンが開発用のマシンと異なる場合に発生する可能性があります。

### <a name="error-example---at-least-one-security-token-in-the-message-could-not-be-validated"></a>エラーの例 - メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

> System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> System.ServiceModel.Security.MessageSecurityException: セキュリティで保護されていない、または正しく保護されていない障害を受信しました。 障害コードと詳細については、FaultException 内部を参照してください。 ---\> System.ServiceModel.FaultException: メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

### <a name="solution---at-least-one-security-token-in-the-message-could-not-be-validated"></a>ソリューション - メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。 2 つの原因が考えられます。

- 証明書が AOS マシンにインストールされていません。 この問題を修正するには、AOSマシンに .cerファイルをコピーしてインストールします。
- 証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。 この問題を修正するには、wifファイルに証明書を追加します。 Wifファイルを更新した後に、必ずMicrosoft インターネット インフォメーション サービス (IIS) を再起動してください。

## <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています

この問題は、通常、負荷 テストを実行する場合にのみ発生します。

### <a name="error-example---msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing"></a>エラーの例 - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が不足しています

> \<Test class name\>.TestSetup が例外をスローしました。 InvalidOperationException: InvalidOperationException: ServiceModelクライアント構成セクションに名前'ClientCommunicationManager'および契約'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager'を持つエンドポイント要素が見つかりませんでした。 これは、アプリケーションに対応する構成ファイルが見つからなかったか、またはこの名前と一致するエンドポイント要素がクライアント要素にて見つからないことが原因です。 SSystem.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors にて (ServiceEndpoint serviceEndpoint, String configurationName)

### <a name="solution---msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing"></a>ソリューション - MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が不足しています

この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。 テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。

\<solution path\>\\TestResults\\\<your test run\>\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。

非常に似た名前を持つ 2 つのファイルがあります。 一方は名前が \*.dll で終わるファイルで、もう一方は名前が \*.dll.configで終わるファイルです。 \*.dll.configファイルはテスト設定の配置項目に含まれている必要があります。

## <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a>CloudEnvironment.Config が配置項目で見つかりません

この問題は、通常、ロード テストを実行する場合にのみ発生します。

### <a name="error-example---cloudenvironmentconfig-is-missing"></a>エラーの例 - CloudEnvironment.Config が見つかりません

> 初期化メソッド \\\<Test class name\>.TestSetup が例外をスローしました。
System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> MS.Dynamics.TestTools.TestLogging.EvaluateException: アサートに失敗しました。 DateTime="10/13/2017 14:42:55" "'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。

### <a name="solution---cloudenvironmentconfig-is-missing"></a>ソリューション - CloudEnvironment.Config が見つかりません

この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。 一般的に、この問題は負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。 テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。

\<solution path\>\\TestResults\\\<your test run\>\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。

[![テスト設定 ダイアログ ボックスの 配置 タブ](./media/troubleshoot-perf-sdk-06.jpg)](./media/troubleshoot-perf-sdk-06.jpg)

## <a name="interactiveclientid-was-not-specified-in-the-settings"></a>InteractiveClientId が設定で指定されていませんでした

### <a name="error-example---interactiveclientid-was-not-specified-in-the-settings"></a>エラーの例 - InteractiveClientId が設定で指定されていませんでした

> 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' のタイプイニシャライザが例外をスローしました。 ---\> Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientIdが設定で指定されていませんでした。

### <a name="solution---interactiveclientid-was-not-specified-in-the-settings"></a>ソリューション - InteractiveClientId が設定で指定されていませんでした

この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。 CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。

```xml
\<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

## <a name="the-remote-host-forcibly-closed-an-existing-connection"></a>リモート ホストは、既存の接続を強制的に終了した

### <a name="error-example---the-remote-host-forcibly-closed-an-existing-connection"></a>エラーの例 - リモート ホストは、既存の接続を強制的に終了した

> System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> System.ServiceModel.CommunicationException: \\\<Host name\>/Services/AxUserManagement/Service.svc/ws2007FedHttp に HTTP 要求をした際にエラーが発生しました。 HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。 これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。 ---\> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。 ---\> System.IO.IOException: 転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。 ---\> System.Net.Sockets.SocketException: 既存の接続がリモートホストによって強制的に切断されました。

### <a name="solution---the-remote-host-forcibly-closed-an-existing-connection"></a>ソリューション - リモート ホストは、既存の接続を強制的に終了した

開発コンピューターで次の Windows PowerShell スクリプトを実行します。

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

## <a name="service-w3svc-was-not-found-on-computer"></a>コンピューターでサービス w3svc が見つかりませんでした

このエラーは Visual Studio Online を使用して負荷テストを実行する場合にのみ発生します。

### <a name="error-example---service-w3svc-was-not-found-on-computer"></a>エラーの例 - コンピューターでサービス w3svc が見つかりませんでした

> テストメソッド MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend が例外をスローしました。System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement'のタイプイニシャライザが例外をスローしました。 ---\> System.InvalidOperationException: コンピューターでサービス w3svc が見つかりませんでした ---\> System.ComponentModel.Win32Exception: 指定されたサービスは、インストールされたサービスに存在しません。

### <a name="solution---service-w3svc-was-not-found-on-computer"></a>ソリューション - コンピューターでサービス w3svc が見つかりませんでした

この問題を解決する修正プログラムが利用可能です。 Microsoft サポート技術情報 (KB) 番号は 4095640 です。

## <a name="the-file-iedriverserverexe-does-not-exist"></a>The file IEDriverServer.exe ファイルが存在しません。

この問題はシングル ユーザー テストにのみ影響します。

### <a name="error-example---the-file-iedriverserverexe-does-not-exist"></a>エラーの例 - IEDriverServer.exe ファイルが存在しません

> ファイル K:\\perfSDK\\PerfSDKLocalDirectory\\SampleProject\\TestResults\\Admin501201994c\_devae648d1909-1 2018-06-25 03\_40\_51\\Out\\Common\\External\\Selenium\\IEDriverServer.exe が存在しません。 ドライバーは、 `https://selenium-release.storage.googleapis.com/index.html`にてダウンロードできます。

### <a name="solution---the-file-iedriverserverexe-does-not-exist"></a>ソリューション - IEDriverServer.exe ファイルが存在しません

**\<Your\_PerfSDK\_Folder\>** にある **Common\\External\\Selenium** フォルダーを **\<Your\_PerfSDK\_Folder>\\SampleProject\\ PerfSDKSample\\bin\\Debug** フォルダーにコピーします。

## <a name="failed-finding-the-certificate-for-minting-tokens-by-thumbprint-your-certificate-thumbprint"></a>拇印によるトークン作成用の証明書の検索に失敗しました: \<your certificate thumbprint\>

### <a name="error-example---failed-finding-the-certificate-for-minting-tokens-by-thumbprint"></a>エラーの例 - 拇印によるトークン作成用の証明書の検索に失敗しました

[![エラーメッセージとエラースタックの追跡](./media/troubleshoot-perf-sdk-07.jpg)](./media/troubleshoot-perf-sdk-07.jpg)

### <a name="solution---failed-finding-the-certificate-for-minting-tokens-by-thumbprint"></a>ソリューション - 拇印によるトークン作成用の証明書の検索に失敗しました

生成された証明書は、サンドボックス環境内の各AOSマシンにインストールしてください。

## <a name="the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a>実行しようとしているアクションには、 Visual Studio チームサービスへの接続が必要です。

この問題はマルチ ユーザー テストにのみ影響します。

### <a name="error-example---the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a>エラーの例 - 実行しようとしているアクションには、Visual Studio チームサービスへの接続が必要です

[![エラーメッセージの詳細](./media/troubleshoot-perf-sdk-08.jpg)](./media/troubleshoot-perf-sdk-08.jpg)

### <a name="solution---the-action-you-are-trying-to-perform-requires-a-connection-to-visual-studio-team-services"></a>ソリューション - 実行しようとしているアクションには、Visual Studio チームサービスへの接続が必要です

Azure DevOps に接続するときは、**dev.azure.com/\<Azure\_DevOps\_Account\>** ではなく、古い URI 形式 (**\<Azure\_DevOps\_Account\>.visualstudio.com**) を使用します。 古いURIを使用して Azure DevOps を開き、 **Visual Studioで開く** を選択します。

## <a name="could-not-load-file-or-assembly-aoskerneldll-or-one-of-its-dependencies"></a>ファイルまたはアセンブリ 'aoskernel.dll' 、あるいは依存関係を読み込みできませんでした

このエラーはマルチ ユーザー テストにのみ影響します。

### <a name="error-example---could-not-load-file-or-assembly-aoskerneldll"></a>エラーの例 - ファイルまたはアセンブリ 'aoskernel.dll' を読み込むことができませんでした

[![エラーメッセージとエラースタックの追跡,デバッグの追跡](./media/troubleshoot-perf-sdk-09.jpg)](./media/troubleshoot-perf-sdk-09.jpg)

### <a name="solution---could-not-load-file-or-assembly-aoskerneldll"></a>ソリューション - ファイルまたはアセンブリ 'aoskernel.dll' を読み込むことができませんでした

プラットフォーム更新プログラム20 またはそれ以降が稼働している環境で、Open Database Connectivity (ODBC) ドライバ17が使用されていることを確認して下さい。

## <a name="azureactivedirectoryconfiguration-node-is-missing-in-cloudenvironmentconfig"></a>CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。

### <a name="error-example---azureactivedirectoryconfiguration-node-is-missing"></a>エラーの例 - AzureActiveDirectoryConfiguration ノードが見つかりません

> 初期化メソッド MS.Dynamics.Performance.Application.TaskRecorder.SalesOrderCreationAndConfirmationBase.TestSetup が例外をスローしました。 System.TypeInitializationException: System.TypeInitializationException: 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' のタイプイニシャライザが例外をスローしました。 ---\> System.Reflection.TargetInvocationException: 呼び出しのターゲットによって例外がスローされました。 ---\> System.MissingFieldException: CloudEnvironment.config 上で AzureActiveDirectoryConfiguration ノードが見つかりません。

### <a name="solution---azureactivedirectoryconfiguration-node-is-missing"></a>ソリューション - AzureActiveDirectoryConfiguration ノードが見つかりません

**"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.AadAuthenticator"** のすべてのインスタンスを、CloudEnvironment.config ファイルの **AuthenticatorConfigurationCollection** セクションにある **"MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator"** で置き換えます。

## <a name="multiple-warning-messages-before-and-after-multi-user-testing-that-uses-azure-devops"></a>Azure DevOpsを使用したマルチユーザーテストの開始前と後に複数の警告メッセージが表示される

### <a name="error-example---multiple-warning-messages-before-and-after-multi-user-testing"></a>エラーの例 - マルチユーザー テストの開始前と後に複数の警告メッセージが表示される

![負荷テストステータスの例](./media/troubleshoot-perf-sdk-10.jpg)

![負荷テスト結果の例](./media/troubleshoot-perf-sdk-11.jpg)]

### <a name="solution---multiple-warning-messages-before-and-after-multi-user-testing"></a>ソリューション - マルチユーザー テストの開始前と後に複数の警告メッセージが表示される

影響はありません。メッセージを無視しても問題ありません。

## <a name="the-type-or-namespace-name-xxxx-could-not-be-found-are-you-missing-a-using-directive-or-an-assembly-reference"></a>タイプまたは名前空間名 'xxxx' が見つかりませんでした (using ディレクティブまたはアセンブリ参照が不足していないかどうか確認してください)。

### <a name="error-example---the-type-or-namespace-name-xxxx-could-not-be-found"></a>エラーの例 - タイプまたは名前空間名 'xxxx' が見つかりませんでした

タイプまたは名前空間名 'InventTransferOrders' が見つかりませんでした (using ディレクティブまたはアセンブリ参照が不足していないかどうか確認してください)。

### <a name="solution---the-type-or-namespace-name-xxxx-could-not-be-found"></a>ソリューション - タイプまたは名前空間名 'xxxx' が見つかりませんでした

perfSDK を使用して出荷されたサンプル ソリューションは既に準備されており、パッケージの分割後に更新されていません。 この問題を解決するには、アセンブリ **MS.Dynamics.TestTools.DirectoryProxyLibrary.dll** を \<Service volume\>:\\PerfSDK\\PerfSDKLocalDirectory に参照として追加します。

## <a name="assembly-was-built-against-the-netframeworkversionv46-framework"></a>アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました

### <a name="error-example---assembly-was-built-against-the-netframeworkversionv46-framework"></a>エラーの例 - アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました

アセンブリ "MS.Dynamics.TestTools.DirectoryProxyLibrary, Version=7.0.0.0, Culture=neutral, PublicKeyToken=a7cf325ee2c8a9ff" which was built against the ".NETFramework,Version=v4.6" フレームワークに間接的な依存関係があるため、プライマリ参照 "MS.Dynamics.TestTools.ApplicationSuiteProxyLibrary" を解決できませんでした。 このバージョンは、現在対象のフレームワーク ".NETFramework,Version=v4.5" よりも新しいバージョンです。

### <a name="solution--assembly-was-built-against-the-netframeworkversionv46-framework"></a>ソリューション - アセンブリは、".NETFramework,Version=v4.6" フレームワークに対してビルドされました

プロパティ ウィンドウの **ターゲット フレームワーク** プロパティを .Net Framework 4.6 に変更します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
