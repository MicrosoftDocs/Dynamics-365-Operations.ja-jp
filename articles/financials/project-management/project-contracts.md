---
title: プロジェクト契約
description: このトピックでは、さまざまな種類のプロジェクトや資金調達ソースで作成できるプロジェクト契約について、また Microsoft Dynamics 365 for Finance and Operations で契約を管理しプロジェクト顧客に請求する方法についての説明と例を提供します。
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f0fcec64ce03c6e1d877fb1c8d004bb416bd95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561436"
---
# <a name="project-contracts"></a><span data-ttu-id="9c6fd-103">プロジェクト契約</span><span class="sxs-lookup"><span data-stu-id="9c6fd-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c6fd-104">この記事では、さまざまな種類のプロジェクトや資金調達ソースで作成できるプロジェクト契約について、また Microsoft Dynamics 365 for Finance and Operations で契約を管理しプロジェクト顧客に請求する方法についての説明と例を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="9c6fd-105">プロジェクト契約に作成するプロジェクト タイプで、プロジェクトの顧客への請求方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="9c6fd-106">プロジェクト契約と関連するプロジェクトは変更できますが、プロジェクト タイプは変更できません。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="9c6fd-107">プロジェクト契約により、1 つ以上のプロジェクトの請求を同時に実行できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="9c6fd-108">また、プロジェクト契約により、プロジェクト構造のすべての下位プロジェクトに対して一貫した請求手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="9c6fd-109">請求対象のすべてのプロジェクトは、プロジェクト契約に関連付けられておきます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="9c6fd-110">プロジェクト契約の設定は、そのプロジェクト契約に関連付けられているすべてのプロジェクトと下位プロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="9c6fd-111">プロジェクト契約では、資金調達の一つ以上のソースを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="9c6fd-112">したがって、複数の出資者に請求を分割でき、資金調達ソースが指定金額を超えて請求されないよう資金調達限度を設定でき、請求経費の資金調達ルールを構成できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="9c6fd-113">プロジェクト契約の資金調達</span><span class="sxs-lookup"><span data-stu-id="9c6fd-113">Funding for project contracts</span></span>
<span data-ttu-id="9c6fd-114">一部のプロジェクト契約では、複数の当事者がプロジェクト原価の資金調達の責任を共有することを指定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="9c6fd-115">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-115">Here are some examples:</span></span>

