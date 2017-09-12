---
title: "原価会計用語"
description: "このトピックでは、原価計算で使用する重要な用語を定義します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1f12e8e82430c79ee93f2284e5fdf47ac559525d
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="cost-accounting-terminology"></a><span data-ttu-id="77c59-103">原価会計用語</span><span class="sxs-lookup"><span data-stu-id="77c59-103">Cost accounting terminology</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="77c59-104">このトピックでは、原価計算で使用する重要な用語を定義します。</span><span class="sxs-lookup"><span data-stu-id="77c59-104">This topic defines the key terms that are used in Cost accounting.</span></span>

<span data-ttu-id="77c59-105">**原価会計**</span><span class="sxs-lookup"><span data-stu-id="77c59-105">**Cost accounting**</span></span>

<span data-ttu-id="77c59-106">原価計算では、総勘定元帳、補助元帳、予算、および統計情報などのさまざまなソースから、データを収集することができます。</span><span class="sxs-lookup"><span data-stu-id="77c59-106">Cost accounting lets you collect data from various sources, such as the general ledger, sub-ledgers, budgets, and statistical information.</span></span> <span data-ttu-id="77c59-107">次に分析、集計、および原価データを評価し、管理者が価格の更新、予算、原価管理などの最善の決定ができるようにします。</span><span class="sxs-lookup"><span data-stu-id="77c59-107">You can then analyze, summarize, and evaluate cost data, so that management can make the best possible decisions for price updates, budgets, cost control, and so on.</span></span> <span data-ttu-id="77c59-108">原価分析に使用されるソース データは、原価計算では別に処理されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-108">The source data that is used for cost analysis is treated independently in Cost accounting.</span></span> <span data-ttu-id="77c59-109">したがって、原価計算の更新はソース データに影響しません。</span><span class="sxs-lookup"><span data-stu-id="77c59-109">Therefore, updates in Cost accounting don’t affect the source data.</span></span> <span data-ttu-id="77c59-110">ただし、さまざまなソースから原価データを収集し、特に原価要素として、Microsoft Dynamics 365 for Finance および Operation, Enterprise Edition の一般会計から主勘定をインポートすると、同じデータが一般会計と原価計算の両方に存在するため、データ冗長があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-110">However, when you collect cost data from various sources, and especially when you import the main accounts from General ledger in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition as cost elements, there is data redundancy, because the same data exists in both General ledger and Cost accounting.</span></span> <span data-ttu-id="77c59-111">この冗長性は、外部レポートでの財務管理および内部レポートでの原価計算を使用するために必要です。</span><span class="sxs-lookup"><span data-stu-id="77c59-111">This redundancy is required, because you use financial management for external reporting and Cost accounting for internal reporting.</span></span>

<span data-ttu-id="77c59-112">**原価会計元帳**</span><span class="sxs-lookup"><span data-stu-id="77c59-112">**Cost accounting ledger**</span></span>

<span data-ttu-id="77c59-113">原価会計元帳は、処理方法、値、および入力された数量を決定し、原価計算の特定の領域を表示する特定のフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="77c59-113">The cost accounting ledger is a specialized framework that determines how processes, values, and quantities are entered and presented for a particular area in Cost accounting.</span></span> <span data-ttu-id="77c59-114">原価会計元帳は原価オブジェクトの原価を測定する際のプロセスおよびルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="77c59-114">The cost accounting ledger defines processes and rules for measuring costs on cost objects.</span></span> <span data-ttu-id="77c59-115">これは、原価トランザクションを処理し、原価トランザクションが作成する値および数量の変更を記録するドキュメントを管理します。</span><span class="sxs-lookup"><span data-stu-id="77c59-115">It handles cost transactions, and manages documents that record the changes in values and quantities that cost transactions produce.</span></span>

<span data-ttu-id="77c59-116">**原価エントリ**</span><span class="sxs-lookup"><span data-stu-id="77c59-116">**Cost entry**</span></span>

<span data-ttu-id="77c59-117">原価エントリとは、総勘定元帳エントリのデータ コネクタによる転送の結果、原価配賦および原価仕訳帳に転記された原価エントリです。</span><span class="sxs-lookup"><span data-stu-id="77c59-117">Cost entries are the result of a transfer via data connectors from general ledger entries, cost allocations, and posted cost entries in cost journals.</span></span>

