---
title: オンプレミス環境でのパフォーマンス SDK およびマルチユーザー テスト
description: このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) を使用して、オンプレミス環境でマルチユーザー負荷テストを実行する方法について説明します。
author: hasaid
ms.date: 03/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: Platform update 19
ms.openlocfilehash: 6e5a0b191147e4f30415d4c6e9c8afafed84d362d8e1f17eaf1cd9f7f76ac7fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724317"
---
# <a name="performance-sdk-and-multiuser-testing-in-on-premises-environments"></a>オンプレミス環境でのパフォーマンス SDK およびマルチユーザー テスト

[!include [banner](../includes/banner.md)]

このトピックでは、パフォーマンス ソフトウェア開発キット (SDK) を使用して、オンプレミス環境でマルチユーザー負荷テストを実行する方法について説明します。

  > [!IMPORTANT]
  > Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。 将来的には、代替ソリューションに向けた推奨案の提案に取り組んでいきます。  
  >
  > - Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。 サポート サイクルが終了するまで継続して使用することができます。 
  >
  >  - クラウド ベースの負荷テストサービスをご利用の場合は、同サービスは2020 年 3 月 31 日までの間、継続してご利用いただけます。 それまでの間は、同サービスの全機能を継続してご利用いただけます。 また、オンプレミス負荷テストに切り替えることがも可能です。 
  >
  > 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。


## <a name="prerequisites"></a>必要条件

- 数量データのあるオンプレミス環境
- 以下の特性を持つ開発環境。

    - Microsoft Visual Studio Enterprise またはそれ以降のバージョンがインストールされています。
    - パフォーマンス SDK をインストールします。 (SDK は K:\\PerfSDK\\PerfSDKLocalDirectory にある可能性があります。 ただし、環境によっては C:\\PerfSDK のような別の場所にある可能性があります。)
    - オンプレミス環境は、Web ブラウザーでアクセスできます。 (オンプレミス環境と同じドメインに開発仮想マシン [VM]が、またはオンプレミス環境には、パブリックに登録済みのドメイン名がある場合があります。)

## <a name="create-a-single-user-c-test-from-an-xml-recording"></a>XML 記録からシングル ユーザー C# テストを作成する

1. タスク レコーダーを使用して、テストするシナリオの記録を作成します。

    > [!IMPORTANT]
    > タスク記録は、既定のダッシュボード ページで開始する必要があります。 それ以外の場合は、テストを実行することはできません。

2. Microsoft Visual Studio を管理者として起動し、**PerfSDKSample** プロジェクトをビルドします。 このプロジェクトは **PerfSDK** フォルダーにあります。 プロジェクトを既に構築している場合、この手順を省略します。
3. **Dynamics 365** &gt; **アドイン** &gt; **記録から C# パフォーマンス テストを作成** を選択します。
4. **タスクの記録をインポート** ダイアログ ボックスで、必要な詳細を入力し、**インポート** を選択します。

    [![インポート タスク記録 ダイアログ ボックス。](./media/perf103a.png)](./media/perf103a.png)

    C# テストは、選択したプロジェクトに対して生成されたフォルダーに生成されます。

    > [!NOTE]
    > コンパイルの問題を解決するために、生成されたテストは編集される必要があります。

## <a name="run-a-single-user-test-by-using-the-performance-sdk"></a>パフォーマンス SDK を使用して単一のユーザーテストを実行

### <a name="prepare-the-development-environment"></a>開発環境の準備
開発環境でこれらの手順に従います。

1. Microsoft Windows のコントロール パネルで、**システムとセキュリティ**  &gt; **システム** &gt; **システムの詳細設定** を選択します。 **TestRoot** 環境変数が PerfSDK フォルダーのパスに設定されていることを確認します。

    [![TestRoot 環境変数。](./media/EnvironmentVariable.PNG)](./media/EnvironmentVariable.PNG)

