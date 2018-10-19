---
title: "間接費の計算"
description: "このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="4952c-103">間接費の計算</span><span class="sxs-lookup"><span data-stu-id="4952c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4952c-104">このトピックでは、間接費を計算し配賦するための標準的なプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4952c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4952c-105">用語の定義</span><span class="sxs-lookup"><span data-stu-id="4952c-105">Term definition</span></span>
---------------

<span data-ttu-id="4952c-106">間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。</span><span class="sxs-lookup"><span data-stu-id="4952c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4952c-107">間接費は、営利活動を生み出すのに不可欠な支援を提供します。</span><span class="sxs-lookup"><span data-stu-id="4952c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4952c-108">間接費の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4952c-109">賃料</span><span class="sxs-lookup"><span data-stu-id="4952c-109">Rent</span></span>
-   <span data-ttu-id="4952c-110">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-110">Electricity</span></span>
-   <span data-ttu-id="4952c-111">管理給与</span><span class="sxs-lookup"><span data-stu-id="4952c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4952c-112">間接費計算の概要</span><span class="sxs-lookup"><span data-stu-id="4952c-112">Overhead calculation overview</span></span>
<span data-ttu-id="4952c-113">間接費計算は、コスト会計ポリシーを正しい順序で実行します。</span><span class="sxs-lookup"><span data-stu-id="4952c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4952c-114">コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4952c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4952c-115">間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4952c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4952c-116">間接費計算が生成するコスト エントリは転記日を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4952c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4952c-117">この転記日は、計算に使用される会計年度期間の終了日と一致します。</span><span class="sxs-lookup"><span data-stu-id="4952c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4952c-118">固有のバージョン ID は、次の要素で構成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4952c-119">バージョン タイプ</span><span class="sxs-lookup"><span data-stu-id="4952c-119">Version type</span></span>
-   <span data-ttu-id="4952c-120">日時</span><span class="sxs-lookup"><span data-stu-id="4952c-120">Date and time</span></span>
-   <span data-ttu-id="4952c-121">原価会計元帳</span><span class="sxs-lookup"><span data-stu-id="4952c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4952c-122">年度</span><span class="sxs-lookup"><span data-stu-id="4952c-122">Fiscal year</span></span>
-   <span data-ttu-id="4952c-123">会計年度期間</span><span class="sxs-lookup"><span data-stu-id="4952c-123">Fiscal period</span></span>

