---
title: "Microsoft Dynamics 365 for Operations &#8211; Warehousing をインストールして構成する"
description: "このトピックでは、Microsoft Dynamics 365 for Operations - Warehousing をインストールして構成する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bbf6df8d43889e7a62bfe28921997c45c8b4c632
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Operations &#8211; Warehousing をインストールして構成する

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations - Warehousing をインストールして構成する方法について説明します。

Dynamics 365 for Operations - Warehousing は、Google Play ストアおよび Windows ストアで利用可能なアプリケーションです。 Microsoft Dynamics 365 for Operations の最新のバージョンでは、このアプリケーションはスタンドアロン コンポーネントとして提供されています。つまり、倉庫のタスクに使用されるデバイスに自己展開することを意味します。 Dynamics 365 for Operations 環境でこのアプリを使用するには、各デバイスでアプリをダウンロードし、Dynamics 365 for Operations 環境に接続するように設定する必要があります。 このトピックでは、デバイスにアプリをインストールする方法について説明します。 また、Dynamics 365 for Operations 環境に接続するようにアプリを設定する方法についても説明します。

## <a name="prerequisites"></a>必要条件
このアプリは Android および Windows オペレーティング システムで使用できます。 このアプリを使用するには、デバイスに次のサポートされているオペレーティング システムの 1 つがインストールされている必要があります。 Dynamics 365 for Operations が次のサポートされているバージョンの 1 つである必要があります。 ハードウェアとソフトウェアがインストールをサポートする環境であるかどうかを評価するために役に立つ次の表の情報を使用します。

| プラットフォーム                    | バージョン                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (すべてのバージョン)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations バージョン 1611 または Microsoft Dynamics Dynamics AX バージョン 7.0/7.0.1 および Microsoft Dynamics AX プラットフォーム更新プログラム 2 (KB 3210014) |

