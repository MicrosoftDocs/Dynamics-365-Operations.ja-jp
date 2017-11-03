---
title: "生産工順で使用される原価カテゴリ"
description: "この記事は、工順を使用する製造環境に適用される原価カテゴリについて説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 53e038183a10b8732a9a5e0f25aac440c224400e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="cost-categories-used-in-production-routing"></a><span data-ttu-id="bf3c9-103">生産工順で使用される原価カテゴリ</span><span class="sxs-lookup"><span data-stu-id="bf3c9-103">Cost categories used in production routing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf3c9-104">この記事は、工順を使用する製造環境に適用される原価カテゴリについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-104">This article provides information about cost categories that apply to manufacturing environments that use routing.</span></span>

<span data-ttu-id="bf3c9-105">原価カテゴリは、工順を使用する製造環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-105">Cost categories apply to manufacturing environments that use routing.</span></span> <span data-ttu-id="bf3c9-106">これらは、製造品目の算出原価における時間原価の定義と原価貢献度の区分を行うことを目的として、運営リソースと工順工程に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-106">They are assigned to operations resources and routing operations to define hourly costs and to segment cost contributions in a manufactured item’s calculated costs.</span></span> <span data-ttu-id="bf3c9-107">原価カテゴリに割り当てられた原価グループは、運営リソースと活動タイプ (段取り時間や実行時間など) に基づいて製造原価の貢献度を分類します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-107">The cost groups that are assigned to cost categories classify manufacturing cost contributions, based on the operation resources and the type of activity, such as setup time and run time.</span></span> <span data-ttu-id="bf3c9-108">原価グループの割当の特異性は、工順情報に基づいて製造間接費を計算できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-108">The specificity of cost group assignments enables manufacturing overhead to be calculated based on routing information.</span></span> 

<span data-ttu-id="bf3c9-109">**メモ:** 製造環境の中では、原価カテゴリは複数の他の名前で呼ばれます (労務率コードや機械率コードなど)。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-109">**Note:** In manufacturing environments, cost categories are known by several other names, such as labor rate codes or machine rate codes.</span></span> 

<span data-ttu-id="bf3c9-110">各原価カテゴリには、関連付けられた原価レコードと割り当てられた原価グループがあります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-110">Each cost category has associated cost records and an assigned cost group.</span></span> <span data-ttu-id="bf3c9-111">異なる生産目的には、異なる原価カテゴリが必要です。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-111">Different cost categories are required for different production purposes.</span></span>

-   <span data-ttu-id="bf3c9-112">運営リソースに基づいて異なる時間原価を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-112">Assign different hourly costs, depending on the operations resource.</span></span> <span data-ttu-id="bf3c9-113">たとえば、さまざまなタイプの労務スキル、機械、生産セルによって原価が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-113">For example, the costs can differ for various types of labor skills, machines, or manufacturing cells.</span></span>
-   <span data-ttu-id="bf3c9-114">工順工程に関連付けられた段取り時間または実行時間に対して、異なる時間原価を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-114">Assign different hourly costs for the setup time or run time that is associated with a routing operation.</span></span>
-   <span data-ttu-id="bf3c9-115">時間原価の代わりに、出来高数量に基づいて原価を運営リソースに割り当てます (労務費を支払うための単価など)。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-115">Assign operations resource costs based on the output quantity instead of hourly costs, such as the piece rates for paying labor.</span></span>
-   <span data-ttu-id="bf3c9-116">原価貢献度の原価グループの区分を、製造品目の算出原価に提供します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-116">Provide cost group segmentation of cost contributions to a manufactured item’s calculated cost.</span></span> <span data-ttu-id="bf3c9-117">たとえば、労務費と機械費を区分できます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-117">For example, you can segment of labor and machine costs.</span></span>
-   <span data-ttu-id="bf3c9-118">労務と機械に関連する間接費や段取り時間と実行時間に関連する間接費の式などの、間接費計算式の基準となる原価グループを用意します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-118">Provide the cost group basis for overhead calculation formulas, such as formulas for labor-related and machine-related overhead, or overhead that is related to setup and run time.</span></span>

