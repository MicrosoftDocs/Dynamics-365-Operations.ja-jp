---
title: 発注受入にすべての費用が含まれていない
description: 発注受入にすべての費用が含まれていない
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
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476834"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>発注受入にすべての費用が含まれていない

## <a name="symptoms"></a>現象

発注書を受領するとき、すべての費用が受領書に含まれていません。

### <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **調達パラメーター** ページの **配送** タブで、**製品受領時に費用を生成** オプションが *はい* に設定されていることを確認します。
1. 費用を含む発注書を作成します。
1. 発注書を確認します。
1. 発注書を受け取ります。
1. 受入合計を確認し、予想される合計と比較します。
1. すべての費用が発注受入に含まれているわけではないことに注意してください。

## <a name="resolution"></a>解決策

解決策は、雑費が設定されている方法によって異なります。 要件に合わせて雑費を設定する方法については、次のブログ記事を参照してください: [製品受領時に雑費を計上する](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。
