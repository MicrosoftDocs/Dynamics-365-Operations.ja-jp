--- 
title: "販売注文からの発注書の作成"
description: "この手順は、販売注文に基づいた発注書を作成する方法を表示します。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 412a8c7acca06fc1be073019f91144e2a3f1c94b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="32e4d-103">販売注文からの発注書の作成</span><span class="sxs-lookup"><span data-stu-id="32e4d-103">Create a purchase order from a sales order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32e4d-104">この手順は、販売注文に基づいた発注書を作成する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="32e4d-105">発注書の製品の数量は、元の販売注文の需要を満たすよう指定されます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="32e4d-106">販売需要を満たすこの方法は、[配送要件計画] のより包括的で最適化された方法の代替です。</span><span class="sxs-lookup"><span data-stu-id="32e4d-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="32e4d-107">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="32e4d-108">販売注文からの発注書の作成</span><span class="sxs-lookup"><span data-stu-id="32e4d-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="32e4d-109">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="32e4d-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-110">Click New.</span></span>
3. <span data-ttu-id="32e4d-111">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="32e4d-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="32e4d-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-113">Click OK.</span></span>
6. <span data-ttu-id="32e4d-114">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="32e4d-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32e4d-116">USMF を使用すると、D0001 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="32e4d-117">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="32e4d-118">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-118">Click Add line.</span></span>
10. <span data-ttu-id="32e4d-119">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="32e4d-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="32e4d-121">USMF を使用すると、T0020 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="32e4d-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="32e4d-123">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="32e4d-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-124">Click Save.</span></span>
15. <span data-ttu-id="32e4d-125">アクション ウィンドウで、[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="32e4d-126">[発注書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-126">Click Purchase order.</span></span>
    * <span data-ttu-id="32e4d-127">[発注の作成] ページは、販売注文からコピーされた、すべての未処理販売注文明細行を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="32e4d-128">注文の詳細を確認し、必要に応じて、購買を作成する前に、購買数量および価格決定条件のような選択された詳細を変更できます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="32e4d-129">[すべてのオプションを含む] を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-129">Select the Include all option.</span></span>
    * <span data-ttu-id="32e4d-130">販売注文明細行のサブセットのみの発注書を生成する場合は、それらをそれぞれ選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="32e4d-131">[仕入先] フィールドには、仕入先番号がすでに入力されている場合とされていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="32e4d-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="32e4d-132">既定の仕入先が製品に対して設定されている場合 (関連する [品目補充] で)、この仕入先は明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="32e4d-133">それ以外の場合は、仕入先を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32e4d-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="32e4d-134">このガイドでは、[仕入先] フィールドが既に値を含むか否かにかかわらず、次の手順で、明細行ごとに異なる新しい仕入先を選択するように指示します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="32e4d-135">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="32e4d-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="32e4d-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="32e4d-138">2 番目の注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-138">Select the second order line.</span></span>
22. <span data-ttu-id="32e4d-139">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="32e4d-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="32e4d-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="32e4d-142">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-142">Click Validate.</span></span>
26. <span data-ttu-id="32e4d-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-143">Click OK.</span></span>
    * <span data-ttu-id="32e4d-144">メッセージは、1 つ以上の発注書が作成されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="32e4d-145">システムは、販売注文明細行に対して指定されている仕入先ごとに別の発注書を生成します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="32e4d-146">これは、複数の販売注文明細行が同じ仕入先によって提供される場合は、複数の明細行で一つの発注書が生成されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="32e4d-147">販売注文から作成された発注書の確認</span><span class="sxs-lookup"><span data-stu-id="32e4d-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="32e4d-148">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="32e4d-149">[関連する注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-149">Click Related orders.</span></span>
    * <span data-ttu-id="32e4d-150">[関連する注文] ページは、販売注文から作成されたすべての注文を一覧にします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="32e4d-151">この例では、それぞれ 2 つの異なる仕入先に対して 2 つの発注書があります。</span><span class="sxs-lookup"><span data-stu-id="32e4d-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="32e4d-152">クリックして、[発注書] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="32e4d-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="32e4d-153">各購買注文明細行は、その購買元になった販売注文明細行に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="32e4d-154">販売注文に対する関係は [参照タイプ]、[参照番号]、および [参照ロット] フィールド内の [明細行の詳細] クイック タブの [製品] タブで表示されます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="32e4d-155">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="32e4d-156">[製品] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="32e4d-156">Click the Product tab.</span></span>
    * <span data-ttu-id="32e4d-157">[参照ロット] により、現在の購買の原価が、関連付けられている販売注文で請求されるようになります。</span><span class="sxs-lookup"><span data-stu-id="32e4d-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="32e4d-158">[参照番号] フィールドのリンクを開くと元の販売注文に移動できます。</span><span class="sxs-lookup"><span data-stu-id="32e4d-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

