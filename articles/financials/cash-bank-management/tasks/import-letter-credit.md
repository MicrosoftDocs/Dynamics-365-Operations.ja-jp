---
title: 輸入信用状
description: この手順は、信用状のインポートのプロセスを説明します。
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d5539fbd17c880d8bbadd47444c9cc53fce039c
ms.sourcegitcommit: 0c1deb100d0bf6dacd14b328968bbc7a9d92583a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "771234"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="a2af0-103">輸入信用状</span><span class="sxs-lookup"><span data-stu-id="a2af0-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2af0-104">この手順は、信用状のインポートのプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="a2af0-105">この手順を実行する前に次の事柄が設定されている必要があります : 銀行融資、転記プロファイル、銀行融資契約と仕入先銀行の詳細。</span><span class="sxs-lookup"><span data-stu-id="a2af0-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="a2af0-106">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="a2af0-107">信用状と共に [発注書] を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="a2af0-108">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a2af0-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-109">Click New.</span></span>
3. <span data-ttu-id="a2af0-110">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="a2af0-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a2af0-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a2af0-113">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-113">Expand the General section.</span></span>
7. <span data-ttu-id="a2af0-114">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="a2af0-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a2af0-116">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="a2af0-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a2af0-118">[会計日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="a2af0-119">[配送日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="a2af0-120">注記 : 「銀行ドキュメント タイプ」フィールドは「信用状」の値と共に選択されているべきです。</span><span class="sxs-lookup"><span data-stu-id="a2af0-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="a2af0-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-121">Click OK.</span></span>
14. <span data-ttu-id="a2af0-122">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="a2af0-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="a2af0-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a2af0-125">[行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="a2af0-126">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="a2af0-127">[配送日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="a2af0-128">[確認済配送日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="a2af0-129">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="a2af0-130">[信用状の詳細] を定義します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="a2af0-131">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="a2af0-132">[信用状 / 輸入取立] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="a2af0-133">[申請日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="a2af0-134">「銀行口座」フィールドに申請日に基づく既定の有効な [銀行口座] があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="a2af0-135">[銀行ドキュメント番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="a2af0-136">[受取日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="a2af0-137">[銀行ドキュメント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="a2af0-138">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="a2af0-139">[銀行詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="a2af0-140">[通知銀行] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="a2af0-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="a2af0-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-142">Click Save.</span></span>
33. <span data-ttu-id="a2af0-143">[発注書の出荷のフェッチ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="a2af0-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-144">Close the page.</span></span>
35. <span data-ttu-id="a2af0-145">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="a2af0-146">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-146">Click Confirm.</span></span>
37. <span data-ttu-id="a2af0-147">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="a2af0-148">[信用状 / 輸入取立] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="a2af0-149">[プロセス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-149">Click Process.</span></span>
40. <span data-ttu-id="a2af0-150">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-150">Click Confirm.</span></span>
    * <span data-ttu-id="a2af0-151">[融資残高] により発注書の金額が減少することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="a2af0-152">この例では、[購買金額] = 500.00、[融資限度] = 10000.00 なので、[融資残高] = 9500.00 となります。</span><span class="sxs-lookup"><span data-stu-id="a2af0-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="a2af0-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-153">Close the page.</span></span>
42. <span data-ttu-id="a2af0-154">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="a2af0-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-155">Click Save.</span></span>
44. <span data-ttu-id="a2af0-156">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="a2af0-157">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-157">Click Confirm.</span></span>
    * <span data-ttu-id="a2af0-158">単価の変更に応じて [信用状] を修正します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="a2af0-159">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="a2af0-160">[信用状 / 輸入取立] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="a2af0-161">[購買単価] の変更に応じて信用状を修正します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="a2af0-162">[プロセス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-162">Click Process.</span></span>
49. <span data-ttu-id="a2af0-163">[修正] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-163">Click Amend.</span></span>
50. <span data-ttu-id="a2af0-164">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-164">Click Remove.</span></span>
51. <span data-ttu-id="a2af0-165">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-165">Click Yes.</span></span>
52. <span data-ttu-id="a2af0-166">[発注書の出荷のフェッチ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="a2af0-167">[プロセス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-167">Click Process.</span></span>
54. <span data-ttu-id="a2af0-168">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-168">Click Confirm.</span></span>
    * <span data-ttu-id="a2af0-169">[融資残高] により発注書の金額が減少することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="a2af0-170">この例では、変更された [購買金額] = 600.00、[融資限度] = 10000.00 なので、[融資残高] = 9400.00 となります。</span><span class="sxs-lookup"><span data-stu-id="a2af0-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="a2af0-171">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="a2af0-172">[梱包明細] の転記</span><span class="sxs-lookup"><span data-stu-id="a2af0-172">Post Packing slip</span></span>
1. <span data-ttu-id="a2af0-173">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="a2af0-174">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-174">Click Product receipt.</span></span>
3. <span data-ttu-id="a2af0-175">PurchParmTable_Num フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="a2af0-176">[信用状] の照会と一緒に作成された [出荷番号] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="a2af0-177">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a2af0-178">[製品受領書の日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="a2af0-179">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-179">Click OK.</span></span>
7. <span data-ttu-id="a2af0-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-180">Close the page.</span></span>
8. <span data-ttu-id="a2af0-181">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="a2af0-182">[輸入信用状] の状態の確認</span><span class="sxs-lookup"><span data-stu-id="a2af0-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="a2af0-183">[現金および銀行管理] > [信用状] > [輸入信用状] および [輸入取立] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="a2af0-184">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a2af0-185">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2af0-186">[輸入信用状] の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="a2af0-187">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-187">Close the page.</span></span>
5. <span data-ttu-id="a2af0-188">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="a2af0-189">仕入請求書の転記</span><span class="sxs-lookup"><span data-stu-id="a2af0-189">Post purchase invoice</span></span>
1. <span data-ttu-id="a2af0-190">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="a2af0-191">信用状と一緒に作成された [発注書] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="a2af0-192">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a2af0-193">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a2af0-194">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="a2af0-195">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-195">Click Invoice.</span></span>
6. <span data-ttu-id="a2af0-196">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="a2af0-197">[出荷番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="a2af0-198">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a2af0-199">[請求日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="a2af0-200">[照合状態の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-200">Click Update match status.</span></span>
11. <span data-ttu-id="a2af0-201">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-201">Click Post.</span></span>
12. <span data-ttu-id="a2af0-202">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-202">Close the page.</span></span>
13. <span data-ttu-id="a2af0-203">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="a2af0-204">[輸入信用状] の状態の確認</span><span class="sxs-lookup"><span data-stu-id="a2af0-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="a2af0-205">[現金および銀行管理] > [信用状] > [輸入信用状] および [輸入取立] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="a2af0-206">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a2af0-207">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2af0-208">[輸入信用状 2] を確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="a2af0-209">検証 : [出荷ステータス] = [請求済銀行融資の詳細]</span><span class="sxs-lookup"><span data-stu-id="a2af0-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="a2af0-210">[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-210">Click View.</span></span>
5. <span data-ttu-id="a2af0-211">[申請の印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-211">Click Print application.</span></span>
6. <span data-ttu-id="a2af0-212">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-212">Click OK.</span></span>
    * <span data-ttu-id="a2af0-213">[信用状の申請書] が印刷されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="a2af0-214">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-214">Close the page.</span></span>
8. <span data-ttu-id="a2af0-215">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-215">Close the page.</span></span>
9. <span data-ttu-id="a2af0-216">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="a2af0-217">信用状と共に作成済の仕入請求書の仕入先支払仕訳帳を転記</span><span class="sxs-lookup"><span data-stu-id="a2af0-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="a2af0-218">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a2af0-219">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-219">Click New.</span></span>
3. <span data-ttu-id="a2af0-220">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a2af0-221">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a2af0-222">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-222">Click Lines.</span></span>
6. <span data-ttu-id="a2af0-223">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="a2af0-224">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="a2af0-225">[トランザクションの決済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="a2af0-226">[合計] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="a2af0-227">[表示] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="a2af0-228">[銀行ドキュメント番号] と [出荷番号] フィールドが更新済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="a2af0-229">[マーク] のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="a2af0-230">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-230">Click OK.</span></span>
13. <span data-ttu-id="a2af0-231">[支払] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="a2af0-232">[銀行ドキュメント番号] と [出荷番号] フィールドが更新済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="a2af0-233">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-233">Click Post.</span></span>
15. <span data-ttu-id="a2af0-234">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-234">Close the page.</span></span>
16. <span data-ttu-id="a2af0-235">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="a2af0-236">請求書が支払われた後の [輸入信用状] の状態の確認</span><span class="sxs-lookup"><span data-stu-id="a2af0-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="a2af0-237">[現金および銀行管理] > [信用状] > [輸入信用状] および [輸入取立] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="a2af0-238">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a2af0-239">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2af0-240">[輸入信用状] の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="a2af0-241">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="a2af0-242">[銀行融資限度] および [使用率レポート] の確認</span><span class="sxs-lookup"><span data-stu-id="a2af0-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="a2af0-243">[現金および銀行管理] > [照会およびレポート] > [信用状または信用保証状] > [銀行融資] と [使用率レポート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="a2af0-244">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="a2af0-245">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-245">Click Filter.</span></span>
    * <span data-ttu-id="a2af0-246">必須銀行口座により、[基準] フィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="a2af0-247">[基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="a2af0-248">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a2af0-249">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-249">Click OK.</span></span>
7. <span data-ttu-id="a2af0-250">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2af0-250">Click OK.</span></span>
    * <span data-ttu-id="a2af0-251">トランザクションを一覧するレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="a2af0-252">[銀行ドキュメント番号]、[融資限度]、[使用金額] および [融資残高] のトランザクションのレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2af0-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="a2af0-253">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2af0-253">Close the page.</span></span>

