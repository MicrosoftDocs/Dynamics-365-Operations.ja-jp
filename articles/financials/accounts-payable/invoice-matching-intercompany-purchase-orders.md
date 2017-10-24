---
title: "請求書照合と会社間発注"
description: "会社間の売買取引に関連する購買側の法人が、買掛金勘定の請求書照合を使用する設定になる場合があります。 その場合、会社間の売買取引と買掛金勘定の請求書照合の両方の転記要件が合っていないと、会社間仕入先請求書は転記できません。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: affdffd5e73958788ed2a5a4959eea71024140ab
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a><span data-ttu-id="3fe23-104">請求書照合と会社間発注</span><span class="sxs-lookup"><span data-stu-id="3fe23-104">Invoice matching and intercompany purchase orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3fe23-105">会社間の売買取引に関連する購買側の法人が、買掛金勘定の請求書照合を使用する設定になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3fe23-105">The purchasing legal entity that is involved in an intercompany trade transaction might be set up to use accounts payable invoice matching.</span></span> <span data-ttu-id="3fe23-106">その場合、会社間の売買取引と買掛金勘定の請求書照合の両方の転記要件が合っていないと、会社間仕入先請求書は転記できません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-106">In this case, the posting requirements for both intercompany trade and accounts payable invoice matching must be met before intercompany vendor invoices can be posted.</span></span>

<span data-ttu-id="3fe23-107">このトピックの例では、会社間取引に次の設定を使用します:</span><span class="sxs-lookup"><span data-stu-id="3fe23-107">The examples in this topic use the following setup for intercompany trade:</span></span>
-   <span data-ttu-id="3fe23-108">Fabrikam Purchase は、購買側の法人です。</span><span class="sxs-lookup"><span data-stu-id="3fe23-108">Fabrikam Purchase is the purchasing legal entity.</span></span>
-   <span data-ttu-id="3fe23-109">Fabrikam Sales は、販売側の法人です。</span><span class="sxs-lookup"><span data-stu-id="3fe23-109">Fabrikam Sales is the selling legal entity.</span></span>
-   <span data-ttu-id="3fe23-110">顧客 4020 が Fabrikam Sales に存在します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-110">Customer 4020 exists in Fabrikam Sales.</span></span>
-   <span data-ttu-id="3fe23-111">仕入先 3024 が Fabrikam Purchase に存在します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-111">Vendor 3024 exists in Fabrikam Purchase.</span></span>
-   <span data-ttu-id="3fe23-112">Fabrikam Purchase では、会社間の情報がベンダー 3024 に指定されています。</span><span class="sxs-lookup"><span data-stu-id="3fe23-112">In Fabrikam Purchase, intercompany information is specified for vendor 3024.</span></span> <span data-ttu-id="3fe23-113">Fabrikam Sales は顧客会社として指定され、顧客 4020 は Fabrikam Purchase 法人に対応する顧客アカウントとして指定されています。</span><span class="sxs-lookup"><span data-stu-id="3fe23-113">Fabrikam Sales is specified as the customer company, and customer 4020 is specified as the customer account that corresponds to the Fabrikam Purchase legal entity.</span></span>
-   <span data-ttu-id="3fe23-114">Fabrikam Sales では、顧客 4020 の会社間の情報が指定されています。</span><span class="sxs-lookup"><span data-stu-id="3fe23-114">In Fabrikam Sales, intercompany information is specified for customer 4020.</span></span> <span data-ttu-id="3fe23-115">Fabrikam Purchase はベンダー会社として指定され、ベンダー 3024 は Fabrikam Sales 法人に対応するベンダー アカウントとして指定されています。</span><span class="sxs-lookup"><span data-stu-id="3fe23-115">Fabrikam Purchase is specified as the vendor company, and vendor 3024 is specified as the vendor account that corresponds to the Fabrikam Sales legal entity.</span></span>

<span data-ttu-id="3fe23-116">これらの例では、Fabrikam Purchase の買掛金勘定の請求書照合に以下の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-116">The examples use the following setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="3fe23-117">買掛金勘定パラメーター ページで [請求書照合の検証を有効化] オプションが選択されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-117">On the Accounts payable parameters page, the Enable invoice matching validation option is selected.</span></span>
-   <span data-ttu-id="3fe23-118">買掛金管理パラメーター ページの [不一致のある請求書を転記] フィールドが [承認の要求] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-118">On the Accounts payable parameters page, the Post invoice with discrepancies field is set to Require approval.</span></span>
-   <span data-ttu-id="3fe23-119">この法人の価格許容値の割合は 2% です。</span><span class="sxs-lookup"><span data-stu-id="3fe23-119">The price tolerance percentage for the legal entity is 2 percent.</span></span>

