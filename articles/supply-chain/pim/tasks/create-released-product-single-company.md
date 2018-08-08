--- 
title: "1 つの会社に対するリリース済製品の作成"
description: "この手順は、1 つの法人単位のコンテキストでリリース済製品を 1 つ作成する方法を説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3449952684d557f410f9b5b9410f94197e12c897
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="98cb2-103">1 つの会社に対するリリース済製品の作成</span><span class="sxs-lookup"><span data-stu-id="98cb2-103">Create a released product for a single company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98cb2-104">この手順は、1 つの法人単位のコンテキストでリリース済製品を 1 つ作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="98cb2-105">リリース済製品を作成したら、すぐにこの単位のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="98cb2-106">デモ データの会社 USMF でこの手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="98cb2-107">このタスクは、通常、製品デザイナーが実行します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="98cb2-108">リリース済製品の作成</span><span class="sxs-lookup"><span data-stu-id="98cb2-108">Create a released product</span></span>
1. <span data-ttu-id="98cb2-109">[リリースされた製品] に進みます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-109">Go to Released products.</span></span>
2. <span data-ttu-id="98cb2-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-110">Click New.</span></span>
3. <span data-ttu-id="98cb2-111">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="98cb2-112">製品番号が [製品番号] フィールドに自動的に入力されない場合、一意の製品番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="98cb2-113">この手順が必要となるのは、番号順序が製品番号に対して設定されていない場合に限られます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="98cb2-114">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="98cb2-115">製品名が検索名の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="98cb2-116">必要に応じて、検索名の変更を選択できます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="98cb2-117">[品目モデル グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-118">品目モデル グループには、品目の入庫および出庫時における品目の管理方法および処理方法を決定する設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98cb2-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="98cb2-119">この設定は、品目の消費の計算方法も決定します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="98cb2-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="98cb2-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="98cb2-122">[品目グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-123">品目グループは、在庫品目を品目の特性に基づいて分類して管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="98cb2-124">たとえば、主要な勘定への情報の転記方法を管理するため、特定の重要な勘定に関連付けられている一連の異なる品目グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="98cb2-125">これにより、さまざまなステージで品目の在庫値を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="98cb2-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="98cb2-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="98cb2-128">[保管分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-129">保管分析コードは、品目の保管方法と在庫からの取得方法を管理できます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="98cb2-130">たとえば、保管分析コードにはサイトと倉庫があります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="98cb2-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="98cb2-132">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="98cb2-133">[追跡用分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-134">追跡用分析コード グループにより、製品に追加できる追跡用分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="98cb2-135">たとえば、バッチ番号とシリアル番号は、在庫品目を追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="98cb2-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="98cb2-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="98cb2-138">[在庫単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-139">在庫単位により、在庫に保管される場合の製品の数量化方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="98cb2-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="98cb2-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="98cb2-142">[購買単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-143">購買単位により、仕入先から購入される場合の製品の数量化方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="98cb2-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="98cb2-145">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="98cb2-146">[販売単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-147">販売単位により、顧客に販売する場合の製品の数量化方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="98cb2-148">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="98cb2-149">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="98cb2-150">[BOM 単位] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-151">BOM 単位により、部品表 (BOM) に含める場合の製品の数量化方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="98cb2-152">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="98cb2-153">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="98cb2-154">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-155">売上税の課税グループの品目売上税グループにより、品目ごとの売上税の計算方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="98cb2-156">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="98cb2-157">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="98cb2-158">[品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="98cb2-159">購買税グループの品目売上税グループにより、品目ごとの購買税の計算方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="98cb2-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="98cb2-160">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="98cb2-161">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="98cb2-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="98cb2-163">製品の特性の追加</span><span class="sxs-lookup"><span data-stu-id="98cb2-163">Add product characteristics</span></span>
1. <span data-ttu-id="98cb2-164">[在庫の管理] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="98cb2-165">[正味重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="98cb2-166">[風袋重量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="98cb2-167">[全体の奥行き] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="98cb2-168">[全体の幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="98cb2-169">[全体の高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="98cb2-170">[容積] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="98cb2-171">財務分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="98cb2-171">Add financial dimensions</span></span>
1. <span data-ttu-id="98cb2-172">[財務分析コード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="98cb2-173">[BusinessUnit] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="98cb2-174">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="98cb2-175">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98cb2-176">[CostCenter] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="98cb2-177">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="98cb2-178">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="98cb2-179">[部門] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="98cb2-180">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="98cb2-181">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="98cb2-182">[ItemGroup] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="98cb2-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="98cb2-183">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98cb2-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="98cb2-184">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98cb2-184">In the list, click the link in the selected row.</span></span>


