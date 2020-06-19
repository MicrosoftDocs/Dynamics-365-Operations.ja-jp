---
title: 休暇計画の見越計上
description: Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f045cb7ab9f5e7aa4259f29e1b026f110425c236
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429062"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="6888c-103">休暇計画の見越計上</span><span class="sxs-lookup"><span data-stu-id="6888c-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="6888c-104">Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。</span><span class="sxs-lookup"><span data-stu-id="6888c-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="6888c-105">複数の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="6888c-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="6888c-106">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6888c-107">**休暇の管理**で、**休暇計画の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="6888c-108">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="6888c-109">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6888c-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="6888c-110">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="6888c-110">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="6888c-111">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="6888c-111">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="6888c-112">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-112">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="6888c-113">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-113">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="6888c-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-114">Select **OK**.</span></span> <span data-ttu-id="6888c-115">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-115">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="6888c-116">個々の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="6888c-116">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="6888c-117">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-117">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="6888c-118">**休暇の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-118">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="6888c-119">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-119">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="6888c-120">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6888c-120">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="6888c-121">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="6888c-121">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="6888c-122">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="6888c-122">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="6888c-123">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-123">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="6888c-124">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-124">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="6888c-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-125">Select **OK**.</span></span> <span data-ttu-id="6888c-126">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-126">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="6888c-127">複数従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="6888c-127">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="6888c-128">特定の計画や日付範囲に対する発生レコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="6888c-128">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="6888c-129">発生日は今日または将来の日付にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6888c-129">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="6888c-130">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-130">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6888c-131">**休暇の管理**で、**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-131">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="6888c-132">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-132">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="6888c-133">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-133">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="6888c-134">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-134">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="6888c-135">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6888c-135">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="6888c-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-136">Select **OK**.</span></span> <span data-ttu-id="6888c-137">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="6888c-137">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="6888c-138">単一従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="6888c-138">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="6888c-139">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-139">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="6888c-140">**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-140">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="6888c-141">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-141">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="6888c-142">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-142">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="6888c-143">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-143">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="6888c-144">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6888c-144">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="6888c-145">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-145">Select **OK**.</span></span> <span data-ttu-id="6888c-146">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="6888c-146">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="6888c-147">休暇の発生および削除プロセスの確認</span><span class="sxs-lookup"><span data-stu-id="6888c-147">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="6888c-148">**休暇発生の監査** は、1 人またはすべての従業員の発生を実行または削除するたびに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-148">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="6888c-149">アクションを実行した日付と担当者も表示されます。</span><span class="sxs-lookup"><span data-stu-id="6888c-149">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="6888c-150">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-150">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6888c-151">**休暇の管理**で、**休暇発生の監査の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6888c-151">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="6888c-152">プレビューの機能の構成</span><span class="sxs-lookup"><span data-stu-id="6888c-152">Configure preview features</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

<span data-ttu-id="6888c-153">休暇および欠勤のプレビュー機能を有効にしている場合は、それらの設定も構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6888c-153">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

### <a name="accrue-leave-per-company-or-per-leave-plan"></a><span data-ttu-id="6888c-154">会社別または休暇プラン別の有給休暇</span><span class="sxs-lookup"><span data-stu-id="6888c-154">Accrue leave per company or per leave plan</span></span>

<span data-ttu-id="6888c-155">休暇および不就業プランの発生時には、すべての会社で発生することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6888c-155">When accruing leave and absence plans, you can choose to accrue for all companies.</span></span> <span data-ttu-id="6888c-156">すべての会社を選択すると、個々の休暇プランを選択できません。</span><span class="sxs-lookup"><span data-stu-id="6888c-156">If you choose all companies, you can't select individual leave plans.</span></span> <span data-ttu-id="6888c-157">すべての会社で発生しないことを選択した場合は、特定の休暇プランで発生できます。</span><span class="sxs-lookup"><span data-stu-id="6888c-157">If you choose to not accrue for all companies, you can accrue for a specific leave plan.</span></span> 

<span data-ttu-id="6888c-158">これらのオプションは、すべての従業員または個々の従業員に対して発生する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6888c-158">These options are available when accruing for all employees or individual employees.</span></span> 

## <a name="see-also"></a><span data-ttu-id="6888c-159">参照</span><span class="sxs-lookup"><span data-stu-id="6888c-159">See also</span></span>

[<span data-ttu-id="6888c-160">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="6888c-160">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="6888c-161">休暇および欠勤計画の作成</span><span class="sxs-lookup"><span data-stu-id="6888c-161">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
