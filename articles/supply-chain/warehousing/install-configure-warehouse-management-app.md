---
title: Warehouse Management モバイル アプリのインストールと接続
description: この記事では、各モバイル デバイスに Warehouse Management モバイル アプリをインストールして、Microsoft Dynamics 365 Supply Chain Management 環境に接続するように構成する方法について説明します。
author: Mirzaab
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1333881f80c735794784831d4042bfe7d070b796
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838475"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリのインストールと接続

[!include [banner](../includes/banner.md)]

この記事では、各モバイル デバイスに Warehouse Management モバイル アプリをダウンロードおよびインストールして、Supply Chain Management 環境へ接続するようアプリを構成する方法について説明します。 各デバイスの設定は手動で行うことも可能ですが、接続設定をファイルで取り込む、またはQRコードをスキャンして取り込むことができます。

## <a name="system-requirements"></a>システム要件

倉庫管理モバイル アプリは、Windows とGoogle Android オペレーティング システムの両方で使用できます。 このアプリを使用するには、モバイル デバイスに次のサポートされているオペレーティング システムの 1 つがインストールされている必要があります。

- Windows 10 (Universal Windows Platform \[UWP\]) 2018 年 10 月更新 1809 (ビルド 10.0.17763) 以降
- Android 4.4 またはそれ以降

## <a name="turn-warehouse-management-mobile-app-features-on-or-off-in-supply-chain-management"></a>Supply Chain Management で Warehouse Management モバイル アプリの機能をオン/オフする

Warehouse Management mobile app を使用するには、ご利用のシステムで *新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル* 機能がオンになっている必要があります。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より以前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル* を検索して、この機能をオンまたはオフにすることができます。

## <a name="get-the-warehouse-management-mobile-app"></a>倉庫管理モバイル アプリケーションを取得する

小規模な配置の場合は、通常、該当のストアから各デバイスにアプリをインストールし、使用している環境への接続を手動で構成します。

大規模な配置の場合は、アプリ配置またはコンフィギュレーションを自動化でき、多くのデバイスを管理するのに便利です。 たとえば、[Microsoft Intune](/mem/intune/fundamentals/what-is-intune) などモバイル デバイス管理やモバイル アプリケーション管理ソリューションを使用する場合があります。 Intune を使用してアプリを追加する方法については、[Microsoft Intune にアプリを追加する](/mem/intune/apps/apps-add) を参照してください。

### <a name="install-the-app-from-an-app-store"></a>アプリ ストアからのアプリのインストール

単一のデバイスにアプリケーションをインストールするもっとも簡単な方法は、常に最新の一般公開バージョンを提供するアプリ ストアからインストールする方法です。 Microsoft Intune は、アプリ ストアからアプリをフェッチすることもできます。 次のいずれかのリンクを使用して、アプリ ストアからアプリをインストールします。

