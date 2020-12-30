---
title: 部分的な場所の循環棚卸
description: 循環棚卸計画は、実際のカウント操作をガイドします。 ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a541818a72f5c24db8784071f447c83a2aa4edfd
ms.sourcegitcommit: 95f90ac3f248716abdab16d5de6ccbf059616e4b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2020
ms.locfileid: "4666749"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="cba58-104">部分的な場所の循環棚卸</span><span class="sxs-lookup"><span data-stu-id="cba58-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cba58-105">循環棚卸計画は、実際のカウント操作をガイドします。</span><span class="sxs-lookup"><span data-stu-id="cba58-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="cba58-106">ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="cba58-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="cba58-107">循環棚卸計画を使用して棚卸作業を作成することにより、実際のカウント操作を導くことができます。</span><span class="sxs-lookup"><span data-stu-id="cba58-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="cba58-108">ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="cba58-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="cba58-109">特定の製品をフィルター処理することで、倉庫マネージャーはレビュー間接費を削減し、統合ミスを回避し、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="cba58-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="cba58-110">部分的な場所の循環棚卸をコンフィギュレーションする方法</span><span class="sxs-lookup"><span data-stu-id="cba58-110">How to configure partial location cycle counting</span></span>

<span data-ttu-id="cba58-111">倉庫作業プロセスを使用して作業をカウントすると、各作業場所ごとに作業ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="cba58-112">循環棚卸計画を定義する場合、**場所の選択** 検索を使用し、作成する循環棚卸作業を制御します。</span><span class="sxs-lookup"><span data-stu-id="cba58-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="cba58-113">サイクル カウント計画の製品を選択すると、製品と製品バリアント クエリの両方を選択し、何を棚卸するかを絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="cba58-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span>

<span data-ttu-id="cba58-114">**作業テンプレート** をサイクル カウント計画に関連付け、循環棚卸作業の作成方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="cba58-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="cba58-115">カウント操作のための作業テンプレートは、循環棚卸計画から直接参照されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span>

<span data-ttu-id="cba58-116">作業テンプレートの詳細を定義する際には、**作業明細行内訳** オプションを使用して、棚卸作業ラインを品目番号または製品バリアント番号でグループ化する必要があるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cba58-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="cba58-117">この設定は、ある場所の特定の製品に対してのみ手持在庫をカウントする場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="cba58-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="cba58-118">作成された循環棚卸作業ラインには、ここで定義するレベルの情報があり、このレベルに基づいてガイドされたカウント操作が処理されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span>

<span data-ttu-id="cba58-119">**作業明細行内訳** オプションを使用して循環棚卸計画をワークテンプレートに関連付けると、作成された循環棚卸作業に対して **部分的な循環棚卸** フィールドが選択され、複数の循環棚卸作業ラインが、作業テンプレートの定義に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span>

<span data-ttu-id="cba58-120">部分的な循環棚卸作業を処理する前に、循環棚卸の設定の一部として、モバイル デバイスのメニュー項目の、**品目番号を表示する** を少なくとも選択します。</span><span class="sxs-lookup"><span data-stu-id="cba58-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="cba58-121">倉庫マネージャーは、棚卸ライン (品目番号および製品分析コード) に関連する棚卸情報のみを記録するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="cba58-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="cba58-122">他の手持在庫はこのカウント プロセスでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-122">All other on-hand inventory will be ignored for this counting process.</span></span>

<span data-ttu-id="cba58-123">部分的なサイクル数のプロセスでは、特定の場所における手持在庫のすべての品目がカウントされますが、その場所については、**最終サイクルカウント** 日時は更新されません。</span><span class="sxs-lookup"><span data-stu-id="cba58-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location, even though all the items on hand at a given location are counted.</span></span> <span data-ttu-id="cba58-124">部分的なサイクル カウントでは、**サイクル数計画** ページの **サイクルカウントの間 のパラメータの日数** は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="cba58-124">The partial cycle count doesn't consider the parameter **Days between cycle counting** on  the **Cycle count plans** page.</span></span> <span data-ttu-id="cba58-125">循環棚卸では、同じ場所にある複数の品目の同時カウントはサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="cba58-125">Partial cycle count doesn't support simultaneous counting of multiple items at the same location.</span></span> <span data-ttu-id="cba58-126">期間を部分的に計算する機能により、**循環棚卸の処理計画** が実行されたときに、同じ場所が複数回カウントされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cba58-126">Partial cycle count functionality may result in the same location being counted multiple times for an item when **Process cycle counting plan** is run.</span></span> <span data-ttu-id="cba58-127">このような状況を回避するには、**場所の選択** フィールドでフィルタを指定します。</span><span class="sxs-lookup"><span data-stu-id="cba58-127">To avoid that scenario, specify filters in the **Select locations** field.</span></span>

> [!NOTE]
> <span data-ttu-id="cba58-128">部分的なサイクル カウント プロセスを使用する場合、倉庫アプリには **LP または品目の追加** ボタンは用意されていません。</span><span class="sxs-lookup"><span data-stu-id="cba58-128">The warehouse app doesn't provide the **Add LP or item** button when you use the partial cycle count process.</span></span>

## <a name="example"></a><span data-ttu-id="cba58-129">例</span><span class="sxs-lookup"><span data-stu-id="cba58-129">Example</span></span>

<span data-ttu-id="cba58-130">この例では、倉庫 61 では品目番号 A0001 のみをカウントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cba58-130">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1. <span data-ttu-id="cba58-131">循環棚卸用の新しい作業時間テンプレートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-131">A new work template for cycle counting is created.</span></span> <span data-ttu-id="cba58-132">**作業明細行内訳** オプションは、品目番号を使用して棚卸作業明細行をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-132">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="cba58-133">したがって、作成された循環棚卸作業には、品目番号ごとに明細行が提供されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-133">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="cba58-134">製品バリアント番号で明細行をグループ化することもできます。</span><span class="sxs-lookup"><span data-stu-id="cba58-134">You can also group the lines by product variant number.</span></span>
1. <span data-ttu-id="cba58-135">新たに作成された作業テンプレートを参照する新しい循環棚卸計画が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-135">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="cba58-136">循環棚卸計画には、品目番号 A0001 の在庫を保持する倉庫 61 内のすべての場所 (**場所の選択** クエリ) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cba58-136">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="cba58-137">特定の製品の選択は、**循環棚卸製品の選択** セクションで定義されています。</span><span class="sxs-lookup"><span data-stu-id="cba58-137">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
1. <span data-ttu-id="cba58-138">**空の場所** フィールドを **空白を除外する** に設定すると、循環棚卸計画の製品を選択できます。</span><span class="sxs-lookup"><span data-stu-id="cba58-138">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="cba58-139">循環棚卸計画が処理されると、品目番号 A0001 の部分的な循環棚卸作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba58-139">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="cba58-140">実際の棚卸プロセスは、ガイド付き循環棚卸のためのモバイル デバイス メニュー項目を使用することによって実行できます。</span><span class="sxs-lookup"><span data-stu-id="cba58-140">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cba58-141">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cba58-141">Additional resources</span></span>

[<span data-ttu-id="cba58-142">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="cba58-142">Cycle counting</span></span>](cycle-counting.md)
