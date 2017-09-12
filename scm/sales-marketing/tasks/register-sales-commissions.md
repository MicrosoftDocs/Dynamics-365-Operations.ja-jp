--- 
title: "販売コミッションの登録"
description: "この手順は、販売コミッションを計算および登録する方法を示します。"
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
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="f243d-103">販売コミッションの登録</span><span class="sxs-lookup"><span data-stu-id="f243d-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f243d-104">この手順は、販売コミッションを計算および登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f243d-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="f243d-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="f243d-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f243d-106">このガイドを開始する前に、必要なすべてのコミッション計算の設定ができていることを確認するために、「販売コミッション ルールの設定」と呼ばれるガイドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f243d-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="f243d-107">このコミッションのプロセスとして選択した顧客と品目をメモして、このガイドで販売注文を作成するように要求された時にそれらを使用してください。</span><span class="sxs-lookup"><span data-stu-id="f243d-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="f243d-108">販売担当者がコミッションを取得する販売注文の請求</span><span class="sxs-lookup"><span data-stu-id="f243d-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="f243d-109">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f243d-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="f243d-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-110">Click New.</span></span>
3. <span data-ttu-id="f243d-111">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f243d-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f243d-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f243d-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f243d-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f243d-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-114">Click OK.</span></span>
7. <span data-ttu-id="f243d-115">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="f243d-116">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-116">Click Change view.</span></span>
9. <span data-ttu-id="f243d-117">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-117">Click Header view.</span></span>
10. <span data-ttu-id="f243d-118">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f243d-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="f243d-119">[売上グループ] フィールドの値は、1 人以上の販売担当者が割り当てられたグループを表します。</span><span class="sxs-lookup"><span data-stu-id="f243d-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="f243d-120">このグループのメンバーが、注文が請求された時に、事前定義されたレートおよび配分でコミッションを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f243d-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="f243d-121">値は顧客カードからコピーされますが、変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="f243d-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="f243d-122">[売上] グループは販売注文明細行にもコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f243d-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="f243d-123">ヘッダーおよび/または明細行間のものと異なるように変更できます。</span><span class="sxs-lookup"><span data-stu-id="f243d-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="f243d-124">[コミッション グループ] フィールドの値は、コミッションを追跡するために、1 人以上の顧客に対して作成したグループを表します。</span><span class="sxs-lookup"><span data-stu-id="f243d-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="f243d-125">値は顧客カードからコピーされますが、変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="f243d-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="f243d-126">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="f243d-127">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-127">Click Change view.</span></span>
13. <span data-ttu-id="f243d-128">[明細行の表示] ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-128">Click Line view.</span></span>
14. <span data-ttu-id="f243d-129">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f243d-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f243d-130">一覧で、コミッション用に設定した品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="f243d-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="f243d-131">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f243d-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f243d-132">ラインの [正味金額] をご確認下さい。</span><span class="sxs-lookup"><span data-stu-id="f243d-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="f243d-133">これは、この例ではコミッション計算の基準となる、売上収益を表します。</span><span class="sxs-lookup"><span data-stu-id="f243d-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="f243d-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-134">Click Save.</span></span>
18. <span data-ttu-id="f243d-135">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="f243d-136">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-136">Click Invoice.</span></span>
20. <span data-ttu-id="f243d-137">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f243d-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="f243d-138">[数量] フィールドで、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f243d-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="f243d-139">[転記] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f243d-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="f243d-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-140">Click OK.</span></span>
24. <span data-ttu-id="f243d-141">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-141">Click OK.</span></span>
    * <span data-ttu-id="f243d-142">トランザクションの転記には、1 分程度必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="f243d-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="f243d-143">処理が完了するまで、ページを閉じないで下さい。</span><span class="sxs-lookup"><span data-stu-id="f243d-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="f243d-144">登録された販売コミッションの確認</span><span class="sxs-lookup"><span data-stu-id="f243d-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="f243d-145">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f243d-146">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-146">Click Invoice.</span></span>
3. <span data-ttu-id="f243d-147">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="f243d-148">[コミッション トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="f243d-149">請求済の販売注文に関連付けられる販売担当者に支払うコミッションの金額を表す行が [概要] タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f243d-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="f243d-150">詳細を確認しましょう。</span><span class="sxs-lookup"><span data-stu-id="f243d-150">Let's review the details.</span></span>     
    * <span data-ttu-id="f243d-151">「販売コミッション ルールの設定」ガイドを使用してコミッション売上グループを設定した場合、販売コミッションを受取る販売担当者は 2 人で、コミッションは、2 人に均等に分割されます。</span><span class="sxs-lookup"><span data-stu-id="f243d-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="f243d-152">この例では、コミッションの合計金額は売上収益の割合 (注文明細行の正味金額) として計算されます。</span><span class="sxs-lookup"><span data-stu-id="f243d-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="f243d-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f243d-153">Close the page.</span></span>
6. <span data-ttu-id="f243d-154">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f243d-154">Click Voucher.</span></span>
    * <span data-ttu-id="f243d-155">伝票トランザクションを確認すると、事前定義されたコミッション経費とコミッション支払勘定に転記されたコミッション金額が分かります。</span><span class="sxs-lookup"><span data-stu-id="f243d-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


