---
title: サインイン リンクが eコマース サイトにリダイレクトする
description: このトピックでは、サインイン リンクがサインイン ページに移動するのではなく、eコマース サイトにリダイレクトする場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585403"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>サインイン リンクが eコマース サイトにリダイレクトする

[!include [banner](../../includes/banner.md)]

このトピックでは、サインイン リンクがサインイン ページに移動するのではなく、eコマース サイトにリダイレクトする場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

Commerce サイト ビルダーで新しい Microsoft Azure Active Directory B2C (Azure AD B2C) テナントを構成すると、**サインイン** リンクを選択したユーザーは、サインイン ページに移動せずに、主要な eコマースのランディング ページにリダイレクトされます。

## <a name="resolution"></a>解像度

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Azure AD B2C アプリケーションで返信 URL が正しく構成されていることを確認する

Azure AD B2C アプリケーションで返信 URL が正しく構成されていることを確認するには、次の手順を実行します。

1. [Azure ポータル](https://portal.azure.com/) に移動します。
1. サイト アクセス用に作成した Azure AD B2C アプリケーションを選択します。
1. Azure AD B2C の設定中に作成したアプリケーションを選択します。
1. 次の図の例に示すように、**返信 URL** で、リストにサイト ドメイン URL と eコマースが生成した URL の両方のエントリが含まれていることを確認します。

    ![Azure AD B2C 返信 URL エントリ](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> サイト ドメイン URL と eコマースで生成された URL の両方が、先頭または末尾のスラッシュを含まない有効な URL 形式である必要があります。

## <a name="additional-resources"></a>追加リソース

[Azure Active Directory B2C にWeb アプリケーションを登録する](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md)
