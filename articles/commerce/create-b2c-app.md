---
title: B2C アプリケーションを作成する
description: この記事では、Microsoft Azure ポータルで企業と顧客間 (B2C) アプリケーションを作成する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785286"
---
# <a name="create-a-b2c-application"></a>B2C アプリケーションを作成する

[!include [banner](includes/banner.md)]

この記事では、Microsoft Azure ポータルで企業と顧客間 (B2C) アプリケーションを作成する方法について説明します。

B2C テナントが作成されたら、新しい Azure Active Directory (Azure AD) テナント内に B2C アプリケーションを作成して、Commerce と通信します。

B2C アプリケーションを作成するには、次の手順に従います。

1. Azure ポータルで、**アプリの登録** を選択し、**新規登録** を選択します。
1. **名前** で、この Azure AD B2C 申請に使用する名前を入力します。
1. **サポートされているアカウント タイプ** で、**任意の ID プロバイダまたは組織ディレクトリで [アカウント] を選択します (ユーザー フローによるユーザーの認証用)**。
1. **リダイレクト URI** の場合は、専用の返信の URL を **Web** タイプとして入力します。 返信 URL およびここでのフォーマットについては、下記の [返信 URL](#reply-urls) を参照してください。 ユーザーが認証を行う際に Azure AD B2C からサイトに戻るアプリケーションを有効にするには、URI / 返信 URL のリダイレクトを入力する必要があります。 登録プロセス中に返信 URL を追加するか、または B2C アプリケーションの **概要** セクションの **概要** メニューから **リダイレクト URI の追加** リンクを選択して後で追加することができます。
1. **アクセス許可** については、**OpenID やオフラインアクセス権限をするための管理者の同意を得る** を選択します。
1. **登録** を選択します。
1. 新しく作成したアプリケーションを選択し、**認証** メニューに移動します。 
1. 返信 URL を入力した場合、**暗黙的な許可とハイブリッド フロー** で、**アクセス トークン** と **ID トークン** の両方のオプションを選択してアプリケーションで使用できるオプションを選択し、**保存** を選択します 。 登録時に返信 URL が入力されていない場合は、**プラットフォームの追加** を選択し、**Web** を選択し、アプリケーションのリダイレクト URL を入力することで、このページに返信 URL を追加することもできます。 **暗黙的な許可とハイブリッド フロー** セクションで、**アクセス トークン** と **ID トークン** のオプションの両方を選択できます。
1. Azure ポータルの **概要** メニューに移動し、**アプリケーション (クライアント) ID** をコピーします。 この ID は、後の設定手順 (後で **クライアント GUID** として参照) に使用します 。

Azure AD B2C のアプリの登録の追加情報については、[Azure Active Directory B2C の新しいアプリケーション登録 エクスペリエンス](/azure/active-directory-b2c/app-registrations-training-guide) を参照してください。

### <a name="reply-urls"></a>返信 URL

返信 URL は、ご利用ののサイトが Azure AD B2C を呼び出してユーザーを認証する際に、リターン ドメインのリストを許可するために重要となります。 これにより、認証されたユーザーがサイン インしたドメイン（ご利用ののサイト ドメイン）に戻ることができます。 

**Azure AD B2C - アプリケーション \> 新しいアプリケーション** の画面の **返信 URL** ボックスには、サイト ドメインと (環境がプロビジョニングされたら) コマースが生成した URL の両方に個別の明細行を作成する必要があります。 これらの URL は、常に有効な URL 形式を使用する必要があり、ベース URL のみにする必要があります (末尾のスラッシュやパスは使用しないでください)。 次に、続く例のように文字列 ``/_msdyn365/authresp`` をベース URL に追加する必要があります。

- ``https://www.fabrikam.com/_msdyn365/authresp`` (ドメインは電子商取引ドメインと完全に一致する必要があります。 複数のドメインがある場合は、ドメインごとにこの URL を追加する必要があります。)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>次のステップ

Commerce で B2C テナントを設定するプロセスを続行するには、[ユーザー フロー ポリシーの作成](create-user-flow-policies.md) に進みます。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
