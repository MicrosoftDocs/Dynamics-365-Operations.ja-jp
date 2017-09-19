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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 210bf36f0e989ce0e6ceda046f02d1091592a3c1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-account-structures"></a><span data-ttu-id="605b6-103">勘定構造の作成</span><span class="sxs-lookup"><span data-stu-id="605b6-103">Create account structures</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="605b6-104">このタスク ガイドでは、勘定構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="605b6-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="605b6-105">手順は、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="605b6-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="605b6-106">[総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="605b6-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="605b6-107">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="605b6-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="605b6-108">[勘定構造] フィールドで、勘定構造の目的を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="605b6-109">[説明] フィールドで、勘定構造の目的を指定するための説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="605b6-110">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-110">Click Create.</span></span>
6. <span data-ttu-id="605b6-111">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-111">Click Add segment.</span></span>
7. <span data-ttu-id="605b6-112">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="605b6-113">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-113">Click Add segment.</span></span>
9. <span data-ttu-id="605b6-114">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-114">Click Add segment.</span></span>
10. <span data-ttu-id="605b6-115">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="605b6-116">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-116">Click Add segment.</span></span>
12. <span data-ttu-id="605b6-117">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-117">Click Add segment.</span></span>
13. <span data-ttu-id="605b6-118">[分析コード リスト] で、勘定構造に追加する分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="605b6-119">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-119">Click Add segment.</span></span>
15. <span data-ttu-id="605b6-120">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="605b6-121">たとえば、[主勘定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="605b6-122">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="605b6-123">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="605b6-124">たとえば、600000 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-124">For example, 600000.</span></span>  
18. <span data-ttu-id="605b6-125">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="605b6-126">たとえば、699999 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-126">For example, 699999.</span></span>  
19. <span data-ttu-id="605b6-127">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-127">Click Apply.</span></span>
20. <span data-ttu-id="605b6-128">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="605b6-129">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="605b6-129">For example, Department.</span></span>  
21. <span data-ttu-id="605b6-130">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="605b6-131">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="605b6-132">例えば 022 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-132">For example, 022.</span></span>  
23. <span data-ttu-id="605b6-133">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="605b6-134">たとえば、031 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-134">For example, 031.</span></span>  
24. <span data-ttu-id="605b6-135">[新しい基準の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="605b6-136">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="605b6-137">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="605b6-138">たとえば、033 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-138">For example, 033.</span></span>  
27. <span data-ttu-id="605b6-139">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="605b6-140">たとえば、034 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-140">For example, 034.</span></span>  
28. <span data-ttu-id="605b6-141">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-141">Click Apply.</span></span>
29. <span data-ttu-id="605b6-142">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="605b6-143">たとえば、[減価部門] です。</span><span class="sxs-lookup"><span data-stu-id="605b6-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="605b6-144">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="605b6-145">たとえば、007..021 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="605b6-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-146">Click Add.</span></span>
32. <span data-ttu-id="605b6-147">[主勘定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="605b6-148">たとえば、600000..699999</span><span class="sxs-lookup"><span data-stu-id="605b6-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="605b6-149">グリッドで、許可された値を編集する区分を選択します。</span><span class="sxs-lookup"><span data-stu-id="605b6-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="605b6-150">例えば [部門] です。</span><span class="sxs-lookup"><span data-stu-id="605b6-150">For example, Department.</span></span>  
34. <span data-ttu-id="605b6-151">[部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="605b6-152">たとえば、032 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-152">For example, 032.</span></span>  
35. <span data-ttu-id="605b6-153">[減価部門] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="605b6-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="605b6-154">たとえば、086 です。</span><span class="sxs-lookup"><span data-stu-id="605b6-154">For example, 086.</span></span>  
36. <span data-ttu-id="605b6-155">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-155">Click Validate.</span></span>
37. <span data-ttu-id="605b6-156">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-156">Click Activate.</span></span>
38. <span data-ttu-id="605b6-157">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="605b6-157">Click Activate.</span></span>

