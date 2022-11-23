---
title: ソーシャル ID プロバイダーの追加
description: この記事では、Microsoft Azure ポータルにソーシャル ID プロバイダーを追加する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785283"
---
# <a name="add-social-identity-providers"></a>ソーシャル ID プロバイダーの追加

[!include [banner](includes/banner.md)]

この記事では、Microsoft Azure ポータルにソーシャル ID プロバイダーを追加する方法について説明します。

ソーシャル ID プロバイダーを使用すると、ユーザーは自分のソーシャル アカウントを使用して認証を行うことができます。 ソーシャル ID プロバイダー認証の追加は Dynamics 365 Commerce で行うことができます。 

ソーシャル ID プロバイダー認証が追加されていない場合、既定の Azure Active Directory (Azure AD) B2C プロファイルがユーザー ベースの主要プロファイルになります。 ユーザーは自分のユーザー名 (お好みの電子メール アドレス) を選択し、パスワードを設定します。 Azure AD B2C はユーザーを直接認証します。 

ソーシャル ID プロバイダー認証が追加され、ユーザーがそのいずれかのソーシャル ID プロバイダーを選択した場合でも、Azure AD B2C テナントにはエンティティが作成されます。 Azure AD B2C は、ソーシャル ID プロバイダーを使用してユーザーの資格情報を認証します。

> [!NOTE]
> ID プロバイダーの登録は B2C テナントにレコードを作成しますが、認証のために外部のソーシャル ID プロバイダーの参照を呼び出すため、ローカル アカウントとは異なる形式です。 ユーザーは、ソーシャル ID プロバイダー間で同じ電子メール アドレスを使用できます。つまり、認証に使用される電子メール ユーザー名はテナントに対して固有ではない可能性があります。 Azure AD B2C は、ユーザーがローカル B2C アカウントで固有の電子メール アドレスを持つ場合にのみ適用されます。

認証用のソーシャル ID プロバイダーを追加する前に、ID プロバイダーのポータルにアクセスして、Azure AD B2C ドキュメントの指示に従って ID プロバイダーアプリケーションを設定する必要があります。 ドキュメントへのリンクの一覧は、次のとおりです。

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (単一テナント)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft アカウント](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>ソーシャル ID プロバイダーの追加と設定

> [!NOTE]
> ソーシャル ID プロバイダーの追加は、Microsoft Dynamics 365 Commerce で企業と顧客間 (B2C) テナントを設定する際のオプションの手順です。

ソーシャル ID プロバイダーを追加および設定するには、次の手順を実行します。  

1. Azure ポータルで、**ID プロバイダー** に移動します。
1. **追加** を選択します。 **ID プロバイダーの追加** 画面が表示されます。
1. **名前** に、サインイン画面でユーザーに表示される名前を入力します。
1. **ID プロバイダー タイプ** で、リストから ID プロバイダーを選択します。
1. **OK** を選択します。
1. **この ID プロバイダーの設定** を選択して **ソーシャル ID プロバイダー** 画面にアクセスします。
1. **クライアント ID** で、ID プロバイダー アプリケーションの設定から取得したクライアント ID を入力します。
1. **クライアント シークレット** で、ID プロバイダー アプリケーションの設定から取得したクライアント シークレットを入力します。
1. サインイン/登録ポリシーのユーザー フローを添付します。
1. **Azure AD B2C – ユーザー フロー (ポリシー) \>{サインイン登録ポリシー} \> ID プロバイダー**。
1. サインイン/登録のユーザー フロー ポリシーを添付するには、アカウントに対して設定した各 ID プロバイダーを選択します。 フローをテストするには、各 ID プロバイダーに対して **ユーザー フローを実行** を選択します。 新しいタブには、新しい ID プロバイダーの選択ボックスを表示するサインイン ページが表示されます。

次の図は、Azure AD B2C での **ID プロバイダーの追加** および **ソーシャル ID プロバイダーの設定** 画面の例を示しています。

![アプリケーションへのソーシャル ID プロバイダーの追加。](./media/B2CImage_14.png)

次の図は、Azure AD B2C **ID プロバイダー** ページで ID プロバイダーを選択する方法の例を示しています。

![各ソーシャル ID プロバイダーを選択して、ポリシーを有効にする。](./media/B2CImage_16.png)

次の図は、ソーシャル ID プロバイダーのサインイン ボタンが表示された既定のサインイン画面の例を示しています。

> [!NOTE]
> ユーザー フローに対して Commerce に組み込みのカスタム ページを使用する場合は、Commerce モジュール ライブラリの機能拡張機能を使用して、ソーシャル ID プロバイダ用のボタンを追加する必要があります。 また、特定のソーシャル ID プロバイダを使用してアプリケーションを設定する際に、URL や構成文字列で大文字と小文字が区別される場合があります。 詳細については、ソーシャル ID プロバイダの接続手順を参照してください。
 
![ソーシャル ID プロバイダーのサインイン ボタンが表示された既定のログイン画面の例。](./media/B2CImage_17.png)

## <a name="next-steps"></a>次のステップ

Commerce で B2C テナントを設定するプロセスを続行するには、[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md) に進みます。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
