---
title: "勤務時間外の登録"
description: "このトピックでは、勤務時間外登録を処理する方法について説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7ccac401b7364006e8ffc229a616bca8e48bf096
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="219f8-103">勤務時間外の登録</span><span class="sxs-lookup"><span data-stu-id="219f8-103">Absence registration in Time and attendance</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="219f8-104">このトピックでは、休暇の概念を説明し、勤務時間外登録を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="219f8-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="219f8-105">通常の勤務時間に基づく休暇</span><span class="sxs-lookup"><span data-stu-id="219f8-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="219f8-106">作業者は、通常の勤務時間中に働かない時間は、不在と見なされます。</span><span class="sxs-lookup"><span data-stu-id="219f8-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="219f8-107">通常の勤務時間は、作業者の標準勤務時間プロファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="219f8-108">たとえば、作業者は午前7時00分に出勤し、午後3時00分に退勤したという一日のプロファイルだったとします。</span><span class="sxs-lookup"><span data-stu-id="219f8-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="219f8-109">9:00に出勤した場合、作業者は、その日の午前7:00から午前9時までは休暇と見做されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="219f8-110">この場合、作業者は休暇の理由を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="219f8-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="219f8-111">作業者達は、休暇コードを選び理由を指定できます。</span><span class="sxs-lookup"><span data-stu-id="219f8-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="219f8-112">休暇コード</span><span class="sxs-lookup"><span data-stu-id="219f8-112">Absence codes</span></span>

<span data-ttu-id="219f8-113">休暇コードでは、さまざまなタイプの休暇を定義します。</span><span class="sxs-lookup"><span data-stu-id="219f8-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="219f8-114">休暇コードは、会社によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="219f8-115">休暇コードには、さまざまなルールを適用できます。</span><span class="sxs-lookup"><span data-stu-id="219f8-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="219f8-116">たとえば、控除または支払を許可する、休暇コードを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="219f8-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="219f8-117">たとえば、ある会社は、作業者が正当な理由がなく遅刻する時に使用する **遅刻** 休暇コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="219f8-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="219f8-118">会社はまた、社内研修に参加するための、**社内研修コース** 休暇コードも定義します。</span><span class="sxs-lookup"><span data-stu-id="219f8-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="219f8-119">これらの休暇コードは、**遅刻** は作業者の給与から差し引きされ、**社内研修コース** は作業者の給与から差し引きされないように設定できます。</span><span class="sxs-lookup"><span data-stu-id="219f8-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="219f8-120">自動休暇コードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="219f8-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="219f8-121">これらの休暇コードは、休暇が登録されなかった場合、作業者の時間を計算できます。</span><span class="sxs-lookup"><span data-stu-id="219f8-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="219f8-122">作業者の時間のプロファイルは、標準勤務時間、または、フレックス時間の休暇コードを使用するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="219f8-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="219f8-123">標準勤務時間とフレックス時間を設定する。</span><span class="sxs-lookup"><span data-stu-id="219f8-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="219f8-124">**時間と休暇のパラメータ**ページの**休暇の自動挿入**と**フレックスの自動挿入-**オプションを使用し、標準勤務時間とフレックスのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="219f8-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="219f8-125">休暇グループ</span><span class="sxs-lookup"><span data-stu-id="219f8-125">Absence groups</span></span>

<span data-ttu-id="219f8-126">休暇コードは、休暇グループに分類されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="219f8-127">休暇グループを使用し、共通の特性を持つ休暇コードをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="219f8-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="219f8-128">例としては、法的な休暇のための休暇コード、病院の予約、陪審義務または子供の病気を原因とする休暇コードなどがあります。</span><span class="sxs-lookup"><span data-stu-id="219f8-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="219f8-129">計画休暇</span><span class="sxs-lookup"><span data-stu-id="219f8-129">Planned absence</span></span>

