---
title: 顧客の損金処理仕訳帳の作成
description: このタスク ガイドでは、損金処理のパラメータを設定し、[コレクション] ページ、[未処理の顧客請求書] ページおよび [顧客ページ] からトランザクションを損金処理する方法を表示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140240"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="326ea-103">顧客の損金処理仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="326ea-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="326ea-104">このタスク ガイドでは、損金処理のパラメータを設定し、[コレクション] ページ、[未処理の顧客請求書] ページおよび [顧客ページ] からトランザクションを損金処理する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="326ea-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="326ea-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="326ea-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="326ea-106">損金処理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="326ea-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="326ea-107">**ナビゲーション ウィンドウ > モジュール > クレジットおよびコレクション > 設定 > 売掛金勘定パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="326ea-108">**回収**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="326ea-109">**損金処理**セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="326ea-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="326ea-110">**損金処理仕訳**とは、作成する損金処理トランザクションを保持する一般仕訳帳のことです。</span><span class="sxs-lookup"><span data-stu-id="326ea-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="326ea-111">各損金処理に理由コードを添付できます。</span><span class="sxs-lookup"><span data-stu-id="326ea-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="326ea-112">損金処理時にこの既定値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="326ea-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="326ea-113">損金処理の元のトランザクションから売上税を分割する場合は、**売上税を分離する**をはいに設定します。</span><span class="sxs-lookup"><span data-stu-id="326ea-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="326ea-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-114">Close the page.</span></span>
5. <span data-ttu-id="326ea-115">**貸方転記および取立 > 設定 > 顧客転記プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="326ea-116">損金処理勘定は、一般仕訳帳で経費勘定として、または準備金の調整として使用されます。</span><span class="sxs-lookup"><span data-stu-id="326ea-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="326ea-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="326ea-118">[指定の期間に達している残高] ページから顧客残高を損金処理します。</span><span class="sxs-lookup"><span data-stu-id="326ea-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="326ea-119">**与信および回収 > 回収 > 指定の期間に達している残高**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="326ea-120">損金処理する顧客の行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="326ea-121">たとえば、Birch 会社の明細行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="326ea-122">**アクション ウィンドウ**で、**回収**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="326ea-123">**損金処理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-123">Click **Write off**.</span></span>
5. <span data-ttu-id="326ea-124">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-124">Click **OK**.</span></span>
6. <span data-ttu-id="326ea-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-125">Close the page.</span></span>
7. <span data-ttu-id="326ea-126">**ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="326ea-127">損金処理を含む仕訳帳の仕訳帳バッチ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="326ea-128">1 つの明細行は、顧客残高を取り消すために作成されます。</span><span class="sxs-lookup"><span data-stu-id="326ea-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="326ea-129">1 つ以上の明細行は、損金処理勘定に損金処理を転記するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="326ea-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="326ea-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-130">Close the page.</span></span>
10. <span data-ttu-id="326ea-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="326ea-132">回収フォームのトランザクションを損金処理します。</span><span class="sxs-lookup"><span data-stu-id="326ea-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="326ea-133">**与信および回収 > 回収 > 指定の期間に達している残高**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="326ea-134">損金処理するトランザクションがある顧客の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="326ea-135">たとえば、「Cave Wholesales (US-004)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="326ea-136">最初のトランザクションの行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="326ea-137">2 番目のトランザクションの行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="326ea-138">**損金処理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-138">Click **Write off**.</span></span>
6. <span data-ttu-id="326ea-139">**理由コメント** フィールドに '貸倒損失' を入力します。</span><span class="sxs-lookup"><span data-stu-id="326ea-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="326ea-140">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-140">Click **OK**.</span></span>
8. <span data-ttu-id="326ea-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-141">Close the page.</span></span>
9. <span data-ttu-id="326ea-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-142">Close the page.</span></span>
10. <span data-ttu-id="326ea-143">**総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="326ea-144">損金処理を含む仕訳帳の仕訳帳バッチ番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="326ea-145">1 つの明細行は、顧客残高を取り消すために作成されます。</span><span class="sxs-lookup"><span data-stu-id="326ea-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="326ea-146">1 つ以上の明細行は、損金処理勘定に損金処理を転記するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="326ea-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="326ea-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-147">Close the page.</span></span>
13. <span data-ttu-id="326ea-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="326ea-149">[未処理の顧客請求書] ページの請求書の損金処理</span><span class="sxs-lookup"><span data-stu-id="326ea-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="326ea-150">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 請求書 > 未処理の顧客請求書**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="326ea-151">請求の明細行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-151">Mark the line for an invoice.</span></span> <span data-ttu-id="326ea-152">たとえば、「CIV-000667」の明細行をマークします。</span><span class="sxs-lookup"><span data-stu-id="326ea-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="326ea-153">**アクション ウィンドウ**で、**請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="326ea-154">**損金処理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-154">Click **Write off**.</span></span>
5. <span data-ttu-id="326ea-155">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-155">Click **OK**.</span></span>
6. <span data-ttu-id="326ea-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="326ea-157">[顧客] ページの顧客残高の損金処理</span><span class="sxs-lookup"><span data-stu-id="326ea-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="326ea-158">**売掛金勘定 > 顧客 > すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="326ea-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="326ea-159">顧客 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-159">Select a customer account.</span></span> <span data-ttu-id="326ea-160">たとえば、「US-001 (Contoso Retail San Diego)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="326ea-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="326ea-161">**アクション ウィンドウ**で、**回収**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="326ea-162">**損金処理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-162">Click **Write off**.</span></span>
5. <span data-ttu-id="326ea-163">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326ea-163">Click **OK**.</span></span>
6. <span data-ttu-id="326ea-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326ea-164">Close the page.</span></span>

