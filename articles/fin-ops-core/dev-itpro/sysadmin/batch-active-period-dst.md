---
title: 有効なバッチ期間における夏時間のサポート
description: このトピックでは、有効なバッチ期間における夏時間のサポートに関する情報を提供します。
author: karimelazzouni
manager: AnnBe
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: Dynamics365Operations
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: NotInToc
ms.assetid: a6685c6f-74bf-4f09-a19d-76130d7ce2da
ms.search.region: Global
ms.author: kaelazzo
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: acc28fc4bd838d985519e5d533b7a363efc92789
ms.sourcegitcommit: f0a45daf60ff0e41ac24de93351d43ec46117757
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2020
ms.locfileid: "3618652"
---
# <a name="daylight-saving-time-support-for-active-batch-periods"></a><span data-ttu-id="02fa9-103">有効なバッチ期間における夏時間のサポート</span><span class="sxs-lookup"><span data-stu-id="02fa9-103">Daylight saving time support for active batch periods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02fa9-104">Microsoft Dynamics 365 Finance バージョン 10.0.12 には、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)で有効にできる、**バッチ ジョブの有効期間における夏時間のサポート**機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02fa9-104">Microsoft Dynamics 365 Finance version 10.0.12 includes a **Daylight Saving Time support for batch job active periods** feature that can be turned on in [Feature management](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span> <span data-ttu-id="02fa9-105">この機能を使用すると、[バッチ ジョブの有効な期間](activeperiod.md)における夏時間 (DST) のサポートが導入され、ユーザーはそれぞれの有効期間を異なるタイムゾーンに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="02fa9-105">This feature introduces daylight saving time (DST) support for the [active periods for batch jobs](activeperiod.md) and lets users associate their active periods with different time zones.</span></span>

> [!NOTE] 
> <span data-ttu-id="02fa9-106">この機能は一方向の機能です。</span><span class="sxs-lookup"><span data-stu-id="02fa9-106">This feature is a one-way feature.</span></span> <span data-ttu-id="02fa9-107">つまり、電源をオンにした後にオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="02fa9-107">In other words, it can't be turned off after it's turned on.</span></span>

<span data-ttu-id="02fa9-108">この機能をオンにすると、次の変化が発生します。</span><span class="sxs-lookup"><span data-stu-id="02fa9-108">When this feature is turned on, the following changes occur:</span></span>

- <span data-ttu-id="02fa9-109">**バッチ ジョブの有効期間** ページで、有効な期間ごとに **タイムゾーン** フィールドが追加されます。</span><span class="sxs-lookup"><span data-stu-id="02fa9-109">On the **Active periods for batch jobs** page, a **Timezone** field is added for each active period.</span></span> <span data-ttu-id="02fa9-110">このフィールドでは、有効な期間が使用するタイムゾーンを指定します。</span><span class="sxs-lookup"><span data-stu-id="02fa9-110">This field specifies the time zone that the active period uses.</span></span> <span data-ttu-id="02fa9-111">既定では、有効なすべての期間において、世界協定時刻 (UTC) タイムゾーンが最初に使用されます。</span><span class="sxs-lookup"><span data-stu-id="02fa9-111">By default, every active period initially uses the Coordinated Universal Time (UTC) time zone.</span></span>

    ![[バッチ ジョブの有効期間] ページの [タイムゾーン] フィールド](./media/active-periods-dst.png)

- <span data-ttu-id="02fa9-113">既存の有効期間の開始時刻と終了時刻は、UTC タイムゾーンに従って調整されます。</span><span class="sxs-lookup"><span data-stu-id="02fa9-113">The start and end times of existing active periods are adjusted according to the UTC time zone.</span></span> <span data-ttu-id="02fa9-114">有効期間は、以前の開始と終了と同じ時刻に開始および終了しますが、ユーザーの優先タイムゾーンが UTC ではない場合は、表示される時間が変わる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="02fa9-114">'Although the active periods will continue to start and end at the same times that they previously started and ended, the times that are shown might change if the user's preferred time zone isn't UTC.</span></span>
- <span data-ttu-id="02fa9-115">有効期間は、関連付けられているタイムゾーンの夏時間調整に従います。</span><span class="sxs-lookup"><span data-stu-id="02fa9-115">Active periods will follow the DST adjustments of the time zones that they are associated with.</span></span>
