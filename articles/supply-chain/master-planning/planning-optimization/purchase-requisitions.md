---
title: 購買要求
description: このトピックでは、計画の最適化で購買要求がどのようにサポートされるのかについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501081"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="7580e-103">購買要求</span><span class="sxs-lookup"><span data-stu-id="7580e-103">Purchase requisitions</span></span>

<span data-ttu-id="7580e-104">マスター プランでは、承認済購買要求の補充を行えます。</span><span class="sxs-lookup"><span data-stu-id="7580e-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="7580e-105">したがって、購買要求を処理するために、ユーザーはワークフローを使用して発注書を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7580e-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="7580e-106">代わりに、購買要求をマスター プランの対象にできます。</span><span class="sxs-lookup"><span data-stu-id="7580e-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="7580e-107">この機能により、購買要求は関連製品に対して設定されている **計画オーダー タイプ** 値に応じて、発注書、移動オーダー、または製造オーダーを生成できます。</span><span class="sxs-lookup"><span data-stu-id="7580e-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="7580e-108">要求を含むマスター プランを有効にする</span><span class="sxs-lookup"><span data-stu-id="7580e-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="7580e-109">マスター プランの補充計算時に要求を含めるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7580e-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="7580e-110">**マスター プラン** \> **設定** \> **計画** \> **マスター プラン** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7580e-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7580e-111">マスター プランを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="7580e-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="7580e-112">**一般** クイック タブで、**要求を含める** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="7580e-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="7580e-113">要求を含める追加のマスタ プランごとに手順2 と 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7580e-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="7580e-114">承認済要求タイム フェンス</span><span class="sxs-lookup"><span data-stu-id="7580e-114">Approved requisitions time fence</span></span>

<span data-ttu-id="7580e-115">*承認済要求タイム フェンス* は、マスター プランに承認済の補充要求の需要が含まれる日数の過去の日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7580e-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="7580e-116">承認済要求タイム フェンスは、補充グループ レベルとマスタ プラン レベルの両方で設定できます。</span><span class="sxs-lookup"><span data-stu-id="7580e-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="7580e-117">補充グループに対する承認済要求タイム フェンスの設定</span><span class="sxs-lookup"><span data-stu-id="7580e-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="7580e-118">**マスター プラン** \> **設定** \> **補充** \> **補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7580e-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="7580e-119">補充グループを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="7580e-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="7580e-120">**その他** のクイック タブで、**承認済要求タイム フェンス (日数)** フィールドをタイム フェンスに含める日数を設定します。</span><span class="sxs-lookup"><span data-stu-id="7580e-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7580e-121">承認済要求タイム フェンスを設定する追加の補充グループごとに手順 2 と 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7580e-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="7580e-122">個々のマスター プランに対する承認済要求タイム フェンスの設定</span><span class="sxs-lookup"><span data-stu-id="7580e-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="7580e-123">個々のマスター プランに対して承認済要求タイム フェンスを設定すると、該当する補充グループのタイム フェンスの設定が設定によって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7580e-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="7580e-124">**マスター プラン** \> **設定** \> **計画** \> **マスター プラン** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7580e-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7580e-125">マスター プランを作成または選択します。</span><span class="sxs-lookup"><span data-stu-id="7580e-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="7580e-126">**タイム フェンス (日)** のクイック タブで、**承認済要求タイム フェンス (日数)** フィールドをタイム フェンスに含める日数を設定します。</span><span class="sxs-lookup"><span data-stu-id="7580e-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7580e-127">承認済要求タイム フェンスを設定する追加のマスター プランごとに手順 2 と 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7580e-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7580e-128">**近い時期:** 承認済の要求タイム フェンスが計画の最適化でまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7580e-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="7580e-129">サポートされるまでは、**承認済要求** タイム フェンス (日数) フィールドに入力のすべての値が無視されます。</span><span class="sxs-lookup"><span data-stu-id="7580e-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="7580e-130">補充コードに関係なく、独立した供給</span><span class="sxs-lookup"><span data-stu-id="7580e-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="7580e-131">購買要求は、補充コードに関係なく、常に独立した計画オーダーによって補充されます。</span><span class="sxs-lookup"><span data-stu-id="7580e-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="7580e-132">この動作によって、購買要求と補充注文の追跡性とワークフローが明確になります。</span><span class="sxs-lookup"><span data-stu-id="7580e-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="7580e-133">例 1</span><span class="sxs-lookup"><span data-stu-id="7580e-133">Example 1</span></span>

