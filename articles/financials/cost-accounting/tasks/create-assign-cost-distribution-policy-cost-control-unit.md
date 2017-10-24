--- 
title: "原価配分ポリシーの作成と原価管理単位への割り当て"
description: "[原価配分ルール] は、集団コスト センターごとに集計される原価を配分するために使用されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbd44816fc2f2569dd477fc21f59418a575bb835
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="fb0d0-103">原価配分ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="fb0d0-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb0d0-104">[原価配分ルール] は、集団コスト センターごとに集計される原価を配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="fb0d0-105">コスト経理担当は、原価が配賦基準に基づいて、コスト センターに配分されるか確認します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="fb0d0-106">ポリシーと対応ルールは、原価管理単位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="fb0d0-107">このタスク ガイドでは、原価配分ポリシーと対応ルールを作成する方法を示す例を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="fb0d0-108">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="fb0d0-108">Create a policy</span></span>
1. <span data-ttu-id="fb0d0-109">[原価会計] > [ポリシー] > [原価配布ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="fb0d0-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-110">Click New.</span></span>
3. <span data-ttu-id="fb0d0-111">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="fb0d0-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fb0d0-113">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-114">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-114">Select Organization.</span></span>  
6. <span data-ttu-id="fb0d0-115">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-116">[CDS P/L] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="fb0d0-117">[統計分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-118">[統計要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="fb0d0-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="fb0d0-120">ポリシーのルールを作成</span><span class="sxs-lookup"><span data-stu-id="fb0d0-120">Create rules for the policy</span></span>
1. <span data-ttu-id="fb0d0-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-121">Click New.</span></span>
2. <span data-ttu-id="fb0d0-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="fb0d0-123">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-124">階層を展開し、094 を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="fb0d0-125">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-126">[その他の営業経費] を選択し、[605110 クリーニング] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="fb0d0-127">[原価動作] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="fb0d0-128">[固定値] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="fb0d0-129">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="fb0d0-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-130">Click New.</span></span>
8. <span data-ttu-id="fb0d0-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fb0d0-132">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-133">階層を展開し、094 を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="fb0d0-134">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fb0d0-135">[その他の営業経費] を選択し、[605150 賃貸] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="fb0d0-136">[原価動作] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="fb0d0-137">[固定値] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="fb0d0-138">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="fb0d0-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="fb0d0-140">原価管理単位へルールを割り当て</span><span class="sxs-lookup"><span data-stu-id="fb0d0-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="fb0d0-141">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="fb0d0-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-142">Click New.</span></span>
3. <span data-ttu-id="fb0d0-143">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="fb0d0-144">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="fb0d0-145">有効な会計年度で、[9 月 1 日] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="fb0d0-146">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="fb0d0-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb0d0-147">Click Save.</span></span>


