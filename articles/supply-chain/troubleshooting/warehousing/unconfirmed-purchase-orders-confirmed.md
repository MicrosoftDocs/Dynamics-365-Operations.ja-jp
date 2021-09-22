---
title: 製品受領書の更新タスクで、未確認の注文を確認する
description: 製品受領書の更新を実行した後で、ステータスが登録済の未確認の注文がシステムによって確認されます。 この問題を修正する機能について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476841"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>製品受領書の更新を実行すると、未確認の発注書が確認される

## <a name="symptoms"></a>現象

*製品受領書の更新* 定期タスクを実行すると、*登録済* の在庫トランザクション ステータスがある未確認の発注書が自動的に確認されます。

## <a name="resolution"></a>解決策

新しい入庫積荷処理機能 *積荷数量の受入超過* によってこの問題が修正されます。 この機能を有効にするには、[機能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) ワークスペースに移動して、次の機能を記載されている順序でオンにします。

1. 購買注文在庫トランザクションを積荷に関連付けます
2. 積荷数量の過剰入荷

詳細については、[発注書に対する登録済製品の数量の転記](/dynamics365/supply-chain/warehousing/inbound-load-handling)を参照してください。
