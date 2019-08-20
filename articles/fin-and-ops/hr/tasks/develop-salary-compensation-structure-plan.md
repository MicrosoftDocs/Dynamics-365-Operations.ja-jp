---
title: 給与/報酬の構造と計画の作成
description: このタスク ガイドでは、固定報酬プランを作成するプロセス、および適格性ルールで計画に登録する従業員を有効にするプロセスについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f0732736736fdc87f3367f24b1d20b9fa6efc59
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794907"
---
# <a name="develop-salarycompensation-structure-and-plan"></a><span data-ttu-id="1c7ff-103">給与/報酬の構造と計画の作成</span><span class="sxs-lookup"><span data-stu-id="1c7ff-103">Develop salary/compensation structure and plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c7ff-104">このタスク ガイドでは、固定報酬プランを作成するプロセス、および適格性ルールで計画に登録する従業員を有効にするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-104">This task guide walks though the process of creating a Fixed compensation plan and enabling employees to be enrolled in the plan through eligibility rules.</span></span> <span data-ttu-id="1c7ff-105">このタスクの作成に使用されるデモ データの会社は USMF で、このタスクは報酬と給付金マネージャー向けの想定です。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-105">The demo data company used to create this task is USMF and the task is intended for Compensation and Benefits Managers.</span></span>


