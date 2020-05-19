---
title: 変動倉庫レベルの分析引当ポリシー
description: このトピックでは、製品に関連付けられている引当階層が特定のバッチの予約を許可していない場合でも、バッチ追跡製品を販売し、WMS 対応工程としてロジスティクスを実行する企業が顧客の販売注文に対して特定のバッチを予約できるようにする在庫引当のポリシーについて説明します。
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6c462a87494c434a6047542d448a85b3bce9f769
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346471"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="0e5df-103">変動倉庫レベルの分析引当ポリシー</span><span class="sxs-lookup"><span data-stu-id="0e5df-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e5df-104">「バッチ下\[場所\]」タイプの在庫引当階層が製品に関連付けられている場合は、バッチ追跡製品を販売し、Microsoft Dynamics 365 Warehouse Management System (WMS) で有効になっている工程で物流を実行する企業は、顧客の販売注文に対して特定のバッチを引当することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="0e5df-105">このトピックでは、製品が「バッチの下\[場所\]」の引当階層に関連付けられている場合でも、これらの企業が特定のバッチを予約できる在庫予約ポリシーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="0e5df-106">在庫引当階層</span><span class="sxs-lookup"><span data-stu-id="0e5df-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="0e5df-107">このセクションでは、既存の在庫引当階層の要約します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="0e5df-108">バッチ追跡品目とシリアル追跡品目の処理方法に焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="0e5df-109">在庫引当階層では、保管分析コードに関する限り、需要オーダーはサイト、倉庫、在庫ステータスの必須分析コードを保持し、倉庫ロジックは場所を要求された数量に割り当てて場所を予約する責任があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="0e5df-110">つまり、需要オーダーと倉庫工程の間の相互作用において、注文の出荷元 (つまり、サイトと倉庫) を示すように需要オーダーが求められます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="0e5df-111">倉庫では、倉庫の施設内で必要な数量を見つけるためにロジックに依存します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="0e5df-112">ただし、ビジネスの運用モデルを反映するために、追跡用分析コード (バッチ番号とシリアル番号) の方が柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="0e5df-113">在庫引当階層は、次の条件が適用されるシナリオに対応できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="0e5df-114">業務は、倉庫保管スペースで数量が検出された後、バッチまたはシリアル番号を持つ数量のピッキングを管理するために倉庫工程に依存しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="0e5df-115">このモデルは、多くの場合*バッチ下\[場所\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="0e5df-116">これは通常、製品のバッチまたはシリアル番号の ID が、販売会社に需要のある顧客にとって重要ではない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="0e5df-117">バッチ番号またはシリアル番号が顧客の注文仕様の一部であり、それらが需要オーダーに記録されている場合、倉庫内の数量を見つける倉庫操作は、特定の要求された番号によって制約され、それらを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="0e5df-118">このモデルは、*バッチ上\[場所\]* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="0e5df-119">これらのシナリオでは、各リリース製品に割り当て可能な在庫引当階層は 1 つだけであるという課題があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="0e5df-120">したがって、WMS が追跡対象の品目を処理するために、階層の割り当てがバッチまたはシリアル番号を予約する時期を決定した後 (需要オーダーを取得したとき、または倉庫ピッキング作業中)、このタイミングをアドホック基準で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="0e5df-121">バッチ追跡品目の変動引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="0e5df-122">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="0e5df-122">Business scenario</span></span>

<span data-ttu-id="0e5df-123">このシナリオでは、会社は完成品をバッチ番号で追跡する在庫戦略を使用しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="0e5df-124">この会社は、WMS ワークロードも使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="0e5df-125">このワークロードには、バッチ対応アイテムの倉庫ピッキングおよび出荷操作を計画および実行するための十分に装備されたロジックがあるため、完成したアイテムのほとんどは「バッチ下\[場所\]」在庫引当階層に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="0e5df-126">このタイプの運用設定の利点は、ピッキングするバッチや倉庫内での配置場所を決定する意思決定 (効果的な引当を決定すること) が、倉庫のピッキング工程を開始するまで延期されるという点です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="0e5df-127">顧客の注文が行われたときに作成されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="0e5df-128">「バッチ下\[場所\]」の引当階層は、会社のビジネス目標にも対応していますが、会社が獲得した顧客の多くは、製品の再注文時に以前に購入したものと同じバッチを必要とします。</span><span class="sxs-lookup"><span data-stu-id="0e5df-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="0e5df-129">したがって、この会社では、バッチ引当ルールの処理方法に関する柔軟性を模索しているため、同じ品目に対する顧客の需要に応じて次のような動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="0e5df-130">バッチ番号は、注文が販売プロセッサによって取得されるときに記録および予約することができ、倉庫行程中に変更したり、他の需要によって取得したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="0e5df-131">この動作により、注文されたバッチ番号が顧客に出荷されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="0e5df-132">顧客にとってバッチ番号が重要ではない場合、倉庫行程でピッキング作業中に、販売注文の登録と予約が完了した後、バッチ番号を決定できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="0e5df-133">販売注文の特定のバッチの引当許可</span><span class="sxs-lookup"><span data-stu-id="0e5df-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="0e5df-134">「バッチ下\[場所\]」在庫引当階層に関連付けられている品目のバッチ引当動作に必要な柔軟性を提供するには、在庫マネージャーは、**在庫引当階層**ページで**バッチ番号**レベルの**需要の引当オーダーを許可**チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![在庫引当階層を柔軟にする](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="0e5df-136">階層内の**バッチ番号**レベルが選択されている場合は、そのレベルより上で**場所**レベルまでのすべての分析コードが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="0e5df-137">(既定では、**場所**レベルの上のすべての分析コードが事前に設定されています。) この動作は、注文明細行で特定のバッチ番号を予約した後、バッチ番号と場所の間の範囲のすべての分析コードも自動的に予約されるロジックを反映しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="0e5df-138">**需要の引当オーダーを許可**チェックボックスは、倉庫の場所分析コードより下にある引当階層レベルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="0e5df-139">**バッチ番号**は、変動引当ポリシーのために開いている階層内の唯一のレベルです。</span><span class="sxs-lookup"><span data-stu-id="0e5df-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="0e5df-140">つまり、**場所**、**ライセンス プレート**、または**シリアル番号**レベルの**需要の引当オーダーを許可**チェックボックスを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="0e5df-141">引当階層にシリアル番号分析コード (常に**バッチ番号**レベル未満でなければならない) が含まれていて、バッチ番号のバッチ固有の予約をオンにした場合、システムは、「シリアル下\[場所\]」引当ポリシーに適用されるルールに基づいて、シリアル番号の予約およびピッキング操作を引き続き処理します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="0e5df-142">いつでも、展開内の既存の「バッチ下\[場所\]」引当階層にバッチ固有の予約を許可できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="0e5df-143">この変更は、変更が発生する前に作成された引当および未処理の倉庫の作業には影響しません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="0e5df-144">ただし、引当階層に関連付けられている 1 つ以上の品目に対して**引当済注文**、**引当済現物**、または**注文済**払出タイプの在庫トランザクションが存在する場合は、**需要の引当オーダーを許可**チェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="0e5df-145">品目の既存の引当階層で、注文のバッチ指定が許可されていない場合は、両方の階層で階層レベル構造が同じであることを条件として、バッチの指定が可能な引当階層に再割り当てすることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="0e5df-146">**品目の引当階層を変更**機能を使用して、再割り当てを行います。</span><span class="sxs-lookup"><span data-stu-id="0e5df-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="0e5df-147">この変更は、バッチ追跡された品目のサブセットに対する変動バッチ引当を防止し、その他の製品ポートフォリオに対して許可する場合に関連します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="0e5df-148">**需要の引当オーダーを許可**チェックボックスを選択したかどうかにかかわらず、注文明細行のアイテムに特定のバッチ番号を引き当てない場合は、「バッチ下\[場所\]」引当階層に有効な既定の倉庫行程ロジックが引き続き適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="0e5df-149">顧客注文の特定のバッチ番号の引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="0e5df-150">バッチ追跡された品目の「バッチ下\[場所\]」在庫引当階層が設定された後、注文の特定のバッチ番号を予約できるようになり、販売注文プロセッサは、顧客の要求に応じて、次のいずれかの方法で同じアイテムの顧客注文を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="0e5df-151">**バッチ番号を指定せずに注文の詳細を入力します** - このアプローチは、製品のバッチの仕様が顧客にとって重要ではない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="0e5df-152">このタイプの注文の処理に関連付けられているすべての既存のプロセスは、システムに変更されずに残ります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="0e5df-153">ユーザー側で追加の考慮事項は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="0e5df-154">**注文の詳細を入力し、特定のバッチ番号を引当** - 顧客が特定のバッチを要求する場合は、この方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="0e5df-155">通常、顧客は以前に購入した製品を再注文するときに特定のバッチを要求します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="0e5df-156">このタイプのバッチ固有の引当は、*確定済み引当*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="0e5df-157">次の一連のルールは、数量が処理されるときに有効になり、バッチ番号は特定の注文にコミットされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="0e5df-158">「バッチ下\[場所\]」引当ポリシーの下で品目の特定のバッチ番号の引当を許可するには、システムは場所まですべての分析コードを引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0e5df-159">通常、この範囲には、ライセンス プレート分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="0e5df-160">注文が確定したバッチ引当を使用する販売明細行に対してピッキング作業が作成される場合、場所ディレクティブは使用されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="0e5df-161">注文が確定したバッチの作業倉庫処理では、ユーザーもシステムもバッチ番号を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="0e5df-162">(この処理には例外処理が含まれています。)</span><span class="sxs-lookup"><span data-stu-id="0e5df-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="0e5df-163">次の例は、エンド ツー エンド フローの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0e5df-164">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="0e5df-164">Example scenario</span></span>

<span data-ttu-id="0e5df-165">この例では、**USMF** デモ データの会社を使用して、デモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="0e5df-166">在庫引当階層を設定して、バッチ固有の引当を許可する</span><span class="sxs-lookup"><span data-stu-id="0e5df-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="0e5df-167">**倉庫管理** \> **設定** \> **在庫 \> 引当階層**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="0e5df-168">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-168">Select **New**.</span></span>
3. <span data-ttu-id="0e5df-169">**名前**フィールドに、名前を入力します (たとえば、**BatchFlex**)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="0e5df-170">**説明**フィールドに、説明を入力します (たとえば、**下の変動バッチ**など)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="0e5df-171">**選択済**フィールドで、**シリアル番号**および**所有者**を選択し、左矢印ボタンを選択して**使用可能**フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="0e5df-172">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-172">Select **OK**.</span></span>
7. <span data-ttu-id="0e5df-173">**バッチ番号**分析コード レベルの行で、**需要の引当オーダーを許可**チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="0e5df-174">**ライセンス プレート**と**場所**のレベルは自動的に選択され、それらのチェックボックスをオフにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="0e5df-175">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="0e5df-176">新しくリリースされた製品の作成</span><span class="sxs-lookup"><span data-stu-id="0e5df-176">Create a new released product</span></span>

1. <span data-ttu-id="0e5df-177">次の値を使用して、製品の 3 つのマスター データ パラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="0e5df-178">**保管分析コード グループ** フィールドで、**Ware** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="0e5df-179">**追跡用分析コード グループ** フィールドで、**Batch-Phy** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="0e5df-180">**引当階層**フィールドで、**BatchFlex** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="0e5df-181">**B11** や **B22** などの 2 つのバッチ番号を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="0e5df-182">次の値を使用して、品目の数量を手持在庫に追加します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="0e5df-183">倉庫</span><span class="sxs-lookup"><span data-stu-id="0e5df-183">Warehouse</span></span> | <span data-ttu-id="0e5df-184">バッチ番号</span><span class="sxs-lookup"><span data-stu-id="0e5df-184">Batch number</span></span> | <span data-ttu-id="0e5df-185">保管場所</span><span class="sxs-lookup"><span data-stu-id="0e5df-185">Location</span></span> | <span data-ttu-id="0e5df-186">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="0e5df-186">License plate</span></span> | <span data-ttu-id="0e5df-187">件数</span><span class="sxs-lookup"><span data-stu-id="0e5df-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="0e5df-188">24</span><span class="sxs-lookup"><span data-stu-id="0e5df-188">24</span></span>        | <span data-ttu-id="0e5df-189">B11</span><span class="sxs-lookup"><span data-stu-id="0e5df-189">B11</span></span>          | <span data-ttu-id="0e5df-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="0e5df-190">BULK-001</span></span> | <span data-ttu-id="0e5df-191">なし</span><span class="sxs-lookup"><span data-stu-id="0e5df-191">None</span></span>          | <span data-ttu-id="0e5df-192">10</span><span class="sxs-lookup"><span data-stu-id="0e5df-192">10</span></span>       |
    | <span data-ttu-id="0e5df-193">24</span><span class="sxs-lookup"><span data-stu-id="0e5df-193">24</span></span>        | <span data-ttu-id="0e5df-194">B11</span><span class="sxs-lookup"><span data-stu-id="0e5df-194">B11</span></span>          | <span data-ttu-id="0e5df-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="0e5df-195">FL-001</span></span>   | <span data-ttu-id="0e5df-196">LP11</span><span class="sxs-lookup"><span data-stu-id="0e5df-196">LP11</span></span>          | <span data-ttu-id="0e5df-197">10</span><span class="sxs-lookup"><span data-stu-id="0e5df-197">10</span></span>       |
    | <span data-ttu-id="0e5df-198">24</span><span class="sxs-lookup"><span data-stu-id="0e5df-198">24</span></span>        | <span data-ttu-id="0e5df-199">B22</span><span class="sxs-lookup"><span data-stu-id="0e5df-199">B22</span></span>          | <span data-ttu-id="0e5df-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="0e5df-200">FL-002</span></span>   | <span data-ttu-id="0e5df-201">LP22</span><span class="sxs-lookup"><span data-stu-id="0e5df-201">LP22</span></span>          | <span data-ttu-id="0e5df-202">10</span><span class="sxs-lookup"><span data-stu-id="0e5df-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="0e5df-203">販売注文詳細の入力</span><span class="sxs-lookup"><span data-stu-id="0e5df-203">Enter sales order details</span></span>

1. <span data-ttu-id="0e5df-204">**販売とマーケティング** \> **販売注文** \> **すべての販売注文**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="0e5df-205">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-205">Select **New**.</span></span>
3. <span data-ttu-id="0e5df-206">販売注文ヘッダーの**顧客 ID** フィールドに、**US-003** と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="0e5df-207">新規の品目の明細行を追加し、数量として **10** を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="0e5df-208">**倉庫**フィールドが **24** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="0e5df-209">**販売注文明細行**クイック タブで**在庫**を選択し、**管理**グループで**バッチ引当**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="0e5df-210">**バッチ引当**ページに、注文明細行の引当に使用できるバッチのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="0e5df-211">この例では、バッチ番号 **B11** の場合は **20** の数量、バッチ番号 **B22** の場合は **10** の数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="0e5df-212">バッチ固有の引当を許可するように設定されていない限り、その行の品目が「バッチ下\[場所\]」引当階層に関連付けられている場合、**バッチ引当**ページにアクセスできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e5df-213">販売注文の特定のバッチを引当するには、**バッチ引当**ページを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="0e5df-214">販売注文明細行にバッチ番号を直接入力すると、「バッチ下\[場所\]」の引当ポリシーの対象となる品目に対して特定のバッチ値を入力した場合と同じようにシステムが動作します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="0e5df-215">明細行を保存すると、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="0e5df-216">バッチ番号が注文明細行に直接指定されていることを確認した場合、その明細行は、通常の倉庫管理ロジックで処理されることはありません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="0e5df-217">**引当**ページの数量を引当すると、特定のバッチは引当されず、その行の倉庫操作の実行は、「バッチ下\[場所\]」の引当ポリシーの下で適用されるルールに従います。</span><span class="sxs-lookup"><span data-stu-id="0e5df-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="0e5df-218">一般に、このページは「バッチ上\[場所\]」タイプの引当階層が関連付けられている品目に対して機能し、同じ方法で連携されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="0e5df-219">ただし、次の例外が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="0e5df-220">**ソース明細行に確定済みのバッチ番号**クイック タブには、注文明細行に対して引き当てられているバッチ番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="0e5df-221">グリッドのバッチ値は、倉庫処理ステージを含む注文明細行のフルフィルメント サイクル全体で表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="0e5df-222">対照的に、**概要**クイックタブでは、通常の注文明細行の引当 (**場所**レベルの上にある分析コードに対して実行される引当) は、倉庫作業が作成される時点までグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="0e5df-223">その後、作業エンティティは明細行の引当を引き継ぎ、明細行の引当はページに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="0e5df-224">**ソース明細行に確定済みのバッチ番号**クイック タブは、販売注文プロセッサが、請求まで、ライフサイクルの任意の時点で顧客の注文に対して確定されたバッチ番号を表示できるようにするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="0e5df-225">特定のバッチの引当に加えて、ユーザーはシステムによって自動的に選択させる代わりに、バッチの特定の場所とライセンス プレートを手動で選択できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="0e5df-226">この機能は、注文が確定したバッチ引当メカニズムの設計に関連しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="0e5df-227">前述のように、バッチ番号が「バッチ下\[場所\]」引当ポリシーの品目で引当されている場合、システムはすべての分析コードを場所まで引当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="0e5df-228">したがって、倉庫作業では、注文を処理したユーザーによって予約されたものと同じ保管分析コードが使用され、ピッキング行程に便利な、または可能な品目保管場所を常に表すとは限りません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="0e5df-229">注文処理担当者が倉庫の制約を認識している場合、バッチを予約する際に特定の場所とライセンス プレートを手動で選択することができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="0e5df-230">この場合、ユーザーはページ ヘッダーの**分析コードの表示**機能を使用し、**概要** クイック タブのグリッドに場所とライセンス プレートを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="0e5df-231">**バッチ引当**ページで、バッチ **B11** の明細行を選択し、**引当行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="0e5df-232">自動引当中に場所とライセンス プレートを割り当てるための指定されたロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="0e5df-233">**引当**フィールドに手動で数量を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="0e5df-234">**ソース明細行に確定済みのバッチ番号**クイック タブでは、バッチ **B11** が**確定済み**として表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![バッチ引当ページの特定のバッチ番号を販売注文明細行にコミットする](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="0e5df-236">販売注文明細行の数量の引当は、複数のバッチ間で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="0e5df-237">同様に、複数の場所およびライセンス プレートに対して同じバッチの引当を行うことができます (その場所でライセンス プレートが有効になっている場合)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="0e5df-238">販売注文明細行の数量に対する特定のバッチの引当も部分的に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="0e5df-239">たとえば、100 単位の合計数量を引当して、特定のバッチを 20 単位にコミットし、80 単位を使用可能なバッチのサイトおよび倉庫レベルで引当できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="0e5df-240">この場合、WMS は 2 つの異なる作業明細行を使用してピッキング工程を処理します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="0e5df-241">**製品情報管理** \> **製品** \> **リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="0e5df-242">品目を選択し、**在庫の管理** \> **表示** \> **トランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![在庫トランザクション タイプとして確定済み引当](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="0e5df-244">販売注文明細行の引当に関連する品目の在庫トランザクションを確認します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="0e5df-245">**参照**フィールドが**販売注文**に設定され、**払出**フィールドが**引当済現物**に設定されているトランザクションは、**場所**レベルより上の在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="0e5df-246">品目の在庫引当階層に従って、これらの分析コードは、サイト、倉庫、および在庫状態になります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="0e5df-247">**参照**フィールドが**確定済み引当**に設定され、**払出**フィールドが**引当済現物**に設定されているトランザクションは、特定のバッチおよびその上のすべての在庫分析コードの注文明細行の引当を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="0e5df-248">品目の在庫引当階層に従って、これらの分析コードは、バッチ番号および場所になります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="0e5df-249">この例では、この場所は **Bulk-001** です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="0e5df-250">販売注文ヘッダーで、**倉庫** \> **アクション** \> **倉庫にリリース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="0e5df-251">注文明細行がウェーブ処理され、積荷と作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="0e5df-252">注文が確定したバッチ番号を持つ倉庫作業の確認および処理</span><span class="sxs-lookup"><span data-stu-id="0e5df-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="0e5df-253">**販売注文明細行**クイック タブで、**倉庫** \> **作業の詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="0e5df-254">販売注文明細行に確定されているバッチの数量のピッキング工程を処理する作業には、次のような特性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="0e5df-255">作業を作成するには、作業テンプレートを使用しますが、場所ディレクティブは使用しません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="0e5df-256">いつ新しい作業を作成するかを決定するために、ピッキング明細行の最大数や特定の測定単位など、作業テンプレートに定義されているすべての標準設定が適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="0e5df-257">ただし、確定済み引当ではすべての在庫分析コードが既に指定されているため、ピッキング場所を識別するための場所ディレクティブに関連付けられているルールは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="0e5df-258">これらの在庫分析コードには、倉庫の保管レベルの分析コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="0e5df-259">したがって、作業では、場所ディレクティブを参照することなく、これらの分析コードが継承されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="0e5df-260">バッチ番号は、ピッキング行には表示されません。(「バッチ上\[場所\]」の引当階層が関連付けられている品目に対して作成される作業明細行と同様です) 代わりに、「開始」バッチ番号と他のすべての保管分析コードが、関連付けられている在庫トランザクションから参照されている作業明細行の作業在庫トランザクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![注文が確定した引当によって発生した作業の倉庫在庫トランザクション](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="0e5df-262">作業が作成されると、**参照**フィールドが**確定済み引当**に設定されている品目の在庫トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="0e5df-263">**参照**フィールドが**作業**に設定されている在庫トランザクションは、すべての数量の在庫分析コードに対して現物引当を保持するようになりました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="0e5df-264">倉庫工程は、作業の実行を通常の方法で処理することができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="0e5df-265">ただし、モバイル デバイスの指示では、特定のバッチ番号を選択するよう作業者に指示します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="0e5df-266">場所がライセンス プレートにより制御されている倉庫環境では、複数のライセンス プレートで同じバッチが保管されている場所に作業者が到達した後、まだ引当されていないライセンス プレートから選択できます (たとえば、別の確定済み引当またはそのタイプの引当から発生する作業による)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="0e5df-267">作業明細行で指定された場所からのピッキングが実際的ではない場合、倉庫オペレーターは次のいずれかのアクションを使用して、特定のバッチのピッキングをより便利な場所からリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="0e5df-268">モバイル デバイスでの標準の**場所の上書き**アクション (倉庫作業者の**ピッキング場所の上書きを許可**設定が有効になっている場合)</span><span class="sxs-lookup"><span data-stu-id="0e5df-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="0e5df-269">**作業一覧詳細**ページでの**場所の変更**アクション。</span><span class="sxs-lookup"><span data-stu-id="0e5df-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="0e5df-270">モバイル デバイスで、ピッキングと作業の配置を完了します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="0e5df-271">バッチ番号 **B11** の数量 **10** が販売注文明細行に対してピッキングされ、**ベイドア**の場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="0e5df-272">この時点で、トラックに積載して、顧客の住所に出荷する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="0e5df-273">注文が確定したバッチ番号を持つ倉庫作業の例外処理</span><span class="sxs-lookup"><span data-stu-id="0e5df-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="0e5df-274">注文が確定したバッチ番号をピッキングする倉庫作業には、通常の作業と同じ標準の倉庫例外処理とアクションが適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="0e5df-275">一般に、オープン作業または作業明細行はキャンセルされたり、ユーザーの場所がいっぱいになったために中断されたり、ショート ピッキングされたり、移動のために更新される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="0e5df-276">同様に、既に完了した作業のピッキング済数量を減らすことも、または作業を取り消すこともできます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="0e5df-277">これらのすべての例外処理アクションに次の主要なルールが適用されます。顧客に対して引当されているバッチ番号を別のバッチ番号に置き換えられることはありませんが、保管分析コード　(場所およびライセン スプレート) は、ユーザーによる手動更新またはシステムによる自動更新によって変更できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="0e5df-278">自動更新は、特定のバッチが自動的に引当され、保管分析コードが指定されていない場合に適用される保管分析コードのランダムな割り当てに基づいています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="0e5df-279">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="0e5df-279">Example scenario</span></span>

<span data-ttu-id="0e5df-280">このシナリオの例としては、**ピッキング済数量の削減**機能を使用して、以前に完了した作業を解除している状況です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="0e5df-281">この例は、このトピックの前の例の続きです。</span><span class="sxs-lookup"><span data-stu-id="0e5df-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="0e5df-282">**倉庫管理** \> **積荷** \> **有効な積荷**に移動します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="0e5df-283">販売注文の出荷に関連して作成された積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="0e5df-284">**積荷注文明細行数**クイック タブから、**ピッキング済数量の削減**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="0e5df-285">**ピッキング済数量の削減**ページの**場所に移動する**フィールドで、**FL-001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="0e5df-286">**ライセンス プレートに移動する**フィールドで、**LP33** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="0e5df-287">グリッドで、**ピッキングを解除する在庫数量**フィールドに **10** と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="0e5df-288">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-288">Select **OK**.</span></span>

<span data-ttu-id="0e5df-289">ピッキング解除アクションの実行結果は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="0e5df-290">以前に終了した作業のステータスは、**キャンセル済**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="0e5df-291">バッチ番号 **B11** の **10** のピッキング済ではない数量に対して、**在庫移動**タイプの新しい作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0e5df-292">この作業は、**ベイドア**の場所から、**FL-001** の場所のライセンス プレート **LP33** への移動を表しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="0e5df-293">ステータスは**終了済**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="0e5df-294">システムは、元の注文バッチ番号を再度準備し、場所とライセンス プレート ID を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="0e5df-295">(このプロセスは、指定されたバッチ番号の注文明細行に対して**引当行**機能を実行することと同じです)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="0e5df-296">その結果、バッチ **B11** は、**バッチ引当**ページの**ソース明細行に確定済みのバッチ番号**クイック タブに確定済みとして表示され、**引当**フィールドには、バッチ番号 **B11** の数量 **10** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="0e5df-297">さらに、**場所**フィールドは **FL-001** に設定され、**ライセンス プレート** フィールドは **LP11** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="0e5df-298">(これらのフィールドが表示されていない場合は、グリッドに追加できます。)</span><span class="sxs-lookup"><span data-stu-id="0e5df-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="0e5df-299">次の表は、特定の倉庫アクションの注文が確定したバッチ引当をシステムが処理する方法を示す概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="0e5df-300">テーブルのコンテンツを解釈するには、各倉庫アクションが注文が確定したバッチ引当から発生する既存の倉庫作業のコンテキストで実行されるか、各倉庫アクションの実行がそのタイプの作業に影響すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="0e5df-301">これらの表の「バッチ数量が利用可能」列は、現在の注文が確定した引当に対して既に引当されている数量、またはそのタイプの引当から発生する倉庫作業によって既に引当されている数量に加えて、バッチ数量が利用可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="0e5df-302">オープン作業のピッキング場所を上書きする</span><span class="sxs-lookup"><span data-stu-id="0e5df-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-303">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-304">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-305">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-305">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-306">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-306">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-307">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-308">作業者で<strong>ピッキング場所の上書きを許可</strong>オプションが有効になっている。</span><span class="sxs-lookup"><span data-stu-id="0e5df-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0e5df-309">有</span><span class="sxs-lookup"><span data-stu-id="0e5df-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-310">ピッキング作業開始時に、倉庫アプリの <strong>場所の上書き</strong> メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-310">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="0e5df-311"><strong>提案</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="0e5df-312">バッチ数量の使用可能性に基づいて提案される新しい場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-313">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0e5df-314">ピッキング行の場所が新しい場所に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="0e5df-315">(場所がライセンス プレートにより制御されている場合、ランダムなライセンス プレートが作業在庫トランザクションに割り当てられ、作業者は使用可能な数量があるライセンス プレートからピッキングできます。)</span><span class="sxs-lookup"><span data-stu-id="0e5df-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="0e5df-316">新しい場所で複数のライセンス プレートに数量が見つかった場合、元のピッキング行を複数の行に分割して、各ライセンス プレートに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-317">該当なし</span><span class="sxs-lookup"><span data-stu-id="0e5df-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-318">無</span><span class="sxs-lookup"><span data-stu-id="0e5df-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-319">ピッキング作業開始時に、倉庫アプリの <strong>場所の上書き</strong> メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-319">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="0e5df-320">場所を手動で入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-321"><strong>場所の上書き</strong>アクションは実行できません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="0e5df-322">失敗すると、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0e5df-323">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="0e5df-324">フル ボタン - ユーザーの場所でオーバーフローしたために作業ラインを分割します</span><span class="sxs-lookup"><span data-stu-id="0e5df-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-325">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-326">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-327">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-327">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-328">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-328">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-329">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0e5df-330">モバイル デバイスのメニュー項目で<strong>作業の分割を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="0e5df-331">該当なし</span><span class="sxs-lookup"><span data-stu-id="0e5df-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-332">ピッキング作業プロセス時に、倉庫アプリのメニュー項目 <strong>フル</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-332">Select the <strong>Full</strong> menu item on the warehousing app when you process picking work.</span></span></li>
<li><span data-ttu-id="0e5df-333"><strong>ピッキング数量</strong>フィールドに、必要なピッキングの一部の数量を入力して、全能力を示します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-334">現在の作業では、数量はピッキングが必要な残余数量に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="0e5df-335">選択した数量の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="0e5df-336">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="0e5df-337">完了した作業のピッキング済数量をする (積荷から)</span><span class="sxs-lookup"><span data-stu-id="0e5df-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-338">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-339">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-340">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-340">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-341">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-341">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-342">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-343">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-343">Not applicable</span></span></td>
<td><span data-ttu-id="0e5df-344">はい</span><span class="sxs-lookup"><span data-stu-id="0e5df-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-345">積荷明細行から<strong>ピッキング済数量の削減</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="0e5df-346">ピッキングを解除する全数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="0e5df-347">「移動先」の場所 / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="0e5df-348">積荷明細行に関連付けられている作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="0e5df-349">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-350">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-351">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-352">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-352">No</span></span></td>
<td><span data-ttu-id="0e5df-353">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-353">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-354">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-354">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-355">数量は、ピッキング中に入力された同じバッチ、および同じ場所、およびライセンス プレート (場所がライセンス プレートで制御されている場合) に対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="0e5df-356">倉庫内の品目を移動する</span><span class="sxs-lookup"><span data-stu-id="0e5df-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="0e5df-357">この倉庫アクションは、**作業作成プロセス** タイプの移動にのみ適用され、テンプレートによる移動には適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-358">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-359">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-360">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-360">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-361">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-361">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-362">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-363">作業者で、<strong>作業が関連付けられている在庫の移動を許可</strong>オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0e5df-364">有</span><span class="sxs-lookup"><span data-stu-id="0e5df-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-365">倉庫アプリで移動を開始します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-365">Start a movement on the warehousing app.</span></span></li>
<li><span data-ttu-id="0e5df-366">「移動元」および「移動先」の場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="0e5df-367">移動によって影響を受けるすべての既存の作業について、ピッキング場所が新しい「移動先」の場所に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="0e5df-368">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-369">特定の場所からの数量の移動によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-370">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-371">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-371">No</span></span></td>
<td><span data-ttu-id="0e5df-372">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-372">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-373">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-373">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-374">特定の場所からの数量の移動によって影響を受けるすべての既存の引当は、同じバッチ、および新しい「移動先」場所とライセンス プレートに対して再引当されます (場所がライセンス プレートで制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="0e5df-375">完了した作業のピッキング済数量を取り消す (積荷もしくはウェーブから)</span><span class="sxs-lookup"><span data-stu-id="0e5df-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-376">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-377">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-378">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-378">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-379">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-379">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-380">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="0e5df-381">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-381">Not applicable</span></span></td>
<td><span data-ttu-id="0e5df-382">はい</span><span class="sxs-lookup"><span data-stu-id="0e5df-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-383"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0e5df-384">要求ページで、<strong>品目を現在の場所に配置したままにする</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-385">積荷に関連付けられているすべての作業はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="0e5df-386">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-387">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-388">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-388">No</span></span></td>
<td><span data-ttu-id="0e5df-389">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-389">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-390">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-390">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-391">数量は、同じバッチ、および取消時に数量が残された場所とライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-392">はい</span><span class="sxs-lookup"><span data-stu-id="0e5df-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-393"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0e5df-394">要求ページで、<strong>品目をこの場所に割り当てる</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-395">現在の作業はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="0e5df-396">在庫移動の新しい作業が作成され、決済されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-397">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-398">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-399">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-399">No</span></span></td>
<td><span data-ttu-id="0e5df-400">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-400">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-401">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-401">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-402">数量は、同じバッチ、および取消時に数量が割り当てられた場所とライセンス プレートに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-403">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-404"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0e5df-405">要求ページで、<strong>品目をこの場所に移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-406">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="0e5df-407">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-408">はい/いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-409"><strong>作業を取消</strong>ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="0e5df-410">要求ページで、<strong>場所のディレクティブに基づいて品目を移動する</strong>オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-411">取消はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="0e5df-412">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="0e5df-413">数量の選択 - ピッキング作業の実行中に、場所 / ライセンス プレートでは見つからない数量を登録する</span><span class="sxs-lookup"><span data-stu-id="0e5df-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-414">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-415">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-416">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-416">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-417">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-417">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-418">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-419"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="0e5df-420">有</span><span class="sxs-lookup"><span data-stu-id="0e5df-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-421">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-421">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-422"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-423"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-424">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0e5df-425"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-426">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-427">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-428">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-428">No</span></span></td>
<td><span data-ttu-id="0e5df-429">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0e5df-430">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="0e5df-431">現在の作業は開いたままになります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-432">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-433"><strong>品目再配賦</strong> = <strong>なし</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="0e5df-434">有</span><span class="sxs-lookup"><span data-stu-id="0e5df-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-435">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-435">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-436"><strong>ピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-437"><strong>理由</strong>フィールドに、<strong>非再配賦</strong>と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-438">現在の作業は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0e5df-439"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-440">簡単なピッキング場所からの数量の調整によって影響を受けるすべての既存の引当は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-441">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-442">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-442">No</span></span></td>
<td><span data-ttu-id="0e5df-443">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-443">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-444">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-444">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-445">簡単なピッキング場所からの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-446"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ / はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="0e5df-447">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0e5df-448">有</span><span class="sxs-lookup"><span data-stu-id="0e5df-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-449">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-449">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-450"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-451"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0e5df-452">一覧から場所 / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-453">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0e5df-454">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0e5df-455">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="0e5df-456">新しいピック行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-456">A new pick line is created.</span></span> <span data-ttu-id="0e5df-457">ユーザーによって選択された場所 / ライセンス プレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="0e5df-458">新しいプット明細行が作成されました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0e5df-459"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-460">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-461"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="0e5df-462">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0e5df-463">無</span><span class="sxs-lookup"><span data-stu-id="0e5df-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-464">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-464">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-465"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-466"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-467">ショートピッキング アクションの実行に失敗し、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="0e5df-468">適用できません</span><span class="sxs-lookup"><span data-stu-id="0e5df-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-469"><strong>品目再配賦</strong> = <strong>手動</strong>、<strong>在庫の調整</strong> = <strong>はい</strong>、および<strong>引当の削除</strong> = <strong>はい</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="0e5df-470">さらに、作業者で<strong>手動による再配置を許可</strong>オプションが有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="0e5df-471">無</span><span class="sxs-lookup"><span data-stu-id="0e5df-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-472">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-472">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-473"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-474"><strong>理由</strong>フィールドで、<strong>手動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="0e5df-475">一覧から場所 / ライセンス プレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="0e5df-476">現在の作業では、次のアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="0e5df-477">ピッキング行は終了済で、ピッキング済数量は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="0e5df-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="0e5df-478">プット明細行はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0e5df-479"><strong>棚卸</strong>タイプの在庫トランザクションおよび<strong>売却</strong>出庫タイプの在庫トランザクションが作成され、調整を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="0e5df-480">簡単なピッキング場所 / ライセンス プレートからの数量の調整によって影響を受けるすべての既存の引当は、削除されました。</span><span class="sxs-lookup"><span data-stu-id="0e5df-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-481"><strong>品目再配賦</strong> = <strong>自動</strong>、<strong>在庫の調整</strong> = <strong>はい / いいえ</strong>、および<strong>引当の削除</strong> = <strong>はい / いいえ</strong>で、<strong>ショートピック</strong> タイプの作業例外が設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="0e5df-482">該当なし</span><span class="sxs-lookup"><span data-stu-id="0e5df-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-483">ピッキング作業のプロセス時に、倉庫アプリのメニュー項目 <strong>ショート ピック</strong> を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-483">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="0e5df-484"><strong>ショートピック数量</strong>フィールドに <strong>0</strong> (ゼロ) と入力します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="0e5df-485"><strong>理由</strong>フィールドで、<strong>自動での再配分を使用したショートピッキング</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-486">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="0e5df-487">自動再割り当てを含むショートピッキングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="0e5df-488">在庫状態の変更</span><span class="sxs-lookup"><span data-stu-id="0e5df-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="0e5df-489">この倉庫アクションは複数のエントリ ポイントから実行できます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="0e5df-490">ここに表示されている例では、**保管場所ごとの手持在庫**ページで**在庫状態の変更**アクションを使用しています。</span><span class="sxs-lookup"><span data-stu-id="0e5df-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0e5df-491">キー設定パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e5df-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="0e5df-492">バッチ数量が利用可能</span><span class="sxs-lookup"><span data-stu-id="0e5df-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="0e5df-493">主要なユーザーの手順</span><span class="sxs-lookup"><span data-stu-id="0e5df-493">Key user steps</span></span></th>
<th><span data-ttu-id="0e5df-494">倉庫作業</span><span class="sxs-lookup"><span data-stu-id="0e5df-494">Warehouse work</span></span></th>
<th><span data-ttu-id="0e5df-495">注文が確定したバッチ引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-496"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>引当</strong>または<strong>マーキングと引当</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="0e5df-497">はい</span><span class="sxs-lookup"><span data-stu-id="0e5df-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-498">特定の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="0e5df-499">特定の品目、場所、およびライセンス プレートがある明細行を選択します (場所がライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0e5df-500"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0e5df-501"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-502">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0e5df-503">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-504">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="0e5df-505"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0e5df-506">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-507">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-507">No</span></span></td>
<td><span data-ttu-id="0e5df-508">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-508">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-509">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="0e5df-510">引当が削除されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="0e5df-511"><strong>在庫状態の変更</strong>タイプの 2 つの在庫トランザクションを作成して、在庫状態分析コードの変更を表します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="0e5df-512">ブロックされた数量の引き当てを表すために、<strong>在庫ブロック</strong>タイプおよび<strong>引当済現物</strong>払出タイプの在庫トランザクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="0e5df-513"><strong>倉庫</strong>タブの<strong>倉庫</strong>レコードで、<strong>引当とマーキングの削除</strong>フィールドが<strong>なし</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="0e5df-514">はい</span><span class="sxs-lookup"><span data-stu-id="0e5df-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="0e5df-515">特定の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="0e5df-516">特定の品目、場所、およびライセンス プレートがある明細行を選択します (場所がライセンス プレートにより制御されている場合)。</span><span class="sxs-lookup"><span data-stu-id="0e5df-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="0e5df-517"><strong>在庫状態の変更</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="0e5df-518"><strong>在庫状態</strong>フィールドを<strong>ブロック</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e5df-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="0e5df-519">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0e5df-520">この数量は、同じバッチに対して再引当されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="0e5df-521">システムは、数量が使用可能な場所とライセンス プレート (場所がライセンス プレートで制御されている場合) をランダムに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0e5df-522">いいえ</span><span class="sxs-lookup"><span data-stu-id="0e5df-522">No</span></span></td>
<td><span data-ttu-id="0e5df-523">前の行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e5df-523">See the previous row.</span></span></td>
<td><span data-ttu-id="0e5df-524">作業用に引き当てられている数量に対して、在庫状態の変更は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="0e5df-525">在庫状態の変更は許可されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="0e5df-526">制限</span><span class="sxs-lookup"><span data-stu-id="0e5df-526">Limitations</span></span>

- <span data-ttu-id="0e5df-527">変動倉庫のレベルの分析コード引当機能では、次の機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="0e5df-528">CW 管理</span><span class="sxs-lookup"><span data-stu-id="0e5df-528">Catch weight management</span></span>
    - <span data-ttu-id="0e5df-529">現物マイナス在庫</span><span class="sxs-lookup"><span data-stu-id="0e5df-529">Physical negative inventory</span></span>
    - <span data-ttu-id="0e5df-530">注文供給に対する引当</span><span class="sxs-lookup"><span data-stu-id="0e5df-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="0e5df-531">移動オーダーおよび原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="0e5df-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="0e5df-532">ディレクティブ単位での梱包のためのコンテナー連結ルールには、制限があります。</span><span class="sxs-lookup"><span data-stu-id="0e5df-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="0e5df-533">注文が確定された引当では、**ディレクティブ単位別の梱包**フィールドが有効になっているコンテナー構築テンプレートを使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0e5df-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="0e5df-534">現在の設計では、倉庫作業の作成時に場所ディレクティブは使用されません。</span><span class="sxs-lookup"><span data-stu-id="0e5df-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="0e5df-535">したがって、コンテナー詰めのウェーブ ステップ中には、単位順序グループ (在庫単位) の最小単位のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="0e5df-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
