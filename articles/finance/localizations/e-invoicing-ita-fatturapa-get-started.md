---
title: イタリアの FatturaPA と SDI の直接統合を設定する
description: この記事では、イタリア向けの電子請求を開始して、Italian FatturaPA と取引システム (SDI) の直接統合を設定する際に役立つ情報を提供します。
author: gionoder
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e050d3896b2ba10433e166995d6fc405996cf0b2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267159"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>イタリアの FatturaPA と SDI の直接統合を設定する

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> イタリア向けの電子請求は、現時点では Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management の電子請求書で利用できるすべての機能に対応していない可能性があります。

この記事では、Finance および Supply Chain Management でイタリア向けの電子請求を使い始めるための情報を提供します。 このガイドでは、Regulatory Configuration Services (RCS) が含む国/地域ごとに異なる構成手順について説明します。 これらの手順は、[電子請求を開始する](e-invoicing-get-started.md) で説明した手順を補完します。

## <a name="prerequisites"></a>必要条件

この記事の手順を完了する前に、次の前提条件を満たす必要があります。

- [電子請求を開始する](e-invoicing-get-started.md) の手順を完了します。
- **Italian FatturaPA (IT)** 電子請求機能をグローバル リポジトリから RCS にインポートします。 詳細については、前述の 「電子請求を開始する」 記事の [Microsoft 構成プロバイダから電子請求機能をインポートする](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) セクションを参照してください。
- 必要な証明書からサービス環境にリンクを追加します。 必要な証明書: デジタル署名証明書、証明機関 (CA) 証明書、クライアント証明書。 詳細については、「電子請求サービスの管理を開始する」 記事の [デジタル証明書シークレットを作成する](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) セクションを参照してください。

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Italian FatturaPA (IT) 電子請求機能の国別コンフィギュレーション

連携した Finance や Supply Chain Management アプリにアプリケーション設定を展開する前に、次の手順を実行してください。

このセクションは 「電子請求を開始する」 記事の [アプリケーション設定の国別コンフィギュレーション](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) セクションを補完します。

### <a name="create-a-new-feature"></a>新しい機能を作成する

1. RCS にサインインします。
2. **電子申告** ワークスペースの **構成プロバイダー** セクションで、会社の構成プロバイダーをアクティブとしてマークします。
3. **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。
4. **電子請求機能** ページで **追加** \> **既存の機能に基づく** を順に選択します。
5. **Microsoft 構成プロバイダー** 配下の **Italian FatturaPA (IT)** を基本機能として選択し、名前を入力してから **機能の作成** を選択します。

### <a name="set-up-application-specific-parameters"></a>申請固有のパラメーターの設定

1. **電子請求機能** ページで編集する機能を選択します。
2. **バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。
3. **Configurations** タブで構成を選択し、**アプリケーション固有のパラメーター** を選択します。
4. **検索** セクションで、**Natura 逆請求サブ カテゴリーの一覧** 検索が選択されていることを確認します。
5. **条件** セクションで **追加** を選択します。
6. システムで定義したサブカテゴリごとに特定の条件を追加し、その変更を保存します。

    > [!NOTE]
    > **名前** 列では、特定の値の代わりに **\*空白\*** や **\*空白でない\*** プレースホルダー値を選択できます。

### <a name="configure-a-processing-pipeline-for-export"></a>エクスポートに使用する処理パイプラインを構成する

1. **電子請求機能** ページで編集する機能を選択します。
2. **設定** タブで **売上請求書** を選択し、**編集** を選択します。
3. **処理パイプライン** セクションでアクションを実行し、必須フィールドをすべて設定します。

    - **ドキュメントに署名** アクションの場合は **証明書名** フィールドにデジタル署名証明書を指定します。
    - **送信** アクションの場合は **URL アドレス** と **証明書** フィールドを設定します。 **証明書** フィールドの値は証明書のチェーンであり、最初の証明書はルート CA 証明書 (caentrate.cer) であり、2 番目の値はクライアント証明書です。

4. **適合性ルール** セクションで、句を実行し、必要なフィールドの確認または設定を行います。
    - **LegalEntityID** 句を確認し、法人の正しい値を使用して更新します。

5. **検証** を選択して、必須フィールドを必ずすべて設定します。
6. 変更を保存して、ページを閉じます。
7. **設定** タブで **プロジェクト請求書** を選択し、**編集** を選択します。
8. プロジェクト請求書について手順 3 〜 6 を繰り返します。

