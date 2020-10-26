---
title: 間接費の計算
description: このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976478"
---
# <a name="overhead-calculation"></a><span data-ttu-id="a0866-103">間接費の計算</span><span class="sxs-lookup"><span data-stu-id="a0866-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0866-104">このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a0866-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a0866-105">用語の定義</span><span class="sxs-lookup"><span data-stu-id="a0866-105">Term definition</span></span>
---------------

<span data-ttu-id="a0866-106">間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。</span><span class="sxs-lookup"><span data-stu-id="a0866-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a0866-107">間接費は、営利活動を生み出すのに不可欠な支援を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0866-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a0866-108">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a0866-109">賃料</span><span class="sxs-lookup"><span data-stu-id="a0866-109">Rent</span></span>
-   <span data-ttu-id="a0866-110">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-110">Electricity</span></span>
-   <span data-ttu-id="a0866-111">管理給与</span><span class="sxs-lookup"><span data-stu-id="a0866-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a0866-112">間接費計算の概要</span><span class="sxs-lookup"><span data-stu-id="a0866-112">Overhead calculation overview</span></span>
<span data-ttu-id="a0866-113">間接費計算は、コスト会計ポリシーを正しい順序で実行します。</span><span class="sxs-lookup"><span data-stu-id="a0866-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a0866-114">コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a0866-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a0866-115">間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a0866-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a0866-116">間接費計算が生成するコスト エントリは転記日を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a0866-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a0866-117">この転記日は、計算に使用される会計年度期間の終了日と一致します。</span><span class="sxs-lookup"><span data-stu-id="a0866-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a0866-118">固有のバージョン ID は、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a0866-119">バージョン タイプ</span><span class="sxs-lookup"><span data-stu-id="a0866-119">Version type</span></span>
-   <span data-ttu-id="a0866-120">日時</span><span class="sxs-lookup"><span data-stu-id="a0866-120">Date and time</span></span>
-   <span data-ttu-id="a0866-121">原価会計元帳</span><span class="sxs-lookup"><span data-stu-id="a0866-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a0866-122">年度</span><span class="sxs-lookup"><span data-stu-id="a0866-122">Fiscal year</span></span>
-   <span data-ttu-id="a0866-123">会計年度期間</span><span class="sxs-lookup"><span data-stu-id="a0866-123">Fiscal period</span></span>

