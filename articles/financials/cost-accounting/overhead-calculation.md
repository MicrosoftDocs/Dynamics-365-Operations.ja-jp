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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "335120"
---
# <a name="overhead-calculation"></a><span data-ttu-id="a1869-103">間接費の計算</span><span class="sxs-lookup"><span data-stu-id="a1869-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1869-104">このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a1869-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a1869-105">用語の定義</span><span class="sxs-lookup"><span data-stu-id="a1869-105">Term definition</span></span>
---------------

<span data-ttu-id="a1869-106">間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。</span><span class="sxs-lookup"><span data-stu-id="a1869-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a1869-107">間接費は、営利活動を生み出すのに不可欠な支援を提供します。</span><span class="sxs-lookup"><span data-stu-id="a1869-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a1869-108">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a1869-109">賃料</span><span class="sxs-lookup"><span data-stu-id="a1869-109">Rent</span></span>
-   <span data-ttu-id="a1869-110">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-110">Electricity</span></span>
-   <span data-ttu-id="a1869-111">管理給与</span><span class="sxs-lookup"><span data-stu-id="a1869-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a1869-112">間接費計算の概要</span><span class="sxs-lookup"><span data-stu-id="a1869-112">Overhead calculation overview</span></span>
<span data-ttu-id="a1869-113">間接費計算は、コスト会計ポリシーを正しい順序で実行します。</span><span class="sxs-lookup"><span data-stu-id="a1869-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a1869-114">コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a1869-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a1869-115">間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a1869-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a1869-116">間接費計算が生成するコスト エントリは転記日を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a1869-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a1869-117">この転記日は、計算に使用される会計年度期間の終了日と一致します。</span><span class="sxs-lookup"><span data-stu-id="a1869-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a1869-118">固有のバージョン ID は、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a1869-119">バージョン タイプ</span><span class="sxs-lookup"><span data-stu-id="a1869-119">Version type</span></span>
-   <span data-ttu-id="a1869-120">日時</span><span class="sxs-lookup"><span data-stu-id="a1869-120">Date and time</span></span>
-   <span data-ttu-id="a1869-121">原価会計元帳</span><span class="sxs-lookup"><span data-stu-id="a1869-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a1869-122">年度</span><span class="sxs-lookup"><span data-stu-id="a1869-122">Fiscal year</span></span>
-   <span data-ttu-id="a1869-123">会計年度期間</span><span class="sxs-lookup"><span data-stu-id="a1869-123">Fiscal period</span></span>

