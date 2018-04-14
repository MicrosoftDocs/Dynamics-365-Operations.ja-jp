---
title: "間接費の計算"
description: "このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f56feac74dfe78b740342688a908d001614cffd0
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="3852d-103">間接費の計算</span><span class="sxs-lookup"><span data-stu-id="3852d-103">Overhead calculation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="3852d-104">このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3852d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="3852d-105">用語の定義</span><span class="sxs-lookup"><span data-stu-id="3852d-105">Term definition</span></span>
---------------

<span data-ttu-id="3852d-106">間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。</span><span class="sxs-lookup"><span data-stu-id="3852d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="3852d-107">間接費は、営利活動を生み出すのに不可欠な支援を提供します。</span><span class="sxs-lookup"><span data-stu-id="3852d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="3852d-108">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="3852d-109">賃料</span><span class="sxs-lookup"><span data-stu-id="3852d-109">Rent</span></span>
-   <span data-ttu-id="3852d-110">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-110">Electricity</span></span>
-   <span data-ttu-id="3852d-111">管理給与</span><span class="sxs-lookup"><span data-stu-id="3852d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="3852d-112">間接費計算の概要</span><span class="sxs-lookup"><span data-stu-id="3852d-112">Overhead calculation overview</span></span>
<span data-ttu-id="3852d-113">間接費計算は、コスト会計ポリシーを正しい順序で実行します。</span><span class="sxs-lookup"><span data-stu-id="3852d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="3852d-114">コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3852d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="3852d-115">間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3852d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="3852d-116">間接費計算が生成するコスト エントリは転記日を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3852d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="3852d-117">この転記日は、計算に使用される会計年度期間の終了日と一致します。</span><span class="sxs-lookup"><span data-stu-id="3852d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="3852d-118">固有のバージョン ID は、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="3852d-119">バージョン タイプ</span><span class="sxs-lookup"><span data-stu-id="3852d-119">Version type</span></span>
-   <span data-ttu-id="3852d-120">日時</span><span class="sxs-lookup"><span data-stu-id="3852d-120">Date and time</span></span>
-   <span data-ttu-id="3852d-121">原価会計元帳</span><span class="sxs-lookup"><span data-stu-id="3852d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="3852d-122">年度</span><span class="sxs-lookup"><span data-stu-id="3852d-122">Fiscal year</span></span>
-   <span data-ttu-id="3852d-123">会計年度期間</span><span class="sxs-lookup"><span data-stu-id="3852d-123">Fiscal period</span></span>

<span data-ttu-id="3852d-124">間接費計算は、バージョンとは無関係に実行されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="3852d-125">そのため、実際のバージョンの前に予算バージョンを計算することができます。</span><span class="sxs-lookup"><span data-stu-id="3852d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="3852d-126">間接費計算は、次の図に示されているように 4 つのステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="3852d-127">各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="3852d-128">この仕訳ヘッダーは、各計算ステップの入力データを保持します。</span><span class="sxs-lookup"><span data-stu-id="3852d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="3852d-129">ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="3852d-130">そのため、常に完全なトレーサビリティがあります。</span><span class="sxs-lookup"><span data-stu-id="3852d-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="3852d-131">[![間接費計算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="3852d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="3852d-132">電気間接費の計算および配賦</span><span class="sxs-lookup"><span data-stu-id="3852d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="3852d-133">財務会計では、電気などの一部のコストは一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="3852d-134">したがって、コスト会計には詳細な管理情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="3852d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="3852d-135">コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3852d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="3852d-136">このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3852d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="3852d-137">一般会計では、電気コストは以下の表に示されているように転記できます。</span><span class="sxs-lookup"><span data-stu-id="3852d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-138">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-139">原価部門</span><span class="sxs-lookup"><span data-stu-id="3852d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-140">主勘定</span><span class="sxs-lookup"><span data-stu-id="3852d-140">Main account</span></span></th>
<th><span data-ttu-id="3852d-141">会計通貨での金額</span><span class="sxs-lookup"><span data-stu-id="3852d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-142">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3852d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="3852d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-143">CC099</span></span></td>
<td><span data-ttu-id="3852d-144">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-144">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-145">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-145">10001</span></span></td>
<td><span data-ttu-id="3852d-146">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-146">Electricity</span></span></td>
<td><span data-ttu-id="3852d-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="3852d-148">手順 1: コスト動作計算を処理する</span><span class="sxs-lookup"><span data-stu-id="3852d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="3852d-149">既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3852d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="3852d-150">コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。</span><span class="sxs-lookup"><span data-stu-id="3852d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="3852d-151">コスト動作ルールの定義</span><span class="sxs-lookup"><span data-stu-id="3852d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="3852d-152">場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。</span><span class="sxs-lookup"><span data-stu-id="3852d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="3852d-153">電気代は多くの場合この定義と一致します。</span><span class="sxs-lookup"><span data-stu-id="3852d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="3852d-154">特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。</span><span class="sxs-lookup"><span data-stu-id="3852d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="3852d-155">たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="3852d-156">固定金額 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="3852d-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="3852d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="3852d-158">1000,01 &lt; N = 変動</span><span class="sxs-lookup"><span data-stu-id="3852d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="3852d-159">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-160">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-160">Journal</span></span></th>
<th><span data-ttu-id="3852d-161">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="3852d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3852d-162">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="3852d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3852d-163">バージョン</span><span class="sxs-lookup"><span data-stu-id="3852d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-164">00001</span><span class="sxs-lookup"><span data-stu-id="3852d-164">00001</span></span></td>
<td><span data-ttu-id="3852d-165">原価動作計算仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="3852d-166">会計年度</span><span class="sxs-lookup"><span data-stu-id="3852d-166">Fiscal</span></span></td>
<td><span data-ttu-id="3852d-167">2017</span><span class="sxs-lookup"><span data-stu-id="3852d-167">2017</span></span></td>
<td><span data-ttu-id="3852d-168">期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-168">Period 1</span></span></td>
<td><span data-ttu-id="3852d-169">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3852d-170">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="3852d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-171">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-172">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-173">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-173">Cost element</span></span></th>
<th><span data-ttu-id="3852d-174">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-175">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-176">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3852d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="3852d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-177">CC099</span></span></td>
<td><span data-ttu-id="3852d-178">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-178">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-179">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-179">10001</span></span></td>
<td><span data-ttu-id="3852d-180">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-180">Electricity</span></span></td>
<td><span data-ttu-id="3852d-181">未分類</span><span class="sxs-lookup"><span data-stu-id="3852d-181">Unclassified</span></span></td>
<td><span data-ttu-id="3852d-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3852d-183">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="3852d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-184">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-185">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-185">Cost element</span></span></th>
<th><span data-ttu-id="3852d-186">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-187">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-187">Amount</span></span></th>
<th><span data-ttu-id="3852d-188">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-189">CC099</span></span></td>
<td><span data-ttu-id="3852d-190">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-190">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-191">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-191">10001</span></span></td>
<td><span data-ttu-id="3852d-192">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-192">Electricity</span></span></td>
<td><span data-ttu-id="3852d-193">未分類</span><span class="sxs-lookup"><span data-stu-id="3852d-193">Unclassified</span></span></td>
<td><span data-ttu-id="3852d-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-194">10,000.00</span></span></td>
<td><span data-ttu-id="3852d-195">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3852d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-196">CC099</span></span></td>
<td><span data-ttu-id="3852d-197">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-197">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-198">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-198">10001</span></span></td>
<td><span data-ttu-id="3852d-199">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-199">Electricity</span></span></td>
<td><span data-ttu-id="3852d-200">未分類</span><span class="sxs-lookup"><span data-stu-id="3852d-200">Unclassified</span></span></td>
<td><span data-ttu-id="3852d-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="3852d-202">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-203">CC099</span></span></td>
<td><span data-ttu-id="3852d-204">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-204">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-205">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-205">10001</span></span></td>
<td><span data-ttu-id="3852d-206">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-206">Electricity</span></span></td>
<td><span data-ttu-id="3852d-207">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-208">1,000.00</span></span></td>
<td><span data-ttu-id="3852d-209">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-210">CC099</span></span></td>
<td><span data-ttu-id="3852d-211">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-211">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-212">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-212">10001</span></span></td>
<td><span data-ttu-id="3852d-213">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-213">Electricity</span></span></td>
<td><span data-ttu-id="3852d-214">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-214">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-215">9,000.00</span></span></td>
<td><span data-ttu-id="3852d-216">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-217">コスト動作に関する詳細については、コスト動作ポリシーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3852d-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="3852d-218">(このトピックはまだ完成していないものの、まもなく公開されます。)</span><span class="sxs-lookup"><span data-stu-id="3852d-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="3852d-219">手順 2: コスト配分計算を処理する</span><span class="sxs-lookup"><span data-stu-id="3852d-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="3852d-220">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="3852d-221">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="3852d-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="3852d-222">コスト配分ルールの定義</span><span class="sxs-lookup"><span data-stu-id="3852d-222">Define the cost distribution rule</span></span>