<span data-ttu-id="77c59-118">**原価オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="77c59-118">**Cost object**</span></span>

<span data-ttu-id="77c59-119">原価オブジェクトは、原価が配賦されたオブジェクトのタイプです。</span><span class="sxs-lookup"><span data-stu-id="77c59-119">Cost objects are any type of object that costs are allocated to.</span></span> <span data-ttu-id="77c59-120">一般的な原価のオブジェクトを挙げます:</span><span class="sxs-lookup"><span data-stu-id="77c59-120">Here are some typical cost objects:</span></span>

-   <span data-ttu-id="77c59-121">製品</span><span class="sxs-lookup"><span data-stu-id="77c59-121">Products</span></span>
-   <span data-ttu-id="77c59-122">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="77c59-122">Projects</span></span>
-   <span data-ttu-id="77c59-123">リソース</span><span class="sxs-lookup"><span data-stu-id="77c59-123">Resources</span></span>
-   <span data-ttu-id="77c59-124">部門</span><span class="sxs-lookup"><span data-stu-id="77c59-124">Departments</span></span>
-   <span data-ttu-id="77c59-125">コスト センター</span><span class="sxs-lookup"><span data-stu-id="77c59-125">Cost centers</span></span>
-   <span data-ttu-id="77c59-126">地理的領域</span><span class="sxs-lookup"><span data-stu-id="77c59-126">Geographic regions</span></span>

<span data-ttu-id="77c59-127">管理者は、原価を定量化するのに原価オブジェクトを使用し、収益性分析を推進します。</span><span class="sxs-lookup"><span data-stu-id="77c59-127">Management uses cost objects to quantify costs, but also to drive profitability analysis.</span></span>

<span data-ttu-id="77c59-128">**原価要素**</span><span class="sxs-lookup"><span data-stu-id="77c59-128">**Cost element**</span></span>

<span data-ttu-id="77c59-129">原価要素は、原価がどこに流れるかを追跡および分類する機能として使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-129">Cost elements are used as a function to track and categorize where costs flow to.</span></span> <span data-ttu-id="77c59-130">原価要素には、主要原価と副次原価要素という 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="77c59-130">There are two types of cost elements: primary costs and secondary costs.</span></span> <span data-ttu-id="77c59-131">**基本原価** 主要原価要素は、財務会計から原価計算までの原価の流れを表します。</span><span class="sxs-lookup"><span data-stu-id="77c59-131">**Primary costs** The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="77c59-132">原価要素構造は、原価要素が主勘定に対応できる総勘定元帳で損益勘定構造に対応します。</span><span class="sxs-lookup"><span data-stu-id="77c59-132">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="77c59-133">業務上の要件に応じて、すべての主勘定が原価要素として表される必要があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-133">Not all main accounts must be represented as cost elements, depending on business requirements.</span></span> <span data-ttu-id="77c59-134">次の主要原価要素の例があります:</span><span class="sxs-lookup"><span data-stu-id="77c59-134">Here are some examples of primary cost elements:</span></span>

-   <span data-ttu-id="77c59-135">売却済商品の原価 (COGs)</span><span class="sxs-lookup"><span data-stu-id="77c59-135">Costs of goods sold (COGs)</span></span>
-   <span data-ttu-id="77c59-136">間接材料原価</span><span class="sxs-lookup"><span data-stu-id="77c59-136">Indirect material costs</span></span>
-   <span data-ttu-id="77c59-137">人件費</span><span class="sxs-lookup"><span data-stu-id="77c59-137">Personnel costs</span></span>
-   <span data-ttu-id="77c59-138">エネルギー原価</span><span class="sxs-lookup"><span data-stu-id="77c59-138">Energy costs</span></span>

<span data-ttu-id="77c59-139">**第 2 原価要素**</span><span class="sxs-lookup"><span data-stu-id="77c59-139">**Secondary cost element**</span></span> 

