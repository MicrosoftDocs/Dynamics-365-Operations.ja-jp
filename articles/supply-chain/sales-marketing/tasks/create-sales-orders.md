--- 
title: "販売注文を作成する。"
description: "この手順では、販売注文を作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 65a91c64c7a622fda2e2358b3a2d46cb05b9bf3a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-sales-orders"></a><span data-ttu-id="60fee-103">販売注文を作成する。</span><span class="sxs-lookup"><span data-stu-id="60fee-103">Create sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60fee-104">この手順では、販売注文を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="60fee-104">This procedure shows you how to create a sales order.</span></span> <span data-ttu-id="60fee-105">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="60fee-105">You can use the procedure in demo data company USMF.</span></span> <span data-ttu-id="60fee-106">販売注文は通常、販売注文プロセッサによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="60fee-106">Sales orders are typically created by a sales order processor.</span></span> 




## <a name="enter-sales-order-header-details"></a><span data-ttu-id="60fee-107">販売注文ヘッダーの詳細を入力</span><span class="sxs-lookup"><span data-stu-id="60fee-107">Enter sales order header details</span></span>
1. <span data-ttu-id="60fee-108">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="60fee-108">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="60fee-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-109">Click New.</span></span>
3. <span data-ttu-id="60fee-110">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="60fee-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="60fee-111">一覧で、顧客のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="60fee-111">In the list, find and select the customer record.</span></span>
    * <span data-ttu-id="60fee-112">この例では、顧客 ID「DE-004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="60fee-112">For this example, select customer number US-004.</span></span>  
5. <span data-ttu-id="60fee-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="60fee-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-114">Click OK.</span></span>

## <a name="enter-sales-order-line-details"></a><span data-ttu-id="60fee-115">販売注文ヘッダーの明細行を入力</span><span class="sxs-lookup"><span data-stu-id="60fee-115">Enter sales order line details</span></span>
    * <span data-ttu-id="60fee-116">組織で販売される製品は、構成、色、サイズ、スタイルなどの分析コードによって差別化されたバリアントが展開されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="60fee-116">The products sold by your organization may come in variants differentiated by dimensions, such as configuration, color, size, and style.</span></span> <span data-ttu-id="60fee-117">また製品には、サイト、倉庫、パレットなどの保管分析コードや、バッチ番号、シリアル番号などのラッキング分析コードが設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="60fee-117">Also, products may be set up to use storage dimensions, such as site, warehouse, and pallet, and racking dimensions, such as batch and serial numbers.</span></span> <span data-ttu-id="60fee-118">これらの分析コードが割り当てられていると、注文明細行でこれらの分析コードの値を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60fee-118">When these dimensions are assigned, you must select the values for those dimensions on the order line.</span></span> <span data-ttu-id="60fee-119">注文入力の効率を向上させるために、注文のグリッドに個々の分析コードのフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="60fee-119">To improve order entry efficiency, you may want to add the respective dimension fields to the order grid.</span></span>  
