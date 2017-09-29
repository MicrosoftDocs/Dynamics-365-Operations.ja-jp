--- 
title: "原価動作ポリシーの作成と原価管理単位への割り当て"
description: "原価の動作は、固定費または変動費の分類です。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 392cb83ceb8612a2e73cc54bb2d8d40c62a6b7b6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="beffc-103">原価動作ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="beffc-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="beffc-104">原価の動作は、固定費または変動費の分類です。</span><span class="sxs-lookup"><span data-stu-id="beffc-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="beffc-105">ポリシーと対応ルールは、有効になるポリシーの原価管理単位へ割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="beffc-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="beffc-106">ポリシーを作成し、原価管理単位へ割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="beffc-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="beffc-107">原価動作階層を作成</span><span class="sxs-lookup"><span data-stu-id="beffc-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="beffc-108">[原価会計] > [分析コード] > [分析コード階層] に移動します。</span><span class="sxs-lookup"><span data-stu-id="beffc-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="beffc-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-109">Click New.</span></span>
3. <span data-ttu-id="beffc-110">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-110">Click Create.</span></span>
4. <span data-ttu-id="beffc-111">[分析コード階層名] フィールドでは、「原価動作階層」を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="beffc-112">[分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-113">[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="beffc-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-114">Click Save.</span></span>
7. <span data-ttu-id="beffc-115">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="beffc-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-116">Click New.</span></span>
9. <span data-ttu-id="beffc-117">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="beffc-118">[固定費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="beffc-119">ツリーで、「原価動作階層」を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="beffc-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-120">Click New.</span></span>
12. <span data-ttu-id="beffc-121">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="beffc-122">[変動費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="beffc-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-123">Click Save.</span></span>
14. <span data-ttu-id="beffc-124">ツリーで、「原価動作階層\固定費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="beffc-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-125">Click New.</span></span>
16. <span data-ttu-id="beffc-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="beffc-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="beffc-127">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-128">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="beffc-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="beffc-129">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-130">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="beffc-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="beffc-131">ツリーで、「原価動作階層\変動費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="beffc-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-132">Click New.</span></span>
21. <span data-ttu-id="beffc-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="beffc-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="beffc-134">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-135">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="beffc-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="beffc-136">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-137">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="beffc-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="beffc-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="beffc-139">ポリシーとルールを作成</span><span class="sxs-lookup"><span data-stu-id="beffc-139">Create the policy and rules</span></span>
1. <span data-ttu-id="beffc-140">[原価会計] > [ポリシー] > [原価動作ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="beffc-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="beffc-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-141">Click New.</span></span>
3. <span data-ttu-id="beffc-142">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="beffc-143">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-144">作成したポリシーの階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="beffc-145">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-146">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-146">Select Organization.</span></span>  
6. <span data-ttu-id="beffc-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-147">Click Save.</span></span>
7. <span data-ttu-id="beffc-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-148">Click New.</span></span>
8. <span data-ttu-id="beffc-149">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="beffc-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="beffc-150">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-151">階層を展開し、[変動費] を選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="beffc-152">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="beffc-153">既定では、変動率は 100 パーセントです。</span><span class="sxs-lookup"><span data-stu-id="beffc-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="beffc-154">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="beffc-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-155">Click New.</span></span>
13. <span data-ttu-id="beffc-156">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="beffc-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="beffc-157">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beffc-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="beffc-158">ルールには有効期限がありますが、もし新しいバージョンが作成された場合、ユーザーまたはシステムがルールを失効させることが出来ます。</span><span class="sxs-lookup"><span data-stu-id="beffc-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="beffc-159">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="beffc-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="beffc-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="beffc-160">Click Save.</span></span>


