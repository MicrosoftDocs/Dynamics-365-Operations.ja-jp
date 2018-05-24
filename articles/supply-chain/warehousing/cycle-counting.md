---
title: "循環棚卸"
description: "この記事は、倉庫管理で使用できる倉庫ソリューションで、循環棚卸を使用する方法について説明します。 この記事は、在庫管理で使用できる倉庫ソリューションには適用されません。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9da40e90982d9d4aca38890ed121782f4236712d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="cycle-counting"></a><span data-ttu-id="ddd6f-104">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ddd6f-104">Cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddd6f-105">この記事は、倉庫管理で使用できる倉庫ソリューションで、循環棚卸を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="ddd6f-106">この記事は、在庫管理で使用できる倉庫ソリューションには適用されません。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="ddd6f-107">循環棚卸は、手持在庫品目を監査するために使用できる倉庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="ddd6f-108">循環棚卸プロセスは 3 つの手順で表すことができます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="ddd6f-109">**循環棚卸作業の作成** – 循環棚卸作業は、品目のしきい値パラメーターに基づいて、または循環棚卸計画を使用して自動的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="ddd6f-110">または、**品目別循環棚卸作業**ページまたは**場所別循環棚卸作業**ページの品目パラメーターまたは倉庫パラメーターを使用して、手動で循環棚卸作業を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="ddd6f-111">**プロセス循環棚卸** – 循環棚卸作業の作成後、倉庫の場所の品目の棚卸をし、Microsoft Dynamics 365 for Finance and Operations への結果の入力にモバイル デバイスを使用して、循環棚卸作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ddd6f-112">または、循環棚卸作業を作成せずに、倉庫の場所の品目を棚卸できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="ddd6f-113">このプロセスは*スポット循環棚卸*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="ddd6f-114">**循環棚卸値の差異の解決** – 循環棚卸後、棚卸値の差異がある品目は、**すべての作業**ページの作業状態が**検討保留**です。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="ddd6f-115">これらの差異は**循環棚卸作業が検討保留**ページで解決できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="ddd6f-116">次の図は、循環棚卸プロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-116">The following illustration shows the cycle counting process.</span></span> ![循環棚卸のプロセス フロー](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="ddd6f-118">循環棚卸計画の前提条件</span><span class="sxs-lookup"><span data-stu-id="ddd6f-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="ddd6f-119">次の表に、循環棚卸を使用する前に準備が整っている必要のある前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ddd6f-120">前提条件</span><span class="sxs-lookup"><span data-stu-id="ddd6f-120">Prerequisite</span></span></th>
<th><span data-ttu-id="ddd6f-121">説明</span><span class="sxs-lookup"><span data-stu-id="ddd6f-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddd6f-122">品目</span><span class="sxs-lookup"><span data-stu-id="ddd6f-122">Item</span></span></td>
<td><span data-ttu-id="ddd6f-123">品目は倉庫管理プロセスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddd6f-124">倉庫</span><span class="sxs-lookup"><span data-stu-id="ddd6f-124">Warehouse</span></span></td>
<td><span data-ttu-id="ddd6f-125">倉庫は倉庫管理プロセスで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="ddd6f-126">倉庫管理プロセスで倉庫を有効にするには、<strong>倉庫</strong> ページで、倉庫を選択し、<strong>倉庫管理プロセスの使用</strong> オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="ddd6f-127">循環棚卸中に作業者がパレットを移動できるようにするには、<strong>倉庫管理</strong> クイック タブで、<strong>循環棚卸中にパレット移動を許可</strong> オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddd6f-128">作業プール</span><span class="sxs-lookup"><span data-stu-id="ddd6f-128">Work pools</span></span></td>
<td><span data-ttu-id="ddd6f-129">オプション: 倉庫作業を作業のタイプ (この場合、循環棚卸作業) に基づいて分類する作業プールを作成します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddd6f-130">場所</span><span class="sxs-lookup"><span data-stu-id="ddd6f-130">Locations</span></span></td>
<td><span data-ttu-id="ddd6f-131">場所の循環棚卸を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="ddd6f-132">倉庫の場所の循環棚卸を許可するには、<strong>場所プロファイル</strong> ページで、<strong>循環棚卸を許可</strong> オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddd6f-133">倉庫管理パラメーター</span><span class="sxs-lookup"><span data-stu-id="ddd6f-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="ddd6f-134">循環棚卸のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="ddd6f-135"><strong>倉庫管理パラメーター</strong> ページで、既定の調整タイプ コード、作業クラス ID、および循環棚卸の作業優先順位を指定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddd6f-136">モバイル デバイス</span><span class="sxs-lookup"><span data-stu-id="ddd6f-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="ddd6f-137"><strong>モバイル デバイスのメニュー項目</strong> ページで、次の方法のいずれかのメニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="ddd6f-138">ユーザー主導の循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ddd6f-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="ddd6f-139">システム主導の循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ddd6f-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="ddd6f-140">循環棚卸のグループ化</span><span class="sxs-lookup"><span data-stu-id="ddd6f-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="ddd6f-141">スポット循環棚卸</span><span class="sxs-lookup"><span data-stu-id="ddd6f-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="ddd6f-142">モバイル デバイスのメニューを設定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="ddd6f-143">作業ユーザー アカウントを作成し、作業のユーザー ID にモバイル デバイス メニューを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ddd6f-144">関連する設定作業</span><span class="sxs-lookup"><span data-stu-id="ddd6f-144">Related setup task</span></span></td>
<td><span data-ttu-id="ddd6f-145">倉庫の場所の循環棚卸計画を設定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="ddd6f-146">循環棚卸作業の自動作成</span><span class="sxs-lookup"><span data-stu-id="ddd6f-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="ddd6f-147">循環棚卸作業の定期的な作成をスケジュールする 2 つの方法があります。循環棚卸作業のしきい値を設定するか、または循環棚卸計画を設定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="ddd6f-148">循環棚卸のしきい値は、在庫品目の数量または割合の限度を示します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="ddd6f-149">循環棚卸作業は、しきい値の限度に達したときに自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="ddd6f-150">循環棚卸計画は、バッチ ジョブを介して直ちにまたは定期的に循環棚卸作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="ddd6f-151">循環棚卸作業が作成されるときには、どの場所をカウントするかに関する情報が棚卸作業明細行に含まれます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="ddd6f-152">この場所に関連付けられる手持の棚卸資産はブロックされず、未処理の棚卸作業がある場合も引当や出荷処理で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="ddd6f-153">品目のしきい値パラメーターに基づいて循環棚卸作業を作成する</span><span class="sxs-lookup"><span data-stu-id="ddd6f-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="ddd6f-154">循環棚卸作業は、品目数が場所の固有のしきい値を下回る場合に作成できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="ddd6f-155">たとえば、循環棚卸のしきい値が 40 の場所に 60 品目あります。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="ddd6f-156">販売注文トランザクション中に、25 品目がその場所からピッキングされてステージング場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="ddd6f-157">新しい品目の総数 35 はしきい値の数量より少ないため、その場所のための循環棚卸作業が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="ddd6f-158">循環棚卸作業のスケジュール</span><span class="sxs-lookup"><span data-stu-id="ddd6f-158">Schedule cycle counting work</span></span>

