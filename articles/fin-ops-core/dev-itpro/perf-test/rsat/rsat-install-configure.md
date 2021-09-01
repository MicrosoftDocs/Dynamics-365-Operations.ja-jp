---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成の方法について説明します。
author: FrankDahl
ms.date: 08/19/2021
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
ms.openlocfilehash: 49aef84f0b474ca2d7d4084f1ccdee5fbac93abf
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404123"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a>Regression Suite Automation Tool のインストールと構成

[!include [banner](../../includes/banner.md)]

このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成の方法について説明します。

## <a name="prerequisites"></a>必要条件

### <a name="test-environment-prerequisite"></a>テスト環境 (前提条件)

テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。 Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。

### <a name="excel"></a>Excel

テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。

### <a name="azure-devops-prerequisite"></a>Azure DevOps (前提条件)

テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。 Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。 たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。 詳細については、[Azure DevOps サービス](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) の価格設定、または [Azure DevOps サーバーの価格設定](https://azure.microsoft.com/pricing/details/devops/server/) を参照してください。

### <a name="authentication-certificate"></a>認証証明書

RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザーを介して環境にリモート接続するように設計されています。

![クライアント コンピュータと環境。](media/client-environment.png)

セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。 RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。 また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。 RSATをインストールして構成するには、次のセクションの指示に従ってください。

## <a name="installation"></a>インストール

### <a name="installer"></a> インストーラー

[Regression Suite Automation Tool ダウンロード](https://www.microsoft.com/download/details.aspx?id=57357) からマシンに .msi ファイルをダウンロードし、ダブルクリックしてインストーラーを実行します。

> [!NOTE]
> Azure DevOps サーバーを使用している場合は、バージョン 1.210.48249.4 以降をダウンロードしてインストールします。

### <a name="selenium-and-browser-drivers"></a>Selenium およびブラウザー ドライバー

RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。 RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。 次の (または類似の) メッセージが表示されたら、はい を選択します。

![Selenium ドライバー。](media/driver-1.png)

![ブラウザー ドライバー。](media/driver-2.png)

RSAT は [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) を使用します。 Web ドライバー ライブラリおよびブラウザー固有のドライバーは **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にダウンロードされます。

## <a name="configuration"></a>構成

1. デスクトップから RSAT を開きます。

    ![RSAT デスクトップ アイコン。](media/desktop-icon.png)

2. 右上にある **設定** ボタンを選択して、RSAT を構成します。

    ![RSAT 設定。](media/rsat-settings.png)

### <a name="general-settings"></a>一般設定

これらの設定は必須です。

#### <a name="azure-devops-general-settings"></a>Azure DevOps (一般設定)

Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。

+ **Azure DevOps URL** - これは、 Azure DevOps 組織の URL です。 たとえば、`https://yourAzureDevOpsUrlHere.visualStudio.com`。

    > [!NOTE]
    > Azure DevOps サーバーを使用している場合は、**/DefaultCollection** を Azure DevOps URL の末尾に追加します。

+ **アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。 個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。 詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。
+ **プロジェクト名** - Azure DevOps プロジェクトの名前。 RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。 その後、テスト プロジェクトおよびテスト計画を選択できます。
+ **テスト計画** - テスト ケースを含む Azure DevOps テスト計画 詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。

**接続のテスト** を選択し、 Azure DevOps への接続をテストします。

#### <a name="test-environment-general-settings"></a>テスト環境 (一般設定)

テスト環境への接続をコンフィギュレーションします。

+ **ホスト名** – myhost.cloudax.dynamics.com. などのテスト環境のホスト名。 https:// または http:// の接頭語を含めないでください。
+ **SOAP ホスト名** – テスト環境の SOAP ホスト名。
    + デモおよび開発環境 (1 ボックス環境とも呼ばれる) については、ホスト名に接尾語 **soap** を追加します。 たとえば、ホスト名が `myhost.cloudax.dynamics.com` の場合、`myhost.soap.cloudax.dynamics.com` を SOAP ホスト名として使用することができます。
    + テスト環境の SOAP ホスト名がわからない場合は、Infrastructure.SoapServicesUrl の AOS サーバーの web.config ファイルで検索できます。
    + テスト環境が、リモート デスクトップ アクセスがないユーザー受け入れテスト (user acceptance testing: UAT) または上位層サンドボックス環境である場合、この SOAP ホスト名はホスト名と等しくなります。

+ **管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレス。 管理者ユーザー名は、RSAT が接続している Finance and Operations テスト環境でのシステム管理者ロールに属しているユーザーの電子メール アドレスである必要があります。 また、ユーザー アカウント (電子メール アドレス) は、テスト環境と同じテナントに属している必要があります。 たとえば、テスト環境の既定のテナントが contoso.com である場合、管理ユーザーは @constoso.com で終了する必要があります。

+ **拇印** – 使用している認証証明書の拇印。
 使用している環境にリモート デスクトップ プロトコル (RDP) でアクセスできない場合は、この記事で後述する手順に従って、Lifecycle Services から証明書をダウンロードし、拇印をここに貼り付けます。
 環境に RDP でアクセスできる場合は、次の手順に従って自己署名証明書を生成します。

    1. 新しい証明書を作成してインストールするには、 **新規** を選択します。 プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。
    2. プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート店舗にインストールされます。

        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. 新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。 この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。

+ **会社名** – Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。 後でExcelファイルを編集して変更できます。

#### <a name="run-setting"></a>実行設定

ローカル設定をコンフィギュレーションします。

+ **作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。 たとえば、 **C:\Temp\RegressionTool** のようになります。
+ **既定のブラウザー** - テストの実行に使用するブラウザーを選択します。 RSAT は (新しい) Microsoft Edge、Microsoft Internet Explorer、 および Google Chrome をサポートします。 [新しい Microsoft Edge の概要](https://www.microsoft.com/edge)から Microsoft Edge ダウンロードすることをお勧めします。

**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。 **キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。 **名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。 **名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。 **開く** を選択して、構成ファイルから設定を復元します。

### <a name="optional-settings"></a>オプション設定

**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。

+ **テストの実行の接頭語** – RSATはテストの実行結果を Azure DevOps に報告します。 テストの実行には、次の規則: **\<Run ID\> \<Prefix\> \<Test Suite\>** に従って名前が付けられます。 この設定を使用して **\<Prefix\>** を設定します。
+ **テストの実行タイムアウト** – テストの実行のタイムアウト (分単位)。 このタイムアウトに達すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは失敗します。
+ **テスト アクションのタイムアウト** – 個々のテスト ステップのタイムアウト (分単位)。 テストステップがタイムアウトになると、テスト ケースは失敗します。
+ **ステップ間の一時停止** – テストケースの自動実行中にテスト ステップ間で一時停止する秒数。 既定値は **0** (ゼロ) です。 監査または調査のために、テストの実行中に強制的に一時停止するには、この値を設定します。 テスト ケースの Excel パラメーター ファイルの **全般** タブにある、**ステップ間の一時停止 (秒)** パラメーターを変更することで、個々のテスト ケースに対して一時停止を指定することもできます。
+ **最初の検証エラーでテストに失敗** – 既定では、テスト ケースに複数の検証ステップがあり、検証に失敗した場合は、最初の失敗が発生するとテスト ケースの実行が停止します。 テスト ケースは失敗としてマークされます。 すべての検証が完了するまでテスト ケースを実行する場合は、このオプションをオフにします。 その後、テスト ケースですべての検証を評価できます。
+ **情報ログのエラーでテストに失敗** - このオプションをチェックし、テスト ケースの実行中に Finance and Operations 情報ログでエラーが発生した場合、テスト ケースが強制的に失敗するようにします。
+ **失敗時にテスト スイートの実行を中止する** – 既定では、テスト ケースのいずれかが失敗した場合でもテスト スイートの実行が続行されます。 この設定をチェックすると、テスト ケースが失敗した場合にテストの実行が中止されます。 残りのすべてのテスト ケースのステータスは **未実行** になります。
+ **ローカル ファイルの検証ルールを有効にする** - この設定をチェックして、テスト ケースの実行準備が整っているかどうかを検証します。 詳細については、[テスト自動化ファイルの準備状況の検証](rsat-run.md#validate-readiness-of-test-automation-files) を参照してください。
+ **Azure DevOps へのアップロードを有効にする** - Azure DevOps へ偶発的にアップロードされる (したがってプロジェクト全体の記録と自動化ファイルが上書きされます) のを回避するために、この設定をオフにすることができます。 これは、RSAT が実行目的でのみクライアント マシンに配置されていて、ユーザーがテスト ケースを永続的に変更することを回避したい場合に特に便利です。
+ **クラウド プロバイダー** – テスト環境のクラウド テナントのプロバイダーを選択します。 サポートされているプロバイダーは、**グローバル** (パブリッククラウド) および **中国** (主権クラウド) です。

    > [!IMPORTANT]
    > Finance and Operations アプリが 21Vianet に配置されている場合、**クラウド プロバイダー** の設定が必要となり、選択された値が **中国** でなければなりません。

### <a name="configure-the-test-environment-to-trust-the-connection"></a>接続を信頼するようにテスト環境を構成する

#### <a name="if-your-aos-allows-for-remote-desktop-connections"></a>AOS がリモート デスクトップ接続を許可している場合

証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。 マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。

1. AOSマシンへのリモート デスクトップ接続を開きます。
2. IIS を開き、サイトの一覧で AOSService を見つけます。

    ![IISで AOS を検索します。](media/configure-aos.png)

3. **AOSService** を右クリックし、**エクスプローラー** を選択します。
4. ファイル **wif.config** を開き、検索します。

    ![wif.config を開きます。](media/open-wif-config.png)

5. 次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。 機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。

    ```xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry, Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="ccbc124d0a119xxxxxxxxxxxxxxxxxxxx841e797" />
            </keys>
                <validIssuers>
                    <add name="CN=127.0.0.1" />
                </validIssuers>
        </authority>
    ```

#### <a name="if-you-have-no-remote-desktop-access-to-the-server"></a>サーバーへのリモート デスクトップ アクセス権がない場合

Microsoft が管理するサンドボックス、またはセルフ サービス タイプ サンドボックスなど、リモート デスクトップ プロトコル (RDP) アクセスが削除された場合、Microsoft は環境に応じた証明書を生成し、事前にコンフィギュレーションします。 次の手順に従って RSAT 証明書を取得し、LCS ユーザー インターフェイスを使用します。 自動化については、[ZIP ファイルで RSAT 証明書をフェッチする](../../lifecycle-services/api/v1/reference-download-rsat-certificate.md) API 参照ページに情報があります。

1. Lifecycle Services の環境詳細ページの **管理** の下に、2 つの新しいオプションが表示されます。

    - RSAT 証明書のダウンロード
    - RSAT 証明書を再生成する

![RSAT 証明書のオプションをダウンロードして再生成します。](media/rsat-lcs1.png)

**ダウンロード** ボタンを使用して、証明書バンドルを .zip ファイルとして取得します。

2. クリアテキスト パスワードが画面に表示されるという警告が表示されます。 後の手順でパスワードが必要になります。  **はい** を選択して続行します。

3. クリアテキスト パスワードを後で使用できるようにコピーします。 .zip ファイルがダウンロードされていることを確認します。 .zip ファイルの内部には、証明書 (.cer) と個人情報交換 (.pfx) ファイルがあります。 ファイルを解凍します。

4. ローカル コンピューターの信頼されたルート ストアに証明書をインストールします。
    + 証明書 (.cer) をダブルクリックして開き、**証明書のインストール** を選択します。 
    + **ローカル コンピューター** を選択し、**信頼済ルート証明機関** ストアを参照して、信頼されたルート ストアにインストールします。

5. ローカル コンピューターの個人ストアに pfx ファイルをインストールします。
   + 個人情報交換 (.pfx) ファイルをダブルクリックして開き、**ローカル コンピューター** を選択します。 
   + 手順 2 で保存したパスワードを入力し、**個人** ストアを参照します。

6. 証明書ファイルをダブルクリックして、開きます。 **詳細** タブを参照し、**拇印** セクションが表示されるまで下にスクロールします。 **拇印** を選択し、テキスト ボックスの ID に注意します。 この捺印を選択するか、RSAT 設定に貼り付けます。
![拇印の設定。](media/rsat-lcs4.png)

これで、この証明書を使用して環境に対してテストを実行できます。 証明書は期限が切れる前に Microsoft によって自動的にローテーションされます。その後、上記の手順 1 からこの証明書の新しいバージョンをダウンロードする必要があります。 セルフ サービス環境では、有効期限に最も近いダウンタイム ウィンドウで 90 日ごとにローテーションされます。 これらのダウンタイム ウィンドウには、顧客が開始したパッケージ展開、および環境を対象とするデータベース移動操作が含まれます。

## <a name="manual-configuration-of-authentication-certificates"></a>認証証明書の手動構成

必要に応じて、RSAT認証証明書を手動で構成することができます。

このプロセスに精通していない場合は、システム管理者に問い合わせてください。 Windows キットがコンピューターにインストールされていることを確認してください。 Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。 このドキュメントで説明されている手順には、これらのコンポーネントが必要です。

+ デスクトップ アプリ用の Windows SDK 署名ツール
+ UWP マネージド アプリ用の Windows SDK。

### <a name="generate-the-certificate"></a>証明書を生成する

RSAT クライアント コンピュータで証明書ファイルを生成する必要があります。 **証明書は、テスト ツールを実行している同じコンピュータで生成する必要があります。** 証明書ファイルを生成するには、次の手順を実行します:

1. コンピューター上にまだ存在しない場合は、 **C:\Temp** フォルダーを作成します。
2. 管理者としてコマンド ライン ウィンドウを開きます。
3. Windows SDKをインストールしたフォルダに移動します。 正確なフォルダは、Windows SDKをインストールした場所によって異なる場合があります。 Windows キット 8.1を使用することもできます。

    ```Console
    cd c:\Program Files (x86)\Windows Kits\10\bin\10.0.17763.0\x64
    ```

4. 次のコマンドを実行します。 秘密キー パスワードを要求するプロンプトが表示されたら、 **なし** を入力します。

    ```Console
    makecert.exe -n "CN=127.0.0.1" -ss My -sr LocalMachine -a sha256 -len 2048 -cy end -r -eku 1.3.6.1.5.5.7.3.1 c:\temp\authCert.cer
    ````

### <a name="install-the-certificate-to-the-trusted-root"></a>信頼済ルートに証明書をインストールする

証明書をインストールするには、次の手順を実行します:

1. 証明書をインストールするには、 **authCert.cer** をダブルクリックします。
2. **証明書のインストール** を選択します。
3. **ローカル コンピューター > 次の店舗で証明書を確定 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** を選択します。
4. **パスワード** フィールドは空白のままにします。
5. **証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。

    ![拇印の一覧を示す証明書ダイアログ。](media/certificate-dialog.png)

6. 拇印をコピーして保存します。 このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
