---
title: 休暇と欠勤の概念
description: このトピックでは、休暇と欠勤の概念、および休暇残高がどのように決定されるかを説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461785"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="a6c02-103">休暇と欠勤の概念</span><span class="sxs-lookup"><span data-stu-id="a6c02-103">Leave and absence concepts</span></span>

<span data-ttu-id="a6c02-104">このトピックで説明されている概念と用語は、従業員に休暇を付与する方法、およびその従業員の休暇残高をどのように計算するかを判断するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="a6c02-105">休暇と欠勤の管理の詳細については、[休暇と欠勤の管理](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6c02-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="a6c02-106">休暇計画の詳細</span><span class="sxs-lookup"><span data-stu-id="a6c02-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="a6c02-107">入社日</span><span class="sxs-lookup"><span data-stu-id="a6c02-107">Start date</span></span>

<span data-ttu-id="a6c02-108">開始日は、見越計上処理が開始される日付です。</span><span class="sxs-lookup"><span data-stu-id="a6c02-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="a6c02-109">開始日は、繰越金額の計算に使用される記念日の日付としても使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="a6c02-110">見越計上</span><span class="sxs-lookup"><span data-stu-id="a6c02-110">Accruals</span></span>

<span data-ttu-id="a6c02-111">見越し計上は、従業員にいつ、どのくらいの頻度で休暇を付与するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="a6c02-112">休暇計画の設定時に、見越額をいつ付与するかに関するポリシー、および比例配分に関するポリシーが **見越計上** セクションで定義されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="a6c02-113">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-113">Accrual frequency</span></span>

<span data-ttu-id="a6c02-114">見越計上の頻度は、どのくらいの頻度で休暇が見越計上または付与されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="a6c02-115"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-115">The following options are available:</span></span>

- <span data-ttu-id="a6c02-116">毎日</span><span class="sxs-lookup"><span data-stu-id="a6c02-116">Daily</span></span>
- <span data-ttu-id="a6c02-117">毎週</span><span class="sxs-lookup"><span data-stu-id="a6c02-117">Weekly</span></span>
- <span data-ttu-id="a6c02-118">隔週</span><span class="sxs-lookup"><span data-stu-id="a6c02-118">Biweekly</span></span>
- <span data-ttu-id="a6c02-119">半月ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-119">Semimonthly</span></span>
- <span data-ttu-id="a6c02-120">月 1 回</span><span class="sxs-lookup"><span data-stu-id="a6c02-120">Monthly</span></span>
- <span data-ttu-id="a6c02-121">四半期に 1 回</span><span class="sxs-lookup"><span data-stu-id="a6c02-121">Quarterly</span></span>
- <span data-ttu-id="a6c02-122">半年ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-122">Semiannually</span></span>
- <span data-ttu-id="a6c02-123">毎年</span><span class="sxs-lookup"><span data-stu-id="a6c02-123">Annually</span></span>
- <span data-ttu-id="a6c02-124">なし</span><span class="sxs-lookup"><span data-stu-id="a6c02-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="a6c02-125">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-125">Accrual period basis</span></span>

<span data-ttu-id="a6c02-126">見越計上期間の基準は、見越計上期間の計算に使用される日付を決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="a6c02-127"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-127">The following options are available:</span></span>

- <span data-ttu-id="a6c02-128">**計画の開始日**</span><span class="sxs-lookup"><span data-stu-id="a6c02-128">**Plan start date**</span></span>
- <span data-ttu-id="a6c02-129">**従業員の特定の日付** ー このオプションが選択されているとき、値は、見越計上期間の計算に使用される最初の日付の値のソースを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="a6c02-130"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-130">The following options are available:</span></span>

    - <span data-ttu-id="a6c02-131">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a6c02-131">Custom</span></span>
    - <span data-ttu-id="a6c02-132">記念日</span><span class="sxs-lookup"><span data-stu-id="a6c02-132">Anniversary date</span></span>
    - <span data-ttu-id="a6c02-133">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="a6c02-133">Original hire date</span></span>
    - <span data-ttu-id="a6c02-134">勤続日数</span><span class="sxs-lookup"><span data-stu-id="a6c02-134">Seniority date</span></span>
    - <span data-ttu-id="a6c02-135">作業者の調整済開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="a6c02-136">作業者の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="a6c02-137">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-137">Accrual award date</span></span>

<span data-ttu-id="a6c02-138">見越休暇付与日は、従業員にいつ休暇を付与するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="a6c02-139"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-139">The following options are available:</span></span>

- <span data-ttu-id="a6c02-140">**見越計上期間の終了日** ー 報酬期間の最終日に従業員に休暇が付与されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="a6c02-141">正確な金額を見越計上するには、見越計上処理に期間全体が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6c02-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="a6c02-142">たとえば、見越計上期間は 2018 年 1 月 1 日から 2018 年 1 月 31 日までです。</span><span class="sxs-lookup"><span data-stu-id="a6c02-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="a6c02-143">この場合、1 月を含めるには、見越計上を 2018 年 2 月 1 日に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6c02-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="a6c02-144">**見越計上期間の開始日** ー 報酬期間の初日に従業員に休暇が付与されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="a6c02-145">登録の見越計上ポリシー</span><span class="sxs-lookup"><span data-stu-id="a6c02-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="a6c02-146">登録の見越計上ポリシーでは、見越計上期間の途中で従業員が登録されたときに、見越計上を計算する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="a6c02-147"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-147">The following options are available:</span></span>

- <span data-ttu-id="a6c02-148">**比例配分** ー 登録日と開始日の日付範囲は、日数の差を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="a6c02-149">見越計上が処理されるときに、その差が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="a6c02-150">**完全な見越計上** ー 階層に基づいた完全な見越計上金額は、最初の見越計上処理中に付与されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="a6c02-151">**見越計上なし** ー 見越計上は、次の見越計上期間まで付与されません。</span><span class="sxs-lookup"><span data-stu-id="a6c02-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="a6c02-152">登録解除の見越計上ポリシー</span><span class="sxs-lookup"><span data-stu-id="a6c02-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="a6c02-153">登録解除の見越計上ポリシーでは、見越計上期間の途中で従業員が登録解除されたときに、見越計上を計算する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="a6c02-154"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-154">The following options are available:</span></span>

- <span data-ttu-id="a6c02-155">**比例配分** ー 登録日と開始日の日付範囲は、日数の差を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="a6c02-156">見越計上が処理されるときに、その差が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="a6c02-157">**完全な見越計上** ー 階層に基づいた完全な見越計上金額は、最初の見越計上処理中に付与されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="a6c02-158">**見越計上なし** ー 見越計上は、次の見越計上期間まで付与されません。</span><span class="sxs-lookup"><span data-stu-id="a6c02-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="a6c02-159">見越計上スケジュール</span><span class="sxs-lookup"><span data-stu-id="a6c02-159">Accrual schedule</span></span>

<span data-ttu-id="a6c02-160">見越計上スケジュールは、従業員が休暇を見越計上する方法、およびその従業員がどの程度の量を見越計上し、繰り越すかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="a6c02-161">さまざまなレベルに基づく休暇が付与されるように、階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="a6c02-162">勤続月数</span><span class="sxs-lookup"><span data-stu-id="a6c02-162">Months of service</span></span>

<span data-ttu-id="a6c02-163">**勤続月数** 値は、従業が見越計上を受ける権利を得るために働く必要のある最低月数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="a6c02-164">従業員に最低月数が要求されていない場合は、値を **0** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="a6c02-165">作業時間</span><span class="sxs-lookup"><span data-stu-id="a6c02-165">Hours worked</span></span>

<span data-ttu-id="a6c02-166">**作業時間** 値は、従業が見越計上を受ける権利を得るために、見越計上期間ごとに働く必要のある最低時間数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="a6c02-167">従業員に最低月数が要求されていない場合は、値を **0** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="a6c02-168">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-168">Accrual amount</span></span>

<span data-ttu-id="a6c02-169">見越計上量は、従業員が期間ごとに見越計上する時間数または日数です。</span><span class="sxs-lookup"><span data-stu-id="a6c02-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="a6c02-170">期間は、見越計上の頻度に基づいています。</span><span class="sxs-lookup"><span data-stu-id="a6c02-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="a6c02-171">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-171">Minimum balance</span></span>

<span data-ttu-id="a6c02-172">従業員が利用可能な休暇の量を超える休暇を要求できる場合は、負の値を最小残高に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="a6c02-173">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-173">Maximum carry-forward</span></span>

<span data-ttu-id="a6c02-174">見越計上処理は、開始日の記念日に最大繰越残高を超過する休暇残高を調整します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="a6c02-175">交付量</span><span class="sxs-lookup"><span data-stu-id="a6c02-175">Grant amount</span></span>

<span data-ttu-id="a6c02-176">交付量は、従業員が最初に休暇計画に登録する際に付与される最初の時間数または日数です。</span><span class="sxs-lookup"><span data-stu-id="a6c02-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="a6c02-177">量は、各見越計上期間ごとに見越計上しません。</span><span class="sxs-lookup"><span data-stu-id="a6c02-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="a6c02-178">登録および残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="a6c02-179">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-179">Enrollment date</span></span>

<span data-ttu-id="a6c02-180">登録日は、従業員が休暇の見越計上をいつ開始できるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a6c02-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="a6c02-181">たとえば、従業員が 2018 年 6 月 15 日に休暇計画に登録した場合、その従業員は 2018 年 6 月 15 日以前の休暇を見越計上することはできません。</span><span class="sxs-lookup"><span data-stu-id="a6c02-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="a6c02-182">現在の残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-182">Current balance</span></span>

<span data-ttu-id="a6c02-183">現在の残高は、休暇時間要求に対して使用できる休暇の量です。</span><span class="sxs-lookup"><span data-stu-id="a6c02-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="a6c02-184">この量には、見越計上、承認済の要求、および現在の日付までの調整が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="a6c02-185">現在の残高の例</span><span class="sxs-lookup"><span data-stu-id="a6c02-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="a6c02-186">年間計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-186">Annual plan</span></span>

<span data-ttu-id="a6c02-187">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-187">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-188">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-188">Plan start date</span></span> | <span data-ttu-id="a6c02-189">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-189">Enrollment date</span></span> | <span data-ttu-id="a6c02-190">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-190">Accrual frequency</span></span> | <span data-ttu-id="a6c02-191">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-191">Accrual period basis</span></span> | <span data-ttu-id="a6c02-192">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-193">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-193">1/1/2018</span></span>        | <span data-ttu-id="a6c02-194">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-194">1/1/2018</span></span>        | <span data-ttu-id="a6c02-195">年次</span><span class="sxs-lookup"><span data-stu-id="a6c02-195">Annual</span></span>            | <span data-ttu-id="a6c02-196">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-196">Plan start date</span></span>      | <span data-ttu-id="a6c02-197">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-197">End of accrual period</span></span> |

<span data-ttu-id="a6c02-198">期間全体が含まれるように、見越計上は 2019 年 1 月 1 日 (1/1/2019) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-199">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-199">**Results**</span></span>

| <span data-ttu-id="a6c02-200">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-200">Accrual amount</span></span> | <span data-ttu-id="a6c02-201">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-201">Minimum balance</span></span> | <span data-ttu-id="a6c02-202">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-202">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-203">要求金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-203">Request amount</span></span> | <span data-ttu-id="a6c02-204">現在の残高 (2019 年 1 月 1 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a6c02-205">200</span><span class="sxs-lookup"><span data-stu-id="a6c02-205">200</span></span>            | <span data-ttu-id="a6c02-206">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-206">0</span></span>               | <span data-ttu-id="a6c02-207">120</span><span class="sxs-lookup"><span data-stu-id="a6c02-207">120</span></span>                   | <span data-ttu-id="a6c02-208">40</span><span class="sxs-lookup"><span data-stu-id="a6c02-208">40</span></span>             | <span data-ttu-id="a6c02-209">160</span><span class="sxs-lookup"><span data-stu-id="a6c02-209">160</span></span>                              |

<span data-ttu-id="a6c02-210">現在の残高 (160) = 見越計上金額 (200) ー 要求金額 (40)</span><span class="sxs-lookup"><span data-stu-id="a6c02-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="a6c02-211">半月ごとの計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-211">Semimonthly plan</span></span>

<span data-ttu-id="a6c02-212">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-212">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-213">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-213">Plan start date</span></span> | <span data-ttu-id="a6c02-214">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-214">Enrollment date</span></span> | <span data-ttu-id="a6c02-215">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-215">Accrual frequency</span></span> | <span data-ttu-id="a6c02-216">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-216">Accrual period basis</span></span> | <span data-ttu-id="a6c02-217">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-218">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-218">1/1/2018</span></span>        | <span data-ttu-id="a6c02-219">2018 年 2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-219">2/1/2018</span></span>        | <span data-ttu-id="a6c02-220">半月ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-220">Semimonthly</span></span>       | <span data-ttu-id="a6c02-221">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-221">Plan start date</span></span>      | <span data-ttu-id="a6c02-222">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-222">End of accrual period</span></span> |

<span data-ttu-id="a6c02-223">期間全体が含まれるように、見越計上は 2018 年 5 月 5 日 (5/1/2018) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-224">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-224">**Results**</span></span>

| <span data-ttu-id="a6c02-225">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-225">Accrual amount</span></span> | <span data-ttu-id="a6c02-226">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-226">Minimum balance</span></span> | <span data-ttu-id="a6c02-227">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-227">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-228">要求金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-228">Request amount</span></span> | <span data-ttu-id="a6c02-229">現在の残高 (2019 年 1 月 1 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a6c02-230">5</span><span class="sxs-lookup"><span data-stu-id="a6c02-230">5</span></span>              | <span data-ttu-id="a6c02-231">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-231">0</span></span>               | <span data-ttu-id="a6c02-232">120</span><span class="sxs-lookup"><span data-stu-id="a6c02-232">120</span></span>                   | <span data-ttu-id="a6c02-233">8</span><span class="sxs-lookup"><span data-stu-id="a6c02-233">8</span></span>              | <span data-ttu-id="a6c02-234">22</span><span class="sxs-lookup"><span data-stu-id="a6c02-234">22</span></span>                               |

<span data-ttu-id="a6c02-235">現在の残高 (22) = 見越計上金額 (5 × 6) ー 要求金額 (8)</span><span class="sxs-lookup"><span data-stu-id="a6c02-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="a6c02-236">月ごとの計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-236">Monthly plan</span></span>

<span data-ttu-id="a6c02-237">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-237">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-238">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-238">Plan start date</span></span> | <span data-ttu-id="a6c02-239">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-239">Enrollment date</span></span> | <span data-ttu-id="a6c02-240">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-240">Accrual frequency</span></span> | <span data-ttu-id="a6c02-241">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-241">Accrual period basis</span></span> | <span data-ttu-id="a6c02-242">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-243">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-243">1/1/2018</span></span>        | <span data-ttu-id="a6c02-244">2018 年 2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-244">2/1/2018</span></span>        | <span data-ttu-id="a6c02-245">半月ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-245">Semimonthly</span></span>       | <span data-ttu-id="a6c02-246">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-246">Plan start date</span></span>      | <span data-ttu-id="a6c02-247">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-247">End of accrual period</span></span> |

<span data-ttu-id="a6c02-248">期間全体が含まれるように、見越計上は 2018 年 5 月 5 日 (5/1/2018) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-249">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-249">**Results**</span></span>

| <span data-ttu-id="a6c02-250">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-250">Accrual amount</span></span> | <span data-ttu-id="a6c02-251">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-251">Minimum balance</span></span> | <span data-ttu-id="a6c02-252">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-252">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-253">要求金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-253">Request amount</span></span> | <span data-ttu-id="a6c02-254">現在の残高 (2019 年 1 月 1 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="a6c02-255">5</span><span class="sxs-lookup"><span data-stu-id="a6c02-255">5</span></span>              | <span data-ttu-id="a6c02-256">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-256">0</span></span>               | <span data-ttu-id="a6c02-257">120</span><span class="sxs-lookup"><span data-stu-id="a6c02-257">120</span></span>                   | <span data-ttu-id="a6c02-258">8</span><span class="sxs-lookup"><span data-stu-id="a6c02-258">8</span></span>              | <span data-ttu-id="a6c02-259">7</span><span class="sxs-lookup"><span data-stu-id="a6c02-259">7</span></span>                                |

<span data-ttu-id="a6c02-260">現在の残高 (7) = 見越計上金額 (5 × 3) ー 要求金額 (8)</span><span class="sxs-lookup"><span data-stu-id="a6c02-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="a6c02-261">予測残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-261">Forecasted balance</span></span>

<span data-ttu-id="a6c02-262">*予測残高* は、未来の日付で使用できる休暇の量です。</span><span class="sxs-lookup"><span data-stu-id="a6c02-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="a6c02-263">見越計上と繰越調整がその日までに予測されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="a6c02-264">次の式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-264">The following formula is used:</span></span>

<span data-ttu-id="a6c02-265">月曜の予測残高 = 現在の残高 ー 要求 + 見越計上 ー 繰越調整</span><span class="sxs-lookup"><span data-stu-id="a6c02-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="a6c02-266">予測残高の例</span><span class="sxs-lookup"><span data-stu-id="a6c02-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="a6c02-267">年間計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-267">Annual plan</span></span>

<span data-ttu-id="a6c02-268">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-268">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-269">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-269">Plan start date</span></span> | <span data-ttu-id="a6c02-270">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-270">Enrollment date</span></span> | <span data-ttu-id="a6c02-271">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-271">Accrual frequency</span></span> | <span data-ttu-id="a6c02-272">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-272">Accrual period basis</span></span> | <span data-ttu-id="a6c02-273">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-274">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-274">1/1/2018</span></span>        | <span data-ttu-id="a6c02-275">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-275">1/1/2018</span></span>        | <span data-ttu-id="a6c02-276">年次</span><span class="sxs-lookup"><span data-stu-id="a6c02-276">Annual</span></span>            | <span data-ttu-id="a6c02-277">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-277">Plan start date</span></span>      | <span data-ttu-id="a6c02-278">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-278">End of accrual period</span></span> |

<span data-ttu-id="a6c02-279">期間全体が含まれるように、見越計上は 2019 年 2 月 15 日 (2/15/2019) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-280">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-280">**Results**</span></span>

| <span data-ttu-id="a6c02-281">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-281">Accrual amount</span></span> | <span data-ttu-id="a6c02-282">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-282">Minimum balance</span></span> | <span data-ttu-id="a6c02-283">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-283">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-284">現在の残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-284">Current balance</span></span> | <span data-ttu-id="a6c02-285">予測残高 (2019 年 2 月 15 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a6c02-286">20</span><span class="sxs-lookup"><span data-stu-id="a6c02-286">20</span></span>             | <span data-ttu-id="a6c02-287">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-287">0</span></span>               | <span data-ttu-id="a6c02-288">20</span><span class="sxs-lookup"><span data-stu-id="a6c02-288">20</span></span>                    | <span data-ttu-id="a6c02-289">40</span><span class="sxs-lookup"><span data-stu-id="a6c02-289">40</span></span>              | <span data-ttu-id="a6c02-290">40</span><span class="sxs-lookup"><span data-stu-id="a6c02-290">40</span></span>                                   |

<span data-ttu-id="a6c02-291">予測残高 (40) = 見越計上金額 (20) + 現在の残高 (40) ー 繰越調整 (20)</span><span class="sxs-lookup"><span data-stu-id="a6c02-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="a6c02-292">半月ごとの計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-292">Semimonthly plan</span></span>

<span data-ttu-id="a6c02-293">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-293">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-294">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-294">Plan start date</span></span> | <span data-ttu-id="a6c02-295">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-295">Enrollment date</span></span> | <span data-ttu-id="a6c02-296">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-296">Accrual frequency</span></span> | <span data-ttu-id="a6c02-297">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-297">Accrual period basis</span></span> | <span data-ttu-id="a6c02-298">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-299">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-299">1/1/2018</span></span>        | <span data-ttu-id="a6c02-300">2018 年 2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-300">2/1/2018</span></span>        | <span data-ttu-id="a6c02-301">半月ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-301">Semimonthly</span></span>       | <span data-ttu-id="a6c02-302">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-302">Plan start date</span></span>      | <span data-ttu-id="a6c02-303">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-303">End of accrual period</span></span> |

<span data-ttu-id="a6c02-304">期間全体が含まれるように、見越計上は 2019 年 2 月 15 日 (2/15/2019) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-305">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-305">**Results**</span></span>

| <span data-ttu-id="a6c02-306">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-306">Accrual amount</span></span> | <span data-ttu-id="a6c02-307">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-307">Minimum balance</span></span> | <span data-ttu-id="a6c02-308">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-308">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-309">現在の残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-309">Current balance</span></span> | <span data-ttu-id="a6c02-310">予測残高 (2019 年 2 月 15 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a6c02-311">5</span><span class="sxs-lookup"><span data-stu-id="a6c02-311">5</span></span>              | <span data-ttu-id="a6c02-312">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-312">0</span></span>               | <span data-ttu-id="a6c02-313">20</span><span class="sxs-lookup"><span data-stu-id="a6c02-313">20</span></span>                    | <span data-ttu-id="a6c02-314">40</span><span class="sxs-lookup"><span data-stu-id="a6c02-314">40</span></span>              | <span data-ttu-id="a6c02-315">35</span><span class="sxs-lookup"><span data-stu-id="a6c02-315">35</span></span>                                   |

<span data-ttu-id="a6c02-316">予測残高 (35) = 見越計上金額 (5 × 3) + 現在の残高 (40) ー 繰越調整 (20)</span><span class="sxs-lookup"><span data-stu-id="a6c02-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="a6c02-317">月ごとの計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-317">Monthly plan</span></span>

<span data-ttu-id="a6c02-318">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-318">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-319">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-319">Plan start date</span></span> | <span data-ttu-id="a6c02-320">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-320">Enrollment date</span></span> | <span data-ttu-id="a6c02-321">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-321">Accrual frequency</span></span> | <span data-ttu-id="a6c02-322">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-322">Accrual period basis</span></span> | <span data-ttu-id="a6c02-323">見越休暇付与日</span><span class="sxs-lookup"><span data-stu-id="a6c02-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="a6c02-324">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-324">1/1/2018</span></span>        | <span data-ttu-id="a6c02-325">2018 年 2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-325">2/1/2018</span></span>        | <span data-ttu-id="a6c02-326">半月ごと</span><span class="sxs-lookup"><span data-stu-id="a6c02-326">Semimonthly</span></span>       | <span data-ttu-id="a6c02-327">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-327">Plan start date</span></span>      | <span data-ttu-id="a6c02-328">見越計上期間の終了日</span><span class="sxs-lookup"><span data-stu-id="a6c02-328">End of accrual period</span></span> |

<span data-ttu-id="a6c02-329">期間全体が含まれるように、見越計上は 2019 年 2 月 15 日 (2/15/2019) に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a6c02-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="a6c02-330">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-330">**Results**</span></span>

| <span data-ttu-id="a6c02-331">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-331">Accrual amount</span></span> | <span data-ttu-id="a6c02-332">最小残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-332">Minimum balance</span></span> | <span data-ttu-id="a6c02-333">最大繰越</span><span class="sxs-lookup"><span data-stu-id="a6c02-333">Maximum carry-forward</span></span> | <span data-ttu-id="a6c02-334">現在の残高</span><span class="sxs-lookup"><span data-stu-id="a6c02-334">Current balance</span></span> | <span data-ttu-id="a6c02-335">予測残高 (2019 年 2 月 15 日時点)</span><span class="sxs-lookup"><span data-stu-id="a6c02-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="a6c02-336">10</span><span class="sxs-lookup"><span data-stu-id="a6c02-336">10</span></span>             | <span data-ttu-id="a6c02-337">0</span><span class="sxs-lookup"><span data-stu-id="a6c02-337">0</span></span>               | <span data-ttu-id="a6c02-338">20</span><span class="sxs-lookup"><span data-stu-id="a6c02-338">20</span></span>                    | <span data-ttu-id="a6c02-339">40</span><span class="sxs-lookup"><span data-stu-id="a6c02-339">40</span></span>              | <span data-ttu-id="a6c02-340">30</span><span class="sxs-lookup"><span data-stu-id="a6c02-340">30</span></span>                                   |

<span data-ttu-id="a6c02-341">予測残高 (30) = 見越計上金額 (10 × 1) + 現在の残高 (40) ー 繰越調整 (20)</span><span class="sxs-lookup"><span data-stu-id="a6c02-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="a6c02-342">比例配分残高の例</span><span class="sxs-lookup"><span data-stu-id="a6c02-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="a6c02-343">比例配分の月間計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-343">Prorated monthly plan</span></span>

<span data-ttu-id="a6c02-344">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-344">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-345">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-345">Plan start date</span></span> | <span data-ttu-id="a6c02-346">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-346">Accrual frequency</span></span> | <span data-ttu-id="a6c02-347">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a6c02-348">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-348">1/1/2018</span></span>        | <span data-ttu-id="a6c02-349">月 1 回</span><span class="sxs-lookup"><span data-stu-id="a6c02-349">Monthly</span></span>           | <span data-ttu-id="a6c02-350">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-350">Plan start date</span></span>      |

<span data-ttu-id="a6c02-351">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-351">**Results**</span></span>

| <span data-ttu-id="a6c02-352">従業員</span><span class="sxs-lookup"><span data-stu-id="a6c02-352">Employee</span></span>            | <span data-ttu-id="a6c02-353">勤続月数</span><span class="sxs-lookup"><span data-stu-id="a6c02-353">Months of service</span></span> | <span data-ttu-id="a6c02-354">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-354">Enrollment date</span></span> | <span data-ttu-id="a6c02-355">入社日</span><span class="sxs-lookup"><span data-stu-id="a6c02-355">Start date</span></span> | <span data-ttu-id="a6c02-356">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-356">Accrual amount</span></span> | <span data-ttu-id="a6c02-357">処理の見越計上</span><span class="sxs-lookup"><span data-stu-id="a6c02-357">Process accrual</span></span> | <span data-ttu-id="a6c02-358">差引</span><span class="sxs-lookup"><span data-stu-id="a6c02-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a6c02-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a6c02-359">Jeannette Nicholson</span></span> | <span data-ttu-id="a6c02-360">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-360">0.00</span></span>              | <span data-ttu-id="a6c02-361">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-361">6/1/2018</span></span>        | <span data-ttu-id="a6c02-362">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-362">6/1/2018</span></span>   | <span data-ttu-id="a6c02-363">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-363">1.00</span></span>           | <span data-ttu-id="a6c02-364">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-364">9/1/2018</span></span>        | <span data-ttu-id="a6c02-365">3.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-365">3.00</span></span>    |
| <span data-ttu-id="a6c02-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a6c02-366">Jay Norman</span></span>          | <span data-ttu-id="a6c02-367">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-367">0.00</span></span>              | <span data-ttu-id="a6c02-368">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-368">6/15/2018</span></span>       | <span data-ttu-id="a6c02-369">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-369">6/15/2018</span></span>  | <span data-ttu-id="a6c02-370">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-370">1.00</span></span>           | <span data-ttu-id="a6c02-371">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-371">9/1/2018</span></span>        | <span data-ttu-id="a6c02-372">2.53</span><span class="sxs-lookup"><span data-stu-id="a6c02-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="a6c02-373">完全な見越計上の月間計画</span><span class="sxs-lookup"><span data-stu-id="a6c02-373">Full accrual monthly plan</span></span>

<span data-ttu-id="a6c02-374">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-374">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-375">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-375">Plan start date</span></span> | <span data-ttu-id="a6c02-376">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-376">Accrual frequency</span></span> | <span data-ttu-id="a6c02-377">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a6c02-378">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-378">1/1/2018</span></span>        | <span data-ttu-id="a6c02-379">月 1 回</span><span class="sxs-lookup"><span data-stu-id="a6c02-379">Monthly</span></span>           | <span data-ttu-id="a6c02-380">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-380">Plan start date</span></span>      |

<span data-ttu-id="a6c02-381">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-381">**Results**</span></span>

| <span data-ttu-id="a6c02-382">従業員</span><span class="sxs-lookup"><span data-stu-id="a6c02-382">Employee</span></span>            | <span data-ttu-id="a6c02-383">勤続月数</span><span class="sxs-lookup"><span data-stu-id="a6c02-383">Months of service</span></span> | <span data-ttu-id="a6c02-384">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-384">Enrollment date</span></span> | <span data-ttu-id="a6c02-385">入社日</span><span class="sxs-lookup"><span data-stu-id="a6c02-385">Start date</span></span> | <span data-ttu-id="a6c02-386">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-386">Accrual amount</span></span> | <span data-ttu-id="a6c02-387">処理の見越計上</span><span class="sxs-lookup"><span data-stu-id="a6c02-387">Process accrual</span></span> | <span data-ttu-id="a6c02-388">差引</span><span class="sxs-lookup"><span data-stu-id="a6c02-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a6c02-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a6c02-389">Jeannette Nicholson</span></span> | <span data-ttu-id="a6c02-390">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-390">0.00</span></span>              | <span data-ttu-id="a6c02-391">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-391">6/1/2018</span></span>        | <span data-ttu-id="a6c02-392">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-392">6/1/2018</span></span>   | <span data-ttu-id="a6c02-393">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-393">1.00</span></span>           | <span data-ttu-id="a6c02-394">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-394">9/1/2018</span></span>        | <span data-ttu-id="a6c02-395">3.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-395">3.00</span></span>    |
| <span data-ttu-id="a6c02-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a6c02-396">Jay Norman</span></span>          | <span data-ttu-id="a6c02-397">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-397">0.00</span></span>              | <span data-ttu-id="a6c02-398">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-398">6/15/2018</span></span>       | <span data-ttu-id="a6c02-399">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-399">6/15/2018</span></span>  | <span data-ttu-id="a6c02-400">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-400">1.00</span></span>           | <span data-ttu-id="a6c02-401">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-401">9/1/2018</span></span>        | <span data-ttu-id="a6c02-402">3.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="a6c02-403">見越計上の月間計画がない</span><span class="sxs-lookup"><span data-stu-id="a6c02-403">No accrual monthly plan</span></span>

<span data-ttu-id="a6c02-404">**計画の設定**</span><span class="sxs-lookup"><span data-stu-id="a6c02-404">**Plan setup**</span></span>

| <span data-ttu-id="a6c02-405">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-405">Plan start date</span></span> | <span data-ttu-id="a6c02-406">見越計上の頻度</span><span class="sxs-lookup"><span data-stu-id="a6c02-406">Accrual frequency</span></span> | <span data-ttu-id="a6c02-407">見越計上期間の基準</span><span class="sxs-lookup"><span data-stu-id="a6c02-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="a6c02-408">2018 年 1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-408">1/1/2018</span></span>        | <span data-ttu-id="a6c02-409">月 1 回</span><span class="sxs-lookup"><span data-stu-id="a6c02-409">Monthly</span></span>           | <span data-ttu-id="a6c02-410">計画の開始日</span><span class="sxs-lookup"><span data-stu-id="a6c02-410">Plan start date</span></span>      |

<span data-ttu-id="a6c02-411">**結果**</span><span class="sxs-lookup"><span data-stu-id="a6c02-411">**Results**</span></span>

| <span data-ttu-id="a6c02-412">従業員</span><span class="sxs-lookup"><span data-stu-id="a6c02-412">Employee</span></span>            | <span data-ttu-id="a6c02-413">勤続月数</span><span class="sxs-lookup"><span data-stu-id="a6c02-413">Months of service</span></span> | <span data-ttu-id="a6c02-414">登録日</span><span class="sxs-lookup"><span data-stu-id="a6c02-414">Enrollment date</span></span> | <span data-ttu-id="a6c02-415">入社日</span><span class="sxs-lookup"><span data-stu-id="a6c02-415">Start date</span></span> | <span data-ttu-id="a6c02-416">見越計上金額</span><span class="sxs-lookup"><span data-stu-id="a6c02-416">Accrual amount</span></span> | <span data-ttu-id="a6c02-417">処理の見越計上</span><span class="sxs-lookup"><span data-stu-id="a6c02-417">Process accrual</span></span> | <span data-ttu-id="a6c02-418">差引</span><span class="sxs-lookup"><span data-stu-id="a6c02-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="a6c02-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="a6c02-419">Jeannette Nicholson</span></span> | <span data-ttu-id="a6c02-420">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-420">0.00</span></span>              | <span data-ttu-id="a6c02-421">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-421">6/1/2018</span></span>        | <span data-ttu-id="a6c02-422">2018 年 6 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-422">6/1/2018</span></span>   | <span data-ttu-id="a6c02-423">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-423">1.00</span></span>           | <span data-ttu-id="a6c02-424">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-424">9/1/2018</span></span>        | <span data-ttu-id="a6c02-425">3.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-425">3.00</span></span>    |
| <span data-ttu-id="a6c02-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="a6c02-426">Jay Norman</span></span>          | <span data-ttu-id="a6c02-427">0.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-427">0.00</span></span>              | <span data-ttu-id="a6c02-428">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-428">6/15/2018</span></span>       | <span data-ttu-id="a6c02-429">2018 年 6 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-429">6/15/2018</span></span>  | <span data-ttu-id="a6c02-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-430">1.00</span></span>           | <span data-ttu-id="a6c02-431">2018 年 9 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a6c02-431">9/1/2018</span></span>        | <span data-ttu-id="a6c02-432">2.00</span><span class="sxs-lookup"><span data-stu-id="a6c02-432">2.00</span></span>    |
