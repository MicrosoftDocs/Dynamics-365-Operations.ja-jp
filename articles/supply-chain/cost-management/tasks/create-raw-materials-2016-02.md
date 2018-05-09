--- 
title: "原材料の作成 (2016 年 2 月のみ)"
description: "このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a33e3f7c2bdc54bab255960cebdeb3edec6d20d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="969b7-103">原材料の作成 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="969b7-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="969b7-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="969b7-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="969b7-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="969b7-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="969b7-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="969b7-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="969b7-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="969b7-107">Create the first material</span></span>
1. <span data-ttu-id="969b7-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="969b7-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="969b7-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-109">Click New.</span></span>
3. <span data-ttu-id="969b7-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="969b7-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="969b7-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-113">Select STD.</span></span> <span data-ttu-id="969b7-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="969b7-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="969b7-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-116">For example, select Audio.</span></span> <span data-ttu-id="969b7-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="969b7-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="969b7-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-119">Select SiteWH.</span></span> <span data-ttu-id="969b7-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="969b7-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="969b7-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="969b7-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="969b7-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-123">Select None.</span></span>  
8. <span data-ttu-id="969b7-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-124">Click OK.</span></span>
9. <span data-ttu-id="969b7-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="969b7-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-126">Click Default order settings.</span></span>
11. <span data-ttu-id="969b7-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="969b7-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="969b7-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="969b7-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-133">Close the page.</span></span>
15. <span data-ttu-id="969b7-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-134">Close the page.</span></span>
16. <span data-ttu-id="969b7-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="969b7-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="969b7-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="969b7-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="969b7-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="969b7-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="969b7-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="969b7-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-141">Click Item price.</span></span>
21. <span data-ttu-id="969b7-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-142">Click New.</span></span>
22. <span data-ttu-id="969b7-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="969b7-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="969b7-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="969b7-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="969b7-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-149">Click Save.</span></span>
26. <span data-ttu-id="969b7-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="969b7-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-151">Close the page.</span></span>
28. <span data-ttu-id="969b7-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="969b7-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="969b7-153">Create the second material</span></span>
1. <span data-ttu-id="969b7-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-154">Click New.</span></span>
2. <span data-ttu-id="969b7-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="969b7-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="969b7-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-158">Select STD.</span></span> <span data-ttu-id="969b7-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="969b7-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="969b7-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-161">For example, select Audio.</span></span> <span data-ttu-id="969b7-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="969b7-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="969b7-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-164">Select SiteWH.</span></span> <span data-ttu-id="969b7-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="969b7-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="969b7-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="969b7-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="969b7-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-168">Select None.</span></span>  
7. <span data-ttu-id="969b7-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-169">Click OK.</span></span>
8. <span data-ttu-id="969b7-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="969b7-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-171">Click Default order settings.</span></span>
10. <span data-ttu-id="969b7-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="969b7-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="969b7-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="969b7-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-178">Close the page.</span></span>
14. <span data-ttu-id="969b7-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-179">Close the page.</span></span>
15. <span data-ttu-id="969b7-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="969b7-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="969b7-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="969b7-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="969b7-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="969b7-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="969b7-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="969b7-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-186">Click Item price.</span></span>
20. <span data-ttu-id="969b7-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-187">Click New.</span></span>
21. <span data-ttu-id="969b7-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-189">For this example, select 10.</span></span> <span data-ttu-id="969b7-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="969b7-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="969b7-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="969b7-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="969b7-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="969b7-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-195">Click Save.</span></span>
25. <span data-ttu-id="969b7-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="969b7-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-197">Close the page.</span></span>
27. <span data-ttu-id="969b7-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="969b7-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="969b7-199">Create the third material</span></span>
1. <span data-ttu-id="969b7-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-200">Click New.</span></span>
2. <span data-ttu-id="969b7-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="969b7-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="969b7-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-204">Select STD.</span></span> <span data-ttu-id="969b7-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="969b7-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="969b7-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-207">For example, select Audio.</span></span> <span data-ttu-id="969b7-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="969b7-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="969b7-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-210">Select SiteWH.</span></span> <span data-ttu-id="969b7-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="969b7-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="969b7-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="969b7-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="969b7-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-214">Select None.</span></span>  
7. <span data-ttu-id="969b7-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-215">Click OK.</span></span>
8. <span data-ttu-id="969b7-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="969b7-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-217">Click Default order settings.</span></span>
10. <span data-ttu-id="969b7-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="969b7-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="969b7-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="969b7-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-224">Close the page.</span></span>
14. <span data-ttu-id="969b7-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-225">Close the page.</span></span>
15. <span data-ttu-id="969b7-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="969b7-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="969b7-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="969b7-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="969b7-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="969b7-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="969b7-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="969b7-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-232">Click Item price.</span></span>
20. <span data-ttu-id="969b7-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-233">Click New.</span></span>
21. <span data-ttu-id="969b7-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-235">For this example, select 10.</span></span> <span data-ttu-id="969b7-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="969b7-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="969b7-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="969b7-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="969b7-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="969b7-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="969b7-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="969b7-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="969b7-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-241">Click Save.</span></span>
25. <span data-ttu-id="969b7-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="969b7-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="969b7-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-243">Close the page.</span></span>
27. <span data-ttu-id="969b7-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="969b7-244">Close the page.</span></span>


