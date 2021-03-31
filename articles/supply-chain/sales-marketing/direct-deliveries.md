---
title: 直納
description: この記事では、直納について説明します。 仕入先から顧客に直接配送する出荷のことを、直納といいます。
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20bf794a6ba2f0759b34afdefdd5fa65e3ad6b68
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224427"
---
# <a name="direct-deliveries"></a><span data-ttu-id="8992b-104">直納</span><span class="sxs-lookup"><span data-stu-id="8992b-104">Direct deliveries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8992b-105">この記事では、直納について説明します。</span><span class="sxs-lookup"><span data-stu-id="8992b-105">This article provides information about direct deliveries.</span></span> <span data-ttu-id="8992b-106">仕入先から顧客に直接配送する出荷のことを、直納といいます。</span><span class="sxs-lookup"><span data-stu-id="8992b-106">Direct deliveries are deliveries that are sent directly from the vendor to your customer.</span></span>

<span data-ttu-id="8992b-107">直納は、顧客に出荷するまで製品を倉庫に保管する必要がないため、配送時間と在庫持ち越し費用を節約できます。</span><span class="sxs-lookup"><span data-stu-id="8992b-107">Direct deliveries save delivery time and reduce the costs that are associated with carrying inventory, because you don't hold the products in your warehouse before you ship them to the customer.</span></span>  

<span data-ttu-id="8992b-108">**販売注文** ページで直納を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8992b-108">You can create direct deliveries from the **Sales order** page.</span></span> <span data-ttu-id="8992b-109">まず、販売注文と注文明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8992b-109">First, create a sales order and order lines.</span></span> <span data-ttu-id="8992b-110">次に、[アクション] ペインの **販売注文** タブで、**直納** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8992b-110">Then, on the Action Pane, on the **Sales order** tab, select **Direct delivery**.</span></span> <span data-ttu-id="8992b-111">最後に、直納として処理する明細行を指定します。</span><span class="sxs-lookup"><span data-stu-id="8992b-111">Finally, specify the lines that must be handled as a direct delivery.</span></span> <span data-ttu-id="8992b-112">直納の販売注文明細行と対応する購買注文明細行の間にリンクができます。</span><span class="sxs-lookup"><span data-stu-id="8992b-112">A link is now created between the sales order lines for the direct delivery and the corresponding purchase order lines.</span></span>  

<span data-ttu-id="8992b-113">**注記:** 注文された数量の一部が既に発送されている場合、残りの数量を分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8992b-113">**Note:** If part of the ordered quantity has already been delivered, you must split the remaining quantity.</span></span> <span data-ttu-id="8992b-114">直接出荷する必要がある数量で新規の行を作成し、元の明細行の数量からその数量を差し引きます。</span><span class="sxs-lookup"><span data-stu-id="8992b-114">Create a new line for the quantity that must be directly delivered, and subtract that quantity from the quantity on the original line.</span></span> <span data-ttu-id="8992b-115">たとえば、元の数量が 15 個で、5 個が発送された場合、10 個の残余数量の新しい明細行を作成して、その数量で元の数量を差し引きます。</span><span class="sxs-lookup"><span data-stu-id="8992b-115">For example, if the original quantity was 15, and five have been delivered, you must create a new line for the remaining quantity, 10, and then reduce the original quantity by that amount.</span></span>  

<span data-ttu-id="8992b-116">販売注文明細行と発注書明細行との間に直納リンクを作成したら、梱包明細で販売注文を更新できます。</span><span class="sxs-lookup"><span data-stu-id="8992b-116">After you create the direct delivery link between the sales order lines and the purchase order lines, you can update the sales order by using a packing slip.</span></span> <span data-ttu-id="8992b-117">発注書から梱包明細の更新または請求書の更新を実行します。</span><span class="sxs-lookup"><span data-stu-id="8992b-117">Run either a packing slip update or an invoice update from the purchase order.</span></span> <span data-ttu-id="8992b-118">**販売注文** ページから販売注文の請求書を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8992b-118">You must invoice-update the sales order from the **Sales order** page.</span></span> <span data-ttu-id="8992b-119">販売注文の請求書を更新して、受け付け時に登録した数量より数量をふやすことはできません。</span><span class="sxs-lookup"><span data-stu-id="8992b-119">An invoice update can't cause the quantity on the sales order to exceed the quantity that has been registered as received.</span></span> <span data-ttu-id="8992b-120">たとえば、販売注文明細行には 10 個とありますが、梱包明細では、販売注文明細行の 5 個だけが更新されました。</span><span class="sxs-lookup"><span data-stu-id="8992b-120">For example, a sales order line has 10 pieces, but only five pieces from the sales order line have been updated by using a packing slip.</span></span> <span data-ttu-id="8992b-121">販売注文の請求更新を行うときに **数量** リストで **すべて** を選択すると、物理的に受け取った品目や、梱包明細で更新した品目だけの請求書が更新されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-121">If you select **All** in the **Quantity** list when you invoice-update the sales order, only those items that have been physically received, or updated by using a packing slip, are invoice-updated.</span></span> <span data-ttu-id="8992b-122">すべての販売注文明細行が更新されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="8992b-122">The whole sales order line isn't updated.</span></span>