<span data-ttu-id="4952c-124">間接費計算は、バージョンとは無関係に実行されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4952c-125">そのため、実際のバージョンの前に予算バージョンを計算することができます。</span><span class="sxs-lookup"><span data-stu-id="4952c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4952c-126">間接費計算は、次の図に示されているように 4 つのステップで構成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4952c-127">各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4952c-128">この仕訳ヘッダーは、各計算ステップの入力データを保持します。</span><span class="sxs-lookup"><span data-stu-id="4952c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4952c-129">ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4952c-130">そのため、常に完全なトレーサビリティがあります。</span><span class="sxs-lookup"><span data-stu-id="4952c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4952c-131">[![間接費計算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4952c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4952c-132">電気間接費の計算および配賦</span><span class="sxs-lookup"><span data-stu-id="4952c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4952c-133">財務会計では、電気などの一部のコストは一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4952c-134">したがって、コスト会計には詳細な管理情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="4952c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4952c-135">コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4952c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4952c-136">このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4952c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4952c-137">一般会計では、電気コストは以下の表に示されているように転記できます。</span><span class="sxs-lookup"><span data-stu-id="4952c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-138">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-139">原価部門</span><span class="sxs-lookup"><span data-stu-id="4952c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-140">主勘定</span><span class="sxs-lookup"><span data-stu-id="4952c-140">Main account</span></span></th>
<th><span data-ttu-id="4952c-141">会計通貨での金額</span><span class="sxs-lookup"><span data-stu-id="4952c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-142">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4952c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4952c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-143">CC099</span></span></td>
<td><span data-ttu-id="4952c-144">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-144">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-145">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-145">10001</span></span></td>
<td><span data-ttu-id="4952c-146">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-146">Electricity</span></span></td>
<td><span data-ttu-id="4952c-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4952c-148">手順 1: コスト動作計算を処理する</span><span class="sxs-lookup"><span data-stu-id="4952c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4952c-149">既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4952c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4952c-150">コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。</span><span class="sxs-lookup"><span data-stu-id="4952c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4952c-151">コスト動作ルールの定義</span><span class="sxs-lookup"><span data-stu-id="4952c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4952c-152">場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。</span><span class="sxs-lookup"><span data-stu-id="4952c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4952c-153">電気代は多くの場合この定義と一致します。</span><span class="sxs-lookup"><span data-stu-id="4952c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4952c-154">特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。</span><span class="sxs-lookup"><span data-stu-id="4952c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4952c-155">たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4952c-156">固定金額 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4952c-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="4952c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4952c-158">1000,01 &lt; N = 変動</span><span class="sxs-lookup"><span data-stu-id="4952c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4952c-159">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-160">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-160">Journal</span></span></th>
<th><span data-ttu-id="4952c-161">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="4952c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4952c-162">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="4952c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4952c-163">バージョン</span><span class="sxs-lookup"><span data-stu-id="4952c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-164">00001</span><span class="sxs-lookup"><span data-stu-id="4952c-164">00001</span></span></td>
<td><span data-ttu-id="4952c-165">原価動作計算仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4952c-166">会計年度</span><span class="sxs-lookup"><span data-stu-id="4952c-166">Fiscal</span></span></td>
<td><span data-ttu-id="4952c-167">2017</span><span class="sxs-lookup"><span data-stu-id="4952c-167">2017</span></span></td>
<td><span data-ttu-id="4952c-168">期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-168">Period 1</span></span></td>
<td><span data-ttu-id="4952c-169">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4952c-170">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="4952c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-171">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-172">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-173">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-173">Cost element</span></span></th>
<th><span data-ttu-id="4952c-174">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-175">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-176">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4952c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4952c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-177">CC099</span></span></td>
<td><span data-ttu-id="4952c-178">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-178">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-179">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-179">10001</span></span></td>
<td><span data-ttu-id="4952c-180">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-180">Electricity</span></span></td>
<td><span data-ttu-id="4952c-181">未分類</span><span class="sxs-lookup"><span data-stu-id="4952c-181">Unclassified</span></span></td>
<td><span data-ttu-id="4952c-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4952c-183">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="4952c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-184">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-185">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-185">Cost element</span></span></th>
<th><span data-ttu-id="4952c-186">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-187">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-187">Amount</span></span></th>
<th><span data-ttu-id="4952c-188">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-189">CC099</span></span></td>
<td><span data-ttu-id="4952c-190">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-190">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-191">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-191">10001</span></span></td>
<td><span data-ttu-id="4952c-192">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-192">Electricity</span></span></td>
<td><span data-ttu-id="4952c-193">未分類</span><span class="sxs-lookup"><span data-stu-id="4952c-193">Unclassified</span></span></td>
<td><span data-ttu-id="4952c-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-194">10,000.00</span></span></td>
<td><span data-ttu-id="4952c-195">2017年 3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4952c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-196">CC099</span></span></td>
<td><span data-ttu-id="4952c-197">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-197">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-198">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-198">10001</span></span></td>
<td><span data-ttu-id="4952c-199">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-199">Electricity</span></span></td>
<td><span data-ttu-id="4952c-200">未分類</span><span class="sxs-lookup"><span data-stu-id="4952c-200">Unclassified</span></span></td>
<td><span data-ttu-id="4952c-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4952c-202">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-203">CC099</span></span></td>
<td><span data-ttu-id="4952c-204">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-204">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-205">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-205">10001</span></span></td>
<td><span data-ttu-id="4952c-206">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-206">Electricity</span></span></td>
<td><span data-ttu-id="4952c-207">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-208">1,000.00</span></span></td>
<td><span data-ttu-id="4952c-209">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-210">CC099</span></span></td>
<td><span data-ttu-id="4952c-211">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-211">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-212">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-212">10001</span></span></td>
<td><span data-ttu-id="4952c-213">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-213">Electricity</span></span></td>
<td><span data-ttu-id="4952c-214">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-214">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-215">9,000.00</span></span></td>
<td><span data-ttu-id="4952c-216">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-217">詳細については、「[原価動作ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4952c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4952c-218">手順 2: コスト配分計算を処理する</span><span class="sxs-lookup"><span data-stu-id="4952c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4952c-219">コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4952c-220">コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。</span><span class="sxs-lookup"><span data-stu-id="4952c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4952c-221">コスト配分ルールの定義</span><span class="sxs-lookup"><span data-stu-id="4952c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4952c-222">財務会計では、電気コストは多くの場合一括比例配分として登録されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4952c-223">コスト会計では、このアプローチは十分に詳細ではありません。</span><span class="sxs-lookup"><span data-stu-id="4952c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4952c-224">変動費は個々のコスト オブジェクトに公平に配分する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4952c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4952c-225">最も論理的な配賦基準は、電気 (Kwh) の消費です。</span><span class="sxs-lookup"><span data-stu-id="4952c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4952c-226">電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4952c-227">既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="4952c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-228">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-228">Cost object</span></span></th>
<th><span data-ttu-id="4952c-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4952c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-230">CC001</span></span></td>
<td><span data-ttu-id="4952c-231">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-231">HR</span></span></td>
<td><span data-ttu-id="4952c-232">1.000</span><span class="sxs-lookup"><span data-stu-id="4952c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-233">CC002</span></span></td>
<td><span data-ttu-id="4952c-234">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-234">Finance</span></span></td>
<td><span data-ttu-id="4952c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4952c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-236">CC003</span></span></td>
<td><span data-ttu-id="4952c-237">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-237">Assembly</span></span></td>
<td><span data-ttu-id="4952c-238">0</span><span class="sxs-lookup"><span data-stu-id="4952c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-239">次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-240">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-240">Cost object</span></span></th>
<th><span data-ttu-id="4952c-241">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-241">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-242">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-243">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-244">CC001</span></span></td>
<td><span data-ttu-id="4952c-245">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-245">HR</span></span></td>
<td><span data-ttu-id="4952c-246">1.000</span><span class="sxs-lookup"><span data-stu-id="4952c-246">1,000</span></span></td>
<td><span data-ttu-id="4952c-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4952c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4952c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-249">CC002</span></span></td>
<td><span data-ttu-id="4952c-250">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-250">Finance</span></span></td>
<td><span data-ttu-id="4952c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4952c-251">6,000</span></span></td>
<td><span data-ttu-id="4952c-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4952c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4952c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-254">CC003</span></span></td>
<td><span data-ttu-id="4952c-255">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-255">Assembly</span></span></td>
<td><span data-ttu-id="4952c-256">0</span><span class="sxs-lookup"><span data-stu-id="4952c-256">0</span></span></td>
<td><span data-ttu-id="4952c-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4952c-258">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-259">固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4952c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4952c-260">フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-261">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-261">Cost object</span></span></th>
<th><span data-ttu-id="4952c-262">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="4952c-262">Formula</span></span></th>
<th><span data-ttu-id="4952c-263">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-263">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-264">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-265">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-266">CC001</span></span></td>
<td><span data-ttu-id="4952c-267">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-267">HR</span></span></td>
<td><span data-ttu-id="4952c-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4952c-269">1</span><span class="sxs-lookup"><span data-stu-id="4952c-269">1</span></span></td>
<td><span data-ttu-id="4952c-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4952c-271">500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-272">CC002</span></span></td>
<td><span data-ttu-id="4952c-273">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-273">Finance</span></span></td>
<td><span data-ttu-id="4952c-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4952c-275">1</span><span class="sxs-lookup"><span data-stu-id="4952c-275">1</span></span></td>
<td><span data-ttu-id="4952c-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4952c-277">500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-278">CC003</span></span></td>
<td><span data-ttu-id="4952c-279">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-279">Assembly</span></span></td>
<td><span data-ttu-id="4952c-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4952c-281">0</span><span class="sxs-lookup"><span data-stu-id="4952c-281">0</span></span></td>
<td><span data-ttu-id="4952c-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4952c-283">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4952c-284">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-285">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-285">Journal</span></span></th>
<th><span data-ttu-id="4952c-286">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="4952c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4952c-287">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="4952c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4952c-288">バージョン</span><span class="sxs-lookup"><span data-stu-id="4952c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-289">00002</span><span class="sxs-lookup"><span data-stu-id="4952c-289">00002</span></span></td>
<td><span data-ttu-id="4952c-290">コスト配分計算仕訳</span><span class="sxs-lookup"><span data-stu-id="4952c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4952c-291">会計年度</span><span class="sxs-lookup"><span data-stu-id="4952c-291">Fiscal</span></span></td>
<td><span data-ttu-id="4952c-292">2017</span><span class="sxs-lookup"><span data-stu-id="4952c-292">2017</span></span></td>
<td><span data-ttu-id="4952c-293">期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-293">Period 1</span></span></td>
<td><span data-ttu-id="4952c-294">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4952c-295">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="4952c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-296">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-297">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-298">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-298">Cost element</span></span></th>
<th><span data-ttu-id="4952c-299">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-300">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-301">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-302">CC099</span></span></td>
<td><span data-ttu-id="4952c-303">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-303">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-304">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-304">10001</span></span></td>
<td><span data-ttu-id="4952c-305">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-305">Electricity</span></span></td>
<td><span data-ttu-id="4952c-306">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-308">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-309">CC099</span></span></td>
<td><span data-ttu-id="4952c-310">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-310">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-311">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-311">10001</span></span></td>
<td><span data-ttu-id="4952c-312">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-312">Electricity</span></span></td>
<td><span data-ttu-id="4952c-313">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-313">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4952c-315">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="4952c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-316">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-317">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-317">Cost element</span></span></th>
<th><span data-ttu-id="4952c-318">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-319">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-319">Amount</span></span></th>
<th><span data-ttu-id="4952c-320">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-321">CC099</span></span></td>
<td><span data-ttu-id="4952c-322">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-322">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-323">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-323">10001</span></span></td>
<td><span data-ttu-id="4952c-324">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-324">Electricity</span></span></td>
<td><span data-ttu-id="4952c-325">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4952c-327">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-328">CC001</span></span></td>
<td><span data-ttu-id="4952c-329">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-329">HR</span></span></td>
<td><span data-ttu-id="4952c-330">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-330">10001</span></span></td>
<td><span data-ttu-id="4952c-331">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-331">Electricity</span></span></td>
<td><span data-ttu-id="4952c-332">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-333">500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-333">500.00</span></span></td>
<td><span data-ttu-id="4952c-334">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-335">CC002</span></span></td>
<td><span data-ttu-id="4952c-336">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-336">Finance</span></span></td>
<td><span data-ttu-id="4952c-337">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-337">10001</span></span></td>
<td><span data-ttu-id="4952c-338">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-338">Electricity</span></span></td>
<td><span data-ttu-id="4952c-339">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-340">500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-340">500.00</span></span></td>
<td><span data-ttu-id="4952c-341">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-342">CC099</span></span></td>
<td><span data-ttu-id="4952c-343">既定のコスト センター</span><span class="sxs-lookup"><span data-stu-id="4952c-343">Default cost center</span></span></td>
<td><span data-ttu-id="4952c-344">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-344">10001</span></span></td>
<td><span data-ttu-id="4952c-345">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-345">Electricity</span></span></td>
<td><span data-ttu-id="4952c-346">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-346">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="4952c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4952c-348">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-349">CC001</span></span></td>
<td><span data-ttu-id="4952c-350">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-350">HR</span></span></td>
<td><span data-ttu-id="4952c-351">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-351">10001</span></span></td>
<td><span data-ttu-id="4952c-352">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-352">Electricity</span></span></td>
<td><span data-ttu-id="4952c-353">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-353">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4952c-354">1,285.71</span></span></td>
<td><span data-ttu-id="4952c-355">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-356">CC002</span></span></td>
<td><span data-ttu-id="4952c-357">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-357">Finance</span></span></td>
<td><span data-ttu-id="4952c-358">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-358">10001</span></span></td>
<td><span data-ttu-id="4952c-359">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-359">Electricity</span></span></td>
<td><span data-ttu-id="4952c-360">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-360">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4952c-361">7,714.29</span></span></td>
<td><span data-ttu-id="4952c-362">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-363">詳細については、「[原価配分ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4952c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4952c-364">手順 3: 間接費率の計算を処理する</span><span class="sxs-lookup"><span data-stu-id="4952c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4952c-365">間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4952c-366">請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。</span><span class="sxs-lookup"><span data-stu-id="4952c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4952c-367">間接費率の定義</span><span class="sxs-lookup"><span data-stu-id="4952c-367">Define the overhead rate</span></span>

<span data-ttu-id="4952c-368">コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4952c-369">HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-370">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-370">Cost object</span></span></th>
<th><span data-ttu-id="4952c-371">時間</span><span class="sxs-lookup"><span data-stu-id="4952c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-372">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-372">Proj 1</span></span></td>
<td><span data-ttu-id="4952c-373">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-373">Project 1</span></span></td>
<td><span data-ttu-id="4952c-374">3</span><span class="sxs-lookup"><span data-stu-id="4952c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-375">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-375">Proj 2</span></span></td>
<td><span data-ttu-id="4952c-376">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-376">Project 2</span></span></td>
<td><span data-ttu-id="4952c-377">1</span><span class="sxs-lookup"><span data-stu-id="4952c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-378">コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。</span><span class="sxs-lookup"><span data-stu-id="4952c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-379">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-379">Cost object</span></span></th>
<th><span data-ttu-id="4952c-380">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-380">Cost element</span></span></th>
<th><span data-ttu-id="4952c-381">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-382">単位</span><span class="sxs-lookup"><span data-stu-id="4952c-382">Units</span></span></th>
<th><span data-ttu-id="4952c-383">率</span><span class="sxs-lookup"><span data-stu-id="4952c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-384">CC001</span></span></td>
<td><span data-ttu-id="4952c-385">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-385">HR</span></span></td>
<td><span data-ttu-id="4952c-386">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-386">10001</span></span></td>
<td><span data-ttu-id="4952c-387">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-387">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-388">1</span><span class="sxs-lookup"><span data-stu-id="4952c-388">1</span></span></td>
<td><span data-ttu-id="4952c-389">10</span><span class="sxs-lookup"><span data-stu-id="4952c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-390">次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-391">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-391">Cost object</span></span></th>
<th><span data-ttu-id="4952c-392">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-392">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-393">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-393">Cost element</span></span></th>
<th><span data-ttu-id="4952c-394">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-395">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-396">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-396">Proj 1</span></span></td>
<td><span data-ttu-id="4952c-397">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-397">Project 1</span></span></td>
<td><span data-ttu-id="4952c-398">3</span><span class="sxs-lookup"><span data-stu-id="4952c-398">3</span></span></td>
<td><span data-ttu-id="4952c-399">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-399">10001</span></span></td>
<td><span data-ttu-id="4952c-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4952c-401">30.00</span><span class="sxs-lookup"><span data-stu-id="4952c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-402">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-402">Proj 2</span></span></td>
<td><span data-ttu-id="4952c-403">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-403">Project 2</span></span></td>
<td><span data-ttu-id="4952c-404">1</span><span class="sxs-lookup"><span data-stu-id="4952c-404">1</span></span></td>
<td><span data-ttu-id="4952c-405">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-405">10001</span></span></td>
<td><span data-ttu-id="4952c-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4952c-407">10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4952c-408">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-409">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-409">Journal</span></span></th>
<th><span data-ttu-id="4952c-410">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="4952c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4952c-411">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="4952c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4952c-412">バージョン</span><span class="sxs-lookup"><span data-stu-id="4952c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-413">00003</span><span class="sxs-lookup"><span data-stu-id="4952c-413">00003</span></span></td>
<td><span data-ttu-id="4952c-414">間接比率計算仕訳</span><span class="sxs-lookup"><span data-stu-id="4952c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4952c-415">会計年度</span><span class="sxs-lookup"><span data-stu-id="4952c-415">Fiscal</span></span></td>
<td><span data-ttu-id="4952c-416">2017</span><span class="sxs-lookup"><span data-stu-id="4952c-416">2017</span></span></td>
<td><span data-ttu-id="4952c-417">期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-417">Period 1</span></span></td>
<td><span data-ttu-id="4952c-418">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4952c-419">仕訳入力 (間接比率計算のための仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="4952c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-420">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-421">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-421">Cost object</span></span></th>
<th><span data-ttu-id="4952c-422">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-423">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-424">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-424">Proj 1</span></span></td>
<td><span data-ttu-id="4952c-425">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4952c-426">3.00</span><span class="sxs-lookup"><span data-stu-id="4952c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-427">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-428">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-428">Proj 2</span></span></td>
<td><span data-ttu-id="4952c-429">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4952c-430">1.00</span><span class="sxs-lookup"><span data-stu-id="4952c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4952c-431">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="4952c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-432">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-433">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-433">Cost element</span></span></th>
<th><span data-ttu-id="4952c-434">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-435">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-435">Amount</span></span></th>
<th><span data-ttu-id="4952c-436">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4952c-437">CC0001</span></span></td>
<td><span data-ttu-id="4952c-438">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-438">HR</span></span></td>
<td><span data-ttu-id="4952c-439">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-439">10001</span></span></td>
<td><span data-ttu-id="4952c-440">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-440">Electricity</span></span></td>
<td><span data-ttu-id="4952c-441">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-441">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="4952c-442">-30.00</span></span></td>
<td><span data-ttu-id="4952c-443">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-444">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-444">Proj 1</span></span></td>
<td><span data-ttu-id="4952c-445">内部プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4952c-446">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-446">10001</span></span></td>
<td><span data-ttu-id="4952c-447">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-447">Electricity</span></span></td>
<td><span data-ttu-id="4952c-448">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-448">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-449">30.00</span><span class="sxs-lookup"><span data-stu-id="4952c-449">30.00</span></span></td>
<td><span data-ttu-id="4952c-450">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-451">CC001</span></span></td>
<td><span data-ttu-id="4952c-452">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-452">HR</span></span></td>
<td><span data-ttu-id="4952c-453">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-453">10001</span></span></td>
<td><span data-ttu-id="4952c-454">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-454">Electricity</span></span></td>
<td><span data-ttu-id="4952c-455">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-455">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-456">-10.00</span></span></td>
<td><span data-ttu-id="4952c-457">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-458">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-458">Proj 2</span></span></td>
<td><span data-ttu-id="4952c-459">内部プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4952c-460">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-460">10001</span></span></td>
<td><span data-ttu-id="4952c-461">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-461">Electricity</span></span></td>
<td><span data-ttu-id="4952c-462">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-462">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-463">10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-463">10.00</span></span></td>
<td><span data-ttu-id="4952c-464">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-465">詳細については、「[間接費計算を実行する](cost-rollup.md#perform-overhead-calculation)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4952c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4952c-466">手順 4: コスト配賦計算を処理する</span><span class="sxs-lookup"><span data-stu-id="4952c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4952c-467">配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4952c-468">Finance と Operations では、相互配賦手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4952c-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="4952c-469">相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4952c-470">システムは、配賦を実行する正しい順序を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="4952c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4952c-471">コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4952c-472">コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4952c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4952c-473">配賦の順序は、コスト制御ユニットによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4952c-474">[![相互手法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4952c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4952c-475">コスト配賦の定義</span><span class="sxs-lookup"><span data-stu-id="4952c-475">Define the cost allocation</span></span>

<span data-ttu-id="4952c-476">次に、コストのフローを追跡する方法を説明する簡単な例を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4952c-477">コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4952c-478">HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-479">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-479">Cost object</span></span></th>
<th><span data-ttu-id="4952c-480">HR サービス</span><span class="sxs-lookup"><span data-stu-id="4952c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-481">CC002</span></span></td>
<td><span data-ttu-id="4952c-482">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-482">Finance</span></span></td>
<td><span data-ttu-id="4952c-483">35</span><span class="sxs-lookup"><span data-stu-id="4952c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-484">CC003</span></span></td>
<td><span data-ttu-id="4952c-485">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-485">Assembly</span></span></td>
<td><span data-ttu-id="4952c-486">55</span><span class="sxs-lookup"><span data-stu-id="4952c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-487">CC004</span></span></td>
<td><span data-ttu-id="4952c-488">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-488">Packaging</span></span></td>
<td><span data-ttu-id="4952c-489">10</span><span class="sxs-lookup"><span data-stu-id="4952c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-490">コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4952c-491">財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-492">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-492">Cost object</span></span></th>
<th><span data-ttu-id="4952c-493">財務サービス</span><span class="sxs-lookup"><span data-stu-id="4952c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-494">CC003</span></span></td>
<td><span data-ttu-id="4952c-495">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-495">Assembly</span></span></td>
<td><span data-ttu-id="4952c-496">65</span><span class="sxs-lookup"><span data-stu-id="4952c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-497">CC004</span></span></td>
<td><span data-ttu-id="4952c-498">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-498">Packaging</span></span></td>
<td><span data-ttu-id="4952c-499">35</span><span class="sxs-lookup"><span data-stu-id="4952c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-500">コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4952c-501">組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-502">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-502">Cost object</span></span></th>
<th><span data-ttu-id="4952c-503">組み立てサービス (時間)</span><span class="sxs-lookup"><span data-stu-id="4952c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-504">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-504">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-505">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-505">Product 1</span></span></td>
<td><span data-ttu-id="4952c-506">60</span><span class="sxs-lookup"><span data-stu-id="4952c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-507">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-507">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-508">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-508">Product 2</span></span></td>
<td><span data-ttu-id="4952c-509">20</span><span class="sxs-lookup"><span data-stu-id="4952c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-510">コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。</span><span class="sxs-lookup"><span data-stu-id="4952c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4952c-511">梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-512">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-512">Cost object</span></span></th>
<th><span data-ttu-id="4952c-513">梱包業サービス (時間)</span><span class="sxs-lookup"><span data-stu-id="4952c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-514">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-514">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-515">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-515">Product 1</span></span></td>
<td><span data-ttu-id="4952c-516">80</span><span class="sxs-lookup"><span data-stu-id="4952c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-517">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-517">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-518">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-518">Product 2</span></span></td>
<td><span data-ttu-id="4952c-519">15</span><span class="sxs-lookup"><span data-stu-id="4952c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4952c-520">Finance and Operations では、製品に消費される生産時間などの統計測定は、ソース データから抽出できます。</span><span class="sxs-lookup"><span data-stu-id="4952c-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4952c-521">詳細については、「[統計測定プロバイダー テンプレート](statistical-measure-provider-template.md#statistical-measure-provider-template)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4952c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4952c-522">次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-523">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-523">Cost object</span></span></th>
<th><span data-ttu-id="4952c-524">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-524">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-525">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-526">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-526">Amount</span></span></th>
<th><span data-ttu-id="4952c-527">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-528">CC002</span></span></td>
<td><span data-ttu-id="4952c-529">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-529">Finance</span></span></td>
<td><span data-ttu-id="4952c-530">35</span><span class="sxs-lookup"><span data-stu-id="4952c-530">35</span></span></td>
<td><span data-ttu-id="4952c-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4952c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4952c-532">175.00</span></span></td>
<td><span data-ttu-id="4952c-533">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-534">CC003</span></span></td>
<td><span data-ttu-id="4952c-535">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-535">Assembly</span></span></td>
<td><span data-ttu-id="4952c-536">55</span><span class="sxs-lookup"><span data-stu-id="4952c-536">55</span></span></td>
<td><span data-ttu-id="4952c-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4952c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4952c-538">275.00</span></span></td>
<td><span data-ttu-id="4952c-539">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-540">CC004</span></span></td>
<td><span data-ttu-id="4952c-541">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-541">Packaging</span></span></td>
<td><span data-ttu-id="4952c-542">10</span><span class="sxs-lookup"><span data-stu-id="4952c-542">10</span></span></td>
<td><span data-ttu-id="4952c-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4952c-544">50.00</span><span class="sxs-lookup"><span data-stu-id="4952c-544">50.00</span></span></td>
<td><span data-ttu-id="4952c-545">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-546">CC002</span></span></td>
<td><span data-ttu-id="4952c-547">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-547">Finance</span></span></td>
<td><span data-ttu-id="4952c-548">35</span><span class="sxs-lookup"><span data-stu-id="4952c-548">35</span></span></td>
<td><span data-ttu-id="4952c-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4952c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4952c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4952c-550">436.00</span></span></td>
<td><span data-ttu-id="4952c-551">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-552">CC003</span></span></td>
<td><span data-ttu-id="4952c-553">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-553">Assembly</span></span></td>
<td><span data-ttu-id="4952c-554">55</span><span class="sxs-lookup"><span data-stu-id="4952c-554">55</span></span></td>
<td><span data-ttu-id="4952c-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4952c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4952c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4952c-556">685.14</span></span></td>
<td><span data-ttu-id="4952c-557">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-558">CC004</span></span></td>
<td><span data-ttu-id="4952c-559">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-559">Packaging</span></span></td>
<td><span data-ttu-id="4952c-560">10</span><span class="sxs-lookup"><span data-stu-id="4952c-560">10</span></span></td>
<td><span data-ttu-id="4952c-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4952c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4952c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4952c-562">124.57</span></span></td>
<td><span data-ttu-id="4952c-563">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-564">次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-565">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-565">Cost object</span></span></th>
<th><span data-ttu-id="4952c-566">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-566">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-567">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-568">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-568">Amount</span></span></th>
<th><span data-ttu-id="4952c-569">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-570">CC003</span></span></td>
<td><span data-ttu-id="4952c-571">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-571">Assembly</span></span></td>
<td><span data-ttu-id="4952c-572">65</span><span class="sxs-lookup"><span data-stu-id="4952c-572">65</span></span></td>
<td><span data-ttu-id="4952c-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4952c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4952c-574">438.75</span></span></td>
<td><span data-ttu-id="4952c-575">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-576">CC004</span></span></td>
<td><span data-ttu-id="4952c-577">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-577">Packaging</span></span></td>
<td><span data-ttu-id="4952c-578">35</span><span class="sxs-lookup"><span data-stu-id="4952c-578">35</span></span></td>
<td><span data-ttu-id="4952c-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4952c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4952c-580">236.25</span></span></td>
<td><span data-ttu-id="4952c-581">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-582">CC003</span></span></td>
<td><span data-ttu-id="4952c-583">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-583">Assembly</span></span></td>
<td><span data-ttu-id="4952c-584">65</span><span class="sxs-lookup"><span data-stu-id="4952c-584">65</span></span></td>
<td><span data-ttu-id="4952c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4952c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4952c-586">5,297.69</span></span></td>
<td><span data-ttu-id="4952c-587">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-588">CC004</span></span></td>
<td><span data-ttu-id="4952c-589">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-589">Packaging</span></span></td>
<td><span data-ttu-id="4952c-590">35</span><span class="sxs-lookup"><span data-stu-id="4952c-590">35</span></span></td>
<td><span data-ttu-id="4952c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="4952c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4952c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4952c-592">2,852.60</span></span></td>
<td><span data-ttu-id="4952c-593">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-594">次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-595">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-595">Cost object</span></span></th>
<th><span data-ttu-id="4952c-596">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-596">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-597">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-598">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-598">Amount</span></span></th>
<th><span data-ttu-id="4952c-599">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-600">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-600">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-601">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-601">Product 1</span></span></td>
<td><span data-ttu-id="4952c-602">60</span><span class="sxs-lookup"><span data-stu-id="4952c-602">60</span></span></td>
<td><span data-ttu-id="4952c-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="4952c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4952c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4952c-604">535.31</span></span></td>
<td><span data-ttu-id="4952c-605">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-606">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-606">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-607">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-607">Product 2</span></span></td>
<td><span data-ttu-id="4952c-608">20</span><span class="sxs-lookup"><span data-stu-id="4952c-608">20</span></span></td>
<td><span data-ttu-id="4952c-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="4952c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4952c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4952c-610">178.44</span></span></td>
<td><span data-ttu-id="4952c-611">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-612">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-612">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-613">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-613">Product 1</span></span></td>
<td><span data-ttu-id="4952c-614">60</span><span class="sxs-lookup"><span data-stu-id="4952c-614">60</span></span></td>
<td><span data-ttu-id="4952c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="4952c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4952c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4952c-616">4,487.12</span></span></td>
<td><span data-ttu-id="4952c-617">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-618">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-618">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-619">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-619">Product 2</span></span></td>
<td><span data-ttu-id="4952c-620">20</span><span class="sxs-lookup"><span data-stu-id="4952c-620">20</span></span></td>
<td><span data-ttu-id="4952c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="4952c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4952c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4952c-622">1,495.71</span></span></td>
<td><span data-ttu-id="4952c-623">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4952c-624">次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-625">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-625">Cost object</span></span></th>
<th><span data-ttu-id="4952c-626">大きさ</span><span class="sxs-lookup"><span data-stu-id="4952c-626">Magnitude</span></span></th>
<th><span data-ttu-id="4952c-627">配賦係数</span><span class="sxs-lookup"><span data-stu-id="4952c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4952c-628">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-628">Amount</span></span></th>
<th><span data-ttu-id="4952c-629">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-630">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-630">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-631">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-631">Product 1</span></span></td>
<td><span data-ttu-id="4952c-632">80</span><span class="sxs-lookup"><span data-stu-id="4952c-632">80</span></span></td>
<td><span data-ttu-id="4952c-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="4952c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4952c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4952c-634">241.05</span></span></td>
<td><span data-ttu-id="4952c-635">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-636">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-636">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-637">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-637">Product 2</span></span></td>
<td><span data-ttu-id="4952c-638">15</span><span class="sxs-lookup"><span data-stu-id="4952c-638">15</span></span></td>
<td><span data-ttu-id="4952c-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="4952c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4952c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4952c-640">45.20</span></span></td>
<td><span data-ttu-id="4952c-641">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-642">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-642">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-643">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-643">Product 1</span></span></td>
<td><span data-ttu-id="4952c-644">80</span><span class="sxs-lookup"><span data-stu-id="4952c-644">80</span></span></td>
<td><span data-ttu-id="4952c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="4952c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4952c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4952c-646">2,507.09</span></span></td>
<td><span data-ttu-id="4952c-647">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-648">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-648">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-649">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-649">Product 2</span></span></td>
<td><span data-ttu-id="4952c-650">15</span><span class="sxs-lookup"><span data-stu-id="4952c-650">15</span></span></td>
<td><span data-ttu-id="4952c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="4952c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4952c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4952c-652">470.08</span></span></td>
<td><span data-ttu-id="4952c-653">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4952c-654">仕訳入力 (コスト オブジェクト残高仕訳入力)</span><span class="sxs-lookup"><span data-stu-id="4952c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-655">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-655">Journal</span></span></th>
<th><span data-ttu-id="4952c-656">仕訳帳タイプ</span><span class="sxs-lookup"><span data-stu-id="4952c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4952c-657">会計カレンダー期間</span><span class="sxs-lookup"><span data-stu-id="4952c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4952c-658">バージョン</span><span class="sxs-lookup"><span data-stu-id="4952c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-659">00004</span><span class="sxs-lookup"><span data-stu-id="4952c-659">00004</span></span></td>
<td><span data-ttu-id="4952c-660">原価配賦仕訳帳</span><span class="sxs-lookup"><span data-stu-id="4952c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4952c-661">会計年度</span><span class="sxs-lookup"><span data-stu-id="4952c-661">Fiscal</span></span></td>
<td><span data-ttu-id="4952c-662">2017</span><span class="sxs-lookup"><span data-stu-id="4952c-662">2017</span></span></td>
<td><span data-ttu-id="4952c-663">期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-663">Period 1</span></span></td>
<td><span data-ttu-id="4952c-664">間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</span><span class="sxs-lookup"><span data-stu-id="4952c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4952c-665">仕訳帳明細行</span><span class="sxs-lookup"><span data-stu-id="4952c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4952c-666">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-667">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-668">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-668">Cost element</span></span></th>
<th><span data-ttu-id="4952c-669">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-670">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-671">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-672">CC001</span></span></td>
<td><span data-ttu-id="4952c-673">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-673">HR</span></span></td>
<td><span data-ttu-id="4952c-674">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-674">10001</span></span></td>
<td><span data-ttu-id="4952c-675">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-675">Electricity</span></span></td>
<td><span data-ttu-id="4952c-676">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-677">500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-678">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-679">CC001</span></span></td>
<td><span data-ttu-id="4952c-680">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-680">HR</span></span></td>
<td><span data-ttu-id="4952c-681">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-681">10001</span></span></td>
<td><span data-ttu-id="4952c-682">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-682">Electricity</span></span></td>
<td><span data-ttu-id="4952c-683">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-683">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4952c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-685">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-686">CC002</span></span></td>
<td><span data-ttu-id="4952c-687">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-687">Finance</span></span></td>
<td><span data-ttu-id="4952c-688">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-688">10001</span></span></td>
<td><span data-ttu-id="4952c-689">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-689">Electricity</span></span></td>
<td><span data-ttu-id="4952c-690">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4952c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-692">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-693">CC002</span></span></td>
<td><span data-ttu-id="4952c-694">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-694">Finance</span></span></td>
<td><span data-ttu-id="4952c-695">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-695">10001</span></span></td>
<td><span data-ttu-id="4952c-696">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-696">Electricity</span></span></td>
<td><span data-ttu-id="4952c-697">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-697">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4952c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-699">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-700">CC003</span></span></td>
<td><span data-ttu-id="4952c-701">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-701">Assembly</span></span></td>
<td><span data-ttu-id="4952c-702">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-702">10001</span></span></td>
<td><span data-ttu-id="4952c-703">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-703">Electricity</span></span></td>
<td><span data-ttu-id="4952c-704">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4952c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-706">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-707">CC003</span></span></td>
<td><span data-ttu-id="4952c-708">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-708">Assembly</span></span></td>
<td><span data-ttu-id="4952c-709">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-709">10001</span></span></td>
<td><span data-ttu-id="4952c-710">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-710">Electricity</span></span></td>
<td><span data-ttu-id="4952c-711">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-711">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4952c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-713">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-714">CC003</span></span></td>
<td><span data-ttu-id="4952c-715">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-715">Packaging</span></span></td>
<td><span data-ttu-id="4952c-716">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-716">10001</span></span></td>
<td><span data-ttu-id="4952c-717">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-717">Electricity</span></span></td>
<td><span data-ttu-id="4952c-718">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4952c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-720">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-721">CC003</span></span></td>
<td><span data-ttu-id="4952c-722">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-722">Packaging</span></span></td>
<td><span data-ttu-id="4952c-723">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-723">10001</span></span></td>
<td><span data-ttu-id="4952c-724">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-724">Electricity</span></span></td>
<td><span data-ttu-id="4952c-725">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-725">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4952c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-727">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-728">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-728">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-729">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-729">Product 1</span></span></td>
<td><span data-ttu-id="4952c-730">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-730">10001</span></span></td>
<td><span data-ttu-id="4952c-731">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-731">Electricity</span></span></td>
<td><span data-ttu-id="4952c-732">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4952c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-734">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-735">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-735">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-736">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-736">Product 1</span></span></td>
<td><span data-ttu-id="4952c-737">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-737">10001</span></span></td>
<td><span data-ttu-id="4952c-738">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-738">Electricity</span></span></td>
<td><span data-ttu-id="4952c-739">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-739">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4952c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-741">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-742">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-742">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-743">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-743">Product 1</span></span></td>
<td><span data-ttu-id="4952c-744">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-744">10001</span></span></td>
<td><span data-ttu-id="4952c-745">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-745">Electricity</span></span></td>
<td><span data-ttu-id="4952c-746">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4952c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-748">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4952c-749">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-749">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-750">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-750">Product 1</span></span></td>
<td><span data-ttu-id="4952c-751">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-751">10001</span></span></td>
<td><span data-ttu-id="4952c-752">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-752">Electricity</span></span></td>
<td><span data-ttu-id="4952c-753">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-753">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4952c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4952c-755">原価エントリ</span><span class="sxs-lookup"><span data-stu-id="4952c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4952c-756">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4952c-757">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-757">Cost element</span></span></th>
<th><span data-ttu-id="4952c-758">原価動作</span><span class="sxs-lookup"><span data-stu-id="4952c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4952c-759">金額</span><span class="sxs-lookup"><span data-stu-id="4952c-759">Amount</span></span></th>
<th><span data-ttu-id="4952c-760">会計日</span><span class="sxs-lookup"><span data-stu-id="4952c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4952c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-761">CC001</span></span></td>
<td><span data-ttu-id="4952c-762">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-762">HR</span></span></td>
<td><span data-ttu-id="4952c-763">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-763">10001</span></span></td>
<td><span data-ttu-id="4952c-764">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-764">Electricity</span></span></td>
<td><span data-ttu-id="4952c-765">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4952c-766">-500.00</span></span></td>
<td><span data-ttu-id="4952c-767">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-768">CC002</span></span></td>
<td><span data-ttu-id="4952c-769">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-769">Finance</span></span></td>
<td><span data-ttu-id="4952c-770">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-770">10001</span></span></td>
<td><span data-ttu-id="4952c-771">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-771">Electricity</span></span></td>
<td><span data-ttu-id="4952c-772">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4952c-773">175.00</span></span></td>
<td><span data-ttu-id="4952c-774">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-775">CC003</span></span></td>
<td><span data-ttu-id="4952c-776">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-776">Assembly</span></span></td>
<td><span data-ttu-id="4952c-777">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-777">10001</span></span></td>
<td><span data-ttu-id="4952c-778">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-778">Electricity</span></span></td>
<td><span data-ttu-id="4952c-779">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4952c-780">275.00</span></span></td>
<td><span data-ttu-id="4952c-781">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-782">CC004</span></span></td>
<td><span data-ttu-id="4952c-783">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-783">Packaging</span></span></td>
<td><span data-ttu-id="4952c-784">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-784">10001</span></span></td>
<td><span data-ttu-id="4952c-785">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-785">Electricity</span></span></td>
<td><span data-ttu-id="4952c-786">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4952c-787">50,00</span></span></td>
<td><span data-ttu-id="4952c-788">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-789">CC001</span></span></td>
<td><span data-ttu-id="4952c-790">HR</span><span class="sxs-lookup"><span data-stu-id="4952c-790">HR</span></span></td>
<td><span data-ttu-id="4952c-791">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-791">10001</span></span></td>
<td><span data-ttu-id="4952c-792">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-792">Electricity</span></span></td>
<td><span data-ttu-id="4952c-793">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-793">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="4952c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4952c-795">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-796">CC002</span></span></td>
<td><span data-ttu-id="4952c-797">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-797">Finance</span></span></td>
<td><span data-ttu-id="4952c-798">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-798">10001</span></span></td>
<td><span data-ttu-id="4952c-799">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-799">Electricity</span></span></td>
<td><span data-ttu-id="4952c-800">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-800">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4952c-801">436.00</span></span></td>
<td><span data-ttu-id="4952c-802">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-803">CC003</span></span></td>
<td><span data-ttu-id="4952c-804">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-804">Assembly</span></span></td>
<td><span data-ttu-id="4952c-805">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-805">10001</span></span></td>
<td><span data-ttu-id="4952c-806">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-806">Electricity</span></span></td>
<td><span data-ttu-id="4952c-807">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-807">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4952c-808">685.14</span></span></td>
<td><span data-ttu-id="4952c-809">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-810">CC004</span></span></td>
<td><span data-ttu-id="4952c-811">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-811">Packaging</span></span></td>
<td><span data-ttu-id="4952c-812">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-812">10001</span></span></td>
<td><span data-ttu-id="4952c-813">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-813">Electricity</span></span></td>
<td><span data-ttu-id="4952c-814">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-814">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4952c-815">124.57</span></span></td>
<td><span data-ttu-id="4952c-816">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-817">CC002</span></span></td>
<td><span data-ttu-id="4952c-818">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-818">Finance</span></span></td>
<td><span data-ttu-id="4952c-819">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-819">10001</span></span></td>
<td><span data-ttu-id="4952c-820">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-820">Electricity</span></span></td>
<td><span data-ttu-id="4952c-821">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="4952c-822">-675.00</span></span></td>
<td><span data-ttu-id="4952c-823">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-824">CC003</span></span></td>
<td><span data-ttu-id="4952c-825">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-825">Assembly</span></span></td>
<td><span data-ttu-id="4952c-826">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-826">10001</span></span></td>
<td><span data-ttu-id="4952c-827">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-827">Electricity</span></span></td>
<td><span data-ttu-id="4952c-828">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4952c-829">438.75</span></span></td>
<td><span data-ttu-id="4952c-830">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-831">CC004</span></span></td>
<td><span data-ttu-id="4952c-832">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-832">Packaging</span></span></td>
<td><span data-ttu-id="4952c-833">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-833">10001</span></span></td>
<td><span data-ttu-id="4952c-834">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-834">Electricity</span></span></td>
<td><span data-ttu-id="4952c-835">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4952c-836">236.25</span></span></td>
<td><span data-ttu-id="4952c-837">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-838">CC002</span></span></td>
<td><span data-ttu-id="4952c-839">財務</span><span class="sxs-lookup"><span data-stu-id="4952c-839">Finance</span></span></td>
<td><span data-ttu-id="4952c-840">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-840">10001</span></span></td>
<td><span data-ttu-id="4952c-841">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-841">Electricity</span></span></td>
<td><span data-ttu-id="4952c-842">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-842">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="4952c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4952c-844">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-845">CC003</span></span></td>
<td><span data-ttu-id="4952c-846">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-846">Assembly</span></span></td>
<td><span data-ttu-id="4952c-847">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-847">10001</span></span></td>
<td><span data-ttu-id="4952c-848">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-848">Electricity</span></span></td>
<td><span data-ttu-id="4952c-849">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-849">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4952c-850">5,297.69</span></span></td>
<td><span data-ttu-id="4952c-851">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-852">CC004</span></span></td>
<td><span data-ttu-id="4952c-853">梱包業</span><span class="sxs-lookup"><span data-stu-id="4952c-853">Packaging</span></span></td>
<td><span data-ttu-id="4952c-854">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-854">10001</span></span></td>
<td><span data-ttu-id="4952c-855">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-855">Electricity</span></span></td>
<td><span data-ttu-id="4952c-856">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-856">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4952c-857">2,852.60</span></span></td>
<td><span data-ttu-id="4952c-858">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-859">CC003</span></span></td>
<td><span data-ttu-id="4952c-860">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-860">Assembly</span></span></td>
<td><span data-ttu-id="4952c-861">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-861">10001</span></span></td>
<td><span data-ttu-id="4952c-862">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-862">Electricity</span></span></td>
<td><span data-ttu-id="4952c-863">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4952c-864">-713.75</span></span></td>
<td><span data-ttu-id="4952c-865">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-866">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-866">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-867">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-867">Product 1</span></span></td>
<td><span data-ttu-id="4952c-868">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-868">10001</span></span></td>
<td><span data-ttu-id="4952c-869">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-869">Electricity</span></span></td>
<td><span data-ttu-id="4952c-870">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4952c-871">535.31</span></span></td>
<td><span data-ttu-id="4952c-872">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-873">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-873">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-874">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-874">Product 2</span></span></td>
<td><span data-ttu-id="4952c-875">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-875">10001</span></span></td>
<td><span data-ttu-id="4952c-876">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-876">Electricity</span></span></td>
<td><span data-ttu-id="4952c-877">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4952c-878">178.44</span></span></td>
<td><span data-ttu-id="4952c-879">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-880">CC003</span></span></td>
<td><span data-ttu-id="4952c-881">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-881">Assembly</span></span></td>
<td><span data-ttu-id="4952c-882">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-882">10001</span></span></td>
<td><span data-ttu-id="4952c-883">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-883">Electricity</span></span></td>
<td><span data-ttu-id="4952c-884">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-884">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="4952c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4952c-886">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-887">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-887">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-888">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-888">Product 1</span></span></td>
<td><span data-ttu-id="4952c-889">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-889">10001</span></span></td>
<td><span data-ttu-id="4952c-890">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-890">Electricity</span></span></td>
<td><span data-ttu-id="4952c-891">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-891">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4952c-892">4,487.12</span></span></td>
<td><span data-ttu-id="4952c-893">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-894">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-894">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-895">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-895">Product 2</span></span></td>
<td><span data-ttu-id="4952c-896">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-896">10001</span></span></td>
<td><span data-ttu-id="4952c-897">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-897">Electricity</span></span></td>
<td><span data-ttu-id="4952c-898">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-898">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4952c-899">1,495.71</span></span></td>
<td><span data-ttu-id="4952c-900">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-901">CC003</span></span></td>
<td><span data-ttu-id="4952c-902">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-902">Assembly</span></span></td>
<td><span data-ttu-id="4952c-903">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-903">10001</span></span></td>
<td><span data-ttu-id="4952c-904">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-904">Electricity</span></span></td>
<td><span data-ttu-id="4952c-905">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="4952c-906">-286.25</span></span></td>
<td><span data-ttu-id="4952c-907">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-908">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-908">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-909">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-909">Product 1</span></span></td>
<td><span data-ttu-id="4952c-910">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-910">10001</span></span></td>
<td><span data-ttu-id="4952c-911">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-911">Electricity</span></span></td>
<td><span data-ttu-id="4952c-912">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4952c-913">241.05</span></span></td>
<td><span data-ttu-id="4952c-914">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-915">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-915">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-916">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-916">Product 2</span></span></td>
<td><span data-ttu-id="4952c-917">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-917">10001</span></span></td>
<td><span data-ttu-id="4952c-918">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-918">Electricity</span></span></td>
<td><span data-ttu-id="4952c-919">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4952c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4952c-920">45.20</span></span></td>
<td><span data-ttu-id="4952c-921">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-922">CC003</span></span></td>
<td><span data-ttu-id="4952c-923">組み立て</span><span class="sxs-lookup"><span data-stu-id="4952c-923">Assembly</span></span></td>
<td><span data-ttu-id="4952c-924">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-924">10001</span></span></td>
<td><span data-ttu-id="4952c-925">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-925">Electricity</span></span></td>
<td><span data-ttu-id="4952c-926">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-926">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="4952c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4952c-928">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-929">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-929">Prod 1</span></span></td>
<td><span data-ttu-id="4952c-930">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-930">Product 1</span></span></td>
<td><span data-ttu-id="4952c-931">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-931">10001</span></span></td>
<td><span data-ttu-id="4952c-932">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-932">Electricity</span></span></td>
<td><span data-ttu-id="4952c-933">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-933">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4952c-934">2,507.09</span></span></td>
<td><span data-ttu-id="4952c-935">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4952c-936">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-936">Prod 2</span></span></td>
<td><span data-ttu-id="4952c-937">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-937">Product 2</span></span></td>
<td><span data-ttu-id="4952c-938">10001</span><span class="sxs-lookup"><span data-stu-id="4952c-938">10001</span></span></td>
<td><span data-ttu-id="4952c-939">電気</span><span class="sxs-lookup"><span data-stu-id="4952c-939">Electricity</span></span></td>
<td><span data-ttu-id="4952c-940">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-940">Variable cost</span></span></td>
<td><span data-ttu-id="4952c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4952c-941">470.08</span></span></td>
<td><span data-ttu-id="4952c-942">2017年 31 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4952c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4952c-943">まとめ</span><span class="sxs-lookup"><span data-stu-id="4952c-943">Conclusion</span></span>
<span data-ttu-id="4952c-944">財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4952c-945">したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。</span><span class="sxs-lookup"><span data-stu-id="4952c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4952c-946">コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。</span><span class="sxs-lookup"><span data-stu-id="4952c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4952c-947">各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4952c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4952c-948">原価要素</span><span class="sxs-lookup"><span data-stu-id="4952c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4952c-949">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4952c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4952c-950">小計</span><span class="sxs-lookup"><span data-stu-id="4952c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4952c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4952c-951">CC099</span></span></th>
<th><span data-ttu-id="4952c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4952c-952">CC001</span></span></th>
<th><span data-ttu-id="4952c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4952c-953">CC002</span></span></th>
<th><span data-ttu-id="4952c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4952c-954">CC003</span></span></th>
<th><span data-ttu-id="4952c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4952c-955">CC004</span></span></th>
<th><span data-ttu-id="4952c-956">プロジェクト 1</span><span class="sxs-lookup"><span data-stu-id="4952c-956">Proj 1</span></span></th>
<th><span data-ttu-id="4952c-957">プロジェクト 2</span><span class="sxs-lookup"><span data-stu-id="4952c-957">Proj 2</span></span></th>
<th><span data-ttu-id="4952c-958">製品 1</span><span class="sxs-lookup"><span data-stu-id="4952c-958">Prod 1</span></span></th>
<th><span data-ttu-id="4952c-959">製品 2</span><span class="sxs-lookup"><span data-stu-id="4952c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4952c-960">10001 電気</span><span class="sxs-lookup"><span data-stu-id="4952c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4952c-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4952c-970">未分類</span><span class="sxs-lookup"><span data-stu-id="4952c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-971">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4952c-972">固定費</span><span class="sxs-lookup"><span data-stu-id="4952c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-973">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-974">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-975">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-976">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-977">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4952c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4952c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4952c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4952c-981">変動費</span><span class="sxs-lookup"><span data-stu-id="4952c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-982">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-983">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-984">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-985">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-986">0.00</span><span class="sxs-lookup"><span data-stu-id="4952c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-987">30.00</span><span class="sxs-lookup"><span data-stu-id="4952c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-988">10.00</span><span class="sxs-lookup"><span data-stu-id="4952c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4952c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4952c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4952c-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4952c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4952c-992">このトピックでは、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。</span><span class="sxs-lookup"><span data-stu-id="4952c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4952c-993">したがって、この間接費は組織の最下位レベルに配賦されます。</span><span class="sxs-lookup"><span data-stu-id="4952c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4952c-994">つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。</span><span class="sxs-lookup"><span data-stu-id="4952c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4952c-995">コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。</span><span class="sxs-lookup"><span data-stu-id="4952c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4952c-996">詳細については、「[原価ロールアップ](cost-rollup.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4952c-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




