---
title: "原価要素分析コード"
description: "原価計算のコアの柱の 1 つとして、原価要素分析コードは、分類または原価がどこに流れているのかを追跡するために使用されます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00a09120116183785d96ed1e18c577d5430fa16b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="0115b-103">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="0115b-103">Cost element dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0115b-104">原価計算のコアの柱の 1 つとして、原価要素分析コードは、分類または原価がどこに流れているのかを追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0115b-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="0115b-105">要素原価は、勘定科目表で関連する品目原価に対応します。</span><span class="sxs-lookup"><span data-stu-id="0115b-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="0115b-106">基本的には、原価が流れる業務の最下位レベルにある任意の要素のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="0115b-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="0115b-107">概念としての原価要素は、勘定科目からすべての原価関連リソースに及びます。</span><span class="sxs-lookup"><span data-stu-id="0115b-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="0115b-108">現在、原価会計は勘定科目をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0115b-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="0115b-109">2 つのタイプの原価要素</span><span class="sxs-lookup"><span data-stu-id="0115b-109">Two types of cost elements</span></span>
<span data-ttu-id="0115b-110">原価要素の 2 つのタイプがあります: 主要原価要素と副次原価要素。</span><span class="sxs-lookup"><span data-stu-id="0115b-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="0115b-111">次の表では、2 つのタイプの差異について説明します。</span><span class="sxs-lookup"><span data-stu-id="0115b-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0115b-112"><strong>主要原価要素</strong></span><span class="sxs-lookup"><span data-stu-id="0115b-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="0115b-113"><strong>副次原価要素</strong></span><span class="sxs-lookup"><span data-stu-id="0115b-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0115b-114">主要原価要素は、財務会計から原価計算までの原価の流れを表します。</span><span class="sxs-lookup"><span data-stu-id="0115b-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="0115b-115">原価要素構造は、原価要素が主勘定に対応できる総勘定元帳で損益勘定構造に対応します。</span><span class="sxs-lookup"><span data-stu-id="0115b-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="0115b-116">業務上のニーズに応じて、すべての主勘定が原価要素として表されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="0115b-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="0115b-117">次の主要原価要素の例があります:</span><span class="sxs-lookup"><span data-stu-id="0115b-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="0115b-118">売却済商品の原価 (COGs)</span><span class="sxs-lookup"><span data-stu-id="0115b-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="0115b-119">間接材料原価</span><span class="sxs-lookup"><span data-stu-id="0115b-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="0115b-120">人件費</span><span class="sxs-lookup"><span data-stu-id="0115b-120">Personnel costs</span></span></li>
<li><span data-ttu-id="0115b-121">エネルギー原価</span><span class="sxs-lookup"><span data-stu-id="0115b-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="0115b-122">副次原価要素は、原価計算でのみ作成および使用されるため、内部の原価の流れを表します。</span><span class="sxs-lookup"><span data-stu-id="0115b-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="0115b-123">それらを使用して原価のソースが追跡できるセキュリティ保護をします。</span><span class="sxs-lookup"><span data-stu-id="0115b-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="0115b-124">これらの原価要素は原価配賦および間接費計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0115b-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="0115b-125">次の副次原価要素の例があります:</span><span class="sxs-lookup"><span data-stu-id="0115b-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="0115b-126">生産原価</span><span class="sxs-lookup"><span data-stu-id="0115b-126">Production costs</span></span></li>
<li><span data-ttu-id="0115b-127">生産、材料およびマーケティングの間接費</span><span class="sxs-lookup"><span data-stu-id="0115b-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="0115b-128">原価要素分析コードと原価要素分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="0115b-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="0115b-129">原価要素は、*原価要素分析コード*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0115b-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="0115b-130">個別の分析コード値は、*原価要素分析コード メンバー*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0115b-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="0115b-131">たとえば、法定レポートの基準となる米国の勘定科目表の構造 (COA) があります。</span><span class="sxs-lookup"><span data-stu-id="0115b-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="0115b-132">この COA は、原価要素分析コードとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="0115b-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="0115b-133">主要原価要素である勘定は、原価計算の原価要素分析コード メンバーとして表されます。</span><span class="sxs-lookup"><span data-stu-id="0115b-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="0115b-134">次のスクリーン ショットは、原価要素分析コード メンバーとしての実際の主勘定である原価要素分析コードとしての主勘定の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0115b-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="0115b-135">[![原価要素分析コード](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="0115b-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="0115b-136">データ コネクタを使用して原価要素分析コード メンバーのインポート</span><span class="sxs-lookup"><span data-stu-id="0115b-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="0115b-137">原価計算の原価要素分析コード メンバーの設定を容易にするために、ビルド済みの、またはカスタム ビルドのいずれかのデータ コネクタを使用して、1 つ以上のソース システムから主要原価要素を取得できます。</span><span class="sxs-lookup"><span data-stu-id="0115b-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="0115b-138">実装の考慮事項</span><span class="sxs-lookup"><span data-stu-id="0115b-138">Implementation considerations</span></span>
<span data-ttu-id="0115b-139">原価要素は原価の詳細の最下位レベルを表すので、原価要素構造を導入する際に、管理レポート作成に必要なすべての原価要素が含まれていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0115b-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="0115b-140">原価管理の原価要素の適切な番号を見つけることはすることは課題です。</span><span class="sxs-lookup"><span data-stu-id="0115b-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="0115b-141">多くの原価要素があると、各原価要素をコントロールすることが難しくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0115b-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="0115b-142">代わりとして、原価要素をグループ化し、集計レベルで原価管理を管理できます。</span><span class="sxs-lookup"><span data-stu-id="0115b-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




