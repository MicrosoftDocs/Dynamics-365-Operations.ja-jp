---
title: 仕入先請求書を使用した AP システムの主請求書データ
description: このタスク ガイドでは、発注書から仕入先請求書を作成し、発注書、受領書、および請求書の照合結果 (スリーウェイ マッチング) を確認します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569635"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="c0685-103">仕入先請求書を使用した AP システムの主請求書データ</span><span class="sxs-lookup"><span data-stu-id="c0685-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0685-104">このタスク ガイドでは、発注書から仕入先請求書を作成し、発注書、受領書、および請求書の照合結果 (スリーウェイ マッチング) を確認します。</span><span class="sxs-lookup"><span data-stu-id="c0685-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="c0685-105">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="c0685-105">Create a purchase order</span></span>
1. <span data-ttu-id="c0685-106">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c0685-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c0685-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-107">Click New.</span></span>
3. <span data-ttu-id="c0685-108">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c0685-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c0685-109">選択する仕入先を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c0685-109">Find a vendor to select.</span></span> <span data-ttu-id="c0685-110">たとえば、US-104 にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="c0685-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="c0685-111">仕入先 US-104 を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="c0685-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-112">Click OK.</span></span>
7. <span data-ttu-id="c0685-113">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c0685-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c0685-114">在庫品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-114">Select an inventory item.</span></span> <span data-ttu-id="c0685-115">たとえば、品目番号「1000」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="c0685-116">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="c0685-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="c0685-117">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="c0685-118">照合ポリシーは、マッチングなし、ツーウェイ マッチング、スリーウェイ マッチングのいずれかで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="c0685-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="c0685-119">[明細行の詳細] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="c0685-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="c0685-120">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="c0685-121">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="c0685-122">製品の入庫</span><span class="sxs-lookup"><span data-stu-id="c0685-122">Receive the products</span></span>
1. <span data-ttu-id="c0685-123">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="c0685-124">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-124">Click Product receipt.</span></span>
3. <span data-ttu-id="c0685-125">[製品受領書] フィールドに、製品受領書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="c0685-126">たとえば、「PR123」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="c0685-127">[OK] をクリックして、製品受領書を転記します。</span><span class="sxs-lookup"><span data-stu-id="c0685-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="c0685-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0685-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="c0685-129">仕入先請求書の作成</span><span class="sxs-lookup"><span data-stu-id="c0685-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="c0685-130">[買掛金勘定] > [発注書] > [受入済未請求発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c0685-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="c0685-131">作成した発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="c0685-132">[アクション] ペインで [請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="c0685-133">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-133">Click Invoice.</span></span>
5. <span data-ttu-id="c0685-134">[番号] フィールドに請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="c0685-135">[請求明細] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="c0685-136">[請求日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="c0685-137">[単価] フィールドに「1200」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="c0685-138">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-138">Click Add line.</span></span>
10. <span data-ttu-id="c0685-139">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c0685-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c0685-140">リストで、設置費用の品目番号を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c0685-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="c0685-141">例: S0001</span><span class="sxs-lookup"><span data-stu-id="c0685-141">For example, S0001</span></span>
12. <span data-ttu-id="c0685-142">設置費用の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="c0685-143">変更があったために、照合が行われなかったことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c0685-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="c0685-144">[照合状態の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-144">Click Update match status.</span></span>
14. <span data-ttu-id="c0685-145">アクション ウィンドウで、[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="c0685-146">[照合の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-146">Click Matching details.</span></span>
    * <span data-ttu-id="c0685-147">サービスを持つ新しい行は、照合を行う必要がないため、ステータスは「実行されませんでした」のままになります。</span><span class="sxs-lookup"><span data-stu-id="c0685-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="c0685-148">受領した在庫品目の製品受領書を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0685-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="c0685-149">製品受領書を含む明細行は照合されましたが、数量または価格の不一致があるため失敗しています。</span><span class="sxs-lookup"><span data-stu-id="c0685-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="c0685-150">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0685-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="c0685-151">単価が一致したので、ステータスは「成功」に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c0685-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="c0685-152">不一致を許容するポリシーの場合、または照合が警告だけの場合、請求書は転記できます。</span><span class="sxs-lookup"><span data-stu-id="c0685-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="c0685-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0685-153">Close the page.</span></span>
19. <span data-ttu-id="c0685-154">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0685-154">Click Post.</span></span>
20. <span data-ttu-id="c0685-155">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0685-155">Close the form.</span></span>
    * <span data-ttu-id="c0685-156">発注書が受入済未請求として一覧に現れないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c0685-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

