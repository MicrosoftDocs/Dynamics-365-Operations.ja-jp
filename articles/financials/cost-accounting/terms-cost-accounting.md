---
title: "原価会計用語"
description: "このトピックでは、原価計算で使用する重要な用語を定義します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 702fa3cb4219aecd95a74d3c225e104be5f281fc
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="cost-accounting-terminology"></a><span data-ttu-id="91541-103">原価会計用語</span><span class="sxs-lookup"><span data-stu-id="91541-103">Cost accounting terminology</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91541-104">このトピックでは、原価計算で使用する重要な用語を定義します。</span><span class="sxs-lookup"><span data-stu-id="91541-104">This topic defines the key terms that are used in Cost accounting.</span></span>

<span data-ttu-id="91541-105">**配賦基準**</span><span class="sxs-lookup"><span data-stu-id="91541-105">**Allocation base**</span></span>

<span data-ttu-id="91541-106">配賦基準は活動を測定および数量化するために使用される基準です。たとえば使用された機械の時間、消費されたキロワット時間、または占有された平方フィート単位などです。</span><span class="sxs-lookup"><span data-stu-id="91541-106">The allocation base is used to measure and quantify activities, such as machine hours that are used, kilowatt hours that are consumed, or square footage that is occupied.</span></span> <span data-ttu-id="91541-107">これは、1 つまたは複数のオブジェクトのコスト配賦の基礎として使用されています。</span><span class="sxs-lookup"><span data-stu-id="91541-107">It's used as basis for allocating costs to one or more cost objects</span></span>

<span data-ttu-id="91541-108">**原価会計**</span><span class="sxs-lookup"><span data-stu-id="91541-108">**Cost accounting**</span></span>

<span data-ttu-id="91541-109">原価計算では、総勘定元帳、補助元帳、予算、および統計情報などのさまざまなソースから、データを収集することができます。</span><span class="sxs-lookup"><span data-stu-id="91541-109">Cost accounting lets you collect data from various sources, such as the general ledger, sub-ledgers, budgets, and statistical information.</span></span> <span data-ttu-id="91541-110">次に分析、集計、および原価データを評価し、管理者が価格の更新、予算、原価管理などの最善の決定ができるようにします。</span><span class="sxs-lookup"><span data-stu-id="91541-110">You can then analyze, summarize, and evaluate cost data, so that management can make the best possible decisions for price updates, budgets, cost control, and so on.</span></span> <span data-ttu-id="91541-111">原価分析に使用されるソース データは、原価計算では別に処理されます。</span><span class="sxs-lookup"><span data-stu-id="91541-111">The source data that is used for cost analysis is treated independently in Cost accounting.</span></span> <span data-ttu-id="91541-112">したがって、原価計算の更新はソース データに影響しません。</span><span class="sxs-lookup"><span data-stu-id="91541-112">Therefore, updates in Cost accounting don’t affect the source data.</span></span> <span data-ttu-id="91541-113">ただし、さまざまなソースから原価データを収集し、特に原価要素として、Microsoft Dynamics 365 for Finance and Operations の総勘定元帳から主勘定をインポートすると、同じデータが総勘定元帳と原価計算の両方に存在するため、データ冗長があります。</span><span class="sxs-lookup"><span data-stu-id="91541-113">However, when you collect cost data from various sources, and especially when you import the main accounts from General ledger in Microsoft Dynamics 365 for Finance and Operations as cost elements, there is data redundancy, because the same data exists in both General ledger and Cost accounting.</span></span> <span data-ttu-id="91541-114">この冗長性は、外部レポートでの財務管理および内部レポートでの原価計算を使用するために必要です。</span><span class="sxs-lookup"><span data-stu-id="91541-114">This redundancy is required, because you use financial management for external reporting and Cost accounting for internal reporting.</span></span>

<span data-ttu-id="91541-115">**原価会計元帳**</span><span class="sxs-lookup"><span data-stu-id="91541-115">**Cost accounting ledger**</span></span>

<span data-ttu-id="91541-116">カレンダー、通貨および原価要素分析コードで定義され、コストを測定する際のプロセスとポリシーをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="91541-116">Defined by calendar, currency, and cost element dimension, it controls processes and policies for measuring costs.</span></span> 

<span data-ttu-id="91541-117">**原価エントリ**</span><span class="sxs-lookup"><span data-stu-id="91541-117">**Cost entry**</span></span>

<span data-ttu-id="91541-118">原価エントリとは、総勘定元帳エントリのデータ コネクタによる転送の結果、原価配賦および原価仕訳帳に転記された原価エントリです。</span><span class="sxs-lookup"><span data-stu-id="91541-118">Cost entries are the result of a transfer via data connectors from general ledger entries, cost allocations, and posted cost entries in cost journals.</span></span>

<span data-ttu-id="91541-119">**原価オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="91541-119">**Cost object**</span></span>

