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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552673"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="a22b0-103">原材料の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="a22b0-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a22b0-104">このタスクでは、完成品と半完成品のコンポーネントの作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="a22b0-105">これは、BOM 計算シリーズの 3 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="a22b0-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a22b0-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="a22b0-107">最初の材料の作成</span><span class="sxs-lookup"><span data-stu-id="a22b0-107">Create the first material</span></span>
1. <span data-ttu-id="a22b0-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a22b0-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-109">Click New.</span></span>
3. <span data-ttu-id="a22b0-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="a22b0-111">この例では、ITEM_A を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="a22b0-112">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-113">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-113">Select STD.</span></span> <span data-ttu-id="a22b0-114">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="a22b0-115">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-116">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-116">For example, select Audio.</span></span> <span data-ttu-id="a22b0-117">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="a22b0-118">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-119">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-119">Select SiteWH.</span></span> <span data-ttu-id="a22b0-120">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="a22b0-121">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-122">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="a22b0-123">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-123">Select None.</span></span>  
8. <span data-ttu-id="a22b0-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-124">Click OK.</span></span>
9. <span data-ttu-id="a22b0-125">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="a22b0-126">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-126">Click Default order settings.</span></span>
11. <span data-ttu-id="a22b0-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="a22b0-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="a22b0-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="a22b0-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-133">Close the page.</span></span>
15. <span data-ttu-id="a22b0-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-134">Close the page.</span></span>
16. <span data-ttu-id="a22b0-135">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a22b0-136">ITEM_A をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="a22b0-137">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="a22b0-138">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="a22b0-139">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="a22b0-140">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="a22b0-141">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-141">Click Item price.</span></span>
21. <span data-ttu-id="a22b0-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-142">Click New.</span></span>
22. <span data-ttu-id="a22b0-143">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-144">たとえば、標準原価の原価タイプの 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="a22b0-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-146">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="a22b0-147">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="a22b0-148">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="a22b0-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-149">Click Save.</span></span>
26. <span data-ttu-id="a22b0-150">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="a22b0-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-151">Close the page.</span></span>
28. <span data-ttu-id="a22b0-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="a22b0-153">2 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="a22b0-153">Create the second material</span></span>
1. <span data-ttu-id="a22b0-154">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-154">Click New.</span></span>
2. <span data-ttu-id="a22b0-155">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="a22b0-156">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="a22b0-157">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-158">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-158">Select STD.</span></span> <span data-ttu-id="a22b0-159">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="a22b0-160">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-161">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-161">For example, select Audio.</span></span> <span data-ttu-id="a22b0-162">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="a22b0-163">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-164">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-164">Select SiteWH.</span></span> <span data-ttu-id="a22b0-165">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="a22b0-166">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-167">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="a22b0-168">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-168">Select None.</span></span>  
7. <span data-ttu-id="a22b0-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-169">Click OK.</span></span>
8. <span data-ttu-id="a22b0-170">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="a22b0-171">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-171">Click Default order settings.</span></span>
10. <span data-ttu-id="a22b0-172">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-173">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="a22b0-174">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-175">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="a22b0-176">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-177">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="a22b0-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-178">Close the page.</span></span>
14. <span data-ttu-id="a22b0-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-179">Close the page.</span></span>
15. <span data-ttu-id="a22b0-180">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a22b0-181">ITEM_B をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="a22b0-182">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="a22b0-183">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="a22b0-184">この例では、「M2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="a22b0-185">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="a22b0-186">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-186">Click Item price.</span></span>
20. <span data-ttu-id="a22b0-187">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-187">Click New.</span></span>
21. <span data-ttu-id="a22b0-188">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-189">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-189">For this example, select 10.</span></span> <span data-ttu-id="a22b0-190">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="a22b0-191">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-192">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="a22b0-193">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="a22b0-194">デモの場合、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="a22b0-195">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-195">Click Save.</span></span>
25. <span data-ttu-id="a22b0-196">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="a22b0-197">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-197">Close the page.</span></span>
27. <span data-ttu-id="a22b0-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="a22b0-199">3 番目の材料の作成</span><span class="sxs-lookup"><span data-stu-id="a22b0-199">Create the third material</span></span>
1. <span data-ttu-id="a22b0-200">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-200">Click New.</span></span>
2. <span data-ttu-id="a22b0-201">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="a22b0-202">デモの場合、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="a22b0-203">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-204">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-204">Select STD.</span></span> <span data-ttu-id="a22b0-205">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="a22b0-206">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-207">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-207">For example, select Audio.</span></span> <span data-ttu-id="a22b0-208">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="a22b0-209">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-210">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-210">Select SiteWH.</span></span> <span data-ttu-id="a22b0-211">サイトと倉庫のみがデモに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="a22b0-212">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-213">追跡用分析コードはこの例には使用されません。</span><span class="sxs-lookup"><span data-stu-id="a22b0-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="a22b0-214">「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-214">Select None.</span></span>  
7. <span data-ttu-id="a22b0-215">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-215">Click OK.</span></span>
8. <span data-ttu-id="a22b0-216">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="a22b0-217">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-217">Click Default order settings.</span></span>
10. <span data-ttu-id="a22b0-218">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-219">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="a22b0-220">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-221">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="a22b0-222">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-223">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="a22b0-224">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-224">Close the page.</span></span>
14. <span data-ttu-id="a22b0-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-225">Close the page.</span></span>
15. <span data-ttu-id="a22b0-226">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a22b0-227">ITEM_C をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="a22b0-228">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="a22b0-229">[原価グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="a22b0-230">この例では、「M1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="a22b0-231">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="a22b0-232">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-232">Click Item price.</span></span>
20. <span data-ttu-id="a22b0-233">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-233">Click New.</span></span>
21. <span data-ttu-id="a22b0-234">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-235">この例では、「10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-235">For this example, select 10.</span></span> <span data-ttu-id="a22b0-236">これは標準原価の原価タイプです。</span><span class="sxs-lookup"><span data-stu-id="a22b0-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="a22b0-237">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a22b0-238">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="a22b0-239">[価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="a22b0-240">この例では、「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a22b0-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="a22b0-241">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-241">Click Save.</span></span>
25. <span data-ttu-id="a22b0-242">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a22b0-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="a22b0-243">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-243">Close the page.</span></span>
27. <span data-ttu-id="a22b0-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a22b0-244">Close the page.</span></span>

