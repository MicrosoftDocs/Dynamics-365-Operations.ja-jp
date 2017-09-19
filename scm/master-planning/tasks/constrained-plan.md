--- 
title: "制約付き計画の生成"
description: "この手順では、材料制約と能力制約の両方を考慮した計画の作成方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="b69d7-103">制約付き計画の生成</span><span class="sxs-lookup"><span data-stu-id="b69d7-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b69d7-104">この手順では、材料制約と能力制約の両方を考慮した計画の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="b69d7-105">計画により、材料が利用可能でないうちに生産が開始しないように、またリソースが予約超過にならないようにします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="b69d7-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b69d7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b69d7-107">この手順は、生産の計画者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="b69d7-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="b69d7-108">制約付き計画の設定</span><span class="sxs-lookup"><span data-stu-id="b69d7-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="b69d7-109">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-109">Click Master planning.</span></span>
2. <span data-ttu-id="b69d7-110">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-110">Click Master plans.</span></span>
3. <span data-ttu-id="b69d7-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b69d7-112">例: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="b69d7-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="b69d7-113">[有限能力] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="b69d7-114">[有限能力タイム フェンス] フィールドに「30」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="b69d7-115">[タイム フェンス (日)] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="b69d7-116">[能力] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="b69d7-117">[能力スケジューリング タイム フェンス (日)] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="b69d7-118">例: 60</span><span class="sxs-lookup"><span data-stu-id="b69d7-118">Example: 60</span></span>  
9. <span data-ttu-id="b69d7-119">[計算済遅延] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="b69d7-120">[遅延の計算タイム フェンス (日)] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="b69d7-121">例: 60</span><span class="sxs-lookup"><span data-stu-id="b69d7-121">Example: 60</span></span>  
11. <span data-ttu-id="b69d7-122">[計算済遅延] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="b69d7-123">[計算済遅延を要求日に追加] フィールドで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="b69d7-124">[計算済遅延を要求日に追加] フィールドで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="b69d7-125">[計算済遅延を要求日に追加] フィールドで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="b69d7-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b69d7-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="b69d7-127">制約付き計画の作成</span><span class="sxs-lookup"><span data-stu-id="b69d7-127">Create a constrained plan</span></span>
1. <span data-ttu-id="b69d7-128">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-128">Click Run.</span></span>
2. <span data-ttu-id="b69d7-129">[マスター プラン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="b69d7-130">制約を設定した計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="b69d7-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="b69d7-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-131">Click OK.</span></span>
    * <span data-ttu-id="b69d7-132">しばらく時間がかかる場合があります</span><span class="sxs-lookup"><span data-stu-id="b69d7-132">This may take a while.</span></span>  
4. <span data-ttu-id="b69d7-133">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b69d7-133">Click Planned orders.</span></span>

