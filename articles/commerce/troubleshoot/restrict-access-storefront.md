---
title: テストまたは開発中の店舗へのアクセスを制限する
description: この記事では、内部のテストまたは開発を行っている間に Microsoft Dynamics 365 Commerce の店舗へのアクセスを制限する方法について説明します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292030"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>テストまたは開発中の店舗へのアクセスを制限する

[!include [banner](../../includes/banner.md)]

この記事では、内部のテストまたは開発を行っている間に Microsoft Dynamics 365 Commerce の店舗へのアクセスを制限する方法について説明します。

## <a name="description"></a>説明

内部のテストや現在開発中の間は、外部ユーザーが公開された店舗ページにアクセスできないように、サイトへのアクセスを制限することができます。

## <a name="resolution"></a>解像度

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>標準のユーザー フローを使用して Azure AD B2C を設定する

eコマース サイトの Azure Active Directory B2C (Azure AD B2C) を構成する方法の詳細については、[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md) を参照してください。

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>店舗ページへのユーザー アクセスを制限して新しいユーザーの作成をブロックする

Commerce サイト ビルダーで店舗ページへのユーザー アクセスを制限するには、次の手順に従います。

1. サイトに移動します。
1. **ページ** を選択し、ユーザー アクセスを制限するページを選択します。
1. モジュールまたはフラグメント スロットを選択して、**編集** を選択します。
1. プロパティ ウィンドウで、**サインインが必要?** を選択して、**編集完了** を選択します。
1. **公開** を選択します。

Azure AD の新しいユーザーの作成をブロックするには、次の手順に従います。

1. [Azure ポータル](https://portal.azure.com/) に移動します。
1. サイト アクセス用に作成した Azure AD B2C アプリケーションを選択します。
1. 左のナビゲーション ウィンドウで、**ユーザー フロー** を選択します。
1. **ユーザー フロー** ページの上部で、**新しいユーザー フロー** を選択します。
1. **ユーザー フロー タイプの選択** ページで、**プレビュー** を選択します。
1. ページの中程で、**v2 にサインイン** を選択します。 次に、[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md) の手順に従って、テストまたは開発中に Azure AD B2C のサイトの標準ユーザー フローとしてフローを構成します。

## <a name="additional-resources"></a>追加リソース

[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md)

[ユーザーのサインインに対するカスタム ページの設定](../custom-pages-user-logins.md)
