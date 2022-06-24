---
title: 評価とレビュー ソリューションが無効な場合に、評価絞り込み機能が検索結果やカテゴリ ページに表示される
description: この記事では、eコマース サイトで Microsoft Dynamics 365 Commerce の評価およびレビュー ソリューションが無効な場合に、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にする方法に関して、トラブルシューティング ガイドを示します。
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c35e176fc5673de194a81a3a4694a83f7bc9aa00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885061"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>評価とレビュー ソリューションが無効な場合に、評価絞り込み機能が検索結果やカテゴリ ページに表示される

[!include [banner](../includes/banner.md)]

この記事では、eコマース サイトで Microsoft Dynamics 365 Commerce の評価およびレビュー ソリューションが無効な場合に、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にする方法に関して、トラブルシューティング ガイドを示します。

## <a name="description"></a>説明

評価とレビュー ソリューションを使用していない eコマース チャネルで、検索結果やカテゴリ ページに表示される評価絞り込み機能が表示されます。

## <a name="resolution"></a>解決策

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>Commerce サイト ビルダーの評価の非表示設定を有効にする

Commerce サイト ビルダーで **評価を非表示にする** 設定を有効にして、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にするには、次の手順に従います。

1. **サイト 設定 \> 拡張機能** に移動します。
1. **評価とレビュー** で、**評価を非表示にする** チェックボックスをオンにします。
1. **保存と公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](../ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](../opt-in-ratings-reviews.md)
