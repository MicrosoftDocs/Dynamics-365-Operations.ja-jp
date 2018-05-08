---
title: "Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing のインストールと構成"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations - Warehousing をインストールして構成する方法について説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: ja-jp
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operations &#8211; Warehousing のインストールと構成

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> このトピックでは、クラウド配置の倉庫管理の構成方法について説明します。 オンプレミス配置の倉庫管理の構成方法を検索する場合、[オンプレミス配置の倉庫管理](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md) を参照してください。


このトピックでは、Microsoft Dynamics 365 for Finance and Operations - Warehousing をインストールして構成する方法について説明します。

Finance and Operations - Warehousing は、Google Play ストアおよび Windows ストアで利用可能なアプリケーションです。 Finance and Operations の最新のバージョンでは、このアプリケーションはスタンドアロン コンポーネントとして提供されています。つまり、倉庫のタスクに使用されるデバイスに自己展開することを意味します。 Finance and Operations 環境でこのアプリを使用するには、各デバイスでアプリをダウンロードし、Finance and Operations 環境に接続するように設定する必要があります。 このトピックでは、デバイスにアプリをインストールする方法について説明します。 また、Finance and Operations 環境に接続するようにアプリを設定する方法についても説明します。

## <a name="prerequisites"></a>前提条件
このアプリは Android および Windows オペレーティング システムで使用できます。 このアプリを使用するには、デバイスに次のサポートされているオペレーティング システムの 1 つがインストールされている必要があります。 Finance and Operations が次のサポートされているバージョンの 1 つである必要があります。 ハードウェアとソフトウェアがインストールをサポートする環境であるかどうかを評価するために役に立つ次の表の情報を使用します。

| プラットフォーム                    | バージョン                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4、5.0、6.0、7.0、8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (すべてのバージョン)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations、バージョン 1611 <br>または <br>Microsoft Dynamics AX バージョン 7.0/7.0.1 および Microsoft Dynamics AX プラットフォーム更新プログラム 2 (KB 3210014) |