1. <span data-ttu-id="60fee-120">[販売注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-120">Click Sales order line.</span></span>
2. <span data-ttu-id="60fee-121">[分析コード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-121">Click Dimensions.</span></span>
    * <span data-ttu-id="60fee-122">この例では、[色]、[サイト]、および [倉庫] の分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="60fee-122">For this example, select the Color, Site and Warehouse dimensions.</span></span> <span data-ttu-id="60fee-123">ここで選択した分析コードは、販売注文グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="60fee-123">The dimensions you select here will appear in the sales order grid.</span></span> <span data-ttu-id="60fee-124">選択を保持する場合は、[設定の保存] オプションに [はい] を設定します。</span><span class="sxs-lookup"><span data-stu-id="60fee-124">If you want your selections to persist, set the Save setup option to Yes.</span></span>   
3. <span data-ttu-id="60fee-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-125">Click OK.</span></span>
4. <span data-ttu-id="60fee-126">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="60fee-126">In the Item number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="60fee-127">この例では、品目番号「T0004」を選択します。</span><span class="sxs-lookup"><span data-stu-id="60fee-127">For this example, select item number T0004.</span></span>
6. <span data-ttu-id="60fee-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="60fee-129">品目が販売カテゴリの一部である場合、品目名は、[販売カテゴリ] フィールドに自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="60fee-129">If the item is part of a sales category, the item name will automatically appear in the Sales category field.</span></span>  
    * <span data-ttu-id="60fee-130">製品分析コードのフィールドに既に値がある場合、それは既定の製品分析コードとして定義されている製品レコードから値がコピーされたことによります。</span><span class="sxs-lookup"><span data-stu-id="60fee-130">If product dimension fields already contain a value, this is because the value was copied from the product record where it is defined as a default product dimension.</span></span> <span data-ttu-id="60fee-131">既定値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="60fee-131">You can change the default value at any time.</span></span>   
7. <span data-ttu-id="60fee-132">[色] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="60fee-132">In the Color field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="60fee-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="60fee-133">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="60fee-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-134">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="60fee-135">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60fee-135">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="60fee-136">購買時、生産時、保管時と異なる単位で品目を販売する場合、かつ販売単位が製品レコードで設定されている場合、この値は [単位] フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="60fee-136">If the item is sold in different units than when it’s purchased, produced, and stored, and a sales unit of measure is set on the product record, this value will be shown in the Unit field.</span></span> <span data-ttu-id="60fee-137">この値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="60fee-137">You can change the value at any time.</span></span>   
    * <span data-ttu-id="60fee-138">[サイト] フィールドに既に値が含まれる場合、それは製品で関連付けられる注文ヘッダーまたは注文設定から値がコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="60fee-138">If the Site field already contains a value, the value was copied from the order header or from the order settings that are associated with the product.</span></span> <span data-ttu-id="60fee-139">この値はいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="60fee-139">You can change the value at any time.</span></span> <span data-ttu-id="60fee-140">そのフィールドが空の場合、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60fee-140">If the field is empty, select a value.</span></span>   
    * <span data-ttu-id="60fee-141">[単価] フィールドに既に値が含まれる場合、それは有効な売買契約または製品レコードから値がコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="60fee-141">If the Unit price field already contains a value, the value was copied from a valid trade agreement, or from the product record.</span></span> <span data-ttu-id="60fee-142">(単価は、販売契約書から取得することもできますが、販売契約書から販売注文を作成するプロセスはここで示したものと異なります。) そのフィールドが空の場合、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60fee-142">(The unit price can also originate from a sales agreement, but the process for creating sales orders from sales agreements is different to the one shown here.) If the field is empty, enter a value.</span></span>   
    * <span data-ttu-id="60fee-143">[割引] フィールドでは、製品の単位あたりの割引金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="60fee-143">The Discount field contains a discount amount per product unit.</span></span> <span data-ttu-id="60fee-144">合計行割引金額の計算は、割引値と明細行数量の乗算により行われます。</span><span class="sxs-lookup"><span data-stu-id="60fee-144">To calculate the total line discount amount, the discount value is multiplied by line quantity.</span></span>    <span data-ttu-id="60fee-145">[割引] フィールドに既に値が含まれる場合、それは有効な売買契約から値がコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="60fee-145">If the Discount field already contains a value, the value was copied from a valid trade agreement.</span></span> <span data-ttu-id="60fee-146">このフィールドが空で、顧客に行割引を提供する場合は、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60fee-146">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="60fee-147">[割引率] フィールドには、明細合計総額を割り引くパーセンテージ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="60fee-147">The Discount percent field contains a percentage value by which the total line gross amount is to be reduced.</span></span>  <span data-ttu-id="60fee-148">[割引率] フィールドに既に値が含まれる場合、それは有効な売買契約からコピーされたものです。</span><span class="sxs-lookup"><span data-stu-id="60fee-148">If the Discount percent field already contains a value, it was copied from a valid trade agreement.</span></span> <span data-ttu-id="60fee-149">このフィールドが空で、顧客に行割引を提供する場合は、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60fee-149">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="60fee-150">[正味金額] フィールドの値には、明細行の数量および単位価格に基づいて計算され、割引によって調整された値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="60fee-150">The Net amount field contains a value that is calculated based on the line's quantity and unit price adjusted by discounts.</span></span>  <span data-ttu-id="60fee-151">計算済の値を、別の金額で上書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="60fee-151">You can override the calculated value to a different one.</span></span>  

## <a name="review-the-order-totals"></a><span data-ttu-id="60fee-152">注文合計の確認</span><span class="sxs-lookup"><span data-stu-id="60fee-152">Review the order totals</span></span>
1. <span data-ttu-id="60fee-153">アクション ウィンドウで、[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-153">On the Action Pane, click Sales order.</span></span>
2. <span data-ttu-id="60fee-154">[合計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-154">Click Totals.</span></span>
    * <span data-ttu-id="60fee-155">[合計] ページは、注文全体に関する詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="60fee-155">The Totals page displays details about the entire order.</span></span> <span data-ttu-id="60fee-156">これには、小計金額が含まれます。小計金額は、明細行割引を加味して調整された明細行の正味金額、注文レベルの割引を加味して調整済の合計請求金額、手数料、売上税、顧客の与信限度額の条件、およびその他の金額の合計です。</span><span class="sxs-lookup"><span data-stu-id="60fee-156">This includes the subtotal amount, which is a sum of all line net amounts adjusted for eventual line discounts, the total invoice amount, which is a subtotal amount adjusted for eventual order-level discount, charges, and sales tax, the customer credit limit situation, and more.</span></span>  <span data-ttu-id="60fee-157">請求金額は、顧客の請求書に表示される金額です。</span><span class="sxs-lookup"><span data-stu-id="60fee-157">The invoice amount is the amount that will appear on the customer's invoice document.</span></span>  
3. <span data-ttu-id="60fee-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60fee-158">Click OK.</span></span>


