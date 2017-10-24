--- 
title: "発注書のプット アウェイ場所のディレクティブの設定"
description: "この手順では、簡単な場所ディレクティブの設定方法を説明します。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e1e54c807597d4d5ff7370748012cbf28c1c6b
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a><span data-ttu-id="404e7-103">発注書のプット アウェイ場所のディレクティブの設定</span><span class="sxs-lookup"><span data-stu-id="404e7-103">Set up a location directive for purchase order put-away</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="404e7-104">この手順では、簡単な場所ディレクティブの設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="404e7-104">This procedure shows you how to set up a simple location directive.</span></span> <span data-ttu-id="404e7-105">示されている例では、発注書に対して受領した品目をプットする場所を決定するために使用される場所ディレクティブを作成します。</span><span class="sxs-lookup"><span data-stu-id="404e7-105">The example that’s shown creates a location directive to be used to determine where to put items that have been received for a purchase order.</span></span> <span data-ttu-id="404e7-106">このタスク ガイドは、デモ データの会社 USMF で前述のデータを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-106">You can play this task guide with the data mentioned using demo data company USMF.</span></span> <span data-ttu-id="404e7-107">事前条件: 廃棄コードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="404e7-107">Pre-conditions: You need to create a disposition code.</span></span> <span data-ttu-id="404e7-108">この手順では、[ラベル書き換え] という廃棄コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="404e7-108">In this procedure we use a disposition code called Relabel.</span></span> <span data-ttu-id="404e7-109">自身のデータ内で場所のディレクティブを作成する場合は、倉庫と品目に高度な倉庫管理を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="404e7-109">If you’re creating a location directive in your own data, you need to have set up advanced warehouse management for your warehouse and items.</span></span>  <span data-ttu-id="404e7-110">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="404e7-110">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="404e7-111">[倉庫管理] > [設定] > [場所のディレクティブ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="404e7-111">Go to Warehouse management > Setup > Location directives.</span></span>
2. <span data-ttu-id="404e7-112">[ワーク オーダー タイプ] フィールドで「発注書」を選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-112">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-location-directive-header"></a><span data-ttu-id="404e7-113">場所のディレクティブ ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="404e7-113">Create a location directive header</span></span>
1. <span data-ttu-id="404e7-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-114">Click New.</span></span>
2. <span data-ttu-id="404e7-115">[順序番号] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-115">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="404e7-116">これは、選択した作業タイプのために場所のディレクティブを処理する順序です。</span><span class="sxs-lookup"><span data-stu-id="404e7-116">This is the sequence in which the location directive is processed for the selected work type.</span></span> <span data-ttu-id="404e7-117">必要に応じて、その順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-117">You can also modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="404e7-118">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="404e7-119">これは、このディレクティブの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="404e7-119">This is the unique identifier for this directive.</span></span>  
4. <span data-ttu-id="404e7-120">[ワーク タイプ] フィールドで [プット] を選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-120">In the Work type field, select 'Put'.</span></span>
    * <span data-ttu-id="404e7-121">実効する作業のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-121">Select the type of work to be performed.</span></span> <span data-ttu-id="404e7-122">ワーク オーダー タイプが発注書であるディレクティブでは、プットは唯一のサポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="404e7-122">For directive with work order type Purchase order, Put is the only supported value.</span></span>  
