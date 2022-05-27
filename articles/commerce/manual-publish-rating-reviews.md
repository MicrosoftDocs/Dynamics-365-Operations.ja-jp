---
title: モデレーターによる評価とレビューの手動公開を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce でモデレーターによる評価とレビューの手動公開を有効にする方法、および評価とレビューを手動公開する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0709173b8c3dfb7018d0bd9a712554112722a1f3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693285"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>モデレーターによる評価とレビューの手動公開を有効にする

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce でモデレーターによる評価とレビューの手動公開を有効にする方法、および評価とレビューを手動公開する方法について説明します。

Dynamics 365 Commerce の評価とレビューのソリューションでは、Azure Cognitive Services を使用して、レビュー タイトルとコンテンツの不適切な言葉を自動的に編集し、評価とレビューを公開します。 したがって、eコマース サイトに対する評価とレビューを確認および公開するために、手動による操作は必要ありません。

ただし、一部の企業では、モデレーターがレビューを公開する前に、手動でレビューを行い、レビューを承認することを選択する場合があります。 モデレーターによる評価とレビューの手動公開を有効にするには、Commerce サイト ビルダーの **評価とレビュー用モデレーターの要求** 機能を有効にする必要があります。

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Commerce サイト ビルダーの評価とレビュー用モデレーターの要求機能を有効にする

Commerce サイト ビルダーの **評価とレビュー用モデレーターの要求** 機能を有効にするには、次の手順を実行します。

1. **ホーム \> レビュー \> 設定** に移動します。
1. **評価とレビュー用モデレーターの要求** オプションを **オン** に設定します。

> [!NOTE]
> **評価とレビュー用モデレーターの要求** 機能を有効にすることで、評価とレビューの自動公開が停止され、手動公開が必要になります。 ただし、Azure Cognitive Services は引き続きレビュー タイトルとコンテンツの不適切な言葉を編集します。

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>評価とレビューを公開する

**評価とレビュー用モデレーターの要求** 機能を有効にした場合、モデレーターは評価とレビューを手動で確認および公開して、eコマース サイトに表示する必要があります。

Commerce サイト ビルダーで評価とレビューを確認および公開するには、次の手順を実行します。

1. **レビュー \> 管理** に移動します。
1. グリッドで、行の **状態** フィールドが **未公開** に設定されている場合、その行の評価とレビューはまだ公開されていません。 未公開の評価とレビューのみを表示するには、グリッドの上にある状態フィルターで **状態: レビューが必要** を選択します。
1. **未公開** の状態を持つ評価とレビューを 1 つ以上選択し、コマンド バーで **公開** を選択します。 選択した評価とレビューは公開キューに追加され、公開後に eコマース サイトに表示されます。

> [!NOTE]
> - 評価とレビューを公開すると、状態値は **未公開** から null 値 (空白のフィールド) に変更します。
> - 状態が混在する複数の評価とレビューを選択し、**公開** を選択した場合、まだ公開されていない評価とレビューが公開されます。 ただし、既に公開されている評価とレビューは、再び公開されません。

次の図は、Commerce サイト ビルダーの **管理** ページで 3 つの未公開の評価とレビューが選択されている例を示します。

![Commerce サイト ビルダーの管理ページで選択された 3 つの未公開の評価とレビュー。](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](opt-in-ratings-reviews.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューのコンフィギュレーション](configure-ratings-reviews.md)

[製品評価の同期](sync-product-ratings.md)

[評価とレビューのインポートとエクスポート](import-export-reviews.md)

[サービス間認証の構成](service-to-service-auth.md)

[評価とレビューに関するよく寄せられる質問](ratings-reviews-faq.md)
