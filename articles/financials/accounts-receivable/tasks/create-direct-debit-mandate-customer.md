---
title: 顧客の口座引落の委任状の作成
description: このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572538"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="2f6e4-103">顧客の口座引落の委任状の作成</span><span class="sxs-lookup"><span data-stu-id="2f6e4-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f6e4-104">このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="2f6e4-105">銀行口座の作成</span><span class="sxs-lookup"><span data-stu-id="2f6e4-105">Create a bank account</span></span>
1. <span data-ttu-id="2f6e4-106">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="2f6e4-107">たとえば、「US-001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-107">For example, select US-001</span></span>
3. <span data-ttu-id="2f6e4-108">[アクション] ウィンドウで、[顧客] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="2f6e4-109">[銀行口座] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="2f6e4-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-110">Click New.</span></span>
6. <span data-ttu-id="2f6e4-111">[銀行口座] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="2f6e4-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="2f6e4-113">[IBAN] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="2f6e4-114">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="2f6e4-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-115">Click Save.</span></span>
11. <span data-ttu-id="2f6e4-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-116">Close the page.</span></span>
12. <span data-ttu-id="2f6e4-117">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="2f6e4-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2f6e4-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="2f6e4-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-120">Click Edit.</span></span>
16. <span data-ttu-id="2f6e4-121">[追加 ID] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="2f6e4-122">[口座引落 ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="2f6e4-123">[IBAN] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="2f6e4-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-124">Close the page.</span></span>
20. <span data-ttu-id="2f6e4-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="2f6e4-126">電子的支払方法の定義</span><span class="sxs-lookup"><span data-stu-id="2f6e4-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="2f6e4-127">[売掛金管理] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="2f6e4-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-128">Click New.</span></span>
3. <span data-ttu-id="2f6e4-129">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="2f6e4-130">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2f6e4-131">口座引落委任状の支払タイプは、電子支払でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="2f6e4-132">[委任状の要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="2f6e4-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="2f6e4-134">口座引落の委任状を顧客に追加します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="2f6e4-135">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="2f6e4-136">たとえば、「US-001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-136">For example, select US-001</span></span>
3. <span data-ttu-id="2f6e4-137">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-137">Click Edit.</span></span>
4. <span data-ttu-id="2f6e4-138">[支払の既定値] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="2f6e4-139">[支払方法] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="2f6e4-140">[支払の既定値] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="2f6e4-141">[口座引落委任状] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="2f6e4-142">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-142">Click Add.</span></span>
9. <span data-ttu-id="2f6e4-143">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="2f6e4-144">[債権者の銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="2f6e4-145">この委任状用に処理を予定している支払回数を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="2f6e4-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-146">Click OK.</span></span>
13. <span data-ttu-id="2f6e4-147">[印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-147">Click Print.</span></span>
14. <span data-ttu-id="2f6e4-148">[委任状レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-148">Click Mandate report.</span></span>
15. <span data-ttu-id="2f6e4-149">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-149">Close the page.</span></span>
16. <span data-ttu-id="2f6e4-150">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-150">Click Edit.</span></span>
17. <span data-ttu-id="2f6e4-151">[署名日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="2f6e4-152">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-152">Click Yes.</span></span>
19. <span data-ttu-id="2f6e4-153">委任状に署名した場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="2f6e4-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-154">Click OK.</span></span>
21. <span data-ttu-id="2f6e4-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="2f6e4-156">委任状と自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="2f6e4-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="2f6e4-157">[売掛金勘定] > [請求書] > [すべての自由書式の請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2f6e4-158">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-158">Click New.</span></span>
3. <span data-ttu-id="2f6e4-159">委任状を追加した顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="2f6e4-160">[口座引落の委任状 ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="2f6e4-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

