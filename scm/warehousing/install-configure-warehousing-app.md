---
title: "工程&#8211のMicrosoft Dynamics 365をインストールしてコンフィギュレーションすること; 倉庫"
description: "このトピックでは、Microsoft Dynamics 365をインストールおよびコンフィギュレーションする方法についてする-倉庫します。"
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>工程&#8211のMicrosoft Dynamics 365をインストールしてコンフィギュレーションすること; 倉庫

このトピックでは、Microsoft Dynamics 365をインストールおよびコンフィギュレーションする方法についてする-倉庫します。

Dynamics 365 for Operations倉庫]- Googleの演劇の店舗とWindowsの店舗で使用できるアプリケーションです。 、Microsoft Dynamics 365 for Operationsの最新のバージョンで、このアプリケーションは、倉庫作業に使用するデバイスの自己配置を意味する、スタンドアロンのコンポーネントとして表示されます。 工程の環境のDynamics 365にアプリケーションを使用するには、各デバイスのアプリケーションをダウンロードし、工程の環境365 for Operationsに接続するように設定する必要があります。 このトピックでは、デバイスにアプリケーションをインストールする方法について説明します。 工程の環境365 for Operationsに接続するアプリケーションを設定する方法を説明します。

## <a name="prerequisites"></a>必要条件
アプリケーションはアンドロイドおよびWindowsオペレーティング システムで使用できます。 このアプリケーションを使用するには、デバイスにインストールされる次のサポートされているオペレーティング システムの一つである必要があります。 また、Dynamics 365 for Operationsの次のサポートされているバージョンの一つである必要があります。 ハードウェアとソフトウェアの環境がインストールをサポートする準備ができたときに、評価する、次の表に従います。

| プラットフォーム                    | バージョン                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 翻訳の特徴をさらに                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)                | Windows 10 (すべてのバージョン)                                                                                                                                                    |
| Dynamics 365 for Operations | 工程バージョン1611では、Microsoft Dynamics 365 -またはMicrosoft Dynamics Dynamics AXのバージョン7.0/7.0.1および修正KB 3210014のプラットフォーム2の更新 |

