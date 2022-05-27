---
title: 手持在庫リスト ページのフィルター ペインが期待した通りに機能しない
description: "\"手持在庫リスト\" ページのフィルター ペインにあるフィルターでは、期待した通りの結果のフィルター処理が行われません。"
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686686"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>手持在庫リスト ページのフィルター ペインが期待した通りに機能しない

## <a name="symptoms"></a>現象

**手持在庫リスト** ページのフィルター ペインにあるフィルターでは、期待した通りの結果のフィルター処理が行われません。

## <a name="resolution"></a>解決策

**手持在庫のリスト** ページは、使用可能なすべての分析コードを含む詳細な手持在庫テーブルから構成されています。 ただし、このページの一覧には概要情報が表示されます。 そのため、表示される分析コードに応じて値を集計することで、ソース テーブルからの行を結合することができます。

フィルターペインで設定したフィルターは、集計リストではなく、ソース テーブルに適用されます。 [これらの例](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples) で示すように、この動作によって予期しない結果が生成される場合があります。

ただし、[グリッドで指定されているフィルタは、](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters)集計リストに適用 *され* ます。 これらのフィルターには、グリッドの上部にクイック フィルターが含まれており、各列のヘッダーに対してフィルターが適用されます。