## <a name="get-the-app"></a>アプリの取得
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing on the Windows ストア](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing on the Google Play ストア](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Active Directory に Web サービス アプリケーションを作成する
アプリケーションが特定の Dynamics 365 for Operations サーバーと対話できるようにするには、Dynamics 365 for Operations テナント用の Azure Active Directory に Web サービス アプリケーションを登録する必要があります。 セキュリティ上の理由から、使用する各デバイス用の Web サービス アプリケーションを作成するようにお勧めします。 Azure Active Directory (Azure AD) で Web サービス アプリケーションを作成するには、次の手順を実行します:

1.  Web ブラウザーで、<https://manage.windowsazure.com> にアクセスします。
2.  Azure サブスクリプションにアクセス可能なユーザーの名前とパスワードを入力します。
3.  Azure Portal の左のナビゲーション ウィンドウで、[**Active Directory**] をクリックします。[](./media/wh-01-active-directory-example.png)[![wh 01 active directory の例](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  グリッドで、Dynamics 365 for Operations で使用されている Active Directory のインスタンスを選択します。
5.  上部のツールバーで、[**アプリケーション**] をクリックします。 [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  下部ウィンドウで、[**追加**] をクリックします。 [**アプリケーションの追加**] ウィザードが起動します。
7.  アプリケーションの名前を入力して、[**Web アプリケーションおよび/または Web API**] を選択します。 [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  テナントのアプリケーション URL またルート Operations URL のサインオン URL を入力します。 サインオン URL は現状アプリの承認のためにアクティブに使用されていませんが、必須のフィールドです。 [アプリ ID URI] フィールドに、同じ URL を入力します。 [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  [**構成**] タブに移動します。 [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. [**他のアプリケーションへのアクセス許可**] セクションが表示されるまで下へスクロールします。 [**アプリケーションの追加**] をクリックします。 [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. [**Microsoft Dynamics ERP**] を一覧から選択します。 ページの右上隅にある [**完了チェック**] ボタンをクリックします。 [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. [**アクセス許可の委任**] リストで、すべてのチェック ボックスをオンにします。 [**保存**] をクリックします。 [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. 次の情報をメモします:
    -   **クライアント ID** - ページを上へスクロールすると、**クライアント ID**が表示されます。
    -   **キー** - **キー** セクションで、期間を選択してキーを作成し、キーをコピーします。 このキーは、後で**クライアント シークレット**と呼ばれます。

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations でユーザー アカウントを作成および設定する
Dynamics 365 for Operations を Azure AD アプリケーションとして使用可能にするには、次の手順を完了する必要があります。

1.  Azure Active Directory で Dynamics 365 for Operations テナント用の新しいユーザー アカウントを作成します。 このユーザー アカウントの目的は、Dynamics 365 for Operations サーバーが公開する、倉庫保管アプリの特定の顧客サービスにアクセスすることです。 この手順を完了した後、WMDP 電子メール アドレスと WMDP パスワードから構成される、WMDP ユーザー資格情報が作成されます。 Azure AD および Dynamics 365 for Operations にユーザーを追加する基本的な方法については、このチュートリアルを参照してください: [Microsoft Dynamics 365 for Operations サブスクリプションのサインアップ](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription)。
2.  倉庫保管アプリ ユーザー資格情報に関連する Dynamics 365 for Operations ユーザーを作成します。
    1.  Dynamics 365 for Operations で、[**システム管理**] &gt; [**共通**] &gt; [**ユーザー**] に移動します。
    2.  新規ユーザーを作成します。
    3.  次のスクリーンショットに示すとおり、倉庫モバイル デバイス ユーザーを割り当てます。 [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Azure Active Directory アプリケーションを倉庫保管アプリ ユーザーに関連付けます。
    1.  Dynamics 365 for Operations で、[**システム管理**] &gt; [**セットアップ**] &gt; [**Azure Active Directory アプリケーション**] に移動します。
    2.  新しい行を作成します。
    3.  **クライアント ID** (前のセクションで取得したもの) を入力し、名前を設定し、以前に作成したユーザーを選択します。 Dynamics 365 for Operations へのアクセスを紛失した場合に備えて、このページから簡単に削除できるように、すべてのデバイスにタグを付けることをお勧めします。 [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>アプリケーションのコンフィギュレーション
Azure AD アプリケーションを使用して Dynamics 365 for Operations サーバーに接続するには、デバイス上でアプリを設定する必要があります。 それには、次の手順を完了します。

1.  アプリで、[**接続設定**] に移動します。
2.  [**デモ モード**] フィールドをクリアします。 [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  次の情報を入力します: - **Azure Active Directory クライアント ID** - クライアント ID は「Active Directory に Web サービス アプリケーションを作成する」のステップ 13 で取得します。 - **Azure Active Directory クライアント シークレット** - クライアント シークレットは「Active Directory に Web サービス アプリケーションを作成する」のステップ 13 で取得します。 - **Azure Active Directory リソース** - The Azure AD Directory リソースは Dynamics 365 for Operations のルート URL を示します。 **注**: スラッシュ (/) でこのフィールドを終了しないでください。 - **Azure Active Directory テナント** - Dynamics 365 for Operations サーバーで使用される Azure AD Directory のテナント: https://login.windows.net/&lt;your-AD-tenant-ID&gt;。 例: https://login.windows.net/contosooperations.onmicrosoft.com 
**注**: スラッシュ (/) でこのフィールドを終了しないでください。 - **会社** - Dynamics 365 for Operations にアプリケーションが接続する法的エンティティを入力します。 [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  アプリケーションの左上隅にある [**戻る**] ボタンを選択します。 アプリケーションは Dynamics 365 for Operations サーバーに接続し、倉庫ワーカーのログイン画面が表示されます。 [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>デバイスへのアクセスを削除する
デバイスの紛失またはセキュリティが侵害された場合、デバイスの Dynamics 365 for Operations のアクセスを削除する必要があります。 次の手順では、アクセスを削除するための推奨プロセスについて説明します。

1.  Dynamics 365 for Operations で、[**システム管理**] &gt; [**セットアップ**] &gt; [**Azure Active Directory アプリケーション**] に移動します。
2.  アクセスを削除するデバイスに対応する行を削除します。 削除したデバイスに使用されている**クライアント ID**を書き留めます。
3.  Azure クラシック ポータル <https://manage.windowsazure.com> にサインインします。
4.  左側のメニューにある [**Active Directory**] アイコンをクリックし、目的のディレクトリをクリックします。
5.  トップ メニューで [**アプリケーション**] をクリックし、次に設定するアプリケーションをクリックします。 **クイック スタート**ページにシングル サインオンおよび他の設定情報が表示されます。
6.  [**構成**] タブをクリックし、スクローン ダウンして、アプリケーションの**クライアント ID**が、このセクションの手順 2 と同じことを確認します。
7.  コマンド バーの [**削除**] ボタンをクリックします。
8.  確認メッセージで [**はい**] をクリックします。





