---
title: 購買がマイナス日以内に存在する場合に計画発注書が作成される
description: 補充コードが最小/最大の場合、マイナス日以内に購買が存在する場合、計画の最適化により計画発注書が作成されます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 94d569684a0bfa2398e98147b9b85531954f8d56748894034a048fa627230ef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775510"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>購買がマイナス日以内に存在する場合に計画発注書が作成される

KB 番号: 4614298

## <a name="symptoms"></a>現象

補充コードが *最小/最大* の場合、マイナス日以内に購買が存在する場合、計画の最適化により計画発注書が作成されます。

## <a name="resolution"></a>解像度

計画の最適化ではマイナス日数はサポートされていません。 ただし、計画オーダーが現在の日付に対するリード タイム内には絶対にスケジュールされないようになります。 たとえば、購買リード タイムが 10 日で、今日から 8 日後に購買注文が到着すると予想されるとします。 この場合、発注書は今日から 5 日後の需要に対する供給として使用されます。

したがって、すべて (またはほとんどすべて) のシナリオをカバーするためにリード タイムを調整することをお勧めします。
