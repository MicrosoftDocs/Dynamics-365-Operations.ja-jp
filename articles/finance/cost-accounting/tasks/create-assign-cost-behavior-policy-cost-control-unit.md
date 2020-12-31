---
title: 原価動作ポリシーの作成と原価管理単位への割り当て
description: 原価の動作は、固定費または変動費の分類です。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfdff9b1af9183d21e988dd53559e749eed077eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445120"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="3f119-103">原価動作ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="3f119-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f119-104">原価の動作は、固定費または変動費の分類です。</span><span class="sxs-lookup"><span data-stu-id="3f119-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="3f119-105">ポリシーと対応ルールは、有効になるポリシーの原価管理単位へ割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f119-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="3f119-106">ポリシーを作成し、原価管理単位へ割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3f119-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="3f119-107">原価動作階層を作成</span><span class="sxs-lookup"><span data-stu-id="3f119-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="3f119-108">[原価会計] > [分析コード] > [分析コード階層] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3f119-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3f119-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-109">Click New.</span></span>
3. <span data-ttu-id="3f119-110">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-110">Click Create.</span></span>
4. <span data-ttu-id="3f119-111">[分析コード階層名] フィールドでは、「原価動作階層」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="3f119-112">[分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-113">[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="3f119-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-114">Click Save.</span></span>
7. <span data-ttu-id="3f119-115">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="3f119-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-116">Click New.</span></span>
9. <span data-ttu-id="3f119-117">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="3f119-118">[固定費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="3f119-119">ツリーで、「原価動作階層」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="3f119-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-120">Click New.</span></span>
12. <span data-ttu-id="3f119-121">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="3f119-122">[変動費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="3f119-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-123">Click Save.</span></span>
14. <span data-ttu-id="3f119-124">ツリーで、「原価動作階層\固定費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="3f119-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-125">Click New.</span></span>
16. <span data-ttu-id="3f119-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3f119-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3f119-127">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-128">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="3f119-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="3f119-129">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-130">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="3f119-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="3f119-131">ツリーで、「原価動作階層\変動費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="3f119-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-132">Click New.</span></span>
21. <span data-ttu-id="3f119-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3f119-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="3f119-134">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-135">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="3f119-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="3f119-136">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-137">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="3f119-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="3f119-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="3f119-139">ポリシーとルールを作成</span><span class="sxs-lookup"><span data-stu-id="3f119-139">Create the policy and rules</span></span>
1. <span data-ttu-id="3f119-140">[原価会計] > [ポリシー] > [原価動作ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="3f119-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="3f119-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-141">Click New.</span></span>
3. <span data-ttu-id="3f119-142">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3f119-143">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-144">作成したポリシーの階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="3f119-145">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-146">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-146">Select Organization.</span></span>  
6. <span data-ttu-id="3f119-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-147">Click Save.</span></span>
7. <span data-ttu-id="3f119-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-148">Click New.</span></span>
8. <span data-ttu-id="3f119-149">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3f119-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3f119-150">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-151">階層を展開し、[変動費] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="3f119-152">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="3f119-153">既定では、変動率は 100 パーセントです。</span><span class="sxs-lookup"><span data-stu-id="3f119-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="3f119-154">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="3f119-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-155">Click New.</span></span>
13. <span data-ttu-id="3f119-156">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3f119-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="3f119-157">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f119-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3f119-158">ルールには有効期限がありますが、もし新しいバージョンが作成された場合、ユーザーまたはシステムがルールを失効させることが出来ます。</span><span class="sxs-lookup"><span data-stu-id="3f119-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="3f119-159">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3f119-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="3f119-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3f119-160">Click Save.</span></span>

