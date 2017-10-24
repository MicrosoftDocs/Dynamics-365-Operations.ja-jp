--- 
title: "BOM の作成 (2016 年 2 月のみ)"
description: "このタスクでは、完成品と半完成品の部品表の構造の作成について説明します。"
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
ms.sourcegitcommit: e089c105a48924d8cb42f34d711125b157c3af2e
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="6447d-103">BOM の作成 (2016 年 2 月のみ)</span><span class="sxs-lookup"><span data-stu-id="6447d-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6447d-104">このタスクでは、完成品と半完成品の部品表の構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="6447d-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="6447d-105">これは、BOM 計算シリーズの 4 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="6447d-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="6447d-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="6447d-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="6447d-107">半完成品の BOM の作成</span><span class="sxs-lookup"><span data-stu-id="6447d-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="6447d-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6447d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6447d-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6447d-110">品目番号 BOM_2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="6447d-111">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="6447d-112">[BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-112">Click BOM versions.</span></span>
5. <span data-ttu-id="6447d-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-113">Click New.</span></span>
6. <span data-ttu-id="6447d-114">[BOM と BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="6447d-115">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6447d-116">たとえば、[BOM_2] を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="6447d-117">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-118">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="6447d-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-119">Click OK.</span></span>
10. <span data-ttu-id="6447d-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-120">Click New.</span></span>
11. <span data-ttu-id="6447d-121">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6447d-122">この例では、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="6447d-123">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-124">たとえば、11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="6447d-125">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-125">Click Header.</span></span>
14. <span data-ttu-id="6447d-126">[承認] をクリックして、部品表を承認します。</span><span class="sxs-lookup"><span data-stu-id="6447d-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="6447d-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-127">Click OK.</span></span>
16. <span data-ttu-id="6447d-128">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-128">Click Approve.</span></span>
    * <span data-ttu-id="6447d-129">[承認] ボタンは、[BOM バージョン] セクションのツールバーにあります。</span><span class="sxs-lookup"><span data-stu-id="6447d-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="6447d-130">表示されていない場合は、部品表のページの右上にあるヘッダーをクリックして、[承認] を表示します。</span><span class="sxs-lookup"><span data-stu-id="6447d-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="6447d-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-131">Click OK.</span></span>
18. <span data-ttu-id="6447d-132">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-132">Click Activate.</span></span>
19. <span data-ttu-id="6447d-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-133">Close the page.</span></span>
20. <span data-ttu-id="6447d-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-134">Close the page.</span></span>
21. <span data-ttu-id="6447d-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="6447d-136">完成品の BOM の作成</span><span class="sxs-lookup"><span data-stu-id="6447d-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="6447d-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6447d-138">品目番号 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="6447d-139">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="6447d-140">[BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-140">Click BOM versions.</span></span>
4. <span data-ttu-id="6447d-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-141">Click New.</span></span>
5. <span data-ttu-id="6447d-142">[BOM と BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="6447d-143">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6447d-144">たとえば、[BOM_1] を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="6447d-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-146">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="6447d-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-147">Click OK.</span></span>
9. <span data-ttu-id="6447d-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-148">Click New.</span></span>
10. <span data-ttu-id="6447d-149">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6447d-150">この例では、「ITEM_A」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="6447d-151">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-152">この例では、「11」を選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="6447d-153">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-153">Click New.</span></span>
13. <span data-ttu-id="6447d-154">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6447d-155">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="6447d-156">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-157">たとえば、11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="6447d-158">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-158">Click New.</span></span>
16. <span data-ttu-id="6447d-159">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6447d-160">この例では、「BOM_2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="6447d-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="6447d-161">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6447d-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="6447d-162">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6447d-163">この例では、倉庫 11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6447d-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="6447d-164">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-164">Click Header.</span></span>
20. <span data-ttu-id="6447d-165">[承認] をクリックして、部品表を承認します。</span><span class="sxs-lookup"><span data-stu-id="6447d-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="6447d-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-166">Click OK.</span></span>
22. <span data-ttu-id="6447d-167">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-167">Click Approve.</span></span>
    * <span data-ttu-id="6447d-168">[承認] ボタンは、[BOM バージョン] セクションのツールバーにあります。</span><span class="sxs-lookup"><span data-stu-id="6447d-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="6447d-169">表示されていない場合は、部品表のページの右上にあるヘッダーをクリックして、[承認] を表示します。</span><span class="sxs-lookup"><span data-stu-id="6447d-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="6447d-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-170">Click OK.</span></span>
24. <span data-ttu-id="6447d-171">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6447d-171">Click Activate.</span></span>
25. <span data-ttu-id="6447d-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-172">Close the page.</span></span>
26. <span data-ttu-id="6447d-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-173">Close the page.</span></span>
27. <span data-ttu-id="6447d-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6447d-174">Close the page.</span></span>


