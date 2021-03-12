---
title: 休暇の管理
description: この手順では、従業員の休暇レコードの作成について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd49e4c1c5c97094061fa119ac1dda99ef69e5e4
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797992"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="bb2d4-103">休暇の管理</span><span class="sxs-lookup"><span data-stu-id="bb2d4-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb2d4-104">この手順では、従業員の休暇レコードの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="bb2d4-105">教育、医療、育児などの休暇時間の理由を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="bb2d4-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bb2d4-107">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="bb2d4-108">一覧で、従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="bb2d4-109">従業員の名前を選択して詳細情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="bb2d4-110">[雇用] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="bb2d4-111">[休暇] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-111">Click Leave.</span></span>
6. <span data-ttu-id="bb2d4-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-112">Click New.</span></span>
7. <span data-ttu-id="bb2d4-113">[休暇タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bb2d4-114">[休暇タイプ] フォームの所得コードに休暇タイプを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="bb2d4-115">休暇タイプを所得コードに関連付けると、入力した休暇期間の間、関連付けられた所得コードのある所得行が生成されます。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="bb2d4-116">一覧で、休暇タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="bb2d4-117">例: 採用</span><span class="sxs-lookup"><span data-stu-id="bb2d4-117">For example: Adoption</span></span>  
9. <span data-ttu-id="bb2d4-118">休暇が開始する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="bb2d4-119">例: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="bb2d4-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="bb2d4-120">例: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="bb2d4-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="bb2d4-121">休暇が開始する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="bb2d4-122">例: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="bb2d4-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="bb2d4-123">[メモ] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="bb2d4-124">例: 採用のための休暇</span><span class="sxs-lookup"><span data-stu-id="bb2d4-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="bb2d4-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb2d4-125">Click Save.</span></span>

