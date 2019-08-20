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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841492"
---
# <a name="overhead-calculation"></a><span data-ttu-id="29780-103">間接費の計算</span><span class="sxs-lookup"><span data-stu-id="29780-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29780-104">このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="29780-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="29780-105">用語の定義</span><span class="sxs-lookup"><span data-stu-id="29780-105">Term definition</span></span>
---------------

<span data-ttu-id="29780-106">間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。</span><span class="sxs-lookup"><span data-stu-id="29780-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="29780-107">間接費は、営利活動を生み出すのに不可欠な支援を提供します。</span><span class="sxs-lookup"><span data-stu-id="29780-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="29780-108">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="29780-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="29780-109">賃料</span><span class="sxs-lookup"><span data-stu-id="29780-109">Rent</span></span>
-   <span data-ttu-id="29780-110">電気</span><span class="sxs-lookup"><span data-stu-id="29780-110">Electricity</span></span>
-   <span data-ttu-id="29780-111">管理給与</span><span class="sxs-lookup"><span data-stu-id="29780-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="29780-112">間接費計算の概要</span><span class="sxs-lookup"><span data-stu-id="29780-112">Overhead calculation overview</span></span>
<span data-ttu-id="29780-113">間接費計算は、コスト会計ポリシーを正しい順序で実行します。</span><span class="sxs-lookup"><span data-stu-id="29780-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="29780-114">コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="29780-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="29780-115">間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="29780-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="29780-116">間接費計算が生成するコスト エントリは転記日を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="29780-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="29780-117">この転記日は、計算に使用される会計年度期間の終了日と一致します。</span><span class="sxs-lookup"><span data-stu-id="29780-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="29780-118">固有のバージョン ID は、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="29780-119">バージョン タイプ</span><span class="sxs-lookup"><span data-stu-id="29780-119">Version type</span></span>
-   <span data-ttu-id="29780-120">日時</span><span class="sxs-lookup"><span data-stu-id="29780-120">Date and time</span></span>
-   <span data-ttu-id="29780-121">原価会計元帳</span><span class="sxs-lookup"><span data-stu-id="29780-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="29780-122">年度</span><span class="sxs-lookup"><span data-stu-id="29780-122">Fiscal year</span></span>
-   <span data-ttu-id="29780-123">会計年度期間</span><span class="sxs-lookup"><span data-stu-id="29780-123">Fiscal period</span></span>