5. <span data-ttu-id="404e7-123">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-123">In the Site field, type a value.</span></span>
6. <span data-ttu-id="404e7-124">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="404e7-125">[ディレクティブ コード] を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="404e7-125">Leave the Directive code blank.</span></span>  <span data-ttu-id="404e7-126">ディレクティブ コードを使用して、タイプが [プット] のワークオーダー明細行を特定のディレクティブにリンクします。</span><span class="sxs-lookup"><span data-stu-id="404e7-126">Directive codes are used to link a work order line of type Put to a specific directive.</span></span> <span data-ttu-id="404e7-127">発注書の場合、作業テンプレートが決定される前に、タイプが [プット] のワーク オーダーの最終明細行の位置が解決されます。</span><span class="sxs-lookup"><span data-stu-id="404e7-127">For purchase orders, the location of the last work order line of type Put is resolved before the work template is determined.</span></span> <span data-ttu-id="404e7-128">そのため、作業テンプレートの最終明細行を特定のディレクティブに接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="404e7-128">Therefore it is not possible to connect the last line of a work template to a specific directive.</span></span>   
7. <span data-ttu-id="404e7-129">[廃棄コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-129">In the Disposition code field, type a value.</span></span>
    * <span data-ttu-id="404e7-130">廃棄コードは、場所のディレクティブの使用を制限します。そのため、場所のディレクティブ が使用されるのは、倉庫作業者がモバイル デバイスを使用して品目を登録する際にこの特定の値を入力する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="404e7-130">The Disposition code limits the use of the location directive, so the location directive is only used if the warehouse worker enters this specific value during registration of the item using a mobile device.</span></span>  
8. <span data-ttu-id="404e7-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-131">Click Save.</span></span>

## <a name="edit-the-query-for-directive"></a><span data-ttu-id="404e7-132">ディレクティブのクエリの編集</span><span class="sxs-lookup"><span data-stu-id="404e7-132">Edit the query for directive</span></span>
1. <span data-ttu-id="404e7-133">[クエリの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-133">Click Edit query.</span></span>
    * <span data-ttu-id="404e7-134">このディレクティブは、指定した廃棄コードにより、指定した倉庫に登録した品目に対しての使用を既に制限されています。</span><span class="sxs-lookup"><span data-stu-id="404e7-134">The use of this directive is already limited to be used for items registered in the warehouse that you specified, and with the disposition code that you specified.</span></span> <span data-ttu-id="404e7-135">クエリを使用して他の制約を追加できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-135">You can add other constraints using the query.</span></span>  
2. <span data-ttu-id="404e7-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-136">Click OK.</span></span>

## <a name="add-directive-lines"></a><span data-ttu-id="404e7-137">ディレクティブ明細行の追加</span><span class="sxs-lookup"><span data-stu-id="404e7-137">Add directive lines</span></span>
1. <span data-ttu-id="404e7-138">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-138">Click New.</span></span>
    * <span data-ttu-id="404e7-139">これは、選択した作業タイプのために場所のディレクティブ明細行を処理する順序です。</span><span class="sxs-lookup"><span data-stu-id="404e7-139">This is the sequence in which the location directive lines are processed for the selected work type.</span></span> <span data-ttu-id="404e7-140">必要に応じて、その順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-140">You can also modify the sequence, if needed.</span></span>  
2. <span data-ttu-id="404e7-141">[開始数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-141">In the From quantity field, enter a number.</span></span>
    * <span data-ttu-id="404e7-142">これはディレクティブの明細行が有効な最小数量です。</span><span class="sxs-lookup"><span data-stu-id="404e7-142">This is the lowest quantity that this directive line is valid for.</span></span>  
3. <span data-ttu-id="404e7-143">[上限数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-143">In the To quantity field, enter a number.</span></span>
4. <span data-ttu-id="404e7-144">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-144">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="404e7-145">開始数量から上限数量までの単位が示されます。</span><span class="sxs-lookup"><span data-stu-id="404e7-145">The unit the From quantity and To quantity is expressed in.</span></span> <span data-ttu-id="404e7-146">フィールドを空白のままにすると、品目の在庫単位が使用されます。</span><span class="sxs-lookup"><span data-stu-id="404e7-146">If you leave this field blank the inventory unit from the item is used.</span></span>  
5. <span data-ttu-id="404e7-147">[数量の検索] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-147">In the Locate quantity field, select an option.</span></span>
    * <span data-ttu-id="404e7-148">なし、またはライセンス プレート数量: 各ライセンス プレートに登録されている数量。</span><span class="sxs-lookup"><span data-stu-id="404e7-148">None, or licence plate quantity: The quantity registered on each licence plate.</span></span> <span data-ttu-id="404e7-149">使用されている数量: 登録されているすべての数量。</span><span class="sxs-lookup"><span data-stu-id="404e7-149">Unitized quantity: The entire quantity that’s been registered.</span></span> <span data-ttu-id="404e7-150">残余数量: 発注書明細行で指定された、まだ登録されていない数量。</span><span class="sxs-lookup"><span data-stu-id="404e7-150">Remaining quantity: The quantity that is yet to be registered from the purchase order line.</span></span> <span data-ttu-id="404e7-151">予定数量: 発注書明細行で指定された、合計数量。</span><span class="sxs-lookup"><span data-stu-id="404e7-151">Expected quantity: The total quantity that is specified on the purchase order line.</span></span>  
6. <span data-ttu-id="404e7-152">[単位ごとに制限] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="404e7-152">Check or uncheck the Restrict by unit checkbox.</span></span>
    * <span data-ttu-id="404e7-153">このオプションを選択し、[単位ごとに制限] ページで単位を指定する場合は、測定単位の品目のみが場所に配置できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-153">If you select this option, and specify the unit on the Restrict by unit page, only items with that unit of measurement can be put into the location.</span></span> <span data-ttu-id="404e7-154">たとえば、測定単位が PL (パレット) である場合、パレット内の品目のみが指定された場所に配置できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-154">For example, if the unit of measurement is PL (pallets), only items in pallets can be put into the specified location.</span></span>  
7. <span data-ttu-id="404e7-155">[分割を許可] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="404e7-155">Check or uncheck the Allow split checkbox.</span></span>
    * <span data-ttu-id="404e7-156">これにより、ディレクティブは複数の場所に数量を分割することができます。</span><span class="sxs-lookup"><span data-stu-id="404e7-156">This allows the directive to split the quantity across multiple locations.</span></span>  
8. <span data-ttu-id="404e7-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-157">Click Save.</span></span>

## <a name="restrict-the-directive-line-to-a-specific-unit"></a><span data-ttu-id="404e7-158">ディレクティブ明細行の特定の単位への制限</span><span class="sxs-lookup"><span data-stu-id="404e7-158">Restrict the directive line to a specific unit</span></span>
1. <span data-ttu-id="404e7-159">[単位ごとに制限] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-159">Click Restrict by unit.</span></span>
    * <span data-ttu-id="404e7-160">このボタンは、[単位ごとに制限] チェック ボックスをオンにしてから [保存] を押す場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-160">This button is only available when you press Save after you have selected the Restrict by unit check box.</span></span>  
2. <span data-ttu-id="404e7-161">[単位] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-161">In the Unit field, type a value.</span></span>
3. <span data-ttu-id="404e7-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="404e7-162">Close the page.</span></span>

## <a name="add-a-location-directive-action-line"></a><span data-ttu-id="404e7-163">場所のディレクティブ アクション明細行の追加</span><span class="sxs-lookup"><span data-stu-id="404e7-163">Add a location directive action line</span></span>
1. <span data-ttu-id="404e7-164">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-164">Click New.</span></span>
    * <span data-ttu-id="404e7-165">これは、選択した作業タイプのために場所のディレクティブ アクション明細行を処理する順序です。</span><span class="sxs-lookup"><span data-stu-id="404e7-165">This is the sequence in which the location directive action lines are processed for the selected work type.</span></span> <span data-ttu-id="404e7-166">必要に応じて、その順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-166">You can also modify the sequence, if needed.</span></span>  
2. <span data-ttu-id="404e7-167">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-167">In the Name field, type a value.</span></span>
    * <span data-ttu-id="404e7-168">これは、このディレクティブ アクションの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="404e7-168">This is the unique identifier for this directive action.</span></span>  
3. <span data-ttu-id="404e7-169">[固定の場所の使用] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-169">In the Fixed location usage field, select an option.</span></span>
    * <span data-ttu-id="404e7-170">固定の場所および固定されていない場所: 製品自体の固定の場所と同様に、クエリで指定された範囲内のすべての固定されていない場所は有効です。</span><span class="sxs-lookup"><span data-stu-id="404e7-170">Fixed and non-fixed locations: All non-fixed locations are valid as well as the product’s own fixed location, within the range specified in the query.</span></span>  <span data-ttu-id="404e7-171">製品の固定の場所のみ: 製品の固定の場所は有効であり、すべての製品バリアントの固定の場所のセットは同じです。</span><span class="sxs-lookup"><span data-stu-id="404e7-171">Only fixed location for the product: Fixed locations for the product are valid, and all product variants share the same set of fixed locations.</span></span> <span data-ttu-id="404e7-172">製品バリアントの固定の場所のみ: 各製品バリアントに指定されている固定の場所だけが有効です。</span><span class="sxs-lookup"><span data-stu-id="404e7-172">Only fixed location for the product variants: Only fixed locations specified for each product variant are valid.</span></span>  
4. <span data-ttu-id="404e7-173">[戦略] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="404e7-173">In the Strategy field, select an option.</span></span>
    * <span data-ttu-id="404e7-174">発注書のワーク オーダー タイプは次の戦略をサポートしています: なし: 品目は、見つかった最初の場所に配置されています。</span><span class="sxs-lookup"><span data-stu-id="404e7-174">Work orders of type Purchase order support the following strategies: None: the item is placed at the first location that’s found.</span></span> <span data-ttu-id="404e7-175">連結: 品目は同様の品目が既に利用可能な場所に配置されています。</span><span class="sxs-lookup"><span data-stu-id="404e7-175">Consolidate: The item is placed in a location where similar items are already available.</span></span> <span data-ttu-id="404e7-176">作業を受け取らない空の場所: 品目は見つかった最初の空の場所に配置されています。</span><span class="sxs-lookup"><span data-stu-id="404e7-176">Empty location with no incoming work: the item is placed in the first empty location that’s found.</span></span> <span data-ttu-id="404e7-177">現物在庫がなく、入荷作業が予定されていない場合、その場所は空であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="404e7-177">A location is considered to be empty if it has no physical inventory and no expected incoming work.</span></span>  
5. <span data-ttu-id="404e7-178">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-178">Click Save.</span></span>

## <a name="edit-the-query-for-directive-action-line"></a><span data-ttu-id="404e7-179">ディレクティブ アクション明細行のクエリの編集</span><span class="sxs-lookup"><span data-stu-id="404e7-179">Edit the query for directive action line</span></span>
1. <span data-ttu-id="404e7-180">[クエリの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-180">Click Edit query.</span></span>
2. <span data-ttu-id="404e7-181">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-181">Click Add.</span></span>
3. <span data-ttu-id="404e7-182">[フィールド] フィールドで、「場所プロファイル ID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-182">In the Field field, type 'location profile ID'.</span></span>
    * <span data-ttu-id="404e7-183">この例では、場所のプロファイル ID を使用して可能な場所を制限します。</span><span class="sxs-lookup"><span data-stu-id="404e7-183">In this example, we’ll restrict the possible locations using a location profile ID.</span></span>  
4. <span data-ttu-id="404e7-184">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="404e7-184">In the Criteria field, type a value.</span></span>
5. <span data-ttu-id="404e7-185">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="404e7-185">Click OK.</span></span>
    * <span data-ttu-id="404e7-186">倉庫のすべての可能なシナリオが対象となるまで、ディレクティブ明細行とディレクティブ アクションの追加を続行できます。</span><span class="sxs-lookup"><span data-stu-id="404e7-186">You can continue to add directive lines and directive actions until you have covered all the possible scenarios in your warehouse.</span></span>  


