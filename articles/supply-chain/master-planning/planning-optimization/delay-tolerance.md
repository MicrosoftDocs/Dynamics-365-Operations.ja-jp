---
title: 遅延許容範囲 (マイナス在庫日数)
description: このトピックでは、遅延許容範囲の計算、および計画の最適化における計画オーダーの作成への影響に関する情報を提供します。
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306466"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="86e92-103">遅延許容範囲 (マイナス在庫日数)</span><span class="sxs-lookup"><span data-stu-id="86e92-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="86e92-104">遅延許容範囲機能を使用すると、計画の最適化により、補償グループに設定されている **マイナス在庫日数** の値を考慮できます。</span><span class="sxs-lookup"><span data-stu-id="86e92-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="86e92-105">これは、マスター プランの際に適用される遅延許容範囲の期間を拡張するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="86e92-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="86e92-106">このようにして、既存の供給が短期間の遅延後に需要を満たすことができる場合は、新しい供給注文の作成を回避できます。</span><span class="sxs-lookup"><span data-stu-id="86e92-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="86e92-107">この機能の目的は、特定の需要に対して新しい供給注文を作成する意味があるかどうかを決定することです。</span><span class="sxs-lookup"><span data-stu-id="86e92-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="86e92-108">システムで機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="86e92-108">Turn on the feature in your system</span></span>

<span data-ttu-id="86e92-109">遅延許容範囲機能をシステムで使用するには、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*計画最適化のマイナス在庫日数* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="86e92-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="86e92-110">計画の最適化の遅延許容範囲</span><span class="sxs-lookup"><span data-stu-id="86e92-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="86e92-111">遅延許容範囲は、既存の供給が既に計画されているときに新しい補充を注文するまでに待機するリード タイムを超えた日数を表します。</span><span class="sxs-lookup"><span data-stu-id="86e92-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="86e92-112">遅延許容範囲は、営業日ではなくカレンダー日を使用して定義します。</span><span class="sxs-lookup"><span data-stu-id="86e92-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="86e92-113">マスター プランの時点で、システムにより遅延許容範囲が計算されるときに **マイナス在庫日数** 設定が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="86e92-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="86e92-114">**補充グループ** ページまたは **品目補充** ページで **マイナス在庫日数** の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="86e92-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="86e92-115">システムにより、*最も早い補充日* に遅延許容範囲の計算がリンクされ、これは今日の日付にリード タイムを加えた日付です。</span><span class="sxs-lookup"><span data-stu-id="86e92-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="86e92-116">遅延許容範囲は、次の式を使用して計算され、*max()* は 2 つの値の大きい方を検出します。</span><span class="sxs-lookup"><span data-stu-id="86e92-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="86e92-117">*max(最も早い補充日、需要期日)* – *需要期日* + *マイナス在庫日数*</span><span class="sxs-lookup"><span data-stu-id="86e92-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="86e92-118">この式により、製品リード タイム中に十分な供給があるときは、マスター プランによって新しい供給注文が作成されないようにします。</span><span class="sxs-lookup"><span data-stu-id="86e92-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="86e92-119">計画の最適化における遅延許容範囲の計算では、組み込みのマスター プランからの動的マイナス在庫日数計算が常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="86e92-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="86e92-120">**マスター プラン パラメーター** ページの **動的マイナス在庫日数を使用** の設定は、この動作には影響しません。</span><span class="sxs-lookup"><span data-stu-id="86e92-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="86e92-121">既存の供給によって計算された遅延許容範囲以下の需要遅延が意味される場合、計画の最適化によって、既存の供給が需要と共に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="86e92-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="86e92-122">場合によっては、過剰な供給よりも需要を遅延することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="86e92-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="86e92-123">次のサブセクションでは、遅延許容範囲が計画最適化での計画オーダーの作成にどのような影響を及ぼすかを示す例を提供します。</span><span class="sxs-lookup"><span data-stu-id="86e92-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="86e92-124">例 1</span><span class="sxs-lookup"><span data-stu-id="86e92-124">Example 1</span></span>

