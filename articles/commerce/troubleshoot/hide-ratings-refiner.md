---
title: 評価とレビュー ソリューションが無効な場合に、評価絞り込み機能が検索結果やカテゴリ ページに表示される
description: この記事では、eコマース サイトで Microsoft Dynamics 365 Commerce の評価およびレビュー ソリューションが無効な場合に、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にする方法に関して、トラブルシューティング ガイドを示します。
author: gvrmohanreddy
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 28a3cefd6aab81f5e7907bda457763f2306e5a1d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267380"
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
