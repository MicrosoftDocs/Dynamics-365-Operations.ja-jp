---
title: 請求管理グループを使用した AP システムへの請求書データの入力
description: このタスク ガイドでは、請求書を作成する仕入帳を使用する方法を示します。
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843220"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="4c4d6-103">請求管理グループを使用した AP システムへの請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="4c4d6-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c4d6-104">このタスク ガイドでは、請求書を作成する仕入帳を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="4c4d6-105">その後、請求書を発注書と一致させるために、また仕入先請求書のページにある経費を確定するために、請求書管理グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="4c4d6-106">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="4c4d6-106">Create a purchase order</span></span>
1. <span data-ttu-id="4c4d6-107">[買掛金勘定] > [発注書] > [発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="4c4d6-108">[新規] をクリックして新しい発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="4c4d6-109">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="4c4d6-110">一覧から仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-110">Select the vendor from the list.</span></span> <span data-ttu-id="4c4d6-111">例としては、仕入先「1001」です。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="4c4d6-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-112">Click OK.</span></span>
6. <span data-ttu-id="4c4d6-113">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="4c4d6-114">サービス品目番号を一覧で見つけます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-114">Find the services item number in the list.</span></span> <span data-ttu-id="4c4d6-115">たとえば、「S0001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-115">For example, select S0001.</span></span>
8. <span data-ttu-id="4c4d6-116">品目番号をクリックし、それを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="4c4d6-117">正味金額は 75.00 です。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-117">The net amount is 75.00.</span></span>  <span data-ttu-id="4c4d6-118">これは、請求書上に表示される金額です。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="4c4d6-119">[アクション] ペインで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="4c4d6-120">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="4c4d6-121">請求書の作成と転記</span><span class="sxs-lookup"><span data-stu-id="4c4d6-121">Create and post and invoice</span></span>
1. <span data-ttu-id="4c4d6-122">[買掛金勘定] > [請求書] > [仕入帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="4c4d6-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-123">Click New.</span></span>
3. <span data-ttu-id="4c4d6-124">ルックアップを開いて、使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="4c4d6-125">使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="4c4d6-126">登録を開いて経費明細行を入力するには [明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="4c4d6-127">ルックアップで、仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="4c4d6-128">たとえば、「仕入先 1001」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="4c4d6-129">[請求書] フィールドに請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="4c4d6-130">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="4c4d6-131">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="4c4d6-132">[発注書] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="4c4d6-133">先ほど作成した発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="4c4d6-134">[承認者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="4c4d6-135">承認者を強調表示して [選択] をクリックすると、その承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="4c4d6-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-136">Click Post.</span></span>
15. <span data-ttu-id="4c4d6-137">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-137">Close the form.</span></span>
16. <span data-ttu-id="4c4d6-138">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="4c4d6-139">プールから請求書を開き、発注書と照合させ、請求書プロセスを完了させます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="4c4d6-140">[買掛金勘定] > [請求書] > [請求管理グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="4c4d6-141">[発注書] をクリックして、プール内の発注書から仕入先請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="4c4d6-142">確認する請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="4c4d6-143">[照合状態の更新] をクリックして、照合を完了させます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="4c4d6-144">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="4c4d6-145">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-145">Click Change view.</span></span>
7. <span data-ttu-id="4c4d6-146">[グリッド ビュー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-146">Click Grid view.</span></span>
8. <span data-ttu-id="4c4d6-147">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-147">Click Post.</span></span>
9. <span data-ttu-id="4c4d6-148">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-148">Close the form.</span></span>
10. <span data-ttu-id="4c4d6-149">[買掛金勘定] > [仕入先] > [仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="4c4d6-150">発注書に記載されていた仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="4c4d6-151">たとえば、「仕入先 1001」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="4c4d6-152">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4c4d6-153">[アクション] ウィンドウで、[仕入先] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="4c4d6-154">[トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-154">Click Transactions.</span></span>
15. <span data-ttu-id="4c4d6-155">作成した請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="4c4d6-156">仕入帳昇給額は取り消されて、適切な経費勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4c4d6-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