2. [https://selenium-release.storage.googleapis.com/index.html?path=2.42/](https://selenium-release.storage.googleapis.com/index.html?path=2.42/) から、**selenium-dotnet-strongnamed-2.42.0.zip** および **IEDriverServer\_Win32\_2.42.0.zip** ファイルをダウンロードし、ファイルを抽出します。
3. 動的リンク ライブラリ (DLL) を、**selenium-dotnet-strongnamed-2.42.0.zip\net40** フォルダから **PerfSDK\\Common\\External\\Selenium** フォルダにコピーします。 **IEDriverServer.exe** を **IEDriverServer\_Win32\_2.42.0.zip** から **PerfSDK\\Common\\External\\Selenium** フォルダーにもコピーします。

    [![PerfSDK\Common\External\Selenium フォルダーにある DLL。](./media/perf103d.png)](./media/perf103d.png)

4. テストの認証に使用する証明書を生成します。 証明書ファイルを生成するには、管理者として [コマンド プロンプト] ウィンドウを開き、次のコマンドを実行します。 プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。

    ```Console
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    これらのコマンドでは次の要素を注意してください。

    - **-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。 証明書の名前には、**127.0.0.1** が必要です。 それ以外の場合は、単一ユーザー テストは実行することはできません。
    - **-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。 証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。

    スクリプトの実行が終了した後、**c:\\Temp** で以下のファイルが表示されます。

    - authcert.pfx
    - authcert.cer
    - authcert.pvk

5. **authcert.pfx** 証明書ファイルをインストールします。 ファイルをインストールするときは、**ローカル コンピューター** を必ず選択します。
6. **authcert.pfx** ファイルを **PerfSDK** フォルダにコピーします。
7. 管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行してインストールされている証明書拇印を取得します。

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

8. Visual Studio で、**PerfSDK** フォルダにある **PerfSDKSample** プロジェクトを開きます。
9. Visual Studio プロジェクトでは **PerfSDK\\Common\\External\\Selenium** フォルダーで **WebDriver.dll** への参照を追加します。
10. **CloudEnvironment.Config** ファイルを開き、コンテンツを次のテンプレートに置き換えます。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <EnvironmentalConfigSettings xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <EnvironmentalConfigSettingsCollection>
            <EnvironmentalConfigSetting ConfigName="DEVFABRIC">
                <!-- NOTE: the HostName value needs to be specified -->
                <ExecutionConfigurations Key="HostName" Value="[yourD365FOdomain]/namespaces/AXSF" />
                <ExecutionConfigurations Key="SoapHostName" Value="[yourD365FOdomain]/namespaces/AXSF" />
                <ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="[ThumbprintFromPowerShell]" />
                <ExecutionConfigurations Key="AdminAuthenticatorConfigurationId" Value="SelfMintingAdminUser" />
                <ExecutionConfigurations Key="DefaultBrowser" Value="InternetExplorer" />
                <ExecutionConfigurations Key="FederationRealm" Value="spn:00000015-0000-0000-c000-000000000000" />
                <ExecutionConfigurations Key="DefaultDispatcher" Value="Microsoft.Dynamics.TestTools.Dispatcher.JsDispatcher, Microsoft.Dynamics.TestTools.Dispatcher.JsDispatcher" />
                <ExecutionConfigurationsNodes ConfigurationName="SVC">
                    <ConfigurationSpecificDetails Key="AppConfig" Value="DEVFABRIC.Config" />
                </ExecutionConfigurationsNodes>
                <ExecutionConfigurationsNodes ConfigurationName="PRF">
                    <ConfigurationSpecificDetails Key="IsAdfs" Value="True" />
                    <ConfigurationSpecificDetails Key="UserCount" Value="2" />
                    <ConfigurationSpecificDetails Key="UserFormat" Value="[AdminUserEmail]" />
                    <ConfigurationSpecificDetails Key="UserPassword" Value="[AdminUserPassword]" />
                    <ConfigurationSpecificDetails Key="UserRole" Value="-SYSADMIN-" />
                    <ConfigurationSpecificDetails Key="ThinkTime" Value="0" />
                    <ConfigurationSpecificDetails Key="Company" Value="USMF" />
                </ExecutionConfigurationsNodes>
            </EnvironmentalConfigSetting>
        </EnvironmentalConfigSettingsCollection>
        <AuthenticatorConfigurationCollection>
            <AuthenticatorConfiguration Id="SelfMintingRunnerUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <Credentials IsFromKeyVault="false" Username="daxrunneruser@daxmdsrunner.com" NetworkDomain="urn:Microsoft:Dynamics:Cloud:DaxRunner" />
            </AuthenticatorConfiguration>
            <AuthenticatorConfiguration Id="SelfMintingSysUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <Credentials IsFromKeyVault="false" Username="testuser@microsoft.com" />
            </AuthenticatorConfiguration>
            <AuthenticatorConfiguration Id="SelfMintingAdminUser" Class="MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator">
                <!-- NOTE: admin username needs to be specified -->
                <Credentials IsFromKeyVault="false" Username="[AdminUserEmail]" NetworkDomain="[AdfsUrl]" />
            </AuthenticatorConfiguration>
        </AuthenticatorConfigurationCollection>
    </EnvironmentalConfigSettings
    ```

11. **CloudEnvironment.Config** ファイルで、次のキーの値を指定します。 これらの値は、テンプレートの角かっこ内のプレース ホルダーの値を置き換えます。

    - **ホスト名** – オンプレミスへのアクセスに使用される URL を指定します。 URL は、**\[yourD365FOdomain\]/namespaces/AXSF** です。
    - **SoapHostName** –**HostName** に指定したものと同じ URL を指定します。
    - **SelfSigningCertificateThumbprint** – 手順 7 で Windows PowerShell から取得した拇印を指定します。
    - **UserFormat** – オンプレミス環境でシステム管理者の役割を持つユーザーの電子メール アドレスを指定します。 ユーザーは、Active Directory フェデレーション サービス (AD FS) ユーザーである必要があります。
    - **UserPassword** –  **UserFormat** に指定した電子メール アドレスのユーザーのパスワードを指定します。
    - **Username** – **UserFormat** に指定したものと同じ電子メール アドレスを指定してください。
    - **NetworkDomain** – AD FS ID プロバイダーの URL を指定します。 オンプレミス配置の **AXDB** データベースに対して次の SQL クエリを実行することにより、この値を見つけることができます。

        ```sql
        select NETWORKDOMAIN, NETWORKALIAS from USERINFO where NETWORKALIAS='[AdminUserEmail]'
        ```

### <a name="prepare-the-on-premises-environment"></a>オンプレミス環境の準備
オンプレミス配置の各アプリケーション オブジェクト サーバー (AOS) VM で以下の手順に従います。

1. このトピックの [開発環境の準備](#prepare-the-development-environment)セクションで作成した **authcert.cer** ファイルを AOS VM にコピーします。
2. **authcert.cer** 証明書ファイルをインストールします。 証明書をインストールするときは、**ローカル コンピューター** を必ず選択します。 証明書を **信頼済ルート証明機関** ストアに置くようにしてください。
3. **wif.config** ファイルをテキスト エディタで開きます。 ファイルのパスは、**C:\\ProgramData\\SF\\AOS1\\Fabric\\work\\Applications\\AXSFType\_App19\\AXSF.Code.1.0.20180717001108** のようになります。

    > [!NOTE]
    > ファイル パスでは、使用している AOS ノードによって AOS 番号 (この例では **AOS1**) が異なります。 さらに、**ProgramData** フォルダーは隠しフォルダーです。 したがって、ファイル エクスプローラーでフォルダを表示するには、非表示のアイテムを有効にする必要があります。

4. **wif.config** ファイルで、`https://fakeacs.accesscontrol.windows.net` という機関を検索します。 この権限に対する拇印の一覧で、[開発環境の準備](#prepare-the-development-environment)セクションで作成した証明書の拇印を追加します。 次の例では、4 番目の拇印が `https://fakeacs.accesscontrol.windows.net` 権限に追加されました。

    ```xml
    <authority name="https://fakeacs.accesscontrol.windows.net/">
        <keys>
            <add thumbprint="9567B0F32F4B312FEE44ACE88A9CAAA13B7FBB86" />
            <add thumbprint="B8F659E2FDD2A6811CD72BE753FF7ACB64351AC1" />
            <add thumbprint="B51C394E6EE9578D8C54AE0A9927D8B6DCEFF84B" />
            <add thumbprint="F9112DE3D4DE65CBE39601EBDC7FBB1F8F525DED" />
        </keys>
        <validIssuers>
            <add name="https://fakeacs.accesscontrol.windows.net/" />
        </validIssuers>
    </authority>
    ```

5. **AXService.exe.config** ファイルをテキスト エディタで開きます。 このファイルは、**wif.config** ファイルと同じディレクトリにあります。
6. **"Aos.AosRole"** の **AXService.exe.config** ファイルを検索します。 **"Aos.AosRole"** を含む行を次の行に置き換えます。

    ```xml
    <add key="Aos.AosRole" value="AosRoleUnknown" />
    ```

    > [!NOTE]
    > **AosRole** を **AosRoleUnknown** に設定すると、ユーザーごとの Web セッションの数の制限を無効にします。 負荷テストでは、単一のユーザーに対して多数のセッションが作成されるため、これは大規模なユーザー負荷で負荷テストを完了するために必要です。 負荷テストが完了したら、この値を **"AosRoleWeb"** にリセットします。


7. Service Fabric Explorer では、AOS ノードのための **コード** パッケージを検索し、省略記号ボタン (**...**) を選択し、アプリケーションを再起動させるため **再起動** を選択します。

    ![Service Fabric Explorer から Finance and Operations を再起動します。](./media/ServiceFabricExplorerRestart.png)

### <a name="run-the-single-user-test"></a>単一ユーザー テストを実行

1. **PerfSDKSample** プロジェクトで、**PurchaseReq.cs** ファイルを検索します。 このファイルは、サンプル シングルユーザー テストです。 ファイルで、次の行をコメントアウトします。

    ```csharp
    if (this.TestContext !=null)
    {
        timerProvider = new TimerProvider(this.TestContext);
    }
    ```

    [![PurchaseReq.cs でコメント アウトされた行。](./media/perf103e.png)](./media/perf103e.png)

2. **テスト** &gt; **テスト設定** を選択し、**既定のプロセッサ アーキテクチャ** フィールドを **x64** に設定して、ソリューションをビルドします。
3. **テスト** &gt; **Windows** &gt; **テスト エクスプローラー** を選択してテストの一覧を表示します。

    > [!NOTE]
    > 場合によっては、タスク記録からテスト スクリプトを作成した後、Visual Studio はテストの一覧を更新しない可能性があります。 この場合、Visual Studio を再起動して、テスト エクスプローラーを再度開きます。

4. **CreatePurchReq** を右クリックして、サンプル シングルユーザー テストを実行します。 または、タスク記録から作成したテストを実行することもできます。 テストを実行すると、Internet Explorer が起動されて、記録したシナリオが再生されるはずです。

## <a name="run-a-multiuser-load-test-by-using-the-performance-sdk"></a>パフォーマンス SDK を使用してマルチユーザー負荷テストを実行

### <a name="create-a-multiuser-test-from-a-single-user-test"></a>シングル ユーザー テストからマルチ ユーザー テストを作成する

このトピックの前半の情報を使用してシングルユーザー テストを作成した後は、マルチユーザー テストに変換することができます。 テスト スクリプトに **MS.Dynamics.TestTools.UIHelpers.Core;** を追加して、**TestSetup** メソッドで次の行を見つけます。

```csharp
Client = DispatchedClient.DefaultInstance;
```

その行を以下の行に置き換えます。

```csharp
DispatchedClientHelper helper = new DispatchedClientHelper();
Client = helper.GetClient();
```

タスクのインポーターによって生成されたテスト スクリプトには次の明細行と似ている明細行が含まれている場合があります。

```csharp
UserContextRole _context = new UserContextRole(UserManagement.AdminUser);
```

ロード テストとして実行される任意のテストからこの明細行を削除します。 このコードはシングル ユーザー テストにのみ必要であり、ロード テストのパフォーマンスに悪影響があります。

タスク記録が行われたときに入力した値がランダム化されていることを確認します。

### <a name="run-the-multiuser-load-test"></a>マルチユーザー負荷テストを実行

1. Visual Studio エディターで、**ProcureToPay.cs** ファイルを開き、**TestSetup** メソッドに次の行を追加します。

    ```csharp
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir"); 
    if (string.IsNullOrEmpty(testroot)) 
    {
        testroot = System.IO.Directory.GetCurrentDirectory(); 
    } 
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

2. [https://www.microsoft.com/download/details.aspx?id=50420](https://www.microsoft.com/download/details.aspx?id=50420)から、SQL サーバーの Microsoft ODBC ドライバー 13 のインストーラー (MSI) ファイルをダウンロードします。 (64 ビット バージョンの .msi ファイルを選択します。) ファイルを **PerfSDK** ディレクトリの **Visual Studio Online** フォルダーに配置します。
3. **Visual Studio Online** フォルダ内の **setup.cmd** ファイル内容を次のコードと一致するように変更します。

    ```Console
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

4. **CloudCtuFakeACSInstall.cmd** ファイルの内容を変更して、**インポート** コマンドに **'パスワード'** の代わりに空の文字列が入るようにします。 スクリプトの 3 行目は、次の行に似ているはずです。

    ```powershell
    set MyStoreInstallCmd= .... $pfxcert.Import('%TestCertPath%', '', 'Exportable,PersistKeySet')....
    ```

5. ソリューション ファイルで、テストの設定を変更する **vsonline.testsettings** ファイルをダブルクリックします。
6. **一般** タブの **テストの設定** ダイアログ ボックスで、**テストの実行場所** フィールドを **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** に設定します。
7. **配置** タブで、次の設定を使用します。

    - **展開の有効化** チェック ボックスをオンにします。
    - **配置する追加のファイルやディレクトリ** フィールドで、以下のファイルおよびディレクトリが表示されていることを確認します。

        - &lt;ソリューション ディレクトリ&gt;\\PerfSDKSample\\bin\\デバッグ\\
        - C:\\PerfSDK\\CloudEnvironment.Config
        - C:\\PerfSDK\\authcert.pfx
        - C:\\PerfSDK\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config
        - C:\\PerfSDK\\ Visual Studio Online\\

        [![フィールドを配置するための追加ファイルおよびディレクトリ。](./media/PerfSDKOnlineTestSettings.PNG)](./media/PerfSDKOnlineTestSettings.PNG)

        > [!NOTE]
        > PerfSDK フォルダーが異なっている場合があります。

8. **設定とクリーンアップ** タブで、 **PerfSDK** ディレクトリ内の **Visual Studio Online** フォルダーにある **setup.cmd** ファイルを選択します。
9. **ホスト** タブについて、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。
10. テストを実行するには、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。

    [![負荷テストを実行する。](./media/perf103u.png)](./media/perf103u.png)

    テストの実行が終了したら、トランザクションの結果を示す概要が表示されます。 次に例を示します。

    [![トランザクションの結果。](./media/perf103v.png)](./media/perf103v.png)

11. テスト コント ローラーとテスト シナリオのさまざまな指標を表示するには、**グラフ** ビューに切り替えます。

    [![グラフ表示。](./media/perf103w.png)](./media/perf103w.png)

    > [!NOTE]
    > テストの実行中、システムに関する情報はこのビューで利用することができません。 この情報にアクセスするには、Microsoft Dynamics Lifecycle Services (LCS) を使用して、AOS マシンの CPU およびメモリ使用量を監視する必要があります。 または、AOS マシンに直接 perfmon を設定して、Microsoft Azure ポータルを設定し、Microsoft SQL Server データベース トランザクションの単位 (DTU) の使用を監視することができます。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="zoom-factor"></a>ズーム係数

この問題はシングル ユーザー テストにのみ影響します。 

#### <a name="error-example"></a>エラーの例

```csharp
Initialization method <Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Unexpected error launching Internet Explorer. Browser zoom level was set to 200%. It should be set to 100% (NoSuchDriver).
```

#### <a name="solution"></a>ソリューション

Internet Explorer で、次のレジストリ キーを変更することにより、ズーム係数を 100% に変更できます。

- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup = 0
- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\ResetZoomOnStartup2 = 0
- Computer\\HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Internet Explorer\\Zoom\\Zoomfactor = 80000

使用されているローカル コンピューターのバージョンによっては、リモート デスクトップ プロトコル (RDP) セッションを開始する前に、**テキスト、アプリ、その他のアイテムのサイズを変更** を選択する必要があります。 このフィールドは、Windows の **表示設定** で使用できます。 

これらの手順が機能しない場合は、Internet Explorer での既定のズーム レベルが 100 % になるよう、RDP セッションを開始する前に、リモート デスクトップのサイズを変更するようにします。

### <a name="certificate-thumbprint-errors"></a>証明書の拇印のエラー

#### <a name="error-example"></a>エラーの例

```csharp
Initialization method MS.Dynamics.Performance.Application.TaskRecorder.TestRecord1Base.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 
'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. --> 
MS.Dynamics.TestTools.CloudCommonTestUtilities.Exceptions.WebAuthenticationException: 
Failed finding the certificate for minting tokens by thumbprint: b4f01d2fc42718198852cd23957fc60a3e4bca2e
```

#### <a name="solution"></a>ソリューション

次のいくつかの理由でエラー メッセージを受け取る可能性があります。

- CloudEnvironment.Config および wif.config ファイルにコピーした証明書の拇印には、非表示の Unicode 文字が含まれています。 拇印に非表示の Unicode 文字が含まれているかどうかを確認するには、Unicode コード コンバータに貼り付けて、**HTML/XML** フィールドに余分な文字が表示されているかどうかを確認します。 たとえば、[https://r12a.github.io/apps/conversion/](https://r12a.github.io/apps/conversion/) で使用可能な Unicode コンバーターを使用できます。

    ![Unicode コードの変換。](./media/sdk_unicode_code_converter.jpg)

- 証明書が AOS マシンに正しくインストールされていません。 AOS マシンで証明書が見つかることを確認するには、次の Windows PowerShell スクリプトを実行します。

    ```powershell
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    スクリプトの実行後に、拇印が Windows PowerShell コンソールに表示されない場合は、証明書を見つけることはできません。 問題を解決するには、このトピックで以前に作成した .cer ファイルをコピーして、AOS マシンにインストールします。

- 負荷テストを実行するときにこの問題が発生した場合、セットアップ スクリプトが .pfx ファイルを正しくインストールしていない可能性があります。 CloudCtuFakeACSInstall.cmd ファイルに指定されているパスワードが証明書が作成されたときに設定されたパスワードと一致していることを確認します。

    ![CloudCtuFakeACSInstall.cmd ファイルのパスワード。](./media/set_cloudctufakeacsinstall.jpg)

### <a name="no-endpoint-is-listening"></a>リッスンしているエンドポイントはありません

#### <a name="error-example"></a>エラーの例

テストが失敗すると、次のエラー メッセージが表示されます。

```csharp
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.EndpointNotFoundException: There was no endpoint listening at <web address> that could accept the message. This is often caused by an incorrect address or SOAP action. 
```

#### <a name="solution"></a>ソリューション

この問題は、CloudEnvironment.Config ファイルで指定されたホストに、テストの実行またはユーザーの作成を試みているマシンからアクセスできない場合に発生します。

CloudEnvironment.Config ファイルで、次のキーに対して指定されている値を確認します。

- &lt;ExecutionConfigurations キー ="HostName" 値 ="&lt;ホストの Web アドレス&gt;" /&gt;
- &lt;ExecutionConfigurations キー ="SoapHostName" 値 ="&lt;SOAP の Web アドレス&gt;" /&gt;

これらのキーで指定された Web アドレスは、テスト実施中の環境である必要があります。 開発者マシンの Web ブラウザで、**HostName** キーに対して指定された Web アドレスを開けることを確認します。

### <a name="users-cant-be-enumerated"></a>ユーザーを列挙できません

この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。

#### <a name="error-example"></a>エラーの例

```csharp
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Could not enumerate AX users ---> System.ServiceModel.FaultException'1[System.ComponentModel.Win32Exception]: Forbidden
```

#### <a name="solution"></a>ソリューション

2 つのシナリオで、このエラーが発生することがあります。

- CloudEnvironment.Config ファイルで **SelfMintingAdminUser** として指定されたユーザーはシステム管理者ロールを持っている必要があります。 この問題は、**SelfMintingAdminUser** として指定されたユーザーにシステム管理者の役割が割り当てられていない場合に発生します。 適切なユーザーが指定されていることを確認するには、エンドポイントにサインインし、ユーザーのロールを表示します。

    ![管理者ユーザー。](./media/sdk_admin.png)

- 正しくない **NetworkDomain** 値が CloudEnvironment.Config ファイルで **SelfMintingAdminUser** として指定されているユーザーに指定されました。 オンプレミス配置の **AXDB** データベースに対して次の SQL クエリを実行することにより、正しい値を見つけることができます。

    ```sql
    select NETWORKDOMAIN, NETWORKALIAS from USERINFO where NETWORKALIAS='[AdminUserEmail]'
    ```

### <a name="at-least-one-security-token-in-the-message-could-not-be-validated"></a>メッセージ内の少なくとも 1 つのセキュリティ トークンを検証できませんでした

この問題は、マルチユーザー テストを実行するとき、または MS.Dynamics.Performance.CreateUsers.exe を使用してユーザーを作成するときに発生する可能性があります。 AOS マシンが開発者のマシンと異なる場合に発生する傾向があります。 

#### <a name="error-example"></a>エラーの例

```csharp
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail. ---> System.ServiceModel.FaultException: At least one security token in the message could not be validated.
```

#### <a name="solution"></a>ソリューション

この問題は、AOS エンドポイントが作成した証明書の拇印を検証できない場合に発生します。 3 つの原因が考えられます。

- CloudEnvironment.Config ファイルで、**IsAdfs** キーの値が指定されていないか、または **False** に設定されています。 **IsAdfs** キーの値が **True** に設定されていることを確認してください。
- 証明書が AOS マシンにインストールされていません。 問題を解決するには、このトピックで以前に作成した .cer ファイルを AOS マシンにコピーして、証明書をインストールします。
- 証明書のサムプリントは、AOS マシンの wif.config ファイルに追加されませんでした。 問題を解決するには、wif.config ファイルに証明書を追加する方法について、[パフォーマンス SDK を使用してシングル ユーザー テストを実行する](#run-a-single-user-test-by-using-the-performance-sdk) の手順 8 を参照してください。 wif.config ファイルを変更した後は、Service Fabric Explorer のエクスプローラー使用してアプリケーションを再起動することを確認します。

### <a name="msdynamicstestteamfoundationwebclientinteractionservicedllconfig-is-missing-from-the-deployment-items"></a>MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config が配置項目から不足しています

この問題は、通常、ロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例

```csharp
<Test class name>.TestSetup threw exception. System.InvalidOperationException: System.InvalidOperationException: Could not find endpoint element with name 'ClientCommunicationManager' and contract 'Microsoft.Dynamics.Client.InteractionService.Communication.Reliable.IReliableCommunicationManager' in the ServiceModel client configuration section. This might be because no configuration file was found for your application, or because no endpoint element matching this name could be found in the client element.. at System.ServiceModel.Description.ConfigLoader.LoadChannelBehaviors(ServiceEndpoint serviceEndpoint, String configurationName)
```

#### <a name="solution"></a>ソリューション

この問題は、ファイルが展開項目として追加されなかったため、ロード テストの実行時にシステムが MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルを検出できない場合に発生します。 テストの実行のために MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config ファイルが Out フォルダにあることを確認します。 

&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。

> [!IMPORTANT]
> 非常に似た名前を持つ 2 つのファイルがあります。 1 つのファイルの名前は、**\*.dll** で終わり、もう 1 つのファイルの名前は、**\*.dll.config** で終わります。**\*.dll.config** ファイルは、テスト設定の配置項目に含まれている必要があります。

### <a name="cloudenvironmentconfig-is-missing-from-the-deployment-items"></a>CloudEnvironment.Config が配置項目で見つかりません

この問題は、通常、ロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例

```csharp
Initialization method <Test class name>.TestSetup threw exception. 
System.TypeInitializationException: System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> MS.Dynamics.TestTools.TestLogging.EvaluateException: Assert.Fail failed. DateTime="10/13/2017 14:42:55" "The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception.".
```

#### <a name="solution"></a>ソリューション

この問題は、テストの実行時に CloudEnvironment.Config ファイルが存在しない場合に発生します。 この問題は、通常、負荷テストを実行し、CloudEnvironment.Config ファイルが配置項目として追加されなかった場合に発生します。 テストの実行のために CloudEnvironment.Config ファイルが Out フォルダーにあることを確認します。

&lt;solution path&gt;\\TestResults\\&lt;your test run&gt;\\Out

ファイルが欠落している場合は、テストの設定で配置項目に追加します。

![テスト設定。](./media/test-settings.png)

### <a name="interactiveclientid-wasnt-specified-in-the-settings"></a>InteractiveClientId は設定で指定されていませんでした

#### <a name="error-example"></a>エラーの例

```Text
The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SecretSettingsHelper' threw an exception. --->
Microsoft.CE.VaultSDK.SecretProviderException: InteractiveClientId was not specified in settings
```

#### <a name="solution"></a>ソリューション

この問題は、CloudEnvironment.Config ファイルで **SelfSigningCertificateThumbprint** キーの値が指定されていない場合に発生します。 CloudEnvironment.Config ファイルで、次の行を検索し、作成してインストールした証明書の拇印に貼り付けます。

```xml
<ExecutionConfigurations Key="SelfSigningCertificateThumbprint" Value="" />
```

### <a name="the-remote-host-forcibly-closed-an-existing-connection"></a>リモート ホストは、既存の接続を強制的に終了した

#### <a name="error-example"></a>エラーの例

```csharp
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

```powershell
Set-ItemProperty HKLM:\SOFTWARE\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319)) 
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false 
}
```

### <a name="the-w3svc-service-wasnt-found-on-the-computer"></a>コンピューターで w3svc サービスが見つかりませんでした

このエラーは、Microsoft Visual Studio Online を使用してロード テストを実行する場合にのみ発生します。

#### <a name="error-example"></a>エラーの例
```Text
Test method MS.Dynamics.Performance.Application.GFM.PDLTrend.ProcureToPayTrend.ProcureToPaymentTrend threw exception: 
System.TypeInitializationException: The type initializer for 'MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.UserManagement' threw an exception. ---> System.InvalidOperationException: Service w3svc was not found on computer '.'. ---> System.ComponentModel.Win32Exception: The specified service does not exist as an installed service
```

#### <a name="solution"></a>ソリューション

この問題を解決する修正プログラムが利用可能です。 Microsoft サポート技術情報 (KB) 番号は 4095640 です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]