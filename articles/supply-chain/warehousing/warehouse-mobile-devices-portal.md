---
title: Finance and Operations の倉庫モバイル デバイス ポータル (WMDP)
description: この記事では、Microsoft Dynamics 365 for Finance and Operations の倉庫モバイル デバイスを有効にする方法について説明します。 また、環境を稼働させてアップグレードする方法についても説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30171
ms.assetid: acdddf48-d385-4f86-8633-013ff2d6eecd
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e71309c30a4046e8da3eb713cdd4a7d95240f75d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "857212"
---
# <a name="warehouse-mobile-devices-portal-wmdp-for-finance-and-operations"></a>Finance and Operations の倉庫モバイル デバイス ポータル (WMDP)

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この機能は非推奨になりました。 詳細については、[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md#warehouse-mobile-devices-portal) を参照してください。


この記事では、Microsoft Dynamics 365 for Finance and Operations の倉庫モバイル デバイスを有効にする方法について説明します。 また、環境を稼働させてアップグレードする方法についても説明します。

倉庫モバイル デバイス ポータル (WMDP) は、IIS でホストされる Web アプリケーションです。 ASP.NET MVC ランタイムを使用します。 Microsoft Dynamics 365 for Finance and Operations の最新のバージョンでは、WMDP は、自己展開オンプレミス専用のスタンドアロン コンポーネントとして提供されています。 環境で WMDP を有効にするために、インストーラーをダウンロードし、WMDP アプリケーションを配置して、Finance and Operations サーバーに接続するように構成する必要があります。 この記事では、環境に WMDP を有効にする方法について説明します。 また、修正プログラムをお客様の環境に導入するプロセスについても説明します。

## <a name="download-the-installer-for-warehouse-mobile-devices-portal"></a>Warehouse Mobile Devices Portal のインストーラーをダウンロード
WMDP は、スタンドアロンの Microsoft インストール パッケージによってインストールされます。 インストーラー ファイル、WarehouseMobileDevicesPortal.msi は、Finance and Operations から直接ダウンロードできます。 インストーラーを入手するためには、倉庫管理モジュールが有効になっている必要があります。 WMDP インストーラーをダウンロードするには、これらの手順に従います。

1.  Dynamics 365 for Finance and Operations に情報技術マネージャのロールを持つユーザーとしてログインします。
2.  **倉庫管理** &gt; **設定** &gt; **モバイル デバイス** &gt; **倉庫モバイル デバイス ポータルのダウンロード**の順に移動します。[![op-wmdp-01](./media/op-wmdp-01.png)](./media/op-wmdp-01.png)
3.  Security Best Practices チェックリストを確認します。 レビューする各品目の **完了** チェック ボックスをオンにします。
4.  法的情報セクションで、ソフトウェアのライセンス条項を読みます。
5.  **OK** をクリックします。 次に、WarehouseMobileDevicesPortal.msi は、次のスクリーン ショットのようにダウンロードします。 [![WarehouseMobileDevicesPortal.msi ダウンロード ダイアログ](./media/02.png)](./media/02.png)

## <a name="install-the-warehouse-mobile-devices-portal"></a>倉庫モバイル デバイス ポータルのインストール
倉庫モバイル デバイス ポータル インストーラーは、同じ Windows サーバー マシンへの最大 100 インスタンスのインストールをサポートします。 WMDP インスタンスのインスタンスをインストールするには、これらの手順に従います。

1.  既定のインスタンスをインストールするには、WarehouseMobileDevicesPortal.msi を実行します。 - または - 既定以外のインスタンスをインストールするには、次のコマンドを実行します。

        msiexec /I WarehouseMobileDevicesPortal.msi TRANSFORMS=:<InstanceID> MSINEWINSTANCE=1

    ここで **InstanceID** は名前付きインスタンス ID です。 展開するインスタンスの名前を識別するには、**インスタンス\_01** から**インスタンス\_99** までの値を使用します。 [![wmdp-wizard-01](./media/wmdp-wizard-01.png)](./media/wmdp-wizard-01.png)

2.  **次へ** をクリックします。
3.  インストール場所を選択するか、既定のインストール場所 (推奨) のままにします。
4.  **次へ** をクリックします。
5.  **IIS コンフィギュレーション**ページの、**Web サイト ポート**フィールドで、Web サイトが利用可能となる TCP ポートを入力します。 たとえば、8999 と入力します。
6.  **次へ** をクリックします。
7.  セットアップ ウィザードはインストールを完了する準備ができました。 

    [![wmdp-wizard-02](./media/wmdp-wizard-02.png)](./media/wmdp-wizard-02.png)

8.  **インストール** をクリックします。
9.  インストールが完了したら、**完了** をクリックします。

## <a name="retrieve-and-install-a-certificate-on-your-warehouse-mobile-device-portal-host-machine"></a>Warehouse モバイル デバイス ポータル のホスト・マシンで証明書を検索してインストールする
倉庫モバイル デバイス ポータルは、https を使用して実行するように配置されます。 インストーラーは、選択したポートに https バインディングを作成しますが、SSL/TLS 証明書はそのポートに関連付けません。 初期コンフィギュレーション プロセスを完了するためには、証明書をバインディングに関連付ける必要があります。

-   よく知られた証明機関によって配布された商用証明書を展開します。 信頼できるプロバイダーを使用することにより、証明書は既定で倉庫内のクライアントのブラウザによって信頼されます。 これは、商用展開に推奨される選択肢です。
-   または、自己署名証明書を作成することもできます。 これは、開発環境とステージング環境にとって便利な方法です。 自己署名サーバー証明書を作成するには、このチュートリアルに従います: <https://technet.microsoft.com/en-us/library/cc753127(v=ws.10).aspx>

Warehouse モバイル デバイス ポータル のホスト・マシンで証明書を検索してインストールするには、次のようにします。

1.  IIS で、次のスクリーンショット [![iis-wmdp-01](./media/iis-wmdp-01-1024x540.png)](./media/iis-wmdp-01.png) に示すように、倉庫モバイル デバイス ポータル サイトのバインディングを開きます。
2.  バインディングを選択します。 [![サイト バインディングの選択](./media/06.png)](./media/06.png)
3.  **編集**をクリックして、倉庫モバイル デバイス ポータル用に使用するホスト名を関連付けます。 詳細については、「<https://technet.microsoft.com/en-us/library/cc771629.aspx>」を参照してください。
4.  次のスクリーン ショットは、ポート 8999 の https バインディングに関連付けられた localhostWMDP\_DEFAULT いう名前の自己署名証明書の例を示しています。 [![編集サイト バインディング](./media/07.png)](./media/07.png)

## <a name="configure-the-warehouse-mobile-devices-portal-web-application"></a>倉庫モバイル デバイス ポータル Web アプリケーションのコンフィギュレーション
Warehouse モバイル デバイス ポータル アプリケーションを特定の Finance and Operations サーバーと相互作用させるには、インストール後に以下の構成手順を完了する必要があります。

1.  Azure Active Directory で Operations テナント用のネイティブ アプリケーションを登録します。 このアプリケーションは、Microsoft Dynamics ERP へのアクセスが必要です。
    1.  Finance and Operations カスタム サービス認証については、[Dynamics 365 for Finance and Operations Services の技術的な概念に関するガイド](../../dev-itpro/data-entities/services-home-page.md) をご覧ください。
    2.  「AAD でネイティブ アプリケーションを登録」するための手順に従います。
    3.  これでアプリケーション **クライアント ID** を取得しました。

2.  Azure Active Directory で Operations テナント用の新しいユーザー アカウントを作成します。 このユーザー アカウントの目的は、Operations サーバーが公開する、WMDP 特有の顧客サービスにアクセスすることです。 この手順を完了した後、**WMDP 電子メール アドレス**と **WMDP パスワード**から構成される、**WMDP ユーザー資格情報**が作成されます。 Azure AD および Finance and Operations にユーザーを追加する基本的な方法については、次のチュートリアルを参照してください: [Finance and Operations サブスクリプションへのサインアップ]((../../dev-itpro/sign-up-preview-subscription.md)。
3.  **WMDP ユーザー資格情報**に対応するオペレーション ユーザーを作成します。
    1.  Finance and Operations で、**システム管理** &gt; **共通** &gt; **ユーザー** に移動します。
    2.  新規ユーザーを作成します。
    3.  例のスクリーンショットに示されているように、倉庫モバイル デバイス ユーザーを割り当てます。 [![WMDP の新規ユーザーの作成](./media/08.png)](./media/08.png)

4.  倉庫モバイル デバイス ポータルの web.config ファイルを更新します。
    1.  Internet Information Services (IIS) マネージャーで、Web サイトを検索します。
    2.  **アクション**ペインで、WMDP Web サイトのソースを参照するために**エクスプローラー**を選択します。
    3.  Web.config ファイルを編集し、**ServiceConnection** 要素を検索します。
    4.  **ServiceReference** 要素の URI 属性に値を割り当てます。

             <your root Operations URL>/api/services.

        例:

             URI="https://dynamics1622aos.cloud.dynamics.com/api/services/

    5.  **認証**要素の次の属性に値を割り当てます。

            ServiceSecurityResource = <your lower-cased root Operations URL>
            ServiceClientID = <Client ID> (obtained in step 1 of this section)
            ServiceUserName = <WMDP email address> (obtained in step 2 of this section)
            ServiceUserPassword = <WMDP password> (obtained in step 2 of this section)
            ServiceAuthenticationURL = <authentication URL to your tenant>

        例:

            ServiceSecurityResource = https://usncax1aos.cloud.onebox.dynamics.com
            ServiceClientID = "aaaaaaaa-1234-bbbb-5678-ccccccccccc"
            ServiceUserName = WMDPapp@contoso.net
            ServiceUserPassword = "wmdpP@ss"
            ServiceAuthenticationURL = "https://login.windows.net/contoso.net"

5.  Web.config ファイルには専用の強力な ACL が適用されますが、セキュリティ上の理由から、Live に入る前に Web.config ファイルから資格情報を削除する必要があります。 この手順では、Windows 資格情報マネージャーに保存して、前の手順で作成された資格情報を保護します。

    1.  倉庫モバイル デバイス ポータルのメイン ページを開きます。
    2.  **Web アプリケーション コンフィギュレーションの読み込み**をクリックします。 [![wmdp-load-config-01](./media/wmdp-load-config-01.png)](./media/wmdp-load-config-01.png)
    3.  資格情報の記録に成功すると、次のメッセージが表示されます。 [![Web コンフィギュレーションの読み込み成功](./media/10.png)](./media/10.png)
    4.  Web.config ファイルで、空の文字列に ServiceUserName および ServiceUserPassword を設定します。

    <!-- -->

        ServiceUserName = "" 
        ServiceUserPassword = ""

6.  ブラウザーに戻り **Web アプリケーション コンフィギュレーションの読み込み**を再度クリックします。 次のメッセージが表示されます。 [![Web コンフィギュレーションの読み込み: 変更なし](./media/11.png)](./media/11.png)
7.  倉庫モバイル デバイス ポータル ページにログオンできるようになりました。 コンフィギュレーションが成功した場合、会社の選択ページが表示されます。 [![会社の選択ページ](./media/12.png)](./media/12.png)

**会社を選択** 画面が表示される場合で、Finance and Operations に接続されます。 それ以外の場合、「トラブルシューティング」を参照してください。 WMDP メニューを使用するには、残りの設定手順を完了する必要があります。Dynamics AX 2012 の <https://technet.microsoft.com/en-us/library/dn553159.aspx> を参照してください。

## <a name="servicing-the-warehouse-mobile-devices-portal"></a>倉庫モバイル デバイス ポータルの保守
倉庫モバイル デバイス ポータルがスタンドアロン コンポーネントとしてリリースされた後、利用可能な修正プログラムを手動で適用する必要があります。 修正プログラムがある場合は、WMDP の新しいインスタンスが古いインスタンスと並んで配置されます。 正しくコンフィギュレーションされテストされた後に、管理者は、古いバージョンを破棄し、新しい更新されたバージョンをライブ バージョンにすることができます。 このホット スワップ サービス モデルは、更新された環境の構成とテストによって引き起こされるダウンタイムの最小化を可能にします。 修正プログラムを適用するには。

1.  倉庫モバイル デバイス ポータルへの新しい更新が LCS ポータルで利用可能になった後、ローカル環境にダウンロードできます。 修正プログラムを取得するにはこのテュートリアルに従います: [Lifecycle Services からの修正プログラムのダウンロード](../../dev-itpro/migration-upgrade/download-hotfix-lcs.md)
2.  この修正プログラム パッケージは zip ファイルとして利用できます。 それを展開すると、SCMSelfService\\Packages の WarehouseMobileDevicesPortal.msi のパッチ バージョンを検索する必要があります。
3.  元のインスタンスとは違う TCP ポートの下で、サーバー コンピューターに WMDP の別のインスタンスをインストールするには、このドキュメントの「倉庫モバイル デバイス ポータルをインストール」セクションに従います。 このインスタンスを**修正プログラム適用済み WMDP** とし、元のインスタンスを**古い WMDP インスタンス**と呼びましょう。 適正なセキュリティ対策として、まだ構成中であるため、ファイアウォールを介して生産ネットワークに公開されていない TCP ポートの使用を検討する必要があります。
4.  **パッチ適用された WMDP** をコンフィギュレーションするため、「倉庫モバイル デバイス ポータル Web アプリケーションのコンフィギュレーション」セクションに従います。
5.  カスタマイズを適用し、**パッチ済み WMDP** が確実に使用準備ができているテストを実行します。
6.  **パッチ済み WMDP** のサイト バインドを更新し、**古い WMDP インスタンス**を廃止します。
    1.  IIS で、**古い WMDP インスタンス**を停止します。 これにより、作業ユーザー セッションは終了しますが、作業セッション状態が Finance and Operations に保存されるため、進行中の作業を破損しません。
    2.  Internet Information Services (IIS) マネージャーで、次のスクリーンショットに示すように**古い WMDP インスタンス**のバインディングを開きます。 [![iis-wmdp-02](./media/iis-wmdp-02-1024x192.png)](./media/iis-wmdp-02.png)
    3.  既定のバインドを削除し、**サイト バインディング** ウィンドウを閉じます。
    4.  インターネット インフォメーション サービス (IIS) マネージャーで **パッチ適用された WMDP インスタンス** サイトを選択して、**バインディング**を開き、**古い WMDP インスタンス** から削除されたバインディングとまったく同じポートで新しい HTTP バインディングを作成します。

7.  ここで、**修正プログラム適用済み WMDP インスタンス** を活性化する必要があります。
8.  **古い WMDP インスタンス** をアンインストールできるようになりました。
    1.  コンピューターで、**プログラム ウィンドウのアンインストールまたは変更** (**コントロール パネル**l &gt; **プログラム** &gt; **プログラムと機能**) を開くか、appwiz.cpl を管理者として開きます。
    2.  **古い WMDP インスタンス**をインストールされているプログラムの一覧で検索します。 次のスクリーン ショットは、リストの DEFAULT インスタンスを示しています。 [![wmdp-control-panel-01](./media/wmdp-control-panel-01-1024x190.png)](./media/wmdp-control-panel-01.png)
    3.  UI またはコマンド ラインを使用して、**古い WMDP インスタンス**をアンインストールします。

## <a name="troubleshooting"></a>トラブルシューティング
**問題:** この一般的なエラーが表示されます: 要求の処理中にエラーが発生しました。 要求を再試行するか、またはシステム管理者に問い合わせてください。 **ソリューション:** イベント ビューアーを開き、アプリケーション ログに移動すると、次の例に示すように、例外の詳細を含む ASP.NET が提供するログが見つかります。 [![イベント ビューアー アプリケーション ログへの ASP.NET ログイン](./media/151.png)](./media/151.png)イベント ビューアーのエラーに関する追加情報は、このブログを参照してください: [Microsoft Dynamics AX の倉庫モバイル デバイス ポータル](http://community.dynamics.com/ax/b/dynamicsaxseven/archive/2016/03/17/warehouse-mobile-devices-portal-for-microsoft-dynamics-ax)。