<span data-ttu-id="77c59-140">副次原価要素は、原価計算でのみ作成および使用されるため、内部の原価の流れを表します。</span><span class="sxs-lookup"><span data-stu-id="77c59-140">The secondary cost elements represent the internal flow of costs, because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="77c59-141">副次原価要素は原価のソースが追跡可能であることを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="77c59-141">Secondary cost elements help guarantee that the source of costs can be traced.</span></span> <span data-ttu-id="77c59-142">これらの原価要素は原価配賦および間接費計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-142">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="77c59-143">次の副次原価要素の例があります:</span><span class="sxs-lookup"><span data-stu-id="77c59-143">Here are some examples of secondary cost elements:</span></span>

-   <span data-ttu-id="77c59-144">生産原価</span><span class="sxs-lookup"><span data-stu-id="77c59-144">Production costs</span></span>
-   <span data-ttu-id="77c59-145">生産、材料およびマーケティングの間接費</span><span class="sxs-lookup"><span data-stu-id="77c59-145">Production, material, and marketing overheads</span></span>

<span data-ttu-id="77c59-146">**原価管理単位**</span><span class="sxs-lookup"><span data-stu-id="77c59-146">**Cost control unit**</span></span>

<span data-ttu-id="77c59-147">原価管理単位は、原価構造を表します。</span><span class="sxs-lookup"><span data-stu-id="77c59-147">A cost control unit represents the cost structure.</span></span> <span data-ttu-id="77c59-148">これは、原価会計元帳の原価オブジェクト分析コードに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-148">It must be associated with cost object dimensions in a cost accounting ledger.</span></span>

<span data-ttu-id="77c59-149">**バージョン**</span><span class="sxs-lookup"><span data-stu-id="77c59-149">**Version**</span></span>

<span data-ttu-id="77c59-150">さまざまなバージョンがさまざまな結果をシミュレーション、表示および比較するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-150">Versions are used to simulate, view, and compare various outcomes.</span></span> <span data-ttu-id="77c59-151">既定では、すべての実際原価は、*実績* として知られる 1 つの基準のバージョンで表示されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-151">By default, all actual costs are viewed in one base version that is known as *actual*.</span></span> <span data-ttu-id="77c59-152">予算と計算のために、必要を満たす数多くのバージョンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-152">For budgets and calculations, you can work with as many versions as you require.</span></span> <span data-ttu-id="77c59-153">たとえば、予算データをオリジナル版にインポートし、変更されたバージョンで予算を変更できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-153">For example, you can import budget data into an original version and then revise the budget in a revised version.</span></span> <span data-ttu-id="77c59-154">計算のために、複数のバージョンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-154">For calculations, you can create multiple versions.</span></span> <span data-ttu-id="77c59-155">これらのさまざまなバージョンでは、原価配賦に適用される異なる計算ルールを使用して、計算を作成できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-155">In these various versions, you can then create calculations by using different calculation rules that will be applied for cost allocation.</span></span>

<span data-ttu-id="77c59-156">**明細書**</span><span class="sxs-lookup"><span data-stu-id="77c59-156">**Statement**</span></span>

<span data-ttu-id="77c59-157">明細書は原価の管理を担当する管理者が使用するビューです。</span><span class="sxs-lookup"><span data-stu-id="77c59-157">Statements are views for the managers who are responsible for controlling costs.</span></span> <span data-ttu-id="77c59-158">明細書は原価コントローラーで定義され、実績および予算化された原価の簡単な概要の表示、および誤差と計算されたバージョンも表示します。</span><span class="sxs-lookup"><span data-stu-id="77c59-158">Statements are defined by a cost controller, and they give a quick overview of actual and budgeted costs, and even deviations and calculation versions.</span></span> <span data-ttu-id="77c59-159">信頼できるデータのみが管理者に表示されることを保証するために、明細書に表示されるデータはアクセス ルールの対象になります。</span><span class="sxs-lookup"><span data-stu-id="77c59-159">To help guarantee that managers view only data that they are accountable for, data that appears in the statements is subject to access rules.</span></span>

<span data-ttu-id="77c59-160">**データ コネクタ**</span><span class="sxs-lookup"><span data-stu-id="77c59-160">**Data connector**</span></span>