## <a name="get-the-app"></a>アプリケーションを発生させる
-   Windows UWP () - [Dynamics 365 for Operations [Windowsの店舗] (https://www.microsoft.com/store/apps/9p1bffd5tstm)を倉庫は必須
-   Googleの演劇の店舗] (https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)に翻訳の特徴をさらに- [Dynamics 365 for Operations倉庫]

## <a name="create-a-web-service-application-in-active-directory"></a>Active DirectoryにWebサービス アプリケーションを作成します。
アプリケーションが、サーバーの特定のDynamics 365と連携するようにするには、テナント365 for OperationsのAzureのActive DirectoryのWebサービス アプリケーションを登録する必要があります。 セキュリティ上の理由から、使用する各デバイスのWebサービス アプリケーションを作成することをお勧めします。 AzureのActive Directory (Azureの広告) Webサービス アプリケーションを作成するには、次の手順を実行します:

1.  Webブラウザでは、https://manage.windowsazure.comに<移動します>。
2.  Azureの定期売買にアクセスできるユーザーの名前とパスワードを入力します。
3.  Azureのポータルでは、左側のナビゲーション ウィンドウで、をクリックして** Active Directory **。[] (。/media/wh 01有効なディレクトリexample.png) [![wh 01有効なディレクトリ例] (。/media/wh 01有効なディレクトリExample.png) ] (。/media/wh 01有効なディレクトリexample.png) 
4.  グリッドでは、Dynamics 365 for Operationsで使用されたActive Directoryのインスタンスを選択します。
5.  上のツール バーをクリックして、アプリケーション** **。 [![wh 02有効なアプリケーション ディレクトリ] (。/media/wh 02有効なアプリケーション ディレクトリ1024x197.png) ] (。/media/wh 02有効なディレクトリapplications.png) 
6.  下部ウィンドウで、[**追加します。**。 **アプリケーションを追加します。**ウィザードの開始。
7.  アプリケーションの名前を入力して選択します** WebアプリケーションやWeb API **。 [![wh 03有効なアプリケーション ディレクトリ追加] (。/media/wh 03有効なディレクトリ追加するapplication.png) ] (。/media/wh 03有効なディレクトリ追加するapplication.png) 
8.  テナント アプリケーションのURLになる承認してURLの分割、工順工程URL入力します。 承認して分割URLは、アプリケーションの認証で現在実行中は使用されませんが、必須フィールドです。 アプリケーションID URIフィールドで同じURLを入力します。 [![のwh 04広告追加プロパティ] (。/media/wh 04広告追加するproperties.png) ] (。/media/wh 04広告追加するproperties.png) 
9.  **コンフィギュレーションします。**タブに移動します。 [![のwh 05広告設定アプリケーション] (。/media/wh 05広告コンフィギュレーションするapp.png) ] (。/media/wh 05広告コンフィギュレーションするapp.png) 
10. **他のアプリケーションへのアクセス許可をスクロール**セクションを表示します。 [**アプリケーションを追加します。**。 [![wh 06広告、追加のアクセス許可] (。/media/wh 06広告アプリケーション追加するpermissions.png) ] (。/media/wh 06広告アプリケーション追加するpermissions.png) 
11. **リストでは** Microsoft Dynamics ERP選択します。 **チェックを実行します。**ボタンをクリックして、ページの右角をクリックします。 [![wh 07広告[アクセス許可] (。/media/wh 07広告[permissions.png) ] (。/media/wh 07広告[permissions.png) 
12. では**委任のアクセス許可**すべてのチェック ボックスの一覧を選択します。 Click **Save**. [![wh 08広告委任アクセス許可] (。/media/wh 08広告委任Permissions.png) ] (。/media/wh 08広告委任permissions.png) 
13. 次の情報をメモします:
    -   **クライアントID - **ページの上部にスクロールするため、**クライアントID **表示されて表示されます。
    -   **キーは** - **キー**セクションで、[期間を選択して、キーおよびキーをコピーします。 このキーは、後で呼ばれます**クライアントのシークレット**。

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Dynamics 365 for Operationsのユーザー アカウントを作成して設定します。
Dynamics 365 for OperationsをAzureの広告のアプリケーションを使用できるようにするには、次の手順を実行する必要があります:

1.  工程テナント365 for OperationsのAzureのActive Directoryに新しいユーザー アカウントを作成します。 このユーザー アカウントの目的は、サーバー365 for Operationsを公開する倉庫のアプリケーションの特定のカスタム サービスにアクセスすることです。 この手順を実行すると、WMDPの電子メール アドレスとパスワードWMDPで構成されるWMDPのユーザーの資格情報があります。 Azureの広告にユーザー、Dynamics 365 for Operationsを追加するための基本的な手順についてついては、このチュートリアルを参照してください: [アクションの定期売買の登録します] (/dynamics365/operations/dev itpro/signは定期売買) は、Microsoft Dynamics 365に。
2.  倉庫のアプリケーションのユーザーの資格情報に対応する工程のユーザー365 for Operationsを作成します。
    1.  Dynamics 365 for Operationsで、共通の管理は**システム** &gt; ** **実行 &gt; **ユーザー**。
    2.  新しいユーザーを作成します。
    3.  次のスクリーン ショットに示すように、倉庫のモバイル デバイスのユーザーを割り当てます。 [![のwh 09追加ユーザー セキュリティ ロール] (。/media/wh 09追加ユーザー セキュリティrole.png) ] (。/media/wh 09追加ユーザー セキュリティrole.png) 

3.  倉庫のアプリケーションのユーザーがActive Directory Azureのアプリケーションを関連付けます。
    1.  Dynamics 365 for Operationsで、管理設定は**システム** &gt; ** **実行 &gt; ** Active Directory Azureのアプリケーション**。
    2.  新しい行を作成します。
    3.  入力します。**クライアント** ID (最新のセクションに派生し)、名前が表示され、以前に作成したユーザーを選択します。 Microsoftでは失われますこのページから簡単に365 for Operationsへのアクセス許可を削除できるようにデバイスにすべて付けることをお勧めします。 [![wh 10広告アプリケーション (フォーム)。/media/wh 10広告アプリケーションForm.png) ] (。/media/wh 10広告アプリケーションform.png) 

## <a name="configure-the-application"></a>アプリケーションを設定します。
Azureの広告のアプリケーションによって、サーバー365 for Operationsに接続するデバイスのアプリケーションを設定する必要があります。 これを行うには、次の手順を実行します。

1.  アプリケーションでは、移動する**接続設定**。
2.  **デモ モード**このフィールドをクリアします。 [![のwh 11アプリケーション接続設定デモ モード] (。/media/wh 11アプリケーション接続設定デモ モード169x300.png) ] (。/media/wh 11アプリケーション接続設定デモmode.png) 
3.  次の情報を入力します: - ** Azureの有効なクライアントのディレクトリID - **クライアントIDがActive Directoryに手順13で、で「作成するWebアプリケーション サービスを参照。 - ** Azureの有効なディレクトリのクライアント シークレットがActive Directoryに手順13で- **クライアントで作成しますシークレットの「Webサービス アプリケーションは」取得されます。 - ** Azureの有効なディレクトリのリソースをAzure - **の広告のリソース工程のルート ディレクトリのURL 365 for Operationsを使用します。 **注記: ** フォワード スラッシュの文字を含むこのフィールドを選択しないでください (/)。 - ** Azureの有効なディレクトリ テナント**工程サーバーに365 for Operationsで使用するAzureの広告のディレクトリ テナント: https://login.windows.net/your-AD-tenant-ID&lt;&gt;です。 例: https://login.windows.net/contosooperations.onmicrosoft.comです。 
**注記: ** フォワード スラッシュの文字を含むこのフィールドを選択しないでください (/)。 - **会社** "をアプリケーションに接続するDynamics 365 for Operationsの法人を入力します。 [![のwh 12アプリケーション接続設定] (。/media/wh 12アプリケーション接続設定169x300.png) ] (。/media/wh 12アプリケーション接続settings.png) 
4.  ** **戻るボタンをクリックしてアプリケーションの左上隅に選択します。 アプリケーションでは、サーバー365 for Operationsに、接続、および倉庫作業員のログイン画面が表示されます。 [![wh 13ログ[] (。/media/wh 13が画面180x300.png) ] (。/media/wh 13ログscreen.png) 

## <a name="remove-access-for-a-device"></a>デバイスのアクセスを削除します。
失注または関するされているデバイスの場合、デバイスの365 for Operationsへのアクセスを必要があります。 次の手順は、アクセス許可を削除するに推奨されるプロセスについて説明します。

1.  Dynamics 365 for Operationsで、管理設定は**システム** &gt; ** **実行 &gt; ** Active Directory Azureのアプリケーション**。
2.  [アクセスを削除するデバイスに対応する明細行を削除します。 削除されたデバイスに使用する]のメモ**クライアント** ID。
3.  https://manage.windowsazure.comをAzureの標準的なポータルに<署名します>。
4.  ** Active Directory **アイコンが左メニューをクリックし、必要なディレクトリをクリックします。
5.  トップ]メニューで、[**アプリケーション**、その後、コンフィギュレーションするアプリケーションをクリックします。 **クイック開始**ページで単一の承認して分割、およびそのほかのコンフィギュレーション情報が表示されます。
6.  **コンフィギュレーションします。**タブをクリックし、スクロール、およびクライアントID **このセクションの手順2と同じが**アプリケーションの日付であることを確認します。
7.  **削除**バー コマンド ボタンをクリックします。
8.  ** [はい**確認メッセージの表示します。



