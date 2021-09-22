---
title: WMS が有効な倉庫に対して処理できない直納
description: 倉庫で WMS が有効になっている場合は、直納はサポートされません。 直納を使用するには、WMS 以外の品目および倉庫を選択する必要があります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476928"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>WMS が有効な倉庫に対して処理できない直納

## <a name="symptoms"></a>現象

倉庫管理 (WMS) に対して有効な倉庫からの直納のために品目が販売明細行に追加された場合、販売明細行の更新時に次のエラー メッセージが表示されます。

> 倉庫管理が有効になっているため、倉庫 1% に対して直納を処理できません。 倉庫管理で有効になっていない別の倉庫を指定してください。

## <a name="resolution"></a>解決策

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現時点では、WMS は直接配送をサポートしていません。 したがって、直納を使用するには、WMS 以外の品目および倉庫を選択する必要があります。
