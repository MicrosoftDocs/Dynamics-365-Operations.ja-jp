---
title: 休暇の中断
description: Dynamics 365 Human Resources の従業員の休暇を一時停止できます。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ed663a8b602e1d3f43a429ba18f515dc84d6d3e3
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428573"
---
# <a name="suspend-leave"></a><span data-ttu-id="ed332-103">休暇の中断</span><span class="sxs-lookup"><span data-stu-id="ed332-103">Suspend leave</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ed332-104">従業員の休暇を一時停止して、選択した休暇タイプに対して休暇の見越計上処理を停止できます。</span><span class="sxs-lookup"><span data-stu-id="ed332-104">You can suspend leave for an employee to stop leave accruals from being processed for selected leave types.</span></span> 

## <a name="suspend-leave-and-absence-for-an-employee"></a><span data-ttu-id="ed332-105">従業員の休暇および欠勤を中断する</span><span class="sxs-lookup"><span data-stu-id="ed332-105">Suspend leave and absence for an employee</span></span>

1. <span data-ttu-id="ed332-106">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed332-106">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="ed332-107">**休暇の中断** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed332-107">Select **Suspend leave**.</span></span>

3. <span data-ttu-id="ed332-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed332-108">Select **New**.</span></span>

4. <span data-ttu-id="ed332-109">**休暇の見越計上の中断** ダイアログ ボックスで、中断の **開始日** および **終了日** と共に **休暇タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed332-109">In the **Suspend leave accrual** dialog box, select the **Leave type** along with the **Start date** and **End date** for the suspension.</span></span>

5. <span data-ttu-id="ed332-110">必要に応じて、中断の **コメント** を追加できます。</span><span class="sxs-lookup"><span data-stu-id="ed332-110">Optionally, you can add a **Comment** for the suspension.</span></span> 

<span data-ttu-id="ed332-111">従業員の休暇が中断されている間に見越計上が処理された場合、中断された休暇タイプの見越計上は行われません。</span><span class="sxs-lookup"><span data-stu-id="ed332-111">If accruals are processed while the employee's leave is suspended, no accrual will be made for the suspended leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed332-112">参照</span><span class="sxs-lookup"><span data-stu-id="ed332-112">See also</span></span>

- [<span data-ttu-id="ed332-113">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="ed332-113">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="ed332-114">休暇および欠勤タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ed332-114">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
- [<span data-ttu-id="ed332-115">休暇計画の累計</span><span class="sxs-lookup"><span data-stu-id="ed332-115">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)

