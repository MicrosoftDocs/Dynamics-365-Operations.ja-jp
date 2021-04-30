---
title: 安全マージン
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインで安全マージンをどのように使用できるかについて説明します。
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9dc305f46dad6b372721805669529bbc9ac554e8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908296"
---
# <a name="safety-margins"></a><span data-ttu-id="cc9ac-103">安全マージン</span><span class="sxs-lookup"><span data-stu-id="cc9ac-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc9ac-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインで安全マージンをどのように使用できるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="cc9ac-105">安全マージンの概要</span><span class="sxs-lookup"><span data-stu-id="cc9ac-105">Safety margins overview</span></span>

<span data-ttu-id="cc9ac-106">安全マージンの目的は、通常のリードタイムの範囲を超えたバッファー時間を提供する設定を有効にすることです。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="cc9ac-107">たとえば、素材が仕入先から到着した後でアンパックまたは検査しなければならない場合、このアプローチではサプライヤーに対して追加のバッファー時間が与えられるので、購入リードタイムに余分な時間を追加するだけではできません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="cc9ac-108">この例では、入庫幅を使用して、仕入先が早期に配送されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="cc9ac-109">この方法では、品目を内部処理できるようにバッファー時間が提供されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="cc9ac-110">安全マージンには 3 つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="cc9ac-111">**マージンの再並べ替え** - 供給注文を配置するためのバッファー時間</span><span class="sxs-lookup"><span data-stu-id="cc9ac-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="cc9ac-112">**入庫幅** - 入荷する供給を処理するためのバッファー時間</span><span class="sxs-lookup"><span data-stu-id="cc9ac-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="cc9ac-113">**払出安全日数** - 出荷の処理に使用されるバッファー時間</span><span class="sxs-lookup"><span data-stu-id="cc9ac-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="cc9ac-114">次の図は、これらの安全マージンが時間の経過と共に適用される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-114">The following illustration shows how these safety margins apply over time.</span></span>

![安全マージン](media/safety-margins-1.png)

<span data-ttu-id="cc9ac-116">すべてのマージンは日数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-116">All margins are defined in days.</span></span> <span data-ttu-id="cc9ac-117">*0* (ゼロ) の規定値は、マージンが適用されていないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="cc9ac-118">複数のマージンを設定すると、それらは供給の *注文日* から需要の *要求日* までの合計時間に加算されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="cc9ac-119">たとえば、設定にリードタイムがなく、3 種類すべてのマージンが 1 日に設定されているとします。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="cc9ac-120">この場合、供給の注文日と需要要求日の間に 3 日間の日数があります。そのため、注文日が 7 月 1 日であれば、要求日は 7 月 4 日になります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="cc9ac-121">入庫幅</span><span class="sxs-lookup"><span data-stu-id="cc9ac-121">Receipt margin</span></span>

<span data-ttu-id="cc9ac-122">入庫幅は、おそらく 3 つの安全マージンで最も使用されています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="cc9ac-123">これは、*出荷日* に対して、*要求日* から逆算して適用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="cc9ac-124">つまり、製品が必要となる前に、指定された入庫幅の日数の間に製品が入庫する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="cc9ac-125">次の図では、入庫幅を強調表示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-125">The following illustration highlights the receipt margin.</span></span>

![入庫幅](media/safety-margins-2.png)

<span data-ttu-id="cc9ac-127">通常、入庫幅は、システムの一般リードタイムの一部としては獲得されない、倉庫登録またはその他の時間がかかるプロセスのための時間を確保するためのバッファーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="cc9ac-128">購入の場合、発注書の *出荷日* がそれに応じて移動することが 1 つのベネフィットになります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="cc9ac-129">安全マージンを使用するのではなく、リードタイムを延長した場合でも、仕入先は最後に出荷するように求められます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="cc9ac-130">入庫幅によって、供給の *要求日* が変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="cc9ac-131">したがって、需要と供給の要求日を比較する場合 (**正味必要量** ページなど) は、入庫幅が直接表示されません 。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="cc9ac-132">たとえば、入庫幅が 4 日間に設定され、購買注文明細行がその月の 15 日に入庫するようにスケジュール設定されている場合、マスター プランの計算によって調整された入荷日はその月の 19 日になります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="cc9ac-133">供給品として手持在庫が使用されている場合は、入庫幅は適用されません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="cc9ac-134">すべての手持在庫は、実際に入庫された時期に関係なく、すぐに使用可能と見なされます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="cc9ac-135">再発注マージン</span><span class="sxs-lookup"><span data-stu-id="cc9ac-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="cc9ac-136">**間もなく:** この機能は計画の最適化ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="cc9ac-137">サポート対象となるまでは、**品目のリードタイムに追加された再注文マージン** に入力されたすべての値はに入力されたすべての値は *0* (ゼロ) として処理されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="cc9ac-138">次の図では、再注文マージンを強調表示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-138">The following illustration highlights the reorder margin.</span></span>

