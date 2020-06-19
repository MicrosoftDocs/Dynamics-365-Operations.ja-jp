---
title: 製品推奨事項の概要
description: このトピックは、製品推奨事項に関する一般情報を提供します。 製品推奨事項により、顧客は必要な製品や元々購入する予定ではなかった製品も簡単かつ迅速に見つけることができます。
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 1b01589322c26b6a7b69d1b992b03603f5f3d29a
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404351"
---
# <a name="product-recommendations-overview"></a>製品推奨事項の概要

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce を使用して、E コマース Web サイトおよび販売時点管理 (POS) デバイスで製品推奨事項を表示できます。 製品推奨事項とは、顧客が興味を持っている可能性がある品目です。 推奨事項は、オンライン ストアおよび従来型店舗における他の顧客の購入傾向に基づいています。

製品の推奨事項により、顧客は自分に役立つ製品を簡単かつ迅速に見つけることができます。 クロスセルおよびアップセルは、顧客が元々購入する予定ではなかった製品を見つけるためにも使用されます。 製品の検出を強化するために推奨事項を使用した場合、より多くの変換の機会を作り出して販売収益を増やし、また顧客満足度と定着を増幅させることもできます。

E コマースにおいて、製品推奨事項は、Microsoft の推奨機械学習マシンの学習技術により大規模に強化されています。

## <a name="recommendation-service"></a>推奨サービス

製品推奨事項サービスは、次の方法で人為的知能と機械学習 (AI-ML) テクノロジを利用します。

- 推奨サービスが必要とする形式のデータは、コマース運用データベースから抽出され、Azure Data Lake Storage かエンティティ ストアに送信されます。
- 推奨サービスは保存済データを使用して、**人気製品**、**よく一緒に購入される製品**、**新規**、**ベストセラー**、および**トレンド** リストに対する推奨モデルをトレーニングします。

## <a name="scenarios"></a>シナリオ

製品推奨事項は、次のシナリオで使用可能です。

- **E コマースの参照またはランディング ページの店舗ページにおいて:** 顧客または店舗スタッフが店舗ページにアクセスする場合、推奨エンジンは、**新規**、**ベストセラー**、および**トレンド** リストの製品を提案することができます。
- **製品の詳細ページにおいて:** 顧客または店舗スタッフが**製品の詳細**ページにアクセスした場合、推奨エンジンは購入される可能性がある追加の品目を提案します。 これらの品目は、**人気製品**リストに表示されます。
- **トランザクション ページまたはチェックアウト ページにおいて:** 推奨エンジンは、買い物カゴ内の品目のリスト全体に基づいて提案します。 これらの項目は、**よく一緒に購入される製品**リストに表示されます。
- **パーソナライズされた推奨事項:** マーチャンダイザーは、既存のリストシナリオをその顧客に基づいてパーソナライズできる新しい機能に加えて、サインインしたユーザーにパーソナライズされた**おすすめ**リストを提供できます。 詳細については、[カスタマイズされた推奨事項を有効にする。](personalized-recommendations.md) を参照してください。

### <a name="types-of-product-recommendations"></a>製品推奨事項のタイプ

次の表では、小売業者が [製品収集モジュール](product-collection-module-overview.md) を介して Dynamics 365 Commerce ソリューションで実装可能なさまざまなタイプの自動化製品推奨事項について説明します。 サイトの作成者がこのオプションを選択している場合、小売業者はサインインしたユーザーに対してパーソナライズされた結果を表示することもできます。

| 製品収集モジュール  | 種類 | 説明 |
|----------------------------|------|-------------|
| 新規                        | アルゴリズム | このモジュールは、チャネルおよびカタログに対して最近類別された最新の製品のリストを表示します。 |
| ベストセラー               | アルゴリズム | このモジュールは、最大販売注文数でランク付けされている製品のリストを表示します。 |
| トレンド                   | アルゴリズム | このモジュールは、指定期間において業績が最上位で、最大販売注文数でランク付けされている製品のリストを表示します。  |
| よく一緒に購入される品目 | AI-ML | このモジュールは、最も消費者の現在の買い物カゴのコンテンツと共に購入される製品の一覧を推奨します。 |
| その他のお勧め           | AI-ML | このモジュールは、消費者の購入パターンに基づき、指定されたシード製品に対する製品を推奨します。 |
| おすすめ              | AI-ML | このモジュールは、サインインしたユーザーの購入パターンに基づいてパーソナライズされた製品の一覧を推奨します。 ゲスト ユーザーの場合、このリストは折りたたまれています。 |

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた製品推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)