- **Windows (UWP):** [Microsoft Store の倉庫管理](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Google Play ストアの倉庫管理](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Microsoft アプリ センターからアプリをダウンロードする

アプリ ストアからインストールする代わりに、Microsoft アプリ センターからアプリをダウンロードすることもできます。 アプリ センターには、サイドロードできるインストール可能なパッケージが提供されています。 アプリ センターでは、現在のバージョンに加えて、以前のバージョンをダウンロードしたり、試せる今後の機能を備えたプレビュー バージョンが提供されている場合もあります。Microsoft アプリ センターから倉庫管理モバイル アプリの最新バージョン、以前のバージョン、またはプレビュー バージョンをダウンロードするには、次のいずれかのリンクを使用します。

- **Windows (UWP):** [倉庫管理 (Windows)](https://aka.ms/wma-windows-official-release)  
    Windows デバイスにダウンロードしたパッケージをインストールし、必要な証明書を設定する方法の手順については、[アプリ センターからのビルドのインストール](/appcenter/distribution/installation)を参照してください。

- **Android:** [倉庫管理 (Android)](https://aka.ms/wma-android-official-release)  
    プレビュー バージョンをダウンロードする場合、インストールするにはいくつかの追加手順が必要です。 詳細については、[Android アプリをテストする](/appcenter/distribution/testers/testing-android) を参照してください。

App Center からダウンロードしたビルドのインストール方法については、[ビルドのインストール](/appcenter/distribution/installation) を参照してください。

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Azure Active Directoryで Web サービス アプリケーションを作成する

倉庫管理モバイル アプリが特定の Supply Chain Management サーバーとやりとりできるようにするには、Azure Active Directory (Azure AD) の Supply Chain Management テナントに Web サービス アプリケーションを登録する必要があります。 このタスクを完了するに当たっての手順を以下に示します。 詳細と代替手段については、手順の後のリンクを参照してください。

1. Web ブラウザーで、[https://portal.azure.com](https://portal.azure.com/) に移動します。
1. Azure のサブスクリプションにアクセス可能なユーザー名とパスワードを入力します。
1. Azure ポータル左側のナビゲーション ウィンドウで、**Azure Active Directory** を選択します。

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Azure AD Supply Chain Management が使用するインスタンスで作業をしていることを確認してください。
1. **管理** の一覧で、**アプリの登録** を選択します。

    ![アプリの登録。](media/app-connect-azure-register.png "アプリの登録")

1. ツールバーの **新規登録** を選択して、**アプリケーションの登録** ウィザードを開きます。
1. アプリケーションの名前を入力し、**この組織ディレクトリ内のアカウントのみ** オプションを選択し、続いて **登録** を選択します。

    ![アプリケーション ウィザードを登録する。](media/app-connect-azure-register-wizard.png "アプリケーション ウィザードを登録する")

1. 新しいアプリの登録が開きます。 後の手順で必要となるため、**アプリケーション (クライアント) ID** の値をメモしておきます。 この ID はこの記事の後半で、*クライアント ID* として参照されます。

    ![アプリケーション (クライアント) ID。](media/app-connect-azure-app-id.png "アプリケーション (クライアント) ID")

1. **管理** リストにて、**証明書 & シークレット** を選択します。 続いて、アプリの認証の構成方法に応じて、次のいずれかのボタンを選択します。 (詳細については、この記事の後半の[証明書またはクライアント シークレットを使用した認証](#authenticate) のセクションを参照してください。)

    - **証明書のアップロード** – 秘密に使用する証明書をアップロードします。 この方法は安全性が高い上に、より完全な自動化もできるため、この方法を推奨します。 Windows デバイスで倉庫管理モバイル アプリを実行している場合は、証明書をアップロードした後に表示される **サムプリント** 値を書き留めておきます。 この値は、Windows デバイスで証明書を構成する際に必要になります。
    - **新しいクライアント シークレット** – **パスワード** セクションにキーの説明と期間を入力してキーを作成し 、**追加** を選択します。 キーのコピーを作成し、安全に保管します。

    ![証明書 & シークレット。](media/app-connect-azure-authentication.png "証明書 & シークレット")

Azure ADでの web サービス アプリケーションの設定方法の詳細については、次のリソースを参照してください:

- Azure AD で、Windows PowerShell を使用した web サービス アプリケーションの設定方法については、[Azure PowerShell を使用して、証明書でサービス プリンシパルを作成する方法](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)を参照してください。
- Azure AD で web サービス アプリケーションを手動で作成する方法の詳細については 、次の記事を参照してください:

    - [クイックスタート: Microsoft ID プラットフォームにアプリケーションを登録する](/azure/active-directory/develop/quickstart-register-app)
    - [ポータルを使用して、リソースにアクセスできる Azure AD アプリケーションとサービス プリンシパルを作成する](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Supply Chain Management でユーザー アカウントを作成および設定する

Supply Chain Management を有効にして Azure AD アプリケーションを使用するには、次の手順に従います。

1. 倉庫管理モバイル アプリで使用するユーザーの資格情報に対応するユーザーを作成します。

    1. Supply Chain Management で、**システム管理 \> ユーザー \> ユーザー** に移動します。
    1. ユーザーを作成します。
    1. ユーザーに *倉庫のモバイル デバイス ユーザー* のロールを割り当てます。

    ![倉庫のモバイル デバイス ユーザーを割り当てます。](media/app-connect-app-users.png "倉庫モバイル デバイスのユーザーを割り当てる")

1. Azure AD アプリケーションと倉庫管理モバイル アプリのユーザーを関連付けます。

    1. **システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動します。
    1. アクション ペインで **新規** を選択して、明細行を作成します。
    1. **クライアント ID** フィールドで、前のセクションでメモしたクライアント ID を入力します。
    1. **名前** フィールドに、名前を入力します。
    1. **ユーザー ID** フィールドで、作成したユーザー ID を選択します。

    ![Azure Active Directory アプリケーション。](media/app-connect-aad-apps.png "Azure Active Directory アプリケーション")

> [!TIP]
> これらの設定を利用する 1 つの方法として、物理デバイスごとに Azure でクライアント ID を作成し、各クライアント ID を **Azure Active Directory アプリケーション** ページに追加します。 また、デバイスを紛失した場合は、そのデバイスのクライアント ID を削除することで、Supply Chain Management へのアクセスを簡単に解除することができます。 (この方法が有効なのは、後述するように、各デバイスに保存されている接続認証情報にクライアント ID が指定されているためです。)
>
> また、各クライアント ID の既定の言語、数値フォーマット、タイムゾーンの設定は、ここにマッピングされている **ユーザー ID** の値に設定されている環境設定によって確立されます。 そのため、これらの環境設定を利用して、クライアント ID に基づいて、各デバイスやデバイスのコレクションの既定の設定を設定できます。 ただし、これらの既定の設定は、作業者がデバイスにサインインする際に使用する *倉庫アプリのユーザー アカウント* にも定義されている場合は、上書きされます。 (詳細については、[作業者のモバイル デバイスのユーザー アカウント](mobile-device-work-users.md)を参照してください。)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>証明書またはクライアント シークレットを使用した認証

Azure AD の認証をすることで、モバイル デバイスを Supply Chain Management に安全に接続することができます。 証明書またはクライアント シークレットを使用して認証できます。 接続の設定をインポートする場合は、クライアント シークレットの代わりに証明書を使用することを推奨します。 この記事で後述するとおり、クライアント シークレットは常に安全に保管されている必要があるため、接続設定ファイル、または QR コードからインポートすることはできません。

証明書は、トークンを要求された際に、アプリケーションの ID を証明する秘密として使用することができます。 証明書の公開部分は Azure portal のアプリ登録にアップロードされますが、完全な証明書は倉庫管理モバイル アプリがインストールされている各デバイスに配置する必要があります。 組織では、ローテーションなどの観点から証明書を管理する責任があります。 自己署名付き証明書を使用することはできますが、常にエクスポートされていない証明書を使用する必要があります。

倉庫管理モバイル アプリを実行する各デバイスで、証明書をローカルで使用できるようにする必要があります。 Intune を使用している場合に、Intune 管理デバイスの証明書を管理する方法については、[Microsoft intune での認証に証明書を使用する](/mem/intune/protect/certificates-configure)を参照してください。

## <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>クラウドおよびエッジ スケール ユニット用 Warehouse Management モバイル アプリの構成

クラウドまたはエッジ スケール ユニットに対して Warehouse Management モバイル アプリを実行する場合は、他の手順が必要です。 詳細については、[クラウドおよびエッジ スケール ユニット用 Warehouse Management モバイル アプリの構成](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md) を参照してください。

## <a name="configure-the-application-by-importing-connection-settings"></a>接続設定をインポートしてアプリケーションを構成する

多くのモバイルデバイス上でのアプリケーションの保守と配置を容易にする目的で、各デバイスでは接続設定を手動で入力するのではなく、インポートすることができます。 ここでは、設定の作成方法とインポート方法について説明します。

### <a name="create-a-connection-settings-file-or-qr-code"></a>接続設定ファイル、またはQRコードを作成する

接続設定は、ファイルまたは QR コードからインポートできます。 いずれの方法でも、最初に JavaScript Object Notation (JSON) 形式と構文を使用した設定ファイルを作成する必要があります。 ファイルには、追加する必要のある個々の接続を含む接続のリストを含める必要があります。 次の表には、接続設定ファイルで指定する必要のあるパラメータをまとめています。

| パラメーター | 説明 |
|---|---|
| ConnectionName | 接続設定の名前を入力します。 最大 20 文字まで指定できます。 この値は、接続設定の固有の ID てあるため、リスト内で一意となっていることを確認してください。 デバイスに同じ名前の接続が既に存在する場合、インポートされたファイル設定によって上書きされます。 |
| ActiveDirectoryClientAppId | [Azure Active Directory で Web サービス アプリケーションを作成する](#create-service) セクションの Azure AD の設定でメモしたクライアント ID を入力します。 |
| ActiveDirectoryResource | Supply Chain Management のルート URL を入力します。 |
| ActiveDirectoryTenant | Supply Chain Management サーバーで使用する Azure AD ドメイン名を入力します。 この値は次のような形式です: `https://login.windows.net/<your-Azure-AD-domain-name>` 次に例を示します: `https://login.windows.net/contosooperations.onmicrosoft.com`。 Azure AD ドメイン名を確認する方法の詳細については、[ユーザーの重要な ID を検索する](/partner-center/find-ids-and-domain-names) を参照してください。 |
| 法人 | アプリケーションが接続する Supply Chain Management の法人を入力します。 |
| ConnectionType | (オプション) 接続設定で、環境に接続する際に証明書を使用するか、クライアント シークレットを使用するかを指定します。 有効な値は、*certificate* および *clientsecret* です。 既定値は *certificate* です。<p>**注意 :** クライアント シークレットはインポートできません。</p> |
| IsEditable | (オプション) アプリのユーザーが接続設定を編集できるようにするかどうかを指定します。 有効な値は、*true* および *false* です。 既定値は *true* です。 |
| IsDefault | (オプション) 接続が既定の接続であるかどうかを指定します。 既定の接続として設定されている接続は、アプリが開かれた際に自動的に設定が選択されます。 既定の接続にはひとつの接続のみを設定できます。 有効な値は、*true* および *false* です。 既定値は *false* です。 |
| CertificateThumbprint | (オプション) Windows デバイスでは、接続に使用する拇印の証明書を指定できます。 Android デバイスの場合、アプリのユーザーは初回の接続時に証明書を選択する必要があります。 |

次の例では、2 つの接続を含む有効な接続設定ファイルを示しています。 こように、接続リスト (ファイル内の  *connectionlist* と呼ばれます) は、各接続をオブジェクトとして格納する配列を持つオブジェクトです。 各オブジェクトは、かっこ ({}) で囲み、コンマで区切る必要があります。また、配列は角かっこ (\[\]) で囲む必要があります。

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

この情報は、JSON ファイルとして保存するか、または同内容の QR コードを生成することができます。 ファイルとして保存する場合、特に各モバイル端末の既定の場所に保存する場合は、*connections.json* という名前で保存することを推奨します。

### <a name="save-the-connection-settings-file-on-each-device"></a>接続設定のファイルを各デバイスに保存します

通常は、デバイス管理ツールまたはスクリプトを使用して、接続設定ファイルを管理しているそれぞれのデバイスに配布します。 接続設定ファイルを各デバイスに保存する際に既定の名前と場所を使用すると、倉庫管理モバイル アプリのインストール後の初回実行時にも自動的にインポートされます。 ファイルにカスタムの名前や場所を使用する場合は、初回実行時にアプリ ユーザーが値を入力する必要があります。 ただし、アプリはその後も指定された名前と場所を使用します。

アプリを起動するたびに、以前の場所からの接続設定を再インポートし、変更があったかどうかを判断します。 アプリは、接続設定ファイルの接続と同じ名前の接続のみを更新します。 他の名前を使用しているユーザーが作成した接続は更新されません。

接続設定ファイルを使用して接続を削除することはできません。

前述の通り、既定のファイル名は *connections.json* です。 既定のファイルの場所は、Windows デバイスを使用しているか Android デバイスを使用しているかによって異なります。

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

通常、このパスは、アプリを初回実行した後に自動的に作成されます。 ただし、インストール前に接続設定ファイルをデバイスに転送する必要がある場合は、手動で作成することができます。

> [!NOTE]
> アプリをアンインストールすると、既定のパスとその内容が削除されます。

### <a name="import-the-connection-settings"></a>接続設定のインポート

ファイル、または QR コードから接続設定をインポートするには、次の手順に従ってください。

1. モバイル デバイスで倉庫管理モバイル アプリを起動します。 アプリを初めて起動すると、ようこそメッセージが表示されます。 **接続の選択** を選択します。

    ![ようこそメッセージ。](media/app-configure-welcome-screen.png "ようこそメッセージ")

1. ファイルから接続設定をインポートしている場合で、ファイル保存時に既定の名前と既定の場所が使われていた場合、アプリがすでにファイルを検出している可能性があります。 この場合は手順4. に進みます。 接続していない場合は、**接続の設定** を選択して、手順3 に進みます。

    ![接続を設定。](media/app-configure-set-up-connection.png "接続を設定")

1. **接続の設定** ダイアログ ボックスで、設定のインポート方法に応じて **ファイルから追加** または **QR コードから追加** を選択します。

    - 接続設定をファイルからインポートする場合は、**ファイルから追加** を選択し、ローカル デバイスのファイルを参照して選択します。 ユーザー定義の場所を選択した場合は、その場所が保管され、次回自動的に使用されます。
    - QR コードをスキャンして接続の設定をインポートする場合は、**QR コードから追加** を選択します。 アプリ上に、デバイスのカメラを使用するかどうかを確認するメッセージが表示されます。 アクセス許可を付与すると、カメラが起動し、スキャンに使用できるようになります。 デバイスのカメラの品質および QR コードの複雑さによっては、正しいスキャンの取得が困難な場合があります。 その場合は、1 つの QR コードにつき 1 つだけの接続を生成することで、QR コードの複雑性を軽減することを試してください。 (現時点では、QR コードのスキャンにはデバイスのカメラのみを使用できます)

    ![接続の設定メニュー。](media/app-configure-connection-setup-flyout.png "接続の設定メニュー")

1. 接続設定が正常に読み込まれると、選択した接続が表示されます。

    ![読み込まれた接続設定。](media/app-configure-select-connection.png "読み込まれた接続設定")

1. Android デバイスを使用していて、かつ認証に証明書を使用している場合は、デバイスにで証明書の選択を促す画面が表示されます。

    ![Android デバイス上の証明書プロンプトを選択する。](media/app-configure-select-certificate.png "Android デバイス上の証明書プロンプトを選択する")

1. アプリケーションが Supply Chain Management サーバーに接続し、サイン インページが表示されます。

    ![サインイン ページ。](media/app-configure-sign-in-page.png "サインイン ページ")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>アプリケーションを手動で構成する

ファイルや QR コードがない場合は、デバイスのアプリを手動で設定して、Azure AD アプリを経由して Supply Chain Management サーバーに接続することができます。

1. モバイル デバイスで倉庫管理モバイル アプリを起動します。
1. アプリが **デモ モード** で開始された場合は、**接続設定** を選択します。 アプリの起動時に **サインイン** ページが表示される場合は、**接続の変更** を選択します。
1. **接続設定** タブを選択します。

    ![接続を設定。](media/app-configure-set-up-connection.png "接続を設定")

1. **手動で入力** を選択します。

    ![接続の設定メニュー。](media/app-configure-connection-setup-flyout.png "接続の設定メニュー")

    **新規接続** ページが表示され、接続の詳細を手動で入力するために必要な設定が表示されます。

    ![手動接続フィールド。](media/app-configure-input-manually.png "手動接続フィールド")

1. 次の情報を入力します。

    - **クライアント シークレットを使用する** – このオプションを _はい_ に設定すると、クライアント シークレットを使用して Supply Chain Management の認証ができます。 認証に証明書を使用するには、_いいえ_ に設定します。 (詳細については、この記事の前半の [Azure Active Directory に Web サービス アプリケーションを作成する](#create-service) セクションを参照してください。)
    - **接続名称** – 新しい接続の名前を入力します。 この名前は、次に接続設定を開いたときに **接続の選択** フィールドに表示されます。 入力する名称は一意である必要があります。 (この名称は、デバイスに保存されている他のすべての接続名とは異なるものでなければなりません。)
    - **アクティブ ディレクトリ クライアント ID** – ここには、[Azure Active Directory で Web サービス アプリケーションを作成する](#create-service) のセクションで Azure AD の設定を行った際にメモしたクライアント ID を入力してください。
    - **アクティブ ディレクトリのクライアント シークレット** – このフィールドは、**クライアント シークレットを使用する** オプションが _はい_ に設定されている場合にのみ使用できます。 [Azure Active Directory で Web サービス アプリケーションを作成する](#create-service)のセクションで Azure AD の設定を行った際にメモしたクライアント シークレットを入力してください。
    - **アクティブ ディレクトリの認証に使用するサムプリント** – このフィールドは、Windows デバイスで **クライアント シークレットを使用する** オプションが _いいえ_ に設定されている場合にのみ使用できます。 [Azure Active Directory で Web サービス アプリケーションを作成する](#create-service)のセクションで Azure AD の設定を行った際にメモした認証用の拇印を入力してください。
    - **アクティブ ディレクトリのリソース** – Supply Chain Management のルート URL を入力します。

        > [!IMPORTANT]
        > この値の末尾には、スラッシュ (/) を入力しないでください。
        > HTTPS (SSL) 証明書が有効である必要があります。

    - **Active Directory テナント** - Supply Chain Management サーバーで使用している Azure AD のドメイン名を入力します。 この値は次のような形式です: `https://login.windows.net/<your-Azure-AD-domain-name>` 次に例を示します: `https://login.windows.net/contosooperations.onmicrosoft.com`。 Azure AD ドメイン名を確認する方法の詳細については、[ユーザーの重要な ID を検索する](/partner-center/find-ids-and-domain-names) を参照してください。

        > [!IMPORTANT]
        > この値の末尾には、スラッシュ (/) を入力しないでください。

    - **会社** - アプリケーションが接続する Supply Chain Management 内の法人 (会社) を入力してください。

1. ページの右上隅にある **保存** ボタンを選択します。
1. Android デバイスを使用していて、かつ認証に証明書を使用している場合は、デバイスにで証明書の選択を促す画面が表示されます。
1. アプリケーションが Supply Chain Management サーバーに接続し、サイン インページが表示されます。

## <a name="remove-access-for-a-device"></a>デバイスへのアクセスを削除する

デバイスが紛失したりセキュリティが侵害された場合、デバイスの Supply Chain Management へのアクセスを削除する必要があります。 次の手順では、アクセス権を削除するにあたっての推奨されるプロセスについて説明します。

1. **システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動します。
1. アクセス権を削除するデバイスに該当する行を削除します。 後の手順で必要となるため、削除されたデバイスに使用されていたクライアント ID をメモしておきます。

    クライアント ID を1つしか登録しておらず、複数のデバイスが同じクライアント ID を使用している場合は、それらのデバイスに新しい接続設定をプッシュする必要があります。 これを行わない場合は、アクセス権が失われます。

1. Azure ポータルにログインします: [https://portal.azure.com](https://portal.azure.com/)
1. 左側のナビゲーション ウィンドウで、**アクティブ ディレクトリ** を選択し、正しいディレクトリにいることを確認してください。
1. **管理** の一覧で、**アプリの登録** を選択し、続いて構成するアプリケーションを選択します。 **設定** ページが表示され、構成の情報が表示されます。
1. アプリケーションのクライアント ID が手順 2 でメモしたクライアント ID と一致していることを確認してください。
1. ツール バーで、**削除** を選択します。
1. 確認メッセージが表示されたら、**はい** を選択します。

## <a name="additional-resources"></a>追加リソース

- [モバイル デバイスのユーザー設定](mobile-device-user-settings.md)
- [Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て](step-icons-titles.md)
- [クラウドおよびエッジ スケール ユニット用 Warehouse Management モバイル アプリの構成](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
