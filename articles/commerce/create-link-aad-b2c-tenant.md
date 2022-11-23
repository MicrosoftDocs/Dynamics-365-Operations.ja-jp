---
title: Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする
description: この記事では、Microsoft Azure ポータルの既存の Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントの作成方法またはリンク方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785301"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする

[!include [banner](includes/banner.md)]

この記事では、Microsoft Azure ポータルの Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントの作成方法またはリンク方法について説明します。 詳細については、[チュートリアル: Azure Active Directory B2C テナントを作成する](/azure/active-directory-b2c/tutorial-create-tenant) を参照してください。

Azure portal での既存の Azure AD B2C テナントを作成またはリンクするには、以下の手順を実行します。

1. [Azure ポータル](https://portal.azure.com/)にサインインします。
1. Azure ポータル メニューから、**リソースの作成** を選択します。 Commerce 環境に関連付けられているサブスクリプションとディレクトリを使用してください。

    ![Azure ポータルでのリソースの作成。](./media/B2CImage_1.png)

1. **ID \> Azure Active Directory B2C** に移動します。
1. **新しい B2C テナントの作成または既存のテナントへのリンク** のページで、会社のニーズに適した以下のオプションのいずれかを使用します。

    - **新しい Azure AD B2C テナントの作成**: 新しい Azure AD B2C テナントを作成するには、このオプションを使用します。
        1. **新しい Azure AD B2C テナントの作成** を選択します。
        1. **組織名** に組織名を入力します。
        1. **最初のドメイン名** に最初のドメイン名を入力します。
        1. **国/地域** では、国または地域を選択します。
        1. **作成** を選択して、テナントを作成します。

     ![新しい Azure AD テナントの作成。](./media/B2CImage_2.png)

     - **既存の Azure AD B2C テナントを Azure サブスクリプションにリンクする**: リンクする Azure AD テナントが既にある場合は、このオプションを使用します。
        1. **既存の Azure AD の B2C テナントを Azure サブスクリプションにリンクする** を選択します。
        1. **Azure AD B2C テナント** には、適切な B2C テナントを選択します。 選択ボックスに「適格な B2C テナントが見つかりません」というメッセージが表示された場合は、適格な B2C テナントが存在しないので、新しいテナントを作成する必要があります。
        1. **リソース グループ** で、**新規作成** を選択します。 テナントを格納するリソース グループの **名前** を入力し、**リソース グループの場所** を選択して、**作成** を選択します。

    ![既存の Azure AD B2C テナントを Azure サブスクリプションにリンクする。](./media/B2CImage_3.png)

1. 新しい Azure AD B2C ディレクトリが作成されると (しばらく時間がかかる場合があります)、新しいディレクトリへのリンクがダッシュボードに表示されます。 このリンクを使用すると、「Azure Active Directory B2C へようこそ」のページに移動します。

    ![新しい Azure AD ディレクトリへのリンク](./media/B2CImage_4.png)

> [!NOTE]
> Azure アカウント内に複数のサブスクリプションがある場合、または有効なサブスクリプションにリンクせずに B2C テナントを設定している場合、**トラブルシューティング** バナーは、テナントをサブスクリプションにリンクするよう指示します。 トラブルシューティングのメッセージを選択し、指示に従ってサブスクリプションの問題を解決します。

次の図は、Azure AD B2C **トラブルシューティング** バナーの例を示しています。

![ディレクトリに有効なサブスクリプションがないことを示す警告。](./media/B2CImage_5.png)

## <a name="next-steps"></a>次のステップ

Commerce で B2C テナントを設定するプロセスを続行するには、[B2C アプリケーションを作成する](create-b2c-app.md) に進みます。

## <a name="additional-resources"></a>追加リソース

[B2C テナントを Commerce に 設定](set-up-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