<span data-ttu-id="219f8-130">予定されている休暇など、作業者が休暇を取ることがわかっている場合、計画休暇を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="219f8-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="219f8-131">計画休暇とみなされるように、休暇コードを設定し、計画休暇を設定します。</span><span class="sxs-lookup"><span data-stu-id="219f8-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="219f8-132">計画休暇を設定する際、ユーザーの時間登録が計算されるときは、休務期間中の休暇コードの入力は求められません。</span><span class="sxs-lookup"><span data-stu-id="219f8-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="219f8-133">1 人の作業者に対し計画休暇を定義できます。または作業者の予定休暇を一括更新する、バッチ ジョブを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="219f8-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="219f8-134">計画休暇を設定する</span><span class="sxs-lookup"><span data-stu-id="219f8-134">Set up planned absence</span></span>

1. <span data-ttu-id="219f8-135">**人事管理** &gt; **労働災害** &gt; **従業員**を選択し、従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="219f8-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="219f8-136">**時間** &gt; **時間の割り当て** &gt; **時間の休暇登録**を選択し、計画休暇を設定します。</span><span class="sxs-lookup"><span data-stu-id="219f8-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="219f8-137">計画休暇の中止</span><span class="sxs-lookup"><span data-stu-id="219f8-137">Interrupted planned absence</span></span>

<span data-ttu-id="219f8-138">計画休暇を設定する際、**中止** オプションを適用した場合、計画休暇期間中に作業者がサインインした場合、計画休暇は中止されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="219f8-139">計画休暇は、**中止**としてマークされ、今後の計算には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="219f8-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="219f8-140">中止する計画休暇を設定する。</span><span class="sxs-lookup"><span data-stu-id="219f8-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="219f8-141">計画休暇設定の手順に従い、**休暇時間登録** を開きます。</span><span class="sxs-lookup"><span data-stu-id="219f8-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="219f8-142">**中止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="219f8-142">Select **Interrupt**.</span></span>

<span data-ttu-id="219f8-143">**中止**オプションは、作業現場ターミナルまたは作業現場端末を通して時間を登録している際に適用されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="219f8-144">登録が計算および承認ページ、または、 **電子タイムカード** ページに入力されている場合、このオプションは適用されません。</span><span class="sxs-lookup"><span data-stu-id="219f8-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="219f8-145">フレックス プロファイルにおける休暇の使用例</span><span class="sxs-lookup"><span data-stu-id="219f8-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="219f8-146">次の 3 つの例は、フレックス期間を持つプロファイルで休暇を計算する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="219f8-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="219f8-147">例では、次のプロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="219f8-147">The examples use the following profile.</span></span>

