--- 
title: "請求書および AP システムの重要データの監査"
description: "発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="cb68c-103">請求書および AP システムの重要データの監査</span><span class="sxs-lookup"><span data-stu-id="cb68c-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb68c-104">発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb68c-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="cb68c-105">始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="cb68c-106">[買掛金勘定パラメータ] ページで、[請求書照合の検証を有効にする] オプションがオンで、[明細行照合ポリシー] のフィールドが [承認の要求] に設定され、[明細行照合ポリシー] が [スリーウェイ マッチング] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="cb68c-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="cb68c-108">買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="cb68c-109">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="cb68c-109">Create a purchase order</span></span>
1. <span data-ttu-id="cb68c-110">**すべての発注書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="cb68c-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-111">Click **New**.</span></span>
3. <span data-ttu-id="cb68c-112">**仕入先口座**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="cb68c-113">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-113">Click **OK**.</span></span>
5. <span data-ttu-id="cb68c-114">**行の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-114">Click **Add line**.</span></span>
6. <span data-ttu-id="cb68c-115">**品目番号**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="cb68c-116">アクション ウィンドウで、**購買**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="cb68c-117">**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="cb68c-118">製品受領書の転記</span><span class="sxs-lookup"><span data-stu-id="cb68c-118">Post a product receipt</span></span>
1. <span data-ttu-id="cb68c-119">アクション ウィンドウで、**受入**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="cb68c-120">**製品受領書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="cb68c-121">**製品受領書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="cb68c-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="cb68c-123">仕入先請求書の製品受領書との記録および照合</span><span class="sxs-lookup"><span data-stu-id="cb68c-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="cb68c-124">アクション ウィンドウで、**請求書 > 請求書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="cb68c-125">**数**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="cb68c-126">**既定の取得元: 注文済数量**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="cb68c-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="cb68c-127">**明細行の既定の数量**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cb68c-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="cb68c-128">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-128">Click **OK**.</span></span>
6. <span data-ttu-id="cb68c-129">**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-129">Click **Yes**.</span></span>
7. <span data-ttu-id="cb68c-130">**製品受領書の照合**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="cb68c-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-131">Click **OK**.</span></span>
9. <span data-ttu-id="cb68c-132">アクション ウィンドウで、**確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="cb68c-133">**照合の詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb68c-133">Click **Matching details**.</span></span>


