---
title: バンドル品目は、会社間プロセスではサポートされません
description: バンドル品目の商品は購入できません。 販売注文では、バンドル品目自体ではなく、バンドル品目のコンポーネントだけが購入されます。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476878"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>バンドル品目は、会社間プロセスではサポートされません

## <a name="symptoms"></a>現象

このバンドル品目は、発注書に対しては使用できません。なぜなら、このバンドル品目の販売注文明細行を確認すると、数量が *0* (ゼロ) になり、ステータスが *キャンセル済* であることがわかります。

## <a name="resolution"></a>解決策

この動作は仕様です。 この販売注文では、バンドル品目のコンポーネントのみが購入されます。 バンドル品目自体は購入されません。 バンドルを購入する必要がある場合、この機能は実際には収益認識シナリオのために設計されているため、バンドル品目としてマークする必要があるかどうかを検討します。 バンドル品目についての詳細情報は、[バンドル](/dynamics365/finance/accounts-receivable/revenue-recognition-setup) を参照してください。