<span data-ttu-id="29780-124">間接費計算は、バージョンとは無関係に実行されます。</span><span class="sxs-lookup"><span data-stu-id="29780-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="29780-125">そのため、実際のバージョンの前に予算バージョンを計算することができます。</span><span class="sxs-lookup"><span data-stu-id="29780-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="29780-126">間接費計算は、次の図に示されているように 4 つのステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="29780-127">各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="29780-128">この仕訳ヘッダーは、各計算ステップの入力データを保持します。</span><span class="sxs-lookup"><span data-stu-id="29780-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="29780-129">ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="29780-130">そのため、常に完全なトレーサビリティがあります。</span><span class="sxs-lookup"><span data-stu-id="29780-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="29780-131">[![間接費計算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="29780-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="29780-132">電気間接費の計算および配賦</span><span class="sxs-lookup"><span data-stu-id="29780-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="29780-133">財務会計では、電気などの一部のコストは一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="29780-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="29780-134">したがって、コスト会計には詳細な管理情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="29780-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="29780-135">コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29780-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="29780-136">このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="29780-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="29780-137">一般会計では、電気コストは以下の表に示されているように転記できます。</span><span class="sxs-lookup"><span data-stu-id="29780-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-138">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="29780-139">原価部門</span><span class="sxs-lookup"><span data-stu-id="29780-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="29780-140">主勘定</span><span class="sxs-lookup"><span data-stu-id="29780-140">Main account</span></span></th>
<th><span data-ttu-id="29780-141">会計通貨での金額</span><span class="sxs-lookup"><span data-stu-id="29780-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-142">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29780-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="29780-143">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-143">CC099</span></span></td>
<td><span data-ttu-id="29780-144">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-144">Default cost center</span></span></td>
<td><span data-ttu-id="29780-145">10001</span><span class="sxs-lookup"><span data-stu-id="29780-145">10001</span></span></td>
<td><span data-ttu-id="29780-146">電気</span><span class="sxs-lookup"><span data-stu-id="29780-146">Electricity</span></span></td>
<td><span data-ttu-id="29780-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="29780-148">手順 1: コスト動作計算を処理する</span><span class="sxs-lookup"><span data-stu-id="29780-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="29780-149">既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="29780-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="29780-150">コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。</span><span class="sxs-lookup"><span data-stu-id="29780-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="29780-151">コスト動作ルールの定義</span><span class="sxs-lookup"><span data-stu-id="29780-151">Define the cost behavior rule</span></span>

<span data-ttu-id="29780-152">場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。</span><span class="sxs-lookup"><span data-stu-id="29780-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="29780-153">電気代は多くの場合この定義と一致します。</span><span class="sxs-lookup"><span data-stu-id="29780-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="29780-154">特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。</span><span class="sxs-lookup"><span data-stu-id="29780-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="29780-155">たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。</span><span class="sxs-lookup"><span data-stu-id="29780-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="29780-156">固定金額 1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="29780-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="29780-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="29780-158">1000,01 &lt; N = 変動</span><span class="sxs-lookup"><span data-stu-id="29780-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="29780-159">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-160">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-160">Journal</span></span></th>
<th><span data-ttu-id="29780-161">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="29780-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="29780-162">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="29780-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="29780-163">バージョン</span><span class="sxs-lookup"><span data-stu-id="29780-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-164">00001</span><span class="sxs-lookup"><span data-stu-id="29780-164">00001</span></span></td>
<td><span data-ttu-id="29780-165">原価動作計算仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="29780-166">会計年度</span><span class="sxs-lookup"><span data-stu-id="29780-166">Fiscal</span></span></td>
<td><span data-ttu-id="29780-167">2017</span><span class="sxs-lookup"><span data-stu-id="29780-167">2017</span></span></td>
<td><span data-ttu-id="29780-168">期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-168">Period 1</span></span></td>
<td><span data-ttu-id="29780-169">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="29780-170">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="29780-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-171">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="29780-172">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-173">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-173">Cost element</span></span></th>
<th><span data-ttu-id="29780-174">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-174">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-175">金額</span><span class="sxs-lookup"><span data-stu-id="29780-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-176">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29780-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="29780-177">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-177">CC099</span></span></td>
<td><span data-ttu-id="29780-178">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-178">Default cost center</span></span></td>
<td><span data-ttu-id="29780-179">10001</span><span class="sxs-lookup"><span data-stu-id="29780-179">10001</span></span></td>
<td><span data-ttu-id="29780-180">電気</span><span class="sxs-lookup"><span data-stu-id="29780-180">Electricity</span></span></td>
<td><span data-ttu-id="29780-181">未分類</span><span class="sxs-lookup"><span data-stu-id="29780-181">Unclassified</span></span></td>
<td><span data-ttu-id="29780-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="29780-183">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="29780-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-184">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-185">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-185">Cost element</span></span></th>
<th><span data-ttu-id="29780-186">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-186">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-187">金額</span><span class="sxs-lookup"><span data-stu-id="29780-187">Amount</span></span></th>
<th><span data-ttu-id="29780-188">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-189">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-189">CC099</span></span></td>
<td><span data-ttu-id="29780-190">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-190">Default cost center</span></span></td>
<td><span data-ttu-id="29780-191">10001</span><span class="sxs-lookup"><span data-stu-id="29780-191">10001</span></span></td>
<td><span data-ttu-id="29780-192">電気</span><span class="sxs-lookup"><span data-stu-id="29780-192">Electricity</span></span></td>
<td><span data-ttu-id="29780-193">未分類</span><span class="sxs-lookup"><span data-stu-id="29780-193">Unclassified</span></span></td>
<td><span data-ttu-id="29780-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-194">10,000.00</span></span></td>
<td><span data-ttu-id="29780-195">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="29780-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-196">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-196">CC099</span></span></td>
<td><span data-ttu-id="29780-197">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-197">Default cost center</span></span></td>
<td><span data-ttu-id="29780-198">10001</span><span class="sxs-lookup"><span data-stu-id="29780-198">10001</span></span></td>
<td><span data-ttu-id="29780-199">電気</span><span class="sxs-lookup"><span data-stu-id="29780-199">Electricity</span></span></td>
<td><span data-ttu-id="29780-200">未分類</span><span class="sxs-lookup"><span data-stu-id="29780-200">Unclassified</span></span></td>
<td><span data-ttu-id="29780-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-201">-10,000.00</span></span></td>
<td><span data-ttu-id="29780-202">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-203">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-203">CC099</span></span></td>
<td><span data-ttu-id="29780-204">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-204">Default cost center</span></span></td>
<td><span data-ttu-id="29780-205">10001</span><span class="sxs-lookup"><span data-stu-id="29780-205">10001</span></span></td>
<td><span data-ttu-id="29780-206">電気</span><span class="sxs-lookup"><span data-stu-id="29780-206">Electricity</span></span></td>
<td><span data-ttu-id="29780-207">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-207">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-208">1,000.00</span></span></td>
<td><span data-ttu-id="29780-209">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-210">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-210">CC099</span></span></td>
<td><span data-ttu-id="29780-211">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-211">Default cost center</span></span></td>
<td><span data-ttu-id="29780-212">10001</span><span class="sxs-lookup"><span data-stu-id="29780-212">10001</span></span></td>
<td><span data-ttu-id="29780-213">電気</span><span class="sxs-lookup"><span data-stu-id="29780-213">Electricity</span></span></td>
<td><span data-ttu-id="29780-214">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-214">Variable cost</span></span></td>
<td><span data-ttu-id="29780-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-215">9,000.00</span></span></td>
<td><span data-ttu-id="29780-216">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-217">詳細については、「[原価動作ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29780-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="29780-218">手順 2: コスト配分計算を処理する</span><span class="sxs-lookup"><span data-stu-id="29780-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="29780-219">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29780-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="29780-220">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="29780-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="29780-221">コスト配分ルールの定義</span><span class="sxs-lookup"><span data-stu-id="29780-221">Define the cost distribution rule</span></span>

<span data-ttu-id="29780-222">財務会計では、電気コストは多くの場合一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="29780-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="29780-223">コスト会計では、このアプローチは十分に詳細ではありません。</span><span class="sxs-lookup"><span data-stu-id="29780-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="29780-224">変動費は個々のコスト オブジェクトに公平に配分する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29780-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="29780-225">最も論理的な配賦基準は、電気 (Kwh) の消費です。</span><span class="sxs-lookup"><span data-stu-id="29780-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="29780-226">電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="29780-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="29780-227">既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="29780-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-228">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-228">Cost object</span></span></th>
<th><span data-ttu-id="29780-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="29780-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-230">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-230">CC001</span></span></td>
<td><span data-ttu-id="29780-231">HR</span><span class="sxs-lookup"><span data-stu-id="29780-231">HR</span></span></td>
<td><span data-ttu-id="29780-232">1.000</span><span class="sxs-lookup"><span data-stu-id="29780-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-233">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-233">CC002</span></span></td>
<td><span data-ttu-id="29780-234">財務</span><span class="sxs-lookup"><span data-stu-id="29780-234">Finance</span></span></td>
<td><span data-ttu-id="29780-235">6,000</span><span class="sxs-lookup"><span data-stu-id="29780-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-236">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-236">CC003</span></span></td>
<td><span data-ttu-id="29780-237">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-237">Assembly</span></span></td>
<td><span data-ttu-id="29780-238">0</span><span class="sxs-lookup"><span data-stu-id="29780-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-239">次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-240">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-240">Cost object</span></span></th>
<th><span data-ttu-id="29780-241">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-241">Magnitude</span></span></th>
<th><span data-ttu-id="29780-242">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-242">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-243">金額</span><span class="sxs-lookup"><span data-stu-id="29780-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-244">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-244">CC001</span></span></td>
<td><span data-ttu-id="29780-245">HR</span><span class="sxs-lookup"><span data-stu-id="29780-245">HR</span></span></td>
<td><span data-ttu-id="29780-246">1.000</span><span class="sxs-lookup"><span data-stu-id="29780-246">1,000</span></span></td>
<td><span data-ttu-id="29780-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="29780-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="29780-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-249">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-249">CC002</span></span></td>
<td><span data-ttu-id="29780-250">財務</span><span class="sxs-lookup"><span data-stu-id="29780-250">Finance</span></span></td>
<td><span data-ttu-id="29780-251">6,000</span><span class="sxs-lookup"><span data-stu-id="29780-251">6,000</span></span></td>
<td><span data-ttu-id="29780-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="29780-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="29780-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-254">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-254">CC003</span></span></td>
<td><span data-ttu-id="29780-255">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-255">Assembly</span></span></td>
<td><span data-ttu-id="29780-256">0</span><span class="sxs-lookup"><span data-stu-id="29780-256">0</span></span></td>
<td><span data-ttu-id="29780-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="29780-258">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-259">固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。</span><span class="sxs-lookup"><span data-stu-id="29780-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="29780-260">フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-261">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-261">Cost object</span></span></th>
<th><span data-ttu-id="29780-262">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="29780-262">Formula</span></span></th>
<th><span data-ttu-id="29780-263">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-263">Magnitude</span></span></th>
<th><span data-ttu-id="29780-264">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-264">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-265">金額</span><span class="sxs-lookup"><span data-stu-id="29780-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-266">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-266">CC001</span></span></td>
<td><span data-ttu-id="29780-267">HR</span><span class="sxs-lookup"><span data-stu-id="29780-267">HR</span></span></td>
<td><span data-ttu-id="29780-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="29780-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="29780-269">1</span><span class="sxs-lookup"><span data-stu-id="29780-269">1</span></span></td>
<td><span data-ttu-id="29780-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="29780-271">500.00</span><span class="sxs-lookup"><span data-stu-id="29780-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-272">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-272">CC002</span></span></td>
<td><span data-ttu-id="29780-273">財務</span><span class="sxs-lookup"><span data-stu-id="29780-273">Finance</span></span></td>
<td><span data-ttu-id="29780-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="29780-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="29780-275">1</span><span class="sxs-lookup"><span data-stu-id="29780-275">1</span></span></td>
<td><span data-ttu-id="29780-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="29780-277">500.00</span><span class="sxs-lookup"><span data-stu-id="29780-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-278">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-278">CC003</span></span></td>
<td><span data-ttu-id="29780-279">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-279">Assembly</span></span></td>
<td><span data-ttu-id="29780-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="29780-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="29780-281">0</span><span class="sxs-lookup"><span data-stu-id="29780-281">0</span></span></td>
<td><span data-ttu-id="29780-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="29780-283">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="29780-284">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-285">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-285">Journal</span></span></th>
<th><span data-ttu-id="29780-286">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="29780-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="29780-287">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="29780-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="29780-288">バージョン</span><span class="sxs-lookup"><span data-stu-id="29780-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-289">00002</span><span class="sxs-lookup"><span data-stu-id="29780-289">00002</span></span></td>
<td><span data-ttu-id="29780-290">コスト配分計算仕訳</span><span class="sxs-lookup"><span data-stu-id="29780-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="29780-291">会計年度</span><span class="sxs-lookup"><span data-stu-id="29780-291">Fiscal</span></span></td>
<td><span data-ttu-id="29780-292">2017</span><span class="sxs-lookup"><span data-stu-id="29780-292">2017</span></span></td>
<td><span data-ttu-id="29780-293">期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-293">Period 1</span></span></td>
<td><span data-ttu-id="29780-294">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="29780-295">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="29780-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-296">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="29780-297">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-298">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-298">Cost element</span></span></th>
<th><span data-ttu-id="29780-299">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-299">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-300">金額</span><span class="sxs-lookup"><span data-stu-id="29780-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-301">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-302">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-302">CC099</span></span></td>
<td><span data-ttu-id="29780-303">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-303">Default cost center</span></span></td>
<td><span data-ttu-id="29780-304">10001</span><span class="sxs-lookup"><span data-stu-id="29780-304">10001</span></span></td>
<td><span data-ttu-id="29780-305">電気</span><span class="sxs-lookup"><span data-stu-id="29780-305">Electricity</span></span></td>
<td><span data-ttu-id="29780-306">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-306">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-308">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-309">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-309">CC099</span></span></td>
<td><span data-ttu-id="29780-310">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-310">Default cost center</span></span></td>
<td><span data-ttu-id="29780-311">10001</span><span class="sxs-lookup"><span data-stu-id="29780-311">10001</span></span></td>
<td><span data-ttu-id="29780-312">電気</span><span class="sxs-lookup"><span data-stu-id="29780-312">Electricity</span></span></td>
<td><span data-ttu-id="29780-313">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-313">Variable cost</span></span></td>
<td><span data-ttu-id="29780-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="29780-315">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="29780-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-316">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-317">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-317">Cost element</span></span></th>
<th><span data-ttu-id="29780-318">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-318">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-319">金額</span><span class="sxs-lookup"><span data-stu-id="29780-319">Amount</span></span></th>
<th><span data-ttu-id="29780-320">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-321">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-321">CC099</span></span></td>
<td><span data-ttu-id="29780-322">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-322">Default cost center</span></span></td>
<td><span data-ttu-id="29780-323">10001</span><span class="sxs-lookup"><span data-stu-id="29780-323">10001</span></span></td>
<td><span data-ttu-id="29780-324">電気</span><span class="sxs-lookup"><span data-stu-id="29780-324">Electricity</span></span></td>
<td><span data-ttu-id="29780-325">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-325">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-326">-1,000.00</span></span></td>
<td><span data-ttu-id="29780-327">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-328">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-328">CC001</span></span></td>
<td><span data-ttu-id="29780-329">HR</span><span class="sxs-lookup"><span data-stu-id="29780-329">HR</span></span></td>
<td><span data-ttu-id="29780-330">10001</span><span class="sxs-lookup"><span data-stu-id="29780-330">10001</span></span></td>
<td><span data-ttu-id="29780-331">電気</span><span class="sxs-lookup"><span data-stu-id="29780-331">Electricity</span></span></td>
<td><span data-ttu-id="29780-332">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-332">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-333">500.00</span><span class="sxs-lookup"><span data-stu-id="29780-333">500.00</span></span></td>
<td><span data-ttu-id="29780-334">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-335">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-335">CC002</span></span></td>
<td><span data-ttu-id="29780-336">財務</span><span class="sxs-lookup"><span data-stu-id="29780-336">Finance</span></span></td>
<td><span data-ttu-id="29780-337">10001</span><span class="sxs-lookup"><span data-stu-id="29780-337">10001</span></span></td>
<td><span data-ttu-id="29780-338">電気</span><span class="sxs-lookup"><span data-stu-id="29780-338">Electricity</span></span></td>
<td><span data-ttu-id="29780-339">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-339">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-340">500.00</span><span class="sxs-lookup"><span data-stu-id="29780-340">500.00</span></span></td>
<td><span data-ttu-id="29780-341">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-342">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-342">CC099</span></span></td>
<td><span data-ttu-id="29780-343">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="29780-343">Default cost center</span></span></td>
<td><span data-ttu-id="29780-344">10001</span><span class="sxs-lookup"><span data-stu-id="29780-344">10001</span></span></td>
<td><span data-ttu-id="29780-345">電気</span><span class="sxs-lookup"><span data-stu-id="29780-345">Electricity</span></span></td>
<td><span data-ttu-id="29780-346">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-346">Variable cost</span></span></td>
<td><span data-ttu-id="29780-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="29780-347">-9,000.00</span></span></td>
<td><span data-ttu-id="29780-348">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-349">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-349">CC001</span></span></td>
<td><span data-ttu-id="29780-350">HR</span><span class="sxs-lookup"><span data-stu-id="29780-350">HR</span></span></td>
<td><span data-ttu-id="29780-351">10001</span><span class="sxs-lookup"><span data-stu-id="29780-351">10001</span></span></td>
<td><span data-ttu-id="29780-352">電気</span><span class="sxs-lookup"><span data-stu-id="29780-352">Electricity</span></span></td>
<td><span data-ttu-id="29780-353">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-353">Variable cost</span></span></td>
<td><span data-ttu-id="29780-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="29780-354">1,285.71</span></span></td>
<td><span data-ttu-id="29780-355">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-356">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-356">CC002</span></span></td>
<td><span data-ttu-id="29780-357">財務</span><span class="sxs-lookup"><span data-stu-id="29780-357">Finance</span></span></td>
<td><span data-ttu-id="29780-358">10001</span><span class="sxs-lookup"><span data-stu-id="29780-358">10001</span></span></td>
<td><span data-ttu-id="29780-359">電気</span><span class="sxs-lookup"><span data-stu-id="29780-359">Electricity</span></span></td>
<td><span data-ttu-id="29780-360">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-360">Variable cost</span></span></td>
<td><span data-ttu-id="29780-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="29780-361">7,714.29</span></span></td>
<td><span data-ttu-id="29780-362">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-363">詳細については、「[原価配分ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29780-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="29780-364">手順 3: 間接費率の計算を処理する</span><span class="sxs-lookup"><span data-stu-id="29780-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="29780-365">間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="29780-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="29780-366">請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。</span><span class="sxs-lookup"><span data-stu-id="29780-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="29780-367">間接費率の定義</span><span class="sxs-lookup"><span data-stu-id="29780-367">Define the overhead rate</span></span>

<span data-ttu-id="29780-368">コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="29780-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="29780-369">HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-370">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-370">Cost object</span></span></th>
<th><span data-ttu-id="29780-371">時間</span><span class="sxs-lookup"><span data-stu-id="29780-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-372">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-372">Proj 1</span></span></td>
<td><span data-ttu-id="29780-373">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-373">Project 1</span></span></td>
<td><span data-ttu-id="29780-374">3</span><span class="sxs-lookup"><span data-stu-id="29780-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-375">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-375">Proj 2</span></span></td>
<td><span data-ttu-id="29780-376">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-376">Project 2</span></span></td>
<td><span data-ttu-id="29780-377">1</span><span class="sxs-lookup"><span data-stu-id="29780-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-378">コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。</span><span class="sxs-lookup"><span data-stu-id="29780-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-379">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-379">Cost object</span></span></th>
<th><span data-ttu-id="29780-380">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-380">Cost element</span></span></th>
<th><span data-ttu-id="29780-381">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-381">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-382">単位</span><span class="sxs-lookup"><span data-stu-id="29780-382">Units</span></span></th>
<th><span data-ttu-id="29780-383">率</span><span class="sxs-lookup"><span data-stu-id="29780-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-384">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-384">CC001</span></span></td>
<td><span data-ttu-id="29780-385">HR</span><span class="sxs-lookup"><span data-stu-id="29780-385">HR</span></span></td>
<td><span data-ttu-id="29780-386">10001</span><span class="sxs-lookup"><span data-stu-id="29780-386">10001</span></span></td>
<td><span data-ttu-id="29780-387">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-387">Variable cost</span></span></td>
<td><span data-ttu-id="29780-388">1</span><span class="sxs-lookup"><span data-stu-id="29780-388">1</span></span></td>
<td><span data-ttu-id="29780-389">10</span><span class="sxs-lookup"><span data-stu-id="29780-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-390">次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-391">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-391">Cost object</span></span></th>
<th><span data-ttu-id="29780-392">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-392">Magnitude</span></span></th>
<th><span data-ttu-id="29780-393">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-393">Cost element</span></span></th>
<th><span data-ttu-id="29780-394">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-394">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-395">金額</span><span class="sxs-lookup"><span data-stu-id="29780-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-396">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-396">Proj 1</span></span></td>
<td><span data-ttu-id="29780-397">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-397">Project 1</span></span></td>
<td><span data-ttu-id="29780-398">3</span><span class="sxs-lookup"><span data-stu-id="29780-398">3</span></span></td>
<td><span data-ttu-id="29780-399">10001</span><span class="sxs-lookup"><span data-stu-id="29780-399">10001</span></span></td>
<td><span data-ttu-id="29780-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="29780-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="29780-401">30.00</span><span class="sxs-lookup"><span data-stu-id="29780-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-402">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-402">Proj 2</span></span></td>
<td><span data-ttu-id="29780-403">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-403">Project 2</span></span></td>
<td><span data-ttu-id="29780-404">1</span><span class="sxs-lookup"><span data-stu-id="29780-404">1</span></span></td>
<td><span data-ttu-id="29780-405">10001</span><span class="sxs-lookup"><span data-stu-id="29780-405">10001</span></span></td>
<td><span data-ttu-id="29780-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="29780-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="29780-407">10.00</span><span class="sxs-lookup"><span data-stu-id="29780-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="29780-408">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-409">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-409">Journal</span></span></th>
<th><span data-ttu-id="29780-410">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="29780-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="29780-411">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="29780-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="29780-412">バージョン</span><span class="sxs-lookup"><span data-stu-id="29780-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-413">00003</span><span class="sxs-lookup"><span data-stu-id="29780-413">00003</span></span></td>
<td><span data-ttu-id="29780-414">間接比率計算仕訳</span><span class="sxs-lookup"><span data-stu-id="29780-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="29780-415">会計年度</span><span class="sxs-lookup"><span data-stu-id="29780-415">Fiscal</span></span></td>
<td><span data-ttu-id="29780-416">2017</span><span class="sxs-lookup"><span data-stu-id="29780-416">2017</span></span></td>
<td><span data-ttu-id="29780-417">期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-417">Period 1</span></span></td>
<td><span data-ttu-id="29780-418">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="29780-419">仕訳入力 (間接比率計算のための仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="29780-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-420">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="29780-421">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-421">Cost object</span></span></th>
<th><span data-ttu-id="29780-422">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-423">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-424">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-424">Proj 1</span></span></td>
<td><span data-ttu-id="29780-425">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="29780-426">3.00</span><span class="sxs-lookup"><span data-stu-id="29780-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-427">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-428">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-428">Proj 2</span></span></td>
<td><span data-ttu-id="29780-429">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="29780-430">1.00</span><span class="sxs-lookup"><span data-stu-id="29780-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="29780-431">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="29780-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-432">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-433">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-433">Cost element</span></span></th>
<th><span data-ttu-id="29780-434">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-434">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-435">金額</span><span class="sxs-lookup"><span data-stu-id="29780-435">Amount</span></span></th>
<th><span data-ttu-id="29780-436">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="29780-437">CC0001</span></span></td>
<td><span data-ttu-id="29780-438">HR</span><span class="sxs-lookup"><span data-stu-id="29780-438">HR</span></span></td>
<td><span data-ttu-id="29780-439">10001</span><span class="sxs-lookup"><span data-stu-id="29780-439">10001</span></span></td>
<td><span data-ttu-id="29780-440">電気</span><span class="sxs-lookup"><span data-stu-id="29780-440">Electricity</span></span></td>
<td><span data-ttu-id="29780-441">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-441">Variable cost</span></span></td>
<td><span data-ttu-id="29780-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="29780-442">-30.00</span></span></td>
<td><span data-ttu-id="29780-443">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-444">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-444">Proj 1</span></span></td>
<td><span data-ttu-id="29780-445">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="29780-446">10001</span><span class="sxs-lookup"><span data-stu-id="29780-446">10001</span></span></td>
<td><span data-ttu-id="29780-447">電気</span><span class="sxs-lookup"><span data-stu-id="29780-447">Electricity</span></span></td>
<td><span data-ttu-id="29780-448">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-448">Variable cost</span></span></td>
<td><span data-ttu-id="29780-449">30.00</span><span class="sxs-lookup"><span data-stu-id="29780-449">30.00</span></span></td>
<td><span data-ttu-id="29780-450">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-451">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-451">CC001</span></span></td>
<td><span data-ttu-id="29780-452">HR</span><span class="sxs-lookup"><span data-stu-id="29780-452">HR</span></span></td>
<td><span data-ttu-id="29780-453">10001</span><span class="sxs-lookup"><span data-stu-id="29780-453">10001</span></span></td>
<td><span data-ttu-id="29780-454">電気</span><span class="sxs-lookup"><span data-stu-id="29780-454">Electricity</span></span></td>
<td><span data-ttu-id="29780-455">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-455">Variable cost</span></span></td>
<td><span data-ttu-id="29780-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="29780-456">-10.00</span></span></td>
<td><span data-ttu-id="29780-457">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-458">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-458">Proj 2</span></span></td>
<td><span data-ttu-id="29780-459">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="29780-460">10001</span><span class="sxs-lookup"><span data-stu-id="29780-460">10001</span></span></td>
<td><span data-ttu-id="29780-461">電気</span><span class="sxs-lookup"><span data-stu-id="29780-461">Electricity</span></span></td>
<td><span data-ttu-id="29780-462">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-462">Variable cost</span></span></td>
<td><span data-ttu-id="29780-463">10.00</span><span class="sxs-lookup"><span data-stu-id="29780-463">10.00</span></span></td>
<td><span data-ttu-id="29780-464">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-465">詳細については、「[間接費計算を実行する](cost-rollup.md#perform-overhead-calculation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29780-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="29780-466">手順 4: コスト配賦計算を処理する</span><span class="sxs-lookup"><span data-stu-id="29780-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="29780-467">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="29780-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="29780-468">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="29780-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="29780-469">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="29780-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="29780-470">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="29780-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="29780-471">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="29780-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="29780-472">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="29780-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="29780-473">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="29780-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="29780-474">[![相互手法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="29780-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="29780-475">コスト配賦の定義</span><span class="sxs-lookup"><span data-stu-id="29780-475">Define the cost allocation</span></span>

<span data-ttu-id="29780-476">次に、コストのフローを追跡する方法を説明する簡単な例を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="29780-477">コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="29780-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="29780-478">HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-479">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-479">Cost object</span></span></th>
<th><span data-ttu-id="29780-480">HR サービス</span><span class="sxs-lookup"><span data-stu-id="29780-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-481">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-481">CC002</span></span></td>
<td><span data-ttu-id="29780-482">財務</span><span class="sxs-lookup"><span data-stu-id="29780-482">Finance</span></span></td>
<td><span data-ttu-id="29780-483">35</span><span class="sxs-lookup"><span data-stu-id="29780-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-484">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-484">CC003</span></span></td>
<td><span data-ttu-id="29780-485">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-485">Assembly</span></span></td>
<td><span data-ttu-id="29780-486">55</span><span class="sxs-lookup"><span data-stu-id="29780-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-487">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-487">CC004</span></span></td>
<td><span data-ttu-id="29780-488">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-488">Packaging</span></span></td>
<td><span data-ttu-id="29780-489">10</span><span class="sxs-lookup"><span data-stu-id="29780-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-490">コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="29780-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="29780-491">財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-492">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-492">Cost object</span></span></th>
<th><span data-ttu-id="29780-493">財務サービス</span><span class="sxs-lookup"><span data-stu-id="29780-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-494">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-494">CC003</span></span></td>
<td><span data-ttu-id="29780-495">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-495">Assembly</span></span></td>
<td><span data-ttu-id="29780-496">65</span><span class="sxs-lookup"><span data-stu-id="29780-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-497">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-497">CC004</span></span></td>
<td><span data-ttu-id="29780-498">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-498">Packaging</span></span></td>
<td><span data-ttu-id="29780-499">35</span><span class="sxs-lookup"><span data-stu-id="29780-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-500">コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="29780-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="29780-501">組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-502">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-502">Cost object</span></span></th>
<th><span data-ttu-id="29780-503">組み立てサービス (時間)</span><span class="sxs-lookup"><span data-stu-id="29780-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-504">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-504">Prod 1</span></span></td>
<td><span data-ttu-id="29780-505">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-505">Product 1</span></span></td>
<td><span data-ttu-id="29780-506">60</span><span class="sxs-lookup"><span data-stu-id="29780-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-507">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-507">Prod 2</span></span></td>
<td><span data-ttu-id="29780-508">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-508">Product 2</span></span></td>
<td><span data-ttu-id="29780-509">20</span><span class="sxs-lookup"><span data-stu-id="29780-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-510">コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="29780-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="29780-511">梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="29780-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-512">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-512">Cost object</span></span></th>
<th><span data-ttu-id="29780-513">梱包業サービス (時間)</span><span class="sxs-lookup"><span data-stu-id="29780-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-514">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-514">Prod 1</span></span></td>
<td><span data-ttu-id="29780-515">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-515">Product 1</span></span></td>
<td><span data-ttu-id="29780-516">80</span><span class="sxs-lookup"><span data-stu-id="29780-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-517">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-517">Prod 2</span></span></td>
<td><span data-ttu-id="29780-518">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-518">Product 2</span></span></td>
<td><span data-ttu-id="29780-519">15</span><span class="sxs-lookup"><span data-stu-id="29780-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="29780-520">Finance and Operations では、製品に消費される生産時間などの統計測定は、ソース データから抽出できます。</span><span class="sxs-lookup"><span data-stu-id="29780-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="29780-521">詳細については、「[統計測定プロバイダー テンプレート](statistical-measure-provider-template.md#statistical-measure-provider-template)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29780-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="29780-522">次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-523">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-523">Cost object</span></span></th>
<th><span data-ttu-id="29780-524">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-524">Magnitude</span></span></th>
<th><span data-ttu-id="29780-525">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-525">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-526">金額</span><span class="sxs-lookup"><span data-stu-id="29780-526">Amount</span></span></th>
<th><span data-ttu-id="29780-527">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-528">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-528">CC002</span></span></td>
<td><span data-ttu-id="29780-529">財務</span><span class="sxs-lookup"><span data-stu-id="29780-529">Finance</span></span></td>
<td><span data-ttu-id="29780-530">35</span><span class="sxs-lookup"><span data-stu-id="29780-530">35</span></span></td>
<td><span data-ttu-id="29780-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="29780-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="29780-532">175.00</span><span class="sxs-lookup"><span data-stu-id="29780-532">175.00</span></span></td>
<td><span data-ttu-id="29780-533">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-534">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-534">CC003</span></span></td>
<td><span data-ttu-id="29780-535">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-535">Assembly</span></span></td>
<td><span data-ttu-id="29780-536">55</span><span class="sxs-lookup"><span data-stu-id="29780-536">55</span></span></td>
<td><span data-ttu-id="29780-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="29780-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="29780-538">275.00</span><span class="sxs-lookup"><span data-stu-id="29780-538">275.00</span></span></td>
<td><span data-ttu-id="29780-539">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-540">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-540">CC004</span></span></td>
<td><span data-ttu-id="29780-541">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-541">Packaging</span></span></td>
<td><span data-ttu-id="29780-542">10</span><span class="sxs-lookup"><span data-stu-id="29780-542">10</span></span></td>
<td><span data-ttu-id="29780-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="29780-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="29780-544">50.00</span><span class="sxs-lookup"><span data-stu-id="29780-544">50.00</span></span></td>
<td><span data-ttu-id="29780-545">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-546">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-546">CC002</span></span></td>
<td><span data-ttu-id="29780-547">財務</span><span class="sxs-lookup"><span data-stu-id="29780-547">Finance</span></span></td>
<td><span data-ttu-id="29780-548">35</span><span class="sxs-lookup"><span data-stu-id="29780-548">35</span></span></td>
<td><span data-ttu-id="29780-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="29780-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="29780-550">436.00</span><span class="sxs-lookup"><span data-stu-id="29780-550">436.00</span></span></td>
<td><span data-ttu-id="29780-551">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-552">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-552">CC003</span></span></td>
<td><span data-ttu-id="29780-553">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-553">Assembly</span></span></td>
<td><span data-ttu-id="29780-554">55</span><span class="sxs-lookup"><span data-stu-id="29780-554">55</span></span></td>
<td><span data-ttu-id="29780-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="29780-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="29780-556">685.14</span><span class="sxs-lookup"><span data-stu-id="29780-556">685.14</span></span></td>
<td><span data-ttu-id="29780-557">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-558">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-558">CC004</span></span></td>
<td><span data-ttu-id="29780-559">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-559">Packaging</span></span></td>
<td><span data-ttu-id="29780-560">10</span><span class="sxs-lookup"><span data-stu-id="29780-560">10</span></span></td>
<td><span data-ttu-id="29780-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="29780-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="29780-562">124.57</span><span class="sxs-lookup"><span data-stu-id="29780-562">124.57</span></span></td>
<td><span data-ttu-id="29780-563">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-564">次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-565">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-565">Cost object</span></span></th>
<th><span data-ttu-id="29780-566">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-566">Magnitude</span></span></th>
<th><span data-ttu-id="29780-567">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-567">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-568">金額</span><span class="sxs-lookup"><span data-stu-id="29780-568">Amount</span></span></th>
<th><span data-ttu-id="29780-569">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-570">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-570">CC003</span></span></td>
<td><span data-ttu-id="29780-571">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-571">Assembly</span></span></td>
<td><span data-ttu-id="29780-572">65</span><span class="sxs-lookup"><span data-stu-id="29780-572">65</span></span></td>
<td><span data-ttu-id="29780-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="29780-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="29780-574">438.75</span><span class="sxs-lookup"><span data-stu-id="29780-574">438.75</span></span></td>
<td><span data-ttu-id="29780-575">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-576">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-576">CC004</span></span></td>
<td><span data-ttu-id="29780-577">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-577">Packaging</span></span></td>
<td><span data-ttu-id="29780-578">35</span><span class="sxs-lookup"><span data-stu-id="29780-578">35</span></span></td>
<td><span data-ttu-id="29780-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="29780-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="29780-580">236.25</span><span class="sxs-lookup"><span data-stu-id="29780-580">236.25</span></span></td>
<td><span data-ttu-id="29780-581">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-582">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-582">CC003</span></span></td>
<td><span data-ttu-id="29780-583">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-583">Assembly</span></span></td>
<td><span data-ttu-id="29780-584">65</span><span class="sxs-lookup"><span data-stu-id="29780-584">65</span></span></td>
<td><span data-ttu-id="29780-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="29780-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="29780-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="29780-586">5,297.69</span></span></td>
<td><span data-ttu-id="29780-587">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-588">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-588">CC004</span></span></td>
<td><span data-ttu-id="29780-589">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-589">Packaging</span></span></td>
<td><span data-ttu-id="29780-590">35</span><span class="sxs-lookup"><span data-stu-id="29780-590">35</span></span></td>
<td><span data-ttu-id="29780-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="29780-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="29780-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="29780-592">2,852.60</span></span></td>
<td><span data-ttu-id="29780-593">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-594">次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-595">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-595">Cost object</span></span></th>
<th><span data-ttu-id="29780-596">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-596">Magnitude</span></span></th>
<th><span data-ttu-id="29780-597">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-597">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-598">金額</span><span class="sxs-lookup"><span data-stu-id="29780-598">Amount</span></span></th>
<th><span data-ttu-id="29780-599">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-600">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-600">Prod 1</span></span></td>
<td><span data-ttu-id="29780-601">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-601">Product 1</span></span></td>
<td><span data-ttu-id="29780-602">60</span><span class="sxs-lookup"><span data-stu-id="29780-602">60</span></span></td>
<td><span data-ttu-id="29780-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="29780-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="29780-604">535.31</span><span class="sxs-lookup"><span data-stu-id="29780-604">535.31</span></span></td>
<td><span data-ttu-id="29780-605">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-606">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-606">Prod 2</span></span></td>
<td><span data-ttu-id="29780-607">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-607">Product 2</span></span></td>
<td><span data-ttu-id="29780-608">20</span><span class="sxs-lookup"><span data-stu-id="29780-608">20</span></span></td>
<td><span data-ttu-id="29780-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="29780-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="29780-610">178.44</span><span class="sxs-lookup"><span data-stu-id="29780-610">178.44</span></span></td>
<td><span data-ttu-id="29780-611">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-612">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-612">Prod 1</span></span></td>
<td><span data-ttu-id="29780-613">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-613">Product 1</span></span></td>
<td><span data-ttu-id="29780-614">60</span><span class="sxs-lookup"><span data-stu-id="29780-614">60</span></span></td>
<td><span data-ttu-id="29780-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="29780-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="29780-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="29780-616">4,487.12</span></span></td>
<td><span data-ttu-id="29780-617">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-618">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-618">Prod 2</span></span></td>
<td><span data-ttu-id="29780-619">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-619">Product 2</span></span></td>
<td><span data-ttu-id="29780-620">20</span><span class="sxs-lookup"><span data-stu-id="29780-620">20</span></span></td>
<td><span data-ttu-id="29780-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="29780-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="29780-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="29780-622">1,495.71</span></span></td>
<td><span data-ttu-id="29780-623">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="29780-624">次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="29780-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-625">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-625">Cost object</span></span></th>
<th><span data-ttu-id="29780-626">大きさ</span><span class="sxs-lookup"><span data-stu-id="29780-626">Magnitude</span></span></th>
<th><span data-ttu-id="29780-627">配賦係数</span><span class="sxs-lookup"><span data-stu-id="29780-627">Allocation factor</span></span></th>
<th><span data-ttu-id="29780-628">金額</span><span class="sxs-lookup"><span data-stu-id="29780-628">Amount</span></span></th>
<th><span data-ttu-id="29780-629">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-630">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-630">Prod 1</span></span></td>
<td><span data-ttu-id="29780-631">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-631">Product 1</span></span></td>
<td><span data-ttu-id="29780-632">80</span><span class="sxs-lookup"><span data-stu-id="29780-632">80</span></span></td>
<td><span data-ttu-id="29780-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="29780-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="29780-634">241.05</span><span class="sxs-lookup"><span data-stu-id="29780-634">241.05</span></span></td>
<td><span data-ttu-id="29780-635">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-636">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-636">Prod 2</span></span></td>
<td><span data-ttu-id="29780-637">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-637">Product 2</span></span></td>
<td><span data-ttu-id="29780-638">15</span><span class="sxs-lookup"><span data-stu-id="29780-638">15</span></span></td>
<td><span data-ttu-id="29780-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="29780-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="29780-640">45.20</span><span class="sxs-lookup"><span data-stu-id="29780-640">45.20</span></span></td>
<td><span data-ttu-id="29780-641">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-642">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-642">Prod 1</span></span></td>
<td><span data-ttu-id="29780-643">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-643">Product 1</span></span></td>
<td><span data-ttu-id="29780-644">80</span><span class="sxs-lookup"><span data-stu-id="29780-644">80</span></span></td>
<td><span data-ttu-id="29780-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="29780-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="29780-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="29780-646">2,507.09</span></span></td>
<td><span data-ttu-id="29780-647">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-648">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-648">Prod 2</span></span></td>
<td><span data-ttu-id="29780-649">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-649">Product 2</span></span></td>
<td><span data-ttu-id="29780-650">15</span><span class="sxs-lookup"><span data-stu-id="29780-650">15</span></span></td>
<td><span data-ttu-id="29780-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="29780-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="29780-652">470.08</span><span class="sxs-lookup"><span data-stu-id="29780-652">470.08</span></span></td>
<td><span data-ttu-id="29780-653">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="29780-654">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="29780-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-655">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-655">Journal</span></span></th>
<th><span data-ttu-id="29780-656">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="29780-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="29780-657">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="29780-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="29780-658">バージョン</span><span class="sxs-lookup"><span data-stu-id="29780-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-659">00004</span><span class="sxs-lookup"><span data-stu-id="29780-659">00004</span></span></td>
<td><span data-ttu-id="29780-660">原価配賦仕訳帳</span><span class="sxs-lookup"><span data-stu-id="29780-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="29780-661">会計年度</span><span class="sxs-lookup"><span data-stu-id="29780-661">Fiscal</span></span></td>
<td><span data-ttu-id="29780-662">2017</span><span class="sxs-lookup"><span data-stu-id="29780-662">2017</span></span></td>
<td><span data-ttu-id="29780-663">期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-663">Period 1</span></span></td>
<td><span data-ttu-id="29780-664">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="29780-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="29780-665">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="29780-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="29780-666">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="29780-667">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-668">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-668">Cost element</span></span></th>
<th><span data-ttu-id="29780-669">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-669">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-670">金額</span><span class="sxs-lookup"><span data-stu-id="29780-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-671">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-672">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-672">CC001</span></span></td>
<td><span data-ttu-id="29780-673">HR</span><span class="sxs-lookup"><span data-stu-id="29780-673">HR</span></span></td>
<td><span data-ttu-id="29780-674">10001</span><span class="sxs-lookup"><span data-stu-id="29780-674">10001</span></span></td>
<td><span data-ttu-id="29780-675">電気</span><span class="sxs-lookup"><span data-stu-id="29780-675">Electricity</span></span></td>
<td><span data-ttu-id="29780-676">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-676">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-677">500.00</span><span class="sxs-lookup"><span data-stu-id="29780-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-678">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-679">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-679">CC001</span></span></td>
<td><span data-ttu-id="29780-680">HR</span><span class="sxs-lookup"><span data-stu-id="29780-680">HR</span></span></td>
<td><span data-ttu-id="29780-681">10001</span><span class="sxs-lookup"><span data-stu-id="29780-681">10001</span></span></td>
<td><span data-ttu-id="29780-682">電気</span><span class="sxs-lookup"><span data-stu-id="29780-682">Electricity</span></span></td>
<td><span data-ttu-id="29780-683">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-683">Variable cost</span></span></td>
<td><span data-ttu-id="29780-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="29780-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-685">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-686">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-686">CC002</span></span></td>
<td><span data-ttu-id="29780-687">財務</span><span class="sxs-lookup"><span data-stu-id="29780-687">Finance</span></span></td>
<td><span data-ttu-id="29780-688">10001</span><span class="sxs-lookup"><span data-stu-id="29780-688">10001</span></span></td>
<td><span data-ttu-id="29780-689">電気</span><span class="sxs-lookup"><span data-stu-id="29780-689">Electricity</span></span></td>
<td><span data-ttu-id="29780-690">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-690">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-691">675.00</span><span class="sxs-lookup"><span data-stu-id="29780-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-692">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-693">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-693">CC002</span></span></td>
<td><span data-ttu-id="29780-694">財務</span><span class="sxs-lookup"><span data-stu-id="29780-694">Finance</span></span></td>
<td><span data-ttu-id="29780-695">10001</span><span class="sxs-lookup"><span data-stu-id="29780-695">10001</span></span></td>
<td><span data-ttu-id="29780-696">電気</span><span class="sxs-lookup"><span data-stu-id="29780-696">Electricity</span></span></td>
<td><span data-ttu-id="29780-697">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-697">Variable cost</span></span></td>
<td><span data-ttu-id="29780-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="29780-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-699">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-700">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-700">CC003</span></span></td>
<td><span data-ttu-id="29780-701">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-701">Assembly</span></span></td>
<td><span data-ttu-id="29780-702">10001</span><span class="sxs-lookup"><span data-stu-id="29780-702">10001</span></span></td>
<td><span data-ttu-id="29780-703">電気</span><span class="sxs-lookup"><span data-stu-id="29780-703">Electricity</span></span></td>
<td><span data-ttu-id="29780-704">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-704">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-705">713.75</span><span class="sxs-lookup"><span data-stu-id="29780-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-706">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-707">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-707">CC003</span></span></td>
<td><span data-ttu-id="29780-708">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-708">Assembly</span></span></td>
<td><span data-ttu-id="29780-709">10001</span><span class="sxs-lookup"><span data-stu-id="29780-709">10001</span></span></td>
<td><span data-ttu-id="29780-710">電気</span><span class="sxs-lookup"><span data-stu-id="29780-710">Electricity</span></span></td>
<td><span data-ttu-id="29780-711">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-711">Variable cost</span></span></td>
<td><span data-ttu-id="29780-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="29780-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-713">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-714">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-714">CC003</span></span></td>
<td><span data-ttu-id="29780-715">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-715">Packaging</span></span></td>
<td><span data-ttu-id="29780-716">10001</span><span class="sxs-lookup"><span data-stu-id="29780-716">10001</span></span></td>
<td><span data-ttu-id="29780-717">電気</span><span class="sxs-lookup"><span data-stu-id="29780-717">Electricity</span></span></td>
<td><span data-ttu-id="29780-718">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-718">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-719">286.25</span><span class="sxs-lookup"><span data-stu-id="29780-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-720">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-721">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-721">CC003</span></span></td>
<td><span data-ttu-id="29780-722">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-722">Packaging</span></span></td>
<td><span data-ttu-id="29780-723">10001</span><span class="sxs-lookup"><span data-stu-id="29780-723">10001</span></span></td>
<td><span data-ttu-id="29780-724">電気</span><span class="sxs-lookup"><span data-stu-id="29780-724">Electricity</span></span></td>
<td><span data-ttu-id="29780-725">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-725">Variable cost</span></span></td>
<td><span data-ttu-id="29780-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="29780-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-727">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-728">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-728">Prod 1</span></span></td>
<td><span data-ttu-id="29780-729">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-729">Product 1</span></span></td>
<td><span data-ttu-id="29780-730">10001</span><span class="sxs-lookup"><span data-stu-id="29780-730">10001</span></span></td>
<td><span data-ttu-id="29780-731">電気</span><span class="sxs-lookup"><span data-stu-id="29780-731">Electricity</span></span></td>
<td><span data-ttu-id="29780-732">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-732">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-733">776.36</span><span class="sxs-lookup"><span data-stu-id="29780-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-734">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-735">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-735">Prod 1</span></span></td>
<td><span data-ttu-id="29780-736">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-736">Product 1</span></span></td>
<td><span data-ttu-id="29780-737">10001</span><span class="sxs-lookup"><span data-stu-id="29780-737">10001</span></span></td>
<td><span data-ttu-id="29780-738">電気</span><span class="sxs-lookup"><span data-stu-id="29780-738">Electricity</span></span></td>
<td><span data-ttu-id="29780-739">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-739">Variable cost</span></span></td>
<td><span data-ttu-id="29780-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="29780-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-741">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-742">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-742">Prod 2</span></span></td>
<td><span data-ttu-id="29780-743">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-743">Product 1</span></span></td>
<td><span data-ttu-id="29780-744">10001</span><span class="sxs-lookup"><span data-stu-id="29780-744">10001</span></span></td>
<td><span data-ttu-id="29780-745">電気</span><span class="sxs-lookup"><span data-stu-id="29780-745">Electricity</span></span></td>
<td><span data-ttu-id="29780-746">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-746">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-747">223.64</span><span class="sxs-lookup"><span data-stu-id="29780-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-748">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="29780-749">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-749">Prod 2</span></span></td>
<td><span data-ttu-id="29780-750">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-750">Product 1</span></span></td>
<td><span data-ttu-id="29780-751">10001</span><span class="sxs-lookup"><span data-stu-id="29780-751">10001</span></span></td>
<td><span data-ttu-id="29780-752">電気</span><span class="sxs-lookup"><span data-stu-id="29780-752">Electricity</span></span></td>
<td><span data-ttu-id="29780-753">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-753">Variable cost</span></span></td>
<td><span data-ttu-id="29780-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="29780-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="29780-755">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="29780-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="29780-756">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="29780-757">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-757">Cost element</span></span></th>
<th><span data-ttu-id="29780-758">原価動作</span><span class="sxs-lookup"><span data-stu-id="29780-758">Cost behavior</span></span></th>
<th><span data-ttu-id="29780-759">金額</span><span class="sxs-lookup"><span data-stu-id="29780-759">Amount</span></span></th>
<th><span data-ttu-id="29780-760">会計日</span><span class="sxs-lookup"><span data-stu-id="29780-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29780-761">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-761">CC001</span></span></td>
<td><span data-ttu-id="29780-762">HR</span><span class="sxs-lookup"><span data-stu-id="29780-762">HR</span></span></td>
<td><span data-ttu-id="29780-763">10001</span><span class="sxs-lookup"><span data-stu-id="29780-763">10001</span></span></td>
<td><span data-ttu-id="29780-764">電気</span><span class="sxs-lookup"><span data-stu-id="29780-764">Electricity</span></span></td>
<td><span data-ttu-id="29780-765">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-765">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="29780-766">-500.00</span></span></td>
<td><span data-ttu-id="29780-767">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-768">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-768">CC002</span></span></td>
<td><span data-ttu-id="29780-769">財務</span><span class="sxs-lookup"><span data-stu-id="29780-769">Finance</span></span></td>
<td><span data-ttu-id="29780-770">10001</span><span class="sxs-lookup"><span data-stu-id="29780-770">10001</span></span></td>
<td><span data-ttu-id="29780-771">電気</span><span class="sxs-lookup"><span data-stu-id="29780-771">Electricity</span></span></td>
<td><span data-ttu-id="29780-772">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-772">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-773">175.00</span><span class="sxs-lookup"><span data-stu-id="29780-773">175.00</span></span></td>
<td><span data-ttu-id="29780-774">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-775">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-775">CC003</span></span></td>
<td><span data-ttu-id="29780-776">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-776">Assembly</span></span></td>
<td><span data-ttu-id="29780-777">10001</span><span class="sxs-lookup"><span data-stu-id="29780-777">10001</span></span></td>
<td><span data-ttu-id="29780-778">電気</span><span class="sxs-lookup"><span data-stu-id="29780-778">Electricity</span></span></td>
<td><span data-ttu-id="29780-779">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-779">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-780">275.00</span><span class="sxs-lookup"><span data-stu-id="29780-780">275.00</span></span></td>
<td><span data-ttu-id="29780-781">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-782">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-782">CC004</span></span></td>
<td><span data-ttu-id="29780-783">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-783">Packaging</span></span></td>
<td><span data-ttu-id="29780-784">10001</span><span class="sxs-lookup"><span data-stu-id="29780-784">10001</span></span></td>
<td><span data-ttu-id="29780-785">電気</span><span class="sxs-lookup"><span data-stu-id="29780-785">Electricity</span></span></td>
<td><span data-ttu-id="29780-786">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-786">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-787">50,00</span><span class="sxs-lookup"><span data-stu-id="29780-787">50,00</span></span></td>
<td><span data-ttu-id="29780-788">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-789">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-789">CC001</span></span></td>
<td><span data-ttu-id="29780-790">HR</span><span class="sxs-lookup"><span data-stu-id="29780-790">HR</span></span></td>
<td><span data-ttu-id="29780-791">10001</span><span class="sxs-lookup"><span data-stu-id="29780-791">10001</span></span></td>
<td><span data-ttu-id="29780-792">電気</span><span class="sxs-lookup"><span data-stu-id="29780-792">Electricity</span></span></td>
<td><span data-ttu-id="29780-793">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-793">Variable cost</span></span></td>
<td><span data-ttu-id="29780-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="29780-794">-1,245.71</span></span></td>
<td><span data-ttu-id="29780-795">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-796">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-796">CC002</span></span></td>
<td><span data-ttu-id="29780-797">財務</span><span class="sxs-lookup"><span data-stu-id="29780-797">Finance</span></span></td>
<td><span data-ttu-id="29780-798">10001</span><span class="sxs-lookup"><span data-stu-id="29780-798">10001</span></span></td>
<td><span data-ttu-id="29780-799">電気</span><span class="sxs-lookup"><span data-stu-id="29780-799">Electricity</span></span></td>
<td><span data-ttu-id="29780-800">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-800">Variable cost</span></span></td>
<td><span data-ttu-id="29780-801">436.00</span><span class="sxs-lookup"><span data-stu-id="29780-801">436.00</span></span></td>
<td><span data-ttu-id="29780-802">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-803">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-803">CC003</span></span></td>
<td><span data-ttu-id="29780-804">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-804">Assembly</span></span></td>
<td><span data-ttu-id="29780-805">10001</span><span class="sxs-lookup"><span data-stu-id="29780-805">10001</span></span></td>
<td><span data-ttu-id="29780-806">電気</span><span class="sxs-lookup"><span data-stu-id="29780-806">Electricity</span></span></td>
<td><span data-ttu-id="29780-807">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-807">Variable cost</span></span></td>
<td><span data-ttu-id="29780-808">685.14</span><span class="sxs-lookup"><span data-stu-id="29780-808">685.14</span></span></td>
<td><span data-ttu-id="29780-809">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-810">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-810">CC004</span></span></td>
<td><span data-ttu-id="29780-811">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-811">Packaging</span></span></td>
<td><span data-ttu-id="29780-812">10001</span><span class="sxs-lookup"><span data-stu-id="29780-812">10001</span></span></td>
<td><span data-ttu-id="29780-813">電気</span><span class="sxs-lookup"><span data-stu-id="29780-813">Electricity</span></span></td>
<td><span data-ttu-id="29780-814">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-814">Variable cost</span></span></td>
<td><span data-ttu-id="29780-815">124.57</span><span class="sxs-lookup"><span data-stu-id="29780-815">124.57</span></span></td>
<td><span data-ttu-id="29780-816">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-817">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-817">CC002</span></span></td>
<td><span data-ttu-id="29780-818">財務</span><span class="sxs-lookup"><span data-stu-id="29780-818">Finance</span></span></td>
<td><span data-ttu-id="29780-819">10001</span><span class="sxs-lookup"><span data-stu-id="29780-819">10001</span></span></td>
<td><span data-ttu-id="29780-820">電気</span><span class="sxs-lookup"><span data-stu-id="29780-820">Electricity</span></span></td>
<td><span data-ttu-id="29780-821">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-821">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="29780-822">-675.00</span></span></td>
<td><span data-ttu-id="29780-823">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-824">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-824">CC003</span></span></td>
<td><span data-ttu-id="29780-825">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-825">Assembly</span></span></td>
<td><span data-ttu-id="29780-826">10001</span><span class="sxs-lookup"><span data-stu-id="29780-826">10001</span></span></td>
<td><span data-ttu-id="29780-827">電気</span><span class="sxs-lookup"><span data-stu-id="29780-827">Electricity</span></span></td>
<td><span data-ttu-id="29780-828">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-828">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-829">438.75</span><span class="sxs-lookup"><span data-stu-id="29780-829">438.75</span></span></td>
<td><span data-ttu-id="29780-830">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-831">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-831">CC004</span></span></td>
<td><span data-ttu-id="29780-832">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-832">Packaging</span></span></td>
<td><span data-ttu-id="29780-833">10001</span><span class="sxs-lookup"><span data-stu-id="29780-833">10001</span></span></td>
<td><span data-ttu-id="29780-834">電気</span><span class="sxs-lookup"><span data-stu-id="29780-834">Electricity</span></span></td>
<td><span data-ttu-id="29780-835">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-835">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-836">236.25</span><span class="sxs-lookup"><span data-stu-id="29780-836">236.25</span></span></td>
<td><span data-ttu-id="29780-837">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-838">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-838">CC002</span></span></td>
<td><span data-ttu-id="29780-839">財務</span><span class="sxs-lookup"><span data-stu-id="29780-839">Finance</span></span></td>
<td><span data-ttu-id="29780-840">10001</span><span class="sxs-lookup"><span data-stu-id="29780-840">10001</span></span></td>
<td><span data-ttu-id="29780-841">電気</span><span class="sxs-lookup"><span data-stu-id="29780-841">Electricity</span></span></td>
<td><span data-ttu-id="29780-842">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-842">Variable cost</span></span></td>
<td><span data-ttu-id="29780-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="29780-843">-8,150.29</span></span></td>
<td><span data-ttu-id="29780-844">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-845">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-845">CC003</span></span></td>
<td><span data-ttu-id="29780-846">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-846">Assembly</span></span></td>
<td><span data-ttu-id="29780-847">10001</span><span class="sxs-lookup"><span data-stu-id="29780-847">10001</span></span></td>
<td><span data-ttu-id="29780-848">電気</span><span class="sxs-lookup"><span data-stu-id="29780-848">Electricity</span></span></td>
<td><span data-ttu-id="29780-849">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-849">Variable cost</span></span></td>
<td><span data-ttu-id="29780-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="29780-850">5,297.69</span></span></td>
<td><span data-ttu-id="29780-851">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-852">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-852">CC004</span></span></td>
<td><span data-ttu-id="29780-853">梱包業</span><span class="sxs-lookup"><span data-stu-id="29780-853">Packaging</span></span></td>
<td><span data-ttu-id="29780-854">10001</span><span class="sxs-lookup"><span data-stu-id="29780-854">10001</span></span></td>
<td><span data-ttu-id="29780-855">電気</span><span class="sxs-lookup"><span data-stu-id="29780-855">Electricity</span></span></td>
<td><span data-ttu-id="29780-856">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-856">Variable cost</span></span></td>
<td><span data-ttu-id="29780-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="29780-857">2,852.60</span></span></td>
<td><span data-ttu-id="29780-858">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-859">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-859">CC003</span></span></td>
<td><span data-ttu-id="29780-860">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-860">Assembly</span></span></td>
<td><span data-ttu-id="29780-861">10001</span><span class="sxs-lookup"><span data-stu-id="29780-861">10001</span></span></td>
<td><span data-ttu-id="29780-862">電気</span><span class="sxs-lookup"><span data-stu-id="29780-862">Electricity</span></span></td>
<td><span data-ttu-id="29780-863">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-863">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="29780-864">-713.75</span></span></td>
<td><span data-ttu-id="29780-865">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-866">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-866">Prod 1</span></span></td>
<td><span data-ttu-id="29780-867">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-867">Product 1</span></span></td>
<td><span data-ttu-id="29780-868">10001</span><span class="sxs-lookup"><span data-stu-id="29780-868">10001</span></span></td>
<td><span data-ttu-id="29780-869">電気</span><span class="sxs-lookup"><span data-stu-id="29780-869">Electricity</span></span></td>
<td><span data-ttu-id="29780-870">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-870">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-871">535.31</span><span class="sxs-lookup"><span data-stu-id="29780-871">535.31</span></span></td>
<td><span data-ttu-id="29780-872">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-873">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-873">Prod 2</span></span></td>
<td><span data-ttu-id="29780-874">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-874">Product 2</span></span></td>
<td><span data-ttu-id="29780-875">10001</span><span class="sxs-lookup"><span data-stu-id="29780-875">10001</span></span></td>
<td><span data-ttu-id="29780-876">電気</span><span class="sxs-lookup"><span data-stu-id="29780-876">Electricity</span></span></td>
<td><span data-ttu-id="29780-877">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-877">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-878">178.44</span><span class="sxs-lookup"><span data-stu-id="29780-878">178.44</span></span></td>
<td><span data-ttu-id="29780-879">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-880">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-880">CC003</span></span></td>
<td><span data-ttu-id="29780-881">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-881">Assembly</span></span></td>
<td><span data-ttu-id="29780-882">10001</span><span class="sxs-lookup"><span data-stu-id="29780-882">10001</span></span></td>
<td><span data-ttu-id="29780-883">電気</span><span class="sxs-lookup"><span data-stu-id="29780-883">Electricity</span></span></td>
<td><span data-ttu-id="29780-884">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-884">Variable cost</span></span></td>
<td><span data-ttu-id="29780-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="29780-885">-5,982.83</span></span></td>
<td><span data-ttu-id="29780-886">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-887">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-887">Prod 1</span></span></td>
<td><span data-ttu-id="29780-888">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-888">Product 1</span></span></td>
<td><span data-ttu-id="29780-889">10001</span><span class="sxs-lookup"><span data-stu-id="29780-889">10001</span></span></td>
<td><span data-ttu-id="29780-890">電気</span><span class="sxs-lookup"><span data-stu-id="29780-890">Electricity</span></span></td>
<td><span data-ttu-id="29780-891">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-891">Variable cost</span></span></td>
<td><span data-ttu-id="29780-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="29780-892">4,487.12</span></span></td>
<td><span data-ttu-id="29780-893">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-894">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-894">Prod 2</span></span></td>
<td><span data-ttu-id="29780-895">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-895">Product 2</span></span></td>
<td><span data-ttu-id="29780-896">10001</span><span class="sxs-lookup"><span data-stu-id="29780-896">10001</span></span></td>
<td><span data-ttu-id="29780-897">電気</span><span class="sxs-lookup"><span data-stu-id="29780-897">Electricity</span></span></td>
<td><span data-ttu-id="29780-898">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-898">Variable cost</span></span></td>
<td><span data-ttu-id="29780-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="29780-899">1,495.71</span></span></td>
<td><span data-ttu-id="29780-900">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-901">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-901">CC003</span></span></td>
<td><span data-ttu-id="29780-902">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-902">Assembly</span></span></td>
<td><span data-ttu-id="29780-903">10001</span><span class="sxs-lookup"><span data-stu-id="29780-903">10001</span></span></td>
<td><span data-ttu-id="29780-904">電気</span><span class="sxs-lookup"><span data-stu-id="29780-904">Electricity</span></span></td>
<td><span data-ttu-id="29780-905">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-905">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="29780-906">-286.25</span></span></td>
<td><span data-ttu-id="29780-907">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-908">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-908">Prod 1</span></span></td>
<td><span data-ttu-id="29780-909">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-909">Product 1</span></span></td>
<td><span data-ttu-id="29780-910">10001</span><span class="sxs-lookup"><span data-stu-id="29780-910">10001</span></span></td>
<td><span data-ttu-id="29780-911">電気</span><span class="sxs-lookup"><span data-stu-id="29780-911">Electricity</span></span></td>
<td><span data-ttu-id="29780-912">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-912">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-913">241.05</span><span class="sxs-lookup"><span data-stu-id="29780-913">241.05</span></span></td>
<td><span data-ttu-id="29780-914">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-915">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-915">Prod 2</span></span></td>
<td><span data-ttu-id="29780-916">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-916">Product 2</span></span></td>
<td><span data-ttu-id="29780-917">10001</span><span class="sxs-lookup"><span data-stu-id="29780-917">10001</span></span></td>
<td><span data-ttu-id="29780-918">電気</span><span class="sxs-lookup"><span data-stu-id="29780-918">Electricity</span></span></td>
<td><span data-ttu-id="29780-919">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-919">Fixed cost</span></span></td>
<td><span data-ttu-id="29780-920">45.20</span><span class="sxs-lookup"><span data-stu-id="29780-920">45.20</span></span></td>
<td><span data-ttu-id="29780-921">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-922">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-922">CC003</span></span></td>
<td><span data-ttu-id="29780-923">組み立て</span><span class="sxs-lookup"><span data-stu-id="29780-923">Assembly</span></span></td>
<td><span data-ttu-id="29780-924">10001</span><span class="sxs-lookup"><span data-stu-id="29780-924">10001</span></span></td>
<td><span data-ttu-id="29780-925">電気</span><span class="sxs-lookup"><span data-stu-id="29780-925">Electricity</span></span></td>
<td><span data-ttu-id="29780-926">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-926">Variable cost</span></span></td>
<td><span data-ttu-id="29780-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="29780-927">-2,977.17</span></span></td>
<td><span data-ttu-id="29780-928">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-929">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-929">Prod 1</span></span></td>
<td><span data-ttu-id="29780-930">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-930">Product 1</span></span></td>
<td><span data-ttu-id="29780-931">10001</span><span class="sxs-lookup"><span data-stu-id="29780-931">10001</span></span></td>
<td><span data-ttu-id="29780-932">電気</span><span class="sxs-lookup"><span data-stu-id="29780-932">Electricity</span></span></td>
<td><span data-ttu-id="29780-933">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-933">Variable cost</span></span></td>
<td><span data-ttu-id="29780-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="29780-934">2,507.09</span></span></td>
<td><span data-ttu-id="29780-935">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29780-936">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-936">Prod 2</span></span></td>
<td><span data-ttu-id="29780-937">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-937">Product 2</span></span></td>
<td><span data-ttu-id="29780-938">10001</span><span class="sxs-lookup"><span data-stu-id="29780-938">10001</span></span></td>
<td><span data-ttu-id="29780-939">電気</span><span class="sxs-lookup"><span data-stu-id="29780-939">Electricity</span></span></td>
<td><span data-ttu-id="29780-940">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-940">Variable cost</span></span></td>
<td><span data-ttu-id="29780-941">470.08</span><span class="sxs-lookup"><span data-stu-id="29780-941">470.08</span></span></td>
<td><span data-ttu-id="29780-942">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="29780-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="29780-943">まとめ</span><span class="sxs-lookup"><span data-stu-id="29780-943">Conclusion</span></span>
<span data-ttu-id="29780-944">財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。</span><span class="sxs-lookup"><span data-stu-id="29780-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="29780-945">したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。</span><span class="sxs-lookup"><span data-stu-id="29780-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="29780-946">コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。</span><span class="sxs-lookup"><span data-stu-id="29780-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="29780-947">各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="29780-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="29780-948">原価要素</span><span class="sxs-lookup"><span data-stu-id="29780-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="29780-949">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="29780-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="29780-950">小計</span><span class="sxs-lookup"><span data-stu-id="29780-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29780-951">CC099</span><span class="sxs-lookup"><span data-stu-id="29780-951">CC099</span></span></th>
<th><span data-ttu-id="29780-952">CC001</span><span class="sxs-lookup"><span data-stu-id="29780-952">CC001</span></span></th>
<th><span data-ttu-id="29780-953">CC002</span><span class="sxs-lookup"><span data-stu-id="29780-953">CC002</span></span></th>
<th><span data-ttu-id="29780-954">CC003</span><span class="sxs-lookup"><span data-stu-id="29780-954">CC003</span></span></th>
<th><span data-ttu-id="29780-955">CC004</span><span class="sxs-lookup"><span data-stu-id="29780-955">CC004</span></span></th>
<th><span data-ttu-id="29780-956">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="29780-956">Proj 1</span></span></th>
<th><span data-ttu-id="29780-957">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="29780-957">Proj 2</span></span></th>
<th><span data-ttu-id="29780-958">製品 1</span><span class="sxs-lookup"><span data-stu-id="29780-958">Prod 1</span></span></th>
<th><span data-ttu-id="29780-959">製品 2</span><span class="sxs-lookup"><span data-stu-id="29780-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="29780-960">10001 電気</span><span class="sxs-lookup"><span data-stu-id="29780-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="29780-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="29780-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="29780-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="29780-970">未分類</span><span class="sxs-lookup"><span data-stu-id="29780-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-971">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="29780-972">固定費</span><span class="sxs-lookup"><span data-stu-id="29780-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-973">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-974">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-975">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-976">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-977">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="29780-978">776.36</span><span class="sxs-lookup"><span data-stu-id="29780-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-979">223.64</span><span class="sxs-lookup"><span data-stu-id="29780-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="29780-981">変動費</span><span class="sxs-lookup"><span data-stu-id="29780-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-982">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-983">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-984">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-985">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-986">0.00</span><span class="sxs-lookup"><span data-stu-id="29780-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-987">30.00</span><span class="sxs-lookup"><span data-stu-id="29780-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-988">10.00</span><span class="sxs-lookup"><span data-stu-id="29780-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="29780-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="29780-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="29780-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="29780-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="29780-992">このトピックでは、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。</span><span class="sxs-lookup"><span data-stu-id="29780-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="29780-993">したがって、この間接費は組織の最下位レベルに配賦されます。</span><span class="sxs-lookup"><span data-stu-id="29780-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="29780-994">つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。</span><span class="sxs-lookup"><span data-stu-id="29780-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="29780-995">コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="29780-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="29780-996">詳細については、「[原価ロールアップ](cost-rollup.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29780-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