<span data-ttu-id="77c59-161">データはデータ コネクタを介して外部システムから原価計算にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="77c59-161">Data can be imported into Cost accounting from external systems via data connectors.</span></span> <span data-ttu-id="77c59-162">たとえば、勘定構造、分析コード、総勘定元帳エントリおよび予算エントリをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="77c59-162">For example, you can import account structures, dimensions, general ledger entries, and budget entries.</span></span> <span data-ttu-id="77c59-163">データのインポートおよびデータ接続の作成には、事前にコンフィギュレーションされたデータ コネクタまたはカスタム コネクタを使用します。</span><span class="sxs-lookup"><span data-stu-id="77c59-163">You can use preconfigured data connectors or custom connectors to import data and create data connections.</span></span>

<span data-ttu-id="77c59-164">**原価分類**</span><span class="sxs-lookup"><span data-stu-id="77c59-164">**Cost classification**</span></span>

<span data-ttu-id="77c59-165">原価分類グループは、共有された特性に基づいて原価をグループ分けします。</span><span class="sxs-lookup"><span data-stu-id="77c59-165">Cost classification groups costs according to their shared characteristics.</span></span> <span data-ttu-id="77c59-166">たとえば、原価は、要素、トレーサビリティ、および動作にグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-166">For example, costs can be grouped by elements, traceability, and behavior.</span></span>

-   <span data-ttu-id="77c59-167">**要素による** – 材料、労務、および経費。</span><span class="sxs-lookup"><span data-stu-id="77c59-167">**By elements** – Materials, labor, and expenses.</span></span>
-   <span data-ttu-id="77c59-168">**トレーサビリティによる** – 直接原価および間接原価。</span><span class="sxs-lookup"><span data-stu-id="77c59-168">**By traceability** – Direct costs and indirect costs.</span></span> <span data-ttu-id="77c59-169">直接原価は原価オブジェクトに直接割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="77c59-169">Direct costs are assigned directly to cost objects.</span></span> <span data-ttu-id="77c59-170">間接原価は、原価オブジェクトを直接追跡できません。</span><span class="sxs-lookup"><span data-stu-id="77c59-170">Indirect costs aren't directly traceable to cost objects.</span></span> <span data-ttu-id="77c59-171">間接原価は、原価オブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="77c59-171">Indirect costs are allocated to cost objects.</span></span>
-   <span data-ttu-id="77c59-172">**動作にる** - 固定、変数、半変数。</span><span class="sxs-lookup"><span data-stu-id="77c59-172">**By behavior** – Fixed, variable, and semi-variable.</span></span>

<span data-ttu-id="77c59-173">**原価動作**</span><span class="sxs-lookup"><span data-stu-id="77c59-173">**Cost behavior**</span></span>

<span data-ttu-id="77c59-174">原価動作は、鍵となる事業活動の変更に関連する動作に基づいて原価を分類します。</span><span class="sxs-lookup"><span data-stu-id="77c59-174">Cost behavior classifies costs according to their behavior in relation to changes in key business activities.</span></span> <span data-ttu-id="77c59-175">原価を効率的に管理するには、管理者は原価の動作を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-175">To control costs effectively, management must understand the cost behavior.</span></span> <span data-ttu-id="77c59-176">原価の動作のパターンには 3 つのタイプ、つまり固定、変数、半変数があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-176">There are three types of cost behavior pattern: fixed, variable, and semi-variable.</span></span>

- <span data-ttu-id="77c59-177">**固定費** - 固定費は、活動レベルの変更に関係なく、短期的に変化しないコストです。</span><span class="sxs-lookup"><span data-stu-id="77c59-177">**Fixed cost** - A fixed cost is a cost that doesn't vary in the short term, regardless of changes in activity level.</span></span> <span data-ttu-id="77c59-178">たとえば、固定費は、家賃などの業務の基本的な作業経費であり、活動の増加および減少の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="77c59-178">For example, a fixed cost can be a basic operating expense of a business, such as rent, that won't be affected even if the activity level increases or decreases.</span></span>

