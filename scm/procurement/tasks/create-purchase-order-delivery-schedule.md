--- 
title: "配送スケジュールと発注書の作成"
description: "この手順では、発注書の配送スケジュールを作成する方法を示します。"
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="13d74-103">配送スケジュールと発注書の作成</span><span class="sxs-lookup"><span data-stu-id="13d74-103">Create a purchase order with a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13d74-104">この手順では、発注書の配送スケジュールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="13d74-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="13d74-105">配送スケジュールは、注文または仕訳帳の数量を複数の出荷で配送する要求があるときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="13d74-106">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="13d74-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="13d74-107">この手順は通常、購買担当者が行います。</span><span class="sxs-lookup"><span data-stu-id="13d74-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="13d74-108">配送スケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="13d74-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="13d74-109">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13d74-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="13d74-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-110">Click New.</span></span>
3. <span data-ttu-id="13d74-111">[仕入先] フィールドに「US-101」を入力します。</span><span class="sxs-lookup"><span data-stu-id="13d74-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="13d74-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-112">Click OK.</span></span>
5. <span data-ttu-id="13d74-113">[品目番号] フィールドに、「M0001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="13d74-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="13d74-114">[数量] フィールドに「10」と入力します。</span><span class="sxs-lookup"><span data-stu-id="13d74-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="13d74-115">[購買注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="13d74-116">[配送スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="13d74-117">[配送スケジュール] ページでは、注文明細行の合計数量が仕入先から配送される出荷の数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="13d74-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="13d74-118">既定では、システムは最初の配送スケジュール行に元の購買注文明細行の合計数量とそのほかの詳細をコピーします。</span><span class="sxs-lookup"><span data-stu-id="13d74-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="13d74-119">この例では、2 回目の出荷が最初の出荷から 1 週間後になされる 2 つの出荷スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="13d74-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="13d74-120">[数量] フィールドで、数量を「4」に変更します。</span><span class="sxs-lookup"><span data-stu-id="13d74-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="13d74-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-121">Click New.</span></span>
11. <span data-ttu-id="13d74-122">[数量] フィールドで、残りの数量として「6」を入力します。</span><span class="sxs-lookup"><span data-stu-id="13d74-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="13d74-123">出荷日フィールドで、最初の配送明細行の日付から 1 週間後となる日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="13d74-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="13d74-124">[合計] および [残余] フィールドを見ると、配送スケジュール行に割り当てられた合計数量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="13d74-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="13d74-125">残余数量がゼロの場合、元の明細行の全数量がスケジュールに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="13d74-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="13d74-126">[諸費用の変換] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="13d74-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="13d74-127">ここのオプションでは、配送スケジュール行間での費用の配分の仕方を制御できます。</span><span class="sxs-lookup"><span data-stu-id="13d74-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="13d74-128">[総額をコピー] を選択すると、元の注文明細行の請求金額が各配送明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="13d74-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="13d74-129">[配送行への割り当て] オプションでは、各配送明細行の数量にしたがい、元の雑費明細行が分割されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="13d74-130">[諸費用の変換] セクションを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="13d74-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="13d74-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-131">Click OK.</span></span>
    * <span data-ttu-id="13d74-132">これで、配送スケジュールが注文に適用されました。</span><span class="sxs-lookup"><span data-stu-id="13d74-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="13d74-133">元の注文明細行、つまり業務行は、複数の配送を含む注文明細行に変換されています。</span><span class="sxs-lookup"><span data-stu-id="13d74-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="13d74-134">これは、専用のアイコンで表示され、出荷明細行のヘッダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="13d74-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="13d74-135">2 つの配送明細行の最初である 2 番目の注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="13d74-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="13d74-136">2 つの新しい明細行、つまり配送明細行は、1 つの配送スケジュールを構成します。</span><span class="sxs-lookup"><span data-stu-id="13d74-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="13d74-137">注文は、元の明細行ではなく、これらの明細行について処理されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="13d74-138">確認伝票、製品受領書仕訳帳、請求書などのドキュメントを印刷する場合、配送明細行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="13d74-139">配送スケジュールの変更</span><span class="sxs-lookup"><span data-stu-id="13d74-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="13d74-140">配送明細行の数量を変更できます。</span><span class="sxs-lookup"><span data-stu-id="13d74-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="13d74-141">その場合、業務行は配送明細行の合計数量に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="13d74-142">最初の配送明細行の [数量] フィールドで、数量を「4」から「5」に変更します。</span><span class="sxs-lookup"><span data-stu-id="13d74-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="13d74-143">最初の注文明細行 (業務行) を選択します。</span><span class="sxs-lookup"><span data-stu-id="13d74-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="13d74-144">業務行の数量は 11 に変更されました。</span><span class="sxs-lookup"><span data-stu-id="13d74-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="13d74-145">配送スケジュールを使用して製品受領書を処理</span><span class="sxs-lookup"><span data-stu-id="13d74-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="13d74-146">製品受領を処理する前に発注書を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d74-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="13d74-147">この例では、受領は発注書に直接記録されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="13d74-148">入庫は商品が倉庫に到着したときに記録される場合があります。</span><span class="sxs-lookup"><span data-stu-id="13d74-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="13d74-149">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="13d74-150">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-150">Click Confirm.</span></span>
3. <span data-ttu-id="13d74-151">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="13d74-152">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13d74-152">Click Product receipt.</span></span>
5. <span data-ttu-id="13d74-153">[製品受領書] フィールドで、任意の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="13d74-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="13d74-154">このフィールドは製品受領書仕訳帳で伝票として使用される参照を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13d74-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="13d74-155">[数量] フィールドで、[注文済数量] を選択します。</span><span class="sxs-lookup"><span data-stu-id="13d74-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="13d74-156">このオプションは、注文明細行を作成した数量に対して受領処理がなされることを意味します。</span><span class="sxs-lookup"><span data-stu-id="13d74-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="13d74-157">[製品受領書の印刷] フィールドが [いいえ] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13d74-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="13d74-158">この例では印刷は不要です。</span><span class="sxs-lookup"><span data-stu-id="13d74-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="13d74-159">[明細行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="13d74-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="13d74-160">元の注文明細行向けではなく、2 つの配送明細行向けに製品受領書が作成された方法に注意します。</span><span class="sxs-lookup"><span data-stu-id="13d74-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="13d74-161">受領書が倉庫で記録されている場合、配送スケジュール行にも記録されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="13d74-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="13d74-162">[明細] セクションを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="13d74-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="13d74-163">[OK] をクリックして、受領書を転記します。</span><span class="sxs-lookup"><span data-stu-id="13d74-163">Click OK to post the receipt.</span></span>