<span data-ttu-id="7580e-134">製品は、**補充コード** 値が *最小/最大* の製品として設定されています。在庫ステータスと要求ステータスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7580e-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7580e-135">手持在庫数 = 10。</span><span class="sxs-lookup"><span data-stu-id="7580e-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="7580e-136">最小在庫数 = 15。</span><span class="sxs-lookup"><span data-stu-id="7580e-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7580e-137">最大在庫数量 = 20。</span><span class="sxs-lookup"><span data-stu-id="7580e-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7580e-138">1 個の購買要求が存在します。</span><span class="sxs-lookup"><span data-stu-id="7580e-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7580e-139">今日の要求日があります。</span><span class="sxs-lookup"><span data-stu-id="7580e-139">It has a requested date of today.</span></span>

<span data-ttu-id="7580e-140">マスター プランを実行すると、2 つの計画オーダーが作成されます (1 つは 10 個で在庫を最大数量に補充し、1 つは 1 個で購買要求の補充を行う)。</span><span class="sxs-lookup"><span data-stu-id="7580e-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="7580e-141">例 2</span><span class="sxs-lookup"><span data-stu-id="7580e-141">Example 2</span></span>

<span data-ttu-id="7580e-142">製品は、**補充コード** 値が *最小/最大* の製品として設定されています。在庫ステータスと要求ステータスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7580e-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7580e-143">手持在庫数 = 17。</span><span class="sxs-lookup"><span data-stu-id="7580e-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="7580e-144">最小在庫数 = 15。</span><span class="sxs-lookup"><span data-stu-id="7580e-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7580e-145">最大在庫数量 = 20。</span><span class="sxs-lookup"><span data-stu-id="7580e-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7580e-146">1 個の購買要求が存在します。</span><span class="sxs-lookup"><span data-stu-id="7580e-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7580e-147">今日の要求日があります。</span><span class="sxs-lookup"><span data-stu-id="7580e-147">It has a requested date of today.</span></span>

<span data-ttu-id="7580e-148">マスター プランを実行すると、購買要求の補充のために、1 個に対して 1 つの計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7580e-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="7580e-149">例 3</span><span class="sxs-lookup"><span data-stu-id="7580e-149">Example 3</span></span>

<span data-ttu-id="7580e-150">製品は、**補充コード** 値が *期間* および期間の長さが 7 日間の値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7580e-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="7580e-151">在庫、販売注文、要求のステータスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7580e-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="7580e-152">手持在庫数 = 0。</span><span class="sxs-lookup"><span data-stu-id="7580e-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="7580e-153">5 個の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="7580e-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="7580e-154">出荷予定日が今日に 1 日を加えたものがあります。</span><span class="sxs-lookup"><span data-stu-id="7580e-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="7580e-155">3 個の購買要求が存在します。</span><span class="sxs-lookup"><span data-stu-id="7580e-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="7580e-156">今日プラス 3 日の要求日があります。</span><span class="sxs-lookup"><span data-stu-id="7580e-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="7580e-157">マスター プランを実行すると、2 つの計画オーダーが作成されます (3 つは 10 個で在庫を最大数量に補充し、1 つは 5 個で販売注文要求の補充を行う)。</span><span class="sxs-lookup"><span data-stu-id="7580e-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="7580e-158">購買要求にペギングされる計画オーダーが固定された後、計画エンジンは購買要求にペギングを維持します。</span><span class="sxs-lookup"><span data-stu-id="7580e-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="7580e-159">確認された注文に購買要求を満たすために必要な数量が不足しているのが見つかった場合は、差異に対して新しい計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7580e-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="7580e-160">購買要求の詳細については、[購買要求の概要](../../procurement/purchase-requisitions-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7580e-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]