- <span data-ttu-id="77c59-179">**変動費** - 変動費は、活動レベルの変化に従って変化します。</span><span class="sxs-lookup"><span data-stu-id="77c59-179">**Variable cost** - A variable cost changes according to changes in activity level.</span></span> <span data-ttu-id="77c59-180">たとえば、特定の直接材料の原価は、販売された各製品に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="77c59-180">For example, a specific direct materials cost is associated with each product that is sold.</span></span> <span data-ttu-id="77c59-181">販売された製品が多くなれば、直接的な材料の原価は多くなります。</span><span class="sxs-lookup"><span data-stu-id="77c59-181">The more products that are sold, the more direct materials costs there are.</span></span>

- <span data-ttu-id="77c59-182">**半変動費** - 半変動費は部分的に固定費であり、また部分的に変動費な費用です。</span><span class="sxs-lookup"><span data-stu-id="77c59-182">**Semi-variable cost** - Semi-variable costs are partly fixed and partly variable costs.</span></span> <span data-ttu-id="77c59-183">たとえば、インターネット アクセス料金には、標準的な月額のアクセス料金とブロードバンド使用料金が含まれます。</span><span class="sxs-lookup"><span data-stu-id="77c59-183">For example, an Internet access fee includes a standard monthly access fee and a broadband usage fee.</span></span> <span data-ttu-id="77c59-184">標準的な月額アクセス料金は固定費で、ブロードバンド使用料金は変動費です。</span><span class="sxs-lookup"><span data-stu-id="77c59-184">The standard monthly access fee is a fixed cost, whereas the broadband usage fee is a variable cost.</span></span>

<span data-ttu-id="77c59-185">**間接費**</span><span class="sxs-lookup"><span data-stu-id="77c59-185">**Overhead cost**</span></span>

<span data-ttu-id="77c59-186">間接費は、事業の遂行に必要な経費を示します。</span><span class="sxs-lookup"><span data-stu-id="77c59-186">Overhead costs refer to the ongoing expenses of operating a business.</span></span> <span data-ttu-id="77c59-187">これらは、特定の営業活動に直接リンクすることができない費用です。</span><span class="sxs-lookup"><span data-stu-id="77c59-187">They are the costs that can’t be linked directly to specific business activities.</span></span> <span data-ttu-id="77c59-188">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="77c59-188">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="77c59-189">会計処理手数料</span><span class="sxs-lookup"><span data-stu-id="77c59-189">Accounting fees</span></span>
-   <span data-ttu-id="77c59-190">減価償却</span><span class="sxs-lookup"><span data-stu-id="77c59-190">Depreciations</span></span>
-   <span data-ttu-id="77c59-191">保険</span><span class="sxs-lookup"><span data-stu-id="77c59-191">Insurance</span></span>
-   <span data-ttu-id="77c59-192">関心事項</span><span class="sxs-lookup"><span data-stu-id="77c59-192">Interest</span></span>
-   <span data-ttu-id="77c59-193">弁護料</span><span class="sxs-lookup"><span data-stu-id="77c59-193">Legal fees</span></span>
-   <span data-ttu-id="77c59-194">税申告</span><span class="sxs-lookup"><span data-stu-id="77c59-194">Taxes</span></span>
-   <span data-ttu-id="77c59-195">光熱費</span><span class="sxs-lookup"><span data-stu-id="77c59-195">Utilities costs</span></span>

<span data-ttu-id="77c59-196">[**原価配分**]</span><span class="sxs-lookup"><span data-stu-id="77c59-196">**Cost distribution**</span></span>

<span data-ttu-id="77c59-197">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-197">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="77c59-198">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="77c59-198">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

<span data-ttu-id="77c59-199">[**原価配賦**]</span><span class="sxs-lookup"><span data-stu-id="77c59-199">**Cost allocation**</span></span>

<span data-ttu-id="77c59-200">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="77c59-200">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="77c59-201">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="77c59-201">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="77c59-202">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-202">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="77c59-203">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="77c59-203">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="77c59-204">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-204">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="77c59-205">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="77c59-205">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="77c59-206">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-206">The allocation order is controlled by the cost control unit.</span></span>

<span data-ttu-id="77c59-207">[**原価配賦ポリシー**]</span><span class="sxs-lookup"><span data-stu-id="77c59-207">**Cost allocation policy**</span></span>

