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
ms.openlocfilehash: 43c16c5d0de91bf1f433f4fde36e7d13775f44a0
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712170"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="03fe0-103">休暇計画の見越計上</span><span class="sxs-lookup"><span data-stu-id="03fe0-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="03fe0-104">Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="03fe0-105">複数の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="03fe0-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="03fe0-106">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="03fe0-107">**休暇の管理**で、**休暇計画の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="03fe0-108">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="03fe0-109">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="03fe0-110">すべての会社に対して見越計上を実行する場合は、**すべての会社**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="03fe0-111">1つの休暇計画の見越計上を処理する場合は、**すべての計画**に対して **いいえ** を選択し、**休暇計画**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="03fe0-112">すべての会社を選択すると、個々の休暇プランは選択できません。</span><span class="sxs-lookup"><span data-stu-id="03fe0-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="03fe0-113">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="03fe0-114">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="03fe0-115">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="03fe0-116">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="03fe0-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-117">Select **OK**.</span></span> <span data-ttu-id="03fe0-118">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="03fe0-119">個々の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="03fe0-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="03fe0-120">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="03fe0-121">**休暇の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="03fe0-122">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="03fe0-123">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="03fe0-124">すべての会社に対して見越計上を実行する場合は、**すべての会社**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="03fe0-125">1つの休暇計画の見越計上を処理する場合は、**すべての計画**に対して **いいえ** を選択し、**休暇計画**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="03fe0-126">すべての会社を選択すると、個々の休暇プランは選択できません。</span><span class="sxs-lookup"><span data-stu-id="03fe0-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="03fe0-127">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="03fe0-128">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="03fe0-129">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="03fe0-130">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="03fe0-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-131">Select **OK**.</span></span> <span data-ttu-id="03fe0-132">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="03fe0-133">複数従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="03fe0-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="03fe0-134">特定の計画や日付範囲に対する発生レコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="03fe0-135">発生日は今日または将来の日付にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03fe0-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="03fe0-136">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="03fe0-137">**休暇の管理**で、**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="03fe0-138">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="03fe0-139">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="03fe0-140">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="03fe0-141">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03fe0-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="03fe0-142">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-142">Select **OK**.</span></span> <span data-ttu-id="03fe0-143">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="03fe0-144">単一従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="03fe0-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="03fe0-145">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="03fe0-146">**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="03fe0-147">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="03fe0-148">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="03fe0-149">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="03fe0-150">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03fe0-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="03fe0-151">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-151">Select **OK**.</span></span> <span data-ttu-id="03fe0-152">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="03fe0-153">休暇の発生および削除プロセスの確認</span><span class="sxs-lookup"><span data-stu-id="03fe0-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="03fe0-154">**休暇発生の監査** は、1 人またはすべての従業員の発生を実行または削除するたびに表示されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="03fe0-155">アクションを実行した日付と担当者も表示されます。</span><span class="sxs-lookup"><span data-stu-id="03fe0-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="03fe0-156">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="03fe0-157">**休暇の管理**で、**休暇発生の監査の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe0-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="03fe0-158">参照</span><span class="sxs-lookup"><span data-stu-id="03fe0-158">See also</span></span>

[<span data-ttu-id="03fe0-159">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="03fe0-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="03fe0-160">休暇および欠勤計画の作成</span><span class="sxs-lookup"><span data-stu-id="03fe0-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
