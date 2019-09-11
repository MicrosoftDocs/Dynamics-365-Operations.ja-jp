---
title: 販売コミッションの登録
description: このトピックでは、販売コミッションを計算および登録する方法を説明します。
author: omulvad
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db27255c74c55b10680594ad23424253e4c3f79e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867056"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="d5b0d-103">販売コミッションの登録</span><span class="sxs-lookup"><span data-stu-id="d5b0d-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5b0d-104">このトピックでは、販売コミッションを計算および登録する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="d5b0d-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d5b0d-106">このガイドを開始する前に、必要なすべてのコミッション計算の設定ができていることを確認するために、「販売コミッション ルールの設定」と呼ばれるガイドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="d5b0d-107">このコミッションのプロセスとして選択した顧客と品目をメモして、このガイドで販売注文を作成するように要求された時にそれらを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="d5b0d-108">販売担当者がコミッションを取得する販売注文の請求</span><span class="sxs-lookup"><span data-stu-id="d5b0d-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="d5b0d-109">ナビゲーション ウィンドウで、**モジュール > 販売とマーケティング > 販売注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="d5b0d-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-110">Select **New**.</span></span>
3. <span data-ttu-id="d5b0d-111">**顧客アカウント** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="d5b0d-112">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-112">Select **OK**.</span></span>
5. <span data-ttu-id="d5b0d-113">アクション ウィンドウで、**オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="d5b0d-114">**ビューの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-114">Select **Change view**.</span></span>
7. <span data-ttu-id="d5b0d-115">**ヘッダーの表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-115">Select **Header view**.</span></span>
8. <span data-ttu-id="d5b0d-116">**設定**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="d5b0d-117">**売上グループ** フィールドの値は、1 人以上の販売担当者が割り当てられたグループを表します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="d5b0d-118">このグループのメンバーが、注文が請求された時に、事前定義されたレートおよび配分でコミッションを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="d5b0d-119">値は顧客カードからコピーされますが、変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="d5b0d-120">[売上] グループは販売注文明細行にもコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="d5b0d-121">ヘッダーおよび/または明細行間のものと異なるように変更できます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="d5b0d-122">**コミッション グループ** フィールドの値は、コミッションを追跡するために、1 人以上の顧客に対して作成したグループを表します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="d5b0d-123">値は顧客カードからコピーされますが、変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="d5b0d-124">アクション ウィンドウで、**オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="d5b0d-125">**ビューの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-125">Select **Change view**.</span></span>
11. <span data-ttu-id="d5b0d-126">**明細行の表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-126">Select **Line view**.</span></span>
12. <span data-ttu-id="d5b0d-127">**品目番号**フィールドのドロップダウン メニューで、コミッションに対して設定した品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="d5b0d-128">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d5b0d-129">ラインの [正味金額] をご確認下さい。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="d5b0d-130">これは、この例ではコミッション計算の基準となる、売上収益を表します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="d5b0d-131">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-131">Select **Save**.</span></span>
15. <span data-ttu-id="d5b0d-132">アクション ウィンドウで、**請求書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="d5b0d-133">**請求書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="d5b0d-134">**パラメーター** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="d5b0d-135">**数量**フィールドで、**すべて**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="d5b0d-136">**転記**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="d5b0d-137">**OK** を選択し、次のウィンドウで **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="d5b0d-138">トランザクションの転記には、1 分程度必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="d5b0d-139">処理が完了するまで、ページを閉じないで下さい。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-139">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="d5b0d-140">登録された販売コミッションの確認</span><span class="sxs-lookup"><span data-stu-id="d5b0d-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="d5b0d-141">アクション ウィンドウで、**請求書**を選択し、再度**請求書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="d5b0d-142">アクション ウィンドウで、**請求書**を選択し、**コミッション トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="d5b0d-143">請求済の販売注文に関連付けられている販売担当者に支払うコミッションの金額を表す明細行が、**概要**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="d5b0d-144">詳細を確認しましょう。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-144">Let's review the details.</span></span>  
    - <span data-ttu-id="d5b0d-145">「販売コミッション ルールの設定」ガイドを使用して**コミッション売上**グループを設定した場合、販売コミッションを受取る販売担当者は 2 人で、コミッションは 2 人に均等に分割されます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="d5b0d-146">この例では、コミッションの合計金額は売上収益の割合 (注文明細行の正味金額) として計算されます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="d5b0d-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-147">Close the page.</span></span>
4. <span data-ttu-id="d5b0d-148">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-148">Select **Voucher**.</span></span> <span data-ttu-id="d5b0d-149">伝票トランザクションを確認すると、事前定義されたコミッション経費とコミッション支払勘定に転記されたコミッション金額が分かります。</span><span class="sxs-lookup"><span data-stu-id="d5b0d-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

