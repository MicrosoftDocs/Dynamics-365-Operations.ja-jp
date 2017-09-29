--- 
title: "見積依頼の作成"
description: "この手順では、見積依頼の作成方法を説明します。"
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="bb6f1-103">見積依頼の作成</span><span class="sxs-lookup"><span data-stu-id="bb6f1-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb6f1-104">この手順では、見積依頼の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="bb6f1-105">これは通常、購買担当者が行います。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="bb6f1-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="bb6f1-107">開始する前に、入札タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="bb6f1-108">このタスクを完了し、RFQ を作成および送信したなら、その後仕入先ごとに返信を入力したり、比較したり、契約を授与したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="bb6f1-109">新規 RFQ を準備します</span><span class="sxs-lookup"><span data-stu-id="bb6f1-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="bb6f1-110">[調達] > [見積依頼] > [すべての見積依頼] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="bb6f1-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-111">Click New.</span></span>
    * <span data-ttu-id="bb6f1-112">次の購買タイプを使用できます。[発注書] (これが既定値です): 製品を購入するという申し出や、または支払いとの引き換えに製品を販売する申し出の受入を確定するドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="bb6f1-113">[購買要求]: 購買要求から RFQ を直接作成する場合は、このタイプが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="bb6f1-114">このオプションを手動で選択すると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="bb6f1-115">[購買契約]: 長期間にわたり特定の数量または金額の製品を購入する契約。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="bb6f1-116">このオプションを選択した場合、購買契約書に適用する日付範囲を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="bb6f1-117">[ドキュメント タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="bb6f1-118">[入札タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="bb6f1-119">スコア方法が入札タイプと関連付けられている場合、このスコア方法が作成する RFQ の規定になります。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="bb6f1-120">後にスコア方法を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="bb6f1-121">[配送日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="bb6f1-122">品目の受け取りを希望する日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="bb6f1-123">[有効期限日時] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="bb6f1-124">仕入先が RFQ に返信する期限を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="bb6f1-125">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="bb6f1-126">配送先住所が既定の倉庫の住所になります。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="bb6f1-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="bb6f1-128">行の追加</span><span class="sxs-lookup"><span data-stu-id="bb6f1-128">Add lines</span></span>
    * <span data-ttu-id="bb6f1-129">自分の RFQ に関する基本情報を指定してから、ベンダーが入札する商品またはサービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="bb6f1-130">この品目が既定の行タイプです。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="bb6f1-131">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bb6f1-132">USMF を使用しているなら、T0020 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="bb6f1-133">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="bb6f1-134">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-134">Click Add line.</span></span>
4. <span data-ttu-id="bb6f1-135">[明細行タイプ] フィールドで、[カテゴリ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="bb6f1-136">棚卸資産ではない商品またはサービスの RFQ を作成するためにカテゴリの行タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="bb6f1-137">次に、調達カテゴリ階層からの商品またはサービスのタイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="bb6f1-138">[調達カテゴリ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="bb6f1-139">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="bb6f1-140">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="bb6f1-141">[単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="bb6f1-142">仕入先の追加</span><span class="sxs-lookup"><span data-stu-id="bb6f1-142">Add vendors</span></span>
1. <span data-ttu-id="bb6f1-143">行表示からヘッダー表示に変更するには、[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="bb6f1-144">[仕入先] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="bb6f1-145">[仕入先の自動追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="bb6f1-146">要求された品目の調達カテゴリに基づいて、RFQ に仕入先を自動的に追加できます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="bb6f1-147">明細行に含まれるカテゴリに対して承認されている仕入先がない場合、仕入先を手動で追加できます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="bb6f1-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-148">Click Add.</span></span>
5. <span data-ttu-id="bb6f1-149">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="bb6f1-150">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-150">Click Add.</span></span>
7. <span data-ttu-id="bb6f1-151">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="bb6f1-152">仕入先を選択すると、ステータスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="bb6f1-153">これは、仕入先情報を RFQ に保存していても、仕入先に RFQ を未送信であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="bb6f1-154">仕入先の状態に関係なく RFQ に仕入先を追加できます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="bb6f1-155">RFQ を 仕入先に送信</span><span class="sxs-lookup"><span data-stu-id="bb6f1-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="bb6f1-156">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-156">Click Send.</span></span>
    * <span data-ttu-id="bb6f1-157">[見積依頼の送信] ページで、リスト内の仕入先が RFQ を受け取る仕入先であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="bb6f1-158">[印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-158">Click Print.</span></span>
    * <span data-ttu-id="bb6f1-159">このダイアログによって RFQ を印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="bb6f1-160">返信シートの印刷を選択する場合、この内容は、[調達パラメーター] で定義されます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="bb6f1-161">返信シートの印刷方法を選択するときは、[印刷ダイアログ] を開き、[詳細印刷オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="bb6f1-162">[作成済] または [送信済] のステータスの明細行を含む一つの RFQ が、各仕入先ごとに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="bb6f1-163">キャンセルした明細行、および登録した返信の明細行は印刷されません。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="bb6f1-164">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-164">Click Cancel.</span></span>
4. <span data-ttu-id="bb6f1-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-165">Click OK.</span></span>
5. <span data-ttu-id="bb6f1-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-166">Close the page.</span></span>
6. <span data-ttu-id="bb6f1-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="bb6f1-168">RFQ 仕訳を表示します</span><span class="sxs-lookup"><span data-stu-id="bb6f1-168">View the RFQ journal</span></span>
1. <span data-ttu-id="bb6f1-169">[調達] > [見積依頼] > [見積依頼のフォローアップ] > [見積依頼仕訳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="bb6f1-170">[プレビュー/印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="bb6f1-171">[元のプレビュー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-171">Click Original preview.</span></span>
4. <span data-ttu-id="bb6f1-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-172">Close the page.</span></span>
5. <span data-ttu-id="bb6f1-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb6f1-173">Close the page.</span></span>