<span data-ttu-id="77c59-208">原価配賦のポリシーは、配賦する必要がある数量と金額を定義します。</span><span class="sxs-lookup"><span data-stu-id="77c59-208">A cost allocation policy defines the amounts and quantities that must be allocated.</span></span> <span data-ttu-id="77c59-209">配賦ルールには配賦元のルールが含まれます。これは配賦されている原価の決定、および原価が割り当てられるところを決定する配賦先のルールを決定します。</span><span class="sxs-lookup"><span data-stu-id="77c59-209">Allocation rules include allocation source rules, which determine the costs that are allocated, and allocation targets rules, which determine where the costs are allocated.</span></span> <span data-ttu-id="77c59-210">たとえば、融資サービスのすべての原価は、組織 (つまり、配賦ターゲット) のさまざまな部門に割り当てることができる配賦ソースです。</span><span class="sxs-lookup"><span data-stu-id="77c59-210">For example, all costs for facility services are an allocation source that can be allocated to various departments in an organization (that is, to allocation targets).</span></span>

<span data-ttu-id="77c59-211">**配賦基準**</span><span class="sxs-lookup"><span data-stu-id="77c59-211">**Allocation base**</span></span>

<span data-ttu-id="77c59-212">配賦基準は活動を測定および数量化するために使用される基準です。たとえば使用された機械の時間、消費されたキロワット時間、費やされた直接労働時間、または占有された平方フィート単位などです。</span><span class="sxs-lookup"><span data-stu-id="77c59-212">The allocation base is the basis that can be used to measure and quantify activities, such as machine hours that are used, kilowatt hours that are consumed, direct labor hours that are spent, or square footage that is occupied.</span></span> <span data-ttu-id="77c59-213">これは、1 つまたは複数のオブジェクトの原価配賦で使用されています。</span><span class="sxs-lookup"><span data-stu-id="77c59-213">It's used to allocate costs to one or more cost objects.</span></span>

<span data-ttu-id="77c59-214">**配賦原則**</span><span class="sxs-lookup"><span data-stu-id="77c59-214">**Allocation principle**</span></span>

<span data-ttu-id="77c59-215">配賦原則の 1 つは原価率で原価を割り当てることです。</span><span class="sxs-lookup"><span data-stu-id="77c59-215">One of the allocation principles is to allocate cost by cost rate.</span></span> <span data-ttu-id="77c59-216">実際の期間率または履歴レートを使用して原価を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="77c59-216">You can choose to allocate costs by using the actual period rate or a historical rate.</span></span> <span data-ttu-id="77c59-217">相互手法を使用する配賦は、実際の期間レートを使用して配賦が実行される前に、一連の並行平均化によって決定される配賦基準を保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="77c59-217">Allocation that uses the reciprocal method helps guarantee that the allocation base is determined by a series of simultaneous equations before allocation is done by using the actual period rate.</span></span>

<span data-ttu-id="77c59-218">**原価ロールアップ**</span><span class="sxs-lookup"><span data-stu-id="77c59-218">**Cost roll-up**</span></span>

<span data-ttu-id="77c59-219">原価のロールアップの目的は、特定の原価オブジェクトのすべての原価を含めることです。</span><span class="sxs-lookup"><span data-stu-id="77c59-219">The purpose of cost roll-up is to include all costs for a given cost object.</span></span> <span data-ttu-id="77c59-220">集計レベルは、ユーザーが定義します。</span><span class="sxs-lookup"><span data-stu-id="77c59-220">The level of aggregation is user-defined.</span></span> <span data-ttu-id="77c59-221">原価のロールアップを使用して、1 つの原価オブジェクトから他の原価オブジェクトに対して配賦される必要がある原価要素を集計できます。</span><span class="sxs-lookup"><span data-stu-id="77c59-221">By using cost roll-up, you can aggregate elements of costs that must be allocated from one cost object to another.</span></span> <span data-ttu-id="77c59-222">原価のロールアップを使用しない場合、原価のすべての単一要素が、1 つの原価オブジェクトから他の原価オブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="77c59-222">When cost roll-up isn't used, every single element of costs is allocated from one cost object to another.</span></span>

<span data-ttu-id="77c59-223">**原価率のポリシー**</span><span class="sxs-lookup"><span data-stu-id="77c59-223">**Cost rate policy**</span></span>

