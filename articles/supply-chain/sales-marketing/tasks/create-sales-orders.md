---
title: 販売注文を作成する。
description: この手順では、販売注文を作成する方法を示します。
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 630e82f737adf2a2c694ba4d6c046f0ae02f2696
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260458"
---
# <a name="create-sales-orders"></a><span data-ttu-id="43098-103">販売注文を作成する。</span><span class="sxs-lookup"><span data-stu-id="43098-103">Create sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43098-104">この手順では、販売注文を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="43098-104">This procedure shows you how to create a sales order.</span></span> <span data-ttu-id="43098-105">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="43098-105">You can use the procedure in demo data company USMF.</span></span> <span data-ttu-id="43098-106">販売注文は通常、販売注文プロセッサによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="43098-106">Sales orders are typically created by a sales order processor.</span></span> 

## <a name="enter-sales-order-header-details"></a><span data-ttu-id="43098-107">販売注文ヘッダーの詳細を入力</span><span class="sxs-lookup"><span data-stu-id="43098-107">Enter sales order header details</span></span>
1. <span data-ttu-id="43098-108">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 販売注文 > すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="43098-108">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="43098-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-109">Select **New**.</span></span>
3. <span data-ttu-id="43098-110">**顧客口座** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="43098-110">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="43098-111">一覧で、顧客のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-111">In the list, find and select the customer record.</span></span>
    - <span data-ttu-id="43098-112">この例では、顧客 ID「DE-004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-112">For this example, select customer number US-004.</span></span>  
5. <span data-ttu-id="43098-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-113">Select **OK**.</span></span>

## <a name="enter-sales-order-line-details"></a><span data-ttu-id="43098-114">販売注文ヘッダーの明細行を入力</span><span class="sxs-lookup"><span data-stu-id="43098-114">Enter sales order line details</span></span>
    
<span data-ttu-id="43098-115">組織で販売される製品は、構成、色、サイズ、スタイルなどの分析コードによって差別化されたバリアントが展開されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="43098-115">The products sold by your organization may come in variants differentiated by dimensions, such as configuration, color, size, and style.</span></span> <span data-ttu-id="43098-116">また製品には、サイト、倉庫、パレットなどの保管分析コードや、バッチ番号、シリアル番号などのトラッキング分析コードが設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="43098-116">Also, products may be set up to use storage dimensions, such as site, warehouse, and pallet, and tracking dimensions, such as batch and serial numbers.</span></span> <span data-ttu-id="43098-117">これらの分析コードが割り当てられていると、注文明細行でこれらの分析コードの値を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43098-117">When these dimensions are assigned, you must select the values for those dimensions on the order line.</span></span> <span data-ttu-id="43098-118">注文入力の効率を向上させるために、注文のグリッドに個々の分析コードのフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="43098-118">To improve order entry efficiency, you may want to add the respective dimension fields to the order grid.</span></span>
    
1. <span data-ttu-id="43098-119">**販売注文明細行** セクションで、**販売注文明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-119">Under the **Sales order lines** section, select the **Sales order line**.</span></span>
2. <span data-ttu-id="43098-120">**分析コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-120">Select **Dimensions**.</span></span>
    
    <span data-ttu-id="43098-121">この例では、[色]、[サイト]、および [倉庫] の分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-121">For this example, select the Color, Site and Warehouse dimensions.</span></span> <span data-ttu-id="43098-122">ここで選択した分析コードは、販売注文グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="43098-122">The dimensions you select here will appear in the sales order grid.</span></span> <span data-ttu-id="43098-123">選択を保持する場合は、**設定の保存** オプションを「はい」に設定します。</span><span class="sxs-lookup"><span data-stu-id="43098-123">If you want your selections to persist, set the **Save setup** option to Yes.</span></span>
    
3. <span data-ttu-id="43098-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-124">Select **OK**.</span></span>
4. <span data-ttu-id="43098-125">**品目番号** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="43098-125">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="43098-126">この例では、品目番号「T0004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-126">For this example, select item number T0004.</span></span>
    - <span data-ttu-id="43098-127">品目が販売カテゴリの一部である場合、品目名は、[販売カテゴリ] フィールドに自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="43098-127">If the item is part of a sales category, the item name will automatically appear in the Sales category field.</span></span>  
    - <span data-ttu-id="43098-128">製品分析コードのフィールドに既に値がある場合、それは既定の製品分析コードとして定義されている製品レコードから値がコピーされたことによります。</span><span class="sxs-lookup"><span data-stu-id="43098-128">If product dimension fields already contain a value, this is because the value was copied from the product record where it is defined as a default product dimension.</span></span> <span data-ttu-id="43098-129">既定値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="43098-129">You can change the default value at any time.</span></span>   
