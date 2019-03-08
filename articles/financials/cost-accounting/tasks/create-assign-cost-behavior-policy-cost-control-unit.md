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
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7b39b7649aaef0d354b61e3d70b6cac887282ed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "313822"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="f03f0-103">原価動作ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="f03f0-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f03f0-104">原価の動作は、固定費または変動費の分類です。</span><span class="sxs-lookup"><span data-stu-id="f03f0-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="f03f0-105">ポリシーと対応ルールは、有効になるポリシーの原価管理単位へ割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f03f0-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="f03f0-106">ポリシーを作成し、原価管理単位へ割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="f03f0-107">原価動作階層を作成</span><span class="sxs-lookup"><span data-stu-id="f03f0-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="f03f0-108">[原価会計] > [分析コード] > [分析コード階層] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="f03f0-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-109">Click New.</span></span>
3. <span data-ttu-id="f03f0-110">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-110">Click Create.</span></span>
4. <span data-ttu-id="f03f0-111">[分析コード階層名] フィールドでは、「原価動作階層」を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="f03f0-112">[分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-113">[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="f03f0-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-114">Click Save.</span></span>
7. <span data-ttu-id="f03f0-115">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="f03f0-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-116">Click New.</span></span>
9. <span data-ttu-id="f03f0-117">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="f03f0-118">[固定費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="f03f0-119">ツリーで、「原価動作階層」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="f03f0-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-120">Click New.</span></span>
12. <span data-ttu-id="f03f0-121">[ノード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="f03f0-122">[変動費] を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="f03f0-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-123">Click Save.</span></span>
14. <span data-ttu-id="f03f0-124">ツリーで、「原価動作階層\固定費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="f03f0-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-125">Click New.</span></span>
16. <span data-ttu-id="f03f0-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="f03f0-127">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-128">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="f03f0-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="f03f0-129">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-130">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="f03f0-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="f03f0-131">ツリーで、「原価動作階層\変動費」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="f03f0-132">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-132">Click New.</span></span>
21. <span data-ttu-id="f03f0-133">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="f03f0-134">[移動元分析コード メンバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-135">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="f03f0-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="f03f0-136">[移動先分析コード メンバー] フィールドでは、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-137">分析コード メンバーの範囲にギャップが生じる可能性がありますが、メンバーとは重複できません。</span><span class="sxs-lookup"><span data-stu-id="f03f0-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="f03f0-138">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="f03f0-139">ポリシーとルールを作成</span><span class="sxs-lookup"><span data-stu-id="f03f0-139">Create the policy and rules</span></span>
1. <span data-ttu-id="f03f0-140">[原価会計] > [ポリシー] > [原価動作ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="f03f0-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-141">Click New.</span></span>
3. <span data-ttu-id="f03f0-142">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="f03f0-143">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-144">作成したポリシーの階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="f03f0-145">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-146">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-146">Select Organization.</span></span>  
6. <span data-ttu-id="f03f0-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-147">Click Save.</span></span>
7. <span data-ttu-id="f03f0-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-148">Click New.</span></span>
8. <span data-ttu-id="f03f0-149">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f03f0-150">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-151">階層を展開し、[変動費] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="f03f0-152">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="f03f0-153">既定では、変動率は 100 パーセントです。</span><span class="sxs-lookup"><span data-stu-id="f03f0-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="f03f0-154">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="f03f0-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-155">Click New.</span></span>
13. <span data-ttu-id="f03f0-156">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f03f0-157">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="f03f0-158">ルールには有効期限がありますが、もし新しいバージョンが作成された場合、ユーザーまたはシステムがルールを失効させることが出来ます。</span><span class="sxs-lookup"><span data-stu-id="f03f0-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="f03f0-159">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f03f0-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="f03f0-160">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f03f0-160">Click Save.</span></span>