-   <span data-ttu-id="9c6fd-116">複数の部署がある大規模な顧客は、そのプロジェクト資金を部門で分割することを要望します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="9c6fd-117">会社が大規模プロジェクトの原価を外部組織と共有します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="9c6fd-118">道路プロジェクトは、2 つの自治体によって共同出資されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="9c6fd-119">橋プロジェクトは、政府補助金および私法人によって資金調達されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="9c6fd-120">Finance and Operations では、1 つのトランザクションまたはプロジェクト全体の請求を複数の顧客、付与、または組織の間で分割できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="9c6fd-121">複数の出資者が存在するプロジェクトでは、高度な資金調達プロジェクトの資金調達に寄与するすべての関係者は 資金調達ソース と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="9c6fd-122">顧客、組織、または付与が資金調達ソースとして定義されたら、1 つ以上の資金調達ルールに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="9c6fd-123">資金調達ルールには、プロジェクトのさまざまな資金調達ソースに雑費を配賦する方法を決定する基準が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="9c6fd-124">購買要求や発注書などに表示される在庫品目は分割できないため、原価金額は配分時に複数の資金調達ソース間で分割することはできません。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="9c6fd-125">したがって、資金調達ソース値は在庫払出が転記されるまで 0 (ゼロ) のままです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="9c6fd-126">在庫払出が転記されると、原価金額がプロジェクトの勘定配布ルールに従って配分されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="9c6fd-127">複数の資金調達ソース間で請求を分割しやすくするために実行できる手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="9c6fd-128">プロジェクトに対して入力されたすべてのトランザクションが、プロジェクト契約と同じ販売通貨を使用することを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="9c6fd-129">資金調達ソースが指定された金額より多くプロジェクトに対して請求されないように、資金調達限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="9c6fd-130">各作業者、品目、カテゴリ、カテゴリ グループ、およびトランザクション タイプの (またはすべてのトランザクション タイプの) 資金調達ルールと資金調達限度をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="9c6fd-131">各資金調達ルールの有効期間を定義するオプションの開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="9c6fd-132">各資金調達ソースが担当する割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="9c6fd-133">資金調達の配賦の計算による丸め誤差を担当する資金調達ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="9c6fd-134">プロジェクトの原価が外部顧客に請求され、内部の組織に請求される方法を決定するルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="9c6fd-135">追加の資金調達を取得できるか、または原価を内部で支払うように決定するまで、保留中の精算勘定のトランザクションを記録します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="9c6fd-136">トランザクションに関連付ける税グループを決定するには、プロジェクトで税グループの割り当てを検索します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="9c6fd-137">税グループの割り当てがプロジェクト レベルで行われていない場合、プロジェクト契約を検索します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="9c6fd-138">例: 複数の資金調達ソース (簡易)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="9c6fd-139">次の表に、複数の資金調達ソース間での資金配賦の管理のシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="9c6fd-140">これらのシナリオは、次の前提に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="9c6fd-141">他の資金調達ルールの基準を適用する前に、優先順位の設定が資金配賦に考慮されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="9c6fd-142">資金調達ルールが有効である期間を定義する日付範囲は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c6fd-143"><strong>シナリオ</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="9c6fd-144"><strong>資金調達ソース</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="9c6fd-145"><strong>配賦割合</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="9c6fd-146"><strong>配賦優先順位</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c6fd-147">1 つの資金調達ソースの資金を使い果たすまでそのソースに原価を配賦し、2 番目の資金調達ソースの資金を使い果たすまでそのソースに原価を配賦し、最後に 3 番目の資金調達ソースに残余原価を配賦するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-148">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="9c6fd-149">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="9c6fd-150">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="9c6fd-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-151">100%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-151">100%</span></span></li>
<li><span data-ttu-id="9c6fd-152">100%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-152">100%</span></span></li>
<li><span data-ttu-id="9c6fd-153">100%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-154">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-154">1</span></span></li>
<li><span data-ttu-id="9c6fd-155">2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-155">2</span></span></li>
<li><span data-ttu-id="9c6fd-156">3</span><span class="sxs-lookup"><span data-stu-id="9c6fd-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c6fd-157">1 つの資金調達ソースに原価の 75% を配賦し、2 番目の資金調達ソースに 25 %を配賦するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="9c6fd-158">これらの資金調達ソースのいずれかを使い果したら、3 番目の資金調達ソースからの残余原価を支払うとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-159">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="9c6fd-160">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="9c6fd-161">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="9c6fd-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-162">75%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-162">75%</span></span></li>
<li><span data-ttu-id="9c6fd-163">25%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-163">25%</span></span></li>
<li><span data-ttu-id="9c6fd-164">100%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-165">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-165">1</span></span></li>
<li><span data-ttu-id="9c6fd-166">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-166">1</span></span></li>
<li><span data-ttu-id="9c6fd-167">2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c6fd-168">1 つの資金調達ソースに原価の 75% を配賦し、2 番目の資金調達ソースに 25 %を配賦するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="9c6fd-169">いずれかの資金調達ソースを使い果したら、3 番目と 4 番目の資金調達ソース間で残余原価を分割するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-170">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="9c6fd-171">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="9c6fd-172">資金調達ソース 3</span><span class="sxs-lookup"><span data-stu-id="9c6fd-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="9c6fd-173">資金調達ソース 4</span><span class="sxs-lookup"><span data-stu-id="9c6fd-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-174">75%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-174">75%</span></span></li>
<li><span data-ttu-id="9c6fd-175">25%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-175">25%</span></span></li>
<li><span data-ttu-id="9c6fd-176">50%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-176">50%</span></span></li>
<li><span data-ttu-id="9c6fd-177">50%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-178">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-178">1</span></span></li>
<li><span data-ttu-id="9c6fd-179">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-179">1</span></span></li>
<li><span data-ttu-id="9c6fd-180">2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-180">2</span></span></li>
<li><span data-ttu-id="9c6fd-181">2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c6fd-182">原価の 25% を 1 つの資金調達ソースに、残りを 2 番目の資金調達ソースに配賦するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-183">資金調達ソース 1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="9c6fd-184">資金調達ソース 2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-185">25%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-185">25%</span></span></li>
<li><span data-ttu-id="9c6fd-186">100%</span><span class="sxs-lookup"><span data-stu-id="9c6fd-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9c6fd-187">1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-187">1</span></span></li>
<li><span data-ttu-id="9c6fd-188">2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="9c6fd-189">例: 複数の資金調達ソース (複雑)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="9c6fd-190">3 つの資金調達ソースがあり、それらのソースを次の順序で使用するとします。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="9c6fd-191">資金調達ソース 2 を使い果たすまで資金調達ソース 2 と資金調達ソース 3 を均等に使用します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="9c6fd-192">資金調達ソース 3 を使い果たすまでそのソースを使用し続けます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="9c6fd-193">資金調達ソース 3 を使い果たした後に資金調達ソース 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="9c6fd-194">この目標を達成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="9c6fd-195">資金調達ソース 2 および資金調達ソース 3 のそれぞれの金額に対して資金調達限度を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="9c6fd-196">次の資金調達ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="9c6fd-197">ルール 1 (優先順位 1): トランザクションの 50% を資金調達ソース 2 に、50% を資金調達ソース 3 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="9c6fd-198">ルール 2 (優先順位 2): トランザクションの 100% を資金調達ソース 3 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="9c6fd-199">ルール 3 (優先順位 3): トランザクションの 100% を資金調達ソース 1 に配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="9c6fd-200">トランザクションがルールおよび制限に照らしてチェックされ、任意のルールおよび限度がトランザクションに適用されるかどうかを判断するため、この設定は有効です。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="9c6fd-201">特定のルールまたは限度がトランザクションに適用されない場合には、すべてのトランザクションのルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="9c6fd-202">すべてのトランザクションのルールがすべてのトランザクションと一致します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="9c6fd-203">トランザクションと一致するルールが見つかった場合、その一致が設定済の任意の制限に対してチェックされた後にのみ、そのルールに割り当てられているた割合が最初に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="9c6fd-204">限度を満たし、資金調達ソースの資金を使い果たした場合、資金調達限度に関連付けられている資金調達ルールが無視され、適用される次のルールがプログラムでチェックされます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="9c6fd-205">場合によっては、トランザクションの一部のみをルールに従って配賦することができます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="9c6fd-206">これは、トランザクションの配賦時に限度に達したために発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="9c6fd-207">この場合、特定の金額のみがそのルール (各資金調達ソースに 50% など) に従って配賦されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="9c6fd-208">これは、このセクションで前述されているルール 1 のケースです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="9c6fd-209">残りは次の順序のルールに従って配賦されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="9c6fd-210">次の表に、このシナリオの詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c6fd-211"><strong>フォーカス</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="9c6fd-212"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="9c6fd-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c6fd-213">資金調達ルール</span><span class="sxs-lookup"><span data-stu-id="9c6fd-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-214">ルール 1 (優先順位 1): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="9c6fd-215">資金調達ソース 2 と資金調達ソース 3 をそれぞれ 50% で配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="9c6fd-216">ルール 2 (優先順位 2): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="9c6fd-217">資金調達ソース 3 を 100% で配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="9c6fd-218">ルール 3 (優先順位 2): すべてのトランザクション。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="9c6fd-219">資金調達ソース 1 を 100% で配賦します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c6fd-220">資金調達限度</span><span class="sxs-lookup"><span data-stu-id="9c6fd-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-221">資金調達ソース 1 の限度 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="9c6fd-222">資金調達ソース 2 の限度 = 500.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="9c6fd-223">資金調達ソース 3 の限度 = 750.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c6fd-224">トランザクション 1</span><span class="sxs-lookup"><span data-stu-id="9c6fd-224">Transaction 1</span></span></td>
<td><span data-ttu-id="9c6fd-225"><strong>トランザクション金額:</strong> 100.00<strong> 資金調達:</strong> トランザクションはルール 1 が適用された後に全額支払われるため、ルール 1 にのみ従って支払われます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="9c6fd-226">トランザクションは、資金調達ソース 2 と資金調達ソース 3 で均等に資金調達されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="9c6fd-227">資金調達ソース 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="9c6fd-228">資金調達ソース 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c6fd-229">トランザクション 2</span><span class="sxs-lookup"><span data-stu-id="9c6fd-229">Transaction 2</span></span></td>
<td><span data-ttu-id="9c6fd-230"><strong>トランザクション金額:</strong> 5,000 <strong>資金調達:</strong> トランザクションは、3 つのすべてのルールに従って支払われます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="9c6fd-231"><strong>ルール 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="9c6fd-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="9c6fd-232">資金調達ソース 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="9c6fd-233">資金調達ソース 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="9c6fd-234">
<strong>ルール 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="9c6fd-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="9c6fd-235">資金調達ソース 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="9c6fd-236">
<strong>ルール 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="9c6fd-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="9c6fd-237">資金調達ソース 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c6fd-238">各資金調達ソースに対して配分される合計資金</span><span class="sxs-lookup"><span data-stu-id="9c6fd-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="9c6fd-239">資金調達ソース 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="9c6fd-240">資金調達ソース 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="9c6fd-241">資金調達ソース 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="9c6fd-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="9c6fd-242">請求ルール</span><span class="sxs-lookup"><span data-stu-id="9c6fd-242">Billing rules</span></span>
<span data-ttu-id="9c6fd-243">顧客とプロジェクト契約を交渉するとき、プロジェクトの作業について顧客に請求書を送ることが可能な方法とタイミングを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="9c6fd-244">プロジェクト契約およびプロジェクトを設定したら、プロジェクトの請求ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="9c6fd-245">請求ルールは、プロジェクト契約で指定されたプロジェクトの条件に基づきます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="9c6fd-246">作成できる請求ルールは、請求ルールに関連付ける、時間/実費払または固定価格などの、プロジェクト契約とプロジェクトのタイプの条件によって異なります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="9c6fd-247">プロジェクト契約に対して複数の請求ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="9c6fd-248">同じプロジェクト契約に関連付けられており、同様の支払い条件を持つ複数のプロジェクトに1つの請求ルールを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="9c6fd-249">次のタイプの請求ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="9c6fd-250">**荷渡の単位** – 配送の単位が完了したら、顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="9c6fd-251">配送の単位は契約で定義します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="9c6fd-252">**進捗状況** – 指定のプロジェクトの割合が完了したら、顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="9c6fd-253">自動的に作業完了率を計算する請求ルールを設定するか、手動で作業完了率と金額を計算して、顧客に請求書を送付することができます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="9c6fd-254">**マイルストーン** – プロジェクトのマイルストーンに達したら、マイルストーンの総量に対して顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="9c6fd-255">**手数料** – サービスおよび、通常はサービスのコストの一定割合である管理手数料の請求書を顧客に送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="9c6fd-256">**時間/実費払** – プロジェクトで使用される時間/実費払の値に対して顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="9c6fd-257">請求ルールのすべてのタイプで、プロジェクトが合意した目標ステージに達するまで、顧客請求書から引く保留割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="9c6fd-258">支払留保割合は、プロジェクト契約で指定されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="9c6fd-259">金額は、顧客請求書の明細行の合計金額を元に計算されて、そこから差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="9c6fd-260">**時間/実費払**と**進捗状況**請求ルールには、請求可能なカテゴリを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="9c6fd-261">請求可能なカテゴリは、顧客請求書に含めるべきトランザクションを示します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="9c6fd-262">顧客に請求書を送る準備ができたら、プロジェクトの請求書の金額は請求ルールに基づいて計算され、それからプロジェクトの仮発行請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="9c6fd-263">次のセクションでは、プロジェクトの請求ルールを設定および管理する方法の例について示します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="9c6fd-264">例: 出荷される単位数に基づいて計算ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="9c6fd-265">組織は、各トレーニング セッションの原価を 10,000 で合計 5 つのトレーニング セッションを顧客の従業員に提供する契約を結びます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="9c6fd-266">各トレーニング セッション後に顧客に請求書が送付されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="9c6fd-267">契約の請求ルールを設定する際、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="9c6fd-268">配送の単位は 1 つのトレーニング セッションです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="9c6fd-269">単位価格は 1 つのトレーニング セッションごとに 10,000 ドルです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="9c6fd-270">単位の合計数は 5 つのトレーニング セッションです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="9c6fd-271">1 つのトレーニング セッションが終了したら、提供された最初の単位に対して 10,000 ドルの請求書を作成して顧客に送付できます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="9c6fd-272">例: 手動で計算された、プロジェクト完了の指定割合に基づいて計算ルールを作成する (手動計算)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="9c6fd-273">組織はソフトウェア コンサルティング会社で、顧客が開発中の製品の一部を開発することで顧客と契約を締結します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="9c6fd-274">組織では 6 か月の期間にわたってソフトウェア コードを提供することに合意しています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="9c6fd-275">顧客は作業に対して合計 100,000 ドルを組織に支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="9c6fd-276">契約で指定された、プロジェクトの作業完了割合に基づいて顧客に請求書を送付する計算ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="9c6fd-277">最初の月末に、作業完了率を決定するために顧客と会合します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="9c6fd-278">あなたと顧客がプロジェクトを確認した後、プロジェクトが 15% 完了していることを判断します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="9c6fd-279">15,000 (100,000 の 15%) で請求書を作成し、顧客に送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="9c6fd-280">例: 手動で計算された、プロジェクト完了の指定割合に基づいて計算ルールを作成する (自動計算)</span><span class="sxs-lookup"><span data-stu-id="9c6fd-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="9c6fd-281">組織は、ソフトウェア開発会社で、30,000 で顧客の給与会計パッケージを作成することに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="9c6fd-282">顧客は、作業の完了率に基づいて組織に支払うことに合意しています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="9c6fd-283">プロジェクト コストが 20,000 ドルであることを見積ります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="9c6fd-284">プロジェクト契約では、計算プロセスで使用する作業のカテゴリを指定しています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="9c6fd-285">各カテゴリに対して完了した作業の割合分について、自動的に請求金額を計算する請求ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="9c6fd-286">各カテゴリの予算を設定します:</span><span class="sxs-lookup"><span data-stu-id="9c6fd-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="9c6fd-287">**開発** – 15,000 ドルの原価、および 20,000 ドルの収益</span><span class="sxs-lookup"><span data-stu-id="9c6fd-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="9c6fd-288">**インストール** – 5,000 ドルの原価、および 10,000 ドルの収益。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="9c6fd-289">顧客請求書に初めて作成するとき、請求金額は、次の情報に基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="9c6fd-290">翌月から、プロジェクト作業者はプロジェクトのタイムシートを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="9c6fd-291">作業者の時間のコストは、開発に 5,000 ドルでインストールに 1,000 ドルです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="9c6fd-292">開発業務は、33% 完了 (実際原価 5,000ドル/予算コスト 15,000ドル)、およびインストール作業は 20% 完了 (実際原価 1,000 ドル/予算コスト 5,000ドル) しています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="9c6fd-293">8,667 ドルの請求金額が自動的に計算されます (20,000 ドルの 33% + 10,000 ドルの 20%)。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="9c6fd-294">8,667 で請求書を作成し、顧客に送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="9c6fd-295">例: マイルストーンの合意に基づいて計算ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="9c6fd-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="9c6fd-296">組織は、経営コンサルティング会社で、顧客が販売を計画する消費者製品の市場を調査することに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="9c6fd-297">顧客は、3 月に開始する 3 か月の期間、サービスを使用して、組織に 50,000 ドルを支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="9c6fd-298">プロジェクトのマイルストーンには 3 種類あります:</span><span class="sxs-lookup"><span data-stu-id="9c6fd-298">The project has three milestones:</span></span>

