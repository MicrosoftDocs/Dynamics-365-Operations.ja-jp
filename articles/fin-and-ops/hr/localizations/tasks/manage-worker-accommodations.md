--- 
title: "作業者の特別設備の管理"
description: "この手順では、人間工学に基づいた椅子または定期的な休暇などの作業環境の特別設備タイプを設定するための手順を説明します。"
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="e252e-103">作業者の特別設備の管理</span><span class="sxs-lookup"><span data-stu-id="e252e-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="e252e-104">この手順では、人間工学に基づいた椅子または定期的な休暇などの作業環境の特別設備タイプを設定するための手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="e252e-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="e252e-105">また、作業者にこれらの特別設備タイプを割り当てる方法、および特別設備 タイプの承認または拒否方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e252e-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="e252e-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="e252e-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="e252e-107">特別設備の設定</span><span class="sxs-lookup"><span data-stu-id="e252e-107">Setup accommodations</span></span>
1. <span data-ttu-id="e252e-108">[人事管理] > [設定] > [特別設備 タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e252e-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="e252e-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-109">Click New.</span></span>
3. <span data-ttu-id="e252e-110">[特別設備 タイプ] フィールドに、特別設備の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="e252e-111">例: キーボード。</span><span class="sxs-lookup"><span data-stu-id="e252e-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="e252e-112">[説明] フィールドに、特別設備の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="e252e-113">例: 人間工学に基づいたキーボード。</span><span class="sxs-lookup"><span data-stu-id="e252e-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="e252e-114">[メモ] フィールドで、特別設備を明確にするのに役立つ情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="e252e-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-115">Click Save.</span></span>
7. <span data-ttu-id="e252e-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e252e-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="e252e-117">特別設備の割り当て</span><span class="sxs-lookup"><span data-stu-id="e252e-117">Assign accommodations</span></span>
1. <span data-ttu-id="e252e-118">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e252e-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="e252e-119">リストから、従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="e252e-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="e252e-120">特別設備を要求している従業員に関する詳細を表示するには、従業員の名前をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="e252e-121">[個人情報] クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="e252e-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="e252e-122">[特別設備] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-122">Click Accommodations.</span></span>
6. <span data-ttu-id="e252e-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-123">Click New.</span></span>
7. <span data-ttu-id="e252e-124">[特別設備 タイプ] フィールドで、適切な特別設備を選択します。</span><span class="sxs-lookup"><span data-stu-id="e252e-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="e252e-125">例: キーボード</span><span class="sxs-lookup"><span data-stu-id="e252e-125">Example: Keyboard</span></span>
8. <span data-ttu-id="e252e-126">[職務] フィールドに特別設備を要求する作業タスクを入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="e252e-127">[ステータス] フィールドに適切なステータスを入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="e252e-128">例: 適当</span><span class="sxs-lookup"><span data-stu-id="e252e-128">Example: Reasonable</span></span>
    * <span data-ttu-id="e252e-129">次のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="e252e-129">The following statuses are available.</span></span> <span data-ttu-id="e252e-130">要求済は、特別設備が作成されているが校閲されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e252e-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="e252e-131">適当は、特別設備が妥当で許可されることを示します。</span><span class="sxs-lookup"><span data-stu-id="e252e-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="e252e-132">不適当な状態は、特別設備が雇用主に不適当な負担をかける可能性があり、拒否されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="e252e-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="e252e-133">この例では、特別設備要求が最小であったため、要求はすぐに承認されました。</span><span class="sxs-lookup"><span data-stu-id="e252e-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="e252e-134">[受入済] フィールドで、特別設備要求を受け入れた従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="e252e-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="e252e-135">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-135">Click Select.</span></span>
12. <span data-ttu-id="e252e-136">[受入日] フィールドに、特別設備要求が承受け入れられた日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="e252e-137">[メモ] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e252e-137">Expand the Note section.</span></span>
14. <span data-ttu-id="e252e-138">[財務] のフィールドに、特別設備の影響を明確にするのに役立つ情報またはリソース コストを入力します。</span><span class="sxs-lookup"><span data-stu-id="e252e-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="e252e-139">特別設備が拒否されている場合、[返信] フィールドは要求が拒否された理由を示すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e252e-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="e252e-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e252e-140">Click Save.</span></span>


