---
title: パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト
description: このトピックでは、タスク レコーダーから生成されたパフォーマンス テスト スクリプトと共に Microsoft Visual Studio とパフォーマンス SDK を使用してマルチユーザー テストを行う方法を説明します。
author: hasaid
manager: AnnBe
ms.date: 06/4/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3304860d756dad26b08d54e704eed3517028d90
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833284"
---
# <a name="multi-user-testing-with-the-performance-sdk-and-a-local-test-controller"></a>パフォーマンス SDK とローカル テスト コントローラーを使用したマルチユーザー テスト

[!include [banner](../includes/banner.md)]

 > [!IMPORTANT]
  > Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。 将来的に、代替ソリューションの推奨を公開します。  
  > - Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。 そのサポート サイクルが終了するまで継続して使用することができます。 
  > - クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。 それまでの間は、同サービスの全機能を継続してご利用いただけます。 また、オンプレミス負荷テストに切り替えることがも可能です。 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。

## <a name="prerequisites"></a>必要条件

このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:

- 自身の Microsoft Azure サブスクリプションで、プラットフォーム更新プログラム 21 以降の Microsoft Dynamics 365 for Finance and Operations 開発環境があります。
- 開発環境に Microsoft Visual Studio 2015 Enterprise edition がある
- 開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。
- [タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従って開発環境を構成しました。
- エンド ツー エンド (E2E) シナリオ用に C\# パフォーマンス テスト クラスが生成され、[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従ってシングルユーザー テストを実行できます。

## <a name="configure-a-finance-and-operations-development-environment-for-multi-user-testing"></a>マルチユーザー テストのための Finance and Operations 開発環境の構成

1. [SQL Server の ODBC ドライバー 17](https://download.microsoft.com/download/E/6/B/E6BFDC7A-5BCD-4C51-9912-635646DA801E/en-US/msodbcsql_17.2.0.1_x64.msi) をダウンロードして、ダウンロードしたファイルを **msodbcsql** に名前を変更して、それを **PerfSDK** フォルダーの **Visual Studio Online** フォルダーにコピーします。

    [![Visual Studio Online フォルダーの msodbcsql ファイル](./media/multi-user-test-local-01.png)](./media/multi-user-test-local-01.png)

2. **TestRoot** という名前の環境変数を作成し、Microsoft Windows PowerShell で次のコマンドレットを実行して **PerfSDK** フォルダーをポイントします。

    ```
    [ENVIRONMENT]::SETENVIRONMENTVARIABLE("TESTROOT", "K:\PERFSDK\PERFSDKLOCALDIRECTORY", "USER")
    ```

    新しい環境変数を表示するには、**システム プロパティ** ダイアログ ボックスの **詳細** タブで **環境変数** を選択します。

    [![[環境変数とシステム プロパティ] ダイアログ ボックス](./media/multi-user-test-local-02.png)](./media/multi-user-test-local-02.png)
    
3. 管理者として **コマンド プロンプト** ウィンドウを開き、次のコマンドを入力して必要な証明書を生成してインストールします。 プライベート キーのパスワードを要求するメッセージが表示されたら、**なし** を選択します。

    ```
    "C:\Program Files (x86)\Windows Kits\8.1\bin\x64\makecert" -n "CN=127.0.0.1" -ss Root -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 -sv c:\temp\authcert.pvk c:\temp\authcert.cer

    "c:\Program Files (x86)\Windows Kits\8.1\bin\x64\pvk2pfx" -pvk c:\temp\authCert.pvk -spc c:\temp\authcert.cer -pfx c:\temp\authcert.pfx
    ```

    上記のコマンドの要素について説明します:

    - **-n "CN=127.0.0.1"** 証明書に人が判読可能な名前が与えられます。 この証明書の名前が **127.0.0.1** であることが非常に重要です。 それ以外の場合は、単一ユーザー テストは実行することはできません。
    - **-eku 1.3.6.1.5.5.7.3.1** は、証明書の目的を示します。 証明書が Secure Sockets Layer (SSL) サーバー証明書として使用できることを示します。

    これらのコマンドは次の証明書を生成し C:\\Temp に保存します。

    - Authcert.pvk
    - Authcert.cer
    - Authcert.pfx

4. **ローカル コンピューター\\個人** 証明書ストアで **authcert.pfx** と **authcert.cer** 証明書をインストールします。

    [![ローカル コンピューター\個人証明書ストア](./media/multi-user-test-local-04.png)](./media/multi-user-test-local-04.png)

5. **PerfSDK\\PerfSDKLocalDirectory** フォルダーに **authcert.pfx** 証明書をコピーします。

    [![PerfSDK の証明書 \\ PerfS フォルダー](./media/multi-user-test-local-05.png)](./media/multi-user-test-local-05.png)

6. 次のコマンドを実行して **Visual Studio Online** フォルダーの **setup.md** ファイルを置き換えます。

    ```
    setx testroot "%DeploymentDirectory%"
    ECHO Installing D365 prerequisites
    ECHO MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    MSIEXEC /a %DeploymentDirectory%\msodbcsql /passive /norestart IACCEPTMSODBCSQLLICENSETERMS=YES
    %windir%\sysnative\windowspowershell\v1.0\powershell.exe -File %DeploymentDirectory%\install-wif.ps1
    Md %DeploymentDirectory%\Common\Team\Foundation\Performance\Framework
    %DeploymentDirectory%\CloudCtuFakeACSInstall.cmd %DeploymentDirectory%\authcert.pfx
    ```

7. **Visual Studio Online** フォルダーの **CloudCtuFakeACSInstall.cmd** ファイルで、**インポート** コマンドから **%TestCertPassword%** を削除します。

    [![CloudCtuFakeACSInstall.cmd インポート コマンド](./media/multi-user-test-local-07.png)](./media/multi-user-test-local-07.png)

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a>マルチユーザー テスト用の PerfSDKSample ソリューションの準備

1. Microsoft Visual Studio の **テスト** メニューで、**テストの設定** にポイントして、**既定のプロセッサ アーキテクチャ** にポイントして、そして **x64** を選択します。
2. 管理者として次のコマンドレットを実行して、開発環境の **authcert.pfx** 証明書の拇印を取得します。階層 2 以上のサンドボックス環境を構成するときに必要になるため、拇印をどこかに保存します。

    ```
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    次の図は、これらのコマンドレットが返す拇印の例を示しています。

    [![コマンド プロンプト ウィンドウの拇印](./media/multi-user-test-local-09.png)](./media/multi-user-test-local-09.png)

    > [!NOTE]
    > プラットフォーム更新プログラム 21 以降の環境では、発行者として **127.0.0.1** を持つ証明書が自動的にインストールされます。 生成した証明書の拇印を取得したことを確認します。

3. **CloudEnvironment.config** ファイルを更新してコンフィギュレーションを反映します。 この更新プログラムの一部として、次の手順を実行します。

    - **HostName** と **SOAPHostName** が階層 2 以上のサンドボックス環境と一致することを確認します。
    - **authcert.pfx** 証明書の拇印を **SelfSigningCertificateThumbprint** の値として追加します。
    - **UserCount** を更新して、このケースでテスト ユーザーの数を反映します。
    - **UserFormat** を更新して、テスト ユーザーの命名規則を反映します。

    [![更新された CloudEnvironment.config ファイル](./media/multi-user-test-local-10.png)](./media/multi-user-test-local-10.png)

4. **vsonline.testsettings** を構成します。 **テストの設定** ダイアログ ボックスの **一般** タブの **テストの実行場所** フィールド グループで **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** オプションを選択します。

    [![[テストの設定] ダイアログボックスの [一般] タブ](./media/multi-user-test-local-11.png)](./media/multi-user-test-local-11.png)

    > [!NOTE]
    > **vsonline.testsettings** が表示されない場合は、ソリューションをもう一度開きます。

5. **配置** タブで **配置を有効にする** チェック ボックスを選択し、**ディレクトリの追加** と **ファイルの追加** ボタンを使用して **配置する追加のファイルやディレクトリ** フィールドにフォルダーとファイルを追加します。

    - **K:\\PerfSDK\\PerfSDKLocalDirectory\\SampleProject\\PerfSDKSample\\bin\\Debug** フォルダー
    - **K:\\PerfSDK\\PerfSDKLocalDirectory\\Visual Studio Online** フォルダー
    - **K:\\PerfSDK\\PerfSDKLocalDirectory\\CloudEnvironment.Config** ファイル
    - **K:\\PerfSDK\\PerfSDKLocalDirectory\\authcert.pfx** ファイル
    - **K:\\PerfSDK\\PerfSDKLocalDirectory\\MS.Dynamics.Test.Team.Foundation.WebClient.InteractionService.dll.config** ファイル

    [![[テストの設定] ダイアログ ボックスの [配置] タブ](./media/multi-user-test-local-12.png)](./media/multi-user-test-local-12.png)

    > [!NOTE]
    > "展開項目がソリューション フォルダにありません" という警告が表示されたら **OK** を選択して続行します。

6. **ホスト** タブの **32 ビットまたは 64 ビット プロセスでテストを実行** フィールドで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。
7. **適用** を選択して **テストの設定** ダイアログ ボックスを閉じます。
8. C\# パフォーマンス テストに次のステートメントを追加して、C\# パフォーマンス クラスを変更します。

    ```
    using MS.Dynamics.TestTools.UIHelpers.Core;
    ```

    [![MS.Dynamics.TestTools.UIHelpers.Core の使用; コマンド プロンプト ウィンドウのステートメント](./media/multi-user-test-local-14.png)](./media/multi-user-test-local-14.png)

9. **TestSetup()** メソッドの先頭に次の行を追加して **TestSetup** メソッドを変更します。

    ```
    var testroot = System.Environment.GetEnvironmentVariable("DeploymentDir");
    if (string.IsNullOrEmpty(testroot))
    {
        testroot = System.IO.Directory.GetCurrentDirectory();
    }
    Environment.SetEnvironmentVariable("testroot", testroot);
    ```

    [![TestSetup メソッドに追加された行](./media/multi-user-test-local-15.png)](./media/multi-user-test-local-15.png)

10. **TestSetup** メソッドで "マルチユーザーの場合は以下の行をコメント解除" というコードの行をコメント解除して、次の行をコメント アウトします。

    ```
    Client = DispatchedClient.DefaultInstance;
    ```

    [![変更されたコード](./media/multi-user-test-local-16.png)](./media/multi-user-test-local-16.png)

11. 次の例と同様に **TestCleanup** メソッドを変更します。

    ```
    public void TestCleanup()
    {
        Client.Close();
        Client.Dispose();
        Client = Null;
        //_userContext.Dispose();
    }
    ```

12. 持っているすべての C\# パフォーマンス テスト クラスについてステップ 2 から 11 を繰り返します。
13. 完了したらソリューションをビルドします。
14. **SampleLoadTest.loadtest** で **テスト ミックス** の下のテスト クラスを選択します。

    [![[テスト ミックスの編集] ダイアログ ボックス](./media/multi-user-test-local-18.png)](./media/multi-user-test-local-18.png)

14. **SampleLoadTest.loadtest** で **実行設定 1 \[有効\]** の **タイミング** フィールドを更新します。 これらのフィールドは **ウォームアップ期間**、**実行期間**、**クールダウン期間** を含みます。

    [![タイミング フィールド](./media/multi-user-test-local-19.png)](./media/multi-user-test-local-19.png)

15. **定数負荷パターン** で、テストの実行に使用するユーザーの総数に **定数ユーザー数** パラメーターを設定します。

    [![定数ユーザー数パラメーター](./media/multi-user-test-local-20.png)](./media/multi-user-test-local-20.png)
    
## <a name="configure-a-tier-2-or-above-sandbox-environment-for-multi-user-testing"></a>マルチユーザー テスト用に階層 2 以上のサンドボックス環境を構成する

1. 各 Application Object Server (AOS) コンピューターの **ローカル コンピュータ\\パーソナル** の下に **authcert.pfx** と **authcert.cer** 証明書をインストールします。

    [![インストールした証明書](./media/multi-user-test-local-21.png)](./media/multi-user-test-local-21.png)

2. **authcert.pfx** 証明書の拇印を階層 2 以上のサンドボックス環境の **wif.config** ファイルに追加します。
3. **管理ツール** から Microsoft インターネット インフォメーション サービス (IIS) マネージャを開き、**サイト** から **AOSService** を選択します。
4. 右側で **アクションの確認** を選択し、次にウィンドウの一番下から **wif.config** ファイルを見つけます。
5. 生成された証明書の拇印を `https://fakeacs.accesscontrol.windows.net/` 認証局の末尾に追加します。

    [![生成された証明書から追加された拇印](./media/multi-user-test-local-22.png)](./media/multi-user-test-local-21.png)

6. 変更を保存して IIRESET を実行します。
7. 各 AOS コンピューターで手順 3 ～ 6 を繰り返します。
8. **SampleLoadTest.load** テストを開き、テスト ユーザーを作成してターゲット環境にインポートします。 次に各ユーザーに **システム管理者** セキュリティ ロールを割り当てます。

    [![ターゲット環境のユーザー ページ](./media/multi-user-test-local-23.png)](./media/multi-user-test-local-22.png)

    > [!NOTE]
    > **MS.Dynamics.Performance.CreateUsers.exe** を実行してテスト ユーザーを作成することもできます。 この場合、IISRESET を実行する必要はありません。

## <a name="run-multi-user-testing-by-using-a-local-test-controller"></a>ローカル テスト コントローラーを使用したマルチユーザー テストの実行

1. devbox 上の Visual Studio で **負荷テストの実行** を選択します。

    [![負荷テストの実行](./media/multi-user-test-local-24.png)](./media/multi-user-test-local-24.png)

2. テスト出力を確認します。

    [![テストの出力](./media/multi-user-test-local-25.png)](./media/multi-user-test-local-25.png)

## <a name="troubleshooting"></a>トラブルシューティング

パフォーマンス SDK を使用したシングルユーザーまたはマルチユーザー テストの詳細は [トラブルシューティング ガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。
