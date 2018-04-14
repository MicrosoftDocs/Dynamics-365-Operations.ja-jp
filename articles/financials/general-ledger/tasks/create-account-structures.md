--- 
title: "勘定構造の作成"
description: "このタスク ガイドでは、勘定構造の作成について説明します。"
author: aprilolson
manager: AnnBe
ms.date: 11/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 38e90441803d5eda397e35eb2c6d310790189d5f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-account-structures"></a><span data-ttu-id="4c8fa-103">勘定構造の作成</span><span class="sxs-lookup"><span data-stu-id="4c8fa-103">Create account structures</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c8fa-104">このタスク ガイドでは、勘定構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="4c8fa-105">手順は、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="4c8fa-106">[総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="4c8fa-107">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="4c8fa-108">[勘定構造] フィールドで、勘定構造の目的を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="4c8fa-109">[説明] フィールドで、勘定構造の目的を指定するための説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="4c8fa-110">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-110">Click Create.</span></span>
6. <span data-ttu-id="4c8fa-111">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-111">Click Add segment.</span></span>
7. <span data-ttu-id="4c8fa-112">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="4c8fa-113">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-113">Click Add segment.</span></span>
9. <span data-ttu-id="4c8fa-114">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-114">Click Add segment.</span></span>
10. <span data-ttu-id="4c8fa-115">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="4c8fa-116">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-116">Click Add segment.</span></span>
12. <span data-ttu-id="4c8fa-117">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-117">Click Add segment.</span></span>
13. <span data-ttu-id="4c8fa-118">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="4c8fa-119">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-119">Click Add segment.</span></span>
15. <span data-ttu-id="4c8fa-120">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="4c8fa-121">たとえば、[主勘定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="4c8fa-122">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="4c8fa-123">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-124">たとえば、600000 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-124">For example, 600000.</span></span>  
18. <span data-ttu-id="4c8fa-125">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-126">たとえば、699999 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-126">For example, 699999.</span></span>  
19. <span data-ttu-id="4c8fa-127">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-127">Click Apply.</span></span>
20. <span data-ttu-id="4c8fa-128">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="4c8fa-129">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-129">For example, Department.</span></span>  
21. <span data-ttu-id="4c8fa-130">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="4c8fa-131">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-132">例えば 022 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-132">For example, 022.</span></span>  
23. <span data-ttu-id="4c8fa-133">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-134">たとえば、031 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-134">For example, 031.</span></span>  
24. <span data-ttu-id="4c8fa-135">[新しい基準の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="4c8fa-136">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="4c8fa-137">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-138">たとえば、033 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-138">For example, 033.</span></span>  
27. <span data-ttu-id="4c8fa-139">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-140">たとえば、034 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-140">For example, 034.</span></span>  
28. <span data-ttu-id="4c8fa-141">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-141">Click Apply.</span></span>
29. <span data-ttu-id="4c8fa-142">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="4c8fa-143">たとえば、[減価部門] です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="4c8fa-144">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-145">たとえば、007..021 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="4c8fa-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-146">Click Add.</span></span>
32. <span data-ttu-id="4c8fa-147">[主勘定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-148">たとえば、600000..699999</span><span class="sxs-lookup"><span data-stu-id="4c8fa-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="4c8fa-149">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="4c8fa-150">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-150">For example, Department.</span></span>  
34. <span data-ttu-id="4c8fa-151">[部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-152">たとえば、032 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-152">For example, 032.</span></span>  
35. <span data-ttu-id="4c8fa-153">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="4c8fa-154">たとえば、086 です。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-154">For example, 086.</span></span>  
36. <span data-ttu-id="4c8fa-155">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-155">Click Validate.</span></span>
37. <span data-ttu-id="4c8fa-156">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-156">Click Activate.</span></span>
38. <span data-ttu-id="4c8fa-157">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c8fa-157">Click Activate.</span></span>


