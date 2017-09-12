--- 
title: "原材料の作成 (2016 年 2 月のみ)"
description: "このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。"
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1c10e0f8275d928c1455cd99105aece8780e7f0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="e074c-103">原材料の作成 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="e074c-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e074c-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="e074c-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="e074c-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="e074c-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="e074c-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="e074c-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="e074c-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="e074c-107">Create the first material</span></span>
1. <span data-ttu-id="e074c-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e074c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e074c-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-109">Click New.</span></span>
3. <span data-ttu-id="e074c-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e074c-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="e074c-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-113">Select STD.</span></span> <span data-ttu-id="e074c-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="e074c-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e074c-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-116">For example, select Audio.</span></span> <span data-ttu-id="e074c-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="e074c-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e074c-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-119">Select SiteWH.</span></span> <span data-ttu-id="e074c-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e074c-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e074c-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="e074c-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e074c-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-123">Select None.</span></span>  
8. <span data-ttu-id="e074c-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-124">Click OK.</span></span>
9. <span data-ttu-id="e074c-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e074c-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-126">Click Default order settings.</span></span>
11. <span data-ttu-id="e074c-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e074c-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e074c-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e074c-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-133">Close the page.</span></span>
15. <span data-ttu-id="e074c-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-134">Close the page.</span></span>
16. <span data-ttu-id="e074c-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e074c-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="e074c-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e074c-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="e074c-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e074c-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="e074c-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="e074c-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-141">Click Item price.</span></span>
21. <span data-ttu-id="e074c-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-142">Click New.</span></span>
22. <span data-ttu-id="e074c-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="e074c-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="e074c-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e074c-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="e074c-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-149">Click Save.</span></span>
26. <span data-ttu-id="e074c-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="e074c-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-151">Close the page.</span></span>
28. <span data-ttu-id="e074c-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="e074c-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="e074c-153">Create the second material</span></span>
1. <span data-ttu-id="e074c-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-154">Click New.</span></span>
2. <span data-ttu-id="e074c-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e074c-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="e074c-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-158">Select STD.</span></span> <span data-ttu-id="e074c-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="e074c-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e074c-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-161">For example, select Audio.</span></span> <span data-ttu-id="e074c-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="e074c-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e074c-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-164">Select SiteWH.</span></span> <span data-ttu-id="e074c-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e074c-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="e074c-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="e074c-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e074c-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-168">Select None.</span></span>  
7. <span data-ttu-id="e074c-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-169">Click OK.</span></span>
8. <span data-ttu-id="e074c-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e074c-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-171">Click Default order settings.</span></span>
10. <span data-ttu-id="e074c-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e074c-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e074c-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e074c-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-178">Close the page.</span></span>
14. <span data-ttu-id="e074c-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-179">Close the page.</span></span>
15. <span data-ttu-id="e074c-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e074c-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="e074c-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e074c-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e074c-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e074c-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="e074c-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e074c-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-186">Click Item price.</span></span>
20. <span data-ttu-id="e074c-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-187">Click New.</span></span>
21. <span data-ttu-id="e074c-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-189">For this example, select 10.</span></span> <span data-ttu-id="e074c-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="e074c-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e074c-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e074c-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e074c-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="e074c-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-195">Click Save.</span></span>
25. <span data-ttu-id="e074c-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e074c-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-197">Close the page.</span></span>
27. <span data-ttu-id="e074c-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="e074c-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="e074c-199">Create the third material</span></span>
1. <span data-ttu-id="e074c-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-200">Click New.</span></span>
2. <span data-ttu-id="e074c-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e074c-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="e074c-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-204">Select STD.</span></span> <span data-ttu-id="e074c-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="e074c-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e074c-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-207">For example, select Audio.</span></span> <span data-ttu-id="e074c-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="e074c-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e074c-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-210">Select SiteWH.</span></span> <span data-ttu-id="e074c-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e074c-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="e074c-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="e074c-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e074c-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-214">Select None.</span></span>  
7. <span data-ttu-id="e074c-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-215">Click OK.</span></span>
8. <span data-ttu-id="e074c-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e074c-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-217">Click Default order settings.</span></span>
10. <span data-ttu-id="e074c-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e074c-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e074c-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e074c-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-224">Close the page.</span></span>
14. <span data-ttu-id="e074c-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-225">Close the page.</span></span>
15. <span data-ttu-id="e074c-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e074c-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="e074c-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e074c-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e074c-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e074c-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="e074c-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e074c-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-232">Click Item price.</span></span>
20. <span data-ttu-id="e074c-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-233">Click New.</span></span>
21. <span data-ttu-id="e074c-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-235">For this example, select 10.</span></span> <span data-ttu-id="e074c-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="e074c-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e074c-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e074c-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e074c-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e074c-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e074c-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e074c-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="e074c-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-241">Click Save.</span></span>
25. <span data-ttu-id="e074c-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e074c-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e074c-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-243">Close the page.</span></span>
27. <span data-ttu-id="e074c-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e074c-244">Close the page.</span></span>


