---
title: 原材料の作成 (2016 年 2 月)
description: このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844588"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="c7688-103">原材料の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="c7688-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7688-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="c7688-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="c7688-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="c7688-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="c7688-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c7688-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="c7688-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c7688-107">Create the first material</span></span>
1. <span data-ttu-id="c7688-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c7688-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c7688-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-109">Click New.</span></span>
3. <span data-ttu-id="c7688-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c7688-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="c7688-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-113">Select STD.</span></span> <span data-ttu-id="c7688-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c7688-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="c7688-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-116">For example, select Audio.</span></span> <span data-ttu-id="c7688-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c7688-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="c7688-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-119">Select SiteWH.</span></span> <span data-ttu-id="c7688-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7688-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="c7688-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c7688-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c7688-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-123">Select None.</span></span>  
8. <span data-ttu-id="c7688-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-124">Click OK.</span></span>
9. <span data-ttu-id="c7688-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="c7688-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-126">Click Default order settings.</span></span>
11. <span data-ttu-id="c7688-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c7688-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c7688-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="c7688-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-133">Close the page.</span></span>
15. <span data-ttu-id="c7688-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-134">Close the page.</span></span>
16. <span data-ttu-id="c7688-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7688-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="c7688-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c7688-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="c7688-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c7688-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="c7688-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="c7688-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-141">Click Item price.</span></span>
21. <span data-ttu-id="c7688-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-142">Click New.</span></span>
22. <span data-ttu-id="c7688-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="c7688-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="c7688-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c7688-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="c7688-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-149">Click Save.</span></span>
26. <span data-ttu-id="c7688-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="c7688-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-151">Close the page.</span></span>
28. <span data-ttu-id="c7688-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="c7688-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c7688-153">Create the second material</span></span>
1. <span data-ttu-id="c7688-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-154">Click New.</span></span>
2. <span data-ttu-id="c7688-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c7688-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="c7688-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-158">Select STD.</span></span> <span data-ttu-id="c7688-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c7688-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c7688-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-161">For example, select Audio.</span></span> <span data-ttu-id="c7688-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c7688-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c7688-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-164">Select SiteWH.</span></span> <span data-ttu-id="c7688-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7688-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="c7688-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c7688-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c7688-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-168">Select None.</span></span>  
7. <span data-ttu-id="c7688-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-169">Click OK.</span></span>
8. <span data-ttu-id="c7688-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c7688-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-171">Click Default order settings.</span></span>
10. <span data-ttu-id="c7688-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c7688-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c7688-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c7688-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-178">Close the page.</span></span>
14. <span data-ttu-id="c7688-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-179">Close the page.</span></span>
15. <span data-ttu-id="c7688-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7688-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="c7688-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c7688-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c7688-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c7688-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="c7688-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c7688-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-186">Click Item price.</span></span>
20. <span data-ttu-id="c7688-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-187">Click New.</span></span>
21. <span data-ttu-id="c7688-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-189">For this example, select 10.</span></span> <span data-ttu-id="c7688-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="c7688-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c7688-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c7688-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c7688-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="c7688-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-195">Click Save.</span></span>
25. <span data-ttu-id="c7688-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c7688-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-197">Close the page.</span></span>
27. <span data-ttu-id="c7688-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="c7688-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="c7688-199">Create the third material</span></span>
1. <span data-ttu-id="c7688-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-200">Click New.</span></span>
2. <span data-ttu-id="c7688-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="c7688-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="c7688-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-204">Select STD.</span></span> <span data-ttu-id="c7688-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="c7688-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="c7688-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-207">For example, select Audio.</span></span> <span data-ttu-id="c7688-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c7688-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="c7688-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-210">Select SiteWH.</span></span> <span data-ttu-id="c7688-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7688-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="c7688-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="c7688-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="c7688-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-214">Select None.</span></span>  
7. <span data-ttu-id="c7688-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-215">Click OK.</span></span>
8. <span data-ttu-id="c7688-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="c7688-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-217">Click Default order settings.</span></span>
10. <span data-ttu-id="c7688-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="c7688-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="c7688-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="c7688-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-224">Close the page.</span></span>
14. <span data-ttu-id="c7688-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-225">Close the page.</span></span>
15. <span data-ttu-id="c7688-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7688-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="c7688-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c7688-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="c7688-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="c7688-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="c7688-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="c7688-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-232">Click Item price.</span></span>
20. <span data-ttu-id="c7688-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-233">Click New.</span></span>
21. <span data-ttu-id="c7688-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-235">For this example, select 10.</span></span> <span data-ttu-id="c7688-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="c7688-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="c7688-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c7688-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c7688-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="c7688-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="c7688-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c7688-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="c7688-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-241">Click Save.</span></span>
25. <span data-ttu-id="c7688-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c7688-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="c7688-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-243">Close the page.</span></span>
27. <span data-ttu-id="c7688-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c7688-244">Close the page.</span></span>

