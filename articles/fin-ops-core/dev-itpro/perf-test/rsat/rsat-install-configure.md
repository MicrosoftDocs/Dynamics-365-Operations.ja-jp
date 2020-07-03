---
title: Regression Suite Automation Tool のインストールと構成
description: このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: f4109d43845fe8df00b176c9a1d0ab9700d06685
ms.sourcegitcommit: 840230f3dc500852791953d05c2737dd539ed0b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2020
ms.locfileid: "3418554"
---
# <a name="regression-suite-automation-tool-installation-and-configuration"></a>Regression Suite Automation Tool のインストールと構成

[!include [banner](../../includes/banner.md)]

このトピックでは、Regression Suite Automation Tool (RSAT) のインストールと構成方法について説明します。

## <a name="prerequisites"></a>必要条件

### <a name="test-environment"></a>テスト環境
テスト環境では、プラットフォーム更新プログラム 15 以降を実行する必要があります。 Regression Suite Automation Tool は、webブラウザー経由でテスト環境にアクセスできる必要があります。  

### <a name="excel"></a>Excel
テスト パラメーターを生成および編集するには、 Microsoft Excel をインストールする必要があります。 

### <a name="azure-devops"></a>Azure DevOps
テスト ケース、テスト計画、およびテストケースの結果を保存および管理するには、 Azure DevOps プロジェクトが必要です。 Azure DevOps テスト管理者またはテスト計画ライセンスが必要です。 たとえば、 Visual Studio エンタープライズ サブスクリプションを所有している場合は、既にテスト計画に対するライセンスを取得しています。 詳細については、[Azure DevOps サービス](https://azure.microsoft.com/pricing/details/devops/azure-devops-services/) の価格設定、または [Azure DevOps サーバーの価格設定](https://azure.microsoft.com/pricing/details/devops/server/) を参照してください。

### <a name="authentication-certificate"></a>認証証明書
RSAT は、任意の Windows 10 コンピュータにインストールされ、Web ブラウザーを介して環境にリモート接続するように設計されています。

![クライアント コンピュータと環境](media/client-environment.png)

セキュリティで保護された認証を有効にするには、RSATでは、RSAT クライアント コンピューターに証明書をインストールする必要があります。 RSAT 設定 ダイアログ ボックスでは、認証証明書を自動的に作成およびインストールできます。 また、接続を信頼するように仮想マシン (VM) をコンフィギュレーションする必要があります。 RSATをインストールして構成するには、次のセクションの指示に従ってください。

## <a name="installation"></a>インストール

### <a name="installer"></a> インストーラー
[Regression Suite Automation Tool ダウンロード](https://www.microsoft.com/download/details.aspx?id=57357) からマシンに .msi ファイルをダウンロードし、ダブルクリックしてインストーラーを実行します。 

> [!NOTE]
> Azure DevOps サーバーを使用している場合は、バージョン 1.210.48249.4 以降をダウンロードしてインストールします。 
 
### <a name="selenium-and-browser-drivers"></a>Selenium およびブラウザー ドライバー
RSATには、Selenium および Web ブラウザー ドライバー ライブラリが必要です。 RSATでは、必要なライブラリが見つからない場合は、プロンプトが表示され、自動的にインストールされます。 次の (または類似の) メッセージが表示されたら、はい を選択します。
 
![Selenium ドライバー](media/driver-1.png)
 
![ブラウザー ドライバー](media/driver-2.png)

または、 [Selenium ドライバーのインストール](#install-selenium-drivers) を参照してください。

## <a name="configuration"></a>構成

デスクトップから RSAT を開きます。

![RSAT デスクトップ アイコン](media/desktop-icon.png)
 
RSATを構成するには、右上の **設定** ボタンを選択します。

![RSAT 設定](media/rsat-settings.png)

### <a name="general-settings"></a>一般設定
これらの設定は必須です。

#### <a name="azure-devops"></a>Azure DevOps
Azure DevOps プロジェクトおよびテスト計画への接続をコンフィギュレーションします。

+ **Azure DevOps URL** - これは、 Azure DevOps 組織のURLです。 たとえば、`https://yourAzureDevOpsUrlHere.visualStudio.com`。

    > [!NOTE]
    > Azure DevOps サーバーを使用している場合は、**/DefaultCollection** を Azure DevOps URL の末尾に追加します。

+ **アクセス トークン** - ツールが Azure DevOps に接続できるようにするアクセス トークン。 個人用アクセス トークンを作成するか、保存した既存のアクセス トークンを使用する必要があります。 詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。 
+ **プロジェクト名** - Azure DevOps プロジェクトの名前。 RSATでは、指定された Azure DevOps URLに基づいて、使用可能なプロジェクト名とテスト プランを自動的に検出します。 その後、テスト プロジェクトおよびテスト計画を選択できます。
+ **テスト計画** - テスト ケースを含む Azure DevOps テスト計画 詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。 

**接続のテスト** を選択し、 Azure DevOps への接続をテストします。

#### <a name="test-environment"></a>テスト環境
テスト環境への接続をコンフィギュレーションします。

+ **ホスト名** – myhost.cloudax.dynamics.com. などのテスト環境のホスト名。 https:// または http:// の接頭語を含めないでください。
+ **SOAP ホスト名** – テスト環境の SOAP ホスト名。 通常は、ホスト名に **soap** の接尾語を追加する必要があります。 たとえば、ホスト名が myhost.cloudax.dynamics.com の場合は、myhost**soap**.cloudax.dynamics.com を SOAP ホスト名として使用します。

    + テスト環境の SOAP ホスト名がわからない場合は、Infrastructure.SoapServicesUrl の AOS サーバーの web.config ファイルで検索できます。
    + テスト環境が、リモート デスクトップ アクセスがないユーザー受け入れテスト (user acceptance testing: UAT) または上位層サンドボックス環境である場合、この SOAP ホスト名はホスト名に一致します。

+ **管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレス。
+ **拇印** – 使用している認証証明書の拇印。

    1. 新しい証明書を作成してインストールするには、 **新規** を選択します。 プロンプトが表示されたら .cer ファイルをどこかに配置して、記録用に保存します。
    2. プロセスが完了すると、新しい証明書がローカル マシンの信頼されたルート店舗にインストールされます。

        ![正常に作成されました。](media/thumbprint-certificate.png)

    3. 新しく作成された証明書の拇印が、このフォームに自動的に挿入されます。 この拇印をコピーし、次のセクションで使用して、接続を信頼するようにAOSをコンフィギュレーションします。

+ **会社名** – Excel パラメーター ファイルの作成時に、既定の会社として使用する会社名を指定します。 後でExcelファイルを編集して変更できます。


#### <a name="run-setting"></a>実行設定
ローカル設定をコンフィギュレーションします。

+ **作業ディレクトリ** - Excel テスト データ ファイルを含むテスト自動化ファイルを格納するフォルダの場所。 たとえば、 **C:\Temp\RegressionTool** のようになります。
+ **既定のブラウザー** - テストの実行に使用するブラウザーを選択します。 RSAT は (新しい) Microsoft Edge、Microsoft Internet Explorer および Google Chrome をサポートします。 [新しい Microsoft Edge の概要](https://www.microsoft.com/edge)から Microsoft Edge ダウンロードすることをお勧めします。 

**OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。 **キャンセル** を選択して変更をキャンセルし、ダイアログ ボックスを閉じます。 **名前を付けて保存** と **開く** ボタンを使用すると、後で再利用するために設定を保存できます。 **名前を付けて保存** を選択して、コンピューターの構成ファイルに現在の設定を保存します。 **開く** を選択して、構成ファイルから設定を復元します。

### <a name="optional-settings"></a>オプション設定
**オプション** タブを選択して、オプションの設定をコンフィギュレーションします。

+ **テストの実行の接頭語** – RSATはテストの実行結果を Azure DevOps に報告します。 テストの実行には、次の規則: **\<Run ID\> \<Prefix\> \<Test Suite\>** に従って名前が付けられます。 この設定を使用して **\<Prefix\>** を設定します。
+ **テストの実行タイムアウト** – テストの実行のタイムアウト (分単位)。 このタイムアウトに達すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは失敗します。
+ **テスト アクションのタイムアウト** – 個々のテスト ステップのタイムアウト (分単位)。 テストステップがタイムアウトになると、テスト ケースは失敗します。
+ **ステップ間の一時停止** – テストケースの自動実行中にテスト ステップ間で一時停止する秒数。 既定値は **0** (ゼロ) です。 監査または調査のために、テストの実行中に強制的に一時停止するには、この値を設定します。 テスト ケースの Excel パラメーター ファイルの**全般**タブにある、**ステップ間の一時停止 (秒)** パラメーターを変更することで、個々のテスト ケースに対して一時停止を指定することもできます。
+ **最初の検証エラーでテストに失敗** – 既定では、テスト ケースに複数の検証ステップがあり、検証に失敗した場合は、最初の失敗が発生するとテスト ケースの実行が停止します。 テスト ケースは失敗としてマークされます。 すべての検証が完了するまでテスト ケースを実行する場合は、このオプションをオフにします。 その後、テスト ケースですべての検証を評価できます。
+ **失敗時にテスト スイートの実行を中止する** – 既定では、いずれかのテスト ケースが失敗した場合でもテスト スイートの実行が続行されます。 このオプションを **True** に設定すると、テスト ケースが失敗した場合にテストの実行が中止されます。 残りのすべてのテスト ケースのステータスは**未実行**になります。
+ **クラウド プロバイダー** – テスト環境のクラウド テナントのプロバイダーを選択します。 サポートされているプロバイダーは、**グローバル** (パブリッククラウド) および**中国** (主権クラウド) です。

    > [!IMPORTANT]
    > Finance and Operations アプリが 21Vianet に配置されている場合、**クラウド プロバイダー** の設定が必要となり、選択された値が **中国** でなければなりません。
+ **Retail POS のコンフィギュレーション**: Microsoft Dynamics 365 Commerce の一部であるクラウド POS の自動テストのために RSAT をコンフィギュレーションするには、このチェックボックスをオンにします。 有効にすると、**設定** ダイアログに **Retail POS** という名前のタブが表示されます。 RSAT とクラウド POS の詳細については、[クラウド POS 用のレコーダーおよび Regression Suite Automation Tool のテスト](../../../../commerce/dev-itpro/pos-rsat) を参照してください。

### <a name="configure-the-test-environment-to-trust-the-connection"></a>接続を信頼するようにテスト環境を構成する

#### <a name="if-your-aos-allows-for-remote-desktop-connections"></a>AOS がリモート デスクトップ接続を許可している場合

証明書を作成した後、テスト自動化接続を信頼するよう AOS をコンフィギュレーションします。 マルチAOS環境では、すべてのAOSマシンに対して次の手順を繰り返します。

1.  AOSマシンへのリモート デスクトップ接続を開きます。
2.  IIS を開き、サイトの一覧で AOSService を見つけます。

    ![IISでのAOSの検索](media/configure-aos.png)

3.  **AOSservice** を右クリックし、 **エクスプローラー** をクリックします。
4.  ファイル **wif.config** を開き、検索します。
  
    ![wif.config を開く](media/open-wif-config.png)

5.  次の例に示すように、新しい機関のエントリを追加して、 **wif.config** ファイルを更新します。 機関名に **127.0.0.1** を使用し、証明書の拇印を貼り付けます。

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

テスト環境でリモート デスクトップ アクセスが許可されていない場合は、次の手順に従って、RSAT 接続を信頼するように環境を構成します。

1. このトピックで前述されているように、RSAT の設定ダイアログ ボックスの**新規**ボタンを使用して、RSAT 認証証明書を作成します。
2. サポート要求を開き、サポート エンジニアに次の情報を提供します。

    - 環境 ID (Microsoft Dynamics Lifecycle Services \[LCS\] の環境ページでこの ID を確認できます。)
    - RSAT によって生成された .cer ファイル
    - サンドボックス環境で許容できるダウンタイム ウィンドウ (ダウンタイムは分単位で表されます。)

### <a name="installation-of-rsat-on-multiple-computers"></a>複数のコンピューターへの RSAT のインストール

テスト環境は、複数の RSAT 接続を信頼するように構成することができます。 複数のコンピューターに RSAT をインストールする場合は、各 RSAT のインストールに対して新しい証明書を生成する必要があります。 証明書を生成し、RSATと同じコンピューターにインストールする必要があります。 RSATがインストールされている複数のクライアントからの接続をAOSに信頼させる場合、AOS wif.config ファイルに複数の拇印エントリを含めることができます。 次の例は、複数の拇印ノードを示しています。

```xml
<keys>
    <add thumbprint="ccbc124d0a119xxxxxxxxxxxxxxxxxxxx841e797" />
    <add thumbprint="bbbbbbbbbbbbbbxxxxxxxxxxxxxxxxxxxx999999" />
</keys>
```

## <a name="install-selenium-drivers"></a>Selenium ドライバーのインストール

Selenium ドライバーを手動でインストールするには、次の手順に従います。
1. [Selenium 3.13.1](https://selenium-release.storage.googleapis.com/3.13/selenium-dotnet-strongnamed-3.13.1.zip) をダウンロードします。 または、 https://docs.seleniumhq.org/download に移動し、 **以前のリリース** をクリックします。 **3.13** を選択して、 **selenium-dotnet-strongnamed-3.13.1.zip** をダウンロードします。
2. Selenium ライブラリをインストールします:
    + ダウンロード ファイルを解凍します。 
    + ファイル **dist\Selenium.WebDriver.StrongNamed.3.13.1.nupkg** を展開します。 このファイルを展開するには、ファイルに .zip拡張子を追加して、解凍します。 
    + **Selenium.WebDriver.StrongNamed.3.13.1.nupkg\lib** という名前のフォルダーの内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** にコピーします。
3.  [Internet Explorer ドライバー バージョン 3.4.0](https://selenium-release.storage.googleapis.com/3.4/IEDriverServer_x64_3.4.0.zip) をダウンロードします。 または、ブラウザーに戻り、**3.4** フォルダを開いて、**IEDriverServer_x64_3.4.0.zip** をダウンロードします。
4.  ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。

Google Chromeをブラウザーとして使用するには、次の手順を実行します:
1. https://sites.google.com/a/chromium.org/chromedriver/downloads に移動します。 
2. 最新/現在のリリースから **chromedriver_win32.zip** をダウンロードします。
3. ダウンロードしたファイルを解凍し、その内容を **C:\Program Files (x86)\Regression Suite Automation Tool\Common\External\Selenium** に移動します。

## <a name="manual-configuration-of-authentication-certificates"></a>認証証明書の手動構成

必要に応じて、RSAT認証証明書を手動で構成することができます。

このプロセスに精通していない場合は、システム管理者に問い合わせてください。 Windows キットがコンピューターにインストールされていることを確認してください。 Windows キットがマシンにインストールされていない場合は、 [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) から Windows 10 SDKをダウンロードできます。 このドキュメントで説明されている手順には、これらのコンポーネントが必要です。

+ デスクトップ アプリ用の Windows SDK 署名ツール
+ UWP マネージド アプリ用のWindows SDK。

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
2. **証明書のインストール** をクリックします。
3. **ローカルマシン > すべての証明書を次のストアにを配置 > 参照 > 信頼済ルート証明機関** を選択し、各画面で **次へ** をクリックします。
4. **パスワード** フィールドは空白のままにします。
5. **証明書** ダイアログ ボックスで、 **詳細** を参照し、 **拇印** を探します。

    ![拇印の一覧を示す証明書ダイアログ](media/certificate-dialog.png)
 
6. 拇印をコピーして保存します。 このトピックで前述されているように、AOS をコンフィギュレーションする必要があります。