<span data-ttu-id="91541-120">原価管理に対して選択されるオブジェクトのすべてのタイプです。</span><span class="sxs-lookup"><span data-stu-id="91541-120">Any type of object that is selected for cost control.</span></span> <span data-ttu-id="91541-121">コストまたは収益は、直接転記または原価オブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="91541-121">Costs or revenues are either directly posted on or allocated to cost objects.</span></span> <span data-ttu-id="91541-122">一般的なコストのオブジェクトを挙げます。</span><span class="sxs-lookup"><span data-stu-id="91541-122">Some typical cost objects are:</span></span>

-  <span data-ttu-id="91541-123">製品</span><span class="sxs-lookup"><span data-stu-id="91541-123">Products</span></span>
-  <span data-ttu-id="91541-124">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="91541-124">Projects</span></span>
-  <span data-ttu-id="91541-125">部門</span><span class="sxs-lookup"><span data-stu-id="91541-125">Departments</span></span>
-  <span data-ttu-id="91541-126">コスト センター</span><span class="sxs-lookup"><span data-stu-id="91541-126">Cost centers</span></span>

<span data-ttu-id="91541-127">管理者は、原価を定量化するのに原価オブジェクトを使用し、収益性分析を推進します。</span><span class="sxs-lookup"><span data-stu-id="91541-127">Management uses cost objects to quantify costs, but also to drive profitability analysis.</span></span>

<span data-ttu-id="91541-128">**原価要素**</span><span class="sxs-lookup"><span data-stu-id="91541-128">**Cost element**</span></span>

<span data-ttu-id="91541-129">追跡およびコストの分類の機能として使用します。</span><span class="sxs-lookup"><span data-stu-id="91541-129">Used as a function to track and categorize costs.</span></span> <span data-ttu-id="91541-130">原価要素には、基本と二次という 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="91541-130">There are two types of cost elements: primary and secondary.</span></span>

<span data-ttu-id="91541-131">主要原価要素は、財務会計から原価会計へのコストの流れを表します。</span><span class="sxs-lookup"><span data-stu-id="91541-131">Primary cost elements represent the cost flow from financial accounting to Cost accounting.</span></span> <span data-ttu-id="91541-132">構造は通常、原価要素が主勘定に対応できる一般会計で損益勘定構造に対応します。</span><span class="sxs-lookup"><span data-stu-id="91541-132">The structure typically corresponds to the profit and loss account structure in the general ledger where a cost element can correspond to a main account.</span></span> <span data-ttu-id="91541-133">業務上の要件に応じて、すべての主勘定が原価要素として表される必要があります。</span><span class="sxs-lookup"><span data-stu-id="91541-133">Not all main accounts must be represented as cost elements, depending on business requirements.</span></span> 

<span data-ttu-id="91541-134">第 2 原価要素は、これらのコストが原価会計でのみ使用されるため、内部のコストの流れを表します。</span><span class="sxs-lookup"><span data-stu-id="91541-134">Secondary cost elements represent the internal cost flow because these costs are only used in Cost accounting.</span></span> <span data-ttu-id="91541-135">これらは、間接費の計算で使用される意味のあるバケットにコストを集計するために、原価ロールアップのルールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="91541-135">They are used in cost roll-up rules to aggregate costs into meaningful buckets used by overhead calculation.</span></span> 

<span data-ttu-id="91541-136">**原価分類**</span><span class="sxs-lookup"><span data-stu-id="91541-136">**Cost classification**</span></span>

<span data-ttu-id="91541-137">原価分類グループは、共有された特性に基づいて原価をグループ分けします。</span><span class="sxs-lookup"><span data-stu-id="91541-137">Cost classification groups costs according to their shared characteristics.</span></span> <span data-ttu-id="91541-138">たとえば、原価は、要素、トレーサビリティ、および動作にグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="91541-138">For example, costs can be grouped by elements, traceability, and behavior.</span></span>

-   <span data-ttu-id="91541-139">**要素による** – 材料、労務、および経費。</span><span class="sxs-lookup"><span data-stu-id="91541-139">**By elements** – Materials, labor, and expenses.</span></span>
-   <span data-ttu-id="91541-140">**トレーサビリティによる** – 直接原価および間接原価。</span><span class="sxs-lookup"><span data-stu-id="91541-140">**By traceability** – Direct costs and indirect costs.</span></span> <span data-ttu-id="91541-141">直接原価は原価オブジェクトに直接割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="91541-141">Direct costs are assigned directly to cost objects.</span></span> <span data-ttu-id="91541-142">間接原価は、原価オブジェクトを直接追跡できません。</span><span class="sxs-lookup"><span data-stu-id="91541-142">Indirect costs aren't directly traceable to cost objects.</span></span> <span data-ttu-id="91541-143">間接原価は、原価オブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="91541-143">Indirect costs are allocated to cost objects.</span></span>
-   <span data-ttu-id="91541-144">**動作にる** - 固定、変数、半変数。</span><span class="sxs-lookup"><span data-stu-id="91541-144">**By behavior** – Fixed, variable, and semi-variable.</span></span>

