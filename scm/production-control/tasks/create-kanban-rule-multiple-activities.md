--- 
title: "複数の活動のかんばんルールの作成"
description: "この手順では、生産フローの複数の活動を含むかんばんルールを作成する方法を示します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d6d0c50da3124553124b65f6ba0e1c5ed35e8613
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="7ca69-103">複数の活動のかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="7ca69-103">Create a kanban rule for multiple activities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ca69-104">この手順では、生産フローの複数の活動を含むかんばんルールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="7ca69-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="7ca69-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7ca69-106">このタスクは、リーン環境で新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="7ca69-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="7ca69-107">新しいかんばんルールの作成</span><span class="sxs-lookup"><span data-stu-id="7ca69-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="7ca69-108">[製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7ca69-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-109">Click New.</span></span>
3. <span data-ttu-id="7ca69-110">[補充方法] フィールドで、「スケジュール済」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="7ca69-111">[最初の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca69-112">SpeakerAssemblyAndPolish を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="7ca69-113">[複数の活動] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="7ca69-114">目的はかんばんルールに複数の活動を含むことです。</span><span class="sxs-lookup"><span data-stu-id="7ca69-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="7ca69-115">最後の計画の活動を選択すると、生産フローのパスを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="7ca69-116">[最後の計画活動] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca69-117">「SpeakerTestAndPackaging」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="7ca69-118">値を選択した後、ページが自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="7ca69-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="7ca69-119">かんばんフローの SpeakerAssemblyAndPolish > SpeakerTestAndPackaging を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="7ca69-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-120">Click OK.</span></span>  
7. <span data-ttu-id="7ca69-121">[詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-121">Expand the Details section.</span></span>
8. <span data-ttu-id="7ca69-122">[製品] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca69-123">品目 L0006 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="7ca69-124">かんばんの作成およびジョブの表示</span><span class="sxs-lookup"><span data-stu-id="7ca69-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="7ca69-125">[かんばん] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="7ca69-126">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-126">Click Add.</span></span>
3. <span data-ttu-id="7ca69-127">[新しいかんばんの数] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="7ca69-128">これで 1 つのかんばんが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7ca69-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="7ca69-129">製品数量を「3」と設定します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="7ca69-130">かんばんは 3 つの製品を処理します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="7ca69-131">[期限日時] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ca69-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="7ca69-132">[今日] を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7ca69-132">You can enter Today.</span></span>  
6. <span data-ttu-id="7ca69-133">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-133">Click Create.</span></span>
7. <span data-ttu-id="7ca69-134">[詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7ca69-134">Click Details.</span></span>
    * <span data-ttu-id="7ca69-135">かんばんには生産フローの 2 つのプロセス ジョブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ca69-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="7ca69-136">1 番目は SpeakerAssemblyAndPolish で、2 番目は SpeakerTestAndPackaging です。</span><span class="sxs-lookup"><span data-stu-id="7ca69-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="7ca69-137">これは最後のステップです!</span><span class="sxs-lookup"><span data-stu-id="7ca69-137">This is the last step!</span></span>  

