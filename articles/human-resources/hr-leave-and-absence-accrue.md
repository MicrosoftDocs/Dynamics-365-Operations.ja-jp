---
title: 休暇計画の見越計上
description: Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3048f9b6b52a150219067430abb54e5b5bf5c3e4
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197316"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="90593-103">休暇計画の見越計上</span><span class="sxs-lookup"><span data-stu-id="90593-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="90593-104">Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。</span><span class="sxs-lookup"><span data-stu-id="90593-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="90593-105">複数の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="90593-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="90593-106">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="90593-107">**休暇の管理**で、**休暇計画の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="90593-108">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="90593-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="90593-109">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="90593-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="90593-110">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="90593-110">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="90593-111">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="90593-111">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="90593-112">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-112">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="90593-113">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-113">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="90593-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-114">Select **OK**.</span></span> <span data-ttu-id="90593-115">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="90593-115">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="90593-116">個々の従業員の休暇を累計する</span><span class="sxs-lookup"><span data-stu-id="90593-116">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="90593-117">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-117">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="90593-118">**休暇の累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-118">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="90593-119">**休暇計画の累計** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="90593-119">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="90593-120">**累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="90593-120">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="90593-121">バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="90593-121">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="90593-122">累計処理の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="90593-122">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="90593-123">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-123">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="90593-124">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-124">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="90593-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-125">Select **OK**.</span></span> <span data-ttu-id="90593-126">設定したパラメーターで累計処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="90593-126">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="90593-127">複数従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="90593-127">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="90593-128">特定の計画や日付範囲に対する発生レコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="90593-128">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="90593-129">発生日は今日または将来の日付にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90593-129">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="90593-130">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-130">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="90593-131">**休暇の管理**で、**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-131">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="90593-132">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-132">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="90593-133">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-133">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="90593-134">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-134">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="90593-135">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="90593-135">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="90593-136">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-136">Select **OK**.</span></span> <span data-ttu-id="90593-137">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="90593-137">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="90593-138">単一従業員の休暇の発生を削除する</span><span class="sxs-lookup"><span data-stu-id="90593-138">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="90593-139">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-139">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="90593-140">**休暇計画の累計の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-140">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="90593-141">**休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-141">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="90593-142">該当する場合は、**残日数調整の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-142">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="90593-143">**有給休暇付与日** を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-143">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="90593-144">この日付は、今日または将来のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="90593-144">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="90593-145">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-145">Select **OK**.</span></span> <span data-ttu-id="90593-146">累計処理では、設定したパラメーターで発生を削除します。</span><span class="sxs-lookup"><span data-stu-id="90593-146">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="90593-147">休暇の発生および削除プロセスの確認</span><span class="sxs-lookup"><span data-stu-id="90593-147">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="90593-148">**休暇発生の監査** は、1 人またはすべての従業員の発生を実行または削除するたびに表示されます。</span><span class="sxs-lookup"><span data-stu-id="90593-148">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="90593-149">アクションを実行した日付と担当者も表示されます。</span><span class="sxs-lookup"><span data-stu-id="90593-149">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="90593-150">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-150">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="90593-151">**休暇の管理**で、**休暇発生の監査の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90593-151">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="90593-152">参照</span><span class="sxs-lookup"><span data-stu-id="90593-152">See also</span></span>

- [<span data-ttu-id="90593-153">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="90593-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="90593-154">休暇および欠勤計画の作成</span><span class="sxs-lookup"><span data-stu-id="90593-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
