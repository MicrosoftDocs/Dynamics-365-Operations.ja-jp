---
title: 販売注文の場所が変更された場合に税金情報が更新されない
description: 販売注文ヘッダーで、サイト、倉庫、または配送先の住所が変更された場合、明細行でケースの税金情報は更新されません。 手動で行う必要があります。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476880"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>販売注文ヘッダーの場所を変更したら、税金情報が更新されない

## <a name="symptoms"></a>現象

販売注文ヘッダーで、サイト、倉庫、または配送先の住所が変更された場合、明細行でケースの税金情報は更新されません。

## <a name="resolution"></a>解決策

この動作は仕様です。 この問題が発生するのは、明細行レベルで配送先住所、サイト、および倉庫が自動的に変更されないためです。 手動でそれらをを更新する必要があります。
