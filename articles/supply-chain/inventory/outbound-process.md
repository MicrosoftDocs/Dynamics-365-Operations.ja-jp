---
title: 出荷プロセスの概要
description: このトピックでは、在庫管理の出荷プロセスの概要を示します。
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 24406f107d796891c315b39d3eff4351ae0aa5be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209686"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="ba31d-103">出荷プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="ba31d-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba31d-104">このトピックでは、在庫管理の出荷プロセスの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="ba31d-105">出荷注文</span><span class="sxs-lookup"><span data-stu-id="ba31d-105">Output orders</span></span>

<span data-ttu-id="ba31d-106">出荷注文は、販売注文明細行をリンクしたり、ピッキング リストを使用する出荷ピッキング プロセスの注文明細行を転送するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="ba31d-107">ピッキング リストは、販売注文または移動オーダーのいずれかから生成され、出荷注文と出荷が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="ba31d-108">ピッキング リストには、出荷で 1 対 1 の関係があります。</span><span class="sxs-lookup"><span data-stu-id="ba31d-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="ba31d-109">移動オーダー出荷または販売注文の梱包明細票は、出荷から処理することができます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="ba31d-110">次の図に、出荷注文のプロセスの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="ba31d-111">[![出荷注文プロセスの概要](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="ba31d-112">出荷ルールを設定することにより、プログラムでの出荷処理方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="ba31d-113">これらのルールを使用し、出荷プロセスを制御できます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="ba31d-114">特に、出荷を送信するプロセスのどのステージを制御するかで、ルールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="ba31d-115">次の設定では、出荷プロセスの処理方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="ba31d-116">販売および移動オーダーのピッキング ルートのステータス</span><span class="sxs-lookup"><span data-stu-id="ba31d-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="ba31d-117">**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** の順に移動し、**更新** タブで、**ピッキング ルートのステータス** フィールドの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="ba31d-118">[![販売注文のピッキング ルート ステータス フィールド](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="ba31d-119">**ピッキング ルートのステータス** フィールドが **完了** 設定されると、ピッキング リストを生成するプロセスの一部として、ピッキング プロセスが自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="ba31d-120">このフィールドが **有効化** に設定されている場合、ピッキング リスト明細行は手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba31d-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="ba31d-121">同じ設定が移動オーダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="ba31d-122">**在庫管理** \> **設定** \> **在庫および倉庫管理パラメーター** の順に移動し、**配送** タブで、**ピッキング ルートのステータス** フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="ba31d-123">[![移動オーダーのピッキング ルート ステータス フィールド](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="ba31d-124">在庫出荷注文の終了</span><span class="sxs-lookup"><span data-stu-id="ba31d-124">End output inventory orders</span></span>

<span data-ttu-id="ba31d-125">**在庫管理** \> **設定** \> **在庫および倉庫管理パラメーター** の順に移動し、**一般** タブで、**在庫出荷注文の終了** オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="ba31d-126">[![在庫出荷注文の終了オプション](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="ba31d-127">倉庫作業員が、ピッキング リスト数量を削減するときに、対応する在庫注文数量は出荷から削除されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="ba31d-128">ピッキング リストがある時点で更新されると、**在庫出荷注文の終了** オプションが **はい** に設定されている場合、残りの数量は注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ba31d-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="ba31d-129">**在庫出荷注文の終了** オプションが **いいえ** に設定されている場合、残りの数量は出荷注文の数量として維持され、**出荷注文を開く** 機能の一部として新しいピッキング リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba31d-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="ba31d-130">[![[機能] メニューで [出荷注文を開く] コマンド](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="ba31d-131">[![[出荷注文を開く] ページの [機能] メニュー](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="ba31d-132">数量の削減</span><span class="sxs-lookup"><span data-stu-id="ba31d-132">Reduce quantity</span></span>

<span data-ttu-id="ba31d-133">ピッキング リストを生成するプロセスの一部として使用できる 3 番目のパラメーターは、**数量の削減** パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="ba31d-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="ba31d-134">このパラメーターの設定は、**引当** 設定と強調し、引当プロセスを倉庫へのリリースの一部としてトリガーします。</span><span class="sxs-lookup"><span data-stu-id="ba31d-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="ba31d-135">[![数量の削減パラメーター](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="ba31d-136">販売注文の出荷プロセスの例</span><span class="sxs-lookup"><span data-stu-id="ba31d-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="ba31d-137">この例では、2 つの品目の販売注文があります。</span><span class="sxs-lookup"><span data-stu-id="ba31d-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="ba31d-138">ピッキング リストの生成時に、**数量の削減** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="ba31d-139">したがって、使用可能な手持在庫に対してのみ、ピッキング明細行をリリースおよび作成します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="ba31d-140">ピッキング リストの登録プロセスを介したピッキングを報告する必要があります (**ピッキング ルートのステータス** = **有効化**)。</span><span class="sxs-lookup"><span data-stu-id="ba31d-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="ba31d-141">まだ引当されていない在庫は、ピッキング リストの生成時に引当されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="ba31d-142">在庫がピッキング可能な場合、使用できない在庫は販売注文から削除されるか、または後で発信処理として倉庫へのリリースされるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="ba31d-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="ba31d-143">[![ピッキング リストの更新](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="ba31d-144">**ピッキング リスト登録** ページですべてのピッキング ラインがピッキングされるとすぐに、関連付けられている出荷が完了します。</span><span class="sxs-lookup"><span data-stu-id="ba31d-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="ba31d-145">販売注文の梱包明細のプロセスは、ピッキング済の在庫に基づいて初期化されます。</span><span class="sxs-lookup"><span data-stu-id="ba31d-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="ba31d-146">[![出荷配送の更新](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="ba31d-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]