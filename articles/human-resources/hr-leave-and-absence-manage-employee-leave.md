---
title: 従業員の休暇の管理
description: Dynamics 365 Human Resources で従業員の休暇を管理する。
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42d51ffe14442e076bafc99035dbd68a555e5b92
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468062"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="04c6e-103">従業員の休暇の管理</span><span class="sxs-lookup"><span data-stu-id="04c6e-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="04c6e-104">従業員の休暇は、休暇タイプで管理できます。</span><span class="sxs-lookup"><span data-stu-id="04c6e-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="04c6e-105">ここには、期限切れの休暇登録と休暇タイプの残高調整が含まれています。</span><span class="sxs-lookup"><span data-stu-id="04c6e-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="04c6e-106">休暇残高の調整</span><span class="sxs-lookup"><span data-stu-id="04c6e-106">Adjust leave balances</span></span>

1. <span data-ttu-id="04c6e-107">従業員のレコードで、**休暇** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="04c6e-108">**休暇と欠勤の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="04c6e-109">**残高の調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="04c6e-110">**休暇タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="04c6e-111">**調整する量** を入力します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="04c6e-112">必要に応じて **日** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="04c6e-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="04c6e-113">従業員の休暇残高を調整する際には、理由コードとコメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="04c6e-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="04c6e-114">休暇残高に関する他の情報は、プレビューで表示します。</span><span class="sxs-lookup"><span data-stu-id="04c6e-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="04c6e-115">**サンドボックス** 環境で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="04c6e-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="04c6e-116">プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04c6e-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="04c6e-117">休暇残高の上にポインターを移動すると、次が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04c6e-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="04c6e-118">**可能な休暇残高**: 今年度の合計 - 今年取得した休暇</span><span class="sxs-lookup"><span data-stu-id="04c6e-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="04c6e-119">**今年度の合計**: 年度のすべての見越計上、調整、および繰り越し</span><span class="sxs-lookup"><span data-stu-id="04c6e-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="04c6e-120">**今年取得した休暇**: すべての承認済休暇</span><span class="sxs-lookup"><span data-stu-id="04c6e-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="04c6e-121">参照</span><span class="sxs-lookup"><span data-stu-id="04c6e-121">See also</span></span>

- [<span data-ttu-id="04c6e-122">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="04c6e-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="04c6e-123">休暇および欠勤要求の管理</span><span class="sxs-lookup"><span data-stu-id="04c6e-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]