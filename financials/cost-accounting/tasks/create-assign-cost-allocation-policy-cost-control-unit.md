--- 
title: "原価配賦ポリシーの作成と原価管理単位への割り当て"
description: "原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="cefcb-103">原価配賦ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="cefcb-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cefcb-104">原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="cefcb-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="cefcb-106">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="cefcb-106">Create a policy</span></span>
1. <span data-ttu-id="cefcb-107">[原価会計] > [ポリシー] > [原価配賦ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="cefcb-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-108">Click New.</span></span>
3. <span data-ttu-id="cefcb-109">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="cefcb-110">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cefcb-111">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-111">Select Organization.</span></span>  
5. <span data-ttu-id="cefcb-112">[統計分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="cefcb-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="cefcb-114">配賦ルールの作成</span><span class="sxs-lookup"><span data-stu-id="cefcb-114">Create allocation rules</span></span>
1. <span data-ttu-id="cefcb-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-115">Click New.</span></span>
2. <span data-ttu-id="cefcb-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cefcb-117">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="cefcb-118">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="cefcb-119">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="cefcb-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-120">Click New.</span></span>
7. <span data-ttu-id="cefcb-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="cefcb-122">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="cefcb-123">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="cefcb-124">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="cefcb-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-125">Click New.</span></span>
12. <span data-ttu-id="cefcb-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="cefcb-127">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="cefcb-128">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="cefcb-129">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="cefcb-130">すべてのルールを作成するまで、続行します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="cefcb-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="cefcb-132">原価管理単位へポリシーを割り当て</span><span class="sxs-lookup"><span data-stu-id="cefcb-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="cefcb-133">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="cefcb-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-134">Click New.</span></span>
3. <span data-ttu-id="cefcb-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cefcb-136">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="cefcb-137">ルールの日付は有効です。</span><span class="sxs-lookup"><span data-stu-id="cefcb-137">The rules are date-effective.</span></span> <span data-ttu-id="cefcb-138">新しいバージョンが作成された場合、ユーザーまたはシステムは、そのルールの期限を切ることが可能です。</span><span class="sxs-lookup"><span data-stu-id="cefcb-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="cefcb-139">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cefcb-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="cefcb-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cefcb-140">Click Save.</span></span>


