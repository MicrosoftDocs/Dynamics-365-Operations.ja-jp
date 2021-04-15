---
title: 報酬の構造の作成
description: この記事では、固定報酬プランを作成する方法、および適格性ルールで計画に従業員を登録する有効にする方法について説明します。
author: andreabichsel
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75d1a05d4f94689581e2a67a13adeef6b14ac0cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800906"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="2fc38-103">報酬の構造の作成</span><span class="sxs-lookup"><span data-stu-id="2fc38-103">Develop a compensation structure</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2fc38-104">この記事では、固定報酬プランを作成する方法、および適格性ルールで計画に従業員を登録する有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="2fc38-105">この記事は、USMF のデモ データを使用し、報酬と給付金マネージャーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="2fc38-106">固定報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="2fc38-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="2fc38-107">**報酬管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="2fc38-108">**固定報酬プランの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="2fc38-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-109">Select **New**.</span></span>

4. <span data-ttu-id="2fc38-110">**プラン** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="2fc38-111">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="2fc38-112">**有効日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="2fc38-113">**タイプ** フィールドで、固定報酬プランが **バンド**、**等級**、**ステップ** 計画のいずれであるかを選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="2fc38-114">**許可された報酬認定** チェック ボックスは、プロセス イベントでこの計画に追加されたアクションの既定値として機能します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="2fc38-115">報酬認定を許可すると、報酬を処理するときに計算された規定額を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="2fc38-116">**許容範囲外** フィールドでは、特定のレベルに対して、指定の報酬構造の範囲外になる報酬額をどのように処理するかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="2fc38-117">**許容範囲外** フィールドを **なし** に設定すると、任意の報酬額を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="2fc38-118">**ソフトの許容範囲** では、報酬額がそのレベルの最小基準点の金額より少ない場合、または最大金額を超える場合に、ユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="2fc38-119">ユーザーは警告を無視して操作を継続できます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="2fc38-120">**ハードの許容範囲** では、従業員の報酬額がそのレベルの最小または最大の基準点の範囲外の場合にエラーを生成します。また、従業員の報酬が範囲内になるように自動的に調整します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="2fc38-121">**採用ルール** フィールドは、プロセス イベントの実行中に従業員の報酬を計算します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="2fc38-122">**割合** の **採用ルール** は、作業者がサイクル内で雇用されている期間に比例する昇給を計算します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="2fc38-123">**通貨** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="2fc38-124">**支払レートの交換** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="2fc38-125">**給与レンジ到達割合マトリックス** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="2fc38-126">必要に応じて、レンジ到達割合のレコードを追加すると、中間点までは早く、範囲の最大値に達するには遅くする調整を従業員に対して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="2fc38-127">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-127">Select **Save**.</span></span> <span data-ttu-id="2fc38-128">これにより、**報酬の設定** ボタンが有効になり、計画の報酬構造の定義が続行されます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="2fc38-129">**報酬の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-129">Select **Set up compensation**.</span></span> <span data-ttu-id="2fc38-130">報酬構造は、次の 3 つのうちいずれかの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="2fc38-131">まったく新しい構造を作成します。基準点のセットを選択し、レベルを追加して独自の構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="2fc38-132">既存の計画から報酬構造をコピーし、開始点とします。これを新しい計画に合うように編集します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="2fc38-133">既存の報酬グリッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-133">Select an existing compensation grid.</span></span> <span data-ttu-id="2fc38-134">別のプランで報酬グリッドが既に使用されている場合、このグリッドに対する変更は、他の計画にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="2fc38-135">**既存の報酬マトリックスから新しいマトリックスを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="2fc38-136">**グリッドからコピー** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="2fc38-137">必要に応じて、選択されたグリッドをコピーして、作成する新しい報酬グリッドの名前を変更できます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="2fc38-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-138">Select **OK**.</span></span>

19. <span data-ttu-id="2fc38-139">**一括変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-139">Select **Mass change**.</span></span> <span data-ttu-id="2fc38-140">**一括変更** では、1 つまたは複数のレベルや基準点に対する、増加割合または一定量の引き上げを指定することにより、報酬マトリックスの金額を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="2fc38-141">**調整金額** フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="2fc38-142">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="2fc38-143">**グリッドに適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2fc38-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="2fc38-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-144">Close the page.</span></span> <span data-ttu-id="2fc38-145">報酬構造を作成した後は、固定報酬プランの標準職務給として使用する基準点を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="2fc38-146">標準職務給は、従業員のコンパレシオの計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="2fc38-147">**標準職務給** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="2fc38-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="2fc38-149">固定報酬プランの適格性ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="2fc38-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="2fc38-150">固定報酬プランは、適格性ルールが計画に対して定義されるまで、従業員に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="2fc38-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="2fc38-151">**適格性ルール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="2fc38-152">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-152">Select **New**.</span></span>

3. <span data-ttu-id="2fc38-153">**適格性** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="2fc38-154">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="2fc38-155">**有効日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="2fc38-156">固定報酬プランと変動報酬プランの両方で適格性ルールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="2fc38-157">**タイプ** フィールドで、計画のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="2fc38-158">**計画** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="2fc38-159">従業員が報酬プランの登録対象になるために満たす必要のある基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="2fc38-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="2fc38-160">基準には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-160">Criteria can include:</span></span>

    - <span data-ttu-id="2fc38-161">**部門**</span><span class="sxs-lookup"><span data-stu-id="2fc38-161">**Department**</span></span>
    - <span data-ttu-id="2fc38-162">**労働組合**</span><span class="sxs-lookup"><span data-stu-id="2fc38-162">**Labor union**</span></span>
    - <span data-ttu-id="2fc38-163">**場所** (**報酬地域**)</span><span class="sxs-lookup"><span data-stu-id="2fc38-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="2fc38-164">**職務**</span><span class="sxs-lookup"><span data-stu-id="2fc38-164">**Job**</span></span>
    - <span data-ttu-id="2fc38-165">**職務**</span><span class="sxs-lookup"><span data-stu-id="2fc38-165">**Function**</span></span>
    - <span data-ttu-id="2fc38-166">**職務タイプ**</span><span class="sxs-lookup"><span data-stu-id="2fc38-166">**Job type**</span></span>
    - <span data-ttu-id="2fc38-167">**報酬レベル**</span><span class="sxs-lookup"><span data-stu-id="2fc38-167">**Compensation level**</span></span>
    
    <span data-ttu-id="2fc38-168">従業員は、報酬プランの登録対象になるには、指定された基準をすべて満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fc38-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="2fc38-169">基準を指定していない場合、すべての従業員が報酬プランの登録対象になります。</span><span class="sxs-lookup"><span data-stu-id="2fc38-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="2fc38-170">従業員が適格性ルールで指定した条件を満たさない場合、または適格性ルールが報酬プランに対して指定されていない場合は、従業員の固定報酬レコードを作成するときに報酬プランがルックアップに表示されません。</span><span class="sxs-lookup"><span data-stu-id="2fc38-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="2fc38-171">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-171">Close the page.</span></span>

8. <span data-ttu-id="2fc38-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2fc38-172">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]