## <a name="create-fixed-compensation-plan"></a><span data-ttu-id="1c7ff-106">固定報酬プランを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-106">Create fixed compensation plan</span></span>
1. <span data-ttu-id="1c7ff-107">[報酬管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-107">Click Compensation management.</span></span>
2. <span data-ttu-id="1c7ff-108">[固定報酬プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-108">Click Fixed compensation plans.</span></span>
3. <span data-ttu-id="1c7ff-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-109">Click New.</span></span>
4. <span data-ttu-id="1c7ff-110">[計画] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-110">In the Plan field, type a value.</span></span>
5. <span data-ttu-id="1c7ff-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1c7ff-112">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-112">In the Effective date field, enter a date.</span></span>
7. <span data-ttu-id="1c7ff-113">[タイプ] フィールドで、固定報酬プランがバンド、等級、ステップ計画のいずれであるかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-113">In the Type field, select whether the Fixed compensation plan is a Band, Grade, or Step plan.</span></span>
8. <span data-ttu-id="1c7ff-114">[許可された報酬認定] チェック ボックスは、プロセス イベントでこの計画に追加されたアクションの既定値として機能します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-114">The Recommendation allowed checkbox acts as a default value for any actions added to this plan in a Process event.</span></span>  <span data-ttu-id="1c7ff-115">報酬認定を許可すると、報酬を処理するときに計算された規定額を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>
9. <span data-ttu-id="1c7ff-116">[許容範囲外] では、特定のレベルに対して、指定の報酬構造の範囲外になる報酬額をどのように処理するかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-116">The Out of range tolerance allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span>  <span data-ttu-id="1c7ff-117">[許容範囲外] が [なし] のとき、任意の報酬額が使用できます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-117">An Out of range tolerance of None will allow any compensation amount to be used.</span></span>  <span data-ttu-id="1c7ff-118">[ソフトの許容範囲] では、報酬額がそのレベルの最小基準点の金額より少ない場合、またはそのレベルの最大金額を超える場合に、ユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-118">A Soft tolerance will warn the user if the compensation amount is less than the minimum reference point amount for that level, or greater than the maximum amount for that level.</span></span> <span data-ttu-id="1c7ff-119">ユーザーは警告を無視して操作を継続できます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-119">The user can ignore the warning and continue.</span></span>  <span data-ttu-id="1c7ff-120">[ハードの許容範囲] では、従業員の報酬額がそのレベルの最小または最大の基準点の範囲外の場合にエラーを生成します。また、従業員の報酬が範囲内になるように自動的に調整します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-120">A Hard tolerance will generate an error if an employee's compensation is set outside of the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>
10. <span data-ttu-id="1c7ff-121">[採用ルール] フィールドは、従業員の報酬を計算するための報酬プロセス イベントの実行時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-121">The Hire rule field is used when a compensation Process event is run to calculate an employee's compensation.</span></span>  <span data-ttu-id="1c7ff-122">[採用ルール] が [割合] の場合、作業者がサイクル内で雇用されている期間に比例する昇給を計算します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-122">A Hire rule of Percent will calculate an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>
11. <span data-ttu-id="1c7ff-123">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-123">In the Currency field, type a value.</span></span>
12. <span data-ttu-id="1c7ff-124">[支払レートの交換] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-124">In the Pay rate conversion field, enter or select a value.</span></span>
13. <span data-ttu-id="1c7ff-125">[給与レンジ到達割合マトリックス] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-125">Expand the Range utilization matrix section.</span></span>
    * <span data-ttu-id="1c7ff-126">必要に応じて、レンジ到達割合のレコードを追加すると、中間点までは早く、範囲の最大値に達するには遅くする調整を従業員に対して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>  
14. <span data-ttu-id="1c7ff-127">この時点で、[報酬の設定] ボタンを有効にするには、固定報酬プランを保存する必要があります。その後、その計画の報酬構造の定義を引き続き行います。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-127">At this point, you must save the Fixed compensation plan to enable the Set up compensation button and continue defining your compensation structure for the plan.</span></span>  <span data-ttu-id="1c7ff-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-128">Click Save.</span></span>
15. <span data-ttu-id="1c7ff-129">[報酬の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-129">Click Set up compensation.</span></span>
    * <span data-ttu-id="1c7ff-130">報酬構造を作成する方法は 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-130">There are three ways to create a compensation structure.</span></span> <span data-ttu-id="1c7ff-131">1: まったく新しい構造を作成します。基準点のセットを選択し、レベルを追加して独自の構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-131">1: Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span> <span data-ttu-id="1c7ff-132">2: 既存の計画から報酬構造をコピーし、開始点とします。これを新しい計画に合うように編集します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-132">2: Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span> <span data-ttu-id="1c7ff-133">3: 既存の報酬グリッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-133">3: Select an existing compensation grid.</span></span> <span data-ttu-id="1c7ff-134">報酬グリッドが別のプランで既に使用されている場合、このグリッドに対する変更は、他の計画にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-134">If the compensation grid is already being used by another plan, any changes made to the grid will also be reflected in the other plan.</span></span>  
16. <span data-ttu-id="1c7ff-135">[既存の報酬マトリックスから新しいマトリックスを作成] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-135">Select the Create new from existing compensation matrix option.</span></span>
17. <span data-ttu-id="1c7ff-136">[グリッドからコピー] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-136">In the Copy from grid field, enter or select a value.</span></span>
    * <span data-ttu-id="1c7ff-137">必要に応じて、選択されたグリッドの複製として作成される新しい報酬グリッドの名前を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-137">Optionally you can change the name of the new compensation grid that will be created as a copy of the selected grid.</span></span>  
18. <span data-ttu-id="1c7ff-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-138">Click OK.</span></span>
19. <span data-ttu-id="1c7ff-139">[一括変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-139">Click Mass change.</span></span>
    * <span data-ttu-id="1c7ff-140">一括変更では、1 つまたは複数のレベルや基準点に対する、増加割合または一定量の引き上げを指定することにより、報酬マトリックスの金額を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-140">Mass change allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels and/or reference points.</span></span>  
20. <span data-ttu-id="1c7ff-141">[調整金額] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-141">In the Adjustment amount field, enter a number.</span></span>
21. <span data-ttu-id="1c7ff-142">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-142">In the list, mark or unmark all rows.</span></span>
22. <span data-ttu-id="1c7ff-143">[グリッドに適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-143">Click Apply to grid.</span></span>
23. <span data-ttu-id="1c7ff-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-144">Close the page.</span></span>
    * <span data-ttu-id="1c7ff-145">報酬構造を作成または選択した後は、固定報酬プランの標準職務給として使用する基準点を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-145">Once a compensation structure has been created or selected, you can select which of the reference points should be used as the Control point for the Fixed compensation plan.</span></span>  <span data-ttu-id="1c7ff-146">標準職務給は、従業員のコンパレシオの計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-146">The Control point is used to calculate an employee's Compa Ratio.</span></span>  
24. <span data-ttu-id="1c7ff-147">[標準職務給] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-147">In the Control point field, enter or select a value.</span></span>
25. <span data-ttu-id="1c7ff-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a><span data-ttu-id="1c7ff-149">新しい固定報酬プランの適格性ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-149">Create an eligibility rule for the new Fixed compensation plan</span></span>
    * <span data-ttu-id="1c7ff-150">新しい固定報酬プランは、適格性ルールが計画に対して定義されるまで、従業員に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-150">The new Fixed compensation plan cannot be assigned to an employee until Eligibility rules have been defined for the plan.</span></span>  
1. <span data-ttu-id="1c7ff-151">[適格性ルール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-151">Click Eligibility rules.</span></span>
2. <span data-ttu-id="1c7ff-152">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-152">Click New.</span></span>
3. <span data-ttu-id="1c7ff-153">[適格性] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-153">In the Eligibility field, type a value.</span></span>
4. <span data-ttu-id="1c7ff-154">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1c7ff-155">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-155">In the Effective date field, enter a date.</span></span>
    * <span data-ttu-id="1c7ff-156">適格性ルールは、固定報酬プランと変動報酬プランの両方に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-156">Eligibility rules are used for both Fixed and Variable compensation plans.</span></span>  <span data-ttu-id="1c7ff-157">[タイプ] フィールドで、この適格性ルールのセットの対象とする計画タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-157">In the Type field, select which type of plan this set of eligibility rules is for.</span></span>  
6. <span data-ttu-id="1c7ff-158">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-158">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="1c7ff-159">従業員が報酬プランの登録対象になるために満たす必要のある基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="1c7ff-160">基準には、部門、労働組合、場所 (報酬場所)、職務、機能、ジョブ タイプ、および報酬レベルを含むことができます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-160">Criteria can include a Department, Labor union, Location (Compensation region), Job, Function, Job type, or Compensation level.</span></span> <span data-ttu-id="1c7ff-161">従業員は、報酬プランの登録対象になるには、指定された基準をすべて満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-161">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="1c7ff-162">基準が指定されていない場合、すべての従業員が報酬プランの登録対象になります。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-162">If no criteria are specified, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="1c7ff-163">従業員が適格性ルールで指定した条件を満たさない場合、または適格性ルールが報酬プランに対して指定されていない場合は、従業員の固定報酬レコードを作成するときに報酬プランがルックアップに表示されません。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-163">If an employee does not meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan will not appear in the lookup when creating a Fixed compensation record for an employee.</span></span>  
7. <span data-ttu-id="1c7ff-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-164">Close the page.</span></span>
8. <span data-ttu-id="1c7ff-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1c7ff-165">Close the page.</span></span>

