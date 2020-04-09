---
title: 販売注文の確認
description: この手順は、販売注文を確認する方法を示します。
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6383576302789d268d64edcbbe05305b03e956d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148710"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="a9e67-103">販売注文の確認</span><span class="sxs-lookup"><span data-stu-id="a9e67-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9e67-104">この手順は、販売注文を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="a9e67-105">1 つの注文を確認する方法と、複数の注文を一度に確認する方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="a9e67-106">通常、これらのタスクを実行するのは、販売注文担当者です。</span><span class="sxs-lookup"><span data-stu-id="a9e67-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="a9e67-107">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a9e67-108">開始する前に、同じ顧客に対して複数のオープン販売注文があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="a9e67-109">USMF を使用すると、顧客 US-027 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="a9e67-110">単一の販売注文の確認</span><span class="sxs-lookup"><span data-stu-id="a9e67-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="a9e67-111">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 販売注文 > すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="a9e67-112">リストで、確認する注文を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="a9e67-113">選択された注文を開くには、販売注文番号のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="a9e67-114">**アクション ウィンドウ**で、**販売**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="a9e67-115">**販売注文の確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="a9e67-116">**パラメーター** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="a9e67-117">**転記**オプションが「はい」に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="a9e67-118">**確認の印刷オプション**を「はい」に設定します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="a9e67-119">**与信限度額の確認** フィールドでは、顧客のクレジット残高の計算に使用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="a9e67-120">既定では、売掛金パラメータ ページからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="a9e67-121">特定の販売注文を確認するときに、与信限度額チェックを省略する場合は、**与信限度額**を「なし」に設定します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="a9e67-122">ただし、このフィールドが「なし」に設定されている場合でも、**与信限度確認必須**オプションが顧客のマスターデータに選択されている場合、与信限度額チェックを実行するには注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="a9e67-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="a9e67-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-123">Click **OK**.</span></span>
9. <span data-ttu-id="a9e67-124">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-124">Click **Yes**.</span></span>
10. <span data-ttu-id="a9e67-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-125">Close the page.</span></span>
11. <span data-ttu-id="a9e67-126">**アクション ウィンドウ**で、**オプション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="a9e67-127">**ビューの変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-127">Click **Change view**.</span></span>
13. <span data-ttu-id="a9e67-128">**ヘッダーの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-128">Click **Header view**.</span></span> <span data-ttu-id="a9e67-129">注文が確認されると、**ドキュメント ステータス**は「確認」に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="a9e67-130">**アクション ウィンドウ**で、**販売**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="a9e67-131">**販売注文確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="a9e67-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="a9e67-133">複数の販売注文の一括確認</span><span class="sxs-lookup"><span data-stu-id="a9e67-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="a9e67-134">**販売とマーケティング > 販売注文 > 注文確認 > 販売注文の確認**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="a9e67-135">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-135">Click **Select**.</span></span>
3. <span data-ttu-id="a9e67-136">**範囲**タブのリストで、**顧客口座**フィールドを参照するレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="a9e67-137">**基準**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a9e67-138">リストで、一括確認する複数の注文を持つ顧客 ID を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="a9e67-139">USMF を使用すると、勘定 US-027 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="a9e67-140">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-140">Click **OK**.</span></span>
    - <span data-ttu-id="a9e67-141">**概要**タブには、クエリ基準に一致する注文の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="a9e67-142">これらは [確認] に含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="a9e67-143">**パラメーター**セクションの**集計更新**フィールドは、複数の注文を 1 つの確認ドキュメントに集計するパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="a9e67-144">既定では、このオプションは、**売掛金管理パラメーター**のページの**集計更新設定の既定値**からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-144">By default, the option is copied from the D**efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="a9e67-145">**集計更新**フィールドで、「注文」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="a9e67-146">集計更新の作成に最低限必要なパラメーターは、**請求元仕入先**と**通貨**です。</span><span class="sxs-lookup"><span data-stu-id="a9e67-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="a9e67-147">これは、異なる請求元仕入先と異なる通貨を持つ集計更新を許可しないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="a9e67-148">追加のパラメーターは、**売掛金管理パラメーター**のページからアクセスできる**集計更新パラメーター**のページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="a9e67-149">**販売注文**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9e67-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a9e67-150">リストで、集計注文表にしたい注文番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9e67-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="a9e67-151">**調整**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="a9e67-152">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-152">Click **OK**.</span></span>
12. <span data-ttu-id="a9e67-153">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9e67-153">Click **OK**.</span></span>