<span data-ttu-id="91541-145">**原価動作**</span><span class="sxs-lookup"><span data-stu-id="91541-145">**Cost behavior**</span></span>

<span data-ttu-id="91541-146">原価動作は、鍵となる事業活動の変更に関連する動作に基づいて原価を分類します。</span><span class="sxs-lookup"><span data-stu-id="91541-146">Cost behavior classifies costs according to their behavior in relation to changes in key business activities.</span></span> <span data-ttu-id="91541-147">原価を効率的に管理するには、管理者は原価の動作を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91541-147">To control costs effectively, management must understand the cost behavior.</span></span> <span data-ttu-id="91541-148">原価の動作のパターンには 3 つのタイプ、つまり固定、変数、半変数があります。</span><span class="sxs-lookup"><span data-stu-id="91541-148">There are three types of cost behavior pattern: fixed, variable, and semi-variable.</span></span>

- <span data-ttu-id="91541-149">**固定費** - 固定費は、活動レベルの変更に関係なく、短期的に変化しないコストです。</span><span class="sxs-lookup"><span data-stu-id="91541-149">**Fixed cost** - A fixed cost is a cost that doesn't vary in the short term, regardless of changes in activity level.</span></span> <span data-ttu-id="91541-150">たとえば、固定費は、家賃などの業務の基本的な作業経費であり、活動の増加および減少の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="91541-150">For example, a fixed cost can be a basic operating expense of a business, such as rent, that won't be affected even if the activity level increases or decreases.</span></span>

- <span data-ttu-id="91541-151">**変動費** - 変動費は、活動レベルの変化に従って変化します。</span><span class="sxs-lookup"><span data-stu-id="91541-151">**Variable cost** - A variable cost changes according to changes in activity level.</span></span> <span data-ttu-id="91541-152">たとえば、特定の直接材料の原価は、販売された各製品に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="91541-152">For example, a specific direct materials cost is associated with each product that is sold.</span></span> <span data-ttu-id="91541-153">販売された製品が多くなれば、直接的な材料の原価は多くなります。</span><span class="sxs-lookup"><span data-stu-id="91541-153">The more products that are sold, the more direct materials costs there are.</span></span>

- <span data-ttu-id="91541-154">**半変動費** - 半変動費は部分的に固定費であり、また部分的に変動費な費用です。</span><span class="sxs-lookup"><span data-stu-id="91541-154">**Semi-variable cost** - Semi-variable costs are partly fixed and partly variable costs.</span></span> <span data-ttu-id="91541-155">たとえば、インターネット アクセス料金には、標準的な月額のアクセス料金とブロードバンド使用料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="91541-155">For example, an Internet access fee includes a standard monthly access fee and a broadband usage fee.</span></span> <span data-ttu-id="91541-156">標準的な月額アクセス料金は固定費で、ブロードバンド使用料金は変動費です。</span><span class="sxs-lookup"><span data-stu-id="91541-156">The standard monthly access fee is a fixed cost, whereas the broadband usage fee is a variable cost.</span></span>

<span data-ttu-id="91541-157">**原価管理単位**</span><span class="sxs-lookup"><span data-stu-id="91541-157">**Cost control unit**</span></span>

<span data-ttu-id="91541-158">原価管理単位は、原価構造を表します。</span><span class="sxs-lookup"><span data-stu-id="91541-158">The cost control unit represents the cost structure.</span></span> <span data-ttu-id="91541-159">構造は、原価オブジェクト分析コードとそれらに対応する原価オブジェクトの間で、コストがどのように階層順に流れるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="91541-159">The structure determines how cost flows in a hierarchical order between cost object dimensions and their respective cost objects.</span></span> 

<span data-ttu-id="91541-160">**原価配分**</span><span class="sxs-lookup"><span data-stu-id="91541-160">**Cost distribution**</span></span>

<span data-ttu-id="91541-161">関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="91541-161">Is used to distribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="91541-162">コスト配分とコスト配賦は、コスト配分は常に元のコストおよび相互的でない処理の主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="91541-162">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost and no reciprocal processing.</span></span>

<span data-ttu-id="91541-163">**原価配賦**</span><span class="sxs-lookup"><span data-stu-id="91541-163">**Cost allocation**</span></span>

<span data-ttu-id="91541-164">配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="91541-164">Is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="91541-165">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="91541-165">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="91541-166">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="91541-166">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="91541-167">システムは、配賦を実行し、繰り返し処理する順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="91541-167">The system automatically determines the order to perform the allocations in and iterate over it.</span></span> <span data-ttu-id="91541-168">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="91541-168">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="91541-169">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="91541-169">Allocations across cost object dimensions and their respective members are supported.</span></span> <span data-ttu-id="91541-170">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="91541-170">The allocation order is controlled by the cost control unit.</span></span>

