---
title: SharePoint 接続の構成
description: この記事では、接続を構成して、電子請求が Microsoft SharePoint サイトにアクセスできるようにする方法について説明します。
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283990"
---
# <a name="configure-a-sharepoint-connection"></a>SharePoint 接続の構成

[!include [banner](../includes/banner.md)]

電子請求サービスでは、Microsoft SharePoint フォルダーからファイルを読み取り、ファイルを SharePoint にアップロードできます。 電子請求が特定の SharePoint サイトにアクセスできるようするには、電子請求サービスにサイトの資格情報を提供する必要があります。 また、資格情報が安全に保存されるのを確認するために、資格情報を直接提供しないでください。 代わりに、資格情報を Azure キー コンテナーに保存し、Azure Key Vault シークレットを提供します。

## <a name="grant-access-to-a-sharepoint-folder"></a>SharePoint フォルダーへのアクセスを許可する

1. Regulatory Configuration Service (RCS) がインストールされているテナントに、アプリ登録を作成します。

    1. [Azure ポータル](https://portal.azure.com/)にサインインします。
    2. **アプリ登録** に移動します。
    3. **新規登録** を選択します。
    4. **電子請求の SharePoint アプリ** などの名前を入力し、登録を完了します
    5. 新しいアプリ登録を選択します。
    6. **認証** タブで、**パブリック クライアント フローを許可する** オプションを有効にします。
    4. **証明書とシークレット** タブで、**新しいクライアント シークレット** を選択してクライアント シークレットを作成します。
    5. 作成されたシークレットの値をコピーします。

    以下のガイドラインに従います。

    - 異なるサービスに対して同じアプリ登録を使用することはできません。
    - [パスワード ポリシーのレコメンデーション](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide) に従います。
    - パスワードのローテーションを設定します。 ローテーション中に、アプリ登録の新しいクライアント シークレットを作成し、キー コンテナーを更新してから古いシークレットを削除します。

2. **アプリ登録のシークレット** および **アプリケーション (クライアント) ID** 値を、電子請求環境の設定で 2 つの新しいシークレットとしてキー コンテナーに保存します。
3. 作成したシークレットを、RCS の電子請求環境の設定にある Key Vault パラメーターに追加します。
4. Azure portal で、SharePoint へのアクセスを許可します。 この手順は、テナント管理者が実行する必要があります。

    1. 作成したアプリ登録を選択します。
    2. **API アクセス許可** タブで、**アクセス許可の追加** を選択します。
    3. **Microsoft Graph (アプリケーションのアクセス許可)** \> **Sites.Selected** を選択します。
    4. **\<user&nbsp;name\> に対して管理者の同意の付与** を選択します。
    5. **状態** フィールドで、アクセス許可が付与済みであるかを確認します。

        ![[API のアクセス許可] タブで付与されるアクセス許可。](media/configured-permissions.jpg)

    6. [Graph エクスプローラー - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) を開いてサインインします。
    7. 左ウィンドウの **サンプル クエリ** タブで、**SharePoint サイト** から **サイトの相対パスに基づいた SharePoint サイトを取得する** を選択します。
    8. **\{host-name\}** および **\{server-relative-path\}** パラメーターに入力します。 たとえば、**\{host-name\}** には `<domain>.sharepoint.com` を、**\{server-relative-path\}** には `sites/<siteName>` を入力します。

        > [!NOTE]
        > 既定の Web サイトでは、**\{server-relative-path\}** パラメーターを空白のままにします。

    9. **クエリの実行** を選択し、結果を保存します。
    10. 次のクエリを構成します。

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        このクエリでは、**\{site-id\}** は、前のクエリの応答からの **id** ノードの値です。

        これが要求本文です。

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        この要求本文では、**\{app-id\}** は **アプリケーション (クライアント) ID** の値で、**\{app-name\}** は **アプリケーション名** の値です。

        ![POST クエリ。](media/app-id-query.jpg)

    11. **アクセス許可の変更** タブで、**アクセス許可パネルを開く** を選択してから、**サイト** \> **Sites.FullControl.All** \> **同意** を選択します。
    12. **クエリの実行** を選択します。

電子請求サービスが、SharePoint サイトにアクセスできるようになりました。
