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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="c739d-103">原材料の作成 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="c739d-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c739d-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="c739d-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="c739d-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="c739d-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="c739d-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c739d-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="c739d-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c739d-107">Create the first material</span></span>
1. <span data-ttu-id="c739d-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c739d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c739d-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-109">Click New.</span></span>
3. <span data-ttu-id="c739d-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c739d-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="c739d-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-113">Select STD.</span></span> <span data-ttu-id="c739d-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c739d-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="c739d-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-116">For example, select Audio.</span></span> <span data-ttu-id="c739d-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c739d-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="c739d-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-119">Select SiteWH.</span></span> <span data-ttu-id="c739d-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c739d-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="c739d-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c739d-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c739d-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-123">Select None.</span></span>  
8. <span data-ttu-id="c739d-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-124">Click OK.</span></span>
9. <span data-ttu-id="c739d-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="c739d-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-126">Click Default order settings.</span></span>
11. <span data-ttu-id="c739d-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c739d-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c739d-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="c739d-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-133">Close the page.</span></span>
15. <span data-ttu-id="c739d-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-134">Close the page.</span></span>
16. <span data-ttu-id="c739d-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c739d-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="c739d-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c739d-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="c739d-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c739d-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="c739d-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="c739d-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-141">Click Item price.</span></span>
21. <span data-ttu-id="c739d-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-142">Click New.</span></span>
22. <span data-ttu-id="c739d-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="c739d-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="c739d-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c739d-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="c739d-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-149">Click Save.</span></span>
26. <span data-ttu-id="c739d-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="c739d-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-151">Close the page.</span></span>
28. <span data-ttu-id="c739d-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="c739d-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c739d-153">Create the second material</span></span>
1. <span data-ttu-id="c739d-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-154">Click New.</span></span>
2. <span data-ttu-id="c739d-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c739d-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="c739d-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-158">Select STD.</span></span> <span data-ttu-id="c739d-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c739d-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c739d-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-161">For example, select Audio.</span></span> <span data-ttu-id="c739d-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c739d-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c739d-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-164">Select SiteWH.</span></span> <span data-ttu-id="c739d-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c739d-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="c739d-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c739d-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c739d-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-168">Select None.</span></span>  
7. <span data-ttu-id="c739d-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-169">Click OK.</span></span>
8. <span data-ttu-id="c739d-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c739d-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-171">Click Default order settings.</span></span>
10. <span data-ttu-id="c739d-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c739d-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c739d-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c739d-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-178">Close the page.</span></span>
14. <span data-ttu-id="c739d-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-179">Close the page.</span></span>
15. <span data-ttu-id="c739d-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c739d-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="c739d-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c739d-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c739d-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c739d-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="c739d-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c739d-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-186">Click Item price.</span></span>
20. <span data-ttu-id="c739d-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-187">Click New.</span></span>
21. <span data-ttu-id="c739d-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-189">For this example, select 10.</span></span> <span data-ttu-id="c739d-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="c739d-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c739d-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c739d-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c739d-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="c739d-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-195">Click Save.</span></span>
25. <span data-ttu-id="c739d-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c739d-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-197">Close the page.</span></span>
27. <span data-ttu-id="c739d-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="c739d-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c739d-199">Create the third material</span></span>
1. <span data-ttu-id="c739d-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-200">Click New.</span></span>
2. <span data-ttu-id="c739d-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c739d-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="c739d-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-204">Select STD.</span></span> <span data-ttu-id="c739d-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c739d-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c739d-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-207">For example, select Audio.</span></span> <span data-ttu-id="c739d-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c739d-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c739d-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-210">Select SiteWH.</span></span> <span data-ttu-id="c739d-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c739d-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="c739d-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c739d-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c739d-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-214">Select None.</span></span>  
7. <span data-ttu-id="c739d-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-215">Click OK.</span></span>
8. <span data-ttu-id="c739d-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c739d-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-217">Click Default order settings.</span></span>
10. <span data-ttu-id="c739d-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c739d-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c739d-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c739d-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-224">Close the page.</span></span>
14. <span data-ttu-id="c739d-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-225">Close the page.</span></span>
15. <span data-ttu-id="c739d-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c739d-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="c739d-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c739d-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c739d-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c739d-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="c739d-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c739d-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-232">Click Item price.</span></span>
20. <span data-ttu-id="c739d-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-233">Click New.</span></span>
21. <span data-ttu-id="c739d-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-235">For this example, select 10.</span></span> <span data-ttu-id="c739d-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="c739d-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c739d-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c739d-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c739d-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c739d-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c739d-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c739d-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="c739d-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-241">Click Save.</span></span>
25. <span data-ttu-id="c739d-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c739d-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c739d-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-243">Close the page.</span></span>
27. <span data-ttu-id="c739d-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c739d-244">Close the page.</span></span>


