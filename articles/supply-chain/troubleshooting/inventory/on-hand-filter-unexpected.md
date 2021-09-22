---
title: 手持在庫リスト ページのフィルター ペインが期待した通りに機能しない
description: "\"手持在庫リスト\" ページのフィルター ペインにあるフィルタ―では、期待した通りの結果のフィルター処理が行われません。"
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476905"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>手持在庫リスト ページのフィルター ペインが期待した通りに機能しない

## <a name="symptoms"></a>現象

**手持在庫リスト**  ページのフィルター ペインにあるフィルタ―では、期待した通りの結果のフィルタ処理は行されません。

## <a name="resolution"></a>解決策

 **手持在庫リスト**  ページは、使用可能なすべての分析コードを含む詳細な手持在庫テーブルから構成されています。 ただし、このページの一覧には概要情報が表示されます。 そのため、表示される分析コードに応じて値を集計することで、ソース テーブルからの行を結合することができます。

フィルターペインで設定したフィルターは、集計リストではなく、ソース テーブルに適用されます。 [これらの例](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) で示すように、この動作によって予期しない結果が生成される場合があります。

ただし、 [グリッドで指定されているフィルタ](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) は集計リストに適用され  *ません* 。 これらのフィルターには、グリッドの上部にクイック フィルターが含まれており、各列のヘッダーに対してフィルターが適用されます。
