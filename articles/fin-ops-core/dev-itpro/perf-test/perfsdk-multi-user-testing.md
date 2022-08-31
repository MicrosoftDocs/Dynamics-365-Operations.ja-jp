---
title: パフォーマンス SDK によるマルチユーザー テストを実行する
description: この記事では、Microsoft Visual Studio、パフォーマンス ソフトウェア開発キット (SDK)、およびタスク レコーダー テスト スクリプトを使用してマルチユーザー テストを実行する方法について説明します。
author: kennysaelen
ms.date: 06/04/2020
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: kesaelen
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 18cad8d57237d86845bae143c39ed118563c8a62
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270649"
---
# <a name="run-multi-user-testing-by-using-the-performance-sdk"></a>パフォーマンス SDK によるマルチユーザー テストを実行する

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Visual Studio、パフォーマンス ソフトウェア開発キット (SDK)、およびタスク レコーダー テスト スクリプトを使用してマルチユーザー テストを実行する方法について説明します。

> [!IMPORTANT]
> Visual Studio 2019 は Web パフォーマンスと負荷テスト機能を含む Visual Studio の最新バージョンです。 Visual Studio および、オンプレミスでの負荷テストに向けたテスト コントローラー/テスト エージェントをご利用の場合、 Visual Studio 2019 が最新のバージョンになります。 そのサポート サイクルが終了するまで継続して使用することができます。 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。

## <a name="prerequisites"></a>必要条件

この記事の手順を完了する前に、次の前提条件が満たされていることを確認してください:

- 開発環境には **Visual Studio Enterprise Edition** があります。 負荷テストを作成するには、Enterprise Edition が必要です。 Microsoft Dynamics Lifecycle Services (LCS) を通じてクラウド ホスト環境として開発ボックスを配置する場合は、配置する適切な Visual Studio バージョンを選択してください 。
- Visual Studio Web パフォーマンスおよび負荷テスト ツールは、[負荷テストコ ンポーネントのインストール](/visualstudio/test/quickstart-create-a-load-test-project#install-the-load-testing-component) の説明に従ってインストールされます。
- 開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックス環境があります。
- [タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従って開発環境を構成しました。
- エンド ツー エンド (E2E) シナリオ用に C\# パフォーマンス テスト クラスが生成され、[タスク レコーダーとパフォーマンス SDK を使用したシングルユーザー テスト](single-user-test-perf-sdk.md) の手順に従ってシングルユーザー テストを実行できます。

## <a name="configure-a-development-environment-for-multi-user-testing"></a>マルチ ユーザー テストのための開発環境のコンフィギュレーション

次のコンフィギュレーションは、テスト コントローラーおよびエージェントをローカルにホストするために使用される開発マシンで設定する必要があります。

> [!NOTE]
> Microsoft が管理するすべてのサンドボックスおよびセルフサービス タイプのサンドボックスについて、Microsoft はご使用の環境の証明書を生成し、事前に構成します。

1. **TestRoot** という名前の環境変数を作成し、Windows PowerShell で次のコマンドレットを実行して **PerfSDK** フォルダーをポイントします。

    ```powershell
    [ENVIRONMENT]::SETENVIRONMENTVARIABLE("TESTROOT", "K:\PERFSDK\PERFSDKLOCALDIRECTORY", "USER")
    ```

    変数を検証するには、Windows PowerShell 次のコマンドを実行します。

    ```powershell
    [ENVIRONMENT]::GETENVIRONMENTVARIABLE("TESTROOT", "USER") | Write-Host
    ```

2. LCS で、ターゲット サンドボックス環境の **環境の詳細** ページを開きます。

    **環境の詳細** ページの **管理** メニューには、次の 2 つの新しいコマンドが表示されます。

    - RSAT 証明書のダウンロード
    - RSAT 証明書を再生成する

    ![RSAT 証明書のダウンロードと RSAT 証明書の再生成コマンド。](rsat/media/rsat-lcs1.png)

3. **RSAT 証明書をダウンロード** を選択して、証明書バンドルを ZIP ファイルとして取得します。
4. クリアテキストのパスワードが画面に表示されるという警告が表示されます。 **はい** を選択して続行します。
5. 後で必要になるため、クリアテキストのパスワードをコピーします。
6. ZIP ファイルをダウンロードした後、解凍します。 内部には、証明書 (.cer) ファイルと個人情報交換 (.pfx) ファイルがあります。
7. 証明書 (.cer) ファイルをダブルタップ (またはダブルクリック) して開き、**インストール** を選択します。 この証明書をローカル コンピューターにインストールしてから、**個人** ストアを参照します。 ローカル コンピューターの場所に対してこの手順を繰り返し、特定の **信頼済ルート証明機関** ストアを参照します。
8. 個人情報交換 (.pfx) ファイルをダブルタップ (またはダブルクリック) して開き、**インストール** を選択します。 この証明書をローカル コンピューターにインストールしてから、手順 5 でコピーしたパスワードを入力して、**個人** ストアを参照します。 ローカル コンピューターの場所に対してこの手順を繰り返し、手順 5 でコピーしたパスワードを入力して、特定の **信頼済ルート証明機関** ストアを参照します。
9. 証明書ファイルをダブルタップ (またはダブルクリック) して、開きます。 **詳細** タブで、**拇印** セクションが見つかるまで下にスクロールします。 **拇印** を選択し、テキスト ボックスに ID をコピーします。 この拇印を保存し、パフォーマンス SDK に対して **CloudEnvironment.config** 拇印を更新します。

> [!NOTE]
> Microsoft は、有効期限が切れる前に証明書を自動的にローテーションします。 その時点で、証明書の新しいバージョンをダウンロードする必要があります。 セルフ サービス環境では、証明書は有効期限に最も近いダウンタイム ウィンドウで 60 日ごとにローテーションされます。 ダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a>マルチユーザー テスト用の PerfSDKSample ソリューションの準備

次の手順に従って、パフォーマンス テスト用のサンプル ソリューションを準備します。 サンプル ソリューションは、開発環境の Performance SDK フォルダーにあります。 既定では、フォルダは K:\\PerfSDK\\PerfSDKLocalDirectory です。

1. 上位のアクセス許可で次のコマンドレットを実行して、以前にインストールした証明書が正しくインストールされていること、および以前に保存した拇印がローカル コンピューターの **個人** ストアにあることを確認します。

    ```powershell
    cd Cert:\LocalMachine\My
    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    次の図は、サンプル結果を示します。 以前に保存した拇印がリストにあることを確認してください。

    ![コマンド プロンプト ウィンドウの拇印。](media/perfsdk-multi-user-testing-01.png)

2. Performance SDK フォルダーの **CloudEnvironment.config** 構成ファイルを更新し、対象の環境を記述します。 この更新プログラムの一部として、次の手順を実行します。

    1. **HostName** と **SOAPHostName** の設定が階層 2 以上のサンドボックス環境と一致することを確認します。
    2. **SelfSigningCertateThumbprint** の値として以前に保存した拇印を追加します。 構成ファイルにエントリがない場合は、次の図に示すように追加できます。
    3. **UserCount** の設定を更新して、ケースのテスト ユーザーの数と一致するようにします。
    4. **UserFormat** の設定を更新して、テスト ユーザーの名前付け規則と一致するようにします。
    5. **AuthenticatorConfigurationCollection** 要素の下の各 **AuthenticatorConfiguration** 要素で、**MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAadAuthenticator** を  **MS.Dynamics.TestTools.CloudCommonTestUtilities.Authentication.SelfMintedTokenAuthenticator** で置き換えます。
    6. **AzureActiveDirectoryConfiguration** 要素と **KeyVaultConfigurations** 要素をコメント行にします。

    > [!NOTE]
    > 財務と運用アプリが V21Vianet に配置されている場合、必ず `NetworkDomain="https://sts.chinacloudapi.cn/"` を **SelfMintingSysUser** および **SelfMintingAdminUser** で指定してください。

    結果は次の例のようになります。

    ![更新された CloudEnvironment.config ファイル。](./media/perfsdk-multi-user-testing-02.png)

3. **vsonline.testsettings** ファイルの名前を **local.testsettings** に変更します。
4. Visual Studio で **local.testsettings** ファイルを開き、次の手順に従って変更します。

    1. **テストの設定** ダイアログ ボックスの **一般** タブの **テストの実行場所** フィールド グループで **ローカル コンピューターまたはテスト コント ローラーを使用してテストを実行** オプションを選択します。
    2. **配置** タブで **配置を有効にする** チェック ボックスを選択し、**ディレクトリの追加** ボタンを使用して **bin\debug** を **配置する追加のファイルやディレクトリ** フィールドに追加します。

        ![[テストの設定] ダイアログ ボックスの [配置] タブ。](./media/perfsdk-multi-user-testing-04.png)

    3. **ホスト** タブの **32 ビットまたは 64 ビット プロセスでテストを実行** フィールドで、**64 ビット コンピューターで 64 ビット プロセスのテストを実行** を選択します。
    4. **適用** を選択して **テストの設定** ダイアログ ボックスを閉じます。
    5. プロジェクト コンフィギュレーションを開き、**ターゲット フレームワーク** を **.NET Framework 4.6.2** に設定して変更します。

    > [!NOTE]
    > Microsoft Dynamics 365 アドインを使用してタスク記録から C\# パフォーマンス テストを生成するたびに、ソリューション全体を再度開くのではなく、プロジェクトを Visual Studio に再読み込みします。 負荷テストを実行する前に、必ずソリューションを再読み込みして、テスト設定ファイルが表示されていることを確認してください。

## <a name="modify-the-performance-test-sources"></a>パフォーマンス テスト ソースの変更

ソリューションで生成された各パフォーマンス テストごとに、次の手順に従います。

1. **使用** ディレクティブ セクションの上部に、次のステートメントを追加します。

    ```csharp
    using MS.Dynamics.TestTools.UIHelpers.Core;
    ```

2. 全体を次の行に置き換えて、**TestSetup** メソッドを変更します。

    ```csharp
    private DispatchedClient Client;
    private UserContext _userContext;
    private TimerProvider timerProvider;
    [TestInitialize]
    public void TestSetup()
    {
        if (this.TestContext != null)
        {
            timerProvider = new TimerProvider(this.TestContext);
        }
        SetupData();
        Client = new DispatchedClientHelper().GetClient();
        Client.ForceEditMode = false;
        Client.Company = WellKnownCompanyID.USMF.ToString();
        Client.Open();
    }
    ```

3. 次の例と同様に **TestCleanup** メソッドを変更します。

    ```csharp
    public void TestCleanup()
    {
        Client.Close();
        Client.Dispose();
        Client = Null;
    }
    ```

4. ソリューションを構築します。

## <a name="add-a-test-to-the-load-test-mix"></a>負荷テスト ミックスにテストの追加

次の手順に従って、テスト ミックスにパフォーマンス テストを追加します。

1. **SampleLoadTest.loadtest** ファイルを開き、**テスト ミックス** ノードを検索します。
2. **テスト ミックス** ノードを選択し、保留 (または右クリック) し、**テスト ミックスの編集** を選択します。
3. **テスト ミックスの編集** ダイアログ ボックスで、**追加** を選択してテストをミックスに追加します。

    ![[テスト ミックスの編集] ダイアログ ボックス。](./media/perfsdk-multi-user-testing-06.png)

4. **実行設定** ノードで、プロパティを変更し、**実行設定 1** の **タイミング** フィールドを更新します。 これらのフィールドは **ウォームアップ期間**、**実行期間**、**クールダウン期間** を含みます。

    ![タイミング フィールド。](./media/perfsdk-multi-user-testing-07.png)

5. **シナリオ** ノードで、必ず **負荷パターン** プロパティを更新し、**定数ユーザー数** パラメーターをテストの実行に使用するユーザーの総数に設定してください。

    ![定数ユーザー数パラメーター。](./media/perfsdk-multi-user-testing-08.png)

## <a name="create-test-users"></a>新規ユーザーのテスト

テスト ユーザーは、ターゲット環境に追加する必要があります。 名前付けパターンは **CloudEnvironment.config** 構成ファイルで指定されたパターンと一致している必要があります。 Microsoft Dynamics 365 環境でユーザーを手動で作成するか、Performance SDK フォルダーの **MS.Dynamics.Performance.CreateUsers.exe** コンソール アプリケーションを使用できます。

ユーザーを手動で作成する場合は、各ユーザーに **システム管理者** セキュリティ ロールが割り当てられている必要があります。

コンソール アプリケーションを使用してユーザーを作成することをお勧めします。コンソール アプリケーションは構成ファイルを読み取り、適切なサービス エンドポイントを呼び出すためです。

## <a name="run-multi-user-testing-by-using-a-local-test-controller"></a>ローカル テスト コントローラーを使用したマルチユーザー テストの実行

1. Visual Studio プロジェクトで、**SampleLoadTest.loadtest** ファイルを開き、**負荷テストを実行** を選択します。
2. テスト出力を確認します。

    ![テスト出力。](./media/perfsdk-multi-user-testing-10.png)

## <a name="troubleshooting"></a>トラブルシューティング

パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

