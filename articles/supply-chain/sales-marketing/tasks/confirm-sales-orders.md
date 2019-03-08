---
title: 販売注文の確認
description: この手順は、販売注文を確認する方法を示します。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "323988"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="15f64-103">販売注文の確認</span><span class="sxs-lookup"><span data-stu-id="15f64-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15f64-104">この手順は、販売注文を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="15f64-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="15f64-105">1 つの注文を確認する方法と、複数の注文を一度に確認する方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="15f64-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="15f64-106">通常、これらのタスクを実行するのは、販売注文担当者です。</span><span class="sxs-lookup"><span data-stu-id="15f64-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="15f64-107">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="15f64-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="15f64-108">開始する前に、同じ顧客に対して複数のオープン販売注文があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="15f64-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="15f64-109">USMF を使用すると、顧客 US-027 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="15f64-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="15f64-110">単一の販売注文の確認</span><span class="sxs-lookup"><span data-stu-id="15f64-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="15f64-111">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="15f64-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="15f64-112">リストで、確認する注文を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="15f64-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="15f64-113">選択された注文を開くには、販売注文番号のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="15f64-114">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="15f64-115">[販売注文の確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="15f64-116">[パラメーター] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="15f64-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="15f64-117">[転記の承認] フィールドが有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="15f64-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="15f64-118">[確認の印刷] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="15f64-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="15f64-119">[与信限度額の確認] フィールドでは、顧客のクレジット残高の計算に使用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="15f64-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="15f64-120">既定では、売掛金管理パラメータのページからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="15f64-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="15f64-121">特定の販売注文を確認するときに、[与信限度額チェック] を省略する場合は、[与信限度額] を [なし] に設定します。</span><span class="sxs-lookup"><span data-stu-id="15f64-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="15f64-122">ただし、このフィールドが [なし] に設定されている場合でも、[与信限度確認必須] オプションが顧客のマスターデータに選択されている場合、与信限度額チェックを実行するには注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="15f64-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="15f64-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-123">Click OK.</span></span>
9. <span data-ttu-id="15f64-124">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-124">Click Yes.</span></span>
10. <span data-ttu-id="15f64-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="15f64-125">Close the page.</span></span>
11. <span data-ttu-id="15f64-126">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="15f64-127">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-127">Click Change view.</span></span>
13. <span data-ttu-id="15f64-128">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-128">Click Header view.</span></span>
    * <span data-ttu-id="15f64-129">注文が確認されると、ドキュメント ステータスは [確認] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="15f64-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="15f64-130">[アクション] ペインで [販売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="15f64-131">[販売注文確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="15f64-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="15f64-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="15f64-133">複数の販売注文の一括確認</span><span class="sxs-lookup"><span data-stu-id="15f64-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="15f64-134">[販売とマーケティング] > [販売注文] > [注文確認] > [販売注文の確認] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="15f64-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="15f64-135">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-135">Click Select.</span></span>
3. <span data-ttu-id="15f64-136">[範囲] タブのリストで、[顧客口座] フィールドを参照するレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="15f64-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="15f64-137">[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="15f64-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="15f64-138">リストで、一括確認する複数の注文を持つ顧客 ID を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="15f64-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="15f64-139">USMF を使用すると、勘定 US-027 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="15f64-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="15f64-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-140">Click OK.</span></span>
    * <span data-ttu-id="15f64-141">[概要] タブには、クエリ基準に一致する注文の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="15f64-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="15f64-142">これらは [確認] に含まれます。</span><span class="sxs-lookup"><span data-stu-id="15f64-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="15f64-143">[集計更新] フィールドは、複数の注文を 1 つの確認ドキュメントに集計するパラメータを指定します。</span><span class="sxs-lookup"><span data-stu-id="15f64-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="15f64-144">既定では、このオプションは、売掛金管理パラメータのページの集計更新設定の既定値からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="15f64-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="15f64-145">[集計更新] フィールドで、[注文] を選択します。</span><span class="sxs-lookup"><span data-stu-id="15f64-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="15f64-146">集計更新の作成に最低限必要なパラメータは、請求元仕入先と通貨です。</span><span class="sxs-lookup"><span data-stu-id="15f64-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="15f64-147">これは、異なる請求元仕入先と異なる通貨を持つ集計更新を許可しないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="15f64-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="15f64-148">追加のパラメータは、売掛金管理パラメータのページからアクセスできる集計更新パラメータのページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="15f64-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="15f64-149">[販売注文] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="15f64-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="15f64-150">リストで、集計注文表にしたい注文番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="15f64-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="15f64-151">[調整] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-151">Click Arrange.</span></span>
11. <span data-ttu-id="15f64-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-152">Click OK.</span></span>
12. <span data-ttu-id="15f64-153">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="15f64-153">Click OK.</span></span>

