---
title: 仕入先リベートは、請求書に基づいて累計されない
description: 仕入先リベートは、請求書に基づいて累計されない
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
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476919"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>仕入先リベートは、請求書に基づいて累計されない

## <a name="symptoms"></a>現象

転記された請求書の支払期日が異なる場合、それらの請求書は、それらから生成される仕入先リベートには反映されません。

## <a name="resolution"></a>解決策

仕入先リベートの計算時に期日は考慮されません。 実際の仕入先リベートに関して、期日と請求書との関係がより明確になるようにシステムをカスタマイズすることを検討してください。