<span data-ttu-id="91541-171">[**原価配賦ポリシー**]</span><span class="sxs-lookup"><span data-stu-id="91541-171">**Cost allocation policy**</span></span>

<span data-ttu-id="91541-172">原価配賦のポリシーは、配賦する必要がある数量と金額を定義します。</span><span class="sxs-lookup"><span data-stu-id="91541-172">A cost allocation policy defines the amounts and quantities that must be allocated.</span></span> <span data-ttu-id="91541-173">配賦ルールには配賦元のルールが含まれます。これは配賦されている原価の決定、および原価が割り当てられるところを決定する配賦先のルールを決定します。</span><span class="sxs-lookup"><span data-stu-id="91541-173">Allocation rules include allocation source rules, which determine the costs that are allocated, and allocation targets rules, which determine where the costs are allocated.</span></span> <span data-ttu-id="91541-174">たとえば、融資サービスのすべての原価は、組織 (つまり、配賦ターゲット) のさまざまな部門に割り当てることができる配賦ソースです。</span><span class="sxs-lookup"><span data-stu-id="91541-174">For example, all costs for facility services are an allocation source that can be allocated to various departments in an organization (that is, to allocation targets).</span></span>

<span data-ttu-id="91541-175">**原価ロールアップ**</span><span class="sxs-lookup"><span data-stu-id="91541-175">**Cost roll-up**</span></span>

<span data-ttu-id="91541-176">コストロールアップのルールの目的は、意味のあるバケットにコストを集計することです。</span><span class="sxs-lookup"><span data-stu-id="91541-176">The purpose of cost roll-up rules is to aggregate costs into meaningful buckets.</span></span> <span data-ttu-id="91541-177">集約のレベルは、ユーザー定義であり、第 2 原価要素の割り当てが含まれます。</span><span class="sxs-lookup"><span data-stu-id="91541-177">The level of aggregation is user-defined and involves the assignment of a secondary cost element.</span></span> <span data-ttu-id="91541-178">原価のロールアップを使用しない場合、コストのすべての要素が、1 つの原価オブジェクトから他の原価オブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="91541-178">If cost roll-up is not used, every element of a cost is allocated from one cost object to another</span></span>

<span data-ttu-id="91541-179">**原価率のポリシー**</span><span class="sxs-lookup"><span data-stu-id="91541-179">**Cost rate policy**</span></span>

<span data-ttu-id="91541-180">原価率は原価オブジェクトあたりの価格を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="91541-180">The cost rate is used to calculate price per cost object.</span></span> <span data-ttu-id="91541-181">価格の要素を理解するために、原価率のポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="91541-181">To understand the elements of the price, you define cost rate policies.</span></span> <span data-ttu-id="91541-182">原価率には、履歴原価率と予定原価率という 2 種類のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="91541-182">There are two types of cost rate: historical cost rate and planned cost rate.</span></span> <span data-ttu-id="91541-183">履歴原価率は原価オブジェクトの配賦基準に対して乗数で使用される計算された率です。</span><span class="sxs-lookup"><span data-stu-id="91541-183">A historical cost rate is a calculated rate that is used as a multiplier for the allocation base of a cost object.</span></span> <span data-ttu-id="91541-184">この率は、前の期間の原価配賦に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="91541-184">The rate is calculated based on the cost allocations in the previous period.</span></span> <span data-ttu-id="91541-185">計画されたレートは、ユーザー定義のレートです。</span><span class="sxs-lookup"><span data-stu-id="91541-185">A planned rate is a user-defined rate.</span></span>

<span data-ttu-id="91541-186">**分析コード階層**</span><span class="sxs-lookup"><span data-stu-id="91541-186">**Dimension hierarchy**</span></span>

<span data-ttu-id="91541-187">カテゴリ階層、および分類階層という 2 つの分析コード階層があります。</span><span class="sxs-lookup"><span data-stu-id="91541-187">There are two dimension hierarchies: categorization hierarchy and classification hierarchy.</span></span> <span data-ttu-id="91541-188">[分析コードカテゴリ階層] タイプはレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="91541-188">The dimension categorization hierarchy type is used for reporting purposes.</span></span> <span data-ttu-id="91541-189">コスト要素分析コードのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="91541-189">It supports only the cost element dimensions.</span></span> <span data-ttu-id="91541-190">[分析コード分類階層] タイプはポリシーの定義、およびレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="91541-190">The dimension classification hierarchy type is used to define policies and for reporting purposes.</span></span> <span data-ttu-id="91541-191">コスト オブジェクト、コスト要素、および統計分析コードなどのすべての分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="91541-191">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span> 

