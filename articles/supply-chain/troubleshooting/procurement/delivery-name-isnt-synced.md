---
title: 発注書の配送先住所を変更した後、配送先名は同期されません
description: 発注書ヘッダーの配送先住所を変更した後、配送先名は同期されません
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476844"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>発注書の配送先住所を変更した後、配送先名は同期されません

## <a name="symptoms"></a>現象

発注書のヘッダーの住所が配送先住所ではない住所に更新されます。 住所は発注書上で更新されますが、更新された住所に基づいて配送先名が更新されることはありません。

## <a name="resolution"></a>解決策

この動作は仕様です。 選択された住所は配送先住所として分類される必要があります。 それ以外の場合、選択した住所に基づいて配送先名が更新されることはありません。
