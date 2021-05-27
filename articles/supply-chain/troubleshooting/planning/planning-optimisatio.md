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
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026683"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="eebe5-103">購買がマイナス日以内に存在する場合に計画発注書が作成される</span><span class="sxs-lookup"><span data-stu-id="eebe5-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="eebe5-104">KB 番号: 4614298</span><span class="sxs-lookup"><span data-stu-id="eebe5-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="eebe5-105">現象</span><span class="sxs-lookup"><span data-stu-id="eebe5-105">Symptoms</span></span>

<span data-ttu-id="eebe5-106">補充コードが *最小/最大* の場合、マイナス日以内に購買が存在する場合、計画の最適化により計画発注書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="eebe5-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="eebe5-107">解像度</span><span class="sxs-lookup"><span data-stu-id="eebe5-107">Resolution</span></span>

<span data-ttu-id="eebe5-108">計画の最適化ではマイナス日数はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="eebe5-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="eebe5-109">ただし、計画オーダーが現在の日付に対するリード タイム内には絶対にスケジュールされないようになります。</span><span class="sxs-lookup"><span data-stu-id="eebe5-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="eebe5-110">たとえば、購買リード タイムが 10 日で、今日から 8 日後に購買注文が到着すると予想されるとします。</span><span class="sxs-lookup"><span data-stu-id="eebe5-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="eebe5-111">この場合、発注書は今日から 5 日後の需要に対する供給として使用されます。</span><span class="sxs-lookup"><span data-stu-id="eebe5-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="eebe5-112">したがって、すべて (またはほとんどすべて) のシナリオをカバーするためにリード タイムを調整することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="eebe5-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