<span data-ttu-id="91541-192">**データ コネクタ**</span><span class="sxs-lookup"><span data-stu-id="91541-192">**Data connector**</span></span>

<span data-ttu-id="91541-193">原価会計は、データ コネクタのセットを経由してのソース システムからのデータの統合をサポートします。</span><span class="sxs-lookup"><span data-stu-id="91541-193">Cost accounting supports integration of data from source systems via a set of data connectors.</span></span> <span data-ttu-id="91541-194">使用できるデータ コネクタは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="91541-194">The following data connectors are available:</span></span>

-  <span data-ttu-id="91541-195">インポートされたトランザクション (コンフィギュレーション済み)</span><span class="sxs-lookup"><span data-stu-id="91541-195">Imported transactions (pre-configured)</span></span>
-  <span data-ttu-id="91541-196">Dynamics 365 for Finance and Operations (コンフィギュレーション済み)</span><span class="sxs-lookup"><span data-stu-id="91541-196">Dynamics 365 for Finance and Operations (pre-configured)</span></span>
-  <span data-ttu-id="91541-197">Dynamics AX (コンフィギュレーションが必須)</span><span class="sxs-lookup"><span data-stu-id="91541-197">Dynamics AX (configuration required)</span></span>

<span data-ttu-id="91541-198">**注記:** データ コネクタは、データ エンティティに基づくトランザクションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="91541-198">**Note:** The data connector Imported transactions is based on data entities.</span></span>

<span data-ttu-id="91541-199">**データ プロバイダー**</span><span class="sxs-lookup"><span data-stu-id="91541-199">**Data provider**</span></span>

<span data-ttu-id="91541-200">ほとんどのソース システムでは、原価会計で1つまたは複数のデータ ソースに一致するデータを提供できます。</span><span class="sxs-lookup"><span data-stu-id="91541-200">Most source systems can provide data that matches one or more data sources in Cost accounting.</span></span> <span data-ttu-id="91541-201">原価会計のデータ ソースとのソース システムデータを調整するには、データ プロバイダーはコンフィギュレーションされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="91541-201">To align data from the source systems with the data source in Cost accounting, a data provider needs to be configured.</span></span> <span data-ttu-id="91541-202">次の表は、データ ソースおよびデータ コネクタごとにデータ プロバイダーが使用できるかを一覧で示しています。</span><span class="sxs-lookup"><span data-stu-id="91541-202">The following table lists the availability of data providers per data connector and data source.</span></span>

|  <span data-ttu-id="91541-203">**データ ソース**</span><span class="sxs-lookup"><span data-stu-id="91541-203">**Data sources**</span></span> |  <span data-ttu-id="91541-204">**インポートされたトランザクション データ コネクタ**</span><span class="sxs-lookup"><span data-stu-id="91541-204">**Imported transactions data connector**</span></span> | <span data-ttu-id="91541-205">**Dynamics 365 for Finance and Operations データ コネクタ**</span><span class="sxs-lookup"><span data-stu-id="91541-205">**Dynamics 365 for Finance and Operations data connector**</span></span>  | <span data-ttu-id="91541-206">**Dynamics AX データ コネクタ**</span><span class="sxs-lookup"><span data-stu-id="91541-206">**Dynamics AX data connector**</span></span>  |
|---|---|---|---|
| <span data-ttu-id="91541-207">原価要素分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="91541-207">Cost element dimension members</span></span>  |  <span data-ttu-id="91541-208">有</span><span class="sxs-lookup"><span data-stu-id="91541-208">Yes</span></span> | <span data-ttu-id="91541-209">有</span><span class="sxs-lookup"><span data-stu-id="91541-209">Yes</span></span>  | <span data-ttu-id="91541-210">有</span><span class="sxs-lookup"><span data-stu-id="91541-210">Yes</span></span>  |
|  <span data-ttu-id="91541-211">原価オブジェクト分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="91541-211">Cost object dimension members</span></span> |  <span data-ttu-id="91541-212">有</span><span class="sxs-lookup"><span data-stu-id="91541-212">Yes</span></span> | <span data-ttu-id="91541-213">有</span><span class="sxs-lookup"><span data-stu-id="91541-213">Yes</span></span>  | <span data-ttu-id="91541-214">有</span><span class="sxs-lookup"><span data-stu-id="91541-214">Yes</span></span>  |
|  <span data-ttu-id="91541-215">統計分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="91541-215">Statistical dimension members</span></span> | <span data-ttu-id="91541-216">有</span><span class="sxs-lookup"><span data-stu-id="91541-216">Yes</span></span>  | <span data-ttu-id="91541-217">無</span><span class="sxs-lookup"><span data-stu-id="91541-217">No</span></span>  | <span data-ttu-id="91541-218">無</span><span class="sxs-lookup"><span data-stu-id="91541-218">No</span></span>  |
|  <span data-ttu-id="91541-219">一般会計</span><span class="sxs-lookup"><span data-stu-id="91541-219">General ledger</span></span> | <span data-ttu-id="91541-220">有</span><span class="sxs-lookup"><span data-stu-id="91541-220">Yes</span></span>  | <span data-ttu-id="91541-221">有</span><span class="sxs-lookup"><span data-stu-id="91541-221">Yes</span></span>  | <span data-ttu-id="91541-222">有</span><span class="sxs-lookup"><span data-stu-id="91541-222">Yes</span></span>  |
|  <span data-ttu-id="91541-223">予算項目</span><span class="sxs-lookup"><span data-stu-id="91541-223">Budget entries</span></span>  | <span data-ttu-id="91541-224">有</span><span class="sxs-lookup"><span data-stu-id="91541-224">Yes</span></span>  | <span data-ttu-id="91541-225">有</span><span class="sxs-lookup"><span data-stu-id="91541-225">Yes</span></span>  | <span data-ttu-id="91541-226">有</span><span class="sxs-lookup"><span data-stu-id="91541-226">Yes</span></span>  |
|  <span data-ttu-id="91541-227">統計測定</span><span class="sxs-lookup"><span data-stu-id="91541-227">Statistical measures</span></span> | <span data-ttu-id="91541-228">有</span><span class="sxs-lookup"><span data-stu-id="91541-228">Yes</span></span>  | <span data-ttu-id="91541-229">有</span><span class="sxs-lookup"><span data-stu-id="91541-229">Yes</span></span>  | <span data-ttu-id="91541-230">有</span><span class="sxs-lookup"><span data-stu-id="91541-230">Yes</span></span>  |

