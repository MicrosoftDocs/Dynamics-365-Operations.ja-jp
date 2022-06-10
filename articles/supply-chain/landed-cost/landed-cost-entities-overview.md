---
title: 陸揚原価エンティティの概要
description: このトピックでは、外部データ ソースが航海と原価を作成し、コンテナー追跡レコードを更新できるようにする、陸揚原価のデータ エンティティの概要を示します。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3edef76ebb84031e5ce906fbf35d2d331781a534
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813083"
---
# <a name="landed-cost-entities-overview"></a>陸揚原価エンティティの概要

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

**陸揚原価** モジュールは、メーカーから倉庫にインポートされた船荷に対する完全な財務および物流管理を提供することによって、企業がインバウンド出荷作業を合理化するのに役立ちます。 陸揚原価のトランザクション データ エンティティは、外部データ ソース (配送業者サービスなど) が航海と原価を作成し、コンテナー追跡レコードを更新できるようにします。

サポートされている操作のいくつかを次に示します:

- 既存の入庫注文明細行の航海、出荷コンテナー、およびフォリオ レコードを作成および更新します。
- 原価領域ごとに見積原価を作成および更新します。
- 出荷コンテナー活動レコードを作成および更新して、コンテナー輸送の各区画に開始日、見積終了日、および実際の終了日を取得します。
- 仕入先原価請求書配賦を作成します。