6. <span data-ttu-id="43098-130">**色** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="43098-130">In the **Color** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="43098-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="43098-132">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43098-132">In the **Quantity** field, enter a number.</span></span>
    - <span data-ttu-id="43098-133">品目が購買時、生産時、保管時と異なる単位で販売され、かつ販売単位が製品レコードで設定されている場合、この値は **単位** フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="43098-133">If the item is sold in different units than when it's purchased, produced, and stored, and a sales unit of measure is set on the product record, this value will be shown in the **Unit** field.</span></span> <span data-ttu-id="43098-134">この値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="43098-134">You can change the value at any time.</span></span>   
    - <span data-ttu-id="43098-135">**サイト** フィールドに既に値が含まれる場合、その値は製品に関連付けられている注文ヘッダーまたは注文設定からコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="43098-135">If the **Site** field already contains a value, the value was copied from the order header or from the order settings that are associated with the product.</span></span> <span data-ttu-id="43098-136">この値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="43098-136">You can change the value at any time.</span></span> <span data-ttu-id="43098-137">そのフィールドが空の場合、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43098-137">If the field is empty, select a value.</span></span>   
    - <span data-ttu-id="43098-138">**単価** フィールドに既に値が含まれる場合、その値は有効な売買契約または製品レコードからコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="43098-138">If the **Unit price** field already contains a value, the value was copied from a valid trade agreement, or from the product record.</span></span> <span data-ttu-id="43098-139">(単価は、販売契約書から取得することもできますが、販売契約書から販売注文を作成するプロセスはここで示したものと異なります。) そのフィールドが空の場合、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43098-139">(The unit price can also originate from a sales agreement, but the process for creating sales orders from sales agreements is different to the one shown here.) If the field is empty, enter a value.</span></span>   
    - <span data-ttu-id="43098-140">**割引** フィールドでは、製品の単位あたりの割引金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="43098-140">The **Discount** field contains a discount amount per product unit.</span></span> <span data-ttu-id="43098-141">合計行割引金額の計算は、割引値と明細行数量の乗算により行われます。</span><span class="sxs-lookup"><span data-stu-id="43098-141">To calculate the total line discount amount, the discount value is multiplied by line quantity.</span></span> <span data-ttu-id="43098-142">**割引** フィールドに既に値が含まれる場合、その値は有効な売買契約からコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="43098-142">If the **Discount** field already contains a value, the value was copied from a valid trade agreement.</span></span> <span data-ttu-id="43098-143">このフィールドが空で、顧客に行割引を提供する場合は、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43098-143">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    - <span data-ttu-id="43098-144">**割引率** フィールドには、明細合計総額を割り引くパーセンテージ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="43098-144">The **Discount percent** field contains a percentage value by which the total line gross amount is to be reduced.</span></span>  <span data-ttu-id="43098-145">**割引率** フィールドに既に値が含まれる場合、それは有効な売買契約からコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="43098-145">If the **Discount percent** field already contains a value, it was copied from a valid trade agreement.</span></span> <span data-ttu-id="43098-146">このフィールドが空で、顧客に行割引を提供する場合は、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="43098-146">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span> 
    - <span data-ttu-id="43098-147">**正味** 金額フィールドには、明細行の数量および単位価格に基づいて計算され、割引によって調整された値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="43098-147">The **Net** amount field contains a value that is calculated based on the line's quantity and unit price adjusted by discounts.</span></span>  <span data-ttu-id="43098-148">計算済の値を、別の金額で上書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="43098-148">You can override the calculated value to a different one.</span></span>  

## <a name="review-the-order-totals"></a><span data-ttu-id="43098-149">注文合計の確認</span><span class="sxs-lookup"><span data-stu-id="43098-149">Review the order totals</span></span>
1. <span data-ttu-id="43098-150">**アクション ウィンドウ** で、**販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-150">On the **Action Pane**, select **Sales order**.</span></span>
2. <span data-ttu-id="43098-151">**合計** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-151">Select **Totals**.</span></span>
    
    <span data-ttu-id="43098-152">**合計** ページは、注文全体に関する詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="43098-152">The **Totals** page displays details about the entire order.</span></span> <span data-ttu-id="43098-153">これには、小計金額が含まれます。小計金額は、明細行割引を加味して調整された明細行の正味金額、注文レベルの割引を加味して調整済の合計請求金額、手数料、売上税、顧客の与信限度額の条件、およびその他の金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="43098-153">This includes the subtotal amount, which is a sum of all line net amounts adjusted for eventual line discounts, the total invoice amount, which is a subtotal amount adjusted for eventual order-level discount, charges, and sales tax, the customer credit limit situation, and more.</span></span> <span data-ttu-id="43098-154">請求金額は、顧客の請求書に表示される金額です。</span><span class="sxs-lookup"><span data-stu-id="43098-154">The invoice amount is the amount that will appear on the customer's invoice document.</span></span>  
    
3. <span data-ttu-id="43098-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="43098-155">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]