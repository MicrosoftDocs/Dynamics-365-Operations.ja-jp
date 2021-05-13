---
title: 検査指示
description: このトピックは、検査指示を使用して在庫をブロックする方法について説明します。
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956185"
---
# <a name="quarantine-orders"></a><span data-ttu-id="f2346-103">検査指示</span><span class="sxs-lookup"><span data-stu-id="f2346-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2346-104">このトピックは、検査指示を使用して在庫をブロックする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2346-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="f2346-105">検査指示により在庫をブロックできます。</span><span class="sxs-lookup"><span data-stu-id="f2346-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="f2346-106">たとえば、 品質テストの理由で品目を検査する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f2346-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="f2346-107">検査された在庫は、検査倉庫に転送されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="f2346-108">高度な倉庫管理プロセス (倉庫管理で) を使用している場合、検査指示の処理は返品販売注文に対してのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="f2346-109">手持在庫品目の検査</span><span class="sxs-lookup"><span data-stu-id="f2346-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="f2346-110">品目を検査する場合、検査指示を手動で作成するか、受信処理時に検査指示を自動的に作成するようにシステムを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f2346-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="f2346-111">検査指示を自動的に生成するようにシステムを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f2346-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="f2346-112">**在庫管理 \> 設定 \> 在庫 \> 品目モデル グループ** の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="f2346-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="f2346-113">リスト ペインで関連するモデル グループを選択するか、新しいモデル グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2346-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="f2346-114">**在庫ポリシー** クイックタブで、**検査管理** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f2346-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="f2346-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f2346-115">Close the page.</span></span>
1. <span data-ttu-id="f2346-116">入荷倉庫の **検査倉庫** フィールドで、既定の検査倉庫を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2346-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="f2346-117">倉庫で入庫済として登録された品目が、**検査管理** チェック ボックスがオンになっているモデル グループに属している場合は、システムはその検査指示を生成します。</span><span class="sxs-lookup"><span data-stu-id="f2346-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="f2346-118">検査指示は、作業員に品目を検査倉庫に移動するように指示します。</span><span class="sxs-lookup"><span data-stu-id="f2346-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="f2346-119">**検査指示** ページで検査指示を手動で作成する場合、関連する品目モデル グループで検査管理のために品目を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f2346-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="f2346-120">このプロセスでは、検査する手持在庫と、使用する検査倉庫を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2346-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="f2346-121">プロセスの計画を支援するために、検査指示のステータスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2346-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="f2346-122">検査指示のステータス</span><span class="sxs-lookup"><span data-stu-id="f2346-122">Quarantine order statuses</span></span>

<span data-ttu-id="f2346-123">検査指示には次のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="f2346-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="f2346-124">作成済み</span><span class="sxs-lookup"><span data-stu-id="f2346-124">Created</span></span>
- <span data-ttu-id="f2346-125">開始済</span><span class="sxs-lookup"><span data-stu-id="f2346-125">Started</span></span>
- <span data-ttu-id="f2346-126">完了レポート済</span><span class="sxs-lookup"><span data-stu-id="f2346-126">Reported as finished</span></span>
- <span data-ttu-id="f2346-127">終了済</span><span class="sxs-lookup"><span data-stu-id="f2346-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="f2346-128">作成済み</span><span class="sxs-lookup"><span data-stu-id="f2346-128">Created</span></span>

<span data-ttu-id="f2346-129">検査指示のステータスが **作成済** になるのは、検査指示が手動で作成されているが、まだ品目が検査倉庫に配置されていない場合です。</span><span class="sxs-lookup"><span data-stu-id="f2346-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="f2346-130">2 つの在庫トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="f2346-131">1 つ目のトランザクションは **注文中**、**引当済現物**、または **ピッキング済** のステータスがある払出トランザクションです。</span><span class="sxs-lookup"><span data-stu-id="f2346-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="f2346-132">2 つ目のトランザクションは、検査倉庫に **注文済** または **登録済** のステータスがある受入トランザクションです。</span><span class="sxs-lookup"><span data-stu-id="f2346-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="f2346-133">通常のプロセスで在庫への更新を引当、ピック、または登録できます。</span><span class="sxs-lookup"><span data-stu-id="f2346-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="f2346-134">開始済</span><span class="sxs-lookup"><span data-stu-id="f2346-134">Started</span></span>

<span data-ttu-id="f2346-135">検査指示のステータスが **開始済** になると、在庫は通常の倉庫から検査倉庫へ移動され、2 つの在庫トランザクションが生成されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="f2346-136">1 つのトランザクションには **払出済** のステータスがあり、もう一方のトランザクションには **受取済** のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="f2346-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="f2346-137">同時に、戻りの転送を処理するための 2 つの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="f2346-138">これらのトランザクションは日付がありません。</span><span class="sxs-lookup"><span data-stu-id="f2346-138">These transactions aren't dated.</span></span> <span data-ttu-id="f2346-139">1 つのトランザクションには **引当済現物** のステータスがあり、もう一方のトランザクションには **注文済** のステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="f2346-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="f2346-140">完了レポート済</span><span class="sxs-lookup"><span data-stu-id="f2346-140">Reported as finished</span></span>

<span data-ttu-id="f2346-141">開始された検査指示を完了として報告するには、注文を開き、アクション ウィンドウで **完了レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2346-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="f2346-142">品目は検査からリリースされますが、まだ通常の倉庫に戻されてはいません。</span><span class="sxs-lookup"><span data-stu-id="f2346-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="f2346-143">通常の倉庫への返送は、完了レポート プロセス時に初期化される着荷仕訳帳によって処理できます。</span><span class="sxs-lookup"><span data-stu-id="f2346-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="f2346-144">終了済</span><span class="sxs-lookup"><span data-stu-id="f2346-144">Ended</span></span>

<span data-ttu-id="f2346-145">検査指示が終了すると、品目は検査倉庫から通常の倉庫に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f2346-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="f2346-146">品目トランザクションのステータスは、検査倉庫で *売却済* に、そして通常の倉庫で *購買済* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="f2346-147">検査指示仕損</span><span class="sxs-lookup"><span data-stu-id="f2346-147">Quarantine order scrap</span></span>

<span data-ttu-id="f2346-148">検査指示のプロセスの一環として、在庫の仕損ができます。</span><span class="sxs-lookup"><span data-stu-id="f2346-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="f2346-149">仕損を処理するときは、在庫のステータスは検査倉庫からの払出トランザクションによって *売却済* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f2346-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2346-150">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f2346-150">Additional resources</span></span>

- [<span data-ttu-id="f2346-151">在庫ブロック</span><span class="sxs-lookup"><span data-stu-id="f2346-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
