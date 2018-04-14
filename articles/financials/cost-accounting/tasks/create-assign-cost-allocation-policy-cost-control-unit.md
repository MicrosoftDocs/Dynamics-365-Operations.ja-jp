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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ff9b4ddeecfdb795c1eead0e9e2100c307f63db4
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="bb001-103">原価配賦ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="bb001-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb001-104">原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="bb001-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="bb001-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bb001-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="bb001-106">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="bb001-106">Create a policy</span></span>
1. <span data-ttu-id="bb001-107">[原価会計] > [ポリシー] > [原価配賦ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="bb001-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="bb001-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-108">Click New.</span></span>
3. <span data-ttu-id="bb001-109">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb001-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="bb001-110">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="bb001-111">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-111">Select Organization.</span></span>  
5. <span data-ttu-id="bb001-112">[統計分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="bb001-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="bb001-114">配賦ルールの作成</span><span class="sxs-lookup"><span data-stu-id="bb001-114">Create allocation rules</span></span>
1. <span data-ttu-id="bb001-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-115">Click New.</span></span>
2. <span data-ttu-id="bb001-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb001-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bb001-117">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="bb001-118">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="bb001-119">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="bb001-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-120">Click New.</span></span>
7. <span data-ttu-id="bb001-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb001-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bb001-122">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="bb001-123">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="bb001-124">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="bb001-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-125">Click New.</span></span>
12. <span data-ttu-id="bb001-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb001-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bb001-127">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="bb001-128">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="bb001-129">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="bb001-130">すべてのルールを作成するまで、続行します。</span><span class="sxs-lookup"><span data-stu-id="bb001-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="bb001-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="bb001-132">原価管理単位へポリシーを割り当て</span><span class="sxs-lookup"><span data-stu-id="bb001-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="bb001-133">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="bb001-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-134">Click New.</span></span>
3. <span data-ttu-id="bb001-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="bb001-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="bb001-136">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb001-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="bb001-137">ルールの日付は有効です。</span><span class="sxs-lookup"><span data-stu-id="bb001-137">The rules are date-effective.</span></span> <span data-ttu-id="bb001-138">新しいバージョンが作成された場合、ユーザーまたはシステムは、そのルールの期限を切ることが可能です。</span><span class="sxs-lookup"><span data-stu-id="bb001-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="bb001-139">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb001-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="bb001-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb001-140">Click Save.</span></span>


