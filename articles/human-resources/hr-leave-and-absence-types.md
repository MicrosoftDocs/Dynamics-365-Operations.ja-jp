---
title: 休暇タイプのコンフィギュレーション
description: Dynamics 365 Human Resources で、従業員が使用できる休暇のタイプを設定します。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115079"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="266a0-103">休暇タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="266a0-103">Configure leave and absence types</span></span>

<span data-ttu-id="266a0-104">Dynamics 365 Human Resources で休暇タイプは、従業員がレポートできる休暇のタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="266a0-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="266a0-105">休暇タイプは、組織のニーズに応じてカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="266a0-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="266a0-106">たとえば次のような休暇タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="266a0-106">Examples of leave types include:</span></span>

- <span data-ttu-id="266a0-107">有給休暇 (PTO)</span><span class="sxs-lookup"><span data-stu-id="266a0-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="266a0-108">無給休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-108">Unpaid leave</span></span>
- <span data-ttu-id="266a0-109">有給休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-109">Paid vacation</span></span>
- <span data-ttu-id="266a0-110">病気休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-110">Sick leave</span></span>
- <span data-ttu-id="266a0-111">病気休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-111">Medical leave</span></span>
- <span data-ttu-id="266a0-112">家族休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-112">Family leave</span></span>
- <span data-ttu-id="266a0-113">短期障碍者</span><span class="sxs-lookup"><span data-stu-id="266a0-113">Short-term disability</span></span>
- <span data-ttu-id="266a0-114">忌引き休暇</span><span class="sxs-lookup"><span data-stu-id="266a0-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="266a0-115">休暇タイプの追加</span><span class="sxs-lookup"><span data-stu-id="266a0-115">Add a leave type</span></span>

1. <span data-ttu-id="266a0-116">**休暇および欠勤** のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="266a0-117">**設定** で、**休暇および欠勤タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="266a0-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-118">Select **New**.</span></span>

4. <span data-ttu-id="266a0-119">**タイプ** に休暇のタイプを入力し、**ワークフロー ID** からワークフローを選択して、**説明** に説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="266a0-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="266a0-120">**全般** で、**カテゴリ** ドロップダウンから、**なし**、**スケジュール済**、**未スケジュール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="266a0-121">**所得コード** ドロップダウンから、所得コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="266a0-122">**理由コードの要否** で、理由コードの要否を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="266a0-123">理由コードを必要とする場合は、それらを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266a0-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="266a0-124">**理由コード** で、**追加** を選択し、その横にある **有効** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="266a0-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="266a0-125">**選択したロールにアクセスを制限** で、アクセスを制限するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="266a0-126">次に、**この休暇タイプに対するセキュリティ ロール** でセキュリティ ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="266a0-127">セキュリティ ロールは、この手順のはじめで説明した **ワークフロー ID** で選択したワークフローで定義されています。</span><span class="sxs-lookup"><span data-stu-id="266a0-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="266a0-128">**カレンダーの色** で、この休暇タイプの休暇と欠勤カレンダーに表示する色を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="266a0-129">**保留関係** で、この休暇タイプで別の休暇タイプを保留にするか、別の休暇タイプで保留にするかを選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="266a0-130">保留中の休暇タイプで休暇申請を行うと、保留済み休暇タイプに対して休暇の停止が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="266a0-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="266a0-131">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="266a0-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="266a0-132">休暇タイプ ルールの構成</span><span class="sxs-lookup"><span data-stu-id="266a0-132">Configure leave type rules</span></span>

1. <span data-ttu-id="266a0-133">休暇タイプの丸めオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="266a0-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="266a0-134">オプションには、**なし**、**上**、**下**、**四捨五入** があります。</span><span class="sxs-lookup"><span data-stu-id="266a0-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="266a0-135">休暇タイプの丸めの精度を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="266a0-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="266a0-136">休暇タイプに **休日の修正** を設定します。</span><span class="sxs-lookup"><span data-stu-id="266a0-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="266a0-137">このオプションを選択すると、Human Resources は作業日に含まれる休日の数を使用して、休暇タイプに対する休暇の見越計上の方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="266a0-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="266a0-138">たとえば、クリスマスの日が月曜に当たる場合、Human Resources は、見越計上を処理するときに休暇タイプから 1 日を減算します。</span><span class="sxs-lookup"><span data-stu-id="266a0-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="266a0-139">休日は作業時間カレンダーで設定します。</span><span class="sxs-lookup"><span data-stu-id="266a0-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="266a0-140">詳細については、[作業時間カレンダーを作成する](hr-leave-and-absence-working-time-calendar.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="266a0-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="266a0-141">休暇タイプに **繰越休暇タイプ** を設定します。</span><span class="sxs-lookup"><span data-stu-id="266a0-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="266a0-142">このオプションを選択すると、繰越残日数は指定された休暇タイプに転送されます。</span><span class="sxs-lookup"><span data-stu-id="266a0-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="266a0-143">繰越休暇タイプも、休暇および不就業プランに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="266a0-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="266a0-144">休暇タイプの **有効期限ルール** を定義します。</span><span class="sxs-lookup"><span data-stu-id="266a0-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="266a0-145">このオプションを設定すると、日数または月数の単位を選択して、有効期限の期間を設定できます。</span><span class="sxs-lookup"><span data-stu-id="266a0-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="266a0-146">有効期限ルールの有効日を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="266a0-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="266a0-147">有効期限の時点で存在する休暇残高は、休暇タイプから差し引かれ、休暇残高に反映されます。</span><span class="sxs-lookup"><span data-stu-id="266a0-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="266a0-148">参照</span><span class="sxs-lookup"><span data-stu-id="266a0-148">See also</span></span>

- [<span data-ttu-id="266a0-149">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="266a0-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="266a0-150">休暇および欠勤計画の作成</span><span class="sxs-lookup"><span data-stu-id="266a0-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="266a0-151">作業時間カレンダーの作成</span><span class="sxs-lookup"><span data-stu-id="266a0-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="266a0-152">休暇の中断</span><span class="sxs-lookup"><span data-stu-id="266a0-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

