---
title: 販売契約書の履行
description: この手順は、販売注文と関連付けることによって販売契約書を履行する方法について説明します。
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3a35c7140b886f931df48e583b1582201b6547
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431765"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="0da95-103">販売契約書の履行</span><span class="sxs-lookup"><span data-stu-id="0da95-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0da95-104">この手順は、販売注文と関連付けることによって販売契約書を履行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0da95-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="0da95-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="0da95-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0da95-106">このガイドを開始する前に、「製品価値確約」タイプの有効な販売契約書を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0da95-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="0da95-107">または、かわりに「販売契約書の作成」というタスク ガイドを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="0da95-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="0da95-108">契約書からの販売注文のリリース</span><span class="sxs-lookup"><span data-stu-id="0da95-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="0da95-109">[販売とマーケティング] > [販売契約書] > [販売契約書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="0da95-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="0da95-110">リストで、注文をリリースする契約書を開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="0da95-111">[アクション ペイン] で、[販売契約書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="0da95-112">[リリース注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-112">Click Release order.</span></span>
    * <span data-ttu-id="0da95-113">[リリース注文の作成] ページ上部のテキストが指摘するとおり、販売注文明細行に必要な詳細は、契約が数量ベースか値ベースかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0da95-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="0da95-114">このガイドの契約は、[製品価値確約] タイプです。</span><span class="sxs-lookup"><span data-stu-id="0da95-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="0da95-115">そのため、このページの [明細行] セクションは空白になります。</span><span class="sxs-lookup"><span data-stu-id="0da95-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="0da95-116">確約が数量に基づく場合は、明細行情報は契約書からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="0da95-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="0da95-117">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-117">Click Create.</span></span>
    * <span data-ttu-id="0da95-118">メッセージは、販売注文が作成されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="0da95-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="0da95-119">明細行が含まれていないため、リリース プロセスを完了するために、注文明細行の詳細を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0da95-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="0da95-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-120">Close the page.</span></span>
7. <span data-ttu-id="0da95-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-121">Close the page.</span></span>
8. <span data-ttu-id="0da95-122">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0da95-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="0da95-123">リストで、前のタスクでの注文リリースの結果作成された注文を検索し、開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="0da95-124">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-124">Click Add line.</span></span>
11. <span data-ttu-id="0da95-125">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0da95-126">[品目番号] フィールドで、関連する販売契約書で指定された品目を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0da95-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="0da95-127">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0da95-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0da95-128">関連付けられている販売契約書の値未満の [正味金額] になる数量の入力を確認します。</span><span class="sxs-lookup"><span data-stu-id="0da95-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="0da95-129">販売注文が契約にリンクされているため、交渉された割引率が注文明細行に適用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0da95-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="0da95-130">[明細行の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-130">Click Update line.</span></span>
15. <span data-ttu-id="0da95-131">[添付済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-131">Click Attached.</span></span>
    * <span data-ttu-id="0da95-132">[添付契約書] のページは、明細行がリリースされる ID と契約条件を表示します。</span><span class="sxs-lookup"><span data-stu-id="0da95-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="0da95-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-133">Close the page.</span></span>
17. <span data-ttu-id="0da95-134">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="0da95-135">[関連付けられている販売契約書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="0da95-136">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="0da95-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="0da95-137">[履行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="0da95-138">[履行] タブは、この確約と関連付けられるすべての販売注文明細行の概要、その履行状態、および、まだリリースされていない金額または数量を表示します。</span><span class="sxs-lookup"><span data-stu-id="0da95-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="0da95-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-139">Close the page.</span></span>
22. <span data-ttu-id="0da95-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-140">Close the page.</span></span>
23. <span data-ttu-id="0da95-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0da95-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="0da95-142">注文プロセスでの販売契約書の適用</span><span class="sxs-lookup"><span data-stu-id="0da95-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="0da95-143">[販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0da95-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="0da95-144">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-144">Click New.</span></span>
3. <span data-ttu-id="0da95-145">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0da95-146">リストで、販売契約書で指定された顧客を検索、選択します。</span><span class="sxs-lookup"><span data-stu-id="0da95-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="0da95-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0da95-148">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="0da95-148">Expand the General section.</span></span>
7. <span data-ttu-id="0da95-149">[販売契約書 ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0da95-150">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0da95-151">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-151">Click Yes.</span></span>
10. <span data-ttu-id="0da95-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-152">Click OK.</span></span>
11. <span data-ttu-id="0da95-153">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0da95-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="0da95-154">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="0da95-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="0da95-155">[品目番号] フィールドで、関連する販売契約書で指定された品目を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0da95-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="0da95-156">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0da95-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-157">Click Save.</span></span>
16. <span data-ttu-id="0da95-158">アクション ウィンドウで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="0da95-159">[梱包明細の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="0da95-160">[パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="0da95-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="0da95-161">[転記] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0da95-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="0da95-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-162">Click OK.</span></span>
21. <span data-ttu-id="0da95-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-163">Click OK.</span></span>
22. <span data-ttu-id="0da95-164">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="0da95-165">[関連付けられている販売契約書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="0da95-166">[履行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0da95-166">Click the Fulfillment tab.</span></span>

