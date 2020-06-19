---
title: 休暇ポリシーの売買管理
description: Dynamics 365 Human Resources で従業員が休暇を売買できるようにすることができます。
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429016"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="5a9a6-103">休暇ポリシーの売買管理</span><span class="sxs-lookup"><span data-stu-id="5a9a6-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5a9a6-104">休暇ポリシーの購入を作成することで、従業員が休暇を購入できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="5a9a6-105">従業員が休暇を売買できるようにする</span><span class="sxs-lookup"><span data-stu-id="5a9a6-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="5a9a6-106">**休暇および欠勤パラメーター** ページで、**従業員が休暇を購入できるようにする** に対して **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="5a9a6-107">休暇ポリシーの購入を作成する</span><span class="sxs-lookup"><span data-stu-id="5a9a6-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="5a9a6-108">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="5a9a6-109">**休暇ポリシーの売買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="5a9a6-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-110">Select **New**.</span></span>

4. <span data-ttu-id="5a9a6-111">**休暇ポリシーの売買** で ポリシーの **名前** と **説明** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="5a9a6-112">**ポリシー タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="5a9a6-113">利用可能なポリシー タイプは、**金額** と **週あたりの時間数** です。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="5a9a6-114">**金額** を選択して、従業員が売買できる上限金額の **固定金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="5a9a6-115">**週あたりの時間数** を選択した場合は、従業員に割り当てられた作業時間カレンダーで定義されている作業時間が、ポリシーの上限金額を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="5a9a6-116">ポリシーに対して **開始日** と **終了日** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="5a9a6-117">休暇の売買申請は、この時間枠でのみ提出することができます。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="5a9a6-118">**ポリシーの購入** で、**フルタイム相当** (FTE) を選択すると、従業員の職位で定義された FTE に基づいて上限金額を比例配分します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="5a9a6-119">ポリシー タイプが **金額** の場合は、**上限固定金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="5a9a6-120">**追加** を選択して、休暇を購入する従業員の休暇タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="5a9a6-121">ポリシーには複数の休暇タイプを追加できます。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="5a9a6-122">休暇タイプに **勤続月数**を入力して、異なる勤続月数で従業員が購入できる上限金額を決定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="5a9a6-123">休暇タイプに **上限金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="5a9a6-124">従業員が休暇を購入する **レート** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="5a9a6-125">必要に応じて、休暇を購入するために使用する **所得コード** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="5a9a6-126">必要に応じて、休暇タイプの上限金額を決定するために FTE を使用するかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="5a9a6-127">休暇および不就業プランに対する、休暇ポリシーの売買を追加する</span><span class="sxs-lookup"><span data-stu-id="5a9a6-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="5a9a6-128">**休暇** ページで、休暇および不就業プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="5a9a6-129">**ルール** で **休暇ポリシーの売買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a9a6-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a9a6-130">参照</span><span class="sxs-lookup"><span data-stu-id="5a9a6-130">See also</span></span>

[<span data-ttu-id="5a9a6-131">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="5a9a6-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="5a9a6-132">休暇および欠勤タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5a9a6-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="5a9a6-133">休暇計画の累計</span><span class="sxs-lookup"><span data-stu-id="5a9a6-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="5a9a6-134">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="5a9a6-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

