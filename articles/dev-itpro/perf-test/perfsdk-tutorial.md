---
title: "パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト"
description: "このトピックでは、Performance SDK について説明し、Visual Studio Online を使用してマルチユーザー テストを行う方法を示します。"
author: jujoh
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f2e3a40f58b57785079e1940b2d24a3598a3ad1b
ms.openlocfilehash: a67ba9129c8c6aed252da83d0018358868da97b7
ms.contentlocale: ja-jp
ms.lasthandoff: 07/09/2018

---

# <a name="performance-sdk-and-multiuser-testing-via-visual-studio-online"></a>パフォーマンス SDK および Visual Studio Online を介したマルチ ユーザー テスト

[!include [banner](../includes/banner.md)]

このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) について説明し、Microsoft Visual Studio Online を使用してマルチユーザー テストを実行する方法について説明します。 また、タスク レコーダーで記録したシナリオをシングルユーザー テスト、そしてマルチユーザー テストに変換する方法についても説明します。

> [!NOTE]
> 管理者として環境を利用できる必要があります。 詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。

## <a name="prerequisites"></a>前提条件

- Microsoft Visual Studio 2015 Enterprise
- 数量データを含むデプロイメント
- パフォーマンス SDK (SDK は K:\\PerfSDK\\PerfSDKLocalDirectory にある可能性があります。 ただし、環境によっては C:\\PerfSDK にある可能性があります。)

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a>XML 記録からシングル ユーザー C# テストを作成する