## <a name="example-price-matching-and-intercompany-trade"></a><span data-ttu-id="3fe23-120">例 : 価格照合と会社間売買</span><span class="sxs-lookup"><span data-stu-id="3fe23-120">Example: Price matching and intercompany trade</span></span>
<span data-ttu-id="3fe23-121">会社間仕入先請求書と会社間顧客請求書の正味金額は同額でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-121">The net amounts for the intercompany vendor invoice and the intercompany customer invoice must be equal.</span></span> <span data-ttu-id="3fe23-122">この要件は、該当するいかなる請求書照合の承認または価格許容率よりも優先します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-122">This requirement overrides any invoice matching approvals or price tolerance percentages that apply.</span></span> <span data-ttu-id="3fe23-123">たとえば、次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-123">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="3fe23-124">Fabrikam Purchase で、顧客 4020 の販売注文 SO888 を作成します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-124">In Fabrikam Purchase, create sales order SO888 for customer 4020.</span></span> <span data-ttu-id="3fe23-125">Fabrikam Purchase に、仕入先 3024 に会社間発注書 ICPO222 が自動的に作成され、Fabrikam Sales では、販売注文 ICSO888 が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-125">Intercompany purchase order ICPO222 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO888 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="3fe23-126">Fabrikam Sales に、品目が受領済みであると登録し、梱包明細を転記します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-126">In Fabrikam Sales, register that the items have been received, and post a packing slip.</span></span> <span data-ttu-id="3fe23-127">ICSO888 の状態が [出荷済み] に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-127">The status of ICSO888 changes to Delivered.</span></span> <span data-ttu-id="3fe23-128">ICPO222 の状態が [受入済] に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-128">The status of ICPO222 changes to Received.</span></span>
3.  <span data-ttu-id="3fe23-129">Fabrikam Sales で、ICSO888 の請求書を更新します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-129">In Fabrikam Sales, perform an invoice update for ICSO888.</span></span> <span data-ttu-id="3fe23-130">単価 0.45 で数量 100 が更新されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-130">The unit price is 0.45, and 100 items are updated.</span></span>
4.  <span data-ttu-id="3fe23-131">Fabrikam Purchase で、ICPO222 の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-131">In Fabrikam Purchase, create an invoice for ICPO222.</span></span> <span data-ttu-id="3fe23-132">誤って正味価格を 45.00 から 54.00 に変更しました。</span><span class="sxs-lookup"><span data-stu-id="3fe23-132">You accidentally change the net price from 45.00 to 54.00.</span></span> <span data-ttu-id="3fe23-133">価格が 2% の価格許容率を超えていることを示すアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-133">An icon is displayed to indicate that the price exceeds the allowable price tolerance of 2 percent.</span></span>
5.  <span data-ttu-id="3fe23-134">請求書照合の詳細ページで、[照合不一致を伴う転記を承認する] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-134">On the Invoice matching details page, select the option to approve posting with matching discrepancies.</span></span> <span data-ttu-id="3fe23-135">仕入先請求書ページで、[OK] をクリックします。仕入先請求書が会社間仕入先請求書ではない場合、転記できません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-135">On the Vendor invoice page, click OK.If the vendor invoice was not an intercompany vendor invoice, posting would be successful.</span></span> <span data-ttu-id="3fe23-136">しかし、処理しているのは会社間仕入先請求書なので、転記できません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-136">However, because you are working with an intercompany vendor invoice, posting is unsuccessful.</span></span> <span data-ttu-id="3fe23-137">会社間の売買取引で、会社間販売注文書の請求合計金額は、対応する会社間発注の請求合計金額と一致していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-137">For intercompany trade, the invoice totals on the intercompany sales order must equal the invoice totals on the corresponding intercompany purchase order.</span></span> <span data-ttu-id="3fe23-138">この問題を解決するため、正味価格を既定の金額 45.00 に戻して、請求書の正味価格を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fe23-138">To resolve this issue, you must correct the net price on the invoice by changing the net price back to the default amount, 45.00.</span></span>

