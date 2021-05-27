---
title: 倉庫在庫調整
description: このトピックでは、倉庫在庫調整仕訳帳と Scale Unit を使用している場合の処理に関する情報を提供します。
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026136"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="9efe1-103">倉庫在庫調整</span><span class="sxs-lookup"><span data-stu-id="9efe1-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9efe1-104">倉庫在庫調整機能は、[製造ワークロード](cloud-edge-workload-manufacturing.md)および[倉庫管理ワークロード](cloud-edge-workload-warehousing.md)に対してクラウドおよびエッジのスケール ユニットを実行している場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="9efe1-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="9efe1-105">作業者が、スケール ユニットの倉庫管理ワークロードに対して倉庫アプリを使用して在庫調整を行う場合、物理的な手動更新は、**倉庫管理 > 定期処理のタスク > 倉庫在庫調整仕訳帳** に移動して実行およびスケジュールする **倉庫在庫調整仕訳帳** バッチ ジョブにより処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9efe1-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="9efe1-106">現在、次の倉庫アプリの作業プロセスは、スケール ユニット ワークロード上で **倉庫在庫調整仕訳帳** を使用しています。</span><span class="sxs-lookup"><span data-stu-id="9efe1-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="9efe1-107">調整 入/出</span><span class="sxs-lookup"><span data-stu-id="9efe1-107">Adjustment in/out</span></span>
- <span data-ttu-id="9efe1-108">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="9efe1-108">Cycle counting</span></span>
- <span data-ttu-id="9efe1-109">ライセンス プレートの読み込み</span><span class="sxs-lookup"><span data-stu-id="9efe1-109">License plate loading</span></span>

<span data-ttu-id="9efe1-110">ハブおよびスケール ユニットの展開は在庫レコードを共有するので、各在庫トランザクションがクラウドおよびエッジの在庫調整処理の一部として作成されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="9efe1-111">在庫調整の例</span><span class="sxs-lookup"><span data-stu-id="9efe1-111">Inventory adjustment example</span></span>

<span data-ttu-id="9efe1-112">この例では、倉庫作業者は倉庫アプリを使用して、手持在庫の追加を登録しました。</span><span class="sxs-lookup"><span data-stu-id="9efe1-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="9efe1-113">最初に、スケール ユニットのワークロードは正の物理的な調整に対して倉庫在庫調整トランザクションを作成してハブと同期させ、それによりハブ上の手持在庫は増加します。</span><span class="sxs-lookup"><span data-stu-id="9efe1-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="9efe1-114">種類</span><span class="sxs-lookup"><span data-stu-id="9efe1-114">Type</span></span>                                    | <span data-ttu-id="9efe1-115">スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="9efe1-115">Scale unit</span></span> | <span data-ttu-id="9efe1-116">方向</span><span class="sxs-lookup"><span data-stu-id="9efe1-116">Direction</span></span> | <span data-ttu-id="9efe1-117">ハブ</span><span class="sxs-lookup"><span data-stu-id="9efe1-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="9efe1-118">倉庫在庫調整</span><span class="sxs-lookup"><span data-stu-id="9efe1-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="9efe1-119">+1</span><span class="sxs-lookup"><span data-stu-id="9efe1-119">+1</span></span>         | ->        | <span data-ttu-id="9efe1-120">+1</span><span class="sxs-lookup"><span data-stu-id="9efe1-120">+1</span></span>  |

<span data-ttu-id="9efe1-121">その後、[メッセージ プロセッサ メッセージ](cloud-edge-message-processor-messages.md)を通して受信される棚卸仕訳帳の転記が処理されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="9efe1-122">これにより、追加の手持在庫が更新されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="9efe1-123">二重の手持在庫を回避するために、ハブはこのプロセスの一部として相殺トランザクションを作成し、以前に記録され、倉庫在庫調整に関連付けられている手持在庫を削除します。</span><span class="sxs-lookup"><span data-stu-id="9efe1-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="9efe1-124">種類</span><span class="sxs-lookup"><span data-stu-id="9efe1-124">Type</span></span>                                    | <span data-ttu-id="9efe1-125">スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="9efe1-125">Scale unit</span></span> | <span data-ttu-id="9efe1-126">方向</span><span class="sxs-lookup"><span data-stu-id="9efe1-126">Direction</span></span> | <span data-ttu-id="9efe1-127">ハブ</span><span class="sxs-lookup"><span data-stu-id="9efe1-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="9efe1-128">棚卸</span><span class="sxs-lookup"><span data-stu-id="9efe1-128">Counting</span></span>                                | <span data-ttu-id="9efe1-129">+1</span><span class="sxs-lookup"><span data-stu-id="9efe1-129">+1</span></span>         | <-        | <span data-ttu-id="9efe1-130">+1</span><span class="sxs-lookup"><span data-stu-id="9efe1-130">+1</span></span>  |
| <span data-ttu-id="9efe1-131">倉庫在庫調整 (相殺)</span><span class="sxs-lookup"><span data-stu-id="9efe1-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="9efe1-132">-1</span><span class="sxs-lookup"><span data-stu-id="9efe1-132">-1</span></span>         | <-        | <span data-ttu-id="9efe1-133">-1</span><span class="sxs-lookup"><span data-stu-id="9efe1-133">-1</span></span>  |

<span data-ttu-id="9efe1-134">スケール ユニットがハブ上で **倉庫在庫調整仕訳帳** を作成した後、調整処理の一部としてハブが作成した **棚卸仕訳帳** と **相殺仕訳帳** の両方を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="9efe1-135">次の手順を実行することにより、Supply Chain Management の各仕訳入力とトランザクションを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="9efe1-136">Scale Unit にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9efe1-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="9efe1-137">**倉庫管理 \> 定期タスク \> 倉庫在庫調整仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9efe1-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="9efe1-138">**倉庫在庫調整仕訳帳** ページで、手持在庫の変更を記録した仕訳帳を検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="9efe1-139">**仕訳帳明細行** セクションには、この仕訳帳によって記録された各調整が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="9efe1-140">ハブにサインインします。</span><span class="sxs-lookup"><span data-stu-id="9efe1-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="9efe1-141">**倉庫管理 \> 定期タスク \> 倉庫在庫調整仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9efe1-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="9efe1-142">ハブとスケール ユニットが同期されている場合、**倉庫在庫調整仕訳帳** ページには同じ仕訳帳が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="9efe1-143">仕訳帳を開きます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-143">Open the journal.</span></span> <span data-ttu-id="9efe1-144">[メッセージ プロセッサ メッセージ](cloud-edge-message-processor-messages.md)が処理されている場合、ヘッダーに **棚卸仕訳帳** と **相殺仕訳帳** へのリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="9efe1-145">**棚卸仕訳帳** には、仕訳帳明細行と同じ分析コード値が表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9efe1-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="9efe1-146">**相殺仕訳帳** には、二重の在庫調整を削除する相殺が表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9efe1-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="9efe1-147">同期と処理がすべて完了したとき、**棚卸仕訳帳** と **相殺仕訳帳** がスケール ユニットに同期されます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="9efe1-148">これらは、関連する **倉庫在庫調整仕訳帳** ページから表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="9efe1-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