<!--To view a video that shows how to create a single-user test, go to [https://mix.office.com/watch/qtdlasy2rcf3](https://mix.office.com/watch/qtdlasy2rcf3).-->

1. タスク レコーダーを使用して、テストするシナリオの記録を作成します。 

    > [!IMPORTANT]
    > 既定のダッシュ ボード ページでレコードが起動しない場合、テストを実行することはできません。

2. Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。 このプロジェクトは **PerfSDK** フォルダーにあります。 プロジェクトを既に構築している場合、この手順を省略します。
3. **Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。
4. **タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート**を選択します。

    [![インポート タスク記録 ダイアログ ボックス](./media/perf103a.png)](./media/perf103a.png)

    C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。

## <a name="run-a-single-user-performance-test-by-using-the-performance-sdk"></a>パフォーマンス SDK を使用して単一ユーザー パフォーマンス テストを実行

1. Microsoft Windows のコントロール パネルで、**システムとセキュリティ** &gt; **システム** &gt; **システムの詳細設定**を選択します。 **TestRoot**環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。

    [![EnvironmentVariable](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)

2. [http://selenium-release.storage.googleapis.com/index.html?path=2.42/](http://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードします。
3. ファイルを抽出します。 動的リンク ライブラリ (DLL) を、**selenium-dotnet-strongnamed-2.42.0.zip\net40** フォルダから **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。  **IEDriverServer.exe** を、**IEDriverServer_Win32_2.42.0.zip** から **PerfSDK\\Common\\External\\Selenium** フォルダにもコピーします。

    [![PerfSDK\Common\External\Selenium フォルダーにある DLL](./media/perf103d.png)](./media/perf103d.png)

4. **PerfSDK\\Common\\External\\Selenium** フォルダーの **WebDriver.dll** への参照を、Visual Studio プロジェクトへ追加します。    

5. 証明書を生成しインストールします。 証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。 プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。

    ```
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    これらのコマンドでは次の要素を注意してください。

    - **-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。 この証明書の名前が **127.0.0.1** であることが非常に重要です。 それ以外の場合は、単一ユーザー テストは実行することはできません。
    - **-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。 証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。

    スクリプトの実行が終了した後、**c:\\Temp** で以下のファイルが表示されます。

    - authcert.pfx
    - authcert.cer 
    - authcert.pvk

6. **authcert.pfx** および **authcert.cer** 証明書ファイルをインストールします。 これらのファイルをインストールするときは、**ローカル コンピューター**をかならず選択します。 **authcert.pfx** ファイルを **PerfSDK** フォルダにコピーします。
7. 管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

8. **CloudEnvironment.Config** ファイルで、**SelfSigningCertificateThumbprint** キーの値として拇印を入力します。

    [![更新された CloudEnvironment.Config ファイル](./media/config-thumbprint.jpg)](./media/config-thumbprint.jpg)

9. **wif.config** ファイルを更新して Application Object Server (AOS) が証明書を信頼できるようにするには、これらの手順に従います。

    1. Microsoft インターネット インフォメーション サービス (IIS) を起動し、サイトの一覧で **Microsoft Dynamics 365 for Finance and Operations** を見つけます。
    2. **エクスプローラー** を選択して、**wif.config** ファイルを検索します。

        [![wif.config ファイル](./media/wifconfig.jpg)](./media/wifconfig.jpg)

    3. **Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。 この権限の捺印のリストに捺印を追加する必要があります。

        [![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)

    4. IIS を再起動します。

10. Visual Studio で、**PerfSDKSample** プロジェクトを開き、**PurchaseReq.cs** ファイルを検索します。 このファイルは、サンプル シングルユーザー テストです。 ファイルで、次の行をコメントアウトします。

    ```
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    [![PurchaseReq.cs でコメント アウトされた行](./media/perf103e.png)](./media/perf103e.png)

11. 管理者のユーザー名を入力することによって **CloudEnvironment.Config** ファイルを変更します。 次に例を示します。

    > [!NOTE]
    > **ConfigName** は **DEVFABRIC** に設定する必要があります。 

    [![変更された CloudEnvironment.Config ファイル](./media/PerfSDKCloudEnvironmentAdminUser.PNG)](./media/PerfSDKCloudEnvironmentAdminUser.PNG) 

12. **CloudEnvironment.Config** ファイルに、エンドポイントを入力します。

    > [!NOTE]
    > 環境をアプリケーション リクエスト ルーティング (ARR) に対して有効にするには、2 つのエンドポイントがあります。 次に例を示します。
    >
    > - apr-arr8aos**soap**.axcloud.test.dynamics.com
    > - apr-arr8aos.axcloud.test.dynamics.com
    >
    > この場合、CloudEnvironment.Config ファイルに両方のエンドポイントを入力する必要があります。
    >
    > [![CloudEnvironment.Config のエンドポイント](./media/perf103upd.png)](./media/perf103upd.png)

13. **テスト** &gt; **テストの設定** を選択し、**既定のプロセッサ アーキテクチャ** を **x64** に設定してソリューションをビルドします。
14. **テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。

    > [!NOTE]
    > 場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。 この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。

    新しいテストに **TestMethod** という名前が付けられます。 TestMethod のメソッド名を変更すると、個々の名前がテストに表示されます。 

テストを実行できるようになりました。 テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。

## <a name="create-a-multiuser-test-from-a-single-user-test"></a>シングル ユーザー テストからマルチ ユーザー テストを作成する

以前のセクションで情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。 テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。

```
Client = DispatchedClient.DefaultInstance;
```

その行を以下の行に置き換えます。

```
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

タスクのインポーターによって生成されたテスト スクリプトには次の明細行と似ている明細行が含まれている場合があります。

```
UserContextRole _context = new UserContextRole(UserManagement.AdminUser);
```

ロード テストとして実行される任意のテストからこの明細行を削除します。 このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。

タスク記録が行われたときに入力した値がランダム化されていることを確認します。 テスト データを生成するために、データ拡張ツールを最初に使用することが必要な可能性があります。

## <a name="set-up-visual-studio-team-services-for-multiuser-testing"></a>Visual Studio Team Services でマルチ ユーザー テストを設定

この例では、ユーザーは ProcureToPay.cs ファイルを使用します。 Visual Studio を開始するには、[Visual Studio Team Services portal ポータル](https://app.vssps.visualstudio.com/profile/view) にサインインし、**Visual Studio で開く**を選択する必要があります。

> [!NOTE]
> このステップは 1 回のみ完了する必要があります。 Visual Studio Team Services にサインインした後、設定が保存されます。

[![Visual Studio で開きます](./media/vsonline-5-1024x323.jpg)](./media/vsonline-5.jpg)

1. **PerfSDKSample** プロジェクトを開きます。
2. **CloudEnvironment.Config** ファイルで、**UserFormat** エントリを更新して、管理者ユーザー URL を反映します。 たとえば、`admin@example.com` に対して、ユーザー形式として **TST\_{0}@example.com** を使用します。 また、**UserCount** 値をパフォーマンス テストに含めるユーザーの数に変更します。

    [![更新された CloudEnvironment.Config ファイル](./media/PerfSDKUserFormatExample.PNG)](./media/PerfSDKUserFormatExample.PNG)

3. 管理者モードでコマンド プロンプトを開き、**PerfSDK** フォルダーに移動します。 次のコマンドを実行して環境のテスト ユーザーを作成します。

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

    必要な数のユーザーを作成することができます。 たとえば、次のコマンドは、USMF 会社で 150 人のテスト ユーザーを作成します。

    ```
    MS.Dynamics.Performance.CreateUsers.exe 150 USMF
    ```

4. 管理者ユーザーとしてエンドポイントにログインし、ユーザーがシステムで作成されたことを確認します。

### <a name="test-the-sandbox-environment"></a>サンドボックス環境をテスト

ここまでは、手順で、AOS マシンが開発マシンでもある開発者トポロジを使用していることを前提としていました。 Visual Studio Team Services でロード テストを実行するには、テスト環境がサンドボックス環境である必要があります。 サンドボックス環境と負荷テストを実行するコンピューター間の信頼関係を確立するには、いくつかの追加手順を完了する必要があります。 負荷テストを実行するコンピューターは、開発マシンまたは Visual Studio Online で作成されたテスト エージェントのいずれかです。

1. サンドボックス AOS マシンへのリモート デスクトップ の接続を確立し、**.cer** ファイルを上書きします。 ファイルをダブルクリックして、インストールします。 証明書ストアの入力を要求するメッセージが表示されたら、**個人** を選択します。
2. IIS を起動し、サイトの一覧で **AOSService** を見つけます。 その後、**エクスプローラー** を選択して、**wif.config** ファイルを検索します。 **Wif.config** ファイルで、**AxTokenIssuer** という機関を検索します。 この権限の捺印のリストに捺印を追加する必要があります。 (以前に生成した証明書の値を使用します。)

    [![拇印を AxTokenIssuer の機関一覧に追加](./media/PerfSDKUpdatedWifConfig.PNG)](./media/PerfSDKUpdatedWifConfig.PNG)

3. IIS を再起動します。

トポロジに対してパフォーマンス テストを実行することができるようになりました。

> [!NOTE]
> トポロジに複数の AOS マシンがある場合、証明書をインストールして、各 AOS マシンの wif.config ファイルを更新する必要があります。

## <a name="run-the-performance-test"></a>パフォーマンス テストの実行

1. Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

2. [https://www.microsoft.com/en-us/download/details.aspx?id=50420](https://www.microsoft.com/en-us/download/details.aspx?id=50420)から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。 (64 ビット バージョンの .msi ファイルを選択します。) ファイルを **PerfSDK** ディレクトリの **Visual Studio Online** フォルダーに配置します。
3. **Visual Studio Online** フォルダで **setup.cmd** ファイルの内容を変更し、次のコードと一致するようにします。

    ```
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

4. **CloudCtuFakeACSInstall.cmd** ファイルの内容を変更して、**インポート**コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。 スクリプトの 3 行目は、次の行に似ているはずです。

    ```
    set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....
    ```

5. ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。
6. **テストの設定**ダイアログ ボックスの**配置**タブで、次の設定を使用します。

    - **展開の有効化** チェック ボックスをオンにします。
    - **配置する追加のファイルやディレクトリ** フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。

        - &lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\
        - C:\\PerfSDK\\CloudEnvironment.Config
        - C:\\PerfSDK\\authcert.pfx
        - C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config
        - C:\\PerfSDK\\Visual Studio Online\\

        [![フィールドを配置するための追加ファイルおよびディレクトリ](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)

        > [!NOTE]
        > PerfSDK フォルダーが異なっている場合があります。

7. **スクリプトの設定とクリーンアップ**タブで、**PerfSDK** ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** ファイルを選択します。
8. **追加設定**タブで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行**を選択します。
9. テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。

    [![負荷テストの実行](./media/perf103u.png)](./media/perf103u.png)

    テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。 次に例を示します。

    [![トランザクションの結果](./media/perf103v.png)](./media/perf103v.png)

10. テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。

    [![グラフ 表示](./media/perf103w.png)](./media/perf103w.png)

    > [!NOTE]
    > テストの実行中、システムに関する情報はこのビューで利用することができません。 この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。 または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="no-client-was-opened-in-the-time-out-period"></a>タイムアウト期間中クライアントが開かれていません
この問題はシングル ユーザー テストにのみ影響します。 テストが実行されているとき、Web クライアントを開きますが、Web サイトが読み込まれることはありません。 代わりに、白い画面を持つ空の Web クライアントがある場合、ページの上部で次のメッセージが表示されます: 「これは WebDriver サーバーの初期開始ページです。」 テストは最終的にタイム アウトおよび失敗し、エラー メッセージが表示されます。

#### <a name="error-example"></a>エラーの例

```
Initialization method <Test class name>.TestSetup threw exception. System.TimeoutException: System.TimeoutException: No client was opened in the timeout period.
```

#### <a name="solution"></a>ソリューション
このトピックの「パフォーマンス SDK を使用してシングル ユーザー パフォーマンス テストを実行する」セクションの、手順 4 から 8 を実行します。 そのセクションでは、このタイプのテストの正しい証明書を作成する方法について説明します。 証明書のサムプリントを wif.config ファイルに追加する方法についても説明します。

### <a name="zoom-factor"></a>ズーム係数

この問題はシングル ユーザー テストにのみ影響します。 

#### <a name="error-example"></a>エラーの例

```
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```

#### <a name="solution"></a>ソリューション

Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。

- コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup = 0
- コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\ResetZoomOnStartup2 = 0
- コンピュータ\\HKEY\_現在\_ユーザー\\ソフトウェア\\Microsoft\\Internet Explorer\\ズーム\\Zoomfactor = 80000
 
使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更**を選択する必要があります。 このフィールドは、Windows の**表示設定**で使用できます。 
 
これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。

### <a name="certificate-thumbprint-errors"></a>証明書の拇印のエラー

#### <a name="error-example"></a>エラーの例

```
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a>ソリューション

次のいくつかの理由でエラー メッセージを受け取る可能性があります。

- CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。 拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。 たとえば、[https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/) で使用可能な Unicode コンバーターを使用できます。

    ![Unicode コードの変換](./media/sdk_unicode_code_converter.jpg)
 
- 証明書が AOS マシンにインストールされていません。 AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=<name of your certificate>" }
    ```

    スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。 問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。
 
- 負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。 CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。
 
    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード](./media/set_cloudctufakeacsinstall.jpg)
 
### <a name="no-endpoint-is-listening"></a>リッスンしているエンドポイントはありません

この問題は、シングルユーザーまたはマルチユーザーのテストを実行する場合、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成する場合に発生する可能性があります。

#### <a name="error-example"></a>エラーの例

テストまたはユーザー作成プロセスが失敗し、次のエラー メッセージが表示されます。

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a>ソリューション

この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。
 
CloudEnvironment.Config ファイルで、次のキーによって指定されている値を確認します。

- &lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;
- &lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;

これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。 開発者マシンの Web ブラウザで、**HostName** キーによって指定された Web アドレスを開けれることを確認します。

オンライン負荷テストでは、CloudEnvironment.Config ファイルの **HostName** キーで指定された環境に、どのマシンからも公にアクセスできる必要があります。 したがって、1 ボックス環境をテストする必要がある場合、Visual Studio Online を使用して負荷テストを実行することはできません。これは、エンドポイントが 1 ボックス環境の外部にアクセスできないためです。

### <a name="users-cant-be-enumerated"></a>ユーザーを列挙できません

この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。

#### <a name="error-example"></a>エラーの例

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a>ソリューション

2 つのシナリオで、このエラーが発生することがあります。

- CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーはシステム管理者ロールを持っている必要があります。 この問題は、**SelfMintingAdminUser** として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。 適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。

    ![管理者ユーザー](./media/sdk_admin.png)

- CloudEnvironment.config ファイルで **SelfMintingAdminUser** として指定されたユーザーは、`"<https://sts.windows-ppe.net/>"` または `"<https://sts.windows.net/>"` 以外の**プロバイダー**を持ちます。 場合によっては、管理者ユーザーの**プロバイダ**フィールドに会社固有のドメインを含めます。 この問題を回避するには、Finance and Operations で、任意の名前と電子メール アドレスを持つユーザーを作成します。 システム管理者ロールを新しいユーザーに割り当てます。 ユーザーを実在の Azure Active Directory ユーザーにリンクする必要はありません。 CloudEnvironment.config ファイルで、この新しい管理者ユーザーを **SelfMintingAdminUser** として指定します。

### <a name="the-http-request-was-forbidden-with-client-authentication-scheme-anonymous"></a>クライアント認証方式「Anonymous」によって HTTP 要求が禁止されました

#### <a name="error-example"></a>エラーの例

```
Initialization method <Test class name>.TestSetup threw exception. System.ServiceModel.Security.MessageSecurityException: System.ServiceModel.Security.MessageSecurityException: The HTTP request was forbidden with client authentication scheme 'Anonymous'. ---> System.Net.WebException: The remote server returned an error: (403) Forbidden..
```

#### <a name="solution"></a>ソリューション

既知の 2 つのシナリオでは、このエラーが発生することがあります。

- テスト ユーザーは、引数なしで MS.Dynamics.Performance.CreateUsers.exe を実行して作成されます。 次に例を示します。

    ```
    MS.Dynamics.Performance.CreateUsers.exe
    ```

    CreateUsers スクリプトを引数なしで実行すると、作成されたテスト ユーザーの電子メール アドレスは正しくフォーマットされません。 これらのユーザーを使用してテストを実行すると、テストは禁止された要求のエラーを生成します。 このシナリオがエラーの原因であることを確認するには、Microsoft Dynamics 365 for Finance and Operations でユーザーを表示します テスト ユーザーの正しくない電子メール アドレスは、次の図の電子メール アドレスに類似します。

    [![電子メール アドレスの設定が正しくない](./media/PerfSDKBadUserFormat.PNG)](./media/PerfSDKBadUserFormat.PNG)

    問題を解決するには、電子メール アドレスの書式設定が誤っているテスト ユーザーを削除します。 CreateUsers スクリプトを再実行し、次のようにしてユーザー数および会社を指定します。

    ```
    MS.Dynamics.Performance.CreateUsers.exe [UserCount] [CompanyCode]
    ```

- CloudEnvironment.Config ファイルの **UserCount** フィールドで指定したユーザー数が、MS.Dynamics.Performance.CreateUsers.exe を実行して作成したテスト ユーザーの数を超えます。 少なくとも CloudEnvironment.Config ファイルで要求するテスト ユーザーをできる限り多く作成したことを確認します。
 
    ![クラウド環境のコンフィギュレーション](./media/cloud-env-config.png)

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a>メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。 AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。 

#### <a name="error-example"></a>エラーの例

```
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a>ソリューション

この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。 2 つの原因が考えられます。

- 証明書が AOS マシンにインストールされていません。 問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、インストールします。
- 証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。 問題を解決するには、wif.config ファイルに証明書を追加する方法について、「パフォーマンス SDK を使用してシングル ユーザーのパフォーマンス テストを実行する」の手順 8 を参照してください。 wif.config ファイルを変更した後は、必ず IIS を再起動してください。
 
### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています

この問題は、通常、ロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例

```
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a>ソリューション

この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。 テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあるかどうかを確認します。 

&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。
 
> [!IMPORTANT]
> 非常に似た名前を持つ 2 つのファイルがあります。 1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。
 
### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a>CloudEnvironment.Config が配置項目で見つかりません

この問題は、通常、ロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例

```
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a>ソリューション

この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。 この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。 テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあるかどうかを確認します。

&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。

![テスト設定](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a>InteractiveClientId は設定で指定されていませんでした

#### <a name="error-example"></a>エラーの例

```
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a>ソリューション

この問題は、**SelfSigningCertificateThumbprint** フィールドが CloudEnvironment.Config ファイルに空白のままになっている場合に発生します。 CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。

```
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a>リモート ホストは、既存の接続を強制的に終了した

#### <a name="error-example"></a>エラーの例

```
System.TypeInitializationException: System.TypeInitializationException: The type initializer for
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --->
System.ServiceModel.CommunicationException: An error occurred while making the HTTP request to
<Host name>/Services/AxUserManagement/Service.svc/ws2007FedHttp. This could be due to the fact 
that the server certificate is not configured properly with HTTP.SYS in the HTTPS case. This could also be caused 
by a mismatch of the security binding between the client and the server.** ---> System.Net.WebException: 
The underlying connection was closed: An unexpected error occurred on a send. ---> System.IO.IOException: 
Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host. ---> 
System.Net.Sockets.SocketException: An existing connection was forcibly closed by the remote host. 
```

#### <a name="solution"></a>ソリューション

開発コンピューターで次の Windows PowerShell スクリプトを実行します。

```
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="service-w3svc-was-not-found-on-computer"></a>コンピューターでサービス w3svc が見つかりませんでした

このエラーは、Visual Studio Online を使用してロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例
```
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a>ソリューション

この問題を解決する修正プログラムが利用可能です。 Microsoft サポート技術情報 (KB) 番号は 4095640 です。

