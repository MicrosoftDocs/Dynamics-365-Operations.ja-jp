---
title: 休暇タイプのコンフィギュレーション
description: Dynamics 365 Human Resources で、従業員が使用できる休暇のタイプを設定します。
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198053"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="8f42f-103">休暇タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8f42f-103">Configure leave and absence types</span></span>

<span data-ttu-id="8f42f-104">Dynamics 365 Human Resources で休暇タイプは、従業員がレポートできる休暇のタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="8f42f-105">休暇タイプは、組織のニーズに応じてカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="8f42f-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="8f42f-106">たとえば次のような休暇タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-106">Examples of leave types include:</span></span>

- <span data-ttu-id="8f42f-107">有給休暇 (PTO)</span><span class="sxs-lookup"><span data-stu-id="8f42f-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="8f42f-108">無給休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-108">Unpaid leave</span></span>
- <span data-ttu-id="8f42f-109">有給休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-109">Paid vacation</span></span>
- <span data-ttu-id="8f42f-110">病気休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-110">Sick leave</span></span>
- <span data-ttu-id="8f42f-111">病気休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-111">Medical leave</span></span>
- <span data-ttu-id="8f42f-112">家族休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-112">Family leave</span></span>
- <span data-ttu-id="8f42f-113">短期障害者</span><span class="sxs-lookup"><span data-stu-id="8f42f-113">Short-term disability</span></span>
- <span data-ttu-id="8f42f-114">忌引き休暇</span><span class="sxs-lookup"><span data-stu-id="8f42f-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="8f42f-115">休暇タイプの追加</span><span class="sxs-lookup"><span data-stu-id="8f42f-115">Add a leave type</span></span>

1. <span data-ttu-id="8f42f-116">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8f42f-117">**設定**で、**休暇および欠勤タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="8f42f-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-118">Select **New**.</span></span>

4. <span data-ttu-id="8f42f-119">**タイプ**に休暇のタイプを入力し、**ワークフロー ID** からワークフローを選択して、**説明**に説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="8f42f-120">**全般**で、**カテゴリ** ドロップダウンから、**なし**、**スケジュール済**、**未スケジュール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="8f42f-121">**所得コード** ドロップダウンから、所得コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="8f42f-122">**理由コードの要否**で、理由コードの要否を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="8f42f-123">理由コードを必要とする場合は、それらを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f42f-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="8f42f-124">**理由コード**で、**追加**を選択し、その横にある**有効**チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="8f42f-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="8f42f-125">**選択したロールにアクセスを制限**で、アクセスを制限するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="8f42f-126">次に、**この休暇タイプに対するセキュリティ ロール**でセキュリティ ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="8f42f-127">セキュリティ ロールは、この手順のはじめで説明した**ワークフロー ID** で選択したワークフローで定義されています。</span><span class="sxs-lookup"><span data-stu-id="8f42f-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="8f42f-128">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="8f42f-129">休暇タイプ ルールの構成</span><span class="sxs-lookup"><span data-stu-id="8f42f-129">Configure leave type rules</span></span>

1. <span data-ttu-id="8f42f-130">休暇タイプの丸めオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="8f42f-131">オプションには、**なし**、**上**、**下**、**四捨五入**があります。</span><span class="sxs-lookup"><span data-stu-id="8f42f-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="8f42f-132">休暇タイプの丸めの精度を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f42f-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="8f42f-133">休暇タイプに**休日の修正**を設定します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="8f42f-134">このオプションを選択すると、Human Resources は作業日に含まれる休日の数を使用して、休暇タイプに対する休暇の見越計上の方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="8f42f-135">たとえば、クリスマスの日が月曜に当たる場合、Human Resources は、見越計上を処理するときに休暇タイプから 1 日を減算します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="8f42f-136">休日は作業時間カレンダーで設定します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="8f42f-137">詳細については、[作業時間カレンダーを作成する](hr-leave-and-absence-working-time-calendar.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="8f42f-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="8f42f-138">プレビューの機能の構成</span><span class="sxs-lookup"><span data-stu-id="8f42f-138">Configure preview features</span></span>

<span data-ttu-id="8f42f-139">休暇および欠勤のプレビュー機能を有効にしている場合は、それらの設定も構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f42f-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="8f42f-140">振り替えるために繰越残日数に対して休暇タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f42f-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="8f42f-141">繰越に新しい休暇タイプを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f42f-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="8f42f-142">参照</span><span class="sxs-lookup"><span data-stu-id="8f42f-142">See also</span></span>

- [<span data-ttu-id="8f42f-143">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="8f42f-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="8f42f-144">休暇および欠勤計画の作成</span><span class="sxs-lookup"><span data-stu-id="8f42f-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="8f42f-145">作業時間カレンダーの作成</span><span class="sxs-lookup"><span data-stu-id="8f42f-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