<span data-ttu-id="91541-231">**式**</span><span class="sxs-lookup"><span data-stu-id="91541-231">**Formula**</span></span>

<span data-ttu-id="91541-232">フォーミュラの配賦基準では、正しい配賦基準を実現する高度な式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="91541-232">Formula allocation bases let you define advanced formulas to achieve the correct allocation basis.</span></span> <span data-ttu-id="91541-233">フォーミュラ配賦基準を手動で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="91541-233">You can manually create formula allocation bases.</span></span> <span data-ttu-id="91541-234">式の定義には次の演算子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="91541-234">You can use the following operators to define your formula.</span></span>

|  <span data-ttu-id="91541-235">**記号:**</span><span class="sxs-lookup"><span data-stu-id="91541-235">**Symbols**</span></span> | <span data-ttu-id="91541-236">**テキスト**</span><span class="sxs-lookup"><span data-stu-id="91541-236">**Text**</span></span>  |
|---|---|
|  <span data-ttu-id="91541-237">( )</span><span class="sxs-lookup"><span data-stu-id="91541-237">( )</span></span> | <span data-ttu-id="91541-238">かっこ</span><span class="sxs-lookup"><span data-stu-id="91541-238">Parentheses</span></span>  |
|  < |  <span data-ttu-id="91541-239">より小さい</span><span class="sxs-lookup"><span data-stu-id="91541-239">Smaller than</span></span> |
|  > |  <span data-ttu-id="91541-240">より大きい</span><span class="sxs-lookup"><span data-stu-id="91541-240">Larger than</span></span> |
|  + |  <span data-ttu-id="91541-241">追加</span><span class="sxs-lookup"><span data-stu-id="91541-241">Addition</span></span> |
|  <span data-ttu-id="91541-242">-</span><span class="sxs-lookup"><span data-stu-id="91541-242">–</span></span> |  <span data-ttu-id="91541-243">減算</span><span class="sxs-lookup"><span data-stu-id="91541-243">Subtraction</span></span> |
| *  | <span data-ttu-id="91541-244">乗算</span><span class="sxs-lookup"><span data-stu-id="91541-244">Multiplication</span></span>  |

<span data-ttu-id="91541-245">従来型の IF ステートメントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="91541-245">Traditional IF statements are not supported.</span></span> <span data-ttu-id="91541-246">ただし、ステートメントを作成し、それが正しいかを検証できます。</span><span class="sxs-lookup"><span data-stu-id="91541-246">However, you can create statements and validate whether they are true.</span></span>

|  <span data-ttu-id="91541-247">**明細書の検証**</span><span class="sxs-lookup"><span data-stu-id="91541-247">**Statement  Validation**</span></span> | <span data-ttu-id="91541-248">**結果**</span><span class="sxs-lookup"><span data-stu-id="91541-248">**Result**</span></span>  |
|---|---|
|  <span data-ttu-id="91541-249">a > b</span><span class="sxs-lookup"><span data-stu-id="91541-249">a > b</span></span>| <span data-ttu-id="91541-250">True</span><span class="sxs-lookup"><span data-stu-id="91541-250">True</span></span>  |
|  <span data-ttu-id="91541-251">a > b</span><span class="sxs-lookup"><span data-stu-id="91541-251">a > b</span></span> |  <span data-ttu-id="91541-252">False</span><span class="sxs-lookup"><span data-stu-id="91541-252">False</span></span> |

