---
title: 仕入先請求書を使用した AP の主請求書データ
description: このタスク ガイドでは、発注書から仕入先請求書を作成し、発注書、受領書、および請求書の照合結果 (スリーウェイ マッチング) を確認します。
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d3f9fc1fb7724632dbc9c4c3e1e28c6e85eaf61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827797"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="06b41-103">仕入先請求書を使用した AP の主請求書データ</span><span class="sxs-lookup"><span data-stu-id="06b41-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06b41-104">このタスク ガイドでは、発注書から仕入先請求書を作成し、発注書、受領書、および請求書の照合結果 (スリーウェイ マッチング) を確認します。</span><span class="sxs-lookup"><span data-stu-id="06b41-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="06b41-105">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="06b41-105">Create a purchase order</span></span>
1. <span data-ttu-id="06b41-106">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="06b41-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="06b41-107">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-107">Click **New**.</span></span>
3. <span data-ttu-id="06b41-108">**仕入先** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06b41-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="06b41-109">選択する仕入先を見つけます。</span><span class="sxs-lookup"><span data-stu-id="06b41-109">Find a vendor to select.</span></span> <span data-ttu-id="06b41-110">たとえば、US-104 にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="06b41-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="06b41-111">仕入先 US-104 を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="06b41-112">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-112">Click **OK**.</span></span>
7. <span data-ttu-id="06b41-113">**品目番号** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06b41-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="06b41-114">在庫品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-114">Select an inventory item.</span></span> <span data-ttu-id="06b41-115">たとえば、品目番号「1000」を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="06b41-116">**行の詳細** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="06b41-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="06b41-117">**設定** タブをクリックします。照合ポリシーはマッチングなし、ツーウェイ マッチング、スリーウェイ マッチングのいずれかで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="06b41-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="06b41-118">アクション ウィンドウで、**購買** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="06b41-119">**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="06b41-120">製品の入庫</span><span class="sxs-lookup"><span data-stu-id="06b41-120">Receive the products</span></span>
1. <span data-ttu-id="06b41-121">アクション ウィンドウで、**受入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="06b41-122">**製品受領書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="06b41-123">**製品受領書** フィールドに、製品受領書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="06b41-124">たとえば、「PR123」を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="06b41-125">**OK** をクリックして、製品受領書を転記します。</span><span class="sxs-lookup"><span data-stu-id="06b41-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="06b41-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06b41-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="06b41-127">仕入先請求書の作成</span><span class="sxs-lookup"><span data-stu-id="06b41-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="06b41-128">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > 受入済未請求発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="06b41-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="06b41-129">作成した発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="06b41-130">アクション ウィンドウで、**請求書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="06b41-131">**請求書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="06b41-132">**番号** フィールドに請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="06b41-133">**請求明細** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="06b41-134">**請求日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="06b41-135">**単価** フィールドに 1200 と入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="06b41-136">**行の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-136">Click **Add line**.</span></span>
10. <span data-ttu-id="06b41-137">**品目番号** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06b41-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="06b41-138">リストで、設置費用の品目番号を見つけます。</span><span class="sxs-lookup"><span data-stu-id="06b41-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="06b41-139">例: S0001</span><span class="sxs-lookup"><span data-stu-id="06b41-139">For example, S0001</span></span>
12. <span data-ttu-id="06b41-140">設置費用の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-140">Select the installation charge item number.</span></span> <span data-ttu-id="06b41-141">変更があったために、照合が行われなかったことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="06b41-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="06b41-142">**照合状態の更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="06b41-143">アクション ウィンドウで、**確認** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="06b41-144">**照合の詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-144">Click **Matching details**.</span></span> <span data-ttu-id="06b41-145">サービスを持つ新しい行は、照合を行う必要がないため、ステータスは「実行されませんでした」のままになります。</span><span class="sxs-lookup"><span data-stu-id="06b41-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="06b41-146">受領した在庫品目の製品受領書を選択します。</span><span class="sxs-lookup"><span data-stu-id="06b41-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="06b41-147">製品受領書を含む明細行は照合されましたが、数量または価格の不一致があるため失敗しています。</span><span class="sxs-lookup"><span data-stu-id="06b41-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="06b41-148">**単価** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06b41-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="06b41-149">単価が一致したので、ステータスは「成功」に更新されます。</span><span class="sxs-lookup"><span data-stu-id="06b41-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="06b41-150">不一致を許容するポリシーの場合、または照合が警告だけの場合、請求書は転記できます。</span><span class="sxs-lookup"><span data-stu-id="06b41-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="06b41-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06b41-151">Close the page.</span></span>
19. <span data-ttu-id="06b41-152">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06b41-152">Click **Post**.</span></span>
20. <span data-ttu-id="06b41-153">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06b41-153">Close the form.</span></span> <span data-ttu-id="06b41-154">発注書が受入済未請求として一覧に現れないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="06b41-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]