| <span data-ttu-id="219f8-148">出勤</span><span class="sxs-lookup"><span data-stu-id="219f8-148">Clock-in</span></span> | <span data-ttu-id="219f8-149">標準勤務時間</span><span class="sxs-lookup"><span data-stu-id="219f8-149">Standard time</span></span>    | <span data-ttu-id="219f8-150">分割</span><span class="sxs-lookup"><span data-stu-id="219f8-150">Break</span></span>             | <span data-ttu-id="219f8-151">標準勤務時間</span><span class="sxs-lookup"><span data-stu-id="219f8-151">Standard time</span></span> | <span data-ttu-id="219f8-152">フレックス-</span><span class="sxs-lookup"><span data-stu-id="219f8-152">Flex-</span></span>        | <span data-ttu-id="219f8-153">退勤</span><span class="sxs-lookup"><span data-stu-id="219f8-153">Clock-out</span></span> | <span data-ttu-id="219f8-154">フレックス+</span><span class="sxs-lookup"><span data-stu-id="219f8-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="219f8-155">午前 8:00</span><span class="sxs-lookup"><span data-stu-id="219f8-155">8 AM</span></span>     | <span data-ttu-id="219f8-156">午前 9:00 から午前 11:30</span><span class="sxs-lookup"><span data-stu-id="219f8-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="219f8-157">午前 11:30 分から午後 12:00</span><span class="sxs-lookup"><span data-stu-id="219f8-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="219f8-158">午後 12:00 から午後 3:00</span><span class="sxs-lookup"><span data-stu-id="219f8-158">12 PM to 3 PM</span></span> | <span data-ttu-id="219f8-159">午後 3:00 から午後 4:00</span><span class="sxs-lookup"><span data-stu-id="219f8-159">3 PM to 4 PM</span></span> | <span data-ttu-id="219f8-160">午後 4:00</span><span class="sxs-lookup"><span data-stu-id="219f8-160">4 PM</span></span>      | <span data-ttu-id="219f8-161">午後 4:00 から午後 6:00</span><span class="sxs-lookup"><span data-stu-id="219f8-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="219f8-162">例1: フレックス期間中のサインアウト</span><span class="sxs-lookup"><span data-stu-id="219f8-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="219f8-163">作業者が午前8時00分に出勤し、午後3時30分に退勤。</span><span class="sxs-lookup"><span data-stu-id="219f8-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="219f8-164">この場合、作業者がフレックス期間中に退勤するため、休暇として計算されず、作業者のフレックス時間残数から 30 分差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="219f8-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="219f8-165">例2: 標準時間内のサインアウト</span><span class="sxs-lookup"><span data-stu-id="219f8-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="219f8-166">作業者が午前8時00分に出勤し、午後2時30分に退勤。</span><span class="sxs-lookup"><span data-stu-id="219f8-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="219f8-167">この場合、作業者が標準勤務時間の期間中に退勤したため、午後2時30分から午後4時までが休暇として計算され、1.5 時間の休暇期間として登録されます。</span><span class="sxs-lookup"><span data-stu-id="219f8-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="219f8-168">その期間の休暇コードは必須です。</span><span class="sxs-lookup"><span data-stu-id="219f8-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="219f8-169">例3: Flex+ 期間中のサインアウト</span><span class="sxs-lookup"><span data-stu-id="219f8-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="219f8-170">作業者が午前8時00分に出勤し、午後4時30分に退勤</span><span class="sxs-lookup"><span data-stu-id="219f8-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="219f8-171">この場合、作業者がフレックス+期間中に退勤するため、休暇として計算されず、作業者のフレックス時間残数から 30 分差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="219f8-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="219f8-172">計算と承認プロセス中の休暇</span><span class="sxs-lookup"><span data-stu-id="219f8-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="219f8-173">勤務時間の登録は、給与明細として給与計算システムに転送する前に、計算して承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="219f8-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="219f8-174">承認者は、作業者の時刻登録を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="219f8-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="219f8-175">承認者は、作業者が登録した全ての休暇を変更することさえできます。</span><span class="sxs-lookup"><span data-stu-id="219f8-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="219f8-176">承認者が休暇コードを持つ期間を手動で入力すると、その期間の休暇コードは、時間と欠勤パラメータのデフォルト休暇コードによって上書きされません。</span><span class="sxs-lookup"><span data-stu-id="219f8-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="219f8-177">たとえば、作業者が午前10時に出勤し、その女性が遅刻したことを示す休暇コードを選択したとします。</span><span class="sxs-lookup"><span data-stu-id="219f8-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="219f8-178">後で、作業者は、上司に対し、午前8:00から午前10:00の間に病院の診察を受けていたことを知らせたとします。</span><span class="sxs-lookup"><span data-stu-id="219f8-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="219f8-179">診察の場合は、作業者の給料から差し引かないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="219f8-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="219f8-180">したがって、この場合、上司は、2時間の病気を示す休暇コードを手動で入力し、午前8:00から午前10:00までの2時間の休暇を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="219f8-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="219f8-181">休暇の計算と承認</span><span class="sxs-lookup"><span data-stu-id="219f8-181">Calculate and approve absence</span></span>

- <span data-ttu-id="219f8-182">**休暇時間** &gt; **確認および承認** &gt; **承認または計算**を選択します。</span><span class="sxs-lookup"><span data-stu-id="219f8-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>

