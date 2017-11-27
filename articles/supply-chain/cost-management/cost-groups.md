---
title: "原価グループ"
description: "原価グループは、原材料、労務、および間接費に対する原価貢献度などのように、製品の計算された原価での原価貢献度を区分および分析するための基礎を提供します。 原価内訳、原価分解、原価分類など、製造環境には原価グループ区分の同義語がいくつかあります。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f44099c2ce30d917838733af072721dd79148d27
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="cost-groups"></a><span data-ttu-id="9d1b8-104">原価グループ</span><span class="sxs-lookup"><span data-stu-id="9d1b8-104">Cost groups</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9d1b8-105">原価グループは、原材料、労務、および間接費に対する原価貢献度などのように、製品の計算された原価での原価貢献度を区分および分析するための基礎を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-105">Cost groups provide the basis for segmenting and analyzing cost contributions in a manufactured item’s calculated cost, such as the cost contributions for material, labor, and overhead.</span></span> <span data-ttu-id="9d1b8-106">原価内訳、原価分解、原価分類など、製造環境には原価グループ区分の同義語がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-106">Cost group segmentation has several synonyms within manufacturing environments, such as cost breakdown, cost decomposition, or cost classification.</span></span> 

<span data-ttu-id="9d1b8-107">原価内訳、原価分解、原価分類など、製造環境には原価グループ区分の同義語がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-107">Cost group segmentation has several synonyms within manufacturing environments, such as cost breakdown, cost decomposition, or cost classification.</span></span> <span data-ttu-id="9d1b8-108">原価グループ区分には、いくつかの目的があります。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-108">Cost group segmentation can serve several purposes.</span></span> <span data-ttu-id="9d1b8-109">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-109">Here are some examples:</span></span>

-   <span data-ttu-id="9d1b8-110">缶詰製品の原料と容器材料などのように、項目に割り当てられた原価グループに基づいて、異なる種類の原材料の原価を区分できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-110">It can segment costs for different types of material, such as ingredients and packaging material for a canned goods product, based on the cost groups that are assigned to items.</span></span>
-   <span data-ttu-id="9d1b8-111">異なる種類の労務や機械装置などのように、運営リソースおよび工程に関係する原価カテゴリに割り当てられている原価グループに基づいて、異なる種類の運営リソースの原価を区分できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-111">It can segment costs for different types of operations resources, such as different types of labor or machines, based on the cost groups that are assigned to cost categories that are related to operations resources and routing operations.</span></span>
-   <span data-ttu-id="9d1b8-112">工程に関係する原価カテゴリに割り当てられている原価グループに基づいて、工程の段取り時間および実行時間に対する原価を区分できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-112">It can segment costs for setup time and run time in routing operations, based on the cost groups that are assigned to cost categories that are related to the routing operations.</span></span>
-   <span data-ttu-id="9d1b8-113">労務関連の間接費や機械装置関連の間接費などのように、原価計算表設定で間接原価に割り当てられている原価グループに基づいて、異なる種類の間接費の原価を区分できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-113">It can segment costs for different types of overhead, such as labor-related and machine-related overhead, based on cost groups that are assigned to indirect costs in the costing sheet setup.</span></span>
-   <span data-ttu-id="9d1b8-114">原価計算表の設定でさまざまなタイプの製造間接費を計算するための基準として機能します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-114">It can act as the basis for calculating various types of manufacturing overhead in the costing sheet setup.</span></span> <span data-ttu-id="9d1b8-115">この間接費には、運営リソース、または設定時間および実行時間についての工順情報に関連する異なるタイプの間接費を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-115">This overhead can include different types of overhead that are related to routing information about operations resources, or information about setup time and run time.</span></span> <span data-ttu-id="9d1b8-116">また、製造間接費は、コンポーネント原材料の原価貢献度に関係し、工順情報の必要性を排除するリーン生産方式の理念を反映する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-116">Manufacturing overhead can also be related to cost contributions of component material, reflecting a lean manufacturing philosophy that eliminates the need for routing information.</span></span>

<span data-ttu-id="9d1b8-117">原価グループ区分は、標準原価または予定原価のどちらが基になっていても、製造品目の算出原価に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-117">Cost group segmentation applies to a manufactured item’s calculated cost, regardless of whether that cost was based on standard costs or planned costs.</span></span> <span data-ttu-id="9d1b8-118">**集計**ページに、原価グループ別、レベル別、または原価グループとレベルの両方でこの区分を表示します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-118">The **Summary** page displays this segmentation by cost group, by level, or by both cost group and level.</span></span> 

