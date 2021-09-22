---
title: 売買契約における通貨換算の問題
description: 通貨が発注書で異なる場合、売買契約価格は通貨に従って再計算されない
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476840"
---
# <a name="trade-agreement-currency-conversion-issues"></a>売買契約における通貨換算の問題

## <a name="symptoms"></a>現象

通貨が発注書で異なる場合、売買契約価格が通貨に従って再計算されません。

## <a name="resolution"></a>解決策

*一般通貨* 機能を使用すると、価格と割引を 1 つの通貨でのみ定義できます。 その後、必要に応じて、他の通貨に換算できます。 さらに、換算が完了すると、機能によって自動的にスマート丸めが適用されます。