<span data-ttu-id="3852d-223">財務会計では、電気コストは多くの場合一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="3852d-224">コスト会計では、このアプローチは十分に詳細ではありません。</span><span class="sxs-lookup"><span data-stu-id="3852d-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="3852d-225">変動費は個々のコスト オブジェクトに公平に配分する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3852d-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="3852d-226">最も論理的な配賦基準は、電気 (Kwh) の消費です。</span><span class="sxs-lookup"><span data-stu-id="3852d-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="3852d-227">電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="3852d-228">既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3852d-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-229">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-229">Cost object</span></span></th>
<th><span data-ttu-id="3852d-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="3852d-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-231">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-231">CC001</span></span></td>
<td><span data-ttu-id="3852d-232">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-232">HR</span></span></td>
<td><span data-ttu-id="3852d-233">1.000</span><span class="sxs-lookup"><span data-stu-id="3852d-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-234">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-234">CC002</span></span></td>
<td><span data-ttu-id="3852d-235">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-235">Finance</span></span></td>
<td><span data-ttu-id="3852d-236">6,000</span><span class="sxs-lookup"><span data-stu-id="3852d-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-237">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-237">CC003</span></span></td>
<td><span data-ttu-id="3852d-238">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-238">Assembly</span></span></td>
<td><span data-ttu-id="3852d-239">0</span><span class="sxs-lookup"><span data-stu-id="3852d-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-240">次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-241">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-241">Cost object</span></span></th>
<th><span data-ttu-id="3852d-242">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-242">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-243">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-243">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-244">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-245">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-245">CC001</span></span></td>
<td><span data-ttu-id="3852d-246">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-246">HR</span></span></td>
<td><span data-ttu-id="3852d-247">1.000</span><span class="sxs-lookup"><span data-stu-id="3852d-247">1,000</span></span></td>
<td><span data-ttu-id="3852d-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3852d-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3852d-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-250">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-250">CC002</span></span></td>
<td><span data-ttu-id="3852d-251">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-251">Finance</span></span></td>
<td><span data-ttu-id="3852d-252">6,000</span><span class="sxs-lookup"><span data-stu-id="3852d-252">6,000</span></span></td>
<td><span data-ttu-id="3852d-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3852d-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3852d-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-255">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-255">CC003</span></span></td>
<td><span data-ttu-id="3852d-256">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-256">Assembly</span></span></td>
<td><span data-ttu-id="3852d-257">0</span><span class="sxs-lookup"><span data-stu-id="3852d-257">0</span></span></td>
<td><span data-ttu-id="3852d-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3852d-259">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-260">固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3852d-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="3852d-261">フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-262">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-262">Cost object</span></span></th>
<th><span data-ttu-id="3852d-263">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="3852d-263">Formula</span></span></th>
<th><span data-ttu-id="3852d-264">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-264">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-265">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-265">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-266">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-267">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-267">CC001</span></span></td>
<td><span data-ttu-id="3852d-268">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-268">HR</span></span></td>
<td><span data-ttu-id="3852d-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3852d-270">1</span><span class="sxs-lookup"><span data-stu-id="3852d-270">1</span></span></td>
<td><span data-ttu-id="3852d-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3852d-272">500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-273">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-273">CC002</span></span></td>
<td><span data-ttu-id="3852d-274">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-274">Finance</span></span></td>
<td><span data-ttu-id="3852d-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3852d-276">1</span><span class="sxs-lookup"><span data-stu-id="3852d-276">1</span></span></td>
<td><span data-ttu-id="3852d-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3852d-278">500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-279">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-279">CC003</span></span></td>
<td><span data-ttu-id="3852d-280">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-280">Assembly</span></span></td>
<td><span data-ttu-id="3852d-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3852d-282">0</span><span class="sxs-lookup"><span data-stu-id="3852d-282">0</span></span></td>
<td><span data-ttu-id="3852d-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3852d-284">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3852d-285">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-286">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-286">Journal</span></span></th>
<th><span data-ttu-id="3852d-287">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="3852d-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3852d-288">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="3852d-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3852d-289">バージョン</span><span class="sxs-lookup"><span data-stu-id="3852d-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-290">00002</span><span class="sxs-lookup"><span data-stu-id="3852d-290">00002</span></span></td>
<td><span data-ttu-id="3852d-291">コスト配分計算仕訳</span><span class="sxs-lookup"><span data-stu-id="3852d-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="3852d-292">会計年度</span><span class="sxs-lookup"><span data-stu-id="3852d-292">Fiscal</span></span></td>
<td><span data-ttu-id="3852d-293">2017</span><span class="sxs-lookup"><span data-stu-id="3852d-293">2017</span></span></td>
<td><span data-ttu-id="3852d-294">期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-294">Period 1</span></span></td>
<td><span data-ttu-id="3852d-295">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3852d-296">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="3852d-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-297">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-298">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-299">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-299">Cost element</span></span></th>
<th><span data-ttu-id="3852d-300">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-300">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-301">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-302">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-303">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-303">CC099</span></span></td>
<td><span data-ttu-id="3852d-304">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-304">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-305">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-305">10001</span></span></td>
<td><span data-ttu-id="3852d-306">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-306">Electricity</span></span></td>
<td><span data-ttu-id="3852d-307">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-307">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-308">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-309">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-310">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-310">CC099</span></span></td>
<td><span data-ttu-id="3852d-311">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-311">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-312">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-312">10001</span></span></td>
<td><span data-ttu-id="3852d-313">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-313">Electricity</span></span></td>
<td><span data-ttu-id="3852d-314">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-314">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3852d-316">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="3852d-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-317">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-318">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-318">Cost element</span></span></th>
<th><span data-ttu-id="3852d-319">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-319">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-320">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-320">Amount</span></span></th>
<th><span data-ttu-id="3852d-321">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-322">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-322">CC099</span></span></td>
<td><span data-ttu-id="3852d-323">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-323">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-324">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-324">10001</span></span></td>
<td><span data-ttu-id="3852d-325">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-325">Electricity</span></span></td>
<td><span data-ttu-id="3852d-326">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-326">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-327">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-327">-1,000.00</span></span></td>
<td><span data-ttu-id="3852d-328">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-329">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-329">CC001</span></span></td>
<td><span data-ttu-id="3852d-330">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-330">HR</span></span></td>
<td><span data-ttu-id="3852d-331">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-331">10001</span></span></td>
<td><span data-ttu-id="3852d-332">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-332">Electricity</span></span></td>
<td><span data-ttu-id="3852d-333">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-333">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-334">500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-334">500.00</span></span></td>
<td><span data-ttu-id="3852d-335">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-336">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-336">CC002</span></span></td>
<td><span data-ttu-id="3852d-337">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-337">Finance</span></span></td>
<td><span data-ttu-id="3852d-338">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-338">10001</span></span></td>
<td><span data-ttu-id="3852d-339">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-339">Electricity</span></span></td>
<td><span data-ttu-id="3852d-340">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-340">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-341">500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-341">500.00</span></span></td>
<td><span data-ttu-id="3852d-342">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-343">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-343">CC099</span></span></td>
<td><span data-ttu-id="3852d-344">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="3852d-344">Default cost center</span></span></td>
<td><span data-ttu-id="3852d-345">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-345">10001</span></span></td>
<td><span data-ttu-id="3852d-346">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-346">Electricity</span></span></td>
<td><span data-ttu-id="3852d-347">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-347">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="3852d-348">-9,000.00</span></span></td>
<td><span data-ttu-id="3852d-349">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-350">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-350">CC001</span></span></td>
<td><span data-ttu-id="3852d-351">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-351">HR</span></span></td>
<td><span data-ttu-id="3852d-352">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-352">10001</span></span></td>
<td><span data-ttu-id="3852d-353">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-353">Electricity</span></span></td>
<td><span data-ttu-id="3852d-354">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-354">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3852d-355">1,285.71</span></span></td>
<td><span data-ttu-id="3852d-356">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-357">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-357">CC002</span></span></td>
<td><span data-ttu-id="3852d-358">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-358">Finance</span></span></td>
<td><span data-ttu-id="3852d-359">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-359">10001</span></span></td>
<td><span data-ttu-id="3852d-360">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-360">Electricity</span></span></td>
<td><span data-ttu-id="3852d-361">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-361">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3852d-362">7,714.29</span></span></td>
<td><span data-ttu-id="3852d-363">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-364">コスト配分と配賦基準の詳細については、コスト配分ポリシーおよび配賦基準を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3852d-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="3852d-365">(このトピックはまだ完成していないものの、まもなく公開されます。)</span><span class="sxs-lookup"><span data-stu-id="3852d-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="3852d-366">手順 3: 間接費率の計算を処理する</span><span class="sxs-lookup"><span data-stu-id="3852d-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="3852d-367">間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="3852d-368">請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。</span><span class="sxs-lookup"><span data-stu-id="3852d-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="3852d-369">間接費率の定義</span><span class="sxs-lookup"><span data-stu-id="3852d-369">Define the overhead rate</span></span>

