---
title: "検査指示"
description: "このトピックは、在庫をブロックする検査指示の使用方法について説明します。"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e77411bbfd5cb2ef09f63bbd0cd6c3441af49d05
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="quarantine-orders"></a><span data-ttu-id="53a9d-103">検査指示</span><span class="sxs-lookup"><span data-stu-id="53a9d-103">Quarantine orders</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="53a9d-104">このトピックは、在庫をブロックする検査指示の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53a9d-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="53a9d-105">検査指示は、在庫をブロックするのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="53a9d-106">たとえば、 品質テストの理由で品目を検査する場合があります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="53a9d-107">検査された在庫は、検査倉庫に転送されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="53a9d-108">**注記:** 高度な倉庫管理プロセス (倉庫管理で) を使用している場合、検査指示の処理は返品販売注文に対してのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="53a9d-109">手持在庫品目の検査</span><span class="sxs-lookup"><span data-stu-id="53a9d-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="53a9d-110">品目を検査する場合、検査指示を手動で作成するか、受信処理時に検査指示を自動的に作成するようにシステムを設定するかのいずれかが可能です。</span><span class="sxs-lookup"><span data-stu-id="53a9d-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="53a9d-111">検査指示を自動的に作成するには、[**品目モデル グループ**] ページの [**在庫ポリシー**] タブの [**検査管理**] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="53a9d-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="53a9d-112">また、入荷倉庫について、[**検査倉庫**] フィールドで既定の検査倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="53a9d-113">Microsoft Dynamics 365 for Finance and Operations では、現物手持在庫が発注書または製造オーダーで記録されると、検査品目は検査倉庫に自動的に移動されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="53a9d-114">この移動は、検査指示のステータスが**開始済**に変更されるため、実行されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="53a9d-115">検査指示を手動で作成する場合、品目は、関連する品目モデル グループで検査管理のために設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="53a9d-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="53a9d-116">このプロセスでは、検査する手持在庫と、使用する検査倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="53a9d-117">プロセスの計画を支援するために、検査指示のステータスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="53a9d-118">検査指示のステータス</span><span class="sxs-lookup"><span data-stu-id="53a9d-118">Quarantine order statuses</span></span>
<span data-ttu-id="53a9d-119">検査指示には次のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="53a9d-120">作成済み</span><span class="sxs-lookup"><span data-stu-id="53a9d-120">Created</span></span>
-   <span data-ttu-id="53a9d-121">開始済</span><span class="sxs-lookup"><span data-stu-id="53a9d-121">Started</span></span>
-   <span data-ttu-id="53a9d-122">完了レポート済</span><span class="sxs-lookup"><span data-stu-id="53a9d-122">Reported as finished</span></span>
-   <span data-ttu-id="53a9d-123">終了済</span><span class="sxs-lookup"><span data-stu-id="53a9d-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="53a9d-124">作成済み</span><span class="sxs-lookup"><span data-stu-id="53a9d-124">Created</span></span>

<span data-ttu-id="53a9d-125">検査指示のステータスが**作成済**になるのは、検査指示が手動で作成されているが、まだ品目が検査倉庫に配置されていない場合です。</span><span class="sxs-lookup"><span data-stu-id="53a9d-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="53a9d-126">2 つの在庫トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="53a9d-127">1 つ目のトランザクションは**注文中**、**引当済現物**、または**ピッキング済**のステータスがある払出トランザクションです。</span><span class="sxs-lookup"><span data-stu-id="53a9d-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="53a9d-128">2 つ目のトランザクションは、検査倉庫に**注文済**または**登録済**のステータスがある受入トランザクションです。</span><span class="sxs-lookup"><span data-stu-id="53a9d-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="53a9d-129">通常のプロセスで在庫への更新を引当、ピック、または登録できます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="53a9d-130">開始済</span><span class="sxs-lookup"><span data-stu-id="53a9d-130">Started</span></span>

<span data-ttu-id="53a9d-131">検査指示のステータスが**開始済**になると、在庫は通常の倉庫から検査倉庫へ移動され、2 つの在庫トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="53a9d-132">1 つのトランザクションには**払出済**のステータスがあり、もう一方のトランザクションには**受取済**のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="53a9d-133">同時に、戻りの転送を処理するための 2 つの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="53a9d-134">これらのトランザクションは日付がありません。</span><span class="sxs-lookup"><span data-stu-id="53a9d-134">These transactions aren't dated.</span></span> <span data-ttu-id="53a9d-135">1 つのトランザクションには**引当済現物**のステータスがあり、もう一方のトランザクションには**注文済**のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="53a9d-136">完了レポート済</span><span class="sxs-lookup"><span data-stu-id="53a9d-136">Reported as finished</span></span>

<span data-ttu-id="53a9d-137">**完了レポート**をクリックすると、開始された検査指示の完了を報告できます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="53a9d-138">品目は検査からリリースされますが、まだ通常の倉庫に戻されてはいません。</span><span class="sxs-lookup"><span data-stu-id="53a9d-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="53a9d-139">通常の倉庫への返送は、完了レポート プロセス時に初期化される着荷仕訳帳によって処理できます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="53a9d-140">終了済</span><span class="sxs-lookup"><span data-stu-id="53a9d-140">Ended</span></span>

<span data-ttu-id="53a9d-141">検査指示が終了すると、品目は検査倉庫から通常の倉庫に戻ります。</span><span class="sxs-lookup"><span data-stu-id="53a9d-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="53a9d-142">品目トランザクションのステータスは、検査倉庫で**売却済**に、そして通常の倉庫で**購買済**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="53a9d-143">検査指示仕損</span><span class="sxs-lookup"><span data-stu-id="53a9d-143">Quarantine order scrap</span></span>
<span data-ttu-id="53a9d-144">検査指示のプロセスの一環として、在庫の仕損ができます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="53a9d-145">仕損を処理するときは、在庫のステータスは検査倉庫からの払出トランザクションによって**売却済**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="53a9d-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="53a9d-146">参照</span><span class="sxs-lookup"><span data-stu-id="53a9d-146">See also</span></span>
--------

[<span data-ttu-id="53a9d-147">在庫ブロック</span><span class="sxs-lookup"><span data-stu-id="53a9d-147">Inventory blocking</span></span>](inventory-blocking.md)