### <a name="configure-the-processing-pipeline-for-import"></a>インポートに使用する処理パイプラインを構成する

1. **電子請求機能** ページで編集する機能を選択します。
2. **設定** タブで **請求書のインポート** を選択し、**編集** を選択します。
3. **データ チャネル** セクションの **パラメーター** タブの **データ チャネル** フィールドに、文字列値を入力します。
4. **適合性ルール** タブで、設定フィールドを設定します。 前の手順で **データ チャネル** フィールドに設定した値を **値** フィールドに渡すことで、既定の **チャネル** 句を使用できます。

    ![適合性ルールを設定します。](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. **検証** を選択して、必須フィールドを必ずすべて設定します。

### <a name="deploy-the-feature"></a>機能を展開する

1. 機能を完成させて公開し、サービス環境に展開します。 詳細については 「電子請求を開始する」 記事の [サービス環境に電子請求機能をデプロイする](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) セクションを参照してください。
2. 連携したアプリケーションに機能を展開します。 詳細については 「電子請求を開始する」 記事の [連携したアプリケーションに電子請求機能をデプロイする](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) セクションを参照してください。

### <a name="set-up-finance"></a>Finance を設定する

1. Finance 環境にサインインします。
2. **電子レポート** ワークスペースの、**構成プロバイダー** セクションで、**Microsoft** タイルを選択します。
3. **リポジトリ** \> **グローバル** \> **開く** を順に選択します。
4. **顧客請求書コンテクスト モデル** と **仕入先請求書のインポート (IT)** の構成を選択し、インポートします。
5. **組織管理** \> **設定** \> **電子ドキュメント パラメーター** に移動します。
6. **機能** タブで **イタリアの電子請求書** 機能を見つけて選択し、**有効化** チェックボックスを選択します。
7. **電子ドキュメント** タブで **顧客請求書仕訳帳** と **プロジェクト請求書** のフィールドを、[アプリケーションの設定を構成する](e-invoicing-get-started.md#configure-the-application-setup) の情報に必ず従って設定します。

### <a name="set-up-vendor-invoice-import"></a>仕入先請求書のインポートを設定する 

1. Finance の **電子申告** ワークスペースの **構成プロバイダー** セクションで、会社の構成プロバイダーをアクティブとしてマークします。
2. **コンフィギュレーションをレポートする** を選択します。
3. **顧客請求書コンテクスト モデル** と **構成の作成** を順に選択します。
4. **名前から派生する: 顧客請求書コンテキスト、Microsoft** を選択し、派生した構成を作成します。
5. **ドラフト** バージョンで **デザイナー** を選択します。
6. **データ モデル** ツリーで **モデルをデータ ソースにマップする** を選択します。
7. **定義** ツリーで **DataChannel** を選択し、**デザイナー** を選択します。
8. **データ ソース** ツリーで、**\$コンテキスト\_チャネル** コンテナーを展開します。
9. **値** フィールドで **編集** を選択します。 
10. データ チャネルの名前を入力します。 名前は最大 10 文字にする必要があります。 RCS の電子請求機能のデータ チャネルで使用する **Data channel** パラメーターの値と、これを一致させる必要があります。
11. この変更を保存してから **申告の構成** \> **完全な構成バージョン** に移動します。
12. **外部チャンネル** タブの **チャンネル** セクションで、**追加** を選択します。
13. **チャネル** フィールドに **\$コンテキスト チャンネル** 値を入力します。
14. **説明** と **会社** のフィールドに値を入力します。
15. **ドキュメント コンテキスト** フィールドで、**顧客請求書コンテキスト モデル** から派生した新しい構成を選択します。 マッピングの説明は、**データ チャネル コンテキスト** である必要があります。
16. **インポート ソース** タブで **追加** を選択し、次の値を設定します。

    - **名前:** OutputFile
    - **データ エンティティ名:** 仕入先請求書ヘッダー (**データ エンティティ:** VendorInvoiceHeaderEntity)
    - **モデル マッピング:** 仕入先請求書インポート (IT)

> [!NOTE]
> さまざまなソースからベンダーの請求書をインポートする場合は、異なる **\$コンテキスト チャンネル** 値を持つ、複数の外部チャネルといくつかの派生構成を作成できます。 たとえば、さまざまな法人のベンダー請求書をインポートする場合に利用します。

## <a name="proxy-server-setup"></a>プロキシ サーバーを設定する

このセクションでは、取引システム (SDI) と電子請求サービスの通信に使用するプロキシ サービスを設定および構成する際に役立つ情報を提供します。

### <a name="create-an-app-registration"></a>アプリ登録を作成する

1. 次の Windows PowerShell スクリプトを使用して、サービス間 (S2S) 認証に使用する自己署名証明書を作成します。

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. .pfx 証明書ファイルを Key Vault に保存し、ローカル コピーを削除します。
3. 管理者として [Azure ポータル](https://portal.azure.com) にサインインします。
4. SDI プロキシ サービスのアプリ登録を作成します。

    1. **App registrations** に移動して登録を作成し、次の値を設定します。

        - **名前:** SDI プロキシ クライアント
        - **サポートするアカウント タイプ:** この組織ディレクトリが含むアカウントのみ (1 件のテナント)

    2. **レジスター** を選択して、先ほど作成したアプリ登録を選択します。
    3. **API アクセス許可** に移動して **管理者の同意を付与する** を選択します。
    4. **証明書とシークレット** に移動して **証明書のアップロード** を選択し、S2S 認証に使用する .cer 証明書ファイルをアップロードします。
    5. **エンタープライズ アプリケーション** に移動して、作成したアプリを選択します。
    6. アプリの **アプリケーション ID** (クライアント ID) 値と **オブジェクト ID** 値を保存します。
    7. 請求サービス チームは、サービスへのアクセス許可をアプリに付与する必要があります。 次のパラメーターの値を <D365EInvoiceSupport@microsoft.com> に送信します。

        - AAD テナント ID
        - LCS 環境 ID
        - アプリケーション ID
        - オブジェクト ID

5. RCS で、サービス環境のアプリケーション リストにアプリを追加します。

    1. **グローバリゼーション機能** \> **環境** \> **電子請求** \> **サービス環境** に移動して、環境を選択します。
    2. **アプリケーション** セクションでグリッドに行を追加し、アプリの名前とオブジェクト ID を入力します。

        ![アプリケーションをサービス環境に追加します。](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. **保存** を選択してから、**発行** を選択します。

### <a name="create-an-azure-virtual-machine"></a>Azure 仮想マシンを作成する

1. [Azure ポータル](https://portal.azure.com) で **仮想マシン** に移動して **新規作成** を選択します。
2. **基本** タブで、自分のサブスクリプションとリソース グループを選択します。 Key Vault と Blob ストレージが存在するサブスクリプションとリソース グループを、この値に指定する必要があります。
3. リージョンを選択します。 この値には Finance 環境を展開したリージョンを指定する必要があります。
4. 管理者のユーザー名とパスワードを追加して Key Vault に保存します。
5. **受信ポートを選択する** フィールドで **HTTPS (443)** と **RPD (3389)** を選択します。

    > [!NOTE]
    > システムを実稼働環境に移行する際は、**RDP (3389)** ポートを無効化することを推奨します。 トラブルシューティングの目的で仮想マシン (VM) に接続する必要がある場合は、再度有効化できます。

    ![基本タブでフィールドを設定し、Azure VM を作成します。](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. **ディスク** タブの **詳細** ファストタブ で、**マネージド ディスクを使用する** チェックボックスを選択します。 **エフェメラル OS ディスク** チェックボックスはオフのままにします。

    ![ディスク タブでフィールドを設定し、Azure VM を作成します。](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. **ネットワーク** タブの **パブリック IP** フィールド配下で、**新規作成** を選択します。

    ![ネットワーク タブでフィールドを設定し、Azure VM を作成します。](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. **パブリック IP アドレスを作成する** ダイアログボックスの **SKU** フィールド グループで **標準** オプションを選択します。 **割り当て** フィールド グループで **静的** オプションを選択します。

    ![パブリック IP アドレスを作成します。](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. **管理** タブで **自動シャットダウン** チェックボックスをオフにして、自動シャットダウンを無効化します。
10. **ゲスト OS の更新** フィールドを **手動** に設定し、その他のポリシーを設定します。
11. VM を確認し、作成します。
12. 新しい VM で **ID** \> **システムによる割り当て** に移動し、**状態** オプションを **オン** に設定します。
13. Key Vault へのアクセス許可を VM に付与します。

    1. Key Vault で **アクセス制御 (IAM)** \> **ロールの割り当て** に移動します。
    2. **ロール割り当ての追加** を選択して次のフィールドを設定します。

        1. **ロール** フィールドに **Key Vault シークレット ユーザー** を指定します。
        2. **アクセス許可の割り当て先** フィールドに **仮想マシン** を指定します。
        3. **サブスクリプション** フィールドに自分のサブスクリプションを指定します。
        4. **選択** フィールドに VM を指定します。

    3. **アクセス許可ポリシー** に移動します。
    4. **アクセス許可ポリシーの追加** を選択して次のフィールドを設定します。

        1. **選択したプリンシパル** フィールドで自分の VM を選択します。
        2. **証明書** セクションで **リスト** と **取得** のアクセス許可を選択します。

14. [Azure ポータル](https://portal.azure.com) で **パブリック IP アドレス** に移動し、VM で作成した IP アドレスを選択します。
15. **構成** に移動してドメイン ネーム システム (DNS) の名前を設定します。

### <a name="prepare-the-proxy-service-environment"></a>プロキシ サービス環境を準備する

プロキシ サービスをホストするコンピューターで、次の手順に従います。

1. リモート デスクトップ接続を使用して VM に接続します。
2. ローカル マシン証明書のスナップインを開きます。 詳細については [手順: MMC スナップインで証明書を表示する](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) を参照してください。
3. 実稼働で使用する **caentrate.cer** 証明書とテストで使用する **CAEntratetest.cer** を [信頼されたルート証明機関ストア](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores) にインポートします。 (**CAEntratetest.cer** は機関が提供したルート CA 証明書です。)
4. コントロール パネルで **Windows 機能のオン/オフ切り替え** を開くか、サーバー オペレーティング システム (OS) の **サーバー マネージャー** \> **ロールと機能の追加** に移動して、インターネット インフォメーション サービス (IIS) 機能をオンにします。

    - Web 管理ツール
        - IIS 管理コンソール
    - World Wide Web サービス
        - アプリケーション開発機能
            - .NET 拡張性 4.7 (または 4.8)
            - ASP
            - ASP.NET 4.7 (または 4.8)
            - CGI
            - ISAPI 拡張機能
            - ISAPI フィルター
        - 一般的な HTTP 機能
            - 既定のドキュメント
            - ディレクトリ参照
            - HTTP エラー
            - 静的コンテンツ
        - 正常性と診断
            - HTTP ログ
            - 追跡
        - パフォーマンス機能
            - 静的コンテンツの圧縮
        - セキュリティ
            - 要求のフィルター

    ![IIS 機能をオンにします。](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>IIS で SDI プロキシ サービスを設定する

1. Microsoft Dynamics Lifecycle Services (LCS) で共有資産ライブラリに移動し、資産タイプとして **データ パッケージ** を選択します。
2. **電子請求サービス SDI プロキシ** を見つけて VM にダウンロードします。
3. サービスを構成します。

    1. ダウンロードした **電子請求サービス SDI プロキシ** アーカイブ フォルダーを解凍します。
    2. **src\\FattureService** フォルダーで **appsettings.json** ファイルを開き、次のパラメーターを設定します。

        - **KeyVaultUri** – 請求サービスのクライアント証明書を格納する Key Vault のアドレスを指定します。
        - **TenantId** – 顧客のテナントのグローバル一意識別子 (GUID) を指定します。
        - **EnvironmentId** – LCS 環境の ID を指定します。
        - **ClientId** – 顧客のテナントが含む中間サービス アプリ登録のアプリ ID を指定します。
        - **ClientCertificateName** – Key Vault で S2S 証明書の名前を指定します。
        - **SecurityServiceClientOptions.Endpoint** – セキュリティ サービスの URL を指定します。
        - **SecurityServiceClientOptions.Resource** – トークンを取得する範囲を指定します。
        - **InvoicingServiceClientOptions.Endpoint** – 請求サービスのエンドポイントを指定します。 この値には、RCS と Finance で使用するエンドポイントと同じ値を指定します。
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – サービス環境の名前を指定します。 この値には Finance 環境の名前を指定します。
        - **NotificationsFolder** – 受信通知ファイルを保存するフォルダーを指定します。

    3. **web.config** ファイルで次の行を見つけ、プロキシ サーバー証明書の拇印を追加します。

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > システムを本番環境に移行する際は、web.config ファイルの値をいくつか変更すると、収集するログ情報の量を減らして、ディスク容量を節約できます。 **\<system.diagnostics\>\<source\>** ノードで **switchValue** の値を **重大、エラー** に変更します。 詳細については [MS サービス追跡ビューア](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) を参照してください。

4. IIS マネージャーを開きます。 左側のツリーでルート ノードを表示します。 右側で **サーバー証明書** を選択します。

    ![IIS マネージャーでサービス証明書を選択します。](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. メニューを開いて **インポート** を選択します。
6. **証明書のインポート** ダイアログ ボックスの **証明書ファイル (.pfx)** フィールドで、プロキシ サーバー証明書の .pfx ファイルのパスを指定します。

    ![プロキシ サービス証明書ファイルを指定します。](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. **サイト** を選択したまま (または右クリック) の操作で **Web サイトの追加** を選択します。
8. **Web サイトの追加** ダイアログ ボックスの **サイト名** フィールドに、サイトの名前を入力します。
9. **物理パス** フィールドで **src\\FattureService** フォルダーをポイントします。
10. **バインドの種類** フィールドで **https** を選択します。
11. **ホスト名** フィールドでホスト名を指定します。
12. **IP アドレス** と **ポート** のフィールドは既定値のままに設定します。
13. SDI はこのテクノロジに対応していないため、**Server Name Indication を要求する** チェックボックスは必ずオフに設定します。
14. **SSL 証明書** フィールドで、インポートしたプロキシ サーバー証明書を選択します。
15. **アプリケーション プール** フィールドでサイトのプールを指定し、その名前をメモします (例: **SdiAppPool**)。

    ![Web サイトを追加します。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Web サイトの作成が完了したら **SSL 設定** のメニューを開きます。

    ![SSL 設定のメニューを開きます。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. **SSL を必須にする** チェックボックスを選択し、**クライアント証明書** フィールド グループで **必須** オプションを選択します。

    ![SSL 設定の構成。](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. **ディレクトリ参照** を開いて **有効化** を選択します。
19. 任意のWebブラウザで **serverDNS/TrasmissioneFatture.svc** に移動します。 サービスに関する標準ページが表示されるはずです。

    ![ブラウザでサービスを確認します。](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. ログとファイルを保存する、次のフォルダを作成します。

    - **C:\\Logs\\** – ここにログ ファイルを保存します。 これらのファイルは [MS サービス追跡ビューアー](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) で表示できます。
    - **C:\\Files\\** – ここに応答ファイルをすべて保存します。

21. ファイル エクスプローラーで、**Logs** と **Files** のフォルダーに、**ネットワーク サービス** と **IIS AppPool\\SdiAppPool** (既定のプールを使用する場合は **IIS AppPool\\DefaultAppPool**) のアクセス許可を付与します。

    1. どちらかのフォルダーを選択したまま (または右クリック) で操作し、**プロパティ** を選択します。
    2. **プロパティ** ダイアログ ボックスの **セキュリティ** タブで、**編集** を選択します。
    3. リストに存在しない場合はユーザーを追加します。
    4. 別のフォルダについても手順 1 〜 3 を繰り返します。

    ![サービス ユーザーにアクセス許可を追加します。](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>プライバシー通知 

**イタリアの電子請求** 機能を有効化する場合は、制限付きのデータ送信が必要な場合があります。 このデータは組織の税登録 ID を含みます。 管理者は、イタリアの電子請求機能の有効化/無効化を設定できます。 この機能を無効化する場合は、次の手順を実行します。

1. **組織管理** \> **設定** \> **電子ドキュメント パラメーター** に移動します。
2. **機能** タブで **イタリアの電子請求** 機能を含む行を選択してから、**今すぐ無効化する** を選択します。

これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、国/地域に固有の機能ドキュメントが含む "プライバシーに関する注意事項" セクションを参照してください。

## <a name="additional-resources"></a>追加リソース

- [電子請求の概要](e-invoicing-service-overview.md)
- [電子請求サービスの管理を開始する](e-invoicing-get-started-service-administration.md)
- [電子請求の使用を開始する](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
