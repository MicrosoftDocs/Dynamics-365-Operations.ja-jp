---
title: 報酬プロセスの定義と結果の計算
description: 報酬プロセスは、固定および変動報酬プランに登録された従業員の新しい報酬金額および報奨を決定するのに使用されます。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e4f49d9167e6d96500c7dbf5c1a25e04796b33a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113224"
---
# <a name="define-compensation-process-and-calculate-results"></a><span data-ttu-id="696e2-103">報酬プロセスの定義と結果の計算</span><span class="sxs-lookup"><span data-stu-id="696e2-103">Define compensation process and calculate results</span></span>

<span data-ttu-id="696e2-104">報酬プロセスは、固定および変動報酬プランに登録された従業員の新しい報酬金額および報奨を決定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="696e2-104">Compensation processes are used to determine new compensation amounts and awards for employees enrolled in fixed and variable compensation plans.</span></span> <span data-ttu-id="696e2-105">報酬プロセスは」は、すべての変更および設定が正しいことを確認するため「what-if」分析を複数回実行できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-105">Compensation processes can be run multiple times to perform "what-if" analysis, to verify all changes and settings are correct.</span></span> <span data-ttu-id="696e2-106">この手順では、報酬プロセスを作成し、プロセスを実行し、結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="696e2-106">This procedure will create a compensation process, run the process, and view the results.</span></span> <span data-ttu-id="696e2-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="696e2-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-compensation-process"></a><span data-ttu-id="696e2-108">報酬プロセスの作成</span><span class="sxs-lookup"><span data-stu-id="696e2-108">Create a compensation process</span></span>
1. <span data-ttu-id="696e2-109">[人事管理] > [報酬] > [プロセス] > [報酬プロセス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="696e2-109">Go to Human resources > Compensation > Process > Compensation processes.</span></span>
2. <span data-ttu-id="696e2-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-110">Click New.</span></span>
3. <span data-ttu-id="696e2-111">[プロセス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-111">In the Process field, type a value.</span></span>
4. <span data-ttu-id="696e2-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="696e2-113">[プロセス タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-113">In the Process type field, select an option.</span></span>
    * <span data-ttu-id="696e2-114">サイクルは報酬を決定するための評価期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="696e2-114">A cycle specifies the time period evaluated to determine compensation.</span></span> <span data-ttu-id="696e2-115">評価は、職位を保持する従業員、含まれる業績評価、従業員がサイクル中に使用した時間の割合の計算などを考慮します。</span><span class="sxs-lookup"><span data-stu-id="696e2-115">The evaluation considers which positions were held by employees, which performance ratings to include, calculation of the percentage of time the employee was employed during the cycle, and more.</span></span> <span data-ttu-id="696e2-116">サイクル開始日の例は過去の会計年度の最初の日の場合があります。</span><span class="sxs-lookup"><span data-stu-id="696e2-116">An example of a cycle start date might be the first day of the past fiscal year.</span></span>  
6. <span data-ttu-id="696e2-117">[サイクル開始] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-117">In the Cycle start field, enter a date.</span></span>
    * <span data-ttu-id="696e2-118">サイクルの終了日は、1 つ以上の報酬プランで実際に雇用され、登録された従業員を特定するのに使用される日付であるため、重要です。</span><span class="sxs-lookup"><span data-stu-id="696e2-118">The cycle end date is  important because it is the date used to determine which employees were actively employed and enrolled in one or more compensation plans.</span></span>  
7. <span data-ttu-id="696e2-119">[サイクル終了] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-119">In the Cycle end field, enter a date.</span></span>
    * <span data-ttu-id="696e2-120">トランザクションの有効日は、新しい報酬率が有効になる日付です。</span><span class="sxs-lookup"><span data-stu-id="696e2-120">The transaction active date is the date the new compensation rates should take effect.</span></span> <span data-ttu-id="696e2-121">一般には、サイクルの終了時と新しい報酬率が有効になる日付の間には数か月含まれます。</span><span class="sxs-lookup"><span data-stu-id="696e2-121">Many companies include a few months between their end of a cycle and the time the new compensation rates go into effect.</span></span> <span data-ttu-id="696e2-122">追加の時間は新しい報酬を処理して確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="696e2-122">The additional time is used for processing and reviewing the new compensation.</span></span>  
8. <span data-ttu-id="696e2-123">[トランザクションの有効日] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-123">In the Transaction active date field, enter a date.</span></span>
    * <span data-ttu-id="696e2-124">特定の時点の日付は、この時点での報酬率に基づいた従業員の報奨額を決定する変動報酬プランのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="696e2-124">The point-in-time date is used for variable compensation plans that determine an employee's award amount based on their compensation rate at this point in time.</span></span>  
    * <span data-ttu-id="696e2-125">固定支払比例配分の採用日付は、パーセンテージの採用ルールによる固定報酬プランに使用されます。</span><span class="sxs-lookup"><span data-stu-id="696e2-125">The fixed pay pro rated hire date is used with fixed compensation plans with a hire rule of Percent.</span></span>  <span data-ttu-id="696e2-126">固定支払比例配分の採用日付の間に採用された従業員は、比例配分率の代わりに、計算済の報酬昇給の 100% を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="696e2-126">Employees who are hired between the cycle start and the fixed pay pro rated hire date will receive 100% of their calculated compensation increase, instead of pro-rated percentage.</span></span>  
9. <span data-ttu-id="696e2-127">[固定支払比例配分の採用日付] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-127">In the Fixed pay pro rated hire date field, enter a date.</span></span>
    * <span data-ttu-id="696e2-128">期限の確認はトランザクションの有効日前に従業員の報酬レコードに読み込むために、すべてのプロセス結果を確認する日付です。</span><span class="sxs-lookup"><span data-stu-id="696e2-128">The review deadline is the date by which all process results should be reviewed so that they can be loaded into an employee's compensation record before the transaction active date.</span></span> <span data-ttu-id="696e2-129">これは情報提供のみを目的としたフィールドです。</span><span class="sxs-lookup"><span data-stu-id="696e2-129">This field is informational only.</span></span>  
10. <span data-ttu-id="696e2-130">[期限の確認] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-130">In the Review deadline field, enter a date.</span></span>
11. <span data-ttu-id="696e2-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-131">Click Save.</span></span>

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a><span data-ttu-id="696e2-132">報酬プロセスのための報酬計画とアクションの設定</span><span class="sxs-lookup"><span data-stu-id="696e2-132">Setup the compensation plans and actions for a compensation process</span></span>
1. <span data-ttu-id="696e2-133">[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-133">Click Setup.</span></span>
    * <span data-ttu-id="696e2-134">[設定] ページは、この報酬プロセスの一部として処理するプランおよび各プランに対して実行する必要のあるアクションを選択するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="696e2-134">The Setup page is used to select which plans to process as part of this compensation process, as well as which actions should be taken against each plan.</span></span>  
2. <span data-ttu-id="696e2-135">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-135">In the Plan field, enter or select a value.</span></span>
3. <span data-ttu-id="696e2-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-136">Click Save.</span></span>
4. <span data-ttu-id="696e2-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-137">Click Add.</span></span>
5. <span data-ttu-id="696e2-138">[アクション] フィールドで、[株主資本] アクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-138">In the Action field, select an Equity type of action.</span></span>
6. <span data-ttu-id="696e2-139">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-139">Click Add.</span></span>
7. <span data-ttu-id="696e2-140">[アクション] フィールドで、[メリット] アクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-140">In the Action field, select a Merit type of action.</span></span>
    * <span data-ttu-id="696e2-141">このアクションの計算の開始点として、選択したアクションが従業員の基準賃金を選択するか、前のアクションの結果を選択するかを示すため [前回の結果を使用] フィールドを使用して、報酬アクションを連鎖することができます。</span><span class="sxs-lookup"><span data-stu-id="696e2-141">Compensation actions can be "chained" together using the Use previous result field to indicate whether the selected action should use the employees base pay or the result of the previous action as the starting point for this action's calculation.</span></span>  
8. <span data-ttu-id="696e2-142">[前回の結果を使用] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-142">Select Yes in the Use previous result field.</span></span>
9. <span data-ttu-id="696e2-143">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-143">Click Add.</span></span>
10. <span data-ttu-id="696e2-144">[アクション] フィールドで、[一般] のアクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-144">In the Action field, select a General type of Action.</span></span>
    * <span data-ttu-id="696e2-145">さまざまな報酬アクションのタイプにより、さまざまなフィールドが有効になります。</span><span class="sxs-lookup"><span data-stu-id="696e2-145">Different compensation action types enable different fields.</span></span> <span data-ttu-id="696e2-146">[一般的な報酬アクション] タイプに対して、増加率または増加額を指定できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-146">For a General compensation action type, an increase percent or increase amount can be specified.</span></span>  
11. <span data-ttu-id="696e2-147">[増加額の選択] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-147">Select the Select increase amount option.</span></span>
12. <span data-ttu-id="696e2-148">[増加額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-148">In the Increase amount field, enter a number.</span></span>
13. <span data-ttu-id="696e2-149">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-149">Click Add.</span></span>
14. <span data-ttu-id="696e2-150">[アクション] フィールドで、[プロモーション] アクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-150">In the Action field, select a Promotion type of Action.</span></span>
    * <span data-ttu-id="696e2-151">[プロモーション] および [その他のレベル変更] アクション タイプにより、ユーザーは従業員報酬に手動調整を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="696e2-151">Promotion and Other level change action types enable users to make manual adjustments to employee compensation.</span></span> <span data-ttu-id="696e2-152">これらのアクション タイプにより報酬認定が有効になり、その他のアクション タイプでも従業員への推奨される報酬値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-152">Recommendations can be enabled for these action types, as well as other action types to enable you to enter a new recommended compensation value for an employee.</span></span>  
15. <span data-ttu-id="696e2-153">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-153">Click Add.</span></span>
16. <span data-ttu-id="696e2-154">[タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-154">In the Type field, select an option.</span></span>
    * <span data-ttu-id="696e2-155">固定と変動報酬プランは同じ報酬プロセスで実行できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-155">Fixed and variable compensation plans can be run in the same compensation process.</span></span>  
17. <span data-ttu-id="696e2-156">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-156">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="696e2-157">[能力給の有効化] チェック ボックスを使用して、固定と変動報酬の金額が、従業員の業績評価に基づいて調整される必要があるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="696e2-157">Use the Enable pay for performance check box to determined whether fixed and variable compensation amounts should be adjusted based on the employee's performance rating.</span></span>  
    * <span data-ttu-id="696e2-158">レバレッジは、変動報酬プランで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="696e2-158">Leverage can be overridden on variable compensation plans.</span></span>  
18. <span data-ttu-id="696e2-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-159">Click Save.</span></span>
19. <span data-ttu-id="696e2-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-160">Click Add.</span></span>
20. <span data-ttu-id="696e2-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="696e2-161">Close the page.</span></span>

## <a name="run-the-compensation-process"></a><span data-ttu-id="696e2-162">報酬プロセスの実行</span><span class="sxs-lookup"><span data-stu-id="696e2-162">Run the compensation process</span></span>
1. <span data-ttu-id="696e2-163">[プロセスの実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-163">Click Run process.</span></span>
    * <span data-ttu-id="696e2-164">[処理結果の表示] コントロールで、処理が完了したら完全報酬プロセスのメッセージの処理を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="696e2-164">The Show processing results control lets you view processing messages for the complete compensation process when processing has finished.</span></span>  
2. <span data-ttu-id="696e2-165">[処理結果の表示] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-165">Select Yes in the Show processing results field.</span></span>
3. <span data-ttu-id="696e2-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-166">Click OK.</span></span>

## <a name="view-the-results"></a><span data-ttu-id="696e2-167">結果の表示</span><span class="sxs-lookup"><span data-stu-id="696e2-167">View the results</span></span>
1. <span data-ttu-id="696e2-168">[プロセス結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-168">Click Process results.</span></span>
2. <span data-ttu-id="696e2-169">[従業員の結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-169">Click Employee results.</span></span>
3. <span data-ttu-id="696e2-170">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-170">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="696e2-171">[固定報酬] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="696e2-171">Expand the Fixed compensation section.</span></span>
    * <span data-ttu-id="696e2-172">プロセスの結果を表示するには、[クイック タブ] を展開します。</span><span class="sxs-lookup"><span data-stu-id="696e2-172">Expand the FastTabs to view the results of the process.</span></span> <span data-ttu-id="696e2-173">[報酬認定の有効化] が報酬アクションにたいしてマークを付けられたら、[認定] フィールドがそのアクションで有効にされます。</span><span class="sxs-lookup"><span data-stu-id="696e2-173">If Enable recommendations was marked for a compensation action, the Recommendation fields will be enabled for that action.</span></span>  
5. <span data-ttu-id="696e2-174">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-174">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="696e2-175">単一の従業員の結果は [結果の表示] ボタンをクリックして表示できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-175">The results for a single employee can be viewed by clicking the View results button.</span></span>  
    * <span data-ttu-id="696e2-176">[認定] フィールドで、割合または増加額を調整することによって、計算された報酬額を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="696e2-176">You can overwrite the calculated compensation amount by adjusting the percent or the increase amount in the Recommendation fields.</span></span>  
6. <span data-ttu-id="696e2-177">推奨率フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-177">In the percent recommended field, enter a number.</span></span>
7. <span data-ttu-id="696e2-178">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="696e2-178">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="696e2-179">推奨率フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="696e2-179">In the percent recommended field, enter a number.</span></span>
    * <span data-ttu-id="696e2-180">[再計算] は既存のレコードに対する変更を無視して、選択した従業員の新しい報酬の結果を生成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="696e2-180">Recalculate can be used to ignore any changes made to the existing record and generate a new compensation result for the selected employee.</span></span>  
    * <span data-ttu-id="696e2-181">すべての変更が従業員に対して完了すると、ステータスを [承認済] に変更します。</span><span class="sxs-lookup"><span data-stu-id="696e2-181">When all changes are complete for an employee, change the status to Approved.</span></span>  
9. <span data-ttu-id="696e2-182">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-182">Click Change status.</span></span>
10. <span data-ttu-id="696e2-183">[承認済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="696e2-183">Click Approved.</span></span>
    * <span data-ttu-id="696e2-184">レコードが承認された後は、従業員の公式の報酬レコードに読み込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="696e2-184">After the record has been approved it can be loaded to the employee's official compensation record.</span></span> <span data-ttu-id="696e2-185">新しい報酬は、報酬プロセスで設定されているトランザクション日付の時点で有効です。</span><span class="sxs-lookup"><span data-stu-id="696e2-185">The new compensation will be effective as of the transaction date set on the compensation process.</span></span>  

