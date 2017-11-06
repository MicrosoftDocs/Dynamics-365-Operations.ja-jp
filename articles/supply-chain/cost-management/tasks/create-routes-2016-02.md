--- 
title: "ルートの作成 (2016 年 2 月のみ)"
description: "このタスクでは、完成品と半完成品の部品表の生産工順の作成について説明します。"
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
ms.sourcegitcommit: 1c2801af8201865f5ae9233c9729a4d59ef84bcd
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="5b6bc-103">ルートの作成 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="5b6bc-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b6bc-104">このタスクでは、完成品と半完成品の部品表の生産工順の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="5b6bc-105">これは、BOM 計算シリーズの 5 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="5b6bc-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="5b6bc-107">半完成品の工順の作成</span><span class="sxs-lookup"><span data-stu-id="5b6bc-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="5b6bc-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5b6bc-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b6bc-110">品目番号 BOM_2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="5b6bc-111">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="5b6bc-112">[工順] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-112">Click Route.</span></span>
5. <span data-ttu-id="5b6bc-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-113">Click New.</span></span>
6. <span data-ttu-id="5b6bc-114">[工順と工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-114">Click Route and route version.</span></span>
7. <span data-ttu-id="5b6bc-115">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5b6bc-116">たとえば、「ROUTE_2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="5b6bc-117">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-118">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="5b6bc-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-119">Click OK.</span></span>
10. <span data-ttu-id="5b6bc-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-120">Click New.</span></span>
11. <span data-ttu-id="5b6bc-121">[操作] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-122">この例では、[組み立て] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="5b6bc-123">[実行時間] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="5b6bc-124">たとえば、「1」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-124">For example, type 1.</span></span> <span data-ttu-id="5b6bc-125">実行時間は、多くの場合、品目について計算される価格の一部になります。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="5b6bc-126">[工順グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-127">この例では、「Std」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="5b6bc-128">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="5b6bc-129">[段取りカテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-130">この例では、[組み立て] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="5b6bc-131">[時間] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-131">Click the Times tab.</span></span>
17. <span data-ttu-id="5b6bc-132">[段取り時間] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="5b6bc-133">この例では、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-133">For this example, type 1.</span></span> <span data-ttu-id="5b6bc-134">段取り時間は、多くの場合、品目について計算される価格の一部になります。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="5b6bc-135">[アクション ペイン] で、[工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="5b6bc-136">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-136">Click Approve.</span></span>
20. <span data-ttu-id="5b6bc-137">[工順も承認しますか?] で [はい] を選択します。] アクションを使用すると、このチェック ボックスは自動的にオンになります。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="5b6bc-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-138">Click OK.</span></span>
22. <span data-ttu-id="5b6bc-139">[アクション ペイン] で、[工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="5b6bc-140">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-140">Click Activate.</span></span>
24. <span data-ttu-id="5b6bc-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-141">Close the page.</span></span>
25. <span data-ttu-id="5b6bc-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="5b6bc-143">完成品の工順の作成</span><span class="sxs-lookup"><span data-stu-id="5b6bc-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="5b6bc-144">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b6bc-145">品目番号 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="5b6bc-146">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="5b6bc-147">[工順] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-147">Click Route.</span></span>
4. <span data-ttu-id="5b6bc-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-148">Click New.</span></span>
5. <span data-ttu-id="5b6bc-149">[工順と工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-149">Click Route and route version.</span></span>
6. <span data-ttu-id="5b6bc-150">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5b6bc-151">この例では、「ROUTE_1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="5b6bc-152">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-153">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="5b6bc-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-154">Click OK.</span></span>
9. <span data-ttu-id="5b6bc-155">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-155">Click New.</span></span>
10. <span data-ttu-id="5b6bc-156">[操作] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-157">この例では、[梱包] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="5b6bc-158">[実行時間] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="5b6bc-159">この例では、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="5b6bc-160">[工順グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-161">この例では、「Std」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="5b6bc-162">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="5b6bc-163">[段取りカテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="5b6bc-164">この例では、[梱包] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="5b6bc-165">[時間] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-165">Click the Times tab.</span></span>
16. <span data-ttu-id="5b6bc-166">[段取り時間] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="5b6bc-167">この例では、「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="5b6bc-168">[アクション ペイン] で、[工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="5b6bc-169">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-169">Click Approve.</span></span>
19. <span data-ttu-id="5b6bc-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-170">Click OK.</span></span>
20. <span data-ttu-id="5b6bc-171">[アクション ペイン] で、[工順バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="5b6bc-172">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-172">Click Activate.</span></span>
22. <span data-ttu-id="5b6bc-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-173">Close the page.</span></span>
23. <span data-ttu-id="5b6bc-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="5b6bc-175">段取り時間の自動消費の有効化</span><span class="sxs-lookup"><span data-stu-id="5b6bc-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="5b6bc-176">[生産管理] > [段取り] > [工順] > [工順グループ] に順に進みます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="5b6bc-177">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b6bc-178">一覧で「Std」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="5b6bc-179">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-179">Click Edit.</span></span>
4. <span data-ttu-id="5b6bc-180">[段取り時間] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="5b6bc-181">段取り時間は、多くの場合、品目について計算される価格の一部になります。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="5b6bc-182">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-182">Click Save.</span></span>
6. <span data-ttu-id="5b6bc-183">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b6bc-183">Close the page.</span></span>

