--- 
title: "配送スケジュールの作成"
description: "この手順は、販売注文の配送スケジュールを作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 956edeac33f8531ecebef64301f2318333000429
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="865fc-103">配送スケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="865fc-103">Create a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="865fc-104">この手順は、販売注文の配送スケジュールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="865fc-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="865fc-105">配送スケジュールは、注文または見積書の数量を複数の出荷で配送する要求があるときにに使用されます。</span><span class="sxs-lookup"><span data-stu-id="865fc-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="865fc-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="865fc-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="865fc-107">配送スケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="865fc-107">Create delivery schedule</span></span>
1. <span data-ttu-id="865fc-108">[すべての販売注文] に移動します。</span><span class="sxs-lookup"><span data-stu-id="865fc-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="865fc-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-109">Click New.</span></span>
3. <span data-ttu-id="865fc-110">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="865fc-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="865fc-111">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-111">Click OK.</span></span>
5. <span data-ttu-id="865fc-112">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="865fc-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="865fc-113">[数量] フィールドに、1 より大きい数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="865fc-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="865fc-114">[販売注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-114">Click Sales order line.</span></span>
8. <span data-ttu-id="865fc-115">[配送スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="865fc-116">[配送スケジュール] ページは、顧客に注文明細行の合計数量を配送するための出荷数を指定できる場所です。</span><span class="sxs-lookup"><span data-stu-id="865fc-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="865fc-117">既定では、システムは最初の配送スケジュール行に元の販売注文明細行の合計数量とそのほかの詳細をコピーします。</span><span class="sxs-lookup"><span data-stu-id="865fc-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="865fc-118">この例では、出荷日に 1 週間の間隔のある 2 つの出荷スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="865fc-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="865fc-119">[数量] フィールドに、合計数量を構成する数を入力します。</span><span class="sxs-lookup"><span data-stu-id="865fc-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="865fc-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-120">Click New.</span></span>
11. <span data-ttu-id="865fc-121">[数量] フィールドに、残りの数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="865fc-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="865fc-122">[出荷予定日] フィールドで、最初の配送明細行の日付の 1 週間後の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="865fc-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="865fc-123">[諸費用の変換] クイック タブの 2 つのオプションは、元の注文明細行に割り当てられた後に、諸費用を配送スケジュール行に配分する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="865fc-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="865fc-124">[総額をコピー] を選択すると、同じ請求金額が各行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="865fc-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="865fc-125">[配送ラインに割り当て] オプションを選択すると、出荷明細行に請求金額を均等に分割します。</span><span class="sxs-lookup"><span data-stu-id="865fc-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="865fc-126">固定費用のみが分割され、変動請求金額は引き続き明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="865fc-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="865fc-127">ページを更新するには、2 番目の配送明細行からカーソルを離します。</span><span class="sxs-lookup"><span data-stu-id="865fc-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="865fc-128">[合計] および [残余] フィールドを見ると、配送スケジュール行に割り当てられた合計数量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="865fc-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="865fc-129">残余数量がゼロの場合、元の明細行の全数量がスケジュールに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="865fc-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="865fc-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-130">Click OK.</span></span>
    * <span data-ttu-id="865fc-131">これで、配送スケジュールが注文明細行にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="865fc-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="865fc-132">元の注文明細行、つまり業務行は、複数の配送を含む注文明細行に変換されています。</span><span class="sxs-lookup"><span data-stu-id="865fc-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="865fc-133">これは、専用のアイコンで表示され、出荷明細行のヘッダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="865fc-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="865fc-134">2 つの新しい明細行、つまり配送明細行は、1 つの配送スケジュールを構成します。</span><span class="sxs-lookup"><span data-stu-id="865fc-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="865fc-135">注文は、元の明細行ではなく、これらの明細行について処理されます。</span><span class="sxs-lookup"><span data-stu-id="865fc-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="865fc-136">確認伝票、ピッキング リスト、梱包明細、請求書などのドキュメントを印刷する場合、配送明細行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="865fc-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="865fc-137">配送明細行が配送日、数量、配送配送のモード、および保管分析コード (サイトおよび倉庫などの) で異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="865fc-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="865fc-138">ただし、製品分析コードは、業務行に常に一致する必要があり、変更できません。</span><span class="sxs-lookup"><span data-stu-id="865fc-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="865fc-139">[数量] フィールドに、現在の値より大きい数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="865fc-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="865fc-140">業務行を選択すると、数量の再計算の影響を確認できます。</span><span class="sxs-lookup"><span data-stu-id="865fc-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="865fc-141">アクション ウィンドウで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="865fc-142">[梱包明細の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="865fc-143">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="865fc-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="865fc-144">[数量] フィールドで、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="865fc-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="865fc-145">梱包明細は、元の注文明細行に対してではなく、2 つの配送スケジュール行に対して作成されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="865fc-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="865fc-146">[梱包明細の印刷] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="865fc-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="865fc-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-147">Click OK.</span></span>
23. <span data-ttu-id="865fc-148">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="865fc-148">Click Yes.</span></span>
24. <span data-ttu-id="865fc-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="865fc-149">Close the page.</span></span>


