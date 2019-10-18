---
title: 顧客の口座引落の委任状の作成
description: このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178702"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="6b18d-103">顧客の口座引落の委任状の作成</span><span class="sxs-lookup"><span data-stu-id="6b18d-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b18d-104">このタスク ガイドでは、口座引落の委任状を作成し、それを請求書に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="6b18d-105">銀行口座の作成</span><span class="sxs-lookup"><span data-stu-id="6b18d-105">Create a bank account</span></span>
1. <span data-ttu-id="6b18d-106">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 顧客 > すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="6b18d-107">一覧で、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-107">In the list, select a record.</span></span> <span data-ttu-id="6b18d-108">たとえば、「US-001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-108">For example, select US-001</span></span>
3. <span data-ttu-id="6b18d-109">アクション ウィンドウで、**顧客**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="6b18d-110">**銀行口座**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="6b18d-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-111">Click **New**.</span></span>
6. <span data-ttu-id="6b18d-112">**銀行口座**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="6b18d-113">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="6b18d-114">**IBAN** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="6b18d-115">**通貨**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="6b18d-116">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-116">Click **Save**.</span></span>
11. <span data-ttu-id="6b18d-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-117">Close the page.</span></span>
12. <span data-ttu-id="6b18d-118">**ナビゲーション ウィンドウ**で、**モジュール > 現金および銀行管理 > 銀行口座 > 銀行口座**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="6b18d-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="6b18d-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="6b18d-121">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-121">Click **Edit**.</span></span>
16. <span data-ttu-id="6b18d-122">**追加 ID** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="6b18d-123">**口座引落 ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="6b18d-124">**IBAN** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="6b18d-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-125">Close the page.</span></span>
20. <span data-ttu-id="6b18d-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="6b18d-127">電子的支払方法の定義</span><span class="sxs-lookup"><span data-stu-id="6b18d-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="6b18d-128">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 支払設定 > 支払方法**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="6b18d-129">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-129">Click **New**.</span></span>
3. <span data-ttu-id="6b18d-130">**支払方法**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="6b18d-131">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6b18d-132">**支払タイプ** フィールドで、'電子支払' を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="6b18d-133">口座引落委任状の支払タイプは、電子支払でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6b18d-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="6b18d-134">**委任状の要求**フィールドで、はいを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="6b18d-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="6b18d-136">口座引落の委任状を顧客に追加します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="6b18d-137">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 顧客 > すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="6b18d-138">一覧で、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-138">In the list, select a record.</span></span> <span data-ttu-id="6b18d-139">たとえば、「US-001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-139">For example, select US-001</span></span>
3. <span data-ttu-id="6b18d-140">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-140">Click **Edit**.</span></span>
4. <span data-ttu-id="6b18d-141">**支払の既定値**クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="6b18d-142">**支払方法**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="6b18d-143">**支払の既定値**クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="6b18d-144">**口座引落委任状**クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="6b18d-145">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-145">Click **Add**.</span></span>
9. <span data-ttu-id="6b18d-146">**銀行口座**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="6b18d-147">**債権者の銀行口座**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="6b18d-148">**支払頻度**フィールドで、この委任状用に処理を予定している支払回数を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="6b18d-149">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-149">Click **OK**.</span></span>
13. <span data-ttu-id="6b18d-150">**印刷** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-150">Click **Print**.</span></span>
14. <span data-ttu-id="6b18d-151">**委任状レポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="6b18d-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-152">Close the page.</span></span>
16. <span data-ttu-id="6b18d-153">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-153">Click **Edit**.</span></span>
17. <span data-ttu-id="6b18d-154">**署名日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="6b18d-155">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-155">Click **Yes**.</span></span>
19. <span data-ttu-id="6b18d-156">委任状に署名した場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="6b18d-157">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-157">Click **OK**.</span></span>
21. <span data-ttu-id="6b18d-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b18d-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="6b18d-159">委任状と自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="6b18d-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="6b18d-160">**ナビゲーション ウィンドウ**で、**モジュール > 売掛金勘定 > 請求書 > すべての自由書式の請求書**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="6b18d-161">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b18d-161">Click **New**.</span></span>
3. <span data-ttu-id="6b18d-162">委任状を追加した顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="6b18d-163">**口座引落の委任状 ID** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="6b18d-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>
