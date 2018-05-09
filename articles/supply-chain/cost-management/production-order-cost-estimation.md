---
title: "原価見積を行う製造オーダー。"
description: "この記事は、生産原価見積に関する情報を提供します。 生産原価見積では、計画製造オーダー数量で品目を製造する場合の予測される材料消費および能力消費の原価が示されます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fe938a0b728205da56aa006583c6be7a44537ff4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="9e559-104">原価見積を行う製造オーダー。</span><span class="sxs-lookup"><span data-stu-id="9e559-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e559-105">この記事は、生産原価見積に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9e559-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="9e559-106">生産原価見積では、計画製造オーダー数量で品目を製造する場合の予測される材料消費および能力消費の原価が示されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="9e559-107">製造オーダーを作成したあと、生産原価を見積もる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e559-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="9e559-108">その目的は、品目消費と工順消費を生産プロセスに対して見積もることです。これらの見積によって、以降のスケジューリングや生産プロセスの基盤を築くことができます。</span><span class="sxs-lookup"><span data-stu-id="9e559-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="9e559-109">製造原価見積</span><span class="sxs-lookup"><span data-stu-id="9e559-109">Production cost estimation</span></span>
<span data-ttu-id="9e559-110">生産原価の見積は、次の情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9e559-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="9e559-111">製造オーダーの数量</span><span class="sxs-lookup"><span data-stu-id="9e559-111">The quantity on the production order</span></span>
-   <span data-ttu-id="9e559-112">製造部品表 (BOM) のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="9e559-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="9e559-113">製造工順の工順工程</span><span class="sxs-lookup"><span data-stu-id="9e559-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="9e559-114">コンポーネントと工程に適用される間接原価</span><span class="sxs-lookup"><span data-stu-id="9e559-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="9e559-115">計算日付においての現在有効な原価データ</span><span class="sxs-lookup"><span data-stu-id="9e559-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="9e559-116">製造 BOM にファントム品目がある場合、ファントムのコンポーネントと工順工程が計算に反映されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="9e559-117">見積タスクを使用すると、見積原価を再計算して更新情報を反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="9e559-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="9e559-118">たとえば、更新情報には、製造オーダーの数量、製造 BOM のコンポーネント、生産工順における工順工程、これらのコンポーネントと工程に適用される間接費、または再計算日の時点での実績原価データの変更などがあります。</span><span class="sxs-lookup"><span data-stu-id="9e559-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="9e559-119">見積原価の計算では、原価に利幅を追加するアプローチに基づいて、製造品目の販売価格も提案されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="9e559-120">オプションで、製造オーダーにリンクされた別の製造オーダーを反映した参照オーダーに見積原価計算を適用できます。</span><span class="sxs-lookup"><span data-stu-id="9e559-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="9e559-121">見積原価の表示</span><span class="sxs-lookup"><span data-stu-id="9e559-121">View the estimated costs</span></span>
<span data-ttu-id="9e559-122">見積を実行した後、**価格計算**ページで結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9e559-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="9e559-123">見積では、次の値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="9e559-124">**生産原価**– 生産原価は、見積のトップラインです。</span><span class="sxs-lookup"><span data-stu-id="9e559-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="9e559-125">製造オーダーを実行するすべての原価と、生産の販売価格合計が示されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="9e559-126">見積のすべての原価明細行の合計になります。</span><span class="sxs-lookup"><span data-stu-id="9e559-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="9e559-127">**工順またはリソース コスト** – 工順またはリソース コストとは、生産工程の原価です。</span><span class="sxs-lookup"><span data-stu-id="9e559-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="9e559-128">ここには、段取り時間、実行時間、間接費などの要素の原価が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e559-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="9e559-129">**原材料の原価** – 原材料の原価は、品目の製造に必要な部品表 (BOM) コンポーネントの原価と価格です。</span><span class="sxs-lookup"><span data-stu-id="9e559-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="9e559-130">これらの原価は事前に作成され、システムに入力されています。</span><span class="sxs-lookup"><span data-stu-id="9e559-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="9e559-131">原価見積のその他の用途</span><span class="sxs-lookup"><span data-stu-id="9e559-131">Other uses of cost estimation</span></span>
<span data-ttu-id="9e559-132">原価見積では、次の情報も提供されます。</span><span class="sxs-lookup"><span data-stu-id="9e559-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="9e559-133">有効な価格見積書</span><span class="sxs-lookup"><span data-stu-id="9e559-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="9e559-134">注文の収益性の見積</span><span class="sxs-lookup"><span data-stu-id="9e559-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="9e559-135">原材料消費の見積</span><span class="sxs-lookup"><span data-stu-id="9e559-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="9e559-136">前の生産からの原価情報の比較</span><span class="sxs-lookup"><span data-stu-id="9e559-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="9e559-137">予算と予測情報</span><span class="sxs-lookup"><span data-stu-id="9e559-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="9e559-138">特定の原価を管理するために必要な生産サイズの見積</span><span class="sxs-lookup"><span data-stu-id="9e559-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





