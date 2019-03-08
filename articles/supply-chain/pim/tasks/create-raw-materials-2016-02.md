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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "351059"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="18655-103">原材料の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="18655-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18655-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="18655-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="18655-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="18655-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="18655-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="18655-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="18655-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="18655-107">Create the first material</span></span>
1. <span data-ttu-id="18655-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="18655-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="18655-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-109">Click New.</span></span>
3. <span data-ttu-id="18655-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="18655-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="18655-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-113">Select STD.</span></span> <span data-ttu-id="18655-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="18655-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="18655-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-116">For example, select Audio.</span></span> <span data-ttu-id="18655-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="18655-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="18655-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-119">Select SiteWH.</span></span> <span data-ttu-id="18655-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="18655-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="18655-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="18655-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="18655-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-123">Select None.</span></span>  
8. <span data-ttu-id="18655-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-124">Click OK.</span></span>
9. <span data-ttu-id="18655-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="18655-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-126">Click Default order settings.</span></span>
11. <span data-ttu-id="18655-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="18655-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="18655-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="18655-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-133">Close the page.</span></span>
15. <span data-ttu-id="18655-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-134">Close the page.</span></span>
16. <span data-ttu-id="18655-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="18655-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="18655-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="18655-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="18655-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="18655-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="18655-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="18655-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-141">Click Item price.</span></span>
21. <span data-ttu-id="18655-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-142">Click New.</span></span>
22. <span data-ttu-id="18655-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="18655-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="18655-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="18655-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="18655-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-149">Click Save.</span></span>
26. <span data-ttu-id="18655-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="18655-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-151">Close the page.</span></span>
28. <span data-ttu-id="18655-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="18655-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="18655-153">Create the second material</span></span>
1. <span data-ttu-id="18655-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-154">Click New.</span></span>
2. <span data-ttu-id="18655-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="18655-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="18655-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-158">Select STD.</span></span> <span data-ttu-id="18655-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="18655-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="18655-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-161">For example, select Audio.</span></span> <span data-ttu-id="18655-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="18655-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="18655-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-164">Select SiteWH.</span></span> <span data-ttu-id="18655-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="18655-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="18655-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="18655-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="18655-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-168">Select None.</span></span>  
7. <span data-ttu-id="18655-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-169">Click OK.</span></span>
8. <span data-ttu-id="18655-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="18655-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-171">Click Default order settings.</span></span>
10. <span data-ttu-id="18655-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="18655-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="18655-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="18655-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-178">Close the page.</span></span>
14. <span data-ttu-id="18655-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-179">Close the page.</span></span>
15. <span data-ttu-id="18655-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="18655-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="18655-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="18655-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="18655-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="18655-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="18655-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="18655-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-186">Click Item price.</span></span>
20. <span data-ttu-id="18655-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-187">Click New.</span></span>
21. <span data-ttu-id="18655-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-189">For this example, select 10.</span></span> <span data-ttu-id="18655-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="18655-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="18655-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="18655-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="18655-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="18655-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-195">Click Save.</span></span>
25. <span data-ttu-id="18655-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="18655-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-197">Close the page.</span></span>
27. <span data-ttu-id="18655-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="18655-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="18655-199">Create the third material</span></span>
1. <span data-ttu-id="18655-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-200">Click New.</span></span>
2. <span data-ttu-id="18655-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="18655-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="18655-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-204">Select STD.</span></span> <span data-ttu-id="18655-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="18655-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="18655-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-207">For example, select Audio.</span></span> <span data-ttu-id="18655-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="18655-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="18655-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-210">Select SiteWH.</span></span> <span data-ttu-id="18655-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="18655-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="18655-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="18655-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="18655-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-214">Select None.</span></span>  
7. <span data-ttu-id="18655-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-215">Click OK.</span></span>
8. <span data-ttu-id="18655-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="18655-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-217">Click Default order settings.</span></span>
10. <span data-ttu-id="18655-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="18655-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="18655-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="18655-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-224">Close the page.</span></span>
14. <span data-ttu-id="18655-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-225">Close the page.</span></span>
15. <span data-ttu-id="18655-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="18655-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="18655-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="18655-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="18655-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="18655-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="18655-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="18655-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-232">Click Item price.</span></span>
20. <span data-ttu-id="18655-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-233">Click New.</span></span>
21. <span data-ttu-id="18655-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-235">For this example, select 10.</span></span> <span data-ttu-id="18655-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="18655-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="18655-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="18655-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="18655-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="18655-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="18655-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="18655-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="18655-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-241">Click Save.</span></span>
25. <span data-ttu-id="18655-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18655-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="18655-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-243">Close the page.</span></span>
27. <span data-ttu-id="18655-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="18655-244">Close the page.</span></span>