## <a name="delivery-date"></a><span data-ttu-id="8992b-123">配送日</span><span class="sxs-lookup"><span data-stu-id="8992b-123">Delivery date</span></span>
<span data-ttu-id="8992b-124">販売注文明細行の **入荷希望日** フィールドを更新すると、対応する購買注文明細行の **出荷日** フィールドも更新されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-124">When you update the **Requested receipt date** field on the sales order line, the **Delivery date** field on the corresponding purchase order line is also updated.</span></span> <span data-ttu-id="8992b-125">同じく、購買注文明細行の **確認済み** フィールドを更新すると、対応する販売注文明細行の **確定入荷日** フィールドと **確定出荷日** フィールドが更新されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-125">Similarly, when you update the **Confirmed** field on the purchase order line, the **Confirmed receipt date** and **Confirmed ship date** fields on the corresponding sales order line are also updated.</span></span>

## <a name="delivery-address"></a><span data-ttu-id="8992b-126">配送先住所</span><span class="sxs-lookup"><span data-stu-id="8992b-126">Delivery address</span></span>
<span data-ttu-id="8992b-127">通常、法人の住所が発注書の配送先住所になります。</span><span class="sxs-lookup"><span data-stu-id="8992b-127">Typically, the delivery address for a purchase order is the company's address.</span></span> <span data-ttu-id="8992b-128">ただし、直納を作成した場合、顧客の住所が配送先住所として入力されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-128">However, when you create a direct delivery, you enter the customer's address as the delivery address.</span></span> <span data-ttu-id="8992b-129">配送タイプが **直納** の発注書明細行の配送先住所を変更すると、対応する販売注文明細行の配送先住所も更新されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-129">If you change the delivery address on a purchase order line that has a delivery type of **Direct delivery**, the delivery address on the corresponding sales order line is also updated.</span></span> <span data-ttu-id="8992b-130">同じく、販売注文明細行の配送先住所を変更すると、購買注文明細行の配送先住所も更新されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-130">Similarly, if you change the delivery address on the sales order line, the delivery address on the purchase order line is also updated.</span></span>

## <a name="deleting-order-lines"></a><span data-ttu-id="8992b-131">注文明細行の削除</span><span class="sxs-lookup"><span data-stu-id="8992b-131">Deleting order lines</span></span>
<span data-ttu-id="8992b-132">配送タイプが **直納** の販売注文明細行を削除しようとすると、発注書明細行がその明細行に関連付けられていることを示すメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-132">If you try to delete a sales order line that has a delivery type of **Direct delivery**, a message box states that purchase order lines are attached to the line.</span></span> <span data-ttu-id="8992b-133">販売注文明細行の一部が出荷済みの場合、その明細行に関連付けられている販売注文明細行や発注書明細行は削除できません。</span><span class="sxs-lookup"><span data-stu-id="8992b-133">If the sales order line has been partially delivered, you can't delete the sales order line or the purchase order lines that are attached to it.</span></span>

## <a name="warehouse"></a><span data-ttu-id="8992b-134">倉庫</span><span class="sxs-lookup"><span data-stu-id="8992b-134">Warehouse</span></span>
<span data-ttu-id="8992b-135">直納を作成すると、販売する品目が倉庫に物理的に入庫することはありません。</span><span class="sxs-lookup"><span data-stu-id="8992b-135">When you create a direct delivery, the items that you sell never physically arrive at your warehouse.</span></span> <span data-ttu-id="8992b-136">ただし、販売注文明細行には倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8992b-136">However, you must still specify a warehouse on the sales order line.</span></span> <span data-ttu-id="8992b-137">同じく、その品目の品目モデル グループでピッキング要求が指定さる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8992b-137">Similarly, picking requirements might be specified on the item model group for the item.</span></span> <span data-ttu-id="8992b-138">ただし、品目は物理的に倉庫に入庫しないため、販売注文が直納の場合、これらの要求は無視されます。</span><span class="sxs-lookup"><span data-stu-id="8992b-138">However, because the items never physically arrive at your warehouse, these requirements are ignored when the sales order is a direct delivery.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]