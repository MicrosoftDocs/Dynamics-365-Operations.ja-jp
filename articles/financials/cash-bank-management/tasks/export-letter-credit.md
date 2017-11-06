--- 
title: "信用状のエクスポート"
description: "この手順は、[輸出信用状] のプロセスを説明します。"
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="b40ea-103">信用状のエクスポート</span><span class="sxs-lookup"><span data-stu-id="b40ea-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b40ea-104">この手順は、[輸出信用状] のプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="b40ea-105">信用状は銀行が発行する契約であり、銀行は、買主と売主の契約が満たされた場合に買主に代わって確実に支払を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="b40ea-106">この手順の前に、「銀行融資と転記プロファイルの設定」手順および「信用状 _ 銀行融資契約の作成」手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="b40ea-107">この手順を正常に実行するためには、USMF のデモ会社が選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b40ea-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="b40ea-108">[輸出信用状] の販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="b40ea-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="b40ea-109">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b40ea-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-110">Click New.</span></span>
3. <span data-ttu-id="b40ea-111">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b40ea-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b40ea-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b40ea-114">[全般] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="b40ea-115">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b40ea-116">発行される品目が保管されているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="b40ea-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b40ea-118">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b40ea-119">発行される品目が保管されている [倉庫] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="b40ea-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b40ea-121">注記 : [銀行ドキュメント タイプ] フィールドは「信用状」の値と共に選択されているべきです。</span><span class="sxs-lookup"><span data-stu-id="b40ea-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="b40ea-122">[銀行ドキュメント タイプ] フィールドで「信用状」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="b40ea-123">[配送] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="b40ea-124">[配送日の管理] = [なし] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="b40ea-125">[入荷希望日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="b40ea-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-126">Click OK.</span></span>
15. <span data-ttu-id="b40ea-127">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b40ea-128">必要な品目を [出庫 / 売却済] として選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="b40ea-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b40ea-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b40ea-131">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="b40ea-132">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="b40ea-133">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="b40ea-134">[指定出荷日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="b40ea-135">[確定出荷日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="b40ea-136">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="b40ea-137">[信用状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="b40ea-138">[銀行ドキュメント番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="b40ea-139">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="b40ea-140">[銀行詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="b40ea-141">[発行銀行] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="b40ea-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="b40ea-143">[通知銀行] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="b40ea-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="b40ea-145">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="b40ea-146">[販売注文の出荷のフェッチ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="b40ea-147">[銀行ドキュメントの発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="b40ea-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="b40ea-149">[梱包明細] の転記</span><span class="sxs-lookup"><span data-stu-id="b40ea-149">Post Packing slip</span></span>
1. <span data-ttu-id="b40ea-150">アクション ウィンドウで、[ピッキングと梱包] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="b40ea-151">[梱包明細の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="b40ea-152">[パラメーター] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="b40ea-153">[数量] フィールドで [すべて] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="b40ea-154">[設定] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="b40ea-155">[梱包明細日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="b40ea-156">[出荷番号] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="b40ea-157">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b40ea-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-158">Click OK.</span></span>
10. <span data-ttu-id="b40ea-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="b40ea-160">売上請求書の転記</span><span class="sxs-lookup"><span data-stu-id="b40ea-160">Post sales invoice</span></span>
1. <span data-ttu-id="b40ea-161">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="b40ea-162">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-162">Click Invoice.</span></span>
3. <span data-ttu-id="b40ea-163">[概要] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="b40ea-164">[出荷番号] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="b40ea-165">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b40ea-166">[設定] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="b40ea-167">[請求日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="b40ea-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-168">Click OK.</span></span>
9. <span data-ttu-id="b40ea-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="b40ea-170">出荷ドキュメントの送信済ステータス</span><span class="sxs-lookup"><span data-stu-id="b40ea-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="b40ea-171">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="b40ea-172">[信用状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="b40ea-173">[明細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="b40ea-174">注記 : 「ドキュメント送信」フィールドは「はい」に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="b40ea-175">[輸出信用状] の確認</span><span class="sxs-lookup"><span data-stu-id="b40ea-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="b40ea-176">[現金および銀行管理] > [信用状] > [輸出信用状] および [輸入取立] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="b40ea-177">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b40ea-178">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b40ea-179">[輸出信用状] が「請求済」の [出荷状態] であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="b40ea-180">顧客支払</span><span class="sxs-lookup"><span data-stu-id="b40ea-180">Customer payment</span></span>
1. <span data-ttu-id="b40ea-181">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b40ea-182">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-182">Click New.</span></span>
3. <span data-ttu-id="b40ea-183">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b40ea-184">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b40ea-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b40ea-185">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b40ea-186">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-186">Click Lines.</span></span>
7. <span data-ttu-id="b40ea-187">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="b40ea-188">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="b40ea-189">[決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-189">Click Settlement.</span></span>
10. <span data-ttu-id="b40ea-190">[合計] のヘッダーにあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="b40ea-191">注記:「表示」フィールドを「信用状」に設定します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="b40ea-192">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b40ea-193">[マーク] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="b40ea-194">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-194">Click OK.</span></span>
14. <span data-ttu-id="b40ea-195">[支払] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="b40ea-196">[銀行ドキュメント番号] と [出荷番号の詳細] を確認します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="b40ea-197">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="b40ea-198">支払後の [輸出信用状] の確認</span><span class="sxs-lookup"><span data-stu-id="b40ea-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="b40ea-199">[現金および銀行管理] > [信用状] > [輸出信用状] および [輸入取立] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="b40ea-200">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b40ea-201">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b40ea-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b40ea-202">[出荷ステータス] = [支払領収済] および [残高金額] = 0.00 となることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b40ea-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