<span data-ttu-id="ddd6f-159">循環棚卸計画は、循環棚卸作業を直ちにまたは定期的に作成するために作成できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="ddd6f-160">循環棚卸計画を設定することで、循環棚卸作業が作成される作業プール、異なる場所の品目に対して作成される循環棚卸の最大数、倉庫の場所が再度数えられるまでの日数を制御できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="ddd6f-161">たとえば、品目が倉庫の 3 つの場所で使用でき、循環棚卸の最大数は **2** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="ddd6f-162">この場合、循環棚卸計画を実行すると、品目が存在する 2 つの場所に対して 2 つの循環棚卸が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="ddd6f-163">別の例として、循環棚卸間の日数を **5** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="ddd6f-164">この場合、循環棚卸作業は 5 日ごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="ddd6f-165">ただし、循環棚卸作業が 3 日目に処理される場合は、次の循環棚卸作業は、最後の循環棚卸処理の 5 日後の 8 日目に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="ddd6f-166">循環棚卸作業の手動作成</span><span class="sxs-lookup"><span data-stu-id="ddd6f-166">Create cycle counting work manually</span></span>
<span data-ttu-id="ddd6f-167">循環棚卸作業を手動で作成するには、**品目別循環棚卸作業**または**場所別循環棚卸作業**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="ddd6f-168">作成する循環棚卸の最大数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="ddd6f-169">たとえば、倉庫マネージャーが値 **5** を指定すると、その品目が 10 の場所にある場合でも、循環棚卸作業は 5 つの場所に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="ddd6f-170">作成された循環棚卸作業 ID を割り当てる作業プール ID も選択できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="ddd6f-171">循環棚卸のために作業プール ID が処理されると、作業プールに割り当てられた循環棚卸作業の ID は、グループとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="ddd6f-172">モバイル デバイスを使用して循環棚卸を実行する</span><span class="sxs-lookup"><span data-stu-id="ddd6f-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="ddd6f-173">モバイル デバイスの Finance and Operations を使用した循環棚卸作業のプロセス処理には複数の方法があります。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-173">There are several methods for processing cycle counting work by using Finance and Operations on a mobile device:</span></span>

