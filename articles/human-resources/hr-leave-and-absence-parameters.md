---
title: 休暇パラメーターのコンフィギュレーション
description: Dynamics 365 Human Resources で休暇のための人事管理パラメーターを定義します。
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712379"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="52b5d-103">休暇パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="52b5d-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="52b5d-104">Dynamics 365 Human Resources で休暇計画を設定する前に、下記を含むすべての関連する人事管理パラメーターの設定を確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="52b5d-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="52b5d-105">休暇申請の番号順序</span><span class="sxs-lookup"><span data-stu-id="52b5d-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="52b5d-106">育児介護休業法 (FMLA) 設定</span><span class="sxs-lookup"><span data-stu-id="52b5d-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="52b5d-107">休暇申請のための従業員セルフ サービス設定</span><span class="sxs-lookup"><span data-stu-id="52b5d-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="52b5d-108">休暇および欠勤パラメーター</span><span class="sxs-lookup"><span data-stu-id="52b5d-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="52b5d-109">人事管理パラメーターの表示および変更</span><span class="sxs-lookup"><span data-stu-id="52b5d-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="52b5d-110">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="52b5d-111">**設定**で、**人事管理パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="52b5d-112">**番号順序**タブで、**休暇申請 ID** のための**番号順序コード**を確認し、必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="52b5d-113">この設定により、休暇申請に自動的に ID を割り当てるために使用される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="52b5d-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="52b5d-114">**FMLA** タブで、FMLA の設定を確認し必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="52b5d-115">**従業員セルフ サービス** タブで、マネージャーが従業員に代わって休暇申請を入力できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="52b5d-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="52b5d-117">休暇と欠勤のパラメータの表示および変更</span><span class="sxs-lookup"><span data-stu-id="52b5d-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="52b5d-118">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="52b5d-119">**設定**で、**休暇および欠勤パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="52b5d-120">**一般** タブで、次パラメーターを設定します:</span><span class="sxs-lookup"><span data-stu-id="52b5d-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="52b5d-121">**休暇および欠勤の単位** を時間数または日数に設定します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="52b5d-122">日数の場合、**半日定義を有効にする** を選択して、従業員が休暇申請の 1 日の前半または後半のいずれかを選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="52b5d-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="52b5d-123">**勤続月数の有効日** を選択して、勤続月数を使用して休暇計画の見越計上レートが有効になる時期を設定します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="52b5d-124">**残日数の計算** を選択して、今日の残日数、または見越計上期間の残日数を表示します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="52b5d-125">**今日現在の残日数** を選択すると、残日数には今日時点のすべての見越、調整、および申請の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52b5d-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="52b5d-126">**見越計上期間の時点での残日数** を選択した場合、残日数には、休暇計画の頻度で定義された見越計上期間の時点でのすべての見越、調整、申請の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52b5d-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="52b5d-127">繰り越し有効期限バッチジョブの開始時刻を設定します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="52b5d-128">**はい**を選択すると、**従業員に休暇の購入を許可する** と **従業員の休暇の売却を許可する**ことができます。</span><span class="sxs-lookup"><span data-stu-id="52b5d-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="52b5d-129">これらのオプションに対して **はい** を選択すると、休暇の購入と売却ポリシーの作成と、従業員が休暇の購入と売却の申請を送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="52b5d-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="52b5d-130">カレンダー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="52b5d-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="52b5d-131">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="52b5d-132">**設定**で、**休暇および欠勤パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="52b5d-133">**カレンダー** タブで、カレンダーの設定を必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="52b5d-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52b5d-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="52b5d-135">参照</span><span class="sxs-lookup"><span data-stu-id="52b5d-135">See also</span></span>

- [<span data-ttu-id="52b5d-136">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="52b5d-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
