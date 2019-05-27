---
title: BOM の作成 (2016 年 2 月)
description: このタスクでは、完成品と半完成品の部品表の構造の作成について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568561"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="b2546-103">BOM の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="b2546-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2546-104">このタスクでは、完成品と半完成品の部品表の構造の作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="b2546-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="b2546-105">これは、BOM 計算シリーズの 4 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="b2546-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="b2546-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b2546-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="b2546-107">半完成品の BOM の作成</span><span class="sxs-lookup"><span data-stu-id="b2546-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="b2546-108">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2546-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b2546-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2546-110">品目番号 BOM_2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="b2546-111">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="b2546-112">[BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-112">Click BOM versions.</span></span>
5. <span data-ttu-id="b2546-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-113">Click New.</span></span>
6. <span data-ttu-id="b2546-114">[BOM と BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="b2546-115">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b2546-116">たとえば、[BOM_2] を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="b2546-117">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-118">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="b2546-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-119">Click OK.</span></span>
10. <span data-ttu-id="b2546-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-120">Click New.</span></span>
11. <span data-ttu-id="b2546-121">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b2546-122">この例では、「ITEM_C」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="b2546-123">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-124">たとえば、11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="b2546-125">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-125">Click Header.</span></span>
14. <span data-ttu-id="b2546-126">[承認] をクリックして、部品表を承認します。</span><span class="sxs-lookup"><span data-stu-id="b2546-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="b2546-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-127">Click OK.</span></span>
16. <span data-ttu-id="b2546-128">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-128">Click Approve.</span></span>
    * <span data-ttu-id="b2546-129">[承認] ボタンは、[BOM バージョン] セクションのツールバーにあります。</span><span class="sxs-lookup"><span data-stu-id="b2546-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="b2546-130">表示されていない場合は、部品表のページの右上にあるヘッダーをクリックして、[承認] を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2546-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="b2546-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-131">Click OK.</span></span>
18. <span data-ttu-id="b2546-132">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-132">Click Activate.</span></span>
19. <span data-ttu-id="b2546-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-133">Close the page.</span></span>
20. <span data-ttu-id="b2546-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-134">Close the page.</span></span>
21. <span data-ttu-id="b2546-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="b2546-136">完成品の BOM の作成</span><span class="sxs-lookup"><span data-stu-id="b2546-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="b2546-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b2546-138">品目番号 BOM_1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="b2546-139">アクション ペインで、[エンジニア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="b2546-140">[BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-140">Click BOM versions.</span></span>
4. <span data-ttu-id="b2546-141">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-141">Click New.</span></span>
5. <span data-ttu-id="b2546-142">[BOM と BOM バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="b2546-143">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b2546-144">たとえば、[BOM_1] を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="b2546-145">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-146">たとえば、サイト 1 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="b2546-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-147">Click OK.</span></span>
9. <span data-ttu-id="b2546-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-148">Click New.</span></span>
10. <span data-ttu-id="b2546-149">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b2546-150">この例では、「ITEM_A」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="b2546-151">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-152">この例では、「11」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="b2546-153">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-153">Click New.</span></span>
13. <span data-ttu-id="b2546-154">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b2546-155">この例では、「ITEM_B」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="b2546-156">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-157">たとえば、11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="b2546-158">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-158">Click New.</span></span>
16. <span data-ttu-id="b2546-159">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b2546-160">この例では、「BOM_2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2546-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="b2546-161">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2546-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="b2546-162">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b2546-163">この例では、倉庫 11 を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2546-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="b2546-164">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-164">Click Header.</span></span>
20. <span data-ttu-id="b2546-165">[承認] をクリックして、部品表を承認します。</span><span class="sxs-lookup"><span data-stu-id="b2546-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="b2546-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-166">Click OK.</span></span>
22. <span data-ttu-id="b2546-167">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-167">Click Approve.</span></span>
    * <span data-ttu-id="b2546-168">[承認] ボタンは、[BOM バージョン] セクションのツールバーにあります。</span><span class="sxs-lookup"><span data-stu-id="b2546-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="b2546-169">表示されていない場合は、部品表のページの右上にあるヘッダーをクリックして、[承認] を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2546-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="b2546-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-170">Click OK.</span></span>
24. <span data-ttu-id="b2546-171">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2546-171">Click Activate.</span></span>
25. <span data-ttu-id="b2546-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-172">Close the page.</span></span>
26. <span data-ttu-id="b2546-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-173">Close the page.</span></span>
27. <span data-ttu-id="b2546-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2546-174">Close the page.</span></span>