<span data-ttu-id="a0866-124">間接費計算は、バージョンとは無関係に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a0866-125">そのため、実際のバージョンの前に予算バージョンを計算することができます。</span><span class="sxs-lookup"><span data-stu-id="a0866-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a0866-126">間接費計算は、次の図に示されているように 4 つのステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a0866-127">各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a0866-128">この仕訳ヘッダーは、各計算ステップの入力データを保持します。</span><span class="sxs-lookup"><span data-stu-id="a0866-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a0866-129">ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a0866-130">そのため、常に完全なトレーサビリティがあります。</span><span class="sxs-lookup"><span data-stu-id="a0866-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a0866-131">[![間接費計算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a0866-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a0866-132">電気間接費の計算および配賦</span><span class="sxs-lookup"><span data-stu-id="a0866-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a0866-133">財務会計では、電気などの一部のコストは一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a0866-134">したがって、コスト会計には詳細な管理情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="a0866-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a0866-135">コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0866-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a0866-136">このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0866-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a0866-137">一般会計では、電気コストは以下の表に示されているように転記できます。</span><span class="sxs-lookup"><span data-stu-id="a0866-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-138">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-139">原価部門</span><span class="sxs-lookup"><span data-stu-id="a0866-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-140">主勘定</span><span class="sxs-lookup"><span data-stu-id="a0866-140">Main account</span></span></th>
<th><span data-ttu-id="a0866-141">会計通貨での金額</span><span class="sxs-lookup"><span data-stu-id="a0866-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a0866-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a0866-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-143">CC099</span></span></td>
<td><span data-ttu-id="a0866-144">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-144">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-145">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-145">10001</span></span></td>
<td><span data-ttu-id="a0866-146">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-146">Electricity</span></span></td>
<td><span data-ttu-id="a0866-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a0866-148">手順 1: コスト動作計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a0866-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a0866-149">既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a0866-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a0866-150">コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。</span><span class="sxs-lookup"><span data-stu-id="a0866-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a0866-151">コスト動作ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a0866-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a0866-152">場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a0866-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a0866-153">電気代は多くの場合この定義と一致します。</span><span class="sxs-lookup"><span data-stu-id="a0866-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a0866-154">特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。</span><span class="sxs-lookup"><span data-stu-id="a0866-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a0866-155">たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a0866-156">固定金額 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a0866-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="a0866-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a0866-158">1000,01 &lt; N = 変動</span><span class="sxs-lookup"><span data-stu-id="a0866-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a0866-159">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-160">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-160">Journal</span></span></th>
<th><span data-ttu-id="a0866-161">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a0866-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a0866-162">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a0866-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a0866-163">バージョン</span><span class="sxs-lookup"><span data-stu-id="a0866-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-164">00001</span><span class="sxs-lookup"><span data-stu-id="a0866-164">00001</span></span></td>
<td><span data-ttu-id="a0866-165">原価動作計算仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a0866-166">会計年度</span><span class="sxs-lookup"><span data-stu-id="a0866-166">Fiscal</span></span></td>
<td><span data-ttu-id="a0866-167">2017</span><span class="sxs-lookup"><span data-stu-id="a0866-167">2017</span></span></td>
<td><span data-ttu-id="a0866-168">期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-168">Period 1</span></span></td>
<td><span data-ttu-id="a0866-169">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a0866-170">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a0866-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-171">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-172">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-173">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-173">Cost element</span></span></th>
<th><span data-ttu-id="a0866-174">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-175">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a0866-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a0866-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-177">CC099</span></span></td>
<td><span data-ttu-id="a0866-178">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-178">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-179">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-179">10001</span></span></td>
<td><span data-ttu-id="a0866-180">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-180">Electricity</span></span></td>
<td><span data-ttu-id="a0866-181">未分類</span><span class="sxs-lookup"><span data-stu-id="a0866-181">Unclassified</span></span></td>
<td><span data-ttu-id="a0866-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a0866-183">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a0866-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-184">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-185">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-185">Cost element</span></span></th>
<th><span data-ttu-id="a0866-186">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-187">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-187">Amount</span></span></th>
<th><span data-ttu-id="a0866-188">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-189">CC099</span></span></td>
<td><span data-ttu-id="a0866-190">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-190">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-191">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-191">10001</span></span></td>
<td><span data-ttu-id="a0866-192">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-192">Electricity</span></span></td>
<td><span data-ttu-id="a0866-193">未分類</span><span class="sxs-lookup"><span data-stu-id="a0866-193">Unclassified</span></span></td>
<td><span data-ttu-id="a0866-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-194">10,000.00</span></span></td>
<td><span data-ttu-id="a0866-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a0866-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-196">CC099</span></span></td>
<td><span data-ttu-id="a0866-197">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-197">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-198">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-198">10001</span></span></td>
<td><span data-ttu-id="a0866-199">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-199">Electricity</span></span></td>
<td><span data-ttu-id="a0866-200">未分類</span><span class="sxs-lookup"><span data-stu-id="a0866-200">Unclassified</span></span></td>
<td><span data-ttu-id="a0866-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a0866-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-203">CC099</span></span></td>
<td><span data-ttu-id="a0866-204">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-204">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-205">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-205">10001</span></span></td>
<td><span data-ttu-id="a0866-206">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-206">Electricity</span></span></td>
<td><span data-ttu-id="a0866-207">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-208">1,000.00</span></span></td>
<td><span data-ttu-id="a0866-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-210">CC099</span></span></td>
<td><span data-ttu-id="a0866-211">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-211">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-212">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-212">10001</span></span></td>
<td><span data-ttu-id="a0866-213">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-213">Electricity</span></span></td>
<td><span data-ttu-id="a0866-214">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-214">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-215">9,000.00</span></span></td>
<td><span data-ttu-id="a0866-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-217">詳細については、「[原価動作ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0866-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a0866-218">手順 2: コスト配分計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a0866-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a0866-219">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a0866-220">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="a0866-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a0866-221">コスト配分ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a0866-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a0866-222">財務会計では、電気コストは多くの場合一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a0866-223">コスト会計では、このアプローチは十分に詳細ではありません。</span><span class="sxs-lookup"><span data-stu-id="a0866-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a0866-224">変動費は個々のコスト オブジェクトに公平に配分する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0866-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a0866-225">最も論理的な配賦基準は、電気 (Kwh) の消費です。</span><span class="sxs-lookup"><span data-stu-id="a0866-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a0866-226">電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a0866-227">既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a0866-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-228">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-228">Cost object</span></span></th>
<th><span data-ttu-id="a0866-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="a0866-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-230">CC001</span></span></td>
<td><span data-ttu-id="a0866-231">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-231">HR</span></span></td>
<td><span data-ttu-id="a0866-232">1.000</span><span class="sxs-lookup"><span data-stu-id="a0866-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-233">CC002</span></span></td>
<td><span data-ttu-id="a0866-234">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-234">Finance</span></span></td>
<td><span data-ttu-id="a0866-235">6,000</span><span class="sxs-lookup"><span data-stu-id="a0866-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-236">CC003</span></span></td>
<td><span data-ttu-id="a0866-237">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-237">Assembly</span></span></td>
<td><span data-ttu-id="a0866-238">0</span><span class="sxs-lookup"><span data-stu-id="a0866-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-239">次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-240">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-240">Cost object</span></span></th>
<th><span data-ttu-id="a0866-241">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-241">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-242">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-243">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-244">CC001</span></span></td>
<td><span data-ttu-id="a0866-245">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-245">HR</span></span></td>
<td><span data-ttu-id="a0866-246">1.000</span><span class="sxs-lookup"><span data-stu-id="a0866-246">1,000</span></span></td>
<td><span data-ttu-id="a0866-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a0866-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a0866-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-249">CC002</span></span></td>
<td><span data-ttu-id="a0866-250">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-250">Finance</span></span></td>
<td><span data-ttu-id="a0866-251">6,000</span><span class="sxs-lookup"><span data-stu-id="a0866-251">6,000</span></span></td>
<td><span data-ttu-id="a0866-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a0866-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a0866-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-254">CC003</span></span></td>
<td><span data-ttu-id="a0866-255">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-255">Assembly</span></span></td>
<td><span data-ttu-id="a0866-256">0</span><span class="sxs-lookup"><span data-stu-id="a0866-256">0</span></span></td>
<td><span data-ttu-id="a0866-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a0866-258">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-259">固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0866-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a0866-260">フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-261">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-261">Cost object</span></span></th>
<th><span data-ttu-id="a0866-262">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="a0866-262">Formula</span></span></th>
<th><span data-ttu-id="a0866-263">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-263">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-264">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-265">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-266">CC001</span></span></td>
<td><span data-ttu-id="a0866-267">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-267">HR</span></span></td>
<td><span data-ttu-id="a0866-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a0866-269">1</span><span class="sxs-lookup"><span data-stu-id="a0866-269">1</span></span></td>
<td><span data-ttu-id="a0866-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a0866-271">500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-272">CC002</span></span></td>
<td><span data-ttu-id="a0866-273">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-273">Finance</span></span></td>
<td><span data-ttu-id="a0866-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a0866-275">1</span><span class="sxs-lookup"><span data-stu-id="a0866-275">1</span></span></td>
<td><span data-ttu-id="a0866-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a0866-277">500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-278">CC003</span></span></td>
<td><span data-ttu-id="a0866-279">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-279">Assembly</span></span></td>
<td><span data-ttu-id="a0866-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a0866-281">0</span><span class="sxs-lookup"><span data-stu-id="a0866-281">0</span></span></td>
<td><span data-ttu-id="a0866-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a0866-283">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a0866-284">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-285">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-285">Journal</span></span></th>
<th><span data-ttu-id="a0866-286">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a0866-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a0866-287">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a0866-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a0866-288">バージョン</span><span class="sxs-lookup"><span data-stu-id="a0866-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-289">00002</span><span class="sxs-lookup"><span data-stu-id="a0866-289">00002</span></span></td>
<td><span data-ttu-id="a0866-290">コスト配分計算仕訳</span><span class="sxs-lookup"><span data-stu-id="a0866-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a0866-291">会計年度</span><span class="sxs-lookup"><span data-stu-id="a0866-291">Fiscal</span></span></td>
<td><span data-ttu-id="a0866-292">2017</span><span class="sxs-lookup"><span data-stu-id="a0866-292">2017</span></span></td>
<td><span data-ttu-id="a0866-293">期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-293">Period 1</span></span></td>
<td><span data-ttu-id="a0866-294">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a0866-295">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a0866-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-296">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-297">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-298">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-298">Cost element</span></span></th>
<th><span data-ttu-id="a0866-299">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-300">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-302">CC099</span></span></td>
<td><span data-ttu-id="a0866-303">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-303">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-304">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-304">10001</span></span></td>
<td><span data-ttu-id="a0866-305">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-305">Electricity</span></span></td>
<td><span data-ttu-id="a0866-306">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-309">CC099</span></span></td>
<td><span data-ttu-id="a0866-310">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-310">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-311">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-311">10001</span></span></td>
<td><span data-ttu-id="a0866-312">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-312">Electricity</span></span></td>
<td><span data-ttu-id="a0866-313">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-313">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a0866-315">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a0866-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-316">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-317">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-317">Cost element</span></span></th>
<th><span data-ttu-id="a0866-318">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-319">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-319">Amount</span></span></th>
<th><span data-ttu-id="a0866-320">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-321">CC099</span></span></td>
<td><span data-ttu-id="a0866-322">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-322">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-323">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-323">10001</span></span></td>
<td><span data-ttu-id="a0866-324">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-324">Electricity</span></span></td>
<td><span data-ttu-id="a0866-325">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a0866-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-328">CC001</span></span></td>
<td><span data-ttu-id="a0866-329">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-329">HR</span></span></td>
<td><span data-ttu-id="a0866-330">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-330">10001</span></span></td>
<td><span data-ttu-id="a0866-331">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-331">Electricity</span></span></td>
<td><span data-ttu-id="a0866-332">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-333">500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-333">500.00</span></span></td>
<td><span data-ttu-id="a0866-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-335">CC002</span></span></td>
<td><span data-ttu-id="a0866-336">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-336">Finance</span></span></td>
<td><span data-ttu-id="a0866-337">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-337">10001</span></span></td>
<td><span data-ttu-id="a0866-338">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-338">Electricity</span></span></td>
<td><span data-ttu-id="a0866-339">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-340">500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-340">500.00</span></span></td>
<td><span data-ttu-id="a0866-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-342">CC099</span></span></td>
<td><span data-ttu-id="a0866-343">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a0866-343">Default cost center</span></span></td>
<td><span data-ttu-id="a0866-344">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-344">10001</span></span></td>
<td><span data-ttu-id="a0866-345">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-345">Electricity</span></span></td>
<td><span data-ttu-id="a0866-346">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-346">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a0866-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a0866-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-349">CC001</span></span></td>
<td><span data-ttu-id="a0866-350">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-350">HR</span></span></td>
<td><span data-ttu-id="a0866-351">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-351">10001</span></span></td>
<td><span data-ttu-id="a0866-352">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-352">Electricity</span></span></td>
<td><span data-ttu-id="a0866-353">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-353">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a0866-354">1,285.71</span></span></td>
<td><span data-ttu-id="a0866-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-356">CC002</span></span></td>
<td><span data-ttu-id="a0866-357">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-357">Finance</span></span></td>
<td><span data-ttu-id="a0866-358">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-358">10001</span></span></td>
<td><span data-ttu-id="a0866-359">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-359">Electricity</span></span></td>
<td><span data-ttu-id="a0866-360">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-360">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a0866-361">7,714.29</span></span></td>
<td><span data-ttu-id="a0866-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-363">詳細については、「[原価配分ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0866-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a0866-364">手順 3: 間接費率の計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a0866-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a0866-365">間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a0866-366">請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。</span><span class="sxs-lookup"><span data-stu-id="a0866-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a0866-367">間接費率の定義</span><span class="sxs-lookup"><span data-stu-id="a0866-367">Define the overhead rate</span></span>

<span data-ttu-id="a0866-368">コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a0866-369">HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-370">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-370">Cost object</span></span></th>
<th><span data-ttu-id="a0866-371">時間</span><span class="sxs-lookup"><span data-stu-id="a0866-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-372">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-372">Proj 1</span></span></td>
<td><span data-ttu-id="a0866-373">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-373">Project 1</span></span></td>
<td><span data-ttu-id="a0866-374">3</span><span class="sxs-lookup"><span data-stu-id="a0866-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-375">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-375">Proj 2</span></span></td>
<td><span data-ttu-id="a0866-376">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-376">Project 2</span></span></td>
<td><span data-ttu-id="a0866-377">1</span><span class="sxs-lookup"><span data-stu-id="a0866-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-378">コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。</span><span class="sxs-lookup"><span data-stu-id="a0866-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-379">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-379">Cost object</span></span></th>
<th><span data-ttu-id="a0866-380">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-380">Cost element</span></span></th>
<th><span data-ttu-id="a0866-381">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-382">単位</span><span class="sxs-lookup"><span data-stu-id="a0866-382">Units</span></span></th>
<th><span data-ttu-id="a0866-383">率</span><span class="sxs-lookup"><span data-stu-id="a0866-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-384">CC001</span></span></td>
<td><span data-ttu-id="a0866-385">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-385">HR</span></span></td>
<td><span data-ttu-id="a0866-386">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-386">10001</span></span></td>
<td><span data-ttu-id="a0866-387">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-387">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-388">1</span><span class="sxs-lookup"><span data-stu-id="a0866-388">1</span></span></td>
<td><span data-ttu-id="a0866-389">10</span><span class="sxs-lookup"><span data-stu-id="a0866-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-390">次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-391">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-391">Cost object</span></span></th>
<th><span data-ttu-id="a0866-392">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-392">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-393">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-393">Cost element</span></span></th>
<th><span data-ttu-id="a0866-394">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-395">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-396">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-396">Proj 1</span></span></td>
<td><span data-ttu-id="a0866-397">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-397">Project 1</span></span></td>
<td><span data-ttu-id="a0866-398">3</span><span class="sxs-lookup"><span data-stu-id="a0866-398">3</span></span></td>
<td><span data-ttu-id="a0866-399">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-399">10001</span></span></td>
<td><span data-ttu-id="a0866-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a0866-401">30.00</span><span class="sxs-lookup"><span data-stu-id="a0866-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-402">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-402">Proj 2</span></span></td>
<td><span data-ttu-id="a0866-403">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-403">Project 2</span></span></td>
<td><span data-ttu-id="a0866-404">1</span><span class="sxs-lookup"><span data-stu-id="a0866-404">1</span></span></td>
<td><span data-ttu-id="a0866-405">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-405">10001</span></span></td>
<td><span data-ttu-id="a0866-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a0866-407">10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a0866-408">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-409">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-409">Journal</span></span></th>
<th><span data-ttu-id="a0866-410">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a0866-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a0866-411">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a0866-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a0866-412">バージョン</span><span class="sxs-lookup"><span data-stu-id="a0866-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-413">00003</span><span class="sxs-lookup"><span data-stu-id="a0866-413">00003</span></span></td>
<td><span data-ttu-id="a0866-414">間接比率計算仕訳</span><span class="sxs-lookup"><span data-stu-id="a0866-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a0866-415">会計年度</span><span class="sxs-lookup"><span data-stu-id="a0866-415">Fiscal</span></span></td>
<td><span data-ttu-id="a0866-416">2017</span><span class="sxs-lookup"><span data-stu-id="a0866-416">2017</span></span></td>
<td><span data-ttu-id="a0866-417">期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-417">Period 1</span></span></td>
<td><span data-ttu-id="a0866-418">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a0866-419">仕訳入力 (間接比率計算のための仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a0866-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-420">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-421">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-421">Cost object</span></span></th>
<th><span data-ttu-id="a0866-422">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-424">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-424">Proj 1</span></span></td>
<td><span data-ttu-id="a0866-425">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a0866-426">3.00</span><span class="sxs-lookup"><span data-stu-id="a0866-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-428">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-428">Proj 2</span></span></td>
<td><span data-ttu-id="a0866-429">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a0866-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a0866-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a0866-431">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a0866-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-432">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-433">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-433">Cost element</span></span></th>
<th><span data-ttu-id="a0866-434">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-435">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-435">Amount</span></span></th>
<th><span data-ttu-id="a0866-436">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a0866-437">CC0001</span></span></td>
<td><span data-ttu-id="a0866-438">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-438">HR</span></span></td>
<td><span data-ttu-id="a0866-439">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-439">10001</span></span></td>
<td><span data-ttu-id="a0866-440">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-440">Electricity</span></span></td>
<td><span data-ttu-id="a0866-441">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-441">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="a0866-442">-30.00</span></span></td>
<td><span data-ttu-id="a0866-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-444">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-444">Proj 1</span></span></td>
<td><span data-ttu-id="a0866-445">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a0866-446">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-446">10001</span></span></td>
<td><span data-ttu-id="a0866-447">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-447">Electricity</span></span></td>
<td><span data-ttu-id="a0866-448">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-448">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-449">30.00</span><span class="sxs-lookup"><span data-stu-id="a0866-449">30.00</span></span></td>
<td><span data-ttu-id="a0866-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-451">CC001</span></span></td>
<td><span data-ttu-id="a0866-452">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-452">HR</span></span></td>
<td><span data-ttu-id="a0866-453">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-453">10001</span></span></td>
<td><span data-ttu-id="a0866-454">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-454">Electricity</span></span></td>
<td><span data-ttu-id="a0866-455">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-455">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-456">-10.00</span></span></td>
<td><span data-ttu-id="a0866-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-458">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-458">Proj 2</span></span></td>
<td><span data-ttu-id="a0866-459">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a0866-460">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-460">10001</span></span></td>
<td><span data-ttu-id="a0866-461">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-461">Electricity</span></span></td>
<td><span data-ttu-id="a0866-462">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-462">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-463">10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-463">10.00</span></span></td>
<td><span data-ttu-id="a0866-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-465">詳細については、「[間接費計算を実行する](cost-rollup.md#perform-overhead-calculation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0866-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a0866-466">手順 4: コスト配賦計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a0866-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a0866-467">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a0866-468">Finance では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a0866-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="a0866-469">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a0866-470">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="a0866-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a0866-471">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a0866-472">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a0866-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a0866-473">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a0866-474">[![相互手法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a0866-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a0866-475">コスト配賦の定義</span><span class="sxs-lookup"><span data-stu-id="a0866-475">Define the cost allocation</span></span>

<span data-ttu-id="a0866-476">次に、コストのフローを追跡する方法を説明する簡単な例を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a0866-477">コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a0866-478">HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-479">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-479">Cost object</span></span></th>
<th><span data-ttu-id="a0866-480">HR サービス</span><span class="sxs-lookup"><span data-stu-id="a0866-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-481">CC002</span></span></td>
<td><span data-ttu-id="a0866-482">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-482">Finance</span></span></td>
<td><span data-ttu-id="a0866-483">35</span><span class="sxs-lookup"><span data-stu-id="a0866-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-484">CC003</span></span></td>
<td><span data-ttu-id="a0866-485">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-485">Assembly</span></span></td>
<td><span data-ttu-id="a0866-486">55</span><span class="sxs-lookup"><span data-stu-id="a0866-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-487">CC004</span></span></td>
<td><span data-ttu-id="a0866-488">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-488">Packaging</span></span></td>
<td><span data-ttu-id="a0866-489">10</span><span class="sxs-lookup"><span data-stu-id="a0866-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-490">コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a0866-491">財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-492">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-492">Cost object</span></span></th>
<th><span data-ttu-id="a0866-493">財務サービス</span><span class="sxs-lookup"><span data-stu-id="a0866-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-494">CC003</span></span></td>
<td><span data-ttu-id="a0866-495">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-495">Assembly</span></span></td>
<td><span data-ttu-id="a0866-496">65</span><span class="sxs-lookup"><span data-stu-id="a0866-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-497">CC004</span></span></td>
<td><span data-ttu-id="a0866-498">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-498">Packaging</span></span></td>
<td><span data-ttu-id="a0866-499">35</span><span class="sxs-lookup"><span data-stu-id="a0866-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-500">コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a0866-501">組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-502">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-502">Cost object</span></span></th>
<th><span data-ttu-id="a0866-503">組み立てサービス (時間)</span><span class="sxs-lookup"><span data-stu-id="a0866-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-504">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-504">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-505">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-505">Product 1</span></span></td>
<td><span data-ttu-id="a0866-506">60</span><span class="sxs-lookup"><span data-stu-id="a0866-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-507">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-507">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-508">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-508">Product 2</span></span></td>
<td><span data-ttu-id="a0866-509">20</span><span class="sxs-lookup"><span data-stu-id="a0866-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-510">コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a0866-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a0866-511">梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-512">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-512">Cost object</span></span></th>
<th><span data-ttu-id="a0866-513">梱包業サービス (時間)</span><span class="sxs-lookup"><span data-stu-id="a0866-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-514">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-514">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-515">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-515">Product 1</span></span></td>
<td><span data-ttu-id="a0866-516">80</span><span class="sxs-lookup"><span data-stu-id="a0866-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-517">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-517">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-518">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-518">Product 2</span></span></td>
<td><span data-ttu-id="a0866-519">15</span><span class="sxs-lookup"><span data-stu-id="a0866-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a0866-520">製品が消費する生産時間などの統計測定は、ソース データから抽出できます。</span><span class="sxs-lookup"><span data-stu-id="a0866-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a0866-521">詳細については、「[統計測定プロバイダー テンプレート](statistical-measure-provider-template.md#statistical-measure-provider-template)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0866-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a0866-522">次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-523">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-523">Cost object</span></span></th>
<th><span data-ttu-id="a0866-524">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-524">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-525">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-526">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-526">Amount</span></span></th>
<th><span data-ttu-id="a0866-527">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-528">CC002</span></span></td>
<td><span data-ttu-id="a0866-529">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-529">Finance</span></span></td>
<td><span data-ttu-id="a0866-530">35</span><span class="sxs-lookup"><span data-stu-id="a0866-530">35</span></span></td>
<td><span data-ttu-id="a0866-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a0866-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a0866-532">175.00</span></span></td>
<td><span data-ttu-id="a0866-533">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-534">CC003</span></span></td>
<td><span data-ttu-id="a0866-535">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-535">Assembly</span></span></td>
<td><span data-ttu-id="a0866-536">55</span><span class="sxs-lookup"><span data-stu-id="a0866-536">55</span></span></td>
<td><span data-ttu-id="a0866-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a0866-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a0866-538">275.00</span></span></td>
<td><span data-ttu-id="a0866-539">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-540">CC004</span></span></td>
<td><span data-ttu-id="a0866-541">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-541">Packaging</span></span></td>
<td><span data-ttu-id="a0866-542">10</span><span class="sxs-lookup"><span data-stu-id="a0866-542">10</span></span></td>
<td><span data-ttu-id="a0866-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a0866-544">50.00</span><span class="sxs-lookup"><span data-stu-id="a0866-544">50.00</span></span></td>
<td><span data-ttu-id="a0866-545">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-546">CC002</span></span></td>
<td><span data-ttu-id="a0866-547">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-547">Finance</span></span></td>
<td><span data-ttu-id="a0866-548">35</span><span class="sxs-lookup"><span data-stu-id="a0866-548">35</span></span></td>
<td><span data-ttu-id="a0866-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a0866-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a0866-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a0866-550">436.00</span></span></td>
<td><span data-ttu-id="a0866-551">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-552">CC003</span></span></td>
<td><span data-ttu-id="a0866-553">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-553">Assembly</span></span></td>
<td><span data-ttu-id="a0866-554">55</span><span class="sxs-lookup"><span data-stu-id="a0866-554">55</span></span></td>
<td><span data-ttu-id="a0866-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a0866-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a0866-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a0866-556">685.14</span></span></td>
<td><span data-ttu-id="a0866-557">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-558">CC004</span></span></td>
<td><span data-ttu-id="a0866-559">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-559">Packaging</span></span></td>
<td><span data-ttu-id="a0866-560">10</span><span class="sxs-lookup"><span data-stu-id="a0866-560">10</span></span></td>
<td><span data-ttu-id="a0866-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a0866-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a0866-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a0866-562">124.57</span></span></td>
<td><span data-ttu-id="a0866-563">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-564">次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-565">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-565">Cost object</span></span></th>
<th><span data-ttu-id="a0866-566">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-566">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-567">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-568">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-568">Amount</span></span></th>
<th><span data-ttu-id="a0866-569">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-570">CC003</span></span></td>
<td><span data-ttu-id="a0866-571">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-571">Assembly</span></span></td>
<td><span data-ttu-id="a0866-572">65</span><span class="sxs-lookup"><span data-stu-id="a0866-572">65</span></span></td>
<td><span data-ttu-id="a0866-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a0866-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a0866-574">438.75</span></span></td>
<td><span data-ttu-id="a0866-575">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-576">CC004</span></span></td>
<td><span data-ttu-id="a0866-577">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-577">Packaging</span></span></td>
<td><span data-ttu-id="a0866-578">35</span><span class="sxs-lookup"><span data-stu-id="a0866-578">35</span></span></td>
<td><span data-ttu-id="a0866-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a0866-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a0866-580">236.25</span></span></td>
<td><span data-ttu-id="a0866-581">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-582">CC003</span></span></td>
<td><span data-ttu-id="a0866-583">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-583">Assembly</span></span></td>
<td><span data-ttu-id="a0866-584">65</span><span class="sxs-lookup"><span data-stu-id="a0866-584">65</span></span></td>
<td><span data-ttu-id="a0866-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a0866-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a0866-586">5,297.69</span></span></td>
<td><span data-ttu-id="a0866-587">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-588">CC004</span></span></td>
<td><span data-ttu-id="a0866-589">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-589">Packaging</span></span></td>
<td><span data-ttu-id="a0866-590">35</span><span class="sxs-lookup"><span data-stu-id="a0866-590">35</span></span></td>
<td><span data-ttu-id="a0866-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a0866-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a0866-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a0866-592">2,852.60</span></span></td>
<td><span data-ttu-id="a0866-593">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-594">次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-595">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-595">Cost object</span></span></th>
<th><span data-ttu-id="a0866-596">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-596">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-597">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-598">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-598">Amount</span></span></th>
<th><span data-ttu-id="a0866-599">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-600">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-600">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-601">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-601">Product 1</span></span></td>
<td><span data-ttu-id="a0866-602">60</span><span class="sxs-lookup"><span data-stu-id="a0866-602">60</span></span></td>
<td><span data-ttu-id="a0866-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a0866-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a0866-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a0866-604">535.31</span></span></td>
<td><span data-ttu-id="a0866-605">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-606">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-606">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-607">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-607">Product 2</span></span></td>
<td><span data-ttu-id="a0866-608">20</span><span class="sxs-lookup"><span data-stu-id="a0866-608">20</span></span></td>
<td><span data-ttu-id="a0866-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a0866-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a0866-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a0866-610">178.44</span></span></td>
<td><span data-ttu-id="a0866-611">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-612">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-612">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-613">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-613">Product 1</span></span></td>
<td><span data-ttu-id="a0866-614">60</span><span class="sxs-lookup"><span data-stu-id="a0866-614">60</span></span></td>
<td><span data-ttu-id="a0866-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a0866-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a0866-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a0866-616">4,487.12</span></span></td>
<td><span data-ttu-id="a0866-617">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-618">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-618">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-619">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-619">Product 2</span></span></td>
<td><span data-ttu-id="a0866-620">20</span><span class="sxs-lookup"><span data-stu-id="a0866-620">20</span></span></td>
<td><span data-ttu-id="a0866-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a0866-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a0866-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a0866-622">1,495.71</span></span></td>
<td><span data-ttu-id="a0866-623">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a0866-624">次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-625">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-625">Cost object</span></span></th>
<th><span data-ttu-id="a0866-626">大きさ</span><span class="sxs-lookup"><span data-stu-id="a0866-626">Magnitude</span></span></th>
<th><span data-ttu-id="a0866-627">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a0866-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a0866-628">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-628">Amount</span></span></th>
<th><span data-ttu-id="a0866-629">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-630">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-630">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-631">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-631">Product 1</span></span></td>
<td><span data-ttu-id="a0866-632">80</span><span class="sxs-lookup"><span data-stu-id="a0866-632">80</span></span></td>
<td><span data-ttu-id="a0866-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a0866-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a0866-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a0866-634">241.05</span></span></td>
<td><span data-ttu-id="a0866-635">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-636">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-636">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-637">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-637">Product 2</span></span></td>
<td><span data-ttu-id="a0866-638">15</span><span class="sxs-lookup"><span data-stu-id="a0866-638">15</span></span></td>
<td><span data-ttu-id="a0866-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a0866-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a0866-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a0866-640">45.20</span></span></td>
<td><span data-ttu-id="a0866-641">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-642">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-642">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-643">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-643">Product 1</span></span></td>
<td><span data-ttu-id="a0866-644">80</span><span class="sxs-lookup"><span data-stu-id="a0866-644">80</span></span></td>
<td><span data-ttu-id="a0866-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a0866-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a0866-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a0866-646">2,507.09</span></span></td>
<td><span data-ttu-id="a0866-647">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-648">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-648">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-649">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-649">Product 2</span></span></td>
<td><span data-ttu-id="a0866-650">15</span><span class="sxs-lookup"><span data-stu-id="a0866-650">15</span></span></td>
<td><span data-ttu-id="a0866-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a0866-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a0866-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a0866-652">470.08</span></span></td>
<td><span data-ttu-id="a0866-653">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a0866-654">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a0866-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-655">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-655">Journal</span></span></th>
<th><span data-ttu-id="a0866-656">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a0866-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a0866-657">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a0866-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a0866-658">バージョン</span><span class="sxs-lookup"><span data-stu-id="a0866-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-659">00004</span><span class="sxs-lookup"><span data-stu-id="a0866-659">00004</span></span></td>
<td><span data-ttu-id="a0866-660">原価配賦仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a0866-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a0866-661">会計年度</span><span class="sxs-lookup"><span data-stu-id="a0866-661">Fiscal</span></span></td>
<td><span data-ttu-id="a0866-662">2017</span><span class="sxs-lookup"><span data-stu-id="a0866-662">2017</span></span></td>
<td><span data-ttu-id="a0866-663">期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-663">Period 1</span></span></td>
<td><span data-ttu-id="a0866-664">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a0866-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a0866-665">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="a0866-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a0866-666">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-667">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-668">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-668">Cost element</span></span></th>
<th><span data-ttu-id="a0866-669">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-670">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-672">CC001</span></span></td>
<td><span data-ttu-id="a0866-673">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-673">HR</span></span></td>
<td><span data-ttu-id="a0866-674">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-674">10001</span></span></td>
<td><span data-ttu-id="a0866-675">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-675">Electricity</span></span></td>
<td><span data-ttu-id="a0866-676">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-677">500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-679">CC001</span></span></td>
<td><span data-ttu-id="a0866-680">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-680">HR</span></span></td>
<td><span data-ttu-id="a0866-681">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-681">10001</span></span></td>
<td><span data-ttu-id="a0866-682">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-682">Electricity</span></span></td>
<td><span data-ttu-id="a0866-683">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-683">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a0866-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-686">CC002</span></span></td>
<td><span data-ttu-id="a0866-687">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-687">Finance</span></span></td>
<td><span data-ttu-id="a0866-688">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-688">10001</span></span></td>
<td><span data-ttu-id="a0866-689">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-689">Electricity</span></span></td>
<td><span data-ttu-id="a0866-690">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a0866-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-693">CC002</span></span></td>
<td><span data-ttu-id="a0866-694">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-694">Finance</span></span></td>
<td><span data-ttu-id="a0866-695">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-695">10001</span></span></td>
<td><span data-ttu-id="a0866-696">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-696">Electricity</span></span></td>
<td><span data-ttu-id="a0866-697">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-697">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a0866-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-700">CC003</span></span></td>
<td><span data-ttu-id="a0866-701">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-701">Assembly</span></span></td>
<td><span data-ttu-id="a0866-702">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-702">10001</span></span></td>
<td><span data-ttu-id="a0866-703">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-703">Electricity</span></span></td>
<td><span data-ttu-id="a0866-704">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a0866-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-707">CC003</span></span></td>
<td><span data-ttu-id="a0866-708">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-708">Assembly</span></span></td>
<td><span data-ttu-id="a0866-709">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-709">10001</span></span></td>
<td><span data-ttu-id="a0866-710">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-710">Electricity</span></span></td>
<td><span data-ttu-id="a0866-711">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-711">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a0866-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-714">CC003</span></span></td>
<td><span data-ttu-id="a0866-715">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-715">Packaging</span></span></td>
<td><span data-ttu-id="a0866-716">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-716">10001</span></span></td>
<td><span data-ttu-id="a0866-717">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-717">Electricity</span></span></td>
<td><span data-ttu-id="a0866-718">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a0866-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-721">CC003</span></span></td>
<td><span data-ttu-id="a0866-722">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-722">Packaging</span></span></td>
<td><span data-ttu-id="a0866-723">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-723">10001</span></span></td>
<td><span data-ttu-id="a0866-724">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-724">Electricity</span></span></td>
<td><span data-ttu-id="a0866-725">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-725">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a0866-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-728">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-728">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-729">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-729">Product 1</span></span></td>
<td><span data-ttu-id="a0866-730">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-730">10001</span></span></td>
<td><span data-ttu-id="a0866-731">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-731">Electricity</span></span></td>
<td><span data-ttu-id="a0866-732">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a0866-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-735">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-735">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-736">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-736">Product 1</span></span></td>
<td><span data-ttu-id="a0866-737">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-737">10001</span></span></td>
<td><span data-ttu-id="a0866-738">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-738">Electricity</span></span></td>
<td><span data-ttu-id="a0866-739">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-739">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a0866-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-742">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-742">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-743">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-743">Product 1</span></span></td>
<td><span data-ttu-id="a0866-744">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-744">10001</span></span></td>
<td><span data-ttu-id="a0866-745">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-745">Electricity</span></span></td>
<td><span data-ttu-id="a0866-746">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a0866-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a0866-749">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-749">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-750">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-750">Product 1</span></span></td>
<td><span data-ttu-id="a0866-751">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-751">10001</span></span></td>
<td><span data-ttu-id="a0866-752">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-752">Electricity</span></span></td>
<td><span data-ttu-id="a0866-753">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-753">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a0866-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a0866-755">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a0866-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a0866-756">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a0866-757">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-757">Cost element</span></span></th>
<th><span data-ttu-id="a0866-758">原価動作</span><span class="sxs-lookup"><span data-stu-id="a0866-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a0866-759">金額</span><span class="sxs-lookup"><span data-stu-id="a0866-759">Amount</span></span></th>
<th><span data-ttu-id="a0866-760">会計日</span><span class="sxs-lookup"><span data-stu-id="a0866-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a0866-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-761">CC001</span></span></td>
<td><span data-ttu-id="a0866-762">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-762">HR</span></span></td>
<td><span data-ttu-id="a0866-763">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-763">10001</span></span></td>
<td><span data-ttu-id="a0866-764">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-764">Electricity</span></span></td>
<td><span data-ttu-id="a0866-765">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="a0866-766">-500.00</span></span></td>
<td><span data-ttu-id="a0866-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-768">CC002</span></span></td>
<td><span data-ttu-id="a0866-769">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-769">Finance</span></span></td>
<td><span data-ttu-id="a0866-770">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-770">10001</span></span></td>
<td><span data-ttu-id="a0866-771">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-771">Electricity</span></span></td>
<td><span data-ttu-id="a0866-772">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a0866-773">175.00</span></span></td>
<td><span data-ttu-id="a0866-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-775">CC003</span></span></td>
<td><span data-ttu-id="a0866-776">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-776">Assembly</span></span></td>
<td><span data-ttu-id="a0866-777">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-777">10001</span></span></td>
<td><span data-ttu-id="a0866-778">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-778">Electricity</span></span></td>
<td><span data-ttu-id="a0866-779">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a0866-780">275.00</span></span></td>
<td><span data-ttu-id="a0866-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-782">CC004</span></span></td>
<td><span data-ttu-id="a0866-783">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-783">Packaging</span></span></td>
<td><span data-ttu-id="a0866-784">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-784">10001</span></span></td>
<td><span data-ttu-id="a0866-785">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-785">Electricity</span></span></td>
<td><span data-ttu-id="a0866-786">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a0866-787">50,00</span></span></td>
<td><span data-ttu-id="a0866-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-789">CC001</span></span></td>
<td><span data-ttu-id="a0866-790">HR</span><span class="sxs-lookup"><span data-stu-id="a0866-790">HR</span></span></td>
<td><span data-ttu-id="a0866-791">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-791">10001</span></span></td>
<td><span data-ttu-id="a0866-792">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-792">Electricity</span></span></td>
<td><span data-ttu-id="a0866-793">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-793">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a0866-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a0866-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-796">CC002</span></span></td>
<td><span data-ttu-id="a0866-797">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-797">Finance</span></span></td>
<td><span data-ttu-id="a0866-798">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-798">10001</span></span></td>
<td><span data-ttu-id="a0866-799">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-799">Electricity</span></span></td>
<td><span data-ttu-id="a0866-800">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-800">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a0866-801">436.00</span></span></td>
<td><span data-ttu-id="a0866-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-803">CC003</span></span></td>
<td><span data-ttu-id="a0866-804">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-804">Assembly</span></span></td>
<td><span data-ttu-id="a0866-805">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-805">10001</span></span></td>
<td><span data-ttu-id="a0866-806">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-806">Electricity</span></span></td>
<td><span data-ttu-id="a0866-807">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-807">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a0866-808">685.14</span></span></td>
<td><span data-ttu-id="a0866-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-810">CC004</span></span></td>
<td><span data-ttu-id="a0866-811">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-811">Packaging</span></span></td>
<td><span data-ttu-id="a0866-812">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-812">10001</span></span></td>
<td><span data-ttu-id="a0866-813">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-813">Electricity</span></span></td>
<td><span data-ttu-id="a0866-814">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-814">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a0866-815">124.57</span></span></td>
<td><span data-ttu-id="a0866-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-817">CC002</span></span></td>
<td><span data-ttu-id="a0866-818">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-818">Finance</span></span></td>
<td><span data-ttu-id="a0866-819">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-819">10001</span></span></td>
<td><span data-ttu-id="a0866-820">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-820">Electricity</span></span></td>
<td><span data-ttu-id="a0866-821">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="a0866-822">-675.00</span></span></td>
<td><span data-ttu-id="a0866-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-824">CC003</span></span></td>
<td><span data-ttu-id="a0866-825">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-825">Assembly</span></span></td>
<td><span data-ttu-id="a0866-826">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-826">10001</span></span></td>
<td><span data-ttu-id="a0866-827">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-827">Electricity</span></span></td>
<td><span data-ttu-id="a0866-828">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a0866-829">438.75</span></span></td>
<td><span data-ttu-id="a0866-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-831">CC004</span></span></td>
<td><span data-ttu-id="a0866-832">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-832">Packaging</span></span></td>
<td><span data-ttu-id="a0866-833">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-833">10001</span></span></td>
<td><span data-ttu-id="a0866-834">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-834">Electricity</span></span></td>
<td><span data-ttu-id="a0866-835">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a0866-836">236.25</span></span></td>
<td><span data-ttu-id="a0866-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-838">CC002</span></span></td>
<td><span data-ttu-id="a0866-839">財務</span><span class="sxs-lookup"><span data-stu-id="a0866-839">Finance</span></span></td>
<td><span data-ttu-id="a0866-840">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-840">10001</span></span></td>
<td><span data-ttu-id="a0866-841">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-841">Electricity</span></span></td>
<td><span data-ttu-id="a0866-842">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-842">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a0866-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a0866-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-845">CC003</span></span></td>
<td><span data-ttu-id="a0866-846">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-846">Assembly</span></span></td>
<td><span data-ttu-id="a0866-847">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-847">10001</span></span></td>
<td><span data-ttu-id="a0866-848">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-848">Electricity</span></span></td>
<td><span data-ttu-id="a0866-849">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-849">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a0866-850">5,297.69</span></span></td>
<td><span data-ttu-id="a0866-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-852">CC004</span></span></td>
<td><span data-ttu-id="a0866-853">梱包業</span><span class="sxs-lookup"><span data-stu-id="a0866-853">Packaging</span></span></td>
<td><span data-ttu-id="a0866-854">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-854">10001</span></span></td>
<td><span data-ttu-id="a0866-855">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-855">Electricity</span></span></td>
<td><span data-ttu-id="a0866-856">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-856">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a0866-857">2,852.60</span></span></td>
<td><span data-ttu-id="a0866-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-859">CC003</span></span></td>
<td><span data-ttu-id="a0866-860">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-860">Assembly</span></span></td>
<td><span data-ttu-id="a0866-861">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-861">10001</span></span></td>
<td><span data-ttu-id="a0866-862">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-862">Electricity</span></span></td>
<td><span data-ttu-id="a0866-863">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="a0866-864">-713.75</span></span></td>
<td><span data-ttu-id="a0866-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-866">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-866">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-867">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-867">Product 1</span></span></td>
<td><span data-ttu-id="a0866-868">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-868">10001</span></span></td>
<td><span data-ttu-id="a0866-869">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-869">Electricity</span></span></td>
<td><span data-ttu-id="a0866-870">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a0866-871">535.31</span></span></td>
<td><span data-ttu-id="a0866-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-873">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-873">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-874">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-874">Product 2</span></span></td>
<td><span data-ttu-id="a0866-875">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-875">10001</span></span></td>
<td><span data-ttu-id="a0866-876">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-876">Electricity</span></span></td>
<td><span data-ttu-id="a0866-877">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a0866-878">178.44</span></span></td>
<td><span data-ttu-id="a0866-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-880">CC003</span></span></td>
<td><span data-ttu-id="a0866-881">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-881">Assembly</span></span></td>
<td><span data-ttu-id="a0866-882">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-882">10001</span></span></td>
<td><span data-ttu-id="a0866-883">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-883">Electricity</span></span></td>
<td><span data-ttu-id="a0866-884">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-884">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a0866-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a0866-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-887">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-887">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-888">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-888">Product 1</span></span></td>
<td><span data-ttu-id="a0866-889">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-889">10001</span></span></td>
<td><span data-ttu-id="a0866-890">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-890">Electricity</span></span></td>
<td><span data-ttu-id="a0866-891">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-891">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a0866-892">4,487.12</span></span></td>
<td><span data-ttu-id="a0866-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-894">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-894">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-895">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-895">Product 2</span></span></td>
<td><span data-ttu-id="a0866-896">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-896">10001</span></span></td>
<td><span data-ttu-id="a0866-897">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-897">Electricity</span></span></td>
<td><span data-ttu-id="a0866-898">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-898">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a0866-899">1,495.71</span></span></td>
<td><span data-ttu-id="a0866-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-901">CC003</span></span></td>
<td><span data-ttu-id="a0866-902">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-902">Assembly</span></span></td>
<td><span data-ttu-id="a0866-903">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-903">10001</span></span></td>
<td><span data-ttu-id="a0866-904">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-904">Electricity</span></span></td>
<td><span data-ttu-id="a0866-905">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="a0866-906">-286.25</span></span></td>
<td><span data-ttu-id="a0866-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-908">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-908">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-909">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-909">Product 1</span></span></td>
<td><span data-ttu-id="a0866-910">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-910">10001</span></span></td>
<td><span data-ttu-id="a0866-911">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-911">Electricity</span></span></td>
<td><span data-ttu-id="a0866-912">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a0866-913">241.05</span></span></td>
<td><span data-ttu-id="a0866-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-915">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-915">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-916">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-916">Product 2</span></span></td>
<td><span data-ttu-id="a0866-917">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-917">10001</span></span></td>
<td><span data-ttu-id="a0866-918">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-918">Electricity</span></span></td>
<td><span data-ttu-id="a0866-919">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a0866-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a0866-920">45.20</span></span></td>
<td><span data-ttu-id="a0866-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-922">CC003</span></span></td>
<td><span data-ttu-id="a0866-923">組み立て</span><span class="sxs-lookup"><span data-stu-id="a0866-923">Assembly</span></span></td>
<td><span data-ttu-id="a0866-924">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-924">10001</span></span></td>
<td><span data-ttu-id="a0866-925">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-925">Electricity</span></span></td>
<td><span data-ttu-id="a0866-926">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-926">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a0866-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a0866-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-929">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-929">Prod 1</span></span></td>
<td><span data-ttu-id="a0866-930">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-930">Product 1</span></span></td>
<td><span data-ttu-id="a0866-931">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-931">10001</span></span></td>
<td><span data-ttu-id="a0866-932">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-932">Electricity</span></span></td>
<td><span data-ttu-id="a0866-933">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-933">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a0866-934">2,507.09</span></span></td>
<td><span data-ttu-id="a0866-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a0866-936">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-936">Prod 2</span></span></td>
<td><span data-ttu-id="a0866-937">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-937">Product 2</span></span></td>
<td><span data-ttu-id="a0866-938">10001</span><span class="sxs-lookup"><span data-stu-id="a0866-938">10001</span></span></td>
<td><span data-ttu-id="a0866-939">電気</span><span class="sxs-lookup"><span data-stu-id="a0866-939">Electricity</span></span></td>
<td><span data-ttu-id="a0866-940">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-940">Variable cost</span></span></td>
<td><span data-ttu-id="a0866-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a0866-941">470.08</span></span></td>
<td><span data-ttu-id="a0866-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a0866-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a0866-943">まとめ</span><span class="sxs-lookup"><span data-stu-id="a0866-943">Conclusion</span></span>
<span data-ttu-id="a0866-944">財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a0866-945">したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。</span><span class="sxs-lookup"><span data-stu-id="a0866-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a0866-946">コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。</span><span class="sxs-lookup"><span data-stu-id="a0866-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a0866-947">各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a0866-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a0866-948">原価要素</span><span class="sxs-lookup"><span data-stu-id="a0866-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a0866-949">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a0866-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a0866-950">小計</span><span class="sxs-lookup"><span data-stu-id="a0866-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a0866-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a0866-951">CC099</span></span></th>
<th><span data-ttu-id="a0866-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a0866-952">CC001</span></span></th>
<th><span data-ttu-id="a0866-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a0866-953">CC002</span></span></th>
<th><span data-ttu-id="a0866-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a0866-954">CC003</span></span></th>
<th><span data-ttu-id="a0866-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a0866-955">CC004</span></span></th>
<th><span data-ttu-id="a0866-956">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a0866-956">Proj 1</span></span></th>
<th><span data-ttu-id="a0866-957">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a0866-957">Proj 2</span></span></th>
<th><span data-ttu-id="a0866-958">製品 1</span><span class="sxs-lookup"><span data-stu-id="a0866-958">Prod 1</span></span></th>
<th><span data-ttu-id="a0866-959">製品 2</span><span class="sxs-lookup"><span data-stu-id="a0866-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a0866-960">10001 電気</span><span class="sxs-lookup"><span data-stu-id="a0866-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a0866-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a0866-970">未分類</span><span class="sxs-lookup"><span data-stu-id="a0866-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-971">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a0866-972">固定費</span><span class="sxs-lookup"><span data-stu-id="a0866-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-973">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-974">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-975">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-976">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-977">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a0866-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a0866-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a0866-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a0866-981">変動費</span><span class="sxs-lookup"><span data-stu-id="a0866-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-982">000</span><span class="sxs-lookup"><span data-stu-id="a0866-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-983">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-984">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-985">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-986">0.00</span><span class="sxs-lookup"><span data-stu-id="a0866-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-987">30.00</span><span class="sxs-lookup"><span data-stu-id="a0866-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-988">10.00</span><span class="sxs-lookup"><span data-stu-id="a0866-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a0866-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a0866-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a0866-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0866-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a0866-992">このトピックでは、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。</span><span class="sxs-lookup"><span data-stu-id="a0866-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a0866-993">したがって、この間接費は組織の最下位レベルに配賦されます。</span><span class="sxs-lookup"><span data-stu-id="a0866-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a0866-994">つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。</span><span class="sxs-lookup"><span data-stu-id="a0866-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a0866-995">コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="a0866-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a0866-996">詳細については、[原価ロールアップ ポリシーおよび間接費の計算](cost-rollup.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0866-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