![再発注マージン](media/safety-margins-3.png)

<span data-ttu-id="cc9ac-140">再注文マージンは、マスター プラン中のすべての計画オーダーについて、品目のリードタイムの前に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="cc9ac-141">したがって、供給オーダーを配置するための時間が余分に必要になります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="cc9ac-142">このマージンは、通常、注文の作成時に承認プロセスまたはその他の内部プロセスに必要な時間を確保するためにバッファーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="cc9ac-143">再注文マージンは、供給の *注文日* と *開始日* の間に置かれます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="cc9ac-144">払出安全日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="cc9ac-145">**間もなく:** この機能は計画の最適化ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="cc9ac-146">サポート対象となるまでは、**要求日から差し引いた払出安全日数** に入力されたすべての値は *0* (ゼロ) として処理されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="cc9ac-147">次の図では、払出安全日数を強調表示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-147">The following illustration highlights the issue margin.</span></span>

![払出安全日数](media/safety-margins-4.png)

<span data-ttu-id="cc9ac-149">払出安全日数は、マスター プラン時に需要要求日から差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="cc9ac-150">この機能を使用すると、需要注文に反応して出荷できるように時間を確保することができます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="cc9ac-151">このマージンは、通常、出荷と関連する出庫倉庫プロセスの時間を保証するためのバッファーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="cc9ac-152">払出安全日が適用されると、関連する供給と需要の要求日が一致しなくなることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="cc9ac-153">代わりに、払出安全日は供給の *要求日* と需要の *要求日* の間に追加されるため、これらは払出安全日によって異なります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="cc9ac-154">安全マージンの設定</span><span class="sxs-lookup"><span data-stu-id="cc9ac-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="cc9ac-155">機能管理で安全マージンをオンにする</span><span class="sxs-lookup"><span data-stu-id="cc9ac-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="cc9ac-156">計画の最適化でこの機能を使用する前に、システム上でこれを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="cc9ac-157">管理者は、[機能の管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-157">Admins can use the [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="cc9ac-158">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="cc9ac-159">**モジュール:** _マスター プラン_</span><span class="sxs-lookup"><span data-stu-id="cc9ac-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="cc9ac-160">**機能名:** _計画の最適化のためのマージン_</span><span class="sxs-lookup"><span data-stu-id="cc9ac-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="cc9ac-161">安全マージンの定義</span><span class="sxs-lookup"><span data-stu-id="cc9ac-161">Define safety margins</span></span>

<span data-ttu-id="cc9ac-162">安全マージンは、柔軟に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="cc9ac-163">これらの設定は、*補充グループ* と *マスター プラン* の両方で設定できます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="cc9ac-164">マージンはそれぞれが加算されることを理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="cc9ac-165">たとえば、補充グループの 2 日とマスター プランの 3 日で、有効な 5 日間の入庫幅となります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="cc9ac-166">マスタープランのマージンの設定機能は、毎日の計画に影響を与えずに、特定の計画について、より長いリードタイムまたは不確実度をシミュレートする場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="cc9ac-167">補充グループの安全マージン</span><span class="sxs-lookup"><span data-stu-id="cc9ac-167">Coverage group safety margins</span></span>

<span data-ttu-id="cc9ac-168">補充グループに安全マージンを適用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="cc9ac-169">**マスター プラン \> 設定 \> 補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="cc9ac-170">一覧ペインで、目的の補充グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="cc9ac-171">**その他** クイックタブの、**安全マージン日数** セクションで、次のフィールドを使用して必要な安全マージンを設定します (日数)。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="cc9ac-172">要求期日に追加される受領安全日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="cc9ac-173">要求期日から差し引かれる払出安全日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="cc9ac-174">品目のリード タイムに追加される再発注余裕日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="cc9ac-175">マスター プランの安全マージン</span><span class="sxs-lookup"><span data-stu-id="cc9ac-175">Master plan safety margins</span></span>

<span data-ttu-id="cc9ac-176">マスター プランに安全マージンを適用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="cc9ac-177">**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="cc9ac-178">一覧ペインで、目的のマスター プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="cc9ac-179">**安全マージン日数** クイックタブで、次のフィールドを使用して必要な安全マージンを設定します (日数)。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="cc9ac-180">要求期日に追加される受領安全日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="cc9ac-181">要求期日から差し引かれる払出安全日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="cc9ac-182">品目のリード タイムに追加される再発注余裕日数</span><span class="sxs-lookup"><span data-stu-id="cc9ac-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="cc9ac-183">計算がカレンダーの日付または作業日のどちらに基づくかを定義する</span><span class="sxs-lookup"><span data-stu-id="cc9ac-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="cc9ac-184">すべての安全マージンを、カレンダーの日付または作業日のどちらかに基づいて計算されるように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="cc9ac-185">**マスター プラン \> 設定 \> マスター プランのパラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="cc9ac-186">**一般** タブの、**安全マージン日数** セクションで、**作業日数** オプションを *はい* に設定すると、稼働日に基づいてマージンが計算されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="cc9ac-187">カレンダーの日付に基づいて余白を計算する場合はこのオプションを *いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="cc9ac-188">たとえば、カレンダーで月曜から金曜までがオープンで、土曜日から日曜日がクローズだとします。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="cc9ac-189">入庫幅が 1 日の場合、土曜日と日曜日は営業日ではないため、月曜日の要求日によって前の週の金曜日に出荷日が生成されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="cc9ac-190">営業日を決定するために使用するカレンダーは、設定と供給タイプによります。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="cc9ac-191">この設定は、補充グループ、倉庫、仕入先のカレンダーによって制御できます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="cc9ac-192">*倉庫* が補充分析コードの一部ではない (つまり、計画が *サイト* のみに基づいている) 場合、倉庫カレンダーは使用されません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="cc9ac-193">1 つ以上のカレンダーが定義されている設定をシステムで処理できます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="cc9ac-194">次のサブセクションでは、結果を制御するために使用できる組み合わせについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="cc9ac-195">期間に使用されるカレンダー</span><span class="sxs-lookup"><span data-stu-id="cc9ac-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="cc9ac-196">定義されたカレンダーによって、供給注文日から需要要求日までの、カレンダー上の実際の合計リードタイムが制御されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="cc9ac-197">次のカレンダーの優先順位付けが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="cc9ac-198">**購入リードタイム** - 補充グループのカレンダーのみが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="cc9ac-199">**入庫幅** -定義されている場合は、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-200">それ以外の場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="cc9ac-201">**払出安全日数** - 定義されている場合は、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-202">それ以外の場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="cc9ac-203">**注文マージン** - 補充グループのカレンダーのみが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="cc9ac-204">最終的な日付に使用されるカレンダー</span><span class="sxs-lookup"><span data-stu-id="cc9ac-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="cc9ac-205">計画エンジンが特定の日付タイプに対して特定の日付を使用できるかどうかを決定するために、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="cc9ac-206">**購買入荷日** - 定義されている場合は、仕入先カレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-207">そうでなければ、定義されている場合は、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-208">これらのカレンダーのどちらも定義されていない場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="cc9ac-209">**移動入庫日** - 定義されている場合は、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-210">それ以外の場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="cc9ac-211">**生産入庫日** - 定義されている場合は、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-212">それ以外の場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="cc9ac-213">**需要払出オープン日** - 定義されている場合は、倉庫のカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="cc9ac-214">そうでなければ、補充グループのカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="cc9ac-215">**注文オープン日** - 補充グループのカレンダーと仕入先のカレンダーの組み合わせ (交差) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="cc9ac-216">この日付を使用するには、両方のカレンダーがオープンでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="cc9ac-217">これらのカレンダーの 1 つのみが定義されている場合は、そのカレンダーだけが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="cc9ac-218">カレンダー設定の概要マトリックス</span><span class="sxs-lookup"><span data-stu-id="cc9ac-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="cc9ac-219">次の図は、安全マージンが計算されるときに適用されるカレンダーをまとめたマトリックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="cc9ac-220">(画像を選択して、高解像度バージョンの画像を開きます。) 各タイプのカレンダーを指定する場所を示すには、次の省略形と色が使用されます:</span><span class="sxs-lookup"><span data-stu-id="cc9ac-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="cc9ac-221">**補充グループ (CG):** グリーン</span><span class="sxs-lookup"><span data-stu-id="cc9ac-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="cc9ac-222">**倉庫 (WH):** イエロー</span><span class="sxs-lookup"><span data-stu-id="cc9ac-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="cc9ac-223">**仕入先 (V):** ブルー</span><span class="sxs-lookup"><span data-stu-id="cc9ac-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="cc9ac-224">[![カレンダー設定の概要マトリックス](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="cc9ac-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="cc9ac-225">計算遅延</span><span class="sxs-lookup"><span data-stu-id="cc9ac-225">Calculating delays</span></span>

<span data-ttu-id="cc9ac-226">注文が遅延しているかどうかをシステムが判断するとき、3 種類の安全マージンすべてが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="cc9ac-227">たとえば、ある品目のリードタイムが 3 日で、入庫幅が 3 日であるとします。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="cc9ac-228">この品目の販売注文は、今日必要として設定されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="cc9ac-229">この場合、*リードタイム* + *入庫幅* = 4 日として計算されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="cc9ac-230">したがって、今日が 8 月 14 日であれば、4 日間の遅延では 8 月 18 日の出荷が生成されます。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="cc9ac-231">次の図は、この例を示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9ac-231">The following illustration shows this example.</span></span>

![遅延計算の例](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="cc9ac-233">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cc9ac-233">Additional resources</span></span>

[<span data-ttu-id="cc9ac-234">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="cc9ac-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="cc9ac-235">計画最適化適合分析</span><span class="sxs-lookup"><span data-stu-id="cc9ac-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]