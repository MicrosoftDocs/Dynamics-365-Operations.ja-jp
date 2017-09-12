---
title: "部分的な場所の循環棚卸"
description: "循環棚卸計画は、実際のカウント操作をガイドします。 ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。"
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: "WHSCycleCountPlan、WHSWorkLineCycleCount、WHSWorkTemplateLineGroup、WHSWorkTemplateTable"
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="c9edd-105">部分的な場所の循環棚卸</span><span class="sxs-lookup"><span data-stu-id="c9edd-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c9edd-106">循環棚卸計画は、実際のカウント操作をガイドします。</span><span class="sxs-lookup"><span data-stu-id="c9edd-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="c9edd-107">ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="c9edd-108">循環棚卸計画を使用して棚卸作業を作成することにより、実際のカウント操作を導くことができます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="c9edd-109">ある特定の場所にあるすべての手持在庫の代わりに、特定の製品と製品の種類のみをカウントするように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="c9edd-110">特定の製品をフィルター処理することで、倉庫マネージャーはレビュー間接費を削減し、統合ミスを回避し、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="c9edd-111">部分的な場所の循環棚卸をコンフィギュレーションする方法</span><span class="sxs-lookup"><span data-stu-id="c9edd-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="c9edd-112">倉庫作業プロセスを使用して作業をカウントすると、各作業場所ごとに作業ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="c9edd-113">循環棚卸計画を定義する場合、[**場所の選択**] 検索を使用し、作成する循環棚卸作業を制御します。</span><span class="sxs-lookup"><span data-stu-id="c9edd-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="c9edd-114">サイクル カウント計画の製品を選択すると、製品と製品バリアント クエリの両方を選択し、何を棚卸するかを絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="c9edd-115">[**作業テンプレート**] をサイクル カウント計画に関連付け、循環棚卸作業の作成方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="c9edd-116">カウント操作のための作業テンプレートは、循環棚卸計画から直接参照されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="c9edd-117">作業テンプレートの詳細を定義する際には、[**作業明細行内訳**] オプションを使用して、棚卸作業ラインを品目番号または製品バリアント番号でグループ化する必要があるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="c9edd-118">この設定は、ある場所の特定の製品に対してのみ手持在庫をカウントする場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="c9edd-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="c9edd-119">作成された循環棚卸作業ラインには、ここで定義するレベルの情報があり、このレベルに基づいてガイドされたカウント操作が処理されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="c9edd-120">[**作業明細行内訳**] オプションを使用して循環棚卸計画をワークテンプレートに関連付けると、作成された循環棚卸作業に対して [**部分的な循環棚卸**] フィールドが選択され、複数の循環棚卸作業ラインが、作業テンプレートの定義に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="c9edd-121">部分的な循環棚卸作業を処理する前に、循環棚卸の設定の一部として、モバイル デバイスのメニュー項目の、[**品目番号を表示する**] を少なくとも選択します。</span><span class="sxs-lookup"><span data-stu-id="c9edd-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="c9edd-122">倉庫マネージャーは、棚卸ライン (品目番号および製品分析コード) に関連する棚卸情報のみを記録するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="c9edd-123">他の手持在庫はこのカウント プロセスでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="c9edd-124">部分的な循環棚卸プロセスでは、[**最後循環棚卸**] 日付/時刻は場所に対しては更新されません。</span><span class="sxs-lookup"><span data-stu-id="c9edd-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="c9edd-125">例</span><span class="sxs-lookup"><span data-stu-id="c9edd-125">Example</span></span>
<span data-ttu-id="c9edd-126">この例では、倉庫 61 では品目番号 A0001 のみをカウントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9edd-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="c9edd-127">循環棚卸用の新しい作業時間テンプレートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="c9edd-128">[**作業明細行内訳**] オプションは、品目番号を使用して棚卸作業明細行をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="c9edd-129">したがって、作成された循環棚卸作業には、品目番号ごとに明細行が提供されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="c9edd-130">製品バリアント番号で明細行をグループ化することもできます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="c9edd-131">新たに作成された作業テンプレートを参照する新しい循環棚卸計画が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="c9edd-132">循環棚卸計画には、品目番号 A0001 の在庫を保持する倉庫 61 内のすべての場所 (**場所の選択** クエリ) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="c9edd-133">特定の製品の選択は、[**循環棚卸製品の選択**] セクションで定義されています。</span><span class="sxs-lookup"><span data-stu-id="c9edd-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="c9edd-134">[**空の場所**] フィールドを [**空白を除外する**] に設定すると、循環棚卸計画の製品を選択できます。循環棚卸計画が処理されると、品目番号 A0001 の部分的な循環棚卸作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="c9edd-135">実際の棚卸プロセスは、ガイド付き循環棚卸のためのモバイル デバイス メニュー項目を使用することによって実行できます。</span><span class="sxs-lookup"><span data-stu-id="c9edd-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="c9edd-136">参照</span><span class="sxs-lookup"><span data-stu-id="c9edd-136">See also</span></span>
--------

[<span data-ttu-id="c9edd-137">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="c9edd-137">Cycle counting</span></span>](cycle-counting.md)


