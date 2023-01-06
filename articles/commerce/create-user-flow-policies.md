---
title: ユーザー フロー ポリシーの作成
description: この記事では、Microsoft Azure ポータルでユーザー フロー ポリシーを作成する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785304"
---
# <a name="create-user-flow-policies"></a>ユーザー フロー ポリシーの作成

[!include [banner](includes/banner.md)]

この記事では、Microsoft Azure ポータルでユーザー フロー ポリシーを作成する方法について説明します。

ユーザー フローは、Azure Active Directory (Azure AD) 企業と顧客間 (B2C) が保護されたサインイン、登録、プロファイルの編集、およびパスワードを忘れた際のユーザー エクスペリエンスを提供するために使用するポリシーです。 Dynamics 365 Commerce では、これらのフローを使用して、Azure AD B2C テナントと対話するポリシー アクションを実行します。 ユーザーは、これらのポリシーを操作するときに、Azure AD B2C テナントにリダイレクトされてアクションを実行します。

Azure AD B2Cでは、次の 3 つの基本的なユーザー フロー タイプを使用できます。
- 登録とサインイン
- プロファイルの編集
- パスワードのリセット

Azure AD が提供する既定のユーザー フローを使用するように選択できます。これにより、Azure AD B2C でホストされるページが表示されます。 また、HTML ページを作成して、これらのユーザー フローのエクスペリエンスの外観をコントロールすることもできます。 

Dynamics 365 Commerce に組み込まれたページでユーザー ポリシー ページをカスタマイズするには、[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md) を参照してください。 詳細については、[Azure Active Directory B2C のユーザーエクスペリエンスのインターフェイスをカスタマイズする](/azure/active-directory-b2c/tutorial-customize-ui) を参照してください。

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>登録を作成し、ユーザー フロー ポリシーにサインインする

登録を作成し、ユーザー フロー ポリシーにサインインするには、次の手順を実行します。

1. Azure ポータルで、左のナビゲーション ウィンドウの **ユーザー フロー (ポリシー)** を選択します。
1. **Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー** を選択します。
1. **サインアップとサインイン** ポリシーを選択して、**推奨** バージョンを選択します。
1. **名前** に、ポリシー名を入力します。 この名前は、後でポータルによって割り当てられる接頭語 (「B2C_1_」など) で表示されます。
1. **ID プロバイダー** の **ローカル アカウント** セクションで、**電子メールの登録** を選択します。 電子メール認証は、Commerce の最も一般的なシナリオで使用されます。 ソーシャル ID プロバイダー認証も使用している場合、この時点で選択することもできます。
1. **マルチファクター認証** で、会社に適した選択肢を選択します。 
1. **ユーザー属性およびクレーム** で、必要に応じて属性を収集したり、クレームを返したりするためのオプションを選択します。 **詳細を表示する...** を選択すると、属性と要求のオプションの全一覧が表示されます。 コマースでは、次の既定のオプションを選択する必要があります。

    | **属性の収集** | **返品クレーム** |
    | ---------------------- | ----------------- |
    | 電子メール アドレス          | 電子メール アドレス   |
    | 指定された名前             | 指定された名前        |
    |                        | ID プロバイダー |
    | 姓                | 姓           |
    |                        | ユーザーのオブジェクト ID  |

1. **作成** を選択します。

次の図は、ユーザー フローにおける Azure AD B2C の登録とサインインの例です。

![登録とサインイン ポリシーの設定。](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>プロファイル編集ユーザー フロー ポリシーの作成

プロファイル編集ユーザー フロー ポリシーを作成するには、次の手順を実行します。

1. Azure ポータルで、左のナビゲーション ウィンドウの **ユーザー フロー (ポリシー)** を選択します。
1. **Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー** を選択します。
1. **プロファイルの編集** を選択し、**推奨** バージョン を選択します。
1. **名前** で、プロファイル編集ユーザー フローを入力します。 この名前は、後でポータルによって割り当てられる接頭語 (「B2C_1_」など) で表示されます。
1. **ID プロバイダー** の **ローカル アカウント** セクションで、**電子メール サインイン** を選択します。
1. **ユーザー属性** で、次のチェック ボックスを選択します。
    
    | **属性の収集** | **返品クレーム** |
    | ---------------------- | ----------------- |
    |                        | 電子メール アドレス   |
    | 指定された名前             | 指定された名前        |
    |                        | ID プロバイダー |
    | 姓                | 姓           |
    |                        | ユーザーのオブジェクト ID  |
    
1. **作成** を選択します。

次の図は、Azure AD B2C プロファイル編集ユーザー フローの例を示しています。

![Azure AD B2C プロファイル編集ユーザー フローの作成の例](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>パスワード リセット ユーザー フロー ポリシーの作成

パスワード リセット ユーザー フロー ポリシーを作成するには、次の手順を実行します。

1. Azure ポータルで、左のナビゲーション ウィンドウの **ユーザー フロー (ポリシー)** を選択します。
1. **Azure AD B2C – ユーザー フロー (ポリシー)** ページで、**新しいユーザー フロー** を選択します。
1. **パスワードのリセット** を選択し、**推奨** バージョン を選択します。
1. **名前** に、パスワード リセット ユーザー フローの名前を入力します。
1. **ID プロバイダー** で、**電子メール アドレスを使用したパスワードのリセット** を選択します。
1. **作成** を選択します。
1. **アプリケーション クレーム** で、次のチェック ボックスを選択します。
    - **電子メール アドレス**
    - **指定された名前**
    - **姓**
    - **ユーザーのオブジェクト ID**
1. **作成** を選択します。

次の図は、Azure AD B2C パスワード リセットのユーザー フローで、**メール アドレスを使用したパスワードのリセット** を設定する場所を示しています。

![パスワード リセット ポリシーで「メール アドレスを使用してパスワードをリセットする」を設定する](./media/B2CImage_13.png)

## <a name="next-steps"></a>次のステップ

Commerce で B2C テナントを設定するプロセスを続行するには、[ソーシャル ID プロバイダーの追加](add-social-identity-providers.md) に進みます。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]