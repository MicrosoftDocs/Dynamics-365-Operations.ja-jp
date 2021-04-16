---
title: クラウドを利用した検索の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。
author: ashishmsft
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b5182df9d45a3b5d2572a5b6b391c924ef23bf9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800424"
---
# <a name="cloud-powered-search-overview"></a>クラウドを利用した検索の概要

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce でのクラウドを利用した検索の概要を示します。

製品の発見可能性は、カテゴリの閲覧、検索、およびフィルタリングにより、顧客が迅速かつ簡単に製品を見つけられることを保証するのに役立ちます。 小売業者は、製品の検出を、すべてのチャネルでの顧客とのやり取りにおける主要なツールと考えています。

顧客は、Web 検索エンジン、洗練された E コマース Web サイト、ソーシャル アプリ、検索用語の入力時に表示される自動提案、ファセット ナビゲーション、および強調表示のほぼ瞬時の応答時間に慣れています。 探している製品を、ある E コマース ストアで十分な速さで見つけることができなければ、顧客は別の E コマース ストアへ移動してしまいます。

Dynamics 365 Commerce のクラウドを利用した製品の発見可能性により、小売業者は、E コマース チャネルと販売時点管理 (POS) チャネルの両方で、すべてのチャネルにおける消費者の保持とコンバージョンを向上させ続けることができます。

Dynamics 365 Commerce 検索エクスペリエンスの機能が改善され、小売業者は製品の発見可能性を向上させることができます。 同時に、これらの機能は、E コマースのトラフィックに必要なスケーラビリティとパフォーマンスを提供します。

## <a name="browse-and-search"></a>参照と検索

製品の発見は主に、情報の取得とコンテンツ ナビゲーションの検索機能に依存するため、検索の関連性とパフォーマンスはオムニチャネル エクスペリエンスの重要な要素です。 効果的かつ効率的な参照と検索のエクスペリエンスによって、コンバージョンが増える場合があります。

次の図は、一般的な参照と検索の機能の例を示しています。

![検索のランディング ページ](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>ファセットナビゲーションと選択の概要 

ファセット ナビゲーションを使用すると、用語セット内の用語にリンクされた絞り込み条件をフィルタ処理することにより、顧客はコンテンツを簡単に参照できるようになります。 顧客が絞り込み条件を選択して適用すると、選択肢の概要が表示されます。 

ファセット ナビゲーションを使用することで、追加のページを作成することなく、用語セット内の用語ごとに異なる絞り込み条件をコンフィギュレーションできます。 

次の図は、ファセット ナビゲーションが検索で使用されている例を示しています。

![選択の概要](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>没入型の自動提案

現在の自動提案機能では、一致するキーワードの検索をトリガーするキーワードが表示されます。 Dynamics 365 Commerce の新しい機能拡張により、ユーザーは入力を完了する前に製品へのリンクを見つけることができます。

Dynamics 365 Commerce では、さまざまなカテゴリでのキーワード照合の機能もサポートされています。 この機能により、顧客はカテゴリ全体で一致するキーワードの数を確認し、他のカテゴリのキーワードの検索をトリガーできます。

次の図は、没入型の自動提案が使用されている例を示しています。

![没入型の自動提案](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>並べ替え

Dynamics 365 Commerce の強化された並べ替えにより、顧客は検索結果を並べ替え、検索、参照し、価格、製品名、製品番号などの基準で検索結果を絞り込むことができます。 顧客は、製品が新しいか、売れ筋か、または最近追加されたかに基づいて、結果を並べ替えることもできます。

>[!NOTE]
>これらのクラウドを利用した検索機能は、バージョン 10.0.8 以降で使用できます。 **コマース パラメーター > コンフィギュレーション パラメーター** で、「ProductSearch.UseAzureSearch が "true" に設定」されたエントリがあることを確認します。 
![クラウドを利用した検索のためのコンフィギュレーション パラメーター](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>追加リソース

[既定のカテゴリ ランディング ページと検索結果ページの概要](category-search-page-overview.md)

[SEO メタデータの管理](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