<span data-ttu-id="9d1b8-119">このように製品構造の複数のレベルについて原価グループ区分を維持する機能は、*分解*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-119">The ability to retain cost group segmentation across multiple levels in a product structure is known as *splitting*.</span></span> <span data-ttu-id="9d1b8-120">分解は、標準原価在庫モデルを使用する製造品目に対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-120">Splitting applies only to manufactured items that use a standard cost inventory model.</span></span> <span data-ttu-id="9d1b8-121">分解を行わない場合、製造されるコンポーネントの原価は、原材料の原価貢献度として扱われます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-121">If splitting isn't used, the cost of a manufactured component is treated as a material cost contribution.</span></span> <span data-ttu-id="9d1b8-122">補助元帳による原価内訳の在庫パラメータが、標準原価計算で複数レベルについて原価グループ区分が維持されることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-122">The inventory parameter for cost breakdown by subledger indicates that cost group segmentation will be retained across multiple levels in standard cost calculations.</span></span> <span data-ttu-id="9d1b8-123">これに対し、レベルを指定しないポリシーは、原価グループ区分が単一レベルの計算にのみ適用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-123">By contrast, if a policy has no levels, cost group segmentation applies only to a single-level calculation.</span></span> <span data-ttu-id="9d1b8-124">たとえば、**原価グループによる原価ロールアップ** ページでは、標準原価品目について、複数レベルの原価グループ区分が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-124">For example, the **Cost rollup by cost group** page displays the cost group segmentation across multiple levels for standard cost items.</span></span> 

<span data-ttu-id="9d1b8-125">原価グループ区分は、標準原価品目の差額にも適用できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-125">Cost group segmentation can also apply to variances for a standard cost item.</span></span> <span data-ttu-id="9d1b8-126">2 番目の在庫パラメータは、差額を原価グループで識別するか、または集計のみを行うかを定義します。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-126">A second inventory parameter defines whether variances are identified by cost group or just summarized.</span></span> 

<span data-ttu-id="9d1b8-127">原価グループには、補助的な区分として、原価グループ タイプおよび動作を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-127">A cost group can be assigned a cost group type and a behavior for supplemental segmentation purposes.</span></span>

-   <span data-ttu-id="9d1b8-128">**原価グループ タイプ** − 各原価グループには原価グループタイプを割り当てて、原価グループが直接材料、直接製造、直接外部委託に適用されることを示す、または間接または未定義として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-128">**Cost group type** − Each cost group must be assigned a cost group type to indicate that the cost group applies to direct material, direct manufacturing, or direct outsourcing, or to designate it as indirect or undefined.</span></span> <span data-ttu-id="9d1b8-129">直接材料として指定した原価グループは、品目に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-129">A cost group that is designated as direct material can be assigned to items.</span></span> <span data-ttu-id="9d1b8-130">直接製造原価グループは、原価カテゴリに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-130">A direct manufacturing cost group can be assigned to cost categories.</span></span> <span data-ttu-id="9d1b8-131">直接外部委託のコスト グループは、サービス購買に関連付けられたコストを外注活動に分類できる、製品タイプのサービスに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-131">A direct outsourcing cost group can be assigned to a product type of service, so that you can classify costs that are associated with the service purchase to subcontracting activities.</span></span> <span data-ttu-id="9d1b8-132">間接原価グループは、割増金またはレートの間接原価に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-132">An indirect cost group can be assigned to indirect costs for surcharges or rates.</span></span> <span data-ttu-id="9d1b8-133">未定義として指定した原価グループは、品目、原価カテゴリ、または間接原価に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-133">A cost group that is designated as undefined can be assigned to items, cost categories, or indirect costs.</span></span> <span data-ttu-id="9d1b8-134">原価グループ タイプの割り当ては、いくつかの目的に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-134">The assignment of a cost group type serves several purposes.</span></span> <span data-ttu-id="9d1b8-135">1 つ目の目的は、原価グループを割り当て、適用可能な原価グループのリストを表示させる機能を制限することです。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-135">First, it constrains the ability to assign a cost group and to view a list of applicable cost groups.</span></span> <span data-ttu-id="9d1b8-136">2 つ目の目的は、レポートに補助区分を使用できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-136">Second, it provides supplemental segmentation for reporting purposes.</span></span> <span data-ttu-id="9d1b8-137">3 つ目の目的は、差異に対する勘定科目の割り当てに使用することです。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-137">Third, it can be used to assign ledger accounts for variances.</span></span>
-   <span data-ttu-id="9d1b8-138">**動作** − 各原価グループには、オプションで動作を割り当て、原価グループが固定費または変動費に適用されることを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-138">**Behavior** − Each cost group can optionally be assigned a behavior to indicate that the cost group applies to fixed costs or variable costs.</span></span> <span data-ttu-id="9d1b8-139">動作の値が NULL の原価グループは、変動費として処理されます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-139">A cost group that has a null value for behavior is treated as a variable cost.</span></span> <span data-ttu-id="9d1b8-140">動作の割り当ては、レポート目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-140">The assignment of a behavior serves only a reporting purpose.</span></span> <span data-ttu-id="9d1b8-141">たとえば、原価計算表および**原価グループによる原価ロールアップ** ページでは、固定費および変動費という区分付けて原価を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-141">For example, costs can be displayed with segmentation of fixed and variable costs on the costing sheet and on the **Cost rollup by cost group** page.</span></span> <span data-ttu-id="9d1b8-142">各原価グループに利益設定の割合を割り当てた場合は、コスト プラス マークアップのアプローチに基づいた推奨販売価格が部品表 (BOM) 計算に使用できます。</span><span class="sxs-lookup"><span data-stu-id="9d1b8-142">If you assign a profit setting percentage to each cost group, the bill of materials (BOM) calculation provides a suggested sales price, based on a cost-plus-markup approach.</span></span>





