---
title: 新しい Azure AD B2C 情報でコマース本社を更新する
description: この記事では、Microsoft Dynamics 365 Commerce headquarters を新しい Azure Active Directory (Azure AD) 企業間 (B2C) 情報で更新する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785322"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>新しい Azure AD B2C 情報でコマース本社を更新する

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce headquarters を新しい Azure Active Directory (Azure AD) 企業間 (B2C) 情報で更新する方法について説明します。

上記の Azure AD B2C プロビジョニングの手順が完了したら、Azure AD B2C アプリケーションをDynamics 365 Commerce 環境に登録する必要があります。

新しい Azure AD B2C 情報を使用して本社を更新するには、次の手順を実行します。

1. コマースで、**コマース共有パラメーター** を開いて、左側のメニューで **ID プロバイダー** を選択します。
1. **ID プロバイダー** で、次の操作を行います。
    1. **発行者** ボックスに、ID プロバイダー発行者文字列を入力します。 発行者文字列を検索するには、[本社の設定の発行者文字列の取得](#obtain-issuer-string-for-headquarters-setup) を参照してください。
    1. **名前** ボックスに、発行者レコードの名前を入力します。
    1. **タイプ** ボックスに、**Azure AD B2C (id_token)** と入力します。
1. **依存する関係者** で、上記の B2C ID プロバイダー品目を選択した状態で、次の操作を行います。
    1. **ClientID** ボックスに、B2C アプリケーション ID を入力します。これは、B2C アプリケーションのプロパティ ページの **アプリケーション ID** ボックスに表示されます。
    1. **タイプ** ボックスに **公的** と入力します。
    1. **ユーザー タイプ** ボックスに **顧客** と入力します。
1. アクション ウィンドウで、**保存** を選択します。
1. コマース検索ボックスで、**配送スケジュール** を検索する
1. **配送スケジュール** ページの左のナビゲーション メニューで、ジョブ **1110 グローバル コンフィギュレーション** を選択します。
1. アクション ウィンドウで、**今すぐ実行** を選択します。

### <a name="obtain-issuer-string-for-headquarters-setup"></a>本社の設定の発行者文字列を取得する

ID プロバイダー発行者文字列を取得するには、次の手順を実行します。

1. Azure portal の Azure AD B2C ページで、**新規登録とログイン** ユーザー フローに移動します。
1. 左ナビゲーション メニューの **ページ レイアウト** を選択し、**レイアウト名** で **統合された新規登録またはログイン ページ** を選択し、**ユーザー フローの実行** を 選択します 。
1. アプリケーションが上で作成された目的の Azure AD B2C アプリケーションに設定されていないことを確認し、``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` を含む **ユーザー フローの実行** ヘッダーの下に表示されるユーザー フロー リンクを選択します 。 (**ユーザー フローの実行** は選択しないでください。) 新しいタブが開き、発行者文字列を収集するポリシーのメタデータが表示されます。
1. ブラウザのタブに表示されているメタデータ ページで、次の例に似た ID プロバイダー発行者文字列 (**発行者** が "https://" で始まり "/v2.0/" で終わる値) をコピーします。
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。
 
**OR**: 同じメタデータ URL を手動で作成するには、次の手順を実行します。

1. B2C テナントとポリシーを使用して、次の形式でメタデータ アドレスの URL を作成します。``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - 例: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``。
1. メタデータ アドレス URL をブラウザーのアドレス バーに入力します。
1. メタデータで、ID プロバイダー発行者 URL (**発行者** の値) をコピーします。
    - 例: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``。

## <a name="next-steps"></a>次のステップ

Commerceで B2C テナントを設定するプロセスを続行するには、[Commerce サイト ビルダーで B2C テナントを構成する](config-b2c-tenant-site-builder.md)手順に進みます。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