-   <span data-ttu-id="9c6fd-299">マイルストーン 1: 消費者データを集める – 3 月 31日</span><span class="sxs-lookup"><span data-stu-id="9c6fd-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="9c6fd-300">マイルストーン 2: 消費者データを分析する – 4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="9c6fd-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="9c6fd-301">マイルストーン 3: 製品の実行可能性の提案を提示する – 5 月 31 日</span><span class="sxs-lookup"><span data-stu-id="9c6fd-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="9c6fd-302">顧客は、最初のマイルストーンに対して組織に 10,000 ドルを、2 番目のマイルストーンに 20,000 ドルを、3 番目のマイルストーンに 20,000 ドルを支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="9c6fd-303">プロジェクト契約を設定時に、完了したマイルストーンに基づいて顧客への請求を行うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="9c6fd-304">設定された請求ルールには、次の手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="9c6fd-305">プロジェクトのマイルストーンを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-305">Define the project milestones.</span></span>
-   <span data-ttu-id="9c6fd-306">各マイルストーンの完了時に顧客に請求書を送付する量を定義します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="9c6fd-307">3 月 31 日に最初のマイルストーンが完了すると、マイルストーンを完了済みとマークして、10,000 で請求書を作成して顧客に送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="9c6fd-308">マイルストーンを完了済みとマークするまでマイルストーンの請求書を作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="9c6fd-309">例: 管理手数料とサービスに基づいて計算ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="9c6fd-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="9c6fd-310">組織は、経営コンサルティング会社で、顧客や小売企業が開発している製品の実行可能性を評価するためにマーケティング調査を行うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="9c6fd-311">契約条項に、組織は、時間/実費払に基づく調査を行う上位 3 つの経営コンサルタントのサービスを提供することが指定されています。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="9c6fd-312">顧客は、時間あたり 100 ドルに加え、プロジェクトで請求されるコンサルティング時間に対して 10% の管理手数料を支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="9c6fd-313">プロジェクト契約の設定時に、プロジェクトで請求されるコンサルティング時間に対して 10% の管理手数料を追加する請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="9c6fd-314">顧客の請求書を作成すると、顧客はコンサルティング時間について 10% の管理手数料とコストが請求されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="9c6fd-315">たとえば、3 人のコンサルタントがプロジェクトで合計 200 時間作業した場合、次の計算を基に 22,000 ドルの金額で請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="9c6fd-316">1 時間あたり 100 ドルで 200 時間 = 20,000 ドル</span><span class="sxs-lookup"><span data-stu-id="9c6fd-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="9c6fd-317">10% の管理手数料 = 2,000 ドル</span><span class="sxs-lookup"><span data-stu-id="9c6fd-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="9c6fd-318">合計請求金額 = 22,000 ドル</span><span class="sxs-lookup"><span data-stu-id="9c6fd-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="9c6fd-319">手数料が顧客に対して課税対象で、プロジェクト契約の売上税グループを選択した場合、売上税グループは、手数料の請求ルールで自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="9c6fd-320">例: 時間/実費払いの値の請求ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="9c6fd-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="9c6fd-321">組織は、ソフトウェア コンサルティング会社で、ソフトウェア開発プロジェクトで作業する 5 人のテクニカル コンサルタントを、顧客に 6 か月の間提供することを同意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="9c6fd-322">顧客は、各コンサルティング時間に対して 150 ドルと、事務用品のコストを支払うことに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="9c6fd-323">組織は、毎月月末に顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="9c6fd-324">プロジェクト契約を設定するとき、プロジェクトの時間/実費払に対して顧客に毎月請求することに合意します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="9c6fd-325">次の情報が含まれる請求ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="9c6fd-326">契約期間は 6 か月です。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-326">The contract period is six months.</span></span>
-   <span data-ttu-id="9c6fd-327">コンサルティング時間は、1 時間あたり 150 のレートで計算されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="9c6fd-328">事務用品はコストで、プロジェクトのコストは 10,000 ドル以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="9c6fd-329">プロジェクト中の各カレンダー月の最終日に顧客請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="9c6fd-330">最初の月に、合計 800 時間がプロジェクトでコンサルタントによって記録されます。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="9c6fd-331">プロジェクトに請求される事務用品のコストは 2,000 ドルです。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="9c6fd-332">したがって、月末に、事務用品の 2,000 ドルと 1 時間あたり 150 ドルの 800 時間として計算された、122,000 ドルの請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="9c6fd-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



