--- 
title: "直納として注文を出荷"
description: "この手順は、販売注文の直納を作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5cd68aa1c15672c702db887c08ecf9b3d63f2618
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="9a1de-103">直納として注文を出荷</span><span class="sxs-lookup"><span data-stu-id="9a1de-103">Ship orders as direct deliveries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a1de-104">この手順は、販売注文の直納を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-104">This procedure demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="9a1de-105">商品を自社倉庫へまず出荷する代わりに、仕入先から顧客へ直接出荷する場合、直納を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="9a1de-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9a1de-107">2 番目のサブタスクの「ワークベンチから直納を作成」を正常に完了するため、販売注文で選択した品目に関して、[リリース済製品マスター] の [購買クイックタブ] で既定の [仕入れ先] が指定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9a1de-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>


## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="9a1de-108">直納のための個々の注文を設定</span><span class="sxs-lookup"><span data-stu-id="9a1de-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="9a1de-109">[すべての販売注文] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-109">Go to All sales orders.</span></span>
2. <span data-ttu-id="9a1de-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-110">Click New.</span></span>
3. <span data-ttu-id="9a1de-111">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-111">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="9a1de-112">USMF を使用すると、勘定 US-001 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-112">If you’re using USMF, you can select account US-001.</span></span>  
4. <span data-ttu-id="9a1de-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-113">Click OK.</span></span>
5. <span data-ttu-id="9a1de-114">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="9a1de-115">USMF を使用すると、品目 T0020 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-115">If you’re using USMF, you can select item T0020.</span></span>  
6. <span data-ttu-id="9a1de-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-116">Click Save.</span></span>
7. <span data-ttu-id="9a1de-117">アクション ウィンドウで、[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-117">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="9a1de-118">[直納] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-118">Click Direct delivery.</span></span>
    * <span data-ttu-id="9a1de-119">[配送の作成] ページは、販売注文からコピーされるように、すべての未処理販売注文明細行を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-119">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="9a1de-120">注文の詳細を確認し、必要に応じて、直納を作成する前に、このような購買数量および価格決定条件詳細を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-120">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
9. <span data-ttu-id="9a1de-121">[すべてを含む] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-121">Select Yes in the Include all field.</span></span>
    * <span data-ttu-id="9a1de-122">販売注文明細行のサブセットのみの直納を生成する場合は、それらをそれぞれ選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-122">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="9a1de-123">[仕入先] フィールドには、仕入先番号がすでに入力されている場合とされていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a1de-123">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="9a1de-124">既定の仕入先が製品に対して設定されている場合 (関連する [品目補充] で)、この仕入先は明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-124">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="9a1de-125">それ以外の場合は、仕入先を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a1de-125">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="9a1de-126">この例では、すでに入力がされている場合でも、次の手順で新しい仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-126">In this example, we’ll select a new vendor in the next step, even if one is already populated.</span></span>   
10. <span data-ttu-id="9a1de-127">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-127">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="9a1de-128">USMF を使用すると、勘定 1001 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-128">If you’re using USMF, you can select account 1001.</span></span>  
11. <span data-ttu-id="9a1de-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-129">Click OK.</span></span>
    * <span data-ttu-id="9a1de-130">メッセージは、発注書が作成されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-130">The message informs you that the purchase order has now been created.</span></span>   
12. <span data-ttu-id="9a1de-131">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-131">Expand the Line details section.</span></span>
13. <span data-ttu-id="9a1de-132">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-132">Click the Delivery tab.</span></span>
    * <span data-ttu-id="9a1de-133">[直納] フィールドは、[はい] に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9a1de-133">The Direct delivery field is now set to Yes.</span></span>  
    * <span data-ttu-id="9a1de-134">[直納] ステータスは作成された発注書を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-134">The Direct delivery status shows the Purchase order created.</span></span>   
14. <span data-ttu-id="9a1de-135">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-135">On the Action Pane, click General.</span></span>
15. <span data-ttu-id="9a1de-136">[関連する注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-136">Click Related orders.</span></span>
16. <span data-ttu-id="9a1de-137">クリックして、[発注書] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-137">Click to follow the link in the Purchase order field.</span></span>
17. <span data-ttu-id="9a1de-138">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-138">Expand the Line details section.</span></span>
18. <span data-ttu-id="9a1de-139">[住所] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-139">Click the Address tab.</span></span>
    * <span data-ttu-id="9a1de-140">この購買注文明細行の配送先住所が会社住所ではなく、顧客の配送先住所であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9a1de-140">Note that the delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    * <span data-ttu-id="9a1de-141">購買注文明細行または元の販売注文明細行の配送先住所を変更した場合、対応する注文明細行の住所は自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-141">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
19. <span data-ttu-id="9a1de-142">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-142">Click the Delivery tab.</span></span>
    * <span data-ttu-id="9a1de-143">販売注文明細行のように、関連付けられている購買注文明細行のタイプは、[直納] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-143">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    * <span data-ttu-id="9a1de-144">購買注文明細行の [出荷日] および [確認された出荷日] は、元の販売注文明細行の [入荷希望日] と[確定入荷日] にそれぞれ設定されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-144">The purchase order line's Delivery  date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    * <span data-ttu-id="9a1de-145">購買注文明細行または販売明細行の日付を更新すると、対応する注文の日付が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-145">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    * <span data-ttu-id="9a1de-146">商品が直接顧客に配送されるように設定されている発注書は、特定の関連付けによって元の販売注文にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-146">The purchase order that is set to deliver goods directly the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="9a1de-147">この関連付けには、販売注文の梱包明細の更新は、販売注文自体からできず、発注書を使用して行う必要があるというルールが課されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-147">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="9a1de-148">ただし、顧客請求書は、販売注文から実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a1de-148">However, customer invoicing must be carried out from the sales order.</span></span>  
20. <span data-ttu-id="9a1de-149">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-149">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="9a1de-150">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-150">Click Confirmation.</span></span>
22. <span data-ttu-id="9a1de-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-151">Click OK.</span></span>
23. <span data-ttu-id="9a1de-152">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-152">On the Action Pane, click Receive.</span></span>
24. <span data-ttu-id="9a1de-153">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-153">Click Product receipt.</span></span>
25. <span data-ttu-id="9a1de-154">[製品受領書] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-154">In the Product receipt field, type a value.</span></span>
26. <span data-ttu-id="9a1de-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-155">Click OK.</span></span>
27. <span data-ttu-id="9a1de-156">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-156">On the Action Pane, click General.</span></span>
28. <span data-ttu-id="9a1de-157">[関連する注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-157">Click Related orders.</span></span>
29. <span data-ttu-id="9a1de-158">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-158">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9a1de-159">発注書が受領済と更新される、つまり、仕入先が顧客の住所に商品を出荷した後、元の販売注文のステータスは自動的に出荷済と更新されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-159">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    * <span data-ttu-id="9a1de-160">これで、販売注文は請求可能になります。</span><span class="sxs-lookup"><span data-stu-id="9a1de-160">The sales order can now be invoiced.</span></span>    
30. <span data-ttu-id="9a1de-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-161">Click OK.</span></span>
31. <span data-ttu-id="9a1de-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-162">Close the page.</span></span>
32. <span data-ttu-id="9a1de-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-163">Click OK.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="9a1de-164">ワークベンチから直納を作成</span><span class="sxs-lookup"><span data-stu-id="9a1de-164">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="9a1de-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-165">Close the page.</span></span>
2. <span data-ttu-id="9a1de-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-166">Close the page.</span></span>
3. <span data-ttu-id="9a1de-167">[すべての販売注文] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-167">Go to All sales orders.</span></span>
4. <span data-ttu-id="9a1de-168">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-168">Click New.</span></span>
5. <span data-ttu-id="9a1de-169">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-169">In the Customer account field, enter or select a value.</span></span>
6. <span data-ttu-id="9a1de-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-170">Click OK.</span></span>
7. <span data-ttu-id="9a1de-171">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-171">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="9a1de-172">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-172">Expand the Line details section.</span></span>
9. <span data-ttu-id="9a1de-173">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-173">Click the Delivery tab.</span></span>
    * <span data-ttu-id="9a1de-174">前の手順のように販売注文処理の一部として直納を作成する代わりに、購買担当者にこのタスクを引き渡すように選択できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-174">Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="9a1de-175">直納処理プロセスに販売注文明細行を含めるには、直納の行にマークを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a1de-175">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
10. <span data-ttu-id="9a1de-176">[直納] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-176">Select Yes in the Direct delivery field.</span></span>
    *   <span data-ttu-id="9a1de-177">品目が既定で直納に既に設定されている場合は、フィールドは注文明細行の入力時に、自動的に [はい] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-177">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="9a1de-178">[リリース済製品マスター] で [直納] オプションを [はい] に設定し、既定の [直納倉庫] を選択することにより、品目を直納に設定できます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-178">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    * <span data-ttu-id="9a1de-179">発注書はまだ作成されていないので、[直納] のステータスは [直納予定] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-179">Because the purchase order has not yet been created, the Direct delivery status is set to To be direct delivered.</span></span>   
11. <span data-ttu-id="9a1de-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-180">Close the page.</span></span>
12. <span data-ttu-id="9a1de-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-181">Close the page.</span></span>
13. <span data-ttu-id="9a1de-182">[直納] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-182">Go to Direct delivery.</span></span>
    * <span data-ttu-id="9a1de-183">[直納] のページは、直納予定のすべての販売注文明細行を購買担当者に提供するワークベンチとして機能し、それぞれの発注書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-183">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="9a1de-184">また、未処理の直納注文および確認済の注文を [確認および出荷] タブで表示することができます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-184">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>   
14. <span data-ttu-id="9a1de-185">[直納の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-185">Click Create direct delivery.</span></span>
15. <span data-ttu-id="9a1de-186">[確認] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a1de-186">Click the Confirmation tab.</span></span>
    * <span data-ttu-id="9a1de-187">直納注文は作成後、自動的に [確認] タブに移動します。このページから注文を直接確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="9a1de-187">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="9a1de-188">購買は確認されると、受領書を登録できる [出荷] タブに自動的に移動します。</span><span class="sxs-lookup"><span data-stu-id="9a1de-188">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  


