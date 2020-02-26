---
title: 製品推奨事項の概要
description: このトピックは、製品推奨事項に関する一般情報を提供します。 製品推奨事項により、顧客は必要な製品や元々購入する予定ではなかった製品も簡単かつ迅速に見つけることができます。
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024982"
---
# <a name="product-recommendations-overview"></a>製品推奨事項の概要

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce を使用して、E コマース Web サイトおよび販売時点管理 (POS) デバイスで製品推奨事項を表示できます。 製品推奨事項とは、顧客が興味を持っている可能性がある品目です。 推奨事項は、オンライン ストアおよび従来型店舗における他の顧客の購入傾向に基づいています。

製品の推奨事項により、顧客は自分に役立つ製品を簡単かつ迅速に見つけることができます。 クロスセルおよびアップセルは、顧客が元々購入する予定ではなかった製品を見つけるためにも使用されます。 製品の検出のために推奨事項を使用した場合、より多くの変換の機会を作り出して販売収益を増やし、また顧客満足度と定着の強化することもできます。

コマースにおいて、製品推奨事項は、Microsoft の推奨機械学習マシンの学習技術により大規模に強化されています。


## <a name="scenarios"></a>シナリオ

製品推奨事項は、次のシナリオで使用可能です。

- **E コマースの参照またはランディング ページの店舗ページにおいて:** 顧客または店舗スタッフが店舗ページにアクセスする場合、推奨エンジンは、**新規**、**ベストセラー**、および**トレンド** リストの製品を提案することができます。
- **製品の詳細ページにおいて:** 顧客または店舗スタッフが**製品の詳細**ページにアクセスした場合、推奨エンジンは購入される可能性がある追加の品目を提案します。 これらの品目は、**人気製品**リストに表示されます。
- **トランザクション ページまたはチェックアウト ページにおいて:** 推奨エンジンは、買い物カゴ内の品目のリスト全体に基づいて提案します。 これらの項目は、**よく一緒に購入される製品**リストに表示されます。
- **パーソナライズされた推奨事項:** マーチャンダイザーは、既存のリストシナリオをその顧客に基づいてパーソナライズできる新しい機能に加えて、サインインしたユーザーにパーソナライズされた**おすすめ**リストを提供できます。 詳細については、機能ドキュメント参照してください: [パーソナライズされた推奨事項を有効にします。](personalized-recommendations.md)

## <a name="recommendation-service"></a>推奨サービス

製品推奨事項は、次のように推奨機械学習マシンの学習技術を使用します。

- 推奨サービスが必要とする形式のデータは、コマース運用データベースから抽出され、エンティティ ストアに送信されます。
- 推奨サービスはデータを使用して、**人気製品**、**よく一緒に購入される製品**、**新規**、**ベストセラー**、および**トレンド** リストに対する推奨モデルをトレーニングします。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の有効化](enable-product-recommendations.md)

[パーソナライズされた推奨事項の有効化](personalized-recommendations.md)

[製品収集モジュールの概要](product-collection-module-overview.md)

[Curated 製品推奨事項リストの作成](create-editorial-recommendation-lists.md)

[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)

[ページへの製品推奨リストの追加](add-reco-list-to-page.md)