<span data-ttu-id="86e92-125">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="86e92-125">A product has the following configuration:</span></span>

- <span data-ttu-id="86e92-126">**リード タイム:** *10*</span><span class="sxs-lookup"><span data-stu-id="86e92-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="86e92-127">**マイナス在庫日数:** *2*</span><span class="sxs-lookup"><span data-stu-id="86e92-127">**Negative days:** *2*</span></span>

<span data-ttu-id="86e92-128">次の供給と需要は製品に対して存在します。</span><span class="sxs-lookup"><span data-stu-id="86e92-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="86e92-129">**今日の需要:** 数量が 10 の販売注文</span><span class="sxs-lookup"><span data-stu-id="86e92-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="86e92-130">**12 日以内の供給:** 数量が 10 の発注書</span><span class="sxs-lookup"><span data-stu-id="86e92-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="86e92-131">既存の供給で、12 日以内の需要をカバーでき、その期間は遅延許容範囲と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="86e92-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="86e92-132">したがって、マスター プランを実行すると、計画オーダーは作成されません。</span><span class="sxs-lookup"><span data-stu-id="86e92-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="86e92-133">例 2</span><span class="sxs-lookup"><span data-stu-id="86e92-133">Example 2</span></span>

<span data-ttu-id="86e92-134">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="86e92-134">A product has the following configuration:</span></span>

- <span data-ttu-id="86e92-135">**リード タイム:** *10*</span><span class="sxs-lookup"><span data-stu-id="86e92-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="86e92-136">**マイナス在庫日数:** *0*</span><span class="sxs-lookup"><span data-stu-id="86e92-136">**Negative days:** *0*</span></span>

<span data-ttu-id="86e92-137">次の供給と需要は製品に対して存在します。</span><span class="sxs-lookup"><span data-stu-id="86e92-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="86e92-138">**今日の需要:** 数量が 10 の販売注文</span><span class="sxs-lookup"><span data-stu-id="86e92-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="86e92-139">**12 日以内の供給:** 数量が 10 の発注書</span><span class="sxs-lookup"><span data-stu-id="86e92-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="86e92-140">既存の供給で需要をカバーできるのは 12 日後のみです。</span><span class="sxs-lookup"><span data-stu-id="86e92-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="86e92-141">ただし、遅延許容範囲は 10 日です。</span><span class="sxs-lookup"><span data-stu-id="86e92-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="86e92-142">したがって、マスター プランを実行すると、数量が 10 の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="86e92-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="86e92-143">例 3</span><span class="sxs-lookup"><span data-stu-id="86e92-143">Example 3</span></span>

<span data-ttu-id="86e92-144">製品のコンフィギュレーションは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="86e92-144">A product has the following configuration:</span></span>

- <span data-ttu-id="86e92-145">**リード タイム:** *10*</span><span class="sxs-lookup"><span data-stu-id="86e92-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="86e92-146">**マイナス在庫日数:** *2*</span><span class="sxs-lookup"><span data-stu-id="86e92-146">**Negative days:** *2*</span></span>

<span data-ttu-id="86e92-147">次の供給と需要は製品に対して存在します。</span><span class="sxs-lookup"><span data-stu-id="86e92-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="86e92-148">**11 日以内の需要:** 数量が 10 の販売注文</span><span class="sxs-lookup"><span data-stu-id="86e92-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="86e92-149">**14 日以内の供給:** 数量が 10 の発注書</span><span class="sxs-lookup"><span data-stu-id="86e92-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="86e92-150">既存の供給で需要をカバーできるのは 3 日後のみです。</span><span class="sxs-lookup"><span data-stu-id="86e92-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="86e92-151">ただし、遅延許容範囲は 2 日です。</span><span class="sxs-lookup"><span data-stu-id="86e92-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="86e92-152">(この場合、遅延許容範囲にはマイナス在庫日数 2 日のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="86e92-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="86e92-153">需要の日付は製品のリード タイムの後なので含まれません。) したがって、マスター プランを実行すると、数量が 10 の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="86e92-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
