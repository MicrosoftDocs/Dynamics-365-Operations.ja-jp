---
title: 生産計画
description: このトピックでは、生産の計画について説明し、計画の最適化を使用して計画製造オーダーを変更する方法について説明します。
author: ChristianRytt
ms.date: 12/15/2020
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
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839226"
---
# <a name="production-planning"></a><span data-ttu-id="3c293-103">生産計画</span><span class="sxs-lookup"><span data-stu-id="3c293-103">Production planning</span></span>

<span data-ttu-id="3c293-104">計画の最適化では、複数の生産シナリオがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="3c293-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="3c293-105">組み込みの既存のマスター プラン エンジンから移行する場合は、動作の変更を確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="3c293-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="3c293-106">次のビデオでは、このトピックで説明されている概念のいくつかを簡単に紹介しています: [Dynamics 365 Supply Chain Management: 計画最適化の機能拡張](https://youtu.be/u1pcmZuZBTw)。</span><span class="sxs-lookup"><span data-stu-id="3c293-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="3c293-107">システムでこの機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="3c293-107">Turn on this feature for your system</span></span>

<span data-ttu-id="3c293-108">このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*計画最適化に使用する計画製造オーダー* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="3c293-108">If your system doesn't already include the features described in this topic, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Planned production orders for Planning Optimization* feature.</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="3c293-109">計画製造オーダー</span><span class="sxs-lookup"><span data-stu-id="3c293-109">Planned production orders</span></span>

<span data-ttu-id="3c293-110">要求を満たすためにマスター プランで計画オーダーを作成する場合、注文タイプは **計画オーダー タイプ** フィールド の値によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-110">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="3c293-111">**計画オーダー タイプ** フィールドが *生産* に設定されている場合は、計画製造オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-111">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="3c293-112">これらの計画製造オーダーには、関連する生産設定からの有効な部品表 (BOM) とルート ID に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c293-112">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="3c293-113">BOM の要件</span><span class="sxs-lookup"><span data-stu-id="3c293-113">Requirements from BOMs</span></span>

<span data-ttu-id="3c293-114">BOM 情報はマスター プランの際に受け入れされます。</span><span class="sxs-lookup"><span data-stu-id="3c293-114">BOM information is honored during master planning.</span></span> <span data-ttu-id="3c293-115">この計画の生産物には、関連する生産必要量をカバーする材料供給が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c293-115">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="3c293-116">マスター プランの間に、生産に必要な材料を決定するために現在の有効な BOM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-116">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="3c293-117">この手順は、必要な製造オーダーに関連する BOM 構造のすべてのレベルから実行されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-117">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="3c293-118">材料の要件は、使用可能な手持在庫、既存の注文供給、承認済の計画オーダーを使用して満たされます。</span><span class="sxs-lookup"><span data-stu-id="3c293-118">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="3c293-119">その他の材料が必要な場合は、需要を満たす計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-119">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="3c293-120">固定中のスケジューリング</span><span class="sxs-lookup"><span data-stu-id="3c293-120">Scheduling during firming</span></span>

<span data-ttu-id="3c293-121">計画製造オーダーには、生産のスケジューリングに必要なルート ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c293-121">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="3c293-122">ただし、計画オーダーの計画の実行時のスケジューリングのサポートは保留中です。</span><span class="sxs-lookup"><span data-stu-id="3c293-122">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="3c293-123">ルート ID は、固定中に計画製造オーダーをスケジュールするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-123">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="3c293-124">したがって、計画製造オーダーのリード タイムは、次の説明に従って、計画製造オーダーから生成される関連するスケジュール済の製造オーダーのリード タイムと異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c293-124">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="3c293-125">**計画製造オーダー** - リード タイムは、リリースされた製品の静的リード タイムに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-125">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="3c293-126">**固定された製造オーダー** - リード タイムは、ルート情報や関連するリソース制約を使用するスケジューリングに基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="3c293-126">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="3c293-127">予想される機能の利用可能性の詳細については、[計画の最適化解析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c293-127">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="3c293-128">計画の最適化にまだ使用できない生産機能に依存する場合は、組み込みのマスター プラン エンジンを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c293-128">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="3c293-129">例外は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3c293-129">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="3c293-130">遅延</span><span class="sxs-lookup"><span data-stu-id="3c293-130">Delays</span></span>

<span data-ttu-id="3c293-131">必要な材料のリード タイムが今日の日付から材料要求日の間の期間よりも長い場合、必要な材料と関連する製造オーダーの計画オーダーは遅延します。</span><span class="sxs-lookup"><span data-stu-id="3c293-131">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="3c293-132">計画オーダーの場合は、リリースされた製品のリード タイムに基づいて遅延 (日数) が計算されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-132">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="3c293-133">遅延情報は、BOM 構造のすべてのレベルに反映されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-133">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="3c293-134">したがって、遅延した原材料の影響を顧客の販売注文までのすべての方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="3c293-134">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="3c293-135">計画オーダーの修正</span><span class="sxs-lookup"><span data-stu-id="3c293-135">Modifying planned orders</span></span>

<span data-ttu-id="3c293-136">計画オーダーの情報を変更すると、"計画オーダーに対する手動変更の影響は、次回のマスター プランの実行までプランの残りの部分に反映されないので注意してください" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-136">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="3c293-137">計画オーダーの情報を変更し、関連する材料要求に対する影響を確認する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3c293-137">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="3c293-138">計画オーダーの更新。</span><span class="sxs-lookup"><span data-stu-id="3c293-138">Update the planned order.</span></span>
2. <span data-ttu-id="3c293-139">計画オーダーの承認。</span><span class="sxs-lookup"><span data-stu-id="3c293-139">Approve the planned order.</span></span>
3. <span data-ttu-id="3c293-140">マスター プランの実行。</span><span class="sxs-lookup"><span data-stu-id="3c293-140">Run master planning.</span></span>

<span data-ttu-id="3c293-141">マスター プランを実行する際、計画製造オーダーを含める場合はフィルタを使用しません。</span><span class="sxs-lookup"><span data-stu-id="3c293-141">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="3c293-142">詳細については、このトピックの後にある [フィルタ―](#filters) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c293-142">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="3c293-143">計画オーダーの出荷日が後の日付に変更された場合、需要は新しい計画オーダーに対してペギングされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c293-143">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="3c293-144">この動作は、新しい供給日によってペギングされた需要に遅延が発生するが、リード タイムの設定に従って遅延を回避できる場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="3c293-144">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="3c293-145">展開ページ</span><span class="sxs-lookup"><span data-stu-id="3c293-145">Explosion page</span></span>

<span data-ttu-id="3c293-146">**展開** ページを使用して、特定の製造オーダーまたは計画製造オーダー、関連する補充、ペギング情報に必要な需要を分析できます。</span><span class="sxs-lookup"><span data-stu-id="3c293-146">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="3c293-147">**展開** ページの情報は、マスター プラン時に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3c293-147">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="3c293-148">**展開** ページから情報を直接更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="3c293-148">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="3c293-149">フィルター</span><span class="sxs-lookup"><span data-stu-id="3c293-149">Filters</span></span>

<span data-ttu-id="3c293-150">生産を含む計画シナリオの場合は、フィルタ処理されたマスター プランの実行を回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3c293-150">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="3c293-151">計画の最適化に必要な情報が正しい結果の計算に必要な情報を確実に提供するには、計画オーダーの BOM 構造全体に製品に関連する製品を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c293-151">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="3c293-152">組み込みのマスター プラン エンジンを使用する場合、依存する子品目が自動的に検出され、マスター プランの実行に含まれますが、計画の最適化ではこのアクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="3c293-152">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="3c293-153">たとえば、製品 A の BOM 構造の一つの締めを使用して製品 B を生産した場合は、製品 A と製品 B の BOM 構造のすべての製品をフィルターに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c293-153">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="3c293-154">すべての製品がフィルターに含まれる保証は非常に複雑になる可能性があるから、製造オーダーが含まれる場合は、フィルタ処理されたマスター プランの実行を回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3c293-154">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]