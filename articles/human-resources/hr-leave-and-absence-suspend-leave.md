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
ms.search.form: SuspendLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ebee395ae4083bb489b1fd77174ae3dc82428a2d
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198077"
---
# <a name="suspend-leave"></a><span data-ttu-id="eb79b-103">休暇の中断</span><span class="sxs-lookup"><span data-stu-id="eb79b-103">Suspend leave</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="eb79b-104">従業員の休暇を一時停止して、選択した休暇タイプに対して休暇の見越計上処理を停止できます。</span><span class="sxs-lookup"><span data-stu-id="eb79b-104">You can suspend leave for an employee to stop leave accruals from being processed for selected leave types.</span></span> 

## <a name="suspend-leave-and-absence-for-an-employee"></a><span data-ttu-id="eb79b-105">従業員の休暇および欠勤を中断する</span><span class="sxs-lookup"><span data-stu-id="eb79b-105">Suspend leave and absence for an employee</span></span>

1. <span data-ttu-id="eb79b-106">従業員のレコードで、**休暇**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb79b-106">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="eb79b-107">**休暇の中断** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb79b-107">Select **Suspend leave**.</span></span>

3. <span data-ttu-id="eb79b-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb79b-108">Select **New**.</span></span>

4. <span data-ttu-id="eb79b-109">**休暇の見越計上の中断** ダイアログ ボックスで、中断の **開始日** および **終了日** と共に **休暇タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb79b-109">In the **Suspend leave accrual** dialog box, select the **Leave type** along with the **Start date** and **End date** for the suspension.</span></span>

5. <span data-ttu-id="eb79b-110">必要に応じて、中断の **コメント** を追加できます。</span><span class="sxs-lookup"><span data-stu-id="eb79b-110">Optionally, you can add a **Comment** for the suspension.</span></span> 

<span data-ttu-id="eb79b-111">従業員の休暇が中断されている間に見越計上が処理された場合、中断された休暇タイプの見越計上は行われません。</span><span class="sxs-lookup"><span data-stu-id="eb79b-111">If accruals are processed while the employee's leave is suspended, no accrual will be made for the suspended leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb79b-112">参照</span><span class="sxs-lookup"><span data-stu-id="eb79b-112">See also</span></span>

- [<span data-ttu-id="eb79b-113">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="eb79b-113">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="eb79b-114">休暇および欠勤タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="eb79b-114">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
- [<span data-ttu-id="eb79b-115">休暇計画の累計</span><span class="sxs-lookup"><span data-stu-id="eb79b-115">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)
