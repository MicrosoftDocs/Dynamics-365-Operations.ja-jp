---
title: クラウドを利用した検索の概要
description: この記事では、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8a3ab869eb9ddc0e73061bd2363cf9b3962da1e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850359"
---
# <a name="cloud-powered-search-overview"></a>クラウドを利用した検索の概要

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。

製品の発見可能性は、カテゴリの閲覧、検索、およびフィルタリングにより、顧客が迅速かつ簡単に製品を見つけられることを保証するのに役立ちます。 小売業者は、eコマースや POS (販売時点情報管理) など、CSU (クラウド スケール ユニット) を活用したチャネルにおいて、商品発見を顧客との対話のための主要なツールとして考えています。

顧客は、Web 検索エンジン、洗練された E コマース Web サイト、ソーシャル アプリ、検索用語の入力時に表示される自動提案、ファセット ナビゲーション、および強調表示のほぼ瞬時の応答時間に慣れています。 ある EC ショップで探している商品がすぐに見つからなければ、お客様は迷わず別の EC ショップに移動してしまいます。

クラウド パワーによる商品検索機能を備えたコマースにより、小売業者は CSU を活用したチャネルで消費者の定着率とコンバージョン率を継続的に向上させることができます。

Commerce の検索機能は、小売業者がより優れた商品発見力を実現するために改良されています。 同時に、これらの機能は e コマースのトラフィックに必要なスケーラビリティとパフォーマンスを提供します。

## <a name="browse-and-search"></a>参照と検索

製品の発見は主に、情報の取得とコンテンツ ナビゲーションの検索機能に依存するため、検索の関連性とパフォーマンスはオムニチャネル エクスペリエンスの重要な要素です。 効果的かつ効率的な参照と検索のエクスペリエンスによって、コンバージョンが増える場合があります。

次の図は、一般的な参照と検索の機能の例を示しています。

![ランディング ページを検索します。](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>ファセットナビゲーションと選択の概要 

ファセット ナビゲーションを使用すると、用語セット内の用語にリンクされた絞り込み条件をフィルタ処理することにより、顧客はコンテンツを簡単に参照できるようになります。 顧客が絞り込み条件を選択して適用すると、選択肢の概要が表示されます。 

ファセット ナビゲーションを使用することで、追加のページを作成することなく、用語セット内の用語ごとに異なる絞り込み条件をコンフィギュレーションできます。 

次の図は、ファセット ナビゲーションが検索で使用されている例を示しています。

![選択の概要。](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>没入型の自動提案

現在の自動提案機能では、一致するキーワードの検索をトリガーするキーワードが表示されます。 Commerce の新しい機能拡張により、ユーザーは入力を完了する前に製品へのリンクを見つけることができます。

Commerce では、さまざまなカテゴリでのキーワード照合の機能もサポートされています。 この機能により、顧客はカテゴリ全体で一致するキーワードの数を確認し、他のカテゴリのキーワードの検索をトリガーできます。

次の図は、没入型の自動提案が使用されている例を示しています。

![没入型の自動提案。](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>並べ替え

Commerce の強化された並べ替えにより、顧客は検索結果を並べ替え、検索、参照し、価格、製品名、製品番号などの基準で検索結果を絞り込むことができます。 顧客は、製品が新しいか、売れ筋か、または最近追加されたかに基づいて、結果を並べ替えることもできます。

> [!NOTE]
> これらのクラウドを利用した検索機能は、バージョン 10.0.8 以降で使用できます。 **Commerce パラメーター > 構成パラメーター** で 「ProductSearch.UseAzureSearch」 の項目が 「true」 に設定されていることを確認します。 
![クラウドを利用した検索のためのコンフィギュレーション パラメーター。](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>追加リソース

[既定のカテゴリ ランディング ページと検索結果ページの概要](category-search-page-overview.md)

[SEO メタデータの管理](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