<span data-ttu-id="91541-253">**間接費**</span><span class="sxs-lookup"><span data-stu-id="91541-253">**Overhead cost**</span></span>

<span data-ttu-id="91541-254">間接費は、事業の遂行に必要な経費を示します。</span><span class="sxs-lookup"><span data-stu-id="91541-254">Overhead costs refer to the ongoing expenses of operating a business.</span></span> <span data-ttu-id="91541-255">これらは、特定の営業活動に直接リンクすることができない費用です。</span><span class="sxs-lookup"><span data-stu-id="91541-255">They are the costs that can’t be linked directly to specific business activities.</span></span> <span data-ttu-id="91541-256">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="91541-256">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="91541-257">会計処理手数料</span><span class="sxs-lookup"><span data-stu-id="91541-257">Accounting fees</span></span>
-   <span data-ttu-id="91541-258">減価償却</span><span class="sxs-lookup"><span data-stu-id="91541-258">Depreciations</span></span>
-   <span data-ttu-id="91541-259">保険</span><span class="sxs-lookup"><span data-stu-id="91541-259">Insurance</span></span>
-   <span data-ttu-id="91541-260">関心事項</span><span class="sxs-lookup"><span data-stu-id="91541-260">Interest</span></span>
-   <span data-ttu-id="91541-261">弁護料</span><span class="sxs-lookup"><span data-stu-id="91541-261">Legal fees</span></span>
-   <span data-ttu-id="91541-262">税申告</span><span class="sxs-lookup"><span data-stu-id="91541-262">Taxes</span></span>
-   <span data-ttu-id="91541-263">光熱費</span><span class="sxs-lookup"><span data-stu-id="91541-263">Utilities costs</span></span>

<span data-ttu-id="91541-264">**間接費率**</span><span class="sxs-lookup"><span data-stu-id="91541-264">**Overhead rate**</span></span>

<span data-ttu-id="91541-265">レートは、原価オブジェクトと原価要素ごとに定義されます。</span><span class="sxs-lookup"><span data-stu-id="91541-265">Rates are defined per cost object and cost element.</span></span> <span data-ttu-id="91541-266">レートには2つのタイプがあります。会計年度期間およびユーザー指定。</span><span class="sxs-lookup"><span data-stu-id="91541-266">There are two types of rates: fiscal period and user-specified.</span></span> <span data-ttu-id="91541-267">会計年度期間の期間率は、間接費の計算によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="91541-267">Fiscal period rates are calculated by the overhead calculation.</span></span> <span data-ttu-id="91541-268">ユーザー固有のレートはユーザー定義され、間接費の計算であらかじめ設定されたレートの原価オブジェクト間の原価を配賦に使用できます。</span><span class="sxs-lookup"><span data-stu-id="91541-268">A user-specific rate is user-defined and can be used to allocate cost between cost objects at a predetermined rate in the overhead calculation.</span></span>

<span data-ttu-id="91541-269">**公開済**</span><span class="sxs-lookup"><span data-stu-id="91541-269">**Published**</span></span>

<span data-ttu-id="91541-270">このフィールドを [はい] に設定した場合、次のロールのいずれかに割り当てられているユーザーは 原価管理ワークスペースでレポートを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="91541-270">If you set this field to Yes, a user who is assigned one of the following roles can view the report in the Cost control workspace:</span></span>

-  <span data-ttu-id="91541-271">原価会計マネージャー</span><span class="sxs-lookup"><span data-stu-id="91541-271">Cost accounting manager</span></span>
-  <span data-ttu-id="91541-272">原価経理担当</span><span class="sxs-lookup"><span data-stu-id="91541-272">Cost accountant</span></span>
-  <span data-ttu-id="91541-273">原価経理担当係</span><span class="sxs-lookup"><span data-stu-id="91541-273">Cost accountant clerk</span></span>
-  <span data-ttu-id="91541-274">原価オブジェクト コントローラー</span><span class="sxs-lookup"><span data-stu-id="91541-274">Cost object controller</span></span>

<span data-ttu-id="91541-275">このフィールドを [いいえ] に設定した場合、次のロールのいずれかに割り当てられているユーザーのみが 原価管理ワークスペースでレポートを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="91541-275">If you set this field to No, only users who are assigned one of the following roles can view the report in the Cost control workspace:</span></span>

-  <span data-ttu-id="91541-276">原価会計マネージャー</span><span class="sxs-lookup"><span data-stu-id="91541-276">Cost accounting manager</span></span>
-  <span data-ttu-id="91541-277">原価経理担当</span><span class="sxs-lookup"><span data-stu-id="91541-277">Cost accountant</span></span>
-  <span data-ttu-id="91541-278">原価経理担当係</span><span class="sxs-lookup"><span data-stu-id="91541-278">Cost accountant clerk</span></span>

