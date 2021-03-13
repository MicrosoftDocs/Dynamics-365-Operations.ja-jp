---
title: 休暇ポリシーの売買管理
description: Dynamics 365 Human Resources で従業員が休暇を売買できるようにすることができます。
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115999"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="72b8c-103">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="72b8c-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="72b8c-104">休暇の売買ポリシーを作成することで、従業員が休暇の購入や売却ができるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="72b8c-105">これらのポリシーを構成して、承認にワークフローを使用したり、最大金額とレートを設定したり、購買と販売のレートを設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="72b8c-106">従業員が休暇を売買できるようにする</span><span class="sxs-lookup"><span data-stu-id="72b8c-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="72b8c-107">**休暇および欠勤パラメーター** ページで、**従業員の休暇の購入を許可する** と **従業員の休暇の売却を許可する** に対して **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="72b8c-108">休暇の売買ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="72b8c-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="72b8c-109">**休暇および欠勤** のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="72b8c-110">**休暇ポリシーの売買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="72b8c-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-111">Select **New**.</span></span>

4. <span data-ttu-id="72b8c-112">**休暇ポリシーの売買** で ポリシーの **名前** と **説明** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="72b8c-113">**ポリシー タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="72b8c-114">利用可能なポリシー タイプは、**金額** と **週あたりの時間数** です。</span><span class="sxs-lookup"><span data-stu-id="72b8c-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="72b8c-115">**金額** を選択して、従業員が売買できる上限金額の **固定金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="72b8c-116">**週あたりの時間数** を選択した場合は、従業員に割り当てられた作業時間カレンダーで定義されている作業時間が、ポリシーの上限金額を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="72b8c-117">ポリシーに対して **開始日** と **終了日** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="72b8c-118">休暇の売買申請は、この時間枠でのみ提出することができます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="72b8c-119">ポリシーで使用する **ワークフロー ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="72b8c-120">すべての売買の申請では、このワークフローを使用してレビューと承認が行われます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="72b8c-121">**ポリシーの購入** で、**フルタイム相当** (FTE) を選択すると、従業員の職位で定義された FTE に基づいて上限金額を比例配分します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="72b8c-122">ポリシー タイプが **金額** の場合は、**上限固定金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="72b8c-123">**追加** を選択して、休暇を購入する従業員の休暇タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="72b8c-124">ポリシーには複数の休暇タイプを追加できます。</span><span class="sxs-lookup"><span data-stu-id="72b8c-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="72b8c-125">休暇タイプに **勤続月数** を入力して、異なる勤続月数で従業員が購入できる上限金額を決定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="72b8c-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="72b8c-126">休暇タイプに **上限金額** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="72b8c-127">従業員が休暇を購入する **レート** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="72b8c-128">必要に応じて、休暇を購入するために使用する **所得コード** を入力します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="72b8c-129">必要に応じて、休暇タイプの上限金額を決定するために FTE を使用するかどうかを設定します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="72b8c-130">売却ポリシーを作成するには、**売却ポリシー** に記載の手順8 から 14 を実行してください。</span><span class="sxs-lookup"><span data-stu-id="72b8c-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="72b8c-131">休暇および不就業プランに対する、休暇ポリシーの売買を追加する</span><span class="sxs-lookup"><span data-stu-id="72b8c-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="72b8c-132">**休暇** ページで、休暇および不就業プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="72b8c-133">**ルール** で **休暇ポリシーの売買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72b8c-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="72b8c-134">参照</span><span class="sxs-lookup"><span data-stu-id="72b8c-134">See also</span></span>

[<span data-ttu-id="72b8c-135">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="72b8c-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="72b8c-136">休暇および欠勤タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72b8c-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="72b8c-137">休暇計画の累計</span><span class="sxs-lookup"><span data-stu-id="72b8c-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="72b8c-138">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="72b8c-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

