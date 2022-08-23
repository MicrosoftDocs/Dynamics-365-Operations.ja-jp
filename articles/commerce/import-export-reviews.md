---
title: 評価やレビューのインポートとエクスポート
description: この記事では、Microsoft Dynamics 365 Commerce で商品の評価やレビューをインポートとエクスポートする方法について説明します。
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271938"
---
# <a name="import-and-export-ratings-and-reviews"></a>評価やレビューのインポートとエクスポート

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で商品の評価やレビューをインポートとエクスポートする方法について説明します。

Dynamics 365 Commerce は、オムニチャネル ソリューションとして、[評価とレビュー](ratings-reviews-overview.md)を提供しています。 Dynamics 365 Commerce の評価、レビュー ソリューションに切り替えた際に、既存の評価とレビュー データを Commerce プラットフォームに移行する場合があります。 また、ビジネス要件に応じて、Commerce から評価やレビューのデータをエクスポートすることもできます。 Power Automate コネクタを使用すると、評価とレビューを Commerce にインポートして Commerce からエクスポートできます。

> [!NOTE]
> Power Automate でロジック フローを使い始める方法については、[Power Automate でクラウド フローを作成する](/power-automate/get-started-logic-flow)を参照してください。

## <a name="prerequisites"></a>必要条件

評価とレビューをインポートおよびエクスポートするには、次の前提条件を満たす必要があります:

- 評価とレビュー ソリューションは、Commerceプラットフォーム上の電子コマース サイトに対して有効にする必要があります。 詳細については、[評価とレビューのオプト イン](opt-in-ratings-reviews.md) を参照してください。
- Dynamics 365 Ratings と Reviews Power App Connector は、Power Automate で「レビューの送信」、または「レビューのエクスポート」のいずれかのアクションを有効にするように設定する必要があります。 詳細については、[Dynamics 365 Commerce - 評価とレビュー (プレビュー)](/connectors/dynamics365ratingsre/)を参照してください。
- Commerce の外部から評価とレビューのアプリケーション プログラミング インターフェース (API) を安全に呼び出すためには、サービス間 (S2S) 認証を構成する必要があります。 詳細については、[サービス間認証の構成](service-to-service-auth.md)を参照してください。

## <a name="import-ratings-and-reviews"></a>評価とレビューのインポート

既存のシステムから Commerce に評価やレビューのデータをインポートするには、Dynamics 365 Ratings と Review Power Automate コネクタを既存の Power Automate フローまたは新規フローに追加する必要があります。 詳細については、[Dynamics 365 Commerce - 評価とレビュー (プレビュー)](/connectors/dynamics365ratingsre/)を参照してください。

> [!IMPORTANT]
> この手順を完了する前に、[S2S 認証を構成](service-to-service-auth.md)する必要があります。

Dynamics 365 Ratings と Reviews Power Automate コネクタを使用して Commerce に評価とレビューをインポートするには、以下の手順に従います。

1. **ユーザー レビューの送信** アクションを選択します。
1. S2S 認証の設定時に作成した Azure Active Directory (Azure AD) アプリの情報を使って、接続を確立します。 詳細については、[サービス間認証の構成](service-to-service-auth.md) を参照してください。
1. **ユーザー レビューの送信** アクションでは、一度に 1 件のレビューが行われます。 そのため、このアクションを繰り返します。 ソース レビューをリストとして使用して、一括レビューを送信します。
    
## <a name="export-ratings-and-reviews"></a>評価とレビューのエクスポート

Commerce から評価とレビューのデータをエクスポートするには、Dynamics 365 Ratings と Review Power Automate コネクタを既存の Power Automate フロー、または新規フローに追加する必要があります。 詳細については、[Dynamics 365 Commerce - 評価とレビュー (プレビュー)](/connectors/dynamics365ratingsre/)を参照してください。

Dynamics 365 Ratings と Reviews Power Automate コネクタを使用して Commerce から評価とレビューをエクスポートするには、次の手順に従います。

1. **すべてのレビューうぃエクスポートする** アクションを選択します。
1. アクションを完了します。 

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](opt-in-ratings-reviews.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューの構成](configure-ratings-reviews.md)

[製品評価の同期](sync-product-ratings.md)

[モデレーターによる評価とレビューの手動公開を有効にする](manual-publish-rating-reviews.md)

[サービス間認証の構成](service-to-service-auth.md)

[評価とレビューに関するよく寄せられる質問](ratings-reviews-faq.md)