<span data-ttu-id="3852d-370">コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="3852d-371">HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-372">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-372">Cost object</span></span></th>
<th><span data-ttu-id="3852d-373">時間</span><span class="sxs-lookup"><span data-stu-id="3852d-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-374">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-374">Proj 1</span></span></td>
<td><span data-ttu-id="3852d-375">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-375">Project 1</span></span></td>
<td><span data-ttu-id="3852d-376">3</span><span class="sxs-lookup"><span data-stu-id="3852d-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-377">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-377">Proj 2</span></span></td>
<td><span data-ttu-id="3852d-378">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-378">Project 2</span></span></td>
<td><span data-ttu-id="3852d-379">1</span><span class="sxs-lookup"><span data-stu-id="3852d-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-380">コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。</span><span class="sxs-lookup"><span data-stu-id="3852d-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-381">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-381">Cost object</span></span></th>
<th><span data-ttu-id="3852d-382">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-382">Cost element</span></span></th>
<th><span data-ttu-id="3852d-383">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-383">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-384">単位</span><span class="sxs-lookup"><span data-stu-id="3852d-384">Units</span></span></th>
<th><span data-ttu-id="3852d-385">率</span><span class="sxs-lookup"><span data-stu-id="3852d-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-386">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-386">CC001</span></span></td>
<td><span data-ttu-id="3852d-387">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-387">HR</span></span></td>
<td><span data-ttu-id="3852d-388">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-388">10001</span></span></td>
<td><span data-ttu-id="3852d-389">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-389">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-390">1</span><span class="sxs-lookup"><span data-stu-id="3852d-390">1</span></span></td>
<td><span data-ttu-id="3852d-391">10</span><span class="sxs-lookup"><span data-stu-id="3852d-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-392">次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-393">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-393">Cost object</span></span></th>
<th><span data-ttu-id="3852d-394">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-394">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-395">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-395">Cost element</span></span></th>
<th><span data-ttu-id="3852d-396">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-396">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-397">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-398">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-398">Proj 1</span></span></td>
<td><span data-ttu-id="3852d-399">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-399">Project 1</span></span></td>
<td><span data-ttu-id="3852d-400">3</span><span class="sxs-lookup"><span data-stu-id="3852d-400">3</span></span></td>
<td><span data-ttu-id="3852d-401">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-401">10001</span></span></td>
<td><span data-ttu-id="3852d-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3852d-403">30.00</span><span class="sxs-lookup"><span data-stu-id="3852d-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-404">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-404">Proj 2</span></span></td>
<td><span data-ttu-id="3852d-405">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-405">Project 2</span></span></td>
<td><span data-ttu-id="3852d-406">1</span><span class="sxs-lookup"><span data-stu-id="3852d-406">1</span></span></td>
<td><span data-ttu-id="3852d-407">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-407">10001</span></span></td>
<td><span data-ttu-id="3852d-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3852d-409">10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3852d-410">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-411">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-411">Journal</span></span></th>
<th><span data-ttu-id="3852d-412">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="3852d-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3852d-413">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="3852d-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3852d-414">バージョン</span><span class="sxs-lookup"><span data-stu-id="3852d-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-415">00003</span><span class="sxs-lookup"><span data-stu-id="3852d-415">00003</span></span></td>
<td><span data-ttu-id="3852d-416">間接比率計算仕訳</span><span class="sxs-lookup"><span data-stu-id="3852d-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="3852d-417">会計年度</span><span class="sxs-lookup"><span data-stu-id="3852d-417">Fiscal</span></span></td>
<td><span data-ttu-id="3852d-418">2017</span><span class="sxs-lookup"><span data-stu-id="3852d-418">2017</span></span></td>
<td><span data-ttu-id="3852d-419">期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-419">Period 1</span></span></td>
<td><span data-ttu-id="3852d-420">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="3852d-421">仕訳入力 (間接比率計算のための仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="3852d-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-422">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-423">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-423">Cost object</span></span></th>
<th><span data-ttu-id="3852d-424">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-425">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-426">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-426">Proj 1</span></span></td>
<td><span data-ttu-id="3852d-427">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3852d-428">3.00</span><span class="sxs-lookup"><span data-stu-id="3852d-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-429">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-430">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-430">Proj 2</span></span></td>
<td><span data-ttu-id="3852d-431">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3852d-432">1.00</span><span class="sxs-lookup"><span data-stu-id="3852d-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3852d-433">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="3852d-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-434">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-435">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-435">Cost element</span></span></th>
<th><span data-ttu-id="3852d-436">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-436">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-437">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-437">Amount</span></span></th>
<th><span data-ttu-id="3852d-438">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="3852d-439">CC0001</span></span></td>
<td><span data-ttu-id="3852d-440">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-440">HR</span></span></td>
<td><span data-ttu-id="3852d-441">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-441">10001</span></span></td>
<td><span data-ttu-id="3852d-442">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-442">Electricity</span></span></td>
<td><span data-ttu-id="3852d-443">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-443">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="3852d-444">-30.00</span></span></td>
<td><span data-ttu-id="3852d-445">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-446">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-446">Proj 1</span></span></td>
<td><span data-ttu-id="3852d-447">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3852d-448">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-448">10001</span></span></td>
<td><span data-ttu-id="3852d-449">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-449">Electricity</span></span></td>
<td><span data-ttu-id="3852d-450">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-450">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-451">30.00</span><span class="sxs-lookup"><span data-stu-id="3852d-451">30.00</span></span></td>
<td><span data-ttu-id="3852d-452">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-453">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-453">CC001</span></span></td>
<td><span data-ttu-id="3852d-454">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-454">HR</span></span></td>
<td><span data-ttu-id="3852d-455">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-455">10001</span></span></td>
<td><span data-ttu-id="3852d-456">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-456">Electricity</span></span></td>
<td><span data-ttu-id="3852d-457">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-457">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-458">-10.00</span></span></td>
<td><span data-ttu-id="3852d-459">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-460">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-460">Proj 2</span></span></td>
<td><span data-ttu-id="3852d-461">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3852d-462">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-462">10001</span></span></td>
<td><span data-ttu-id="3852d-463">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-463">Electricity</span></span></td>
<td><span data-ttu-id="3852d-464">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-464">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-465">10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-465">10.00</span></span></td>
<td><span data-ttu-id="3852d-466">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-467">間接費率ポリシーの詳細については、間接費率ポリシーおよび配賦基準を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3852d-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="3852d-468">(このトピックはまだ完成していないものの、まもなく公開されます。)</span><span class="sxs-lookup"><span data-stu-id="3852d-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="3852d-469">手順 4: コスト配賦計算を処理する</span><span class="sxs-lookup"><span data-stu-id="3852d-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="3852d-470">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="3852d-471">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3852d-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="3852d-472">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="3852d-473">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="3852d-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="3852d-474">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="3852d-475">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3852d-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="3852d-476">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="3852d-477">[![相互手法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="3852d-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="3852d-478">コスト配賦の定義</span><span class="sxs-lookup"><span data-stu-id="3852d-478">Define the cost allocation</span></span>

<span data-ttu-id="3852d-479">次に、コストのフローを追跡する方法を説明する簡単な例を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="3852d-480">コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="3852d-481">HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-482">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-482">Cost object</span></span></th>
<th><span data-ttu-id="3852d-483">HR サービス</span><span class="sxs-lookup"><span data-stu-id="3852d-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-484">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-484">CC002</span></span></td>
<td><span data-ttu-id="3852d-485">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-485">Finance</span></span></td>
<td><span data-ttu-id="3852d-486">35</span><span class="sxs-lookup"><span data-stu-id="3852d-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-487">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-487">CC003</span></span></td>
<td><span data-ttu-id="3852d-488">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-488">Assembly</span></span></td>
<td><span data-ttu-id="3852d-489">55</span><span class="sxs-lookup"><span data-stu-id="3852d-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-490">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-490">CC004</span></span></td>
<td><span data-ttu-id="3852d-491">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-491">Packaging</span></span></td>
<td><span data-ttu-id="3852d-492">10</span><span class="sxs-lookup"><span data-stu-id="3852d-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-493">コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="3852d-494">財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-495">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-495">Cost object</span></span></th>
<th><span data-ttu-id="3852d-496">財務サービス</span><span class="sxs-lookup"><span data-stu-id="3852d-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-497">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-497">CC003</span></span></td>
<td><span data-ttu-id="3852d-498">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-498">Assembly</span></span></td>
<td><span data-ttu-id="3852d-499">65</span><span class="sxs-lookup"><span data-stu-id="3852d-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-500">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-500">CC004</span></span></td>
<td><span data-ttu-id="3852d-501">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-501">Packaging</span></span></td>
<td><span data-ttu-id="3852d-502">35</span><span class="sxs-lookup"><span data-stu-id="3852d-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-503">コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="3852d-504">組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-505">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-505">Cost object</span></span></th>
<th><span data-ttu-id="3852d-506">組み立てサービス (時間)</span><span class="sxs-lookup"><span data-stu-id="3852d-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-507">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-507">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-508">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-508">Product 1</span></span></td>
<td><span data-ttu-id="3852d-509">60</span><span class="sxs-lookup"><span data-stu-id="3852d-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-510">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-510">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-511">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-511">Product 2</span></span></td>
<td><span data-ttu-id="3852d-512">20</span><span class="sxs-lookup"><span data-stu-id="3852d-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-513">コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="3852d-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="3852d-514">梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-515">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-515">Cost object</span></span></th>
<th><span data-ttu-id="3852d-516">梱包業サービス (時間)</span><span class="sxs-lookup"><span data-stu-id="3852d-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-517">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-517">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-518">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-518">Product 1</span></span></td>
<td><span data-ttu-id="3852d-519">80</span><span class="sxs-lookup"><span data-stu-id="3852d-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-520">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-520">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-521">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-521">Product 2</span></span></td>
<td><span data-ttu-id="3852d-522">15</span><span class="sxs-lookup"><span data-stu-id="3852d-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-523">**注記:** Finance と Operations では、製品に消費される生産時間などの統計測定は、ソース データから抽出できます。</span><span class="sxs-lookup"><span data-stu-id="3852d-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="3852d-524">統計測定プロバイダーの詳細については、統計測定プロバイダー テンプレートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3852d-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="3852d-525">(このトピックはまだ完成していないものの、まもなく公開されます。) 次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-526">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-526">Cost object</span></span></th>
<th><span data-ttu-id="3852d-527">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-527">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-528">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-528">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-529">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-529">Amount</span></span></th>
<th><span data-ttu-id="3852d-530">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-531">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-531">CC002</span></span></td>
<td><span data-ttu-id="3852d-532">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-532">Finance</span></span></td>
<td><span data-ttu-id="3852d-533">35</span><span class="sxs-lookup"><span data-stu-id="3852d-533">35</span></span></td>
<td><span data-ttu-id="3852d-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3852d-535">175.00</span><span class="sxs-lookup"><span data-stu-id="3852d-535">175.00</span></span></td>
<td><span data-ttu-id="3852d-536">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-537">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-537">CC003</span></span></td>
<td><span data-ttu-id="3852d-538">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-538">Assembly</span></span></td>
<td><span data-ttu-id="3852d-539">55</span><span class="sxs-lookup"><span data-stu-id="3852d-539">55</span></span></td>
<td><span data-ttu-id="3852d-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3852d-541">275.00</span><span class="sxs-lookup"><span data-stu-id="3852d-541">275.00</span></span></td>
<td><span data-ttu-id="3852d-542">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-543">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-543">CC004</span></span></td>
<td><span data-ttu-id="3852d-544">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-544">Packaging</span></span></td>
<td><span data-ttu-id="3852d-545">10</span><span class="sxs-lookup"><span data-stu-id="3852d-545">10</span></span></td>
<td><span data-ttu-id="3852d-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3852d-547">50.00</span><span class="sxs-lookup"><span data-stu-id="3852d-547">50.00</span></span></td>
<td><span data-ttu-id="3852d-548">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-549">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-549">CC002</span></span></td>
<td><span data-ttu-id="3852d-550">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-550">Finance</span></span></td>
<td><span data-ttu-id="3852d-551">35</span><span class="sxs-lookup"><span data-stu-id="3852d-551">35</span></span></td>
<td><span data-ttu-id="3852d-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3852d-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3852d-553">436.00</span><span class="sxs-lookup"><span data-stu-id="3852d-553">436.00</span></span></td>
<td><span data-ttu-id="3852d-554">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-555">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-555">CC003</span></span></td>
<td><span data-ttu-id="3852d-556">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-556">Assembly</span></span></td>
<td><span data-ttu-id="3852d-557">55</span><span class="sxs-lookup"><span data-stu-id="3852d-557">55</span></span></td>
<td><span data-ttu-id="3852d-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3852d-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3852d-559">685.14</span><span class="sxs-lookup"><span data-stu-id="3852d-559">685.14</span></span></td>
<td><span data-ttu-id="3852d-560">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-561">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-561">CC004</span></span></td>
<td><span data-ttu-id="3852d-562">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-562">Packaging</span></span></td>
<td><span data-ttu-id="3852d-563">10</span><span class="sxs-lookup"><span data-stu-id="3852d-563">10</span></span></td>
<td><span data-ttu-id="3852d-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="3852d-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3852d-565">124.57</span><span class="sxs-lookup"><span data-stu-id="3852d-565">124.57</span></span></td>
<td><span data-ttu-id="3852d-566">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-567">次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-568">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-568">Cost object</span></span></th>
<th><span data-ttu-id="3852d-569">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-569">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-570">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-570">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-571">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-571">Amount</span></span></th>
<th><span data-ttu-id="3852d-572">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-573">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-573">CC003</span></span></td>
<td><span data-ttu-id="3852d-574">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-574">Assembly</span></span></td>
<td><span data-ttu-id="3852d-575">65</span><span class="sxs-lookup"><span data-stu-id="3852d-575">65</span></span></td>
<td><span data-ttu-id="3852d-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3852d-577">438.75</span><span class="sxs-lookup"><span data-stu-id="3852d-577">438.75</span></span></td>
<td><span data-ttu-id="3852d-578">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-579">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-579">CC004</span></span></td>
<td><span data-ttu-id="3852d-580">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-580">Packaging</span></span></td>
<td><span data-ttu-id="3852d-581">35</span><span class="sxs-lookup"><span data-stu-id="3852d-581">35</span></span></td>
<td><span data-ttu-id="3852d-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3852d-583">236.25</span><span class="sxs-lookup"><span data-stu-id="3852d-583">236.25</span></span></td>
<td><span data-ttu-id="3852d-584">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-585">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-585">CC003</span></span></td>
<td><span data-ttu-id="3852d-586">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-586">Assembly</span></span></td>
<td><span data-ttu-id="3852d-587">65</span><span class="sxs-lookup"><span data-stu-id="3852d-587">65</span></span></td>
<td><span data-ttu-id="3852d-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3852d-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3852d-589">5,297.69</span></span></td>
<td><span data-ttu-id="3852d-590">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-591">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-591">CC004</span></span></td>
<td><span data-ttu-id="3852d-592">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-592">Packaging</span></span></td>
<td><span data-ttu-id="3852d-593">35</span><span class="sxs-lookup"><span data-stu-id="3852d-593">35</span></span></td>
<td><span data-ttu-id="3852d-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="3852d-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3852d-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3852d-595">2,852.60</span></span></td>
<td><span data-ttu-id="3852d-596">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-597">次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-598">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-598">Cost object</span></span></th>
<th><span data-ttu-id="3852d-599">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-599">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-600">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-600">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-601">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-601">Amount</span></span></th>
<th><span data-ttu-id="3852d-602">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-603">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-603">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-604">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-604">Product 1</span></span></td>
<td><span data-ttu-id="3852d-605">60</span><span class="sxs-lookup"><span data-stu-id="3852d-605">60</span></span></td>
<td><span data-ttu-id="3852d-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="3852d-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3852d-607">535.31</span><span class="sxs-lookup"><span data-stu-id="3852d-607">535.31</span></span></td>
<td><span data-ttu-id="3852d-608">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-609">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-609">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-610">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-610">Product 2</span></span></td>
<td><span data-ttu-id="3852d-611">20</span><span class="sxs-lookup"><span data-stu-id="3852d-611">20</span></span></td>
<td><span data-ttu-id="3852d-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="3852d-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3852d-613">178.44</span><span class="sxs-lookup"><span data-stu-id="3852d-613">178.44</span></span></td>
<td><span data-ttu-id="3852d-614">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-615">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-615">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-616">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-616">Product 1</span></span></td>
<td><span data-ttu-id="3852d-617">60</span><span class="sxs-lookup"><span data-stu-id="3852d-617">60</span></span></td>
<td><span data-ttu-id="3852d-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="3852d-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3852d-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3852d-619">4,487.12</span></span></td>
<td><span data-ttu-id="3852d-620">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-621">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-621">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-622">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-622">Product 2</span></span></td>
<td><span data-ttu-id="3852d-623">20</span><span class="sxs-lookup"><span data-stu-id="3852d-623">20</span></span></td>
<td><span data-ttu-id="3852d-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="3852d-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3852d-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3852d-625">1,495.71</span></span></td>
<td><span data-ttu-id="3852d-626">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3852d-627">次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-628">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-628">Cost object</span></span></th>
<th><span data-ttu-id="3852d-629">大きさ</span><span class="sxs-lookup"><span data-stu-id="3852d-629">Magnitude</span></span></th>
<th><span data-ttu-id="3852d-630">配賦係数</span><span class="sxs-lookup"><span data-stu-id="3852d-630">Allocation factor</span></span></th>
<th><span data-ttu-id="3852d-631">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-631">Amount</span></span></th>
<th><span data-ttu-id="3852d-632">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-633">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-633">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-634">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-634">Product 1</span></span></td>
<td><span data-ttu-id="3852d-635">80</span><span class="sxs-lookup"><span data-stu-id="3852d-635">80</span></span></td>
<td><span data-ttu-id="3852d-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="3852d-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3852d-637">241.05</span><span class="sxs-lookup"><span data-stu-id="3852d-637">241.05</span></span></td>
<td><span data-ttu-id="3852d-638">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-639">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-639">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-640">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-640">Product 2</span></span></td>
<td><span data-ttu-id="3852d-641">15</span><span class="sxs-lookup"><span data-stu-id="3852d-641">15</span></span></td>
<td><span data-ttu-id="3852d-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="3852d-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3852d-643">45.20</span><span class="sxs-lookup"><span data-stu-id="3852d-643">45.20</span></span></td>
<td><span data-ttu-id="3852d-644">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-645">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-645">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-646">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-646">Product 1</span></span></td>
<td><span data-ttu-id="3852d-647">80</span><span class="sxs-lookup"><span data-stu-id="3852d-647">80</span></span></td>
<td><span data-ttu-id="3852d-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="3852d-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3852d-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3852d-649">2,507.09</span></span></td>
<td><span data-ttu-id="3852d-650">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-651">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-651">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-652">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-652">Product 2</span></span></td>
<td><span data-ttu-id="3852d-653">15</span><span class="sxs-lookup"><span data-stu-id="3852d-653">15</span></span></td>
<td><span data-ttu-id="3852d-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="3852d-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3852d-655">470.08</span><span class="sxs-lookup"><span data-stu-id="3852d-655">470.08</span></span></td>
<td><span data-ttu-id="3852d-656">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3852d-657">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="3852d-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-658">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-658">Journal</span></span></th>
<th><span data-ttu-id="3852d-659">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="3852d-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3852d-660">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="3852d-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3852d-661">バージョン</span><span class="sxs-lookup"><span data-stu-id="3852d-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-662">00004</span><span class="sxs-lookup"><span data-stu-id="3852d-662">00004</span></span></td>
<td><span data-ttu-id="3852d-663">原価配賦仕訳帳</span><span class="sxs-lookup"><span data-stu-id="3852d-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="3852d-664">会計年度</span><span class="sxs-lookup"><span data-stu-id="3852d-664">Fiscal</span></span></td>
<td><span data-ttu-id="3852d-665">2017</span><span class="sxs-lookup"><span data-stu-id="3852d-665">2017</span></span></td>
<td><span data-ttu-id="3852d-666">期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-666">Period 1</span></span></td>
<td><span data-ttu-id="3852d-667">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="3852d-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="3852d-668">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="3852d-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3852d-669">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-670">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-671">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-671">Cost element</span></span></th>
<th><span data-ttu-id="3852d-672">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-672">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-673">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-674">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-675">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-675">CC001</span></span></td>
<td><span data-ttu-id="3852d-676">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-676">HR</span></span></td>
<td><span data-ttu-id="3852d-677">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-677">10001</span></span></td>
<td><span data-ttu-id="3852d-678">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-678">Electricity</span></span></td>
<td><span data-ttu-id="3852d-679">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-679">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-680">500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-681">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-682">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-682">CC001</span></span></td>
<td><span data-ttu-id="3852d-683">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-683">HR</span></span></td>
<td><span data-ttu-id="3852d-684">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-684">10001</span></span></td>
<td><span data-ttu-id="3852d-685">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-685">Electricity</span></span></td>
<td><span data-ttu-id="3852d-686">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-686">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="3852d-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-688">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-689">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-689">CC002</span></span></td>
<td><span data-ttu-id="3852d-690">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-690">Finance</span></span></td>
<td><span data-ttu-id="3852d-691">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-691">10001</span></span></td>
<td><span data-ttu-id="3852d-692">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-692">Electricity</span></span></td>
<td><span data-ttu-id="3852d-693">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-693">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-694">675.00</span><span class="sxs-lookup"><span data-stu-id="3852d-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-695">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-696">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-696">CC002</span></span></td>
<td><span data-ttu-id="3852d-697">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-697">Finance</span></span></td>
<td><span data-ttu-id="3852d-698">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-698">10001</span></span></td>
<td><span data-ttu-id="3852d-699">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-699">Electricity</span></span></td>
<td><span data-ttu-id="3852d-700">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-700">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="3852d-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-702">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-703">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-703">CC003</span></span></td>
<td><span data-ttu-id="3852d-704">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-704">Assembly</span></span></td>
<td><span data-ttu-id="3852d-705">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-705">10001</span></span></td>
<td><span data-ttu-id="3852d-706">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-706">Electricity</span></span></td>
<td><span data-ttu-id="3852d-707">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-707">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-708">713.75</span><span class="sxs-lookup"><span data-stu-id="3852d-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-709">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-710">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-710">CC003</span></span></td>
<td><span data-ttu-id="3852d-711">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-711">Assembly</span></span></td>
<td><span data-ttu-id="3852d-712">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-712">10001</span></span></td>
<td><span data-ttu-id="3852d-713">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-713">Electricity</span></span></td>
<td><span data-ttu-id="3852d-714">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-714">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="3852d-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-716">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-717">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-717">CC003</span></span></td>
<td><span data-ttu-id="3852d-718">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-718">Packaging</span></span></td>
<td><span data-ttu-id="3852d-719">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-719">10001</span></span></td>
<td><span data-ttu-id="3852d-720">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-720">Electricity</span></span></td>
<td><span data-ttu-id="3852d-721">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-721">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-722">286.25</span><span class="sxs-lookup"><span data-stu-id="3852d-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-723">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-724">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-724">CC003</span></span></td>
<td><span data-ttu-id="3852d-725">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-725">Packaging</span></span></td>
<td><span data-ttu-id="3852d-726">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-726">10001</span></span></td>
<td><span data-ttu-id="3852d-727">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-727">Electricity</span></span></td>
<td><span data-ttu-id="3852d-728">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-728">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="3852d-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-730">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-731">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-731">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-732">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-732">Product 1</span></span></td>
<td><span data-ttu-id="3852d-733">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-733">10001</span></span></td>
<td><span data-ttu-id="3852d-734">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-734">Electricity</span></span></td>
<td><span data-ttu-id="3852d-735">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-735">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-736">776.36</span><span class="sxs-lookup"><span data-stu-id="3852d-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-737">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-738">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-738">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-739">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-739">Product 1</span></span></td>
<td><span data-ttu-id="3852d-740">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-740">10001</span></span></td>
<td><span data-ttu-id="3852d-741">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-741">Electricity</span></span></td>
<td><span data-ttu-id="3852d-742">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-742">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3852d-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-744">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-745">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-745">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-746">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-746">Product 1</span></span></td>
<td><span data-ttu-id="3852d-747">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-747">10001</span></span></td>
<td><span data-ttu-id="3852d-748">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-748">Electricity</span></span></td>
<td><span data-ttu-id="3852d-749">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-749">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-750">223.64</span><span class="sxs-lookup"><span data-stu-id="3852d-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-751">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="3852d-752">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-752">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-753">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-753">Product 1</span></span></td>
<td><span data-ttu-id="3852d-754">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-754">10001</span></span></td>
<td><span data-ttu-id="3852d-755">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-755">Electricity</span></span></td>
<td><span data-ttu-id="3852d-756">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-756">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3852d-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3852d-758">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="3852d-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3852d-759">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3852d-760">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-760">Cost element</span></span></th>
<th><span data-ttu-id="3852d-761">原価動作</span><span class="sxs-lookup"><span data-stu-id="3852d-761">Cost behavior</span></span></th>
<th><span data-ttu-id="3852d-762">金額</span><span class="sxs-lookup"><span data-stu-id="3852d-762">Amount</span></span></th>
<th><span data-ttu-id="3852d-763">会計日</span><span class="sxs-lookup"><span data-stu-id="3852d-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3852d-764">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-764">CC001</span></span></td>
<td><span data-ttu-id="3852d-765">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-765">HR</span></span></td>
<td><span data-ttu-id="3852d-766">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-766">10001</span></span></td>
<td><span data-ttu-id="3852d-767">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-767">Electricity</span></span></td>
<td><span data-ttu-id="3852d-768">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-768">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="3852d-769">-500.00</span></span></td>
<td><span data-ttu-id="3852d-770">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-771">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-771">CC002</span></span></td>
<td><span data-ttu-id="3852d-772">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-772">Finance</span></span></td>
<td><span data-ttu-id="3852d-773">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-773">10001</span></span></td>
<td><span data-ttu-id="3852d-774">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-774">Electricity</span></span></td>
<td><span data-ttu-id="3852d-775">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-775">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-776">175.00</span><span class="sxs-lookup"><span data-stu-id="3852d-776">175.00</span></span></td>
<td><span data-ttu-id="3852d-777">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-778">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-778">CC003</span></span></td>
<td><span data-ttu-id="3852d-779">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-779">Assembly</span></span></td>
<td><span data-ttu-id="3852d-780">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-780">10001</span></span></td>
<td><span data-ttu-id="3852d-781">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-781">Electricity</span></span></td>
<td><span data-ttu-id="3852d-782">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-782">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-783">275.00</span><span class="sxs-lookup"><span data-stu-id="3852d-783">275.00</span></span></td>
<td><span data-ttu-id="3852d-784">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-785">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-785">CC004</span></span></td>
<td><span data-ttu-id="3852d-786">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-786">Packaging</span></span></td>
<td><span data-ttu-id="3852d-787">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-787">10001</span></span></td>
<td><span data-ttu-id="3852d-788">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-788">Electricity</span></span></td>
<td><span data-ttu-id="3852d-789">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-789">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-790">50,00</span><span class="sxs-lookup"><span data-stu-id="3852d-790">50,00</span></span></td>
<td><span data-ttu-id="3852d-791">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-792">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-792">CC001</span></span></td>
<td><span data-ttu-id="3852d-793">HR</span><span class="sxs-lookup"><span data-stu-id="3852d-793">HR</span></span></td>
<td><span data-ttu-id="3852d-794">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-794">10001</span></span></td>
<td><span data-ttu-id="3852d-795">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-795">Electricity</span></span></td>
<td><span data-ttu-id="3852d-796">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-796">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="3852d-797">-1,245.71</span></span></td>
<td><span data-ttu-id="3852d-798">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-799">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-799">CC002</span></span></td>
<td><span data-ttu-id="3852d-800">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-800">Finance</span></span></td>
<td><span data-ttu-id="3852d-801">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-801">10001</span></span></td>
<td><span data-ttu-id="3852d-802">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-802">Electricity</span></span></td>
<td><span data-ttu-id="3852d-803">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-803">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-804">436.00</span><span class="sxs-lookup"><span data-stu-id="3852d-804">436.00</span></span></td>
<td><span data-ttu-id="3852d-805">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-806">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-806">CC003</span></span></td>
<td><span data-ttu-id="3852d-807">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-807">Assembly</span></span></td>
<td><span data-ttu-id="3852d-808">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-808">10001</span></span></td>
<td><span data-ttu-id="3852d-809">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-809">Electricity</span></span></td>
<td><span data-ttu-id="3852d-810">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-810">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-811">685.14</span><span class="sxs-lookup"><span data-stu-id="3852d-811">685.14</span></span></td>
<td><span data-ttu-id="3852d-812">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-813">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-813">CC004</span></span></td>
<td><span data-ttu-id="3852d-814">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-814">Packaging</span></span></td>
<td><span data-ttu-id="3852d-815">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-815">10001</span></span></td>
<td><span data-ttu-id="3852d-816">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-816">Electricity</span></span></td>
<td><span data-ttu-id="3852d-817">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-817">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-818">124.57</span><span class="sxs-lookup"><span data-stu-id="3852d-818">124.57</span></span></td>
<td><span data-ttu-id="3852d-819">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-820">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-820">CC002</span></span></td>
<td><span data-ttu-id="3852d-821">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-821">Finance</span></span></td>
<td><span data-ttu-id="3852d-822">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-822">10001</span></span></td>
<td><span data-ttu-id="3852d-823">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-823">Electricity</span></span></td>
<td><span data-ttu-id="3852d-824">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-824">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="3852d-825">-675.00</span></span></td>
<td><span data-ttu-id="3852d-826">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-827">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-827">CC003</span></span></td>
<td><span data-ttu-id="3852d-828">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-828">Assembly</span></span></td>
<td><span data-ttu-id="3852d-829">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-829">10001</span></span></td>
<td><span data-ttu-id="3852d-830">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-830">Electricity</span></span></td>
<td><span data-ttu-id="3852d-831">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-831">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-832">438.75</span><span class="sxs-lookup"><span data-stu-id="3852d-832">438.75</span></span></td>
<td><span data-ttu-id="3852d-833">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-834">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-834">CC004</span></span></td>
<td><span data-ttu-id="3852d-835">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-835">Packaging</span></span></td>
<td><span data-ttu-id="3852d-836">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-836">10001</span></span></td>
<td><span data-ttu-id="3852d-837">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-837">Electricity</span></span></td>
<td><span data-ttu-id="3852d-838">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-838">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-839">236.25</span><span class="sxs-lookup"><span data-stu-id="3852d-839">236.25</span></span></td>
<td><span data-ttu-id="3852d-840">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-841">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-841">CC002</span></span></td>
<td><span data-ttu-id="3852d-842">財務</span><span class="sxs-lookup"><span data-stu-id="3852d-842">Finance</span></span></td>
<td><span data-ttu-id="3852d-843">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-843">10001</span></span></td>
<td><span data-ttu-id="3852d-844">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-844">Electricity</span></span></td>
<td><span data-ttu-id="3852d-845">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-845">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="3852d-846">-8,150.29</span></span></td>
<td><span data-ttu-id="3852d-847">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-848">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-848">CC003</span></span></td>
<td><span data-ttu-id="3852d-849">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-849">Assembly</span></span></td>
<td><span data-ttu-id="3852d-850">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-850">10001</span></span></td>
<td><span data-ttu-id="3852d-851">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-851">Electricity</span></span></td>
<td><span data-ttu-id="3852d-852">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-852">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3852d-853">5,297.69</span></span></td>
<td><span data-ttu-id="3852d-854">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-855">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-855">CC004</span></span></td>
<td><span data-ttu-id="3852d-856">梱包業</span><span class="sxs-lookup"><span data-stu-id="3852d-856">Packaging</span></span></td>
<td><span data-ttu-id="3852d-857">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-857">10001</span></span></td>
<td><span data-ttu-id="3852d-858">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-858">Electricity</span></span></td>
<td><span data-ttu-id="3852d-859">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-859">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3852d-860">2,852.60</span></span></td>
<td><span data-ttu-id="3852d-861">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-862">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-862">CC003</span></span></td>
<td><span data-ttu-id="3852d-863">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-863">Assembly</span></span></td>
<td><span data-ttu-id="3852d-864">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-864">10001</span></span></td>
<td><span data-ttu-id="3852d-865">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-865">Electricity</span></span></td>
<td><span data-ttu-id="3852d-866">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-866">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="3852d-867">-713.75</span></span></td>
<td><span data-ttu-id="3852d-868">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-869">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-869">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-870">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-870">Product 1</span></span></td>
<td><span data-ttu-id="3852d-871">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-871">10001</span></span></td>
<td><span data-ttu-id="3852d-872">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-872">Electricity</span></span></td>
<td><span data-ttu-id="3852d-873">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-873">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-874">535.31</span><span class="sxs-lookup"><span data-stu-id="3852d-874">535.31</span></span></td>
<td><span data-ttu-id="3852d-875">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-876">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-876">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-877">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-877">Product 2</span></span></td>
<td><span data-ttu-id="3852d-878">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-878">10001</span></span></td>
<td><span data-ttu-id="3852d-879">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-879">Electricity</span></span></td>
<td><span data-ttu-id="3852d-880">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-880">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-881">178.44</span><span class="sxs-lookup"><span data-stu-id="3852d-881">178.44</span></span></td>
<td><span data-ttu-id="3852d-882">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-883">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-883">CC003</span></span></td>
<td><span data-ttu-id="3852d-884">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-884">Assembly</span></span></td>
<td><span data-ttu-id="3852d-885">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-885">10001</span></span></td>
<td><span data-ttu-id="3852d-886">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-886">Electricity</span></span></td>
<td><span data-ttu-id="3852d-887">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-887">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="3852d-888">-5,982.83</span></span></td>
<td><span data-ttu-id="3852d-889">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-890">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-890">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-891">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-891">Product 1</span></span></td>
<td><span data-ttu-id="3852d-892">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-892">10001</span></span></td>
<td><span data-ttu-id="3852d-893">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-893">Electricity</span></span></td>
<td><span data-ttu-id="3852d-894">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-894">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3852d-895">4,487.12</span></span></td>
<td><span data-ttu-id="3852d-896">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-897">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-897">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-898">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-898">Product 2</span></span></td>
<td><span data-ttu-id="3852d-899">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-899">10001</span></span></td>
<td><span data-ttu-id="3852d-900">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-900">Electricity</span></span></td>
<td><span data-ttu-id="3852d-901">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-901">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3852d-902">1,495.71</span></span></td>
<td><span data-ttu-id="3852d-903">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-904">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-904">CC003</span></span></td>
<td><span data-ttu-id="3852d-905">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-905">Assembly</span></span></td>
<td><span data-ttu-id="3852d-906">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-906">10001</span></span></td>
<td><span data-ttu-id="3852d-907">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-907">Electricity</span></span></td>
<td><span data-ttu-id="3852d-908">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-908">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="3852d-909">-286.25</span></span></td>
<td><span data-ttu-id="3852d-910">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-911">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-911">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-912">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-912">Product 1</span></span></td>
<td><span data-ttu-id="3852d-913">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-913">10001</span></span></td>
<td><span data-ttu-id="3852d-914">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-914">Electricity</span></span></td>
<td><span data-ttu-id="3852d-915">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-915">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-916">241.05</span><span class="sxs-lookup"><span data-stu-id="3852d-916">241.05</span></span></td>
<td><span data-ttu-id="3852d-917">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-918">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-918">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-919">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-919">Product 2</span></span></td>
<td><span data-ttu-id="3852d-920">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-920">10001</span></span></td>
<td><span data-ttu-id="3852d-921">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-921">Electricity</span></span></td>
<td><span data-ttu-id="3852d-922">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-922">Fixed cost</span></span></td>
<td><span data-ttu-id="3852d-923">45.20</span><span class="sxs-lookup"><span data-stu-id="3852d-923">45.20</span></span></td>
<td><span data-ttu-id="3852d-924">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-925">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-925">CC003</span></span></td>
<td><span data-ttu-id="3852d-926">組み立て</span><span class="sxs-lookup"><span data-stu-id="3852d-926">Assembly</span></span></td>
<td><span data-ttu-id="3852d-927">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-927">10001</span></span></td>
<td><span data-ttu-id="3852d-928">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-928">Electricity</span></span></td>
<td><span data-ttu-id="3852d-929">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-929">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="3852d-930">-2,977.17</span></span></td>
<td><span data-ttu-id="3852d-931">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-932">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-932">Prod 1</span></span></td>
<td><span data-ttu-id="3852d-933">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-933">Product 1</span></span></td>
<td><span data-ttu-id="3852d-934">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-934">10001</span></span></td>
<td><span data-ttu-id="3852d-935">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-935">Electricity</span></span></td>
<td><span data-ttu-id="3852d-936">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-936">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3852d-937">2,507.09</span></span></td>
<td><span data-ttu-id="3852d-938">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3852d-939">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-939">Prod 2</span></span></td>
<td><span data-ttu-id="3852d-940">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-940">Product 2</span></span></td>
<td><span data-ttu-id="3852d-941">10001</span><span class="sxs-lookup"><span data-stu-id="3852d-941">10001</span></span></td>
<td><span data-ttu-id="3852d-942">電気</span><span class="sxs-lookup"><span data-stu-id="3852d-942">Electricity</span></span></td>
<td><span data-ttu-id="3852d-943">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-943">Variable cost</span></span></td>
<td><span data-ttu-id="3852d-944">470.08</span><span class="sxs-lookup"><span data-stu-id="3852d-944">470.08</span></span></td>
<td><span data-ttu-id="3852d-945">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3852d-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="3852d-946">まとめ</span><span class="sxs-lookup"><span data-stu-id="3852d-946">Conclusion</span></span>
<span data-ttu-id="3852d-947">財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="3852d-948">したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。</span><span class="sxs-lookup"><span data-stu-id="3852d-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="3852d-949">コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。</span><span class="sxs-lookup"><span data-stu-id="3852d-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="3852d-950">各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="3852d-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="3852d-951">原価要素</span><span class="sxs-lookup"><span data-stu-id="3852d-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="3852d-952">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3852d-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="3852d-953">小計</span><span class="sxs-lookup"><span data-stu-id="3852d-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3852d-954">CC099</span><span class="sxs-lookup"><span data-stu-id="3852d-954">CC099</span></span></th>
<th><span data-ttu-id="3852d-955">CC001</span><span class="sxs-lookup"><span data-stu-id="3852d-955">CC001</span></span></th>
<th><span data-ttu-id="3852d-956">CC002</span><span class="sxs-lookup"><span data-stu-id="3852d-956">CC002</span></span></th>
<th><span data-ttu-id="3852d-957">CC003</span><span class="sxs-lookup"><span data-stu-id="3852d-957">CC003</span></span></th>
<th><span data-ttu-id="3852d-958">CC004</span><span class="sxs-lookup"><span data-stu-id="3852d-958">CC004</span></span></th>
<th><span data-ttu-id="3852d-959">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="3852d-959">Proj 1</span></span></th>
<th><span data-ttu-id="3852d-960">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="3852d-960">Proj 2</span></span></th>
<th><span data-ttu-id="3852d-961">製品 1</span><span class="sxs-lookup"><span data-stu-id="3852d-961">Prod 1</span></span></th>
<th><span data-ttu-id="3852d-962">製品 2</span><span class="sxs-lookup"><span data-stu-id="3852d-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="3852d-963">10001 電気</span><span class="sxs-lookup"><span data-stu-id="3852d-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3852d-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="3852d-973">未分類</span><span class="sxs-lookup"><span data-stu-id="3852d-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-974">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3852d-975">固定費</span><span class="sxs-lookup"><span data-stu-id="3852d-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-976">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-977">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-978">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-979">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-980">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3852d-981">776.36</span><span class="sxs-lookup"><span data-stu-id="3852d-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-982">223.64</span><span class="sxs-lookup"><span data-stu-id="3852d-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3852d-984">変動費</span><span class="sxs-lookup"><span data-stu-id="3852d-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-985">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-986">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-987">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-988">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-989">0.00</span><span class="sxs-lookup"><span data-stu-id="3852d-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-990">30.00</span><span class="sxs-lookup"><span data-stu-id="3852d-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-991">10.00</span><span class="sxs-lookup"><span data-stu-id="3852d-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3852d-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3852d-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3852d-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3852d-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3852d-995">このトピックでは、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。</span><span class="sxs-lookup"><span data-stu-id="3852d-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="3852d-996">したがって、この間接費は組織の最下位レベルに配賦されます。</span><span class="sxs-lookup"><span data-stu-id="3852d-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="3852d-997">つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。</span><span class="sxs-lookup"><span data-stu-id="3852d-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="3852d-998">コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="3852d-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="3852d-999">詳細については、コスト ロールアップ ポリシーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3852d-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="3852d-1000">(このトピックはまだ完成していないものの、まもなく公開されます。)</span><span class="sxs-lookup"><span data-stu-id="3852d-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