## <a name="example-quantity-matching-with-intercompany-trade"></a><span data-ttu-id="3fe23-139">例 : 会社間取引の数量照合</span><span class="sxs-lookup"><span data-stu-id="3fe23-139">Example: Quantity matching with intercompany trade</span></span>
<span data-ttu-id="3fe23-140">会社間発注書と会社間販売注文書の数量は一致していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-140">The quantities on the intercompany purchase order and the intercompany sales order must be equal.</span></span> <span data-ttu-id="3fe23-141">この要件は、該当する請求書照合のいかなる承認よりも優先します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-141">This requirement overrides any invoice matching approvals that apply.</span></span> <span data-ttu-id="3fe23-142">この例では、会社間取引で以下の追加設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-142">This example uses the following additional setup for intercompany trade:</span></span>
-   <span data-ttu-id="3fe23-143">Fabrikam Purchase で、仕入先 3024 の発注書のアクション ポリシーを、元の顧客請求書と会社間仕入先請求書の両方で自動的に転記するよう設定します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-143">In Fabrikam Purchase, the purchase order action policy for vendor 3024 is set up to automatically post both the original customer invoice and the intercompany vendor invoice.</span></span>

<span data-ttu-id="3fe23-144">この例では、Fabrikam Purchase に、以下の追加の買掛金勘定の請求書照合の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-144">This example uses the following additional setup for accounts payable invoice matching for Fabrikam Purchase:</span></span>
-   <span data-ttu-id="3fe23-145">品目 B-R14 で使用するモデル グループの品目モデル グループのページで、入荷の条件のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-145">On the Item model groups page for the model group that is used by item B-R14, the Receiving requirements option is selected.</span></span>
-   <span data-ttu-id="3fe23-146">品目 B-R14 の手持数量は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3fe23-146">The on-hand quantity for item B-R14 is 0 (zero).</span></span>

<span data-ttu-id="3fe23-147">たとえば、次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-147">For example, you follow these steps.</span></span>
1.  <span data-ttu-id="3fe23-148">Fabrikam Purchase で、顧客 4020 の販売注文 SO999 を作成します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-148">In Fabrikam Purchase, create sales order SO999 for customer 4020.</span></span> <span data-ttu-id="3fe23-149">この注文には 1 つの明細行品目 : 電池 100 個 (品目 B-R14)、単価 1.00 があります。</span><span class="sxs-lookup"><span data-stu-id="3fe23-149">The order contains one line item: 100 batteries (item B-R14) at a unit price of 1.00 each.</span></span> <span data-ttu-id="3fe23-150">Fabrikam Purchase に、仕入先 3024 に会社間発注書 ICPO333 が自動的に作成され、Fabrikam Sales では、販売注文 ICSO999 が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-150">Intercompany purchase order ICPO333 is automatically created for vendor 3024 in Fabrikam Purchase, and sales order ICSO999 is automatically created in Fabrikam Sales.</span></span>
2.  <span data-ttu-id="3fe23-151">Fabrikam Sales で ICSO999 の請求書を更新します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-151">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="3fe23-152">品目が在庫切れで、まだ受領されていないので、転記は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-152">Posting is unsuccessful, because the item is out of stock and has not yet been received.</span></span> <span data-ttu-id="3fe23-153">したがって、財務情報は更新できません。</span><span class="sxs-lookup"><span data-stu-id="3fe23-153">Therefore, the financial information cannot be updated.</span></span>
3.  <span data-ttu-id="3fe23-154">Fabrikam Sales で、品目の受領を登録し、ICSO999 の梱包明細を転記します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-154">In Fabrikam Sales, register that the items have been received, and post a packing slip for ICSO999.</span></span> <span data-ttu-id="3fe23-155">ICPO333 の製品受領書が Fabrikam Purchase に自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="3fe23-155">A product receipt for ICPO333 is automatically posted in Fabrikam Purchase.</span></span> <span data-ttu-id="3fe23-156">Fabrikam Purchase の品目 B-R14 の受領数量は 100 に変化します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-156">In Fabrikam Purchase, the received quantity for item B-R14 changes to 100.</span></span>
4.  <span data-ttu-id="3fe23-157">Fabrikam Sales で ICSO999 の請求書を更新します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-157">In Fabrikam Sales, perform an invoice update for ICSO999.</span></span> <span data-ttu-id="3fe23-158">両方の法人で転記が成功します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-158">Posting is successful in both legal entities.</span></span> <span data-ttu-id="3fe23-159">Fabrikam Purchase の品目 B-R14 の購買済数量は 100 に変化します。</span><span class="sxs-lookup"><span data-stu-id="3fe23-159">In Fabrikam Purchase, the quantity that is purchased for item B-R14 changes to 100.</span></span>