-   <span data-ttu-id="ddd6f-174">**ユーザー主導** – 作業者は**オープン**状態の循環棚卸作業の ID を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="ddd6f-175">**システム主導** – Finance and Operations が作業者に循環棚卸作業の ID を割当てます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-175">**System directed** – Finance and Operations assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="ddd6f-176">**循環棚卸のグループ化** – 作業者は特定の場所、ゾーン、または作業プールに固有の、循環棚卸作業の ID をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="ddd6f-177">**スポット循環棚卸** – 作業者は循環棚卸作業を作成せずに、いつでも倉庫の場所の品目を棚卸できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="ddd6f-178">場所で循環棚卸を実行するには、作業者が場所の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="ddd6f-179">モバイル デバイスを使用してスポット循環棚卸を実行する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="ddd6f-180">デバイスで作業者に表示される指示は、スポット循環棚卸のメニュー項目の設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="ddd6f-181">モバイル デバイスで、スポット循環棚卸作業をプロセス処理するメニュー品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="ddd6f-182">スポット循環棚卸を実行する場所を登録します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="ddd6f-183">品目番号およびカウント済の品目の数量を登録して確認します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="ddd6f-184">**メモ:** 循環棚卸作業の状態は、**作業者**ページで設定されたパラメーターに応じ、**すべての作業**ページで**検討保留**または**終了済み**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="ddd6f-185">オプション: その場所の残りの品目に対してステップ 3 を繰り返し、棚卸に使用できる追加品目がないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="ddd6f-186">循環棚卸の差異を解決する</span><span class="sxs-lookup"><span data-stu-id="ddd6f-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="ddd6f-187">循環棚卸の差異は、作業ユーザー ID の**循環棚卸の監督ですか**オプションが**いいえ**に設定されている場合、次のシナリオで発生します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="ddd6f-188">棚卸の値は、**作業ユーザー**ページの**割合の上限**または**数量の上限**フィールドで指定された、誤差限度内にありません。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="ddd6f-189">たとえば、場所の手持棚卸資産の数量は 50 で、作業ユーザーの誤差限度は 10 です。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="ddd6f-190">作業ユーザーが 40 から 60 の間の値を入力する場合、差異が発生します。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="ddd6f-191">棚卸の値は手持ち棚卸資産の数量と異なり、誤差限度は設定されません。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="ddd6f-192">棚卸の値の差異を調整し、棚卸の値を**循環棚卸の検討保留**ページで受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="ddd6f-193">品目の数量の変更済み総数は、**保管場所ごとの手持在庫**ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="ddd6f-194">差異を承認できない場合、棚卸の値は否認されます。</span><span class="sxs-lookup"><span data-stu-id="ddd6f-194">The counted value is rejected if the difference can't be approved.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddd6f-195">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ddd6f-195">Additional resources</span></span>
[<span data-ttu-id="ddd6f-196">倉庫作業のモバイル デバイスの構成</span><span class="sxs-lookup"><span data-stu-id="ddd6f-196">Configure mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)