## <a name="get-the-app"></a>アプリの取得
-   Windows (UWP)
     - [Windows ストアの Finance and Operations - Warehousing](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Google Play ストアの Finance and Operations - Warehousing](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Zebra App Gallery ストアの Finance and Operations - Warehousing](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Azure Active Directory に Web サービス アプリケーションを作成する
アプリケーションが特定の Finance and Operations サーバーと対話できるようにするには、Finance and Operations テナント用の Azure Active Directory に Web サービス アプリケーションを登録する必要があります。 セキュリティ上の理由から、使用する各デバイス用の Web サービス アプリケーションを作成するようにお勧めします。 Azure Active Directory (Azure AD) で Web サービス アプリケーションを作成するには、次の手順を実行します:

1.  Web ブラウザーで、<https://portal.azure.com>に移動します。
2.  Azure サブスクリプションにアクセス可能なユーザーの名前とパスワードを入力します。
3.  Azure Portal の左のナビゲーション ウィンドウで、[**Azure Active Directory**] をクリックします。[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Finance and Operations で使用されている Active Directory のインスタンスであることを確認してください。
5.  ボックスの一覧で、[**アプリの登録**] をクリックします。 [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  上部ウィンドウで、[**新しい申請の登録**] をクリックしてください。 [**アプリケーションの追加**] ウィザードが起動します。
7.  アプリケーションの名前を入力して、[**Web アプリケーション/Web API**] を選択します。 web アプリケーション URL である、サインオン URL を入力します。 この URL は配置 URL と同じですが、oauth が最後に追加されます。 [**作成**] をクリックします。 [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  一覧で新しいアプリを選択します。 [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  後で必要になりますので、**申請 ID** 値を忘れないようにしてください **申請 ID** は後で、**クライアント ID** として参照されます。
10. [**設定ウィンドウ**] 内の [**キー**] をクリックします。 [**パスワード**] セクションでキーの説明および期間を入力してキーを作成します。 
11. [**保存**] をクリックし、 キーをコピーします。 このキーは、後で**クライアント シークレット**と呼ばれます。 [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operations でユーザー アカウントを作成および設定する
Finance and Operations を Azure AD アプリケーションとして使用可能にするには、次の手順を完了する必要があります。

1.  Azure Active Directory で Finance and Operations テナント用の新しいユーザー アカウントを作成します。 このユーザー アカウントの目的は、Finance and Operations サーバーが公開する、倉庫保管アプリの特定の顧客サービスにアクセスすることです。 この手順を完了した後、WMDP 電子メール アドレスと WMDP パスワードから構成される、WMDP ユーザー資格情報が作成されます。 Azure AD および Finance and Operations にユーザーを追加する基本的な方法については、このチュートリアルを参照してください: [Finance and Operations サブスクリプションのサインアップ](../../dev-itpro/dev-tools/sign-up-preview-subscription.md)。
2.  倉庫保管アプリ ユーザー資格情報に関連する Finance and Operations ユーザーを作成します。
    1.  Finance and Operations で、[**システム管理**] &gt; [**共通**] &gt; [**ユーザー**] に移動します。
    2.  新規ユーザーを作成します。
    3.  次のスクリーンショットに示すとおり、倉庫モバイル デバイス ユーザーを割り当てます。 [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Azure Active Directory アプリケーションを倉庫保管アプリ ユーザーに関連付けます。
    1.  Finance and Operations で、[**システム管理**] &gt; [**セットアップ**] &gt; [**Azure Active Directory アプリケーション**] に移動します。
    2.  新しい行を作成します。
    3.  **クライアント ID** (前のセクションで取得したもの) を入力し、名前を設定し、以前に作成したユーザーを選択します。 Finance and Operations へのアクセスを紛失した場合に備えて、このページから簡単に削除できるように、すべてのデバイスにタグを付けることをお勧めします。 [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>アプリケーションのコンフィギュレーション
Azure AD アプリケーションを使用して Finance and Operations サーバーに接続するには、デバイス上でアプリを設定する必要があります。 それには、次の手順を完了します。

1.  アプリで、[**接続設定**] に移動します。
2.  [**デモ モード**] フィールドをクリアします。 <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  次の情報を入力します。 
    + [**Azure Active Directory クライアント ID**] - クライアント ID は「Active Directory に Web サービス アプリケーションを作成する」のステップ 9 で取得します。 
    + [**Azure Active Directory クライアント シークレット**] - クライアント シークレットは「Active Directory に Web サービス アプリケーションを作成する」のステップ 11 で取得します。 
    + [**Azure Active Directory リソース**] - The Azure AD Directory リソースは Finance and Operations のルート URL を示します。 **注**: スラッシュ (/) でこのフィールドを終了しないでください。 
    + [Azure Active directory テナント] - Finance and Operationsサーバーで使用される Azure AD Directory のテナント: `https://login.windows.net/your-AD-tenant-ID`。 例: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**注**: スラッシュ (/) でこのフィールドを終了しないでください。 
    + [**会社**] - Finance and Operations にアプリケーションが接続する法的エンティティを入力します。 <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  アプリケーションの左上隅にある [**戻る**] ボタンを選択します。 アプリケーションは Finance and Operations サーバーに接続し、倉庫ワーカーのログイン画面が表示されます。 <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

モバイル デバイスでカメラを使用してバーコードをスキャンするために Dynamics 365 for Finance and Operations – Warehousing を設定する方法の詳細については、 [Dynamics 365 for Finance and Operations – Warehousing でカメラを使用してバーコードをスキャンします。](scan-bar-codes-using-a-camera.md) を参照してください。

## <a name="remove-access-for-a-device"></a>デバイスへのアクセスを削除する
デバイスの紛失またはセキュリティが侵害された場合、デバイスの Finance and Operations のアクセスを削除する必要があります。 次の手順では、アクセスを削除するための推奨プロセスについて説明します。

1.  Finance and Operations で、[**システム管理**] &gt; [**セットアップ**] &gt; [**Azure Active Directory アプリケーション**] に移動します。
2.  アクセスを削除するデバイスに対応する行を削除します。 後で必要になりますので、削除したデバイスに使用されている**クライアント ID** を忘れないようにしてください。
3.  <https://portal.azure.com>で Azure ポータルにログインします。
4.  左側のメニューにある [**Active Directory**] アイコンをクリックし、適切なディレクトリであることを確認します。
5.  ボックスの一覧で、[**アプリの登録**] をクリックし、構成したいアプリケーションをクリックします。 コンフィギュレーション情報を含む**設定**ページが表示されます。
6.  アプリケーションの**クライアント ID** がこのセクションのステップ 2と同じであることを確認します。
7.  上部ウィンドウの [**削除**] ボタンをクリックします。
8.  確認メッセージで [**はい**] をクリックします。

