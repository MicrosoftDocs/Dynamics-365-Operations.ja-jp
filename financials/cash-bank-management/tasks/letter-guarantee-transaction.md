--- 
title: "信用保証状のトランザクション"
description: "この手順では、信用保証状のプロセスを説明します。"
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 21895bcda8f0fe46e9b7c4b2189ca8b13e0dc012
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="66b86-103">信用保証状のトランザクション</span><span class="sxs-lookup"><span data-stu-id="66b86-103">Letter of guarantee transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66b86-104">この手順では、信用保証状のプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="66b86-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="66b86-105">この手順を完了する前に、次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66b86-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="66b86-106">信用保証状についての銀行融資と転記プロファイルの設定。</span><span class="sxs-lookup"><span data-stu-id="66b86-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="66b86-107">信用保証状の銀行融資契約の作成。</span><span class="sxs-lookup"><span data-stu-id="66b86-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="66b86-108">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="66b86-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="66b86-109">信用保証状を添付した販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="66b86-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="66b86-110">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="66b86-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-111">Click New.</span></span>
3. <span data-ttu-id="66b86-112">[顧客口座] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="66b86-113">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-113">Expand the General section.</span></span>
5. <span data-ttu-id="66b86-114">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="66b86-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="66b86-116">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="66b86-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="66b86-118">[銀行ドキュメント タイプ] フィールドで「信用保証状」を選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="66b86-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-119">Click OK.</span></span>
11. <span data-ttu-id="66b86-120">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="66b86-121">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="66b86-122">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="66b86-123">[出荷] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="66b86-124">注記: [配送日の管理] = [なし] を選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="66b86-125">[指定出荷日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="66b86-126">[確定出荷日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="66b86-127">信用保証状_要求 プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="66b86-128">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="66b86-129">[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="66b86-130">アクション ペインで、[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="66b86-131">[要求] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="66b86-132">[タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="66b86-133">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="66b86-134">[値] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="66b86-135">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="66b86-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-136">Click OK.</span></span>
10. <span data-ttu-id="66b86-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66b86-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="66b86-138">信用保証状_銀行に送信 プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="66b86-139">[現金および銀行管理] > [信用保証状] > [信用保証状] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="66b86-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="66b86-141">[銀行に送信] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="66b86-142">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="66b86-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="66b86-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="66b86-145">信用保証状_銀行から受信 プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="66b86-146">[銀行から受信] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="66b86-147">[銀行番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="66b86-148">計算された [利益幅] と[経費] フィールドの値を確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="66b86-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-149">Click OK.</span></span>
4. <span data-ttu-id="66b86-150">[アクション] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="66b86-151">「銀行から受信」レコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="66b86-152">[仕訳帳バッチ番号] フィールドをクリックしてリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="66b86-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="66b86-153">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-153">Click Lines.</span></span>
    * <span data-ttu-id="66b86-154">仕訳入力の転記を確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="66b86-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66b86-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="66b86-156">信用保証状_受益者に渡す プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="66b86-157">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="66b86-158">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="66b86-159">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="66b86-160">[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="66b86-161">アクション ペインで、[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="66b86-162">[受益者に渡す] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="66b86-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-163">Click OK.</span></span>
8. <span data-ttu-id="66b86-164">[現金および銀行管理] > [信用保証状] > [信用保証状] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="66b86-165">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="66b86-166">[受益者に渡す] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="66b86-167">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-167">Click OK.</span></span>
12. <span data-ttu-id="66b86-168">[アクション] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="66b86-169">「受益者に渡す」レコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="66b86-170">信用保証状_増加額 プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="66b86-171">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="66b86-172">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="66b86-173">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="66b86-174">[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="66b86-175">アクション ペインで、[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="66b86-176">[値の増加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="66b86-177">[追加額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66b86-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="66b86-178">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-178">Click OK.</span></span>
9. <span data-ttu-id="66b86-179">[現金および銀行管理] > [信用保証状] > [信用保証状] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="66b86-180">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="66b86-181">[値の増加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="66b86-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-182">Click OK.</span></span>
13. <span data-ttu-id="66b86-183">[アクション] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="66b86-184">「値の増加」レコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="66b86-185">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="66b86-186">[仕訳帳バッチ番号] フィールドをクリックしてリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="66b86-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="66b86-187">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-187">Click Lines.</span></span>
    * <span data-ttu-id="66b86-188">転記済みの仕訳入力を確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="66b86-189">信用保証状_清算 プロセス</span><span class="sxs-lookup"><span data-stu-id="66b86-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="66b86-190">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="66b86-191">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="66b86-192">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="66b86-193">[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="66b86-194">アクション ペインで、[信用保証状] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="66b86-195">[清算] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="66b86-196">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-196">Click OK.</span></span>
8. <span data-ttu-id="66b86-197">[現金および銀行管理] > [信用保証状] > [信用保証状] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="66b86-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="66b86-198">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="66b86-199">[清算] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="66b86-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="66b86-200">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-200">Click OK.</span></span>
12. <span data-ttu-id="66b86-201">[アクション] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="66b86-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="66b86-202">「清算」レコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="66b86-203">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="66b86-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="66b86-204">[仕訳帳バッチ番号] フィールドをクリックしてリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="66b86-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="66b86-205">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="66b86-205">Click Lines.</span></span>
    * <span data-ttu-id="66b86-206">転記済みの仕訳入力を確認します。</span><span class="sxs-lookup"><span data-stu-id="66b86-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="66b86-207">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="66b86-207">Close the page.</span></span>