<span data-ttu-id="77c59-224">原価率は原価オブジェクトあたりの価格を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-224">The cost rate is used to calculate price per cost object.</span></span> <span data-ttu-id="77c59-225">価格の要素を理解するために、原価率のポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="77c59-225">To understand the elements of the price, you define cost rate policies.</span></span> <span data-ttu-id="77c59-226">原価率には、履歴原価率と予定原価率という 2 種類のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="77c59-226">There are two types of cost rate: historical cost rate and planned cost rate.</span></span> <span data-ttu-id="77c59-227">履歴原価率は原価オブジェクトの配賦基準に対して乗数で使用される計算された率です。</span><span class="sxs-lookup"><span data-stu-id="77c59-227">A historical cost rate is a calculated rate that is used as a multiplier for the allocation base of a cost object.</span></span> <span data-ttu-id="77c59-228">この率は、前の期間の原価配賦に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-228">The rate is calculated based on the cost allocations in the previous period.</span></span> <span data-ttu-id="77c59-229">計画されたレートは、ユーザー定義のレートです。</span><span class="sxs-lookup"><span data-stu-id="77c59-229">A planned rate is a user-defined rate.</span></span>

<span data-ttu-id="77c59-230">**分析コード階層**</span><span class="sxs-lookup"><span data-stu-id="77c59-230">**Dimensional hierarchy**</span></span>

<span data-ttu-id="77c59-231">分析コード階層は、レポート構造として使用され、配賦のルール、原価率、および原価のロールアップ、明細書の表示などのルールの定義、または Microsoft Excel のデータおよび集計済みのデータへのアクセス定義のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-231">Dimension hierarchies are used as reporting structures when you define rules for allocation, cost rate, and cost roll-up, view statements or data in Microsoft Excel, and define access to the aggregated data.</span></span> <span data-ttu-id="77c59-232">カテゴリ階層、および分類階層という 2 つの分析コード階層があります。</span><span class="sxs-lookup"><span data-stu-id="77c59-232">There are two dimension hierarchies: categorization hierarchy and classification hierarchy.</span></span> <span data-ttu-id="77c59-233">カテゴリ階層は、原価要素に基づいて定義されますが、分類階層は原価オブジェクトに基づいて定義されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-233">A categorization hierarchy is defined based on cost elements, whereas a classification hierarchy is defined based on cost objects.</span></span>

<span data-ttu-id="77c59-234">**統計分析コード**</span><span class="sxs-lookup"><span data-stu-id="77c59-234">**Statistical dimension**</span></span>

<span data-ttu-id="77c59-235">統計分析コードは、配賦または原価率の計算の基準として使用できるオブジェクトの番号または合計を表します。</span><span class="sxs-lookup"><span data-stu-id="77c59-235">A statistical dimension is the expression of a count or sum of an object that can be used as the basis for allocations or cost rate calculations.</span></span> <span data-ttu-id="77c59-236">これは手動で作成するか、またはソース システムからインポートされます。</span><span class="sxs-lookup"><span data-stu-id="77c59-236">It's either created manually or imported from source systems.</span></span> <span data-ttu-id="77c59-237">統計分析コードの例には、従業員数、各デバイスのライセンスされたソフトウェアの数、各マシンのパワー消費量、またはコスト センターの平方メートルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="77c59-237">Examples of statistical dimensions include the number of employees, the count of licensed software on each device, power consumption of each machine, or square meters for a cost center.</span></span>

<span data-ttu-id="77c59-238">**統計エントリ**</span><span class="sxs-lookup"><span data-stu-id="77c59-238">**Statistical entry**</span></span>

<span data-ttu-id="77c59-239">統計エントリは、特定の統計分析コードの記録された合計または数値を保持します。</span><span class="sxs-lookup"><span data-stu-id="77c59-239">Statistical entries hold the recorded sum or count value for a given statistical dimension.</span></span> <span data-ttu-id="77c59-240">記録された合計または数値も大きさとして参照されます。</span><span class="sxs-lookup"><span data-stu-id="77c59-240">The recorded sum or count value is also referred to as the magnitude.</span></span>