<span data-ttu-id="bf3c9-119">原価カテゴリは、工順工程の段取り時間、処理時間、および数量に対して割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-119">A cost category can be assigned to the setup time, the process time, and the quantity for a routing operation.</span></span> <span data-ttu-id="bf3c9-120">たとえば、原価または原価グループの区分が、たとえば段取り時間と処理時間で異なる場合は、異なる原価カテゴリを定義して段取り時間と処理時間に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-120">When, for example, costs or cost group segmentation differs between the setup time and the process time, different cost categories should be defined and assigned to the setup time and the process time.</span></span> <span data-ttu-id="bf3c9-121">段取り時間、処理時間、および数量に対する原価カテゴリの選択的使用は、工程に割り当てられた工順グループによって決まります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-121">The selective use of cost categories for setup time, process time, and quantity is determined by the route group that is assigned to an operation.</span></span> <span data-ttu-id="bf3c9-122">時間と数量に対する原価カテゴリの割り当ては、[**生産管理パラメーター**] ページで定義された全社的なポリシーによって要求することができます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-122">The assignment of cost categories to time and quantity can be mandated by company-wide policies that are defined on the **Production control parameters** page.</span></span> 

<span data-ttu-id="bf3c9-123">各原価カテゴリには、原価バージョンの原価レコードの定義に基づいて関連付けられた原価があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-123">Each cost category has associated costs that are based on the definition of cost records in a costing version.</span></span> <span data-ttu-id="bf3c9-124">特定の原価バージョンとサイト用の原価レコードを定義するには、[**原価カテゴリ価格**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-124">Use the **Cost category price** page to define the cost records for a specified costing version and site.</span></span> <span data-ttu-id="bf3c9-125">原価カテゴリの原価レコードが最初に入力されると、ステータスは [**保留中**] であり、発効日が設定されています。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-125">When the cost record for a cost category is first entered, it has a status of **Pending** and an intended effective date.</span></span> <span data-ttu-id="bf3c9-126">原価レコードを有効にすると、ステータスは [**現在有効**] に更新され、発効日は有効化した日に更新されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-126">When you activate the cost record, the status is updated to **Current active**, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="bf3c9-127">各原価レコードで、反映されるサイト、発効日、またはステータスが異なっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-127">Different cost records might reflect different sites, effective dates, or statuses.</span></span> <span data-ttu-id="bf3c9-128">未来または過去の日付での部品表 (BOM) 計算では、関連する有効日を持つ原価レコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-128">Bills of materials (BOM) calculations for a future or historical date use cost records that have the relevant effective date.</span></span> <span data-ttu-id="bf3c9-129">現在有効な原価レコードは、製造オーダー原価の見積と、製造オーダーに対して報告された時間の評価を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-129">The current active cost record will be used to estimate production order costs and to value reported time against a production order.</span></span> 

<span data-ttu-id="bf3c9-130">原価カテゴリの原価レコードは、サイト固有にすることも、全社的にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-130">The cost record for a cost category can be site-specific or company-wide.</span></span> <span data-ttu-id="bf3c9-131">原価レコードをサイト固有にするには、サイトを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-131">To make a cost record site-specific, assign a site to it.</span></span> <span data-ttu-id="bf3c9-132">それ以外の場合、空白の値は、原価レコードが会社内の全サイトに適用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-132">Otherwise, a blank value indicates that the cost record applies to all sites in the company.</span></span> <span data-ttu-id="bf3c9-133">原価はサイトごとに異なる場合があるため、たとえば原価レコードをサイト固有として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-133">Because costs can differ between sites, for example, the cost records must be defined as site-specific.</span></span> 

<span data-ttu-id="bf3c9-134">工順工程は、通常は運営リソースまたはマスター工程に割り当てられた原価カテゴリを継承します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-134">A routing operation generally inherits the cost categories that are assigned to the operations resource or master operation.</span></span> <span data-ttu-id="bf3c9-135">製造オーダーを作成すると、生産工順内の工順工程は、選択された工順バージョンを反映します。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-135">When a production order is created, the routing operations in the production route reflect the selected route version.</span></span> <span data-ttu-id="bf3c9-136">生産工順内の工程に割り当てられた原価カテゴリは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-136">You can override the cost categories that are assigned to the operations in the production route.</span></span> 

<span data-ttu-id="bf3c9-137">生産作業によっては、プロジェクト時間の見積と報告に適用できます。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-137">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="bf3c9-138">この場合、生産とプロジェクトのために原価カテゴリが必要です。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-138">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="bf3c9-139">原価カテゴリにプロジェクトでの使用を示すフラグを設定する場合は、プロジェクト関連の追加情報を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c9-139">You must define additional project-related information when a cost category is flagged for use in projects.</span></span>