<span data-ttu-id="a1869-124">間接費計算は、バージョンとは無関係に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a1869-125">そのため、実際のバージョンの前に予算バージョンを計算することができます。</span><span class="sxs-lookup"><span data-stu-id="a1869-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a1869-126">間接費計算は、次の図に示されているように 4 つのステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a1869-127">各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a1869-128">この仕訳ヘッダーは、各計算ステップの入力データを保持します。</span><span class="sxs-lookup"><span data-stu-id="a1869-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a1869-129">ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a1869-130">そのため、常に完全なトレーサビリティがあります。</span><span class="sxs-lookup"><span data-stu-id="a1869-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a1869-131">[![間接費計算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a1869-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a1869-132">電気間接費の計算および配賦</span><span class="sxs-lookup"><span data-stu-id="a1869-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a1869-133">財務会計では、電気などの一部のコストは一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a1869-134">したがって、コスト会計には詳細な管理情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="a1869-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a1869-135">コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1869-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a1869-136">このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1869-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a1869-137">一般会計では、電気コストは以下の表に示されているように転記できます。</span><span class="sxs-lookup"><span data-stu-id="a1869-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-138">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-139">原価部門</span><span class="sxs-lookup"><span data-stu-id="a1869-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-140">主勘定</span><span class="sxs-lookup"><span data-stu-id="a1869-140">Main account</span></span></th>
<th><span data-ttu-id="a1869-141">会計通貨での金額</span><span class="sxs-lookup"><span data-stu-id="a1869-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-142">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a1869-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a1869-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-143">CC099</span></span></td>
<td><span data-ttu-id="a1869-144">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-144">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-145">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-145">10001</span></span></td>
<td><span data-ttu-id="a1869-146">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-146">Electricity</span></span></td>
<td><span data-ttu-id="a1869-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a1869-148">手順 1: コスト動作計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a1869-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a1869-149">既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a1869-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a1869-150">コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。</span><span class="sxs-lookup"><span data-stu-id="a1869-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a1869-151">コスト動作ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a1869-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a1869-152">場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a1869-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a1869-153">電気代は多くの場合この定義と一致します。</span><span class="sxs-lookup"><span data-stu-id="a1869-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a1869-154">特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。</span><span class="sxs-lookup"><span data-stu-id="a1869-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a1869-155">たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a1869-156">固定金額 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a1869-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="a1869-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a1869-158">1000,01 &lt; N = 変動</span><span class="sxs-lookup"><span data-stu-id="a1869-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a1869-159">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-160">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-160">Journal</span></span></th>
<th><span data-ttu-id="a1869-161">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a1869-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1869-162">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a1869-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1869-163">バージョン</span><span class="sxs-lookup"><span data-stu-id="a1869-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-164">00001</span><span class="sxs-lookup"><span data-stu-id="a1869-164">00001</span></span></td>
<td><span data-ttu-id="a1869-165">原価動作計算仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a1869-166">会計年度</span><span class="sxs-lookup"><span data-stu-id="a1869-166">Fiscal</span></span></td>
<td><span data-ttu-id="a1869-167">2017</span><span class="sxs-lookup"><span data-stu-id="a1869-167">2017</span></span></td>
<td><span data-ttu-id="a1869-168">期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-168">Period 1</span></span></td>
<td><span data-ttu-id="a1869-169">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1869-170">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a1869-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-171">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-172">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-173">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-173">Cost element</span></span></th>
<th><span data-ttu-id="a1869-174">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-175">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-176">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a1869-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a1869-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-177">CC099</span></span></td>
<td><span data-ttu-id="a1869-178">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-178">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-179">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-179">10001</span></span></td>
<td><span data-ttu-id="a1869-180">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-180">Electricity</span></span></td>
<td><span data-ttu-id="a1869-181">未分類</span><span class="sxs-lookup"><span data-stu-id="a1869-181">Unclassified</span></span></td>
<td><span data-ttu-id="a1869-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1869-183">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a1869-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-184">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-185">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-185">Cost element</span></span></th>
<th><span data-ttu-id="a1869-186">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-187">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-187">Amount</span></span></th>
<th><span data-ttu-id="a1869-188">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-189">CC099</span></span></td>
<td><span data-ttu-id="a1869-190">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-190">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-191">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-191">10001</span></span></td>
<td><span data-ttu-id="a1869-192">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-192">Electricity</span></span></td>
<td><span data-ttu-id="a1869-193">未分類</span><span class="sxs-lookup"><span data-stu-id="a1869-193">Unclassified</span></span></td>
<td><span data-ttu-id="a1869-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-194">10,000.00</span></span></td>
<td><span data-ttu-id="a1869-195">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a1869-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-196">CC099</span></span></td>
<td><span data-ttu-id="a1869-197">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-197">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-198">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-198">10001</span></span></td>
<td><span data-ttu-id="a1869-199">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-199">Electricity</span></span></td>
<td><span data-ttu-id="a1869-200">未分類</span><span class="sxs-lookup"><span data-stu-id="a1869-200">Unclassified</span></span></td>
<td><span data-ttu-id="a1869-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a1869-202">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-203">CC099</span></span></td>
<td><span data-ttu-id="a1869-204">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-204">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-205">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-205">10001</span></span></td>
<td><span data-ttu-id="a1869-206">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-206">Electricity</span></span></td>
<td><span data-ttu-id="a1869-207">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-208">1,000.00</span></span></td>
<td><span data-ttu-id="a1869-209">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-210">CC099</span></span></td>
<td><span data-ttu-id="a1869-211">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-211">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-212">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-212">10001</span></span></td>
<td><span data-ttu-id="a1869-213">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-213">Electricity</span></span></td>
<td><span data-ttu-id="a1869-214">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-214">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-215">9,000.00</span></span></td>
<td><span data-ttu-id="a1869-216">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-217">詳細については、「[原価動作ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1869-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a1869-218">手順 2: コスト配分計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a1869-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a1869-219">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a1869-220">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="a1869-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a1869-221">コスト配分ルールの定義</span><span class="sxs-lookup"><span data-stu-id="a1869-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a1869-222">財務会計では、電気コストは多くの場合一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a1869-223">コスト会計では、このアプローチは十分に詳細ではありません。</span><span class="sxs-lookup"><span data-stu-id="a1869-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a1869-224">変動費は個々のコスト オブジェクトに公平に配分する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1869-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a1869-225">最も論理的な配賦基準は、電気 (Kwh) の消費です。</span><span class="sxs-lookup"><span data-stu-id="a1869-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a1869-226">電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a1869-227">既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a1869-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-228">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-228">Cost object</span></span></th>
<th><span data-ttu-id="a1869-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="a1869-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-230">CC001</span></span></td>
<td><span data-ttu-id="a1869-231">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-231">HR</span></span></td>
<td><span data-ttu-id="a1869-232">1.000</span><span class="sxs-lookup"><span data-stu-id="a1869-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-233">CC002</span></span></td>
<td><span data-ttu-id="a1869-234">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-234">Finance</span></span></td>
<td><span data-ttu-id="a1869-235">6,000</span><span class="sxs-lookup"><span data-stu-id="a1869-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-236">CC003</span></span></td>
<td><span data-ttu-id="a1869-237">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-237">Assembly</span></span></td>
<td><span data-ttu-id="a1869-238">0</span><span class="sxs-lookup"><span data-stu-id="a1869-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-239">次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-240">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-240">Cost object</span></span></th>
<th><span data-ttu-id="a1869-241">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-241">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-242">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-243">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-244">CC001</span></span></td>
<td><span data-ttu-id="a1869-245">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-245">HR</span></span></td>
<td><span data-ttu-id="a1869-246">1.000</span><span class="sxs-lookup"><span data-stu-id="a1869-246">1,000</span></span></td>
<td><span data-ttu-id="a1869-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1869-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a1869-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-249">CC002</span></span></td>
<td><span data-ttu-id="a1869-250">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-250">Finance</span></span></td>
<td><span data-ttu-id="a1869-251">6,000</span><span class="sxs-lookup"><span data-stu-id="a1869-251">6,000</span></span></td>
<td><span data-ttu-id="a1869-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1869-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a1869-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-254">CC003</span></span></td>
<td><span data-ttu-id="a1869-255">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-255">Assembly</span></span></td>
<td><span data-ttu-id="a1869-256">0</span><span class="sxs-lookup"><span data-stu-id="a1869-256">0</span></span></td>
<td><span data-ttu-id="a1869-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a1869-258">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-259">固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1869-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a1869-260">フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-261">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-261">Cost object</span></span></th>
<th><span data-ttu-id="a1869-262">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="a1869-262">Formula</span></span></th>
<th><span data-ttu-id="a1869-263">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-263">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-264">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-265">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-266">CC001</span></span></td>
<td><span data-ttu-id="a1869-267">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-267">HR</span></span></td>
<td><span data-ttu-id="a1869-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1869-269">1</span><span class="sxs-lookup"><span data-stu-id="a1869-269">1</span></span></td>
<td><span data-ttu-id="a1869-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1869-271">500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-272">CC002</span></span></td>
<td><span data-ttu-id="a1869-273">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-273">Finance</span></span></td>
<td><span data-ttu-id="a1869-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1869-275">1</span><span class="sxs-lookup"><span data-stu-id="a1869-275">1</span></span></td>
<td><span data-ttu-id="a1869-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1869-277">500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-278">CC003</span></span></td>
<td><span data-ttu-id="a1869-279">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-279">Assembly</span></span></td>
<td><span data-ttu-id="a1869-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a1869-281">0</span><span class="sxs-lookup"><span data-stu-id="a1869-281">0</span></span></td>
<td><span data-ttu-id="a1869-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a1869-283">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a1869-284">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-285">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-285">Journal</span></span></th>
<th><span data-ttu-id="a1869-286">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a1869-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1869-287">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a1869-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1869-288">バージョン</span><span class="sxs-lookup"><span data-stu-id="a1869-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-289">00002</span><span class="sxs-lookup"><span data-stu-id="a1869-289">00002</span></span></td>
<td><span data-ttu-id="a1869-290">コスト配分計算仕訳</span><span class="sxs-lookup"><span data-stu-id="a1869-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a1869-291">会計年度</span><span class="sxs-lookup"><span data-stu-id="a1869-291">Fiscal</span></span></td>
<td><span data-ttu-id="a1869-292">2017</span><span class="sxs-lookup"><span data-stu-id="a1869-292">2017</span></span></td>
<td><span data-ttu-id="a1869-293">期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-293">Period 1</span></span></td>
<td><span data-ttu-id="a1869-294">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1869-295">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a1869-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-296">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-297">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-298">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-298">Cost element</span></span></th>
<th><span data-ttu-id="a1869-299">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-300">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-301">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-302">CC099</span></span></td>
<td><span data-ttu-id="a1869-303">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-303">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-304">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-304">10001</span></span></td>
<td><span data-ttu-id="a1869-305">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-305">Electricity</span></span></td>
<td><span data-ttu-id="a1869-306">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-308">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-309">CC099</span></span></td>
<td><span data-ttu-id="a1869-310">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-310">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-311">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-311">10001</span></span></td>
<td><span data-ttu-id="a1869-312">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-312">Electricity</span></span></td>
<td><span data-ttu-id="a1869-313">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-313">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1869-315">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a1869-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-316">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-317">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-317">Cost element</span></span></th>
<th><span data-ttu-id="a1869-318">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-319">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-319">Amount</span></span></th>
<th><span data-ttu-id="a1869-320">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-321">CC099</span></span></td>
<td><span data-ttu-id="a1869-322">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-322">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-323">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-323">10001</span></span></td>
<td><span data-ttu-id="a1869-324">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-324">Electricity</span></span></td>
<td><span data-ttu-id="a1869-325">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a1869-327">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-328">CC001</span></span></td>
<td><span data-ttu-id="a1869-329">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-329">HR</span></span></td>
<td><span data-ttu-id="a1869-330">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-330">10001</span></span></td>
<td><span data-ttu-id="a1869-331">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-331">Electricity</span></span></td>
<td><span data-ttu-id="a1869-332">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-333">500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-333">500.00</span></span></td>
<td><span data-ttu-id="a1869-334">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-335">CC002</span></span></td>
<td><span data-ttu-id="a1869-336">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-336">Finance</span></span></td>
<td><span data-ttu-id="a1869-337">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-337">10001</span></span></td>
<td><span data-ttu-id="a1869-338">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-338">Electricity</span></span></td>
<td><span data-ttu-id="a1869-339">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-340">500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-340">500.00</span></span></td>
<td><span data-ttu-id="a1869-341">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-342">CC099</span></span></td>
<td><span data-ttu-id="a1869-343">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="a1869-343">Default cost center</span></span></td>
<td><span data-ttu-id="a1869-344">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-344">10001</span></span></td>
<td><span data-ttu-id="a1869-345">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-345">Electricity</span></span></td>
<td><span data-ttu-id="a1869-346">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-346">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a1869-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a1869-348">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-349">CC001</span></span></td>
<td><span data-ttu-id="a1869-350">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-350">HR</span></span></td>
<td><span data-ttu-id="a1869-351">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-351">10001</span></span></td>
<td><span data-ttu-id="a1869-352">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-352">Electricity</span></span></td>
<td><span data-ttu-id="a1869-353">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-353">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a1869-354">1,285.71</span></span></td>
<td><span data-ttu-id="a1869-355">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-356">CC002</span></span></td>
<td><span data-ttu-id="a1869-357">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-357">Finance</span></span></td>
<td><span data-ttu-id="a1869-358">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-358">10001</span></span></td>
<td><span data-ttu-id="a1869-359">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-359">Electricity</span></span></td>
<td><span data-ttu-id="a1869-360">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-360">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a1869-361">7,714.29</span></span></td>
<td><span data-ttu-id="a1869-362">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-363">詳細については、「[原価配分ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1869-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a1869-364">手順 3: 間接費率の計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a1869-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a1869-365">間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a1869-366">請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。</span><span class="sxs-lookup"><span data-stu-id="a1869-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a1869-367">間接費率の定義</span><span class="sxs-lookup"><span data-stu-id="a1869-367">Define the overhead rate</span></span>

<span data-ttu-id="a1869-368">コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a1869-369">HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-370">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-370">Cost object</span></span></th>
<th><span data-ttu-id="a1869-371">時間</span><span class="sxs-lookup"><span data-stu-id="a1869-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-372">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-372">Proj 1</span></span></td>
<td><span data-ttu-id="a1869-373">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-373">Project 1</span></span></td>
<td><span data-ttu-id="a1869-374">3</span><span class="sxs-lookup"><span data-stu-id="a1869-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-375">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-375">Proj 2</span></span></td>
<td><span data-ttu-id="a1869-376">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-376">Project 2</span></span></td>
<td><span data-ttu-id="a1869-377">1</span><span class="sxs-lookup"><span data-stu-id="a1869-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-378">コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。</span><span class="sxs-lookup"><span data-stu-id="a1869-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-379">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-379">Cost object</span></span></th>
<th><span data-ttu-id="a1869-380">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-380">Cost element</span></span></th>
<th><span data-ttu-id="a1869-381">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-382">単位</span><span class="sxs-lookup"><span data-stu-id="a1869-382">Units</span></span></th>
<th><span data-ttu-id="a1869-383">率</span><span class="sxs-lookup"><span data-stu-id="a1869-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-384">CC001</span></span></td>
<td><span data-ttu-id="a1869-385">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-385">HR</span></span></td>
<td><span data-ttu-id="a1869-386">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-386">10001</span></span></td>
<td><span data-ttu-id="a1869-387">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-387">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-388">1</span><span class="sxs-lookup"><span data-stu-id="a1869-388">1</span></span></td>
<td><span data-ttu-id="a1869-389">10</span><span class="sxs-lookup"><span data-stu-id="a1869-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-390">次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-391">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-391">Cost object</span></span></th>
<th><span data-ttu-id="a1869-392">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-392">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-393">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-393">Cost element</span></span></th>
<th><span data-ttu-id="a1869-394">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-395">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-396">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-396">Proj 1</span></span></td>
<td><span data-ttu-id="a1869-397">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-397">Project 1</span></span></td>
<td><span data-ttu-id="a1869-398">3</span><span class="sxs-lookup"><span data-stu-id="a1869-398">3</span></span></td>
<td><span data-ttu-id="a1869-399">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-399">10001</span></span></td>
<td><span data-ttu-id="a1869-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a1869-401">30.00</span><span class="sxs-lookup"><span data-stu-id="a1869-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-402">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-402">Proj 2</span></span></td>
<td><span data-ttu-id="a1869-403">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-403">Project 2</span></span></td>
<td><span data-ttu-id="a1869-404">1</span><span class="sxs-lookup"><span data-stu-id="a1869-404">1</span></span></td>
<td><span data-ttu-id="a1869-405">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-405">10001</span></span></td>
<td><span data-ttu-id="a1869-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a1869-407">10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a1869-408">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-409">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-409">Journal</span></span></th>
<th><span data-ttu-id="a1869-410">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a1869-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1869-411">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a1869-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1869-412">バージョン</span><span class="sxs-lookup"><span data-stu-id="a1869-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-413">00003</span><span class="sxs-lookup"><span data-stu-id="a1869-413">00003</span></span></td>
<td><span data-ttu-id="a1869-414">間接比率計算仕訳</span><span class="sxs-lookup"><span data-stu-id="a1869-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a1869-415">会計年度</span><span class="sxs-lookup"><span data-stu-id="a1869-415">Fiscal</span></span></td>
<td><span data-ttu-id="a1869-416">2017</span><span class="sxs-lookup"><span data-stu-id="a1869-416">2017</span></span></td>
<td><span data-ttu-id="a1869-417">期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-417">Period 1</span></span></td>
<td><span data-ttu-id="a1869-418">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a1869-419">仕訳入力 (間接比率計算のための仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a1869-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-420">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-421">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-421">Cost object</span></span></th>
<th><span data-ttu-id="a1869-422">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-423">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-424">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-424">Proj 1</span></span></td>
<td><span data-ttu-id="a1869-425">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a1869-426">3.00</span><span class="sxs-lookup"><span data-stu-id="a1869-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-427">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-428">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-428">Proj 2</span></span></td>
<td><span data-ttu-id="a1869-429">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a1869-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a1869-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1869-431">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a1869-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-432">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-433">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-433">Cost element</span></span></th>
<th><span data-ttu-id="a1869-434">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-435">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-435">Amount</span></span></th>
<th><span data-ttu-id="a1869-436">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a1869-437">CC0001</span></span></td>
<td><span data-ttu-id="a1869-438">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-438">HR</span></span></td>
<td><span data-ttu-id="a1869-439">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-439">10001</span></span></td>
<td><span data-ttu-id="a1869-440">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-440">Electricity</span></span></td>
<td><span data-ttu-id="a1869-441">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-441">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="a1869-442">-30.00</span></span></td>
<td><span data-ttu-id="a1869-443">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-444">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-444">Proj 1</span></span></td>
<td><span data-ttu-id="a1869-445">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a1869-446">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-446">10001</span></span></td>
<td><span data-ttu-id="a1869-447">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-447">Electricity</span></span></td>
<td><span data-ttu-id="a1869-448">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-448">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-449">30.00</span><span class="sxs-lookup"><span data-stu-id="a1869-449">30.00</span></span></td>
<td><span data-ttu-id="a1869-450">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-451">CC001</span></span></td>
<td><span data-ttu-id="a1869-452">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-452">HR</span></span></td>
<td><span data-ttu-id="a1869-453">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-453">10001</span></span></td>
<td><span data-ttu-id="a1869-454">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-454">Electricity</span></span></td>
<td><span data-ttu-id="a1869-455">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-455">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-456">-10.00</span></span></td>
<td><span data-ttu-id="a1869-457">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-458">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-458">Proj 2</span></span></td>
<td><span data-ttu-id="a1869-459">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a1869-460">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-460">10001</span></span></td>
<td><span data-ttu-id="a1869-461">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-461">Electricity</span></span></td>
<td><span data-ttu-id="a1869-462">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-462">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-463">10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-463">10.00</span></span></td>
<td><span data-ttu-id="a1869-464">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-465">詳細については、「[間接費計算を実行する](cost-rollup.md#perform-overhead-calculation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1869-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a1869-466">手順 4: コスト配賦計算を処理する</span><span class="sxs-lookup"><span data-stu-id="a1869-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a1869-467">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a1869-468">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a1869-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="a1869-469">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a1869-470">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="a1869-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a1869-471">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a1869-472">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a1869-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a1869-473">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a1869-474">[![相互手法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a1869-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a1869-475">コスト配賦の定義</span><span class="sxs-lookup"><span data-stu-id="a1869-475">Define the cost allocation</span></span>

<span data-ttu-id="a1869-476">次に、コストのフローを追跡する方法を説明する簡単な例を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a1869-477">コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a1869-478">HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-479">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-479">Cost object</span></span></th>
<th><span data-ttu-id="a1869-480">HR サービス</span><span class="sxs-lookup"><span data-stu-id="a1869-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-481">CC002</span></span></td>
<td><span data-ttu-id="a1869-482">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-482">Finance</span></span></td>
<td><span data-ttu-id="a1869-483">35</span><span class="sxs-lookup"><span data-stu-id="a1869-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-484">CC003</span></span></td>
<td><span data-ttu-id="a1869-485">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-485">Assembly</span></span></td>
<td><span data-ttu-id="a1869-486">55</span><span class="sxs-lookup"><span data-stu-id="a1869-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-487">CC004</span></span></td>
<td><span data-ttu-id="a1869-488">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-488">Packaging</span></span></td>
<td><span data-ttu-id="a1869-489">10</span><span class="sxs-lookup"><span data-stu-id="a1869-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-490">コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a1869-491">財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-492">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-492">Cost object</span></span></th>
<th><span data-ttu-id="a1869-493">財務サービス</span><span class="sxs-lookup"><span data-stu-id="a1869-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-494">CC003</span></span></td>
<td><span data-ttu-id="a1869-495">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-495">Assembly</span></span></td>
<td><span data-ttu-id="a1869-496">65</span><span class="sxs-lookup"><span data-stu-id="a1869-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-497">CC004</span></span></td>
<td><span data-ttu-id="a1869-498">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-498">Packaging</span></span></td>
<td><span data-ttu-id="a1869-499">35</span><span class="sxs-lookup"><span data-stu-id="a1869-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-500">コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a1869-501">組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-502">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-502">Cost object</span></span></th>
<th><span data-ttu-id="a1869-503">組み立てサービス (時間)</span><span class="sxs-lookup"><span data-stu-id="a1869-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-504">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-504">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-505">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-505">Product 1</span></span></td>
<td><span data-ttu-id="a1869-506">60</span><span class="sxs-lookup"><span data-stu-id="a1869-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-507">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-507">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-508">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-508">Product 2</span></span></td>
<td><span data-ttu-id="a1869-509">20</span><span class="sxs-lookup"><span data-stu-id="a1869-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-510">コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="a1869-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a1869-511">梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-512">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-512">Cost object</span></span></th>
<th><span data-ttu-id="a1869-513">梱包業サービス (時間)</span><span class="sxs-lookup"><span data-stu-id="a1869-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-514">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-514">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-515">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-515">Product 1</span></span></td>
<td><span data-ttu-id="a1869-516">80</span><span class="sxs-lookup"><span data-stu-id="a1869-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-517">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-517">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-518">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-518">Product 2</span></span></td>
<td><span data-ttu-id="a1869-519">15</span><span class="sxs-lookup"><span data-stu-id="a1869-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a1869-520">Finance and Operations では、製品に消費される生産時間などの統計測定は、ソース データから抽出できます。</span><span class="sxs-lookup"><span data-stu-id="a1869-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a1869-521">詳細については、「[統計測定プロバイダー テンプレート](statistical-measure-provider-template.md#statistical-measure-provider-template)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1869-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a1869-522">次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-523">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-523">Cost object</span></span></th>
<th><span data-ttu-id="a1869-524">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-524">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-525">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-526">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-526">Amount</span></span></th>
<th><span data-ttu-id="a1869-527">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-528">CC002</span></span></td>
<td><span data-ttu-id="a1869-529">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-529">Finance</span></span></td>
<td><span data-ttu-id="a1869-530">35</span><span class="sxs-lookup"><span data-stu-id="a1869-530">35</span></span></td>
<td><span data-ttu-id="a1869-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1869-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a1869-532">175.00</span></span></td>
<td><span data-ttu-id="a1869-533">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-534">CC003</span></span></td>
<td><span data-ttu-id="a1869-535">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-535">Assembly</span></span></td>
<td><span data-ttu-id="a1869-536">55</span><span class="sxs-lookup"><span data-stu-id="a1869-536">55</span></span></td>
<td><span data-ttu-id="a1869-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1869-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a1869-538">275.00</span></span></td>
<td><span data-ttu-id="a1869-539">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-540">CC004</span></span></td>
<td><span data-ttu-id="a1869-541">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-541">Packaging</span></span></td>
<td><span data-ttu-id="a1869-542">10</span><span class="sxs-lookup"><span data-stu-id="a1869-542">10</span></span></td>
<td><span data-ttu-id="a1869-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a1869-544">50.00</span><span class="sxs-lookup"><span data-stu-id="a1869-544">50.00</span></span></td>
<td><span data-ttu-id="a1869-545">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-546">CC002</span></span></td>
<td><span data-ttu-id="a1869-547">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-547">Finance</span></span></td>
<td><span data-ttu-id="a1869-548">35</span><span class="sxs-lookup"><span data-stu-id="a1869-548">35</span></span></td>
<td><span data-ttu-id="a1869-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1869-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1869-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a1869-550">436.00</span></span></td>
<td><span data-ttu-id="a1869-551">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-552">CC003</span></span></td>
<td><span data-ttu-id="a1869-553">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-553">Assembly</span></span></td>
<td><span data-ttu-id="a1869-554">55</span><span class="sxs-lookup"><span data-stu-id="a1869-554">55</span></span></td>
<td><span data-ttu-id="a1869-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1869-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1869-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a1869-556">685.14</span></span></td>
<td><span data-ttu-id="a1869-557">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-558">CC004</span></span></td>
<td><span data-ttu-id="a1869-559">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-559">Packaging</span></span></td>
<td><span data-ttu-id="a1869-560">10</span><span class="sxs-lookup"><span data-stu-id="a1869-560">10</span></span></td>
<td><span data-ttu-id="a1869-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1869-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a1869-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a1869-562">124.57</span></span></td>
<td><span data-ttu-id="a1869-563">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-564">次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-565">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-565">Cost object</span></span></th>
<th><span data-ttu-id="a1869-566">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-566">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-567">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-568">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-568">Amount</span></span></th>
<th><span data-ttu-id="a1869-569">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-570">CC003</span></span></td>
<td><span data-ttu-id="a1869-571">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-571">Assembly</span></span></td>
<td><span data-ttu-id="a1869-572">65</span><span class="sxs-lookup"><span data-stu-id="a1869-572">65</span></span></td>
<td><span data-ttu-id="a1869-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a1869-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a1869-574">438.75</span></span></td>
<td><span data-ttu-id="a1869-575">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-576">CC004</span></span></td>
<td><span data-ttu-id="a1869-577">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-577">Packaging</span></span></td>
<td><span data-ttu-id="a1869-578">35</span><span class="sxs-lookup"><span data-stu-id="a1869-578">35</span></span></td>
<td><span data-ttu-id="a1869-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a1869-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a1869-580">236.25</span></span></td>
<td><span data-ttu-id="a1869-581">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-582">CC003</span></span></td>
<td><span data-ttu-id="a1869-583">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-583">Assembly</span></span></td>
<td><span data-ttu-id="a1869-584">65</span><span class="sxs-lookup"><span data-stu-id="a1869-584">65</span></span></td>
<td><span data-ttu-id="a1869-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a1869-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a1869-586">5,297.69</span></span></td>
<td><span data-ttu-id="a1869-587">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-588">CC004</span></span></td>
<td><span data-ttu-id="a1869-589">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-589">Packaging</span></span></td>
<td><span data-ttu-id="a1869-590">35</span><span class="sxs-lookup"><span data-stu-id="a1869-590">35</span></span></td>
<td><span data-ttu-id="a1869-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="a1869-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a1869-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a1869-592">2,852.60</span></span></td>
<td><span data-ttu-id="a1869-593">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-594">次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-595">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-595">Cost object</span></span></th>
<th><span data-ttu-id="a1869-596">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-596">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-597">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-598">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-598">Amount</span></span></th>
<th><span data-ttu-id="a1869-599">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-600">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-600">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-601">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-601">Product 1</span></span></td>
<td><span data-ttu-id="a1869-602">60</span><span class="sxs-lookup"><span data-stu-id="a1869-602">60</span></span></td>
<td><span data-ttu-id="a1869-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a1869-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a1869-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a1869-604">535.31</span></span></td>
<td><span data-ttu-id="a1869-605">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-606">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-606">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-607">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-607">Product 2</span></span></td>
<td><span data-ttu-id="a1869-608">20</span><span class="sxs-lookup"><span data-stu-id="a1869-608">20</span></span></td>
<td><span data-ttu-id="a1869-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="a1869-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a1869-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a1869-610">178.44</span></span></td>
<td><span data-ttu-id="a1869-611">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-612">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-612">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-613">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-613">Product 1</span></span></td>
<td><span data-ttu-id="a1869-614">60</span><span class="sxs-lookup"><span data-stu-id="a1869-614">60</span></span></td>
<td><span data-ttu-id="a1869-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a1869-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a1869-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a1869-616">4,487.12</span></span></td>
<td><span data-ttu-id="a1869-617">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-618">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-618">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-619">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-619">Product 2</span></span></td>
<td><span data-ttu-id="a1869-620">20</span><span class="sxs-lookup"><span data-stu-id="a1869-620">20</span></span></td>
<td><span data-ttu-id="a1869-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="a1869-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a1869-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a1869-622">1,495.71</span></span></td>
<td><span data-ttu-id="a1869-623">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a1869-624">次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-625">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-625">Cost object</span></span></th>
<th><span data-ttu-id="a1869-626">大きさ</span><span class="sxs-lookup"><span data-stu-id="a1869-626">Magnitude</span></span></th>
<th><span data-ttu-id="a1869-627">配賦係数</span><span class="sxs-lookup"><span data-stu-id="a1869-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a1869-628">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-628">Amount</span></span></th>
<th><span data-ttu-id="a1869-629">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-630">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-630">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-631">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-631">Product 1</span></span></td>
<td><span data-ttu-id="a1869-632">80</span><span class="sxs-lookup"><span data-stu-id="a1869-632">80</span></span></td>
<td><span data-ttu-id="a1869-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a1869-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a1869-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a1869-634">241.05</span></span></td>
<td><span data-ttu-id="a1869-635">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-636">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-636">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-637">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-637">Product 2</span></span></td>
<td><span data-ttu-id="a1869-638">15</span><span class="sxs-lookup"><span data-stu-id="a1869-638">15</span></span></td>
<td><span data-ttu-id="a1869-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="a1869-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a1869-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a1869-640">45.20</span></span></td>
<td><span data-ttu-id="a1869-641">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-642">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-642">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-643">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-643">Product 1</span></span></td>
<td><span data-ttu-id="a1869-644">80</span><span class="sxs-lookup"><span data-stu-id="a1869-644">80</span></span></td>
<td><span data-ttu-id="a1869-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a1869-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a1869-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a1869-646">2,507.09</span></span></td>
<td><span data-ttu-id="a1869-647">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-648">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-648">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-649">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-649">Product 2</span></span></td>
<td><span data-ttu-id="a1869-650">15</span><span class="sxs-lookup"><span data-stu-id="a1869-650">15</span></span></td>
<td><span data-ttu-id="a1869-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="a1869-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a1869-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a1869-652">470.08</span></span></td>
<td><span data-ttu-id="a1869-653">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a1869-654">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="a1869-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-655">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-655">Journal</span></span></th>
<th><span data-ttu-id="a1869-656">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="a1869-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a1869-657">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="a1869-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a1869-658">バージョン</span><span class="sxs-lookup"><span data-stu-id="a1869-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-659">00004</span><span class="sxs-lookup"><span data-stu-id="a1869-659">00004</span></span></td>
<td><span data-ttu-id="a1869-660">原価配賦仕訳帳</span><span class="sxs-lookup"><span data-stu-id="a1869-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a1869-661">会計年度</span><span class="sxs-lookup"><span data-stu-id="a1869-661">Fiscal</span></span></td>
<td><span data-ttu-id="a1869-662">2017</span><span class="sxs-lookup"><span data-stu-id="a1869-662">2017</span></span></td>
<td><span data-ttu-id="a1869-663">期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-663">Period 1</span></span></td>
<td><span data-ttu-id="a1869-664">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="a1869-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a1869-665">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="a1869-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1869-666">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-667">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-668">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-668">Cost element</span></span></th>
<th><span data-ttu-id="a1869-669">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-670">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-671">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-672">CC001</span></span></td>
<td><span data-ttu-id="a1869-673">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-673">HR</span></span></td>
<td><span data-ttu-id="a1869-674">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-674">10001</span></span></td>
<td><span data-ttu-id="a1869-675">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-675">Electricity</span></span></td>
<td><span data-ttu-id="a1869-676">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-677">500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-678">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-679">CC001</span></span></td>
<td><span data-ttu-id="a1869-680">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-680">HR</span></span></td>
<td><span data-ttu-id="a1869-681">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-681">10001</span></span></td>
<td><span data-ttu-id="a1869-682">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-682">Electricity</span></span></td>
<td><span data-ttu-id="a1869-683">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-683">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1869-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-685">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-686">CC002</span></span></td>
<td><span data-ttu-id="a1869-687">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-687">Finance</span></span></td>
<td><span data-ttu-id="a1869-688">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-688">10001</span></span></td>
<td><span data-ttu-id="a1869-689">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-689">Electricity</span></span></td>
<td><span data-ttu-id="a1869-690">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a1869-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-692">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-693">CC002</span></span></td>
<td><span data-ttu-id="a1869-694">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-694">Finance</span></span></td>
<td><span data-ttu-id="a1869-695">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-695">10001</span></span></td>
<td><span data-ttu-id="a1869-696">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-696">Electricity</span></span></td>
<td><span data-ttu-id="a1869-697">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-697">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a1869-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-699">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-700">CC003</span></span></td>
<td><span data-ttu-id="a1869-701">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-701">Assembly</span></span></td>
<td><span data-ttu-id="a1869-702">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-702">10001</span></span></td>
<td><span data-ttu-id="a1869-703">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-703">Electricity</span></span></td>
<td><span data-ttu-id="a1869-704">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a1869-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-706">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-707">CC003</span></span></td>
<td><span data-ttu-id="a1869-708">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-708">Assembly</span></span></td>
<td><span data-ttu-id="a1869-709">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-709">10001</span></span></td>
<td><span data-ttu-id="a1869-710">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-710">Electricity</span></span></td>
<td><span data-ttu-id="a1869-711">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-711">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a1869-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-713">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-714">CC003</span></span></td>
<td><span data-ttu-id="a1869-715">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-715">Packaging</span></span></td>
<td><span data-ttu-id="a1869-716">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-716">10001</span></span></td>
<td><span data-ttu-id="a1869-717">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-717">Electricity</span></span></td>
<td><span data-ttu-id="a1869-718">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a1869-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-720">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-721">CC003</span></span></td>
<td><span data-ttu-id="a1869-722">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-722">Packaging</span></span></td>
<td><span data-ttu-id="a1869-723">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-723">10001</span></span></td>
<td><span data-ttu-id="a1869-724">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-724">Electricity</span></span></td>
<td><span data-ttu-id="a1869-725">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-725">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a1869-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-727">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-728">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-728">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-729">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-729">Product 1</span></span></td>
<td><span data-ttu-id="a1869-730">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-730">10001</span></span></td>
<td><span data-ttu-id="a1869-731">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-731">Electricity</span></span></td>
<td><span data-ttu-id="a1869-732">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a1869-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-734">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-735">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-735">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-736">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-736">Product 1</span></span></td>
<td><span data-ttu-id="a1869-737">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-737">10001</span></span></td>
<td><span data-ttu-id="a1869-738">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-738">Electricity</span></span></td>
<td><span data-ttu-id="a1869-739">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-739">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a1869-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-741">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-742">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-742">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-743">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-743">Product 1</span></span></td>
<td><span data-ttu-id="a1869-744">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-744">10001</span></span></td>
<td><span data-ttu-id="a1869-745">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-745">Electricity</span></span></td>
<td><span data-ttu-id="a1869-746">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a1869-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-748">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a1869-749">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-749">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-750">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-750">Product 1</span></span></td>
<td><span data-ttu-id="a1869-751">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-751">10001</span></span></td>
<td><span data-ttu-id="a1869-752">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-752">Electricity</span></span></td>
<td><span data-ttu-id="a1869-753">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-753">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a1869-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a1869-755">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="a1869-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a1869-756">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a1869-757">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-757">Cost element</span></span></th>
<th><span data-ttu-id="a1869-758">原価動作</span><span class="sxs-lookup"><span data-stu-id="a1869-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a1869-759">金額</span><span class="sxs-lookup"><span data-stu-id="a1869-759">Amount</span></span></th>
<th><span data-ttu-id="a1869-760">会計日</span><span class="sxs-lookup"><span data-stu-id="a1869-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1869-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-761">CC001</span></span></td>
<td><span data-ttu-id="a1869-762">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-762">HR</span></span></td>
<td><span data-ttu-id="a1869-763">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-763">10001</span></span></td>
<td><span data-ttu-id="a1869-764">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-764">Electricity</span></span></td>
<td><span data-ttu-id="a1869-765">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="a1869-766">-500.00</span></span></td>
<td><span data-ttu-id="a1869-767">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-768">CC002</span></span></td>
<td><span data-ttu-id="a1869-769">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-769">Finance</span></span></td>
<td><span data-ttu-id="a1869-770">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-770">10001</span></span></td>
<td><span data-ttu-id="a1869-771">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-771">Electricity</span></span></td>
<td><span data-ttu-id="a1869-772">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a1869-773">175.00</span></span></td>
<td><span data-ttu-id="a1869-774">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-775">CC003</span></span></td>
<td><span data-ttu-id="a1869-776">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-776">Assembly</span></span></td>
<td><span data-ttu-id="a1869-777">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-777">10001</span></span></td>
<td><span data-ttu-id="a1869-778">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-778">Electricity</span></span></td>
<td><span data-ttu-id="a1869-779">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a1869-780">275.00</span></span></td>
<td><span data-ttu-id="a1869-781">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-782">CC004</span></span></td>
<td><span data-ttu-id="a1869-783">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-783">Packaging</span></span></td>
<td><span data-ttu-id="a1869-784">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-784">10001</span></span></td>
<td><span data-ttu-id="a1869-785">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-785">Electricity</span></span></td>
<td><span data-ttu-id="a1869-786">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a1869-787">50,00</span></span></td>
<td><span data-ttu-id="a1869-788">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-789">CC001</span></span></td>
<td><span data-ttu-id="a1869-790">HR</span><span class="sxs-lookup"><span data-stu-id="a1869-790">HR</span></span></td>
<td><span data-ttu-id="a1869-791">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-791">10001</span></span></td>
<td><span data-ttu-id="a1869-792">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-792">Electricity</span></span></td>
<td><span data-ttu-id="a1869-793">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-793">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a1869-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a1869-795">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-796">CC002</span></span></td>
<td><span data-ttu-id="a1869-797">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-797">Finance</span></span></td>
<td><span data-ttu-id="a1869-798">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-798">10001</span></span></td>
<td><span data-ttu-id="a1869-799">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-799">Electricity</span></span></td>
<td><span data-ttu-id="a1869-800">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-800">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a1869-801">436.00</span></span></td>
<td><span data-ttu-id="a1869-802">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-803">CC003</span></span></td>
<td><span data-ttu-id="a1869-804">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-804">Assembly</span></span></td>
<td><span data-ttu-id="a1869-805">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-805">10001</span></span></td>
<td><span data-ttu-id="a1869-806">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-806">Electricity</span></span></td>
<td><span data-ttu-id="a1869-807">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-807">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a1869-808">685.14</span></span></td>
<td><span data-ttu-id="a1869-809">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-810">CC004</span></span></td>
<td><span data-ttu-id="a1869-811">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-811">Packaging</span></span></td>
<td><span data-ttu-id="a1869-812">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-812">10001</span></span></td>
<td><span data-ttu-id="a1869-813">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-813">Electricity</span></span></td>
<td><span data-ttu-id="a1869-814">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-814">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a1869-815">124.57</span></span></td>
<td><span data-ttu-id="a1869-816">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-817">CC002</span></span></td>
<td><span data-ttu-id="a1869-818">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-818">Finance</span></span></td>
<td><span data-ttu-id="a1869-819">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-819">10001</span></span></td>
<td><span data-ttu-id="a1869-820">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-820">Electricity</span></span></td>
<td><span data-ttu-id="a1869-821">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="a1869-822">-675.00</span></span></td>
<td><span data-ttu-id="a1869-823">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-824">CC003</span></span></td>
<td><span data-ttu-id="a1869-825">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-825">Assembly</span></span></td>
<td><span data-ttu-id="a1869-826">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-826">10001</span></span></td>
<td><span data-ttu-id="a1869-827">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-827">Electricity</span></span></td>
<td><span data-ttu-id="a1869-828">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a1869-829">438.75</span></span></td>
<td><span data-ttu-id="a1869-830">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-831">CC004</span></span></td>
<td><span data-ttu-id="a1869-832">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-832">Packaging</span></span></td>
<td><span data-ttu-id="a1869-833">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-833">10001</span></span></td>
<td><span data-ttu-id="a1869-834">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-834">Electricity</span></span></td>
<td><span data-ttu-id="a1869-835">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a1869-836">236.25</span></span></td>
<td><span data-ttu-id="a1869-837">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-838">CC002</span></span></td>
<td><span data-ttu-id="a1869-839">財務</span><span class="sxs-lookup"><span data-stu-id="a1869-839">Finance</span></span></td>
<td><span data-ttu-id="a1869-840">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-840">10001</span></span></td>
<td><span data-ttu-id="a1869-841">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-841">Electricity</span></span></td>
<td><span data-ttu-id="a1869-842">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-842">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a1869-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a1869-844">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-845">CC003</span></span></td>
<td><span data-ttu-id="a1869-846">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-846">Assembly</span></span></td>
<td><span data-ttu-id="a1869-847">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-847">10001</span></span></td>
<td><span data-ttu-id="a1869-848">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-848">Electricity</span></span></td>
<td><span data-ttu-id="a1869-849">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-849">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a1869-850">5,297.69</span></span></td>
<td><span data-ttu-id="a1869-851">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-852">CC004</span></span></td>
<td><span data-ttu-id="a1869-853">梱包業</span><span class="sxs-lookup"><span data-stu-id="a1869-853">Packaging</span></span></td>
<td><span data-ttu-id="a1869-854">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-854">10001</span></span></td>
<td><span data-ttu-id="a1869-855">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-855">Electricity</span></span></td>
<td><span data-ttu-id="a1869-856">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-856">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a1869-857">2,852.60</span></span></td>
<td><span data-ttu-id="a1869-858">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-859">CC003</span></span></td>
<td><span data-ttu-id="a1869-860">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-860">Assembly</span></span></td>
<td><span data-ttu-id="a1869-861">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-861">10001</span></span></td>
<td><span data-ttu-id="a1869-862">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-862">Electricity</span></span></td>
<td><span data-ttu-id="a1869-863">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="a1869-864">-713.75</span></span></td>
<td><span data-ttu-id="a1869-865">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-866">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-866">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-867">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-867">Product 1</span></span></td>
<td><span data-ttu-id="a1869-868">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-868">10001</span></span></td>
<td><span data-ttu-id="a1869-869">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-869">Electricity</span></span></td>
<td><span data-ttu-id="a1869-870">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a1869-871">535.31</span></span></td>
<td><span data-ttu-id="a1869-872">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-873">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-873">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-874">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-874">Product 2</span></span></td>
<td><span data-ttu-id="a1869-875">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-875">10001</span></span></td>
<td><span data-ttu-id="a1869-876">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-876">Electricity</span></span></td>
<td><span data-ttu-id="a1869-877">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a1869-878">178.44</span></span></td>
<td><span data-ttu-id="a1869-879">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-880">CC003</span></span></td>
<td><span data-ttu-id="a1869-881">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-881">Assembly</span></span></td>
<td><span data-ttu-id="a1869-882">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-882">10001</span></span></td>
<td><span data-ttu-id="a1869-883">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-883">Electricity</span></span></td>
<td><span data-ttu-id="a1869-884">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-884">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a1869-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a1869-886">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-887">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-887">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-888">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-888">Product 1</span></span></td>
<td><span data-ttu-id="a1869-889">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-889">10001</span></span></td>
<td><span data-ttu-id="a1869-890">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-890">Electricity</span></span></td>
<td><span data-ttu-id="a1869-891">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-891">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a1869-892">4,487.12</span></span></td>
<td><span data-ttu-id="a1869-893">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-894">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-894">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-895">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-895">Product 2</span></span></td>
<td><span data-ttu-id="a1869-896">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-896">10001</span></span></td>
<td><span data-ttu-id="a1869-897">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-897">Electricity</span></span></td>
<td><span data-ttu-id="a1869-898">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-898">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a1869-899">1,495.71</span></span></td>
<td><span data-ttu-id="a1869-900">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-901">CC003</span></span></td>
<td><span data-ttu-id="a1869-902">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-902">Assembly</span></span></td>
<td><span data-ttu-id="a1869-903">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-903">10001</span></span></td>
<td><span data-ttu-id="a1869-904">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-904">Electricity</span></span></td>
<td><span data-ttu-id="a1869-905">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="a1869-906">-286.25</span></span></td>
<td><span data-ttu-id="a1869-907">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-908">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-908">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-909">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-909">Product 1</span></span></td>
<td><span data-ttu-id="a1869-910">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-910">10001</span></span></td>
<td><span data-ttu-id="a1869-911">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-911">Electricity</span></span></td>
<td><span data-ttu-id="a1869-912">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a1869-913">241.05</span></span></td>
<td><span data-ttu-id="a1869-914">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-915">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-915">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-916">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-916">Product 2</span></span></td>
<td><span data-ttu-id="a1869-917">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-917">10001</span></span></td>
<td><span data-ttu-id="a1869-918">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-918">Electricity</span></span></td>
<td><span data-ttu-id="a1869-919">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a1869-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a1869-920">45.20</span></span></td>
<td><span data-ttu-id="a1869-921">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-922">CC003</span></span></td>
<td><span data-ttu-id="a1869-923">組み立て</span><span class="sxs-lookup"><span data-stu-id="a1869-923">Assembly</span></span></td>
<td><span data-ttu-id="a1869-924">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-924">10001</span></span></td>
<td><span data-ttu-id="a1869-925">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-925">Electricity</span></span></td>
<td><span data-ttu-id="a1869-926">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-926">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a1869-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a1869-928">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-929">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-929">Prod 1</span></span></td>
<td><span data-ttu-id="a1869-930">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-930">Product 1</span></span></td>
<td><span data-ttu-id="a1869-931">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-931">10001</span></span></td>
<td><span data-ttu-id="a1869-932">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-932">Electricity</span></span></td>
<td><span data-ttu-id="a1869-933">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-933">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a1869-934">2,507.09</span></span></td>
<td><span data-ttu-id="a1869-935">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1869-936">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-936">Prod 2</span></span></td>
<td><span data-ttu-id="a1869-937">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-937">Product 2</span></span></td>
<td><span data-ttu-id="a1869-938">10001</span><span class="sxs-lookup"><span data-stu-id="a1869-938">10001</span></span></td>
<td><span data-ttu-id="a1869-939">電気</span><span class="sxs-lookup"><span data-stu-id="a1869-939">Electricity</span></span></td>
<td><span data-ttu-id="a1869-940">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-940">Variable cost</span></span></td>
<td><span data-ttu-id="a1869-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a1869-941">470.08</span></span></td>
<td><span data-ttu-id="a1869-942">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="a1869-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a1869-943">まとめ</span><span class="sxs-lookup"><span data-stu-id="a1869-943">Conclusion</span></span>
<span data-ttu-id="a1869-944">財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a1869-945">したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。</span><span class="sxs-lookup"><span data-stu-id="a1869-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a1869-946">コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。</span><span class="sxs-lookup"><span data-stu-id="a1869-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a1869-947">各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a1869-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a1869-948">原価要素</span><span class="sxs-lookup"><span data-stu-id="a1869-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a1869-949">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a1869-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a1869-950">小計</span><span class="sxs-lookup"><span data-stu-id="a1869-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a1869-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a1869-951">CC099</span></span></th>
<th><span data-ttu-id="a1869-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a1869-952">CC001</span></span></th>
<th><span data-ttu-id="a1869-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a1869-953">CC002</span></span></th>
<th><span data-ttu-id="a1869-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a1869-954">CC003</span></span></th>
<th><span data-ttu-id="a1869-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a1869-955">CC004</span></span></th>
<th><span data-ttu-id="a1869-956">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="a1869-956">Proj 1</span></span></th>
<th><span data-ttu-id="a1869-957">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="a1869-957">Proj 2</span></span></th>
<th><span data-ttu-id="a1869-958">製品 1</span><span class="sxs-lookup"><span data-stu-id="a1869-958">Prod 1</span></span></th>
<th><span data-ttu-id="a1869-959">製品 2</span><span class="sxs-lookup"><span data-stu-id="a1869-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a1869-960">10001 電気</span><span class="sxs-lookup"><span data-stu-id="a1869-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a1869-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a1869-970">未分類</span><span class="sxs-lookup"><span data-stu-id="a1869-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-971">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a1869-972">固定費</span><span class="sxs-lookup"><span data-stu-id="a1869-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-973">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-974">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-975">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-976">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-977">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a1869-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a1869-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a1869-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a1869-981">変動費</span><span class="sxs-lookup"><span data-stu-id="a1869-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-982">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-983">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-984">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-985">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-986">0.00</span><span class="sxs-lookup"><span data-stu-id="a1869-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-987">30.00</span><span class="sxs-lookup"><span data-stu-id="a1869-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-988">10.00</span><span class="sxs-lookup"><span data-stu-id="a1869-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a1869-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a1869-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a1869-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a1869-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a1869-992">このトピックでは、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。</span><span class="sxs-lookup"><span data-stu-id="a1869-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a1869-993">したがって、この間接費は組織の最下位レベルに配賦されます。</span><span class="sxs-lookup"><span data-stu-id="a1869-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a1869-994">つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。</span><span class="sxs-lookup"><span data-stu-id="a1869-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a1869-995">コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="a1869-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a1869-996">詳細については、「[原価ロールアップ](cost-rollup.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1869-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



