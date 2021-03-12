---
title: 仕入先請求書の受領記録および入庫済数量との照合
description: 発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979266"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="22ceb-103">仕入先請求書の受領記録および入庫済数量との照合</span><span class="sxs-lookup"><span data-stu-id="22ceb-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22ceb-104">発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="22ceb-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="22ceb-105">始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="22ceb-106">[買掛金勘定パラメータ] ページで、[請求書照合の検証を有効にする] オプションがオンで、[明細行照合ポリシー] のフィールドが [承認の要求] に設定され、[明細行照合ポリシー] が [スリーウェイ マッチング] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="22ceb-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="22ceb-108">買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="22ceb-109">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="22ceb-109">Create a purchase order</span></span>
1. <span data-ttu-id="22ceb-110">[すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="22ceb-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-111">Click New.</span></span>
3. <span data-ttu-id="22ceb-112">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22ceb-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="22ceb-113">[仕入先] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="22ceb-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-114">Click OK.</span></span>
6. <span data-ttu-id="22ceb-115">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-115">Click Add line.</span></span>
7. <span data-ttu-id="22ceb-116">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="22ceb-117">アクション ウィンドウで、[購買] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="22ceb-118">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="22ceb-119">製品受領書の転記</span><span class="sxs-lookup"><span data-stu-id="22ceb-119">Post a product receipt</span></span>
1. <span data-ttu-id="22ceb-120">アクション ウィンドウで、[入庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="22ceb-121">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-121">Click Product receipt.</span></span>
3. <span data-ttu-id="22ceb-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="22ceb-123">[製品受領書] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="22ceb-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="22ceb-125">仕入先請求書の製品受領書との記録および照合</span><span class="sxs-lookup"><span data-stu-id="22ceb-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="22ceb-126">アクション ウィンドウで、[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="22ceb-127">[請求書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-127">Click Invoice.</span></span>
3. <span data-ttu-id="22ceb-128">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="22ceb-129">[既定の取得元: 注文済数量] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="22ceb-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="22ceb-130">[明細行の既定の数量] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="22ceb-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="22ceb-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-131">Click OK.</span></span>
7. <span data-ttu-id="22ceb-132">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-132">Click Yes.</span></span>
8. <span data-ttu-id="22ceb-133">[製品受領書の照合] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="22ceb-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-134">Click OK.</span></span>
10. <span data-ttu-id="22ceb-135">アクション ウィンドウで、[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="22ceb-136">[照合の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22ceb-136">Click Matching details.</span></span>

