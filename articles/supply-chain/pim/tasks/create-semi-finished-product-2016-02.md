---
title: 半完成品の作成 (2016 年 2 月)
description: このタスクでは、半完成品の作成に重点を置きます。
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
ms.openlocfilehash: 39fb652d704da33d24a206da2c18cc2a7a50e9e4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844516"
---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="2cae4-103">半完成品の作成 (2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="2cae4-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cae4-104">このタスクでは、半完成品の作成に重点を置きます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="2cae4-105">これは、BOM 計算シリーズの 2 番目のタスクです。</span><span class="sxs-lookup"><span data-stu-id="2cae4-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="2cae4-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="2cae4-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2cae4-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2cae4-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-108">Click New.</span></span>
3. <span data-ttu-id="2cae4-109">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="2cae4-110">この例では、「BOM_2」を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="2cae4-111">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-112">[STD] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-112">Select STD.</span></span> <span data-ttu-id="2cae4-113">STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。</span><span class="sxs-lookup"><span data-stu-id="2cae4-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="2cae4-114">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-115">たとえば、「AUDIO」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-115">For example, select Audio.</span></span> <span data-ttu-id="2cae4-116">これは原価計算には影響しません。</span><span class="sxs-lookup"><span data-stu-id="2cae4-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="2cae4-117">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-118">「SiteWH」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-118">Select SiteWH.</span></span> <span data-ttu-id="2cae4-119">この例では、サイトと倉庫のみが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="2cae4-120">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-121">追跡用分析コードはこの例には使用されません。「なし」を選択してください。</span><span class="sxs-lookup"><span data-stu-id="2cae4-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="2cae4-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-122">Click OK.</span></span>
9. <span data-ttu-id="2cae4-123">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="2cae4-124">[既定の注文設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-124">Click Default order settings.</span></span>
11. <span data-ttu-id="2cae4-125">[既定の注文タイプ] フィールドで、「生産」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="2cae4-126">これは生成される半完成品であるので、「生産」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="2cae4-127">[購買サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-128">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="2cae4-129">[在庫サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-130">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="2cae4-131">[販売サイト] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-132">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="2cae4-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-133">Close the page.</span></span>
16. <span data-ttu-id="2cae4-134">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="2cae4-135">品目価格をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-135">Click Item price.</span></span>
18. <span data-ttu-id="2cae4-136">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-136">Click New.</span></span>
19. <span data-ttu-id="2cae4-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="2cae4-138">[バージョン] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-139">この例では、「バージョン 10」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="2cae4-140">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-141">この例では、「サイト 1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="2cae4-142">単価を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="2cae4-143">たとえば、原価価格 10 を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="2cae4-144">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-144">Click Save.</span></span>
24. <span data-ttu-id="2cae4-145">[保留中の価格の有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cae4-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="2cae4-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-146">Close the page.</span></span>
26. <span data-ttu-id="2cae4-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-147">Close the page.</span></span>
27. <span data-ttu-id="2cae4-148">[BOM_2] をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="2cae4-149">[原価の管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="2cae4-150">[原価グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="2cae4-151">この例では、原価グループ M1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="2cae4-152">レコードを保存するショートカットを使用します。</span><span class="sxs-lookup"><span data-stu-id="2cae4-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="2cae4-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2cae4-153">Close the page.</span></span>