<span data-ttu-id="91541-279">**統計分析コード**</span><span class="sxs-lookup"><span data-stu-id="91541-279">**Statistical dimension**</span></span>

<span data-ttu-id="91541-280">統計分析コードとそのメンバーは、原価会計の非通貨入力を登録および制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="91541-280">A statistical dimension and its members are used to register and control non-monetary entries in Cost accounting.</span></span> <span data-ttu-id="91541-281">統計分析コードのメンバーは、次の 2 つの目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="91541-281">Statistical dimension members can be used for two purposes:</span></span>

-  <span data-ttu-id="91541-282">コスト配分やコスト配賦などのポリシーにおける配賦基準として。</span><span class="sxs-lookup"><span data-stu-id="91541-282">As an allocation base in policies such as cost distribution or cost allocation.</span></span>
-  <span data-ttu-id="91541-283">非金銭消費の報告として。</span><span class="sxs-lookup"><span data-stu-id="91541-283">For reporting of non-monetary consumption.</span></span>

<span data-ttu-id="91541-284">統計分析コードは、配賦または原価率の計算の基準として使用できる活動の番号または合計を表します。</span><span class="sxs-lookup"><span data-stu-id="91541-284">A statistical dimension is the expression of a count or sum of an activity that can be used as the basis for allocations or rate calculations.</span></span> <span data-ttu-id="91541-285">これは手動で作成するか、またはソース システムからインポートされます。</span><span class="sxs-lookup"><span data-stu-id="91541-285">It's either created manually or imported from source systems.</span></span> <span data-ttu-id="91541-286">統計分析コードの例には、従業員数、各デバイスのライセンスされたソフトウェアの数、各マシンのパワー消費量、またはコスト センターの平方メートルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="91541-286">Examples of statistical dimensions include the number of employees, the count of licensed software on each device, power consumption of each machine, or square meters for a cost center.</span></span>

<span data-ttu-id="91541-287">**ステートメント**</span><span class="sxs-lookup"><span data-stu-id="91541-287">**Statement**</span></span>

<span data-ttu-id="91541-288">明細書は原価の管理を担当する管理者が使用するビューです。</span><span class="sxs-lookup"><span data-stu-id="91541-288">Statements are views for the managers who are responsible for controlling costs.</span></span> <span data-ttu-id="91541-289">明細書は原価コントローラーで定義され、実際原価および予算化されたコスト、および誤差の簡単な概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="91541-289">Statements are defined by a cost controller, and they provide a quick overview of actual costs, budgeted costs, and deviations.</span></span> <span data-ttu-id="91541-290">マネージャーは、詳細が要求された際さらに掘り下げることができます。</span><span class="sxs-lookup"><span data-stu-id="91541-290">A manager can drill further into details if required.</span></span> <span data-ttu-id="91541-291">信頼できるデータのみが管理者に表示されることを確実にするために、明細書に表示されるデータはアクセス ルールの対象になります。</span><span class="sxs-lookup"><span data-stu-id="91541-291">To help ensure that managers view only data that they are accountable for, data that appears in the statements is subject to access rules.</span></span>

<span data-ttu-id="91541-292">**バージョン**</span><span class="sxs-lookup"><span data-stu-id="91541-292">**Version**</span></span>

<span data-ttu-id="91541-293">さまざまなバージョンがさまざまな結果をシミュレーション、表示および比較するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="91541-293">Versions are used to simulate, view, and compare various outcomes.</span></span> <span data-ttu-id="91541-294">既定では、すべての実際原価は、*実績* として知られる 1 つの基準のバージョンで表示されます。</span><span class="sxs-lookup"><span data-stu-id="91541-294">By default, all actual costs are viewed in one base version that is known as *actual*.</span></span> <span data-ttu-id="91541-295">予算と計算のために、必要を満たす数多くのバージョンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="91541-295">For budgets and calculations, you can work with as many versions as you require.</span></span> <span data-ttu-id="91541-296">たとえば、予算データをオリジナル版にインポートし、変更されたバージョンで予算を変更できます。</span><span class="sxs-lookup"><span data-stu-id="91541-296">For example, you can import budget data into an original version and then revise the budget in a revised version.</span></span> <span data-ttu-id="91541-297">計算のために、複数のバージョンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="91541-297">For calculations, you can create multiple versions.</span></span> <span data-ttu-id="91541-298">これらのさまざまなバージョンでは、原価配賦に適用される異なる計算ルールを使用して、計算を作成できます。</span><span class="sxs-lookup"><span data-stu-id="91541-298">In these various versions, you can then create calculations by using different calculation rules that will be applied for cost allocation.</span></span>



