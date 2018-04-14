--- 
title: "休暇の管理"
description: "この手順では、従業員の休暇レコードの作成について説明します。"
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ec30fc5e4d3289264da0e40dc981c597c04f4c15
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="3d758-103">休暇の管理</span><span class="sxs-lookup"><span data-stu-id="3d758-103">Manage leave of absence</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d758-104">この手順では、従業員の休暇レコードの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d758-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="3d758-105">教育、医療、育児などの休暇時間の理由を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="3d758-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="3d758-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="3d758-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3d758-107">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d758-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="3d758-108">一覧で、従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d758-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="3d758-109">従業員の名前を選択して詳細情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3d758-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="3d758-110">[雇用] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d758-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="3d758-111">[休暇] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d758-111">Click Leave.</span></span>
6. <span data-ttu-id="3d758-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d758-112">Click New.</span></span>
7. <span data-ttu-id="3d758-113">[休暇タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d758-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3d758-114">[休暇タイプ] フォームの所得コードに休暇タイプを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="3d758-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="3d758-115">休暇タイプを所得コードに関連付けると、入力した休暇期間の間、関連付けられた所得コードのある所得行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="3d758-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="3d758-116">一覧で、休暇タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d758-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="3d758-117">例: 採用</span><span class="sxs-lookup"><span data-stu-id="3d758-117">For example: Adoption</span></span>  
9. <span data-ttu-id="3d758-118">休暇が開始する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d758-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="3d758-119">例: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="3d758-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="3d758-120">例: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="3d758-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="3d758-121">休暇が開始する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d758-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="3d758-122">例: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="3d758-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="3d758-123">[メモ] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d758-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="3d758-124">例: 採用のための休暇</span><span class="sxs-lookup"><span data-stu-id="3d758-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="3d758-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d758-125">Click Save.</span></span>


