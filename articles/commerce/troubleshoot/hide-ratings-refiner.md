---
title: 評価とレビュー ソリューションが無効な場合に、評価絞り込み機能が検索結果やカテゴリ ページに表示される
description: このトピックでは、eコマース サイトで Microsoft Dynamics 365 Commerce の評価およびレビュー ソリューションが無効な場合に、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にする方法に関して、トラブルシューティング ガイドを示します。
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3438d12f4ffd06b07cbef724cda8fa490a5f4eb
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472641"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>評価とレビュー ソリューションが無効な場合に、評価絞り込み機能が検索結果やカテゴリ ページに表示される

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、eコマース サイトで Microsoft Dynamics 365 Commerce の評価およびレビュー ソリューションが無効な場合に、検索結果およびカテゴリ ページで評価の絞り込み機能を非表示にする方法に関して、トラブルシューティング ガイドを示します。

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
