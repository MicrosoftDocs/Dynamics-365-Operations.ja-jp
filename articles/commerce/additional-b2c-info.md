---
title: B2C 追加情報
description: この記事では、Microsoft Dynamics 365 Commerce に企業と顧客間 (B2C) テナントを設定する方法の追加情報を提供します。
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785268"
---
# <a name="additional-b2c-information"></a>B2C 追加情報

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce に企業と顧客間 (B2C) テナントを設定する方法の追加情報を提供します。

### <a name="customer-migration"></a>顧客の移行

以前の ID プロバイダー プラットフォームからの顧客レコードの移行を検討している場合は、Dynamics 365 Commerce チームと協力して、顧客移行のニーズを確認してください。

顧客の移行に関する Azure AD B2C 追加ドキュメントについては、[Azure Active Directory B2C へのユーザー移行](/azure/active-directory-b2c/active-directory-b2c-user-migration)を参照してください。

### <a name="custom-policies"></a>カスタム ポリシー

Azure AD B2C の操作および B2C 標準ポリシーで提供されるものを超えるポリシー フローのカスタマイズに関する追加情報については、[Azure Active Directory B2C のカスタム ポリシー](/azure/active-directory-b2c/active-directory-b2c-overview-custom)を参照してください。 

### <a name="secondary-admin"></a>二次管理者

B2C テナントの **ユーザー** セクションには、オプションで二次管理者アカウントを追加することができます。 これは、直接アカウントまたは一般アカウントにすることができます。 チーム リソース間でアカウントを共有する必要がある場合は、共通のアカウントも作成できます。 Azure AD B2C に保管されるデータの機密性のため、共通アカウントは会社のセキュリティ慣行に従って綿密に監視する必要があります。

### <a name="set-up-a-custom-sign-in-domain"></a>カスタム サインイン ドメインの設定

Azure AD B2C では、Azure AD B2C テナントに対してカスタム サインイン ドメインを設定できます。 手順については、[Azure Active Directory B2C のカスタム ドメインを有効にする](/azure/active-directory-b2c/custom-domain) を参照してください。 

カスタム サインイン ドメインを使用する場合は、そのドメインを Commerce サイト ビルダーに入力する必要があります。

サイト ビルダーでカスタム サインイン ドメインを入力するには、次の手順を実行します。

1. サイト ビルダーの右上隅で [サイトの切り替え] を選択し、**サイトの管理** を選択します。
1. 左のナビゲーション ウィンドウで、**テナント設定 \> サイト認証設定** の順に選択します。
1. **サイト認証プロファイル** セクションで、**管理** を選択します。
1. 右側のポップアップ メニューで、カスタム ドメインを入力したいサイト認証プロファイルの横にある **編集** ボタン (鉛筆記号) を選択します。
1. **カスタム ドメインにログイン** にある **サイト認証プロファイルの編集** ダイアログ ボックスで、カスタム サインイン ドメイン ("login.fabrikam.com" など) を入力します。

> [!WARNING]
> Azure AD B2C テナントのカスタム ドメインに更新すると、この変更が、生成されたトークンに対するテナントの発行者の詳細に影響します。 発行者の詳細には、Azure AD B2C が提供する既定のドメインではなく、カスタム ドメインが含まれます。 Commerce headquarters の異なる **発行者** 構成 (**小売とコマース \> Headquarters 設定 \> パラメーター \> Commerce 共有パラメーター \> ID プロバイダー**) は、サイト ユーザーとのシステムのやりとりを変更し、新しい発行者に対してユーザーが認証を実行している場合は、新しい顧客レコードが作成される可能性があります。 Azure AD B2C の実稼働環境でカスタム ドメインに切り替える前に、カスタム ドメインの変更を十分にテストする必要があります。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
